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
ms.openlocfilehash: 41e903a478559d942de2202ab89e05c8c46a8460
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51496338"
---
# <a name="data-processor-service-for-windows-enterprise-breach-notification-under-the-gdpr"></a>Serviço de processamento de dados da notificação de violação do Windows Enterprise sob o GDPR

>[!NOTE]
>Este tópico é destinado aos participantes do serviço de processador de dados do programa de visualização prévia do Windows Enterprise e requer a aceitação de termos de uso específicos. Para saber mais sobre o programa e concordar com os termos de uso, acesse [https://aka.ms/WindowsEnterprisePublicPreview](https://aka.ms/WindowsEnterprisePublicPreview).

O serviço do processador de dados da Microsoft para o Windows Enterprise leva a sério as suas obrigações nos termos do Regulamento Geral de Proteção de Dados (GDPR). O serviço de processador de dados da Microsoft para o Windows Enterprise toma extensas medidas de segurança para proteger contra violações de dados. Essas medidas incluem equipes dedicadas de gerenciamento de ameaças que atuam proativamente para prever, impedir e atenuar acessos mal-intencionados.Medidas de segurança interna como a verificação de portas, verificação de vulnerabilidades de perímetro e detecção de invasores detectam e impedem acessos mal-intencionados, além de processos de segurança automatizados, políticas abrangentes de privacidade e segurança da informação e treinamento de segurança e privacidade para todo o pessoal. 

A segurança está incorporada no serviço de processador de dados da Microsoft para o Windows Enterprise desde o início, começando com o [Ciclo de Vida de Desenvolvimento de Segurança](https://www.microsoft.com/sdl/), um processo de desenvolvimento obrigatório que incorpora metodologias de privacidade por projeto e privacidade por defeito. O princípio orientador da estratégia de segurança da Microsoft é “presumir a violação”, uma extensão da estratégia de defesa em profundidade. Ao desafiar constantemente os recursos de segurança do serviço de processador de dados do Windows Enterprise, a Microsoft pode ficar à frente das ameaças emergentes. Para obter mais informações do serviço de processador de dados para a segurança do Windows Enterprise, reveja estes [recursos](https://www.microsoft.com/TrustCenter/Security/windows10-security), o serviço de processador de dados do Windows Enterprise responde a uma possível violação de dados de acordo com o processo de resposta a incidentes de segurança. A resposta a incidentes de segurança do serviço de processador de dados do Windows é implementada por um processo em cinco etapas: Detecção, Avaliação, Diagnóstico, Estabilização e Fechamento. A equipe de Resposta a Incidentes de Segurança pode alternar entre as etapas Diagnóstico e Estabilização à medida que a investigação progride. Abaixo um resumo do processo de resposta a incidentes de segurança: 

|**Stage**|**Descrição**|
|:------- |:------------- |
| ***1: Detectar*** | Primeira indicação de um possível incidente. |
| ***2: Avaliar*** | Um membro de plantão da equipe de resposta a incidentes avalia o impacto e a gravidade do evento. Com base em evidências, a avaliação pode ou não resultar num escalonamento para a equipe de resposta de segurança. |
| ***3: Diagnosticar*** | Os especialistas em resposta de segurança realizam a investigação técnica ou forense, identificam estratégias de confinamento, de atenuação e de solução alternativa. Se a equipe de segurança achar que os dados do cliente podem ter sido expostos a um indivíduo criminoso ou não autorizado, a execução do processo de notificação de incidente do cliente começa em paralelo. |
| ***4: Estabilizar e Recuperar*** | A equipe de resposta a incidentes cria um plano de recuperação para atenuar o problema. As etapas de contenção de crise, como colocar em quarentena os sistemas afetados, podem ocorrer imediatamente e em paralelo com o diagnóstico. As atenuações de longo prazo podem ser planejadas, e ocorrer após o risco imediato ter passado. |
| ***5: Fechamento e Post-mortem*** | A equipe de resposta a incidentes cria um post-mortem que descreve os detalhes do incidente com a intenção de revisar políticas, procedimentos e processos para evitar a recorrência do evento. |

Os processos de detecção usados pelo serviço de processador de dados da Microsoft para o Windows Enterprise são projetados para descobrir eventos que arriscam a confidencialidade, integridade e disponibilidade do serviço de processador de dados do Windows Enterprise. Vários eventos podem desencadear uma investigação:

- Alertas de sistema automatizados por monitoramento interno e estruturas de alerta. Esses alertas podem vir na forma de alarmes baseados em assinatura, como anti-malware, detecção de invasão ou via algoritmos projetados para analisar a atividade esperada e alertar sobre anomalias.
- Relatórios internos dos Serviços da Microsoft em execução no Microsoft Azure e no Azure Governamental.
- As vulnerabilidades de segurança são notificadas ao [Microsoft Security Response Center (MSRC)](https://technet.microsoft.com/security/dn440717) pelo email [secure@microsoft.com] (mailto:secure@microsoft.com). O MSRC trabalha com parceiros e pesquisadores de segurança do mundo inteiro para ajudar a impedir incidentes de segurança e aprimorar a segurança dos produtos da Microsoft.
- Relatórios de cliente via Portal de Suporte ao Cliente ou via Portal de Gerenciamento do Azure Governamental ou do Microsoft Azure, que descrevem as atividades suspeitas atribuídas à infraestrutura do Azure (em vez das atividades que ocorrem dentro do escopo de responsabilidade do cliente).
- Atividade de segurança da [Equipe Azul e da Equipe Vermelha](https://azure.microsoft.com/blog/red-teaming-using-cutting-edge-threat-simulation-to-harden-the-microsoft-enterprise-cloud/). Essa estratégia usa uma equipe Vermelha ofensiva, da Microsoft, altamente especializada em segurança para descobrir e atacar possíveis falhas no Azure. A equipe Azul de resposta de segurança deve detectar e se defender das atividades da equipe Vermelha. As ações tanto da Equipe Vermelha quanto da Equipe Azul são usadas para verificar se os esforços de resposta de segurança do Azure estão gerenciando com eficiência os incidentes de segurança. As atividades de segurança da Equipe Vermelha e da Equipe Azul são operadas de acordo com as regras de envolvimento para ajudar a garantir a proteção dos dados do cliente.
- Escalonamento por operadores de Serviços do Azure. Os funcionários da Microsoft são treinados para identificar e escalonar possíveis problemas de segurança.

## <a name="data-processor-service-for-windows-enterprise-data-breach-response"></a>Serviço de processador de dados para a resposta da violação de dados do Windows Enterprise

 A Microsoft atribui a prioridade adequada e os níveis de gravidade ao determinar o impacto funcional, a capacidade de recuperação e o impacto das informações do incidente. A prioridade e a severidade podem mudar durante a investigação, com base nas novas descobertas e conclusões. Os eventos de segurança que envolvem riscos iminentes ou confirmados para os dados dos clientes são tratados como de alta gravidade e trabalham o tempo todo até a resolução. O serviço de processador de dados da Microsoft para o Windows Enterprise categoriza o impacto nas informações do incidente nas seguintes categorias de violação:

| **Categoria** | **Definição** |
|:------------ |:-------------- |
| ***Nenhum*** | Nenhuma informação foi removida, alterada, apagada ou de outra forma comprometida. |
| ***Violação de privacidade*** | Dados pessoais confidenciais de contribuintes, funcionários, beneficiários, etc., foram acessados ou removidos. |
| ***Violação proprietária*** | Informações proprietárias não-classificadas, tais como informações de infra-estrutura crítica protegida (PCII), foram acessadas ou removidas. |
| ***Perda de integridade*** | Informações confidenciais ou proprietárias foram alteradas ou excluídas. |

A equipe de Resposta de segurança trabalha com os Engenheiros de segurança e especialistas no assunto (SMEs) do serviço de processador de dados Windows do Microsoft Enterprise para classificar o evento com base em dados concretos das evidências. Um evento de segurança pode ser classificado como:

- **Falso Positivo**: Um evento que atende aos critérios de detecção, mas que é considerado como parte de uma prática empresarial normal e talvez precise ser filtrado. A equipe de serviço identificará a causa raiz dos falsos positivos e os tratará de forma sistemática usando fontes de detecção e ajustando-as conforme necessário.
- **Incidente de Segurança**: Um incidente em que houve acesso criminoso aos Dados do Cliente ou Dados de Suporte armazenados em equipamentos ou instalações da Microsoft, ou acesso não autorizado a tais equipamentos ou instalações resultando na perda, divulgação ou alteração dos Dados do Cliente ou Dados de Suporte.
- **Incidente de Segurança Relatável para o Cliente (CRSI)**: um acesso ilegal ou não autorizado ou uso não autorizado dos sistemas, equipamentos ou instalações da Microsoft que resultem em divulgação, modificação ou perda de dados do cliente.
- **Violação de Privacidade**: Um subtipo de Incidente de Segurança que envolve dados pessoais. Manipular procedimentos não é diferente de um incidente de segurança.

 Para que um CRSI seja declarado, a Microsoft deve determinar que o acesso não autorizado aos dados do cliente ocorreu ou provavelmente ocorreu e/ou que existe um compromisso legal ou contratual de que a notificação deve ocorrer. É desejável, mas não obrigatório, que sejam conhecidos o impacto específico no cliente, o acesso a recursos e as etapas de reparo. Um incidente é geralmente declarado um CRSI após a conclusão da etapa de Diagnóstico de um incidente de segurança; entretanto, a declaração pode acontecer a qualquer momento em que todas as informações pertinentes estejam disponíveis. O gerente de incidente de segurança deve estabelecer evidências além de qualquer dúvida razoável de que um evento relatável ocorreu para iniciar a execução do Processo de Notificação de Incidente do Cliente.

Durante a investigação, a equipe de resposta de segurança trabalha em estreita colaboração com consultores jurídicos globais para ajudar a garantir que a perícia seja realizada de acordo com as obrigações legais e compromissos com os clientes. Existem também restrições significativas na visualização e manipulação de dados do sistema e do cliente em vários ambientes operacionais. Os dados sensíveis ou confidenciais e os Dados do cliente não são transferidos para fora do ambiente de produção sem a aprovação explícita por escrito do Gerente de Incidentes registrado no ticket de incidente correspondente.

A Microsoft confirma que o risco à empresa e ao cliente foi suprimido com êxito e que foram implementadas medidas corretivas. Se necessário, realizam-se etapas de atenuação emergenciais para resolver riscos de segurança imediatos associados ao evento.

A Microsoft também concluiu um post-mortem interno para violações de dados. Como parte deste exercício, a suficiência de respostas e os procedimentos operacionais são avaliados e todas as atualizações que possam ser necessárias para o SOP de Resposta a Incidentes de Segurança ou processos relacionados são identificados e implementados. Os postmortems internos para violações de dados são registros altamente confidenciais que não estão disponíveis para os clientes. No entanto, postmortems podem ser resumidos e incluídos nas notificações de evento de outro cliente. Esses relatórios são fornecidos aos auditores externos para revisão como parte do serviço de processador de dados do ciclo de auditoria de rotina do Windows Enterprise.

## <a name="customer-notice"></a>Notificação ao cliente

O serviço de processador de dados da Microsoft para o Enterprise notifica os clientes e as autoridades reguladoras sobre violações de dados, conforme necessário. A Microsoft conta com forte compartimentação interna na operação do serviço de processador de dados do Windows Enterprise. Os logs do fluxo de dados também são consistentes. Uma vantagem desse design é que a maioria dos incidentes pode ser filtrada por um escopo para clientes específicos. O objetivo é notificar os clientes afetados de forma precisa, acionável e em tempo hábil quando seus dados forem violados.

Após a declaração de um CRSPI, o processo de notificação ocorre o mais rapidamente possível, sem deixar de levar em conta os riscos de segurança de uma movimentação muito rápida. Geralmente, o processo de elaboração das notificações ocorre enquanto a investigação do incidente está em andamento. As notificações aos clientes são entregues no mais tardar 72 horas após a declaração de uma violação, com exceção das seguintes situações:

- A Microsoft acredita que a notificação aumentará o risco para outros clientes. Por exemplo, após uma notificação, um adversário pode ficar sabendo de informações que utilizará para impossibilitar a correção.
- Outras circunstâncias extremas ou incomuns investigadas pelo departamento jurídico da Microsoft, o Corporate External and Legal Affairs (CELA) e pelo Gerente de Incidentes Executivo.

 O serviço de processador de dados da Microsoft para Windows Empresa fornece aos clientes informações detalhadas, permitindo-lhes realizar investigações internas e auxiliá-los a cumprir os compromissos do usuário final, sem atrasar indevidamente o processo de notificação.

A notificação de uma violação de dados pessoal será enviada ao cliente por qualquer meio que a Microsoft selecionar, incluindo via email. A notificação de violação de dados será entregue à lista de contatos de segurança fornecida na Central de Segurança do Azure, que pode ser configurada seguindo as[diretrizes de implementação](/azure/security-center/security-center-provide-security-contact-details). Se as informações de contato não forem fornecidas na Central de Segurança do Azure, a notificação é enviada para um ou mais administradores em uma assinatura do Azure. Para garantir que as notificações possam ser entregues com êxito, é responsabilidade do cliente garantir que as informações de contato administrativas em cada assinatura aplicável e o portal de serviços online estejam corretas.

A equipe do serviço de processador de dados do Windows Enterprise também pode optar por notificar outras equipes da Microsoft, como o Atendimento ao cliente (CSS) e os Gerentes de contas (AM) ou Gerentes Técnicos da Conta (TAM) do cliente. Esses indivíduos geralmente têm um relacionamento próximo com o cliente e podem facilitar uma correção mais rápida.

Para obter mais informações sobre como a Microsoft detecta e responde a uma violação de dados pessoais, confira [Notificação de violação de dados no RGPD](https://servicetrust.microsoft.com/ViewPage/GDPRBreach) no Portal de Confiança do Serviço.
