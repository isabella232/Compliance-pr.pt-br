---
title: Resiliência de dados do SharePoint e do OneDrive no Microsoft 365
description: Este artigo fornece uma visão geral da resiliência de dados do SharePoint e do OneDrive no Microsoft 365.
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
ms.openlocfilehash: c940b778681805a1e50a9e565117cd67deb52566
ms.sourcegitcommit: 2973d25e9e0185b84d281f963553a332eac1c1a3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/28/2021
ms.locfileid: "50040374"
---
# <a name="sharepoint-and-onedrive-data-resiliency-in-microsoft-365"></a>Resiliência de dados do SharePoint e do OneDrive no Microsoft 365

No Microsoft 365, o OneDrive é criado com base na plataforma de arquivos do SharePoint. Neste artigo, somente o SharePoint será usado para se referir a ambos os produtos. O conteúdo deste artigo é relevante para o Microsoft 365 e não se aplica aos serviços de consumidor.

Há dois ativos principais que compom o armazenamento de conteúdo principal do SharePoint:

- **Metadados:** os metadados sobre cada arquivo são armazenados no Banco de Dados SQL do Azure. O SQL do Azure oferece uma história de continuidade de negócios completa que o SharePoint usa e os detalhes são abordados posteriormente neste artigo.
- **Armazenamento de blob:** o conteúdo do usuário carregado no SharePoint é armazenado no Armazenamento do Azure. O SharePoint criou um plano de resiliência personalizado sobre o Armazenamento do Azure para garantir a duplicação quase em tempo real do conteúdo do usuário e um sistema realmente ativo/ativo.

O conjunto completo de controles para garantir a resiliência de dados é explicado em seções posteriores.

## <a name="blob-storage-resilience"></a>Resiliência de armazenamento de blob

O SharePoint tem uma solução personalizada para armazenamento de dados do cliente no Armazenamento do Azure. Cada arquivo é gravado simultaneamente em uma região de datacenter principal e secundária. Se as gravações em uma das regiões do Azure falharem, o arquivo salvo falhará. Depois que o conteúdo é gravado no Armazenamento do Azure, as verificações são armazenadas separadamente com metadados e são usadas para garantir que a gravação comprometida seja idêntica ao arquivo original enviado ao SharePoint durante todas as leituras futuras. Essa mesma técnica é usada em todos os fluxos de trabalho para evitar a propagação de qualquer corrupção que deva ocorrer. Em cada região, o Armazenamento Redundante Local (LRS) do Azure fornece um alto nível de confiabilidade. Confira o [artigo de redundância de](https://docs.microsoft.com/azure/storage/common/storage-redundancy-lrs) Armazenamento do Azure para obter detalhes.

O SharePoint usa Append-Only armazenamento. Esse processo garante que os arquivos não possam ser alterados ou corrompidos após um salvar inicial, mas também usando o versionamento no produto, qualquer versão anterior do conteúdo do arquivo pode ser recuperada.

Os ambientes do SharePoint em qualquer datacenter podem acessar contêineres de armazenamento em ambas as regiões do Azure. Por motivos de desempenho, o contêiner de armazenamento no mesmo datacenter local é sempre preferencial, no entanto, as solicitações de leitura que não veem os resultados dentro de um limite desejado terão o mesmo conteúdo solicitado do datacenter remoto para garantir que os dados estão sempre disponíveis.

## <a name="metadata-resilience"></a>Resiliência de metadados

Os metadados do SharePoint também são fundamentais para acessar o conteúdo do usuário, pois armazenam o local e as teclas de acesso ao conteúdo armazenado no Armazenamento do Azure. Esses bancos de dados são armazenados no SQL do Azure, que tem um amplo [plano de continuidade de negócios.](https://docs.microsoft.com/azure/sql-database/sql-database-business-continuity)

O SharePoint usa o modelo de replicação fornecido pelo SQL do Azure e criou uma tecnologia de automação proprietária para determinar que um failover é necessário e para iniciar a operação, se necessário. Dessa forma, ele se enquadra na categoria "Failover de banco de dados manual" de uma perspectiva sql do Azure. As métricas mais recentes para recuperação de banco de dados SQL do Azure estão disponíveis [aqui.](https://docs.microsoft.com/azure/azure-sql/database/business-continuity-high-availability-disaster-recover-hadr-overview#recover-a-database-to-the-existing-server)

O SharePoint usa o sistema de backup do Azure SQL para habilitar o Point in Time Restores (PITR) por até 14 dias. O PITR é abordado mais em [uma seção posterior.](#deletion-backup-and-point-in-time-restore)

## <a name="automated-failover"></a>Failover automatizado

O SharePoint usa um failover automatizado personalizado para minimizar o impacto na experiência do cliente quando ocorre um evento específico do local. A detecção de uma falha única ou de vários componentes, controlada pelo monitoramento além de certos limites, resultará no redirecionamento automatizado da atividade de todos os usuários fora do ambiente problemático e em um secundário morno. Um failover resulta em metadados e armazenamento de computação sendo atendido inteiramente fora do novo datacenter. Como o armazenamento de blob sempre é executado inteiramente ativo/ativo, nenhuma alteração é necessária para um failover. A camada de computação preferirá o contêiner de blob mais próximo, mas usará os locais de armazenamento de blob local e remoto a qualquer momento para garantir a disponibilidade.

O SharePoint usa o serviço de Porta Frontal do Azure para fornecer roteamento interno à rede da Microsoft. Essa configuração permite o redirecionamento de failover independente do DNS e reduz o efeito do cache da máquina local. A maioria das operações de failover é transparente para os usuários finais. Se houver um failover, os clientes não precisarão fazer alterações para manter o acesso ao serviço.

## <a name="versioning-and-files-restore"></a>Versioning and Files Restore

Para bibliotecas de documentos recém-criadas, o SharePoint assume como padrão 500 versões em cada arquivo e pode ser configurado para reter mais versões, se desejado. A interface do usuário não permite que um valor com menos de 100 versões seja definido, mas é possível definir o sistema para armazenar menos versões usando APIs públicas. Para uma confiabilidade, qualquer valor menor que 100 não é recomendado e pode resultar em atividade do usuário causando perda de dados inadvertida.

Para obter mais informações sobre o versionamento, consulte [Versioning no SharePoint.](https://docs.microsoft.com/microsoft-365/community/versioning-basics-best-practices)

Restauração de arquivos é a capacidade de voltar 'no tempo' em qualquer biblioteca de documentos no SharePoint a qualquer segundo tempo nos últimos 30 dias. Esse processo pode ser usado para se recuperar de ransomware, exclusões em massa, corrupção ou qualquer outro evento. Esse recurso usa versões de arquivo para reduzir as versões padrão pode reduzir a eficácia dessa restauração.

O recurso De restauração de arquivos está documentado para [o OneDrive](https://support.office.com/article/restore-your-onedrive-fa231298-759d-41cf-bcd0-25ac53eb8a15) e [o SharePoint.](https://support.office.com/article/Restore-a-document-library-317791c3-8bd0-4dfd-8254-3ca90883d39a)

## <a name="deletion-backup-and-point-in-time-restore"></a>Exclusão, backup e restauração de ponto no tempo

O conteúdo do usuário excluído do SharePoint passa pelo seguinte fluxo de exclusão.

Os itens excluídos são mantidos nas lixeiras por um determinado período de tempo. Para o SharePoint, o tempo de retenção é de 93 dias. Ele começa quando você exclui o item do local original. Quando você exclui o item da lixeira do site, ele vai para a lixeira [do conjunto de sites.](https://support.office.com/article/restore-deleted-items-from-the-site-collection-recycle-bin-5fa924ee-16d7-487b-9a0a-021b9062d14b) Ele permanece lá pelo restante dos 93 dias e, em seguida, é excluído permanentemente. Mais informações sobre como usar a lixeira estão disponíveis nestes links:

- [Restaurar itens na Lixeira](https://support.office.com/article/Restore-items-in-the-Recycle-Bin-of-a-SharePoint-site-6df466b6-55f2-4898-8d6e-c0dff851a0be)
- [Restaure os itens excluídos da Lixeira do Conjunto de Sites.](https://support.office.com/article/Restore-deleted-items-from-the-site-collection-recycle-bin-5fa924ee-16d7-487b-9a0a-021b9062d14b)

Esse processo é o fluxo de exclusão padrão e não leva em conta políticas ou rótulos de retenção. Para saber mais, confira [Saiba mais sobre retenção para o SharePoint e o OneDrive.](https://docs.microsoft.com/microsoft-365/compliance/retention-policies-sharepoint)

Depois que o pipeline de reciclagem de 93 dias for concluído, a exclusão ocorrerá de forma independente para Metadados e para o Armazenamento de Blob. Os metadados serão removidos imediatamente do banco de dados, o que torna o conteúdo ilegível, a menos que os metadados sejam restaurados do backup. O SharePoint mantém 14 dias de backups de metadados. Esses backups são feitos localmente quase em tempo real e, em [seguida,](https://docs.microsoft.com/azure/sql-database/sql-database-automated-backups) são encaminhados para o armazenamento em contêineres redundantes de Armazenamento do Azure, de acordo com a documentação no momento desta publicação, um cronograma de 5 a 10 minutos.

Ao excluir o conteúdo do Armazenamento de Blob, o SharePoint utiliza o recurso de exclusão suave do Armazenamento de Blob do Azure para se proteger contra exclusão acidental ou mal-intencionada. Usando esse recurso, temos um total de 14 dias para restaurar o conteúdo antes que ele seja excluído permanentemente.

>[!Note]
>Embora os aplicativos da Microsoft enviem conteúdo para a lixeira para o processo padrão, o SharePoint fornece APIs que permitem ignorar a lixeira e forçar uma exclusão imediata. Revise seus aplicativos para garantir que isso só seja feito quando necessário por motivos de conformidade.

## <a name="integrity-checks"></a>Verificações de integridade

O SharePoint usa vários métodos para garantir a integridade de blobs e metadados em todos os estágios do ciclo de vida dos dados:

- **Hash de arquivo armazenado em** metadados: o hash de todo o arquivo é armazenado com metadados de arquivo para garantir que a integridade dos dados no nível do documento seja mantida durante todas as operações
- **Hash de blob armazenado em** metadados: cada item de blob armazena um hash do conteúdo criptografado para proteger contra corrupção no armazenamento subjacente do Azure.
- **Trabalho de** integridade de dados: a cada 14 dias, cada site é verificado quanto à integridade listando itens no banco de dados e combinando-os com os blobs listados no armazenamento do Azure. O trabalho relata qualquer blob-reference de blob ausente blobs de armazenamento e pode recuperar esses blobs por meio do recurso de exclusão suave de armazenamento do [Azure,](https://docs.microsoft.com/azure/storage/blobs/soft-delete-blob-overview) se necessário.
