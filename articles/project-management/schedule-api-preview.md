---
title: Use APIs de agendamento do Project para realizar operações com entidades de Agendamento
description: Este tópico fornece informações e exemplos para o uso de APIs de agendamento do Project.
author: sigitac
ms.date: 09/09/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6be35b1c52996f4f94dc429974ef47343a027c8c
ms.sourcegitcommit: bbe484e58a77efe77d28b34709fb6661d5da00f9
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2021
ms.locfileid: "7487671"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Use APIs de agendamento do Project para realizar operações com entidades de Agendamento

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_



## <a name="scheduling-entities"></a>Entidades de agendamento

APIs de agendamento do Project fornecem a capacidade de executar operações de criação, atualização e exclusão com **Entidades de agendamento**. Essas entidades são gerenciadas por meio do mecanismo de agendamento no projeto para a Web. Criar, atualizar e excluir operações com **Entidades de agendamento** foram restritos em versões anteriores do Dynamics 365 Project Operations.

A tabela a seguir fornece uma lista completa das entidades de agendamento do Project.

| Nome da entidade  | Nome lógico da entidade |
| --- | --- |
| Project | msdyn_project |
| Tarefa do Projeto  | msdyn_projecttask  |
| Dependência de Tarefa do Projeto  | msdyn_projecttaskdependency  |
| Atribuição de Recurso | msdyn_resourceassignment |
| Bucket do Projeto  | msdyn_projectbucket |
| Membro da Equipe do Projeto | msdyn_projectteam |

## <a name="operationset"></a>OperationSet

OperationSet é um padrão de unidade de trabalho que pode ser usado quando várias solicitações de impacto de agenda devem ser processadas em uma transação.

## <a name="project-schedule-apis"></a>APIs de agendamento do Project

A seguir está uma lista de APIs atuais de agendamento do Project.

- **msdyn_CreateProjectV1**: Esta API pode ser usada para criar um projeto. O projeto e o bucket de projeto padrão são criados imediatamente.
- **msdyn_CreateTeamMemberV1**: Esta API pode ser usada para criar um membro da equipe do projeto. O registro do membro da equipe é criado imediatamente.
- **msdyn_CreateOperationSetV1**: Esta API pode ser usada para agendar várias solicitações que devem ser executadas em uma transação.
- **msdyn_PSSCreateV1**: Esta API pode ser usada para criar uma entidade. A entidade pode ser qualquer uma das entidades de agendamento do Project que oferecem suporte à operação de criação.
- **msdyn_PSSUpdateV1**: Esta API pode ser usada para atualizar uma entidade. A entidade pode ser qualquer uma das entidades de agendamento do Project que oferecem suporte à operação de atualização.
- **msdyn_PSSDeleteV1**: Esta API pode ser usada para excluir uma entidade. A entidade pode ser qualquer uma das entidades de agendamento do Project que oferecem suporte à operação de exclusão.
- **msdyn_ExecuteOperationSetV1**: Esta API é usada para executar todas as operações no conjunto de operações especificado.

## <a name="using-project-schedule-apis-with-operationset"></a>Usando APIs de agendamento do Project com OperationSet

Como registros com **CreateProjectV1** e **CreateTeamMemberV1** são criados imediatamente, essas APIs não podem ser usadas diretamente no **OperationSet**. No entanto, você pode usar a API para criar os registros necessários, criar um **OperationSet** e usar esses registros pré-criados no **OperationSet**.

## <a name="supported-operations"></a>Operações com suporte

| Entidade de agendamento | Criar | Atualizar | Excluir | Considerações importantes |
| --- | --- | --- | --- | --- |
Tarefa do projeto | Sim | Sim | Sim | Nenhum(a) |
| Dependência de tarefa do projeto | Sim | Sim | | Os registros de dependência da tarefa do projeto não são atualizados. Em vez disso, um registro antigo pode ser excluído e um novo registro pode ser criado. |
| Atribuição de recurso | Sim | Sim | | Não há suporte a operações com os seguintes campos: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** e **PlannedWork**. Os registros de atribuição de recursos não são atualizados. Em vez disso, o registro antigo pode ser excluído e um novo registro pode ser criado. |
| Bucket do projeto | N/D | N/D | N/D | O intervalo padrão é criado usando a API **CreateProjectV1**. |
| Membro da equipe do projeto | Sim | Sim | Sim | Para a operação de criação, use a API **CreateTeamMemberV1**. |
| Project | Sim | Sim | N/D | Não há suporte para operações com os seguintes campos: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** e **Duration**. |

Essas APIs podem ser chamadas com objetos de entidade que incluem campos personalizados.

A propriedade da ID é opcional. Se ela for fornecida, o sistema tentará usá-la e lançará uma exceção se ela não puder ser usada. Se ela não for fornecida, o sistema irá gerá-la.

## <a name="restricted-fields"></a>Campos restritos

As tabelas a seguir definem os campos que são restritos de **Criar** e **Editar**.

### <a name="project-task"></a>Tarefa do projeto

| **Nome lógico**                       | **Pode criar** | **Pode editar**     |
|----------------------------------------|----------------|------------------|
| msdyn_actualcost                       | não             | não               |
| msdyn_actualcost_base                  | não             | não               |
| msdyn_actualend                        | não             | não               |
| msdyn_actualsales                      | não             | não               |
| msdyn_actualsales_base                 | não             | não               |
| msdyn_actualstart                      | não             | não               |
| msdyn_costatcompleteestimate           | não             | não               |
| msdyn_costatcompleteestimate_base      | não             | não               |
| msdyn_costconsumptionpercentage        | não             | não               |
| msdyn_effortcompleted                  | não             | não               |
| msdyn_effortestimateatcomplete         | não             | não               |
| msdyn_iscritical                       | não             | não               |
| msdyn_iscriticalname                   | não             | não               |
| msdyn_ismanual                         | não             | não               |
| msdyn_ismanualname                     | não             | não               |
| msdyn_ismilestone                      | não             | não               |
| msdyn_ismilestonename                  | não             | não               |
| msdyn_LinkStatus                       | não             | não               |
| msdyn_linkstatusname                   | não             | não               |
| msdyn_msprojectclientid                | não             | não               |
| msdyn_plannedcost                      | não             | não               |
| msdyn_plannedcost_base                 | não             | não               |
| msdyn_plannedsales                     | não             | não               |
| msdyn_plannedsales_base                | não             | não               |
| msdyn_pluginprocessingdata             | não             | não               |
| msdyn_progress                         | não             | não (sim para P4W) |
| msdyn_remainingcost                    | não             | não               |
| msdyn_remainingcost_base               | não             | não               |
| msdyn_remainingsales                   | não             | não               |
| msdyn_remainingsales_base              | não             | não               |
| msdyn_requestedhours                   | não             | não               |
| msdyn_resourcecategory                 | não             | não               |
| msdyn_resourcecategoryname             | não             | não               |
| msdyn_resourceorganizationalunitid     | não             | não               |
| msdyn_resourceorganizationalunitidname | não             | não               |
| msdyn_salesconsumptionpercentage       | não             | não               |
| msdyn_salesestimateatcomplete          | não             | não               |
| msdyn_salesestimateatcomplete_base     | não             | não               |
| msdyn_salesvariance                    | não             | não               |
| msdyn_salesvariance_base               | não             | não               |
| msdyn_scheduleddurationminutes         | não             | não               |
| msdyn_scheduledend                     | não             | não               |
| msdyn_scheduledstart                   | não             | não               |
| msdyn_schedulevariance                 | não             | não               |
| msdyn_skipupdateestimateline           | não             | não               |
| msdyn_skipupdateestimatelinename       | não             | não               |
| msdyn_summary                          | não             | não               |
| msdyn_varianceofcost                   | não             | não               |
| msdyn_varianceofcost_base              | não             | não               |

### <a name="project-task-dependency"></a>Dependência de tarefa do projeto

| **Nome lógico**              | **Pode criar** | **Pode editar** |
|-------------------------------|----------------|--------------|
| msdyn_linktype                | não             | não           |
| msdyn_linktypename            | não             | não           |
| msdyn_predecessortask         | sim            | não           |
| msdyn_predecessortaskname     | sim            | não           |
| msdyn_project                 | sim            | não           |
| msdyn_projectname             | sim            | não           |
| msdyn_projecttaskdependencyid | sim            | não           |
| msdyn_successortask           | sim            | não           |
| msdyn_successortaskname       | sim            | não           |

### <a name="resource-assignment"></a>Atribuição de recurso

| **Nome lógico**             | **Pode criar** | **Pode editar** |
|------------------------------|----------------|--------------|
| msdyn_bookableresourceid     | sim            | não           |
| msdyn_bookableresourceidname | sim            | não           |
| msdyn_bookingstatusid        | não             | não           |
| msdyn_bookingstatusidname    | não             | não           |
| msdyn_committype             | não             | não           |
| msdyn_committypename         | não             | não           |
| msdyn_effort                 | não             | não           |
| msdyn_effortcompleted        | não             | não           |
| msdyn_effortremaining        | não             | não           |
| msdyn_finish                 | não             | não           |
| msdyn_plannedcost            | não             | não           |
| msdyn_plannedcost_base       | não             | não           |
| msdyn_plannedcostcontour     | não             | não           |
| msdyn_plannedsales           | não             | não           |
| msdyn_plannedsales_base      | não             | não           |
| msdyn_plannedsalescontour    | não             | não           |
| msdyn_plannedwork            | não             | não           |
| msdyn_projectid              | sim            | não           |
| msdyn_projectidname          | não             | não           |
| msdyn_projectteamid          | não             | não           |
| msdyn_projectteamidname      | não             | não           |
| msdyn_start                  | não             | não           |
| msdyn_taskid                 | não             | não           |
| msdyn_taskidname             | não             | não           |
| msdyn_userresourceid         | não             | não           |

### <a name="project-team-member"></a>Membro da equipe do projeto

| **Nome lógico**                                 | **Pode criar** | **Pode editar** |
|--------------------------------------------------|----------------|--------------|
| msdyn_calendarid                                 | não             | não           |
| msdyn_creategenericteammemberwithrequirementname | não             | não           |
| msdyn_deletestatus                               | não             | não           |
| msdyn_deletestatusname                           | não             | não           |
| msdyn_effort                                     | não             | não           |
| msdyn_effortcompleted                            | não             | não           |
| msdyn_effortremaining                            | não             | não           |
| msdyn_finish                                     | não             | não           |
| msdyn_hardbookedhours                            | não             | não           |
| msdyn_hours                                      | não             | não           |
| msdyn_markedfordeletiontimer                     | não             | não           |
| msdyn_markedfordeletiontimestamp                 | não             | não           |
| msdyn_msprojectclientid                          | não             | não           |
| msdyn_percentage                                 | não             | não           |
| msdyn_requiredhours                              | não             | não           |
| msdyn_softbookedhours                            | não             | não           |
| msdyn_start                                      | não             | não           |

### <a name="project"></a>Project

| **Nome lógico**                       | **Pode criar** | **Pode editar** |
|----------------------------------------|----------------|--------------|
| msdyn_actualexpensecost                | não             | não           |
| msdyn_actualexpensecost_base           | não             | não           |
| msdyn_actuallaborcost                  | não             | não           |
| msdyn_actuallaborcost_base             | não             | não           |
| msdyn_actualsales                      | não             | não           |
| msdyn_actualsales_base                 | não             | não           |
| msdyn_contractlineproject              | sim            | não           |
| msdyn_contractorganizationalunitid     | sim            | não           |
| msdyn_contractorganizationalunitidname | sim            | não           |
| msdyn_costconsumption                  | não             | não           |
| msdyn_costestimateatcomplete           | não             | não           |
| msdyn_costestimateatcomplete_base      | não             | não           |
| msdyn_costvariance                     | não             | não           |
| msdyn_costvariance_base                | não             | não           |
| msdyn_duration                         | não             | não           |
| msdyn_effort                           | não             | não           |
| msdyn_effortcompleted                  | não             | não           |
| msdyn_effortestimateatcompleteeac      | não             | não           |
| msdyn_effortremaining                  | não             | não           |
| msdyn_finish                           | sim            | sim          |
| msdyn_globalrevisiontoken              | não             | não           |
| msdyn_islinkedtomsprojectclient        | não             | não           |
| msdyn_islinkedtomsprojectclientname    | não             | não           |
| msdyn_linkeddocumenturl                | não             | não           |
| msdyn_msprojectdocument                | não             | não           |
| msdyn_msprojectdocumentname            | não             | não           |
| msdyn_plannedexpensecost               | não             | não           |
| msdyn_plannedexpensecost_base          | não             | não           |
| msdyn_plannedlaborcost                 | não             | não           |
| msdyn_plannedlaborcost_base            | não             | não           |
| msdyn_plannedsales                     | não             | não           |
| msdyn_plannedsales_base                | não             | não           |
| msdyn_progress                         | não             | não           |
| msdyn_remainingcost                    | não             | não           |
| msdyn_remainingcost_base               | não             | não           |
| msdyn_remainingsales                   | não             | não           |
| msdyn_remainingsales_base              | não             | não           |
| msdyn_replaylogheader                  | não             | não           |
| msdyn_salesconsumption                 | não             | não           |
| msdyn_salesestimateatcompleteeac       | não             | não           |
| msdyn_salesestimateatcompleteeac_base  | não             | não           |
| msdyn_salesvariance                    | não             | não           |
| msdyn_salesvariance_base               | não             | não           |
| msdyn_scheduleperformance              | não             | não           |
| msdyn_scheduleperformancename          | não             | não           |
| msdyn_schedulevariance                 | não             | não           |
| msdyn_taskearlieststart                | não             | não           |
| msdyn_teamsize                         | não             | não           |
| msdyn_teamsize_date                    | não             | não           |
| msdyn_teamsize_state                   | não             | não           |
| msdyn_totalactualcost                  | não             | não           |
| msdyn_totalactualcost_base             | não             | não           |
| msdyn_totalplannedcost                 | não             | não           |
| msdyn_totalplannedcost_base            | não             | não           |


## <a name="limitations-and-known-issues"></a>Limitações e problemas conhecidos
Esta é uma lista de limitações e problemas conhecidos:

- APIs de agendamento do Project só podem ser usadas por **Usuários com Licença do Microsoft Project.** Elas não podem ser usadas por:
    - Usuários do aplicativo
    - Usuários do sistema
    - Usuários de Integração
    - Outros usuários sem a licença necessária
- Cada **OperationSet** pode ter no máximo 100 operações.
- Cada usuário pode ter no máximo 10 **OperationSets** abertos.
- No momento, o Project Operations dá suporte no máximo a 500 tarefas em um projeto.
- O status de falha e logs de falha do **OperationSet** não estão disponíveis no momento.
- [Limites em projetos e tarefas](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a>Tratamento de erros

   - Para revisar erros gerados a partir dos Conjuntos de Operações, acesse **Configurações** \> **Integração de Agenda** \> **Conjuntos de Operações**.
   - Para revisar os erros gerados a partir do serviço de agendamento do Project, vá para **Definições** \> **Integração de agendamento** \> **Logs de Erros do PSS**.

## <a name="sample-scenario"></a>Cenário de exemplo

Neste cenário, você criará um projeto, um membro da equipe, quatro tarefas e duas atribuições de recursos. Em seguida, você atualizará uma tarefa, atualizará o projeto, excluirá uma tarefa, excluirá uma atribuição de recurso e criará uma dependência de tarefa.

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

## <a name="additional-samples"></a>Exemplos adicionais

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
