---
title: Exchange Online Resiliência de dados no Microsoft 365
description: Neste artigo, encontre uma explicação dos vários aspectos da resiliência de dados no Exchange Online e Microsoft 365.
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
hideEdit: true
ms.openlocfilehash: 8952d492c4427d5f4af64a853adaaf15303e8caf
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/23/2021
ms.locfileid: "53088630"
---
# <a name="exchange-online-data-resiliency-in-microsoft-365"></a>Exchange Online resiliência de dados no Microsoft 365

>[!IMPORTANT]
>À medida que continuamos a investir em diferentes maneiras de preservar o conteúdo da caixa de correio, anunciamos In-Place ressarção do In-Place No Centro de administração do Exchange (EAC) no Exchange Online. A partir de 1º de julho de 2020, você não poderá criar novos In-Place Holds. Mas você ainda poderá gerenciar os In-Place no EAC ou usando o cmdlet **Set-MailboxSearch** no Exchange Online PowerShell. No entanto, a partir de 1º de outubro de 2020, você não poderá gerenciar In-Place Holds. Você só poderá removê-los no EAC ou usando o cmdlet **Remove-MailboxSearch.** O In-Place de Exchange Server e Exchange implantações híbridas ainda serão suportadas. Para obter mais informações sobre a In-Place de Exchange Online, consulte [Retirement of legacy eDiscovery tools](/microsoft-365/compliance/legacy-ediscovery-retirement).

Uma In-Place Deter preserva todo o conteúdo da caixa de correio, incluindo itens excluídos e versões originais de itens modificados. Todos os itens da caixa de correio são retornados em uma pesquisa de [Descoberta eletrônica In-loco](/exchange/security-and-compliance/in-place-ediscovery/in-place-ediscovery). Quando você coloca um In-Place na caixa de correio de um usuário, o conteúdo na caixa de correio de arquivo morto correspondente (se estiver habilitada) também é colocado em espera e retornado em uma pesquisa de Descoberta Eletrônico.

Há dois tipos de corrupção que podem afetar um banco de dados Exchange: corrupção física, que normalmente é causada por problemas de hardware (em particular, hardware de armazenamento) e corrupção lógica, que ocorre devido a outros fatores. Geralmente, há dois tipos de corrupção lógica que podem ocorrer em um banco de dados Exchange:

- **Corrupção lógica do banco** de dados - A página de banco de dados verifica se corresponde, mas os dados na página estão errados logicamente. Isso pode ocorrer quando o mecanismo de banco de dados (o Mecanismo extensível Armazenamento (ESE)) tenta gravar uma página de banco de dados e, mesmo que o sistema operacional retorne uma mensagem de sucesso, os dados nunca serão gravados no disco ou gravados no lugar errado. Isso é conhecido como *liberação perdida*. O ESE inclui vários recursos e proteções projetados para evitar a corrupção física de um banco de dados e outros cenários de perda de dados. Para evitar que as liberações perdidas percam dados, o ESE inclui um mecanismo de detecção de liberação perdida no banco de dados juntamente com um recurso (restauração de página única) para corrigi-lo.
- **Armazenar corrupção lógica** - Os dados são adicionados, excluídos ou manipulados de uma maneira que o usuário não espera. Esses casos são causados por aplicativos de terceiros. Normalmente, é corrupção no sentido de que o usuário a vê como corrupção. O repositório do Exchange considera a transação que produziu o dano lógico uma série de operações MAPI válidas. Os recursos de espera [in-locar](/exchange/security-and-compliance/create-or-remove-in-place-holds) no Exchange Online fornece proteção contra corrupção lógica do armazenamento (porque impede que o conteúdo seja excluído permanentemente por um usuário ou um aplicativo). 

Exchange Online realiza várias verificações de consistência em arquivos de log replicados durante a inspeção de log e a repetição de log. Essas verificações de consistência impedem que a corrupção física seja replicada pelo sistema. Por exemplo, durante a inspeção de log, há uma verificação de integridade física que verifica o arquivo de log e valida se o checkum gravado no arquivo de log corresponde ao checksum gerado na memória. Além disso, o header do arquivo de log é examinado para garantir que a assinatura de arquivo de log registrada no header de log corresponde à do arquivo de log. Durante a repetição de log, o arquivo de log passa por um exame mais minuário. Por exemplo, o header do banco de dados também contém a assinatura de log que é comparada com a assinatura do arquivo de log para garantir que eles corresponderem. 

A proteção contra corrupção de dados de caixa de correio no Exchange Online é alcançada usando o Exchange Native Data Protection, uma estratégia de resiliência que aproveita a replicação no nível do aplicativo em vários servidores e vários datacenters, juntamente com outros recursos que ajudam a proteger os dados contra perda devido a corrupção ou outros motivos. Esses recursos incluem recursos nativos gerenciados pela Microsoft ou pelo aplicativo Exchange Online em si, como:

- [Grupos de Disponibilidade de Dados](/exchange/back-up-email)
- Correção de bit único 
- Verificação de banco de dados online 
- Detecção de Flush Perdido 
- Restauração de página única 
- Serviço de Replicação de Caixa de Correio 
- Verificações de arquivo de log 
- Implantação no Sistema de Arquivos Resilientes 

Para obter mais informações sobre os recursos nativos listados anteriormente, selecione os hiperlinks e consulte o seguinte para obter informações adicionais e para obter detalhes sobre itens sem hiperlinks. Além desses recursos nativos, Exchange Online também inclui recursos de resiliência de dados que os clientes podem gerenciar, como: 
- [Recuperação de Item Único (habilitada por padrão)](/exchange/recipients-in-exchange-online/manage-user-mailboxes/recover-deleted-messages) 
- [Bloqueio In-loco e Retenção de Litígio](/exchange/security-and-compliance/in-place-and-litigation-holds) 
- [Retenção de itens excluídos e Soft-Deleted caixas de correio (ambas habilitadas por padrão)](/exchange/recipients-in-exchange-online/delete-or-restore-mailboxes) 

## <a name="database-availability-groups"></a>Grupos de disponibilidade de banco de dados 
Cada banco de dados de caixa de correio no Microsoft 365 é hospedado em um grupo de disponibilidade de banco de dados [(DAG)](/exchange/back-up-email) e replicado para datacenters geograficamente separados na mesma região. A configuração mais comum é quatro cópias de banco de dados em quatro datacenters; no entanto, algumas regiões têm menos datacenters (bancos de dados são replicados para três datacenters na Índia e dois datacenters na Austrália e no Japão). Mas, em todos os casos, cada banco de dados de caixa de correio tem quatro cópias distribuídas em vários datacenters, garantindo assim que os dados da caixa de correio sejam protegidos contra falhas de software, hardware e até datacenter. 

Dessas quatro cópias, três delas estão configuradas como altamente disponíveis. A quarta cópia é configurada como uma cópia de banco [de dados com um tempo defasado.](/Exchange/high-availability/manage-ha/activate-lagged-db-copies) A cópia de banco de dados comfasado não se destina à recuperação individual de caixa de correio ou à recuperação de item de caixa de correio. Seu objetivo é fornecer um mecanismo de recuperação para o evento raro de corrupção lógica catastrófica em todo o sistema. 

Cópias de banco de dados com atraso Exchange Online são configuradas com um tempo de retardo de repetição de arquivo de log de sete dias. Além disso, o Exchange Gerenciador de Retardo de Repetição está habilitado para fornecer um arquivo de log dinâmico para baixo para cópias com atraso para permitir que cópias de banco de dados com retardo se reparem e gerenciem o crescimento do arquivo de log. Embora as cópias de banco de dados com Exchange Online sejam usadas no Exchange Online, é importante entender que elas não são um backup de ponto-a-hora garantido. Cópias de banco de dados com espera no Exchange Online têm um limite de disponibilidade, normalmente em torno de 90%, devido aos períodos em que o disco que contém uma cópia com espera é perdido devido a uma falha de disco, a cópia com espera se tornando uma cópia altamente disponível (devido à reprodução automática), bem como os períodos em que a cópia de banco de dados com espera está recriando a fila de repetição de log. 

## <a name="transport-resilience"></a>Resiliência de Transporte 
Exchange Online inclui dois recursos principais de resiliência de transporte: Redundância de Sombra e Rede de Segurança. A Redundância de Sombra mantém uma cópia redundante de uma mensagem enquanto está em trânsito. A Rede de Segurança mantém uma cópia redundante de uma mensagem depois que a mensagem é entregue com êxito. 

Com a Redundância de Sombra, cada Exchange Online de transporte faz uma cópia de cada mensagem que recebe antes de confirmar o recebimento com êxito da mensagem para o servidor de envio. Isso torna todas as mensagens no pipeline de transporte redundantes enquanto estão em trânsito. Se Exchange Online determinar que a mensagem original foi perdida em trânsito, uma cópia redundante da mensagem será reprojetada. 

A Rede de Segurança é uma fila de transporte associada ao serviço de Transporte em um servidor de Caixa de Correio. Essa fila armazena cópias de mensagens que foram processadas com êxito pelo servidor. Quando um banco de dados de caixa de correio ou uma falha de servidor exige a ativação de uma cópia desajustada do banco de dados de caixa de correio, as mensagens na fila rede de segurança são automaticamente retransmitidas para a nova cópia ativa do banco de dados de caixa de correio. A Rede de Segurança também é redundante, eliminando o transporte como um único ponto de falha. Ele usa o conceito de uma Rede de Segurança Primária e uma Rede de Segurança de Sombra em que, se a Rede de Segurança Primária estiver indisponível por mais de 12 horas, as solicitações de reenviação se tornarão solicitações de reenviação de sombra e as mensagens serão reprojetadas da Rede de Segurança de Sombra.

As reenviações de mensagens da Rede de Segurança são iniciadas automaticamente pelo componente do Active Manager do serviço de replicação do Microsoft Exchange que gerencia DAGs e cópias de banco de dados de caixa de correio. Nenhuma ação manual é necessária para reemubmitir mensagens da Rede de Segurança. 

## <a name="single-bit-correction"></a>Correção de bit único 
O ESE inclui um mecanismo para detectar e resolver erros de CRC de bit único (também conhecidos como flips de bit único) que são o resultado de erros de hardware (e, como tal, eles representam corrupção física). Quando esses erros ocorrem, o ESE corrige-os automaticamente e registra um evento no log de eventos. 

## <a name="online-database-scanning"></a>Verificação de banco de dados online 
A verificação de banco de dados online (também conhecida como soma de verificação de banco de dados *)* é o processo em que um ESE usa um verificador de consistência de banco de dados para ler cada página e verificar se há corrupção de página. O objetivo principal é detectar a corrupção física e as liberações perdidas que podem não ser detectadas por operações transacionais. A verificação de banco de dados também executa operações de falha pós-armazenamento. O espaço pode ser vazado devido a falhas e a verificação de banco de dados online localiza e recupera espaço perdido. O sistema foi projetado com a expectativa de que cada banco de dados seja totalmente verificado uma vez a cada sete dias. 

## <a name="lost-flush-detection"></a>Detecção de Flush Perdido 
Ocorre uma liberação perdida quando uma operação de gravação de banco de dados que o subsistema de disco/sistema operacional retornado como concluído não foi realmente gravado em disco ou foi gravado no local errado. Incidentes de flush perdidos podem resultar em corrupção lógica do banco de dados, portanto, para evitar que as liberações perdidas resultem em dados perdidos, o ESE inclui um mecanismo de detecção de liberação perdida. À medida que as páginas do banco de dados são escritas em cópias passivas, uma verificação é realizada para liberações perdidas na cópia ativa. Se uma liberação perdida for detectada, o ESE poderá reparar o processo usando um processo de correção de página. 

## <a name="single-page-restore"></a>Restauração de página única 
A restauração de página única, também conhecida como *patch de* página, é um processo automático em que páginas de banco de dados corrompidas são substituídas por cópias saudáveis de uma réplica saudável. O processo de reparo de uma página corrompida depende se a cópia do banco de dados está ativa ou passiva. Quando uma cópia de banco de dados ativa encontra uma página corrompida, ela pode copiar uma página de uma de suas réplicas, desde que a página copiada seja atualizada. Esse processo é realizado colocando uma solicitação para a página no fluxo de log, que é a base da replicação do banco de dados de caixa de correio. Assim que uma réplica encontra a solicitação de página, ela responde enviando uma cópia da página para a cópia do banco de dados solicitando. A restauração de página única também fornece um mecanismo de comunicação assíncrono para o ativo solicitar uma página de réplicas, mesmo se as réplicas estão offline no momento. 

Em caso de corrupção em uma cópia passiva do banco de dados, incluindo uma cópia de banco de dados com atraso, pois essas cópias estão sempre atrás de sua cópia ativa, é sempre seguro copiar qualquer página da cópia ativa para uma cópia passiva. Uma cópia passiva do banco de dados está por natureza altamente disponível, portanto, durante o processo de correção de página, a reprodução de log é suspensa, mas a cópia de log continua. A cópia passiva do banco de dados recupera uma cópia da página corrompida da cópia ativa, aguarda até que o arquivo de log que atenda ao requisito máximo de geração de log necessário seja copiado e inspecionado e, em seguida, remenda a página corrompida. Depois que a página for corrigida, o log será reiniciado. O processo é o mesmo para a cópia de banco de dados com um tempo defasado, exceto que o banco de dados com o tempo defasado primeiro reproduz todos os arquivos de log necessários para atingir um estado corretável. 

## <a name="mailbox-replication-service"></a>Serviço de Replicação de Caixa de Correio 
Mover caixas de correio é uma parte fundamental do gerenciamento de um serviço de email em grande escala. Há sempre tecnologias atualizadas e atualizações de hardware e versão para lidar, portanto, ter um sistema robusto e com aceleração que permite que nossos engenheiros realizem esse trabalho enquanto mantém as movimentações de caixa de correio transparentes para os usuários (ao garantir que eles permaneçam online durante todo o processo) é fundamental e garantir que o processo seja dimensionado normalmente à medida que as caixas de correio ficam maiores e maiores. 

O Exchange Mrs (Serviço de Replicação de Caixa de Correio) é responsável pela movimentação de caixas de correio entre bancos de dados. Durante a movimentação, o MRS executa uma verificação de consistência em todos os itens dentro da caixa de correio. Se um problema de consistência for encontrado, o MRS corrigirá o problema ou ignorará os itens corrompidos, removendo assim a corrupção da caixa de correio. 

Como o MRS é um componente Exchange Online, podemos fazer alterações em seu código para resolver novas formas de corrupção detectadas no futuro. Por exemplo, se detectarmos um problema de consistência que o MRS não é capaz de corrigir, podemos analisar a corrupção, alterar o código MRS e corrigir a inconsistência (se entendermos como corrigir). 

## <a name="log-file-checks"></a>Verificações de arquivo de log 
Todos os arquivos de log de transações gerados por um banco de dados Exchange passam por várias formas de verificações de consistência. Quando um arquivo de log é criado, a primeira coisa feita é um padrão de bits é gravado e, em seguida, uma série de gravações de log é executada. Essa estrutura permite Exchange Online executar uma série de verificações (liberação perdida, CRC e outras verificações) para validar cada arquivo de log conforme ele é gravado e novamente conforme é replicado. 

## <a name="deployment-on-resilient-file-system"></a>Implantação no Sistema de Arquivos Resilientes 
Para ajudar a evitar a ocorrência de corrupção no nível do sistema de arquivos, Exchange Online está sendo implantado em partições do Sistema de Arquivos Resilientes (ReFS) para fornecer recursos de recuperação aprimorados. O ReFS é um sistema de arquivos no Windows Server 2012 e posterior que foi projetado para ser mais resiliente contra a corrupção de dados, maximizando a disponibilidade e a integridade dos dados. Especificamente, o ReFS traz melhorias na maneira como os metadados são atualizados, o que oferece melhor proteção para dados e reduz os casos de corrupção de dados. Ele também usa verificações para verificar a integridade de dados de arquivo e metadados garantindo que a corrupção de dados seja facilmente encontrada e reparada. 

Exchange Online aproveita vários benefícios reFS: 
- Mais resiliência na integridade de dados significa menos incidentes de corrupção de dados. Reduzir o número de incidentes de corrupção significa menos reseações desnecessárias de banco de dados. 
- Verificações em execução em metadados que permitem detecções de casos de corrupção mais cedo e mais deterministicamente, permitindo corrigir a corrupção de dados do cliente antes que ocorram falhas cinzas em volumes de dados.
- Projetado para funcionar bem com conjuntos de dados grandes, petabytes e maiores, sem impacto no desempenho
- Suporte para outros recursos usados pelo Exchange Online, como a criptografia BitLocker. 

Exchange Online também se beneficia de outros recursos ReFS: 
- **Integridade (integridade Fluxos)** - O ReFS armazena dados de uma maneira que os protege contra muitos dos erros comuns que normalmente podem causar perda de dados. Microsoft 365 A pesquisa usa Fluxos integridade para ajudar na detecção inicial de corrupção de disco e verificações de conteúdo de arquivo. O recurso também reduz os incidentes de corrupção causados por "Gravações Cortadas" (quando uma operação de gravação não é concluída devido a falta de energia, etc.). 
- **Disponibilidade (Salvamento)** - O ReFS prioriza a disponibilidade de dados. Historicamente, os sistemas de arquivos eram frequentemente suscetíveis a corrupção de dados que exigiriam que o sistema fosse offline para reparo. Embora raro, se a corrupção ocorrer, o ReFS implementará o salvamento, um recurso que remove os dados corrompidos do namespace em um volume ao vivo e garante que os bons dados não sejam afetados adversamente por dados corrompidos não recuperáveis. Aplicar o recurso Salvamento e isolar a corrupção de dados Exchange Online volumes de banco de dados significa que podemos manter os bancos de dados não afetados em um volume corrompido íntegre entre o momento da corrupção e a ação de reparo. Essa estrutura aumenta a disponibilidade de bancos de dados que normalmente seriam afetados por esses problemas de corrupção de disco. 
