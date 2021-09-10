---
title: Microsoft 365 Monitoramento e auditoria de controles de acesso
description: 'Resumo: um resumo dos vários controles de acesso de monitoramento e auditoria disponíveis no Microsoft 365.'
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: medium
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
ms.openlocfilehash: bf760bf68169092f99fe5a668c9f0087060f7ea2
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2021
ms.locfileid: "58946919"
---
# <a name="monitoring-and-auditing-access-controls-in-microsoft-365"></a>Monitoramento e auditoria de controles de acesso Microsoft 365

A Microsoft realiza um monitoramento extensivo e auditoria de todas as delegações, privilégios e operações que ocorrem dentro Microsoft 365. Microsoft 365 de acesso é um processo automatizado criado com base no princípio de privilégio mínimo e incorporação de controles e auditorias de acesso a dados:

- Todo o acesso permitido pode ser rastreado para um usuário exclusivo. Os administradores são responsáveis pela manipulação do conteúdo do cliente.
- Solicitações de controle de acesso, aprovações e logs de operações administrativas são capturados para análise de eventos mal-intencionados e de segurança.
- Os níveis de acesso são revisados quase em tempo real com base na associação ao grupo de segurança para garantir que somente os usuários que tenham justificativas comerciais autorizadas e atenderem aos requisitos de qualificação tenham acesso aos sistemas.
- Microsoft 365, seus controles de acesso e serviços de suporte, incluindo Azure Active Directory e datacenters físicos, são regularmente auditados por terceiros independentes para conformidade com [ISO/IEC 27001,](https://www.microsoft.com/TrustCenter/Compliance/iso-iec-27001) [ISO/IEC 27018,](https://www.microsoft.com/TrustCenter/Compliance/iso-iec-27018) [SOC,](https://www.microsoft.com/TrustCenter/Compliance/SOC) [FedRAMP (Office 365)](https://www.microsoft.com/TrustCenter/Compliance/FedRAMP)e outros [padrões.](https://www.microsoft.com/TrustCenter/Compliance?service=Office#Icons)
- Microsoft 365 os engenheiros devem fazer treinamento anual de segurança, revisar os melhores procedimentos de acesso elevado e reconhecer as políticas de segurança e privacidade da Microsoft para manter direitos ao serviço.

Alertas automatizados disparam quando atividades suspeitas são detectadas, como vários logons com falha em um curto período. A Microsoft 365 de Resposta de Segurança usa aprendizado de máquina e análise de big data para revisar e analisar atividades, procurar padrões de acesso irregulares e responder proativamente a atividades anômalas e ilícitas. A Microsoft também emprega uma equipe dedicada de testadores de penetração e se envolve em exercícios periódicos de Equipe Vermelha e Equipe Azul para encontrar problemas de segurança e controle de acesso no serviço. Os clientes podem verificar a eficácia dos sistemas de controle de acesso usando relatórios de auditoria e a API de atividade de gerenciamento fornecida por Microsoft 365.

Para obter mais informações, [consulte Office 365 referência](/office/office-365-management-api/office-365-management-activity-api-reference) da API de Atividade de Gerenciamento e Auditoria e relatórios em [Microsoft 365](assurance-auditing-and-reporting-overview.md).
