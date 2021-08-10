---
title: RGPD para servidores do Office
description: Aprenda a resolver Regulamentações Gerais de Proteção de Dados (RGPD) para o SharePoint Server local.
f1.keywords:
- NOCSH
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
titleSuffix: Microsoft GDPR
ms.collection: MS-Compliance
ms.custom: seo-marvel-apr2020
hideEdit: true
ms.openlocfilehash: 071b3d63372d2fb2c2d730c4f946ae469007f4c25f6ae0e4d07826d04a481044
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/05/2021
ms.locfileid: "54293508"
---
# <a name="gdpr-for-office-on-premises-servers"></a>RGPD para servidores locais do Office

O RGPD (Regulamento Geral sobre a Proteção de Dados) apresenta os requisitos para as organizações protegerem dados pessoais adequadamente e atender adequadamente às solicitações de titulares de dados. Esta série de artigos fornece abordagens recomendadas para cargas de trabalho locais:

- [SharePoint Server](gdpr-for-sharepoint-server.md)

- [Exchange Server](gdpr-for-exchange-server.md)

- [Skype for Business Server](gdpr-for-skype-for-business-server.md)

- [Project Server](gdpr-for-project-server.md)

- [Servidor do Office Web Apps e Servidor do Office Online](gdpr-for-office-online-server.md)

- [Compartilhamentos de arquivos locais](gdpr-for-on-premises-file-shares.md)

Para obter mais informações sobre o RGPD e como a Microsoft pode ajudar você, confira a [Central de Confiabilidade da Microsoft](https://www.microsoft.com/trust-center/privacy/gdpr-overview
).

Antes de trabalhar com dados locais, consulte suas equipes de conformidade e jurídica para buscar orientações e saber mais sobre os esquemas e as abordagens existentes de classificação para trabalhar com dados pessoais. A Microsoft fornece recomendações para desenvolver e estender esquemas de classificação no Microsoft GDPR Data Discovery Toolkit em [https://aka.ms/gdprpartners](<https://aka.ms/gdprpartners>). Esse kit de ferramentas também descreve abordagens para mover dados locais para a nuvem, onde você pode usar recursos de governança de dados mais sofisticados, se desejar. Os artigos nesta seção fornecem recomendações para os dados destinados a permanecerem no local.

A ilustração a seguir lista os recursos recomendados para usar em cada uma dessas cargas de trabalho para descobrir, classificar, proteger e monitorar dados pessoais. Confira os artigos desta seção para saber mais.

![Diagrama descrevendo os recursos para descobrir, classificar, proteger e monitorar dados pessoais entre cargas de trabalho](../media/gdpr-for-office-servers-image1.png)

## <a name="illustration-description"></a>Descrição da ilustração

Para maior acessibilidade, a tabela a seguir fornece os mesmos exemplos da ilustração.

****

|Ação|Compartilhamentos de arquivos do Windows Server|SharePoint Server|Exchange Server|Skype for Business|Project Server|
|---|---|---|---|---|---|
|Descobrir|Scanner da Proteção de Informações do Azure<sup>\*</sup>|Centro de Pesquisa ou de Descoberta Eletrônica (depois que os dados forem classificados) <br/><br/> Scanner da Proteção de Informações do Azure<sup>\*</sup>|Portal de Descoberta Eletrônica do Exchange|Portal de Descoberta Eletrônica do Exchange|Scripts SQL para descobrir e exportar|
|Classificar|Scanner da Proteção de Informações do Azure<sup>\*</sup> <br/><br/> Tipos de informações confidenciais do Office 365|Scanner da Proteção de Informações do Azure<sup>\*</sup> <br/><br/> Tipos de informações confidenciais do Office 365|Marcas e políticas de retenção do Exchange|Marcas e políticas de retenção do Exchange||
|Proteger||Regras de prevenção contra perda de dados do Exchange Server <br/><br/> Permissões, proteção do IRM para bibliotecas|Regras de prevenção contra perda de dados do Exchange Server <br/><br/> Integração do IRM com o Exchange Server|||
|Monitorar|Integrar logs com ferramentas SIEM|Integrar logs com ferramentas SIEM|Integrar logs com ferramentas SIEM|Integrar logs com ferramentas SIEM|Integrar logs com ferramentas SIEM|
|

<sup>\*</sup> Nota que a proteção criptografa o arquivo. Consequentemente, o Microsoft Office SharePoint Online Server não consegue encontrar os tipos de informações confidenciais em arquivos protegidos.
