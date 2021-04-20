---
title: Listas de preços de produtos
description: Este tópico fornece informações sobre as listas de preços em preços de catálogo usados para cotações e contratos de projetos.
author: rumant
manager: AnnBe
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e37f0bf9eef946ab4ebd658cef4e1269cbaf686d
ms.sourcegitcommit: ac90be6106592f883a0de39a75836fb40255d65a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2021
ms.locfileid: "5877476"
---
# <a name="product-price-lists"></a><span data-ttu-id="6c23d-103">Listas de preços de produtos</span><span class="sxs-lookup"><span data-stu-id="6c23d-103">Product price lists</span></span>

<span data-ttu-id="6c23d-104">_**Aplica-se a:** Implantação leve - gerenciar faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="6c23d-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

 <span data-ttu-id="6c23d-105">Em Project Operations, **Listas de preços de produtos** e entidades de itens de lista de preços relacionadas dão suporte à funcionalidade para produtos de preços em linhas de contrato e cotação baseada em produto.</span><span class="sxs-lookup"><span data-stu-id="6c23d-105">In Project Operations, **Product price lists** and related price list item entities support functionality for pricing products on product-based quote and contract lines.</span></span> <span data-ttu-id="6c23d-106">Para produtos usados em projetos, os registros de item da lista de preços para listas de preços do projeto são usados.</span><span class="sxs-lookup"><span data-stu-id="6c23d-106">For products used on projects, the price list item records for project price lists are used.</span></span> 

<span data-ttu-id="6c23d-107">Os produtos devem ser configurados para que tenham listas de preços e custos padrão no catálogo de produtos.</span><span class="sxs-lookup"><span data-stu-id="6c23d-107">Products should be set up so that they have default cost and price lists in the product catalog.</span></span> <span data-ttu-id="6c23d-108">Use o preço da listas, o custo padrão e o custo atual para configurar preços de lista e custos padrão.</span><span class="sxs-lookup"><span data-stu-id="6c23d-108">Use the list price, standard cost, and current cost to configure default cost and list prices.</span></span> <span data-ttu-id="6c23d-109">Os preços de lista padrão são usados em uma linha de cotação ou linha de contrato do projeto somente quando o sistema não pode encontrar uma linha da lista de preços para esse produto na lista de preços do produto para a cotação ou o contrato do projeto.</span><span class="sxs-lookup"><span data-stu-id="6c23d-109">The default list prices are used on a quote line or a project contract line only when the system can't find a price list line for that product in the product price list for the quote or project contract.</span></span>

<span data-ttu-id="6c23d-110">O preço de custo das linhas do catálogo de produtos pode ser alterado entre cotações.</span><span class="sxs-lookup"><span data-stu-id="6c23d-110">The cost price of product catalog lines can be changed between quotes.</span></span> <span data-ttu-id="6c23d-111">Esse recurso é importante, pois se você não rastrear precisamente os custos, não será possível determinar os lucros operacionais nas participações do projeto.</span><span class="sxs-lookup"><span data-stu-id="6c23d-111">This capability is important, because if you don't accurately track costs, you can't determine operational profits on project engagements.</span></span> <span data-ttu-id="6c23d-112">A regra geral é usar o custo padrão do produto como o preço de custo.</span><span class="sxs-lookup"><span data-stu-id="6c23d-112">By default, the standard cost of the product is used as the cost price.</span></span> <span data-ttu-id="6c23d-113">Entretanto, o preço de custo padrão pode ser atualizado na linha de cotação se houver um preço de custo diferente para essa cotação.</span><span class="sxs-lookup"><span data-stu-id="6c23d-113">However, the default cost price can be updated on the quote line if there's a different cost price for that quote.</span></span>

## <a name="price-list-items"></a><span data-ttu-id="6c23d-114">Itens da lista de preços</span><span class="sxs-lookup"><span data-stu-id="6c23d-114">Price list items</span></span>

<span data-ttu-id="6c23d-115">É possível adicionar produtos de um catálogo de produtos a diferentes listas de preços.</span><span class="sxs-lookup"><span data-stu-id="6c23d-115">You can add products from a product catalog to different price lists.</span></span> <span data-ttu-id="6c23d-116">As linhas da lista de preços para produtos sempre fazem referência a uma unidade específica.</span><span class="sxs-lookup"><span data-stu-id="6c23d-116">Price list lines for products always reference a specific unit.</span></span> <span data-ttu-id="6c23d-117">O preço de um produto em itens da lista de preços pode ser configurado como um valor monetário.</span><span class="sxs-lookup"><span data-stu-id="6c23d-117">Pricing for a product on price list items can be configured as a currency amount.</span></span> <span data-ttu-id="6c23d-118">Como alternativa, ele pode ser configurado como uma função do preço de lista, custo atual ou custo padrão.</span><span class="sxs-lookup"><span data-stu-id="6c23d-118">Alternatively, it can be configured as a function of the list price, current cost, or standard cost.</span></span>

<span data-ttu-id="6c23d-119">A funcionalidade de preços dá suporte a várias opções de arredondamento quando os preços de produtos são configurados como uma função de preço de lista, custo padrão ou custo atual.</span><span class="sxs-lookup"><span data-stu-id="6c23d-119">Pricing functionality supports various rounding options when product prices are configured as a function of the list price, standard cost, or current cost.</span></span> <span data-ttu-id="6c23d-120">Além de aproveitar vários métodos de precificação e opções de arredondamento, você pode associar listas de descontos a itens da lista de preços.</span><span class="sxs-lookup"><span data-stu-id="6c23d-120">In addition to taking advantage of multiple pricing methods and rounding options, you can associate discount lists with price list items.</span></span> 

 
## <a name="default-product-price-list"></a><span data-ttu-id="6c23d-121">Lista de preços padrão do produto</span><span class="sxs-lookup"><span data-stu-id="6c23d-121">Default product price list</span></span>
<span data-ttu-id="6c23d-122">Cada registro do cliente tem um campo **Lista de Preços Padrão**, onde é possível especificar uma lista de preços que corresponda a moeda do cliente.</span><span class="sxs-lookup"><span data-stu-id="6c23d-122">Each customer record has a **Default Price List** field, where you can specify a price list that matches the currency of the customer.</span></span> <span data-ttu-id="6c23d-123">Um valor padrão não é inserido automaticamente nesse campo.</span><span class="sxs-lookup"><span data-stu-id="6c23d-123">A default value isn't automatically entered in this field.</span></span> <span data-ttu-id="6c23d-124">Quando existe um contrato de preço personalizado com um cliente específico, é possível usar esse campo para associar uma lista de preços a esse cliente.</span><span class="sxs-lookup"><span data-stu-id="6c23d-124">When a custom pricing agreement with a specific customer exists, you can use this field to associate a price list with that customer.</span></span>

<span data-ttu-id="6c23d-125">As entidades Oportunidade, Cotação e Contrato de Projeto usam a ordem a seguir para inserir listas de preços padrão do produto.</span><span class="sxs-lookup"><span data-stu-id="6c23d-125">The Opportunity, Quote, and Project Contract entities use the following order to enter default product price lists.</span></span> <span data-ttu-id="6c23d-126">A mesma ordem é usada para listas de preços do projeto.</span><span class="sxs-lookup"><span data-stu-id="6c23d-126">The same order is used for project price lists.</span></span>

1.  <span data-ttu-id="6c23d-127">Cotação</span><span class="sxs-lookup"><span data-stu-id="6c23d-127">Quote</span></span>
2.  <span data-ttu-id="6c23d-128">Oportunidade</span><span class="sxs-lookup"><span data-stu-id="6c23d-128">Opportunity</span></span>
3.  <span data-ttu-id="6c23d-129">Cliente</span><span class="sxs-lookup"><span data-stu-id="6c23d-129">Customer</span></span>
4.  <span data-ttu-id="6c23d-130">Configurações globais</span><span class="sxs-lookup"><span data-stu-id="6c23d-130">Global settings</span></span> 

<span data-ttu-id="6c23d-131">Por padrão, o campo **Produto** na linha de cotação lista todos os produtos ativos na lista de preços de produto da cotação.</span><span class="sxs-lookup"><span data-stu-id="6c23d-131">By default, the **Product** field on the quote line lists all the active products in the product price list of the quote.</span></span> <span data-ttu-id="6c23d-132">Se um produto foi inativado, ou se for um produto em rascunho, ele não será listado, mesmo se estiver na lista de preços.</span><span class="sxs-lookup"><span data-stu-id="6c23d-132">If a product has been inactivated, or if it's a draft product, it isn't listed, even if it's in the price list.</span></span> 

<span data-ttu-id="6c23d-133">As linhas do catálogo de produtos são adicionadas como linhas da fatura na primeira fatura que é criada para um contrato de projeto.</span><span class="sxs-lookup"><span data-stu-id="6c23d-133">Product catalog lines are added as invoice lines on the first invoice that is created for a project contract.</span></span> <span data-ttu-id="6c23d-134">Em uma fatura de rascunho, essas linhas de fatura podem ser excluídas.</span><span class="sxs-lookup"><span data-stu-id="6c23d-134">On a draft invoice, those invoice lines can be deleted.</span></span> <span data-ttu-id="6c23d-135">Nesse caso, as linhas aparecerão em uma fatura subsequente até que sejam faturadas, ou até que a fatura seja enviada ao cliente.</span><span class="sxs-lookup"><span data-stu-id="6c23d-135">In that case, the lines will appear on a subsequent invoice until they are invoiced, or until the invoice is sent to the customer.</span></span> <span data-ttu-id="6c23d-136">Não é possível faturar uma quantidade parcial de uma linha de fatura do produto.</span><span class="sxs-lookup"><span data-stu-id="6c23d-136">You can't invoice a partial quantity of a product invoice line.</span></span> <span data-ttu-id="6c23d-137">Quando as linhas de produto do contrato do projeto são faturadas, dados reais são criados.</span><span class="sxs-lookup"><span data-stu-id="6c23d-137">When the product lines from the project contract are invoiced, actuals are created.</span></span> <span data-ttu-id="6c23d-138">No entanto, esses dados reais não são vinculados à entidade de projeto relacionada.</span><span class="sxs-lookup"><span data-stu-id="6c23d-138">However, those actuals aren't linked to the related project entity.</span></span> <span data-ttu-id="6c23d-139">Em outras palavras, as linhas de contrato do projeto baseadas em produto são independentes de qualquer uso baseado em projeto.</span><span class="sxs-lookup"><span data-stu-id="6c23d-139">In other words, product-based project contract lines are independent of any project-based use.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
