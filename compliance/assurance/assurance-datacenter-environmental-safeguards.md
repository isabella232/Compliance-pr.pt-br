---
title: Proteções ambientais do datacenter
description: Saiba mais sobre as proteções ambientais do datacenter da Microsoft.
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
ms.openlocfilehash: 525aab55d3f56490ecd1f1da1e00d6c5ddd32dc4
ms.sourcegitcommit: cf424cb1e7c12048120977f294f780b776119a96
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/11/2021
ms.locfileid: "60265075"
---
# <a name="datacenter-environmental-safeguards"></a>Proteções ambientais do datacenter

A Microsoft emprega várias proteções para proteger contra ameaças ambientais à disponibilidade do datacenter. Essas proteções permitem que a Microsoft forneça plataformas de nuvem seguras e disponíveis que são confiáveis pelos clientes.

## <a name="site-selection"></a>Seleção do local

A proteção dos datacenters da Microsoft contra riscos ambientais começa com a seleção do local onde serão construídos. Os locais passam por uma avaliação rigorosa antes de serem selecionados para a construção de um datacenter da Microsoft. Os sites de datacenter da Microsoft são selecionados estrategicamente para minimizar o risco de vários fatores, incluindo inundações, terremotos, furacões e outros desastres naturais. Além de minimizar o risco ambiental, o acesso à energia de baixo custo e à infraestrutura confiável de telecomunicações estão entre os principais fatores que influenciam a seleção da localização do datacenter.

## <a name="climate-control"></a>Controle climático

O controle climático é um componente fundamental da infraestrutura crítica dentro de um datacenter e é utilizado para monitorar e manter espaços condicionais otimizados para funcionários e equipamento/hardware. A carga de calor (como um subproduto do consumo de energia) e a umidade precisam ser gerenciadas para garantir condições operacionais adequadas por meio de intervenção mecânica. Condições climáticos locais, vários requisitos regulatórios e restrições determinarão a maneira mais eficiente de alcançar isso.

Os níveis de temperatura e umidade são mantidos de acordo com os requisitos ambientais do hardware de IT esperados em cada datacenter. Os datacenters da Microsoft mantêm um contrato de nível operacional com seus clientes para que a eficiência ideal seja atendida enquanto mantém requisitos ambientais mínimos. Os níveis de temperatura e umidade são monitorados continuamente pelo Sistema de Gerenciamento de Construção (BMS) do datacenter. Os membros da equipe ambientes críticos (CE) monitoram o BMS a partir do Centro de Operações de Instalações (FOC), para que eles possam gerenciar a temperatura e a umidade dentro do datacenter antes que qualquer ponto de alarme seja excedido. O BMS é configurado para notificar a equipe ce quando determinados marcadores são atingidos, que, em seguida, investigam e fazem ajustes para correção do problema climático. Intervalos aceitáveis para temperatura e umidade são consistentes com as diretrizes da American Society of Temperature, Refrigerating e Air-air engineers (ASHRAE) ou diretrizes locais semelhantes aplicáveis localmente. A umidade do datacenter é medida pela porcentagem de Umidade Relativa, Não Condensando com o intervalo atual entre 40%-55%. O intervalo de temperatura é geralmente entre 18 graus Celsius e 27 graus Celsius (entre 64,4 graus Fahrenheit e 80,6 graus Fahrenheit).

## <a name="fire-and-water-damage-protection"></a>Proteção contra danos causados por incêndio e água

A Microsoft emprega sistemas de detecção e supressão de incêndio de última geração em cada instalação do datacenter. Os sistemas de prevenção contra incêndios são suportados por uma fonte de energia independente para garantir a proteção dos funcionários e infraestrutura da Microsoft se houver um incêndio. As instalações dos datacenters também são protegidas de danos por sensores de vazamento de água colocados em áreas com risco de vazamentos. Esses sensores de água notificam rapidamente a equipe apropriada se houver uma emergência relacionada à água. As válvulas de desligamento de água foram projetadas para serem acessíveis e os funcionários são treinados em sua operação e localização.

Os datacenters da Microsoft implementam mecanismos robustos de detecção de incêndio, incluindo detectores de fumaça fotoelétrica instalados abaixo do piso e no teto, sistemas VESDA (Aparato de Detecção de Fumaça Muito Cedo) Xtralis em cada colocação, caixas de alarme de incêndio de estação de puxão instaladas em todos os datacenters, extintores de incêndio localizados em todos os datacenters, equipes de segurança em todas as áreas de construção várias vezes a cada oito horas de turno,  e os sistemas de detecção/supressão/supressão de incêndio e iluminação de emergência são conectados aos sistemas de energia de backup do datacenter fornecendo uma fonte de energia redundante. As áreas que contêm equipamentos elétricos confidenciais são protegidas por sistemas de pré-ação de intertravamento duplo (canal seco).

A equipe ce faz um passo a passo diário do site (DSWT) para verificar cada sala e muitas partes de componentes dentro delas para garantir que todos os requisitos de inspeção de incêndio estão sendo atendidos.

A Microsoft emprega dispositivos/sistemas de detecção de incêndio para o sistema de informações que ativa automaticamente e notifica o pessoal do datacenter juntamente com os respondentes de emergência se ocorrer um incêndio. Se um dos mecanismos de detecção de incêndio for ativado em qualquer espaço de colocação, o corpo de bombeiros local e o Centro de Operações de Segurança Global em Redmond, Washington será notificado automaticamente. Os sistemas de proteção e detecção de incêndio estão vinculados ao sistema de segurança notificando a equipe de segurança e instalações locais.

A Microsoft fornece detecção de água/vazamento em áreas com risco de vazamento de água. Os sistemas de supressão de incêndio também têm alarmes de detecção de vazamento monitorados. O sistema de detecção de água/vazamento é integrado ao sistema de notificação e alarme de instalações, e os sistemas de aspersão nos datacenters são zoneados. As equipes de Gerenciamento de Datacenter e CE estão familiarizados com os procedimentos de emergência que exigem o uso das válvulas de saída de água e seus locais. Os risers do pulverizador podem ser desligados individualmente ou como um grupo por meio de válvulas de portal. Todos os aspersores no espaço crítico são aspersores de pré-ação de intertravamento duplo que exigem duas formas de ativação antes que o fluxo seja iniciado. A pressão do sistema de aspersores é monitorada e alarmada contra vazamento de água.

## <a name="health-and-safety"></a>Saúde e segurança

O compromisso com a saúde e a segurança dos funcionários da Microsoft é fundamental para medir o sucesso. Os datacenters da Microsoft operam de acordo com os regulamentos locais, regionais, nacionais e federais de segurança e saúde. Na maioria dos casos, as políticas de segurança e saúde da Microsoft excedem os requisitos governamentais e regulatórios para garantir a proteção da saúde, segurança e bem-estar de todos os funcionários do datacenter durante todas as fases do ciclo de vida do datacenter, da construção ao descomissionamento. Planos de gerenciamento de segurança, avaliação de risco, gerenciamento de atividades de alto risco e treinamento de segurança são os princípios centrais para fornecer um ambiente de trabalho seguro para todos os funcionários.

## <a name="energy-efficiency"></a>Eficiência de energia

A Microsoft opera em carbono neutro desde 2012. Até 2030, a Microsoft será negativa por carbono e, até 2050, a Microsoft terá removido do ambiente todo o carbono que a empresa emitiu diretamente ou por consumo elétrico desde que foi criada em 1975. Até 2025, os datacenters da Microsoft serão fornecidos por 100% de energia renovável. Para atingir esse objetivo, a Microsoft implementou ferramentas de contratação, como contratos de compra de energia de geração de proxy para energia verde para fornecer 100% da eletricidade de emissão de carbono consumida por todos os datacenters.
