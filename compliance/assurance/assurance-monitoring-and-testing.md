---
title: Simulação de ataque no Microsoft 365
description: Neste artigo, saiba como a Microsoft monitora e testa continuamente os limites de locatários do Microsoft 365.
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
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 9d38131a6ec8f3213c288d76dc3b176ceaa3aace
ms.sourcegitcommit: b06fa9f1b230fd5e470817486ea51f460f28b691
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/27/2021
ms.locfileid: "50012887"
---
# <a name="attack-simulation-in-microsoft-365"></a>Simulação de ataque no Microsoft 365

A Microsoft monitora continuamente e testa explicitamente pontos fracos e vulnerabilidades nos limites do locatário, incluindo o monitoramento de invasão, tentativas de violação de permissão e falta de recursos. Também usamos vários sistemas internos para monitorar continuamente a utilização inadequada de recursos, que, se detectada, dispara a throttling interna.

O Microsoft 365 tem sistemas de monitoramento internos que monitoram continuamente qualquer falha e impulsionam a recuperação automatizada quando uma falha é detectada. Os sistemas do Microsoft 365 analisam desvios no comportamento do serviço e iniciam processos de autorrecarregação integrados ao sistema. O Microsoft 365 também usa monitoramento externo no qual o monitoramento é realizado em vários locais, tanto de serviços de terceiros confiáveis (para verificação de SLA independente) quanto de nossos próprios datacenters para a geração de alertas. Para diagnóstico, temos registro em log extensivo, auditoria e rastreamento. O rastreamento granular e o monitoramento nos ajudam a isolar problemas e executar uma análise de causa raiz rápida e eficaz.

Embora o Microsoft 365 automatize as ações de recuperação sempre que possível, os engenheiros de chamada da Microsoft estão disponíveis 24 horas por dia, 7 dias por semana, para investigar todos os escalonamentos de segurança da Gravidade 1, e as revisões pós-mortem de cada incidente de serviço contribuem para o aprendizado contínuo e aprimoramento. Essa equipe inclui engenheiros de suporte, desenvolvedores de produtos, gerentes de programa, gerentes de produto e liderança sênior. Nossos profissionais de chamada fornecem backup em tempo há tempo e, muitas vezes, podem automatizar as ações de recuperação, para que na próxima vez que um evento ocorrer, ele possa ser auto-recuperado.

A Microsoft realiza uma revisão completa após o incidente sempre que um incidente de segurança do Microsoft 365 ocorre independentemente da magnitude do impacto. Uma revisão pós-incidente consiste em uma análise do que aconteceu, de como respondemos e de como evitamos incidentes semelhantes no futuro. No interesse da transparência e da responsabilidade, compartilhamos a revisão pós-incidente de quaisquer incidentes de serviço principais com os clientes afetados. Para obter detalhes específicos, consulte Gerenciamento de Incidentes de Segurança [do Office 365.](https://aka.ms/Office365SIM)

## <a name="assume-breach-methodology"></a>Presumir a metodologia de violação

Com base na análise detalhada das tendências de segurança, a Microsoft defenderá e destacará a necessidade de outros investimentos em processos e tecnologias de segurança reativos que se concentram na detecção e na resposta a ameaças emergentes, em vez de apenas na prevenção dessas ameaças. Devido às alterações no panorama das ameaças e na análise profunda, a Microsoft refinou sua estratégia de segurança, além de impedir apenas as violações de segurança para um melhor preparado para lidar com violações quando elas ocorrem; uma estratégia que considera eventos de segurança importantes não como uma questão de se, mas quando.

Embora as práticas [de](https://www.microsoft.com/TrustCenter/Security/default.aspx) violação de pressuções da Microsoft já tenham sido realizadas há muitos anos, muitos clientes não estão cientes do trabalho que está sendo feito nos bastidores para proteger a nuvem da Microsoft. Pressuporta que a violação é uma mentalidade que orienta investimentos em segurança, decisões de design e práticas operacionais de segurança. Suponha que a violação limita a confiança colocada em aplicativos, serviços, identidades e redes tratando todas elas internas e externas como inseguras e já comprometidas. Embora a estratégia de presumir a violação não tenha sido quebrada de uma violação real de qualquer empresa da Microsoft ou serviços de nuvem, ela foi reconhecida de que muitas organizações, em todo o setor, estavam sendo violadas apesar de todas as tentativas de impedi-la. Embora a prevenção de violações seja uma parte essencial das operações de qualquer organização, essas práticas devem ser testadas e aumentadas continuamente para lidar efetivamente com adversários modernos e ameaças persistentes avançadas. Para que qualquer organização se prepare para uma violação, primeiro ela deve criar e manter procedimentos de resposta de segurança robustos, repetidos e testados exaustivamente.

Embora os processos de segurança impedir violações, como modelagem de ameaças, revisões de código e testes de segurança sejam muito úteis como parte do Ciclo de Vida de Desenvolvimento de [Segurança,](https://www.microsoft.com/securityengineering/sdl/)suponha que a violação fornece várias vantagens que ajudam a contabilização da segurança geral, exerçando e medindo os recursos reativos no caso de uma violação.

Na Microsoft, planejamos fazer isso por meio de exercícios contínuos de jogos de jogos e testes de penetração no site ao vivo de nossos planos de resposta de segurança com o objetivo de melhorar nossa capacidade de detecção e resposta. A Microsoft simula regularmente violações do mundo real, realiza monitoramento contínuo de segurança e práticas de gerenciamento de incidentes de segurança para validar e melhorar a segurança do Microsoft 365, do Azure e de outros serviços em nuvem da Microsoft.

A Microsoft executa sua estratégia de segurança Assume Breach usando dois grupos principais:

- Equipes vermelhas (invasores)
- Equipes azuis (defensores)

Tanto o Microsoft Azure quanto a equipe do Microsoft 365 separam equipes em vermelho em tempo integral e equipes azuis.

Conhecida como["](https://go.microsoft.com/fwlink/?linkid=518599)Equipe Vermelha ", a abordagem é testar sistemas e operações do Azure e do Microsoft 365 usando as mesmas táticas, técnicas e procedimentos que adversários reais, em relação à infraestrutura de produção ao vivo, sem o conhecimento das equipes de Engenharia ou Operações. Isso testa os recursos de detecção e resposta de segurança da Microsoft e ajuda a identificar vulnerabilidades de produção, erros de configuração, suposições inválidas e outros problemas de segurança de maneira controlada. Cada violação de equipe vermelha é seguida por divulgação total entre ambas as equipes para identificar lacunas, resolver descobertas e melhorar a resposta a violações.

**OBSERVAÇÃO:** nenhum dado do cliente é direcionado deliberadamente durante o teaming vermelho ou teste de penetração do site ao vivo. Os testes são contra a infraestrutura e as plataformas do Microsoft 365 e do Azure, bem como os próprios locatários, aplicativos e dados da Microsoft. Locatários, aplicativos e conteúdo do cliente hospedados no Microsoft 365 ou Azure nunca são direcionados.

## <a name="red-teams"></a>Equipes vermelhas

A equipe vermelha é um grupo de funcionários em tempo integral da Microsoft que se concentra em violar a infraestrutura, a plataforma e os próprios locatários e aplicativos da Microsoft. Eles são os adversários dedicados (um grupo de hackers éticos) que executam ataques direcionados e persistentes aos Serviços Online (infraestrutura, plataformas e aplicativos da Microsoft, mas não aplicativos ou conteúdo dos clientes finais).

A função da equipe vermelha é atacar e atacar ambientes usando as mesmas etapas de um adversário:

![Estágios de violação](../media/office-365-isolation-breach-stages.png)

Entre outras funções, as equipes vermelhas tentam especificamente violar os limites de isolamento do locatário para encontrar bugs ou lacunas em nosso design de isolamento.

## <a name="blue-teams"></a>Equipes azuis

A equipe azul é composta por um conjunto dedicado de respondentes ou membros de segurança de toda a resposta a incidentes de segurança, engenharia e organizações de operações. Independentemente da com que eles se comam, eles são independentes e operam separadamente da equipe vermelha. A equipe azul segue os processos de segurança estabelecidos e usa as ferramentas e tecnologias mais recentes para detectar e responder a ataques e penetração. Assim como os ataques do mundo real, a equipe azul não sabe quando ou como os ataques da equipe vermelha ocorrerão ou quais métodos podem ser usados. O trabalho deles, seja um ataque de equipe vermelho ou um verdadeiro ataque, é detectar e responder a todos os incidentes de segurança. Por esse motivo, a equipe azul está continuamente em chamada e deve reagir às violações da equipe vermelha da mesma maneira que faria para qualquer outra violação.

Quando um adversário, como uma equipe vermelha, violou um ambiente, a equipe azul deve:

- Coletar evidências deixadas pelo adversário
- Detectar a evidência como uma indicação de comprometimento
- Alertar as equipes de Engenharia e Operação apropriadas
- Triagem dos alertas para determinar se eles garantem mais investigação
- Coletar contexto do ambiente para escopo da violação
- Formar um plano de correção para conter ou despejar o adversário
- Executar o plano de correção e recuperar-se de uma violação

Essas etapas formam a resposta a incidentes de segurança que é executado em paralelo com a do adversário, conforme mostrado abaixo:

![Estágios de resposta a violações](../media/office-365-isolation-breach-response-stages.png)

As violações da equipe vermelha permitem exercer a capacidade da equipe azul de detectar e responder a ataques do mundo real de ponta a ponta. O mais importante, ele permite a resposta a incidentes de segurança de incidentes de segurança antes de uma violação original. Além disso, devido às violações da equipe vermelha, a equipe azul aprimora seu reconhecimento de situação, o que pode ser valioso ao lidar com futuras violações (seja da equipe vermelha ou de outro adversário). Durante todo o processo de detecção e resposta, a equipe azul produz inteligência a actionable e ganha visibilidade das condições reais dos ambientes que estão tentando defender. Frequentemente, isso é feito por meio de análise de dados e perícia, realizada pela equipe azul, ao responder a ataques da equipe vermelha e ao estabelecer indicadores de ameaças, como indicadores de comprometimento. Assim como a equipe vermelha identifica lacunas na história de segurança, as equipes azuis identificam lacunas em sua capacidade de detectar e responder. Além disso, como os ataques do modelo de equipe vermelha no mundo real, a equipe azul pode ser avaliada com precisão sobre sua capacidade ou incapacidade de lidar com adversários determinados e persistentes. Por fim, as violações da equipe vermelha medem a preparação e o impacto da nossa resposta à violação.
