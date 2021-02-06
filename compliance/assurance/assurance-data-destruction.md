---
title: Destruição de dados no Microsoft 365
description: Uma visão geral das políticas da Microsoft sobre reciclagem, descarte ou destruição de servidores e unidades de disco do data center do Microsoft 365.
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
ms.openlocfilehash: d97c5f1be6bf09a772244aac14086171643af89e
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120670"
---
# <a name="data-destruction-in-microsoft-365"></a>Destruição de dados no Microsoft 365

## <a name="physical-data-destruction"></a>Destruição de dados físicos

A Microsoft tem políticas Padrão de Tratamento de Dados que abordam a reciclagem e o descarte de unidades de disco e servidores com falha ou retirada. Antes de reutilizar todas as unidades de disco do Microsoft 365, a Microsoft realiza um processo de higienização física consistente com a Publicação Especial 800-88 do Instituto Nacional de Padrões e Tecnologia[(NIST SP 800-88 Guidelines for Media Sanitization).](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-88r1.pdf) Como todas as unidades de disco no Microsoft 365 são criptografadas usando criptografia de nível de volume do BitLocker, a eliminação compatível com NIST SP 800-88 não é tecnicamente necessária. No entanto, a Microsoft realiza esse processo.

Discos com falha usados em datacenters do Microsoft 365 são destruídos fisicamente e auditados por meio do processo ISO. O tipo de ativo determina os meios apropriados de descarte. Para discos rígidos que não podem ser apagados, a Microsoft usa um processo de destruição para destruir a mídia e tornar impossível a recuperação de informações. Por exemplo, os discos são destruídos fisicamente, pulverizados ou apagados. A Microsoft retém todos os registros da destruição e realiza um processo de higienização semelhante em servidores reutilizados no Microsoft 365. Essas diretrizes abrangem a higienização eletrônica e física.

Cada datacenter usa um processo de destruição física local para descartar seus discos. As lixeiras seguras para mídia de armazenamento designada para descarte de disco estão em cada área do datacenter. Cada estação de lixeira segura tem monitoramento de vídeo. Depois que uma lixeira atinge aproximadamente 50% da capacidade, a equipe de Serviços de Site contata a equipe de Segurança Física para coordenar a remoção. A equipe de Serviços do Site e um Escritório de Segurança removem a lixeira de descarte segura e a colocam em uma área de armazenamento protegida designada. Políticas e procedimentos que regem a manipulação de dispositivos de suporte de dados durante o descarte são testados rotineiramente, incluindo procedimentos para garantir a condição de máquina aprovada para destruição.

No processo de destruição de dados, os discos são apagados de maneira compatível com NIST 800-88 (se possível) e, em seguida, colocados em um fragmentador industrial e fisicamente obrigados. A Microsoft mantém a responsabilidade pelos ativos que deixam o datacenter usando a limpeza/limpeza consistente do NIST SP 800-88, destruição de ativos, criptografia, inventário preciso, rastreamento e proteção da cadeia de custodia durante o transporte. Esse processo é monitorado por meio de televisão de circuito fechado e um Certificado de Destruição é emitido após a conclusão.

A Microsoft usa unidades de eliminação de dados de [Soluções de Protocolo Extremo](https://www.enterprisedataerasure.com/) (EPS). O software EPS dá suporte aos requisitos NIST SP 800-88 para limpeza e limpeza/eliminação segura. Antes de limpar ou destruir, um inventário é criado pelo gerenciador de ativos da Microsoft. Se um fornecedor for usado para destruição, o fornecedor fornece um certificado de destruição para cada ativo destruído, que é validado pelo gerente de ativos.

## <a name="virtual-data-destruction"></a>Destruição de dados virtuais

A Microsoft tem políticas e procedimentos de tratamento de dados que abordam a destruição virtual efetiva de dados para proteger contra a possibilidade de os dados serem compartilhados inadequadamente entre locatários de serviço ou serem acessíveis após a exclusão permanente no serviço. Os dados excluídos do serviço em um locatário não podem ser acessados por outro locatário de serviço, mesmo que qualquer armazenamento físico subjacente seja reatribuido. Isso é um resultado dos efeitos compostos de várias tecnologias de virtualização e fragmentação usadas para dimensionar ambientes virtuais, os comportamentos de exclusão ativos de aplicativos em cada locatário de serviço (como anulação de [página)](/office365/securitycompliance/office-365-exchange-online-data-deletion#page-zeroing)e os processos de criptografia de conteúdo de mídia e aplicativo necessários.