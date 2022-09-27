---
title: Use APIs de agendamento do Project para realizar operações com entidades de Agendamento
description: Este artigo fornece informações e exemplos para usar APIs de agendamento do projeto.
author: sigitac
ms.date: 01/13/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 159d395efff98f2af780e5ed1e5ab3d6483cba89
ms.sourcegitcommit: b1c26ea57be721c5b0b1a33f2de0380ad102648f
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/20/2022
ms.locfileid: "9541110"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Use APIs de agendamento do Project para realizar operações com entidades de Agendamento

_**Aplica-se a:** operações de projeto para cenários baseados em recursos/não estocados, implantação Lite - transação para faturamento pro forma_


**Entidades de agendamento**

APIs de agendamento do Project fornecem a capacidade de executar operações de criação, atualização e exclusão com **Entidades de agendamento**. Essas entidades são gerenciadas por meio do mecanismo de agendamento no projeto para a Web. Criar, atualizar e excluir operações com **Entidades de agendamento** foram restritos em versões anteriores do Dynamics 365 Project Operations.

A tabela a seguir fornece uma lista completa das entidades de agendamento do Project.

| **Nome da entidade**         | **Nome lógico da entidade**     |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Tarefa do Projeto            | msdyn_projecttask           |
| Dependência de Tarefa do Projeto | msdyn_projecttaskdependency |
| Atribuição de Recurso     | msdyn_resourceassignment    |
| Bucket do Projeto          | msdyn_projectbucket         |
| Membro da Equipe do Projeto     | msdyn_projectteam           |
| Listas de Verificação do Projeto      | msdyn_projectchecklist      |
| Rótulo do Projeto           | msdyn_projectlabel          |
| Tarefa do Projeto para o Rótulo   | msdyn_projecttasktolabel    |
| Sprint do Projeto          | msdyn_projectsprint         |

**OperationSet**

OperationSet é um padrão de unidade de trabalho que pode ser usado quando várias solicitações de impacto de agenda devem ser processadas em uma transação.

**APIs de agendamento do Project**

A seguir está uma lista de APIs atuais de agendamento do Project.

| **API**                                 | Description                                                                                                                       |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| **msdyn_CreateProjectV1**               | Essa API é usada para criar um projeto. O projeto e o bucket de projeto padrão são criados imediatamente.                         |
| **msdyn_CreateTeamMemberV1**            | Essa API é usada para criar um membro da equipe do projeto. O registro do membro da equipe é criado imediatamente.                                  |
| **msdyn_CreateOperationSetV1**          | Essa API é usada para agendar várias solicitações que devem ser executadas em uma transação.                                        |
| **msdyn_PssCreateV1**                   | Essa API é usada para criar uma entidade. A entidade pode ser qualquer uma das entidades de agendamento do Project que oferecem suporte à operação de criação. |
| **msdyn_PssUpdateV1**                   | Essa API é usada para atualizar uma entidade. A entidade pode ser qualquer uma das entidades de agendamento do Project que ofereçam suporte à operação de atualização  |
| **msdyn_PssDeleteV1**                   | Essa API é usada para excluir uma entidade. A entidade pode ser qualquer uma das entidades de agendamento do Project que oferecem suporte à operação de exclusão. |
| **msdyn_ExecuteOperationSetV1**         | Essa API é usada para executar todas as operações no conjunto de operações especificado.                                                 |
| **msdyn_PssUpdateResourceAssignmentV1** | Essa API é usada para atualizar um contorno de trabalho planejado de Atribuição de Recurso.                                                        |



**Usando APIs de agendamento do Project com OperationSet**

Como registros com **CreateProjectV1** e **CreateTeamMemberV1** são criados imediatamente, essas APIs não podem ser usadas diretamente no **OperationSet**. No entanto, você pode usar a API para criar os registros necessários, criar um **OperationSet** e usar esses registros pré-criados no **OperationSet**.

**Operações com suporte**

| **Entidade de agendamento**   | **Criar** | **Atualização** | **Delete** | **Considerações importantes**                                                                                                                                                                                                                                                                                                                            |
|-------------------------|------------|------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tarefa do projeto            | Sim        | Sim        | Sim        | É possível editar os campos **Progress**, **EffortCompleted** e **EffortRemaining** no Project for the Web, mas não no Project Operations.                                                                                                                                                                                             |
| Dependência de tarefa do projeto | Sim        | No         | Sim        | Os registros de dependência da tarefa do projeto não são atualizados. Em vez disso, é possível excluir um registro antigo e criar um novo registro.                                                                                                                                                                                                                                 |
| Atribuição de recurso     | Sim        | Sim\*      | Sim        | Não há suporte a operações com os seguintes campos: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** e **PlannedWork**. Os registros de atribuição de recursos não são atualizados. Em vez disso, é possível excluir o registro antigo e criar um novo registro. Uma API separada foi fornecida para atualizar os contornos da Atribuição de Recurso. |
| Bucket do projeto          | Sim        | Sim        | Sim        | O bucket padrão é criado usando a API **CreateProjectV1**. O suporte para a criação e exclusão de buckets de projeto foi adicionado na Versão de atualização 16.                                                                                                                                                                                                   |
| Membro da equipe do projeto     | Sim        | Sim        | Sim        | Para a operação de criação, use a API **CreateTeamMemberV1**.                                                                                                                                                                                                                                                                                           |
| Project                 | Sim        | Sim        |            | Não há suporte para operações com os seguintes campos: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** e **Duration**.                                                                                       |
| Listas de Verificação do Projeto      | Sim        | Sim        | Sim        |                                                                                                                                                                                                                                                                                                                                                         |
| Rótulo do Projeto           | No         | Sim        | No         | Os nomes dos rótulos podem ser alterados. Esse recurso está disponível somente para o Project for the Web                                                                                                                                                                                                                                                                      |
| Tarefa do Projeto para o Rótulo   | Sim        | No         | Sim        | Esse recurso está disponível somente para o Project for the Web                                                                                                                                                                                                                                                                                                  |
| Sprint do Projeto          | Sim        | Sim        | Sim        | O campo **Iniciar** deve ter uma data anterior ao campo **Concluir**. Os sprints para o mesmo projeto não podem se sobrepor. Esse recurso está disponível somente para o Project for the Web                                                                                                                                                                    |




A propriedade da ID é opcional. Se ela for fornecida, o sistema tentará usá-la e lançará uma exceção se ela não puder ser usada. Se ela não for fornecida, o sistema irá gerá-la.

**Limitações e problemas conhecidos**

Esta é uma lista de limitações e problemas conhecidos:

-   As APIs de agendamento de projetos podem ser usadas somente por **Usuários com Licença do Microsoft Project**. Elas não podem ser usadas por:
    -   Usuários do aplicativo
    -   Usuários do sistema
    -   Usuários de Integração
    -   Outros usuários sem a licença necessária
-   Cada **OperationSet** pode ter no máximo 100 operações.
-   Cada usuário pode ter no máximo 10 **OperationSets** abertos.
-   No momento, o Project Operations dá suporte no máximo a 500 tarefas em um projeto.
-   Cada operação Atualizar o Contorno da Atribuição de Recurso conta como uma única operação.
-   Cada lista de contornos atualizados pode conter no máximo 100 frações de tempo.
-   O status de falha e logs de falha do **OperationSet** não estão disponíveis no momento.
-   Há um máximo de 400 sprints por projeto.
-   [Limites em projetos e tarefas](/project-for-the-web/project-for-the-web-limits-and-boundaries).
-   No momento, os rótulos estão disponíveis somente para o Project for the Web.

**Tratamento de erros**

-   Para revisar erros gerados a partir dos Conjuntos de Operações, acesse **Configurações** \> **Integração de Agenda** \> **Conjuntos de Operações**.
-   Para revisar os erros gerados a partir do serviço de agendamento do Project, vá para **Definições** \> **Integração de agendamento** \> **Logs de Erros do PSS**.

**Editando Contornos da Atribuição de Recurso**

Diferentemente de todas as outras APIs de agendamento de projeto que atualizam uma entidade, a API de contorno de atribuição de recurso é a única responsável por atualizações em um único campo, msdyn_plannedwork, em uma única entidade, msydn_resourceassignment.

O modo de agendamento fornecido é:

-   **unidades fixas**
-   o calendário do projeto é 9-5p é 9-5pst, seg, ter, qui, sexta (SEM TRABALHO ÀS QUARTAS)
-   e o calendário de recursos é 9-1p PST de segunda a sexta

Esta tarefa é para uma semana, quatro horas por dia. Isso ocorre porque o calendário de recursos é das 9 a 1 PST, ou quatro horas por dia.

| &nbsp;     | Tarefa | Data de Início | Data de Término  | Quantidade | 13/06/2022 | 14/06/2022 | 15/06/2022 | 16/06/2022 | 17/06/2022 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| Trabalhador 9 a 1 |  T1  | 13/06/2022  | 17/06/2022 | 20       | 4         | 4         | 4         | 4         | 4         |

Por exemplo, se você quiser que o trabalhador trabalhe somente três horas por dia nesta semana e permitir uma hora para outras tarefas.

#### <a name="updatedcontours-sample-payload"></a>Conteúdo de exemplo de UpdatedContours:

```json
[{

"minutes":900.0,

"start":"2022-06-13T00:00:00-07:00",

"end":"2022-06-18T00:00:00-07:00"

}]
```

Esta é a atribuição após a execução da API Atualizar Agenda de Contorno.

| &nbsp;     | Tarefa | Data de Início | Data de Término  | Quantidade | 13/06/2022 | 14/06/2022 | 15/06/2022 | 16/06/2022 | 17/06/2022 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| Trabalhador 9 a 1 | T1   | 13/06/2022  | 17/06/2022 | 15       | 3         | 3         | 3         | 3         | 3         |


**Cenário de exemplo**

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

** Exemplos adicionais

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
