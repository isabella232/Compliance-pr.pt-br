---
title: Publicação 140-2 do FIPS (Federal Information Processing Standard)
description: A Microsoft certifica que seus módulos criptográficos estão em conformidade com o Padrão de Processamento de Informações Federais dos EUA.
keywords: Microsoft 365, conformidade, ofertas
localization_priority: None
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
ms.openlocfilehash: d7d1f47d7f76f9fc6d3cefa6cac5be807af98cbc
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120830"
---
# <a name="federal-information-processing-standard-fips-publication-140-2"></a>Publicação 140-2 do FIPS (Federal Information Processing Standard)

## <a name="fips-140-2-standard-overview"></a>Visão geral do padrão FIPS 140-2

A Publicação 140-2 do FiPS (Federal Information Processing Standard) é um padrão do governo dos EUA que define requisitos mínimos de segurança para módulos criptográficos em produtos de tecnologia da informação, conforme definido na Seção 5131 da Reforma do Gerenciamento de Tecnologia da Informação de 1996.

O [](https://csrc.nist.gov/Projects/cryptographic-module-validation-program) Programa de Validação de Módulo Criptográfico (CMVP), um esforço conjunto do Instituto Nacional de Padrões e Tecnologia (NIST) dos EUA e do Centro Canadense de Segurança Cibernética (CCCS), valida módulos criptográficos para os Requisitos de Segurança para *Módulos Criptográficos* padrão (ou seja, FIPS 140-2) e padrões de criptografia FIPS relacionados. Os requisitos de segurança FIPS 140-2 abrangem 11 áreas relacionadas ao design e à implementação de um módulo criptográfico. O Laboratório de Tecnologia da Informação NIST opera um programa relacionado que valida os algoritmos criptográficos aprovados pelo FIPS no módulo.

## <a name="microsofts-approach-to-fips-140-2-validation"></a>Abordagem da Microsoft para validação FIPS 140-2

A Microsoft mantém um compromisso ativo para atender aos requisitos 140-2, tendo módulos criptográficos validados desde a criação do padrão em 2001. A Microsoft valida seus módulos criptográficos no Programa de [](https://csrc.nist.gov/Projects/cryptographic-module-validation-program) Validação de Módulo Criptográfico (CMVP) do Instituto Nacional de Padrões e Tecnologia (NIST). Vários produtos da Microsoft, incluindo muitos serviços de nuvem, usam esses módulos criptográficos.

Para obter informações técnicas sobre módulos criptográficos do Microsoft Windows, a política de segurança para cada módulo e o catálogo de detalhes do certificado CMVP, consulte o conteúdo do Windows e do [Windows Server FIPS 140-2.](https://aka.ms/AA6ehud)

## <a name="microsoft-in-scope-cloud-services"></a>Serviços de nuvem no Escopo da Microsoft 

Embora a orientação atual de implementação FIPS 140-2 do CMVP preclua uma validação FIPS 140-2 para um serviço de nuvem em si; os provedores de serviços de nuvem podem optar por obter e operar módulos criptográficos validados fiPS 140 para os elementos de computação que compõem seu serviço de nuvem. Os serviços online da Microsoft que incluem componentes, que foram validados pelo FIPS 140-2 incluem, entre outros:

- [Azure e Azure Governamental](/azure/azure-government/documentation-government-plan-security)
- [Dynamics 365 e Dynamics 365 Government](/microsoft-365/compliance/office-365-encryption-in-microsoft-dynamics-365)
- [Office 365, Office 365 U.S. Government e Office 365 U.S. Government Defense](/microsoft-365/compliance/office-365-encryption-risks-and-protections)

## <a name="frequently-asked-questions"></a>Perguntas frequentes

**Qual é a diferença entre "FIPS 140 validado" e "compatível com FIPS 140"?**

"FIPS 140 Validated" significa que o módulo criptográfico ou um produto que incorpora o módulo foi validado ("certificado") pelo CMVP como a atender aos requisitos FIPS 140-2. "Compatível com FIPS 140" é um termo do setor para produtos de IT que dependem de produtos validados FIPS 140 para funcionalidade criptográfica.

**Quando a Microsoft realiza uma validação FIPS 140?**

A cadência para iniciar uma validação de módulo se alinha às atualizações de recursos do Windows 10 e do Windows Server. À medida que o setor de software evoluiu, os sistemas operacionais são lançados com mais frequência, com atualizações mensais de software. A Microsoft realiza a validação para versões de recursos, mas, entre as versões, busca minimizar as alterações nos módulos criptográficos.

**Quais computadores estão incluídos em uma validação FIPS 140?**

A Microsoft valida módulos criptográficos em um exemplo representativo das configurações de hardware que executam o Windows 10 e o Windows Server. É prática comum do setor aceitar essa validação FIPS 140-2 quando um ambiente usa hardware, que é semelhante aos exemplos usados para o processo de validação.

**Há muitos módulos listados no site NIST. Como saber qual delas se aplica à minha agência?**

Se for necessário usar módulos criptográficos validados por meio do FIPS 140-2, você precisará verificar se a versão usada aparece na lista de validação. O CMVP e a Microsoft mantêm uma lista de módulos criptográficos validados, organizados por lançamento de produto, juntamente com instruções para identificar quais módulos são instalados em um sistema Windows. Para obter mais informações sobre como configurar sistemas para serem compatíveis, consulte o conteúdo do [Windows e do Windows Server FIPS 140-2.](https://aka.ms/AA6ehud)

**O que significa "Quando operado no modo FIPS" em um certificado?**

Essa advertência informa ao leitor que as regras de segurança e configuração necessárias devem ser seguidas para usar o módulo criptográfico de forma consistente com sua política de segurança FIPS 140-2. Cada módulo tem sua própria política de segurança — uma especificação precisa das regras de segurança sob as quais ele funcionará — e emprega algoritmos criptográficos aprovados, gerenciamento de chaves criptográficas e técnicas de autenticação. As regras de segurança são definidas na política de segurança para cada módulo. Para obter mais informações, incluindo links para a política de segurança para cada módulo validado por meio do CMVP, consulte o conteúdo [140-2 do Windows e do Windows Server FIPS 140-2.](https://aka.ms/AA6ehud)

**O FedRAMP exige validação FIPS 140-2?**

Sim, o FedRAMP (Federal Risk and Authorization Management Program) depende de linhas de base de controle definidas pelo [NIST SP 800-53 Revisão 4,](https://nvd.nist.gov/800-53/Rev4/)incluindo a Proteção Criptográfica [SC-13](https://nvd.nist.gov/800-53/Rev4/control/SC-13) que está ificando o uso de criptografia validada por FIPS ou criptografia aprovada pela NSA.

**Como o Microsoft Azure dá suporte ao FIPS 140-2?**

O Azure foi criado com uma combinação de hardware, sistemas operacionais disponíveis comercialmente (Linux e Windows) e uma versão específica do Azure do Windows. Por meio do SDL [(Ciclo](https://www.microsoft.com/securityengineering/sdl/) de Vida de Desenvolvimento de Segurança) da Microsoft, todos os serviços do Azure usam algoritmos aprovados pelo FIPS 140-2 para segurança de dados porque o sistema operacional usa algoritmos aprovados fips 140-2 enquanto opera em uma nuvem de hiper escala.

**Posso usar a adesão da Microsoft ao FIPS 140-2 no processo de certificação da minha agência?**

Para estar em conformidade com o FIPS 140-2, seu sistema deve ser configurado para ser executado em um modo de operação aprovado pelo FIPS, o que inclui garantir que um módulo criptográfico use apenas algoritmos aprovados pelo FIPS. Para obter mais informações sobre como configurar sistemas para serem compatíveis, consulte o conteúdo do [Windows e do Windows Server FIPS 140-2.](https://aka.ms/AA6ehud)

**Qual é a relação entre FIPS 140-2 e critérios comuns?**

Esses são dois padrões de segurança separados com finalidades diferentes, mas complementares. O FIPS 140-2 foi projetado especificamente para validar módulos criptográficos de software e hardware, enquanto os Critérios Comuns foram projetados para avaliar funções de segurança em produtos de hardware e software de IT. As avaliações de Critérios comuns geralmente dependem de validações FIPS 140-2 para fornecer garantia de que a funcionalidade criptográfica básica é implementada corretamente.

## <a name="resources"></a>Recursos

- [Requisitos de segurança do FIPS Pub 140-2 para módulos criptográficos](https://csrc.nist.gov/publications/fips/fips140-2/fips1402.pdf)
- [Programa de Validação de Módulo Criptográfico NIST](https://csrc.nist.gov/groups/STM/cmvp/index.html)
- [Windows, Windows Server e FIPS 140-2](/windows/security/threat-protection/fips-140-validation)
- [Conformidade na Central de Confiabilidade da Microsoft](https://www.microsoft.com/trust-center/compliance/compliance-overview)
