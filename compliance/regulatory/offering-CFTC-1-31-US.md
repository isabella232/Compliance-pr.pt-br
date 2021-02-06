---
title: Regra 1.31(c-d) da CfTC (Comissão de Negociação de Futuros de Mercadorias) dos Estados Unidos
description: Uma empresa de avaliação independente validou que o Azure e o Office 365 podem ajudar as instituições financeiras a atender aos requisitos de retenção e armazenamento imutáveis da Regra 1.31 da CFTC.
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
ms.openlocfilehash: 474cd04d98dc91668e48d1999f4fbd91d81523ec
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2021
ms.locfileid: "50121750"
---
# <a name="commodity-futures-trading-commission-cftc-rule-131c-d-united-states"></a>Regra 1.31(c-d) da CfTC (Comissão de Negociação de Futuros de Mercadorias) dos Estados Unidos

## <a name="about-cftc-rule-13c-d"></a>Sobre a Regra CFTC 1.3(c-d)

A [CFTC (Comissão](https://www.cftc.gov/) de Negociação de Futuros de Mercadorias), uma agência federal independente dos EUA, regula os mercados de futuros e opções de mercadorias e, mais recentemente, o mercado de trocas.  
  
A Regra CFTC de longa data 1.31 define os requisitos de retenção de registros estabelecidos pela regra 17a-4(f) da SEC. Além disso, especifica que os registros eletrônicos devem ser mantidos por cinco anos e que os originais sejam mantidos "prontamente acessíveis" durante os dois primeiros anos e disponibilizados para inspeção pela Comissão ou pelo Departamento de Saúde dos EUA durante todo o período de retenção.  
  
Em 2017, a [CFTC](https://www.cftc.gov/sites/default/files/idc/groups/public/@lrfederalregister/documents/file/2017-11014a.pdf)revisou sua regra, alterando e modernizando sua regulamentação de manutenção de registros para adotar padrões baseados em princípios menos prescritivos que oferecem maior flexibilidade na forma como os registros podem ser mantidos. Essa revisão torna a regra mais neutra em termos de tecnologia, permitindo que entidades regulamentadas escolham a tecnologia mais apropriada para seus negócios, mantendo as proteções que "garantem a confiabilidade do processo de manutenção de registros". A regra revisada remove o requisito de que as organizações mantenham os registros originais por dois anos, mas mantém o período de manutenção de cinco anos, o que harmoniza as práticas para empresas regulamentadas pela CFTC e pela SEC.

## <a name="microsoft-and-cftc-rule-131c-d"></a>Regra 1.31(c-d) da Microsoft e da CFTC

Os clientes de serviços financeiros, que representam um dos setores mais regulamentados do mundo, estão sujeitos a provisões complexas, como a retenção de transações financeiras e comunicação relacionada em um estado não a ser apagado e não modificável. Uma das mais prescritivas é a Regra 1.31 da CFTC (Comissão de Negociação de Futuros de Mercadorias dos EUA) que estipula requisitos rigorosos para entidades regulamentadas que optam por reter livros e registros em mídia de armazenamento eletrônico. Os registros armazenados devem ser contra adulterações sem a capacidade de alterá-los ou excluí-los até o período de retenção designado. O Armazenamento Imutável de Blob do Microsoft Azure com Bloqueio de Política e o Microsoft Office 365 com Bloqueio de Preservação podem ajudar as instituições financeiras a atender aos requisitos de armazenamento da Regra 1.31(c-d) da CFTC.

### <a name="microsoft-azure"></a>Microsoft Azure

Para avaliar a conformidade do Azure com a Regra 1.31(c-d) da CFTC, a Microsoft reservou uma empresa de avaliação independente especializada em gerenciamento de registros e governança de informações, a Cohasset Associates. No relatório resultante, a [CFTC 1.31 (c)–(d)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=19b08fd4-d276-43e8-9461-715981d0ea20&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_GRC_Assessment_Reports)Avaliação de Conformidade: Armazenamento do Microsoft Azure , Cohasset validou que o Armazenamento de [Blob Imutável do Azure](/azure/storage/blobs/storage-blob-immutable-storage) com a opção Bloqueio de Política, quando usado para reter Blobs baseados em tempo em um formato não-aprivável e não reesritável (WORM), atende aos requisitos baseados em princípios da regra CFTC. Cada Blob (registro) está protegido contra modificação, sobrescrita ou exclusão até que o período de retenção necessário tenha expirado e todas as retenções legais associadas tenham sido lançadas. Provedores de software e parceiros com cargas de trabalho confidenciais agora podem contar com o Armazenamento de Blob Imutável do Azure como uma solução de nuvem de compra única para retenção de registros. As instituições financeiras agora podem criar seus próprios aplicativos aproveitando esses recursos enquanto permanecem em conformidade.

### <a name="microsoft-365"></a>Microsoft 365

Para os requisitos da [CFTC 1.31(c)-(d),](/microsoft-365/compliance/retention-regulatory-requirements#sec-17a-4f-finra-4511c-and-cftc-131c-d) a Cohasset validou que o Microsoft 365 inclui recursos de arquivamento que permitem que clientes regulamentados, incluindo agentes, armazenem dados de maneira que os ajude a cumprir os requisitos da SEC para retenção de registros. Os recursos de retenção no Microsoft 365 ajudam a preservar uma ampla variedade de dados, incluindo email, caixa postal, documentos compartilhados, mensagens instantâneas e dados de terceiros. Em particular, o arquivamento no Microsoft 365 permite que os clientes de definidas políticas de retenção de mensagens globais ou granulares armazenem dados por um período definido e além em um formato não reescrito e não-apagado.

## <a name="microsoft-in-scope-cloud-services"></a>Serviços de nuvem no Escopo da Microsoft 

- [Azure](https://aka.ms/AzureCompliance)
- [Office 365](https://aka.ms/o365-compliance-framework)

## <a name="audits-reports-and-certificates"></a>Auditorias, relatórios e certificados

[Azure & CFTC Rule 1.31: SEC 17a-4(f) & CFTC 1.31(c-d) Compliance Assessment of Azure Storage

[Office 365 & CFTC Regra 1.31: Arquivamento no Office 365, retenção de dados e conformidade com a Regra 17a-4 da SEC

## <a name="how-to-implement"></a>Como implementar

- [Regulamentação de serviços financeiros:](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=5b483567-00b0-4d86-96ae-ee887dadb61c&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_Compliance_Guides)mapa de conformidade dos principais princípios regulatórios dos EUA para computação em nuvem e serviços online da Microsoft.
- [Guia de conformidade e avaliação de risco](https://aka.ms/RiskGovernanceGuide): cria um modelo de governança para a avaliação de risco dos serviços de nuvem da Microsoft e notificações do regulador.
- [Casos de uso financeiro](/azure/industry/financial/): Visões gerais de uso, tutoriais e outros recursos para criar soluções Azure para serviços financeiros.

## <a name="resources"></a>Recursos

- [Programa de Conformidade para Serviços Financeiros da Microsoft](https://aka.ms/FSCP-Print)
- [ serviços corporativos de nuvem e serviços financeiros da Microsoft ](https://www.microsoft.com/trustcenter/cloudservices/financialservices)
- [conformidade dos serviços financeiros no Azure](https://azure.microsoft.com/resources/videos/azurecon-2015-financial-services-compliance-in-azure/)
- [Políticas de retenção do Microsoft Office 365](/office365/securitycompliance/retention-policies)
- [Blog dos Serviços Financeiros da Microsoft](https://techcommunity.microsoft.com/t5/Financial-Services-Blog/bg-p/FinancialServicesBlog)
- [Conformidade na Central de Confiabilidade da Microsoft](https://www.microsoft.com/trust-center/compliance/compliance-overview)
