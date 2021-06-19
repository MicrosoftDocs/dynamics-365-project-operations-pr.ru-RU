---
title: Использование API расписания для выполнения операций с сущностями планирования
description: Этот тема содержит информацию и примеры использования API расписания.
author: sigitac
ms.date: 04/27/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4a032dc7bcbdf23fce3c3b2ca63c51d473bd8e26
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116813"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="3d7eb-103">Использование API расписания для выполнения операций с сущностями планирования</span><span class="sxs-lookup"><span data-stu-id="3d7eb-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="3d7eb-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="3d7eb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="3d7eb-105">Некоторые или все функции, описанные в этой статье, доступны в рамках предварительного выпуска.</span><span class="sxs-lookup"><span data-stu-id="3d7eb-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="3d7eb-106">Содержимое и функциональность могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="3d7eb-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="3d7eb-107">Сущности планирования</span><span class="sxs-lookup"><span data-stu-id="3d7eb-107">Scheduling entities</span></span>

<span data-ttu-id="3d7eb-108">API расписания предоставляют возможность выполнять операции создания, обновления и удаления с помощью **сущностей планирования**.</span><span class="sxs-lookup"><span data-stu-id="3d7eb-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="3d7eb-109">Управление этими сущностями осуществляется через механизм планирования в проекте для Интернета.</span><span class="sxs-lookup"><span data-stu-id="3d7eb-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="3d7eb-110">Операции создания, обновления и удаления с помощью **сущностей планирования** были ограничены в ранних выпусках Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="3d7eb-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="3d7eb-111">В следующей таблице представлен полный список **сущностей планирования**.</span><span class="sxs-lookup"><span data-stu-id="3d7eb-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="3d7eb-112">Имя сущности</span><span class="sxs-lookup"><span data-stu-id="3d7eb-112">Entity name</span></span>  | <span data-ttu-id="3d7eb-113">Логическое имя сущности</span><span class="sxs-lookup"><span data-stu-id="3d7eb-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="3d7eb-114">Project</span><span class="sxs-lookup"><span data-stu-id="3d7eb-114">Project</span></span> | <span data-ttu-id="3d7eb-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="3d7eb-115">msdyn_project</span></span> |
| <span data-ttu-id="3d7eb-116">Задача проекта</span><span class="sxs-lookup"><span data-stu-id="3d7eb-116">Project Task</span></span>  | <span data-ttu-id="3d7eb-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="3d7eb-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="3d7eb-118">Зависимость задач проекта</span><span class="sxs-lookup"><span data-stu-id="3d7eb-118">Project Task Dependency</span></span>  | <span data-ttu-id="3d7eb-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="3d7eb-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="3d7eb-120">Назначение ресурса</span><span class="sxs-lookup"><span data-stu-id="3d7eb-120">Resource Assignment</span></span> | <span data-ttu-id="3d7eb-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="3d7eb-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="3d7eb-122">Группа проекта</span><span class="sxs-lookup"><span data-stu-id="3d7eb-122">Project Bucket</span></span>  | <span data-ttu-id="3d7eb-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="3d7eb-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="3d7eb-124">Участник проектной группы</span><span class="sxs-lookup"><span data-stu-id="3d7eb-124">Project Team Member</span></span> | <span data-ttu-id="3d7eb-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="3d7eb-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="3d7eb-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="3d7eb-126">OperationSet</span></span>

<span data-ttu-id="3d7eb-127">OperationSet — это шаблон единицы работы, который можно использовать, когда в рамках транзакции необходимо обработать несколько запросов, влияющих на расписание.</span><span class="sxs-lookup"><span data-stu-id="3d7eb-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="3d7eb-128">API расписания</span><span class="sxs-lookup"><span data-stu-id="3d7eb-128">Schedule APIs</span></span>

<span data-ttu-id="3d7eb-129">Ниже приведен список текущих API расписаний.</span><span class="sxs-lookup"><span data-stu-id="3d7eb-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="3d7eb-130">**msdyn_CreateProjectV1**: этот API можно использовать для создания проекта.</span><span class="sxs-lookup"><span data-stu-id="3d7eb-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="3d7eb-131">Немедленно создается проект и группа проекта по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3d7eb-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="3d7eb-132">**msdyn_CreateTeamMemberV1**: этот API можно использовать для создания участника рабочей группы проекта.</span><span class="sxs-lookup"><span data-stu-id="3d7eb-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="3d7eb-133">Запись участника рабочей группы создается немедленно.</span><span class="sxs-lookup"><span data-stu-id="3d7eb-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="3d7eb-134">**msdyn_CreateOperationSetV1**: этот API можно использовать для планирования нескольких запросов, которые должны выполняться в рамках транзакции.</span><span class="sxs-lookup"><span data-stu-id="3d7eb-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="3d7eb-135">**msdyn_PSSCreateV1**: этот API можно использовать для создания сущности.</span><span class="sxs-lookup"><span data-stu-id="3d7eb-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="3d7eb-136">Сущность может быть любой из сущностей планирования, поддерживающих операцию создания.</span><span class="sxs-lookup"><span data-stu-id="3d7eb-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="3d7eb-137">**msdyn_PSSUpdateV1**: этот API можно использовать для обновления сущности.</span><span class="sxs-lookup"><span data-stu-id="3d7eb-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="3d7eb-138">Сущность может быть любой из сущностей планирования, поддерживающих операцию обновления.</span><span class="sxs-lookup"><span data-stu-id="3d7eb-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="3d7eb-139">**msdyn_PSSDeleteV1**: этот API можно использовать для удаления сущности.</span><span class="sxs-lookup"><span data-stu-id="3d7eb-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="3d7eb-140">Сущность может быть любой из сущностей планирования, поддерживающих операцию удаления.</span><span class="sxs-lookup"><span data-stu-id="3d7eb-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="3d7eb-141">**msdyn_ExecuteOperationSetV1**: этот API используется для выполнения всех операций в рамках данного набора операций.</span><span class="sxs-lookup"><span data-stu-id="3d7eb-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="3d7eb-142">Использование API расписания с OperationSet</span><span class="sxs-lookup"><span data-stu-id="3d7eb-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="3d7eb-143">Поскольку записи **CreateProjectV1** и **CreateTeamMemberV1** создаются мгновенно, эти API нельзя использовать в **OperationSet** напрямую.</span><span class="sxs-lookup"><span data-stu-id="3d7eb-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="3d7eb-144">Однако вы можете использовать API для создания необходимых записей, создайте **OperationSet**, а затем используйте эти предварительно созданные записи в **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="3d7eb-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="3d7eb-145">Поддерживаемые операции</span><span class="sxs-lookup"><span data-stu-id="3d7eb-145">Supported operations</span></span>

| <span data-ttu-id="3d7eb-146">Сущность планирования</span><span class="sxs-lookup"><span data-stu-id="3d7eb-146">Scheduling entity</span></span> | <span data-ttu-id="3d7eb-147">Создание</span><span class="sxs-lookup"><span data-stu-id="3d7eb-147">Create</span></span> | <span data-ttu-id="3d7eb-148">При обновлении</span><span class="sxs-lookup"><span data-stu-id="3d7eb-148">Update</span></span> | <span data-ttu-id="3d7eb-149">DELETE</span><span class="sxs-lookup"><span data-stu-id="3d7eb-149">Delete</span></span> | <span data-ttu-id="3d7eb-150">Важные замечания</span><span class="sxs-lookup"><span data-stu-id="3d7eb-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="3d7eb-151">Задача проекта</span><span class="sxs-lookup"><span data-stu-id="3d7eb-151">Project task</span></span> | <span data-ttu-id="3d7eb-152">Да</span><span class="sxs-lookup"><span data-stu-id="3d7eb-152">Yes</span></span> | <span data-ttu-id="3d7eb-153">Да</span><span class="sxs-lookup"><span data-stu-id="3d7eb-153">Yes</span></span> | <span data-ttu-id="3d7eb-154">Да</span><span class="sxs-lookup"><span data-stu-id="3d7eb-154">Yes</span></span> | <span data-ttu-id="3d7eb-155">Без доступа</span><span class="sxs-lookup"><span data-stu-id="3d7eb-155">None</span></span> |
| <span data-ttu-id="3d7eb-156">Зависимость задач проекта</span><span class="sxs-lookup"><span data-stu-id="3d7eb-156">Project task dependency</span></span> | <span data-ttu-id="3d7eb-157">Да</span><span class="sxs-lookup"><span data-stu-id="3d7eb-157">Yes</span></span> | <span data-ttu-id="3d7eb-158">Да</span><span class="sxs-lookup"><span data-stu-id="3d7eb-158">Yes</span></span> | | <span data-ttu-id="3d7eb-159">Записи о зависимостях задач проекта не обновляются.</span><span class="sxs-lookup"><span data-stu-id="3d7eb-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="3d7eb-160">Вместо этого можно удалить старую запись и создать новую.</span><span class="sxs-lookup"><span data-stu-id="3d7eb-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="3d7eb-161">Назначение ресурса</span><span class="sxs-lookup"><span data-stu-id="3d7eb-161">Resource assignment</span></span> | <span data-ttu-id="3d7eb-162">Да</span><span class="sxs-lookup"><span data-stu-id="3d7eb-162">Yes</span></span> | <span data-ttu-id="3d7eb-163">Да</span><span class="sxs-lookup"><span data-stu-id="3d7eb-163">Yes</span></span> | | <span data-ttu-id="3d7eb-164">Не поддерживаются операции со следующими полями: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** и **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="3d7eb-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="3d7eb-165">Записи о назначении ресурсов не обновляются.</span><span class="sxs-lookup"><span data-stu-id="3d7eb-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="3d7eb-166">Вместо этого можно удалить старую запись и создать новую.</span><span class="sxs-lookup"><span data-stu-id="3d7eb-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="3d7eb-167">Группа проекта</span><span class="sxs-lookup"><span data-stu-id="3d7eb-167">Project bucket</span></span> | <span data-ttu-id="3d7eb-168">Н/Д</span><span class="sxs-lookup"><span data-stu-id="3d7eb-168">N/A</span></span> | <span data-ttu-id="3d7eb-169">Н/Д</span><span class="sxs-lookup"><span data-stu-id="3d7eb-169">N/A</span></span> | <span data-ttu-id="3d7eb-170">Н/Д</span><span class="sxs-lookup"><span data-stu-id="3d7eb-170">N/A</span></span> | <span data-ttu-id="3d7eb-171">Сегмент по умолчанию создается с помощью API **CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="3d7eb-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="3d7eb-172">Участник проектной группы</span><span class="sxs-lookup"><span data-stu-id="3d7eb-172">Project team member</span></span> | <span data-ttu-id="3d7eb-173">Да</span><span class="sxs-lookup"><span data-stu-id="3d7eb-173">Yes</span></span> | <span data-ttu-id="3d7eb-174">Да</span><span class="sxs-lookup"><span data-stu-id="3d7eb-174">Yes</span></span> | <span data-ttu-id="3d7eb-175">Да</span><span class="sxs-lookup"><span data-stu-id="3d7eb-175">Yes</span></span> | <span data-ttu-id="3d7eb-176">Для операции создания используйте API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="3d7eb-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="3d7eb-177">Project</span><span class="sxs-lookup"><span data-stu-id="3d7eb-177">Project</span></span> | <span data-ttu-id="3d7eb-178">Да</span><span class="sxs-lookup"><span data-stu-id="3d7eb-178">Yes</span></span> | <span data-ttu-id="3d7eb-179">Да</span><span class="sxs-lookup"><span data-stu-id="3d7eb-179">Yes</span></span> | <span data-ttu-id="3d7eb-180">Н/Д</span><span class="sxs-lookup"><span data-stu-id="3d7eb-180">N/A</span></span> | <span data-ttu-id="3d7eb-181">Не поддерживаются операции со следующими полями: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** и **Duration**.</span><span class="sxs-lookup"><span data-stu-id="3d7eb-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="3d7eb-182">Эти API можно вызывать с объектами сущности, которые включают настраиваемые поля.</span><span class="sxs-lookup"><span data-stu-id="3d7eb-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="3d7eb-183">Свойство кода необязательно.</span><span class="sxs-lookup"><span data-stu-id="3d7eb-183">The ID property is optional.</span></span> <span data-ttu-id="3d7eb-184">Если оно указано, система пытается его использовать и выдает исключение, если оно не может быть использовано.</span><span class="sxs-lookup"><span data-stu-id="3d7eb-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="3d7eb-185">Если оно не указано, система его сгенерирует.</span><span class="sxs-lookup"><span data-stu-id="3d7eb-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="3d7eb-186">Запрещенные поля</span><span class="sxs-lookup"><span data-stu-id="3d7eb-186">Restricted fields</span></span>

<span data-ttu-id="3d7eb-187">В следующих таблицах определены поля, которые защищены от **Создать** и **Изменить.**</span><span class="sxs-lookup"><span data-stu-id="3d7eb-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="3d7eb-188">Задача проекта</span><span class="sxs-lookup"><span data-stu-id="3d7eb-188">Project task</span></span>

| <span data-ttu-id="3d7eb-189">**Логическое имя**</span><span class="sxs-lookup"><span data-stu-id="3d7eb-189">**Logical name**</span></span>                       | <span data-ttu-id="3d7eb-190">**Можно создать**</span><span class="sxs-lookup"><span data-stu-id="3d7eb-190">**Can create**</span></span> | <span data-ttu-id="3d7eb-191">**Может изменить**</span><span class="sxs-lookup"><span data-stu-id="3d7eb-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="3d7eb-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="3d7eb-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="3d7eb-193">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-193">no</span></span>             | <span data-ttu-id="3d7eb-194">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-194">no</span></span>               |
| <span data-ttu-id="3d7eb-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="3d7eb-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="3d7eb-196">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-196">no</span></span>             | <span data-ttu-id="3d7eb-197">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-197">no</span></span>               |
| <span data-ttu-id="3d7eb-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="3d7eb-198">msdyn_actualend</span></span>                        | <span data-ttu-id="3d7eb-199">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-199">no</span></span>             | <span data-ttu-id="3d7eb-200">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-200">no</span></span>               |
| <span data-ttu-id="3d7eb-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="3d7eb-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="3d7eb-202">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-202">no</span></span>             | <span data-ttu-id="3d7eb-203">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-203">no</span></span>               |
| <span data-ttu-id="3d7eb-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="3d7eb-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="3d7eb-205">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-205">no</span></span>             | <span data-ttu-id="3d7eb-206">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-206">no</span></span>               |
| <span data-ttu-id="3d7eb-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="3d7eb-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="3d7eb-208">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-208">no</span></span>             | <span data-ttu-id="3d7eb-209">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-209">no</span></span>               |
| <span data-ttu-id="3d7eb-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="3d7eb-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="3d7eb-211">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-211">no</span></span>             | <span data-ttu-id="3d7eb-212">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-212">no</span></span>               |
| <span data-ttu-id="3d7eb-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="3d7eb-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="3d7eb-214">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-214">no</span></span>             | <span data-ttu-id="3d7eb-215">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-215">no</span></span>               |
| <span data-ttu-id="3d7eb-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="3d7eb-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="3d7eb-217">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-217">no</span></span>             | <span data-ttu-id="3d7eb-218">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-218">no</span></span>               |
| <span data-ttu-id="3d7eb-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="3d7eb-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="3d7eb-220">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-220">no</span></span>             | <span data-ttu-id="3d7eb-221">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-221">no</span></span>               |
| <span data-ttu-id="3d7eb-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="3d7eb-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="3d7eb-223">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-223">no</span></span>             | <span data-ttu-id="3d7eb-224">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-224">no</span></span>               |
| <span data-ttu-id="3d7eb-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="3d7eb-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="3d7eb-226">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-226">no</span></span>             | <span data-ttu-id="3d7eb-227">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-227">no</span></span>               |
| <span data-ttu-id="3d7eb-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="3d7eb-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="3d7eb-229">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-229">no</span></span>             | <span data-ttu-id="3d7eb-230">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-230">no</span></span>               |
| <span data-ttu-id="3d7eb-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="3d7eb-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="3d7eb-232">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-232">no</span></span>             | <span data-ttu-id="3d7eb-233">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-233">no</span></span>               |
| <span data-ttu-id="3d7eb-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="3d7eb-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="3d7eb-235">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-235">no</span></span>             | <span data-ttu-id="3d7eb-236">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-236">no</span></span>               |
| <span data-ttu-id="3d7eb-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="3d7eb-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="3d7eb-238">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-238">no</span></span>             | <span data-ttu-id="3d7eb-239">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-239">no</span></span>               |
| <span data-ttu-id="3d7eb-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="3d7eb-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="3d7eb-241">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-241">no</span></span>             | <span data-ttu-id="3d7eb-242">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-242">no</span></span>               |
| <span data-ttu-id="3d7eb-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="3d7eb-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="3d7eb-244">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-244">no</span></span>             | <span data-ttu-id="3d7eb-245">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-245">no</span></span>               |
| <span data-ttu-id="3d7eb-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="3d7eb-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="3d7eb-247">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-247">no</span></span>             | <span data-ttu-id="3d7eb-248">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-248">no</span></span>               |
| <span data-ttu-id="3d7eb-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="3d7eb-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="3d7eb-250">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-250">no</span></span>             | <span data-ttu-id="3d7eb-251">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-251">no</span></span>               |
| <span data-ttu-id="3d7eb-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="3d7eb-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="3d7eb-253">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-253">no</span></span>             | <span data-ttu-id="3d7eb-254">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-254">no</span></span>               |
| <span data-ttu-id="3d7eb-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="3d7eb-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="3d7eb-256">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-256">no</span></span>             | <span data-ttu-id="3d7eb-257">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-257">no</span></span>               |
| <span data-ttu-id="3d7eb-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="3d7eb-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="3d7eb-259">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-259">no</span></span>             | <span data-ttu-id="3d7eb-260">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-260">no</span></span>               |
| <span data-ttu-id="3d7eb-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="3d7eb-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="3d7eb-262">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-262">no</span></span>             | <span data-ttu-id="3d7eb-263">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-263">no</span></span>               |
| <span data-ttu-id="3d7eb-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="3d7eb-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="3d7eb-265">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-265">no</span></span>             | <span data-ttu-id="3d7eb-266">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-266">no</span></span>               |
| <span data-ttu-id="3d7eb-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="3d7eb-267">msdyn_progress</span></span>                         | <span data-ttu-id="3d7eb-268">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-268">no</span></span>             | <span data-ttu-id="3d7eb-269">нет (да для P4W)</span><span class="sxs-lookup"><span data-stu-id="3d7eb-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="3d7eb-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="3d7eb-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="3d7eb-271">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-271">no</span></span>             | <span data-ttu-id="3d7eb-272">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-272">no</span></span>               |
| <span data-ttu-id="3d7eb-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="3d7eb-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="3d7eb-274">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-274">no</span></span>             | <span data-ttu-id="3d7eb-275">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-275">no</span></span>               |
| <span data-ttu-id="3d7eb-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="3d7eb-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="3d7eb-277">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-277">no</span></span>             | <span data-ttu-id="3d7eb-278">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-278">no</span></span>               |
| <span data-ttu-id="3d7eb-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="3d7eb-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="3d7eb-280">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-280">no</span></span>             | <span data-ttu-id="3d7eb-281">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-281">no</span></span>               |
| <span data-ttu-id="3d7eb-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="3d7eb-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="3d7eb-283">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-283">no</span></span>             | <span data-ttu-id="3d7eb-284">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-284">no</span></span>               |
| <span data-ttu-id="3d7eb-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="3d7eb-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="3d7eb-286">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-286">no</span></span>             | <span data-ttu-id="3d7eb-287">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-287">no</span></span>               |
| <span data-ttu-id="3d7eb-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="3d7eb-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="3d7eb-289">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-289">no</span></span>             | <span data-ttu-id="3d7eb-290">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-290">no</span></span>               |
| <span data-ttu-id="3d7eb-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="3d7eb-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="3d7eb-292">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-292">no</span></span>             | <span data-ttu-id="3d7eb-293">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-293">no</span></span>               |
| <span data-ttu-id="3d7eb-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="3d7eb-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="3d7eb-295">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-295">no</span></span>             | <span data-ttu-id="3d7eb-296">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-296">no</span></span>               |
| <span data-ttu-id="3d7eb-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="3d7eb-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="3d7eb-298">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-298">no</span></span>             | <span data-ttu-id="3d7eb-299">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-299">no</span></span>               |
| <span data-ttu-id="3d7eb-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="3d7eb-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="3d7eb-301">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-301">no</span></span>             | <span data-ttu-id="3d7eb-302">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-302">no</span></span>               |
| <span data-ttu-id="3d7eb-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="3d7eb-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="3d7eb-304">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-304">no</span></span>             | <span data-ttu-id="3d7eb-305">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-305">no</span></span>               |
| <span data-ttu-id="3d7eb-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="3d7eb-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="3d7eb-307">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-307">no</span></span>             | <span data-ttu-id="3d7eb-308">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-308">no</span></span>               |
| <span data-ttu-id="3d7eb-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="3d7eb-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="3d7eb-310">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-310">no</span></span>             | <span data-ttu-id="3d7eb-311">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-311">no</span></span>               |
| <span data-ttu-id="3d7eb-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="3d7eb-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="3d7eb-313">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-313">no</span></span>             | <span data-ttu-id="3d7eb-314">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-314">no</span></span>               |
| <span data-ttu-id="3d7eb-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="3d7eb-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="3d7eb-316">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-316">no</span></span>             | <span data-ttu-id="3d7eb-317">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-317">no</span></span>               |
| <span data-ttu-id="3d7eb-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="3d7eb-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="3d7eb-319">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-319">no</span></span>             | <span data-ttu-id="3d7eb-320">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-320">no</span></span>               |
| <span data-ttu-id="3d7eb-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="3d7eb-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="3d7eb-322">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-322">no</span></span>             | <span data-ttu-id="3d7eb-323">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-323">no</span></span>               |
| <span data-ttu-id="3d7eb-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="3d7eb-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="3d7eb-325">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-325">no</span></span>             | <span data-ttu-id="3d7eb-326">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-326">no</span></span>               |
| <span data-ttu-id="3d7eb-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="3d7eb-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="3d7eb-328">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-328">no</span></span>             | <span data-ttu-id="3d7eb-329">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-329">no</span></span>               |
| <span data-ttu-id="3d7eb-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="3d7eb-330">msdyn_summary</span></span>                          | <span data-ttu-id="3d7eb-331">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-331">no</span></span>             | <span data-ttu-id="3d7eb-332">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-332">no</span></span>               |
| <span data-ttu-id="3d7eb-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="3d7eb-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="3d7eb-334">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-334">no</span></span>             | <span data-ttu-id="3d7eb-335">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-335">no</span></span>               |
| <span data-ttu-id="3d7eb-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="3d7eb-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="3d7eb-337">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-337">no</span></span>             | <span data-ttu-id="3d7eb-338">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="3d7eb-339">Зависимость задач проекта</span><span class="sxs-lookup"><span data-stu-id="3d7eb-339">Project task dependency</span></span>

| <span data-ttu-id="3d7eb-340">**Логическое имя**</span><span class="sxs-lookup"><span data-stu-id="3d7eb-340">**Logical name**</span></span>              | <span data-ttu-id="3d7eb-341">**Можно создать**</span><span class="sxs-lookup"><span data-stu-id="3d7eb-341">**Can create**</span></span> | <span data-ttu-id="3d7eb-342">**Может изменить**</span><span class="sxs-lookup"><span data-stu-id="3d7eb-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="3d7eb-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="3d7eb-343">msdyn_linktype</span></span>                | <span data-ttu-id="3d7eb-344">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-344">no</span></span>             | <span data-ttu-id="3d7eb-345">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-345">no</span></span>           |
| <span data-ttu-id="3d7eb-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="3d7eb-346">msdyn_linktypename</span></span>            | <span data-ttu-id="3d7eb-347">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-347">no</span></span>             | <span data-ttu-id="3d7eb-348">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-348">no</span></span>           |
| <span data-ttu-id="3d7eb-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="3d7eb-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="3d7eb-350">да</span><span class="sxs-lookup"><span data-stu-id="3d7eb-350">yes</span></span>            | <span data-ttu-id="3d7eb-351">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-351">no</span></span>           |
| <span data-ttu-id="3d7eb-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="3d7eb-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="3d7eb-353">да</span><span class="sxs-lookup"><span data-stu-id="3d7eb-353">yes</span></span>            | <span data-ttu-id="3d7eb-354">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-354">no</span></span>           |
| <span data-ttu-id="3d7eb-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="3d7eb-355">msdyn_project</span></span>                 | <span data-ttu-id="3d7eb-356">да</span><span class="sxs-lookup"><span data-stu-id="3d7eb-356">yes</span></span>            | <span data-ttu-id="3d7eb-357">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-357">no</span></span>           |
| <span data-ttu-id="3d7eb-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="3d7eb-358">msdyn_projectname</span></span>             | <span data-ttu-id="3d7eb-359">да</span><span class="sxs-lookup"><span data-stu-id="3d7eb-359">yes</span></span>            | <span data-ttu-id="3d7eb-360">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-360">no</span></span>           |
| <span data-ttu-id="3d7eb-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="3d7eb-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="3d7eb-362">да</span><span class="sxs-lookup"><span data-stu-id="3d7eb-362">yes</span></span>            | <span data-ttu-id="3d7eb-363">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-363">no</span></span>           |
| <span data-ttu-id="3d7eb-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="3d7eb-364">msdyn_successortask</span></span>           | <span data-ttu-id="3d7eb-365">да</span><span class="sxs-lookup"><span data-stu-id="3d7eb-365">yes</span></span>            | <span data-ttu-id="3d7eb-366">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-366">no</span></span>           |
| <span data-ttu-id="3d7eb-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="3d7eb-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="3d7eb-368">да</span><span class="sxs-lookup"><span data-stu-id="3d7eb-368">yes</span></span>            | <span data-ttu-id="3d7eb-369">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="3d7eb-370">Назначение ресурса</span><span class="sxs-lookup"><span data-stu-id="3d7eb-370">Resource assignment</span></span>

| <span data-ttu-id="3d7eb-371">**Логическое имя**</span><span class="sxs-lookup"><span data-stu-id="3d7eb-371">**Logical name**</span></span>             | <span data-ttu-id="3d7eb-372">**Можно создать**</span><span class="sxs-lookup"><span data-stu-id="3d7eb-372">**Can create**</span></span> | <span data-ttu-id="3d7eb-373">**Может изменить**</span><span class="sxs-lookup"><span data-stu-id="3d7eb-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="3d7eb-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="3d7eb-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="3d7eb-375">да</span><span class="sxs-lookup"><span data-stu-id="3d7eb-375">yes</span></span>            | <span data-ttu-id="3d7eb-376">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-376">no</span></span>           |
| <span data-ttu-id="3d7eb-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="3d7eb-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="3d7eb-378">да</span><span class="sxs-lookup"><span data-stu-id="3d7eb-378">yes</span></span>            | <span data-ttu-id="3d7eb-379">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-379">no</span></span>           |
| <span data-ttu-id="3d7eb-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="3d7eb-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="3d7eb-381">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-381">no</span></span>             | <span data-ttu-id="3d7eb-382">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-382">no</span></span>           |
| <span data-ttu-id="3d7eb-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="3d7eb-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="3d7eb-384">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-384">no</span></span>             | <span data-ttu-id="3d7eb-385">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-385">no</span></span>           |
| <span data-ttu-id="3d7eb-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="3d7eb-386">msdyn_committype</span></span>             | <span data-ttu-id="3d7eb-387">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-387">no</span></span>             | <span data-ttu-id="3d7eb-388">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-388">no</span></span>           |
| <span data-ttu-id="3d7eb-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="3d7eb-389">msdyn_committypename</span></span>         | <span data-ttu-id="3d7eb-390">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-390">no</span></span>             | <span data-ttu-id="3d7eb-391">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-391">no</span></span>           |
| <span data-ttu-id="3d7eb-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="3d7eb-392">msdyn_effort</span></span>                 | <span data-ttu-id="3d7eb-393">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-393">no</span></span>             | <span data-ttu-id="3d7eb-394">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-394">no</span></span>           |
| <span data-ttu-id="3d7eb-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="3d7eb-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="3d7eb-396">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-396">no</span></span>             | <span data-ttu-id="3d7eb-397">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-397">no</span></span>           |
| <span data-ttu-id="3d7eb-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="3d7eb-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="3d7eb-399">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-399">no</span></span>             | <span data-ttu-id="3d7eb-400">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-400">no</span></span>           |
| <span data-ttu-id="3d7eb-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="3d7eb-401">msdyn_finish</span></span>                 | <span data-ttu-id="3d7eb-402">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-402">no</span></span>             | <span data-ttu-id="3d7eb-403">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-403">no</span></span>           |
| <span data-ttu-id="3d7eb-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="3d7eb-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="3d7eb-405">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-405">no</span></span>             | <span data-ttu-id="3d7eb-406">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-406">no</span></span>           |
| <span data-ttu-id="3d7eb-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="3d7eb-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="3d7eb-408">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-408">no</span></span>             | <span data-ttu-id="3d7eb-409">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-409">no</span></span>           |
| <span data-ttu-id="3d7eb-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="3d7eb-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="3d7eb-411">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-411">no</span></span>             | <span data-ttu-id="3d7eb-412">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-412">no</span></span>           |
| <span data-ttu-id="3d7eb-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="3d7eb-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="3d7eb-414">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-414">no</span></span>             | <span data-ttu-id="3d7eb-415">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-415">no</span></span>           |
| <span data-ttu-id="3d7eb-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="3d7eb-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="3d7eb-417">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-417">no</span></span>             | <span data-ttu-id="3d7eb-418">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-418">no</span></span>           |
| <span data-ttu-id="3d7eb-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="3d7eb-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="3d7eb-420">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-420">no</span></span>             | <span data-ttu-id="3d7eb-421">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-421">no</span></span>           |
| <span data-ttu-id="3d7eb-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="3d7eb-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="3d7eb-423">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-423">no</span></span>             | <span data-ttu-id="3d7eb-424">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-424">no</span></span>           |
| <span data-ttu-id="3d7eb-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="3d7eb-425">msdyn_projectid</span></span>              | <span data-ttu-id="3d7eb-426">да</span><span class="sxs-lookup"><span data-stu-id="3d7eb-426">yes</span></span>            | <span data-ttu-id="3d7eb-427">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-427">no</span></span>           |
| <span data-ttu-id="3d7eb-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="3d7eb-428">msdyn_projectidname</span></span>          | <span data-ttu-id="3d7eb-429">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-429">no</span></span>             | <span data-ttu-id="3d7eb-430">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-430">no</span></span>           |
| <span data-ttu-id="3d7eb-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="3d7eb-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="3d7eb-432">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-432">no</span></span>             | <span data-ttu-id="3d7eb-433">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-433">no</span></span>           |
| <span data-ttu-id="3d7eb-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="3d7eb-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="3d7eb-435">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-435">no</span></span>             | <span data-ttu-id="3d7eb-436">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-436">no</span></span>           |
| <span data-ttu-id="3d7eb-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="3d7eb-437">msdyn_start</span></span>                  | <span data-ttu-id="3d7eb-438">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-438">no</span></span>             | <span data-ttu-id="3d7eb-439">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-439">no</span></span>           |
| <span data-ttu-id="3d7eb-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="3d7eb-440">msdyn_taskid</span></span>                 | <span data-ttu-id="3d7eb-441">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-441">no</span></span>             | <span data-ttu-id="3d7eb-442">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-442">no</span></span>           |
| <span data-ttu-id="3d7eb-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="3d7eb-443">msdyn_taskidname</span></span>             | <span data-ttu-id="3d7eb-444">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-444">no</span></span>             | <span data-ttu-id="3d7eb-445">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-445">no</span></span>           |
| <span data-ttu-id="3d7eb-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="3d7eb-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="3d7eb-447">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-447">no</span></span>             | <span data-ttu-id="3d7eb-448">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="3d7eb-449">Участник проектной группы</span><span class="sxs-lookup"><span data-stu-id="3d7eb-449">Project team member</span></span>

| <span data-ttu-id="3d7eb-450">**Логическое имя**</span><span class="sxs-lookup"><span data-stu-id="3d7eb-450">**Logical name**</span></span>                                 | <span data-ttu-id="3d7eb-451">**Можно создать**</span><span class="sxs-lookup"><span data-stu-id="3d7eb-451">**Can create**</span></span> | <span data-ttu-id="3d7eb-452">**Может изменить**</span><span class="sxs-lookup"><span data-stu-id="3d7eb-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="3d7eb-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="3d7eb-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="3d7eb-454">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-454">no</span></span>             | <span data-ttu-id="3d7eb-455">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-455">no</span></span>           |
| <span data-ttu-id="3d7eb-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="3d7eb-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="3d7eb-457">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-457">no</span></span>             | <span data-ttu-id="3d7eb-458">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-458">no</span></span>           |
| <span data-ttu-id="3d7eb-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="3d7eb-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="3d7eb-460">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-460">no</span></span>             | <span data-ttu-id="3d7eb-461">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-461">no</span></span>           |
| <span data-ttu-id="3d7eb-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="3d7eb-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="3d7eb-463">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-463">no</span></span>             | <span data-ttu-id="3d7eb-464">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-464">no</span></span>           |
| <span data-ttu-id="3d7eb-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="3d7eb-465">msdyn_effort</span></span>                                     | <span data-ttu-id="3d7eb-466">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-466">no</span></span>             | <span data-ttu-id="3d7eb-467">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-467">no</span></span>           |
| <span data-ttu-id="3d7eb-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="3d7eb-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="3d7eb-469">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-469">no</span></span>             | <span data-ttu-id="3d7eb-470">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-470">no</span></span>           |
| <span data-ttu-id="3d7eb-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="3d7eb-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="3d7eb-472">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-472">no</span></span>             | <span data-ttu-id="3d7eb-473">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-473">no</span></span>           |
| <span data-ttu-id="3d7eb-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="3d7eb-474">msdyn_finish</span></span>                                     | <span data-ttu-id="3d7eb-475">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-475">no</span></span>             | <span data-ttu-id="3d7eb-476">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-476">no</span></span>           |
| <span data-ttu-id="3d7eb-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="3d7eb-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="3d7eb-478">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-478">no</span></span>             | <span data-ttu-id="3d7eb-479">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-479">no</span></span>           |
| <span data-ttu-id="3d7eb-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="3d7eb-480">msdyn_hours</span></span>                                      | <span data-ttu-id="3d7eb-481">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-481">no</span></span>             | <span data-ttu-id="3d7eb-482">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-482">no</span></span>           |
| <span data-ttu-id="3d7eb-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="3d7eb-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="3d7eb-484">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-484">no</span></span>             | <span data-ttu-id="3d7eb-485">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-485">no</span></span>           |
| <span data-ttu-id="3d7eb-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="3d7eb-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="3d7eb-487">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-487">no</span></span>             | <span data-ttu-id="3d7eb-488">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-488">no</span></span>           |
| <span data-ttu-id="3d7eb-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="3d7eb-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="3d7eb-490">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-490">no</span></span>             | <span data-ttu-id="3d7eb-491">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-491">no</span></span>           |
| <span data-ttu-id="3d7eb-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="3d7eb-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="3d7eb-493">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-493">no</span></span>             | <span data-ttu-id="3d7eb-494">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-494">no</span></span>           |
| <span data-ttu-id="3d7eb-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="3d7eb-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="3d7eb-496">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-496">no</span></span>             | <span data-ttu-id="3d7eb-497">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-497">no</span></span>           |
| <span data-ttu-id="3d7eb-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="3d7eb-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="3d7eb-499">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-499">no</span></span>             | <span data-ttu-id="3d7eb-500">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-500">no</span></span>           |
| <span data-ttu-id="3d7eb-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="3d7eb-501">msdyn_start</span></span>                                      | <span data-ttu-id="3d7eb-502">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-502">no</span></span>             | <span data-ttu-id="3d7eb-503">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="3d7eb-504">Project</span><span class="sxs-lookup"><span data-stu-id="3d7eb-504">Project</span></span>

| <span data-ttu-id="3d7eb-505">**Логическое имя**</span><span class="sxs-lookup"><span data-stu-id="3d7eb-505">**Logical name**</span></span>                       | <span data-ttu-id="3d7eb-506">**Можно создать**</span><span class="sxs-lookup"><span data-stu-id="3d7eb-506">**Can create**</span></span> | <span data-ttu-id="3d7eb-507">**Может изменить**</span><span class="sxs-lookup"><span data-stu-id="3d7eb-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="3d7eb-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="3d7eb-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="3d7eb-509">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-509">no</span></span>             | <span data-ttu-id="3d7eb-510">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-510">no</span></span>           |
| <span data-ttu-id="3d7eb-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="3d7eb-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="3d7eb-512">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-512">no</span></span>             | <span data-ttu-id="3d7eb-513">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-513">no</span></span>           |
| <span data-ttu-id="3d7eb-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="3d7eb-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="3d7eb-515">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-515">no</span></span>             | <span data-ttu-id="3d7eb-516">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-516">no</span></span>           |
| <span data-ttu-id="3d7eb-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="3d7eb-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="3d7eb-518">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-518">no</span></span>             | <span data-ttu-id="3d7eb-519">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-519">no</span></span>           |
| <span data-ttu-id="3d7eb-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="3d7eb-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="3d7eb-521">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-521">no</span></span>             | <span data-ttu-id="3d7eb-522">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-522">no</span></span>           |
| <span data-ttu-id="3d7eb-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="3d7eb-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="3d7eb-524">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-524">no</span></span>             | <span data-ttu-id="3d7eb-525">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-525">no</span></span>           |
| <span data-ttu-id="3d7eb-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="3d7eb-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="3d7eb-527">да</span><span class="sxs-lookup"><span data-stu-id="3d7eb-527">yes</span></span>            | <span data-ttu-id="3d7eb-528">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-528">no</span></span>           |
| <span data-ttu-id="3d7eb-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="3d7eb-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="3d7eb-530">да</span><span class="sxs-lookup"><span data-stu-id="3d7eb-530">yes</span></span>            | <span data-ttu-id="3d7eb-531">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-531">no</span></span>           |
| <span data-ttu-id="3d7eb-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="3d7eb-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="3d7eb-533">да</span><span class="sxs-lookup"><span data-stu-id="3d7eb-533">yes</span></span>            | <span data-ttu-id="3d7eb-534">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-534">no</span></span>           |
| <span data-ttu-id="3d7eb-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="3d7eb-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="3d7eb-536">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-536">no</span></span>             | <span data-ttu-id="3d7eb-537">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-537">no</span></span>           |
| <span data-ttu-id="3d7eb-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="3d7eb-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="3d7eb-539">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-539">no</span></span>             | <span data-ttu-id="3d7eb-540">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-540">no</span></span>           |
| <span data-ttu-id="3d7eb-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="3d7eb-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="3d7eb-542">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-542">no</span></span>             | <span data-ttu-id="3d7eb-543">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-543">no</span></span>           |
| <span data-ttu-id="3d7eb-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="3d7eb-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="3d7eb-545">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-545">no</span></span>             | <span data-ttu-id="3d7eb-546">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-546">no</span></span>           |
| <span data-ttu-id="3d7eb-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="3d7eb-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="3d7eb-548">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-548">no</span></span>             | <span data-ttu-id="3d7eb-549">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-549">no</span></span>           |
| <span data-ttu-id="3d7eb-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="3d7eb-550">msdyn_duration</span></span>                         | <span data-ttu-id="3d7eb-551">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-551">no</span></span>             | <span data-ttu-id="3d7eb-552">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-552">no</span></span>           |
| <span data-ttu-id="3d7eb-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="3d7eb-553">msdyn_effort</span></span>                           | <span data-ttu-id="3d7eb-554">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-554">no</span></span>             | <span data-ttu-id="3d7eb-555">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-555">no</span></span>           |
| <span data-ttu-id="3d7eb-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="3d7eb-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="3d7eb-557">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-557">no</span></span>             | <span data-ttu-id="3d7eb-558">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-558">no</span></span>           |
| <span data-ttu-id="3d7eb-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="3d7eb-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="3d7eb-560">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-560">no</span></span>             | <span data-ttu-id="3d7eb-561">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-561">no</span></span>           |
| <span data-ttu-id="3d7eb-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="3d7eb-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="3d7eb-563">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-563">no</span></span>             | <span data-ttu-id="3d7eb-564">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-564">no</span></span>           |
| <span data-ttu-id="3d7eb-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="3d7eb-565">msdyn_finish</span></span>                           | <span data-ttu-id="3d7eb-566">да</span><span class="sxs-lookup"><span data-stu-id="3d7eb-566">yes</span></span>            | <span data-ttu-id="3d7eb-567">да</span><span class="sxs-lookup"><span data-stu-id="3d7eb-567">yes</span></span>          |
| <span data-ttu-id="3d7eb-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="3d7eb-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="3d7eb-569">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-569">no</span></span>             | <span data-ttu-id="3d7eb-570">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-570">no</span></span>           |
| <span data-ttu-id="3d7eb-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="3d7eb-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="3d7eb-572">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-572">no</span></span>             | <span data-ttu-id="3d7eb-573">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-573">no</span></span>           |
| <span data-ttu-id="3d7eb-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="3d7eb-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="3d7eb-575">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-575">no</span></span>             | <span data-ttu-id="3d7eb-576">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-576">no</span></span>           |
| <span data-ttu-id="3d7eb-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="3d7eb-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="3d7eb-578">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-578">no</span></span>             | <span data-ttu-id="3d7eb-579">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-579">no</span></span>           |
| <span data-ttu-id="3d7eb-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="3d7eb-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="3d7eb-581">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-581">no</span></span>             | <span data-ttu-id="3d7eb-582">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-582">no</span></span>           |
| <span data-ttu-id="3d7eb-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="3d7eb-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="3d7eb-584">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-584">no</span></span>             | <span data-ttu-id="3d7eb-585">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-585">no</span></span>           |
| <span data-ttu-id="3d7eb-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="3d7eb-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="3d7eb-587">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-587">no</span></span>             | <span data-ttu-id="3d7eb-588">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-588">no</span></span>           |
| <span data-ttu-id="3d7eb-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="3d7eb-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="3d7eb-590">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-590">no</span></span>             | <span data-ttu-id="3d7eb-591">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-591">no</span></span>           |
| <span data-ttu-id="3d7eb-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="3d7eb-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="3d7eb-593">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-593">no</span></span>             | <span data-ttu-id="3d7eb-594">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-594">no</span></span>           |
| <span data-ttu-id="3d7eb-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="3d7eb-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="3d7eb-596">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-596">no</span></span>             | <span data-ttu-id="3d7eb-597">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-597">no</span></span>           |
| <span data-ttu-id="3d7eb-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="3d7eb-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="3d7eb-599">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-599">no</span></span>             | <span data-ttu-id="3d7eb-600">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-600">no</span></span>           |
| <span data-ttu-id="3d7eb-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="3d7eb-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="3d7eb-602">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-602">no</span></span>             | <span data-ttu-id="3d7eb-603">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-603">no</span></span>           |
| <span data-ttu-id="3d7eb-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="3d7eb-604">msdyn_progress</span></span>                         | <span data-ttu-id="3d7eb-605">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-605">no</span></span>             | <span data-ttu-id="3d7eb-606">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-606">no</span></span>           |
| <span data-ttu-id="3d7eb-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="3d7eb-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="3d7eb-608">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-608">no</span></span>             | <span data-ttu-id="3d7eb-609">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-609">no</span></span>           |
| <span data-ttu-id="3d7eb-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="3d7eb-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="3d7eb-611">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-611">no</span></span>             | <span data-ttu-id="3d7eb-612">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-612">no</span></span>           |
| <span data-ttu-id="3d7eb-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="3d7eb-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="3d7eb-614">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-614">no</span></span>             | <span data-ttu-id="3d7eb-615">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-615">no</span></span>           |
| <span data-ttu-id="3d7eb-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="3d7eb-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="3d7eb-617">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-617">no</span></span>             | <span data-ttu-id="3d7eb-618">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-618">no</span></span>           |
| <span data-ttu-id="3d7eb-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="3d7eb-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="3d7eb-620">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-620">no</span></span>             | <span data-ttu-id="3d7eb-621">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-621">no</span></span>           |
| <span data-ttu-id="3d7eb-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="3d7eb-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="3d7eb-623">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-623">no</span></span>             | <span data-ttu-id="3d7eb-624">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-624">no</span></span>           |
| <span data-ttu-id="3d7eb-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="3d7eb-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="3d7eb-626">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-626">no</span></span>             | <span data-ttu-id="3d7eb-627">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-627">no</span></span>           |
| <span data-ttu-id="3d7eb-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="3d7eb-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="3d7eb-629">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-629">no</span></span>             | <span data-ttu-id="3d7eb-630">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-630">no</span></span>           |
| <span data-ttu-id="3d7eb-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="3d7eb-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="3d7eb-632">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-632">no</span></span>             | <span data-ttu-id="3d7eb-633">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-633">no</span></span>           |
| <span data-ttu-id="3d7eb-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="3d7eb-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="3d7eb-635">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-635">no</span></span>             | <span data-ttu-id="3d7eb-636">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-636">no</span></span>           |
| <span data-ttu-id="3d7eb-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="3d7eb-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="3d7eb-638">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-638">no</span></span>             | <span data-ttu-id="3d7eb-639">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-639">no</span></span>           |
| <span data-ttu-id="3d7eb-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="3d7eb-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="3d7eb-641">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-641">no</span></span>             | <span data-ttu-id="3d7eb-642">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-642">no</span></span>           |
| <span data-ttu-id="3d7eb-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="3d7eb-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="3d7eb-644">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-644">no</span></span>             | <span data-ttu-id="3d7eb-645">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-645">no</span></span>           |
| <span data-ttu-id="3d7eb-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="3d7eb-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="3d7eb-647">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-647">no</span></span>             | <span data-ttu-id="3d7eb-648">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-648">no</span></span>           |
| <span data-ttu-id="3d7eb-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="3d7eb-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="3d7eb-650">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-650">no</span></span>             | <span data-ttu-id="3d7eb-651">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-651">no</span></span>           |
| <span data-ttu-id="3d7eb-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="3d7eb-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="3d7eb-653">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-653">no</span></span>             | <span data-ttu-id="3d7eb-654">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-654">no</span></span>           |
| <span data-ttu-id="3d7eb-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="3d7eb-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="3d7eb-656">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-656">no</span></span>             | <span data-ttu-id="3d7eb-657">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-657">no</span></span>           |
| <span data-ttu-id="3d7eb-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="3d7eb-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="3d7eb-659">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-659">no</span></span>             | <span data-ttu-id="3d7eb-660">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-660">no</span></span>           |
| <span data-ttu-id="3d7eb-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="3d7eb-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="3d7eb-662">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-662">no</span></span>             | <span data-ttu-id="3d7eb-663">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-663">no</span></span>           |
| <span data-ttu-id="3d7eb-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="3d7eb-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="3d7eb-665">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-665">no</span></span>             | <span data-ttu-id="3d7eb-666">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-666">no</span></span>           |
| <span data-ttu-id="3d7eb-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="3d7eb-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="3d7eb-668">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-668">no</span></span>             | <span data-ttu-id="3d7eb-669">нет</span><span class="sxs-lookup"><span data-stu-id="3d7eb-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="3d7eb-670">Известные проблемы и ограничения</span><span class="sxs-lookup"><span data-stu-id="3d7eb-670">Limitations and known issues</span></span>
<span data-ttu-id="3d7eb-671">Ниже приводится список ограничений и известных проблем:</span><span class="sxs-lookup"><span data-stu-id="3d7eb-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="3d7eb-672">API расписания могут использоваться только **пользователями с лицензией Microsoft Project.**</span><span class="sxs-lookup"><span data-stu-id="3d7eb-672">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="3d7eb-673">Их не могут использовать:</span><span class="sxs-lookup"><span data-stu-id="3d7eb-673">They can't be used by:</span></span>
    - <span data-ttu-id="3d7eb-674">Пользователи приложений</span><span class="sxs-lookup"><span data-stu-id="3d7eb-674">Application users</span></span>
    - <span data-ttu-id="3d7eb-675">Системные пользователи</span><span class="sxs-lookup"><span data-stu-id="3d7eb-675">System users</span></span>
    - <span data-ttu-id="3d7eb-676">Пользователи-интеграторы</span><span class="sxs-lookup"><span data-stu-id="3d7eb-676">Integration users</span></span>
    - <span data-ttu-id="3d7eb-677">Другие пользователи, у которых нет необходимой лицензии</span><span class="sxs-lookup"><span data-stu-id="3d7eb-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="3d7eb-678">У каждого **OperationSet** может быть не более 100 операций.</span><span class="sxs-lookup"><span data-stu-id="3d7eb-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="3d7eb-679">У каждого пользователя может быть не более 10 открытых **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="3d7eb-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="3d7eb-680">В настоящее время Project Operations поддерживает не более 500 общих задач в проекте.</span><span class="sxs-lookup"><span data-stu-id="3d7eb-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="3d7eb-681">Статус сбоя и журналы ошибок в **OperationSet** в настоящее время недоступны.</span><span class="sxs-lookup"><span data-stu-id="3d7eb-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- [<span data-ttu-id="3d7eb-682">Пределы и границы проектов и задач</span><span class="sxs-lookup"><span data-stu-id="3d7eb-682">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="3d7eb-683">Обработка ошибок</span><span class="sxs-lookup"><span data-stu-id="3d7eb-683">Error handling</span></span>

   - <span data-ttu-id="3d7eb-684">Чтобы просмотреть ошибки, сгенерированные из наборов операций, перейдите к **Параметры** \> **Интеграция расписания** \> **Наборы операций**.</span><span class="sxs-lookup"><span data-stu-id="3d7eb-684">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="3d7eb-685">Чтобы просмотреть ошибки, сгенерированные службой планирования проекта, перейдите к **Параметры** \> **Интеграция расписания** \> **Журналы ошибок PSS**.</span><span class="sxs-lookup"><span data-stu-id="3d7eb-685">To review errors generated from the Project Scheduling Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="3d7eb-686">Пример сценария</span><span class="sxs-lookup"><span data-stu-id="3d7eb-686">Sample scenario</span></span>

<span data-ttu-id="3d7eb-687">В этом сценарии вы создадите проект, участника команды, четыре задачи и два назначения ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3d7eb-687">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="3d7eb-688">Затем вы обновите одну задачу, обновите проект, удалите одну задачу, удалите одно назначение ресурса и создадите зависимость задачи.</span><span class="sxs-lookup"><span data-stu-id="3d7eb-688">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

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

## <a name="additional-samples"></a><span data-ttu-id="3d7eb-689">Дополнительные примеры</span><span class="sxs-lookup"><span data-stu-id="3d7eb-689">Additional samples</span></span>

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
