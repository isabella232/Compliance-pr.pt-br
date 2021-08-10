---
title: RGPD para Project Server
description: Aprenda a resolver Regulamentações Gerais de Proteção de Dados (RGPD) para o SharePoint Server local.
f1.keywords:
- NOCSH
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
titleSuffix: Microsoft GDPR
ms.custom: seo-marvel-apr2020
ms.collection: MS-Compliance
hideEdit: true
ms.openlocfilehash: 092bbe9e7abe0329e822b011d41b5db96f33d169606945f5801bc36771a1944c
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/05/2021
ms.locfileid: "54292938"
---
# <a name="gdpr-for-project-server"></a>RGPD para Project Server

O Project Server usa scripts personalizados para exportar e ocultar dados do usuário no Project Web App. O processo básico é o seguinte:

1.  Encontre os sites do Project Web App em seu farm.

2.  Encontre os projetos que contêm o usuário em cada site.

3.  Exporte e verifique os tipos de dados que você deseja analisar.

4.  Oculte os dados conforme for necessário.

Estas etapas são abordadas em detalhes nos seguintes artigos:

- [Exportar dados do usuário do Project Server](/Project/export-user-data-from-project-server?toc=/Office365/Enterprise/toc.json)

- [Excluir dados do usuário do Project Server](/Project/delete-user-data-from-project-server?toc=/Office365/Enterprise/toc.json)


Observe que o Project Server foi criado a partir do SharePoint Server e que ele registra eventos nos logs de ULS do SharePoint e no banco de dados de uso. Consulte [RGPD para SharePoint Server](gdpr-for-sharepoint-server.md) para ter mais informações.
