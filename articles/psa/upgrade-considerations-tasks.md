---
title: Considerações sobre atualização para a estrutura de detalhamento de trabalho
description: Este tópico fornece informações sobre a atualização da estrutura de detalhamento de trabalho do Project Service Automation 2.x para 3.x.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
author: ruhercul
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
ms.openlocfilehash: a067521410f0fe0d8f5d4c510a35f2a3b018dce3
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281734"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a><span data-ttu-id="7c1fd-103">Considerações sobre atualização para a estrutura de detalhamento de trabalho</span><span class="sxs-lookup"><span data-stu-id="7c1fd-103">Upgrade considerations for the work breakdown structure</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="7c1fd-104">Este tópico fornece informações sobre a atualização da estrutura de detalhamento de trabalho do Project Service Automation 2.x para 3.x.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-104">This topic provides information about upgrading the work breakdown structure from Project Service Automation 2.x to 3.x.</span></span> <span data-ttu-id="7c1fd-105">Este tópico define o estado íntegro de um projeto no Project Service Automation (PSA) necessário para uma atualização bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-105">This topic defines the healthy state of a project in Project Service Automation (PSA) that is required for a successful upgrade.</span></span> <span data-ttu-id="7c1fd-106">Há também informações sobre as condições de bloqueio comuns que causarão falhas na atualização.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-106">There is also information about the common blocking conditions that will cause upgrade to fail.</span></span> <span data-ttu-id="7c1fd-107">Para obter mais informações sobre como definir tarefas do projeto e suas funções em uma agenda do projeto, consulte [Agendas de projeto](project-creating.md).</span><span class="sxs-lookup"><span data-stu-id="7c1fd-107">For more information about defining project tasks and their functions within a project schedule, see [Project schedules](project-creating.md).</span></span>

## <a name="key-entities"></a><span data-ttu-id="7c1fd-108">Entidades principais</span><span class="sxs-lookup"><span data-stu-id="7c1fd-108">Key entities</span></span>
<span data-ttu-id="7c1fd-109">Para uma estrutura de detalhamento de trabalho precisa que já esteja carregada com recursos, são necessárias as seguintes entidades:</span><span class="sxs-lookup"><span data-stu-id="7c1fd-109">For an accurate work breakdown structure that is already loaded with resources, the following entities are required:</span></span>

- [<span data-ttu-id="7c1fd-110">Projeto</span><span class="sxs-lookup"><span data-stu-id="7c1fd-110">Project</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [<span data-ttu-id="7c1fd-111">Equipe do Projeto</span><span class="sxs-lookup"><span data-stu-id="7c1fd-111">Project Team</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [<span data-ttu-id="7c1fd-112">Tarefa do Projeto</span><span class="sxs-lookup"><span data-stu-id="7c1fd-112">Project Task</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [<span data-ttu-id="7c1fd-113">Atribuições de Recursos</span><span class="sxs-lookup"><span data-stu-id="7c1fd-113">Resource Assignments</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [<span data-ttu-id="7c1fd-114">Dependência de Tarefa do Projeto</span><span class="sxs-lookup"><span data-stu-id="7c1fd-114">Project Task Dependency</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [<span data-ttu-id="7c1fd-115">Recursos Reserváveis</span><span class="sxs-lookup"><span data-stu-id="7c1fd-115">Bookable Resources</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

<span data-ttu-id="7c1fd-116">Para definir uma estrutura de detalhamento de trabalho carregada por recurso, você deve concluir as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="7c1fd-116">To define a resource loaded work breakdown structure, you must complete the following steps:</span></span>

1. <span data-ttu-id="7c1fd-117">Crie um projeto.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-117">Create a new project.</span></span> <span data-ttu-id="7c1fd-118">Para obter mais informações sobre como criar um projeto, consulte [msdyn_project](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).</span><span class="sxs-lookup"><span data-stu-id="7c1fd-118">For more information about how to create a new project, see [msdyn_project](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).</span></span>
2. <span data-ttu-id="7c1fd-119">Crie uma ou mais tarefas.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-119">Create one or more tasks.</span></span> <span data-ttu-id="7c1fd-120">Para obter mais informações sobre como criar uma tarefa, consulte [msdyn_projecttask](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).</span><span class="sxs-lookup"><span data-stu-id="7c1fd-120">For more information about how to create a task, see [msdyn_projecttask](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).</span></span>
3. <span data-ttu-id="7c1fd-121">Defina as dependências da tarefa.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-121">Define the task dependencies.</span></span> <span data-ttu-id="7c1fd-122">Para mais informações, consulte [Dependência da tarefa do projeto](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).</span><span class="sxs-lookup"><span data-stu-id="7c1fd-122">For more information, see [Project Task Dependency](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).</span></span>
4. <span data-ttu-id="7c1fd-123">Atribua membros da equipe do projeto para o projeto.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-123">Assign project team members to the project.</span></span> <span data-ttu-id="7c1fd-124">Para obter mais informações, consulte [msdyn_projectteam](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).</span><span class="sxs-lookup"><span data-stu-id="7c1fd-124">For more information, see [msdyn_projectteam](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).</span></span>
5. <span data-ttu-id="7c1fd-125">Atribua membros da equipe do projeto para as tarefas.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-125">Assign project team members to the tasks.</span></span> <span data-ttu-id="7c1fd-126">Para obter mais informações, consulte [msdyn_resourceassignment](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).</span><span class="sxs-lookup"><span data-stu-id="7c1fd-126">For more information, see [msdyn_resourceassignment](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).</span></span>

## <a name="project-team-relationships"></a><span data-ttu-id="7c1fd-127">Relações da equipe do projeto</span><span class="sxs-lookup"><span data-stu-id="7c1fd-127">Project team relationships</span></span>

<span data-ttu-id="7c1fd-128">Para garantir uma atualização bem-sucedida, os seguintes relacionamentos devem ser mantidos corretamente:</span><span class="sxs-lookup"><span data-stu-id="7c1fd-128">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>
- <span data-ttu-id="7c1fd-129">Todos os membros da equipe do projeto devem estar associados a um recurso que pode ser reservado.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-129">All project team members must be associated with a bookable resource.</span></span>
- <span data-ttu-id="7c1fd-130">Todos os membros da equipe do projeto devem estar associados ao mesmo projeto.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-130">All project team members must be associated with the same project.</span></span> 

## <a name="project-task-relationships"></a><span data-ttu-id="7c1fd-131">Relações de tarefas do projeto</span><span class="sxs-lookup"><span data-stu-id="7c1fd-131">Project task relationships</span></span>
<span data-ttu-id="7c1fd-132">Para garantir uma atualização bem-sucedida, os seguintes relacionamentos devem ser mantidos corretamente:</span><span class="sxs-lookup"><span data-stu-id="7c1fd-132">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="7c1fd-133">Todas as tarefas relacionadas devem ser associadas ao mesmo projeto.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-133">Any related tasks must be associated with the same project.</span></span>
- <span data-ttu-id="7c1fd-134">Toda tarefa de linha deve ter uma tarefa pai.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-134">Every line task must have a parent task.</span></span>
- <span data-ttu-id="7c1fd-135">Toda tarefa deve ter um projeto pai.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-135">Every task must have a parent project.</span></span>

### <a name="valid-conditions"></a><span data-ttu-id="7c1fd-136">Condições válidas</span><span class="sxs-lookup"><span data-stu-id="7c1fd-136">Valid conditions</span></span>

- <span data-ttu-id="7c1fd-137">Todas as durações de tarefa devem ser maiores ou iguais a (>=) uma hora e inferiores a 1.800.000 minutos (1.250 dias).\*</span><span class="sxs-lookup"><span data-stu-id="7c1fd-137">All task durations must be greater than or equal to (>=) one hour and less than 1,800,000 minutes (1,250 days).\*</span></span>
- <span data-ttu-id="7c1fd-138">Todas as tarefas devem ter uma data de início não anterior a 2000/01/01.\*</span><span class="sxs-lookup"><span data-stu-id="7c1fd-138">All tasks must have a start date no earlier than 2000/01/01.\*</span></span>
- <span data-ttu-id="7c1fd-139">Todas as tarefas devem ter uma data de início, de no máximo 17 anos a partir do dia atual.\*</span><span class="sxs-lookup"><span data-stu-id="7c1fd-139">All tasks must have a start date no later than 17 years from the present day.\*</span></span>
- <span data-ttu-id="7c1fd-140">Todas as tarefas devem ter uma data de início anterior ou igual à data de término.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-140">All tasks must have a start date earlier or equal to their finish date.</span></span>
- <span data-ttu-id="7c1fd-141">Todos os tipos de transação nas classificações (despesa, material, imposto e hora) devem ter valores para **Unidade Padrão** e **Grupo de Unidades**.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-141">All transaction types on classifications (Expense, Material, Tax, and Time) must have values for **Default Unit** and **Unit Group**.</span></span>
- <span data-ttu-id="7c1fd-142">Os formatos de data com letras devem ser evitados.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-142">Date formats with letters should be avoided.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="7c1fd-143">Etapas de mitigação potencial</span><span class="sxs-lookup"><span data-stu-id="7c1fd-143">Potential mitigation steps</span></span>
- <span data-ttu-id="7c1fd-144">Use a Localização Avançada para identificar tarefas do Projeto que não contêm uma ID do Projeto.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-144">Use Advanced Find to identify Project tasks that do not contain a Project ID.</span></span>
- <span data-ttu-id="7c1fd-145">Use a Localização Avançada para identificar tarefas do Projeto em que a duração agendada é maior que 1.800.000.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-145">Use Advanced Find to identify Project tasks where the scheduled duration is greater than > 1,800,000.</span></span>
- <span data-ttu-id="7c1fd-146">Antes de fazer alterações nos dados, você deve investigar personalizações associadas à entidade que possam ter levado os dados a um estado ruim.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-146">Prior to making any data changes, you should investigate any customizations associated with the entity that may have led to getting the data into a bad state.</span></span> <span data-ttu-id="7c1fd-147">Essas personalizações devem ser abordadas antes de prosseguir com as atualizações relacionadas a dados.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-147">These customizations should be addressed before proceeding with any data-related updates.</span></span>
- <span data-ttu-id="7c1fd-148">Para as tarefas identificadas que ficaram órfãs, considere excluí-las se não forem necessárias ou se devessem estar associadas ao projeto pai correto.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-148">For the identified tasks that have been orphaned, consider deleting these tasks if they are not needed or if they should be associated with the correct parent project.</span></span>
- <span data-ttu-id="7c1fd-149">Para tarefas cuja duração seja maior que 1.250 dias, considere adicionar várias tarefas para representar a duração total, se possível.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-149">For any tasks where the duration is greater than 1,250 days, consider adding multiple tasks to represent the total duration, if feasible.</span></span>

> [!NOTE]
> <span data-ttu-id="7c1fd-150">Os itens anotados com um asterisco (\*) têm limites porque o CRM oferece suporte a apenas a 7.320 expansões de recorrência.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-150">Items noted with an asterisk (\*) have limits that are due to the fact that customer relationship management (CRM) supports only 7,320 recurrence expansions.</span></span> <span data-ttu-id="7c1fd-151">Você deve permanecer abaixo desse limite.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-151">You must stay below this limit.</span></span>

## <a name="resource-assignment-relationships"></a><span data-ttu-id="7c1fd-152">Relações de atribuição de recursos</span><span class="sxs-lookup"><span data-stu-id="7c1fd-152">Resource Assignment relationships</span></span>
<span data-ttu-id="7c1fd-153">Para garantir uma atualização bem-sucedida, os seguintes relacionamentos devem ser mantidos corretamente:</span><span class="sxs-lookup"><span data-stu-id="7c1fd-153">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="7c1fd-154">Todas as atribuições de recursos em uma estrutura de detalhamento de trabalho devem estar relacionadas ao mesmo projeto.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-154">All Resource Assignments in a work breakdown structure must be related to the same project.</span></span>
- <span data-ttu-id="7c1fd-155">Todas as atribuições de recursos em uma estrutura de detalhamento de trabalho devem ser associadas aos membros da equipe do projeto no mesmo projeto.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-155">All Resource Assignments in a work breakdown structure must be associated to project team members in the same project.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="7c1fd-156">Etapas de mitigação potencial</span><span class="sxs-lookup"><span data-stu-id="7c1fd-156">Potential mitigation steps</span></span>
- <span data-ttu-id="7c1fd-157">Identifique todas as tarefas que estão fora das condições descritas acima.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-157">Identify all tasks that fall outside the conditions described above.</span></span>  
- <span data-ttu-id="7c1fd-158">As atribuições de recursos que não sejam mais válidas devem ser excluídas.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-158">Any Resource Assignments that are no longer valid should be deleted.</span></span>

## <a name="project-task-dependency-relationships"></a><span data-ttu-id="7c1fd-159">Relacionamentos de dependência de tarefas do projeto</span><span class="sxs-lookup"><span data-stu-id="7c1fd-159">Project task dependency relationships</span></span>
<span data-ttu-id="7c1fd-160">Para garantir uma atualização bem-sucedida, os seguintes relacionamentos devem ser mantidos corretamente:</span><span class="sxs-lookup"><span data-stu-id="7c1fd-160">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="7c1fd-161">Todas as dependências de tarefa do projeto devem estar relacionadas ao mesmo projeto.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-161">All project task dependencies must be related to the same project.</span></span>
- <span data-ttu-id="7c1fd-162">Uma tarefa não pode ter a mesma dependência referenciada mais de uma vez.</span><span class="sxs-lookup"><span data-stu-id="7c1fd-162">A task can't have the same dependency referenced more than once.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]