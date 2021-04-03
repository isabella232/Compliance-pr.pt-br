---
title: Notificação de Violação do Azure e do Dynamics 365 no GDPR
description: Como o Azure e o Dynamics 365 protegem contra a violação de dados pessoais e como a Microsoft responderá e notificará se ocorrer uma violação.
keywords: Azure, Microsoft 365, Dynamics 365, documentação da Microsoft 365, GDPR
localization_priority: Priority
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
ms.openlocfilehash: d969144880735224136db47282f620cfa985f939
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51496445"
---
# <a name="azure-and-dynamics-365-breach-notification-under-the-gdpr"></a>Notificação de Violação do Azure e do Dynamics 365 no GDPR

A Microsoft leva a sério suas obrigações de acordo com o Regulamento Geral sobre a Proteção de Dados (GDPR). A Microsoft adota medidas de segurança abrangentes em seus serviços online para se proteger contra violações de dados. Essas medidas incluem controles de segurança físicos e lógicos, bem como processos de segurança automatizados, políticas de privacidade e segurança de informações abrangentes e treinamento de segurança e privacidade para todo o pessoal.

A segurança é integrada ao Microsoft Azure do zero, começando com o [Microsoft Security Development Lifecycle](https://www.microsoft.com/sdl/), um processo de desenvolvimento obrigatório que incorpora metodologias de privacidade por design e privacidade por padrão. O princípio orientador da estratégia de segurança da Microsoft é 'presumir violação', que é uma extensão da estratégia de defesa em profundidade. Ao desafiar constantemente os recursos de segurança do Azure, a Microsoft pode ficar à frente das ameaças emergentes. Para obter mais informações sobre a segurança do Azure, analise esses [recursos](https://www.microsoft.com/trustcenter/security/azure-security).

A Microsoft tem um serviço global dedicado de resposta a incidentes 24 horas por dia, 7 dias por semana, que trabalha para mitigar os efeitos dos ataques contra o Microsoft Azure. Atestada por várias auditorias de segurança e conformidade (por exemplo, [ISO/IEC 27018](offering-iso-27018.md)), a Microsoft emprega operações e processos rigorosos em seus data centers para evitar o acesso não autorizado, incluindo monitoramento de vídeo 24 horas por dia, 7 dias por semana, pessoal de segurança treinado, cartões inteligentes e controles biométricos.

## <a name="detection-of-potential-breaches"></a>Detecção de possíveis violações

Devido à natureza da computação moderna em nuvem, nem todas as violações de dados ocorrem no ambiente de nuvem do cliente envolvemos os serviços do Microsoft Azure. A Microsoft emprega um modelo de responsabilidade compartilhado para os serviços do Azure para definir as responsabilidades operacionais e de segurança. A responsabilidade compartilhada é importante ao discutir a segurança de um serviço de nuvem, porque o provedor de serviços de nuvem e o cliente são responsáveis por partes da segurança na nuvem.

A Microsoft não monitora ou responde a incidentes de segurança dentro da esfera de responsabilidade do cliente. Um comprometimento de segurança exclusivo do cliente não seria processado como um incidente de segurança do Azure e exigiria que o locatário do cliente gerencie o esforço de resposta. A resposta a incidentes do cliente pode envolver a colaboração com o [suporte ao cliente](https://azure.microsoft.com/support/options/) do Microsoft Azure, mediante contratos de serviço apropriados. O Microsoft Azure também oferece vários serviços (por exemplo, [Central de Segurança do Azure](https://azure.microsoft.com/services/security-center/)) que os clientes podem utilizar para desenvolver e gerenciar a resposta a incidentes de segurança.

O Azure responde a uma possível violação de dados de acordo com o processo de resposta a incidentes de segurança, que é um subconjunto do plano de gerenciamento de incidentes do Microsoft Azure. A resposta a incidentes de segurança do Azure da Microsoft é implementada usando um processo de cinco estágios: Detectar, Avaliar, Diagnosticar, Estabilizar e Fechar. A equipe de resposta a incidentes de segurança pode alternar entre os estágios de diagnóstico e estabilização conforme o andamento da investigação. Uma visão geral do processo de resposta a incidentes de segurança está abaixo:

|**Stage**|**Descrição**|
|:------- |------------- |
| ***1: Detectar*** | Primeira indicação de um possível incidente. |
| ***2: Avaliar*** | Um membro de plantão da equipe de resposta a incidentes avalia o impacto e a gravidade do evento. Com base em evidências, a avaliação pode ou não resultar num escalonamento para a equipe de resposta de segurança. |
| ***3: Diagnosticar*** | Os especialistas em resposta de segurança realizam a investigação técnica ou forense, identificam estratégias de confinamento, de atenuação e de solução alternativa. Se a equipe de segurança achar que os dados do cliente podem ter sido expostos a um indivíduo criminoso ou não autorizado, a execução do processo de notificação de incidente do cliente começa em paralelo. |
| ***4: Estabilizar e Recuperar*** | A equipe de resposta a incidentes cria um plano de recuperação para atenuar o problema. As etapas de contenção de crise, como colocar em quarentena os sistemas afetados, podem ocorrer imediatamente e em paralelo com o diagnóstico. As atenuações de longo prazo podem ser planejadas, e ocorrer após o risco imediato ter passado. |
| ***5: Fechamento e Post-mortem*** | A equipe de resposta a incidentes cria um post-mortem que descreve os detalhes do incidente com a intenção de revisar políticas, procedimentos e processos para evitar a recorrência do evento. |

O [Azure para adoção segura da nuvem pelo setor público em todo o mundo](/azure/azure-government/documentation-government-overview-wwps#breach-notification-process) O tópico detalha como a Microsoft investiga, gerencia e responde a incidentes de segurança no Azure.

Os processos de detecção usados pelo Microsoft Azure foram projetados para detectar eventos que põem em risco a confidencialidade, a integridade e a disponibilidade dos serviços do Azure. Vários eventos podem provocar o início de uma investigação:

- Alertas de sistema automatizados por monitoramento interno e estruturas de alerta. Esses alertas podem vir na forma de alarmes baseados em assinatura, como anti-malware, detecção de invasão ou via algoritmos projetados para analisar a atividade esperada e alertar sobre anomalias.
- Relatórios internos dos Serviços da Microsoft em execução no Microsoft Azure e no Azure Governamental.
- As vulnerabilidades de segurança são relatadas para o [Centro de Respostas de Segurança da Microsoft(MSRC)](https://technet.microsoft.com/security/dn440717) via [secure@microsoft.com](mailto:secure@microsoft.com). O MSRC trabalha com parceiros e pesquisadores de segurança do mundo inteiro para ajudar a impedir incidentes de segurança e aprimorar a segurança dos produtos da Microsoft.
- Relatórios de cliente via [Portal de suporte ao cliente](https://www.windowsazure.com/support/contact/) ou via Portal de Gerenciamento do Azure Governamental ou do Microsoft Azure, que descrevem as atividades suspeitas atribuídas à infraestrutura do Azure (em vez das atividades que ocorrem dentro do escopo de responsabilidade do cliente).
- Atividade de segurança da [Equipe Azul e da Equipe Vermelha](https://azure.microsoft.com/blog/red-teaming-using-cutting-edge-threat-simulation-to-harden-the-microsoft-enterprise-cloud/). Essa estratégia usa uma equipe Vermelha ofensiva, da Microsoft, altamente especializada em segurança para descobrir e atacar possíveis falhas no Azure. A equipe Azul de resposta de segurança deve detectar e se defender das atividades da equipe Vermelha. As ações tanto da Equipe Vermelha quanto da Equipe Azul são usadas para verificar se os esforços de resposta de segurança do Azure estão gerenciando com eficiência os incidentes de segurança. As atividades de segurança da Equipe Vermelha e da Equipe Azul são operadas de acordo com as regras de envolvimento para ajudar a garantir a proteção dos dados do cliente.
- Escalonamento por operadores de Serviços do Azure. Os funcionários da Microsoft são treinados para identificar e escalonar possíveis problemas de segurança.

## <a name="azures-data-breach-response"></a>Resposta à violação de dados do Azure

A Microsoft atribui a prioridade adequada e os níveis de gravidade ao determinar o impacto funcional, a capacidade de recuperação e o impacto das informações do incidente. A prioridade e a severidade podem mudar durante a investigação, com base nas novas descobertas e conclusões. Os eventos de segurança que envolvem riscos iminentes ou confirmados para os dados dos clientes são tratados como de alta gravidade e trabalham o tempo todo até a resolução. 

O Microsoft Azure classifica o impacto das informações do incidente nas seguintes categorias:

| **Categoria** | **Definição** |
|:------------ |:-------------- |
| ***Nenhum*** | Nenhuma informação foi vazada, alterada, excluída ou comprometida de outra forma. |
| ***Violação de privacidade*** | Dados pessoais confidenciais de contribuintes tributários, funcionários, beneficiários, etc. foram acessados ou vazados. |
| ***Violação proprietária*** | Informações proprietárias não classificadas, como informações de infraestrutura crítica protegida (PCII), foram acessadas ou vazadas. |
| ***Perda de integridade*** | Informações confidenciais ou proprietárias foram alteradas ou excluídas. |

A equipe de resposta de segurança trabalha com os engenheiros de segurança do Microsoft Azure e Especialistas no Assunto (EAs) para classificar o evento com base em dados concretos das evidências. Um evento de segurança pode ser classificado como:

- **Falso Positivo**: Um evento que atende aos critérios de detecção, mas que é considerado como parte de uma prática empresarial normal e talvez precise ser filtrado. A equipe de serviços identifica a causa raiz dos falsos positivos e os aborda de maneira sistemática, usando as fontes de detecção e ajustando-as conforme for necessário.
- **Incidente de Segurança**: um incidente quando ocorre acesso ilegal a quaisquer Dados do Cliente ou Dados de Suporte armazenados no equipamento da Microsoft ou nas instalações da Microsoft, ou acesso não autorizado a tais equipamentos ou instalações, resultando na perda, divulgação ou alteração dos Dados do Cliente ou Dados de Suporte.
- **Incidente de Segurança Relatado pelo Cliente (CRSPI)**: Um acesso ilegal ou não autorizado ou o uso de sistemas, equipamentos ou recursos da Microsoft que resultem em divulgação, modificação ou perda de dados de clientes.
- **Violação de Privacidade**: Um subtipo de Incidente de Segurança que envolve dados pessoais. Manipular procedimentos não é diferente de um incidente de segurança.

Para um CRSI ser declarado, a Microsoft deve determinar que o acesso não autorizado aos dados do cliente ocorreu ou muito provavelmente ocorreu e/ou que há um compromisso jurídico ou contratual exigindo a notificação. É recomendável, mas não obrigatório, que as etapas de impacto, acesso a recursos e reparo de um cliente específico sejam notificadas. Um incidente geralmente é declarado como CRSI após a conclusão da etapa Diagnosticar um incidente de segurança. No entanto, a declaração pode ocorrer a qualquer momento quando todas as informações pertinentes estiverem disponíveis. O gerente de incidentes de segurança deve estabelecer evidências acima de dúvida razoável de que um evento a ser relatado ocorreu, a fim de começar a execução do Processo de Notificação do Incidente do Cliente.

A Microsoft confirma que o risco à empresa e ao cliente foi suprimido com êxito e que foram implementadas medidas corretivas. Se necessário, realizam-se etapas de atenuação emergenciais para resolver riscos de segurança imediatos associados ao evento.

A Microsoft também concluiu um post-mortem interno para violações de dados. Como parte deste exercício, a suficiência de respostas e os procedimentos operacionais são avaliados e todas as atualizações que possam ser necessárias para o SOP de Resposta a Incidentes de Segurança ou processos relacionados são identificados e implementados. Os postmortems internos para violações de dados são registros altamente confidenciais que não estão disponíveis para os clientes. No entanto, postmortems podem ser resumidos e incluídos nas notificações de evento de outro cliente. Esses relatórios são fornecidos para auditores externos para revisão como parte do ciclo de auditoria de rotina do Azure.

## <a name="customer-notification"></a>Notificação de cliente

A Microsoft notifica os clientes afetados e as autoridades regulatórias sobre violações de dados, conforme necessário. A Microsoft depende de uma forte compartimentação interna na operação do Azure. Os logs do fluxo de dados também são consistentes. Uma vantagem desse design é que a maioria dos incidentes pode ser filtrada por um escopo para clientes específicos. O objetivo é notificar os clientes afetados de forma precisa, acionável e em tempo hábil quando seus dados forem violados.

Após a declaração de um CRSPI, o processo de notificação ocorrerá o mais rapidamente possível, considerando os riscos de segurança da mudança rápida. Geralmente, o processo de redação das notificações acontece quando a investigação do incidente está em andamento. As notificações dos clientes são entregues em até 72 horas a partir do momento em que declaramos uma violação *exceto* nas seguintes circunstâncias:

- A Microsoft acredita que o ato de executar uma notificação aumentará o risco para outros clientes. Por exemplo, o ato de notificar pode alertar algum adversário, causando uma incapacidade para remediar.
- Outras circunstâncias incomuns ou extremas examinadas pelo departamento jurídico da Microsoft e pelo Gerente Executivo de Incidentes.
- O cronograma de 72 horas pode deixar alguns detalhes do incidente disponíveis. Esses detalhes são fornecidos aos clientes e autoridades regulatórias à medida que a investigação avança.

A Microsoft fornece aos clientes afetados informações detalhadas, permitindo-lhes realizar investigações internas e ajudá-los a cumprir os compromissos do usuário final, sem atrasar indevidamente o processo de notificação.

A notificação de uma violação de dados pessoais será entregue ao cliente afetado por qualquer meio que a Microsoft selecionar, incluindo por email. A notificação de uma violação de dados será entregue à lista de contatos de segurança fornecida na Central de Segurança do Azure, que pode ser configurada seguindo as [diretrizes de implementação](/azure/security-center/security-center-provide-security-contact-details). Se as informações de contato não forem fornecidas na Central de Segurança do Azure, a notificação é enviada para um ou mais administradores em uma assinatura do Azure. Para garantir que as notificações possam ser entregues com êxito, é responsabilidade do cliente garantir que as informações de contato administrativas em cada assinatura aplicável e o portal de serviços online estejam corretas.

A equipe do Microsoft Azure ou do Azure Government também pode optar por notificar outro pessoal da Microsoft, como membros da equipe do Serviço de Suporte ao Cliente (CSS) da Microsoft e o (s) Gerente (s) de Conta (AM) ou Gerente (es) Técnico (s) de Conta (TAM) do cliente. Essas pessoas geralmente mantêm um relacionamento próximo com o cliente e podem facilitar uma correção mais rápida.

## <a name="microsoft-dynamics-365-built-in-security-features"></a>Recursos de segurança internos do Microsoft Dynamics 365

O Microsoft Dynamics 365 utiliza a infraestrutura de serviços na nuvem e os recursos de segurança internos para proteger dados usando medidas e mecanismos de segurança. Além disso, o Dynamics 365 fornece um acesso a dados eficiente e colaboração com privacidade e integridade de dados nas seguintes áreas: [identidade segura, proteção de dados, segurança baseada em função e gerenciamento de ameaças](https://www.microsoft.com/trustcenter/security/dynamics365-security).

A oferta do Microsoft Dynamics 365 segue as mesmas medidas técnicas e organizacionais que uma ou mais equipes de serviço do Microsoft Azure tomam para proteção contra processos de violação de dados. Portanto, qualquer informação documentada no documento de notificação 'Violação de dados do Microsoft Azure' aqui é análoga ao Microsoft Dynamics 365 também.

## <a name="learn-more"></a>Saiba mais

[Central de Confiabilidade da Microsoft](https://www.microsoft.com/trust-center/privacy/gdpr-overview)
