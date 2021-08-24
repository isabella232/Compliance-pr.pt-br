---
title: Microsoft 365 Lidando com corrupção de dados
description: Este artigo explica a corrupção de dados Microsoft 365 e os esforços da Microsoft para impedir e recuperar dados.
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
ms.openlocfilehash: 860a150760e080df4a577d73478a75ac94b8700b
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2021
ms.locfileid: "58482074"
---
# <a name="dealing-with-data-corruption-in-microsoft-365"></a>Lidar com a corrupção de dados em Microsoft 365

Um dos aspectos desafiadores da execução de um serviço de nuvem em grande escala é como lidar com a corrupção de dados, dado o grande volume de dados e sistemas independentes. A corrupção de dados pode ser causada por:

- Bugs de aplicativo ou infraestrutura, corrompendo parte ou todo o estado do aplicativo
- Problemas de hardware que resultam em perda de dados ou incapacidade de ler dados
- Erros operacionais humanos
- Hackers mal-intencionados e funcionários insatisfeitos
- Incidentes em serviços externos que resultam em alguma perda de dados

Como uma resiliência maior na integridade de dados significa menos incidentes de corrupção de dados, a Microsoft criou mecanismos de proteção Microsoft 365 para impedir que a corrupção aconteça, bem como sistemas e processos que nos permitem recuperar dados se isso acontecer. Verificações e processos existem dentro dos vários estágios do processo de lançamento de engenharia para aumentar a resiliência contra a corrupção de dados, incluindo:

- Design do sistema
- Organização e estrutura de códigos
- Revisão de código
- Testes de unidade, testes de integração e testes de sistema
- Testes/portas de fio de viagem

Em Microsoft 365 ambientes de produção, a replicação de pares entre datacenters garante que sempre haja várias cópias ao vivo de todos os dados. As imagens e scripts padrão são usados para recuperar servidores perdidos e os dados replicados são usados para restaurar dados do cliente. Devido às verificações e processos internos de resiliência de dados, a Microsoft mantém backups somente da documentação do sistema de informações do Microsoft 365 (incluindo documentação relacionada à segurança), usando a replicação interna no SharePoint Online e nossa ferramenta de repositório de código interno, Source Depot. A documentação do sistema é armazenada no SharePoint Online, e o Source Depot contém imagens do sistema e do aplicativo. Os SharePoint Online e o Source Depot usam o versioning e são replicados em tempo real.
