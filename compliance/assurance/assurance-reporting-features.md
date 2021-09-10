---
title: Recursos de relatório do Microsoft 365
description: Saiba mais sobre vários recursos de relatórios Microsoft 365, incluindo Azure Active Directory e Exchange Online.
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
- M365-analytics
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: be05c96c725f8d0e05bc27f410d7f19e4e5d9a23
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2021
ms.locfileid: "58946863"
---
# <a name="microsoft-365-reporting-features"></a>Recursos de relatório do Microsoft 365

Os recursos de relatório no Microsoft 365 fornece vários relatórios de auditoria para Azure Active Directory (Azure AD), Exchange Online, gerenciamento de dispositivos, revisão de supervisão e prevenção contra perda de dados (DLP). Esses relatórios são diferentes e separados dos relatórios Microsoft 365 atividades.

## <a name="microsoft-365-reports-dashboard"></a>Microsoft 365 Painel relatórios

O painel Relatórios na visualização Centro de administração do Microsoft 365 exibe a atividade de uso em Microsoft 365. Microsoft 365 administradores globais, ou um administrador Exchange Online, SharePoint Online ou Skype for Business, podem obter informações granulares sobre o uso desse serviço. Por exemplo, o número de usuários em um serviço de Microsoft 365 específico, o número de usuários que ativaram o Microsoft 365 Apps para Grandes Empresas (anteriormente chamado Office 365 ProPlus) e a quantidade de emails fluindo pela organização. Os relatórios estão disponíveis para os últimos 7, 30, 90 e 180 dias.

Os relatórios a seguir estão disponíveis:

- [Relatório de atividade de email](https://support.office.com/article/Office-365-Reports-in-the-admin-center-preview--Email-activity-1cbe2c00-ca65-4fb9-9663-1bbfa58ebe44)
- [Microsoft Office relatório de ativações](https://support.office.com/article/Office-365-Reports-in-the-admin-center-preview--Microsoft-Office-activations-87c24ae2-82e0-4d1e-be01-c3bcc3f18c60)
- [SharePoint Relatório de uso do site online](https://support.office.com/article/Office-365-Reports-in-the-admin-center-preview--SharePoint-site-usage-4ecfb843-e5d5-464d-8bf6-7ed512a9b213)
- [OneDrive for Business relatório de uso](https://support.office.com/article/Office-365-Reports-in-the-Admin-Center-Preview--OneDrive-for-Business-usage-0de3b312-c4e8-4e4b-a02d-32b2f726a680)
- [Relatórios de atividades do Yammer](https://support.office.com/article/View-the-Yammer-Activity-report-in-the-Office-365-admin-center-preview-c7c9f938-5b8e-4d52-b1a2-c7c32cb2312a)
- [Skype for Business relatório de atividades](/SkypeForBusiness/skype-for-business-online-reporting/activity-report)
- [Skype for Business Relatório de atividades ponto a ponto](/SkypeForBusiness/skype-for-business-online-reporting/peer-to-peer-activity-report)
- [Skype for Business Relatório organizador de conferências](/SkypeForBusiness/skype-for-business-online-reporting/conference-organizer-activity-report)
- [Skype for Business Relatório de atividade do participante da conferência](/SkypeForBusiness/skype-for-business-online-reporting/conference-participant-activity-report)

Para obter mais informações, consulte [Relatórios de Atividades no Centro de administração do Microsoft 365](https://support.office.com/article/activity-reports-in-the-office-365-admin-center-0d6dfb17-8582-4172-a9a9-aed798150263).

## <a name="azure-ad-reports"></a>Relatórios do Azure AD

Microsoft 365 usa o Azure AD para gerenciamento de autenticação e identidade. Microsoft 365 administradores usam relatórios gerados pelo Azure para identificar atividades incomuns e acesso não autorizado a seus dados. Você pode usar relatórios de acesso e uso no Azure AD para obter visibilidade sobre a integridade e a segurança do diretório para sua organização. Com essas informações, você pode identificar e reduzir possíveis riscos de segurança.

Os relatórios do Azure AD podem ser exportados para Microsoft Excel e correlacionados com outros dados de Microsoft 365. Por exemplo, os resultados de uma pesquisa de log de auditoria podem fornecer informações sobre atividades de acesso, autenticação e nível de aplicativo. Relatórios avançados de anomalia e uso de recursos estão disponíveis com Azure AD Premium. Esses relatórios avançados ajudam a melhorar sua postura de segurança e ajudá-lo a responder a possíveis ameaças aplicando análises sobre o acesso ao dispositivo e o uso do aplicativo. Para obter mais informações, [consulte Azure Active Directory relatório](/azure/active-directory/reports-monitoring/overview-reports/).

## <a name="exchange-online-audit-reports"></a>Exchange Online Relatórios de auditoria

Exchange Online relatórios de auditoria incluem detalhes sobre o acesso à caixa de correio e as alterações feitas pelos administradores em seu Exchange Online locatário. Com a auditoria de caixa de correio, você pode usar as tarefas na tabela a seguir para executar relatórios e exportar Exchange Online logs de auditoria.

> [!NOTE]
> Você deve habilitar o log de auditoria de caixa de correio para cada caixa de correio para que os eventos auditados sejam salvos no log de auditoria dessa caixa de correio. Se o log de auditoria de caixa de correio não estiver habilitado para uma caixa de correio, os eventos dessa caixa de correio não serão salvos no log de auditoria e não aparecerão nos relatórios de auditoria de caixa de correio. Para obter mais informações, consulte [enable mailbox auditing](https://support.office.com/article/Enable-mailbox-auditing-in-Office-365-aaca8987-5b62-458b-9882-c28476a66918).

| Tarefa | Descrição |
|----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Executar relatório de acesso à caixa de correio de um não proprietário](/exchange/security-and-compliance/exchange-auditing-reports/non-owner-mailbox-access-report) | Exibe a lista de caixas de correio acessadas por alguém diferente do proprietário da caixa de correio. O relatório contém informações sobre quem acessou a caixa de correio, as ações realizadas na caixa de correio e se as ações foram bem-sucedidas. |
| [Exportar logs de auditoria de caixas de correio](/exchange/security-and-compliance/exchange-auditing-reports/export-mailbox-audit-logs) | Os logs de auditoria de caixa de correio contêm informações sobre acesso e ações em uma caixa de correio tomada por um usuário diferente do proprietário da caixa de correio. Os administradores podem especificar caixas de correio junto com um intervalo de datas para gerar relatórios. Os logs são exportados em XML, anexados a uma mensagem e enviados a usuários específicos conforme determinado pelo administrador. |
| [Executar um relatório de grupo de função de administrador](/Office365/SecurityCompliance/eop/run-an-administrator-role-group-report-in-eop-eop) | O grupo de função de administrador atribui privilégios administrativos aos usuários. Esses privilégios permitem que os usuários executem tarefas administrativas, como redefinir senhas, criar ou modificar caixas de correio e atribuir privilégios de administrador a outros usuários. O relatório do grupo de funções de administrador mostra alterações em grupos de função, incluindo a adição ou remoção de membros. |
| [Exibir o log de auditoria administrador](/exchange/security-and-compliance/exchange-auditing-reports/view-administrator-audit-log) | O relatório de log de auditoria do administrador lista todas as funções de criação, atualização e exclusão executadas pelos administradores Exchange Online. Entradas de log fornecem informações sobre qual cmdlet foi executado, quais parâmetros foram usados, quem correu o cmdlet e quais objetos foram afetados. |
| [Pesquisa e espera de conteúdo de caixa de correio](/exchange/security-and-compliance/in-place-ediscovery/in-place-ediscovery) | Fornece detalhes de quaisquer alterações nas configurações In-Place Descoberta In-Place de In-Place em caixas de correio. |
| [Exportar o log de auditoria do administrador](/exchange/security-and-compliance/exchange-auditing-reports/search-role-group-changes) | O log de auditoria do administrador registra ações administrativas específicas, como criar, atualizar e excluir em Exchange Online. Os resultados do log são exportados para XML e os administradores podem optar por enviar esse log para um conjunto de usuários. |
| [Executar um relatório de retenção de litígio por caixa de correio](/exchange/security-and-compliance/exchange-auditing-reports/per-mailbox-litigation-hold-report) | Fornece detalhes de quaisquer alterações nas configurações de responsabilidade de litígio em caixas de correio. |
| [Exibir e exportar o log de auditoria de administrador externo](/exchange/security-and-compliance/exchange-auditing-reports/view-external-admin-audit-log) | Contém detalhes das ações executadas por administradores externos. As entradas fornecem informações sobre qual cmdlet foi executado, quais parâmetros foram usados e qualquer ação que crie, modifique ou exclua objetos no Exchange Online. |

## <a name="device-compliance-reports"></a>Relatórios de conformidade do dispositivo

Você gerencia e segura dispositivos móveis conectados à sua assinatura usando o Basic Mobility and Security para Microsoft 365. Dispositivos móveis usados para acessar emails de trabalho, calendário, contatos e documentos têm um papel significativo em garantir que os funcionários sejam capazes de trabalhar a qualquer momento e em qualquer lugar. É fundamental proteger as informações da sua organização. Você usa o Basic Mobility and Security para Microsoft 365 definir políticas de segurança de dispositivos e regras de acesso. Se for perdido ou roubado, você também usará o Basic Mobility and Security para Microsoft 365 apagar dispositivos móveis.

Os relatórios básicos de conformidade de mobilidade e segurança fornecem uma visão geral das políticas configuradas por uma organização para proteger dispositivos móveis que acessam Microsoft 365 dados. O relatório permite a filtragem de dispositivos por status de conformidade, violações relatadas, dispositivos bloqueados e quantos dispositivos foram apagados como resultado de políticas de segurança. Para obter mais informações, consulte [Overview of Basic Mobility and Security for Microsoft 365](https://support.microsoft.com/office/overview-of-basic-mobility-and-security-for-microsoft-365-faa7d8e5-645d-4d59-839c-c8d4c1869e4a).

## <a name="data-loss-prevention"></a>Prevenção contra perda de dados

As políticas DLP ajudam a gerenciar a segurança e o fluxo de informações em uma organização. Você pode configurar políticas para bloquear o acesso ao conteúdo, criptografar dados ou notificar os usuários sobre violações de política e política usando a Política de DLP no aplicativo Dicas. Os relatórios DLP fornecem informações sobre o número de diretivas e de combinações de regras, substituições e falsos positivos.

Você usa o Centro de administração do Microsoft 365 para exibir informações sobre o número de mensagens detectadas por suas políticas de DLP. Os relatórios DLP fornecem informações sobre correspondências de política e regra para emails enviados e recebidos. Você também pode exibir o número de combinações, substituições e falsos positivos para cada política nas últimas 24 horas usando o centro de administração Exchange. Se você baixar um relatório Excel, poderá exibir ainda mais detalhes, como quem enviou a mensagem, em que dia e quais as combinações de política foram disparadas. Para obter mais informações, consulte [Exibir relatórios sobre detecções de política DLP.](/previous-versions/exchange-server/exchange-150/jj889415(v=exchg.150))

## <a name="auditing-in-yammer-enterprise"></a>Auditoria no Yammer Enterprise

Yammer Enterprise fornece aos administradores a capacidade de exportar dados de atividade do usuário de sua rede Yammer por meio da [API](https://support.office.com/article/export-data-from-yammer-enterprise-b303d8f3-007d-4ad4-81f8-54fb1ecfb3f2)de exportação de dados Yammer ou manualmente por meio da página de administrador de rede Yammer. A capacidade de exportar logs é restrita aos administradores de rede Yammer. (Todos os Microsoft 365 globais são Yammer administradores de rede.)

Os seguintes dados são exportáveis:

| Nome do arquivo | Descrição |
|----------------------------|-------------------------------------------------------------------------|
| Users.csv | Todos os usuários novos, pendentes e suspensos na rede |
| Messages.csv | Todas as mensagens na rede |
| Files.csv (metadados) | Metadados como nome do arquivo, URL da API de arquivo, ID do uploader, carregado em, etc. |
| Files.csv (arquivos originais) | Arquivo ZIP dos arquivos originais carregados pelos usuários em Yammer |
| Topics.csv | Tópicos criados na rede |
| Pages.csv | Páginas (anotações) criadas por usuários na rede |
| Admins.csv | Todos os administradores verificados na rede |
| Networks.csv | Todas as Yammer externas |

Yammer Enterprise dados também estão disponíveis por meio dos relatórios Microsoft 365 atividades. Além disso, Yammer está trabalhando ativamente na exposição de log adicional por meio da API de Atividade de Gerenciamento Microsoft 365 e na capacidade de raciocínio sobre os dados usando Power BI. Consulte o [Office roteiro para](https://fasttrack.microsoft.com/roadmap?filters=yammer) obter mais informações sobre esses recursos.
