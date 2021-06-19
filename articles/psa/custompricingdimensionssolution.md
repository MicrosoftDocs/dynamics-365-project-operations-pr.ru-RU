---
title: Создание настраиваемых решений для измерений ценообразования
description: В этой теме объясняется, как создать настраиваемое решение при создании пользовательских измерений ценообразования.
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
ms.openlocfilehash: ae7f22b9cb092e956d0f1eaf1f1997c8e97392f4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012332"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a><span data-ttu-id="506f4-103">Создание настраиваемых решений для измерений ценообразования</span><span class="sxs-lookup"><span data-stu-id="506f4-103">Create custom solutions for pricing dimensions</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

> [!IMPORTANT]
> <span data-ttu-id="506f4-104">Все изменения пользовательского измерения ценообразования должны быть в отдельном решении.</span><span class="sxs-lookup"><span data-stu-id="506f4-104">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="506f4-105">Эта важная рекомендация гарантирует гибкость в будущем для обновления или удаления изменений по мере необходимости, поможет с повторным использованием вашей работы и упростит перенос этих изменений в другой экземпляр.</span><span class="sxs-lookup"><span data-stu-id="506f4-105">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="506f4-106">После внесения всех требуемых изменений экспортируйте это решение как **Управляемое решение** и импортируйте его в другие экземпляры, чтобы повторно использовать настройку ценообразования.</span><span class="sxs-lookup"><span data-stu-id="506f4-106">After you make the required changes, export this solution as a **Managed solution**, and import it into other instances to reuse your pricing setup.</span></span>

1. <span data-ttu-id="506f4-107">Выберите **Параметры** > **Решения**, затем выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="506f4-107">Select **Settings** > **Solutions**, and then select **New**.</span></span> 
2. <span data-ttu-id="506f4-108">Назовите решение, **Измерения ценообразования \<your organization name>**, введите остальные необходимые сведения, затем выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="506f4-108">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then select **Save**.</span></span>

> ![Создание настраиваемого решения для измерений ценообразования](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="506f4-110">Добавление всех требуемых сущностей и связанных компонентов в решение измерения ценообразования</span><span class="sxs-lookup"><span data-stu-id="506f4-110">Add all required entities and related components to the Pricing dimension solution</span></span>
<span data-ttu-id="506f4-111">Необходимо добавить следующие сущности Project Service в ваше решение ценообразования.</span><span class="sxs-lookup"><span data-stu-id="506f4-111">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="506f4-112">Выполните шаги в этой процедуре, чтобы выполнить некоторые важные изменения схемы в решении ценообразования, чтобы сущности знали о новых измерениях ценообразования.</span><span class="sxs-lookup"><span data-stu-id="506f4-112">Complete the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="506f4-113">Выберите **Параметры** > **Решения** и затем дважды щелкните **Измерения ценообразования \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="506f4-113">Select **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="506f4-114">В обозревателе решений в левой навигационной панели выберите **Добавить существующий** > **Сущности**.</span><span class="sxs-lookup"><span data-stu-id="506f4-114">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="506f4-115">В диалоговом окне **Компоненты решения** выберите следующие сущности:</span><span class="sxs-lookup"><span data-stu-id="506f4-115">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="506f4-116">Фактическая</span><span class="sxs-lookup"><span data-stu-id="506f4-116">Actual</span></span>
- <span data-ttu-id="506f4-117">Резервируемый ресурс</span><span class="sxs-lookup"><span data-stu-id="506f4-117">Bookable Resource</span></span>
- <span data-ttu-id="506f4-118">Строка оценки</span><span class="sxs-lookup"><span data-stu-id="506f4-118">Estimate Line</span></span>
- <span data-ttu-id="506f4-119">Задача проекта</span><span class="sxs-lookup"><span data-stu-id="506f4-119">Project Task</span></span>
- <span data-ttu-id="506f4-120">Сведения строки счета</span><span class="sxs-lookup"><span data-stu-id="506f4-120">Invoice Line Detail</span></span>
- <span data-ttu-id="506f4-121">Строка журнала</span><span class="sxs-lookup"><span data-stu-id="506f4-121">Journal Line</span></span>
- <span data-ttu-id="506f4-122">Сведения строки контракта проекта</span><span class="sxs-lookup"><span data-stu-id="506f4-122">Project Contract Line Detail</span></span>
- <span data-ttu-id="506f4-123">Участник проектной группы</span><span class="sxs-lookup"><span data-stu-id="506f4-123">Project Team Member</span></span>
- <span data-ttu-id="506f4-124">Сведения строки предложения с расценками</span><span class="sxs-lookup"><span data-stu-id="506f4-124">Quote Line Detail</span></span>
- <span data-ttu-id="506f4-125">Наценка цены роли</span><span class="sxs-lookup"><span data-stu-id="506f4-125">Role Price Markup</span></span>
- <span data-ttu-id="506f4-126">Цена роли</span><span class="sxs-lookup"><span data-stu-id="506f4-126">Role Price</span></span> 
- <span data-ttu-id="506f4-127">Запись времени</span><span class="sxs-lookup"><span data-stu-id="506f4-127">Time Entry</span></span> 

> ![Добавление существующих сущностей в решение измерения ценообразования](media/Existing-entities-to-PD-solution.png)

> ![Выберите компоненты решения](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="506f4-130">Обязательно включите все формы и представления для каждой выбранной сущности.</span><span class="sxs-lookup"><span data-stu-id="506f4-130">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="506f4-131">При появлении запроса на включение всех зависимых сущностей для выбранных сущностей выберите **Нет**.</span><span class="sxs-lookup"><span data-stu-id="506f4-131">When prompted to include any dependent entities for the selected entities, select **No**.</span></span>

> ![Не включайте все связанные компоненты](media/Do-not-include-required.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]