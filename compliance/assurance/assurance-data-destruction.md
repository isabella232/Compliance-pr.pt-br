---
title: Destruição de dados no Microsoft 365
description: Uma visão geral das políticas da Microsoft sobre reciclagem, descarte ou destruição de unidades de disco e servidores do data center do Microsoft 365.
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
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 1b9d410422e22fe67cb27617ba16e2ddbbaec0fd
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497645"
---
# <a name="data-destruction-in-microsoft-365"></a>Destruição de dados no Microsoft 365

## <a name="physical-data-destruction"></a>Destruição física de dados

A Microsoft tem políticas Padrão de Tratamento de Dados que abordam a reciclagem e o descarte de unidades de disco e servidores com falha ou retirada. Antes de reutilizar quaisquer unidades de disco do Microsoft 365, a Microsoft executa um processo de higienização física consistente com a Publicação Especial do Instituto Nacional de Padrões e Tecnologias 800-88 ([NIST SP 800-88 Guidelines for Media Sanitization](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-88r1.pdf)). Como todas as unidades de disco no Microsoft 365 são criptografadas usando criptografia de nível de volume do BitLocker, o apagamento compatível com nist SP 800-88 não é tecnicamente necessário. No entanto, a Microsoft realiza esse processo.

Os discos com falha usados nos datacenters do Microsoft 365 são fisicamente destruídos e auditados por meio do processo ISO. O tipo de ativo determina os meios apropriados de descarte. Para discos rígidos que não podem ser apagados, a Microsoft usa um processo de destruição para destruir a mídia e tornar impossível a recuperação de informações. Por exemplo, os discos são fisicamente destruídos, pulverizados ou in-locados. A Microsoft mantém todos os registros da destruição e executa um processo de higienização semelhante em servidores reutilizado no Microsoft 365. Essas diretrizes abrangem a higienização eletrônica e física.

Cada datacenter usa um processo de destruição física no local para descartar seus discos. As caixas de segurança para mídia de armazenamento designadas para descarte de disco estão em cada área do datacenter. Cada estação de lixeira segura tem monitoramento de vídeo. Quando uma lixeira atinge aproximadamente 50% de capacidade, a equipe de Serviços de Site entra em contato com a equipe de Segurança Física para coordenar a remoção. A equipe de Serviços de Site e um Escritório de Segurança removem a lixeira segura e a movê-la em uma área de armazenamento protegida designada. Políticas e procedimentos que regem o tratamento de dispositivos de suporte de dados durante o descarte são testados rotineiramente, incluindo procedimentos para garantir a condição de máquinas aprovadas para destruição.

No processo de destruição de dados, os discos são apagados de maneira compatível com o NIST 800-88 (se possível) e colocados em um triturador industrial e fisicamente destruídos. A Microsoft mantém a responsabilidade pelos ativos que deixam o datacenter usando a limpeza/limpeza consistente do NIST SP 800-88, destruição de ativos, criptografia, inventário preciso, rastreamento e proteção da cadeia de custodia durante o transporte. Esse processo é monitorado por meio de televisão de circuito fechado e um Certificado de Destruição é emitido após a conclusão.

A Microsoft usa unidades de eliminação de dados de [Soluções de Protocolo Extremo](https://www.enterprisedataerasure.com/) (EPS). O software EPS dá suporte aos requisitos do NIST SP 800-88 para limpeza e limpeza/eliminação de segurança. Antes de limpar ou destruir, um inventário é criado pelo gerente de ativos da Microsoft. Se um fornecedor for usado para destruição, o fornecedor fornece um certificado de destruição para cada ativo destruído, que é validado pelo gerente de ativos.

## <a name="virtual-data-destruction"></a>Destruição de dados virtuais

A Microsoft tem políticas e procedimentos de tratamento de dados que abordam a destruição virtual efetiva de dados para proteger contra a possibilidade de dados serem compartilhados inadequadamente entre locatários de serviço ou serem acessíveis após a exclusão difícil no serviço. Os dados excluídos do serviço em um locatário não são acessíveis a outro locatário de serviço, mesmo que qualquer um dos armazenamentos físicos subjacentes seja reatribuido. Este é um resultado dos efeitos compostos de várias tecnologias de virtualização e fragmentação usadas para dimensionar ambientes virtuais, os comportamentos de exclusão ativa de aplicativos em cada locatário de serviço (como a zeroação de página [)](/office365/securitycompliance/office-365-exchange-online-data-deletion#page-zeroing)e os processos de criptografia de conteúdo de mídia e aplicativos necessários.