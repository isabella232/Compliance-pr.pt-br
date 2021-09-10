---
title: Publicação FIPS (Federal Information Processing Standard) 140-2
description: A Microsoft certifica que seus módulos criptográficos estão em conformidade com o Us Federal Information Processing Standard.
keywords: Microsoft 365, conformidade, ofertas
ms.localizationpriority: medium
ms.prod: microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmazz
manager: laurawi
audience: itpro
ms.collection:
- M365-security-compliance
- MS-Compliance
hideEdit: true
titleSuffix: Microsoft Compliance
ms.openlocfilehash: 0e087393901b76a798c4a4ea3bef25fad8dcda84
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2021
ms.locfileid: "58947484"
---
# <a name="federal-information-processing-standard-fips-publication-140-2"></a>Publicação FIPS (Federal Information Processing Standard) 140-2

## <a name="fips-140-2-standard-overview"></a>Visão geral padrão do FIPS 140-2

A Publicação 140-2 do Fips (Federal Information Processing Standard) é um padrão governamental dos EUA que define requisitos mínimos de segurança para módulos criptográficos em produtos de tecnologia da informação, conforme definido na Seção 5131 da Lei de Reforma do Gerenciamento de Tecnologia da Informação de 1996.

O [](https://csrc.nist.gov/Projects/cryptographic-module-validation-program) Programa de Validação de Módulos Criptográficos (CMVP), um esforço conjunto do Instituto Nacional de Padrões e Tecnologia dos EUA (NIST) e do Centro Canadense de Segurança Cibernética (CCCS), valida módulos criptográficos para o padrão Requisitos de Segurança para *Módulos Criptográficos* (ou seja, FIPS 140-2) e padrões de criptografia FIPS relacionados. Os requisitos de segurança fips 140-2 abrangem 11 áreas relacionadas ao design e implementação de um módulo criptográfico. O Laboratório de Tecnologia da Informação NIST opera um programa relacionado que valida os algoritmos criptográficos aprovados pelo FIPS no módulo.

## <a name="microsofts-approach-to-fips-140-2-validation"></a>Abordagem da Microsoft para validação fips 140-2

A Microsoft mantém um compromisso ativo para atender aos requisitos 140-2, tendo validado módulos criptográficos desde a criação do padrão em 2001. A Microsoft valida seus módulos criptográficos no Programa de [](https://csrc.nist.gov/Projects/cryptographic-module-validation-program) Validação de Módulo Criptográfico (CMVP) do Instituto Nacional de Padrões e Tecnologia (NIST). Vários produtos Microsoft, incluindo muitos serviços de nuvem, usam esses módulos criptográficos.

Para obter informações técnicas sobre os módulos criptográficos do Microsoft Windows, a política de segurança para cada módulo e o catálogo de detalhes do certificado CMVP, consulte o conteúdo do Windows e [do Windows Server FIPS 140-2](https://aka.ms/AA6ehud).

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Plataformas e serviços em nuvem no escopo da Microsoft

Embora a orientação de implementação atual do CMVP FIPS 140-2 preclua uma validação FIPS 140-2 para um serviço de nuvem em si; os provedores de serviços de nuvem podem optar por obter e operar módulos criptográficos validados fips 140 para os elementos de computação que compõem seu serviço de nuvem. Os serviços online da Microsoft que incluem componentes, que foram fips 140-2 validados incluem, entre outros:

- Azure e Azure Governamental
- Dynamics 365 e Dynamics 365 Government
- Office 365, Office 365 U.S. Government e Office 365 U.S. Government Defense

## <a name="azure-dynamics-365-and-fips-140-2"></a>Azure, Dynamics 365 e FIPS 140-2

Para obter mais informações sobre a conformidade do Azure, dynamics 365 e outros serviços online, consulte a oferta [fips 140-2 do Azure.](/azure/compliance/offerings/offering-fips-140-2)

## <a name="office-365-and-fips-140-2"></a>Office 365 e FIPS 140-2

### <a name="office-365-cloud-environments"></a>Ambientes da nuvem do Office 365

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Aplicabilidade do Office 365 e serviços no escopo

Use a seguinte tabela para determinar a aplicabilidade para seus serviços e assinatura do Office 365:

| **Aplicabilidade** | **Serviços no escopo** |
|:------------------|:----------------------|
| Office 365, GCC, GCC Alta, DoD | Consulte [Validação fips 140-2](/windows/security/threat-protection/fips-140-validation) |

### <a name="frequently-asked-questions"></a>Perguntas frequentes

**Qual é a diferença entre 'FIPS 140 Validado' e 'compatível com FIPS 140'?**

'FIPS 140 Validated' significa que o módulo criptográfico ou um produto que incorpora o módulo foi validado ('certificado') pelo CMVP como a atender aos requisitos fips 140-2. 'Compatível com FIPS 140' é um termo do setor para produtos de IT que dependem de produtos FIPS 140 Validados para funcionalidade criptográfica.

**Quando a Microsoft realiza uma validação FIPS 140?**

A cadência para iniciar uma validação de módulo se alinha com as atualizações de recursos do Windows 10 e Windows Server. À medida que o setor de software evoluiu, os sistemas operacionais são lançados com mais frequência, com atualizações mensais de software. A Microsoft realiza validação para versões de recursos, mas, entre as versões, procura minimizar as alterações nos módulos criptográficos.

**Quais computadores estão incluídos em uma validação FIPS 140?**

A Microsoft valida módulos criptográficos em um exemplo representativo de configurações de hardware que executam Windows 10 e Windows Server. É prática comum do setor aceitar essa validação FIPS 140-2 quando um ambiente usa hardware, que é semelhante aos exemplos usados para o processo de validação.

**Há muitos módulos listados no site do NIST. Como saber qual delas se aplica à minha agência?**

Se for necessário usar módulos criptográficos validados por meio do FIPS 140-2, você precisará verificar se a versão usada aparece na lista de validação. O CMVP e a Microsoft mantêm uma lista de módulos criptográficos validados, organizados pela versão do produto, juntamente com instruções para identificar quais módulos são instalados em um sistema Windows. Para obter mais informações sobre como configurar sistemas em conformidade, consulte o Windows e [Windows conteúdo fips 140-2 do servidor.](https://aka.ms/AA6ehud)

**O que significa "Quando operado no modo FIPS" em um certificado?**

Essa advertência informa ao leitor que as regras de segurança e configuração necessárias devem ser seguidas para usar o módulo criptográfico de forma consistente com sua política de segurança FIPS 140-2. Cada módulo tem sua própria política de segurança — uma especificação precisa das regras de segurança sob as quais ele operará — e emprega algoritmos criptográficos aprovados, gerenciamento de chaves criptográficas e técnicas de autenticação. As regras de segurança são definidas na política de segurança para cada módulo. Para obter mais informações, incluindo links para a política de segurança para cada módulo validado por meio do CMVP, consulte o conteúdo Windows e [Windows Server FIPS 140-2](https://aka.ms/AA6ehud).

**A FedRAMP exige validação FIPS 140-2?**

Sim, o Programa Federal de Gerenciamento de Riscos e Autorizações (FedRAMP) depende das linhas de base de controle definidas pela Revisão 4 do [NIST SP 800-53](https://nvd.nist.gov/800-53/Rev4/), incluindo a [Proteção Criptográfica SC-13](https://nvd.nist.gov/800-53/Rev4/control/SC-13) que obriga o uso de criptografia validada por FIPS ou criptografia aprovada pela NSA.

**Posso usar a adesão da Microsoft ao FIPS 140-2 no processo de certificação da minha agência?**

Para estar em conformidade com o FIPS 140-2, seu sistema deve ser configurado para ser executado em um modo de operação aprovado pelo FIPS, o que inclui garantir que um módulo criptográfico use apenas algoritmos aprovados pelo FIPS. Para obter mais informações sobre como configurar sistemas em conformidade, consulte o Windows e [Windows conteúdo fips 140-2 do servidor.](https://aka.ms/AA6ehud)

**Qual é a relação entre FIPS 140-2 e Common Criteria?**

Esses são dois padrões de segurança separados com finalidades diferentes, mas complementares. O FIPS 140-2 foi projetado especificamente para validar módulos criptográficos de software e hardware, enquanto o Common Criteria foi projetado para avaliar funções de segurança em produtos de software e hardware de IT. As avaliações de Critérios Comuns geralmente dependem de validações FIPS 140-2 para garantir que a funcionalidade criptográfica básica seja implementada corretamente.

### <a name="resources"></a>Recursos

- [Requisitos de segurança do FIPS Pub 140-2 para módulos criptográficos](https://csrc.nist.gov/publications/fips/fips140-2/fips1402.pdf)
- [Programa de Validação de Módulo Criptográfico NIST](https://csrc.nist.gov/groups/STM/cmvp/index.html)
- [Windows, Windows Server e FIPS 140-2](/windows/security/threat-protection/fips-140-validation)
- [Conformidade na Central de Confiabilidade da Microsoft](https://www.microsoft.com/trust-center/compliance/compliance-overview)
