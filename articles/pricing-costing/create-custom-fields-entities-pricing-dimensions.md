---
title: Создание настраиваемых полей и сущностей в качестве измерений цен
description: Эта тема предоставляет информацию о том, как создавать настраиваемые наборы параметров или сущности.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 41c57690fecbc3bee2a1eb5d26f8a6aa56d8bea9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000542"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="88399-103">Создание настраиваемых полей и сущностей в качестве измерений цен</span><span class="sxs-lookup"><span data-stu-id="88399-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="88399-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="88399-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="88399-105">Выполните следующие шаги, если требуется создать настраиваемый набор параметров для использования в качестве измерения цены.</span><span class="sxs-lookup"><span data-stu-id="88399-105">Complete the following steps when you want to create a custom option set or entity for using it as a pricing dimension.</span></span> <span data-ttu-id="88399-106">Дополнительные сведения см. в [Обзор измерений цен](pricing-dimensions-overview.md).</span><span class="sxs-lookup"><span data-stu-id="88399-106">For more information, see [Pricing dimensions overview](pricing-dimensions-overview.md).</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="88399-107">Рекомендуется внести все изменения настраиваемых измерений ценообразования в отдельном решении.</span><span class="sxs-lookup"><span data-stu-id="88399-107">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="88399-108">Эта важная рекомендация обеспечивает гибкость в будущем для обновления или удаления изменений по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="88399-108">This important best practice provides flexibility in the future to update or remove changes as needed.</span></span> <span data-ttu-id="88399-109">Это также поможет повторно использовать вашу работу и упростит перенос этих изменений в другой экземпляр. После внесения всех необходимых изменений экспортируйте это решение как **управляемое решение** и импортируйте его в другие экземпляры, чтобы повторно использовать настройки цен.</span><span class="sxs-lookup"><span data-stu-id="88399-109">This will also help with re-use of your work and make it easier to port these changes to another instance After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="88399-110">Создание настраиваемых полей и наборов параметров в решении измерений ценообразования</span><span class="sxs-lookup"><span data-stu-id="88399-110">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="88399-111">Изменение ценообразования может быть набором параметров или сущностью.</span><span class="sxs-lookup"><span data-stu-id="88399-111">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="88399-112">Оба необходимо создать в вашем решении ценообразования.</span><span class="sxs-lookup"><span data-stu-id="88399-112">Both must be created in your pricing solution.</span></span> <span data-ttu-id="88399-113">Шаги данной процедуры объясняют, как создавать измерения на основе сущности измерения на основе набора параметров.</span><span class="sxs-lookup"><span data-stu-id="88399-113">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="88399-114">Измерения на основе сущности</span><span class="sxs-lookup"><span data-stu-id="88399-114">Entity-based dimensions</span></span>
<span data-ttu-id="88399-115">Чтобы создать измерения на основе сущностей, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="88399-115">To create entity-based dimensions, follow these steps:</span></span>

1. <span data-ttu-id="88399-116">Перейдите в пункт **Параметры** > **Решения** и затем дважды щелкните **Измерения ценообразования \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="88399-116">Go to **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="88399-117">В обозревателе решений в левой навигационной панели выберите **Сущности**.</span><span class="sxs-lookup"><span data-stu-id="88399-117">In Solution Explorer, in the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="88399-118">Выберите **Создать** для создания новой сущности с названием **Стандартный заголовок**.</span><span class="sxs-lookup"><span data-stu-id="88399-118">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="88399-119">Введите остальные обязательные сведения, затем выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="88399-119">Enter the remaining required information, and then select **Save**.</span></span>

> ![Определение сущности стандартного заголовка](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a><span data-ttu-id="88399-121">Измерения на основе набора параметров</span><span class="sxs-lookup"><span data-stu-id="88399-121">Option set-based dimensions</span></span> 
<span data-ttu-id="88399-122">Можно создать два измерения на основе набора параметров.</span><span class="sxs-lookup"><span data-stu-id="88399-122">You can create two option set-based dimensions.</span></span> 

- <span data-ttu-id="88399-123">Использовать **Место работы ресурса** для отслеживания цены места работы **Дом** и работы **На месте**.</span><span class="sxs-lookup"><span data-stu-id="88399-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work.</span></span> 
- <span data-ttu-id="88399-124">Использовать **Рабочие часы ресурса** с значениями **Обычный** и **Сверхурочные** для применения наценки после завершения работы.</span><span class="sxs-lookup"><span data-stu-id="88399-124">Use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when the work is complete.</span></span>

<span data-ttu-id="88399-125">На следующем рисунке показано представление измерения **Место работы ресурса**.</span><span class="sxs-lookup"><span data-stu-id="88399-125">The following graphic provides a view of the **Resource Work Location** dimension.</span></span> 

> ![Измерение ценообразования на основе набора параметров под названием "Место работы ресурса"](media/Option-set-PD-called-Resource-Work-Location.png)

<span data-ttu-id="88399-127">На следующем рисунке показано представление измерения **Рабочие часы ресурса**.</span><span class="sxs-lookup"><span data-stu-id="88399-127">The following graphic provides a view of the **Resource Work Hours** dimension.</span></span> 

> ![Измерение ценообразования на основе набора параметров под названием "Рабочие часы ресурса"](media/Option-set-PD-called-Resource-Work-Hours.png)

1. <span data-ttu-id="88399-129">Перейдите в пункт **Параметры** > **Решения** и дважды щелкните **Измерения ценообразования \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="88399-129">Go to **Settings** > **Solutions**, and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="88399-130">В обозревателе решений в левой навигационной панели выберите **Наборы параметров**.</span><span class="sxs-lookup"><span data-stu-id="88399-130">In Solution Explorer, in the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="88399-131">Выберите **Создать** для создания нового набора параметров, введите остальное обязательные сведения, затем выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="88399-131">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="88399-132">Создание данные для измерений на основе сущности</span><span class="sxs-lookup"><span data-stu-id="88399-132">Create data for entity-based dimensions</span></span>

<span data-ttu-id="88399-133">Можно создавать данные для измерений на основе сущности вручную или с помощью импорта Microsoft Excel или служебных вызовов.</span><span class="sxs-lookup"><span data-stu-id="88399-133">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="88399-134">Используйте шаги в этой процедуре для создания двух стандартных заголовков, **Системный инженер** и **Главный системный инженер** из измерения на основе сущности, **Стандартный заголовок**.</span><span class="sxs-lookup"><span data-stu-id="88399-134">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="88399-135">Если данные, которые нужно создать, небольшие, как в следующем примере, можно использовать стандартную форму.</span><span class="sxs-lookup"><span data-stu-id="88399-135">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="88399-136">Выберите **Расширенный поиск**.</span><span class="sxs-lookup"><span data-stu-id="88399-136">Select **Advanced Find**.</span></span>
2. <span data-ttu-id="88399-137">Выделите сущность **Стандартный заголовок**, затем выберите **Результаты**.</span><span class="sxs-lookup"><span data-stu-id="88399-137">Select the entity **Standard Title**, and then select **Results**.</span></span> <span data-ttu-id="88399-138">Отображаются все строки в сущности **Стандартный заголовок**.</span><span class="sxs-lookup"><span data-stu-id="88399-138">All of the rows in the **Standard Title** entity will be shown.</span></span>
3. <span data-ttu-id="88399-139">Выберите **Создать** и в поле **Имя** введите "Системный инженер" и затем выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="88399-139">Select **New**, and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
4. <span data-ttu-id="88399-140">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="88399-140">Close the page.</span></span> 
5. <span data-ttu-id="88399-141">Повторите шаги с 1 по 3 для создания другого стандартного заголовка для "Главный системный инженер".</span><span class="sxs-lookup"><span data-stu-id="88399-141">Repeat steps 1-3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![Демонстрационные данные для сущности стандартного заголовка](media/ST-data.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]