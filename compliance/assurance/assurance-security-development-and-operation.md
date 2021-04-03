---
title: Visão geral de desenvolvimento e operações de segurança
description: Saiba mais sobre desenvolvimento e operações de segurança no Microsoft 365
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
hideEdit: true
ms.openlocfilehash: b63c73b54cb16389d071945a8fcf849f8b1d58a9
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497453"
---
# <a name="security-development-and-operations-overview"></a>Visão geral de desenvolvimento e operações de segurança

## <a name="how-does-microsoft-implement-secure-development-practices"></a>Como a Microsoft implementa práticas de desenvolvimento seguro?

O Ciclo de Vida do Desenvolvimento de Segurança (SDL) da Microsoft é um processo de garantia de segurança focado no desenvolvimento e operação de software seguro. O SDL fornece requisitos detalhados e mensuráveis de segurança para desenvolvedores e engenheiros da Microsoft para reduzir o número e a gravidade das vulnerabilidades em nossos produtos e serviços. Todas as equipes de desenvolvimento de software da Microsoft devem seguir os requisitos do SDL e atualizamos continuamente o SDL para refletir o cenário de ameaças, as práticas recomendadas do setor e os padrões regulatórios para conformidade.

## <a name="how-does-microsofts-sdl-improve-application-security"></a>Como o SDL da Microsoft melhora a segurança do aplicativo?

O processo SDL na Microsoft pode ser pensado em termos de cinco fases de desenvolvimento: requisitos, design, implementação, verificação e versão. Ele começa definindo requisitos de software com segurança em mente. Para fazer isso, fazemos perguntas relevantes para a segurança sobre o que o aplicativo deve realizar. O aplicativo precisa coletar dados confidenciais? O aplicativo executará tarefas confidenciais ou importantes? O aplicativo precisa aceitar a entrada de fontes não confiáveis?

Depois que os requisitos de segurança relevantes foram identificados, projetamos nosso software para incorporar recursos de segurança que atendem a esses requisitos. Nossos desenvolvedores implementam requisitos de SDL e design no código, que verificamos por meio de revisão manual de código, ferramentas de segurança automatizadas e testes de penetração. Por fim, antes que o código possa ser lançado, novos recursos e alterações materiais passam pela revisão final de segurança e privacidade para garantir que todos os requisitos sejam atendidos.

## <a name="how-does-microsoft-test-source-code-for-common-vulnerabilities"></a>Como a Microsoft testa o código-fonte para vulnerabilidades comuns?

Para dar suporte aos desenvolvedores na implementação de requisitos de segurança durante o desenvolvimento de código e após a versão, a Microsoft fornece um pacote de ferramentas de desenvolvimento seguro para verificar automaticamente o código-fonte para verificar falhas e vulnerabilidades de segurança. A Microsoft define e publica uma lista de ferramentas aprovadas para nossos desenvolvedores usarem, como compiladores e ambientes de desenvolvimento, juntamente com as verificações de segurança internas executadas automaticamente em pipelines de compilação da Microsoft. Nossos desenvolvedores usam as versões mais recentes das ferramentas aprovadas para tirar proveito dos novos recursos de segurança.

Antes que o código possa ser verificado em um branch de versão, o SDL requer a revisão manual de código por um revistor separado. Os revisadores de código verificam se há erros de codificação e verificam se as alterações de código atendem aos requisitos de SDL e design, passam por testes funcionais e de segurança e executam com confiança. Eles também analisam documentação, configs e dependências associadas para garantir que as alterações de código sejam documentadas adequadamente e não causarão efeitos colaterais não intencionais. Se um revisor encontrar problemas durante a revisão de código, ele pode pedir ao enviador para reenviar o código com alterações sugeridas e testes adicionais. Os revisadores de código também podem decidir bloquear o check-in inteiramente para um código que não atender aos requisitos. Depois que o código for considerado satisfatório pelo revistor, o revistor fornece aprovação, o que é necessário para que o código possa prosseguir para a próxima fase de implantação.

Além de ferramentas de desenvolvimento seguras e revisão manual de código, a Microsoft impõe requisitos de SDL usando ferramentas de segurança automatizadas. Muitas dessas ferramentas são internas no pipeline de confirmação e analisam automaticamente o código para falhas de segurança à medida que são verificadas e conforme novas compilações são compiladas. Exemplos incluem a análise de código estático para falhas comuns de segurança e scanners de credenciais que analisam o código para segredos incorporados. Os problemas descobertos por ferramentas de segurança automatizadas devem ser corrigidos antes que novas versões possam passar na revisão de segurança e serem aprovadas para lançamento.

## <a name="how-does-microsoft-manage-open-source-software"></a>Como a Microsoft gerencia software de código aberto?

A Microsoft adotou uma estratégia de alto nível para gerenciar a segurança de código aberto, que aproveita ferramentas e fluxos de trabalho projetados para:

- Entenda quais componentes de código aberto estão sendo usados em nossos produtos e serviços.
- Acompanhe onde e como esses componentes são usados.
- Determine se esses componentes têm vulnerabilidades.
- Responda corretamente quando as vulnerabilidades são descobertas que afetam esses componentes.

As equipes de engenharia da Microsoft mantêm a responsabilidade pela segurança de todos os softwares de código aberto incluídos em um produto ou serviço. Para fazer isso em escala, a Microsoft criou recursos essenciais em sistemas de engenharia por meio de CG, o que automatiza a detecção de código aberto, fluxos de trabalho de requisitos legais e alerta para componentes vulneráveis. As ferramentas CG automatizadas digitalizem builds na Microsoft para componentes de código aberto e vulnerabilidades de segurança associadas ou obrigações legais. Os componentes descobertos são registrados e enviados às equipes apropriadas para análises de segurança e negócios. Essas análises foram projetadas para avaliar quaisquer obrigações legais ou vulnerabilidades de segurança associadas a componentes de código aberto e resolvê-los antes de aprovar componentes para implantação.

## <a name="related-external-regulations--certifications"></a>Regulamentações externas relacionadas & certificações

Os serviços online da Microsoft são regularmente auditados para conformidade com regulamentações e certificações externas. Consulte a tabela a seguir para validação de controles relacionados ao desenvolvimento e operação de segurança.

| **Auditorias externas** | **Section** | **Data do relatório mais recente** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | SA-3: Ciclo de Vida do Desenvolvimento do Sistema | 24 de setembro de 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Instrução of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.2: Alterar controles de gerenciamento <br> A.14.2: Segurança nos processos de desenvolvimento e suporte | 22 de fevereiro de 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Instrução of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.2: Alterar controles de gerenciamento <br> A.14.2: Segurança nos processos de desenvolvimento e suporte | 22 de fevereiro de 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-03: Gerenciamento de riscos <br> CA-18: Gerenciamento de alterações <br> CA-19: Alterar monitoramento <br> CA-21: Alterar teste <br> CA-38: Configurações de linha de base <br> CA-46: Revisão de segurança | 24 de dezembro de 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-03: Gerenciamento de riscos <br> CA-18: Gerenciamento de alterações <br> CA-19: Alterar monitoramento <br> CA-21: Alterar teste <br> CA-38: Configurações de linha de base <br> CA-46: Revisão de segurança | 24 de dezembro de 2020 |

## <a name="resources"></a>Recursos

- [Ciclo de vida do desenvolvimento de segurança da Microsoft](https://www.microsoft.com/securityengineering/sdl)
