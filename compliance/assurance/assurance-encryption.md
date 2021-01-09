---
title: Visão geral de gerenciamento de criptografia e chaves
description: Saiba mais sobre criptografia e gerenciamento de chaves no Microsoft 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: ca13c5dfb229acd46ef0dd027b537afc2ac20b5a
ms.sourcegitcommit: 7a5b6bc58fc4613b38f3fda20aebee5cec6a5730
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "49787340"
---
# <a name="encryption-and-key-management-overview"></a>Visão geral de gerenciamento de criptografia e chaves

## <a name="what-role-does-encryption-play-in-protecting-customer-content"></a>Qual é a função da criptografia na proteção do conteúdo do cliente?

A maioria dos serviços de nuvem de negócios da Microsoft é multi-intencional, o que significa que o conteúdo do cliente pode ser armazenado no mesmo hardware físico de outros clientes. Para proteger a confidencialidade do conteúdo do cliente, o Microsoft 365 criptografa todos os dados em repouso e em trânsito com alguns dos protocolos de criptografia mais seguros disponíveis.

A criptografia não substitui controles de acesso fortes. A política de controle de acesso do ZSA (Acesso Zero Permanente) do Microsoft 365 protege o conteúdo do cliente contra acesso não autorizado por funcionários da Microsoft. A criptografia complementa o controle de acesso, protegendo a confidencialidade do conteúdo do cliente onde quer que ele esteja armazenado e evitando que o conteúdo seja lido enquanto estiver em trânsito entre os sistemas do Microsoft 365 ou entre o Microsoft 365 e o cliente.

## <a name="how-does-microsoft-365-encrypt-data-at-rest"></a>Como o Microsoft 365 criptografa dados em repouso?

Todo o conteúdo do cliente no Microsoft 365 é protegido por uma ou mais formas de criptografia. Os servidores da Microsoft usam o BitLocker para criptografar as unidades de disco que contêm conteúdo do cliente no nível do volume. A criptografia fornecida pelo BitLocker protege o conteúdo do cliente em caso de falhas em outros processos ou controles (por exemplo, controle de acesso ou reciclagem de hardware) que pode levar a acesso físico não autorizado a discos que contêm conteúdo do cliente.

O Exchange Online, o Microsoft Teams, o SharePoint Online e o OneDrive for Business também usam a Criptografia de Serviço na camada de aplicativos para criptografar o conteúdo do cliente. A Criptografia de Serviço fornece recursos de proteção e gerenciamento de direitos sobre a forte proteção de criptografia. Ele também permite a separação entre sistemas operacionais Windows e os dados do cliente armazenados ou processados por esses sistemas operacionais.

## <a name="how-does-microsoft-365-encrypt-data-in-transit"></a>Como o Microsoft 365 criptografa dados em trânsito?

Os produtos e serviços do Microsoft 365 usam protocolos de transporte fortes, como TLS, para impedir que terceiros não autorizados a espionagem dados do cliente enquanto ele se move pela rede. Exemplos de dados em trânsito incluem mensagens de email que estão em processo de entrega, conversas ocorrendo em uma reunião online ou arquivos replicados entre datacenters.

No Microsoft 365, os dados são considerados 'em trânsito' sempre que um dispositivo do usuário está se comunicando com um servidor da Microsoft ou com um servidor da Microsoft está se comunicando com outro servidor. O Exchange Online, o SharePoint Online, o Microsoft Teams e o Office Online usam o TLS para garantir que os dados permaneçam confidenciais enquanto estão em trânsito.

## <a name="how-does-microsoft-365-manage-the-keys-used-for-encryption"></a>Como o Microsoft 365 gerencia as chaves usadas para criptografia?

A criptografia forte só é tão segura quanto as chaves usadas para criptografar dados. A Microsoft usa seus próprios certificados de segurança para criptografar conexões TLS para dados em trânsito. Para dados em repouso, os volumes protegidos pelo BitLocker são criptografados com uma chave de criptografia de volume completa, que é criptografada com uma chave mestra de volume, que, por sua vez, está vinculada ao Trusted Platform Module (TPM) no servidor. O BitLocker usa algoritmos compatíveis com FIPS para garantir que as chaves de criptografia nunca sejam armazenadas ou enviadas pela transmissão sem criptografia.

A Criptografia de Serviço fornece uma camada adicional de criptografia para dados em repouso do cliente no Exchange Online, Microsoft Teams, SharePoint Online e OneDrive for Business. A Criptografia de Serviço oferece aos clientes duas opções de gerenciamento de chave de criptografia: chaves gerenciadas pela Microsoft ou Chave do Cliente. Ao usar chaves gerenciadas pela Microsoft, os serviços do Microsoft 365 geram automaticamente e armazenam com segurança as chaves raiz usadas para a Criptografia de Serviço.

Os clientes com requisitos para controlar suas próprias chaves de criptografia raiz podem aproveitar a Criptografia de Serviço com a Chave do Cliente. Usando a Chave do Cliente, os clientes podem gerar suas próprias chaves criptográficas usando um HSM (Módulo de Serviço de Hardware) local ou AZure Key Vault (AKV). As chaves raiz do cliente são armazenadas em AKV, onde podem ser usadas como raiz de um dos chaves que criptografam dados ou arquivos da caixa de correio do cliente. As chaves raiz do cliente só podem ser acessadas indiretamente pelo código de serviço do Microsoft 365 para criptografia de dados e não podem ser acessadas diretamente por funcionários da Microsoft.

## <a name="related-external-regulations--certifications"></a>Regulamentações externas relacionadas & certificações

Os serviços online da Microsoft são auditados regularmente para conformidade com regulamentações e certificações externas. Consulte a tabela a seguir para validação de controles relacionados à criptografia e ao gerenciamento de chaves.

| **Auditorias externas** | **Section** | **Data do relatório mais recente** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | SC-8: Confidencialidade e integridade da transmissão <br> SC-13: Uso de criptografia <br> SC-28: Proteção de informações em repouso <br>  | 24 de setembro de 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaração de Aplicabilidade](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.10.1: Controles criptográficos <br> A.18.1.5: Controles criptográficos | 22 de fevereiro de 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaração de Aplicabilidade](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.10.1: Controles criptográficos <br> A.18.1.5: Controles criptográficos | 22 de fevereiro de 2020 |
| [ISO 27018 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaração de Aplicabilidade](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=43e89534-f48d-42ea-a7a7-3523ff516036&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.11.6: Criptografia de PII transmitida por redes públicas de transmissão de dados | 22 de fevereiro de 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-44: Criptografia de dados em trânsito <br> CA-54: criptografia de dados em repouso <br> CA-62: Criptografia de caixa de correio de chave do cliente <br> CA-63: Exclusão de dados da chave do cliente <br> CA-64: Chave do cliente | 24 de dezembro de 2020 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-16: Chaves de criptografia do cliente <br> CUEC-17: Cofre de chaves do cliente <br>  CUEC-18: rotação de chaves do cliente| 24 de dezembro de 2020 |
