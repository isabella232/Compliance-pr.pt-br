---
title: Visão geral do gerenciamento de identidades e acesso
description: Saiba mais sobre gerenciamento de identidade e acesso no Microsoft 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: d431a7f04b156b003f5f4e213aef9bb9792874fe
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497166"
---
# <a name="identity-and-access-management-overview"></a>Visão geral do gerenciamento de identidades e acesso

## <a name="how-does-microsoft-365-protect-production-systems-from-unauthorized-or-malicious-access"></a>Como o Microsoft 365 protege sistemas de produção contra acesso não autorizado ou mal-intencionado?

O Microsoft 365 foi projetado para permitir que os engenheiros da Microsoft operem o serviço sem acessar o conteúdo do cliente. Por padrão, os engenheiros do Microsoft 365 têm o ZSA (Zero Standing Access) para conteúdo do cliente e nenhum acesso privilegiado ao ambiente de produção. O Microsoft 365 usa um modelo Just-In-Time (JIT), Just-Enough-Access (JEA) para fornecer aos engenheiros de equipe de serviço acesso privilegiado temporário a ambientes de produção quando esse acesso for necessário para dar suporte ao Microsoft 365. O modelo de acesso JIT substitui o acesso administrativo tradicional persistente por um processo para os engenheiros solicitarem elevação temporária em funções privilegiadas quando necessário.

Engenheiros atribuídos a uma equipe de serviço para dar suporte à qualificação de solicitação de serviços de produção para uma conta de equipe de serviço por meio da Ferramenta de Gerenciamento de Identidade (IDM). A solicitação de qualificação dispara uma série de verificações de funcionários para garantir que o engenheiro tenha passado todos os requisitos de triagem na nuvem, concluído o treinamento necessário e recebido aprovação de gerenciamento apropriada antes da criação da conta. Somente depois de atender a todos os requisitos de qualificação pode ser criada uma conta de equipe de serviço para o ambiente solicitado.

As contas de equipe de serviço não concedem privilégios de administrador permanente ou acesso ao conteúdo do cliente. Quando um engenheiro exige acesso adicional para dar suporte ao serviço do Microsoft 365, eles solicitam acesso temporário elevado aos recursos necessários usando uma ferramenta de gerenciamento de acesso chamada Lockbox. O lockbox restringe o acesso elevado aos privilégios mínimos, recursos e tempo necessários para concluir a tarefa atribuída. Se um revistor autorizado aprovar a solicitação de acesso JIT, o engenheiro recebe uma conta temporária com apenas os privilégios necessários para concluir seu trabalho atribuído. Essa conta temporária requer autenticação multifa factor e é excluída automaticamente após o período aprovado expirar.

## <a name="how-does-microsoft-365-handle-remote-access-to-production-systems"></a>Como o Microsoft 365 lida com o acesso remoto a sistemas de produção?

Os componentes do sistema do Microsoft 365 são ativos em datacenters geograficamente separados das equipes de operações. O pessoal do datacenter não tem acesso lógico aos sistemas do Microsoft 365. Como resultado, a equipe de serviço do Microsoft 365 gerencia o ambiente por meio do acesso remoto. A equipe de serviço que exige acesso remoto para dar suporte ao Microsoft 365 só tem acesso remoto após a aprovação de um gerente autorizado. Todo o acesso remoto usa TLS compatível com FIPS 140-2 para conexões remotas seguras.

O Microsoft 365 usa Estações de Trabalho de Administrador Seguro (SAWs) para o acesso remoto da equipe de serviço para ajudar a proteger os ambientes do Microsoft 365 contra comprometimento. Essas estações de trabalho foram projetadas especificamente para evitar perda intencional ou não intencional de dados de produção, incluindo o bloqueio de portas USB e a limitação do software disponível no SAW para o que é necessário para dar suporte ao ambiente. Os SAWs são acompanhados e monitorados de perto para detectar e impedir o comprometimento mal-intencionado ou inadvertido dos dados do cliente pelos engenheiros da Microsoft.

## <a name="how-does-customer-lockbox-add-additional-protection-for-customer-content"></a>Como o Customer Lockbox adiciona proteção ao conteúdo do cliente?

Os clientes podem adicionar um nível adicional de controle de acesso ao conteúdo habilitando o Customer Lockbox. Quando uma solicitação de elevação de lockbox envolve acesso ao conteúdo do cliente, o Customer Lockbox exige aprovação do cliente como uma etapa final no fluxo de trabalho de aprovação. Isso oferece às organizações a opção de aprovar ou negar essas solicitações e fornece controle de acesso direto ao cliente. Se o cliente rejeitar uma solicitação de Caixa de Bloqueio do Cliente, o acesso ao conteúdo solicitado será negado. Se o cliente não rejeitar ou aprovar a solicitação dentro de um determinado período, a solicitação expirará automaticamente sem que a Microsoft obtenha acesso ao conteúdo do cliente. Se o cliente aprovar a solicitação, o acesso temporário da Microsoft ao conteúdo do cliente será registrado, auditável e revogado automaticamente após o tempo atribuído para concluir a operação de solução de problemas expirar.

## <a name="related-external-regulations--certifications"></a>Regulamentações externas relacionadas & certificações

Os serviços online da Microsoft são regularmente auditados para conformidade com regulamentações e certificações externas. Consulte a tabela a seguir para validação de controles relacionados ao controle de identidade e acesso.

| **Auditorias externas** | **Section** | **Data do relatório mais recente** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | AC-2: Gerenciamento de contas <br> AC-3: Imposição de acesso <br> AC-5: separação de funções <br> AC-6: Privilégio mínimo <br> AC-17: Acesso remoto | 24 de setembro de 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Instrução of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.9.1: Requisitos de negócios do controle de acesso <br> A.9.2: Gerenciamento de acesso do usuário <br> A.9.3: responsabilidades do usuário <br> A.9.4: Controle de acesso de sistema e aplicativo <br> A.15.1: Segurança de informações nas relações de fornecedores | 22 de fevereiro de 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Instrução of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.9.2: Gerenciamento de acesso do usuário <br> A.9.4: Controle de acesso de sistema e aplicativo <br> A.15.1: Segurança de informações nas relações de fornecedores | 22 de fevereiro de 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-33: Modificação da conta <br> CA-34: Autenticação do usuário <br> CA-35: Acesso privilegiado <br> CA-36: Acesso remoto <br> CA-57: Aprovação de gerenciamento do Microsoft Customer Lockbox <br> CA-58: Solicitações de serviço de Caixa de Bloqueio do Cliente <br> CA-59: Notificações de Caixa de Bloqueio do Cliente <br> CA-61: revisão e aprovação do JIT | 24 de dezembro de 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-32: Política de conta compartilhada <br> CA-33: Modificação da conta <br> CA-34: Autenticação do usuário <br> CA-35: Acesso privilegiado <br> CA-36: Acesso remoto <br> CA-53: Monitoramento de terceiros <br> CA-56: Aprovação do cliente do Customer Lockbox <br> CA-57: Aprovação de gerenciamento do Microsoft Customer Lockbox <br> CA-58: Solicitações de serviço de Caixa de Bloqueio do Cliente <br> CA-59: Notificações de Caixa de Bloqueio do Cliente <br> CA-61: revisão e aprovação do JIT | 24 de dezembro de 2020 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-15: Solicitações de Cofre do Cliente | 24 de dezembro de 2020 |