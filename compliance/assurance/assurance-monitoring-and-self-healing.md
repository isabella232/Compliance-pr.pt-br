---
title: Monitoramento de dados e auto-recuperação em Microsoft 365
description: Neste artigo, você aprenderá sobre os recursos de monitoramento e auto-recuperação de Microsoft 365.
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
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom:
- seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: d55621d10284c427afedeb3d60807411841d41dda2e07c52b293a676448dbe73
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/05/2021
ms.locfileid: "54290619"
---
# <a name="data-monitoring-and-self-healing-in-microsoft-365"></a>Monitoramento de dados e auto-recuperação em Microsoft 365

Dada a escala de Microsoft 365, seria impossível manter os dados do cliente resilientes e seguros contra malware sem monitoramento integrado abrangente, alertando que é inteligente e auto-recuperação rápido e confiável. Monitorar um conjunto de serviços na escala de Microsoft 365 é muito desafiador. Novos conjuntos de ideias e metodologias precisavam ser introduzidos e novos conjuntos de tecnologia necessários para serem criados para operar e gerenciar o serviço em um ambiente global conectado. Nos afastamos da abordagem de monitoramento tradicional da coleta e filtragem de dados para criar alertas para uma abordagem baseada na análise de dados; levando sinais e criando confiança nos dados e, em seguida, usando a automação para recuperar ou resolver o problema. Essa abordagem ajuda a tirar os humanos da equação de recuperação, o que, por sua vez, torna as operações menos caras, mais rápidas e menos propensas a erros. 

Fundamental para Microsoft 365 monitoramento é uma coleção de tecnologias que compõem nosso Mecanismo de Insights de dados, que é criado com a tecnologia de banco de dados de streaming do Azure, SQL Azure e de código [aberto.](https://cassandra.apache.org/) Ele foi projetado para coletar e agregar dados e chegar a conclusões. Atualmente, ele processa mais de 500 milhões de eventos por hora de mais de 100.000 servidores (~15 TB por dia) espalhados por dezenas de datacenters em muitas regiões, e esses números estão crescendo. 

Microsoft 365 usa *monitoramento externo*, que envolve a criação de transações sintéticas para testar tudo o que é importante. Por exemplo, em Exchange Online cada cenário está testando todos os bancos de dados em todo o mundo a cada cinco minutos de forma dispersa, fornecendo uma cobertura quase contínua de tudo o que reside no sistema. Em vários locais, 250 milhões de transações de teste por dia são executadas para criar uma linha de base robusta ou pulsação para o serviço. 

Microsoft 365 também usa o conceito de *Alerta* Vermelho , que reduz todos os sinais de monitoramento de todos os máquinas em nossos datacenters para algo gerenciável por um ser humano. O conceito é bastante simples: se algo estiver acontecendo em vários sinais, deve haver algo acontecendo. Não se trata de criar confiança em um sinal, trata-se de ter fidelidade razoável para cada sinal para que você tenha maior precisão. Esse sistema de monitoramento é tão poderoso que não temos equipe 24 horas por dia, 7 dias por dia, 7 dias por semana. tudo o que temos é o computador que é a primeira vez que ele detecta um problema, nesse caso, ele irá páginar o pessoal de chamada apropriado ou, mais frequentemente, como é o caso, ele simplesmente irá em frente e resolverá o problema. Depois de começar a coletar sinais e criar alertas vermelhos deles, podemos começar a triangular em todas as nossas partições de serviço. 

Com base na combinação do alerta de falha e dos Alertas Vermelhos, esse alerta indica exatamente quais componentes podem estar com um problema e que o sistema tentará corrigir o problema sozinho reiniciando um servidor de caixa de correio. 

Além dos recursos de auto-recuperação, como restauração de página única, o Exchange Online inclui vários recursos que abordam o monitoramento e a auto-recuperação que se concentra na preservação da experiência do usuário final. Esses recursos incluem *Disponibilidade* Gerenciada , que fornece ações de monitoramento e recuperação integradas, e AutoReseed, que restaura automaticamente a redundância do banco de dados após uma falha no disco. 

## <a name="managed-availability"></a>Disponibilidade gerenciada 

A disponibilidade gerenciada fornece uma solução nativa de verificação e recuperação de saúde que monitora e protege a experiência do usuário final por meio de ações orientadas para recuperação. Disponibilidade gerenciada é a integração de ações de monitoramento e recuperação integradas com a plataforma Exchange alta disponibilidade. O recurso foi projetado para detectar e se recuperar de problemas assim que eles ocorrem e são descobertos pelo sistema. Diferentemente das soluções e técnicas anteriores de monitoramento externo do Exchange, a disponibilidade gerenciada não tenta identificar ou comunicar a causa raiz de um problema. Em vez disso, ele se concentra em aspectos de recuperação que abordam três áreas principais da experiência do usuário final:

- **Disponibilidade** - Os usuários podem acessar o serviço? 
- **Latência** - Como é a experiência para os usuários? 
- **Erros** - Os usuários são capazes de realizar o que querem? 

A disponibilidade gerenciada é um recurso interno que é executado em todos os Microsoft 365 que executam Exchange Online. Ela examina e analisa centenas de métricas de integridade a cada segundo. Se algo estiver errado, a maioria das vezes é corrigida automaticamente. Mas sempre haverá problemas que a disponibilidade gerenciada não poderá corrigir por conta própria. Nesses casos, a disponibilidade gerenciada aumentará o problema para uma equipe de Microsoft 365 suporte por meio do registro em log de eventos.

## <a name="autoreseed"></a>Propagação automática

Exchange Online servidores são implantados em uma configuração que armazena vários bancos de dados e seus fluxos de log no mesmo disco não RAID. Essa configuração geralmente é conhecida como apenas um grupo de *discos* (JBOD), pois nenhum mecanismo de redundância de armazenamento, como RAID, está sendo usado para duplicar os dados no disco. Quando um disco falha em um ambiente JBOD, os dados nesse disco são perdidos. 

Dado o tamanho da Exchange Online e o fato de que implantado dentro dela há milhões de unidades de disco, as falhas na unidade de disco são uma ocorrência regular no Exchange Online. Na verdade, mais de 100 falham todos os dias. Quando um disco falha em uma implantação corporativa local, um administrador deve substituir manualmente o disco com falha e restaurar os dados afetados. Em uma implantação de nuvem do tamanho Microsoft 365, ter operadores (administradores de nuvem) substituindo manualmente discos não é prático nem viável economicamente. 

Reseed automático, ou *AutoReseed*, é um recurso que é a substituição do que normalmente é ação orientada pelo operador em resposta a uma falha de disco, evento de corrupção de banco de dados ou outro problema que exige uma nova semeada de uma cópia de banco de dados. A AutoReseed foi projetada para restaurar automaticamente a redundância de banco de dados após uma falha de disco usando discos sobressalentes provisionados no sistema. Se um disco falhar, as cópias de banco de dados armazenadas nesse disco serão automaticamente reseadas para um disco sobressalente pré-configurado no servidor, restaurando a redundância. 