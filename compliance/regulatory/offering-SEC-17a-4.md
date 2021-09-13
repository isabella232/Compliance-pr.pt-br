---
title: Securities and Exchange Commission (SEC) Rule 17a-4(f) United States
description: Uma empresa de avaliação independente validou que o Azure e o Office 365 podem ajudar as empresas financeiras a atender aos requisitos de retenção e armazenamento imutáveis da Regra SEC 17a-4(f).
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
ms.openlocfilehash: 50c44b6801e15af02bf4bfa4f4d46758b7a6c7a8
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/12/2021
ms.locfileid: "59158403"
---
# <a name="securities-and-exchange-commission-sec-rule-17a-4f-united-states"></a>Securities and Exchange Commission (SEC) Rule 17a-4(f) United States

## <a name="about-sec-rule-17a-4f"></a>Sobre a Regra SEC 17a-4(f)

A Comissão de Títulos e Exchange dos EUA [(SEC)](https://www.sec.gov/) é uma agência independente do governo federal dos EUA e o supervisor principal e regulador dos mercados de valores mobiliários dos EUA. Ele exerce autoridade de aplicação sobre leis de valores mobiliários federais, propõe novas regras de valores mobiliários e supervisiona a regulamentação de mercado do setor de valores mobiliários.

A SEC define requisitos rigorosos e explícitos para entidades regulamentadas que optam por reter livros e registros em mídia de armazenamento eletrônico. Ele [estabeleceu 17 CFR 240.17a-3](https://www.govinfo.gov/app/details/CFR-2012-title17-vol3/CFR-2012-title17-vol3-sec240-17a-3) e [17 CFR 240.17a-4](https://www.ecfr.gov/cgi-bin/text-idx?mc=true&node=pt17.4.240&rgn=div5#se17.4.240_117a_64) para regular a manutenção de registros, incluindo períodos de retenção, para operadores de agente de valores mobiliários. Posteriormente, [a](https://www.sec.gov/rules/interp/34-47806.htm) SEC alterou o parágrafo 17 CFR 240.17a-4 (f), emissão de duas versões interpretativas expressamente para permitir que livros e registros sejam mantidos na mídia de armazenamento eletrônico, desde que determinadas condições sejam atendidas.

Um sistema de armazenamento eletrônico atende a essas condições se impedir a alteração ou a eliminação de registros para o período de retenção necessário. Os períodos de retenção variam de três a seis anos com base nos tipos de registro, com a acessibilidade imediata ordenada para os dois primeiros anos. Além disso, uma das versões interpretativas exige que o sistema de armazenamento seja capaz de reter registros além do período de retenção estabelecido pela SEC para cumprir intimações, suspensão legal ou outros requisitos desse tipo.

## <a name="microsoft-and-sec-rule-17a-4f"></a>Regra microsoft e SEC 17a-4(f)

Os clientes de serviços financeiros, que representam um dos setores mais fortemente regulamentados do mundo, estão sujeitos a disposições complexas, como a retenção de transações financeiras e a comunicação relacionada em um estado não a apagavel e não modificável. Entre as mais prescritivas está a Regra 17a-4(f) da Sec (Comissão de Segurança e Exchange) dos EUA que estipula requisitos rigorosos para entidades regulamentadas que optam por reter livros e registros em mídia de armazenamento eletrônico. Os registros armazenados devem ser à prova de adulteração sem capacidade de alterá-los ou excluí-los até depois do período de retenção designado.

Microsoft Azure O blob imutável Armazenamento bloqueio de política e Microsoft Office 365 com o Bloqueio de Preservação podem ajudar as instituições financeiras a atender aos requisitos de armazenamento imutáveis da Regra DA SEC 17a-4(f).

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Plataformas e serviços em nuvem no escopo da Microsoft

- [Azure](https://gallery.technet.microsoft.com/Overview-of-Azure-c1be3942)
- [Office 365](https://aka.ms/Office365ComplianceOfferings)

## <a name="independent-assessments"></a>Avaliações independentes

Para avaliar o Azure e Office 365 conformidade com a Regra DA SEC 17a-4(f), a Microsoft reteve uma empresa de avaliação independente especializada em gerenciamento de registros e governança de informações, Cohasset Associates.

### <a name="azure"></a>Azure

[O armazenamento imutável](/azure/storage/blobs/storage-blob-immutable-storage) para o armazenamento do Blob do Azure permite que os usuários armazenem registros críticos para os negócios em um estado de gravação depois de ler muitos (WORM). Esse estado torna os dados não apagados e não modificáveis para um intervalo especificado pelo usuário. Durante o intervalo de retenção, os blobs podem ser criados e lidos, mas não podem ser modificados ou excluídos. Esses recursos do armazenamento imutável do Azure podem ajudar os clientes a atender aos requisitos de retenção de registros.

A Microsoft reteve uma empresa independente de avaliação de terceiros especializada em gerenciamento de registros e governança de informações para avaliar o armazenamento imutável para a conformidade do armazenamento do Blob do Azure com os requisitos da Regra SEC 17a-4(f). O relatório resultante *[Avaliação de Cohasset: Microsoft Azure Armazenamento WORM](https://azure.microsoft.com/resources/azure-immutable-storage-assessment-for-sec-17a-4f-by-cohasset/)* está disponível para os clientes.

É a opinião do avaliador de que o Azure Armazenamento com o armazenamento imutável para o recurso blobs do *Azure* e a opção de política com base no tempo bloqueado mantém Blobs (registros) baseados em tempo em um não-apagamento e não-rew Formatoritável e atende aos requisitos de armazenamento relevantes da Regra SEC 17a-4(f), da [Regra FINRA 4511(c)](offering-FINRA-4511.md)e dos requisitos baseados em princípios da Regra [CFTC 1.31(c)-(d)](offering-cftc-1-31-us.md). 

Após a solicitação, a Microsoft também fornecerá uma carta de *90* dias necessária para atender aos requisitos da SEC 17a-4(f)(2) para que os clientes notifiquem sua autoridade de exame designada pelo menos 90 dias antes de empregar mídia de armazenamento eletrônico. Conforme indicado nos regulamentos, "o membro, agente ou revendedor deve fornecer sua própria representação ou uma do fornecedor médio de armazenamento ou de outro terceiro com conhecimento apropriado de que a mídia de armazenamento selecionada atende às condições definidas neste parágrafo (f)(2)." Para obter o Atestado de Armazenamento Serviços de Mídia da Microsoft para a Regra 17a-4 da SEC, os clientes com um plano de suporte do [Azure](https://azure.microsoft.com/support/plans/) podem criar um tíquete de suporte no portal do Azure e solicitar *a* carta de atestado para [a](https://azure.microsoft.com/support/create-ticket/) Regra SEC 17a-4. Neste documento, a Microsoft fornece garantias relevantes para os requisitos da SEC 17a-4(f)(2).

### <a name="office-365"></a>Office 365

Para requisitos da [SEC 17a-4(f),](/microsoft-365/compliance/retention-regulatory-requirements#sec-17a-4f-finra-4511c-and-cftc-131c-d) a Cohasset validou que o Microsoft 365 inclui recursos de arquivamento que permitem que clientes regulamentados, incluindo corretores, armazenem dados de maneira que os ajude a cumprir os requisitos sec para retenção de registros. Os recursos de retenção Microsoft 365 ajudam a preservar uma ampla variedade de dados, incluindo email, caixa postal, documentos compartilhados, mensagens instantâneas e dados de terceiros. Em particular, o arquivamento no Microsoft 365 permite aos clientes definir políticas de retenção de mensagens globais ou granulares para armazenar dados por um período definido e além em um formato não regravável e não-reescrita.

## <a name="audits-reports-and-certificates"></a>Auditorias, relatórios e certificados

### <a name="azure--sec-rule-17"></a>Azure & Regra 17 da SEC

- [SEC 17a-4(f) & Avaliação de Conformidade do CFTC 1.31 (c-d) do Azure Armazenamento](https://azure.microsoft.com/resources/azure-immutable-storage-assessment-for-sec-17a-4f-by-cohasset/)

O *Atestado de* Armazenamento Serviços de Mídia da Microsoft para [a](https://azure.microsoft.com/support/create-ticket/) Regra SEC 17a-4 pode ser solicitado criando um tíquete de suporte com suporte [do Azure.](https://azure.microsoft.com/support/plans/) Nesta carta de atestado, a Microsoft oferece garantias para ajudar os clientes a cumprir os requisitos da SEC 17a-4(f)(2).

### <a name="office-365--sec-rule-17"></a>Office 365 & SEC Regra 17

- [Avaliação de Conformidade da SEC 17a-4(f): Centro de Conformidade do Microsoft Security & com SharePoint, OneDrive, Teams, Exchange e Skype for Business](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=2dc92867-5f83-49d8-ad04-9e7295c9e40e&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)

## <a name="how-to-implement"></a>Como implementar

### <a name="financial-services-regulation"></a>Regulamentação de serviços financeiros

Mapa de conformidade dos principais princípios regulatórios dos EUA para computação em nuvem e serviços online da Microsoft. [Saiba mais](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=5b483567-00b0-4d86-96ae-ee887dadb61c&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_Compliance_Guides)

### <a name="risk-assessment--compliance-guide"></a>Guia de Conformidade & Avaliação de Riscos

Crie um modelo de governança para avaliação de risco dos serviços de nuvem da Microsoft e notificação de regulamentação. [Saiba mais](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=edee9b14-3661-4a16-ba83-c35caf672bd7&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers)

### <a name="financial-use-cases"></a>Casos de uso financeiro

Use visão geral de caso, tutoriais e outros recursos para criar soluções do Azure para serviços financeiros. [Saiba mais](/azure/industry/financial/)

## <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Usar o Gerenciador de Conformidade da Microsoft para avaliar o risco

O[Gerenciador de Conformidade da Microsoft](/microsoft-365/compliance/compliance-manager) é um recurso no [Centro de conformidade do Microsoft 365](/microsoft-365/compliance/microsoft-365-compliance-center) para ajudá-lo a entender a postura de conformidade da sua organização e executar ações para ajudar a reduzir os riscos. O Gerenciador de Conformidade oferece um modelo premium para criar uma avaliação para essa regulamentação. Encontre o modelo na página **modelos de avaliação** no Gerenciador de Conformidade. Saiba como [criar avaliações no Compliance Manager](/microsoft-365/compliance/compliance-manager-assessments).

## <a name="resources"></a>Recursos

- [Documentação de conformidade do Azure](/azure/compliance/)
- [O Azure habilita um mundo de conformidade](https://azure.microsoft.com/resources/azure-enables-a-world-of-compliance/)
- [Securities and Exchange Commission](https://www.sec.gov/) (SEC) [Rule 17a-4](https://www.sec.gov/rules/final/34-38245.txt)
- [Recursos de serviços financeiros da Microsoft Cloud](https://servicetrust.microsoft.com/viewpage/financialservicesoverview)
- [Programa de conformidade de serviços financeiros da Microsoft Cloud](https://aka.ms/FSCP-Print)
- [Mapa de conformidade de princípios regulatórios de computação em nuvem e serviços online da Microsoft](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=5b483567-00b0-4d86-96ae-ee887dadb61c&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_Compliance_Guides)
- [Guia de avaliação e conformidade de riscos para instituições financeiras no Microsoft Cloud](https://azure.microsoft.com/resources/risk-assessment-and-compliance-guide-for-financial-institutions-in-the-microsoft-cloud-/)
- [Casos de uso do setor de Serviços Financeiros](/azure/industry/financial/)
- [Arquivamento em Microsoft Office 365, Retenção de Dados e Regra 17a-4](https://www.microsoft.com/microsoft-365/blog/2015/11/10/office-365-exchange-online-archiving-now-meets-sec-rule-17a-4-requirements/)
