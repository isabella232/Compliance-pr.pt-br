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
ms.openlocfilehash: ff1719ce931a50904fb6b7e6069cd29a1883aa90
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2021
ms.locfileid: "58946927"
---
# <a name="resiliency-and-continuity-overview"></a>Visão geral da resiliência e continuidade

## <a name="how-does-microsoft-ensure-business-continuity-if-a-disaster-or-other-threat-to-service-availability-occurs"></a>Como a Microsoft garante a continuidade dos negócios se ocorrer um desastre ou outra ameaça à disponibilidade do serviço?

A equipe Enterprise Business Continuity Management (EBCM) da Microsoft supervisiona as atividades de gerenciamento de continuidade de negócios e recuperação de desastres em serviços Microsoft e ofertas de nuvem. Representantes das unidades de negócios da Microsoft coordenam com a equipe do EBCM para desenvolver planos de continuidade de negócios e validar a conformidade com os requisitos de continuidade de negócios.

O ciclo de vida do BCM (Gerenciamento de Continuidade de Negócios) está no centro da metodologia BCM. Esse processo de três fases foi projetado para ser adaptável para que possa ser implementado por uma ampla variedade de modelos de negócios na Microsoft. Ele começa com uma fase **de Avaliação** para identificar processos críticos e objetivos que devem ser incluídos no programa de continuidade de negócios. A fase de Avaliação também requer uma Análise de Impacto empresarial (BIA). A **fase planejamento** se concentra no desenvolvimento e implementação de estratégias de resiliência e recuperação e documentá-las em planos oficiais de continuidade de negócios. Por fim, **a Validação de Funcionalidade** testa planos de continuidade de negócios e suas implementações para verificar a eficácia e identificar possíveis melhorias.

As estratégias de continuidade de negócios dos serviços online da Microsoft usam redundância de hardware, rede e datacenter. A replicação de dados entre datacenters fornece alta disponibilidade e confiabilidade durante um incidente catastrófico. Ele também aumenta a resiliência para incidentes mundane, como falha de hardware isolado ou corrupção de dados.

## <a name="how-does-microsoft-test-business-continuity-and-disaster-recovery-plans"></a>Como a Microsoft testa planos de continuidade de negócios e recuperação de desastres?

A política Enterprise Business Continuity Management (EBCM) da Microsoft estipula que todos os planos de continuidade de negócios e recuperação de desastres da Microsoft devem ser testados, atualizados e revisados anualmente. Os serviços online da Microsoft testam seus planos de continuidade de negócios pelo menos anualmente por políticas de EBCM. Depois que os relatórios de ação são criados e revisados para validar, testar resultados e informar as atualizações do plano em resposta a quaisquer problemas descobertos durante o teste.

Para validar estratégias de resiliência e recuperação em uma ampla variedade de possíveis incidentes, o Programa EBCM define várias categorias de cenários de teste que afetam pessoas, locais e tecnologia. O nível de validação necessário para cada serviço baseia-se na importância do serviço, com serviços mais críticos recebendo validação mais rigorosa. Cada equipe de serviço online da Microsoft testa seu plano de continuidade de negócios de acordo com as diretrizes do EBCM para medir a eficácia do plano e a prontidão da equipe de serviço para executar o plano.

De acordo com as diretrizes do EBCM, as análises anuais de planos de continuidade de negócios e validação de funcionalidade devem ocorrer dentro de 12 meses após a última revisão. A validação de funcionalidade deve incluir a revisão da documentação de suporte, como a BIA, para garantir que ela permaneça precisa. A Microsoft disponibiliza resultados de validação de recursos para selecionar serviços online da Microsoft para nossos clientes por meio de relatórios trimestrais.

## <a name="how-do-microsoft-online-services-ensure-system-capacity-meets-demand"></a>Como os serviços online da Microsoft garantem que a capacidade do sistema atenda à demanda?

O planejamento de capacidade ajuda as equipes de serviço a alocar os recursos necessários para dar suporte à disponibilidade do serviço online da Microsoft. O planejamento de capacidade regular é necessário como parte do programa EBCM da Microsoft. As equipes de serviço analisam dados de capacidade durante análises trimestrais e durante situações de emergência que garantem mais revisão de capacidade.

Os dados brutos para planejamento de capacidade são mantidos por cada equipe de serviço e incluem métricas como processamento do sistema, memória e capacidade de hardware. As revisões agendadas usam um modelo da capacidade atual do sistema e o testam em relação às necessidades projetivas em situações de emergência. Se o modelo indicar lacunas na capacidade, as alterações propostas na capacidade do sistema serão enviadas à liderança da equipe de serviço para revisão. As alterações aprovadas são incorporadas em um novo modelo antes da implementação pelos engenheiros da equipe de serviço.

## <a name="how-do-microsoft-online-services-maintain-service-availability-during-routine-system-failures"></a>Como os serviços online da Microsoft mantêm a disponibilidade do serviço durante falhas de rotina do sistema?

Os serviços online da Microsoft alcançam resiliência de serviço por meio de arquitetura redundante, replicação de dados e verificação automatizada de integridade. A arquitetura redundante envolve a implantação de várias instâncias de um serviço em hardware geograficamente e fisicamente separado, fornecendo maior tolerância a falhas para serviços online da Microsoft. A replicação de dados garante que sempre haja várias cópias de dados do cliente em diferentes zonas de falha, permitindo que dados críticos do cliente sejam recuperados se corrompidos, perdidos ou até mesmo excluídos acidentalmente pelo cliente. A verificação automatizada de integridade aumenta a disponibilidade de dados restaurando automaticamente os dados afetados por vários tipos de corrupção física ou lógica.

## <a name="related-external-regulations--certifications"></a>Regulamentações externas relacionadas & certificações

Os serviços online da Microsoft são regularmente auditados para conformidade com regulamentações e certificações externas. Consulte a tabela a seguir para validação de controles relacionados à resiliência e continuidade.

### <a name="azure-and-dynamics-365"></a>Azure e Dynamics 365

| **Auditorias externas** | **Section** | **Data do relatório mais recente** |
|:--------------------|:------------|:-----------------------|
| [ISO 27001/27002](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Instrução of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7af5304-3a31-40e6-9abb-e26352305d41&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.17.1: Continuidade da segurança da informação <br> A.17.2: Redundâncias | 2 de dezembro de 2020 |
| [ISO 22301](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=6d388547-fc88-46e3-8de2-6bc2edc08b06&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=ee4b611b-bb4d-4056-b189-00da36e88949&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | Todos os controles | 13 de maio de 2020 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b8721ebd-af20-42fe-b22f-8332b0a19517&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=234a0f57-83c1-4afc-a586-a0e7a59592f7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=75c8cbf6-e456-473c-a05e-34fea888ec2a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | BC-1: Planos de continuidade de negócios <br> BC-3: Procedimentos de continuidade de negócios e recuperação de desastres <br> BC-4: teste de BCDR <br> BC-7: Planos de continuidade de negócios do Datacenter <br> BC-8: Teste de continuidade de negócios do datacenter <br> BC-9: avaliação de resiliência do datacenter <br> DS-5: Componentes de serviço de chave de backup <br> DS-6: Redundância de componentes críticos <br> DS-7: Replicação automática de dados do cliente <br> DS-8: Agendamento de backup <br> DS-9: Procedimentos de restauração de backup <br> DS-11: backups externos <br> DS-14: Restauração automática de serviços ao cliente | 31 de março de 2021 |

### <a name="office-365"></a>Office 365

| **Auditorias externas** | **Section** | **Data do relatório mais recente** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP](https://compliance.microsoft.com/compliancemanager) | CP-2: Plano de contingência <br> CP-3: Treinamento de contingência <br> CP-4: Teste de plano de contingência <br> CP-6: site de armazenamento alternativo <br> CP-7: site de processamento alternativo <br> CP-9: Backup do sistema de informações <br> CP-10: Recuperação e reconstituição do sistema de informações | 24 de setembro de 2020 |
| [ISO 27001/27002](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Instrução of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.17.1: Continuidade da segurança da informação <br> A.17.2: Redundâncias | Abril de 20, 2021 |
| [ISO 22301](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=13951eb3-6339-4629-b80d-dd0d43812fe7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | Todos os controles | 18 de março de 2019 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-49: Políticas de backup <br> CA-50: Continuidade de negócios <br> CA-51: Replicação de dados | 24 de dezembro de 2020 |
| [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-09: restauração de email do EXO | 24 de dezembro de 2020 |

## <a name="resources"></a>Recursos

- [Whitepaper Enterprise do Programa de Gerenciamento de Continuidade de Negócios da Microsoft](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=64f922a6-d624-40dd-a8ae-6f996b5186f3&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f)
- [Relatório de validação do Plano de Recuperação de Desastres e EBCM do Microsoft Cloud: FY21 Q4](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=83dc940a-2078-4e14-8b7d-07128e5b453d&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)

## <a name="legal-disclaimer"></a>Aviso de isenção de responsabilidade legal

- [Aviso de isenção de responsabilidade legal da continuidade de negócios empresariais](assurance-ebcm-legal-disclaimer.md)