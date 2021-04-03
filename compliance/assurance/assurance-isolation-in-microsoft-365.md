---
title: Isolamento e controle de acesso no Microsoft 365
description: 'Resumo: uma explicação do isolamento e do controle de acesso dentro dos vários aplicativos do Microsoft 365.'
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
- SPO_Content
- MS-Compliance
f1.keywords:
- NOCSH
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: f1166ce766c2b1158d50242b9411f051992bf121
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497048"
---
# <a name="isolation-and-access-control-in-microsoft-365"></a>Isolamento e controle de acesso no Microsoft 365

O Azure Active Directory (Azure AD) e o Microsoft 365 usam um modelo de dados altamente complexo que inclui dezenas de serviços, centenas de entidades, milhares de relações e dezenas de milhares de atributos. Em alto nível, o Azure AD e os diretórios de serviço são os contêineres de locatários e destinatários mantidos em sincronia usando protocolos de replicação baseados em estado. Além das informações de diretório mantidas no Azure AD, cada uma das cargas de trabalho de serviço têm sua própria infraestrutura de serviços de diretório.
 
![Sincronização de dados de locatários do Microsoft 365](../media/office-365-isolation-tenant-data-sync.png)

Nesse modelo, não há uma única fonte de dados de diretório. Sistemas específicos têm partes individuais de dados, mas nenhum único sistema contém todos os dados. Os serviços do Microsoft 365 cooperam com o Azure AD neste modelo de dados. O Azure AD é o "sistema de verdade" para dados compartilhados, que normalmente são dados pequenos e estáticos usados por cada serviço. O modelo federado usado no Microsoft 365 e no Azure AD fornece a exibição compartilhada dos dados.

O Microsoft 365 usa armazenamento físico e armazenamento em nuvem do Azure. O Exchange Online (incluindo a Proteção do Exchange Online) e o Skype for Business usam seu próprio armazenamento para dados do cliente. O SharePoint Online usa armazenamento SQL Server armazenamento do Azure e, portanto, a necessidade de isolamento adicional dos dados do cliente no nível de armazenamento.

## <a name="exchange-online"></a>Exchange Online

O Exchange Online armazena dados do cliente em caixas de correio. As caixas de correio são hospedadas em bancos de dados do Mecanismo de Armazenamento Extensível (ESE) chamados bancos de dados de caixa de correio. Isso inclui caixas de correio de usuário, caixas de correio vinculadas, caixas de correio compartilhadas e caixas de correio de pasta pública. As caixas de correio de usuário incluem conteúdo salvo do Skype for Business, como histórias de conversas.

O conteúdo da caixa de correio do usuário inclui:

- Emails e anexos de email
- Informações de calendário e de ocupado/agendamento
- Contatos
- Tarefas
- Observações
- Grupos
- Dados de inferência

Cada banco de dados de caixa de correio no Exchange Online contém caixas de correio de vários locatários. Um código de autorização assegura cada caixa de correio, incluindo em um local de trabalho. Por padrão, somente o usuário atribuído tem acesso a uma caixa de correio. A lista de controles de acesso (ACL) que garante uma caixa de correio contém uma identidade autenticada pelo Azure AD no nível do locatário. As caixas de correio para cada locatário são limitadas a identidades autenticadas no provedor de autenticação do locatário, que inclui apenas usuários desse locatário. O conteúdo no locatário A não pode ser obtido de forma alguma pelos usuários no locatário B, a menos que seja explicitamente aprovado pelo locatário A.

## <a name="skype-for-business"></a>Skype for Business

O Skype for Business armazena dados em vários lugares:

- As informações de usuário e conta, que incluem pontos de extremidade de conexão, IDs de locatário, planos de discagem, configurações de roaming, estado de presença, listas de contatos, etc., são armazenadas nos servidores do Skype for Business Active Directory e em vários servidores de banco de dados do Skype for Business. As listas de contatos são armazenadas na caixa de correio do Exchange Online do usuário se o usuário estiver habilitado para ambos os produtos ou em servidores skype for Business, se o usuário não estiver. Os servidores de banco de dados do Skype for Business não são particionados por locatário, mas o isolamento de vários locatários de dados é imposto por meio do controle de acesso baseado em função (RBAC).
- O conteúdo da reunião e os dados carregados são armazenados em compartilhamentos dfs (sistema de arquivos distribuídos). Esse conteúdo também pode ser arquivado no Exchange Online, se habilitado. As compartilhamentos DFS não são particionadas por locatário. o conteúdo é protegido com ACLs e a multi-enancy é imposta por meio do RBAC.
- Registros de detalhes de chamada, que são o histórico de atividades, como histórico de chamada, sessões de mensagens IM, compartilhamento de aplicativos, histórico de mensagens, etc., também podem ser armazenados no Exchange Online, mas a maioria dos registros de detalhes de chamada são temporariamente armazenados em servidores cdr (registro de detalhes de chamada). O conteúdo não é particionado por locatário, mas a multi locação é imposta por meio do RBAC.

## <a name="sharepoint-online"></a>SharePoint Online

O SharePoint Online tem vários mecanismos independentes que fornecem isolamento de dados. Armazena objetos como código abstraído em bancos de dados de aplicativos. Por exemplo, quando um usuário carrega um arquivo no SharePoint Online, o arquivo é desmontado, convertido em código de aplicativo e armazenado em várias tabelas em vários bancos de dados.

Se um usuário puder obter acesso direto ao armazenamento que contém os dados, o conteúdo não poderá ser interpretado para um humano ou qualquer outro sistema que não seja o SharePoint Online. Esses mecanismos incluem o controle de acesso à segurança e propriedades. Todos os recursos do SharePoint Online são protegidos pelo código de autorização e pela política do RBAC, incluindo dentro de uma área de trabalho. A lista de controles de acesso (ACL) que garante um recurso contém uma identidade autenticada no nível do locatário. Os dados do SharePoint Online para um locatário estão limitados às identidades autenticadas pelo provedor de autenticação do locatário.

Além das ACLs, uma propriedade de nível de locatário que especifica o provedor de autenticação (que é o Azure AD específico do locatário), é escrita uma vez e não pode ser alterada depois de definida. Depois que a propriedade de locatário do provedor de autenticação tiver sido definida para um locatário, ela não poderá ser alterada usando as APIs expostas a um locatário.

Um *SubscriptionId exclusivo* é usado para cada locatário. Todos os sites de clientes são de propriedade de um locatário e atribuídos a *SubscriptionId* exclusivo para o locatário. A *propriedade SubscriptionId* em um site é escrita uma vez e é permanente. Depois de atribuído a um locatário, um site não pode ser movido para um locatário diferente. *SubscriptionId* é a chave usada para criar o escopo de segurança do provedor de autenticação e está vinculada ao locatário.

O SharePoint Online usa SQL Server e armazenamento do Azure para armazenamento de metadados de conteúdo. A chave de partição do armazenamento de conteúdo *é SiteId* no SQL. Ao executar uma SQL, o SharePoint Online usa um *SiteId* verificado como parte de uma verificação *SubscriptionId* no nível de locatário.

O SharePoint Online armazena conteúdo de arquivo criptografado em blobs do Microsoft Azure. Cada farm do SharePoint Online tem sua própria conta do Microsoft Azure e todos os blobs salvos no Azure são criptografados individualmente com uma chave armazenada no SQL de conteúdo. A chave de criptografia protegida em código pela camada de autorização e não exposta diretamente ao usuário final. O SharePoint Online tem monitoramento em tempo real para detectar quando uma solicitação HTTP lê ou grava dados para mais de um locatário. A identidade de *solicitação SubscriptionId* é rastreada em *SubscriptionId* do recurso acessado. As solicitações para acessar recursos de mais de um locatário nunca devem acontecer por usuários finais. As solicitações de serviço em um ambiente de vários locatários são a única exceção. Por exemplo, o rastreador de pesquisa puxa alterações de conteúdo para um banco de dados inteiro de uma só vez. Isso geralmente envolve consultar sites de mais de um locatário em uma única solicitação de serviço, o que é feito por motivos de eficiência.

## <a name="teams"></a>Teams

Seus dados do Teams são armazenados de forma diferente, dependendo do tipo de conteúdo. 

Confira a sessão de [saída do Ignite na arquitetura do Microsoft Teams](https://channel9.msdn.com/Events/Ignite/Microsoft-Ignite-Orlando-2017/BRK3071) para uma discussão detalhada.

### <a name="core-teams-customer-data"></a>Principais dados do cliente do Teams

Se seu locatário for provisionado na Austrália, Canadá, União Europeia, França, Alemanha, Índia, Japão, África do Sul, Coreia do Sul, Suíça (que inclui Liechtenstein), Emirados Árabes Unidos, Reino Unido ou Estados Unidos, a Microsoft armazenará os seguintes dados do cliente em repouso somente nesse local:

- Chats do Teams, conversas de equipe e canal, imagens, mensagens de caixa postal e contatos.
- O conteúdo do site do SharePoint Online e os arquivos armazenados neste site.
- Arquivos carregados no OneDrive para trabalho ou escola.

#### <a name="chat-channel-messages-team-structure"></a>Chat, mensagens de canal, estrutura de equipe

Todas as equipes no Teams têm o suporte de um Grupo do Microsoft 365 e seu site do SharePoint e caixa de correio do Exchange. Chats privados (incluindo chats de grupo), mensagens enviadas como parte de uma conversa em um canal e a estrutura de equipes e canais são armazenadas em um serviço de chat em execução no Azure. Os dados também são armazenados em uma pasta oculta nas caixas de correio de usuário e grupo para habilitar recursos de Proteção de Informações.

#### <a name="voicemail-and-contacts"></a>Caixa postal e contatos

As caixas postal são armazenadas no Exchange. Os contatos são armazenados no armazenamento de dados em nuvem baseado no Exchange. O Exchange e o armazenamento de nuvem baseado no Exchange já fornecem residência de dados em cada um dos geos do datacenter mundial. Para todas as equipes, a caixa postal e os contatos são armazenados no país para Austrália, Canadá, França, Alemanha, Índia, Japão, Emirados Árabes Unidos, Reino Unido, África do Sul, Coreia do Sul, Suíça (que inclui Liechtenstein) e Estados Unidos. Para todos os outros países, os arquivos são armazenados nos EUA, na Europa ou Asia-Pacific local com base na afinidade de locatários.

#### <a name="images-and-media"></a>Imagens e mídia

A mídia usada em chats (exceto giphy GIFs que não são armazenados, mas são um link de referência para a URL de serviço Giphy original, Giphy é um serviço que não é da Microsoft) é armazenada em um serviço de mídia baseado no Azure que é implantado nos mesmos locais que o serviço de chat.

#### <a name="files"></a>Arquivos

Os arquivos (incluindo o OneNote e o Wiki) que alguém compartilha em um canal são armazenados no site do SharePoint da equipe. Os arquivos compartilhados em um chat privado ou em um chat durante uma reunião ou chamada são carregados e armazenados na conta do OneDrive para trabalho ou estudante do usuário que compartilha o arquivo. Exchange, SharePoint e OneDrive já fornecem residência de dados em cada um dos geos do datacenter mundial. Portanto, para clientes existentes, todos os arquivos, blocos de anotações do OneNote, conteúdo wiki do Teams e caixas de correio que fazem parte da experiência do Teams já estão armazenadas no local com base na afinidade do locatário. Os arquivos são armazenados no país para Austrália, Canadá, França, Alemanha, Índia, Japão, Emirados Árabes Unidos, Reino Unido, África do Sul, Coreia do Sul e Suíça (que inclui Liechtenstein). Para todos os outros países, os arquivos são armazenados no local dos EUA, Europa ou Ásia-Pacífico com base na afinidade de locatários.
