---
title: Controles de acesso de monitoramento e auditoria do Microsoft 365
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
ms.openlocfilehash: 3021ce1dd59d5d071edec22286ae9c63833f1277
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120440"
---
# <a name="monitoring-and-auditing-access-controls-in-microsoft-365"></a>Monitorando e auditando controles de acesso no Microsoft 365

A Microsoft realiza monitoramento e auditoria abrangentes de toda a delegação, privilégios e operações que ocorrem no Microsoft 365. O controle de acesso do Microsoft 365 é um processo automatizado criado com base no princípio de privilégios mínimos e na incorporação de controles e auditorias de acesso a dados:

- Todo o acesso permitido é rastreável para um usuário exclusivo. Os administradores são responsáveis pela manipulação do conteúdo do cliente.
- Solicitações de controle de acesso, aprovações e logs de operações administrativas são capturados para análise de segurança e eventos mal-intencionados.
- Os níveis de acesso são revisados quase em tempo real com base na associação ao grupo de segurança para garantir que somente os usuários que tenham justificativas comerciais autorizadas e atenderem aos requisitos de qualificação tenham acesso aos sistemas.
- O Microsoft 365, seus controles de acesso e serviços de suporte, incluindo o Azure Active Directory e datacenters físicos, são auditados regularmente por terceiros independentes para conformidade com a [ISO/IEC 27001,](https://www.microsoft.com/TrustCenter/Compliance/iso-iec-27001) [ISO/IEC 27018,](https://www.microsoft.com/TrustCenter/Compliance/iso-iec-27018) [SOC,](https://www.microsoft.com/TrustCenter/Compliance/SOC) [FedRAMP (Office 365)](https://www.microsoft.com/TrustCenter/Compliance/FedRAMP)e outros [padrões.](https://www.microsoft.com/TrustCenter/Compliance?service=Office#Icons)
- Os engenheiros do Microsoft 365 devem fazer treinamento anual de segurança, revisar os melhores procedimentos de acesso elevado e reconhecer as políticas de segurança e privacidade da Microsoft para manter direitos ao serviço.

Alertas automatizados disparam quando atividades suspeitas são detectadas, como vários logons com falha em um curto período. A equipe de Resposta de Segurança do Microsoft 365 usa aprendizado de máquina e análise de big data para revisar e analisar a atividade, procurar padrões de acesso irregular e responder proativamente a atividades anômalas e ilícitas. A Microsoft também emprega uma equipe dedicada de testadores de penetração e se envolve em exercícios periódicos da equipe vermelha e azul para encontrar problemas de segurança e controle de acesso no serviço. Os clientes podem verificar a eficácia dos sistemas de controle de acesso usando relatórios de auditoria e a API de atividade de gerenciamento fornecida pelo Microsoft 365.

Para saber mais, confira Referência da API da Atividade de Gerenciamento do [Office 365](/office/office-365-management-api/office-365-management-activity-api-reference) e [Auditoria e relatórios no Microsoft 365.](assurance-auditing-and-reporting-overview.md)
