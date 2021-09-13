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
ms.openlocfilehash: dc53f42c6aa7ce16e1291538bfad6d63c5a1689d
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/12/2021
ms.locfileid: "59157954"
---
# <a name="encryption-and-key-management-overview"></a>Visão geral de gerenciamento de criptografia e chaves

## <a name="what-role-does-encryption-play-in-protecting-customer-content"></a>Qual função a criptografia desempenha na proteção do conteúdo do cliente?

A maioria dos serviços de nuvem empresarial da Microsoft é multi-locatário, o que significa que o conteúdo do cliente pode ser armazenado no mesmo hardware físico que outros clientes. Para proteger a confidencialidade do conteúdo do cliente, os serviços online da Microsoft criptografam todos os dados em repouso e em trânsito com alguns dos protocolos de criptografia mais fortes e seguros disponíveis.

A criptografia não é um substituto para controles de acesso forte. A política de controle de acesso da Microsoft do ZSA (Zero Standing Access) protege o conteúdo do cliente contra o acesso não autorizado por funcionários da Microsoft. A criptografia complementa o controle de acesso protegendo a confidencialidade do conteúdo do cliente onde quer que esteja armazenado e impedindo que o conteúdo seja lido enquanto estiver em trânsito entre os sistemas de serviços online da Microsoft ou entre os serviços online da Microsoft e o cliente.

## <a name="how-do-microsoft-online-services-encrypt-data-at-rest"></a>Como os serviços online da Microsoft criptografam dados em repouso?

Todo o conteúdo do cliente nos serviços online da Microsoft é protegido por uma ou mais formas de criptografia. Os servidores Microsoft usam o BitLocker para criptografar as unidades de disco que contêm conteúdo do cliente no nível de volume. A criptografia fornecida pelo BitLocker protege o conteúdo do cliente se houver falhas em outros processos ou controles (por exemplo, controle de acesso ou reciclagem de hardware) que podem levar ao acesso físico não autorizado a discos que contenham conteúdo do cliente.

Além da criptografia de nível de volume, os serviços online da Microsoft usam a Criptografia de Serviço na camada do aplicativo para criptografar o conteúdo do cliente. A Criptografia de Serviço fornece recursos de proteção e gerenciamento de direitos, além de uma forte proteção de criptografia. Ele também permite a separação entre Windows sistemas operacionais e os dados do cliente armazenados ou processados por esses sistemas operacionais.

## <a name="how-do-microsoft-online-services-encrypt-data-in-transit"></a>Como os serviços online da Microsoft criptografam dados em trânsito?

Os serviços online da Microsoft usam protocolos de transporte fortes, como o TLS, para impedir que as partes não autorizadas escutam dados do cliente enquanto eles se movem por uma rede. Exemplos de dados em trânsito incluem mensagens de email que estão em processo de entrega, conversas ocorrendo em uma reunião online ou arquivos sendo replicados entre datacenters.

Para os serviços online da Microsoft, os dados são considerados 'em trânsito' sempre que um dispositivo do usuário está se comunicando com um servidor Microsoft ou um servidor Microsoft está se comunicando com outro servidor.

## <a name="how-do-microsoft-online-services-manage-the-keys-used-for-encryption"></a>Como os serviços online da Microsoft gerenciam as chaves usadas para criptografia?

A criptografia forte é tão segura quanto as chaves usadas para criptografar dados. A Microsoft usa seus próprios certificados de segurança para criptografar conexões TLS para dados em trânsito. Para dados em repouso, os volumes protegidos pelo BitLocker são criptografados com uma chave de criptografia de volume total, que é criptografada com uma chave mestra de volume, que, por sua vez, está vinculada ao Módulo de Plataforma Confiável (TPM) no servidor. O BitLocker usa algoritmos compatíveis com FIPS para garantir que as chaves de criptografia nunca sejam armazenadas ou enviadas pelo fio de forma clara.

A Criptografia de Serviço fornece outra camada de criptografia para dados do cliente em repouso, fornecendo aos clientes duas opções para gerenciamento de chaves de criptografia: chaves gerenciadas pela Microsoft ou Chave do Cliente. Ao usar chaves gerenciadas pela Microsoft, os serviços online da Microsoft geram automaticamente e armazenam com segurança as chaves raiz usadas para Criptografia de Serviço.

Os clientes com requisitos para controlar suas próprias chaves de criptografia raiz podem usar a Criptografia de Serviço com a Chave do Cliente. Usando a Chave do Cliente, os clientes podem gerar suas próprias chaves criptográficas usando um HSM (Hardware Service Module) local ou a Azure Key Vault (AKV). As chaves raiz do cliente são armazenadas no AKV, onde podem ser usadas como a raiz de um dos chaveiros que criptografam dados ou arquivos de caixa de correio do cliente. As chaves raiz do cliente só podem ser acessadas indiretamente pelo código de serviço online da Microsoft para criptografia de dados e não podem ser acessadas diretamente pelos funcionários da Microsoft.

## <a name="related-external-regulations--certifications"></a>Regulamentações externas relacionadas & certificações

Os serviços online da Microsoft são regularmente auditados para conformidade com regulamentações e certificações externas. Consulte a tabela a seguir para validação de controles relacionados à criptografia e gerenciamento de chaves.

### <a name="azure-and-dynamics-365"></a>Azure e Dynamics 365

| **Auditorias externas** | **Section** | **Data do relatório mais recente** |
|:--------------------|:------------|:-----------------------|
| [ISO 27001/27002](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Instrução of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7af5304-3a31-40e6-9abb-e26352305d41&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.10.1: controles criptográficos <br> A.18.1.5: controles criptográficos | 2 de dezembro de 2020 |
| [ISO 27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Instrução of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a3bca0ac-867d-4204-b66b-13665f5f1e8d&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=25718a8a-f34d-41e1-a95a-c49246508787&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.10.1: controles criptográficos <br> A.18.1.5: controles criptográficos | 2 de dezembro de 2020 |
| [ISO 27018](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Instrução of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificação](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=56904fc3-0942-4ff5-9eef-7cabc751a25c&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.11.6: Criptografia de PII transmitida por redes públicas de transmissão de dados | 2 de dezembro de 2020 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b8721ebd-af20-42fe-b22f-8332b0a19517&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=234a0f57-83c1-4afc-a586-a0e7a59592f7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=75c8cbf6-e456-473c-a05e-34fea888ec2a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | DS-1: Armazenamento seguro de certificados e chaves criptográficos <br> DS-2: Os dados do cliente são criptografados em trânsito <br> DS-3: Comunicação interna de componentes do Azure criptografados em trânsito <br> DS-4: controles e procedimentos criptográficos | 31 de março de 2021 |

### <a name="office-365"></a>Office 365

| **Auditorias externas** | **Section** | **Data do relatório mais recente** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP](https://compliance.microsoft.com/compliancemanager) | SC-8: Confidencialidade e integridade de transmissão <br> SC-13: Uso de criptografia <br> SC-28: Proteção de informações em repouso <br>  | 24 de setembro de 2020 |
| [ISO 27001/27002/27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Instrução of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.10.1: controles criptográficos <br> A.18.1.5: controles criptográficos | Abril de 20, 2021 |
| [ISO 27018](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Instrução of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.11.6: Criptografia de PII transmitida por redes públicas de transmissão de dados | Abril de 20, 2021 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-44: criptografia de dados em trânsito <br> CA-54: criptografia de dados em repouso <br> CA-62: criptografia de caixa de correio de chave do cliente <br> CA-63: Exclusão de dados de chave do cliente <br> CA-64: Chave do cliente | 24 de dezembro de 2020 |
| [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-16: Chaves de criptografia do cliente <br> CUEC-17: Cofre de chaves do cliente <br>  CUEC-18: Rotação da chave do cliente| 24 de dezembro de 2020 |
