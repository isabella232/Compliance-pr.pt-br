---
title: Controles de acesso administrativo no Microsoft 365
description: Este artigo fornece uma visão geral dos controles de acesso administrativo e categorização de dados no Microsoft 365.
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
f1.keywords:
- NOCSH
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: e7dc9d73b6eb1961387d85910bb558e85498ffae
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497697"
---
# <a name="administrative-access-controls-in-microsoft-365"></a>Controles de acesso administrativo no Microsoft 365 

A Microsoft investiu pesadamente em sistemas e controles que automatizam a maioria das operações do Microsoft 365, limitando intencionalmente o acesso ao conteúdo do cliente pela Microsoft. Os humanos governam o serviço e o software opera o serviço. Essa estrutura permite que a Microsoft gerencie o Microsoft 365 em escala e gerencie os riscos de ameaças internas ao conteúdo do cliente.

Por padrão, os engenheiros da Microsoft têm zero privilégios administrativos permanentes e zero acesso permanente ao conteúdo do cliente no Microsoft 365. Um engenheiro da Microsoft pode ter acesso limitado, auditado e protegido ao conteúdo de um cliente por um período limitado de tempo. O acesso é somente quando necessário para operações de serviço e somente quando aprovado por um membro do gerenciamento sênior da Microsoft. Para clientes licenciados no Customer Lockbox, o cliente fornece aprovação de acesso ao conteúdo hospedado no Microsoft 365.

A Microsoft fornece serviços online usando várias formas de entrega na nuvem:

- **Nuvens públicas:** Inclui versões multi-locatários do Microsoft 365, Azure e outros serviços hospedados na América do Norte, América do Sul, Europa, Ásia, Austrália, etc.
- **Nuvens nacionais:** Inclui todas as nuvens soberanas e de terceiros operados fora dos Estados Unidos (exceto aquelas notadas anteriormente), como o Microsoft 365 na China (operado pela 21Vianet) e o Microsoft 365 na Alemanha (operado pela Microsoft, mas em um modelo no qual um administrador de dados alemão, Deutsche Telekom, controla e monitora o acesso da Microsoft aos dados do cliente e sistemas que contêm dados do cliente).
- **Nuvens do governo:** Inclui serviços do Microsoft 365 e do Azure que estão disponíveis para clientes do governo dos Estados Unidos.

Para fins deste artigo, os serviços do Microsoft 365 incluem:

- [Exchange Online](/Exchange/exchange-online)
- [Proteção do Exchange Online](/Office365/SecurityCompliance/eop/exchange-online-protection-overview)
- [SharePoint Online](/sharepoint/sharepoint-online)
- [OneDrive for Business](/OneDrive/onedrive)
- [Skype for Business](/SkypeForBusiness/skype-for-business-online)
- [Microsoft Teams](/MicrosoftTeams/Teams-overview)
- [Yammer](/yammer/yammer-landing-page)

## <a name="microsoft-365-access-controls"></a>Controles de acesso do Microsoft 365

Para fins de controle de acesso, a Microsoft categoriza os dados do Microsoft 365 como dados do cliente ou outros tipos de dados.

### <a name="customer-data"></a>Dados do cliente

Os dados do cliente são todos os dados fornecidos por ou em nome de um cliente ao usar os serviços do Microsoft 365. Esses dados são conteúdo do cliente criado ou carregado diretamente pelos usuários do Microsoft 365, incluindo:

- Emails
- Conteúdo do SharePoint Online
- Mensagens instantâneas
- Itens de calendário
- Documentos
- Contatos
- Informações de identificação do usuário final (EUII) (dados exclusivos de um usuário ou que podem ser vinculados a um usuário individual, mas não incluem conteúdo do cliente)

### <a name="other-types-of-data"></a>Outros tipos de dados

Outros tipos de dados incluem:

- **Dados da conta:** Inclui dados administrativos (informações fornecidas pelos administradores ao se inscrever ou comprar serviços) e dados de pagamento (informações sobre os instrumentos de pagamento, como detalhes do cartão de crédito).
- **Informações de identificação organizacional:** Inclui dados usados para identificar um locatário, dados de uso e não vinculáveis a um usuário individual ou incluídos no conteúdo do cliente.
- **Metadados do sistema:** Inclui logs de serviço que contêm configurações, status do sistema, endereços IP da Microsoft e informações técnicas sobre assinaturas e locatários.

A Microsoft estabeleceu mecanismos de controle de acesso para garantir que ninguém tenha acesso não aprovado aos Dados do Cliente ou aos dados de controle de acesso. Os dados de controle de acesso gerenciam o acesso a outros tipos de dados ou funções no ambiente, incluindo o acesso ao conteúdo do cliente ou à EUII, senhas da Microsoft, certificados de segurança e outros dados relacionados à autenticação. Os mecanismos de controle de acesso também se resguardam contra acesso físico, lógico ou remoto não aprovado ao ambiente de produção do Microsoft 365.

Há três categorias de controles de acesso usados pela Microsoft para operar o Microsoft 365:

- Controles de isolamento
- Controles de equipe
- Controles de tecnologia

Quando combinados, esses controles ajudam a evitar e detectar ações mal-intencionadas no Microsoft 365. Além dos controles de isolamento, pessoal e tecnologia usados pela Microsoft, há uma quarta categoria de controles: os controles implementados pelos clientes.

O Microsoft 365 permite gerenciar dados da mesma maneira que os dados são gerenciados em ambientes locais. A pessoa que insissou uma organização para o Microsoft 365 se torna automaticamente um administrador global. O administrador global tem acesso a todos os recursos em Portais de Gerenciamento e pode:

- Criar ou editar usuários
- Atribuir funções de administrador a outras pessoas
- Redefinir senhas do usuário
- Gerenciar licenças de usuário
- Gerenciar domínios
- Aprovar solicitações do Customer Lockbox

Recomendamos que cada organização configure pelo menos duas contas de administrador. Para grandes organizações empresariais, recomendamos contas de administrador especializadas que atendem a funções diferentes.

Para obter informações sobre como atribuir funções e permissões de administrador, consulte [Assign admin roles](/microsoft-365/admin/add-users/assign-admin-roles) and About admin [roles](/microsoft-365/admin/add-users/about-admin-roles).

## <a name="related-links"></a>Links relacionados

- [Isolamento no Microsoft 365](assurance-isolation-in-microsoft-365.md)
- [Triagem de pré-emprego da Microsoft](assurance-pre-employment-screening.md)
- [Verificação de antecedentes da nuvem da Microsoft](assurance-cloud-background-check.md)
- [Monitorando e auditando controles de acesso ](assurance-monitoring-and-auditing-access-controls.md)
- [Controles de acesso do Yammer Enterprise](assurance-yammer-enterprise-access-controls.md)
