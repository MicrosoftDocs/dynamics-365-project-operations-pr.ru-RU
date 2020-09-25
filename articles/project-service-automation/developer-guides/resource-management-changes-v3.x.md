---
title: Изменения управления ресурсами (Project Service Automation 3.x)
description: В этом разделе представлена информация об изменениях в области управления ресурсами.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 25fafd22-fe94-4865-8d4d-3e6582c999d5
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
ms.openlocfilehash: e00ce5a9604e25764567a3f9d38ec85aec4245d4
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754973"
---
# <a name="resource-management-changes-project-service-automation-3x"></a><span data-ttu-id="06c43-103">Изменения управления ресурсами (Project Service Automation 3.x)</span><span class="sxs-lookup"><span data-stu-id="06c43-103">Resource management changes (Project Service Automation 3.x)</span></span>

<span data-ttu-id="06c43-104">Разделы этой темы содержат сведения об изменениях, которые были сделаны в области управления ресурсами Dynamics 365 Project Service Automation версии 3.x.</span><span class="sxs-lookup"><span data-stu-id="06c43-104">The sections of this topic provide information about the changes that have been made to the Resource management area of Dynamics 365 Project Service Automation version 3.x.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="06c43-105">Оценки проекта</span><span class="sxs-lookup"><span data-stu-id="06c43-105">Project estimates</span></span>

<span data-ttu-id="06c43-106">Вместо сущности **msdyn\_projecttask** (**Задача проекта**), оценки проекта основаны на сущности **msdyn\_resourceassignment** (**Назначение ресурса**).</span><span class="sxs-lookup"><span data-stu-id="06c43-106">Instead of being based on the **msdyn\_projecttask** entity (**Project Task**), project estimates are based on the **msdyn\_resourceassignment** entity (**Resource Assignment**).</span></span> <span data-ttu-id="06c43-107">Назначения ресурсов стали "источником истины" для планирования и цен задач.</span><span class="sxs-lookup"><span data-stu-id="06c43-107">Resource assignments have become the "source of truth" for task scheduling and pricing.</span></span>

## <a name="line-tasks"></a><span data-ttu-id="06c43-108">Задачи строки</span><span class="sxs-lookup"><span data-stu-id="06c43-108">Line tasks</span></span>

<span data-ttu-id="06c43-109">В PSA 3.x задачи строки устарели (нерекомендуемый).</span><span class="sxs-lookup"><span data-stu-id="06c43-109">In PSA 3.x, line tasks are obsolete (deprecated).</span></span> <span data-ttu-id="06c43-110">Назначения теперь указывают на всю задачу, а не на задачи строки.</span><span class="sxs-lookup"><span data-stu-id="06c43-110">Assignments now point to the whole task instead of the line tasks.</span></span>

<span data-ttu-id="06c43-111">Следующий пример показывает, как задача с названием "Тестовая задача" назначается участникам рабочей группы A и B в предыдущих версиях PSA и в PSA 3.x.</span><span class="sxs-lookup"><span data-stu-id="06c43-111">The following example shows how a task that is named "Test task" is assigned to team members A and B in earlier versions of PSA and in PSA 3.x.</span></span>

- <span data-ttu-id="06c43-112">**До PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="06c43-112">**Before PSA 3.x:**</span></span>

    - <span data-ttu-id="06c43-113">Тестовая задача</span><span class="sxs-lookup"><span data-stu-id="06c43-113">Test task</span></span>

        - <span data-ttu-id="06c43-114">Тестовая задача — задача строки 1</span><span class="sxs-lookup"><span data-stu-id="06c43-114">Test task – Line task 1</span></span>

            - <span data-ttu-id="06c43-115">Назначение A</span><span class="sxs-lookup"><span data-stu-id="06c43-115">Assignment to A</span></span>

        - <span data-ttu-id="06c43-116">Тестовая задача — задача строки 2</span><span class="sxs-lookup"><span data-stu-id="06c43-116">Test task – Line task 2</span></span>

            - <span data-ttu-id="06c43-117">Назначение B</span><span class="sxs-lookup"><span data-stu-id="06c43-117">Assignment to B</span></span>

- <span data-ttu-id="06c43-118">**PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="06c43-118">**PSA 3.x:**</span></span>

    - <span data-ttu-id="06c43-119">Тестовая задача</span><span class="sxs-lookup"><span data-stu-id="06c43-119">Test task</span></span>

        - <span data-ttu-id="06c43-120">Назначение A</span><span class="sxs-lookup"><span data-stu-id="06c43-120">Assignment to A</span></span>
        - <span data-ttu-id="06c43-121">Назначение B</span><span class="sxs-lookup"><span data-stu-id="06c43-121">Assignment to B</span></span>

## <a name="unassigned-assignment"></a><span data-ttu-id="06c43-122">Неназначенное назначение</span><span class="sxs-lookup"><span data-stu-id="06c43-122">Unassigned assignment</span></span>

<span data-ttu-id="06c43-123">В PSA 3.x неназначенное назначение — это назначение, которое назначено участнику рабочей группы **NULL** и ресурсу **NULL**.</span><span class="sxs-lookup"><span data-stu-id="06c43-123">In PSA 3.x, an unassigned assignment is an assignment that is assigned to a **NULL** team member and a **NULL** resource.</span></span> <span data-ttu-id="06c43-124">Неназначенные назначения могут возникать в паре случаев:</span><span class="sxs-lookup"><span data-stu-id="06c43-124">Unassigned assignments can occur in a couple of scenarios:</span></span>

- <span data-ttu-id="06c43-125">Если задача была создано, но пока еще не была назначена какому-либо участнику рабочей группы, неназначенное назначение всегда создается.</span><span class="sxs-lookup"><span data-stu-id="06c43-125">If a task has been created, but it hasn't yet been assigned to any team member, an unassigned assignment is always created.</span></span> 
- <span data-ttu-id="06c43-126">Если все назначенные для задачи будут удалены, то неназначенное назначение снова создается для этой задачи.</span><span class="sxs-lookup"><span data-stu-id="06c43-126">If all assignees on a task are removed, an unassigned assignment is re-created for that task.</span></span>

## <a name="scheduling-fields-on-the-project-task-entity"></a><span data-ttu-id="06c43-127">Поля планирования в сущности задачи проекта</span><span class="sxs-lookup"><span data-stu-id="06c43-127">Scheduling fields on the Project Task entity</span></span>

<span data-ttu-id="06c43-128">Поля в сущности **msdyn\_projecttask** стали нерекомендуемыми или были перемещены в сущность **msdyn\_resourceassignment**, или на них теперь имеются ссылки из сущности **msdyn\_projectteam** (**Участник проектной группы**).</span><span class="sxs-lookup"><span data-stu-id="06c43-128">The fields on the **msdyn\_projecttask** entity have been deprecated or moved to the **msdyn\_resourceassignment** entity, or they are now referenced from the **msdyn\_projectteam** entity (**Project Team Member**).</span></span>

| <span data-ttu-id="06c43-129">Нерекомендуемое поле в msdyn\_projecttask (Задача проекта)</span><span class="sxs-lookup"><span data-stu-id="06c43-129">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="06c43-130">Новое поле в msdyn\_resourceassignment (Назначение ресурса)</span><span class="sxs-lookup"><span data-stu-id="06c43-130">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> | <span data-ttu-id="06c43-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="06c43-131">Comment</span></span> |
|---|---|---|
| <span data-ttu-id="06c43-132">msdyn\_assignedresources</span><span class="sxs-lookup"><span data-stu-id="06c43-132">msdyn\_assignedresources</span></span> | <span data-ttu-id="06c43-133">Нет</span><span class="sxs-lookup"><span data-stu-id="06c43-133">None</span></span> | |
| <span data-ttu-id="06c43-134">msdyn\_assignedteammembers</span><span class="sxs-lookup"><span data-stu-id="06c43-134">msdyn\_assignedteammembers</span></span> | <span data-ttu-id="06c43-135">Нет</span><span class="sxs-lookup"><span data-stu-id="06c43-135">None</span></span> | |
| <span data-ttu-id="06c43-136">msdyn\_numberofresources</span><span class="sxs-lookup"><span data-stu-id="06c43-136">msdyn\_numberofresources</span></span> | <span data-ttu-id="06c43-137">Нет</span><span class="sxs-lookup"><span data-stu-id="06c43-137">None</span></span> | |
| <span data-ttu-id="06c43-138">msdyn\_scheduledhours</span><span class="sxs-lookup"><span data-stu-id="06c43-138">msdyn\_scheduledhours</span></span> | <span data-ttu-id="06c43-139">Нет</span><span class="sxs-lookup"><span data-stu-id="06c43-139">None</span></span> | |
| <span data-ttu-id="06c43-140">msdyn\_effortcontour</span><span class="sxs-lookup"><span data-stu-id="06c43-140">msdyn\_effortcontour</span></span> | <span data-ttu-id="06c43-141">msdyn\_plannedwork</span><span class="sxs-lookup"><span data-stu-id="06c43-141">msdyn\_plannedwork</span></span> | <span data-ttu-id="06c43-142">Был изменен формат структуры данных нотации объектов JavaScript (JSON), которая хранится в поле.</span><span class="sxs-lookup"><span data-stu-id="06c43-142">The format of the JavaScript Object Notation (JSON) data structure that is stored in the field has been changed.</span></span> |

## <a name="schedule-contour"></a><span data-ttu-id="06c43-143">Контур расписания</span><span class="sxs-lookup"><span data-stu-id="06c43-143">Schedule contour</span></span>

<span data-ttu-id="06c43-144">Контур расписания хранится в поле **Запланированная работа** (**msdyn\_plannedwork**) каждой сущности **Resource Assignment** (**msdyn\_resourceassignment**).</span><span class="sxs-lookup"><span data-stu-id="06c43-144">The schedule contour is stored in the **Planned Work** field (**msdyn\_plannedwork**) of each **Resource Assignment** entity (**msdyn\_resourceassignment**).</span></span>

### <a name="structure"></a><span data-ttu-id="06c43-145">Структура</span><span class="sxs-lookup"><span data-stu-id="06c43-145">Structure</span></span>

<span data-ttu-id="06c43-146">Новая структура контура расписания состоит из гибких слоев времени, которые определяются для каждого дня расписания.</span><span class="sxs-lookup"><span data-stu-id="06c43-146">The new structure of the schedule contour consists of flexible time slices that are defined for each day of the schedule.</span></span> <span data-ttu-id="06c43-147">Каждый слой времени имеет следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="06c43-147">Each time slice has the following properties:</span></span>

- <span data-ttu-id="06c43-148">**Начало** — время начала рабочих часов на определенный день по календарю проекта.</span><span class="sxs-lookup"><span data-stu-id="06c43-148">**Start** – The start of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="06c43-149">**Конец** — время окончания рабочих часов на определенный день по календарю проекта.</span><span class="sxs-lookup"><span data-stu-id="06c43-149">**End** – The end of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="06c43-150">**Часы** — число часов, которые назначены на день.</span><span class="sxs-lookup"><span data-stu-id="06c43-150">**Hours** – The number of hours that are assigned on the day.</span></span>

<span data-ttu-id="06c43-151">**Пример**</span><span class="sxs-lookup"><span data-stu-id="06c43-151">**Example**</span></span>

<span data-ttu-id="06c43-152">В этом примере используется календарь проекта, где рабочий день занимает время с 9 утра до 5 вечера в часовом поясе UTC-8.</span><span class="sxs-lookup"><span data-stu-id="06c43-152">This example uses a project calendar where the workday is from 9 AM to 5 PM in the UTC-8 time zone.</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a><span data-ttu-id="06c43-153">Автоматическое и ручное планирование</span><span class="sxs-lookup"><span data-stu-id="06c43-153">Auto-scheduling and manual scheduling</span></span>

<span data-ttu-id="06c43-154">Если задача автоматически запланирована, часы загружаются сначала, а длительность задачи может быть уменьшена.</span><span class="sxs-lookup"><span data-stu-id="06c43-154">If a task is auto-scheduled, the hours are front-loaded, and the task duration might be reduced.</span></span>

<span data-ttu-id="06c43-155">**Пример**</span><span class="sxs-lookup"><span data-stu-id="06c43-155">**Example**</span></span>

<span data-ttu-id="06c43-156">Следующая задача автоматической запланирована на 18 часов за 3 дня (с 3-го декабря 2018 по 5-е декабря 2018).</span><span class="sxs-lookup"><span data-stu-id="06c43-156">The following task is auto-scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

<span data-ttu-id="06c43-157">Если задача запланирована вручную, часы распределяются равномерно по всем датам.</span><span class="sxs-lookup"><span data-stu-id="06c43-157">If a task is manually scheduled, the hours are evenly distributed to all the dates.</span></span>

<span data-ttu-id="06c43-158">**Пример**</span><span class="sxs-lookup"><span data-stu-id="06c43-158">**Example**</span></span>

<span data-ttu-id="06c43-159">Следующая задача вручную запланирована на 18 часов за 3 дня (с 3-го декабря 2018 по 5-е декабря 2018).</span><span class="sxs-lookup"><span data-stu-id="06c43-159">The following task is manually scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a><span data-ttu-id="06c43-160">Единица назначение</span><span class="sxs-lookup"><span data-stu-id="06c43-160">Assignment unit</span></span>

<span data-ttu-id="06c43-161">Единица назначения устарела в PSA 3.x.</span><span class="sxs-lookup"><span data-stu-id="06c43-161">The assignment unit has been deprecated in PSA 3.x.</span></span> <span data-ttu-id="06c43-162">Часы усилий по задаче теперь поровну делятся на дни среди всех назначенных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="06c43-162">The task effort hours are now equally divided, per day, among all the assigned resources.</span></span>

<span data-ttu-id="06c43-163">**Пример**</span><span class="sxs-lookup"><span data-stu-id="06c43-163">**Example**</span></span>

<span data-ttu-id="06c43-164">В этом примере задача назначена двум ресурсам и автоматически запланирована на 36 часов за 3 дня (с 3-го декабря 2018 по 5-е декабря 2018).</span><span class="sxs-lookup"><span data-stu-id="06c43-164">In this example, the task is is assigned to two resources and is auto-scheduled for 36 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

- <span data-ttu-id="06c43-165">Назначение 1:</span><span class="sxs-lookup"><span data-stu-id="06c43-165">Assignment 1:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- <span data-ttu-id="06c43-166">Назначение 2:</span><span class="sxs-lookup"><span data-stu-id="06c43-166">Assignment 2:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a><span data-ttu-id="06c43-167">Измерения цен</span><span class="sxs-lookup"><span data-stu-id="06c43-167">Pricing dimensions</span></span>

<span data-ttu-id="06c43-168">В PSA 3.x специфичные для ресурсов поля измерения цен (такие как **Роль** и **Подразделение**) были удалены из сущности **msdyn\_projecttask**.</span><span class="sxs-lookup"><span data-stu-id="06c43-168">In PSA 3.x, resource-specific pricing dimension fields (such as **Role** and **Organizational Unit**) have been removed from the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="06c43-169">Эти поля теперь можно извлечь из соответствующего участника рабочей группы проекта (**msdyn\_projectteam**) назначения ресурса (**msdyn\_resourceassignment**) при создании оценок проекта.</span><span class="sxs-lookup"><span data-stu-id="06c43-169">These fields can now be retrieved from the corresponding project team member (**msdyn\_projectteam**) of the resource assignment (**msdyn\_resourceassignment**) when project estimates are generated.</span></span> <span data-ttu-id="06c43-170">Новое поле **msdyn\_organizationalunit** было добавлено в сущность **msdyn\_projectteam**.</span><span class="sxs-lookup"><span data-stu-id="06c43-170">A new field, **msdyn\_organizationalunit**, has been added to the **msdyn\_projectteam** entity.</span></span>

| <span data-ttu-id="06c43-171">Нерекомендуемое поле в msdyn\_projecttask (Задача проекта)</span><span class="sxs-lookup"><span data-stu-id="06c43-171">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="06c43-172">Поле из msdyn\_projectteam (Участник проектной группы), которое используется взамен</span><span class="sxs-lookup"><span data-stu-id="06c43-172">Field from msdyn\_projectteam (Project Team Member) that is used instead</span></span> |
|---|---|
| <span data-ttu-id="06c43-173">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="06c43-173">msdyn\_resourcecategory</span></span> | <span data-ttu-id="06c43-174">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="06c43-174">msdyn\_resourcecategory</span></span> |
| <span data-ttu-id="06c43-175">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="06c43-175">msdyn\_organizationalunit</span></span> | <span data-ttu-id="06c43-176">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="06c43-176">msdyn\_organizationalunit</span></span> |

## <a name="contours"></a><span data-ttu-id="06c43-177">Контуры</span><span class="sxs-lookup"><span data-stu-id="06c43-177">Contours</span></span>

<span data-ttu-id="06c43-178">Поле цен и контуров оценки устарели в сущности **msdyn\_projecttask**.</span><span class="sxs-lookup"><span data-stu-id="06c43-178">The pricing and estimation contour fields have been deprecated on the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="06c43-179">Они удалены из сущности **msdyn\_resourceassignment**.</span><span class="sxs-lookup"><span data-stu-id="06c43-179">They have been moved to the **msdyn\_resourceassignment** entity.</span></span>

| <span data-ttu-id="06c43-180">Нерекомендуемое поле в msdyn\_projecttask (Задача проекта)</span><span class="sxs-lookup"><span data-stu-id="06c43-180">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="06c43-181">Новое поле в msdyn\_resourceassignment (Назначение ресурса)</span><span class="sxs-lookup"><span data-stu-id="06c43-181">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> |
|---|---|
| <span data-ttu-id="06c43-182">msdyn\_costestimatecontour</span><span class="sxs-lookup"><span data-stu-id="06c43-182">msdyn\_costestimatecontour</span></span> | <span data-ttu-id="06c43-183">msdyn\_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="06c43-183">msdyn\_plannedcostcontour</span></span> |
| <span data-ttu-id="06c43-184">msdyn\_salesestimatecontour</span><span class="sxs-lookup"><span data-stu-id="06c43-184">msdyn\_salesestimatecontour</span></span> | <span data-ttu-id="06c43-185">msdyn\_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="06c43-185">msdyn\_plannedsalescontour</span></span> |

<span data-ttu-id="06c43-186">Следующие поля добавлены в сущность **msdyn\_resourceassignment**:</span><span class="sxs-lookup"><span data-stu-id="06c43-186">The following fields have been added to the **msdyn\_resourceassignment** entity:</span></span>

* <span data-ttu-id="06c43-187">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="06c43-187">msdyn\_plannedcost</span></span>
* <span data-ttu-id="06c43-188">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="06c43-188">msdyn\_plannedsales</span></span>

<span data-ttu-id="06c43-189">Следующие поля для плановой, фактической и оставшейся стоимости и продажам не изменились в сущности **msdyn\_projecttask**:</span><span class="sxs-lookup"><span data-stu-id="06c43-189">The following fields for planned, actual, and remaining cost and sales are unchanged on the **msdyn\_projecttask** entity:</span></span>

* <span data-ttu-id="06c43-190">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="06c43-190">msdyn\_plannedcost</span></span>
* <span data-ttu-id="06c43-191">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="06c43-191">msdyn\_plannedsales</span></span>
* <span data-ttu-id="06c43-192">msdyn\_actualcost</span><span class="sxs-lookup"><span data-stu-id="06c43-192">msdyn\_actualcost</span></span>
* <span data-ttu-id="06c43-193">msdyn\_actualsales</span><span class="sxs-lookup"><span data-stu-id="06c43-193">msdyn\_actualsales</span></span>
* <span data-ttu-id="06c43-194">msdyn\_remainingcost</span><span class="sxs-lookup"><span data-stu-id="06c43-194">msdyn\_remainingcost</span></span>
* <span data-ttu-id="06c43-195">msdyn\_remainingsales</span><span class="sxs-lookup"><span data-stu-id="06c43-195">msdyn\_remainingsales</span></span>