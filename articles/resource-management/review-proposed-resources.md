---
title: Просмотр предложенных ресурсов
description: В этом разделе представлена информация о том, как предлагать ресурсы проекта.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: ad5cbdeb5fe05e6115eb024833a8d58b626ea4c9
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083155"
---
# <a name="review-proposed-resources"></a><span data-ttu-id="8c852-103">Просмотр предложенных ресурсов</span><span class="sxs-lookup"><span data-stu-id="8c852-103">Review proposed resources</span></span>

<span data-ttu-id="8c852-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="8c852-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8c852-105">Менеджеры по ресурсам могут предложить ресурс руководителю проекта с помощью запроса ресурса.</span><span class="sxs-lookup"><span data-stu-id="8c852-105">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="8c852-106">В сетке запросов либо в самом запросе выберите **Найти ресурсы**.</span><span class="sxs-lookup"><span data-stu-id="8c852-106">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="8c852-107">На странице **Помощник по расписанию** выберите ресурс, затем в области **Создать резервирование ресурса** в поле **Состояние резервирования** выберите **Резервировать**.</span><span class="sxs-lookup"><span data-stu-id="8c852-107">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

<span data-ttu-id="8c852-108">Следующие обновления статуса происходят:</span><span class="sxs-lookup"><span data-stu-id="8c852-108">The following status updates occur:</span></span>

- <span data-ttu-id="8c852-109">На странице **Помощник по расписанию** , индикаторы состояния обновляются для указания, что резервирование предложено, это не жесткое резервирование.</span><span class="sxs-lookup"><span data-stu-id="8c852-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>
- <span data-ttu-id="8c852-110">В запросе ресурса состояние меняется на **Требует проверки**.</span><span class="sxs-lookup"><span data-stu-id="8c852-110">On the resource request, the status is changed to **Needs Review**.</span></span>
- <span data-ttu-id="8c852-111">На вкладке **Рабочая группа** проекта значение в столбце **Состояние запроса** универсального участника группы изменяется на **Требует проверки**.</span><span class="sxs-lookup"><span data-stu-id="8c852-111">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

<span data-ttu-id="8c852-112">Руководитель проекта может принять или отклонить предложение.</span><span class="sxs-lookup"><span data-stu-id="8c852-112">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="8c852-113">Когда менеджеры по ресурсам обрабатывают запросы ресурсов, они могут использовать любой из приведенных ниже способов:</span><span class="sxs-lookup"><span data-stu-id="8c852-113">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="8c852-114">Предложить несколько ресурсов, чтобы удовлетворять требование, если один подходящий ресурс недоступен, чтобы заполнить необходимые часы.</span><span class="sxs-lookup"><span data-stu-id="8c852-114">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="8c852-115">Предложенные часы затем разделяются между несколькими ресурсами, которые могут удовлетворить необходимые часы.</span><span class="sxs-lookup"><span data-stu-id="8c852-115">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="8c852-116">В этом сценарии часы не могут перекрываться.</span><span class="sxs-lookup"><span data-stu-id="8c852-116">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="8c852-117">Предложить меньше ресурсов, чем требуется.</span><span class="sxs-lookup"><span data-stu-id="8c852-117">Propose fewer resources than are required.</span></span> <span data-ttu-id="8c852-118">В этом сценарии предложенная производительность ресурса меньше требуемых часов, указанных автором запроса.</span><span class="sxs-lookup"><span data-stu-id="8c852-118">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="8c852-119">Следовательно, когда запрашивающая сторона принимает предлагаемые ресурсы, создается невыполненный запрос ресурсов, чтобы покрыть оставшееся требование.</span><span class="sxs-lookup"><span data-stu-id="8c852-119">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="8c852-120">Зарезервировать несколько ресурсов, чтобы удовлетворять требование, если никакой один ресурс недоступен, чтобы выполнить работу.</span><span class="sxs-lookup"><span data-stu-id="8c852-120">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="8c852-121">Зарезервировать меньше ресурсов, чем требуется.</span><span class="sxs-lookup"><span data-stu-id="8c852-121">Book fewer resources than are required.</span></span> <span data-ttu-id="8c852-122">В этом сценарии зарезервированные часы меньше, чем требуемые часы.</span><span class="sxs-lookup"><span data-stu-id="8c852-122">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="8c852-123">Система подсказывает вам, что следует предложить ресурсы вместо резервирования, чтобы запрашивающая сторона могла проверить и отслеживать оставшееся требование.</span><span class="sxs-lookup"><span data-stu-id="8c852-123">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="billable-utilization"></a><span data-ttu-id="8c852-124">Оплачиваемая загруженность</span><span class="sxs-lookup"><span data-stu-id="8c852-124">Billable utilization</span></span>

<span data-ttu-id="8c852-125">Ресурсы могут иметь целевую оплачиваемую загруженность.</span><span class="sxs-lookup"><span data-stu-id="8c852-125">Resources can have a target billable utilization.</span></span> <span data-ttu-id="8c852-126">Эта целевая загруженность определяется как атрибут роли ресурса по умолчанию или задается в записи отдельного резервируемого ресурса.</span><span class="sxs-lookup"><span data-stu-id="8c852-126">This target utilization is either defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="8c852-127">Расчеты загруженности основаны на фактических часах, о которых сообщают ресурсы с помощью утвержденных записей времени.</span><span class="sxs-lookup"><span data-stu-id="8c852-127">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="8c852-128">Формулы следующие используются для расчета загруженности:</span><span class="sxs-lookup"><span data-stu-id="8c852-128">The following formulas are used to calculate utilization:</span></span>

- <span data-ttu-id="8c852-129">Оплачиваемая загруженность = Оплачиваемые фактические часов ÷ Производительность ресурса</span><span class="sxs-lookup"><span data-stu-id="8c852-129">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
- <span data-ttu-id="8c852-130">Неоплачиваемая загруженность = Фактическое время с ИД типа выставления счетов = Не подлежит оплате, Бесплатно или Недоступно ÷ Производительность ресурса</span><span class="sxs-lookup"><span data-stu-id="8c852-130">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
- <span data-ttu-id="8c852-131">Внутреннее = Фактическое время без контракта на продажу ÷ Производительность ресурса</span><span class="sxs-lookup"><span data-stu-id="8c852-131">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
- <span data-ttu-id="8c852-132">Производительность ресурса = Рабочие часы ресурса – Не на работе – Нерабочие дни</span><span class="sxs-lookup"><span data-stu-id="8c852-132">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="8c852-133">Представление **Загруженность ресурсов** можно найти на панели **Ресурсы**.</span><span class="sxs-lookup"><span data-stu-id="8c852-133">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

<span data-ttu-id="8c852-134">Каждая ячейка в сетке представляет процент оплачиваемой загруженности ресурса в период, такой как день, неделя или месяц.</span><span class="sxs-lookup"><span data-stu-id="8c852-134">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="8c852-135">Следующие формулы используются для задания цветов ячеек:</span><span class="sxs-lookup"><span data-stu-id="8c852-135">The following formulas are used to color the cells:</span></span>

- <span data-ttu-id="8c852-136">**Зеленый** : Оплачиваемая загруженность \>= Целевая загруженность ресурса</span><span class="sxs-lookup"><span data-stu-id="8c852-136">**Green:** Billable utilization \>= Resource target utilization</span></span>
- <span data-ttu-id="8c852-137">**Желтый** : Целевая загруженность – 20 \<= Оплачиваемая загруженность \< Целевая загруженность</span><span class="sxs-lookup"><span data-stu-id="8c852-137">**Yellow:** Target utilization – 20 \<= Billable utilization \< Target utilization</span></span>
- <span data-ttu-id="8c852-138">**Красный:** Оплачиваемая загруженность \< Целевая загруженность – 20</span><span class="sxs-lookup"><span data-stu-id="8c852-138">**Red:** Billable utilization \< Target utilization – 20</span></span>

<span data-ttu-id="8c852-139">Поскольку представление **Загруженность ресурсов** основано на доске расписания, можно использовать возможности фильтрации доски расписания для фильтрации результатов.</span><span class="sxs-lookup"><span data-stu-id="8c852-139">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="8c852-140">Сетка требует, чтобы вы задали целевую загруженность для роли или отдельного ресурса.</span><span class="sxs-lookup"><span data-stu-id="8c852-140">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="8c852-141">Чтобы выполнить эту настройку, выберите **Ресурсы** \> **Роли ресурса**.</span><span class="sxs-lookup"><span data-stu-id="8c852-141">To do this setup, go to **Resources** \> **Resource roles**.</span></span>

<span data-ttu-id="8c852-142">Кроме того, необходимо назначить роль по умолчанию всем резервируемым ресурсам.</span><span class="sxs-lookup"><span data-stu-id="8c852-142">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="8c852-143">Выберите **Ресурсы** \> **Ресурсы**.</span><span class="sxs-lookup"><span data-stu-id="8c852-143">Go to **Resources** \> **Resources**.</span></span> <span data-ttu-id="8c852-144">На вкладке **Project Service** убедитесь, что определена роль ресурса, и что в поле **По умолчанию** установлено значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="8c852-144">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field for it is set to **Yes**.</span></span> <span data-ttu-id="8c852-145">Можно добавить дополнительные роли, в которых **По умолчанию = Нет**.</span><span class="sxs-lookup"><span data-stu-id="8c852-145">You can add additional roles where **Is Default = No**.</span></span> <span data-ttu-id="8c852-146">Роль, в которой **По умолчанию = Да** , используется для оценки загруженности ресурса относительно цели для этой роли.</span><span class="sxs-lookup"><span data-stu-id="8c852-146">The role where the **Is Default = Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

<span data-ttu-id="8c852-147">На вкладке **Project Service** можно также задать индивидуальную целевую загруженность для ресурса.</span><span class="sxs-lookup"><span data-stu-id="8c852-147">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="8c852-148">Расчет загруженности затем использует целевую загруженность, чтобы оценить цель ресурса вместо цели роли ресурса по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8c852-148">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="8c852-149">Загруженность отображается для ресурса только в том случае, если этот ресурс имеет утвержденное оплачиваемое время в течение переиода, который отображается в сетке.</span><span class="sxs-lookup"><span data-stu-id="8c852-149">Utilization is shown for a resource only if that resource has approved, chargeable time during the period that is shown in the grid.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="8c852-150">Доступность ресурсов</span><span class="sxs-lookup"><span data-stu-id="8c852-150">Resource availability</span></span>

<span data-ttu-id="8c852-151">Важно, чтобы менеджеры по ресурсам могли просматривать доступность ресурсов и обновлять резервирования.</span><span class="sxs-lookup"><span data-stu-id="8c852-151">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="8c852-152">В некоторых случаях нет официального требования (запроса ресурса), но руководитель по ресурсам должен реагировать на незапланированное требование, которое поступает по таким каналам, как сообщение электронной почты, звонок или мгновенное сообщение.</span><span class="sxs-lookup"><span data-stu-id="8c852-152">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="8c852-153">Менеджеры по ресурсам используют доску расписания для обновления ресурсов и резервирований.</span><span class="sxs-lookup"><span data-stu-id="8c852-153">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="8c852-154">Рабочие часов ресурса используются в качестве основы для вычисления доступности ресурса.</span><span class="sxs-lookup"><span data-stu-id="8c852-154">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="8c852-155">Резервирования ресурсов потребляют производительность ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8c852-155">Resource bookings consume the capacity of the resources.</span></span>

<span data-ttu-id="8c852-156">Доска расписания использует цвета и затенение для индикации резервирований, доступности и избыточного резервирования, а также состояния резервирований.</span><span class="sxs-lookup"><span data-stu-id="8c852-156">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="8c852-157">Параметр в параметрах доски расписания позволяет показать условные обозначения.</span><span class="sxs-lookup"><span data-stu-id="8c852-157">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="8c852-158">Если стрелка вправо появляется рядом с отдельным резервируемым ресурсом на доске расписания, ресурс можно развернуть для отображения сведений о работе, для которой зарезервирован этот ресурс.</span><span class="sxs-lookup"><span data-stu-id="8c852-158">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

<span data-ttu-id="8c852-159">Поскольку Dynamics 365 Project Operations использует механизм Universal Resource Scheduling, то, если также установлен Dynamics 365 Field Service, можно просматривать сведения резервирований ресурсов для проектов, заказов на работу и любых других сущностей, на которые расширено планирование.</span><span class="sxs-lookup"><span data-stu-id="8c852-159">Because Dynamics 365 Project Operations uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

<span data-ttu-id="8c852-160">Для просмотра подробных сведений об отдельном ресурсе щелкните правой кнопкой мыши для открытия карточки ресурса.</span><span class="sxs-lookup"><span data-stu-id="8c852-160">To view more details about an individual resource, right-click it to open the resource card.</span></span>

