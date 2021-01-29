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
ms.openlocfilehash: b14a9fa236cd71cff7dd02baf04a30c249bc4346
ms.sourcegitcommit: 2973d25e9e0185b84d281f963553a332eac1c1a3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/28/2021
ms.locfileid: "50040334"
---
# <a name="microsoft-365-security-incident-management-preparation"></a>Gerenciamento de incidentes de segurança do Microsoft 365: Preparação

## <a name="training-and-background-checks"></a>Verificações em segundo plano e treinamento

Cada funcionário que trabalha no Microsoft 365 recebe treinamento sobre incidentes de segurança e procedimentos de resposta apropriados à sua função. Todos os funcionários do Microsoft 365 recebem treinamento ao ingressar e treinamento anual de atualização todos os anos depois disso. O treinamento foi projetado para fornecer ao funcionário uma compreensão básica da abordagem da Microsoft para a segurança para que, após a conclusão do treinamento, todos os funcionários entendam:

- A definição de um incidente de segurança
- A responsabilidade de todos os funcionários de relatar incidentes de segurança
- Como escalonar um possível incidente de segurança para a equipe de Resposta de Segurança do Microsoft 365
- Como a equipe de resposta a incidentes de segurança do Microsoft 365 responde a incidentes de segurança
- Preocupações especiais em relação à privacidade, particularmente à privacidade do cliente
- Onde encontrar informações adicionais sobre segurança e privacidade e contatos de escalonamento
- Quaisquer outras áreas de segurança relevantes (conforme necessário)

Os funcionários apropriados recebem treinamento atualizado anualmente sobre segurança. O treinamento anual de atualização se concentra em:

- Quaisquer alterações feitas nos procedimentos operacionais padrão no ano anterior
- A responsabilidade de todos relatar incidentes de segurança e como fazer isso
- Onde encontrar informações adicionais sobre segurança e privacidade e contatos de escalonamento
- Quaisquer outras áreas de foco de segurança que possam ser relevantes a cada ano

Cada funcionário que trabalha no Microsoft 365 também passa por uma verificação de antecedentes apropriada e completa que inclui educação, emprego, histórico criminal e outras informações específicas do candidato de acordo com as regulamentações dos Estados Unidos, como HipAA (Health Insurance Portability and Accountability Act), INTERNATIONAL Traffic in Arms Regulations (ITAR), Federal Risk and Authorization Management Program (FedRAMP) e outros.

As verificações em segundo plano são obrigatórias para todos os funcionários que trabalham na engenharia do Microsoft 365. Alguns ambientes e funções de operador do Microsoft 365 também podem exigir impressão digital completa, requisitos de cidadania, requisitos de autorização governamental e outros controles mais rigorosos. Além disso, algumas equipes de serviço e funções podem passar por um treinamento especializado de segurança, conforme necessário. Por fim, os próprios membros da equipe de segurança têm treinamento especializado e participação em conferências diretamente relacionados à segurança. Esse treinamento varia de acordo com a necessidade da equipe e do funcionário, mas inclui coisas como conferências do setor, conferências internas de Segurança da Microsoft e cursos de treinamento externos por meio de fornecedores de treinamento de segurança conhecidos no setor. Também temos artigos dedicados de treinamento de segurança publicados ao longo do ano para a comunidade de segurança na Microsoft e especializados no Microsoft 365 regularmente.

## <a name="penetration-testing--assessment"></a>Teste de penetração & avaliação

A Microsoft trabalha com vários corpos do setor e especialistas em segurança para entender novas ameaças e tendências em evolução. A Microsoft avalia continuamente seus próprios sistemas em busca de vulnerabilidades e contratos com vários especialistas externos independentes que fazem o mesmo.

Os testes realizados para a segurança do serviço no Microsoft 365 podem ser agrupados em quatro categorias gerais:

1. **Teste de segurança automatizado:** A equipe interna e externa regularmente verificará o ambiente do Microsoft 365 com base nas práticas SDL da Microsoft, OWASP (Open Web Application Security Project) os 10 principais riscos e ameaças emergentes relatadas por diferentes corpos do setor.
2. **Avaliações de vulnerabilidade:** Os compromissos formais com testadores independentes de terceiros validam regularmente se os principais controles lógicos estão operando efetivamente para cumprir as obrigações de serviço de vários órgãos reguladores. As avaliações são realizadas pelo Conselho de Testadores de Segurança Ética Registrados (CREST) certificados e se baseiam nos 10 principais riscos OWASP e em outras ameaças aplicáveis ao serviço. Todas as ameaças encontradas são controladas para fechamento.
3. **Teste contínuo de vulnerabilidade do sistema:** A Microsoft realiza testes regulares nos quais as equipes tentam violar o sistema usando ameaças emergentes, ameaças mescladas e/ou ameaças persistentes avançadas, enquanto outras equipes tentam bloquear essas tentativas de violação.
4. **Programa de Vulnerabilidade** do Microsoft Online Services : este programa opera uma política para permitir avaliações de vulnerabilidade limitadas, originadas pelo cliente no Microsoft 365. Para obter mais informações, consulte [Termos de Bug do Microsoft Online Services .](https://www.microsoft.com/msrc/bounty-terms)

A equipe de engenharia do Microsoft 365 publica periodicamente vários documentos de conformidade. Vários desses documentos estão disponíveis sob um contrato de confidencialidade do Portal de Confiança do Serviço na Nuvem da [Microsoft](https://aka.ms/STP) ou na área de Garantia de Serviço do centro de conformidade do [Microsoft 365](https://compliance.office.com)

>[!NOTE]
>Confira o Portal de Confiança do Serviço para assinaturas do Office 365 para empresas, Azure e Dynamics CRM Online para obter detalhes sobre como acessar o Portal de Confiança do Serviço. Uma assinatura do Microsoft 365 é necessária para acessar o centro de conformidade do Microsoft 365.

## <a name="attack-simulation"></a>Simulação de ataque

A Microsoft se envolve em exercícios contínuos de simulação de ataques e testes de penetração no site ao vivo de nossos planos de segurança e resposta com a intenção de melhorar a capacidade de detecção e resposta. A Microsoft simula regularmente violações do mundo real, realiza monitoramento contínuo de segurança e práticas de resposta a incidentes de segurança para validar e melhorar a segurança do Microsoft 365 e do Azure.

A Microsoft executa uma estratégia de segurança de violação usando duas equipes principais:

### <a name="red-teams"></a>Equipes vermelhas

A Equipe Vermelha de Segurança do Microsoft 365 é um grupo de funcionários em tempo integral da Microsoft que se concentra na violação da infraestrutura, da plataforma e dos próprios locatários e aplicativos da Microsoft. Eles são os adversários dedicados (um grupo de hackers éticos) que executam ataques direcionados e persistentes contra serviços online (mas não aplicativos ou dados do cliente). Eles fornecem validação contínua de "espectro completo" (por exemplo, controles técnicos, política de papel, resposta humana, etc.) dos recursos de resposta a incidentes de serviço.

### <a name="blue-teams"></a>Equipes azuis

A Equipe Azul de Segurança do Microsoft 365 é composta por um conjunto dedicado de respondentes de segurança e membros de todas as equipes de resposta a incidentes de segurança, engenharia e operações. Eles são independentes e operam separadamente da Equipe Vermelha. A Equipe Azul segue os processos de segurança estabelecidos e usa as ferramentas e tecnologias mais recentes para detectar e responder a ataques e tentativas de penetração. Assim como os ataques do mundo real, a equipe azul não sabe quando ou como os ataques da equipe vermelha ocorrerão ou quais métodos podem ser usados. O trabalho deles, seja um ataque da Equipe Vermelha ou um verdadeiro ataque, é detectar e responder a todos os incidentes de segurança. Por esse motivo, a equipe azul está continuamente em chamada e deve reagir às violações da equipe vermelha da mesma maneira que faria para qualquer outro adversário.

As equipes da Microsoft separam equipes vermelhas em tempo integral e equipes azuis na Microsoft em várias divisões que realizam operações em todos os serviços e dentro delas. Conhecida como Equipe *Vermelha,* a abordagem é testar os sistemas e operações dos serviços Microsoft usando as mesmas táticas, técnicas e procedimentos como adversários reais, em relação à infraestrutura de produção ao vivo, sem o conhecimento da infraestrutura e da engenharia de plataforma ou das equipes de operações. Isso testa os recursos de detecção e resposta de segurança e ajuda a identificar vulnerabilidades de produção, erros de configuração, suposições inválidas ou outros problemas de segurança de maneira controlada. Cada violação da Equipe Vermelha é seguida por divulgação total entre a equipe vermelha e a equipe azul, incluindo as equipes de serviço, para identificar lacunas, resolver descobertas e melhorar significativamente a resposta a violações.

>[!NOTE]
>Nenhum dado do cliente é direcionado durante o Teaming Vermelho ou exercícios de penetração do site ao vivo. Os testes são contra a infraestrutura e as plataformas do Microsoft 365 e do Azure, bem como os próprios locatários, aplicativos e dados da Microsoft. Os locatários, aplicativos e dados do cliente hospedados no Microsoft 365 ou no Azure nunca são direcionados de acordo com as regras de envolvimento.

### <a name="joint-exercises"></a>Exercícios em conjunto

Às vezes, as equipes de segurança azul e vermelha do Microsoft 365 realizarão operações conjuntas em que o relacionamento durante a operação é mais parceiro do que adversário com um conjunto seleto de funcionários de cada equipe. Esses exercícios são bem coordenados entre as equipes para impulsionar um conjunto mais direcionado de resultados por meio da colaboração em tempo real entre hackers éticos e respondentes. Esses exercícios "equipe roxo" são altamente adaptados para cada operação maximizar a oportunidade, mas fundamental para cada operação é o compartilhamento de informações de largura de banda alta e parceria para atingir os objetivos.

## <a name="related-articles"></a>Artigos relacionados

- [Gerenciamento de incidentes do Centro de segurança do Microsoft 365](assurance-security-incident-management.md)
- [Análise e detecção de gerenciamento de incidentes de segurança do Microsoft 365](assurance-sim-detection-analysis.md)
- [Contenção, eliminação e recuperação do gerenciamento de incidentes de segurança do Microsoft 365](assurance-sim-containment-eradication-recovery.md)
- [Atividade pós-incidente de gerenciamento de incidentes de segurança do Microsoft 365](assurance-sim-post-incident-activity.md)
