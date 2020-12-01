---
title: Visão geral da arquitetura
description: Saiba mais sobre arquitetura no Microsoft 365
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
ms.openlocfilehash: 7ceceb59d0afcbc72fac9758f3de500082b8b365
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/30/2020
ms.locfileid: "49505841"
---
# <a name="architecture-overview"></a>Visão geral da arquitetura

## <a name="what-is-microsoft-365"></a>O que é o Microsoft 365?

O Microsoft 365 é a versão com base em nuvem, baseada em assinatura do Office, Windows 10, Enterprise Mobility + Security e conformidade. Os clientes do Microsoft 365 têm clientes como o Outlook e o Windows e também se beneficiam dos serviços que a Microsoft hospeda em seu nome, como o Exchange Online, o Microsoft Teams e o SharePoint Online. Todos os componentes do serviço são atualizados regularmente como parte do modelo de assinatura, para que nossos clientes tenham um produto "verde". A Microsoft gerencia a infraestrutura de serviço em nome dos clientes, o que significa que a Microsoft é responsável por proteger a infraestrutura que armazena os dados do cliente.

Em termos de escala, usamos atualmente mais de um milhão de computadores para alimentar os serviços do Microsoft 365. A infraestrutura que força esses serviços varia muito além de hardware e ambientes virtualizados específicos de serviço no Azure, Windows e Linux, e plataformas de vários locatários e dedicados. A Microsoft 365 é uma empresa global, e nossa infraestrutura é distribuída nos datacenters em todo o mundo, permitindo que nossos clientes atendam aos requisitos de residência de dados e da soberania nacional.

Em suma, o serviço é complexo, é executado em escala incrível e exige milhares de engenheiros da Microsoft para criar e manter. É nossa principal prioridade para nós manter toda essa infraestrutura segura.

## <a name="how-does-microsoft-365-ensure-isolation-between-customer-tenants"></a>Como a Microsoft 365 garante o isolamento entre os locatários do cliente?

Os serviços de nuvem da Microsoft são criados na pressuposição de que todos os locatários são potencialmente hostis para todos os outros locatários. Para isolar adequadamente os locatários uns dos outros, a Microsoft implementa uma variedade de tecnologias e controles de isolamento. Esses controles foram projetados para proteger contra vazamento de informações ou acesso não autorizado a dados do cliente em locatários e para impedir que as ações de um locatário afetem negativamente o serviço para outro locatário.

O conteúdo do cliente é logicamente isolado nos locatários do Microsoft 365 usando o Azure Active Directory (Azure AD). A autenticação do usuário no Microsoft 365 verifica não apenas a identidade do usuário, mas também a identidade do locatário para a qual a conta de usuário faz parte, impedindo que os usuários acessem os dados fora do ambiente do locatário. Para complementar o isolamento lógico do Azure AD, o conteúdo do cliente é sempre criptografado em repouso e em trânsito. Os serviços individuais também podem fornecer camadas adicionais de isolamento de locatário, como isolamento do SharePoint Online de dados do locatário em bancos de dados criptografados e separados.

## <a name="how-does-microsoft-365-engineer-resilient-services-that-avoid-single-points-of-failure"></a>Como o engenheiro da Microsoft 365 oferece serviços resistentes que evitam pontos únicos de falha?

A Microsoft cria e cria serviços em nuvem para maximizar a confiabilidade e minimizar os efeitos negativos sobre os clientes diante de falhas e desafios para operações normais. Essa estratégia começa com o design da rede que conecta nossos datacenters geograficamente distribuídos. A arquitetura de rede da Microsoft inclui interconexões diretas e vários caminhos de rede. Os serviços do Microsoft 365 aproveitam essa redundância para rotear automaticamente o tráfego em torno de falhas para melhorar a qualidade do serviço.

No nível de serviço, a estratégia de resiliência do Microsoft 365 prioriza a resiliência de software. Sempre que possível, nossos serviços são implantados em configurações ativas/ativas com o monitoramento automatizado da integridade do serviço, permitindo que o serviço detecte e recupere várias falhas e falhas comuns sem intervenção humana. Além das configurações ativas/ativas, os serviços do Microsoft 365 aumentam a tolerância a falhas garantindo que o serviço seja implantado em zonas de falha separadas, evitando que uma falha em uma zona afete a disponibilidade de outras zonas.

A resiliência de dados complementa a resiliência de serviço protegendo a integridade e a disponibilidade de dados nos serviços do Microsoft 365. Nossos serviços usam redundância de armazenamento local e redundância geográfica para replicar cópias de dados de clientes em diferentes zonas de falha. Se os dados estiverem corrompidos ou perdidos em uma zona de falha, poderão ser acessados em outra zona de falha sem perda de disponibilidade. A verificação de integridade automatizada restaura automaticamente os dados afetados por vários tipos de danos físicos ou lógicos. O Microsoft 365 também fornece aos clientes ferramentas para restaurar dados acidentalmente excluídos ou modificados pelo cliente no Exchange Online e no SharePoint Online.

## <a name="how-does-microsoft-365-track-dependencies-and-prevent-unauthorized-external-system-connections"></a>Como a Microsoft 365 controla as dependências e impede conexões de sistema externo não autorizadas?

O Microsoft 365 Service Teams identifica os componentes críticos do sistema e suas dependências como parte do gerenciamento de continuidade de negócios. Além disso, o Microsoft 365 documenta e rastreia todas as conexões do sistema externo para garantir que apenas as conexões autorizadas sejam permitidas nas configurações de firewall de rede. Os sistemas, as dependências e as conexões externas do Microsoft 365 estão documentados na arquitetura de segurança de informações do Microsoft 365. A arquitetura de segurança de informações e os diagramas de fluxo de dados correspondentes são revisados e atualizados anualmente no mínimo, bem como sempre que são feitas alterações significativas no sistema.

A arquitetura do Microsoft 365 é validada regularmente e automaticamente usando ferramentas baseadas em nuvem para verificar o alinhamento com nossos princípios de segurança e testar continuamente os recursos de isolamento e resiliência. A validação de arquitetura funciona para identificar automaticamente as instâncias nas quais o estado atual do serviço foi desatualizado do estado desejado, sinalizando qualquer desvio para revisão e atenuação. O objetivo da validação da arquitetura é garantir que os recursos de segurança da nossa infra-estrutura de serviço continuem funcionando conforme o esperado.

## <a name="related-external-regulations--certifications"></a>Normas externas relacionadas & certificações

Os serviços online da Microsoft são auditados regularmente para fins de conformidade com regulamentos externos e certificações. Consulte a tabela a seguir para validação de controles relacionados à arquitetura do Microsoft 365.

| **Auditorias externas** | **Section** | **Data do relatório mais recente** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | AC-4: imposição de fluxo de informações <br> CP-9: backup do sistema de informações <br> PL-8: arquitetura de segurança de informações <br> SC-7: proteção de limite <br> SC-22: arquitetura e provisionamento | 24 de setembro de 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaração de aplicabilidade](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 6: organização da segurança de informações <br> A. 13.1: gerenciamento de segurança de rede <br> A. 17.2: redundâncias | 22 de fevereiro de 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaração de aplicabilidade](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 6: organização da segurança de informações <br> A. 13.1: gerenciamento de segurança de rede | 22 de fevereiro de 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | AC-37: isolamento de locatário <br> AC-49: políticas de backup <br> AC-51: replicação de dados | 30 de setembro de 2019 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-05: diagramas de fluxo de dados <br> AC-37: isolamento de locatário <br> AC-49: políticas de backup <br> AC-51: replicação de dados | 30 de setembro de 2019 |