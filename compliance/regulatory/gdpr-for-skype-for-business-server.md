---
title: RGPD para Skype for Business Server
description: Saiba mais sobre como atender aos requisitos de RGPD no Skype for Business Server e no Lync Server.
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
hideEdit: true
ms.openlocfilehash: 945c9a90b117aca97b5b1af56e802e62bed91c9f700cddb595fc32bbe325559e
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/05/2021
ms.locfileid: "54287960"
---
# <a name="gdpr-for-skype-for-business-server-and-lync-server"></a>RGPD para Skype for Business Server e Lync Server

A maioria dos dados do Skype for Business Server e do Lync Server é armazenada no Exchange Server. Isso inclui:

-   Histórico de conversas

-   Transcrições e notificações da caixa postal

-   Convites de reuniões

Use os procedimentos descritos para [RGPD para Exchange Server](gdpr-for-exchange-server.md) para localizar, exportar ou excluir esses tipos de dados para solicitações de RGPD.

Listas de contatos são armazenadas no banco de dados do SQL Server. Elas podem ser exportadas das seguintes maneiras:

-   Os usuários finais podem exportar os contatos por conta própria clicando no cabeçalho do grupo com o botão direito do mouse e selecionando Copiar. Isso copiará os contatos para a área de transferência, e eles poderão ser colados em qualquer aplicativo.

-   Você pode usar o cmdlet [Export-CsUserData](/powershell/module/skype/export-csuserdata) para exportar esses dados.

Conteúdo carregado em reuniões (como arquivos do PowerPoint ou folhetos) ou conteúdo gerado em uma reunião (como quadro de comunicações, votações ou sessões de perguntas e respostas) armazenado no servidor de dados. Também é possível exportar esse conteúdo se os usuários finais entrarem novamente em qualquer reunião que não tenha expirado e baixarem o conteúdo carregado ou fizerem capturas de tela no caso do conteúdo gerado.

Reuniões do MeetNow que não estão no Calendário do Exchange e na Lista de Contatos e os direitos de contado (familiares, colegas de trabalho etc.) se encontram no banco de dados do usuário. No Lync Server 2013 e em versões posteriores, você poderá usar o cmdlet [Export-CsUserData](/powershell/module/skype/export-csuserdata) para exportar esses dados.
