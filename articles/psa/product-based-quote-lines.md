---
title: Linhas de cotação baseadas em produto
description: Este tópico fornece informações sobre linhas de cotação baseadas em produto.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 9c3b2b35abe894e79d6f55a7ddd6e5c64d0f12f2
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123184"
---
# <a name="product-based-quote-lines"></a><span data-ttu-id="2b6ac-103">Linhas de cotação baseadas em produto</span><span class="sxs-lookup"><span data-stu-id="2b6ac-103">Product-based quote lines</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


<span data-ttu-id="2b6ac-104">Você pode criar linhas de cotação baseadas em produto no Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="2b6ac-104">You can create product-based quote lines in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="2b6ac-105">As linhas de cotação baseadas em produto podem ser linhas "fora do catálogo" ou podem ser itens do catálogo de produtos.</span><span class="sxs-lookup"><span data-stu-id="2b6ac-105">Product-based quote lines can be "write-in" lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="2b6ac-106">Catálogo de produtos</span><span class="sxs-lookup"><span data-stu-id="2b6ac-106">Product catalog</span></span>

<span data-ttu-id="2b6ac-107">Os produtos no catálogo de produtos do Dynamics 365 têm uma unidade e um grupo de unidades padrão.</span><span class="sxs-lookup"><span data-stu-id="2b6ac-107">The products in a Dynamics 365 product catalog have a default unit and unit group.</span></span> <span data-ttu-id="2b6ac-108">Se vários produtos compartilharem o mesmo conjunto de atributos, será possível criar uma família de produtos que também tenha esses atributos.</span><span class="sxs-lookup"><span data-stu-id="2b6ac-108">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="2b6ac-109">Todos os produtos em uma família de produtos herdam o mesmo conjunto de atributos.</span><span class="sxs-lookup"><span data-stu-id="2b6ac-109">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="2b6ac-110">Por exemplo, uma empresa vende licenças de assinatura para uma variedade de programas de software.</span><span class="sxs-lookup"><span data-stu-id="2b6ac-110">For example, a company sells subscription licenses for a variety of software.</span></span> <span data-ttu-id="2b6ac-111">Todos os programas de software por assinatura têm os dois seguintes atributos:</span><span class="sxs-lookup"><span data-stu-id="2b6ac-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="2b6ac-112">Número de usuários</span><span class="sxs-lookup"><span data-stu-id="2b6ac-112">Number of users</span></span> 
- <span data-ttu-id="2b6ac-113">Duração da assinatura (em meses)</span><span class="sxs-lookup"><span data-stu-id="2b6ac-113">Subscription duration (in months)</span></span>

<span data-ttu-id="2b6ac-114">Uma boa maneira de manter esse tipo de catálogo é criar uma família de produtos chamada **Software por Assinatura** e que tenha **Número de usuários** e **Duração da assinatura** como atributos.</span><span class="sxs-lookup"><span data-stu-id="2b6ac-114">A good way to maintain this type of catalog is to create a product family that is named **Subscription Software**, and that has **Number of users** and **Subscription duration** as attributes.</span></span> <span data-ttu-id="2b6ac-115">Assim, você pode adicionar produtos individuais, como **Dynamics 365 Sales** ou **Dynamics 365 Field Service** à família de produtos **Software por Assinatura**.</span><span class="sxs-lookup"><span data-stu-id="2b6ac-115">You can then add individual products, such as **Dynamics 365 Sales** or **Dynamics 365 Field Service** to the **Subscription Software** product family.</span></span>

## <a name="adding-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="2b6ac-116">Adicionando itens do catálogo de produtos a uma cotação de projeto</span><span class="sxs-lookup"><span data-stu-id="2b6ac-116">Adding product catalog items to a project quote</span></span>

<span data-ttu-id="2b6ac-117">As páginas de cotação e contrato de projeto têm seções para dois tipos de linha: linhas baseadas em projeto e baseadas em produto.</span><span class="sxs-lookup"><span data-stu-id="2b6ac-117">Project quote and project contract pages have sections for two types of lines: project-based lines and product-based lines.</span></span> <span data-ttu-id="2b6ac-118">Para linhas baseadas em produto, o Dynamics 365 é usado para adicionar itens de um catálogo de produtos a uma cotação.</span><span class="sxs-lookup"><span data-stu-id="2b6ac-118">For product-based lines, Dynamics 365 is used to add items from a product catalog to a quote.</span></span> <span data-ttu-id="2b6ac-119">A lista suspensa na linha de cotação ou na linha de contrato do projeto inclui todos os produtos e unidades na lista de preços do produto que é anexada à cotação ou ao contrato do projeto.</span><span class="sxs-lookup"><span data-stu-id="2b6ac-119">The drop-down list on the quote line or project contract line includes all the products and units in the product price list that is attached to the quote or project contract.</span></span> <span data-ttu-id="2b6ac-120">Também é possível adicionar produtos que não fazem parte da lista de preços do produto da cotação.</span><span class="sxs-lookup"><span data-stu-id="2b6ac-120">You can also add products that aren't part of quote's product price list.</span></span>

<span data-ttu-id="2b6ac-121">Além disso, é possível selecionar produtos de outras listas de preços ou selecionar produtos diretamente do catálogo de produtos.</span><span class="sxs-lookup"><span data-stu-id="2b6ac-121">Additionally, you can select products from other price lists, or you can select products directly from the product catalog.</span></span> <span data-ttu-id="2b6ac-122">Quando você seleciona produtos diretamente em um catálogo de produtos, a lista de preços padrão desse produto é usada para se chegar ao preço de vendas dos produtos.</span><span class="sxs-lookup"><span data-stu-id="2b6ac-122">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="2b6ac-123">Se uma lista de preços padrão não for definida, o preço será definido como 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="2b6ac-123">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="2b6ac-124">Se uma linha de cotação for baseada em um catálogo de produtos, você poderá substituir o preço de vendas diretamente na linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="2b6ac-124">If a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="2b6ac-125">Observe que uma linha de cotação no Dynamics 365 tem um campo **Preço**.</span><span class="sxs-lookup"><span data-stu-id="2b6ac-125">Note that a quote line in Dynamics 365 has a **Pricing** field.</span></span> <span data-ttu-id="2b6ac-126">Dois valores estão disponíveis:</span><span class="sxs-lookup"><span data-stu-id="2b6ac-126">Two values are available:</span></span>

- <span data-ttu-id="2b6ac-127">Substituir preço</span><span class="sxs-lookup"><span data-stu-id="2b6ac-127">Override pricing</span></span>  
- <span data-ttu-id="2b6ac-128">Usar padrão</span><span class="sxs-lookup"><span data-stu-id="2b6ac-128">Use default</span></span>

<span data-ttu-id="2b6ac-129">Se você definir esse campo como **Substituir preço**, o Dynamics 365 não definirá um preço padrão.</span><span class="sxs-lookup"><span data-stu-id="2b6ac-129">If you set this field to **Override pricing**, Dynamics 365 doesn't set a default price.</span></span> <span data-ttu-id="2b6ac-130">Você deve inserir um preço para o produto na linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="2b6ac-130">You must enter a price for the product on the quote line.</span></span> <span data-ttu-id="2b6ac-131">Se você definir esse campo como **Usar padrão**, o Dynamics 365 usará o preço de vendas padrão e bloqueará o campo para impedir a edição.</span><span class="sxs-lookup"><span data-stu-id="2b6ac-131">If you set this field to **Use default**, Dynamics 365 uses the default sales price and locks the field to prevent editing.</span></span>

<span data-ttu-id="2b6ac-132">Após a instalação do PSA, os preços de vendas padrão são inseridos nas linhas baseadas em produto em uma cotação.</span><span class="sxs-lookup"><span data-stu-id="2b6ac-132">After you install PSA, default sales prices are entered on the product-based lines on a quote.</span></span> <span data-ttu-id="2b6ac-133">O campo **Preço** é definido como **Substituir preço** para que seja possível editar o preço padrão nas linhas de cotação.</span><span class="sxs-lookup"><span data-stu-id="2b6ac-133">The **Pricing** field is then set to **Override pricing** so that you can edit the default price on the quote lines.</span></span>

> ![Definindo a substituição de preço](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a><span data-ttu-id="2b6ac-135">Fatores de quantidade para produtos</span><span class="sxs-lookup"><span data-stu-id="2b6ac-135">Quantity factors for products</span></span>

<span data-ttu-id="2b6ac-136">O PSA usa fatores de quantidade para dar suporte a produtos baseados em assinatura.</span><span class="sxs-lookup"><span data-stu-id="2b6ac-136">PSA uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="2b6ac-137">Para produtos baseados em assinatura, a quantidade na linha de contrato do projeto ou da cotação é expressada como o número de meses do usuário.</span><span class="sxs-lookup"><span data-stu-id="2b6ac-137">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user months.</span></span>

<span data-ttu-id="2b6ac-138">Geralmente, o preço do software por assinatura é armazenado no catálogo como o preço mensal por usuário.</span><span class="sxs-lookup"><span data-stu-id="2b6ac-138">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="2b6ac-139">No entanto, você pode usar outras descrições de tempo.</span><span class="sxs-lookup"><span data-stu-id="2b6ac-139">However, you can use other time descriptions instead.</span></span> <span data-ttu-id="2b6ac-140">Durante o processo de vendas, o preço na linha de cotação normalmente é o preço mensal por usuário que foi negociado e descontado pelo agente de vendas de TI.</span><span class="sxs-lookup"><span data-stu-id="2b6ac-140">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="2b6ac-141">Cada negociação tem um número diferente de usuários e um número diferente de meses de assinatura.</span><span class="sxs-lookup"><span data-stu-id="2b6ac-141">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="2b6ac-142">A quantidade usada para calcular o valor da linha de cotação é um produto do número de usuários e do número de meses de assinatura.</span><span class="sxs-lookup"><span data-stu-id="2b6ac-142">The quantity that is used to compute the amount of the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="2b6ac-143">Para dar suporte a esse tipo de vendas, o PSA introduziu o conceito de fatores de quantidade.</span><span class="sxs-lookup"><span data-stu-id="2b6ac-143">To support this type of sale, PSA introduced the concept of quantity factors.</span></span> <span data-ttu-id="2b6ac-144">Os fatores de quantidade dependem dos atributos de produto no Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="2b6ac-144">Quantity factors rely on the product attributes in Dynamics 365.</span></span> <span data-ttu-id="2b6ac-145">Quando você configura propriedades específicas para um produto, o PSA permite sinalizar um subconjunto dessas propriedades, ou todas as propriedades, como fatores de quantidade.</span><span class="sxs-lookup"><span data-stu-id="2b6ac-145">When you configure specific properties for a product, PSA lets you flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="2b6ac-146">O PSA valida que apenas propriedades numéricas ou propriedades de produto que tenham tipo de dados numéricos sejam sinalizadas como fatores de quantidade.</span><span class="sxs-lookup"><span data-stu-id="2b6ac-146">PSA validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="2b6ac-147">Quando um produto para o qual os fatores de quantidade são configurados é adicionado a uma linha de cotação,o campo **Quantidade** na linha de cotação se torna um campo somente leitura.</span><span class="sxs-lookup"><span data-stu-id="2b6ac-147">When a product that quantity factors are configured for is added to a quote line, the **Quantity** field on the quote line becomes a read-only field.</span></span> <span data-ttu-id="2b6ac-148">Depois que você insere valores para propriedades do produto que são fatores de quantidade, o PSA calcula a quantidade da linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="2b6ac-148">After you enter values for product properties that are quantity factors, PSA computes the quantity of the quote line.</span></span>

<span data-ttu-id="2b6ac-149">Por exemplo, o Dynamics 365 pode ter as seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="2b6ac-149">For example, Dynamics 365 might have the following properties:</span></span> 

- <span data-ttu-id="2b6ac-150">**Número de usuários** – o número de usuários</span><span class="sxs-lookup"><span data-stu-id="2b6ac-150">**No of users** - The number of users</span></span> 
- <span data-ttu-id="2b6ac-151">**Número de Meses** – o número de meses de assinatura</span><span class="sxs-lookup"><span data-stu-id="2b6ac-151">**No of Months** - The number of subscription months</span></span>
- <span data-ttu-id="2b6ac-152">**SKU do Produto**</span><span class="sxs-lookup"><span data-stu-id="2b6ac-152">**Product SKU**</span></span> 

<span data-ttu-id="2b6ac-153">As propriedades **Número de Usuários** e **Número de Meses** podem ser sinalizadas como fatores de quantidade, bastando para isso editá-las na linha de produto.</span><span class="sxs-lookup"><span data-stu-id="2b6ac-153">Tne **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span> 

> ![Sinalizando Número de Usuários e Número de Meses como fatores de qualidade](media/basic-guide-11.png)
 
