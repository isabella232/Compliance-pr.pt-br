---
title: 'Gerenciamento de incidentes de segurança do Microsoft 365: Preparação'
description: Este artigo fornece uma visão geral do processo de preparação do gerenciamento de incidentes de segurança no Microsoft 365.
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
ms.openlocfilehash: b3f16620564d525245c21c375bbc9a3f5b0923b7
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497396"
---
# <a name="microsoft-365-security-incident-management-preparation"></a>Gerenciamento de incidentes de segurança do Microsoft 365: Preparação

## <a name="training-and-background-checks"></a>Verificações de treinamento e plano de fundo

Cada funcionário que trabalha no Microsoft 365 recebe treinamento sobre incidentes de segurança e procedimentos de resposta apropriados à sua função. Todos os funcionários do Microsoft 365 recebem treinamento ao ingressar e treinamento anual de atualização todos os anos depois disso. O treinamento foi projetado para fornecer ao funcionário uma compreensão básica da abordagem da Microsoft para a segurança para que, após a conclusão do treinamento, todos os funcionários entendam:

- A definição de um incidente de segurança
- A responsabilidade de todos os funcionários para relatar incidentes de segurança
- Como escalonar um possível incidente de segurança para a equipe de Resposta de Segurança do Microsoft 365
- Como a equipe de Resposta a Incidentes de Segurança do Microsoft 365 responde a incidentes de segurança
- Preocupações especiais em relação à privacidade, especialmente à privacidade do cliente
- Onde encontrar informações adicionais sobre segurança e privacidade e contatos de escalonamento
- Quaisquer outras áreas de segurança relevantes (conforme necessário)

Os funcionários apropriados recebem treinamento de atualização sobre segurança anualmente. O treinamento anual de atualização se concentra em:

- Quaisquer alterações feitas nos procedimentos operacionais padrão no ano anterior
- A responsabilidade de todos relatar incidentes de segurança e como fazer isso
- Onde encontrar informações adicionais sobre segurança e privacidade e contatos de escalonamento
- Quaisquer outras áreas de foco de segurança que possam ser relevantes a cada ano

Cada funcionário que trabalha no Microsoft 365 também passa por uma verificação de plano de fundo apropriada e completa que inclui a educação do candidato, o emprego, o histórico criminal e outras informações específicas de acordo com as regulamentações dos Estados Unidos, como HipAA (Health Insurance Portability and Accountability Act), International Traffic in Arms Regulations (ITAR), Federal Risk and Authorization Management Program (FedRAMP) e outros.

As verificações em segundo plano são obrigatórias para todos os funcionários que trabalham na engenharia do Microsoft 365. Alguns ambientes e funções de operador do Microsoft 365 também podem exigir impressão digital completa, requisitos de cidadania, requisitos de autorização governamental e outros controles mais rigorosos. Além disso, algumas equipes de serviço e funções podem passar por treinamento especializado de segurança conforme necessário. Por fim, os próprios membros da equipe de segurança têm treinamento especializado e participação em conferências relacionadas diretamente à segurança. Esse treinamento varia de acordo com a necessidade da equipe e do funcionário, mas inclui coisas como conferências do setor, conferências internas da Microsoft Security e cursos de treinamento externo por meio de fornecedores de treinamento de segurança conhecidos no setor. Também temos artigos dedicados de treinamento de segurança publicados ao longo do ano para a comunidade de segurança em toda a Microsoft e especializados no Microsoft 365 regularmente.

## <a name="penetration-testing--assessment"></a>Avaliação de testes de & de penetração

A Microsoft trabalha com vários órgãos do setor e especialistas em segurança para entender novas ameaças e tendências em evolução. A Microsoft avalia continuamente seus próprios sistemas em busca de vulnerabilidades e contratos com vários especialistas externos independentes que fazem o mesmo.

Os testes realizados para o fortalecimento do serviço no Microsoft 365 podem ser agrupados em quatro categorias gerais:

1. **Teste de segurança automatizado:** Equipes internas e externas regularmente digitalizarão o ambiente do Microsoft 365 com base em práticas do Microsoft SDL, OWASP (Projeto de Segurança de Aplicativos Da Web) Top 10 e ameaças emergentes relatadas por diferentes entidades do setor.
2. **Avaliações de vulnerabilidade:** As inações formais com testadores independentes e de terceiros regularmente validam se os principais controles lógicos estão operando efetivamente para cumprir as obrigações de serviço de vários órgãos regulatórios. As avaliações são realizadas pela equipe certificada pelo Conselho de Testadores de Segurança Ética Registrados (CREST) e se baseiam nos riscos top 10 da OWASP e em outras ameaças aplicáveis ao serviço. Todas as ameaças encontradas são controladas até o fechamento.
3. **Teste contínuo de vulnerabilidade do sistema:** A Microsoft realiza testes regulares nos quais as equipes tentam violar o sistema usando ameaças emergentes, ameaças misturadas e/ou ameaças persistentes avançadas, enquanto outras equipes tentam bloquear essas tentativas de violação.
4. **Microsoft Online Services Programa de Recompensa** por Bugs : Este programa opera uma política de permitir avaliações de vulnerabilidade limitadas, originadas pelo cliente no Microsoft 365. Para obter mais informações, [consulte Microsoft Online Services Termos de Recompensa de Bug.](https://www.microsoft.com/msrc/bounty-terms)

A equipe de engenharia do Microsoft 365 publica periodicamente vários documentos de conformidade. Vários desses documentos estão disponíveis em um contrato de não divulgação do Portal de Confiança do [Microsoft Cloud Service ou](https://aka.ms/STP) da área de Garantia de Serviço do Centro de conformidade do Microsoft [365](https://compliance.office.com)

>[!NOTE]
>Confira Começar com o Portal de Confiança de Serviço para assinaturas do Office 365 para empresas, do Azure e do Dynamics CRM Online para obter detalhes sobre como acessar o Portal de Confiança do Serviço. Uma assinatura do Microsoft 365 é necessária para acessar o centro de conformidade do Microsoft 365.

## <a name="attack-simulation"></a>Simulação de Ataque

A Microsoft se envolve em exercícios de simulação de ataque em andamento e testes de penetração no local real de nossos planos de segurança e resposta com a intenção de melhorar a capacidade de detecção e resposta. A Microsoft simula regularmente violações do mundo real, realiza monitoramento contínuo de segurança e práticas de resposta a incidentes de segurança para validar e melhorar a segurança do Microsoft 365 e do Azure.

A Microsoft executa uma estratégia de segurança de violação de supor usando duas equipes principais:

### <a name="red-teams"></a>Equipes vermelhas

A Equipe Vermelha de Segurança do Microsoft 365 é um grupo de funcionários em tempo integral da Microsoft que se concentra em violar a infraestrutura, a plataforma e os próprios locatários e aplicativos da Microsoft. Eles são o adversário dedicado (um grupo de hackers éticas) que executa ataques direcionados e persistentes contra serviços online (mas não aplicativos ou dados do cliente). Eles fornecem validação contínua de "espectro completo" (por exemplo, controles técnicos, política de papel, resposta humana, etc.) dos recursos de resposta a incidentes de serviço.

### <a name="blue-teams"></a>Equipes azuis

A Equipe Azul de Segurança do Microsoft 365 é composta por um conjunto dedicado de respondentes de segurança e membros de todas as equipes de resposta a incidentes de segurança, engenharia e operações. Eles são independentes e operam separadamente da Equipe Vermelha. A Equipe Azul segue os processos de segurança estabelecidos e usa as ferramentas e tecnologias mais recentes para detectar e responder a ataques e tentativas de penetração. Assim como os ataques do mundo real, a Equipe Azul não sabe quando ou como os ataques da Equipe Vermelha ocorrerão ou quais métodos podem ser usados. O trabalho deles, seja um ataque da Equipe Vermelha ou um ataque real, é detectar e responder a todos os incidentes de segurança. Por esse motivo, a Equipe Azul está continuamente de plantão e deve reagir às violações da Equipe Vermelha da mesma maneira que faria com qualquer outro adversário.

As equipes da Microsoft separam equipes vermelhas em tempo integral e equipes azuis na Microsoft em várias divisões que conduzem operações entre os serviços e dentro delas. Conhecida como *Red Teaming*, a abordagem é testar os sistemas e operações dos serviços Microsoft usando as mesmas táticas, técnicas e procedimentos como adversários reais, em relação à infraestrutura de produção ao vivo, sem o conhecimento da infraestrutura e da engenharia de plataforma ou das equipes de operações. Isso testa os recursos de detecção e resposta de segurança e ajuda a identificar vulnerabilidades de produção, erros de configuração, suposições inválidas ou outros problemas de segurança de forma controlada. Cada violação da Equipe Vermelha é seguida pela divulgação completa entre a Equipe Vermelha e a Equipe Azul, incluindo equipes de serviço, para identificar lacunas, resolver descobertas e melhorar significativamente a resposta a violações.

>[!NOTE]
>Nenhum dado do cliente é direcionado durante o Red Teaming ou exercícios de penetração de site ao vivo. Os testes são contra as infraestruturas e plataformas do Microsoft 365 e do Azure, bem como dos próprios locatários, aplicativos e dados da Microsoft. Os locatários, aplicativos e dados do cliente hospedados no Microsoft 365 ou no Azure nunca são direcionados de acordo com as regras de envolvimento aceitas.

### <a name="joint-exercises"></a>Exercícios conjuntos

Às vezes, as equipes de Segurança Azul e Vermelho do Microsoft 365 realizarão operações conjuntas em que o relacionamento durante a operação é mais parceiro do que adversário com um conjunto selecionado de funcionários de cada equipe. Esses exercícios são bem coordenados entre as equipes para impulsionar um conjunto mais direcionado de resultados por meio da colaboração em tempo real entre hackers e respondentes éticas. Esses exercícios de "equipe roxa" são altamente personalizados para cada operação para maximizar a oportunidade, mas fundamental para cada operação é o compartilhamento de informações de alta largura de banda e a parceria para atingir os objetivos.

## <a name="related-articles"></a>Artigos relacionados

- [Gerenciamento de incidentes do Centro de segurança do Microsoft 365](assurance-security-incident-management.md)
- [Análise e detecção de gerenciamento de incidentes de segurança do Microsoft 365](assurance-sim-detection-analysis.md)
- [Contenção, erradicação e recuperação de gerenciamento de incidentes de segurança do Microsoft 365](assurance-sim-containment-eradication-recovery.md)
- [Atividade pós-incidente de gerenciamento de incidentes de segurança do Microsoft 365](assurance-sim-post-incident-activity.md)
