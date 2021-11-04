---
title: Visão geral da arquitetura
description: Saiba mais sobre arquitetura Microsoft 365
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
ms.openlocfilehash: 86c49d78deee975b0f7a1504938d81b0dc609cdf
ms.sourcegitcommit: 444a58b28f8611323e16d28b4c63a0f68eaaafa6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2021
ms.locfileid: "60780107"
---
# <a name="architecture-overview"></a>Visão geral da arquitetura

## <a name="what-are-microsoft-online-services"></a>O que são serviços online da Microsoft?

Os serviços online da Microsoft referem-se aos serviços baseados em nuvem oferecidos pela Microsoft, que inclui o Azure, o Dynamics 365 e o Microsoft 365.  Cada serviço oferece soluções exclusivas para as necessidades comuns de negócios e produtividade, atendendo clientes em todo o mundo, desde pequenas empresas a grandes empresas e governos. Datacenters distribuídos globalmente conectados pela infraestrutura de rede gerenciada independentemente da Microsoft atuam como o backbone para oferecer suporte a serviços online, fornecendo a capacidade de manter a disponibilidade em quase todas as situações e dimensionar para uma demanda mundial em massa.

Todos os serviços online da Microsoft têm o mesmo objetivo de proteger a infraestrutura de serviço que gerenciam e os dados de seus clientes, mas cada serviço online é operado por uma unidade de negócios separada. Em muitos casos, os controles de segurança são implementados da mesma maneira em todos os serviços, mas, em alguns casos, eles têm uma abordagem diferente para cumprir suas promessas de cliente e obrigações de conformidade.

## <a name="what-is-azure"></a>O que é o Azure?

Microsoft Azure é uma plataforma de computação em nuvem para criar, implantar e gerenciar aplicativos por meio de uma rede global da Microsoft e de datacenters gerenciados de terceiros. Ele dá suporte a modelos de serviço de nuvem (Platform as a Service) e Infrastructure as a Service (IaaS) e habilita soluções híbridas que integram serviços de nuvem aos recursos locais dos clientes. Microsoft Azure dá suporte a muitos clientes, parceiros e organizações governamentais que abrangem uma ampla variedade de produtos e serviços, geografias e setores. Microsoft Azure foi projetado para atender aos requisitos de segurança, confidencialidade e conformidade.

## <a name="what-is-dynamics-365"></a>O que é o Dynamics 365?

O Dynamics 365 é um pacote de aplicativos corporativos online que integra os recursos de Gerenciamento de Relacionamento com o Cliente (CRM) e suas extensões com os recursos do ERP (Planejamento de Recursos do Enterprise). Esses aplicativos de negócios de ponta a ponta ajudam os clientes a transformar relacionamentos em receita, a ganhar clientes e acelerar o crescimento dos negócios. O Dynamics 365 é um pacote Software as a Service (SaaS) criado com base na infraestrutura do Azure e disponibilizado para clientes em todo o mundo por meio de seus datacenters distribuídos globalmente.

## <a name="what-is-microsoft-365"></a>O que é o Microsoft 365?

Microsoft 365 é a versão baseada em assinatura baseada em nuvem do Office, Windows 10, Enterprise Mobility + Security e Conformidade. Microsoft 365 clientes recebem clientes como Outlook e Windows, e também se beneficiam dos serviços que a Microsoft hospeda em seu nome, como Exchange Online, Microsoft Teams e SharePoint Online. Todos os componentes do serviço são atualizados regularmente como parte do modelo de assinatura, para que nossos clientes tenham um produto "evergreen". A Microsoft gerencia a infraestrutura de serviço em nome dos clientes, o que significa que a Microsoft é responsável por proteger a infraestrutura que armazena dados do cliente.

Em termos de escala, a Microsoft usa atualmente cerca de um milhão de máquinas para Microsoft 365 serviços. A infraestrutura de energia desses serviços varia amplamente entre o hardware específico do serviço e ambientes virtualizados no Azure, Windows e Linux, além de plataformas dedicadas e de vários locatários. O Microsoft 365 é um negócio global e nossa infraestrutura é distribuída em datacenters em todo o mundo, permitindo que nossos clientes atendam aos requisitos de residência e soberania de dados.

## <a name="how-do-microsoft-online-services-ensure-isolation-between-customer-tenants"></a>Como os serviços online da Microsoft garantem o isolamento entre locatários do cliente?

Os serviços de nuvem da Microsoft são construídos com base na suposição de que todos os locatários são potencialmente hostil a todos os outros locatários. Para isolar corretamente os locatários um do outro, a Microsoft implementa várias tecnologias e controles de isolamento. Esses controles foram projetados para proteger contra vazamento de informações ou acesso não autorizado a dados do cliente entre locatários e para impedir que as ações de um locatário afetem adversamente o serviço para outro locatário.

O conteúdo do cliente é logicamente isolado em locatários usando Azure Active Directory (Azure AD). A autenticação do usuário nos serviços online da Microsoft verifica não apenas a identidade do usuário, mas também a identidade do locatário da quais a conta de usuário faz parte, impedindo que os usuários acessem dados fora de seu ambiente de locatário. Para complementar o isolamento lógico do Azure AD, o conteúdo do cliente é sempre criptografado em repouso e em trânsito. Os serviços individuais também podem fornecer camadas adicionais de isolamento de locatários, como SharePoint isolamento online de dados de locatários em bancos de dados criptografados separados.

## <a name="how-do-microsoft-online-services-engineer-resilient-services-that-avoid-single-points-of-failure"></a>Como os serviços online da Microsoft são engenheiros de serviços resilientes que evitam pontos de falha individuais?

A Microsoft projeta e cria serviços de nuvem para maximizar a confiabilidade e minimizar os efeitos negativos nos clientes em face de falhas e desafios para operações normais. Essa estratégia começa com o design da rede que conecta nossos datacenters geograficamente distribuídos. A arquitetura de rede da Microsoft inclui interconexões diretas e vários caminhos de rede. Os serviços online da Microsoft usam essa redundância para rotear automaticamente o tráfego em torno de falhas para melhorar a qualidade do serviço.

Sempre que possível, os serviços online da Microsoft são implantados em configurações ativas/ativas com monitoramento automatizado de saúde do serviço, permitindo que o serviço detecte e recupere de muitas falhas e falhas comuns sem intervenção humana. Além das configurações ativas/ativas, os serviços online da Microsoft aumentam a tolerância a falhas garantindo que o serviço seja implantado em zonas de falha separadas, impedindo que uma falha em uma zona afete a disponibilidade de outras zonas.

A resiliência de dados complementa a resiliência do serviço protegendo a integridade e a disponibilidade de dados nos serviços online da Microsoft. Nossos serviços usam redundância de armazenamento local e redundância geográfica para replicar cópias de dados do cliente em diferentes zonas de falha. Se os dados forem corrompidos ou perdidos em uma zona de falha, eles poderão ser acessados em outra zona de falha sem perda de disponibilidade. A verificação automatizada de integridade restaura automaticamente os dados afetados por vários tipos de corrupção física ou lógica. A Microsoft também fornece aos clientes ferramentas para restaurar dados excluídos acidentalmente ou modificados pelo cliente em serviços como Exchange Online e SharePoint Online.

## <a name="how-do-microsoft-online-services-track-dependencies-and-prevent-unauthorized-external-system-connections"></a>Como os serviços online da Microsoft rastreia dependências e impedem conexões de sistema externo não autorizadas?

As equipes de serviços online da Microsoft identificam componentes críticos do sistema e suas dependências como parte do Gerenciamento de Continuidade de Negócios. Além disso, a Microsoft documenta e rastreia todas as conexões do sistema externo para garantir que apenas conexões autorizadas sejam permitidas em configurações de firewall de rede. Os sistemas de serviços online da Microsoft, dependências e conexões externas são documentados na arquitetura de segurança de informações dos serviços online da Microsoft. A arquitetura de segurança da informação e os diagramas de fluxo de dados correspondentes são revisados e atualizados anualmente no mínimo, bem como sempre que alterações significativas são feitas no sistema.

A arquitetura de serviços online da Microsoft é validada regularmente e automaticamente usando ferramentas baseadas em nuvem para verificar o alinhamento com nossos princípios de segurança e testar continuamente os recursos de isolamento e resiliência. A validação de arquitetura funciona para identificar automaticamente instâncias onde o estado atual do serviço se desviou do estado desejado, sinalizando quaisquer desvios para revisão e mitigação. O objetivo da validação da arquitetura é garantir que os recursos de segurança de nossa infraestrutura de serviço continuem a funcionar conforme o esperado.

## <a name="related-external-regulations--certifications"></a>Regulamentações externas relacionadas & certificações

Os serviços online da Microsoft são regularmente auditados para conformidade com regulamentações e certificações externas. Consulte a tabela a seguir para validação de controles relacionados à arquitetura.

### <a name="azure-and-dynamics-365"></a>Azure e Dynamics 365

| **Auditorias externas** | **Section** | **Data do relatório mais recente** |
|:--------------------|:------------|:-----------------------|
| [ISO 27001/27002](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Instrução of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7af5304-3a31-40e6-9abb-e26352305d41&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.6: Organização da segurança da informação <br> A.13.1: Gerenciamento de segurança de rede <br> A.17.2: Redundâncias | 2 de dezembro de 2020 |
| [ISO 27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Instrução of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a3bca0ac-867d-4204-b66b-13665f5f1e8d&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=25718a8a-f34d-41e1-a95a-c49246508787&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.6: Organização da segurança da informação <br> A.13.1: Gerenciamento de segurança de rede <br> A.17.2: Redundâncias | 2 de dezembro de 2020 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b8721ebd-af20-42fe-b22f-8332b0a19517&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=234a0f57-83c1-4afc-a586-a0e7a59592f7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=75c8cbf6-e456-473c-a05e-34fea888ec2a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | BC-1: Planos de continuidade de negócios <br> BC-3: procedimentos BCDR <br> BC-4: teste de BCDR <br> BC-5: Avaliações de risco de continuidade de negócios <br> BC-6: continuidade de negócios de terceiros <br> BC-7: Procedimentos de continuidade de negócios do Datacenter <br> BC-8: Teste de continuidade de negócios do datacenter <br> BC-9: avaliação de resiliência do datacenter <br>  DS-6: Redundância de componentes críticos <br> DS-7: Replicação de dados do cliente <br> DS-14: Restauração de serviços ao cliente <br> DS-16: Segregação de dados do cliente | 31 de março de 2021 |

### <a name="office-365"></a>Office 365

| **Auditorias externas** | **Section** | **Data do relatório mais recente** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP](https://compliance.microsoft.com/compliancemanager) | AC-4: Imposição de fluxo de informações <br> CP-9: Backup do sistema de informações <br> PL-8: Arquitetura de segurança da informação <br> SC-7: Proteção de limite <br> SC-22: Arquitetura e provisionamento | 24 de setembro de 2020 |
| [ISO 27001/27002/27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=08ce227f-d1d9-4c4c-b255-4f2e4ec8f941&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Instrução of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.6: Organização da segurança da informação <br> A.13.1: Gerenciamento de segurança de rede <br> A.17.2: Redundâncias | Abril de 20, 2021 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-37: isolamento de locatário <br> CA-49: Políticas de backup <br> CA-51: Replicação de dados | 24 de dezembro de 2020 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-05: Diagramas de fluxo de dados <br> CA-37: isolamento de locatário <br> CA-49: Políticas de backup <br> CA-51: Replicação de dados | 24 de dezembro de 2020 |