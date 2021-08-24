---
title: RGPD para compartilhamentos de arquivos locais
description: Aprenda a resolver os requisitos gerais de RGPD (Regulamentações Gerais de Proteção de Dados) em compartilhamentos de arquivos locais do Windows Server.
f1.keywords:
- NOCSH
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: high
titleSuffix: Microsoft GDPR
ms.custom: seo-marvel-apr2020
ms.collection: MS-Compliance
hideEdit: true
ms.openlocfilehash: 9c281b6096512f65f20286948addc32127278b98
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2021
ms.locfileid: "58482324"
---
# <a name="gdpr-for-on-premises-windows-server-file-shares"></a>RGPD para compartilhamentos de arquivos no Windows Server local

A abordagem básica recomendada para compartilhamentos de arquivos é a seguinte:

-   Use a Proteção de Informações do Azure para identificar os dados confidenciais.

-   Use o verificador da Proteção de Informações do Azure para encontrar dados.

A abordagem recomendada para compartilhamentos de arquivos inclui estas etapas:

1.  **Instale e configure o verificador da Proteção de Informações do Azure.**

    -   Decida quais tipos de dados confidenciais usar.

    -   Especifique pastas locais e compartilhamentos de rede a serem usados.

2.  **Execute um ciclo de descoberta.**

    -   Execute o verificador no modo de descoberta e valide os resultados.

    -   Se necessário, otimize as condições e os tipos de informações confidenciais.

    -   Avalie o impacto esperado de aplicar rótulos automaticamente.

3.  **Execute o verificador da Proteção de Informações do Azure para aplicar rótulos a documentos qualificados**.

4.  **Para a proteção:**

    -   Configure regras de prevenção contra a perda de dados do Exchange para proteger documentos com o rótulo desejado.

    -   Certifique-se de usar permissões para limitar quem pode acessar os arquivos.

5.  **Para monitorar, integre os registros do Windows Server com uma ferramenta SIEM.**

    -   Para localizar dados pessoais para solicitações de titulares de dados, use o verificador da Proteção de Informações do Azure. Você também pode configurar a pesquisa do SharePoint Server para rastrear compartilhamentos de arquivos.

Para mais informações sobre o uso do verificador de Proteção de Informações do Azure para encontrar e rotular dados pessoais, confira [Implantar a AIP de Verificação](/azure/information-protection/deploy-aip-scanner).

Confira informações sobre como configurar o verificador para utilizar condições e os tipos de informações confidenciais para prevenção contra perda de dados (DLP) do Office 365 em [Como configurar as condições de classificação automática e recomendada para a Proteção de Informações do Azure](/information-protection/deploy-use/configure-policy-classification). Observe que os novos tipos de informações confidenciais do Office 365 não estarão disponíveis imediatamente para uso com o verificador e que tipos de informações confidenciais personalizadas não podem ser usadas com o verificador.
