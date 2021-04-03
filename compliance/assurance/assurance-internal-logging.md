---
title: Log interno do Microsoft 365 para engenharia do Microsoft 365
description: Neste artigo, encontre uma explicação sobre como funciona o log interno para as equipes de Engenharia do Microsoft 365.
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
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
ms.openlocfilehash: 110a61c27a00380eede4d4f2303acfb025a27a1f
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497071"
---
# <a name="internal-logging-for-microsoft-365-engineering"></a>Log interno para engenharia do Microsoft 365

Além dos eventos e dados de log disponíveis para clientes, há também um sistema de coleta de dados de log interno que está disponível para engenheiros do Microsoft 365 na Microsoft. Muitos tipos diferentes de dados de log são carregados dos servidores do Microsoft 365 para um serviço interno de computação de dados grandes chamado Cosmos. Cada equipe de serviço carrega logs de auditoria de seus respectivos servidores no banco de dados do Cosmos para agregação e análise. Essa transferência de dados ocorre por meio de uma conexão TLS validada pelo FIPS 140-2 em portas e protocolos especificamente aprovados usando uma ferramenta de automação proprietária chamada ODL (Office Data Loader). As ferramentas usadas no Microsoft 365 para coletar e processar registros de auditoria não permitem alterações permanentes ou irreversíveis no conteúdo do registro de auditoria original ou na ordem de tempo.

As equipes de serviço usam o Cosmos como um repositório centralizado para conduzir uma análise do uso do aplicativo, para medir o desempenho operacional e do sistema e procurar por anormalidades e padrões que possam indicar problemas ou problemas de segurança. Cada equipe de serviço carrega uma linha de base de logs no Cosmos, dependendo do que eles estão procurando analisar, que geralmente incluem:

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

Antes de carregar dados no Cosmos, o aplicativo ODL usa um serviço de limpeza para ofuscar todos os campos que contenham dados do cliente, como informações de locatário e informações de identificação do usuário final, e substitua esses campos por um valor de hash. Os logs anonimizados e com hashed são reescritos e carregados no Cosmos. As equipes de serviço executarão consultas com escopo em relação aos dados no Cosmos para correlação, alertas e relatórios. O período de retenção de dados de log de auditoria no Cosmos é determinado pelas equipes de serviço; a maioria dos dados de log de auditoria é mantida por 90 dias ou mais para dar suporte a investigações de incidentes de segurança e para atender aos requisitos de retenção regulamentar.

O acesso aos dados do Microsoft 365 armazenados no Cosmos é restrito a funcionários autorizados. A Microsoft restringe o gerenciamento da funcionalidade de auditoria ao subconjunto limitado de membros da equipe de serviço responsáveis pela funcionalidade de auditoria. Esses membros da equipe não têm a capacidade de modificar ou excluir dados do Cosmos, e todas as alterações nos mecanismos de registro em log para o Cosmos são registradas e auditadas.

Cada equipe de serviço acessa seus dados de log para análise, autorizando determinados aplicativos a realizar análises específicas. Por exemplo, a equipe de Segurança do Microsoft 365 usa dados do Cosmos por meio de um analisador de log de eventos proprietário para correlacionar, alertar e gerar relatórios acionáveis sobre possíveis atividades suspeitas no ambiente de produção do Microsoft 365. Os relatórios desses dados são usados para corrigir vulnerabilidades e para melhorar o desempenho geral do serviço. Se um alerta ou relatório específico exigir mais investigação, a equipe de serviço poderá solicitar que os dados sejam importados de volta para o serviço do Microsoft 365. Como o log específico que está sendo importado do Cosmos está criptografado e o pessoal do serviço não tem acesso a chaves de descriptografia, o log de destino é passado programaticamente por um serviço de descriptografia que retorna resultados com escopo para a equipe de serviço autorizada. Quaisquer vulnerabilidades encontradas neste exercício são relatadas e escalonados usando os canais de gerenciamento de incidentes de segurança padrão da Microsoft.
