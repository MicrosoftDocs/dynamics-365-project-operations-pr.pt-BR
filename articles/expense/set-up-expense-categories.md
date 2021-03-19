---
title: Configurar categorias de despesa
description: Este tópico fornece informações sobre como configurar categorias de despesas e categorias compartilhadas para relatórios de despesas.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 1589cf82626e744d35f31fef8e8437a5ad71360d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276109"
---
# <a name="set-up-expense-categories"></a><span data-ttu-id="64d13-103">Configurar categorias de despesa</span><span class="sxs-lookup"><span data-stu-id="64d13-103">Set up expense categories</span></span>

<span data-ttu-id="64d13-104">_**Aplicável A:** Project Operations para cenários baseados em recursos/sem estoque_</span><span class="sxs-lookup"><span data-stu-id="64d13-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="64d13-105">Quando os funcionários criam relatórios de despesas, cada despesa que eles registram deve ser associada a uma categoria de despesas.</span><span class="sxs-lookup"><span data-stu-id="64d13-105">When employees create expense reports, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="64d13-106">As categorias de despesas são derivadas de categorias compartilhadas que podem ser compartilhadas entre as entidades legais em sua organização.</span><span class="sxs-lookup"><span data-stu-id="64d13-106">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="64d13-107">Dependendo de como sua organização é definida, essas categorias de despesas também podem ser compartilhadas em outras áreas.</span><span class="sxs-lookup"><span data-stu-id="64d13-107">Depending on how your organization is defined, these expense categories can also be shared in other areas.</span></span> <span data-ttu-id="64d13-108">Com base na definição da sua organização e orientação da equipe de implementação, você deverá determinar se as categorias que são usadas no gerenciamento de despesas serão usadas apenas no gerenciamento de despesas ou se deverão ser compartilhadas em outras áreas.</span><span class="sxs-lookup"><span data-stu-id="64d13-108">Based on the definition of your organization and guidance from the implementation team, you must determine whether the categories that are used in Expense management will be used only in Expense management or should be shared in other areas.</span></span>

> [!NOTE]
> <span data-ttu-id="64d13-109">Essas categorias podem ser compartilhadas entre Gerenciamento e contabilidade do projeto e Gerenciamento de despesas, ou entre Gerenciamento e contabilidade do projeto e Produção.</span><span class="sxs-lookup"><span data-stu-id="64d13-109">These categories can be shared between Project management and accounting and Expense management, or between Project management and accounting and Production.</span></span> <span data-ttu-id="64d13-110">No entanto, elas não podem ser compartilhadas entre Gerenciamento de despesas e Produção.</span><span class="sxs-lookup"><span data-stu-id="64d13-110">However, they can't be shared between Expense management and Production.</span></span>

<span data-ttu-id="64d13-111">Antes de iniciar o processo de configuração, as seguintes decisões deverão ser tomadas para cada categoria de despesas:</span><span class="sxs-lookup"><span data-stu-id="64d13-111">Before you can begin the setup process, the following decisions must be made for each expense category:</span></span>

- <span data-ttu-id="64d13-112">Qual é a categoria da despesa?</span><span class="sxs-lookup"><span data-stu-id="64d13-112">What is the expense category?</span></span> <span data-ttu-id="64d13-113">Os exemplos incluem categorias para voos, hotel ou milhagem.</span><span class="sxs-lookup"><span data-stu-id="64d13-113">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="64d13-114">A categoria de despesas também pode ser usada no Gerenciamento e contabilidade de projeto?</span><span class="sxs-lookup"><span data-stu-id="64d13-114">Can the expense category also be used in Project management and accounting?</span></span> <span data-ttu-id="64d13-115">Se a respostas for positiva, você também precisará tomar as seguintes decisões:</span><span class="sxs-lookup"><span data-stu-id="64d13-115">If it can, you must also make the following decisions:</span></span>

    - <span data-ttu-id="64d13-116">Quais contas de custo serão usadas para as despesas a seguir?</span><span class="sxs-lookup"><span data-stu-id="64d13-116">Which cost accounts will be used for the following expenses?</span></span>

        - <span data-ttu-id="64d13-117">Custo</span><span class="sxs-lookup"><span data-stu-id="64d13-117">Cost</span></span>
        - <span data-ttu-id="64d13-118">Alocação de folha de pagamento</span><span class="sxs-lookup"><span data-stu-id="64d13-118">Payroll allocation</span></span>
        - <span data-ttu-id="64d13-119">WIP – Valor de custo</span><span class="sxs-lookup"><span data-stu-id="64d13-119">WIP-cost value</span></span>
        - <span data-ttu-id="64d13-120">Custo – Item</span><span class="sxs-lookup"><span data-stu-id="64d13-120">Cost-item</span></span>
        - <span data-ttu-id="64d13-121">WIP – Valor de custo – Item</span><span class="sxs-lookup"><span data-stu-id="64d13-121">WIP-cost value-item</span></span>
        - <span data-ttu-id="64d13-122">Perda acumulada</span><span class="sxs-lookup"><span data-stu-id="64d13-122">Accrued loss</span></span>
        - <span data-ttu-id="64d13-123">WIP – Perda acumulada</span><span class="sxs-lookup"><span data-stu-id="64d13-123">WIP-accrued loss</span></span>

    - <span data-ttu-id="64d13-124">Quais contas de receita serão usadas para as fontes de receita a seguir?</span><span class="sxs-lookup"><span data-stu-id="64d13-124">Which revenue accounts will be used for the following sources of revenue?</span></span>

        - <span data-ttu-id="64d13-125">Receita faturada</span><span class="sxs-lookup"><span data-stu-id="64d13-125">Invoiced revenue</span></span>
        - <span data-ttu-id="64d13-126">Receita acumulada - Valor de venda</span><span class="sxs-lookup"><span data-stu-id="64d13-126">Accrued revenue-sales value</span></span>
        - <span data-ttu-id="64d13-127">WIP – Valor de venda</span><span class="sxs-lookup"><span data-stu-id="64d13-127">WIP-sales value</span></span>
        - <span data-ttu-id="64d13-128">Receita acumulada – Produção</span><span class="sxs-lookup"><span data-stu-id="64d13-128">Accrued revenue-production</span></span>
        - <span data-ttu-id="64d13-129">WIP – Produção</span><span class="sxs-lookup"><span data-stu-id="64d13-129">WIP-production</span></span>
        - <span data-ttu-id="64d13-130">Receita acumulada – Lucro</span><span class="sxs-lookup"><span data-stu-id="64d13-130">Accrued revenue-profit</span></span>
        - <span data-ttu-id="64d13-131">WIP – Lucro</span><span class="sxs-lookup"><span data-stu-id="64d13-131">WIP-profit</span></span>
        - <span data-ttu-id="64d13-132">Receita acumulada – Subscrição</span><span class="sxs-lookup"><span data-stu-id="64d13-132">Accrued revenue-subscription</span></span>
        - <span data-ttu-id="64d13-133">WIP – Subscrição</span><span class="sxs-lookup"><span data-stu-id="64d13-133">WIP-subscription</span></span>

- <span data-ttu-id="64d13-134">Qual é o tipo de despesa?</span><span class="sxs-lookup"><span data-stu-id="64d13-134">What is the expense type?</span></span>
- <span data-ttu-id="64d13-135">Qual é a forma de pagamento padrão para a categoria de despesas?</span><span class="sxs-lookup"><span data-stu-id="64d13-135">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="64d13-136">As despesas na categoria de despesas devem ser discriminadas?</span><span class="sxs-lookup"><span data-stu-id="64d13-136">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="64d13-137">Qual é a conta principal padrão para a categoria de despesas?</span><span class="sxs-lookup"><span data-stu-id="64d13-137">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="64d13-138">Qual é o grupo de impostos do item padrão para a categoria de despesas?</span><span class="sxs-lookup"><span data-stu-id="64d13-138">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="64d13-139">São permitidas formas de pagamento adicionais para a categoria de despesas?</span><span class="sxs-lookup"><span data-stu-id="64d13-139">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="64d13-140">Em caso afirmativo, quais são elas?</span><span class="sxs-lookup"><span data-stu-id="64d13-140">If so, what are they?</span></span>
- <span data-ttu-id="64d13-141">Existem subcategorias nesta categoria de despesas?</span><span class="sxs-lookup"><span data-stu-id="64d13-141">Are there subcategories in this expense category?</span></span> <span data-ttu-id="64d13-142">Se houver subcategorias, você também precisará tomar as seguintes decisões:</span><span class="sxs-lookup"><span data-stu-id="64d13-142">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="64d13-143">Alguma das subcategorias foi excluída da recuperação de impostos?</span><span class="sxs-lookup"><span data-stu-id="64d13-143">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="64d13-144">Qual é o grupo de impostos do item das subcategorias?</span><span class="sxs-lookup"><span data-stu-id="64d13-144">What is the item sales tax group of the subcategories?</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]