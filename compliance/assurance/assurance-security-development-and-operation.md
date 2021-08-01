---
title: Visão geral de desenvolvimento e operações de segurança
description: Saiba mais sobre o desenvolvimento e operações de segurança no Microsoft 365
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
- MS-Compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 3e2b1e62e0d614c503c978dff98d6952ff7de20d
ms.sourcegitcommit: 0ffa79db0bbb35258496c7702285ed9d473b4ad9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/31/2021
ms.locfileid: "53678216"
---
# <a name="security-development-and-operations-overview"></a>Visão geral de desenvolvimento e operações de segurança

## <a name="how-does-microsoft-implement-secure-development-practices"></a>Como a Microsoft implementa práticas de desenvolvimento seguro?

O SDL (Security Development Lifecycle) da Microsoft é um processo de garantia de segurança focado no desenvolvimento e operação de software seguro. O SDL fornece requisitos de segurança detalhados e mensuráveis para desenvolvedores e engenheiros da Microsoft reduzirem o número e a gravidade das vulnerabilidades em nossos produtos e serviços. Todas as equipes de desenvolvimento de software da Microsoft devem seguir os requisitos do SDL e atualizamos continuamente o SDL para refletir o cenário de ameaças, as práticas recomendadas do setor e os padrões regulatórios para conformidade.

## <a name="how-does-microsofts-sdl-improve-application-security"></a>Como o SDL da Microsoft melhora a segurança do aplicativo?

O processo SDL na Microsoft pode ser pensado em termos de cinco fases de desenvolvimento: requisitos, design, implementação, verificação e versão. Ele começa definindo requisitos de software com a segurança em mente. Para cumprir essa meta, fazemos perguntas relevantes para a segurança sobre o que o aplicativo deve realizar. O aplicativo precisa coletar dados confidenciais? O aplicativo executará tarefas confidenciais ou importantes? O aplicativo precisa aceitar a entrada de fontes não confiáveis?

Depois que os requisitos de segurança relevantes forem identificados, projetamos nosso software para incorporar recursos de segurança que atendam a esses requisitos. Nossos desenvolvedores implementam requisitos de SDL e design no código, que verificamos por meio de revisão manual de código, ferramentas de segurança automatizadas e testes de penetração. Por fim, antes que o código possa ser lançado, novos recursos e alterações materiais passam pela revisão final de segurança e privacidade para garantir que todos os requisitos sejam atendidos.

## <a name="how-does-microsoft-test-source-code-for-common-vulnerabilities"></a>Como a Microsoft testa o código-fonte para vulnerabilidades comuns?

Para dar suporte aos nossos desenvolvedores na implementação de requisitos de segurança durante o desenvolvimento de código e após o lançamento, a Microsoft fornece um pacote de ferramentas de desenvolvimento seguro para verificar automaticamente o código-fonte em caso de falhas e vulnerabilidades de segurança. A Microsoft define e publica uma lista de ferramentas aprovadas para nossos desenvolvedores usarem, como compiladores e ambientes de desenvolvimento, juntamente com as verificações de segurança internas executadas automaticamente em pipelines de compilação da Microsoft. Nossos desenvolvedores usam as versões mais recentes das ferramentas aprovadas para aproveitar os novos recursos de segurança.

Antes que o código possa ser verificado em um branch de versão, o SDL requer a revisão manual de código por um revistor separado. Os revisores de código verificam se há erros de codificação e se as alterações no código atendem aos requisitos de SDL e de design, passam nos testes funcionais e de segurança e têm um desempenho confiável. Eles também analisam a documentação, configurações e dependências associadas para garantir que as alterações no código sejam documentadas de forma adequada e não causem efeitos colaterais indesejados. Se um revisor encontrar problemas durante a revisão do código, ele pode pedir ao remetente para reenviar o código com as alterações sugeridas e testes adicionais. Os revisores de código também podem decidir bloquear totalmente o check-in de código que não atenda aos requisitos. Depois que o código for considerado satisfatório pelo revistor, o revistor fornece aprovação, o que é necessário para que o código possa prosseguir para a próxima fase de implantação.

Além de ferramentas de desenvolvimento seguras e revisão manual de código, a Microsoft impõe requisitos de SDL usando ferramentas de segurança automatizadas. Muitas dessas ferramentas são internas no pipeline de confirmação e analisam automaticamente o código para falhas de segurança à medida que são verificadas e conforme novas compilações são compiladas. Exemplos incluem a análise de código estático para falhas comuns de segurança e scanners de credenciais que analisam o código para segredos incorporados. Os problemas descobertos por ferramentas de segurança automatizadas devem ser corrigidos antes que novas versões possam passar na revisão de segurança e serem aprovadas para lançamento.

## <a name="how-does-microsoft-manage-open-source-software"></a>Como a Microsoft gerencia software de código aberto?

A Microsoft adotou uma estratégia de alto nível para gerenciar a segurança de código aberto, que usa ferramentas e fluxos de trabalho projetados para:

- Entender quais componentes de software livre estão sendo usados em nossos produtos e serviços.
- Acompanhar onde e como esses componentes são usados.
- Determinar se esses componentes têm vulnerabilidades.
- Responder corretamente quando forem descobertas vulnerabilidades que afetam esses componentes.

As equipes de engenharia da Microsoft mantêm a responsabilidade pela segurança de todos os softwares livres incluídos em um produto ou serviço. Para atingir essa segurança em escala, a Microsoft criou recursos essenciais em sistemas de engenharia por meio do CG, o que automatiza a detecção de código aberto, fluxos de trabalho de requisitos legais e alerta para componentes vulneráveis. As ferramentas CG automatizadas digitalizem builds na Microsoft para componentes de código aberto e vulnerabilidades de segurança associadas ou obrigações legais. Os componentes descobertos são registrados e enviados para as equipes apropriadas para revisões de negócios e segurança. Essas revisões foram projetadas para avaliar quaisquer obrigações legais ou vulnerabilidades de segurança associadas a componentes de software livre e resolvê-las antes de aprovar componentes para implantação.

## <a name="related-external-regulations--certifications"></a>Regulamentações externas relacionadas & certificações

Os serviços online da Microsoft são regularmente auditados para conformidade com regulamentações e certificações externas. Consulte a tabela a seguir para validação de controles relacionados ao desenvolvimento e operação de segurança.

### <a name="azure-and-dynamics-365"></a>Azure e Dynamics 365

| **Auditorias externas** | **Section** | **Data do relatório mais recente** |
|:--------------------|:------------|:-----------------------|
| [ISO 27001/27002](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Instrução of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7af5304-3a31-40e6-9abb-e26352305d41&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.2: Alterar controles de gerenciamento <br> A.14.2: Segurança nos processos de desenvolvimento e suporte | 2 de dezembro de 2020 |
| [ISO 27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Instrução of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a3bca0ac-867d-4204-b66b-13665f5f1e8d&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=25718a8a-f34d-41e1-a95a-c49246508787&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.2: Alterar controles de gerenciamento <br> A.14.2: Segurança nos processos de desenvolvimento e suporte | 2 de dezembro de 2020 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b8721ebd-af20-42fe-b22f-8332b0a19517&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=234a0f57-83c1-4afc-a586-a0e7a59592f7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=75c8cbf6-e456-473c-a05e-34fea888ec2a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | SDL-1: metodologia SDL (Ciclo de Vida do Desenvolvimento de Segurança) <br> SDL-2: Requisitos de controle de segurança documentados em versões <br> SDL-4: Segregação de ambientes de teste e produção <br> SDL-6: Verificações de malware em builds de código-fonte <br> SDL7: revisão SDL semesanuais | 31 de março de 2021 |

### <a name="office-365"></a>Office 365

| **Auditorias externas** | **Section** | **Data do relatório mais recente** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP](https://compliance.microsoft.com/compliancemanager) | SA-3: Ciclo de Vida do Desenvolvimento do Sistema | 24 de setembro de 2020 |
| [ISO 27001/27002/27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Instrução of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.2: Alterar controles de gerenciamento <br> A.14.2: Segurança nos processos de desenvolvimento e suporte | Abril de 20, 2021 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-03: Gerenciamento de riscos <br> CA-18: Gerenciamento de alterações <br> CA-19: Alterar monitoramento <br> CA-21: Alterar teste <br> CA-38: Configurações de linha de base <br> CA-46: Revisão de segurança | 24 de dezembro de 2020 |

## <a name="resources"></a>Recursos

- [Ciclo de vida do desenvolvimento de segurança da Microsoft](https://www.microsoft.com/securityengineering/sdl)
