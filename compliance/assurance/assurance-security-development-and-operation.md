---
title: Visão geral de operações e desenvolvimento de segurança
description: Saiba mais sobre o desenvolvimento e as operações de segurança no Microsoft 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 916303ff2a65777785c89c6ccae70bea9a0bfda9
ms.sourcegitcommit: 7a5b6bc58fc4613b38f3fda20aebee5cec6a5730
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "49787300"
---
# <a name="security-development-and-operations-overview"></a>Visão geral de operações e desenvolvimento de segurança

## <a name="how-does-microsoft-implement-secure-development-practices"></a>Como a Microsoft implementa as práticas de desenvolvimento seguro?

O SDL (Ciclo de Vida de Desenvolvimento de Segurança) da Microsoft é um processo de garantia de segurança focado no desenvolvimento e operação de softwares seguros. O SDL fornece requisitos de segurança detalhados e mensuráveis para desenvolvedores e engenheiros da Microsoft reduzirem o número e a gravidade das vulnerabilidades em nossos produtos e serviços. Todas as equipes de desenvolvimento de software da Microsoft devem seguir os requisitos de SDL e atualizamos continuamente o SDL para refletir o panorama das ameaças em constante mudança, as práticas recomendadas do setor e os padrões regulatórios de conformidade.

## <a name="how-does-microsofts-sdl-improve-application-security"></a>Como o SDL da Microsoft melhora a segurança do aplicativo?

O processo SDL na Microsoft pode ser pensado em termos de cinco fases de desenvolvimento: requisitos, design, implementação, verificação e lançamento. Ele começa definindo requisitos de software com segurança em mente. Para fazer isso, fazemos perguntas relevantes à segurança sobre o que o aplicativo deve realizar. O aplicativo precisa coletar dados confidenciais? O aplicativo executará tarefas confidenciais ou importantes? O aplicativo precisa aceitar a entrada de fontes não confiáveis?

Depois que requisitos de segurança relevantes foram identificados, projetamos nosso software para incorporar recursos de segurança que atendem a esses requisitos. Nossos desenvolvedores implementam requisitos de SDL e design no código, que verificamos por meio de revisão manual de código, ferramentas de segurança automatizadas e testes de penetração. Por fim, antes que o código possa ser lançado, novos recursos e alterações materiais passam pela revisão final de segurança e privacidade para garantir que todos os requisitos sejam atendidos.

## <a name="how-does-microsoft-test-source-code-for-common-vulnerabilities"></a>Como a Microsoft testa o código-fonte para vulnerabilidades comuns?

Para dar suporte aos desenvolvedores na implementação de requisitos de segurança durante o desenvolvimento de código e após o lançamento, a Microsoft fornece um pacote de ferramentas de desenvolvimento seguro para verificar automaticamente o código-fonte em busca de falhas e vulnerabilidades de segurança. A Microsoft define e publica uma lista de ferramentas aprovadas para nossos desenvolvedores usarem, como compiladores e ambientes de desenvolvimento, juntamente com as verificações de segurança internas executadas automaticamente nos pipelines de compilação da Microsoft. Nossos desenvolvedores usam as versões mais recentes das ferramentas aprovadas para aproveitar os novos recursos de segurança.

Antes que o código possa ser verificado em uma ramificação de lançamento, o SDL requer a revisão manual de código por um revistor separado. Os revisadores de código verificam se há erros de codificação e verificam se as alterações de código atendem aos requisitos de SDL e design, passam em testes funcionais e de segurança e executam de forma confiável. Eles também revisam a documentação, as configurações e as dependências associadas para garantir que as alterações de código sejam documentadas adequadamente e não causem efeitos colaterais não intencionais. Se um revisor encontrar problemas durante a revisão do código, ele poderá pedir ao enviador para reenviar o código com alterações sugeridas e testes adicionais. Os revisadores de código também podem optar por bloquear totalmente o check-in para códigos que não atendem aos requisitos. Depois que o código for considerado satisfatório pelo revistor, o revisdor fornece aprovação, o que é necessário para que o código possa prosseguir para a próxima fase de implantação.

Além das ferramentas de desenvolvimento seguro e da revisão manual de código, a Microsoft impõe os requisitos de SDL usando ferramentas de segurança automatizadas. Muitas dessas ferramentas são compiladas no pipeline de confirmação e analisam automaticamente o código em busca de falhas de segurança durante o check-in e à medida que novas compilações são compiladas. Exemplos incluem análise de código estático para falhas comuns de segurança e scanners de credenciais que analisam o código para segredos incorporados. Os problemas descobertos pelas ferramentas de segurança automatizadas devem ser corrigidos antes que os novos builds possam passar pela revisão de segurança e serem aprovados para versão.

## <a name="how-does-microsoft-manage-open-source-software"></a>Como a Microsoft gerencia software de software de software livre?

A Microsoft adotou uma estratégia de alto nível para gerenciar a segurança de código aberto, que utiliza ferramentas e fluxos de trabalho projetados para:

- Entenda quais componentes de código aberto estão sendo usados em nossos produtos e serviços.
- Rastreia onde e como esses componentes são usados.
- Determine se esses componentes têm alguma vulnerabilidade.
- Responda corretamente quando são descobertas vulnerabilidades que afetam esses componentes.

As equipes de engenharia da Microsoft mantêm a responsabilidade pela segurança de todos os softwares de software livre incluídos em um produto ou serviço. Para conseguir isso em escala, a Microsoft criou recursos essenciais em sistemas de engenharia por meio do CG, que automatiza a detecção de software livre, fluxos de trabalho de requisitos legais e alertas para componentes vulneráveis. As ferramentas de CG automatizadas verificarão builds na Microsoft em busca de componentes de código aberto e vulnerabilidades de segurança associadas ou obrigações legais. Os componentes descobertos são registrados e enviados às equipes apropriadas para avaliações comerciais e de segurança. Essas análises foram projetadas para avaliar quaisquer obrigações legais ou vulnerabilidades de segurança associadas a componentes de código aberto e resolvê-las antes de aprovar componentes para implantação.

## <a name="related-external-regulations--certifications"></a>Regulamentações externas relacionadas & certificações

Os serviços online da Microsoft são auditados regularmente para conformidade com regulamentações e certificações externas. Consulte a tabela a seguir para validação de controles relacionados ao desenvolvimento e operação de segurança.

| **Auditorias externas** | **Section** | **Data do relatório mais recente** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | SA-3: Ciclo de vida de desenvolvimento do sistema | 24 de setembro de 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaração de Aplicabilidade](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.2: Alterar controles de gerenciamento <br> A.14.2: Segurança em processos de desenvolvimento e suporte | 22 de fevereiro de 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaração de Aplicabilidade](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.2: Alterar controles de gerenciamento <br> A.14.2: Segurança em processos de desenvolvimento e suporte | 22 de fevereiro de 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-03: Gerenciamento de riscos <br> CA-18: Gerenciamento de alterações <br> CA-19: Alterar monitoramento <br> CA-21: Alterar testes <br> CA-38: Configurações de linha de base <br> CA-46: Revisão de segurança | 24 de dezembro de 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-03: Gerenciamento de riscos <br> CA-18: Gerenciamento de alterações <br> CA-19: Alterar monitoramento <br> CA-21: Alterar testes <br> CA-38: Configurações de linha de base <br> CA-46: Revisão de segurança | 24 de dezembro de 2020 |

## <a name="resources"></a>Recursos

- [Ciclo de vida de desenvolvimento de segurança da Microsoft](https://www.microsoft.com/securityengineering/sdl)
