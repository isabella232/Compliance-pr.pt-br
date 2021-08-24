---
title: Notificação de violação do Azure, Dynamics 365 e Windows no GDPR
description: Como o Azure e o Dynamics 365 protegem contra a violação de dados pessoais e como a Microsoft responderá e notificará se ocorrer uma violação.
keywords: Azure, Microsoft 365, Dynamics 365, documentação da Microsoft 365, GDPR
ms.localizationpriority: high
ms.prod: microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmazz
manager: laurawi
audience: itpro
ms.collection:
- GDPR
- M365-security-compliance
- MS-Compliance
titleSuffix: Microsoft GDPR
hideEdit: true
ms.openlocfilehash: 23d6b1ebb30f34fcb549e3e1f44c98a0c0e11b12
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2021
ms.locfileid: "58479803"
---
# <a name="azure-dynamics-365-and-windows-breach-notification-under-the-gdpr"></a>Notificação de violação do Azure, Dynamics 365 e Windows no GDPR

A Microsoft leva a sério suas obrigações de acordo com o Regulamento Geral sobre a Proteção de Dados (GDPR). A Microsoft adota medidas de segurança abrangentes em seus serviços online para se proteger contra violações de dados. Essas medidas incluem controles de segurança físicos e lógicos, bem como processos de segurança automatizados, políticas de privacidade e segurança de informações abrangentes e treinamento de segurança e privacidade para todo o pessoal.

A segurança é integrada ao Microsoft Azure do zero, começando com o [Microsoft Security Development Lifecycle](https://www.microsoft.com/sdl/), um processo de desenvolvimento obrigatório que incorpora metodologias de privacidade por design e privacidade por padrão. O princípio orientador da estratégia de segurança da Microsoft é 'presumir violação', que é uma extensão da estratégia de defesa em profundidade. Ao desafiar constantemente os recursos de segurança do Azure, a Microsoft pode ficar à frente das ameaças emergentes. Para obter mais informações sobre a segurança do Azure, analise esses [recursos](https://www.microsoft.com/trustcenter/security/azure-security).

A Microsoft tem um serviço global dedicado de resposta a incidentes 24 horas por dia, 7 dias por semana, que trabalha para mitigar os efeitos dos ataques contra o Microsoft Azure. Atestada por várias auditorias de segurança e conformidade (por exemplo, [ISO/IEC 27018](offering-iso-27018.md)), a Microsoft emprega operações e processos rigorosos em seus data centers para evitar o acesso não autorizado, incluindo monitoramento de vídeo 24 horas por dia, 7 dias por semana, pessoal de segurança treinado, cartões inteligentes e controles biométricos.

## <a name="detection-of-potential-breaches"></a>Detecção de possíveis violações

Devido à natureza da computação em nuvem moderna, nem todas as violações de dados que ocorrem em um ambiente de nuvem do cliente envolvem serviços do Microsoft Azure. A Microsoft emprega um modelo de responsabilidade compartilhada para serviços do Azure para definir segurança e responsabilidades operacionais. A responsabilidade compartilhada é importante ao discutir a segurança de um serviço em nuvem, porque tanto o provedor de serviços em nuvem quanto o cliente são responsáveis por partes da segurança em nuvem.

A Microsoft não monitora ou responde a incidentes de segurança dentro da esfera de responsabilidade do cliente. Um comprometimento de segurança exclusivo do cliente não seria processado como um incidente de segurança do Azure e exigiria que o locatário do cliente gerencie o esforço de resposta. A resposta a incidentes do cliente pode envolver a colaboração com o [suporte ao cliente](https://azure.microsoft.com/support/options/) do Microsoft Azure, mediante contratos de serviço apropriados. O Microsoft Azure também oferece vários serviços (por exemplo, [Central de Segurança do Azure](https://azure.microsoft.com/services/security-center/)) que os clientes podem utilizar para desenvolver e gerenciar a resposta a incidentes de segurança.

O Azure responde a uma possível violação de dados de acordo com o processo de resposta a incidentes de segurança, que é um subconjunto do plano de gerenciamento de incidentes do Microsoft Azure. A resposta a incidentes de segurança do Azure da Microsoft é implementada usando um processo de cinco estágios: Detectar, Avaliar, Diagnosticar, Estabilizar e Fechar. A equipe de resposta a incidentes de segurança pode alternar entre os estágios de diagnóstico e estabilização conforme o andamento da investigação. Uma visão geral do processo de resposta a incidentes de segurança está abaixo:

| Etapa | Descrição |
|:------- |------------- |
| ***1: Detectar*** | Primeira indício de um possível incidente. |
| ***2: Avaliar*** | Um membro de plantão da equipe de resposta a incidentes avalia o impacto e a gravidade do evento. Com base em evidências, a avaliação pode ou não resultar num escalonamento à equipe de resposta de segurança. |
| ***3: Diagnosticar*** | Os especialistas em resposta de segurança realizam a investigação técnica ou forense, identificam estratégias de contenção, mitigação e solução alternativa. Se a equipe de segurança achar que os dados do cliente podem ter sido expostos a um indivíduo criminoso ou não autorizado, a execução do processo de Notificação de Incidente do Cliente começa em paralelo. |
| ***4: Estabilizar e Recuperar*** | A equipe de resposta a incidentes cria um plano de recuperação para atenuar o problema. As etapas de contenção de crise, como colocar em quarentena os sistemas afetados, podem ocorrer imediatamente e em paralelo com o diagnóstico. As atenuações de longo prazo podem ser planejadas, e ocorrer após o risco imediato ter passado. |
| ***5: Fechamento e Post-mortem*** | A equipe de resposta a incidentes cria um post-mortem que descreve os detalhes do incidente com a intenção de revisar políticas, procedimentos e processos para evitar a recorrência do evento. |

Os processos de detecção usados pelo Microsoft Azure foram projetados para detectar eventos que põem em risco a confidencialidade, a integridade e a disponibilidade dos serviços do Azure. Vários eventos podem provocar o início de uma investigação:

- Alertas automatizados do sistema por meio de estruturas internas de monitoramento e alertas. Esses alertas podem vir na forma de alarmes baseados em assinatura, como antimalware, detecção de intrusão ou por meio de algoritmos projetados para analisar a atividade esperada e alertar sobre anomalias.
- Relatórios internos dos Serviços da Microsoft em execução no Microsoft Azure e no Azure Governamental.
- As vulnerabilidades de segurança são relatadas ao [Microsoft Security Response Center (MSRC)](https://www.microsoft.com/msrc) por meio de [Relatar um problema](https://msrc.microsoft.com/create-report). O MSRC trabalha com parceiros e pesquisadores de segurança do mundo inteiro para ajudar a impedir incidentes de segurança e aprimorar a segurança dos produtos da Microsoft.
- Relatórios de cliente via [Portal de suporte ao cliente](https://www.windowsazure.com/support/contact/) ou via Portal de Gerenciamento do Azure Governamental ou do Microsoft Azure, que descrevem as atividades suspeitas atribuídas à infraestrutura do Azure (em vez das atividades que ocorrem dentro do escopo de responsabilidade do cliente).
- Atividade de segurança da [Equipe Azul e da Equipe Vermelha](https://azure.microsoft.com/blog/red-teaming-using-cutting-edge-threat-simulation-to-harden-the-microsoft-enterprise-cloud/). Essa estratégia usa uma equipe Vermelha ofensiva, da Microsoft, altamente especializada em segurança para descobrir e atacar possíveis falhas no Azure. A equipe Azul de resposta de segurança deve detectar e se defender das atividades da equipe Vermelha. As ações tanto da Equipe Vermelha quanto da Equipe Azul são usadas para verificar se os esforços de resposta de segurança do Azure estão gerenciando com eficiência os incidentes de segurança. As atividades de segurança da Equipe Vermelha e da Equipe Azul são operadas de acordo com as regras de envolvimento para ajudar a garantir a proteção dos dados do cliente.
- Escalonamentos por operadores de Serviços do Azure. Os funcionários da Microsoft fazem treinamentos para identificar e escalonar possíveis problemas de segurança.

## <a name="azures-data-breach-response"></a>Resposta à violação de dados do Azure

A Microsoft atribui à investigação os níveis de prioridade e gravidade apropriados, determinando o impacto funcional, a capacidade de recuperação e o impacto das informações do incidente. Tanto a prioridade quanto a gravidade podem alterar no decorrer da investigação, com base em novos achados e conclusões. Os eventos de segurança que envolvem risco iminente ou confirmado para os dados do cliente são tratados como de alta gravidade e trabalhados continuamente para resolução.

A equipe de resposta de segurança trabalha com os engenheiros de segurança do Microsoft Azure e Especialistas no Assunto (EAs) para classificar o evento com base em dados concretos das evidências. Um evento de segurança pode ser classificado como:

- **Falso Positivo**: um evento que atende aos critérios de detecção, mas é considerado parte de uma prática comercial normal e pode precisar ser filtrado. As equipes de serviço identificarão a causa raiz dos falsos positivos e os abordarão de forma sistemática para ajustá-los conforme necessário.
- **Evento de Segurança**: uma ocorrência observável em um sistema, serviço e/ou rede para tentativa de ataque, evasão de controles de segurança ou um problema identificado onde os fatos indicam que os dados do cliente ou dados pessoais podem ter sido perdidos, destruídos, alterados, divulgados, ou acessado sem autorização.
- **Incidente de Segurança/Incidente de segurança/privacidade relatável pelo cliente (CRSPI)**: uma violação de segurança confirmada (por exemplo, declarada) que leva à destruição acidental ou ilegal, perda, alteração, divulgação não autorizada ou acesso aos Dados do Cliente ou Dados Pessoais durante o processamento pela Microsoft.
- **Evento de Privacidade**: um Evento de Segurança que afeta os Dados Pessoais ou o processamento de dados que resulta em consequências indesejadas para a privacidade, incluindo a não conformidade com as políticas, padrões e controles de privacidade da Microsoft.
- **Incidente de Privacidade/Incidente de Privacidade/Segurança Reportável pelo Cliente (CRSPI)**: um incidente de segurança que afeta Dados pessoais, Dados ou processamento de dados que resulta em consequências indesejadas para a privacidade, incluindo não conformidade com as políticas, padrões e controles de privacidade da Microsoft.

Para que um CRSPI seja declarado, a Microsoft deve determinar que o acesso não autorizado aos dados do cliente ocorreu ou provavelmente ocorreu ou que existe um compromisso legal ou contratual de que a notificação deve ocorrer. É desejável, mas não obrigatório, que sejam conhecidos o impacto específico no cliente, o acesso a recursos e as etapas de reparo. Um incidente é geralmente declarado um CRSPI após a conclusão do estágio de Diagnóstico de um incidente de segurança. No entanto, a declaração pode acontecer a qualquer momento em que todas as informações pertinentes estejam disponíveis.

A Microsoft confirma que o risco à empresa e ao cliente foi suprimido com êxito e que foram implementadas medidas corretivas. Se necessário, realizam-se etapas de atenuação emergenciais para resolver riscos de segurança imediatos associados ao evento.

A Microsoft também conclui uma autópsia interna para violações de dados. Como parte deste exercício, a suficiência da resposta e dos procedimentos operacionais são avaliados, e quaisquer atualizações que possam ser necessárias ao SOP de Réplica a Incidentes de Segurança ou processos relacionados são identificadas e implementadas. As autópsias internas para violações de dados são registros altamente confidenciais não disponíveis para os clientes. No entanto, as autópsias podem ser resumidas e incluídas em outras notificações de eventos do cliente. Esses relatórios são fornecidos a auditores externos para revisão como parte do ciclo de auditoria de rotina do Azure.

## <a name="customer-notification"></a>Notificação de cliente

A Microsoft notifica os clientes afetados e as autoridades regulatórias sobre violações de dados, conforme necessário. A Microsoft depende de uma forte compartimentação interna na operação do Azure. Os registros de fluxo de dados também são robustos. Como benefício desse design, a maioria dos incidentes pode ter como escopo clientes específicos. O objetivo é fornecer aos clientes afetados um aviso preciso, acionável e oportuno quando seus dados forem violados.

Após a declaração de um CRSPI, o processo de notificação ocorrerá o mais rapidamente possível, considerando os riscos de segurança da mudança rápida. Geralmente, o processo de redação das notificações acontece quando a investigação do incidente está em andamento. As notificações dos clientes são entregues em até 72 horas a partir do momento em que declaramos uma violação *exceto* nas seguintes circunstâncias:

- A Microsoft acredita que o ato de executar uma notificação aumenta o risco para outros clientes. Por exemplo, o ato de notificar pode alertar um adversário, causando uma incapacidade de corrigir.
- Outras circunstâncias incomuns ou extremas examinadas pelo departamento jurídico da Microsoft e pelo Gerente Executivo de Incidentes.
- O cronograma de 72 horas pode deixar alguns detalhes do incidente disponíveis. Esses detalhes são fornecidos aos clientes e autoridades regulatórias à medida que a investigação avança.

A Microsoft fornece aos clientes afetados informações detalhadas, permitindo-lhes realizar investigações internas e ajudá-los a cumprir os compromissos do usuário final, sem atrasar indevidamente o processo de notificação.

A notificação de uma violação de dados pessoais será entregue ao cliente afetado por qualquer meio que a Microsoft selecionar, incluindo por email. A notificação de uma violação de dados será entregue à lista de contatos de segurança fornecida na Central de Segurança do Azure, que pode ser configurada seguindo as [diretrizes de implementação](/azure/security-center/security-center-provide-security-contact-details). Se as informações de contato não forem fornecidas na Central de Segurança do Azure, a notificação é enviada para um ou mais administradores em uma assinatura do Azure. Para garantir que as notificações possam ser entregues com êxito, é responsabilidade do cliente garantir que as informações de contato administrativas em cada assinatura aplicável e o portal de serviços online estejam corretas.

A equipe do Microsoft Azure ou do Azure Governamental também pode optar por notificar outro pessoal da Microsoft, como membros da equipe do Serviço de Suporte ao Cliente (CSS) da Microsoft e o(s) Gerente(s) de Conta (AM) ou Gerente(es) Técnico(s) de Conta (TAM) do cliente. Esses indivíduos costumam ter relacionamentos próximos com o cliente e podem facilitar uma reparação mais rápida.

## <a name="microsoft-dynamics-365-built-in-security-features"></a>Recursos de segurança internos do Microsoft Dynamics 365

O Microsoft Dynamics 365 utiliza a infraestrutura de serviços na nuvem e os recursos de segurança internos para proteger dados usando medidas e mecanismos de segurança. Além disso, o Dynamics 365 fornece um acesso a dados eficiente e colaboração com privacidade e integridade de dados nas seguintes áreas: [identidade segura, proteção de dados, segurança baseada em função e gerenciamento de ameaças](https://www.microsoft.com/trustcenter/security/dynamics365-security).

A oferta do Microsoft Dynamics 365 segue as mesmas medidas técnicas e organizacionais que uma ou mais equipes de serviço do Microsoft Azure tomam para proteção contra processos de violação de dados. Portanto, qualquer informação documentada no documento de notificação 'Violação de dados do Microsoft Azure' aqui é análoga ao Microsoft Dynamics 365 também.

## <a name="windows-diagnostic-data-processor-configuration"></a>Configuração do processador de dados de diagnóstico do Windows

A [configuração do processador de dados de diagnóstico do Windows](/windows/privacy/configure-windows-diagnostic-data-in-your-organization) aproveita a infraestrutura do serviço em nuvem e os recursos de segurança integrados para manter os dados protegidos, usando medidas e mecanismos de segurança para proteger os dados.

Ele segue as mesmas medidas técnicas e organizacionais que uma ou mais equipes de serviço do Microsoft Azure tomam para proteção contra processos de violação de dados. Portanto, qualquer informação documentada no documento de notificação 'Violação de dados do Microsoft Azure' aqui é análoga à configuração do processador de dados de diagnóstico do Windows.

## <a name="learn-more"></a>Saiba mais

[Central de Confiabilidade da Microsoft](https://www.microsoft.com/trust-center/privacy/gdpr-overview)
