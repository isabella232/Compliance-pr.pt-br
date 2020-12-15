---
title: Resiliência e continuidade
description: Saiba mais sobre resiliência e continuidade no Microsoft 365
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
ms.openlocfilehash: 2cc3f35a9d109a1a84159de8d0518f58270e3fe9
ms.sourcegitcommit: 1dc97ae3f0511cb1a41565da56e725bbe0cb013c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "49671176"
---
# <a name="resiliency-and-continuity-overview"></a>Visão geral de resiliência e continuidade

## <a name="how-does-microsoft-ensure-business-continuity-in-the-case-of-a-disaster-or-other-threat-to-service-availability"></a>Como a Microsoft garante a continuidade de negócios no caso de um desastre ou outra ameaça à disponibilidade do serviço?

A equipe do EBCM (Enterprise Business Continuity Management) da Microsoft supervisiona as atividades de gerenciamento de continuidade de negócios e de recuperação de desastres nos serviços e nas ofertas de nuvem da Microsoft. Representantes das unidades de negócios da Microsoft, como o Microsoft 365, coordenam com a equipe do EBCM para desenvolver planos de continuidade de negócios e validar a conformidade com os requisitos de continuidade de negócios.

O núcleo da nossa metodologia de gerenciamento de continuidade de negócios (BCM) é o ciclo de vida do BCM. Esse processo de três fases foi projetado para ser adaptável, para que possa ser implementado por uma ampla variedade de modelos de negócios na Microsoft. Ele começa com uma fase de **avaliação** para identificar processos e objetivos críticos que devem ser incluídos no programa de continuidade de negócios. A fase de avaliação também requer uma BIA (análise de impacto de negócios). A fase de **planejamento** enfoca o desenvolvimento e a implementação de estratégias de resiliência e recuperação, além de documentar-as em planos de continuidade de negócios oficiais. Por fim, a **validação de recursos** testa os planos de continuidade de negócios e suas implementações para verificar a eficácia e identificar possíveis aprimoramentos.

A estratégia de continuidade de negócios do Microsoft 365 aproveita a redundância de hardware, rede e Data Center. A replicação de dados entre data centers oferece alta disponibilidade e confiabilidade no caso de um incidente catastrófico. Ele também aumenta a resiliência para incidentes mundane como falha isolada de hardware ou corrupção de dados.

## <a name="how-does-microsoft-test-business-continuity-and-disaster-recovery-plans"></a>Como a Microsoft testa a continuidade dos negócios e os planos de recuperação de desastres?

A política do EBCM (Enterprise Business Continuity Management) da Microsoft determina que todos os planos de continuidade de negócios e recuperação de desastres da Microsoft devem ser testados, atualizados e revisados anualmente. Os serviços 365 da Microsoft testam seus planos de continuidade de negócios pelo menos anualmente por políticas do EBCM. Após os relatórios de ação serem criados e revisados para validar, testar os resultados e informar as atualizações de plano em resposta a quaisquer problemas descobertos durante o teste.

Para validar as estratégias de resiliência e recuperação em uma ampla variedade de possíveis incidentes, o programa EBCM define várias categorias de cenários de teste que afetam pessoas, locais e tecnologia. O nível de validação necessário para cada serviço é baseado na criticalidade do serviço, com serviços mais críticos recebendo mais rigorosa validação. Cada equipe de serviço do Microsoft 365 testa o plano de continuidade de negócios de acordo com as diretrizes do EBCM para medir a eficácia do plano e a preparação da equipe de serviço para executar o plano.

Por EBCM diretrizes, as revisões anuais de planos de continuidade de negócios e a validação de recursos devem ocorrer dentro de 12 meses da última revisão. A validação de recursos deve incluir a revisão da documentação de suporte, como o BIA, para garantir que ela permaneça precisa. A Microsoft faz resultados de validação de recursos para os serviços do Microsoft 365 disponíveis para nossos clientes por meio de relatórios trimestrais.

## <a name="how-does-microsoft-365-ensure-system-capacity-meets-demand"></a>Como a Microsoft 365 garante que a capacidade do sistema atenda à demanda?

O planejamento de capacidade ajuda as equipes de serviço a alocar os recursos necessários para suportar a disponibilidade do serviço Microsoft 365. O planejamento regular da capacidade é necessário como parte do programa EBCM da Microsoft. As equipes de serviço analisam os dados de capacidade durante revisões trimestrais, bem como durante situações de emergência que garantem uma análise adicional da capacidade.

Os dados brutos para planejamento de capacidade são mantidos por cada equipe de serviço e incluem métricas como processamento do sistema, memória e capacidade de hardware. Revisões agendadas use um modelo da capacidade atual do sistema e teste-o em relação às necessidades projetadas em situações de emergência. Se o modelo indica intervalos de capacidade, as alterações propostas para a capacidade do sistema serão enviadas à liderança da equipe de serviço para revisão. As alterações aprovadas são incorporadas em um novo modelo antes da implementação por engenheiros de equipe de serviço.

## <a name="how-does-microsoft-365-maintain-service-availability-during-routine-system-failures"></a>Como a Microsoft 365 mantém a disponibilidade do serviço durante falhas de sistema de rotina?

A Microsoft 365 Obtém resiliência de serviço por meio de arquitetura redundante, replicação de dados e verificação de integridade automatizada. A arquitetura redundante envolve a implantação de várias instâncias de um serviço em um hardware geograficamente e fisicamente separado, fornecendo maior tolerância a falhas para os serviços do Microsoft 365. A replicação de dados garante que haja sempre várias cópias de dados do cliente em diferentes zonas de falha, permitindo que dados críticos do cliente sejam recuperados se estiverem corrompidos, perdidos ou excluídos acidentalmente pelo cliente. A verificação de integridade automatizada aumenta a disponibilidade dos dados, restaurando automaticamente os dados afetados por vários tipos de danos físicos ou lógicos.

## <a name="related-external-regulations--certifications"></a>Normas externas relacionadas & certificações

Os serviços online da Microsoft são auditados regularmente para fins de conformidade com regulamentos externos e certificações. Consulte a tabela a seguir para validação de controles relacionados à resiliência e continuidade.

| **Auditorias externas** | **Section** | **Data do relatório mais recente** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | CP-2: plano de contingência <br> CP-3: treinamento de contingência <br> CP-4: teste do plano de contingência <br> CP-6: local de armazenamento alternativo <br> CP-7: site de processamento alternativo <br> CP-9: backup do sistema de informações <br> CP-10: recuperação e reconstituição do sistema de informações | 24 de setembro de 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaração de aplicabilidade](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 17.1: continuidade de segurança de informações <br> A. 17.2: redundâncias | 22 de fevereiro de 2020 |
| [ISO 22301 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=13951eb3-6339-4629-b80d-dd0d43812fe7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=2bb29cc0-53e7-4a53-a9de-871316e1b80c&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | Todos os controles | 18 de março de 2019 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | AC-49: políticas de backup <br> AC-50: continuidade de negócios <br> AC-51: replicação de dados | 30 de setembro de 2019 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | AC-49: políticas de backup <br> AC-50: continuidade de negócios <br> AC-51: replicação de dados | 30 de setembro de 2019 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=9df8b99b-96ce-49a9-bff4-268031dcc9a6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CUEC-09: restauração de email do EXO | 30 de setembro de 2019 |

## <a name="resources"></a>Recursos

- [Whitepaper do programa de gerenciamento de continuidade de negócios da Microsoft](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=64f922a6-d624-40dd-a8ae-6f996b5186f3&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f) 
- [Microsoft Cloud EBCM e relatório de validação do plano de recuperação de desastres: FY21 Q1 e Q2](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=b4181ab3-b03d-4a62-b396-4bfd1c98ddb0&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)

## <a name="legal-disclaimer"></a>Isenção de responsabilidade legal

- [Aviso de isenção de responsabilidade legal da continuidade de negócios empresariais](assurance-ebcm-legal-disclaimer.md)