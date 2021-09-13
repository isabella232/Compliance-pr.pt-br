---
title: Simulação de ataque no Microsoft 365
description: Neste artigo, saiba como a Microsoft monitora e testa continuamente os limites de locatários Microsoft 365.
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
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: ff5860197375d6504bc85f257a442915dfff50cc
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/12/2021
ms.locfileid: "59158143"
---
# <a name="attack-simulation-in-microsoft-365"></a>Simulação de ataque no Microsoft 365

A Microsoft monitora continuamente e testa explicitamente as deficiências e vulnerabilidades nos limites dos locatários, incluindo o monitoramento de intrusão, tentativas de violação de permissão e falta de recursos. Também usamos vários sistemas internos para monitorar continuamente a utilização inadequada de recursos, que, se detectado, dispara a throttling interna.

Microsoft 365 tem sistemas de monitoramento internos que monitoram continuamente qualquer falha e impulsionam a recuperação automatizada quando a falha é detectada. Microsoft 365 os sistemas analisam desvios no comportamento do serviço e iniciam processos de auto-recuperação integrados ao sistema. Microsoft 365 também usa monitoramento externo no qual o monitoramento é executado de vários locais, tanto de serviços de terceiros confiáveis (para verificação independente de SLA) quanto de nossos próprios datacenters para levantar alertas. Para diagnósticos, temos registro em log, auditoria e rastreamento extensivos. O rastreamento e o monitoramento granulares nos ajudam a isolar problemas e executar uma análise de causa raiz rápida e eficaz.

Embora o Microsoft 365 tenha automatizado as ações de recuperação sempre que possível, os engenheiros de chamada da Microsoft estão disponíveis 24 horas por dia, 7 dias por semana, para investigar todas as escalonamentos de segurança da Gravidade 1, e as análises pós-mortem de cada incidente de serviço contribuem para o aprendizado contínuo e melhoria. Essa equipe inclui engenheiros de suporte, desenvolvedores de produtos, gerentes de programas, gerentes de produto e liderança sênior. Nossos profissionais de chamada fornecem backup em tempo há tempo e, muitas vezes, podem automatizar ações de recuperação, para que, na próxima vez que um evento ocorrer, ele possa ser auto-recuperado.

A Microsoft realiza uma revisão completa após o incidente sempre que um incidente de segurança Microsoft 365 ocorre independentemente da magnitude do impacto. Uma revisão pós-incidente consiste em uma análise do que aconteceu, como respondemos e como evitamos incidentes semelhantes no futuro. No interesse da transparência e da responsabilidade, compartilharemos avaliações pós-incidentes para quaisquer incidentes de serviço importantes com clientes afetados. Para obter detalhes específicos, consulte [Gerenciamento de incidentes de segurança da Microsoft.](assurance-security-incident-management.md)

## <a name="assume-breach-methodology"></a>Suponha que a metodologia de violação

Com base na análise detalhada das tendências de segurança, a Microsoft defende e destaca a necessidade de outros investimentos em processos e tecnologias de segurança reativa que se concentrem na detecção e na resposta a ameaças emergentes, em vez de apenas na prevenção dessas ameaças. Devido às alterações no cenário de ameaças e análise aprofundada, a Microsoft refinou sua estratégia de segurança além de impedir apenas violações de segurança para um melhor equipado para lidar com violações quando elas ocorrem; uma estratégia que considera os principais eventos de segurança não como uma questão de se, mas quando.

Embora as práticas [de](https://www.microsoft.com/TrustCenter/Security/default.aspx) violação da Microsoft tenham sido realizadas por muitos anos, muitos clientes não estão cientes do trabalho que está sendo feito nos bastidores para proteger a nuvem da Microsoft. Suponha que a violação seja um mindset que orienta investimentos em segurança, decisões de design e práticas de segurança operacional. Suponha que a violação limite a confiança colocada em aplicativos, serviços, identidades e redes tratando-as todas , internas e externas, como inseguras e já comprometidas. Embora a estratégia de violação não tenha sido assumida de uma violação real de qualquer empresa da Microsoft ou serviços de nuvem, foi reconhecido que muitas organizações, em todo o setor, estavam sendo violadas apesar de todas as tentativas de impedi-la. Embora a prevenção de violações seja uma parte crítica das operações de qualquer organização, essas práticas devem ser continuamente testadas e aumentadas para lidar efetivamente com adversários modernos e ameaças persistentes avançadas. Para que qualquer organização se prepare para uma violação, ela deve primeiro criar e manter procedimentos robustos, repetitivos e de resposta de segurança completamente testados.

Embora impeça processos de segurança de violação, como modelagem de ameaças, análises de código e testes de segurança são muito úteis como parte do Ciclo de Vida do Desenvolvimento de [Segurança,](https://www.microsoft.com/securityengineering/sdl/)suponha que a violação fornece várias vantagens que ajudam a contabilização da segurança geral, exercendo e medindo recursos reativos no caso de uma violação.

Na Microsoft, nos definimos para fazer isso por meio de exercícios de jogos de guerra em andamento e testes de penetração de site ao vivo de nossos planos de resposta de segurança com o objetivo de melhorar nosso recurso de detecção e resposta. A Microsoft simula regularmente violações do mundo real, realiza monitoramento contínuo de segurança e práticas de gerenciamento de incidentes de segurança para validar e melhorar a segurança do Microsoft 365, do Azure e de outros serviços de nuvem da Microsoft.

A Microsoft executa sua estratégia de segurança de violação de pressupo usando dois grupos principais:

- Red Teams (invasores)
- Azul Teams (defensores)

Tanto Microsoft Azure quanto Microsoft 365 equipe separada em tempo integral red Teams e blue Teams.

Conhecida como "[Red Teaming](https://go.microsoft.com/fwlink/?linkid=518599)", a abordagem é testar sistemas e operações do Azure e Microsoft 365 usando as mesmas táticas, técnicas e procedimentos como adversários reais, em relação à infraestrutura de produção ao vivo, sem o conhecimento das equipes de Engenharia ou Operações. Isso testa os recursos de detecção e resposta de segurança da Microsoft e ajuda a identificar vulnerabilidades de produção, erros de configuração, suposições inválidas e outros problemas de segurança de forma controlada. Cada violação da Equipe Vermelha é seguida pela divulgação completa entre ambas as equipes para identificar lacunas, resolver descobertas e melhorar a resposta a violações.

**OBSERVAÇÃO**: Nenhum dado do cliente é direcionado deliberadamente durante o Red Teaming ou teste de penetração de site ao vivo. Os testes são contra Microsoft 365 e plataformas e infraestruturas do Azure, bem como os próprios locatários, aplicativos e dados da Microsoft. Os locatários, aplicativos e conteúdo do cliente hospedados no Microsoft 365 ou no Azure nunca são direcionados.

## <a name="red-teams"></a>Red Teams

A Equipe Vermelha é um grupo de funcionários em tempo integral da Microsoft que se concentra em violar a infraestrutura, a plataforma e os próprios locatários e aplicativos da Microsoft. Eles são o adversário dedicado (um grupo de hackers éticas) executando ataques direcionados e persistentes contra Serviços Online (infraestrutura, plataformas e aplicativos da Microsoft, mas não aplicativos ou conteúdo dos clientes finais).

A função da Equipe Vermelha é atacar e penetrar ambientes usando as mesmas etapas de um adversário:

![Estágios de violação.](../media/office-365-isolation-breach-stages.png)

Entre outras funções, as equipes vermelhas tentam especificamente violar limites de isolamento de locatários para encontrar bugs ou lacunas em nosso design de isolamento.

Para ajudar a dimensionar os esforços de simulação de ataque, a Equipe Vermelha criou uma ferramenta de emulação de ataque automatizada que é executado com segurança em ambientes Microsoft 365 específicos de forma recorrente. A ferramenta tem uma ampla variedade de ataques predefinidos que são constantemente expandidos e aprimorados para ajudar a refletir o cenário de ameaças em evolução. Além de ampliar a cobertura do teste de Equipe Vermelha, ele ajuda a Equipe Azul a validar e melhorar sua lógica de monitoramento de segurança. A emulação de ataque regular e contínua fornece à Equipe Azul um fluxo consistente e diversificado de sinais que são comparados e validados em relação às respostas esperadas. Isso ajuda a levar a melhorias Microsoft 365 lógica e recursos de resposta de monitoramento de segurança do Microsoft 365.

## <a name="blue-teams"></a>Azul Teams

A Equipe Azul é composta por um conjunto dedicado de respondentes de segurança ou membros de todas as organizações de resposta a incidentes de segurança, Engenharia e Operações. Independentemente da sua make-up, eles são independentes e operam separadamente da Equipe Vermelha. A Equipe Azul segue os processos de segurança estabelecidos e usa as ferramentas e tecnologias mais recentes para detectar e responder a ataques e penetração. Assim como os ataques do mundo real, a Equipe Azul não sabe quando ou como os ataques da Equipe Vermelha ocorrerão ou quais métodos podem ser usados. O trabalho deles, seja um ataque da Equipe Vermelha ou um ataque real, é detectar e responder a todos os incidentes de segurança. Por esse motivo, a Equipe Azul está continuamente em chamada e deve reagir às violações da Equipe Vermelha da mesma maneira que faria para qualquer outra violação.

Quando um adversário, como uma Equipe Vermelha, violou um ambiente, a Equipe Azul deve:

- Coletar evidências deixadas pelo adversário
- Detectar a evidência como uma indicação de comprometimento
- Alertar as equipes de Engenharia e Operação apropriadas
- Triagem dos alertas para determinar se eles garantem uma investigação posterior
- Coletar contexto do ambiente para escopo da violação
- Formar um plano de correção para conter ou despejar o adversário
- Execute o plano de correção e recupere-se da violação

Estas etapas formam a resposta a incidentes de segurança que é paralela à do adversário, conforme mostrado abaixo:

![Estágios de resposta de violação.](../media/office-365-isolation-breach-response-stages.png)

As violações da Equipe Vermelha permitem exercitar a capacidade da Equipe Azul de detectar e responder a ataques do mundo real de ponta a ponta. O mais importante é que ele permite a resposta a incidentes de segurança prática antes de uma violação genuína. Além disso, devido às violações da Equipe Vermelha, a Equipe Azul aprimora sua percepção de situação, o que pode ser valioso ao lidar com futuras violações (seja da Equipe Vermelha ou de outro adversário). Durante todo o processo de detecção e resposta, a Equipe Azul produz inteligência a actionable e ganha visibilidade sobre as condições reais dos ambientes que estão tentando defender. Frequentemente, isso é realizado por meio da análise de dados e da perícia, realizadas pela Equipe Azul, ao responder a ataques da Equipe Vermelha e estabelecendo indicadores de ameaça, como indicadores de comprometimento. Assim como a Equipe Vermelha identifica lacunas no artigo de segurança, as equipes azuis identificam lacunas na capacidade de detectar e responder. Além disso, como o modelo vermelho de equipes ataques do mundo real, a Equipe Azul pode ser avaliada com precisão sobre sua capacidade ou incapacidade de lidar com adversários determinados e persistentes. Por fim, as violações da Equipe Vermelha medem a preparação e o impacto de nossa resposta de violação.
