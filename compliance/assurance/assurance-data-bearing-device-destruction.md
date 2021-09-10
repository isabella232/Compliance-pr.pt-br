---
title: Destruição de dispositivo portador de dados
description: Neste artigo, você encontrará uma visão geral do processo de destruição de dispositivos com suporte a dados para datacenters da Microsoft.
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
ms.openlocfilehash: 6a26334b805be069298302d3ad1e8e5b9e728150
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2021
ms.locfileid: "58946858"
---
# <a name="data-bearing-device-destruction"></a>Destruição de dispositivo portador de dados

## <a name="data-destruction-overview"></a>Visão geral da destruição de dados

A Microsoft tem diretrizes, políticas, requisitos de segurança e procedimentos de manipulação e gerenciamento de DBDs nos datacenters da Microsoft.

Um DBD é qualquer dispositivo de armazenamento capaz de armazenar dados do cliente ou proprietários da Microsoft:

- Unidades de disco rígido (HDD)
- Unidades de estado sólido (SSD)
- Unidades USB
- Cartões aceleradores de IO
- Cartões Flash SD/Compact
- Cartões HSM
- Cartões SSD PCIe
- NVDIMM (Módulo de memória não volátil dual em linha)

DbDs com falha usados nos datacenters da Microsoft são auditados e destruídos no campus do datacenter. Qualquer ativo retirado do serviço é avaliado para descarte de forma proporcional aos seus requisitos de segurança/privacidade e classificação de ativos e de acordo com quaisquer regras, leis e regulamentos aplicáveis.

A Microsoft usa três categorias de higienização de dados para DBDs e ativos que contêm dados:

- **Clear**: relaciona-se às técnicas lógicas que ajudam a higienizar dados em todos os locais de armazenamento acessível pelo usuário para proteção contra técnicas simples de recuperação de dados não invasivas. Essas são técnicas normalmente aplicadas por meio dos comandos de leitura e gravação padrão ao dispositivo de armazenamento, como reescrever com um novo valor ou usar uma opção de menu para redefinir o dispositivo para o estado de fábrica (onde não há suporte para reconfiguração).
- **Limpeza**: relaciona-se a técnicas físicas ou lógicas que tornam inviável a recuperação de dados de destino usando técnicas de laboratório de última geração.
- **Destruir**: torna inviável a recuperação de dados de destino usando técnicas de laboratório de última geração e resulta na incapacidade subsequente de usar a mídia para armazenamento de dados.

A limpeza e a limpeza são executadas usando ferramentas e processos aprovados pelo Grupo de Segurança. Os registros são mantidos da eliminação e destruição de ativos. Os dispositivos que não conseguem concluir a limpa são desgaussados com êxito (somente para mídia magnética), com vários pinos perfurados (para placas com base lascadas, como SSDs) ou destruídos.

## <a name="clear"></a>Limpar

Se um ativo aposentado for avaliado e considerado não acessível, ele será limpo por uma solução de erradicação de dados aprovada. Os datacenters da Microsoft usam as diretrizes claras do NIST SP-800-88.

## <a name="purge"></a>Purge

Dependendo da configuração local e da disponibilidade do dispositivo, alguns dispositivos são limpos antes da destruição. Os dispositivos de limpeza incluem degaussers aprovados pela NSA para mídia magnética e dispositivos de punção de vários pinos para mídia de estado sólido. Os datacenters da Microsoft usam as diretrizes de limpeza do NIST SP-800-88.

## <a name="destroy"></a>Destruir

Se um ativo aposentado for avaliado e considerado acessível, ele será destruído no local usando um procedimento operacional padrão aprovado que atenda às diretrizes do NIST SP-800-88. Esses DBDs são rastreados física e logicamente para manter a cadeia de custodia por meio da disposição final.

Cada datacenter da Microsoft usa um processo local para higienizar e descartar DBDs com falha e ressarção. Durante esse processo, a equipe da Microsoft garante que a cadeia de proteção seja mantida durante todo o processo de descarte.

## <a name="resources"></a>Recursos

- [Publicação Especial NIST 800-88](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-88r1.pdf)
