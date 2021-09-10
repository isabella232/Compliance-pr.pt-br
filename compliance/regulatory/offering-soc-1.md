---
title: Controles de Sistema e Organização (SOC) 1 Tipo 2
description: Saiba como os serviços em nuvem da Microsoft estão em conformidade com os padrões de Controle de Sistema e Organização (SOC) 1 Tipo 2 para segurança operacional.
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
ms.openlocfilehash: 8c374ce340538e4030e0cd07a2bdbe0aa4f4615d
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2021
ms.locfileid: "58947492"
---
# <a name="system-and-organization-controls-soc-1-type-2"></a>Controles de Sistema e Organização (SOC) 1 Tipo 2

## <a name="soc-1-type-2-overview"></a>Visão geral do SOC 1 Tipo 2

Os SOC (Controles de Sistema e Organização) para Organizações de Serviço são relatórios de controle interno criados pelo AICPA (American Institute of Certified Public Controls). Eles se destinam a examinar os serviços fornecidos por uma organização de serviço para que os usuários finais possam avaliar e resolver o risco associado a um serviço terceirizado.

Um atestado SOC 1 Tipo 2 é executado em:

- N. SSAE 18, Padrões de Atestado: Esclarecimento e Recodificação, que inclui a seção 320 da AT-C, relatório do *sobre um exame de controles em uma organização de serviço relevante para o controle interno das entidades de usuário sobre relatórios financeiros* (AICPA, padrões profissionais).
- Relatório SOC 1 sobre um Exame de Controles em uma Organização de Serviço Relevante para o Controle Interno de Entidades de Usuário Sobre Relatórios Pinanceiros (Guia AICPA).

Além da Declaração da AICPA sobre Normas para Compromissos de Atestado 18 (SSAE 18), a auditoria do Office 365 SOC 1 Tipo 2 é conduzida de acordo com a Norma Internacional sobre Compromissos de Atestado No. 3402 (ISAE 3402). O atestado SOC 1 substituiu o SAS 70, e é apropriado para relatórios sobre controles em uma organização de serviços relevantes para os controles internos das entidades usuárias sobre relatórios financeiros. Um relatório Tipo 2 inclui a opinião do auditor sobre a eficácia do controle para alcançar os objetivos de controle relacionados durante o período de monitoramento especificado.

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Plataformas e serviços em nuvem no escopo da Microsoft

Os serviços online da Microsoft no escopo são mostrados no relatório de atestado Azure SOC 1 Tipo 2:

- Microsoft Azure (para obter informações detalhadas, consulte as [Ofertas de Conformidade Azure da Microsoft](https://azure.microsoft.com/resources/microsoft-azure-compliance-offerings/) ou o relatório de certificação SOC 1 Tipo 2 do Azure)
- Azure DevOps (ver relatório de atestação SOC 1 Tipo 2 do Azure DevOps separado)
- Dynamics 365 (para obter informações detalhadas, ver relatório de atestado Azure SOC 1 Tipo 2)
- Microsoft 365 Defender
- MCAS (Microsoft Cloud App Security)
- Microsoft Defender para Ponto de Extremidade (anteriormente Proteção avançada contra ameaças do Microsoft Defender)
- Microsoft Defender para Identidade (anteriormente Proteção Avançada contra Ameaças do Azure)
- Microsoft Forms Pro (não está no escopo para Azure Governamental)
- Microsoft Graph
- Microsoft Intune
- Área de Trabalho Gerenciada da Microsoft (não está no escopo para Azure Governamental)
- Microsoft Stream
- Especialistas em Ameaças da Microsoft (não no escopo Azure Governamental)
- Portal de Indicação
- Office 365, Office 365 U.S. Government e Office 365 U.S. Government - High, Office 365 Government Defense
- Power Apps
- Power Automate
- Power BI
- Power Virtual Agents (não está no escopo para Azure Governamental)
- Conformidade de Atualizações (não está no escopo para Azure Governamental)

## <a name="azure-dynamics-365-and-soc-1"></a>Azure, Dynamics 365 e SOC 1

Para obter mais informações sobre o Azure, o Dynamics 365 e outros serviços de conformidade do serviços online, consulte [oferta do SOC 1 do Azure](/azure/compliance/offerings/offering-soc-1).

## <a name="office-365-and-soc-1"></a>Office 365 e SOC 1

### <a name="office-365-cloud-environments"></a>Ambientes da nuvem do Office 365

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Aplicabilidade do Office 365 e serviços no escopo

Use a seguinte tabela para determinar a aplicabilidade para seus serviços e assinatura do Office 365:

| **Aplicabilidade** | **Serviços no escopo** |
|:------------------|:----------------------|
| **Comercial** | Gerente de Conformidade, Sistema de Proteção de Dados do Cliente, Delve, Proteção do Exchange Online, Exchange Online, Formulários, Core, Identity Manager, Lockbox (Torus), Microsoft Teams, MyAnalytics, Portal do Cliente do Office 365, Microsserviços do Office 365 (incluindo, entre outros, Kaizala, ObjectStore, Sway, Serviço de Documento do PowerPoint Online, Serviço de Anotação de Consulta, School Data Sync, Siphon, Speech, StaffHub, eXtensible Application Program), Office Online, Infraestrutura de Serviços do Office, OneDrive for Business, Planner, PowerApps, Power Automate, Power BI, Project Online, Criptografia de Serviço com Chave do Cliente, SharePoint Online, Skype for Business |
| **GCC** | Azure Active Directory, Gerente de Conformidade, Delve, Exchange Online, Forms, Microsoft Defender para Office 365, Microsoft Teams, MyAnalytics, complemento de Conformidade Avançada do Office 365, Centro de Segurança e Conformidade do Office 365, Office Online, Office Pro Plus, OneDrive for Business, Planner, PowerApps, Power Automate, Power BI, SharePoint Online, Skype for Business, Stream |
| **GCC Alta** | Azure Active Directory, Exchange Online, Forms, Microsoft Defender para Office 365, Microsoft Teams, complemento de Conformidade Avançada do Office 365, Centro de Segurança e Conformidade do Office 365, Office Online, Office Pro Plus, OneDrive for Business, Planner, PowerApps, Power Automate, Power BI, SharePoint Online, Skype for Business |
| **DoD** | Azure Active Directory, Exchange Online, Microsoft Defender para Office 365, Microsoft Teams, complemento de Conformidade Avançada do Office 365, Centro de Segurança e Conformidade do Office 365, Office Online, Office Pro Plus, OneDrive for Business, Planner, Power Automate, Power BI, SharePoint Online, Skype for Business |

### <a name="office-365-audit-reports"></a>Relatórios de auditoria do Office 365

- [Relatório do Office 365 Core-SSAE 18 SOC 1](https://aka.ms/o365SOC-1)
- Ver as cartas de ponte e os relatórios de auditoria adicionais

Você deve ter uma assinatura ou uma conta de avaliação gratuita existente no Office 365 ou no Office 365 U.S. Government para baixar relatórios de atestado SOC 1 e SOC 2 e quaisquer cartas de ponte, conforme necessário.

### <a name="frequently-asked-questions"></a>Perguntas frequentes

**Com que frequência os relatórios SOC do Office 365 são emitidos?**

Os relatórios do SOC para o Office 365 e outros serviços online são baseados em uma janela de execução semestral de 12 meses (período de auditoria) com novos relatórios emitidos semestralmente (o período termina em 31 de março e 30 de setembro). As *cartas de ponte* são emitidas a cada trimestre para cobrir o período dos três meses anteriores. Por exemplo, a carta de janeiro abrange de 1 de outubro a 31 de dezembro, a carta de abril abrange de 1 de janeiro a 31 de março, a carta de julho abrange de 1 de abril a 30 de junho e a carta de outubro abrange de 1 de julho a 30 de setembro.

**Como os clientes podem se beneficiar do atestado do Office 365 SOC 1 Tipo 2?**

Os clientes podem usar o certificado Office 365 SOC 1 Tipo 2 quando perseguem seus próprios requisitos de conformidade específicos da indústria financeira, tais como Sarbanes-Oxley (SOX), Conselho Federal de Exame de Instituições Financeiras (FFIEC), Lei Gramm-Leach-Bliley (GLBA), e outros.

**Onde posso obter a documentação de auditoria do Office 365 SOC, incluindo cartas de ponte?**

Para obter links para a documentação de auditoria, consulte a seção de relatório de auditoria. Você deve ter uma assinatura existente ou uma conta de teste gratuita no Office 365 ou Office 365 do Governo dos Estados Unidos para fazer o login. Em seguida, você pode baixar certificados de auditoria, relatórios de avaliação e outros documentos aplicáveis para ajudá-lo com seus próprios requisitos regulatórios.

**Onde posso ver respostas de gerenciamento para exceções detectadas?**

As respostas de gerenciamento estão localizadas no final do relatório de atestado SOC. Pesquise por “Resposta de Gerenciamento” no documento.

**Onde posso ver as responsabilidades da entidade do usuário?**

As responsabilidades da entidade usuária estão localizadas no final do relatório de atestado SOC. Pesquise por “Responsabilidades da Entidade do Usuário” no documento.

### <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Usar o Gerenciador de Conformidade da Microsoft para avaliar o risco

O[Gerenciador de Conformidade da Microsoft](/microsoft-365/compliance/compliance-manager) é um recurso no [Centro de conformidade do Microsoft 365](/microsoft-365/compliance/microsoft-365-compliance-center) para ajudá-lo a entender a postura de conformidade da sua organização e executar ações para ajudar a reduzir os riscos. O Gerenciador de Conformidade oferece um modelo premium para criar uma avaliação para essa regulamentação. Encontre o modelo na página **modelos de avaliação** no Gerenciador de Conformidade. Saiba como [criar avaliações no Compliance Manager](/microsoft-365/compliance/compliance-manager-assessments).

### <a name="resources"></a>Recursos

- [Relatórios de auditoria do Portal de Confiança do Serviço](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3)
- [SSAE No. 18, Attestation Standards: Clarificação e Recodificação](https://www.aicpa.org/Research/Standards/AuditAttest/DownloadableDocuments/SSAE_No_18.pdf)
- [SOC 1 Relatório sobre um Exame de Controles em uma Organização de Serviços Relevante para o Controle Interno de Entidades Usuárias sobre Relatórios Financeiros (Guia AICPA) (disponível para compra)](https://future.aicpa.org/cpe-learning/publication/reporting-on-an-examination-of-controls-at-a-service-organization-relevant-to-user-entities-internal-control-over-financial-reporting-soc-1-guide-OPL)
