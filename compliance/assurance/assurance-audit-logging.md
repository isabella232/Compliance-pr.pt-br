---
title: Visão geral do registro de Auditoria
description: Saiba mais sobre o log de auditoria no Microsoft 365
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
ms.openlocfilehash: 11695a941e5d5e6740833ab19bf2d68ac487c1c5
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/12/2021
ms.locfileid: "59158029"
---
# <a name="audit-logging-overview"></a>Visão geral do registro de Auditoria

## <a name="how-do-microsoft-online-services-employ-audit-logging"></a>Como os serviços online da Microsoft empregam o log de auditoria?

Os serviços online da Microsoft empregam log de auditoria para detectar atividades não autorizadas e fornecer responsabilidade para a equipe da Microsoft. Os logs de auditoria capturam detalhes sobre alterações de configuração do sistema e eventos de acesso, com detalhes para identificar quem foi responsável pela atividade, quando e onde a atividade ocorreu e qual foi o resultado da atividade. A análise de log automatizada dá suporte à detecção quase em tempo real de comportamento suspeito. Possíveis incidentes são escalonados para a equipe de resposta de segurança apropriada da Microsoft para investigação posterior.

O registro em log de auditoria interna dos serviços online da Microsoft captura dados de log de várias fontes, como:

- Logs de eventos
- Logs do AppLocker
- Dados de desempenho
- System Center dados
- Registros de detalhes de chamada
- Qualidade dos dados de experiência
- Logs do Servidor Web do IIS
- SQL Server logs
- Dados de syslog
- Logs de auditoria de segurança

## <a name="how-do-microsoft-online-services-centralize-and-report-on-audit-logs"></a>Como os serviços online da Microsoft centralizam e relatam logs de auditoria?

Muitos tipos diferentes de dados de log são carregados dos servidores Microsoft para uma solução de monitoramento de segurança proprietária para análise quase em tempo real (NRT) e um serviço interno de computação de dados grandes (Cosmos) ou o Azure Data Explorer (Kusto) para armazenamento de longo prazo. Essa transferência de dados ocorre por meio de uma conexão TLS validada pelo FIPS 140-2 em portas e protocolos aprovados usando ferramentas de gerenciamento de log automatizadas.

Os logs são processados no NRT usando métodos de aprendizado de máquina, estatísticas e baseados em regras para detectar indicadores de desempenho do sistema e possíveis eventos de segurança. Os modelos de aprendizado de máquina usam dados de log de entrada e dados de log históricos armazenados em Cosmos ou Kusto para melhorar continuamente os recursos de detecção. As detecções relacionadas à segurança geram alertas, notificando os engenheiros de chamada sobre um possível incidente e disparando ações de correção automatizadas quando aplicável. Além do monitoramento de segurança automatizado, as equipes de serviço usam ferramentas de análise e painéis para correlação de dados, consultas interativas e análise de dados. Esses relatórios são usados para monitorar e melhorar o desempenho geral do serviço.

Para obter mais informações sobre monitoramento e alertas de segurança, consulte a visão geral [do monitoramento de segurança.](assurance-security-monitoring.md)

![Auditar o fluxo de dados.](../media/assurance-audit-data-flow.png)

## <a name="how-do-microsoft-online-services-protect-audit-logs"></a>Como os serviços online da Microsoft protegem logs de auditoria?

As ferramentas usadas nos serviços online da Microsoft para coletar e processar registros de auditoria não permitem alterações permanentes ou irreversíveis no conteúdo do registro de auditoria original ou na ordem de tempo. O acesso aos dados de serviço online da Microsoft armazenados Cosmos ou Kusto é restrito a funcionários autorizados. Além disso, a Microsoft restringe o gerenciamento de logs de auditoria a um subconjunto limitado de membros da equipe de segurança responsáveis pela funcionalidade de auditoria. Os funcionários da equipe de segurança não têm acesso administrativo permanente a Cosmos ou Kusto. O acesso administrativo requer aprovação de acesso just-in-time (JIT), e todas as alterações nos mecanismos de registro em log para Cosmos são registradas e auditadas. Os logs de auditoria são mantidos por tempo suficiente para dar suporte a investigações de incidentes e atender aos requisitos regulatórios. O período exato de retenção de dados de log de auditoria determinado pelas equipes de serviço; a maioria dos dados de log de auditoria é mantida por 90 dias Cosmos e 180 dias em Kusto.

## <a name="how-do-microsoft-online-services-protect-user-personal-data-that-may-be-captured-in-audit-logs"></a>Como os serviços online da Microsoft protegem os dados pessoais do usuário que podem ser capturados em logs de auditoria?

Antes de carregar dados de log, um aplicativo de gerenciamento de log automatizado usa um serviço de limpeza para remover todos os campos que contenham dados do cliente, como informações de locatários e dados pessoais do usuário, e substituir esses campos por um valor de hash. Os logs anonimizados e com hashed são reescritos e carregados em Cosmos. Todas as transferências de log ocorrem em uma conexão criptografada TLS (FIPS 140-2).

## <a name="related-external-regulations--certifications"></a>Regulamentações externas relacionadas & certificações

Os serviços online da Microsoft são regularmente auditados para conformidade com regulamentações e certificações externas. Consulte a tabela a seguir para validação de controles relacionados ao log de auditoria.

### <a name="azure-and-dynamics-365"></a>Azure e Dynamics 365

| **Auditorias externas** | **Section** | **Data do relatório mais recente** |
|:--------------------|:------------|:-----------------------|
| [ISO 27001/27002](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Instrução of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7af5304-3a31-40e6-9abb-e26352305d41&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.4: Registro em log e monitoramento | 2 de dezembro de 2020 |
| [ISO 27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Instrução of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a3bca0ac-867d-4204-b66b-13665f5f1e8d&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=25718a8a-f34d-41e1-a95a-c49246508787&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.4: Registro em log e monitoramento | 2 de dezembro de 2020 |
| [ISO 27018](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Instrução of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=56904fc3-0942-4ff5-9eef-7cabc751a25c&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.4: Registro em log e monitoramento | 2 de dezembro de 2020 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b8721ebd-af20-42fe-b22f-8332b0a19517&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | VM-1: Log e coleção de eventos de segurança | 31 de março de 2021 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=234a0f57-83c1-4afc-a586-a0e7a59592f7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | C5-6: Acesso restrito a logs <br> VM-1: Log e coleção de eventos de segurança | 31 de março de 2021 |

### <a name="office-365"></a>Office 365

| **Auditorias externas** | **Section** | **Data do relatório mais recente** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP](https://compliance.microsoft.com/compliancemanager) | AU-2: Eventos de auditoria <br> AU-3: Conteúdo dos registros de auditoria <br> AU-4: Capacidade de armazenamento de auditoria <br> AU-5: Resposta a falhas de processamento de auditoria <br> AU-6: Revisão, análise e relatórios de auditoria <br> AU-7: Redução de auditoria e geração de relatório <br> AU-8: Carimbos de data/hora <br> AU-9: Proteção de informações de auditoria  <br> AU-10: não repúdio <br> AU-11: Retenção de registro de auditoria <br> AU-12: Geração de auditoria  | 24 de setembro de 2020 |
| [ISO 27001/27002/27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Instrução of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.4: Registro em log e monitoramento | Abril de 20, 2021 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-48: log de datacenter <br> CA-60: Log de auditoria | 24 de dezembro de 2020 |