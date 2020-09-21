---
title: Desativar uma dimensão de precificação
description: Este tópico mostra como configurar dimensões de precificação na solução Project Service.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 689e5a8d-e39a-471d-a6c4-7e2fc3bb5590
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 5cf2cd86fb1eba50c8e08b2bd624669ab0b1deb3
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749113"
---
# <a name="turn-off-a-pricing-dimension"></a><span data-ttu-id="e9c46-103">Desativar uma dimensão de precificação</span><span class="sxs-lookup"><span data-stu-id="e9c46-103">Turn off a pricing dimension</span></span>

<span data-ttu-id="e9c46-104">Pode ser necessário analisar e atualizar sua estratégia de precificação de tempos a tempos.</span><span class="sxs-lookup"><span data-stu-id="e9c46-104">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="e9c46-105">Quaisquer atualizações que você fizer podem exigir que você desative uma dimensão de precificação existente e crie uma outra.</span><span class="sxs-lookup"><span data-stu-id="e9c46-105">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="e9c46-106">Por exemplo, você pode ter precificado anteriormente por **Função**, mas agora optou por **Experiência de trabalho**.</span><span class="sxs-lookup"><span data-stu-id="e9c46-106">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="e9c46-107">Isso pode exigir que você desative **Função** como uma dimensão de precificação e crie **Experiência de trabalho** como uma nova dimensão de precificação.</span><span class="sxs-lookup"><span data-stu-id="e9c46-107">This may require you to turn off **Role** as a pricing dimension and create **Work Expereince** as a new pricing dimension.</span></span> 

<span data-ttu-id="e9c46-108">É possível desativar uma dimensão de precificação, independentemente de ser predefinida ou personalizada, definindo os campos **Aplicável ao custo** e **Aplicável a vendas** da dimensão de precificação como **Não**.</span><span class="sxs-lookup"><span data-stu-id="e9c46-108">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="e9c46-109">Contudo, ao fazer isso, você receberá a mensagem de erro a seguir.</span><span class="sxs-lookup"><span data-stu-id="e9c46-109">However, when you do this, you might receive the following error message.</span></span>

![É provável que haja um erro no processo de negócios ao desativar uma dimensão de precificação](media/Business-Process-Error.png)


<span data-ttu-id="e9c46-111">Essa mensagem de erro indica que existem registros de preços configurados anteriormente para a dimensão que está sendo desativada.</span><span class="sxs-lookup"><span data-stu-id="e9c46-111">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="e9c46-112">Todos os registros **Preço da Função** e **Markup de Preço da Função** que se referem a uma dimensão devem ser excluídos antes que a aplicabilidade da dimensão possa ser definida como **Não**.</span><span class="sxs-lookup"><span data-stu-id="e9c46-112">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="e9c46-113">Esta regra se aplica às dimensões de precificação predefinidas e a quaisquer dimensões de precificação personalizadas que você possa ter criado.</span><span class="sxs-lookup"><span data-stu-id="e9c46-113">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="e9c46-114">O motivo dessa validação é porque o Project Service tem uma restrição de que cada registro **Preço da Função** deve ter uma combinação exclusiva de dimensões.</span><span class="sxs-lookup"><span data-stu-id="e9c46-114">The reason for this validation is because Project Service has a constraint that each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="e9c46-115">Por exemplo, em uma lista de preços chamada **US Cost Rates 2018**, você tem a seguinte linha **Preço da função**.</span><span class="sxs-lookup"><span data-stu-id="e9c46-115">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="e9c46-116">Título padrão</span><span class="sxs-lookup"><span data-stu-id="e9c46-116">Standard Title</span></span>         | <span data-ttu-id="e9c46-117">Unidades Organizacionais</span><span class="sxs-lookup"><span data-stu-id="e9c46-117">Org Unit</span></span>    |<span data-ttu-id="e9c46-118">Unidade</span><span class="sxs-lookup"><span data-stu-id="e9c46-118">Unit</span></span>   |<span data-ttu-id="e9c46-119">Preço</span><span class="sxs-lookup"><span data-stu-id="e9c46-119">Price</span></span>  |<span data-ttu-id="e9c46-120">Moeda</span><span class="sxs-lookup"><span data-stu-id="e9c46-120">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="e9c46-121">Engenheiro de sistemas</span><span class="sxs-lookup"><span data-stu-id="e9c46-121">Systems Engineer</span></span>|<span data-ttu-id="e9c46-122">Cabral EUA</span><span class="sxs-lookup"><span data-stu-id="e9c46-122">Contoso US</span></span>|<span data-ttu-id="e9c46-123">Hour</span><span class="sxs-lookup"><span data-stu-id="e9c46-123">Hour</span></span>| <span data-ttu-id="e9c46-124">100</span><span class="sxs-lookup"><span data-stu-id="e9c46-124">100</span></span>|<span data-ttu-id="e9c46-125">USD</span><span class="sxs-lookup"><span data-stu-id="e9c46-125">USD</span></span>|
| <span data-ttu-id="e9c46-126">Engenheiro de sistemas sênior</span><span class="sxs-lookup"><span data-stu-id="e9c46-126">Senior Systems Engineer</span></span>|<span data-ttu-id="e9c46-127">Cabral EUA</span><span class="sxs-lookup"><span data-stu-id="e9c46-127">Contoso US</span></span>|<span data-ttu-id="e9c46-128">Hour</span><span class="sxs-lookup"><span data-stu-id="e9c46-128">Hour</span></span>| <span data-ttu-id="e9c46-129">150</span><span class="sxs-lookup"><span data-stu-id="e9c46-129">150</span></span>| <span data-ttu-id="e9c46-130">USD</span><span class="sxs-lookup"><span data-stu-id="e9c46-130">USD</span></span>|


<span data-ttu-id="e9c46-131">Quando você desativa o **Título padrão** como a dimensão de precificação e o mecanismo de precificação do Project Service procura um preço, ele usa apenas o valor **Unidade Organizacional** no contexto de entrada.</span><span class="sxs-lookup"><span data-stu-id="e9c46-131">When you turn off **Standard Title** as the pricing dimension, and the Project Service pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="e9c46-132">Se a **Unidade Organizacional** do contexto de entrada for “Cabral US”, o resultado será não determinado porque as duas linhas corresponderão.</span><span class="sxs-lookup"><span data-stu-id="e9c46-132">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="e9c46-133">Para evitar esse cenário, ao criar registros **Preço da Função**, o Project Service valida que a combinação de dimensões é exclusiva.</span><span class="sxs-lookup"><span data-stu-id="e9c46-133">To avoid this scenario, when you create **Role Price** records, Project Service validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="e9c46-134">Se a dimensão for desativada após a criação dos registros **Preço da Função**, essa restrição poderá ser violada.</span><span class="sxs-lookup"><span data-stu-id="e9c46-134">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="e9c46-135">Portanto, é necessário que, antes de desativar uma dimensão, você exclua todas as linhas **Preço da Função** e **Markup de Preço da Função** que tenham esse valor de dimensão preenchido.</span><span class="sxs-lookup"><span data-stu-id="e9c46-135">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>

