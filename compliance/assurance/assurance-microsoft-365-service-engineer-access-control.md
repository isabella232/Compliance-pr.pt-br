---
title: Microsoft 365 de acesso do engenheiro de serviço
description: Uma visão geral da arquitetura Microsoft 365 de controle de acesso do engenheiro de serviço.
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
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 2700c95feb5c32765e2dc3420c67800b154b1e9d
ms.sourcegitcommit: 85b36ce8c79fb111980cc6462f2addb44a924065
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2021
ms.locfileid: "60678458"
---
# <a name="microsoft-365-service-engineer-access-control"></a>Microsoft 365 de acesso do engenheiro de serviço

Zero Standing Access (ZSA) significa que os funcionários da equipe de serviço da Microsoft não têm acesso privilegiado permanente ao ambiente de produção Microsoft 365 ou aos dados do cliente. Quando um membro da equipe de serviço da Microsoft deseja atualizar o serviço ou acessar dados do cliente por qualquer motivo, ele deve enviar uma solicitação que justifique a necessidade e receba aprovação de um gerente autorizado. Em escala, não é viável fornecer e remover o acesso manualmente conforme necessário para manter os serviços Microsoft 365, portanto, a Microsoft desenvolveu uma solução automatizada para gerenciar o acesso privilegiado conforme necessário.

## <a name="lockbox"></a>Lockbox

Todo o acesso aos sistemas Microsoft 365 e aos dados do cliente é intermediado pelo Lockbox, um sistema de controle de acesso que usa um modelo Just-In-Time (JIT) e Just-Enough-Access (JEA) para fornecer aos engenheiros de serviço acesso privilegiado temporário aos serviços e dados de Microsoft 365 especificados. Além disso, todas as solicitações e ações são registradas para fins de auditoria e podem ser acessadas usando [Office 365 API](/office/office-365-management-api/get-started-with-office-365-management-apis) de Atividade de Gerenciamento e o Centro de Segurança [e Conformidade.](https://protection.office.com/)

Antes que um engenheiro de serviço da Microsoft possa se conectar a qualquer sistema Microsoft 365 ou acessar dados do cliente, ele deve enviar uma solicitação de acesso por meio do Lockbox. Essa solicitação só poderá ser aprovada se determinados critérios são atendidos:

- O engenheiro de serviço atende [aos requisitos de qualificação para uma conta de equipe de serviço,](assurance-microsoft-365-account-management.md)
- Eles pertencem à função Lockbox associada ao trabalho na solicitação,
- O tempo de acesso solicitado não excede o tempo máximo permitido,
- Eles têm uma justificativa de negócios legítima,
- O recurso solicitado que eles desejam acessar está dentro do escopo de trabalho e
- Eles recebem aprovação do gerente

Depois que todos os critérios foram atendidos e verificados pelo Lockbox, o acesso temporário é concedido para executar a ação específica solicitada. Após o tempo decorrido para a solicitação, o acesso é revogado.

![Processo de acesso ao cofre.](../media/assurance-lockbox-process.png)

Além disso, se um cliente licenciar e habilitar o recurso de Caixa de Bloqueio do Cliente, qualquer tentativa de um engenheiro de serviço da Microsoft para acessar dados do cliente deverá ser aprovada adicionalmente por um administrador no locatário do cliente. [](/microsoft-365/compliance/customer-lockbox-requests) A necessidade de acessar dados do cliente pode surgir tanto do cliente quanto da Microsoft. Por exemplo, um incidente gerado por um cliente pode exigir acesso a seus dados para corrigir o problema ou quando a Microsoft precisa de acesso a dados para aplicar uma atualização específica.

![Processo de acesso ao Cofre do Cliente.](../media/assurance-customer-lockbox-process.png)

Os clientes não têm ferramentas para iniciar uma solicitação de Caixa de Bloqueio do Cliente; eles devem enviar um tíquete para a Microsoft que exige que uma solicitação de Caixa de Bloqueio do Cliente seja a levantada. Uma solicitação de Caixa de Bloqueio de Cliente acatada por um engenheiro de serviço da Microsoft deve ser aprovada por um Microsoft Manager e um administrador autorizado no locatário do cliente.

### <a name="lockbox-roles"></a>Funções de cofre

Para impor a separação de funções e o princípio de privilégio mínimo, os engenheiros de serviço devem pertencer a uma função lockbox que corresponde à sua função na equipe. As funções de cofre são gerenciadas na ferramenta Gerenciamento de Identidade e definem os privilégios e ações para as quais um membro da equipe de serviço pode ser aprovado por meio do processo de solicitação do Lockbox. A equipe de serviço deve solicitar ser membro de uma função de Lockbox e receber aprovação gerencial. Se aprovado, a conta de equipe de serviço do funcionário é colocada em um grupo de segurança imposto pelo Active Directory (AD) e Azure Active Directory (AAD).

## <a name="constrained-management-interfaces"></a>Interfaces de gerenciamento restritas

Os engenheiros de serviço usam duas interfaces de gerenciamento para executar tarefas administrativas: Área de trabalho remota de uma Estação de Trabalho de Acesso Seguro (SAW) por meio de um TSG (Terminal Service Gateway) protegido e o PowerShell Remoto. Dentro dessas interfaces de gerenciamento, os controles de acesso com base na solicitação de Lockbox e políticas de software aprovadas impõem restrições significativas sobre quais aplicativos são executados e quais comandos e cmdlets estão disponíveis.

## <a name="remote-desktop"></a>Área de Trabalho Remota

Os membros da equipe de serviço que administram o serviço usando a Área de Trabalho Remota devem se conectar a partir de um SAW, laptops especialmente projetados e fabricados gerenciados pela Microsoft especificamente para esse caso de uso. A Microsoft faz parcerias com fornecedores para criar SAWs, criando uma cadeia de fornecimento curta e segura. Os SAWs usam sistemas operacionais fortemente configurados para limitar todas as funcionalidades, exceto o necessário para tarefas de gerenciamento definidas. Essas limitações incluem desabilitação de todas as portas USB, listas estritas de acesso a aplicativos, remoção de acesso de email, limitação da navegação na Internet e imposição de bloqueios de protetor de tela de inatividade. Os sistemas de controle de acesso da Microsoft examinam periodicamente as máquinas SAW para garantir que estão em conformidade com os controles de segurança mais recentes e desabilitam automaticamente os máquinas se eles são determinados como não compatíveis.

Os engenheiros de serviço só têm permissão para se conectar a um TSG por vez e várias sessões não são permitidas. No entanto, os TSGs permitem que Microsoft 365 de equipe de serviço se conectem a vários servidores, cada um com apenas uma sessão simultânea, para que os administradores possam efetivamente executar suas obrigações. Os administradores da equipe de serviço não têm permissões nos próprios TSGs. O TSG é usado apenas para impor requisitos de autenticação multifator (MFA) e criptografia. Quando o administrador da equipe de serviço se conecta a um servidor específico por meio de um TSG, o servidor específico impõe um limite de sessão de um por administrador.

As restrições de uso, a conexão e os requisitos de configuração Microsoft 365 pessoal são estabelecidos pelas políticas de grupo do Active Directory. Essas políticas incluem as seguintes características TSG:

- Usar somente [criptografia validada FIPS 140-2](/compliance/regulatory/offering-FIPS-140-2)
- Sessões desconectadas após 15 minutos de inatividade
- As sessões são automaticamente desligadas após 24 horas

As conexões com TSGs também exigem MFA usando um cartão inteligente físico separado. Os engenheiros de serviço são emitidos cartões inteligentes diferentes para várias plataformas e plataformas de gerenciamento de segredos, garantindo o armazenamento seguro de credenciais. Os TSGs usam políticas de grupo do Active Directory para controlar quem pode fazer logon em servidores remotos, o número de sessões permitidas e as configurações de tempo de tempo ocioso.

## <a name="remote-powershell"></a>PowerShell Remoto

Além do acesso remoto usando TSGs especialmente configurados, a equipe de serviço com a função de Lockbox operações do Engenheiro de Serviço pode acessar determinada funcionalidade administrativa em servidores de produção usando o PowerShell Remoto. Para usar esse acesso, o usuário deve ser autorizado para acesso somente leitura (depuração) ao ambiente Microsoft 365 produção. A escalonamento de privilégios é habilitada da mesma maneira que está habilitada para TSGs usando o processo lockbox.

Para acesso remoto, cada datacenter tem um IP virtual com balanceamento de carga que serve como um único ponto de acesso. Os cmdlets do PowerShell remoto disponíveis se baseiam no nível de privilégio identificado na declaração de acesso obtida durante a autenticação. Esses cmdlets fornecem a única funcionalidade administrativa acessível pelos usuários que se conectam usando esse método. O PowerShell remoto limita o escopo de comandos disponíveis para o engenheiro e se baseia no nível de acesso concedido por meio do processo lockbox. Por exemplo, Exchange Online, o cmdlet Get-Mailbox pode estar disponível, mas o cmdlet Set-Mailbox não.

## <a name="resources"></a>Recursos

- [Isolamento no Microsoft 365](assurance-isolation-in-microsoft-365.md)
- [Verificação de plano de fundo](assurance-pre-employment-screening.md)de nuvem da Microsoft de[pré-contratação da Microsoft](assurance-cloud-background-check.md)
