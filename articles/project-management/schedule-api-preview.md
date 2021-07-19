---
title: Use APIs de agendamento do Project para realizar operações com entidades de Agendamento
description: Este tópico fornece informações e exemplos para o uso de APIs de agendamento do Project.
author: sigitac
ms.date: 06/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4915261c08a3271a919e04084e92a14b297c1b35
ms.sourcegitcommit: 2f16c2bc7c8350676a6a380c61fffa9958db6a0b
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/22/2021
ms.locfileid: "6293213"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="2a3ff-103">Use APIs de agendamento do Project para realizar operações com entidades de Agendamento</span><span class="sxs-lookup"><span data-stu-id="2a3ff-103">Use Project schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="2a3ff-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="2a3ff-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="2a3ff-105">Parte de ou toda a funcionalidade observada neste tópico está disponível como parte de uma versão preliminar.</span><span class="sxs-lookup"><span data-stu-id="2a3ff-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="2a3ff-106">O conteúdo e a funcionalidade estão sujeitos a alterações.</span><span class="sxs-lookup"><span data-stu-id="2a3ff-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="2a3ff-107">Entidades de agendamento</span><span class="sxs-lookup"><span data-stu-id="2a3ff-107">Scheduling entities</span></span>

<span data-ttu-id="2a3ff-108">APIs de agendamento do Project fornecem a capacidade de executar operações de criação, atualização e exclusão com **Entidades de agendamento**.</span><span class="sxs-lookup"><span data-stu-id="2a3ff-108">Project schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="2a3ff-109">Essas entidades são gerenciadas por meio do mecanismo de agendamento no projeto para a Web.</span><span class="sxs-lookup"><span data-stu-id="2a3ff-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="2a3ff-110">Criar, atualizar e excluir operações com **Entidades de agendamento** foram restritos em versões anteriores do Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="2a3ff-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="2a3ff-111">A tabela a seguir fornece uma lista completa das entidades de agendamento do Project.</span><span class="sxs-lookup"><span data-stu-id="2a3ff-111">The following table provides a full list of the Project schedule entities.</span></span>

| <span data-ttu-id="2a3ff-112">Nome da entidade</span><span class="sxs-lookup"><span data-stu-id="2a3ff-112">Entity name</span></span>  | <span data-ttu-id="2a3ff-113">Nome lógico da entidade</span><span class="sxs-lookup"><span data-stu-id="2a3ff-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="2a3ff-114">Project</span><span class="sxs-lookup"><span data-stu-id="2a3ff-114">Project</span></span> | <span data-ttu-id="2a3ff-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="2a3ff-115">msdyn_project</span></span> |
| <span data-ttu-id="2a3ff-116">Tarefa do Projeto</span><span class="sxs-lookup"><span data-stu-id="2a3ff-116">Project Task</span></span>  | <span data-ttu-id="2a3ff-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="2a3ff-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="2a3ff-118">Dependência de Tarefa do Projeto</span><span class="sxs-lookup"><span data-stu-id="2a3ff-118">Project Task Dependency</span></span>  | <span data-ttu-id="2a3ff-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="2a3ff-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="2a3ff-120">Atribuição de Recurso</span><span class="sxs-lookup"><span data-stu-id="2a3ff-120">Resource Assignment</span></span> | <span data-ttu-id="2a3ff-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="2a3ff-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="2a3ff-122">Bucket do Projeto</span><span class="sxs-lookup"><span data-stu-id="2a3ff-122">Project Bucket</span></span>  | <span data-ttu-id="2a3ff-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="2a3ff-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="2a3ff-124">Membro da Equipe do Projeto</span><span class="sxs-lookup"><span data-stu-id="2a3ff-124">Project Team Member</span></span> | <span data-ttu-id="2a3ff-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="2a3ff-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="2a3ff-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="2a3ff-126">OperationSet</span></span>

<span data-ttu-id="2a3ff-127">OperationSet é um padrão de unidade de trabalho que pode ser usado quando várias solicitações de impacto de agenda devem ser processadas em uma transação.</span><span class="sxs-lookup"><span data-stu-id="2a3ff-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="project-schedule-apis"></a><span data-ttu-id="2a3ff-128">APIs de agendamento do Project</span><span class="sxs-lookup"><span data-stu-id="2a3ff-128">Project schedule APIs</span></span>

<span data-ttu-id="2a3ff-129">A seguir está uma lista de APIs atuais de agendamento do Project.</span><span class="sxs-lookup"><span data-stu-id="2a3ff-129">The following is a list of current Project schedule APIs.</span></span>

- <span data-ttu-id="2a3ff-130">**msdyn_CreateProjectV1**: Esta API pode ser usada para criar um projeto.</span><span class="sxs-lookup"><span data-stu-id="2a3ff-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="2a3ff-131">O projeto e o bucket de projeto padrão são criados imediatamente.</span><span class="sxs-lookup"><span data-stu-id="2a3ff-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="2a3ff-132">**msdyn_CreateTeamMemberV1**: Esta API pode ser usada para criar um membro da equipe do projeto.</span><span class="sxs-lookup"><span data-stu-id="2a3ff-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="2a3ff-133">O registro do membro da equipe é criado imediatamente.</span><span class="sxs-lookup"><span data-stu-id="2a3ff-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="2a3ff-134">**msdyn_CreateOperationSetV1**: Esta API pode ser usada para agendar várias solicitações que devem ser executadas em uma transação.</span><span class="sxs-lookup"><span data-stu-id="2a3ff-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="2a3ff-135">**msdyn_PSSCreateV1**: Esta API pode ser usada para criar uma entidade.</span><span class="sxs-lookup"><span data-stu-id="2a3ff-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="2a3ff-136">A entidade pode ser qualquer uma das entidades de agendamento do Project que oferecem suporte à operação de criação.</span><span class="sxs-lookup"><span data-stu-id="2a3ff-136">The entity can be any of the Project scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="2a3ff-137">**msdyn_PSSUpdateV1**: Esta API pode ser usada para atualizar uma entidade.</span><span class="sxs-lookup"><span data-stu-id="2a3ff-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="2a3ff-138">A entidade pode ser qualquer uma das entidades de agendamento do Project que oferecem suporte à operação de atualização.</span><span class="sxs-lookup"><span data-stu-id="2a3ff-138">The entity can be any of the Project scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="2a3ff-139">**msdyn_PSSDeleteV1**: Esta API pode ser usada para excluir uma entidade.</span><span class="sxs-lookup"><span data-stu-id="2a3ff-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="2a3ff-140">A entidade pode ser qualquer uma das entidades de agendamento do Project que oferecem suporte à operação de exclusão.</span><span class="sxs-lookup"><span data-stu-id="2a3ff-140">The entity can be any of the Project scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="2a3ff-141">**msdyn_ExecuteOperationSetV1**: Esta API é usada para executar todas as operações no conjunto de operações especificado.</span><span class="sxs-lookup"><span data-stu-id="2a3ff-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-project-schedule-apis-with-operationset"></a><span data-ttu-id="2a3ff-142">Usando APIs de agendamento do Project com OperationSet</span><span class="sxs-lookup"><span data-stu-id="2a3ff-142">Using Project schedule APIs with OperationSet</span></span>

<span data-ttu-id="2a3ff-143">Como registros com **CreateProjectV1** e **CreateTeamMemberV1** são criados imediatamente, essas APIs não podem ser usadas diretamente no **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="2a3ff-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="2a3ff-144">No entanto, você pode usar a API para criar os registros necessários, criar um **OperationSet** e usar esses registros pré-criados no **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="2a3ff-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="2a3ff-145">Operações com suporte</span><span class="sxs-lookup"><span data-stu-id="2a3ff-145">Supported operations</span></span>

| <span data-ttu-id="2a3ff-146">Entidade de agendamento</span><span class="sxs-lookup"><span data-stu-id="2a3ff-146">Scheduling entity</span></span> | <span data-ttu-id="2a3ff-147">Criar</span><span class="sxs-lookup"><span data-stu-id="2a3ff-147">Create</span></span> | <span data-ttu-id="2a3ff-148">Atualizar</span><span class="sxs-lookup"><span data-stu-id="2a3ff-148">Update</span></span> | <span data-ttu-id="2a3ff-149">Excluir</span><span class="sxs-lookup"><span data-stu-id="2a3ff-149">Delete</span></span> | <span data-ttu-id="2a3ff-150">Considerações importantes</span><span class="sxs-lookup"><span data-stu-id="2a3ff-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="2a3ff-151">Tarefa do projeto</span><span class="sxs-lookup"><span data-stu-id="2a3ff-151">Project task</span></span> | <span data-ttu-id="2a3ff-152">Sim</span><span class="sxs-lookup"><span data-stu-id="2a3ff-152">Yes</span></span> | <span data-ttu-id="2a3ff-153">Sim</span><span class="sxs-lookup"><span data-stu-id="2a3ff-153">Yes</span></span> | <span data-ttu-id="2a3ff-154">Sim</span><span class="sxs-lookup"><span data-stu-id="2a3ff-154">Yes</span></span> | <span data-ttu-id="2a3ff-155">Nenhum(a)</span><span class="sxs-lookup"><span data-stu-id="2a3ff-155">None</span></span> |
| <span data-ttu-id="2a3ff-156">Dependência de tarefa do projeto</span><span class="sxs-lookup"><span data-stu-id="2a3ff-156">Project task dependency</span></span> | <span data-ttu-id="2a3ff-157">Sim</span><span class="sxs-lookup"><span data-stu-id="2a3ff-157">Yes</span></span> | <span data-ttu-id="2a3ff-158">Sim</span><span class="sxs-lookup"><span data-stu-id="2a3ff-158">Yes</span></span> | | <span data-ttu-id="2a3ff-159">Os registros de dependência da tarefa do projeto não são atualizados.</span><span class="sxs-lookup"><span data-stu-id="2a3ff-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="2a3ff-160">Em vez disso, um registro antigo pode ser excluído e um novo registro pode ser criado.</span><span class="sxs-lookup"><span data-stu-id="2a3ff-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="2a3ff-161">Atribuição de recurso</span><span class="sxs-lookup"><span data-stu-id="2a3ff-161">Resource assignment</span></span> | <span data-ttu-id="2a3ff-162">Sim</span><span class="sxs-lookup"><span data-stu-id="2a3ff-162">Yes</span></span> | <span data-ttu-id="2a3ff-163">Sim</span><span class="sxs-lookup"><span data-stu-id="2a3ff-163">Yes</span></span> | | <span data-ttu-id="2a3ff-164">Não há suporte a operações com os seguintes campos: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** e **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="2a3ff-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="2a3ff-165">Os registros de atribuição de recursos não são atualizados.</span><span class="sxs-lookup"><span data-stu-id="2a3ff-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="2a3ff-166">Em vez disso, o registro antigo pode ser excluído e um novo registro pode ser criado.</span><span class="sxs-lookup"><span data-stu-id="2a3ff-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="2a3ff-167">Bucket do projeto</span><span class="sxs-lookup"><span data-stu-id="2a3ff-167">Project bucket</span></span> | <span data-ttu-id="2a3ff-168">N/D</span><span class="sxs-lookup"><span data-stu-id="2a3ff-168">N/A</span></span> | <span data-ttu-id="2a3ff-169">N/D</span><span class="sxs-lookup"><span data-stu-id="2a3ff-169">N/A</span></span> | <span data-ttu-id="2a3ff-170">N/D</span><span class="sxs-lookup"><span data-stu-id="2a3ff-170">N/A</span></span> | <span data-ttu-id="2a3ff-171">O intervalo padrão é criado usando a API **CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="2a3ff-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="2a3ff-172">Membro da equipe do projeto</span><span class="sxs-lookup"><span data-stu-id="2a3ff-172">Project team member</span></span> | <span data-ttu-id="2a3ff-173">Sim</span><span class="sxs-lookup"><span data-stu-id="2a3ff-173">Yes</span></span> | <span data-ttu-id="2a3ff-174">Sim</span><span class="sxs-lookup"><span data-stu-id="2a3ff-174">Yes</span></span> | <span data-ttu-id="2a3ff-175">Sim</span><span class="sxs-lookup"><span data-stu-id="2a3ff-175">Yes</span></span> | <span data-ttu-id="2a3ff-176">Para a operação de criação, use a API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="2a3ff-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="2a3ff-177">Project</span><span class="sxs-lookup"><span data-stu-id="2a3ff-177">Project</span></span> | <span data-ttu-id="2a3ff-178">Sim</span><span class="sxs-lookup"><span data-stu-id="2a3ff-178">Yes</span></span> | <span data-ttu-id="2a3ff-179">Sim</span><span class="sxs-lookup"><span data-stu-id="2a3ff-179">Yes</span></span> | <span data-ttu-id="2a3ff-180">N/D</span><span class="sxs-lookup"><span data-stu-id="2a3ff-180">N/A</span></span> | <span data-ttu-id="2a3ff-181">Não há suporte para operações com os seguintes campos: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** e **Duration**.</span><span class="sxs-lookup"><span data-stu-id="2a3ff-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="2a3ff-182">Essas APIs podem ser chamadas com objetos de entidade que incluem campos personalizados.</span><span class="sxs-lookup"><span data-stu-id="2a3ff-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="2a3ff-183">A propriedade da ID é opcional.</span><span class="sxs-lookup"><span data-stu-id="2a3ff-183">The ID property is optional.</span></span> <span data-ttu-id="2a3ff-184">Se ela for fornecida, o sistema tentará usá-la e lançará uma exceção se ela não puder ser usada.</span><span class="sxs-lookup"><span data-stu-id="2a3ff-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="2a3ff-185">Se ela não for fornecida, o sistema irá gerá-la.</span><span class="sxs-lookup"><span data-stu-id="2a3ff-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="2a3ff-186">Campos restritos</span><span class="sxs-lookup"><span data-stu-id="2a3ff-186">Restricted fields</span></span>

<span data-ttu-id="2a3ff-187">As tabelas a seguir definem os campos que são restritos de **Criar** e **Editar**.</span><span class="sxs-lookup"><span data-stu-id="2a3ff-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="2a3ff-188">Tarefa do projeto</span><span class="sxs-lookup"><span data-stu-id="2a3ff-188">Project task</span></span>

| <span data-ttu-id="2a3ff-189">**Nome lógico**</span><span class="sxs-lookup"><span data-stu-id="2a3ff-189">**Logical name**</span></span>                       | <span data-ttu-id="2a3ff-190">**Pode criar**</span><span class="sxs-lookup"><span data-stu-id="2a3ff-190">**Can create**</span></span> | <span data-ttu-id="2a3ff-191">**Pode editar**</span><span class="sxs-lookup"><span data-stu-id="2a3ff-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="2a3ff-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="2a3ff-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="2a3ff-193">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-193">no</span></span>             | <span data-ttu-id="2a3ff-194">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-194">no</span></span>               |
| <span data-ttu-id="2a3ff-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="2a3ff-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="2a3ff-196">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-196">no</span></span>             | <span data-ttu-id="2a3ff-197">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-197">no</span></span>               |
| <span data-ttu-id="2a3ff-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="2a3ff-198">msdyn_actualend</span></span>                        | <span data-ttu-id="2a3ff-199">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-199">no</span></span>             | <span data-ttu-id="2a3ff-200">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-200">no</span></span>               |
| <span data-ttu-id="2a3ff-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="2a3ff-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="2a3ff-202">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-202">no</span></span>             | <span data-ttu-id="2a3ff-203">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-203">no</span></span>               |
| <span data-ttu-id="2a3ff-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="2a3ff-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="2a3ff-205">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-205">no</span></span>             | <span data-ttu-id="2a3ff-206">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-206">no</span></span>               |
| <span data-ttu-id="2a3ff-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="2a3ff-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="2a3ff-208">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-208">no</span></span>             | <span data-ttu-id="2a3ff-209">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-209">no</span></span>               |
| <span data-ttu-id="2a3ff-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="2a3ff-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="2a3ff-211">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-211">no</span></span>             | <span data-ttu-id="2a3ff-212">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-212">no</span></span>               |
| <span data-ttu-id="2a3ff-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="2a3ff-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="2a3ff-214">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-214">no</span></span>             | <span data-ttu-id="2a3ff-215">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-215">no</span></span>               |
| <span data-ttu-id="2a3ff-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="2a3ff-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="2a3ff-217">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-217">no</span></span>             | <span data-ttu-id="2a3ff-218">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-218">no</span></span>               |
| <span data-ttu-id="2a3ff-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="2a3ff-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="2a3ff-220">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-220">no</span></span>             | <span data-ttu-id="2a3ff-221">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-221">no</span></span>               |
| <span data-ttu-id="2a3ff-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="2a3ff-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="2a3ff-223">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-223">no</span></span>             | <span data-ttu-id="2a3ff-224">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-224">no</span></span>               |
| <span data-ttu-id="2a3ff-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="2a3ff-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="2a3ff-226">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-226">no</span></span>             | <span data-ttu-id="2a3ff-227">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-227">no</span></span>               |
| <span data-ttu-id="2a3ff-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="2a3ff-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="2a3ff-229">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-229">no</span></span>             | <span data-ttu-id="2a3ff-230">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-230">no</span></span>               |
| <span data-ttu-id="2a3ff-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="2a3ff-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="2a3ff-232">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-232">no</span></span>             | <span data-ttu-id="2a3ff-233">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-233">no</span></span>               |
| <span data-ttu-id="2a3ff-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="2a3ff-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="2a3ff-235">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-235">no</span></span>             | <span data-ttu-id="2a3ff-236">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-236">no</span></span>               |
| <span data-ttu-id="2a3ff-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="2a3ff-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="2a3ff-238">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-238">no</span></span>             | <span data-ttu-id="2a3ff-239">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-239">no</span></span>               |
| <span data-ttu-id="2a3ff-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="2a3ff-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="2a3ff-241">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-241">no</span></span>             | <span data-ttu-id="2a3ff-242">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-242">no</span></span>               |
| <span data-ttu-id="2a3ff-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="2a3ff-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="2a3ff-244">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-244">no</span></span>             | <span data-ttu-id="2a3ff-245">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-245">no</span></span>               |
| <span data-ttu-id="2a3ff-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="2a3ff-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="2a3ff-247">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-247">no</span></span>             | <span data-ttu-id="2a3ff-248">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-248">no</span></span>               |
| <span data-ttu-id="2a3ff-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="2a3ff-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="2a3ff-250">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-250">no</span></span>             | <span data-ttu-id="2a3ff-251">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-251">no</span></span>               |
| <span data-ttu-id="2a3ff-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="2a3ff-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="2a3ff-253">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-253">no</span></span>             | <span data-ttu-id="2a3ff-254">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-254">no</span></span>               |
| <span data-ttu-id="2a3ff-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="2a3ff-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="2a3ff-256">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-256">no</span></span>             | <span data-ttu-id="2a3ff-257">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-257">no</span></span>               |
| <span data-ttu-id="2a3ff-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="2a3ff-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="2a3ff-259">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-259">no</span></span>             | <span data-ttu-id="2a3ff-260">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-260">no</span></span>               |
| <span data-ttu-id="2a3ff-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="2a3ff-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="2a3ff-262">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-262">no</span></span>             | <span data-ttu-id="2a3ff-263">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-263">no</span></span>               |
| <span data-ttu-id="2a3ff-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="2a3ff-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="2a3ff-265">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-265">no</span></span>             | <span data-ttu-id="2a3ff-266">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-266">no</span></span>               |
| <span data-ttu-id="2a3ff-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="2a3ff-267">msdyn_progress</span></span>                         | <span data-ttu-id="2a3ff-268">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-268">no</span></span>             | <span data-ttu-id="2a3ff-269">não (sim para P4W)</span><span class="sxs-lookup"><span data-stu-id="2a3ff-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="2a3ff-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="2a3ff-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="2a3ff-271">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-271">no</span></span>             | <span data-ttu-id="2a3ff-272">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-272">no</span></span>               |
| <span data-ttu-id="2a3ff-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="2a3ff-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="2a3ff-274">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-274">no</span></span>             | <span data-ttu-id="2a3ff-275">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-275">no</span></span>               |
| <span data-ttu-id="2a3ff-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="2a3ff-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="2a3ff-277">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-277">no</span></span>             | <span data-ttu-id="2a3ff-278">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-278">no</span></span>               |
| <span data-ttu-id="2a3ff-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="2a3ff-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="2a3ff-280">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-280">no</span></span>             | <span data-ttu-id="2a3ff-281">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-281">no</span></span>               |
| <span data-ttu-id="2a3ff-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="2a3ff-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="2a3ff-283">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-283">no</span></span>             | <span data-ttu-id="2a3ff-284">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-284">no</span></span>               |
| <span data-ttu-id="2a3ff-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="2a3ff-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="2a3ff-286">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-286">no</span></span>             | <span data-ttu-id="2a3ff-287">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-287">no</span></span>               |
| <span data-ttu-id="2a3ff-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="2a3ff-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="2a3ff-289">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-289">no</span></span>             | <span data-ttu-id="2a3ff-290">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-290">no</span></span>               |
| <span data-ttu-id="2a3ff-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="2a3ff-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="2a3ff-292">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-292">no</span></span>             | <span data-ttu-id="2a3ff-293">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-293">no</span></span>               |
| <span data-ttu-id="2a3ff-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="2a3ff-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="2a3ff-295">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-295">no</span></span>             | <span data-ttu-id="2a3ff-296">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-296">no</span></span>               |
| <span data-ttu-id="2a3ff-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="2a3ff-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="2a3ff-298">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-298">no</span></span>             | <span data-ttu-id="2a3ff-299">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-299">no</span></span>               |
| <span data-ttu-id="2a3ff-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="2a3ff-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="2a3ff-301">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-301">no</span></span>             | <span data-ttu-id="2a3ff-302">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-302">no</span></span>               |
| <span data-ttu-id="2a3ff-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="2a3ff-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="2a3ff-304">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-304">no</span></span>             | <span data-ttu-id="2a3ff-305">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-305">no</span></span>               |
| <span data-ttu-id="2a3ff-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="2a3ff-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="2a3ff-307">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-307">no</span></span>             | <span data-ttu-id="2a3ff-308">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-308">no</span></span>               |
| <span data-ttu-id="2a3ff-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="2a3ff-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="2a3ff-310">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-310">no</span></span>             | <span data-ttu-id="2a3ff-311">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-311">no</span></span>               |
| <span data-ttu-id="2a3ff-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="2a3ff-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="2a3ff-313">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-313">no</span></span>             | <span data-ttu-id="2a3ff-314">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-314">no</span></span>               |
| <span data-ttu-id="2a3ff-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="2a3ff-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="2a3ff-316">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-316">no</span></span>             | <span data-ttu-id="2a3ff-317">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-317">no</span></span>               |
| <span data-ttu-id="2a3ff-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="2a3ff-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="2a3ff-319">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-319">no</span></span>             | <span data-ttu-id="2a3ff-320">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-320">no</span></span>               |
| <span data-ttu-id="2a3ff-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="2a3ff-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="2a3ff-322">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-322">no</span></span>             | <span data-ttu-id="2a3ff-323">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-323">no</span></span>               |
| <span data-ttu-id="2a3ff-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="2a3ff-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="2a3ff-325">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-325">no</span></span>             | <span data-ttu-id="2a3ff-326">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-326">no</span></span>               |
| <span data-ttu-id="2a3ff-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="2a3ff-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="2a3ff-328">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-328">no</span></span>             | <span data-ttu-id="2a3ff-329">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-329">no</span></span>               |
| <span data-ttu-id="2a3ff-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="2a3ff-330">msdyn_summary</span></span>                          | <span data-ttu-id="2a3ff-331">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-331">no</span></span>             | <span data-ttu-id="2a3ff-332">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-332">no</span></span>               |
| <span data-ttu-id="2a3ff-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="2a3ff-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="2a3ff-334">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-334">no</span></span>             | <span data-ttu-id="2a3ff-335">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-335">no</span></span>               |
| <span data-ttu-id="2a3ff-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="2a3ff-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="2a3ff-337">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-337">no</span></span>             | <span data-ttu-id="2a3ff-338">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="2a3ff-339">Dependência de tarefa do projeto</span><span class="sxs-lookup"><span data-stu-id="2a3ff-339">Project task dependency</span></span>

| <span data-ttu-id="2a3ff-340">**Nome lógico**</span><span class="sxs-lookup"><span data-stu-id="2a3ff-340">**Logical name**</span></span>              | <span data-ttu-id="2a3ff-341">**Pode criar**</span><span class="sxs-lookup"><span data-stu-id="2a3ff-341">**Can create**</span></span> | <span data-ttu-id="2a3ff-342">**Pode editar**</span><span class="sxs-lookup"><span data-stu-id="2a3ff-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="2a3ff-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="2a3ff-343">msdyn_linktype</span></span>                | <span data-ttu-id="2a3ff-344">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-344">no</span></span>             | <span data-ttu-id="2a3ff-345">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-345">no</span></span>           |
| <span data-ttu-id="2a3ff-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="2a3ff-346">msdyn_linktypename</span></span>            | <span data-ttu-id="2a3ff-347">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-347">no</span></span>             | <span data-ttu-id="2a3ff-348">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-348">no</span></span>           |
| <span data-ttu-id="2a3ff-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="2a3ff-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="2a3ff-350">sim</span><span class="sxs-lookup"><span data-stu-id="2a3ff-350">yes</span></span>            | <span data-ttu-id="2a3ff-351">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-351">no</span></span>           |
| <span data-ttu-id="2a3ff-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="2a3ff-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="2a3ff-353">sim</span><span class="sxs-lookup"><span data-stu-id="2a3ff-353">yes</span></span>            | <span data-ttu-id="2a3ff-354">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-354">no</span></span>           |
| <span data-ttu-id="2a3ff-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="2a3ff-355">msdyn_project</span></span>                 | <span data-ttu-id="2a3ff-356">sim</span><span class="sxs-lookup"><span data-stu-id="2a3ff-356">yes</span></span>            | <span data-ttu-id="2a3ff-357">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-357">no</span></span>           |
| <span data-ttu-id="2a3ff-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="2a3ff-358">msdyn_projectname</span></span>             | <span data-ttu-id="2a3ff-359">sim</span><span class="sxs-lookup"><span data-stu-id="2a3ff-359">yes</span></span>            | <span data-ttu-id="2a3ff-360">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-360">no</span></span>           |
| <span data-ttu-id="2a3ff-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="2a3ff-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="2a3ff-362">sim</span><span class="sxs-lookup"><span data-stu-id="2a3ff-362">yes</span></span>            | <span data-ttu-id="2a3ff-363">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-363">no</span></span>           |
| <span data-ttu-id="2a3ff-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="2a3ff-364">msdyn_successortask</span></span>           | <span data-ttu-id="2a3ff-365">sim</span><span class="sxs-lookup"><span data-stu-id="2a3ff-365">yes</span></span>            | <span data-ttu-id="2a3ff-366">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-366">no</span></span>           |
| <span data-ttu-id="2a3ff-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="2a3ff-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="2a3ff-368">sim</span><span class="sxs-lookup"><span data-stu-id="2a3ff-368">yes</span></span>            | <span data-ttu-id="2a3ff-369">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="2a3ff-370">Atribuição de recurso</span><span class="sxs-lookup"><span data-stu-id="2a3ff-370">Resource assignment</span></span>

| <span data-ttu-id="2a3ff-371">**Nome lógico**</span><span class="sxs-lookup"><span data-stu-id="2a3ff-371">**Logical name**</span></span>             | <span data-ttu-id="2a3ff-372">**Pode criar**</span><span class="sxs-lookup"><span data-stu-id="2a3ff-372">**Can create**</span></span> | <span data-ttu-id="2a3ff-373">**Pode editar**</span><span class="sxs-lookup"><span data-stu-id="2a3ff-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="2a3ff-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="2a3ff-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="2a3ff-375">sim</span><span class="sxs-lookup"><span data-stu-id="2a3ff-375">yes</span></span>            | <span data-ttu-id="2a3ff-376">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-376">no</span></span>           |
| <span data-ttu-id="2a3ff-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="2a3ff-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="2a3ff-378">sim</span><span class="sxs-lookup"><span data-stu-id="2a3ff-378">yes</span></span>            | <span data-ttu-id="2a3ff-379">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-379">no</span></span>           |
| <span data-ttu-id="2a3ff-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="2a3ff-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="2a3ff-381">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-381">no</span></span>             | <span data-ttu-id="2a3ff-382">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-382">no</span></span>           |
| <span data-ttu-id="2a3ff-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="2a3ff-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="2a3ff-384">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-384">no</span></span>             | <span data-ttu-id="2a3ff-385">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-385">no</span></span>           |
| <span data-ttu-id="2a3ff-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="2a3ff-386">msdyn_committype</span></span>             | <span data-ttu-id="2a3ff-387">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-387">no</span></span>             | <span data-ttu-id="2a3ff-388">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-388">no</span></span>           |
| <span data-ttu-id="2a3ff-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="2a3ff-389">msdyn_committypename</span></span>         | <span data-ttu-id="2a3ff-390">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-390">no</span></span>             | <span data-ttu-id="2a3ff-391">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-391">no</span></span>           |
| <span data-ttu-id="2a3ff-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="2a3ff-392">msdyn_effort</span></span>                 | <span data-ttu-id="2a3ff-393">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-393">no</span></span>             | <span data-ttu-id="2a3ff-394">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-394">no</span></span>           |
| <span data-ttu-id="2a3ff-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="2a3ff-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="2a3ff-396">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-396">no</span></span>             | <span data-ttu-id="2a3ff-397">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-397">no</span></span>           |
| <span data-ttu-id="2a3ff-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="2a3ff-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="2a3ff-399">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-399">no</span></span>             | <span data-ttu-id="2a3ff-400">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-400">no</span></span>           |
| <span data-ttu-id="2a3ff-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="2a3ff-401">msdyn_finish</span></span>                 | <span data-ttu-id="2a3ff-402">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-402">no</span></span>             | <span data-ttu-id="2a3ff-403">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-403">no</span></span>           |
| <span data-ttu-id="2a3ff-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="2a3ff-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="2a3ff-405">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-405">no</span></span>             | <span data-ttu-id="2a3ff-406">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-406">no</span></span>           |
| <span data-ttu-id="2a3ff-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="2a3ff-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="2a3ff-408">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-408">no</span></span>             | <span data-ttu-id="2a3ff-409">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-409">no</span></span>           |
| <span data-ttu-id="2a3ff-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="2a3ff-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="2a3ff-411">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-411">no</span></span>             | <span data-ttu-id="2a3ff-412">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-412">no</span></span>           |
| <span data-ttu-id="2a3ff-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="2a3ff-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="2a3ff-414">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-414">no</span></span>             | <span data-ttu-id="2a3ff-415">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-415">no</span></span>           |
| <span data-ttu-id="2a3ff-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="2a3ff-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="2a3ff-417">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-417">no</span></span>             | <span data-ttu-id="2a3ff-418">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-418">no</span></span>           |
| <span data-ttu-id="2a3ff-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="2a3ff-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="2a3ff-420">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-420">no</span></span>             | <span data-ttu-id="2a3ff-421">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-421">no</span></span>           |
| <span data-ttu-id="2a3ff-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="2a3ff-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="2a3ff-423">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-423">no</span></span>             | <span data-ttu-id="2a3ff-424">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-424">no</span></span>           |
| <span data-ttu-id="2a3ff-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="2a3ff-425">msdyn_projectid</span></span>              | <span data-ttu-id="2a3ff-426">sim</span><span class="sxs-lookup"><span data-stu-id="2a3ff-426">yes</span></span>            | <span data-ttu-id="2a3ff-427">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-427">no</span></span>           |
| <span data-ttu-id="2a3ff-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="2a3ff-428">msdyn_projectidname</span></span>          | <span data-ttu-id="2a3ff-429">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-429">no</span></span>             | <span data-ttu-id="2a3ff-430">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-430">no</span></span>           |
| <span data-ttu-id="2a3ff-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="2a3ff-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="2a3ff-432">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-432">no</span></span>             | <span data-ttu-id="2a3ff-433">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-433">no</span></span>           |
| <span data-ttu-id="2a3ff-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="2a3ff-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="2a3ff-435">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-435">no</span></span>             | <span data-ttu-id="2a3ff-436">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-436">no</span></span>           |
| <span data-ttu-id="2a3ff-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="2a3ff-437">msdyn_start</span></span>                  | <span data-ttu-id="2a3ff-438">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-438">no</span></span>             | <span data-ttu-id="2a3ff-439">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-439">no</span></span>           |
| <span data-ttu-id="2a3ff-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="2a3ff-440">msdyn_taskid</span></span>                 | <span data-ttu-id="2a3ff-441">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-441">no</span></span>             | <span data-ttu-id="2a3ff-442">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-442">no</span></span>           |
| <span data-ttu-id="2a3ff-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="2a3ff-443">msdyn_taskidname</span></span>             | <span data-ttu-id="2a3ff-444">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-444">no</span></span>             | <span data-ttu-id="2a3ff-445">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-445">no</span></span>           |
| <span data-ttu-id="2a3ff-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="2a3ff-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="2a3ff-447">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-447">no</span></span>             | <span data-ttu-id="2a3ff-448">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="2a3ff-449">Membro da equipe do projeto</span><span class="sxs-lookup"><span data-stu-id="2a3ff-449">Project team member</span></span>

| <span data-ttu-id="2a3ff-450">**Nome lógico**</span><span class="sxs-lookup"><span data-stu-id="2a3ff-450">**Logical name**</span></span>                                 | <span data-ttu-id="2a3ff-451">**Pode criar**</span><span class="sxs-lookup"><span data-stu-id="2a3ff-451">**Can create**</span></span> | <span data-ttu-id="2a3ff-452">**Pode editar**</span><span class="sxs-lookup"><span data-stu-id="2a3ff-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="2a3ff-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="2a3ff-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="2a3ff-454">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-454">no</span></span>             | <span data-ttu-id="2a3ff-455">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-455">no</span></span>           |
| <span data-ttu-id="2a3ff-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="2a3ff-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="2a3ff-457">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-457">no</span></span>             | <span data-ttu-id="2a3ff-458">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-458">no</span></span>           |
| <span data-ttu-id="2a3ff-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="2a3ff-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="2a3ff-460">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-460">no</span></span>             | <span data-ttu-id="2a3ff-461">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-461">no</span></span>           |
| <span data-ttu-id="2a3ff-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="2a3ff-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="2a3ff-463">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-463">no</span></span>             | <span data-ttu-id="2a3ff-464">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-464">no</span></span>           |
| <span data-ttu-id="2a3ff-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="2a3ff-465">msdyn_effort</span></span>                                     | <span data-ttu-id="2a3ff-466">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-466">no</span></span>             | <span data-ttu-id="2a3ff-467">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-467">no</span></span>           |
| <span data-ttu-id="2a3ff-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="2a3ff-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="2a3ff-469">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-469">no</span></span>             | <span data-ttu-id="2a3ff-470">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-470">no</span></span>           |
| <span data-ttu-id="2a3ff-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="2a3ff-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="2a3ff-472">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-472">no</span></span>             | <span data-ttu-id="2a3ff-473">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-473">no</span></span>           |
| <span data-ttu-id="2a3ff-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="2a3ff-474">msdyn_finish</span></span>                                     | <span data-ttu-id="2a3ff-475">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-475">no</span></span>             | <span data-ttu-id="2a3ff-476">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-476">no</span></span>           |
| <span data-ttu-id="2a3ff-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="2a3ff-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="2a3ff-478">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-478">no</span></span>             | <span data-ttu-id="2a3ff-479">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-479">no</span></span>           |
| <span data-ttu-id="2a3ff-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="2a3ff-480">msdyn_hours</span></span>                                      | <span data-ttu-id="2a3ff-481">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-481">no</span></span>             | <span data-ttu-id="2a3ff-482">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-482">no</span></span>           |
| <span data-ttu-id="2a3ff-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="2a3ff-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="2a3ff-484">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-484">no</span></span>             | <span data-ttu-id="2a3ff-485">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-485">no</span></span>           |
| <span data-ttu-id="2a3ff-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="2a3ff-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="2a3ff-487">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-487">no</span></span>             | <span data-ttu-id="2a3ff-488">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-488">no</span></span>           |
| <span data-ttu-id="2a3ff-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="2a3ff-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="2a3ff-490">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-490">no</span></span>             | <span data-ttu-id="2a3ff-491">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-491">no</span></span>           |
| <span data-ttu-id="2a3ff-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="2a3ff-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="2a3ff-493">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-493">no</span></span>             | <span data-ttu-id="2a3ff-494">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-494">no</span></span>           |
| <span data-ttu-id="2a3ff-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="2a3ff-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="2a3ff-496">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-496">no</span></span>             | <span data-ttu-id="2a3ff-497">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-497">no</span></span>           |
| <span data-ttu-id="2a3ff-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="2a3ff-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="2a3ff-499">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-499">no</span></span>             | <span data-ttu-id="2a3ff-500">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-500">no</span></span>           |
| <span data-ttu-id="2a3ff-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="2a3ff-501">msdyn_start</span></span>                                      | <span data-ttu-id="2a3ff-502">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-502">no</span></span>             | <span data-ttu-id="2a3ff-503">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="2a3ff-504">Project</span><span class="sxs-lookup"><span data-stu-id="2a3ff-504">Project</span></span>

| <span data-ttu-id="2a3ff-505">**Nome lógico**</span><span class="sxs-lookup"><span data-stu-id="2a3ff-505">**Logical name**</span></span>                       | <span data-ttu-id="2a3ff-506">**Pode criar**</span><span class="sxs-lookup"><span data-stu-id="2a3ff-506">**Can create**</span></span> | <span data-ttu-id="2a3ff-507">**Pode editar**</span><span class="sxs-lookup"><span data-stu-id="2a3ff-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="2a3ff-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="2a3ff-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="2a3ff-509">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-509">no</span></span>             | <span data-ttu-id="2a3ff-510">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-510">no</span></span>           |
| <span data-ttu-id="2a3ff-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="2a3ff-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="2a3ff-512">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-512">no</span></span>             | <span data-ttu-id="2a3ff-513">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-513">no</span></span>           |
| <span data-ttu-id="2a3ff-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="2a3ff-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="2a3ff-515">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-515">no</span></span>             | <span data-ttu-id="2a3ff-516">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-516">no</span></span>           |
| <span data-ttu-id="2a3ff-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="2a3ff-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="2a3ff-518">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-518">no</span></span>             | <span data-ttu-id="2a3ff-519">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-519">no</span></span>           |
| <span data-ttu-id="2a3ff-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="2a3ff-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="2a3ff-521">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-521">no</span></span>             | <span data-ttu-id="2a3ff-522">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-522">no</span></span>           |
| <span data-ttu-id="2a3ff-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="2a3ff-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="2a3ff-524">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-524">no</span></span>             | <span data-ttu-id="2a3ff-525">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-525">no</span></span>           |
| <span data-ttu-id="2a3ff-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="2a3ff-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="2a3ff-527">sim</span><span class="sxs-lookup"><span data-stu-id="2a3ff-527">yes</span></span>            | <span data-ttu-id="2a3ff-528">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-528">no</span></span>           |
| <span data-ttu-id="2a3ff-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="2a3ff-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="2a3ff-530">sim</span><span class="sxs-lookup"><span data-stu-id="2a3ff-530">yes</span></span>            | <span data-ttu-id="2a3ff-531">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-531">no</span></span>           |
| <span data-ttu-id="2a3ff-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="2a3ff-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="2a3ff-533">sim</span><span class="sxs-lookup"><span data-stu-id="2a3ff-533">yes</span></span>            | <span data-ttu-id="2a3ff-534">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-534">no</span></span>           |
| <span data-ttu-id="2a3ff-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="2a3ff-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="2a3ff-536">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-536">no</span></span>             | <span data-ttu-id="2a3ff-537">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-537">no</span></span>           |
| <span data-ttu-id="2a3ff-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="2a3ff-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="2a3ff-539">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-539">no</span></span>             | <span data-ttu-id="2a3ff-540">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-540">no</span></span>           |
| <span data-ttu-id="2a3ff-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="2a3ff-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="2a3ff-542">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-542">no</span></span>             | <span data-ttu-id="2a3ff-543">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-543">no</span></span>           |
| <span data-ttu-id="2a3ff-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="2a3ff-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="2a3ff-545">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-545">no</span></span>             | <span data-ttu-id="2a3ff-546">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-546">no</span></span>           |
| <span data-ttu-id="2a3ff-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="2a3ff-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="2a3ff-548">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-548">no</span></span>             | <span data-ttu-id="2a3ff-549">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-549">no</span></span>           |
| <span data-ttu-id="2a3ff-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="2a3ff-550">msdyn_duration</span></span>                         | <span data-ttu-id="2a3ff-551">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-551">no</span></span>             | <span data-ttu-id="2a3ff-552">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-552">no</span></span>           |
| <span data-ttu-id="2a3ff-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="2a3ff-553">msdyn_effort</span></span>                           | <span data-ttu-id="2a3ff-554">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-554">no</span></span>             | <span data-ttu-id="2a3ff-555">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-555">no</span></span>           |
| <span data-ttu-id="2a3ff-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="2a3ff-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="2a3ff-557">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-557">no</span></span>             | <span data-ttu-id="2a3ff-558">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-558">no</span></span>           |
| <span data-ttu-id="2a3ff-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="2a3ff-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="2a3ff-560">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-560">no</span></span>             | <span data-ttu-id="2a3ff-561">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-561">no</span></span>           |
| <span data-ttu-id="2a3ff-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="2a3ff-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="2a3ff-563">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-563">no</span></span>             | <span data-ttu-id="2a3ff-564">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-564">no</span></span>           |
| <span data-ttu-id="2a3ff-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="2a3ff-565">msdyn_finish</span></span>                           | <span data-ttu-id="2a3ff-566">sim</span><span class="sxs-lookup"><span data-stu-id="2a3ff-566">yes</span></span>            | <span data-ttu-id="2a3ff-567">sim</span><span class="sxs-lookup"><span data-stu-id="2a3ff-567">yes</span></span>          |
| <span data-ttu-id="2a3ff-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="2a3ff-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="2a3ff-569">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-569">no</span></span>             | <span data-ttu-id="2a3ff-570">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-570">no</span></span>           |
| <span data-ttu-id="2a3ff-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="2a3ff-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="2a3ff-572">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-572">no</span></span>             | <span data-ttu-id="2a3ff-573">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-573">no</span></span>           |
| <span data-ttu-id="2a3ff-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="2a3ff-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="2a3ff-575">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-575">no</span></span>             | <span data-ttu-id="2a3ff-576">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-576">no</span></span>           |
| <span data-ttu-id="2a3ff-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="2a3ff-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="2a3ff-578">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-578">no</span></span>             | <span data-ttu-id="2a3ff-579">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-579">no</span></span>           |
| <span data-ttu-id="2a3ff-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="2a3ff-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="2a3ff-581">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-581">no</span></span>             | <span data-ttu-id="2a3ff-582">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-582">no</span></span>           |
| <span data-ttu-id="2a3ff-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="2a3ff-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="2a3ff-584">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-584">no</span></span>             | <span data-ttu-id="2a3ff-585">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-585">no</span></span>           |
| <span data-ttu-id="2a3ff-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="2a3ff-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="2a3ff-587">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-587">no</span></span>             | <span data-ttu-id="2a3ff-588">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-588">no</span></span>           |
| <span data-ttu-id="2a3ff-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="2a3ff-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="2a3ff-590">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-590">no</span></span>             | <span data-ttu-id="2a3ff-591">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-591">no</span></span>           |
| <span data-ttu-id="2a3ff-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="2a3ff-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="2a3ff-593">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-593">no</span></span>             | <span data-ttu-id="2a3ff-594">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-594">no</span></span>           |
| <span data-ttu-id="2a3ff-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="2a3ff-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="2a3ff-596">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-596">no</span></span>             | <span data-ttu-id="2a3ff-597">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-597">no</span></span>           |
| <span data-ttu-id="2a3ff-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="2a3ff-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="2a3ff-599">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-599">no</span></span>             | <span data-ttu-id="2a3ff-600">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-600">no</span></span>           |
| <span data-ttu-id="2a3ff-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="2a3ff-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="2a3ff-602">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-602">no</span></span>             | <span data-ttu-id="2a3ff-603">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-603">no</span></span>           |
| <span data-ttu-id="2a3ff-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="2a3ff-604">msdyn_progress</span></span>                         | <span data-ttu-id="2a3ff-605">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-605">no</span></span>             | <span data-ttu-id="2a3ff-606">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-606">no</span></span>           |
| <span data-ttu-id="2a3ff-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="2a3ff-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="2a3ff-608">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-608">no</span></span>             | <span data-ttu-id="2a3ff-609">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-609">no</span></span>           |
| <span data-ttu-id="2a3ff-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="2a3ff-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="2a3ff-611">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-611">no</span></span>             | <span data-ttu-id="2a3ff-612">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-612">no</span></span>           |
| <span data-ttu-id="2a3ff-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="2a3ff-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="2a3ff-614">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-614">no</span></span>             | <span data-ttu-id="2a3ff-615">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-615">no</span></span>           |
| <span data-ttu-id="2a3ff-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="2a3ff-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="2a3ff-617">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-617">no</span></span>             | <span data-ttu-id="2a3ff-618">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-618">no</span></span>           |
| <span data-ttu-id="2a3ff-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="2a3ff-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="2a3ff-620">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-620">no</span></span>             | <span data-ttu-id="2a3ff-621">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-621">no</span></span>           |
| <span data-ttu-id="2a3ff-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="2a3ff-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="2a3ff-623">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-623">no</span></span>             | <span data-ttu-id="2a3ff-624">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-624">no</span></span>           |
| <span data-ttu-id="2a3ff-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="2a3ff-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="2a3ff-626">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-626">no</span></span>             | <span data-ttu-id="2a3ff-627">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-627">no</span></span>           |
| <span data-ttu-id="2a3ff-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="2a3ff-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="2a3ff-629">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-629">no</span></span>             | <span data-ttu-id="2a3ff-630">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-630">no</span></span>           |
| <span data-ttu-id="2a3ff-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="2a3ff-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="2a3ff-632">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-632">no</span></span>             | <span data-ttu-id="2a3ff-633">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-633">no</span></span>           |
| <span data-ttu-id="2a3ff-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="2a3ff-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="2a3ff-635">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-635">no</span></span>             | <span data-ttu-id="2a3ff-636">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-636">no</span></span>           |
| <span data-ttu-id="2a3ff-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="2a3ff-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="2a3ff-638">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-638">no</span></span>             | <span data-ttu-id="2a3ff-639">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-639">no</span></span>           |
| <span data-ttu-id="2a3ff-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="2a3ff-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="2a3ff-641">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-641">no</span></span>             | <span data-ttu-id="2a3ff-642">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-642">no</span></span>           |
| <span data-ttu-id="2a3ff-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="2a3ff-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="2a3ff-644">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-644">no</span></span>             | <span data-ttu-id="2a3ff-645">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-645">no</span></span>           |
| <span data-ttu-id="2a3ff-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="2a3ff-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="2a3ff-647">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-647">no</span></span>             | <span data-ttu-id="2a3ff-648">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-648">no</span></span>           |
| <span data-ttu-id="2a3ff-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="2a3ff-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="2a3ff-650">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-650">no</span></span>             | <span data-ttu-id="2a3ff-651">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-651">no</span></span>           |
| <span data-ttu-id="2a3ff-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="2a3ff-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="2a3ff-653">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-653">no</span></span>             | <span data-ttu-id="2a3ff-654">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-654">no</span></span>           |
| <span data-ttu-id="2a3ff-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="2a3ff-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="2a3ff-656">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-656">no</span></span>             | <span data-ttu-id="2a3ff-657">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-657">no</span></span>           |
| <span data-ttu-id="2a3ff-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="2a3ff-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="2a3ff-659">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-659">no</span></span>             | <span data-ttu-id="2a3ff-660">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-660">no</span></span>           |
| <span data-ttu-id="2a3ff-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="2a3ff-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="2a3ff-662">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-662">no</span></span>             | <span data-ttu-id="2a3ff-663">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-663">no</span></span>           |
| <span data-ttu-id="2a3ff-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="2a3ff-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="2a3ff-665">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-665">no</span></span>             | <span data-ttu-id="2a3ff-666">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-666">no</span></span>           |
| <span data-ttu-id="2a3ff-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="2a3ff-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="2a3ff-668">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-668">no</span></span>             | <span data-ttu-id="2a3ff-669">não</span><span class="sxs-lookup"><span data-stu-id="2a3ff-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="2a3ff-670">Limitações e problemas conhecidos</span><span class="sxs-lookup"><span data-stu-id="2a3ff-670">Limitations and known issues</span></span>
<span data-ttu-id="2a3ff-671">Esta é uma lista de limitações e problemas conhecidos:</span><span class="sxs-lookup"><span data-stu-id="2a3ff-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="2a3ff-672">APIs de agendamento do Project só podem ser usadas por **Usuários com Licença do Microsoft Project.**</span><span class="sxs-lookup"><span data-stu-id="2a3ff-672">Project Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="2a3ff-673">Elas não podem ser usadas por:</span><span class="sxs-lookup"><span data-stu-id="2a3ff-673">They can't be used by:</span></span>
    - <span data-ttu-id="2a3ff-674">Usuários do aplicativo</span><span class="sxs-lookup"><span data-stu-id="2a3ff-674">Application users</span></span>
    - <span data-ttu-id="2a3ff-675">Usuários do sistema</span><span class="sxs-lookup"><span data-stu-id="2a3ff-675">System users</span></span>
    - <span data-ttu-id="2a3ff-676">Usuários de Integração</span><span class="sxs-lookup"><span data-stu-id="2a3ff-676">Integration users</span></span>
    - <span data-ttu-id="2a3ff-677">Outros usuários sem a licença necessária</span><span class="sxs-lookup"><span data-stu-id="2a3ff-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="2a3ff-678">Cada **OperationSet** pode ter no máximo 100 operações.</span><span class="sxs-lookup"><span data-stu-id="2a3ff-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="2a3ff-679">Cada usuário pode ter no máximo 10 **OperationSets** abertos.</span><span class="sxs-lookup"><span data-stu-id="2a3ff-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="2a3ff-680">No momento, o Project Operations dá suporte no máximo a 500 tarefas em um projeto.</span><span class="sxs-lookup"><span data-stu-id="2a3ff-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="2a3ff-681">O status de falha e logs de falha do **OperationSet** não estão disponíveis no momento.</span><span class="sxs-lookup"><span data-stu-id="2a3ff-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- [<span data-ttu-id="2a3ff-682">Limites em projetos e tarefas</span><span class="sxs-lookup"><span data-stu-id="2a3ff-682">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="2a3ff-683">Tratamento de erros</span><span class="sxs-lookup"><span data-stu-id="2a3ff-683">Error handling</span></span>

   - <span data-ttu-id="2a3ff-684">Para revisar erros gerados a partir dos Conjuntos de Operações, acesse **Configurações** \> **Integração de Agenda** \> **Conjuntos de Operações**.</span><span class="sxs-lookup"><span data-stu-id="2a3ff-684">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="2a3ff-685">Para revisar os erros gerados a partir do serviço de agendamento do Project, vá para **Definições** \> **Integração de agendamento** \> **Logs de Erros do PSS**.</span><span class="sxs-lookup"><span data-stu-id="2a3ff-685">To review errors generated from the Project schedule Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="2a3ff-686">Cenário de exemplo</span><span class="sxs-lookup"><span data-stu-id="2a3ff-686">Sample scenario</span></span>

<span data-ttu-id="2a3ff-687">Neste cenário, você criará um projeto, um membro da equipe, quatro tarefas e duas atribuições de recursos.</span><span class="sxs-lookup"><span data-stu-id="2a3ff-687">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="2a3ff-688">Em seguida, você atualizará uma tarefa, atualizará o projeto, excluirá uma tarefa, excluirá uma atribuição de recurso e criará uma dependência de tarefa.</span><span class="sxs-lookup"><span data-stu-id="2a3ff-688">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

```csharp
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
var task4 = GetTask("4ZZ", projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment("R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

var assignment1Response = CallPssCreateAction(assignment1, operationSetId);
var assignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

var assignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a><span data-ttu-id="2a3ff-689">Exemplos adicionais</span><span class="sxs-lookup"><span data-stu-id="2a3ff-689">Additional samples</span></span>

```csharp
#region Call actions --- Sample code ----

/// <summary>
/// Calls the action to create an operationSet
/// </summary>
/// <param name="projectId">project id for the operations to be included in this operationSet</param>
/// <param name="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
private string CallCreateOperationSetAction(Guid projectId, string description)
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
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>

private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet Id</param>
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
/// </summary>
/// <param name="recordId">Id of the record to be deleted</param>
/// <param name="entityLogicalName">Entity logical name of the record</param>
/// <param name="operationSetId">OperationSet Id</param>
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
/// </summary>
/// <param name="operationSetId">operationSet id</param>
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
/// <param name="operationSetId">operationSet id</param>
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
/// <param name="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1");
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);
    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <param name="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
private string CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject<OperationSetResponse>((string)orgResponse.Results["OperationSetResponse"]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet("msdyn_project", "msdyn_name");
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
    task["msdyn_effort"] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
    task["new_custom1"] = "Just my test";
    task["new_age"] = 98;
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
public class OperationSetResponse
{
[DataMember(Name = "operationSetId")]
public Guid OperationSetId { get; set; }

[DataMember(Name = "operationSetDetailId")]
public Guid OperationSetDetailId { get; set; }

[DataMember(Name = "operationType")]
public string OperationType { get; set; }

[DataMember(Name = "recordId")]
public string RecordId { get; set; }

[DataMember(Name = "correlationId")]
public string CorrelationId { get; set; }
}

#endregion
```
