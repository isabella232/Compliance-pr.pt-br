---
title: Serviço de processador de dados das Solicitações do Titular de Dados do Windows Enterprise para o GDPR e o CCPA
description: Saiba como usar produtos, serviços e ferramentas de administração da Microsoft para encontrar e tomar medidas em relação a dados pessoais para responder às DSRs.
keywords: Microsoft 365, Microsoft 365 Education, documentação do Microsoft 365, RGPD
localization_priority: Priority
ROBOTS: NOINDEX, NOFOLLOW
ms.prod: microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmaz
manager: laurawi
ms.reviewer: delinat
audience: itpro
ms.collection:
- GDPR
- M365-security-compliance
- MS-Compliance
hideEdit: true
ms.openlocfilehash: 1c677e2877142c866f82c00df6c1b3957231ae99
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/23/2021
ms.locfileid: "53088730"
---
# <a name="data-processor-service-for-windows-enterprise-data-subject-requests-for-the-gdpr-and-ccpa"></a>Serviço de processador de dados das Solicitações do Titular de Dados do Windows Enterprise para o GDPR e o CCPA 

>[!NOTE]
>Este tópico se destina aos participantes do serviço de processador de dados do programa de visualização prévia do Windows Enterprise e requer a aceitação dos termos de uso específicos. Para saber mais sobre o programa e concordar com os termos de uso, acesse [https://aka.ms/WindowsEnterprisePublicPreview](https://aka.ms/WindowsEnterprisePublicPreview).

## <a name="introduction-to-data-subject-requests-dsrs"></a>Introdução às DSRs (Solicitações de Titulares de Dados) 

O RGPD (Regulamento Geral sobre a Proteção de Dados) da União Europeia concede o direito às pessoas (reconhecidas na regulamentação como _titulares de dados_) de gerenciar os dados pessoais coletados por um empregador ou outro tipo de agência ou organização (conhecidos como _controladores de dados_ ou apenas _controladores_). Os dados pessoais são definidos nas linhas gerais no RGPD como todos os dados relacionados a uma pessoa física identificada ou identificável. O GDPR fornece às entidades de dados direitos específicos a seus dados pessoais. Esses direitos incluem obter cópias, solicitar alterações, restringir o processamento, excluir ou receber os dados em um formato eletrônico para que eles possam ser passados para outro controlador. Uma solicitação formal feita por uma entidade de dados a um controlador para executar uma ação em seus dados pessoais é chamada neste documento de _Solicitação de Direitos da Entidade de Dados_ ou DSR. 

Da mesma forma, a Lei de Privacidade do Consumidor da Califórnia (CCPA), fornece direitos e obrigações de privacidade aos consumidores da Califórnia, incluindo direitos semelhantes aos Direitos do Titular dos Dados do RGDP, como o direito de excluir, acessar e receber (portabilidade) suas informações pessoais. O CCPA também fornece certas divulgações, proteções contra discriminação ao eleger direitos de exercício e requisitos de aceitação/recusa para determinadas transferências de dados classificadas como "vendas". As vendas são amplamente definidas para incluir o compartilhamento de dados para uma consideração valiosa. Para obter mais informações sobre o CCPA, confira a [Lei de Privacidade do Consumidor da Califórnia](/microsoft-365/compliance/offering-ccpa) e as [Perguntas Frequentes Sobre a Lei de Privacidade do Consumidor da Califórnia](/microsoft-365/compliance/ccpa-faq).

O guia descreve como usar os produtos, serviços e ferramentas administrativas da Microsoft para ajudar os nossos clientes controladores a encontrar dados pessoais e agir em relação a eles para responder a DSRs. Especificamente, isso inclui como localizar, acessar e agir em dados pessoais que residem na nuvem da Microsoft. Veja aqui uma breve visão geral dos processos descritos neste guia: 

1. **Acessar**: recupere os dados pessoais que residem na nuvem da Microsoft e, se solicitado, faça uma cópia para disponibilizar para o titular dos dados. 
2. **Excluir**: remova permanentemente os dados pessoais que residem na nuvem da Microsoft. 
3. **Exportar**: forneça uma cópia eletrônica (em um formato legível por máquina) dos dados pessoais para o titular dos dados. Os dados pessoais do CCPA são quaisquer informações relacionadas a uma pessoa identificada ou identificável.

Os dados pessoais do CCPA são quaisquer informações relacionadas a uma pessoa, identificável ou não. Não há distinção entre as funções pública, privada ou de trabalho de uma pessoa. O termo definido "informações pessoais" se alinha aproximadamente aos "dados pessoais" do GDPR. No entanto, o CCPA também inclui dados da família e do domicílio. Para obter mais informações sobre o CCPA, confira a [Lei de Privacidade do Consumidor da Califórnia](/microsoft-365/compliance/offering-ccpa) e as [Perguntas Frequentes Sobre a Lei de Privacidade do Consumidor da Califórnia](/microsoft-365/compliance/ccpa-faq).

Cada seção deste guia descreve os procedimentos técnicos que uma organização controladora de dados pode realizar para responder a uma DSR para dados pessoais na nuvem da Microsoft. 

## <a name="terminology"></a>Terminologia

A lista a seguir fornece as definições dos termos que são relevantes para este guia. 

* _Controlador_ — a pessoa física ou jurídica, autoridade pública, órgão ou outra entidade que, sozinha ou em conjunto com terceiros, determina os fins e os meios do processamento de dados pessoais, onde tais fins e meios são determinados por lei da União ou Estado-Membro, o controlador ou os critérios específicos para sua indicação podem ser fornecidos por lei da União ou Estado-Membro. 

* _Dados pessoais e titular dos dados_— qualquer informação relativa a uma pessoa natural identificada ou identificável ("titular dos dados"); uma pessoa natural identificável é aquela que pode ser identificada, direta ou indiretamente, especialmente por referência a um identificador, como nome, um número de identificação, dados de localização, um identificador online ou um ou mais fatores específicos de natureza física, fisiológica, genética, mental, econômica, cultural ou social dessa pessoa natural. 

* _Processador_— é uma pessoa física ou jurídica, autoridade pública, agência ou outro órgão que processa dados pessoais em nome do controlador. 

* _Dados do Cliente_ — Todos os dados, incluindo texto, som, vídeo ou arquivos de imagem e software que são fornecidos para a Microsoft, por ou em nome de um cliente, através do uso do serviço corporativo. 

* _Dados de Diagnóstico do Windows_ — Dados técnicos vitais sobre os dispositivos Windows e como o Windows e os softwares relacionados estão funcionando. Ele é usado para manter o Windows atualizado, seguro, confiável, com desempenho e melhora o Windows por meio da análise agregada do uso do Windows. Alguns exemplos de Dados de Diagnóstico do Windows são o tipo de hardware que está sendo usado, os aplicativos instalados com o respectivo uso e as informações sobre a confiabilidade dos drivers de dispositivos. Alguns aplicativos e componentes do Windows se conectam aos serviços Microsoft diretamente, mas os dados que eles trocam não são Dados de Diagnóstico do Windows. Por exemplo, não alterar o local de um usuário para o clima ou a notícia local não é um exemplo de Dados de Diagnóstico do Windows. 

## <a name="how-to-use-this-guide"></a>Como usar este guia 

Quando você usa o serviço de processador de dados dos dispositivos inscritos no Windows Enterprise, o Windows gera algumas informações conhecidas como Windows Diagnostic Data para fornecer o serviço.

## <a name="windows-diagnostic-data"></a>Dados de Diagnóstico do Windows 

A Microsoft fornece a você a capacidade de acessar, excluir e exportar os dados de diagnóstico do Windows associados ao uso pelo usuário do serviço de processador de dados do Windows Enterprise.

>[!IMPORTANT]
>Não há suporte para a capacidade de corrigir Dados de Diagnóstico do Windows. Os Dados de Diagnóstico do Windows formam concretas ações conduzidas no Windows, e as modificações a esses dados comprometeriam o registro histórico das ações, aumentando os riscos de segurança e danificando a confiabilidade. Todos os dados abordados neste documento são considerados Dados de Diagnóstico do Windows. 

## <a name="executing-dsrs-against-windows-diagnostic-data"></a>Executando DSRs em Dados de Diagnóstico do Windows 

A Microsoft oferece a capacidade de acessar, excluir e exportar alguns dados de diagnóstico do Windows por meio do portal do Azure, e também diretamente por meio de interfaces de programação de aplicativos (APIs) pré-existentes.

### <a name="step-1-access"></a>Etapa 1: Acessar 

O administrador do locatário é a única pessoa dentro da organização que pode acessar os Dados de Diagnóstico do Windows associados ao uso por um determinado usuário de um serviço de processador de dados de um dispositivo Windows Enterprise registrado. Os dados recuperados de uma solicitação de acesso serão fornecidos, por meio de exportação, em um formato legível por computador e serão fornecidos em arquivos que permitem ao usuário saber quais dispositivos e serviços os dados serão associados. Conforme observado anteriormente, os dados recuperados não incluirão dados que possam comprometer a segurança ou estabilidade do dispositivo Windows. 

A Microsoft oferece uma experiência de portal, fornecendo ao administrador de locatário do cliente empresarial a capacidade de gerenciar solicitações de acesso DSR. [Azure DSR, Parte 2, Etapa 3: Exportar](/microsoft-365/compliance/gdpr-dsr-azure#step-3-export), descreve como executar uma solicitação de acesso DSR por meio de exportação, por meio do portal do Azure.

### <a name="step-2-delete"></a>Etapa 2: Excluir 

A Microsoft oferece uma maneira de executar solicitações de exclusão do DSR baseadas no usuário com base em um objeto do Azure Active Directory de um usuário específico.

Para solicitações de exclusão baseadas no usuário, a Microsoft oferece uma experiência de portal, fornecendo ao administrador de locatário do cliente empresarial a capacidade de gerenciar solicitações de exclusão de DSR. [Azure DSR, Parte 1, Etapa 5: Excluir](/microsoft-365/compliance/gdpr-dsr-azure#step-5-delete), descreve como executar uma solicitação de exclusão de DSR por meio do portal do Azure. 

A Microsoft oferece a capacidade de excluir usuários, o que, por sua vez, excluirá os dados do cliente, diretamente por meio de uma interface de programação de aplicativos (API) pré-existente. Os detalhes são descritos na [documentação de referência da API](/graph/api/directory-deleteditems-delete). 

>[!IMPORTANT]  
>Excluir os dados coletados não interrompe outras coletas. Para desabilitar a coleta de dados, siga o procedimento descrito na [documentação de referência do respectivo serviço](/windows/privacy/configure-windows-diagnostic-data-in-your-organization#enterprise-management).
 
 Além disso, as solicitações de exclusão baseadas no usuário exigem a exclusão da própria conta de usuário. 

### <a name="step-3-export"></a>Etapa 3: exportar 

O administrador do locatário é a única pessoa na organização que pode acessar os dados de diagnóstico do Windows associados ao uso de um serviço de processador de dados por um usuário específico para o dispositivo registrado do Windows Enterprise. Os dados recuperados de uma solicitação de exportação serão fornecidos em um formato legível por computador e serão fornecidos em arquivos que permitem ao usuário saber para quais dispositivos e serviços os dados serão associados. Conforme observado anteriormente, os dados recuperados não incluirão dados que possam comprometer a segurança ou estabilidade do dispositivo Windows. [Azure DSR, Parte 2, Etapa 3: Exportar](/microsoft-365/compliance/gdpr-dsr-azure#step-3-export), descreve como executar uma solicitação de exportação de DSR por meio do portal do Azure. 

A Microsoft oferece a capacidade de exportar Dados de Clientes diretamente por meio de uma interface de programação de aplicativos (API) pré-existente. Os detalhes são descritos na [documentação de referência da API](/graph/api/user-exportpersonaldata).

## <a name="notify-about-exporting-or-deleting-issues"></a>Notificar problemas de exportação ou exclusão 

Se você tiver problemas ao exportar ou excluir dados do Portal do Azure, acesse a folha **Ajuda e suporte** do portal do Azure e envie um novo tíquete na folha **Gerenciamento de Assinaturas > Outra Solicitação de Segurança e Conformidade > Privacidade e Solicitações de RGPD**. 
