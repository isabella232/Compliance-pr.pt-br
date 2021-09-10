---
title: Auditoria e relatórios nos serviços de nuvem da Microsoft
description: Uma visão geral dos recursos de auditoria e relatório dentro Office 365, Microsoft 365 e Garantia de Serviço.
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: medium
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- M365-analytics
- SPO_Content
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: c1a2cc9e770678683fb3823da73ed667de6d1f2b
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2021
ms.locfileid: "58946861"
---
# <a name="auditing-and-reporting-in-microsoft-cloud-services"></a>Auditoria e relatórios nos serviços de nuvem da Microsoft

Os serviços de nuvem da Microsoft incluem vários recursos de auditoria e relatório que você pode usar para rastrear atividades administrativas e de usuários em seu locatário, exemplos incluem alterações feitas nas configurações de locatário do Exchange Online e do SharePoint Online e alterações feitas pelos usuários em documentos e outros itens. Você pode usar informações de auditoria e relatórios disponíveis nos serviços de nuvem da Microsoft para gerenciar com mais eficiência a experiência do usuário, reduzir riscos e cumprir obrigações de conformidade.

## <a name="security--compliance-centers"></a>Centros de conformidade & segurança

O [Microsoft 365 Centro](https://protection.office.com)de Conformidade & Segurança, o Centro de Segurança do [Microsoft 365](https://security.microsoft.com)e o Centro de Conformidade do [Microsoft 365](https://compliance.microsoft.com) são portais de parada única para proteger dados em sua organização e incluem muitos recursos de auditoria e relatórios. Esses centros ajudam você com suas necessidades de proteção de dados ou conformidade e auditam a atividade do usuário e do administrador. Você pode acessar esses centros usando sua conta de administrador de assinatura.

Esses centros incluem painéis de navegação para acesso a vários recursos:

- **Alertas:** Permite gerenciar alertas, exibir alertas relacionados à segurança e gerenciar alertas avançados usando [Cloud App Security](/cloud-app-security/what-is-cloud-app-security).
- **Permissões:** Permite que você [atribua](/microsoft-365/security/office-365-security/grant-access-to-the-security-and-compliance-center) permissões como Administrador de Conformidade, Gerenciador de Descobertas e Outras Pessoas a pessoas em sua organização para que possam executar tarefas nesses centros. Você atribui permissões para a maioria dos recursos em cada centro, mas outras permissões devem ser configuradas usando o centro de administração Exchange e o SharePoint de administração.
- **Gerenciamento de ameaças:** Permite que você crie e aplique políticas de gerenciamento de dispositivo usando o Basic [Mobility](https://support.microsoft.com/office/overview-of-basic-mobility-and-security-for-microsoft-365-faa7d8e5-645d-4d59-839c-c8d4c1869e4a)and Security para Microsoft 365 , para configurar políticas de prevenção contra perda de dados [](/microsoft-365/compliance/data-loss-prevention-policies) (DLP) para sua organização, para configurar filtragem de email, anti-malware, DomainKeys Identified Mail (DKIM), anexos seguros, links seguros e aplicativos OAuth.
- **Governança de dados:** Permite importar emails ou SharePoint dados de outros sistemas para [Microsoft 365,](https://support.office.com/article/Import-PST-files-or-SharePoint-data-to-Office-365-ba688e0a-0fcb-4bd7-8e57-2b669564ea84)configurar caixas de [](/microsoft-365/compliance/retention-policies) correio de arquivo morto e definir políticas de retenção para email e outros conteúdos em sua organização. [](https://support.office.com/article/Enable-archive-mailboxes-in-the-Office-365-Security-Compliance-Center-268a109e-7843-405b-bb3d-b9393b2342ce)
- **Pesquisa & investigação:** Fornece [ferramentas](https://support.office.com/article/Run-a-Content-Search-in-the-Office-365-Security-Compliance-Center-61852fd9-fe8a-4880-a339-cb19ed3bff4a)de gerenciamento de caso de pesquisa de conteúdo, [log](https://support.office.com/article/Search-the-audit-log-in-the-Office-365-Security-Compliance-Center-0d4d0f35-390b-4518-800e-0c7ec95e946c)de auditoria, quarentena e Exchange Online [Descoberta](https://support.office.com/article/Manage-eDiscovery-cases-in-the-Office-365-Security-Compliance-Center-edea80d6-20a7-40fb-b8c4-5e8c8395f6da) Automática para detalhar rapidamente a atividade em caixas de correio, grupos e pastas públicas do SharePoint Online e OneDrive for Business.
- **Relatórios:** Permite que você acesse rapidamente relatórios [para](https://support.office.com/article/Reports-in-the-Office-365-Security-Compliance-Center-7acd33ce-1ec8-49fb-b625-43bac7b58c5a) SharePoint Online, OneDrive for Business, Exchange Online e Azure AD.
- **Garantia de serviço:** Fornece informações sobre como a Microsoft mantém segurança, privacidade e conformidade com padrões globais para Microsoft 365, Azure, Microsoft Dynamics CRM Online, Microsoft Intune e outros serviços de nuvem. Também inclui o acesso a ISO, SOC e outros relatórios de auditoria de terceiros, bem como Controles Auditados, que fornece detalhes sobre os vários controles que foram testados e verificados por auditores de terceiros do Microsoft 365.

## <a name="service-assurance"></a>Garantia de Serviço

Muitas organizações em setores regulamentados estão sujeitas a requisitos abrangentes de conformidade. Para realizar suas próprias avaliações de risco, os clientes geralmente precisam de informações detalhadas sobre como Microsoft 365 mantém a segurança e a privacidade de seus dados. A Microsoft está comprometida com a segurança e a privacidade dos dados do cliente em seus serviços de nuvem e para ganhar a confiança do cliente, fornecendo uma visão transparente de suas operações e acesso fácil a relatórios e avaliações de conformidade independentes.

A Garantia de Serviço fornece transparência de operações e informações sobre como a Microsoft mantém a segurança, a privacidade e a conformidade dos dados do cliente Microsoft 365. Ele inclui relatórios de auditoria de terceiros, juntamente com uma biblioteca de white papers, perguntas frequentes e outros materiais em tópicos Microsoft 365 como criptografia de dados, resiliência de dados, gerenciamento de incidentes de segurança e muito mais. Os clientes podem usar essas informações para executar suas próprias avaliações de risco regulatório. Os responsáveis pela conformidade podem atribuir a função "Usuário de Garantia de Serviço" para dar aos usuários acesso ao Service Assurance. O administrador de locatários também pode fornecer usuários externos, como auditores independentes, com acesso a informações no painel de Garantia de Serviço por meio do Portal de Confiança do [Microsoft Cloud Service](https://aka.ms/STP) (STP).

## <a name="onedrive-for-business-admin-center"></a>OneDrive for Business de administração

O Microsoft OneDrive de administração ajuda você a gerenciar rapidamente e facilmente as configurações de OneDrive for Business da sua organização em um só lugar. Para usar o OneDrive de administração, o acesso ao onedrive.com é necessário. Você também deve ser um administrador global para sua organização ou um administrador personalizado com a função SharePoint administrador. Acesse o OneDrive for Business de administração em [https://admin.onedrive.com](https://admin.onedrive.com/) .

Os principais recursos incluem uma área de conformidade que fornece aos administradores links para o centro de gerenciamento apropriado para cenários importantes, como pesquisar o log de auditoria, trabalhar com DLP, retenção, Descoberta e alerta.

## <a name="related-links"></a>Links relacionados

- [Recursos de relatório do Microsoft 365](assurance-reporting-features.md)
- [ Registro interno para engenharia do Microsoft 365 ](assurance-internal-logging.md)
