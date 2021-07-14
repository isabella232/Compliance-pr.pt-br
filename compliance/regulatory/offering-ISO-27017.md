---
title: Código de Conduta ISO/IEC 27017:2015 para Controles de Segurança de Informações
description: Os serviços de nuvem da Microsoft implementaram esse Código de Conduta para Controles de Segurança de Informações.
keywords: Microsoft 365, conformidade, ofertas
localization_priority: Priority
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
ms.openlocfilehash: 6c431d856fc03f328148722c14dfc558082aacb5
ms.sourcegitcommit: 9b0c8852e73e2be54a0f9c6570da67f4964f616c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/12/2021
ms.locfileid: "53384721"
---
# <a name="isoiec-270172015-code-of-practice-for-information-security-controls"></a>Código de Conduta ISO/IEC 27017:2015 para Controles de Segurança de Informações

## <a name="iso-iec-27017-overview"></a>Visão geral da ISO/IEC 27017

O código de conduta ISO/IEC 27017:2015 foi criado para as empresas usarem como referência para a seleção de controles de segurança de informações de serviços de nuvem ao implementarem um sistema de gerenciamento de segurança de informações de computação em nuvem com base na ISO/IEC 27002:2013. Ele também pode ser usado por provedores de serviços de nuvem como um documento de orientação para a implementação de controles de proteção geralmente aceitos.

Esse padrão internacional fornece orientações adicionais de implementação específicas para a nuvem com base na ISO/IEC 27002 e oferece controles adicionais para lidar com ameaças e riscos de segurança de informações específicos da nuvem referentes às cláusulas 5-18 da ISO/IEC 27002: 2013 para controles, orientação de implementação e outras informações. Especificamente, esse padrão fornece orientações sobre 37 controles na ISO/IEC 27002 e também apresenta 7 controles novos que não estão duplicados na ISO/IEC 27002. Esses novos controles abordam as seguintes áreas importantes:

- Funções e responsabilidades compartilhadas em um ambiente de computação em nuvem
- Remoção e devolução de ativos de clientes no serviço de nuvem ao término do contrato
- Proteção e separação do ambiente virtual de um cliente dos ambientes de outros clientes
- Requisitos para fortalecimento das máquinas virtuais para atender a necessidades comerciais
- Procedimentos para operações administrativas de um ambiente de computação em nuvem
- Capacitação dos clientes para monitorar atividades relevantes em um ambiente de computação em nuvem
- Alinhamento do gerenciamento da segurança para redes virtuais e físicas

## <a name="microsoft-and-isoiec-27017"></a>Microsoft e ISO/IEC 27017

A ISO/IEC 27017 é única no que diz respeito a fornecer orientações para provedores e clientes de serviços de nuvem. Ele também fornece aos clientes de serviços de nuvem informações práticas sobre o que devem esperar dos provedores de serviços de nuvem. Os clientes podem se beneficiar diretamente da ISO/IEC 27017, garantindo que entendam as responsabilidades compartilhadas na nuvem.

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Plataformas e serviços em nuvem no escopo da Microsoft

- [Azure, Azure Governamental e Azure Alemanha](https://aka.ms/AzureCompliance)
- Segurança no aplicativo na nuvem da Microsoft
- [Dynamics 365, Dynamics 365 e Dynamics 365 Germany](https://aka.ms/d365-compliance-list)
- Intune
- Microsoft Defender para Ponto de Extremidade
- Microsoft Graph
- Bot do Microsoft Healthcare
- [Área de Trabalho Gerenciada da Microsoft](/microsoft-365/managed-desktop/intro/compliance)
- Office 365, Office 365 U.S. Government e Office 365 U.S. Government Defense e Office 365 Germany
- Serviço de nuvem do Power Automate (anteriormente Microsoft Flow) como um serviço autônomo ou incluído em um plano ou pacote do Office 365 ou Dynamics 365
- Serviço de nuvem do PowerApps como um serviço autônomo ou incluído em um plano ou pacote do Office 365 ou Dynamics 365
- Serviço de nuvem do Power BI como um serviço autônomo ou incluído em um plano ou pacote do Office 365
- Power BI incorporado

## <a name="azure-dynamics-365-and-iso-270172015"></a>Azure, Dynamics 365 e ISO 27017:2015

Para obter mais informações sobre o Azure, o Dynamics 365 e outros serviços de conformidade do serviços online, consulte [Oferta do ISO 27017 do Azure](/azure/compliance/offerings/offering-iso-27017).

## <a name="office-365-and-iso-270172015"></a>Office 365 e ISO 27017:2015

### <a name="office-365-cloud-environments"></a>Ambientes de nuvem do Office 365

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Aplicabilidade do Office 365 e serviços no escopo

Use a tabela a seguir para determinar a aplicabilidade de seus serviços e da assinatura do Office 365:

| **Aplicabilidade** | **Serviços no escopo** |
|:------------------|:----------------------|
| **Office 365** | Access Online, Azure Active Directory, Azure Communications Service, Compliance Manager, Customer Lockbox, Delve, Exchange Online Protection, Exchange Online, Forms, Griffin, Identity Manager, Lockbox (Torus), Microsoft Defender para Office 365, Microsoft Teams, MyAnalytics, Suplemento Avançado de Conformidade do Office 365, Portal do Cliente do Office 365, Microsserviços do Office 365 (incluindo, mas não limitado ao Kaizala, ObjectStore, Sway, PowerPoint Online Document Service, Query Annotation Service, School Data Sync, Siphon, Speech, StaffHub, eXtensible Application Program), Centro de Segurança e Conformidade do Office 365, Office Online, Office Pro Plus, Infraestrutura de Serviços do Office, OneDrive for Business, Planner, PowerApps, Power Automate, Power BI, Project Online, Criptografia de Serviço com Chave de Cliente, SharePoint Online, Skype for Business, Stream |
| **GCC** | Azure Active Directory, Exchange Online, Flow, Microsoft Defender para Office 365, Microsoft Teams, complemento de Conformidade Avançada do Office 365, Centro de Segurança e Conformidade do Office 365, Office Online, Office Pro Plus, OneDrive for Business, Planner, PowerApps, Power Automate, Power BI, SharePoint Online, Skype for Business, Stream |
| **GCC Alta** | Azure Active Directory, Exchange Online, Flow, Microsoft Defender para Office 365, Microsoft Teams, complemento de Conformidade Avançada do Office 365, Centro de Segurança e Conformidade do Office 365, Office Online, Office Pro Plus, OneDrive for Business, Planner, PowerApps, Power Automate, Power BI, SharePoint Online, Skype for Business |
| **DoD** | Azure Active Directory, Exchange Online, Flow, Microsoft Defender para Office 365, Microsoft Teams, complemento de Conformidade Avançada do Office 365, Centro de Segurança e Conformidade do Office 365, Office Online, Office Pro Plus, OneDrive for Business, Planner, PowerApps, Power Automate, Power BI, SharePoint Online, Skype for Business |

### <a name="office-365-audits-reports-and-certificates"></a>Auditorias, relatórios e certificados do Office 365

Os serviços de nuvem da Microsoft são auditados uma vez ao ano de acordo com o código de conduta da ISO/IEC 27017:2015 como parte do processo de certificação da ISO/IEC 27001:2013.

- [Office 365: Relatório da avaliação de auditoria do ISO 27001, 27018, ISO 27017 e 27017](https://aka.ms/o365isoreport)

### <a name="frequently-asked-questions"></a>Perguntas frequentes

**A quem esse padrão se aplica?**

Este código de conduta fornece controles e orientações de implementação tanto para provedores quanto para clientes de serviços de nuvem. Ele é estruturado em um formato semelhante ao da ISO/IEC 27002:2013.

**Onde posso ver as informações de conformidade da Microsoft com a ISO/IEC 27017:2015?**

Você pode baixar o [certificado ISO/IEC 27017:2015](https://aka.ms/azureiso27017) do Azure, Intune e Power BI.

**Posso usar a conformidade dos serviços Microsoft com a ISO/IEC 27017 no processo de certificação da minha organização?**

Sim. Se a sua empresa estiver buscando uma certificação para implementações realizadas em qualquer serviço de nuvem empresarial no escopo da Microsoft, você poderá usar as respectivas certificações da Microsoft em sua avaliação de conformidade. Contudo, você é responsável por contratar um avaliador para analisar a conformidade de sua implementação e pelos controles e processos dentro de sua organização.

**Como posso obter cópias dos relatórios de auditoria aplicáveis?**

O [Portal de Confiança do Serviço](https://aka.ms/stphelp) fornece relatórios de auditoria de terceiros independentes e outros documentos relacionadas. Você pode usar o portal para baixar e analisar essa documentação para obter assistência com seus próprios requisitos regulatórios.

### <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Use o Gerenciador de Conformidade da Microsoft para avaliar o risco

O[Gerenciador de Conformidade da Microsoft](/microsoft-365/compliance/compliance-manager) é um recurso no [Centro de conformidade do Microsoft 365](/microsoft-365/compliance/microsoft-365-compliance-center) para ajudá-lo a entender a postura de conformidade da sua organização e executar ações para ajudar a reduzir os riscos. O Gerenciador de Conformidade oferece um modelo premium para criar uma avaliação para essa regulamentação. Encontre o modelo na página **modelos de avaliação** no Gerenciador de Conformidade. Saiba como [criar avaliações no Compliance Manager](/microsoft-365/compliance/compliance-manager-assessments).

### <a name="resources"></a>Recursos

- [Código de conduta ISO/IEC 27017:2015](https://www.iso.org/iso/iso_catalogue/catalogue_tc/catalogue_detail.htm?csnumber=43757)
- [Termos do Microsoft Online Services](https://aka.ms/Online-Services-Terms)
- [Conformidade na Central de Confiabilidade da Microsoft](https://www.microsoft.com/trust-center/compliance/compliance-overview)
