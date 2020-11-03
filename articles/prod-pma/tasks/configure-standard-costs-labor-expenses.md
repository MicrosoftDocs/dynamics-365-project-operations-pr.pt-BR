---
title: Configurar custos padrão para mão de obra e despesas
description: Este tópico explicar como configurar custos padrão para mão de obra e despesas de um projeto.
author: Yowelle
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
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b3eb6b1d4d75b095383689dd53a59a15fe9e884a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071485"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="c860f-103">Configurar custos padrão para mão de obra e despesas</span><span class="sxs-lookup"><span data-stu-id="c860f-103">Configure standard costs for labor and expenses</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c860f-104">Este tópico explicar como configurar custos padrão para mão de obra e despesas de um projeto.</span><span class="sxs-lookup"><span data-stu-id="c860f-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="c860f-105">Esta tarefa usa o conjunto de dados USSI.</span><span class="sxs-lookup"><span data-stu-id="c860f-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="c860f-106">No painel de navegação, acesse **Módulos > Gerenciamento e contabilidade de projeto > Configurar > Preços > Preço de custo (hora)**.</span><span class="sxs-lookup"><span data-stu-id="c860f-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="c860f-107">Selecione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="c860f-107">Select **New**.</span></span>
3. <span data-ttu-id="c860f-108">No campo **Data de efetivação** , insira uma data.</span><span class="sxs-lookup"><span data-stu-id="c860f-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="c860f-109">No campo **Preço de custo** , insira um número.</span><span class="sxs-lookup"><span data-stu-id="c860f-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="c860f-110">Você pode configurar um preço de custo padrão para a categoria de projeto ou pode configurar um preço de custo por número de trabalhador, número de projeto, categoria, data ou qualquer combinação dessas opções.</span><span class="sxs-lookup"><span data-stu-id="c860f-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="c860f-111">O preço de custo aplicado é o preço de custo com o maior nível de detalhes.</span><span class="sxs-lookup"><span data-stu-id="c860f-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="c860f-112">Selecione **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="c860f-112">Select **Save**.</span></span>
6. <span data-ttu-id="c860f-113">No painel de navegação, acesse **Módulos > Gerenciamento e contabilidade de projeto > Configurar > Preços > Preço de venda (hora)**.</span><span class="sxs-lookup"><span data-stu-id="c860f-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="c860f-114">Selecione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="c860f-114">Select **New**.</span></span>
8. <span data-ttu-id="c860f-115">No campo **Data de efetivação** , insira uma data.</span><span class="sxs-lookup"><span data-stu-id="c860f-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="c860f-116">No campo **Válido por** , selecione uma opção.</span><span class="sxs-lookup"><span data-stu-id="c860f-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="c860f-117">No campo **Preço** , insira um número.</span><span class="sxs-lookup"><span data-stu-id="c860f-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="c860f-118">Você pode configurar um preço de venda padrão para transações por hora ou para uma categoria de projeto.</span><span class="sxs-lookup"><span data-stu-id="c860f-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="c860f-119">Você também pode configurar preços de venda por número de trabalhador, número de projeto, categoria, data da transação ou qualquer combinação dessas opções.</span><span class="sxs-lookup"><span data-stu-id="c860f-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="c860f-120">O preço de venda real, que é aplicado quando um trabalhador insere uma transação no Diário de horas é o preço de venda com o maior nível de detalhes.</span><span class="sxs-lookup"><span data-stu-id="c860f-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="c860f-121">Por exemplo, se um preço de venda geral e um preço de venda específico de um trabalhador forem configurados, o preço de venda específico do trabalhador será usado.</span><span class="sxs-lookup"><span data-stu-id="c860f-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="c860f-122">Selecione **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="c860f-122">Select **Save**.</span></span>
12. <span data-ttu-id="c860f-123">Feche a página.</span><span class="sxs-lookup"><span data-stu-id="c860f-123">Close the page.</span></span>
13. <span data-ttu-id="c860f-124">No painel de navegação, acesse **Módulos > Gerenciamento e contabilidade de projeto > Configurar > Preços > Preço de custo (despesa)**.</span><span class="sxs-lookup"><span data-stu-id="c860f-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="c860f-125">Selecione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="c860f-125">Select **New**.</span></span>
15. <span data-ttu-id="c860f-126">No campo **Data de efetivação** , insira uma data.</span><span class="sxs-lookup"><span data-stu-id="c860f-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="c860f-127">No campo **Preço de custo** , insira um número.</span><span class="sxs-lookup"><span data-stu-id="c860f-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="c860f-128">Vários campos podem ser preenchidos, mas isso é o mínimo necessário para salvar o registro.</span><span class="sxs-lookup"><span data-stu-id="c860f-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="c860f-129">Selecione **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="c860f-129">Select **Save**.</span></span>
18. <span data-ttu-id="c860f-130">No painel de navegação, acesse **Módulos > Gerenciamento e contabilidade de projeto > Configurar > Preços > Preço de venda (despesa)**.</span><span class="sxs-lookup"><span data-stu-id="c860f-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="c860f-131">Selecione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="c860f-131">Select **New**.</span></span>
20. <span data-ttu-id="c860f-132">No campo **Data de efetivação** , insira uma data.</span><span class="sxs-lookup"><span data-stu-id="c860f-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="c860f-133">No campo **Válido por** , selecione uma opção.</span><span class="sxs-lookup"><span data-stu-id="c860f-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="c860f-134">No campo **Preço** , insira um número.</span><span class="sxs-lookup"><span data-stu-id="c860f-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="c860f-135">O preço de venda real, que é aplicado quando um trabalhador insere transações em um diário de despesas é o preço de venda com o maior nível de detalhes.</span><span class="sxs-lookup"><span data-stu-id="c860f-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="c860f-136">Por exemplo, se um preço de venda geral e um preço de venda específico de um trabalhador forem configurados, o preço de venda específico do trabalhador será usado.</span><span class="sxs-lookup"><span data-stu-id="c860f-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="c860f-137">Selecione **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="c860f-137">Select **Save**.</span></span>

