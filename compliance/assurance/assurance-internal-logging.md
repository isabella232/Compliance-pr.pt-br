---
title: Microsoft 365 log interno para Microsoft 365 engenharia
description: Neste artigo, encontre uma explicação de como funciona o log interno para Microsoft 365 Engenharia.
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
ms.openlocfilehash: 71b08509ae920ad88ecfa1566b9a11d640b0534f
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/23/2021
ms.locfileid: "53088590"
---
# <a name="internal-logging-for-microsoft-365-engineering"></a><span data-ttu-id="b5511-103">Log interno para engenharia do Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="b5511-103">Internal logging for Microsoft 365 engineering</span></span>

<span data-ttu-id="b5511-104">Além dos eventos e dados de log disponíveis para clientes, a Microsoft mantém um sistema de coleta de dados de log interno que está disponível para engenheiros Microsoft 365 log.</span><span class="sxs-lookup"><span data-stu-id="b5511-104">In addition to the events and log data available for customers, Microsoft maintains an internal log data collection system that is available to Microsoft 365 engineers.</span></span> <span data-ttu-id="b5511-105">Muitos tipos diferentes de dados de log são carregados de servidores Microsoft 365 para uma solução de monitoramento de segurança proprietária para análise quase em tempo real (NRT) e um serviço interno de computação de big data (Cosmos) para armazenamento a longo prazo.</span><span class="sxs-lookup"><span data-stu-id="b5511-105">Many different types of log data are uploaded from Microsoft 365 servers to a proprietary security monitoring solution for near real-time (NRT) analysis and an internal, big data computing service (Cosmos) for long-term storage.</span></span> <span data-ttu-id="b5511-106">Essa transferência de dados ocorre por meio de uma conexão TLS validada pelo FIPS 140-2 em portas e protocolos aprovados usando uma ferramenta de automação proprietária chamada ODL (carregador de dados Office).</span><span class="sxs-lookup"><span data-stu-id="b5511-106">This data transfer occurs over a FIPS 140-2-validated TLS connection on approved ports and protocols using a proprietary automation tool called the Office Data Loader (ODL).</span></span> <span data-ttu-id="b5511-107">As ferramentas usadas no Microsoft 365 para coletar e processar registros de auditoria não permitem alterações permanentes ou irreversíveis no conteúdo do registro de auditoria original ou na ordem de tempo.</span><span class="sxs-lookup"><span data-stu-id="b5511-107">The tools used in Microsoft 365 to collect and process audit records do not allow permanent or irreversible changes to the original audit record content or time ordering.</span></span>

<span data-ttu-id="b5511-108">As equipes de serviço usam o Cosmos como um repositório centralizado para conduzir uma análise do uso do aplicativo, para medir o desempenho do sistema e operacional e para procurar anormalidades e padrões que possam indicar problemas ou problemas de segurança.</span><span class="sxs-lookup"><span data-stu-id="b5511-108">Service teams use Cosmos as a centralized repository to conduct an analysis of application usage, to measure system and operational performance, and to look for abnormalities and patterns that may indicate problems or security issues.</span></span> <span data-ttu-id="b5511-109">Cada equipe de serviço carrega uma linha de base que inclui:</span><span class="sxs-lookup"><span data-stu-id="b5511-109">Each service team uploads a baseline that includes:</span></span>

- <span data-ttu-id="b5511-110">Logs de eventos</span><span class="sxs-lookup"><span data-stu-id="b5511-110">Event logs</span></span>
- <span data-ttu-id="b5511-111">Logs do AppLocker</span><span class="sxs-lookup"><span data-stu-id="b5511-111">AppLocker logs</span></span>
- <span data-ttu-id="b5511-112">Dados de desempenho</span><span class="sxs-lookup"><span data-stu-id="b5511-112">Performance data</span></span>
- <span data-ttu-id="b5511-113">System Center dados</span><span class="sxs-lookup"><span data-stu-id="b5511-113">System Center data</span></span>
- <span data-ttu-id="b5511-114">Registros de detalhes de chamada</span><span class="sxs-lookup"><span data-stu-id="b5511-114">Call detail records</span></span>
- <span data-ttu-id="b5511-115">Qualidade dos dados de experiência</span><span class="sxs-lookup"><span data-stu-id="b5511-115">Quality of experience data</span></span>
- <span data-ttu-id="b5511-116">Logs do Servidor Web do IIS</span><span class="sxs-lookup"><span data-stu-id="b5511-116">IIS Web Server logs</span></span>
- <span data-ttu-id="b5511-117">SQL Server logs</span><span class="sxs-lookup"><span data-stu-id="b5511-117">SQL Server logs</span></span>
- <span data-ttu-id="b5511-118">Dados de syslog</span><span class="sxs-lookup"><span data-stu-id="b5511-118">Syslog data</span></span>
- <span data-ttu-id="b5511-119">Logs de auditoria de segurança</span><span class="sxs-lookup"><span data-stu-id="b5511-119">Security audit logs</span></span>

<span data-ttu-id="b5511-120">Antes de carregar, o aplicativo ODL usa um serviço de limpeza para remover todos os campos que contenham dados do cliente, como informações de locatário e informações de identificação do usuário final, e substituir esses campos por um valor de hash.</span><span class="sxs-lookup"><span data-stu-id="b5511-120">Prior to uploading, the ODL application uses a scrubbing service to remove any fields that contain customer data, such as tenant information and end-user identifiable information, and replace those fields with a hash value.</span></span> <span data-ttu-id="b5511-121">Os logs limpos são carregados para Cosmos e para a solução de monitoramento de segurança NRT que analisa os logs para possíveis eventos de segurança e indicadores de desempenho.</span><span class="sxs-lookup"><span data-stu-id="b5511-121">The scrubbed logs are uploaded to Cosmos and to the NRT security monitoring solution that analyzes the logs for potential security events and performance indicators.</span></span> <span data-ttu-id="b5511-122">O período de retenção de dados de log de auditoria no Cosmos é determinado pelas equipes de serviço; a maioria dos dados de log de auditoria é mantida por 90 dias ou mais para dar suporte a investigações de incidentes de segurança e para atender aos requisitos de retenção regulamentar.</span><span class="sxs-lookup"><span data-stu-id="b5511-122">The period of audit log data retention in Cosmos is determined by the service teams; most audit log data is retained for 90 days or longer to support security incident investigations and to meet regulatory retention requirements.</span></span>

<span data-ttu-id="b5511-123">O acesso Microsoft 365 dados armazenados no Cosmos é restrito a funcionários autorizados.</span><span class="sxs-lookup"><span data-stu-id="b5511-123">Access to Microsoft 365 data stored in Cosmos is restricted to authorized personnel.</span></span> <span data-ttu-id="b5511-124">A Microsoft restringe o gerenciamento de logs de auditoria a um subconjunto limitado de membros da Equipe de Segurança responsáveis pela funcionalidade de auditoria.</span><span class="sxs-lookup"><span data-stu-id="b5511-124">Microsoft restricts the management of audit logs to a limited subset of Security Team members responsible for audit functionality.</span></span> <span data-ttu-id="b5511-125">A Equipe de Segurança não tem acesso administrativo permanente Cosmos e todas as alterações são gravadas e auditadas.</span><span class="sxs-lookup"><span data-stu-id="b5511-125">The Security Team does not have standing administrative access to Cosmos, and all changes are recorded and audited.</span></span>

<span data-ttu-id="b5511-126">Após a análise de NRT, cada equipe de serviço pode usar ferramentas de análise e painéis para correlação de dados, consultas interativas e análise de dados.</span><span class="sxs-lookup"><span data-stu-id="b5511-126">After NRT analysis, each service team can use analysis tools and dashboards for data correlation, interactive queries, and data analytics.</span></span> <span data-ttu-id="b5511-127">Esses relatórios são usados para monitorar e melhorar o desempenho geral do serviço.</span><span class="sxs-lookup"><span data-stu-id="b5511-127">These reports are used to monitor and improve the overall performance of the service.</span></span>
