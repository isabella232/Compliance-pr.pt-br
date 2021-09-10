---
title: Resiliência de dados no Microsoft 365
description: Neste artigo, saiba mais sobre o design e os princípios de resiliência e recuperação de dados no Microsoft 365.
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
ms.openlocfilehash: 48fe50347e7e81c7e5f8552299c04a268b8b449c
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2021
ms.locfileid: "58946872"
---
# <a name="data-resiliency-in-microsoft-365"></a>Resiliência de dados no Microsoft 365

Dada a natureza complexa da computação em nuvem, a Microsoft tem em mente que não é um caso de se as coisas vão dar errado, mas sim quando. Projetamos nossos serviços de nuvem para maximizar a confiabilidade e minimizar os efeitos negativos nos clientes quando as coisas deem errado. Ultrapassamos a estratégia tradicional de confiar em infraestrutura física complexa e construímos redundância diretamente em nossos serviços de nuvem. Usamos uma combinação de infraestrutura física menos complexa e software mais inteligente que cria resiliência de dados em nossos serviços e oferece alta disponibilidade para nossos clientes.

## <a name="resiliency-and-recoverability-are-built-in"></a>Resiliência e capacidade de recuperação são integrados

A criação de resiliência e recuperação começa com a suposição de que a infraestrutura e os processos subjacentes falharão em algum momento: o hardware (infraestrutura) falhará, os humanos cometerão erros e o software terá bugs. Embora seja incorreto dizer que os desenvolvedores de software não estavam pensando nessas coisas antes da nuvem, como esses problemas eram tratados em uma implementação de TI típica era diferente antes da nuvem:

- Primeiro, as proteções de hardware e infraestrutura eram significativas. Essa estrutura significava ter datacenters com confiabilidade de 99,99% que exigiam redundância significativa de rede e energia, e os servidores foram implementados com clustering baseado em hardware, fontes de alimentação duplas, interfaces de rede duplas e semelhantes.
- Segundo, o processo foi fundamental. As equipes de operações mantinham procedimentos rigorosos, as janelas de alteração eram empregadas e frequentemente havia sobrecarga significativa de gerenciamento de projeto.
- Em terceiro lugar, a implantação ocorreu em um ritmo glaciar. A implantação de código sem a propriedade da fonte significava esperar por versões de patch, e as versões principais envolviam a substituição de hardware e a sobreposição de capital significativa. Além disso, a única maneira de corrigir um problema era reverter. Assim, a maioria das organizações de IT implantaria apenas versões principais para evitar o trabalho para se manter atualizado.
- Por fim, a escala de sistemas implantados e o nível de sua interconexão era historicamente muito menor do que agora.

Hoje, os clientes esperam inovação contínua da Microsoft sem comprometer a qualidade, e esse é um dos motivos pelos quais os serviços e software da Microsoft são construídos com resiliência e capacidade de recuperação em mente.

## <a name="microsoft-365-data-resiliency-principles"></a>Microsoft 365 princípios de resiliência de dados

A resiliência refere-se à capacidade de um serviço baseado em nuvem suportar determinados tipos de falhas e ainda permanecer totalmente funcional da perspectiva dos clientes. A resiliência de dados significa que, independentemente das falhas que ocorrem no Microsoft 365, os dados críticos do cliente permanecem intactos e não afetados. Para esse fim, Microsoft 365 serviços foram projetados em torno de cinco princípios específicos de resiliência:

- Há dados críticos e não críticos. Dados não críticos (por exemplo, se uma mensagem foi lida) podem ser descartados em cenários de falha rara. Dados críticos (por exemplo, dados do cliente, como mensagens de email) devem ser protegidos a custo extremo. Como uma meta de design, as mensagens de email entregues são sempre críticas, e coisas como se uma mensagem foi lida não é crítica.
- Cópias de dados do cliente devem ser separadas em zonas de falha diferentes ou no maior número possível de domínios de falha (por exemplo, datacenters, acessíveis por credenciais simples (processo, servidor ou operador)) para fornecer isolamento de falhas. 
- Os dados críticos do cliente devem ser monitorados para falha em qualquer parte de Atomicity, Consistency, Isolation, Durability (ACID).
- Os dados do cliente devem ser protegidos contra corrupção. Ele deve ser verificado ativamente ou monitorado, reparado e recuperável.
- A maioria dos resultados de perda de dados de ações do cliente permite que os clientes se recuperem por conta própria usando uma GUI que permite restaurar itens excluídos acidentalmente.

Por meio da criação de nossos serviços de nuvem para esses princípios, juntamente com testes e validação robustos, o Microsoft 365 é capaz de atender e exceder os requisitos dos clientes, garantindo uma plataforma para inovação contínua e melhoria.

## <a name="related-articles"></a>Artigos relacionados

- [Lidando com dados corrompidos](assurance-dealing-with-data-corruption.md)
- [Proteção contra ransomware e malware](assurance-malware-and-ransomware-protection.md)
- [Monitoramento e Autorrecuperação](assurance-monitoring-and-self-healing.md)
- [Exchange Resiliência de Dados](assurance-exchange-data-resiliency.md)
