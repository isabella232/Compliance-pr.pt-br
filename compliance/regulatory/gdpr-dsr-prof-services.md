---
title: Solicitações de titulares dos dados ao suporte e aos Serviços profissionais da Microsoft sobre o RGPD e CCPA
description: Como o Suporte da Microsoft e os serviços profissionais cuidam das solicitações de entidades de dados para o RGPD e CCPA.
keywords: Serviços profissionais, Microsoft 365, Microsoft 365 Education, documentação do Microsoft 365, RGPD
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
ms.custom: seo-marvel-apr2020
hideEdit: true
ms.openlocfilehash: 06dbe8eeeddc32fb98b7b4bf0351834fb6a34944
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/12/2021
ms.locfileid: "59157925"
---
# <a name="microsoft-support-and-professional-services-data-subject-requests-for-the-gdpr-and-ccpa"></a>Solicitações de titulares dos dados ao suporte e aos Serviços profissionais da Microsoft sobre o RGPD e CCPA

## <a name="introduction-to-microsoft-professional-services"></a>Introdução aos serviços profissionais da Microsoft

Os Serviços Profissionais da Microsoft inclui um grupo diversificado de arquitetos técnicos, engenheiros, consultores e profissionais de suporte dedicados a cumprir a missão da Microsoft de permitir que os clientes façam mais e conquistem mais. Nossa equipe de serviços profissionais inclui mais de 21.000 consultores, assessores digitais, suporte de primeira linha, engenheiros e profissionais de vendas trabalhando em 191 países, oferecendo suporte a 46 idiomas diferentes, gerenciando vários milhões de compromissos por mês e participando de interações com clientes e parceiros por meio de instalações, telefone, web, comunidade e ferramentas automatizadas. A organização traz ampla experiência em todo o portfólio da Microsoft, usando uma extensa rede de parceiros, comunidades técnicas, ferramentas, diagnósticos e canais que nos conectam com nossos clientes empresariais.

Saiba mais sobre os Serviços Profissionais da Microsoft acessando a página da Web [Documentação de Segurança dos Serviços Profissionais da Microsoft](https://www.microsoft.com/professionalservices/overview). O Serviços Profissionais da Microsoft leva a sério suas obrigações sob o Regulamento Geral de Proteção de Dados (GDPR). As informações neste documento foram elaboradas para responder às perguntas dos clientes sobre como as ofertas de suporte e consultoria da Microsoft responderão e ajudarão os clientes a responder às obrigações de Solicitação do Titular dos Dados (DSR) sob a GDPR.

### <a name="introduction-to-dsrs"></a>Introdução às DSRs 

O RGPD fornece direitos às pessoas (conhecidas na regulamentação como *titulares de dados*) para gerenciar os dados pessoais que foram coletados por um funcionário ou outro tipo de órgão ou organização (conhecido como *controlador de dados* ou apenas *controlador*). Os dados pessoais são definidos genericamente no RGPD como quaisquer dados relacionados a uma pessoa identificada ou identificável. O RGPD fornece aos titulares dos dados direitos específicos a seus dados pessoais; esses direitos incluem a obtenção de cópias, a solicitação de alterações, a restrição do processamento e a exclusão deles. Uma solicitação formal realizada por um titular dos dados para que um controlador realize um determinado pedido com os dados pessoais do titular é chamada de *Solicitação do Titular dos Dados* ou DSR. Além disso, ela obriga as empresas que trabalham em nome de um controlador (conhecido como *processador de dados* ou apenas *processador*) a ajudar razoavelmente o controlador a atender às DSRs.

Da mesma forma, a Lei de Privacidade do Consumidor da Califórnia (CCPA), fornece direitos e obrigações de privacidade aos consumidores da Califórnia, incluindo direitos semelhantes aos Direitos do Titular dos Dados do RGDP, como o direito de excluir, acessar e receber (portabilidade) suas informações pessoais.  O CCPA também fornece certas divulgações, proteções contra discriminação ao eleger direitos de exercício e requisitos de "aceitação/recusa" para determinadas transferências de dados classificadas como "vendas". As vendas são amplamente definidas para incluir o compartilhamento de dados para uma consideração valiosa. Para obter mais informações sobre o CCPA, confira a [Lei de Privacidade do Consumidor da Califórnia](offering-ccpa.md) e as [Perguntas Frequentes Sobre a Lei de Privacidade do Consumidor da Califórnia](ccpa-faq.yml).

Este guia discute como localizar, acessar e atuar em dados pessoais que residem nos sistemas de TI da Microsoft que podem ter sido coletados para fornecer Suporte e outras ofertas dos Serviços Profissionais.

Ao desenvolver uma resposta para as DSRs, é importante para os clientes da Microsoft entenderem que os dados de consultoria e de suporte são separados dos dados de cliente nos Serviços Online ou de outros dados que eles ou seus titulares de dados possam ter fornecido à Microsoft. As ferramentas e os processos fornecidos para Serviços Online, para o Painel de Privacidade da Microsoft ou outros sistemas da Microsoft para resposta às DSRs da Microsoft não podem ser usados para responder às DSRs relativas aos dados pessoais mantidos pelo Suporte da Microsoft ou outros Serviços Profissionais.

Todas as solicitações precisam ser realizadas por meio de um representante do suporte, conforme descrito mais adiante nesse artigo. Atualmente não há nenhuma ferramenta de autoatendimento para os clientes acessarem dados pessoais nas organizações de Serviços Profissionais.

#### <a name="overview-of-the-processes-outlined-in-this-guide"></a>Visão geral dos processos descritos neste guia

- **Descobrir**: use as ferramentas de pesquisa e descoberta para encontrar com mais facilidade os dados de clientes que possam estar sujeitos a uma DSR. Assim que os documentos potencialmente responsivos forem coletados, você pode executar uma ou mais ações de DSR descritas nas etapas a seguir para responder à solicitação. Como alternativa, você pode determinar que a solicitação não atende às diretrizes da sua organização para responder às DSRs.
- **Acesso:** recupere dados pessoais que residem na nuvem da Microsoft e, se solicitado, faça uma cópia para disponibilizar para o titular dos dados.
- **Retificação:** faça alterações ou implemente outras ações solicitadas nos dados pessoais, onde for possível.
- **Restringir**: restrinja o processamento de dados pessoais, removendo licenças para vários serviços do Azure ou desligando os serviços desejados quando possível. Você também pode remover dados da nuvem da Microsoft e mantê-los no local ou em outro local.
- **Exclusão:** remova permanentemente os dados pessoais que residem na nuvem da Microsoft.
- **Exportar/Receber (Portabilidade):** forneça uma cópia eletrônica (em formato legível para computador) de dados pessoais ou informações pessoais para o titular dos dados. Os dados pessoais do CCPA são quaisquer informações relacionadas a uma pessoa, identificável ou não. Não há distinção entre as funções pública, privada ou de trabalho de uma pessoa. O termo definido "informações pessoais" se alinha aproximadamente aos "dados pessoais" do RGPD. No entanto, o CCPA também inclui dados da família e do domicílio. Para obter mais informações sobre o CCPA, confira a [Lei de Privacidade do Consumidor da Califórnia](offering-ccpa.md) e as [Perguntas Frequentes Sobre a Lei de Privacidade do Consumidor da Califórnia](ccpa-faq.yml).

### <a name="terminology"></a>Terminologia

Vejamos abaixo as definições relevantes dos termos do RGPD para este guia:

- **Controlador:** a pessoa física ou jurídica, autoridade pública, órgão ou outra entidade que, sozinha ou em conjunto com terceiros, determina os fins e os meios do processamento de dados pessoais, onde tais fins e meios são determinados por lei da União ou Estado-Membro, o controlador ou os critérios específicos para sua indicação podem ser fornecidos por lei da União ou Estado-Membro.
- **Dados pessoais e titular dos dados:** qualquer informação relativa a uma pessoa natural identificada ou identificável (“titular dos dados”); uma pessoa natural identificável é aquela que pode ser identificada, direta ou indiretamente, especialmente por referência a um identificador, como nome, um número de identificação, dados de localização, um identificador online ou um ou mais fatores específicos de natureza física, fisiológica, genética, mental, econômica, cultural ou social dessa pessoa natural.
- **Processador:** uma pessoa física ou jurídica, autoridade pública, agência ou outro órgão que processa dados pessoais em nome do controlador.

#### <a name="additional-terms-and-definitions-that-may-be-helpful-in-understanding-this-guide"></a>Outros termos e definições que podem ser úteis à compreensão deste guia

- **Dados de consultoria e de suporte:** são todos os dados, incluindo qualquer texto, som, vídeo, arquivos de imagem ou software que são fornecidos à Microsoft por ou em nome do Cliente (ou que o Cliente autoriza a Microsoft a obter de um serviço online) por meio de uma interação com a Microsoft para obter suporte ou Serviços profissionais. A título de esclarecimento, isso não inclui os dados coletados em que a Microsoft é o controlador de dados, como os dados do contato do cliente.
- **Contato do cliente:** são os dados pessoais que podem fazer parte da sua relação comercial com a Microsoft, como os dados pessoais contidos nas suas informações de contato do cliente. Entre esses dados podemos citar o seu nome, email ou número de telefone do Gerente de Serviço de Contrato Premier (CSM), o Administrador global ou de TI para um serviço online ou funções semelhantes.
- **Dados de pseudônimo:** Quando você usa o suporte da Microsoft para serviços e produtos corporativos da Microsoft, a Microsoft gera algumas informações vinculadas a um identificador numérico da Microsoft para fornecer o suporte. Normalmente eles são tíquetes de "Dados de pseudônimo". Embora esses dados não possam ser atribuídos a um titular de dados específico sem o uso de informações adicionais, alguns deles podem ser considerados pessoais sob a definição genérica do RGPD sobre dados pessoais. No escopo dos Serviços profissionais, as solicitações para atender ou auxiliar na conclusão de DSRs sempre incluirá automaticamente dados de pseudônimo de endereçamento.

### <a name="how-to-use-this-guide"></a>Como usar este guia

Este guia trata de quatro cenários que um cliente pode encontrar se tiver utilizado os Serviços profissionais da Microsoft.

- **DSR para um contato do cliente envolvendo a Microsoft:** explicação de como a Microsoft responderá às solicitações de um contato do cliente ou administrador de TI para exercer os seus direitos de entidades de dados.
- **DSR para um Usuário Final Envolvendo a Microsoft:** Explicação de como a Microsoft responderá às solicitações dos funcionários de um cliente ou de outras entidades de dados para exercer seus direitos.
- **DSR para Dados Fornecidos pelo Cliente: Suporte Comercial:** Explicação de como receber assistência da Microsoft quando um cliente tiver recebido uma solicitação de um funcionário ou de outras entidades de dados para exercer seus direitos, e que os dados pessoais da entidade de dados tenham sido coletados pelo Suporte da Microsoft durante uma interação do suporte.
- **DSR para Dados Fornecidos pelo Cliente: Serviços de Consultoria, incluindo Serviços de Migração FastTrack:** Explicação de como receber assistência da Microsoft quando um cliente tiver recebido uma solicitação de um funcionário ou de outras entidades de dados para exercer seus direitos, e que os dados pessoais do usuário tenham sido coletados pela Microsoft durante uma interação de consultoria.

## <a name="dsr-for-a-customer-contact-engaging-microsoft"></a>DSR para um contato do cliente à Microsoft

*Como a Microsoft responde às solicitações de um contato do cliente ou administrador de TI a fim de exercer os direitos do titular dos dados.*

Quando um cliente interage com a Microsoft para receber serviços de consultoria e de suporte, o Suporte da Microsoft coleta ou recupera automaticamente dos registros de conta os dados pessoais do Contato do Cliente (por exemplo, CSM Premier, Administrador de TI, Administrador Global). Isso provavelmente inclui o nome, o e-mail, o telefone e outros dados pessoais da pessoa que busca suporte ou serviços de consultoria.

Os dados pessoais do Contato do Cliente fazem parte da relação de negócios da Microsoft com o cliente, e a Microsoft é uma Controladora de Dados, exceto quando esses dados são coletados durante o fornecimento de suporte técnico. Uma resposta da Microsoft aos DSRs do Contato do Cliente sobre seus dados pessoais, independentemente de eles ainda estarem na organização.

Quando os Dados Pessoais do Contato do Cliente são coletados durante o fornecimento de suporte técnico, a Microsoft é o Processador de Dados.

Os clientes devem compreender que a DSR só abrange os dados pessoais do Contato do Cliente e nenhuma alteração ou exclusão será feita em qualquer um dos dados do cliente enviados como parte de interações (por exemplo, transcrições, descrições de caso, arquivos, produtos de trabalho), pois a Microsoft é o processador de dados. Além disso, para manter o registro histórico da interação, nenhum tipo de alteração será feito nas interações fechadas, inclusive o registro de quem abriu uma interação.

Ao ser consultado por um Contato do Cliente sobre uma DSR, a equipe da Microsoft encaminhará um contato do cliente para o [Centro de Resposta de Privacidade](https://go.microsoft.com/fwlink/?LinkId=321116). Este é o mecanismo de entrada principal da Microsoft para consultas e reclamações sobre privacidade. Ao receber uma consulta, o Centro de Resposta de Privacidade identificará que isso faz parte de uma conta comercial ou organizacional e responderá de acordo.

Onde a Microsoft é o Processador de Dados, confira <b>DSR para Dados Fornecidos pelo Cliente: Suporte Comercial</b> abaixo.

Para garantir a continuidade de negócios do cliente, a Microsoft também não processará uma DSR associada a uma interação até a confirmação de um contato substituto. Após a confirmação de um novo contato, a Microsoft trocará o contato antigo pelo novo em interações abertas.

Os clientes podem optar por fazer alterações em seus dados coletados durante as interações com os Serviços Profissionais pelo suporte normal ou por canais de consultoria, separado dessa DSR. Por exemplo, a Microsoft pode ajudá-lo a eliminar interações com o suporte, mediante solicitação (consulte na seção *Guia de DSR sobre os dados fornecidos pelo cliente*).

*Exemplo apenas para fins ilustrativos*

Davi é um administrador de TI de um cliente empresarial do O365, com uma Interação de consultoria aberta e duas interações fechadas. Agora, Davi está saindo da sua empresa e deseja excluir os seus dados. Davi entra em contato com o Centro de Respostas de Privacidade, que o identifica como o administrador de TI. Davi fica sabendo que seu nome não pode ser excluído das interações anteriores (fechadas) nem de qualquer dado nas interações abertas. No entanto, o Centro de Respostas de Privacidade substituirá Davi como contato no tíquete aberto atual caso ele indique um contato substituto. Davi avisa à Microsoft que Laura será o contato substituto e a Microsoft fará a alteração em todos os sistemas de suporte.

## <a name="dsr-for-an-end-user-engaging-microsoft"></a>DSR para um usuário final de envolvimento da Microsoft

*Como a Microsoft responde às solicitações dos funcionários do cliente ou de outros titulares dos dados para exercer os direitos deles.*

Se os funcionários do cliente ou outros titulares dos dados entrarem em contato com a Microsoft para fazerem solicitações sobre seus dados coletados pela Microsoft na qualidade de processador de dados, o titular dos dados será informado de que precisará contatar o cliente da Microsoft, como o controlador de dados, para exercer esses direitos. Isso é tudo o que a Microsoft fará.

Se o titular dos dados também tiver contatado a Microsoft para exercer seus direitos sobre os dados que a Microsoft coletou em situações em que ela é a controladora de dados (por exemplo, suporte ao consumidor, contato do cliente comercial), a Microsoft responderá separadamente à solicitação de exercício de direito do titular dos dados do indivíduo relativa àqueles dados pessoais.

*Exemplo apenas para fins ilustrativos*

Laura é uma funcionária de um cliente empresarial, a Contoso, que lhe concedeu uma conta do Dynamics 365. Ela entra em contato com a Microsoft para excluir todos os seus dados e é encaminhada para a Central de Resposta a Assuntos de Privacidade. Laura preenche o formulário de solicitação. A Central de Resposta a Assuntos de Privacidade a identifica como uma usuária final corporativa e informa que ela precisa excluir os seus dados corporativos através da Contoso. A Central também a identifica como usuária do Microsoft X-Box e exclui seus dados da conta de consumidor da Microsoft.

## <a name="dsr-for-customer-provided-data-commercial-support"></a>DSR para dados fornecidos pelo cliente: suporte comercial

*Como obter assistência da Microsoft quando um cliente recebe uma solicitação de seus funcionários ou de outras entidades de dados pedindo o exercício de direitos, e esses dados pessoais do titular dos dados tenham sido coletados pelo Suporte da Microsoft durante a interação com o suporte.*

Quando um cliente interage com o Suporte da Microsoft, a Microsoft coleta os Dados de Suporte do cliente para resolver os problemas que precisaram de interação com o suporte. Esses Dados de Suporte incluem a interação da Microsoft com o cliente (por exemplo, chat, telefone, e-mail, envio pela Web) e quaisquer arquivos de conteúdo que o cliente envia à Microsoft ou que a Microsoft tem, com permissão do cliente, extraídos do ambiente de TI ou do locatário de Serviços Online do cliente para resolver o problema de suporte. No caso de Suporte Premier, isso também incluirá todos os dados que coletamos de você para evitar proativamente problemas futuros. No entanto, isso exclui informações de Contato do Cliente ou outras informações das relações comerciais da Microsoft com o cliente (por exemplo, registros de cobranças).

Para todos os Dados de Suporte, a Microsoft é a processadora de dados. Dessa forma, a Microsoft não responderá às solicitações diretas dos titulares dos dados sobre os Dados de Suporte fornecidos quando foram associados a um cliente comercial da Microsoft. A Microsoft trabalhará com o cliente por meio dos canais de suporte normais para ajudá-lo a responder às DSRs.

## <a name="step-1-discover"></a>Etapa 1: Descoberta

A primeira etapa para se obter assistência da Microsoft na resposta a uma DSR é localizar os dados pessoais concernentes à DSR. Esta primeira etapa, localizar e analisar os dados pessoais em questão, ajudará um cliente a determinar se uma DSR atende às políticas da organização tocantes à execução de uma solicitação do titular dos dados.

Depois que o cliente encontrar os dados, o cliente, em seguida, poderá executar a ação específica para atender à solicitação do titular dos dados. A determinação do nível de descoberta com que o cliente precisa se envolver dependerá do que o cliente está tentando fazer.

Quando a Microsoft auxilia um cliente com a solução de uma DSR, isso é uma função empresarial, e a solicitação é feita pelo canal de suporte normal, não por meio de uma solicitação ao Centro de Respostas de Privacidade.

Ao descobrir os dados relevantes e obter assistência da Microsoft, um cliente tem várias opções de como abordar a DSR:

*Opção A: DSR do cliente de suporte cruzado da Microsoft*. Aplique o DSR a todos os dados de suporte do cliente em todo o ambiente de Suporte da Microsoft. Para fazer isso, o cliente pode simplesmente pedir à Microsoft que aplique o DSR a todos os Dados de Suporte coletados.

*Opção B: interações de cliente específicas.* Use sistemas online para analisar tíquetes e depois identificar interações específicas que contenham os dados pessoais relevantes e relatá-los à Microsoft. A Microsoft tentará dar assistência à realização de uma pesquisa se o cliente não puder pesquisar nas interações (tíquetes).

*Assim que os contratos forem identificados, solicite a aplicação da DSR a uma parte específica do registro ou a tudo relacionado a essa interação na Microsoft.*

Para identificar interações específicas, os clientes precisam pesquisar as suas interações. Para os clientes Premier, o Gerente de Serviço de Contrato Premier (CSM) de um cliente tem a visibilidade de todas as Solicitações de Suporte (SRs) criadas sob essa Agenda do Contrato. Para os clientes não Premier, estão disponíveis portais de interação com o suporte equivalentes, como por meio das áreas de suporte dos Serviços Online.

O CSM pode ir ao portal no [Hub de Serviços](https://serviceshub.microsoft.com/support/contactsupport) e selecionar gerenciar todas as Solicitações de Suporte.

>[!IMPORTANT]
>Além do histórico de casos no SMC, os clientes também podem ter dados pessoais de um usuário final em arquivos, dados que foram coletados pela Microsoft (ou, com permissão do cliente, removidos do Serviço Online) durante a interação com o suporte. Como exemplo, podemos citar cópias das caixas de correio do Exchange, VMs do Azure ou bancos de dados do cliente. Esses dados pessoais podem ou não ser mencionados no histórico de casos (ou seja, tíquete) para uma interação específica. Para conferir esses dados, o Contato do Cliente deve ser um contato específico e autenticado da Solicitação de Suporte (via AAD ou MSA) que recebeu uma URL para um espaço de trabalho na ferramenta de Gerenciamento e Transferência de Dados do Suporte da Microsoft (DTM). Um Contato do Cliente terá acesso aos arquivos, mas nenhuma exibição global estará disponível, e o SMC não indicará se os arquivos existem.

Depois que os clientes identificarem todos os dados relevantes nos tíquetes de suporte selecionados, os clientes poderão decidir se devem solicitar a exclusão de tudo o que estiver relacionado a um tíquete ou aplicar seletivamente a DSR a instâncias individuais dos dados pessoais.

## <a name="step-2-access"></a>Etapa 2: Acesso

Depois que um cliente encontrar Dados de Suporte que contenham dados pessoais potencialmente responsivos a uma DSR, cabe ao cliente decidir quais dados pessoais serão incluídos na resposta. Por exemplo, o cliente pode optar por remover dados pessoais sobre titulares dos dados e quaisquer informações confidenciais.

A resposta à DSR pode incluir uma cópia do documento real, uma versão adequadamente redigida ou uma captura de tela das partes que o cliente considerou adequadas ao compartilhamento. Para todas essas respostas a uma solicitação de acesso, o cliente precisará recuperar uma cópia do documento ou outro item que contenha dados responsivos.

O acesso aos dados pessoais de um usuário final pode ser realizado de uma menção ou anotação em vários tipos de documentação de conteúdo. Como os clientes podem acessar o tíquete de interação e o conteúdo, eles mesmos podem fornecer um resumo dos dados pessoais sem ajuda adicional da Microsoft.

Em casos raros, o cliente pode precisar de cópias dos dados de interação com o suporte (por exemplo, e-mails, cópias transcritas das gravações de telefone, transcrições de chat) entre um representante da Microsoft e o representante do cliente. Dentro do limite necessário, a Microsoft pode fornecer cópias redigidas dessas transcrições com base na necessidade, confidencialidade e dificuldade.

## <a name="step-3-rectify"></a>Etapa 3: Retificação

Se um titular dos dados pedir para o cliente retificar os dados pessoais residentes nos Dados de Suporte da organização, o cliente precisará determinar se é apropriado executar a solicitação. Se o cliente decidir atender à solicitação, poderá solicitar que a Microsoft faça a alteração. A Microsoft pode retificar ou excluir os dados do cliente dos sistemas de suporte e solicitar que o cliente os reenvie à Microsoft no formato corrigido.

## <a name="step-4-restrict"></a>Etapa 4: Restrição

A qualquer momento, o cliente pode fechar uma interação ou contatar a Microsoft e solicitar o fechamento da interação. Uma interação fechada impedirá a execução de qualquer trabalho.

Para garantia adicional, o cliente pode contatar a Microsoft e solicitar a colocação de uma observação no sistema de tíquetes de interação dizendo que o caso não deve ser reaberto por nenhum motivo sem a permissão do cliente.

Observação: as interações (tíquetes) também serão excluídas de acordo com um cronograma de retenção e de exclusão, com base na confidencialidade dos dados, no serviço e no sistema. Se os clientes exigirem uma cópia dos dados, não poderão se esquecer de extrair os dados antes da exclusão.

## <a name="step-5-delete"></a>Etapa 5: Exclusão

O "direito de apagar" por meio da remoção dos dados pessoais dos Dados de Suporte de uma organização é uma importante proteção do RGPD. A remoção de dados pessoais compreende a exclusão de documentos, arquivos ou interações inteiros, ou a exclusão de dados específicos em um documento, interação ou arquivo.

Conforme um cliente investiga ou se prepara para excluir dados pessoais em resposta a uma DSR, existem alguns pontos importantes a serem entendidos sobre como a exclusão funciona para o Suporte da Microsoft.

Todos os dados da Microsoft têm uma política de retenção e exclusão aplicada a eles, que variam de acordo com o risco e outros fatores.

Os clientes que solicitarem a exclusão universal dos dados pessoais de um titular dos dados em todos os sistemas de suporte pode fazê-lo por meio do TAM ou apresentando uma Solicitação de Suporte (SS) no CMS ou sistema equivalente. Você *deve* indicar que essa é uma solicitação para ajudá-lo com a DSR em RGPD.

*Opção A: DSR de cliente de suporte em toda a Microsoft*. Para uma DSR de sistema cruzado, o cliente deve fornecer os dados pessoais que a Microsoft precisa para identificar os dados necessários (por exemplo, endereço de email ou número de telefone). A Microsoft não correlacionará nem pesquisará registros e só pesquisará diretamente nos identificadores fornecidos pelo cliente. Quando os dados forem encontrados, a Microsoft excluirá todas as interações e todos os dados associados. Observação importante: isso pode resultar na perda de registros históricos que são importantes para a organização do cliente.

> Observação Importante: isso pode resultar na perda de registros históricos importantes para a organização do cliente.

*Opção B: interações de cliente específicas*. Para interações específicas que o cliente identificou e quer excluir, não exclua tíquetes do SMC. Isso resultará em dados pessoais remanescentes em logs e sistemas downstream, que talvez não possam ser excluídos no prazo necessário. Em vez disso, identifique o tíquete ou os dados pessoais no tíquete que deve ser excluído e contate o Suporte da Microsoft para ajudá-lo a excluir os dados.

### <a name="microsoft-support-data-transfer-and-management-tool-dtm-instructions"></a>Instruções sobre a ferramenta de Gerenciamento e Transferência de Dados do Suporte da Microsoft (DTM)

Para todas essas pesquisas, a Microsoft não procurará na DTM devido à possível confidencialidade de conteúdo dos arquivos. No entanto, se o cliente quiser, a Microsoft excluirá todos os arquivos contidos na DTM associada à conta do cliente. Devido à possibilidade de implicações graves aos clientes, a Microsoft requer uma solicitação separada do cliente especificando a exclusão dos arquivos da DTM.

- Para casos abertos, o Contato do Cliente pode acessar a DTM e excluir os arquivos.
- Para os casos fechados há menos de 90 dias, deve ser feita uma solicitação de remoção de arquivos a um TAM ou em uma SR.
- Nos casos fechados depois de 90 dias, os arquivos já foram automaticamente excluídos.
- Ainda que os dados pessoais só estivessem localizados em um arquivo que foi excluído, os clientes ainda precisam pedir para a Microsoft executar uma busca por dados pessoais nos sistemas, pois alguns dados podem ter sido removidos da DTM no decorrer do suporte.

## <a name="step-6-export"></a>Etapa 6: Exportação

O "direito de portabilidade de dados" permite que um titular dos dados solicite uma cópia dos dados pessoais em um formato eletrônico e solicite que a sua organização os transmita para outro controlador. No caso dos Dados de Suporte, quaisquer informações úteis que a Microsoft tem estariam na forma de informações de interação ou arquivos que podem ser retornados para você para a retransmissão ou carregamento para outro controlador.

Observação: Os dados exportados podem não incluir a propriedade intelectual da Microsoft ou quaisquer dados que possam comprometer a segurança ou a estabilidade do serviço.

*Exemplo apenas para fins ilustrativos*

Davi é um CSM Premier para um cliente empresarial, a Contoso, que usa o Office 365 para os e-mails dos funcionários e o Azure para hospedar um banco de dados SQL da Contoso. A Contoso tem vários tíquetes abertos e fechados. Recentemente, o Suporte da Microsoft, com permissão da Contoso, moveu uma cópia do banco de dados SQL para a DTM para fins de suporte e solução de problemas.

Davi recebe uma DSR de Laura solicitando a exclusão dos dados dela. Davi acessa o CMS e pesquisa as interações para identificar que Laura tinha problemas de conta de e-mail, o que estava documentado em dois tíquetes por nome e endereço de e-mail. Ele entra em contato com seu TAM, fornece ao TAM o nome e o endereço de e-mail da Laura como um identificador e solicita que os dois tíquetes sejam excluídos, juntamente com todos os dados de downstream gerados a partir desses tíquetes.

Ele também suspeita que estava envolvido em uma conversa de chat com a equipe de suporte na qual menciona Laura, então solicita que o log do bate-papo seja excluído.

Ele também sabe que os dados pessoais de Laura estão no banco de dados SQL. Como a VM do SQL foi movida para a DTM há menos de 90 dias, ele pede separadamente a seu TAM que ajude na exclusão imediata do banco de dados da DTM.

Por fim, como ele sabe que os dados podem ter sido removidos do arquivo da DTM durante o suporte, ele pede que a Microsoft procure pelos dados pessoais de Laura nos sistemas de TI a partir do banco de dados SQL.

O Suporte da Microsoft executa todas essas exclusões e, com base na solicitação do cliente, o TAM lhe fornece uma instrução de atestado de que os dados necessários foram excluídos.

## <a name="dsr-guide-for-customer-provided-data-in-consulting-services-including-migration-services"></a>O Guia DSR para dados fornecidos pelo cliente em serviços de consultoria incluem os Serviços de migração

*Como obter assistência da Microsoft quando um cliente recebe uma solicitação de seus funcionários ou de outros titulares dos dados, pedindo o exercício de direitos, e os dados pessoais do titular dos dados foram coletados pela Microsoft durante a interação com a consultoria.*

## <a name="microsoft-consulting-services"></a>Serviços de consultoria da Microsoft

Para as interações com os serviços de consultoria da Microsoft contratadas em que se aplica o adendo de proteção de dados de Serviços profissionais da Microsoft (<https://aka.ms/professionalservicesdpa>).

A Microsoft é o controlador de dados dos Contatos do Cliente que trabalham com a equipe de interação. Esses indivíduos devem contatar o [Centro de Respostas de Privacidade](https://go.microsoft.com/fwlink/?LinkId=321116) para atender aos direitos do titular dos dados.

A Microsoft é o processador de dados para uma DSR localizada nos dados fornecidos durante a interação de consultoria. O cliente deve entrar em contato com o gerente de interação para criar um plano para ajudá-lo a responder à DSR com base nos dados coletados e, depois, no tipo específico dos serviços de consultoria fornecidos. Na extensão em que a sua solicitação constitui um nível de esforço geralmente visto dentro de uma interação dos Serviços de Consultoria da Microsoft, pode haver a necessidade de um pedido de trabalho adicional. Além disso, os dados pessoais serão excluídos após cada interação de consultoria em um período de tempo dependente do tipo de interação de consultoria. O cliente pode solicitar a exclusão de dados mais cedo e solicitar um atestado de exclusão.

## <a name="microsoft-fasttrack-services"></a>Serviços do Microsoft FastTrack

O [Microsoft FastTrack](https://na01.safelinks.protection.outlook.com/?url=https%3A%2F%2Ffasttrack.microsoft.com%2Fabout&data=02%7C01%7C%7Cd0521d8739c841df674508d596834585%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C636580412901207944&sdata=PO5eh56pm9IYk5Y%2Ff%2F31e%2BRVPmrC2Qi%2FCsw1NphR8gY%3D&reserved=0) fornece serviços de consultoria de TI às organizações para ajudá-las a integrar e usar os serviços em nuvem da Microsoft como o Microsoft 365, o Azure e o Dynamics 365.

A Microsoft é a controladora de dados para os Contatos do Cliente que trabalham com a equipe do FastTrack. Se os Contatos do Cliente quiserem acessar, analisar ou remover informações de contato dos registros do Microsoft FastTrack, os clientes poderão pedir que o titular dos dados envie a solicitação diretamente à caixa de entrada de Solicitação do RGPD do FastTrack do Office 365, \<<o365ftgdpr@microsoft.com>\>.

Para os serviços de migração do FastTrack, a Microsoft é a processadora de dados. De acordo com nossa política do Fast Track de divulgação de privacidade adicional, todos os dados na migração são considerados “dados de migração”. Se precisar executar DSRs enquanto sua organização estiver envolvida em um projeto de migração do FastTrack, será necessário tomar cuidados especiais.
  
Se houver necessidade de processar acesso, retificar ou exportar solicitações de DSR enquanto os dados dos usuários estiverem sendo processados por meio dos sistemas de migração do FastTrack, será responsabilidade do cliente preencher tais DSRs por meio de seus sistemas de origem existentes, nos quais os dados do usuário estão armazenados. Após a conclusão da migração do usuário e da migração dos dados para o serviço de nuvem de destino da Microsoft, será aplicada a diretriz fornecida pela Microsoft sobre como os clientes podem usar produtos, serviços e ferramentas administrativas da Microsoft para localizar e executar ações nos dados pessoais para responder à solicitação do titular dos dados. Para exibir esta diretriz, confira o artigo [Solicitações do Titular dos Dados para o RGPD](/microsoft-365/compliance/gdpr-data-subject-requests). 

Se você precisar excluir uma conta de usuário em réplica a uma solicitação de exclusão de DSR enquanto sua organização está envolvida em um projeto de migração FastTrack em andamento, você deve estar ciente de que os sistemas de migração podem reter uma cópia dos dados de migração de usuário por um período de tempo após a conclusão de a migração do usuário e a exclusão da conta do usuário não excluirão automaticamente esses dados de migração do usuário armazenados nos sistemas de migração FastTrack. Se desejar que a equipe do Microsoft FastTrack exclua os dados de migração do usuário, você pode [enviar uma solicitação](https://go.microsoft.com/fwlink/?linkid=874544). No curso normal dos negócios, o Microsoft FastTrack excluirá todas as cópias de dados assim que a migração da sua organização for concluída.

## <a name="other-consulting-services"></a>Outros serviços de consultoria

O cliente que recebe outros Serviços Profissionais através da Microsoft deve trabalhar com a equipe de interação para atender a todos os requisitos do RGPD. Se a equipe de interação não puder fornecer instruções claras sobre o cumprimento do GDPR DSR, os clientes poderão pedir ajuda ao [Centro de Respostas de Privacidade](https://go.microsoft.com/fwlink/?LinkId=321116).
