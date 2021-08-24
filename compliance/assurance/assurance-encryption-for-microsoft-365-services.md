---
title: Criptografia para Skype, OneDrive, SharePoint e Exchange
description: 'Resumo: uma descrição da criptografia para Skype, OneDrive, SharePoint, Microsoft Teams e Exchange Online.'
ms.author: krowley
author: kccross
manager: laurawi
ms.reviewer: sosstah
f1.keywords:
- NOCSH
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: medium
search.appverid:
- MET150
ms.collection:
- Strat_O365_Enterprise
- M365-security-compliance
- Strat_O365_Enterprise
- SPO_Content
- MS-Compliance
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 480e7e03564075707c90e25ad5777631c1e68ed8
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2021
ms.locfileid: "58482023"
---
# <a name="encryption-for-skype-for-business-onedrive-for-business-sharepoint-online-microsoft-teams-and-exchange-online"></a>Criptografia para Skype for Business, OneDrive for Business, SharePoint Online, Microsoft Teams e Exchange Online

Microsoft 365 é um ambiente altamente seguro que oferece proteção extensiva em várias camadas: segurança física do data center, segurança de rede, segurança de acesso, segurança de aplicativos e segurança de dados.

## <a name="skype-for-business"></a>Skype for Business

Skype for Business dados do cliente podem ser armazenados em repouso na forma de arquivos ou apresentações carregados pelos participantes da reunião. O servidor de WebConferência criptografa dados do cliente usando o AES com uma chave de 256 bits. Os dados do cliente criptografados são armazenados em um compartilhamento de arquivos. Cada parte dos dados do cliente é criptografada usando uma chave de 256 bits gerada aleatoriamente. Quando um dado do cliente é compartilhado em uma conferência, o servidor de WebConferência instrui os clientes de conferência a baixar os dados do cliente criptografados por meio de HTTPS. Ele envia a chave correspondente aos clientes para que os dados do cliente possam ser descriptografados. O servidor de WebConferência também autentica clientes de conferência antes de permitir que os clientes acessem dados do cliente de conferência. Ao ingressar em uma conferência da Web, cada cliente de conferência estabelece uma caixa de diálogo SIP com o componente de foco de conferência em execução no servidor front-end por TLS primeiro. O foco de conferência passa para o cliente de conferência um cookie de autenticação gerado pelo servidor de WebConferência. Em seguida, o cliente de conferência se conecta ao servidor de WebConferência que apresenta o cookie de autenticação a ser autenticado pelo servidor.

## <a name="sharepoint-online-and-onedrive-for-business"></a>SharePoint Online e OneDrive for Business

Todos os arquivos do cliente SharePoint Online são protegidos por chaves exclusivas por arquivo que são sempre exclusivas de um único locatário. As chaves são criadas e gerenciadas pelo serviço SharePoint Online ou quando a Chave do Cliente é usada, criada e gerenciada pelos clientes. Quando um arquivo é carregado, a criptografia é executada pelo SharePoint Online no contexto da solicitação de carregamento, antes de ser enviada para o armazenamento do Azure. Quando um arquivo é baixado, o SharePoint Online recupera os dados do cliente criptografados do armazenamento do Azure com base no identificador de documento exclusivo e descriptografa os dados do cliente antes de enviá-los ao usuário. O armazenamento do Azure não tem capacidade de descriptografar, nem mesmo identificar ou entender os dados do cliente. Toda a criptografia e a descriptografia ocorrem nos mesmos sistemas que impõem o isolamento de locatários, que são Azure Active Directory e SharePoint Online.

Várias cargas de trabalho no Microsoft 365 armazenam dados no SharePoint Online, incluindo o Microsoft Teams, que armazena todos os arquivos no SharePoint Online e no OneDrive for Business, que usa o SharePoint Online para seu armazenamento. Todos os dados do cliente armazenados no SharePoint Online são criptografados (com uma ou mais chaves de 256 bits do AES) e distribuídos no datacenter da seguinte forma. (Cada etapa desse processo de criptografia é FIPS 140-2 Nível 2 validada. Para obter informações adicionais sobre a conformidade com o FIPS 140-2, consulte [FIPS 140-2 Compliance](/previous-versions/sql/sql-server-2008-r2/bb326611(v=sql.105)).)

- Cada arquivo é dividido em uma ou mais partes, dependendo do tamanho do arquivo. Cada parte é criptografada usando sua própria chave exclusiva do AES de 256 bits.
- Quando um arquivo é atualizado, a atualização é manipulada da mesma maneira: a alteração é dividida em uma ou mais partes e cada parte é criptografada com uma chave exclusiva separada.
- Essas partes – arquivos, arquivos e deltas de atualização – são armazenadas como blobs no armazenamento do Azure que são distribuídos aleatoriamente em várias contas de armazenamento do Azure.
- O conjunto de chaves de criptografia para essas partes de dados do cliente é criptografado.

    - As chaves usadas para criptografar os blobs são armazenadas no banco de dados de conteúdo SharePoint Online.
    - O Banco de Dados de Conteúdo é protegido por controles de acesso ao banco de dados e criptografia em repouso. A criptografia é executada [usando Transparent Data Encryption](/sql/relational-databases/security/encryption/transparent-data-encryption-tde) (TDE) [em Banco de Dados SQL do Azure](/azure/sql-database/sql-database-technical-overview). (Banco de Dados SQL do Azure é um serviço de banco de dados relacional de finalidade geral no Microsoft Azure que oferece suporte a estruturas como dados relacionais, JSON, espacial e XML.) Esses segredos estão no nível de serviço para SharePoint Online, não no nível do locatário. Esses segredos (às vezes chamados de chaves mestras) são armazenados em um repositório seguro separado chamado Repositório de Chaves. O TDE fornece segurança em repouso para o banco de dados ativo e os backups de banco de dados e logs de transação.
    - Quando os clientes fornecem a chave opcional, a chave do cliente é armazenada no Azure Key Vault e o serviço usa a chave para criptografar uma chave de locatário, que é usada para criptografar uma chave de site, que é usada para criptografar as chaves de nível de arquivo. Essencialmente, uma nova hierarquia de chaves é introduzida quando o cliente fornece uma chave.
- O mapa usado para montar o arquivo é armazenado no Banco de Dados de Conteúdo juntamente com as chaves criptografadas, separadamente da chave mestra necessária para descriptografá-las.
- Cada conta de armazenamento do Azure tem suas próprias credenciais exclusivas por tipo de acesso (leitura, gravação, enumeração e exclusão). Cada conjunto de credenciais é mantido no Repositório de Chaves seguro e atualizado regularmente. Conforme descrito acima, há três tipos diferentes de armazenamentos, cada um com uma função distinta:
    - Os dados do cliente são armazenados como blobs criptografados no armazenamento do Azure. A chave para cada parte dos dados do cliente é criptografada e armazenada separadamente no Banco de Dados de Conteúdo. Os dados do cliente em si não têm nenhuma pista sobre como eles podem ser descriptografados.
    - O banco de dados de conteúdo é um banco de dados do SQL Server. Ele mantém o mapa necessário para localizar e remontar os blobs de dados do cliente mantidos no armazenamento do Azure, bem como as chaves necessárias para criptografar esses blobs. No entanto, o conjunto de chaves é criptografado (conforme explicado acima) e mantido em um Key Store separado.
    - O Key Store é fisicamente separado do banco de dados de conteúdo e do armazenamento do Azure. Ele contém as credenciais para cada contêiner de armazenamento do Azure e a chave mestra para o conjunto de chaves criptografadas mantidas no Banco de Dados de Conteúdo.

Cada um desses três componentes de armazenamento – o armazenamento de blob do Azure, o Banco de Dados de Conteúdo e o Armazenamento de Chaves – está fisicamente separado. As informações contidas nesses componentes por si só não são utilizáveis. Sem acesso a todos os três, é impossível recuperar as chaves das partes, descriptografar as chaves para torná-las usáveis, associar as chaves às partes correspondentes, descriptografar cada parte ou reconstruir um documento de suas partes constituintes.

Os certificados BitLocker, que protegem os volumes de disco físico em máquinas no datacenter, são armazenados em um repositório seguro (o repositório secreto do SharePoint Online) que é protegido pela chave Farm.

As teclas TDE que protegem as chaves por blob são armazenadas em dois locais:

- O repositório seguro, que abriga os certificados do BitLocker e é protegido pela Chave do Farm; e
- Em um repositório seguro gerenciado por Banco de Dados SQL do Azure.

As credenciais usadas para acessar os contêineres de armazenamento do Azure também são mantidas no armazenamento secreto do SharePoint Online e delegadas a cada farm SharePoint Online, conforme necessário. Essas credenciais são assinaturas SAS de armazenamento do Azure, com credenciais separadas usadas para ler ou gravar dados e com a política aplicada para que elas expirem automaticamente a cada 60 dias. Credenciais diferentes são usadas para ler ou gravar dados (não ambos) e SharePoint farms Online não têm permissões para enumerar.

> [!NOTE]
> Para Office 365 clientes do governo dos EUA, os blobs de dados são armazenados no Azure U.S. Government Armazenamento. Além disso, o acesso SharePoint chaves online Office 365 governo dos EUA está limitado Office 365 equipe que foram especificamente monitoradas. A equipe de operações do governo dos EUA do Azure não tem acesso ao armazenamento de chaves do SharePoint Online que é usado para criptografar blobs de dados.

Para obter mais informações sobre criptografia de dados no SharePoint Online e OneDrive for Business, consulte [Data Encryption in OneDrive for Business and SharePoint Online](https://technet.microsoft.com/library/dn905447.aspx).

### <a name="list-items-in-sharepoint-online"></a>Listar itens no SharePoint Online

Itens de lista são partes menores de dados do cliente que são criados ad-hoc ou que podem viver mais dinamicamente em um site, como linhas em uma lista criada pelo usuário, postagens individuais em um blog do SharePoint Online ou entradas dentro de uma página wiki do SharePoint Online. Os itens de lista são armazenados no Banco de Dados de Conteúdo (Banco de Dados SQL do Azure) e protegidos com o TDE.

## <a name="encryption-of-data-in-transit"></a>Criptografia de dados em trânsito

No OneDrive for Business e no SharePoint Online, há dois cenários em que os dados entram e saem dos data centers.

- **Comunicação do cliente com o servidor** - A comunicação SharePoint online e OneDrive for Business internet usa conexões TLS.
- **Movimentação de dados entre datacenters** - O principal motivo para mover dados entre datacenters é a replicação geográfica para habilitar a recuperação de desastres. Por exemplo, os logs de transação e os deltas de armazenamento de blobs do SQL Server passam por esse pipe. Embora esses dados já sejam transmitidos por meio de uma rede privada, eles estarão ainda mais protegidos com a melhor criptografia do mercado.

## <a name="exchange-online"></a>Exchange Online

Exchange Online usa o BitLocker para todos os dados de caixa de correio e a configuração do BitLocker é descrita em [BitLocker for Encryption](/microsoft-365/compliance/office-365-bitlocker-and-distributed-key-manager-for-encryption). A criptografia de nível de serviço criptografa todos os dados da caixa de correio no nível da caixa de correio. 

Além da criptografia de serviço, o Microsoft 365 oferece suporte à Chave do Cliente, que é criada com base na criptografia de serviço. A Chave do Cliente é uma opção de chave gerenciada pela Microsoft para Exchange Online de serviço que também está no Roteiro da Microsoft. Esse método de criptografia fornece maior proteção não proporcionada pelo BitLocker porque fornece a separação de administradores de servidores e as chaves criptográficas necessárias para a descriptografia de dados e porque a criptografia é aplicada diretamente aos dados (em contraste com o BitLocker, que aplica criptografia no volume de disco lógico) todos os dados do cliente copiados de um servidor Exchange permanecem criptografados.

O escopo para Exchange Online de serviço são os dados do cliente armazenados em repouso no Exchange Online. (Skype for Business armazena quase todo o conteúdo gerado pelo usuário na caixa de correio Exchange Online do usuário e, portanto, herda o recurso de criptografia de serviço Exchange Online.)


## <a name="microsoft-teams"></a>Microsoft Teams

Teams usa TLS e MTLS para criptografar mensagens instantâneas. Todo o tráfego de servidor para servidor requer MTLS, independentemente de o tráfego estar confinado à rede interna ou cruzar o perímetro de rede interno.

Esta tabela resume os protocolos usados por Teams.

|**Tipo de tráfego**|**Criptografado por**|
|:-----|:-----|
|Servidor para servidor|MTLS|
|Cliente para servidor (ex. mensagens instantâneas e presença)|TLS|
|Fluxos de mídia (ex. compartilhamento de áudio e vídeo de mídia)|TLS|
|Compartilhamento de áudio e vídeo de mídia|SRTP/TLS|
|Sinalização|TLS|

#### <a name="media-encryption"></a>Criptografia da mídia

O tráfego de mídia é criptografado usando SRTP, um perfil de protocolo RTP que fornece confidencialidade, autenticação e proteção contra ataque de repetição para o tráfego RTP. O SRTP usa uma chave de sessão gerada usando um gerador de número aleatório seguro e é trocado usando o canal TLS de sinalização. O tráfego de mídia de cliente para cliente é negociado por meio de uma sinalização de conexão de cliente para servidor, mas é criptografado usando SRTP ao ir de cliente para cliente diretamente.

Teams usa um token baseado em credenciais para acesso seguro a retransmissão de mídia por TURN. As retransmissão de mídia trocam o token por um canal protegido por TLS.

#### <a name="fips"></a>FIPS

Teams usa algoritmos compatíveis com FIPS (Federal Information Processing Standard) para trocas de chaves de criptografia. Para obter mais informações sobre a implementação do FIPS, consulte [FiPS (Federal Information Processing Standard) Publication 140-2](/microsoft-365/compliance/offering-fips-140-2).
