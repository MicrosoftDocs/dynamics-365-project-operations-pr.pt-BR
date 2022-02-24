---
title: Resolvendo preços de custo para estimativas e dados reais
description: Este tópico fornece informações sobre como os preços de custo para estimativas e reais são resolvidos.
author: rumant
manager: Annbe
ms.date: 04/09/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 13903acc22e765ddc5bc1b87428ef3565f2b0a44
ms.sourcegitcommit: ac90be6106592f883a0de39a75836fb40255d65a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2021
ms.locfileid: "5877298"
---
# <a name="resolving-cost-prices-for-estimates-and-actuals"></a>Resolvendo preços de custo para estimativas e dados reais

_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_

Para resolver os preços de custo e a lista de preços de custo para estimativas e reais, o sistema usa as informações dos campos **Data**, **Moeda** e **Unidade de Contratação** do projeto relacionado. Depois que a lista de preços de custo é resolvida, o aplicativo resolve a taxa de custo.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Como resolver taxas de custo em linhas reais e estimadas para Tempo

As linhas de estimativa de Tempo referem-se aos detalhes da linha de contrato e cotação para tempo e atribuições de recursos em um projeto.

Depois que uma lista de preços de custo é resolvida, o sistema usa os campos **Função**, **Empresa de Recursos** e **Unidade de Recursos** na linha de estimativa para Tempo para corresponder às linhas de preço da função na lista de preços. Essa correspondência pressupõe que você esteja usando dimensões de precificação prontas para uso para custo de mão de obra. Se você tiver configurado o sistema para corresponder aos campos em vez de, ou além de **Função**, **Empresa de Recursos** e **Unidade de Recursos**, uma combinação diferente será usada para recuperar uma linha de preço de função correspondente. Se o aplicativo encontrar uma linha de preço de função que tenha uma taxa de custo para a combinação **Função**, **Empresa de Recursos** e **Unidade de Recursos**, essa será a taxa de custo padrão. Se o aplicativo não puder corresponder exatamente à combinação dos valores **Função**, **Empresa de Recursos** e **Unidade de Recursos**, ele irá recuperar as linhas de preço da função com um valor de função correspondente, mas tem valores nulos para **Unidade de Recursos** e **Empresa de Recursos**. Depois que um registro de preço de função correspondente com o valor de preço de função correspondente for encontrado, a taxa de custo é padronizada para esse registro. 

> [!NOTE]
> Se você configurar uma priorização diferente de **Função**, **Empresa de Recursos** e **Unidade de Recursos**, ou se tiver outras dimensões com prioridade mais alta, esse comportamento será devidamente alterado. O sistema recupera registros de preço de função com valores que correspondem a cada um dos valores de dimensão de precificação em ordem de prioridade com linhas que possuem valores nulos para as dimensões que vêm por último na ordem de prioridade.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Como resolver taxas de custo em linhas reais e estimadas para Despesa

As linhas de estimativa para Despesa referem-se aos detalhes da cotação e da linha de contrato para despesas e as linhas de estimativa de despesa em um projeto.

Depois que uma lista de preços de custo é resolvida, o sistema usa uma combinação dos campos **Categoria** e **Unidade** na linha de estimativa para uma despesa para corresponder às linhas **Preço da Categoria** na lista de preços resolvida. Se o sistema encontrar uma linha de preço de categoria que tenha uma taxa de custo para a combinação dos campos **Categoria** e **Unidade**, a taxa de custo terá o padrão. Se o sistema não puder fazer a correspondência dos valores **Categoria** e **Unidade**, ou se ele for capaz de encontrar uma linha de preço de categoria correspondente, mas o método de precificação não for **Preço por Unidade**, a taxa de custo será padronizada como zero (0).

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-material"></a>Resolver taxas de custo em dados reais e linhas de estimativa para material

As linhas de estimativa de material referem-se aos detalhes da linha de orçamento e contrato para materiais e as linhas de estimativa de material em um projeto.

Depois que uma lista de preços de custo é resolvida, o sistema usa uma combinação dos campos **Produtos** e **Unidade** na linha de estimativa para uma estimativa de material para combinar com as linhas de **Itens da Lista de Preços** na lista de preços resolvida. Se o sistema encontrar uma linha de preço de produto que tenha uma taxa de custo para a combinação de campo **Produto** e **Unidade**, a taxa de custo é padronizada. Se o sistema não corresponder aos valores de **Produto** e **Unidade**, o custo unitários será padronizado como zero. Esse padrão também acontecerá se houver uma linha de item da lista de preços correspondente, mas o método de precificação se baseia em um custo padrão ou custo atual que não está definido no produto.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
