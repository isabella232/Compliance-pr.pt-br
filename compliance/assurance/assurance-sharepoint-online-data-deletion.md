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
hideEdit: true
ms.openlocfilehash: e89a261e44ef4eb4a1399027b70be88fffb82036
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497410"
---
# <a name="sharepoint-online-data-deletion-in-microsoft-365"></a><span data-ttu-id="846e6-103">Exclusão de dados do SharePoint Online no Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="846e6-103">SharePoint Online data deletion in Microsoft 365</span></span>

<span data-ttu-id="846e6-104">O SharePoint Online armazena objetos como código abstraído em bancos de dados de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="846e6-104">SharePoint Online stores objects as abstracted code within application databases.</span></span> <span data-ttu-id="846e6-105">Quando um usuário carrega um arquivo no SharePoint Online, esse arquivo é desmontado e convertido em código de aplicativo e armazenado em várias tabelas em vários bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="846e6-105">When a user uploads a file to SharePoint Online, that file is disassembled and translated into application code and stored in multiple tables across multiple databases.</span></span> <span data-ttu-id="846e6-106">No SharePoint Online, todo o conteúdo que um cliente carrega é dividido em partes, criptografadas (potencialmente com várias chaves de 256 bits do AES) e distribuídas pelo datacenter.</span><span class="sxs-lookup"><span data-stu-id="846e6-106">In SharePoint Online, all content that a customer uploads is broken into chunks, encrypted (potentially with multiple AES 256-bit keys), and distributed across the datacenter.</span></span> <span data-ttu-id="846e6-107">Para obter detalhes específicos sobre o processo de criptografia e partes, consulte [Encryption in the Microsoft Cloud](/microsoft-365/compliance/office-365-encryption-in-the-microsoft-cloud-overview).</span><span class="sxs-lookup"><span data-stu-id="846e6-107">For specific details about the chunking and encryption process, see [Encryption in the Microsoft Cloud](/microsoft-365/compliance/office-365-encryption-in-the-microsoft-cloud-overview).</span></span> 

<span data-ttu-id="846e6-108">No SharePoint Online, os itens são mantidos por 93 dias a partir do momento em que você os exclui do local original.</span><span class="sxs-lookup"><span data-stu-id="846e6-108">In SharePoint Online, items are retained for 93 days from the time you delete them from their original location.</span></span> <span data-ttu-id="846e6-109">Eles ficam na Lixeira do site o tempo todo, a menos que alguém os exclua de lá ou esvazia essa Lixeira.</span><span class="sxs-lookup"><span data-stu-id="846e6-109">They stay in the site Recycle Bin the entire time, unless someone deletes them from there or empties that Recycle Bin.</span></span> <span data-ttu-id="846e6-110">Nesse caso, os itens vão para a Lixeira do conjunto de sites, onde ficam pelo restante dos 93 dias.</span><span class="sxs-lookup"><span data-stu-id="846e6-110">In that case, the items go to the site collection Recycle Bin, where they stay for the remainder of the 93 days.</span></span> <span data-ttu-id="846e6-111">Para obter informações sobre como restaurar itens excluídos, consulte [Restore items in the Recycle Bin of a SharePoint site](https://support.office.com/article/6df466b6-55f2-4898-8d6e-c0dff851a0be#ID0EAADAAA=Online
) and Restore [deleted items from the site collection recycle bin](https://support.office.com/article/5fa924ee-16d7-487b-9a0a-021b9062d14b).</span><span class="sxs-lookup"><span data-stu-id="846e6-111">For info about restoring deleted items, see [Restore items in the Recycle Bin of a SharePoint site](https://support.office.com/article/6df466b6-55f2-4898-8d6e-c0dff851a0be#ID0EAADAAA=Online
) and [Restore deleted items from the site collection recycle bin](https://support.office.com/article/5fa924ee-16d7-487b-9a0a-021b9062d14b).</span></span> <span data-ttu-id="846e6-112">O tempo de retenção da Lixeira não é configurável no SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="846e6-112">The Recycle Bin retention time is not configurable in SharePoint Online.</span></span>

<span data-ttu-id="846e6-113">Ao excluir um conjunto de sites, você também está excluindo a hierarquia de sites no conjunto e todo o conteúdo dentro deles:</span><span class="sxs-lookup"><span data-stu-id="846e6-113">When you delete a site collection, you're also deleting the hierarchy of sites in the collection, and all content within them:</span></span>

- <span data-ttu-id="846e6-114">Documentos e bibliotecas de documentos</span><span class="sxs-lookup"><span data-stu-id="846e6-114">Documents and document libraries</span></span>
- <span data-ttu-id="846e6-115">Listas e dados de lista</span><span class="sxs-lookup"><span data-stu-id="846e6-115">Lists and list data</span></span>
- <span data-ttu-id="846e6-116">Configurações do site</span><span class="sxs-lookup"><span data-stu-id="846e6-116">Site configuration settings</span></span>
- <span data-ttu-id="846e6-117">Informações de função e segurança relacionadas ao site ou seus subsites</span><span class="sxs-lookup"><span data-stu-id="846e6-117">Role and security information that is related to the site or its subsites</span></span>
- <span data-ttu-id="846e6-118">Subsites do site de nível superior, seus conteúdos e informações do usuário</span><span class="sxs-lookup"><span data-stu-id="846e6-118">Subsites of the top-level website, their contents, and user information</span></span>

<span data-ttu-id="846e6-119">Se você excluir acidentalmente um conjunto de sites, ele poderá ser restaurado por um administrador global ou do SharePoint usando o Centro de administração do SharePoint.</span><span class="sxs-lookup"><span data-stu-id="846e6-119">If you accidentally delete a site collection, it can be restored by a global or SharePoint admin using the SharePoint admin center.</span></span>

<span data-ttu-id="846e6-120">Os conjunto de sites excluídos são mantidos por 93 dias.</span><span class="sxs-lookup"><span data-stu-id="846e6-120">Deleted site collections are retained for 93 days.</span></span> <span data-ttu-id="846e6-121">Após 93 dias, sites e todo o conteúdo e as configurações serão excluídos permanentemente, incluindo listas, bibliotecas, páginas e subsites.</span><span class="sxs-lookup"><span data-stu-id="846e6-121">After 93 days, sites and all their content and settings are permanently deleted, including lists, libraries, pages, and any subsites.</span></span>

<span data-ttu-id="846e6-122">A exclusão dura ocorre quando um usuário limpa itens excluídos da Lixeira do conjunto de sites, quando os períodos de retenção e backup expiram ou quando um administrador exclui permanentemente um conjunto de sites usando o [cmdlet Remove-SPODeletedSite.](/powershell/module/sharepoint-online/remove-spodeletedsite)</span><span class="sxs-lookup"><span data-stu-id="846e6-122">Hard deletion occurs when a user purges deleted items from the site collection Recycle Bin, when the retention and backup periods expire, or when an administrator permanently deletes a site collection using the [Remove-SPODeletedSite cmdlet](/powershell/module/sharepoint-online/remove-spodeletedsite).</span></span> <span data-ttu-id="846e6-123">Quando um usuário exclui permanentemente (exclui ou limpa) conteúdo do SharePoint Online, todas as chaves de criptografia para as partes excluídas também são excluídas.</span><span class="sxs-lookup"><span data-stu-id="846e6-123">When a user hard deletes (permanently deletes, or purges) content from SharePoint Online, all encryption keys for the deleted chunks are also deleted.</span></span> <span data-ttu-id="846e6-124">Os blocos nos discos que anteriormente armazenavam as partes excluídas são marcados como não usado e disponíveis para reutilizável.</span><span class="sxs-lookup"><span data-stu-id="846e6-124">The blocks on the disks that previously stored the deleted chunks are marked as unused and available for re-use.</span></span>
