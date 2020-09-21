---
title: Consumo de custo e progresso do projeto
description: Este tópico fornece informações sobre como acompanhar o consumo de custo e o progresso do projeto.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 0d742164-5469-421d-8917-63160a81f651
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8aa5814938129f30885d8161a7c86197ab013364
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749133"
---
# <a name="project-progress-and-cost-consumption"></a><span data-ttu-id="31e32-103">Consumo de custo e progresso do projeto</span><span class="sxs-lookup"><span data-stu-id="31e32-103">Project progress and cost consumption</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="31e32-104">A necessidade de acompanhar o progresso em relação a uma agenda varia por setor.</span><span class="sxs-lookup"><span data-stu-id="31e32-104">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="31e32-105">Alguns setores fazem o acompanhamento em um nível granular, enquanto outros o fazem em um nível superior.</span><span class="sxs-lookup"><span data-stu-id="31e32-105">Some industries track at a granular level, whereas other industries track at a higher level.</span></span> <span data-ttu-id="31e32-106">Este tópico mostra como fazer agendamentos para atender aos requisitos da sua organização.</span><span class="sxs-lookup"><span data-stu-id="31e32-106">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="31e32-107">Exibição de Acompanhamento de Esforço</span><span class="sxs-lookup"><span data-stu-id="31e32-107">Effort tracking view</span></span>

<span data-ttu-id="31e32-108">A exibição **Acompanhamento de esforço** acompanha o progresso de tarefas na agenda.</span><span class="sxs-lookup"><span data-stu-id="31e32-108">The **Effort tracking** view tracks the progress of tasks in the schedule.</span></span> <span data-ttu-id="31e32-109">Ela compara as horas de esforço reais gastas em uma tarefa com as horas de esforço planejadas para essa tarefa.</span><span class="sxs-lookup"><span data-stu-id="31e32-109">It compares the actual effort hours that have been spent on a task to the planned effort hours for that task.</span></span> <span data-ttu-id="31e32-110">O PSA usa as fórmulas a seguir para calcular as métricas de acompanhamento:</span><span class="sxs-lookup"><span data-stu-id="31e32-110">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="31e32-111">Porcentagem de progresso = Esforço real empenhado até o momento ÷ Esforço planejado para a tarefa</span><span class="sxs-lookup"><span data-stu-id="31e32-111">Progress percentage = Actual effort spent to date ÷ Planned effort for the task</span></span> 
- <span data-ttu-id="31e32-112">Estimativa até a conclusão (ETC) = Esforço planejado – Esforço real empenhado até o momento</span><span class="sxs-lookup"><span data-stu-id="31e32-112">Estimate to complete (ETC) = Planned effort – Actual effort spent to date</span></span> 
- <span data-ttu-id="31e32-113">Estimativa ao término (EAT) = Esforço restante + Esforço real empenhado até o momento</span><span class="sxs-lookup"><span data-stu-id="31e32-113">Estimate at complete (EAC) = Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="31e32-114">Variação de esforço projetada = Esforço planejado – EAT</span><span class="sxs-lookup"><span data-stu-id="31e32-114">Projected effort variance = Planned effort – EAC</span></span>

<span data-ttu-id="31e32-115">O PSA mostra uma projeção da variação de esforço na tarefa.</span><span class="sxs-lookup"><span data-stu-id="31e32-115">PSA shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="31e32-116">Se a EAT for maior do que o esforço planejado, a projeção é de que a tarefa levará mais tempo do que foi planejado originalmente.</span><span class="sxs-lookup"><span data-stu-id="31e32-116">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned.</span></span> <span data-ttu-id="31e32-117">Portanto, está atrasada.</span><span class="sxs-lookup"><span data-stu-id="31e32-117">Therefore, it's behind schedule.</span></span> <span data-ttu-id="31e32-118">Se a EAT for menor do que o esforço planejado, a projeção é de que a tarefa levará menos tempo do que foi planejado originalmente.</span><span class="sxs-lookup"><span data-stu-id="31e32-118">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned.</span></span> <span data-ttu-id="31e32-119">Portanto, está adiantada.</span><span class="sxs-lookup"><span data-stu-id="31e32-119">Therefore, it's ahead of schedule.</span></span>

## <a name="re-projecting-effort"></a><span data-ttu-id="31e32-120">Reprojetar esforço</span><span class="sxs-lookup"><span data-stu-id="31e32-120">Re-projecting effort</span></span>

<span data-ttu-id="31e32-121">É comum que um gerente de projetos revise as estimativas originais em uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="31e32-121">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="31e32-122">As reprojeções de projetos são a percepção de um gerente de projetos sobre as estimativas, considerando o estado atual de um projeto.</span><span class="sxs-lookup"><span data-stu-id="31e32-122">Project re-projections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="31e32-123">No entanto, não é recomendável que os gerentes de projetos alterem os números da linha de base, pois a linha de base do projeto representa a fonte de referência estabelecida para a estimativa de custo e de agenda dele e todos os participantes do projeto concordaram com ela.</span><span class="sxs-lookup"><span data-stu-id="31e32-123">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="31e32-124">Um gerente de projetos pode reprojetar o esforço em tarefas de duas maneiras:</span><span class="sxs-lookup"><span data-stu-id="31e32-124">There are two ways that a project manager can re-project effort on tasks:</span></span>

- <span data-ttu-id="31e32-125">Substituindo a ETC padrão por uma nova estimativa do esforço restante real na tarefa.</span><span class="sxs-lookup"><span data-stu-id="31e32-125">Override the default ETC with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="31e32-126">Substituindo a porcentagem de progresso padrão por uma nova estimativa do verdadeiro progresso na tarefa.</span><span class="sxs-lookup"><span data-stu-id="31e32-126">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="31e32-127">Cada uma dessas abordagens causa o recálculo de ETC, EAT, porcentagem de progresso e variação de esforço projetada em uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="31e32-127">Each of these approaches cause a recalculation of the task's ETC, EAC, and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="31e32-128">A EAT, a ETC e a porcentagem de progresso nas tarefas de resumo também são recalculadas e produzem uma nova projeção da variação de esforço.</span><span class="sxs-lookup"><span data-stu-id="31e32-128">The EAC, ETC, and progress percentage on the summary tasks are also recalculated, and produce a new projection of effort variance.</span></span>

## <a name="re-projection-of-effort-on-summary-tasks"></a><span data-ttu-id="31e32-129">Reprojeção de esforço em tarefas de resumo</span><span class="sxs-lookup"><span data-stu-id="31e32-129">Re-projection of effort on summary tasks</span></span>

<span data-ttu-id="31e32-130">O esforço em tarefas de resumo ou de contêiner pode ser reprojetado.</span><span class="sxs-lookup"><span data-stu-id="31e32-130">Effort on summary tasks or container tasks can be re-projected.</span></span> <span data-ttu-id="31e32-131">Independentemente do usuário reprojetar usando o esforço restante ou a porcentagem de progresso nas tarefas de resumo, o seguinte conjunto de cálculos é iniciado:</span><span class="sxs-lookup"><span data-stu-id="31e32-131">Regardless of whether the user re-projects by using the remaining effort or the progress percentage on the summary tasks, the following set of calculations begins:</span></span>

- <span data-ttu-id="31e32-132">A EAT, a ETC e a porcentagem de progresso na tarefa são calculadas.</span><span class="sxs-lookup"><span data-stu-id="31e32-132">The EAC, ETC, and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="31e32-133">A nova EAT é distribuída até as tarefas filho na mesma proporção em que a EAT original foi distribuída na tarefa.</span><span class="sxs-lookup"><span data-stu-id="31e32-133">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="31e32-134">A nova EAT em cada uma das tarefas individuais até as tarefas de nó folha é calculada.</span><span class="sxs-lookup"><span data-stu-id="31e32-134">The new EAC on each of the individualt tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="31e32-135">As tarefas filho afetadas até os nós folha têm sua ETC e porcentagem de progresso recalculadas com base no valor da EAT.</span><span class="sxs-lookup"><span data-stu-id="31e32-135">The affected child tasks down to the leaf nodes have their ETC and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="31e32-136">Isso resulta em uma nova projeção da variação de esforço da tarefa.</span><span class="sxs-lookup"><span data-stu-id="31e32-136">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="31e32-137">As EATs das tarefas de resumo até o nó raiz são recalculadas.</span><span class="sxs-lookup"><span data-stu-id="31e32-137">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>

### <a name="cost-tracking-view"></a><span data-ttu-id="31e32-138">Exibição Acompanhamento de custo</span><span class="sxs-lookup"><span data-stu-id="31e32-138">Cost tracking view</span></span> 

<span data-ttu-id="31e32-139">A exibição **Acompanhamento de custo** compara o custo real empenhado em uma tarefa com o custo planejado para essa tarefa.</span><span class="sxs-lookup"><span data-stu-id="31e32-139">The **Cost tracking** view compares the actual cost that was spent on a task to the planned cost on a task.</span></span> 

> [!NOTE]
> <span data-ttu-id="31e32-140">Essa exibição mostra apenas os custos de mão de obra e não inclui os custos das estimativas de despesas.</span><span class="sxs-lookup"><span data-stu-id="31e32-140">This view shows only labor costs and doesn’t include costs from the expense estimates.</span></span> 

<span data-ttu-id="31e32-141">O PSA usa as fórmulas a seguir para calcular as métricas de acompanhamento:</span><span class="sxs-lookup"><span data-stu-id="31e32-141">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="31e32-142">Porcentagem de custo consumido = Custo real empenhado até o momento ÷ Custo planejado para a tarefa</span><span class="sxs-lookup"><span data-stu-id="31e32-142">Percentage of cost consumed = Actual cost spent to date ÷ Planned cost for the task</span></span>
- <span data-ttu-id="31e32-143">Custo até a conclusão (CTC) = Custo planejado – Custo real empenhado até o momento</span><span class="sxs-lookup"><span data-stu-id="31e32-143">Cost to complete (CTC) = Planned cost – Actual cost spent to date</span></span>
- <span data-ttu-id="31e32-144">EAT = CTC + Custo real empenhado até o momento</span><span class="sxs-lookup"><span data-stu-id="31e32-144">EAC = CTC + Actual cost spent to date</span></span>
- <span data-ttu-id="31e32-145">Variação de custo projetada = Custo planejado – EAT</span><span class="sxs-lookup"><span data-stu-id="31e32-145">Projected cost variance = Planned cost – EAC</span></span>

<span data-ttu-id="31e32-146">Uma projeção da variação de custo é exibida na tarefa.</span><span class="sxs-lookup"><span data-stu-id="31e32-146">A projection of the cost variance is shown on the task.</span></span> <span data-ttu-id="31e32-147">Se a EAT for maior do que o custo planejado, a projeção é de que a tarefa custe mais do que foi planejado originalmente.</span><span class="sxs-lookup"><span data-stu-id="31e32-147">If the EAC is more than the planned cost, the task is projected to cost more than was originally planned.</span></span> <span data-ttu-id="31e32-148">Portanto, está acima do orçamento.</span><span class="sxs-lookup"><span data-stu-id="31e32-148">Therefore, it's trending over budget.</span></span> <span data-ttu-id="31e32-149">Se a EAT for menor do que o custo planejado, a projeção é de que a tarefa custe menos do que foi planejado originalmente.</span><span class="sxs-lookup"><span data-stu-id="31e32-149">If the EAC is less than the planned cost, the task is projected to cost less than was originally planned.</span></span> <span data-ttu-id="31e32-150">Portanto, está abaixo do orçamento.</span><span class="sxs-lookup"><span data-stu-id="31e32-150">Therefore, it's trending under budget.</span></span>

## <a name="project-managers-re-projection-of-cost"></a><span data-ttu-id="31e32-151">Reprojeção de custo realizada pelo gerente do projeto</span><span class="sxs-lookup"><span data-stu-id="31e32-151">Project manager’s re-projection of cost</span></span>

<span data-ttu-id="31e32-152">Quando o esforço é reprojetado, CTC, EAT, porcentagem de custo consumido e variação de custo projetada são todos recalculados na exibição **Acompanhamento de custo**.</span><span class="sxs-lookup"><span data-stu-id="31e32-152">When effort is re-projected, the CTC, EAC, percentage of cost consumed, and projected cost variance are all recalculated in the **Cost tracking** view.</span></span>

## <a name="project-status-summary"></a><span data-ttu-id="31e32-153">Resumo de status do projeto</span><span class="sxs-lookup"><span data-stu-id="31e32-153">Project status summary</span></span>

<span data-ttu-id="31e32-154">Os dados de acompanhamento nas exibições **Acompanhamento de esforço** e **Acompanhamento de custo** mostram o progresso e o consumo de custo nos níveis do nó raiz, das tarefas de resumo e das tarefas de nó folha.</span><span class="sxs-lookup"><span data-stu-id="31e32-154">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="31e32-155">A seção **Status** na página **Entidade de projeto** mostra um resumo do status no nível do projeto.</span><span class="sxs-lookup"><span data-stu-id="31e32-155">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="31e32-156">Campos do resumo do status</span><span class="sxs-lookup"><span data-stu-id="31e32-156">Status summary fields</span></span>

<span data-ttu-id="31e32-157">**Status geral do projeto** é um campo editável que mostra o status geral do projeto.</span><span class="sxs-lookup"><span data-stu-id="31e32-157">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="31e32-158">Ele usa um código de cores, como verde, amarelo e vermelho, para indicar o aumento do risco.</span><span class="sxs-lookup"><span data-stu-id="31e32-158">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="31e32-159">O campo **Comentários** permite ao gerente do projeto inserir comentários específicos sobre o status.</span><span class="sxs-lookup"><span data-stu-id="31e32-159">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="31e32-160">O campo **Status atualizado em** não é editável e o valor é um carimbo de data/hora que indica quando o status foi atualizado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="31e32-160">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="31e32-161">Os campos **Desempenho da agenda** e **Desempenho do custo** são definidos a partir da data de acompanhamento.</span><span class="sxs-lookup"><span data-stu-id="31e32-161">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="31e32-162">Quando a variação de agenda e de custo para o nó raiz na exibição **Acompanhamento de esforço** for positiva, você poderá definir esses campos como **Adiantado**.</span><span class="sxs-lookup"><span data-stu-id="31e32-162">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="31e32-163">Quando a variação de agenda e de custo para o nó raiz for negativa, você poderá defini-los como **Atrasado**.</span><span class="sxs-lookup"><span data-stu-id="31e32-163">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>
