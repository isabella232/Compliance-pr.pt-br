---
title: 'Gerenciamento de incidentes de segurança da Microsoft: contenção, erradicação e recuperação'
description: Este artigo fornece uma visão geral do processo de contenção, erradicação e recuperação de gerenciamento de incidentes de segurança nos serviços online da Microsoft.
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
f1.keywords:
- NOCSH
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 0c99c28ee6a291acbcfe913a87aa107d3be5c75a
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2021
ms.locfileid: "58946912"
---
# <a name="microsoft-security-incident-management-containment-eradication-and-recovery"></a>Gerenciamento de incidentes de segurança da Microsoft: contenção, erradicação e recuperação

Com base na análise realizada pela equipe de resposta à segurança, a equipe de serviço e outras, um plano de recuperação e contenção apropriado é desenvolvido para minimizar o efeito do incidente de segurança. Em seguida, as equipes de serviço apropriadas aplicam esse plano em produção com suporte da equipe de resposta de segurança.

## <a name="containment"></a>Contenção

Depois de detectar um incidente de segurança, é importante conter a intrusão antes que o adversário possa acessar mais recursos ou causar mais danos. O principal objetivo de nossos procedimentos de resposta a incidentes de segurança é limitar o impacto aos clientes ou seus dados ou aos sistemas, serviços e aplicativos da Microsoft.

## <a name="eradication"></a>Erradicação

A eliminação é o processo de eliminar a causa raiz do incidente de segurança com um alto grau de confiança. O objetivo é duas vezes:

- para despejar completamente o adversário do ambiente
- para atenuar a vulnerabilidade (se conhecida) que habilitada ou poderia permitir que o adversário reentra no ambiente.

Dependendo da natureza do incidente, do escopo do incidente de segurança, da profundidade da penetração e das possíveis consequências, a equipe de resposta de segurança recomendará que as equipes de serviço adotem técnicas de erradicação. Considerando o impacto comercial potencial que pode ser causado por essas etapas de erradicação, essas decisões serão tomadas pelas equipes de serviço e pela equipe de resposta de segurança após uma análise detalhada e aprovação do Gerente executivo de Incidentes (se necessário).

## <a name="recovery"></a>Recuperação

À medida que a equipe de resposta obtém um nível razoável de confiança de que o adversário foi despejado do ambiente e todos os caminhos vulneráveis conhecidos foram eliminados, as equipes de serviço individuais iniciarão etapas de restauração para trazer o serviço para uma configuração conhecida e boa. Essas etapas de restauração estarão em consulta com a equipe de resposta à segurança. Essa atividade inclui identificar o último estado bom conhecido do serviço, restaurar de backups para esse estado, inspecionar caminhos de ataque vulneráveis no estado restaurado, etc. A equipe de resposta de segurança, em consulta com as equipes de serviço, determinará o melhor plano de recuperação possível para o ambiente.

Um aspecto importante para a recuperação é ter a segurança e os controles aprimorados para validar que o plano de recuperação foi executado com êxito e que não existem sinais de violação no ambiente.

## <a name="customer-notification-of-security-incident"></a>Notificação do cliente de incidente de segurança

Se a Microsoft determinar que ocorreu um incidente de segurança, notificaremos você com atraso indevido, e dentro dos requisitos contratuais e de conformidade que fizemos acordo. Depois de identificar todos os locatários afetados, a equipe de comunicações correspondente trabalha para identificar quaisquer regulamentos relevantes que possam se aplicar aos locatários afetados. A equipe de comunicações usa o canal de comunicação apropriado definido nos regulamentos aplicáveis para notificar o contato de locatário apropriado.

![Processo de resposta a incidentes.](../media/assurance-incident-response-process.png)

A notificação incluirá informações detalhadas sobre o incidente, como uma descrição do incidente, o efeito sobre os dados do cliente, se for o caso, ações tomadas pela Microsoft e/ou ações sugeridas para os clientes tomarem para resolver o problema e evitar a recorrência. A notificação será entregue aos administradores designados do locatário de serviços online da Microsoft. Para garantir que as notificações sejam recebidas, você deve garantir que seus administradores forneçam e mantenham informações de contato precisas em seus perfis de locatário. Além disso, dependendo da natureza do incidente, os clientes Microsoft 365 também podem ser notificados por meio do Painel de Microsoft 365 [de Saúde do Serviço.](http://status.yammer.com/)

## <a name="related-articles"></a>Artigos relacionados

- [Gerenciamento de incidentes de segurança da Microsoft](assurance-security-incident-management.md)
- [Gerenciamento de incidentes de segurança da Microsoft: Preparação](assurance-sim-preparation.md)
- [Gerenciamento de incidentes de segurança da Microsoft: Detecção e análise](assurance-sim-detection-analysis.md)
- [Gerenciamento de incidentes de segurança da Microsoft: atividade pós-incidente](assurance-sim-post-incident-activity.md)
- [Como registrar um tíquete de suporte a eventos de segurança](/azure/security/fundamentals/event-support-ticket)
- [Notificação de Violação do Azure e do Dynamics 365 no GDPR](/compliance/regulatory/gdpr-breach-azure-dynamics)
