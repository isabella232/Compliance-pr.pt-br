---
title: Nível de impacto do Departamento de Defesa (DoD) 2 (IL2)
description: Saiba como a Microsoft atende aos padrões do Nível de Impacto do Departamento de Defesa (DoD) 2 (IL2).
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
ms.openlocfilehash: c57183a53c563fffa2bb3eb1cedb2fca23db26f4
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2021
ms.locfileid: "58947478"
---
# <a name="department-of-defense-dod-impact-level-2-il2"></a>Nível de impacto do Departamento de Defesa (DoD) 2 (IL2)

## <a name="dod-il2-overview"></a>Visão geral do DoD IL2

A Disa (Agência de Sistemas de Informações de Defesa) é uma agência do Departamento de Defesa dos EUA (DoD) responsável pelo desenvolvimento e manutenção do Guia de Requisitos de Segurança de Computação em Nuvem [(SRG)](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html)do DoD. O SRG define os requisitos de segurança de linha de base usados pelo DoD para avaliar a postura de segurança de um provedor de serviços de nuvem (CSP), dando suporte à decisão de conceder uma Autorização Provisória (PA) do DoD que permite que um CSP hospede missões do DoD. Ele incorpora, sobressalva e rescinde o Modelo de Segurança de Nuvem do DoD (CSM) publicado anteriormente e mapeia para a Estrutura de Gerenciamento de Riscos do DoD (RMF).

O DISA orienta as agências e departamentos do DoD no planejamento e autorização do uso de um CSP. Ele também avalia as ofertas de CSP para conformidade com o SRG, um processo de autorização no qual os CSPs podem fornecer documentação explicando sua conformidade com os padrões do DoD. Ele emite PAs (Autorizações Provisórias do DoD) quando apropriado, para que as agências do DoD e organizações de suporte possam usar serviços de nuvem sem precisar passar por um processo de aprovação completo por conta própria, economizando tempo e esforço.

O [memorando CIO do DoD 15](https://www.esi.mil/contentview.aspx?id=585) de  dezembro de 2014 sobre Diretrizes Atualizadas sobre a Aquisição e o Uso de Serviços comerciais de Computação em Nuvem afirma que 'FedRAMP servirá como a linha de base de segurança mínima para todos os serviços de nuvem do DoD'. O SRG usa a linha de base Moderada fedRAMP em todos os níveis de impacto de informações (IL) e considera a Linha de Base Alta em alguns.

O uso do DoD da Seção [5.1.1](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5SECURITYREQUIREMENTS) do SRG dos Controles de Segurança *fedRAMP* afirma que as informações il2 podem ser hospedadas em um CSP que detém minimamente uma PA moderada fedRAMP e uma PA de Nível 2 do DoD, sujeitas à conformidade com os requisitos de segurança da equipe descritos na Seção 5.6.2. No entanto, essa abordagem não alivia o CSP de atender a outros requisitos de segurança e integração, conforme exigido pelo Proprietário da Missão. De acordo com os Requisitos de Localização e SEPARAÇÃO do SRG Seção [5.2.2.1](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5.2LegalConsiderations) *IL2,* o DoD IL2 PA é adequadamente coberto por um PA moderado fedRAMP para que os requisitos não sejam avaliados adicionalmente para um PA IL2.

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Plataformas e serviços em nuvem no escopo da Microsoft

- Azure
- Dynamics 365
- Microsoft Cloud App Security
- Microsoft Defender para Ponto de Extremidade
- Microsoft Graph
- Microsoft Intune
- Microsoft Stream
- Office 365 Governo dos EUA, Office 365 governo dos EUA - Alta
- Power Apps
- Power Automate
- Power BI

## <a name="azure-dynamics-365-and-dod-il2"></a>Azure, Dynamics 365 e DoD IL2

Para obter mais informações sobre a conformidade do Azure, dynamics 365 e outros serviços online, consulte a oferta [do Azure DoD IL2](/azure/compliance/offerings/offering-dod-il2).

## <a name="office-365-and-dod-il2"></a>Office 365 e DoD IL2

### <a name="office-365-cloud-environments"></a>Ambientes da nuvem do Office 365

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Aplicabilidade do Office 365 e serviços no escopo

Use a seguinte tabela para determinar a aplicabilidade para seus serviços e assinatura do Office 365:

| **Aplicabilidade** | **Serviços no escopo** |
|:------------------|:----------------------|
| **GCC** | Serviço de Feed de Atividades, Serviços Bing, Delve, Proteção do Exchange Online, Exchange Online, Serviços Inteligentes, Microsoft Teams, Portal do Cliente Office 365, Office Online, infraestrutura de serviço Office, relatórios de uso Office, OneDrive for Business, Cartão de Pessoas, SharePoint Online, Skype for Business, Windows Ink |
| **GCC Alta** | Serviço de Feed de Atividades, Serviços Bing, Delve, Proteção do Exchange Online, Exchange Online, Serviços Inteligentes, Microsoft Teams, Portal do Cliente Office 365, Office Online, infraestrutura de serviço Office, relatórios de uso Office, OneDrive for Business, Cartão de Pessoas, SharePoint Online, Skype for Business, Windows Ink |

### <a name="resources"></a>Recursos

- [Soluções governamentais da Microsoft](https://www.microsoft.com/enterprise/government)
- [Guia de Requisitos de Segurança de Computação em Nuvem do DoD](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html)
- [Documentos fedRAMP](https://www.fedramp.gov/documents/)
- [NIST SP 800-37](https://csrc.nist.gov/publications/detail/sp/800-37/rev-2/final) *Risk Management Framework for Information Systems and Organizations: A System Life-Cycle Approach for Security and Privacy*
- Controles de Segurança e Privacidade do [NIST SP 800-53](https://csrc.nist.gov/Projects/risk-management/sp800-53-controls/release-search#!/800-53) *para sistemas e organizações de informações*
- [RmF (DoD Instruction 8510.01](https://www.esd.whs.mil/Portals/54/Documents/DD/issuances/dodi/851001p.pdf) *DoD Risk Management Framework) para Tecnologia de Informações do DoD (IT)*
