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
ms.localizationpriority: medium
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 8ba736fbd6e72963badc3245e11cbed2292cba94
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/12/2021
ms.locfileid: "59158129"
---
# <a name="security-monitoring-overview"></a>Visão geral de monitoramento de segurança

## <a name="what-is-microsofts-strategy-for-monitoring-security"></a>Qual é a estratégia da Microsoft para monitorar a segurança?

A Microsoft se envolve no monitoramento contínuo de segurança de seus sistemas para detectar e responder a ameaças aos serviços online da Microsoft. Nossos princípios principais para monitoramento e alertas de segurança são:

- Robustez: sinais e lógica para detectar vários comportamentos de ataque
- Precisão: alertas significativos para evitar distrações de ruído
- Velocidade: capacidade de capturar invasores rapidamente o suficiente para impedi-los

As soluções baseadas em nuvem, escala e automação são pilares fundamentais de nossa estratégia de monitoramento e resposta. Para evitarmos ataques efetivamente na escala de alguns dos serviços online da Microsoft, nossos sistemas de monitoramento precisam levantar automaticamente alertas altamente precisos em tempo real. Da mesma forma, quando um problema é detectado, precisamos da capacidade de reduzir o risco em escala, não podemos contar com nossa equipe para corrigir manualmente problemas máquina a máquina. Para reduzir os riscos em escala, usamos ferramentas baseadas em nuvem para aplicar automaticamente contramedidas e fornecer ferramentas aos engenheiros para aplicar ações de mitigação aprovadas rapidamente em todo o ambiente.

## <a name="how-do-microsoft-online-services-perform-security-monitoring"></a>Como os serviços online da Microsoft executam o monitoramento de segurança?

Os serviços online da Microsoft usam o log centralizado para coletar e analisar eventos de log para atividades que possam indicar um incidente de segurança. As ferramentas de log centralizadas agregam logs de todos os componentes do sistema, incluindo logs de eventos, logs de aplicativos, logs de controle de acesso e sistemas de detecção de intrusão baseados em rede. Além do registro em log do servidor e dados no nível do aplicativo, a infraestrutura principal é equipada com agentes de segurança personalizados que geram telemetria detalhada e fornecem detecção de intrusão baseada em host. Usamos essa telemetria para monitoramento e análise forense.

Os dados de log e telemetria que coletamos permitem alertas de segurança 24 horas por dia. Nosso sistema de alertas analisa os dados de log conforme eles são carregados, produzindo alertas quase em tempo real. Isso inclui alertas baseados em regras e alertas mais sofisticados com base em modelos de aprendizado de máquina. Nossa lógica de monitoramento vai além dos cenários de ataque genéricos e incorpora reconhecimento profundo da arquitetura e das operações do serviço. Analisamos os dados de monitoramento de segurança para melhorar continuamente nossos modelos para detectar novos tipos de ataques e melhorar a precisão do nosso monitoramento de segurança.

## <a name="how-do-microsoft-online-services-respond-to-security-monitoring-alerts"></a>Como os serviços online da Microsoft respondem aos alertas de monitoramento de segurança?

Quando os eventos de segurança que disparam alertas exigem ação responsiva ou investigação posterior de evidências forenses em todo o serviço, nossas ferramentas baseadas em nuvem permitem uma resposta rápida em todo o ambiente. Essas ferramentas incluem agentes inteligentes e totalmente automatizados que respondem a ameaças detectadas com contramedidas de segurança. Em muitos casos, esses agentes implantam contramedidas automáticas para atenuar detecções de segurança em escala sem intervenção humana. Quando essa resposta não é possível, o sistema de monitoramento de segurança alerta automaticamente os engenheiros de chamada apropriados, que são equipados com um conjunto de ferramentas que permitem que eles ajam em tempo real para mitigar ameaças detectadas em escala. Os possíveis incidentes são escalonados para a equipe de resposta de segurança apropriada da Microsoft e são resolvidos usando o processo de resposta a incidentes de segurança.

## <a name="how-do-microsoft-online-services-monitor-system-availability"></a>Como os serviços online da Microsoft monitoram a disponibilidade do sistema?

A Microsoft monitora ativamente seus sistemas em busca de indicadores de sobreutilização de recursos e uso anormal. O monitoramento de recursos é complementado por redundâncias de serviço para ajudar a evitar o tempo de inatividade inesperado e fornecer aos clientes acesso confiável a produtos e serviços. Os problemas de saúde do serviço online da Microsoft são comunicados prontamente aos clientes por meio do ShD (Painel de Saúde do Serviço).

Os serviços online do Azure e do Dynamics 365 utilizam vários serviços de infraestrutura para monitorar sua disponibilidade de segurança e saúde. A implementação do teste de Transação Sintética (STX) permite que os serviços do Azure e do Dynamics verifiquem a disponibilidade de seus serviços. A estrutura STX foi projetada para dar suporte ao teste automatizado de componentes em serviços em execução e é testada em alertas de falha de site ao vivo. Além disso, o serviço de Monitoramento de Segurança do Azure (ASM) implementou procedimentos de teste sintético centralizado para verificar a função de alertas de segurança conforme esperado em serviços novos e em execução.

## <a name="related-external-regulations--certifications"></a>Regulamentações externas relacionadas & certificações

Os serviços online da Microsoft são regularmente auditados para conformidade com regulamentações e certificações externas. Consulte a tabela a seguir para validação de controles relacionados ao monitoramento de segurança.

### <a name="azure-and-dynamics-365"></a>Azure e Dynamics 365

| **Auditorias externas** | **Section** | **Data do relatório mais recente** |
|:--------|:--------|:------|
| [ISO 27001/27002](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> <br> [Instrução of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7af5304-3a31-40e6-9abb-e26352305d41&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.3: Monitoramento de disponibilidade e planejamento de capacidade | 2 de dezembro de 2020 |
| [ISO 27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Instrução of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a3bca0ac-867d-4204-b66b-13665f5f1e8d&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=25718a8a-f34d-41e1-a95a-c49246508787&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.3: Monitoramento de disponibilidade e planejamento de capacidade <br> A.16.1: Gerenciamento de incidentes e melhorias de segurança da informação | 2 de dezembro de 2020 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b8721ebd-af20-42fe-b22f-8332b0a19517&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | IM-1: Estrutura de gerenciamento de incidentes <br> IM-2: Configuração de detecção de incidentes <br> IM-3: Procedimentos de gerenciamento de incidentes <br> IM-4: Incidente pós-morte <br> VM-1: Log e coleção de eventos de segurança <br> VM-12: Monitoramento de disponibilidade de serviços do Azure <br> VM-4: Investigação de eventos mal-intencionados <br> VM-6: Monitoramento de vulnerabilidades de segurança | 31 de março de 2021 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=234a0f57-83c1-4afc-a586-a0e7a59592f7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=75c8cbf6-e456-473c-a05e-34fea888ec2a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | IM-1: Estrutura de gerenciamento de incidentes <br> IM-2: Configuração de detecção de incidentes <br> IM-3: Procedimentos de gerenciamento de incidentes <br> IM-4: Incidente pós-morte <br> PI-2: Revisão de desempenho do SLA do portal do Azure <br> VM-1: Log e coleção de eventos de segurança <br> VM-12: Monitoramento de disponibilidade de serviços do Azure <br> VM-4: Investigação de eventos mal-intencionados <br> VM-6: Monitoramento de vulnerabilidades de segurança | 31 de março de 2021 |

### <a name="office-365"></a>Office 365

| **Auditorias externas** | **Section** | **Data do relatório mais recente** |
|:--------|:--------|:------|
| [FedRAMP](https://compliance.microsoft.com/compliancemanager) | AC-2: Gerenciamento de contas <br> AC-17: Acesso remoto <br> AU-7: Redução de auditoria e geração de relatório <br> SI-4: Monitoramento do sistema de informações <br> SI-7: Integridade de software, firmware e informações <br> | 24 de setembro de 2020 |
| [ISO 27001/27002/27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> <br> [Instrução of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.3: Monitoramento de disponibilidade e planejamento de capacidade | Abril de 20, 2021 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-19: Alterar monitoramento <br> CA-26: Relatório de incidentes de segurança <br> CA-29: engenheiros de chamada <br> CA-48: log de datacenter | 24 de dezembro de 2020 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-19: Alterar monitoramento <br> CA-26: Relatório de incidentes de segurança <br> CA-29: engenheiros de chamada <br> CA-30: Monitoramento de disponibilidade <br> CA-48: log de datacenter | 24 de dezembro de 2020 |
| [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-08: Relatórios de incidentes <br> CUEC-10: Contratos de serviço | 24 de dezembro de 2020 |

## <a name="resources"></a>Recursos

- [Nos bastidores: protegendo a infraestrutura que faz o Serviço do Microsoft 365 funcionar](https://download.microsoft.com/download/c/4/5/c45b197e-f0d9-4f40-bd5f-ed8fc7d0cd8c/M365DCSecurityIntro_Whitepaper.pdf)
