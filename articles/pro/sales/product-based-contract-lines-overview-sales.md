---
title: Visão geral de linhas de contrato baseadas em produto - lite
description: Este tópico fornece informações sobre linhas de contrato baseadas em produto.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6e9ef33cc9c79f828e85733f4f5a199bce842700
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272644"
---
# <a name="product-based-contract-lines-overview---lite"></a><span data-ttu-id="120ce-103">Visão geral de linhas de contrato baseadas em produto - lite</span><span class="sxs-lookup"><span data-stu-id="120ce-103">Product-based contract lines overview - lite</span></span>

<span data-ttu-id="120ce-104">_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="120ce-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="120ce-105">Você pode criar linhas de contrato baseadas em produto no Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="120ce-105">You can create product-based contract lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="120ce-106">As linhas de contrato baseadas em produto podem ser linhas criadas manualmente ou podem ser itens do catálogo de produtos.</span><span class="sxs-lookup"><span data-stu-id="120ce-106">Product-based contract lines can be manually created lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="120ce-107">Catálogo de produtos</span><span class="sxs-lookup"><span data-stu-id="120ce-107">Product catalog</span></span>

<span data-ttu-id="120ce-108">Os produtos no catálogo de produtos têm uma unidade e um grupo de unidades padrão.</span><span class="sxs-lookup"><span data-stu-id="120ce-108">The products in the product catalog have a default unit and unit group.</span></span> <span data-ttu-id="120ce-109">Se vários produtos compartilharem o mesmo conjunto de atributos, será possível criar uma família de produtos que também tenha esses atributos.</span><span class="sxs-lookup"><span data-stu-id="120ce-109">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="120ce-110">Todos os produtos em uma família de produtos herdam o mesmo conjunto de atributos.</span><span class="sxs-lookup"><span data-stu-id="120ce-110">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="120ce-111">Por exemplo, uma empresa vende licenças de assinatura para diferentes tipos de software.</span><span class="sxs-lookup"><span data-stu-id="120ce-111">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="120ce-112">Todos os programas de software por assinatura têm os dois seguintes atributos:</span><span class="sxs-lookup"><span data-stu-id="120ce-112">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="120ce-113">Número de usuários</span><span class="sxs-lookup"><span data-stu-id="120ce-113">Number of users</span></span>
- <span data-ttu-id="120ce-114">Duração da assinatura (em meses)</span><span class="sxs-lookup"><span data-stu-id="120ce-114">Subscription duration (in months)</span></span>

<span data-ttu-id="120ce-115">Para manter esse tipo de catálogo, crie uma família de produtos chamada **Software de Assinatura**.</span><span class="sxs-lookup"><span data-stu-id="120ce-115">To maintain this type of catalog, create a product family that is named **Subscription Software**.</span></span> <span data-ttu-id="120ce-116">Adicione os atributos **Número de usuários** e **Duração da assinatura** para a família de produtos.</span><span class="sxs-lookup"><span data-stu-id="120ce-116">Add the attributes, **Number of users** and **Subscription duration** to the product family.</span></span> <span data-ttu-id="120ce-117">Em seguida, adicione produtos individuais à família de produtos **Software de Assinatura**.</span><span class="sxs-lookup"><span data-stu-id="120ce-117">Then, add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-contract"></a><span data-ttu-id="120ce-118">Adicionar itens do catálogo de produtos a um contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="120ce-118">Add product catalog items to a project Contract</span></span>

<span data-ttu-id="120ce-119">Os contratos de projeto têm seções para dois tipos de linhas baseadas em projeto e baseadas em produto.</span><span class="sxs-lookup"><span data-stu-id="120ce-119">Project contracts have sections for two types of lines, project-based and product-based.</span></span> <span data-ttu-id="120ce-120">As linhas baseadas em produto incluem todos os produtos e unidades da lista de preços de produtos do contrato.</span><span class="sxs-lookup"><span data-stu-id="120ce-120">Product-based lines include all of the products and units in the product price list on the contract.</span></span> <span data-ttu-id="120ce-121">Produtos que não fazem parte da lista de preços de produtos do contrato podem ser adicionados.</span><span class="sxs-lookup"><span data-stu-id="120ce-121">Products that aren't part of contract's product price list can be added.</span></span>

<span data-ttu-id="120ce-122">Você pode selecionar produtos de outras listas de preços ou diretamente do catálogo de produtos.</span><span class="sxs-lookup"><span data-stu-id="120ce-122">You can select products from other price lists, or directly from the product catalog.</span></span> <span data-ttu-id="120ce-123">Quando você seleciona produtos diretamente em um catálogo de produtos, a lista de preços padrão desse produto é usada para se chegar ao preço de vendas dos produtos.</span><span class="sxs-lookup"><span data-stu-id="120ce-123">When you select products directly from a product catalog, the default price list of that product is used for the product's sales price.</span></span> <span data-ttu-id="120ce-124">Se uma lista de preços padrão não for definida, o preço será definido como 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="120ce-124">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="120ce-125">Se uma linha de contrato for baseada em um catálogo de produtos, você poderá substituir o preço de vendas diretamente na linha de contrato.</span><span class="sxs-lookup"><span data-stu-id="120ce-125">If a contract line is based on a product catalog, you can override the sales price directly on the line.</span></span> <span data-ttu-id="120ce-126">Uma linha de contrato tem o campo **Preço** com os dois valores:</span><span class="sxs-lookup"><span data-stu-id="120ce-126">A contract line has the **Pricing** field with the two values:</span></span>

- <span data-ttu-id="120ce-127">**Substituir preço**</span><span class="sxs-lookup"><span data-stu-id="120ce-127">**Override pricing**</span></span>
- <span data-ttu-id="120ce-128">**Usar padrão**</span><span class="sxs-lookup"><span data-stu-id="120ce-128">**Use default**</span></span>

<span data-ttu-id="120ce-129">Se você definir o campo **Preço** como **Substituir preço**, o preço padrão não será definido.</span><span class="sxs-lookup"><span data-stu-id="120ce-129">If you set the **Pricing** field to **Override pricing**, the default price isn't set.</span></span> <span data-ttu-id="120ce-130">Insira um preço para o produto na linha de contrato.</span><span class="sxs-lookup"><span data-stu-id="120ce-130">Enter a price for the product on the contract line.</span></span> <span data-ttu-id="120ce-131">Se você definir o campo como **Usar padrão**, o preço de venda padrão será usado e o campo não poderá ser editado.</span><span class="sxs-lookup"><span data-stu-id="120ce-131">If you set the field to **Use default**, the default sales price is used and the field can't be edited.</span></span>

<span data-ttu-id="120ce-132">Após a instalação do Project Operations, os preços de vendas padrão são inseridos nas linhas baseadas em produto em um contrato.</span><span class="sxs-lookup"><span data-stu-id="120ce-132">After you install Project Operations, default sales prices are entered on the product-based lines on a contract.</span></span> <span data-ttu-id="120ce-133">O campo **Preço** é definido como **Substituir preço** para que seja possível editar o preço padrão nas linhas de contrato.</span><span class="sxs-lookup"><span data-stu-id="120ce-133">The **Pricing** field is set to **Override pricing** so that you can edit the default price on the contract lines.</span></span> <span data-ttu-id="120ce-134">Esta é uma substituição específica do Project Operations para o comportamento das linhas baseadas no produto no Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="120ce-134">This is a Project Operations-specific override to product-based lines behavior in Dynamics 365 Sales.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]