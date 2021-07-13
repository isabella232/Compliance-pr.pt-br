---
title: Transferência e rescisão de funcionários da Microsoft
description: Saiba mais sobre o processo de transferência e rescisão de funcionários da Microsoft Microsoft 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 862bd05a84e5144602a24ac2aca1780cffaff3fe
ms.sourcegitcommit: 48b8ec2dd00e957508e5af82458bf697e1a97ebb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/12/2021
ms.locfileid: "53395611"
---
# <a name="microsoft-employee-transfer-and-termination"></a>Transferência e rescisão de funcionários da Microsoft

A Microsoft, como todas as outras organizações, lida com transferências e terminações de funcionários como parte de sua operação comercial normal. Quando um funcionário muda de posição ou sai da empresa, é essencial revogar o acesso inadequado em tempo hábil. Para facilitar alterações de acesso eficientes e revogações de acesso, a Microsoft usa procedimentos padronizados e processos automatizados para coordenar o HRIS (Sistema de Informações de Recursos Humanos) com o sistema de Gerenciamento de Identidade (IDM). A orquestração automatizada entre esses dois sistemas é essencial para manter a consistência operacional, proteger os serviços online e os dados da Microsoft, evitar o rebaixamento de privilégios e reduzir os riscos relacionados a ameaças internas.

Os serviços online da Microsoft foram projetados para operar sem acesso administrativo permanente a ambientes de produção para nossos engenheiros. A Microsoft usa um modelo Just-In-Time (JIT), Just-Enough-Access (JEA) para fornecer aos engenheiros o acesso temporário necessário para dar suporte ao serviço quando necessário. Para solicitar e usar uma conta de equipe de serviço para acesso JIT, os engenheiros devem solicitar e manter eligibilidades por meio da ferramenta IDM. Quando os funcionários são transferidos ou encerrados, a conta da equipe de serviço e as eligibilidades relacionadas são modificadas automaticamente para impedir o acesso inadequado.

## <a name="transfer-and-reassignment"></a>Transferência e reatribuição

As transferências de funcionários são iniciadas por meio de uma solicitação de transação de transferência pelo gerente do funcionário. O gerente cria uma requisição e se envolve com a Aquisição Global de Talentos para o processo de carta de oferta. Depois que o funcionário aceita a oferta para a nova função, os serviços de RH concluem a transferência nas ferramentas principais de RH, disparando o IDM para definir uma data de expiração para todas as eligibilidades do funcionário. O funcionário deve enviar uma solicitação e receber aprovação de seu novo gerente para manter suas eligibilidades. A falha ao enviar uma solicitação ou receber aprovação do gerente resulta na revogação das eligibilidades do funcionário transferido. Para transferências que incluem implicações de segurança específicas, os acessos ao sistema e associações a grupos de segurança são reavaliados imediatamente para refletir sua nova função.

## <a name="termination"></a>Terminação

A Microsoft usa políticas e procedimentos claramente definidos para revogar prontamente o acesso físico e lógico aos sistemas e recursos da Microsoft quando um funcionário é encerrado. Quando um funcionário dá sua notificação, o gerente do funcionário ins fornece a data de término no HRIS. Após o último dia útil do funcionário, o HRIS marca o funcionário como encerrado e compartilha as informações com o IDM, que remove todas as contas de equipe de serviço e as eligibilidades automaticamente.

Para terminações involuntárias, o RH trabalha com o gerente do funcionário para seguir as etapas apropriadas para encerrar e desalocar o funcionário. Semelhante a uma rescisão voluntária, as informações de término são inseridas no HRIS juntamente com todas as etapas necessárias, como coordenação de data efetiva, remoção de acesso. e quaisquer outras etapas relativas à transição para fora da função.
