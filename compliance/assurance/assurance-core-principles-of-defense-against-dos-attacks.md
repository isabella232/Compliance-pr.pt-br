---
title: Princípios básicos da Microsoft 365 sobre defesa contra ataques de negação de serviço
description: Como a Microsoft utiliza os princípios fundamentais de absorção, detecção e atenuação em sua defesa contra ataques de negação de serviço (DoS).
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
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 56ab287371f012fdf1d31304ddc8afe8f4334658
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/30/2020
ms.locfileid: "49505836"
---
# <a name="core-principles-of-defense-against-denial-of-service-attacks"></a><span data-ttu-id="c0f38-103">Princípios básicos de defesa contra ataques de negação de serviço</span><span class="sxs-lookup"><span data-stu-id="c0f38-103">Core principles of defense against denial-of-service attacks</span></span>

<span data-ttu-id="c0f38-104">Os três princípios fundamentais ao se defender contra ataques de DoS baseados em rede são absorção, detecção e mitigação.</span><span class="sxs-lookup"><span data-stu-id="c0f38-104">The three core principles when defending against network-based DoS attacks are Absorption, Detection, and Mitigation.</span></span> <span data-ttu-id="c0f38-105">A absorção ocorre antes da detecção e a detecção ocorre antes da redução.</span><span class="sxs-lookup"><span data-stu-id="c0f38-105">Absorption happens before detection, and detection happens before mitigation.</span></span> <span data-ttu-id="c0f38-106">O absorção é a melhor defesa contra um ataque de DoS.</span><span class="sxs-lookup"><span data-stu-id="c0f38-106">Absorption is the best defense against a DoS attack.</span></span> <span data-ttu-id="c0f38-107">Se não for possível detectar o ataque, não será possível diminuí-lo.</span><span class="sxs-lookup"><span data-stu-id="c0f38-107">If the attack can't be detected, it can't be mitigated.</span></span> <span data-ttu-id="c0f38-108">Mas, se mesmo o menor ataque de DoS não puder ser absorvido, os serviços não ficarão sobreviventes o suficiente para que o ataque seja detectado.</span><span class="sxs-lookup"><span data-stu-id="c0f38-108">But if even the smallest DoS attack can't be absorbed, then services aren't going to survive long enough for the attack to be detected.</span></span>

<span data-ttu-id="c0f38-109">Não é economicamente viável para a maioria das organizações comprar capacidade em excesso para absorver ataques de DoS, já que isso requer um investimento considerável em tecnologia e habilidades técnicas.</span><span class="sxs-lookup"><span data-stu-id="c0f38-109">It is not economically feasible for most organizations to purchase excess capacity to absorb DoS attacks, as this requires a considerable investment in technology and technical skills.</span></span> <span data-ttu-id="c0f38-110">Isso realça um dos benefícios de segurança do uso dos serviços de nuvem da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c0f38-110">This highlights one of the security benefits of using Microsoft cloud services.</span></span> <span data-ttu-id="c0f38-111">A escalabilidade dos serviços Microsoft oferece uma forte proteção de rede para os clientes da nuvem de forma econômica.</span><span class="sxs-lookup"><span data-stu-id="c0f38-111">The sheer scale of Microsoft services provides strong network protection to cloud customers in a cost-effective manner.</span></span> <span data-ttu-id="c0f38-112">Mas mesmo em uma escala grande, deve haver um equilíbrio entre absorção, detecção e mitigação.</span><span class="sxs-lookup"><span data-stu-id="c0f38-112">But even at a large scale, there must be a balance between absorption, detection, and mitigation.</span></span> <span data-ttu-id="c0f38-113">Para encontrar esse saldo, a Microsoft estuda as taxas de crescimento de ataques para estimar a quantidade de necessidade de absorver a Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c0f38-113">To find that balance, Microsoft studies attack growth rates to estimate how much Microsoft needs to absorb.</span></span>

<span data-ttu-id="c0f38-114">A detecção é um jogo de gato e mouse.</span><span class="sxs-lookup"><span data-stu-id="c0f38-114">Detection is a cat-and-mouse game.</span></span> <span data-ttu-id="c0f38-115">Você deve procurar constantemente por novas maneiras pelas quais as pessoas são atacadas e tentar derrotar seus sistemas.</span><span class="sxs-lookup"><span data-stu-id="c0f38-115">You must constantly look for new ways people are attack and try to defeat your systems.</span></span> <span data-ttu-id="c0f38-116">Detect-> mitigate-> Detect-> mitigate, etc., é um estado permanente e persistente que continua indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="c0f38-116">Detect -> Mitigate -> Detect -> Mitigate, etc., is a perpetual, persistent state that continues indefinitely.</span></span>

## <a name="defending-against-dos-attacks"></a><span data-ttu-id="c0f38-117">Como se proteger contra ataques de DoS</span><span class="sxs-lookup"><span data-stu-id="c0f38-117">Defending Against DoS Attacks</span></span>

<span data-ttu-id="c0f38-118">Para se defender com êxito contra ataques de DoS, a detecção antecipada é essencial.</span><span class="sxs-lookup"><span data-stu-id="c0f38-118">To successfully defend against a DoS attack, early detection is essential.</span></span> <span data-ttu-id="c0f38-119">Ao detectar um ataque antes que o sistema fique sobrecarregado, os defensores podem executar um plano de resposta.</span><span class="sxs-lookup"><span data-stu-id="c0f38-119">By detecting an attack before the system is overwhelmed, defenders can execute a response plan.</span></span>

<span data-ttu-id="c0f38-120">A fórmula a seguir ajuda a aproximar o tempo de impacto de um ataque de DoS:</span><span class="sxs-lookup"><span data-stu-id="c0f38-120">The following formula helps approximate the time to impact of a DoS attack:</span></span>

   <span data-ttu-id="c0f38-121">**Capacidade máxima (em bytes/seg)/taxa de crescimento (em bytes/seg) = tempo de impacto (em segundos)**</span><span class="sxs-lookup"><span data-stu-id="c0f38-121">**Maximum Capacity (in bytes/sec) / Growth Rate (in bytes/sec) = Time to Impact (in sec)**</span></span>

<span data-ttu-id="c0f38-122">Se o tempo de detecção ocorrer após o tempo de impacto, é provável que o ataque de DoS seja bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="c0f38-122">If the time-to-detection occurs after time-to-impact, it is likely the DoS attack will be successful.</span></span> <span data-ttu-id="c0f38-123">Se o tempo de detecção ocorrer antes do tempo de impacto, os serviços atacados deverão permanecer online e acessíveis se as estratégias de mitigação forem usadas.</span><span class="sxs-lookup"><span data-stu-id="c0f38-123">If the time-to-detection occurs before time-to-impact, the attacked services should remain online and accessible if mitigation strategies are used.</span></span> <span data-ttu-id="c0f38-124">Portanto, há apenas duas coisas que podem ser realizadas para se defender contra ataques de DoS:</span><span class="sxs-lookup"><span data-stu-id="c0f38-124">Thus, there are only two things that can be done to defend against DoS attacks:</span></span>

- <span data-ttu-id="c0f38-125">Aumente a capacidade para elevar o teto da capacidade máxima (que, por sua vez, fornece mais tempo para detectar um ataque); ou</span><span class="sxs-lookup"><span data-stu-id="c0f38-125">Increase capacity to raise the ceiling of maximum capacity (which in turn provides more time to detect an attack); or</span></span>
- <span data-ttu-id="c0f38-126">Diminuir o tempo para detectar.</span><span class="sxs-lookup"><span data-stu-id="c0f38-126">Decrease the time to detect.</span></span>

<span data-ttu-id="c0f38-127">O aumento da capacidade tem um impacto fiscal direto.</span><span class="sxs-lookup"><span data-stu-id="c0f38-127">Increasing capacity has a direct fiscal impact.</span></span> <span data-ttu-id="c0f38-128">A Microsoft recomenda que os clientes desenvolvam pelo menos a capacidade básica de absorção para garantir que eles possam sobreviver a algum nível de ataque de DoS.</span><span class="sxs-lookup"><span data-stu-id="c0f38-128">Microsoft recommends that customers develop at least basic absorption capacity to ensure that they can survive some level of DoS attack.</span></span> <span data-ttu-id="c0f38-129">A capacidade de absorção real varia de cliente para cliente, uma vez que cada cliente tem seus próprios limites de exposição, risco e outlay financeiro.</span><span class="sxs-lookup"><span data-stu-id="c0f38-129">The actual absorption capacity varies from customer to customer, as each customer has their own thresholds for exposure, risk, and financial outlay.</span></span> <span data-ttu-id="c0f38-130">Por motivos econômicos, os investimentos em pesquisa e tempo para reduzir o tempo de detecção costumam ser a defesa mais econômica.</span><span class="sxs-lookup"><span data-stu-id="c0f38-130">For economic reasons, investments in research and time for ways to decrease time-to-detection are usually the most cost-effective defense.</span></span>
