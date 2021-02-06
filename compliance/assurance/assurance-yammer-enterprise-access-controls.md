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
# <a name="yammer-enterprise-access-controls"></a>Controles de acesso empresarial do Yammer 

O acesso físico e lógico ao ambiente de produção do Yammer é restrito a um pequeno conjunto de pessoas (infraestrutura e operações). Assim como com outros engenheiros do Microsoft 365, os engenheiros do Yammer têm zero acesso permanente aos dados do cliente. O acesso deve ser solicitado usando um sistema de controle de acesso just-in-time baseado em aprovação semelhante ao Lockbox com um número limitado de aprovadores. Os aprovadores verificam a solicitação (por exemplo, verificam se a solicitação é legítima com base na necessidade, no caso comercial, no horário etc.) e aprovam ou negam a solicitação. Se a solicitação for aprovada, o acesso JIT será concedido por um tempo definido e limitado. Após o tempo de acesso ser excedido, o acesso expirará automaticamente.

Assim como com outros serviços do Microsoft 365, todo o acesso ao ambiente de produção do Yammer usa a autenticação multifatório. Todo o acesso e o histórico de comandos são atribuídos a um usuário e registrados e revisados regularmente pela equipe de segurança do Yammer.

Para saber mais sobre administração e gerenciamento do Yammer, confira a ajuda [do administrador do Yammer.](/yammer/yammer-landing-page)