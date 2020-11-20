---
title: Andamento do projeto e consumo de custo
description: Este tópico fornece informações sobre como rastrear o progresso do projeto e o consumo de custos.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 08/21/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 0793ee0c75bcbdde0fd92a16634457f73f872b5e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120619"
---
# <a name="project-progress-and-cost-consumption"></a>Andamento do projeto e consumo de custo

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

A necessidade de acompanhar o progresso em relação a uma agenda varia por setor. Alguns setores fazem o acompanhamento em um nível granular, enquanto outros o fazem em um nível superior. Este tópico mostra como fazer agendamentos para atender aos requisitos da sua organização.

## <a name="effort-tracking-view"></a>Exibição de Acompanhamento de Esforço

A exibição **Acompanhamento de esforço** acompanha o progresso de tarefas na agenda. Compara as horas de esforço reais gastas em uma tarefa com as horas de esforço planejado da tarefa. O Project Service Automation usa as fórmulas a seguir para calcular as métricas de acompanhamento:

Inicialmente na criação da tarefa: o Custo planejado será definido como o Custo estimado na conclusão. Assim que os Dados reais forem registrados na tarefa, o seguinte será calculado na exibição Rastreamento para Esforço

- Porcentagem de progresso = Esforço real até o momento ÷ Estimativa na conclusão (EAC) 
- Estimativa até a conclusão (ETC) = Estimativa na conclusão (EAC) - Esforço real empenhado até o momento 
- EAC = Esforço restante + Esforço real empenhado até o momento 
- Variação de esforço projetada = Esforço planejado – EAT

O Project Service Automation mostra uma projeção da variação de esforço na tarefa. Se a EAT for maior do que o esforço planejado, a projeção é de que a tarefa levará mais tempo do que foi planejado originalmente. Portanto, está atrasada. Se a EAT for menor do que o esforço planejado, a projeção é de que a tarefa levará menos tempo do que foi planejado originalmente. Portanto, está adiantada.

## <a name="reprojecting-effort"></a>Reprojetar esforço

É comum que um gerente de projetos revise as estimativas originais em uma tarefa. As reprojeções de projetos são a percepção de um gerente de projetos sobre as estimativas, considerando o estado atual de um projeto. No entanto, não é recomendável que os gerentes de projetos alterem os números da linha de base, pois a linha de base do projeto representa a fonte de referência estabelecida para a estimativa de custo e de agenda dele e todos os participantes do projeto concordaram com ela.

Um gerente de projetos pode reprojetar o esforço em tarefas de duas maneiras:

- Substituindo a ETC padrão por uma nova estimativa do esforço restante real na tarefa. 
- Substituindo a porcentagem de progresso padrão por uma nova estimativa do verdadeiro progresso na tarefa.

Cada uma dessas abordagens causa o recálculo de ETC, EAT, porcentagem de progresso e variação de esforço projetada em uma tarefa. A EAT, a ETC e a porcentagem de progresso nas tarefas de resumo também são recalculadas e produzem uma nova projeção da variação de esforço.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Reprojeção de esforço em tarefas de resumo

O esforço em tarefas de resumo ou de contêiner pode ser reprojetado. Independentemente do usuário reprojetar usando o esforço restante ou a porcentagem de progresso nas tarefas de resumo, o seguinte conjunto de cálculos é iniciado:

- A EAT, a ETC e a porcentagem de progresso na tarefa são calculadas.
- A nova EAT é distribuída até as tarefas filho na mesma proporção em que a EAT original foi distribuída na tarefa.
- A nova EAT em cada uma das tarefas individuais até as tarefas de nó folha é calculada. 
- As tarefas filho afetadas até os nós folha têm sua ETC e porcentagem de progresso recalculadas com base no valor da EAT. Isso resulta em uma nova projeção da variação de esforço da tarefa. 
- As EATs das tarefas de resumo até o nó raiz são recalculadas.

### <a name="cost-tracking-view"></a>Exibição Acompanhamento de custo 

A exibição **Rastreamento do custo** compara o custo real empenhado em uma tarefa com o custo planejado. 

> [!NOTE]
> Essa exibição mostra apenas os custos de mão de obra e não inclui os custos das estimativas de despesas. 

O Project Service Automation usa as fórmulas a seguir para calcular as métricas de acompanhamento:

Quando uma tarefa é criada, o custo planejado é igual ao custo estimado na conclusão. Após o registro de dados reais na tarefa, o seguinte será calculado na exibição **Rastreamento** para custo:

 - Porcentagem de custo consumido = Custo real empenhado até o momento ÷ Custo estimado na conclusão para a tarefa
 - Custo até a conclusão (CTC) = Custo estimado na conclusão – Custo real empenhado até o momento
 - Custo estimado na conclusão = CTC – Custo real empenhado até o momento
 - Variação de custo projetado = Custo planejado - Custo estimado na conclusão

Uma projeção da variação de custo é exibida na tarefa. Se o custo estimado na conclusão for maior do que o custo planejado, a tarefa será projetada para um custo superior ao que foi planejado originalmente. Portanto, está acima do orçamento. Se o Custo estimado na conclusão for menor do que o custo planejado, a tarefa será projetada para um custo inferior ao que foi planejado originalmente e tende a ficar abaixo do orçamento.

## <a name="project-managers-reprojection-of-cost"></a>Reprojeção de custo realizada pelo gerente do projeto

Quando o esforço é reprojetado, o CTC, o Custo estimado na conclusão, a porcentagem de custo consumido e a variação de custo projetado são todos recalculados na exibição **Rastreamento do custo**.

## <a name="project-status-summary"></a>Resumo de status do projeto

Os dados de acompanhamento nas exibições **Acompanhamento de esforço** e **Acompanhamento de custo** mostram o progresso e o consumo de custo nos níveis do nó raiz, das tarefas de resumo e das tarefas de nó folha. A seção **Status** na página **Entidade de projeto** mostra um resumo do status no nível do projeto.

## <a name="status-summary-fields"></a>Campos do resumo do status

**Status geral do projeto** é um campo editável que mostra o status geral do projeto. Ele usa um código de cores, como verde, amarelo e vermelho, para indicar o aumento do risco. O campo **Comentários** permite ao gerente do projeto inserir comentários específicos sobre o status. O campo **Status atualizado em** não é editável e o valor é um carimbo de data/hora que indica quando o status foi atualizado pela última vez.

Os campos **Desempenho da agenda** e **Desempenho do custo** são definidos a partir da data de acompanhamento. Quando a variação de agenda e de custo para o nó raiz na exibição **Acompanhamento de esforço** for positiva, você poderá definir esses campos como **Adiantado**. Quando a variação de agenda e de custo para o nó raiz for negativa, você poderá defini-los como **Atrasado**.
