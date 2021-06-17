---
title: Просмотр предложенных ресурсов
description: В этом разделе представлена информация о том, как предлагать ресурсы проекта.
author: ruhercul
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 987ea08c77c1824182856c0d52ee0cd15e7029b9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000767"
---
# <a name="review-proposed-resources"></a><span data-ttu-id="2a447-103">Просмотр предложенных ресурсов</span><span class="sxs-lookup"><span data-stu-id="2a447-103">Review proposed resources</span></span>

<span data-ttu-id="2a447-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="2a447-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2a447-105">Менеджеры по ресурсам могут предложить ресурс руководителю проекта с помощью запроса ресурса.</span><span class="sxs-lookup"><span data-stu-id="2a447-105">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="2a447-106">В сетке запросов либо в самом запросе выберите **Найти ресурсы**.</span><span class="sxs-lookup"><span data-stu-id="2a447-106">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="2a447-107">На странице **Помощник по расписанию** выберите ресурс, затем в области **Создать резервирование ресурса** в поле **Состояние резервирования** выберите **Резервировать**.</span><span class="sxs-lookup"><span data-stu-id="2a447-107">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

<span data-ttu-id="2a447-108">Следующие обновления статуса происходят:</span><span class="sxs-lookup"><span data-stu-id="2a447-108">The following status updates occur:</span></span>

- <span data-ttu-id="2a447-109">На странице **Помощник по расписанию**, индикаторы состояния обновляются для указания, что резервирование предложено, это не жесткое резервирование.</span><span class="sxs-lookup"><span data-stu-id="2a447-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>
- <span data-ttu-id="2a447-110">В запросе ресурса состояние меняется на **Требует проверки**.</span><span class="sxs-lookup"><span data-stu-id="2a447-110">On the resource request, the status is changed to **Needs Review**.</span></span>
- <span data-ttu-id="2a447-111">На вкладке **Рабочая группа** проекта значение в столбце **Состояние запроса** универсального участника группы изменяется на **Требует проверки**.</span><span class="sxs-lookup"><span data-stu-id="2a447-111">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

<span data-ttu-id="2a447-112">Руководитель проекта может принять или отклонить предложение.</span><span class="sxs-lookup"><span data-stu-id="2a447-112">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="2a447-113">Когда менеджеры по ресурсам обрабатывают запросы ресурсов, они могут использовать любой из приведенных ниже способов:</span><span class="sxs-lookup"><span data-stu-id="2a447-113">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="2a447-114">Предложить несколько ресурсов, чтобы удовлетворять требование, если один подходящий ресурс недоступен, чтобы заполнить необходимые часы.</span><span class="sxs-lookup"><span data-stu-id="2a447-114">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="2a447-115">Предложенные часы затем разделяются между несколькими ресурсами, которые могут удовлетворить необходимые часы.</span><span class="sxs-lookup"><span data-stu-id="2a447-115">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="2a447-116">В этом сценарии часы не могут перекрываться.</span><span class="sxs-lookup"><span data-stu-id="2a447-116">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="2a447-117">Предложить меньше ресурсов, чем требуется.</span><span class="sxs-lookup"><span data-stu-id="2a447-117">Propose fewer resources than are required.</span></span> <span data-ttu-id="2a447-118">В этом сценарии предложенная производительность ресурса меньше требуемых часов, указанных автором запроса.</span><span class="sxs-lookup"><span data-stu-id="2a447-118">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="2a447-119">Следовательно, когда запрашивающая сторона принимает предлагаемые ресурсы, создается невыполненный запрос ресурсов, чтобы покрыть оставшееся требование.</span><span class="sxs-lookup"><span data-stu-id="2a447-119">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="2a447-120">Зарезервировать несколько ресурсов, чтобы удовлетворять требование, если никакой один ресурс недоступен, чтобы выполнить работу.</span><span class="sxs-lookup"><span data-stu-id="2a447-120">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="2a447-121">Зарезервировать меньше ресурсов, чем требуется.</span><span class="sxs-lookup"><span data-stu-id="2a447-121">Book fewer resources than are required.</span></span> <span data-ttu-id="2a447-122">В этом сценарии зарезервированные часы меньше, чем требуемые часы.</span><span class="sxs-lookup"><span data-stu-id="2a447-122">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="2a447-123">Система подсказывает вам, что следует предложить ресурсы вместо резервирования, чтобы запрашивающая сторона могла проверить и отслеживать оставшееся требование.</span><span class="sxs-lookup"><span data-stu-id="2a447-123">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="2a447-124">Доступность ресурсов</span><span class="sxs-lookup"><span data-stu-id="2a447-124">Resource availability</span></span>

<span data-ttu-id="2a447-125">Важно, чтобы менеджеры по ресурсам могли просматривать доступность ресурсов и обновлять резервирования.</span><span class="sxs-lookup"><span data-stu-id="2a447-125">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="2a447-126">В некоторых случаях нет официального требования (запроса ресурса), но руководитель по ресурсам должен реагировать на незапланированное требование, которое поступает по таким каналам, как сообщение электронной почты, звонок или мгновенное сообщение.</span><span class="sxs-lookup"><span data-stu-id="2a447-126">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="2a447-127">Менеджеры по ресурсам используют доску расписания для обновления ресурсов и резервирований.</span><span class="sxs-lookup"><span data-stu-id="2a447-127">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="2a447-128">Рабочие часов ресурса используются в качестве основы для вычисления доступности ресурса.</span><span class="sxs-lookup"><span data-stu-id="2a447-128">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="2a447-129">Резервирования ресурсов потребляют производительность ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2a447-129">Resource bookings consume the capacity of the resources.</span></span>

<span data-ttu-id="2a447-130">Доска расписания использует цвета и затенение для индикации резервирований, доступности и избыточного резервирования, а также состояния резервирований.</span><span class="sxs-lookup"><span data-stu-id="2a447-130">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="2a447-131">Параметр в параметрах доски расписания позволяет показать условные обозначения.</span><span class="sxs-lookup"><span data-stu-id="2a447-131">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="2a447-132">Если стрелка вправо появляется рядом с отдельным резервируемым ресурсом на доске расписания, ресурс можно развернуть для отображения сведений о работе, для которой зарезервирован этот ресурс.</span><span class="sxs-lookup"><span data-stu-id="2a447-132">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

<span data-ttu-id="2a447-133">Поскольку Dynamics 365 Project Operations использует механизм Universal Resource Scheduling, то, если также установлен Dynamics 365 Field Service, можно просматривать сведения резервирований ресурсов для проектов, заказов на работу и любых других сущностей, на которые расширено планирование.</span><span class="sxs-lookup"><span data-stu-id="2a447-133">Because Dynamics 365 Project Operations uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

<span data-ttu-id="2a447-134">Для просмотра подробных сведений об отдельном ресурсе щелкните правой кнопкой мыши для открытия карточки ресурса.</span><span class="sxs-lookup"><span data-stu-id="2a447-134">To view more details about an individual resource, right-click it to open the resource card.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]