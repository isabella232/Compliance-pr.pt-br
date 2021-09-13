---
title: Microsoft 365 Limites de Recursos
description: Neste artigo, você pode encontrar informações sobre limites de recursos para os vários aplicativos dentro Microsoft 365.
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: medium
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 764259e22b23ecc7cea363283fc313a94875a2d1
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/12/2021
ms.locfileid: "59158048"
---
# <a name="service-resource-limits"></a>Limites de recursos de serviço

Os limites de recursos são imposto usando cotas (limites) e limitação. Azure Active Directory (Azure AD) e os serviços Microsoft 365 individuais usam ambos. Os limites são específicos do serviço e mudam ao longo do tempo à medida que novos recursos são adicionados. Para obter detalhes sobre os limites atuais para os vários serviços, consulte os seguintes tópicos:

- [Limites e restrições de serviço do Azure AD](/azure/azure-resource-manager/management/azure-subscription-service-limits)
- [Limites do Exchange Online](/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits)
- [SharePoint Limites e limites de software online](https://support.office.com/article/SharePoint-Online-software-boundaries-and-limits-8F34FF47-B749-408B-ABC0-B605E1F6D498)
- [Skype for Business Limites](https://technet.microsoft.com/library/skype-for-business-online-limits.aspx)
- [Yammer LIMITES DE TAXA e API REST](https://developer.yammer.com/docs/rest-api-rate-limits)
- [Limites de tamanho do arquivo no Sway](https://support.office.com/article/File-size-limits-in-Sway-4db21bc6-b42b-499f-9272-66e089db109f)

Além desses limites, vários mecanismos de limitação são usados em todo o Azure AD e Microsoft 365. A otimização no serviço é especialmente importante, já que os recursos de rede nos datacenters da Microsoft são otimizados para o amplo conjunto de clientes que usam os serviços. Os mecanismos de throttling incluem:

- O Azure AD e Microsoft 365 recursos de limitação no nível do usuário, que limitam o número de transações ou chamadas simultâneas (por script ou código) que podem ser executadas por um único usuário.
- Uma política de throttling padrão do PowerShell é atribuída a cada locatário na criação de locatários. Essas configurações afetam outros itens, como o número máximo de sessões simultâneas do PowerShell que podem ser abertas por um único administrador.
- Cada Exchange Online cliente tem uma política padrão de Serviços Web (EWS) padrão que é ajustada para operações de cliente EWS e a taxação que se aplica Exchange a todos os clientes Outlook.
