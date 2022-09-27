---
title: Использование API расписания проекта для выполнения операций с сущностями планирования
description: В этой статье представлены сведения и примеры использования API-интерфейсов расписания проекта.
author: sigitac
ms.date: 01/13/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 159d395efff98f2af780e5ed1e5ab3d6483cba89
ms.sourcegitcommit: b1c26ea57be721c5b0b1a33f2de0380ad102648f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/20/2022
ms.locfileid: "9541141"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Использование API расписания проекта для выполнения операций с сущностями планирования

_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_


**Сущности планирования**

API расписания проекта предоставляют возможность выполнять операции создания, обновления и удаления с помощью **сущностей планирования**. Управление этими сущностями осуществляется через механизм планирования в проекте для Интернета. Операции создания, обновления и удаления с помощью **сущностей планирования** были ограничены в ранних выпусках Dynamics 365 Project Operations.

В следующей таблице представлен полный список сущностей расписания проекта.

| **имя сущности,**         | **Логическое имя сущности**     |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Задача проекта            | msdyn_projecttask           |
| Зависимость задач проекта | msdyn_projecttaskdependency |
| Назначение ресурса     | msdyn_resourceassignment    |
| Группа проекта          | msdyn_projectbucket         |
| Участник проектной группы     | msdyn_projectteam           |
| Контрольные списки проекта      | msdyn_projectchecklist      |
| Метка проекта           | msdyn_projectlabel          |
| Задача проекта для пометки   | msdyn_projecttasktolabel    |
| Спринт проекта          | msdyn_projectsprint         |

**OperationSet**

OperationSet — это шаблон единицы работы, который можно использовать, когда в рамках транзакции необходимо обработать несколько запросов, влияющих на расписание.

**API расписания проектов**

Ниже приводится список текущих API для расписания проекта.

| **API**                                 | Description                                                                                                                       |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| **msdyn_CreateProjectV1**               | Этот API используется для создания проекта. Проект и группа проекта по умолчанию создаются немедленно.                         |
| **msdyn_CreateTeamMemberV1**            | Этот API используется для создания участника рабочей группы проекта. Запись участника рабочей группы создается немедленно.                                  |
| **msdyn_CreateOperationSetV1**          | Этот API используется для планирования нескольких запросов, которые должны выполняться в рамках транзакции.                                        |
| **msdyn_PssCreateV1**                   | Этот API используется для создания сущности. Сущность может быть любой из сущностей планирования проекта, поддерживающих операцию создания. |
| **msdyn_PssUpdateV1**                   | Этот API используется для обновления сущности. Сущность может быть любой из сущностей планирования проекта, поддерживающих операцию обновления  |
| **msdyn_PssDeleteV1**                   | Этот API используется для удаления сущности. Сущность может быть любой из сущностей планирования проекта, поддерживающих операцию удаления. |
| **msdyn_ExecuteOperationSetV1**         | Этот API используется для выполнения всех операций в рамках данного набора операций.                                                 |
| **msdyn_PssUpdateResourceAssignmentV1** | Этот API используется для обновления запланированного рабочего контура назначения ресурсов.                                                        |



**Использование API расписания проекта с OperationSet**

Поскольку записи **CreateProjectV1** и **CreateTeamMemberV1** создаются мгновенно, эти API нельзя использовать в **OperationSet** напрямую. Однако вы можете использовать API для создания необходимых записей, создайте **OperationSet**, а затем используйте эти предварительно созданные записи в **OperationSet**.

**Поддерживаемые операции**

| **Сущность планирования**   | **Создание** | **Update** | **DELETE** | **Важные замечания**                                                                                                                                                                                                                                                                                                                            |
|-------------------------|------------|------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Задача проекта            | Да        | Да        | Да        | Поля **Progress**, **EffortCompleted** и **EffortRemaining** можно редактировать в Project for the Web, но нельзя редактировать в Project Operations.                                                                                                                                                                                             |
| Зависимость задач проекта | Да        | No         | Да        | Записи о зависимостях задач проекта не обновляются. Вместо этого можно удалить старую запись и создать новую.                                                                                                                                                                                                                                 |
| Назначение ресурса     | Да        | Да\*      | Да        | Не поддерживаются операции со следующими полями: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** и **PlannedWork**. Записи о назначении ресурсов не обновляются. Вместо этого можно удалить старую запись и создать новую. Для обновления контуров назначения ресурсов был предоставлен отдельный API. |
| Группа проекта          | Да        | Да        | Да        | Группа по умолчанию создается с помощью API **CreateProjectV1**. Поддержка создания и удаления групп проекта была добавлена в выпуске-обновлении 16.                                                                                                                                                                                                   |
| Участник проектной группы     | Да        | Да        | Да        | Для операции создания используйте API **CreateTeamMemberV1**.                                                                                                                                                                                                                                                                                           |
| Project                 | Да        | Да        |            | Не поддерживаются операции со следующими полями: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** и **Duration**.                                                                                       |
| Контрольные списки проекта      | Да        | Да        | Да        |                                                                                                                                                                                                                                                                                                                                                         |
| Метка проекта           | No         | Да        | No         | Названия ярлыков можно изменить. Эта функция доступна только для Project for the Web                                                                                                                                                                                                                                                                      |
| Задача проекта для пометки   | Да        | No         | Да        | Эта функция доступна только для Project for the Web                                                                                                                                                                                                                                                                                                  |
| Спринт проекта          | Да        | Да        | Да        | Поле **Начало** должно иметь более раннюю дату, чем поле **Конец**. Спринты одного и того же проекта не могут пересекаться друг с другом. Эта функция доступна только для Project for the Web                                                                                                                                                                    |




Свойство кода необязательно. Если оно указано, система пытается его использовать и выдает исключение, если оно не может быть использовано. Если оно не указано, система его сгенерирует.

**Известные проблемы и ограничения**

Ниже приводится список ограничений и известных проблем:

-   API расписания проекта могут использоваться только **пользователями с лицензией Microsoft Project.** Их не могут использовать:
    -   Пользователи приложений
    -   Системные пользователи
    -   Пользователи-интеграторы
    -   Другие пользователи, у которых нет необходимой лицензии
-   У каждого **OperationSet** может быть не более 100 операций.
-   У каждого пользователя может быть не более 10 открытых **OperationSet**.
-   В настоящее время Project Operations поддерживает не более 500 общих задач в проекте.
-   Каждая операция обновления контура назначения ресурсов считается одной операцией.
-   Каждый список обновленных контуров может содержать не более 100 временных интервалов.
-   Статус сбоя и журналы ошибок в **OperationSet** в настоящее время недоступны.
-   Предусмотрено максимум 400 спринтов на проект.
-   [Пределы и границы проектов и задач](/project-for-the-web/project-for-the-web-limits-and-boundaries).
-   Метки в настоящее время доступны только для Project for the Web.

**Обработка ошибок**

-   Чтобы просмотреть ошибки, сгенерированные из наборов операций, перейдите к **Параметры** \> **Интеграция расписания** \> **Наборы операций**.
-   Чтобы просмотреть ошибки, сгенерированные службой расписания проекта, перейдите в раздел **Настройки** \> **Интеграция расписаний** \> **Журналы ошибок PSS**.

**Редактирование контуров назначения ресурсов**

В отличие от всех других API-интерфейсов планирования проектов, которые обновляют сущность, API-интерфейс контура назначения ресурсов несет единоличную ответственность за обновления одного поля, msdyn_plannedwork, в одной сущности, msydn_resourceassignment.

Данный режим расписания:

-   **фиксированные единицы**
-   календарь проекта: 9-5p, то есть 09:00-17:00 по тихоокеанскому времени, пн, вт, чт, пятница (НЕ РАБОТАЕТ ПО СРЕДАМ)
-   и календарь ресурсов: 09:00–13:00 по тихоокеанскому времени с понедельника по пятницу

Это назначение рассчитано на одну неделю, четыре часа в день. Это связано с тем, что календарь ресурса начинается с 09:00 по 13:00 по тихоокеанскому времени или четыре часа в день.

| &nbsp;     | Задача | Дата начала | Дата окончания  | Количество | 13.06.2022 | 14.06.2022 | 15.06.2022 | 16.06.2022 | 17.06.2022 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| 09-13 Рабочий |  T1  | 13.06.2022  | 17.06.2022 | 20       | 4         | 4         | 4         | 4         | 4         |

Например, если вы хотите, чтобы рабочий работал только три часа каждый день на этой неделе и оставить один час на другие задачи.

#### <a name="updatedcontours-sample-payload"></a>Пример полезных данных UpdatedContours:

```json
[{

"minutes":900.0,

"start":"2022-06-13T00:00:00-07:00",

"end":"2022-06-18T00:00:00-07:00"

}]
```

Это назначение выполняется после запуска API-интерфейса обновления контура планирования.

| &nbsp;     | Задача | Дата начала | Дата окончания  | Количество | 13.06.2022 | 14.06.2022 | 15.06.2022 | 16.06.2022 | 17.06.2022 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| 09-13 Рабочий | T1   | 13.06.2022  | 17.06.2022 | 15       | 3         | 3         | 3         | 3         | 3         |


**Пример сценария**

В этом сценарии вы создадите проект, участника команды, четыре задачи и два назначения ресурсов. Затем вы обновите одну задачу, обновите проект, удалите одну задачу, удалите одно назначение ресурса и создадите зависимость задачи.

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

** Дополнительные примеры

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
