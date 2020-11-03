---
title: Atualizar estimativa ao término
description: Este tópico fornece informações sobre como atualizar a projeção de esforço em um projeto.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 16393133a5de17308caceb069d7bca670caa04c8
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071611"
---
# <a name="update-estimate-at-completion"></a>Atualizar estimativa ao término

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pró-forma_

É comum que um gerente de projetos revise as estimativas originais em uma tarefa. As reprojeções de projetos são a percepção de um gerente de projetos sobre as estimativas, considerando o estado atual de um projeto. No entanto, não é recomendável que os gerentes de projetos alterem os números da linha de base, pois a linha de base do projeto representa a fonte de referência estabelecida para a estimativa de custo e de agenda dele e todos os participantes do projeto concordaram com ela.

Um gerente de projetos pode reprojetar o esforço em tarefas de duas maneiras:

- Substituindo a estimativa até a conclusão (ETC) padrão por uma nova estimativa do esforço restante real na tarefa. 
- Substituindo a porcentagem de progresso padrão por uma nova estimativa do verdadeiro progresso na tarefa.

Cada uma dessas abordagens causa o recálculo de ETC, estimativa ao término (EAT), porcentagem de progresso e variação de esforço projetada da tarefa. A EAT, a ETC e a porcentagem de progresso nas tarefas de resumo são recalculadas e produzem uma nova projeção da variação de esforço.
