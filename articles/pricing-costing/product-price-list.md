---
title: Listas de preços de produtos
description: Este artigo fornece informações sobre as listas de preços em preços de catálogo usados para cotações e contratos de projeto.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 68203f5adf7bf41d97e662e335d481ccac959ed6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917608"
---
# <a name="product-price-lists"></a>Listas de preços de produtos

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

 Em Project Operations, **Listas de preços de produtos** e entidades de itens de lista de preços relacionadas dão suporte à funcionalidade para produtos de preços em linhas de contrato e cotação baseada em produto. Para produtos usados em projetos, os registros de item da lista de preços para listas de preços do projeto são usados. 

Os produtos devem ser configurados para que tenham listas de preços e custos padrão no catálogo de produtos. Use o preço da listas, o custo padrão e o custo atual para configurar preços de lista e custos padrão. Os preços de lista padrão são usados em uma linha de cotação ou linha de contrato do projeto somente quando o sistema não pode encontrar uma linha da lista de preços para esse produto na lista de preços do produto para a cotação ou o contrato do projeto.

O preço de custo das linhas do catálogo de produtos pode ser alterado entre cotações. Esse recurso é importante, pois se você não rastrear precisamente os custos, não será possível determinar os lucros operacionais nas participações do projeto. A regra geral é usar o custo padrão do produto como o preço de custo. Entretanto, o preço de custo padrão pode ser atualizado na linha de cotação se houver um preço de custo diferente para essa cotação.

## <a name="price-list-items"></a>Itens da lista de preços

É possível adicionar produtos de um catálogo de produtos a diferentes listas de preços. As linhas da lista de preços para produtos sempre fazem referência a uma unidade específica. O preço de um produto em itens da lista de preços pode ser configurado como um valor monetário. Como alternativa, ele pode ser configurado como uma função do preço de lista, custo atual ou custo padrão.

A funcionalidade de preços dá suporte a várias opções de arredondamento quando os preços de produtos são configurados como uma função de preço de lista, custo padrão ou custo atual. Além de aproveitar vários métodos de precificação e opções de arredondamento, você pode associar listas de descontos a itens da lista de preços. 

 
## <a name="default-product-price-list"></a>Lista de preços padrão do produto
Cada registro do cliente tem um campo **Lista de Preços Padrão**, onde é possível especificar uma lista de preços que corresponda a moeda do cliente. Um valor padrão não é inserido automaticamente nesse campo. Quando existe um contrato de preço personalizado com um cliente específico, é possível usar esse campo para associar uma lista de preços a esse cliente.

As entidades Oportunidade, Cotação e Contrato de Projeto usam a ordem a seguir para inserir listas de preços padrão do produto. A mesma ordem é usada para listas de preços do projeto.

1.  Cotação
2.  Oportunidade
3.  Cliente
4.  Configurações globais 

Por padrão, o campo **Produto** na linha de cotação lista todos os produtos ativos na lista de preços de produto da cotação. Se um produto foi inativado, ou se for um produto em rascunho, ele não será listado, mesmo se estiver na lista de preços. 

As linhas do catálogo de produtos são adicionadas como linhas da fatura na primeira fatura que é criada para um contrato de projeto. Em uma fatura de rascunho, essas linhas de fatura podem ser excluídas. Nesse caso, as linhas aparecerão em uma fatura subsequente até que sejam faturadas, ou até que a fatura seja enviada ao cliente. Não é possível faturar uma quantidade parcial de uma linha de fatura do produto. Quando as linhas de produto do contrato do projeto são faturadas, dados reais são criados. No entanto, esses dados reais não são vinculados à entidade de projeto relacionada. Em outras palavras, as linhas de contrato do projeto baseadas em produto são independentes de qualquer uso baseado em projeto. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
