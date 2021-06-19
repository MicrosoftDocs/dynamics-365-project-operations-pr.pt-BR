---
title: Use APIs de programação para realizar operações com entidades de agendamento
description: Este tópico fornece informações e exemplos para usar APIs de programação.
author: sigitac
ms.date: 04/27/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4a032dc7bcbdf23fce3c3b2ca63c51d473bd8e26
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116783"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="1734f-103">Use APIs de programação para realizar operações com entidades de agendamento</span><span class="sxs-lookup"><span data-stu-id="1734f-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="1734f-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="1734f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="1734f-105">Parte de ou toda a funcionalidade observada neste tópico está disponível como parte de uma versão preliminar.</span><span class="sxs-lookup"><span data-stu-id="1734f-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="1734f-106">O conteúdo e a funcionalidade estão sujeitos a alterações.</span><span class="sxs-lookup"><span data-stu-id="1734f-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="1734f-107">Entidades de agendamento</span><span class="sxs-lookup"><span data-stu-id="1734f-107">Scheduling entities</span></span>

<span data-ttu-id="1734f-108">As APIs de programação fornecem a capacidade de executar operações de criação, atualização e exclusão com **Entidades de agendamento**.</span><span class="sxs-lookup"><span data-stu-id="1734f-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="1734f-109">Essas entidades são gerenciadas por meio do mecanismo de agendamento no projeto para a Web.</span><span class="sxs-lookup"><span data-stu-id="1734f-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="1734f-110">Criar, atualizar e excluir operações com **Entidades de agendamento** foram restritos em versões anteriores do Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="1734f-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="1734f-111">A tabela a seguir fornece uma lista completa das **Entidades de agendamento**.</span><span class="sxs-lookup"><span data-stu-id="1734f-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="1734f-112">Nome da entidade</span><span class="sxs-lookup"><span data-stu-id="1734f-112">Entity name</span></span>  | <span data-ttu-id="1734f-113">Nome lógico da entidade</span><span class="sxs-lookup"><span data-stu-id="1734f-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="1734f-114">Project</span><span class="sxs-lookup"><span data-stu-id="1734f-114">Project</span></span> | <span data-ttu-id="1734f-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="1734f-115">msdyn_project</span></span> |
| <span data-ttu-id="1734f-116">Tarefa do Projeto</span><span class="sxs-lookup"><span data-stu-id="1734f-116">Project Task</span></span>  | <span data-ttu-id="1734f-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="1734f-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="1734f-118">Dependência de Tarefa do Projeto</span><span class="sxs-lookup"><span data-stu-id="1734f-118">Project Task Dependency</span></span>  | <span data-ttu-id="1734f-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="1734f-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="1734f-120">Atribuição de Recurso</span><span class="sxs-lookup"><span data-stu-id="1734f-120">Resource Assignment</span></span> | <span data-ttu-id="1734f-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="1734f-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="1734f-122">Bucket do Projeto</span><span class="sxs-lookup"><span data-stu-id="1734f-122">Project Bucket</span></span>  | <span data-ttu-id="1734f-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="1734f-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="1734f-124">Membro da Equipe do Projeto</span><span class="sxs-lookup"><span data-stu-id="1734f-124">Project Team Member</span></span> | <span data-ttu-id="1734f-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="1734f-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="1734f-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="1734f-126">OperationSet</span></span>

<span data-ttu-id="1734f-127">OperationSet é um padrão de unidade de trabalho que pode ser usado quando várias solicitações de impacto de agenda devem ser processadas em uma transação.</span><span class="sxs-lookup"><span data-stu-id="1734f-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="1734f-128">APIs de programação</span><span class="sxs-lookup"><span data-stu-id="1734f-128">Schedule APIs</span></span>

<span data-ttu-id="1734f-129">A seguir está uma lista de APIs de programação atuais.</span><span class="sxs-lookup"><span data-stu-id="1734f-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="1734f-130">**msdyn_CreateProjectV1**: Esta API pode ser usada para criar um projeto.</span><span class="sxs-lookup"><span data-stu-id="1734f-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="1734f-131">O projeto e o bucket de projeto padrão são criados imediatamente.</span><span class="sxs-lookup"><span data-stu-id="1734f-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="1734f-132">**msdyn_CreateTeamMemberV1**: Esta API pode ser usada para criar um membro da equipe do projeto.</span><span class="sxs-lookup"><span data-stu-id="1734f-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="1734f-133">O registro do membro da equipe é criado imediatamente.</span><span class="sxs-lookup"><span data-stu-id="1734f-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="1734f-134">**msdyn_CreateOperationSetV1**: Esta API pode ser usada para agendar várias solicitações que devem ser executadas em uma transação.</span><span class="sxs-lookup"><span data-stu-id="1734f-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="1734f-135">**msdyn_PSSCreateV1**: Esta API pode ser usada para criar uma entidade.</span><span class="sxs-lookup"><span data-stu-id="1734f-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="1734f-136">A entidade pode ser qualquer uma das entidades de agendamento que dão suporte à operação de criação.</span><span class="sxs-lookup"><span data-stu-id="1734f-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="1734f-137">**msdyn_PSSUpdateV1**: Esta API pode ser usada para atualizar uma entidade.</span><span class="sxs-lookup"><span data-stu-id="1734f-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="1734f-138">A entidade pode ser qualquer uma das entidades de agendamento que dão suporte à operação de atualização.</span><span class="sxs-lookup"><span data-stu-id="1734f-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="1734f-139">**msdyn_PSSDeleteV1**: Esta API pode ser usada para excluir uma entidade.</span><span class="sxs-lookup"><span data-stu-id="1734f-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="1734f-140">A entidade pode ser uma das entidades de agendamento com suporte à operação de exclusão.</span><span class="sxs-lookup"><span data-stu-id="1734f-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="1734f-141">**msdyn_ExecuteOperationSetV1**: Esta API é usada para executar todas as operações no conjunto de operações especificado.</span><span class="sxs-lookup"><span data-stu-id="1734f-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="1734f-142">Usar APIs de programação com OperationSet</span><span class="sxs-lookup"><span data-stu-id="1734f-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="1734f-143">Como registros com **CreateProjectV1** e **CreateTeamMemberV1** são criados imediatamente, essas APIs não podem ser usadas diretamente no **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="1734f-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="1734f-144">No entanto, você pode usar a API para criar os registros necessários, criar um **OperationSet** e usar esses registros pré-criados no **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="1734f-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="1734f-145">Operações com suporte</span><span class="sxs-lookup"><span data-stu-id="1734f-145">Supported operations</span></span>

| <span data-ttu-id="1734f-146">Entidade de agendamento</span><span class="sxs-lookup"><span data-stu-id="1734f-146">Scheduling entity</span></span> | <span data-ttu-id="1734f-147">Criar</span><span class="sxs-lookup"><span data-stu-id="1734f-147">Create</span></span> | <span data-ttu-id="1734f-148">Atualizar</span><span class="sxs-lookup"><span data-stu-id="1734f-148">Update</span></span> | <span data-ttu-id="1734f-149">Excluir</span><span class="sxs-lookup"><span data-stu-id="1734f-149">Delete</span></span> | <span data-ttu-id="1734f-150">Considerações importantes</span><span class="sxs-lookup"><span data-stu-id="1734f-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="1734f-151">Tarefa do projeto</span><span class="sxs-lookup"><span data-stu-id="1734f-151">Project task</span></span> | <span data-ttu-id="1734f-152">Sim</span><span class="sxs-lookup"><span data-stu-id="1734f-152">Yes</span></span> | <span data-ttu-id="1734f-153">Sim</span><span class="sxs-lookup"><span data-stu-id="1734f-153">Yes</span></span> | <span data-ttu-id="1734f-154">Sim</span><span class="sxs-lookup"><span data-stu-id="1734f-154">Yes</span></span> | <span data-ttu-id="1734f-155">Nenhum(a)</span><span class="sxs-lookup"><span data-stu-id="1734f-155">None</span></span> |
| <span data-ttu-id="1734f-156">Dependência de tarefa do projeto</span><span class="sxs-lookup"><span data-stu-id="1734f-156">Project task dependency</span></span> | <span data-ttu-id="1734f-157">Sim</span><span class="sxs-lookup"><span data-stu-id="1734f-157">Yes</span></span> | <span data-ttu-id="1734f-158">Sim</span><span class="sxs-lookup"><span data-stu-id="1734f-158">Yes</span></span> | | <span data-ttu-id="1734f-159">Os registros de dependência da tarefa do projeto não são atualizados.</span><span class="sxs-lookup"><span data-stu-id="1734f-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="1734f-160">Em vez disso, um registro antigo pode ser excluído e um novo registro pode ser criado.</span><span class="sxs-lookup"><span data-stu-id="1734f-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="1734f-161">Atribuição de recurso</span><span class="sxs-lookup"><span data-stu-id="1734f-161">Resource assignment</span></span> | <span data-ttu-id="1734f-162">Sim</span><span class="sxs-lookup"><span data-stu-id="1734f-162">Yes</span></span> | <span data-ttu-id="1734f-163">Sim</span><span class="sxs-lookup"><span data-stu-id="1734f-163">Yes</span></span> | | <span data-ttu-id="1734f-164">Não há suporte a operações com os seguintes campos: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** e **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="1734f-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="1734f-165">Os registros de atribuição de recursos não são atualizados.</span><span class="sxs-lookup"><span data-stu-id="1734f-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="1734f-166">Em vez disso, o registro antigo pode ser excluído e um novo registro pode ser criado.</span><span class="sxs-lookup"><span data-stu-id="1734f-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="1734f-167">Bucket do projeto</span><span class="sxs-lookup"><span data-stu-id="1734f-167">Project bucket</span></span> | <span data-ttu-id="1734f-168">N/D</span><span class="sxs-lookup"><span data-stu-id="1734f-168">N/A</span></span> | <span data-ttu-id="1734f-169">N/D</span><span class="sxs-lookup"><span data-stu-id="1734f-169">N/A</span></span> | <span data-ttu-id="1734f-170">N/D</span><span class="sxs-lookup"><span data-stu-id="1734f-170">N/A</span></span> | <span data-ttu-id="1734f-171">O intervalo padrão é criado usando a API **CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="1734f-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="1734f-172">Membro da equipe do projeto</span><span class="sxs-lookup"><span data-stu-id="1734f-172">Project team member</span></span> | <span data-ttu-id="1734f-173">Sim</span><span class="sxs-lookup"><span data-stu-id="1734f-173">Yes</span></span> | <span data-ttu-id="1734f-174">Sim</span><span class="sxs-lookup"><span data-stu-id="1734f-174">Yes</span></span> | <span data-ttu-id="1734f-175">Sim</span><span class="sxs-lookup"><span data-stu-id="1734f-175">Yes</span></span> | <span data-ttu-id="1734f-176">Para a operação de criação, use a API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="1734f-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="1734f-177">Project</span><span class="sxs-lookup"><span data-stu-id="1734f-177">Project</span></span> | <span data-ttu-id="1734f-178">Sim</span><span class="sxs-lookup"><span data-stu-id="1734f-178">Yes</span></span> | <span data-ttu-id="1734f-179">Sim</span><span class="sxs-lookup"><span data-stu-id="1734f-179">Yes</span></span> | <span data-ttu-id="1734f-180">N/D</span><span class="sxs-lookup"><span data-stu-id="1734f-180">N/A</span></span> | <span data-ttu-id="1734f-181">Não há suporte para operações com os seguintes campos: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** e **Duration**.</span><span class="sxs-lookup"><span data-stu-id="1734f-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="1734f-182">Essas APIs podem ser chamadas com objetos de entidade que incluem campos personalizados.</span><span class="sxs-lookup"><span data-stu-id="1734f-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="1734f-183">A propriedade da ID é opcional.</span><span class="sxs-lookup"><span data-stu-id="1734f-183">The ID property is optional.</span></span> <span data-ttu-id="1734f-184">Se ela for fornecida, o sistema tentará usá-la e lançará uma exceção se ela não puder ser usada.</span><span class="sxs-lookup"><span data-stu-id="1734f-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="1734f-185">Se ela não for fornecida, o sistema irá gerá-la.</span><span class="sxs-lookup"><span data-stu-id="1734f-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="1734f-186">Campos restritos</span><span class="sxs-lookup"><span data-stu-id="1734f-186">Restricted fields</span></span>

<span data-ttu-id="1734f-187">As tabelas a seguir definem os campos que são restritos de **Criar** e **Editar**.</span><span class="sxs-lookup"><span data-stu-id="1734f-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="1734f-188">Tarefa do projeto</span><span class="sxs-lookup"><span data-stu-id="1734f-188">Project task</span></span>

| <span data-ttu-id="1734f-189">**Nome lógico**</span><span class="sxs-lookup"><span data-stu-id="1734f-189">**Logical name**</span></span>                       | <span data-ttu-id="1734f-190">**Pode criar**</span><span class="sxs-lookup"><span data-stu-id="1734f-190">**Can create**</span></span> | <span data-ttu-id="1734f-191">**Pode editar**</span><span class="sxs-lookup"><span data-stu-id="1734f-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="1734f-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="1734f-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="1734f-193">não</span><span class="sxs-lookup"><span data-stu-id="1734f-193">no</span></span>             | <span data-ttu-id="1734f-194">não</span><span class="sxs-lookup"><span data-stu-id="1734f-194">no</span></span>               |
| <span data-ttu-id="1734f-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="1734f-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="1734f-196">não</span><span class="sxs-lookup"><span data-stu-id="1734f-196">no</span></span>             | <span data-ttu-id="1734f-197">não</span><span class="sxs-lookup"><span data-stu-id="1734f-197">no</span></span>               |
| <span data-ttu-id="1734f-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="1734f-198">msdyn_actualend</span></span>                        | <span data-ttu-id="1734f-199">não</span><span class="sxs-lookup"><span data-stu-id="1734f-199">no</span></span>             | <span data-ttu-id="1734f-200">não</span><span class="sxs-lookup"><span data-stu-id="1734f-200">no</span></span>               |
| <span data-ttu-id="1734f-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="1734f-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="1734f-202">não</span><span class="sxs-lookup"><span data-stu-id="1734f-202">no</span></span>             | <span data-ttu-id="1734f-203">não</span><span class="sxs-lookup"><span data-stu-id="1734f-203">no</span></span>               |
| <span data-ttu-id="1734f-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="1734f-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="1734f-205">não</span><span class="sxs-lookup"><span data-stu-id="1734f-205">no</span></span>             | <span data-ttu-id="1734f-206">não</span><span class="sxs-lookup"><span data-stu-id="1734f-206">no</span></span>               |
| <span data-ttu-id="1734f-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="1734f-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="1734f-208">não</span><span class="sxs-lookup"><span data-stu-id="1734f-208">no</span></span>             | <span data-ttu-id="1734f-209">não</span><span class="sxs-lookup"><span data-stu-id="1734f-209">no</span></span>               |
| <span data-ttu-id="1734f-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="1734f-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="1734f-211">não</span><span class="sxs-lookup"><span data-stu-id="1734f-211">no</span></span>             | <span data-ttu-id="1734f-212">não</span><span class="sxs-lookup"><span data-stu-id="1734f-212">no</span></span>               |
| <span data-ttu-id="1734f-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="1734f-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="1734f-214">não</span><span class="sxs-lookup"><span data-stu-id="1734f-214">no</span></span>             | <span data-ttu-id="1734f-215">não</span><span class="sxs-lookup"><span data-stu-id="1734f-215">no</span></span>               |
| <span data-ttu-id="1734f-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="1734f-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="1734f-217">não</span><span class="sxs-lookup"><span data-stu-id="1734f-217">no</span></span>             | <span data-ttu-id="1734f-218">não</span><span class="sxs-lookup"><span data-stu-id="1734f-218">no</span></span>               |
| <span data-ttu-id="1734f-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="1734f-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="1734f-220">não</span><span class="sxs-lookup"><span data-stu-id="1734f-220">no</span></span>             | <span data-ttu-id="1734f-221">não</span><span class="sxs-lookup"><span data-stu-id="1734f-221">no</span></span>               |
| <span data-ttu-id="1734f-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="1734f-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="1734f-223">não</span><span class="sxs-lookup"><span data-stu-id="1734f-223">no</span></span>             | <span data-ttu-id="1734f-224">não</span><span class="sxs-lookup"><span data-stu-id="1734f-224">no</span></span>               |
| <span data-ttu-id="1734f-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="1734f-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="1734f-226">não</span><span class="sxs-lookup"><span data-stu-id="1734f-226">no</span></span>             | <span data-ttu-id="1734f-227">não</span><span class="sxs-lookup"><span data-stu-id="1734f-227">no</span></span>               |
| <span data-ttu-id="1734f-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="1734f-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="1734f-229">não</span><span class="sxs-lookup"><span data-stu-id="1734f-229">no</span></span>             | <span data-ttu-id="1734f-230">não</span><span class="sxs-lookup"><span data-stu-id="1734f-230">no</span></span>               |
| <span data-ttu-id="1734f-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="1734f-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="1734f-232">não</span><span class="sxs-lookup"><span data-stu-id="1734f-232">no</span></span>             | <span data-ttu-id="1734f-233">não</span><span class="sxs-lookup"><span data-stu-id="1734f-233">no</span></span>               |
| <span data-ttu-id="1734f-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="1734f-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="1734f-235">não</span><span class="sxs-lookup"><span data-stu-id="1734f-235">no</span></span>             | <span data-ttu-id="1734f-236">não</span><span class="sxs-lookup"><span data-stu-id="1734f-236">no</span></span>               |
| <span data-ttu-id="1734f-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="1734f-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="1734f-238">não</span><span class="sxs-lookup"><span data-stu-id="1734f-238">no</span></span>             | <span data-ttu-id="1734f-239">não</span><span class="sxs-lookup"><span data-stu-id="1734f-239">no</span></span>               |
| <span data-ttu-id="1734f-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="1734f-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="1734f-241">não</span><span class="sxs-lookup"><span data-stu-id="1734f-241">no</span></span>             | <span data-ttu-id="1734f-242">não</span><span class="sxs-lookup"><span data-stu-id="1734f-242">no</span></span>               |
| <span data-ttu-id="1734f-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="1734f-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="1734f-244">não</span><span class="sxs-lookup"><span data-stu-id="1734f-244">no</span></span>             | <span data-ttu-id="1734f-245">não</span><span class="sxs-lookup"><span data-stu-id="1734f-245">no</span></span>               |
| <span data-ttu-id="1734f-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="1734f-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="1734f-247">não</span><span class="sxs-lookup"><span data-stu-id="1734f-247">no</span></span>             | <span data-ttu-id="1734f-248">não</span><span class="sxs-lookup"><span data-stu-id="1734f-248">no</span></span>               |
| <span data-ttu-id="1734f-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="1734f-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="1734f-250">não</span><span class="sxs-lookup"><span data-stu-id="1734f-250">no</span></span>             | <span data-ttu-id="1734f-251">não</span><span class="sxs-lookup"><span data-stu-id="1734f-251">no</span></span>               |
| <span data-ttu-id="1734f-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="1734f-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="1734f-253">não</span><span class="sxs-lookup"><span data-stu-id="1734f-253">no</span></span>             | <span data-ttu-id="1734f-254">não</span><span class="sxs-lookup"><span data-stu-id="1734f-254">no</span></span>               |
| <span data-ttu-id="1734f-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="1734f-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="1734f-256">não</span><span class="sxs-lookup"><span data-stu-id="1734f-256">no</span></span>             | <span data-ttu-id="1734f-257">não</span><span class="sxs-lookup"><span data-stu-id="1734f-257">no</span></span>               |
| <span data-ttu-id="1734f-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="1734f-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="1734f-259">não</span><span class="sxs-lookup"><span data-stu-id="1734f-259">no</span></span>             | <span data-ttu-id="1734f-260">não</span><span class="sxs-lookup"><span data-stu-id="1734f-260">no</span></span>               |
| <span data-ttu-id="1734f-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="1734f-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="1734f-262">não</span><span class="sxs-lookup"><span data-stu-id="1734f-262">no</span></span>             | <span data-ttu-id="1734f-263">não</span><span class="sxs-lookup"><span data-stu-id="1734f-263">no</span></span>               |
| <span data-ttu-id="1734f-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="1734f-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="1734f-265">não</span><span class="sxs-lookup"><span data-stu-id="1734f-265">no</span></span>             | <span data-ttu-id="1734f-266">não</span><span class="sxs-lookup"><span data-stu-id="1734f-266">no</span></span>               |
| <span data-ttu-id="1734f-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="1734f-267">msdyn_progress</span></span>                         | <span data-ttu-id="1734f-268">não</span><span class="sxs-lookup"><span data-stu-id="1734f-268">no</span></span>             | <span data-ttu-id="1734f-269">não (sim para P4W)</span><span class="sxs-lookup"><span data-stu-id="1734f-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="1734f-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="1734f-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="1734f-271">não</span><span class="sxs-lookup"><span data-stu-id="1734f-271">no</span></span>             | <span data-ttu-id="1734f-272">não</span><span class="sxs-lookup"><span data-stu-id="1734f-272">no</span></span>               |
| <span data-ttu-id="1734f-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="1734f-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="1734f-274">não</span><span class="sxs-lookup"><span data-stu-id="1734f-274">no</span></span>             | <span data-ttu-id="1734f-275">não</span><span class="sxs-lookup"><span data-stu-id="1734f-275">no</span></span>               |
| <span data-ttu-id="1734f-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="1734f-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="1734f-277">não</span><span class="sxs-lookup"><span data-stu-id="1734f-277">no</span></span>             | <span data-ttu-id="1734f-278">não</span><span class="sxs-lookup"><span data-stu-id="1734f-278">no</span></span>               |
| <span data-ttu-id="1734f-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="1734f-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="1734f-280">não</span><span class="sxs-lookup"><span data-stu-id="1734f-280">no</span></span>             | <span data-ttu-id="1734f-281">não</span><span class="sxs-lookup"><span data-stu-id="1734f-281">no</span></span>               |
| <span data-ttu-id="1734f-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="1734f-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="1734f-283">não</span><span class="sxs-lookup"><span data-stu-id="1734f-283">no</span></span>             | <span data-ttu-id="1734f-284">não</span><span class="sxs-lookup"><span data-stu-id="1734f-284">no</span></span>               |
| <span data-ttu-id="1734f-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="1734f-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="1734f-286">não</span><span class="sxs-lookup"><span data-stu-id="1734f-286">no</span></span>             | <span data-ttu-id="1734f-287">não</span><span class="sxs-lookup"><span data-stu-id="1734f-287">no</span></span>               |
| <span data-ttu-id="1734f-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="1734f-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="1734f-289">não</span><span class="sxs-lookup"><span data-stu-id="1734f-289">no</span></span>             | <span data-ttu-id="1734f-290">não</span><span class="sxs-lookup"><span data-stu-id="1734f-290">no</span></span>               |
| <span data-ttu-id="1734f-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="1734f-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="1734f-292">não</span><span class="sxs-lookup"><span data-stu-id="1734f-292">no</span></span>             | <span data-ttu-id="1734f-293">não</span><span class="sxs-lookup"><span data-stu-id="1734f-293">no</span></span>               |
| <span data-ttu-id="1734f-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="1734f-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="1734f-295">não</span><span class="sxs-lookup"><span data-stu-id="1734f-295">no</span></span>             | <span data-ttu-id="1734f-296">não</span><span class="sxs-lookup"><span data-stu-id="1734f-296">no</span></span>               |
| <span data-ttu-id="1734f-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="1734f-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="1734f-298">não</span><span class="sxs-lookup"><span data-stu-id="1734f-298">no</span></span>             | <span data-ttu-id="1734f-299">não</span><span class="sxs-lookup"><span data-stu-id="1734f-299">no</span></span>               |
| <span data-ttu-id="1734f-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="1734f-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="1734f-301">não</span><span class="sxs-lookup"><span data-stu-id="1734f-301">no</span></span>             | <span data-ttu-id="1734f-302">não</span><span class="sxs-lookup"><span data-stu-id="1734f-302">no</span></span>               |
| <span data-ttu-id="1734f-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="1734f-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="1734f-304">não</span><span class="sxs-lookup"><span data-stu-id="1734f-304">no</span></span>             | <span data-ttu-id="1734f-305">não</span><span class="sxs-lookup"><span data-stu-id="1734f-305">no</span></span>               |
| <span data-ttu-id="1734f-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="1734f-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="1734f-307">não</span><span class="sxs-lookup"><span data-stu-id="1734f-307">no</span></span>             | <span data-ttu-id="1734f-308">não</span><span class="sxs-lookup"><span data-stu-id="1734f-308">no</span></span>               |
| <span data-ttu-id="1734f-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="1734f-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="1734f-310">não</span><span class="sxs-lookup"><span data-stu-id="1734f-310">no</span></span>             | <span data-ttu-id="1734f-311">não</span><span class="sxs-lookup"><span data-stu-id="1734f-311">no</span></span>               |
| <span data-ttu-id="1734f-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="1734f-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="1734f-313">não</span><span class="sxs-lookup"><span data-stu-id="1734f-313">no</span></span>             | <span data-ttu-id="1734f-314">não</span><span class="sxs-lookup"><span data-stu-id="1734f-314">no</span></span>               |
| <span data-ttu-id="1734f-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="1734f-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="1734f-316">não</span><span class="sxs-lookup"><span data-stu-id="1734f-316">no</span></span>             | <span data-ttu-id="1734f-317">não</span><span class="sxs-lookup"><span data-stu-id="1734f-317">no</span></span>               |
| <span data-ttu-id="1734f-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="1734f-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="1734f-319">não</span><span class="sxs-lookup"><span data-stu-id="1734f-319">no</span></span>             | <span data-ttu-id="1734f-320">não</span><span class="sxs-lookup"><span data-stu-id="1734f-320">no</span></span>               |
| <span data-ttu-id="1734f-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="1734f-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="1734f-322">não</span><span class="sxs-lookup"><span data-stu-id="1734f-322">no</span></span>             | <span data-ttu-id="1734f-323">não</span><span class="sxs-lookup"><span data-stu-id="1734f-323">no</span></span>               |
| <span data-ttu-id="1734f-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="1734f-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="1734f-325">não</span><span class="sxs-lookup"><span data-stu-id="1734f-325">no</span></span>             | <span data-ttu-id="1734f-326">não</span><span class="sxs-lookup"><span data-stu-id="1734f-326">no</span></span>               |
| <span data-ttu-id="1734f-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="1734f-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="1734f-328">não</span><span class="sxs-lookup"><span data-stu-id="1734f-328">no</span></span>             | <span data-ttu-id="1734f-329">não</span><span class="sxs-lookup"><span data-stu-id="1734f-329">no</span></span>               |
| <span data-ttu-id="1734f-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="1734f-330">msdyn_summary</span></span>                          | <span data-ttu-id="1734f-331">não</span><span class="sxs-lookup"><span data-stu-id="1734f-331">no</span></span>             | <span data-ttu-id="1734f-332">não</span><span class="sxs-lookup"><span data-stu-id="1734f-332">no</span></span>               |
| <span data-ttu-id="1734f-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="1734f-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="1734f-334">não</span><span class="sxs-lookup"><span data-stu-id="1734f-334">no</span></span>             | <span data-ttu-id="1734f-335">não</span><span class="sxs-lookup"><span data-stu-id="1734f-335">no</span></span>               |
| <span data-ttu-id="1734f-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="1734f-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="1734f-337">não</span><span class="sxs-lookup"><span data-stu-id="1734f-337">no</span></span>             | <span data-ttu-id="1734f-338">não</span><span class="sxs-lookup"><span data-stu-id="1734f-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="1734f-339">Dependência de tarefa do projeto</span><span class="sxs-lookup"><span data-stu-id="1734f-339">Project task dependency</span></span>

| <span data-ttu-id="1734f-340">**Nome lógico**</span><span class="sxs-lookup"><span data-stu-id="1734f-340">**Logical name**</span></span>              | <span data-ttu-id="1734f-341">**Pode criar**</span><span class="sxs-lookup"><span data-stu-id="1734f-341">**Can create**</span></span> | <span data-ttu-id="1734f-342">**Pode editar**</span><span class="sxs-lookup"><span data-stu-id="1734f-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="1734f-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="1734f-343">msdyn_linktype</span></span>                | <span data-ttu-id="1734f-344">não</span><span class="sxs-lookup"><span data-stu-id="1734f-344">no</span></span>             | <span data-ttu-id="1734f-345">não</span><span class="sxs-lookup"><span data-stu-id="1734f-345">no</span></span>           |
| <span data-ttu-id="1734f-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="1734f-346">msdyn_linktypename</span></span>            | <span data-ttu-id="1734f-347">não</span><span class="sxs-lookup"><span data-stu-id="1734f-347">no</span></span>             | <span data-ttu-id="1734f-348">não</span><span class="sxs-lookup"><span data-stu-id="1734f-348">no</span></span>           |
| <span data-ttu-id="1734f-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="1734f-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="1734f-350">sim</span><span class="sxs-lookup"><span data-stu-id="1734f-350">yes</span></span>            | <span data-ttu-id="1734f-351">não</span><span class="sxs-lookup"><span data-stu-id="1734f-351">no</span></span>           |
| <span data-ttu-id="1734f-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="1734f-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="1734f-353">sim</span><span class="sxs-lookup"><span data-stu-id="1734f-353">yes</span></span>            | <span data-ttu-id="1734f-354">não</span><span class="sxs-lookup"><span data-stu-id="1734f-354">no</span></span>           |
| <span data-ttu-id="1734f-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="1734f-355">msdyn_project</span></span>                 | <span data-ttu-id="1734f-356">sim</span><span class="sxs-lookup"><span data-stu-id="1734f-356">yes</span></span>            | <span data-ttu-id="1734f-357">não</span><span class="sxs-lookup"><span data-stu-id="1734f-357">no</span></span>           |
| <span data-ttu-id="1734f-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="1734f-358">msdyn_projectname</span></span>             | <span data-ttu-id="1734f-359">sim</span><span class="sxs-lookup"><span data-stu-id="1734f-359">yes</span></span>            | <span data-ttu-id="1734f-360">não</span><span class="sxs-lookup"><span data-stu-id="1734f-360">no</span></span>           |
| <span data-ttu-id="1734f-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="1734f-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="1734f-362">sim</span><span class="sxs-lookup"><span data-stu-id="1734f-362">yes</span></span>            | <span data-ttu-id="1734f-363">não</span><span class="sxs-lookup"><span data-stu-id="1734f-363">no</span></span>           |
| <span data-ttu-id="1734f-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="1734f-364">msdyn_successortask</span></span>           | <span data-ttu-id="1734f-365">sim</span><span class="sxs-lookup"><span data-stu-id="1734f-365">yes</span></span>            | <span data-ttu-id="1734f-366">não</span><span class="sxs-lookup"><span data-stu-id="1734f-366">no</span></span>           |
| <span data-ttu-id="1734f-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="1734f-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="1734f-368">sim</span><span class="sxs-lookup"><span data-stu-id="1734f-368">yes</span></span>            | <span data-ttu-id="1734f-369">não</span><span class="sxs-lookup"><span data-stu-id="1734f-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="1734f-370">Atribuição de recurso</span><span class="sxs-lookup"><span data-stu-id="1734f-370">Resource assignment</span></span>

| <span data-ttu-id="1734f-371">**Nome lógico**</span><span class="sxs-lookup"><span data-stu-id="1734f-371">**Logical name**</span></span>             | <span data-ttu-id="1734f-372">**Pode criar**</span><span class="sxs-lookup"><span data-stu-id="1734f-372">**Can create**</span></span> | <span data-ttu-id="1734f-373">**Pode editar**</span><span class="sxs-lookup"><span data-stu-id="1734f-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="1734f-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="1734f-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="1734f-375">sim</span><span class="sxs-lookup"><span data-stu-id="1734f-375">yes</span></span>            | <span data-ttu-id="1734f-376">não</span><span class="sxs-lookup"><span data-stu-id="1734f-376">no</span></span>           |
| <span data-ttu-id="1734f-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="1734f-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="1734f-378">sim</span><span class="sxs-lookup"><span data-stu-id="1734f-378">yes</span></span>            | <span data-ttu-id="1734f-379">não</span><span class="sxs-lookup"><span data-stu-id="1734f-379">no</span></span>           |
| <span data-ttu-id="1734f-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="1734f-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="1734f-381">não</span><span class="sxs-lookup"><span data-stu-id="1734f-381">no</span></span>             | <span data-ttu-id="1734f-382">não</span><span class="sxs-lookup"><span data-stu-id="1734f-382">no</span></span>           |
| <span data-ttu-id="1734f-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="1734f-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="1734f-384">não</span><span class="sxs-lookup"><span data-stu-id="1734f-384">no</span></span>             | <span data-ttu-id="1734f-385">não</span><span class="sxs-lookup"><span data-stu-id="1734f-385">no</span></span>           |
| <span data-ttu-id="1734f-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="1734f-386">msdyn_committype</span></span>             | <span data-ttu-id="1734f-387">não</span><span class="sxs-lookup"><span data-stu-id="1734f-387">no</span></span>             | <span data-ttu-id="1734f-388">não</span><span class="sxs-lookup"><span data-stu-id="1734f-388">no</span></span>           |
| <span data-ttu-id="1734f-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="1734f-389">msdyn_committypename</span></span>         | <span data-ttu-id="1734f-390">não</span><span class="sxs-lookup"><span data-stu-id="1734f-390">no</span></span>             | <span data-ttu-id="1734f-391">não</span><span class="sxs-lookup"><span data-stu-id="1734f-391">no</span></span>           |
| <span data-ttu-id="1734f-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="1734f-392">msdyn_effort</span></span>                 | <span data-ttu-id="1734f-393">não</span><span class="sxs-lookup"><span data-stu-id="1734f-393">no</span></span>             | <span data-ttu-id="1734f-394">não</span><span class="sxs-lookup"><span data-stu-id="1734f-394">no</span></span>           |
| <span data-ttu-id="1734f-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="1734f-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="1734f-396">não</span><span class="sxs-lookup"><span data-stu-id="1734f-396">no</span></span>             | <span data-ttu-id="1734f-397">não</span><span class="sxs-lookup"><span data-stu-id="1734f-397">no</span></span>           |
| <span data-ttu-id="1734f-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="1734f-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="1734f-399">não</span><span class="sxs-lookup"><span data-stu-id="1734f-399">no</span></span>             | <span data-ttu-id="1734f-400">não</span><span class="sxs-lookup"><span data-stu-id="1734f-400">no</span></span>           |
| <span data-ttu-id="1734f-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="1734f-401">msdyn_finish</span></span>                 | <span data-ttu-id="1734f-402">não</span><span class="sxs-lookup"><span data-stu-id="1734f-402">no</span></span>             | <span data-ttu-id="1734f-403">não</span><span class="sxs-lookup"><span data-stu-id="1734f-403">no</span></span>           |
| <span data-ttu-id="1734f-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="1734f-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="1734f-405">não</span><span class="sxs-lookup"><span data-stu-id="1734f-405">no</span></span>             | <span data-ttu-id="1734f-406">não</span><span class="sxs-lookup"><span data-stu-id="1734f-406">no</span></span>           |
| <span data-ttu-id="1734f-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="1734f-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="1734f-408">não</span><span class="sxs-lookup"><span data-stu-id="1734f-408">no</span></span>             | <span data-ttu-id="1734f-409">não</span><span class="sxs-lookup"><span data-stu-id="1734f-409">no</span></span>           |
| <span data-ttu-id="1734f-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="1734f-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="1734f-411">não</span><span class="sxs-lookup"><span data-stu-id="1734f-411">no</span></span>             | <span data-ttu-id="1734f-412">não</span><span class="sxs-lookup"><span data-stu-id="1734f-412">no</span></span>           |
| <span data-ttu-id="1734f-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="1734f-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="1734f-414">não</span><span class="sxs-lookup"><span data-stu-id="1734f-414">no</span></span>             | <span data-ttu-id="1734f-415">não</span><span class="sxs-lookup"><span data-stu-id="1734f-415">no</span></span>           |
| <span data-ttu-id="1734f-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="1734f-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="1734f-417">não</span><span class="sxs-lookup"><span data-stu-id="1734f-417">no</span></span>             | <span data-ttu-id="1734f-418">não</span><span class="sxs-lookup"><span data-stu-id="1734f-418">no</span></span>           |
| <span data-ttu-id="1734f-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="1734f-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="1734f-420">não</span><span class="sxs-lookup"><span data-stu-id="1734f-420">no</span></span>             | <span data-ttu-id="1734f-421">não</span><span class="sxs-lookup"><span data-stu-id="1734f-421">no</span></span>           |
| <span data-ttu-id="1734f-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="1734f-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="1734f-423">não</span><span class="sxs-lookup"><span data-stu-id="1734f-423">no</span></span>             | <span data-ttu-id="1734f-424">não</span><span class="sxs-lookup"><span data-stu-id="1734f-424">no</span></span>           |
| <span data-ttu-id="1734f-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="1734f-425">msdyn_projectid</span></span>              | <span data-ttu-id="1734f-426">sim</span><span class="sxs-lookup"><span data-stu-id="1734f-426">yes</span></span>            | <span data-ttu-id="1734f-427">não</span><span class="sxs-lookup"><span data-stu-id="1734f-427">no</span></span>           |
| <span data-ttu-id="1734f-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="1734f-428">msdyn_projectidname</span></span>          | <span data-ttu-id="1734f-429">não</span><span class="sxs-lookup"><span data-stu-id="1734f-429">no</span></span>             | <span data-ttu-id="1734f-430">não</span><span class="sxs-lookup"><span data-stu-id="1734f-430">no</span></span>           |
| <span data-ttu-id="1734f-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="1734f-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="1734f-432">não</span><span class="sxs-lookup"><span data-stu-id="1734f-432">no</span></span>             | <span data-ttu-id="1734f-433">não</span><span class="sxs-lookup"><span data-stu-id="1734f-433">no</span></span>           |
| <span data-ttu-id="1734f-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="1734f-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="1734f-435">não</span><span class="sxs-lookup"><span data-stu-id="1734f-435">no</span></span>             | <span data-ttu-id="1734f-436">não</span><span class="sxs-lookup"><span data-stu-id="1734f-436">no</span></span>           |
| <span data-ttu-id="1734f-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="1734f-437">msdyn_start</span></span>                  | <span data-ttu-id="1734f-438">não</span><span class="sxs-lookup"><span data-stu-id="1734f-438">no</span></span>             | <span data-ttu-id="1734f-439">não</span><span class="sxs-lookup"><span data-stu-id="1734f-439">no</span></span>           |
| <span data-ttu-id="1734f-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="1734f-440">msdyn_taskid</span></span>                 | <span data-ttu-id="1734f-441">não</span><span class="sxs-lookup"><span data-stu-id="1734f-441">no</span></span>             | <span data-ttu-id="1734f-442">não</span><span class="sxs-lookup"><span data-stu-id="1734f-442">no</span></span>           |
| <span data-ttu-id="1734f-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="1734f-443">msdyn_taskidname</span></span>             | <span data-ttu-id="1734f-444">não</span><span class="sxs-lookup"><span data-stu-id="1734f-444">no</span></span>             | <span data-ttu-id="1734f-445">não</span><span class="sxs-lookup"><span data-stu-id="1734f-445">no</span></span>           |
| <span data-ttu-id="1734f-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="1734f-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="1734f-447">não</span><span class="sxs-lookup"><span data-stu-id="1734f-447">no</span></span>             | <span data-ttu-id="1734f-448">não</span><span class="sxs-lookup"><span data-stu-id="1734f-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="1734f-449">Membro da equipe do projeto</span><span class="sxs-lookup"><span data-stu-id="1734f-449">Project team member</span></span>

| <span data-ttu-id="1734f-450">**Nome lógico**</span><span class="sxs-lookup"><span data-stu-id="1734f-450">**Logical name**</span></span>                                 | <span data-ttu-id="1734f-451">**Pode criar**</span><span class="sxs-lookup"><span data-stu-id="1734f-451">**Can create**</span></span> | <span data-ttu-id="1734f-452">**Pode editar**</span><span class="sxs-lookup"><span data-stu-id="1734f-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="1734f-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="1734f-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="1734f-454">não</span><span class="sxs-lookup"><span data-stu-id="1734f-454">no</span></span>             | <span data-ttu-id="1734f-455">não</span><span class="sxs-lookup"><span data-stu-id="1734f-455">no</span></span>           |
| <span data-ttu-id="1734f-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="1734f-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="1734f-457">não</span><span class="sxs-lookup"><span data-stu-id="1734f-457">no</span></span>             | <span data-ttu-id="1734f-458">não</span><span class="sxs-lookup"><span data-stu-id="1734f-458">no</span></span>           |
| <span data-ttu-id="1734f-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="1734f-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="1734f-460">não</span><span class="sxs-lookup"><span data-stu-id="1734f-460">no</span></span>             | <span data-ttu-id="1734f-461">não</span><span class="sxs-lookup"><span data-stu-id="1734f-461">no</span></span>           |
| <span data-ttu-id="1734f-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="1734f-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="1734f-463">não</span><span class="sxs-lookup"><span data-stu-id="1734f-463">no</span></span>             | <span data-ttu-id="1734f-464">não</span><span class="sxs-lookup"><span data-stu-id="1734f-464">no</span></span>           |
| <span data-ttu-id="1734f-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="1734f-465">msdyn_effort</span></span>                                     | <span data-ttu-id="1734f-466">não</span><span class="sxs-lookup"><span data-stu-id="1734f-466">no</span></span>             | <span data-ttu-id="1734f-467">não</span><span class="sxs-lookup"><span data-stu-id="1734f-467">no</span></span>           |
| <span data-ttu-id="1734f-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="1734f-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="1734f-469">não</span><span class="sxs-lookup"><span data-stu-id="1734f-469">no</span></span>             | <span data-ttu-id="1734f-470">não</span><span class="sxs-lookup"><span data-stu-id="1734f-470">no</span></span>           |
| <span data-ttu-id="1734f-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="1734f-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="1734f-472">não</span><span class="sxs-lookup"><span data-stu-id="1734f-472">no</span></span>             | <span data-ttu-id="1734f-473">não</span><span class="sxs-lookup"><span data-stu-id="1734f-473">no</span></span>           |
| <span data-ttu-id="1734f-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="1734f-474">msdyn_finish</span></span>                                     | <span data-ttu-id="1734f-475">não</span><span class="sxs-lookup"><span data-stu-id="1734f-475">no</span></span>             | <span data-ttu-id="1734f-476">não</span><span class="sxs-lookup"><span data-stu-id="1734f-476">no</span></span>           |
| <span data-ttu-id="1734f-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="1734f-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="1734f-478">não</span><span class="sxs-lookup"><span data-stu-id="1734f-478">no</span></span>             | <span data-ttu-id="1734f-479">não</span><span class="sxs-lookup"><span data-stu-id="1734f-479">no</span></span>           |
| <span data-ttu-id="1734f-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="1734f-480">msdyn_hours</span></span>                                      | <span data-ttu-id="1734f-481">não</span><span class="sxs-lookup"><span data-stu-id="1734f-481">no</span></span>             | <span data-ttu-id="1734f-482">não</span><span class="sxs-lookup"><span data-stu-id="1734f-482">no</span></span>           |
| <span data-ttu-id="1734f-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="1734f-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="1734f-484">não</span><span class="sxs-lookup"><span data-stu-id="1734f-484">no</span></span>             | <span data-ttu-id="1734f-485">não</span><span class="sxs-lookup"><span data-stu-id="1734f-485">no</span></span>           |
| <span data-ttu-id="1734f-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="1734f-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="1734f-487">não</span><span class="sxs-lookup"><span data-stu-id="1734f-487">no</span></span>             | <span data-ttu-id="1734f-488">não</span><span class="sxs-lookup"><span data-stu-id="1734f-488">no</span></span>           |
| <span data-ttu-id="1734f-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="1734f-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="1734f-490">não</span><span class="sxs-lookup"><span data-stu-id="1734f-490">no</span></span>             | <span data-ttu-id="1734f-491">não</span><span class="sxs-lookup"><span data-stu-id="1734f-491">no</span></span>           |
| <span data-ttu-id="1734f-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="1734f-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="1734f-493">não</span><span class="sxs-lookup"><span data-stu-id="1734f-493">no</span></span>             | <span data-ttu-id="1734f-494">não</span><span class="sxs-lookup"><span data-stu-id="1734f-494">no</span></span>           |
| <span data-ttu-id="1734f-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="1734f-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="1734f-496">não</span><span class="sxs-lookup"><span data-stu-id="1734f-496">no</span></span>             | <span data-ttu-id="1734f-497">não</span><span class="sxs-lookup"><span data-stu-id="1734f-497">no</span></span>           |
| <span data-ttu-id="1734f-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="1734f-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="1734f-499">não</span><span class="sxs-lookup"><span data-stu-id="1734f-499">no</span></span>             | <span data-ttu-id="1734f-500">não</span><span class="sxs-lookup"><span data-stu-id="1734f-500">no</span></span>           |
| <span data-ttu-id="1734f-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="1734f-501">msdyn_start</span></span>                                      | <span data-ttu-id="1734f-502">não</span><span class="sxs-lookup"><span data-stu-id="1734f-502">no</span></span>             | <span data-ttu-id="1734f-503">não</span><span class="sxs-lookup"><span data-stu-id="1734f-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="1734f-504">Project</span><span class="sxs-lookup"><span data-stu-id="1734f-504">Project</span></span>

| <span data-ttu-id="1734f-505">**Nome lógico**</span><span class="sxs-lookup"><span data-stu-id="1734f-505">**Logical name**</span></span>                       | <span data-ttu-id="1734f-506">**Pode criar**</span><span class="sxs-lookup"><span data-stu-id="1734f-506">**Can create**</span></span> | <span data-ttu-id="1734f-507">**Pode editar**</span><span class="sxs-lookup"><span data-stu-id="1734f-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="1734f-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="1734f-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="1734f-509">não</span><span class="sxs-lookup"><span data-stu-id="1734f-509">no</span></span>             | <span data-ttu-id="1734f-510">não</span><span class="sxs-lookup"><span data-stu-id="1734f-510">no</span></span>           |
| <span data-ttu-id="1734f-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="1734f-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="1734f-512">não</span><span class="sxs-lookup"><span data-stu-id="1734f-512">no</span></span>             | <span data-ttu-id="1734f-513">não</span><span class="sxs-lookup"><span data-stu-id="1734f-513">no</span></span>           |
| <span data-ttu-id="1734f-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="1734f-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="1734f-515">não</span><span class="sxs-lookup"><span data-stu-id="1734f-515">no</span></span>             | <span data-ttu-id="1734f-516">não</span><span class="sxs-lookup"><span data-stu-id="1734f-516">no</span></span>           |
| <span data-ttu-id="1734f-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="1734f-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="1734f-518">não</span><span class="sxs-lookup"><span data-stu-id="1734f-518">no</span></span>             | <span data-ttu-id="1734f-519">não</span><span class="sxs-lookup"><span data-stu-id="1734f-519">no</span></span>           |
| <span data-ttu-id="1734f-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="1734f-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="1734f-521">não</span><span class="sxs-lookup"><span data-stu-id="1734f-521">no</span></span>             | <span data-ttu-id="1734f-522">não</span><span class="sxs-lookup"><span data-stu-id="1734f-522">no</span></span>           |
| <span data-ttu-id="1734f-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="1734f-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="1734f-524">não</span><span class="sxs-lookup"><span data-stu-id="1734f-524">no</span></span>             | <span data-ttu-id="1734f-525">não</span><span class="sxs-lookup"><span data-stu-id="1734f-525">no</span></span>           |
| <span data-ttu-id="1734f-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="1734f-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="1734f-527">sim</span><span class="sxs-lookup"><span data-stu-id="1734f-527">yes</span></span>            | <span data-ttu-id="1734f-528">não</span><span class="sxs-lookup"><span data-stu-id="1734f-528">no</span></span>           |
| <span data-ttu-id="1734f-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="1734f-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="1734f-530">sim</span><span class="sxs-lookup"><span data-stu-id="1734f-530">yes</span></span>            | <span data-ttu-id="1734f-531">não</span><span class="sxs-lookup"><span data-stu-id="1734f-531">no</span></span>           |
| <span data-ttu-id="1734f-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="1734f-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="1734f-533">sim</span><span class="sxs-lookup"><span data-stu-id="1734f-533">yes</span></span>            | <span data-ttu-id="1734f-534">não</span><span class="sxs-lookup"><span data-stu-id="1734f-534">no</span></span>           |
| <span data-ttu-id="1734f-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="1734f-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="1734f-536">não</span><span class="sxs-lookup"><span data-stu-id="1734f-536">no</span></span>             | <span data-ttu-id="1734f-537">não</span><span class="sxs-lookup"><span data-stu-id="1734f-537">no</span></span>           |
| <span data-ttu-id="1734f-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="1734f-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="1734f-539">não</span><span class="sxs-lookup"><span data-stu-id="1734f-539">no</span></span>             | <span data-ttu-id="1734f-540">não</span><span class="sxs-lookup"><span data-stu-id="1734f-540">no</span></span>           |
| <span data-ttu-id="1734f-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="1734f-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="1734f-542">não</span><span class="sxs-lookup"><span data-stu-id="1734f-542">no</span></span>             | <span data-ttu-id="1734f-543">não</span><span class="sxs-lookup"><span data-stu-id="1734f-543">no</span></span>           |
| <span data-ttu-id="1734f-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="1734f-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="1734f-545">não</span><span class="sxs-lookup"><span data-stu-id="1734f-545">no</span></span>             | <span data-ttu-id="1734f-546">não</span><span class="sxs-lookup"><span data-stu-id="1734f-546">no</span></span>           |
| <span data-ttu-id="1734f-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="1734f-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="1734f-548">não</span><span class="sxs-lookup"><span data-stu-id="1734f-548">no</span></span>             | <span data-ttu-id="1734f-549">não</span><span class="sxs-lookup"><span data-stu-id="1734f-549">no</span></span>           |
| <span data-ttu-id="1734f-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="1734f-550">msdyn_duration</span></span>                         | <span data-ttu-id="1734f-551">não</span><span class="sxs-lookup"><span data-stu-id="1734f-551">no</span></span>             | <span data-ttu-id="1734f-552">não</span><span class="sxs-lookup"><span data-stu-id="1734f-552">no</span></span>           |
| <span data-ttu-id="1734f-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="1734f-553">msdyn_effort</span></span>                           | <span data-ttu-id="1734f-554">não</span><span class="sxs-lookup"><span data-stu-id="1734f-554">no</span></span>             | <span data-ttu-id="1734f-555">não</span><span class="sxs-lookup"><span data-stu-id="1734f-555">no</span></span>           |
| <span data-ttu-id="1734f-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="1734f-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="1734f-557">não</span><span class="sxs-lookup"><span data-stu-id="1734f-557">no</span></span>             | <span data-ttu-id="1734f-558">não</span><span class="sxs-lookup"><span data-stu-id="1734f-558">no</span></span>           |
| <span data-ttu-id="1734f-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="1734f-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="1734f-560">não</span><span class="sxs-lookup"><span data-stu-id="1734f-560">no</span></span>             | <span data-ttu-id="1734f-561">não</span><span class="sxs-lookup"><span data-stu-id="1734f-561">no</span></span>           |
| <span data-ttu-id="1734f-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="1734f-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="1734f-563">não</span><span class="sxs-lookup"><span data-stu-id="1734f-563">no</span></span>             | <span data-ttu-id="1734f-564">não</span><span class="sxs-lookup"><span data-stu-id="1734f-564">no</span></span>           |
| <span data-ttu-id="1734f-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="1734f-565">msdyn_finish</span></span>                           | <span data-ttu-id="1734f-566">sim</span><span class="sxs-lookup"><span data-stu-id="1734f-566">yes</span></span>            | <span data-ttu-id="1734f-567">sim</span><span class="sxs-lookup"><span data-stu-id="1734f-567">yes</span></span>          |
| <span data-ttu-id="1734f-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="1734f-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="1734f-569">não</span><span class="sxs-lookup"><span data-stu-id="1734f-569">no</span></span>             | <span data-ttu-id="1734f-570">não</span><span class="sxs-lookup"><span data-stu-id="1734f-570">no</span></span>           |
| <span data-ttu-id="1734f-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="1734f-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="1734f-572">não</span><span class="sxs-lookup"><span data-stu-id="1734f-572">no</span></span>             | <span data-ttu-id="1734f-573">não</span><span class="sxs-lookup"><span data-stu-id="1734f-573">no</span></span>           |
| <span data-ttu-id="1734f-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="1734f-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="1734f-575">não</span><span class="sxs-lookup"><span data-stu-id="1734f-575">no</span></span>             | <span data-ttu-id="1734f-576">não</span><span class="sxs-lookup"><span data-stu-id="1734f-576">no</span></span>           |
| <span data-ttu-id="1734f-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="1734f-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="1734f-578">não</span><span class="sxs-lookup"><span data-stu-id="1734f-578">no</span></span>             | <span data-ttu-id="1734f-579">não</span><span class="sxs-lookup"><span data-stu-id="1734f-579">no</span></span>           |
| <span data-ttu-id="1734f-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="1734f-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="1734f-581">não</span><span class="sxs-lookup"><span data-stu-id="1734f-581">no</span></span>             | <span data-ttu-id="1734f-582">não</span><span class="sxs-lookup"><span data-stu-id="1734f-582">no</span></span>           |
| <span data-ttu-id="1734f-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="1734f-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="1734f-584">não</span><span class="sxs-lookup"><span data-stu-id="1734f-584">no</span></span>             | <span data-ttu-id="1734f-585">não</span><span class="sxs-lookup"><span data-stu-id="1734f-585">no</span></span>           |
| <span data-ttu-id="1734f-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="1734f-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="1734f-587">não</span><span class="sxs-lookup"><span data-stu-id="1734f-587">no</span></span>             | <span data-ttu-id="1734f-588">não</span><span class="sxs-lookup"><span data-stu-id="1734f-588">no</span></span>           |
| <span data-ttu-id="1734f-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="1734f-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="1734f-590">não</span><span class="sxs-lookup"><span data-stu-id="1734f-590">no</span></span>             | <span data-ttu-id="1734f-591">não</span><span class="sxs-lookup"><span data-stu-id="1734f-591">no</span></span>           |
| <span data-ttu-id="1734f-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="1734f-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="1734f-593">não</span><span class="sxs-lookup"><span data-stu-id="1734f-593">no</span></span>             | <span data-ttu-id="1734f-594">não</span><span class="sxs-lookup"><span data-stu-id="1734f-594">no</span></span>           |
| <span data-ttu-id="1734f-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="1734f-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="1734f-596">não</span><span class="sxs-lookup"><span data-stu-id="1734f-596">no</span></span>             | <span data-ttu-id="1734f-597">não</span><span class="sxs-lookup"><span data-stu-id="1734f-597">no</span></span>           |
| <span data-ttu-id="1734f-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="1734f-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="1734f-599">não</span><span class="sxs-lookup"><span data-stu-id="1734f-599">no</span></span>             | <span data-ttu-id="1734f-600">não</span><span class="sxs-lookup"><span data-stu-id="1734f-600">no</span></span>           |
| <span data-ttu-id="1734f-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="1734f-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="1734f-602">não</span><span class="sxs-lookup"><span data-stu-id="1734f-602">no</span></span>             | <span data-ttu-id="1734f-603">não</span><span class="sxs-lookup"><span data-stu-id="1734f-603">no</span></span>           |
| <span data-ttu-id="1734f-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="1734f-604">msdyn_progress</span></span>                         | <span data-ttu-id="1734f-605">não</span><span class="sxs-lookup"><span data-stu-id="1734f-605">no</span></span>             | <span data-ttu-id="1734f-606">não</span><span class="sxs-lookup"><span data-stu-id="1734f-606">no</span></span>           |
| <span data-ttu-id="1734f-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="1734f-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="1734f-608">não</span><span class="sxs-lookup"><span data-stu-id="1734f-608">no</span></span>             | <span data-ttu-id="1734f-609">não</span><span class="sxs-lookup"><span data-stu-id="1734f-609">no</span></span>           |
| <span data-ttu-id="1734f-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="1734f-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="1734f-611">não</span><span class="sxs-lookup"><span data-stu-id="1734f-611">no</span></span>             | <span data-ttu-id="1734f-612">não</span><span class="sxs-lookup"><span data-stu-id="1734f-612">no</span></span>           |
| <span data-ttu-id="1734f-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="1734f-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="1734f-614">não</span><span class="sxs-lookup"><span data-stu-id="1734f-614">no</span></span>             | <span data-ttu-id="1734f-615">não</span><span class="sxs-lookup"><span data-stu-id="1734f-615">no</span></span>           |
| <span data-ttu-id="1734f-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="1734f-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="1734f-617">não</span><span class="sxs-lookup"><span data-stu-id="1734f-617">no</span></span>             | <span data-ttu-id="1734f-618">não</span><span class="sxs-lookup"><span data-stu-id="1734f-618">no</span></span>           |
| <span data-ttu-id="1734f-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="1734f-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="1734f-620">não</span><span class="sxs-lookup"><span data-stu-id="1734f-620">no</span></span>             | <span data-ttu-id="1734f-621">não</span><span class="sxs-lookup"><span data-stu-id="1734f-621">no</span></span>           |
| <span data-ttu-id="1734f-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="1734f-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="1734f-623">não</span><span class="sxs-lookup"><span data-stu-id="1734f-623">no</span></span>             | <span data-ttu-id="1734f-624">não</span><span class="sxs-lookup"><span data-stu-id="1734f-624">no</span></span>           |
| <span data-ttu-id="1734f-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="1734f-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="1734f-626">não</span><span class="sxs-lookup"><span data-stu-id="1734f-626">no</span></span>             | <span data-ttu-id="1734f-627">não</span><span class="sxs-lookup"><span data-stu-id="1734f-627">no</span></span>           |
| <span data-ttu-id="1734f-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="1734f-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="1734f-629">não</span><span class="sxs-lookup"><span data-stu-id="1734f-629">no</span></span>             | <span data-ttu-id="1734f-630">não</span><span class="sxs-lookup"><span data-stu-id="1734f-630">no</span></span>           |
| <span data-ttu-id="1734f-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="1734f-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="1734f-632">não</span><span class="sxs-lookup"><span data-stu-id="1734f-632">no</span></span>             | <span data-ttu-id="1734f-633">não</span><span class="sxs-lookup"><span data-stu-id="1734f-633">no</span></span>           |
| <span data-ttu-id="1734f-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="1734f-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="1734f-635">não</span><span class="sxs-lookup"><span data-stu-id="1734f-635">no</span></span>             | <span data-ttu-id="1734f-636">não</span><span class="sxs-lookup"><span data-stu-id="1734f-636">no</span></span>           |
| <span data-ttu-id="1734f-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="1734f-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="1734f-638">não</span><span class="sxs-lookup"><span data-stu-id="1734f-638">no</span></span>             | <span data-ttu-id="1734f-639">não</span><span class="sxs-lookup"><span data-stu-id="1734f-639">no</span></span>           |
| <span data-ttu-id="1734f-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="1734f-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="1734f-641">não</span><span class="sxs-lookup"><span data-stu-id="1734f-641">no</span></span>             | <span data-ttu-id="1734f-642">não</span><span class="sxs-lookup"><span data-stu-id="1734f-642">no</span></span>           |
| <span data-ttu-id="1734f-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="1734f-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="1734f-644">não</span><span class="sxs-lookup"><span data-stu-id="1734f-644">no</span></span>             | <span data-ttu-id="1734f-645">não</span><span class="sxs-lookup"><span data-stu-id="1734f-645">no</span></span>           |
| <span data-ttu-id="1734f-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="1734f-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="1734f-647">não</span><span class="sxs-lookup"><span data-stu-id="1734f-647">no</span></span>             | <span data-ttu-id="1734f-648">não</span><span class="sxs-lookup"><span data-stu-id="1734f-648">no</span></span>           |
| <span data-ttu-id="1734f-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="1734f-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="1734f-650">não</span><span class="sxs-lookup"><span data-stu-id="1734f-650">no</span></span>             | <span data-ttu-id="1734f-651">não</span><span class="sxs-lookup"><span data-stu-id="1734f-651">no</span></span>           |
| <span data-ttu-id="1734f-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="1734f-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="1734f-653">não</span><span class="sxs-lookup"><span data-stu-id="1734f-653">no</span></span>             | <span data-ttu-id="1734f-654">não</span><span class="sxs-lookup"><span data-stu-id="1734f-654">no</span></span>           |
| <span data-ttu-id="1734f-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="1734f-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="1734f-656">não</span><span class="sxs-lookup"><span data-stu-id="1734f-656">no</span></span>             | <span data-ttu-id="1734f-657">não</span><span class="sxs-lookup"><span data-stu-id="1734f-657">no</span></span>           |
| <span data-ttu-id="1734f-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="1734f-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="1734f-659">não</span><span class="sxs-lookup"><span data-stu-id="1734f-659">no</span></span>             | <span data-ttu-id="1734f-660">não</span><span class="sxs-lookup"><span data-stu-id="1734f-660">no</span></span>           |
| <span data-ttu-id="1734f-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="1734f-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="1734f-662">não</span><span class="sxs-lookup"><span data-stu-id="1734f-662">no</span></span>             | <span data-ttu-id="1734f-663">não</span><span class="sxs-lookup"><span data-stu-id="1734f-663">no</span></span>           |
| <span data-ttu-id="1734f-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="1734f-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="1734f-665">não</span><span class="sxs-lookup"><span data-stu-id="1734f-665">no</span></span>             | <span data-ttu-id="1734f-666">não</span><span class="sxs-lookup"><span data-stu-id="1734f-666">no</span></span>           |
| <span data-ttu-id="1734f-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="1734f-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="1734f-668">não</span><span class="sxs-lookup"><span data-stu-id="1734f-668">no</span></span>             | <span data-ttu-id="1734f-669">não</span><span class="sxs-lookup"><span data-stu-id="1734f-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="1734f-670">Limitações e problemas conhecidos</span><span class="sxs-lookup"><span data-stu-id="1734f-670">Limitations and known issues</span></span>
<span data-ttu-id="1734f-671">Esta é uma lista de limitações e problemas conhecidos:</span><span class="sxs-lookup"><span data-stu-id="1734f-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="1734f-672">APIs de programação só podem ser usadas por **Usuários com licença do Microsoft Project**.</span><span class="sxs-lookup"><span data-stu-id="1734f-672">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="1734f-673">Elas não podem ser usadas por:</span><span class="sxs-lookup"><span data-stu-id="1734f-673">They can't be used by:</span></span>
    - <span data-ttu-id="1734f-674">Usuários do aplicativo</span><span class="sxs-lookup"><span data-stu-id="1734f-674">Application users</span></span>
    - <span data-ttu-id="1734f-675">Usuários do sistema</span><span class="sxs-lookup"><span data-stu-id="1734f-675">System users</span></span>
    - <span data-ttu-id="1734f-676">Usuários de Integração</span><span class="sxs-lookup"><span data-stu-id="1734f-676">Integration users</span></span>
    - <span data-ttu-id="1734f-677">Outros usuários sem a licença necessária</span><span class="sxs-lookup"><span data-stu-id="1734f-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="1734f-678">Cada **OperationSet** pode ter no máximo 100 operações.</span><span class="sxs-lookup"><span data-stu-id="1734f-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="1734f-679">Cada usuário pode ter no máximo 10 **OperationSets** abertos.</span><span class="sxs-lookup"><span data-stu-id="1734f-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="1734f-680">No momento, o Project Operations dá suporte no máximo a 500 tarefas em um projeto.</span><span class="sxs-lookup"><span data-stu-id="1734f-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="1734f-681">O status de falha e logs de falha do **OperationSet** não estão disponíveis no momento.</span><span class="sxs-lookup"><span data-stu-id="1734f-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- [<span data-ttu-id="1734f-682">Limites em projetos e tarefas</span><span class="sxs-lookup"><span data-stu-id="1734f-682">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="1734f-683">Tratamento de erros</span><span class="sxs-lookup"><span data-stu-id="1734f-683">Error handling</span></span>

   - <span data-ttu-id="1734f-684">Para revisar erros gerados a partir dos Conjuntos de Operações, acesse **Configurações** \> **Integração de Agenda** \> **Conjuntos de Operações**.</span><span class="sxs-lookup"><span data-stu-id="1734f-684">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="1734f-685">Para revisar erros gerados a partir do Serviço de Agendamento de Projetos, acesse **Configurações** \> **Integração de Agenda** \> **Logs de Erros PSS**.</span><span class="sxs-lookup"><span data-stu-id="1734f-685">To review errors generated from the Project Scheduling Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="1734f-686">Cenário de exemplo</span><span class="sxs-lookup"><span data-stu-id="1734f-686">Sample scenario</span></span>

<span data-ttu-id="1734f-687">Neste cenário, você criará um projeto, um membro da equipe, quatro tarefas e duas atribuições de recursos.</span><span class="sxs-lookup"><span data-stu-id="1734f-687">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="1734f-688">Em seguida, você atualizará uma tarefa, atualizará o projeto, excluirá uma tarefa, excluirá uma atribuição de recurso e criará uma dependência de tarefa.</span><span class="sxs-lookup"><span data-stu-id="1734f-688">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

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

## <a name="additional-samples"></a><span data-ttu-id="1734f-689">Exemplos adicionais</span><span class="sxs-lookup"><span data-stu-id="1734f-689">Additional samples</span></span>

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
