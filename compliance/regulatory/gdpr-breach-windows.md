---
title: Serviço de processador de dados da notificação do Windows Enterprise no âmbito do GDPR
description: Como o serviço de processador de dados do Windows Enterprise protege contra uma violação de dados pessoais e como a Microsoft responderá e o notificará se ocorrer uma violação.
keywords: Serviço de processador de dados do Windows Enterprise, Microsoft 365, documentação do Microsoft 365, GDPR
localization_priority: Priority
ROBOTS: NOINDEX, NOFOLLOW
ms.prod: microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmaz
manager: laurawi
ms.reviewer: delinat
audience: itpro
ms.collection:
- GDPR
- M365-security-compliance
- MS-Compliance
ms.openlocfilehash: 1fbbdb16fd1231d6044ed556090823cd36f90c78
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/23/2021
ms.locfileid: "53088860"
---
# <a name="data-processor-service-for-windows-enterprise-breach-notification-under-the-gdpr"></a>Serviço de processamento de dados da notificação de violação do Windows Enterprise sob o GDPR

>[!NOTE]
>Este tópico é destinado aos participantes do serviço de processador de dados do programa de visualização prévia do Windows Enterprise e requer a aceitação de termos de uso específicos. Para saber mais sobre o programa e concordar com os termos de uso, acesse [https://aka.ms/WindowsEnterprisePublicPreview](https://aka.ms/WindowsEnterprisePublicPreview).

O serviço do processador de dados da Microsoft para o Windows Enterprise leva a sério as suas obrigações nos termos do Regulamento Geral de Proteção de Dados (GDPR). O serviço de processador de dados da Microsoft para o Windows Enterprise toma extensas medidas de segurança para proteger contra violações de dados. Essas medidas incluem equipes dedicadas de gerenciamento de ameaças que atuam proativamente para prever, impedir e atenuar acessos mal-intencionados.Medidas de segurança interna como a verificação de portas, verificação de vulnerabilidades de perímetro e detecção de invasores detectam e impedem acessos mal-intencionados, além de processos de segurança automatizados, políticas abrangentes de privacidade e segurança da informação e treinamento de segurança e privacidade para todo o pessoal.

A segurança está incorporada no serviço de processador de dados da Microsoft para o Windows Enterprise desde o início, começando com o [Ciclo de Vida de Desenvolvimento de Segurança](https://www.microsoft.com/sdl/), um processo de desenvolvimento obrigatório que incorpora metodologias de privacidade por projeto e privacidade por defeito. O princípio orientador da estratégia de segurança da Microsoft é “presumir a violação”, uma extensão da estratégia de defesa em profundidade. Ao desafiar constantemente os recursos de segurança do serviço de processador de dados do Windows Enterprise, a Microsoft pode ficar à frente das ameaças emergentes. Para obter mais informações do serviço de processador de dados para a segurança do Windows Enterprise, reveja estes [recursos](https://www.microsoft.com/TrustCenter/Security/windows10-security), o serviço de processador de dados do Windows Enterprise responde a uma possível violação de dados de acordo com o processo de resposta a incidentes de segurança. A resposta a incidentes de segurança do serviço de processador de dados do Windows é implementada por um processo em cinco etapas: Detecção, Avaliação, Diagnóstico, Estabilização e Fechamento. A equipe de Resposta a Incidentes de Segurança pode alternar entre as etapas Diagnóstico e Estabilização à medida que a investigação progride. Abaixo um resumo do processo de resposta a incidentes de segurança:

|**Stage**|**Descrição**|
|:------- |:------------- |
| **_1: Detectar_* _ | Primeira indício de um possível incidente. |
| _*_2: Avaliar_*_ | Um membro de plantão da equipe de resposta a incidentes avalia o impacto e a gravidade do evento. Com base em evidências, a avaliação pode ou não resultar num escalonamento à equipe de resposta de segurança. |
| _*_3: Diagnosticar_*_ | Os especialistas em resposta de segurança realizam a investigação técnica ou forense, identificam estratégias de contenção, mitigação e solução alternativa. Se a equipe de segurança achar que os dados do cliente podem ter sido expostos a um indivíduo criminoso ou não autorizado, a execução do processo de Notificação de Incidente do Cliente começa em paralelo. |
| _*_4: Estabilizar e Recuperar_*_ | A equipe de resposta a incidentes cria um plano de recuperação para atenuar o problema. As etapas de contenção de crise, como colocar em quarentena os sistemas afetados, podem ocorrer imediatamente e em paralelo com o diagnóstico. As atenuações de longo prazo podem ser planejadas, e ocorrer após o risco imediato ter passado. |
| _*_5: Fechar e post-mortem_*_ | A equipe de resposta a incidentes cria um post-mortem que descreve os detalhes do incidente com a intenção de revisar políticas, procedimentos e processos para evitar a recorrência do evento. |

Os processos de detecção usados pelo serviço de processador de dados da Microsoft para o Windows Enterprise são projetados para descobrir eventos que arriscam a confidencialidade, integridade e disponibilidade do serviço de processador de dados do Windows Enterprise. Vários eventos podem desencadear uma investigação:

- Alertas automatizados do sistema por meio de estruturas internas de monitoramento e alertas. Esses alertas podem vir na forma de alarmes baseados em assinatura, como antimalware, detecção de intrusão ou por meio de algoritmos projetados para analisar a atividade esperada e alertar sobre anomalias.
- Relatórios internos dos Serviços da Microsoft em execução no Microsoft Azure e no Azure Governamental.
- As vulnerabilidades de segurança são notificadas ao [Microsoft Security Response Center (MSRC)](https://technet.microsoft.com/security/dn440717) pelo email [secure@microsoft.com] (mailto:secure@microsoft.com). O MSRC trabalha com parceiros e pesquisadores de segurança do mundo inteiro para ajudar a impedir incidentes de segurança e aprimorar a segurança dos produtos da Microsoft.
- Relatórios de cliente via Portal de Suporte ao Cliente ou via Portal de Gerenciamento do Azure Governamental ou do Microsoft Azure, que descrevem as atividades suspeitas atribuídas à infraestrutura do Azure (em vez das atividades que ocorrem dentro do escopo de responsabilidade do cliente).
- Atividade de segurança da [Equipe Azul e da Equipe Vermelha](https://azure.microsoft.com/blog/red-teaming-using-cutting-edge-threat-simulation-to-harden-the-microsoft-enterprise-cloud/). Essa estratégia usa uma equipe Vermelha ofensiva, da Microsoft, altamente especializada em segurança para descobrir e atacar possíveis falhas no Azure. A equipe Azul de resposta de segurança deve detectar e se defender das atividades da equipe Vermelha. As ações tanto da Equipe Vermelha quanto da Equipe Azul são usadas para verificar se os esforços de resposta de segurança do Azure estão gerenciando com eficiência os incidentes de segurança. As atividades de segurança da Equipe Vermelha e da Equipe Azul são operadas de acordo com as regras de envolvimento para ajudar a garantir a proteção dos dados do cliente.
- Escalonamentos por operadores de Serviços do Azure. Os funcionários da Microsoft fazem treinamentos para identificar e escalonar possíveis problemas de segurança.

## <a name="data-processor-service-for-windows-enterprise-data-breach-response"></a>Serviço de processador de dados para a resposta da violação de dados do Windows Enterprise

 A Microsoft atribui a investigação os níveis de prioridade e severidade apropriados determinando o impacto funcional, a capacidade de recuperação e o impacto das informações do incidente. A prioridade e a gravidade podem mudar ao longo da investigação, com base em novas conclusões. Eventos de segurança que envolvem riscos iminentes ou confirmados para os dados do cliente são tratados como alta severidade e funcionam 24 horas por dia até a resolução. O serviço de processador de dados da Microsoft para Windows Enterprise categoriza o impacto das informações do incidente nas seguintes categorias de violação:

| _ *Categoria** | **Definição** |
|:------------ |:-------------- |
| **_Nenhum_* _ | Nenhuma informação foi removida, alterada, apagada ou de outra forma comprometida. |
| _*_Violação de Privacidade_*_ | Dados pessoais confidenciais de contribuintes, funcionários, beneficiários, etc., foram acessados ou removidos. |
| _*_Violação de Propriedade_*_ | Informações proprietárias não-classificadas, tais como informações de infra-estrutura crítica protegida (PCII), foram acessadas ou removidas. |
| _*_Perda de integridade_*_ | Informações confidenciais ou proprietárias foram alteradas ou excluídas. |

A Equipe de Resposta de Segurança trabalha com o serviço de processador de dados da Microsoft para SMEs e engenheiros de segurança do Windows Enterprise para classificar o evento com base em dados reais da evidência. Um evento de segurança pode ser classificado como:

- _*Falso positivo**: Um evento que atende aos critérios de detecção, mas que é considerado parte de uma prática de negócios normal e pode precisar ser filtrado. A equipe de serviço identificará a causa raiz de falsos positivos e os abordará de maneira sistemática usando fontes de detecção e ajustando-as conforme necessário.
- **Incidente de Segurança**: Um incidente em que houve acesso criminoso aos Dados do Cliente ou Dados de Suporte armazenados em equipamentos ou instalações da Microsoft, ou acesso não autorizado a tais equipamentos ou instalações resultando na perda, divulgação ou alteração dos Dados do Cliente ou Dados de Suporte.
- **Incidente de Segurança Relatável para o Cliente (CRSI)**: um acesso ilegal ou não autorizado ou uso não autorizado dos sistemas, equipamentos ou instalações da Microsoft que resultem em divulgação, modificação ou perda de dados do cliente.
- **Violação de privacidade**: Um subtipo de Incidente de Segurança que envolve dados pessoais. Os procedimentos de tratamento não são diferentes de um incidente de segurança.

 Para que um CRSI seja declarado, a Microsoft deve determinar que o acesso não autorizado aos dados do cliente ocorreu ou provavelmente ocorreu e/ou que existe um compromisso legal ou contratual de que a notificação deve ocorrer. É desejável, mas não obrigatório, que sejam conhecidos o impacto específico no cliente, o acesso a recursos e as etapas de reparo. Um incidente é geralmente declarado um CRSI após a conclusão da etapa de Diagnóstico de um incidente de segurança; entretanto, a declaração pode acontecer a qualquer momento em que todas as informações pertinentes estejam disponíveis. O gerente de incidente de segurança deve estabelecer evidências além de qualquer dúvida razoável de que um evento relatável ocorreu para iniciar a execução do Processo de Notificação de Incidente do Cliente.

Durante a investigação, a equipe de resposta de segurança trabalha em estreita colaboração com consultores jurídicos globais para ajudar a garantir que a perícia seja realizada de acordo com as obrigações legais e compromissos com os clientes. Existem também restrições significativas na visualização e manipulação de dados do sistema e do cliente em vários ambientes operacionais. Os dados sensíveis ou confidenciais e os Dados do cliente não são transferidos para fora do ambiente de produção sem a aprovação explícita por escrito do Gerente de Incidentes registrado no ticket de incidente correspondente.

A Microsoft confirma que o risco à empresa e ao cliente foi suprimido com êxito e que foram implementadas medidas corretivas. Se necessário, realizam-se etapas de atenuação emergenciais para resolver riscos de segurança imediatos associados ao evento.

A Microsoft também conclui um post-mortem interno para violações de dados. Como parte deste exercício, a suficiência de procedimentos operacionais e de resposta são avaliadas e todas as atualizações que podem ser necessárias para o SOP de Resposta a Incidentes de Segurança ou processos relacionados são identificadas e implementadas. Os erros internos para violações de dados são registros altamente confidenciais que não estão disponíveis para os clientes. No entanto, as palavras-chave podem ser resumidas e incluídas em outras notificações de eventos do cliente. Esses relatórios são fornecidos a auditores externos para revisão como parte do ciclo de auditoria de rotina do serviço de processador de dados do Windows Enterprise.

## <a name="customer-notice"></a>Notificação ao cliente

O serviço de processador de dados da Microsoft para Windows Enterprise notifica clientes e autoridades regulatórias sobre violações de dados conforme necessário. A Microsoft depende de compartimentalização interna pesada na operação do serviço de processador de dados para o Windows Enterprise. Os logs de fluxo de dados também são robustos. Como benefício desse design, a maioria dos incidentes pode ser delimitado a clientes específicos. O objetivo é fornecer aos clientes afetados um aviso preciso, acionável e em tempo hábil quando seus dados forem violados.

Após a declaração de um CRSI, o processo de notificação ocorrerá da forma mais eficiente possível, levando em conta os riscos de segurança de um trabalho agilizado. Em geral, o processo de criação de notificações ocorre durante o andamento da investigação do incidente. As notificações ao cliente são realizadas dentro de 72 horas após declararmos uma violação, exceto nas seguintes circunstâncias:

- A Microsoft acredita que a notificação aumentará o risco para outros clientes. Por exemplo, após uma notificação, um adversário pode ficar sabendo de informações que utilizará para impossibilitar a correção.
- Outras circunstâncias extremas ou incomuns investigadas pelo departamento jurídico da Microsoft, o Corporate External and Legal Affairs (CELA) e pelo Gerente de Incidentes Executivo.

 O serviço de processador de dados da Microsoft para Windows Empresa fornece aos clientes informações detalhadas, permitindo-lhes realizar investigações internas e auxiliá-los a cumprir os compromissos do usuário final, sem atrasar indevidamente o processo de notificação.

A notificação de uma violação de dados pessoal será enviada ao cliente por qualquer meio que a Microsoft selecionar, incluindo via email. A notificação de violação de dados será entregue à lista de contatos de segurança fornecida na Central de Segurança do Azure, que pode ser configurada seguindo as[diretrizes de implementação](/azure/security-center/security-center-provide-security-contact-details). Se as informações de contato não forem fornecidas na Central de Segurança do Azure, a notificação é enviada para um ou mais administradores em uma assinatura do Azure. Para garantir que as notificações possam ser entregues com êxito, é responsabilidade do cliente garantir que as informações de contato administrativas em cada assinatura aplicável e o portal de serviços online estejam corretas.

O serviço de processador de dados para a equipe do Windows Enterprise também pode optar por notificar funcionários adicionais da Microsoft, como o Serviço de Atendimento ao Consumidor (SAC) e o(s) Gerente(s) de Conta do Cliente (GCC) ou Gerente(s) Técnico(s) de Conta (GTC) do cliente. Esses indivíduos geralmente têm relacionamentos próximos com o cliente e podem facilitar a correção mais rápida.

Para obter mais informações sobre como a Microsoft detecta e responde a uma violação de dados pessoais, confira [Notificação de violação de dados no RGPD](https://servicetrust.microsoft.com/ViewPage/GDPRBreach) no Portal de Confiança do Serviço.
