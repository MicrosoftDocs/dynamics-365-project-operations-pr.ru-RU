---
title: Создание резервирование по проекту с доски расписания
description: В этом разделе представлена информация о том, как создавать резервирование по проекту с доски расписания.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
ms.topic: article
ms.prod: Dynamics 365 Project Service Automation 2.x and 3.x
ms.technology: ''
ms.assetid: bbc1bbe2-3482-4b84-9e89-f7e0e585ade8
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 7b6c7e07ea6451e0654ccf1ba7be10e7b38e0d09
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755015"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a><span data-ttu-id="3c3c2-103">Создание резервирование по проекту с доски расписания</span><span class="sxs-lookup"><span data-stu-id="3c3c2-103">Create a project booking from the Schedule board</span></span>

<span data-ttu-id="3c3c2-104">Можно зарезервировать ресурс в проект либо напрямую с вкладки **Рабочая группа** проекта или путем создания потребности в ресурсах из назначения универсального участника рабочей группы, а затем выполнить созданное требование с участником проектной группы.</span><span class="sxs-lookup"><span data-stu-id="3c3c2-104">You can book a resource onto a project directly from the **Team** tab of the project or by generating a resource requirement from a generic team member assignment and then fulfilling the generated requirement with a project team member.</span></span>

<span data-ttu-id="3c3c2-105">Также можно зарезервировать ресурс в проект непосредственно из доски расписания.</span><span class="sxs-lookup"><span data-stu-id="3c3c2-105">You can also book a resource onto a project directly from the Schedule board.</span></span> <span data-ttu-id="3c3c2-106">Существует три способа это сделать:</span><span class="sxs-lookup"><span data-stu-id="3c3c2-106">There are three ways to do this:</span></span>

- <span data-ttu-id="3c3c2-107">**Резервирование из созданного требования ресурса:** можно создать требование ресурса после создания универсального ресурса и назначения задач в проекте.</span><span class="sxs-lookup"><span data-stu-id="3c3c2-107">**Book from a generated resource requirement:** You can generate a resource requirement after you create a generic resource and assign tasks within a project.</span></span>

- <span data-ttu-id="3c3c2-108">**Резервирование из основного требования:** основное требование отображаются на доске расписания на вкладке **Проект**.</span><span class="sxs-lookup"><span data-stu-id="3c3c2-108">**Book from the primary requirement:** The primary requirements show up on the Schedule board on the **Project** tab.</span></span> 

- <span data-ttu-id="3c3c2-109">**Резервирование из нового требования ресурса:** можно создать требование ресурса с нуля и связать его с проектом.</span><span class="sxs-lookup"><span data-stu-id="3c3c2-109">**Book from a new resource requirement:** You can create a resource requirement from scratch and associate it with a project.</span></span> <span data-ttu-id="3c3c2-110">На доске расписания эта потребность в ресурсах отображает на вкладке **Открытые требования**.</span><span class="sxs-lookup"><span data-stu-id="3c3c2-110">On the Schedule board, the resource requirement shows up on the **Open Requirements** tab.</span></span>

## <a name="book-from-a-generated-resource-requirement"></a><span data-ttu-id="3c3c2-111">Резервирование из созданного требования ресурса</span><span class="sxs-lookup"><span data-stu-id="3c3c2-111">Book from a generated resource requirement</span></span>

<span data-ttu-id="3c3c2-112">Можно создать родовой ресурс и назначить ему одну или несколько задач в рамках проекта.</span><span class="sxs-lookup"><span data-stu-id="3c3c2-112">You can create a generic resource and assign it one or more tasks within a project.</span></span> <span data-ttu-id="3c3c2-113">Затем можно сформировать требование ресурса из универсального участника рабочей группы.</span><span class="sxs-lookup"><span data-stu-id="3c3c2-113">Then you can generate a resource requirement from the generic team member.</span></span> 

1.  <span data-ttu-id="3c3c2-114">На доске расписания этот ресурс будет показан на вкладке **Открытые требования**. Можно использовать фильтры столбцов в таблице, если имеется много открытых требований.</span><span class="sxs-lookup"><span data-stu-id="3c3c2-114">On the Schedule board, this resource will show up on the **Open Requirements** tab. You might need to use column filters on the grid if you have many open requirements.</span></span> 

    <span data-ttu-id="3c3c2-115">![Вкладка "Открытые требования" на таблице расписаний](media/FAQ-Project-Booking-Schedule-Board-1.png "Снимок экрана таблицы резервирований и назначений")</span><span class="sxs-lookup"><span data-stu-id="3c3c2-115">![Open Requirements tab on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-1.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="3c3c2-116">Выберите требование.</span><span class="sxs-lookup"><span data-stu-id="3c3c2-116">Select the requirement.</span></span> <span data-ttu-id="3c3c2-117">Открывается вкладка **Найти доступность** поверх выбранной строки.</span><span class="sxs-lookup"><span data-stu-id="3c3c2-117">The **Find Availability** tab will appear at the top of the selected row.</span></span>
 
3. <span data-ttu-id="3c3c2-118">При выборе этой вкладки открывается режим помощника по расписанию доски расписания и затем фильтруются доступные ресурсы, удовлетворяющие требованию ресурса.</span><span class="sxs-lookup"><span data-stu-id="3c3c2-118">When you select the tab, the Schedule Assistant mode of the Schedule board opens and then filters the available resources that meet the resource requirement.</span></span> <span data-ttu-id="3c3c2-119">После этого можно зарезервировать ресурс.</span><span class="sxs-lookup"><span data-stu-id="3c3c2-119">After that, you can book a resource.</span></span>

4. <span data-ttu-id="3c3c2-120">Можно также перетащить выбранную строку снизу доски расписания в ячейку ресурса в сетке выше.</span><span class="sxs-lookup"><span data-stu-id="3c3c2-120">You can also drag and drop the selected row from the bottom of the Schedule board to a resource cell in the grid above.</span></span> <span data-ttu-id="3c3c2-121">После перетаскивания открывается панель **Создать резервирование ресурса** справа.</span><span class="sxs-lookup"><span data-stu-id="3c3c2-121">When you drop it, it opens the **Create Resource Booking** panel on the right.</span></span>

    <span data-ttu-id="3c3c2-122">При выборе **Резервировать** резервируется ресурс в проектную рабочую группу.</span><span class="sxs-lookup"><span data-stu-id="3c3c2-122">Selecting **Book** books the resource onto the project team.</span></span>

![Панель создания резервирования ресурса](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a><span data-ttu-id="3c3c2-124">Резервирование из основного требования</span><span class="sxs-lookup"><span data-stu-id="3c3c2-124">Book from the Primary Requirement</span></span>

<span data-ttu-id="3c3c2-125">При создание проекта в Project Service автоматически создается требование ресурса, которое называется основным требованием.</span><span class="sxs-lookup"><span data-stu-id="3c3c2-125">Creating a project in Project Service automatically creates a resource requirement called the Primary Requirement.</span></span> <span data-ttu-id="3c3c2-126">Это пустое требование, используемое для быстрого резервирования ресурса с доской расписания без создания требования или создания требования с нуля.</span><span class="sxs-lookup"><span data-stu-id="3c3c2-126">This is an empty requirement that is used to quickly book a resource with the Schedule board without generating a requirement or creating one from scratch.</span></span> <span data-ttu-id="3c3c2-127">Поскольку требование пусто, потребуется задать даты, а также способ распределения и часы, если это применимо.</span><span class="sxs-lookup"><span data-stu-id="3c3c2-127">Because the requirement is empty, you’ll need to specify dates as well as the allocation method and hours, if applicable.</span></span> 

1. <span data-ttu-id="3c3c2-128">Чтобы зарезервировать ресурс с помощью основного требования, на доске расписания выберите вкладку **Проект**. Может потребоваться использовать фильтр столбца **Проект**, если имеется много проектов.</span><span class="sxs-lookup"><span data-stu-id="3c3c2-128">To book a resource with the Primary Requirement, on the Schedule board, select the **Project** tab. You might need to use the column filter on the **Project** column if you have many projects.</span></span>

   <span data-ttu-id="3c3c2-129">![Фильтры столбцов на таблице расписаний](media/FAQ-Project-Booking-Schedule-Board-2.png "Снимок экрана таблицы резервирований и назначений")</span><span class="sxs-lookup"><span data-stu-id="3c3c2-129">![Column filters on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-2.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="3c3c2-130">Выберите требование, которое имеет только имя проекта в качестве имени и содержит нулевую (0) длительность.</span><span class="sxs-lookup"><span data-stu-id="3c3c2-130">Select the requirement that only has the project name as its name and has a duration of zero (0).</span></span>

3. <span data-ttu-id="3c3c2-131">Выберите вкладку **Найти доступность**, которая отображается для строки.</span><span class="sxs-lookup"><span data-stu-id="3c3c2-131">Select the **Find Availability** tab that appears on the row.</span></span> <span data-ttu-id="3c3c2-132">При этом доска расписания переходит в режим помощника по расписанию, и отображаются доступные ресурсы, которые можно зарезервировать в проект.</span><span class="sxs-lookup"><span data-stu-id="3c3c2-132">This puts the Schedule board in Schedule Assistant mode and shows the available resources that can be booked onto the project.</span></span>

4. <span data-ttu-id="3c3c2-133">Так как **Основное требование** пустое с нулевой (0) длительностью, потребуется установить продолжительность на панели **Создать резервирование ресурса** при выборе и резервировании ресурса.</span><span class="sxs-lookup"><span data-stu-id="3c3c2-133">Because a **Primary Requirement** is an empty requirement with zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when selecting and booking a resource.</span></span>

5. <span data-ttu-id="3c3c2-134">Можно также выбрать **Основное требование проекта** внизу доски расписания и перетащить его на ресурс, чтобы зарезервировать его.</span><span class="sxs-lookup"><span data-stu-id="3c3c2-134">You can also select the **Project Primary Requirement** at the bottom of the Schedule board and drag and drop it on a resource to book it.</span></span>
 
    <span data-ttu-id="3c3c2-135">Так как **Основное требование** пустое и имеет нулевую (0) длительность, потребуется установить продолжительность на панели **Создать резервирование ресурса** при выборе и резервировании ресурса.</span><span class="sxs-lookup"><span data-stu-id="3c3c2-135">Because the **Primary Requirement** is an empty requirement that has zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when you select and book a resource.</span></span>
 
    <span data-ttu-id="3c3c2-136">При резервировании ресурса с помощью **Основного требования** на доске расписания вы добавляете его к проектной группе без каких-либо назначений.</span><span class="sxs-lookup"><span data-stu-id="3c3c2-136">When you book a resource through the **Primary Requirement** on the Schedule board, you add it to the project team without any assignments.</span></span>
 
## <a name="book-from-a-new-resource-requirement"></a><span data-ttu-id="3c3c2-137">Резервирование из нового требования ресурса</span><span class="sxs-lookup"><span data-stu-id="3c3c2-137">Book from a new resource requirement</span></span>
<span data-ttu-id="3c3c2-138">Выполните следующие действия для резервирования из нового требования ресурса.</span><span class="sxs-lookup"><span data-stu-id="3c3c2-138">Complete the following steps to book from a new resource requirement.</span></span> 

1. <span data-ttu-id="3c3c2-139">Перейдите в раздел **Требования ресурсов**, затем выберите **Создать** для создания новой потребности в ресурсах.</span><span class="sxs-lookup"><span data-stu-id="3c3c2-139">Go to **Resource Requirements**, and then select **New** to create a new resource requirement.</span></span>

2. <span data-ttu-id="3c3c2-140">На вкладке **Проект** выберите проект, чтобы связать требование с проектом.</span><span class="sxs-lookup"><span data-stu-id="3c3c2-140">On the **Project** tab, select a project to associate the requirement to the project.</span></span>
 
    <span data-ttu-id="3c3c2-141">На доске расписания это новое требование отображается как **Открытое требование**, которое можно выполнить.</span><span class="sxs-lookup"><span data-stu-id="3c3c2-141">On the Schedule board, this new requirement shows as an **Open Requirement** that you can fulfill.</span></span>

3. <span data-ttu-id="3c3c2-142">Зарезервируйте ресурса, чтобы добавить его в проектную группу.</span><span class="sxs-lookup"><span data-stu-id="3c3c2-142">Book the resource to add it to the project team.</span></span>

4. <span data-ttu-id="3c3c2-143">Теперь, когда ресурс зарезервирован, необходимо назначить задачи вручную.</span><span class="sxs-lookup"><span data-stu-id="3c3c2-143">Now that the resource is booked, you must assign tasks manually.</span></span>

