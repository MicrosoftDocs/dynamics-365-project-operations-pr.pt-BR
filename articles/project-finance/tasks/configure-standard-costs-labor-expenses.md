---
title: Configurar custos padrão para mão de obra e despesas
description: Este tópico explicar como configurar custos padrão para mão de obra e despesas de um projeto.
author: KimANelson
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.assetid: fa7c024f-4b18-4d29-9fd4-9c430cd83fad
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f3e796cc03aeaa28938c56ce37d5075755248dfa
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749166"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="d9362-103">Configurar custos padrão para mão de obra e despesas</span><span class="sxs-lookup"><span data-stu-id="d9362-103">Configure standard costs for labor and expenses</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d9362-104">Este tópico explicar como configurar custos padrão para mão de obra e despesas de um projeto.</span><span class="sxs-lookup"><span data-stu-id="d9362-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="d9362-105">Esta tarefa usa o conjunto de dados USSI.</span><span class="sxs-lookup"><span data-stu-id="d9362-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="d9362-106">No painel de navegação, acesse **Módulos > Gerenciamento e contabilidade de projeto > Configurar > Preços > Preço de custo (hora)**.</span><span class="sxs-lookup"><span data-stu-id="d9362-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="d9362-107">Selecione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="d9362-107">Select **New**.</span></span>
3. <span data-ttu-id="d9362-108">No campo **Data de efetivação**, insira uma data.</span><span class="sxs-lookup"><span data-stu-id="d9362-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="d9362-109">No campo **Preço de custo**, insira um número.</span><span class="sxs-lookup"><span data-stu-id="d9362-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="d9362-110">Você pode configurar um preço de custo padrão para a categoria de projeto ou pode configurar um preço de custo por número de trabalhador, número de projeto, categoria, data ou qualquer combinação dessas opções.</span><span class="sxs-lookup"><span data-stu-id="d9362-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="d9362-111">O preço de custo aplicado é o preço de custo com o maior nível de detalhes.</span><span class="sxs-lookup"><span data-stu-id="d9362-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="d9362-112">Selecione **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="d9362-112">Select **Save**.</span></span>
6. <span data-ttu-id="d9362-113">No painel de navegação, acesse **Módulos > Gerenciamento e contabilidade de projeto > Configurar > Preços > Preço de venda (hora)**.</span><span class="sxs-lookup"><span data-stu-id="d9362-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="d9362-114">Selecione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="d9362-114">Select **New**.</span></span>
8. <span data-ttu-id="d9362-115">No campo **Data de efetivação**, insira uma data.</span><span class="sxs-lookup"><span data-stu-id="d9362-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="d9362-116">No campo **Válido por**, selecione uma opção.</span><span class="sxs-lookup"><span data-stu-id="d9362-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="d9362-117">No campo **Preço**, insira um número.</span><span class="sxs-lookup"><span data-stu-id="d9362-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="d9362-118">Você pode configurar um preço de venda padrão para transações por hora ou para uma categoria de projeto.</span><span class="sxs-lookup"><span data-stu-id="d9362-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="d9362-119">Você também pode configurar preços de venda por número de trabalhador, número de projeto, categoria, data da transação ou qualquer combinação dessas opções.</span><span class="sxs-lookup"><span data-stu-id="d9362-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="d9362-120">O preço de venda real, que é aplicado quando um trabalhador insere uma transação no Diário de horas é o preço de venda com o maior nível de detalhes.</span><span class="sxs-lookup"><span data-stu-id="d9362-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="d9362-121">Por exemplo, se um preço de venda geral e um preço de venda específico de um trabalhador forem configurados, o preço de venda específico do trabalhador será usado.</span><span class="sxs-lookup"><span data-stu-id="d9362-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="d9362-122">Selecione **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="d9362-122">Select **Save**.</span></span>
12. <span data-ttu-id="d9362-123">Feche a página.</span><span class="sxs-lookup"><span data-stu-id="d9362-123">Close the page.</span></span>
13. <span data-ttu-id="d9362-124">No painel de navegação, acesse **Módulos > Gerenciamento e contabilidade de projeto > Configurar > Preços > Preço de custo (despesa)**.</span><span class="sxs-lookup"><span data-stu-id="d9362-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="d9362-125">Selecione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="d9362-125">Select **New**.</span></span>
15. <span data-ttu-id="d9362-126">No campo **Data de efetivação**, insira uma data.</span><span class="sxs-lookup"><span data-stu-id="d9362-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="d9362-127">No campo **Preço de custo**, insira um número.</span><span class="sxs-lookup"><span data-stu-id="d9362-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="d9362-128">Vários campos podem ser preenchidos, mas isso é o mínimo necessário para salvar o registro.</span><span class="sxs-lookup"><span data-stu-id="d9362-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="d9362-129">Selecione **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="d9362-129">Select **Save**.</span></span>
18. <span data-ttu-id="d9362-130">No painel de navegação, acesse **Módulos > Gerenciamento e contabilidade de projeto > Configurar > Preços > Preço de venda (despesa)**.</span><span class="sxs-lookup"><span data-stu-id="d9362-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="d9362-131">Selecione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="d9362-131">Select **New**.</span></span>
20. <span data-ttu-id="d9362-132">No campo **Data de efetivação**, insira uma data.</span><span class="sxs-lookup"><span data-stu-id="d9362-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="d9362-133">No campo **Válido por**, selecione uma opção.</span><span class="sxs-lookup"><span data-stu-id="d9362-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="d9362-134">No campo **Preço**, insira um número.</span><span class="sxs-lookup"><span data-stu-id="d9362-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="d9362-135">O preço de venda real, que é aplicado quando um trabalhador insere transações em um diário de despesas é o preço de venda com o maior nível de detalhes.</span><span class="sxs-lookup"><span data-stu-id="d9362-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="d9362-136">Por exemplo, se um preço de venda geral e um preço de venda específico de um trabalhador forem configurados, o preço de venda específico do trabalhador será usado.</span><span class="sxs-lookup"><span data-stu-id="d9362-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="d9362-137">Selecione **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="d9362-137">Select **Save**.</span></span>

