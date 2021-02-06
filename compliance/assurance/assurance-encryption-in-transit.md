---
title: Criptografia para dados em trânsito
description: Neste artigo, encontre uma breve explicação sobre como a Microsoft criptografa dados de clientes do Microsoft 365 em trânsito.
ms.author: krowley
author: kccross
manager: laurawi
ms.reviewer: sosstah
f1.keywords:
- NOCSH
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_Enterprise
- M365-security-compliance
- Strat_O365_Enterprise
- MS-Compliance
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: b6d6ae53ef2ade842e0e9205c01b44fe17891a97
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120530"
---
# <a name="encryption-for-data-in-transit"></a><span data-ttu-id="5d431-103">Criptografia para dados em trânsito</span><span class="sxs-lookup"><span data-stu-id="5d431-103">Encryption for data-in-transit</span></span>

<span data-ttu-id="5d431-104">Além de proteger os dados do cliente em repouso, a Microsoft usa tecnologias de criptografia para proteger os dados do cliente em trânsito.</span><span class="sxs-lookup"><span data-stu-id="5d431-104">In addition to protecting customer data at rest, Microsoft uses encryption technologies to protect customer data in transit.</span></span> <span data-ttu-id="5d431-105">Os dados estão em trânsito:</span><span class="sxs-lookup"><span data-stu-id="5d431-105">Data is in transit:</span></span>

- <span data-ttu-id="5d431-106">quando um computador cliente se comunica com um servidor da Microsoft;</span><span class="sxs-lookup"><span data-stu-id="5d431-106">when a client machine communicates with a Microsoft server;</span></span>
- <span data-ttu-id="5d431-107">quando um servidor Microsoft se comunica com outro servidor da Microsoft; e</span><span class="sxs-lookup"><span data-stu-id="5d431-107">when a Microsoft server communicates with another Microsoft server; and</span></span>
- <span data-ttu-id="5d431-108">quando um servidor microsoft se comunica com um servidor que não é da Microsoft (por exemplo, Exchange Online entregando email para um servidor de email de terceiros).</span><span class="sxs-lookup"><span data-stu-id="5d431-108">when a Microsoft server communicates with a non-Microsoft server (for example, Exchange Online delivering email to a third-party email server).</span></span>

<span data-ttu-id="5d431-109">As comunicações entre data center entre servidores da Microsoft ocorrem sobre TLS ou IPsec, e todos os servidores voltados para o cliente negociam uma sessão segura usando TLS com máquinas cliente (por exemplo, o Exchange Online usa TLS 1.2 com o uso de força de codificação de 256 bits (FIPS 140-2 Nível 2 validado).</span><span class="sxs-lookup"><span data-stu-id="5d431-109">Inter-data center communications between Microsoft servers take place over TLS or IPsec, and all customer-facing servers negotiate a secure session using TLS with client machines (for example, Exchange Online uses TLS 1.2 with 256-bit cipher strength is used (FIPS 140-2 Level 2-validated).</span></span> <span data-ttu-id="5d431-110">(Confira [detalhes de referência técnica sobre](/microsoft-365/compliance/technical-reference-details-about-encryption) criptografia para uma lista de pacote de codificação TLS suportados pelo Office 365.) Isso se aplica aos protocolos usados por clientes como o Outlook, o Skype for Business, o Microsoft Teams e o Outlook na Web (por exemplo, HTTP, POP3 etc.).</span><span class="sxs-lookup"><span data-stu-id="5d431-110">(See [Technical reference details about encryption](/microsoft-365/compliance/technical-reference-details-about-encryption) for a list of TLS cipher suites supported by Office 365.) This applies to the protocols that are used by clients such as Outlook, Skype for Business, Microsoft Teams, and Outlook on the web (for example, HTTP, POP3, etc.).</span></span>

<span data-ttu-id="5d431-111">Os certificados públicos são emitidos pelo Microsoft IT SSL usando SSLAdmin, uma ferramenta interna da Microsoft para proteger a confidencialidade das informações transmitidas.</span><span class="sxs-lookup"><span data-stu-id="5d431-111">The public certificates are issued by Microsoft IT SSL using SSLAdmin, an internal Microsoft tool to protect confidentiality of transmitted information.</span></span> <span data-ttu-id="5d431-112">Todos os certificados emitidos pela IT da Microsoft têm um comprimento mínimo de 2048 bits, e a conformidade com a Webtrust exige que o SSLAdmin certifique-se de que os certificados sejam emitidos apenas para endereços IP públicos pertencentes à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="5d431-112">All certificates issued by Microsoft IT have a minimum of 2048 bits in length, and Webtrust compliance requires SSLAdmin to make sure that certificates are issued only to public IP addresses owned by Microsoft.</span></span> <span data-ttu-id="5d431-113">Todos os endereços IP que não atenderem a esse critério serão roteados por meio de um processo de exceção.</span><span class="sxs-lookup"><span data-stu-id="5d431-113">Any IP addresses that fail to meet this criterion are routed through an exception process.</span></span>

<span data-ttu-id="5d431-114">Todos os detalhes de implementação, como a versão do TLS que está sendo usada, se o FS (FS) está habilitado, a ordem dos pacote de codificação, etc., estão disponíveis publicamente.</span><span class="sxs-lookup"><span data-stu-id="5d431-114">All implementation details such as the version of TLS being used, whether Forward Secrecy (FS) is enabled, the order of cipher suites, etc., are available publicly.</span></span> <span data-ttu-id="5d431-115">Uma maneira de ver esses detalhes é usar um site de terceiros, como [a Qualys SSL Labs.](https://www.ssllabs.com)</span><span class="sxs-lookup"><span data-stu-id="5d431-115">One way to see these details is to use a third-party website, such as [Qualys SSL Labs](https://www.ssllabs.com).</span></span> <span data-ttu-id="5d431-116">A seguir estão os links para páginas de teste automatizadas de Quaisys que exibem informações para os seguintes serviços:</span><span class="sxs-lookup"><span data-stu-id="5d431-116">Below are the links to automated test pages from Qualys that display information for the following services:</span></span>

- [<span data-ttu-id="5d431-117">Office 365 Portal</span><span class="sxs-lookup"><span data-stu-id="5d431-117">Office 365 Portal</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=portal.office.com&hideResults=on)
- [<span data-ttu-id="5d431-118">Exchange Online</span><span class="sxs-lookup"><span data-stu-id="5d431-118">Exchange Online</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=outlook.office365.com&hideResults=on)
- [<span data-ttu-id="5d431-119">SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="5d431-119">SharePoint Online</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=microsoft-my.sharepoint.com&hideResults=on)
- [<span data-ttu-id="5d431-120">Skype for Business (SIP)</span><span class="sxs-lookup"><span data-stu-id="5d431-120">Skype for Business (SIP)</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=sipdir.online.lync.com)
- [<span data-ttu-id="5d431-121">Skype for Business (Web)</span><span class="sxs-lookup"><span data-stu-id="5d431-121">Skype for Business (Web)</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=webdir.online.lync.com&hideResults=on)
- [<span data-ttu-id="5d431-122">Proteção do Exchange Online</span><span class="sxs-lookup"><span data-stu-id="5d431-122">Exchange Online Protection</span></span>](https://ssl-tools.net/mailservers/microsoft-com.mail.protection.outlook.com)
- [<span data-ttu-id="5d431-123">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="5d431-123">Microsoft Teams</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=teams.microsoft.com&latest)

<span data-ttu-id="5d431-124">Para o Proteção do Exchange Online, as URLs variam de acordo com os nomes de locatários; No entanto, todos os clientes podem testar o Microsoft 365 usando **o microsoft-com.mail.protection.outlook.com**.</span><span class="sxs-lookup"><span data-stu-id="5d431-124">For Exchange Online Protection, URLs vary by tenant names; however, all customers can test Microsoft 365 using **microsoft-com.mail.protection.outlook.com**.</span></span>
