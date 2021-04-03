---
title: Controles de acesso administrativo no Microsoft 365
description: Este artigo fornece uma visão geral dos controles de acesso administrativo e categorização de dados no Microsoft 365.
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
f1.keywords:
- NOCSH
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: e7dc9d73b6eb1961387d85910bb558e85498ffae
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497697"
---
# <a name="administrative-access-controls-in-microsoft-365"></a><span data-ttu-id="4aef8-103">Controles de acesso administrativo no Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="4aef8-103">Administrative access controls in Microsoft 365</span></span> 

<span data-ttu-id="4aef8-104">A Microsoft investiu pesadamente em sistemas e controles que automatizam a maioria das operações do Microsoft 365, limitando intencionalmente o acesso ao conteúdo do cliente pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4aef8-104">Microsoft has invested heavily in systems and controls that automate most Microsoft 365 operations while intentionally limiting access to customer content by Microsoft.</span></span> <span data-ttu-id="4aef8-105">Os humanos governam o serviço e o software opera o serviço.</span><span class="sxs-lookup"><span data-stu-id="4aef8-105">Humans govern the service, and software operates the service.</span></span> <span data-ttu-id="4aef8-106">Essa estrutura permite que a Microsoft gerencie o Microsoft 365 em escala e gerencie os riscos de ameaças internas ao conteúdo do cliente.</span><span class="sxs-lookup"><span data-stu-id="4aef8-106">This structure enables Microsoft to manage Microsoft 365 at scale and manage the risks of internal threats to customer content.</span></span>

<span data-ttu-id="4aef8-107">Por padrão, os engenheiros da Microsoft têm zero privilégios administrativos permanentes e zero acesso permanente ao conteúdo do cliente no Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="4aef8-107">By default, Microsoft engineers have zero standing administrative privileges and zero standing access to customer content in Microsoft 365.</span></span> <span data-ttu-id="4aef8-108">Um engenheiro da Microsoft pode ter acesso limitado, auditado e protegido ao conteúdo de um cliente por um período limitado de tempo.</span><span class="sxs-lookup"><span data-stu-id="4aef8-108">A Microsoft engineer can have limited, audited, and secured access to a customer's content for a limited amount of time.</span></span> <span data-ttu-id="4aef8-109">O acesso é somente quando necessário para operações de serviço e somente quando aprovado por um membro do gerenciamento sênior da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4aef8-109">Access is only when necessary for service operations and only when approved by a member of Microsoft senior management.</span></span> <span data-ttu-id="4aef8-110">Para clientes licenciados no Customer Lockbox, o cliente fornece aprovação de acesso ao conteúdo hospedado no Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="4aef8-110">For Customer Lockbox licensed customers, the customer provides access approval to their content hosted on Microsoft 365.</span></span>

<span data-ttu-id="4aef8-111">A Microsoft fornece serviços online usando várias formas de entrega na nuvem:</span><span class="sxs-lookup"><span data-stu-id="4aef8-111">Microsoft provides online services using multiple forms of cloud delivery:</span></span>

- <span data-ttu-id="4aef8-112">**Nuvens públicas:** Inclui versões multi-locatários do Microsoft 365, Azure e outros serviços hospedados na América do Norte, América do Sul, Europa, Ásia, Austrália, etc.</span><span class="sxs-lookup"><span data-stu-id="4aef8-112">**Public clouds:** Includes multi-tenant versions of Microsoft 365, Azure, and other services hosted in North America, South America, Europe, Asia, Australia, etc.</span></span>
- <span data-ttu-id="4aef8-113">**Nuvens nacionais:** Inclui todas as nuvens soberanas e de terceiros operados fora dos Estados Unidos (exceto aquelas notadas anteriormente), como o Microsoft 365 na China (operado pela 21Vianet) e o Microsoft 365 na Alemanha (operado pela Microsoft, mas em um modelo no qual um administrador de dados alemão, Deutsche Telekom, controla e monitora o acesso da Microsoft aos dados do cliente e sistemas que contêm dados do cliente).</span><span class="sxs-lookup"><span data-stu-id="4aef8-113">**National clouds:** Includes all sovereign and third party-operated clouds outside of the United States (except ones noted previously), such as Microsoft 365 in China (operated by 21Vianet), and Microsoft 365 in Germany (operated by Microsoft, but under a model in which a German data trustee, Deutsche Telekom, controls and monitors Microsoft's access to customer data and systems that contain customer data).</span></span>
- <span data-ttu-id="4aef8-114">**Nuvens do governo:** Inclui serviços do Microsoft 365 e do Azure que estão disponíveis para clientes do governo dos Estados Unidos.</span><span class="sxs-lookup"><span data-stu-id="4aef8-114">**Government clouds:** Includes Microsoft 365 and Azure services that are available to United States government customers.</span></span>

<span data-ttu-id="4aef8-115">Para fins deste artigo, os serviços do Microsoft 365 incluem:</span><span class="sxs-lookup"><span data-stu-id="4aef8-115">For purposes of this article, Microsoft 365 services include:</span></span>

- [<span data-ttu-id="4aef8-116">Exchange Online</span><span class="sxs-lookup"><span data-stu-id="4aef8-116">Exchange Online</span></span>](/Exchange/exchange-online)
- [<span data-ttu-id="4aef8-117">Proteção do Exchange Online</span><span class="sxs-lookup"><span data-stu-id="4aef8-117">Exchange Online Protection</span></span>](/Office365/SecurityCompliance/eop/exchange-online-protection-overview)
- [<span data-ttu-id="4aef8-118">SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="4aef8-118">SharePoint Online</span></span>](/sharepoint/sharepoint-online)
- [<span data-ttu-id="4aef8-119">OneDrive for Business</span><span class="sxs-lookup"><span data-stu-id="4aef8-119">OneDrive for Business</span></span>](/OneDrive/onedrive)
- [<span data-ttu-id="4aef8-120">Skype for Business</span><span class="sxs-lookup"><span data-stu-id="4aef8-120">Skype for Business</span></span>](/SkypeForBusiness/skype-for-business-online)
- [<span data-ttu-id="4aef8-121">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="4aef8-121">Microsoft Teams</span></span>](/MicrosoftTeams/Teams-overview)
- [<span data-ttu-id="4aef8-122">Yammer</span><span class="sxs-lookup"><span data-stu-id="4aef8-122">Yammer</span></span>](/yammer/yammer-landing-page)

## <a name="microsoft-365-access-controls"></a><span data-ttu-id="4aef8-123">Controles de acesso do Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="4aef8-123">Microsoft 365 access controls</span></span>

<span data-ttu-id="4aef8-124">Para fins de controle de acesso, a Microsoft categoriza os dados do Microsoft 365 como dados do cliente ou outros tipos de dados.</span><span class="sxs-lookup"><span data-stu-id="4aef8-124">For access control purposes, Microsoft categorizes Microsoft 365 data as customer data or other types of data.</span></span>

### <a name="customer-data"></a><span data-ttu-id="4aef8-125">Dados do cliente</span><span class="sxs-lookup"><span data-stu-id="4aef8-125">Customer data</span></span>

<span data-ttu-id="4aef8-126">Os dados do cliente são todos os dados fornecidos por ou em nome de um cliente ao usar os serviços do Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="4aef8-126">Customer data is all data provided by or on behalf of a customer when using Microsoft 365 services.</span></span> <span data-ttu-id="4aef8-127">Esses dados são conteúdo do cliente criado ou carregado diretamente pelos usuários do Microsoft 365, incluindo:</span><span class="sxs-lookup"><span data-stu-id="4aef8-127">This data is customer content directly created or uploaded by Microsoft 365 users, including:</span></span>

- <span data-ttu-id="4aef8-128">Emails</span><span class="sxs-lookup"><span data-stu-id="4aef8-128">Emails</span></span>
- <span data-ttu-id="4aef8-129">Conteúdo do SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="4aef8-129">SharePoint Online content</span></span>
- <span data-ttu-id="4aef8-130">Mensagens instantâneas</span><span class="sxs-lookup"><span data-stu-id="4aef8-130">Instant messages</span></span>
- <span data-ttu-id="4aef8-131">Itens de calendário</span><span class="sxs-lookup"><span data-stu-id="4aef8-131">Calendar items</span></span>
- <span data-ttu-id="4aef8-132">Documentos</span><span class="sxs-lookup"><span data-stu-id="4aef8-132">Documents</span></span>
- <span data-ttu-id="4aef8-133">Contatos</span><span class="sxs-lookup"><span data-stu-id="4aef8-133">Contacts</span></span>
- <span data-ttu-id="4aef8-134">Informações de identificação do usuário final (EUII) (dados exclusivos de um usuário ou que podem ser vinculados a um usuário individual, mas não incluem conteúdo do cliente)</span><span class="sxs-lookup"><span data-stu-id="4aef8-134">End-user identifiable information (EUII) (data that is unique to a user or that is linkable to an individual user but does not include customer content)</span></span>

### <a name="other-types-of-data"></a><span data-ttu-id="4aef8-135">Outros tipos de dados</span><span class="sxs-lookup"><span data-stu-id="4aef8-135">Other types of data</span></span>

<span data-ttu-id="4aef8-136">Outros tipos de dados incluem:</span><span class="sxs-lookup"><span data-stu-id="4aef8-136">Other types of data include:</span></span>

- <span data-ttu-id="4aef8-137">**Dados da conta:** Inclui dados administrativos (informações fornecidas pelos administradores ao se inscrever ou comprar serviços) e dados de pagamento (informações sobre os instrumentos de pagamento, como detalhes do cartão de crédito).</span><span class="sxs-lookup"><span data-stu-id="4aef8-137">**Account data:** Includes administrative data (information provided by administrators when they sign-up or purchase services), and payment data (information about payment instruments, such as credit card details).</span></span>
- <span data-ttu-id="4aef8-138">**Informações de identificação organizacional:** Inclui dados usados para identificar um locatário, dados de uso e não vinculáveis a um usuário individual ou incluídos no conteúdo do cliente.</span><span class="sxs-lookup"><span data-stu-id="4aef8-138">**Organizationally identifiable information:** Includes data used to identify a tenant, usage data, and not linkable to an individual user or included in customer content.</span></span>
- <span data-ttu-id="4aef8-139">**Metadados do sistema:** Inclui logs de serviço que contêm configurações, status do sistema, endereços IP da Microsoft e informações técnicas sobre assinaturas e locatários.</span><span class="sxs-lookup"><span data-stu-id="4aef8-139">**System metadata:** Includes service logs that contain configuration settings, system status, Microsoft IP addresses, and technical information about subscriptions and tenants.</span></span>

<span data-ttu-id="4aef8-140">A Microsoft estabeleceu mecanismos de controle de acesso para garantir que ninguém tenha acesso não aprovado aos Dados do Cliente ou aos dados de controle de acesso.</span><span class="sxs-lookup"><span data-stu-id="4aef8-140">Microsoft has established access control mechanisms to ensure that no one has unapproved access to Customer Data or access control data.</span></span> <span data-ttu-id="4aef8-141">Os dados de controle de acesso gerenciam o acesso a outros tipos de dados ou funções no ambiente, incluindo o acesso ao conteúdo do cliente ou à EUII, senhas da Microsoft, certificados de segurança e outros dados relacionados à autenticação.</span><span class="sxs-lookup"><span data-stu-id="4aef8-141">Access control data manages access to other types of data or functions within the environment, including access to customer content or EUII, Microsoft passwords, security certificates, and other authentication-related data.</span></span> <span data-ttu-id="4aef8-142">Os mecanismos de controle de acesso também se resguardam contra acesso físico, lógico ou remoto não aprovado ao ambiente de produção do Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="4aef8-142">Access control mechanisms also guard against unapproved physical, logical, or remote access to the Microsoft 365 production environment.</span></span>

<span data-ttu-id="4aef8-143">Há três categorias de controles de acesso usados pela Microsoft para operar o Microsoft 365:</span><span class="sxs-lookup"><span data-stu-id="4aef8-143">There are three categories of access controls used by Microsoft for operating Microsoft 365:</span></span>

- <span data-ttu-id="4aef8-144">Controles de isolamento</span><span class="sxs-lookup"><span data-stu-id="4aef8-144">Isolation controls</span></span>
- <span data-ttu-id="4aef8-145">Controles de equipe</span><span class="sxs-lookup"><span data-stu-id="4aef8-145">Personnel controls</span></span>
- <span data-ttu-id="4aef8-146">Controles de tecnologia</span><span class="sxs-lookup"><span data-stu-id="4aef8-146">Technology controls</span></span>

<span data-ttu-id="4aef8-147">Quando combinados, esses controles ajudam a evitar e detectar ações mal-intencionadas no Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="4aef8-147">When combined, these controls help prevent and detect malicious actions in Microsoft 365.</span></span> <span data-ttu-id="4aef8-148">Além dos controles de isolamento, pessoal e tecnologia usados pela Microsoft, há uma quarta categoria de controles: os controles implementados pelos clientes.</span><span class="sxs-lookup"><span data-stu-id="4aef8-148">In addition to the isolation, personnel, and technology controls used by Microsoft, there is a fourth category of controls: those controls implemented by customers.</span></span>

<span data-ttu-id="4aef8-149">O Microsoft 365 permite gerenciar dados da mesma maneira que os dados são gerenciados em ambientes locais.</span><span class="sxs-lookup"><span data-stu-id="4aef8-149">Microsoft 365 allows you to manage data the same way data is managed in on-premises environments.</span></span> <span data-ttu-id="4aef8-150">A pessoa que insissou uma organização para o Microsoft 365 se torna automaticamente um administrador global.</span><span class="sxs-lookup"><span data-stu-id="4aef8-150">The person who signs up an organization for Microsoft 365 automatically becomes a global administrator.</span></span> <span data-ttu-id="4aef8-151">O administrador global tem acesso a todos os recursos em Portais de Gerenciamento e pode:</span><span class="sxs-lookup"><span data-stu-id="4aef8-151">The global admin has access to all features in Management Portals and can:</span></span>

- <span data-ttu-id="4aef8-152">Criar ou editar usuários</span><span class="sxs-lookup"><span data-stu-id="4aef8-152">Create or edit users</span></span>
- <span data-ttu-id="4aef8-153">Atribuir funções de administrador a outras pessoas</span><span class="sxs-lookup"><span data-stu-id="4aef8-153">Assign admin roles to others</span></span>
- <span data-ttu-id="4aef8-154">Redefinir senhas do usuário</span><span class="sxs-lookup"><span data-stu-id="4aef8-154">Reset user passwords</span></span>
- <span data-ttu-id="4aef8-155">Gerenciar licenças de usuário</span><span class="sxs-lookup"><span data-stu-id="4aef8-155">Manage user licenses</span></span>
- <span data-ttu-id="4aef8-156">Gerenciar domínios</span><span class="sxs-lookup"><span data-stu-id="4aef8-156">Manage domains</span></span>
- <span data-ttu-id="4aef8-157">Aprovar solicitações do Customer Lockbox</span><span class="sxs-lookup"><span data-stu-id="4aef8-157">Approve Customer Lockbox requests</span></span>

<span data-ttu-id="4aef8-158">Recomendamos que cada organização configure pelo menos duas contas de administrador.</span><span class="sxs-lookup"><span data-stu-id="4aef8-158">We recommend that each organization configure at least two admin accounts.</span></span> <span data-ttu-id="4aef8-159">Para grandes organizações empresariais, recomendamos contas de administrador especializadas que atendem a funções diferentes.</span><span class="sxs-lookup"><span data-stu-id="4aef8-159">For large enterprise organizations, we recommend specialized admin accounts that serve different functions.</span></span>

<span data-ttu-id="4aef8-160">Para obter informações sobre como atribuir funções e permissões de administrador, consulte [Assign admin roles](/microsoft-365/admin/add-users/assign-admin-roles) and About admin [roles](/microsoft-365/admin/add-users/about-admin-roles).</span><span class="sxs-lookup"><span data-stu-id="4aef8-160">For information about assigning admin roles and permissions, see [Assign admin roles](/microsoft-365/admin/add-users/assign-admin-roles) and [About admin roles](/microsoft-365/admin/add-users/about-admin-roles).</span></span>

## <a name="related-links"></a><span data-ttu-id="4aef8-161">Links relacionados</span><span class="sxs-lookup"><span data-stu-id="4aef8-161">Related Links</span></span>

- [<span data-ttu-id="4aef8-162">Isolamento no Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="4aef8-162">Isolation in Microsoft 365</span></span>](assurance-isolation-in-microsoft-365.md)
- [<span data-ttu-id="4aef8-163">Triagem de pré-emprego da Microsoft</span><span class="sxs-lookup"><span data-stu-id="4aef8-163">Microsoft pre-employment screening</span></span>](assurance-pre-employment-screening.md)
- [<span data-ttu-id="4aef8-164">Verificação de antecedentes da nuvem da Microsoft</span><span class="sxs-lookup"><span data-stu-id="4aef8-164">Microsoft cloud background check</span></span>](assurance-cloud-background-check.md)
- [<span data-ttu-id="4aef8-165">Monitorando e auditando controles de acesso </span><span class="sxs-lookup"><span data-stu-id="4aef8-165">Monitoring and Auditing Access Controls</span></span>](assurance-monitoring-and-auditing-access-controls.md)
- [<span data-ttu-id="4aef8-166">Controles de acesso do Yammer Enterprise</span><span class="sxs-lookup"><span data-stu-id="4aef8-166">Yammer Enterprise Access Controls</span></span>](assurance-yammer-enterprise-access-controls.md)
