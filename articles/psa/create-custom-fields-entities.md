---
title: Создание настраиваемых полей и сущностей
description: В этом разделе объясняется, как создавать наборы параметров и сущности в вашем собственном решении на платформе Power Apps.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 3d838bde8a3d7cbc15e06fb3289924468c284a8a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998967"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="39426-103">Создание настраиваемых полей и сущностей</span><span class="sxs-lookup"><span data-stu-id="39426-103">Create custom fields and entities</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="39426-104">Выполните следующие шаги в любое время, когда требуется создать настраиваемый набор параметров или сущность на платформе Power Apps.</span><span class="sxs-lookup"><span data-stu-id="39426-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="39426-105">Процедуры в данном разделе необходимо выполнить с помощью веб-интерфейса Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="39426-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="39426-106">Рекомендуется внести все изменения настраиваемых измерений ценообразования в отдельном решении.</span><span class="sxs-lookup"><span data-stu-id="39426-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="39426-107">Эта важная рекомендация гарантирует гибкость в будущем для обновления или удаления изменений по мере необходимости, поможет с повторным использованием вашей работы и упростит перенос этих изменений в другой экземпляр.</span><span class="sxs-lookup"><span data-stu-id="39426-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="39426-108">После внесения всех требуемых изменений экспортируйте это решение как **Управляемое решение** и импортируйте его в другие экземпляры, чтобы повторно использовать настройку ценообразования.</span><span class="sxs-lookup"><span data-stu-id="39426-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="39426-109">Создание настраиваемых полей и наборов параметров в решении измерений ценообразования</span><span class="sxs-lookup"><span data-stu-id="39426-109">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="39426-110">Изменение ценообразования может быть набором параметров или сущностью.</span><span class="sxs-lookup"><span data-stu-id="39426-110">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="39426-111">Оба необходимо создать в вашем решении ценообразования.</span><span class="sxs-lookup"><span data-stu-id="39426-111">Both must be created in your pricing solution.</span></span> <span data-ttu-id="39426-112">Шаги данной процедуры объясняют, как создавать измерения на основе сущности измерения на основе набора параметров.</span><span class="sxs-lookup"><span data-stu-id="39426-112">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="39426-113">Измерения на основе сущности</span><span class="sxs-lookup"><span data-stu-id="39426-113">Entity-based dimensions</span></span>

1. <span data-ttu-id="39426-114">В PSA щелкните **Параметры** > **Решения** и затем дважды щелкните **Измерения ценообразования \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="39426-114">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="39426-115">В обозревателе решений в левой навигационной панели выберите **Сущности**.</span><span class="sxs-lookup"><span data-stu-id="39426-115">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="39426-116">Щелкните **Создать** для создания новой сущности с названием **Стандартный заголовок**.</span><span class="sxs-lookup"><span data-stu-id="39426-116">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="39426-117">Введите остальные обязательные сведения, затем щелкните **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="39426-117">Enter the remaining required information, and then click **Save**.</span></span>

> ![Определение сущности стандартного заголовка](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="39426-119">Измерения на основе набора параметров</span><span class="sxs-lookup"><span data-stu-id="39426-119">Option set-based dimensions</span></span> 
<span data-ttu-id="39426-120">Можно создать два измерения на основе набора параметров.</span><span class="sxs-lookup"><span data-stu-id="39426-120">You can create two option set-based dimensions.</span></span> <span data-ttu-id="39426-121">Используйте **Место работы ресурса** для отслеживания цены места работы **Дом** и работы **На месте**, и используйте **Рабочие часы ресурса** со значениями **Обычные** и **Сверхурочные** для применения наценки после завершения работы.</span><span class="sxs-lookup"><span data-stu-id="39426-121">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="39426-122">В PSA щелкните **Параметры** > **Решения** и затем дважды щелкните **Измерения ценообразования \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="39426-122">In PSA, click **Settings** > **Solutions**, and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="39426-123">В обозревателе решений в левой навигационной панели выберите **Наборы параметров**.</span><span class="sxs-lookup"><span data-stu-id="39426-123">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="39426-124">Щелкните **Создать** для создания нового набора параметров, введите остальное обязательные сведения, затем нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="39426-124">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="39426-125">Измерение ценообразования на основе набора параметров под названием "Место работы ресурса"</span><span class="sxs-lookup"><span data-stu-id="39426-125">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="39426-126">Измерение ценообразования на основе набора параметров под названием "Рабочие часы ресурса"</span><span class="sxs-lookup"><span data-stu-id="39426-126">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="39426-127">Создание данные для измерений на основе сущности</span><span class="sxs-lookup"><span data-stu-id="39426-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="39426-128">Можно создавать данные для измерений на основе сущности вручную или с помощью импорта Microsoft Excel или служебных вызовов.</span><span class="sxs-lookup"><span data-stu-id="39426-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="39426-129">Используйте шаги в этой процедуре для создания двух стандартных заголовков, **Системный инженер** и **Главный системный инженер** из измерения на основе сущности, **Стандартный заголовок**.</span><span class="sxs-lookup"><span data-stu-id="39426-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="39426-130">Если данные, которые нужно создать, небольшие, как в следующем примере, можно использовать стандартную форму.</span><span class="sxs-lookup"><span data-stu-id="39426-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="39426-131">В PSA щелкните **Расширенный поиск**.</span><span class="sxs-lookup"><span data-stu-id="39426-131">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="39426-132">Выделите сущность **Стандартный заголовок**, затем щелкните **Результаты**.</span><span class="sxs-lookup"><span data-stu-id="39426-132">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="39426-133">Отображаются все строки в сущности **Стандартный заголовок**.</span><span class="sxs-lookup"><span data-stu-id="39426-133">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="39426-134">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="39426-134">Click **New**.</span></span> <span data-ttu-id="39426-135">В поле **Имя** введите "Системный инженер" и нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="39426-135">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="39426-136">Закройте форму.</span><span class="sxs-lookup"><span data-stu-id="39426-136">Close the form.</span></span> 
4. <span data-ttu-id="39426-137">Повторите шаги с 1 по 3 для создания другого стандартного заголовка для "Главный системный инженер".</span><span class="sxs-lookup"><span data-stu-id="39426-137">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="39426-138">Демонстрационные данные для сущности стандартного заголовка</span><span class="sxs-lookup"><span data-stu-id="39426-138">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]