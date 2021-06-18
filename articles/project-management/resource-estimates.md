---
title: Estimativas financeiras para tempo do recurso em projetos
description: Este tópico fornece informações sobre como as estimativas financeiras de tempo são calculadas.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e79e33da618c4ab32b1ba13f33e50f60a550ff0b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010772"
---
# <a name="financial-estimates-for-resource-time-on-projects"></a>Estimativas financeiras para tempo do recurso em projetos

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

As estimativas financeiras para o tempo são calculadas com base em três fatores: 

- O tipo de membro da equipe genérico ou nomeado atribuído a cada tarefa do nó folha no plano do projeto. 
- O tipo ou complexidade do trabalho.
- A distribuição do esforço para a atribuição do recurso na tarefa. 

Os primeiros dois fatores influenciam o custo unitário ou a taxa de cobrança da atribuição de um recurso. O custo unitário ou taxa de cobrança de uma atribuição de recurso é determinada pelos atributos do recurso atribuído. Esses atributos incluem a unidade organizacional à qual o recurso pertence e a função padrão do recurso. Você também pode adicionar atributos personalizados relevantes ao seu negócio para o recurso, como título padrão ou nível de experiência, e fazer com que influenciem o custo unitário ou a taxa de cobrança da atribuição.
Além dos atributos do recurso, os atributos do trabalho, como a tarefa, também podem influenciar a taxa de cobrança da unidade ou a taxa de custo da atribuição. Por exemplo, quando certas tarefas são mais complexas, a atribuição do recurso a essas tarefas específicas resulta em um custo unitário ou taxa de cobrança mais alta do que as tarefas menos complexas.   

O terceiro fator fornece a quantidade de horas nessa taxa. Nos casos em que uma tarefa cobre dois períodos de preços, é provável que a primeira parte da atribuição de recursos para essa tarefa tenha custo e preço diferentes daqueles da segunda parte da tarefa. A estimativa de esforço em cada atribuição de recurso é um valor complexo armazenado com a distribuição diária de esforço por dia.

Para obter instruções detalhadas sobre como configurar atributos personalizados de trabalho e recursos como preços e dimensões de custo, consulte [Visão geral de Dimensões de Preços](../pricing-costing/pricing-dimensions-overview.md).

A estimativa financeira em cada atribuição de recursos é calculada como **taxa/hora para a atribuição multiplicada pelo número de horas**.  Semelhante à estimativa de esforço, a estimativa financeira de custo e receita para cada atribuição de recurso é um valor complexo armazenado com a distribuição diária da quantia monetária por dia. 

## <a name="summarizing-financial-estimates-for-time"></a>Resumir estimativas financeiras por tempo
Uma estimativa financeira por tempo em uma tarefa de nó folha é a soma das estimativas financeiras em todas as atribuições de recursos para essa tarefa.

Uma estimativa financeira por tempo em uma tarefa de resumo ou pai é a soma das estimativas financeiras em todas as tarefas filho. Este é o custo estimado da mão de obra no projeto. 

![Estimativas de Recurso](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>Preço de custo e moeda de custo padrão

O preço de custo padrão é obtido das listas de preços anexadas à unidade de contratação do projeto. A moeda do custo de um projeto é sempre a moeda da unidade contratante do projeto. Em uma atribuição de recursos, a estimativa financeira de custo é armazenada na moeda de custo do projeto. Às vezes, a moeda em que a taxa de custo é configurada na lista de preços é diferente da moeda de custo do projeto. Nesses casos, o aplicativo converte a moeda na qual o preço de custo está configurado para a moeda do projeto. Na grade **Estimativas**, todas as estimativas de custo são exibidas e resumidas na moeda de custo do projeto. 

## <a name="default-bill-rate-and-sales-currency"></a>Taxa de cobrança e moeda de vendas padrão

O preço de venda padrão será obtido das listas de preços do projeto anexadas ao contrato do projeto relacionado se o negócio for ganho, ou da cotação do projeto relacionado se o negócio ainda estiver em estágio de pré-venda. A moeda de vendas do projeto é sempre a moeda da cotação do projeto ou do contrato do projeto. Em uma atribuição de recursos, a estimativa financeira de vendas é armazenada na moeda de vendas do projeto. Ao contrário do custo, o preço de venda configurado na lista de preços nunca pode ser diferente da moeda de venda do projeto. Não há cenário em que a conversão de moeda seja necessária. Na grade **Estimativas**, todas as estimativas de vendas são exibidas e resumidas na moeda de vendas do projeto. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
