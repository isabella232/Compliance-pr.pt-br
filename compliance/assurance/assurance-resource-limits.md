---
title: Limites de recursos do Microsoft 365
description: Neste artigo, você pode encontrar informações sobre limites de recursos para vários aplicativos no Microsoft 365.
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
ms.openlocfilehash: 632a0b78c5c5ba02a59f8863c2e751f009cc968e
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120750"
---
# <a name="service-resource-limits"></a>Limites de recursos de serviço

Os limites de recursos são aplicados usando cotas (limites) e limitação. O Azure Active Directory (Azure AD) e os serviços individuais do Microsoft 365 usam ambos. Os limites são específicos do serviço e mudam ao longo do tempo à medida que novos recursos são adicionados. Para obter detalhes sobre os limites atuais para os vários serviços, consulte os seguintes tópicos:

- [Restrições e limites de serviço do Azure AD](/azure/azure-resource-manager/management/azure-subscription-service-limits)
- [Limites do Exchange Online](/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits)
- [Limites de software do SharePoint Online](https://support.office.com/article/SharePoint-Online-software-boundaries-and-limits-8F34FF47-B749-408B-ABC0-B605E1F6D498)
- [Limites do Skype for Business](https://technet.microsoft.com/library/skype-for-business-online-limits.aspx)
- [API REST e limites de taxa do Yammer](https://developer.yammer.com/docs/rest-api-rate-limits)
- [Limites de tamanho de arquivo no Sway](https://support.office.com/article/File-size-limits-in-Sway-4db21bc6-b42b-499f-9272-66e089db109f)

Além desses limites, vários mecanismos de limitação são usados no Azure AD e no Microsoft 365. A otimização no serviço é especialmente importante, já que os recursos de rede nos datacenters da Microsoft são otimizados para o amplo conjunto de clientes que usam os serviços. Os mecanismos de controle incluem:

- O Azure AD e o Microsoft 365 apresentam limitação no nível do usuário, que limita o número de transações ou chamadas simultâneas (por script ou código) que podem ser executadas por um único usuário.
- Uma política de throttling padrão do PowerShell é atribuída a cada locatário na criação do locatário. Essas configurações afetam outros itens, como o número máximo de sessões simultâneas do PowerShell que podem ser abertas por um único administrador.
- Cada cliente do Exchange Online tem uma política padrão dos Serviços Web do Exchange (EWS) que é ajustada para operações de cliente EWS e que se aplica a todos os clientes do Outlook.
