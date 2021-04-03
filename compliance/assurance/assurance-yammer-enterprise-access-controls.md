---
title: Controles de acesso empresarial do Microsoft 365 Yammer
description: Este artigo contém um breve resumo sobre os Controles do Yammer Enterprise Access no ambiente de produção.
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
ms.openlocfilehash: df345d922bbd0c9106cf0714377803a9c0870d82
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497348"
---
# <a name="yammer-enterprise-access-controls"></a>Controles de acesso empresarial do Yammer 

O acesso físico e lógico ao ambiente de produção do Yammer é restrito a um pequeno conjunto de pessoas (infraestrutura e operações). Assim como com outros engenheiros do Microsoft 365, os engenheiros do Yammer não têm acesso permanente aos dados do cliente. O acesso deve ser solicitado usando um sistema de controle de acesso just-in-time baseado em aprovação semelhante ao Lockbox com um número limitado de aprovadores. Os aprovadores verificam a solicitação (por exemplo, eles verificam se a solicitação é legítima com base na necessidade, caso comercial, hora etc.) e aprovam ou negam a solicitação. Se a solicitação for aprovada, o acesso JIT será concedido por um tempo definido e limitado. Após o tempo de acesso ser excedido, o acesso expira automaticamente.

Assim como com outros serviços do Microsoft 365, todo o acesso ao ambiente de produção do Yammer usa autenticação multifatório. Todo o histórico de acesso e comando é atribuído a um usuário e registrado e revisado regularmente pela equipe de segurança do Yammer.

Para obter mais informações sobre administração e gerenciamento do Yammer, consulte [Ajuda do administrador do Yammer.](/yammer/yammer-landing-page)