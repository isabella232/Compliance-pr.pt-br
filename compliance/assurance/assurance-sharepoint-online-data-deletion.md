---
title: Microsoft 365 SharePoint Exclusão de Dados Online
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
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 5a507dcd68aeda46ccf744e31828559aa6102a4f0fc50987f97041c6da8ab56f
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/05/2021
ms.locfileid: "54292039"
---
# <a name="sharepoint-online-data-deletion-in-microsoft-365"></a>SharePoint Exclusão de dados online em Microsoft 365

SharePoint O Online armazena objetos como código abstraído em bancos de dados de aplicativos. Quando um usuário carrega um arquivo para SharePoint Online, esse arquivo é desmontado e convertido em código de aplicativo e armazenado em várias tabelas em vários bancos de dados. No SharePoint Online, todo o conteúdo que um cliente carrega é dividido em partes, criptografadas (potencialmente com várias chaves de 256 bits do AES) e distribuídas pelo datacenter. Para obter detalhes específicos sobre o processo de criptografia e partes, consulte [Encryption in the Microsoft Cloud](/microsoft-365/compliance/office-365-encryption-in-the-microsoft-cloud-overview). 

No SharePoint Online, os itens são mantidos por 93 dias a partir do momento em que você os exclui do local original. Eles ficam na Lixeira do site o tempo todo, a menos que alguém os exclua de lá ou esvazia essa Lixeira. Nesse caso, os itens vão para a Lixeira do conjunto de sites, onde ficam pelo restante dos 93 dias. Para obter informações sobre como restaurar itens excluídos, consulte [Restore items in the Recycle Bin of a SharePoint site](https://support.office.com/article/6df466b6-55f2-4898-8d6e-c0dff851a0be#ID0EAADAAA=Online
) and Restore [deleted items from the site collection recycle bin](https://support.office.com/article/5fa924ee-16d7-487b-9a0a-021b9062d14b). O tempo de retenção da Lixeira não é configurável no SharePoint Online.

Ao excluir um conjunto de sites, você também está excluindo a hierarquia de sites no conjunto e todo o conteúdo dentro deles:

- Documentos e bibliotecas de documentos
- Listas e dados de lista
- Configurações do site
- Informações de função e segurança relacionadas ao site ou seus subsites
- Subsites do site de nível superior, seus conteúdos e informações do usuário

Se você excluir acidentalmente um conjunto de sites, ele poderá ser restaurado por um administrador global ou SharePoint usando o SharePoint de administração.

Os conjunto de sites excluídos são mantidos por 93 dias. Após 93 dias, sites e todo o conteúdo e as configurações serão excluídos permanentemente, incluindo listas, bibliotecas, páginas e subsites.

A exclusão dura ocorre quando um usuário limpa itens excluídos da Lixeira do conjunto de sites, quando os períodos de retenção e backup expiram ou quando um administrador exclui permanentemente um conjunto de sites usando o [cmdlet Remove-SPODeletedSite.](/powershell/module/sharepoint-online/remove-spodeletedsite) Quando um usuário exclui (exclui permanentemente ou limpa) o conteúdo do SharePoint Online, todas as chaves de criptografia para as partes excluídas também são excluídas. Os blocos nos discos que anteriormente armazenavam as partes excluídas são marcados como não usado e disponíveis para reutilizável.
