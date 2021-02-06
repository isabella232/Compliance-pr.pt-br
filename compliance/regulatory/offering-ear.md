---
title: US Export Administration Regulations (EAR)
description: Os serviços de nuvem da Microsoft ajudam os clientes sujeitos aos Regulamentos da Administração de Exportação dos EUA (EAR) a atenderem aos requisitos de conformidade e gerenciarem o risco de controle de exportação.
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
ms.openlocfilehash: fbc8166770a3ad2539264bbf76319116a2c306a9
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120000"
---
# <a name="us-export-administration-regulations-ear"></a>US Export Administration Regulations (EAR)

## <a name="about-the-ear"></a>Sobre o EAR

O Departamento de Comércio dos EUA impõe os Regulamentos de Administração de Exportação (EAR) por meio do [BIS (Bureau of Industry and Security).](https://www.bis.doc.gov/) O EAR rege amplamente e impõe controles sobre a exportação e a nova exportação da maioria dos bens comerciais, software e tecnologia, incluindo itens de "uso duplo" que podem ser usados para fins comerciais e militares e determinados itens de defesa.

A orientação do BIS contém que, quando os dados ou softwares são carregados na nuvem ou transferidos entre nós do usuário, o cliente, não o provedor de nuvem, é o "exportador" que tem a responsabilidade de garantir que as transferências, o armazenamento e o acesso a esses dados ou softwares estão em conformidade com o EAR.

De acordo com  o [BIS,](https://www.bis.doc.gov/index.php/documents/regulation-docs/412-part-734-scope-of-the-export-administration-regulations/file) *a* exportação refere-se à transferência de tecnologia protegida ou dados técnicos para um destino estrangeiro ou sua versão para uma pessoa estrangeira nos Estados Unidos (também conhecida como exportação considerada). O EAR rege amplamente:

- Exporta dos Estados Unidos.
- Exporta ou retransfere itens de origem dos EUA e determinados  itens de origem estrangeira com mais de uma parte mínima do conteúdo de origem dos EUA.
- Transferências ou divulgações para pessoas de outros países.

Itens sujeitos ao EAR podem ser encontrados na Lista de Controle de Comércio (CCL) onde cada item é atribuído a um Número de Classificação de Controle de Exportação [(ECCN) exclusivo.](https://www.bis.doc.gov/index.php/licensing/commerce-control-list-classification/export-control-classification-number-eccn) Os itens não listados no CCL são designados como EAR99 e a maioria dos produtos comerciais EAR99 não exigem uma licença para serem exportados. No entanto, dependendo do destino, do usuário final ou do uso final do item, até mesmo um item ear99 pode exigir uma licença de exportação do BIS.

A regra [final](https://www.federalregister.gov/documents/2016/06/03/2016-12734/revisions-to-definitions-in-the-export-administration-regulations), publicada em junho de 2016, esclareceu que os requisitos de licenciamento ear também não se aplicariam à transmissão e ao armazenamento de dados técnicos não classificados e software se eles foram criptografados de ponta a ponta usando módulos criptográficos validados FIPS 140-2 e não foram armazenados intencionalmente em um país com domínio estrangeiro ou na Federação Russo.

## <a name="microsoft-and-the-ear"></a>Microsoft e o EAR

Tecnologias, produtos e serviços da Microsoft estão sujeitos aos Regulamentos de Administração de Exportação dos EUA (EAR). Embora não haja certificação de conformidade para o EAR, o Microsoft Azure, o Microsoft Azure Government e o Microsoft Office 365 Government (ambientes GCCHigh e DoD) oferecem recursos e ferramentas importantes para ajudar os clientes qualificados sujeitos ao EAR a gerenciar riscos de controle de exportação e atender aos requisitos de conformidade.

O Departamento de Comércio dos EUA, que impõe o EAR, tomou a posição de que os clientes, não os provedores de serviços de nuvem como a Microsoft, são considerados exportadores de seus próprios dados de clientes. Embora a maioria dos dados do cliente não seja considerada "tecnologia" ou "dados técnicos" sujeitos aos controles de exportação de EAR, os serviços de nuvem no escopo da Microsoft são estruturados para ajudar os clientes a gerenciar e reduzir significativamente os possíveis riscos de controle de exportação que enfrentam. A Microsoft geralmente, mas não exclusivamente, recomenda o uso de seus serviços de nuvem governamentais para clientes qualificados. Com o planejamento apropriado, os clientes podem usar as ferramentas a seguir e seus próprios procedimentos internos para ajudar a garantir a conformidade total com os controles de exportação dos EUA.

- **Controles no local dos dados.** Os clientes têm visibilidade de onde seus dados estão armazenados e acesso a ferramentas robustas para restringir seu armazenamento. Portanto, eles podem garantir que seus dados estejam armazenados nos Estados Unidos e minimizar a transferência de tecnologia controlada ou dados técnicos fora dos Estados Unidos. Além disso, os dados do cliente não são armazenados em um local não em conformidade, consistentes com proibições de EAR sobre onde os dados são "armazenados intencionalmente": nenhum datacenter do Azure está localizado em nenhum dos 25 países do Grupo D:5 ou na Federação Russo.
- **Criptografia de ponta a ponta.** Ao aproveitar a segurança de criptografia de ponta a ponta para locais de armazenamento físico especificados no EAR, os serviços de nuvem no escopo da Microsoft oferecem recursos de criptografia que podem ajudar a proteger contra riscos de controle de exportação. Eles também oferecem aos clientes uma ampla variedade de opções para criptografar dados em trânsito e em repouso e [a](https://aka.ms/Azure-Encryption-Overview) flexibilidade de escolher entre as opções de criptografia.
- **Ferramentas e protocolos para impedir a exportação não autorizada considerada.** O uso de criptografia também ajuda a proteger contra uma possível exportação considerada (ou considerada uma nova exportação) sob o EAR, porque mesmo que uma pessoa que não seja dos EUA tenha acesso a dados criptografados, nada será revelado se não puder ler ou entender os dados enquanto eles estão criptografados; portanto, não há nenhuma "versão" de dados controlados.

## <a name="microsoft-in-scope-cloud-services"></a>Serviços de nuvem no Escopo da Microsoft 

- [Azure e Azure Governamental](https://aka.ms/AzureCompliance)
- [Office 365 Government (GCC-High e DoD)](https://aka.ms/Office-365-Export-Controls)
- Intune

## <a name="how-to-implement"></a>Como implementar

Visão geral dos controles de exportação dos EUA e orientações para clientes que avaliam suas obrigações no EAR.

- [Azure](https://aka.ms/Azure-Export-Controls)
- [Office 365](https://aka.ms/Office-365-Export-Controls)

## <a name="frequently-asked-questions"></a>Perguntas frequentes

**O que devo fazer para estar em conformidade com os controles de exportação ao usar os serviços de nuvem da Microsoft?**

Sob o EAR, quando os dados são carregados em um servidor de nuvem como a nuvem da Microsoft, o cliente que possui os dados — não o provedor de serviços de nuvem — é considerado o exportador. Por esse motivo, o proprietário dos dados — ou seja, o cliente microsoft — deve avaliar cuidadosamente como seu uso da nuvem da Microsoft pode implicar os controles de exportação dos EUA e determinar se qualquer um dos dados que ele deseja usar ou armazenar pode estar sujeito aos controles EAR e, em caso afirmato, quais controles se aplicam. Saiba mais sobre como os serviços de nuvem do [Azure](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=c24c11f2-2cd4-444a-9160-19762855ad3a&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers) e [do Office 365](https://query.prod.cms.rt.microsoft.com/cms/api/am/binary/RE1s5kI) podem ajudar os clientes a garantir a conformidade total com os controles de exportação dos EUA.

**As tecnologias, produtos e serviços da Microsoft estão sujeitos ao EAR?**

A maioria das tecnologias, produtos e serviços da Microsoft:

- Não estão sujeitos ao EAR e, portanto, não estão na Lista de Controle de Comércio e não têm ECCN;
- Ou são EAR99 ou 5D992 qualificados para mercado em massa para auto-classificação pela Microsoft e podem ser exportados para países sem licença como Nenhuma Licença Necessária (NLR).

Dito isso, alguns produtos da Microsoft foram atribuídos a um ECCN que pode ou não exigir uma licença. Consulte o EAR ou o jurídico para determinar o tipo de licença apropriado e os países qualificados para fins de exportação.

**Qual é a diferença entre o EAR e o ITAR (Regulamento Internacional de Tráfego de Armas)?**

Os principais controles de exportação dos EUA com o aplicativo mais amplo são o EAR, administrado pelo Departamento de Comércio dos EUA. O EAR é aplicável a itens de uso duplo que têm aplicativos comerciais e militares e a itens com aplicativos puramente comerciais.

Os Estados Unidos também têm regulamentações separadas e mais especializadas de controle de exportação, como o ITAR, que regem os itens e tecnologia mais confidenciais. Administrados pelo Departamento de Estado dos EUA, eles impõem controles sobre a exportação, importação temporária, exportação e transferência de muitos itens militares, de defesa e de inteligência (também conhecidos como "artigos de defesa"), incluindo dados técnicos relacionados.

## <a name="resources"></a>Recursos

- [Exportando produtos da Microsoft: visão geral](https://www.microsoft.com/exporting/overview.aspx)
- [Exportando produtos da Microsoft: perguntas frequentes](https://www.microsoft.com/exporting/faq.aspx)
- [Exportando produtos da Microsoft: Produto](https://www.microsoft.com/exporting/exporting-information.aspx)
- [Restrições de exportação na criptografia](/windows/uwp/security/export-restrictions-on-cryptography)
- [Microsoft e FIPS 140-2](offering-fips-140-2.md)
- [Microsoft e ITAR](offering-itar.md)
- [Conformidade na Central de Confiabilidade da Microsoft](https://www.microsoft.com/trust-center/compliance/compliance-overview)
