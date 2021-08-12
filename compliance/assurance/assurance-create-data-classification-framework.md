---
title: Criar uma estrutura de classificação de dados bem projetada
description: Neste artigo, você pode encontrar uma visão geral de como criar uma estrutura de classificação de dados bem projetada para Microsoft 365.
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
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 88a07e5c6d5e3e84260c5099d957ebf38745819e239f951df62a5d04886f3fa4
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/05/2021
ms.locfileid: "54288719"
---
# <a name="create-a-well-designed-data-classification-framework"></a>Criar uma estrutura de classificação de dados bem projetada

À medida que você desenvolve, renova ou refina sua estrutura de classificação de dados, considere as seguintes práticas principais:

- Não espere ir de 0 a **100** no dia 1 : a Microsoft recomenda uma abordagem de rastreamento a pé, priorizando recursos críticos para a organização e mapeando-os em uma linha do tempo. Conclua a primeira etapa, verifique se foi bem-sucedido e, em seguida, vá para a próxima fase aplicando lições aprendidas. Lembre-se de que sua organização ainda pode ser exposta ao risco enquanto você projeta sua estrutura de classificação de dados, portanto, não há problema em começar pequeno com apenas alguns níveis de classificação e expandir mais tarde, conforme necessário.
- **Você não está apenas** escrevendo para profissionais de segurança cibernética: as estruturas de classificação de dados são destinadas a um público amplo, incluindo seu membro médio da equipe, suas equipes de conformidade e legal e legal e sua equipe de TI. É importante escrever definições claras e fáceis de entender para seus níveis de classificação de dados, fornecendo exemplos do mundo real sempre que possível. Tente evitar jargões e considere um glossário para acrônimos e termos altamente técnicos. Por exemplo, use 'Informações de identificação pessoal' e forneça uma definição em vez de simplesmente dizer 'PII'.
- **Estruturas de classificação de dados devem ser** implementadas: para que as estruturas de classificação de dados sejam bem-sucedidas, elas devem ser implementadas. É especialmente relevante ao criar os requisitos de controle para cada nível de classificação de dados. Certifique-se de que os requisitos sejam claramente definidos e que eles prevejam e abordam qualquer ambiguidade que possa surgir durante a implementação. Por exemplo, se você tiver um controle sobre Informações de Identificação Pessoal, certifique-se de soletrar exatamente o que esse controle significa, como a Previdência Social ou o número do passaporte.
- **Somente vá granular se você precisar**: Estruturas de classificação de dados geralmente contêm em qualquer lugar de 3 a 5 níveis de classificação de dados. Mas só porque você *pode incluir* cinco níveis não significa que *você deve*. Considere os seguintes critérios ao decidir o número de níveis de classificação necessários:

    - Sua indústria e suas obrigações regulatórias associadas (setores altamente regulamentados tendem a precisar de mais níveis de classificação)
    - A sobrecarga operacional necessária para manter uma estrutura mais complexa
    - Seus usuários e sua capacidade de estar em conformidade com a complexidade e a nuance crescentes associadas a mais níveis de classificação
    - Experiência do usuário e acessibilidade ao tentar aplicar a classificação manual em vários tipos de dispositivos

- **Obter as pessoas certas envolvidas**: ter um stakeholder sênior é fundamental para o sucesso, pois muitos projetos se esforçam para iniciar ou levar mais tempo sem o gerenciamento sênior. As estruturas de classificação de dados geralmente pertencem a equipes de tecnologia da informação, mas podem ter implicações legais, de conformidade, de privacidade e de gerenciamento de alterações. Para garantir que você está criando uma estrutura que ajude a proteger sua empresa, inclua a privacidade e as partes interessadas legais, como seu Diretor de Privacidade e o Office do Conselho Geral no desenvolvimento de sua política. Se sua organização tiver uma divisão de Conformidade, profissionais de governança de informações ou uma equipe de gerenciamento de registros, eles também poderão ter entradas valiosas. À medida que sua estrutura é rolada para a empresa, seu departamento de Comunicações também tem uma função fundamental a ser desempenhada para a adoção e mensagens internas.
- **Balancear a segurança em relação** à conveniência : um erro comum é redigir uma estrutura de classificação de dados segura, mas muito restritiva. Essa estrutura pode ter sido projetada com segurança em mente, mas geralmente é difícil de implementar na prática. Se os usuários precisam seguir procedimentos complexos, rígidos e demorados para aplicar a estrutura em suas vidas diárias, sempre há o risco de que eles possam não acreditar mais em seu valor e eventualmente interromperão os procedimentos a seguir. Esse risco existe em todos os níveis da organização, incluindo gerentes de nível executivo (C-suite) dentro da organização. Um bom equilíbrio de segurança em relação à conveniência juntamente com ferramentas fáceis de usar geralmente levam à adoção e ao uso mais amplos do usuário. Se houver lacunas em sua estrutura, não espere até que tudo seja perfeito para iniciar a implementação. Em vez disso, avalie o risco ou a lacuna, crie um plano para atenuar e continue avançando. Lembre-se de que a proteção de informações é uma jornada, não é algo que é ativado durante a noite e, em seguida, feito. Planeje, implemente alguns recursos, confirme o sucesso e itere para a próxima etapa à medida que as ferramentas evoluem e os usuários obtenham maturidade e experiência.

Lembre-se também de que uma estrutura de classificação de dados só aborda *o que* sua organização deve fazer para proteger dados confidenciais. As estruturas de classificação de dados geralmente são acompanhadas por regras ou diretrizes de tratamento de dados que *definem* como colocar essas políticas em vigor de uma perspectiva técnica e de tecnologia. Nas seções a seguir, vamos usar algumas diretrizes práticas sobre como levar sua estrutura de classificação de dados de um documento de política para uma iniciativa totalmente implementada e a ação.

## <a name="pain-points-in-creating-a-data-classification-framework"></a>Pontos de dor na criação de uma estrutura de classificação de dados

Os esforços de classificação de dados são por natureza abrangentes, tocando quase todas as funções comerciais em uma empresa. Devido a esse amplo escopo e à complexidade de gerenciar conteúdo em ambientes digitais modernos, as empresas geralmente enfrentam desafios em saber por onde começar, como gerenciar uma implementação bem-sucedida e como medir seu progresso. Os pontos de dor comuns geralmente incluem:

- Projetando uma estrutura de classificação de dados robusta e fácil de entender, incluindo a determinação de níveis de classificação e controles de segurança associados.
- Desenvolver um plano de implementação que inclua confirmar a solução de tecnologia apropriada, alinhar o plano aos processos comerciais existentes e identificar o impacto para a força de trabalho.
- Configurar uma estrutura de classificação de dados dentro da solução de tecnologia escolhida e resolver quaisquer lacunas entre os recursos de tecnologia da ferramenta e a própria estrutura.
- Estabelecendo uma estrutura de governança que supervisiona a manutenção e a saúde dos esforços de classificação de dados.
- Identificar KPIs (indicadores de desempenho de chave) específicos para monitorar e medir o progresso.
- Aumentar a conscientização e a compreensão das políticas de classificação de dados, por que elas são importantes e como cumpri-las.
- Em conformidade com as análises de auditoria internas que visam a perda de dados e controles de segurança cibernética.
- Treinar e envolver usuários para que eles se tornem atentos à necessidade de classificação correta em seu trabalho diário e apliquem as medidas de classificação corretas.

## <a name="change-management-and-training"></a>Alterar o gerenciamento e o treinamento

Atualmente, as organizações usam ferramentas como Microsoft 365 para implementar sua estrutura de classificação de dados. O objetivo é tentar automatizar a classificação de dados e não aumentar a carga em sua força de trabalho. Essa estrutura não significa que sua organização não tem a responsabilidade de aumentar a conscientização sobre a necessidade de gerenciar o conteúdo e proteger a organização dos riscos discutidos neste artigo. A prática principal continua sendo conduzir o treinamento de conscientização em toda a organização como parte do cronograma de treinamento anual. Nossa experiência mostra que colocar um esforço robusto e abrangente no treinamento de seus usuários, que são o público-chave que executa esse trabalho, aumenta sua "compra" para o esforço e pode aumentar a adoção e a qualidade. Adicionar [recomendações de rótulo e](/microsoft-365/compliance/apply-sensitivity-label-automatically#recommend-that-the-user-apply-a-sensitivity-label) dicas no aplicativo pode ampliar esses esforços. Esse treinamento não precisa ser um curso autônomo extensivo. Sua organização pode incorporá-lo a outros treinamentos regulares, como seu treinamento anual de segurança de informações e incluir uma visão geral dos níveis e definições de classificação de dados. O principal ponto é que sua força de trabalho tem a compreensão de que, embora a ferramenta esteja automatizando a classificação de dados, isso não elimina a responsabilidade geral de cada usuário para proteger os dados de acordo com a política da empresa.

Além disso, você deve considerar um treinamento mais aprofundado para equipes de TI e segurança da informação para reforçar a prontidão operacional. As equipes que gerenciam a ferramenta e a estrutura de classificação de dados devem estar na mesma página. Essa coordenação pode exigir que você invista em um cronograma de treinamento mais robusto que pode ser mais frequente do que anualmente. O investimento em treinamento mais frequente representa outro caminho para reduzir o risco para sua organização. Essa equipe é responsável pela implementação e, portanto, pode ser um ponto de falha se não for treinado na ferramenta e na política.

Se você precisar marcar manualmente o conteúdo na ferramenta, desenvolver um grupo de super-usuários que receberam treinamento mais avançado é apropriado. Esses super usuários seriam contratados para situações em que os usuários são obrigados a marcar manualmente documentos com rótulos de sensibilidade de dados e teriam uma compreensão profunda da estrutura de classificação de dados e dos requisitos regulatórios da sua organização.

Por fim, sua liderança deve priorizar a defensoria dos comportamentos de segurança da informação para reforçar para a força de trabalho a importância das iniciativas de gerenciamento de riscos. Eles incluem o desenvolvimento e a implementação de uma estrutura robusta de classificação de dados e a atribuição de líderes-chave para promover a iniciativa, às vezes chamados de embaixadores ou campeões da mudança.

## <a name="governance-and-maintenance"></a>Governança e manutenção

Depois de desenvolver e implementar sua estrutura de classificação de dados, a governança e a manutenção contínuas serão essenciais para o sucesso. Além de acompanhar como os rótulos de sensibilidade são usados na prática, você precisará atualizar seus requisitos de controle com base nas alterações nos regulamentos, nas práticas líderes de segurança cibernética e na natureza do conteúdo que você gerencia. Os esforços de governança e manutenção podem incluir:

- Estabelecer um corpo de governança dedicado à classificação de dados ou adicionar uma responsabilidade de classificação de dados à carta de um corpo de segurança de informações existente.
- Definindo funções e responsabilidades para os usuários que supervisionam a classificação de dados.
- Estabelecendo KPIs para monitorar e medir o progresso.
- Acompanhamento de práticas de segurança cibernética e alterações regulatórias.
- Desenvolvendo procedimentos operacionais padrão que suportam e impõem uma estrutura de classificação de dados.

## <a name="industry-considerations"></a>Considerações do setor

Embora os princípios básicos para o desenvolvimento de uma estrutura forte de classificação de dados sejam universais, os detalhes da sua estrutura dependerão da natureza do seu setor e dos fatores exclusivos de conformidade e segurança de suas demandas de dados.

Por exemplo, as empresas de serviços financeiros podem precisar considerar a conformidade com várias estruturas regulatórias, dependendo do escopo de seus negócios e das regiões em que operam. As empresas de valores mobiliários nos Estados Unidos devem estar em conformidade com os regulamentos de conta, como a Regra [DA SEC 17a-4(f)](/compliance/regulatory/offering-sec-17a-4) ou a [Regra FINRA 4511](/microsoft-365/compliance/offering-finra-4511) que atende aos requisitos em torno da segurança e retenção de livros e registros. Da mesma forma, as empresas que operam no Reino Unido precisam considerar a [conformidade do FCA.](/microsoft-365/compliance/offering-fca-uk)

As agências governamentais enfrentam vários regulamentos que regem seus dados, que variam com base no território e na natureza de seu trabalho. Nos Estados Unidos, por exemplo, as agências governamentais e seus agentes que acessam informações fiscais federais (FTI) estão sujeitos ao [IRS 1075](/microsoft-365/compliance/offering-irs-1075), que visa minimizar o risco de perda, violação ou uso indevido de informações fiscais federais.

Embora as empresas de serviços financeiros e agências governamentais estão entre as organizações mais regulamentadas do mundo, a maioria das empresas tem considerações específicas do setor que precisam ser consideradas. Veja a seguir alguns exemplos:

- Organizações do setor [de saúde que garantem a conformidade com a HIPAA](/microsoft-365/compliance/offering-hipaa-hitech).
- Instituições de ensino, de escolas K-12 a universidades, gerenciando a [conformidade ferpa.](/microsoft-365/compliance/offering-ferpa)
- Fabricantes de drogas que trabalham para cumprir as diretrizes [da GxP](/microsoft-365/compliance/offering-gxp) em seu país ou região em torno da segurança da informação.
- Mídia, varejo e muitas outras empresas que lidam com a conformidade [do RGPD.](/microsoft-365/compliance/gdpr)
- Entrega e armazenamento de conteúdo de entretenimento, software e informações que lidam com [CDSA.](/microsoft-365/compliance/offering-cdsa)
- Segurança de informações do setor de energia em conformidade com o [padrão CIP do NERC.](/microsoft-365/compliance/offering-nerc-cip)

## <a name="implementing-your-data-classification-framework-in-microsoft-365"></a>Implementando sua estrutura de classificação de dados Microsoft 365

Depois de desenvolver sua estrutura de classificação de dados, a próxima etapa será a implementação. A [Centro de conformidade do Microsoft 365](https://compliance.microsoft.com/) permite que os administradores descubram, classifiquem, revisem e monitorem seus dados de acordo com a estrutura de classificação de dados. Os rótulos de sensibilidade podem ser usados para ajudar a proteger seus dados, aplicando várias proteções, como criptografia e marcação de conteúdo. Eles podem ser aplicados aos dados manualmente; por padrão, com base nas configurações de política; ou automaticamente, como resultado de uma condição como PII identificado.

Para organizações menores ou organizações com uma estrutura de classificação de dados relativamente simplificada, a criação de um único rótulo de sensibilidade para cada um dos seus níveis de classificação de dados pode ser suficiente. O exemplo a seguir mostra um nível de classificação de dados um para um para o mapeamento de rótulos de sensibilidade:

|**Rótulo de classificação**|**Rótulo de confidencialidade**|**Configurações de rótulos**|**Publicado para**|
|:-----------------------|:--------------------|:-----------------|:---------------|
| Irrestrita | Irrestrita | Aplicar o rodapé 'Irrestrito' | Todos os usuários |
| Geral | Geral | Aplicar rodapé 'Geral' | Todos os usuários |

>[!TIP]
>Durante um piloto de proteção de informações internas da Microsoft, houve dificuldades no entendimento e no uso do rótulo "Pessoal". Os usuários estavam confusos sobre se isso significava PII ou apenas relacionado a uma questão pessoal. O rótulo foi alterado para "não comercial" para ser mais claro. Este exemplo mostra que a taxonomia não precisa ser perfeita desde o início. Comece com o que você acha correto, pilote-o e ajuste o rótulo com base nos comentários, se necessário

Para organizações maiores com um alcance global ou necessidades de segurança de informações mais complexas, você pode achar que essa relação um para um entre o número de níveis de classificação em sua política e o número de rótulos de sensibilidade em seu ambiente Microsoft 365 é um desafio. Esse desafio é especialmente verdadeiro em organizações globais em que um determinado nível de classificação de dados, como "Restrito", pode ter uma definição diferente ou um conjunto diferente de controles, dependendo da região.

Para obter mais informações sobre a implementação, consulte [Understand data classification and](/microsoft-365/compliance/data-classification-overview) Learn about [sensitivity labels](/microsoft-365/compliance/sensitivity-labels).

## <a name="references"></a>Referências

- [Ofertas de conformidade da Microsoft](/microsoft-365/compliance/offering-home)
