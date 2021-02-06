---
title: Retenção, exclusão e destruição de dados no Microsoft 365
description: Uma visão geral das políticas da Microsoft para o Microsoft 365 em relação à retenção, exclusão e destruição de dados.
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
f1.keywords:
- NOCSH
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 025e2c422c05dbffdf5a510f93809beaed3fe09d
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120650"
---
# <a name="data-retention-deletion-and-destruction-in-microsoft-365"></a>Retenção, exclusão e destruição de dados no Microsoft 365

A Microsoft tem uma política Padrão de Manipulação de Dados para o Microsoft 365 que especifica por quanto tempo os dados do cliente são mantidos após a exclusão. Geralmente, há dois cenários em que os dados do cliente são excluídos:

- **Exclusão Ativa**: o locatário tem uma assinatura ativa e um usuário ou administrador exclui dados, ou os administradores excluem um usuário.
- **Exclusão passiva**: a assinatura do locatário termina.

## <a name="data-retention"></a>Retenção de dados

Para cada um desses cenários de exclusão, a tabela a seguir mostra o período máximo de retenção de dados, por categoria e classificação de dados:

| Categoria de Dados | Classificação de Dados | Descrição | Exemplos | Período de retenção |
|-----------------|-----------------|-----------------|----------------------------------|-------------------------------|
| Dados do cliente | Conteúdo do cliente| Conteúdo fornecido/criado diretamente por administradores e usuários <br><br> Inclui todo o texto, som, vídeo, arquivos de imagem e software criados e armazenados em data centers da Microsoft ao usar os serviços no Microsoft 365 | Exemplos dos aplicativos do Microsoft 365 mais usados que permitem aos usuários a autoria de dados incluem Word, Excel, PowerPoint, Outlook e OneNote <br><br> O conteúdo do cliente também inclui segredos de propriedade do cliente/fornecidos (senhas, certificados, chaves de criptografia, chaves de armazenamento) | **Cenário de exclusão ativa:** no máximo 30 dias <br><br> **Cenário de exclusão passiva:** no máximo 180 dias |
| Dados do cliente | EuII (Informações de Identificação do Usuário Final) | Dados que identificam ou podem ser usados para identificar o usuário de um serviço da Microsoft. EUII não contém conteúdo do cliente | Nome de usuário ou nome de exibição (DOMAIN\UserName) <br><br> Nome principal do usuário (name@domain) <br><br>  Endereços IP específicos do usuário | **Cenário de Exclusão Ativa:** no máximo 180 dias (somente uma ação de administrador de locatários) <br><br> **Cenário de exclusão passiva:** no máximo 180 dias |
| Dados pessoais <br> (dados não incluídos nos Dados do Cliente) | Identificadores pseudônimos do usuário final (EUPI) | Um identificador criado pela Microsoft vinculado ao usuário de um serviço da Microsoft. Quando combinado com outras informações, como uma tabela de mapeamento, o EUPI identifica o usuário final <br><br> O EUPI não contém informações carregadas ou criadas pelo cliente | GUIDs, PUIDs ou SIDs do usuário <br><br> IDs de sessão | **Cenário de exclusão ativa:** no máximo 30 dias <br><br> **Cenário de exclusão passiva:** no máximo 180 dias |

## <a name="subscription-retention"></a>Retenção de Assinatura

No termo de uma assinatura ativa, um assinante pode acessar, extrair ou excluir dados do cliente armazenados no Microsoft 365. Se uma assinatura paga terminar ou for encerrada, a Microsoft manterá os dados do cliente armazenados no Microsoft 365 em uma conta de função limitada por 90 dias para permitir que o assinante extraia os dados. Após o período de retenção de 90 dias, a Microsoft desabilita a conta e exclui os dados do cliente. No prazo de 180 dias após a expiração ou o término de uma assinatura do Microsoft 365, a Microsoft desabilita a conta e exclui todos os dados do cliente da conta. Depois que o período máximo de retenção de todos os dados tiver decorrido, os dados serão renderizados comercialmente irrecuperáveis.

Para uma avaliação gratuita, sua conta passa para um status de carência por 30 dias na maioria dos países e regiões. Durante esse período de cortesia, você pode comprar o Microsoft 365. Se você decidir não comprar o Microsoft 365, poderá cancelar sua avaliação ou deixar que o período de cortesia expire, e as informações e dados da sua conta serão excluídos.

## <a name="expedited-deletion"></a>Exclusão Expedida

Para qualquer assinatura, um assinante pode entrar em contato com o Suporte da Microsoft e solicitar o des provisionamento de assinatura expedido. Nesse processo, todos os dados do usuário são excluídos três dias após o administrador inserir o código de bloqueio fornecido pela Microsoft. Isso inclui dados no SharePoint Online e no Exchange Online em espera ou armazenados em caixas de correio inativas.

Para obter mais informações sobre o des provisionamento expedido, consulte [Cancelar sua assinatura.](/microsoft-365/commerce/subscriptions/cancel-your-subscription)

## <a name="related-links"></a>Links relacionados

- [Destruição de dados](assurance-data-destruction.md)

- [Imutabilidade no Office 365](assurance-data-immutability.md)
- [Exclusão de dados do Exchange Online](assurance-exchange-online-data-deletion.md)
- [Exclusão de dados do SharePoint Online](assurance-sharepoint-online-data-deletion.md)
