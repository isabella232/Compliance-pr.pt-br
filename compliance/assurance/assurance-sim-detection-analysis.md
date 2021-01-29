---
title: 'Gerenciamento de incidentes de segurança do Microsoft 365: detecção e análise'
description: Este artigo fornece uma visão geral do processo de detecção e análise do gerenciamento de incidentes de segurança no Microsoft 365.
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
ms.openlocfilehash: 1fbdca0c0b08c793732ba31414bedd943d4dc115
ms.sourcegitcommit: d67e4d4fdc664f1da450c8ef2f6732e19bdd403a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/28/2021
ms.locfileid: "50037571"
---
# <a name="microsoft-365-security-incident-management-detection-and-analysis"></a>Gerenciamento de incidentes de segurança do Microsoft 365: detecção e análise

Para detectar atividades mal-intencionadas, o Microsoft 365 registra centralmente eventos de segurança e outros dados e realiza várias técnicas analíticas para encontrar atividades anômalas ou suspeitas. Os arquivos de log são coletados dos servidores e dispositivos de infraestrutura do Microsoft 365 e armazenados em um banco de dados central e consolidado.

A Microsoft toma uma abordagem baseada em risco para detectar atividades mal-intencionadas. Usamos dados de incidentes e inteligência contra ameaças para definir e priorizar nossas detecções.

Empregar uma equipe de pessoas experientes, proficientes e qualificadas é um dos pilares mais importantes para o sucesso na fase de detecção e análise. O Microsoft 365 emprega várias equipes de serviço, e essas equipes incluem funcionários com competências em todos os componentes da pilha, incluindo a rede, roteadores, firewalls, balanceadores de carga, sistemas operacionais e aplicativos.

Os mecanismos de detecção de segurança no Microsoft 365 também incluem notificações e alertas iniciados por fontes diferentes. A equipe de Resposta de Segurança do Microsoft 365 é o principal orquestrador do processo de escalonamento de incidentes de segurança. Essa equipe recebe todos os escalonamentos e é responsável por analisar e confirmar a validade do incidente de segurança.

Um dos principais pilares da detecção é a notificação:

- Cada equipe de serviço é responsável por registrar qualquer ação ou evento dentro do serviço com base nos requisitos da equipe de Segurança do Microsoft 365. Todos os logs criados pelas diferentes equipes de serviço são processados por uma solução siem (gerenciamento de eventos e informações de segurança) com regras de detecção e segurança predefinidos. Essas regras evoluem com base na recomendação da equipe de Segurança do Microsoft 365, em informações aprendidas de incidentes de segurança anteriores, para determinar se há atividades suspeitas ou maliciosas.
- Se um cliente determinar que um incidente de segurança está em andamento, ele poderá abrir um caso de suporte com a Microsoft, que é atribuída à equipe de Comunicações da Experiência do Usuário do Microsoft 365 (CxP) e transformada em um escalonamento para todas as equipes apropriadas.

As equipes de serviço do Microsoft 365 também usam a inteligência obtida na análise de tendências por meio do monitoramento de segurança e registro em log para detectar anormais nos sistemas de informações do Microsoft 365 que podem indicar um ataque ou um incidente de segurança. Os servidores do Microsoft 365 agregam a saída desses logs no ambiente de produção em um servidor de registro em log centralizado. Desse servidor de registro centralizado, os logs são examinados para identificar tendências em todo o ambiente de produção. Os dados agregados no servidor centralizado são transmitidos com segurança para um serviço de registro em log para consulta avançada, criação de painéis e detecção de atividades anômalas e maliciosas. O serviço também usa o aprendizado de máquina para detectar anomalias com saída de log.

Durante a fase de escalonamento e dependendo da natureza do incidente de segurança, a equipe de Resposta de Segurança do Microsoft 365 pode envolver um ou mais especialistas no assunto de várias equipes da Microsoft:

- Equipe de Segurança e Conformidade dos Serviços Online
- Central de Inteligência contra Ameaças da Microsoft (MSTIC)
- Microsoft Security Response Center (MSRC)
- Assuntos Corporativos, Externos e Jurídicos (CASO)
- Segurança do Azure
- Engenharia do Microsoft 365 e outros.

Antes de qualquer escalonamento para a equipe de Resposta de Segurança do Microsoft 365 ocorrer, a equipe de serviço é responsável por determinar e definir o nível de gravidade do incidente de segurança com base em critérios definidos, como:

- Privacidade
- Impacto
- Escopo
- Número de locatários afetados
- Região
- Serviço
- Detalhes do incidente
- Regulamentações específicas do mercado ou do setor do cliente.

A priorização de incidentes é determinada pelo uso de fatores distintos, incluindo, entre outros, o impacto funcional do incidente, o impacto informacional do incidente e a capacidade de recuperação do incidente.

Depois de receber um escalonamento sobre um incidente de segurança, a equipe de Segurança do Microsoft 365 organiza uma equipe virtual (v-team) composta por membros da equipe de Resposta de Segurança do Microsoft 365, equipes de serviço e a equipe de Comunicação de Incidentes do Microsoft 365. A parte mais complexa das atividades dessa equipe v é confirmar o incidente de segurança e eliminar falsos positivos. A precisão das informações fornecidas pelos indicadores determinados na fase de preparação é fundamental. Analisando essas informações por categoria de ataque de vetor, a equipe v pode determinar se o incidente de segurança é uma preocupação legítima.

No início da investigação, a equipe de Resposta a Incidentes de Segurança do Office registra todas as informações sobre o incidente de acordo com nossas políticas de gerenciamento de caso. À medida que o caso progride, acompanhamos as ações em andamento e seguiremos os padrões de tratamento de evidências para coletar, reter e proteger esses dados durante todo o ciclo de vida do incidente.

Alguns exemplos dessas ações incluem:

- Um resumo, que é uma breve descrição do incidente e seu impacto potencial
- A gravidade e a prioridade do incidente, derivadas da avaliação do impacto potencial
- Uma lista de todos os indicadores identificados, o que levou à detecção do incidente
- Uma lista de incidentes relacionados
- Uma lista de todas as ações tomadas pela equipe v
- Todas as evidências coletadas, que também serão preservadas para análise pós-mortem e investigações forenses futuras
- Próximas etapas e ações recomendadas

Após a confirmação do incidente de segurança, os principais objetivos da equipe de Resposta de Segurança do Microsoft 365 e da equipe de serviço apropriada são conter o ataque, proteger os serviços sob ataque e evitar um impacto global maior. Ao mesmo tempo, as equipes de engenharia apropriadas trabalham para determinar a causa raiz e preparar o primeiro plano de recuperação.

Na próxima fase, a equipe de Resposta de Segurança do Microsoft 365 identifica os clientes afetados pelo incidente de segurança, se algum. O escopo do efeito pode levar algum tempo para determinar, com base na região, datacenter, serviço, farm de servidores, servidor e assim por diante. A lista de clientes afetados é compilada pela equipe de serviços e pela equipe de Comunicações CxP do Microsoft 365, que então lida com o processo de notificação do cliente dentro de obrigações contratuais e de conformidade.

## <a name="related-articles"></a>Artigos relacionados

- [Gerenciamento de incidentes do Centro de segurança do Microsoft 365](assurance-security-incident-management.md)
- [Preparação do gerenciamento de incidentes de segurança do Microsoft 365](assurance-sim-preparation.md)
- [Contenção, eliminação e recuperação do gerenciamento de incidentes de segurança do Microsoft 365](assurance-sim-containment-eradication-recovery.md)
- [Atividade pós-incidente de gerenciamento de incidentes de segurança do Microsoft 365](assurance-sim-post-incident-activity.md)
