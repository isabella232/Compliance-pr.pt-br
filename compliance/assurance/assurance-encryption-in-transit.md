---
title: Criptografia para dados em trânsito
description: Neste artigo, encontre uma breve explicação sobre como a Microsoft criptografa Microsoft 365 dados do cliente em trânsito.
ms.author: krowley
author: kccross
manager: laurawi
ms.reviewer: sosstah
f1.keywords:
- NOCSH
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: medium
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
ms.openlocfilehash: ebeface33b0d5ba419773c13305c277d681e8400
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2021
ms.locfileid: "58946885"
---
# <a name="encryption-for-data-in-transit"></a>Criptografia para dados em trânsito

Além de proteger os dados do cliente em repouso, a Microsoft usa tecnologias de criptografia para proteger dados do cliente em trânsito. Os dados estão em trânsito:

- quando uma máquina cliente se comunica com um servidor Microsoft;
- quando um servidor Microsoft se comunica com outro servidor Microsoft; e
- quando um servidor Microsoft se comunica com um servidor que não seja da Microsoft (por exemplo, Exchange Online entrega de email para um servidor de email de terceiros).

As comunicações entre data center entre servidores Microsoft ocorrem em TLS ou IPsec e todos os servidores voltados para o cliente negociam uma sessão segura usando TLS com máquinas cliente (por exemplo, o Exchange Online usa TLS 1.2 com a força de codificação de 256 bits é usada (FIPS 140-2 Nível 2 validado). (Consulte [Detalhes de referência técnica sobre](/microsoft-365/compliance/technical-reference-details-about-encryption) criptografia para uma lista de pacote de codificação TLS com suporte Office 365.) Isso se aplica aos protocolos usados por clientes como Outlook, Skype for Business, Microsoft Teams e Outlook na Web (por exemplo, HTTP, POP3 etc.).

Os certificados públicos são emitidos pelo Microsoft IT SSL usando SSLAdmin, uma ferramenta interna da Microsoft para proteger a confidencialidade das informações transmitidas. Todos os certificados emitidos pela MICROSOFT IT têm no mínimo 2.048 bits de comprimento, e a conformidade com a Webtrust requer SSLAdmin para garantir que os certificados sejam emitidos apenas para endereços IP públicos pertencentes à Microsoft. Todos os endereços IP que não atendem a esse critério são roteados por meio de um processo de exceção.

Todos os detalhes da implementação, como a versão do TLS em uso, se o Segredo de Encaminhamento (FS) está habilitado, a ordem dos suites de codificação, etc., estão disponíveis publicamente. Uma maneira de ver esses detalhes é usar um site de terceiros, como [o Qualys SSL Labs](https://www.ssllabs.com). Abaixo estão os links para páginas de teste automatizadas de Quaisys que exibem informações para os seguintes serviços:

- [Office 365 Portal](https://www.ssllabs.com/ssltest/analyze.html?d=portal.office.com&hideResults=on)
- [Exchange Online](https://www.ssllabs.com/ssltest/analyze.html?d=outlook.office365.com&hideResults=on)
- [SharePoint Online](https://www.ssllabs.com/ssltest/analyze.html?d=microsoft-my.sharepoint.com&hideResults=on)
- [Skype for Business (SIP)](https://www.ssllabs.com/ssltest/analyze.html?d=sipdir.online.lync.com)
- [Skype for Business (Web)](https://www.ssllabs.com/ssltest/analyze.html?d=webdir.online.lync.com&hideResults=on)
- [Proteção do Exchange Online](https://ssl-tools.net/mailservers/microsoft-com.mail.protection.outlook.com)
- [Microsoft Teams](https://www.ssllabs.com/ssltest/analyze.html?d=teams.microsoft.com&latest)

Para Proteção do Exchange Online, as URLs variam de acordo com os nomes de locatários; no entanto, todos os clientes podem testar Microsoft 365 usando **microsoft-com.mail.protection.outlook.com**.
