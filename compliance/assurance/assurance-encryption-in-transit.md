---
title: Criptografia para dados em trânsito
description: Neste artigo, encontre uma breve explicação sobre como a Microsoft criptografa dados do cliente do Microsoft 365 em trânsito.
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
hideEdit: true
ms.openlocfilehash: 227f74140ecd9b6283b92e8b0e87bd70912ec8e3
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497248"
---
# <a name="encryption-for-data-in-transit"></a><span data-ttu-id="fb6ef-103">Criptografia para dados em trânsito</span><span class="sxs-lookup"><span data-stu-id="fb6ef-103">Encryption for data-in-transit</span></span>

<span data-ttu-id="fb6ef-104">Além de proteger os dados do cliente em repouso, a Microsoft usa tecnologias de criptografia para proteger dados do cliente em trânsito.</span><span class="sxs-lookup"><span data-stu-id="fb6ef-104">In addition to protecting customer data at rest, Microsoft uses encryption technologies to protect customer data in transit.</span></span> <span data-ttu-id="fb6ef-105">Os dados estão em trânsito:</span><span class="sxs-lookup"><span data-stu-id="fb6ef-105">Data is in transit:</span></span>

- <span data-ttu-id="fb6ef-106">quando uma máquina cliente se comunica com um servidor Microsoft;</span><span class="sxs-lookup"><span data-stu-id="fb6ef-106">when a client machine communicates with a Microsoft server;</span></span>
- <span data-ttu-id="fb6ef-107">quando um servidor Microsoft se comunica com outro servidor Microsoft; e</span><span class="sxs-lookup"><span data-stu-id="fb6ef-107">when a Microsoft server communicates with another Microsoft server; and</span></span>
- <span data-ttu-id="fb6ef-108">quando um servidor Microsoft se comunica com um servidor que não seja da Microsoft (por exemplo, o Exchange Online entrega emails para um servidor de email de terceiros).</span><span class="sxs-lookup"><span data-stu-id="fb6ef-108">when a Microsoft server communicates with a non-Microsoft server (for example, Exchange Online delivering email to a third-party email server).</span></span>

<span data-ttu-id="fb6ef-109">As comunicações entre data center entre servidores Microsoft ocorrem em TLS ou IPsec e todos os servidores voltados para o cliente negociam uma sessão segura usando TLS com máquinas cliente (por exemplo, o Exchange Online usa TLS 1.2 com a força de criptografia de 256 bits é usada (FIPS 140-2 Nível 2 validado).</span><span class="sxs-lookup"><span data-stu-id="fb6ef-109">Inter-data center communications between Microsoft servers take place over TLS or IPsec, and all customer-facing servers negotiate a secure session using TLS with client machines (for example, Exchange Online uses TLS 1.2 with 256-bit cipher strength is used (FIPS 140-2 Level 2-validated).</span></span> <span data-ttu-id="fb6ef-110">(Consulte [Detalhes de referência técnica sobre](/microsoft-365/compliance/technical-reference-details-about-encryption) criptografia para uma lista de pacote de codificação TLS com suporte do Office 365.) Isso se aplica aos protocolos usados por clientes como Outlook, Skype for Business, Microsoft Teams e Outlook na Web (por exemplo, HTTP, POP3, etc.).</span><span class="sxs-lookup"><span data-stu-id="fb6ef-110">(See [Technical reference details about encryption](/microsoft-365/compliance/technical-reference-details-about-encryption) for a list of TLS cipher suites supported by Office 365.) This applies to the protocols that are used by clients such as Outlook, Skype for Business, Microsoft Teams, and Outlook on the web (for example, HTTP, POP3, etc.).</span></span>

<span data-ttu-id="fb6ef-111">Os certificados públicos são emitidos pelo Microsoft IT SSL usando SSLAdmin, uma ferramenta interna da Microsoft para proteger a confidencialidade das informações transmitidas.</span><span class="sxs-lookup"><span data-stu-id="fb6ef-111">The public certificates are issued by Microsoft IT SSL using SSLAdmin, an internal Microsoft tool to protect confidentiality of transmitted information.</span></span> <span data-ttu-id="fb6ef-112">Todos os certificados emitidos pela MICROSOFT IT têm no mínimo 2.048 bits de comprimento, e a conformidade com a Webtrust requer SSLAdmin para garantir que os certificados sejam emitidos apenas para endereços IP públicos pertencentes à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="fb6ef-112">All certificates issued by Microsoft IT have a minimum of 2048 bits in length, and Webtrust compliance requires SSLAdmin to make sure that certificates are issued only to public IP addresses owned by Microsoft.</span></span> <span data-ttu-id="fb6ef-113">Todos os endereços IP que não atendem a esse critério são roteados por meio de um processo de exceção.</span><span class="sxs-lookup"><span data-stu-id="fb6ef-113">Any IP addresses that fail to meet this criterion are routed through an exception process.</span></span>

<span data-ttu-id="fb6ef-114">Todos os detalhes da implementação, como a versão do TLS em uso, se o Segredo de Encaminhamento (FS) está habilitado, a ordem dos suites de codificação, etc., estão disponíveis publicamente.</span><span class="sxs-lookup"><span data-stu-id="fb6ef-114">All implementation details such as the version of TLS being used, whether Forward Secrecy (FS) is enabled, the order of cipher suites, etc., are available publicly.</span></span> <span data-ttu-id="fb6ef-115">Uma maneira de ver esses detalhes é usar um site de terceiros, como [o Qualys SSL Labs](https://www.ssllabs.com).</span><span class="sxs-lookup"><span data-stu-id="fb6ef-115">One way to see these details is to use a third-party website, such as [Qualys SSL Labs](https://www.ssllabs.com).</span></span> <span data-ttu-id="fb6ef-116">Abaixo estão os links para páginas de teste automatizadas de Quaisys que exibem informações para os seguintes serviços:</span><span class="sxs-lookup"><span data-stu-id="fb6ef-116">Below are the links to automated test pages from Qualys that display information for the following services:</span></span>

- [<span data-ttu-id="fb6ef-117">Office 365 Portal</span><span class="sxs-lookup"><span data-stu-id="fb6ef-117">Office 365 Portal</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=portal.office.com&hideResults=on)
- [<span data-ttu-id="fb6ef-118">Exchange Online</span><span class="sxs-lookup"><span data-stu-id="fb6ef-118">Exchange Online</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=outlook.office365.com&hideResults=on)
- [<span data-ttu-id="fb6ef-119">SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="fb6ef-119">SharePoint Online</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=microsoft-my.sharepoint.com&hideResults=on)
- [<span data-ttu-id="fb6ef-120">Skype for Business (SIP)</span><span class="sxs-lookup"><span data-stu-id="fb6ef-120">Skype for Business (SIP)</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=sipdir.online.lync.com)
- [<span data-ttu-id="fb6ef-121">Skype for Business (Web)</span><span class="sxs-lookup"><span data-stu-id="fb6ef-121">Skype for Business (Web)</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=webdir.online.lync.com&hideResults=on)
- [<span data-ttu-id="fb6ef-122">Proteção do Exchange Online</span><span class="sxs-lookup"><span data-stu-id="fb6ef-122">Exchange Online Protection</span></span>](https://ssl-tools.net/mailservers/microsoft-com.mail.protection.outlook.com)
- [<span data-ttu-id="fb6ef-123">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="fb6ef-123">Microsoft Teams</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=teams.microsoft.com&latest)

<span data-ttu-id="fb6ef-124">Para a Proteção do Exchange Online, as URLs variam de acordo com os nomes de locatários; no entanto, todos os clientes podem testar o Microsoft 365 usando **microsoft-com.mail.protection.outlook.com**.</span><span class="sxs-lookup"><span data-stu-id="fb6ef-124">For Exchange Online Protection, URLs vary by tenant names; however, all customers can test Microsoft 365 using **microsoft-com.mail.protection.outlook.com**.</span></span>
