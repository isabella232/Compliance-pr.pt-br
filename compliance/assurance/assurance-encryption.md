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
hideEdit: true
ms.openlocfilehash: 5e46fdb5ddc3b1b80df0bcadf9054b9353a0dc8e
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/23/2021
ms.locfileid: "53088640"
---
# <a name="encryption-and-key-management-overview"></a>Visão geral de gerenciamento de criptografia e chaves

## <a name="what-role-does-encryption-play-in-protecting-customer-content"></a>Qual função a criptografia desempenha na proteção do conteúdo do cliente?

A maioria dos serviços de nuvem empresarial da Microsoft é multitenente, o que significa que o conteúdo do cliente pode ser armazenado no mesmo hardware físico de outros clientes. Para proteger a confidencialidade do conteúdo do cliente, Microsoft 365 criptografa todos os dados em repouso e em trânsito com alguns dos protocolos de criptografia mais fortes e seguros disponíveis.

A criptografia não é um substituto para controles de acesso forte. Microsoft 365 política de controle de acesso do ZSA (Zero Standing Access) protege o conteúdo do cliente contra acesso não autorizado por funcionários da Microsoft. A criptografia complementa o controle de acesso protegendo a confidencialidade do conteúdo do cliente onde quer que esteja armazenado e impedindo que o conteúdo seja lido enquanto estiver em trânsito entre os sistemas Microsoft 365 ou entre o Microsoft 365 e o cliente.

## <a name="how-does-microsoft-365-encrypt-data-at-rest"></a>Como Microsoft 365 criptografar dados em repouso?

Todo o conteúdo do cliente Microsoft 365 é protegido por uma ou mais formas de criptografia. Os servidores Microsoft usam o BitLocker para criptografar as unidades de disco que contêm conteúdo do cliente no nível de volume. A criptografia fornecida pelo BitLocker protege o conteúdo do cliente em caso de falhas em outros processos ou controles (por exemplo, controle de acesso ou reciclagem de hardware) que podem levar ao acesso físico não autorizado a discos que contenham conteúdo do cliente.

Exchange Online, Microsoft Teams, SharePoint Online e OneDrive for Business também usam a Criptografia de Serviço na camada de aplicativos para criptografar o conteúdo do cliente. A Criptografia de Serviço fornece recursos de proteção e gerenciamento de direitos, além de uma forte proteção de criptografia. Ele também permite a separação entre Windows sistemas operacionais e os dados do cliente armazenados ou processados por esses sistemas operacionais.

## <a name="how-does-microsoft-365-encrypt-data-in-transit"></a>Como Microsoft 365 criptografar dados em trânsito?

Microsoft 365 produtos e serviços usam protocolos de transporte fortes, como o TLS, para impedir que as partes não autorizadas escutam dados do cliente enquanto eles se movem por uma rede. Exemplos de dados em trânsito incluem mensagens de email que estão em processo de entrega, conversas ocorrendo em uma reunião online ou arquivos sendo replicados entre datacenters.

No Microsoft 365, os dados são considerados 'em trânsito' sempre que um dispositivo do usuário está se comunicando com um servidor microsoft ou um servidor Microsoft está se comunicando com outro servidor. Exchange Online, SharePoint Online, Microsoft Teams e Office Online usam TLS para garantir que os dados permaneçam confidenciais enquanto estão em trânsito.

## <a name="how-does-microsoft-365-manage-the-keys-used-for-encryption"></a>Como você Microsoft 365 as chaves usadas para criptografia?

A criptografia forte é tão segura quanto as chaves usadas para criptografar dados. A Microsoft usa seus próprios certificados de segurança para criptografar conexões TLS para dados em trânsito. Para dados em repouso, os volumes protegidos pelo BitLocker são criptografados com uma chave de criptografia de volume total, que é criptografada com uma chave mestra de volume, que, por sua vez, está vinculada ao Módulo de Plataforma Confiável (TPM) no servidor. O BitLocker usa algoritmos compatíveis com FIPS para garantir que as chaves de criptografia nunca sejam armazenadas ou enviadas pelo fio de forma clara.

A Criptografia de Serviço fornece uma camada adicional de criptografia para dados em repouso do cliente em Exchange Online, Microsoft Teams, SharePoint Online e OneDrive for Business. A Criptografia de Serviço oferece aos clientes duas opções para gerenciamento de chaves de criptografia: chaves gerenciadas pela Microsoft ou Chave do Cliente. Ao usar chaves gerenciadas pela Microsoft, Microsoft 365 serviços geram automaticamente e armazenam com segurança as chaves raiz usadas para Criptografia de Serviço.

Os clientes com requisitos para controlar suas próprias chaves de criptografia raiz podem aproveitar a Criptografia de Serviço com a Chave do Cliente. Usando a Chave do Cliente, os clientes podem gerar suas próprias chaves criptográficas usando um HSM (Hardware Service Module) local ou a Azure Key Vault (AKV). As chaves raiz do cliente são armazenadas no AKV, onde podem ser usadas como a raiz de um dos chaveiros que criptografam dados ou arquivos de caixa de correio do cliente. As chaves raiz do cliente só podem ser acessadas indiretamente Microsoft 365 código de serviço para criptografia de dados e não podem ser acessadas diretamente pelos funcionários da Microsoft.

## <a name="related-external-regulations--certifications"></a>Regulamentações externas relacionadas & certificações

Os serviços online da Microsoft são regularmente auditados para conformidade com regulamentações e certificações externas. Consulte a tabela a seguir para validação de controles relacionados à criptografia e gerenciamento de chaves.

| **Auditorias externas** | **Section** | **Data do relatório mais recente** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | SC-8: Confidencialidade e integridade de transmissão <br> SC-13: Uso de criptografia <br> SC-28: Proteção de informações em repouso <br>  | 24 de setembro de 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Instrução of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.10.1: controles criptográficos <br> A.18.1.5: controles criptográficos | Abril de 20, 2021 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Instrução of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.10.1: controles criptográficos <br> A.18.1.5: controles criptográficos | Abril de 20, 2021 |
| [ISO 27018 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Instrução of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=43e89534-f48d-42ea-a7a7-3523ff516036&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.11.6: Criptografia de PII transmitida por redes públicas de transmissão de dados | Abril de 20, 2021 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-44: criptografia de dados em trânsito <br> CA-54: criptografia de dados em repouso <br> CA-62: criptografia de caixa de correio de chave do cliente <br> CA-63: Exclusão de dados de chave do cliente <br> CA-64: Chave do cliente | 24 de dezembro de 2020 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-16: Chaves de criptografia do cliente <br> CUEC-17: Cofre de chaves do cliente <br>  CUEC-18: Rotação da chave do cliente| 24 de dezembro de 2020 |
