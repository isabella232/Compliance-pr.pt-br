---
title: 'Resiliência de dados do SharePoint e OneDrive no Microsoft 365 '
description: Este artigo fornece uma visão geral da SharePoint e OneDrive resiliência de dados no Microsoft 365.
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
f1.keywords:
- NOCSH
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 8b2c0cea5ea9af46b947fe8e3f76a8c17bd86494837073be77e1c7894270e97b
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/05/2021
ms.locfileid: "54292069"
---
# <a name="sharepoint-and-onedrive-data-resiliency-in-microsoft-365"></a>Resiliência de dados do SharePoint e OneDrive no Microsoft 365 

Dentro Microsoft 365, OneDrive é criado sobre a plataforma de arquivos SharePoint de arquivo. Neste artigo, somente SharePoint serão usados para se referir a ambos os produtos. O conteúdo deste artigo é relevante para Microsoft 365 e não se aplicam aos serviços de consumidor.

Há dois ativos principais que compoem o armazenamento de conteúdo principal de SharePoint:

- **Metadados**: Os metadados sobre cada arquivo são armazenados Banco de Dados SQL do Azure. O Azure SQL oferece uma história completa de continuidade de negócios que SharePoint usos e detalhes são abordados posteriormente neste artigo.
- **Armazenamento de blob**: O conteúdo do usuário carregado no SharePoint é armazenado no Azure Armazenamento. SharePoint criou um plano de resiliência personalizado sobre o Azure Armazenamento para garantir a duplicação quase em tempo real do conteúdo do usuário e um sistema realmente ativo/ativo.

O conjunto completo de controles para garantir a resiliência de dados é explicado em seções posteriores.

## <a name="blob-storage-resilience"></a>Resiliência de armazenamento de blob

SharePoint tem uma solução personalizada para armazenamento de dados do cliente no Azure Armazenamento. Cada arquivo é gravado simultaneamente em uma região de datacenter principal e secundária. Se as gravações na região do Azure falharem, o arquivo salvo falhará. Depois que o conteúdo for gravado no Azure Armazenamento, os checksums serão armazenados separadamente com metadados e serão usados para garantir que a gravação comprometida seja idêntica ao arquivo original enviado ao SharePoint durante todas as leituras futuras. Essa mesma técnica é usada em todos os fluxos de trabalho para evitar a propagação de qualquer corrupção que deve ocorrer. Em cada região, o Azure Locally Redundant Armazenamento (LRS) fornece um alto nível de confiabilidade. Consulte o [artigo Armazenamento redundância do Azure](/azure/storage/common/storage-redundancy-lrs) para obter detalhes.

SharePoint usa Append-Only armazenamento. Esse processo garante que os arquivos não possam ser alterados ou corrompidos após uma salvação inicial, mas também usando o versionamento no produto, qualquer versão anterior do conteúdo do arquivo pode ser recuperada.

![Resiliência de armazenamento de blob](../media/assurance-blob-storage-resiliency-diagram.png)

SharePoint ambientes em qualquer datacenter podem acessar contêineres de armazenamento em ambas as regiões do Azure. Por motivos de desempenho, o contêiner de armazenamento no mesmo datacenter local é sempre preferencial, no entanto, as solicitações de leitura que não veem resultados dentro de um limite desejado terão o mesmo conteúdo solicitado do datacenter remoto para garantir que os dados sempre estão disponíveis.

## <a name="metadata-resilience"></a>Resiliência de metadados

SharePoint metadados também é fundamental para acessar o conteúdo do usuário à medida que armazena o local e as chaves de acesso ao conteúdo armazenado no Azure Armazenamento. Esses bancos de dados são armazenados no Azure SQL, que tem um plano extensivo [de continuidade de negócios.](/azure/sql-database/sql-database-business-continuity)

SharePoint usa o modelo de replicação fornecido pelo Azure SQL e criou uma tecnologia de automação proprietária para determinar que um failover é necessário e iniciar a operação, se necessário. Como tal, ele se enquadra na categoria "Failover de banco de dados manual" de uma perspectiva do Azure SQL. As métricas mais recentes para a recuperação SQL banco de dados do Azure estão disponíveis [aqui](/azure/azure-sql/database/business-continuity-high-availability-disaster-recover-hadr-overview#recover-a-database-to-the-existing-server).

![Resiliência de metadados](../media/assurance-metadata-resiliency-diagram.png)

SharePoint usa o sistema de backup do Azure SQL para habilitar o PitR (Point in Time Restores) por até 14 dias. O PITR é abordado mais em [uma seção posterior.](#deletion-backup-and-point-in-time-restore)

## <a name="automated-failover"></a>Failover automatizado

SharePoint usa um failover automatizado personalizado para minimizar o impacto na experiência do cliente quando ocorre um evento específico do local. A automação controlada pelo monitoramento detectando uma falha única ou multi componente além de determinados limites resultará em redirecionamento automatizado da atividade de todos os usuários fora do ambiente problemático e em um secundário quente. Um failover resulta em metadados e armazenamento de computação sendo atendido inteiramente fora do novo datacenter. Como o armazenamento de blob sempre é executado totalmente ativo/ativo, nenhuma alteração é necessária para um failover. A camada de computação preferirá o contêiner de blob mais próximo, mas usará locais de armazenamento de blob remoto e local a qualquer momento para garantir a disponibilidade.

SharePoint usa o serviço porta da frente do Azure para fornecer roteamento interno para a rede da Microsoft. Essa configuração permite o redirecionamento de failover independente do DNS e reduz o efeito do cache da máquina local. A maioria das operações de failover são transparentes para usuários finais. Se houver um failover, os clientes não precisarão fazer alterações para manter o acesso ao serviço.

## <a name="versioning-and-files-restore"></a>Versão e restauração de arquivos

Para bibliotecas de documentos recém-criadas, SharePoint padrão para 500 versões em cada arquivo e pode ser configurado para reter mais versões, se desejado. A interface do usuário não permite que um valor menor que 100 versões seja definido, mas é possível definir o sistema para armazenar menos versões usando APIs públicas. Para confiabilidade, qualquer valor menor que 100 não é recomendado e pode resultar em atividade do usuário causando perda de dados inadvertida.

Para obter mais informações sobre o versioning, consulte [Versioning in SharePoint](/microsoft-365/community/versioning-basics-best-practices).

A restauração de arquivos é a capacidade de voltar "no tempo" em qualquer Biblioteca de Documentos SharePoint a qualquer segundo tempo nos últimos 30 dias. Esse processo pode ser usado para recuperar de ransomware, exclusões em massa, corrupção ou qualquer outro evento. Esse recurso usa versões de arquivo para reduzir versões padrão pode reduzir a eficácia dessa restauração.

O recurso Restauração de Arquivos é documentado para [OneDrive](https://support.office.com/article/restore-your-onedrive-fa231298-759d-41cf-bcd0-25ac53eb8a15) e [SharePoint](https://support.office.com/article/Restore-a-document-library-317791c3-8bd0-4dfd-8254-3ca90883d39a).

## <a name="deletion-backup-and-point-in-time-restore"></a>Exclusão, backup e Restauração de Ponto no Tempo

O conteúdo do usuário excluído SharePoint passa pelo fluxo de exclusão a seguir.

Os itens excluídos são mantidos em lixeiras por um determinado período de tempo. Para SharePoint, o tempo de retenção é de 93 dias. Ele começa quando você exclui o item de seu local original. Quando você exclui o item da lixeira do site, ele entra na lixeira [do conjunto de sites.](https://support.office.com/article/restore-deleted-items-from-the-site-collection-recycle-bin-5fa924ee-16d7-487b-9a0a-021b9062d14b) Ele permanece lá pelo restante dos 93 dias e, em seguida, é excluído permanentemente. Mais informações sobre como usar a lixeira estão disponíveis nestes links:

- [Restaurar itens na Lixeira](https://support.office.com/article/Restore-items-in-the-Recycle-Bin-of-a-SharePoint-site-6df466b6-55f2-4898-8d6e-c0dff851a0be)
- [Restaurar itens excluídos da Lixeira do Conjunto de Sites.](https://support.office.com/article/Restore-deleted-items-from-the-site-collection-recycle-bin-5fa924ee-16d7-487b-9a0a-021b9062d14b)

Esse processo é o fluxo de exclusão padrão e não leva em conta políticas ou rótulos de retenção. Para obter mais informações, [consulte Learn about retention for SharePoint and OneDrive](/microsoft-365/compliance/retention-policies-sharepoint).

Depois que o pipeline de reciclagem de 93 dias é concluído, a exclusão ocorre independentemente para Metadados e para blob Armazenamento. Os metadados serão removidos imediatamente do banco de dados, o que torna o conteúdo ilegível, a menos que os metadados sejam restaurados do backup. SharePoint mantém 14 dias de backups de metadados. Esses backups são feitos localmente em tempo quase real e, em seguida, são levados para o armazenamento em contêineres redundantes do Azure Armazenamento [em,](/azure/sql-database/sql-database-automated-backups) de acordo com a documentação no momento desta publicação, um cronograma de 5 a 10 minutos.

Ao excluir o conteúdo Armazenamento Blob, SharePoint utiliza o recurso de exclusão suave do Azure Blob Armazenamento para proteger contra exclusão acidental ou mal-intencionada. Usando esse recurso, temos um total de 14 dias para restaurar o conteúdo antes que ele seja excluído permanentemente.

>[!Note]
>Embora os aplicativos Microsoft enviem conteúdo para a lixeira para o processo padrão, o SharePoint fornece APIs que permitem ignorar a lixeira e forçar uma exclusão imediata. Revise seus aplicativos para garantir que isso só seja feito quando necessário por motivos de conformidade.

## <a name="integrity-checks"></a>Verificações de integridade

SharePoint usa vários métodos para garantir a integridade de blobs e metadados em todos os estágios do ciclo de vida dos dados:

- **Hash de arquivo armazenado em metadados**: o hash de todo o arquivo é armazenado com metadados de arquivo para garantir que a integridade dos dados no nível do documento seja mantida durante todas as operações
- **Hash de blob armazenado em metadados**: Cada blob-item armazena um hash do conteúdo criptografado para proteger contra corrupção no armazenamento subjacente do Azure.
- **Trabalho de** integridade de dados : a cada 14 dias, cada site é verificado para a integridade, listando itens no banco de dados e combinando-os com os blobs listados no armazenamento do Azure. O trabalho relata qualquer blob-references ausentes de blobs de armazenamento e pode recuperar esses blobs por meio do recurso de exclusão suave de armazenamento do [Azure,](/azure/storage/blobs/soft-delete-blob-overview) se necessário.
