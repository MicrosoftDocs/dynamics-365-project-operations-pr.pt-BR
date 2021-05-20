---
title: Use APIs de programação para realizar operações com entidades de agendamento
description: Este tópico fornece informações e exemplos para usar APIs de programação.
author: sigitac
manager: Annbe
ms.date: 04/27/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e03f4e6c49a835206b23cade3fabe3fd26693441
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950790"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="a9a0a-103">Use APIs de programação para realizar operações com entidades de agendamento</span><span class="sxs-lookup"><span data-stu-id="a9a0a-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="a9a0a-104">_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_</span><span class="sxs-lookup"><span data-stu-id="a9a0a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="a9a0a-105">Parte de ou toda a funcionalidade observada neste tópico está disponível como parte de uma versão preliminar.</span><span class="sxs-lookup"><span data-stu-id="a9a0a-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="a9a0a-106">O conteúdo e a funcionalidade estão sujeitos a alterações.</span><span class="sxs-lookup"><span data-stu-id="a9a0a-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="a9a0a-107">Entidades de agendamento</span><span class="sxs-lookup"><span data-stu-id="a9a0a-107">Scheduling entities</span></span>

<span data-ttu-id="a9a0a-108">As APIs de programação fornecem a capacidade de executar operações de criação, atualização e exclusão com **Entidades de agendamento**.</span><span class="sxs-lookup"><span data-stu-id="a9a0a-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="a9a0a-109">Essas entidades são gerenciadas por meio do mecanismo de agendamento no projeto para a Web.</span><span class="sxs-lookup"><span data-stu-id="a9a0a-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="a9a0a-110">Criar, atualizar e excluir operações com **Entidades de agendamento** foram restritos em versões anteriores do Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="a9a0a-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="a9a0a-111">A tabela a seguir fornece uma lista completa das **Entidades de agendamento**.</span><span class="sxs-lookup"><span data-stu-id="a9a0a-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="a9a0a-112">Nome da entidade</span><span class="sxs-lookup"><span data-stu-id="a9a0a-112">Entity name</span></span>  | <span data-ttu-id="a9a0a-113">Nome lógico da entidade</span><span class="sxs-lookup"><span data-stu-id="a9a0a-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="a9a0a-114">Project</span><span class="sxs-lookup"><span data-stu-id="a9a0a-114">Project</span></span> | <span data-ttu-id="a9a0a-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="a9a0a-115">msdyn_project</span></span> |
| <span data-ttu-id="a9a0a-116">Tarefa do Projeto</span><span class="sxs-lookup"><span data-stu-id="a9a0a-116">Project Task</span></span>  | <span data-ttu-id="a9a0a-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="a9a0a-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="a9a0a-118">Dependência de Tarefa do Projeto</span><span class="sxs-lookup"><span data-stu-id="a9a0a-118">Project Task Dependency</span></span>  | <span data-ttu-id="a9a0a-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="a9a0a-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="a9a0a-120">Atribuição de Recurso</span><span class="sxs-lookup"><span data-stu-id="a9a0a-120">Resource Assignment</span></span> | <span data-ttu-id="a9a0a-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="a9a0a-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="a9a0a-122">Bucket do Projeto</span><span class="sxs-lookup"><span data-stu-id="a9a0a-122">Project Bucket</span></span>  | <span data-ttu-id="a9a0a-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="a9a0a-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="a9a0a-124">Membro da Equipe do Projeto</span><span class="sxs-lookup"><span data-stu-id="a9a0a-124">Project Team Member</span></span> | <span data-ttu-id="a9a0a-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="a9a0a-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="a9a0a-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="a9a0a-126">OperationSet</span></span>

<span data-ttu-id="a9a0a-127">OperationSet é um padrão de unidade de trabalho que pode ser usado quando várias solicitações de impacto de agenda devem ser processadas em uma transação.</span><span class="sxs-lookup"><span data-stu-id="a9a0a-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="a9a0a-128">APIs de programação</span><span class="sxs-lookup"><span data-stu-id="a9a0a-128">Schedule APIs</span></span>

<span data-ttu-id="a9a0a-129">A seguir está uma lista de APIs de programação atuais.</span><span class="sxs-lookup"><span data-stu-id="a9a0a-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="a9a0a-130">**msdyn_CreateProjectV1**: Esta API pode ser usada para criar um projeto.</span><span class="sxs-lookup"><span data-stu-id="a9a0a-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="a9a0a-131">O projeto e o bucket de projeto padrão são criados imediatamente.</span><span class="sxs-lookup"><span data-stu-id="a9a0a-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="a9a0a-132">**msdyn_CreateTeamMemberV1**: Esta API pode ser usada para criar um membro da equipe do projeto.</span><span class="sxs-lookup"><span data-stu-id="a9a0a-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="a9a0a-133">O registro do membro da equipe é criado imediatamente.</span><span class="sxs-lookup"><span data-stu-id="a9a0a-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="a9a0a-134">**msdyn_CreateOperationSetV1**: Esta API pode ser usada para agendar várias solicitações que devem ser executadas em uma transação.</span><span class="sxs-lookup"><span data-stu-id="a9a0a-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="a9a0a-135">**msdyn_PSSCreateV1**: Esta API pode ser usada para criar uma entidade.</span><span class="sxs-lookup"><span data-stu-id="a9a0a-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="a9a0a-136">A entidade pode ser qualquer uma das entidades de agendamento que dão suporte à operação de criação.</span><span class="sxs-lookup"><span data-stu-id="a9a0a-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="a9a0a-137">**msdyn_PSSUpdateV1**: Esta API pode ser usada para atualizar uma entidade.</span><span class="sxs-lookup"><span data-stu-id="a9a0a-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="a9a0a-138">A entidade pode ser qualquer uma das entidades de agendamento que dão suporte à operação de atualização.</span><span class="sxs-lookup"><span data-stu-id="a9a0a-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="a9a0a-139">**msdyn_PSSDeleteV1**: Esta API pode ser usada para excluir uma entidade.</span><span class="sxs-lookup"><span data-stu-id="a9a0a-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="a9a0a-140">A entidade pode ser uma das entidades de agendamento com suporte à operação de exclusão.</span><span class="sxs-lookup"><span data-stu-id="a9a0a-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="a9a0a-141">**msdyn_ExecuteOperationSetV1**: Esta API é usada para executar todas as operações no conjunto de operações especificado.</span><span class="sxs-lookup"><span data-stu-id="a9a0a-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="a9a0a-142">Usar APIs de programação com OperationSet</span><span class="sxs-lookup"><span data-stu-id="a9a0a-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="a9a0a-143">Como registros com **CreateProjectV1** e **CreateTeamMemberV1** são criados imediatamente, essas APIs não podem ser usadas diretamente no **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="a9a0a-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="a9a0a-144">No entanto, você pode usar a API para criar os registros necessários, criar um **OperationSet** e usar esses registros pré-criados no **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="a9a0a-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="a9a0a-145">Operações com suporte</span><span class="sxs-lookup"><span data-stu-id="a9a0a-145">Supported operations</span></span>

| <span data-ttu-id="a9a0a-146">Entidade de agendamento</span><span class="sxs-lookup"><span data-stu-id="a9a0a-146">Scheduling entity</span></span> | <span data-ttu-id="a9a0a-147">Criar</span><span class="sxs-lookup"><span data-stu-id="a9a0a-147">Create</span></span> | <span data-ttu-id="a9a0a-148">Atualizar</span><span class="sxs-lookup"><span data-stu-id="a9a0a-148">Update</span></span> | <span data-ttu-id="a9a0a-149">Excluir</span><span class="sxs-lookup"><span data-stu-id="a9a0a-149">Delete</span></span> | <span data-ttu-id="a9a0a-150">Considerações importantes</span><span class="sxs-lookup"><span data-stu-id="a9a0a-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="a9a0a-151">Tarefa do projeto</span><span class="sxs-lookup"><span data-stu-id="a9a0a-151">Project task</span></span> | <span data-ttu-id="a9a0a-152">Sim</span><span class="sxs-lookup"><span data-stu-id="a9a0a-152">Yes</span></span> | <span data-ttu-id="a9a0a-153">Sim</span><span class="sxs-lookup"><span data-stu-id="a9a0a-153">Yes</span></span> | <span data-ttu-id="a9a0a-154">Sim</span><span class="sxs-lookup"><span data-stu-id="a9a0a-154">Yes</span></span> | <span data-ttu-id="a9a0a-155">Nenhum(a)</span><span class="sxs-lookup"><span data-stu-id="a9a0a-155">None</span></span> |
| <span data-ttu-id="a9a0a-156">Dependência de tarefa do projeto</span><span class="sxs-lookup"><span data-stu-id="a9a0a-156">Project task dependency</span></span> | <span data-ttu-id="a9a0a-157">Sim</span><span class="sxs-lookup"><span data-stu-id="a9a0a-157">Yes</span></span> | <span data-ttu-id="a9a0a-158">Sim</span><span class="sxs-lookup"><span data-stu-id="a9a0a-158">Yes</span></span> | | <span data-ttu-id="a9a0a-159">Os registros de dependência da tarefa do projeto não são atualizados.</span><span class="sxs-lookup"><span data-stu-id="a9a0a-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="a9a0a-160">Em vez disso, um registro antigo pode ser excluído e um novo registro pode ser criado.</span><span class="sxs-lookup"><span data-stu-id="a9a0a-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="a9a0a-161">Atribuição de recurso</span><span class="sxs-lookup"><span data-stu-id="a9a0a-161">Resource assignment</span></span> | <span data-ttu-id="a9a0a-162">Sim</span><span class="sxs-lookup"><span data-stu-id="a9a0a-162">Yes</span></span> | <span data-ttu-id="a9a0a-163">Sim</span><span class="sxs-lookup"><span data-stu-id="a9a0a-163">Yes</span></span> | | <span data-ttu-id="a9a0a-164">Não há suporte a operações com os seguintes campos: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** e **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="a9a0a-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="a9a0a-165">Os registros de atribuição de recursos não são atualizados.</span><span class="sxs-lookup"><span data-stu-id="a9a0a-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="a9a0a-166">Em vez disso, o registro antigo pode ser excluído e um novo registro pode ser criado.</span><span class="sxs-lookup"><span data-stu-id="a9a0a-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="a9a0a-167">Bucket do projeto</span><span class="sxs-lookup"><span data-stu-id="a9a0a-167">Project bucket</span></span> | <span data-ttu-id="a9a0a-168">N/D</span><span class="sxs-lookup"><span data-stu-id="a9a0a-168">N/A</span></span> | <span data-ttu-id="a9a0a-169">N/D</span><span class="sxs-lookup"><span data-stu-id="a9a0a-169">N/A</span></span> | <span data-ttu-id="a9a0a-170">N/D</span><span class="sxs-lookup"><span data-stu-id="a9a0a-170">N/A</span></span> | <span data-ttu-id="a9a0a-171">O intervalo padrão é criado usando a API **CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="a9a0a-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="a9a0a-172">Membro da equipe do projeto</span><span class="sxs-lookup"><span data-stu-id="a9a0a-172">Project team member</span></span> | <span data-ttu-id="a9a0a-173">Sim</span><span class="sxs-lookup"><span data-stu-id="a9a0a-173">Yes</span></span> | <span data-ttu-id="a9a0a-174">Sim</span><span class="sxs-lookup"><span data-stu-id="a9a0a-174">Yes</span></span> | <span data-ttu-id="a9a0a-175">Sim</span><span class="sxs-lookup"><span data-stu-id="a9a0a-175">Yes</span></span> | <span data-ttu-id="a9a0a-176">Para a operação de criação, use a API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="a9a0a-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="a9a0a-177">Project</span><span class="sxs-lookup"><span data-stu-id="a9a0a-177">Project</span></span> | <span data-ttu-id="a9a0a-178">Sim</span><span class="sxs-lookup"><span data-stu-id="a9a0a-178">Yes</span></span> | <span data-ttu-id="a9a0a-179">Sim</span><span class="sxs-lookup"><span data-stu-id="a9a0a-179">Yes</span></span> | <span data-ttu-id="a9a0a-180">N/D</span><span class="sxs-lookup"><span data-stu-id="a9a0a-180">N/A</span></span> | <span data-ttu-id="a9a0a-181">Não há suporte para operações com os seguintes campos: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** e **Duration**.</span><span class="sxs-lookup"><span data-stu-id="a9a0a-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="a9a0a-182">Essas APIs podem ser chamadas com objetos de entidade que incluem campos personalizados.</span><span class="sxs-lookup"><span data-stu-id="a9a0a-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="a9a0a-183">A propriedade da ID é opcional.</span><span class="sxs-lookup"><span data-stu-id="a9a0a-183">The ID property is optional.</span></span> <span data-ttu-id="a9a0a-184">Se ela for fornecida, o sistema tentará usá-la e lançará uma exceção se ela não puder ser usada.</span><span class="sxs-lookup"><span data-stu-id="a9a0a-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="a9a0a-185">Se ela não for fornecida, o sistema irá gerá-la.</span><span class="sxs-lookup"><span data-stu-id="a9a0a-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="a9a0a-186">Campos restritos</span><span class="sxs-lookup"><span data-stu-id="a9a0a-186">Restricted fields</span></span>

<span data-ttu-id="a9a0a-187">As tabelas a seguir definem os campos que são restritos de **Criar** e **Editar**.</span><span class="sxs-lookup"><span data-stu-id="a9a0a-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="a9a0a-188">Tarefa do projeto</span><span class="sxs-lookup"><span data-stu-id="a9a0a-188">Project task</span></span>

| <span data-ttu-id="a9a0a-189">**Nome lógico**</span><span class="sxs-lookup"><span data-stu-id="a9a0a-189">**Logical name**</span></span>                       | <span data-ttu-id="a9a0a-190">**Pode criar**</span><span class="sxs-lookup"><span data-stu-id="a9a0a-190">**Can create**</span></span> | <span data-ttu-id="a9a0a-191">**Pode editar**</span><span class="sxs-lookup"><span data-stu-id="a9a0a-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="a9a0a-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="a9a0a-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="a9a0a-193">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-193">no</span></span>             | <span data-ttu-id="a9a0a-194">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-194">no</span></span>               |
| <span data-ttu-id="a9a0a-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="a9a0a-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="a9a0a-196">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-196">no</span></span>             | <span data-ttu-id="a9a0a-197">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-197">no</span></span>               |
| <span data-ttu-id="a9a0a-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="a9a0a-198">msdyn_actualend</span></span>                        | <span data-ttu-id="a9a0a-199">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-199">no</span></span>             | <span data-ttu-id="a9a0a-200">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-200">no</span></span>               |
| <span data-ttu-id="a9a0a-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="a9a0a-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="a9a0a-202">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-202">no</span></span>             | <span data-ttu-id="a9a0a-203">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-203">no</span></span>               |
| <span data-ttu-id="a9a0a-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="a9a0a-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="a9a0a-205">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-205">no</span></span>             | <span data-ttu-id="a9a0a-206">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-206">no</span></span>               |
| <span data-ttu-id="a9a0a-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="a9a0a-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="a9a0a-208">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-208">no</span></span>             | <span data-ttu-id="a9a0a-209">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-209">no</span></span>               |
| <span data-ttu-id="a9a0a-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="a9a0a-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="a9a0a-211">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-211">no</span></span>             | <span data-ttu-id="a9a0a-212">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-212">no</span></span>               |
| <span data-ttu-id="a9a0a-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="a9a0a-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="a9a0a-214">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-214">no</span></span>             | <span data-ttu-id="a9a0a-215">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-215">no</span></span>               |
| <span data-ttu-id="a9a0a-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="a9a0a-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="a9a0a-217">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-217">no</span></span>             | <span data-ttu-id="a9a0a-218">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-218">no</span></span>               |
| <span data-ttu-id="a9a0a-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="a9a0a-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="a9a0a-220">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-220">no</span></span>             | <span data-ttu-id="a9a0a-221">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-221">no</span></span>               |
| <span data-ttu-id="a9a0a-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="a9a0a-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="a9a0a-223">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-223">no</span></span>             | <span data-ttu-id="a9a0a-224">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-224">no</span></span>               |
| <span data-ttu-id="a9a0a-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="a9a0a-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="a9a0a-226">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-226">no</span></span>             | <span data-ttu-id="a9a0a-227">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-227">no</span></span>               |
| <span data-ttu-id="a9a0a-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="a9a0a-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="a9a0a-229">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-229">no</span></span>             | <span data-ttu-id="a9a0a-230">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-230">no</span></span>               |
| <span data-ttu-id="a9a0a-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="a9a0a-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="a9a0a-232">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-232">no</span></span>             | <span data-ttu-id="a9a0a-233">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-233">no</span></span>               |
| <span data-ttu-id="a9a0a-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="a9a0a-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="a9a0a-235">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-235">no</span></span>             | <span data-ttu-id="a9a0a-236">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-236">no</span></span>               |
| <span data-ttu-id="a9a0a-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="a9a0a-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="a9a0a-238">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-238">no</span></span>             | <span data-ttu-id="a9a0a-239">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-239">no</span></span>               |
| <span data-ttu-id="a9a0a-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="a9a0a-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="a9a0a-241">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-241">no</span></span>             | <span data-ttu-id="a9a0a-242">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-242">no</span></span>               |
| <span data-ttu-id="a9a0a-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="a9a0a-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="a9a0a-244">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-244">no</span></span>             | <span data-ttu-id="a9a0a-245">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-245">no</span></span>               |
| <span data-ttu-id="a9a0a-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="a9a0a-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="a9a0a-247">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-247">no</span></span>             | <span data-ttu-id="a9a0a-248">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-248">no</span></span>               |
| <span data-ttu-id="a9a0a-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="a9a0a-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="a9a0a-250">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-250">no</span></span>             | <span data-ttu-id="a9a0a-251">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-251">no</span></span>               |
| <span data-ttu-id="a9a0a-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="a9a0a-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="a9a0a-253">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-253">no</span></span>             | <span data-ttu-id="a9a0a-254">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-254">no</span></span>               |
| <span data-ttu-id="a9a0a-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="a9a0a-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="a9a0a-256">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-256">no</span></span>             | <span data-ttu-id="a9a0a-257">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-257">no</span></span>               |
| <span data-ttu-id="a9a0a-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="a9a0a-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="a9a0a-259">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-259">no</span></span>             | <span data-ttu-id="a9a0a-260">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-260">no</span></span>               |
| <span data-ttu-id="a9a0a-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="a9a0a-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="a9a0a-262">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-262">no</span></span>             | <span data-ttu-id="a9a0a-263">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-263">no</span></span>               |
| <span data-ttu-id="a9a0a-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="a9a0a-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="a9a0a-265">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-265">no</span></span>             | <span data-ttu-id="a9a0a-266">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-266">no</span></span>               |
| <span data-ttu-id="a9a0a-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="a9a0a-267">msdyn_progress</span></span>                         | <span data-ttu-id="a9a0a-268">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-268">no</span></span>             | <span data-ttu-id="a9a0a-269">não (sim para P4W)</span><span class="sxs-lookup"><span data-stu-id="a9a0a-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="a9a0a-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="a9a0a-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="a9a0a-271">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-271">no</span></span>             | <span data-ttu-id="a9a0a-272">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-272">no</span></span>               |
| <span data-ttu-id="a9a0a-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="a9a0a-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="a9a0a-274">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-274">no</span></span>             | <span data-ttu-id="a9a0a-275">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-275">no</span></span>               |
| <span data-ttu-id="a9a0a-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="a9a0a-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="a9a0a-277">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-277">no</span></span>             | <span data-ttu-id="a9a0a-278">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-278">no</span></span>               |
| <span data-ttu-id="a9a0a-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="a9a0a-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="a9a0a-280">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-280">no</span></span>             | <span data-ttu-id="a9a0a-281">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-281">no</span></span>               |
| <span data-ttu-id="a9a0a-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="a9a0a-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="a9a0a-283">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-283">no</span></span>             | <span data-ttu-id="a9a0a-284">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-284">no</span></span>               |
| <span data-ttu-id="a9a0a-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="a9a0a-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="a9a0a-286">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-286">no</span></span>             | <span data-ttu-id="a9a0a-287">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-287">no</span></span>               |
| <span data-ttu-id="a9a0a-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="a9a0a-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="a9a0a-289">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-289">no</span></span>             | <span data-ttu-id="a9a0a-290">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-290">no</span></span>               |
| <span data-ttu-id="a9a0a-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="a9a0a-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="a9a0a-292">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-292">no</span></span>             | <span data-ttu-id="a9a0a-293">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-293">no</span></span>               |
| <span data-ttu-id="a9a0a-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="a9a0a-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="a9a0a-295">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-295">no</span></span>             | <span data-ttu-id="a9a0a-296">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-296">no</span></span>               |
| <span data-ttu-id="a9a0a-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="a9a0a-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="a9a0a-298">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-298">no</span></span>             | <span data-ttu-id="a9a0a-299">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-299">no</span></span>               |
| <span data-ttu-id="a9a0a-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="a9a0a-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="a9a0a-301">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-301">no</span></span>             | <span data-ttu-id="a9a0a-302">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-302">no</span></span>               |
| <span data-ttu-id="a9a0a-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="a9a0a-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="a9a0a-304">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-304">no</span></span>             | <span data-ttu-id="a9a0a-305">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-305">no</span></span>               |
| <span data-ttu-id="a9a0a-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="a9a0a-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="a9a0a-307">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-307">no</span></span>             | <span data-ttu-id="a9a0a-308">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-308">no</span></span>               |
| <span data-ttu-id="a9a0a-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="a9a0a-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="a9a0a-310">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-310">no</span></span>             | <span data-ttu-id="a9a0a-311">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-311">no</span></span>               |
| <span data-ttu-id="a9a0a-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="a9a0a-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="a9a0a-313">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-313">no</span></span>             | <span data-ttu-id="a9a0a-314">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-314">no</span></span>               |
| <span data-ttu-id="a9a0a-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="a9a0a-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="a9a0a-316">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-316">no</span></span>             | <span data-ttu-id="a9a0a-317">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-317">no</span></span>               |
| <span data-ttu-id="a9a0a-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="a9a0a-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="a9a0a-319">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-319">no</span></span>             | <span data-ttu-id="a9a0a-320">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-320">no</span></span>               |
| <span data-ttu-id="a9a0a-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="a9a0a-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="a9a0a-322">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-322">no</span></span>             | <span data-ttu-id="a9a0a-323">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-323">no</span></span>               |
| <span data-ttu-id="a9a0a-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="a9a0a-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="a9a0a-325">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-325">no</span></span>             | <span data-ttu-id="a9a0a-326">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-326">no</span></span>               |
| <span data-ttu-id="a9a0a-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="a9a0a-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="a9a0a-328">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-328">no</span></span>             | <span data-ttu-id="a9a0a-329">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-329">no</span></span>               |
| <span data-ttu-id="a9a0a-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="a9a0a-330">msdyn_summary</span></span>                          | <span data-ttu-id="a9a0a-331">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-331">no</span></span>             | <span data-ttu-id="a9a0a-332">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-332">no</span></span>               |
| <span data-ttu-id="a9a0a-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="a9a0a-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="a9a0a-334">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-334">no</span></span>             | <span data-ttu-id="a9a0a-335">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-335">no</span></span>               |
| <span data-ttu-id="a9a0a-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="a9a0a-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="a9a0a-337">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-337">no</span></span>             | <span data-ttu-id="a9a0a-338">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="a9a0a-339">Dependência de tarefa do projeto</span><span class="sxs-lookup"><span data-stu-id="a9a0a-339">Project task dependency</span></span>

| <span data-ttu-id="a9a0a-340">**Nome lógico**</span><span class="sxs-lookup"><span data-stu-id="a9a0a-340">**Logical name**</span></span>              | <span data-ttu-id="a9a0a-341">**Pode criar**</span><span class="sxs-lookup"><span data-stu-id="a9a0a-341">**Can create**</span></span> | <span data-ttu-id="a9a0a-342">**Pode editar**</span><span class="sxs-lookup"><span data-stu-id="a9a0a-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="a9a0a-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="a9a0a-343">msdyn_linktype</span></span>                | <span data-ttu-id="a9a0a-344">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-344">no</span></span>             | <span data-ttu-id="a9a0a-345">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-345">no</span></span>           |
| <span data-ttu-id="a9a0a-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="a9a0a-346">msdyn_linktypename</span></span>            | <span data-ttu-id="a9a0a-347">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-347">no</span></span>             | <span data-ttu-id="a9a0a-348">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-348">no</span></span>           |
| <span data-ttu-id="a9a0a-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="a9a0a-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="a9a0a-350">sim</span><span class="sxs-lookup"><span data-stu-id="a9a0a-350">yes</span></span>            | <span data-ttu-id="a9a0a-351">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-351">no</span></span>           |
| <span data-ttu-id="a9a0a-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="a9a0a-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="a9a0a-353">sim</span><span class="sxs-lookup"><span data-stu-id="a9a0a-353">yes</span></span>            | <span data-ttu-id="a9a0a-354">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-354">no</span></span>           |
| <span data-ttu-id="a9a0a-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="a9a0a-355">msdyn_project</span></span>                 | <span data-ttu-id="a9a0a-356">sim</span><span class="sxs-lookup"><span data-stu-id="a9a0a-356">yes</span></span>            | <span data-ttu-id="a9a0a-357">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-357">no</span></span>           |
| <span data-ttu-id="a9a0a-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="a9a0a-358">msdyn_projectname</span></span>             | <span data-ttu-id="a9a0a-359">sim</span><span class="sxs-lookup"><span data-stu-id="a9a0a-359">yes</span></span>            | <span data-ttu-id="a9a0a-360">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-360">no</span></span>           |
| <span data-ttu-id="a9a0a-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="a9a0a-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="a9a0a-362">sim</span><span class="sxs-lookup"><span data-stu-id="a9a0a-362">yes</span></span>            | <span data-ttu-id="a9a0a-363">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-363">no</span></span>           |
| <span data-ttu-id="a9a0a-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="a9a0a-364">msdyn_successortask</span></span>           | <span data-ttu-id="a9a0a-365">sim</span><span class="sxs-lookup"><span data-stu-id="a9a0a-365">yes</span></span>            | <span data-ttu-id="a9a0a-366">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-366">no</span></span>           |
| <span data-ttu-id="a9a0a-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="a9a0a-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="a9a0a-368">sim</span><span class="sxs-lookup"><span data-stu-id="a9a0a-368">yes</span></span>            | <span data-ttu-id="a9a0a-369">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="a9a0a-370">Atribuição de recurso</span><span class="sxs-lookup"><span data-stu-id="a9a0a-370">Resource assignment</span></span>

| <span data-ttu-id="a9a0a-371">**Nome lógico**</span><span class="sxs-lookup"><span data-stu-id="a9a0a-371">**Logical name**</span></span>             | <span data-ttu-id="a9a0a-372">**Pode criar**</span><span class="sxs-lookup"><span data-stu-id="a9a0a-372">**Can create**</span></span> | <span data-ttu-id="a9a0a-373">**Pode editar**</span><span class="sxs-lookup"><span data-stu-id="a9a0a-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="a9a0a-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="a9a0a-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="a9a0a-375">sim</span><span class="sxs-lookup"><span data-stu-id="a9a0a-375">yes</span></span>            | <span data-ttu-id="a9a0a-376">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-376">no</span></span>           |
| <span data-ttu-id="a9a0a-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="a9a0a-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="a9a0a-378">sim</span><span class="sxs-lookup"><span data-stu-id="a9a0a-378">yes</span></span>            | <span data-ttu-id="a9a0a-379">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-379">no</span></span>           |
| <span data-ttu-id="a9a0a-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="a9a0a-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="a9a0a-381">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-381">no</span></span>             | <span data-ttu-id="a9a0a-382">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-382">no</span></span>           |
| <span data-ttu-id="a9a0a-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="a9a0a-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="a9a0a-384">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-384">no</span></span>             | <span data-ttu-id="a9a0a-385">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-385">no</span></span>           |
| <span data-ttu-id="a9a0a-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="a9a0a-386">msdyn_committype</span></span>             | <span data-ttu-id="a9a0a-387">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-387">no</span></span>             | <span data-ttu-id="a9a0a-388">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-388">no</span></span>           |
| <span data-ttu-id="a9a0a-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="a9a0a-389">msdyn_committypename</span></span>         | <span data-ttu-id="a9a0a-390">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-390">no</span></span>             | <span data-ttu-id="a9a0a-391">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-391">no</span></span>           |
| <span data-ttu-id="a9a0a-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="a9a0a-392">msdyn_effort</span></span>                 | <span data-ttu-id="a9a0a-393">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-393">no</span></span>             | <span data-ttu-id="a9a0a-394">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-394">no</span></span>           |
| <span data-ttu-id="a9a0a-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="a9a0a-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="a9a0a-396">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-396">no</span></span>             | <span data-ttu-id="a9a0a-397">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-397">no</span></span>           |
| <span data-ttu-id="a9a0a-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="a9a0a-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="a9a0a-399">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-399">no</span></span>             | <span data-ttu-id="a9a0a-400">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-400">no</span></span>           |
| <span data-ttu-id="a9a0a-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="a9a0a-401">msdyn_finish</span></span>                 | <span data-ttu-id="a9a0a-402">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-402">no</span></span>             | <span data-ttu-id="a9a0a-403">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-403">no</span></span>           |
| <span data-ttu-id="a9a0a-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="a9a0a-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="a9a0a-405">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-405">no</span></span>             | <span data-ttu-id="a9a0a-406">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-406">no</span></span>           |
| <span data-ttu-id="a9a0a-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="a9a0a-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="a9a0a-408">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-408">no</span></span>             | <span data-ttu-id="a9a0a-409">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-409">no</span></span>           |
| <span data-ttu-id="a9a0a-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="a9a0a-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="a9a0a-411">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-411">no</span></span>             | <span data-ttu-id="a9a0a-412">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-412">no</span></span>           |
| <span data-ttu-id="a9a0a-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="a9a0a-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="a9a0a-414">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-414">no</span></span>             | <span data-ttu-id="a9a0a-415">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-415">no</span></span>           |
| <span data-ttu-id="a9a0a-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="a9a0a-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="a9a0a-417">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-417">no</span></span>             | <span data-ttu-id="a9a0a-418">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-418">no</span></span>           |
| <span data-ttu-id="a9a0a-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="a9a0a-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="a9a0a-420">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-420">no</span></span>             | <span data-ttu-id="a9a0a-421">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-421">no</span></span>           |
| <span data-ttu-id="a9a0a-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="a9a0a-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="a9a0a-423">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-423">no</span></span>             | <span data-ttu-id="a9a0a-424">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-424">no</span></span>           |
| <span data-ttu-id="a9a0a-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="a9a0a-425">msdyn_projectid</span></span>              | <span data-ttu-id="a9a0a-426">sim</span><span class="sxs-lookup"><span data-stu-id="a9a0a-426">yes</span></span>            | <span data-ttu-id="a9a0a-427">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-427">no</span></span>           |
| <span data-ttu-id="a9a0a-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="a9a0a-428">msdyn_projectidname</span></span>          | <span data-ttu-id="a9a0a-429">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-429">no</span></span>             | <span data-ttu-id="a9a0a-430">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-430">no</span></span>           |
| <span data-ttu-id="a9a0a-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="a9a0a-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="a9a0a-432">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-432">no</span></span>             | <span data-ttu-id="a9a0a-433">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-433">no</span></span>           |
| <span data-ttu-id="a9a0a-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="a9a0a-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="a9a0a-435">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-435">no</span></span>             | <span data-ttu-id="a9a0a-436">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-436">no</span></span>           |
| <span data-ttu-id="a9a0a-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="a9a0a-437">msdyn_start</span></span>                  | <span data-ttu-id="a9a0a-438">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-438">no</span></span>             | <span data-ttu-id="a9a0a-439">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-439">no</span></span>           |
| <span data-ttu-id="a9a0a-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="a9a0a-440">msdyn_taskid</span></span>                 | <span data-ttu-id="a9a0a-441">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-441">no</span></span>             | <span data-ttu-id="a9a0a-442">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-442">no</span></span>           |
| <span data-ttu-id="a9a0a-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="a9a0a-443">msdyn_taskidname</span></span>             | <span data-ttu-id="a9a0a-444">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-444">no</span></span>             | <span data-ttu-id="a9a0a-445">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-445">no</span></span>           |
| <span data-ttu-id="a9a0a-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="a9a0a-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="a9a0a-447">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-447">no</span></span>             | <span data-ttu-id="a9a0a-448">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="a9a0a-449">Membro da equipe do projeto</span><span class="sxs-lookup"><span data-stu-id="a9a0a-449">Project team member</span></span>

| <span data-ttu-id="a9a0a-450">**Nome lógico**</span><span class="sxs-lookup"><span data-stu-id="a9a0a-450">**Logical name**</span></span>                                 | <span data-ttu-id="a9a0a-451">**Pode criar**</span><span class="sxs-lookup"><span data-stu-id="a9a0a-451">**Can create**</span></span> | <span data-ttu-id="a9a0a-452">**Pode editar**</span><span class="sxs-lookup"><span data-stu-id="a9a0a-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="a9a0a-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="a9a0a-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="a9a0a-454">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-454">no</span></span>             | <span data-ttu-id="a9a0a-455">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-455">no</span></span>           |
| <span data-ttu-id="a9a0a-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="a9a0a-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="a9a0a-457">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-457">no</span></span>             | <span data-ttu-id="a9a0a-458">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-458">no</span></span>           |
| <span data-ttu-id="a9a0a-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="a9a0a-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="a9a0a-460">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-460">no</span></span>             | <span data-ttu-id="a9a0a-461">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-461">no</span></span>           |
| <span data-ttu-id="a9a0a-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="a9a0a-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="a9a0a-463">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-463">no</span></span>             | <span data-ttu-id="a9a0a-464">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-464">no</span></span>           |
| <span data-ttu-id="a9a0a-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="a9a0a-465">msdyn_effort</span></span>                                     | <span data-ttu-id="a9a0a-466">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-466">no</span></span>             | <span data-ttu-id="a9a0a-467">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-467">no</span></span>           |
| <span data-ttu-id="a9a0a-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="a9a0a-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="a9a0a-469">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-469">no</span></span>             | <span data-ttu-id="a9a0a-470">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-470">no</span></span>           |
| <span data-ttu-id="a9a0a-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="a9a0a-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="a9a0a-472">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-472">no</span></span>             | <span data-ttu-id="a9a0a-473">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-473">no</span></span>           |
| <span data-ttu-id="a9a0a-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="a9a0a-474">msdyn_finish</span></span>                                     | <span data-ttu-id="a9a0a-475">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-475">no</span></span>             | <span data-ttu-id="a9a0a-476">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-476">no</span></span>           |
| <span data-ttu-id="a9a0a-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="a9a0a-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="a9a0a-478">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-478">no</span></span>             | <span data-ttu-id="a9a0a-479">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-479">no</span></span>           |
| <span data-ttu-id="a9a0a-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="a9a0a-480">msdyn_hours</span></span>                                      | <span data-ttu-id="a9a0a-481">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-481">no</span></span>             | <span data-ttu-id="a9a0a-482">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-482">no</span></span>           |
| <span data-ttu-id="a9a0a-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="a9a0a-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="a9a0a-484">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-484">no</span></span>             | <span data-ttu-id="a9a0a-485">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-485">no</span></span>           |
| <span data-ttu-id="a9a0a-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="a9a0a-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="a9a0a-487">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-487">no</span></span>             | <span data-ttu-id="a9a0a-488">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-488">no</span></span>           |
| <span data-ttu-id="a9a0a-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="a9a0a-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="a9a0a-490">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-490">no</span></span>             | <span data-ttu-id="a9a0a-491">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-491">no</span></span>           |
| <span data-ttu-id="a9a0a-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="a9a0a-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="a9a0a-493">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-493">no</span></span>             | <span data-ttu-id="a9a0a-494">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-494">no</span></span>           |
| <span data-ttu-id="a9a0a-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="a9a0a-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="a9a0a-496">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-496">no</span></span>             | <span data-ttu-id="a9a0a-497">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-497">no</span></span>           |
| <span data-ttu-id="a9a0a-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="a9a0a-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="a9a0a-499">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-499">no</span></span>             | <span data-ttu-id="a9a0a-500">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-500">no</span></span>           |
| <span data-ttu-id="a9a0a-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="a9a0a-501">msdyn_start</span></span>                                      | <span data-ttu-id="a9a0a-502">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-502">no</span></span>             | <span data-ttu-id="a9a0a-503">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="a9a0a-504">Project</span><span class="sxs-lookup"><span data-stu-id="a9a0a-504">Project</span></span>

| <span data-ttu-id="a9a0a-505">**Nome lógico**</span><span class="sxs-lookup"><span data-stu-id="a9a0a-505">**Logical name**</span></span>                       | <span data-ttu-id="a9a0a-506">**Pode criar**</span><span class="sxs-lookup"><span data-stu-id="a9a0a-506">**Can create**</span></span> | <span data-ttu-id="a9a0a-507">**Pode editar**</span><span class="sxs-lookup"><span data-stu-id="a9a0a-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="a9a0a-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="a9a0a-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="a9a0a-509">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-509">no</span></span>             | <span data-ttu-id="a9a0a-510">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-510">no</span></span>           |
| <span data-ttu-id="a9a0a-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="a9a0a-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="a9a0a-512">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-512">no</span></span>             | <span data-ttu-id="a9a0a-513">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-513">no</span></span>           |
| <span data-ttu-id="a9a0a-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="a9a0a-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="a9a0a-515">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-515">no</span></span>             | <span data-ttu-id="a9a0a-516">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-516">no</span></span>           |
| <span data-ttu-id="a9a0a-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="a9a0a-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="a9a0a-518">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-518">no</span></span>             | <span data-ttu-id="a9a0a-519">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-519">no</span></span>           |
| <span data-ttu-id="a9a0a-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="a9a0a-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="a9a0a-521">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-521">no</span></span>             | <span data-ttu-id="a9a0a-522">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-522">no</span></span>           |
| <span data-ttu-id="a9a0a-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="a9a0a-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="a9a0a-524">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-524">no</span></span>             | <span data-ttu-id="a9a0a-525">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-525">no</span></span>           |
| <span data-ttu-id="a9a0a-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="a9a0a-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="a9a0a-527">sim</span><span class="sxs-lookup"><span data-stu-id="a9a0a-527">yes</span></span>            | <span data-ttu-id="a9a0a-528">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-528">no</span></span>           |
| <span data-ttu-id="a9a0a-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="a9a0a-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="a9a0a-530">sim</span><span class="sxs-lookup"><span data-stu-id="a9a0a-530">yes</span></span>            | <span data-ttu-id="a9a0a-531">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-531">no</span></span>           |
| <span data-ttu-id="a9a0a-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="a9a0a-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="a9a0a-533">sim</span><span class="sxs-lookup"><span data-stu-id="a9a0a-533">yes</span></span>            | <span data-ttu-id="a9a0a-534">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-534">no</span></span>           |
| <span data-ttu-id="a9a0a-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="a9a0a-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="a9a0a-536">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-536">no</span></span>             | <span data-ttu-id="a9a0a-537">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-537">no</span></span>           |
| <span data-ttu-id="a9a0a-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="a9a0a-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="a9a0a-539">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-539">no</span></span>             | <span data-ttu-id="a9a0a-540">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-540">no</span></span>           |
| <span data-ttu-id="a9a0a-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="a9a0a-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="a9a0a-542">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-542">no</span></span>             | <span data-ttu-id="a9a0a-543">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-543">no</span></span>           |
| <span data-ttu-id="a9a0a-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="a9a0a-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="a9a0a-545">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-545">no</span></span>             | <span data-ttu-id="a9a0a-546">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-546">no</span></span>           |
| <span data-ttu-id="a9a0a-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="a9a0a-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="a9a0a-548">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-548">no</span></span>             | <span data-ttu-id="a9a0a-549">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-549">no</span></span>           |
| <span data-ttu-id="a9a0a-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="a9a0a-550">msdyn_duration</span></span>                         | <span data-ttu-id="a9a0a-551">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-551">no</span></span>             | <span data-ttu-id="a9a0a-552">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-552">no</span></span>           |
| <span data-ttu-id="a9a0a-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="a9a0a-553">msdyn_effort</span></span>                           | <span data-ttu-id="a9a0a-554">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-554">no</span></span>             | <span data-ttu-id="a9a0a-555">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-555">no</span></span>           |
| <span data-ttu-id="a9a0a-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="a9a0a-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="a9a0a-557">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-557">no</span></span>             | <span data-ttu-id="a9a0a-558">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-558">no</span></span>           |
| <span data-ttu-id="a9a0a-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="a9a0a-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="a9a0a-560">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-560">no</span></span>             | <span data-ttu-id="a9a0a-561">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-561">no</span></span>           |
| <span data-ttu-id="a9a0a-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="a9a0a-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="a9a0a-563">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-563">no</span></span>             | <span data-ttu-id="a9a0a-564">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-564">no</span></span>           |
| <span data-ttu-id="a9a0a-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="a9a0a-565">msdyn_finish</span></span>                           | <span data-ttu-id="a9a0a-566">sim</span><span class="sxs-lookup"><span data-stu-id="a9a0a-566">yes</span></span>            | <span data-ttu-id="a9a0a-567">sim</span><span class="sxs-lookup"><span data-stu-id="a9a0a-567">yes</span></span>          |
| <span data-ttu-id="a9a0a-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="a9a0a-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="a9a0a-569">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-569">no</span></span>             | <span data-ttu-id="a9a0a-570">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-570">no</span></span>           |
| <span data-ttu-id="a9a0a-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="a9a0a-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="a9a0a-572">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-572">no</span></span>             | <span data-ttu-id="a9a0a-573">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-573">no</span></span>           |
| <span data-ttu-id="a9a0a-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="a9a0a-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="a9a0a-575">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-575">no</span></span>             | <span data-ttu-id="a9a0a-576">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-576">no</span></span>           |
| <span data-ttu-id="a9a0a-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="a9a0a-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="a9a0a-578">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-578">no</span></span>             | <span data-ttu-id="a9a0a-579">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-579">no</span></span>           |
| <span data-ttu-id="a9a0a-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="a9a0a-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="a9a0a-581">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-581">no</span></span>             | <span data-ttu-id="a9a0a-582">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-582">no</span></span>           |
| <span data-ttu-id="a9a0a-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="a9a0a-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="a9a0a-584">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-584">no</span></span>             | <span data-ttu-id="a9a0a-585">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-585">no</span></span>           |
| <span data-ttu-id="a9a0a-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="a9a0a-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="a9a0a-587">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-587">no</span></span>             | <span data-ttu-id="a9a0a-588">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-588">no</span></span>           |
| <span data-ttu-id="a9a0a-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="a9a0a-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="a9a0a-590">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-590">no</span></span>             | <span data-ttu-id="a9a0a-591">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-591">no</span></span>           |
| <span data-ttu-id="a9a0a-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="a9a0a-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="a9a0a-593">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-593">no</span></span>             | <span data-ttu-id="a9a0a-594">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-594">no</span></span>           |
| <span data-ttu-id="a9a0a-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="a9a0a-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="a9a0a-596">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-596">no</span></span>             | <span data-ttu-id="a9a0a-597">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-597">no</span></span>           |
| <span data-ttu-id="a9a0a-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="a9a0a-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="a9a0a-599">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-599">no</span></span>             | <span data-ttu-id="a9a0a-600">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-600">no</span></span>           |
| <span data-ttu-id="a9a0a-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="a9a0a-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="a9a0a-602">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-602">no</span></span>             | <span data-ttu-id="a9a0a-603">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-603">no</span></span>           |
| <span data-ttu-id="a9a0a-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="a9a0a-604">msdyn_progress</span></span>                         | <span data-ttu-id="a9a0a-605">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-605">no</span></span>             | <span data-ttu-id="a9a0a-606">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-606">no</span></span>           |
| <span data-ttu-id="a9a0a-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="a9a0a-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="a9a0a-608">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-608">no</span></span>             | <span data-ttu-id="a9a0a-609">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-609">no</span></span>           |
| <span data-ttu-id="a9a0a-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="a9a0a-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="a9a0a-611">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-611">no</span></span>             | <span data-ttu-id="a9a0a-612">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-612">no</span></span>           |
| <span data-ttu-id="a9a0a-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="a9a0a-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="a9a0a-614">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-614">no</span></span>             | <span data-ttu-id="a9a0a-615">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-615">no</span></span>           |
| <span data-ttu-id="a9a0a-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="a9a0a-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="a9a0a-617">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-617">no</span></span>             | <span data-ttu-id="a9a0a-618">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-618">no</span></span>           |
| <span data-ttu-id="a9a0a-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="a9a0a-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="a9a0a-620">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-620">no</span></span>             | <span data-ttu-id="a9a0a-621">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-621">no</span></span>           |
| <span data-ttu-id="a9a0a-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="a9a0a-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="a9a0a-623">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-623">no</span></span>             | <span data-ttu-id="a9a0a-624">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-624">no</span></span>           |
| <span data-ttu-id="a9a0a-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="a9a0a-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="a9a0a-626">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-626">no</span></span>             | <span data-ttu-id="a9a0a-627">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-627">no</span></span>           |
| <span data-ttu-id="a9a0a-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="a9a0a-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="a9a0a-629">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-629">no</span></span>             | <span data-ttu-id="a9a0a-630">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-630">no</span></span>           |
| <span data-ttu-id="a9a0a-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="a9a0a-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="a9a0a-632">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-632">no</span></span>             | <span data-ttu-id="a9a0a-633">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-633">no</span></span>           |
| <span data-ttu-id="a9a0a-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="a9a0a-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="a9a0a-635">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-635">no</span></span>             | <span data-ttu-id="a9a0a-636">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-636">no</span></span>           |
| <span data-ttu-id="a9a0a-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="a9a0a-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="a9a0a-638">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-638">no</span></span>             | <span data-ttu-id="a9a0a-639">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-639">no</span></span>           |
| <span data-ttu-id="a9a0a-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="a9a0a-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="a9a0a-641">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-641">no</span></span>             | <span data-ttu-id="a9a0a-642">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-642">no</span></span>           |
| <span data-ttu-id="a9a0a-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="a9a0a-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="a9a0a-644">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-644">no</span></span>             | <span data-ttu-id="a9a0a-645">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-645">no</span></span>           |
| <span data-ttu-id="a9a0a-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="a9a0a-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="a9a0a-647">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-647">no</span></span>             | <span data-ttu-id="a9a0a-648">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-648">no</span></span>           |
| <span data-ttu-id="a9a0a-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="a9a0a-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="a9a0a-650">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-650">no</span></span>             | <span data-ttu-id="a9a0a-651">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-651">no</span></span>           |
| <span data-ttu-id="a9a0a-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="a9a0a-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="a9a0a-653">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-653">no</span></span>             | <span data-ttu-id="a9a0a-654">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-654">no</span></span>           |
| <span data-ttu-id="a9a0a-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="a9a0a-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="a9a0a-656">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-656">no</span></span>             | <span data-ttu-id="a9a0a-657">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-657">no</span></span>           |
| <span data-ttu-id="a9a0a-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="a9a0a-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="a9a0a-659">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-659">no</span></span>             | <span data-ttu-id="a9a0a-660">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-660">no</span></span>           |
| <span data-ttu-id="a9a0a-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="a9a0a-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="a9a0a-662">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-662">no</span></span>             | <span data-ttu-id="a9a0a-663">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-663">no</span></span>           |
| <span data-ttu-id="a9a0a-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="a9a0a-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="a9a0a-665">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-665">no</span></span>             | <span data-ttu-id="a9a0a-666">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-666">no</span></span>           |
| <span data-ttu-id="a9a0a-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="a9a0a-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="a9a0a-668">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-668">no</span></span>             | <span data-ttu-id="a9a0a-669">não</span><span class="sxs-lookup"><span data-stu-id="a9a0a-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="a9a0a-670">Limitações e problemas conhecidos</span><span class="sxs-lookup"><span data-stu-id="a9a0a-670">Limitations and known issues</span></span>
<span data-ttu-id="a9a0a-671">Esta é uma lista de limitações e problemas conhecidos:</span><span class="sxs-lookup"><span data-stu-id="a9a0a-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="a9a0a-672">APIs de programação só podem ser usadas por **Usuários com licença do Microsoft Project**.</span><span class="sxs-lookup"><span data-stu-id="a9a0a-672">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="a9a0a-673">Elas não podem ser usadas por:</span><span class="sxs-lookup"><span data-stu-id="a9a0a-673">They can't be used by:</span></span>
    - <span data-ttu-id="a9a0a-674">Usuários do aplicativo</span><span class="sxs-lookup"><span data-stu-id="a9a0a-674">Application users</span></span>
    - <span data-ttu-id="a9a0a-675">Usuários do sistema</span><span class="sxs-lookup"><span data-stu-id="a9a0a-675">System users</span></span>
    - <span data-ttu-id="a9a0a-676">Usuários de Integração</span><span class="sxs-lookup"><span data-stu-id="a9a0a-676">Integration users</span></span>
    - <span data-ttu-id="a9a0a-677">Outros usuários sem a licença necessária</span><span class="sxs-lookup"><span data-stu-id="a9a0a-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="a9a0a-678">Cada **OperationSet** pode ter no máximo 100 operações.</span><span class="sxs-lookup"><span data-stu-id="a9a0a-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="a9a0a-679">Cada usuário pode ter no máximo 10 **OperationSets** abertos.</span><span class="sxs-lookup"><span data-stu-id="a9a0a-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="a9a0a-680">No momento, o Project Operations dá suporte no máximo a 500 tarefas em um projeto.</span><span class="sxs-lookup"><span data-stu-id="a9a0a-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="a9a0a-681">O status de falha e logs de falha do **OperationSet** não estão disponíveis no momento.</span><span class="sxs-lookup"><span data-stu-id="a9a0a-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- <span data-ttu-id="a9a0a-682">APIs de programação estão na versão preliminar pública.</span><span class="sxs-lookup"><span data-stu-id="a9a0a-682">Schedule APIs are in Public preview.</span></span> <span data-ttu-id="a9a0a-683">O uso dessas APIs em um ambiente de produção não é compatível com a Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a9a0a-683">Using these APIs in a Production environment isn't supported by Microsoft.</span></span>
- [<span data-ttu-id="a9a0a-684">Limites em projetos e tarefas</span><span class="sxs-lookup"><span data-stu-id="a9a0a-684">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="a9a0a-685">Tratamento de erros</span><span class="sxs-lookup"><span data-stu-id="a9a0a-685">Error handling</span></span>

   - <span data-ttu-id="a9a0a-686">Para revisar erros gerados a partir dos Conjuntos de Operações, acesse **Configurações** \> **Integração de Agenda** \> **Conjuntos de Operações**.</span><span class="sxs-lookup"><span data-stu-id="a9a0a-686">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="a9a0a-687">Para revisar erros gerados a partir do Serviço de Agendamento de Projetos, acesse **Configurações** \> **Integração de Agenda** \> **Logs de Erros PSS**.</span><span class="sxs-lookup"><span data-stu-id="a9a0a-687">To review errors generated from the Project Scheduling Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="a9a0a-688">Cenário de exemplo</span><span class="sxs-lookup"><span data-stu-id="a9a0a-688">Sample scenario</span></span>

<span data-ttu-id="a9a0a-689">Neste cenário, você criará um projeto, um membro da equipe, quatro tarefas e duas atribuições de recursos.</span><span class="sxs-lookup"><span data-stu-id="a9a0a-689">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="a9a0a-690">Em seguida, você atualizará uma tarefa, atualizará o projeto, excluirá uma tarefa, excluirá uma atribuição de recurso e criará uma dependência de tarefa.</span><span class="sxs-lookup"><span data-stu-id="a9a0a-690">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

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

## <a name="additional-samples"></a><span data-ttu-id="a9a0a-691">Exemplos adicionais</span><span class="sxs-lookup"><span data-stu-id="a9a0a-691">Additional samples</span></span>

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
