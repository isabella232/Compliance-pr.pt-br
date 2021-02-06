---
title: Exclusão de dados do Microsoft 365 SharePoint Online
description: Saiba como a exclusão de dados funciona no SharePoint Online, como onde o conteúdo excluído é armazenado e por quanto tempo.
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
- SPO_Content
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 89281b32dbc577f935224396fd358ed753348ea1
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120740"
---
# <a name="sharepoint-online-data-deletion-in-microsoft-365"></a>Exclusão de dados do SharePoint Online no Microsoft 365

O SharePoint Online armazena objetos como código abstraído em bancos de dados de aplicativos. Quando um usuário carrega um arquivo no SharePoint Online, esse arquivo é desmontado e convertido em código de aplicativo e armazenado em várias tabelas em vários bancos de dados. No SharePoint Online, todo o conteúdo carregado pelo cliente é dividido em partes, criptografado (potencialmente com várias chaves AES de 256 bits) e distribuído pelo datacenter. Para obter detalhes específicos sobre o processo de partes e criptografia, consulte [Criptografia no Microsoft Cloud.](/microsoft-365/compliance/office-365-encryption-in-the-microsoft-cloud-overview) 

No SharePoint Online, os itens são mantidos por 93 dias a partir do momento em que você os exclui do local original. Eles permanecem na Lixeira do site o tempo todo, a menos que alguém os exclua ou esvazie essa Lixeira. Nesse caso, os itens vão para a Lixeira do conjunto de sites, onde permanecerão pelo restante dos 93 dias. Para obter informações sobre como restaurar itens excluídos, consulte Restaurar itens na Lixeira de um site do [SharePoint](https://support.office.com/article/6df466b6-55f2-4898-8d6e-c0dff851a0be#ID0EAADAAA=Online
) e restaurar itens excluídos da lixeira do conjunto [de sites.](https://support.office.com/article/5fa924ee-16d7-487b-9a0a-021b9062d14b) O tempo de retenção da Lixeira não é configurável no SharePoint Online.

Ao excluir um conjunto de sites, você também exclui a hierarquia de sites no conjunto e todo o conteúdo dentro deles:

- Documentos e bibliotecas de documentos
- Listas e dados de lista
- Definições de configuração do site
- Informações de função e segurança relacionadas ao site ou seus subsites
- Subsites do site de nível superior, seu conteúdo e informações do usuário

Se você excluir acidentalmente um conjunto de sites, ele poderá ser restaurado por um administrador global ou do SharePoint usando o centro de administração do SharePoint.

Os conjunto de sites excluídos são mantidos por 93 dias. Após 93 dias, sites e todo o conteúdo e as configurações serão excluídos permanentemente, incluindo listas, bibliotecas, páginas e subsites.

A exclusão permanente ocorre quando um usuário limpa itens excluídos da Lixeira do conjunto de sites, quando os períodos de retenção e backup expiram ou quando um administrador exclui permanentemente um conjunto de sites usando o [cmdlet Remove-SPODeletedSite.](/powershell/module/sharepoint-online/remove-spodeletedsite) Quando um usuário exclui permanentemente (ou exclui permanentemente) conteúdo do SharePoint Online, todas as chaves de criptografia para as partes excluídas também são excluídas. Os blocos nos discos que anteriormente armazenavam as partes excluídas são marcados como não usado e estão disponíveis para reutilizável.
