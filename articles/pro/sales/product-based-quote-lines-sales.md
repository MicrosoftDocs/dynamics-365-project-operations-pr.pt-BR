---
title: Visão geral de linhas de cotação baseadas no produto - lite
description: Este tópico fornece informações sobre como trabalhar com linhas de cotação baseadas no produto.
author: rumant
manager: Annbe
ms.date: 10/30/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 29d82637c6c8bb5b5cde7707d181d5b3d3b235c4
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272554"
---
# <a name="product-based-quote-lines-overview---lite"></a>Visão geral de linhas de cotação baseadas no produto - lite

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

Você pode criar linhas de cotação baseadas em produto no Dynamics 365 Project Operations. As linhas de cotação baseadas no produto podem ser adicionadas manualmente ou podem ser itens do catálogo de produtos.

## <a name="product-catalog"></a>Catálogo de produtos

Cada produto do catálogo de produtos tem uma unidade padrão e um grupo de unidades. Se vários produtos compartilharem o mesmo conjunto de atributos, será possível criar uma família de produtos que compartilha esses atributos. 

Por exemplo, uma empresa vende licenças de assinatura para diferentes tipos de software. Todos os programas de software por assinatura têm os dois seguintes atributos:

- Número de usuários
- Duração de uma assinatura medida em meses

Para manter este tipo de catálogo, crie uma família de produtos chamada **Software por Assinatura** e adicione o número de usuários e a duração da assinatura como atributos. Em seguida, você pode adicionar produtos individuais à família de produtos **Software por Assinatura**.

## <a name="add-product-catalog-items-to-a-project-quote"></a>Adicionar itens do catálogo de produtos a uma cotação de projeto

As páginas **Cotação do Projeto** e **Contrato do Projeto** têm seções para linhas baseadas nos projetos e no produto. Para linhas baseados no produto, a lista suspensa na linha de cotação ou na linha de contrato do projeto inclui todos os produtos e unidades na lista de preços do produto. Também é possível adicionar produtos que não fazem parte da lista de preços do produto.

Além disso, é possível selecionar produtos de outras listas de preços ou diretamente do catálogo de produtos. Quando você seleciona produtos diretamente em um catálogo de produtos, a lista de preços padrão desse produto é usada para se chegar ao preço de vendas dos produtos. Se uma lista de preços padrão não for definida, o preço será definido como 0 (zero).

Quando uma linha de cotação for baseada em um catálogo de produtos, você poderá substituir o preço de vendas diretamente na linha de cotação. Uma linha de cotação no campo **Preço** com dois valores disponíveis:

- **Substituir Preços**
- **Usar Padrão**

Se você selecionar **Substituir Preços**, o preço padrão não será definido. Em vez disso, você deve inserir um preço para o produto na linha de cotação. Se você selecionar **Usar Padrão**, o preço de venda padrão será usado e o campo será bloqueado para edição.

Os preços de venda padrão serão inseridos nas linhas baseadas no produto de uma cotação. O campo **Preço** é definido como **Substituir Preços**, de forma que você possa editar o preço padrão nas linhas de cotação. Esta é uma substituição específica do Project Operations para o comportamento das linhas baseadas no produto no Dynamics 365 Sales.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]