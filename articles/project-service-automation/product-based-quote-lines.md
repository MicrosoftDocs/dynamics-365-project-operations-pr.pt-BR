---
title: Linhas de cotação baseadas em produto
description: Este tópico fornece informações sobre linhas de cotação baseadas em produto.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 76b90c95-1b3a-4704-a13f-9d7099b83f4c
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: d8bb36fbfe8d01aa26faf5515ca218ad836126b7
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749055"
---
# <a name="product-based-quote-lines"></a>Linhas de cotação baseadas em produto

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


Você pode criar linhas de cotação baseadas em produto no Dynamics 365 Project Service Automation. As linhas de cotação baseadas em produto podem ser linhas "fora do catálogo" ou podem ser itens do catálogo de produtos.

## <a name="product-catalog"></a>Catálogo de produtos

Os produtos no catálogo de produtos do Dynamics 365 têm uma unidade e um grupo de unidades padrão. Se vários produtos compartilharem o mesmo conjunto de atributos, será possível criar uma família de produtos que também tenha esses atributos. Todos os produtos em uma família de produtos herdam o mesmo conjunto de atributos.

Por exemplo, uma empresa vende licenças de assinatura para uma variedade de programas de software. Todos os programas de software por assinatura têm os dois seguintes atributos:

- Número de usuários 
- Duração da assinatura (em meses)

Uma boa maneira de manter esse tipo de catálogo é criar uma família de produtos chamada **Software por Assinatura** e que tenha **Número de usuários** e **Duração da assinatura** como atributos. Assim, você pode adicionar produtos individuais, como **Dynamics 365 Sales** ou **Dynamics 365 Field Service** à família de produtos **Software por Assinatura**.

## <a name="adding-product-catalog-items-to-a-project-quote"></a>Adicionando itens do catálogo de produtos a uma cotação de projeto

As páginas de cotação e contrato de projeto têm seções para dois tipos de linha: linhas baseadas em projeto e baseadas em produto. Para linhas baseadas em produto, o Dynamics 365 é usado para adicionar itens de um catálogo de produtos a uma cotação. A lista suspensa na linha de cotação ou na linha de contrato do projeto inclui todos os produtos e unidades na lista de preços do produto que é anexada à cotação ou ao contrato do projeto. Também é possível adicionar produtos que não fazem parte da lista de preços do produto da cotação.

Além disso, é possível selecionar produtos de outras listas de preços ou selecionar produtos diretamente do catálogo de produtos. Quando você seleciona produtos diretamente em um catálogo de produtos, a lista de preços padrão desse produto é usada para se chegar ao preço de vendas dos produtos. Se uma lista de preços padrão não for definida, o preço será definido como 0 (zero).

Se uma linha de cotação for baseada em um catálogo de produtos, você poderá substituir o preço de vendas diretamente na linha de cotação. Observe que uma linha de cotação no Dynamics 365 tem um campo **Preço**. Dois valores estão disponíveis:

- Substituir preço  
- Usar padrão

Se você definir esse campo como **Substituir preço**, o Dynamics 365 não definirá um preço padrão. Você deve inserir um preço para o produto na linha de cotação. Se você definir esse campo como **Usar padrão**, o Dynamics 365 usará o preço de vendas padrão e bloqueará o campo para impedir a edição.

Após a instalação do PSA, os preços de vendas padrão são inseridos nas linhas baseadas em produto em uma cotação. O campo **Preço** é definido como **Substituir preço** para que seja possível editar o preço padrão nas linhas de cotação.

> ![Definindo a substituição de preço](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a>Fatores de quantidade para produtos

O PSA usa fatores de quantidade para dar suporte a produtos baseados em assinatura. Para produtos baseados em assinatura, a quantidade na linha de contrato do projeto ou da cotação é expressada como o número de meses do usuário.

Geralmente, o preço do software por assinatura é armazenado no catálogo como o preço mensal por usuário. No entanto, você pode usar outras descrições de tempo. Durante o processo de vendas, o preço na linha de cotação normalmente é o preço mensal por usuário que foi negociado e descontado pelo agente de vendas de TI. Cada negociação tem um número diferente de usuários e um número diferente de meses de assinatura. A quantidade usada para calcular o valor da linha de cotação é um produto do número de usuários e do número de meses de assinatura.

Para dar suporte a esse tipo de vendas, o PSA introduziu o conceito de fatores de quantidade. Os fatores de quantidade dependem dos atributos de produto no Dynamics 365. Quando você configura propriedades específicas para um produto, o PSA permite sinalizar um subconjunto dessas propriedades, ou todas as propriedades, como fatores de quantidade.

O PSA valida que apenas propriedades numéricas ou propriedades de produto que tenham tipo de dados numéricos sejam sinalizadas como fatores de quantidade. Quando um produto para o qual os fatores de quantidade são configurados é adicionado a uma linha de cotação,o campo **Quantidade** na linha de cotação se torna um campo somente leitura. Depois que você insere valores para propriedades do produto que são fatores de quantidade, o PSA calcula a quantidade da linha de cotação.

Por exemplo, o Dynamics 365 pode ter as seguintes propriedades: 

- **Número de usuários** – o número de usuários 
- **Número de Meses** – o número de meses de assinatura
- **SKU do Produto** 

As propriedades **Número de Usuários** e **Número de Meses** podem ser sinalizadas como fatores de quantidade, bastando para isso editá-las na linha de produto. 

> ![Sinalizando Número de Usuários e Número de Meses como fatores de qualidade](media/basic-guide-11.png)
 
