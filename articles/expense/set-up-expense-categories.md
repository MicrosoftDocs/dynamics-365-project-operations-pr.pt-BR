---
title: Configurar categorias de despesa
description: Este tópico fornece informações sobre como configurar categorias de despesas e categorias compartilhadas para relatórios de despesas.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: f051d70f3dfe3b241dc0a206c0cdfda000f87c76
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071318"
---
# <a name="set-up-expense-categories"></a>Configurar categorias de despesa

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Quando os funcionários criam relatórios de despesas, cada despesa que eles registram deve ser associada a uma categoria de despesas. As categorias de despesas são derivadas de categorias compartilhadas que podem ser compartilhadas entre as entidades legais em sua organização. Dependendo de como sua organização é definida, essas categorias de despesas também podem ser compartilhadas em outras áreas. Com base na definição da sua organização e orientação da equipe de implementação, você deverá determinar se as categorias que são usadas no gerenciamento de despesas serão usadas apenas no gerenciamento de despesas ou se deverão ser compartilhadas em outras áreas.

> [!NOTE]
> Essas categorias podem ser compartilhadas entre Gerenciamento e contabilidade do projeto e Gerenciamento de despesas, ou entre Gerenciamento e contabilidade do projeto e Produção. No entanto, elas não podem ser compartilhadas entre Gerenciamento de despesas e Produção.

Antes de iniciar o processo de configuração, as seguintes decisões deverão ser tomadas para cada categoria de despesas:

- Qual é a categoria da despesa? Os exemplos incluem categorias para voos, hotel ou milhagem.
- A categoria de despesas também pode ser usada no Gerenciamento e contabilidade de projeto? Se a respostas for positiva, você também precisará tomar as seguintes decisões:

    - Quais contas de custo serão usadas para as despesas a seguir?

        - Custo
        - Alocação de folha de pagamento
        - WIP – Valor de custo
        - Custo – Item
        - WIP – Valor de custo – Item
        - Perda acumulada
        - WIP – Perda acumulada

    - Quais contas de receita serão usadas para as fontes de receita a seguir?

        - Receita faturada
        - Receita acumulada - Valor de venda
        - WIP – Valor de venda
        - Receita acumulada – Produção
        - WIP – Produção
        - Receita acumulada – Lucro
        - WIP – Lucro
        - Receita acumulada – Subscrição
        - WIP – Subscrição

- Qual é o tipo de despesa?
- Qual é a forma de pagamento padrão para a categoria de despesas?
- As despesas na categoria de despesas devem ser discriminadas?
- Qual é a conta principal padrão para a categoria de despesas?
- Qual é o grupo de impostos do item padrão para a categoria de despesas?
- São permitidas formas de pagamento adicionais para a categoria de despesas? Em caso afirmativo, quais são elas?
- Existem subcategorias nesta categoria de despesas? Se houver subcategorias, você também precisará tomar as seguintes decisões:

    - Alguma das subcategorias foi excluída da recuperação de impostos?
    - Qual é o grupo de impostos do item das subcategorias?
