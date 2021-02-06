---
title: Controles de acesso empresarial do Microsoft 365 Yammer
description: Este artigo contém um breve resumo sobre os Controles de Acesso do Yammer Enterprise no ambiente de produção.
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
ms.openlocfilehash: 916f26d5f2defdfb21cb9babe3a64cf618e8cd4a
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120360"
---
# <a name="yammer-enterprise-access-controls"></a><span data-ttu-id="210ae-103">Controles de acesso empresarial do Yammer</span><span class="sxs-lookup"><span data-stu-id="210ae-103">Yammer enterprise access controls</span></span> 

<span data-ttu-id="210ae-104">O acesso físico e lógico ao ambiente de produção do Yammer é restrito a um pequeno conjunto de pessoas (infraestrutura e operações).</span><span class="sxs-lookup"><span data-stu-id="210ae-104">Physical and logical access to the Yammer production environment is restricted to a small set of people (infrastructure and operations).</span></span> <span data-ttu-id="210ae-105">Assim como com outros engenheiros do Microsoft 365, os engenheiros do Yammer têm zero acesso permanente aos dados do cliente.</span><span class="sxs-lookup"><span data-stu-id="210ae-105">As with other Microsoft 365 engineers, Yammer engineers have zero standing access to customer data.</span></span> <span data-ttu-id="210ae-106">O acesso deve ser solicitado usando um sistema de controle de acesso just-in-time baseado em aprovação semelhante ao Lockbox com um número limitado de aprovadores.</span><span class="sxs-lookup"><span data-stu-id="210ae-106">Access must be requested using an approval-based just-in-time access control system similar to Lockbox with a limited number of approvers.</span></span> <span data-ttu-id="210ae-107">Os aprovadores verificam a solicitação (por exemplo, verificam se a solicitação é legítima com base na necessidade, no caso comercial, no horário etc.) e aprovam ou negam a solicitação.</span><span class="sxs-lookup"><span data-stu-id="210ae-107">Approvers verify the request (for example, they verify whether the request is legitimate based on need, business case, time, etc.), and then approve or deny the request.</span></span> <span data-ttu-id="210ae-108">Se a solicitação for aprovada, o acesso JIT será concedido por um tempo definido e limitado.</span><span class="sxs-lookup"><span data-stu-id="210ae-108">If the request is approved, JIT access is granted for a defined and limited time.</span></span> <span data-ttu-id="210ae-109">Após o tempo de acesso ser excedido, o acesso expirará automaticamente.</span><span class="sxs-lookup"><span data-stu-id="210ae-109">After access time is exceeded, the access automatically expires.</span></span>

<span data-ttu-id="210ae-110">Assim como com outros serviços do Microsoft 365, todo o acesso ao ambiente de produção do Yammer usa a autenticação multifatório.</span><span class="sxs-lookup"><span data-stu-id="210ae-110">As with other Microsoft 365 services, all access to the Yammer production environment uses multi-factor authentication.</span></span> <span data-ttu-id="210ae-111">Todo o acesso e o histórico de comandos são atribuídos a um usuário e registrados e revisados regularmente pela equipe de segurança do Yammer.</span><span class="sxs-lookup"><span data-stu-id="210ae-111">All access and command history is attributed to a user, and logged and reviewed regularly by the Yammer security team.</span></span>

<span data-ttu-id="210ae-112">Para saber mais sobre administração e gerenciamento do Yammer, confira a ajuda [do administrador do Yammer.](/yammer/yammer-landing-page)</span><span class="sxs-lookup"><span data-stu-id="210ae-112">For more information about Yammer administration and management, see [Yammer admin help](/yammer/yammer-landing-page).</span></span>