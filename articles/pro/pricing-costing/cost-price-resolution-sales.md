---
title: Resolver preços de custo em estimativas e dados reais - lite
description: Este tópico fornece informações sobre como os preços de custo em estimativas e reais são resolvidos.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d2afaa2231f4044dbcbfa24b91aec39289275a91
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764554"
---
# <a name="resolve-cost-prices-on-estimates-and-actuals---lite"></a>Resolver preços de custo em estimativas e dados reais - lite

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
