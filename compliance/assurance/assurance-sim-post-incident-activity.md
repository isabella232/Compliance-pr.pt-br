---
title: 'Gerenciamento de incidentes de segurança do Microsoft 365: atividade pós-incidente'
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
ms.openlocfilehash: 66c25503ac574de512f5201981112a0e54714968
ms.sourcegitcommit: 2973d25e9e0185b84d281f963553a332eac1c1a3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/28/2021
ms.locfileid: "50040344"
---
# <a name="microsoft-365-security-incident-management-post-incident-activity"></a>Gerenciamento de incidentes de segurança do Microsoft 365: atividade pós-incidente

## <a name="postmortem"></a>Suál

Alguns incidentes de segurança, especialmente aqueles que estão afetando o cliente ou resultando em uma violação de dados, estão sujeitos a um incidente completo. A equipe de Resposta de Segurança do Microsoft 365 realiza um trabalho detalhado com todas as partes envolvidas na resposta a incidentes de segurança para:

- Documentar a sequência de eventos que causou o incidente
- Crie um resumo técnico do incidente, conforme suportado pelas evidências que inclui os atores envolvidos na violação (se conhecido). Este resumo incluirá como a resposta foi executada e outras principais respostas.
- Identifique problemas técnicos, falhas de procedimento, erros manuais, falhas de processo e falhas de comunicação e/ou qualquer vetor de ataque anteriormente desconhecido que foi identificado durante a resposta a incidentes de segurança.

Esse processo influenciará diretamente o aprimoramento do serviço, os processos operacionais e a documentação do Microsoft 365 definindo novas prioridades no ciclo de desenvolvimento de engenharia do Microsoft 365.

## <a name="documentation"></a>Documentação

Todas as principais descobertas técnicas no processo de transformação são capturadas em um relatório e investimentos em serviços ou correções na forma de bugs ou solicitações de alteração de desenvolvimento. Essas descobertas são acompanhadas com as equipes de engenharia apropriadas. Para falhas de processo e problemas entre organizações, os problemas são documentados no banco de dados da equipe de Resposta de Segurança do Microsoft 365 e acompanhados com os grupos apropriados para lidar com eles.

## <a name="process-improvement"></a>Melhoria do processo

Responder a um incidente de segurança no Microsoft 365 envolve a coordenação com vários grupos espalhados por diferentes organizações dentro da Microsoft e, potencialmente, até mesmo organizações externas apropriadas, como a imposição da lei. Sabemos que é fundamental avaliar nossas respostas após cada incidente de segurança para a suficiência e a totalidade. Para quaisquer melhorias ou alterações identificadas, a equipe de Resposta de Segurança do Microsoft 365 avalia as sugestões em consulta com as equipes e participantes apropriados e, quando apropriado, as incorpora aos procedimentos operacionais padrão. Todas as alterações, bugs ou melhorias de serviço necessárias identificadas durante a resposta a incidentes de segurança ou atividade de incidentes de segurança são registradas e controladas em um banco de dados de engenharia interno do Microsoft 365. Todos os bugs ou recursos em potencial são atribuídos ao proprietário apropriado. A equipe de Resposta de Segurança do Microsoft 365 analisa todas as entradas até que o problema seja resolvido.

## <a name="related-articles"></a>Artigos relacionados

- [Gerenciamento de incidentes do Centro de segurança do Microsoft 365](assurance-security-incident-management.md)
- [Preparação do gerenciamento de incidentes de segurança do Microsoft 365](assurance-sim-preparation.md)
- [Análise e detecção de gerenciamento de incidentes de segurança do Microsoft 365](assurance-sim-detection-analysis.md)
- [Contenção, eliminação e recuperação do gerenciamento de incidentes de segurança do Microsoft 365](assurance-sim-containment-eradication-recovery.md)
