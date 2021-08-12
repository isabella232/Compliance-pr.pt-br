---
title: Visão geral do gerenciamento de incidentes
description: Saiba mais sobre o gerenciamento de incidentes Microsoft 365
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
ms.openlocfilehash: a699f3fbaeded6922ec6c82aa732ed52474f936b2d6a8391650474064334249c
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/05/2021
ms.locfileid: "54290989"
---
# <a name="incident-management-overview"></a>Visão geral do gerenciamento de incidentes

## <a name="what-is-a-security-incident"></a>O que é um incidente de segurança?

A Microsoft define um incidente de segurança em sua serviços online como uma violação confirmada de segurança que leva à destruição acidental ou ilegal, à perda, à alteração, à divulgação não autorizada ou ao acesso aos dados do cliente ou aos dados pessoais durante o processamento pela Microsoft. Por exemplo, o acesso não autorizado à infraestrutura de serviços online da Microsoft e à filtragem de dados do cliente constituiria um incidente de segurança, enquanto os eventos de conformidade que não afetam a confidencialidade, a integridade ou a disponibilidade de serviços ou dados do cliente não são considerados incidentes de segurança.

## <a name="how-does-microsoft-respond-to-security-incidents"></a>Como a Microsoft responde a incidentes de segurança?

Sempre que houver um incidente de segurança, a Microsoft se esforça para responder de forma rápida e eficaz para proteger serviços Microsoft dados do cliente. A Microsoft emprega uma estratégia de resposta a incidentes projetada para investigar, conter e remover ameaças de segurança de forma rápida e eficiente.

Os serviços de nuvem da Microsoft são monitorados continuamente em busca de sinais de comprometimento. Além do monitoramento e alertas de segurança automatizados, todos os funcionários recebem treinamento anual para reconhecer e relatar sinais de possíveis incidentes de segurança. Qualquer atividade suspeita detectada por funcionários, clientes ou ferramentas de monitoramento de segurança é escalonada para equipes de Resposta de Segurança específicas do serviço para investigação. Todas as equipes de operações de serviço, incluindo equipes de Resposta de Segurança específicas do serviço, mantêm uma rotação profunda ao chamar para garantir que os recursos estão disponíveis para a resposta a incidentes 24x7x365. Nossas rotações de chamada permitem que a Microsoft monte uma resposta efetiva a incidentes a qualquer momento ou escala, incluindo eventos generalizados ou simultâneos.

Quando atividades suspeitas são detectadas e escalonadas, as equipes de Resposta de Segurança específicas do serviço iniciam um processo de **análise, contenção, erradicação e recuperação.** Essas equipes coordenam a análise do possível incidente para determinar seu escopo, incluindo qualquer impacto nos clientes ou dados do cliente. Com base nessa análise, as equipes de Resposta de Segurança específicas do serviço trabalham com equipes de serviço impactadas para desenvolver um plano para conter a ameaça e minimizar o impacto do incidente, erradicar a ameaça do ambiente e recuperar totalmente para um estado seguro conhecido. As equipes de serviço relevantes implementam o plano com suporte de equipes de Resposta de Segurança específicas do serviço para garantir que a ameaça seja eliminada com êxito e os serviços afetados passam por uma recuperação completa.

Após a solução de um incidente, as equipes de serviço implementam as lições aprendidas com o incidente para evitar, detectar e responder melhor a incidentes semelhantes no futuro. Selecione incidentes de segurança, especialmente aqueles que são afetados pelo cliente ou resultam em uma violação de dados, passam por um incidente completo após a morte. O post-mortem foi projetado para identificar deslizes técnicos, falhas de procedimento, erros manuais e outras falhas de processo que podem ter contribuído para o incidente ou que foram identificados durante o processo de resposta a incidentes. Melhorias identificadas durante a pós-morte são implementadas com a coordenação das equipes de Resposta de Segurança específicas do serviço para ajudar a evitar incidentes futuros e melhorar os recursos de detecção e resposta.

## <a name="how-and-when-are-customers-notified-of-security-or-privacy-incidents"></a>Como e quando os clientes são notificados de incidentes de segurança ou privacidade?

Sempre que a Microsoft se torna ciente de uma violação de segurança envolvendo perda, divulgação ou modificação não autorizada de dados do cliente, a Microsoft notifica os clientes afetados dentro de 72 horas, conforme descrito no DPA (Data Protection Addendum) dos Termos de Serviços Online (OST). O compromisso com a linha do tempo de notificação começa quando ocorre a declaração oficial de incidentes de segurança. Ao declarar um incidente de segurança, o processo de notificação ocorre o mais rápido possível, sem atrasos indevidos.

As notificações incluem uma descrição da natureza da violação, do impacto aproximado do usuário e das etapas de mitigação (se aplicável). Se a investigação da Microsoft não estiver concluída no momento da notificação inicial, a notificação também indicará as próximas etapas e cronogramas para comunicação subsequente.

Se um cliente se tornar ciente de um incidente que pode ter um impacto sobre a Microsoft, incluindo, mas não se limitando a uma violação de dados, o cliente será responsável por notificar prontamente a Microsoft sobre o incidente, conforme definido na DPA.

## <a name="related-external-regulations--certifications"></a>Regulamentações externas relacionadas & certificações

Os serviços online da Microsoft são regularmente auditados para conformidade com regulamentações e certificações externas. Consulte a tabela a seguir para validação de controles relacionados ao gerenciamento de incidentes.

### <a name="azure-and-dynamics-365"></a>Azure e Dynamics 365

| **Auditorias externas** | **Section** | **Data do relatório mais recente** |
|:--------------------|:------------|:-----------------------|
| [ISO 27001/27002](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Instrução of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7af5304-3a31-40e6-9abb-e26352305d41&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.16.1: Gerenciamento de incidentes e melhorias de segurança da informação | 2 de dezembro de 2021 |
| [ISO 27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Instrução of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a3bca0ac-867d-4204-b66b-13665f5f1e8d&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=25718a8a-f34d-41e1-a95a-c49246508787&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.16.1: Gerenciamento de incidentes e melhorias de segurança da informação | 2 de dezembro de 2021 |
| [ISO 27018](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Instrução of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=56904fc3-0942-4ff5-9eef-7cabc751a25c&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.9.1: Notificação de uma violação de dados envolvendo PII  | 2 de dezembro de 2021 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b8721ebd-af20-42fe-b22f-8332b0a19517&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | IM-1: Estrutura de gerenciamento de incidentes <br> IM-2: mecanismos de detecção e alertas <br> IM-3: Execução de resposta a incidentes <br> IM-4: Incidente pós-morte <br> IM-6: Teste de resposta a incidentes <br> OA-7: acesso de engenheiro de chamada | 31 de março de 2021 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=234a0f57-83c1-4afc-a586-a0e7a59592f7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=75c8cbf6-e456-473c-a05e-34fea888ec2a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CCM-9: Procedimentos forenses <br> CUEC: Relatórios de incidentes <br> IM-1: Estrutura de gerenciamento de incidentes <br> IM-2: mecanismos de detecção e alertas <br> IM-3: Execução de resposta a incidentes <br> IM-4: Incidente pós-morte <br> IM-6: Teste de resposta a incidentes <br> OA-7: acesso de engenheiro de chamada <br> SOC2-6: site de Suporte ao Cliente <br> SOC2-9: Painéis de serviço | 31 de março de 2021 |

### <a name="office-365"></a>Office 365

| **Auditorias externas** | **Section** | **Data do relatório mais recente** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP](https://compliance.microsoft.com/compliancemanager) | IR-4: Tratamento de incidentes <br> IR-6: Relatório de incidentes <br> IR-8: Plano de resposta a incidentes | 24 de setembro de 2020 |
| [ISO 27001/27002/27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Instrução of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.16.1: Gerenciamento de incidentes e melhorias de segurança da informação | Abril de 20, 2021 |
| [ISO 27018](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Instrução of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.9.1: Notificação de uma violação de dados envolvendo PII  | Abril de 20, 2021 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-26: Relatório de incidentes de segurança <br> CA-47: Resposta a incidentes | 24 de dezembro de 2020 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-12: Contratos de nível de serviço (SLAs) <br> CA-13: Guias de resposta a incidentes <br> CA-15: Notificações de saúde do serviço  <br>  <br> CA-26: Relatório de incidentes de segurança <br> CA-29: engenheiros de chamada <br> CA-47: Resposta a incidentes | 24 de dezembro de 2020 |
| [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-08: Relatórios de incidentes  | 24 de dezembro de 2020  |

## <a name="resources"></a>Recursos

- [Termos de serviços online (OST)](https://www.microsoft.com/licensing/product-licensing/products)
- [DPA (Data Protection Addendum)](https://www.microsoft.com/licensing/product-licensing/products)
- [Diretrizes de implementação de gerenciamento de incidentes na nuvem da Microsoft para o Azure e Office 365](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=a8a7cb87-9710-4d09-8748-0835b6754e95&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)
- [Office 365 - Avaliação de vulnerabilidade de terceiros do Office 365 - 2019](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=e85e478f-2491-435d-9c1b-2f0ad7ca8e56&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_Pen_Test_and_Security_Assessments)
