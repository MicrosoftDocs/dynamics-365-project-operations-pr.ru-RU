---
title: Создание решения для настраиваемых измерений ценообразования
description: В этом разделе представлена информация о том, как создавать решения для настраиваемых измерений цен.
author: Rumant
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3e3f688b0147974ef252a0ee00be20c4669d7165
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278434"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="28b28-103">Создание решения для настраиваемых измерений ценообразования</span><span class="sxs-lookup"><span data-stu-id="28b28-103">Create a solution for custom pricing dimensions</span></span>

 <span data-ttu-id="28b28-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="28b28-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span> 

>[!IMPORTANT]
><span data-ttu-id="28b28-105">Все изменения пользовательского измерения ценообразования должны быть в отдельном решении.</span><span class="sxs-lookup"><span data-stu-id="28b28-105">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="28b28-106">Эта важная рекомендация обеспечивает гибкость для обновления или удаления изменений по мере необходимости, помогает с повторным использованием вашей работы и упростит перенос этих изменений в другие экземпляры.</span><span class="sxs-lookup"><span data-stu-id="28b28-106">This important best practice allows the flexibility to update or remove changes as needed, helps with re-use of your work, and makes it easier to port changes to other instances.</span></span> <span data-ttu-id="28b28-107">После внесения всех требуемых изменений экспортируйте это решение как **Управляемое** решение и импортируйте его в другие экземпляры, чтобы повторно использовать.</span><span class="sxs-lookup"><span data-stu-id="28b28-107">After you make the required changes, export this solution as a **Managed** solution, and then import into other instances for reuse.</span></span>

## <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="28b28-108">Создание решения для настраиваемых измерений ценообразования</span><span class="sxs-lookup"><span data-stu-id="28b28-108">Create a solution for custom pricing dimensions</span></span>

1.  <span data-ttu-id="28b28-109">Выберите **Параметры** > **Решения**, затем выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="28b28-109">Select **Settings** > **Solutions**, and then select **New**.</span></span>
2.  <span data-ttu-id="28b28-110">Назовите решение, *<your organization name> измерения цен*.</span><span class="sxs-lookup"><span data-stu-id="28b28-110">Name the solution, *<your organization name> pricing dimensions*.</span></span>
3. <span data-ttu-id="28b28-111">Введите остальные обязательные сведения, затем выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="28b28-111">Enter the remaining required information, and then select **Save**.</span></span>

  ![Создание решения для настраиваемых измерений цен](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="28b28-113">Добавление всех требуемых сущностей и связанных компонентов в решение измерения ценообразования</span><span class="sxs-lookup"><span data-stu-id="28b28-113">Add all required entities and related components to the Pricing dimension solution</span></span>

<span data-ttu-id="28b28-114">Добавьте следующие сущности Project Service в свое решение ценообразования, чтобы внести важные изменения схемы в решение ценообразования.</span><span class="sxs-lookup"><span data-stu-id="28b28-114">Add the following Project Service entities to your pricing solution to make important schema changes in the pricing solution.</span></span> <span data-ttu-id="28b28-115">После того, как вы завершите эту процедуру, организации узнают новые измерения цен.</span><span class="sxs-lookup"><span data-stu-id="28b28-115">After you have completed this procedure, the entities will recognize the new pricing dimensions.</span></span>

1.  <span data-ttu-id="28b28-116">Выберите **Параметры** > **Решения**, затем дважды щелкните **<*имя организации*> измерения цен**.</span><span class="sxs-lookup"><span data-stu-id="28b28-116">Select **Settings** > **Solutions**, and then double-click **<*your organization name*> pricing dimensions**.</span></span>
2.  <span data-ttu-id="28b28-117">В обозревателе решений в левой навигационной панели выберите **Добавить существующий** > **Сущности**.</span><span class="sxs-lookup"><span data-stu-id="28b28-117">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3.  <span data-ttu-id="28b28-118">В диалоговом окне **Компоненты решения** выберите следующие сущности:</span><span class="sxs-lookup"><span data-stu-id="28b28-118">In the **Solution Components** dialog box, select the following entities:</span></span>
 
   - <span data-ttu-id="28b28-119">**Фактическая**</span><span class="sxs-lookup"><span data-stu-id="28b28-119">**Actual**</span></span>
   - <span data-ttu-id="28b28-120">**Резервируемый ресурс**</span><span class="sxs-lookup"><span data-stu-id="28b28-120">**Bookable Resource**</span></span>
   - <span data-ttu-id="28b28-121">**Строка оценки**</span><span class="sxs-lookup"><span data-stu-id="28b28-121">**Estimate Line**</span></span>
   - <span data-ttu-id="28b28-122">**Задача проекта**</span><span class="sxs-lookup"><span data-stu-id="28b28-122">**Project Task**</span></span>
   - <span data-ttu-id="28b28-123">**Сведения строки счета**</span><span class="sxs-lookup"><span data-stu-id="28b28-123">**Invoice Line Detail**</span></span>
   - <span data-ttu-id="28b28-124">**Строка журнала**</span><span class="sxs-lookup"><span data-stu-id="28b28-124">**Journal Line**</span></span>
   - <span data-ttu-id="28b28-125">**Сведения строки контракта проекта**</span><span class="sxs-lookup"><span data-stu-id="28b28-125">**Project Contract Line Detail**</span></span>
   - <span data-ttu-id="28b28-126">**Участник проектной группы**</span><span class="sxs-lookup"><span data-stu-id="28b28-126">**Project Team Member**</span></span>
   - <span data-ttu-id="28b28-127">**Сведения строки предложения с расценками**</span><span class="sxs-lookup"><span data-stu-id="28b28-127">**Quote Line Detail**</span></span>
   - <span data-ttu-id="28b28-128">**Наценка цены роли**</span><span class="sxs-lookup"><span data-stu-id="28b28-128">**Role Price Markup**</span></span>
   - <span data-ttu-id="28b28-129">**Цена роли**</span><span class="sxs-lookup"><span data-stu-id="28b28-129">**Role Price**</span></span>
   - <span data-ttu-id="28b28-130">**Запись времени**</span><span class="sxs-lookup"><span data-stu-id="28b28-130">**Time Entry**</span></span>
 
   ![Добавление существующих сущностей в решение для настраиваемых измерений цен](./media/Existing-entities-to-PD-solution.png)
 
 4. <span data-ttu-id="28b28-132">Для каждой сущности просмотрите добавляемые компоненты и окончательный список активов сущности для каждой сущности.</span><span class="sxs-lookup"><span data-stu-id="28b28-132">For each entity, review the components being added and the final list of entity assets for each entity.</span></span> 

   >[!NOTE]
   > <span data-ttu-id="28b28-133">Включите все формы и представления для каждой выбранной сущности.</span><span class="sxs-lookup"><span data-stu-id="28b28-133">Include all forms and views for each of the selected entities.</span></span>

  ![Сущности добавлены](./media/solution-component-selection.png)


5.  <span data-ttu-id="28b28-135">Когда будет предложено включить любые зависимые сущности для выбранных сущностей, выберите **Нет, не включать требуемые компоненты**.</span><span class="sxs-lookup"><span data-stu-id="28b28-135">When prompted to include any dependent entities for the selected entities, select **No, do not include required components.**</span></span>

    ![Включая зависимые сущности](./media/Do-not-include-required.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]