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
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Use APIs de programação para realizar operações com entidades de agendamento

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_

> [!IMPORTANT] 
> Parte de ou toda a funcionalidade observada neste tópico está disponível como parte de uma versão preliminar. O conteúdo e a funcionalidade estão sujeitos a alterações. 

## <a name="scheduling-entities"></a>Entidades de agendamento

As APIs de programação fornecem a capacidade de executar operações de criação, atualização e exclusão com **Entidades de agendamento**. Essas entidades são gerenciadas por meio do mecanismo de agendamento no projeto para a Web. Criar, atualizar e excluir operações com **Entidades de agendamento** foram restritos em versões anteriores do Dynamics 365 Project Operations.

A tabela a seguir fornece uma lista completa das **Entidades de agendamento**.

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

## <a name="schedule-apis"></a>APIs de programação

A seguir está uma lista de APIs de programação atuais.

- **msdyn_CreateProjectV1**: Esta API pode ser usada para criar um projeto. O projeto e o bucket de projeto padrão são criados imediatamente.
- **msdyn_CreateTeamMemberV1**: Esta API pode ser usada para criar um membro da equipe do projeto. O registro do membro da equipe é criado imediatamente.
- **msdyn_CreateOperationSetV1**: Esta API pode ser usada para agendar várias solicitações que devem ser executadas em uma transação.
- **msdyn_PSSCreateV1**: Esta API pode ser usada para criar uma entidade. A entidade pode ser qualquer uma das entidades de agendamento que dão suporte à operação de criação.
- **msdyn_PSSUpdateV1**: Esta API pode ser usada para atualizar uma entidade. A entidade pode ser qualquer uma das entidades de agendamento que dão suporte à operação de atualização.
- **msdyn_PSSDeleteV1**: Esta API pode ser usada para excluir uma entidade. A entidade pode ser uma das entidades de agendamento com suporte à operação de exclusão.
- **msdyn_ExecuteOperationSetV1**: Esta API é usada para executar todas as operações no conjunto de operações especificado.

## <a name="using-schedule-apis-with-operationset"></a>Usar APIs de programação com OperationSet

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

## <a name="limitations-and-known-issues"></a>Limitações e problemas conhecidos
Esta é uma lista de limitações e problemas conhecidos:

- APIs de programação só podem ser usadas por **Usuários com licença do Microsoft Project**. Elas não podem ser usadas por:
    - Usuários do aplicativo
    - Usuários do sistema
    - Usuários de Integração
    - Outros usuários sem a licença necessária
- Cada **OperationSet** pode ter no máximo 100 operações.
- Cada usuário pode ter no máximo 10 **OperationSets** abertos.
- No momento, o Project Operations dá suporte no máximo a 500 tarefas em um projeto.
- O status de falha e logs de falha do **OperationSet** não estão disponíveis no momento.
- APIs de programação estão na versão preliminar pública. O uso dessas APIs em um ambiente de produção não é compatível com a Microsoft.

## <a name="sample-scenario"></a>Cenário de exemplo

Neste cenário, você criará um projeto, um membro da equipe, quatro tarefas e duas atribuições de recursos. Em seguida, você atualizará uma tarefa, atualizará o projeto, excluirá uma tarefa, excluirá uma atribuição de recurso e criará uma dependência de tarefa.

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

## <a name="additional-samples"></a>Exemplos adicionais

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
