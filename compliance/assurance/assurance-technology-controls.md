---
title: 'Controles de tecnologia no Microsoft 365 '
description: Este artigo fornece uma visão geral das ferramentas e tecnologias usadas pela Microsoft para controle de tecnologia no Microsoft 365.
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
f1.keywords:
- NOCSH
ms.custom:
- seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 2c02e1739f6d3b5981e4327139477a12f987ed68
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120730"
---
# <a name="technology-controls-in-microsoft-365"></a>Controles de tecnologia no Microsoft 365 

A Microsoft usa várias ferramentas e tecnologias para controlar, gerenciar e auditar o acesso aos dados do cliente em seus serviços online. Elas se aplicam ao Exchange Online, SharePoint Online, Lockbox e Sistema de Proteção de Dados do Cliente, autenticação multifatório e muito mais. O Yammer usa controles semelhantes descritos [nos controles de acesso do Yammer Enterprise.](assurance-yammer-enterprise-access-controls.md)

Os engenheiros do Microsoft 365 não têm acesso permanente aos dados do cliente do Microsoft 365. Os engenheiros devem passar por um processo de aprovação da Microsoft antes que ocorra o acesso aos Dados do Cliente para operações de serviço. Se o cliente licenciar o recurso Sistema de Proteção de Dados do Cliente para o Exchange Online e o SharePoint Online, o acesso aos Dados do Cliente exigirá aprovação do cliente. Após a aprovação, as contas administrativas específicas do serviço são provisionadas com acesso just-in-time para tarefas exigidas pela solicitação de serviço.

## <a name="lockbox-and-customer-lockbox"></a>Lockbox e Customer Lockbox

Embora raro, um cliente pode solicitar assistência da Microsoft que exponha o conteúdo do cliente a um engenheiro da Microsoft. Para controlar o acesso ao Exchange Online, a Microsoft usa um sistema de controle de acesso chamado Lockbox. Antes de qualquer engenheiro da Microsoft acessar qualquer sistema ou dados do Exchange Online ou do SharePoint Online, ele deve enviar uma solicitação de acesso usando o Lockbox. Todas as solicitações de serviço para o Exchange Online e o SharePoint Online são manipuladas pelo sistema do Lockbox. Com o Lockbox e o Sistema de Proteção de Dados do Cliente, todo o acesso aprovado é rastreável para um usuário exclusivo, tornando os engenheiros responsáveis pela manipulação dos Dados do Cliente.

> [!NOTE]
> O Exchange Online inclui todos os dados do Skype for Business armazenados nas caixas de correio do usuário. A cobertura do Skype for Business não inclui gravações da Transmissão de Reunião do Skype ou conteúdo carregado para reuniões pelos usuários. O SharePoint Online inclui o OneDrive for Business.

O Lockbox processa solicitações de permissões que concedem aos engenheiros a capacidade de executar funções operacionais e administrativas dentro do serviço. Os engenheiros enviam solicitações por meio do Lockbox e um gerente da Microsoft deve aprovar a solicitação para que o engenheiro possa acessar os Dados do Cliente. Após a aprovação do gerente, o engenheiro tem acesso limitado por tempo e escopo aos Dados do Cliente para trabalhar no problema do cliente.

O Sistema de Proteção de Dados do Cliente do Microsoft 365 ajuda você a cumprir as obrigações de conformidade se precisar de procedimentos para autorização explícita de acesso a dados. Esse é um requisito para alguns padrões de conformidade, como FedRAMP e HIPAA. O Sistema de Proteção de Dados do Cliente insere você no processo de aprovação do Lockbox e oferece a capacidade de controlar a autorização do acesso da Microsoft ao conteúdo do Exchange Online ou do SharePoint Online para operações de serviço.

Na rara instância em que um engenheiro de serviços da Microsoft precisa acessar seus dados, conceda acesso apenas aos dados necessários para resolver o problema e por um período limitado de tempo. Se você rejeitar uma solicitação de acesso, os engenheiros da Microsoft não terão acesso ao seu conteúdo e não poderão concluir as operações de serviço. Se você aprovar a solicitação, os engenheiros da Microsoft limitaram o acesso just-in-time ao seu conteúdo por meio de interfaces de gerenciamento monitoradas e restritas.

As ações tomadas pelo engenheiro de suporte são registradas para fins de auditoria e podem ser acessadas por meio da API da Atividade de Gerenciamento do [Office 365](/office/office-365-management-api/get-started-with-office-365-management-apis) e do Centro de Conformidade [e Segurança.](https://protection.office.com/)

>[!NOTE]
> O Sistema de Bloqueio do Cliente está disponível [no Microsoft 365 E5](https://products.office.com/business/office-365-enterprise-e5-business-software) como uma compra de complemento. Para saber mais, confira Solicitações do Sistema de Bloqueio de Clientes [do Microsoft 365.](https://support.office.com/article/Office-365-Customer-Lockbox-Requests-36f9cdd1-e64c-421b-a7e4-4a54d16440a2)

## <a name="just-in-time-access"></a>Acesso just-in-time

A Microsoft usa o princípio de acesso just-in-time (JIT) do Microsoft 365 para reduzir os riscos de adulteração de credenciais e ataques laterais. O JIT remove o acesso administrativo persistente aos serviços e substitui os direitos pela capacidade de elevar essas funções sob demanda. A remoção de direitos de acesso persistente dos administradores garante que as credenciais sejam disponibilizadas somente quando necessárias e reduz os riscos de roubo de credenciais.

O modelo de acesso JIT exige que os engenheiros solicitem privilégios elevados por um período limitado para executar tarefas administrativas. Além disso, os engenheiros usam contas temporárias criadas com senhas complexas geradas por máquina e concedem apenas as funções que lhes permitem executar as tarefas necessárias. Por exemplo, o acesso administrativo concedido pelo Lockbox tem limite de tempo, e a quantidade de tempo de acesso concedido depende da função solicitada. Um engenheiro especifica a duração do acesso de tempo necessário na solicitação para o sistema do Lockbox. O sistema do Lockbox rejeita solicitações quando o tempo solicitado excede o tempo máximo permitido para a elevação. Após a expiração, o acesso administrativo é removido e a conta temporária expira.

Quando autorizados e aprovados para acesso, os engenheiros recebem uma senha administrativa de uso único gerada pelo sistema de autorização. Novas senhas são geradas sempre que uma solicitação de acesso elevado é aprovada. A senha é copiada para uma senha segura, é separada das credenciais do engenheiro para o ambiente corporativo da Microsoft e é boa somente para a sessão de acesso elevado aprovada.

## <a name="constrained-management-interfaces"></a>Interfaces de Gerenciamento Restritas

Os engenheiros usam duas interfaces de gerenciamento para realizar tarefas administrativas: Área de Trabalho Remota por meio de TSGs (Gateways de Serviço de Terminal) e PowerShell Remoto. Nessas interfaces de gerenciamento, as políticas de software e os controles de acesso impõem restrições significativas sobre quais aplicativos são executados e quais comandos e cmdlets estão disponíveis.

Os servidores do Microsoft 365 restringem sessões simultâneas a uma sessão por administrador de equipe por serviço, por servidor. Os TSGs permitem apenas uma única sessão simultânea para os usuários e não permitem várias sessões. Usando uma única sessão por servidor, os TSGs permitem que os administradores da equipe de serviço do Microsoft 365 se conectem a vários servidores simultaneamente para que os administradores possam executar efetivamente suas tarefas. Os administradores da equipe de serviço não têm permissões nos próprios TSGs. O TSG é usado apenas para impor requisitos de autenticação multifafa (MFA) e criptografia. Depois que o administrador da equipe de serviço se conecta a um servidor específico por meio de um TSG, o servidor específico impõe um limite de sessão de um por administrador.

As restrições de uso e os requisitos de conexão e configuração para a equipe do Microsoft 365 são estabelecidos pelas políticas de grupo do Active Directory. Essas políticas incluem as seguintes características:

- Os TSGs usam apenas [criptografia validada FIPS](https://www.microsoft.com/TrustCenter/Compliance/FIPS) 140-2.
- As sessões TSG se desconectam após 30 minutos de inatividade.
- As sessões do TSG são automaticamente desaconhecdas após 24 horas.

As conexões com TSGs também exigem a MFA usando um cartão inteligente físico separado e uma conta separada das credenciais corporativas da Microsoft do engenheiro. Os engenheiros emissão de cartões inteligentes diferentes para várias plataformas e plataformas de gerenciamento de segredos garantem um armazenamento seguro de credenciais. Os TSGs usam políticas de grupo do Active Directory para controlar quem pode fazer logon em servidores remotos, o número de sessões permitidas e as configurações de tempo de ociosidade. Políticas adicionais limitam o acesso a aplicativos permitidos e restringem o acesso à Internet.

Além do acesso remoto usando TSGs especialmente configurados, o Exchange Online permite que os usuários com a função de Engenheiro de Serviço acessem determinadas funcionalidades administrativas em servidores de produção usando o PowerShell Remoto. Para fazer isso, o usuário deve estar autorizado para acesso somente leitura (depuração) ao ambiente de produção do Microsoft 365. O escalonamento de privilégios é habilitado da mesma maneira que é habilitado para TSGs usando o processo do Lockbox.

Para acesso remoto, cada datacenter tem um IP virtual com balanceamento de carga que serve como um único ponto de acesso. Os cmdlets do PowerShell Remoto disponíveis se baseiam no nível de privilégio identificado na declaração de acesso obtida durante a autenticação. Esses cmdlets fornecem a única funcionalidade administrativa acessível pelos usuários que se conectam usando esse método. O PowerShell remoto limita o escopo dos comandos disponíveis para o engenheiro e se baseia no nível de acesso concedido por meio do processo do Lockbox. Por exemplo, no Exchange Online, Get-Mailbox pode estar disponível, Set-Mailbox não.
