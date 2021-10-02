---
title: Dados de diagnóstico do Windows solicitações de titulares de dados de configuração do processador para o RGPD e CCPA
description: Saiba como usar produtos, serviços e ferramentas de administração da Microsoft para encontrar e tomar medidas em relação a dados pessoais para responder às DSRs.
keywords: Microsoft 365, Microsoft 365 Education, documentação do Microsoft 365, RGPD
ms.localizationpriority: high
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
ms.openlocfilehash: 52db464f30ac518cb60fcb62ad908e0fb3de31eb
ms.sourcegitcommit: 0777355cfb73c07d2b7e11d95a5996be8913b2af
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/01/2021
ms.locfileid: "60050565"
---
# <a name="windows-diagnostic-data-processor-configuration-data-subject-requests-for-the-gdpr-and-ccpa"></a>Dados de diagnóstico do Windows solicitações de titulares de dados de configuração do processador para o RGPD e CCPA

**Aplica-se a:**
-   Edição Windows 10 Enterprise, Pro e Education, versão 1809 com atualização de julho de 2021 e mais recente.
-   Edição Windows 11 Enterprise, Pro e Education

## <a name="introduction-to-data-subject-requests-dsrs"></a>Introdução às DSRs (Solicitações de Entidades de Dados)

O Regulamento Geral sobre a Proteção de Dados (RGPD) da UE fornece direitos às pessoas (conhecidas no regulamento como _titulares de dados_) para gerenciar os dados pessoais que foram coletados por um funcionário, ou outro tipo de órgão ou organização (conhecido como _controlador de dados_ ou apenas _controlador_). Os dados pessoais são definidos amplamente no RGPD como os dados relacionados a uma pessoa identificada ou identificável. O RGPD fornece aos titulares de dados os direitos específicos dos seus dados pessoais; esses direitos incluem a obtenção das cópias dos dados pessoais, a solicitação de correções, a restrição do processamento, a exclusão ou o recebimento desses dados em formato eletrônico para que possam ser migrados para outro controlador. Uma solicitação formal de um titular de dados feita a um controlador para realizar uma ação nos seus dados pessoais é chamada de _Solicitação de Titular de Dados_ ou DSR.

Da mesma forma, a Lei de Privacidade do Consumidor da Califórnia (CCPA), fornece direitos e obrigações de privacidade aos consumidores da Califórnia, incluindo direitos semelhantes aos Direitos do Titular dos Dados do RGDP, como o direito de excluir, acessar e receber (portabilidade) suas informações pessoais. O CCPA também fornece certas divulgações, proteções contra discriminação ao eleger direitos de exercício e requisitos de "aceitação/recusa" para determinadas transferências de dados classificadas como "vendas". As vendas são amplamente definidas para incluir o compartilhamento de dados para uma consideração valiosa. Para obter mais informações sobre o CCPA, confira a [Lei de Privacidade do Consumidor da Califórnia](/microsoft-365/compliance/offering-ccpa) e as [Perguntas Frequentes Sobre a Lei de Privacidade do Consumidor da Califórnia](/microsoft-365/compliance/ccpa-faq).

O guia discute como usar produtos, serviços e ferramentas administrativas da Microsoft para ajudar nossos clientes controladores a localizar e agir sobre dados pessoais para responder a DSRs. Especificamente, inclui como localizar, acessar e agir sobre dados pessoais no dados de diagnóstico do Windows coletados pela Microsoft quando a configuração do processador dados de diagnóstico do Windows está habilitada. Aqui está uma visão geral rápida dos processos descritos neste guia:

1. **Acessar**: recupere dados de diagnóstico do Windows associado a um titular de dados e, se solicitado, faça uma cópia dele que possa estar disponível para o titular dos dados.
2. **Excluir**: remova permanentemente dados de diagnóstico do Windows associado a um titular de dados.
3. **Exportar**: forneça uma cópia eletrônica (em um formato legível por máquina) dos dados pessoais para o titular dos dados.

Os dados pessoais do CCPA são quaisquer informações relacionadas a uma pessoa, identificável ou não. Não há distinção entre as funções pública, privada ou de trabalho de uma pessoa. O termo definido "informações pessoais" se alinha aproximadamente aos "dados pessoais" do RGPD. No entanto, o CCPA também inclui dados da família e do domicílio. Para obter mais informações sobre o CCPA, confira a [Lei de Privacidade do Consumidor da Califórnia](/microsoft-365/compliance/offering-ccpa) e as [Perguntas Frequentes Sobre a Lei de Privacidade do Consumidor da Califórnia](/microsoft-365/compliance/ccpa-faq).

Cada seção neste guia descreve os procedimentos técnicos que uma organização do controlador de dados pode seguir para responder a uma DSR para dados de diagnóstico do Windows coletada pela Microsoft quando a configuração do processador dados de diagnóstico do Windows está habilitada.

## <a name="terminology"></a>Terminologia

A lista a seguir fornece as definições dos termos que são relevantes para este guia.

* _Controlador_ — a pessoa física ou jurídica, autoridade pública, órgão ou outra entidade que, sozinha ou em conjunto com terceiros, determina os fins e os meios do processamento de dados pessoais, onde tais fins e meios são determinados por lei da União ou Estado-Membro, o controlador ou os critérios específicos para sua indicação podem ser fornecidos por lei da União ou Estado-Membro.

* _Dados pessoais e titular dos dados_— qualquer informação relativa a uma pessoa natural identificada ou identificável ("titular dos dados"); uma pessoa natural identificável é aquela que pode ser identificada, direta ou indiretamente, especialmente por referência a um identificador, como nome, um número de identificação, dados de localização, um identificador online ou um ou mais fatores específicos de natureza física, fisiológica, genética, mental, econômica, cultural ou social dessa pessoa natural.

* _Processador_— é uma pessoa física ou jurídica, autoridade pública, agência ou outro órgão que processa dados pessoais em nome do controlador.

* _Dados do Cliente_ — Todos os dados, incluindo texto, som, vídeo ou arquivos de imagem e software que são fornecidos para a Microsoft, por ou em nome de um cliente, através do uso do serviço corporativo. 

* _Dados de Diagnóstico do Windows_: dados técnicos vitais sobre os dispositivos Windows e como o Windows e os softwares relacionados estão funcionando. Ele é usado para manter o Windows atualizado, seguro, confiável, de alto desempenho e fazer melhorias no produto. Alguns exemplos de Dados de Diagnóstico do Windows são o tipo de hardware que está sendo usado, os aplicativos instalados com o respectivo uso e as informações sobre a confiabilidade dos drivers de dispositivos. Alguns aplicativos e componentes do Windows se conectam aos serviços Microsoft diretamente, mas os dados que eles trocam não são dados de diagnóstico do Windows. Por exemplo, trocar o local de um usuário pelo clima ou a notícia local não é um exemplo de Dados de Diagnóstico do Windows.

## <a name="how-to-use-this-guide"></a>Como usar este guia

Quando você habilita dados de diagnóstico do Windows configuração do processador, você se torna o controlador do dados de diagnóstico do Windows coletados dos dispositivos. Para obter mais informações sobre o nível Avançado, consulte [Configurar os dados de diagnóstico do Windows em sua organização](/windows/privacy/configure-windows-diagnostic-data-in-your-organization).

## <a name="windows-diagnostic-data"></a>Dados de diagnóstico do Windows

A Microsoft oferece a capacidade de acessar, excluir e exportar dados de diagnóstico do Windows associados ao uso dos dispositivos habilitados pelo usuário com a configuração do dados de diagnóstico do Windows processador.

> [!IMPORTANT]
> Alguns dados de diagnóstico do Windows estão associados apenas a um identificador de dispositivo e não estão associados a um usuário específico. Esse tipo de dados no nível do dispositivo não é exportado e é excluído de nossos sistemas dentro de 30 dias.<br><br>
> Não há suporte para a capacidade de corrigir Dados de Diagnóstico do Windows. Os Dados de Diagnóstico do Windows constituem ações concretas conduzidas no Windows, e as modificações a esses dados comprometeriam o registro histórico das ações, aumentando os riscos de segurança e danificando a confiabilidade.

A próxima seção fornece etapas sobre como executar uma solicitação de titular de dados para dados de diagnóstico do Windows associada a uma ID de usuário do Azure Active Directory (AAD). Para obter mais informações, consulte [Windows 10 e Conformidade de Privacidade do Windows 11. Um Guia para Profissionais de TI e de Conformidade](/windows/privacy/windows-10-and-privacy-compliance).

## <a name="executing-dsrs-against-windows-diagnostic-data"></a>Executando DSRs em Dados de Diagnóstico do Windows

A Microsoft oferece a capacidade de acessar, excluir e exportar alguns dados de diagnóstico do Windows por meio do portal do Azure, e também diretamente por meio de interfaces de programação de aplicativos (APIs) pré-existentes.

### <a name="step-1-access"></a>Etapa 1: Acessar

O administrador do locatário é a única pessoa dentro da organização que pode acessar os Dados de Diagnóstico do Windows associados ao uso por um determinado usuário de um serviço de processador de dados de um dispositivo Windows Enterprise registrado. Os dados recuperados de uma solicitação de acesso serão fornecidos, por meio de exportação, em um formato legível por computador e serão fornecidos em arquivos que permitem ao usuário saber quais dispositivos e serviços os dados serão associados. Conforme observado anteriormente, os dados recuperados não incluirão dados que possam comprometer a segurança ou estabilidade do dispositivo Windows.

A portal do Azure fornece ao administrador de locatários do cliente corporativo a capacidade de gerenciar solicitações de acesso DSR. [Azure DSR, Parte 2, Etapa 3: Exportar](/microsoft-365/compliance/gdpr-dsr-azure#step-3-export), descreve como executar uma solicitação de acesso DSR por meio de exportação, por meio do portal do Azure.

### <a name="step-2-delete"></a>Etapa 2: Excluir

A Microsoft oferece uma maneira de executar solicitações de exclusão do DSR baseadas no usuário com base em um objeto do Azure Active Directory de um usuário específico.

Para solicitações de exclusão baseadas no usuário, a Microsoft oferece duas soluções.  A Microsoft oferece uma experiência de portal, fornecendo ao administrador de locatário do cliente empresarial a capacidade de gerenciar solicitações de acesso DSR. [DSR do Azure, Parte 1, Etapa 5: Excluir](/microsoft-365/compliance/gdpr-dsr-azure#step-5-delete), descreve como executar uma solicitação de exclusão de DSR para dados de diagnóstico do Windows por meio do portal do Azure excluindo um usuário e dados associados.

A Microsoft também fornece a capacidade de excluir usuários, que, por sua vez, excluirão dados de diagnóstico do Windows, diretamente por uma interface de programação de aplicativo (API) pré-existente. Os detalhes são descritos na [Documentação de Referência da API](/graph/api/directory-deleteditems-delete).

>[!IMPORTANT]
>Excluir os dados coletados não interrompe outras coletas. Para desabilitar a coleta de dados, siga o procedimento descrito na [documentação de referência do respectivo serviço](/windows/privacy/configure-windows-diagnostic-data-in-your-organization#enterprise-management).

### <a name="step-3-export"></a>Etapa 3: exportar

O administrador do locatário é a única pessoa na sua organização que pode acessar os dados de diagnóstico do Windows associados ao uso de um determinado usuário de um dispositivo habilitado com a configuração do processador de dados de diagnóstico do Windows. TOs dados recuperados de uma solicitação de exportação serão fornecidos em um formato legível por computador e serão fornecidos em arquivos que permitirão que o usuário saiba a quais dispositivos e serviços os dados estão associados. Conforme observado anteriormente, os dados recuperados não incluirão dados que possam comprometer a segurança ou a estabilidade do dispositivo do Windows. O [Azure DSR, Parte 2, etapa 3: Exportar](/microsoft-365/compliance/gdpr-dsr-azure#step-3-export), descreve como executar um pedido de exportação de DSR para os dados de diagnóstico do Windows pelo portal do Azure.

A Microsoft também fornece a capacidade de exportar dados de diagnóstico do Windows diretamente de uma interface de programação dos aplicativos (API) pré-existentes. Os detalhes estão descritos na [Documentação de referência da API](/graph/api/user-exportpersonaldata).

## <a name="notify-us-about-exporting-or-deleting-issues"></a>Notificar problemas de exportação ou exclusão

Se você tiver problemas ao exportar ou excluir dados do Portal do Azure, acesse a folha **Ajuda e suporte** do portal do Azure e envie um novo tíquete na folha **Gerenciamento de Assinaturas > Outra Solicitação de Segurança e Conformidade > Privacidade e Solicitações de RGPD**.

>[!NOTE]
>Pode levar até 5 dias para completar um pedido de exportação de dados de diagnóstico do Windows. Se você tiver problemas, aguarde pelo menos sete dias antes de abrir um tíquete de suporte.
