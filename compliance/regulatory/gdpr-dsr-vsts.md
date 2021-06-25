---
title: Solicitações do titular dos dados do Azure DevOps para GDPR e CCPA
description: Aprenda a usar as ferramentas do Microsoft para exportar ou excluir dados pessoais coletados durante uma sessão autenticada do Azure DevOps Services.
keywords: Visual Studio Team Services, VSTS, documentação do Azure DevOps, privacidade, GDPR e CCPA
localization_priority: Priority
audience: itpro
ms.prod: devops
ms.topic: article
author: robmazz
ms.author: robmazz
f1.keywords:
- NOCSH
manager: laurawi
ms.collection:
- GDPR
- M365-security-compliance
- MS-Compliance
ms.workload:
- multiple
titleSuffix: Microsoft GDPR
ms.custom: seo-marvel-mar2020
hideEdit: true
ms.openlocfilehash: 5511888b34cd9e3eb7f4e76d86c91cea4f4924c6
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/23/2021
ms.locfileid: "53088520"
---
# <a name="azure-devops-services-data-subject-requests-for-the-gdpr-and-ccpa"></a>Solicitações de assunto de dados do Azure DevOps Services para o RGPD e CCPA

O RGPD [(Regulamento Geral sobre a Proteção de Dados)](https://ec.europa.eu/justice/data-protection/reform/index_en.htm) da União Europeia fornece direitos às pessoas, conhecidas na regulamentação como *titulares de dados*, para gerenciar os dados pessoais coletados por um *controlador de dados*. Um controlador de dados, ou somente *controlador*, é um funcionário ou outro tipo de agência ou organização. Os dados pessoais são definidos amplamente no RGPD como quaisquer dados relacionados a uma pessoa identificada ou identificável. O RGPD fornece aos titulares de dados direitos específicos aos dados pessoais deles. Esses direitos incluem a obtenção de cópias desses dados pessoais, a solicitação de correções, a restrição do processamento, a exclusão ou o recebimento desses dados em formato eletrônico para que possam ser migrados para outro controlador. Uma solicitação formal de um titular de dados feita a um controlador para realizar uma ação nos dados pessoais dele é chamada de *Solicitação de Titular de Dados* ou DSR.

Da mesma forma, a Lei de Privacidade do Consumidor da Califórnia (CCPA), fornece direitos e obrigações de privacidade aos consumidores da Califórnia, incluindo direitos semelhantes aos Direitos do Titular dos Dados do GDPR, como o direito de excluir, acessar e receber (portabilidade) suas informações pessoais.  O CCPA também fornece certas divulgações, proteções contra discriminação ao eleger direitos de exercício e requisitos de "aceitação/recusa" para determinadas transferências de dados classificadas como "vendas". As vendas são amplamente definidas para incluir o compartilhamento de dados para uma consideração valiosa. Para obter mais informações sobre o CCPA, confira a [Lei de Privacidade do Consumidor da Califórnia](offering-ccpa.md) e as [Perguntas Frequentes Sobre a Lei de Privacidade do Consumidor da Califórnia](ccpa-faq.md).

Para saber mais sobre o RGPD, confira a [Seção RGPD do portal de Confiança do Serviço](https://servicetrust.microsoft.com/ViewPage/GDPRGetStarted).

Este guia descreve como usar as ferramentas da Microsoft para exportar ou excluir dados pessoais coletados durante uma sessão autenticada (conectada) do Azure DevOps Services (anteriormente conhecido como Visual Studio Team Services).

## <a name="additional-privacy-information"></a>Informações adicionais sobre privacidade

Os artigos [Política de Privacidade da Microsoft](https://privacy.microsoft.com/privacystatement), [Termos de Serviços Online (OST)](https://www.microsoft.com/licensing/product-licensing/products.aspx) e [Compromissos com o RGPD da Microsoft](/legal/gdpr) descrevem nossas práticas de processamento de dados.

## <a name="personal-data-we-collect"></a>Dados pessoais que coletamos

A Microsoft coleta dados de usuários para operar e aprimorar o Azure DevOps Services. O Azure DevOps Services coleta duas categorias de dados do cliente e logs gerados pelo sistema. Os dados do cliente incluem dados de interação e transacionais de que o Azure DevOps Services precisa para operar o serviço. Os logs gerados pelo sistema incluem dados de uso do serviço agregados para cada recurso e área de produto.

## <a name="delete-azure-devops-data"></a>Excluir dados do Azure DevOps

O primeiro passo para excluir os dados do cliente do Azure DevOps Services associados e tornar anônimo os dados pessoalmente identificáveis encontrados em logs gerados pelo sistema é fechar a conta de identidade Azure Active Directory (AAD) ou a conta da Microsoft (MSA). O Azure DevOps Services é confiável como um sistema de registro com integridade, capacidade de rastreamento e regras de auditoria rigorosas. Essas obrigações existentes afetam nossas obrigações de retenção e exclusão para o RGPD. Fechar a conta de identidade não altera nem remove artefatos e registros associados à identidade individual na organização do Azure DevOps Services. Garantimos que, quando uma organização do Azure DevOps Services inteira é excluída, todos os dados e logs gerados pelo sistema pessoalmente identificáveis encontrados na organização são removidos de nossos sistema (após o prazo de exclusão de 30 dias da organização do Azure DevOps Services).

## <a name="export-azure-devops-data"></a>Exportar dados do Azure DevOps

Os controladores podem exportar dados do cliente e logs gerados pelo sistema coletados dos titulares de dados por um de dois métodos, dependendo do provedor de identidade (MSA ou AAD) usado para entrar no Azure DevOps Services.

- Os usuários que autenticarem usando uma conta com backup de um locatário do Azure, por exemplo, conta AAD ou conta MSA associada a uma assinatura do Azure, podem seguir as instruções em [Solicitações de Titulares de Dados do Azure para o RGPD](gdpr-dsr-azure.md).

- Os usuários que autenticam usando uma identidade MSA podem usar esse [site de Solicitação de Privacidade](https://www.microsoft.com/concern/privacyrequest-msa) para exibir dados da atividade ligados à identidade deles no MSA em vários serviços da Microsoft. Nesse cenário, o usuário é um controlador dos próprios dados pessoais.

## <a name="export-or-delete-issues"></a>Exportar ou excluir problemas

Para identidades do AAD, se você tiver problemas ao exportar ou excluir dados do portal do Azure, vá para a folha **Ajuda + Suporte** do portal do Azure e envie um novo tíquete em **Gerenciamento de Assinaturas** > **Solicitações de privacidade e Conformidade** > **Folha de Privacidade e Solicitações do GDPR**.

Para identidades MSA, se você tiver problemas ao exportar dados do site de Solicitação de Privacidade, faça login no [site de Solicitação de Privacidade](https://www.microsoft.com/concern/privacyrequest-msa) e envie uma solicitação de ajuda da equipe de Privacidade Microsoft pelo formulário de solicitação na Web.

## <a name="learn-more"></a>Saiba mais

A Microsoft se compromete a garantir que seus dados do Azure DevOps Services permanecem seguros e privados sem exceção. Acesse o white paper [Visão geral de proteção de dados do Azure DevOps Services](/vsts/articles/team-services-security-whitepaper) para saber mais sobre como podemos proteger seus dados no Azure DevOps Services.

## <a name="see-also"></a>Confira também

- [Compromissos da Microsoft sobre o RGPD para com os clientes dos nossos produtos de software empresarial disponibilizados de maneira geral](/legal/gdpr)
- [Central de Confiabilidade da Microsoft](https://www.microsoft.com/trust-center/privacy/gdpr-overview)
- [Portal de Confiança do Serviço](https://servicetrust.microsoft.com/ViewPage/GDPRGetStarted)
- [Painel de Privacidade da Microsoft](https://account.microsoft.com/privacy)
- [Centro de Resposta Privacidade da Microsoft](https://aka.ms/userprivacysite)
- [Solicitações de Entidades de Dados do Azure para o RGPD](gdpr-dsr-azure.md)
