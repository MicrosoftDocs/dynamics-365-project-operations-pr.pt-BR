---
title: Acompanhamento de custo do projeto
description: Este tópico fornece informações sobre como o Project Operations rastreia o progresso em relação ao custo de mão de obra e gastos em um projeto.
author: rumant
manager: AnnBe
ms.date: 03/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 28cb692c61ae4137a28973dc1bd70ffd989dd535
ms.sourcegitcommit: a1f9f92546ab5d8d8e5a4710ce4c96414ea55d14
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/24/2021
ms.locfileid: "5711020"
---
# <a name="labor-cost-tracking-on-projects"></a>Acompanhamento de custos de mão de obra em projetos

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

O Dynamics 365 Project Operations rastreia estimativas de mão de obra e gastos com a menor granularidade necessária no plano do projeto. A estimativa financeira do custo da mão de obra é baseada no esforço planejado e nos recursos genéricos ou nomeados que são atribuídos a cada tarefa do nó folha no plano do projeto. Quando o projeto começa e as pessoas relatam o tempo em várias tarefas do projeto, o gasto real do trabalho é resumido, iniciando um cálculo das projeções.

## <a name="labor-cost-tracking-view"></a>Exibição Acompanhamento de custos de mão de obra

Na página **Projetos**, na guia **Acompanhamento**, você pode selecionar **Acompanhamento** > **Custo** para abrir a exibição **Acompanhamento de Custos** e ver o andamento da mão de obra gasta em cada tarefa no plano do projeto. Essa exibição também compara o custo de mão de obra real gasto em uma tarefa com o custo de mão de obra planejado da tarefa. O Project Operations usa as seguintes fórmulas para calcular métricas de custo de mão de obra:

- **Custo planejado**: Custo estimado de todas as atribuições de recursos em cada tarefa do nó folha
- **Custo real**: Soma de todos os custos reais para o tempo registrado na tarefa
- **Porcentagem de consumo de custo**: Custo real ÷ Estimativa de custo completa
- **Custo restante**: Estimativa de custo completa – Custo real
- **Custo até a conclusão**: Custo restante + Custo real
- **Variação de custo**: Custo planejado – Estimativa de custo completa

Cada tarefa mostra uma projeção da variação de custo na tarefa. Se a estimativa de custo completa for maior do que o custo planejado, a tarefa será projetada para ultrapassar o orçamento. Se a estimativa de custo completa for menor do que o custo planejado, a tarefa será projetada para terminar dentro do orçamento.

>[!NOTE]
> O Project Operations mostra apenas os custos de mão de obra na página **Projeto** na guia **Acompanhamento**. Embora os materiais e despesas possam ser estimados e rastreados para consumo, esses custos não estão incluídos nos custos mostrados na guia **Acompanhamento**. Esta guia foi projetada para funcionar apenas para reprojetar custos de mão de obra por meio de esforço de reprojeção.
Todos os valores de custo mostrados são convertidos na moeda de custo do projeto a partir da moeda do preço de custo do projeto usada para determinar a taxa de custo. A moeda do custo do projeto é a moeda da unidade contratante no projeto. Os valores de custo estimado para tempo que são mostrados na guia **Estimativas** na página **Projeto** podem não ser adicionados ao custo planejado na guia **Acompanhamento**. A razão dessa discrepância são as diferenças em como o custo estimado é resumido na grade **Estimativas** e como o custo planejado é calculado na grade **Acompanhamento**. 
>
> - A guia **Estimativas** calcula o custo estimado usando a mesma moeda da taxa de custo na lista de preços. O custo estimado na moeda da lista de preços é convertido no custo estimado na moeda de custo do projeto. O custo estimado na moeda do projeto é arredondado para 2 casas decimais. Em nenhum ponto dessa conversão a precisão da moeda é aplicada. 
> - Na guia **Acompanhamento**, o cálculo do custo planejado segue uma ordem de cálculo ligeiramente diferente que envolve a aplicação da precisão da moeda em dois estágios: 
   ><ol>
   ><li>O valor do custo estimado na moeda da lista de preços é convertido na moeda base (conversão 1).</li>
   ><li>O valor do custo estimado na moeda base é convertido na moeda de custo do projeto (conversão 2). </li>
   ></ol>
   >A precisão da moeda é aplicada em ambas as etapas para obter um custo planejado (na guia **Acompanhamento**) que se desvia um pouco do custo estimado (na exibição **Tempo - em fases** na guia **Estimativas**). 
   
## <a name="reprojecting-costs-on-leaf-node-tasks"></a>Reprojetar custos em tarefas de nó folha

Os custos de mão de obra em uma tarefa de nó folha não podem ser reprojetados diretamente na guia **Acompanhamento** na página **Projeto**. Mas, você pode usar a exibição **Acompanhamento de Esforço** para reprojetar o esforço restante em uma tarefa. Isso causa um recálculo do custo restante na tarefa. A seguir está uma descrição de como isso funciona.

1. Um gerente de projeto pode reprojetar o esforço em tarefas, atualizando o valor padrão no campo **Esforço Restante** com uma nova estimativa do esforço restante na tarefa. A reprojeção causa um recálculo de estimativa até a conclusão (EAC) de esforço da tarefa, porcentagem de progresso e variação de esforço projetada em uma tarefa. A EAC, a ETC (estimativa até a conclusão) e a porcentagem de progresso nas tarefas de resumo também são recalculadas e geram uma nova projeção da variação de esforço.
2. Com base no novo valor para o esforço restante na tarefa, o sistema calcula o custo restante na exibição **Acompanhamento de Custos**. Para calcular o custo restante com base no esforço restante, o sistema primeiro calcula o custo médio de uma hora de esforço na tarefa como custo planejado ou esforço planejado. O custo planejado é a soma do custo de todas as atribuições de recursos na tarefa. O custo médio por hora é usado para calcular o custo restante do esforço restante recém-projetado na tarefa.
3. O custo na conclusão e a porcentagem de consumo de custo na tarefa do nó folha são recalculados.
4. O custo no valor total das tarefas de resumo até o nó raiz é recalculado.

## <a name="reprojecting-costs-on-summary-tasks"></a>Reprojetar custos em tarefas de resumo

Você pode reprojetar custos de mão de obra em tarefas de resumo ou tarefas de contêiner. Mas não é possível reprojetar diretamente o custo de mão de obra em uma tarefa de projeto de resumo na guia **Acompanhamento** na página **Projeto**. Semelhante às tarefas de nó folha, a reprojeção de tarefas de resumo e contêiner pode ser feita usando a exibição **Acompanhamento de Esforço**. Nesta exibição, você pode reprojetar o esforço restante em uma tarefa de resumo, causando um recálculo do custo restante na tarefa de resumo. A seguir está uma descrição de como isso funciona.

1. Um gerente de projeto pode reprojetar o esforço em tarefas de resumo, atualizando o valor padrão do esforço restante com uma nova estimativa na tarefa. Essa atualização causa um recálculo de estimativa até a conclusão (EAC) da tarefa de resumo, porcentagem de progresso e variação de esforço projetada em uma tarefa. A EAC, a ETC e a porcentagem de progresso nas tarefas de resumo também são recalculadas e produzem uma nova projeção da variação de esforço.
2. Com base no novo valor para o esforço restante na tarefa de resumo, o sistema calcula o custo restante na exibição **Acompanhamento de Custos**. Para calcular o custo restante com base no esforço restante, o sistema primeiro calcula o custo médio de uma hora de esforço na tarefa de resumo como custo planejado ou esforço planejado. O custo médio por hora é usado para calcular o custo do esforço restante recém-projetado na tarefa de resumo.
3. O custo na conclusão e a porcentagem de consumo de custo na tarefa de resumo do nó folha são recalculados.
4. O novo custo na conclusão é distribuído até as tarefas filho na mesma proporção que o custo planejado original na tarefa.
5. O valor do novo custo na conclusão em cada uma das tarefas individuais até as tarefas de nó folha é calculado. Com base nesse valor, as tarefas filho afetadas até os nós folha terão o custo restante e a porcentagem de consumo de custo recalculados com base no valor do custo na conclusão. Esse valor resulta em uma nova projeção da variação de custo da tarefa. 


O campo **Desempenho de custo** pode ser definido a partir dos dados de acompanhamento. Quando a variação de custo do nó raiz na exibição **Acompanhamento de custos** é negativa, você pode definir este campo como **Abaixo do Orçamento**. Quando a variação de custo do nó raiz é positiva, você pode definir o valor como **Acima do Orçamento**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
