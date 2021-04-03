---
title: Controles de Acesso de Monitoramento e Auditoria do Microsoft 365
description: 'Resumo: um resumo dos vários controles de acesso de monitoramento e auditoria disponíveis no Microsoft 365.'
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
hideEdit: true
ms.openlocfilehash: e9a9ea713afbf7568c1ae67d31a57dd9dce51fc3
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497538"
---
# <a name="monitoring-and-auditing-access-controls-in-microsoft-365"></a><span data-ttu-id="11e8e-103">Controles de acesso de monitoramento e auditoria no Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="11e8e-103">Monitoring and auditing access controls in Microsoft 365</span></span>

<span data-ttu-id="11e8e-104">A Microsoft realiza um monitoramento extensivo e auditoria de todas as delegações, privilégios e operações que ocorrem no Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="11e8e-104">Microsoft performs extensive monitoring and auditing of all delegation, privileges, and operations that occur within Microsoft 365.</span></span> <span data-ttu-id="11e8e-105">O controle de acesso do Microsoft 365 é um processo automatizado criado com base no princípio do privilégio mínimo e da incorporação de controles e auditorias de acesso a dados:</span><span class="sxs-lookup"><span data-stu-id="11e8e-105">Microsoft 365 access control is an automated process built on the principle of least privilege and incorporating data access controls and audits:</span></span>

- <span data-ttu-id="11e8e-106">Todo o acesso permitido pode ser rastreado para um usuário exclusivo.</span><span class="sxs-lookup"><span data-stu-id="11e8e-106">All permitted access is traceable to a unique user.</span></span> <span data-ttu-id="11e8e-107">Os administradores são responsáveis pela manipulação do conteúdo do cliente.</span><span class="sxs-lookup"><span data-stu-id="11e8e-107">Administrators are accountable for their handling of customer content.</span></span>
- <span data-ttu-id="11e8e-108">Solicitações de controle de acesso, aprovações e logs de operações administrativas são capturados para análise de eventos mal-intencionados e de segurança.</span><span class="sxs-lookup"><span data-stu-id="11e8e-108">Access control requests, approvals, and administrative operations logs are captured for analysis of security and malicious events.</span></span>
- <span data-ttu-id="11e8e-109">Os níveis de acesso são revisados quase em tempo real com base na associação ao grupo de segurança para garantir que somente os usuários que tenham justificativas comerciais autorizadas e atenderem aos requisitos de qualificação tenham acesso aos sistemas.</span><span class="sxs-lookup"><span data-stu-id="11e8e-109">Access levels are reviewed in near real-time based on security group membership to ensure that only users who have authorized business justifications and meet the eligibility requirements have access to the systems.</span></span>
- <span data-ttu-id="11e8e-110">O Microsoft 365, seus controles de acesso e serviços de suporte, incluindo o Azure Active Directory e datacenters físicos, são regularmente auditados por terceiros independentes para conformidade com [ISO/IEC 27001,](https://www.microsoft.com/TrustCenter/Compliance/iso-iec-27001) [ISO/IEC 27018,](https://www.microsoft.com/TrustCenter/Compliance/iso-iec-27018) [SOC,](https://www.microsoft.com/TrustCenter/Compliance/SOC) [FedRAMP (Office 365)](https://www.microsoft.com/TrustCenter/Compliance/FedRAMP)e outros [padrões.](https://www.microsoft.com/TrustCenter/Compliance?service=Office#Icons)</span><span class="sxs-lookup"><span data-stu-id="11e8e-110">Microsoft 365, its access controls, and supporting services, including Azure Active Directory and physical datacenters, are regularly audited by independent third-parties for compliance with [ISO/IEC 27001](https://www.microsoft.com/TrustCenter/Compliance/iso-iec-27001), [ISO/IEC 27018](https://www.microsoft.com/TrustCenter/Compliance/iso-iec-27018), [SOC](https://www.microsoft.com/TrustCenter/Compliance/SOC), [FedRAMP (Office 365)](https://www.microsoft.com/TrustCenter/Compliance/FedRAMP), and other [standards](https://www.microsoft.com/TrustCenter/Compliance?service=Office#Icons).</span></span>
- <span data-ttu-id="11e8e-111">Os engenheiros do Microsoft 365 devem fazer treinamento anual de segurança, revisar os melhores procedimentos de acesso elevado e reconhecer as políticas de segurança e privacidade da Microsoft para manter direitos ao serviço.</span><span class="sxs-lookup"><span data-stu-id="11e8e-111">Microsoft 365 engineers must take yearly security training, review elevated access best procedures, and acknowledge Microsoft's security and privacy policies to maintain entitlements to the service.</span></span>

<span data-ttu-id="11e8e-112">Alertas automatizados disparam quando atividades suspeitas são detectadas, como vários logons com falha em um curto período.</span><span class="sxs-lookup"><span data-stu-id="11e8e-112">Automated alerts trigger when suspicious activity is detected, such as multiple failed logins within a short period.</span></span> <span data-ttu-id="11e8e-113">A equipe de Resposta de Segurança do Microsoft 365 usa aprendizado de máquina e análise de big data para revisar e analisar a atividade, procurar padrões de acesso irregular e responder proativamente a atividades anômalas e ilícitas.</span><span class="sxs-lookup"><span data-stu-id="11e8e-113">The Microsoft 365 Security Response team uses machine learning and big data analysis to review and analyze activity, look for irregular access patterns, and proactively respond to anomalous and illicit activities.</span></span> <span data-ttu-id="11e8e-114">A Microsoft também emprega uma equipe dedicada de testadores de penetração e se envolve em exercícios periódicos de Equipe Vermelha e Equipe Azul para encontrar problemas de segurança e controle de acesso no serviço.</span><span class="sxs-lookup"><span data-stu-id="11e8e-114">Microsoft also employs a dedicated team of penetration testers and engages in periodic Red Team and Blue Team exercises to find security and access control issues in the service.</span></span> <span data-ttu-id="11e8e-115">Os clientes podem verificar a eficácia dos sistemas de controle de acesso usando relatórios de auditoria e a API de atividade de gerenciamento fornecida pelo Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="11e8e-115">Customers can verify the effectiveness of access control systems by using audit reports and the management activity API provided by Microsoft 365.</span></span>

<span data-ttu-id="11e8e-116">Para obter mais informações, consulte Referência da API de Atividade de Gerenciamento do [Office 365](/office/office-365-management-api/office-365-management-activity-api-reference) e [Auditoria e relatórios no Microsoft 365](assurance-auditing-and-reporting-overview.md).</span><span class="sxs-lookup"><span data-stu-id="11e8e-116">For more information, see [Office 365 Management Activity API reference](/office/office-365-management-api/office-365-management-activity-api-reference) and [Auditing and reporting in Microsoft 365](assurance-auditing-and-reporting-overview.md).</span></span>
