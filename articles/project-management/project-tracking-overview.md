---
title: Visão geral do acompanhamento de projeto
description: Este tópico fornece informações sobre como acompanhar o consumo de custo e o progresso do projeto.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: f159ecac53b824ef208221bb14958923fb5da63b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127325"
---
# <a name="project-tracking-overview"></a>Visão geral do acompanhamento de projeto

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

A necessidade de acompanhar o progresso em relação a uma agenda varia por setor. Alguns setores fazem o acompanhamento em um nível granular, enquanto outros o fazem em um nível superior. Este tópico mostra como fazer agendamentos para atender aos requisitos da sua organização.

## <a name="effort-tracking-view"></a>Exibição de Acompanhamento de Esforço

A exibição de **Acompanhamento de Esforço** acompanha o progresso das tarefas na agenda comparando as horas de esforço reais gastas em uma tarefa com as horas de esforço planejadas para a tarefa. O Dynamics 365 Project Operations usa as fórmulas a seguir para calcular as métricas de acompanhamento:

- **Porcentagem de progresso**: Esforço real até o momento ÷ Estimativa na conclusão (EAC) 
- **Estimativa até a conclusão (ETC)**: Esforço planejado – Esforço real empenhado até o momento 
- **EAC**: Esforço restante + Esforço real empenhado até o momento 
- **Variação de esforço projetada**: Esforço planejado – EAC

O Project Operations mostra uma projeção da variação de esforço na tarefa. Se a EAC for maior do que o esforço planejado, a projeção é de que a tarefa levará mais tempo do que foi planejado e está atrasada. Se a EAC for menor do que o esforço planejado, a projeção é de que a tarefa levará menos tempo do que foi planejado e está adiantada.

## <a name="reprojecting-effort"></a>Reprojetar esforço

Os gerentes de projeto frequentemente revisam as estimativas originais em uma tarefa. As reprojeções de projetos são a percepção de um gerente de projetos sobre as estimativas, considerando o estado atual de um projeto. No entanto, não recomendamos que os gerentes de projeto alterem os números da linha de base. Isso ocorre porque a linha de base do projeto representa a fonte de referência estabelecida para a estimativa de custo e de agenda dele e todos os participantes do projeto concordaram com ela.

Um gerente de projetos pode reprojetar o esforço em tarefas de duas maneiras:

- Substituindo a ETC padrão por uma nova estimativa do esforço restante real na tarefa. 
- Substituindo a porcentagem de progresso padrão por uma nova estimativa do verdadeiro progresso na tarefa.

Cada abordagem causa o recálculo da ETC, EAC, porcentagem de progresso e variação de esforço projetada em uma tarefa. A EAC, a ETC e a porcentagem de progresso nas tarefas de resumo também são recalculadas e produzem uma nova projeção da variação de esforço.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Reprojeção de esforço em tarefas de resumo

O esforço em tarefas de resumo ou de contêiner pode ser reprojetado. Independentemente do usuário reprojetar usando o esforço restante ou a porcentagem de progresso nas tarefas de resumo, o seguinte conjunto de cálculos é iniciado:

- A EAT, a ETC e a porcentagem de progresso na tarefa são calculadas.
- A nova EAT é distribuída até as tarefas filho na mesma proporção em que a EAT original foi distribuída na tarefa.
- A nova EAT em cada uma das tarefas individuais até as tarefas de nó folha é calculada. 
- As tarefas filho afetadas até os nós folha têm sua ETC e porcentagem de progresso recalculadas com base no valor da EAT. Isso resulta em uma nova projeção da variação de esforço da tarefa. 
- As EATs das tarefas de resumo até o nó raiz são recalculadas.

### <a name="cost-tracking-view"></a>Exibição Acompanhamento de custo 

A exibição **Acompanhamento de custo** compara o custo real empenhado em uma tarefa com o custo planejado para essa tarefa. 

> [!NOTE]
> Essa exibição mostra apenas os custos de mão de obra e não inclui os custos das estimativas de despesas. O Project Operations usa as fórmulas a seguir para calcular as métricas de acompanhamento:

- **Porcentagem de custo consumido**: Custo real empenhado até o momento ÷ Custo estimado na conclusão
- **Custo até a conclusão (CTC)**: Custo planejado – Custo real empenhado até o momento
- **EAC**: Custo restante + Soma do custo real gasto até a data
- **Variação de custo projetada**: Custo planejado – EAC

Uma projeção da variação de custo é exibida na tarefa. Se a EAT for maior do que o custo planejado, a projeção é de que a tarefa custe mais do que foi planejado originalmente. Portanto, está acima do orçamento. Se a EAT for menor do que o custo planejado, a projeção é de que a tarefa custe menos do que foi planejado originalmente. Portanto, está abaixo do orçamento.

## <a name="project-managers-reprojection-of-cost"></a>Reprojeção de custo realizada pelo gerente do projeto

Quando o esforço é reprojetado, CTC, EAT, porcentagem de custo consumido e variação de custo projetada são todos recalculados na exibição **Rastreamento de custo**.

## <a name="project-status-summary"></a>Resumo de status do projeto

Os dados de acompanhamento nas exibições **Acompanhamento de esforço** e **Acompanhamento de custo** mostram o progresso e o consumo de custo nos níveis do nó raiz, das tarefas de resumo e das tarefas de nó folha. A seção **Status** na página **Entidade de projeto** mostra um resumo do status no nível do projeto.

## <a name="status-summary-fields"></a>Campos do resumo do status

**Status geral do projeto** é um campo editável que mostra o status geral do projeto. Ele usa um código de cores, como verde, amarelo e vermelho, para indicar o aumento do risco. O campo **Comentários** permite ao gerente do projeto inserir comentários específicos sobre o status. O campo **Status atualizado em** não é editável e o valor é um carimbo de data/hora que indica quando o status foi atualizado pela última vez.

Os campos **Desempenho da agenda** e **Desempenho do custo** são definidos a partir da data de acompanhamento. Quando a variação de agenda e de custo para o nó raiz na exibição **Acompanhamento de esforço** for positiva, você poderá definir esses campos como **Adiantado**. Quando a variação de agenda e de custo para o nó raiz for negativa, você poderá defini-los como **Atrasado**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]