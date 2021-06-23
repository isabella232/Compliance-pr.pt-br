---
title: Securities and Exchange Commission - Regulation Systems Compliance and Integrity (SCI)
description: As regras SCI se aplicam a entidades SCI, que incluem organizações auto-regulamentadas (SROs) como bolsas de ações e opções, agências de limpeza registradas e sistemas de negociação alternativos (ATSs).
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
ms.openlocfilehash: 06537749b60f40ab87211aa6efa65e8e88ed691b
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/23/2021
ms.locfileid: "53087530"
---
# <a name="securities-and-exchange-commission-regulation-systems-compliance-and-integrity-sci"></a>Securities and Exchange Commission: Regulation Systems Compliance and Integrity (SCI)

## <a name="about-regulation-sci"></a>Sobre a regulamentação SCI

A Comissão de Títulos e Exchange dos EUA (SEC) é uma agência independente do governo federal dos EUA e o supervisor principal e regulador dos mercados de valores mobiliários dos EUA. Ele exerce autoridade de aplicação sobre leis de valores mobiliários federais, propõe novas regras de valores mobiliários e supervisiona a regulamentação de mercado do setor de valores mobiliários.

Em novembro de 2014, a SEC adotou o [SCI (Regulation Systems Compliance and Integrity)](https://www.sec.gov/rules/final/2014/34-73639.pdf) (e o Form SCI para relatar eventos SCI) para reforçar a infraestrutura de tecnologia nos mercados de valores mobiliários dos EUA. A regulamentação foi projetada para reduzir a frequência de paralisações do sistema, melhorar a resiliência quando esses incidentes ocorrem e aumentar a supervisão da SEC da tecnologia do mercado de valores mobiliários e a aplicação de suas regulamentações.

As regras SCI se aplicam a entidades SCI, que incluem organizações auto-regulamentadas (SROs) como bolsas de ações e opções, agências de limpeza registradas e sistemas de negociação alternativos (ATSs). As regras regulam principalmente os sistemas que suportam diretamente as principais funções do mercado de valores mobiliários: negociação, liberação e liquidação, roteamento de ordem, dados de mercado, regulamentação de mercado e monitoramento de mercado.

## <a name="microsoft-and-sec-regulation-sci"></a>Microsoft e SEC Regulation SCI

A Comissão de Valores Mobiliários e Exchange dos EUA (SEC) adotou o REGULAMENTO SCI para fortalecer a infraestrutura de tecnologia das organizações financeiras que operam e suportam os mercados de valores mobiliários dos EUA. Em supervisão da SEC, seus requisitos são projetados para garantir que esses sistemas tenham alta disponibilidade, resiliência forte e baixa latência (alto volume de mensagens com pouco atraso).

Para ajudar a orientar os clientes de serviços financeiros dos EUA que devem estar em conformidade com essa regulamentação, a Microsoft publicou o Guia de Conformidade e Implementação de Sistemas de Regulamentação Microsoft Azure [SEC.](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=a69ce0c1-7b7e-44e9-9143-867241e6b2f9&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers) As diretrizes neste documento:

- Fornece uma visão geral dos recursos gerais do Azure que suportam forte resiliência, alta disponibilidade e baixa latência.
- Deixa claro quais áreas de controle e aspectos regulatórios o Azure aborda. Esse mapeamento ponto a ponto dos recursos e serviços do Azure para requisitos SCI mede a conformidade do Azure em relação à estrutura regulatória. Ele também ajuda os clientes a entender onde eles podem mudar as responsabilidades de segurança para o Azure de que eles tinham propriedade total quando operaram no local. Esses recursos são respaldados pelas promessas que a Microsoft faz no Azure SLAs.
- Especifica cada requisito SCI de regulamentação que é responsabilidade do cliente resolver e oferece documentação e serviços do Azure para ajudá-los a lidar com essas responsabilidades.

Este documento fornece uma lista de verificação completa das áreas críticas de foco SCI de regulamentação. Essa lista de verificação ajuda as organizações financeiras a entender como podem adotar o Azure para ajudar a garantir aos seus reguladores, clientes e liderança que eles possam estar em conformidade com os requisitos regulatórios aplicáveis.

## <a name="microsoft-in-scope-cloud-services"></a>Serviços de nuvem no escopo da Microsoft

- [Azure](https://aka.ms/AzureCompliance)

## <a name="how-to-implement"></a>Como implementar

- [Guia de Implementação SCI](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=a69ce0c1-7b7e-44e9-9143-867241e6b2f9&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)de regulamentação : Mapas recursos do Azure em relação à regulamentação e detalha a responsabilidade compartilhada pela conformidade.
- [Projetando aplicativos confiáveis do Azure:](/azure/architecture/resiliency/)uma breve visão geral de como criar confiabilidade em cada etapa do design do aplicativo do Azure.
- [Projetando aplicativos altamente disponíveis:](/azure/storage/common/storage-designing-ha-apps-with-ragrs)como os desenvolvedores podem ajudar a garantir que seus aplicativos Armazenamento do Azure estão altamente disponíveis.
- [Guia de conformidade e avaliação de risco](https://aka.ms/RiskGovernanceGuide): cria um modelo de governança para a avaliação de risco dos serviços de nuvem da Microsoft e notificações do regulador.

## <a name="frequently-asked-questions"></a>Perguntas frequentes

**O que significa a responsabilidade compartilhada ao usar a tecnologia de nuvem?**

À medida que os ambientes de computação se movem de datacenters locais para aqueles na nuvem, a responsabilidade da segurança também muda — o provedor de serviços de nuvem (CSP) e o cliente agora compartilham essa responsabilidade. Para cada aplicativo e solução, quanto dessa responsabilidade recai sobre o cliente e quanto no CSP depende do modelo do Azure que um cliente implanta— IaaS, SaaS ou PaaS. É dever do cliente entender até que ponto eles são responsáveis pela implementação dos controles de segurança necessários. No entanto, a Microsoft fornece orientações para ajudar os clientes a navegar por essa dinâmica complexa. Para obter mais informações, leia [Shared Responsibilities for Cloud Computing](https://gallery.technet.microsoft.com/Shared-Responsibilities-81d0ff91).

**Quais instituições financeiras podem tirar proveito do Azure para ajudar a atender aos requisitos sci de regulamentação?**

Organizações financeiras ou entidades SCI sujeitas a essa regulamentação podem implantar o Azure. A SEC diz que sua regulamentação se aplica a "organizações auto-regulamentares (SROs), incluindo bolsas de ações e opções, agências de compensação registradas, FINRA e o MSRB, sistemas de negociação alternativos (ATSs), que negociam ações NMS e não-NMS excedendo limites de volume especificados, disseminadores de dados de mercado consolidados (plano de processadores) e determinadas agências de compensação isentas.

## <a name="resources"></a>Recursos

- [Respostas da SEC a perguntas frequentes sobre a regulamentação SCI](https://www.sec.gov/divisions/marketreg/regulation-sci-faq.shtml)
- [Continuidade de negócios e recuperação de desastres (BCDR): Regiões emparelhadas do Azure](/azure/best-practices-availability-paired-regions)
- [Mapa de conformidade dos princípios regulatórios de computação em nuvem e Microsoft Online Services](https://aka.ms/FinServ-Guide-US)
- [Programa de conformidade para serviços financeiros do Microsoft Cloud](https://aka.ms/FSCP-Print)
- [Conformidade de serviços financeiros no Azure](https://aka.ms/FinServ-Compliance-Azure)
- [Microsoft Financial Services](https://aka.ms/FinServ-Compliance)
- [Regra 17a-4 da Microsoft e SEC](offering-SEC-17a-4.md)
- [Conformidade na Central de Confiabilidade da Microsoft](https://www.microsoft.com/trust-center/compliance/compliance-overview)
