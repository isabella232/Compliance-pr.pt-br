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
hideEdit: true
ms.openlocfilehash: b37ca23fa403bd0a4a657be78654a02bf23721b3
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497530"
---
# <a name="attack-simulation-in-microsoft-365"></a>Simulação de ataque no Microsoft 365

A Microsoft monitora continuamente e testa explicitamente as deficiências e vulnerabilidades nos limites dos locatários, incluindo o monitoramento de intrusão, tentativas de violação de permissão e falta de recursos. Também usamos vários sistemas internos para monitorar continuamente a utilização inadequada de recursos, que, se detectado, dispara a throttling interna.

O Microsoft 365 tem sistemas de monitoramento internos que monitoram continuamente qualquer falha e impulsionam a recuperação automatizada quando a falha é detectada. Os sistemas do Microsoft 365 analisam desvios no comportamento do serviço e iniciam processos de auto-recuperação integrados ao sistema. O Microsoft 365 também usa monitoramento externo no qual o monitoramento é executado de vários locais, tanto de serviços de terceiros confiáveis (para verificação independente de SLA) quanto de nossos próprios datacenters para levantar alertas. Para diagnósticos, temos registro em log, auditoria e rastreamento extensivos. O rastreamento e o monitoramento granulares nos ajudam a isolar problemas e executar uma análise de causa raiz rápida e eficaz.

Embora o Microsoft 365 tenha automatizado as ações de recuperação sempre que possível, os engenheiros de chamada da Microsoft estão disponíveis 24 horas por dia, 7 dias por semana, para investigar todas as escalonamentos de segurança da Gravidade 1, e as análises pós-mortem de cada incidente de serviço contribuem para o aprendizado contínuo e melhoria. Essa equipe inclui engenheiros de suporte, desenvolvedores de produtos, gerentes de programas, gerentes de produto e liderança sênior. Nossos profissionais de chamada fornecem backup em tempo há tempo e, muitas vezes, podem automatizar ações de recuperação, para que, na próxima vez que um evento ocorrer, ele possa ser auto-recuperado.

A Microsoft realiza uma revisão completa após o incidente sempre que ocorre um incidente de segurança do Microsoft 365, independentemente da magnitude do impacto. Uma revisão pós-incidente consiste em uma análise do que aconteceu, como respondemos e como evitamos incidentes semelhantes no futuro. No interesse da transparência e da responsabilidade, compartilharemos a revisão pós-incidente para todos os principais incidentes de serviço com clientes afetados. Para obter detalhes específicos, consulte [Office 365 Security Incident Management](https://aka.ms/Office365SIM).

## <a name="assume-breach-methodology"></a>Suponha que a metodologia de violação

Com base na análise detalhada das tendências de segurança, a Microsoft defende e destaca a necessidade de outros investimentos em processos e tecnologias de segurança reativa que se concentrem na detecção e na resposta a ameaças emergentes, em vez de apenas na prevenção dessas ameaças. Devido às alterações no cenário de ameaças e análise aprofundada, a Microsoft refinou sua estratégia de segurança além de impedir apenas violações de segurança para um melhor equipado para lidar com violações quando elas ocorrem; uma estratégia que considera os principais eventos de segurança não como uma questão de se, mas quando.

Embora as práticas [de Violação](https://www.microsoft.com/TrustCenter/Security/default.aspx) de Pressuções da Microsoft tenham sido realizadas por muitos anos, muitos clientes não estão cientes do trabalho que está sendo feito nos bastidores para proteger a nuvem da Microsoft. Suponha que a Violação seja um mindset que orienta investimentos em segurança, decisões de design e práticas de segurança operacional. Suponha que a Violação limite a confiança colocada em aplicativos, serviços, identidades e redes tratando-as todas , internas e externas, como inseguras e já comprometidas. Embora a estratégia Assume Breach não tenha sido carregada de uma violação real de qualquer empresa da Microsoft ou serviços de nuvem, foi reconhecido que muitas organizações, em todo o setor, estavam sendo violadas apesar de todas as tentativas de impedi-la. Embora a prevenção de violações seja uma parte crítica das operações de qualquer organização, essas práticas devem ser continuamente testadas e aumentadas para lidar efetivamente com adversários modernos e ameaças persistentes avançadas. Para que qualquer organização se prepare para uma violação, ela deve primeiro criar e manter procedimentos robustos, repetitivos e de resposta de segurança completamente testados.

Embora Impedir processos de segurança de violação, como modelagem de ameaças, análises de código e testes de segurança sejam muito úteis como parte do Ciclo de Vida de Desenvolvimento de [Segurança,](https://www.microsoft.com/securityengineering/sdl/)suponha que a Violação fornece várias vantagens que ajudam a contar com a segurança geral, exercendo e medindo recursos reativos no caso de uma violação.

Na Microsoft, nos definimos para fazer isso por meio de exercícios de jogos de guerra em andamento e testes de penetração de site ao vivo de nossos planos de resposta de segurança com o objetivo de melhorar nosso recurso de detecção e resposta. A Microsoft simula regularmente violações do mundo real, realiza monitoramento contínuo de segurança e práticas de gerenciamento de incidentes de segurança para validar e melhorar a segurança do Microsoft 365, do Azure e de outros serviços de nuvem da Microsoft.

A Microsoft executa sua estratégia de segurança Assumir Violação usando dois grupos principais:

- Equipes vermelhas (invasores)
- Equipes Azuis (defensores)

Tanto o Microsoft Azure quanto a equipe do Microsoft 365 separam equipes vermelhas em tempo integral e equipes azuis.

Conhecida como "[Red Teaming](https://go.microsoft.com/fwlink/?linkid=518599)", a abordagem é testar sistemas e operações do Azure e do Microsoft 365 usando as mesmas táticas, técnicas e procedimentos como adversários reais, em relação à infraestrutura de produção ao vivo, sem o conhecimento das equipes de Engenharia ou Operações. Isso testa os recursos de detecção e resposta de segurança da Microsoft e ajuda a identificar vulnerabilidades de produção, erros de configuração, suposições inválidas e outros problemas de segurança de forma controlada. Cada violação de equipe vermelha é seguida pela divulgação completa entre ambas as equipes para identificar lacunas, resolver descobertas e melhorar a resposta a violações.

**OBSERVAÇÃO**: Nenhum dado do cliente é direcionado deliberadamente durante o Red Teaming ou teste de penetração de site ao vivo. Os testes são contra as infraestruturas e plataformas do Microsoft 365 e do Azure, bem como dos próprios locatários, aplicativos e dados da Microsoft. Os locatários, aplicativos e conteúdo do cliente hospedados no Microsoft 365 ou no Azure nunca são direcionados.

## <a name="red-teams"></a>Equipes vermelhas

A equipe vermelha é um grupo de funcionários em tempo integral da Microsoft que se concentra em violar a infraestrutura, a plataforma e os próprios locatários e aplicativos da Microsoft. Eles são o adversário dedicado (um grupo de hackers éticas) executando ataques direcionados e persistentes contra Serviços Online (infraestrutura, plataformas e aplicativos da Microsoft, mas não aplicativos ou conteúdo dos clientes finais).

A função da equipe vermelha é atacar e penetrar ambientes usando as mesmas etapas de um adversário:

![Estágios de violação](../media/office-365-isolation-breach-stages.png)

Entre outras funções, as equipes vermelhas tentam especificamente violar limites de isolamento de locatários para encontrar bugs ou lacunas em nosso design de isolamento.

## <a name="blue-teams"></a>Equipes azuis

A equipe azul é composta por um conjunto dedicado de respondentes de segurança ou membros de todas as organizações de resposta a incidentes de segurança, Engenharia e Operações. Independentemente da sua make-up, eles são independentes e operam separadamente da equipe vermelha. A equipe azul segue os processos de segurança estabelecidos e usa as ferramentas e tecnologias mais recentes para detectar e responder a ataques e penetração. Assim como os ataques do mundo real, a equipe azul não sabe quando ou como os ataques da equipe vermelha ocorrerão ou quais métodos podem ser usados. O trabalho deles, seja um ataque de equipe vermelho ou um ataque real, é detectar e responder a todos os incidentes de segurança. Por esse motivo, a equipe azul está continuamente em chamada e deve reagir a violações de equipe vermelha da mesma forma que faria para qualquer outra violação.

Quando um adversário, como uma equipe vermelha, violou um ambiente, a equipe azul deve:

- Coletar evidências deixadas pelo adversário
- Detectar a evidência como uma indicação de comprometimento
- Alertar as equipes de Engenharia e Operação apropriadas
- Triagem dos alertas para determinar se eles garantem uma investigação posterior
- Coletar contexto do ambiente para escopo da violação
- Formar um plano de correção para conter ou despejar o adversário
- Execute o plano de correção e recupere-se da violação

Estas etapas formam a resposta a incidentes de segurança que é paralela à do adversário, conforme mostrado abaixo:

![Estágios de resposta de violação](../media/office-365-isolation-breach-response-stages.png)

As violações de equipe vermelha permitem exercitar a capacidade da equipe azul de detectar e responder a ataques do mundo real de ponta a ponta. O mais importante é que ele permite a resposta a incidentes de segurança prática antes de uma violação genuína. Além disso, devido a violações de equipe vermelhas, a equipe azul aprimora sua percepção de situação, o que pode ser valioso ao lidar com futuras violações (seja da equipe vermelha ou de outro adversário). Durante todo o processo de detecção e resposta, a equipe azul produz inteligência a actionable e ganha visibilidade sobre as condições reais dos ambientes que estão tentando defender. Frequentemente, isso é realizado por meio da análise de dados e da perícia, realizadas pela equipe azul, ao responder a ataques de equipe vermelhos e estabelecer indicadores de ameaça, como indicadores de comprometimento. Assim como a equipe vermelha identifica lacunas no artigo de segurança, as equipes azuis identificam lacunas na capacidade de detectar e responder. Além disso, como o modelo vermelho de equipes ataques do mundo real, a equipe azul pode ser avaliada com precisão sobre sua capacidade ou incapacidade de lidar com adversários determinados e persistentes. Por fim, as violações de equipe vermelha medem a preparação e o impacto da resposta de violação.
