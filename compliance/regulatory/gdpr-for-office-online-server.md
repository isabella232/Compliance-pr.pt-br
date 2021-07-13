---
title: RGPD para Servidor do Office Online e para o Servidor do Office Web Apps
description: Neste artigo, você aprenderá sobre como resolver os requisitos do RGPD para o servidor do Office Online e para o Office Web Apps.
f1.keywords:
- NOCSH
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
ms.collection: MS-Compliance
ms.custom:
- seo-marvel-mar2020
titleSuffix: Microsoft GDPR
hideEdit: true
ms.openlocfilehash: 6e088f64d6b0113640100269b29ef31737befe92
ms.sourcegitcommit: 8bf2602d56eedee4447ddb374ef95b0587f254e7
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/12/2021
ms.locfileid: "53377948"
---
# <a name="gdpr-for-office-web-apps-server-and-office-online-server"></a><span data-ttu-id="79379-103">RGPD para Servidor do Office Web Apps e Servidor do Office Online</span><span class="sxs-lookup"><span data-stu-id="79379-103">GDPR for Office Web Apps Server and Office Online Server</span></span>

<span data-ttu-id="79379-p101">Dados de telemetria do Servidor do Office Web Apps e do Servidor do Office Online são armazenados em forma de logs ULS. Você pode usar [ULSViewer](https://www.microsoft.com/download/details.aspx?id=44020) para exibir os logs ULS do seu locatário local.</span><span class="sxs-lookup"><span data-stu-id="79379-p101">Office Online Server and Office Web Apps Server telemetry data is stored in the form of ULS logs. You can use [ULS Viewer](https://www.microsoft.com/download/details.aspx?id=44020) to view ULS logs from your on-premises tenant.</span></span>

<span data-ttu-id="79379-p102">Todas as linhas de log contêm uma CorrelationID. Linhas de log relacionadas compartilham a mesma CorrelationID. Cada CorrelationID está vinculada a uma SessionID e uma SessionID pode estar relacionada a muitas CorrelationIDs. Cada SessionID pode estar relacionada a uma única UserID, embora algumas sessões possam ser anônimas e, portanto, não estarem associadas a uma UserID. Para determinar quais dados estão associados a um usuário específico, é possível mapear de uma única UserID para as SessionIDs associadas ao usuário, das SessionIDs para as CorrelationIDs associadas, e dessas CorrelationIDs para todos os logs nessas correlações. Confira o diagrama abaixo para verificar a relação entre as diferentes IDs.</span><span class="sxs-lookup"><span data-stu-id="79379-p102">Every log line contains a CorrelationID. Related log lines share the same CorrelationID. Each CorrelationID is tied to a single SessionID, and one SessionID may be related to many CorrelationIDs. Each SessionID may be related to a single UserID, although some sessions can be anonymous and therefore not have an associated UserID. In order to determine what data is associated with a particular user, it is therefore possible to map from a single UserID to the SessionIDs associated with that user, from those SessionIDs to the associated CorrelationIDs, and from those CorrelationIDs to all the logs in those correlations. See the below diagram for the relationship between the different IDs.</span></span>

![Fluxograma mostrando a relação entre SessionIDs e CorrelationIds](../media/gdpr-for-office-online-server-image1.jpg)

## <a name="gathering-logs"></a><span data-ttu-id="79379-113">Coletar logs</span><span class="sxs-lookup"><span data-stu-id="79379-113">Gathering Logs</span></span>

<span data-ttu-id="79379-p103">Para reunir todos os logs associados ao UserID 1, por exemplo, a primeira etapa seria reunir todas as sessões associadas ao UserID 1 (ou seja, SessionID 1 e SessionID2). A próxima etapa seria reunir todas as correlações associadas com SessionID 1 (ou seja, CorrelationIDs 1, 2 e 3) e com SessionID 2 (ou seja, CorrelationID 4). Finalmente, reúna todos os logs associados a cada uma das correlações na lista.</span><span class="sxs-lookup"><span data-stu-id="79379-p103">In order to gather all logs associated with UserID 1, for example, the first step would be to gather all sessions associated with UserID 1 (that is, SessionID 1 and SessionID2). The next step would be to gather all correlations associated with SessionID 1 (that is, CorrelationIDs 1, 2, and 3) and with SessionID 2 (that is, CorrelationID 4). Finally, gather all logs associated with each of the correlations in the list.</span></span>

1. <span data-ttu-id="79379-117">Iniciar o ULSViewer</span><span class="sxs-lookup"><span data-stu-id="79379-117">Launch UlsViewer</span></span>

2. <span data-ttu-id="79379-118">Abra o log ULS correspondente ao período de tempo pretendido; logs ULS são armazenados em %PROGRAMDATA%\\Microsoft\\OfficeWebApps\\Data\\Logs\\ULS</span><span class="sxs-lookup"><span data-stu-id="79379-118">Open up the uls log corresponding to the intended timeframe; ULS logs are stored in %PROGRAMDATA%\\Microsoft\\OfficeWebApps\\Data\\Logs\\ULS</span></span>

3. <span data-ttu-id="79379-119">Editar | Modificar Filtro</span><span class="sxs-lookup"><span data-stu-id="79379-119">Edit | Modify Filter</span></span>

4. <span data-ttu-id="79379-120">Aplique um filtro que seja:</span><span class="sxs-lookup"><span data-stu-id="79379-120">Apply a filter that is:</span></span>

    - <span data-ttu-id="79379-121">EventID igual a apr3y</span><span class="sxs-lookup"><span data-stu-id="79379-121">EventID equals apr3y</span></span>

      <span data-ttu-id="79379-122">Ou</span><span class="sxs-lookup"><span data-stu-id="79379-122">Or</span></span>

    - <span data-ttu-id="79379-123">EventID igual a bp2d6</span><span class="sxs-lookup"><span data-stu-id="79379-123">EventID equals bp2d6</span></span>

5. <span data-ttu-id="79379-124">UserIDs com hash estarão na mensagem de qualquer um desses dois eventos</span><span class="sxs-lookup"><span data-stu-id="79379-124">Hashed UserIds will be in the Message of either one of these two events</span></span>

6. <span data-ttu-id="79379-125">Para apr3y, a mensagem conterá um valor de UserID e um valor de PUID</span><span class="sxs-lookup"><span data-stu-id="79379-125">For apr3y, the Message will contain a UserID value and a PUID value</span></span>

7. <span data-ttu-id="79379-p104">Para bp2d6, a mensagem conterá uma grande quantidade de informações. O campo de valor LoggableUserId é a UserID com hash.</span><span class="sxs-lookup"><span data-stu-id="79379-p104">For bp2d6, the Message will contain quite a bit of information. The LoggableUserId Value field is the hashed UserID.</span></span>

8. <span data-ttu-id="79379-128">Depois de obter a UserID com hash dessas duas marcas, o valor de WacSessionId dessa linha no ULSViewer conterá a WacSessionId associada ao usuário</span><span class="sxs-lookup"><span data-stu-id="79379-128">Once the hashed UserId is obtained from either of these two tags, the WacSessionId value of that row in ULSViewer will contain the WacSessionId associated with that user</span></span>

9. <span data-ttu-id="79379-129">Colete todos os valores de WacSessionId associados com usuários em questão</span><span class="sxs-lookup"><span data-stu-id="79379-129">Collect all of the WacSessionId values associated with the user in question</span></span>

10. <span data-ttu-id="79379-130">Filtre todos EventId iguais a "xmnv", Message igual a "UserSessionId =\<WacSessionId\>WacSessionId" para a primeira WacSessionId na lista (substituindo a parte \<WacSessionId\> do filtro com sua WacSessionId)</span><span class="sxs-lookup"><span data-stu-id="79379-130">Filter for all EventId equals "xmnv", Message equals "UserSessionId=\<WacSessionId\>" for the first WacSessionId in the list (replacing the \<WacSessionId\> part of the filter with your WacSessionId)</span></span>

11. <span data-ttu-id="79379-131">Colete todos os valores de correlação que correspondam a essa WacSessionId</span><span class="sxs-lookup"><span data-stu-id="79379-131">Collect all values of Correlation that match that WacSessionId</span></span>

12. <span data-ttu-id="79379-132">Repita as etapas 10 e 11 para todos os valores de WacSessionId em sua lista de usuários em questão</span><span class="sxs-lookup"><span data-stu-id="79379-132">Repeat steps 10-11 for all values of WacSessionId in your list for the user in question</span></span>

13. <span data-ttu-id="79379-133">Filtrar para todos os valores de correlação iguais à primeira correlação da sua lista</span><span class="sxs-lookup"><span data-stu-id="79379-133">Filter for all Correlation equals the first Correlation in your list</span></span>

14. <span data-ttu-id="79379-134">Colete todos os logs correspondentes a essa correlação</span><span class="sxs-lookup"><span data-stu-id="79379-134">Collect all logs matching that Correlation</span></span>

15. <span data-ttu-id="79379-135">Repita as etapas 13 e 14 para todos os valores de correlação em sua lista de usuários em questão</span><span class="sxs-lookup"><span data-stu-id="79379-135">Repeat steps 13-14 for all values of Correlation in your list for the user in question</span></span>

## <a name="types-of-data"></a><span data-ttu-id="79379-136">Tipos de dados</span><span class="sxs-lookup"><span data-stu-id="79379-136">Types of Data</span></span>

<span data-ttu-id="79379-p105">Os logs do Office contêm vários tipos diferentes de dados. A seguir estão exemplos dos dados que os registros ULS podem conter:</span><span class="sxs-lookup"><span data-stu-id="79379-p105">Office logs contain various different types of data. The following are examples of the data that ULS logs may contain:</span></span>

- <span data-ttu-id="79379-139">Códigos de erro para problemas encontrados durante o uso do produto</span><span class="sxs-lookup"><span data-stu-id="79379-139">Error codes for issues encountered during use of the product</span></span>

- <span data-ttu-id="79379-140">Cliques de botão e outros dados sobre o uso do aplicativo</span><span class="sxs-lookup"><span data-stu-id="79379-140">Button clicks and other pieces of data about app usage</span></span>

- <span data-ttu-id="79379-141">Dados de desempenho do aplicativo e/ou recursos específicos do aplicativo</span><span class="sxs-lookup"><span data-stu-id="79379-141">Performance data about the app and/or particular features within the app</span></span>

- <span data-ttu-id="79379-142">Informações gerais de localização sobre onde está o computador do usuário (por exemplo, país/região, estado e cidade, derivado do endereço de IP), mas não a localização geográfica precisa.</span><span class="sxs-lookup"><span data-stu-id="79379-142">General location information about where the user's computer is (for example, country/region, state, and city, derived from the IP address), but not precise geo location.</span></span>

- <span data-ttu-id="79379-143">Metadados básicos sobre o navegador, por exemplo, nome e versão do navegador e o computador, por exemplo, tipo e versão do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="79379-143">Basic metadata about the browser, for example, browser name and version, and the computer, for example, OS type and version</span></span>

- <span data-ttu-id="79379-144">Mensagens de erro do host do documento (por exemplo, Microsoft OneDrive, Microsoft Office SharePoint Online e Microsoft Exchange)</span><span class="sxs-lookup"><span data-stu-id="79379-144">Error messages from the document host (for example, OneDrive, SharePoint, Exchange)</span></span>

- <span data-ttu-id="79379-145">Informações sobre processos internos do aplicativo não relacionados a ações do usuário</span><span class="sxs-lookup"><span data-stu-id="79379-145">Information about processes internal to the app, unrelated to any action the user has taken</span></span>
