---
title: Gerenciamento de contas em Microsoft 365
description: Saiba mais sobre o gerenciamento de contas Microsoft 365
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
ms.openlocfilehash: d525edfb9854df156f5b7b8571199b7a0102a0bf
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/12/2021
ms.locfileid: "59157994"
---
# <a name="account-management-in-microsoft-365"></a>Gerenciamento de contas em Microsoft 365

A Microsoft investiu pesadamente em sistemas e controles que automatizam a maioria das operações Microsoft 365, limitando intencionalmente a necessidade de acesso direto a servidores e dados do cliente pela equipe de serviço. Os humanos governam o serviço e o software opera o serviço. Essa estrutura permite que a Microsoft gerencie Microsoft 365 em escala e minimiza os riscos de ameaças internas e externas. A Microsoft aborda o controle de acesso com a suposição de que todos são uma ameaça potencial para Microsoft 365 serviços e dados do cliente. Por esse motivo, o princípio ZSA (Zero Standing Access) estabelece a base para toda a estrutura de controle de acesso usada pelo Microsoft 365.

Por padrão, a equipe da Microsoft tem acesso privilegiado zero a qualquer ambiente Microsoft 365 ou dados do cliente de uma organização. É apenas por meio de um sistema robusto de verificações e aprovações que os funcionários da equipe de serviço podem obter acesso privilegiado com uma ação estreita e escopo de tempo. Por meio desse sistema, a Microsoft pode reduzir significativamente o potencial Microsoft 365 equipe de serviço e invasores de obter acesso não autorizado ou causar danos mal-intencionados ou acidentais a serviços Microsoft e clientes.

## <a name="account-types"></a>Tipos de conta

Microsoft 365 atende a todas as missões organizacionais e funções comerciais usando três categorias de contas: contas de equipe de serviço, contas de serviço e contas de clientes. Gerenciar essas contas é uma responsabilidade compartilhada entre a Microsoft e os clientes. A Microsoft gerencia a equipe de serviço e contas de serviço, que são usadas para operar e dar suporte a produtos e serviços da Microsoft. As contas de clientes são gerenciadas pelo cliente e permitem que eles adaptem o acesso à conta para atender aos requisitos de controle de acesso interno.

![Responsabilidade compartilhada por contas](../media/assurance-shared-responsibility-for-accounts.png)

## <a name="microsoft-managed-accounts"></a>Contas gerenciadas pela Microsoft

**As contas de equipe de** serviço são usadas Microsoft 365 equipe de serviço desenvolvendo e mantendo Microsoft 365 serviços. Essas contas não têm acesso privilegiado permanente aos serviços Microsoft 365, em vez disso, podem ser usadas para solicitar acesso privilegiado temporário e limitado para executar uma função de trabalho especificada. Nem todas as contas de equipe de serviço podem executar as mesmas ações, a separação de funções é imposta usando o controle de acesso baseado em função (RBAC). As funções garantem que os membros da equipe de serviço e suas contas tenham apenas o acesso mínimo necessário para executar tarefas específicas. Além disso, as contas de equipe de serviço não podem pertencer a várias funções nas quais elas podem atuar como aprovadores de suas próprias ações.

**As contas de** serviço são usadas Microsoft 365 serviços para autenticar ao se comunicar com outros serviços por meio de processos automatizados. Assim como as contas de equipe de serviço só têm o acesso mínimo necessário para executar as obrigações de trabalho da equipe específica, as contas de serviço só têm o acesso mínimo necessário para sua finalidade pretendida. Além disso, há vários tipos de contas de serviço projetadas para atender a uma necessidade específica. Um Microsoft 365 pode ter várias contas de serviço, cada uma com uma função diferente a ser desempenhada.

## <a name="customer-managed-accounts"></a>Contas gerenciadas pelo cliente

**As contas de** clientes são usadas para acessar Microsoft 365 serviço e são as únicas contas pelas que cada cliente é responsável. É dever do cliente criar e gerenciar as contas em sua organização para manter um ambiente seguro. O gerenciamento de contas de clientes é feito Azure Active Directory (AAD) ou federado com o Active Directory (AD) local. Cada cliente tem um conjunto exclusivo de requisitos de controle de acesso que devem atender, e as contas de clientes concedem a cada cliente a capacidade de atender às suas necessidades individuais. As contas de clientes não podem acessar dados fora da organização do cliente.

## <a name="service-team-account-management"></a>Gerenciamento de conta de equipe de serviço

Microsoft 365 gerencia contas de equipe de serviço durante todo o ciclo de vida usando um sistema de gerenciamento de conta chamado Gerenciamento de Identidade (IDM). O IDM usa uma combinação de processos de verificação automatizados e aprovação gerencial para impor os requisitos de segurança relacionados ao acesso à conta da equipe de serviço.

Os membros da equipe de serviço não têm automaticamente uma conta de equipe de serviço, eles devem primeiro atender aos requisitos de qualificação e obter aprovação de um gerente autorizado. Para ser qualificado para uma conta de equipe de serviço, o pessoal da equipe de serviço deve primeiro passar pela triagem de funcionários pré-empregatícios, uma verificação em segundo plano na nuvem [e](assurance-cloud-background-check.md)concluir todo o treinamento padrão e obrigatório baseado em função. [](assurance-pre-employment-screening.md) Depois que todos os requisitos de qualificação foram atendidos, uma solicitação para uma conta de equipe de serviço pode ser feita e deve ser aprovada por um gerente autorizado.

![Processo de triagem de equipe](../media/assurance-personnel-screening-process.png)

O IDM também é responsável por acompanhar a rescreening periódica e o treinamento necessários para manter uma conta de equipe de serviço. A verificação de plano de fundo da nuvem da Microsoft deve ser concluída a cada dois anos e todo o material de treinamento deve ser revisado anualmente. Se um desses requisitos não for atendido pela data de expiração, sua qualificação será revogada e a conta da equipe de serviço será desabilitada automaticamente.

Além disso, a qualificação da conta de equipe de serviço é atualizada automaticamente por [transferência e término de pessoal.](assurance-employee-transfer-termination.md) As alterações feitas no SISTEMA de Informações de Recursos Humanos (HRIS) disparam o IDM para tomar medidas, o que varia dependendo da situação. A transferência de funcionários para outra equipe de serviço terá uma data de expiração definida para suas eligibilidades e uma solicitação para manter as eligibilidades deve ser enviada pelo membro da equipe de serviço e aprovada pelo novo gerente. Funcionários encerrados automaticamente têm todas as eligibilidades revogadas e sua conta de equipe de serviço é desabilitada no último dia. Uma solicitação urgente de revogação de conta pode ser feita para terminações involuntárias.

Por padrão, as contas de equipe de serviço têm acesso de leitura limitado a metadados de sistema amplos usados para solução de problemas regulares. Além disso, as contas de equipe de serviço de linha de base não podem solicitar acesso privilegiado Microsoft 365 ou dados do cliente. Outra solicitação deve ser feita para que a conta da equipe de serviço seja adicionada a uma função que permita que o membro da equipe de serviço solicite privilégios elevados para executar tarefas e operações específicas.
