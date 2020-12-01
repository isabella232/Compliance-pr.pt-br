---
title: Visão geral de gerenciamento de chaves e criptografia
description: Saiba mais sobre o gerenciamento de chaves e criptografia no Microsoft 365
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
ms.openlocfilehash: 96a3871657dc1e6021949ca9fc2376df382fe15b
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/30/2020
ms.locfileid: "49505744"
---
# <a name="encryption-and-key-management-overview"></a>Visão geral de gerenciamento de chaves e criptografia

## <a name="what-role-does-encryption-play-in-protecting-customer-content"></a>Qual função a criptografia exerce na proteção do conteúdo do cliente?

A maioria dos serviços do Microsoft Business Cloud é multilocatário, o que significa que o conteúdo do cliente pode ser armazenado no mesmo hardware físico que outros clientes. Para proteger a confidencialidade do conteúdo do cliente, a Microsoft 365 criptografa todos os dados em repouso e em trânsito com alguns dos protocolos de criptografia mais fortes e seguros disponíveis.

A criptografia não é um substituto para os controles de acesso seguro. A política de controle de acesso de zero (ZSA) do Microsoft 365 protege o conteúdo do cliente contra o acesso não autorizado por funcionários da Microsoft. A criptografia complementa o controle de acesso, protegendo a confidencialidade do conteúdo do cliente onde quer que ele esteja armazenado e impedindo que o conteúdo seja lido enquanto estiver em trânsito entre os sistemas Microsoft 365 ou entre o Microsoft 365 e o cliente.

## <a name="how-does-microsoft-365-encrypt-data-at-rest"></a>Como a Microsoft 365 criptografa dados em repouso?

Todo o conteúdo do cliente no Microsoft 365 é protegido por uma ou mais formas de criptografia. Os servidores da Microsoft usam o BitLocker para criptografar as unidades de disco que contêm o conteúdo do cliente no nível do volume. A criptografia fornecida pelo BitLocker protege o conteúdo do cliente em caso de interrupções em outros processos ou controles (por exemplo, controle de acesso ou reciclagem de hardware) que podem levar a acesso físico não autorizado a discos que contêm conteúdo do cliente.

O Exchange Online, o Microsoft Teams, o SharePoint Online e o OneDrive for Business também usam a criptografia de serviço na camada de aplicativo para criptografar o conteúdo do cliente. A criptografia de serviço fornece recursos de gerenciamento e proteção de direitos à parte superior da proteção de criptografia forte. Ele também permite a separação entre os sistemas operacionais Windows e os dados do cliente armazenados ou processados por esses sistemas operacionais.

## <a name="how-does-microsoft-365-encrypt-data-in-transit"></a>Como a Microsoft 365 criptografa dados em trânsito?

Os produtos e serviços do Microsoft 365 usam protocolos de transporte fortes, como o TLS, para impedir que partes não autorizadas sejam interceptadas em dados do cliente enquanto se movimenta por uma rede. Exemplos de dados em trânsito incluem mensagens de email que estão no processo de entrega, conversas em uma reunião online ou arquivos que estão sendo replicados entre os data centers.

No Microsoft 365, os dados são considerados ' em trânsito ' sempre que o dispositivo de um usuário está se comunicando com um servidor Microsoft ou um servidor Microsoft está se comunicando com outro servidor. O Exchange Online, o SharePoint Online, o Microsoft Teams e o Office Online usam o TLS para garantir que os dados permaneçam confidenciais enquanto estão em trânsito.

## <a name="how-does-microsoft-365-manage-the-keys-used-for-encryption"></a>Como a Microsoft 365 gerencia as chaves usadas para criptografia?

A criptografia forte é tão segura quanto as chaves usadas para criptografar dados. A Microsoft usa seus próprios certificados de segurança para criptografar conexões de TLS para dados em trânsito. Para dados em repouso, os volumes protegidos por BitLocker são criptografados com uma chave de criptografia de volume completo, que é criptografada com uma chave mestra de volume, que, por sua vez, é associada ao TPM (módulo de plataforma confiável) no servidor. O BitLocker usa algoritmos compatíveis com FIPS para garantir que as chaves de criptografia nunca sejam armazenadas ou enviadas pela conexão.

A criptografia de serviço fornece uma camada adicional de criptografia para os dados do cliente em repouso no Exchange Online, no Microsoft Teams, no SharePoint Online e no OneDrive for Business. A criptografia de serviço oferece aos clientes duas opções de gerenciamento de chave de criptografia: chaves gerenciadas pela Microsoft ou chave do cliente. Ao usar chaves gerenciadas pela Microsoft, os serviços do Microsoft 365 geram e armazenam com segurança automaticamente as chaves raiz usadas para a criptografia de serviço.

Os clientes com requisitos para controlar suas próprias chaves de criptografia raiz podem aproveitar a criptografia de serviço com a chave do cliente. Usando a chave do cliente, os clientes podem gerar suas próprias chaves criptográficas usando um módulo de serviço de hardware local (HSM) ou o Azure Key Vault (AKV). As chaves raiz do cliente são armazenadas no AKV, onde podem ser usadas como a raiz de um dos cadeias de chaves que criptografam os arquivos ou dados de caixa de correio do cliente. As chaves raiz do cliente podem ser acessadas indiretamente pelo código de serviço do Microsoft 365 para criptografia de dados e não podem ser acessadas diretamente por funcionários da Microsoft.

## <a name="related-external-regulations--certifications"></a>Normas externas relacionadas & certificações

Os serviços online da Microsoft são auditados regularmente para fins de conformidade com regulamentos externos e certificações. Consulte a tabela a seguir para validação de controles relacionados a criptografia e gerenciamento de chaves.

| **Auditorias externas** | **Section** | **Data do relatório mais recente** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | SC-8: confidencialidade e integridade da transmissão <br> SC-13: uso de criptografia <br> SC-28: proteção de informações em repouso <br>  | 24 de setembro de 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaração de aplicabilidade](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 10.1: controles de criptografia <br> A. 18.1.5: controles de criptografia | 22 de fevereiro de 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaração de aplicabilidade](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 10.1: controles de criptografia <br> A. 18.1.5: controles de criptografia | 22 de fevereiro de 2020 |
| [ISO 27018 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Declaração de aplicabilidade](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=43e89534-f48d-42ea-a7a7-3523ff516036&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 11.6: criptografia de PII transmitidas por redes de transmissão de dados públicos | 22 de fevereiro de 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | AC-44: criptografia de dados em trânsito <br> AC-54: criptografia de dados em repouso <br> AC-62: criptografia de caixa de correio de chave do cliente <br> AC-63: exclusão de dados de chave do cliente <br> AC-64: chave do cliente | 30 de setembro de 2019 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=9df8b99b-96ce-49a9-bff4-268031dcc9a6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CUEC-16: chaves de criptografia do cliente <br> CUEC-17: cofre de chave do cliente <br>  CUEC-18: rotação de chave do cliente| 30 de setembro de 2019 |
