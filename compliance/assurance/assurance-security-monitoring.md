---
title: Visão geral de monitoramento de segurança
description: Saiba mais sobre monitoramento de segurança Microsoft 365
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
- MS-Compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: c39acaae68ea8c9f6b4503df55a52d344f10c36fc2792b2202961b5ebe51f32a
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/05/2021
ms.locfileid: "54292059"
---
# <a name="security-monitoring-overview"></a>Visão geral de monitoramento de segurança

## <a name="what-is-microsofts-strategy-for-monitoring-security"></a>Qual é a estratégia da Microsoft para monitorar a segurança?

O Microsoft 365 envolve o monitoramento contínuo de segurança de seus sistemas para detectar e responder a ameaças aos Microsoft 365 Services. Nossos princípios principais para monitoramento e alertas de segurança são:

- Robustez: sinais e lógica para detectar uma variedade de comportamentos de ataque
- Precisão: alertas significativos para evitar distrações de ruído
- Velocidade: capacidade de capturar invasores rapidamente o suficiente para impedi-los

As soluções baseadas em nuvem, escala e automação são pilares fundamentais de nossa estratégia de monitoramento e resposta. Para que nós capturemos e interrompamos ataques com eficiência na escala de alguns dos principais serviços do Microsoft 365, nossos sistemas de monitoramento precisam gerar automaticamente alertas altamente precisos quase em tempo real. Da mesma forma, quando um problema é detectado, precisamos da capacidade de reduzir o risco em escala, não podemos contar com nossa equipe para corrigir manualmente problemas máquina a máquina. Para reduzir os riscos em escala, usamos ferramentas baseadas em nuvem para aplicar contramedidas automaticamente e fornecer aos engenheiros ferramentas para aplicar mitigações aprovadas rapidamente em todo o ambiente.

## <a name="how-does-microsoft-365-perform-security-monitoring"></a>Como o Microsoft 365 executa o monitoramento de segurança?

Microsoft 365 utiliza o log centralizado para coletar e analisar eventos de log para atividades que possam indicar um incidente de segurança. As ferramentas de log centralizadas agregam logs de todos os componentes do sistema, incluindo logs de eventos, logs de aplicativos, logs de controle de acesso e sistemas de detecção de intrusão baseados em rede. Além do registro em log do servidor e dos dados no nível do aplicativo, a infraestrutura principal em nosso serviço é equipada com agentes de segurança personalizados que geram telemetria detalhada e fornecem detecção de intrusão baseada em host. Usamos essa telemetria para monitoramento e análise forense.

Os dados de log e telemetria que coletamos permitem alertas de segurança 24 horas por dia. Nosso sistema de alertas analisa os dados de log conforme eles são carregados, produzindo alertas quase em tempo real. Isso inclui alertas baseados em regras e alertas mais sofisticados com base em modelos de aprendizado de máquina. Nossa lógica de monitoramento vai além dos cenários de ataque genéricos e incorpora reconhecimento profundo da arquitetura e das operações do serviço. Usamos dados de monitoramento de segurança para melhorar continuamente nossos modelos para detectar novos tipos de ataques e melhorar a precisão de nosso monitoramento de segurança.

## <a name="how-does-microsoft-365-respond-to-security-monitoring-alerts"></a>Como o Microsoft 365 responde aos alertas de monitoramento de segurança?

Quando precisamos tomar uma ação em resposta a um alerta ou investigar ainda mais as evidências forenses em todo o serviço, nossas ferramentas baseadas em nuvem nos permitem responder rapidamente em todo o ambiente. Essas ferramentas incluem agentes inteligentes e totalmente automatizados que respondem a ameaças detectadas com contramedidas de segurança. Em muitos casos, esses agentes implantam contramedidas automáticas para atenuar detecções de segurança em escala sem intervenção humana. Quando isso não é possível, o sistema de monitoramento de segurança alerta automaticamente os engenheiros de chamada apropriados, que estão equipados com um conjunto de ferramentas que permitem que eles atuem em tempo real para atenuar as ameaças detectadas em escala. Os possíveis incidentes escalonados para Microsoft 365 equipe de Resposta de Segurança são resolvidos usando o processo de resposta a incidentes de segurança.

## <a name="how-does-microsoft-365-monitor-system-availability"></a>Como o Microsoft 365 monitora a disponibilidade do sistema?

Microsoft 365 monitora ativamente seus sistemas para indicadores de sobreutilização de recursos e uso anormal. O monitoramento de recursos é complementado por redundâncias de serviço para ajudar a evitar o tempo de inatividade inesperado e fornecer aos clientes acesso confiável a produtos e serviços. Os problemas de saúde do serviço são comunicados prontamente aos clientes por meio do Painel de Saúde do Serviço (SHD).

## <a name="related-external-regulations--certifications"></a>Regulamentações externas relacionadas & certificações

Os serviços online da Microsoft são regularmente auditados para conformidade com regulamentações e certificações externas. Consulte a tabela a seguir para validação de controles relacionados ao monitoramento de segurança.

| **Auditorias externas** | **Section** | **Data do relatório mais recente** |
|:--------|:--------|:------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | AC-2: Gerenciamento de contas <br> AC-17: Acesso remoto <br> AU-7: Redução de auditoria e geração de relatório <br> SI-4: Monitoramento do sistema de informações <br> SI-7: Integridade de software, firmware e informações <br> | 24 de setembro de 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> <br> [Instrução of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.3: Monitoramento de disponibilidade e planejamento de capacidade | Abril de 20, 2021 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Instrução of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.3: Monitoramento de disponibilidade e planejamento de capacidade <br> A.16.1: Gerenciamento de incidentes e melhorias de segurança da informação | Abril de 20, 2021 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-19: Alterar monitoramento <br> CA-26: Relatório de incidentes de segurança <br> CA-29: engenheiros de chamada <br> CA-48: log de datacenter | 24 de dezembro de 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-19: Alterar monitoramento <br> CA-26: Relatório de incidentes de segurança <br> CA-29: engenheiros de chamada <br> CA-30: Monitoramento de disponibilidade <br> CA-48: log de datacenter | 24 de dezembro de 2020 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-08: Relatórios de incidentes <br> CUEC-10: Contratos de serviço | 24 de dezembro de 2020 |

## <a name="resources"></a>Recursos

- [Nos bastidores: protegendo a infraestrutura que faz o Serviço do Microsoft 365 funcionar](https://download.microsoft.com/download/c/4/5/c45b197e-f0d9-4f40-bd5f-ed8fc7d0cd8c/M365DCSecurityIntro_Whitepaper.pdf)
