---
title: Consumo de custo e progresso do projeto
description: Este tópico fornece informações sobre como acompanhar o consumo de custo e o progresso do projeto.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 0d742164-5469-421d-8917-63160a81f651
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8aa5814938129f30885d8161a7c86197ab013364
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749133"
---
# <a name="project-progress-and-cost-consumption"></a>Consumo de custo e progresso do projeto

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

A necessidade de acompanhar o progresso em relação a uma agenda varia por setor. Alguns setores fazem o acompanhamento em um nível granular, enquanto outros o fazem em um nível superior. Este tópico mostra como fazer agendamentos para atender aos requisitos da sua organização.

## <a name="effort-tracking-view"></a>Exibição de Acompanhamento de Esforço

A exibição **Acompanhamento de esforço** acompanha o progresso de tarefas na agenda. Ela compara as horas de esforço reais gastas em uma tarefa com as horas de esforço planejadas para essa tarefa. O PSA usa as fórmulas a seguir para calcular as métricas de acompanhamento:

- Porcentagem de progresso = Esforço real empenhado até o momento ÷ Esforço planejado para a tarefa 
- Estimativa até a conclusão (ETC) = Esforço planejado – Esforço real empenhado até o momento 
- Estimativa ao término (EAT) = Esforço restante + Esforço real empenhado até o momento 
- Variação de esforço projetada = Esforço planejado – EAT

O PSA mostra uma projeção da variação de esforço na tarefa. Se a EAT for maior do que o esforço planejado, a projeção é de que a tarefa levará mais tempo do que foi planejado originalmente. Portanto, está atrasada. Se a EAT for menor do que o esforço planejado, a projeção é de que a tarefa levará menos tempo do que foi planejado originalmente. Portanto, está adiantada.

## <a name="re-projecting-effort"></a>Reprojetar esforço

É comum que um gerente de projetos revise as estimativas originais em uma tarefa. As reprojeções de projetos são a percepção de um gerente de projetos sobre as estimativas, considerando o estado atual de um projeto. No entanto, não é recomendável que os gerentes de projetos alterem os números da linha de base, pois a linha de base do projeto representa a fonte de referência estabelecida para a estimativa de custo e de agenda dele e todos os participantes do projeto concordaram com ela.

Um gerente de projetos pode reprojetar o esforço em tarefas de duas maneiras:

- Substituindo a ETC padrão por uma nova estimativa do esforço restante real na tarefa. 
- Substituindo a porcentagem de progresso padrão por uma nova estimativa do verdadeiro progresso na tarefa.

Cada uma dessas abordagens causa o recálculo de ETC, EAT, porcentagem de progresso e variação de esforço projetada em uma tarefa. A EAT, a ETC e a porcentagem de progresso nas tarefas de resumo também são recalculadas e produzem uma nova projeção da variação de esforço.

## <a name="re-projection-of-effort-on-summary-tasks"></a>Reprojeção de esforço em tarefas de resumo

O esforço em tarefas de resumo ou de contêiner pode ser reprojetado. Independentemente do usuário reprojetar usando o esforço restante ou a porcentagem de progresso nas tarefas de resumo, o seguinte conjunto de cálculos é iniciado:

- A EAT, a ETC e a porcentagem de progresso na tarefa são calculadas.
- A nova EAT é distribuída até as tarefas filho na mesma proporção em que a EAT original foi distribuída na tarefa.
- A nova EAT em cada uma das tarefas individuais até as tarefas de nó folha é calculada. 
- As tarefas filho afetadas até os nós folha têm sua ETC e porcentagem de progresso recalculadas com base no valor da EAT. Isso resulta em uma nova projeção da variação de esforço da tarefa. 
- As EATs das tarefas de resumo até o nó raiz são recalculadas.

### <a name="cost-tracking-view"></a>Exibição Acompanhamento de custo 

A exibição **Acompanhamento de custo** compara o custo real empenhado em uma tarefa com o custo planejado para essa tarefa. 

> [!NOTE]
> Essa exibição mostra apenas os custos de mão de obra e não inclui os custos das estimativas de despesas. 

O PSA usa as fórmulas a seguir para calcular as métricas de acompanhamento:

- Porcentagem de custo consumido = Custo real empenhado até o momento ÷ Custo planejado para a tarefa
- Custo até a conclusão (CTC) = Custo planejado – Custo real empenhado até o momento
- EAT = CTC + Custo real empenhado até o momento
- Variação de custo projetada = Custo planejado – EAT

Uma projeção da variação de custo é exibida na tarefa. Se a EAT for maior do que o custo planejado, a projeção é de que a tarefa custe mais do que foi planejado originalmente. Portanto, está acima do orçamento. Se a EAT for menor do que o custo planejado, a projeção é de que a tarefa custe menos do que foi planejado originalmente. Portanto, está abaixo do orçamento.

## <a name="project-managers-re-projection-of-cost"></a>Reprojeção de custo realizada pelo gerente do projeto

Quando o esforço é reprojetado, CTC, EAT, porcentagem de custo consumido e variação de custo projetada são todos recalculados na exibição **Acompanhamento de custo**.

## <a name="project-status-summary"></a>Resumo de status do projeto

Os dados de acompanhamento nas exibições **Acompanhamento de esforço** e **Acompanhamento de custo** mostram o progresso e o consumo de custo nos níveis do nó raiz, das tarefas de resumo e das tarefas de nó folha. A seção **Status** na página **Entidade de projeto** mostra um resumo do status no nível do projeto.

## <a name="status-summary-fields"></a>Campos do resumo do status

**Status geral do projeto** é um campo editável que mostra o status geral do projeto. Ele usa um código de cores, como verde, amarelo e vermelho, para indicar o aumento do risco. O campo **Comentários** permite ao gerente do projeto inserir comentários específicos sobre o status. O campo **Status atualizado em** não é editável e o valor é um carimbo de data/hora que indica quando o status foi atualizado pela última vez.

Os campos **Desempenho da agenda** e **Desempenho do custo** são definidos a partir da data de acompanhamento. Quando a variação de agenda e de custo para o nó raiz na exibição **Acompanhamento de esforço** for positiva, você poderá definir esses campos como **Adiantado**. Quando a variação de agenda e de custo para o nó raiz for negativa, você poderá defini-los como **Atrasado**.
