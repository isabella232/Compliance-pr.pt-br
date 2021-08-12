---
title: Resiliência de serviço integrado no Microsoft 365
description: Descrição Microsoft 365 Resiliência de Serviço
author: robmazz
ms.author: robmazz
manager: laurawi
ms.reviewer: sosstah
f1.keywords:
- NOCSH
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Strat_O365_Enterprise
- MS-Compliance
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 59316ed6c9a2935047cc9c3c137f886eecd3e77d427d3ac6e8c3808bf29f9b7d
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/05/2021
ms.locfileid: "54290909"
---
# <a name="built-in-service-resiliency-in-microsoft-365"></a>Resiliência de serviço integrado no Microsoft 365

Como seu provedor de colaboração na nuvem, a Microsoft reconhece a necessidade de obter continuamente a sua confiança, fornecendo soluções que funcionam de maneira consistente e que seus usuários adoram. Quando um determinado serviço não está disponível, ele é chamado de tempo de inatividade. A definição do tempo de inatividade varia de acordo com o serviço do Microsoft 365, mas normalmente se concentra em qualquer período de tempo em que os usuários não conseguem usar a funcionalidade essencial do serviço. Por exemplo, esta é a definição de tempo de inatividade do SharePoint Online, extraída do contrato de nível de serviço do Microsoft 365:

**"Tempo de inatividade do SharePoint Online**: qualquer período de tempo em que os usuários não consigam ler ou gravar nenhuma parte de um conjunto de sites do SharePoint Online para o qual têm as permissões apropriadas."

Você pode encontrar as definições de tempo de inatividade para cada serviço nos [Acordos de nível de serviço](https://www.microsoftvolumelicensing.com/DocumentSearch.aspx?Mode=3&DocumentTypeId=37).

Para minimizar o tempo de inatividade, seja planejado ou inesperado, os serviços do Microsoft 365 são projetados e operados para estarem altamente disponíveis e serem resilientes a falhas, concentrando-se em quatro áreas:

## <a name="activeactive-design"></a>Design ativo/ativo

Em Microsoft 365, estamos voltando para ter todos os serviços projetados e operados em um design ativo/ativo que aumenta a resiliência. Esse design significa que sempre há várias instâncias de um serviço em execução que podem responder às solicitações do usuário e que elas são hospedadas em datacenters geograficamente dispersos. Todo o tráfego de usuário é fornecido pelo serviço de Porta Frontal da Microsoft e é roteado automaticamente para a instância com localização ideal para o serviço e para se desviar de qualquer falha de serviço a fim de evitar ou reduzir o impacto em nossos clientes.

## <a name="reduce-incident-scope"></a>Redução do escopo do incidente

O escopo de um incidente de serviço é medido de acordo com a gravidade, duração e número de clientes afetados. Gostaríamos de limitar o escopo de todos os incidentes ao:

- ter várias instâncias de cada serviço particionadas umas das outras
- implantar atualizações de forma controlada e graduada usando anéis de validação, para que seja possível detectar e atenuar todos os problemas que possam surgir com a atualização logo no início do processo de implantação. Esse design permite a regressão da atualização, se necessário, e ocorre primeiro em um pequeno grupo dentro da Microsoft (anel interno) antes de ser implantado para grupos maiores, como todos os 140.000 funcionários da Microsoft (anel 2), em seguida, para anéis de adoção antecipados (anel 3) e, por fim, para todos os clientes globalmente (anel 4).
- gerando melhorias no monitoramento por meio da automação. Microsoft 365 é um serviço grande e o tempo de atividade de destino SLA é alto. No início de um incidente de serviço, se houvesse a necessidade de intervenção humana na detecção e resposta, não conseguiríamos responder de forma rápida o suficiente para atender aos SLAs. A automação é a chave para a detecção e resposta rápidas e eficazes de incidentes de serviço. Quanto mais cedo soubermos de algo, mais rápido poderemos corrigir o problema.

Juntamente com os recursos ativos/ativos integrados Microsoft 365 arquitetura de serviço, esses esforços atenuam a gravidade, a duração e o número de clientes afetados durante um incidente de serviço.  

## <a name="fault-isolation"></a>Isolamento de falhas

Assim como os serviços são projetados e operados de maneira ativa/ativa e são divididos entre si para evitar que uma falha afete outra, a base de código do serviço é desenvolvida usando princípios de particionamento semelhantes, os chamados isolamento de falhas. As medidas de isolamento de falha são proteções incrementais feitas dentro da própria base de código. Essas medidas ajudam a impedir que um problema em uma área se propague para outras áreas de operação.
As medidas de isolamento de falhas são aplicadas em vários estágios do desenvolvimento e entrega de um serviço, incluindo desenvolvimento de código, implantação de serviço, balanceamento de carga e replicação de banco de dados.

O SDL (Microsoft Security Development Lifecycle) promove a resiliência e consiste em um conjunto de práticas que oferece suporte a requisitos de segurança e conformidade. O SDL orienta nossos desenvolvedores na criação de serviços resilientes, seguros e em conformidade. Os principais elementos do SDL incluem revisões de códigos, modelagem de ameaças, testes de penetração e processos padronizados de resposta a incidentes na nuvem da Microsoft.

Microsoft 365 serviços são altamente interconectados, mas os sistemas e a tecnologia por trás deles são projetados de forma a limitar o impacto de um incidente de serviço de vazamento para outros serviços. Por exemplo, um problema que afeta o Exchange Online não afetará a funcionalidade principal no Teams, ou um problema com a funcionalidade de pesquisa no SharePoint Online não afetará a capacidade dos usuários de carregar ou baixar arquivos.

## <a name="continuous-service-improvement"></a>Melhoria contínua do serviço

Levamos a sério quando um incidente ocorre. Afinal, nossa arquitetura de nuvem redundante e processos internos rigorosos visam manter nossos serviços acessíveis. Durante um incidente, nosso monitoramento detecta rapidamente os serviços afetados e, se seu locatário for afetado, você será notificado imediatamente por meio de vários canais. Simultaneamente, os engenheiros seguem processos bem definidos para analisar o problema e tomar as medidas necessárias para restaurar a operação normal assim que possível. Depois que o serviço volta a funcionar normalmente, realizamos revisões pós-incidente como parte do ciclo de melhoria contínua do serviço. Durante a revisão pós-incidente, identificamos as causas principais do incidente e o que foi necessário para corrigir os problemas. Em seguida, usamos o que foi aprendido com a situação e aplicamos ao design e às operações de todo o nosso pacote de ofertas. Com esse conhecimento, podemos impedir que a mesma causa raiz impacte outros serviços e clientes adicionais.
