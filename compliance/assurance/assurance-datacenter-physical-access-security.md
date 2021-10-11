---
title: Segurança de acesso físico do datacenter
description: Saiba mais sobre a segurança de acesso físico do datacenter da Microsoft.
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
ms.openlocfilehash: f7cc71354c4be52d97c8b4b6efbe5a88ca9413a5
ms.sourcegitcommit: cf424cb1e7c12048120977f294f780b776119a96
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/11/2021
ms.locfileid: "60265076"
---
# <a name="datacenter-physical-access-security"></a>Segurança de acesso físico do datacenter

A Microsoft entende a importância de proteger dados do cliente e está comprometida em proteger os datacenters que os contêm. Os datacenters da Microsoft são projetados, criados e operados para limitar estritamente o acesso físico às áreas onde os dados do cliente são armazenados.

A segurança física nos datacenters está alinhada com o princípio de defesa em profundidade. Várias medidas de segurança são implementadas para reduzir o risco de usuários não autorizados acessarem dados e outros recursos do datacenter.

- **Segurança de** perímetro : os datacenters da Microsoft são edifícios não descritos com cerca de perímetro e iluminação externa de 24 horas. As cercas altas feitas de metal e concreto abrangem cada centímetro do perímetro e toda a entrada no campus do datacenter deve passar por um ponto de acesso bem definido. Portões de entrada monitorados pela câmera e proteções de segurança garantem que a entrada e a saída sejam restritas às áreas designadas. Os bollards e outras medidas protegem o exterior do datacenter contra possíveis ameaças, incluindo acesso não autorizado.
- **Inserindo o datacenter**: a entrada do datacenter está com funcionários profissionais de segurança que passaram por rigorosos treinamentos e verificações em segundo plano. Os agentes de segurança rotineiramente patrulam o datacenter e os feeds de vídeo de câmeras dentro do datacenter são sempre monitorados.
- **Dentro do datacenter**: Ao entrar no edifício, a autenticação de dois fatores com biometria é necessária para continuar a mover-se pelo datacenter. Depois de autenticado, o acesso é concedido à parte autorizada do datacenter e somente pelo tempo aprovado. Dentro do datacenter, as áreas designadas como altamente confidenciais exigem autenticação adicional de dois fatores.
- **Piso do datacenter**: o piso do datacenter só pode ser acessado com aprovação prévia e após uma triagem de detecção de metal de corpo completo no momento da entrada. Para reduzir o risco de entrada ou saída de dados não autorizados do datacenter, somente dispositivos aprovados podem entrar no piso do datacenter. Além disso, as câmeras de vídeo monitoram a parte frontal e traseira de cada rack de servidor. Ao sair do piso do datacenter, todos os indivíduos estão sujeitos a uma triagem adicional de detecção de metal de corpo inteiro.
- **Sair do datacenter**: Para sair da instalação do datacenter, cada pessoa deve passar por um ponto de verificação de segurança final e todos os visitantes devem render seus selos temporários. Após a coleção, todos os selos de visitante têm seus níveis de acesso removidos antes de ser reutilizáveis para futuras visitas.

## <a name="access-provisioning"></a>Provisionamento de acesso

A equipe de Gerenciamento de Datacenter (DCM) implementou procedimentos operacionais para restringir o acesso físico apenas a funcionários autorizados, contratados e visitantes. As solicitações de acesso temporário ou permanente são controladas usando um sistema de tíquetes. Os selos são emitidos ou ativados para funcionários que exigem acesso após a verificação da identificação. Chaves físicas e selos de acesso temporário são protegidos no CENTRO de operações de segurança (SOC).

Os datacenters da Microsoft estão sujeitos a uma política de acesso com privilégios mínimos, o que significa que o acesso ao datacenter é restrito a funcionários com uma necessidade de negócios aprovada, sem mais acesso do que o necessário. As solicitações de acesso são limitadas por tempo e só serão renovadas se a necessidade de negócios do solicitante permanecer válida.

Os registros de acesso ao datacenter são mantidos na forma de solicitações aprovadas. As solicitações só podem ser aprovadas pela equipe do DCM, e as solicitações de acesso de visitante aos datacenters são registradas e disponibilizadas para quaisquer investigações futuras

## <a name="datacenter-security-personnel"></a>Equipe de segurança do Datacenter

A equipe de segurança em todas as instalações do datacenter e campus são responsáveis pelas seguintes atividades:

- Opere estações de trabalho localizadas no Centro de Operações de Segurança no edifício de administração principal.
- Conduza inspeções periódicas por meio de passo a passo de instalações e de patrulheiros dos terrenos.
- Responder a alarmes de incêndio e problemas de segurança
- Expedir equipes de segurança para ajudar solicitações de serviço e emergências
- Fornecer à equipe de Gerenciamento de Datacenter atualizações periódicas sobre eventos de segurança e logs de entrada
- Operar e monitorar sistemas de alarme, controle de acesso e monitoramento

## <a name="visitor-access"></a>Acesso para visitantes

A verificação e o check-in de segurança são necessários para funcionários que exigem acesso temporário ao interior da instalação do datacenter, incluindo grupos de tour e outros visitantes. Os visitantes do datacenter devem assinar um contrato de não divulgação, passar por uma revisão de gerenciamento de datacenter e obter aprovação pelo gerenciamento de datacenter antes de sua visita agendada. Após a chegada inicial, os visitantes do datacenter são processados com credenciais de acesso temporário e com menos privilégios. Além disso, um FTE (funcionário em tempo integral) da Microsoft ou um designador autorizado aprovado pelo gerenciamento de datacenter é atribuído para acompanhar os visitantes durante a visita.

Todos os visitantes que tenham acesso aprovado ao datacenter são designados como *Escort Only* em seus selos e devem permanecer sempre com suas acompanhantes. Os visitantes acompanhados não têm níveis de acesso concedidos a eles e só podem viajar no acesso de suas acompanhantes. A acompanhante é responsável por revisar as ações e o acesso de seus visitantes durante a visita ao datacenter.

O acesso aos visitantes é monitorado pela acompanhante atribuída e pelo Supervisor da Sala de Controle por meio da TV de circuito fechado (CFTV) e do sistema de monitoramento de alarme. Os visitantes com uma solicitação de acesso aprovada têm sua solicitação de acesso revisada no momento em que sua identificação é verificada em uma forma de identificação emitida pelo governo ou selo emitido pela Microsoft. Os visitantes aprovados para acesso acompanhado são emitidos com um selo auto-expirado e, ao retornar o registro de acesso dentro da ferramenta, é encerrado. Se um visitante sair com seu selo, o selo expira automaticamente dentro de 24 horas.

Os selos de acesso temporário são armazenados no SOC controlado pelo acesso e inventariados no início e no final de cada turno. Os agentes de segurança são funcionários 24x7 e as chaves físicas são armazenadas em um sistema de gerenciamento de chaves eletrônicas que está vinculado ao sistema de acesso físico que exige o PIN e o selo de acesso de um agente de segurança para obter acesso.

## <a name="access-review-and-deprovisioning"></a>Revisão e desprovisionamento do Access

A equipe do DCM é responsável pela revisão do acesso ao datacenter regularmente e pela realização de uma auditoria trimestral para verificar se o acesso individual ainda é necessário.

Para terminações ou transferências, o acesso da pessoa é imediatamente removido do sistema e seu selo de acesso é removido. Isso remove qualquer acesso de datacenter que a pessoa possa ter tido. As equipes do DCM também executam análises de acesso trimestral para validar a adequação da lista de acesso ao datacenter no sistema.

## <a name="key-management"></a>Gerenciamento-chave

As chaves físicas/duras são verificadas para funcionários específicos, correspondendo o selo de acesso da pessoa à chave física. Uma pessoa deve ter o nível de acesso apropriado na ferramenta para verificar chaves específicas. Chaves não são permitidas fora do local.

As teclas e selos rígidos são mantidos sob controle estrito pela Microsoft e são auditados diariamente. A Microsoft também reduz os riscos implementando a atribuição estrita de níveis de acesso e a distribuição controlada e o gerenciamento de chaves. Os principais métodos de acesso em datacenters são selos de acesso eletrônico e biometria, o que permite revogar imediatamente o acesso conforme necessário. A Microsoft tem procedimentos para determinar a ação apropriada proporcional ao risco de todas as chaves perdidas. Essas ações podem exigir o rekeying de um rack ou porta de servidor único e até o rekeying de toda a instalação do datacenter.

## <a name="access-logging-and-monitoring"></a>Log de acesso e monitoramento

Solicitações de acesso e eventos de entrada/saída são registrados e mantidos como parte de uma trilha de auditoria eletrônica, permitindo após a reconciliação e a reconciliação dos dados de fatos. Os relatórios do sistema de controle de acesso e a análise de dados permitem uma detecção adicional de anomalias para identificar e impedir o acesso desnecessário e não autorizado.

Os sistemas de vigilância de datacenter monitoram áreas críticas do datacenter, como entrada/saída principal do datacenter, entrada/saída de colocações de datacenter, enjaulações, gabinetes bloqueados, formas de passagem, áreas de envio e recebimento, ambientes críticos, portas de perímetro e áreas de estacionamento. As gravações de segurança são mantidas por um mínimo de 90 dias, a menos que a lei local dita o contrário.

Um Supervisor de Sala de Controle está sempre no SOC para fornecer monitoramento do acesso físico no datacenter. A segurança de vídeo é empregada para monitorar o acesso físico ao datacenter e ao sistema de informações. O sistema de monitoramento de vídeo é vinculado ao sistema de monitoramento de alarme de construção para dar suporte ao monitoramento de acesso físico de pontos de alarme. Os agentes de segurança garantem que somente os funcionários com autorização adequada tenham acesso permitido e verifiquem se qualquer pessoa que traz equipamentos para dentro e para fora de instalações de infraestrutura críticas segue os procedimentos adequados.

Os eventos de segurança que ocorrem no datacenter são documentados pela equipe de segurança em um relatório chamado Notificação de Evento de Segurança (SEN). Os relatórios SEN capturam os detalhes de um evento de segurança e são necessários para serem documentados depois que um evento ocorre para capturar detalhes com a maior precisão possível. Os relatórios do SEN também contêm a análise investigativa conduzida em um Relatório após a ação (AAR), que documenta a investigação de um evento de segurança, tenta identificar a causa raiz do evento e registra todas as ações de correção e lições aprendidas. As ações de correção e as lições aprendidas são usadas para melhorar os procedimentos de segurança e reduzir a agregação do evento que se repete. Se um incidente afetar os ativos ou serviços da Microsoft, a equipe de Gerenciamento de Incidentes de Segurança (SIM) terá procedimentos detalhados para responder.

Além da segurança 24x7 no local, os datacenters da Microsoft utilizam sistemas de monitoramento de alarmes que fornecem monitoramento de vídeo e alarme em tempo real. As portas do datacenter têm alarmes que relatam cada abertura e quando permanecem abertas após um período de tempo programado. O sistema de segurança é programado para exibir imagem de vídeo ao vivo quando um alarme de porta é disparado. Os leitores biométricos e de cartão de acesso são programados e monitorados por meio do sistema de monitoramento de alarmes. Os alarmes são monitorados e respondidos 24 x 7 pelo Supervisor da Sala de Controle que utiliza câmeras na área do incidente que está sendo investigado para dar informações em tempo real ao respondente.
