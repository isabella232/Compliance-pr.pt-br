---
title: Health Data Hosting (HDS) França
description: Os serviços de nuvem da Microsoft são certificados quanto a conformidade por meio do padrão Health Data Hosting (Hébergeurs de Données de Santé).
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
ms.openlocfilehash: f8c99a93cac767439d157a7d709c7ed1d706c113
ms.sourcegitcommit: 16cec8f7ca799a415bfbae937b177a628a0f2987
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/24/2021
ms.locfileid: "58505934"
---
# <a name="health-data-hosting-hds-france"></a>Hospedagem de Dados de Integridade (HDS) França

## <a name="about-hds"></a>Sobre a HDS

A certificação Hébergeurs de Données de Santé (HDS) é exigida de entidades como provedores de serviços de nuvem que hospedam dados pessoais de saúde regidos pelas leis francesas e coletados para fornecer serviços de saúde preventivos, de diagnóstico, entre outros. O regulamento da HDS foi emitido pela [ASIP SANTÉ](https://esante.gouv.fr/) que, de acordo com o Ministério da Saúde francês, é responsável por promover soluções de saúde por meios eletrônicos na França.

A hospedagem de dados de saúde é regulamentada de acordo com a lei francesa pelo Código de Saúde Pública da França (Artigo L.1111-8) que estipula que qualquer organização de saúde, como hospitais, empresas farmacêuticas e laboratórios, que manipule dados médicos pessoais deve usar um provedor de serviços certificado pela HDS. Em abril de 2018, entraram em vigor os novos artigos, que vão do R1111-8-8 ao R1111-11, do Código de Saúde Pública que alteram o procedimento de credenciamento de uma autorização pelo Ministério da Saúde francês por uma certificação de um organismo autorizado como o BSI.

A certificação HDS exige que os provedores de serviços implementem medidas para manter os dados pessoais de saúde seguros, confidenciais e que possam ser acessados pelos pacientes. Essas medidas incluem procedimentos fortes de autenticação e autorização, sistemas de backup robustos e métodos de criptografia eficientes. A HDS também especifica disposições obrigatórias que devem ser incluídas nos contratos com o provedor de serviços de nuvem. Esses requisitos aplicam-se independentemente do local em que os dados são armazenados.

## <a name="microsoft-and-hds"></a>Microsoft e HDS

O Microsoft Azure, o Microsoft Dynamics 365 e o Microsoft Office 365 receberam a certificação HDS (Health Data Hosting) necessária para todas as entidades que hospedam dados pessoais de saúde regidos pela lei francesa. Isso fez da Microsoft o primeiro grande provedor de serviços de nuvem a atender aos rígidos padrões franceses de armazenamento e processamento de dados de saúde. Essa certificação, exigida pela revisão do Código de Saúde Pública da França de 2018, impõe requisitos avançados de segurança e privacidade sobre os serviços de hospedagem e provedores de nuvem para garantir que a confidencialidade e a integridade dos dados confidenciais sejam adequadamente protegidas.

A conformidade da Microsoft com os requisitos da HDS foi auditada e certificada pelo [Grupo BSI](https://www.bsigroup.com/fr-FR/), um organismo de certificação independente credenciado pelas autoridades francesas para realizar auditorias na HDS.

A certificação HDS permite que os provedores de assistência médica na França usem os serviços de nuvem da Microsoft para economizar custos melhorando a eficiência clínica e operacional, além de permitir o desenvolvimento de soluções inovadoras e avançadas em assistência médica. Os provedores podem desenvolver aplicativos inteligentes ou usar aplicativos de terceiros hospedados no Azure para implementar análises preditivas para personalizar a assistência médica, avaliar e tratar pacientes à distância (telemedicina) e aprimorar o monitoramento terapêutico de medicamentos.

A rigorosa auditoria abrangeu as medidas adotadas pela Microsoft para proteger dados pessoais de saúde e sua confidencialidade, incluindo:

- A certificação de [Gerenciamento da Segurança da Informação ISO/IEC 27001:2013](offering-iso-27001.md) dos serviços de nuvem da Microsoft que são auditados anualmente para verificar a conformidade.
- Alto nível de privacidade baseado no cumprimento do RGPD e no [Código de conduta da ISO/IEC 27018 para a proteção de dados pessoais na nuvem](offering-iso-27018.md).

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Plataformas e serviços em nuvem no escopo da Microsoft

- [Azure](https://aka.ms/AzureCompliance). O certificado HDS se aplica aos serviços do Azure listados como em conformidade com o padrão ISO/IEC 27001 nas ofertas de Conformidade do Azure e provisionados nas regiões do Azure:
    - Central da França (Paris)
    - Sul da França (Marselha)
    - Norte da Europa (Irlanda)
    - Europa Ocidental (Países Baixos)
- Dynamics 365. O certificado HDS aplica-se aos [Principais Serviços Online](https://aka.ms/Online-Services-Terms) do Dynamics 365 provisionados pelas regiões geográficas da França e União Europeia.
- Intune
- Microsoft 365. O certificado HDS aplica-se aos [Principais Serviços Online](https://aka.ms/Online-Services-Terms) do Office 365 provisionados pelas regiões geográficas da França e União Europeia.
- Serviço de nuvem do Power BI como um serviço autônomo ou incluído em um plano ou pacote do Office 365

O certificado HDS não se aplica ao Microsoft Online Serviços em versão prévia ou pré-lançamento.

## <a name="audits-reports-and-certificates"></a>Auditorias, relatórios e certificados

[A certificação HDS](https://esante.gouv.fr/labels-certifications/hebergement-des-donnees-de-sante) impõe requisitos de segurança e privacidade avançados em serviços de hospedagem e provedores de nuvem para garantir que a confidencialidade e a integridade dos dados confidenciais sejam adequadamente protegidas. Os serviços de nuvem da Microsoft (incluindo o Azure) receberam a certificação HDS, conforme mostrado na lista ASIP Santé [de hosts certificados pela HDS](https://esante.gouv.fr/labels-certifications/hds/liste-des-herbergeurs-certifies).

## <a name="how-to-implement"></a>Como implementar

- **Termos contratuais**: O Código de Saúde Pública da França exige a execução de termos contratuais específicos entre o serviço de hospedagem de dados de saúde ou o provedor de serviços de nuvem e seus clientes. Os clientes qualificados devem entrar em contato com o ponto de contato de licenciamento da Microsoft para firmar esses termos contratuais específicos antes de hospedar dados pessoais de saúde nos serviços online da Microsoft.
- **Saúde e ciências da vida**: Visões gerais de casos, guias de solução, tutoriais e outros recursos para ajudar a criar soluções do Azure.

## <a name="resources"></a>Recursos

- [Documentação de conformidade do Azure](/azure/compliance/)
- [Termos do Microsoft Online Services](https://aka.ms/Online-Services-Terms)
- [Blog de certificação do Microsoft HDS](https://news.microsoft.com/2018/11/06/microsoft-1er-acteur-majeur-du-cloud-public-a-etre-certifie-hebergeur-de-donnees-de-sante-en-france/)
- [Azure França](https://azure.microsoft.com/global-infrastructure/france/)
- [Azure for health](https://azure.microsoft.com/industries/healthcare/)
- [Segurança na Microsoft](https://www.microsoft.com/security)
- [Conformidade na Central de Confiabilidade da Microsoft](https://www.microsoft.com/trust-center/compliance/compliance-overview)
