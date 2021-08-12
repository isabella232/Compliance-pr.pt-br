---
title: Estratégia de defesa contra negação de serviço do Microsoft 365
description: Neste artigo, você pode encontrar uma visão geral da estratégia de defesa da Microsoft para ataques de negação de serviço (DoS).
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
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
ms.openlocfilehash: 720925408016af86d0bb16590f341970c0c5f0d0958c91b12e6b810c9b8a939a
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/05/2021
ms.locfileid: "54290589"
---
# <a name="microsoft-365-denial-of-service-defense-strategy"></a>Estratégia de defesa contra negação de serviço do Microsoft 365

## <a name="core-principles-of-defense-against-denial-of-service-attacks"></a>Princípios básicos de defesa contra ataques de negação de serviço

Há três princípios fundamentais ao se defender contra ataques de negação de serviço (DoS) baseados em rede: absorção, detecção e mitigação. A absorção ocorre antes da detecção e a detecção deve ocorrer antes que a mitigação possa começar. Se mesmo um pequeno ataque do DoS não puder ser absorto, os serviços não sobreviverão por tempo suficiente para que o ataque seja detectado. Detectando um ataque antes que o sistema seja sobrecarregado, os defensores podem implementar um plano de resposta.

A fórmula a seguir ajuda a aproximar o tempo de impacto de um ataque do DoS:

  **Capacidade Máxima (em bytes/seg) / Taxa de Crescimento (em bytes/seg) = Tempo para Impacto (em segundo)**

Se o tempo de detecção for maior do que o tempo de impacto, o ataque do DoS provavelmente será bem-sucedido. Se o tempo de detecção for menor do que o tempo de impacto, os serviços atacados devem permanecer online e acessíveis se as estratégias de mitigação são bem-sucedidas.

Portanto, há duas estratégias principais para se defender contra ataques do DoS:

- Aumentar a capacidade de elevar o teto da capacidade máxima (que, por sua vez, oferece mais tempo para detectar um ataque); ou
- Reduza o tempo para detectar um ataque.

Um benefício de segurança do uso dos serviços de nuvem da Microsoft é a forma como as serviços Microsoft de rede em grande escala fornecem uma proteção de rede forte aos clientes de nuvem de maneira econômica. Mesmo em grande escala, deve haver um equilíbrio entre a absorção, a detecção e a mitigação. Para encontrar esse equilíbrio, a Microsoft pesquisa taxas de crescimento de ataque para estimar quanto serviços Microsoft precisa ser absorvida.

## <a name="denial-of-service-defense-strategy"></a>Estratégia de defesa de negação de serviço

A estratégia da Microsoft para se defender contra ataques do DoS baseados em rede é exclusiva devido à nossa escala e ao nosso espaço global. Essa escala permite que a Microsoft utilize estratégias e técnicas que não estão disponíveis para a maioria das outras organizações. A base de nossa estratégia do DoS é nossa presença global. A Microsoft se envolve com provedores de Internet, provedores de paração (públicos e privados) e corporações privadas em todo o mundo. Esse envolvimento proporciona à Microsoft uma presença significativa na Internet e permite que a Microsoft absorva ataques em uma área de superfície grande.

À medida que a capacidade de borda da Microsoft aumentou com o passar do tempo, a significância dos ataques contra bordas individuais diminuiu substancialmente. Devido a essa diminuição, a Microsoft separa os componentes de detecção e mitigação de seu sistema de prevenção do DoS. A Microsoft implanta sistemas de detecção de várias camadas em datacenters regionais para detectar ataques mais próximos de seus pontos de saturação, mantendo a mitigação global nos nós de borda. Essa estratégia garante que o serviços Microsoft possa lidar com vários ataques simultâneos.

Uma das defesas mais eficazes e de baixo custo empregadas pela Microsoft contra ataques do DoS é reduzir superfícies de ataque de serviço. O tráfego indesejado é descartado na borda da rede em vez de analisar, processar e limpar os dados em linha.

Na interface com a rede pública, a Microsoft usa dispositivos de segurança de finalidade especial para funções de firewall, conversão de endereço de rede e filtragem de IP. A Microsoft também usa o roteamento global de vários caminhos de custo igual (ECMP). O roteamento ecmp global é uma estrutura de rede para garantir que haja vários caminhos globais para alcançar um serviço. Com vários caminhos para cada serviço, os ataques do DoS são limitados à região da qual o ataque se origina. Outras regiões devem ser afetadas pelo ataque, pois os usuários finais usariam outros caminhos para alcançar o serviço nessas regiões. A Microsoft também desenvolveu sistemas internos de correlação e detecção do DoS que usam dados de fluxo, métricas de desempenho e outras informações para detectar rapidamente ataques do DoS.

Para proteger ainda mais nossos serviços de nuvem, o Microsoft 365 usa um sistema de defesa de negação de serviço distribuído (DDoS) integrado aos processos de monitoramento e testes de penetração contínuos do Microsoft Azure. O sistema de defesa do Azure DDoS foi projetado não apenas para suportar ataques externos, mas também ataques de outros locatários do Azure. O Azure usa técnicas padrão de detecção e mitigação, como cookies SYN, limitação de taxa e limites de conexão para proteger contra ataques DDoS. Para dar suporte a nossas proteções automatizadas, uma equipe de resposta a incidentes do DoS entre cargas de trabalho identifica as funções e responsabilidades entre as equipes, os critérios para escalonamentos e os protocolos para o tratamento de incidentes entre as equipes afetadas.

A maioria dos ataques do DoS lançados contra destinos está nas camadas Rede (L3) e Transporte (L4) do modelo OSI [(Open Systems Interconnection).](/windows-hardware/drivers/network/windows-network-architecture-and-the-osi-model) Os ataques direcionados às camadas L3 e L4 foram projetados para inundar uma interface de rede ou serviço com tráfego de ataque para sobrecarregar recursos e negar a capacidade de responder a tráfego legítimo. Para proteger contra ataques L3 e L4, as soluções do DoS da Microsoft usam dados de amostragem de tráfego de roteadores de datacenter para proteger a infraestrutura e os destinos do cliente. Os dados de amostragem de tráfego são analisados por um serviço de monitoramento de rede para detectar ataques. Quando um ataque é detectado, os mecanismos de defesa automatizados são ativos para reduzir o ataque e garantir que o tráfego de ataque direcionado a um cliente não resulte em danos colaterais ou diminuição da qualidade do serviço de rede para outros clientes.

## <a name="application-level-defenses"></a>Defesas no nível do aplicativo

As equipes de engenharia da Microsoft seguem os rigorosos padrões definidos pelo [Microsoft Operational Security Assurance](https://www.microsoft.com/SDL/OperationalSecurityAssurance) para ajudar a proteger os dados do cliente. Os serviços de nuvem da Microsoft são intencionalmente construídos para dar suporte a cargas elevadas, o que ajuda a proteger contra ataques do DoS no nível do aplicativo. Microsoft 365 arquitetura dimensionada da Microsoft 365 distribui serviços em vários datacenters globais com recursos de isolamento regional e de retração específicos da carga de trabalho para cargas de trabalho relevantes.

O país ou região de cada cliente, que o administrador do cliente identifica durante a configuração inicial dos serviços, determina o local de armazenamento principal para os dados desse cliente. Os dados do cliente são replicados entre datacenters redundantes de acordo com uma estratégia primária/de backup. Um datacenter primário hospeda o software do aplicativo juntamente com todos os principais dados do cliente em execução no software. Um datacenter de backup fornece failover automático. Se o datacenter principal deixar de funcionar por qualquer motivo, as solicitações serão redirecionadas para a cópia do software e dos dados do cliente no datacenter de backup. A qualquer momento, os dados do cliente podem ser processados no datacenter primário ou de backup. A distribuição de dados em vários datacenters reduz a área de superfície afetada caso um datacenter seja atacado. Além disso, os serviços no datacenter afetado podem ser redirecionados rapidamente para o datacenter secundário para manter a disponibilidade durante um ataque e redirecionados de volta para o datacenter principal depois que um ataque foi mitigado.

Como outra mitigação contra ataques do DoS, as cargas de trabalho individuais incluem recursos integrados que gerenciam a utilização de recursos. Por exemplo, os mecanismos de Exchange Online e SharePoint Online fazem parte de uma abordagem em várias camadas para se defender contra ataques do DoS.
