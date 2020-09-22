---
title: Создание настраиваемых полей и сущностей
description: В этом разделе объясняется, как создавать наборы параметров и сущности в вашем собственном решении на платформе Power Apps.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/26/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: fb160bfd-e037-4a21-a968-3ff2e6e16481
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 7ee30e3bb6b8034ef226e2e9181195685355011f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755021"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="1ad1c-103">Создание настраиваемых полей и сущностей</span><span class="sxs-lookup"><span data-stu-id="1ad1c-103">Create custom fields and entities</span></span> 

<span data-ttu-id="1ad1c-104">Выполните следующие шаги в любое время, когда требуется создать настраиваемый набор параметров или сущность на платформе Power Apps.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="1ad1c-105">Процедуры в данном разделе необходимо выполнить с помощью веб-интерфейса Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="1ad1c-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1ad1c-106">Рекомендуется внести все изменения настраиваемых измерений ценообразования в отдельном решении.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="1ad1c-107">Эта важная рекомендация гарантирует гибкость в будущем для обновления или удаления изменений по мере необходимости, поможет с повторным использованием вашей работы и упростит перенос этих изменений в другой экземпляр.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="1ad1c-108">После внесения всех требуемых изменений экспортируйте это решение как **Управляемое решение** и импортируйте его в другие экземпляры, чтобы повторно использовать настройку ценообразования.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="1ad1c-109">Создание настраиваемого решения для измерений ценообразования</span><span class="sxs-lookup"><span data-stu-id="1ad1c-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="1ad1c-110">В PSA выберите **Параметры** > **Решения**, затем щелкните **Создать**, чтобы создать новое решение.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-110">In PSA, click **Settings** > **Solutions**, and then click **New** to create a new solution.</span></span> 
2. <span data-ttu-id="1ad1c-111">Назовите решение, **Измерения ценообразования \<название вашей организации>**, введите остальные необходимые сведения, затем щелкните **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-111">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then click **Save**.</span></span>

> ![Создание настраиваемого решения для измерений ценообразования](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="1ad1c-113">Создание настраиваемых полей и наборов параметров в решении измерений ценообразования</span><span class="sxs-lookup"><span data-stu-id="1ad1c-113">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="1ad1c-114">Изменение ценообразования может быть набором параметров или сущностью.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-114">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="1ad1c-115">Оба необходимо создать в вашем решении ценообразования.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-115">Both must be created in your pricing solution.</span></span> <span data-ttu-id="1ad1c-116">Шаги данной процедуры объясняют, как создавать измерения на основе сущности измерения на основе набора параметров.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-116">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="1ad1c-117">Измерения на основе сущности</span><span class="sxs-lookup"><span data-stu-id="1ad1c-117">Entity-based dimensions</span></span>

1. <span data-ttu-id="1ad1c-118">В PSA щелкните **Параметры** > **Решения**, затем дважды щелкните **Аналитики ценообразования \<название вашей организации>**.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-118">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="1ad1c-119">В обозревателе решений в левой навигационной панели выберите **Сущности**.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-119">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="1ad1c-120">Щелкните **Создать** для создания новой сущности с названием **Стандартный заголовок**.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-120">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="1ad1c-121">Введите остальные обязательные сведения, затем щелкните **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-121">Enter the remaining required information, and then click **Save**.</span></span>

> ![Определение сущности стандартного заголовка](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="1ad1c-123">Измерения на основе набора параметров</span><span class="sxs-lookup"><span data-stu-id="1ad1c-123">Option set-based dimensions</span></span> 
<span data-ttu-id="1ad1c-124">Можно создать два измерения на основе набора параметров.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-124">You can create two option set-based dimensions.</span></span> <span data-ttu-id="1ad1c-125">Используйте **Место работы ресурса** для отслеживания цены места работы **Дом** и работы **На месте**, и используйте **Рабочие часы ресурса** со значениями **Обычные** и **Сверхурочные** для применения наценки после завершения работы.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-125">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="1ad1c-126">В PSA щелкните **Параметры** > **Решения**, затем дважды щелкните **Аналитики ценообразования \<название вашей организации>**.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-126">In PSA, click **Settings** > **Solutions**, and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="1ad1c-127">В обозревателе решений в левой навигационной панели выберите **Наборы параметров**.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-127">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="1ad1c-128">Щелкните **Создать** для создания нового набора параметров, введите остальное обязательные сведения, затем нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-128">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="1ad1c-129">Измерение ценообразования на основе набора параметров под названием "Место работы ресурса"</span><span class="sxs-lookup"><span data-stu-id="1ad1c-129">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="1ad1c-130">Измерение ценообразования на основе набора параметров под названием "Рабочие часы ресурса"</span><span class="sxs-lookup"><span data-stu-id="1ad1c-130">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="1ad1c-131">Создание данные для измерений на основе сущности</span><span class="sxs-lookup"><span data-stu-id="1ad1c-131">Create data for entity-based dimensions</span></span>

<span data-ttu-id="1ad1c-132">Можно создавать данные для измерений на основе сущности вручную или с помощью импорта Microsoft Excel или служебных вызовов.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-132">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="1ad1c-133">Используйте шаги в этой процедуре для создания двух стандартных заголовков, **Системный инженер** и **Главный системный инженер** из измерения на основе сущности, **Стандартный заголовок**.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-133">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="1ad1c-134">Если данные, которые нужно создать, небольшие, как в следующем примере, можно использовать стандартную форму.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-134">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="1ad1c-135">В PSA щелкните **Расширенный поиск**.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-135">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="1ad1c-136">Выделите сущность **Стандартный заголовок**, затем щелкните **Результаты**.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-136">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="1ad1c-137">Отображаются все строки в сущности **Стандартный заголовок**.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-137">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="1ad1c-138">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-138">Click **New**.</span></span> <span data-ttu-id="1ad1c-139">В поле **Имя** введите "Системный инженер" и нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-139">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="1ad1c-140">Закройте форму.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-140">Close the form.</span></span> 
4. <span data-ttu-id="1ad1c-141">Повторите шаги с 1 по 3 для создания другого стандартного заголовка для "Главный системный инженер".</span><span class="sxs-lookup"><span data-stu-id="1ad1c-141">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="1ad1c-142">Демонстрационные данные для сущности стандартного заголовка</span><span class="sxs-lookup"><span data-stu-id="1ad1c-142">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)

## <a name="add-all-required-psa-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="1ad1c-143">Добавление всех требуемых сущностей PSA и связанных компонентов в решение измерения ценообразования</span><span class="sxs-lookup"><span data-stu-id="1ad1c-143">Add all required PSA entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="1ad1c-144">Необходимо добавить следующие сущности Project Service в ваше решение ценообразования.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-144">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="1ad1c-145">Используйте шаги в этой процедуре, чтобы выполнить некоторые важные изменения схемы в решении ценообразования, чтобы сущности знали о новых измерениях ценообразования.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-145">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="1ad1c-146">В PSA щелкните **Параметры** > **Решения**, затем дважды щелкните **Аналитики ценообразования \<название вашей организации>**.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-146">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="1ad1c-147">В обозревателе решений в левой навигационной панели выберите **Добавить существующий** > **Сущности**.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-147">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="1ad1c-148">В диалоговом окне **Компоненты решения** выберите следующие сущности:</span><span class="sxs-lookup"><span data-stu-id="1ad1c-148">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="1ad1c-149">Фактические</span><span class="sxs-lookup"><span data-stu-id="1ad1c-149">Actual</span></span>
- <span data-ttu-id="1ad1c-150">Резервируемый ресурс</span><span class="sxs-lookup"><span data-stu-id="1ad1c-150">Bookable Resource</span></span>
- <span data-ttu-id="1ad1c-151">Строка оценки</span><span class="sxs-lookup"><span data-stu-id="1ad1c-151">Estimate Line</span></span>
- <span data-ttu-id="1ad1c-152">Сведения строки счета</span><span class="sxs-lookup"><span data-stu-id="1ad1c-152">Invoice Line Detail</span></span>
- <span data-ttu-id="1ad1c-153">Строка журнала</span><span class="sxs-lookup"><span data-stu-id="1ad1c-153">Journal Line</span></span>
- <span data-ttu-id="1ad1c-154">Сведения строки контракта проекта</span><span class="sxs-lookup"><span data-stu-id="1ad1c-154">Project Contract Line Detail</span></span>
- <span data-ttu-id="1ad1c-155">Участник проектной группы</span><span class="sxs-lookup"><span data-stu-id="1ad1c-155">Project Team Member</span></span>
- <span data-ttu-id="1ad1c-156">Сведения строки предложения с расценками</span><span class="sxs-lookup"><span data-stu-id="1ad1c-156">Quote Line Detail</span></span>
- <span data-ttu-id="1ad1c-157">Наценка цены роли</span><span class="sxs-lookup"><span data-stu-id="1ad1c-157">Role Price Markup</span></span>
- <span data-ttu-id="1ad1c-158">Цена роли</span><span class="sxs-lookup"><span data-stu-id="1ad1c-158">Role Price</span></span> 
- <span data-ttu-id="1ad1c-159">Запись времени</span><span class="sxs-lookup"><span data-stu-id="1ad1c-159">Time Entry</span></span> 

> ![Добавление существующих сущностей в решение измерения ценообразования](media/Existing-entities-to-PD-solution.png)

> ![Выберите компоненты решения](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="1ad1c-162">Обязательно включите все формы и представления для каждой выбранной сущности.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-162">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="1ad1c-163">При появлении запроса на включение всех зависимых сущностей для выбранных выше сущностей щелкните **Нет**.</span><span class="sxs-lookup"><span data-stu-id="1ad1c-163">When prompted to include any dependent entities for the entities selected above, click **No**.</span></span>

> ![Не включайте все связанные компоненты](media/Do-not-include-required.png)


