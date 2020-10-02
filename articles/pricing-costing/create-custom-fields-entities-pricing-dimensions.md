---
title: Создание настраиваемых полей и сущностей в качестве измерений цен
description: Эта тема предоставляет информацию о том, как создавать настраиваемые наборы параметров или сущности.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 2000f7e710267560fe2bd52b0e33024617d108ea
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898277"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="8529e-103">Создание настраиваемых полей и сущностей в качестве измерений цен</span><span class="sxs-lookup"><span data-stu-id="8529e-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="8529e-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="8529e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8529e-105">Выполните следующие шаги в любое время, когда требуется создать настраиваемый набор параметров или сущность.</span><span class="sxs-lookup"><span data-stu-id="8529e-105">Complete the following steps any time that you want to create a custom option set or entity.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8529e-106">Рекомендуется внести все изменения настраиваемых измерений ценообразования в отдельном решении.</span><span class="sxs-lookup"><span data-stu-id="8529e-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="8529e-107">Эта важная рекомендация гарантирует гибкость в будущем для обновления или удаления изменений по мере необходимости, поможет с повторным использованием вашей работы и упростит перенос этих изменений в другой экземпляр.</span><span class="sxs-lookup"><span data-stu-id="8529e-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="8529e-108">После внесения всех требуемых изменений экспортируйте это решение как **Управляемое решение** и импортируйте его в другие экземпляры, чтобы повторно использовать настройку ценообразования.</span><span class="sxs-lookup"><span data-stu-id="8529e-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="8529e-109">Создание настраиваемого решения для измерений ценообразования</span><span class="sxs-lookup"><span data-stu-id="8529e-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="8529e-110">Перейдите в раздел **Параметры** > **Решения**, затем выберите **Создать**, чтобы создать новое решение.</span><span class="sxs-lookup"><span data-stu-id="8529e-110">Go to **Settings** > **Solutions**, and then select **New** to create a new solution.</span></span> 
2. <span data-ttu-id="8529e-111">Назовите решение, **Измерения ценообразования \<your organization name>**, введите остальные необходимые сведения, затем выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="8529e-111">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then select **Save**.</span></span>
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="8529e-112">Создание настраиваемых полей и наборов параметров в решении измерений ценообразования</span><span class="sxs-lookup"><span data-stu-id="8529e-112">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="8529e-113">Изменение ценообразования может быть набором параметров или сущностью.</span><span class="sxs-lookup"><span data-stu-id="8529e-113">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="8529e-114">Оба необходимо создать в вашем решении ценообразования.</span><span class="sxs-lookup"><span data-stu-id="8529e-114">Both must be created in your pricing solution.</span></span> <span data-ttu-id="8529e-115">Шаги данной процедуры объясняют, как создавать измерения на основе сущности измерения на основе набора параметров.</span><span class="sxs-lookup"><span data-stu-id="8529e-115">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="8529e-116">Измерения на основе сущности</span><span class="sxs-lookup"><span data-stu-id="8529e-116">Entity-based dimensions</span></span>

1. <span data-ttu-id="8529e-117">Перейдите в пункт **Параметры** > **Решения** и затем дважды щелкните **Измерения ценообразования \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="8529e-117">Go to **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="8529e-118">В обозревателе решений в левой навигационной панели выберите **Сущности**.</span><span class="sxs-lookup"><span data-stu-id="8529e-118">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="8529e-119">Выберите **Создать** для создания новой сущности с названием **Стандартный заголовок**.</span><span class="sxs-lookup"><span data-stu-id="8529e-119">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="8529e-120">Введите остальные обязательные сведения, затем выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="8529e-120">Enter the remaining required information, and then select **Save**.</span></span>


### <a name="option-set-based-dimensions"></a><span data-ttu-id="8529e-121">Измерения на основе набора параметров</span><span class="sxs-lookup"><span data-stu-id="8529e-121">Option set-based dimensions</span></span> 
<span data-ttu-id="8529e-122">Можно создать два измерения на основе набора параметров.</span><span class="sxs-lookup"><span data-stu-id="8529e-122">You can create two option set-based dimensions.</span></span> <span data-ttu-id="8529e-123">Используйте **Место работы ресурса** для отслеживания цены места работы **Дом** и работы **На месте**, и используйте **Рабочие часы ресурса** со значениями **Обычные** и **Сверхурочные** для применения наценки после завершения работы.</span><span class="sxs-lookup"><span data-stu-id="8529e-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="8529e-124">Перейдите в пункт **Параметры** > **Решения** и дважды щелкните **Измерения ценообразования \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="8529e-124">Go to **Settings** > **Solutions**, and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="8529e-125">В обозревателе решений в левой навигационной панели выберите **Наборы параметров**.</span><span class="sxs-lookup"><span data-stu-id="8529e-125">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="8529e-126">Выберите **Создать** для создания нового набора параметров, введите остальное обязательные сведения, затем выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="8529e-126">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="8529e-127">Создание данные для измерений на основе сущности</span><span class="sxs-lookup"><span data-stu-id="8529e-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="8529e-128">Можно создавать данные для измерений на основе сущности вручную или с помощью импорта Microsoft Excel или служебных вызовов.</span><span class="sxs-lookup"><span data-stu-id="8529e-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="8529e-129">Используйте шаги в этой процедуре для создания двух стандартных заголовков, **Системный инженер** и **Главный системный инженер** из измерения на основе сущности, **Стандартный заголовок**.</span><span class="sxs-lookup"><span data-stu-id="8529e-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="8529e-130">Если данные, которые нужно создать, небольшие, как в следующем примере, можно использовать стандартную форму.</span><span class="sxs-lookup"><span data-stu-id="8529e-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="8529e-131">Выберите **Расширенный поиск**, выберите сущность **Стандартный заголовок**, затем выберите **Результаты**.</span><span class="sxs-lookup"><span data-stu-id="8529e-131">Select **Advanced Find**, select the entity **Standard Title**, and then select **Results**.</span></span> <span data-ttu-id="8529e-132">Отображаются все строки в сущности **Стандартный заголовок**.</span><span class="sxs-lookup"><span data-stu-id="8529e-132">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="8529e-133">Выберите **Создать** и в поле **Имя** введите "Системный инженер" и затем выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="8529e-133">Select **New**, and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
3. <span data-ttu-id="8529e-134">Закрытие формы.</span><span class="sxs-lookup"><span data-stu-id="8529e-134">Close the form.</span></span> 
4. <span data-ttu-id="8529e-135">Повторите шаги с 1 по 3 для создания другого стандартного заголовка для "Главный системный инженер".</span><span class="sxs-lookup"><span data-stu-id="8529e-135">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="8529e-136">Добавление всех требуемых сущностей и связанных компонентов в решение измерения ценообразования</span><span class="sxs-lookup"><span data-stu-id="8529e-136">Add all required entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="8529e-137">Необходимо добавить следующие сущности в ваше решение ценообразования.</span><span class="sxs-lookup"><span data-stu-id="8529e-137">You will need to add the following entities to your pricing solution.</span></span> <span data-ttu-id="8529e-138">Используйте шаги в этой процедуре, чтобы выполнить некоторые важные изменения схемы в решении ценообразования, чтобы сущности знали о новых измерениях ценообразования.</span><span class="sxs-lookup"><span data-stu-id="8529e-138">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="8529e-139">Выберите **Параметры** > **Решения** и дважды щелкните **Измерения ценообразования \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="8529e-139">Select **Settings** > **Solutions**, and double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="8529e-140">В обозревателе решений в левой навигационной панели выберите **Добавить существующий** > **Сущности**.</span><span class="sxs-lookup"><span data-stu-id="8529e-140">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="8529e-141">В диалоговом окне **Компоненты решения** выберите следующие сущности:</span><span class="sxs-lookup"><span data-stu-id="8529e-141">In the **Solution Components** dialog box, select the following entities:</span></span>

  - <span data-ttu-id="8529e-142">Фактические</span><span class="sxs-lookup"><span data-stu-id="8529e-142">Actual</span></span>
  - <span data-ttu-id="8529e-143">Резервируемый ресурс</span><span class="sxs-lookup"><span data-stu-id="8529e-143">Bookable Resource</span></span>
  - <span data-ttu-id="8529e-144">Строка оценки</span><span class="sxs-lookup"><span data-stu-id="8529e-144">Estimate Line</span></span>
  - <span data-ttu-id="8529e-145">Сведения строки счета</span><span class="sxs-lookup"><span data-stu-id="8529e-145">Invoice Line Detail</span></span>
  - <span data-ttu-id="8529e-146">Строка журнала</span><span class="sxs-lookup"><span data-stu-id="8529e-146">Journal Line</span></span>
  - <span data-ttu-id="8529e-147">Сведения строки контракта проекта</span><span class="sxs-lookup"><span data-stu-id="8529e-147">Project Contract Line Detail</span></span>
  - <span data-ttu-id="8529e-148">Участник проектной группы</span><span class="sxs-lookup"><span data-stu-id="8529e-148">Project Team Member</span></span>
  - <span data-ttu-id="8529e-149">Сведения строки предложения с расценками</span><span class="sxs-lookup"><span data-stu-id="8529e-149">Quote Line Detail</span></span>
  - <span data-ttu-id="8529e-150">Наценка цены роли</span><span class="sxs-lookup"><span data-stu-id="8529e-150">Role Price Markup</span></span>
  - <span data-ttu-id="8529e-151">Цена роли</span><span class="sxs-lookup"><span data-stu-id="8529e-151">Role Price</span></span> 
  - <span data-ttu-id="8529e-152">Запись времени</span><span class="sxs-lookup"><span data-stu-id="8529e-152">Time Entry</span></span> 


> [!NOTE]
> <span data-ttu-id="8529e-153">Обязательно включите все формы и представления для каждой выбранной сущности.</span><span class="sxs-lookup"><span data-stu-id="8529e-153">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="8529e-154">При появлении запроса на включение всех зависимых сущностей для выбранных выше сущностей выберите **Нет**.</span><span class="sxs-lookup"><span data-stu-id="8529e-154">When prompted to include any dependent entities for the entities selected above, select **No**.</span></span>

