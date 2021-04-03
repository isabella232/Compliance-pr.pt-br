---
title: RGPD para servidores do Office
description: Aprenda a resolver Regulamentações Gerais de Proteção de Dados (RGPD) para o SharePoint Server local.
f1.keywords:
- NOCSH
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
titleSuffix: Microsoft GDPR
ms.collection: MS-Compliance
ms.custom: seo-marvel-apr2020
hideEdit: true
ms.openlocfilehash: 58f3d9108fe36175c2ce879054a35c2cc94d93c8
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51496086"
---
# <a name="gdpr-for-office-on-premises-servers"></a><span data-ttu-id="98d12-103">RGPD para servidores locais do Office</span><span class="sxs-lookup"><span data-stu-id="98d12-103">GDPR for Office on-premises Servers</span></span>

<span data-ttu-id="98d12-p101">O RGPD (Regulamento Geral sobre a Proteção de Dados) apresenta os requisitos para as organizações protegerem dados pessoais adequadamente e atender adequadamente às solicitações de titulares de dados. Esta série de artigos fornece abordagens recomendadas para cargas de trabalho locais:</span><span class="sxs-lookup"><span data-stu-id="98d12-p101">The General Data Protection Regulation (GDPR) introduces requirements for organizations to protect personal data and respond appropriately to data subject requests. This series of articles provides recommended approaches for on-premises workloads:</span></span>

- [<span data-ttu-id="98d12-106">SharePoint Server</span><span class="sxs-lookup"><span data-stu-id="98d12-106">SharePoint Server</span></span>](gdpr-for-sharepoint-server.md)

- [<span data-ttu-id="98d12-107">Exchange Server</span><span class="sxs-lookup"><span data-stu-id="98d12-107">Exchange Server</span></span>](gdpr-for-exchange-server.md)

- [<span data-ttu-id="98d12-108">Skype for Business Server</span><span class="sxs-lookup"><span data-stu-id="98d12-108">Skype for Business Server</span></span>](gdpr-for-skype-for-business-server.md)

- [<span data-ttu-id="98d12-109">Project Server</span><span class="sxs-lookup"><span data-stu-id="98d12-109">Project Server</span></span>](gdpr-for-project-server.md)

- [<span data-ttu-id="98d12-110">Servidor do Office Web Apps e Servidor do Office Online</span><span class="sxs-lookup"><span data-stu-id="98d12-110">Office Web Apps Server and Office Online Server</span></span>](gdpr-for-office-online-server.md)

- [<span data-ttu-id="98d12-111">Compartilhamentos de arquivos locais</span><span class="sxs-lookup"><span data-stu-id="98d12-111">On-premises file shares</span></span>](gdpr-for-on-premises-file-shares.md)

<span data-ttu-id="98d12-112">Para obter mais informações sobre o RGPD e como a Microsoft pode ajudar você, confira a [Central de Confiabilidade da Microsoft](https://www.microsoft.com/trust-center/privacy/gdpr-overview
).</span><span class="sxs-lookup"><span data-stu-id="98d12-112">For more information about the GDPR and how Microsoft can help you, see the [Microsoft Trust Center](https://www.microsoft.com/trust-center/privacy/gdpr-overview
).</span></span>

<span data-ttu-id="98d12-p102">Antes de trabalhar com dados locais, consulte suas equipes de conformidade e jurídica para buscar orientações e saber mais sobre os esquemas e as abordagens existentes de classificação para trabalhar com dados pessoais. A Microsoft fornece recomendações para desenvolver e estender esquemas de classificação no Microsoft GDPR Data Discovery Toolkit em [https://aka.ms/gdprpartners](<https://aka.ms/gdprpartners>). Esse kit de ferramentas também descreve abordagens para mover dados locais para a nuvem, onde você pode usar recursos de governança de dados mais sofisticados, se desejar. Os artigos nesta seção fornecem recomendações para os dados destinados a permanecerem no local.</span><span class="sxs-lookup"><span data-stu-id="98d12-p102">Before doing any work with on-premises data, consult with your legal and compliance teams to seek guidance and to learn about existing classification schemas and approaches to working with personal data. Microsoft provides recommendations for developing and extending classifications schemas in the Microsoft GDPR Data Discovery Toolkit at [https://aka.ms/gdprpartners](<https://aka.ms/gdprpartners>). This toolkit also describes approaches for moving on-premises data to the cloud where you can use more sophisticated data governance capabilities, if this is desired. The articles in this section provide recommendations for data that is intended to remain on premises.</span></span>

<span data-ttu-id="98d12-p103">A ilustração a seguir lista os recursos recomendados para usar em cada uma dessas cargas de trabalho para descobrir, classificar, proteger e monitorar dados pessoais. Confira os artigos desta seção para saber mais.</span><span class="sxs-lookup"><span data-stu-id="98d12-p103">The following illustration lists recommended capabilities to use across each of these workloads to discover, classify, protect, and monitor personal data. See the articles in this section for more information.</span></span>

![Diagrama descrevendo os recursos para descobrir, classificar, proteger e monitorar dados pessoais entre cargas de trabalho](../media/gdpr-for-office-servers-image1.png)

## <a name="illustration-description"></a><span data-ttu-id="98d12-120">Descrição da ilustração</span><span class="sxs-lookup"><span data-stu-id="98d12-120">Illustration description</span></span>

<span data-ttu-id="98d12-121">Para maior acessibilidade, a tabela a seguir fornece os mesmos exemplos da ilustração.</span><span class="sxs-lookup"><span data-stu-id="98d12-121">For accessibility, the following table provides the same examples in the illustration.</span></span>

****

|<span data-ttu-id="98d12-122">Ação</span><span class="sxs-lookup"><span data-stu-id="98d12-122">Action</span></span>|<span data-ttu-id="98d12-123">Compartilhamentos de arquivos do Windows Server</span><span class="sxs-lookup"><span data-stu-id="98d12-123">Windows Server file shares</span></span>|<span data-ttu-id="98d12-124">SharePoint Server</span><span class="sxs-lookup"><span data-stu-id="98d12-124">SharePoint Server</span></span>|<span data-ttu-id="98d12-125">Exchange Server</span><span class="sxs-lookup"><span data-stu-id="98d12-125">Exchange Server</span></span>|<span data-ttu-id="98d12-126">Skype for Business</span><span class="sxs-lookup"><span data-stu-id="98d12-126">Skype for Business</span></span>|<span data-ttu-id="98d12-127">Project Server</span><span class="sxs-lookup"><span data-stu-id="98d12-127">Project Server</span></span>|
|---|---|---|---|---|---|
|<span data-ttu-id="98d12-128">Descobrir</span><span class="sxs-lookup"><span data-stu-id="98d12-128">Discover</span></span>|<span data-ttu-id="98d12-129">Scanner da Proteção de Informações do Azure<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="98d12-129">Azure Information Protection scanner<sup>\*</sup></span></span>|<span data-ttu-id="98d12-130">Centro de Pesquisa ou de Descoberta Eletrônica (depois que os dados forem classificados)</span><span class="sxs-lookup"><span data-stu-id="98d12-130">Search Center or eDiscovery (after data is classified)</span></span> <br/><br/> <span data-ttu-id="98d12-131">Scanner da Proteção de Informações do Azure<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="98d12-131">Azure Information Protection scanner<sup>\*</sup></span></span>|<span data-ttu-id="98d12-132">Portal de Descoberta Eletrônica do Exchange</span><span class="sxs-lookup"><span data-stu-id="98d12-132">Exchange eDiscovery Portal</span></span>|<span data-ttu-id="98d12-133">Portal de Descoberta Eletrônica do Exchange</span><span class="sxs-lookup"><span data-stu-id="98d12-133">Exchange eDiscovery portal</span></span>|<span data-ttu-id="98d12-134">Scripts SQL para descobrir e exportar</span><span class="sxs-lookup"><span data-stu-id="98d12-134">SQL scripts for discovery and exporting</span></span>|
|<span data-ttu-id="98d12-135">Classificar</span><span class="sxs-lookup"><span data-stu-id="98d12-135">Classify</span></span>|<span data-ttu-id="98d12-136">Scanner da Proteção de Informações do Azure<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="98d12-136">Azure Information Protection scanner<sup>\*</sup></span></span> <br/><br/> <span data-ttu-id="98d12-137">Tipos de informações confidenciais do Office 365</span><span class="sxs-lookup"><span data-stu-id="98d12-137">Office 365 sensitive information types</span></span>|<span data-ttu-id="98d12-138">Scanner da Proteção de Informações do Azure<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="98d12-138">Azure Information Protection scanner<sup>\*</sup></span></span> <br/><br/> <span data-ttu-id="98d12-139">Tipos de informações confidenciais do Office 365</span><span class="sxs-lookup"><span data-stu-id="98d12-139">Office 365 sensitive information types</span></span>|<span data-ttu-id="98d12-140">Marcas e políticas de retenção do Exchange</span><span class="sxs-lookup"><span data-stu-id="98d12-140">Exchange retention tags and retention policies</span></span>|<span data-ttu-id="98d12-141">Marcas e políticas de retenção do Exchange</span><span class="sxs-lookup"><span data-stu-id="98d12-141">Exchange retention tags and retention policies</span></span>||
|<span data-ttu-id="98d12-142">Proteger</span><span class="sxs-lookup"><span data-stu-id="98d12-142">Protect</span></span>||<span data-ttu-id="98d12-143">Regras de prevenção contra perda de dados do Exchange Server</span><span class="sxs-lookup"><span data-stu-id="98d12-143">Exchange Server data loss prevention rules</span></span> <br/><br/> <span data-ttu-id="98d12-144">Permissões, proteção do IRM para bibliotecas</span><span class="sxs-lookup"><span data-stu-id="98d12-144">Permissions, IRM-protection for libraries</span></span>|<span data-ttu-id="98d12-145">Regras de prevenção contra perda de dados do Exchange Server</span><span class="sxs-lookup"><span data-stu-id="98d12-145">Exchange Server data loss prevention rules</span></span> <br/><br/> <span data-ttu-id="98d12-146">Integração do IRM com o Exchange Server</span><span class="sxs-lookup"><span data-stu-id="98d12-146">IRM integration with Exchange Server</span></span>|||
|<span data-ttu-id="98d12-147">Monitorar</span><span class="sxs-lookup"><span data-stu-id="98d12-147">Monitor</span></span>|<span data-ttu-id="98d12-148">Integrar logs com ferramentas SIEM</span><span class="sxs-lookup"><span data-stu-id="98d12-148">Integrate logs with SIEM tools</span></span>|<span data-ttu-id="98d12-149">Integrar logs com ferramentas SIEM</span><span class="sxs-lookup"><span data-stu-id="98d12-149">Integrate logs with SIEM tools</span></span>|<span data-ttu-id="98d12-150">Integrar logs com ferramentas SIEM</span><span class="sxs-lookup"><span data-stu-id="98d12-150">Integrate logs with SIEM tools</span></span>|<span data-ttu-id="98d12-151">Integrar logs com ferramentas SIEM</span><span class="sxs-lookup"><span data-stu-id="98d12-151">Integrate logs with SIEM tools</span></span>|<span data-ttu-id="98d12-152">Integrar logs com ferramentas SIEM</span><span class="sxs-lookup"><span data-stu-id="98d12-152">Integrate logs with SIEM tools</span></span>|
|

<span data-ttu-id="98d12-153"><sup>\*</sup> Observe que a proteção criptografa o arquivo.</span><span class="sxs-lookup"><span data-stu-id="98d12-153"><sup>\*</sup> Note that protection encrypts the file.</span></span> <span data-ttu-id="98d12-154">Consequentemente, o SharePoint Server não consegue encontrar os tipos de informações confidenciais nos arquivos protegidos.</span><span class="sxs-lookup"><span data-stu-id="98d12-154">Consequently, SharePoint Server can't find the sensitive information types in protected files.</span></span>
