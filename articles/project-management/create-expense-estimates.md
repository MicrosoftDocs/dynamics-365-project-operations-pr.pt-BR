---
title: Estimativas financeiras para despesas em projetos
description: Este tópico fornece informações sobre como definir ou estimar despesas baseadas em projetos.
author: rumant
manager: Annbe
ms.date: 03/19/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ad4901b1264289f1da881154bc147fc3f8da698f
ms.sourcegitcommit: 386921f44f1e9a8a828b140206d52945de07aee7
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "5701768"
---
# <a name="financial-estimates-for-expenses-on-projects"></a>Estimativas financeiras para despesas em projetos
_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

O Dynamics 365 Project Operations permite que os gerentes de Projeto definam despesas baseadas em projeto para cada projeto ou tarefa. Cada item de despesa pode ser associado a uma tarefa específica do projeto. As despesas são categorizadas em diferentes categorias de despesas, que são definidas no nível organizacional. O preço e o custo de cada categoria de despesas são definidos na lista de preços. 

Execute as seguintes etapas para exibir, adicionar ou excluir uma despesa de projeto.

1. Vá para **Projetos** e selecione o projeto no qual deseja trabalhar.
2. Selecione a guia **Estimativas de Projeto** e exiba a lista de despesas do projeto.
3. Selecione **Nova Despesa** para adicionar uma despesa. Ou, selecione uma despesa a ser excluída e, em seguida, selecione **Excluir Despesa**.

A tabela a seguir fornece informações sobre os campos na página **Linha de Estimativa de despesa** em um Projeto. 

| **Campo** | **Descrição** | **Impacto a jusante** |
| --- | --- | --- |
| Tarefa | Uma lista de tarefas no projeto. Isso inclui tarefas de resumo e nó folha. | Selecionar uma tarefa para uma linha de estimativa de despesas afetará o custo de despesas estimado e as vendas de despesas estimadas para uma tarefa. Se este campo for deixado em branco, a estimativa de despesas será rastreada e resumida apenas no nível do projeto. |
| Categoria | Uma lista de categorias de transação que possuem categorias de despesas vinculadas no aplicativo. | A seleção de uma categoria direciona os preços e custos na linha de estimativa de despesas. |
| Data de Início | A data prevista em que a despesa ocorrerá. | Não há impacto posterior para este campo. |
| Grupo de unidades | O valor padrão neste campo é obtido do grupo de unidades configurado como o padrão na categoria selecionada. Você pode atualizar este campo para selecionar outro grupo de unidades. | Não há impacto posterior para este campo. |
| Unidade | O valor neste campo é padronizado para a unidade padrão da categoria selecionada. Você pode atualizar este campo para selecionar outra unidade. | Alterar a unidade resulta em um preço e custo unitário padrão diferente. |
| Quantidade | A quantidade da despesa estimada em que você incorrerá. | Não há impacto posterior para este campo. |
| Custo Unitário | O custo da combinação de categoria selecionada e unidade, conforme configurado na lista de preços de custo aplicável | O custo unitário é sempre mostrado na moeda de custo do projeto. |
| Preço Unitário | O preço da combinação de categoria e unidade selecionada, conforme configurado na lista de preços de vendas aplicável. | O preço unitário é sempre mostrado na moeda de vendas do projeto. |
| Custo Total | O valor do custo que é calculado como quantidade\*custo unitário.| O valor de custo é sempre mostrado na moeda de custo do projeto. |
| Total de Vendas | O valor de vendas que é calculado como quantidade\*preço unitário. | O valor de vendas é sempre mostrado na moeda de vendas do projeto. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
