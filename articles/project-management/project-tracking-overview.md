---
title: Acompanhamento do esforço do projeto
description: Este tópico fornece informações sobre como acompanhar o esforço do projeto e o progresso do trabalho.
author: ruhercul
ms.date: 03/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3fdf7787f0144dace84852a0442406085bdc1639
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010862"
---
# <a name="project-effort-tracking"></a>Acompanhamento do esforço do projeto

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

A necessidade de acompanhar o progresso em relação a uma agenda varia por setor. Alguns setores fazem o acompanhamento em um nível granular, enquanto outros o fazem em um nível superior. Este tópico mostra como fazer agendamentos para atender aos requisitos da sua organização.

## <a name="effort-tracking-view"></a>Exibição de Acompanhamento de Esforço

A exibição de **Acompanhamento de Esforço** acompanha o progresso das tarefas na agenda comparando as horas de esforço reais gastas em uma tarefa com as horas de esforço planejadas para a tarefa. O Dynamics 365 Project Operations usa as fórmulas a seguir para calcular as métricas de acompanhamento:

- **Porcentagem de progresso**: Esforço real até o momento ÷ Estimativa na conclusão (EAC) 
- **Esforço Restante**: estimativa de esforço ao término – esforço real até o momento 
- **EAC**: Esforço restante + Esforço real empenhado até o momento 
- **Variação de esforço projetada**: Esforço planejado – EAC

O Project Operations mostra uma projeção da variação de esforço na tarefa. Se a EAC for maior do que o esforço planejado, a projeção é de que a tarefa levará mais tempo do que foi planejado e está atrasada. Se a EAC for menor do que o esforço planejado, a projeção é de que a tarefa levará menos tempo do que foi planejado e está adiantada.

## <a name="reprojecting-effort-on-leaf-node-tasks"></a>Reprojetar esforço em tarefas de nó folha

Os gerentes de projeto frequentemente revisam as estimativas originais em uma tarefa. As reprojeções de projetos são a percepção de um gerente de projetos sobre as estimativas, considerando o estado atual de um projeto. No entanto, não recomendamos que os gerentes de projeto alterem os números de esforço planejado. Isso ocorre porque o esforço planejado do projeto representa a fonte de verdade estabelecida para o cronograma do projeto e a estimativa de custo. Todos os participantes do projeto concordaram com isso.

Um gerente de projeto pode reprojetar o esforço em tarefas, atualizando o **Esforço Restante** padrão com uma nova estimativa da tarefa. Essa atualização causa um recálculo de estimativa até a conclusão (EAC) da tarefa, porcentagem de progresso e variação de esforço projetada em uma tarefa. A EAC, a ETC e a porcentagem de progresso nas tarefas de resumo também são recalculadas e produzem uma nova projeção da variação de esforço.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Reprojeção de esforço em tarefas de resumo

O esforço em tarefas de resumo ou de contêiner pode ser reprojetado. Os gerentes de projeto podem atualizar o esforço restante nas tarefas de resumo. Atualizar o esforço restante aciona o seguinte conjunto de cálculos no aplicativo:

- A EAC e a porcentagem de progresso na tarefa são calculadas.
- A nova EAT é distribuída até as tarefas filho na mesma proporção em que a EAT original foi distribuída na tarefa.
- A nova EAT em cada uma das tarefas individuais até as tarefas de nó folha é calculada. 
- As tarefas filho afetadas até os nós folha têm a porcentagem de esforço restante e progresso recalculadas com base no valor da EAC. Isso resulta em uma nova projeção da variação de esforço da tarefa. 
- As EATs das tarefas de resumo até o nó raiz são recalculadas.


## <a name="project-status-summary"></a>Resumo de status do projeto

Os dados de acompanhamento nas exibições **Acompanhamento de esforço** e **Acompanhamento de custo** mostram o progresso e o consumo de custo nos níveis do nó raiz, das tarefas de resumo e das tarefas de nó folha. A seção **Status** na página **Entidade de projeto** mostra um resumo do status no nível do projeto.

## <a name="status-summary-fields"></a>Campos do resumo do status

**Status geral do projeto** é um campo editável que mostra o status geral do projeto. Ele usa um código de cores, como verde, amarelo e vermelho, para indicar o aumento do risco. O campo **Comentários** permite ao gerente do projeto inserir comentários específicos sobre o status. O campo **Status atualizado em** não é editável e o valor é um carimbo de data/hora que indica quando o status foi atualizado pela última vez.

Os campos **Desempenho da agenda** e **Desempenho do custo** são definidos a partir da data de acompanhamento. Quando a variação de agenda e de custo para o nó raiz na exibição **Acompanhamento de esforço** for positiva, você poderá definir esses campos como **Adiantado**. Quando a variação de agenda e de custo para o nó raiz for negativa, você poderá defini-los como **Atrasado**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
