---
title: Classificação de dados & taxonomia do rótulo de sensibilidade
description: Neste artigo, você pode encontrar uma visão geral do uso da classificação de dados & taxonomia de rótulo de sensibilidade com Microsoft 365.
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
hideEdit: true
ms.openlocfilehash: 396063b9ab094c7e5834572fe778046464ade81d
ms.sourcegitcommit: 01938022a292c07e98041dc6ae1312a1b8c617db
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2021
ms.locfileid: "58260326"
---
# <a name="data-classification--sensitivity-label-taxonomy"></a>Classificação de dados & taxonomia do rótulo de sensibilidade

Os dados confidenciais apresentam um risco significativo para uma empresa se eles são roubados, compartilhados inadvertidamente ou expostos por meio de uma violação. Os fatores de risco incluem danos à reputação, impacto financeiro e perda de vantagem competitiva. Proteger os dados e informações que sua empresa gerencia é uma prioridade máxima para sua organização, mas talvez seja difícil saber se seus esforços são realmente eficazes, considerando a quantidade de conteúdo mantida pela sua empresa.

Além do volume, seu conteúdo pode variar de altamente sensível e impactante a trivial e transitório. Ele também pode estar sob a alçada de vários requisitos de conformidade regulamentar. Saber o que priorizar e onde aplicar controles pode ser um desafio. Leia para saber mais sobre a classificação de dados *,* uma ferramenta importante para proteger seu conteúdo contra roubo, sabotagem ou destruição inadvertida e como a Microsoft 365 pode ajudá-lo a cumprir suas metas de segurança de informações.

## <a name="what-is-data-classification"></a>O que é classificação de dados?

[A classificação](/microsoft-365/compliance/data-classification-overview) de dados é um termo especializado usado nos campos de segurança cibernética e governança de informações para descrever o processo de identificação, categorização e proteção de conteúdo de acordo com sua sensibilidade ou nível de impacto. Em sua forma mais básica, a classificação de dados é um meio de proteger seus dados contra divulgação, alteração ou destruição não autorizadas com base no quão confidencial ou impactante eles são.

## <a name="what-is-a-data-classification-framework"></a>O que é uma estrutura de classificação de dados?

Geralmente codificada em uma política formal em toda a empresa, uma estrutura de classificação de dados (às vezes chamada de "política de classificação de dados") geralmente é composta por níveis de classificação de 3 a 5. Geralmente, eles incluem três elementos: um nome, uma descrição e exemplos do mundo real. A Microsoft recomenda não mais do que cinco rótulos pai de nível superior, cada um com cinco sub-rótulos (25 no total) para manter a interface do usuário (UI) gerenciável. Normalmente, os níveis são organizados do mínimo para o mais confidencial, como *Público,* *Interno,* *Confidencial* e *Altamente* 
 *Confidencial.* Outras variações de nome de nível que você pode encontrar *incluem Restricted,* *Unrestricted* e *Consumer Protected*. A Microsoft recomenda nomes de rótulo auto-descritivos e que realçam claramente sua sensibilidade relativa. Por exemplo, *Confidencial* e *Restrito* pode deixar os usuários supondo qual rótulo é apropriado, enquanto *Confidencial* e Altamente *Confidencial* são mais claros sobre o qual é mais confidencial. 

A tabela a seguir mostra um exemplo de *um* nível de estrutura de classificação de dados altamente confidencial:

|**Nível de classificação**|**Descrição**|**Exemplos**|
|:-----------------------|:--------------|:-----------|
| Altamente Confidencial | Os dados altamente confidenciais são o tipo mais confidencial de dados armazenados ou gerenciados pela empresa e podem exigir notificações legais se violadas ou divulgadas de outra forma. <br><br> Os Dados Restritos exigem o mais alto nível de controle e segurança, e o acesso deve ser limitado a "precisa saber". | Informações de identificação pessoal confidenciais (PII sensível) <br> Dados de titulares de cartão <br> Informações de saúde protegidas (PHI) <br> Dados de conta bancária |

>[!TIP]
>A estrutura de classificação de dados corporativos da Microsoft originalmente usou uma categoria e um rótulo chamado "Interno" durante a fase piloto, mas descobriu que havia motivos legítimos para um documento ser compartilhado externamente e deslocado para o uso de "Geral".

Outro componente importante de uma estrutura de classificação de dados são os controles associados a cada nível. Os níveis de classificação de dados por si só são rótulos (ou marcas) que indicam o valor ou a sensibilidade do conteúdo. Para *proteger* esse conteúdo, as estruturas de classificação de dados definem os controles que devem estar no local para cada um dos seus níveis de classificação de dados. Esses controles podem incluir requisitos relacionados a:

- Armazenamento tipo e local
- Criptografia
- Controle de acesso
- Destruição de dados
- Prevenção contra perda de dados
- Divulgação pública
- Log e controle de acesso
- Outros objetivos de controle, conforme necessário

Seus controles de segurança variam de acordo com o nível de classificação de dados, de forma que as medidas de proteção definidas em sua estrutura aumentem proporcionalmente com a sensibilidade do conteúdo. Por exemplo, seus requisitos de controle de armazenamento de dados variam dependendo da mídia que está sendo usada, bem como do nível de classificação aplicado a um determinado conteúdo. A tabela a seguir mostra um exemplo de controles de classificação de dados para um tipo de armazenamento específico:

|**Tipo de armazenamento**|**Confidencial**|**Interno**|**Irrestrita**|
|:---------------|:---------------|:-----------|:---------------|
| Removível Armazenamento | Proibido | Proibido, a menos que criptografado | Nenhum controle necessário |

A aplicação correta do nível correto de classificação de dados pode ser complexa em situações da vida real e, às vezes, sobrecarregar os usuários finais. Depois que uma política ou padrão é criada que define os níveis necessários de classificação de dados, é importante orientar os usuários finais sobre como dar vida a essa estrutura em seu trabalho diário. Essa área é onde as regras ou diretrizes de tratamento de classificação de dados chegam.

As diretrizes de tratamento de classificação de dados ajudarão os usuários finais com orientações específicas sobre como lidar com cada nível de dados adequadamente, para diferentes mídias de armazenamento ao longo de seu ciclo de vida. Essas diretrizes ajudam os usuários finais a aplicar corretamente regras na prática, por exemplo, ao compartilhar documentos, enviar emails ou colaborar em diferentes plataformas e organizações.

Os clientes da Microsoft indicam que aproximadamente 50% de um projeto de Proteção de Informações é voltado para os negócios, em vez de técnico, portanto, o treinamento e a comunicação do usuário final são fundamentais para o sucesso.
