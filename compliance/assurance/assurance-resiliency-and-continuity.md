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
hideEdit: true
ms.openlocfilehash: 9f63630ac0e9c7a1b68d65c738e88b55f351a3ef
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51496890"
---
# <a name="resiliency-and-continuity-overview"></a>Visão geral da resiliência e continuidade

## <a name="how-does-microsoft-ensure-business-continuity-in-the-case-of-a-disaster-or-other-threat-to-service-availability"></a>Como a Microsoft garante a continuidade dos negócios no caso de um desastre ou outra ameaça à disponibilidade do serviço?

A equipe do Enterprise Business Continuity Management (EBCM) da Microsoft supervisiona as atividades de gerenciamento de continuidade de negócios e recuperação de desastres nos serviços microsoft e ofertas de nuvem. Representantes das unidades de negócios da Microsoft, como o Microsoft 365, coordenam com a equipe do EBCM para desenvolver planos de continuidade de negócios e validar a conformidade com os requisitos de continuidade de negócios.

No centro de nossa metodologia de Gerenciamento de Continuidade de Negócios (BCM) está o ciclo de vida do BCM. Esse processo de três fases foi projetado para ser adaptável para que possa ser implementado por uma ampla variedade de modelos de negócios na Microsoft. Ele começa com uma fase **de Avaliação** para identificar processos críticos e objetivos que devem ser incluídos no programa de continuidade de negócios. A fase de Avaliação também requer uma Análise de Impacto empresarial (BIA). A **fase planejamento** se concentra no desenvolvimento e implementação de estratégias de resiliência e recuperação, bem como documentá-las em planos oficiais de continuidade de negócios. Por fim, **a Validação de Funcionalidade** testa planos de continuidade de negócios e suas implementações para verificar a eficácia e identificar possíveis melhorias.

A estratégia de continuidade de negócios do Microsoft 365 aproveita a redundância de hardware, rede e datacenter. A replicação de dados entre datacenters oferece alta disponibilidade e confiabilidade no caso de um incidente catastrófico. Ele também aumenta a resiliência para incidentes mundane, como falha de hardware isolado ou corrupção de dados.

## <a name="how-does-microsoft-test-business-continuity-and-disaster-recovery-plans"></a>Como a Microsoft testa planos de continuidade de negócios e recuperação de desastres?

A política enterprise business continuity management (EBCM) da Microsoft estipula que todos os planos de continuidade de negócios e recuperação de desastres da Microsoft devem ser testados, atualizados e revisados anualmente. Os serviços do Microsoft 365 testam seus planos de continuidade de negócios pelo menos anualmente por políticas de EBCM. Depois que os relatórios de ação são criados e revisados para validar, testar resultados e informar as atualizações do plano em resposta a quaisquer problemas descobertos durante o teste.

Para validar estratégias de resiliência e recuperação em uma ampla variedade de possíveis incidentes, o Programa EBCM define várias categorias de cenários de teste que afetam pessoas, locais e tecnologia. O nível de validação necessário para cada serviço baseia-se na criticidade do serviço, com serviços mais críticos recebendo validação mais rigorosa. Cada equipe de serviço do Microsoft 365 testa seu plano de continuidade de negócios de acordo com as diretrizes do EBCM para medir a eficácia do plano e a prontidão da equipe de serviço para executar o plano.

De acordo com as diretrizes do EBCM, as análises anuais de planos de continuidade de negócios e validação de funcionalidade devem ocorrer dentro de 12 meses após a última revisão. A validação de funcionalidade deve incluir a revisão da documentação de suporte, como a BIA, para garantir que ela permaneça precisa. A Microsoft disponibiliza resultados de validação de recursos para selecionar serviços do Microsoft 365 para nossos clientes por meio de relatórios trimestrais.

## <a name="how-does-microsoft-365-ensure-system-capacity-meets-demand"></a>Como o Microsoft 365 garante que a capacidade do sistema atenda à demanda?

O planejamento de capacidade ajuda as equipes de serviço a alocar os recursos necessários para dar suporte à disponibilidade de serviço do Microsoft 365. O planejamento de capacidade regular é necessário como parte do programa EBCM da Microsoft. As equipes de serviço analisam dados de capacidade durante análises trimestrais, bem como durante situações de emergência que garantem uma revisão de capacidade adicional.

Os dados brutos para planejamento de capacidade são mantidos por cada equipe de serviço e incluem métricas como processamento do sistema, memória e capacidade de hardware. As análises agendadas usam um modelo da capacidade atual do sistema e testam-no em relação às necessidades projetadas em situações de emergência. Se o modelo indicar lacunas de capacidade, as alterações propostas à capacidade do sistema serão enviadas à liderança da equipe de serviço para revisão. As alterações aprovadas são incorporadas a um novo modelo antes da implementação pelos engenheiros de equipe de serviço.

## <a name="how-does-microsoft-365-maintain-service-availability-during-routine-system-failures"></a>Como o Microsoft 365 mantém a disponibilidade do serviço durante falhas de rotina do sistema?

O Microsoft 365 atinge a resiliência do serviço por meio de arquitetura redundante, replicação de dados e verificação de integridade automatizada. A arquitetura redundante envolve a implantação de várias instâncias de um serviço em hardware geograficamente e fisicamente separado, fornecendo maior tolerância a falhas para serviços do Microsoft 365. A replicação de dados garante que sempre haja várias cópias de dados do cliente em diferentes zonas de falha, permitindo que dados críticos do cliente sejam recuperados se corrompidos, perdidos ou até mesmo excluídos acidentalmente pelo cliente. A verificação automatizada de integridade aumenta a disponibilidade de dados restaurando automaticamente os dados afetados por vários tipos de corrupção física ou lógica.

## <a name="related-external-regulations--certifications"></a>Regulamentações externas relacionadas & certificações

Os serviços online da Microsoft são regularmente auditados para conformidade com regulamentações e certificações externas. Consulte a tabela a seguir para validação de controles relacionados à resiliência e continuidade.

| **Auditorias externas** | **Section** | **Data do relatório mais recente** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | CP-2: Plano de contingência <br> CP-3: Treinamento de contingência <br> CP-4: Teste de plano de contingência <br> CP-6: site de armazenamento alternativo <br> CP-7: site de processamento alternativo <br> CP-9: Backup do sistema de informações <br> CP-10: Recuperação e reconstituição do sistema de informações | 24 de setembro de 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Instrução of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.17.1: Continuidade da segurança da informação <br> A.17.2: Redundâncias | 22 de fevereiro de 2020 |
| [ISO 22301 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=13951eb3-6339-4629-b80d-dd0d43812fe7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=2bb29cc0-53e7-4a53-a9de-871316e1b80c&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | Todos os controles | 18 de março de 2019 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-49: Políticas de backup <br> CA-50: Continuidade de negócios <br> CA-51: Replicação de dados | 24 de dezembro de 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-49: Políticas de backup <br> CA-50: Continuidade de negócios <br> CA-51: Replicação de dados | 24 de dezembro de 2020 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-09: restauração de email do EXO | 24 de dezembro de 2020 |

## <a name="resources"></a>Recursos

- [Whitepaper do Programa de Gerenciamento de Continuidade de Negócios da Microsoft Enterprise](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=64f922a6-d624-40dd-a8ae-6f996b5186f3&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f) 
- [Relatório de validação do Plano de Recuperação de Desastres e EBCM do Microsoft Cloud: FY21 Q1 e Q2](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=b4181ab3-b03d-4a62-b396-4bfd1c98ddb0&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)

## <a name="legal-disclaimer"></a>Aviso de isenção de responsabilidade legal

- [Aviso de isenção de responsabilidade legal da continuidade de negócios empresariais](assurance-ebcm-legal-disclaimer.md)