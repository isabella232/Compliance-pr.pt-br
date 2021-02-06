---
title: Imutabilidade de dados no Microsoft 365
description: Saiba como o Microsoft 365 preserva dados em formato para descobrir a conformidade regulamentar, os requisitos de governança interna e os riscos de litígio.
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
ms.openlocfilehash: da465b850a9216dd64f8e4d9e6450c6a17f7b26d
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120660"
---
# <a name="data-immutability-in-microsoft-365"></a>Imutabilidade de dados no Microsoft 365

A conformidade regulamentar, os requisitos de governança interna ou os riscos de litígio exigem que as organizações preservem emails e dados associados em uma forma que pode ser descoberta. Todos os dados no sistema devem ser descobertos e nenhum deles pode ser destruído ou alterado. O termo padrão do setor para isso é "imutabilidade".

Métodos tradicionais de imutabilidade geralmente funcionava movendo mensagens de email para um local de armazenamento separado somente leitura. Embora esses sistemas servem para preservar itens de caixa de correio para descoberta, eles geralmente afetam a experiência do usuário removendo itens preservados do fluxo de trabalho diário personalizado. Para profissionais de TI, essa abordagem de imutabilidade requer a implantação e a manutenção contínua de uma infraestrutura separada de servidor e armazenamento. A descoberta é realizada com ferramentas externas ao sistema de email e inclui os custos associados de implantação e manutenção.

Por meio dos recursos de política de retenção e preservação no local de arquivamento no Microsoft 365 e em seus serviços, você pode preservar e reter muitas classes de dados de entrada, internos e de saída. Isso inclui:

- Comunicações de email de entrada e saída
- Livros e registros contidos no formulário de email ou em documentos online compartilhados
- Solicitações de reunião
- Faxes
- Mensagens instantâneas
- Documentos compartilhados durante reuniões online
- Voicemails

Além disso, a Microsoft desenvolveu recursos [](https://support.office.com/article/Archiving-third-party-data-in-Office-365-0ce338d5-3666-4a18-86ab-c6910ff408cc) de complemento para permitir o arquivamento de dados de outras fontes por meio da integração com soluções de captura e gerenciamento de dados de terceiros. Depois que os dados de terceiros são importados, você pode aplicar recursos de conformidade do Microsoft 365 aos dados, incluindo:

- [Retenção de litígio](/microsoft-365/compliance/create-a-litigation-hold)
- [Descoberta e Espera In-loco](/microsoft-365/compliance/manage-legal-investigations)
- [Pesquisa de Conformidade](/microsoft-365/compliance/search-for-content)
- [Arquivamento no Local](/microsoft-365/compliance/enable-archive-mailboxes)
- [Auditoria de caixa de correio](/microsoft-365/compliance/enable-mailbox-auditing)
- [Políticas de retenção](/microsoft-365/compliance/retention-policies)

Por exemplo, quando uma caixa de correio é colocada em Litígio, os dados de terceiros são preservados. Você pode pesquisar dados de terceiros usando a In-Place eDiscovery ou a Pesquisa de Conformidade. Ou você pode aplicar políticas de arquivamento e retenção a dados de terceiros, assim como faz para os dados da Microsoft. O arquivamento de dados de terceiros no Microsoft 365 ajuda sua organização a manter a conformidade com políticas governamentais e regulatórias.

O arquivamento no Microsoft 365 fornece armazenamento compatível com a Regra 17a-4 da Sec (Comissão de Valores Mobiliários e Câmbio). O Microsoft 365 preserva arquivos permanentes de todos os dados coletados em um formato não reescrevível e não-reescrita usando políticas de retenção in-loco e políticas de preservação, incluindo o bloqueio de preservação.

Especificamente:

- Todos os registros armazenados usando as políticas de retenção mencionadas acima são mantidos em uma área de armazenamento dedicada fora da visualização do usuário comum. Somente usuários autorizados podem acessar e pesquisar esses registros, mas não podem alterá-los ou apagá-los.
- Os metadados de cada item incluem um timestamp usado no cálculo da duração da retenção. Os timestamps são aplicados quando um novo item é recebido ou criado e não podem ser modificados ou removidos dos metadados.
- O arquivamento no Microsoft 365 permite que os usuários combinem diferentes políticas de retenção e realizam ações para criar políticas de retenção granulares. Essas políticas definem o tipo ou local dos itens preservados e a duração da preservação.
- O recurso Bloqueio de Preservação permite que os usuários escolham se a política será restritiva. Uma política restritiva proíbe que qualquer pessoa tenha a capacidade de remover, desabilitar ou fazer alterações na política de retenção. Isso significa que, depois que o Bloqueio de Preservação for habilitado, ele não poderá ser desabilitado, e nenhum mecanismo existirá sob o qual quaisquer dados de custodiantes existentes coletados pelas políticas de retenção in-loco possam ser substituídos, modificados, apagados ou excluídos durante o período de preservação. Além disso, o período de espera definido pelo Bloqueio de Preservação pode não ser reduzido ou diminuído. No entanto, ele pode ser alongado, no caso de um requisito legal para continuar a retenção dos dados armazenados, conforme mencionado acima. O Bloqueio de Preservação garante que ninguém, nem mesmo os administradores ou aqueles com determinado acesso de controle, possam alterar as configurações, substituir ou apagar dados armazenados, colocando o arquivamento no Microsoft 365 em linha com as diretrizes definidas na Versão 2003 da Regra 17a-4 da SEC.

Para entender como o Microsoft 365 ajuda você a cumprir obrigações regulatórias, especificamente em relação aos requisitos da Regra 17a-4, confira o [whitepaper](https://www.microsoft.com/microsoft-365/blog/wp-content/uploads/2015/11/Microsoft-EOA-White-Paper.pdf) que aborda o Arquivamento do Exchange Online, o SharePoint Online, o OneDrive for Business e o Skype for Business. O whitepaper também fornece uma análise detalhada dos recursos e funcionalidades de arquivamento do Microsoft 365 em relação a cada um dos requisitos da regra 17a-4 da SEC e demonstra aos clientes regulamentados como o arquivamento do Microsoft 365 pode permitir que eles atenderem a esses requisitos.
