---
title: Padrão de linha de base do Informatiebeveiliging Rijksdienst (BIR 2012)
description: Os serviços de nuvem da Microsoft ajudam as agências do setor público nos Países Baixos a cumprir com o padrão BIR 2012.
keywords: Microsoft 365, conformidade, ofertas
ms.localizationpriority: high
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
ms.openlocfilehash: d0f7bd0db5d71c91a163e05e582ad8c227a8aa22
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/12/2021
ms.locfileid: "59158159"
---
# <a name="baseline-informatiebeveiliging-rijksdienst-standard-bir-2012"></a>Padrão de linha de base do Informatiebeveiliging Rijksdienst (BIR 2012)

## <a name="bir-2012-overview"></a>Visão geral do BIR 2012

As organizações que operam no setor governamental holandês devem estar em conformidade com o padrão de linha de base Informatiebeveiliging Rijksdienst (BIR 2012). O BIR 2012 oferece uma estrutura padrão baseada na ISO 27001 e ISO 27002. Ao usar o Microsoft Azure ou o Office 365, parte dos controles do BIR 2012 para esses serviços em nuvem são gerenciados pela Microsoft seguindo o modelo de responsabilidade compartilhada na computação em nuvem. As organizações que precisam estar em conformidade com o BIR 2012 são, portanto, obrigadas a determinar se os serviços subjacentes da Microsoft que elas usam estão em conformidade com o BIR 2012.

O relatório de cobertura BIR fornece orientações onde as normas BIR são cobertas pelas certificações ISO 27001 existentes que estão disponíveis para os serviços em nuvem da Microsoft. Onde houver outros controles BIR que não estejam cobertos pela ISO 27001, serão feitas referências a outros atestados, documentação de auditoria ou declarações contratuais independentes.

## <a name="microsoft-and-bir-2012"></a>Microsoft e BIR 2012

Embora a Microsoft não esteja sujeita à conformidade com o BIR 2012, os clientes do setor governamental que desejam usar serviços de nuvem podem usar as certificações existentes da Microsoft para indicar sua conformidade com este padrão. O Azure e o Office 365 passam por várias certificações e atestados independentes periódicos, alguns deles intimamente relacionados ao BIR 2012.

[Baixe o Microsoft Cloud: Manual do Usuário Azure e Office 365 BIR-2012 para cobertura da linha de base](https://go.microsoft.com/fwlink/p/?linkid=2099461)

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Plataformas e serviços de nuvem no escopo da Microsoft

- Azure
- Intune
- Office 365

## <a name="office-365-and-bir-2012"></a>Office 365 e BIR 2012

### <a name="office-365-cloud-environments"></a>Ambientes de nuvem do Office 365

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Aplicabilidade do Office 365 e serviços no escopo

Use a seguinte tabela para determinar a aplicabilidade para seus serviços e assinatura do Office 365:

| **Aplicabilidade** | **Serviços no escopo** |
|:------------------|:----------------------|
| **Comercial** | Proteção de Informações do Azure, Bookings, Proteção do Exchange Online, Exchange Online, Kaizala, Microsoft Analytics, Microsoft Booking, Microsoft Graph, Microsoft Teams, Microsoft To Do para Web, MyAnalytics, Office 365 Cloud App Security, Grupos do Office 365, Vídeo do Office 365, Office Delve, OneDrive for Business, Planner, Power Apps, Power Automate, Power BI para Office 365, PowerApps, SharePoint Online, Skype for Business, StaffHub, Stream, Sway, Yammer Enterprise |

## <a name="audits-reports-and-certificates"></a>Auditorias, relatórios e certificados

A Microsoft selecionou uma empresa de auditoria terceirizada e independente para analisar até que ponto as certificações e atestados atuais do Azure e do Office 365 (como ISO/IEC 27001 e SOC 2 Tipo 2) abrangem a parte do BIR 2012 pela qual a Microsoft é responsável. O relatório resultante fornece um mapeamento dessas certificações e atestados existentes para os controles listados no padrão BIR 2012. Os clientes podem usar o relatório como uma ferramenta para ajudar a adotar o Azure em conformidade com o BIR 2012. O relatório demonstra claramente quais controles BIR 2012 são cobertos pela Microsoft e quais controles continuam sendo implementados pelos clientes. O relatório 'Microsoft Cloud: cobertura da linha de base do Azure e Office 365 BIR 2012' pode ser baixado da seção [Relatórios de Auditoria do Portal de Confiança do Serviço  - Relatórios de Avaliação do GRC](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3).

## <a name="frequently-asked-questions"></a>Perguntas frequentes

**O Microsoft BIR 2012 é certificado?**

A responsabilidade pela conformidade com o BIR aplica-se ao setor governamental. Ela exige que a organização implemente um sistema de gerenciamento de segurança das informações e trate do risco com medidas técnicas e organizacionais apropriadas. Para a Microsoft, no papel de provedor de serviços de nuvem, a conformidade com o BIR não é o objetivo nem é tecnicamente viável. Quando um cliente implementa ou utiliza os serviços em nuvem da Microsoft, esses serviços podem estar no escopo de uma avaliação do BIR. No entanto, a organização deve acrescentar seus próprios controles, escolhas e processos (adicionais) que fazem parte da avaliação geral do BIR. O objetivo do relatório é demonstrar que uma agência governamental pode adotar os serviços em nuvem da Microsoft de uma maneira que esteja em conformidade com o BIR 2012.

**Um cliente que usa os serviços em nuvem da Microsoft está em conformidade com o BIR 2012?**

A demonstração de conformidade com o BIR é responsabilidade do cliente. Ao usar um provedor de serviços de nuvem, os clientes geralmente exigem garantias do provedor e acrescentam sua própria tecnologia (adicional) e decisões, escolhas e processos organizacionais. Esse esforço resulta em uma avaliação geral do cliente quanto à sua conformidade com o BIR, que pode ser submetida para revisão ou certificação a um auditor externo. O relatório de cobertura BIR fornece uma visão sobre o que os controles BIR são cobertos pelos serviços de nuvem da Microsoft, mas como tal não cobre a conformidade de ponta a ponta.

**O relatório não mostra uma cobertura total. A conformidade com o BIR 2012 não é viável?**

Os serviços em nuvem da Microsoft fornecem muitos controles que ajudam as organizações dentro dos Países Baixos com suas necessidades de conformidade com o BIR. No entanto, uma organização precisa complementar essas garantias do provedor com suas próprias opções de implementação, controles adicionais de tecnologia e processos administrativos. O relatório já mostra mais de 91% de cobertura direta da lista completa de controles aplicáveis. Para os demais controles, a Microsoft fornece orientações no relatório sobre como a conformidade com esses controles pode ser demonstrada.

**O relatório sobre a cobertura do BIR é um documento de associação legal?**

Não. É uma ferramenta para dar suporte ao processo interno de garantia do BIR do cliente e ajudar a estabelecer a confiança sobre a viabilidade da conformidade com o BIR. O relatório tem um status descritivo e inclui um aviso de isenção de responsabilidade legal.

**Podemos compartilhar este relatório?**

O relatório é fornecido aos clientes sob um acordo de confidencialidade tendo como base o fato de destinar-se apenas a informações do cliente e que não será copiado ou divulgado por outros canais além do Microsoft [Service Trust Platform](https://www.microsoft.com/TrustCenter/STP/default.aspx). Os clientes podem compartilhar o relatório com seu próprio auditor interno ou externo como parte dos processos de conformidade ou garantia.

## <a name="resources"></a>Recursos

- [ISO-IEC 27001](offering-iso-27001.md)
- [Prescrição de segurança nacional 2013 (BVR)](https://wetten.overheid.nl/BWBR0033512/2013-06-01)
- [Prescrição de segurança das informações nacional 2007 (VIR)](https://wetten.overheid.nl/BWBR0022141/2007-07-01)
- [Segurança da informações da linha de base (BIR)](https://www.earonline.nl/index.php/BIR_2012)
- [Conformidade na Central de Confiabilidade da Microsoft](https://www.microsoft.com/trust-center/compliance/compliance-overview)
