---
title: Use APIs de programação para realizar operações com entidades de agendamento
description: Este tópico fornece informações e exemplos para usar APIs de programação.
author: sigitac
manager: Annbe
ms.date: 04/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a50a2c6220bb49de8146d0758019827e120e0526
ms.sourcegitcommit: 8ff9fe396db6dec581c21cd6bb9acc2691c815b0
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/07/2021
ms.locfileid: "5868115"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="9c3cd-103">Use APIs de programação para realizar operações com entidades de agendamento</span><span class="sxs-lookup"><span data-stu-id="9c3cd-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="9c3cd-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="9c3cd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="9c3cd-105">Parte de ou toda a funcionalidade observada neste tópico está disponível como parte de uma versão preliminar.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="9c3cd-106">O conteúdo e a funcionalidade estão sujeitos a alterações.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="9c3cd-107">Entidades de agendamento</span><span class="sxs-lookup"><span data-stu-id="9c3cd-107">Scheduling entities</span></span>

<span data-ttu-id="9c3cd-108">As APIs de programação fornecem a capacidade de executar operações de criação, atualização e exclusão com **Entidades de agendamento**.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="9c3cd-109">Essas entidades são gerenciadas por meio do mecanismo de agendamento no projeto para a Web.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="9c3cd-110">Criar, atualizar e excluir operações com **Entidades de agendamento** foram restritos em versões anteriores do Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="9c3cd-111">A tabela a seguir fornece uma lista completa das **Entidades de agendamento**.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="9c3cd-112">Nome da entidade</span><span class="sxs-lookup"><span data-stu-id="9c3cd-112">Entity name</span></span>  | <span data-ttu-id="9c3cd-113">Nome lógico da entidade</span><span class="sxs-lookup"><span data-stu-id="9c3cd-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="9c3cd-114">Project</span><span class="sxs-lookup"><span data-stu-id="9c3cd-114">Project</span></span> | <span data-ttu-id="9c3cd-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="9c3cd-115">msdyn_project</span></span> |
| <span data-ttu-id="9c3cd-116">Tarefa do Projeto</span><span class="sxs-lookup"><span data-stu-id="9c3cd-116">Project Task</span></span>  | <span data-ttu-id="9c3cd-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="9c3cd-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="9c3cd-118">Dependência de Tarefa do Projeto</span><span class="sxs-lookup"><span data-stu-id="9c3cd-118">Project Task Dependency</span></span>  | <span data-ttu-id="9c3cd-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="9c3cd-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="9c3cd-120">Atribuição de Recurso</span><span class="sxs-lookup"><span data-stu-id="9c3cd-120">Resource Assignment</span></span> | <span data-ttu-id="9c3cd-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="9c3cd-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="9c3cd-122">Bucket do Projeto</span><span class="sxs-lookup"><span data-stu-id="9c3cd-122">Project Bucket</span></span>  | <span data-ttu-id="9c3cd-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="9c3cd-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="9c3cd-124">Membro da Equipe do Projeto</span><span class="sxs-lookup"><span data-stu-id="9c3cd-124">Project Team Member</span></span> | <span data-ttu-id="9c3cd-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="9c3cd-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="9c3cd-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="9c3cd-126">OperationSet</span></span>

<span data-ttu-id="9c3cd-127">OperationSet é um padrão de unidade de trabalho que pode ser usado quando várias solicitações de impacto de agenda devem ser processadas em uma transação.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="9c3cd-128">APIs de programação</span><span class="sxs-lookup"><span data-stu-id="9c3cd-128">Schedule APIs</span></span>

<span data-ttu-id="9c3cd-129">A seguir está uma lista de APIs de programação atuais.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="9c3cd-130">**msdyn_CreateProjectV1**: Esta API pode ser usada para criar um projeto.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="9c3cd-131">O projeto e o bucket de projeto padrão são criados imediatamente.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="9c3cd-132">**msdyn_CreateTeamMemberV1**: Esta API pode ser usada para criar um membro da equipe do projeto.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="9c3cd-133">O registro do membro da equipe é criado imediatamente.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="9c3cd-134">**msdyn_CreateOperationSetV1**: Esta API pode ser usada para agendar várias solicitações que devem ser executadas em uma transação.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="9c3cd-135">**msdyn_PSSCreateV1**: Esta API pode ser usada para criar uma entidade.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="9c3cd-136">A entidade pode ser qualquer uma das entidades de agendamento que dão suporte à operação de criação.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="9c3cd-137">**msdyn_PSSUpdateV1**: Esta API pode ser usada para atualizar uma entidade.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="9c3cd-138">A entidade pode ser qualquer uma das entidades de agendamento que dão suporte à operação de atualização.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="9c3cd-139">**msdyn_PSSDeleteV1**: Esta API pode ser usada para excluir uma entidade.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="9c3cd-140">A entidade pode ser uma das entidades de agendamento com suporte à operação de exclusão.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="9c3cd-141">**msdyn_ExecuteOperationSetV1**: Esta API é usada para executar todas as operações no conjunto de operações especificado.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="9c3cd-142">Usar APIs de programação com OperationSet</span><span class="sxs-lookup"><span data-stu-id="9c3cd-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="9c3cd-143">Como registros com **CreateProjectV1** e **CreateTeamMemberV1** são criados imediatamente, essas APIs não podem ser usadas diretamente no **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="9c3cd-144">No entanto, você pode usar a API para criar os registros necessários, criar um **OperationSet** e usar esses registros pré-criados no **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="9c3cd-145">Operações com suporte</span><span class="sxs-lookup"><span data-stu-id="9c3cd-145">Supported operations</span></span>

| <span data-ttu-id="9c3cd-146">Entidade de agendamento</span><span class="sxs-lookup"><span data-stu-id="9c3cd-146">Scheduling entity</span></span> | <span data-ttu-id="9c3cd-147">Criar</span><span class="sxs-lookup"><span data-stu-id="9c3cd-147">Create</span></span> | <span data-ttu-id="9c3cd-148">Atualizar</span><span class="sxs-lookup"><span data-stu-id="9c3cd-148">Update</span></span> | <span data-ttu-id="9c3cd-149">Excluir</span><span class="sxs-lookup"><span data-stu-id="9c3cd-149">Delete</span></span> | <span data-ttu-id="9c3cd-150">Considerações importantes</span><span class="sxs-lookup"><span data-stu-id="9c3cd-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="9c3cd-151">Tarefa do projeto</span><span class="sxs-lookup"><span data-stu-id="9c3cd-151">Project task</span></span> | <span data-ttu-id="9c3cd-152">Sim</span><span class="sxs-lookup"><span data-stu-id="9c3cd-152">Yes</span></span> | <span data-ttu-id="9c3cd-153">Sim</span><span class="sxs-lookup"><span data-stu-id="9c3cd-153">Yes</span></span> | <span data-ttu-id="9c3cd-154">Sim</span><span class="sxs-lookup"><span data-stu-id="9c3cd-154">Yes</span></span> | <span data-ttu-id="9c3cd-155">Nenhum(a)</span><span class="sxs-lookup"><span data-stu-id="9c3cd-155">None</span></span> |
| <span data-ttu-id="9c3cd-156">Dependência de tarefa do projeto</span><span class="sxs-lookup"><span data-stu-id="9c3cd-156">Project task dependency</span></span> | <span data-ttu-id="9c3cd-157">Sim</span><span class="sxs-lookup"><span data-stu-id="9c3cd-157">Yes</span></span> | <span data-ttu-id="9c3cd-158">Sim</span><span class="sxs-lookup"><span data-stu-id="9c3cd-158">Yes</span></span> | | <span data-ttu-id="9c3cd-159">Os registros de dependência da tarefa do projeto não são atualizados.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="9c3cd-160">Em vez disso, um registro antigo pode ser excluído e um novo registro pode ser criado.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="9c3cd-161">Atribuição de recurso</span><span class="sxs-lookup"><span data-stu-id="9c3cd-161">Resource assignment</span></span> | <span data-ttu-id="9c3cd-162">Sim</span><span class="sxs-lookup"><span data-stu-id="9c3cd-162">Yes</span></span> | <span data-ttu-id="9c3cd-163">Sim</span><span class="sxs-lookup"><span data-stu-id="9c3cd-163">Yes</span></span> | | <span data-ttu-id="9c3cd-164">Não há suporte a operações com os seguintes campos: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** e **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="9c3cd-165">Os registros de atribuição de recursos não são atualizados.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="9c3cd-166">Em vez disso, o registro antigo pode ser excluído e um novo registro pode ser criado.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="9c3cd-167">Bucket do projeto</span><span class="sxs-lookup"><span data-stu-id="9c3cd-167">Project bucket</span></span> | <span data-ttu-id="9c3cd-168">N/D</span><span class="sxs-lookup"><span data-stu-id="9c3cd-168">N/A</span></span> | <span data-ttu-id="9c3cd-169">N/D</span><span class="sxs-lookup"><span data-stu-id="9c3cd-169">N/A</span></span> | <span data-ttu-id="9c3cd-170">N/D</span><span class="sxs-lookup"><span data-stu-id="9c3cd-170">N/A</span></span> | <span data-ttu-id="9c3cd-171">O intervalo padrão é criado usando a API **CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="9c3cd-172">Membro da equipe do projeto</span><span class="sxs-lookup"><span data-stu-id="9c3cd-172">Project team member</span></span> | <span data-ttu-id="9c3cd-173">Sim</span><span class="sxs-lookup"><span data-stu-id="9c3cd-173">Yes</span></span> | <span data-ttu-id="9c3cd-174">Sim</span><span class="sxs-lookup"><span data-stu-id="9c3cd-174">Yes</span></span> | <span data-ttu-id="9c3cd-175">Sim</span><span class="sxs-lookup"><span data-stu-id="9c3cd-175">Yes</span></span> | <span data-ttu-id="9c3cd-176">Para a operação de criação, use a API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="9c3cd-177">Project</span><span class="sxs-lookup"><span data-stu-id="9c3cd-177">Project</span></span> | <span data-ttu-id="9c3cd-178">Sim</span><span class="sxs-lookup"><span data-stu-id="9c3cd-178">Yes</span></span> | <span data-ttu-id="9c3cd-179">Sim</span><span class="sxs-lookup"><span data-stu-id="9c3cd-179">Yes</span></span> | <span data-ttu-id="9c3cd-180">N/D</span><span class="sxs-lookup"><span data-stu-id="9c3cd-180">N/A</span></span> | <span data-ttu-id="9c3cd-181">Não há suporte para operações com os seguintes campos: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** e **Duration**.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="9c3cd-182">Essas APIs podem ser chamadas com objetos de entidade que incluem campos personalizados.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="9c3cd-183">A propriedade da ID é opcional.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-183">The ID property is optional.</span></span> <span data-ttu-id="9c3cd-184">Se ela for fornecida, o sistema tentará usá-la e lançará uma exceção se ela não puder ser usada.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="9c3cd-185">Se ela não for fornecida, o sistema irá gerá-la.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-185">If it isn't provided, the system will generate it.</span></span>

## <a name="limitations-and-known-issues"></a><span data-ttu-id="9c3cd-186">Limitações e problemas conhecidos</span><span class="sxs-lookup"><span data-stu-id="9c3cd-186">Limitations and known issues</span></span>
<span data-ttu-id="9c3cd-187">Esta é uma lista de limitações e problemas conhecidos:</span><span class="sxs-lookup"><span data-stu-id="9c3cd-187">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="9c3cd-188">APIs de programação só podem ser usadas por **Usuários com licença do Microsoft Project**.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-188">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="9c3cd-189">Elas não podem ser usadas por:</span><span class="sxs-lookup"><span data-stu-id="9c3cd-189">They can't be used by:</span></span>
    - <span data-ttu-id="9c3cd-190">Usuários do aplicativo</span><span class="sxs-lookup"><span data-stu-id="9c3cd-190">Application users</span></span>
    - <span data-ttu-id="9c3cd-191">Usuários do sistema</span><span class="sxs-lookup"><span data-stu-id="9c3cd-191">System users</span></span>
    - <span data-ttu-id="9c3cd-192">Usuários de Integração</span><span class="sxs-lookup"><span data-stu-id="9c3cd-192">Integration users</span></span>
    - <span data-ttu-id="9c3cd-193">Outros usuários sem a licença necessária</span><span class="sxs-lookup"><span data-stu-id="9c3cd-193">Other users that don't have the required license</span></span>
- <span data-ttu-id="9c3cd-194">Cada **OperationSet** pode ter no máximo 100 operações.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-194">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="9c3cd-195">Cada usuário pode ter no máximo 10 **OperationSets** abertos.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-195">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="9c3cd-196">No momento, o Project Operations dá suporte no máximo a 500 tarefas em um projeto.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-196">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="9c3cd-197">O status de falha e logs de falha do **OperationSet** não estão disponíveis no momento.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-197">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- <span data-ttu-id="9c3cd-198">APIs de programação estão na versão preliminar pública.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-198">Schedule APIs are in Public preview.</span></span> <span data-ttu-id="9c3cd-199">O uso dessas APIs em um ambiente de produção não é compatível com a Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-199">Using these APIs in a Production environment isn't supported by Microsoft.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="9c3cd-200">Cenário de exemplo</span><span class="sxs-lookup"><span data-stu-id="9c3cd-200">Sample scenario</span></span>

<span data-ttu-id="9c3cd-201">Neste cenário, você criará um projeto, um membro da equipe, quatro tarefas e duas atribuições de recursos.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-201">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="9c3cd-202">Em seguida, você atualizará uma tarefa, atualizará o projeto, excluirá uma tarefa, excluirá uma atribuição de recurso e criará uma dependência de tarefa.</span><span class="sxs-lookup"><span data-stu-id="9c3cd-202">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

```C#
Entity project = CreateProject();
project.Id = CallCreateProjectAction(project);
var projectReference = project.ToEntityReference();

var teamMember = new Entity("msdyn_projectteam", Guid.NewGuid());
teamMember["msdyn_name"] = $"TM {DateTime.Now.ToShortTimeString()}";
teamMember["msdyn_project"] = projectReference;
var createTeamMemberResponse = CallCreateTeamMemberAction(teamMember);

var description = $"My demo {DateTime.Now.ToShortTimeString()}";
var operationSetId = CallCreateOperationSetAction(project.Id, description);

var task1 = GetTask("1WW", projectReference);
var task2 = GetTask("2XX", projectReference, task1.ToEntityReference());
var task3 = GetTask("3YY", projectReference);
var task4 = GetTask("4ZZ";, projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment"R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

varassignment1Response = CallPssCreateAction(assignment1, operationSetId);
varassignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

varassignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a><span data-ttu-id="9c3cd-203">Exemplos adicionais</span><span class="sxs-lookup"><span data-stu-id="9c3cd-203">Additional samples</span></span>

```C#
#region Call actions 

///<summary>
/// Calls the action to create an operationSet
/// </summary>
/// <paramname="projectId">project id for the operations to be included in this operationSet>/param>
/// <paramname="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
privatestring CallCreateOperationSetAction(Guid projectId, string description)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_CreateOperationSetV1");
    operationSetRequest["ProjectId"] = projectId.ToString();
    operationSetRequest["Description"] = description;
    OrganizationResponse response = organizationService.Execute(operationSetRequest);
    return response["OperationSetId"].ToString();
}

/// <summary>
/// Calls the action to create an entity, only Task and Resource Assignment for now
/// </summary>
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary<
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssUpdateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssUpdateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task and Resource Assignment for now
/// <summary>
/// <paramname="recordId">Id of the record to be deleted</param>
/// <paramname="entityLogicalName">Entity logical name of the record</param>
/// <paramname="operationSetId">OperationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssDeleteAction(string recordId, string entityLogicalName, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssDeleteV1");
    operationSetRequest["RecordId"] = recordId;
    operationSetRequest["EntityLogicalName"] = entityLogicalName;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to execute requests in an operationSet
/// <summary>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallExecuteOperationSetAction(string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_ExecuteOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// This can be used to abandon an operationSet that is no longer needed
/// </summary>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
protected OperationSetResponse CallAbandonOperationSetAction(Guid operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_AbandonOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId.ToString();
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to create a new project
/// </summary>
/// <paramname="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1";
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);

    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <paramname="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
privatestring CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject><OperationSetResponse>
    ((string)orgResponse.Results["OperationSetResponse";]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet(";msdyn_project", "msdyn_name");
    var getDefaultBucket = new QueryExpression("msdyn_projectbucket")
    {
        ColumnSet = columnsToFetch,
        Criteria =
        {
            Conditions =
            {
                new ConditionExpression("msdyn_project", ConditionOperator.Equal, projectReference.Id),
                new ConditionExpression("msdyn_name", ConditionOperator.Equal, "Bucket 1")
            }
        }
    };
    return organizationService.RetrieveMultiple(getDefaultBucket);
}

private Entity GetBucket(EntityReference projectReference)
{
    var bucketCollection = GetDefaultBucket(projectReference);
    if (bucketCollection.Entities.Count > 0)
    {
    return bucketCollection[0].ToEntity<Entity>();
    }

    throw new Exception($"Please open project with id {projectReference.Id} in the Dynamics UI and navigate to the Tasks tab");
}

private Entity CreateProject()
{
    var project = new Entity("msdyn_project", Guid.NewGuid());
    project["msdyn_subject"] = $"Proj {DateTime.Now.ToShortTimeString()}";
    return project;
}

private Entity GetTask(string name, EntityReference projectReference, EntityReference parentReference = null)
{
    var task = new Entity("msdyn_projecttask", Guid.NewGuid());
    task["msdyn_project"] = projectReference;
    task["msdyn_subject"] = name;
    task["msdyn_effort";] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
        task["new_custom1"] = "Just my test";
        task[";new_age"] = 98;
        task["new_amount"] = 591.34m;
        task["new_isready"] = new OptionSetValue(100000000);
    */

    if (parentReference == null)
    {
        task["msdyn_outlinelevel"] = 1;
    }
    else
    {
        task["msdyn_parenttask"] = parentReference;
    }
    return task;
}

private Entity GetResourceAssignment(string name, Entity teamMember, Entity task, Entity project)
{
    var assignment = new Entity("msdyn_resourceassignment", Guid.NewGuid());
    assignment["msdyn_projectteamid"] = teamMember.ToEntityReference();
    assignment["msdyn_taskid"] = task.ToEntityReference();
    assignment["msdyn_projectid"] = project.ToEntityReference();
    assignment["msdyn_name"] = name;
    assignment["msdyn_start"] = DateTime.Now;
    assignment["msdyn_finish"] = DateTime.Now;
    return assignment;
}

protected Entity GetTaskDependency(Entity project, Entity predecessor, Entity successor)
{
    var taskDependency = new Entity("msdyn_projecttaskdependency", Guid.NewGuid());
    taskDependency["msdyn_project"] = project.ToEntityReference();
    taskDependency["msdyn_predecessortask"] = predecessor.ToEntityReference();
    taskDependency["msdyn_successortask"] = successor.ToEntityReference();
    taskDependency["msdyn_linktype"] = new OptionSetValue(192350000);
    return taskDependency;
}

#endregion

#region OperationSetResponse DataContract --- Sample code ----

[DataContract]
publicclassOperationSetResponse
{
    [DataMember(Name = "operationSetId")]
    public Guid OperationSetId { get; set; }

    [DataMember(Name = "operationSetDetailId")]
    public Guid OperationSetDetailId { get; set; }

    [DataMember(Name = "operationType")]
    publicstring OperationType { get; set; }

    [DataMember(Name = "recordId")]
    publicstring RecordId { get; set; }

    [DataMember(Name = "correlationId")]
    publicstring CorrelationId { get; set; }
}

#endregion
```
