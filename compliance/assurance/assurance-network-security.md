---
title: Segurança de rede
description: Saiba mais sobre segurança de rede no Microsoft 365
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
ms.openlocfilehash: a2b153b2f2f57a011c28ee65cbe03019cbaa27a1
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51496921"
---
# <a name="network-security-overview"></a>Visão geral de segurança de rede

## <a name="how-does-microsoft-365-secure-the-network-boundary"></a>Como o Microsoft 365 garante o limite de rede?

O Microsoft 365 emprega várias estratégias para proteger seu limite de rede, incluindo detecção e prevenção automatizadas de ataques baseados em rede, dispositivos de firewall especializados e Proteção do Exchange Online (EOP) para proteção anti-spam e anti-malware. Além disso, o Microsoft 365 separa seu ambiente de produção em segmentos de rede logicamente isolados, com apenas a comunicação necessária permitida entre segmentos. O tráfego de rede é protegido usando firewalls de rede adicionais em pontos de limite para ajudar a detectar, evitar e mitigar ataques de rede.

## <a name="how-does-microsoft-365-defend-against-ddos-attacks"></a>Como o Microsoft 365 se defende contra ataques DDoS?

A grande presença da Microsoft na Internet o isola dos efeitos negativos de muitos ataques DDoS (negação de serviço) distribuídos. Instâncias distribuídas de cada serviço do Microsoft 365 e várias rotas para cada serviço limitam o impacto de ataques DDoS contra o sistema. Essa redundância melhora a capacidade do Microsoft 365 de absorver ataques DDoS e aumenta o tempo disponível para detectar e atenuar ataques DDoS antes de afetar a disponibilidade do serviço.

Além da arquitetura de sistema redundante da Microsoft, a Microsoft usa ferramentas sofisticadas de detecção e mitigação para responder a ataques DDoS. Firewalls de finalidade especial monitoram e soltam tráfego indesejado antes que ele cruze o limite para a rede, reduzindo o estresse nos sistemas localizados dentro do limite da rede. Para proteger ainda mais nossos serviços de nuvem, a Microsoft utiliza um sistema de defesa DDoS implantado como parte do Microsoft Azure. O sistema de defesa do Azure DDoS foi projetado para suportar ataques de fora e de outros locatários do Azure.

## <a name="how-does-microsoft-365-protect-users-against-spam-and-malware-being-uploaded-or-sent-through-online-services"></a>Como o Microsoft 365 protege os usuários contra spam e malware sendo carregados ou enviados por meio de serviços online?

O Microsoft 365 cria proteção antimalware em serviços que podem ser vetores de código mal-intencionado, como o Exchange Online e o SharePoint Online. A Proteção do Exchange Online (EOP) verifica todos os emails e anexos de email em busca de malware à medida que entram e saem do sistema, impedindo que mensagens e anexos infectados seja entregue. A filtragem avançada de spam é aplicada automaticamente a mensagens de entrada e de saída para ajudar a impedir que as organizações de clientes recebam e enviem spam. Essa camada de proteção protege contra ataques que aproveitam emails não solicitados ou não autorizados, como ataques de phishing. O SharePoint Online usa o mesmo mecanismo de detecção de vírus para examinar seletivamente os arquivos carregados por malware. Se um arquivo estiver marcado como infectado, os usuários serão impedidos de baixar ou sincronizar o arquivo para proteger os pontos de extremidade do cliente.

## <a name="related-external-regulations--certifications"></a>Regulamentações externas relacionadas & certificações

Os serviços online da Microsoft são regularmente auditados para conformidade com regulamentações e certificações externas. Consulte a tabela a seguir para validação de controles relacionados à segurança da rede.

| **Auditorias externas** | **Section** | **Data do relatório mais recente** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | SC-5: Proteção contra negação de serviço <br> SC-7: Proteção de limite <br> SI-2: Correção de falhas <br> SI-3: Proteção contra código mal-intencionado <br> SI-8: Proteção contra spam | 24 de setembro de 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-27: Verificação de vulnerabilidade | 24 de dezembro de 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-27: Verificação de vulnerabilidade <br> CA-45: Anti-malware | 24 de dezembro de 2020 |