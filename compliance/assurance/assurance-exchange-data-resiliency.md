---
title: Resiliência de dados do Exchange Online no Microsoft 365
description: Neste artigo, encontre uma explicação dos vários aspectos da resiliência de dados no Exchange Online e no Microsoft 365.
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
ms.openlocfilehash: 2cdd37d34612421cc7a9e4687134e2a1e2b1aeec
ms.sourcegitcommit: b06fa9f1b230fd5e470817486ea51f460f28b691
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/27/2021
ms.locfileid: "50012937"
---
# <a name="exchange-online-data-resiliency-in-microsoft-365"></a>Resiliência de dados do Exchange Online no Microsoft 365

>[!IMPORTANT]
>À medida que continuamos investindo em maneiras diferentes de preservar o conteúdo da caixa de correio, anunciamos a ressarção do In-Place Holds no Centro de administração do Exchange (EAC) no Exchange Online. A partir de 1º de julho de 2020, você não poderá criar novas re In-Place Retém. Mas você ainda poderá gerenciar In-Place Retém no EAC ou usando o cmdlet **Set-MailboxSearch** no PowerShell do Exchange Online. No entanto, a partir de 1º de outubro de 2020, você não poderá gerenciar o In-Place Retém. Você só poderá removê-los no EAC ou usando o cmdlet **Remove-MailboxSearch.** Ainda haverá suporte para In-Place Respaldados no Exchange Server e em implantações híbridas do Exchange. For more information about the retirement of In-Place Holds in Exchange Online, see [Retirement of legacy eDiscovery tools](https://docs.microsoft.com/microsoft-365/compliance/legacy-ediscovery-retirement).

Um In-Place preserva todo o conteúdo da caixa de correio, incluindo itens excluídos e versões originais de itens modificados. Todos os itens da caixa de correio são retornados em uma pesquisa de [Descoberta eletrônica In-loco](https://docs.microsoft.com/exchange/security-and-compliance/in-place-ediscovery/in-place-ediscovery). Quando você coloca um In-Place de correio de um usuário, o conteúdo na caixa de correio de arquivo morto correspondente (se estiver habilitada) também é colocado em espera e retornado em uma pesquisa de Descoberta Eletrônico.

Há dois tipos de corrupção que podem afetar um banco de dados do Exchange: corrupção física, que normalmente é causada por problemas de hardware (em particular, hardware de armazenamento) e dano lógico, que ocorre devido a outros fatores. Geralmente, há dois tipos de corrupção lógica que podem ocorrer em um banco de dados do Exchange:

- **Corrupção lógica do banco de** dados - A verificação da página do banco de dados corresponde, mas os dados na página estão errados logicamente. Isso pode ocorrer quando o mecanismo de banco de dados (o Mecanismo de Armazenamento Extensível (ESE)) tenta gravar uma página de banco de dados e, mesmo que o sistema operacional retorne uma mensagem de sucesso, os dados nunca são gravados no disco ou são gravados no lugar errado. Isso é conhecido como *liberação perdida*. O ESE inclui vários recursos e proteções projetados para evitar a corrupção física de um banco de dados e outros cenários de perda de dados. Para evitar que liberações perdidas percam dados, o ESE inclui um mecanismo de detecção de liberação perdida no banco de dados juntamente com um recurso (restauração de página única) para corrigi-lo.
- **Armazenar corrupção lógica** - Os dados são adicionados, excluídos ou manipulados de uma maneira que o usuário não espera. Esses casos são causados por aplicativos de terceiros. Geralmente, é corrupção no sentido de que o usuário o vê como corrupção. O repositório do Exchange considera a transação que produziu o dano lógico uma série de operações MAPI válidas. Os [recursos de](https://docs.microsoft.com/exchange/security-and-compliance/create-or-remove-in-place-holds) Reter Local no Exchange Online oferece proteção contra corrupção lógica do armazenamento (porque impede que o conteúdo seja excluído permanentemente por um usuário ou um aplicativo). 

O Exchange Online realiza várias verificações de consistência nos arquivos de log replicados durante a inspeção de log e a repetição de log. Essas verificações de consistência impedem que a corrupção física seja replicada pelo sistema. Por exemplo, durante a inspeção de log, há uma verificação de integridade física que verifica o arquivo de log e valida que a verificação registrada no arquivo de log corresponde à verificação gerada na memória. Além disso, o header do arquivo de log é examinado para garantir que a assinatura do arquivo de log registrada no header do log corresponde à do arquivo de log. Durante a repetição do log, o arquivo de log passa por mais exames. Por exemplo, o header do banco de dados também contém a assinatura de log que é comparada com a assinatura do arquivo de log para garantir que eles se matchm. 

A proteção contra corrupção de dados de caixa de correio no Exchange Online é alcançada usando a Proteção de Dados Nativa do Exchange, uma estratégia de resiliência que aproveita a replicação no nível do aplicativo em vários servidores e vários datacenters, juntamente com outros recursos que ajudam a proteger os dados contra perda devido a corrupção ou outros motivos. Esses recursos incluem recursos nativos gerenciados pela Microsoft ou pelo próprio aplicativo do Exchange Online, como:

- [Grupos de Disponibilidade de Dados](https://docs.microsoft.com/exchange/back-up-email)
- Correção de bit único 
- Verificação de banco de dados online 
- Detecção de liberação perdida 
- Restauração de página única 
- Serviço de Replicação de Caixa de Correio 
- Verificações do arquivo de log 
- Implantação em sistema de arquivos resiliente 

Para obter mais informações sobre os recursos nativos listados anteriormente, selecione os hiperlinks e consulte o seguinte para obter informações adicionais e para obter detalhes sobre itens sem hiperlinks. Além desses recursos nativos, o Exchange Online também inclui recursos de resiliência de dados que os clientes podem gerenciar, como: 
- [Recuperação de Item Único (habilitada por padrão)](https://docs.microsoft.com/exchange/recipients-in-exchange-online/manage-user-mailboxes/recover-deleted-messages) 
- [Bloqueio In-loco e Retenção de Litígio](https://docs.microsoft.com/exchange/security-and-compliance/in-place-and-litigation-holds) 
- [Caixas de correio de retenção e Soft-Deleted itens excluídos (ambas habilitadas por padrão)](https://docs.microsoft.com/exchange/recipients-in-exchange-online/delete-or-restore-mailboxes) 

## <a name="database-availability-groups"></a>Grupos de Disponibilidade de Banco de Dados 
Cada banco de dados de caixa de correio no Microsoft 365 é hospedado em um grupo de disponibilidade de banco de dados [(DAG)](https://docs.microsoft.com/exchange/back-up-email) e replicado para datacenters geograficamente separados dentro da mesma região. A configuração mais comum é quatro cópias de banco de dados em quatro datacenters; No entanto, algumas regiões têm menos datacenters (os bancos de dados são replicados para três datacenters na Índia e dois datacenters na Austrália e no Japão). Mas, em todos os casos, cada banco de dados de caixa de correio tem quatro cópias distribuídas em vários datacenters, garantindo assim que os dados da caixa de correio sejam protegidos contra falhas de software, hardware e até mesmo datacenter. 

Dessas quatro cópias, três delas estão configuradas como altamente disponíveis. A quarta cópia é configurada como uma cópia [de banco de dados com tempo.](https://docs.microsoft.com/Exchange/high-availability/manage-ha/activate-lagged-db-copies) A cópia de banco de dados com tempo não se destina à recuperação de caixa de correio individual ou à recuperação de item de caixa de correio. Seu objetivo é fornecer um mecanismo de recuperação para o raro evento de corrupção lógica catastrófica em todo o sistema. 

As cópias de banco de dados com retardo no Exchange Online são configuradas com um tempo de retardo de repetição do arquivo de log de sete dias. Além disso, o Gerenciador de Retardo de Repetição do Exchange está habilitado para fornecer o arquivo de log dinâmico para cópias com retardo a fim de permitir que as cópias de banco de dados com retardo reparem e gerenciem o crescimento do arquivo de log. Embora as cópias de banco de dados comfaçadas sejam usadas no Exchange Online, é importante entender que elas não são um backup de ponto no tempo garantido. As cópias de banco de dados com espera no Exchange Online têm um limite de disponibilidade, geralmente em torno de 90%, devido aos períodos em que o disco que contém uma cópia com tempo é perdido devido a uma falha de disco, a cópia comfasagem se torna uma cópia altamente disponível (devido à reprodução automática), bem como os períodos em que a cópia de banco de dados com espera está recriando a fila de repetição do log. 

## <a name="transport-resilience"></a>Resiliência de transporte 
O Exchange Online inclui dois recursos principais de resiliência de transporte: Redundância de Sombra e Rede De Segurança. A Redundância de Sombra mantém uma cópia redundante de uma mensagem enquanto ela está em trânsito. A Rede Segura mantém uma cópia redundante de uma mensagem após a entrega bem-sucedida da mensagem. 

Com a Redundância de Sombra, cada servidor de transporte do Exchange Online faz uma cópia de cada mensagem que recebe antes de confirmar o recebimento bem-sucedido da mensagem para o servidor de envio. Isso torna redundantes todas as mensagens no pipeline de transporte em trânsito. Se o Exchange Online determinar que a mensagem original foi perdida em trânsito, uma cópia redundante da mensagem será entregue outra vez. 

Rede Segura é uma fila de transporte associada ao serviço de Transporte em um servidor de Caixa de Correio. Essa fila armazena cópias de mensagens que foram processadas com êxito pelo servidor. Quando um banco de dados de caixa de correio ou um servidor exige a ativação de uma cópia des date do banco de dados de caixa de correio, as mensagens na fila rede de segurança são automaticamente retransmitidas para a nova cópia ativa do banco de dados de caixa de correio. A Rede Segura também é redundante, eliminando o transporte como um único ponto de falha. Ele usa o conceito de uma Rede de Segurança Primária e uma Rede De Segurança de Sombra, em que, se a Rede De Segurança Primária não estiver disponível por mais de 12 horas, as solicitações de reenviação se tornarão solicitações de reenviação de sombra e as mensagens serão entregues de volta da Rede De Segurança de Sombra.

As reenviações de mensagens da Rede Segura são iniciadas automaticamente pelo componente Active Manager do serviço de Replicação do Microsoft Exchange que gerencia DAGs e cópias de banco de dados de caixa de correio. Nenhuma ação manual é necessária para remmitir mensagens da Rede Segura. 

## <a name="single-bit-correction"></a>Correção de bit único 
O ESE inclui um mecanismo para detectar e resolver erros de CRC de bit único (também conhecidos como invasões de bit único) que são o resultado de erros de hardware (e, como tal, representam corrupção física). Quando esses erros ocorrem, o ESE os corrige automaticamente e registra um evento no log de eventos. 

## <a name="online-database-scanning"></a>Verificação de banco de dados online 
A verificação de banco de dados online (também conhecida como somatório de verificação de banco de *dados)* é o processo em que um ESE usa um verificador de consistência de banco de dados para ler cada página e verificar se há corrupção de página. O objetivo principal é detectar danos físicos e liberações perdidas que podem não estar sendo detectadas por operações transacionais. A verificação de banco de dados também executa operações de falha pós-armazenamento. O espaço pode ser vazado devido a falhas e a verificação de banco de dados online localiza e recupera espaço perdido. O sistema é projetado com a expectativa de que todos os bancos de dados são totalmente verificados uma vez a cada sete dias. 

## <a name="lost-flush-detection"></a>Detecção de liberação perdida 
Uma liberação perdida ocorre quando uma operação de gravação de banco de dados que o subsistema/sistema operacional de disco retornado como concluído não foi realmente gravado no disco ou foi escrita no local errado. Os incidentes de liberação perdida podem resultar em corrupção lógica do banco de dados, portanto, para evitar que liberações perdidas resultem em dados perdidos, o ESE inclui um mecanismo de detecção de liberação perdida. À medida que as páginas de banco de dados são escritas em cópias passivas, é realizada uma verificação de liberações perdidas na cópia ativa. Se uma liberação perdida for detectada, o ESE poderá reparar o processo usando um processo de correção de página. 

## <a name="single-page-restore"></a>Restauração de página única 
A restauração de página única, também conhecida como correção de *página,* é um processo automático em que as páginas corrompidas do banco de dados são substituídas por cópias saudável de uma réplica saudável. O processo de reparo de uma página corrompida depende de a cópia do banco de dados ser ativa ou passiva. Quando uma cópia de banco de dados ativa encontra uma página corrompida, ela pode copiar uma página de uma de suas réplicas, desde que a página que copia está atualizada. Esse processo é realizado colocando uma solicitação para a página no fluxo de log, que é a base da replicação de banco de dados de caixa de correio. Assim que uma réplica encontra a solicitação de página, ela responde enviando uma cópia da página para a cópia do banco de dados solicitante. A restauração de página única também fornece um mecanismo de comunicação assíncrona para o ativo solicitar uma página de réplicas, mesmo se as réplicas estão offline no momento. 

Em caso de corrupção em uma cópia de banco de dados passiva, incluindo uma cópia de banco de dados com atraso, como essas cópias estão sempre atrás de sua cópia ativa, é sempre seguro copiar qualquer página da cópia ativa para uma cópia passiva. Uma cópia de banco de dados passiva é, por natureza, altamente disponível, portanto, durante o processo de correção de página, a reprodução de log é suspensa, mas a cópia de log continua. A cópia passiva do banco de dados recupera uma cópia da página corrompida da cópia ativa, aguarda até que o arquivo de log que atende ao requisito máximo necessário de geração de log seja copiado e inspecionado e, em seguida, correção da página corrompida. Depois que a página tiver sido corrigida, a repetição de log será retomada. O processo é o mesmo para a cópia de banco de dados com tempo, exceto pelo fato de que o banco de dados com tempo defasado primeiro reproduz todos os arquivos de log necessários para alcançar um estado a patches. 

## <a name="mailbox-replication-service"></a>Serviço de Replicação de Caixa de Correio 
Mover caixas de correio é uma parte importante do gerenciamento de um serviço de email em grande escala. Sempre há tecnologias atualizadas e atualizações de hardware e versão para lidar, portanto, ter um sistema robusto e acelerador que permite que nossos engenheiros realizem esse trabalho, mantendo a caixa de correio transparente para os usuários (ao garantir que eles permaneçam online durante todo o processo) é fundamental e garantir que o processo seja ampliado normalmente à medida que as caixas de correio ficam maiores e maiores. 

O Serviço de Replicação de Caixa de Correio do Exchange (MRS) é responsável por mover caixas de correio entre bancos de dados. Durante a movimentação, o MRS realiza uma verificação de consistência em todos os itens da caixa de correio. Se for encontrado um problema de consistência, o MRS corrigirá o problema ou ignorará os itens corrompidos, removendo, assim, a corrupção da caixa de correio. 

Como o MRS é um componente do Exchange Online, podemos fazer alterações em seu código para lidar com novas formas de corrupção detectadas no futuro. Por exemplo, se detectarmos um problema de consistência que o MRS não consegue corrigir, podemos analisar a corrupção, alterar o código MRS e corrigir a inconsistência (se entendermos como fazer). 

## <a name="log-file-checks"></a>Verificações do arquivo de log 
Todos os arquivos de log de transações gerados por um banco de dados do Exchange passam por várias formas de verificações de consistência. Quando um arquivo de log é criado, a primeira coisa a fazer é um padrão de bits é gravado e, em seguida, uma série de gravações de log é executada. Essa estrutura permite que o Exchange Online execute uma série de verificações (liberação perdida, CRC e outras verificações) para validar cada arquivo de log conforme ele é gravado e novamente conforme é replicado. 

## <a name="deployment-on-resilient-file-system"></a>Implantação em sistema de arquivos resiliente 
Para ajudar a evitar que a corrupção ocorra no nível do sistema de arquivos, o Exchange Online está sendo implantado em partições do Sistema de Arquivos Resiliente (ReFS) para fornecer recursos de recuperação aprimorados. O ReFS é um sistema de arquivos no Windows Server 2012 e posterior que foi projetado para ser mais resiliente contra corrupção de dados, maximizando a disponibilidade e a integridade dos dados. Especificamente, o ReFS traz melhorias na maneira como os metadados são atualizados, o que oferece melhor proteção para dados e reduz os casos de corrupção de dados. Ele também usa as verificações para verificar a integridade dos dados e metadados do arquivo, garantindo que os dados corrupções são facilmente encontrados e reparados. 

O Exchange Online aproveita vários benefícios do ReFS: 
- Mais resiliência na integridade de dados significa menos incidentes de corrupção de dados. Reduzir o número de incidentes de corrupção significa menos reações desnecessárias do banco de dados. 
- A verificação em execução em metadados permitindo detecções de casos de corrupção mais cedo e mais deterministicamente, permitindo corrigir a corrupção de dados do cliente antes que ocorram falhas cinza nos volumes de dados.
- Projetado para funcionar bem com grandes conjuntos de dados — petabytes e maiores — sem impacto no desempenho
- Suporte para outros recursos usados pelo Exchange Online, como criptografia BitLocker. 

O Exchange Online também se beneficia de outros recursos do ReFS: 
- **Integridade (Fluxos de Integridade)** – o ReFS armazena dados de maneira a protegê-los contra muitos dos erros comuns que normalmente podem causar perda de dados. A Pesquisa do Microsoft 365 usa Fluxos de Integridade para ajudar com a detecção de corrupção de disco antecipada e as verificações de conteúdo do arquivo. O recurso também reduz os incidentes de corrupção causados por "Gravações de Filme" (quando uma operação de gravação não é concluída devido a falta de energia etc.). 
- **Disponibilidade (recuperação)** - o ReFS prioriza a disponibilidade de dados. Historicamente, os sistemas de arquivos eram frequentemente suscetíveis à corrupção de dados que exigia que o sistema fosse offline para reparo. Embora raro, se ocorrer corrupção, o ReFS implementa recuperação, um recurso que remove os dados corrompidos do namespace em um volume ao vivo e garante que os dados bons não sejam afetados negativamente por dados corrompidos não reparáveis. Aplicar o recurso Recuperação e isolar dados corrompidos nos volumes de banco de dados do Exchange Online significa que podemos manter íntepar bancos de dados não afetados em um volume corrompido entre o tempo de corrupção e ação de reparo. Essa estrutura aumenta a disponibilidade de bancos de dados que normalmente seriam afetados por esses problemas de corrupção de disco. 
