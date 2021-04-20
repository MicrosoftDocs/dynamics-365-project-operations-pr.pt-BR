---
title: Acompanhamento de vendas do projeto
description: Este tópico fornece informações sobre como o Project Operations rastreia o progresso em relação à receita de mão de obra em um projeto.
author: rumant
manager: AnnBe
ms.date: 03/24/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 438c44dcfaf9677075eb07688c1e65c6e7053755
ms.sourcegitcommit: a1f9f92546ab5d8d8e5a4710ce4c96414ea55d14
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/24/2021
ms.locfileid: "5711021"
---
# <a name="project-sales-tracking"></a>Acompanhamento de vendas do projeto

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

O Dynamics 365 Project Operations rastreia estimativas de mão de obra e receita com a menor granularidade necessária em um plano do projeto. A estimativa de receita da mão de obra é baseada no esforço planejado e nos recursos genéricos ou nomeados que são atribuídos a cada tarefa do nó folha no plano do projeto. Quando o projeto começa e as pessoas relatam o tempo em várias tarefas do projeto, a receita real do trabalho é resumida, iniciando um cálculo das projeções.

## <a name="labor-revenue-tracking-view"></a>Visualização de acompanhamento de receita de mão de obra

Na página **Projetos**, na guia **Acompanhamento**, você pode selecionar **Acompanhamento** > **Custo** para abrir a exibição **Acompanhamento de Custo**. Ou você pode selecionar **Usar** > **Taxa de Cobrança** para abrir a exibição **Acompanhamento de Receita** , que mostra o andamento da receita de mão de obra em cada tarefa no plano do projeto. Essa exibição também compara a receita de mão de obra real gasta em uma tarefa com a receita de mão de obra planejada da tarefa. O Project Operations usa as seguintes fórmulas para calcular métricas de receita de mão de obra:

- **Receita Planejada**: Valores de vendas estimados de todas as atribuições de recursos em cada tarefa do nó folha
- **Receita Real**: Soma de todos os dados reais de vendas não cobradas para o tempo registrado na tarefa
- **% de Receita Cobrável**: Receita real ÷ Estimativa de receita na conclusão
- **Receita Restante**: Estimativa de receita na conclusão – Receita real
- **Receita Estimada na Conclusão**: Receita restante + Receita real
- **Variação de receita**: Receita planejada – Receita estimada na conclusão


> [!NOTE]
> O Project Operations mostra apenas as receitas de mão de obra na página **Projeto** na guia **Acompanhamento**. Embora os materiais e despesas possam ser estimados e rastreados para consumo, essas receitas não estão incluídas nas receitas mostradas na guia **Acompanhamento**. Esta guia foi projetada para funcionar apenas para reprojetar receitas de mão de obra por meio de esforço de reprojeção.  
> Todos os valores de receita mostrados são convertidos na moeda de custo do projeto. A moeda do custo do projeto é a moeda da unidade contratante no projeto. Para projetos de preço fixo, os números de receita na exibição **Acompanhamento de receita de mão de obra** não são relevantes porque dados reais de vendas não cobradas não são registrados na aprovação de tempo.
> Os valores de vendas estimados para o tempo que aparecem na guia **Estimativa** do projeto podem não ser adicionados ao valor da receita planejada na guia **Acompanhamento**. Há duas razões possíveis para esta discrepância:
><ol>
   ><li> A guia <b>Estimativas</b> mostra a receita estimada na moeda de vendas, enquanto a guia <b>Acompanhamento</b> mostra a receita planejada convertida na moeda de custo. </li>
   ><li> Quando as vendas estimadas são convertidas na moeda do contrato, conforme mostrado na guia <b>Estimativas</b>, para a moeda do projeto, a conversão envolve etapas que podem resultar em perda de precisão: </li>
><ol>
><li> O valor de vendas estimadas na moeda de contrato é primeiro convertido na moeda base (conversão 1).</li>
><li> O valor de vendas estimadas na moeda base é convertido na moeda de custo do projeto (conversão 2). </li>
></ol>
></ol>
> A precisão da moeda é aplicada em ambas as etapas, o que resulta em um desvio da receita planejada na moeda do projeto a partir das vendas planejadas na moeda do contrato.
   

## <a name="reprojecting-revenues-on-leaf-node-tasks"></a>Reprojetar receitas em tarefas de nó folha

As receitas de mão de obra em uma tarefa de nó folha não podem ser reprojetadas diretamente na guia **Acompanhamento** na página **Projeto**. Mas, você pode usar a exibição **Acompanhamento de Esforço** para reprojetar o esforço restante em uma tarefa. Isso causa um recálculo da receita restante na tarefa. A seguir está uma descrição de como isso funciona.

1. Um gerente de projeto pode reprojetar o esforço em tarefas, atualizando o valor padrão no campo **Esforço Restante** com uma nova estimativa do esforço restante na tarefa. A reprojeção causa um recálculo de estimativa até a conclusão (EAC) de esforço da tarefa, porcentagem de progresso e variação de esforço projetada em uma tarefa. A EAC, a ETC (estimativa até a conclusão) e a porcentagem de progresso nas tarefas de resumo também são recalculadas e geram uma nova projeção da variação de esforço.
2. Com base no novo valor para o esforço restante na tarefa, o sistema calcula a receita restante na exibição **Acompanhamento de Receita**. Para calcular a receita restante com base no esforço restante, o sistema primeiro calcula a receita média de uma hora de esforço na tarefa como receita planejada ou esforço planejado. A receita planejada é a soma da receita de todas as atribuições de recursos na tarefa. A receita média por hora é usada para calcular a receita restante do esforço restante recém-projetado na tarefa.
3. A receita estimada na conclusão e a porcentagem de consumo da receita na tarefa do nó folha são recalculadas.
4. A receita no valor total das tarefas de resumo até o nó raiz é recalculada.

## <a name="reprojecting-revenues-on-summary-tasks"></a>Reprojetar receitas em tarefas de resumo

Você pode reprojetar receita de mão de obra em tarefas de resumo ou tarefas de contêiner. Mas não é possível reprojetar diretamente as receitas de mão de obra em uma tarefa de projeto de resumo na guia **Acompanhamento** na página **Projeto**. Semelhante às tarefas de nó folha, a reprojeção de tarefas de resumo e contêiner pode ser feita usando a exibição **Acompanhamento de Esforço**. Nesta exibição, você pode reprojetar o esforço restante em uma tarefa de resumo, causando um recálculo da receita restante na tarefa de resumo. A seguir está uma descrição de como isso funciona.

1. Um gerente de projeto pode reprojetar o esforço em tarefas, atualizando o valor padrão no campo **Esforço Restante** com uma nova estimativa do **Esforço Restante** na tarefa. A reprojeção causa um recálculo de estimativa até a conclusão (EAC) da tarefa, porcentagem de progresso e variação de esforço projetada em uma tarefa. A EAC, a ETC e a porcentagem de progresso nas tarefas de resumo também são recalculadas e produzem uma nova projeção da variação de esforço.
2. Com base no novo valor no campo **Esforço restante** na tarefa, o sistema calcula a receita restante na exibição **Acompanhamento de Receita**. Para calcular a receita restante com base no esforço restante, o sistema primeiro calcula a receita média de uma hora de esforço na tarefa como receita planejada ou esforço planejado. A receita planejada é a soma da receita de todas as atribuições de recursos na tarefa. Esta receita média por hora é usada para calcular a receita do esforço restante recém-projetado na tarefa.
3. A receita estimada na conclusão e as porcentagens de consumo da receita na tarefa de resumo são recalculadas.
4. O novo valor da receita estimada na conclusão é distribuído até as tarefas filho na mesma proporção que a receita planejada original na tarefa.
5. A nova receita estimada na conclusão em cada uma das tarefas individuais até as tarefas de nó folha é calculada. Com base nesse valor, as tarefas filho afetadas até os nós folha terão a receita restante e a porcentagem de consumo de receita recalculadas com base no valor da receita na conclusão. Isso resulta em uma nova projeção da variação de receita da tarefa. 
6. A receita no valor total das tarefas de resumo até o nó raiz é recalculada.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

