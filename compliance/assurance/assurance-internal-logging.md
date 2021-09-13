---
title: Microsoft 365 log interno para Microsoft 365 engenharia
description: Neste artigo, encontre uma explicação de como funciona o log interno para Microsoft 365 Engenharia.
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: medium
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 20a21fe0d67f8986ec6e89b8ecbfd2915f9b8245
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/12/2021
ms.locfileid: "59157938"
---
# <a name="internal-logging-for-microsoft-365-engineering"></a>Log interno para engenharia do Microsoft 365

Além dos eventos e dados de log disponíveis para clientes, a Microsoft mantém um sistema de coleta de dados de log interno que está disponível para engenheiros Microsoft 365 log. Muitos tipos diferentes de dados de log são carregados de servidores Microsoft 365 para uma solução de monitoramento de segurança proprietária para análise quase em tempo real (NRT) e um serviço interno de computação de big data (Cosmos) para armazenamento a longo prazo. Essa transferência de dados ocorre por meio de uma conexão TLS validada pelo FIPS 140-2 em portas e protocolos aprovados usando uma ferramenta de automação proprietária chamada ODL (carregador de dados Office). As ferramentas usadas no Microsoft 365 para coletar e processar registros de auditoria não permitem alterações permanentes ou irreversíveis no conteúdo do registro de auditoria original ou na ordem de tempo.

As equipes de serviço usam o Cosmos como um repositório centralizado para conduzir uma análise do uso do aplicativo, para medir o desempenho do sistema e operacional e para procurar anormalidades e padrões que possam indicar problemas ou problemas de segurança. Cada equipe de serviço carrega uma linha de base que inclui:

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

Antes de carregar, o aplicativo ODL usa um serviço de limpeza para remover todos os campos que contenham dados do cliente, como informações de locatário e informações de identificação do usuário final, e substituir esses campos por um valor de hash. Os logs limpos são carregados para Cosmos e para a solução de monitoramento de segurança NRT que analisa os logs para possíveis eventos de segurança e indicadores de desempenho. O período de retenção de dados de log de auditoria no Cosmos é determinado pelas equipes de serviço; a maioria dos dados de log de auditoria é mantida por 90 dias ou mais para dar suporte a investigações de incidentes de segurança e para atender aos requisitos de retenção regulamentar.

O acesso Microsoft 365 dados armazenados no Cosmos é restrito a funcionários autorizados. A Microsoft restringe o gerenciamento de logs de auditoria a um subconjunto limitado de membros da Equipe de Segurança responsáveis pela funcionalidade de auditoria. A Equipe de Segurança não tem acesso administrativo permanente Cosmos e todas as alterações são gravadas e auditadas.

Após a análise de NRT, cada equipe de serviço pode usar ferramentas de análise e painéis para correlação de dados, consultas interativas e análise de dados. Esses relatórios são usados para monitorar e melhorar o desempenho geral do serviço.
