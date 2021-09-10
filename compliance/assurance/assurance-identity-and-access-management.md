---
title: Visão geral do gerenciamento de identidades e acesso
description: Saiba mais sobre gerenciamento de identidade e acesso em Microsoft 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH
ms.service: O365-seccomp
ms.localizationpriority: medium
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 933db3783c6672fa952f70f18c4815955bcedb21
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2021
ms.locfileid: "58946890"
---
# <a name="identity-and-access-management-overview"></a>Visão geral do gerenciamento de identidades e acesso

## <a name="how-do-microsoft-online-services-protect-production-systems-from-unauthorized-or-malicious-access"></a>Como os serviços online da Microsoft protegem os sistemas de produção contra acesso não autorizado ou mal-intencionado?

Os serviços online da Microsoft foram projetados para permitir que os engenheiros da Microsoft operem serviços sem acessar o conteúdo do cliente. Por padrão, os engenheiros da Microsoft têm o ZSA (Zero Standing Access) para conteúdo do cliente e nenhum acesso privilegiado ao ambiente de produção. Os serviços online da Microsoft usam um modelo Just-In-Time (JIT), Just-Enough-Access (JEA) para fornecer aos engenheiros de equipe de serviço acesso privilegiado temporário a ambientes de produção quando esse acesso for necessário para dar suporte aos serviços online da Microsoft. O modelo de acesso JIT substitui o acesso administrativo tradicional e persistente por um processo para os engenheiros solicitarem elevação temporária em funções privilegiadas quando necessário.

Engenheiros atribuídos a uma equipe de serviço para dar suporte à qualificação de solicitação de serviços de produção para uma conta de equipe de serviço por meio de uma solução de gerenciamento de identidade e acesso. A solicitação de qualificação dispara uma série de verificações de funcionários para garantir que o engenheiro tenha passado todos os requisitos de triagem na nuvem, concluído o treinamento necessário e recebido aprovação de gerenciamento apropriada antes da criação da conta. Somente depois de atender a todos os requisitos de qualificação, uma conta de equipe de serviço pode ser criada para o ambiente solicitado. Para manter a qualificação de uma conta de equipe de serviço, a equipe deve passar pelo treinamento baseado em função anualmente e rescreening a cada dois anos. A falha ao concluir ou passar essas verificações resulta em eligibilidades automaticamente revogadas.

As contas de equipe de serviço não concedem privilégios de administrador permanente ou acesso ao conteúdo do cliente. Quando um engenheiro exige acesso adicional para dar suporte aos serviços online da Microsoft, eles solicitam acesso temporário elevado aos recursos necessários usando uma ferramenta de gerenciamento de acesso chamada Lockbox. O lockbox restringe o acesso elevado aos privilégios mínimos, recursos e tempo necessários para concluir a tarefa atribuída. Se um revistor autorizado aprovar a solicitação de acesso JIT, o engenheiro recebe uma conta temporária com apenas os privilégios necessários para concluir seu trabalho atribuído. Essa conta temporária requer autenticação multifator e é excluída automaticamente após o período aprovado expirar.

JEA é imposto por eligibilidades e funções de Lockbox no momento da solicitação de acesso JIT. Somente as solicitações de acesso a ativos no escopo das eligibilidades do engenheiro são aceitas e repassadas ao aprovador. O Lockbox rejeita automaticamente as solicitações JIT que estão fora do escopo das funções de segurança e De bloqueio do engenheiro, incluindo solicitações que excedem limites permitidos.  

## <a name="how-do-microsoft-online-services-use-role-based-access-control-rbac-with-lockbox-to-enforce-least-privilege"></a>Como os serviços online da Microsoft usam o controle de acesso baseado em função (RBAC) com o Lockbox para impor o mínimo privilégio?

As contas de equipe de serviço não concedem privilégios de administrador permanente ou acesso ao conteúdo do cliente. As solicitações JIT para privilégios de administrador limitados são gerenciadas por meio do Lockbox. O lockbox usa o RBAC para limitar os tipos de solicitações de elevação JIT que os engenheiros podem fazer, fornecendo uma camada adicional de proteção para impor o mínimo privilégio. O RBAC também ajuda a impor a separação de funções limitando as contas de equipe de serviço às funções apropriadas.
Os engenheiros que suportam um serviço têm a associação a grupos de segurança com base em suas funções. A associação a um grupo de segurança não concede acesso privilegiado. Em vez disso, os grupos de segurança permitem que os engenheiros usem o Lockbox para solicitar a elevação JIT quando necessário para dar suporte ao sistema. As solicitações JIT específicas que um engenheiro pode fazer são limitadas por suas associações de grupo de segurança.

## <a name="how-do-microsoft-online-services-handle-remote-access-to-production-systems"></a>Como os serviços online da Microsoft lidam com o acesso remoto aos sistemas de produção?

Os componentes do sistema de serviços online da Microsoft estão ativos em datacenters geograficamente separados das equipes de operações. O pessoal do datacenter não tem acesso lógico aos sistemas de serviços online da Microsoft. Como resultado, a equipe de serviço da Microsoft gerencia o ambiente por meio do acesso remoto. A equipe de serviço que exige acesso remoto para dar suporte aos serviços online da Microsoft só tem acesso remoto após a aprovação de um gerente autorizado. Todo o acesso remoto usa TLS compatível com FIPS 140-2 para conexões remotas seguras.

Os serviços online da Microsoft usam Estações de Trabalho de Administrador Seguro (SAW) para acesso remoto da equipe de serviço para ajudar a proteger os ambientes de serviço online da Microsoft contra comprometimento. Essas estações de trabalho foram projetadas para evitar perda intencional ou não intencional de dados de produção, incluindo o bloqueio de portas USB e a limitação do software disponível na Estação de Trabalho de Administração Segura para o que é necessário para dar suporte ao ambiente. As Estações de Trabalho de Administrador Seguro são rastreadas e monitoradas de perto para detectar e impedir o comprometimento mal-intencionado ou inadvertido dos dados do cliente pelos engenheiros da Microsoft.

## <a name="how-does-customer-lockbox-add-additional-protection-for-customer-content"></a>Como o Customer Lockbox adiciona proteção ao conteúdo do cliente?

Os clientes podem adicionar um nível adicional de controle de acesso ao conteúdo habilitando o Customer Lockbox. Quando uma solicitação de elevação de lockbox envolve acesso ao conteúdo do cliente, o Customer Lockbox exige aprovação do cliente como uma etapa final no fluxo de trabalho de aprovação. Esse processo oferece às organizações a opção de aprovar ou negar essas solicitações e fornece controle de acesso direto ao cliente. Se o cliente rejeitar uma solicitação de Caixa de Bloqueio do Cliente, o acesso ao conteúdo solicitado será negado. Se o cliente não rejeitar ou aprovar a solicitação dentro de um determinado período, a solicitação expirará automaticamente sem que a Microsoft obtenha acesso ao conteúdo do cliente. Se o cliente aprovar a solicitação, o acesso temporário da Microsoft ao conteúdo do cliente será registrado, auditável e revogado automaticamente após o tempo atribuído para concluir a operação de solução de problemas expirar.

## <a name="related-external-regulations--certifications"></a>Regulamentações externas relacionadas & certificações

Os serviços online da Microsoft são regularmente auditados para conformidade com regulamentações e certificações externas. Consulte a tabela a seguir para validação de controles relacionados ao controle de identidade e acesso.

### <a name="azure-and-dynamics-365"></a>Azure e Dynamics 365

| **Auditorias externas** | **Section** | **Data do relatório mais recente** |
|:--------------------|:------------|:-----------------------|
| [ISO 27001/27002](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Instrução of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7af5304-3a31-40e6-9abb-e26352305d41&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.9.1: Requisitos de negócios do controle de acesso <br> A.9.2: Gerenciamento de acesso do usuário <br> A.9.3: responsabilidades do usuário <br> A.9.4: Controle de acesso de sistema e aplicativo <br> A.15.1: Segurança de informações nas relações de fornecedores | 2 de dezembro de 2020 |
| [ISO 27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Instrução of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a3bca0ac-867d-4204-b66b-13665f5f1e8d&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=25718a8a-f34d-41e1-a95a-c49246508787&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.9.1: Requisitos de negócios do controle de acesso <br> A.9.2: Gerenciamento de acesso do usuário <br> A.9.3: responsabilidades do usuário <br> A.9.4: Controle de acesso de sistema e aplicativo <br> A.15.1: Segurança de informações nas relações de fornecedores | 2 de dezembro de 2020 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b8721ebd-af20-42fe-b22f-8332b0a19517&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=234a0f57-83c1-4afc-a586-a0e7a59592f7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=75c8cbf6-e456-473c-a05e-34fea888ec2a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | OA-2: Acesso de provisionamento <br> OA-7: acesso JIT <br> OA-21: Estações de Trabalho de Administrador Seguro e MFA | 31 de março de 2021 |

### <a name="office-365"></a>Office 365

| **Auditorias externas** | **Section** | **Data do relatório mais recente** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP](https://compliance.microsoft.com/compliancemanager) | AC-2: Gerenciamento de contas <br> AC-3: Imposição de acesso <br> AC-5: separação de funções <br> AC-6: Privilégio mínimo <br> AC-17: Acesso remoto | 24 de setembro de 2020 |
| [ISO 27001/27002/27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Instrução of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.9.1: Requisitos de negócios do controle de acesso <br> A.9.2: Gerenciamento de acesso do usuário <br> A.9.3: responsabilidades do usuário <br> A.9.4: Controle de acesso de sistema e aplicativo <br> A.15.1: Segurança de informações nas relações de fornecedores | Abril de 20, 2021 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-33: Modificação da conta <br> CA-34: Autenticação do usuário <br> CA-35: Acesso privilegiado <br> CA-36: Acesso remoto <br> CA-57: Aprovação de gerenciamento do Microsoft Customer Lockbox <br> CA-58: Solicitações de serviço de Caixa de Bloqueio do Cliente <br> CA-59: Notificações de Caixa de Bloqueio do Cliente <br> CA-61: revisão e aprovação do JIT | 24 de dezembro de 2020 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-32: Política de conta compartilhada <br> CA-33: Modificação da conta <br> CA-34: Autenticação do usuário <br> CA-35: Acesso privilegiado <br> CA-36: Acesso remoto <br> CA-53: Monitoramento de terceiros <br> CA-56: Aprovação do cliente do Customer Lockbox <br> CA-57: Aprovação de gerenciamento do Microsoft Customer Lockbox <br> CA-58: Solicitações de serviço de Caixa de Bloqueio do Cliente <br> CA-59: Notificações de Caixa de Bloqueio do Cliente <br> CA-61: revisão e aprovação do JIT | 24 de dezembro de 2020 |
| [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-15: Solicitações de Cofre do Cliente | 24 de dezembro de 2020 |