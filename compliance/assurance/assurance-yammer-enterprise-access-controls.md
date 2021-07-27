---
title: Microsoft 365 Yammer controles de acesso empresarial
description: Este artigo contém um breve resumo sobre Yammer Enterprise Controles do Access no ambiente de produção.
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
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: ac02d8ba8719d9ef78a24bee37732007af7cba8b
ms.sourcegitcommit: 07578a8e03b931f47c49f4e34b78cf8ba0605e8f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/23/2021
ms.locfileid: "53573569"
---
# <a name="yammer-enterprise-access-controls"></a>Yammer controles de acesso empresarial 

O acesso físico e lógico ao ambiente Yammer de produção é restrito a um pequeno conjunto de pessoas (infraestrutura e operações). Assim como com outros engenheiros Microsoft 365, os engenheiros Yammer têm zero acesso permanente aos dados do cliente. O acesso deve ser solicitado usando um sistema de controle de acesso just-in-time baseado em aprovação semelhante ao Lockbox com um número limitado de aprovadores. Os aprovadores verificam a solicitação (por exemplo, eles verificam se a solicitação é legítima com base na necessidade, caso comercial, hora etc.) e aprovam ou negam a solicitação. Se a solicitação for aprovada, o acesso JIT será concedido por um tempo definido e limitado. Após o tempo de acesso ser excedido, o acesso expira automaticamente.

Assim como com outros Microsoft 365, todo o acesso ao ambiente Yammer de produção usa autenticação multifafatório. Todo o histórico de acesso e comando é atribuído a um usuário e registrado e revisado regularmente pela equipe Yammer segurança.

Para obter mais informações sobre Yammer administração e gerenciamento, [consulte Yammer ajuda do administrador.](/yammer/yammer-landing-page)