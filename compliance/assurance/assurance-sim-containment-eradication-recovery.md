---
title: 'Gerenciamento de incidentes de segurança do Microsoft 365: contenção, eliminação e recuperação'
description: Este artigo fornece uma visão geral do processo de recuperação, eliminação e contenção de gerenciamento de incidentes de segurança no Microsoft 365.
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
ms.openlocfilehash: 702735ed2ba35a4f3b0a02123f0c58b5fb4d397e
ms.sourcegitcommit: d67e4d4fdc664f1da450c8ef2f6732e19bdd403a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/28/2021
ms.locfileid: "50037572"
---
# <a name="microsoft-365-security-incident-management-containment-eradication-and-recovery"></a>Gerenciamento de incidentes de segurança do Microsoft 365: contenção, eliminação e recuperação

Com base na análise realizada pela equipe de Resposta de Segurança do Microsoft 365, pela equipe de serviço e outros, um plano de contenção e recuperação apropriado é desenvolvido para minimizar o efeito do incidente de segurança. As equipes de serviço apropriadas aplicam esse plano em produção com suporte da equipe de Resposta de Segurança do Microsoft 365.

## <a name="containment"></a>Contenção

Depois de detectar um incidente de segurança, é importante conter a invasão antes que o adversário possa acessar mais recursos ou causar mais danos. O principal objetivo dos nossos procedimentos de resposta a incidentes de segurança é limitar o impacto aos clientes ou seus dados, ou a sistemas, serviços e aplicativos da Microsoft.

## <a name="eradication"></a>Eliminação

A eliminação é o processo de eliminação da causa raiz do incidente de segurança com um alto grau de confiança. O objetivo é de duas vezes:

- para despejar o adversário completamente do ambiente
- para atenuar a vulnerabilidade (se conhecida) que habilitar ou pode permitir que o adversário entre novamente no ambiente.

Dependendo da natureza do incidente, do escopo do incidente de segurança, da profundidade da penetração e da possível invasão, a equipe de Resposta de Segurança do Microsoft 365 recomendará que as equipes de serviço adotem técnicas de eliminação. Considerando o impacto comercial potencial que pode ser causado por essas etapas de eliminação, essas decisões serão tomadas pelas equipes de serviço e pela equipe de Resposta de Segurança do Microsoft 365 após uma análise detalhada e aprovação do Gerente executivo de incidentes (se necessário).

## <a name="recovery"></a>Recuperação

À medida que a equipe de resposta obtém um nível razoável de confiança de que o adversário foi eliminado do ambiente e todos os caminhos vulneráveis conhecidos foram eliminados, as equipes de serviço individuais iniciarão as etapas de restauração para levar o serviço a uma configuração conhecida e boa. Estas etapas de restauração estarão em consultoria com a equipe de Resposta de Segurança do Microsoft 365. Essa atividade inclui identificar o último estado bom conhecido do serviço, restaurar de backups para esse estado, inspecionar caminhos de ataque vulneráveis no estado restaurado etc. A equipe de Resposta de Segurança do Microsoft 365, em consultoria com as equipes de serviço, determinará o melhor plano de recuperação possível para o ambiente.

Um aspecto importante da recuperação é ter agilização e os controles aprimorados no local para validar se o plano de recuperação foi executado com êxito e que não existem sinais de violação no ambiente.

## <a name="customer-notification-of-security-incident"></a>Notificação de incidente de segurança do cliente

Se a Microsoft determinar que ocorreu um incidente de segurança, notificaremos você com atrasos indevidos e dentro dos requisitos contratuais e de conformidade que concordarmos. Depois de identificar todos os locatários afetados, a equipe de Comunicações da Experiência do Usuário do Microsoft 365 (CxP) trabalha para identificar quaisquer regulamentos relevantes que possam se aplicar aos locatários afetados. A equipe de Comunicações CxP do Microsoft 365 usa o canal de comunicação apropriado definido nas regulamentações aplicáveis para notificar o contato de locatário apropriado.

A notificação incluirá informações detalhadas sobre o incidente, como uma descrição do incidente, o efeito sobre os dados do cliente, se algum, ações tomadas pela Microsoft e/ou ações sugeridas para os clientes tomarem para resolver o problema e evitar a recorrência. A notificação será entregue aos administradores designados do locatário do Microsoft 365. Para garantir que as notificações sejam recebidas, você deve garantir que seus administradores forneçam e mantenham informações de contato precisas em seus perfis de locatário. Além disso, dependendo da natureza do incidente, os clientes também podem ser notificados por meio do Painel de Saúde do Serviço do Microsoft 365.[](http://status.yammer.com/)

## <a name="related-articles"></a>Artigos relacionados

- [Gerenciamento de incidentes do Centro de segurança do Microsoft 365](assurance-security-incident-management.md)
- [Preparação do gerenciamento de incidentes de segurança do Microsoft 365](assurance-sim-preparation.md)
- [Análise e detecção de gerenciamento de incidentes de segurança do Microsoft 365](assurance-sim-detection-analysis.md)
- [Atividade pós-incidente de gerenciamento de incidentes de segurança do Microsoft 365](assurance-sim-post-incident-activity.md)
