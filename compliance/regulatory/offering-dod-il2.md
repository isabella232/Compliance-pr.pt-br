---
title: Nível de impacto do Departamento de Defesa (DoD) 2 (IL2)
description: Saiba como a Microsoft atende aos padrões do Nível de Impacto do Departamento de Defesa (DoD) 2 (IL2).
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
ms.openlocfilehash: 77e8cb50f815c167e50293d495b4a548a73d022e
ms.sourcegitcommit: 9b0c8852e73e2be54a0f9c6570da67f4964f616c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/12/2021
ms.locfileid: "53385692"
---
# <a name="department-of-defense-dod-impact-level-2-il2"></a><span data-ttu-id="bea93-104">Nível de impacto do Departamento de Defesa (DoD) 2 (IL2)</span><span class="sxs-lookup"><span data-stu-id="bea93-104">Department of Defense (DoD) Impact Level 2 (IL2)</span></span>

## <a name="dod-il2-overview"></a><span data-ttu-id="bea93-105">Visão geral do DoD IL2</span><span class="sxs-lookup"><span data-stu-id="bea93-105">DoD IL2 overview</span></span>

<span data-ttu-id="bea93-106">A Disa (Agência de Sistemas de Informações de Defesa) é uma agência do Departamento de Defesa dos EUA (DoD) responsável pelo desenvolvimento e manutenção do Guia de Requisitos de Segurança de Computação em Nuvem [(SRG)](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html)do DoD.</span><span class="sxs-lookup"><span data-stu-id="bea93-106">The Defense Information Systems Agency (DISA) is an agency of the US Department of Defense (DoD) that is responsible for developing and maintaining the DoD Cloud Computing [Security Requirements Guide (SRG)](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html).</span></span> <span data-ttu-id="bea93-107">O SRG define os requisitos de segurança de linha de base usados pelo DoD para avaliar a postura de segurança de um provedor de serviços de nuvem (CSP), dando suporte à decisão de conceder uma Autorização Provisória (PA) do DoD que permite que um CSP hospede missões do DoD.</span><span class="sxs-lookup"><span data-stu-id="bea93-107">The SRG defines the baseline security requirements used by DoD to assess the security posture of a cloud service provider (CSP), supporting the decision to grant a DoD Provisional Authorization (PA) that allows a CSP to host DoD missions.</span></span> <span data-ttu-id="bea93-108">Ele incorpora, sobressalva e rescinde o Modelo de Segurança de Nuvem do DoD (CSM) publicado anteriormente e mapeia para a Estrutura de Gerenciamento de Riscos do DoD (RMF).</span><span class="sxs-lookup"><span data-stu-id="bea93-108">It incorporates, supersedes, and rescinds the previously published DoD Cloud Security Model (CSM) and maps to the DoD Risk Management Framework (RMF).</span></span>

<span data-ttu-id="bea93-109">O DISA orienta as agências e departamentos do DoD no planejamento e autorização do uso de um CSP.</span><span class="sxs-lookup"><span data-stu-id="bea93-109">DISA guides DoD agencies and departments in planning and authorizing the use of a CSP.</span></span> <span data-ttu-id="bea93-110">Ele também avalia as ofertas de CSP para conformidade com o SRG, um processo de autorização no qual os CSPs podem fornecer documentação explicando sua conformidade com os padrões do DoD.</span><span class="sxs-lookup"><span data-stu-id="bea93-110">It also evaluates CSP offerings for compliance with the SRG, an authorization process whereby CSPs can furnish documentation outlining their compliance with DoD standards.</span></span> <span data-ttu-id="bea93-111">Ele emite PAs (Autorizações Provisórias do DoD) quando apropriado, para que as agências do DoD e organizações de suporte possam usar serviços de nuvem sem precisar passar por um processo de aprovação completo por conta própria, economizando tempo e esforço.</span><span class="sxs-lookup"><span data-stu-id="bea93-111">It issues DoD Provisional Authorizations (PAs) when appropriate, so DoD agencies and supporting organizations can use cloud services without having to go through a full approval process on their own, saving time and effort.</span></span>

<span data-ttu-id="bea93-112">O [memorando CIO do DoD 15](https://www.esi.mil/contentview.aspx?id=585) de  dezembro de 2014 sobre Diretrizes Atualizadas sobre a Aquisição e o Uso de Serviços comerciais de Computação em Nuvem afirma que 'FedRAMP servirá como a linha de base de segurança mínima para todos os serviços de nuvem do DoD'.</span><span class="sxs-lookup"><span data-stu-id="bea93-112">The [15 December 2014 DoD CIO memo](https://www.esi.mil/contentview.aspx?id=585) regarding *Updated Guidance on the Acquisition and Use of Commercial Cloud Computing Services* states that 'FedRAMP will serve as the minimum security baseline for all DoD cloud services'.</span></span> <span data-ttu-id="bea93-113">O SRG usa a linha de base Moderada fedRAMP em todos os níveis de impacto de informações (IL) e considera a Linha de Base Alta em alguns.</span><span class="sxs-lookup"><span data-stu-id="bea93-113">The SRG uses the FedRAMP Moderate baseline at all information impact levels (IL) and considers the High Baseline at some.</span></span>

<span data-ttu-id="bea93-114">O uso do DoD da Seção [5.1.1](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5SECURITYREQUIREMENTS) do SRG dos Controles de Segurança *fedRAMP* afirma que as informações il2 podem ser hospedadas em um CSP que detém minimamente uma PA moderada fedRAMP e uma PA de Nível 2 do DoD, sujeitas à conformidade com os requisitos de segurança da equipe descritos na Seção 5.6.2.</span><span class="sxs-lookup"><span data-stu-id="bea93-114">[SRG Section 5.1.1](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5SECURITYREQUIREMENTS) *DoD use of FedRAMP Security Controls* states that IL2 information may be hosted in a CSP that minimally holds a FedRAMP Moderate PA and a DoD Level 2 PA, subject to compliance with the personnel security requirements outlined in Section 5.6.2.</span></span> <span data-ttu-id="bea93-115">No entanto, essa abordagem não alivia o CSP de atender a outros requisitos de segurança e integração, conforme exigido pelo Proprietário da Missão.</span><span class="sxs-lookup"><span data-stu-id="bea93-115">However, this approach does not alleviate the CSP from meeting other security and integration requirements as required by the Mission Owner.</span></span> <span data-ttu-id="bea93-116">De acordo com os Requisitos de Localização e SEPARAÇÃO do SRG Seção [5.2.2.1](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5.2LegalConsiderations) *IL2,* o DoD IL2 PA é adequadamente coberto por um PA moderado fedRAMP para que os requisitos não sejam avaliados adicionalmente para um PA IL2.</span><span class="sxs-lookup"><span data-stu-id="bea93-116">According to [SRG Section 5.2.2.1](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5.2LegalConsiderations) *IL2 Location and Separation Requirements*, DoD IL2 PA is adequately covered by a FedRAMP Moderate PA such that the requirements will not be additionally assessed for an IL2 PA.</span></span>

## <a name="microsoft-in-scope-cloud-platforms--services"></a><span data-ttu-id="bea93-117">Plataformas de nuvem no escopo da Microsoft & serviços</span><span class="sxs-lookup"><span data-stu-id="bea93-117">Microsoft in-scope cloud platforms & services</span></span>

- <span data-ttu-id="bea93-118">Azure</span><span class="sxs-lookup"><span data-stu-id="bea93-118">Azure</span></span>
- <span data-ttu-id="bea93-119">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="bea93-119">Dynamics 365</span></span>
- <span data-ttu-id="bea93-120">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="bea93-120">Microsoft Cloud App Security</span></span>
- <span data-ttu-id="bea93-121">Microsoft Defender para Ponto de Extremidade</span><span class="sxs-lookup"><span data-stu-id="bea93-121">Microsoft Defender for Endpoint</span></span>
- <span data-ttu-id="bea93-122">Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="bea93-122">Microsoft Graph</span></span>
- <span data-ttu-id="bea93-123">Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="bea93-123">Microsoft Intune</span></span>
- <span data-ttu-id="bea93-124">Microsoft Stream</span><span class="sxs-lookup"><span data-stu-id="bea93-124">Microsoft Stream</span></span>
- <span data-ttu-id="bea93-125">Office 365 Governo dos EUA, Office 365 governo dos EUA - Alta</span><span class="sxs-lookup"><span data-stu-id="bea93-125">Office 365 U.S. Government, Office 365 U.S. Government - High</span></span>
- <span data-ttu-id="bea93-126">Aplicativos de energia</span><span class="sxs-lookup"><span data-stu-id="bea93-126">Power Apps</span></span>
- <span data-ttu-id="bea93-127">Power Automate</span><span class="sxs-lookup"><span data-stu-id="bea93-127">Power Automate</span></span>
- <span data-ttu-id="bea93-128">Power BI</span><span class="sxs-lookup"><span data-stu-id="bea93-128">Power BI</span></span>

## <a name="azure-dynamics-365-and-dod-il2"></a><span data-ttu-id="bea93-129">Azure, Dynamics 365 e DoD IL2</span><span class="sxs-lookup"><span data-stu-id="bea93-129">Azure, Dynamics 365, and DoD IL2</span></span>

<span data-ttu-id="bea93-130">Para obter mais informações sobre a conformidade do Azure, dynamics 365 e outros serviços online, consulte a oferta [do Azure DoD IL2](/azure/compliance/offerings/offering-dod-il2).</span><span class="sxs-lookup"><span data-stu-id="bea93-130">For more information about Azure, Dynamics 365, and other online services compliance, see the [Azure DoD IL2 offering](/azure/compliance/offerings/offering-dod-il2).</span></span>

## <a name="office-365-and-dod-il2"></a><span data-ttu-id="bea93-131">Office 365 e DoD IL2</span><span class="sxs-lookup"><span data-stu-id="bea93-131">Office 365 and DoD IL2</span></span>

### <a name="office-365-cloud-environments"></a><span data-ttu-id="bea93-132">Office 365 ambientes de nuvem</span><span class="sxs-lookup"><span data-stu-id="bea93-132">Office 365 cloud environments</span></span>

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a><span data-ttu-id="bea93-133">Office 365 aplicabilidade e serviços no escopo</span><span class="sxs-lookup"><span data-stu-id="bea93-133">Office 365 applicability and in-scope services</span></span>

<span data-ttu-id="bea93-134">Use a tabela a seguir para determinar a aplicabilidade para seus serviços Office 365 e assinatura:</span><span class="sxs-lookup"><span data-stu-id="bea93-134">Use the following table to determine applicability for your Office 365 services and subscription:</span></span>

| <span data-ttu-id="bea93-135">**Aplicabilidade**</span><span class="sxs-lookup"><span data-stu-id="bea93-135">**Applicability**</span></span> | <span data-ttu-id="bea93-136">**Serviços no escopo**</span><span class="sxs-lookup"><span data-stu-id="bea93-136">**In-scope services**</span></span> |
|:------------------|:----------------------|
| <span data-ttu-id="bea93-137">**GCC**</span><span class="sxs-lookup"><span data-stu-id="bea93-137">**GCC**</span></span> | <span data-ttu-id="bea93-138">Serviço de Feed de Atividades, Serviços Bing, Delve, Proteção do Exchange Online, Exchange Online, Serviços Inteligentes, Microsoft Teams, Portal do Cliente Office 365, Office Online, infraestrutura de serviço Office, relatórios de uso Office, OneDrive for Business, Cartão de Pessoas, SharePoint Online, Skype for Business, Windows Ink</span><span class="sxs-lookup"><span data-stu-id="bea93-138">Activity Feed Service, Bing Services, Delve, Exchange Online Protection, Exchange Online, Intelligent Services, Microsoft Teams, Office 365 Customer Portal, Office Online, Office Service Infrastructure, Office Usage Reports, OneDrive for Business, People Card, SharePoint Online, Skype for Business, Windows Ink</span></span> |
| <span data-ttu-id="bea93-139">**CCG Alto**</span><span class="sxs-lookup"><span data-stu-id="bea93-139">**GCC High**</span></span> | <span data-ttu-id="bea93-140">Serviço de Feed de Atividades, Serviços Bing, Delve, Proteção do Exchange Online, Exchange Online, Serviços Inteligentes, Microsoft Teams, Portal do Cliente Office 365, Office Online, infraestrutura de serviço Office, relatórios de uso Office, OneDrive for Business, Cartão de Pessoas, SharePoint Online, Skype for Business, Windows Ink</span><span class="sxs-lookup"><span data-stu-id="bea93-140">Activity Feed Service, Bing Services, Delve, Exchange Online Protection, Exchange Online, Intelligent Services, Microsoft Teams, Office 365 Customer Portal, Office Online, Office Service Infrastructure, Office Usage Reports, OneDrive for Business, People Card, SharePoint Online, Skype for Business, Windows Ink</span></span> |

### <a name="resources"></a><span data-ttu-id="bea93-141">Recursos</span><span class="sxs-lookup"><span data-stu-id="bea93-141">Resources</span></span>

- [<span data-ttu-id="bea93-142">Soluções governamentais da Microsoft</span><span class="sxs-lookup"><span data-stu-id="bea93-142">Microsoft government solutions</span></span>](https://www.microsoft.com/enterprise/government)
- [<span data-ttu-id="bea93-143">Guia de Requisitos de Segurança de Computação em Nuvem do DoD</span><span class="sxs-lookup"><span data-stu-id="bea93-143">DoD Cloud Computing Security Requirements Guide</span></span>](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html)
- [<span data-ttu-id="bea93-144">Documentos fedRAMP</span><span class="sxs-lookup"><span data-stu-id="bea93-144">FedRAMP documents</span></span>](https://www.fedramp.gov/documents/)
- <span data-ttu-id="bea93-145">[NIST SP 800-37](https://csrc.nist.gov/publications/detail/sp/800-37/rev-2/final) *Risk Management Framework for Information Systems and Organizations: A System Life-Cycle Approach for Security and Privacy*</span><span class="sxs-lookup"><span data-stu-id="bea93-145">[NIST SP 800-37](https://csrc.nist.gov/publications/detail/sp/800-37/rev-2/final) *Risk Management Framework for Information Systems and Organizations: A System Life-Cycle Approach for Security and Privacy*</span></span>
- <span data-ttu-id="bea93-146">Controles de Segurança e Privacidade do [NIST SP 800-53](https://csrc.nist.gov/Projects/risk-management/sp800-53-controls/release-search#!/800-53) *para sistemas e organizações de informações*</span><span class="sxs-lookup"><span data-stu-id="bea93-146">[NIST SP 800-53](https://csrc.nist.gov/Projects/risk-management/sp800-53-controls/release-search#!/800-53) *Security and Privacy Controls for Information Systems and Organizations*</span></span>
- <span data-ttu-id="bea93-147">[RmF (DoD Instruction 8510.01](https://www.esd.whs.mil/Portals/54/Documents/DD/issuances/dodi/851001p.pdf) *DoD Risk Management Framework) para Tecnologia de Informações do DoD (IT)*</span><span class="sxs-lookup"><span data-stu-id="bea93-147">[DoD Instruction 8510.01](https://www.esd.whs.mil/Portals/54/Documents/DD/issuances/dodi/851001p.pdf) *DoD Risk Management Framework (RMF) for DoD Information Technology (IT)*</span></span>
