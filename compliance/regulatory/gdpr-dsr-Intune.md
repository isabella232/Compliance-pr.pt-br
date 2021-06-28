---
title: Solicitações de Entidades de Dados para o RGPD e CCPA
description: Aprenda como encontrar e agir sobre dados pessoais e responder às solicitações de DSR e CCPA de clientes que usam o Microsoft Intune.
keywords: Microsoft 365, Microsoft 365 Education, documentação do Microsoft 365, RGPD, CCPA
localization_priority: Priority
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
ms.custom:
- seo-marvel-mar2020
hideEdit: true
titleSuffix: Microsoft GDPR
ms.openlocfilehash: ac172e68f025161fac9c68cc465c5eae9ada930f
ms.sourcegitcommit: 5d8e670e9d9968458047b51b6b2930f7bd14a011
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/25/2021
ms.locfileid: "53141512"
---
# <a name="intune-data-subject-requests-for-the-gdpr-and-ccpa"></a>Solicitações de Entidades de Dados para o RGPD e CCPA

O Regulamento Geral [de Proteção de Dados da União Europeia (GDPR)](https://ec.europa.eu/justice/data-protection/reform/index_en.htm) concede direitos às pessoas (conhecidas no regulamento como *titulares de dados*) para gerenciarem os dados pessoais coletados por um empregador ou outro tipo de agência ou organização (conhecido como *controlador de dados* ou apenas *controlador*). Os dados pessoais são definidos de maneira ampla, sob o GDPR, como qualquer dado relacionado à uma pessoa física identificada ou identificável. O GDPR concede aos titulares de dados direitos específicos sobre seus dados pessoais; esses direitos incluem obter cópias dos dados pessoais, solicitar correções, restringir o processamento, excluí-los ou recebê-los em formato eletrônico para que possam ser movidos para outro controlador. Uma solicitação formal de um titular de dados a um controlador para executar uma ação em seus dados pessoais é chamada de *Solicitação de titular de dados* ou DSR.

Da mesma forma, a Lei de Privacidade do Consumidor da Califórnia (CCPA), fornece direitos e obrigações de privacidade aos consumidores da Califórnia, incluindo direitos semelhantes aos Direitos do Titular dos Dados do RGDP, como o direito de excluir, acessar e receber (portabilidade) suas informações pessoais.  O CCPA também fornece certas divulgações, proteções contra discriminação ao eleger direitos de exercício e requisitos de "aceitação/recusa" para determinadas transferências de dados classificadas como "vendas". As vendas são amplamente definidas para incluir o compartilhamento de dados para uma consideração valiosa. Para obter mais informações sobre o CCPA, confira a [Lei de Privacidade do Consumidor da Califórnia](offering-ccpa.md) e as [Perguntas Frequentes Sobre a Lei de Privacidade do Consumidor da Califórnia](ccpa-faq.yml).

O guia descreve como usar os produtos, serviços e ferramentas administrativas da Microsoft para ajudar os nossos clientes controladores a encontrar dados pessoais e agir em relação a eles para responder a DSRs. Especificamente, isso inclui como localizar, acessar e agir em dados pessoais que residem na nuvem da Microsoft. Veja aqui uma breve visão geral dos processos descritos neste guia:

- **Descobrir**: use ferramentas de pesquisa e descoberta para localizar mais facilmente os dados do cliente que podem estar sujeitos a uma DSR. Assim que os documentos potencialmente responsivos forem coletados, você pode executar uma ou mais das ações de DSR descritas nas etapas a seguir para responder à solicitação. Como alternativa, você pode determinar que a solicitação não atende às diretrizes da sua organização para responder as DSRs.
- **Acesso:** recupere dados pessoais que residem na nuvem da Microsoft e, se solicitado, faça uma cópia para disponibilizar para o titular dos dados.
- **Retificação:** faça alterações ou implemente outras ações solicitadas nos dados pessoais, onde for possível.
- **Restringir**: restrinja o processamento de dados pessoais, removendo licenças para vários serviços do Azure ou desligando os serviços desejados quando possível. Você também pode remover dados da nuvem da Microsoft e mantê-los no local ou em outro local.
- **Exclusão:** remova permanentemente os dados pessoais que residem na nuvem da Microsoft.
- **Exportar/Receber (Portabilidade):** forneça uma cópia eletrônica (em formato legível para computador) de dados pessoais ou informações pessoais para o titular dos dados. Os dados pessoais do CCPA são quaisquer informações relacionadas a uma pessoa, identificável ou não. Não há distinção entre as funções pública, privada ou de trabalho de uma pessoa. O termo definido "informações pessoais" se alinha aproximadamente aos "dados pessoais" do RGPD. No entanto, o CCPA também inclui dados da família e do domicílio. Para obter mais informações sobre o CCPA, confira a [Lei de Privacidade do Consumidor da Califórnia](offering-ccpa.md) e as [Perguntas Frequentes Sobre a Lei de Privacidade do Consumidor da Califórnia](ccpa-faq.yml).

Cada seção deste guia descreve os procedimentos técnicos que uma organização controladora de dados pode realizar para responder a uma DSR para dados pessoais na nuvem da Microsoft.

#### <a name="terminology"></a>Terminologia

A lista a seguir fornece as definições dos termos que são relevantes para este guia.

- **Controlador:** a pessoa física ou jurídica, autoridade pública, órgão ou outra entidade que, sozinha ou em conjunto com terceiros, determina os fins e os meios do processamento de dados pessoais, onde tais fins e meios são determinados por lei da União ou Estado-Membro, o controlador ou os critérios específicos para sua indicação podem ser fornecidos por lei da União ou Estado-Membro.
- **Dados pessoais e titular dos dados:** qualquer informação relativa a uma pessoa natural identificada ou identificável (“titular dos dados”); uma pessoa natural identificável é aquela que pode ser identificada, direta ou indiretamente, especialmente por referência a um identificador, como nome, um número de identificação, dados de localização, um identificador online ou um ou mais fatores específicos de natureza física, fisiológica, genética, mental, econômica, cultural ou social dessa pessoa natural.
- **Processador:** uma pessoa física ou jurídica, autoridade pública, órgão ou outra entidade que processa dados pessoais em nome do controlador.
- **Dados do Cliente**: todos os dados, incluindo todos os arquivos de texto, som, vídeo ou imagem e software, fornecidos à Microsoft por ou em nome de um cliente por meio do serviço corporativo. Os Dados do Cliente incluem (1) informações identificáveis de usuários finais (por exemplo, nomes de usuário e informações de contato no Azure Active Directory) e Conteúdo do Cliente que um cliente carrega ou cria em serviços específicos (por exemplo, conteúdo do cliente em uma conta de Armazenamento do Microsoft Azure, o conteúdo do cliente de um Banco de Dados SQL do Azure ou a imagem da máquina virtual de um cliente em Máquinas Virtuais do Azure).
- **Logs Gerados pelo Sistema:** logs e dados relacionados gerados pela Microsoft que ajudam a Microsoft a fornecer serviços corporativos aos usuários. Os logs gerados pelo sistema contêm principalmente dados pseudonimizados, como identificadores únicos - normalmente um número gerado pelo sistema que não consegue identificar sozinho uma pessoa, mas é usado para fornecer os serviços corporativos aos usuários. Os logs gerados pelo sistema também podem conter informações identificáveis sobre os usuários finais, como um nome de usuário.

#### <a name="how-to-use-this-guide"></a>Como usar este guia

Este guia consiste em duas partes:

- **Parte 1: respondendo às Solicitações do Titular dos Dados para Dados do Cliente:** a Parte 1 deste guia discute como acessar, retificar, restringir, excluir e exportar dados de aplicativos nos quais você criou dados. Esta seção detalha como executar as solicitações do titular dos dados em relação ao Conteúdo do Cliente e também às informações identificáveis dos usuários finais.
- **Parte 2**: respondendo a Solicitações de Titulares de dados para Logs Gerados pelo Sistema: quando você usa os serviços corporativos da Microsoft, a Microsoft gera algumas informações, conhecidas como Logs Gerados pelo Sistema, para fornecer o serviço. A Parte 2 deste guia discute como acessar, excluir e exportar essas informações para o Azure.

### <a name="understanding-dsrs-for-azure-active-directory-and-microsoft-intune"></a>Noções básicas sobre DSRs para Azure Active Directory e Microsoft Intune

Ao considerar serviços fornecidos para clientes empresariais, a execução de DSRs sempre deve ser compreendida no contexto de um locatário específico do Azure Active Directory. As DSRs sempre são executadas em um determinado locatário do Azure Active Directory. Se um usuário fizer parte de vários locatários, é importante enfatizar que uma determinada DSR é executada *apenas* no contexto do locatário específico no qual a solicitação foi recebida. Esse contexto é essencial para entender que isso significa que a execução da DSR por um cliente corporativo **não** afeta os dados de um cliente corporativo adjacente.

O mesmo também se aplica ao Microsoft Intune fornecido a um cliente corporativo: execução de um DSR em uma conta do Intune *associada a um locatário do Azure Active Directory* **se refere apenas** aos dados dentro do locatário. Além disso, é importante compreender o seguinte ao lidar com a contas do Intune em um locatário:

- Se um usuário do Intune criar uma assinatura do Azure, a assinatura será tratada como se fosse um locatário do Azure Active Directory. Consequentemente, o escopo dessas DSRs está no locatário, como descrito anteriormente.
- Se for excluída uma assinatura do Azure criada por uma conta do Intune, **isso não afetará** a conta do Intune em si. Novamente, como mencionado anteriormente, os DSRs em execução em assinaturas do Azure são limitadas ao escopo do locatário em si.

Os DSRs em relação à própria conta do Intune, **fora de um determinado locatário**, são executados por meio do Painel de Privacidade do Cliente. Consulte o Guia de Solicitações de Titulares de Dados do Windows para saber mais.

## <a name="part-1-dsr-guide-for-customer-data"></a>Parte 1: Guia DSR para dados de clientes

### <a name="executing-dsrs-against-customer-data"></a>Executar os DSRs em relação aos dados de cliente

A Microsoft fornece a capacidade de acessar, excluir e exportar determinados dados do cliente através do portal do Azure e também diretamente através de APIs (interfaces de programação de aplicativos) preexistentes ou interfaces de usuário (UIs) para serviços específicos (também chamados de *experiências no produto*). Detalhes sobre essas experiências no produto estão descritas na documentação de referência dos respectivos serviços.

>[!IMPORTANT]  
>Os serviços que suportam DSRs no produto requerem o uso direto da API (Interface de Programação de Aplicativos) do serviço ou da Interface do usuário (UI), descrevendo as operações CRUD aplicáveis (criar, ler, atualizar, excluir). Consequentemente, a execução de DSRs em um determinado serviço deve ser feita além da execução de um DSR no Portal do Azure para concluir uma solicitação total para um determinado titular de dados. Consulte a documentação de referência de serviços específicos para obter mais detalhes.

### <a name="step-1-discover"></a>Etapa 1: Descoberta

A primeira etapa para responder a um DSR é encontrar os dados pessoais que são o assunto da solicitação. Esta primeira etapa - encontrar e revisar os dados pessoais em questão - o ajudará a determinar se um DSR atende aos requisitos da sua organização para honrar ou recusar um DSR. Por exemplo, depois de encontrar e revisar os dados pessoais em questão, você pode determinar que a solicitação não atende aos requisitos da sua organização, pois isso pode afetar adversamente os direitos e liberdades de outras pessoas.

Depois de encontrar os dados, você pode executar uma ação específica que atenda à solicitação feita pelo titular dos dados. Para obter detalhes, confira os seguintes recursos:

- [Conjunto de dados](/intune/privacy-data-collect)
- [Armazenamento e processamento de dados](/intune/privacy-data-store-process)
- [Exibir dados pessoais](/intune/privacy-data-view-correct#view-personal-data)

### <a name="step-2-access"></a>Etapa 2: Acesso

Depois de encontrar os Dados do cliente que contêm dados pessoais que são potencialmente responsivos a um DSR, você e sua organização decidem quais dados devem fornecer ao titular dos dados. Você pode fornecer-lhes uma cópia do documento real, uma versão adequadamente editada ou uma captura de tela das partes que você considera adequadas de serem compartilhadas. Para cada uma dessas respostas à uma solicitação de acesso, você precisará recuperar uma cópia do documento ou outro item que contenha os dados responsivos.

Ao oferecer uma cópia ao titular dos dados, talvez você tenha que remover ou redigir informações pessoais sobre outros titulares de dados e quaisquer informações confidenciais.

A seguir explicamos como obter uma cópia dos dados em resposta a uma solicitação de acesso a DSR.

#### <a name="azure-active-directory"></a>Azure Active Directory

A Microsoft oferece um portal e experiências de produtos, proporcionando ao administrador de locatários do cliente corporativo a capacidade de gerenciar solicitações de acesso a DSR. As solicitações de acesso a DSR permitem acessar dados pessoais do usuário, incluindo: (a) informações de identificação sobre um usuário final e (b) logs gerados pelo sistema.

#### <a name="service-specific-interfaces"></a>Interfaces específicas de serviços

O Microsoft Intune fornece a capacidade de [descobrir os Dados dos Clientes](#step-1-discover) diretamente por meio de UIs (interfaces de usuário) ou APIs (interfaces de programação de aplicativo) pré-existentes.

### <a name="step-3-rectify"></a>Etapa 3: Retificação

Se um titular de dados solicitar que você retifique os dados pessoais que residem nos dados da sua organização, você e sua organização terão que determinar se é apropriado atender à solicitação. A retificação dos dados pode incluir ações como editar, redigir ou remover dados pessoais de um documento ou outro tipo ou item.

Como processador de dados, a Microsoft não oferece a capacidade de corrigir logs gerados pelo sistema, pois reflete atividades factuais e constitui um registro histórico de eventos nos serviços da Microsoft. Com relação ao Intune, os administradores não podem atualizar informações específicas do dispositivo ou aplicativo. Se um usuário final quiser corrigir quaisquer dados pessoais (como o nome do dispositivo), deverá fazê-lo diretamente no dispositivo. Essas alterações são sincronizadas na próxima vez que se conectarem ao Intune.

### <a name="step-4-restrict"></a>Etapa 4: Restrição

Os titulares de dados podem solicitar que você restrinja o processamento dos dados pessoais. Fornecemos o Portal do Azure e APIs (interfaces de programação de aplicativos) preexistentes ou IUs (interfaces de usuário). Essas experiências proporcionam ao administrador de locatários do cliente corporativo a capacidade de gerenciar tais DSRs por meio de uma combinação de exportação e exclusão de dados. Para obter detalhes, consulte [Processamento de dados pessoais](/intune/privacy-data-store-process#processing-personal-data).

### <a name="step-5-delete"></a>Etapa 5: Exclusão

O "direito de apagar" pela remoção de dados pessoais dos Dados do cliente de uma organização é uma proteção essencial no GDPR. A remoção de dados pessoais inclui a remoção de todos os dados pessoais e logs gerados pelo sistema, exceto as informações do log de auditoria. Para mais detalhes, consulte [Excluir dados pessoais do usuário final](/intune/privacy-data-audit-export-delete#delete-end-user-personal-data).

## <a name="part-2-system-generated-logs"></a>Parte 2: Logs gerados pelo sistema

Os logs de auditoria dão aos administradores de locatário um registro de atividades que geram uma alteração no Microsoft Intune. Os Logs de Auditoria disponíveis para várias atividades de gerenciamento e normalmente criam, atualizam (editam), excluem e atribuem ações. Também é possível revisar tarefas remotas que geram eventos de auditoria. Esses logs de auditoria podem conter dados pessoais de usuários cujos dispositivos estão registrados no Intune. Os administradores não podem excluir os logs de auditoria. Para saber mais, confira [Auditoria de dados pessoais](/intune/privacy-data-audit-export-delete#audit-personal-data).

## <a name="notify-about-exporting-or-deleting-issues"></a>Notificar problemas de exportação ou exclusão

Se você tiver problemas ao exportar ou excluir dados do Portal do Azure, acesse a folha **Ajuda e suporte** do portal do Azure e envie um novo tíquete na folha **Gerenciamento de Assinaturas > Outra Solicitação de Segurança e Conformidade > Privacidade e Solicitações de RGPD**.

## <a name="learn-more"></a>Saiba mais

- [Central de Confiabilidade da Microsoft](https://www.microsoft.com/trust-center/privacy/gdpr-overview)
