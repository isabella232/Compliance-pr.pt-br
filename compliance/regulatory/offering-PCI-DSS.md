---
title: Padrão de Segurança de Dados (DSS) da Indústria de Cartões de Pagamento (PCI)
description: O Azure, o SharePoint Online e o OneDrive for Business estão em conformidade com os Padrões de Segurança de Dados da Indústria de Cartões de Pagamento Level 1 versão 3.2.
keywords: Microsoft 365, conformidade, ofertas
ms.localizationpriority: high
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
ms.openlocfilehash: 09c18fce6544984a7e9d639e68d0f0201c584768
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2021
ms.locfileid: "58947522"
---
# <a name="payment-card-industry-pci-data-security-standard-dss"></a>Padrão de Segurança de Dados (DSS) da Indústria de Cartões de Pagamento (PCI)

## <a name="pci-dss-overview"></a>Visão geral do PCI DSS

O DSS (Padrão de Segurança de Dados) da PCI (Indústria de Cartões de Pagamento) é um padrão de segurança de informação global criado para prevenir fraudes por meio do maior controle de dados de cartões de crédito. Organizações de todos os tamanhos devem seguir os padrões PCI DSS se aceitarem cartões de pagamento das cinco principais marcas de cartão de crédito: Visa, MasterCard, American Express, Discover e Japan Credit Bureau (JCB). A conformidade com o PCI DSS é obrigatória para toda empresa que armazene, processe ou transmita dados de pagamento e do titular do cartão.

## <a name="microsoft-and-pci-dss"></a>Microsoft e PCI DSS

A Microsoft completou uma avaliação anual de PCI DSS por um avaliador qualificado de segurança (Qualified Security Assessor - QSA). Os auditores avaliaram os ambientes do Microsoft Azure, do Microsoft OneDrive for Business e do Microsoft SharePoint Online, que inclui validar a infraestrutura, desenvolvimento, operações, gerenciamento, suporte e serviços dentro do escopo. O PCI DSS especifica quatro níveis de conformidade de acordo com o volume de transações. Azure, OneDrive for Business e Microsoft Office SharePoint Online são certificados como compatíveis com PCI DSS versão 3.2 no Provedor de Serviços Nível 1 (o maior volume de transações, mais de 6 milhões por ano).

A avaliação resulta em um Certificado de Conformidade (Attestation of Compliance - AoC), que está disponível para clientes e um Relatório sobre Conformidade (Report on Compliance - RoC) emitidos pelo QSA. O período de vigência da conformidade tem início no momento da aprovação na auditoria e recebimento do AoC do avaliador e termina um ano após a data de assinatura do AoC. 

Os clientes que desejam desenvolver um ambiente do titular do cartão ou um serviço de processamento de cartões podem utilizar essas validações em muitas das partes subjacentes, reduzindo assim o trabalho e os custos associados à obtenção de sua própria certificação PCI DSS.

É importante entender que o status de conformidade do Azure, do OneDrive for Business e do SharePoint Online com o PCI DSS não se converte automaticamente na certificação PCI DSS para os serviços que os clientes desenvolvam ou hospedem nessas plataformas. Os clientes são responsáveis por garantir sua conformidade com os requisitos do PCI DSS.

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Plataformas e serviços de nuvem da Microsoft no escopo

- Azure e Azure Governamental
- Intune
- Microsoft Cloud App Security
- [Microsoft Defender para Ponto de Extremidade](/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection)
- Microsoft Graph
- Office 365
- OneDrive for Business e SharePoint Online (somente nos Estados Unidos)
- Serviço de nuvem do PowerApps como um serviço autônomo ou incluído em um plano ou pacote com a marca Office 365 ou Dynamics 365
- Power Automate (como um serviço autônomo ou incluído em um plano ou pacote com a marca Office 365 ou Dynamics 365)
- Serviço de nuvem do Power BI como um serviço autônomo ou incluído em um plano ou pacote com a marca Office 365

## <a name="azure-dynamics-365-and-pci-dss"></a>Azure, Dynamics 365 e PCI DSS

Para obter mais informações sobre o Azure, o Dynamics 365 e outros serviços online, consulte a [Oferta do Azure PCI DSS](/azure/compliance/offerings/offering-pci-dss).

## <a name="office-365-and-pci-dss"></a>Office 365 e PCI DSS

### <a name="office-365-cloud-environments"></a>Nuvem do Office 365

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Aplicabilidade do Office 365 e serviços no escopo

Use a seguinte tabela para determinar a aplicabilidade para seus serviços e assinatura do Office 365:

| **Aplicabilidade** | **Serviços no escopo** |
|:------------------|:----------------------|
| **Comercial** | OneDrive for Business (Estados Unidos), SharePoint Online |

### <a name="office-365-audit-reports-and-certificates"></a>Auditoria, relatórios e certificados do Office 365

- [Atestado de Conformidade ( AoC) PCI DSS do OneDrive for Business e SharePoint Online](https://aka.ms/spo-pci)

### <a name="frequently-asked-questions"></a>Perguntas frequentes

**Por que a página de rosto do Atestado de Conformidade (AoC) mostra “Junho de 2018”?**

A data de junho de 2018 na página de rosto é de quando o modelo de AoC foi publicado. Consulte a data da avaliação na Seção 2. 

**Qual é a relação entre PA DSS e PCI DSS?**

O Padrão de Segurança de Dados em Aplicativos de Pagamento (Payment Application Data Security Standard - PA DSS) é um conjunto de requisitos que cumpre o PCI DSS e substitui as Práticas Recomendadas para Aplicativos de Pagamento da Visa (Visa’s Payment Application Best Practices) e consolida os requisitos de conformidade dos outros emissores de cartões principais. O PA DSS ajuda os fornecedores de software a desenvolver aplicativos de terceiros para armazenar, processar ou transmitir dados de pagamento do titular do cartão como parte do processo de autorização ou pagamento do cartão. Os varejistas precisam usar aplicativos com a certificação PA DSS para obter efetivamente a conformidade com o PCI DSS. O PA DSS não se aplica ao Azure.

**O que é um adquirente? O Azure usa um?**

Os adquirentes são bancos ou outras entidades que processam transações de cartões de pagamento. O Azure não oferece o serviço de processamento de cartões de pagamento e, portanto, não utiliza um adquirente.

**A quais organizações e comerciantes o PCI DSS se aplica?**

O PCI DSS se aplica a qualquer empresa, independentemente do tamanho ou do número de transações que aceite, transmita ou armazene dados de titulares de cartões. Ou seja, se qualquer cliente pagar uma empresa usando um cartão de crédito ou débito, os requisitos do PCI DSS se aplicarão. As empresas são validadas em um dos quatro níveis de acordo com o volume total de transações durante um período de 12 meses. O Level 1 engloba empresas que processam mais de 6 milhões de transações por ano; o Level 2, de 1 milhão a 6 milhões de transações; o Level 3, de 20.000 a 1 milhão de transações e o Level 4, para menos de 20.000 transações.

**Há planos para que o OneDrive for Business e o SharePoint Online estejam em conformidade com o PCI DSS fora dos Estados Unidos?**

Atualmente, o OneDrive for Business e o SharePoint Online estão em conformidade com o PCI DSS somente nos Estados Unidos (EUA). A Microsoft avaliará os requisitos e as linhas do tempo em outras regiões fora dos EUA e fornecerá atualizações quando e se outras regiões forem adicionadas ao roteiro.

**O que está no escopo do OneDrive for Business e do Microsoft Office SharePoint Online?**

Atualmente, apenas os arquivos e documentos carregados no OneDrive for Business e no SharePoint Online estarão em conformidade com o PCI DSS.

### <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Use o Gerenciador de Conformidade da Microsoft para avaliar o risco

O[Gerenciador de Conformidade da Microsoft](/microsoft-365/compliance/compliance-manager) é um recurso no [Centro de conformidade do Microsoft 365](/microsoft-365/compliance/microsoft-365-compliance-center) para ajudá-lo a entender a postura de conformidade da sua organização e executar ações para ajudar a reduzir os riscos. O Gerenciador de Conformidade oferece um modelo premium para criar uma avaliação para essa regulamentação. Encontre o modelo na página **modelos de avaliação** no Gerenciador de Conformidade. Saiba como [criar avaliações no Compliance Manager](/microsoft-365/compliance/compliance-manager-assessments).

### <a name="resources"></a>Recursos

- [Conselho de Padrões de Segurança (Security Standards Council) do PCI](https://www.pcisecuritystandards.org/)
- [Padrão de Segurança de Dados (Data Security Standard) do PCI](https://www.pcisecuritystandards.org/documents/PCI_DSS_v3-1.pdf)
- [Guia de Referência (Quick Reference Guide) do PCI DSS](https://www.pcisecuritystandards.org/documents/PCISSC%20QRG%20August%202014%20-print.pdf)
- [Conformidade na Central de Confiabilidade da Microsoft](https://www.microsoft.com/trust-center/compliance/compliance-overview)
