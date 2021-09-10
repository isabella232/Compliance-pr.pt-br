---
title: Solicitações de assunto de dados do Azure para o GDPR e o CCPA
description: Saiba como usar produtos, serviços e ferramentas de administração da Microsoft para encontrar e tomar medidas em relação a dados pessoais para responder às DSRs.
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
hideEdit: true
titleSuffix: Microsoft GDPR
ms.custom: seo-marvel-mar2020
ms.openlocfilehash: 820197523e37958873853e00afdcff555408f423
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2021
ms.locfileid: "58947466"
---
# <a name="azure-data-subject-requests-for-the-gdpr-and-ccpa"></a>Solicitações de assunto de dados do Azure para o GDPR e o CCPA

## <a name="introduction-to-data-subject-requests-dsrs"></a>Introdução às DSRs (Solicitações de Entidades de Dados)

O Regulamento Geral [de Proteção de Dados da União Europeia (GDPR)](https://ec.europa.eu/justice/data-protection/reform/index_en.htm) concede direitos às pessoas (conhecidas no regulamento como *titulares de dados*) para gerenciarem os dados pessoais coletados por um empregador ou outro tipo de agência ou organização (conhecido como *controlador de dados* ou apenas *controlador*). Os dados pessoais são definidos de maneira muito ampla, sob o GDPR, assim como qualquer dado relacionado à uma pessoa física identificada ou identificável. O GDPR concede aos titulares de dados direitos específicos sobre seus dados pessoais; esses direitos incluem obter cópias dos dados pessoais, solicitar correções, restringir o processamento, excluí-los ou recebê-los em formato eletrônico para que possam ser movidos para outro controlador. Uma solicitação formal de um titular de dados a um controlador para executar uma ação em seus dados pessoais é chamada de *Solicitação de titular de dados* ou DSR.

Da mesma forma, a Lei de Privacidade do Consumidor da Califórnia (CCPA), fornece direitos e obrigações de privacidade aos consumidores da Califórnia, incluindo direitos semelhantes aos Direitos do Titular dos Dados do GDPR, como o direito de excluir, acessar e receber (portabilidade) suas informações pessoais. O CCPA também fornece certas divulgações, proteções contra discriminação ao eleger direitos de exercício e requisitos de "aceitação/recusa" para determinadas transferências de dados classificadas como "vendas". As vendas são amplamente definidas para incluir o compartilhamento de dados para uma consideração valiosa. Para obter mais informações sobre o CCPA, confira a [Lei de Privacidade do Consumidor da Califórnia](offering-ccpa.md) e as [Perguntas Frequentes Sobre a Lei de Privacidade do Consumidor da Califórnia](ccpa-faq.yml).

O guia descreve como usar os produtos, serviços e ferramentas administrativas da Microsoft para ajudar os nossos clientes controladores a encontrar dados pessoais e agir em relação a eles para responder a DSRs. Especificamente, isso inclui como localizar, acessar e agir em dados pessoais que residem na nuvem da Microsoft. Veja aqui uma breve visão geral dos processos descritos neste guia:

- **Descubra:** use as ferramentas de pesquisa e descoberta para encontrar com mais facilidade os dados de clientes que possam estar sujeitos a uma DSR. Assim que os documentos potencialmente responsivos forem coletados, você pode executar uma ou mais ações de DSR descritas nas etapas a seguir a fim de responder à solicitação. Como alternativa, você pode determinar que a solicitação não atende às diretrizes de sua organização para responder a DSRs.
- **Acesso:** recupere dados pessoais que residem na nuvem da Microsoft e, se solicitado, faça uma cópia para disponibilizar para o titular dos dados.
- **Retificação:** faça alterações ou implemente outras ações solicitadas nos dados pessoais, onde for possível.
- **Restringir**: restrinja o processamento de dados pessoais, removendo licenças para vários serviços do Azure ou desligando os serviços desejados quando possível. Você também pode remover dados da nuvem da Microsoft e mantê-los no local ou em outro local.
- **Exclusão:** remova permanentemente os dados pessoais que residem na nuvem da Microsoft.
- **Exportar/Receber (Portabilidade):** forneça uma cópia eletrônica (em formato legível para computador) de dados pessoais ou informações pessoais para o titular dos dados. Os dados pessoais do CCPA são quaisquer informações relacionadas a uma pessoa, identificável ou não. Não há distinção entre as funções pública, privada ou de trabalho de uma pessoa. O termo definido "informações pessoais" se alinha aproximadamente aos "dados pessoais" do RGPD. No entanto, o CCPA também inclui dados da família e do domicílio. Para obter mais informações sobre o CCPA, confira a [Lei de Privacidade do Consumidor da Califórnia](offering-ccpa.md) e as [Perguntas Frequentes Sobre a Lei de Privacidade do Consumidor da Califórnia](ccpa-faq.yml).

Cada seção deste guia descreve os procedimentos técnicos que uma organização controladora de dados pode realizar para responder a uma DSR para dados pessoais na nuvem da Microsoft.

## <a name="terminology"></a>Terminologia

Veja a seguir as definições dos termos que são relevantes para este guia.

- **Controlador:** a pessoa física ou jurídica, autoridade pública, órgão ou outra entidade que, sozinha ou em conjunto com terceiros, determina os fins e os meios do processamento de dados pessoais, onde tais fins e meios são determinados por lei da União ou Estado-Membro, o controlador ou os critérios específicos para sua indicação podem ser fornecidos por lei da União ou Estado-Membro.
- **Dados pessoais e titular dos dados:** qualquer informação relativa a uma pessoa natural identificada ou identificável (“titular dos dados”); uma pessoa natural identificável é aquela que pode ser identificada, direta ou indiretamente, especialmente por referência a um identificador, como nome, um número de identificação, dados de localização, um identificador online ou um ou mais fatores específicos de natureza física, fisiológica, genética, mental, econômica, cultural ou social dessa pessoa natural.
- **Processador:** uma pessoa física ou jurídica, autoridade pública, órgão ou outra entidade que processa dados pessoais em nome do controlador.
- **Dados do cliente:** todos os dados, incluindo texto, som, vídeo ou arquivos de imagem e software que são fornecidos à Microsoft, por ou em nome de um cliente, através do uso de serviço corporativo. Os dados do cliente incluem (1) informações de identificação de usuários finais (por exemplo, nomes de usuário e informações de contato no Azure Active Directory) e conteúdo do cliente que um cliente carrega ou cria em serviços específicos (por exemplo, conteúdo de cliente na conta de Armazenamento do Azure, conteúdo do cliente em um Banco de Dados SQL do Azure ou imagem da máquina virtual do cliente em máquinas virtuais do Azure).
- **Logs gerados pelo sistema:** logs e dados relacionados gerados pela Microsoft que nos ajudam a fornecer os serviços corporativos aos usuários. Logs gerados pelo sistema contêm, principalmente, dados pseudônimos, tais como identificadores exclusivos, normalmente um número gerado pelo sistema que não pode identificar sozinho um indivíduo, mas que é usado para fornecer serviços corporativos aos usuários. Logs gerados pelo sistema também podem conter informações de identificação dos usuários finais, como nomes de usuário.

## <a name="how-to-use-this-guide"></a>Como usar este guia

Este guia consiste em duas partes:

- **Parte 1: respondendo às Solicitações do Titular dos Dados para Dados do Cliente:** a Parte 1 deste guia discute como acessar, retificar, restringir, excluir e exportar dados de aplicativos nos quais você criou dados. Esta seção detalha como executar as solicitações do titular dos dados em relação ao Conteúdo do Cliente e também às informações identificáveis dos usuários finais.
- **Parte 2: responder às Solicitações de Titulares dos Dados por Logs Gerados pelo Sistema:** quando você usa os serviços corporativos da Microsoft, nós geramos informações, conhecidas como logs gerados pelo sistema, para fornecer o serviço. A parte 2 deste guia descreve como acessar, excluir e exportar tais informações para o Azure.

## <a name="understanding-dsrs-for-azure-active-directory-and-microsoft-service-accounts"></a>Entender noções básicas dos DSRs para contas de serviço do Azure Active Directory e Microsoft

Ao considerar serviços fornecidos para clientes empresariais, a execução de DSRs sempre deve ser compreendida no contexto de um locatário específico do Azure Active Directory (AAD). As DSRs sempre são executadas em um determinado locatário do AAD. Se um usuário fizer parte de vários locatários, é importante enfatizar que uma determinada DSR é executada *apenas* no contexto do locatário específico no qual a solicitação foi recebida. É essencial entender que isso significa que a execução da DSR por um cliente corporativo **não** afeta os dados de um cliente corporativo adjacente.

O mesmo também se aplica a contas de serviço da Microsoft (MSA) no contexto dos serviços fornecidos a um cliente corporativo: a execução de uma DSR em uma conta MSA *associada a um locatário do AAD* **se refere apenas** aos dados dentro do locatário. Além disso, é importante compreender o seguinte ao lidar com a contas MSA em um locatário:

- Se um usuário MSA criar uma assinatura do Azure, a assinatura será tratada como se fosse um locatário do AAD. Consequentemente, o escopo dessas DSRs está no locatário, como descrito acima.
- Se for excluída uma assinatura do Azure criada por uma conta MSA, **isso não afeta** a conta MSA em si. Novamente, como mencionado acima, as DSRs em execução em assinaturas do Azure são limitadas ao escopo do locatário em si.

As DSRs em relação à própria conta MSA, **fora de um determinado locatário**, são executadas por meio do Painel de privacidade do cliente. Consulte o Guia de solicitações de titulares de dados do Windows para saber mais.

## <a name="part-1-dsr-guide-for-customer-data"></a>Parte 1: guia de DSR para dados do cliente

### <a name="executing-dsrs-against-customer-data"></a>Executando DSRs contra dados do cliente

A Microsoft fornece a capacidade de acessar, excluir e exportar determinados Dados do cliente através do Portal do Azure e também diretamente através de APIs (interfaces de programação de aplicativos) preexistentes ou interfaces de usuário (UIs) para serviços específicos (também chamados de *experiências no produto*). Detalhes sobre essas experiências no produto estão descritos na documentação de referência dos respectivos serviços.

>[!IMPORTANT]  
> Os serviços que suportam DSRs no produto requerem o uso direto da API (Interface de Programação de Aplicativos) do serviço ou da Interface do usuário (UI), descrevendo as operações CRUD aplicáveis (criar, ler, atualizar, excluir). Consequentemente, a execução de DSRs em um determinado serviço deve ser feita além da execução de um DSR no Portal do Azure para concluir uma solicitação total para um determinado titular de dados. Consulte a documentação de referência de serviços específicos para obter mais detalhes.

### <a name="step-1-discover"></a>Etapa 1: Descoberta

A primeira etapa para responder a um DSR é encontrar os dados pessoais que são o assunto da solicitação. Esta primeira etapa — encontrar e revisar os dados pessoais em questão — o ajudará a determinar se um DSR atende aos requisitos da sua organização para honrar ou recusar um DSR. Por exemplo, depois de encontrar e revisar os dados pessoais em questão, você pode determinar que a solicitação não atende aos requisitos da sua organização, pois isso pode afetar adversamente os direitos e liberdades de outras pessoas.

Depois de encontrar os dados, você pode executar uma ação específica que atenda à solicitação feita pelo titular dos dados.

O [Azure Active Directory](https://azure.microsoft.com/services/active-directory/) é um serviço da Microsoft para gerenciamento de identidades e diretórios com vários locatários baseados na nuvem. Você pode localizar informações de identificação de usuários finais, como perfis de usuários de clientes e funcionários, e informações de trabalho de usuários, que contenham dados pessoais do ambiente do [Azure Active Directory](https://azure.microsoft.com/services/active-directory/) (AAD) usando o [portal do Azure](https://portal.azure.com/).

Isso é especialmente útil se você quiser localizar ou alterar dados pessoais de um usuário específico. Também é possível adicionar ou alterar informações de trabalho e de perfil de usuário. Você deve entrar com uma conta de administrador global do diretório.

#### <a name="how-do-i-locate-or-view-user-profile-and-work-information"></a>Como localizar ou exibir informações de trabalho e de perfil de um usuário?

1. Entre no [portal do Azure](https://portal.azure.com/) com uma conta de administrador global do diretório.

2. Selecione **Azure Active Directory**.

     ![Selecione Todos os serviços.](../media/gdpr-azure-dsr-azure-portal.png)

3. Selecione **Usuários**.

     ![Selecione usuários.](../media/gdpr-azure-dsr-azure-all-users.png)

4. No painel **Todos os usuários**, selecione um usuário na lista e, em seguida, no painel do usuário selecionado, selecione **Perfil** para visualizar as informações de perfil do usuário que possam conter dados pessoais.

    ![Selecione perfil.](../media/gdpr-azure-dsr-azure-user-profile.png)

5. Se você precisa adicionar ou alterar as informações do perfil do usuário, selecione **Editar** na barra de comandos e selecione **Salvar** depois de fazer as alterações.

#### <a name="service-specific-interfaces"></a>Interfaces específicas do serviço

A Microsoft oferece a capacidade de descobrir os dados dos clientes diretamente por APIs (interfaces de programação de aplicativos) preexistentes ou por IUs (interfaces de usuário) para serviços específicos. Os detalhes são descritos na documentação de referência dos respectivos serviços e descrevem as operações aplicáveis de CRUD (criar, ler, atualizar e excluir).

### <a name="step-2-access"></a>Etapa 2: Acesso

Depois de encontrar os Dados do cliente que contêm dados pessoais que são potencialmente responsivos a um DSR, você e sua organização decidem quais dados devem fornecer ao titular dos dados. Você pode fornecer-lhes uma cópia do documento real, uma versão adequadamente editada ou uma captura de tela das partes que você considera adequadas de serem compartilhadas. Para cada uma dessas respostas à uma solicitação de acesso, você precisará recuperar uma cópia do documento ou outro item que contenha os dados responsivos.

Ao oferecer uma cópia ao titular dos dados, talvez você tenha que remover ou redigir informações pessoais sobre outros titulares de dados e quaisquer informações confidenciais.

#### <a name="azure-active-directory"></a>Azure Active Directory

A Microsoft oferece um portal e experiências de produtos, proporcionando ao administrador de locatários do cliente corporativo a capacidade de gerenciar solicitações de acesso a DSR. As solicitações de acesso a DSR permitem acessar dados pessoais do usuário, incluindo: (a) informações de identificação sobre um usuário final e (b) logs gerados pelo sistema.

#### <a name="service-specific-interfaces"></a>Interfaces específicas do serviço

A Microsoft oferece a capacidade de descobrir os dados dos clientes diretamente por APIs (interfaces de programação de aplicativos) preexistentes ou por IUs (interfaces de usuário) para serviços específicos. Os detalhes são descritos na documentação de referência dos respectivos serviços e descrevem as operações aplicáveis de CRUD (criar, ler, atualizar e excluir).

### <a name="step-3-rectify"></a>Etapa 3: Retificação

Se um titular dos dados pediu para corrigir os dados pessoais que residem nos dados da sua organização, você e sua organização precisam determinar se é apropriado aceitar a solicitação. A correção dos dados pode incluir a execução de ações como editar, redigir ou remover dados pessoais de um documento ou de outro tipo de item. A maneira mais apropriada para fazer isso com dados do Suporte da Microsoft e do Microsoft FastTrack é fornecida abaixo.

#### <a name="azure-active-directory"></a>Azure Active Directory

Clientes corporativos têm a capacidade de gerenciar solicitações de retificação de DSR, incluindo recursos de edição limitados por natureza de um determinado serviço da Microsoft. Como processador de dados, a Microsoft não oferece a capacidade de corrigir logs gerados pelo sistema, pois refletem atividades concretas e constituem um registro do histórico de eventos em serviços da Microsoft. Em relação ao Azure Active Directory, os recursos de edição limitados existem para retificar as informações de identificação sobre usuários finais, como descrito abaixo.

##### <a name="azure-active-directory-rectifycorrect-inaccurate-or-incomplete-personal-data"></a>Azure Active Directory: retificar/corrigir dados pessoais incorretos ou incompletos

Você pode corrigir, atualizar ou excluir informações de identificação sobre usuários finais, como perfis de usuário de funcionários e clientes, e informações de trabalho de usuário que contêm dados pessoais, como nome do usuário, título de trabalho, endereço ou número de telefone no seu ambiente [Azure Active Directory](https://azure.microsoft.com/services/active-directory/) (AAD) usando a [portal do Azure](https://portal.azure.com/). Você deve entrar com uma conta de administrador global do diretório.

###### <a name="how-do-i-correct-or-update-user-profile-and-work-information-in-azure-active-directory"></a>Como corrigir ou atualizar o perfil de usuário e as informações de trabalho no Azure Active Directory?

1. Entre no [portal do Azure](https://portal.azure.com/) com uma conta de administrador global do diretório.

2. Selecione **Azure Active Directory**.

    ![Selecione Todos os serviços.](../media/gdpr-azure-dsr-azure-portal.png)

3. Selecione **Usuários**.

    ![Selecione usuários.](../media/gdpr-azure-dsr-azure-all-users.png)

4. No painel **Todos os usuários**, selecione um usuário na lista e, em seguida, no painel do usuário selecionado, selecione **Perfil** para visualizar as informações do perfil do usuário que precisam ser corrigidas ou atualizadas.

    ![Selecione o perfil de usuário.](../media/gdpr-azure-dsr-azure-user-profile.png)

5. Corrija ou atualize as informações do perfil do usuário, incluindo as informações de trabalho, selecionando **Editar** na barra de comandos e selecione  **Salvar** depois de fazer as alterações.

    ![Selecione editar.](../media/gdpr-azure-dsr-azure-edit-user-profile.png)

#### <a name="service-specific-interfaces"></a>Interfaces específicas de serviços

A Microsoft oferece a capacidade de descobrir os dados dos clientes diretamente por APIs (interfaces de programação de aplicativos) preexistentes ou por IUs (interfaces de usuário) para serviços específicos. Os detalhes são descritos na documentação de referência dos respectivos serviços e descrevem as operações aplicáveis de CRUD (criar, ler, atualizar e excluir).

### <a name="step-4-restrict"></a>Etapa 4: Restrição

Os titulares de dados podem solicitar que você restrinja o processamento dos dados pessoais. Fornecemos o Portal do Azure e APIs (interfaces de programação de aplicativos) preexistentes ou IUs (interfaces de usuário). Essas experiências proporcionam ao administrador de locatários do cliente corporativo a capacidade de gerenciar tais DSRs por meio de uma combinação de exportação e exclusão de dados. Um cliente pode (1) exportar uma cópia eletrônica de dados pessoais do usuário, incluindo (a) conta(s), (b) logs gerados pelo sistema e (c) logs associados, seguidos de (2) exclusão da conta e dos dados associados que residem em sistemas da Microsoft.

### <a name="step-5-delete"></a>Etapa 5: Exclusão

O "direito de apagar" por meio da remoção de dados pessoais do cliente de uma organização é uma importante proteção do RGPD. A remoção de dados pessoais compreende a exclusão de todos os dados pessoais e logs gerados pelo sistema, exceto informações do log de auditoria. Quando um usuário é **excluído temporariamente** (veja detalhes abaixo), a conta é desativada por 30 dias. Se nenhuma ação for executada durante o período de 30 dias, o usuário é **excluído permanentemente** (novamente, veja os detalhes abaixo). Em uma **exclusão permanente**, a conta de usuário, os dados pessoais e os logs gerados pelo sistema são eliminados após mais 30 dias adicionais. Se um administrador de locatário emitir imediatamente uma **exclusão permanente**, a conta de usuário, os dados pessoais e os logs gerados pelo sistema são eliminados dentro de 30 dias da data de emissão.

> [!IMPORTANT]
> Você deve ser um administrador de locatários para excluir um usuário do locatário.

#### <a name="delete-a-user-and-associated-data-through-the-azure-portal"></a>Excluir um usuário e os dados associados no portal do Azure

Após receber uma solicitação de exclusão de um titular de dados, você pode usar o portal do Azure para excluir um usuário e as informações pessoais associadas, assim como logs gerados pelo sistema.

Excluir dados significa também excluir o usuário do locatário. Inicialmente os usuários são excluídos temporariamente, o que significa que a conta pode ser recuperada por um administrador de locatário em até 30 dias após ser marcada para exclusão temporária. Após 30 dias, a conta será automática e permanentemente excluída do locatário. Antes desses 30 dias, você pode excluir manualmente na Lixeira o usuário excluído temporariamente.

Veja a seguir o processo detalhado para excluir usuários de seu locatário.

1. Acesse o portal do Azure e localize o usuário.

2. Exclua o usuário. Ao excluir o usuário inicialmente, a conta do usuário é enviada para a Lixeira. **Neste ponto, o usuário é excluído temporariamente, ou seja, a conta é desabilitada, mas não eliminada do Azure Active Directory.**

3. Acesse a lista de usuários excluídos recentemente e exclua permanentemente o usuário. **Agora o usuário é excluído permanentemente (também conhecido como exclusão irreversível), o que significa que a conta foi eliminada do Azure Active Directory**

###### <a name="to-delete-a-user-from-an-azure-tenant"></a>Para excluir um usuário de um locatário do Azure

1. Entre no [Portal do Azure](https://portal.azure.com/) com uma conta de administrador global do diretório.

2. Selecione **Azure Active Directory**.

    ![Selecione Todos os serviços.](../media/gdpr-azure-dsr-azure-portal.png)

3. Selecione **Usuários**.

    ![Selecione usuários.](../media/gdpr-azure-dsr-azure-all-users.png)

4. Marque a caixa ao lado do usuário que você deseja excluir, selecione **Excluir usuário** e selecione **Sim** na caixa que confirma se você deseja excluir o usuário.

    ![Gerenciamento de usuários.](../media/gdpr-azure-dsr-azure-selected-user.png)

5. Na folha  **Todos os usuários** , selecione **Usuários excluídos**.

    ![Exibir perfil do usuário.](../media/gdpr-azure-dsr-azure-deleted-user.png)

4. Selecione o mesmo usuário novamente, selecione  **Excluir permanentemente** na barra de comandos e selecione  **Sim**  na caixa que pergunta se você tem certeza.

>[!IMPORTANT]  
>Lembre-se que, ao clicar em **Sim**, você exclui permanente e irrevogavelmente o usuário, todos os dados associados e os logs gerados pelo sistema. Se você fizer isso por engano, será necessário adicioná-lo manualmente ao locatário. Os dados associados e os logs gerados pelo sistema não podem ser recuperados.

   ![Exibir informações de trabalho do usuário.](../media/gdpr-azure-dsr-azure-permanently-deleted-user.png)

#### <a name="service-specific-interfaces"></a>Interfaces específicas do serviço

A Microsoft oferece a capacidade de descobrir os dados dos clientes diretamente por APIs (interfaces de programação de aplicativos) preexistentes ou por IUs (interfaces de usuário) para serviços específicos. Os detalhes são descritos na documentação de referência dos respectivos serviços e descrevem as operações aplicáveis de CRUD (criar, ler, atualizar e excluir).

## <a name="step-6-export"></a>Etapa 6: Exportação

O "direito de portabilidade de dados" permite que o titular de dados solicite uma cópia dos seus dados pessoais em formato eletrônico (que é um "formato estruturado, comumente usado, interoperável e legível por máquina") que pode ser transmitido para outro controlador de dados. O Azure dá suporte a isso ao habilitar a sua organização a exportar dados no formato nativo JSON para o contêiner de armazenamento especificado do Azure.

>[!IMPORTANT]
>Você deve ser um administrador de locatários para exportar dados de usuário do locatário.

### <a name="azure-active-directory"></a>Azure Active Directory

Em relação aos dados do cliente, a Microsoft oferece um portal e experiências internas do produto que proporcionam ao administrador de locatários do cliente corporativo a capacidade de gerenciar solicitações de exportação de informações de identificação de um usuário final.

### <a name="service-specific-interfaces"></a>Interfaces específicas do serviço

A Microsoft oferece a capacidade de descobrir os dados dos clientes diretamente por APIs (interfaces de programação de aplicativos) preexistentes ou por IUs (interfaces de usuário) para serviços específicos. Os detalhes são descritos na documentação de referência dos respectivos serviços e descrevem as operações aplicáveis de CRUD (criar, ler, atualizar e excluir).

## <a name="part-2-system-generated-logs"></a>Parte 2: Logs gerados pelo sistema

A Microsoft também proporciona a capacidade de acessar, excluir e exportar determinados logs gerados pelo sistema associados à utilização do Azure por um usuário.

>[!IMPORTANT]
> Não há suporte para a capacidade de restringir ou corrigir dados nos logs gerados pelo sistema. Logs gerados pelo sistema constituem ações concretas realizadas na nuvem da Microsoft e dados de diagnóstico. A modificação de tais dados comprometeria o registro histórico de ações e aumentaria os riscos de segurança e fraude.

### <a name="executing-dsrs-against-system-generated-logs"></a>Executar as DSRs em logs gerados pelo sistema

A Microsoft fornece a capacidade de acessar, excluir e exportar determinados logs gerados pelo sistema por meio do Portal do Azure e, também, diretamente por meio de interfaces de programação ou interfaces de usuário para serviços específicos. Os detalhes são descritos na documentação de referência desses respectivos serviços.

>[!IMPORTANT]  
> Serviços de suporte a DSRs de produtos exigem o uso direto de APIs (interfaces de programação de aplicativos) preexistentes ou IUs (interfaces de usuário). Consequentemente, **é necessário executar as DSRs e também executar uma DSR no Portal do Azure para concluir totalmente a solicitação de um determinado titular de dados. Consulte a documentação de referência de serviços específicos para saber mais.**

### <a name="step-1-access"></a>Etapa 1: Acessar

O administrador de locatário é a única pessoa em sua organização que tem acesso aos logs geradas pelo sistema associados ao uso do Azure por um usuário específico. Dados recuperados para uma solicitação de acesso são fornecidos em um formato legível por máquina em arquivos que permitem ao usuário saber com quais serviços os dados estão associados. Como mencionado acima, os dados recuperados não incluem dados que possam comprometer a segurança do serviço.

#### <a name="azure-active-directory"></a>Azure Active Directory

A Microsoft oferece um portal e experiências de produto, proporcionando ao administrador de locatários do cliente corporativo a capacidade de gerenciar solicitações de acesso que permitem acessar dados pessoais do usuário, incluindo: (a) informações de identificação sobre um usuário final e (b) logs gerados pelo sistema. O processo é idêntico ao descrito na seção do Azure Active Directory da Parte 1, Etapa 2: Acessar.

#### <a name="service-specific-interfaces"></a>Interfaces específicas do serviço

A Microsoft oferece a capacidade de descobrir os dados dos clientes diretamente por APIs (interfaces de programação de aplicativos) preexistentes ou por IUs (interfaces de usuário) para serviços específicos. Os detalhes são descritos na documentação de referência dos respectivos serviços e descrevem as operações aplicáveis de CRUD (criar, ler, atualizar e excluir).

### <a name="step-2-delete"></a>Etapa 2: Excluir

O administrador de locatário é a única pessoa em sua organização que pode executar uma solicitação de exclusão de DSR de um determinado usuário em um locatário do Azure.

#### <a name="azure-active-directory"></a>Azure Active Directory

A Microsoft oferece um portal e experiências de produto, proporcionando ao administrador de locatários do cliente corporativo a capacidade de gerenciar solicitações de exclusão de DSR, que seguem o mesmo processo descrito em Excluir um usuário e dados associados na seção do portal do Azure da Parte 1, Etapa 5: Excluir.

#### <a name="service-specific-interfaces"></a>Interfaces específicas do serviço

A Microsoft oferece a capacidade de descobrir os dados dos clientes diretamente por APIs (interfaces de programação de aplicativos) preexistentes ou por IUs (interfaces de usuário) para serviços específicos. Os detalhes são descritos na documentação de referência dos respectivos serviços e descrevem as operações aplicáveis de CRUD (criar, ler, atualizar e excluir).

### <a name="step-3-export"></a>Etapa 3: Exportação

O administrador de locatários é a única pessoa em sua organização que tem acesso aos logs gerados pelo sistema associados ao uso do Azure por um usuário específico. Dados recuperados para uma solicitação de exportação são fornecidos em um formato legível por máquina em arquivos que permitem ao usuário saber com quais serviços os dados estão associados. Como mencionado acima, dados recuperados não incluem dados que possam comprometer a segurança ou estabilidade do serviço.

#### <a name="export-system-generated-logs-using-the-azure-portal"></a>Exportar logs gerados pelo sistema usando o portal do Azure

Após receber uma solicitação de exportação de um titular de dados, você pode usar o portal do Azure para exportar os logs gerados pelo sistema associados a um determinado usuário.

Veja a seguir o processo detalhado para exportar os dados de seu locatário.

1. Acesse o portal do Azure e crie uma solicitação de exportação em nome do usuário.
2. Exporte os dados e envie o arquivo para o usuário.

###### <a name="to-export-a-users-info-from-an-azure-tenant"></a>Para exportar informações de um usuário de um locatário do Azure

1. Abra o portal do Azure, selecione **Todos os serviços**, digite *Política* para filtrar e selecione **Política**.

     ![Filtro Todos os serviços](../media/gdpr-azure-dsr-azure-policy.png)

2. Na folha **Política**, selecione **Privacidade do usuário**, selecione **Gerenciar Solicitações de Usuário** e selecione **Adicionar solicitação de exportação**.

    ![Adicionar solicitação de exportação .](../media/gdpr-azure-dsr-azure-add-export-request.png)

3. Preencha a **Solicitação de exportação de dados**:

    ![Nova solicitação de exportação de dados.](../media/gdpr-azure-dsr-azure-export-data-request.png)

- **Usuário.** Digite o endereço de email do usuário do Azure Active Directory que solicitou a exportação.
- **Assinatura.** Selecione a conta que você usa para relatar o uso de recursos e cobrar pelos serviços. Esse também é o local de sua conta de armazenamento do Azure.
- **Conta de armazenamento.** Selecione o local do Armazenamento do Azure (Blob). Para saber mais, consulte o artigo [Introdução ao Armazenamento do Microsoft Azure: armazenamento de blob](/azure/storage/common/storage-introduction#blob-storage).
- **Contêiner.** Crie um novo contêiner (ou selecione um existente) como o local de armazenamento para os dados de privacidade exportados do usuário.

4. Selecione **Criar**. 

A solicitação de exportação entra no status **Pendente**. Você pode exibir o status do relatório na folha **Privacidade do usuário– Visão geral**.

>[!IMPORTANT]  
>Como dados pessoais podem vir de vários sistemas, é possível que o processo de exportação possa levar até um mês para ser concluído.

#### <a name="service-specific-interfaces"></a>Interfaces específicas de serviços

A Microsoft oferece a capacidade de descobrir os dados dos clientes diretamente por APIs (interfaces de programação de aplicativos) preexistentes ou por IUs (interfaces de usuário) para serviços específicos. Os detalhes são descritos na documentação de referência dos respectivos serviços e descrevem as operações aplicáveis de CRUD (criar, ler, atualizar e excluir).

### <a name="notify-about-exporting-or-deleting-issues"></a>Notificar problemas de exportação ou exclusão

Se você tiver problemas ao exportar ou excluir dados do Portal do Azure, acesse a folha **Ajuda e suporte** do portal do Azure e envie um novo tíquete na folha **Gerenciamento de Assinaturas > Outra Solicitação de Segurança e Conformidade > Privacidade e Solicitações de RGPD**.

## <a name="learn-more"></a>Saiba mais

- [Central de Confiabilidade da Microsoft](https://www.microsoft.com/trust-center/privacy/gdpr-overview)
