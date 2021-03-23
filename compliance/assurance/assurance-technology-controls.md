---
title: Controles de tecnologia no Microsoft 365
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
ms.openlocfilehash: c3b443505c78832af47719e6840c8b7011f9dfe1
ms.sourcegitcommit: 2b347c9b778ac9b6450daf20fdf8eb74ed14cbbd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51002161"
---
# <a name="technology-controls-in-microsoft-365"></a>Controles de tecnologia no Microsoft 365 

A Microsoft usa várias ferramentas e tecnologias para controlar, gerenciar e auditar o acesso aos dados do cliente em seus serviços online. Elas se aplicam ao Exchange Online, SharePoint Online, Lockbox e Customer Lockbox, autenticação multifatório e muito mais. O Yammer usa controles semelhantes descritos em [Controles do Yammer Enterprise Access.](assurance-yammer-enterprise-access-controls.md)

Os engenheiros do Microsoft 365 não têm acesso permanente aos dados do cliente do Microsoft 365. Os engenheiros devem passar por um processo de aprovação da Microsoft antes que o acesso aos Dados do Cliente para operações de serviço ocorra. Se o cliente licenciar o recurso de Caixa de Bloqueio do Cliente para o Exchange Online e o SharePoint Online, o acesso aos Dados do Cliente exigirá aprovação do cliente. Depois de aprovadas, contas administrativas específicas do serviço são provisionadas acesso just-in-time para tarefas exigidas pela solicitação de serviço.

## <a name="lockbox-and-customer-lockbox"></a>Lockbox e Customer Lockbox

Embora raro, um cliente pode solicitar assistência da Microsoft que expõe o conteúdo do cliente a um engenheiro da Microsoft. Para controlar o acesso ao Exchange Online, a Microsoft usa um sistema de controle de acesso chamado Lockbox. Antes que qualquer engenheiro da Microsoft acesse qualquer sistema ou dados do Exchange Online ou do SharePoint Online, ele deve enviar uma solicitação de acesso usando o Lockbox. Todas as solicitações de serviço para o Exchange Online e o SharePoint Online são manipuladas pelo sistema lockbox. Com o Lockbox e o Customer Lockbox, todo o acesso aprovado pode ser rastreado para um usuário exclusivo, tornando os engenheiros responsáveis pela manipulação dos Dados do Cliente.

> [!NOTE]
> O Exchange Online inclui todos os dados do Skype for Business armazenados em caixas de correio de usuário. A cobertura do Skype for Business não inclui gravações de Transmissão de Reunião do Skype ou conteúdo carregado em reuniões pelos usuários. O SharePoint Online inclui o OneDrive for Business.

O lockbox processa solicitações de permissões que concedem aos engenheiros a capacidade de executar funções operacionais e administrativas dentro do serviço. Os engenheiros enviam solicitações por meio do Lockbox e um gerente da Microsoft deve aprovar a solicitação para que o engenheiro possa acessar Dados do Cliente. Após a aprovação do gerente, o engenheiro tem acesso limitado por tempo e escopo aos Dados do Cliente para trabalhar no problema do cliente.

O Customer Lockbox do Microsoft 365 ajuda você a cumprir as obrigações de conformidade se precisar de procedimentos para autorização explícita de acesso a dados. Esse é um requisito para alguns padrões de conformidade, como FedRAMP e HIPAA. O Customer Lockbox insere você no processo de aprovação do Lockbox e oferece a capacidade de controlar a autorização do acesso da Microsoft ao conteúdo do Exchange Online ou do SharePoint Online para operações de serviço.

Na rara instância em que um engenheiro de serviço da Microsoft precisa acessar seus dados, você concede acesso apenas aos dados necessários para resolver o problema e por um período limitado de tempo. Se você rejeitar uma solicitação de acesso, os engenheiros da Microsoft não terão acesso ao conteúdo e não poderão concluir as operações de serviço. Se você aprovar a solicitação, os engenheiros da Microsoft terão acesso just-in-time limitado ao seu conteúdo por meio de interfaces de gerenciamento monitoradas e restritas.

As ações realizadas pelo engenheiro de suporte são registradas para fins de auditoria e podem ser acessadas por meio da API de Atividade de Gerenciamento do [Office 365](/office/office-365-management-api/get-started-with-office-365-management-apis) e do Centro de Segurança [e Conformidade.](https://protection.office.com/)

>[!NOTE]
> O Customer Lockbox está disponível no [Microsoft 365 E5](https://products.office.com/business/office-365-enterprise-e5-business-software) como uma compra de complemento. Para obter mais informações, consulte Solicitações de Caixa de Bloqueio do [Cliente do Microsoft 365.](https://support.office.com/article/Office-365-Customer-Lockbox-Requests-36f9cdd1-e64c-421b-a7e4-4a54d16440a2)

## <a name="just-in-time-access"></a>Acesso just-in-time

A Microsoft usa o princípio de acesso just-in-time (JIT) para o Microsoft 365 para reduzir os riscos de adulteração de credenciais e ataques laterais. O JIT remove o acesso administrativo persistente aos serviços e substitui os direitos pela capacidade de elevar para essas funções sob demanda. Remover direitos de acesso persistente dos administradores garante que as credenciais só estarão disponíveis quando necessárias e reduz os riscos de roubo de credenciais.

O modelo de acesso JIT exige que os engenheiros solicitem privilégios elevados por um período limitado para executar tarefas administrativas. Além disso, os engenheiros usam contas temporárias criadas com senhas complexas geradas por máquina e concedem apenas as funções que lhes permitem executar tarefas necessárias. Por exemplo, o acesso administrativo concedido pelo Lockbox tem limite de tempo e o tempo de acesso concedido depende da função solicitada. Um engenheiro especifica a duração do acesso de tempo necessário na solicitação para o sistema lockbox. O sistema lockbox rejeita solicitações quando o tempo solicitado excede o tempo máximo permitido para a elevação. Após a expiração, o acesso administrativo é removido e a conta temporária expira.

Quando autorizados e aprovados para acesso, os engenheiros recebem uma senha administrativa de uso único gerada pelo sistema de autorização. Novas senhas são geradas sempre que uma solicitação de acesso elevado é aprovada. A senha é copiada para um cofre de senha, é separada das credenciais do engenheiro para o ambiente corporativo da Microsoft e só é boa para a sessão de acesso elevado aprovada.

## <a name="constrained-management-interfaces"></a>Interfaces de Gerenciamento Restritas

Os engenheiros usam duas interfaces de gerenciamento para executar tarefas administrativas: Área de trabalho remota por meio de TSGs (Gateways de Serviço de Terminal) protegidos e PowerShell Remoto. Dentro dessas interfaces de gerenciamento, as políticas de software e os controles de acesso impõem restrições significativas sobre quais aplicativos são executados e quais comandos e cmdlets estão disponíveis.

Os servidores do Microsoft 365 restringem sessões simultâneas a um administrador de equipe por serviço, por servidor. Os TSGs permitem apenas uma única sessão simultânea para os usuários e não permitem várias sessões. Usando uma única sessão por servidor, os TSGs permitem que os administradores de equipe de serviço do Microsoft 365 se conectem a vários servidores simultaneamente para que os administradores possam efetivamente executar suas obrigações. Os administradores da equipe de serviço não têm permissões nos próprios TSGs. O TSG é usado apenas para impor requisitos de autenticação multifagão (MFA) e criptografia. Quando o administrador da equipe de serviço se conecta a um servidor específico por meio de um TSG, o servidor específico impõe um limite de sessão de um por administrador.

As restrições de uso e os requisitos de conexão e configuração para a equipe do Microsoft 365 são estabelecidos pelas políticas de grupo do Active Directory. Essas políticas incluem as seguintes características:

- Os TSGs usam apenas [criptografia fips](https://www.microsoft.com/TrustCenter/Compliance/FIPS) 140-2 validada.
- As sessões TSG se desconectam após 30 minutos de inatividade.
- As sessões TSG são automaticamente desligadas após 24 horas.

As conexões com TSGs também exigem MFA usando um cartão inteligente físico separado e uma conta separada das credenciais corporativas da Microsoft do engenheiro. Os engenheiros são emitidos cartões inteligentes diferentes para várias plataformas e plataformas de gerenciamento de segredos, garantindo o armazenamento seguro de credenciais. Os TSGs usam políticas de grupo do Active Directory para controlar quem pode fazer logon em servidores remotos, o número de sessões permitidas e as configurações de tempo de tempo ocioso. Políticas adicionais limitam o acesso a aplicativos permitidos e restringem o acesso à Internet.

Além do acesso remoto usando TSGs especialmente configurados, o Exchange Online permite que os usuários com a função Operações de Engenheiro de Serviço acessem determinada funcionalidade administrativa em servidores de produção usando o PowerShell Remoto. Para fazer isso, o usuário deve ser autorizado para acesso somente leitura (depuração) ao ambiente de produção do Microsoft 365. A escalonamento de privilégios é habilitada da mesma maneira que está habilitada para TSGs usando o processo lockbox.

Para acesso remoto, cada datacenter tem um IP virtual com balanceamento de carga que serve como um único ponto de acesso. Os cmdlets do PowerShell remoto disponíveis se baseiam no nível de privilégio identificado na declaração de acesso obtida durante a autenticação. Esses cmdlets fornecem a única funcionalidade administrativa acessível pelos usuários que se conectam usando esse método. O PowerShell remoto limita o escopo de comandos disponíveis para o engenheiro e se baseia no nível de acesso concedido por meio do processo lockbox. Por exemplo, no Exchange Online, Get-Mailbox pode estar disponível, mas Set-Mailbox não estaria.
