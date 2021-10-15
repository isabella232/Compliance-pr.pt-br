---
title: Gerenciamento de ativos de datacenter
description: Uma visão geral do gerenciamento de ativos do datacenter da Microsoft.
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: medium
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
f1.keywords:
- NOCSH
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: fafba29a25c5b01fa37d091fb210185a98365192
ms.sourcegitcommit: b228be59e13ae2e05ba85f65c1d4648fef5e9260
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/14/2021
ms.locfileid: "60356377"
---
# <a name="datacenter-asset-management"></a>Gerenciamento de ativos de datacenter

Os datacenters da Microsoft são feitos de vários componentes físicos e virtuais, cada um deles chamado de ativo. O grupo de engenharia de Operações e Inovação na Nuvem da Microsoft (CO+I) segue processos padronizados seguros para a implantação, o controle e o descomissionamento de ativos físicos e virtuais.

## <a name="supply-chain-integrity"></a>Integridade da cadeia de fornecedores

A segurança de ativos começa com a segurança da cadeia de fornecimento. A Microsoft está comprometida com a integridade da cadeia de fornecedores e com a segurança da cadeia de fornecedores de ponta a ponta. Os fornecedores seguem procedimentos estritos de cadeia de proteção ao transportar nossos componentes de nuvem para reduzir o risco de alteração e adulteração. Todos os inventários de entrada e saída são inspecionados e monitorados cuidadosamente para garantir a integridade dos componentes e firmware.

As entregas de componentes do sistema de informações aos datacenters da Microsoft normalmente são agendadas. Para entregas não agendadas, a Microsoft inspeciona e garante que eles sejam aprovados para entrada em uma sala de computador da Microsoft antes da entrada física. Quando um componente do sistema de informações entra no edifício, a equipe de Gerenciamento de Ativos compara o item recebido com o tíquete referenciado e verifica o dispositivo na ferramenta de gerenciamento de ativos. Todos os componentes do sistema de informações recebidos ou enviados são acompanhados pela ferramenta de tíquete de fluxo de trabalho e nos logs de envio na ferramenta de gerenciamento de ativos. Os visitantes são proibidos de usar laptops pessoais e telefones celulares (exceto para chamada de emergência e anotações), embora sejam permitidos no ambiente de produção (colocações). Conectar celulares a um dispositivo ou tirar fotos é proibido por política de datacenter. Se o equipamento que entra no datacenter for usado para fins de manutenção, o equipamento exigirá aprovação do Gerenciamento de Datacenter no sistema ferramenta de acesso do Datacenter.

## <a name="asset-inventory"></a>Inventário de ativos

A Microsoft exige que todos os ativos de datacenter sejam contabilizados e tenham um proprietário designado. Os proprietários são responsáveis por manter as informações atualizadas para seus ativos físicos e virtuais. Quando novos ativos físicos são adicionados a um datacenter, eles são assinados, verificados, marcados de forma única e checados nos sistemas de controle de inventário. As ferramentas automatizadas de monitoramento ajudam no acompanhamento de ativos físicos e virtuais.

## <a name="asset-maintenance"></a>Manutenção de ativos

A Microsoft tem duas equipes que fornecem diferentes tipos de manutenção de ativos: as equipes de Ambiente Crítico (CE) e Serviços de Site. A equipe ce fornece gerenciamento de instalações para sistemas elétricos, mecânicos e físicos que compõem a infraestrutura operacional da instalação. Eles também agendam, executam, documentam e analisam todas as atividades de manutenção realizadas em componentes ce. Os datacenters da Microsoft dependem de um sistema de gerenciamento de manutenção computadorizado para gerenciar agendas de manutenção e ordens de trabalho. A equipe de Serviços de Site presta serviços a todos os ativos de serviço online da Microsoft localizados nos datacenters da Microsoft. Além disso, a equipe de Serviços de Site fornece suporte técnico local e serviço de correção de quebra para ativos pertencentes aos serviços de provisionamento de propriedades do datacenter.

## <a name="asset-classification"></a>Classificação de ativos

Os ativos da Microsoft , incluindo dados, são classificados de acordo com as Enterprise de Taxonomia de Dados. Essas diretrizes promovem a padronização em toda a empresa e são revisadas e atualizadas anualmente. Os padrões de classificação de ativos e proteção de ativos definem os procedimentos de segurança que os funcionários devem seguir ao interagir com cada ativo. Observe que os clientes são considerados proprietários dos dados armazenados no ambiente do Microsoft Cloud. Os ativos de dados classificados como conteúdo do cliente ou dados do cliente são protegidos por procedimentos de segurança aplicáveis.

A Microsoft considera toda a documentação categorizada como um ativo do sistema. A equipe de Serviços de Site é responsável por classificar seus ativos e empregar as proteções associadas de acordo com os padrões de classificação de ativos e proteção de ativos, bem como quaisquer requisitos adicionais definidos pela equipe de serviço.

Os proprietários de ativos são obrigados a atribuir a seus ativos uma classificação de ativo, sem exceção. Em ambientes de datacenter da Microsoft, os ativos referem-se a servidores e dispositivos de rede. Outras mídias digitais como unidades flash USB, discos rígidos externos ou CD/DVDs não são usadas para a operação de serviços. A mídia não digital não é usada em datacenters.

## <a name="media-storage"></a>Armazenamento de mídia

Os ativos de mídia digital da Microsoft são armazenados fisicamente e com segurança nas salas de colocação do datacenter da Microsoft. Várias camadas de controles de acesso físico e de vídeo estão no local para proteger e monitorar esses ativos. Quando os ativos de mídia digital chegam ao final do ciclo de vida, eles são limpos, limpos ou destruídos usando métodos consistentes com o NIST SP 800-88 antes do descarte. O [artigo de destruição de dispositivos com](assurance-data-bearing-device-destruction.md) suporte de dados aborda o processo de descarte seguro de ativos.

## <a name="media-transport"></a>Transporte de mídia

A Microsoft restringe as atividades de transporte de ativos para funcionários autorizados por meio da cadeia de proteções de custodia. O uso de bloqueios, selos à prova de adulteração e validação necessária do inventário de ativos garante que apenas funcionários autorizados estão envolvidos no transporte de ativos.

Todas as mídias transportadas dos datacenters da Microsoft exigem controle preciso. A Microsoft contratou vários fornecedores aprovados para fornecer serviços de envio seguros. O transporte seguro começa com um inventário preciso e uma cadeia de proteção. No local de entrega, o pessoal aprovado da empresa de transporte deve presenciar a remoção do selo à prova de adulteração e o desbloqueio do contêiner. A equipe de recebimento inventaria o carregamento e envia uma mensagem confirmando o recebimento dos ativos. A Microsoft também contratou com um fornecedor para fornecer destruição de equipamento. Dependendo da classificação de ativos, alguns equipamentos são necessários para serem destruídos no local.

O transporte de mídia digital da Microsoft fora do espaço controlado pela segurança requer a supervisão de dois membros da equipe de Operações do Datacenter. Os ativos são continuamente acompanhados e supervisionados por funcionários autorizados até que sejam destruídos.

A equipe de Gerenciamento de Datacenter controla a entrega e a remoção de componentes do sistema de informações por meio de tíquetes rastreados na ferramenta de tíquete. A entrega e a remoção de componentes do sistema de informações são autorizadas pelos proprietários do sistema.

## <a name="asset-retention"></a>Retenção de ativos

Os ativos de propriedade da Microsoft são mantidos conforme apropriado com base nos requisitos de retenção definidos pelo Gerenciamento de Registros Corporativos, pela classificação de ativos ou pelos requisitos contratuais. Para obter mais informações sobre retenção de dados, consulte [Retenção de dados, exclusão](assurance-data-retention-deletion-and-destruction-overview.md)e destruição em Microsoft 365 .
