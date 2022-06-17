---
title: Estimativas financeiras para materiais em projetos
description: Este artigo fornece informações sobre como definir ou estimar materiais baseados em projeto.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: eb33c8e2ead2a558bf53256095645011212ff343
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925665"
---
# <a name="financial-estimates-for-materials-on-projects"></a>Estimativas financeiras para materiais em projetos

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

O Dynamics 365 Project Operations permite que os gerentes de Projeto definam custos de materiais baseadas em projeto para cada projeto ou tarefa. Cada estimativa de material pode ser associada a uma tarefa específica do projeto. Os materiais usados em projetos podem ser produtos fora do catálogo ou produtos do catálogo de produtos. Para cada combinação de produto e unidade, um preço pode ser definido nas listas de preços do projeto para vendas e nas listas de preços do projeto para custo.  

Conclua as etapas a seguir para visualizar, adicionar ou excluir uma estimativa de material do projeto.

1. Vá para **Projetos** e selecione o projeto que deseja atualizar.
2. Na guia **Estimativas de Materiais**, veja a lista de estimativas de materiais do projeto.
3. Selecione **Estimativa de novo material** para criar uma nova estimativa de material. Ou selecione uma estimativa de material para excluir e, em seguida, selecione **Excluir Estimativa de Material**.

A tabela a seguir fornece informações sobre os campos na página **Linha de Estimativa de material** em um projeto. 

| **Campo** | **Descrição** | **Impacto a jusante** |
| --- | --- | --- |
| Tarefa | Uma lista de tarefas no projeto. Isso inclui tarefas de resumo e nó folha. | Quando você seleciona uma tarefa para uma linha de estimativa de material, o custo de material estimado e as vendas de material estimadas para uma tarefa são afetados. Se este campo for deixado em branco, a estimativa de material será rastreada e resumida apenas no nível do projeto. |
| Selecionar Produto |  É possível especificar se a linha de estimativa é para um produto existente (catálogo) ou um produto fora do catálogo. | Este campo determina se você seleciona um produto do catálogo ou fora do catálogo do produto. |
| Produto | O ID do produto do catálogo de produtos. Quando você seleciona uma ID de produto o valor no campo **Selecionar Produto** é atualizado automaticamente para **Produto existente**. A ID é usada para recuperar os preços de custo e venda da lista de preços. | Não há impacto posterior para esse campo. |
| Descrição do Produto Fora do Catálogo | Um campo de texto para escrever o nome do produto. Este campo deve ser usado quando **Fora do catálogo** é selecionado no campo **Selecionar Produto**.| Não há impacto posterior para esse campo. |
| Data de Início | A data prevista em que se espera que o material seja usado. | Não há impacto posterior para esse campo. |
| Grupo de unidades | O valor padrão neste campo é obtido do grupo de unidades padrão no produto do catálogo. Você pode atualizar este campo para selecionar outro grupo de unidades. | Não há impacto posterior para esse campo. |
| Unidade | O valor padrão neste campo é derivado da unidade padrão do produto selecionado. Você pode atualizar este campo para selecionar outra unidade. | Alterar a unidade resulta em um preço e custo unitário padrão diferente. |
| Quantidade | A quantidade estimada do produto que será utilizada no projeto. | Não há impacto posterior para esse campo. |
| Custo Unitário | O custo unitário da combinação de produto e unidade selecionados, conforme configurado na lista de preços de custo aplicável. | O custo unitário é sempre mostrado na moeda de custo do projeto. Se não houver configuração de custo unitário para a configuração de produto e unidade na lista de preços, o custo unitário padrão será de 0,00. |
| Preço Unitário | O preço da combinação de produto e unidade selecionados, conforme configurado na lista de preços de vendas aplicável. | O preço unitário é sempre mostrado na moeda de vendas do projeto. Se não houver configuração de preço unitário para a configuração de produto e unidade na lista de preços, o preço unitário padrão será de 0,00.|
| Custo Total | O valor do custo que é calculado como quantidade\*custo unitário.| O valor de custo é sempre mostrado na moeda de custo do projeto. |
| Total de Vendas | O valor de vendas que é calculado como quantidade\*preço unitário. | O valor de vendas é sempre mostrado na moeda de vendas do projeto. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
