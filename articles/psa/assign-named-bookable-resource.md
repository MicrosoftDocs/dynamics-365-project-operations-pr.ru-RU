---
title: Резервирование резервируемых ресурсов для проектной группы и назначение задач
description: В этом разделе приводятся сведения о том, как резервировать именованные ресурсы для проектной рабочей группы и назначать их задачам.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
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
ms.openlocfilehash: 0300c494a3294b26e2de6bbfa1dd50a76bb72651
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130189"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a><span data-ttu-id="9d1cd-103">Резервирование резервируемых ресурсов для проектной группы и назначение задач</span><span class="sxs-lookup"><span data-stu-id="9d1cd-103">Book named bookable resources to a project team and assign tasks</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="9d1cd-104">Можно добавить именованный ресурс в проектную группу, зарезервировав их непосредственно в рабочую группу.</span><span class="sxs-lookup"><span data-stu-id="9d1cd-104">You can  add a named resource to your project team by booking them directly onto the team.</span></span> <span data-ttu-id="9d1cd-105">Для этого требуется выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="9d1cd-105">To do this, complete the following steps.</span></span>

1. <span data-ttu-id="9d1cd-106">В Project Service Automation перейдите к пункту **Проекты** и выберите проект, для которого выполняется резервирование.</span><span class="sxs-lookup"><span data-stu-id="9d1cd-106">In  Project Service Automation, go to **Projects**, and select the open the project that you are booking for.</span></span>
2. <span data-ttu-id="9d1cd-107">На странице **Проект** на вкладке **Рабочая группа** щелкните **Создать**.</span><span class="sxs-lookup"><span data-stu-id="9d1cd-107">On the **Project** page, on the **Team** tab, click **New**.</span></span> 

![Добавление участника рабочей группы с вкладки рабочей группы](media/RM-how-to-1.png)

3. <span data-ttu-id="9d1cd-109">В диалоговом окне **Быстрое создание: участник проектной группы** выберите резервируемый ресурс.</span><span class="sxs-lookup"><span data-stu-id="9d1cd-109">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="9d1cd-110">Поле **Роль** будет заполнено ролью по умолчанию ресурса, если его она назначена.</span><span class="sxs-lookup"><span data-stu-id="9d1cd-110">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="9d1cd-111">При необходимости вы можете изменить эту роль.</span><span class="sxs-lookup"><span data-stu-id="9d1cd-111">You can change the role if needed.</span></span> 
4. <span data-ttu-id="9d1cd-112">Выберите даты начала и окончания, когда требуется этот ресурс, и выберите способ распределения производительности ресурса.</span><span class="sxs-lookup"><span data-stu-id="9d1cd-112">Select the from and to dates that the resource will be needed and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="9d1cd-113">Если требуется, чтобы участник рабочей группы был утверждающим проекта, выберите **Да** " в поле **Утверждающий проекта**.</span><span class="sxs-lookup"><span data-stu-id="9d1cd-113">If you want the team member to be a project approver, select **Yes** in the **Project Approver** field.</span></span> <span data-ttu-id="9d1cd-114">Это будет означать, что участник рабочей группы может утверждать представленные записи времени и расходов для этого проекта.</span><span class="sxs-lookup"><span data-stu-id="9d1cd-114">This will mean that the team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="9d1cd-115">Щелкните **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="9d1cd-115">Click **Save**.</span></span>

![Добавление участника рабочей группы в форме быстрого создания](media/RM-how-to-2.png)


<span data-ttu-id="9d1cd-117">Теперь можно назначать резервируемый ресурс задачам по проекту.</span><span class="sxs-lookup"><span data-stu-id="9d1cd-117">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="9d1cd-118">На странице **Проект** щелкните на вкладке **Расписание** для назначения задач новому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="9d1cd-118">On the **Project** page, click the **Schedule** tab to assign tasks to the new resource.</span></span> <span data-ttu-id="9d1cd-119">Подборщик ресурсов, который запущен из поля **Ресурсы** в сетке задач, отображает участников рабочей группы, которых можно выбрать.</span><span class="sxs-lookup"><span data-stu-id="9d1cd-119">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>

![Назначение участников рабочей группы задаче на вкладке расписания](media/RM-how-to-3.png)

<span data-ttu-id="9d1cd-121">В версии 3 для Project Service Automation (PSA) резервирования ресурсов и назначения задач не имеют тесной связи.</span><span class="sxs-lookup"><span data-stu-id="9d1cd-121">In version 3 for Project Service Automation (PSA), resource bookings and task assignments are not tightly coupled.</span></span> <span data-ttu-id="9d1cd-122">Это значит, что при использовании средства выбора ресурсов в расписании можно назначить задачи участникам рабочей группы на большее количество часов, чем покрывается их резервированием по проекту.</span><span class="sxs-lookup"><span data-stu-id="9d1cd-122">This means that when you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>
<span data-ttu-id="9d1cd-123">Вы можете посмотреть различия между резервированиями и назначениями участника рабочей группы на вкладке **Рабочая группа** или на вкладке **Выверка ресурсов**. Также можно провести выверку различий между резервированиями и назначениями для ресурсов на более детальном уровне.</span><span class="sxs-lookup"><span data-stu-id="9d1cd-123">You can see the differences between team member bookings and assignments on the **Team** tab or on the **Resource Reconciliation** tab. You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

![Вкладка выверки ресурсов](media/RM-how-to-4.png)

<span data-ttu-id="9d1cd-125">Можно также использовать средство выбора ресурсов на вкладке **Расписание** для поиска и выбора резервируемых ресурсов, которые еще не входят в проектную группу.</span><span class="sxs-lookup"><span data-stu-id="9d1cd-125">You can also use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="9d1cd-126">Они отображаются в средстве выбора ресурсов как **Другие ресурсы**.</span><span class="sxs-lookup"><span data-stu-id="9d1cd-126">These are shown in the resource picker as **Other Resources**.</span></span>

![Назначение задаче ресурса, который не является участником рабочей группы](media/RM-how-to-5.png)

<span data-ttu-id="9d1cd-128">При выполнении этой операции ресурс добавляется в проектную группу и назначается задаче, но резервирования не создаются.</span><span class="sxs-lookup"><span data-stu-id="9d1cd-128">When you do this, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

![Участник рабочей группы с назначениями, но без резервирований](media/RM-how-to-6.png)

<span data-ttu-id="9d1cd-130">Можно использовать расширенные возможности резервирования на вкладке **Выверка ресурсов** или **Доску расписания** для резервирования производительности ресурса для проекта.</span><span class="sxs-lookup"><span data-stu-id="9d1cd-130">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

![Расширенные резервирования для участника рабочей группы на вкладке выверки ресурсов](media/RM-how-to-7.png)

<span data-ttu-id="9d1cd-132">После того как участник рабочей группы зарезервирован для вашего проекта, можно использовать ведение резервирование или доску расписания непосредственно, чтобы управлять его резервированиями.</span><span class="sxs-lookup"><span data-stu-id="9d1cd-132">After a team member is booked on your project, you can use maintain bookings or use the Schedule Board directly to manage their bookings.</span></span>
