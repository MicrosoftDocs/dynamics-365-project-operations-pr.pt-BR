---
title: Andamento do projeto e consumo de custo
description: Este tópico fornece informações sobre como rastrear o progresso do projeto e o consumo de custos.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 08/21/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 0b69cee49e028b98bbb32e4a7e7aedf5479527dc
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147999"
---
# <a name="project-progress-and-cost-consumption"></a><span data-ttu-id="e66d0-103">Andamento do projeto e consumo de custo</span><span class="sxs-lookup"><span data-stu-id="e66d0-103">Project progress and cost consumption</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="e66d0-104">A necessidade de acompanhar o progresso em relação a uma agenda varia por setor.</span><span class="sxs-lookup"><span data-stu-id="e66d0-104">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="e66d0-105">Alguns setores fazem o acompanhamento em um nível granular, enquanto outros o fazem em um nível superior.</span><span class="sxs-lookup"><span data-stu-id="e66d0-105">Some industries track at a granular level, whereas other industries track at a higher level.</span></span> <span data-ttu-id="e66d0-106">Este tópico mostra como fazer agendamentos para atender aos requisitos da sua organização.</span><span class="sxs-lookup"><span data-stu-id="e66d0-106">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="e66d0-107">Exibição de Acompanhamento de Esforço</span><span class="sxs-lookup"><span data-stu-id="e66d0-107">Effort tracking view</span></span>

<span data-ttu-id="e66d0-108">A exibição **Acompanhamento de esforço** acompanha o progresso de tarefas na agenda.</span><span class="sxs-lookup"><span data-stu-id="e66d0-108">The **Effort tracking** view tracks the progress of tasks in the schedule.</span></span> <span data-ttu-id="e66d0-109">Compara as horas de esforço reais gastas em uma tarefa com as horas de esforço planejado da tarefa.</span><span class="sxs-lookup"><span data-stu-id="e66d0-109">It compares the actual effort hours spent on a task to the task's planned effort hours.</span></span> <span data-ttu-id="e66d0-110">O Project Service Automation usa as fórmulas a seguir para calcular as métricas de acompanhamento:</span><span class="sxs-lookup"><span data-stu-id="e66d0-110">Project Service Automation uses the following formulas to calculate the tracking metrics:</span></span>

<span data-ttu-id="e66d0-111">Inicialmente na criação da tarefa: o Custo planejado será definido como o Custo estimado na conclusão.</span><span class="sxs-lookup"><span data-stu-id="e66d0-111">Initially on the task creation: Planned cost will be set to the Estimated cost at complete.</span></span> <span data-ttu-id="e66d0-112">Assim que os Dados reais forem registrados na tarefa, o seguinte será calculado na exibição Rastreamento para Esforço</span><span class="sxs-lookup"><span data-stu-id="e66d0-112">Once Actuals are recorded on the task, the following will be calculation on the Tracking view for Effort</span></span>

- <span data-ttu-id="e66d0-113">Porcentagem de progresso = Esforço real até o momento ÷ Estimativa na conclusão (EAC)</span><span class="sxs-lookup"><span data-stu-id="e66d0-113">Progress percentage = Actual effort spent to date ÷ Estimate at complete (EAC)</span></span> 
- <span data-ttu-id="e66d0-114">Estimativa até a conclusão (ETC) = Estimativa na conclusão (EAC) - Esforço real empenhado até o momento</span><span class="sxs-lookup"><span data-stu-id="e66d0-114">Estimate to complete (ETC) = Estimate at complete (EAC)  – Actual effort spent to date</span></span> 
- <span data-ttu-id="e66d0-115">EAC = Esforço restante + Esforço real empenhado até o momento</span><span class="sxs-lookup"><span data-stu-id="e66d0-115">EAC = Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="e66d0-116">Variação de esforço projetada = Esforço planejado – EAT</span><span class="sxs-lookup"><span data-stu-id="e66d0-116">Projected effort variance = Planned effort – EAC</span></span>

<span data-ttu-id="e66d0-117">O Project Service Automation mostra uma projeção da variação de esforço na tarefa.</span><span class="sxs-lookup"><span data-stu-id="e66d0-117">Project Service Automation shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="e66d0-118">Se a EAT for maior do que o esforço planejado, a projeção é de que a tarefa levará mais tempo do que foi planejado originalmente.</span><span class="sxs-lookup"><span data-stu-id="e66d0-118">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned.</span></span> <span data-ttu-id="e66d0-119">Portanto, está atrasada.</span><span class="sxs-lookup"><span data-stu-id="e66d0-119">Therefore, it's behind schedule.</span></span> <span data-ttu-id="e66d0-120">Se a EAT for menor do que o esforço planejado, a projeção é de que a tarefa levará menos tempo do que foi planejado originalmente.</span><span class="sxs-lookup"><span data-stu-id="e66d0-120">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned.</span></span> <span data-ttu-id="e66d0-121">Portanto, está adiantada.</span><span class="sxs-lookup"><span data-stu-id="e66d0-121">Therefore, it's ahead of schedule.</span></span>

## <a name="reprojecting-effort"></a><span data-ttu-id="e66d0-122">Reprojetar esforço</span><span class="sxs-lookup"><span data-stu-id="e66d0-122">Reprojecting effort</span></span>

<span data-ttu-id="e66d0-123">É comum que um gerente de projetos revise as estimativas originais em uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="e66d0-123">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="e66d0-124">As reprojeções de projetos são a percepção de um gerente de projetos sobre as estimativas, considerando o estado atual de um projeto.</span><span class="sxs-lookup"><span data-stu-id="e66d0-124">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="e66d0-125">No entanto, não é recomendável que os gerentes de projetos alterem os números da linha de base, pois a linha de base do projeto representa a fonte de referência estabelecida para a estimativa de custo e de agenda dele e todos os participantes do projeto concordaram com ela.</span><span class="sxs-lookup"><span data-stu-id="e66d0-125">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="e66d0-126">Um gerente de projetos pode reprojetar o esforço em tarefas de duas maneiras:</span><span class="sxs-lookup"><span data-stu-id="e66d0-126">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="e66d0-127">Substituindo a ETC padrão por uma nova estimativa do esforço restante real na tarefa.</span><span class="sxs-lookup"><span data-stu-id="e66d0-127">Override the default ETC with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="e66d0-128">Substituindo a porcentagem de progresso padrão por uma nova estimativa do verdadeiro progresso na tarefa.</span><span class="sxs-lookup"><span data-stu-id="e66d0-128">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="e66d0-129">Cada uma dessas abordagens causa o recálculo de ETC, EAT, porcentagem de progresso e variação de esforço projetada em uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="e66d0-129">Each of these approaches cause a recalculation of the task's ETC, EAC, and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="e66d0-130">A EAT, a ETC e a porcentagem de progresso nas tarefas de resumo também são recalculadas e produzem uma nova projeção da variação de esforço.</span><span class="sxs-lookup"><span data-stu-id="e66d0-130">The EAC, ETC, and progress percentage on the summary tasks are also recalculated, and produce a new projection of effort variance.</span></span>

## <a name="reprojection-of-effort-on-summary-tasks"></a><span data-ttu-id="e66d0-131">Reprojeção de esforço em tarefas de resumo</span><span class="sxs-lookup"><span data-stu-id="e66d0-131">Reprojection of effort on summary tasks</span></span>

<span data-ttu-id="e66d0-132">O esforço em tarefas de resumo ou de contêiner pode ser reprojetado.</span><span class="sxs-lookup"><span data-stu-id="e66d0-132">Effort on summary tasks or container tasks can be reprojected.</span></span> <span data-ttu-id="e66d0-133">Independentemente do usuário reprojetar usando o esforço restante ou a porcentagem de progresso nas tarefas de resumo, o seguinte conjunto de cálculos é iniciado:</span><span class="sxs-lookup"><span data-stu-id="e66d0-133">Regardless of whether the user reprojects by using the remaining effort or the progress percentage on the summary tasks, the following set of calculations begins:</span></span>

- <span data-ttu-id="e66d0-134">A EAT, a ETC e a porcentagem de progresso na tarefa são calculadas.</span><span class="sxs-lookup"><span data-stu-id="e66d0-134">The EAC, ETC, and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="e66d0-135">A nova EAT é distribuída até as tarefas filho na mesma proporção em que a EAT original foi distribuída na tarefa.</span><span class="sxs-lookup"><span data-stu-id="e66d0-135">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="e66d0-136">A nova EAT em cada uma das tarefas individuais até as tarefas de nó folha é calculada.</span><span class="sxs-lookup"><span data-stu-id="e66d0-136">The new EAC on each of the individual tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="e66d0-137">As tarefas filho afetadas até os nós folha têm sua ETC e porcentagem de progresso recalculadas com base no valor da EAT.</span><span class="sxs-lookup"><span data-stu-id="e66d0-137">The affected child tasks down to the leaf nodes have their ETC and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="e66d0-138">Isso resulta em uma nova projeção da variação de esforço da tarefa.</span><span class="sxs-lookup"><span data-stu-id="e66d0-138">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="e66d0-139">As EATs das tarefas de resumo até o nó raiz são recalculadas.</span><span class="sxs-lookup"><span data-stu-id="e66d0-139">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>

### <a name="cost-tracking-view"></a><span data-ttu-id="e66d0-140">Exibição Acompanhamento de custo</span><span class="sxs-lookup"><span data-stu-id="e66d0-140">Cost tracking view</span></span> 

<span data-ttu-id="e66d0-141">A exibição **Rastreamento do custo** compara o custo real empenhado em uma tarefa com o custo planejado.</span><span class="sxs-lookup"><span data-stu-id="e66d0-141">The **Cost tracking** view compares the actual cost that was spent on a task to the planned cost.</span></span> 

> [!NOTE]
> <span data-ttu-id="e66d0-142">Essa exibição mostra apenas os custos de mão de obra e não inclui os custos das estimativas de despesas.</span><span class="sxs-lookup"><span data-stu-id="e66d0-142">This view shows only labor costs and doesn’t include costs from the expense estimates.</span></span> 

<span data-ttu-id="e66d0-143">O Project Service Automation usa as fórmulas a seguir para calcular as métricas de acompanhamento:</span><span class="sxs-lookup"><span data-stu-id="e66d0-143">Project Service Automation uses the following formulas to calculate the tracking metrics:</span></span>

<span data-ttu-id="e66d0-144">Quando uma tarefa é criada, o custo planejado é igual ao custo estimado na conclusão.</span><span class="sxs-lookup"><span data-stu-id="e66d0-144">When a task is created, the planned cost is equal to the estimated cost at complete.</span></span> <span data-ttu-id="e66d0-145">Após o registro de dados reais na tarefa, o seguinte será calculado na exibição **Rastreamento** para custo:</span><span class="sxs-lookup"><span data-stu-id="e66d0-145">After actuals are recorded on the task, the following is calculated on the **Tracking** view for cost:</span></span>

 - <span data-ttu-id="e66d0-146">Porcentagem de custo consumido = Custo real empenhado até o momento ÷ Custo estimado na conclusão para a tarefa</span><span class="sxs-lookup"><span data-stu-id="e66d0-146">Percentage of cost consumed = Actual cost spent to date ÷ Estimated cost at complete for the task</span></span>
 - <span data-ttu-id="e66d0-147">Custo até a conclusão (CTC) = Custo estimado na conclusão – Custo real empenhado até o momento</span><span class="sxs-lookup"><span data-stu-id="e66d0-147">Cost to complete (CTC) = Estimated cost at complete – Actual cost spent to date</span></span>
 - <span data-ttu-id="e66d0-148">Custo estimado na conclusão = CTC – Custo real empenhado até o momento</span><span class="sxs-lookup"><span data-stu-id="e66d0-148">Estimated cost at complete = CTC + Actual cost spent to date</span></span>
 - <span data-ttu-id="e66d0-149">Variação de custo projetado = Custo planejado - Custo estimado na conclusão</span><span class="sxs-lookup"><span data-stu-id="e66d0-149">Projected cost variance = Planned cost – Estimated cost at complete</span></span>

<span data-ttu-id="e66d0-150">Uma projeção da variação de custo é exibida na tarefa.</span><span class="sxs-lookup"><span data-stu-id="e66d0-150">A projection of the cost variance is shown on the task.</span></span> <span data-ttu-id="e66d0-151">Se o custo estimado na conclusão for maior do que o custo planejado, a tarefa será projetada para um custo superior ao que foi planejado originalmente.</span><span class="sxs-lookup"><span data-stu-id="e66d0-151">If the estimated cost at complete is more than the planned cost, the task is projected to cost more than was originally planned.</span></span> <span data-ttu-id="e66d0-152">Portanto, está acima do orçamento.</span><span class="sxs-lookup"><span data-stu-id="e66d0-152">Therefore, it's trending over budget.</span></span> <span data-ttu-id="e66d0-153">Se o Custo estimado na conclusão for menor do que o custo planejado, a tarefa será projetada para um custo inferior ao que foi planejado originalmente e tende a ficar abaixo do orçamento.</span><span class="sxs-lookup"><span data-stu-id="e66d0-153">If the Estimated cost at complete is less than the planned cost, the task is projected to cost less than was originally planned and is trending under budget.</span></span>

## <a name="project-managers-reprojection-of-cost"></a><span data-ttu-id="e66d0-154">Reprojeção de custo realizada pelo gerente do projeto</span><span class="sxs-lookup"><span data-stu-id="e66d0-154">Project manager’s reprojection of cost</span></span>

<span data-ttu-id="e66d0-155">Quando o esforço é reprojetado, o CTC, o Custo estimado na conclusão, a porcentagem de custo consumido e a variação de custo projetado são todos recalculados na exibição **Rastreamento do custo**.</span><span class="sxs-lookup"><span data-stu-id="e66d0-155">When effort is reprojected, the CTC, Estimated cost at complete, percentage of cost consumed, and projected cost variance are all recalculated in the **Cost tracking** view.</span></span>

## <a name="project-status-summary"></a><span data-ttu-id="e66d0-156">Resumo de status do projeto</span><span class="sxs-lookup"><span data-stu-id="e66d0-156">Project status summary</span></span>

<span data-ttu-id="e66d0-157">Os dados de acompanhamento nas exibições **Acompanhamento de esforço** e **Acompanhamento de custo** mostram o progresso e o consumo de custo nos níveis do nó raiz, das tarefas de resumo e das tarefas de nó folha.</span><span class="sxs-lookup"><span data-stu-id="e66d0-157">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="e66d0-158">A seção **Status** na página **Entidade de projeto** mostra um resumo do status no nível do projeto.</span><span class="sxs-lookup"><span data-stu-id="e66d0-158">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="e66d0-159">Campos do resumo do status</span><span class="sxs-lookup"><span data-stu-id="e66d0-159">Status summary fields</span></span>

<span data-ttu-id="e66d0-160">**Status geral do projeto** é um campo editável que mostra o status geral do projeto.</span><span class="sxs-lookup"><span data-stu-id="e66d0-160">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="e66d0-161">Ele usa um código de cores, como verde, amarelo e vermelho, para indicar o aumento do risco.</span><span class="sxs-lookup"><span data-stu-id="e66d0-161">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="e66d0-162">O campo **Comentários** permite ao gerente do projeto inserir comentários específicos sobre o status.</span><span class="sxs-lookup"><span data-stu-id="e66d0-162">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="e66d0-163">O campo **Status atualizado em** não é editável e o valor é um carimbo de data/hora que indica quando o status foi atualizado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="e66d0-163">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="e66d0-164">Os campos **Desempenho da agenda** e **Desempenho do custo** são definidos a partir da data de acompanhamento.</span><span class="sxs-lookup"><span data-stu-id="e66d0-164">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="e66d0-165">Quando a variação de agenda e de custo para o nó raiz na exibição **Acompanhamento de esforço** for positiva, você poderá definir esses campos como **Adiantado**.</span><span class="sxs-lookup"><span data-stu-id="e66d0-165">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="e66d0-166">Quando a variação de agenda e de custo para o nó raiz for negativa, você poderá defini-los como **Atrasado**.</span><span class="sxs-lookup"><span data-stu-id="e66d0-166">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>
