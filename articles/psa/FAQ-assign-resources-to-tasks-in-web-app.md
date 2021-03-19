---
title: Как назначить резервируемый ресурс задаче в веб-приложении
description: Обзор способов назначения резервируемых ресурсов.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: b4296837cabd4c6f7e2d2924079658e45ce8b87c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286309"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a><span data-ttu-id="ed983-103">Как назначить резервируемый ресурс задаче в веб-приложении (приложение Project Service v2.x)?</span><span class="sxs-lookup"><span data-stu-id="ed983-103">How do I assign a bookable resource to a task in the web app (Project Service app v2.x)?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="ed983-104">Существует два способа назначить ресурс задаче в Project Service.</span><span class="sxs-lookup"><span data-stu-id="ed983-104">There are two ways to assign a resource to a task in Project Service.</span></span> <span data-ttu-id="ed983-105">Можно зарезервировать ресурс как участника рабочей группы, а затем назначить его задаче.</span><span class="sxs-lookup"><span data-stu-id="ed983-105">You can book a resource as a team member and then assign it to a task.</span></span> <span data-ttu-id="ed983-106">Кроме того, можно создать универсального участника рабочей группы через назначение роли для задач, создать рабочую группу, а затем выполнять требования по комплектованию с именованным ресурсом.</span><span class="sxs-lookup"><span data-stu-id="ed983-106">Or, you can create a generic team member through role assignment on tasks, generate a team, and then fulfill the backing requirements with a named resource.</span></span>

<span data-ttu-id="ed983-107">Обратите внимание, что если нужно назначить резервируемый ресурс задаче, участник группы резервируемого ресурса должен иметь достаточно доступных резервирований.</span><span class="sxs-lookup"><span data-stu-id="ed983-107">Note that if you’d like to assign a bookable resource to a task, the bookable resource team member must have enough available bookings.</span></span> <span data-ttu-id="ed983-108">Состояние резервирования должно быть типом исполнения "Окончательное резервирование" и состоянием "Исполнено".</span><span class="sxs-lookup"><span data-stu-id="ed983-108">The status of the booking must be Commit Type Hard Book and Status Committed.</span></span> <span data-ttu-id="ed983-109">Если нет достаточных резервирований для этого ресурса, Project Service удаляет назначение и выводит следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="ed983-109">If there aren’t enough bookings for the resource, Project Service removes the assignment and displays the following error message:</span></span>

<span data-ttu-id="ed983-110">*Не удалось назначить ресурс задаче — У следующих ресурсов нет достаточного количества часов, зарезервированных для проекта*</span><span class="sxs-lookup"><span data-stu-id="ed983-110">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project*</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="ed983-111">Резервирование ресурса как участника рабочей группы, затем назначение ресурса задаче</span><span class="sxs-lookup"><span data-stu-id="ed983-111">Book a resource as a team member and then assign the resource to a task</span></span>

<span data-ttu-id="ed983-112">При использовании этого метода вы добавляете ресурс в рабочую группу проекта, затем назначаете задачи ресурсу в расписании проекта.</span><span class="sxs-lookup"><span data-stu-id="ed983-112">With this method you add a resource to the project team and then assign tasks to the resource in the project schedule.</span></span> <span data-ttu-id="ed983-113">Вот как это делается:</span><span class="sxs-lookup"><span data-stu-id="ed983-113">Here’s how you do this:</span></span>
1.  <span data-ttu-id="ed983-114">В сетке участников рабочих групп добавьте нового участника рабочей группы, выбрав **Создать**.</span><span class="sxs-lookup"><span data-stu-id="ed983-114">On the team member grid, add a new team member by selecting **New**.</span></span>
2.  <span data-ttu-id="ed983-115">На экране быстрого создания участника рабочей группы выберите имя резервируемого ресурса и задайте роль.</span><span class="sxs-lookup"><span data-stu-id="ed983-115">On the Team Member Quick Create screen, select the bookable resource name and set a role.</span></span>
3.  <span data-ttu-id="ed983-116">Выберите даты **От** и **До**.</span><span class="sxs-lookup"><span data-stu-id="ed983-116">Select the **From** and **To** dates.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="ed983-117">![Снимок экрана с добавлением участника рабочей группы](media/FAQ-Resources-to-Tasks2-1.png "Снимок экрана с добавлением участника рабочей группы")</span><span class="sxs-lookup"><span data-stu-id="ed983-117">![Screenshot of adding team member](media/FAQ-Resources-to-Tasks2-1.png "Screenshot of adding team member")</span></span>
 
4.  <span data-ttu-id="ed983-118">Выберите один из следующих методов распределения для резервирования ресурса:</span><span class="sxs-lookup"><span data-stu-id="ed983-118">Select one of the following allocation methods for booking the resource:</span></span>
    - <span data-ttu-id="ed983-119">**Полная загрузка** резервирует полную загрузку ресурса для указанных дат от и до.</span><span class="sxs-lookup"><span data-stu-id="ed983-119">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="ed983-120">**Процент загрузки** резервирует ресурс для процент производительности ресурса для указанных дат от и до.</span><span class="sxs-lookup"><span data-stu-id="ed983-120">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="ed983-121">**По часам — распределить равномерно** резервирует ресурс для указанного количества часов, распределяя их равномерно по дням за указанные даты от и до.</span><span class="sxs-lookup"><span data-stu-id="ed983-121">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing it evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="ed983-122">**По часам — передняя погрузка** резервирует ресурс для указанного количества часов с передней погрузкой часов по дням за указанные даты от и до.</span><span class="sxs-lookup"><span data-stu-id="ed983-122">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>

    <span data-ttu-id="ed983-123">Не следует выбирать вариант **Нет**, поскольку он добавляет ресурсы в рабочую группу, но не создает никаких резервирований, которые загружают ресурс.</span><span class="sxs-lookup"><span data-stu-id="ed983-123">Don’t select **None** because it adds the resource to the team but doesn’t create any bookings that absorb the resource's capacity.</span></span>
5.  <span data-ttu-id="ed983-124">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="ed983-124">Select **Save**.</span></span>

    <span data-ttu-id="ed983-125">Обратите внимание, что часов резервирования должно быть достаточно, чтобы охватывать диапазоны часов и дат задач, на которые назначен этот ресурс.</span><span class="sxs-lookup"><span data-stu-id="ed983-125">Note that the hours of the booking must be enough to cover the effort hours and date ranges of the tasks that you assign this resource to.</span></span> <span data-ttu-id="ed983-126">Если они не находятся в соответствии, нельзя назначить ресурс задаче.</span><span class="sxs-lookup"><span data-stu-id="ed983-126">If they aren’t in alignment, you can’t assign the resource to the task.</span></span>

6.  <span data-ttu-id="ed983-127">На структурной декомпозиции работ (WBS) для задачи щелкните раскрывающееся меню ячейки ресурса.</span><span class="sxs-lookup"><span data-stu-id="ed983-127">On the work breakdown structure (WBS) for the task, click the resource cell dropdown.</span></span> <span data-ttu-id="ed983-128">Затем:</span><span class="sxs-lookup"><span data-stu-id="ed983-128">Then:</span></span> 

    1. <span data-ttu-id="ed983-129">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="ed983-129">Select **Add**.</span></span>
    2. <span data-ttu-id="ed983-130">Выберите раскрывающийся список по заголовком **Ресурсы** и выберите участника рабочей группы, который был добавлен выше.</span><span class="sxs-lookup"><span data-stu-id="ed983-130">Select the dropdown under **Resources** and select the team member you added above.</span></span>
    3. <span data-ttu-id="ed983-131">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="ed983-131">Select **OK**.</span></span> <span data-ttu-id="ed983-132">Участник команды теперь назначен задаче.</span><span class="sxs-lookup"><span data-stu-id="ed983-132">The team member is now assigned to the task.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="ed983-133">![Снимок экрана с добавлением ресурсов с помощью WBS](media/FAQ-Resources-to-Tasks2-2.png "Снимок экрана с добавлением ресурсов с помощью WBS")</span><span class="sxs-lookup"><span data-stu-id="ed983-133">![Screenshot of adding resources with WBS](media/FAQ-Resources-to-Tasks2-2.png "Screenshot of adding resources with WBS")</span></span>
 
<span data-ttu-id="ed983-134">В сетке участников рабочих групп вы увидите сводку назначенных часов ресурса в поле "Назначенные часы".</span><span class="sxs-lookup"><span data-stu-id="ed983-134">On the team member grid, you’ll see the aggregate of the resource’s assigned hours under Assigned Hours.</span></span> <span data-ttu-id="ed983-135">Значение будет меньше или равно зарезервированным часам для ресурса.</span><span class="sxs-lookup"><span data-stu-id="ed983-135">It will be less than or equal to the booked hours for the resource.</span></span> 

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="ed983-136">![Снимок экрана с назначенными часами для ресурса](media/FAQ-Resources-to-Tasks2-3.png "Снимок экрана с назначенными часами для ресурса")</span><span class="sxs-lookup"><span data-stu-id="ed983-136">![Screenshot of assigned hours for a resource](media/FAQ-Resources-to-Tasks2-3.png "Screenshot of assigned hours for a resource")</span></span>
 
<span data-ttu-id="ed983-137">Если задача, которую вы пытаетесь назначить ресурсу, начинается после конечной даты резервирований ресурса, ресурс не будет появляться в раскрывающемся списке".</span><span class="sxs-lookup"><span data-stu-id="ed983-137">If the task you’re attempting to assign to the resource starts after the end date of the resources bookings, the resource won’t appear in the dropdown.</span></span>

<span data-ttu-id="ed983-138">Обратите внимание, что можно назначить ресурсу больше часов, чем его зарезервированные часы, если ресурс имеет некоторую оставшуюся нераспределенную производительность.</span><span class="sxs-lookup"><span data-stu-id="ed983-138">Note that you can assign a resource to more hours than their booked hours if the resource has some remaining unassigned capacity.</span></span> <span data-ttu-id="ed983-139">В этом случае ресурс будет только частично назначен вплоть до его резервирований.</span><span class="sxs-lookup"><span data-stu-id="ed983-139">In this case the resource will only be partially assigned up to their bookings.</span></span> <span data-ttu-id="ed983-140">Можно просмотреть эти оставшиеся неназначенные часы задач, добавив столбец "Необеспеченные персоналом часы" в структурную декомпозицию работ.</span><span class="sxs-lookup"><span data-stu-id="ed983-140">You can see these remaining unassigned task hours by adding the Unstaffed Hours column to the work breakdown structure.</span></span>

<span data-ttu-id="ed983-141">Если ресурсам назначены все их зарезервированные часы (их зарезервированные часы равны их назначенным часам), вы увидите следующее сообщение об ошибке при попытке назначить им дополнительные задачи:</span><span class="sxs-lookup"><span data-stu-id="ed983-141">If resources are assigned to their booked hours (their booked hours equals their assigned hours), you’ll see the following error message when you attempt to assign them further tasks:</span></span>

<span data-ttu-id="ed983-142">*Не удалось назначить ресурс задаче — У следующих ресурсов нет достаточного количества часов, зарезервированных для проекта.*</span><span class="sxs-lookup"><span data-stu-id="ed983-142">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project.*</span></span>

<span data-ttu-id="ed983-143">Кроме того, участник рабочей группы руководителя проекта по умолчанию, который добавляется к группе при создании проекта, добавляется без каких-либо резервирований и ему не может быть назначена никакая задача.</span><span class="sxs-lookup"><span data-stu-id="ed983-143">Additionally, the default project manager team member that is added to the team when you create the project is added without any bookings and can’t be assigned to any task.</span></span> <span data-ttu-id="ed983-144">Они не отображаются в раскрывающемся списке ресурсов для задач.</span><span class="sxs-lookup"><span data-stu-id="ed983-144">They won’t show up in the resource dropdown for tasks.</span></span>

<span data-ttu-id="ed983-145">Если требуется назначить этот ресурс, необходимо удалить его из группы, а затем повторно добавить его, используя метод распределения, отличный от "Нет".</span><span class="sxs-lookup"><span data-stu-id="ed983-145">If you want to assign this resource, you need to remove them from the team and then re-add them with an allocation method other than None.</span></span> <span data-ttu-id="ed983-146">Причина их добавления в рабочую группу при создании проекта заключается в том, что проект должен иметь по крайней мере одного утверждающего по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ed983-146">The reason they’re added to the team when the project is created is so that a project has at least one project approver by default.</span></span>

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a><span data-ttu-id="ed983-147">Создание универсального участника рабочей группы через назначение роли для задач</span><span class="sxs-lookup"><span data-stu-id="ed983-147">Create a generic team member through role assignment on tasks</span></span>

<span data-ttu-id="ed983-148">Этот способ обеспечивает, что ресурсы имеют достаточно резервирований для задач.</span><span class="sxs-lookup"><span data-stu-id="ed983-148">This method assures that resources have enough bookings for tasks.</span></span> <span data-ttu-id="ed983-149">Во-первых, следует создать местозаполнитель или универсальный ресурс, описывающий характеристики именованного ресурса, который должен обязательно работать на задачах, путем создания рабочей группы после назначения ролей задачам.</span><span class="sxs-lookup"><span data-stu-id="ed983-149">First, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks by generating a team after assigning roles to tasks.</span></span> <span data-ttu-id="ed983-150">Вот как это делается:</span><span class="sxs-lookup"><span data-stu-id="ed983-150">Here’s how you do this:</span></span>

1. <span data-ttu-id="ed983-151">В структурной декомпозиции работ выберите задачу.</span><span class="sxs-lookup"><span data-stu-id="ed983-151">On the work breakdown structure, select a task.</span></span>
2. <span data-ttu-id="ed983-152">Выберите значок раскрывающегося списка **Назначенная роль** в ячейке ресурса.</span><span class="sxs-lookup"><span data-stu-id="ed983-152">Select the **Assigned Role** dropdown icon in the resource cell.</span></span>
3. <span data-ttu-id="ed983-153">Выберите раскрывающийся список **Роль** и выберите роль для универсального ресурса.</span><span class="sxs-lookup"><span data-stu-id="ed983-153">Select the **Role** dropdown and select the role for the generic resource.</span></span>
4. <span data-ttu-id="ed983-154">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="ed983-154">Select **OK**.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="ed983-155">![Снимок экрана с использованием WBS для добавления ресурсов](media/FAQ-Resources-to-Tasks2-4.png "Снимок экрана с использованием WBS для добавления ресурсов")</span><span class="sxs-lookup"><span data-stu-id="ed983-155">![Screenshot of using WBS to add resource](media/FAQ-Resources-to-Tasks2-4.png "Screenshot of using WBS to add resource")</span></span>
 
<span data-ttu-id="ed983-156">После завершения назначение ролей задачам в WBS выберите **Создать рабочую группу проекта**.</span><span class="sxs-lookup"><span data-stu-id="ed983-156">Once you’ve completed assigning roles to the tasks in the WBS, select **Generate Project Team**.</span></span> <span data-ttu-id="ed983-157">Project Service создает минимальное количество универсальных участников рабочей группы на основе ролей, подразделений для выделения ресурсов и календаря проекта путем суммирования назначений задач.</span><span class="sxs-lookup"><span data-stu-id="ed983-157">Project Service creates the minimum number of generic team members based on the roles, resourcing organization units, and project calendar by aggregating the task assignments.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="ed983-158">![Снимок экрана с созданием рабочей группы проекта](media/FAQ-Resources-to-Tasks2-5.png "Снимок экрана с созданием рабочей группы проекта")</span><span class="sxs-lookup"><span data-stu-id="ed983-158">![Screenshot of generating project team](media/FAQ-Resources-to-Tasks2-5.png "Screenshot of generating project team")</span></span>
 
<span data-ttu-id="ed983-159">В сетке участников рабочей группы можно видеть ресурсы типа "Универсальный ресурс" с именем ролей и должностей.</span><span class="sxs-lookup"><span data-stu-id="ed983-159">On the Team Member grid, you’ll see resources of the Generic Resource type with the role and position name.</span></span> <span data-ttu-id="ed983-160">Если два ресурса нужны для того, чтобы роль выполнила работу, функция "Создать рабочую группу" создает двух участников рабочей группы и использует имя должности для их разделения.</span><span class="sxs-lookup"><span data-stu-id="ed983-160">If two resources are needed for a role to complete the work, the Generate Team feature creates two team members and uses position name to set them apart.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="ed983-161">![Снимок экрана с добавлением двух универсальных ресурсов](media/FAQ-Resources-to-Tasks2-6.png "Снимок экрана с добавлением двух универсальных ресурсов")</span><span class="sxs-lookup"><span data-stu-id="ed983-161">![Screenshot of adding two generic resources](media/FAQ-Resources-to-Tasks2-6.png "Screenshot of adding two generic resources")</span></span>
 
<span data-ttu-id="ed983-162">Можно открыть потребность в комплектации ресурсов для универсального участника рабочей группы, выбрав ссылку под пунктом "Требование ресурса".</span><span class="sxs-lookup"><span data-stu-id="ed983-162">You can open the backing resource requirement for the generic team member by selecting the link under Resource Requirement.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="ed983-163">![Снимок экрана с открытием потребности в комплектации ресурса](media/FAQ-Resources-to-Tasks2-7.png "Снимок экрана с открытием потребности в комплектации ресурса")</span><span class="sxs-lookup"><span data-stu-id="ed983-163">![Screenshot of opening backing resource requirement](media/FAQ-Resources-to-Tasks2-7.png "Screenshot of opening backing resource requirement")</span></span>

<span data-ttu-id="ed983-164">Выберите **Резервировать** для универсального ресурса, после чего можно будет использовать доску расписания для поиска и резервирования реального ресурса.</span><span class="sxs-lookup"><span data-stu-id="ed983-164">Select **Book** for the generic resource, and then you can use the schedule board to find and book a real resource.</span></span> <span data-ttu-id="ed983-165">Можно также отправить требование для заполнения менеджером по ресурсам, выбрав **Отправить запрос**.</span><span class="sxs-lookup"><span data-stu-id="ed983-165">You can also submit the requirement for fulfillment by a resource manager by selecting **Submit Request**.</span></span>

<span data-ttu-id="ed983-166">Когда универсальный ресурс заполняется именованным ресурсом, универсальный ресурс удаляется из участников группы, и назначения задач для универсального ресурса назначаются именованному ресурсу, который заполнив требования ресурса для универсального ресурса.</span><span class="sxs-lookup"><span data-stu-id="ed983-166">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>
 



[!INCLUDE[footer-include](../includes/footer-banner.md)]