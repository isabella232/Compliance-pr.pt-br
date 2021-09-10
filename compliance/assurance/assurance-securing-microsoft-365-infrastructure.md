---
title: Protegendo a infraestrutura do Microsoft 365
description: Saiba como a Microsoft garante a infraestrutura Microsoft 365 de segurança.
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH
ms.service: O365-seccomp
ms.localizationpriority: medium
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 6c20c62feb1ff3ab23eeb97d5ad11abb5ad85a07
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2021
ms.locfileid: "58946921"
---
# <a name="securing-the-microsoft-365-infrastructure"></a>Protegendo a infraestrutura do Microsoft 365

Microsoft 365 é um dos maiores serviços de nuvem empresarial e consumidor do mundo e continua a crescer rapidamente, tanto na base de clientes, produtos e recursos. Os clientes se Microsoft 365 para suas soluções de produtividade de classe mundial, mas para ajudar a proteger suas informações mais confidenciais do cenário de ameaças cibernéticas em constante evolução. É a prioridade máxima da Microsoft para manter os dados do cliente seguros e manter a confiança do cliente.

A segurança de um sistema dessa escala e complexidade não é possível se a segurança for um efeito final, ela só será efetiva se a segurança for integrada durante o processo de design inicial. Exige um sistema robusto de detecção de ameaças com respostas de prompt de sistemas automatizados e engenheiros altamente qualificados. A avaliação contínua e a validação desses sistemas são essenciais para garantir que as configurações seguras permaneçam intactas e, anteriormente, as vulnerabilidades desconhecidas sejam identificadas.

## <a name="core-security-principles"></a>Principais princípios de segurança

Sete princípios de segurança estabelecem  a base para nossa estrutura de proteção dos serviços Microsoft 365  contra *ameaças,* detecção e resposta a quaisquer ameaças e avaliação contínua da postura de segurança e melhoria dos serviços com base nos resultados dessas avaliações.

- **Privacidade de** dados : os clientes têm seus dados e a Microsoft é o custodiante. Microsoft 365 serviços foram projetados para operar sem que os engenheiros acessem dados do cliente, a menos que sejam solicitados explicitamente e aprovados pelo cliente.
- **Pressupondo** violação : Funcionários e serviços são tratados como se o comprometimento fosse uma possibilidade real.
- **Privilégio mínimo**: o acesso e as permissões aos recursos estão limitados apenas ao que é necessário para executar as tarefas necessárias.
- **Limites de violação:** identidades e infraestrutura em um limite são isolados de recursos em outros limites. O comprometimento de um limite não deve levar ao comprometimento de outro.
- **Segurança integrada de** malha de serviço : As prioridades e os requisitos de segurança são integrados ao design de novos recursos e recursos, garantindo que uma postura de segurança forte seja dimensionado com cada serviço.
- **Automatizado e automático:** a Microsoft se concentra no desenvolvimento de produtos e arquiteturas duráveis que podem impor de forma inteligente e automática a segurança do serviço, ao mesmo tempo que dão aos engenheiros da Microsoft a capacidade de gerenciar com segurança as respostas a ameaças de segurança em escala.
- **Segurança adaptável**: os recursos de segurança da Microsoft se adaptam e são aprimorados por modelos de aprendizado de máquina, testes de penetração de rotina e avaliações automatizadas.

## <a name="protection"></a>Proteção

### <a name="access-control"></a>Controle de acesso

Por padrão, os funcionários responsáveis pelo desenvolvimento e manutenção Microsoft 365 serviços têm o ZSA (Zero Standing Access) para a infraestrutura de serviço. Embora a Microsoft se esforça para contratar apenas os melhores engenheiros e verificações rigorosas em segundo plano são necessárias, a Microsoft não assume que eles sejam confiáveis por padrão nos serviços operacionais. Além disso, quando os engenheiros são aprovados para acesso privilegiado, eles só têm acesso por um período limitado para executar apenas as ações necessárias para um escopo específico da infraestrutura de serviço. A Microsoft se refere a essas políticas como Just-in-Time (JIT) e Just-Enough-Access (JEA), que são implementadas por meio de um sistema chamado Lockbox.

Para adquirir privilégios elevados, os engenheiros da Microsoft enviam uma solicitação para a tarefa específica e especificam o período de tempo para realvá-la. Depois de aprovado, o Lockbox gera uma conta JIT especializada com a capacidade de executar apenas a tarefa solicitada. As ações geralmente têm a forma de fluxos de trabalho automatizados que executam com segurança qualquer solução de problemas ou recuperação necessária. Em raras instâncias, quando o acesso direto à infraestrutura é necessário, as PAWs (Estações de Trabalho de Acesso Privilegiado) estritamente monitoradas são necessárias.

Usuários desonestos e contas comprometidas são uma possibilidade real em qualquer organização, e nosso sistema de controle de acesso foi projetado para proteger contra essas ameaças.

Para obter mais informações sobre o controle de acesso, consulte [Identity and access management overview](assurance-identity-and-access-management.md).

### <a name="encryption"></a>Criptografia

Embora os controles de acesso forneçam uma função vital na defesa dos serviços Microsoft 365, a criptografia é usada em todo o ciclo de vida de dados para proteger ainda mais a confidencialidade e a privacidade dos clientes da Microsoft.

Os dados em trânsito entre máquinas cliente, Microsoft 365 servidores e servidores não Microsoft 365 são criptografados usando o TLS 1.2. Revisamos regularmente as codificações e protocolos em uso, adicionando protocolos aprimorados quando disponíveis e removendo os mais fracos conforme necessário.

O conteúdo do cliente em repouso nos servidores Microsoft é criptografado no nível de volume usando o BitLocker. A criptografia no nível do aplicativo também pode ser aplicada usando chaves gerenciadas pela Microsoft ou pelo cliente. O acesso às chaves gerenciadas pela Microsoft só é possível quando autorizado e aprovado por meio do processo JIT e JEA.

Para obter mais informações sobre criptografia em Microsoft 365, consulte [Encryption and key management overview](assurance-encryption.md).

### <a name="network-isolation"></a>Isolamento de rede

Em linha com o princípio de privilégio mínimo, Microsoft 365 restringe a comunicação entre diferentes partes da infraestrutura de serviço apenas ao que é necessário para operar. Todo o tráfego de rede é negado por padrão, com apenas a comunicação explicitamente definida sendo permitida. Essa restrição estabelece limites de violação em toda a infraestrutura. Teams que gostaria de adicionar novos caminhos de rede para acomodar um novo recurso ao seu serviço deve ter a solicitação avaliada e aprovada antes de poder ser aberta.

Para obter mais informações sobre isolamento de rede Microsoft 365, [consulte Microsoft 365 controles de isolamento](/microsoft-365/enterprise/microsoft-365-isolation-controls).

## <a name="detection--response"></a>Resposta & detecção

### <a name="security-monitoring"></a>Monitoramento de segurança

O monitoramento de segurança na escala em massa da Microsoft só é possível gerando alertas altamente precisos usando soluções automatizadas baseadas em nuvem. Os logs de auditoria de cada serviço e dados de telemetria coletados em toda a infraestrutura principal são enviados para uma solução de processamento e alerta centralizada centralizada em tempo real.

As ameaças detectadas são corrigidas usando ações disparadas automaticamente quando possível. Quando soluções automatizadas não são bem-sucedidas ou incapazes de resolver o problema, os engenheiros da Microsoft de chamada imediatamente tomarão medidas para atenuar a ameaça.

Para obter mais informações sobre o monitoramento de segurança Microsoft 365, consulte [Visão geral do monitoramento de segurança.](assurance-security-monitoring.md)

## <a name="assessment"></a>Avaliação

### <a name="automated-assessments"></a>Avaliações automatizadas

Independentemente de como um sistema é projetado, a postura de segurança pode se degradar devido à deriva de configuração intencional e não intencional ao longo do tempo. As ferramentas automatizadas avaliam constantemente Microsoft 365 sistemas que estão procurando serviços não configurados e não configurados. Essa avaliação é geralmente chamada de patching, antivírus, vulnerabilidade e verificação de configuração (PAVC).

Nossa arquitetura também é validada com frequência, identificando instâncias como portas abertas nãousadas e contas com acesso administrativo permanente. Todos os serviços que derivam de um estado desejado pré-definido são automaticamente levados de volta ao alinhamento.

Para obter mais informações sobre o monitoramento de segurança Microsoft 365, consulte Visão geral do gerenciamento [de vulnerabilidades.](assurance-vulnerability-management.md)

### <a name="attack-simulation-and-penetration-testing"></a>Simulação de ataque e teste de penetração

Microsoft 365 prioridade principal é evitar que ataques se infileiem em defesas. Microsoft 365 tem uma equipe dedicada de especialistas em segurança que estão constantemente realizando ataques simulados para identificar vulnerabilidades desconhecidas anteriormente e fornecer um fluxo constante de dados avançados para melhorar os recursos de monitoramento de segurança. Esses ataques simulados se formam de ataques automatizados frequentes em pequena escala e imersões profundas orientadas por especialistas. A partir dessas atividades, a Microsoft avalia a capacidade de detectar, responder e despejar invasores.

Para obter mais informações sobre o monitoramento de segurança Microsoft 365, consulte [Simulação de ataque em Microsoft 365](assurance-monitoring-and-testing.md).

## <a name="resources"></a>Recursos

[Nos bastidores: protegendo a infraestrutura que faz o Serviço do Microsoft 365 funcionar](https://download.microsoft.com/download/c/4/5/c45b197e-f0d9-4f40-bd5f-ed8fc7d0cd8c/M365DCSecurityIntro_Whitepaper.pdf)
