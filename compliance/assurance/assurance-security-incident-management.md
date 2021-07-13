---
title: Gerenciamento de incidentes de segurança da Microsoft
description: Este artigo fornece uma visão geral do processo de gerenciamento de incidentes de segurança nos serviços online da Microsoft.
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
- MS-Compliance0
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: a2c2a472d911034952814da51db133acc5744288
ms.sourcegitcommit: 8bf2602d56eedee4447ddb374ef95b0587f254e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/12/2021
ms.locfileid: "53377498"
---
# <a name="microsoft-security-incident-management"></a>Gerenciamento de incidentes de segurança da Microsoft

A Microsoft trabalha continuamente para fornecer serviços de nível empresarial altamente seguros para os clientes da Microsoft, mas os incidentes de segurança são uma realidade inevitável que deve ser gerenciada de forma completa e rápida. Este documento fornece uma visão geral sobre como a Microsoft lida com incidentes de segurança usando métodos e tecnologias tentados e verdadeiros para minimizar seu impacto potencial. Um incidente de segurança refere-se a qualquer acesso ilegal aos dados do cliente armazenados no equipamento da Microsoft ou nas instalações da Microsoft ou acesso não autorizado a esses equipamentos ou instalações que tenham o potencial de resultar na perda, divulgação ou alteração de dados do cliente. As metas da Microsoft ao responder a incidentes de segurança são proteger os dados do cliente e os serviços online da Microsoft.

As equipes de segurança dos serviços online da Microsoft e as várias equipes de serviço trabalham em conjunto e têm a mesma abordagem para incidentes de segurança:

- Preparação
- Detecção e análise
- Contenção, Erradicação e Recuperação
- Atividade pós-incidente

## <a name="microsoft-approach-to-security-incident-management"></a>Abordagem da Microsoft para o gerenciamento de incidentes de segurança

A abordagem da Microsoft para gerenciar um incidente de segurança está em conformidade com a Publicação Especial (SP) 800-61 do Instituto Nacional de Padrões e Tecnologia [(NIST).](https://www.nist.gov/) A Microsoft tem várias equipes dedicadas que trabalham juntas para evitar, monitorar, detectar e responder a incidentes de segurança.

|**Equipe/Área**|**Descrição**|
|:------------|:--------------|
| Centro de Resposta de Segurança da Microsoft | Identifica, monitora, resolve e responde a incidentes de segurança e vulnerabilidades de segurança de software da Microsoft. |
| Centro de Operações de Defesa Cibernética | O Centro de Operações de Defesa Cibernética é o local físico que reúne equipes de resposta de segurança e especialistas de toda a empresa para ajudar a proteger, detectar e responder a ameaças em tempo real. |
| Assuntos corporativos, externos e jurídicos | Fornece orientações legais e regulatórias para um incidente de segurança suspeito. |
| Equipe de Segurança do Microsoft Datacenter | Equipe que se concentra nos vários serviços em investimentos comuns de engenharia de segurança para proteger, detectar e responder a riscos e ameaças da arquitetura de serviço. |
| Equipes de resposta de segurança da Microsoft | Equipes de segurança independentes do Azure, do Dynamics 365 e Microsoft 365 que são parceiras com equipes de serviço para criar o processo de gerenciamento de incidentes de segurança apropriado e para conduzir qualquer resposta a incidentes de segurança. |
| Equipes de Governança, Risco e Conformidade (GRC) da Microsoft | Forneça orientações sobre requisitos regulatórios, conformidade e privacidade. |
| Equipes de serviço | Equipes de engenharia do Azure, Dynamics 365, Microsoft 365 que são responsáveis por políticas e decisões relacionadas à segurança para cada serviço. |
| Gerentes de operações do Azure | Supervisiona a investigação e a resolução de incidentes de segurança e privacidade relacionados ao Azure. |
| Microsoft Threat Intelligence Center (MSTIC) | Fornece o estado de arte atual em ameaças de segurança digital contra a infraestrutura e ativos da Microsoft, ajuda as equipes parceiras dentro da Microsoft a priorizar planos de ação de mitigação e prevenção e aumenta a proteção adotando o monitoramento/detecção de incidentes quase em tempo real. |
| Equipes de comunicação de experiência do cliente | Equipes de engenharia responsáveis por todas as comunicações do cliente sobre incidentes de segurança e serviço. As equipes separadas são dedicadas ao Azure, Ao Dynamics 365 e Microsoft 365. |

## <a name="response-management-process"></a>Processo de gerenciamento de resposta

As equipes de segurança e de serviços online da Microsoft trabalham em conjunto e têm a mesma abordagem para incidentes de segurança, que se baseia nas fases de gerenciamento de resposta do NIST 800-61:

- **Preparação**: refere-se à preparação organizacional necessária para poder responder, incluindo ferramentas, processos, competências e preparação.
- **Análise & detecção**: refere-se à atividade para detectar um incidente de segurança em um ambiente de produção e analisar todos os eventos para confirmar a autenticidade do incidente de segurança.
- **Contenção, erradicação, recuperação**: refere-se às ações necessárias e apropriadas tomadas para conter o incidente de segurança com base na análise feita na fase anterior. Mais análises também podem ser necessárias nesta fase para a recuperação completa do incidente de segurança.
- **Atividade pós-incidente**: refere-se à análise pós-mortem realizada após a recuperação de um incidente de segurança. As ações operacionais executadas durante o processo são revisadas para determinar se alguma alteração precisa ser feita nas fases de preparação ou detecção e análise.

![Fases de gerenciamento de incidentes de segurança](../media/assurance-sim-phases.png)

## <a name="federated-security-response-model"></a>Modelo de resposta de segurança federada

Os serviços online da Microsoft consistem em produtos principais da Microsoft, incluindo o Azure, o Dynamics 365 e o Microsoft 365. Cada um desses serviços é operado por equipes separadas com seus próprios processos operacionais de segurança. Outras equipes da Microsoft, como o MSTIC, também estão envolvidas em vários aspectos de segurança dos serviços online da Microsoft. Devido à multiplicidade de equipes que trabalham no gerenciamento de operações de segurança em todos os vários serviços online da Microsoft, a Microsoft implementou um modelo de resposta de segurança federado.

Esta tabela apresenta os limites operacionais entre as várias equipes de operações de segurança do serviço online da Microsoft e as equipes de serviço da Microsoft:

|**Atividades**|**Operações da Equipe de Segurança da Microsoft**|**Operações de equipe de serviço da Microsoft**|
|:-----------|:-----------------------------------------|:----------------------------------------|
| Detecção e análise | - Requisitos de detecção <br> - Monitoramento e análise de segurança <br> - Indicador de varreduras de comprometimento (IOC) <br> - Busca de violação <br> - Líder de resposta a incidentes e segurança 24x7 | - Requisitos de detecção <br> - Monitoramento da implantação de infraestrutura <br> - Análise e visão do serviço <br> - Triagem de eventos e alertas <br> - Engenharia de serviço 24x7 em chamada  |
| Contenção, erradicação, recuperação | - Líder de resposta a incidentes <br> - Investigação forense <br> - Experiência em segurança e consultoria <br> - Diretrizes de recuperação | - Proprietário de incidentes de segurança <br> - Experiência e experiência do serviço <br> - Executar contenção, erradicação e recuperação |
| Atividade pós-incidente | - Líder de análise pós-incidente <br> - Coleta e arquivamento de dados <br> - Lições aprendidas e solicitações de bugs <br> - Relatório de incidentes | - Análise de incidentes do lado do serviço <br> - Priorizar atividades de acompanhamento <br> - Implementação de investimentos em segurança <br> - Preparação de segurança do serviço |

## <a name="related-articles"></a>Artigos relacionados

- [Gerenciamento de incidentes de segurança da Microsoft: Preparação](assurance-sim-preparation.md)
- [Gerenciamento de incidentes de segurança da Microsoft: Detecção e análise](assurance-sim-detection-analysis.md)
- [Gerenciamento de incidentes de segurança da Microsoft: contenção, erradicação e recuperação](assurance-sim-containment-eradication-recovery.md)
- [Gerenciamento de incidentes de segurança da Microsoft: atividade pós-incidente](assurance-sim-post-incident-activity.md)
