---
title: 'Gerenciamento de incidentes de segurança do Microsoft 365: Detecção e análise'
description: Este artigo fornece uma visão geral do processo de detecção e análise de gerenciamento de incidentes de segurança no Microsoft 365.
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
ms.openlocfilehash: 433b8da98e25c4f465473143074eda055419234d
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497399"
---
# <a name="microsoft-365-security-incident-management-detection-and-analysis"></a>Gerenciamento de incidentes de segurança do Microsoft 365: Detecção e análise

Para detectar atividades mal-intencionadas, o Microsoft 365 registra centralmente eventos de segurança e outros dados e executa várias técnicas analíticas para encontrar atividades anômalas ou suspeitas. Os arquivos de log são coletados de servidores e dispositivos de infraestrutura do Microsoft 365 e armazenados em um banco de dados central e consolidado.

A Microsoft assume uma abordagem baseada em risco para detectar atividades mal-intencionadas. Usamos dados de incidentes e inteligência contra ameaças para definir e priorizar nossas detecções.

Empregar uma equipe de pessoas altamente experientes, proficientes e qualificadas é um dos pilares mais importantes para o sucesso na fase de detecção e análise. O Microsoft 365 emprega várias equipes de serviço, e essas equipes incluem funcionários com competências em todos os componentes da pilha, incluindo a rede, roteadores, firewalls, balanceadores de carga, sistemas operacionais e aplicativos.

Os mecanismos de detecção de segurança no Microsoft 365 também incluem notificações e alertas iniciados por fontes diferentes. A equipe de Resposta de Segurança do Microsoft 365 é o principal orquestrador do processo de escalonamento de incidentes de segurança. Essa equipe recebe todas as escalações e é responsável por analisar e confirmar a validade do incidente de segurança.

Um dos principais pilares da detecção é a notificação:

- Cada equipe de serviço é responsável por registrar qualquer ação ou evento dentro do serviço com base nos requisitos da equipe de Segurança do Microsoft 365. Todos os logs criados pelas diferentes equipes de serviço são processados por uma solução SIEM (Gerenciamento de Informações de Segurança e Eventos) com regras de segurança e detecção predefinidos. Essas regras evoluem com base na recomendação da equipe de Segurança do Microsoft 365, em informações aprendidas de incidentes de segurança anteriores, para determinar se há alguma atividade suspeita ou mal-intencionada.
- Se um cliente determinar que um incidente de segurança está em andamento, ele poderá abrir um caso de suporte com a Microsoft, que é atribuída à equipe de Comunicações de Experiência do Cliente (CxP) do Microsoft 365 e transformada em uma escalonamento para todas as equipes apropriadas.

As equipes de serviço do Microsoft 365 também usam a inteligência obtida na análise de tendência por meio do monitoramento de segurança e registro em log para detectar anormalidades nos sistemas de informações do Microsoft 365 que podem indicar um ataque ou um incidente de segurança. Os servidores do Microsoft 365 agregam a saída desses logs no ambiente de produção em um servidor de registro em log centralizado. Neste servidor de registro em log centralizado, os logs são examinados para detectar tendências em todo o ambiente de produção. Os dados agregados no servidor centralizado são transmitidos com segurança para um serviço de registro em log para consulta avançada, criação de painel e detecção de atividade anômala e mal-intencionada. O serviço também usa aprendizado de máquina para detectar anomalias com a saída de log.

Durante a fase de escalonamento e dependendo da natureza do incidente de segurança, a equipe de Resposta de Segurança do Microsoft 365 pode envolver um ou mais especialistas em assuntos de várias equipes da Microsoft:

- Equipe de Segurança e Conformidade de Serviços Online
- Microsoft Threat Intelligence Center (MSTIC)
- Centro de Resposta de Segurança da Microsoft (MSRC)
- Assuntos Corporativos, Externos e Jurídicos (CELA)
- Segurança do Azure
- Engenharia do Microsoft 365 e outros.

Antes que qualquer escalonamento para a equipe de Resposta de Segurança do Microsoft 365 ocorra, a equipe de serviço é responsável por determinar e definir o nível de gravidade do incidente de segurança com base em critérios definidos, como:

- Privacidade
- Impacto
- Escopo
- Número de locatários afetados
- Região
- Serviço
- Detalhes do incidente
- Regulamentações específicas do mercado ou do setor do cliente.

A priorização de incidentes é determinada usando fatores distintos, incluindo, mas não se limitando ao impacto funcional do incidente, ao impacto informacional do incidente e à capacidade de recuperação do incidente.

Após receber uma escalada sobre um incidente de segurança, a equipe de Segurança do Microsoft 365 organiza uma equipe virtual (v-team) composta por membros da equipe de Resposta de Segurança do Microsoft 365, equipes de serviço e a equipe de Comunicação de Incidentes do Microsoft 365. A parte mais complexa das atividades dessa equipe V é confirmar o incidente de segurança e eliminar quaisquer falsos positivos. A precisão das informações fornecidas pelos indicadores determinados na fase de preparação é fundamental. Analisando essas informações por categoria de ataque vetorial, a equipe v pode determinar se o incidente de segurança é uma preocupação legítima.

No início da investigação, a equipe de Resposta a Incidentes de Segurança do Office registra todas as informações sobre o incidente de acordo com nossas políticas de gerenciamento de casos. À medida que o caso avança, acompanhamos as ações em andamento e acompanhamos os padrões de tratamento de evidências para coletar, reter e proteger esses dados durante todo o ciclo de vida do incidente.

Alguns exemplos dessas ações incluem:

- Um resumo, que é uma breve descrição do incidente e seu impacto potencial
- A gravidade e a prioridade do incidente, que são derivadas pela avaliação do impacto potencial
- Uma lista de todos os indicadores identificados que levaram à detecção do incidente
- Uma lista de incidentes relacionados
- Uma lista de todas as ações realizadas pela equipe v
- Qualquer evidência coletada, que também será preservada para análise pós-mortem e futuras investigações forenses
- Próximas etapas e ações recomendadas

Após a confirmação de incidentes de segurança, os principais objetivos da equipe de Resposta de Segurança do Microsoft 365 e da equipe de serviço apropriada devem conter o ataque, proteger os serviços sob ataque e evitar um impacto global maior. Ao mesmo tempo, as equipes de engenharia apropriadas trabalham para determinar a causa raiz e preparar o primeiro plano de recuperação.

Na próxima fase, a equipe de Resposta de Segurança do Microsoft 365 identifica os clientes afetados pelo incidente de segurança, se for o caso. O escopo de efeito pode levar algum tempo para determinar, com base na região, datacenter, serviço, farm de servidores, servidor e assim por diante. A lista de clientes afetados é compilada pela equipe de serviço e pela equipe de Comunicações CxP do Microsoft 365, que, em seguida, lida com o processo de notificação do cliente dentro de obrigações contratuais e de conformidade.

## <a name="related-articles"></a>Artigos relacionados

- [Gerenciamento de incidentes do Centro de segurança do Microsoft 365](assurance-security-incident-management.md)
- [Preparação do gerenciamento de incidentes de segurança do Microsoft 365](assurance-sim-preparation.md)
- [Contenção, erradicação e recuperação de gerenciamento de incidentes de segurança do Microsoft 365](assurance-sim-containment-eradication-recovery.md)
- [Atividade pós-incidente de gerenciamento de incidentes de segurança do Microsoft 365](assurance-sim-post-incident-activity.md)
