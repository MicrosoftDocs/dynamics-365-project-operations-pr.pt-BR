---
title: Resolver preços de venda para estimativas e dados reais - lite
description: Este tópico fornece informações sobre como resolver preços de venda em estimativas e reais.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 92cebbe851c3cface86d0580e7e060134295e8c2
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176732"
---
# <a name="resolve-sales-prices-for-estimates-and-actuals---lite"></a>Resolver preços de venda para estimativas e dados reais - lite

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

Quando os preços de venda em estimativas e reais são resolvidos no Dynamics 365 Project Operations, o sistema primeiro usa a data e a moeda da cotação de projeto ou contrato relacionado para resolver a lista de preços de venda. Depois que a lista de preços de venda é resolvida, o sistema resolve a taxa de vendas ou cobrança.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-time"></a>Resolver as taxas de venda em linhas reais e estimadas para tempo

No Project Operations, as linhas de estimativa de tempo são usadas para denotar a linha de cotação e os detalhes da linha de contrato de tempo e as atribuições de recursos no projeto.

Depois que uma lista de preços para vendas é resolvida, o sistema conclui as seguintes etapas para padronizar a taxa de cobrança.

1. O sistema usa os campos **Função** e **Unidade de Recursos** na linha de estimativa para tempo para corresponder às linhas de preço da função na lista de preços resolvidos. Essa correspondência pressupõe que as dimensões de precificação prontas para uso para taxas de cobrança estão sendo usadas. Se você configurou o preço com base em qualquer outro campo em vez de, ou além de **Função** e **Unidade de Recursos**, essa é a combinação que será usada para recuperar uma linha de preço de função correspondente.
2. Se o sistema encontrar uma linha de preço de função que tenha uma taxa de cobrança para a combinação dos campos **Função** e **Unidade de Recursos**, essa taxa de cobrança assumirá o padrão.
3. Se o sistema não corresponder aos valores de campo **Função** e **Unidade de Recursos**, então irá recuperar as linhas de preço da função com uma função correspondente, mas os valores nulos da **Unidade de Recursos**. Depois que o sistema encontrar um registro de preço de função correspondente, ele assumirá como padrão a taxa de cobrança desse registro. Essa correspondência pressupõe uma configuração pronta para uso para a prioridade relativa de **Função** em comparação a **Unidade de Recursos** como uma dimensão de preço de venda.

> [!NOTE]
> Se você configurou uma priorização diferente de **Função** e **Unidade de Recursos**, ou se tiver outras dimensões com prioridade mais alta, esse comportamento será devidamente alterado. O sistema recupera registros de preço de função com valores que correspondem a cada um dos valores de dimensão de precificação em ordem de prioridade com linhas que possuem valores nulos para as dimensões que vêm por último.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Resolver as taxas de venda em linhas reais e estimadas para despesa

No Project Operations, as linhas de estimativa de despesa são usadas para denotar a linha de cotação e os detalhes da linha de contrato para as despesas e linhas de estimativa de despesas no projeto.

Depois que uma lista de preços para vendas é resolvida, o sistema conclui as seguintes etapas para padronizar o preço de venda unitário.

1. O sistema usa a combinação de campos **Categoria** e **Unidade** na linha de estimativa de despesas para corresponder às linhas de preço da categoria na lista de preços que foi resolvida.
2. Se o sistema encontrar uma linha de preço de categoria que tenha uma taxa de venda para a combinação dos campos **Categoria** e **Unidade**, essa taxa de venda assumirá o padrão.
3. Se o sistema encontrar uma linha de preço de categoria correspondente, o método de precificação pode ser usado para definir o preço de venda padrão. A tabela a seguir mostra o comportamento padrão do preço de despesa no Project Operations.

    | Contexto | Método de precificação | Preço padrão |
    | --- | --- | --- |
    | Estimativa | Preço por unidade | Com base na linha de preço da categoria |
    | &nbsp; | A preço de custo | 0.00 |
    | &nbsp; | Markup sobre custo | 0.00 |
    | Real | Preço por unidade | Com base na linha de preço da categoria |
    | &nbsp; | A preço de custo | Com base no custo real relacionado |
    | &nbsp; | Markup sobre custo | Aplicar uma marcação conforme definido pela linha de preço da categoria na taxa de custo unitário do custo real relacionado |

4. Se o sistema não corresponder aos valores de campo **Categoria** e **Unidade**, a taxa de venda será zero (0) como padrão.
