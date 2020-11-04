---
title: Управление ресурсами
description: В этой теме содержится информация об управлении ресурсами.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/13/2019
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
ms.openlocfilehash: 5b34ad66750dba9459d551a2527c13111196511e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083389"
---
# <a name="manage-resources"></a><span data-ttu-id="cb6c6-103">Управление ресурсами</span><span class="sxs-lookup"><span data-stu-id="cb6c6-103">Manage resources</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="cb6c6-104">Dynamics 365 Project Service Automation включает панель мониторинга для управления ресурсами, которая содержит визуальные общие сведения о потребности в ресурсе и его использовании в организации.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-104">Dynamics 365 Project Service Automation includes a resource manager dashboard that provides a visual overview of resource demand and utilization throughout the organization.</span></span> <span data-ttu-id="cb6c6-105">Графики на этой панели мониторинга можно использовать для визуализации следующей информации:</span><span class="sxs-lookup"><span data-stu-id="cb6c6-105">You can use the charts on this dashboard to visualize the following information:</span></span>

- <span data-ttu-id="cb6c6-106">**Требования ресурса** — диаграмма **Активные запросы ресурсов** показывает ресурсы, которые были отправлены.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-106">**Resource demand** – The **Active Resource Request** chart shows resources that have been submitted.</span></span> <span data-ttu-id="cb6c6-107">Ресурсы объединяются по роли или по проекту.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-107">The resources are aggregated by either role or project.</span></span>
- <span data-ttu-id="cb6c6-108">**Неотправленные требования ресурса** — диаграмма **Неназначенный спрос на ресурс** показывает все потребности в ресурсах, которые еще не отправлены.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-108">**Unsubmitted resource demand** – The **Unassigned Resource Demand** chart shows all the resource requirements that haven't been submitted.</span></span> <span data-ttu-id="cb6c6-109">Это помогает менеджерам по ресурсам просматривать спрос, который не подтвержден и может быть выставлен через запрос ресурса.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-109">It helps resource managers view demand that isn't firm and might be submitted through a resource request.</span></span>
- <span data-ttu-id="cb6c6-110">**Оплачиваемая загруженность за последнюю неделю** — диаграмма **Загруженность по роли** отображает процент оплачиваемой фактической загруженности организации по ролям относительно целевой оплачиваемой загруженности по ролям.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-110">**Billable utilization for the past week** – The **Utilization by Role** chart shows the percentage of the organization's actual billable utilization by role against its target billable utilization by role.</span></span>

    > [!NOTE]
    > <span data-ttu-id="cb6c6-111">Чтобы сделать диаграмму **Загруженность по роли** доступной, создайте задание. которое запускает рабочий процесс UpdateRoleUtilization.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-111">To make the **Utilization by Role** chart available, create a job that runs the UpdateRoleUtilization workflow.</span></span> <span data-ttu-id="cb6c6-112">Это повторяющееся задание выполняется каждые семь дней для вычисления оплачиваемой загруженности за предыдущие семь дней.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-112">This recurring job runs every seven days to calculate billable utilization for the previous seven days.</span></span> <span data-ttu-id="cb6c6-113">Результаты объединяются по ролям.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-113">The results are aggregated by role.</span></span>

## <a name="manage-project-team-members"></a><span data-ttu-id="cb6c6-114">Управление участниками проектной рабочей группы</span><span class="sxs-lookup"><span data-stu-id="cb6c6-114">Manage project team members</span></span>

<span data-ttu-id="cb6c6-115">Руководители проекта могут использовать панель мониторинга менеджера по ресурсам для управления ресурсами по проектам.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-115">Project managers can use the resource manager dashboard to manage the resources on projects.</span></span> <span data-ttu-id="cb6c6-116">Например, они могут добавить участника рабочей группы непосредственно в проект и зарезервировать участника рабочей группы для выполнения потребности в ресурсах, которые были зарегистрированы для универсального ресурса.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-116">For example, they can add a team member directly to a project and book a team member to fulfill the resource requirements that were captured by a generic resource.</span></span>

### <a name="add-a-team-member-directly-to-a-project"></a><span data-ttu-id="cb6c6-117">Добавление участника рабочей группы непосредственно в проект</span><span class="sxs-lookup"><span data-stu-id="cb6c6-117">Add a team member directly to a project</span></span>

<span data-ttu-id="cb6c6-118">Чтобы добавить участника рабочей группы непосредственно в проект, на странице **Проекты** на вкладке **Рабочая группа** , выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-118">To add a team member directly to a project, on the **Projects** page, on the **Team** tab, select **New**.</span></span> <span data-ttu-id="cb6c6-119">Открывается диалоговое окно **Быстрое создание:Участник проектной группы**.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-119">The **Quick Create:Project Team Member** dialog box appears.</span></span> <span data-ttu-id="cb6c6-120">В этом диалоговом окне можно выполнить следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="cb6c6-120">In this dialog box, you can perform these tasks:</span></span>

- <span data-ttu-id="cb6c6-121">**Зарезервировать именованный ресурс** — в поле **Резервируемый ресурс** выберите имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-121">**Book a named resource** – In the **Bookable Resource** field, select the name of the resource.</span></span> <span data-ttu-id="cb6c6-122">Затем выберите роль, задайте период и выберите способ распределения.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-122">Then select the role, set the period, and select an allocation method.</span></span> <span data-ttu-id="cb6c6-123">Выбранный именованный ресурс добавляется в проект с помощью выбранного способа распределения и календаря ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-123">The named resource that you selected is added to the project by using the selected allocation method and the resources calendar.</span></span>
- <span data-ttu-id="cb6c6-124">**Добавление универсального ресурса** — оставьте поле **Резервируемый ресурс** пустым, затем выберите роль, задайте период и выберите предпочитаемый способ распределения.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-124">**Add a generic resource** – Leave the **Bookable resource** field blank, and then select the role, set the period, and select the preferred allocation method.</span></span> <span data-ttu-id="cb6c6-125">Универсальный ресурс добавляется в рабочую группу в качестве заполнителя для резервирования схемы требования, которая используется для резервирования именованных ресурсов в рабочей группе.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-125">A generic resource is added to the team as a placeholder to hold the demand pattern that is used to book named resources on the team.</span></span> <span data-ttu-id="cb6c6-126">Требование осуществляться в соответствии с календарем проекта.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-126">The requirement is made according to the project calendar.</span></span>
- <span data-ttu-id="cb6c6-127">**Добавление именованного ресурса в рабочую группу без потребления производительности ресурса** — в поле **Резервируемый ресурс** выберите ресурс.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-127">**Add a named resource to the team without consuming resource capacity** – In the **Bookable Resource** field, select a resource.</span></span> <span data-ttu-id="cb6c6-128">Затем выберите период и задайте **Нет** в качестве способа распределения.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-128">Then select the period, and select **None** as the allocation method.</span></span> <span data-ttu-id="cb6c6-129">Ресурс добавляется к рабочей группе, но производительность ресурса не потребляется при резервировании.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-129">The resource is added to the team, but the resource's capacity isn't consumed through a booking.</span></span>

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a><span data-ttu-id="cb6c6-130">Резервирование участников рабочей группы для выполнения потребности в ресурсах для универсального ресурса</span><span class="sxs-lookup"><span data-stu-id="cb6c6-130">Book a team member to fulfill resource requirements for a generic resource</span></span>

<span data-ttu-id="cb6c6-131">В PSA можно зарезервировать универсальный ресурс в рабочей группе проекта и можно определить роль, необходимую производительность и порядок распределения производительности.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-131">In PSA, you can book a generic resource on a project team, and can specify the role, the required capacity, and how that capacity is distributed.</span></span> <span data-ttu-id="cb6c6-132">В требовании ресурса можно определить атрибуты, связанные с универсальным ресурсом.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-132">On the resource requirement, you can specify attributes that are associated with the generic resource.</span></span> <span data-ttu-id="cb6c6-133">Данные атрибуты включают необходимые навыки, предпочтительное подразделение и предпочтительные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-133">These attributes include required skills, the preferred organizational unit, and preferred resources.</span></span>

<span data-ttu-id="cb6c6-134">Выполните следующие действия. чтобы определить необходимые навыки в универсальном ресурсе для разработчика.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-134">Follow these steps to specify required skills on a generic resource for a developer.</span></span>

1. <span data-ttu-id="cb6c6-135">На странице **Проекты** на вкладке **Рабочая группа** выберите **Создать** для резервирования универсального ресурса.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-135">On the **Projects** page, on the **Team** tab, select **New** to book a generic resource.</span></span>

    ![Универсальный ресурс, зарезервированный для рабочей группы](media/Resource-Management-image9.png)

2. <span data-ttu-id="cb6c6-137">В представлении **Все участники рабочей группы** в столбце **Требование ресурса** выберите ссылку для добавления необходимых навыков для универсального ресурса.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-137">In the **All Team Members** view, in the **Resource Requirement** column, select the link to add required skills for the generic resource.</span></span>

    ![Ссылка требования](media/Resource-Management-image10.png)

3. <span data-ttu-id="cb6c6-139">На странице **Требование ресурса** , которая появляется в сетке **Навыки** , выберите многоточие ( **...** ), затем выберите **Добавить новую характеристику требования** , чтобы добавить необходимый навык для разработчика.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-139">On the **Resource Requirement** page that appears, in the **Skills** grid, select the ellipsis ( **...** ) and then select **Add New Requirement Characteristic** to add the required skills for your developer.</span></span>

    ![Команда добавления новой характеристики требования](media/Resource-Management-image11.png)

4. <span data-ttu-id="cb6c6-141">В открывшемся диалоговом окне **Быстрое создание: характеристика требования** в поле **Характеристика** выберите необходимый навык.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-141">In the **Quick Create: Requirement Characteristic** dialog box that appears, in the **Characteristic** field, select the required skill.</span></span> <span data-ttu-id="cb6c6-142">Затем в поле **Значение оценки** выберите уровень квалификации для данного навыка.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-142">Then, in the **Rating value** field, select the proficiency level for that skill.</span></span> <span data-ttu-id="cb6c6-143">В заключение, в поле **Требование ресурса** , задайте требования для подбора ресурсов из подразделений или даже именованных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-143">Finally, in the **Resource Requirement** field, set the requirement to source resources from organizational units or even named resources.</span></span> <span data-ttu-id="cb6c6-144">По завершении выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-144">When you've finished, select **Save**.</span></span>

    ![Диалоговое окно "Быстрое создание: характеристика требования"](media/Resource-Management-image12.png)

5. <span data-ttu-id="cb6c6-146">На странице **Требование ресурса** выберите **Резервировать** для выполнения потребности в ресурсах.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-146">On the **Resource Requirement** page, select **Book** to fulfill the resource requirement.</span></span>

    ![Кнопка резервирования на странице требования ресурса](media/Resource-Management-image13.png)

    <span data-ttu-id="cb6c6-148">Можно также выбрать универсальный ресурс в сетке **Все участники рабочей группы** , затем выберите **Резервировать**.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-148">You can also select the generic resource in the **All Team Members** grid and then select **Book**.</span></span>

    ![Кнопка резервирования над сеткой участников рабочей группы](media/Resource-Management-image14.png)

    > [!NOTE]
    > <span data-ttu-id="cb6c6-150">В этом примере имеется 40 необходимых часов, но нет фактических зарезервированных часов, поскольку универсальные ресурсы не имеют резервирования.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-150">In this example, there are 40 required hours but no actual booked hours, because generic resources don't have bookings.</span></span> <span data-ttu-id="cb6c6-151">Кроме того, нет назначенных часов, поскольку универсальный ресурс был добавлен непосредственно в рабочую группу.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-151">Additionally, there are no assigned hours, because the generic resource was added directly to the team.</span></span> <span data-ttu-id="cb6c6-152">Он не был добавлен с использованием назначения задачи.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-152">It wasn't added by using task assignment.</span></span>

    <span data-ttu-id="cb6c6-153">На странице **Помощник планирования** можно фильтровать доступные ресурсы по требованиям, которые указаны в потребности в ресурсах.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-153">On the **Scheduling Assistant** page, you can filter available resources by the requirements that are specified on the resource requirement.</span></span> <span data-ttu-id="cb6c6-154">Ресурсы сортируются по параметрам сортировки, которые определяются на доске расписания.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-154">Resources are sorted according to the sorting parameters that are specified on the Schedule Board.</span></span>

    ![Страница помощника по расписанию](media/Resource-Management-image15.png)

    <span data-ttu-id="cb6c6-156">Вот некоторые фильтры, которые часто используются:</span><span class="sxs-lookup"><span data-stu-id="cb6c6-156">Here are some filters that are often used:</span></span>

    - <span data-ttu-id="cb6c6-157">**Характеристики вместе с оценкой** — фильтрация по навыкам, полученным сертификатам и другими качествами ресурса, в дополнение к оценкам квалификации.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-157">**Characteristics along with a rating** – Filter by skills, certifications, and other resource qualities, in addition to ratings of proficiency.</span></span>
    - <span data-ttu-id="cb6c6-158">**Роли** — фильтрация по ролям по умолчанию, которые назначены резервируемым ресурсам.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-158">**Roles** – Filter by the default roles that are assigned to bookable resources.</span></span>
    - <span data-ttu-id="cb6c6-159">**Подразделения** — фильтрация резервируемых ресурсов по подразделениям, которым они назначены.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-159">**Organizational units** – Filter bookable resources by the organizational units that they are assigned to.</span></span>

6. <span data-ttu-id="cb6c6-160">Если вы не удовлетворены результатами начального поиска требований, можно изменить условия фильтра.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-160">If you aren't satisfied with the results of the initial requirement search, you can change the filter criteria.</span></span> <span data-ttu-id="cb6c6-161">Разверните область **Представление фильтра** слева, затем выберите **Поиска** для поиска дополнительных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-161">Expand the **Filter View** pane on the left, and then select **Search** to find additional resources.</span></span>

    ![Область представления фильтра](media/Resource-Management-image16.png)

7. <span data-ttu-id="cb6c6-163">Чтобы изменить способ сортировки результатов, выберите **Сортировка**.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-163">To change how the results are sorted, select **Sort**.</span></span>

    ![Команда сортировки](media/Resource-Management-image17.png)

8. <span data-ttu-id="cb6c6-165">Выберите ресурсы в соответствии с требованием, которое указано в требовании, как показано вверху сетки.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-165">Select resources according to the demand that is specified on the requirement, as indicated at the top of the grid.</span></span> <span data-ttu-id="cb6c6-166">Можно очистить выбор ячеек в сетке и оставить эту производительность ресурса открытой.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-166">You can clear the selection of cells in the grid and leave that resource capacity open.</span></span> <span data-ttu-id="cb6c6-167">Только один ресурс одновременно может быть выбран как зарезервированный.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-167">Only one resource at a time can be selected as booked.</span></span>

9. <span data-ttu-id="cb6c6-168">Выберите **Резервировать** , чтобы зарезервировать ресурс и оставить доску расписания открытой, чтобы можно было выбрать дополнительные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-168">Select **Book** to book the selected resource and leave the Schedule Board open, so that you can select additional resources.</span></span> <span data-ttu-id="cb6c6-169">В качестве альтернативы выберите **Зарезервировать и выйти** , чтобы зарезервировать книгу выбранный ресурс и закрыть доску расписания.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-169">Alternatively, select **Book & Exit** to book the selected resource and close the Schedule Board.</span></span>

    ![Ресурс для резервирования](media/Resource-Management-image19.png)

    <span data-ttu-id="cb6c6-171">Вы получаете уведомление о зарезервированных рабочих часах.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-171">You receive a notification about booked hours.</span></span> <span data-ttu-id="cb6c6-172">Указатели спроса показывают, сколько требований резервирования удовлетворено и сколько остается.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-172">The demand indicators show how much the booking requirement is satisfied and how much remains.</span></span> <span data-ttu-id="cb6c6-173">Можно также увидеть, какая часть производительности выбранного ресурса потреблена.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-173">You can also see how much of the selected resource's capacity is consumed.</span></span> <span data-ttu-id="cb6c6-174">Выберите **Развернуть** для просмотра подробных сведений о резервированиях ресурса.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-174">Select **Expand** to view more details about resource bookings.</span></span>

9. <span data-ttu-id="cb6c6-175">Вернитесь в представление **Все участники рабочей группы**.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-175">Return to the **All Team Members** view.</span></span> <span data-ttu-id="cb6c6-176">В сетке обратите внимание, что универсальный ресурс был заменен именованным ресурсом, и 40 часов указаны как зарезервированные для данного ресурса.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-176">In the grid, notice that the generic resource has been replaced by the named resource, and 40 hours are listed as booked for that resource.</span></span>

    ![Обновленная сетка участников рабочей группы](media/Resource-Management-image20.png)

    > [!NOTE]
    > <span data-ttu-id="cb6c6-178">Никакие назначенные часы не отображаются, поскольку они зарезервированы непосредственно на рабочую группу.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-178">No assigned hours are shown, because they were booked directly on the team.</span></span> <span data-ttu-id="cb6c6-179">Они не были зарезервированы с использованием назначения задачи.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-179">They weren't booked by using task assignment.</span></span>

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a><span data-ttu-id="cb6c6-180">Назначение универсальных ресурсов задачам и создание потребностей в ресурсах</span><span class="sxs-lookup"><span data-stu-id="cb6c6-180">Assign generic resources to tasks and generate resource requirements</span></span>

<span data-ttu-id="cb6c6-181">В PSA можно создавать задачи, а затем назначить им универсальные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-181">In PSA, you can create tasks and then assign generic resources to them.</span></span> <span data-ttu-id="cb6c6-182">Таким образом,потребность в ресурсах может быть представлена местозаполнителями ,пока вы оцениваете расписание и финансовые показатели.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-182">In this way, resource demand can be represented by placeholders while you estimate your schedule and financial numbers.</span></span> <span data-ttu-id="cb6c6-183">Затем можно создать требования ресурсов для универсальных ресурсов и выполнить их.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-183">You can then generate resource requirements for the generic resources and fulfill them.</span></span>

1. <span data-ttu-id="cb6c6-184">На странице **Проекты** на вкладке **Расписание** выберите **Добавить** для создания задачи.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-184">On the **Projects** page, on the **Schedule** tab, select **Add** to create a task.</span></span>

    ![Создана новая задача](media/Resource-Management-image21.png)

2. <span data-ttu-id="cb6c6-186">В поле **Ресурсы** выберите символ **Средство выбора ресурсов**.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-186">In the **Resources** field, select the **Resource Picker** symbol.</span></span> <span data-ttu-id="cb6c6-187">Появится средство выбора ресурса, который показывает существующих участников рабочей группы для проекта.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-187">The Resource Picker appears and shows existing team members for the project.</span></span>

    ![Средство выбора ресурсов](media/Resource-Management-image22.png)

3. <span data-ttu-id="cb6c6-189">Введите имя нового универсального ресурса, затем выберите команду **Создать**.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-189">Enter the name of the new generic resource, and then select **Create**.</span></span>

    ![Введенное имя нового универсального ресурса](media/Resource-Management-image23.png)

4. <span data-ttu-id="cb6c6-191">В открывшемся диалоговом окне **Быстрое создание: участник проектной группы** в поле **Роль** выберите роль для универсального ресурса.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-191">In the **Quick Create: Project Team Member** dialog box that appears, in the **Role** field, select the role for the generic resource.</span></span> <span data-ttu-id="cb6c6-192">В поле **Единица распределения ресурсов** выберите подразделение для универсального ресурса.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-192">In the **Resourcing Unit** field, select the organizational unit for the generic resource.</span></span> <span data-ttu-id="cb6c6-193">Затем выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-193">Then select **Save**.</span></span>

    ![Диалоговое окно "Быстрое создание: участник проектной группы"](media/Resource-Management-image24.png)

    <span data-ttu-id="cb6c6-195">Универсальный участник рабочей группы теперь назначен задаче.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-195">The generic team member is now assigned to the task.</span></span>

    ![Универсальный участник рабочей группы назначен задаче](media/Resource-Management-image25.png)

    <span data-ttu-id="cb6c6-197">На вкладке **Рабочая группа** можно увидеть нового универсального участника рабочей группы.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-197">On the **Team** tab, you will see the new generic team member.</span></span> <span data-ttu-id="cb6c6-198">Обратите внимание, что он имеет только назначенные часы.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-198">Notice that it has only assigned hours.</span></span> <span data-ttu-id="cb6c6-199">Эти часы являются суммой всех задач, которые назначены универсальному участнику рабочей группы.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-199">These hours are the sum of all tasks that are assigned to the generic team member.</span></span> <span data-ttu-id="cb6c6-200">Универсальный участник рабочей группы еще не имеет необходимых часов или требования ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-200">The generic team member doesn't yet have required hours or a resource requirement.</span></span>

    ![Универсальный участник рабочей группы на вкладке рабочей группы](media/Resource-Management-image26.png)

5. <span data-ttu-id="cb6c6-202">Теперь можно назначить универсального участника рабочей группы другим задачам с помощью средства выбора ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-202">You can now assign the generic team member to other tasks by using the Resource Picker.</span></span>

    ![Универсальный участник рабочей группы в средстве выбора ресурсов](media/Resource-Management-image27.png)

    <span data-ttu-id="cb6c6-204">Закончив назначать универсальный ресурс задачам, можно создать требование ресурсов для универсального ресурса.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-204">When you've finished assigning the generic resource to tasks, you can generate a resource requirement for the generic resource.</span></span>

5. <span data-ttu-id="cb6c6-205">На вкладке **Рабочая группа** выберите универсальный ресурс, затем выберите **Создать требование**.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-205">On the **Team** tab, select the generic resource, and then select **Generate Requirement**.</span></span>

    ![Команда "Создать требование"](media/Resource-Management-image28.png)

    <span data-ttu-id="cb6c6-207">Когда требование создано, универсальный участник рабочей группы будет иметь необходимые часы и ссылку на требование ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-207">When the requirement is generated, the generic team member will have required hours and a link for the resource requirement.</span></span>

    ![Ссылка требования ресурса](media/Resource-Management-image29.png)

    <span data-ttu-id="cb6c6-209">После резервирования именованного ресурса универсальный ресурс удаляется из рабочей группы и заменяется именованным ресурсом.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-209">After you book a named resource, the generic resource is removed from the team and replaced by the named resource.</span></span>

    ![Универсальный ресурс заменен именованным ресурсом](media/Resource-Management-image30.png)

    <span data-ttu-id="cb6c6-211">На вкладке **Расписание** , назначения универсального ресурса удаляются и заменяются именованным ресурсом.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-211">On the **Schedule** tab, the generic resource assignments are removed and replaced by the named resource.</span></span>

    ![Назначения универсального ресурса заменены именованным ресурсом на вкладке "Расписание"](media/Resource-Management-image31.png)

    > [!NOTE]
    > <span data-ttu-id="cb6c6-213">Это поведение возникает только тогда, когда именованный ресурс полностью зарезервирован для требования универсального ресурса.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-213">This behavior occurs only when a named resource is fully booked for the generic resource requirement.</span></span> <span data-ttu-id="cb6c6-214">Когда именованный ресурс частично заменяет требование универсального ресурса или несколько именованных ресурсов заменяют требование универсального ресурса, универсальный ресурс остается назначенным задаче.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-214">When either a named resource partially replaces the generic resource requirement or multiple named resources replace the generic resource requirement, the generic resource remains assigned to the task.</span></span>

    <span data-ttu-id="cb6c6-215">На следующем рисунке задача на 80 часов была запланирована для пятидневной длительности (16 часов в день в течение пяти дней) и была назначена универсальному ресурсу с именем **Функциональный**.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-215">In the following illustration, an 80-hour task has been planned for a five-day duration (16 hours per day over five days) and assigned to the generic resource that is named **Functional**.</span></span>

    ![Задача на 80 часов и пять дней назначена универсальному ресурсу "Функциональный"](media/Resource-Management-image32.png)

    <span data-ttu-id="cb6c6-217">При создании требования оно создается на 80 часов в течение пяти дней.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-217">When you generate the requirement, it's for 80 hours over five days.</span></span>

    ![Требование, созданное для 80 часов на пять дней](media/Resource-Management-image33.png)

    <span data-ttu-id="cb6c6-219">Поскольку доступные ресурсы работают только восемь часов в день, два ресурса необходимы для выполнения требования.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-219">Because available resources work only eight hours per day, two resources are needed to fulfill the requirement.</span></span>

    ![Второй ресурс](media/Resource-Management-image35.png)

    <span data-ttu-id="cb6c6-221">На вкладке **Рабочая группа** теперь можно видеть, что универсальный ресурс не имеет необходимых часов, но назначенные часы по-прежнему находятся вместе с двумя именованными ресурсами, которые составляют выполнение.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-221">On the **Team** tab, you can now see that the generic resource has no required hours, but the assigned hours still appear together with the two named resources that make up the fulfillment.</span></span>

    ![Два именованных ресурса на вкладке рабочей группы](media/Resource-Management-image36.png)

    <span data-ttu-id="cb6c6-223">На вкладке **Расписание** универсальный ресурс остается назначенным задаче.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-223">On the **Schedule** tab, the generic resource remains assigned to the task.</span></span>

    ![Универсальные ресурсы на вкладке расписания](media/Resource-Management-image37.png)

<span data-ttu-id="cb6c6-225">PSA не назначает оба ресурса задаче, поскольку это поведение произвело бы менее прогнозируемое расписание.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-225">PSA doesn't assign both resources to the task, because that behavior would produce a less predictable schedule.</span></span> <span data-ttu-id="cb6c6-226">В этом простом примере легко разделить часы поровну между двумя ресурсами.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-226">In this simple example, it's easy to divide the hours equally between two resources.</span></span> <span data-ttu-id="cb6c6-227">Тем не менее, в более сложных сценариях, которые содержат несколько задач и несколько ресурсов, PSA должен был бы сделать предположения о том, как следует выделить резервирования, которые получены для нескольких ресурсов на несколько задач.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-227">However, in more complex scenarios that involve multiple tasks and multiple resources, PSA would have to make assumptions about how it should allocate the bookings that are received for multiple resources across multiple tasks.</span></span>

<span data-ttu-id="cb6c6-228">Следовательно, в этих сценариях" руководитель проекта отвечает за разделение нескольких резервирований и их назначение по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-228">Therefore, in these scenarios, the project manager is responsible for parsing the multiple bookings and assigning them as needed.</span></span> <span data-ttu-id="cb6c6-229">Чтобы выделить резервирования, руководителя проекта назначает задачи из универсальных ресурсов именованным ресурсам, затем использует представление **Выверка** , чтобы убедиться, что выделение работает с этими резервированиями.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-229">To allocate the bookings, the project manager assigns the tasks from the generic resources to the named resources and then uses the **Reconciliation** view to make sure that the allocation works with the bookings.</span></span>

### <a name="edit-a-resource-requirement"></a><span data-ttu-id="cb6c6-230">Изменение требования ресурса</span><span class="sxs-lookup"><span data-stu-id="cb6c6-230">Edit a resource requirement</span></span>

<span data-ttu-id="cb6c6-231">После того как будет создано требование ресурсов, руководитель проекта или менеджер ресурсов может захотеть изменить сведения, чтобы уточнить условия поиска при использовании доски расписания.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-231">After a resource requirement has been created, a project manager or resource manager might want to edit the details to refine the search criteria when the Schedule Board is used.</span></span> <span data-ttu-id="cb6c6-232">Для редактирования потребности в ресурсах выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-232">To edit the resource requirement, follow these steps.</span></span>

1. <span data-ttu-id="cb6c6-233">На странице **Проекты** на вкладке **Рабочая группа** выберите ссылку на любое требование универсального ресурса.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-233">On the **Projects** page, on the **Team** tab, select the link to any requirement on a generic resource.</span></span>
2. <span data-ttu-id="cb6c6-234">На открывшейся странице **Требование ресурса** можно обновить несколько атрибутов.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-234">On the **Resource Requirement** page that appears, you can update several attributes.</span></span> <span data-ttu-id="cb6c6-235">Ниже приведено несколько примеров:</span><span class="sxs-lookup"><span data-stu-id="cb6c6-235">Here are some examples:</span></span>

    - <span data-ttu-id="cb6c6-236">Имя</span><span class="sxs-lookup"><span data-stu-id="cb6c6-236">Name</span></span>
    - <span data-ttu-id="cb6c6-237">С даты</span><span class="sxs-lookup"><span data-stu-id="cb6c6-237">From Date</span></span>
    - <span data-ttu-id="cb6c6-238">По дату</span><span class="sxs-lookup"><span data-stu-id="cb6c6-238">To Date</span></span>
    - <span data-ttu-id="cb6c6-239">Длительность</span><span class="sxs-lookup"><span data-stu-id="cb6c6-239">Duration</span></span>
    - <span data-ttu-id="cb6c6-240">Тип ресурса</span><span class="sxs-lookup"><span data-stu-id="cb6c6-240">Resource Type</span></span>

<span data-ttu-id="cb6c6-241">На странице **Требование ресурса** руководитель проекта или менеджер по ресурсам может указать следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="cb6c6-241">On the **Resource Requirement** page, the project manager or resource manager can also define the following information:</span></span>

- <span data-ttu-id="cb6c6-242">Навыки</span><span class="sxs-lookup"><span data-stu-id="cb6c6-242">Skills</span></span>
- <span data-ttu-id="cb6c6-243">Роли</span><span class="sxs-lookup"><span data-stu-id="cb6c6-243">Roles</span></span>
- <span data-ttu-id="cb6c6-244">Предпочтения ресурсов</span><span class="sxs-lookup"><span data-stu-id="cb6c6-244">Resource preferences</span></span>
- <span data-ttu-id="cb6c6-245">Предпочтительное подразделение</span><span class="sxs-lookup"><span data-stu-id="cb6c6-245">Preferred organizational unit</span></span>

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a><span data-ttu-id="cb6c6-246">Обновление резервирования ресурсов после их резервирования для проекта</span><span class="sxs-lookup"><span data-stu-id="cb6c6-246">Update resource bookings after they are booked on a project</span></span>

<span data-ttu-id="cb6c6-247">После добавления универсального или именованного ресурса в проектную группу можно изменить резервирования ресурса.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-247">After you've added a generic or named resource to a project team, you can change the resource's bookings.</span></span>

1. <span data-ttu-id="cb6c6-248">На странице **Проекты** на вкладке **Рабочая группа** выберите участника рабочей группы, затем выберите **Ведение резервирований**.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-248">On the **Projects** page, on the **Team** tab, select a team member, and then select **Maintain Bookings**.</span></span>

    ![Таблица расписаний, открытая для выбранного участника рабочей группы](media/Resource-Management-image40.png)

    <span data-ttu-id="cb6c6-250">Доска расписания появляется и показывает резервирования участника проектной группы.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-250">The Schedule Board appears and shows the project team member's bookings.</span></span> <span data-ttu-id="cb6c6-251">Разверните запись участника рабочей группы для просмотра часов, которые были зарезервированы по этому проекту и другим проектам, которые расходуют производительность участника рабочей группы.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-251">Expand the team member's record to view the hours that have been booked against this project and other projects that are consuming the team member's capacity.</span></span>

2. <span data-ttu-id="cb6c6-252">Выберите и перетащите резервирование, чтобы удлинить или сократить его.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-252">Select and drag the booking to extend or shorten it.</span></span> <span data-ttu-id="cb6c6-253">Открывается диалоговое окно **Создать резервирование ресурса** , позволяющее корректировать резервирование.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-253">A **Create Resource Booking** dialog box appears that lets you adjust the booking.</span></span>

    ![Диалоговое окно "Создать резервирование ресурса"](media/Resource-Management-image41.png)

3. <span data-ttu-id="cb6c6-255">Щелкните правой кнопкой мыши на резервировании.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-255">Right-click the booking.</span></span> <span data-ttu-id="cb6c6-256">После этого можно использовать контекстное меню для выполнения следующих действий:</span><span class="sxs-lookup"><span data-stu-id="cb6c6-256">You can then use the shortcut menu to complete the following actions:</span></span>

    - <span data-ttu-id="cb6c6-257">Изменение состояния резервирования.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-257">Change the booking status.</span></span>
    - <span data-ttu-id="cb6c6-258">Изменение резервирования.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-258">Edit the booking.</span></span>
    - <span data-ttu-id="cb6c6-259">Замена ресурса в проектной группе.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-259">Substitute a resource on the project team.</span></span>

### <a name="change-the-booking-status"></a><span data-ttu-id="cb6c6-260">Изменение состояния резервирования</span><span class="sxs-lookup"><span data-stu-id="cb6c6-260">Change the booking status</span></span>

<span data-ttu-id="cb6c6-261">Можно изменить любой статус резервирования по умолчанию или настраиваемый статус резервирования.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-261">You can change any default or custom booking status.</span></span>

![Команда изменения состояния](media/Resource-Management-image42.png)

<span data-ttu-id="cb6c6-263">Следующие состояния включены в PSA:</span><span class="sxs-lookup"><span data-stu-id="cb6c6-263">The following statuses are included in PSA:</span></span>

- <span data-ttu-id="cb6c6-264">**Отменено** — это состояние отменяет резервирование ресурса и освобождает производительность ресурса.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-264">**Canceled** – This status cancels a resource's booking and frees up the resource's capacity.</span></span>
- <span data-ttu-id="cb6c6-265">**Окончательное резервирование** — это состояние потребляет производительность ресурса.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-265">**Hard Book** – This status consumes a resource's capacity.</span></span> <span data-ttu-id="cb6c6-266">Резервирование обычно имеет это состояние при открытии пункта **Ведение резервирований** из сетки **Все участники рабочей группы** на странице **Проекты**.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-266">A booking typically has this status when you open **Maintain Bookings** from the **All Team Members** grid on the **Projects** page.</span></span>
- <span data-ttu-id="cb6c6-267">**Предварительное резервирование** — это состояние добавляет ресурс в рабочую группу, но не потребляет производительность ресурса.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-267">**Soft Book** – This status adds a resource to a team but doesn't consume the resource's capacity.</span></span> <span data-ttu-id="cb6c6-268">Оно указывает, что ресурс зарезервирован для потенциальной работы, но все еще имеет мощность, если она потребуется для других заданий.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-268">It indicates that the resource has been reserved for potential work but still has capacity if it's needed on other jobs.</span></span> <span data-ttu-id="cb6c6-269">В представлении общей доступности ресурсов предварительные резервирования имеют другое статус, чем жесткие резервирования.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-269">In the view of overall resource availability, soft bookings have a different status than hard bookings.</span></span>
- <span data-ttu-id="cb6c6-270">**Предложено** — это состояние представляет предложение менеджера по ресурсам или руководителя проекта для ресурса.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-270">**Proposed** – This status represents a resource manager's or project manager's proposal for a resource.</span></span> <span data-ttu-id="cb6c6-271">Предложения не используют производительность ресурса, и ресурс не добавляется в проектную рабочую группу.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-271">Proposals don't consume the capacity of a resource, and the resource isn't added to the project team.</span></span> <span data-ttu-id="cb6c6-272">Чтобы жестко зарезервировать ресурс в рабочей группе руководитель проекта должен принять предложение.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-272">To hard-book the resource on the team, the project manager must accept the proposal.</span></span>

### <a name="submit-resource-requests"></a><span data-ttu-id="cb6c6-273">Отправка запросов ресурса</span><span class="sxs-lookup"><span data-stu-id="cb6c6-273">Submit resource requests</span></span>

<span data-ttu-id="cb6c6-274">Запросы ресурса служат для задания спроса (требования ресурса), который должен быть удовлетворен менеджером по ресурсам.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-274">Resource requests are used to carry the demand (resource requirement) that must be fulfilled by a resource manager.</span></span> <span data-ttu-id="cb6c6-275">Для универсального ресурса, который уже имеется в рабочей группе, можно отправить запрос ресурса непосредственно.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-275">For a generic resource that is already on the team, you can submit a resource request directly.</span></span> <span data-ttu-id="cb6c6-276">Запрос ресурса можно выполнить двумя способами.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-276">A resource request can be fulfilled in two ways:</span></span>

- <span data-ttu-id="cb6c6-277">Менеджер по ресурсам непосредственно выполняет запрос.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-277">The resource manager directly fulfills the request.</span></span> <span data-ttu-id="cb6c6-278">В этом случае универсальный ресурс заменяется жестким резервированием, имеющим именованный ресурс.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-278">In this case, the generic resource is replaced by a hard booking that has a named resource.</span></span>
- <span data-ttu-id="cb6c6-279">Менеджер по ресурсам предлагает ресурс руководителю проекта, а руководитель проекта утверждает или отклоняет предложенный ресурс.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-279">The resource manager proposes a resource to the project manager, and the project manager approves or rejects the proposed resource.</span></span>

#### <a name="direct-fulfillment-of-resource-requests"></a><span data-ttu-id="cb6c6-280">Прямое выполнение запросов ресурсов</span><span class="sxs-lookup"><span data-stu-id="cb6c6-280">Direct fulfillment of resource requests</span></span>

<span data-ttu-id="cb6c6-281">Когда создается требование ресурса, руководитель проекта может отправить запрос ресурса для универсального ресурса, выбрав этот ресурс, затем выбрав **Отправить запрос**.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-281">When a resource requirement is generated, a project manager can submit a resource request for a generic resource by selecting the resource and then selecting **Submit Request**.</span></span>

![Кнопка "Отправить запрос"](media/Resource-Management-image45.png)

<span data-ttu-id="cb6c6-283">Комментарии о ресурсе могут быть предоставлены менеджеру по ресурсам, который выполняет запрос.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-283">Comments about the resource can be provided to the resource manager who is fulfilling the request.</span></span> <span data-ttu-id="cb6c6-284">После отправки запроса поле **Состояние** для участника группы команды меняется на **Отправлено**.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-284">After the request is submitted, the **Status** field for the team member is changed to **Submitted**.</span></span>

![Ввод необязательных комментариев](media/Resource-Management-image46.png)

<span data-ttu-id="cb6c6-286">Когда руководитель по ресурсам выполняет запрос, универсальный участник рабочей группы заменяется именованным ресурсом в сетке **Все участники рабочей группы**.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-286">When the resource manager fulfills the request, the generic team member is replaced by the named resource in the **All Team Members** grid.</span></span>

![Родовой участник рабочей группы, замененный именованным ресурсом в сетке "Все участники рабочей группы"](media/Resource-Management-image47.png)

#### <a name="use-a-resource-proposal-for-resource-requests"></a><span data-ttu-id="cb6c6-288">Использование предложения ресурса для запросов ресурса</span><span class="sxs-lookup"><span data-stu-id="cb6c6-288">Use a resource proposal for resource requests</span></span>

<span data-ttu-id="cb6c6-289">Вместо непосредственного резервирования ресурса по запросу ресурса менеджер по ресурсам может предложить ресурс руководителю проекта.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-289">Instead of directly booking a resource on a resource request, a resource manager can propose a resource to the project manager.</span></span> <span data-ttu-id="cb6c6-290">Менеджер по ресурсам может использовать этот вариант, если точное совпадение для требований недоступно.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-290">A resource manager might use this option when an exact match for the requirements isn't available.</span></span> <span data-ttu-id="cb6c6-291">Когда руководитель по ресурсам предлагает ресурс, руководитель проекта видит, что поле **Состояние** универсального участника группы изменилось на **Требует проверки**.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-291">When a resource manager proposes a resource, the project manager sees that the **Status** field for the generic team member is changed to **Needs Review**.</span></span>

![Состояние универсального участника рабочей группы изменилось на "Требует проверки"](media/Resource-Management-image48.png)

<span data-ttu-id="cb6c6-293">Для просмотра предложенного ресурса вместе с визуализацией эффекта резервирования предложения дважды щелкните на участнике рабочей группы, который имеет статус **Требует проверки**.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-293">To view the proposed resource together with a visualization of the effect of the proposal's booking, double-click the team member that has a status of **Needs Review**.</span></span> <span data-ttu-id="cb6c6-294">Затем выберите вкладку **Предложенные ресурсы**.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-294">Then select the **Proposed Resources** tab.</span></span>

![Вкладка "Предложенные ресурсы"](media/Resource-Management-image49.png)

<span data-ttu-id="cb6c6-296">Выберите **Принять все предложения** , чтобы принять все предлагаемые ресурсы, или **Отклонить все предложения** , чтобы отклонить их.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-296">Select **Accept All Proposals** to accept all proposed resources or **Reject All Proposals** to reject them.</span></span> <span data-ttu-id="cb6c6-297">Если вы принимаете предлагаемые ресурсы, они жестко резервируются в проекте как члены рабочей группы и заменяют универсальные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-297">If you accept the proposed resources, they are hard-booked on the project as team members and replace the generic resources.</span></span>

> [!NOTE]
> <span data-ttu-id="cb6c6-298">Необходимо или принять, или отклонить все предлагаемые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-298">You must either accept or reject all proposed resources.</span></span> <span data-ttu-id="cb6c6-299">Нельзя частично принять или отклонить их.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-299">You can't partially accept or reject them.</span></span>

### <a name="substitute-a-resource-on-the-project-team"></a><span data-ttu-id="cb6c6-300">Замена ресурса в проектной группе</span><span class="sxs-lookup"><span data-stu-id="cb6c6-300">Substitute a resource on the project team</span></span>

<span data-ttu-id="cb6c6-301">Иногда, руководитель проекта должен заменить зарезервированного участника рабочей группы по проекту.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-301">Sometimes, a project manager must substitute a booked team member on a project.</span></span>

1. <span data-ttu-id="cb6c6-302">На странице **Проекты** на вкладке **Рабочая группа** выберите ресурс, который требуется заменить, затем выберите **Ведение резервирований**.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-302">On the **Projects** page, on the **Team** tab, select the resource that needs a substitute, and then select **Maintain Bookings**.</span></span>
2. <span data-ttu-id="cb6c6-303">Разверните ресурс для просмотра проектов, которым он назначен.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-303">Expand the resource to view the projects that it's assigned to.</span></span>

    ![Ресурс, развернутый для отображения назначенных проектов](media/Resource-Management-image50.png)

3. <span data-ttu-id="cb6c6-305">Щелкните правой кнопкой мыши проект, затем выберите **Заменить ресурс**.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-305">Right-click the project, and then select **Substitute Resource**.</span></span>
4. <span data-ttu-id="cb6c6-306">Если известен ресурс, которым необходимо заменить текущий ресурс, выберите или введите его имя, затем выберите **Переназначить**.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-306">If you know the resource that you want to substitute for the current resource, select or type the name, and then select **Re-assign**.</span></span>

    ![Указание заменяющего ресурса](media/Resource-Management-image51.png)

    <span data-ttu-id="cb6c6-308">В качестве альтернативы выполните следующие шаги для поиска ресурса:</span><span class="sxs-lookup"><span data-stu-id="cb6c6-308">Alternatively, follow these steps to search for a resource:</span></span>

    1. <span data-ttu-id="cb6c6-309">Выберите **Найти замену**.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-309">Select **Find Substitution**.</span></span>

        ![Поиск заменяющего ресурса](media/Resource-Management-image52.png)

        <span data-ttu-id="cb6c6-311">Помощник по расписанию возвращает список доступных заменителей.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-311">The Schedule Assistant returns a list of available substitutes.</span></span> <span data-ttu-id="cb6c6-312">В помощнике по расписанию можно выполнить дополнительную фильтрацию доступных ресурсов для обнаружения соответствующего заменителя.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-312">In the Schedule Assistant, you can further filter the available resources to find a suitable substitute.</span></span>

        ![Список доступных замен](media/Resource-Management-image53.png)

    2. <span data-ttu-id="cb6c6-314">Чтобы заменить ресурс, выберите требуемый ресурс, затем выберите **Заменить**.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-314">To substitute the resource, select the resource that you want, and then select **Substitute**.</span></span>

        ![Выбран заменяющий ресурс](media/Resource-Management-image54.png)

    <span data-ttu-id="cb6c6-316">Резервирования и назначения заменяются новым ресурсом.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-316">The bookings and assignments are substituted with the new resource.</span></span>

    ![Резервирования и назначения, замененные новым ресурсом](media/Resource-Management-image55.png)

## <a name="reconcile-team-member-bookings-and-assignments"></a><span data-ttu-id="cb6c6-318">Сверка резервирований и назначений участников рабочей группы</span><span class="sxs-lookup"><span data-stu-id="cb6c6-318">Reconcile team member bookings and assignments</span></span>

<span data-ttu-id="cb6c6-319">Для участников рабочей группы резервирования и назначения свободно связаны между собой.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-319">For team members, bookings and assignments are loosely coupled.</span></span> <span data-ttu-id="cb6c6-320">Другими словами, ресурсы могут иметь назначения без резервирований, или могут иметь резервирования без назначений.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-320">In other words, resources can have assignments but no bookings, or they can have bookings but no assignments.</span></span> <span data-ttu-id="cb6c6-321">В идеальном случае, назначения и резервирования должны соответствовать друг другу, чтобы ресурсы имели выделенные мощности для выполнения назначенных задач.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-321">Ideally, bookings and assignments should be aligned, so that resources have committed capacity to perform the task assignments.</span></span> <span data-ttu-id="cb6c6-322">Тем не менее резервирования могут быть основаны на доступности, а значения времени выполнения задач могут измениться по мере развития проекта.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-322">However, the bookings might be based on availability, and task timings might change as the project continues.</span></span> <span data-ttu-id="cb6c6-323">Следовательно, мягкие связи резервирований и назначений предоставляют гибкость.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-323">Therefore, the loose coupling of bookings and assignments provides flexibility.</span></span>

<span data-ttu-id="cb6c6-324">В PSA имеется вкладка **Сверка** , которая позволяет руководителям проекта сверить резервирования участников рабочей группы и их назначения для проектных групп.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-324">PSA has a **Reconciliation** tab that lets project managers reconcile team members' bookings and their assignments for project teams.</span></span>

![Вкладка сверки](media/Resource-Management-image56.png)

<span data-ttu-id="cb6c6-326">Вкладка **Сверка** отображает резервирования и назначения вплоть до уровня индивидуального назначения задачи для каждого участника рабочей группы.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-326">The **Reconciliation** tab shows bookings and assignments down to the level of the individual task assignment for each team member.</span></span> <span data-ttu-id="cb6c6-327">Она показывает часы в ячейках, отражающих периоды времени от месяцев и вниз до дней.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-327">It shows hours in cells that represent time periods from months down to days.</span></span>

<span data-ttu-id="cb6c6-328">Вкладка также отображает общий нетто итог для проекта, вместе со столбцом итогов.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-328">The tab also shows an overall net total for the project, together with a total column.</span></span>

<span data-ttu-id="cb6c6-329">Для каждого из ресурсов вкладка вычислит различие между резервированиями участника рабочей группы и сверткой назначений задач участников рабочей группы.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-329">For each resource, the tab calculates the difference between the team member's bookings and a rollup of the team member's task assignments.</span></span> <span data-ttu-id="cb6c6-330">В идеальном случае это различие должно быть равно 0 (нулю).</span><span class="sxs-lookup"><span data-stu-id="cb6c6-330">Ideally, this difference should be 0 (zero).</span></span> <span data-ttu-id="cb6c6-331">Другими словами, не должно быть разницы между резервированиями и назначениями.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-331">In other words, there should be no difference between bookings and assignments.</span></span> <span data-ttu-id="cb6c6-332">Различия окрашены и затенены, чтобы нарисовать два условия:</span><span class="sxs-lookup"><span data-stu-id="cb6c6-332">Differences are colored and shaded to draw attention to two conditions:</span></span>

- <span data-ttu-id="cb6c6-333">**Недорезервирование** — недостаток резервирования возникает, когда ресурс имеет больше назначений, чем резервирований.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-333">**Booking shortage** – A booking shortage occurs when a resource has more assignments than bookings.</span></span> <span data-ttu-id="cb6c6-334">Поскольку вся его производительность не была зарезервирована, руководитель проекта может захотеть исправить это состояние, расширив резервирования, чтобы дефицит охватывать.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-334">Because this capacity hasn't been reserved, a project manager might want to correct this condition by extending the resource's bookings to cover the deficit.</span></span>
- <span data-ttu-id="cb6c6-335">**Перерезервирование** — избыточные резервирования происходящих, когда ресурс зарезервирован на проект, но ему не назначены задачи.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-335">**Excess bookings** – Excess bookings occur when a resource has been booked to the project but hasn't been assigned to tasks.</span></span> <span data-ttu-id="cb6c6-336">Это условие может быть допустимо в случаях, когда ресурс был зарезервирован для проекта до того, как было выполнено назначение задачи.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-336">This condition might be acceptable in the cases where the resource was booked to the project before task assignment occurred.</span></span> <span data-ttu-id="cb6c6-337">Тем не менее, в других случаях ресурс не запланирован для назначения задачам.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-337">However, in other cases, the resource isn't planned to be assigned to tasks.</span></span> <span data-ttu-id="cb6c6-338">В таких случаях руководитель проекта должен рассмотреть отмену резервирования ресурса, чтобы его производительность могла быть использована для другого проекта.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-338">In these cases, the project manager should consider canceling the resource's bookings, so that the capacity can be used for another project.</span></span>

<span data-ttu-id="cb6c6-339">В некоторых случаях, когда вы просматриваете время на более высоком уровне, чем уровень дня (например, уровень месяца), вы можете видеть нулевое чистое различие для ресурса (иначе говоря, резервирования = назначения).</span><span class="sxs-lookup"><span data-stu-id="cb6c6-339">In some cases, when you view time at a higher level than the day level (for example, the month level), you might see a net difference of zero for a resource (in other words, bookings = assignments).</span></span> <span data-ttu-id="cb6c6-340">Однако при просмотре времени на уровне недели вы можете увидеть ноль часов назначения и 40 часов резервирования для первой недели, но 40 часов назначений и ноль часов резервирования для второй недели.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-340">However, if you view time at the week level, you might see that there are assignments of zero hours and bookings of 40 hours in the first week, but assignments of 40 hours and bookings of zero hours in the second week.</span></span> <span data-ttu-id="cb6c6-341">В целом резервирования и назначения выверены, однако они отличаются от одной недели до следующей.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-341">Overall, the bookings and assignments are reconciled, but they differ from one week to the next.</span></span>

<span data-ttu-id="cb6c6-342">При просмотре времени на высоких уровнях ячейки на вкладке **Сверка** имеют индикатор, чтобы информировать о различиях на более низких уровнях.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-342">When you view time at higher levels, cells in the **Reconciliation** tab have an indicator to inform you that there are differences at lower levels.</span></span> <span data-ttu-id="cb6c6-343">Дважды щелкнув в ячейке, можно увеличить ее для просмотра различия.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-343">By double-clicking in a cell, you can zoom in to view the difference.</span></span> <span data-ttu-id="cb6c6-344">Можно затем щелкнуть правой кнопкой мыши, чтобы уменьшить ее. Выбрав ресурс, затем используя элемент управления **Следующая разница** на панели инструментов сетки, можно перейти к следующему различию между резервированиями и назначениями для данного ресурса.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-344">You can then right-click to zoom out. By selecting a resource and then using the **Next difference** control on the grid toolbar, you can go to the next difference between bookings and assignments for that resource.</span></span> <span data-ttu-id="cb6c6-345">Затем можно использовать элемент управления **Предыдущая разница** для перехода назад.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-345">You can then use the **Previous difference** control to go back.</span></span> <span data-ttu-id="cb6c6-346">Можно также отключить индикатор различия и поведение перехода в разделе **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-346">You can also turn off the difference indicator and navigation behavior under **Settings**.</span></span>

![Индикатор различия](media/Resource-Management-image57.png)

<span data-ttu-id="cb6c6-348">Если имеются назначения для ресурса, но нет резервирований, на странице **Проекты** на вкладке **Сверка** выберите недостаток резервирований, затем выберите **Продлить резервирование**.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-348">If you have task assignments for a resource but no bookings, on the **Projects** page, on the **Reconciliation** tab, select the booking shortage, and then select **Extend Booking**.</span></span> <span data-ttu-id="cb6c6-349">Открывается диалоговое окно **Продлить резервирование** , в котором отображается резервирование, необходимое для исправления недостатка ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-349">The **Extend Booking** dialog box appears and shows the booking that is needed to address the resource's shortage.</span></span> <span data-ttu-id="cb6c6-350">Оно также показывает существующие резервирования ресурса по всем проекты или другим планируемым объектам.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-350">It also shows the resource's existing bookings across all projects or other schedulable entities.</span></span> <span data-ttu-id="cb6c6-351">Если вы выбираете **ОК** для создания резервирования для этого ресурса, независимо от доступности ресурса, это может привести к избыточному резервированию.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-351">If you select **OK** to create the booking for the resource, regardless of that resource's availability, you might cause overbooking.</span></span>

![Диалоговое окно продления резервирования](media/Resource-Management-image58.png)

<span data-ttu-id="cb6c6-353">Руководитель проекта и руководитель по ресурсам затем могут использовать доску расписания для управления всеми ситуациями, где ресурс излишне зарезервирован с превышением его производительности.</span><span class="sxs-lookup"><span data-stu-id="cb6c6-353">The project manager or resource manager can then use the Schedule Board to manage any situations where a resource is overbooked beyond its capacity.</span></span>
