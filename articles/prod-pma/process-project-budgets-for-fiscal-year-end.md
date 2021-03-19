---
title: Перенос бюджетов проектов в конце финансового года
description: В этой статье представлена информация о том, как перенести оставшиеся суммы бюджета на будущие годы и создать детали реестра бюджета.
author: Yowelle
manager: AnnBe
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 1f601be072e84fc04246cd55a260c8004f6fb3e5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289745"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a><span data-ttu-id="03b69-103">Перенос бюджетов проектов в конце финансового года</span><span class="sxs-lookup"><span data-stu-id="03b69-103">Transfer project budgets at fiscal year end</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="03b69-104">При работе над многолетним проектом у вас может остаться остаток бюджета на конец финансового года.</span><span class="sxs-lookup"><span data-stu-id="03b69-104">When working on a multi-year project, you might have remaining budget at the end of the fiscal year.</span></span> <span data-ttu-id="03b69-105">Вы можете перенести оставшиеся суммы бюджета на будущий год и создать детали регистра бюджета для сумм в связанных счетах главной книги.</span><span class="sxs-lookup"><span data-stu-id="03b69-105">You can transfer the remaining budget amounts to a future year, and create budget register details for the amounts in the associated general ledger accounts.</span></span> <span data-ttu-id="03b69-106">Прежде чем переносить оставшиеся суммы, просмотрите и проанализируйте оставшиеся суммы бюджета.</span><span class="sxs-lookup"><span data-stu-id="03b69-106">Before you carry forward the remaining amounts, review and analyze the remaining budget amounts.</span></span>

## <a name="review-and-analyze-remaining-budget-amounts"></a><span data-ttu-id="03b69-107">Просмотр и анализ оставшихся сумм бюджета</span><span class="sxs-lookup"><span data-stu-id="03b69-107">Review and analyze remaining budget amounts</span></span>

<span data-ttu-id="03b69-108">Выполните следующие шаги, чтобы просмотреть суммы бюджета проектов на конец года, но не переносить суммы на будущее.</span><span class="sxs-lookup"><span data-stu-id="03b69-108">Complete the following steps to review the year-end budget amounts for projects, but not carry the amounts forward.</span></span>

1. <span data-ttu-id="03b69-109">Перейдите в раздел **Управление и учет по проектам** > **Периодические операции** > **Бюджеты** > **Перенесенные бюджеты**.</span><span class="sxs-lookup"><span data-stu-id="03b69-109">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="03b69-110">На странице **Процесс переноса бюджета проекта** на вкладке **Варианты на конец года** убедитесь, что параметр **Перенести суммы остатков бюджета по проекту** не включен.</span><span class="sxs-lookup"><span data-stu-id="03b69-110">On the **Project budget carry-forward process** page, on the **Year-end options** tab, verify that **Carry forward remaining project budget amounts** is not enabled.</span></span>
3. <span data-ttu-id="03b69-111">На вкладке **Параметры** в поле **Год бюджета проекта** выберите финансовый год, для которого вы хотите просмотреть оставшуюся сумму бюджета.</span><span class="sxs-lookup"><span data-stu-id="03b69-111">On the **Parameters** tab, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
4. <span data-ttu-id="03b69-112">В поле **Открывающий финансовый год** выберите финансовый год, для которого вы хотите просмотреть оставшуюся сумму бюджета.</span><span class="sxs-lookup"><span data-stu-id="03b69-112">In the **Opening fiscal year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
5. <span data-ttu-id="03b69-113">В поле **Из модели прогноза** выберите **Остающийся бюджет**.</span><span class="sxs-lookup"><span data-stu-id="03b69-113">In the **From forecast model** field, select **Remaining budget**.</span></span> 
6. <span data-ttu-id="03b69-114">Чтобы включить проекты, соответствующие выбранным критериям и не имеющие остатка бюджета, выберите **Показать нулевые остатки**.</span><span class="sxs-lookup"><span data-stu-id="03b69-114">To include projects that meet your selected criteria and have no remaining budget, select **Show zero remaining**.</span></span>  
7. <span data-ttu-id="03b69-115">На вкладке **Выберите бюджеты** выберите **Получить все бюджеты**, чтобы загрузить все бюджеты, соответствующие выбранным критериям, затем выберите **Обработать**.</span><span class="sxs-lookup"><span data-stu-id="03b69-115">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match your selected criteria, and then select **Process**.</span></span> 
8. <span data-ttu-id="03b69-116">Чтобы создать запрос к базе данных, который загружает на панель определенный набор бюджетов, выберите **Получить выбранные бюджеты**.</span><span class="sxs-lookup"><span data-stu-id="03b69-116">To design a database query that loads a specific set of budgets into the pane, select **Retrieve selected budgets**.</span></span>

<span data-ttu-id="03b69-117">Для получения дополнительных сведений об определенной строке на панели выберите строку, затем выберите **Просмотр сведений бюджета** или **Просмотр счетов**.</span><span class="sxs-lookup"><span data-stu-id="03b69-117">For more information about a specific line in the pane, select the line, and then select **View budget details** or **View accounts**.</span></span>

## <a name="carry-forward-remaining-budget-amounts"></a><span data-ttu-id="03b69-118">Перенос оставшихся сумм бюджета</span><span class="sxs-lookup"><span data-stu-id="03b69-118">Carry forward remaining budget amounts</span></span> 

<span data-ttu-id="03b69-119">Когда вы обрабатываете оставшиеся суммы бюджета, вы можете создавать проводки в главной книге для сумм, которые вы переносите.</span><span class="sxs-lookup"><span data-stu-id="03b69-119">When you process remaining budget amounts, you can create transactions in the general ledger for the amounts that you are carrying forward.</span></span> <span data-ttu-id="03b69-120">Чтобы создать проводки в главной книге, выполните действия, описанные в разделе [Перенос сумм бюджета и создание проводок в главной книге](#carry-forward).</span><span class="sxs-lookup"><span data-stu-id="03b69-120">To create general ledger transactions, complete the steps in the section, [Carry forward budget amounts and create general ledger transactions](#carry-forward).</span></span> 

> [!NOTE]
> <span data-ttu-id="03b69-121">Переносимые суммы бюджета переносятся в модель прогноза, выбранную на странице **Модели прогнозов** в качестве модели прогноза переноса.</span><span class="sxs-lookup"><span data-stu-id="03b69-121">Budget amounts that are carried forward are transferred to the forecast model that is selected in the **Forecast models** page as the carry-forward forecast model.</span></span>  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a><span data-ttu-id="03b69-122">Перенос сумм бюджета и создание проводок главной книги</span><span class="sxs-lookup"><span data-stu-id="03b69-122">Carry forward budget amounts and create general ledger transactions</span></span>

1.  <span data-ttu-id="03b69-123">Выберите **Управление и учет по проектам** > **Периодические операции** > **Бюджеты** > **Перенесенные бюджеты**.</span><span class="sxs-lookup"><span data-stu-id="03b69-123">Select **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="03b69-124">На странице **Процесс переноса бюджета проекта** выберите **Конец года**, затем включите параметры **Перенести суммы остатков бюджета по проекту** и **Создать записи регистра бюджета в главной книге**.</span><span class="sxs-lookup"><span data-stu-id="03b69-124">On the **Project budget carry-forward process** page, select **Year-end**, and then enable **Carry forward remaining project budget amounts** and **Create budget register entries in general ledger**.</span></span> 
3. <span data-ttu-id="03b69-125">На вкладке **Параметры** в группе полей **Параметры проекта** выберите следующее:</span><span class="sxs-lookup"><span data-stu-id="03b69-125">On the **Parameters** tab, in the **Project parameters** field group, select the following:</span></span>

   - <span data-ttu-id="03b69-126">**Год бюджета проекта**: выберите начало финансового года, для которого вы хотите просмотреть оставшиеся суммы бюджета.</span><span class="sxs-lookup"><span data-stu-id="03b69-126">**Project budget year**: Select the beginning of the fiscal year for which you want to view the remaining budget amounts.</span></span> 
   - <span data-ttu-id="03b69-127">**Прибыли и убытки**: создайте проводки прибылей и убытков в главной книге.</span><span class="sxs-lookup"><span data-stu-id="03b69-127">**Profit and loss**: Create profit and loss transactions in the general ledger.</span></span> 
   -  <span data-ttu-id="03b69-128">**НЗП**: создайте проводки незавершенного производства (НЗП) в главной книге.</span><span class="sxs-lookup"><span data-stu-id="03b69-128">**WIP**: Create Work in Progress (WIP) transactions in the general ledger.</span></span>
   -  <span data-ttu-id="03b69-129">**Заработная плата**: создайте проводки распределения заработной платы в главной книге.</span><span class="sxs-lookup"><span data-stu-id="03b69-129">**Payroll**: Create payroll allocation transactions in the general ledger.</span></span> 

5. <span data-ttu-id="03b69-130">В группе полей **Главная книга** укажите следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="03b69-130">In the **General ledger** field group, provide the following information:</span></span> 

   - <span data-ttu-id="03b69-131">В поле **Открывающий финансовый год** выберите финансовый год, на который вы хотите перенести оставшиеся суммы бюджета для проектов.</span><span class="sxs-lookup"><span data-stu-id="03b69-131">In the **Opening fiscal year** field, select the fiscal year that you want to transfer remaining budget amounts to for the projects.</span></span> <span data-ttu-id="03b69-132">Значение по умолчанию — один год после значения в поле **Год бюджета проекта**.</span><span class="sxs-lookup"><span data-stu-id="03b69-132">The default value is one year after the value in the **Project budget year** field.</span></span>
   -  <span data-ttu-id="03b69-133">В поле **Период переноса** выберите период, для которого вы хотите создать сведения регистра бюджета в главной книге.</span><span class="sxs-lookup"><span data-stu-id="03b69-133">In the **Carry-forward period** field, select the period that you want to create the budget register details for in the general ledger.</span></span> <span data-ttu-id="03b69-134">Обычно это первый период в открывающемся финансовом году.</span><span class="sxs-lookup"><span data-stu-id="03b69-134">This is typically the first period in the opening fiscal year.</span></span>

6. <span data-ttu-id="03b69-135">В группе полей **Копировать из/в** укажите следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="03b69-135">In the **Copy from/to** field group, provide the following information:</span></span>

   - <span data-ttu-id="03b69-136">В поле **Из модели прогноза** выберите модель прогноза бюджета проекта, связанную с оставшимися суммами бюджета, которые вы хотите перенести для проектов.</span><span class="sxs-lookup"><span data-stu-id="03b69-136">In the **From forecast model** field, select the project budget forecast model associated with the remaining budget amounts you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="03b69-137">В поле **В модель бюджета ГК** выберите модель бюджета главной книги, связанную с оставшимися суммами бюджета, которые вы хотите перенести в главную книгу.</span><span class="sxs-lookup"><span data-stu-id="03b69-137">In the **To ledger budget model** field, select the ledger budget model associated with the budget amounts you want to transfer to the general ledger.</span></span> 
   -  <span data-ttu-id="03b69-138">Выберите **Перенос в валюте реализации**, чтобы использовать валюту продаж проекта для проводок главной книги, которые создаются при переносе сумм бюджета для проектов.</span><span class="sxs-lookup"><span data-stu-id="03b69-138">Select **Transfer sales currency** to use the project's sales currency for the general ledger transactions that are created when you transfer the budget amounts for the projects.</span></span> <span data-ttu-id="03b69-139">Если этот параметр не выбран, в проводках используется валюта учета.</span><span class="sxs-lookup"><span data-stu-id="03b69-139">When the option is not selected, the transactions use the accounting currency.</span></span> 
   -  <span data-ttu-id="03b69-140">Выберите **Показать нулевые остатки** для включения проектов, у которых нет остатков бюджета, но которые соответствуют другим критериям, выбранным вами в проектах, отображаемых на нижней панели.</span><span class="sxs-lookup"><span data-stu-id="03b69-140">Select **Show zero remaining** to include projects that have no remaining budget amounts, but meet the other criteria that you select in the projects displayed in the bottom pane.</span></span>

7. <span data-ttu-id="03b69-141">На вкладке **Выберите бюджеты** выберите **Получить все бюджеты**, чтобы загрузить все бюджеты, соответствующие выбранным критериям.</span><span class="sxs-lookup"><span data-stu-id="03b69-141">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match the criteria you selected.</span></span> <span data-ttu-id="03b69-142">Если вы предпочитаете создать запрос к базе данных, который загружает на панель определенный набор бюджетов проектов, выберите **Получить выбранные бюджеты**.</span><span class="sxs-lookup"><span data-stu-id="03b69-142">If you prefer to design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>
8. <span data-ttu-id="03b69-143">Для каждого проекта, который вы хотите обработать, выберите параметр в начале строки проекта.</span><span class="sxs-lookup"><span data-stu-id="03b69-143">For each project that you want to process, select the option at the beginning of the line for the project.</span></span>

    > [!TIP]
    > <span data-ttu-id="03b69-144">Чтобы выбрать все или большинство проектов, установите флажок в левом верхнем углу.</span><span class="sxs-lookup"><span data-stu-id="03b69-144">To select all or most of the projects, select the check mark in the top upper-left corner.</span></span> <span data-ttu-id="03b69-145">Чтобы исключить обработку какого-либо проекта, снимите флажок для этого проекта.</span><span class="sxs-lookup"><span data-stu-id="03b69-145">To exclude processing any project, clear the check mark for that project.</span></span>

9. <span data-ttu-id="03b69-146">Чтобы перенести оставшиеся суммы бюджета для выбранных проектов в выбранный финансовый год и создать детали регистра бюджета в главной книге, выберите **Обработать**.</span><span class="sxs-lookup"><span data-stu-id="03b69-146">To transfer the remaining budget amounts for the selected projects to the selected fiscal year and create budget register details in the general ledger, select **Process**.</span></span>

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a><span data-ttu-id="03b69-147">Перенос сумм бюджета без создания проводок главной книги</span><span class="sxs-lookup"><span data-stu-id="03b69-147">Carry forward budget amounts without creating general ledger transactions</span></span>

1. <span data-ttu-id="03b69-148">Перейдите в раздел **Управление и учет по проектам** > **Периодические операции** > **Бюджеты** > **Перенесенные бюджеты**.</span><span class="sxs-lookup"><span data-stu-id="03b69-148">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span>
2. <span data-ttu-id="03b69-149">На странице **Процесс переноса бюджета проекта** в поле **Варианты на конец года** выберите **Перенести суммы остатков бюджета по проекту**.</span><span class="sxs-lookup"><span data-stu-id="03b69-149">On the **Project budget carry-forward process** page, in the **Year-end options** field, select **Carry forward remaining project budget amounts**.</span></span>
3. <span data-ttu-id="03b69-150">В группе **Параметры** в поле **Год бюджета проекта** выберите финансовый год, для которого вы хотите просмотреть оставшийся бюджет.</span><span class="sxs-lookup"><span data-stu-id="03b69-150">In the **Parameters** group, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amounts.</span></span>
4. <span data-ttu-id="03b69-151">В группе **Копировать из/в** укажите следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="03b69-151">In the **Copy from/to** group, provide the following information:</span></span>

   - <span data-ttu-id="03b69-152">В поле **Из модели прогноза** выберите модель прогноза бюджета проекта, которая связана с оставшимися суммами бюджета, которые вы хотите перенести для проектов.</span><span class="sxs-lookup"><span data-stu-id="03b69-152">In the **From forecast model** field, select the project budget forecast model that is associated with the remaining budget amounts that you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="03b69-153">Выберите **Показать нулевые остатки**, чтобы включить проекты, не имеющие остатка бюджета, но соответствующие другим выбранным критериям.</span><span class="sxs-lookup"><span data-stu-id="03b69-153">Select **Show zero remaining** to include projects that have no remaining budget amounts, but that meet the other criteria you selected.</span></span>
   - <span data-ttu-id="03b69-154">В группе **Выберите бюджеты** выберите **Получить все бюджеты**, чтобы загрузить все бюджеты, соответствующие выбранным критериям.</span><span class="sxs-lookup"><span data-stu-id="03b69-154">In the **Select Budgets** group, select **Retrieve all budgets** to load all budgets that match the criteria that you selected.</span></span> <span data-ttu-id="03b69-155">Чтобы создать запрос к базе данных, который загружает на панель определенный набор бюджетов проектов, выберите **Получить выбранные бюджеты**.</span><span class="sxs-lookup"><span data-stu-id="03b69-155">To design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>

5. <span data-ttu-id="03b69-156">Для каждого проекта, который вы хотите обработать, выберите параметр в начале строки проекта.</span><span class="sxs-lookup"><span data-stu-id="03b69-156">For each project that you want to process, select the option at the beginning of the line for the project.</span></span> 
6. <span data-ttu-id="03b69-157">Выберите **Обработать** для переноса оставшихся сумм бюджета для выбранных проектов на выбранный финансовый год.</span><span class="sxs-lookup"><span data-stu-id="03b69-157">Select **Process** to transfer the remaining budget amounts for the selected projects to the selected fiscal year.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]