---
title: Использование API расписания для выполнения операций с сущностями планирования
description: Этот тема содержит информацию и примеры использования API расписания.
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
ms.contentlocale: ru-RU
ms.lasthandoff: 04/07/2021
ms.locfileid: "5868145"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="890e8-103">Использование API расписания для выполнения операций с сущностями планирования</span><span class="sxs-lookup"><span data-stu-id="890e8-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="890e8-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="890e8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="890e8-105">Некоторые или все функции, описанные в этой статье, доступны в рамках предварительного выпуска.</span><span class="sxs-lookup"><span data-stu-id="890e8-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="890e8-106">Содержимое и функциональность могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="890e8-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="890e8-107">Сущности планирования</span><span class="sxs-lookup"><span data-stu-id="890e8-107">Scheduling entities</span></span>

<span data-ttu-id="890e8-108">API расписания предоставляют возможность выполнять операции создания, обновления и удаления с помощью **сущностей планирования**.</span><span class="sxs-lookup"><span data-stu-id="890e8-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="890e8-109">Управление этими сущностями осуществляется через механизм планирования в проекте для Интернета.</span><span class="sxs-lookup"><span data-stu-id="890e8-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="890e8-110">Операции создания, обновления и удаления с помощью **сущностей планирования** были ограничены в ранних выпусках Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="890e8-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="890e8-111">В следующей таблице представлен полный список **сущностей планирования**.</span><span class="sxs-lookup"><span data-stu-id="890e8-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="890e8-112">Имя сущности</span><span class="sxs-lookup"><span data-stu-id="890e8-112">Entity name</span></span>  | <span data-ttu-id="890e8-113">Логическое имя сущности</span><span class="sxs-lookup"><span data-stu-id="890e8-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="890e8-114">Project</span><span class="sxs-lookup"><span data-stu-id="890e8-114">Project</span></span> | <span data-ttu-id="890e8-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="890e8-115">msdyn_project</span></span> |
| <span data-ttu-id="890e8-116">Задача проекта</span><span class="sxs-lookup"><span data-stu-id="890e8-116">Project Task</span></span>  | <span data-ttu-id="890e8-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="890e8-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="890e8-118">Зависимость задач проекта</span><span class="sxs-lookup"><span data-stu-id="890e8-118">Project Task Dependency</span></span>  | <span data-ttu-id="890e8-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="890e8-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="890e8-120">Назначение ресурса</span><span class="sxs-lookup"><span data-stu-id="890e8-120">Resource Assignment</span></span> | <span data-ttu-id="890e8-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="890e8-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="890e8-122">Группа проекта</span><span class="sxs-lookup"><span data-stu-id="890e8-122">Project Bucket</span></span>  | <span data-ttu-id="890e8-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="890e8-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="890e8-124">Участник проектной группы</span><span class="sxs-lookup"><span data-stu-id="890e8-124">Project Team Member</span></span> | <span data-ttu-id="890e8-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="890e8-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="890e8-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="890e8-126">OperationSet</span></span>

<span data-ttu-id="890e8-127">OperationSet — это шаблон единицы работы, который можно использовать, когда в рамках транзакции необходимо обработать несколько запросов, влияющих на расписание.</span><span class="sxs-lookup"><span data-stu-id="890e8-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="890e8-128">API расписания</span><span class="sxs-lookup"><span data-stu-id="890e8-128">Schedule APIs</span></span>

<span data-ttu-id="890e8-129">Ниже приведен список текущих API расписаний.</span><span class="sxs-lookup"><span data-stu-id="890e8-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="890e8-130">**msdyn_CreateProjectV1**: этот API можно использовать для создания проекта.</span><span class="sxs-lookup"><span data-stu-id="890e8-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="890e8-131">Немедленно создается проект и группа проекта по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="890e8-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="890e8-132">**msdyn_CreateTeamMemberV1**: этот API можно использовать для создания участника рабочей группы проекта.</span><span class="sxs-lookup"><span data-stu-id="890e8-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="890e8-133">Запись участника рабочей группы создается немедленно.</span><span class="sxs-lookup"><span data-stu-id="890e8-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="890e8-134">**msdyn_CreateOperationSetV1**: этот API можно использовать для планирования нескольких запросов, которые должны выполняться в рамках транзакции.</span><span class="sxs-lookup"><span data-stu-id="890e8-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="890e8-135">**msdyn_PSSCreateV1**: этот API можно использовать для создания сущности.</span><span class="sxs-lookup"><span data-stu-id="890e8-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="890e8-136">Сущность может быть любой из сущностей планирования, поддерживающих операцию создания.</span><span class="sxs-lookup"><span data-stu-id="890e8-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="890e8-137">**msdyn_PSSUpdateV1**: этот API можно использовать для обновления сущности.</span><span class="sxs-lookup"><span data-stu-id="890e8-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="890e8-138">Сущность может быть любой из сущностей планирования, поддерживающих операцию обновления.</span><span class="sxs-lookup"><span data-stu-id="890e8-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="890e8-139">**msdyn_PSSDeleteV1**: этот API можно использовать для удаления сущности.</span><span class="sxs-lookup"><span data-stu-id="890e8-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="890e8-140">Сущность может быть любой из сущностей планирования, поддерживающих операцию удаления.</span><span class="sxs-lookup"><span data-stu-id="890e8-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="890e8-141">**msdyn_ExecuteOperationSetV1**: этот API используется для выполнения всех операций в рамках данного набора операций.</span><span class="sxs-lookup"><span data-stu-id="890e8-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="890e8-142">Использование API расписания с OperationSet</span><span class="sxs-lookup"><span data-stu-id="890e8-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="890e8-143">Поскольку записи **CreateProjectV1** и **CreateTeamMemberV1** создаются мгновенно, эти API нельзя использовать в **OperationSet** напрямую.</span><span class="sxs-lookup"><span data-stu-id="890e8-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="890e8-144">Однако вы можете использовать API для создания необходимых записей, создайте **OperationSet**, а затем используйте эти предварительно созданные записи в **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="890e8-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="890e8-145">Поддерживаемые операции</span><span class="sxs-lookup"><span data-stu-id="890e8-145">Supported operations</span></span>

| <span data-ttu-id="890e8-146">Сущность планирования</span><span class="sxs-lookup"><span data-stu-id="890e8-146">Scheduling entity</span></span> | <span data-ttu-id="890e8-147">Создание</span><span class="sxs-lookup"><span data-stu-id="890e8-147">Create</span></span> | <span data-ttu-id="890e8-148">При обновлении</span><span class="sxs-lookup"><span data-stu-id="890e8-148">Update</span></span> | <span data-ttu-id="890e8-149">DELETE</span><span class="sxs-lookup"><span data-stu-id="890e8-149">Delete</span></span> | <span data-ttu-id="890e8-150">Важные замечания</span><span class="sxs-lookup"><span data-stu-id="890e8-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="890e8-151">Задача проекта</span><span class="sxs-lookup"><span data-stu-id="890e8-151">Project task</span></span> | <span data-ttu-id="890e8-152">Да</span><span class="sxs-lookup"><span data-stu-id="890e8-152">Yes</span></span> | <span data-ttu-id="890e8-153">Да</span><span class="sxs-lookup"><span data-stu-id="890e8-153">Yes</span></span> | <span data-ttu-id="890e8-154">Да</span><span class="sxs-lookup"><span data-stu-id="890e8-154">Yes</span></span> | <span data-ttu-id="890e8-155">Без доступа</span><span class="sxs-lookup"><span data-stu-id="890e8-155">None</span></span> |
| <span data-ttu-id="890e8-156">Зависимость задач проекта</span><span class="sxs-lookup"><span data-stu-id="890e8-156">Project task dependency</span></span> | <span data-ttu-id="890e8-157">Да</span><span class="sxs-lookup"><span data-stu-id="890e8-157">Yes</span></span> | <span data-ttu-id="890e8-158">Да</span><span class="sxs-lookup"><span data-stu-id="890e8-158">Yes</span></span> | | <span data-ttu-id="890e8-159">Записи о зависимостях задач проекта не обновляются.</span><span class="sxs-lookup"><span data-stu-id="890e8-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="890e8-160">Вместо этого можно удалить старую запись и создать новую.</span><span class="sxs-lookup"><span data-stu-id="890e8-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="890e8-161">Назначение ресурса</span><span class="sxs-lookup"><span data-stu-id="890e8-161">Resource assignment</span></span> | <span data-ttu-id="890e8-162">Да</span><span class="sxs-lookup"><span data-stu-id="890e8-162">Yes</span></span> | <span data-ttu-id="890e8-163">Да</span><span class="sxs-lookup"><span data-stu-id="890e8-163">Yes</span></span> | | <span data-ttu-id="890e8-164">Не поддерживаются операции со следующими полями: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** и **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="890e8-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="890e8-165">Записи о назначении ресурсов не обновляются.</span><span class="sxs-lookup"><span data-stu-id="890e8-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="890e8-166">Вместо этого можно удалить старую запись и создать новую.</span><span class="sxs-lookup"><span data-stu-id="890e8-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="890e8-167">Группа проекта</span><span class="sxs-lookup"><span data-stu-id="890e8-167">Project bucket</span></span> | <span data-ttu-id="890e8-168">Н/Д</span><span class="sxs-lookup"><span data-stu-id="890e8-168">N/A</span></span> | <span data-ttu-id="890e8-169">Н/Д</span><span class="sxs-lookup"><span data-stu-id="890e8-169">N/A</span></span> | <span data-ttu-id="890e8-170">Н/Д</span><span class="sxs-lookup"><span data-stu-id="890e8-170">N/A</span></span> | <span data-ttu-id="890e8-171">Сегмент по умолчанию создается с помощью API **CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="890e8-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="890e8-172">Участник проектной группы</span><span class="sxs-lookup"><span data-stu-id="890e8-172">Project team member</span></span> | <span data-ttu-id="890e8-173">Да</span><span class="sxs-lookup"><span data-stu-id="890e8-173">Yes</span></span> | <span data-ttu-id="890e8-174">Да</span><span class="sxs-lookup"><span data-stu-id="890e8-174">Yes</span></span> | <span data-ttu-id="890e8-175">Да</span><span class="sxs-lookup"><span data-stu-id="890e8-175">Yes</span></span> | <span data-ttu-id="890e8-176">Для операции создания используйте API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="890e8-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="890e8-177">Project</span><span class="sxs-lookup"><span data-stu-id="890e8-177">Project</span></span> | <span data-ttu-id="890e8-178">Да</span><span class="sxs-lookup"><span data-stu-id="890e8-178">Yes</span></span> | <span data-ttu-id="890e8-179">Да</span><span class="sxs-lookup"><span data-stu-id="890e8-179">Yes</span></span> | <span data-ttu-id="890e8-180">Н/Д</span><span class="sxs-lookup"><span data-stu-id="890e8-180">N/A</span></span> | <span data-ttu-id="890e8-181">Не поддерживаются операции со следующими полями: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** и **Duration**.</span><span class="sxs-lookup"><span data-stu-id="890e8-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="890e8-182">Эти API можно вызывать с объектами сущности, которые включают настраиваемые поля.</span><span class="sxs-lookup"><span data-stu-id="890e8-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="890e8-183">Свойство кода необязательно.</span><span class="sxs-lookup"><span data-stu-id="890e8-183">The ID property is optional.</span></span> <span data-ttu-id="890e8-184">Если оно указано, система пытается его использовать и выдает исключение, если оно не может быть использовано.</span><span class="sxs-lookup"><span data-stu-id="890e8-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="890e8-185">Если оно не указано, система его сгенерирует.</span><span class="sxs-lookup"><span data-stu-id="890e8-185">If it isn't provided, the system will generate it.</span></span>

## <a name="limitations-and-known-issues"></a><span data-ttu-id="890e8-186">Известные проблемы и ограничения</span><span class="sxs-lookup"><span data-stu-id="890e8-186">Limitations and known issues</span></span>
<span data-ttu-id="890e8-187">Ниже приводится список ограничений и известных проблем:</span><span class="sxs-lookup"><span data-stu-id="890e8-187">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="890e8-188">API расписания могут использоваться только **пользователями с лицензией Microsoft Project.**</span><span class="sxs-lookup"><span data-stu-id="890e8-188">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="890e8-189">Их не могут использовать:</span><span class="sxs-lookup"><span data-stu-id="890e8-189">They can't be used by:</span></span>
    - <span data-ttu-id="890e8-190">Пользователи приложений</span><span class="sxs-lookup"><span data-stu-id="890e8-190">Application users</span></span>
    - <span data-ttu-id="890e8-191">Системные пользователи</span><span class="sxs-lookup"><span data-stu-id="890e8-191">System users</span></span>
    - <span data-ttu-id="890e8-192">Пользователи-интеграторы</span><span class="sxs-lookup"><span data-stu-id="890e8-192">Integration users</span></span>
    - <span data-ttu-id="890e8-193">Другие пользователи, у которых нет необходимой лицензии</span><span class="sxs-lookup"><span data-stu-id="890e8-193">Other users that don't have the required license</span></span>
- <span data-ttu-id="890e8-194">У каждого **OperationSet** может быть не более 100 операций.</span><span class="sxs-lookup"><span data-stu-id="890e8-194">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="890e8-195">У каждого пользователя может быть не более 10 открытых **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="890e8-195">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="890e8-196">В настоящее время Project Operations поддерживает не более 500 общих задач в проекте.</span><span class="sxs-lookup"><span data-stu-id="890e8-196">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="890e8-197">Статус сбоя и журналы ошибок в **OperationSet** в настоящее время недоступны.</span><span class="sxs-lookup"><span data-stu-id="890e8-197">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- <span data-ttu-id="890e8-198">API расписания — общедоступная предварительная версия.</span><span class="sxs-lookup"><span data-stu-id="890e8-198">Schedule APIs are in Public preview.</span></span> <span data-ttu-id="890e8-199">Использование этих API в рабочей среде не поддерживается Microsoft.</span><span class="sxs-lookup"><span data-stu-id="890e8-199">Using these APIs in a Production environment isn't supported by Microsoft.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="890e8-200">Пример сценария</span><span class="sxs-lookup"><span data-stu-id="890e8-200">Sample scenario</span></span>

<span data-ttu-id="890e8-201">В этом сценарии вы создадите проект, участника команды, четыре задачи и два назначения ресурсов.</span><span class="sxs-lookup"><span data-stu-id="890e8-201">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="890e8-202">Затем вы обновите одну задачу, обновите проект, удалите одну задачу, удалите одно назначение ресурса и создадите зависимость задачи.</span><span class="sxs-lookup"><span data-stu-id="890e8-202">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

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

## <a name="additional-samples"></a><span data-ttu-id="890e8-203">Дополнительные примеры</span><span class="sxs-lookup"><span data-stu-id="890e8-203">Additional samples</span></span>

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
