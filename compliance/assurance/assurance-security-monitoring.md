---
title: Visão geral do monitoramento de segurança
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
ms.openlocfilehash: f3eae0aa5ba79372a7ce0d9a34d4dd35fe83a36b
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/30/2020
ms.locfileid: "49505967"
---
# <a name="security-monitoring-overview"></a>Visão geral do monitoramento de segurança

## <a name="what-is-microsofts-strategy-for-monitoring-security"></a>Qual é a estratégia da Microsoft para monitorar a segurança?

A Microsoft 365 se encaixa no monitoramento contínuo de segurança de seus sistemas para detectar e responder a ameaças aos serviços da Microsoft 365. Os principais princípios para monitoramento e alerta de segurança são:

- Robustez: sinais e lógica para detectar uma variedade de comportamentos de ataque
- Precisão: alertas significativos para evitar distrações de ruído
- Velocidade: capacidade de detectar invasores com rapidez suficiente para interrompê-los

Automação, escala e soluções baseadas em nuvem são os principais pilares da nossa estratégia de monitoramento e resposta. Para que possamos capturar e parar com eficácia os ataques na escala de alguns dos serviços principais da Microsoft 365, nossos sistemas de monitoramento precisam gerar automaticamente alertas altamente precisos em tempo quase real. Da mesma forma, quando um problema é detectado, precisamos da capacidade de reduzir o risco em escala, não podemos contar com a nossa equipe para corrigir problemas manualmente máquina por máquina. Para reduzir os riscos em escala, usamos ferramentas baseadas em nuvem para aplicar automaticamente medidas defensivas e fornecer aos engenheiros ferramentas para aplicar atenuações aprovadas rapidamente em todo o ambiente.

## <a name="how-does-microsoft-365-perform-security-monitoring"></a>Como a Microsoft 365 realiza o monitoramento de segurança?

O Microsoft 365 usa o registro em log centralizado para coletar e analisar eventos de log para atividades que podem indicar um incidente de segurança. As ferramentas de log centralizado agregam logs de todos os componentes do sistema, incluindo logs de eventos, logs de aplicativos, logs de controle de acesso e sistemas de detecção de invasão baseados em rede. Além de logs de servidor e dados de nível de aplicativo, a infraestrutura principal do nosso serviço é equipada com agentes de segurança personalizados que geram telemetria detalhada e fornecem detecção de invasão baseada em host. Usamos essa telemetria para monitoramento e perícia.

Os dados de registro e telemetria que coletamos habilitam o alerta de segurança 24/7. Nosso sistema de alerta analisa os dados de log à medida que são carregados, produzindo alertas quase em tempo real. Isso inclui alertas baseados em regras e alertas mais sofisticados com base nos modelos de aprendizado da máquina. Nossa lógica de monitoramento vai além dos cenários de ataque genéricos e incorpora a conscientização profunda da arquitetura e das operações do serviço. Usamos dados de monitoramento de segurança para melhorar continuamente nossos modelos para detectar novos tipos de ataques e melhorar a precisão de nosso monitoramento de segurança.

## <a name="how-does-microsoft-365-respond-to-security-monitoring-alerts"></a>Como a Microsoft 365 responde aos alertas de monitoramento de segurança?

Quando precisamos realizar uma ação em resposta a um alerta ou para investigar mais evidências forenses por todo o serviço, nossas ferramentas baseadas em nuvem permitem que possamos responder rapidamente em todo o ambiente. Essas ferramentas incluem agentes totalmente automatizados e inteligentes que respondem a ameaças detectadas por medidas de segurança. Em muitos casos, esses agentes implantam contramedidas automáticas para reduzir as detecções de segurança em escala sem intervenção humana. Quando isso não é possível, o sistema de monitoramento de segurança alerta automaticamente os engenheiros de chamada apropriados, que estão equipados com um conjunto de ferramentas que permitem agir em tempo real para reduzir as ameaças detectadas em escala. Possíveis incidentes escalonados para a equipe de resposta de segurança do Microsoft 365 são resolvidos usando o processo de resposta a incidentes de segurança.

## <a name="how-does-microsoft-365-monitor-system-availability"></a>Como a Microsoft 365 monitora a disponibilidade do sistema?

A Microsoft 365 monitora ativamente seus sistemas em busca de indicadores de utilização de recursos e uso anormal. O monitoramento de recursos é complementado por redundâncias de serviço para ajudar a evitar tempo de inatividade inesperado e fornecer aos clientes acesso confiável a produtos e serviços. Os problemas de integridade do serviço são comunicados imediatamente aos clientes por meio do painel de integridade do serviço (SDH).

## <a name="related-external-regulations--certifications"></a>Normas externas relacionadas & certificações

Os serviços online da Microsoft são auditados regularmente para fins de conformidade com regulamentos externos e certificações. Consulte a tabela a seguir para a validação de controles relacionados ao monitoramento de segurança.

| **Auditorias externas** | **Section** | **Data do relatório mais recente** |
|:--------|:--------|:------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | AC-2: gerenciamento de contas <br> AC-17: acesso remoto <br> AU-7: redução de auditoria e geração de relatórios <br> SI-4: monitoramento do sistema de informações <br> SI-7: software, firmware e integridade de informações <br> | 24 de setembro de 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> <br> [Declaração de aplicabilidade](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 12.1.3: monitoramento de disponibilidade e planejamento de capacidade | 22 de fevereiro de 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaração de aplicabilidade](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 12.1.3: monitoramento de disponibilidade e planejamento de capacidade <br> A. 16.1: gerenciamento de incidentes e melhorias de segurança de informações | 22 de fevereiro de 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | AC-19: alterar o monitoramento <br> AC-26: relatórios de incidentes de segurança <br> CA – 29: engenheiros em chamada <br> AC-48: log de datacenter | 30 de setembro de 2019 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | AC-19: alterar o monitoramento <br> AC-26: relatórios de incidentes de segurança <br> CA – 29: engenheiros em chamada <br> CA-30: monitoramento de disponibilidade <br> AC-48: log de datacenter | 30 de setembro de 2019 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=9df8b99b-96ce-49a9-bff4-268031dcc9a6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CUEC-08: relatórios de incidentes <br> CUEC-10: contratos de serviço | 30 de setembro de 2019 |

## <a name="resources"></a>Recursos

- [Nos bastidores: Securing the Infrastructure Power The Microsoft 365 Service](https://download.microsoft.com/download/c/4/5/c45b197e-f0d9-4f40-bd5f-ed8fc7d0cd8c/M365DCSecurityIntro_Whitepaper.pdf)
