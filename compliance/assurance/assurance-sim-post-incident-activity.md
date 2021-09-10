---
title: 'Gerenciamento de incidentes de segurança da Microsoft: atividade pós-incidente'
description: Este artigo fornece uma visão geral do processo de atividade pós-incidente de gerenciamento de incidentes de segurança nos serviços online da Microsoft.
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
f1.keywords:
- NOCSH
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 820c912dc55d5cc98cedc38676b5039591cf5baa
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2021
ms.locfileid: "58946915"
---
# <a name="microsoft-security-incident-management-post-incident-activity"></a>Gerenciamento de incidentes de segurança da Microsoft: atividade pós-incidente

## <a name="postmortem"></a>Post-mortem

Alguns incidentes de segurança, especialmente aqueles incidentes que estão afetando o cliente ou resultando em uma violação de dados, estão sujeitos a um incidente completo pós-morte. A equipe de resposta de segurança conduz uma post-morte detalhada com todas as partes envolvidas na resposta a incidentes de segurança:

- Documente a sequência de eventos que causaram o incidente.
- Crie um resumo técnico do incidente como suportado pelas evidências que incluem os atores envolvidos na violação (se conhecido). Este resumo incluirá como a resposta foi executada e outros pontos importantes.
- Identifique erros técnicos, falhas de procedimento, erros manuais, falhas de processo e falhas de comunicação e/ou quaisquer vetores de ataque desconhecidos anteriormente identificados durante a resposta a incidentes de segurança.

A postagem pós-morte influenciará diretamente o aperfeiçoamento do serviço online da Microsoft, os processos operacionais e a documentação definindo novas prioridades no ciclo de desenvolvimento de engenharia de serviços online da Microsoft.

## <a name="documentation"></a>Documentação

Todas as principais descobertas técnicas no processo pós-morte são capturadas em um relatório e investimentos de serviço ou correções na forma de bugs ou solicitações de alteração de desenvolvimento. Essas descobertas são acompanhadas com as equipes de engenharia apropriadas. Para falhas de processo e problemas organizacionais entre organizações, os problemas são documentados no banco de dados da equipe de resposta de segurança e acompanhados com os grupos apropriados para lidar com eles.

## <a name="process-improvement"></a>Melhoria do processo

Responder a um incidente de segurança nos serviços online da Microsoft envolve a coordenação com vários grupos espalhados por diferentes organizações dentro da Microsoft e, potencialmente, até mesmo organizações externas apropriadas, como a aplicação da lei. Sabemos que é fundamental avaliar nossas respostas após cada incidente de segurança para suficiência e conclusão. Para quaisquer melhorias ou alterações identificadas, a equipe de resposta de segurança avalia as sugestões em consulta com as equipes e partes interessadas apropriadas e, quando apropriado, as incorpora em procedimentos operacionais padrão. Todas as alterações, bugs ou melhorias de serviço necessárias identificadas durante a resposta a incidentes de segurança ou atividades pós-morte são registradas e rastreadas em um banco de dados de engenharia interno da Microsoft. Todos os possíveis bugs ou recursos são atribuídos ao proprietário apropriado. A equipe de resposta de segurança da Microsoft revisa todas as entradas até que o problema seja resolvido.

## <a name="related-articles"></a>Artigos relacionados

- [Gerenciamento de incidentes de segurança da Microsoft](assurance-security-incident-management.md)
- [Gerenciamento de incidentes de segurança da Microsoft: Preparação](assurance-sim-preparation.md)
- [Gerenciamento de incidentes de segurança da Microsoft: Detecção e análise](assurance-sim-detection-analysis.md)
- [Gerenciamento de incidentes de segurança da Microsoft: contenção, erradicação e recuperação](assurance-sim-containment-eradication-recovery.md)
- [Como registrar um tíquete de suporte a eventos de segurança](/azure/security/fundamentals/event-support-ticket)
- [Notificação de Violação do Azure e do Dynamics 365 no GDPR](/compliance/regulatory/gdpr-breach-azure-dynamics)
