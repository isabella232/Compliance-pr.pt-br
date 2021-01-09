---
title: Visão geral da arquitetura
description: Saiba mais sobre a arquitetura no Microsoft 365
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
ms.openlocfilehash: e1b4e9701e76c1e758f683750c8ebfeda2bc1f1f
ms.sourcegitcommit: 7a5b6bc58fc4613b38f3fda20aebee5cec6a5730
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "49787480"
---
# <a name="architecture-overview"></a>Visão geral da arquitetura

## <a name="what-is-microsoft-365"></a>O que é o Microsoft 365?

O Microsoft 365 é a versão baseada em assinatura baseada em nuvem do Office, Windows 10, Enterprise Mobility + Security e Conformidade. Os clientes do Microsoft 365 recebem clientes, como o Outlook e o Windows, e também se beneficiam dos serviços que a Microsoft hospeda em seu nome, como o Exchange Online, o Microsoft Teams e o SharePoint Online. Todos os componentes do serviço são atualizados regularmente como parte do modelo de assinatura, para que nossos clientes tenham um produto "evergreen". A Microsoft gerencia a infraestrutura de serviço em nome dos clientes, o que significa que a Microsoft é responsável por proteger a infraestrutura que armazena os dados do cliente.

Em termos de escala, atualmente usamos quase um milhão de máquinas para a energia dos serviços do Microsoft 365. A infraestrutura de energia desses serviços varia amplamente entre hardware específico do serviço e ambientes virtualizados no Azure, Windows e Linux, e plataformas dedicadas e multi-locatários. O Microsoft 365 é uma empresa global, e nossa infraestrutura é distribuída em datacenters em todo o mundo, permitindo que nossos clientes atendem aos requisitos de residência e soberania de dados.

Em resumo, o serviço é complexo, é executado em escala incrível e exige milhares de engenheiros da Microsoft para criar e manter. É nossa principal prioridade manter toda essa infraestrutura segura.

## <a name="how-does-microsoft-365-ensure-isolation-between-customer-tenants"></a>Como o Microsoft 365 garante o isolamento entre locatários do cliente?

Os serviços de nuvem da Microsoft são construídos com a suposição de que todos os locatários são potencialmente ofensivos a todos os outros locatários. Para isolar corretamente os locatários um do outro, a Microsoft implementa uma variedade de tecnologias e controles de isolamento. Esses controles foram projetados para proteger contra vazamento de informações ou acesso não autorizado a dados do cliente entre locatários e para impedir que as ações de um locatário afetem negativamente o serviço para outro locatário.

O conteúdo do cliente é logicamente isolado nos locatários do Microsoft 365 usando o Azure Active Directory (Azure AD). A autenticação do usuário no Microsoft 365 verifica não apenas a identidade do usuário, mas também a identidade do locatário da conta do usuário, impedindo que os usuários acessem dados fora de seu ambiente de locatário. Para complementar o isolamento lógico do Azure AD, o conteúdo do cliente é sempre criptografado em repouso e em trânsito. Os serviços individuais também podem fornecer camadas adicionais de isolamento de locatário, como o isolamento do SharePoint Online de dados de locatários em bancos de dados criptografados separados.

## <a name="how-does-microsoft-365-engineer-resilient-services-that-avoid-single-points-of-failure"></a>Como o Microsoft 365 faz engenharia de serviços resilientes que evitam pontos de falha individuais?

A Microsoft projeta e cria serviços de nuvem para maximizar a confiabilidade e minimizar os efeitos negativos sobre os clientes diante de falhas e desafios para operações normais. Essa estratégia começa com o design da rede que conecta nossos datacenters geograficamente distribuídos. A arquitetura de rede da Microsoft inclui interconexões diretas e vários caminhos de rede. Os serviços do Microsoft 365 aproveitam essa redundância para rotear automaticamente o tráfego em torno de falhas para melhorar a qualidade do serviço.

No nível de serviço, a estratégia de resiliência do Microsoft 365 prioriza a resiliência de software. Sempre que possível, nossos serviços são implantados em configurações ativas/ativas com monitoramento automatizado de saúde do serviço, permitindo que o serviço detecte e se recupere de muitas falhas e falhas comuns sem intervenção humana. Além das configurações ativas/ativas, os serviços do Microsoft 365 aumentam a tolerância a falhas garantindo que o serviço seja implantado em zonas de falha separadas, impedindo que uma falha em uma zona afete a disponibilidade de outras zonas.

A resiliência de dados complementa a resiliência do serviço, protegendo a integridade e a disponibilidade de dados nos serviços do Microsoft 365. Nossos serviços usam redundância de armazenamento local e redundância geográfica para replicar cópias dos dados do cliente para diferentes zonas de falha. Se os dados estão corrompidos ou perdidos em uma zona de falha, eles podem ser acessados em outra zona de falha sem perda de disponibilidade. A verificação de integridade automatizada restaura automaticamente os dados afetados por vários tipos de danos físicos ou lógicos. O Microsoft 365 também fornece aos clientes ferramentas para restaurar dados excluídos ou modificados acidentalmente pelo cliente no Exchange Online e no SharePoint Online.

## <a name="how-does-microsoft-365-track-dependencies-and-prevent-unauthorized-external-system-connections"></a>Como o Microsoft 365 rastreia dependências e impede conexões não autorizadas do sistema externo?

As equipes de serviço do Microsoft 365 identificam componentes críticos do sistema e suas dependências como parte do Gerenciamento de Continuidade de Negócios. Além disso, o Microsoft 365 documenta e rastreia todas as conexões do sistema externo para garantir que somente conexões autorizadas sejam permitidas em configurações de firewall de rede. Os sistemas, dependências e conexões externas do Microsoft 365 estão documentados na arquitetura de segurança de informações do Microsoft 365. A arquitetura de segurança da informação e os diagramas de fluxo de dados correspondentes são revisados e atualizados anualmente no mínimo, bem como sempre que alterações significativas são feitas no sistema.

A arquitetura do Microsoft 365 é validada regularmente e automaticamente usando ferramentas baseadas em nuvem para verificar o alinhamento com nossos princípios de segurança e testar continuamente os recursos de isolamento e resiliência. A validação arquitetônica funciona para identificar automaticamente instâncias em que o estado atual do serviço se desviou do estado desejado, sinalizando todos os desvios para revisão e mitigação. O objetivo da validação da arquitetura é garantir que os recursos de segurança de nossa infraestrutura de serviço continuem a funcionar conforme o esperado.

## <a name="related-external-regulations--certifications"></a>Regulamentações externas relacionadas & certificações

Os serviços online da Microsoft são auditados regularmente para conformidade com regulamentações e certificações externas. Consulte a tabela a seguir para validação de controles relacionados à arquitetura do Microsoft 365.

| **Auditorias externas** | **Section** | **Data do relatório mais recente** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | AC-4: Imposição do fluxo de informações <br> CP-9: backup do sistema de informações <br> PL-8: Arquitetura de segurança de informações <br> SC-7: Proteção de limite <br> SC-22: Arquitetura e provisionamento | 24 de setembro de 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaração de Aplicabilidade](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.6: Organização da segurança das informações <br> A.13.1: Gerenciamento de segurança de rede <br> A.17.2: Redundâncias | 22 de fevereiro de 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaração de Aplicabilidade](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.6: Organização da segurança das informações <br> A.13.1: Gerenciamento de segurança de rede | 22 de fevereiro de 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-37: Isolamento de locatário <br> CA-49: Políticas de backup <br> CA-51: Replicação de dados | 24 de dezembro de 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-05: Diagramas de fluxo de dados <br> CA-37: Isolamento de locatário <br> CA-49: Políticas de backup <br> CA-51: Replicação de dados | 24 de dezembro de 2020 |