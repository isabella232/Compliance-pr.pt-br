---
title: Arquitetura e infraestrutura de datacenter
description: Uma visão geral da arquitetura e da infraestrutura do datacenter da Microsoft.
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
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 44876abef95f269d454139fd721194ef3d48dcd4
ms.sourcegitcommit: cf424cb1e7c12048120977f294f780b776119a96
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/11/2021
ms.locfileid: "60265077"
---
# <a name="datacenter-architecture-and-infrastructure"></a>Arquitetura e infraestrutura de datacenter

Os datacenters da Microsoft foram projetados para implementar uma estratégia de defesa aprofundada, empregando várias camadas de proteções para proteger confiávelmente nossa arquitetura de nuvem e oferecer suporte à infraestrutura. A redundância é criada em todos os sistemas em vários níveis para dar suporte à disponibilidade do datacenter.

A Microsoft tem instalações de datacenter altamente protegidas em todo o mundo criando uma infraestrutura de datacenter distribuído, suportando milhares de serviços online. Essa infraestrutura distribuída globalmente foi projetada para aproximar os aplicativos dos usuários, preservar a residência de dados e oferecer opções abrangentes de conformidade e resiliência para clientes.

Regiões são conjuntos de datacenters que são interconectados por meio de uma rede massivo e resiliente. As regiões são organizadas em geografias, concedendo aos clientes uma residência de dados específica e a conformidade precisa da capacidade de manter seus dados e aplicativos próximos. A tolerância a falhas embutida permite que as geografias suportem a falha completa da região por meio de sua conexão com a infraestrutura de rede dedicada e de alta capacidade.

Locais fisicamente separados em uma região são chamados de zonas de disponibilidade, cada um sendo feito de um ou mais datacenters equipados com energia independente, arrefego e rede. As zonas de disponibilidade permitem que aplicativos críticos de missão executem com alta disponibilidade e replicação de baixa latência.

Datacenters geograficamente distribuídos permitem que a Microsoft traga serviços mais perto dos clientes, reduza a latência de rede e permita backup e failover geo-redundantes.

## <a name="availability"></a>Disponibilidade

Os datacenters da Microsoft são projetados para fornecer 99,999% de disponibilidade para atender às necessidades de serviço e SLAs do cliente. A Microsoft investe significativamente nas operações globais, gerenciamento, redes e sustentabilidade de instalações que oferecem serviços 24x7x365.

## <a name="compliance-standards-and-requirements"></a>Requisitos e padrões de conformidade

A Microsoft investiu mais de US$ 15 bilhões criando nossa infraestrutura global e mais de US$ 9 bilhões em pesquisa e desenvolvimento para aumentar a eficiência e impulsionar a inovação. Como resultado, os datacenters da Microsoft estão evoluindo em um ritmo mais rápido do que muitas instalações no setor e, portanto, não seguem os requisitos prescritivos descritos pelos padrões de datacenter tradicionais. Além da riqueza de informações operacionais que vêm com a execução de um dos maiores portfólios de datacenter do mundo, a Microsoft usa dados do IEEE Gold Book e software de simulação de confiabilidade de terceiros para melhorar continuamente nossos padrões de design de datacenter. Os datacenters da Microsoft são auditados extensivamente como parte de várias auditorias regulatórias, conforme chamado no portfólio de conformidade. O nível de vencimento nos datacenters da Microsoft pode ser avaliado por meio do portfólio de conformidade e, para resiliência especificamente, a certificação ISO 22301.

Embora a Microsoft opere programas em alinhamento com o espírito da Infraestrutura de Telecomunicações ANSI/TIA-942 do Datacenters Standard, partes desse padrão não são aplicáveis à Microsoft ou conflitam com outros requisitos regulatórios e/ou específicos do país. Além disso, a Microsoft optou por usar uma abordagem mais baseada em desempenho para corresponder às necessidades do cliente.

## <a name="data-and-network-redundancy"></a>Redundância de dados e de rede

Instalações críticas de datacenter empregam várias camadas de sistemas redundantes para sustentar falhas e minimizar interrupções de serviço. O armazenamento com redundância local no nível do disco protege os dados em uma região, com armazenamento com redundância geográfica fornecendo redundância dentro da região. Para garantir comunicações de rede confiáveis, a Microsoft possui e utiliza diversas rotas de fibra e hardware redundante para proteger componentes críticos contra falhas ou interrupções de serviço.

A replicação geográfica é usada para fornecer redundância para locais geográficos alternativos. A durabilidade dos dados é obtida pela réplica síncrona de dados em vários bancos de dados em datacenters diferentes. Os testes de restauração são executados para todos os dados de backup pertencentes à nuvem. A Recuperação de Desastre é atingida pela replicação assíncrona para um datacenter em uma região geográfica diferente.

## <a name="capacity"></a>Capacidade

Operações na nuvem é uma equipe de capacidade dedicada que prevê os requisitos futuros para garantir que a capacidade necessária seja estruturada e disponível para uso interno e do cliente. Os sistemas são monitorados para garantir o desempenho, a disponibilidade, a utilização do serviço, a utilização do armazenamento, a latência da rede e a capacidade de log de auditoria. A Microsoft também protege datacenters contra os efeitos de ataques de negação de serviço na largura de banda, capacidade transacional e capacidade de armazenamento.

Todas as equipes de serviço incluem o planejamento de capacidade como um recurso importante de seus modelos de datacenter e planos de replicação de dados para garantir que haja capacidade necessária para processamento de informações, telecomunicações e suporte ao ambiente.

## <a name="power"></a>Potência

Os datacenters da Microsoft têm upss (fontes de alimentação ininterruptíveis) dedicadas 24x7 e suporte a energia de emergência, que inclui geradores no local que fornecem energia de backup. A manutenção planejada e os testes são realizados nas UPS e nos geradores, e as equipes de operação têm acordos contratuais com fornecedores locais para fornecimento de combustível de emergência. Os datacenters também têm uma Central de Operações da Instalação, dedicado a monitorar os sistemas de energia, incluindo componentes elétricos essenciais.

Os datacenters da Microsoft são equipados com espaços de proteção e rotulagem apropriada para cabos. O equipamento de infraestrutura de energia é colocado em ambientes que foram projetados para proteger contra riscos ambientais. Todos os ativos de serviços online portáteis devem ser bloqueados ou fixados no local para fornecer proteção contra roubos ou danos de movimento. Os cabos de energia são executados sob os pisos, sobrecarga em bandejas de cabos e em gabinetes para proteção contra partes móveis e danos acidentais. Todos os espaços elétricos estão atrás de leitores de cartão ou bloqueios de chaves adicionais conforme apropriado. Os corredores de acesso, entradas externas e jardas de equipamento são monitorados por meio de vídeo de monitoramento. Os sistemas de energia também utilizam a redundância como uma forma de proteção, com vários feeds de energia/utilitário nas instalações e geradores e sistemas UPS.

Uma fonte de energia alternativa de longo prazo é implementada para o sistema de informações que é capaz de manter a energia em um recurso operacional minimamente necessário. Quando a energia falha ou cai para um nível de tensão inaceitável, os sistemas UPS instantaneamente são online. Isso fornece energia suficiente para executar os servidores até que os geradores possam assumir o controle. Os geradores de emergência fornecem energia de back-up para paralisações estendidas, manutenção planejada e podem operar o datacenter com reservas de energia local se ocorrer um desastre natural.

Os datacenters da Microsoft (locados e totalmente gerenciados) implementam a iluminação de emergência na forma de iluminação de emergência de sobrecarga em circuitos dedicados com backup por sistemas UPS e geradores. A iluminação de emergência automática é implementada de acordo com o Código de Segurança de Vida da Associação Nacional de Proteção e Incêndio (NFPA) ou o código/lei local aplicável. Se a energia do utilitário for perdida, a iluminação de emergência alterna automaticamente para a energia fornecida pelos sistemas UPS e gerador. Os sistemas de iluminação de emergência nos datacenters passam por manutenção de rotina para garantir que permaneçam em ordem de trabalho adequada.

## <a name="maintenance"></a>Manutenção

A política e os procedimentos de manutenção do sistema estão em prática de acordo com o Padrão de Segurança Física e Ambiental dos Serviços Online da *Microsoft.* Todos os equipamentos e sistemas da Microsoft são mantidos regularmente para garantir a eficiência operacional. A manutenção de qualquer equipamento ou sistema deve ser executada de acordo com as recomendações do fabricante, realizadas por funcionários autorizados e registradas em um tíquete de manutenção.

Há duas equipes de ativos que mantêm diferentes tipos de sistemas:

- **Equipe de Ambiente Crítico (CE):**

    - A CE é a equipe que fornece gerenciamento de instalações para sistemas elétricos, mecânicos e físicos que compõem a infraestrutura operacional da instalação. A equipe ce agenda, executa, documenta e revisa todas as atividades de manutenção realizadas em componentes ce. Os datacenters da Microsoft dependem de um sistema computadorizado para gerenciar agendas de manutenção e pedidos de trabalho.
    - O gerenciamento de datacenter (DCM) é responsável por toda a manutenção ce executada no site ou remotamente. A manutenção ce é prescrita em documentos passo a passo necessários chamados Métodos de Procedimento (MOP). Os MOPs são revisados/aprovados pelo gerenciamento de datacenter antes de qualquer início de trabalho.

- **Equipe de Serviços do Site:**

    - Os Serviços de Site são a equipe que fornece a manutenção dos ativos de serviço online da Microsoft localizados no datacenter da Microsoft. A equipe do Dc Site Services fornece um serviço de correção de mãos/quebras inteligentes para ativos pertencentes aos serviços de provisionamento de propriedades do datacenter. Por exemplo, ativos que exigem manutenção física podem solicitar o serviço de mãos inteligentes da equipe do Dc Site Services. Todos os Serviços de Site funcionam em ativos da Microsoft são agendados, executados, documentados e revisados em tíquetes de trabalho dentro da ferramenta de tíquete de fluxo de trabalho, e nenhum trabalho pode ocorrer sem um tíquete de trabalho aprovado.
    - O Gerente de Programas Técnicos (TPM) e a equipe do DCM são responsáveis por todo o trabalho dos Serviços de Site que ocorre no datacenter e pelo trabalho que exige que o ativo seja transferido fora do local. A manutenção dos Serviços de Site é executada em áreas do datacenter que são controladas e protegidas por mecanismos de segurança física.

Se os componentes ce são necessários para serem removidos da instalação, o tratamento do equipamento é aprovado pelo DCM. Na maioria das instâncias, os componentes ce recebem manutenção no local e não são removidos da instalação. Os ativos de propriedade (por exemplo, dispositivos de rede ou servidores) que exigem transferência externa devem ter aprovação explícita do proprietário do ativo.

A mídia digital dentro da nuvem pode não ser transportada do espaço de colocação, a menos que ela seja movida para ser destruída. Quando esses ativos devem ser destruídos, eles são armazenados em caixas de armazenamento bloqueadas que estão sob cobertura da câmera DOLS. Quando os ativos estão prontos para serem destruídos, um agente de segurança física e um funcionário em tempo integral da Microsoft do Gerenciamento de Ativos devem acompanhar a lixeira bloqueada do espaço de colocação para onde a trituração no local deve ocorrer. À medida que a trituração ocorre no datacenter e sob a supervisão da Microsoft, os ativos da Microsoft não saem das áreas controladas do datacenter.

Todo o trabalho de manutenção deve ser aprovado antes do início do trabalho, incluindo o acesso às ferramentas de manutenção do sistema. A Infraestrutura da Microsoft implementou o controle de ferramentas de manutenção criando um nível de acesso dentro da Ferramenta de Acesso do Datacenter (DCAT). Cada instalação contém uma caixa de bloqueio físico restrita ou uma sala controlada por acesso para o armazenamento de ferramentas de manutenção especializadas. O acesso à caixa de bloqueio ou à sala de armazenamento é controlado na ferramenta DCAT para proibir o acesso não autorizado às ferramentas de manutenção. Este programa garante que somente funcionários com acesso aprovado possam acessar as ferramentas. A equipe de Serviços de Site realiza verificações de inventário de rotina para verificar o status de todas as ferramentas. Trimestralmente, a equipe de gerenciamento de datacenter e as equipes de segurança física executam auditorias da lista de acesso do DCAT para manter a lista de acesso do pessoal de manutenção atual. As terminações ou transferências de funcionários são refletidas imediatamente por meio de uma atualização manual da lista de acesso. O acesso à caixa de bloqueio ou à sala de armazenamento de manutenção é rastreado nos logs de leitor de selos de acesso, que estão disponíveis para quaisquer investigações.

A equipe de Serviços de Site mantém um inventário de ferramentas de manutenção aprovadas para uso no datacenter. A equipe de manutenção é direcionada para usar as ferramentas de manutenção fornecidas. A aprovação do Gerenciamento de Datacenter (DCM) é necessária para usar ferramentas não fornecidas pelo datacenter. As ferramentas manuais físicas estão isentas desse tipo de controle.

Os datacenters da Microsoft mantêm a equipe de manutenção de residentes para dar suporte a sistemas críticos de infraestrutura de datacenter (a equipe de Ambiente Crítico) e operações de datacenter (a equipe de Serviços de Site). As equipes de Ambiente Crítico e Serviços de Site identificaram componentes críticos do sistema de tecnologia e segurança que mantêm sobressalente para o local. Os serviços críticos do sistema de informações são provisionados de mais de um datacenter para evitar uma interrupção no serviço devido a um incidente em um dos datacenters.
