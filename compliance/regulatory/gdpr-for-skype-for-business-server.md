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
ms.openlocfilehash: f0c59e0b4fb6fd80fd13521a3ed4996e787474bc
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51496007"
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
