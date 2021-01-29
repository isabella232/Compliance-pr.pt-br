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
ms.openlocfilehash: 9a76a258edf77708786cf19b160c4c5ee7af7ee6
ms.sourcegitcommit: 2973d25e9e0185b84d281f963553a332eac1c1a3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/28/2021
ms.locfileid: "50040354"
---
# <a name="microsoft-365-security-incident-management"></a>Gerenciamento de incidentes do Centro de segurança do Microsoft 365

A Microsoft trabalha continuamente para fornecer serviços altamente seguros e de nível empresarial para clientes do Microsoft 365. Este documento descreve como a Microsoft lida com incidentes de segurança no Microsoft 365. Um incidente de segurança refere-se a qualquer acesso ilegal aos dados do cliente armazenados no equipamento da Microsoft ou em instalações da Microsoft, ou acesso não autorizado a tais equipamentos ou instalações que têm o potencial de resultar na perda, divulgação ou alteração de dados do cliente. As metas da Microsoft ao responder a incidentes de segurança são proteger os dados do cliente e os serviços do Microsoft 365.

A equipe de Segurança do Microsoft 365 e as várias equipes de serviço trabalham em conjunto e têm a mesma abordagem para incidentes de segurança:

- Preparação
- Detecção e análise
- Contenção
- Eliminação
- Recuperação
- Atividade pós-incidente

## <a name="microsoft-approach-to-security-incident-management"></a>Abordagem da Microsoft para o gerenciamento de incidentes de segurança

A abordagem da Microsoft para gerenciar um incidente de segurança está em conformidade com a Publicação Especial (SP) 800-61 do Instituto Nacional de Padrões e Tecnologia [(NIST).](https://www.nist.gov/) A Microsoft tem várias equipes dedicadas que trabalham juntas para evitar, monitorar, detectar e responder a incidentes de segurança.

|**Equipe/Área**|**Description**|
|:------------|:--------------|
| Centro de Resposta de Segurança da Microsoft | Identifica, monitora, resolve e responde a incidentes de segurança e vulnerabilidades de segurança de software da Microsoft. |
| Centro de Operações de Defesa Cibernética | O Centro de Operações de Defesa Cibernética é o local físico que reúne equipes de resposta de segurança e especialistas de toda a empresa para ajudar a proteger, detectar e responder a ameaças em tempo real. |
| Assuntos corporativos, externos e jurídicos | Fornece conselhos legais e regulatórios para um incidente de segurança suspeito. |
| Equipe de Resposta de Segurança do Microsoft 365 | Parceiros com as equipes do Serviço do Microsoft 365 para criar o processo apropriado de gerenciamento de incidentes de segurança e para impulsionar qualquer resposta a incidentes de segurança. |
| Confiança do Office 365 | Fornece diretrizes sobre requisitos regulatórios, conformidade e privacidade. |
| Equipe de Segurança do Datacenter do Microsoft 365 | Equipe que se concentra em vários serviços em investimentos comuns em engenharia de segurança para proteger, detectar e responder a riscos e ameaças da arquitetura de serviço do Microsoft 365. |
| Equipes de serviço | Equipes de engenharia para os serviços do Microsoft 365, como o Exchange, o SharePoint e o Microsoft Teams, são responsáveis por políticas e decisões relacionadas à segurança de cada serviço. |
| Central de Inteligência contra Ameaças da Microsoft (MSTIC) | Fornece o estado atual das ameaças à segurança digital contra a infraestrutura e os ativos da Microsoft, ajuda as equipes parceiras dentro da Microsoft a priorizar planos de ação de mitigação e prevenção e aumenta a proteção adotando monitoramento/detecção de incidentes quase em tempo real. |
| Equipes de Segurança de Parceiros | Outras equipes de segurança de parceiros dentro da Microsoft que fornecem serviços importantes ou são responsáveis pelas principais dependências no Microsoft 365, como a equipe de Resposta de Segurança do Azure, a Resposta de Segurança de Identidade e as equipes de Resposta de Segurança Corporativa da Microsoft. |
| Comunicações da Experiência do Usuário do Microsoft 365 | Equipe de engenharia responsável por todas as comunicações do cliente sobre incidentes de segurança e serviço. |

## <a name="response-management-process"></a>Processo de gerenciamento de resposta

A equipe de Segurança do Microsoft 365 e as equipes de serviço trabalham juntas e têm a mesma abordagem para incidentes de segurança, que se baseia nas fases de gerenciamento de resposta NIST 800-61:

- **Preparação:** refere-se à preparação organizacional necessária para poder responder, incluindo ferramentas, processos, competências e preparação.
- **Análise &** detecção: refere-se à atividade para detectar um incidente de segurança em um ambiente de produção e analisar todos os eventos para confirmar a autenticidade do incidente de segurança.
- **Contenção, eliminação,** recuperação: refere-se às ações necessárias e apropriadas tomadas para conter o incidente de segurança com base na análise feita na fase anterior. Mais análises também podem ser necessárias nesta fase para a recuperação total do incidente de segurança.
- **Atividade pós-incidente:** refere-se à análise pós-mortem realizada após a recuperação de um incidente de segurança. As ações operacionais executadas durante o processo são revisadas para determinar se alguma alteração precisa ser feita nas fases de preparação ou detecção e análise.

## <a name="federated-security-response-model"></a>Modelo de resposta de segurança federada

Os serviços do Microsoft 365 incluem os principais serviços online da Microsoft (Exchange, SharePoint, Microsoft Teams etc.) e outros serviços em nuvem da Microsoft, como o Azure Active Directory, a Plataforma Microsoft Commerce e o MSTIC. Esses serviços são operados por equipes separadas com seus próprios processos operacionais de segurança. Outras equipes da Microsoft também estão envolvidas em vários aspectos de segurança do Microsoft 365. Devido à infinidade de equipes trabalhando no gerenciamento de operações de segurança em todos os vários serviços que com o Microsoft 365, a Microsoft implementou um modelo de resposta de segurança federado.

Esta tabela apresenta os limites operacionais entre as diversas equipes de operações de segurança do Microsoft 365 e as equipes de serviço do Microsoft 365:

|**Atividades**|**Operações da Equipe de Segurança do Microsoft 365**|**Operações da Equipe de Serviço do Microsoft 365**|
|:-----------|:-----------------------------------------|:----------------------------------------|
| Detecção e análise | - Requisitos de detecção <br> - Monitoramento e análise de segurança <br> - Indicador de limpezas de comprometimento (IOC) <br> - Busca de violação <br> - Líder de resposta a incidentes e segurança 24x7 em chamada | - Requisitos de detecção <br> - Monitorando a implantação da infraestrutura <br> - Análise e visão do serviço <br> - Triagem de eventos e alertas <br> - Engenharia de serviço 24x7 em chamada  |
| Contenção, eliminação, recuperação | - Líder de resposta a incidentes <br> - Investigação forense <br> – Experiência em segurança e consultoria <br> - Diretrizes de recuperação | - Proprietário do incidente de segurança <br> – Conhecimento e experiência do serviço <br> - Executar a contenção, a eliminação e a recuperação |
| Atividade pós-incidente | - Líder de análise pós-incidente <br> - Coleta e arquivamento de dados <br> - Lições aprendidas e solicitações de bugs <br> - Relatório de incidentes | - Análise de incidentes no lado do serviço <br> - Priorizar atividades de acompanhamento <br> - Investimentos em segurança de implementação <br> - Preparação de segurança do serviço |

## <a name="related-articles"></a>Artigos relacionados

- [Preparação do gerenciamento de incidentes de segurança do Microsoft 365](assurance-sim-preparation.md)
- [Análise e detecção de gerenciamento de incidentes de segurança do Microsoft 365](assurance-sim-detection-analysis.md)
- [Contenção, eliminação e recuperação do gerenciamento de incidentes de segurança do Microsoft 365](assurance-sim-containment-eradication-recovery.md)
- [Atividade pós-incidente de gerenciamento de incidentes de segurança do Microsoft 365](assurance-sim-post-incident-activity.md)
