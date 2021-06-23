---
title: Us Export Administration Regulations (EAR)
description: Os serviços de nuvem da Microsoft ajudam os clientes sujeitos aos Regulamentos de Administração de Exportação dos EUA (EAR) atenderem aos seus requisitos de conformidade e gerenciar o risco de controle de exportação.
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
ms.openlocfilehash: 0c05010d43ea345024b63e2653e37eb0f42443f4
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/23/2021
ms.locfileid: "53089765"
---
# <a name="us-export-administration-regulations-ear"></a>Us Export Administration Regulations (EAR)

## <a name="about-the-ear"></a>Sobre o EAR

O Departamento de Comércio dos EUA impõe os Regulamentos de Administração de Exportação (EAR) por meio do [Bureau of Industry and Security (BIS)](https://www.bis.doc.gov/). O EAR rege amplamente e impõe controles sobre a exportação e a exportação da maioria dos produtos comerciais, software e tecnologia, incluindo itens de "uso duplo" que podem ser usados para fins comerciais e militares e determinados itens de defesa.

As diretrizes do BIS sustentam que, quando dados ou softwares são carregados na nuvem ou transferidos entre nós do usuário, o cliente, não o provedor de nuvem, é o "exportador" que tem a responsabilidade de garantir que as transferências, o armazenamento e o acesso a esses dados ou softwares estão em conformidade com o EAR.

De acordo com o [BIS](https://www.bis.doc.gov/index.php/documents/regulation-docs/412-part-734-scope-of-the-export-administration-regulations/file) *,* *a* exportação refere-se à transferência de tecnologia protegida ou dados técnicos para um destino estrangeiro ou sua versão para uma pessoa estrangeira nos Estados Unidos (também chamada de exportação considerada ). O EAR rege amplamente:

- Exporta dos Estados Unidos.
- Re-exporta ou retransfere de itens de origem dos EUA e determinados itens de origem estrangeira com mais de uma parte *de minimis* do conteúdo de origem dos EUA.
- Transferências ou divulgações para pessoas de outros países.

Os itens sujeitos ao EAR podem ser encontrados na Lista de Controle de Comércio (CCL) onde cada item recebe um [ECCN (Export Control Classification Number)](https://www.bis.doc.gov/index.php/licensing/commerce-control-list-classification/export-control-classification-number-eccn)exclusivo. Os itens não listados no CCL são designados como EAR99 e a maioria dos produtos comerciais EAR99 não exigirá que uma licença seja exportada. No entanto, dependendo do destino, do usuário final ou do uso final do item, até mesmo um item EAR99 pode exigir uma licença de exportação bis.

A regra [final](https://www.federalregister.gov/documents/2016/06/03/2016-12734/revisions-to-definitions-in-the-export-administration-regulations), publicada em junho de 2016, esclareceu que os requisitos de licenciamento ear também não se aplicariam à transmissão e ao armazenamento de dados técnicos e software não classificados se eles fossem criptografados de ponta a ponta usando módulos criptográficos validados fips 140-2 e não fossem armazenados intencionalmente em um país embargado por militares ou na Federação Russo.

## <a name="microsoft-and-the-ear"></a>Microsoft e o EAR

As tecnologias, produtos e serviços da Microsoft estão sujeitas aos Regulamentos de Administração de Exportação dos EUA (EAR). Embora não haja certificação de conformidade para os ambientes EAR, Microsoft Azure, Microsoft Azure Government e Microsoft Office 365 Government (GCCHigh e DoD) oferecem recursos e ferramentas importantes para ajudar os clientes qualificados sujeitos ao EAR a gerenciar riscos de controle de exportação e atender aos seus requisitos de conformidade.

O Departamento de Comércio dos EUA, que impõe o EAR, tomou a posição de que os clientes, não provedores de serviços de nuvem, como a Microsoft, são considerados exportadores de seus próprios dados de cliente. Embora a maioria dos dados do cliente não seja considerada "tecnologia" ou "dados técnicos" sujeitos aos controles de exportação ear, os serviços de nuvem no escopo da Microsoft são estruturados para ajudar os clientes a gerenciar e reduzir significativamente os possíveis riscos de controle de exportação que enfrentam. A Microsoft geralmente, mas não exclusivamente, recomenda o uso de seus serviços de nuvem governamental para clientes qualificados. Com o planejamento apropriado, os clientes podem usar as ferramentas a seguir e seus próprios procedimentos internos para ajudar a garantir a conformidade total com os controles de exportação dos EUA.

- **Controles no local dos dados**. Os clientes têm visibilidade de onde seus dados são armazenados e o acesso a ferramentas robustas para restringir seu armazenamento. Eles podem, portanto, garantir que seus dados estejam armazenados nos Estados Unidos e minimizar a transferência de tecnologia controlada ou dados técnicos fora dos Estados Unidos. Além disso, os dados do cliente não são armazenados em um local não em conformidade, consistente com as proibições de EAR em que os dados são "armazenados intencionalmente": nenhum datacenter do Azure está localizado em nenhum dos 25 países do Grupo D:5 ou na Federação Russa.
- **Criptografia de ponta a ponta.** Aproveitando o porto seguro de criptografia de ponta a ponta para locais de armazenamento físico especificados no EAR, os serviços de nuvem no escopo da Microsoft oferecem recursos de criptografia que podem ajudar a proteger contra riscos de controle de exportação. Eles também oferecem aos clientes uma [ampla](https://aka.ms/Azure-Encryption-Overview) variedade de opções para criptografar dados em trânsito e em repouso e a flexibilidade de escolher entre opções de criptografia.
- **Ferramentas e protocolos para impedir a exportação não autorizada considerada**. O uso da criptografia também ajuda a proteger contra uma exportação potencial considerada (ou considerada re-exportação) sob o EAR, porque mesmo que uma pessoa não-EUA tenha acesso a dados criptografados, nada será revelado se não puder ler ou entender os dados enquanto eles são criptografados; portanto, não há "versão" de dados controlados.

## <a name="microsoft-in-scope-cloud-services"></a>Serviços de nuvem no escopo da Microsoft

- [Azure e Azure Governamental](https://aka.ms/AzureCompliance)
- [Office 365 Government (GCC-High e DoD)](https://aka.ms/Office-365-Export-Controls)
- Intune

## <a name="how-to-implement"></a>Como implementar

Visão geral dos controles de exportação e diretrizes dos EUA para clientes que avaliam suas obrigações no EAR.

- [Azure](https://aka.ms/Azure-Export-Controls)
- [Office 365](https://aka.ms/Office-365-Export-Controls)

## <a name="frequently-asked-questions"></a>Perguntas frequentes

**O que devo fazer para estar em conformidade com controles de exportação ao usar serviços de nuvem da Microsoft?**

Sob o EAR, quando os dados são carregados em um servidor de nuvem, como a nuvem da Microsoft, o cliente que possui os dados — e não o provedor de serviços de nuvem — é considerado o exportador. Por esse motivo, o proprietário dos dados — ou seja, o cliente microsoft — deve avaliar cuidadosamente como o uso da nuvem da Microsoft pode implicar os controles de exportação dos EUA e determinar se qualquer um dos dados que deseja usar ou armazenar pode estar sujeito a controles EAR e, em caso afirmado, quais controles se aplicam. Saiba mais sobre como os serviços de nuvem do [Azure](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=c24c11f2-2cd4-444a-9160-19762855ad3a&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers) [e Office 365](https://query.prod.cms.rt.microsoft.com/cms/api/am/binary/RE1s5kI) podem ajudar os clientes a garantir a conformidade total com os controles de exportação dos EUA.

**As tecnologias, produtos e serviços da Microsoft estão sujeitas ao EAR?**

A maioria das tecnologias, produtos e serviços da Microsoft:

- Não estão sujeitos ao EAR e, portanto, não estão na Lista de Controle de Comércio e não têm ECCN;
- Ou eles são ear99 ou 5D992 mass Market qualificados para auto-classificação pela Microsoft e podem ser exportados para países não embargados sem uma licença como Nenhuma Licença Necessária (NLR).

Dito isso, alguns produtos da Microsoft foram atribuídos a um ECCN que pode ou não exigir uma licença. Consulte o EAR ou o conselho jurídico para determinar o tipo de licença apropriado e os países qualificados para fins de exportação.

**Qual é a diferença entre o EAR e o ITAR (International Traffic in Arms Regulations)?**

Os principais controles de exportação dos EUA com o aplicativo mais amplo são o EAR, administrado pelo Departamento de Comércio dos EUA. O EAR é aplicável a itens de uso duplo que têm aplicativos comerciais e militares e itens com aplicativos puramente comerciais.

Os Estados Unidos também têm regulamentos de controle de exportação separados e mais especializados, como o ITAR, que rege os itens e tecnologia mais confidenciais. Administrados pelo Departamento de Estado dos EUA, eles impõem controles sobre a exportação, importação temporária, re-exportação e transferência de muitos itens militares, de defesa e de inteligência (também conhecidos como "artigos de defesa"), incluindo dados técnicos relacionados.

## <a name="resources"></a>Recursos

- [Exportando produtos microsoft: visão geral](https://www.microsoft.com/exporting/overview.aspx)
- [Exportando produtos microsoft: perguntas frequentes](https://www.microsoft.com/exporting/faq.aspx)
- [Exportando produtos Microsoft: Product Lookup](https://www.microsoft.com/exporting/exporting-information.aspx)
- [Exportar restrições à criptografia](/windows/uwp/security/export-restrictions-on-cryptography)
- [Microsoft e FIPS 140-2](offering-fips-140-2.md)
- [Microsoft e ITAR](offering-itar.md)
- [Conformidade na Central de Confiabilidade da Microsoft](https://www.microsoft.com/trust-center/compliance/compliance-overview)
