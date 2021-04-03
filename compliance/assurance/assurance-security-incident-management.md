---
title: Gerenciamento de incidentes do Centro de segurança do Microsoft 365
description: Este artigo fornece uma visão geral do processo de gerenciamento de incidentes de segurança no Microsoft 365.
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
ms.openlocfilehash: a61a4406c4951c4d4584831cf58030545955fd35
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51496785"
---
# <a name="microsoft-365-security-incident-management"></a>Gerenciamento de incidentes do Centro de segurança do Microsoft 365

A Microsoft trabalha continuamente para fornecer serviços de nível empresarial altamente seguros para clientes do Microsoft 365. Este documento descreve como a Microsoft lida com incidentes de segurança no Microsoft 365. Um incidente de segurança refere-se a qualquer acesso ilegal aos dados do cliente armazenados no equipamento da Microsoft ou nas instalações da Microsoft ou acesso não autorizado a esses equipamentos ou instalações que tenham o potencial de resultar na perda, divulgação ou alteração de dados do cliente. As metas da Microsoft ao responder a incidentes de segurança são proteger os dados do cliente e os serviços do Microsoft 365.

A equipe de Segurança do Microsoft 365 e as várias equipes de serviço trabalham em conjunto e têm a mesma abordagem para incidentes de segurança:

- Preparação
- Detecção e análise
- Contenção
- Erradicação
- Recuperação
- Atividade pós-incidente

## <a name="microsoft-approach-to-security-incident-management"></a>Abordagem da Microsoft para o gerenciamento de incidentes de segurança

A abordagem da Microsoft para gerenciar um incidente de segurança está em conformidade com a Publicação Especial (SP) 800-61 do Instituto Nacional de Padrões e Tecnologia [(NIST).](https://www.nist.gov/) A Microsoft tem várias equipes dedicadas que trabalham juntas para evitar, monitorar, detectar e responder a incidentes de segurança.

|**Equipe/Área**|**Descrição**|
|:------------|:--------------|
| Centro de Resposta de Segurança da Microsoft | Identifica, monitora, resolve e responde a incidentes de segurança e vulnerabilidades de segurança de software da Microsoft. |
| Centro de Operações de Defesa Cibernética | O Centro de Operações de Defesa Cibernética é o local físico que reúne equipes de resposta de segurança e especialistas de toda a empresa para ajudar a proteger, detectar e responder a ameaças em tempo real. |
| Assuntos corporativos, externos e jurídicos | Fornece orientações legais e regulatórias para um incidente de segurança suspeito. |
| Equipe de Resposta de Segurança do Microsoft 365 | Parceiros com as equipes do Serviço do Microsoft 365 para criar o processo de gerenciamento de incidentes de segurança apropriado e para conduzir qualquer resposta a incidentes de segurança. |
| Confiança do Office 365 | Fornece orientações sobre requisitos regulatórios, conformidade e privacidade. |
| Equipe de Segurança do Datacenter do Microsoft 365 | Equipe que se concentra nos vários serviços em investimentos comuns de engenharia de segurança para proteger, detectar e responder aos riscos e ameaças da arquitetura de serviço do Microsoft 365. |
| Equipes de serviço | Equipes de engenharia para serviços do Microsoft 365, como Exchange, SharePoint e Microsoft Teams, que são responsáveis por políticas e decisões relacionadas à segurança para cada serviço. |
| Microsoft Threat Intelligence Center (MSTIC) | Fornece o estado de arte atual em ameaças de segurança digital contra a infraestrutura e ativos da Microsoft, ajuda as equipes parceiras dentro da Microsoft a priorizar planos de ação de mitigação e prevenção e aumenta a proteção adotando o monitoramento/detecção de incidentes quase em tempo real. |
| Equipes de Segurança de Parceiros | Outras equipes de segurança de parceiros dentro da Microsoft que fornecem serviços importantes ou são responsáveis pelas principais dependências no Microsoft 365, como a equipe de Resposta de Segurança do Azure, a Resposta de Segurança de Identidade e as equipes de Resposta de Segurança Corporativa da Microsoft. |
| Comunicações de Experiência do Cliente do Microsoft 365 | Equipe de engenharia responsável por todas as comunicações do cliente sobre incidentes de segurança e serviço. |

## <a name="response-management-process"></a>Processo de gerenciamento de resposta

A equipe de Segurança do Microsoft 365 e as equipes de serviço trabalham em conjunto e têm a mesma abordagem para incidentes de segurança, que se baseia nas fases de gerenciamento de resposta do NIST 800-61:

- **Preparação**: refere-se à preparação organizacional necessária para poder responder, incluindo ferramentas, processos, competências e preparação.
- **Análise & detecção**: refere-se à atividade para detectar um incidente de segurança em um ambiente de produção e analisar todos os eventos para confirmar a autenticidade do incidente de segurança.
- **Contenção, erradicação, recuperação**: refere-se às ações necessárias e apropriadas tomadas para conter o incidente de segurança com base na análise feita na fase anterior. Mais análises também podem ser necessárias nesta fase para a recuperação completa do incidente de segurança.
- **Atividade pós-incidente**: refere-se à análise pós-mortem realizada após a recuperação de um incidente de segurança. As ações operacionais executadas durante o processo são revisadas para determinar se alguma alteração precisa ser feita nas fases de preparação ou detecção e análise.

## <a name="federated-security-response-model"></a>Modelo de resposta de segurança federada

Os serviços do Microsoft 365 incluem os principais serviços online da Microsoft (Exchange, SharePoint e Microsoft Teams, etc.) e outros serviços de nuvem da Microsoft, como o Azure Active Directory, a Plataforma do Microsoft Commerce e o MSTIC. Esses serviços são operados por equipes separadas com seus próprios processos operacionais de segurança. Outras equipes da Microsoft também estão envolvidas em vários aspectos de segurança do Microsoft 365. Devido à multiplicidade de equipes que trabalham no gerenciamento de operações de segurança em todos os vários serviços que comem o Microsoft 365, a Microsoft implementou um modelo de resposta de segurança federado.

Esta tabela apresenta os limites operacionais entre as várias equipes de operações de segurança do Microsoft 365 e as equipes de serviço do Microsoft 365:

|**Atividades**|**Operações de equipe de segurança do Microsoft 365**|**Operações de equipe de serviço do Microsoft 365**|
|:-----------|:-----------------------------------------|:----------------------------------------|
| Detecção e análise | - Requisitos de detecção <br> - Monitoramento e análise de segurança <br> - Indicador de varreduras de comprometimento (IOC) <br> - Busca de violação <br> - Líder de resposta a incidentes e segurança 24x7 | - Requisitos de detecção <br> - Monitoramento da implantação de infraestrutura <br> - Análise e visão do serviço <br> - Triagem de eventos e alertas <br> - Engenharia de serviço 24x7 em chamada  |
| Contenção, erradicação, recuperação | - Líder de resposta a incidentes <br> - Investigação forense <br> - Experiência em segurança e consultoria <br> - Diretrizes de recuperação | - Proprietário de incidentes de segurança <br> - Experiência e experiência do serviço <br> - Executar contenção, erradicação e recuperação |
| Atividade pós-incidente | - Líder de análise pós-incidente <br> - Coleta e arquivamento de dados <br> - Lições aprendidas e solicitações de bugs <br> - Relatório de incidentes | - Análise de incidentes do lado do serviço <br> - Priorizar atividades de acompanhamento <br> - Implementação de investimentos em segurança <br> - Preparação de segurança do serviço |

## <a name="related-articles"></a>Artigos relacionados

- [Preparação do gerenciamento de incidentes de segurança do Microsoft 365](assurance-sim-preparation.md)
- [Análise e detecção de gerenciamento de incidentes de segurança do Microsoft 365](assurance-sim-detection-analysis.md)
- [Contenção, erradicação e recuperação de gerenciamento de incidentes de segurança do Microsoft 365](assurance-sim-containment-eradication-recovery.md)
- [Atividade pós-incidente de gerenciamento de incidentes de segurança do Microsoft 365](assurance-sim-post-incident-activity.md)
