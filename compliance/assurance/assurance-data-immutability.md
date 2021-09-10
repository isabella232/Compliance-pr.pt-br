---
title: Imutabilidade de dados no Microsoft 365
description: Saiba como Microsoft 365 preserva dados na forma de descoberta para lidar com a conformidade regulamentar, os requisitos de governança interna e os riscos de litígio.
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
ms.openlocfilehash: e17685c7d927ab8188abe1ef4dae4d2cdf0f3764
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2021
ms.locfileid: "58946871"
---
# <a name="data-immutability-in-microsoft-365"></a>Imutabilidade de dados no Microsoft 365

A conformidade regulamentar, os requisitos de governança interna ou os riscos de litígio exigem que as organizações preservem emails e dados associados em um formulário descobrivel. Todos os dados no sistema devem ser descobertos e nenhum deles pode ser destruído ou alterado. O termo padrão do setor para isso é "imutabilidade".

Métodos tradicionais para imutabilidade normalmente funcionava movendo mensagens de email para um local de armazenamento separado somente leitura. Embora esses sistemas sirva para preservar itens de caixa de correio para descoberta, eles geralmente afetam a experiência do usuário removendo itens preservados do fluxo de trabalho diário personalizado. Para profissionais de TI, essa abordagem de imutabilidade requer a implantação e a manutenção contínua de uma infraestrutura de armazenamento e servidor separados. A descoberta é realizada com ferramentas externas ao sistema de email e inclui custos associados de implantação e manutenção.

Por meio dos recursos de política de retenção e preservação in-locar de arquivamento no Microsoft 365 e seus serviços, você pode preservar e reter muitas classes de dados de entrada, internos e de saída. Isso inclui:

- Comunicações por email de entrada e saída
- Livros e registros contidos no formulário de email ou em documentos online compartilhados
- Solicitações de reunião
- Faxes
- Mensagens instantâneas
- Documentos compartilhados durante reuniões online
- Caixas postais

Além disso, a Microsoft desenvolveu recursos [](https://support.office.com/article/Archiving-third-party-data-in-Office-365-0ce338d5-3666-4a18-86ab-c6910ff408cc) de complemento para permitir o arquivamento de dados de outras fontes por meio da integração com soluções de gerenciamento e captura de dados de terceiros. Depois que os dados de terceiros são importados, você pode aplicar Microsoft 365 de conformidade aos dados, incluindo:

- [Retenção de litígio](/microsoft-365/compliance/create-a-litigation-hold)
- [Bloqueio e Descoberta Eletrônica In-loco](/microsoft-365/compliance/manage-legal-investigations)
- [Pesquisa de Conformidade](/microsoft-365/compliance/search-for-content)
- [Arquivamento no Local](/microsoft-365/compliance/enable-archive-mailboxes)
- [Auditoria de caixa de correio](/microsoft-365/compliance/enable-mailbox-auditing)
- [Políticas de retenção](/microsoft-365/compliance/retention-policies)

Por exemplo, quando uma caixa de correio é colocada em Contencioso, os dados de terceiros são preservados. Você pode pesquisar dados de terceiros usando In-Place Descoberta eDiscovery ou Pesquisa de Conformidade. Ou você pode aplicar políticas de arquivamento e retenção a dados de terceiros, assim como pode para dados da Microsoft. O arquivamento de dados de terceiros em Microsoft 365 ajuda sua organização a permanecer em conformidade com políticas governamentais e regulatórias.

O arquivamento em Microsoft 365 fornece armazenamento compatível com a Regra 17a-4 da Securities e Exchange Sec (SEC). Microsoft 365 preserva arquivos permanentes de todos os dados coletados em um formato não regravável e não a apagavel usando políticas de retenção in-loco e políticas de preservação, incluindo bloqueio de preservação.

Especificamente:

- Todos os registros armazenados usando as políticas de retenção mencionadas acima são mantidos em uma área de armazenamento dedicada fora da alçada do usuário comum. Somente usuários autorizados podem acessar e pesquisar esses registros, mas não podem alterá-los ou apagá-los.
- Os metadados para cada item incluem um data/hora usado no cálculo da duração da retenção. Os dados de data/hora são aplicados quando um novo item é recebido ou criado e não podem ser modificados ou removidos dos metadados.
- O arquivamento no Microsoft 365 permite que os usuários combinem políticas de retenção diferentes e mantenha ações para criar políticas de retenção granulares. Essas políticas definem o tipo ou local dos itens preservados e a duração da preservação.
- O recurso Bloqueio de Preservação permite que os usuários escolham se a política é restritiva. Uma política restritiva proíbe qualquer pessoa de ter a capacidade de remover, desabilitar ou fazer alterações na política de retenção. Isso significa que, depois que o Bloqueio de Preservação for habilitado, ele não poderá ser desabilitado e nenhum mecanismo existirá no qual quaisquer dados de custodiantes existentes coletados pelas políticas de retenção no local possam ser substituídos, modificados, apagados ou excluídos durante o período de preservação. Além disso, o período de bloqueio definido pelo Bloqueio de Preservação pode não ser reduzido ou reduzido. Ele pode, no entanto, ser alongado, no caso de um requisito legal para continuar a retenção dos dados armazenados, conforme mencionado acima. O Bloqueio de Preservação garante que ninguém, nem mesmo os administradores ou aqueles com determinado acesso de controle, possam alterar as configurações ou substituir ou apagar dados armazenados, colocando o arquivamento no Microsoft 365 em conformidade com as diretrizes definidas na Versão 2003 da Regra SEC 17a-4.

Para entender como Microsoft 365 ajuda você a cumprir obrigações regulatórias, especificamente em relação aos requisitos da Regra 17a-4, consulte o [whitepaper](https://www.microsoft.com/microsoft-365/blog/wp-content/uploads/2015/11/Microsoft-EOA-White-Paper.pdf) que abrange Arquivamento do Exchange Online, SharePoint Online, OneDrive for Business e Skype for Business. O whitepaper também fornece uma análise detalhada dos recursos e funcionalidades de arquivamento do Microsoft 365 em relação a cada um dos requisitos da Regra SEC 17a-4 e demonstra aos clientes regulamentados como o arquivamento Microsoft 365 pode permitir que eles atendem a esses requisitos.
