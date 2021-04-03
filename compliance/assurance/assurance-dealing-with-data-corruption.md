---
title: Microsoft 365 Lidando com corrupção de dados
description: Este artigo explica a corrupção de dados no Microsoft 365 e os esforços da Microsoft para impedir e recuperar dados.
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
ms.openlocfilehash: 9e9f0951f7e349cc70bc96bb6a2d62275848cf04
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497592"
---
# <a name="dealing-with-data-corruption-in-microsoft-365"></a><span data-ttu-id="6c7e7-103">Lidar com corrupção de dados no Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="6c7e7-103">Dealing with data corruption in Microsoft 365</span></span>

<span data-ttu-id="6c7e7-104">Um dos aspectos desafiadores da execução de um serviço de nuvem em grande escala é como lidar com a corrupção de dados, dado o grande volume de dados e sistemas independentes.</span><span class="sxs-lookup"><span data-stu-id="6c7e7-104">One of the challenging aspects of running a large-scale cloud service is how to handle data corruption, given the large volume of data and independent systems.</span></span> <span data-ttu-id="6c7e7-105">A corrupção de dados pode ser causada por:</span><span class="sxs-lookup"><span data-stu-id="6c7e7-105">Data corruption can be caused by:</span></span>

- <span data-ttu-id="6c7e7-106">Bugs de aplicativo ou infraestrutura, corrompendo parte ou todo o estado do aplicativo</span><span class="sxs-lookup"><span data-stu-id="6c7e7-106">Application or infrastructure bugs, corrupting some or all of the application state</span></span>
- <span data-ttu-id="6c7e7-107">Problemas de hardware que resultam em perda de dados ou incapacidade de ler dados</span><span class="sxs-lookup"><span data-stu-id="6c7e7-107">Hardware issues that result in lost data or an inability to read data</span></span>
- <span data-ttu-id="6c7e7-108">Erros operacionais humanos</span><span class="sxs-lookup"><span data-stu-id="6c7e7-108">Human operational errors</span></span>
- <span data-ttu-id="6c7e7-109">Hackers mal-intencionados e funcionários insatisfeitos</span><span class="sxs-lookup"><span data-stu-id="6c7e7-109">Malicious hackers and disgruntled employees</span></span>
- <span data-ttu-id="6c7e7-110">Incidentes em serviços externos que resultam em alguma perda de dados</span><span class="sxs-lookup"><span data-stu-id="6c7e7-110">Incidents in external services that result in some loss of data</span></span>

<span data-ttu-id="6c7e7-111">Como uma resiliência maior na integridade de dados significa menos incidentes de corrupção de dados, a Microsoft criou mecanismos de proteção do Microsoft 365 para impedir que a corrupção aconteça, bem como sistemas e processos que nos permitem recuperar dados se isso acontecer.</span><span class="sxs-lookup"><span data-stu-id="6c7e7-111">Because greater resiliency in data integrity means fewer data corruption incidents, Microsoft has built into Microsoft 365 protection mechanisms to prevent corruption from happening, as well as systems and processes that enable us to recover data if it does.</span></span> <span data-ttu-id="6c7e7-112">Verificações e processos existem dentro dos vários estágios do processo de lançamento de engenharia para aumentar a resiliência contra a corrupção de dados, incluindo:</span><span class="sxs-lookup"><span data-stu-id="6c7e7-112">Checks and processes exist within the various stages of the engineering release process to increase resiliency against data corruption, including:</span></span>

- <span data-ttu-id="6c7e7-113">Design do sistema</span><span class="sxs-lookup"><span data-stu-id="6c7e7-113">System Design</span></span>
- <span data-ttu-id="6c7e7-114">Organização e estrutura de códigos</span><span class="sxs-lookup"><span data-stu-id="6c7e7-114">Code organization and structure</span></span>
- <span data-ttu-id="6c7e7-115">Revisão de código</span><span class="sxs-lookup"><span data-stu-id="6c7e7-115">Code review</span></span>
- <span data-ttu-id="6c7e7-116">Testes de unidade, testes de integração e testes de sistema</span><span class="sxs-lookup"><span data-stu-id="6c7e7-116">Unit tests, integration tests, and system tests</span></span>
- <span data-ttu-id="6c7e7-117">Testes/portas de fio de viagem</span><span class="sxs-lookup"><span data-stu-id="6c7e7-117">Trip wires tests/gates</span></span>

<span data-ttu-id="6c7e7-118">Em ambientes de produção do Microsoft 365, a replicação de pares entre datacenters garante que sempre haja várias cópias ao vivo de todos os dados.</span><span class="sxs-lookup"><span data-stu-id="6c7e7-118">Within Microsoft 365 production environments, peer replication between datacenters ensures that there are always multiple live copies of any data.</span></span> <span data-ttu-id="6c7e7-119">As imagens e scripts padrão são usados para recuperar servidores perdidos e os dados replicados são usados para restaurar dados do cliente.</span><span class="sxs-lookup"><span data-stu-id="6c7e7-119">Standard images and scripts are used to recover lost servers, and replicated data is used to restore customer data.</span></span> <span data-ttu-id="6c7e7-120">Devido às verificações e processos internos de resiliência de dados, a Microsoft mantém backups somente da documentação do sistema de informações do Microsoft 365 (incluindo documentação relacionada à segurança), usando a replicação interna no SharePoint Online e nossa ferramenta de repositório de código interno, Source Depot.</span><span class="sxs-lookup"><span data-stu-id="6c7e7-120">Because of the built-in data resiliency checks and processes, Microsoft maintains backups only of Microsoft 365 information system documentation (including security-related documentation), using built-in replication in SharePoint Online and our internal code repository tool, Source Depot.</span></span> <span data-ttu-id="6c7e7-121">A documentação do sistema é armazenada no SharePoint Online, e o Source Depot contém imagens do sistema e do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6c7e7-121">System documentation is stored in SharePoint Online, and Source Depot contains system and application images.</span></span> <span data-ttu-id="6c7e7-122">O SharePoint Online e o Source Depot usam o versioning e são replicados em tempo real.</span><span class="sxs-lookup"><span data-stu-id="6c7e7-122">Both SharePoint Online and Source Depot use versioning and are replicated in near real time.</span></span>
