---
title: Резервирования ресурсов и их связь с назначениями задач
description: В этом разделе представлена информация о том, как управлять именованными ресурсам, резервированиями ресурсов и назначениями задач, а также сведения о том, как они связаны друг с другом.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 700eb78a-31ff-4e3b-8c38-3944c74f3413
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 74369753fba4b5d29e5b49f5b6a6593f902d1133
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754898"
---
# <a name="resource-bookings-and-how-they-relate-to-task-assignments"></a><span data-ttu-id="b6f42-103">Резервирования ресурсов и их связь с назначениями задач</span><span class="sxs-lookup"><span data-stu-id="b6f42-103">Resource bookings and how they relate to task assignments</span></span>


<span data-ttu-id="b6f42-104">Существует два способа, которыми именованные ресурсы можно резервировать в проектную рабочую группу и назначить им задачи проекта:</span><span class="sxs-lookup"><span data-stu-id="b6f42-104">There are two ways that named resources can be booked to a project team and assigned project tasks:</span></span>

- <span data-ttu-id="b6f42-105">Ресурс можно непосредственно зарезервировать для проекта, затем назначить ему задачи проекта.</span><span class="sxs-lookup"><span data-stu-id="b6f42-105">The resource can be directly booked onto a project, and then assigned to project tasks.</span></span>
- <span data-ttu-id="b6f42-106">Задачи можно назначить универсальному ресурсу, который затем используется для нахождения и замены универсального ресурса именованным ресурсом.</span><span class="sxs-lookup"><span data-stu-id="b6f42-106">The tasks can be assigned to a generic resource, which is then used to find and replace the generic with a named resource.</span></span> 

<span data-ttu-id="b6f42-107">В обоих случаях действие резервирования ресурса резервирует производительность ресурса.</span><span class="sxs-lookup"><span data-stu-id="b6f42-107">In both cases, the act of booking the resource reserves the resource’s capacity.</span></span>

<span data-ttu-id="b6f42-108">Руководитель проекта, который планирует проект, является ответственным за план и расписание проекта.</span><span class="sxs-lookup"><span data-stu-id="b6f42-108">The project manager who is planning the project owns the project plan and the schedule.</span></span> <span data-ttu-id="b6f42-109">Используя универсальный ресурс для назначения, затем создания запроса ресурса из него, руководитель проекта может резервировать ресурсы в проект с профилями, указанными в плане проекта.</span><span class="sxs-lookup"><span data-stu-id="b6f42-109">By using the generic resource for the assignment and then generating a resource request from it, the project manager can book resources onto the project with contours specified in the project plan.</span></span> <span data-ttu-id="b6f42-110">Они могут зарезервировать ресурсы в проект, затем назначить их задачам, но нет способа выравнивания профилей резервирования с профилями задач.</span><span class="sxs-lookup"><span data-stu-id="b6f42-110">They can book resources to a project and then assign them to tasks, however there is no way to align the booking contours with the contours of the tasks.</span></span> <span data-ttu-id="b6f42-111">Резервирования не влияют на расписание проекта.</span><span class="sxs-lookup"><span data-stu-id="b6f42-111">Bookings don't affect the project schedule.</span></span>

<span data-ttu-id="b6f42-112">Рассмотрим сложный проект с многочисленными перекрывающимися задачами, где несколько ресурсов одного типа должны работать одновременно.</span><span class="sxs-lookup"><span data-stu-id="b6f42-112">Consider a complex project with multiple overlapping tasks where multiple resources of the same type need to work concurrently.</span></span> <span data-ttu-id="b6f42-113">Если ресурсу предоставлен профиль, который отличается от сводного по его назначениям, сложно изменить задачи, чтобы профиль резервирований соответствовал его отдельным задачам и их оригинальным профилям.</span><span class="sxs-lookup"><span data-stu-id="b6f42-113">If a resource is given a contour that differs from that of the aggregate of their assignments, it’s difficult to modify the tasks to fit the contour of the bookings to their discrete tasks and their original contours.</span></span>

<span data-ttu-id="b6f42-114">В приведенном ниже примере общие усилия, необходимые от одного ресурса по набору из четырех задач, составляют 62 часа за период в две недели, и имеется определенный профиль.</span><span class="sxs-lookup"><span data-stu-id="b6f42-114">In the example below, the total effort required by the same resource from a set of four tasks is 62 hours over a two-week period and there is a specific contour.</span></span> <span data-ttu-id="b6f42-115">Если ресурс Борис зарезервирован на 62 часа на эти же две недели, но с другим профилем, требование и резервирования соответствуют друг другу.</span><span class="sxs-lookup"><span data-stu-id="b6f42-115">If the resource Bob is booked for 62 hours during the same two weeks but with a different contour, the requirement and bookings are in alignment.</span></span>

| <span data-ttu-id="b6f42-116">**Профили задач**</span><span class="sxs-lookup"><span data-stu-id="b6f42-116">**Task contours**</span></span>    | <span data-ttu-id="b6f42-117">**Всего часов**</span><span class="sxs-lookup"><span data-stu-id="b6f42-117">**Total hours**</span></span> | <span data-ttu-id="b6f42-118">Пн 04.06</span><span class="sxs-lookup"><span data-stu-id="b6f42-118">Mo 6/4</span></span> | <span data-ttu-id="b6f42-119">Вт 05.06</span><span class="sxs-lookup"><span data-stu-id="b6f42-119">Tu 6/5</span></span> | <span data-ttu-id="b6f42-120">Ср 06.06</span><span class="sxs-lookup"><span data-stu-id="b6f42-120">We 6/6</span></span> | <span data-ttu-id="b6f42-121">Чт 07.06</span><span class="sxs-lookup"><span data-stu-id="b6f42-121">Th 6/7</span></span> | <span data-ttu-id="b6f42-122">Пт 08.06</span><span class="sxs-lookup"><span data-stu-id="b6f42-122">Fr 6/8</span></span> | <span data-ttu-id="b6f42-123">Сб 09.06</span><span class="sxs-lookup"><span data-stu-id="b6f42-123">Sa 6/9</span></span> | <span data-ttu-id="b6f42-124">Вс 10.06</span><span class="sxs-lookup"><span data-stu-id="b6f42-124">Su 6/10</span></span> | <span data-ttu-id="b6f42-125">Пн 11.06</span><span class="sxs-lookup"><span data-stu-id="b6f42-125">Mo 6/11</span></span> | <span data-ttu-id="b6f42-126">Вт 12.06</span><span class="sxs-lookup"><span data-stu-id="b6f42-126">Tu 6/12</span></span> | <span data-ttu-id="b6f42-127">Ср 13.06</span><span class="sxs-lookup"><span data-stu-id="b6f42-127">We 6/13</span></span> | <span data-ttu-id="b6f42-128">Чт 14.06</span><span class="sxs-lookup"><span data-stu-id="b6f42-128">Th 6/14</span></span> | <span data-ttu-id="b6f42-129">Пт 15.06</span><span class="sxs-lookup"><span data-stu-id="b6f42-129">Fr 6/15</span></span> |
|----------------------|-----------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|---------|---------|---------|
| <span data-ttu-id="b6f42-130">Задача 1</span><span class="sxs-lookup"><span data-stu-id="b6f42-130">Task 1</span></span>               | <span data-ttu-id="b6f42-131">24</span><span class="sxs-lookup"><span data-stu-id="b6f42-131">24</span></span>              | <span data-ttu-id="b6f42-132">8</span><span class="sxs-lookup"><span data-stu-id="b6f42-132">8</span></span>      | <span data-ttu-id="b6f42-133">8</span><span class="sxs-lookup"><span data-stu-id="b6f42-133">8</span></span>      | <span data-ttu-id="b6f42-134">4</span><span class="sxs-lookup"><span data-stu-id="b6f42-134">4</span></span>      |        |        |        |         |         |         | <span data-ttu-id="b6f42-135">4</span><span class="sxs-lookup"><span data-stu-id="b6f42-135">4</span></span>       |         |         |
| <span data-ttu-id="b6f42-136">Задача 2</span><span class="sxs-lookup"><span data-stu-id="b6f42-136">Task 2</span></span>               | <span data-ttu-id="b6f42-137">16</span><span class="sxs-lookup"><span data-stu-id="b6f42-137">16</span></span>              |        |        | <span data-ttu-id="b6f42-138">4</span><span class="sxs-lookup"><span data-stu-id="b6f42-138">4</span></span>      | <span data-ttu-id="b6f42-139">4</span><span class="sxs-lookup"><span data-stu-id="b6f42-139">4</span></span>      |        |        |         | <span data-ttu-id="b6f42-140">8</span><span class="sxs-lookup"><span data-stu-id="b6f42-140">8</span></span>       |         |         |         |         |
| <span data-ttu-id="b6f42-141">Задача 3</span><span class="sxs-lookup"><span data-stu-id="b6f42-141">Task 3</span></span>               | <span data-ttu-id="b6f42-142">10</span><span class="sxs-lookup"><span data-stu-id="b6f42-142">10</span></span>              |        |        |        |        | <span data-ttu-id="b6f42-143">4</span><span class="sxs-lookup"><span data-stu-id="b6f42-143">4</span></span>      |        |         |         | <span data-ttu-id="b6f42-144">4</span><span class="sxs-lookup"><span data-stu-id="b6f42-144">4</span></span>       |         | <span data-ttu-id="b6f42-145">2</span><span class="sxs-lookup"><span data-stu-id="b6f42-145">2</span></span>       |         |
| <span data-ttu-id="b6f42-146">Задача 4</span><span class="sxs-lookup"><span data-stu-id="b6f42-146">Task 4</span></span>               | <span data-ttu-id="b6f42-147">12</span><span class="sxs-lookup"><span data-stu-id="b6f42-147">12</span></span>              |        |        |        |        |        |        |         |         |         | <span data-ttu-id="b6f42-148">4</span><span class="sxs-lookup"><span data-stu-id="b6f42-148">4</span></span>       |         | <span data-ttu-id="b6f42-149">8</span><span class="sxs-lookup"><span data-stu-id="b6f42-149">8</span></span>       |
|                      |                 |        |        |        |        |        |        |         |         |         |         |         |         |
| <span data-ttu-id="b6f42-150">**Итоги**</span><span class="sxs-lookup"><span data-stu-id="b6f42-150">**Totals**</span></span>           | <span data-ttu-id="b6f42-151">62</span><span class="sxs-lookup"><span data-stu-id="b6f42-151">62</span></span>              | <span data-ttu-id="b6f42-152">8</span><span class="sxs-lookup"><span data-stu-id="b6f42-152">8</span></span>      | <span data-ttu-id="b6f42-153">8</span><span class="sxs-lookup"><span data-stu-id="b6f42-153">8</span></span>      | <span data-ttu-id="b6f42-154">8</span><span class="sxs-lookup"><span data-stu-id="b6f42-154">8</span></span>      | <span data-ttu-id="b6f42-155">4</span><span class="sxs-lookup"><span data-stu-id="b6f42-155">4</span></span>      | <span data-ttu-id="b6f42-156">4</span><span class="sxs-lookup"><span data-stu-id="b6f42-156">4</span></span>      |        |         | <span data-ttu-id="b6f42-157">8</span><span class="sxs-lookup"><span data-stu-id="b6f42-157">8</span></span>       | <span data-ttu-id="b6f42-158">4</span><span class="sxs-lookup"><span data-stu-id="b6f42-158">4</span></span>       | <span data-ttu-id="b6f42-159">8</span><span class="sxs-lookup"><span data-stu-id="b6f42-159">8</span></span>       | <span data-ttu-id="b6f42-160">2</span><span class="sxs-lookup"><span data-stu-id="b6f42-160">2</span></span>       | <span data-ttu-id="b6f42-161">8</span><span class="sxs-lookup"><span data-stu-id="b6f42-161">8</span></span>       |
|                      |                 |        |        |        |        |        |        |         |         |         |         |

### <a name="bobs-availability"></a><span data-ttu-id="b6f42-162">Доступность Бориса</span><span class="sxs-lookup"><span data-stu-id="b6f42-162">Bob's availability</span></span>
| <span data-ttu-id="b6f42-163">**Резервирование ресурса**</span><span class="sxs-lookup"><span data-stu-id="b6f42-163">**Resource   booking**</span></span> | <span data-ttu-id="b6f42-164">**Всего часов**</span><span class="sxs-lookup"><span data-stu-id="b6f42-164">**Total hours**</span></span> | <span data-ttu-id="b6f42-165">Пн 04.06</span><span class="sxs-lookup"><span data-stu-id="b6f42-165">Mo 6/4</span></span> | <span data-ttu-id="b6f42-166">Вт 05.06</span><span class="sxs-lookup"><span data-stu-id="b6f42-166">Tu 6/5</span></span> | <span data-ttu-id="b6f42-167">Ср 06.06</span><span class="sxs-lookup"><span data-stu-id="b6f42-167">We 6/6</span></span> | <span data-ttu-id="b6f42-168">Чт 07.06</span><span class="sxs-lookup"><span data-stu-id="b6f42-168">Th 6/7</span></span> | <span data-ttu-id="b6f42-169">Пт 08.06</span><span class="sxs-lookup"><span data-stu-id="b6f42-169">Fr 6/8</span></span> | <span data-ttu-id="b6f42-170">Сб 09.06</span><span class="sxs-lookup"><span data-stu-id="b6f42-170">Sa 6/9</span></span> | <span data-ttu-id="b6f42-171">Вс 10.06</span><span class="sxs-lookup"><span data-stu-id="b6f42-171">Su 6/10</span></span> | <span data-ttu-id="b6f42-172">Пн 11.06</span><span class="sxs-lookup"><span data-stu-id="b6f42-172">Mo 6/11</span></span> | <span data-ttu-id="b6f42-173">Вт 12.06</span><span class="sxs-lookup"><span data-stu-id="b6f42-173">Tu 6/12</span></span> | <span data-ttu-id="b6f42-174">Ср 13.06</span><span class="sxs-lookup"><span data-stu-id="b6f42-174">We 6/13</span></span> | <span data-ttu-id="b6f42-175">Чт 14.06</span><span class="sxs-lookup"><span data-stu-id="b6f42-175">Th 6/14</span></span> | <span data-ttu-id="b6f42-176">Пт 15.06</span><span class="sxs-lookup"><span data-stu-id="b6f42-176">Fr 6/15</span></span> |
|------------------------|-----------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|---------|---------|---------|
| <span data-ttu-id="b6f42-177">Борис</span><span class="sxs-lookup"><span data-stu-id="b6f42-177">Bob</span></span>                    | <span data-ttu-id="b6f42-178">62</span><span class="sxs-lookup"><span data-stu-id="b6f42-178">62</span></span>              | <span data-ttu-id="b6f42-179">4</span><span class="sxs-lookup"><span data-stu-id="b6f42-179">4</span></span>      | <span data-ttu-id="b6f42-180">4</span><span class="sxs-lookup"><span data-stu-id="b6f42-180">4</span></span>      | <span data-ttu-id="b6f42-181">8</span><span class="sxs-lookup"><span data-stu-id="b6f42-181">8</span></span>      | <span data-ttu-id="b6f42-182">8</span><span class="sxs-lookup"><span data-stu-id="b6f42-182">8</span></span>      | <span data-ttu-id="b6f42-183">8</span><span class="sxs-lookup"><span data-stu-id="b6f42-183">8</span></span>      |        |         | <span data-ttu-id="b6f42-184">4</span><span class="sxs-lookup"><span data-stu-id="b6f42-184">4</span></span>       | <span data-ttu-id="b6f42-185">4</span><span class="sxs-lookup"><span data-stu-id="b6f42-185">4</span></span>       | <span data-ttu-id="b6f42-186">8</span><span class="sxs-lookup"><span data-stu-id="b6f42-186">8</span></span>       | <span data-ttu-id="b6f42-187">8</span><span class="sxs-lookup"><span data-stu-id="b6f42-187">8</span></span>       | <span data-ttu-id="b6f42-188">6</span><span class="sxs-lookup"><span data-stu-id="b6f42-188">6</span></span>       |

<span data-ttu-id="b6f42-189">Однако отсутствует систематичный способ назначить профиль зарезервированных часов задачам на повседневной основе.</span><span class="sxs-lookup"><span data-stu-id="b6f42-189">However, there is no systematic way to assign the booked hours contour to tasks on a per-day basis.</span></span> <span data-ttu-id="b6f42-190">Если руководитель проекта хочет изменить расписание проекта в соответствии с доступностью ресурса, то он должен удалить назначение и пересмотреть все задачи для соответствия профилям резервирования.</span><span class="sxs-lookup"><span data-stu-id="b6f42-190">If the project manager is willing to change the project schedule to meet the availability of the resource, then they’ll have to remove the assignment and revise all the tasks to match the booking contours.</span></span>

<span data-ttu-id="b6f42-191">В случае, когда организация отдала задачу планирования проекта как руководителю проекта, так и менеджеру по ресурсам, руководитель проекта устанавливает расписание, которое включает профили необходимых действий.</span><span class="sxs-lookup"><span data-stu-id="b6f42-191">In the case where an organization has given the task of project planning to both a project manager and a resource manager, the project manager sets the schedule, and that includes contouring of the work required.</span></span> <span data-ttu-id="b6f42-192">Менеджер по ресурсам не должен иметь возможности влиять на расписание без ведома руководителя проекта за счет изменения профилей трудозатрат во время резервирования фактических ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b6f42-192">The resource manager shouldn’t be able to affect the schedule without the project manager’s knowledge by changing effort contours while booking real resources.</span></span> <span data-ttu-id="b6f42-193">Если менеджер по ресурсам выполняет что-то, отличное от затребованного руководителем проекта, они должны прийти к соглашению, что изменения необходимы в расписании проекта.</span><span class="sxs-lookup"><span data-stu-id="b6f42-193">If the resource manager is fulfilling something different from what the project manager requested, they need to come to agreement about what changes are needed in the project schedule.</span></span>

<span data-ttu-id="b6f42-194">Поскольку резервирования и назначения не являются тесно связанными, возможно, что профили резервирования отличаются от профилей задач или изменение в назначениях приводят к обстоятельствам, когда резервирования и назначения не согласованы.</span><span class="sxs-lookup"><span data-stu-id="b6f42-194">Since bookings and assignments are not tightly coupled, it’s possible to book contours that are different than the task contours or change the assignments to result in circumstances where bookings and assignments are out of alignment.</span></span>

<span data-ttu-id="b6f42-195">Представление **Выверка** позволяет руководителю проекта просмотреть резервирования и назначения для каждого участника проектной группы.</span><span class="sxs-lookup"><span data-stu-id="b6f42-195">The **Reconciliation View** allows the project manager to see the bookings and assignments for each project team member.</span></span> <span data-ttu-id="b6f42-196">В представлении используются цвета и штриховка, которые показывают, где имеется несоответствие между резервированиями и назначениями участников рабочей группы.</span><span class="sxs-lookup"><span data-stu-id="b6f42-196">The view uses colors and shading to show where there is a mismatch between a team members bookings and assignments.</span></span> <span data-ttu-id="b6f42-197">На основании этих сведений руководитель проекта может принимать корректирующие меры для продления резервирований в случаях, когда имеются назначения, но нет резервирований, или отмены резервирований, когда ресурсы зарезервированы, но у них нет назначений.</span><span class="sxs-lookup"><span data-stu-id="b6f42-197">Based on this information, the project manager can take corrective action to either extend resource bookings for cases where there are assignments and no bookings or cancel bookings where resources are booked but have no assignments.</span></span>

> [!NOTE]
> <span data-ttu-id="b6f42-198">При перемещении задачи, которой вы сами задали профили, эти профили не сохраняются.</span><span class="sxs-lookup"><span data-stu-id="b6f42-198">If you move a task that you have contoured yourself, these contours aren’t maintained.</span></span> <span data-ttu-id="b6f42-199">Профили создаются заново в соответствии с календарем проекта для учета изменений в рабочих часах и праздниках.</span><span class="sxs-lookup"><span data-stu-id="b6f42-199">The contours are regenerated according to the project calendar to account for changes in work hours and holidays.</span></span> <span data-ttu-id="b6f42-200">Это предусмотрено программой, поскольку система не знает цели первоначального профиля и не может определить, имеет ли смысл сохранить этот профиль в новом периоде времени.</span><span class="sxs-lookup"><span data-stu-id="b6f42-200">This is by design because the system doesn’t know the intent of the original contour and can’t determine whether it makes sense to retain that contour in a new time period.</span></span> <span data-ttu-id="b6f42-201">Поскольку резервирования и назначения не связаны, резервирования сохраняют первоначальные профили резервирования.</span><span class="sxs-lookup"><span data-stu-id="b6f42-201">Because bookings and assignments are disconnected, the bookings retain the original booking contours.</span></span> <span data-ttu-id="b6f42-202">В этом случае необходимо отменить и заново зарезервировать для нового профиля назначения.</span><span class="sxs-lookup"><span data-stu-id="b6f42-202">In this case, you’ll need to cancel and rebook to the new assignment contour.</span></span>
