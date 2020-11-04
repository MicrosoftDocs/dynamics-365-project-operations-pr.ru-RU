---
title: Резервирование для проекта
description: В этом разделе представлена информация о резервировании ресурса для проекта.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 19128264ed3db7efeeba948155f0ddbdc806c2a0
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083040"
---
# <a name="book-to-a-project"></a><span data-ttu-id="33030-103">Резервирование для проекта</span><span class="sxs-lookup"><span data-stu-id="33030-103">Book to a project</span></span>

<span data-ttu-id="33030-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="33030-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="33030-105">Бывают случаи, когда менеджеру проекта или менеджеру ресурсов нужно будет выделить ресурс для проекта без определенных требований, определяемых универсальным участником рабочей группы.</span><span class="sxs-lookup"><span data-stu-id="33030-105">There are times where a Project manager or Resource manager will need to allocate a resource to project without a specific requirement being defined from a generic team member.</span></span> <span data-ttu-id="33030-106">Это можно достигнуть одним из трех способов.</span><span class="sxs-lookup"><span data-stu-id="33030-106">This can be achieved in one of three ways.</span></span>

- <span data-ttu-id="33030-107">Резервирование из сетки участников рабочих групп</span><span class="sxs-lookup"><span data-stu-id="33030-107">Book from the team member grid</span></span>
- <span data-ttu-id="33030-108">Резервирование с доски расписания</span><span class="sxs-lookup"><span data-stu-id="33030-108">Book from the schedule board</span></span>
- <span data-ttu-id="33030-109">Резервирование из формы **Проект**</span><span class="sxs-lookup"><span data-stu-id="33030-109">Book from the **Project** form</span></span>

## <a name="book-from-the-team-member-grid"></a><span data-ttu-id="33030-110">Резервирование из сетки участников рабочих групп</span><span class="sxs-lookup"><span data-stu-id="33030-110">Book from the team member grid</span></span>

<span data-ttu-id="33030-111">Если ваша организация работает в гибридном режиме распределения ресурсов, менеджер проекта может зарезервировать ресурс непосредственно для проекта, выполнив следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="33030-111">If your organization is operating in hybrid Resource allocation mode, the Project manager can book a resource directly to the project by completing the following steps.</span></span>

1. <span data-ttu-id="33030-112">В проекте перейдите к сетке участников рабочей группы и выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="33030-112">From the project, go to the team member grid and select **New**.</span></span>
2. <span data-ttu-id="33030-113">Определите название должности и роль ресурса.</span><span class="sxs-lookup"><span data-stu-id="33030-113">Define the position name and the role of the resource.</span></span>
3. <span data-ttu-id="33030-114">Выберите доступный для резервирования ресурс из доступной подстановки.</span><span class="sxs-lookup"><span data-stu-id="33030-114">Select the bookable resource from the available lookup.</span></span>
4. <span data-ttu-id="33030-115">После выбора ресурса определите следующую информацию в полях для резервирования ресурса:</span><span class="sxs-lookup"><span data-stu-id="33030-115">After you select the resource, define the following field information to book the resource:</span></span>

    - <span data-ttu-id="33030-116">Дата начала</span><span class="sxs-lookup"><span data-stu-id="33030-116">Start date</span></span>
    - <span data-ttu-id="33030-117">Дата окончания</span><span class="sxs-lookup"><span data-stu-id="33030-117">Finish date</span></span>
    - <span data-ttu-id="33030-118">Метод выделения</span><span class="sxs-lookup"><span data-stu-id="33030-118">Allocation method</span></span>
    - <span data-ttu-id="33030-119">Часы, если применимо</span><span class="sxs-lookup"><span data-stu-id="33030-119">Hours, if applicable</span></span>
    - <span data-ttu-id="33030-120">Утверждающий проекта</span><span class="sxs-lookup"><span data-stu-id="33030-120">Project approver</span></span>

6. <span data-ttu-id="33030-121">Выберите **Сохранить и закрыть**</span><span class="sxs-lookup"><span data-stu-id="33030-121">Select **Save and Close**</span></span>

## <a name="book-from-the-schedule-board"></a><span data-ttu-id="33030-122">Резервирование с доски расписания</span><span class="sxs-lookup"><span data-stu-id="33030-122">Book from the schedule board</span></span>

<span data-ttu-id="33030-123">Когда менеджеру ресурсов необходимо зарезервировать ресурс непосредственно для проекта, он может использовать доску расписания и требования проекта.</span><span class="sxs-lookup"><span data-stu-id="33030-123">When a Resource manager needs to book a resource directly to a project, they can use the schedule board and the project requirement.</span></span> <span data-ttu-id="33030-124">Требование проекта — это требование ресурса, которое всегда доступно для резервирования по нему.</span><span class="sxs-lookup"><span data-stu-id="33030-124">The project requirement is a resource requirement that is always available to be booked against.</span></span> <span data-ttu-id="33030-125">Чтобы зарезервировать напрямую для проекта из доски расписания, выполните следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="33030-125">To book directly to a project form the schedule board, complete the following steps.</span></span>

1. <span data-ttu-id="33030-126">Перейдите к доске расписания и на левой странице отфильтруйте ресурсы, которые вы рассматриваете для требования.</span><span class="sxs-lookup"><span data-stu-id="33030-126">Navigate to the schedule board and on the left page, filter for the resources you are considering for the requirement.</span></span>
2. <span data-ttu-id="33030-127">На нижней панели выберите вкладку **Проект** , чтобы просмотреть список требований проекта.</span><span class="sxs-lookup"><span data-stu-id="33030-127">In the bottom pane, select the **Project** tab to view a list of project requirements.</span></span>
3. <span data-ttu-id="33030-128">Перетащите требование на ресурс и укажите следующую информацию:</span><span class="sxs-lookup"><span data-stu-id="33030-128">Drag the requirement onto a resource and define the following information:</span></span>

    - <span data-ttu-id="33030-129">Дата начала</span><span class="sxs-lookup"><span data-stu-id="33030-129">Start date</span></span>
    - <span data-ttu-id="33030-130">Дата окончания</span><span class="sxs-lookup"><span data-stu-id="33030-130">Finish date</span></span>
    - <span data-ttu-id="33030-131">Состояние резервирования</span><span class="sxs-lookup"><span data-stu-id="33030-131">Booking status</span></span>
    - <span data-ttu-id="33030-132">Метод резервирования</span><span class="sxs-lookup"><span data-stu-id="33030-132">Booking method</span></span>
    - <span data-ttu-id="33030-133">Продолжительность</span><span class="sxs-lookup"><span data-stu-id="33030-133">Duration</span></span>

## <a name="book-from-the-project-form"></a><span data-ttu-id="33030-134">Резервирование из формы "Проект"</span><span class="sxs-lookup"><span data-stu-id="33030-134">Book from the Project form</span></span>

<span data-ttu-id="33030-135">Как менеджеру проекта, вам может потребоваться зарезервировать ресурс для проекта, но вы знаете только критерии, а не название ресурса.</span><span class="sxs-lookup"><span data-stu-id="33030-135">As a Project manager, you might need to book a resource to a project, but only know the criteria rather than the name of the resource.</span></span> <span data-ttu-id="33030-136">Выполните следующие шаги, чтобы использовать помощник по расписанию для поиска ресурса на основе любых доступных атрибутов ресурса.</span><span class="sxs-lookup"><span data-stu-id="33030-136">Complete the following steps to use the schedule assistant to find a resource based on any available attributes of the resource.</span></span> 

1. <span data-ttu-id="33030-137">Перейдите к проекту и выберите **Резервировать** , чтобы открыть помощник по расписанию.</span><span class="sxs-lookup"><span data-stu-id="33030-137">Navigate to the project and select **Book** to open the Schedule Assistant.</span></span>
2. <span data-ttu-id="33030-138">Используя фильтры в левой части помощника по расписанию, уточните критерии и выберите **Поиск**.</span><span class="sxs-lookup"><span data-stu-id="33030-138">Using the filters on the left side of the Schedule Assistant, narrow the criteria and select **Search.**</span></span>
3. <span data-ttu-id="33030-139">На основе ресурсов, возвращенных в результатах, вы можете зарезервировать ресурс.</span><span class="sxs-lookup"><span data-stu-id="33030-139">Based on resources returned in the results, you can book a resource.</span></span>

> [!NOTE]
> <span data-ttu-id="33030-140">Этот метод не создает никаких резервирований для ресурса.</span><span class="sxs-lookup"><span data-stu-id="33030-140">This method doesn't create any bookings for the resource.</span></span> <span data-ttu-id="33030-141">Вместо этого он добавляет ресурс в рабочую группу.</span><span class="sxs-lookup"><span data-stu-id="33030-141">Instead, it adds the resource to the team.</span></span> <span data-ttu-id="33030-142">После того как участник рабочей группы был добавлен в проект, менеджер проекта может использовать ведение резервирований или продление резервирований, чтобы добавить необходимые резервирования к ресурсу.</span><span class="sxs-lookup"><span data-stu-id="33030-142">After the team member has been added to the project, the project manager can use maintain bookings or extend bookings to add the required bookings to the resource.</span></span>
