---
title: Visão geral do log de auditoria
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
ms.openlocfilehash: 3714a5df73253d0814e1d4067248116cb6e10a40
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/30/2020
ms.locfileid: "49505840"
---
# <a name="audit-logging-overview"></a>Visão geral do log de auditoria

## <a name="how-does-microsoft-365-employ-audit-logging"></a>Como a Microsoft 365 emprega o log de auditoria?

A Microsoft 365 utiliza logs de auditoria para detectar atividades não autorizadas em seus produtos e serviços e fornecer responsabilidade para a equipe da Microsoft. Os logs de auditoria capturam detalhes sobre alterações de configuração do sistema e eventos de acesso, com detalhes para identificar quem era responsável pela atividade, quando e onde a atividade ocorreu e o resultado da atividade. A análise de logs automatizada oferece suporte à detecção de comportamento suspeito em tempo real. Possíveis incidentes são escalonados para a equipe de resposta de segurança do Microsoft 365 para uma investigação mais detalhada.

O log de auditoria interna do Microsoft 365 captura dados de log de várias fontes, como:

- Logs de eventos
- Logs do AppLocker
- Dados de desempenho
- Dados do System Center
- Registros de detalhes da chamada
- Dados de qualidade da experiência
- Logs de servidor Web do IIS
- Logs do SQL Server
- Dados de syslog
- Logs de auditoria de segurança

## <a name="how-does-microsoft-365-centralize-and-report-on-audit-logs"></a>Como a Microsoft 365 centraliza e relata logs de auditoria?

Muitos tipos diferentes de dados de log são carregados dos servidores da Microsoft 365 para um serviço de computação de dados interno e global chamado Cosmos. Cada equipe de serviço carrega logs de auditoria de seus respectivos servidores no banco de dados do cosmos para agregação e análise. Essa transferência de dados ocorre em uma conexão TLS validada pelo FIPS 140-2 em portas e protocolos aprovados usando uma ferramenta de automação proprietária chamada de ODL (Office Data Loader).

As equipes de serviço executam consultas com escopo em seus dados no cosmos para correlação de logs, alerta e relatórios. Por exemplo, a equipe de segurança do Microsoft 365 usa dados do cosmos com um analisador de log de eventos proprietário para correlacionar dados de log, enviar alertas e gerar relatórios acionáveis sobre possíveis atividades suspeitas no ambiente de produção do Microsoft 365. Os relatórios desses dados são usados para corrigir as vulnerabilidades e melhorar o desempenho geral do serviço.

## <a name="how-does-microsoft-365-protect-audit-logs"></a>Como a Microsoft 365 protege logs de auditoria?

As ferramentas usadas no Microsoft 365 para coletar e processar registros de auditoria não permitem alterações permanentes ou irreversíveis no conteúdo do registro de auditoria original ou na ordenação do tempo. O acesso aos dados do Microsoft 365 armazenados no cosmos é restrito a pessoal autorizado. A Microsoft 365 restringe o gerenciamento da funcionalidade de auditoria ao subconjunto limitado de membros da equipe de serviço responsáveis pela funcionalidade de auditoria. Esses membros da equipe não têm a capacidade de modificar ou excluir dados do cosmos, e todas as alterações nos mecanismos de registro em log para cosmos são registradas e auditadas. Os logs de auditoria são retidos por tempo suficiente para dar suporte a investigações de incidentes e cumprir requisitos normativos. O período exato de retenção de dados de log de auditoria no cosmos é determinado pelas equipes de serviço; a maioria dos dados de log de auditoria é mantida por 90 dias ou mais.

## <a name="how-does-microsoft-365-protect-end-user-identifiable-information-that-may-be-captured-in-audit-logs"></a>Como a Microsoft 365 protege as informações identificáveis pelo usuário final que podem ser capturadas nos logs de auditoria?

Antes de carregar dados no cosmos, o aplicativo do ODL usa um serviço de depuração para ofuscar quaisquer campos que contenham dados do cliente, como informações de locatário e informações de identificação do usuário final, e substitua esses campos por um valor de hash. Os logs anônimos e de hash são reconfigurados e, em seguida, carregados no cosmos.

## <a name="related-external-regulations--certifications"></a>Normas externas relacionadas & certificações

Os serviços online da Microsoft são auditados regularmente para fins de conformidade com regulamentos externos e certificações. Consulte a tabela a seguir para validar os controles relacionados ao log de auditoria.

| **Auditorias externas** | **Section** | **Data do relatório mais recente** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | AU-2: eventos de auditoria <br> AU-3: conteúdo de registros de auditoria <br> AU-4: auditoria da capacidade de armazenamento <br> AU-5: resposta a falhas de processamento de auditoria <br> AU-6: análise, análise e relatórios de auditoria <br> AU-7: redução de auditoria e geração de relatórios <br> AU-8: carimbos de data/hora <br> AU-9: proteção de informações de auditoria  <br> AU-10: não repudiação <br> AU-11: auditoria de retenção de registros <br> AU-12: geração de auditoria  | 24 de setembro de 2020 | 
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaração de aplicabilidade](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 12.4: Logging and Monitoring | 22 de fevereiro de 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaração de aplicabilidade](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 12.4: Logging and Monitoring | 22 de fevereiro de 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | AC-48: log de datacenter <br> AC-60: log de auditoria | 30 de setembro de 2019 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | AC-48: log de datacenter <br> AC-60: log de auditoria | 30 de setembro de 2019 |