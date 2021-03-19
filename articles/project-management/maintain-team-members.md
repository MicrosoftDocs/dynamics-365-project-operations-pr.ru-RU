---
title: Ведение участников рабочей группы
description: В этом разделе приводятся сведения о резервировании именованных ресурсов для проектной рабочей группы и их назначении задачам.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 60b6788d881518502d314e9ee5daf6bbc0ae8764
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286849"
---
# <a name="maintain-team-members"></a><span data-ttu-id="149a8-103">Ведение участников рабочей группы</span><span class="sxs-lookup"><span data-stu-id="149a8-103">Maintain team members</span></span>

<span data-ttu-id="149a8-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="149a8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="149a8-105">Можно добавить именованный ресурс в проектную группу, зарезервировав их непосредственно в рабочую группу.</span><span class="sxs-lookup"><span data-stu-id="149a8-105">You can add a named resource to your project team by booking them directly to the team.</span></span>

1. <span data-ttu-id="149a8-106">В Dynamics 365 Project Operations перейдите к пункту **Проекты** и выберите проект, для которого выполняется резервирование.</span><span class="sxs-lookup"><span data-stu-id="149a8-106">In Dynamics 365 Project Operations, go to **Projects**, and select the open the project that you're booking for.</span></span>
2. <span data-ttu-id="149a8-107">На странице **Проект** на вкладке **Рабочая группа** выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="149a8-107">On the **Project** page, on the **Team** tab, select **New**.</span></span> 
3. <span data-ttu-id="149a8-108">В диалоговом окне **Быстрое создание: участник проектной группы** выберите резервируемый ресурс.</span><span class="sxs-lookup"><span data-stu-id="149a8-108">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="149a8-109">Поле **Роль** будет заполнено ролью по умолчанию ресурса, если его она назначена.</span><span class="sxs-lookup"><span data-stu-id="149a8-109">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="149a8-110">Роль можно изменить.</span><span class="sxs-lookup"><span data-stu-id="149a8-110">You can change the role.</span></span> 
4. <span data-ttu-id="149a8-111">Выберите даты начала и окончания, когда требуется этот ресурс, и выберите способ распределения производительности ресурса.</span><span class="sxs-lookup"><span data-stu-id="149a8-111">Select the from and to dates that the resource will be needed, and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="149a8-112">В поле **Утверждающий проекта** выберите **Да**, если требуется, чтобы участник рабочей группы был утверждающим проекта.</span><span class="sxs-lookup"><span data-stu-id="149a8-112">In the **Project Approver** field, select **Yes** if you want the team member to be a project approver.</span></span> <span data-ttu-id="149a8-113">Этот участник рабочей группы может утверждать представленные записи времени и расходов для этого проекта.</span><span class="sxs-lookup"><span data-stu-id="149a8-113">The team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="149a8-114">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="149a8-114">Select **Save**.</span></span>

<span data-ttu-id="149a8-115">Теперь можно назначать резервируемый ресурс задачам по проекту.</span><span class="sxs-lookup"><span data-stu-id="149a8-115">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="149a8-116">На странице **Проект** на вкладке **Расписание** назначьте задачи новому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="149a8-116">On the **Project** page, on the **Schedule** tab, assign tasks to the new resource.</span></span> <span data-ttu-id="149a8-117">Подборщик ресурсов, который запущен из поля **Ресурсы** в сетке задач, отображает участников рабочей группы, которых можно выбрать.</span><span class="sxs-lookup"><span data-stu-id="149a8-117">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>


<span data-ttu-id="149a8-118">В Project Operations резервирование ресурсов и назначение задач не связаны тесно.</span><span class="sxs-lookup"><span data-stu-id="149a8-118">In Project Operations, resource bookings and task assignments aren't tightly coupled.</span></span> <span data-ttu-id="149a8-119">При использовании средства выбора ресурсов в расписании можно назначить задачи участникам рабочей группы на большее количество часов, чем покрывается их резервированием по проекту.</span><span class="sxs-lookup"><span data-stu-id="149a8-119">When you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>

<span data-ttu-id="149a8-120">Различия между резервированиями и назначениями участников рабочей группы показаны на вкладках **Рабочая группа** и **Согласование ресурсов**.</span><span class="sxs-lookup"><span data-stu-id="149a8-120">The differences between team member bookings and assignments are shown on the **Team** and **Resource Reconciliation** tabs.</span></span> <span data-ttu-id="149a8-121">Вы также можете согласовать различия между резервированиями и назначениями ресурсов на более подробном уровне.</span><span class="sxs-lookup"><span data-stu-id="149a8-121">You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

<span data-ttu-id="149a8-122">Используйте средство выбора ресурсов на вкладке **Расписание** для поиска и выбора резервируемых ресурсов, которые еще не входят в проектную группу.</span><span class="sxs-lookup"><span data-stu-id="149a8-122">Use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="149a8-123">Эти ресурсы отображаются в средстве выбора ресурсов как **Другие ресурсы**.</span><span class="sxs-lookup"><span data-stu-id="149a8-123">These resources are shown in the resource picker as **Other Resources**.</span></span>

<span data-ttu-id="149a8-124">При выполнении выбора ресурс добавляется в проектную группу и назначается задаче, но резервирования не создаются.</span><span class="sxs-lookup"><span data-stu-id="149a8-124">When you make a selection, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

<span data-ttu-id="149a8-125">Можно использовать расширенные возможности резервирования на вкладке **Выверка ресурсов** или **Доску расписания** для резервирования производительности ресурса для проекта.</span><span class="sxs-lookup"><span data-stu-id="149a8-125">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

<span data-ttu-id="149a8-126">После того как участник рабочей группы зарезервирован для вашего проекта, можно использовать **Ведение резервирования** или **Доску расписания** непосредственно, чтобы управлять его резервированиями.</span><span class="sxs-lookup"><span data-stu-id="149a8-126">After a team member is booked on your project, you can use **Maintain bookings** or the **Schedule Board** directly to manage their bookings.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]