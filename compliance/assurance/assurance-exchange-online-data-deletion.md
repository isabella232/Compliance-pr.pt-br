---
title: Exclusão de dados do Microsoft 365 Exchange Online
description: Saiba como exclusões de dados rígidos e suaves para caixas de correio e itens em caixas de correio são tratadas no Exchange Online.
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
ms.openlocfilehash: b86c855a113706731ac6037a2851ae0f1adaccb9
ms.sourcegitcommit: b06fa9f1b230fd5e470817486ea51f460f28b691
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/27/2021
ms.locfileid: "50012957"
---
# <a name="exchange-online-data-deletion-in-microsoft-365"></a>Exclusão de dados do Exchange Online no Microsoft 365

No Exchange Online, há dois tipos de exclusões: exclusões suaves e exclusões permanentes. Isso se aplica a caixas de correio e itens dentro de uma caixa de correio.

## <a name="soft-deleted-and-hard-deleted-mailboxes"></a>Caixas de correio excluídas de forma fácil e permanente

Uma caixa de correio de usuário excluída de forma suave é uma caixa de correio que foi excluída usando o centro de administração do Microsoft 365 ou o cmdlet do Remove-Mailbox e ainda está na lixeira do Azure Active Directory há menos de 30 dias. Uma caixa de correio pode ser excluída de forma suave de qualquer uma das seguintes maneiras:

- A conta de usuário do Azure Active Directory associada à caixa de correio do usuário é excluída de forma temporário (o objeto de usuário está fora do escopo ou no contêiner da lixeira).
- A conta de usuário do Azure Active Directory associada à caixa de correio do usuário foi excluída ilegível, mas a caixa de correio do Exchange Online está sob uma responsabilidade de litígio ou de Descoberta Eletrônico.
- A conta de usuário do Azure Active Directory associada à caixa de correio do usuário foi limpa nos últimos 30 dias; que é o comprimento máximo de retenção que o Exchange Online manterá a caixa de correio em um estado de exclusão suave antes que ela seja permanentemente limpa e irrecuperável.

Uma caixa de correio de usuário excluída de forma permanente é uma caixa de correio que foi excluída de uma das seguintes maneiras:

- A caixa de correio do usuário foi excluída de forma temporário há mais de 30 dias, e o usuário associado do Azure Active Directory foi excluído imamente. Todo o conteúdo da caixa de correio, como emails, contatos e arquivos, é excluído permanentemente.
- A conta de usuário associada à caixa de correio do usuário foi excluída ilegitivamente do Azure Active Directory. A caixa de correio do usuário agora é excluída de forma suave no Exchange Online e permanece em um estado de exclusão por 30 dias. Se, no período de 30 dias, um novo usuário do Azure Active Directory for sincronizado da conta de destinatário original com o mesmo **ExchangeGuid** ou **ArchiveGuid** e essa nova conta estiver licenciada para o Exchange Online, isso resultará em uma exclusão permanente da caixa de correio do usuário original. Todo o conteúdo da caixa de correio, como emails, contatos e arquivos, é excluído permanentemente.
- Uma caixa de correio excluída de forma suave é excluída **usando Remove-Mailbox -PermanentlyDelete**.

Os cenários de exclusão acima pressupom que a caixa de correio do usuário não está em nenhum dos estados de espera, como a responsabilidade por litígio ou a descoberta de eDiscovery. Se houver algum tipo de espera na caixa de correio, a caixa de correio não poderá ser excluída. Para todos os tipos de [](https://support.office.com/article/manage-legal-investigations-in-office-365-2e5fbe9f-ee4d-4178-8ff8-4356bc1b168e?ui=en-US&rs=en-US&ad=US) destinatários de usuário de email, qualquer configuração de Espera será ignorada e não terá efeito em exclusões permanentes ou exclusões suaves.

## <a name="soft-deleted-and-hard-deleted-items"></a>Itens excluídos de forma suave e permanente

Quando um usuário exclui um item de caixa de correio (como uma mensagem de email, um contato, um compromisso de calendário ou uma tarefa), o item é movido para a pasta Itens Recuperáveis e para uma subpasta chamada "Exclusões". Isso é conhecido como exclusão suave. O tempo de permanência dos itens excluídos na pasta Exclusões depende do período de retenção do item excluído que é definido para a caixa de correio. Uma caixa de correio do Exchange Online mantém os itens excluídos por 14 dias por padrão, mas os administradores do Exchange Online podem alterar essa configuração para aumentar o período para um máximo de 30 dias. (Para etapas detalhadas para aumentar o período de retenção de itens excluídos para uma caixa de correio do Exchange Online, confira Alterar por quanto tempo os itens excluídos permanentemente são mantidos para uma caixa de correio do [Exchange Online.)](https://docs.microsoft.com/exchange/recipients-in-exchange-online/manage-user-mailboxes/change-deleted-item-retention) Os usuários podem recuperar ou limpar itens excluídos antes que o tempo de retenção de um item excluído expire. Para fazer isso, eles usam o recurso Recuperar Itens Excluídos no Microsoft Outlook ou no Outlook na Web.

Se um usuário limpa um item excluído usando o recurso Recuperar Itens Excluídos no Outlook ou no Outlook na Web, isso é conhecido como exclusão permanente. No Exchange Online, a recuperação de item único é habilitada [](https://docs.microsoft.com/Exchange/recipients/user-mailboxes/recover-deleted-messages) por padrão quando uma nova caixa de correio é criada, para que um administrador ainda possa recuperar itens excluídos de forma permanente antes que o período de retenção do item excluído expire. Além disso, se uma mensagem for alterada por um usuário ou por um processo, as cópias do item original também serão mantidas quando a recuperação de item único estiver habilitada.

## <a name="page-zeroing"></a>Zero de página

*A zero* é um mecanismo de segurança que grava zeros ou um padrão binário sobre dados excluídos para que os dados excluídos seja mais difícil de recuperar. No Exchange Online, os bancos de dados de caixa de correio *usam* páginas como unidade de armazenamento e implementam um processo de substituição chamado *anulação de página.* A zeroação de página é habilitada por padrão e não pode ser desabilitada por clientes ou pela Microsoft. As operações de anulação de página são registradas nos arquivos de log de transações para que todas as cópias de um determinado banco de dados sejam anuladas por página de maneira semelhante. Anulando uma página em uma cópia de banco de dados ativa faz com que a página seja anulada em cópias passivas do banco de dados.

A zeroação de página grava um padrão binário sobre registros excluídos de forma permanente. O padrão de zero página é específico para operações do Mecanismo de Armazenamento Extensível (ESE) (o nome do mecanismo de banco de dados interno usado pelos servidores no Exchange Online) e é diferente para operações em tempo de executar versus operações de manutenção de banco de dados em segundo plano. (A manutenção de banco de dados em segundo plano é um processo que verifica continuamente cada banco de dados. Sua função principal é a verificação de páginas de banco de dados, mas também lida com a limpeza do espaço e a reação de registros e páginas que não foram zeradas por causa de uma falha na Loja.)

A tabela a seguir lista os padrões de preenchimento que correspondem a operações em tempo de execução específicas.

| Operação em tempo real do ESE   | Padrão de preenchimento |
|--------------------------|--------------|
| Substituir                  | R            |
| Exclusão de valor longo/registro | D            |
| Liberação de espaço em página         | H            |

A tabela a seguir lista os padrões de preenchimento que correspondem a operações específicas que ocorrem durante a manutenção de banco de dados em segundo plano do ESE.

| Operação de manutenção de banco de dados em segundo plano do ESE | Padrão de preenchimento |
|-----------------------------------------------|--------------|
| Exclusão de gravação                                 | D            |
| Exclusão de valor longo                             | L            |
| Liberação de espaço em página parcialmente utilizada       | Z            |
| Liberação de espaço em página não utilizada               | U            |

### <a name="page-zeroing-process"></a>Processo de reação de página

O processo de zero de página depende do cenário de exclusão. A tabela a seguir discute os cenários de exclusão de banco de dados, e quando as funções de anulação de página ocorrem.

| Cenário de exclusão de banco de dados | Processo do ESE e tempo para anulação dos dados do banco de dados |
|:--------------------------|:------------------------------------------------|
| O item expira com base no período de retenção do item excluído. | Um thread assíncrono grava um padrão binário sobre os dados excluídos. Essa ação ocorre milissegundos após a exclusão do registro. Se o processo do Store falhar enquanto o trabalho de anulação assíncrona ainda estiver pendente (ou a limpeza do armazenamento de versão for cancelada devido ao crescimento do armazenamento de versão), a anulação será concluída quando a manutenção do banco de dados em segundo plano processar essa seção do banco de dados. |
| Cenário de exibição: Expiração de itens do Outlook/Outlook na exibição de pasta da Web (por exemplo, exibição de conversa) | A anulação de dados ocorre quando uma manutenção de banco de dados em segundo plano processa esta seção do banco de dados. |
| Cenário mover caixa de correio/excluir caixa de correio: caixa de correio de origem excluída (expiração da caixa de correio excluída) | A anulação de dados ocorre quando uma manutenção de banco de dados em segundo plano processa esta seção do banco de dados. |

### <a name="mailbox-data-types-without-page-zeroing"></a>Tipos de dados de caixa de correio sem a reação de página

Os tipos de dados de caixa de correio a seguir não têm provisões para a zeroação de página:

- Logs de transação de banco de dados de caixa de correio **-** Quando os logs de transações são excluídos como parte das operações normais, não há nenhum processo para zerar os blocos no sistema de arquivos que armazenou o(s) arquivo(s) de log excluído(s). É provável que o sistema de arquivos reutilize rapidamente esse espaço livre para logs recém-criados, mas não há garantia de que isso acontecerá.
- **Arquivos de catálogo de índice de** conteúdo - O Exchange Online usa o Search Foundation (também conhecido como FAST) para a funcionalidade de indexação de pesquisa. O catálogo de índices de pesquisa é composto por várias dezenas de arquivos armazenados no mesmo volume do arquivo de banco de dados de caixa de correio. Quando um arquivo é excluído de forma irreversível do banco de dados de caixa de correio, o conteúdo associado no catálogo de pesquisa não é excluído imediatamente. A exclusão de conteúdo ocorre quando o Search Foundation faz uma sombra (ou mesclagem mestra) de muitos arquivos de catálogo pequenos em um único arquivo maior. Depois que a mesclagem mestre é concluída, os arquivos menores de catálogo são excluídos. Não há nenhum processo para zerar os blocos que armazenaram os arquivos de catálogo excluídos.

## <a name="continuous-replication"></a>Replicação contínua

A replicação contínua (também conhecida como envio e repetição de log) é tecnologia no Exchange Online que cria e mantém cópias de cada banco de dados de caixa de correio para fornecer alta disponibilidade, resiliência de site e recuperação de desastres. A replicação contínua usa o suporte à recuperação de falhas do banco de dados do Exchange Server para fornecer tecnologia que executa a atualização assíncrona de uma ou mais cópias de um banco de dados de caixa de correio. Cada servidor de caixa de correio registra atualizações de banco de dados feitas em um banco de dados ativo (por exemplo, atividade de email do usuário) como registros de log em um conjunto sequencial de arquivos de log de transações de 1 MB. Esse conjunto de arquivos é conhecido como fluxo de log. Na replicação contínua, o fluxo de log também é usado para atualizar de forma assíncrona uma ou mais cópias de um banco de dados. Isso é realizado transmitindo os logs para um local que contém uma cópia passiva do banco de dados ativo e, em seguida, reproduzindo-os na cópia passiva do banco de dados. Se todos os logs do banco de dados ativo são repetidos em relação a uma cópia passiva do banco de dados, os dois bancos de dados são equivalentes e é por esse processo que qualquer alteração física feita em um banco de dados ativo é replicada para todas as cópias passivas desse banco de dados.

Qualquer exclusão de um banco de dados de caixa de correio, seja um item de caixa de correio ou uma caixa de correio inteira, e se uma exclusão suave ou exclusão permanente, representa uma alteração física no banco de dados ativo. A zera de página também envolve fazer alterações físicas no banco de dados ativo. Essas alterações são escritas nos arquivos de log por meio de um processo chamado replicação contínua e, quando esses arquivos de log são replicados em cópias passivas do banco de dados, as mesmas alterações físicas são feitas nesses bancos de dados passivos.
