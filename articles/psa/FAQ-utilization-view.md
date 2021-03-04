---
title: Просмотр оплачиваемой загруженности для ресурсов
description: В этом разделе представлена информация о представлении загруженности ресурсов.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: 4516c562e7eaf35c5fef638183967eef5a033b11
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146409"
---
# <a name="view-chargeable-utilization-for-resources"></a><span data-ttu-id="7d5a9-103">Просмотр оплачиваемой загруженности для ресурсов</span><span class="sxs-lookup"><span data-stu-id="7d5a9-103">View chargeable utilization for resources</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]
 
<span data-ttu-id="7d5a9-104">**Представление загруженности** на странице **Загруженность ресурсов Project Service** отображает оплачиваемую загруженность для каждого резервируемого ресурса.</span><span class="sxs-lookup"><span data-stu-id="7d5a9-104">The **Utilization View** on the **Project Service Resource Utilization** page shows the chargeable utilization for each bookable resource.</span></span> <span data-ttu-id="7d5a9-105">Поскольку это представление основано на доске расписания, вы найдете много тех же функций.</span><span class="sxs-lookup"><span data-stu-id="7d5a9-105">Because the view is based on the schedule board, you’ll find many of the same functions.</span></span>

> ![Снимок экрана представления загруженности](media/FAQ-utilization-1.png)
 

<span data-ttu-id="7d5a9-107">Расчет оплачиваемой загруженности работает следующим образом:</span><span class="sxs-lookup"><span data-stu-id="7d5a9-107">The chargeable utilization calculation works as follows:</span></span>

   <span data-ttu-id="7d5a9-108">Оплачиваемая загруженность = (Оплачиваемые фактические часы) / (производительность ресурса)</span><span class="sxs-lookup"><span data-stu-id="7d5a9-108">Chargeable utilization = (Chargeable actual hours) / (resource capacity)</span></span>

<span data-ttu-id="7d5a9-109">Ячейки представляют расчетную оплачиваемую загруженность за выбранный период (дни, недели или месяцы).</span><span class="sxs-lookup"><span data-stu-id="7d5a9-109">The cells represent the calculated chargeable utilization for the selected period (days, weeks, or months).</span></span>

<span data-ttu-id="7d5a9-110">Цвета каждой ячейки показывают оплачиваемую загруженность для ресурса по сравнению с их целевой оплачиваемой загруженностью.</span><span class="sxs-lookup"><span data-stu-id="7d5a9-110">The colors in each cell show the chargeable utilization for a resource as compared to their target chargeable utilization.</span></span> 

<span data-ttu-id="7d5a9-111">Целевую загруженность можно установить для роли ресурса по умолчанию или для самого отдельного ресурса.</span><span class="sxs-lookup"><span data-stu-id="7d5a9-111">The target utilization can be set on the resource’s default role or on the individual resource itself.</span></span> <span data-ttu-id="7d5a9-112">Расчет сначала ищет индивидуальное значение для цели, затем роль ресурса по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7d5a9-112">The calculation looks at the individual for the target first, and then to the resource’s default role.</span></span>

## <a name="set-target-on-a-resource"></a><span data-ttu-id="7d5a9-113">Установка цели по ресурсу</span><span class="sxs-lookup"><span data-stu-id="7d5a9-113">Set target on a resource</span></span>

1. <span data-ttu-id="7d5a9-114">Выберите **Ресурсы** \> **Ресурсы**.</span><span class="sxs-lookup"><span data-stu-id="7d5a9-114">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="7d5a9-115">Выберите ресурс, чтобы открыть запись.</span><span class="sxs-lookup"><span data-stu-id="7d5a9-115">Select a resource to open the record.</span></span> 
3. <span data-ttu-id="7d5a9-116">На вкладке **Project Service** можно задать целевую загруженность ресурса.</span><span class="sxs-lookup"><span data-stu-id="7d5a9-116">On the **Project Service** tab, you can set the resource’s target utilization.</span></span>

> ![Снимок экрана использования вкладки Project Service для задания целевой загруженности](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a><span data-ttu-id="7d5a9-118">Задание целевой загруженности для роли</span><span class="sxs-lookup"><span data-stu-id="7d5a9-118">Set target utilization on a role</span></span>

1. <span data-ttu-id="7d5a9-119">Выберите **Ресурсы** \> **Роли ресурса**.</span><span class="sxs-lookup"><span data-stu-id="7d5a9-119">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="7d5a9-120">Выберите роль и откройте запись.</span><span class="sxs-lookup"><span data-stu-id="7d5a9-120">Select a role and open the record.</span></span> 
3. <span data-ttu-id="7d5a9-121">Задайте целевую загруженность для роли.</span><span class="sxs-lookup"><span data-stu-id="7d5a9-121">Set the target utilization for the role.</span></span>

> ![Снимок экрана использования пункта "Роли ресурса" для задания целевой загруженности](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a><span data-ttu-id="7d5a9-123">Вычисление оплачиваемой загруженности для ресурса</span><span class="sxs-lookup"><span data-stu-id="7d5a9-123">Calculate chargeable utilization for a resource</span></span>

<span data-ttu-id="7d5a9-124">Для вычисления оплачиваемой загруженности для ресурса потребуется выполнить несколько предварительных условий.</span><span class="sxs-lookup"><span data-stu-id="7d5a9-124">To calculate chargeable utilization for a resource, you will need to complete some pre-requisites.</span></span> 

### <a name="set-default-role-for-individual-resource"></a><span data-ttu-id="7d5a9-125">Задание роли по умолчанию для отдельного ресурса</span><span class="sxs-lookup"><span data-stu-id="7d5a9-125">Set default role for individual resource</span></span>

<span data-ttu-id="7d5a9-126">Во-первых, целевая загруженность должна быть задана для отдельного ресурса или для ролей ресурса.</span><span class="sxs-lookup"><span data-stu-id="7d5a9-126">First, the target utilization must be set on either the individual resource or on resource roles.</span></span> <span data-ttu-id="7d5a9-127">Если используются роли ресурса для целей, каждый отдельный ресурс должен иметь роль по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7d5a9-127">If you are using resource roles for targets, each individual resource must have a default role.</span></span> 

1. <span data-ttu-id="7d5a9-128">Чтобы установить это, откройте **Ресурсы** \> **Ресурсы**.</span><span class="sxs-lookup"><span data-stu-id="7d5a9-128">To set this, go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="7d5a9-129">Выберите ресурс, откройте запись, затем перейдите на вкладку **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="7d5a9-129">Select a resource, open the record, and then select the **Project Service** tab.</span></span> 
3. <span data-ttu-id="7d5a9-130">В сетке **Роль ресурса** убедитесь, что имеется одна роль для ресурса, и для параметра **По умолчанию** задано значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="7d5a9-130">In the **Resource Role** grid, make sure there’s one role for the resource and **Is Default** is set to **Yes**.</span></span>
 
### <a name="change-billing-type-for-resource-role"></a><span data-ttu-id="7d5a9-131">Изменение тип выставления счетов для роли ресурса</span><span class="sxs-lookup"><span data-stu-id="7d5a9-131">Change billing type for resource role</span></span>

<span data-ttu-id="7d5a9-132">Ролям ресурса необходимо задать тип выставления счетов **Оплачивается**.</span><span class="sxs-lookup"><span data-stu-id="7d5a9-132">The resource roles must be set to have a billing type of **Chargeable**.</span></span> 

1. <span data-ttu-id="7d5a9-133">Выберите **Ресурсы** \> **Роли ресурса**.</span><span class="sxs-lookup"><span data-stu-id="7d5a9-133">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="7d5a9-134">Откройте запись, которую требуется обновить, затем задайте тип выставления счетов по умолчанию **Оплачивается**.</span><span class="sxs-lookup"><span data-stu-id="7d5a9-134">Open the record you want to update, and then set the billing type default to **Chargeable**.</span></span>

### <a name="set-working-hours-for-resource-role"></a><span data-ttu-id="7d5a9-135">Задание рабочих часов для роли ресурса</span><span class="sxs-lookup"><span data-stu-id="7d5a9-135">Set working hours for resource role</span></span>
 
<span data-ttu-id="7d5a9-136">У ресурса должны быть рабочие часы для расчета производительности.</span><span class="sxs-lookup"><span data-stu-id="7d5a9-136">The resource must have working hours for the capacity calculation.</span></span> 

1. <span data-ttu-id="7d5a9-137">Выберите **Ресурсы** \> **Ресурсы**.</span><span class="sxs-lookup"><span data-stu-id="7d5a9-137">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="7d5a9-138">Выберите ресурс для открытия записи, затем выберите **Показать рабочие часы**.</span><span class="sxs-lookup"><span data-stu-id="7d5a9-138">Select a resource to open the record, and then select **Show Work Hours**.</span></span> 
3. <span data-ttu-id="7d5a9-139">Можно выполнять групповое обновление ресурсов, применив **Шаблон рабочих часов** из представления **Список ресурсов**.</span><span class="sxs-lookup"><span data-stu-id="7d5a9-139">You can bulk-update the list of resources by applying a **Work Hour Template** from the **Resource List** view.</span></span>

## <a name="troubleshooting-chargeable-actual-hours"></a><span data-ttu-id="7d5a9-140">Устранение неполадок оплачиваемых фактических часов</span><span class="sxs-lookup"><span data-stu-id="7d5a9-140">Troubleshooting chargeable actual hours</span></span>

<span data-ttu-id="7d5a9-141">Фактические оплачиваемые часы берутся из сущности **Фактические**.</span><span class="sxs-lookup"><span data-stu-id="7d5a9-141">The chargeable actual hours are sourced from the **Actuals** entity.</span></span> <span data-ttu-id="7d5a9-142">Фактические данные с типом выставления счетов **Оплачивается** включаются в расчет, и, по этой причине, необходимо иметь проекты, в которых фактические данные подлежат оплате.</span><span class="sxs-lookup"><span data-stu-id="7d5a9-142">Actuals with a billing type of **Chargeable** are included in the calculation and, for this reason, you must have projects where the actuals that are chargeable.</span></span>

<span data-ttu-id="7d5a9-143">Если вы не видите оплачиваемую загруженность, вот что можно проверить:</span><span class="sxs-lookup"><span data-stu-id="7d5a9-143">If you are not seeing chargeable utilization, here are some things you can check:</span></span>

- <span data-ttu-id="7d5a9-144">У ресурса для производительности определены рабочие часы.</span><span class="sxs-lookup"><span data-stu-id="7d5a9-144">The resource has working hours defined for capacity.</span></span>
- <span data-ttu-id="7d5a9-145">У ресурса имеется отдельно определенная целевая загруженность или ему назначена роль по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7d5a9-145">The resource has either an individually defined utilization target or has a default role assigned to it.</span></span> <span data-ttu-id="7d5a9-146">Для роли определена целевая загруженность.</span><span class="sxs-lookup"><span data-stu-id="7d5a9-146">The role has a utilization target defined for it.</span></span>
- <span data-ttu-id="7d5a9-147">Фактические данные имеют тип выставления счетов **Оплачивается** за период, для которого ожидается расчет загруженности.</span><span class="sxs-lookup"><span data-stu-id="7d5a9-147">Actuals have a billing type of **Chargeable** for the period you are expecting a utilization calculation for.</span></span> <span data-ttu-id="7d5a9-148">Проверьте следующее, если вы видите фактические данные с типами выставления счетов, отличными от оплачиваемых:</span><span class="sxs-lookup"><span data-stu-id="7d5a9-148">Check the following if you are seeing actuals with billing types other than chargeable:</span></span>

  - <span data-ttu-id="7d5a9-149">Роль, используемая для фактических данных, имеет типом выставления счетов по умолчанию, отличный от оплачиваемого.</span><span class="sxs-lookup"><span data-stu-id="7d5a9-149">The role used on the actual has a default billing type of something other than chargeable.</span></span>
  - <span data-ttu-id="7d5a9-150">Роль в строке контракта по проекту, поддерживающей проект, была установлена на неоплачиваемое значение.</span><span class="sxs-lookup"><span data-stu-id="7d5a9-150">The role on the project contract line backing the project has been set to non-chargeable.</span></span>
  - <span data-ttu-id="7d5a9-151">У проекта нет связанной строки контракта.</span><span class="sxs-lookup"><span data-stu-id="7d5a9-151">The project does not have an associated contract line.</span></span>

