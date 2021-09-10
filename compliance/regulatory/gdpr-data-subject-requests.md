---
title: Solicitações de assunto de dados para o RGPD e o CCPA
keywords: Microsoft 365, Microsoft 365 Education, documentação do Microsoft 365, RGPD, CCPA
ms.localizationpriority: high
ms.prod: microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmazz
manager: laurawi
audience: itpro
ms.collection:
- GDPR
- M365-security-compliance
- MS-Compliance
titleSuffix: Microsoft GDPR
description: Aprenda a concluir o DSRs sob as Normas Gerais de Proteção de Dados (GPDR) e a Lei de Privacidade do Consumidor da Califórnia (CCPA) usando produtos e serviços da Microsoft.
ms.custom: seo-marvel-mar2020
hideEdit: true
ms.openlocfilehash: b5ef9464a686a5f2c8823f196408fd71026fa52d
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2021
ms.locfileid: "58947460"
---
# <a name="data-subject-requests-and-the-gdpr-and-ccpa"></a>Solicitações de assunto de dados e o RGPD e CCPA

O Regulamento Geral de Proteção de Dados (RGPD) introduz novas regras a organizações que ofereçam bens e serviços a pessoas na União Europeia (UE) ou que coletam e analisam dados vinculados a residentes na UE. independentemente de onde você ou sua empresa estejam localizados. É possível encontrar mais informações no [tópico Resumo RGDP](gdpr.md).

Da mesma forma, a Lei de Privacidade do Consumidor da Califórnia (CCPA), fornece direitos e obrigações de privacidade aos consumidores da Califórnia, incluindo direitos semelhantes aos Direitos do Titular dos Dados do RGDP, como o direito de excluir, acessar e receber (portabilidade) suas informações pessoais.  O CCPA também fornece certas divulgações, proteções contra discriminação ao eleger direitos de exercício e requisitos de "aceitação/recusa" para determinadas transferências de dados classificadas como "vendas". Neste documento, você poderá obter informações sobre como concluir as solicitações de entidades de dados (DSRs) em RGPD e CCPA usando produtos e serviços da Microsoft.

- [Office 365](gdpr-dsr-Office365.md)
- [Azure](gdpr-dsr-Azure.md)
- [Intune](gdpr-dsr-Intune.md)
- [Dynamics 365](gdpr-dsr-Dynamics365.md)
- [Família do Visual Studio](gdpr-dsr-visual-studio-family.md)
- [Azure DevOps Services](gdpr-dsr-vsts.md)
- [Suporte e Serviços Profissionais da Microsoft](gdpr-dsr-prof-services.md)

## <a name="terminology"></a>Terminologia

Definições úteis para os termos do RGPD usados neste documento:

- *Controlador de Dados (Controlador*): uma pessoa jurídica, uma autoridade pública, uma agência ou outro corpo que, isoladamente ou em conjunto com outras pessoas, determina a finalidade e o meio de processamento de dados pessoais.  
- *Dados pessoais* e *entidade de dados*: qualquer informação relacionada a uma pessoa natural identificada ou identificável (entidade de dados); uma pessoa natural identificável é uma que pode ser identificada, direta ou indiretamente.  
- *Processador:* uma pessoa física ou jurídica, autoridade pública, órgão ou outra entidade que processa dados pessoais em nome do controlador.  
- *Dados do cliente*: dados produzidos e armazenados nas operações do dia a dia para o trabalho em andamento.

## <a name="what-is-a-dsr"></a>O que é um DSR?

O Regulamento Geral sobre a Proteção de Dados (RGPD) concede direitos às pessoas (conhecidas na regulamentação como titulares dos dados) para gerenciar os dados pessoais coletados por um empregador ou outro tipo de agência ou organização (conhecido como controlador de dados ou apenas controlador). O GDPR fornece aos titulares de dados direitos específicos para seus dados pessoais; esses direitos incluem obter cópias dele, solicitar alterações nele, restringir o processamento, excluí-lo ou recebê-lo em um formato eletrônico para que possa ser movido para outro controlador.

A Lei de Privacidade do Consumidor da Califórnia (CCPA), fornece direitos e obrigações de privacidade aos consumidores da Califórnia, incluindo direitos semelhantes aos Direitos do Titular dos Dados do GDPR, como o direito de excluir, acessar e receber (portabilidade) suas informações pessoais.  

Como controlador, você é obrigado a levar em consideração imediatamente cada DSR e fornecer uma resposta substantiva, basta executar a ação solicitada ou fornecer uma explicação sobre por que o DSR não pode ser acomodado pelo controlador. Um controlador deve consultar seus próprios consultores legais ou de conformidade quanto ao descarte apropriado de um determinado DSR.

Vários processos podem estar envolvidos na conclusão de um DSR, sujeito às regras de RGPD de conformidade da sua organização.
  
- **Descoberta**. O processo de determinar quais dados são necessários para concluir um DSR.
- **Acessar**. Recuperação e transmissão potencial para o assunto dos dados das informações descobertas.
- **Retificar**. Implemente alterações ou outros dados pessoais solicitados.
- **Restringir**. Alterar o acesso ou processamento de dados persona restringindo o acesso ou removendo dados da nuvem da Microsoft.
- **Exportar**. Fornecendo um formato "estruturado, comumente usado, de leitura por máquina" de dados pessoais para o titular de dados, conforme fornecido pelo "direito à portabilidade de dados" do RGPD".
- **Delete**. Remoção permanente de dados pessoais da nuvem da Microsoft.

## <a name="specific-dsr-considerations"></a>Considerações específicas sobre DSR

### <a name="insights-generated-by-microsoft-products-or-services"></a>Ideias geradas por produtos ou serviços da Microsoft

[As ideias](/microsoft-365/compliance/gdpr-dsr-office365#part-2-responding-to-dsrs-with-respect-to-insights-generated-by-office-365) podem ser geradas por serviços (MyAnalytics, etc.) O Office 365 inclui serviços online que fornecem ideias para usuários e organizações que os utilizam. Os dados gerados por esses serviços podem produzir dados pessoais relevantes para um DSR. Siga o link na lista abaixo para obter detalhes sobre processos DSR específicos do serviço.  

### <a name="dsrs-for-system-generated-logs"></a>DSRs para logs gerados pelo sistema

Os logs e os dados relacionados gerados pela Microsoft podem conter dados pessoais considerados pessoais sob a definição RGPD de "dados pessoais". Não há suporte para a capacidade de restringir ou corrigir dados nos logs gerados pelo sistema. Dados em logs gerados pelo sistema constituem ações concretas realizadas na nuvem da Microsoft e dados de diagnóstico, e a modificação de tais dados comprometeria o registro histórico de ações e aumentaria os riscos de segurança e fraude. A Microsoft oferece a capacidade de acessar, exportar e excluir registros gerados pelo sistema que podem ser necessários para concluir um DSR. Alguns exemplos de dados podem incluir:  

- Dados de uso de produtos e serviços, como os log de atividades do usuário
- Dados de solicitações e consultas de pesquisa do usuário
- Dados gerados por produtos e serviços como resultado da funcionalidade do sistema e da interação de usuários ou de outros sistemas.  

### <a name="yammer-and-kaizala"></a>Yammer e Kaizala

Excluir a conta de um usuário não removerá os logs gerados pelo sistema para o Yammer e o Kaizala. Para remover os dados desses aplicativos, consulte um dos seguintes recursos:

- [Gerenciar solicitações de entidades de dados do RGPD do Yammer Enterprise](/yammer/manage-security-and-compliance/gdpr-requests-in-yammer-enterprise)
- [Exportar ou excluir dados organizacionais do usuário no Kaizala](/office365/kaizala/export-or-delete-a-user-s-data)

### <a name="national-clouds"></a>Nuvens nacionais

Em algumas nuvens nacionais, um administrador de TI global precisa excluir os logs gerados pelo sistema.

### <a name="microsoft-services"></a>Serviços da Microsoft

Se a sua organização ou os usuários se envolver com a Microsoft para receber o suporte, os produtos e serviços da Microsoft podem conter dados pessoais. Para saber mais informações, confira [Solicitações de titulares dos dados ao suporte e aos Serviços profissionais da Microsoft sobre o RGPD](gdpr-dsr-prof-services.md).

### <a name="microsoft-controller-products"></a>Produtos do Microsoft Controller

Em algumas circunstâncias, os usuários de sua organização podem acessar produtos ou serviços da Microsoft para os quais a Microsoft é o controlador de dados. Nesses casos, os usuários precisam iniciar seu próprio DSRs diretamente na Microsoft, e a Microsoft preenche as solicitações diretamente para o usuário.

### <a name="third-party-products"></a>Produtos de terceiros

Para produtos e serviços de terceiros acessados por meio da autenticação de conta da Microsoft, as solicitações de assunto de dados devem ser direcionadas para a terceira parte aplicável.

## <a name="data-subject-request-admin-tools"></a>Ferramentas de administração de Solicitações de Entidades de Dados

- **Centro de Conformidade e Segurança**: os dados gerados pelo usuário são exportados pelo [Centro de Conformidade e Segurança](https://aka.ms/stpsecurityandcompliance) ou pelos recursos no aplicativo.
- **Centro de Administração do Azure AD**: exclua um assunto de dados do Azure Active Directory e os serviços relacionados usando o [Centro de Administração do Microsoft Azure AD](https://ms.portal.azure.com/#blade/Microsoft_AAD_IAM/UserManagementMenuBlade/Allusers/menuId/).
- **Exportação de Log de Dados da Microsoft**: os logs gerados pelo sistema podem ser exportados por administradores de locatários usando a [Exportação de Log de Dados da Microsoft](https://aka.ms/MicrosoftGDPR).

## <a name="learn-more"></a>Saiba mais

- [Central de Confiabilidade da Microsoft](https://www.microsoft.com/trust-center/privacy/gdpr-overview)
