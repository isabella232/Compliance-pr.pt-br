---
title: 'Gerenciamento de incidentes de segurança da Microsoft: atividade pós-incidente'
description: Este artigo fornece uma visão geral do processo de atividade pós-incidente de gerenciamento de incidentes de segurança nos serviços online da Microsoft.
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
f1.keywords:
- NOCSH
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 965c7d6d0d469b9eea981252805bda598c92a4c8
ms.sourcegitcommit: 8bf2602d56eedee4447ddb374ef95b0587f254e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/12/2021
ms.locfileid: "53377528"
---
# <a name="microsoft-security-incident-management-post-incident-activity"></a><span data-ttu-id="af147-103">Gerenciamento de incidentes de segurança da Microsoft: atividade pós-incidente</span><span class="sxs-lookup"><span data-stu-id="af147-103">Microsoft security incident management: Post-incident activity</span></span>

## <a name="postmortem"></a><span data-ttu-id="af147-104">Post-mortem</span><span class="sxs-lookup"><span data-stu-id="af147-104">Postmortem</span></span>

<span data-ttu-id="af147-105">Alguns incidentes de segurança, especialmente aqueles incidentes que estão afetando o cliente ou resultando em uma violação de dados, estão sujeitos a um incidente completo pós-morte.</span><span class="sxs-lookup"><span data-stu-id="af147-105">Some security incidents, especially those incidents that are customer impacting or result in a data breach, are subject to a full incident postmortem.</span></span> <span data-ttu-id="af147-106">A equipe de resposta de segurança conduz uma post-morte detalhada com todas as partes envolvidas na resposta a incidentes de segurança:</span><span class="sxs-lookup"><span data-stu-id="af147-106">The security response team conducts a detailed postmortem with all the parties involved in security incident response to:</span></span>

- <span data-ttu-id="af147-107">Documente a sequência de eventos que causaram o incidente.</span><span class="sxs-lookup"><span data-stu-id="af147-107">Document the sequence of events that caused the incident.</span></span>
- <span data-ttu-id="af147-108">Crie um resumo técnico do incidente como suportado pelas evidências que incluem os atores envolvidos na violação (se conhecido).</span><span class="sxs-lookup"><span data-stu-id="af147-108">Create a technical summary of the incident as supported by the evidence that includes the actors involved in the breach (if known).</span></span> <span data-ttu-id="af147-109">Este resumo incluirá como a resposta foi executada e outros pontos importantes.</span><span class="sxs-lookup"><span data-stu-id="af147-109">This summary will include how the response was executed and other key takeaways.</span></span>
- <span data-ttu-id="af147-110">Identifique erros técnicos, falhas de procedimento, erros manuais, falhas de processo e falhas de comunicação e/ou quaisquer vetores de ataque desconhecidos anteriormente identificados durante a resposta a incidentes de segurança.</span><span class="sxs-lookup"><span data-stu-id="af147-110">Identify technical lapses, procedural failures, manual errors, process flaws, and communication glitches, and/or any previously unknown attack vectors that were identified during the security incident response.</span></span>

<span data-ttu-id="af147-111">A postagem pós-morte influenciará diretamente o aperfeiçoamento do serviço online da Microsoft, os processos operacionais e a documentação definindo novas prioridades no ciclo de desenvolvimento de engenharia de serviços online da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="af147-111">The postmortem will directly influence Microsoft online service improvement, operational processes, and documentation by setting new priorities in the Microsoft online services engineering development cycle.</span></span>

## <a name="documentation"></a><span data-ttu-id="af147-112">Documentação</span><span class="sxs-lookup"><span data-stu-id="af147-112">Documentation</span></span>

<span data-ttu-id="af147-113">Todas as principais descobertas técnicas no processo pós-morte são capturadas em um relatório e investimentos de serviço ou correções na forma de bugs ou solicitações de alteração de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="af147-113">All key technical findings in the postmortem process are captured in a report and service investments or fixes in the form of bugs or development change requests.</span></span> <span data-ttu-id="af147-114">Essas descobertas são acompanhadas com as equipes de engenharia apropriadas.</span><span class="sxs-lookup"><span data-stu-id="af147-114">These findings are followed-up with the appropriate engineering teams.</span></span> <span data-ttu-id="af147-115">Para falhas de processo e problemas organizacionais entre organizações, os problemas são documentados no banco de dados da equipe de resposta de segurança e acompanhados com os grupos apropriados para lidar com eles.</span><span class="sxs-lookup"><span data-stu-id="af147-115">For process failures and cross-organizational issues, issues are documented in the security response team's database and followed-up with the appropriate groups to address them.</span></span>

## <a name="process-improvement"></a><span data-ttu-id="af147-116">Melhoria do processo</span><span class="sxs-lookup"><span data-stu-id="af147-116">Process improvement</span></span>

<span data-ttu-id="af147-117">Responder a um incidente de segurança nos serviços online da Microsoft envolve a coordenação com vários grupos espalhados por diferentes organizações dentro da Microsoft e, potencialmente, até mesmo organizações externas apropriadas, como a aplicação da lei.</span><span class="sxs-lookup"><span data-stu-id="af147-117">Responding to a security incident in Microsoft online services involves coordination with multiple groups spread across different organizations within Microsoft, and potentially even appropriate external organizations such as law enforcement.</span></span> <span data-ttu-id="af147-118">Sabemos que é fundamental avaliar nossas respostas após cada incidente de segurança para suficiência e conclusão.</span><span class="sxs-lookup"><span data-stu-id="af147-118">We know that it is critical to evaluate our responses after every security incident for both sufficiency and completeness.</span></span> <span data-ttu-id="af147-119">Para quaisquer melhorias ou alterações identificadas, a equipe de resposta de segurança avalia as sugestões em consulta com as equipes e partes interessadas apropriadas e, quando apropriado, as incorpora em procedimentos operacionais padrão.</span><span class="sxs-lookup"><span data-stu-id="af147-119">For any identified improvements or changes, the security response team evaluates the suggestions in consultation with the appropriate teams and stakeholders, and where appropriate incorporates them into standard operating procedures.</span></span> <span data-ttu-id="af147-120">Todas as alterações, bugs ou melhorias de serviço necessárias identificadas durante a resposta a incidentes de segurança ou atividades pós-morte são registradas e rastreadas em um banco de dados de engenharia interno da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="af147-120">All required changes, bugs, or service improvements identified during the security incident response or postmortem activity are logged and tracked in an internal Microsoft engineering database.</span></span> <span data-ttu-id="af147-121">Todos os possíveis bugs ou recursos são atribuídos ao proprietário apropriado.</span><span class="sxs-lookup"><span data-stu-id="af147-121">All potential bugs or features are assigned to the appropriate owner.</span></span> <span data-ttu-id="af147-122">A equipe de resposta de segurança da Microsoft revisa todas as entradas até que o problema seja resolvido.</span><span class="sxs-lookup"><span data-stu-id="af147-122">The Microsoft security response team reviews all entries until the issue is resolved.</span></span>

## <a name="related-articles"></a><span data-ttu-id="af147-123">Artigos relacionados</span><span class="sxs-lookup"><span data-stu-id="af147-123">Related articles</span></span>

- [<span data-ttu-id="af147-124">Gerenciamento de incidentes de segurança da Microsoft</span><span class="sxs-lookup"><span data-stu-id="af147-124">Microsoft security incident management</span></span>](assurance-security-incident-management.md)
- [<span data-ttu-id="af147-125">Gerenciamento de incidentes de segurança da Microsoft: Preparação</span><span class="sxs-lookup"><span data-stu-id="af147-125">Microsoft security incident management: Preparation</span></span>](assurance-sim-preparation.md)
- [<span data-ttu-id="af147-126">Gerenciamento de incidentes de segurança da Microsoft: Detecção e análise</span><span class="sxs-lookup"><span data-stu-id="af147-126">Microsoft security incident management: Detection and analysis</span></span>](assurance-sim-detection-analysis.md)
- [<span data-ttu-id="af147-127">Gerenciamento de incidentes de segurança da Microsoft: contenção, erradicação e recuperação</span><span class="sxs-lookup"><span data-stu-id="af147-127">Microsoft security incident management: Containment, eradication, and recovery</span></span>](assurance-sim-containment-eradication-recovery.md)
- [<span data-ttu-id="af147-128">Como registrar um tíquete de suporte a eventos de segurança</span><span class="sxs-lookup"><span data-stu-id="af147-128">How to Log a Security Event Support Ticket</span></span>](/azure/security/fundamentals/event-support-ticket)
- [<span data-ttu-id="af147-129">Notificação de Violação do Azure e do Dynamics 365 no GDPR</span><span class="sxs-lookup"><span data-stu-id="af147-129">Azure and Dynamics 365 breach notification under the GDPR</span></span>](/compliance/regulatory/gdpr-breach-azure-dynamics)
