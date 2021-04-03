---
title: Limites de recursos do Microsoft 365
description: Neste artigo, você pode encontrar informações sobre limites de recursos para os vários aplicativos no Microsoft 365.
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
ms.collection:
- Strat_O365_IP
- M365-security-compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 54ea001e542cdd1ab078546cf96bd011e27ab1dc
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497505"
---
# <a name="service-resource-limits"></a><span data-ttu-id="7f472-103">Limites de recursos de serviço</span><span class="sxs-lookup"><span data-stu-id="7f472-103">Service resource limits</span></span>

<span data-ttu-id="7f472-104">Os limites de recursos são imposto usando cotas (limites) e limitação.</span><span class="sxs-lookup"><span data-stu-id="7f472-104">Resource limits are enforced using quotas (limits) and throttling.</span></span> <span data-ttu-id="7f472-105">O Azure Active Directory (Azure AD) e os serviços individuais do Microsoft 365 usam ambos.</span><span class="sxs-lookup"><span data-stu-id="7f472-105">Azure Active Directory (Azure AD) and the individual Microsoft 365 services use both.</span></span> <span data-ttu-id="7f472-106">Os limites são específicos do serviço e mudam ao longo do tempo à medida que novos recursos são adicionados.</span><span class="sxs-lookup"><span data-stu-id="7f472-106">Limits are service-specific and change over time as new capabilities are added.</span></span> <span data-ttu-id="7f472-107">Para obter detalhes sobre os limites atuais para os vários serviços, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="7f472-107">For details on the current limits for the various services, see the following topics:</span></span>

- [<span data-ttu-id="7f472-108">Limites e restrições de serviço do Azure AD</span><span class="sxs-lookup"><span data-stu-id="7f472-108">Azure AD service limits and restrictions</span></span>](/azure/azure-resource-manager/management/azure-subscription-service-limits)
- [<span data-ttu-id="7f472-109">Limites do Exchange Online</span><span class="sxs-lookup"><span data-stu-id="7f472-109">Exchange Online Limits</span></span>](/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits)
- [<span data-ttu-id="7f472-110">Limites e limites de software do SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="7f472-110">SharePoint Online software boundaries and limits</span></span>](https://support.office.com/article/SharePoint-Online-software-boundaries-and-limits-8F34FF47-B749-408B-ABC0-B605E1F6D498)
- [<span data-ttu-id="7f472-111">Limites do Skype for Business</span><span class="sxs-lookup"><span data-stu-id="7f472-111">Skype for Business Limits</span></span>](https://technet.microsoft.com/library/skype-for-business-online-limits.aspx)
- [<span data-ttu-id="7f472-112">Limites de API REST e Taxa do Yammer</span><span class="sxs-lookup"><span data-stu-id="7f472-112">Yammer REST API and Rate Limits</span></span>](https://developer.yammer.com/docs/rest-api-rate-limits)
- [<span data-ttu-id="7f472-113">Limites de tamanho do arquivo no Sway</span><span class="sxs-lookup"><span data-stu-id="7f472-113">File Size Limits in Sway</span></span>](https://support.office.com/article/File-size-limits-in-Sway-4db21bc6-b42b-499f-9272-66e089db109f)

<span data-ttu-id="7f472-114">Além desses limites, vários mecanismos de limitação são usados no Azure AD e no Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="7f472-114">In addition to these limits, several throttling mechanisms are used throughout Azure AD and Microsoft 365.</span></span> <span data-ttu-id="7f472-115">A otimização no serviço é especialmente importante, já que os recursos de rede nos datacenters da Microsoft são otimizados para o amplo conjunto de clientes que usam os serviços.</span><span class="sxs-lookup"><span data-stu-id="7f472-115">Throttling within the service is especially important, given that network resources in Microsoft's datacenters are optimized for the broad set of customers that use the services.</span></span> <span data-ttu-id="7f472-116">Os mecanismos de throttling incluem:</span><span class="sxs-lookup"><span data-stu-id="7f472-116">Throttling mechanisms include:</span></span>

- <span data-ttu-id="7f472-117">O Azure AD e o Microsoft 365 apresentam limitação no nível do usuário, que limitam o número de transações ou chamadas simultâneas (por script ou código) que podem ser executadas por um único usuário.</span><span class="sxs-lookup"><span data-stu-id="7f472-117">Azure AD and Microsoft 365 feature user-level throttling, which limit the number of transactions or concurrent calls (by script or code) that can be performed by a single user.</span></span>
- <span data-ttu-id="7f472-118">Uma política de throttling padrão do PowerShell é atribuída a cada locatário na criação de locatários.</span><span class="sxs-lookup"><span data-stu-id="7f472-118">A default PowerShell throttling policy is assigned to each tenant at tenant creation.</span></span> <span data-ttu-id="7f472-119">Essas configurações afetam outros itens, como o número máximo de sessões simultâneas do PowerShell que podem ser abertas por um único administrador.</span><span class="sxs-lookup"><span data-stu-id="7f472-119">These settings affect other items, such as the maximum number of simultaneous PowerShell sessions that can be opened by a single administrator.</span></span>
- <span data-ttu-id="7f472-120">Cada cliente do Exchange Online tem uma política padrão dos Serviços Web do Exchange (EWS) que é ajustada para operações de cliente EWS e a throttling que se aplica a todos os clientes do Outlook.</span><span class="sxs-lookup"><span data-stu-id="7f472-120">Each Exchange Online customer has a default Exchange Web Services (EWS) policy that is tuned for EWS client operations, and throttling that applies to all Outlook clients.</span></span>
