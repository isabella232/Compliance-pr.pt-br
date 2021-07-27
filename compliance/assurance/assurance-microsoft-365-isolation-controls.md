---
title: Controles de isolamento do Microsoft 365
description: Saiba mais sobre controles de isolamento Microsoft 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 1876ee933b0f94057abb2a6edd8fae9ca66111a4
ms.sourcegitcommit: 07578a8e03b931f47c49f4e34b78cf8ba0605e8f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/23/2021
ms.locfileid: "53573439"
---
# <a name="microsoft-365-isolation-controls"></a>Controles de isolamento do Microsoft 365

A Microsoft trabalha continuamente para garantir que a arquitetura de vários locatários do Microsoft 365 dê suporte à segurança, confidencialidade, privacidade, integridade, padrões locais, internacionais e de disponibilidade no nível [da empresa.](https://www.microsoft.com/trust-center/compliance/compliance-overview) A escala e o escopo dos serviços fornecidos pela Microsoft dificultam e não são econômicos gerenciar Microsoft 365 com interação humana significativa. Microsoft 365 serviços são fornecidos por meio de data centers distribuídos globalmente, cada um altamente automatizado com poucas operações que exigem um toque humano ou qualquer acesso ao conteúdo do cliente. Nossa equipe dá suporte a esses serviços e data centers usando ferramentas automatizadas e acesso remoto altamente seguro.

Microsoft 365 é composto por vários serviços que fornecem funcionalidades comerciais importantes e contribuem para toda Microsoft 365 experiência. Cada um desses serviços é autoconstruido e projetado para se integrar uns aos outros. Microsoft 365 é projetado com os seguintes princípios:

- Arquitetura orientada para serviço: projetando e desenvolvendo software na forma de serviços interoperáveis que proporcionam funcionalidades de negócios bem definidas.
- Garantia de segurança operacional [:](https://www.microsoft.com/securityengineering/osa)uma estrutura que incorpora o conhecimento obtido por meio de vários recursos exclusivos da [Microsoft,](https://www.microsoft.com/sdl/default.aspx)incluindo o Ciclo de Vida de Desenvolvimento de Segurança da [Microsoft,](https://www.microsoft.com/msrc)o Centro de Resposta à Segurança da Microsoft e uma profunda conscientização sobre o cenário de ameaças de segurança cibernética.

Microsoft 365 os serviços interagem entre si, mas são projetados e implementados para que possam ser implantados e operados como serviços autônomos, independentemente uns dos outros. A Microsoft segrega direitos e áreas de responsabilidade Microsoft 365 reduzir oportunidades de modificação não autorizada ou não intencional ou uso indevido dos ativos da organização. Microsoft 365 equipes têm funções definidas como parte de um mecanismo de controle de acesso baseado em função abrangente.

## <a name="tenant-isolation"></a>Isolamento de locatário

Um dos principais benefícios da computação em nuvem é o conceito de uma infraestrutura comum compartilhada entre vários clientes simultaneamente, levando a economias de escala. A Microsoft trabalha continuamente para garantir que as arquiteturas multilocatário de nossos serviços de nuvem dão suporte a padrões de segurança, confidencialidade, privacidade, integridade e disponibilidade de nível empresarial.

Os serviços de nuvem da Microsoft foram projetados com a suposição de que todos os locatários são potencialmente hostil a todos os outros locatários, e implementamos medidas de segurança para impedir que as ações de um locatário afetem a segurança ou o serviço de outro locatário ou acessem o conteúdo de outro locatário.

Os dois principais objetivos de manter o isolamento de locatários em um ambiente de vários locatários são:

- Impedir vazamento de conteúdo do cliente ou acesso não autorizado a locatários; e
- Impedir que as ações de um locatário afetem adversamente o serviço para outro locatário

Várias formas de proteção foram implementadas em todo o Microsoft 365 para impedir que os clientes comprometerem serviços ou aplicativos do Microsoft 365 ou obtenham acesso não autorizado às informações de outros locatários ou do próprio sistema Microsoft 365, incluindo:

- O isolamento lógico do conteúdo do cliente em cada locatário para serviços Microsoft 365 é obtido por meio Azure Active Directory autorização e controle de acesso baseado em função.
- SharePoint Online fornece mecanismos de isolamento de dados no nível de armazenamento.
- A Microsoft usa segurança física rigorosa, triagem em segundo plano e uma estratégia de criptografia em várias camadas para proteger a confidencialidade e a integridade do conteúdo do cliente. Todos Microsoft 365 datacenters têm controles de acesso biométrico, com a maioria exigindo impressões de palma para obter acesso físico. Além disso, todos os funcionários da Microsoft baseados nos EUA são necessários para concluir com êxito uma verificação padrão em segundo plano como parte do processo de contratação. Para obter mais informações sobre os controles usados para acesso administrativo Microsoft 365, [consulte Microsoft 365 Controles de Acesso Administrativo.](assurance-administrative-access-controls-overview.md)
- Microsoft 365 usa tecnologias do lado do serviço que criptografam o conteúdo do cliente em repouso e em trânsito, incluindo o BitLocker, a criptografia por arquivo, o TLS (Transport Layer Security) e o Internet Protocol Security (IPsec). Para obter detalhes específicos sobre criptografia Microsoft 365, consulte [Tecnologias de Criptografia](/microsoft-365/compliance/office-365-encryption-in-the-microsoft-cloud-overview)de Dados em Microsoft 365 .

Juntas, as proteções listadas acima fornecem controles de isolamento lógico robustos que fornecem proteção contra ameaças e mitigação equivalentes às fornecidas apenas pelo isolamento físico.

## <a name="resources"></a>Recursos

- [Isolamento e controle de acesso no Azure Active Directory](/microsoft-365/enterprise/microsoft-365-isolation-in-azure-active-directory)
- [Monitorando e testando limites de locatários](assurance-monitoring-and-testing.md)
- [Isolamento e controle de acesso no Microsoft 365](/microsoft-365/enterprise/microsoft-365-isolation-in-microsoft-365)
