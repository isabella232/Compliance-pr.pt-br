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
# <a name="service-resource-limits"></a>Limites de recursos de serviço

Os limites de recursos são imposto usando cotas (limites) e limitação. O Azure Active Directory (Azure AD) e os serviços individuais do Microsoft 365 usam ambos. Os limites são específicos do serviço e mudam ao longo do tempo à medida que novos recursos são adicionados. Para obter detalhes sobre os limites atuais para os vários serviços, consulte os seguintes tópicos:

- [Limites e restrições de serviço do Azure AD](/azure/azure-resource-manager/management/azure-subscription-service-limits)
- [Limites do Exchange Online](/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits)
- [Limites e limites de software do SharePoint Online](https://support.office.com/article/SharePoint-Online-software-boundaries-and-limits-8F34FF47-B749-408B-ABC0-B605E1F6D498)
- [Limites do Skype for Business](https://technet.microsoft.com/library/skype-for-business-online-limits.aspx)
- [Limites de API REST e Taxa do Yammer](https://developer.yammer.com/docs/rest-api-rate-limits)
- [Limites de tamanho do arquivo no Sway](https://support.office.com/article/File-size-limits-in-Sway-4db21bc6-b42b-499f-9272-66e089db109f)

Além desses limites, vários mecanismos de limitação são usados no Azure AD e no Microsoft 365. A otimização no serviço é especialmente importante, já que os recursos de rede nos datacenters da Microsoft são otimizados para o amplo conjunto de clientes que usam os serviços. Os mecanismos de throttling incluem:

- O Azure AD e o Microsoft 365 apresentam limitação no nível do usuário, que limitam o número de transações ou chamadas simultâneas (por script ou código) que podem ser executadas por um único usuário.
- Uma política de throttling padrão do PowerShell é atribuída a cada locatário na criação de locatários. Essas configurações afetam outros itens, como o número máximo de sessões simultâneas do PowerShell que podem ser abertas por um único administrador.
- Cada cliente do Exchange Online tem uma política padrão dos Serviços Web do Exchange (EWS) que é ajustada para operações de cliente EWS e a throttling que se aplica a todos os clientes do Outlook.
