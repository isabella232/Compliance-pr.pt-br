---
title: Visão geral do gerenciamento de incidentes
description: Saiba mais sobre o gerenciamento de incidentes no Microsoft 365
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
ms.openlocfilehash: 6b5c77a2a81f8231ad620fbc40205457c6ba1a49
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/30/2020
ms.locfileid: "49505674"
---
# <a name="incident-management-overview"></a>Visão geral do gerenciamento de incidentes

## <a name="what-is-a-security-incident"></a>O que é um incidente de segurança?

A Microsoft define um incidente de segurança em seus serviços online como uma violação confirmada de segurança que leva à destruição acidental ou ilegal, perda, alteração, divulgação não autorizada ou acesso a dados do cliente ou dados pessoais durante o processamento da Microsoft. Por exemplo, o acesso não autorizado à infraestrutura do Microsoft 365 e aos dados do cliente constituiria um incidente de segurança, enquanto os eventos de conformidade que não afetam a confidencialidade, integridade ou disponibilidade de serviços ou dados do cliente não são considerados incidentes de segurança.

## <a name="how-does-microsoft-respond-to-security-incidents"></a>Como a Microsoft responde a incidentes de segurança?

Sempre que houver um incidente de segurança, a Microsoft se empenhará em responder com rapidez e eficácia para proteger os serviços da Microsoft e os dados dos clientes. A Microsoft emprega uma estratégia de resposta a incidentes projetada para investigar, conter e remover ameaças à segurança com rapidez e eficiência.

Os serviços de nuvem da Microsoft são continuamente monitorados quanto a sinais de comprometimento. Além do monitoramento e alerta automáticos de segurança, todos os funcionários recebem treinamento anual para reconhecer e relatar os sinais de possíveis incidentes de segurança. Qualquer atividade suspeita detectada por funcionários, clientes ou ferramentas de monitoramento de segurança é escalonada para equipes de resposta de segurança específicas de serviço para investigação. Todas as equipes de operações de serviço, incluindo equipes de resposta de segurança específicas de serviço, mantêm uma rotação de chamadas profunda para garantir que os recursos estejam disponíveis para a resposta de incidentes 24x7x365. Nossas rotações de chamadas permitem que a Microsoft monte uma resposta de incidente efetiva a qualquer momento ou escala, incluindo eventos disseminados ou simultâneos.

Quando atividades suspeitas são detectadas e escalonadas, as equipes de resposta de segurança específicas do serviço iniciam um processo de **análise, contenção, erradicação e recuperação**. Essas equipes coordenam a análise de possíveis incidentes para determinar seu escopo, incluindo qualquer impacto para os clientes ou dados do cliente. Com base nessa análise, as equipes de resposta de segurança específicas do serviço trabalham com equipes de serviço impactadas para desenvolver um plano para conter a ameaça e minimizar o impacto do incidente, erradicar a ameaça do ambiente e recuperar totalmente para um estado seguro conhecido. As equipes de serviço relevantes implementam o plano com suporte de equipes de resposta de segurança específicas de serviço para garantir que a ameaça seja eliminada com êxito e os serviços afetados passam por uma recuperação completa.

Depois que um incidente é resolvido, as equipes de serviço implementam as lições aprendidas do incidente para prevenir, detectar e responder a incidentes semelhantes no futuro. Selecionar incidentes de segurança, especialmente aqueles que têm impacto no cliente ou resultam em uma violação de dados, passam por um incidente completo post-mortem. O post-morte foi projetado para identificar lapsos técnicos, falhas de procedimentos, erros manuais e outras falhas de processo que possam ter contribuído com o incidente ou que foram identificados durante o processo de resposta a incidentes. Os aprimoramentos identificados durante o post-mortem são implementados com a coordenação de equipes de resposta de segurança específicas de serviço para ajudar a evitar futuros incidentes e aprimorar os recursos de detecção e resposta.

## <a name="how-and-when-are-customers-notified-of-security-or-privacy-incidents"></a>Como e quando os clientes são notificados sobre incidentes de segurança ou privacidade?

Sempre que a Microsoft ficar ciente de uma violação de segurança envolvendo perda não autorizada, divulgação ou modificação de dados do cliente, a Microsoft notifica os clientes afetados dentro de 72 horas, conforme descrito no adendo de proteção de dados (DPA) dos termos dos serviços online (OST). O compromisso da linha do tempo de notificação começa quando ocorre a declaração de incidentes de segurança oficial. Após declarar um incidente de segurança, o processo de notificação ocorrerá como expeditiously possível, sem atraso inesperado.

As notificações incluem uma descrição da natureza da violação, o impacto aproximado do usuário e as etapas de mitigação (se aplicável). Se a investigação da Microsoft não for concluída no momento da notificação inicial, a notificação também indicará as próximas etapas e linhas do tempo para comunicação subsequente.

Se um cliente ficar ciente de um incidente que pode ter um impacto no Microsoft, incluindo, mas não se limitar a uma violação de dados, o cliente será responsável por notificar imediatamente a Microsoft sobre o incidente, conforme definido no DPA.

## <a name="related-external-regulations--certifications"></a>Normas externas relacionadas & certificações

Os serviços online da Microsoft são auditados regularmente para fins de conformidade com regulamentos externos e certificações. Consulte a tabela a seguir para validação de controles relacionados ao gerenciamento de incidentes.

| **Auditorias externas** | **Section** | **Data do relatório mais recente** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | IV-4: tratamento de incidentes <br> IV-6: relatório de incidentes <br> IV-8: plano de resposta a incidentes | 24 de setembro de 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaração de aplicabilidade](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 16.1: gerenciamento de incidentes e melhorias de segurança de informações | 22 de fevereiro de 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaração de aplicabilidade](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 16.1: gerenciamento de incidentes e melhorias de segurança de informações | 22 de fevereiro de 2020 |
| [ISO 27018 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaração de aplicabilidade](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=43e89534-f48d-42ea-a7a7-3523ff516036&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 10.1: notificação de uma violação de dados envolvendo PII  | 22 de fevereiro de 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | AC-26: relatórios de incidentes de segurança <br> AC-47: resposta a incidentes | 30 de setembro de 2019 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | AC-12: contratos de nível de serviço (SLAs) <br> AC-13: guias de resposta a incidentes <br> AC-15: notificações de integridade do serviço  <br>  <br> AC-26: relatórios de incidentes de segurança <br> CA – 29: engenheiros em chamada <br> AC-47: resposta a incidentes | 30 de setembro de 2019 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=9df8b99b-96ce-49a9-bff4-268031dcc9a6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CUEC-08: relatórios de incidentes  | 30 de setembro de 2019  |

## <a name="resources"></a>Recursos

- [Termos de serviços online (OST)](https://www.microsoft.com/licensing/product-licensing/products)
- [Adendo de proteção de dados (DPA)](https://www.microsoft.com/licensing/product-licensing/products)
- [Orientações de implementação do Microsoft Cloud Incident Management para Azure e Office 365](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=a8a7cb87-9710-4d09-8748-0835b6754e95&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)
- [Office 365-avaliação de vulnerabilidade de terceiros do Office 365-2019](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=e85e478f-2491-435d-9c1b-2f0ad7ca8e56&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_Pen_Test_and_Security_Assessments)
