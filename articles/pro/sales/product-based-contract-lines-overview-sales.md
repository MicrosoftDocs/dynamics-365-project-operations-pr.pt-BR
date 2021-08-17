---
title: Visão geral de linhas de contrato baseadas em produto - lite
description: Este tópico fornece informações sobre linhas de contrato baseadas em produto.
author: rumant
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 79b4f6355afb7472f843eda06bf33a3fe732274d6f2566bd23000aa11cbfdce1
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007537"
---
# <a name="product-based-contract-lines-overview---lite"></a>Visão geral de linhas de contrato baseadas em produto - lite

_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_

Você pode criar linhas de contrato baseadas em produto no Dynamics 365 Project Operations. As linhas de contrato baseadas em produto podem ser linhas criadas manualmente ou podem ser itens do catálogo de produtos.

## <a name="product-catalog"></a>Catálogo de produtos

Os produtos no catálogo de produtos têm uma unidade e um grupo de unidades padrão. Se vários produtos compartilharem o mesmo conjunto de atributos, será possível criar uma família de produtos que também tenha esses atributos. Todos os produtos em uma família de produtos herdam o mesmo conjunto de atributos.

Por exemplo, uma empresa vende licenças de assinatura para diferentes tipos de software. Todos os programas de software por assinatura têm os dois seguintes atributos:

- Número de usuários
- Duração da assinatura (em meses)

Para manter esse tipo de catálogo, crie uma família de produtos chamada **Software de Assinatura**. Adicione os atributos **Número de usuários** e **Duração da assinatura** para a família de produtos. Em seguida, adicione produtos individuais à família de produtos **Software de Assinatura**.

## <a name="add-product-catalog-items-to-a-project-contract"></a>Adicionar itens do catálogo de produtos a um contrato de projeto

Os contratos de projeto têm seções para dois tipos de linhas baseadas em projeto e baseadas em produto. As linhas baseadas em produto incluem todos os produtos e unidades da lista de preços de produtos do contrato. Produtos que não fazem parte da lista de preços de produtos do contrato podem ser adicionados.

Você pode selecionar produtos de outras listas de preços ou diretamente do catálogo de produtos. Quando você seleciona produtos diretamente em um catálogo de produtos, a lista de preços padrão desse produto é usada para se chegar ao preço de vendas dos produtos. Se uma lista de preços padrão não for definida, o preço será definido como 0 (zero).

Se uma linha de contrato for baseada em um catálogo de produtos, você poderá substituir o preço de vendas diretamente na linha de contrato. Uma linha de contrato tem o campo **Preço** com os dois valores:

- **Substituir preço**
- **Usar padrão**

Se você definir o campo **Preço** como **Substituir preço**, o preço padrão não será definido. Insira um preço para o produto na linha de contrato. Se você definir o campo como **Usar padrão**, o preço de venda padrão será usado e o campo não poderá ser editado.

Após a instalação do Project Operations, os preços de vendas padrão são inseridos nas linhas baseadas em produto em um contrato. O campo **Preço** é definido como **Substituir preço** para que seja possível editar o preço padrão nas linhas de contrato. Esta é uma substituição específica do Project Operations para o comportamento das linhas baseadas no produto no Dynamics 365 Sales.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]