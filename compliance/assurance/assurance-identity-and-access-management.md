---
title: Visão geral do gerenciamento de identidades e acesso
description: Saiba mais sobre o gerenciamento de acesso e identidade no Microsoft 365
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
ms.openlocfilehash: b62219faa5bc55ef4bef9557d953caf1a2f95fc7
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/30/2020
ms.locfileid: "49505671"
---
# <a name="identity-and-access-management-overview"></a>Visão geral do gerenciamento de identidades e acesso

## <a name="how-does-microsoft-365-protect-production-systems-from-unauthorized-or-malicious-access"></a>Como a Microsoft 365 protege os sistemas de produção contra acessos maliciosos ou não autorizados?

O Microsoft 365 foi projetado para permitir que os engenheiros da Microsoft operem o serviço sem acessar o conteúdo do cliente. Por padrão, os engenheiros da Microsoft 365 têm zero ZSA (acesso à pé) ao conteúdo do cliente e nenhum acesso privilegiado ao ambiente de produção. A Microsoft 365 usa um modelo de just-in-time (JIT), JEA (apenas para acesso) para fornecer aos engenheiros de equipe de serviço acessos com privilégios temporários a ambientes de produção quando esse acesso é necessário para dar suporte ao Microsoft 365. O modelo de acesso JIT substitui o acesso administrativo tradicional e persistente a um processo de engenheiros para solicitar a elevação temporária em funções privilegiadas quando necessário.

Engenheiros atribuídos a uma equipe de serviço para dar suporte à elegibilidade de solicitação de serviços de produção para uma conta de equipe de serviço por meio da ferramenta de gerenciamento de identidades (IDM). A solicitação de qualificação dispara uma série de verificações de pessoal para garantir que o engenheiro tenha passado por todos os requisitos de triagem de nuvem, conclusão do treinamento necessário e recebido a aprovação de gerenciamento apropriada antes da criação da conta. Somente após atender todos os requisitos de qualificação pode ser criada uma conta de equipe de serviço para o ambiente solicitado.

As contas de equipe de serviço não concedem nenhum privilégio de administrador ou acesso ao conteúdo do cliente. Quando um engenheiro requer acesso adicional para dar suporte ao serviço do Microsoft 365, ele solicita acesso elevado temporário aos recursos que eles exigem usando uma ferramenta de gerenciamento de acesso chamada lockbox. O Lockbox restringe o acesso elevado para os privilégios mínimos, os recursos e o tempo necessário para concluir a tarefa atribuída. Se um revisor autorizado aprovar a solicitação de acesso JIT, o engenheiro receberá uma conta temporária apenas com os privilégios necessários para concluir o trabalho atribuído. Essa conta temporária requer autenticação multifator e é automaticamente excluída após o período aprovado expirar.

## <a name="how-does-microsoft-365-handle-remote-access-to-production-systems"></a>Como a Microsoft 365 lida com o acesso remoto aos sistemas de produção?

Os componentes do sistema Microsoft 365 são hospedados em datacenters geograficamente separados das equipes de operações. O pessoal do datacenter não tem acesso lógico aos sistemas Microsoft 365. Como resultado, a equipe do Microsoft 365 Service Team gerencia o ambiente por meio de acesso remoto. O pessoal da equipe de serviço que precisa de acesso remoto para dar suporte ao Microsoft 365 só recebe acesso remoto após a aprovação de um gerente autorizado. Todo acesso remoto usa o TLS compatível com FIPS 140-2 para conexões remotas seguras.

A Microsoft 365 usa as estações de trabalho de administração (SAWs) seguras para acesso remoto da equipe de serviço para ajudar a proteger os ambientes do Microsoft 365 contra o comprometimento. Essas estações de trabalho foram especificamente projetadas para evitar a perda intencional ou involuntária de dados de produção, incluindo o bloqueio de portas USB e a limitação do software disponível no visto para o suporte ao ambiente. SAWs são rigorosamente rastreados e monitorados para detectar e impedir o comprometimento mal-intencionado ou inadvertido dos dados do cliente por engenheiros da Microsoft.

## <a name="how-does-customer-lockbox-add-additional-protection-for-customer-content"></a>Como a Lockbox do cliente adiciona proteção adicional ao conteúdo do cliente?

Os clientes podem adicionar um nível adicional de controle de acesso ao conteúdo habilitando o Lockbox do cliente. Quando uma solicitação de elevação de lockbox envolve o acesso ao conteúdo do cliente, a Lockbox do cliente requer a aprovação do cliente como uma etapa final no fluxo de trabalho de aprovação. Isso oferece às organizações a opção de aprovar ou negar essas solicitações e fornece controle de acesso direto ao cliente. Se o cliente rejeitar uma solicitação de lockbox do cliente, o acesso ao conteúdo solicitado será negado. Se o cliente não rejeitar ou aprovar a solicitação dentro de um determinado período, a solicitação expirará automaticamente sem que a Microsoft obtenha acesso ao conteúdo do cliente. Se o cliente aprovar a solicitação, o acesso temporário da Microsoft ao conteúdo do cliente será registrado, auditável e revogado automaticamente após o tempo atribuído para concluir a operação de solução de problemas expirar.

## <a name="related-external-regulations--certifications"></a>Normas externas relacionadas & certificações

Os serviços online da Microsoft são auditados regularmente para fins de conformidade com regulamentos externos e certificações. Consulte a tabela a seguir para validação de controles relacionados ao controle de acesso e identidades.

| **Auditorias externas** | **Section** | **Data do relatório mais recente** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | AC-2: gerenciamento de contas <br> AC-3: imposição de acesso <br> AC-5: separação de direitos <br> AC-6: privilégios mínimos <br> AC-17: acesso remoto | 24 de setembro de 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaração de aplicabilidade](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 9.1: requisitos de negócios do controle de acesso <br> A. 9.2: gerenciamento de acesso do usuário <br> A. 9,3: responsabilidades do usuário <br> A. 9.4: controle de acesso de sistema e aplicativo <br> A. 15.1: segurança de informações em relações de fornecedores | 22 de fevereiro de 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaração de aplicabilidade](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 9.2: gerenciamento de acesso do usuário <br> A. 9.4: controle de acesso de sistema e aplicativo <br> A. 15.1: segurança de informações em relações de fornecedores | 22 de fevereiro de 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | AC-33: modificação de conta <br> AC-34: autenticação de usuário <br> AC-35: acesso privilegiado <br> AC-36: acesso remoto <br> AC-57: aprovação de gerenciamento Microsoft de lockbox de cliente <br> AC-58: solicitações de serviço de lockbox do cliente <br> AC-59: notificações de lockbox do cliente <br> AC-61: revisão e aprovação do JIT | 30 de setembro de 2019 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | AC-32: política de conta compartilhada <br> AC-33: modificação de conta <br> AC-34: autenticação de usuário <br> AC-35: acesso privilegiado <br> AC-36: acesso remoto <br> AC-53: monitoramento de terceiros <br> CA-56: aprovação do cliente de lockbox do cliente <br> AC-57: aprovação de gerenciamento Microsoft de lockbox de cliente <br> AC-58: solicitações de serviço de lockbox do cliente <br> AC-59: notificações de lockbox do cliente <br> AC-61: revisão e aprovação do JIT | 30 de setembro de 2019 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=9df8b99b-96ce-49a9-bff4-268031dcc9a6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CUEC-15: solicitações de lockbox do cliente | 30 de setembro de 2019 |