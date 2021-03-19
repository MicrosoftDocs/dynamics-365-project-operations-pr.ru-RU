---
title: Рекомендации по обновлению структурной декомпозиции работ
description: В этом разделе приведены сведения об обновлении структурной декомпозиции работ из Project Service Automation версий с 2.x по 3.x.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
author: ruhercul
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: a067521410f0fe0d8f5d4c510a35f2a3b018dce3
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281764"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a><span data-ttu-id="3f24b-103">Рекомендации по обновлению структурной декомпозиции работ</span><span class="sxs-lookup"><span data-stu-id="3f24b-103">Upgrade considerations for the work breakdown structure</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="3f24b-104">В этом разделе приведены сведения об обновлении структурной декомпозиции работ из Project Service Automation версий с 2.x по 3.x.</span><span class="sxs-lookup"><span data-stu-id="3f24b-104">This topic provides information about upgrading the work breakdown structure from Project Service Automation 2.x to 3.x.</span></span> <span data-ttu-id="3f24b-105">В этом разделе определяется рабочее состояние проекта в Project Service Automation (PSA), которое требуется для успешного обновления.</span><span class="sxs-lookup"><span data-stu-id="3f24b-105">This topic defines the healthy state of a project in Project Service Automation (PSA) that is required for a successful upgrade.</span></span> <span data-ttu-id="3f24b-106">Также имеется информация об общих условиях блокировки, которые приведут к сбою обновления.</span><span class="sxs-lookup"><span data-stu-id="3f24b-106">There is also information about the common blocking conditions that will cause upgrade to fail.</span></span> <span data-ttu-id="3f24b-107">Дополнительные сведения об определении задач проекта и их функций в расписании проекта см. [Расписания проекта](project-creating.md).</span><span class="sxs-lookup"><span data-stu-id="3f24b-107">For more information about defining project tasks and their functions within a project schedule, see [Project schedules](project-creating.md).</span></span>

## <a name="key-entities"></a><span data-ttu-id="3f24b-108">Основные сущности</span><span class="sxs-lookup"><span data-stu-id="3f24b-108">Key entities</span></span>
<span data-ttu-id="3f24b-109">Для точной структурной декомпозиции работ, которая уже загружена ресурсами, требуются следующие сущности:</span><span class="sxs-lookup"><span data-stu-id="3f24b-109">For an accurate work breakdown structure that is already loaded with resources, the following entities are required:</span></span>

- [<span data-ttu-id="3f24b-110">Проект</span><span class="sxs-lookup"><span data-stu-id="3f24b-110">Project</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [<span data-ttu-id="3f24b-111">Проектная группа</span><span class="sxs-lookup"><span data-stu-id="3f24b-111">Project Team</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [<span data-ttu-id="3f24b-112">Задача проекта</span><span class="sxs-lookup"><span data-stu-id="3f24b-112">Project Task</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [<span data-ttu-id="3f24b-113">Назначения ресурсов</span><span class="sxs-lookup"><span data-stu-id="3f24b-113">Resource Assignments</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [<span data-ttu-id="3f24b-114">Зависимость задач проекта</span><span class="sxs-lookup"><span data-stu-id="3f24b-114">Project Task Dependency</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [<span data-ttu-id="3f24b-115">Резервируемые ресурсы</span><span class="sxs-lookup"><span data-stu-id="3f24b-115">Bookable Resources</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

<span data-ttu-id="3f24b-116">Чтобы определить загруженную ресурсом структурную декомпозицию работ, необходимо выполнить следующие шаги:</span><span class="sxs-lookup"><span data-stu-id="3f24b-116">To define a resource loaded work breakdown structure, you must complete the following steps:</span></span>

1. <span data-ttu-id="3f24b-117">Создание нового проекта.</span><span class="sxs-lookup"><span data-stu-id="3f24b-117">Create a new project.</span></span> <span data-ttu-id="3f24b-118">Дополнительные сведения о том, как создать новый проект, см. в статье [msdyn_project](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).</span><span class="sxs-lookup"><span data-stu-id="3f24b-118">For more information about how to create a new project, see [msdyn_project](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).</span></span>
2. <span data-ttu-id="3f24b-119">Создайте одну или несколько задач.</span><span class="sxs-lookup"><span data-stu-id="3f24b-119">Create one or more tasks.</span></span> <span data-ttu-id="3f24b-120">Дополнительные сведения о том, как создать задачу, см. в статье [msdyn_projecttask](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).</span><span class="sxs-lookup"><span data-stu-id="3f24b-120">For more information about how to create a task, see [msdyn_projecttask](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).</span></span>
3. <span data-ttu-id="3f24b-121">Определите зависимости задачи.</span><span class="sxs-lookup"><span data-stu-id="3f24b-121">Define the task dependencies.</span></span> <span data-ttu-id="3f24b-122">Дополнительные сведения см. в разделе [Зависимость задач проекта](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency),</span><span class="sxs-lookup"><span data-stu-id="3f24b-122">For more information, see [Project Task Dependency](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).</span></span>
4. <span data-ttu-id="3f24b-123">Назначьте участников проектной рабочей группы проекту.</span><span class="sxs-lookup"><span data-stu-id="3f24b-123">Assign project team members to the project.</span></span> <span data-ttu-id="3f24b-124">Дополнительные сведения см. в статье [msdyn_projectteam](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).</span><span class="sxs-lookup"><span data-stu-id="3f24b-124">For more information, see [msdyn_projectteam](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).</span></span>
5. <span data-ttu-id="3f24b-125">Назначьте участников проектной рабочей группы задаче.</span><span class="sxs-lookup"><span data-stu-id="3f24b-125">Assign project team members to the tasks.</span></span> <span data-ttu-id="3f24b-126">Дополнительные сведения см. в статье [msdyn_resourceassignment](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).</span><span class="sxs-lookup"><span data-stu-id="3f24b-126">For more information, see [msdyn_resourceassignment](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).</span></span>

## <a name="project-team-relationships"></a><span data-ttu-id="3f24b-127">Отношения проектной рабочей группы</span><span class="sxs-lookup"><span data-stu-id="3f24b-127">Project team relationships</span></span>

<span data-ttu-id="3f24b-128">Чтобы обеспечить успешное обновление, необходимо правильно поддерживать следующие отношения:</span><span class="sxs-lookup"><span data-stu-id="3f24b-128">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>
- <span data-ttu-id="3f24b-129">Всех участники проектной рабочей группы должны быть связаны с резервируемым ресурсом.</span><span class="sxs-lookup"><span data-stu-id="3f24b-129">All project team members must be associated with a bookable resource.</span></span>
- <span data-ttu-id="3f24b-130">Всех участники проектной рабочей группы должны быть связаны с тем же проектом.</span><span class="sxs-lookup"><span data-stu-id="3f24b-130">All project team members must be associated with the same project.</span></span> 

## <a name="project-task-relationships"></a><span data-ttu-id="3f24b-131">Отношения задачи проекта</span><span class="sxs-lookup"><span data-stu-id="3f24b-131">Project task relationships</span></span>
<span data-ttu-id="3f24b-132">Чтобы обеспечить успешное обновление, необходимо правильно поддерживать следующие отношения:</span><span class="sxs-lookup"><span data-stu-id="3f24b-132">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="3f24b-133">Все связанные задачи должно быть связано с тем же проектом.</span><span class="sxs-lookup"><span data-stu-id="3f24b-133">Any related tasks must be associated with the same project.</span></span>
- <span data-ttu-id="3f24b-134">Каждая задача строки должна иметь родительскую задачу.</span><span class="sxs-lookup"><span data-stu-id="3f24b-134">Every line task must have a parent task.</span></span>
- <span data-ttu-id="3f24b-135">Каждая задача должна иметь родительский проект.</span><span class="sxs-lookup"><span data-stu-id="3f24b-135">Every task must have a parent project.</span></span>

### <a name="valid-conditions"></a><span data-ttu-id="3f24b-136">Допустимые условия</span><span class="sxs-lookup"><span data-stu-id="3f24b-136">Valid conditions</span></span>

- <span data-ttu-id="3f24b-137">Все длительности задачи должны быть больше или равны (>=) одному часу и менее 1800000 минут (1250 дней).\*</span><span class="sxs-lookup"><span data-stu-id="3f24b-137">All task durations must be greater than or equal to (>=) one hour and less than 1,800,000 minutes (1,250 days).\*</span></span>
- <span data-ttu-id="3f24b-138">Все задачи должны иметь дату начала не ранее 01/01/2000.\*</span><span class="sxs-lookup"><span data-stu-id="3f24b-138">All tasks must have a start date no earlier than 2000/01/01.\*</span></span>
- <span data-ttu-id="3f24b-139">Все задачи должны иметь дату начала не позднее 17 лет с сегодняшнего дня.\*</span><span class="sxs-lookup"><span data-stu-id="3f24b-139">All tasks must have a start date no later than 17 years from the present day.\*</span></span>
- <span data-ttu-id="3f24b-140">Все задачи должны иметь дату начала ранее или равную их дате окончания.</span><span class="sxs-lookup"><span data-stu-id="3f24b-140">All tasks must have a start date earlier or equal to their finish date.</span></span>
- <span data-ttu-id="3f24b-141">Все типы проводок по классификациям (расходы, материалы, налоги и время) должны иметь значения для **Единица измерения по умолчанию** и **Группа единиц измерения**.</span><span class="sxs-lookup"><span data-stu-id="3f24b-141">All transaction types on classifications (Expense, Material, Tax, and Time) must have values for **Default Unit** and **Unit Group**.</span></span>
- <span data-ttu-id="3f24b-142">Форматы даты с буквами следует избегать.</span><span class="sxs-lookup"><span data-stu-id="3f24b-142">Date formats with letters should be avoided.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="3f24b-143">Шаги по устранению потенциальных проблем</span><span class="sxs-lookup"><span data-stu-id="3f24b-143">Potential mitigation steps</span></span>
- <span data-ttu-id="3f24b-144">С помощью расширенного поиска выявите задачи проекта, которые не содержат идентификатора проекта.</span><span class="sxs-lookup"><span data-stu-id="3f24b-144">Use Advanced Find to identify Project tasks that do not contain a Project ID.</span></span>
- <span data-ttu-id="3f24b-145">С помощью расширенного поиска выявите задачи проекта, у которых запланированная длительность превышает 1 800 000.</span><span class="sxs-lookup"><span data-stu-id="3f24b-145">Use Advanced Find to identify Project tasks where the scheduled duration is greater than > 1,800,000.</span></span>
- <span data-ttu-id="3f24b-146">Прежде чем вносить какие-либо изменения в данные, вы должны изучить все настройки, связанные с сущностью, которые могли бы привести к неправильному состоянию данных.</span><span class="sxs-lookup"><span data-stu-id="3f24b-146">Prior to making any data changes, you should investigate any customizations associated with the entity that may have led to getting the data into a bad state.</span></span> <span data-ttu-id="3f24b-147">Решить проблему с этими настройками необходимо до того, как переходить к каким-либо связанным с данными обновлениям.</span><span class="sxs-lookup"><span data-stu-id="3f24b-147">These customizations should be addressed before proceeding with any data-related updates.</span></span>
- <span data-ttu-id="3f24b-148">Что касается найденных "потерянных" задач, рассмотрите возможность удаления этих задач, если они не нужны или если они должны быть связаны с соответствующим родительским проектом.</span><span class="sxs-lookup"><span data-stu-id="3f24b-148">For the identified tasks that have been orphaned, consider deleting these tasks if they are not needed or if they should be associated with the correct parent project.</span></span>
- <span data-ttu-id="3f24b-149">Что касается задач, длительность которых превышает 1250 дней, рассмотрите возможность добавления нескольких задач, чтобы разделить эту длительность на меньшие периоды, если это допустимо.</span><span class="sxs-lookup"><span data-stu-id="3f24b-149">For any tasks where the duration is greater than 1,250 days, consider adding multiple tasks to represent the total duration, if feasible.</span></span>

> [!NOTE]
> <span data-ttu-id="3f24b-150">Элементы, отмеченные звездочкой (\*), имеют ограничения, связанные с тем, что система управления отношениями с клиентами (CRM) поддерживает только 7320 расширений повторения.</span><span class="sxs-lookup"><span data-stu-id="3f24b-150">Items noted with an asterisk (\*) have limits that are due to the fact that customer relationship management (CRM) supports only 7,320 recurrence expansions.</span></span> <span data-ttu-id="3f24b-151">Необходимо оставаться ниже этого предела.</span><span class="sxs-lookup"><span data-stu-id="3f24b-151">You must stay below this limit.</span></span>

## <a name="resource-assignment-relationships"></a><span data-ttu-id="3f24b-152">Отношения назначений ресурсов</span><span class="sxs-lookup"><span data-stu-id="3f24b-152">Resource Assignment relationships</span></span>
<span data-ttu-id="3f24b-153">Чтобы обеспечить успешное обновление, необходимо правильно поддерживать следующие отношения:</span><span class="sxs-lookup"><span data-stu-id="3f24b-153">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="3f24b-154">Все назначения ресурсов в структурной декомпозиции работ должны быть связаны с тем же проектом.</span><span class="sxs-lookup"><span data-stu-id="3f24b-154">All Resource Assignments in a work breakdown structure must be related to the same project.</span></span>
- <span data-ttu-id="3f24b-155">Все назначения ресурсов в структурной декомпозиции работ должны быть связаны с участниками проектной рабочей группы в том же проекте.</span><span class="sxs-lookup"><span data-stu-id="3f24b-155">All Resource Assignments in a work breakdown structure must be associated to project team members in the same project.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="3f24b-156">Шаги по устранению потенциальных проблем</span><span class="sxs-lookup"><span data-stu-id="3f24b-156">Potential mitigation steps</span></span>
- <span data-ttu-id="3f24b-157">Выявите все задачи, не соответствующие приведенным выше условиям.</span><span class="sxs-lookup"><span data-stu-id="3f24b-157">Identify all tasks that fall outside the conditions described above.</span></span>  
- <span data-ttu-id="3f24b-158">Все назначения ресурсов, которые больше не действительны, необходимо удалить.</span><span class="sxs-lookup"><span data-stu-id="3f24b-158">Any Resource Assignments that are no longer valid should be deleted.</span></span>

## <a name="project-task-dependency-relationships"></a><span data-ttu-id="3f24b-159">Отношения зависимости задачи проекта</span><span class="sxs-lookup"><span data-stu-id="3f24b-159">Project task dependency relationships</span></span>
<span data-ttu-id="3f24b-160">Чтобы обеспечить успешное обновление, необходимо правильно поддерживать следующие отношения:</span><span class="sxs-lookup"><span data-stu-id="3f24b-160">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="3f24b-161">Все зависимости задач проекта должны быть связаны с одним и тем же проектом.</span><span class="sxs-lookup"><span data-stu-id="3f24b-161">All project task dependencies must be related to the same project.</span></span>
- <span data-ttu-id="3f24b-162">Задача не может иметь одну и ту же зависимость, на которую ссылаются более одного раза.</span><span class="sxs-lookup"><span data-stu-id="3f24b-162">A task can't have the same dependency referenced more than once.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]