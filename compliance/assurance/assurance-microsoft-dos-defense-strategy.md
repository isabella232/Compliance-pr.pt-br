---
title: Estratégia de defesa de negação de serviço da Microsoft
description: Neste artigo, você pode encontrar uma visão geral da estratégia de defesa da Microsoft para ataques de negação de serviço (DoS).
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
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: e1613765d3ffb7b43b80d07823fe8aef45719b70
ms.sourcegitcommit: cb0b058800d3a8f04921066b4c59fb427eb9c268
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/23/2021
ms.locfileid: "59486188"
---
# <a name="microsoft-denial-of-service-defense-strategy"></a>Estratégia de defesa de negação de serviço da Microsoft

## <a name="denial-of-service-defense-strategy"></a>Estratégia de defesa de negação de serviço

A estratégia da Microsoft para se defender contra ataques DDoS (negação de serviço distribuído) baseados em rede é exclusiva devido a um grande impacto global, permitindo que a Microsoft utilize estratégias e técnicas que não estão disponíveis para a maioria das outras organizações. Além disso, a Microsoft contribui para e extrai do conhecimento coletivo agregado por uma extensa rede de inteligência contra ameaças, que inclui parceiros da Microsoft e a comunidade de segurança da Internet mais ampla. Essa inteligência, juntamente com as informações coletadas dos serviços online e da base global de clientes da Microsoft, melhora continuamente o sistema de defesa DDoS da Microsoft que protege todos os ativos dos serviços online da Microsoft.

A base da estratégia DDoS da Microsoft é a presença global. A Microsoft se envolve com provedores de Internet, provedores de paração (públicos e privados) e corporações privadas em todo o mundo. Esse envolvimento proporciona à Microsoft uma presença significativa na Internet e permite que a Microsoft absorva ataques em uma área de superfície grande

À medida que a capacidade de borda da Microsoft aumentou com o passar do tempo, a significância dos ataques contra bordas individuais diminuiu substancialmente. Devido a essa diminuição, a Microsoft separa os componentes de detecção e mitigação de seu sistema de prevenção DDoS. A Microsoft implanta sistemas de detecção de várias camadas em datacenters regionais para detectar ataques mais próximos de seus pontos de saturação, mantendo a mitigação global nos nós de borda. Essa estratégia garante que o serviços Microsoft possa lidar com vários ataques simultâneos.

Uma das defesas mais eficazes e de baixo custo empregadas pela Microsoft contra ataques DDoS é reduzir superfícies de ataque de serviço. O tráfego indesejado é descartado na borda da rede em vez de analisar, processar e limpar os dados em linha.

Na interface com a rede pública, a Microsoft usa dispositivos de segurança de finalidade especial para funções de firewall, conversão de endereço de rede e filtragem de IP. A Microsoft também usa o roteamento global de vários caminhos de custo igual (ECMP). O roteamento ecmp global é uma estrutura de rede para garantir que haja vários caminhos globais para alcançar um serviço. Com vários caminhos para cada serviço, os ataques DDoS são limitados à região da qual o ataque se origina. Outras regiões devem ser afetadas pelo ataque, pois os usuários finais usariam outros caminhos para alcançar o serviço nessas regiões. A Microsoft também desenvolveu sistemas internos de correlação e detecção DDoS que usam dados de fluxo, métricas de desempenho e outras informações para detectar rapidamente ataques DDoS.

Para proteger ainda mais os serviços de nuvem, a Microsoft usa a Proteção do Azure DDoS, um sistema de defesa DDoS integrado aos processos contínuos de monitoramento e testes de penetração do Microsoft Azure. A Proteção do Azure DDoS foi projetada não apenas para suportar ataques externos, mas também ataques de outros locatários do Azure. O Azure usa técnicas padrão de detecção e mitigação, como cookies SYN, limitação de taxa e limites de conexão para proteger contra ataques DDoS. Para dar suporte a proteções automatizadas, uma equipe de resposta a incidentes DDoS entre cargas de trabalho identifica as funções e responsabilidades entre as equipes, os critérios para escalonamentos e os protocolos para o tratamento de incidentes entre as equipes afetadas.

A maioria dos ataques DDoS lançados contra destinos está nas camadas Rede (L3) e Transporte (L4) do modelo OSI [(Open Systems Interconnection).](/windows-hardware/drivers/network/windows-network-architecture-and-the-osi-model) Os ataques direcionados às camadas L3 e L4 foram projetados para inundar uma interface de rede ou serviço com tráfego de ataque para sobrecarregar recursos e negar a capacidade de responder a tráfego legítimo. Para proteger contra ataques L3 e L4, as soluções DDoS da Microsoft usam dados de amostragem de tráfego de roteadores de datacenter para proteger a infraestrutura e os destinos do cliente. Os dados de amostragem de tráfego são analisados por um serviço de monitoramento de rede para detectar ataques. Quando um ataque é detectado, os mecanismos de defesa automatizados são ativos para reduzir o ataque e garantir que o tráfego de ataque direcionado a um cliente não resulte em danos colaterais ou diminuição da qualidade do serviço de rede para outros clientes.

A Microsoft também tem uma abordagem ofensiva para a defesa DDoS. Botnets são uma fonte comum de comando e controle para conduzir ataques DDoS para ampliar ataques e manter o anonimato. A Unidade de Crimes Digitais da Microsoft (DCU) se concentra na identificação, investigação e interrupção da infraestrutura de distribuição e comunicações de malware para reduzir a escala e o impacto das botnets.

## <a name="application-level-defenses"></a>Defesas no nível do aplicativo

As equipes de engenharia da Microsoft seguem os rigorosos padrões definidos pelo [Microsoft Operational Security Assurance](https://www.microsoft.com/SDL/OperationalSecurityAssurance) para ajudar a proteger os dados do cliente. Os serviços de nuvem da Microsoft são intencionalmente construídos para dar suporte a cargas elevadas, o que ajuda a proteger contra ataques DDoS no nível do aplicativo. A arquitetura de dimensionamento da Microsoft distribui serviços em vários datacenters globais com isolamento regional e recursos de throttling específicos da carga de trabalho para cargas de trabalho relevantes.

O país ou região de cada cliente, que o administrador do cliente identifica durante a configuração inicial dos serviços, determina o local de armazenamento principal para os dados desse cliente. Os dados do cliente são replicados entre datacenters redundantes de acordo com uma estratégia primária/de backup. Um datacenter primário hospeda o software do aplicativo juntamente com todos os principais dados do cliente em execução no software. Um datacenter de backup fornece failover automático. Se o datacenter principal deixar de funcionar por qualquer motivo, as solicitações serão redirecionadas para a cópia do software e dos dados do cliente no datacenter de backup. A qualquer momento, os dados do cliente podem ser processados no datacenter primário ou de backup. A distribuição de dados em vários datacenters reduz a área de superfície afetada caso um datacenter seja atacado. Além disso, os serviços no datacenter afetado podem ser redirecionados rapidamente para o datacenter secundário para manter a disponibilidade durante um ataque e redirecionados de volta para o datacenter principal depois que um ataque foi mitigado.

Como outra mitigação contra ataques DDoS, as cargas de trabalho individuais incluem recursos integrados que gerenciam a utilização de recursos. Por exemplo, os mecanismos de Exchange Online e SharePoint Online fazem parte de uma abordagem em várias camadas para se defender contra ataques DDoS.

Banco de Dados SQL do Azure tem uma camada extra de segurança na forma de um serviço de gateway chamado DoSGuard que rastreia tentativas de logon com base no endereço IP. Se o limite para tentativas de logon com falha do mesmo IP for atingido, o DoSGuard bloqueará o endereço por um período de tempo pré-determinado.

## <a name="resources"></a>Recursos

- [Visão geral do Azure DDoS Protection Standard](/azure/ddos-protection/ddos-protection-overview)
- [Práticas recomendadas fundamentais do Azure DDoS Protection Standard](/azure/ddos-protection/fundamental-best-practices)
- [Componentes de uma estratégia de resposta DDoS](/azure/ddos-protection/ddos-response-strategy)
