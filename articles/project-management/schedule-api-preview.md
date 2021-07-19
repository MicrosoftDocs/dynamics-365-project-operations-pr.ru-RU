---
title: Использование API расписания проекта для выполнения операций с сущностями планирования
description: В этом разделе предоставлена информация и примеры по использованию API для расписания проекта.
author: sigitac
ms.date: 06/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4915261c08a3271a919e04084e92a14b297c1b35
ms.sourcegitcommit: 2f16c2bc7c8350676a6a380c61fffa9958db6a0b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/22/2021
ms.locfileid: "6293243"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="5e337-103">Использование API расписания проекта для выполнения операций с сущностями планирования</span><span class="sxs-lookup"><span data-stu-id="5e337-103">Use Project schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="5e337-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="5e337-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="5e337-105">Некоторые или все функции, описанные в этой статье, доступны в рамках предварительного выпуска.</span><span class="sxs-lookup"><span data-stu-id="5e337-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="5e337-106">Содержимое и функциональность могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="5e337-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="5e337-107">Сущности планирования</span><span class="sxs-lookup"><span data-stu-id="5e337-107">Scheduling entities</span></span>

<span data-ttu-id="5e337-108">API расписания проекта предоставляют возможность выполнять операции создания, обновления и удаления с помощью **сущностей планирования**.</span><span class="sxs-lookup"><span data-stu-id="5e337-108">Project schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="5e337-109">Управление этими сущностями осуществляется через механизм планирования в проекте для Интернета.</span><span class="sxs-lookup"><span data-stu-id="5e337-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="5e337-110">Операции создания, обновления и удаления с помощью **сущностей планирования** были ограничены в ранних выпусках Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="5e337-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="5e337-111">В следующей таблице представлен полный список сущностей расписания проекта.</span><span class="sxs-lookup"><span data-stu-id="5e337-111">The following table provides a full list of the Project schedule entities.</span></span>

| <span data-ttu-id="5e337-112">Имя сущности</span><span class="sxs-lookup"><span data-stu-id="5e337-112">Entity name</span></span>  | <span data-ttu-id="5e337-113">Логическое имя сущности</span><span class="sxs-lookup"><span data-stu-id="5e337-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="5e337-114">Project</span><span class="sxs-lookup"><span data-stu-id="5e337-114">Project</span></span> | <span data-ttu-id="5e337-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="5e337-115">msdyn_project</span></span> |
| <span data-ttu-id="5e337-116">Задача проекта</span><span class="sxs-lookup"><span data-stu-id="5e337-116">Project Task</span></span>  | <span data-ttu-id="5e337-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="5e337-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="5e337-118">Зависимость задач проекта</span><span class="sxs-lookup"><span data-stu-id="5e337-118">Project Task Dependency</span></span>  | <span data-ttu-id="5e337-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="5e337-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="5e337-120">Назначение ресурса</span><span class="sxs-lookup"><span data-stu-id="5e337-120">Resource Assignment</span></span> | <span data-ttu-id="5e337-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="5e337-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="5e337-122">Группа проекта</span><span class="sxs-lookup"><span data-stu-id="5e337-122">Project Bucket</span></span>  | <span data-ttu-id="5e337-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="5e337-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="5e337-124">Участник проектной группы</span><span class="sxs-lookup"><span data-stu-id="5e337-124">Project Team Member</span></span> | <span data-ttu-id="5e337-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="5e337-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="5e337-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="5e337-126">OperationSet</span></span>

<span data-ttu-id="5e337-127">OperationSet — это шаблон единицы работы, который можно использовать, когда в рамках транзакции необходимо обработать несколько запросов, влияющих на расписание.</span><span class="sxs-lookup"><span data-stu-id="5e337-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="project-schedule-apis"></a><span data-ttu-id="5e337-128">API расписания проектов</span><span class="sxs-lookup"><span data-stu-id="5e337-128">Project schedule APIs</span></span>

<span data-ttu-id="5e337-129">Ниже приводится список текущих API для расписания проекта.</span><span class="sxs-lookup"><span data-stu-id="5e337-129">The following is a list of current Project schedule APIs.</span></span>

- <span data-ttu-id="5e337-130">**msdyn_CreateProjectV1**: этот API можно использовать для создания проекта.</span><span class="sxs-lookup"><span data-stu-id="5e337-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="5e337-131">Немедленно создается проект и группа проекта по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5e337-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="5e337-132">**msdyn_CreateTeamMemberV1**: этот API можно использовать для создания участника рабочей группы проекта.</span><span class="sxs-lookup"><span data-stu-id="5e337-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="5e337-133">Запись участника рабочей группы создается немедленно.</span><span class="sxs-lookup"><span data-stu-id="5e337-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="5e337-134">**msdyn_CreateOperationSetV1**: этот API можно использовать для планирования нескольких запросов, которые должны выполняться в рамках транзакции.</span><span class="sxs-lookup"><span data-stu-id="5e337-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="5e337-135">**msdyn_PSSCreateV1**: этот API можно использовать для создания сущности.</span><span class="sxs-lookup"><span data-stu-id="5e337-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="5e337-136">Сущность может быть любой из сущностей планирования проекта, поддерживающих операцию создания.</span><span class="sxs-lookup"><span data-stu-id="5e337-136">The entity can be any of the Project scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="5e337-137">**msdyn_PSSUpdateV1**: этот API можно использовать для обновления сущности.</span><span class="sxs-lookup"><span data-stu-id="5e337-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="5e337-138">Сущность может быть любой из сущностей планирования проекта, поддерживающих операцию обновления.</span><span class="sxs-lookup"><span data-stu-id="5e337-138">The entity can be any of the Project scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="5e337-139">**msdyn_PSSDeleteV1**: этот API можно использовать для удаления сущности.</span><span class="sxs-lookup"><span data-stu-id="5e337-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="5e337-140">Сущность может быть любой из сущностей планирования проекта, поддерживающих операцию удаления.</span><span class="sxs-lookup"><span data-stu-id="5e337-140">The entity can be any of the Project scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="5e337-141">**msdyn_ExecuteOperationSetV1**: этот API используется для выполнения всех операций в рамках данного набора операций.</span><span class="sxs-lookup"><span data-stu-id="5e337-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-project-schedule-apis-with-operationset"></a><span data-ttu-id="5e337-142">Использование API расписания проекта с OperationSet</span><span class="sxs-lookup"><span data-stu-id="5e337-142">Using Project schedule APIs with OperationSet</span></span>

<span data-ttu-id="5e337-143">Поскольку записи **CreateProjectV1** и **CreateTeamMemberV1** создаются мгновенно, эти API нельзя использовать в **OperationSet** напрямую.</span><span class="sxs-lookup"><span data-stu-id="5e337-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="5e337-144">Однако вы можете использовать API для создания необходимых записей, создайте **OperationSet**, а затем используйте эти предварительно созданные записи в **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="5e337-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="5e337-145">Поддерживаемые операции</span><span class="sxs-lookup"><span data-stu-id="5e337-145">Supported operations</span></span>

| <span data-ttu-id="5e337-146">Сущность планирования</span><span class="sxs-lookup"><span data-stu-id="5e337-146">Scheduling entity</span></span> | <span data-ttu-id="5e337-147">Создание</span><span class="sxs-lookup"><span data-stu-id="5e337-147">Create</span></span> | <span data-ttu-id="5e337-148">При обновлении</span><span class="sxs-lookup"><span data-stu-id="5e337-148">Update</span></span> | <span data-ttu-id="5e337-149">DELETE</span><span class="sxs-lookup"><span data-stu-id="5e337-149">Delete</span></span> | <span data-ttu-id="5e337-150">Важные замечания</span><span class="sxs-lookup"><span data-stu-id="5e337-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="5e337-151">Задача проекта</span><span class="sxs-lookup"><span data-stu-id="5e337-151">Project task</span></span> | <span data-ttu-id="5e337-152">Да</span><span class="sxs-lookup"><span data-stu-id="5e337-152">Yes</span></span> | <span data-ttu-id="5e337-153">Да</span><span class="sxs-lookup"><span data-stu-id="5e337-153">Yes</span></span> | <span data-ttu-id="5e337-154">Да</span><span class="sxs-lookup"><span data-stu-id="5e337-154">Yes</span></span> | <span data-ttu-id="5e337-155">Без доступа</span><span class="sxs-lookup"><span data-stu-id="5e337-155">None</span></span> |
| <span data-ttu-id="5e337-156">Зависимость задач проекта</span><span class="sxs-lookup"><span data-stu-id="5e337-156">Project task dependency</span></span> | <span data-ttu-id="5e337-157">Да</span><span class="sxs-lookup"><span data-stu-id="5e337-157">Yes</span></span> | <span data-ttu-id="5e337-158">Да</span><span class="sxs-lookup"><span data-stu-id="5e337-158">Yes</span></span> | | <span data-ttu-id="5e337-159">Записи о зависимостях задач проекта не обновляются.</span><span class="sxs-lookup"><span data-stu-id="5e337-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="5e337-160">Вместо этого можно удалить старую запись и создать новую.</span><span class="sxs-lookup"><span data-stu-id="5e337-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="5e337-161">Назначение ресурса</span><span class="sxs-lookup"><span data-stu-id="5e337-161">Resource assignment</span></span> | <span data-ttu-id="5e337-162">Да</span><span class="sxs-lookup"><span data-stu-id="5e337-162">Yes</span></span> | <span data-ttu-id="5e337-163">Да</span><span class="sxs-lookup"><span data-stu-id="5e337-163">Yes</span></span> | | <span data-ttu-id="5e337-164">Не поддерживаются операции со следующими полями: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** и **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="5e337-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="5e337-165">Записи о назначении ресурсов не обновляются.</span><span class="sxs-lookup"><span data-stu-id="5e337-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="5e337-166">Вместо этого можно удалить старую запись и создать новую.</span><span class="sxs-lookup"><span data-stu-id="5e337-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="5e337-167">Группа проекта</span><span class="sxs-lookup"><span data-stu-id="5e337-167">Project bucket</span></span> | <span data-ttu-id="5e337-168">Н/Д</span><span class="sxs-lookup"><span data-stu-id="5e337-168">N/A</span></span> | <span data-ttu-id="5e337-169">Н/Д</span><span class="sxs-lookup"><span data-stu-id="5e337-169">N/A</span></span> | <span data-ttu-id="5e337-170">Н/Д</span><span class="sxs-lookup"><span data-stu-id="5e337-170">N/A</span></span> | <span data-ttu-id="5e337-171">Сегмент по умолчанию создается с помощью API **CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="5e337-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="5e337-172">Участник проектной группы</span><span class="sxs-lookup"><span data-stu-id="5e337-172">Project team member</span></span> | <span data-ttu-id="5e337-173">Да</span><span class="sxs-lookup"><span data-stu-id="5e337-173">Yes</span></span> | <span data-ttu-id="5e337-174">Да</span><span class="sxs-lookup"><span data-stu-id="5e337-174">Yes</span></span> | <span data-ttu-id="5e337-175">Да</span><span class="sxs-lookup"><span data-stu-id="5e337-175">Yes</span></span> | <span data-ttu-id="5e337-176">Для операции создания используйте API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="5e337-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="5e337-177">Project</span><span class="sxs-lookup"><span data-stu-id="5e337-177">Project</span></span> | <span data-ttu-id="5e337-178">Да</span><span class="sxs-lookup"><span data-stu-id="5e337-178">Yes</span></span> | <span data-ttu-id="5e337-179">Да</span><span class="sxs-lookup"><span data-stu-id="5e337-179">Yes</span></span> | <span data-ttu-id="5e337-180">Н/Д</span><span class="sxs-lookup"><span data-stu-id="5e337-180">N/A</span></span> | <span data-ttu-id="5e337-181">Не поддерживаются операции со следующими полями: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** и **Duration**.</span><span class="sxs-lookup"><span data-stu-id="5e337-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="5e337-182">Эти API можно вызывать с объектами сущности, которые включают настраиваемые поля.</span><span class="sxs-lookup"><span data-stu-id="5e337-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="5e337-183">Свойство кода необязательно.</span><span class="sxs-lookup"><span data-stu-id="5e337-183">The ID property is optional.</span></span> <span data-ttu-id="5e337-184">Если оно указано, система пытается его использовать и выдает исключение, если оно не может быть использовано.</span><span class="sxs-lookup"><span data-stu-id="5e337-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="5e337-185">Если оно не указано, система его сгенерирует.</span><span class="sxs-lookup"><span data-stu-id="5e337-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="5e337-186">Запрещенные поля</span><span class="sxs-lookup"><span data-stu-id="5e337-186">Restricted fields</span></span>

<span data-ttu-id="5e337-187">В следующих таблицах определены поля, которые защищены от **Создать** и **Изменить.**</span><span class="sxs-lookup"><span data-stu-id="5e337-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="5e337-188">Задача проекта</span><span class="sxs-lookup"><span data-stu-id="5e337-188">Project task</span></span>

| <span data-ttu-id="5e337-189">**Логическое имя**</span><span class="sxs-lookup"><span data-stu-id="5e337-189">**Logical name**</span></span>                       | <span data-ttu-id="5e337-190">**Можно создать**</span><span class="sxs-lookup"><span data-stu-id="5e337-190">**Can create**</span></span> | <span data-ttu-id="5e337-191">**Может изменить**</span><span class="sxs-lookup"><span data-stu-id="5e337-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="5e337-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="5e337-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="5e337-193">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-193">no</span></span>             | <span data-ttu-id="5e337-194">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-194">no</span></span>               |
| <span data-ttu-id="5e337-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="5e337-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="5e337-196">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-196">no</span></span>             | <span data-ttu-id="5e337-197">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-197">no</span></span>               |
| <span data-ttu-id="5e337-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="5e337-198">msdyn_actualend</span></span>                        | <span data-ttu-id="5e337-199">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-199">no</span></span>             | <span data-ttu-id="5e337-200">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-200">no</span></span>               |
| <span data-ttu-id="5e337-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="5e337-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="5e337-202">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-202">no</span></span>             | <span data-ttu-id="5e337-203">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-203">no</span></span>               |
| <span data-ttu-id="5e337-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="5e337-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="5e337-205">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-205">no</span></span>             | <span data-ttu-id="5e337-206">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-206">no</span></span>               |
| <span data-ttu-id="5e337-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="5e337-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="5e337-208">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-208">no</span></span>             | <span data-ttu-id="5e337-209">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-209">no</span></span>               |
| <span data-ttu-id="5e337-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="5e337-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="5e337-211">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-211">no</span></span>             | <span data-ttu-id="5e337-212">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-212">no</span></span>               |
| <span data-ttu-id="5e337-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="5e337-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="5e337-214">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-214">no</span></span>             | <span data-ttu-id="5e337-215">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-215">no</span></span>               |
| <span data-ttu-id="5e337-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="5e337-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="5e337-217">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-217">no</span></span>             | <span data-ttu-id="5e337-218">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-218">no</span></span>               |
| <span data-ttu-id="5e337-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="5e337-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="5e337-220">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-220">no</span></span>             | <span data-ttu-id="5e337-221">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-221">no</span></span>               |
| <span data-ttu-id="5e337-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="5e337-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="5e337-223">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-223">no</span></span>             | <span data-ttu-id="5e337-224">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-224">no</span></span>               |
| <span data-ttu-id="5e337-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="5e337-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="5e337-226">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-226">no</span></span>             | <span data-ttu-id="5e337-227">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-227">no</span></span>               |
| <span data-ttu-id="5e337-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="5e337-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="5e337-229">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-229">no</span></span>             | <span data-ttu-id="5e337-230">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-230">no</span></span>               |
| <span data-ttu-id="5e337-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="5e337-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="5e337-232">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-232">no</span></span>             | <span data-ttu-id="5e337-233">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-233">no</span></span>               |
| <span data-ttu-id="5e337-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="5e337-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="5e337-235">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-235">no</span></span>             | <span data-ttu-id="5e337-236">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-236">no</span></span>               |
| <span data-ttu-id="5e337-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="5e337-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="5e337-238">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-238">no</span></span>             | <span data-ttu-id="5e337-239">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-239">no</span></span>               |
| <span data-ttu-id="5e337-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="5e337-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="5e337-241">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-241">no</span></span>             | <span data-ttu-id="5e337-242">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-242">no</span></span>               |
| <span data-ttu-id="5e337-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="5e337-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="5e337-244">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-244">no</span></span>             | <span data-ttu-id="5e337-245">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-245">no</span></span>               |
| <span data-ttu-id="5e337-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="5e337-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="5e337-247">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-247">no</span></span>             | <span data-ttu-id="5e337-248">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-248">no</span></span>               |
| <span data-ttu-id="5e337-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="5e337-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="5e337-250">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-250">no</span></span>             | <span data-ttu-id="5e337-251">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-251">no</span></span>               |
| <span data-ttu-id="5e337-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="5e337-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="5e337-253">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-253">no</span></span>             | <span data-ttu-id="5e337-254">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-254">no</span></span>               |
| <span data-ttu-id="5e337-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="5e337-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="5e337-256">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-256">no</span></span>             | <span data-ttu-id="5e337-257">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-257">no</span></span>               |
| <span data-ttu-id="5e337-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="5e337-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="5e337-259">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-259">no</span></span>             | <span data-ttu-id="5e337-260">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-260">no</span></span>               |
| <span data-ttu-id="5e337-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="5e337-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="5e337-262">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-262">no</span></span>             | <span data-ttu-id="5e337-263">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-263">no</span></span>               |
| <span data-ttu-id="5e337-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="5e337-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="5e337-265">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-265">no</span></span>             | <span data-ttu-id="5e337-266">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-266">no</span></span>               |
| <span data-ttu-id="5e337-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="5e337-267">msdyn_progress</span></span>                         | <span data-ttu-id="5e337-268">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-268">no</span></span>             | <span data-ttu-id="5e337-269">нет (да для P4W)</span><span class="sxs-lookup"><span data-stu-id="5e337-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="5e337-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="5e337-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="5e337-271">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-271">no</span></span>             | <span data-ttu-id="5e337-272">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-272">no</span></span>               |
| <span data-ttu-id="5e337-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="5e337-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="5e337-274">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-274">no</span></span>             | <span data-ttu-id="5e337-275">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-275">no</span></span>               |
| <span data-ttu-id="5e337-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="5e337-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="5e337-277">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-277">no</span></span>             | <span data-ttu-id="5e337-278">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-278">no</span></span>               |
| <span data-ttu-id="5e337-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="5e337-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="5e337-280">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-280">no</span></span>             | <span data-ttu-id="5e337-281">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-281">no</span></span>               |
| <span data-ttu-id="5e337-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="5e337-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="5e337-283">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-283">no</span></span>             | <span data-ttu-id="5e337-284">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-284">no</span></span>               |
| <span data-ttu-id="5e337-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="5e337-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="5e337-286">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-286">no</span></span>             | <span data-ttu-id="5e337-287">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-287">no</span></span>               |
| <span data-ttu-id="5e337-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="5e337-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="5e337-289">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-289">no</span></span>             | <span data-ttu-id="5e337-290">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-290">no</span></span>               |
| <span data-ttu-id="5e337-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="5e337-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="5e337-292">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-292">no</span></span>             | <span data-ttu-id="5e337-293">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-293">no</span></span>               |
| <span data-ttu-id="5e337-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="5e337-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="5e337-295">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-295">no</span></span>             | <span data-ttu-id="5e337-296">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-296">no</span></span>               |
| <span data-ttu-id="5e337-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="5e337-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="5e337-298">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-298">no</span></span>             | <span data-ttu-id="5e337-299">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-299">no</span></span>               |
| <span data-ttu-id="5e337-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="5e337-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="5e337-301">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-301">no</span></span>             | <span data-ttu-id="5e337-302">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-302">no</span></span>               |
| <span data-ttu-id="5e337-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="5e337-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="5e337-304">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-304">no</span></span>             | <span data-ttu-id="5e337-305">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-305">no</span></span>               |
| <span data-ttu-id="5e337-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="5e337-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="5e337-307">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-307">no</span></span>             | <span data-ttu-id="5e337-308">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-308">no</span></span>               |
| <span data-ttu-id="5e337-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="5e337-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="5e337-310">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-310">no</span></span>             | <span data-ttu-id="5e337-311">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-311">no</span></span>               |
| <span data-ttu-id="5e337-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="5e337-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="5e337-313">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-313">no</span></span>             | <span data-ttu-id="5e337-314">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-314">no</span></span>               |
| <span data-ttu-id="5e337-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="5e337-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="5e337-316">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-316">no</span></span>             | <span data-ttu-id="5e337-317">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-317">no</span></span>               |
| <span data-ttu-id="5e337-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="5e337-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="5e337-319">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-319">no</span></span>             | <span data-ttu-id="5e337-320">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-320">no</span></span>               |
| <span data-ttu-id="5e337-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="5e337-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="5e337-322">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-322">no</span></span>             | <span data-ttu-id="5e337-323">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-323">no</span></span>               |
| <span data-ttu-id="5e337-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="5e337-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="5e337-325">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-325">no</span></span>             | <span data-ttu-id="5e337-326">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-326">no</span></span>               |
| <span data-ttu-id="5e337-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="5e337-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="5e337-328">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-328">no</span></span>             | <span data-ttu-id="5e337-329">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-329">no</span></span>               |
| <span data-ttu-id="5e337-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="5e337-330">msdyn_summary</span></span>                          | <span data-ttu-id="5e337-331">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-331">no</span></span>             | <span data-ttu-id="5e337-332">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-332">no</span></span>               |
| <span data-ttu-id="5e337-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="5e337-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="5e337-334">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-334">no</span></span>             | <span data-ttu-id="5e337-335">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-335">no</span></span>               |
| <span data-ttu-id="5e337-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="5e337-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="5e337-337">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-337">no</span></span>             | <span data-ttu-id="5e337-338">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="5e337-339">Зависимость задач проекта</span><span class="sxs-lookup"><span data-stu-id="5e337-339">Project task dependency</span></span>

| <span data-ttu-id="5e337-340">**Логическое имя**</span><span class="sxs-lookup"><span data-stu-id="5e337-340">**Logical name**</span></span>              | <span data-ttu-id="5e337-341">**Можно создать**</span><span class="sxs-lookup"><span data-stu-id="5e337-341">**Can create**</span></span> | <span data-ttu-id="5e337-342">**Может изменить**</span><span class="sxs-lookup"><span data-stu-id="5e337-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="5e337-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="5e337-343">msdyn_linktype</span></span>                | <span data-ttu-id="5e337-344">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-344">no</span></span>             | <span data-ttu-id="5e337-345">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-345">no</span></span>           |
| <span data-ttu-id="5e337-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="5e337-346">msdyn_linktypename</span></span>            | <span data-ttu-id="5e337-347">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-347">no</span></span>             | <span data-ttu-id="5e337-348">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-348">no</span></span>           |
| <span data-ttu-id="5e337-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="5e337-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="5e337-350">да</span><span class="sxs-lookup"><span data-stu-id="5e337-350">yes</span></span>            | <span data-ttu-id="5e337-351">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-351">no</span></span>           |
| <span data-ttu-id="5e337-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="5e337-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="5e337-353">да</span><span class="sxs-lookup"><span data-stu-id="5e337-353">yes</span></span>            | <span data-ttu-id="5e337-354">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-354">no</span></span>           |
| <span data-ttu-id="5e337-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="5e337-355">msdyn_project</span></span>                 | <span data-ttu-id="5e337-356">да</span><span class="sxs-lookup"><span data-stu-id="5e337-356">yes</span></span>            | <span data-ttu-id="5e337-357">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-357">no</span></span>           |
| <span data-ttu-id="5e337-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="5e337-358">msdyn_projectname</span></span>             | <span data-ttu-id="5e337-359">да</span><span class="sxs-lookup"><span data-stu-id="5e337-359">yes</span></span>            | <span data-ttu-id="5e337-360">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-360">no</span></span>           |
| <span data-ttu-id="5e337-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="5e337-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="5e337-362">да</span><span class="sxs-lookup"><span data-stu-id="5e337-362">yes</span></span>            | <span data-ttu-id="5e337-363">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-363">no</span></span>           |
| <span data-ttu-id="5e337-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="5e337-364">msdyn_successortask</span></span>           | <span data-ttu-id="5e337-365">да</span><span class="sxs-lookup"><span data-stu-id="5e337-365">yes</span></span>            | <span data-ttu-id="5e337-366">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-366">no</span></span>           |
| <span data-ttu-id="5e337-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="5e337-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="5e337-368">да</span><span class="sxs-lookup"><span data-stu-id="5e337-368">yes</span></span>            | <span data-ttu-id="5e337-369">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="5e337-370">Назначение ресурса</span><span class="sxs-lookup"><span data-stu-id="5e337-370">Resource assignment</span></span>

| <span data-ttu-id="5e337-371">**Логическое имя**</span><span class="sxs-lookup"><span data-stu-id="5e337-371">**Logical name**</span></span>             | <span data-ttu-id="5e337-372">**Можно создать**</span><span class="sxs-lookup"><span data-stu-id="5e337-372">**Can create**</span></span> | <span data-ttu-id="5e337-373">**Может изменить**</span><span class="sxs-lookup"><span data-stu-id="5e337-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="5e337-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="5e337-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="5e337-375">да</span><span class="sxs-lookup"><span data-stu-id="5e337-375">yes</span></span>            | <span data-ttu-id="5e337-376">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-376">no</span></span>           |
| <span data-ttu-id="5e337-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="5e337-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="5e337-378">да</span><span class="sxs-lookup"><span data-stu-id="5e337-378">yes</span></span>            | <span data-ttu-id="5e337-379">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-379">no</span></span>           |
| <span data-ttu-id="5e337-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="5e337-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="5e337-381">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-381">no</span></span>             | <span data-ttu-id="5e337-382">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-382">no</span></span>           |
| <span data-ttu-id="5e337-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="5e337-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="5e337-384">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-384">no</span></span>             | <span data-ttu-id="5e337-385">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-385">no</span></span>           |
| <span data-ttu-id="5e337-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="5e337-386">msdyn_committype</span></span>             | <span data-ttu-id="5e337-387">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-387">no</span></span>             | <span data-ttu-id="5e337-388">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-388">no</span></span>           |
| <span data-ttu-id="5e337-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="5e337-389">msdyn_committypename</span></span>         | <span data-ttu-id="5e337-390">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-390">no</span></span>             | <span data-ttu-id="5e337-391">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-391">no</span></span>           |
| <span data-ttu-id="5e337-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="5e337-392">msdyn_effort</span></span>                 | <span data-ttu-id="5e337-393">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-393">no</span></span>             | <span data-ttu-id="5e337-394">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-394">no</span></span>           |
| <span data-ttu-id="5e337-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="5e337-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="5e337-396">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-396">no</span></span>             | <span data-ttu-id="5e337-397">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-397">no</span></span>           |
| <span data-ttu-id="5e337-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="5e337-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="5e337-399">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-399">no</span></span>             | <span data-ttu-id="5e337-400">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-400">no</span></span>           |
| <span data-ttu-id="5e337-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="5e337-401">msdyn_finish</span></span>                 | <span data-ttu-id="5e337-402">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-402">no</span></span>             | <span data-ttu-id="5e337-403">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-403">no</span></span>           |
| <span data-ttu-id="5e337-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="5e337-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="5e337-405">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-405">no</span></span>             | <span data-ttu-id="5e337-406">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-406">no</span></span>           |
| <span data-ttu-id="5e337-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="5e337-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="5e337-408">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-408">no</span></span>             | <span data-ttu-id="5e337-409">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-409">no</span></span>           |
| <span data-ttu-id="5e337-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="5e337-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="5e337-411">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-411">no</span></span>             | <span data-ttu-id="5e337-412">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-412">no</span></span>           |
| <span data-ttu-id="5e337-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="5e337-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="5e337-414">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-414">no</span></span>             | <span data-ttu-id="5e337-415">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-415">no</span></span>           |
| <span data-ttu-id="5e337-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="5e337-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="5e337-417">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-417">no</span></span>             | <span data-ttu-id="5e337-418">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-418">no</span></span>           |
| <span data-ttu-id="5e337-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="5e337-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="5e337-420">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-420">no</span></span>             | <span data-ttu-id="5e337-421">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-421">no</span></span>           |
| <span data-ttu-id="5e337-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="5e337-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="5e337-423">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-423">no</span></span>             | <span data-ttu-id="5e337-424">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-424">no</span></span>           |
| <span data-ttu-id="5e337-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="5e337-425">msdyn_projectid</span></span>              | <span data-ttu-id="5e337-426">да</span><span class="sxs-lookup"><span data-stu-id="5e337-426">yes</span></span>            | <span data-ttu-id="5e337-427">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-427">no</span></span>           |
| <span data-ttu-id="5e337-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="5e337-428">msdyn_projectidname</span></span>          | <span data-ttu-id="5e337-429">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-429">no</span></span>             | <span data-ttu-id="5e337-430">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-430">no</span></span>           |
| <span data-ttu-id="5e337-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="5e337-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="5e337-432">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-432">no</span></span>             | <span data-ttu-id="5e337-433">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-433">no</span></span>           |
| <span data-ttu-id="5e337-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="5e337-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="5e337-435">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-435">no</span></span>             | <span data-ttu-id="5e337-436">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-436">no</span></span>           |
| <span data-ttu-id="5e337-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="5e337-437">msdyn_start</span></span>                  | <span data-ttu-id="5e337-438">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-438">no</span></span>             | <span data-ttu-id="5e337-439">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-439">no</span></span>           |
| <span data-ttu-id="5e337-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="5e337-440">msdyn_taskid</span></span>                 | <span data-ttu-id="5e337-441">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-441">no</span></span>             | <span data-ttu-id="5e337-442">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-442">no</span></span>           |
| <span data-ttu-id="5e337-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="5e337-443">msdyn_taskidname</span></span>             | <span data-ttu-id="5e337-444">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-444">no</span></span>             | <span data-ttu-id="5e337-445">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-445">no</span></span>           |
| <span data-ttu-id="5e337-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="5e337-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="5e337-447">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-447">no</span></span>             | <span data-ttu-id="5e337-448">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="5e337-449">Участник проектной группы</span><span class="sxs-lookup"><span data-stu-id="5e337-449">Project team member</span></span>

| <span data-ttu-id="5e337-450">**Логическое имя**</span><span class="sxs-lookup"><span data-stu-id="5e337-450">**Logical name**</span></span>                                 | <span data-ttu-id="5e337-451">**Можно создать**</span><span class="sxs-lookup"><span data-stu-id="5e337-451">**Can create**</span></span> | <span data-ttu-id="5e337-452">**Может изменить**</span><span class="sxs-lookup"><span data-stu-id="5e337-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="5e337-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="5e337-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="5e337-454">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-454">no</span></span>             | <span data-ttu-id="5e337-455">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-455">no</span></span>           |
| <span data-ttu-id="5e337-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="5e337-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="5e337-457">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-457">no</span></span>             | <span data-ttu-id="5e337-458">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-458">no</span></span>           |
| <span data-ttu-id="5e337-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="5e337-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="5e337-460">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-460">no</span></span>             | <span data-ttu-id="5e337-461">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-461">no</span></span>           |
| <span data-ttu-id="5e337-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="5e337-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="5e337-463">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-463">no</span></span>             | <span data-ttu-id="5e337-464">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-464">no</span></span>           |
| <span data-ttu-id="5e337-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="5e337-465">msdyn_effort</span></span>                                     | <span data-ttu-id="5e337-466">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-466">no</span></span>             | <span data-ttu-id="5e337-467">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-467">no</span></span>           |
| <span data-ttu-id="5e337-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="5e337-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="5e337-469">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-469">no</span></span>             | <span data-ttu-id="5e337-470">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-470">no</span></span>           |
| <span data-ttu-id="5e337-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="5e337-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="5e337-472">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-472">no</span></span>             | <span data-ttu-id="5e337-473">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-473">no</span></span>           |
| <span data-ttu-id="5e337-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="5e337-474">msdyn_finish</span></span>                                     | <span data-ttu-id="5e337-475">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-475">no</span></span>             | <span data-ttu-id="5e337-476">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-476">no</span></span>           |
| <span data-ttu-id="5e337-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="5e337-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="5e337-478">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-478">no</span></span>             | <span data-ttu-id="5e337-479">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-479">no</span></span>           |
| <span data-ttu-id="5e337-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="5e337-480">msdyn_hours</span></span>                                      | <span data-ttu-id="5e337-481">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-481">no</span></span>             | <span data-ttu-id="5e337-482">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-482">no</span></span>           |
| <span data-ttu-id="5e337-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="5e337-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="5e337-484">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-484">no</span></span>             | <span data-ttu-id="5e337-485">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-485">no</span></span>           |
| <span data-ttu-id="5e337-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="5e337-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="5e337-487">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-487">no</span></span>             | <span data-ttu-id="5e337-488">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-488">no</span></span>           |
| <span data-ttu-id="5e337-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="5e337-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="5e337-490">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-490">no</span></span>             | <span data-ttu-id="5e337-491">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-491">no</span></span>           |
| <span data-ttu-id="5e337-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="5e337-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="5e337-493">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-493">no</span></span>             | <span data-ttu-id="5e337-494">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-494">no</span></span>           |
| <span data-ttu-id="5e337-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="5e337-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="5e337-496">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-496">no</span></span>             | <span data-ttu-id="5e337-497">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-497">no</span></span>           |
| <span data-ttu-id="5e337-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="5e337-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="5e337-499">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-499">no</span></span>             | <span data-ttu-id="5e337-500">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-500">no</span></span>           |
| <span data-ttu-id="5e337-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="5e337-501">msdyn_start</span></span>                                      | <span data-ttu-id="5e337-502">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-502">no</span></span>             | <span data-ttu-id="5e337-503">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="5e337-504">Project</span><span class="sxs-lookup"><span data-stu-id="5e337-504">Project</span></span>

| <span data-ttu-id="5e337-505">**Логическое имя**</span><span class="sxs-lookup"><span data-stu-id="5e337-505">**Logical name**</span></span>                       | <span data-ttu-id="5e337-506">**Можно создать**</span><span class="sxs-lookup"><span data-stu-id="5e337-506">**Can create**</span></span> | <span data-ttu-id="5e337-507">**Может изменить**</span><span class="sxs-lookup"><span data-stu-id="5e337-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="5e337-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="5e337-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="5e337-509">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-509">no</span></span>             | <span data-ttu-id="5e337-510">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-510">no</span></span>           |
| <span data-ttu-id="5e337-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="5e337-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="5e337-512">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-512">no</span></span>             | <span data-ttu-id="5e337-513">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-513">no</span></span>           |
| <span data-ttu-id="5e337-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="5e337-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="5e337-515">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-515">no</span></span>             | <span data-ttu-id="5e337-516">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-516">no</span></span>           |
| <span data-ttu-id="5e337-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="5e337-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="5e337-518">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-518">no</span></span>             | <span data-ttu-id="5e337-519">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-519">no</span></span>           |
| <span data-ttu-id="5e337-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="5e337-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="5e337-521">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-521">no</span></span>             | <span data-ttu-id="5e337-522">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-522">no</span></span>           |
| <span data-ttu-id="5e337-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="5e337-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="5e337-524">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-524">no</span></span>             | <span data-ttu-id="5e337-525">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-525">no</span></span>           |
| <span data-ttu-id="5e337-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="5e337-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="5e337-527">да</span><span class="sxs-lookup"><span data-stu-id="5e337-527">yes</span></span>            | <span data-ttu-id="5e337-528">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-528">no</span></span>           |
| <span data-ttu-id="5e337-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="5e337-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="5e337-530">да</span><span class="sxs-lookup"><span data-stu-id="5e337-530">yes</span></span>            | <span data-ttu-id="5e337-531">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-531">no</span></span>           |
| <span data-ttu-id="5e337-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="5e337-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="5e337-533">да</span><span class="sxs-lookup"><span data-stu-id="5e337-533">yes</span></span>            | <span data-ttu-id="5e337-534">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-534">no</span></span>           |
| <span data-ttu-id="5e337-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="5e337-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="5e337-536">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-536">no</span></span>             | <span data-ttu-id="5e337-537">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-537">no</span></span>           |
| <span data-ttu-id="5e337-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="5e337-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="5e337-539">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-539">no</span></span>             | <span data-ttu-id="5e337-540">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-540">no</span></span>           |
| <span data-ttu-id="5e337-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="5e337-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="5e337-542">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-542">no</span></span>             | <span data-ttu-id="5e337-543">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-543">no</span></span>           |
| <span data-ttu-id="5e337-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="5e337-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="5e337-545">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-545">no</span></span>             | <span data-ttu-id="5e337-546">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-546">no</span></span>           |
| <span data-ttu-id="5e337-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="5e337-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="5e337-548">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-548">no</span></span>             | <span data-ttu-id="5e337-549">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-549">no</span></span>           |
| <span data-ttu-id="5e337-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="5e337-550">msdyn_duration</span></span>                         | <span data-ttu-id="5e337-551">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-551">no</span></span>             | <span data-ttu-id="5e337-552">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-552">no</span></span>           |
| <span data-ttu-id="5e337-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="5e337-553">msdyn_effort</span></span>                           | <span data-ttu-id="5e337-554">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-554">no</span></span>             | <span data-ttu-id="5e337-555">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-555">no</span></span>           |
| <span data-ttu-id="5e337-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="5e337-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="5e337-557">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-557">no</span></span>             | <span data-ttu-id="5e337-558">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-558">no</span></span>           |
| <span data-ttu-id="5e337-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="5e337-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="5e337-560">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-560">no</span></span>             | <span data-ttu-id="5e337-561">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-561">no</span></span>           |
| <span data-ttu-id="5e337-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="5e337-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="5e337-563">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-563">no</span></span>             | <span data-ttu-id="5e337-564">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-564">no</span></span>           |
| <span data-ttu-id="5e337-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="5e337-565">msdyn_finish</span></span>                           | <span data-ttu-id="5e337-566">да</span><span class="sxs-lookup"><span data-stu-id="5e337-566">yes</span></span>            | <span data-ttu-id="5e337-567">да</span><span class="sxs-lookup"><span data-stu-id="5e337-567">yes</span></span>          |
| <span data-ttu-id="5e337-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="5e337-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="5e337-569">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-569">no</span></span>             | <span data-ttu-id="5e337-570">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-570">no</span></span>           |
| <span data-ttu-id="5e337-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="5e337-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="5e337-572">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-572">no</span></span>             | <span data-ttu-id="5e337-573">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-573">no</span></span>           |
| <span data-ttu-id="5e337-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="5e337-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="5e337-575">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-575">no</span></span>             | <span data-ttu-id="5e337-576">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-576">no</span></span>           |
| <span data-ttu-id="5e337-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="5e337-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="5e337-578">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-578">no</span></span>             | <span data-ttu-id="5e337-579">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-579">no</span></span>           |
| <span data-ttu-id="5e337-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="5e337-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="5e337-581">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-581">no</span></span>             | <span data-ttu-id="5e337-582">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-582">no</span></span>           |
| <span data-ttu-id="5e337-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="5e337-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="5e337-584">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-584">no</span></span>             | <span data-ttu-id="5e337-585">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-585">no</span></span>           |
| <span data-ttu-id="5e337-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="5e337-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="5e337-587">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-587">no</span></span>             | <span data-ttu-id="5e337-588">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-588">no</span></span>           |
| <span data-ttu-id="5e337-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="5e337-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="5e337-590">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-590">no</span></span>             | <span data-ttu-id="5e337-591">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-591">no</span></span>           |
| <span data-ttu-id="5e337-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="5e337-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="5e337-593">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-593">no</span></span>             | <span data-ttu-id="5e337-594">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-594">no</span></span>           |
| <span data-ttu-id="5e337-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="5e337-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="5e337-596">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-596">no</span></span>             | <span data-ttu-id="5e337-597">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-597">no</span></span>           |
| <span data-ttu-id="5e337-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="5e337-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="5e337-599">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-599">no</span></span>             | <span data-ttu-id="5e337-600">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-600">no</span></span>           |
| <span data-ttu-id="5e337-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="5e337-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="5e337-602">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-602">no</span></span>             | <span data-ttu-id="5e337-603">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-603">no</span></span>           |
| <span data-ttu-id="5e337-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="5e337-604">msdyn_progress</span></span>                         | <span data-ttu-id="5e337-605">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-605">no</span></span>             | <span data-ttu-id="5e337-606">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-606">no</span></span>           |
| <span data-ttu-id="5e337-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="5e337-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="5e337-608">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-608">no</span></span>             | <span data-ttu-id="5e337-609">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-609">no</span></span>           |
| <span data-ttu-id="5e337-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="5e337-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="5e337-611">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-611">no</span></span>             | <span data-ttu-id="5e337-612">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-612">no</span></span>           |
| <span data-ttu-id="5e337-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="5e337-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="5e337-614">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-614">no</span></span>             | <span data-ttu-id="5e337-615">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-615">no</span></span>           |
| <span data-ttu-id="5e337-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="5e337-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="5e337-617">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-617">no</span></span>             | <span data-ttu-id="5e337-618">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-618">no</span></span>           |
| <span data-ttu-id="5e337-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="5e337-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="5e337-620">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-620">no</span></span>             | <span data-ttu-id="5e337-621">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-621">no</span></span>           |
| <span data-ttu-id="5e337-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="5e337-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="5e337-623">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-623">no</span></span>             | <span data-ttu-id="5e337-624">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-624">no</span></span>           |
| <span data-ttu-id="5e337-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="5e337-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="5e337-626">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-626">no</span></span>             | <span data-ttu-id="5e337-627">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-627">no</span></span>           |
| <span data-ttu-id="5e337-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="5e337-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="5e337-629">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-629">no</span></span>             | <span data-ttu-id="5e337-630">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-630">no</span></span>           |
| <span data-ttu-id="5e337-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="5e337-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="5e337-632">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-632">no</span></span>             | <span data-ttu-id="5e337-633">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-633">no</span></span>           |
| <span data-ttu-id="5e337-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="5e337-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="5e337-635">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-635">no</span></span>             | <span data-ttu-id="5e337-636">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-636">no</span></span>           |
| <span data-ttu-id="5e337-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="5e337-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="5e337-638">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-638">no</span></span>             | <span data-ttu-id="5e337-639">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-639">no</span></span>           |
| <span data-ttu-id="5e337-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="5e337-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="5e337-641">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-641">no</span></span>             | <span data-ttu-id="5e337-642">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-642">no</span></span>           |
| <span data-ttu-id="5e337-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="5e337-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="5e337-644">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-644">no</span></span>             | <span data-ttu-id="5e337-645">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-645">no</span></span>           |
| <span data-ttu-id="5e337-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="5e337-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="5e337-647">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-647">no</span></span>             | <span data-ttu-id="5e337-648">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-648">no</span></span>           |
| <span data-ttu-id="5e337-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="5e337-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="5e337-650">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-650">no</span></span>             | <span data-ttu-id="5e337-651">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-651">no</span></span>           |
| <span data-ttu-id="5e337-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="5e337-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="5e337-653">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-653">no</span></span>             | <span data-ttu-id="5e337-654">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-654">no</span></span>           |
| <span data-ttu-id="5e337-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="5e337-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="5e337-656">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-656">no</span></span>             | <span data-ttu-id="5e337-657">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-657">no</span></span>           |
| <span data-ttu-id="5e337-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="5e337-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="5e337-659">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-659">no</span></span>             | <span data-ttu-id="5e337-660">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-660">no</span></span>           |
| <span data-ttu-id="5e337-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="5e337-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="5e337-662">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-662">no</span></span>             | <span data-ttu-id="5e337-663">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-663">no</span></span>           |
| <span data-ttu-id="5e337-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="5e337-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="5e337-665">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-665">no</span></span>             | <span data-ttu-id="5e337-666">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-666">no</span></span>           |
| <span data-ttu-id="5e337-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="5e337-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="5e337-668">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-668">no</span></span>             | <span data-ttu-id="5e337-669">нет</span><span class="sxs-lookup"><span data-stu-id="5e337-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="5e337-670">Известные проблемы и ограничения</span><span class="sxs-lookup"><span data-stu-id="5e337-670">Limitations and known issues</span></span>
<span data-ttu-id="5e337-671">Ниже приводится список ограничений и известных проблем:</span><span class="sxs-lookup"><span data-stu-id="5e337-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="5e337-672">API расписания проекта могут использоваться только **Пользователями с лицензией Microsoft Project.**</span><span class="sxs-lookup"><span data-stu-id="5e337-672">Project Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="5e337-673">Их не могут использовать:</span><span class="sxs-lookup"><span data-stu-id="5e337-673">They can't be used by:</span></span>
    - <span data-ttu-id="5e337-674">Пользователи приложений</span><span class="sxs-lookup"><span data-stu-id="5e337-674">Application users</span></span>
    - <span data-ttu-id="5e337-675">Системные пользователи</span><span class="sxs-lookup"><span data-stu-id="5e337-675">System users</span></span>
    - <span data-ttu-id="5e337-676">Пользователи-интеграторы</span><span class="sxs-lookup"><span data-stu-id="5e337-676">Integration users</span></span>
    - <span data-ttu-id="5e337-677">Другие пользователи, у которых нет необходимой лицензии</span><span class="sxs-lookup"><span data-stu-id="5e337-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="5e337-678">У каждого **OperationSet** может быть не более 100 операций.</span><span class="sxs-lookup"><span data-stu-id="5e337-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="5e337-679">У каждого пользователя может быть не более 10 открытых **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="5e337-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="5e337-680">В настоящее время Project Operations поддерживает не более 500 общих задач в проекте.</span><span class="sxs-lookup"><span data-stu-id="5e337-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="5e337-681">Статус сбоя и журналы ошибок в **OperationSet** в настоящее время недоступны.</span><span class="sxs-lookup"><span data-stu-id="5e337-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- [<span data-ttu-id="5e337-682">Пределы и границы проектов и задач</span><span class="sxs-lookup"><span data-stu-id="5e337-682">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="5e337-683">Обработка ошибок</span><span class="sxs-lookup"><span data-stu-id="5e337-683">Error handling</span></span>

   - <span data-ttu-id="5e337-684">Чтобы просмотреть ошибки, сгенерированные из наборов операций, перейдите к **Параметры** \> **Интеграция расписания** \> **Наборы операций**.</span><span class="sxs-lookup"><span data-stu-id="5e337-684">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="5e337-685">Чтобы просмотреть ошибки, сгенерированные службой расписания проекта, перейдите в раздел **Настройки** \> **Интеграция расписаний** \> **Журналы ошибок PSS**.</span><span class="sxs-lookup"><span data-stu-id="5e337-685">To review errors generated from the Project schedule Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="5e337-686">Пример сценария</span><span class="sxs-lookup"><span data-stu-id="5e337-686">Sample scenario</span></span>

<span data-ttu-id="5e337-687">В этом сценарии вы создадите проект, участника команды, четыре задачи и два назначения ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5e337-687">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="5e337-688">Затем вы обновите одну задачу, обновите проект, удалите одну задачу, удалите одно назначение ресурса и создадите зависимость задачи.</span><span class="sxs-lookup"><span data-stu-id="5e337-688">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

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

## <a name="additional-samples"></a><span data-ttu-id="5e337-689">Дополнительные примеры</span><span class="sxs-lookup"><span data-stu-id="5e337-689">Additional samples</span></span>

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
