---
title: US DoE 10 CFR Part 810
description: Os clientes sujeitos aos requisitos de controle de exportação do US DoE 10 CFR Part 810 podem usar o Azure Government.
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
ms.openlocfilehash: 1a16495f5cfe3e293910ebe84e6af566aea17621
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/23/2021
ms.locfileid: "53087540"
---
# <a name="us-doe-10-cfr-part-810"></a>US DoE 10 CFR Part 810

## <a name="microsoft-and-doe-10-cfr-part-810"></a>Microsoft e DoE 10 CFR Part 810

Microsoft Azure O governo pode ajudar a dar suporte aos clientes sujeitos aos requisitos de controle de exportação do Departamento de Energia dos EUA (DoE) 10 CFR Parte 810 por meio de duas autorizações:

- A Alta Autorização Provisória fedRAMP para operar (P-ATO) emitida pela Junta de Autorização (JAB)
- As Autorizações Provisórias de Nível 4 e 5 da Agência de Sistemas de Informações de Defesa do Departamento de Defesa (DoD)

A FedRAMP oferece uma linha de base apropriada para fornecer garantias de que o Azure Government fornece tecnologias e serviços básicos de infraestrutura e virtualização, como computação, armazenamento e rede projetados com controles NIST rigorosos. Eles ajudam a atender aos requisitos de separação de dados do cliente e ajudam a habilitar conexões seguras aos ambientes locais dos clientes.

Além disso, o Azure Government é uma nuvem da comunidade governamental dos EUA que está fisicamente separada da nuvem do Azure. Ele fornece garantias adicionais em relação a requisitos específicos de triagem em segundo plano pelo governo dos EUA, incluindo controles específicos que restringem o acesso a informações e sistemas a cidadãos dos EUA na tela entre o pessoal de operações do Azure.

## <a name="microsoft-in-scope-cloud-services"></a>Serviços de nuvem no escopo da Microsoft

- [Governo do Azure](https://aka.ms/AzureCompliance)
- Intune

## <a name="how-to-implement"></a>Como implementar

- [NeRC CIP Standards & Cloud Computing](https://aka.ms/AzureNERC): Diretrizes para utilitários elétricos e Entidades Registradas implantando cargas de trabalho no Azure ou no Azure Government.

## <a name="about-doe-10-cfr-part-810"></a>Sobre o DoE 10 CFR Part 810

A regulamentação de controle de exportação do Departamento de Energia dos EUA (DoE) [10 CFR Parte 810](https://www.govinfo.gov/content/pkg/FR-2015-02-23/pdf/2015-03479.pdf) rege a exportação de tecnologia e assistência não classificadas para o sistema. Isso ajuda a garantir que as tecnologias atômicas exportadas dos Estados Unidos sejam usadas apenas para fins pacíficos. A Parte 810 revisada (Regra Final) entrou em vigor em março de 2015 e é administrada pela Administração Nacional de [Segurança Atômica](https://www.energy.gov/nnsa/national-nuclear-security-administration). A Seção 810.6 afirma que a autorização específica do DoE é necessária para as disposições de assistência e transferências de tecnologias digitais confidenciais que são "geralmente autorizadas", bem como aquelas que exigem autorização específica (como para assistência envolvendo tecnologias digitais confidenciais, como enriquecimento e produção de água pesada).

## <a name="frequently-asked-questions"></a>Perguntas frequentes

**Os 10 regulamentos da Parte 110 do CFR da Comissão Reguladora Atômica dos EUA se aplicam ao Governo do Azure?**

Não. A [Comissão Reguladora Atômica](https://www.nrc.gov/) dos EUA [](https://www.nrc.gov/about-nrc/ip/export-import.html) (NRC) regulamenta a exportação e importação de instalações atômicas e equipamentos e materiais relacionados sob [10 CFR Parte 110](https://www.nrc.gov/reading-rm/doc-collections/cfr/part110/). A NRC não regula a tecnologia e a assistência atômica relacionadas a esses itens que se enquadram na jurisdição do DoE. Portanto, os regulamentos da Parte 110 da CFR NRC 10 não se aplicariam ao Governo do Azure.

**Como posso fornecer evidências de que estou em conformidade com o DoE 10 CFR Part 810?**

Se sua organização estiver implantando dados no Azure Government, você poderá contar com o FedRAMP High P-ATO do Azure Government como evidência de que você está manipulando dados de maneira restrita adequadamente. No entanto, você é responsável por obter autorização do DoE de seus próprios sistemas, incluindo o uso de serviços de nuvem.

**Quais são as minhas responsabilidades para classificar dados implantados no Azure Government?**

Os clientes que implantam dados no Azure Government são responsáveis por seu próprio processo de classificação de segurança. Para dados do cliente sujeitos a controles de exportação do DoE, o sistema de classificação é aumentado pelos controles UCNI (Informações Atômicas Controladas Não Classificados) estabelecidos pela Seção 148 da Lei de Energia Atômica dos EUA [.](https://www.epa.gov/laws-regulations/summary-atomic-energy-act)

## <a name="resources"></a>Recursos

- [Serviços de Nuvem do Azure e Controles de Exportação dos EUA](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=c24c11f2-2cd4-444a-9160-19762855ad3a&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers)
- [Microsoft e FedRAMP](offering-fedramp.md)
- [Microsoft e DoD](offering-dod-disa-l2-l4-l5.md)
- [Nuvem Governamental da Microsoft](https://www.microsoft.com/enterprise/government)
- [Conformidade na Central de Confiabilidade da Microsoft](https://www.microsoft.com/trust-center/compliance/compliance-overview)
