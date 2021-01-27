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
ms.openlocfilehash: 361400bf6330fb82d34f384d17e4d4ee438ccf08
ms.sourcegitcommit: b06fa9f1b230fd5e470817486ea51f460f28b691
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/27/2021
ms.locfileid: "50012897"
---
# <a name="data-resiliency-in-microsoft-365"></a>Resiliência de dados no Microsoft 365

Considerando a natureza complexa da computação em nuvem, a Microsoft está pensando em que não é um caso em que as coisas darão errado, mas em vez de quando. Projetamos nossos serviços de nuvem para maximizar a confiabilidade e minimizar os efeitos negativos sobre os clientes quando algo der errado. Nós nos movemos além da estratégia tradicional de depender de uma infraestrutura física complexa e temos criado redundância diretamente em nossos serviços de nuvem. Usamos uma combinação de infraestrutura física menos complexa e software mais inteligente que cria resiliência de dados em nossos serviços e oferece alta disponibilidade aos nossos clientes.

## <a name="resiliency-and-recoverability-are-built-in"></a>A resiliência e a capacidade de recuperação são integrados

Construir em resiliência e recuperação começa com a suposição de que a infraestrutura e os processos subjacentes falharão em algum momento: o hardware (infraestrutura) falhará, os humanos irão cometer erros e o software terá bugs. Embora não seja correto dizer que os desenvolvedores de software não estavam pensando nessas coisas antes da nuvem, como esses problemas eram tratados em uma implementação típica de TI era diferente antes da nuvem:

- Primeiro, as proteções de hardware e infraestrutura foram significativas. Essa estrutura significava ter datacenters com 99,99% de confiabilidade exigindo redundância significativa de rede e energia, e os servidores foram implementados com clustering baseado em hardware, fontes de alimentação duplas, interfaces de rede dupla e semelhantes.
- Segundo, o processo foi desmontado. As equipes de operações tinham procedimentos rigorosos, as janelas de alteração eram empregadas e muitas vezes havia uma sobrecarga de gerenciamento de projeto significativa.
- Terceiro, a implantação ocorreu em um ritmo lento. A implantação do código sem a propriedade da fonte significa aguardar versões de patch, e as versões principais envolveram a substituição de hardware e a sobreposição significativa de maiúsculas. Além disso, a única maneira de corrigir um problema era reverter. Assim, a maioria das organizações de IT implantaria apenas as principais versões para evitar que o trabalho se mantenha atualizado.
- Por fim, a escala de sistemas implantados e o nível de sua interconexão foram historicamente muito menores do que agora.

Hoje, os clientes esperam inovação contínua da Microsoft sem comprometer a qualidade, e esse é um dos motivos pelos quais os serviços e software da Microsoft são construídos com resiliência e capacidade de recuperação em mente.

## <a name="microsoft-365-data-resiliency-principles"></a>Princípios de resiliência de dados do Microsoft 365

A resiliência refere-se à capacidade de um serviço baseado em nuvem de suportar determinados tipos de falhas e ainda permanecer totalmente funcional da perspectiva dos clientes. A resiliência de dados significa que, independentemente das falhas que ocorrerem no Microsoft 365, os dados críticos do cliente permanecerão intactos e não serão afetados. Para isso, os serviços do Microsoft 365 foram projetados em torno de cinco princípios de resiliência específicos:

- Há dados críticos e não críticos. Dados não críticos (por exemplo, se uma mensagem foi lida) podem ser descartados em cenários de falha raras. Dados críticos (por exemplo, dados do cliente, como mensagens de email) devem ser protegidos a custo extremo. Como meta de design, as mensagens de email entregues são sempre críticas, e coisas como se uma mensagem foi lida não são críticas.
- Cópias de dados do cliente devem ser separadas em diferentes zonas de falha ou no máximo de domínios com falha possível (por exemplo, datacenters, acessíveis por credenciais individuais (processo, servidor ou operador)) para fornecer isolamento de falha. 
- Dados críticos do cliente devem ser monitorados em busca de falha em qualquer parte da atomicidade, consistência, isolamento, durabilidade (ACID).
- Os dados do cliente devem ser protegidos contra corrupção. Ela deve ser ativamente digitalizada ou monitorada, reparavel e recuperável.
- A maioria dos resultados de perda de dados de ações do cliente permite que os clientes se recuperem por conta própria usando uma GUI que permite restaurar itens excluídos acidentalmente.

Por meio da criação de nossos serviços de nuvem para esses princípios, juntamente com testes e validação robustos, o Microsoft 365 é capaz de atender e exceder os requisitos dos clientes, garantindo uma plataforma para inovação contínua e melhoria.

## <a name="related-articles"></a>Artigos relacionados

- [Lidando com dados corrompidos](assurance-dealing-with-data-corruption.md)
- [Proteção contra ransomware e malware](assurance-malware-and-ransomware-protection.md)
- [Monitoramento e Autorrecuperação](assurance-monitoring-and-self-healing.md)
- [Resiliência de dados do Exchange](assurance-exchange-data-resiliency.md)
