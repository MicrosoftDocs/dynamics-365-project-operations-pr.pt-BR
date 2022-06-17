---
title: Resolver preços de custo em estimativas e dados reais do projeto
description: Este artigo fornece informações sobre como preços de custo em estimativas e dados reais do projeto são resolvidos.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c278d8994389145c6dbee7574d2354724d985722
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917516"
---
# <a name="resolve-cost-prices-on-project-estimates-and-actuals"></a>Resolver preços de custo em estimativas e dados reais do projeto 

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

Para resolver os preços de custo e a lista de preços de custo para estimativas e reais, o sistema usa as informações dos campos **Data**, **Moeda** e **Unidade de Contratação** do projeto relacionado. Depois que a lista de preços de custo é resolvida, o aplicativo resolve a taxa de custo.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Como resolver taxas de custo em linhas reais e estimadas para Tempo

As linhas de estimativa de Tempo referem-se aos detalhes da linha de contrato e cotação para tempo e atribuições de recursos em um projeto.

Depois que uma lista de preços de custo é resolvida, os campos **Função** e **Unidade de Recursos** na linha de estimativa para Tempo são comparados com as linhas de preço da função na lista de preços. Essa correspondência pressupõe que você está usando as dimensões de preço padrão para custo de mão de obra. Se você tiver configurado o sistema para corresponder aos campos em vez de, ou além de **Função** e **Unidade de Recursos**, uma combinação diferente será usada para recuperar uma linha de preço de função correspondente. Se o aplicativo encontrar uma linha de preço de função que tenha uma taxa de custo para a combinação **Função** e **Unidade de Recursos**, essa será a taxa de custo padrão. Se o aplicativo não corresponder aos valores de **Função** e **Unidade de Recursos**, então irá recuperar as linhas de preço da função com uma função correspondente, mas os valores nulos da **Unidade de Recursos**. Depois de ter um registro de preço de função correspondente, a taxa de custo terá como padrão desse registro. 

> [!NOTE]
> Se você configurar uma priorização diferente de **Função** e **Unidade de Recursos**, ou se tiver outras dimensões com prioridade mais alta, esse comportamento será devidamente alterado. O sistema recupera registros de preço de função com valores que correspondem a cada um dos valores de dimensão de precificação em ordem de prioridade com linhas que possuem valores nulos para as dimensões que vêm por último.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Como resolver taxas de custo em linhas reais e estimadas para Despesa

As linhas de estimativa para Despesa referem-se aos detalhes da cotação e da linha de contrato para despesas e as linhas de estimativa de despesa em um projeto.

Depois que uma lista de preços de custo é resolvida, o sistema usa uma combinação dos campos **Categoria** e **Unidade** na linha de estimativa de despesas para combinar com as linhas do **Preço da categoria** na lista de preços resolvida. Se o sistema encontrar uma linha de preço de categoria que tenha uma taxa de custo para a combinação dos campos **Categoria** e **Unidade**, a taxa de custo terá o padrão. Se o sistema não puder corresponder aos valores **Categoria** e **Unidade**, ou se conseguir encontrar uma linha de preço de categoria correspondente, mas o método de precificação não for **Preço por unidade**, a taxa de custo será padronizada como zero (0).

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-material"></a>Resolver taxas de custo em dados reais e linhas de estimativa para Material

As linhas de estimativa de material referem-se aos detalhes da linha de orçamento e contrato para materiais e as linhas de estimativa de material em um projeto.

Depois que uma lista de preços de custo é resolvida, o sistema usa uma combinação dos campos **Produtos** e **Unidade** na linha de estimativa para uma estimativa de material para combinar com as linhas de **Itens da Lista de Preços** na lista de preços resolvida. Se o sistema encontrar uma linha de preço de produto que tenha uma taxa de custo para a combinação de campo **Produto** e **Unidade**, a taxa de custo é padronizada. Se o sistema não pode corresponder aos valores **Produto** e **Unidade**, ou se for capaz de encontrar uma linha de item de lista de preços correspondente, mas o método de precificação é baseado no Custo padrão ou Custo atual e nenhum é definido no produto, o custo unitário é padronizado para zero.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
