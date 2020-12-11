---
title: RGPD para compartilhamentos de arquivos locais
description: Aprenda a resolver os requisitos gerais de RGPD (Regulamentações Gerais de Proteção de Dados) em compartilhamentos de arquivos locais do Windows Server.
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
ms.openlocfilehash: 5a3b192e4c374dac4248300627e5659a1b5f66fd
ms.sourcegitcommit: 18c7e403d6ffbc9afa323fadc04c673dbb7bd391
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "49620756"
---
# <a name="gdpr-for-on-premises-windows-server-file-shares"></a><span data-ttu-id="b4906-103">RGPD para compartilhamentos de arquivos no Windows Server local</span><span class="sxs-lookup"><span data-stu-id="b4906-103">GDPR for on-premises Windows Server file shares</span></span>

<span data-ttu-id="b4906-104">A abordagem básica recomendada para compartilhamentos de arquivos é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="b4906-104">The basic recommended approach for file shares is:</span></span>

-   <span data-ttu-id="b4906-105">Use a Proteção de Informações do Azure para identificar os dados confidenciais.</span><span class="sxs-lookup"><span data-stu-id="b4906-105">Use Azure Information Protection to label sensitive data.</span></span>

-   <span data-ttu-id="b4906-106">Use o verificador da Proteção de Informações do Azure para encontrar dados.</span><span class="sxs-lookup"><span data-stu-id="b4906-106">Use Azure Information Protection scanner to find data.</span></span>

<span data-ttu-id="b4906-107">A abordagem recomendada para compartilhamentos de arquivos inclui estas etapas:</span><span class="sxs-lookup"><span data-stu-id="b4906-107">The recommended approach for files shares includes these steps:</span></span>

1.  <span data-ttu-id="b4906-108">**Instale e configure o verificador da Proteção de Informações do Azure.**</span><span class="sxs-lookup"><span data-stu-id="b4906-108">**Install and configure Azure Information Protection scanner.**</span></span>

    -   <span data-ttu-id="b4906-109">Decida quais tipos de dados confidenciais usar.</span><span class="sxs-lookup"><span data-stu-id="b4906-109">Decide which sensitive data types to use.</span></span>

    -   <span data-ttu-id="b4906-110">Especifique pastas locais e compartilhamentos de rede a serem usados.</span><span class="sxs-lookup"><span data-stu-id="b4906-110">Specify local folders and network shares to use.</span></span>

2.  <span data-ttu-id="b4906-111">**Execute um ciclo de descoberta.**</span><span class="sxs-lookup"><span data-stu-id="b4906-111">**Complete a discovery cycle.**</span></span>

    -   <span data-ttu-id="b4906-112">Execute o verificador no modo de descoberta e valide os resultados.</span><span class="sxs-lookup"><span data-stu-id="b4906-112">Run the scanner in discovery mode and validate the findings.</span></span>

    -   <span data-ttu-id="b4906-113">Se necessário, otimize as condições e os tipos de informações confidenciais.</span><span class="sxs-lookup"><span data-stu-id="b4906-113">If needed, optimize the conditions and sensitive information types.</span></span>

    -   <span data-ttu-id="b4906-114">Avalie o impacto esperado de aplicar rótulos automaticamente.</span><span class="sxs-lookup"><span data-stu-id="b4906-114">Assess the expected impact of automatically applying labels.</span></span>

3.  <span data-ttu-id="b4906-115">**Execute o verificador da Proteção de Informações do Azure para aplicar rótulos a documentos qualificados**.</span><span class="sxs-lookup"><span data-stu-id="b4906-115">**Run the Azure Information Protection scanner to apply labels to qualifying documents**.</span></span>

4.  <span data-ttu-id="b4906-116">**Para a proteção:**</span><span class="sxs-lookup"><span data-stu-id="b4906-116">**For protection:**</span></span>

    -   <span data-ttu-id="b4906-117">Configure regras de prevenção contra a perda de dados do Exchange para proteger documentos com o rótulo desejado.</span><span class="sxs-lookup"><span data-stu-id="b4906-117">Configure Exchange data loss prevention rules to protect documents with the desired label.</span></span>

    -   <span data-ttu-id="b4906-118">Certifique-se de usar permissões para limitar quem pode acessar os arquivos.</span><span class="sxs-lookup"><span data-stu-id="b4906-118">Be sure to use permissions to limit who can access files.</span></span>

5.  <span data-ttu-id="b4906-119">**Para monitorar, integre os registros do Windows Server com uma ferramenta SIEM.**</span><span class="sxs-lookup"><span data-stu-id="b4906-119">**For monitoring, integrate Windows Server logs with a SIEM tool.**</span></span>

    -   <span data-ttu-id="b4906-p101">Para localizar dados pessoais para solicitações de titulares de dados, use o verificador da Proteção de Informações do Azure. Você também pode configurar a pesquisa do SharePoint Server para rastrear compartilhamentos de arquivos.</span><span class="sxs-lookup"><span data-stu-id="b4906-p101">To find personal data for data subject requests, use Azure Information Protection scanner. You can also configure SharePoint Server search to crawl file shares.</span></span>

<span data-ttu-id="b4906-122">Para mais informações sobre o uso do verificador de Proteção de Informações do Azure para encontrar e rotular dados pessoais, consulte [Implantar a AIP de Verificação](<https://docs.microsoft.com/azure/information-protection/deploy-aip-scanner).</span><span class="sxs-lookup"><span data-stu-id="b4906-122">For more information on using Azure Information Protection scanner to find and label personal data, see [Deploy AIP Scanner](<https://docs.microsoft.com/azure/information-protection/deploy-aip-scanner).</span></span>

<span data-ttu-id="b4906-p102">Confira informações sobre como configurar o verificador para utilizar condições e os tipos de informações confidenciais para prevenção contra perda de dados (DLP) do Office 365 em [Como configurar as condições de classificação automática e recomendada para a Proteção de Informações do Azure](https://docs.microsoft.com/information-protection/deploy-use/configure-policy-classification). Observe que os novos tipos de informações confidenciais do Office 365 não estarão disponíveis imediatamente para uso com o verificador e que tipos de informações confidenciais personalizadas não podem ser usadas com o verificador.</span><span class="sxs-lookup"><span data-stu-id="b4906-p102">For information on configuring the scanner for conditions and using the Office 365 data loss prevention (DLP) sensitive information types, see [How to configure conditions for automatic and recommended classification for Azure Information Protection](https://docs.microsoft.com/information-protection/deploy-use/configure-policy-classification). Note that new Office 365 sensitive information types will not be immediately available to use with the scanner and custom sensitive information types cannot be used with the scanner.</span></span>
