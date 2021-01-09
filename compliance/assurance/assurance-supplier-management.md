---
title: Visão geral do gerenciamento de fornecedores
description: Saiba mais sobre o gerenciamento de fornecedores no Microsoft 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH'
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 4da4775332989c4a40738777dfae7318e27086f0
ms.sourcegitcommit: 7a5b6bc58fc4613b38f3fda20aebee5cec6a5730
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "49787370"
---
# <a name="supplier-management-overview"></a>Visão geral do gerenciamento de fornecedores

## <a name="how-does-microsoft-manage-risk-related-to-suppliers"></a>Como a Microsoft gerencia os riscos relacionados aos fornecedores?

A Microsoft faz parcerias com empresas de terceiros para ajudar a atender às necessidades dos nossos clientes. Essas empresas de terceiros são referidas como fornecedores ou subprocessadores. A segurança e a privacidade dos fornecedores na Microsoft são regidos pelo nosso programa [SSPA (Supplier Security and Privacy Assurance),](https://www.microsoft.com/procurement/sspa?activetab=pivot1%3aprimaryr6)um conjunto de requisitos para toda a empresa para todos os fornecedores parceiros da Microsoft fornecerem nossos serviços online. Embora o programa SSPA fornece governança e gerenciamento abrangentes de nossa base de fornecedores, unidades de negócios individuais, como o Microsoft 365, podem manter requisitos adicionais para seus fornecedores.

## <a name="how-does-microsofts-supplier-security-and-privacy-assurance-sspa-program-protect-customer-data"></a>Como o programa SSPA (Supplier Security and Privacy Assurance) da Microsoft protege os dados do cliente?

O SSPA é uma parceria entre Compras da Microsoft, Assuntos Jurídicos e Externos Corporativos e Segurança Corporativa para garantir que os fornecedores cumpram os princípios de privacidade e segurança da Microsoft. O escopo do SSPA abrange todos os fornecedores que processam Dados Pessoais ou Dados Confidenciais da Microsoft. O registro do programa SSPA inclui a adesão aos Requisitos de Proteção de Dados (DPR) da Microsoft. A DPR consiste em controles de segurança e privacidade que os fornecedores devem implementar antes de começar a trabalhar com a Microsoft. Todos os fornecedores inscritos autotestam a conformidade com a DPR anualmente.

Os requisitos de DPR têm como escopo seis categorias distintas de processamento de dados que um fornecedor pode aprovar como parte de seu registro no SSPA. Essas categorias são usadas para identificar o risco associado aos serviços que um fornecedor fornece à Microsoft. O perfil de processamento de dados do fornecedor determina quais controles de DPR são considerados no escopo para fornecer proteção de dados apropriada. Fornecedores que processam dados considerados de risco mais alto devem atender a todos os requisitos de DPR e também podem precisar fornecer verificação independente de conformidade. As ferramentas de compra da Microsoft validam o status do SSPA de todos os fornecedores, incluindo a conformidade com as partes aplicáveis da DPR, antes de permitir a aquisição desse fornecedor.

## <a name="what-types-of-subprocessors-provide-services-for-microsoft"></a>Quais tipos de subprocessadores fornecem serviços para a Microsoft?

Um "subprocessador" é um terceiro que a Microsoft envolve cujas obrigações incluem o processamento de Dados Pessoais da Microsoft para os quais a Microsoft é um processador. Os subprocessadores da Microsoft se enquadram em três categorias distintas. Cada um deve demonstrar a conformidade com o SSPA antes de poder processar dados do cliente em nome da Microsoft.

- **Os** subprocessadores de tecnologia fornecem tecnologias usadas para fornecer serviços online específicos da Microsoft. Se um cliente implantar um desses serviços, os subprocessadores identificados para esse serviço poderão processar, armazenar ou acessar dados pessoais do cliente enquanto ajudam a fornecer esse serviço.
- **Os** subprocessadores auxiliares fornecem serviços que suportam, operam e mantêm os serviços online. Se um cliente implantar um desses serviços, os subprocessadores identificados poderão processar, armazenar ou acessar dados pessoais ou dados pessoais limitados enquanto fornece seus serviços auxiliares.
- **Os** subprocessadores de Aumento de Equipe têm duas formas diferentes: em ambos os cenários, os Dados Pessoais residem apenas em instalações da Microsoft, em sistemas Microsoft, e estão sujeitos a políticas e supervisão da Microsoft.

    - A primeira forma de aumento da equipe fornece equipe que oferece suporte, opera e mantém os serviços online da Microsoft. Embora cumpram suas responsabilidades, esses subprocessadores podem ser expostos aos dados do cliente ou aos dados pessoais. Por exemplo, um subprocessador pode executar a solução de problemas remota em um servidor da Microsoft e, ao fazer isso, pode ser exposto a trechos de dados do cliente em um log de despejo de falha do servidor.
    - A segunda forma de aumento da equipe envolve os subprocessadores que trabalham lado a lado com os funcionários em tempo integral da Microsoft para dar suporte, operar e manter os serviços online da Microsoft. Esses subprocessadores podem ser expostos a dados pseudonimizados como parte de seu trabalho junto com os funcionários em tempo integral da Microsoft.

A tecnologia e os subprocessadores auxiliares são necessários para implementar controles de acesso em conformidade com os Requisitos de Proteção de Dados (DPR) da Microsoft. Esses requisitos atendem ou excedem os compromissos contratuais que a Microsoft faz com seus clientes nos Termos de Serviço Online (OST). Fornecedores que executam o trabalho de aumento da equipe estão sujeitos aos mesmos controles de acesso para funcionários em tempo integral da Microsoft.

## <a name="how-does-microsoft-onboard-suppliers"></a>Como a Microsoft integra fornecedores?

Fornecedores terceirizados são obrigados a assinar um Contrato Mestre da Microsoft como parte do processo de integração. Este contrato rege a relação entre a Microsoft e seus fornecedores e garante um gerenciamento consistente das relações com fornecedores. Como parte da integração, os fornecedores se inscrevem no SSPA e devem concluir todos os requisitos aplicáveis antes de serem aprovados para qualquer categoria de processamento de dados. As unidades de negócios da Microsoft só poderão criar inações com fornecedores quando a atividade de processamento de dados para o contrato corresponde às categorias de processamento de dados para as quais o fornecedor foi aprovado.

## <a name="how-does-microsoft-notify-customers-of-changes-to-suppliers-who-process-their-data"></a>Como a Microsoft notifica os clientes sobre alterações em fornecedores que processam seus dados?

De acordo com o Adendo de Proteção de Dados do Serviço Online da Microsoft (DPA), a Microsoft faz compromissos adicionais em relação aos períodos de aviso para a adição de qualquer subprocessador. Os períodos de tempo de aviso dependem do tipo de dados que o subprocessador processará em nome da Microsoft. Conforme indicado no DPA, a Microsoft se compromete a fornecer aviso aos clientes com pelo menos seis meses de antecedência sobre qualquer novo subprocessador que processará os Dados do Cliente. Para quaisquer outros Dados Pessoais, a Microsoft fornecerá pelo menos 30 dias de aviso. O aviso é fornecido pela atualização da Lista [de Subprocessadores](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=926b2cf5-6b6e-43ca-9bc3-f73e961aad5f&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_Subprocessor_List)do Microsoft Online Services.

## <a name="related-external-regulations--certifications"></a>Regulamentações externas relacionadas & certificações

Os serviços online da Microsoft são auditados regularmente para conformidade com regulamentações e certificações externas. Consulte a tabela abaixo para validação de controles relacionados ao gerenciamento de fornecedores.

| **Auditorias externas** | **Section** | **Data do relatório mais recente** |
|:--------------------|:------------|:-----------------------|  
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | CA-3: Interconexões do sistema <br> IA-4: Gerenciamento de identificador <br> PS-6: Acordos de acesso <br> PS-7: Segurança de funcionários de terceiros <br> SA-4: Processo de aquisições <br> SA-9: Serviços do sistema de informações externos <br> SA-12: Proteção da cadeia de fornecimento | 24 de setembro de 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaração de Aplicabilidade](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.15.1: Segurança de informações em relações com fornecedores | 22 de fevereiro de 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaração de Aplicabilidade](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.15.1: Segurança de informações em relações com fornecedores | 22 de fevereiro de 2020 |
| [ISO 27018 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaração de Aplicabilidade](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=43e89534-f48d-42ea-a7a7-3523ff516036&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) |  A.8.1: Divulgação de processamento de PII subcontratado | 24 de dezembro de 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-53: Monitoramento de terceiros | 24 de dezembro de 2020 |

## <a name="resources"></a>Recursos

- [Programa de Garantia e Privacidade de Segurança de Fornecedores](https://www.microsoft.com/procurement/sspa?activetab=pivot1%3aprimaryr6)
