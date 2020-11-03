---
title: Alterações no Gerenciamento de recursos (Project Service Automation 3.x)
description: Este tópico fornece informações sobre as alterações na área de Gerenciamento de recursos.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 5176d2c6b7b00d47d4aeb12f54bdb84d4b87304c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4071619"
---
# <a name="resource-management-changes-project-service-automation-3x"></a><span data-ttu-id="97226-103">Alterações no Gerenciamento de recursos (Project Service Automation 3.x)</span><span class="sxs-lookup"><span data-stu-id="97226-103">Resource management changes (Project Service Automation 3.x)</span></span>

<span data-ttu-id="97226-104">As seções deste tópico fornecem informações sobre as alterações feitas na área de Gerenciamento de recursos do Dynamics 365 Project Service Automation versão 3.x.</span><span class="sxs-lookup"><span data-stu-id="97226-104">The sections of this topic provide information about the changes that have been made to the Resource management area of Dynamics 365 Project Service Automation version 3.x.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="97226-105">Estimativas de projeto</span><span class="sxs-lookup"><span data-stu-id="97226-105">Project estimates</span></span>

<span data-ttu-id="97226-106">Em vez de se basearem na entidade **msdyn\_projecttask** ( **Tarefa do Projeto** ), as estimativas de projeto se baseiam na entidade **msdyn\_resourceassignment** ( **Atribuição de Recurso** ).</span><span class="sxs-lookup"><span data-stu-id="97226-106">Instead of being based on the **msdyn\_projecttask** entity ( **Project Task** ), project estimates are based on the **msdyn\_resourceassignment** entity ( **Resource Assignment** ).</span></span> <span data-ttu-id="97226-107">As atribuições de recursos se tornaram a "fonte de referência" para preços e agendamento de tarefas.</span><span class="sxs-lookup"><span data-stu-id="97226-107">Resource assignments have become the "source of truth" for task scheduling and pricing.</span></span>

## <a name="line-tasks"></a><span data-ttu-id="97226-108">Tarefas de linha</span><span class="sxs-lookup"><span data-stu-id="97226-108">Line tasks</span></span>

<span data-ttu-id="97226-109">No PSA 3.x, as tarefas de linha são obsoletas (preteridas).</span><span class="sxs-lookup"><span data-stu-id="97226-109">In PSA 3.x, line tasks are obsolete (deprecated).</span></span> <span data-ttu-id="97226-110">As atribuições agora apontam para a tarefa inteira em vez das tarefas de linha.</span><span class="sxs-lookup"><span data-stu-id="97226-110">Assignments now point to the whole task instead of the line tasks.</span></span>

<span data-ttu-id="97226-111">O exemplo a seguir mostra como uma tarefa chamada "Tarefa de teste" é atribuída aos membros da equipe A e B em versões anteriores do PSA e no PSA 3.x.</span><span class="sxs-lookup"><span data-stu-id="97226-111">The following example shows how a task that is named "Test task" is assigned to team members A and B in earlier versions of PSA and in PSA 3.x.</span></span>

- <span data-ttu-id="97226-112">**Antes do PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="97226-112">**Before PSA 3.x:**</span></span>

    - <span data-ttu-id="97226-113">Tarefa de teste</span><span class="sxs-lookup"><span data-stu-id="97226-113">Test task</span></span>

        - <span data-ttu-id="97226-114">Tarefa de teste – Tarefa de linha 1</span><span class="sxs-lookup"><span data-stu-id="97226-114">Test task – Line task 1</span></span>

            - <span data-ttu-id="97226-115">Atribuição a A</span><span class="sxs-lookup"><span data-stu-id="97226-115">Assignment to A</span></span>

        - <span data-ttu-id="97226-116">Tarefa de teste – Tarefa de linha 2</span><span class="sxs-lookup"><span data-stu-id="97226-116">Test task – Line task 2</span></span>

            - <span data-ttu-id="97226-117">Atribuição a B</span><span class="sxs-lookup"><span data-stu-id="97226-117">Assignment to B</span></span>

- <span data-ttu-id="97226-118">**PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="97226-118">**PSA 3.x:**</span></span>

    - <span data-ttu-id="97226-119">Tarefa de teste</span><span class="sxs-lookup"><span data-stu-id="97226-119">Test task</span></span>

        - <span data-ttu-id="97226-120">Atribuição a A</span><span class="sxs-lookup"><span data-stu-id="97226-120">Assignment to A</span></span>
        - <span data-ttu-id="97226-121">Atribuição a B</span><span class="sxs-lookup"><span data-stu-id="97226-121">Assignment to B</span></span>

## <a name="unassigned-assignment"></a><span data-ttu-id="97226-122">Atribuição não atribuída</span><span class="sxs-lookup"><span data-stu-id="97226-122">Unassigned assignment</span></span>

<span data-ttu-id="97226-123">No PSA 3.x, uma atribuição não atribuída é aquela que é atribuída a um membro da equipe **NULO** e a um recurso **NULO**.</span><span class="sxs-lookup"><span data-stu-id="97226-123">In PSA 3.x, an unassigned assignment is an assignment that is assigned to a **NULL** team member and a **NULL** resource.</span></span> <span data-ttu-id="97226-124">As atribuições não atribuídas podem ocorrer em alguns cenários:</span><span class="sxs-lookup"><span data-stu-id="97226-124">Unassigned assignments can occur in a couple of scenarios:</span></span>

- <span data-ttu-id="97226-125">Se uma tarefa tiver sido criada, mas ainda não tiver sido atribuída a nenhum membro da equipe, uma atribuição não atribuída é sempre criada.</span><span class="sxs-lookup"><span data-stu-id="97226-125">If a task has been created, but it hasn't yet been assigned to any team member, an unassigned assignment is always created.</span></span> 
- <span data-ttu-id="97226-126">Se todos os destinatários em uma tarefa forem removidos, uma atribuição não atribuída é recriada para essa tarefa.</span><span class="sxs-lookup"><span data-stu-id="97226-126">If all assignees on a task are removed, an unassigned assignment is re-created for that task.</span></span>

## <a name="scheduling-fields-on-the-project-task-entity"></a><span data-ttu-id="97226-127">Campos de agendamento na entidade Tarefa do Projeto</span><span class="sxs-lookup"><span data-stu-id="97226-127">Scheduling fields on the Project Task entity</span></span>

<span data-ttu-id="97226-128">Os campos na entidade **msdyn\_projecttask** foram preteridos, movidos para a entidade **msdyn\_resourceassignment** ou agora são referenciados da entidade **msdyn\_projectteam** ( **Membro da Equipe do Projeto** ).</span><span class="sxs-lookup"><span data-stu-id="97226-128">The fields on the **msdyn\_projecttask** entity have been deprecated or moved to the **msdyn\_resourceassignment** entity, or they are now referenced from the **msdyn\_projectteam** entity ( **Project Team Member** ).</span></span>

| <span data-ttu-id="97226-129">Campo preterido em msdyn\_projecttask (Tarefa do Projeto)</span><span class="sxs-lookup"><span data-stu-id="97226-129">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="97226-130">Novo campo em msdyn\_resourceassignment (Atribuição de Recurso)</span><span class="sxs-lookup"><span data-stu-id="97226-130">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> | <span data-ttu-id="97226-131">Comentário</span><span class="sxs-lookup"><span data-stu-id="97226-131">Comment</span></span> |
|---|---|---|
| <span data-ttu-id="97226-132">msdyn\_assignedresources</span><span class="sxs-lookup"><span data-stu-id="97226-132">msdyn\_assignedresources</span></span> | <span data-ttu-id="97226-133">Nenhum(a)</span><span class="sxs-lookup"><span data-stu-id="97226-133">None</span></span> | |
| <span data-ttu-id="97226-134">msdyn\_assignedteammembers</span><span class="sxs-lookup"><span data-stu-id="97226-134">msdyn\_assignedteammembers</span></span> | <span data-ttu-id="97226-135">Nenhum(a)</span><span class="sxs-lookup"><span data-stu-id="97226-135">None</span></span> | |
| <span data-ttu-id="97226-136">msdyn\_numberofresources</span><span class="sxs-lookup"><span data-stu-id="97226-136">msdyn\_numberofresources</span></span> | <span data-ttu-id="97226-137">Nenhum(a)</span><span class="sxs-lookup"><span data-stu-id="97226-137">None</span></span> | |
| <span data-ttu-id="97226-138">msdyn\_scheduledhours</span><span class="sxs-lookup"><span data-stu-id="97226-138">msdyn\_scheduledhours</span></span> | <span data-ttu-id="97226-139">Nenhum(a)</span><span class="sxs-lookup"><span data-stu-id="97226-139">None</span></span> | |
| <span data-ttu-id="97226-140">msdyn\_effortcontour</span><span class="sxs-lookup"><span data-stu-id="97226-140">msdyn\_effortcontour</span></span> | <span data-ttu-id="97226-141">msdyn\_plannedwork</span><span class="sxs-lookup"><span data-stu-id="97226-141">msdyn\_plannedwork</span></span> | <span data-ttu-id="97226-142">O formato da estrutura de dados JavaScript Object Notation (JSON) que é armazenada no campo foi alterado.</span><span class="sxs-lookup"><span data-stu-id="97226-142">The format of the JavaScript Object Notation (JSON) data structure that is stored in the field has been changed.</span></span> |

## <a name="schedule-contour"></a><span data-ttu-id="97226-143">Contorno de agenda</span><span class="sxs-lookup"><span data-stu-id="97226-143">Schedule contour</span></span>

<span data-ttu-id="97226-144">O contorno de agenda é armazenado no campo **Trabalho Planejado** ( **msdyn\_plannedwork** ) de cada entidade **Atribuição de Recurso** ( **msdyn\_resourceassignment** ).</span><span class="sxs-lookup"><span data-stu-id="97226-144">The schedule contour is stored in the **Planned Work** field ( **msdyn\_plannedwork** ) of each **Resource Assignment** entity ( **msdyn\_resourceassignment** ).</span></span>

### <a name="structure"></a><span data-ttu-id="97226-145">Estrutura</span><span class="sxs-lookup"><span data-stu-id="97226-145">Structure</span></span>

<span data-ttu-id="97226-146">A nova estrutura do contorno de agenda consiste em intervalos de tempo flexíveis que são definidos para cada dia da agenda.</span><span class="sxs-lookup"><span data-stu-id="97226-146">The new structure of the schedule contour consists of flexible time slices that are defined for each day of the schedule.</span></span> <span data-ttu-id="97226-147">Cada intervalo de tempo tem as seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="97226-147">Each time slice has the following properties:</span></span>

- <span data-ttu-id="97226-148">**Início** – O início das horas de trabalho do dia, de acordo com o calendário do projeto.</span><span class="sxs-lookup"><span data-stu-id="97226-148">**Start** – The start of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="97226-149">**Término** – O término das horas de trabalho do dia, de acordo com o calendário do projeto.</span><span class="sxs-lookup"><span data-stu-id="97226-149">**End** – The end of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="97226-150">**Horas** – O número de horas atribuídas no dia.</span><span class="sxs-lookup"><span data-stu-id="97226-150">**Hours** – The number of hours that are assigned on the day.</span></span>

<span data-ttu-id="97226-151">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="97226-151">**Example**</span></span>

<span data-ttu-id="97226-152">Esse exemplo usa um calendário de projeto em que o dia de trabalho é das 9h às 17h no fuso horário UTC-8.</span><span class="sxs-lookup"><span data-stu-id="97226-152">This example uses a project calendar where the workday is from 9 AM to 5 PM in the UTC-8 time zone.</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a><span data-ttu-id="97226-153">Agendamento automático e manual</span><span class="sxs-lookup"><span data-stu-id="97226-153">Auto-scheduling and manual scheduling</span></span>

<span data-ttu-id="97226-154">Se uma tarefa é agendada de forma automática, as horas são decrescentes e a duração da tarefa pode ser reduzida.</span><span class="sxs-lookup"><span data-stu-id="97226-154">If a task is auto-scheduled, the hours are front-loaded, and the task duration might be reduced.</span></span>

<span data-ttu-id="97226-155">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="97226-155">**Example**</span></span>

<span data-ttu-id="97226-156">A tarefa a seguir foi agendada automaticamente para 18 horas ao longo de três dias (3 de dezembro de 2018 a 5 de dezembro de 2018).</span><span class="sxs-lookup"><span data-stu-id="97226-156">The following task is auto-scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

<span data-ttu-id="97226-157">Se uma tarefa é agendada de forma manual, as horas são igualmente distribuídas entre todas as datas.</span><span class="sxs-lookup"><span data-stu-id="97226-157">If a task is manually scheduled, the hours are evenly distributed to all the dates.</span></span>

<span data-ttu-id="97226-158">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="97226-158">**Example**</span></span>

<span data-ttu-id="97226-159">A tarefa a seguir foi agendada manualmente para 18 horas ao longo de três dias (3 de dezembro de 2018 a 5 de dezembro de 2018).</span><span class="sxs-lookup"><span data-stu-id="97226-159">The following task is manually scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a><span data-ttu-id="97226-160">Unidade de atribuição</span><span class="sxs-lookup"><span data-stu-id="97226-160">Assignment unit</span></span>

<span data-ttu-id="97226-161">A unidade de atribuição foi preterida no PSA 3.x.</span><span class="sxs-lookup"><span data-stu-id="97226-161">The assignment unit has been deprecated in PSA 3.x.</span></span> <span data-ttu-id="97226-162">As horas de esforço da tarefa agora são igualmente divididas, por dia, entre todos os recursos atribuídos.</span><span class="sxs-lookup"><span data-stu-id="97226-162">The task effort hours are now equally divided, per day, among all the assigned resources.</span></span>

<span data-ttu-id="97226-163">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="97226-163">**Example**</span></span>

<span data-ttu-id="97226-164">Nesse exemplo, a tarefa foi atribuída a dois recursos e agendada automaticamente para 36 horas ao longo de três dias (3 de dezembro de 2018 a 5 de dezembro de 2018).</span><span class="sxs-lookup"><span data-stu-id="97226-164">In this example, the task is is assigned to two resources and is auto-scheduled for 36 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

- <span data-ttu-id="97226-165">Atribuição 1:</span><span class="sxs-lookup"><span data-stu-id="97226-165">Assignment 1:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- <span data-ttu-id="97226-166">Atribuição 2:</span><span class="sxs-lookup"><span data-stu-id="97226-166">Assignment 2:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a><span data-ttu-id="97226-167">Dimensões de precificação</span><span class="sxs-lookup"><span data-stu-id="97226-167">Pricing dimensions</span></span>

<span data-ttu-id="97226-168">No PSA 3.x, campos de dimensões de precificação específicos aos recursos (como **Função** e **Unidade Organizacional** ) foram removidos da entidade **msdyn\_projecttask**.</span><span class="sxs-lookup"><span data-stu-id="97226-168">In PSA 3.x, resource-specific pricing dimension fields (such as **Role** and **Organizational Unit** ) have been removed from the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="97226-169">Esses campos agora podem ser recuperados do membro da equipe do projeto correspondente ( **msdyn\_projectteam** ) da atribuição de recursos ( **msdyn\_resourceassignment** ) quando as estimativas do projeto forem geradas.</span><span class="sxs-lookup"><span data-stu-id="97226-169">These fields can now be retrieved from the corresponding project team member ( **msdyn\_projectteam** ) of the resource assignment ( **msdyn\_resourceassignment** ) when project estimates are generated.</span></span> <span data-ttu-id="97226-170">Um novo campo, **msdyn\_organizationalunit** , foi adicionado à entidade **msdyn\_projectteam**.</span><span class="sxs-lookup"><span data-stu-id="97226-170">A new field, **msdyn\_organizationalunit** , has been added to the **msdyn\_projectteam** entity.</span></span>

| <span data-ttu-id="97226-171">Campo preterido em msdyn\_projecttask (Tarefa do Projeto)</span><span class="sxs-lookup"><span data-stu-id="97226-171">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="97226-172">Campo de msdyn\_projectteam (Membro da Equipe do Projeto) que é usado no lugar</span><span class="sxs-lookup"><span data-stu-id="97226-172">Field from msdyn\_projectteam (Project Team Member) that is used instead</span></span> |
|---|---|
| <span data-ttu-id="97226-173">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="97226-173">msdyn\_resourcecategory</span></span> | <span data-ttu-id="97226-174">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="97226-174">msdyn\_resourcecategory</span></span> |
| <span data-ttu-id="97226-175">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="97226-175">msdyn\_organizationalunit</span></span> | <span data-ttu-id="97226-176">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="97226-176">msdyn\_organizationalunit</span></span> |

## <a name="contours"></a><span data-ttu-id="97226-177">Contornos</span><span class="sxs-lookup"><span data-stu-id="97226-177">Contours</span></span>

<span data-ttu-id="97226-178">Os campos de contornos de estimativas e preços foram preteridos na entidade **msdyn\_projecttask**.</span><span class="sxs-lookup"><span data-stu-id="97226-178">The pricing and estimation contour fields have been deprecated on the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="97226-179">Eles foram movidos para a entidade **msdyn\_resourceassignment**.</span><span class="sxs-lookup"><span data-stu-id="97226-179">They have been moved to the **msdyn\_resourceassignment** entity.</span></span>

| <span data-ttu-id="97226-180">Campo preterido em msdyn\_projecttask (Tarefa do Projeto)</span><span class="sxs-lookup"><span data-stu-id="97226-180">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="97226-181">Novo campo em msdyn\_resourceassignment (Atribuição de Recurso)</span><span class="sxs-lookup"><span data-stu-id="97226-181">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> |
|---|---|
| <span data-ttu-id="97226-182">msdyn\_costestimatecontour</span><span class="sxs-lookup"><span data-stu-id="97226-182">msdyn\_costestimatecontour</span></span> | <span data-ttu-id="97226-183">msdyn\_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="97226-183">msdyn\_plannedcostcontour</span></span> |
| <span data-ttu-id="97226-184">msdyn\_salesestimatecontour</span><span class="sxs-lookup"><span data-stu-id="97226-184">msdyn\_salesestimatecontour</span></span> | <span data-ttu-id="97226-185">msdyn\_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="97226-185">msdyn\_plannedsalescontour</span></span> |

<span data-ttu-id="97226-186">Os campos a seguir foram adicionados à entidade **msdyn\_resourceassignment** :</span><span class="sxs-lookup"><span data-stu-id="97226-186">The following fields have been added to the **msdyn\_resourceassignment** entity:</span></span>

* <span data-ttu-id="97226-187">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="97226-187">msdyn\_plannedcost</span></span>
* <span data-ttu-id="97226-188">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="97226-188">msdyn\_plannedsales</span></span>

<span data-ttu-id="97226-189">Os campos a seguir de custo e vendas planejados, reais e restantes não foram alterados na entidade **msdyn\_projecttask** :</span><span class="sxs-lookup"><span data-stu-id="97226-189">The following fields for planned, actual, and remaining cost and sales are unchanged on the **msdyn\_projecttask** entity:</span></span>

* <span data-ttu-id="97226-190">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="97226-190">msdyn\_plannedcost</span></span>
* <span data-ttu-id="97226-191">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="97226-191">msdyn\_plannedsales</span></span>
* <span data-ttu-id="97226-192">msdyn\_actualcost</span><span class="sxs-lookup"><span data-stu-id="97226-192">msdyn\_actualcost</span></span>
* <span data-ttu-id="97226-193">msdyn\_actualsales</span><span class="sxs-lookup"><span data-stu-id="97226-193">msdyn\_actualsales</span></span>
* <span data-ttu-id="97226-194">msdyn\_remainingcost</span><span class="sxs-lookup"><span data-stu-id="97226-194">msdyn\_remainingcost</span></span>
* <span data-ttu-id="97226-195">msdyn\_remainingsales</span><span class="sxs-lookup"><span data-stu-id="97226-195">msdyn\_remainingsales</span></span>
