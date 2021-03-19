---
title: Назначение ресурса задаче
description: В этом разделе представлена информация о том, как назначать ресурсы задачам.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
ms.topic: article
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
ms.openlocfilehash: 486371df2de8b400f200dbf38e66cb5e2dec7ae7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286264"
---
# <a name="assign-a-resource-to-a-task"></a><span data-ttu-id="f6e3b-103">Назначение ресурса задаче</span><span class="sxs-lookup"><span data-stu-id="f6e3b-103">Assign a resource to a task</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="f6e3b-104">Существует три способа назначить ресурс задаче в Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="f6e3b-104">There are three ways to assign a resource to a task in Microsoft Dynamics 365 Project Service Automation.</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="f6e3b-105">Резервирование ресурса как участника рабочей группы, затем назначение ресурса задаче</span><span class="sxs-lookup"><span data-stu-id="f6e3b-105">Book a resource as a team member, and then assign the resource to a task</span></span>

<span data-ttu-id="f6e3b-106">Можно добавить ресурс в рабочую группу проекта, затем назначить ресурс задачам в расписании проекта.</span><span class="sxs-lookup"><span data-stu-id="f6e3b-106">You can add a resource to the project team, and then assign the resource to tasks in the project schedule.</span></span>

1. <span data-ttu-id="f6e3b-107">На вкладке **Участник рабочей группы** добавьте нового участника рабочей группы, выбрав **Создать**.</span><span class="sxs-lookup"><span data-stu-id="f6e3b-107">On the **Team Member** tab, add a new team member by selecting **New**.</span></span> 

2. <span data-ttu-id="f6e3b-108">Открывается панель **быстрого создания участника рабочей группы**, на которой можно выбрать имя резервируемого ресурса и задать роль.</span><span class="sxs-lookup"><span data-stu-id="f6e3b-108">The **Team Member Quick Create** panel opens, where you can select the bookable resource name and set a role.</span></span> 

    <span data-ttu-id="f6e3b-109">Выберите один из следующих методов распределения для резервирования ресурса:</span><span class="sxs-lookup"><span data-stu-id="f6e3b-109">Select one of the following allocation methods for the resource’s booking:</span></span>

    - <span data-ttu-id="f6e3b-110">**Полная загрузка** резервирует полную загрузку ресурса для указанных дат от и до.</span><span class="sxs-lookup"><span data-stu-id="f6e3b-110">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="f6e3b-111">**Процент загрузки** резервирует ресурс для процент производительности ресурса для указанных дат от и до.</span><span class="sxs-lookup"><span data-stu-id="f6e3b-111">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="f6e3b-112">**По часам — распределить равномерно** резервирует ресурс для указанного количества часов, распределяя их равномерно по дням за указанные даты "от" и "до".</span><span class="sxs-lookup"><span data-stu-id="f6e3b-112">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing them evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="f6e3b-113">**По часам — передняя погрузка** резервирует ресурс для указанного количества часов с передней погрузкой часов по дням за указанные даты от и до.</span><span class="sxs-lookup"><span data-stu-id="f6e3b-113">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>
    - <span data-ttu-id="f6e3b-114">**Нет** добавляет ресурсы в рабочую группу, но не создает никаких резервирований, которые их загружают.</span><span class="sxs-lookup"><span data-stu-id="f6e3b-114">**None** adds the resource to the team but doesn’t create any bookings that absorb their capacity.</span></span>

3. <span data-ttu-id="f6e3b-115">В таблице **Расписание** для задач выберите значок **Ресурс** в ячейке ресурса, затем в разделе **Участники рабочей группы** выберите участника рабочей группы, которого вы только что добавили.</span><span class="sxs-lookup"><span data-stu-id="f6e3b-115">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell, and then under **Team Members**, select the team member you just added.</span></span> 

> [!NOTE]
> <span data-ttu-id="f6e3b-116">На вкладках **Участник рабочей группы** и **Выверка** для ресурса отображаются зарезервированные часы и назначенные часы.</span><span class="sxs-lookup"><span data-stu-id="f6e3b-116">On the **Team Member** and **Reconciliation** tabs, the resource shows booked and assigned hours.</span></span> <span data-ttu-id="f6e3b-117">Часы должны быть одинаковыми, но это не обязательно, так как резервирования и назначения не имеют жесткой связи.</span><span class="sxs-lookup"><span data-stu-id="f6e3b-117">The hours should be the same, but it isn't required as bookings and assignments are not tightly coupled.</span></span> <span data-ttu-id="f6e3b-118">Вкладка **Выверка** предоставляет сведения, когда эти значения не совпадают, например если ресурсу назначено больше часов, чем зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="f6e3b-118">The **Reconciliation** tab gives you details when they are different, such as when you assign a resource more hours than you have booked.</span></span> <span data-ttu-id="f6e3b-119">Если требуется, можно скорректировать сведения, либо расширяя резервирования ресурса, либо изменяя назначение.</span><span class="sxs-lookup"><span data-stu-id="f6e3b-119">If needed, you can correct the information by extending the resource's bookings or changing the assignment.</span></span>

## <a name="create-a-generic-team-member-through-task-assignment"></a><span data-ttu-id="f6e3b-120">Создание универсального участника рабочей группы через назначение задач</span><span class="sxs-lookup"><span data-stu-id="f6e3b-120">Create a generic team member through task assignment</span></span>

<span data-ttu-id="f6e3b-121">При создании универсального участника рабочей группы через назначение задачи создается местозаполнитель или универсальный ресурс, описывающий характеристики именованного ресурса, который должен в конечном счете работать на задачах.</span><span class="sxs-lookup"><span data-stu-id="f6e3b-121">When you create a generic team member through task assignment, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks.</span></span> <span data-ttu-id="f6e3b-122">Затем создается требование (или подается запрос с помощью этого требования), который используется для поиска и резервирования именованного ресурса.</span><span class="sxs-lookup"><span data-stu-id="f6e3b-122">You then generate a requirement (or submit a request using the requirement) that is used to search for and book the named resource.</span></span>

1. <span data-ttu-id="f6e3b-123">В таблице **Расписание** для задачи выберите значок **Ресурс** в ячейке ресурса.</span><span class="sxs-lookup"><span data-stu-id="f6e3b-123">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="f6e3b-124">Введите название, которое будет местозаполнителем для имени ресурса.</span><span class="sxs-lookup"><span data-stu-id="f6e3b-124">Type a name to serve as the placeholder resource’s name.</span></span> <span data-ttu-id="f6e3b-125">Например, Руководитель программы.</span><span class="sxs-lookup"><span data-stu-id="f6e3b-125">For example, Program Manager.</span></span>

3. <span data-ttu-id="f6e3b-126">Выберите **Создать** и в поле **Быстрое создание участника рабочей группы проекта** задайте роль для универсального ресурса.</span><span class="sxs-lookup"><span data-stu-id="f6e3b-126">Select **Create**, and in the **Quick Create Project Team Member** field, set the role for the generic resource.</span></span>

4. <span data-ttu-id="f6e3b-127">Вы можете продолжить назначать задачи этого ресурсу-местозаполнителю путем выбора ресурса в поле **Селектор ресурсов** для задачи.</span><span class="sxs-lookup"><span data-stu-id="f6e3b-127">You can continue to assign tasks to this placeholder resource by selecting the resource on the **Resource Selector** for the task.</span></span> <span data-ttu-id="f6e3b-128">Они отображаются в разделе **Участники рабочей группы**.</span><span class="sxs-lookup"><span data-stu-id="f6e3b-128">They’re listed under **Team Members**.</span></span>

5. <span data-ttu-id="f6e3b-129">Завершив назначение универсального ресурса, выберите этот универсальный ресурс на вкладке **Рабочая группа**, затем выберите **Создать требование**, чтобы создать требование ресурса для универсального ресурса.</span><span class="sxs-lookup"><span data-stu-id="f6e3b-129">When you’re done assigning the generic resource, select the generic resource on the **Team** tab, and then select **Generate Requirement** to create a resource requirement for the generic resource.</span></span>

6. <span data-ttu-id="f6e3b-130">Выберите **Резервировать** для универсального ресурса.</span><span class="sxs-lookup"><span data-stu-id="f6e3b-130">Select **Book** for the generic resource.</span></span> <span data-ttu-id="f6e3b-131">После этого можно использовать доску расписания для поиска и резервирования реального ресурса.</span><span class="sxs-lookup"><span data-stu-id="f6e3b-131">You can then use the Schedule board to find and book a real resource.</span></span> <span data-ttu-id="f6e3b-132">Можно также отправить требование для заполнения менеджером по ресурсам.</span><span class="sxs-lookup"><span data-stu-id="f6e3b-132">You can also submit the requirement for fulfillment by a resource manager.</span></span>

7. <span data-ttu-id="f6e3b-133">Когда универсальный ресурс заполняется именованным ресурсом, универсальный ресурс удаляется из участников группы, и назначения задач для универсального ресурса назначаются именованному ресурсу, который заполнив требования ресурса для универсального ресурса.</span><span class="sxs-lookup"><span data-stu-id="f6e3b-133">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a><span data-ttu-id="f6e3b-134">Назначение именованного ресурса из списка всех резервируемых ресурсов</span><span class="sxs-lookup"><span data-stu-id="f6e3b-134">Assign a named resource from the list of all bookable resources</span></span>

<span data-ttu-id="f6e3b-135">Окно поиска в области **Селектор ресурсов** можно использовать для поиска всех резервируемых ресурсов и назначения их задачам.</span><span class="sxs-lookup"><span data-stu-id="f6e3b-135">You can use the search box in the **Resource Selector** to search all bookable resources and assign them to a task.</span></span>

<span data-ttu-id="f6e3b-136">Ресурсы, назначенные таким образом, добавляются в рабочую группу без всяких резервирований.</span><span class="sxs-lookup"><span data-stu-id="f6e3b-136">Resources assigned this way are added to the team without any bookings.</span></span> <span data-ttu-id="f6e3b-137">Это подобно добавлению участников рабочей группы и выбору значения "Нет" в качестве способа распределения.</span><span class="sxs-lookup"><span data-stu-id="f6e3b-137">This is similar to adding a team member and selecting None as the allocation method.</span></span> <span data-ttu-id="f6e3b-138">Ресурс отображается на вкладках **Рабочая группа** и **Выверка** как ресурсы только с назначениями и дефицитом резервирования.</span><span class="sxs-lookup"><span data-stu-id="f6e3b-138">The resource is displayed in the **Team** and **Reconciliation** tabs as resources with only assignments and a booking deficit.</span></span> <span data-ttu-id="f6e3b-139">Зарезервируйте их, если требуется использовать их доступность.</span><span class="sxs-lookup"><span data-stu-id="f6e3b-139">Book them if you want to use their availability.</span></span>

1. <span data-ttu-id="f6e3b-140">В таблице **Расписание** для задачи выберите значок **Ресурс** в ячейке ресурса.</span><span class="sxs-lookup"><span data-stu-id="f6e3b-140">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="f6e3b-141">Начните вводить имя.</span><span class="sxs-lookup"><span data-stu-id="f6e3b-141">Start typing a name.</span></span> <span data-ttu-id="f6e3b-142">Результаты поиска для имени отображаются в области **Селектор ресурсов** в разделе **Другие ресурсы**.</span><span class="sxs-lookup"><span data-stu-id="f6e3b-142">The search results for the name are displayed in the **Resource Selector** under **Other Resources**.</span></span>

3. <span data-ttu-id="f6e3b-143">Выберите ресурс, который нужно назначить задаче.</span><span class="sxs-lookup"><span data-stu-id="f6e3b-143">Select the resource that you want to assign to the task.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]