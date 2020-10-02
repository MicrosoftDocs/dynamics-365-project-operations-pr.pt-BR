---
title: Configuração da lista de preços de vendas
description: Este tópico fornece informações sobre listas de preços de vendas para precificação de projetos.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 2a66802adfcadab7b4d34149b146ca3cb27c903e
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896447"
---
# <a name="sales-price-list-setup"></a><span data-ttu-id="3cef2-103">Configuração da lista de preços de vendas</span><span class="sxs-lookup"><span data-stu-id="3cef2-103">Sales price list setup</span></span>

<span data-ttu-id="3cef2-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pró-forma_</span><span class="sxs-lookup"><span data-stu-id="3cef2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3cef2-105">Em cotações e contratos do projeto, uma lista de preços de projeto tem um padrão de substituição de preço diferente de uma lista de preços de produto.</span><span class="sxs-lookup"><span data-stu-id="3cef2-105">For project quotes and contracts, a project price list has a different price override pattern than a product price list.</span></span> <span data-ttu-id="3cef2-106">Em uma linha de cotação baseada em catálogo de produtos, você pode substituir o preço de funções e categorias diretamente na linha de cotação, pois cada linha de cotação aponta exatamente para um item do catálogo.</span><span class="sxs-lookup"><span data-stu-id="3cef2-106">On a product catalog–based quote line, you can override the price to roles and categories directly on the quote line, because each quote line points to exactly one catalog item.</span></span> <span data-ttu-id="3cef2-107">No entanto, em uma linha de cotação baseada em projeto, não é possível substituir o preço de funções e categorias diretamente na linha de cotação.</span><span class="sxs-lookup"><span data-stu-id="3cef2-107">However, on a project-based quote line, you can't override the price to roles and categories directly on the quote line.</span></span> <span data-ttu-id="3cef2-108">Você pode usar a lista de preços de projeto para trabalhar com os dois padrões de substituição distintos.</span><span class="sxs-lookup"><span data-stu-id="3cef2-108">You can use the project price list to work with the two distinct override patterns.</span></span>

> [!NOTE]
> <span data-ttu-id="3cef2-109">É recomendável ter uma lista de preços separada para seus recursos de projeto e itens de catálogo devido às diferenças de comportamento entre as duas quando você substitui preços.</span><span class="sxs-lookup"><span data-stu-id="3cef2-109">We recommend that you have a separate price list for your project resources and your catalog items, because of the behavior differences between the two when you override pricing.</span></span>

<span data-ttu-id="3cef2-110">Cada uma das seguintes entidades pode ter uma ou mais listas de preços de vendas associadas para preço de projeto:</span><span class="sxs-lookup"><span data-stu-id="3cef2-110">Each of the following entities can have one or more associated sales price lists for project pricing:</span></span>

- <span data-ttu-id="3cef2-111">Cliente (conta)</span><span class="sxs-lookup"><span data-stu-id="3cef2-111">Customer (account)</span></span> 
- <span data-ttu-id="3cef2-112">Oportunidade</span><span class="sxs-lookup"><span data-stu-id="3cef2-112">Opportunity</span></span> 
- <span data-ttu-id="3cef2-113">Cotação</span><span class="sxs-lookup"><span data-stu-id="3cef2-113">Quote</span></span> 
- <span data-ttu-id="3cef2-114">Contrato de Projeto</span><span class="sxs-lookup"><span data-stu-id="3cef2-114">Project Contract</span></span>

<span data-ttu-id="3cef2-115">A associação dessas entidades a uma lista de preços é indicada pelas listas de preços de projeto.</span><span class="sxs-lookup"><span data-stu-id="3cef2-115">The association of these entities with a price list is indicated by the project price lists.</span></span> <span data-ttu-id="3cef2-116">Você pode associar uma ou mais listas de preços às entidades de vendas Cliente, Oportunidade, Cotação e Contrato de Projeto.</span><span class="sxs-lookup"><span data-stu-id="3cef2-116">You can associate one or more price lists with the Customer, Opportunity, Quote, and Project Contract sales entities.</span></span>

<span data-ttu-id="3cef2-117">Uma lista de preços de projeto padrão não é inserida automaticamente em um registro do cliente.</span><span class="sxs-lookup"><span data-stu-id="3cef2-117">A default project price list isn't automatically entered on a customer record.</span></span> <span data-ttu-id="3cef2-118">No entanto, você pode anexar manualmente uma lista de preços de projeto ao registro do cliente.</span><span class="sxs-lookup"><span data-stu-id="3cef2-118">However, you can manually attach a project price list to the customer record.</span></span> <span data-ttu-id="3cef2-119">Todavia, você deve anexar manualmente uma lista de preço de projeto somente quando tiver um contrato de preço personalizado com o cliente.</span><span class="sxs-lookup"><span data-stu-id="3cef2-119">Nevertheless, you should manually attach a project price list only when you have a custom pricing agreement with the customer.</span></span> 

<span data-ttu-id="3cef2-120">Quando uma lista de preços de projeto é anexada a uma entidade de vendas, as seguintes informações são validadas:</span><span class="sxs-lookup"><span data-stu-id="3cef2-120">When a project price list is attached to a sales entity, the following information is validated:</span></span>

- <span data-ttu-id="3cef2-121">A lista de preços tem um contexto de **Vendas**.</span><span class="sxs-lookup"><span data-stu-id="3cef2-121">The price list has a context of **Sales**.</span></span> 
- <span data-ttu-id="3cef2-122">A moeda da lista de preços corresponde à moeda do cliente.</span><span class="sxs-lookup"><span data-stu-id="3cef2-122">The price list currency matches the customer currency.</span></span> 

<span data-ttu-id="3cef2-123">Em um contrato de projeto, a seguinte ordem de precedência é usada para definir automaticamente as listas de preços de projetos relacionadas:</span><span class="sxs-lookup"><span data-stu-id="3cef2-123">On a project contract, the following order of precedence is used to automatically set related project price lists:</span></span>

1. <span data-ttu-id="3cef2-124">Cotação</span><span class="sxs-lookup"><span data-stu-id="3cef2-124">Quote</span></span>
2. <span data-ttu-id="3cef2-125">Oportunidade</span><span class="sxs-lookup"><span data-stu-id="3cef2-125">Opportunity</span></span>
3. <span data-ttu-id="3cef2-126">Cliente</span><span class="sxs-lookup"><span data-stu-id="3cef2-126">Customer</span></span> 
4. <span data-ttu-id="3cef2-127">Configurações globais</span><span class="sxs-lookup"><span data-stu-id="3cef2-127">Global settings</span></span> 

<span data-ttu-id="3cef2-128">Quando uma lista de preços de projeto é inserida por padrão, o sistema valida que a moeda corresponde à moeda do cliente e que as listas de preços padrão que foram inseridas têm um contexto de **Vendas**.</span><span class="sxs-lookup"><span data-stu-id="3cef2-128">When a project price list is entered by default, the system validates that the currency matches the customer’s currency, and that the default price lists that have been entered have a context of **Sales**.</span></span>

<span data-ttu-id="3cef2-129">Você pode associar várias listas de preços de projeto às entidades Cliente, Oportunidade, Cotação e Contrato de Projeto.</span><span class="sxs-lookup"><span data-stu-id="3cef2-129">You can associate multiple project price lists with the Customer, Opportunity, Quote, and Project Contract entities.</span></span> <span data-ttu-id="3cef2-130">Esse recurso aceita preços padrão específicos de data para um contrato de projeto de longa duração, onde você pode exigir mais de uma lista de preços para considerar atualizações de preço que ocorrem por conta da inflação.</span><span class="sxs-lookup"><span data-stu-id="3cef2-130">This capability supports date-specific default prices for a long-running project contract, where you might require more than one price list to account for price updates that occur because of inflation.</span></span> <span data-ttu-id="3cef2-131">No entanto, se as listas de preços que você associa à entidade Cliente, Oportunidade, Cotação ou Contrato de Projeto tiverem sobreposição de data efetiva, os preços padrão poderão estar incorretos.</span><span class="sxs-lookup"><span data-stu-id="3cef2-131">However, if the price lists that you associate with the Customer, Opportunity, Quote, or Project Contract entity have overlapping date effectivity, the default prices might be incorrect.</span></span> <span data-ttu-id="3cef2-132">Desse modo, é preciso ter certeza de que as listas de preços de projeto que tenham sobreposição de data efetiva não sejam associadas a essas entidades.</span><span class="sxs-lookup"><span data-stu-id="3cef2-132">Therefore, you should make sure that project price lists that have overlapping date effectivity aren't associated with those entities.</span></span>
