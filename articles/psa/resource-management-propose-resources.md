---
title: Предложение ресурсов проекта
description: В этом разделе представлена информация о предложении ресурсов проекта.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 2003f6f06912b0c47eb942aae17e509b00e19487
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283024"
---
# <a name="propose-project-resources"></a><span data-ttu-id="6a618-103">Предложение ресурсов проекта</span><span class="sxs-lookup"><span data-stu-id="6a618-103">Propose project resources</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="6a618-104">Менеджеры по ресурсам могут предложить ресурс руководителю проекта с помощью запроса ресурса.</span><span class="sxs-lookup"><span data-stu-id="6a618-104">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="6a618-105">В сетке запросов либо в самом запросе выберите **Найти ресурсы**.</span><span class="sxs-lookup"><span data-stu-id="6a618-105">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="6a618-106">На странице **Помощник по расписанию** выберите ресурс, затем в области **Создать резервирование ресурса** в поле **Состояние резервирования** выберите **Резервировать**.</span><span class="sxs-lookup"><span data-stu-id="6a618-106">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

    ![Выбран предлагаемый ресурс](media/Resource-Management-image62.png)

<span data-ttu-id="6a618-108">Следующие обновления статуса происходят:</span><span class="sxs-lookup"><span data-stu-id="6a618-108">The following status updates occur:</span></span>

- <span data-ttu-id="6a618-109">На странице **Помощник по расписанию**, индикаторы состояния обновляются для указания, что резервирование предложено, это не жесткое резервирование.</span><span class="sxs-lookup"><span data-stu-id="6a618-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>

    ![Индикаторы состояния для предложенного резервирования на странице "Помощник по расписанию"](media/Resource-Management-image63.png)

- <span data-ttu-id="6a618-111">В запросе ресурса состояние меняется на **Требует проверки**.</span><span class="sxs-lookup"><span data-stu-id="6a618-111">On the resource request, the status is changed to **Needs Review**.</span></span>

    ![Состояние запроса ресурса меняется на "Требует проверки"](media/Resource-Management-image64.png)

- <span data-ttu-id="6a618-113">На вкладке **Рабочая группа** проекта значение в столбце **Состояние запроса** универсального участника группы изменяется на **Требует проверки**.</span><span class="sxs-lookup"><span data-stu-id="6a618-113">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

    ![Состояние запроса универсального участника группы изменено на "Требует проверки" на вкладке "Рабочая группа"](media/Resource-Management-image48.png)

<span data-ttu-id="6a618-115">Руководитель проекта может принять или отклонить предложение.</span><span class="sxs-lookup"><span data-stu-id="6a618-115">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="6a618-116">Когда менеджеры по ресурсам обрабатывают запросы ресурсов, они могут использовать любой из приведенных ниже способов:</span><span class="sxs-lookup"><span data-stu-id="6a618-116">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="6a618-117">Предложить несколько ресурсов, чтобы удовлетворять требование, если один подходящий ресурс недоступен, чтобы заполнить необходимые часы.</span><span class="sxs-lookup"><span data-stu-id="6a618-117">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="6a618-118">Предложенные часы затем разделяются между несколькими ресурсами, которые могут удовлетворить необходимые часы.</span><span class="sxs-lookup"><span data-stu-id="6a618-118">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="6a618-119">В этом сценарии часы не могут перекрываться.</span><span class="sxs-lookup"><span data-stu-id="6a618-119">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="6a618-120">Предложить меньше ресурсов, чем требуется.</span><span class="sxs-lookup"><span data-stu-id="6a618-120">Propose fewer resources than are required.</span></span> <span data-ttu-id="6a618-121">В этом сценарии предложенная производительность ресурса меньше требуемых часов, указанных автором запроса.</span><span class="sxs-lookup"><span data-stu-id="6a618-121">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="6a618-122">Следовательно, когда запрашивающая сторона принимает предлагаемые ресурсы, создается невыполненный запрос ресурсов, чтобы покрыть оставшееся требование.</span><span class="sxs-lookup"><span data-stu-id="6a618-122">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="6a618-123">Зарезервировать несколько ресурсов, чтобы удовлетворять требование, если никакой один ресурс недоступен, чтобы выполнить работу.</span><span class="sxs-lookup"><span data-stu-id="6a618-123">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="6a618-124">Зарезервировать меньше ресурсов, чем требуется.</span><span class="sxs-lookup"><span data-stu-id="6a618-124">Book fewer resources than are required.</span></span> <span data-ttu-id="6a618-125">В этом сценарии зарезервированные часы меньше, чем требуемые часы.</span><span class="sxs-lookup"><span data-stu-id="6a618-125">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="6a618-126">Система подсказывает вам, что следует предложить ресурсы вместо резервирования, чтобы запрашивающая сторона могла проверить и отслеживать оставшееся требование.</span><span class="sxs-lookup"><span data-stu-id="6a618-126">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="billable-utilization"></a><span data-ttu-id="6a618-127">Оплачиваемая загруженность</span><span class="sxs-lookup"><span data-stu-id="6a618-127">Billable utilization</span></span>

<span data-ttu-id="6a618-128">Ресурсы могут иметь целевую оплачиваемую загруженность.</span><span class="sxs-lookup"><span data-stu-id="6a618-128">Resources can have a target billable utilization.</span></span> <span data-ttu-id="6a618-129">Эта целевая загруженность определяется как атрибут роли ресурса по умолчанию или задается в записи отдельного резервируемого ресурса.</span><span class="sxs-lookup"><span data-stu-id="6a618-129">This target utilization is either defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="6a618-130">Расчеты загруженности основаны на фактических часах, о которых сообщают ресурсы с помощью утвержденных записей времени.</span><span class="sxs-lookup"><span data-stu-id="6a618-130">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="6a618-131">Формулы следующие используются для расчета загруженности:</span><span class="sxs-lookup"><span data-stu-id="6a618-131">The following formulas are used to calculate utilization:</span></span>

- <span data-ttu-id="6a618-132">Оплачиваемая загруженность = Оплачиваемые фактические часов ÷ Производительность ресурса</span><span class="sxs-lookup"><span data-stu-id="6a618-132">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
- <span data-ttu-id="6a618-133">Неоплачиваемая загруженность = Фактическое время с ИД типа выставления счетов = Не подлежит оплате, Бесплатно или Недоступно ÷ Производительность ресурса</span><span class="sxs-lookup"><span data-stu-id="6a618-133">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
- <span data-ttu-id="6a618-134">Внутреннее = Фактическое время без контракта на продажу ÷ Производительность ресурса</span><span class="sxs-lookup"><span data-stu-id="6a618-134">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
- <span data-ttu-id="6a618-135">Производительность ресурса = Рабочие часы ресурса – Не на работе – Нерабочие дни</span><span class="sxs-lookup"><span data-stu-id="6a618-135">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="6a618-136">Представление **Загруженность ресурсов** можно найти на панели **Ресурсы**.</span><span class="sxs-lookup"><span data-stu-id="6a618-136">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

![Представление загруженности ресурсов](media/Resource-Management-image65.png)

<span data-ttu-id="6a618-138">Каждая ячейка в сетке представляет процент оплачиваемой загруженности ресурса в период, такой как день, неделя или месяц.</span><span class="sxs-lookup"><span data-stu-id="6a618-138">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="6a618-139">Следующие формулы используются для задания цветов ячеек:</span><span class="sxs-lookup"><span data-stu-id="6a618-139">The following formulas are used to color the cells:</span></span>

- <span data-ttu-id="6a618-140">**Зеленый**: Оплачиваемая загруженность \>= Целевая загруженность ресурса</span><span class="sxs-lookup"><span data-stu-id="6a618-140">**Green:** Billable utilization \>= Resource target utilization</span></span>
- <span data-ttu-id="6a618-141">**Желтый**: Целевая загруженность – 20 \<= Оплачиваемая загруженность \< Целевая загруженность</span><span class="sxs-lookup"><span data-stu-id="6a618-141">**Yellow:** Target utilization – 20 \<= Billable utilization \< Target utilization</span></span>
- <span data-ttu-id="6a618-142">**Красный:** Оплачиваемая загруженность \< Целевая загруженность – 20</span><span class="sxs-lookup"><span data-stu-id="6a618-142">**Red:** Billable utilization \< Target utilization – 20</span></span>

<span data-ttu-id="6a618-143">Поскольку представление **Загруженность ресурсов** основано на доске расписания, можно использовать возможности фильтрации доски расписания для фильтрации результатов.</span><span class="sxs-lookup"><span data-stu-id="6a618-143">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="6a618-144">Сетка требует, чтобы вы задали целевую загруженность для роли или отдельного ресурса.</span><span class="sxs-lookup"><span data-stu-id="6a618-144">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="6a618-145">Чтобы выполнить эту настройку, выберите **Ресурсы** \> **Роли ресурса**.</span><span class="sxs-lookup"><span data-stu-id="6a618-145">To do this setup, go to **Resources** \> **Resource roles**.</span></span>

<span data-ttu-id="6a618-146">Кроме того, необходимо назначить роль по умолчанию всем резервируемым ресурсам.</span><span class="sxs-lookup"><span data-stu-id="6a618-146">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="6a618-147">Выберите **Ресурсы** \> **Ресурсы**.</span><span class="sxs-lookup"><span data-stu-id="6a618-147">Go to **Resources** \> **Resources**.</span></span> <span data-ttu-id="6a618-148">На вкладке **Project Service** убедитесь, что определена роль ресурса, и что в поле **По умолчанию** установлено значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="6a618-148">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field for it is set to **Yes**.</span></span> <span data-ttu-id="6a618-149">Можно добавить дополнительные роли, в которых **По умолчанию = Нет**.</span><span class="sxs-lookup"><span data-stu-id="6a618-149">You can add additional roles where **Is Default = No**.</span></span> <span data-ttu-id="6a618-150">Роль, в которой **По умолчанию = Да**, используется для оценки загруженности ресурса относительно цели для этой роли.</span><span class="sxs-lookup"><span data-stu-id="6a618-150">The role where the **Is Default = Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

![Задана роль по умолчанию](media/Resource-Management-image67.png)

<span data-ttu-id="6a618-152">На вкладке **Project Service** можно также задать индивидуальную целевую загруженность для ресурса.</span><span class="sxs-lookup"><span data-stu-id="6a618-152">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="6a618-153">Расчет загруженности затем использует целевую загруженность, чтобы оценить цель ресурса вместо цели роли ресурса по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6a618-153">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="6a618-154">Загруженность отображается для ресурса только в том случае, если этот ресурс имеет утвержденное оплачиваемое время в течение переиода, который отображается в сетке.</span><span class="sxs-lookup"><span data-stu-id="6a618-154">Utilization is shown for a resource only if that resource has approved, chargeable time during the period that is shown in the grid.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="6a618-155">Доступность ресурсов</span><span class="sxs-lookup"><span data-stu-id="6a618-155">Resource availability</span></span>

<span data-ttu-id="6a618-156">Важно, чтобы менеджеры по ресурсам могли просматривать доступность ресурсов и обновлять резервирования.</span><span class="sxs-lookup"><span data-stu-id="6a618-156">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="6a618-157">В некоторых случаях нет официального требования (запроса ресурса), но руководитель по ресурсам должен реагировать на незапланированное требование, которое поступает по таким каналам, как сообщение электронной почты, звонок или мгновенное сообщение.</span><span class="sxs-lookup"><span data-stu-id="6a618-157">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="6a618-158">Менеджеры по ресурсам используют доску расписания для обновления ресурсов и резервирований.</span><span class="sxs-lookup"><span data-stu-id="6a618-158">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="6a618-159">Рабочие часов ресурса используются в качестве основы для вычисления доступности ресурса.</span><span class="sxs-lookup"><span data-stu-id="6a618-159">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="6a618-160">Резервирования ресурсов потребляют производительность ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6a618-160">Resource bookings consume the capacity of the resources.</span></span>

![Таблица расписаний](media/Resource-Management-image68.png)

<span data-ttu-id="6a618-162">Доска расписания использует цвета и затенение для индикации резервирований, доступности и избыточного резервирования, а также состояния резервирований.</span><span class="sxs-lookup"><span data-stu-id="6a618-162">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="6a618-163">Параметр в параметрах доски расписания позволяет показать условные обозначения.</span><span class="sxs-lookup"><span data-stu-id="6a618-163">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="6a618-164">Если стрелка вправо появляется рядом с отдельным резервируемым ресурсом на доске расписания, ресурс можно развернуть для отображения сведений о работе, для которой зарезервирован этот ресурс.</span><span class="sxs-lookup"><span data-stu-id="6a618-164">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

![Резервируемый ресурс, развернутый на доску расписания](media/Resource-Management-image69.png)

<span data-ttu-id="6a618-166">Поскольку Dynamics 365 Project Service Automation использует механизм Universal Resource Scheduling, то, если также установлен Dynamics 365 Field Service, можно просматривать сведения резервирований ресурсов для проектов, заказов на работу и любых других сущностей, на которые расширено планирование.</span><span class="sxs-lookup"><span data-stu-id="6a618-166">Because Dynamics 365 Project Service Automation uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

![Сведения резервирований ресурсов для проектов и заказов на работу](media/Resource-Management-image70.png)

<span data-ttu-id="6a618-168">Для просмотра подробных сведений об отдельном ресурсе щелкните правой кнопкой мыши для открытия карточки ресурса.</span><span class="sxs-lookup"><span data-stu-id="6a618-168">To view more details about an individual resource, right-click it to open the resource card.</span></span>

![Карточка ресурса](media/Resource-Management-image71.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]