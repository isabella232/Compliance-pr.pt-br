---
title: Segurança de rede
description: Saiba mais sobre segurança de rede Microsoft 365
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
ms.openlocfilehash: 92da9e7bb2716f61088e02c244cb9905af142ead
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/12/2021
ms.locfileid: "59158367"
---
# <a name="network-security-overview"></a>Visão geral de segurança de rede

## <a name="how-do-microsoft-online-services-secure-the-network-boundary"></a>Como os serviços online da Microsoft garantem o limite de rede?

Os serviços online da Microsoft empregam várias estratégias para proteger seu limite de rede, incluindo detecção e prevenção automatizadas de ataques baseados em rede, dispositivos de firewall especializados e Proteção do Exchange Online (EOP) para proteção anti-spam e anti-malware. Além disso, os serviços online da Microsoft separam seus ambientes de produção em segmentos de rede logicamente isolados, com apenas a comunicação necessária permitida entre segmentos. O tráfego de rede é protegido usando firewalls de rede adicionais em pontos de limite para ajudar a detectar, evitar e mitigar ataques de rede.

## <a name="how-do-microsoft-online-services-defend-against-ddos-attacks"></a>Como os serviços online da Microsoft se defendem contra ataques DDoS?

A grande presença da Microsoft na Internet o isola dos efeitos negativos de muitos ataques DDoS (negação de serviço) distribuídos. Instâncias distribuídas de cada serviço online da Microsoft e várias rotas para cada serviço limitam o impacto de ataques DDoS contra o sistema. Essa redundância melhora a capacidade dos serviços online da Microsoft de absorver ataques DDoS e aumenta o tempo disponível para detectar e mitigar ataques DDoS antes de afetar a disponibilidade do serviço.

Além da arquitetura de sistema redundante da Microsoft, a Microsoft usa ferramentas sofisticadas de detecção e mitigação para responder a ataques DDoS. Firewalls de finalidade especial monitoram e soltam tráfego indesejado antes que ele cruze o limite para a rede, reduzindo o estresse nos sistemas localizados dentro do limite da rede. Para proteger ainda mais nossos serviços de nuvem, a Microsoft utiliza um sistema de defesa DDoS implantado como parte do Microsoft Azure. O sistema de defesa do Azure DDoS foi projetado para suportar ataques de fora e de outros locatários do Azure.

## <a name="how-does-microsoft-protect-users-against-spam-and-malware-being-uploaded-or-sent-through-online-services"></a>Como a Microsoft protege os usuários contra spam e malware que estão sendo carregados ou enviados por meio de serviços online?

Os serviços online da Microsoft constroem proteção antimalware em serviços que podem ser vetores de código mal-intencionado, como Exchange Online e SharePoint Online. Proteção do Exchange Online (EOP) verifica todos os emails e anexos de email para malware à medida que entram e saem do sistema, impedindo que mensagens e anexos infectados seja entregue. A filtragem avançada de spam é aplicada automaticamente a mensagens de entrada e de saída para ajudar a impedir que as organizações de clientes recebam e enviem spam. Essa camada de proteção protege contra ataques que aproveitam emails não solicitados ou não autorizados, como ataques de phishing. SharePoint Online usa o mesmo mecanismo de detecção de vírus para examinar seletivamente arquivos carregados por malware. Se um arquivo estiver marcado como infectado, os usuários serão impedidos de baixar ou sincronizar o arquivo para proteger os pontos de extremidade do cliente. Da mesma forma, o Azure compara hashes relacionados aos arquivos carregados no Azure Armazenamento aos hashes de malware conhecido. Quando as combinações são encontradas, um alerta é gerado no Centro de Segurança do Azure, onde uma decisão é tomada sobre a legitimidade do alerta e como ele deve ser resolvido.

## <a name="related-external-regulations--certifications"></a>Regulamentações externas relacionadas & certificações

Os serviços online da Microsoft são regularmente auditados para conformidade com regulamentações e certificações externas. Consulte a tabela a seguir para validação de controles relacionados à segurança da rede.

### <a name="azure-and-dynamics-365"></a>Azure e Dynamics 365

| **Auditorias externas** | **Section** | **Data do relatório mais recente** |
|:--------------------|:------------|:-----------------------|
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b8721ebd-af20-42fe-b22f-8332b0a19517&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=234a0f57-83c1-4afc-a586-a0e7a59592f7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=75c8cbf6-e456-473c-a05e-34fea888ec2a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | VM-1: Log de eventos de segurança <br> VM-3: Detecção e monitoramento de intrusões <br> VM-4: Investigação de eventos mal-intencionados <br> VM-6: Verificação de vulnerabilidade <br> VM-7: Configuração do dispositivo de rede <br> VM-8: Teste de penetração <br> VM-9: log de eventos de segurança de dispositivo de rede <br> VM-13: Mitigação de vulnerabilidade de dispositivo de rede | 31 de março. 2021 |

### <a name="office-365"></a>Office 365

| **Auditorias externas** | **Section** | **Data do relatório mais recente** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP](https://compliance.microsoft.com/compliancemanager) | SC-5: Proteção contra negação de serviço <br> SC-7: Proteção de limite <br> SI-2: Correção de falhas <br> SI-3: Proteção contra código mal-intencionado <br> SI-8: Proteção contra spam | 24 de setembro de 2020 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-27: Verificação de vulnerabilidade | 24 de dezembro de 2020 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-27: Verificação de vulnerabilidade <br> CA-45: Anti-malware | 24 de dezembro de 2020 |