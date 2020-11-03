---
title: Listas de preços de produtos
description: Este tópico fornece informações sobre as listas de preços em preços de catálogo usados para cotações e contratos de projetos.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 504aa90bfb478207059b5e2894a3990f9a4a5e9e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071496"
---
# <a name="product-price-lists"></a>Listas de preços de produtos

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pró-forma_

As entidades de listas de preços e item da lista de preços suportam preços do catálogo de produtos. De modo geral, essa funcionalidade é usada para linhas baseadas em catálogo em cotações e contratos de projeto.

Para linhas baseadas em projeto, um contrato representa a negociação depois que ela é ganha. Como o processo de negociação geralmente antecede a vitória, o preço que é anexado à cotação sempre é copiado como está em uma nova lista de preços e anexado ao contrato. Essa nova lista de preços não pode ser alterada fora do escopo do contrato. Essa limitação ajuda a proteger a tabela de tarifas que foi negociada contra qualquer alteração de preço que ocorra na lista de preços mestre.

Os produtos devem ser configurados para que tenham listas de preços e custos padrão no catálogo de produtos. Use o preço da listas, o custo padrão e o custo atual para configurar preços de lista e custos padrão. Os preços de lista padrão são usados em uma linha de cotação ou linha de contrato do projeto somente quando o sistema não pode encontrar uma linha da lista de preços para esse produto na lista de preços do produto para a cotação ou o contrato do projeto.

O preço de custo das linhas do catálogo de produtos pode ser alterado entre cotações. Esse recurso é importante, pois se você não rastrear precisamente os custos, não será possível determinar os lucros operacionais nas participações do projeto. A regra geral é usar o custo padrão do produto como o preço de custo. Entretanto, o preço de custo padrão pode ser atualizado na linha de cotação se houver um preço de custo diferente para essa cotação.

## <a name="price-list-items"></a>Itens da lista de preços

É possível adicionar produtos de um catálogo de produtos a diferentes listas de preços. As linhas da lista de preços para produtos sempre fazem referência a uma unidade específica. O preço de um produto em itens da lista de preços pode ser configurado como um valor monetário. Como alternativa, ele pode ser configurado como uma função do preço de lista, custo atual ou custo padrão.

O PSA dá suporte a várias opções de arredondamento quando os preços são configurados como uma função de preço de lista, custo padrão ou custo atual. Além de aproveitar vários métodos de precificação e opções de arredondamento, você pode associar listas de descontos a itens da lista de preços. 

Quando você cria uma nova lista de preços personalizada para uma cotação selecionando **Criar Preço Personalizado** na página **Cotação do Projeto** , é criada uma cópia da lista de preços e o campo **Entidade** no cabeçalho da nova lista de preços é definido como **Entidade de Vendas**. O nome da nova lista de preços é acrescentada com o nome da cotação e um carimbo de data/hora. Você também pode usar o nome da nova lista de preços e o nome da cotação em fluxos de trabalho personalizados para disparar revisão adicional e aprovações para cotações que usam preço personalizado.

 
## <a name="default-product-price-list"></a>Lista de preços padrão do produto
Cada registro do cliente tem um campo **Lista de Preços Padrão** , onde é possível especificar uma lista de preços que corresponda a moeda do cliente. Um valor padrão não é inserido automaticamente nesse campo. Quando existe um contrato de preço personalizado com um cliente específico, é possível usar esse campo para associar uma lista de preços a esse cliente.

As entidades Oportunidade, Cotação e Contrato de Projeto usam a ordem a seguir para inserir listas de preços padrão do produto. A mesma ordem é usada para listas de preços do projeto.

1.  Cotação
2.  Oportunidade
3.  Cliente
4.  Configurações globais 

Por padrão, o campo **Produto** na linha de cotação lista todos os produtos ativos na lista de preços de produto da cotação. Se um produto foi inativado, ou se for um produto em rascunho, ele não será listado, mesmo se estiver na lista de preços. 

As linhas do catálogo de produtos são adicionadas como linhas da fatura na primeira fatura que é criada para um contrato de projeto. Em uma fatura de rascunho, essas linhas de fatura podem ser excluídas. Nesse caso, as linhas aparecerão em uma fatura subsequente até que sejam faturadas, ou até que a fatura seja enviada ao cliente. Não é possível faturar uma quantidade parcial de uma linha de fatura do produto. Quando as linhas de produto do contrato do projeto são faturadas, dados reais são criados. No entanto, esses dados reais não são vinculados à entidade de projeto relacionada. Em outras palavras, as linhas de contrato do projeto baseadas em produto são independentes de qualquer uso baseado em projeto. O consumo de material em projetos não é rastreado.
