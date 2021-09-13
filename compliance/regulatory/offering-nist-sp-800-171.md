---
title: NIST SP 800-171
description: Os serviços de nuvem da Microsoft estão em conformidade com as diretrizes do NIST SP 800-171 para proteger informações não classificadas controladas (CUI) em sistemas de informações não essenciais.
keywords: Microsoft 365, conformidade, ofertas
ms.localizationpriority: medium
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
ms.openlocfilehash: bce6847fe4c0cd1541348b70aadacc9c13238c31
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/12/2021
ms.locfileid: "59158071"
---
# <a name="nist-sp-800-171"></a>NIST SP 800-171

## <a name="about-nist-sp-800-171"></a>Sobre o NIST SP 800-171

O Instituto Nacional de Padrões e Tecnologia dos EUA (NIST) promove e mantém padrões de medida e diretrizes para ajudar a proteger os sistemas de informações e informações de agências federais. Em resposta à Ordem Executiva 13556 sobre o gerenciamento de informações não classificadas controladas (CUI), ele publicou o [NIST SP 800-171](https://csrc.nist.gov/publications/detail/sp/800-171/rev-1/final), protegendo informações controladas não *classificadas* em sistemas e organizações não-governamentais de informações. A CUI é definida como informações, digitais e físicas, criadas por um governo (ou uma entidade em seu nome) que, embora não seja classificado, ainda é confidencial e requer proteção.

O NIST SP 800-171 foi originalmente publicado em junho de 2015 e foi atualizado várias vezes desde então em resposta à evolução de ciberthreats. Ele fornece diretrizes sobre como a CUI deve ser acessada, transmitida e armazenada com segurança em sistemas e organizações de informações não governamentais; seus requisitos se enquadram em quatro categorias principais:

- Controles e processos para gerenciar e proteger
- Monitoramento e gerenciamento de sistemas de IT
- Limpar práticas e procedimentos para usuários finais
- Implementação de medidas de segurança física e tecnológica

## <a name="microsoft-and-nist-sp-800-171"></a>Microsoft e NIST SP 800-171

As organizações de avaliação de terceiros credenciadas, Kratos Secureinfo e Coalfire, fizeram uma parceria com a Microsoft para atestar que seus serviços de nuvem no escopo atendem aos critérios no NIST SP 800-171, Protegendo informações controladas não classificadas *(CUI)* em Sistemas e Organizações de Informações Não Essenciais , quando eles processam a CUI. A implementação da Microsoft dos requisitos [fedRAMP](offering-fedramp.md) ajuda a garantir que os serviços de nuvem no escopo da Microsoft atendem ou excedam os requisitos do NIST SP 800-171 usando os sistemas e as práticas já em uso.

Os requisitos do NIST SP 800-171 são um subconjunto do NIST SP 800-53, o padrão que o FedRAMP usa. O Apêndice D do NIST SP 800-171 fornece um mapeamento direto de seus requisitos de segurança cui para os controles de segurança relevantes no NIST SP 800-53, para o qual os serviços de nuvem no escopo já foram avaliados e autorizados no programa FedRAMP.

Qualquer entidade que processe ou armazene a CUI do governo dos EUA — instituições de pesquisa, empresas de consultoria, fornecedores de manufatura, deve estar em conformidade com os requisitos rigorosos do NIST SP 800-171. Esse atestado significa que os serviços de nuvem no escopo da Microsoft podem acomodar clientes que procuram implantar cargas de trabalho cui com a garantia de que a Microsoft está em conformidade total. Por exemplo, todos os contratados do DoD que processam, armazenam ou transmitem "informações de defesa cobertas" usando serviços de nuvem da Microsoft em seus sistemas de informações atendem às cláusulas DFARS do Departamento de Defesa dos EUA que exigem conformidade com os requisitos de segurança do NIST SP 800-171.

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Plataformas e serviços em nuvem no escopo da Microsoft

- Azure Commercial, Azure Government
- Dynamics 365 U.S. Government
- Intune
- Office 365 Eua Nuvem da Comunidade Governamental (GCC), Office 365 GCC Alta e DoD

## <a name="azure-dynamics-365-and-nist-sp-800-171"></a>Azure, Dynamics 365 e NIST SP 800-171

Para obter mais informações sobre a conformidade do Azure, do Dynamics 365 e de outros serviços online, consulte a oferta do [Azure NIST SP 800-171.](/azure/compliance/offerings/offering-nist-800-171)

## <a name="office-365-and-nist-sp-800-171"></a>Office 365 e NIST SP 800-171

### <a name="office-365-cloud-environments"></a>Ambientes da nuvem do Office 365

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Aplicabilidade do Office 365 e serviços no escopo

Use a seguinte tabela para determinar a aplicabilidade para seus serviços e assinatura do Office 365:

| **Aplicabilidade** | **Serviços no escopo** |
|:------------------|:----------------------|
| **GCC** | Serviço de Feed de Atividades, Serviços Bing, Delve, Exchange Online, Serviços Inteligentes, Microsoft Teams, Portal do Cliente Office 365, Office Online, Infraestrutura de Serviço Office, Relatórios de Uso Office, OneDrive for Business, Cartão de Pessoas, SharePoint Online, Skype for Business, Windows Ink |
| **GCC Alta** | Serviço de Feed de Atividades, serviços Bing, Exchange Online, Serviços Inteligentes, Microsoft Teams, portal do cliente Office 365, Office Online, infraestrutura de serviço Office, relatórios de uso Office, OneDrive for Business, Cartão de Pessoas, 
SharePoint Online, Skype for Business, Windows Ink |
| **DoD** | Serviço de Feed de Atividades, Serviços Bing, Exchange Online, Serviços Inteligentes, Portal do Cliente do Office 365, Office Online, Infraestrutura de Serviço do Office, Relatórios de Uso do Office, OneDrive for Business, Cartão de Pessoas, Microsoft Teams, SharePoint Online, Skype for Business, Windows Ink |

### <a name="frequently-asked-questions"></a>Perguntas frequentes

**Posso usar a conformidade da Microsoft com o NIST SP 800-171 para minha organização?**

Sim. Os clientes da Microsoft podem usar os controles auditados descritos nos relatórios de organizações independentes de avaliação de terceiros (3PAO) em padrões FedRAMP como parte de seus próprios esforços de análise e qualificação de risco fedRAMP e NIST. Esses relatórios atestam a eficácia dos controles que a Microsoft implementou em seus serviços de nuvem no escopo. Os clientes são responsáveis por garantir que suas cargas de trabalho cui estão em conformidade com as diretrizes do NIST SP 800-171.

### <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Usar o Gerenciador de Conformidade da Microsoft para avaliar o risco

O[Gerenciador de Conformidade da Microsoft](/microsoft-365/compliance/compliance-manager) é um recurso no [Centro de conformidade do Microsoft 365](/microsoft-365/compliance/microsoft-365-compliance-center) para ajudá-lo a entender a postura de conformidade da sua organização e executar ações para ajudar a reduzir os riscos. O Gerenciador de Conformidade oferece um modelo premium para criar uma avaliação para essa regulamentação. Encontre o modelo na página **modelos de avaliação** no Gerenciador de Conformidade. Saiba como [criar avaliações no Compliance Manager](/microsoft-365/compliance/compliance-manager-assessments).

### <a name="resources"></a>Recursos

- [A certificação do Microsoft DoD atende aos requisitos do NIST 800-171](offering-DoD-DISA-L2-L4-L5.md)
- [Conformidade do NIST 800-171 começa com a documentação de segurança cibernética](https://www.nist800171.com/)
- [Autorizações fedRAMP do Microsoft Cloud Services](https://marketplace.fedramp.gov/index.html?status=Compliant&sort=productName#/products)
- [Auditoria e responsabilidade do NIST 800-171 3.3 com Office 365 GCC Alta](https://info.summit7systems.com/blog/nist-3.3-audit-and-accountability-with-office-365)
- [Microsoft e a Estrutura de Segurança Cibernética do NIST](offering-nist-csf.md)
- [Nuvem Governamental da Microsoft](https://www.microsoft.com/enterprise/government)
- [Conformidade na Central de Confiabilidade da Microsoft](https://www.microsoft.com/trust-center/compliance/compliance-overview)
