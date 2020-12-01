---
title: Visão geral do desenvolvimento e operações de segurança
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
ms.openlocfilehash: 7c6752b84470eebbdb6ad78c212361156dea957b
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/30/2020
ms.locfileid: "49505723"
---
# <a name="security-development-and-operations-overview"></a>Visão geral do desenvolvimento e operações de segurança

## <a name="how-does-microsoft-implement-secure-development-practices"></a>Como a Microsoft implementa as práticas seguras de desenvolvimento?

O SDL (ciclo de vida de desenvolvimento de segurança) da Microsoft é um processo de garantia de segurança voltado ao desenvolvimento e operação de software seguro. O SDL fornece requisitos de segurança detalhados e mensuráveis para desenvolvedores e engenheiros da Microsoft para reduzir o número e a gravidade de vulnerabilidades em nossos produtos e serviços. Todas as equipes de desenvolvimento de software da Microsoft devem seguir os requisitos de SDL e atualizamos continuamente o SDL para refletir a alteração do panorama da ameaça, as práticas recomendadas do setor e os padrões normativos de conformidade.

## <a name="how-does-microsofts-sdl-improve-application-security"></a>Como o SDL da Microsoft aumenta a segurança do aplicativo?

O processo SDL da Microsoft pode ser considerado em termos de cinco fases de desenvolvimento: requisitos, design, implementação, verificação e versão. Ele começa definindo os requisitos de software com segurança em mente. Para fazer isso, pedimos perguntas relevantes sobre o que o aplicativo deve realizar. O aplicativo precisa coletar dados confidenciais? O aplicativo executará tarefas confidenciais ou importantes? O aplicativo precisa aceitar entradas de fontes não confiáveis?

Após a identificação dos requisitos de segurança relevantes, projetamos nosso software para incorporar recursos de segurança que atendam a esses requisitos. Nossos desenvolvedores implementam os requisitos de SDL e design no código, que verificamos por meio da revisão manual do código, das ferramentas de segurança automatizada e do teste de penetração. Por fim, antes que o código possa ser lançado, novos recursos e alterações de material passam pela análise final de segurança e privacidade para garantir que todos os requisitos sejam atendidos.

## <a name="how-does-microsoft-test-source-code-for-common-vulnerabilities"></a>Como a Microsoft testa o código-fonte para vulnerabilidades comuns?

Para dar suporte aos desenvolvedores na implementação dos requisitos de segurança durante o desenvolvimento de código e após o lançamento, a Microsoft fornece um pacote de ferramentas de desenvolvimento seguro para verificar automaticamente se há falhas e vulnerabilidades de segurança no código-fonte. A Microsoft define e publica uma lista de ferramentas aprovadas para nossos desenvolvedores usar, como compiladores e ambientes de desenvolvimento, junto com as verificações de segurança internas executadas automaticamente em pipelines do Microsoft Build. Nossos desenvolvedores usam as versões mais recentes das ferramentas aprovadas para aproveitar os novos recursos de segurança.

Antes que o código possa ser verificado em uma ramificação de lançamento, o SDL requer análise manual de código por um revisor separado. Os revisores de código verificam erros de codificação e verificam se as alterações de código atendem aos requisitos de desenvolvimento e SDL, passam em testes funcionais e de segurança e são executados de forma confiável. Eles também confiram a documentação associada, as configurações e as dependências para garantir que as alterações de código sejam documentadas de forma adequada e não causarão efeitos colaterais não pretendidos. Se um revisor encontrar problemas durante a revisão do código, eles podem solicitar que o remetente reenvie o código com alterações sugeridas e testes adicionais. Os revisores de código também podem decidir bloquear o check-in totalmente para o código que não atende aos requisitos. Depois que o código é considerado satisfatório pelo revisor, o revisor fornece aprovação, que é necessário antes que o código possa prosseguir para a próxima fase de implantação.

Além de ferramentas de desenvolvimento seguras e análise manual de código, a Microsoft impõe requisitos de SDL usando a ferramenta de segurança automatizada. Muitas dessas ferramentas estão incorporadas ao pipeline de confirmação e automaticamente analisam o código para falhas de segurança à medida que é feito o check-in e as novas compilações são compiladas. Exemplos incluem análise de código estático para falhas de segurança comuns e verificadores de credenciais que analisam o código para segredos incorporados. Problemas descobertos por ferramentas de segurança automatizadas devem ser corrigidos para que as novas compilações possam passar por uma revisão de segurança e ser aprovadas para lançamento.

## <a name="how-does-microsoft-manage-open-source-software"></a>Como a Microsoft gerencia o software de origem aberta?

A Microsoft adotou uma estratégia de alto nível para gerenciar a segurança de código-fonte aberto, que aproveita as ferramentas e fluxos de trabalho projetados para:

- Entenda quais componentes de origem aberta estão sendo usados em nossos produtos e serviços.
- Controlar onde e como esses componentes são usados.
- Determine se esses componentes têm alguma vulnerabilidade.
- Responder corretamente quando forem descobertas vulnerabilidades que afetam esses componentes.

As equipes de engenharia da Microsoft mantêm a responsabilidade da segurança de todos os softwares de software livre incluídos em um produto ou serviço. Para conseguir isso em escala, a Microsoft criou recursos essenciais para sistemas de engenharia por meio de CG, que automatiza a detecção de código-fonte aberta, fluxos de trabalho de requisitos legais e alertas para componentes vulneráveis. A verificação de ferramentas do CG automática na Microsoft cria componentes de código-fonte aberto e vulnerabilidades de segurança e obrigações legais associadas. Os componentes descobertos são registrados e enviados para as equipes apropriadas de negócios e revisões de segurança. Essas revisões foram projetadas para avaliar qualquer obrigação legal ou vulnerabilidades de segurança associadas a componentes de código aberto e resolvê-los antes de aprovar componentes para implantação.

## <a name="related-external-regulations--certifications"></a>Normas externas relacionadas & certificações

Os serviços online da Microsoft são auditados regularmente para fins de conformidade com regulamentos externos e certificações. Consulte a tabela a seguir para validação de controles relacionados ao desenvolvimento e operação de segurança.

| **Auditorias externas** | **Section** | **Data do relatório mais recente** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | SA-3: ciclo de vida de desenvolvimento do sistema | 24 de setembro de 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaração de aplicabilidade](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 12.1.2: alterar controles de gerenciamento <br> A. 14.2: segurança em processos de desenvolvimento e suporte | 22 de fevereiro de 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaração de aplicabilidade](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 12.1.2: alterar controles de gerenciamento <br> A. 14.2: segurança em processos de desenvolvimento e suporte | 22 de fevereiro de 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-03: gerenciamento de risco <br> AC-18: gerenciamento de alterações <br> AC-19: alterar o monitoramento <br> AC-21: alterar o teste <br> AC-38: configurações de linha de base <br> AC-46: revisão de segurança | 30 de setembro de 2019 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-03: gerenciamento de risco <br> AC-18: gerenciamento de alterações <br> AC-19: alterar o monitoramento <br> AC-21: alterar o teste <br> AC-38: configurações de linha de base <br> AC-46: revisão de segurança | 30 de setembro de 2019 |

## <a name="resources"></a>Recursos

- [Ciclo de vida de desenvolvimento de segurança da Microsoft](https://www.microsoft.com/securityengineering/sdl)
