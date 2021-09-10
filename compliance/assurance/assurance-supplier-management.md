---
title: Visão geral do gerenciamento de fornecedores
description: Saiba mais sobre o gerenciamento de fornecedores Microsoft 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH'
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
ms.openlocfilehash: 3b0a4c7f12eba49c252f71e47eda1685fd4d41a4
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2021
ms.locfileid: "58946933"
---
# <a name="supplier-management-overview"></a>Visão geral do gerenciamento de fornecedores

## <a name="how-does-microsoft-manage-risk-related-to-suppliers"></a>Como a Microsoft gerencia o risco relacionado a fornecedores?

A Microsoft faz parcerias com empresas de terceiros para ajudar a atender às necessidades de nossos clientes. Essas empresas de terceiros são conhecidas como fornecedores ou subprocessadores. A segurança e a privacidade de fornecedores na Microsoft são governadas pelo nosso programa de Garantia de Segurança e Privacidade de Fornecedores [(SSPA),](https://www.microsoft.com/procurement/sspa?activetab=pivot1%3aprimaryr6)um conjunto de requisitos em toda a empresa para todos os fornecedores que são parceiros da Microsoft para fornecer nossos serviços online. Embora o programa SSPA fornece uma governança abrangente e gerenciamento de nossa base de fornecedores, unidades de negócios individuais podem manter requisitos adicionais para seus fornecedores.

## <a name="how-does-microsofts-supplier-security-and-privacy-assurance-sspa-program-protect-customer-data"></a>Como o Programa de Garantia de Segurança e Privacidade de Fornecedores (SSPA) da Microsoft protege os dados do cliente?

O SSPA é uma parceria entre a Microsoft Procurement, Assuntos Jurídicos e Externos Corporativos e a Segurança Corporativa para garantir que os fornecedores aderam aos princípios de privacidade e segurança da Microsoft. O escopo do SSPA abrange todos os fornecedores que processam Dados Pessoais ou Dados Confidenciais da Microsoft. O registro do programa SSPA inclui a adesão aos Requisitos de Proteção de Dados (DPR) da Microsoft. A DPR consiste em controles de segurança e privacidade que os fornecedores devem implementar antes de iniciar o trabalho contratado com a Microsoft. Todos os fornecedores inscritos autotestam a conformidade com a DPR anualmente.

Os requisitos de DPR são escopos com base em seis categorias de processamento de dados distintas para as que um fornecedor pode ser aprovado como parte de seu registro no SSPA. Essas categorias são usadas para identificar o risco associado aos serviços que um fornecedor fornece à Microsoft. O perfil de processamento de dados do fornecedor determina quais controles DPR são considerados no escopo para fornecer proteção de dados apropriada. Os fornecedores que processam dados considerados um risco maior devem estar em conformidade com todos os requisitos de DPR e também podem precisar fornecer verificação independente da conformidade. As ferramentas de compra da Microsoft validam o status SSPA de todos os fornecedores, incluindo a conformidade com partes aplicáveis da DPR, antes de permitir a aquisição desse fornecedor.

## <a name="what-types-of-subprocessors-provide-services-for-microsoft"></a>Quais tipos de subprocessadores fornecem serviços para a Microsoft?

Um "subprocessador" é um terceiro que a Microsoft engaja cujas obrigações incluem o processamento de Dados Pessoais da Microsoft para os quais a Microsoft é um processador. Os subprocessadores da Microsoft se enquadram em três categorias distintas. Cada um deve demonstrar a conformidade com o SSPA antes de poder processar dados do cliente em nome da Microsoft.

- Os subprocessadores de **tecnologia** fornecem tecnologias usadas para fornecer recursos específicos dos serviços online da Microsoft. Se um cliente implantar um desses serviços, os subprocessadores identificados para esse serviço poderão processar, armazenar ou acessar dados do cliente ou dados pessoais enquanto ajudam a fornecer esse serviço.
- **Os subprocessadores** auxiliares fornecem serviços que dão suporte, operam e mantêm os serviços online. Se um cliente implantar um desses serviços, os subprocessadores identificados poderão processar, armazenar ou acessar dados de clientes limitados ou dados pessoais ao fornecer seus serviços auxiliares.
- **Os subprocessadores** de Aumento de Equipe têm duas formas diferentes: em ambos os cenários, Os Dados Pessoais residem apenas em instalações da Microsoft, nos sistemas Microsoft, e estão sujeitos às políticas e supervisão da Microsoft.

    - A primeira forma de aumento de equipe fornece à equipe que dá suporte, opera e mantém o Microsoft serviços online. Embora cumpram suas responsabilidades, esses subprocessadores podem ser expostos a dados do cliente ou dados pessoais. Por exemplo, um subprocessador pode executar a solução de problemas remota em um servidor Microsoft e, ao fazer isso, pode ser exposto a snippets de dados do cliente em um log de despejo de memória do servidor.
    - A segunda forma de aumento de equipe envolve subprocessadores que trabalham lado a lado com funcionários em tempo integral da Microsoft para dar suporte, operar e manter os serviços online da Microsoft. Esses subprocessadores podem ser expostos a dados pseudonimizados como parte de seu trabalho junto com funcionários em tempo integral da Microsoft.

Os subprocessadores de tecnologia e auxiliar são necessários para implementar controles de acesso em conformidade com os Requisitos de Proteção de Dados (DPR) da Microsoft. Esses requisitos atendem ou excedem os compromissos contratuais que a Microsoft faz com seus clientes nos Termos de Serviço Online (OST). Os fornecedores que executam o trabalho de aumento de equipe estão sujeitos aos mesmos controles de acesso no local para funcionários em tempo integral da Microsoft.

## <a name="how-does-microsoft-onboard-suppliers"></a>Como a Microsoft integra fornecedores?

Fornecedores de terceiros são obrigados a assinar um Contrato Mestre da Microsoft como parte do processo de integração. Este contrato rege a relação entre a Microsoft e seus fornecedores e garante o gerenciamento consistente das relações de fornecedores. Como parte da integração, os fornecedores se inscrevem no SSPA e devem concluir todos os requisitos aplicáveis antes de serem aprovados para qualquer categoria de processamento de dados. As unidades de negócios da Microsoft só são capazes de criar compromissos com fornecedores quando a atividade de processamento de dados para o envolvimento corresponde às categorias de processamento de dados para as quais o fornecedor foi aprovado.

## <a name="how-does-microsoft-notify-customers-of-changes-to-suppliers-who-process-their-data"></a>Como a Microsoft notifica os clientes sobre alterações nos fornecedores que processam seus dados?

De acordo com o DPA (Microsoft Online Service Data Protection Addendum), a Microsoft faz compromissos adicionais em relação aos períodos de aviso para a adição de qualquer subprocessador. Os quadros de tempo de aviso dependem do tipo de dados que o subprocessador processará em nome da Microsoft. Conforme declarado na DPA, a Microsoft se compromete a fornecer aviso aos clientes com pelo menos seis meses de antecedência de qualquer novo subprocessador que processará Dados do Cliente. Para quaisquer outros Dados Pessoais, a Microsoft fornecerá pelo menos 30 dias de aviso. O aviso é fornecido pela atualização da lista [Microsoft Online Services Subprocessador](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=926b2cf5-6b6e-43ca-9bc3-f73e961aad5f&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_Subprocessor_List).

## <a name="related-external-regulations--certifications"></a>Regulamentações externas relacionadas & certificações

Os serviços online da Microsoft são regularmente auditados para conformidade com regulamentações e certificações externas. Consulte a tabela abaixo para validação de controles relacionados ao gerenciamento de fornecedores.

### <a name="azure-and-dynamics-365"></a>Azure e Dynamics 365

| **Auditorias externas** | **Section** | **Data do relatório mais recente** |
|:--------------------|:------------|:-----------------------|  
| [ISO 27001/27002](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Instrução of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7af5304-3a31-40e6-9abb-e26352305d41&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.15.1: Segurança de informações nas relações de fornecedores | 2 de dezembro de 2020 |
| [ISO 27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Instrução of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a3bca0ac-867d-4204-b66b-13665f5f1e8d&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=25718a8a-f34d-41e1-a95a-c49246508787&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.15.1: Segurança de informações nas relações de fornecedores | 2 de dezembro de 2020 |
| [ISO 27018](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Instrução of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=56904fc3-0942-4ff5-9eef-7cabc751a25c&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) |  A.8.1: Divulgação do processamento de PII subcontratado | 2 de dezembro de 2020 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=234a0f57-83c1-4afc-a586-a0e7a59592f7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=75c8cbf6-e456-473c-a05e-34fea888ec2a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | SOC2-25: Gerenciamento de risco de fornecedor <br> C5-2: Revisão de perfil de risco de fornecedor| 31 de março de 2021 |

### <a name="office-365"></a>Office 365

| **Auditorias externas** | **Section** | **Data do relatório mais recente** |
|:--------------------|:------------|:-----------------------|  
| [FedRAMP](https://compliance.microsoft.com/compliancemanager) | CA-3: Interconexões do sistema <br> IA-4: Gerenciamento de identificador <br> PS-6: contratos de acesso <br> PS-7: Segurança de funcionários de terceiros <br> SA-4: Processo de aquisições <br> SA-9: Serviços do sistema de informações externos <br> SA-12: Proteção de cadeia de fornecimento | 24 de setembro de 2020 |
| [ISO 27001/27002/27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Instrução of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.15.1: Segurança de informações nas relações de fornecedores | Abril de 20, 2021 |
| [ISO 27018](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Instrução of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) |  A.8.1: Divulgação do processamento de PII subcontratado | 24 de dezembro de 2020 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-53: Monitoramento de terceiros | 24 de dezembro de 2020 |

## <a name="resources"></a>Recursos

- [Programa de Garantia e Privacidade de Segurança do Fornecedor](https://www.microsoft.com/procurement/sspa?activetab=pivot1%3aprimaryr6)
