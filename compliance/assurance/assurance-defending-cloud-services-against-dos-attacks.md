---
title: Defender os serviços de nuvem do Microsoft 365 contra ataques de negação de serviço
description: Neste artigo, saiba como a Microsoft defenderá seus serviços de nuvem contra ataques de Negação de Serviço (DoS).
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
ms.openlocfilehash: e632c1524d5cc8c21aec9dab3d95d285a3b8801e
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120570"
---
# <a name="defending-microsoft-365-cloud-services-against-denial-of-service-attacks"></a>Defender os serviços de nuvem do Microsoft 365 contra ataques de negação de serviço

Os datacenters da Microsoft são protegidos por segurança de defesa abrangente que inclui a cerca de perímetro, câmeras de vídeo, pessoal de segurança e entradas seguras que usam biometria, cartão inteligente e autenticação multifatores. A segurança de defesa abrangente continua em todas as áreas das instalações e em cada unidade de servidor físico. O [Microsoft Cloud Infrastructure and Operations Group](https://www.microsoft.com/cloud-platform/global-datacenters) oferece a infraestrutura principal e as tecnologias fundamentais para nossos serviços de nuvem. Nossos datacenters estão em conformidade com os padrões do setor para segurança física e confiabilidade e são gerenciados, monitorados e administrados pela equipe de operações da Microsoft.

Para proteger ainda mais nossos serviços de nuvem, a Microsoft fornece um sistema de defesa DDoS que faz parte dos processos de monitoramento contínuo e teste de penetração do Microsoft Azure. O sistema de defesa do Azure DDoS foi projetado não apenas para atacar ataques externos, mas também de outros locatários do Azure. O Azure usa técnicas padrão de detecção e mitigação, como cookies SYN, limitação de taxa e limites de conexão para proteger contra ataques DDoS.

Os serviços de nuvem da Microsoft estão sujeitos à ameaça de ataque de várias fontes. Para reduzir e proteger contra as várias ameaças do DoS, um sistema de mitigação e detecção de ameaças altamente escalonável e dinâmico baseado no Azure foi desenvolvido e implementado com o objetivo principal de proteger a infraestrutura subjacente contra ataques do DoS e ajudar a evitar interrupções de serviço para clientes de serviços de nuvem. O sistema de mitigação do Azure DoS protege o tráfego de entrada, saída e região para região.

A maioria dos ataques do DoS é lançada contra destinos nas camadas de rede (L3) e transporte (L4) do modelo [OSI (Open Systems Interconnection).](/windows-hardware/drivers/network/windows-network-architecture-and-the-osi-model) Os ataques direcionados às camadas L3 e L4 são projetados para inundar uma interface de rede ou serviço com tráfego de ataque para sobrecarregar os recursos e negar a capacidade de responder a tráfego legítimo. Especificamente, os ataques L3 e L4 tentam saturar a capacidade de links de rede, dispositivos ou serviços ou sobrecarregar as CPUs de servidores ou máquinas virtuais que suportam um aplicativo.

Para se proteger contra ataques L3 e L4, a Microsoft projetou, desenvolveu e implantou uma solução destinada especificamente a proteger a infraestrutura e os alvos do cliente que estão sob ataque protegendo essas camadas. Proteger a infraestrutura garante que o tráfego de ataque destinado a um cliente não resulte em danos materiais ou qualidade de serviço de rede diminuída para outros clientes. A solução usa dados de amostragem de tráfego de roteadores de datacenter. Esses dados são analisados por um serviço de monitoramento de rede para detectar ataques. Quando um ataque é detectado, mecanismos de defesa automatizados iniciam.

## <a name="application-level-defenses"></a>Application-Level Defesas do Application-Level
As equipes de engenharia da Microsoft seguem os rigorosos padrões definidos pela [Garantia de](https://www.microsoft.com/SDL/OperationalSecurityAssurance) Segurança Operacional da Microsoft para ajudar a proteger os dados do cliente. Os serviços de nuvem da Microsoft foram intencionalmente construídos para dar suporte a uma carga muito alta, bem como para proteger e atenuar contra ataques DoS no nível do aplicativo. Implementamos uma arquitetura dimensionada onde os serviços são distribuídos por vários datacenters globais com isolamento regional e recursos de throttling em algumas das cargas de trabalho.

O país ou a região de cada cliente, que o administrador do cliente identifica durante a configuração inicial dos serviços, determina o local de armazenamento principal para os dados desse cliente. Os dados do cliente são replicados entre datacenters redundantes de acordo com uma estratégia principal/de backup. Um datacenter primário hospeda o software do aplicativo juntamente com todos os dados principais do cliente em execução no software. Um datacenter de backup fornece failover automático. Se o datacenter primário deixar de funcionar por qualquer motivo, as solicitações serão redirecionadas para a cópia do software e dos dados do cliente no datacenter de backup. A qualquer momento, os dados do cliente podem ser processados no datacenter primário ou de backup. A distribuição de dados entre vários datacenters reduz a área de superfície afetada caso um datacenter seja prejudicado. Além disso, os serviços no datacenter afetado podem ser redirecionados rapidamente para o datacenter secundário como um dos mecanismos de recuperação e vice-versa (redirecionado de volta para o datacenter principal após a restauração do serviço).

As cargas de trabalho individuais incluem recursos integrados que gerenciam a utilização de recursos. Por exemplo, os mecanismos de controle no Exchange Online e no SharePoint Online fazem parte de uma abordagem de várias camadas para se defender contra ataques do DoS. A throttling para usuários do Exchange Online baseia-se no nível de recursos consumidos pelo usuário final, se os recursos estão no Active Directory, no armazenamento de informações do Exchange Online ou em outro lugar. Um orçamento é alocado a cada cliente para limitar os recursos consumidos por um usuário. A controle do Exchange Online para a atividade do usuário e componentes do sistema é baseada no gerenciamento [de carga de trabalho.](https://technet.microsoft.com/library/jj150503(v=exchg.150).aspx) Uma carga de trabalho do Exchange Online é um recurso, protocolo ou serviço do Exchange Online que foi explicitamente definido para as finalidades de gerenciamento de recursos do sistema do Exchange Online. Cada carga de trabalho do Exchange Online requer recursos do sistema, como CPU, operações de banco de dados de caixa de correio ou solicitações do Active Directory para executar solicitações de usuário ou trabalho em segundo plano. Exemplos de cargas de trabalho do Exchange Online incluem Outlook na Web, Exchange ActiveSync, migração de caixa de correio e assistentes de caixa de correio. Os administradores de locatários podem gerenciar as configurações de gerenciamento de carga de trabalho do Exchange para usuários com o Shell de Gerenciamento do Exchange. Há várias formas de replicação que foram implementadas no Exchange Online, incluindo PowerShell, Serviços Web do Exchange e POP e IMAP, Exchange ActiveSync, conexões de dispositivo móvel, destinatários e muito mais. Embora os administradores de implantações locais do Exchange possam configurar políticas de controle, os administradores não podem configurar políticas de controle para o Exchange Online.

O gatilho mais comum para a redução no SharePoint Online é o código do modelo de objeto do lado do cliente (CSOM) que executa muitas ações em uma frequência muito alta. Com o CSOM, muitas ações podem ser executadas com uma única solicitação, o que pode exceder os limites de uso e causar limitação por usuário.

Independentemente da atividade que pode resultar na limitação, quando um usuário excede os limites de uso, o SharePoint Online limita qualquer solicitação adicional dessa conta de usuário, geralmente por um curto período. Enquanto o acelerador do usuário estiver em vigor, todas as ações desse usuário serão aceleradas até que a aceleração expire, de acordo com os seguintes critérios:
- Para solicitações executadas pelo usuário diretamente em um navegador, o SharePoint Online redireciona para uma página de informações de throttling e as solicitações falham.
- Para todas as outras solicitações, incluindo chamadas CSOM, o SharePoint Online retorna o código de status HTTP 429 ("muitas solicitações") e as solicitações falham.

Se o processo ofensivo continuar excedendo os limites de uso, o SharePoint Online poderá bloquear completamente o processo e retornar o código de status HTTP 503 ("serviço indisponível").

## <a name="vulnerability-and-penetration-testing"></a>Teste de vulnerabilidade e penetração
A Microsoft [](https://www.microsoft.com/trustcenter/security/threatmanagement) usa muitas [](https://blogs.technet.microsoft.com/hybridcloud/2015/05/05/protecting-your-datacenter-and-cloud-from-emerging-threats/) tecnologias e práticas de segurança para proteger sua infraestrutura de nuvem e redes locais contra ameaças modernas e sofisticadas, incluindo o uso de componentes e serviços antimalware para serviços de nuvem, máquinas virtuais (VMs) e outros sistemas. Advanced Threat Analytics, which monitors normal usage patterns for networks, systems, and users, and employs machine learning to flag any behavior that is out the normal, and regular penetration testing.

Além de realizar nossos próprios testes de penetração e oferecer aos nossos clientes um programa de Teste de Penetração Unificada na Nuvem da [Microsoft,](https://technet.microsoft.com/mt784683)também nos envolvemos com profissionais de segurança de terceiros que realizam avaliações regulares de vulnerabilidades e testes de penetração em nossos serviços de nuvem. Disponibilizamos os relatórios dessas avaliações de vulnerabilidade de terceiros [](https://aka.ms/STP) para download nos portais de Confiança do Serviço e de Garantia [do](https://aka.ms/ServiceAssurance) Serviço.
