---
title: Segurança da rede
description: Saiba mais sobre a segurança de rede no Microsoft 365
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
ms.openlocfilehash: c063460fdfba44265b3a1504a049a4772b484dff
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/30/2020
ms.locfileid: "49505656"
---
# <a name="network-security-overview"></a>Visão geral da segurança de rede

## <a name="how-does-microsoft-365-secure-the-network-boundary"></a>Como a Microsoft 365 segura o limite da rede?

A Microsoft 365 emprega várias estratégias para proteger seu limite de rede, incluindo detecção e prevenção automatizadas de ataques baseados em rede, dispositivos de firewall especializados e proteção do Exchange Online (EOP) para proteção antispam e antimalware. Além disso, a Microsoft 365 separa seu ambiente de produção em segmentos de rede logicamente isolados, apenas com a comunicação necessária permitida entre segmentos. O tráfego de rede é protegido usando firewalls de rede adicionais em pontos de limite para ajudar a detectar, prevenir e reduzir ataques à rede.

## <a name="how-does-microsoft-365-defend-against-ddos-attacks"></a>Como a Microsoft 365 defende contra ataques de DDoS?

A presença ampla da Internet da Microsoft a protege dos efeitos negativos de vários ataques de DDoS (negação de serviço) distribuídos. Instâncias distribuídas de cada serviço Microsoft 365 e várias rotas para cada serviço limitam o impacto de ataques de DDoS contra o sistema. Essa redundância melhora a capacidade do Microsoft 365 de absorver ataques de DDoS e aumenta a quantidade de tempo disponível para detectar e mitigar os ataques de DDoS antes que eles afetem a disponibilidade do serviço.

Além da arquitetura de sistema redundante da Microsoft, a Microsoft usa ferramentas sofisticadas de detecção e atenuação para responder a ataques de DDoS. Os firewalls de uso especial monitoram e descartam o tráfego indesejado antes de cruzar o limite da rede, reduzindo a carga em sistemas localizados dentro do limite da rede. Para proteger ainda mais nossos serviços em nuvem, a Microsoft utiliza um sistema de defesa contra DDoS implantado como parte do Microsoft Azure. O sistema de defesa de DDoS do Azure foi projetado para resistir a ataques de fora, bem como de outros locatários do Azure.

## <a name="how-does-microsoft-365-protect-users-against-spam-and-malware-being-uploaded-or-sent-through-online-services"></a>Como a Microsoft 365 protege os usuários contra spam e malware sendo carregado ou enviado por meio de serviços online?

A Microsoft 365 cria proteção antimalware em serviços que podem ser vetores de código mal-intencionado, como o Exchange Online e o SharePoint Online. O proteção do Exchange Online (EOP) examina todos os emails e anexos de email em busca de malware conforme eles entram e saem do sistema, impedindo que mensagens e anexos infectados sejam entregues. A filtragem de spam avançada é automaticamente aplicada às mensagens de entrada e de saída para ajudar a impedir que as organizações do cliente recebam e enviem spam. Esta camada de proteção protege contra ataques que se beneficiam de emails não solicitados ou não autorizados, como ataques de phishing. O SharePoint Online usa o mesmo mecanismo de detecção de vírus para examinar seletivamente os arquivos carregados em busca de malware. Se um arquivo estiver marcado como infectado, os usuários serão impedidos de baixar ou sincronizar o arquivo para proteger os pontos de extremidade do cliente.

## <a name="related-external-regulations--certifications"></a>Normas externas relacionadas & certificações

Os serviços online da Microsoft são auditados regularmente para fins de conformidade com regulamentos externos e certificações. Consulte a tabela a seguir para validação de controles relacionados à segurança de rede.

| **Auditorias externas** | **Section** | **Data do relatório mais recente** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | SC-5: negação de serviço de proteção <br> SC-7: proteção de limite <br> SI-2: correção de falha <br> SI-3: proteção de código mal-intencionado <br> SI-8: proteção contra spam | 24 de setembro de 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | AC-27: verificação de vulnerabilidade | 30 de setembro de 2019 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | AC-27: verificação de vulnerabilidade <br> AC-45: anti-malware | 30 de setembro de 2019 |