---
title: 'Gerenciamento de incidentes de segurança do Microsoft 365: Atividade pós-incidente'
description: Este artigo fornece uma visão geral do processo de atividade pós-incidente de gerenciamento de incidentes de segurança no Microsoft 365.
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
f1.keywords:
- NOCSH
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 4ebd31c16f8abb3eddd6ed924a045d88597aba40
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51496708"
---
# <a name="microsoft-365-security-incident-management-post-incident-activity"></a>Gerenciamento de incidentes de segurança do Microsoft 365: Atividade pós-incidente

## <a name="postmortem"></a>Post-mortem

Alguns incidentes de segurança, especialmente aqueles incidentes que estão afetando o cliente ou resultando em uma violação de dados, estão sujeitos a um incidente completo pós-morte. A equipe de Resposta de Segurança do Microsoft 365 conduz uma post-morte detalhada com todas as partes envolvidas na resposta a incidentes de segurança:

- Documente a sequência de eventos que causaram o incidente
- Crie um resumo técnico do incidente como suportado pelas evidências que incluem os atores envolvidos na violação (se conhecido). Este resumo incluirá como a resposta foi executada e outros pontos importantes.
- Identifique erros técnicos, falhas de procedimento, erros manuais, falhas de processo e falhas de comunicação e/ou quaisquer vetores de ataque desconhecidos anteriormente identificados durante a resposta a incidentes de segurança.

A postagem pós-morte influenciará diretamente o aperfeiçoamento do serviço, os processos operacionais e a documentação do Microsoft 365 definindo novas prioridades no ciclo de desenvolvimento de engenharia do Microsoft 365.

## <a name="documentation"></a>Documentação

Todas as principais descobertas técnicas no processo pós-morte são capturadas em um relatório e investimentos de serviço ou correções na forma de bugs ou solicitações de alteração de desenvolvimento. Essas descobertas são acompanhadas com as equipes de engenharia apropriadas. Para falhas de processo e problemas organizacionais entre organizações, os problemas são documentados no banco de dados da equipe de Resposta de Segurança do Microsoft 365 e acompanhados com os grupos apropriados para lidar com eles.

## <a name="process-improvement"></a>Melhoria do processo

Responder a um incidente de segurança no Microsoft 365 envolve a coordenação com vários grupos espalhados por organizações diferentes dentro da Microsoft e, potencialmente, até mesmo organizações externas apropriadas, como a aplicação da lei. Sabemos que é fundamental avaliar nossas respostas após cada incidente de segurança para suficiência e conclusão. Para quaisquer melhorias ou alterações identificadas, a equipe de Resposta de Segurança do Microsoft 365 avalia as sugestões em consulta com as equipes e participantes apropriados e, quando apropriado, as incorpora em procedimentos operacionais padrão. Todas as alterações, bugs ou melhorias de serviço necessárias identificadas durante a resposta a incidentes de segurança ou atividades pós-morte são registradas e rastreadas em um banco de dados de engenharia interno do Microsoft 365. Todos os possíveis bugs ou recursos são atribuídos ao proprietário apropriado. A equipe de Resposta de Segurança do Microsoft 365 revisa todas as entradas até que o problema seja resolvido.

## <a name="related-articles"></a>Artigos relacionados

- [Gerenciamento de incidentes do Centro de segurança do Microsoft 365](assurance-security-incident-management.md)
- [Preparação do gerenciamento de incidentes de segurança do Microsoft 365](assurance-sim-preparation.md)
- [Análise e detecção de gerenciamento de incidentes de segurança do Microsoft 365](assurance-sim-detection-analysis.md)
- [Contenção, erradicação e recuperação de gerenciamento de incidentes de segurança do Microsoft 365](assurance-sim-containment-eradication-recovery.md)
