---
title: 'Gerenciamento de incidentes de segurança do Microsoft 365: Atividade pós-incidente'
description: Este artigo fornece uma visão geral do processo de atividade pós-incidente de gerenciamento de incidentes de segurança no Microsoft 365.
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
ms.openlocfilehash: 4ebd31c16f8abb3eddd6ed924a045d88597aba40
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51496708"
---
# <a name="microsoft-365-security-incident-management-post-incident-activity"></a><span data-ttu-id="45d51-103">Gerenciamento de incidentes de segurança do Microsoft 365: Atividade pós-incidente</span><span class="sxs-lookup"><span data-stu-id="45d51-103">Microsoft 365 security incident management: Post-incident activity</span></span>

## <a name="postmortem"></a><span data-ttu-id="45d51-104">Post-mortem</span><span class="sxs-lookup"><span data-stu-id="45d51-104">Postmortem</span></span>

<span data-ttu-id="45d51-105">Alguns incidentes de segurança, especialmente aqueles incidentes que estão afetando o cliente ou resultando em uma violação de dados, estão sujeitos a um incidente completo pós-morte.</span><span class="sxs-lookup"><span data-stu-id="45d51-105">Some security incidents, especially those incidents that are customer impacting or result in a data breach, are subject to a full incident postmortem.</span></span> <span data-ttu-id="45d51-106">A equipe de Resposta de Segurança do Microsoft 365 conduz uma post-morte detalhada com todas as partes envolvidas na resposta a incidentes de segurança:</span><span class="sxs-lookup"><span data-stu-id="45d51-106">The Microsoft 365 Security Response team conducts a detailed postmortem with all the parties involved in security incident response to:</span></span>

- <span data-ttu-id="45d51-107">Documente a sequência de eventos que causaram o incidente</span><span class="sxs-lookup"><span data-stu-id="45d51-107">Document the sequence of events that caused the incident</span></span>
- <span data-ttu-id="45d51-108">Crie um resumo técnico do incidente como suportado pelas evidências que incluem os atores envolvidos na violação (se conhecido).</span><span class="sxs-lookup"><span data-stu-id="45d51-108">Create a technical summary of the incident as supported by the evidence that includes the actors involved in the breach (if known).</span></span> <span data-ttu-id="45d51-109">Este resumo incluirá como a resposta foi executada e outros pontos importantes.</span><span class="sxs-lookup"><span data-stu-id="45d51-109">This summary will include how the response was executed and other key takeaways.</span></span>
- <span data-ttu-id="45d51-110">Identifique erros técnicos, falhas de procedimento, erros manuais, falhas de processo e falhas de comunicação e/ou quaisquer vetores de ataque desconhecidos anteriormente identificados durante a resposta a incidentes de segurança.</span><span class="sxs-lookup"><span data-stu-id="45d51-110">Identify technical lapses, procedural failures, manual errors, process flaws, and communication glitches, and/or any previously unknown attack vectors that were identified during the security incident response.</span></span>

<span data-ttu-id="45d51-111">A postagem pós-morte influenciará diretamente o aperfeiçoamento do serviço, os processos operacionais e a documentação do Microsoft 365 definindo novas prioridades no ciclo de desenvolvimento de engenharia do Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="45d51-111">The postmortem will directly influence Microsoft 365 service improvement, operational processes, and documentation by setting new priorities in the Microsoft 365 engineering development cycle.</span></span>

## <a name="documentation"></a><span data-ttu-id="45d51-112">Documentação</span><span class="sxs-lookup"><span data-stu-id="45d51-112">Documentation</span></span>

<span data-ttu-id="45d51-113">Todas as principais descobertas técnicas no processo pós-morte são capturadas em um relatório e investimentos de serviço ou correções na forma de bugs ou solicitações de alteração de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="45d51-113">All key technical findings in the postmortem process are captured in a report and service investments or fixes in the form of bugs or development change requests.</span></span> <span data-ttu-id="45d51-114">Essas descobertas são acompanhadas com as equipes de engenharia apropriadas.</span><span class="sxs-lookup"><span data-stu-id="45d51-114">These findings are followed-up with the appropriate engineering teams.</span></span> <span data-ttu-id="45d51-115">Para falhas de processo e problemas organizacionais entre organizações, os problemas são documentados no banco de dados da equipe de Resposta de Segurança do Microsoft 365 e acompanhados com os grupos apropriados para lidar com eles.</span><span class="sxs-lookup"><span data-stu-id="45d51-115">For process failures and cross-organizational issues, issues are documented in the Microsoft 365 Security Response team's database and followed-up with the appropriate groups to address them.</span></span>

## <a name="process-improvement"></a><span data-ttu-id="45d51-116">Melhoria do processo</span><span class="sxs-lookup"><span data-stu-id="45d51-116">Process improvement</span></span>

<span data-ttu-id="45d51-117">Responder a um incidente de segurança no Microsoft 365 envolve a coordenação com vários grupos espalhados por organizações diferentes dentro da Microsoft e, potencialmente, até mesmo organizações externas apropriadas, como a aplicação da lei.</span><span class="sxs-lookup"><span data-stu-id="45d51-117">Responding to a security incident in Microsoft 365 involves coordination with multiple groups spread across different organizations within Microsoft, and potentially even appropriate external organizations such as law enforcement.</span></span> <span data-ttu-id="45d51-118">Sabemos que é fundamental avaliar nossas respostas após cada incidente de segurança para suficiência e conclusão.</span><span class="sxs-lookup"><span data-stu-id="45d51-118">We know that it is critical to evaluate our responses after every security incident for both sufficiency and completeness.</span></span> <span data-ttu-id="45d51-119">Para quaisquer melhorias ou alterações identificadas, a equipe de Resposta de Segurança do Microsoft 365 avalia as sugestões em consulta com as equipes e participantes apropriados e, quando apropriado, as incorpora em procedimentos operacionais padrão.</span><span class="sxs-lookup"><span data-stu-id="45d51-119">For any identified improvements or changes, the Microsoft 365 Security Response team evaluates the suggestions in consultation with the appropriate teams and stakeholders, and where appropriate incorporates them into standard operating procedures.</span></span> <span data-ttu-id="45d51-120">Todas as alterações, bugs ou melhorias de serviço necessárias identificadas durante a resposta a incidentes de segurança ou atividades pós-morte são registradas e rastreadas em um banco de dados de engenharia interno do Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="45d51-120">All required changes, bugs, or service improvements identified during the security incident response or postmortem activity are logged and tracked in an internal Microsoft 365 engineering database.</span></span> <span data-ttu-id="45d51-121">Todos os possíveis bugs ou recursos são atribuídos ao proprietário apropriado.</span><span class="sxs-lookup"><span data-stu-id="45d51-121">All potential bugs or features are assigned to the appropriate owner.</span></span> <span data-ttu-id="45d51-122">A equipe de Resposta de Segurança do Microsoft 365 revisa todas as entradas até que o problema seja resolvido.</span><span class="sxs-lookup"><span data-stu-id="45d51-122">The Microsoft 365 Security Response team reviews all entries until the issue is resolved.</span></span>

## <a name="related-articles"></a><span data-ttu-id="45d51-123">Artigos relacionados</span><span class="sxs-lookup"><span data-stu-id="45d51-123">Related articles</span></span>

- [<span data-ttu-id="45d51-124">Gerenciamento de incidentes do Centro de segurança do Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="45d51-124">Microsoft 365 security incident management</span></span>](assurance-security-incident-management.md)
- [<span data-ttu-id="45d51-125">Preparação do gerenciamento de incidentes de segurança do Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="45d51-125">Microsoft 365 security incident management preparation</span></span>](assurance-sim-preparation.md)
- [<span data-ttu-id="45d51-126">Análise e detecção de gerenciamento de incidentes de segurança do Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="45d51-126">Microsoft 365 security incident management detection and analysis</span></span>](assurance-sim-detection-analysis.md)
- [<span data-ttu-id="45d51-127">Contenção, erradicação e recuperação de gerenciamento de incidentes de segurança do Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="45d51-127">Microsoft 365 security incident management containment, eradication, and recovery</span></span>](assurance-sim-containment-eradication-recovery.md)
