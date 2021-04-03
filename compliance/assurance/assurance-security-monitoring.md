---
title: Visão geral de monitoramento de segurança
description: Saiba mais sobre monitoramento de segurança no Microsoft 365
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
hideEdit: true
ms.openlocfilehash: 7a38d4c16de5ee489dab76165b952140af6a4656
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497417"
---
# <a name="security-monitoring-overview"></a>Visão geral de monitoramento de segurança

## <a name="what-is-microsofts-strategy-for-monitoring-security"></a>Qual é a estratégia da Microsoft para monitorar a segurança?

O Microsoft 365 se envolve no monitoramento contínuo de segurança de seus sistemas para detectar e responder a ameaças aos Serviços do Microsoft 365. Nossos princípios principais para monitoramento e alertas de segurança são:

- Robustez: sinais e lógica para detectar uma variedade de comportamentos de ataque
- Precisão: alertas significativos para evitar distrações de ruído
- Velocidade: capacidade de capturar invasores rapidamente o suficiente para impedi-los

Soluções baseadas em automação, escala e nuvem são os principais pilares de nossa estratégia de monitoramento e resposta. Para capturar e parar ataques efetivamente na escala de alguns dos serviços principais do Microsoft 365, nossos sistemas de monitoramento precisam levantar automaticamente alertas altamente precisos em tempo real. Da mesma forma, quando um problema é detectado, precisamos da capacidade de reduzir o risco em escala, não podemos contar com nossa equipe para corrigir manualmente problemas máquina a máquina. Para reduzir os riscos em escala, usamos ferramentas baseadas em nuvem para aplicar contramedidas automaticamente e fornecer aos engenheiros ferramentas para aplicar mitigações aprovadas rapidamente em todo o ambiente.

## <a name="how-does-microsoft-365-perform-security-monitoring"></a>Como o Microsoft 365 executa o monitoramento de segurança?

O Microsoft 365 usa o log centralizado para coletar e analisar eventos de log para atividades que possam indicar um incidente de segurança. As ferramentas de registro em log centralizadas agregam logs de todos os componentes do sistema, incluindo logs de eventos, logs de aplicativos, logs de controle de acesso e sistemas de detecção de intrusão baseados em rede. Além dos dados de log do servidor e do nível do aplicativo, a infraestrutura principal em nosso serviço é equipada com agentes de segurança personalizados que geram telemetria detalhada e fornecem detecção de intrusão baseada em host. Usamos essa telemetria para monitoramento e perícia.

Os dados de log e telemetria que coletamos permitem alertas de segurança 24 horas por dia. Nosso sistema de alerta analisa os dados de log à medida que são carregados, produzindo alertas em tempo real. Isso inclui alertas baseados em regras e alertas mais sofisticados com base em modelos de aprendizado de máquina. Nossa lógica de monitoramento vai além dos cenários de ataque genéricos e incorpora uma profunda percepção da arquitetura e das operações do serviço. Usamos dados de monitoramento de segurança para melhorar continuamente nossos modelos para detectar novos tipos de ataques e melhorar a precisão do nosso monitoramento de segurança.

## <a name="how-does-microsoft-365-respond-to-security-monitoring-alerts"></a>Como o Microsoft 365 responde aos alertas de monitoramento de segurança?

Quando precisamos tomar uma ação em resposta a um alerta ou investigar ainda mais as evidências forenses em todo o serviço, nossas ferramentas baseadas em nuvem nos permitem responder rapidamente em todo o ambiente. Essas ferramentas incluem agentes inteligentes e totalmente automatizados que respondem a ameaças detectadas com medidas de segurança. Em muitos casos, esses agentes implantam contramedidas automáticas para reduzir as detecções de segurança em escala sem intervenção humana. Quando isso não é possível, o sistema de monitoramento de segurança alerta automaticamente os engenheiros de chamada apropriados, que estão equipados com um conjunto de ferramentas que permitem que eles ajam em tempo real para mitigar ameaças detectadas em escala. Possíveis incidentes escalonados para a equipe de Resposta de Segurança do Microsoft 365 são resolvidos usando o processo de resposta a incidentes de segurança.

## <a name="how-does-microsoft-365-monitor-system-availability"></a>Como o Microsoft 365 monitora a disponibilidade do sistema?

O Microsoft 365 monitora ativamente seus sistemas em busca de indicadores de sobreutilização de recursos e uso anormal. O monitoramento de recursos é complementado por redundâncias de serviço para ajudar a evitar o tempo de inatividade inesperado e fornecer aos clientes acesso confiável a produtos e serviços. Os problemas de saúde do serviço são comunicados prontamente aos clientes por meio do Painel de Saúde do Serviço (SHD).

## <a name="related-external-regulations--certifications"></a>Regulamentações externas relacionadas & certificações

Os serviços online da Microsoft são regularmente auditados para conformidade com regulamentações e certificações externas. Consulte a tabela a seguir para validação de controles relacionados ao monitoramento de segurança.

| **Auditorias externas** | **Section** | **Data do relatório mais recente** |
|:--------|:--------|:------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | AC-2: Gerenciamento de contas <br> AC-17: Acesso remoto <br> AU-7: Redução de auditoria e geração de relatório <br> SI-4: Monitoramento do sistema de informações <br> SI-7: Integridade de software, firmware e informações <br> | 24 de setembro de 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> <br> [Instrução of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.3: Monitoramento de disponibilidade e planejamento de capacidade | 22 de fevereiro de 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Instrução of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.3: Monitoramento de disponibilidade e planejamento de capacidade <br> A.16.1: Gerenciamento de incidentes e melhorias de segurança da informação | 22 de fevereiro de 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-19: Alterar monitoramento <br> CA-26: Relatório de incidentes de segurança <br> CA-29: engenheiros de chamada <br> CA-48: log de datacenter | 24 de dezembro de 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-19: Alterar monitoramento <br> CA-26: Relatório de incidentes de segurança <br> CA-29: engenheiros de chamada <br> CA-30: Monitoramento de disponibilidade <br> CA-48: log de datacenter | 24 de dezembro de 2020 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-08: Relatórios de incidentes <br> CUEC-10: Contratos de serviço | 24 de dezembro de 2020 |

## <a name="resources"></a>Recursos

- [Bastidores: proteger a infraestrutura que está usando o serviço do Microsoft 365](https://download.microsoft.com/download/c/4/5/c45b197e-f0d9-4f40-bd5f-ed8fc7d0cd8c/M365DCSecurityIntro_Whitepaper.pdf)
