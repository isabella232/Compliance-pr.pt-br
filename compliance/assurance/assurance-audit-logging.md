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
ms.openlocfilehash: dc56d0413811d59309c974931e1fa50ee184e94a
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497677"
---
# <a name="audit-logging-overview"></a>Visão geral do registro de Auditoria

## <a name="how-does-microsoft-365-employ-audit-logging"></a>Como o Microsoft 365 emprega o log de auditoria?

O Microsoft 365 emprega o log de auditoria para detectar atividades não autorizadas em seus produtos e serviços e fornecer responsabilidade para a equipe da Microsoft. Os logs de auditoria capturam detalhes sobre alterações de configuração do sistema e eventos de acesso, com detalhes para identificar quem foi responsável pela atividade, quando e onde a atividade ocorreu e qual foi o resultado da atividade. A análise de log automatizada dá suporte à detecção quase em tempo real de comportamento suspeito. Possíveis incidentes são escalonados para a equipe de Resposta de Segurança do Microsoft 365 para investigação posterior.

O registro em log de auditoria interna do Microsoft 365 captura dados de log de várias fontes, como:

- Logs de eventos
- Logs do AppLocker
- Dados de desempenho
- Dados do System Center
- Registros de detalhes de chamada
- Qualidade dos dados de experiência
- Logs do Servidor Web do IIS
- SQL Server logs
- Dados de syslog
- Logs de auditoria de segurança

## <a name="how-does-microsoft-365-centralize-and-report-on-audit-logs"></a>Como o Microsoft 365 centraliza e relata logs de auditoria?

Muitos tipos diferentes de dados de log são carregados dos servidores do Microsoft 365 para um serviço interno de computação de dados grandes chamado Cosmos. Cada equipe de serviço carrega logs de auditoria de seus respectivos servidores no banco de dados do Cosmos para agregação e análise. Essa transferência de dados ocorre por meio de uma conexão TLS validada pelo FIPS 140-2 em portas e protocolos aprovados usando uma ferramenta de automação proprietária chamada Office Data Loader (ODL).

As equipes de serviço executarão consultas com escopo em relação aos dados no Cosmos para correlação de log, alertas e relatórios. Por exemplo, a equipe de Segurança do Microsoft 365 usa dados do Cosmos com um analisador de log de eventos proprietário para correlacionar dados de log, enviar alertas e gerar relatórios acionáveis sobre possíveis atividades suspeitas no ambiente de produção do Microsoft 365. Os relatórios desses dados são usados para corrigir vulnerabilidades e melhorar o desempenho geral do serviço.

## <a name="how-does-microsoft-365-protect-audit-logs"></a>Como o Microsoft 365 protege logs de auditoria?

As ferramentas usadas no Microsoft 365 para coletar e processar registros de auditoria não permitem alterações permanentes ou irreversíveis no conteúdo do registro de auditoria original ou na ordem de tempo. O acesso aos dados do Microsoft 365 armazenados no Cosmos é restrito a funcionários autorizados. O Microsoft 365 restringe o gerenciamento da funcionalidade de auditoria ao subconjunto limitado de membros da equipe de serviço responsáveis pela funcionalidade de auditoria. Esses membros da equipe não têm a capacidade de modificar ou excluir dados do Cosmos, e todas as alterações nos mecanismos de registro em log para o Cosmos são registradas e auditadas. Os logs de auditoria são mantidos por tempo suficiente para dar suporte a investigações de incidentes e atender aos requisitos regulatórios. O período exato de retenção de dados de log de auditoria no Cosmos é determinado pelas equipes de serviço; a maioria dos dados de log de auditoria é mantida por 90 dias ou mais.

## <a name="how-does-microsoft-365-protect-end-user-identifiable-information-that-may-be-captured-in-audit-logs"></a>Como o Microsoft 365 protege informações de identificação do usuário final que podem ser capturadas em logs de auditoria?

Antes de carregar dados no Cosmos, o aplicativo ODL usa um serviço de limpeza para ofuscar todos os campos que contenham dados do cliente, como informações de locatário e informações de identificação do usuário final, e substitua esses campos por um valor de hash. Os logs anonimizados e com hashed são reescritos e carregados no Cosmos.

## <a name="related-external-regulations--certifications"></a>Regulamentações externas relacionadas & certificações

Os serviços online da Microsoft são regularmente auditados para conformidade com regulamentações e certificações externas. Consulte a tabela a seguir para validação de controles relacionados ao log de auditoria.

| **Auditorias externas** | **Section** | **Data do relatório mais recente** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | AU-2: Eventos de auditoria <br> AU-3: Conteúdo dos registros de auditoria <br> AU-4: Capacidade de armazenamento de auditoria <br> AU-5: Resposta a falhas de processamento de auditoria <br> AU-6: Revisão, análise e relatórios de auditoria <br> AU-7: Redução de auditoria e geração de relatório <br> AU-8: Carimbos de data/hora <br> AU-9: Proteção de informações de auditoria  <br> AU-10: não repúdio <br> AU-11: Retenção de registro de auditoria <br> AU-12: Geração de auditoria  | 24 de setembro de 2020 | 
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Instrução of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.4: Registro em log e monitoramento | 22 de fevereiro de 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Instrução of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.4: Registro em log e monitoramento | 22 de fevereiro de 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-48: log de datacenter <br> CA-60: Log de auditoria | 24 de dezembro de 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-48: log de datacenter <br> CA-60: Log de auditoria | 24 de dezembro de 2020|