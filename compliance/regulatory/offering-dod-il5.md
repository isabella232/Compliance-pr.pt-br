---
title: Nível de impacto do Departamento de Defesa (DoD) 5 (IL5)
description: Saiba como a Microsoft atende aos padrões de Nível de Impacto do Departamento de Defesa (DoD) 5 (IL5).
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
ms.openlocfilehash: 9f92ed19a22b7eff8a7e9988e66c51aea90d42ab
ms.sourcegitcommit: 9b0c8852e73e2be54a0f9c6570da67f4964f616c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/12/2021
ms.locfileid: "53385693"
---
# <a name="department-of-defense-dod-impact-level-5-il5"></a>Nível de impacto do Departamento de Defesa (DoD) 5 (IL5)

## <a name="dod-il5-overview"></a>Visão geral do DoD IL5

A Disa (Agência de Sistemas de Informações de Defesa) é uma agência do Departamento de Defesa dos EUA (DoD) responsável pelo desenvolvimento e manutenção do Guia de Requisitos de Segurança de Computação em Nuvem [(SRG)](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html)do DoD. O SRG define os requisitos de segurança de linha de base usados pelo DoD para avaliar a postura de segurança de um provedor de serviços de nuvem (CSP), dando suporte à decisão de conceder uma Autorização Provisória (PA) do DoD que permite que um CSP hospede missões do DoD. Ele incorpora, sobressalva e rescinde o Modelo de Segurança de Nuvem do DoD (CSM) publicado anteriormente e mapeia para a Estrutura de Gerenciamento de Riscos do DoD (RMF).

O DISA orienta as agências e departamentos do DoD no planejamento e autorização do uso de um CSP. Ele também avalia as ofertas de CSP para conformidade com o SRG, um processo de autorização no qual os CSPs podem fornecer documentação explicando sua conformidade com os padrões do DoD. Ele emite PAs (Autorizações Provisórias do DoD) quando apropriado, para que as agências do DoD e organizações de suporte possam usar serviços de nuvem sem precisar passar por um processo de aprovação completo por conta própria, economizando tempo e esforço.

De acordo com os Níveis de Impacto de Informações da Seção [3.2 do SRG,](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#3.2InformationImpactLevels) as informações do IL5 abrangem:

- Informações não classificadas controladas (CUI) que exigem um nível de proteção maior do que o do IL4
    - O [Registro cui fornece](https://www.archives.gov/cui) categorias específicas de informações que estão sob proteção do Poder Executivo, por exemplo, mais de 20 grupos de categorias estão incluídos na lista de categorias [cui](https://www.archives.gov/cui/registry/category-list).
    - [NIST SP 800-171](https://csrc.nist.gov/publications/detail/sp/800-171/rev-2/final) Protegendo informações não *classificadas* controladas em sistemas e organizações não-aderais destina-se a ser usado por agências federais em contratos ou outros acordos estabelecidos com organizações não federais.

- NSS (National Security Systems)
    - [A Diretriz do NIST SP 800-59](https://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-59.pdf)  para identificar um sistema de informações como um sistema de segurança nacional fornece definições de NSS.
    - [CnSSI 1253](https://www.dcsa.mil/portals/91/documents/ctp/nao/CNSSI_No1253.pdf) *Security Categorization and Control Selection for National Security Systems* fornece orientações sobre os padrões de segurança que as agências federais devem aplicar para categorizar informações de segurança nacional.

O [memorando CIO do DoD 15](https://www.esi.mil/contentview.aspx?id=585) de  dezembro de 2014 sobre Diretrizes Atualizadas sobre a Aquisição e o Uso de Serviços comerciais de Computação em Nuvem afirma que 'FedRAMP servirá como a linha de base de segurança mínima para todos os serviços de nuvem do DoD'. O SRG usa a linha de base Moderada fedRAMP em todos os níveis de impacto de informações (IL) e considera a Linha de Base Alta em alguns.

O uso do DoD da Seção [5.1.1](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5SECURITYREQUIREMENTS) do SRG dos Controles de Segurança *fedRAMP* afirma que um FedRAMP High PA, complementado com controles FedRAMP+ do DoD e aprimoramentos de controle (C/CEs) e requisitos no SRG, são usados para avaliar os CSPs para a concessão de um PA do DoD no IL5. Independentemente da linha de base C/CE ser usada como base para um Pa Alto FedRAMP, considerações adicionais e/ou requisitos precisarão ser avaliados e aprovados antes que um PA do DoD possa ser concedido no IL5. Especificamente, a [Seção SRG 5.1.2](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5SECURITYREQUIREMENTS) FedRAMP+ Estados de *Controles/Aprimoramentos* de Segurança do DoD na Tabela 2 que 10 C/CEs adicionais além da linha de base FedRAMP High são necessárias para um PA do DoD IL5.

Além disso, de acordo com a [Seção 5.2.2.3](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5.2LegalConsiderations) *IL5 Requisitos* de Localização e Separação do SRG, os seguintes requisitos (entre outros) devem estar em uso para um NÍVEL 5 PA:

- A separação virtual/lógica entre locatários/missões do DoD e do Governo Federal é suficiente. A separação virtual/lógica entre sistemas de locatário/missão é necessária.
- A separação física de locatários que não são do DoD/do Governo Federal (ou seja, locatários públicos, locais/estatais do governo) é necessária.
- O CSP restringe o acesso potencial às informações do DoD e da comunidade aos funcionários do CSP que são cidadãos dos EUA.

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Plataformas de nuvem no escopo da Microsoft & serviços

- Azure
- Serviço de Atendimento ao Cliente do Dynamics 365
- Microsoft Defender para Ponto de Extremidade (anteriormente Proteção Avançada contra Ameaças do Microsoft Defender)
- Microsoft Graph
- Microsoft Stream
- Office 365 U.S. Government Defense
- Power Automate (anteriormente Microsoft Flow)
- Power BI

## <a name="azure-dynamics-365-and-dod-il5"></a>Azure, Dynamics 365 e DoD IL5

Para obter mais informações sobre a conformidade do Azure, dynamics 365 e outros serviços online, consulte a oferta [do Azure DoD IL5](/azure/compliance/offerings/offering-dod-il5).

## <a name="office-365-and-dod-il5"></a>Office 365 e DoD IL5

### <a name="office-365-cloud-environments"></a>Office 365 ambientes de nuvem

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365 aplicabilidade e serviços no escopo

Use a tabela a seguir para determinar a aplicabilidade para seus serviços Office 365 e assinatura:

| **Aplicabilidade** | **Serviços no escopo** |
|:------------------|:----------------------|
| **DoD** | Serviço de Feed de Atividades, serviços Bing, Exchange Online, Proteção do Exchange Online, Serviços Inteligentes, Microsoft Teams, Portal do Cliente Office 365, Office Online, infraestrutura de serviço Office, relatórios de uso Office, OneDrive for Business, Cartão de Pessoas, SharePoint Online, Skype for Business, Windows Ink |

### <a name="attestation-documents"></a>Documentos de atestado

Os clientes do governo dos EUA podem solicitar Office 365 documentação fedRAMP de defesa governamental dos EUA diretamente do [FedRAMP Marketplace](https://marketplace.fedramp.gov/#!/products?sort=productName&productNameSearch=azure) enviando um formulário de solicitação de acesso ao pacote. Você deve ter um endereço de email .gov ou .mil para acessar um pacote de segurança fedRAMP diretamente do FedRAMP.

Selecione a documentação FedRAMP e DoD, incluindo o Plano de Segurança do Sistema (SSP), relatórios de monitoramento contínuos, Plano de Ações e Marcos (POA M), etc., está disponível para clientes em NDA e autorização de acesso pendente na seção Relatórios de Auditoria do Portal de Confiança de Serviço \& [- FedRAMP Reports.](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3) Entre em contato com seu representante de conta da Microsoft para assistência.

### <a name="resources"></a>Recursos

- [Soluções governamentais da Microsoft](https://www.microsoft.com/enterprise/government)
- [Guia de Requisitos de Segurança de Computação em Nuvem do DoD](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html)
- [Documentos fedRAMP](https://www.fedramp.gov/documents/)
- [RmF (DoD Instruction 8510.01](https://www.esd.whs.mil/Portals/54/Documents/DD/issuances/dodi/851001p.pdf) *DoD Risk Management Framework) para Tecnologia de Informações do DoD (IT)*
- [NIST SP 800-37](https://csrc.nist.gov/publications/detail/sp/800-37/rev-2/final) *Risk Management Framework for Information Systems and Organizations: A System Life-Cycle Approach for Security and Privacy*
- Controles de Segurança e Privacidade do [NIST SP 800-53](https://csrc.nist.gov/Projects/risk-management/sp800-53-controls/release-search#!/800-53) *para sistemas e organizações de informações*
- [Diretriz do NIST SP 800-59](https://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-59.pdf) para identificar um sistema de informações *como um sistema de segurança nacional*
- [CnSSI 1253](https://www.dcsa.mil/portals/91/documents/ctp/nao/CNSSI_No1253.pdf) *Security Categorization and Control Selection for National Security Systems*
- [NIST SP 800-171](https://csrc.nist.gov/publications/detail/sp/800-171/rev-2/final) *Protecting Controlled Unclassified Information in Nonfederal Systems and Organizations*
- Registro de informações não classificadas controladas (CUI) [e](https://www.archives.gov/cui) lista de [categorias cui.](https://www.archives.gov/cui/registry/category-list)
