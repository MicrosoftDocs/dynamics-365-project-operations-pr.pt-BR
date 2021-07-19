---
title: Visão geral de linhas de cotação baseadas no produto - lite
description: Este tópico fornece informações sobre como trabalhar com linhas de cotação baseadas no produto.
author: rumant
ms.date: 10/30/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 8b904f9abd3d2505c5397906f63a5ae8ff4be41b
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369767"
---
# <a name="product-based-quote-lines-overview---lite"></a><span data-ttu-id="ea3c0-103">Visão geral de linhas de cotação baseadas no produto - lite</span><span class="sxs-lookup"><span data-stu-id="ea3c0-103">Product-based quote lines overview - lite</span></span>

<span data-ttu-id="ea3c0-104">_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="ea3c0-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ea3c0-105">Você pode criar linhas de cotação baseadas em produto no Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="ea3c0-105">You can create product-based quote lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="ea3c0-106">As linhas de cotação baseadas no produto podem ser adicionadas manualmente ou podem ser itens do catálogo de produtos.</span><span class="sxs-lookup"><span data-stu-id="ea3c0-106">Product-based quote lines can be manually added, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="ea3c0-107">Catálogo de produtos</span><span class="sxs-lookup"><span data-stu-id="ea3c0-107">Product catalog</span></span>

<span data-ttu-id="ea3c0-108">Cada produto do catálogo de produtos tem uma unidade padrão e um grupo de unidades.</span><span class="sxs-lookup"><span data-stu-id="ea3c0-108">Each product in the product catalog has a default unit and unit group.</span></span> <span data-ttu-id="ea3c0-109">Se vários produtos compartilharem o mesmo conjunto de atributos, será possível criar uma família de produtos que compartilha esses atributos.</span><span class="sxs-lookup"><span data-stu-id="ea3c0-109">If multiple products share the same set of attributes, you can create a product family that share those attributes.</span></span> 

<span data-ttu-id="ea3c0-110">Por exemplo, uma empresa vende licenças de assinatura para diferentes tipos de software.</span><span class="sxs-lookup"><span data-stu-id="ea3c0-110">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="ea3c0-111">Todos os programas de software por assinatura têm os dois seguintes atributos:</span><span class="sxs-lookup"><span data-stu-id="ea3c0-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="ea3c0-112">Número de usuários</span><span class="sxs-lookup"><span data-stu-id="ea3c0-112">Number of users</span></span>
- <span data-ttu-id="ea3c0-113">Duração de uma assinatura medida em meses</span><span class="sxs-lookup"><span data-stu-id="ea3c0-113">A subscription duration measured in months</span></span>

<span data-ttu-id="ea3c0-114">Para manter este tipo de catálogo, crie uma família de produtos chamada **Software por Assinatura** e adicione o número de usuários e a duração da assinatura como atributos.</span><span class="sxs-lookup"><span data-stu-id="ea3c0-114">To maintain this type of catalog, create a product family named **Subscription Software** and add the number of users and the subscription duration as attributes.</span></span> <span data-ttu-id="ea3c0-115">Em seguida, você pode adicionar produtos individuais à família de produtos **Software por Assinatura**.</span><span class="sxs-lookup"><span data-stu-id="ea3c0-115">Next, you can add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="ea3c0-116">Adicionar itens do catálogo de produtos a uma cotação de projeto</span><span class="sxs-lookup"><span data-stu-id="ea3c0-116">Add product catalog items to a project quote</span></span>

<span data-ttu-id="ea3c0-117">As páginas **Cotação do Projeto** e **Contrato do Projeto** têm seções para linhas baseadas nos projetos e no produto.</span><span class="sxs-lookup"><span data-stu-id="ea3c0-117">The **Project Quote** and **Project Contract** pages have sections for project-based lines and product-based lines.</span></span> <span data-ttu-id="ea3c0-118">Para linhas baseados no produto, a lista suspensa na linha de cotação ou na linha de contrato do projeto inclui todos os produtos e unidades na lista de preços do produto.</span><span class="sxs-lookup"><span data-stu-id="ea3c0-118">For product-based lines, the drop-down list on the quote line or project contract line includes all the products and units in the product price list.</span></span> <span data-ttu-id="ea3c0-119">Também é possível adicionar produtos que não fazem parte da lista de preços do produto.</span><span class="sxs-lookup"><span data-stu-id="ea3c0-119">You can also add products that aren't part of the product price list.</span></span>

<span data-ttu-id="ea3c0-120">Além disso, é possível selecionar produtos de outras listas de preços ou diretamente do catálogo de produtos.</span><span class="sxs-lookup"><span data-stu-id="ea3c0-120">Additionally, you can select products from other price lists or directly from the product catalog.</span></span> <span data-ttu-id="ea3c0-121">Quando você seleciona produtos diretamente em um catálogo de produtos, a lista de preços padrão desse produto é usada para se chegar ao preço de vendas dos produtos.</span><span class="sxs-lookup"><span data-stu-id="ea3c0-121">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="ea3c0-122">Se uma lista de preços padrão não for definida, o preço será definido como 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="ea3c0-122">If a default price list isn't set, the price is set to zero (0).</span></span>

<span data-ttu-id="ea3c0-123">Quando uma linha de cotação for baseada em um catálogo de produtos, você poderá substituir o preço de vendas diretamente na linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="ea3c0-123">When a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="ea3c0-124">Uma linha de cotação no campo **Preço** com dois valores disponíveis:</span><span class="sxs-lookup"><span data-stu-id="ea3c0-124">A quote line in **Pricing** field with two available values:</span></span>

- <span data-ttu-id="ea3c0-125">**Substituir Preços**</span><span class="sxs-lookup"><span data-stu-id="ea3c0-125">**Override Pricing**</span></span>
- <span data-ttu-id="ea3c0-126">**Usar Padrão**</span><span class="sxs-lookup"><span data-stu-id="ea3c0-126">**Use Default**</span></span>

<span data-ttu-id="ea3c0-127">Se você selecionar **Substituir Preços**, o preço padrão não será definido.</span><span class="sxs-lookup"><span data-stu-id="ea3c0-127">If you select **Override Pricing**, the default price isn't set.</span></span> <span data-ttu-id="ea3c0-128">Em vez disso, você deve inserir um preço para o produto na linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="ea3c0-128">Instead, you must enter a price for the product on the quote line.</span></span> <span data-ttu-id="ea3c0-129">Se você selecionar **Usar Padrão**, o preço de venda padrão será usado e o campo será bloqueado para edição.</span><span class="sxs-lookup"><span data-stu-id="ea3c0-129">If you select **Use Default**, the default sales price is used and the field is locked for editing.</span></span>

<span data-ttu-id="ea3c0-130">Os preços de venda padrão serão inseridos nas linhas baseadas no produto de uma cotação.</span><span class="sxs-lookup"><span data-stu-id="ea3c0-130">Default sales prices are entered on the product-based lines of a quote.</span></span> <span data-ttu-id="ea3c0-131">O campo **Preço** é definido como **Substituir Preços**, de forma que você possa editar o preço padrão nas linhas de cotação.</span><span class="sxs-lookup"><span data-stu-id="ea3c0-131">The **Pricing** field is then set to **Override Pricing** so that you can edit the default price on the quote lines.</span></span> <span data-ttu-id="ea3c0-132">Esta é uma substituição específica do Project Operations para o comportamento das linhas baseadas no produto no Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="ea3c0-132">This is a Project Operations-specific override to the product-based lines behavior in Dynamics 365 Sales.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]