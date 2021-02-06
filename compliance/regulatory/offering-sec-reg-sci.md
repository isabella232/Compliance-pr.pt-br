---
title: Comissão de Títulos e Câmbio - Conformidade e Integridade dos Sistemas de Regulamentação (SCI)
description: As regras SCI se aplicam a entidades SCI, que incluem tais organizações auto-regulamentadores (SROs) como trocas de ações e opções, agências de limpeza registradas e sistemas de negociação alternativos (ATSs).
keywords: Microsoft 365, conformidade, ofertas
localization_priority: None
ms.prod: microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmazz
manager: laurawi
audience: itpro
ms.collection:
- M365-security-compliance
- MS-Compliance
hideEdit: true
titleSuffix: Microsoft Compliance
ms.openlocfilehash: 049f0516598209411b0c5ca47eea39140762fd3d
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2021
ms.locfileid: "50119870"
---
# <a name="securities-and-exchange-commission-regulation-systems-compliance-and-integrity-sci"></a>Comissão de Títulos e Câmbio: Conformidade e Integridade dos Sistemas de Regulamentação (SCI)

## <a name="about-regulation-sci"></a>Sobre a regulamentação SCI

A SEC (Comissão de Títulos e Câmbio dos EUA) é uma agência independente do governo federal dos EUA e o supervisor principal e regulador de mercados de valores mobiliários dos EUA. Ele pede autoridade de aplicação sobre as leis federais de valores mobiliários, proponha novas regras de títulos e supervisiona a regulamentação de mercado do setor de valores mobiliários.

Em novembro de 2014, a SEC adotou a conformidade e integridade dos sistemas de regulamentação [(SCI) (e](https://www.sec.gov/rules/final/2014/34-73639.pdf) o formulário SCI para relatar eventos SCI) para reforçar a infraestrutura de tecnologia nos mercados de valores mobiliários dos EUA. A regulamentação foi projetada para reduzir a frequência de paralisações do sistema, melhorar a resiliência quando esses incidentes ocorrerem e aumentar a supervisão da SEC sobre a tecnologia do mercado de valores mobiliários e a imposição de seus regulamentos.

As regras SCI se aplicam a entidades SCI, que incluem tais organizações auto-regulamentadores (SROs) como trocas de ações e opções, agências de limpeza registradas e sistemas de negociação alternativos (ATSs). As regras regulam principalmente os sistemas que suportam diretamente as principais funções do mercado de valores mobiliários: negociação, autorização e liquidação, roteamento de ordem, dados de mercado, regulamentação de mercado e controle de mercado.

## <a name="microsoft-and-sec-regulation-sci"></a>Regulamentação da Microsoft e da SEC SCI

A SEC (Comissão de Títulos e Câmbio dos EUA) adotou a REGULAMENTAÇÃO SCI para reforçar a infraestrutura de tecnologia das organizações financeiras que operam e suportam os mercados de valores mobiliários dos EUA. Sob supervisão da SEC, seus requisitos foram projetados para garantir que esses sistemas tenham alta disponibilidade, alta resiliência e baixa latência (alto volume de mensagens com pouco atraso).

Para ajudar a orientar os clientes de serviços financeiros dos EUA que devem estar em conformidade com essa regulamentação, a Microsoft publicou o Guia de Implementação de Conformidade e Integridade dos Sistemas de Regulamentação da SEC do [Microsoft Azure.](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=a69ce0c1-7b7e-44e9-9143-867241e6b2f9&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers) As diretrizes neste documento:

- Fornece uma visão geral dos recursos gerais do Azure que suportam forte resiliência, alta disponibilidade e baixa latência.
- Deixa claro quais áreas de controle e aspectos regulatórios o Azure aborda. Esse mapeamento ponto a ponto de recursos e serviços do Azure para requisitos de SCI mede a conformidade do Azure com a estrutura regulatória. Ele também ajuda os clientes a entender onde eles podem mudar as responsabilidades de segurança para o Azure de que eles tinham totalmente de propriedade quando operavam no local. Esses recursos são respaldados pelas promessas que a Microsoft faz nos SLAs do Azure.
- Especifica cada requisito de REGULAMENTAÇÃO SCI que é responsabilidade do cliente abordar e oferece a documentação e os serviços do Azure para ajudá-lo a lidar com essas responsabilidades.

Este documento fornece uma lista de verificação completa das áreas críticas de foco do SCI de regulamentação. Esta lista de verificação ajuda as organizações financeiras a entender como elas podem adotar o Azure para ajudar a garantir aos reguladores, aos clientes e à liderança que podem atender aos requisitos regulatórios aplicáveis.

## <a name="microsoft-in-scope-cloud-services"></a>Serviços de nuvem no Escopo da Microsoft 

- [Azure](https://aka.ms/AzureCompliance)

## <a name="how-to-implement"></a>Como implementar

- [Guia de implementação do SCI de](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=a69ce0c1-7b7e-44e9-9143-867241e6b2f9&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)regulamentação: mapeia os recursos do Azure em relação à regulamentação e detalha a responsabilidade compartilhada pela conformidade.
- [Criação de aplicativos confiáveis do Azure:](/azure/architecture/resiliency/)uma breve visão geral de como criar confiabilidade em cada etapa do design de aplicativos do Azure.
- [Criação de aplicativos altamente disponíveis:](/azure/storage/common/storage-designing-ha-apps-with-ragrs)como os desenvolvedores podem ajudar a garantir que seus aplicativos de Armazenamento do Azure estão altamente disponíveis.
- [Guia de conformidade e avaliação de risco](https://aka.ms/RiskGovernanceGuide): cria um modelo de governança para a avaliação de risco dos serviços de nuvem da Microsoft e notificações do regulador.

## <a name="frequently-asked-questions"></a>Perguntas frequentes

**O que significa a responsabilidade compartilhada ao usar a tecnologia de nuvem?**

À medida que os ambientes de computação mudam de datacenters locais para aqueles na nuvem, a responsabilidade da segurança também muda — o provedor de serviços de nuvem (CSP) e o cliente agora compartilham essa responsabilidade. Para cada aplicativo e solução, quanto dessa responsabilidade se enquadra no cliente e quanto no CSP depende do modelo do Azure que um cliente implanta — IaaS, SaaS ou PaaS. É dever do cliente entender até que ponto eles são responsáveis pela implementação dos controles de segurança necessários. No entanto, a Microsoft fornece orientações para ajudar os clientes a navegar nessa dinâmica complexa. Para obter mais informações, leia [Shared Responsibilities for Cloud Computing](https://gallery.technet.microsoft.com/Shared-Responsibilities-81d0ff91).

**Quais instituições financeiras podem tirar proveito do Azure para ajudar a atender aos requisitos regulamentados do SCI?**

As organizações financeiras ou entidades SCI sujeitas a essa regulamentação podem implantar o Azure. A SEC diz que sua regulamentação se aplica a "organizações auto-regulamentares (SROs), incluindo cotações e opções, agências de limpeza registradas, FINRA e o MSRB, sistemas de negociação alternativos (ATSs), que negociam ações NMS e não NMS excedendo limites de volume especificados, disseminadores de dados de mercado consolidados (planos de processadores) e determinadas agências de limpeza isentas.'

## <a name="resources"></a>Recursos

- [Respostas da SEC a perguntas frequentes sobre a regulamentação SCI](https://www.sec.gov/divisions/marketreg/regulation-sci-faq.shtml)
- [Continuidade de negócios e recuperação de desastre (BCDR): Regiões emparelhadas do Azure](/azure/best-practices-availability-paired-regions)
- [Mapa de Conformidade dos Princípios Regulatórios de Computação em Nuvem e do Microsoft Online Services](https://aka.ms/FinServ-Guide-US)
- [Programa de conformidade para serviços financeiros do Microsoft Cloud](https://aka.ms/FSCP-Print)
- [Conformidade de serviços financeiros no Azure](https://aka.ms/FinServ-Compliance-Azure)
- [Serviços Financeiros da Microsoft](https://aka.ms/FinServ-Compliance)
- [Regra 17a-4 da Microsoft e da SEC](offering-SEC-17a-4.md)
- [Conformidade na Central de Confiabilidade da Microsoft](https://www.microsoft.com/trust-center/compliance/compliance-overview)
