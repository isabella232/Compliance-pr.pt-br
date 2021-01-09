---
title: Visão geral de monitoramento de segurança
description: Saiba mais sobre o monitoramento de segurança no Microsoft 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 8a538ee055d10b002ea7efcc7d39ce20658df12b
ms.sourcegitcommit: 7a5b6bc58fc4613b38f3fda20aebee5cec6a5730
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "49787350"
---
# <a name="security-monitoring-overview"></a>Visão geral de monitoramento de segurança

## <a name="what-is-microsofts-strategy-for-monitoring-security"></a>Qual é a estratégia da Microsoft para monitorar a segurança?

O Microsoft 365 se envolve no monitoramento contínuo de segurança de seus sistemas para detectar e responder a ameaças aos Serviços do Microsoft 365. Nossos principais princípios para monitoramento e alerta de segurança são:

- Robustez: sinais e lógica para detectar uma variedade de comportamentos de ataque
- Precisão: alertas significativos para evitar distrações de ruído
- Velocidade: capacidade de capturar invasores rapidamente o suficiente para impedi-los

As soluções baseadas em nuvem, automação e escala são os principais pilares de nossa estratégia de monitoramento e resposta. Para capturar e parar ataques efetivamente na escala de alguns dos principais serviços do Microsoft 365, nossos sistemas de monitoramento precisam criar alertas altamente precisos automaticamente quase em tempo real. Da mesma forma, quando um problema é detectado, precisamos da capacidade de reduzir o risco em escala, não podemos confiar na nossa equipe para corrigir manualmente os problemas máquina por máquina. Para reduzir os riscos em escala, usamos ferramentas baseadas em nuvem para aplicar automaticamente contramedidas e fornecer aos engenheiros ferramentas para aplicar mitigações aprovadas rapidamente em todo o ambiente.

## <a name="how-does-microsoft-365-perform-security-monitoring"></a>Como o Microsoft 365 executa o monitoramento de segurança?

O Microsoft 365 usa o registro centralizado para coletar e analisar eventos de log para atividades que possam indicar um incidente de segurança. As ferramentas de registro centralizado agregam logs de todos os componentes do sistema, incluindo logs de eventos, logs de aplicativos, logs de controle de acesso e sistemas de detecção de intrusões baseados na rede. Além dos dados de nível de aplicativo e log do servidor, a infraestrutura principal em nosso serviço é equipado com agentes de segurança personalizados que geram telemetria detalhada e fornecem detecção de invasão baseada em host. Usamos essa telemetria para monitoramento e perícia.

Os dados de registro em log e telemetria que coletamos permitem alertas de segurança 24 horas por dia, sete dias por dia. Nosso sistema de alertas analisa os dados de log conforme eles são carregados, produzindo alertas quase em tempo real. Isso inclui alertas baseados em regras e alertas mais sofisticados com base em modelos de aprendizado de máquina. Nossa lógica de monitoramento vai além dos cenários de ataque genéricos e incorpora reconhecimento profundo da arquitetura e das operações do serviço. Usamos dados de monitoramento de segurança para melhorar continuamente nossos modelos para detectar novos tipos de ataques e melhorar a precisão de nosso monitoramento de segurança.

## <a name="how-does-microsoft-365-respond-to-security-monitoring-alerts"></a>Como o Microsoft 365 responde a alertas de monitoramento de segurança?

Quando precisamos tomar uma ação em resposta a um alerta ou investigar ainda mais as evidências forenses em todo o serviço, nossas ferramentas baseadas em nuvem nos permitem responder rapidamente em todo o ambiente. Essas ferramentas incluem agentes totalmente automatizados e inteligentes que respondem a ameaças detectadas com contramedidas de segurança. Em muitos casos, esses agentes implantam contramedidas automáticas para reduzir as detecções de segurança em escala sem intervenção humana. Quando isso não é possível, o sistema de monitoramento de segurança alerta automaticamente os engenheiros de chamada apropriados, que são equipados com um conjunto de ferramentas que os permitem agir em tempo real para reduzir as ameaças detectadas em escala. Possíveis incidentes escalonados para a equipe de Resposta de Segurança do Microsoft 365 são resolvidos usando o processo de resposta a incidentes de segurança.

## <a name="how-does-microsoft-365-monitor-system-availability"></a>Como o Microsoft 365 monitora a disponibilidade do sistema?

O Microsoft 365 monitora ativamente seus sistemas em busca de indicadores de sobreutilização de recursos e uso anormal. O monitoramento de recursos é complementado por redundâncias de serviço para ajudar a evitar o tempo de inatividade inesperado e fornecer aos clientes acesso confiável a produtos e serviços. Os problemas de saúde do serviço são comunicados imediatamente aos clientes por meio do SHD (Painel de Saúde do Serviço).

## <a name="related-external-regulations--certifications"></a>Regulamentações externas relacionadas & certificações

Os serviços online da Microsoft são auditados regularmente para conformidade com regulamentações e certificações externas. Consulte a tabela a seguir para validação de controles relacionados ao monitoramento de segurança.

| **Auditorias externas** | **Section** | **Data do relatório mais recente** |
|:--------|:--------|:------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | AC-2: Gerenciamento de contas <br> AC-17: Acesso remoto <br> AU-7: Redução de auditoria e geração de relatório <br> SI-4: Monitoramento do sistema de informações <br> SI-7: Integridade de software, firmware e informações <br> | 24 de setembro de 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> <br> [Declaração de Aplicabilidade](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.3: Monitoramento de disponibilidade e planejamento de capacidade | 22 de fevereiro de 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaração de Aplicabilidade](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.3: Monitoramento de disponibilidade e planejamento de capacidade <br> A.16.1: Gerenciamento de incidentes e melhorias de segurança de informações | 22 de fevereiro de 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-19: Alterar monitoramento <br> CA-26: Relatório de incidentes de segurança <br> CA-29: Engenheiros de chamada <br> CA-48: log de datacenter | 24 de dezembro de 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-19: Alterar monitoramento <br> CA-26: Relatório de incidentes de segurança <br> CA-29: Engenheiros de chamada <br> CA-30: Monitoramento de disponibilidade <br> CA-48: log de datacenter | 24 de dezembro de 2020 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-08: Relatar incidentes <br> CUEC-10: Contratos de serviço | 24 de dezembro de 2020 |

## <a name="resources"></a>Recursos

- [Nos bastidores: proteger a infraestrutura de energia do serviço do Microsoft 365](https://download.microsoft.com/download/c/4/5/c45b197e-f0d9-4f40-bd5f-ed8fc7d0cd8c/M365DCSecurityIntro_Whitepaper.pdf)
