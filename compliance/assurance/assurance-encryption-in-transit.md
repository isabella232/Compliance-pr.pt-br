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
# <a name="encryption-for-data-in-transit"></a>Criptografia para dados em trânsito

Além de proteger os dados do cliente em repouso, a Microsoft usa tecnologias de criptografia para proteger os dados do cliente em trânsito. Os dados estão em trânsito:

- quando um computador cliente se comunica com um servidor da Microsoft;
- quando um servidor Microsoft se comunica com outro servidor da Microsoft; e
- quando um servidor microsoft se comunica com um servidor que não é da Microsoft (por exemplo, Exchange Online entregando email para um servidor de email de terceiros).

As comunicações entre data center entre servidores da Microsoft ocorrem sobre TLS ou IPsec, e todos os servidores voltados para o cliente negociam uma sessão segura usando TLS com máquinas cliente (por exemplo, o Exchange Online usa TLS 1.2 com o uso de força de codificação de 256 bits (FIPS 140-2 Nível 2 validado). (Confira [detalhes de referência técnica sobre](/microsoft-365/compliance/technical-reference-details-about-encryption) criptografia para uma lista de pacote de codificação TLS suportados pelo Office 365.) Isso se aplica aos protocolos usados por clientes como o Outlook, o Skype for Business, o Microsoft Teams e o Outlook na Web (por exemplo, HTTP, POP3 etc.).

Os certificados públicos são emitidos pelo Microsoft IT SSL usando SSLAdmin, uma ferramenta interna da Microsoft para proteger a confidencialidade das informações transmitidas. Todos os certificados emitidos pela IT da Microsoft têm um comprimento mínimo de 2048 bits, e a conformidade com a Webtrust exige que o SSLAdmin certifique-se de que os certificados sejam emitidos apenas para endereços IP públicos pertencentes à Microsoft. Todos os endereços IP que não atenderem a esse critério serão roteados por meio de um processo de exceção.

Todos os detalhes de implementação, como a versão do TLS que está sendo usada, se o FS (FS) está habilitado, a ordem dos pacote de codificação, etc., estão disponíveis publicamente. Uma maneira de ver esses detalhes é usar um site de terceiros, como [a Qualys SSL Labs.](https://www.ssllabs.com) A seguir estão os links para páginas de teste automatizadas de Quaisys que exibem informações para os seguintes serviços:

- [Office 365 Portal](https://www.ssllabs.com/ssltest/analyze.html?d=portal.office.com&hideResults=on)
- [Exchange Online](https://www.ssllabs.com/ssltest/analyze.html?d=outlook.office365.com&hideResults=on)
- [SharePoint Online](https://www.ssllabs.com/ssltest/analyze.html?d=microsoft-my.sharepoint.com&hideResults=on)
- [Skype for Business (SIP)](https://www.ssllabs.com/ssltest/analyze.html?d=sipdir.online.lync.com)
- [Skype for Business (Web)](https://www.ssllabs.com/ssltest/analyze.html?d=webdir.online.lync.com&hideResults=on)
- [Proteção do Exchange Online](https://ssl-tools.net/mailservers/microsoft-com.mail.protection.outlook.com)
- [Microsoft Teams](https://www.ssllabs.com/ssltest/analyze.html?d=teams.microsoft.com&latest)

Para o Proteção do Exchange Online, as URLs variam de acordo com os nomes de locatários; No entanto, todos os clientes podem testar o Microsoft 365 usando **o microsoft-com.mail.protection.outlook.com**.
