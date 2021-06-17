---
title: Resolver preços de venda para estimativas e dados reais
description: Este tópico fornece informações sobre como resolver taxas de vendas para estimativas e reais.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bf0d92c08cb32d7bddb72246623b608831ff883e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004832"
---
# <a name="resolve-sales-prices-for-estimates-and-actuals"></a>Resolver preços de venda para estimativas e dados reais

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Quando os preços de vendas em estimativas e dados reais forem resolvidos no Dynamics 365 Project Operations, o sistema primeiro usará a data e a moeda da cotação ou contrato do projeto relacionado para resolver a lista de preços de venda. Depois que a lista de preços de venda é resolvida, o sistema resolve a taxa de vendas ou cobrança.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-time"></a>Resolver as taxas de venda em linhas reais e estimadas para tempo

No Project Operations, as linhas de estimativa de tempo são usadas para denotar a linha de cotação e os detalhes da linha de contrato de tempo e as atribuições de recursos no projeto.

Depois que uma lista de preços para vendas é resolvida, o sistema conclui as seguintes etapas para padronizar a taxa de cobrança.

1. O sistema usa os campos **Função**, **Empresa de Recursos** e **Unidade de Recursos** na linha de estimativa para tempo para corresponder às linhas de preço da função na lista de preços resolvidos. Essa correspondência pressupõe que as dimensões de precificação prontas para uso para taxas de cobrança estão sendo usadas. Se você configurou o preço com base em qualquer outro campo em vez de, ou além de **Função**, **Empresa de Recursos** e **Unidade de Recursos**, essa é a combinação que será usada para recuperar uma linha de preço de função correspondente.
2. Se o sistema encontrar uma linha de preço de função que tenha uma taxa de cobrança para a combinação dos campos **Função**, **Empresa de Recursos** e **Unidade de Recursos**, essa taxa de cobrança assumirá o padrão.
3. Se o sistema não corresponder aos valores de campo **Função**, **Empresa de Recursos** e **Unidade de Recursos**, ele recuperará as linhas de preço da função com uma função correspondente, mas os valores nulos da **Unidade de Recursos**. Depois que o sistema encontrar um registro de preço de função correspondente, ele assumirá como padrão a taxa de cobrança desse registro. Essa correspondência pressupõe uma configuração pronta para uso para a prioridade relativa de **Função** em comparação a **Unidade de Recursos** como uma dimensão de preço de venda.

> [!NOTE]
> Se você configurou uma priorização diferente de **Função**, **Empresa de Recursos** e **Unidade de Recursos**, ou se tiver outras dimensões com prioridade mais alta, esse comportamento será devidamente alterado. O sistema recupera registros de preço de função com valores que correspondem a cada um dos valores de dimensão de precificação em ordem de prioridade com linhas que possuem valores nulos para as dimensões que vêm por último.

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

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-material"></a>Resolver taxas de vendas em dados reais e linhas de estimativa para material

Em Project Operations, as linhas de estimativa de material são usadas para denotar a linha de cotação e os detalhes da linha de contrato para materiais e as linhas de estimativa de material no projeto.

Depois que uma lista de preços para vendas é resolvida, o sistema conclui as seguintes etapas para padronizar o preço de venda unitário.

1. O sistema usa a combinação de campos **Produto** e **Unidade** na linha de estimativa para o material corresponder às linhas de item da lista de preços na lista de preços que foi resolvida.
2. Se o sistema encontrar uma linha de item da lista de preços com uma taxa de vendas para a combinação de campos **Produto** e **Unidade** e o método de precificação for **Valor da moeda**, o preço de venda especificado na linha da lista de preços será usado.
3. Se os valores dos campos **Produto** e **Unidade** não coincidirem, o padrão da taxa de vendas será zero.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
