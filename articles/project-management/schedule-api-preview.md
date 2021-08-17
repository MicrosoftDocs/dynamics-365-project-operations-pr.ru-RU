---
title: Использование API расписания проекта для выполнения операций с сущностями планирования
description: В этом разделе предоставлена информация и примеры по использованию API для расписания проекта.
author: sigitac
ms.date: 06/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 55bd9020275fbb72761b45ba09294f57266b418c0e5b506ba55a2a498aff24e5
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/06/2021
ms.locfileid: "7008782"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Использование API расписания проекта для выполнения операций с сущностями планирования

_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_

> [!IMPORTANT] 
> Некоторые или все функции, описанные в этой статье, доступны в рамках предварительного выпуска. Содержимое и функциональность могут быть изменены. 

## <a name="scheduling-entities"></a>Сущности планирования

API расписания проекта предоставляют возможность выполнять операции создания, обновления и удаления с помощью **сущностей планирования**. Управление этими сущностями осуществляется через механизм планирования в проекте для Интернета. Операции создания, обновления и удаления с помощью **сущностей планирования** были ограничены в ранних выпусках Dynamics 365 Project Operations.

В следующей таблице представлен полный список сущностей расписания проекта.

| Имя сущности  | Логическое имя сущности |
| --- | --- |
| Project | msdyn_project |
| Задача проекта  | msdyn_projecttask  |
| Зависимость задач проекта  | msdyn_projecttaskdependency  |
| Назначение ресурса | msdyn_resourceassignment |
| Группа проекта  | msdyn_projectbucket |
| Участник проектной группы | msdyn_projectteam |

## <a name="operationset"></a>OperationSet

OperationSet — это шаблон единицы работы, который можно использовать, когда в рамках транзакции необходимо обработать несколько запросов, влияющих на расписание.

## <a name="project-schedule-apis"></a>API расписания проектов

Ниже приводится список текущих API для расписания проекта.

- **msdyn_CreateProjectV1**: этот API можно использовать для создания проекта. Немедленно создается проект и группа проекта по умолчанию.
- **msdyn_CreateTeamMemberV1**: этот API можно использовать для создания участника рабочей группы проекта. Запись участника рабочей группы создается немедленно.
- **msdyn_CreateOperationSetV1**: этот API можно использовать для планирования нескольких запросов, которые должны выполняться в рамках транзакции.
- **msdyn_PSSCreateV1**: этот API можно использовать для создания сущности. Сущность может быть любой из сущностей планирования проекта, поддерживающих операцию создания.
- **msdyn_PSSUpdateV1**: этот API можно использовать для обновления сущности. Сущность может быть любой из сущностей планирования проекта, поддерживающих операцию обновления.
- **msdyn_PSSDeleteV1**: этот API можно использовать для удаления сущности. Сущность может быть любой из сущностей планирования проекта, поддерживающих операцию удаления.
- **msdyn_ExecuteOperationSetV1**: этот API используется для выполнения всех операций в рамках данного набора операций.

## <a name="using-project-schedule-apis-with-operationset"></a>Использование API расписания проекта с OperationSet

Поскольку записи **CreateProjectV1** и **CreateTeamMemberV1** создаются мгновенно, эти API нельзя использовать в **OperationSet** напрямую. Однако вы можете использовать API для создания необходимых записей, создайте **OperationSet**, а затем используйте эти предварительно созданные записи в **OperationSet**.

## <a name="supported-operations"></a>Поддерживаемые операции

| Сущность планирования | Создание | При обновлении | DELETE | Важные замечания |
| --- | --- | --- | --- | --- |
Задача проекта | Да | Да | Да | Без доступа |
| Зависимость задач проекта | Да | Да | | Записи о зависимостях задач проекта не обновляются. Вместо этого можно удалить старую запись и создать новую. |
| Назначение ресурса | Да | Да | | Не поддерживаются операции со следующими полями: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** и **PlannedWork**. Записи о назначении ресурсов не обновляются. Вместо этого можно удалить старую запись и создать новую. |
| Группа проекта | Н/Д | Н/Д | Н/Д | Сегмент по умолчанию создается с помощью API **CreateProjectV1**. |
| Участник проектной группы | Да | Да | Да | Для операции создания используйте API **CreateTeamMemberV1**. |
| Project | Да | Да | Н/Д | Не поддерживаются операции со следующими полями: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** и **Duration**. |

Эти API можно вызывать с объектами сущности, которые включают настраиваемые поля.

Свойство кода необязательно. Если оно указано, система пытается его использовать и выдает исключение, если оно не может быть использовано. Если оно не указано, система его сгенерирует.

## <a name="restricted-fields"></a>Запрещенные поля

В следующих таблицах определены поля, которые защищены от **Создать** и **Изменить.**

### <a name="project-task"></a>Задача проекта

| **Логическое имя**                       | **Можно создать** | **Может изменить**     |
|----------------------------------------|----------------|------------------|
| msdyn_actualcost                       | нет             | нет               |
| msdyn_actualcost_base                  | нет             | нет               |
| msdyn_actualend                        | нет             | нет               |
| msdyn_actualsales                      | нет             | нет               |
| msdyn_actualsales_base                 | нет             | нет               |
| msdyn_actualstart                      | нет             | нет               |
| msdyn_costatcompleteestimate           | нет             | нет               |
| msdyn_costatcompleteestimate_base      | нет             | нет               |
| msdyn_costconsumptionpercentage        | нет             | нет               |
| msdyn_effortcompleted                  | нет             | нет               |
| msdyn_effortestimateatcomplete         | нет             | нет               |
| msdyn_iscritical                       | нет             | нет               |
| msdyn_iscriticalname                   | нет             | нет               |
| msdyn_ismanual                         | нет             | нет               |
| msdyn_ismanualname                     | нет             | нет               |
| msdyn_ismilestone                      | нет             | нет               |
| msdyn_ismilestonename                  | нет             | нет               |
| msdyn_LinkStatus                       | нет             | нет               |
| msdyn_linkstatusname                   | нет             | нет               |
| msdyn_msprojectclientid                | нет             | нет               |
| msdyn_plannedcost                      | нет             | нет               |
| msdyn_plannedcost_base                 | нет             | нет               |
| msdyn_plannedsales                     | нет             | нет               |
| msdyn_plannedsales_base                | нет             | нет               |
| msdyn_pluginprocessingdata             | нет             | нет               |
| msdyn_progress                         | нет             | нет (да для P4W) |
| msdyn_remainingcost                    | нет             | нет               |
| msdyn_remainingcost_base               | нет             | нет               |
| msdyn_remainingsales                   | нет             | нет               |
| msdyn_remainingsales_base              | нет             | нет               |
| msdyn_requestedhours                   | нет             | нет               |
| msdyn_resourcecategory                 | нет             | нет               |
| msdyn_resourcecategoryname             | нет             | нет               |
| msdyn_resourceorganizationalunitid     | нет             | нет               |
| msdyn_resourceorganizationalunitidname | нет             | нет               |
| msdyn_salesconsumptionpercentage       | нет             | нет               |
| msdyn_salesestimateatcomplete          | нет             | нет               |
| msdyn_salesestimateatcomplete_base     | нет             | нет               |
| msdyn_salesvariance                    | нет             | нет               |
| msdyn_salesvariance_base               | нет             | нет               |
| msdyn_scheduleddurationminutes         | нет             | нет               |
| msdyn_scheduledend                     | нет             | нет               |
| msdyn_scheduledstart                   | нет             | нет               |
| msdyn_schedulevariance                 | нет             | нет               |
| msdyn_skipupdateestimateline           | нет             | нет               |
| msdyn_skipupdateestimatelinename       | нет             | нет               |
| msdyn_summary                          | нет             | нет               |
| msdyn_varianceofcost                   | нет             | нет               |
| msdyn_varianceofcost_base              | нет             | нет               |

### <a name="project-task-dependency"></a>Зависимость задач проекта

| **Логическое имя**              | **Можно создать** | **Может изменить** |
|-------------------------------|----------------|--------------|
| msdyn_linktype                | нет             | нет           |
| msdyn_linktypename            | нет             | нет           |
| msdyn_predecessortask         | да            | нет           |
| msdyn_predecessortaskname     | да            | нет           |
| msdyn_project                 | да            | нет           |
| msdyn_projectname             | да            | нет           |
| msdyn_projecttaskdependencyid | да            | нет           |
| msdyn_successortask           | да            | нет           |
| msdyn_successortaskname       | да            | нет           |

### <a name="resource-assignment"></a>Назначение ресурса

| **Логическое имя**             | **Можно создать** | **Может изменить** |
|------------------------------|----------------|--------------|
| msdyn_bookableresourceid     | да            | нет           |
| msdyn_bookableresourceidname | да            | нет           |
| msdyn_bookingstatusid        | нет             | нет           |
| msdyn_bookingstatusidname    | нет             | нет           |
| msdyn_committype             | нет             | нет           |
| msdyn_committypename         | нет             | нет           |
| msdyn_effort                 | нет             | нет           |
| msdyn_effortcompleted        | нет             | нет           |
| msdyn_effortremaining        | нет             | нет           |
| msdyn_finish                 | нет             | нет           |
| msdyn_plannedcost            | нет             | нет           |
| msdyn_plannedcost_base       | нет             | нет           |
| msdyn_plannedcostcontour     | нет             | нет           |
| msdyn_plannedsales           | нет             | нет           |
| msdyn_plannedsales_base      | нет             | нет           |
| msdyn_plannedsalescontour    | нет             | нет           |
| msdyn_plannedwork            | нет             | нет           |
| msdyn_projectid              | да            | нет           |
| msdyn_projectidname          | нет             | нет           |
| msdyn_projectteamid          | нет             | нет           |
| msdyn_projectteamidname      | нет             | нет           |
| msdyn_start                  | нет             | нет           |
| msdyn_taskid                 | нет             | нет           |
| msdyn_taskidname             | нет             | нет           |
| msdyn_userresourceid         | нет             | нет           |

### <a name="project-team-member"></a>Участник проектной группы

| **Логическое имя**                                 | **Можно создать** | **Может изменить** |
|--------------------------------------------------|----------------|--------------|
| msdyn_calendarid                                 | нет             | нет           |
| msdyn_creategenericteammemberwithrequirementname | нет             | нет           |
| msdyn_deletestatus                               | нет             | нет           |
| msdyn_deletestatusname                           | нет             | нет           |
| msdyn_effort                                     | нет             | нет           |
| msdyn_effortcompleted                            | нет             | нет           |
| msdyn_effortremaining                            | нет             | нет           |
| msdyn_finish                                     | нет             | нет           |
| msdyn_hardbookedhours                            | нет             | нет           |
| msdyn_hours                                      | нет             | нет           |
| msdyn_markedfordeletiontimer                     | нет             | нет           |
| msdyn_markedfordeletiontimestamp                 | нет             | нет           |
| msdyn_msprojectclientid                          | нет             | нет           |
| msdyn_percentage                                 | нет             | нет           |
| msdyn_requiredhours                              | нет             | нет           |
| msdyn_softbookedhours                            | нет             | нет           |
| msdyn_start                                      | нет             | нет           |

### <a name="project"></a>Project

| **Логическое имя**                       | **Можно создать** | **Может изменить** |
|----------------------------------------|----------------|--------------|
| msdyn_actualexpensecost                | нет             | нет           |
| msdyn_actualexpensecost_base           | нет             | нет           |
| msdyn_actuallaborcost                  | нет             | нет           |
| msdyn_actuallaborcost_base             | нет             | нет           |
| msdyn_actualsales                      | нет             | нет           |
| msdyn_actualsales_base                 | нет             | нет           |
| msdyn_contractlineproject              | да            | нет           |
| msdyn_contractorganizationalunitid     | да            | нет           |
| msdyn_contractorganizationalunitidname | да            | нет           |
| msdyn_costconsumption                  | нет             | нет           |
| msdyn_costestimateatcomplete           | нет             | нет           |
| msdyn_costestimateatcomplete_base      | нет             | нет           |
| msdyn_costvariance                     | нет             | нет           |
| msdyn_costvariance_base                | нет             | нет           |
| msdyn_duration                         | нет             | нет           |
| msdyn_effort                           | нет             | нет           |
| msdyn_effortcompleted                  | нет             | нет           |
| msdyn_effortestimateatcompleteeac      | нет             | нет           |
| msdyn_effortremaining                  | нет             | нет           |
| msdyn_finish                           | да            | да          |
| msdyn_globalrevisiontoken              | нет             | нет           |
| msdyn_islinkedtomsprojectclient        | нет             | нет           |
| msdyn_islinkedtomsprojectclientname    | нет             | нет           |
| msdyn_linkeddocumenturl                | нет             | нет           |
| msdyn_msprojectdocument                | нет             | нет           |
| msdyn_msprojectdocumentname            | нет             | нет           |
| msdyn_plannedexpensecost               | нет             | нет           |
| msdyn_plannedexpensecost_base          | нет             | нет           |
| msdyn_plannedlaborcost                 | нет             | нет           |
| msdyn_plannedlaborcost_base            | нет             | нет           |
| msdyn_plannedsales                     | нет             | нет           |
| msdyn_plannedsales_base                | нет             | нет           |
| msdyn_progress                         | нет             | нет           |
| msdyn_remainingcost                    | нет             | нет           |
| msdyn_remainingcost_base               | нет             | нет           |
| msdyn_remainingsales                   | нет             | нет           |
| msdyn_remainingsales_base              | нет             | нет           |
| msdyn_replaylogheader                  | нет             | нет           |
| msdyn_salesconsumption                 | нет             | нет           |
| msdyn_salesestimateatcompleteeac       | нет             | нет           |
| msdyn_salesestimateatcompleteeac_base  | нет             | нет           |
| msdyn_salesvariance                    | нет             | нет           |
| msdyn_salesvariance_base               | нет             | нет           |
| msdyn_scheduleperformance              | нет             | нет           |
| msdyn_scheduleperformancename          | нет             | нет           |
| msdyn_schedulevariance                 | нет             | нет           |
| msdyn_taskearlieststart                | нет             | нет           |
| msdyn_teamsize                         | нет             | нет           |
| msdyn_teamsize_date                    | нет             | нет           |
| msdyn_teamsize_state                   | нет             | нет           |
| msdyn_totalactualcost                  | нет             | нет           |
| msdyn_totalactualcost_base             | нет             | нет           |
| msdyn_totalplannedcost                 | нет             | нет           |
| msdyn_totalplannedcost_base            | нет             | нет           |


## <a name="limitations-and-known-issues"></a>Известные проблемы и ограничения
Ниже приводится список ограничений и известных проблем:

- API расписания проекта могут использоваться только **Пользователями с лицензией Microsoft Project.** Их не могут использовать:
    - Пользователи приложений
    - Системные пользователи
    - Пользователи-интеграторы
    - Другие пользователи, у которых нет необходимой лицензии
- У каждого **OperationSet** может быть не более 100 операций.
- У каждого пользователя может быть не более 10 открытых **OperationSet**.
- В настоящее время Project Operations поддерживает не более 500 общих задач в проекте.
- Статус сбоя и журналы ошибок в **OperationSet** в настоящее время недоступны.
- [Пределы и границы проектов и задач](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a>Обработка ошибок

   - Чтобы просмотреть ошибки, сгенерированные из наборов операций, перейдите к **Параметры** \> **Интеграция расписания** \> **Наборы операций**.
   - Чтобы просмотреть ошибки, сгенерированные службой расписания проекта, перейдите в раздел **Настройки** \> **Интеграция расписаний** \> **Журналы ошибок PSS**.

## <a name="sample-scenario"></a>Пример сценария

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

## <a name="additional-samples"></a>Дополнительные примеры

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
