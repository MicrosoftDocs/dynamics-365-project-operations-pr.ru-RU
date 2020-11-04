---
title: Массовое исправление фактических данных, созданных утвержденными записями времени и расходов
description: В этой теме объясняется, как администратор может вносить одиночные или массовые исправления в ранее утвержденные записи времени или расходов, если выставление счетов не завершено.
author: rumant
manager: AnnBe
ms.date: 04/02/2020
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
search.app:
- ProjectOperations
ms.openlocfilehash: 6d6c03cc74d47ca3ae7c2bd7d0aa0720bb2f3c01
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083364"
---
# <a name="bulk-corrections-of-actuals-created-by-approved-time-and-expense-entries"></a><span data-ttu-id="1c383-103">Массовое исправление фактических данных, созданных утвержденными записями времени и расходов</span><span class="sxs-lookup"><span data-stu-id="1c383-103">Bulk corrections of actuals created by approved time and expense entries</span></span>

<span data-ttu-id="1c383-104">Иногда запись времени или расходов может быть введена неправильно.</span><span class="sxs-lookup"><span data-stu-id="1c383-104">Occasionally a time or expense entry may be entered incorrectly.</span></span> <span data-ttu-id="1c383-105">Например, консультант мог выбрать неправильную дату при создании записи времени или мог ошибочно поменять местами числа при вводе расходов.</span><span class="sxs-lookup"><span data-stu-id="1c383-105">For example, a consultant might select the wrong date when creating a time entry or they might transpose the numbers when entering an expense.</span></span> <span data-ttu-id="1c383-106">Если консультант не может сделать обновления отправленных записей, администратор может напрямую исправить запись для проекта.</span><span class="sxs-lookup"><span data-stu-id="1c383-106">If a consultant can’t make the updates to the submitted entries, an administrator can directly correct the entry for a project.</span></span>

<span data-ttu-id="1c383-107">Для выполнения процедур, описанных в этой теме, вам понадобятся разрешения администратора.</span><span class="sxs-lookup"><span data-stu-id="1c383-107">To complete the procedures in this topic, you will need Administrator permissions.</span></span>

## <a name="correct-approved-time-entries"></a><span data-ttu-id="1c383-108">Исправление утвержденных записей времени</span><span class="sxs-lookup"><span data-stu-id="1c383-108">Correct approved time entries</span></span>     

<span data-ttu-id="1c383-109">Выполните следующие шаги, чтобы исправить одну или несколько записей времени для проекта.</span><span class="sxs-lookup"><span data-stu-id="1c383-109">Complete the following steps to correct single or multiple time entries for a project.</span></span>

1. <span data-ttu-id="1c383-110">В области **Продажи** выберите **Проводки** , затем выберите **Утвержденное время**.</span><span class="sxs-lookup"><span data-stu-id="1c383-110">In the **Sales** area, select **Transactions** , and then select **Approved Time**.</span></span> 

2. <span data-ttu-id="1c383-111">В списке **Утвержденное время** найдите и выберите одну или несколько утвержденных записей времени для исправления.</span><span class="sxs-lookup"><span data-stu-id="1c383-111">In the **Approved Time** list, locate and select one or more approved time entries to correct.</span></span> <span data-ttu-id="1c383-112">Вы можете использовать фильтр для поиска связанных записей.</span><span class="sxs-lookup"><span data-stu-id="1c383-112">You can use the filter to locate related entries.</span></span> <span data-ttu-id="1c383-113">Например, вы можете отфильтровать по идентификатору проекта и выбрать все утвержденные записи времени с этим идентификатором проекта.</span><span class="sxs-lookup"><span data-stu-id="1c383-113">For example, you might filter on a Project ID, and select all approved time entries with that Project ID.</span></span>

3. <span data-ttu-id="1c383-114">Выберите **Исправить записи**.</span><span class="sxs-lookup"><span data-stu-id="1c383-114">Select **Correct entries**.</span></span> <span data-ttu-id="1c383-115">Новый журнал исправлений создается автоматически с назначенным типом **Корректировка времени**.</span><span class="sxs-lookup"><span data-stu-id="1c383-115">A new correction journal is automatically created, with the assigned type **Time correction**.</span></span> <span data-ttu-id="1c383-116">Выбранные вами записи будут добавлены в журнал.</span><span class="sxs-lookup"><span data-stu-id="1c383-116">The entries you selected are added to the journal.</span></span> 

4. <span data-ttu-id="1c383-117">На странице **Создать журнал** введите **Описание** для журнала корректировок, затем выберите вкладку **Корректировки записей времени**.</span><span class="sxs-lookup"><span data-stu-id="1c383-117">On the **New Journal** page, enter a **Description** for your correction journal, and then select the **Time Entry Corrections** tab.</span></span>  
5. <span data-ttu-id="1c383-118">В разделе **Новые значения для записей времени** обновите поля, введя требуемую правильную информацию.</span><span class="sxs-lookup"><span data-stu-id="1c383-118">In the **New Values for Time Entries** section, update the fields with the correct information as necessary.</span></span> <span data-ttu-id="1c383-119">Например, вы можете изменить назначенный проект или резервируемый ресурс.</span><span class="sxs-lookup"><span data-stu-id="1c383-119">For example, you can change the assigned project or the bookable resource.</span></span>

6. <span data-ttu-id="1c383-120">Выберите **Предварительный просмотр**.</span><span class="sxs-lookup"><span data-stu-id="1c383-120">Select **Preview**.</span></span> <span data-ttu-id="1c383-121">В диалоговом окне выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="1c383-121">In the dialog box, select **OK**.</span></span> <span data-ttu-id="1c383-122">На вкладке **Строки журнала** можно просмотреть список исходных фактических данных, связанных с выбранными записями времени, которые были сторнированы, и соответствующие исправленные строки, которые были созданы.</span><span class="sxs-lookup"><span data-stu-id="1c383-122">On the **Journal lines** tab, you can view a list of the original actuals that are related to the selected time entries that have been reversed and the corrected corresponding lines that have been created.</span></span> <span data-ttu-id="1c383-123">Если необходимо внести дополнительные исправления, повторите шаги 5 и 6.</span><span class="sxs-lookup"><span data-stu-id="1c383-123">If additional corrections need to be made, repeat steps 5 and 6.</span></span> 

> [!NOTE]
> <span data-ttu-id="1c383-124">Все исправленные фактические значения будут иметь те значения, которые вы выбрали в разделе **Новые значения для записей времени**.</span><span class="sxs-lookup"><span data-stu-id="1c383-124">All the corrected actuals will have the same values that you selected in the **New values for Time Entries** section.</span></span>

7. <span data-ttu-id="1c383-125">Если исправления отображаются так, как ожидается, выберите **Подтвердить**.</span><span class="sxs-lookup"><span data-stu-id="1c383-125">If the corrections appear as expected, select **Confirm**.</span></span> <span data-ttu-id="1c383-126">В диалоговом окне выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="1c383-126">In the dialog box, select **OK**.</span></span>

8. <span data-ttu-id="1c383-127">Вернитесь в область **Продажи** , выберите **Проекты** , затем откройте проект, для которого вы только что обновили записи времени.</span><span class="sxs-lookup"><span data-stu-id="1c383-127">Return to the **Sales** area, select **Projects** , and then open the project for which you just updated the time entries.</span></span> 

9. <span data-ttu-id="1c383-128">На странице **Проекта** , на вкладке **Фактические данные** просмотрите внесенные изменения.</span><span class="sxs-lookup"><span data-stu-id="1c383-128">On the **Projects** page, on the **Actuals** tab, view the changes that you made.</span></span> 

> [!NOTE]
> <span data-ttu-id="1c383-129">Если вкладка **Фактические данные** не видна, выберите **Связанные** > **Фактические данные**.</span><span class="sxs-lookup"><span data-stu-id="1c383-129">If the **Actuals** tab is not visible, select **Related** > **Actuals**.</span></span>  

10. <span data-ttu-id="1c383-130">В списке **Представление связанных фактических данных** можно увидеть, что исходные записи времени, которые были сторнированы, все еще указаны в списке, как и соответствующие исправленные записи времени.</span><span class="sxs-lookup"><span data-stu-id="1c383-130">In the **Actual Associated View** list, you can see that the original time entries that have been reversed are still listed, as are the corresponding corrected time entries.</span></span> 

<span data-ttu-id="1c383-131">Например, на следующем рисунке есть две номенклатуры строки с количеством 8,00, дебет которых перечислен в столбце "Сумма".</span><span class="sxs-lookup"><span data-stu-id="1c383-131">For example, in the following graphic, there are two line items with a quantity of 8.00 that have debits listed in the Amount column.</span></span> <span data-ttu-id="1c383-132">Кроме того, есть две номенклатуры строки с количеством –8,00, которые отображают суммы кредита в столбце "Сумма".</span><span class="sxs-lookup"><span data-stu-id="1c383-132">Additionally, there are two line items with a quantity of -8.00 that show credited amounts in the Amount column.</span></span> <span data-ttu-id="1c383-133">Эти коррекции сводят количество к нулю.</span><span class="sxs-lookup"><span data-stu-id="1c383-133">These corrections bring the quantity to zero.</span></span>

![Список связанного представления фактических данных](https://github.com/MicrosoftDocs/dynamics-365-customer-engagement-pr/blob/bulk-corrections-actuals-created-by-approved-time-expense-entries.md/time-actuals.png)
 
## <a name="correct-approved-expense-entries"></a><span data-ttu-id="1c383-135">Исправление утвержденных записей расходов</span><span class="sxs-lookup"><span data-stu-id="1c383-135">Correct approved expense entries</span></span>

<span data-ttu-id="1c383-136">Выполните следующие шаги, чтобы исправить одну или несколько записей расходов.</span><span class="sxs-lookup"><span data-stu-id="1c383-136">Complete the following steps to correct one or more expense entries.</span></span> 

1. <span data-ttu-id="1c383-137">В области **Продажи** в левой панели навигации в пункте **Проводки** выберите **Утвержденные расходы**.</span><span class="sxs-lookup"><span data-stu-id="1c383-137">In the **Sales** area, in the left navigation pane, under **Transactions** , select **Approved Expenses**.</span></span>

2. <span data-ttu-id="1c383-138">В списке **Утвержденные расходы** выберите проект, который вы хотите исправить, затем выберите **Исправить записи**.</span><span class="sxs-lookup"><span data-stu-id="1c383-138">In the **Approved Expenses** list, select the project that you want to correct, and then select **Correct entries**.</span></span> <span data-ttu-id="1c383-139">Новый журнал исправлений будет создан автоматически с назначенным типом **Корректировка расходов**.</span><span class="sxs-lookup"><span data-stu-id="1c383-139">A new correction journal will be created automatically with the assigned type of **Expense correction**.</span></span> 

3. <span data-ttu-id="1c383-140">На странице **Создать журнал** введите **Описание** для исправления, и на вкладке **Корректировка расходов** в разделе **Новые значения для расходов** выберите поля данных, которые вы хотите исправить для выбранных строк расходов.</span><span class="sxs-lookup"><span data-stu-id="1c383-140">On the **New Journal** page, enter a **Description** for the correction, and on the **Expense Correction** tab, in the **New Values for Expenses** section, select the data fields that you want to correct for the selected expense lines.</span></span> <span data-ttu-id="1c383-141">Например, вы можете назначить расходы другому **Проекту** или исправить поля **Категория расходов** , **Дата расхода** или **Резервируемый ресурс**.</span><span class="sxs-lookup"><span data-stu-id="1c383-141">For example, you can assign the expense to another **Project** , or correct the **Expense Category** , **Expense Date** , or **Bookable Resource**.</span></span>

4. <span data-ttu-id="1c383-142">Выберите **Предварительный просмотр**.</span><span class="sxs-lookup"><span data-stu-id="1c383-142">Select **Preview**.</span></span> <span data-ttu-id="1c383-143">В диалоговом окне выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="1c383-143">In the dialog box, select **OK**.</span></span> 

5. <span data-ttu-id="1c383-144">Проверьте корректировки на вкладке **Строки журнала**. Можно просмотреть список исходных фактических данных, связанных с выбранными записями расходов, которые были сторнированы, и соответствующие исправленные строки, которые были созданы.</span><span class="sxs-lookup"><span data-stu-id="1c383-144">Verify the corrections on the **Journal lines** tab. You can view a list of the original actuals that are related to the selected expense entries that have been reversed and the corrected corresponding lines that have been created.</span></span>

6. <span data-ttu-id="1c383-145">Если исправленные значения отображаются так, как ожидается, выберите **Подтвердить**.</span><span class="sxs-lookup"><span data-stu-id="1c383-145">If the corrected values are as expected, select **Confirm**.</span></span> <span data-ttu-id="1c383-146">В диалоговом окне выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="1c383-146">In the dialog box, select **OK.**</span></span> <span data-ttu-id="1c383-147">Если значения не отображаются должным образом, выберите **Отмена** , чтобы вернуться к списку **Утвержденные расходы**.</span><span class="sxs-lookup"><span data-stu-id="1c383-147">If the values are not showing as expected, select **Cancel** to return to the **Approved Expenses** list.</span></span> <span data-ttu-id="1c383-148">Повторите шаги со 2 по 5.</span><span class="sxs-lookup"><span data-stu-id="1c383-148">Repeat steps 2 through 5.</span></span> 

> [!NOTE]
> <span data-ttu-id="1c383-149">Исправленные фактические значения будут иметь те значения, которые вы выбрали в разделе **Новые значения для расходов**.</span><span class="sxs-lookup"><span data-stu-id="1c383-149">The corrected actuals will have the same values that you selected in the **New values for Expenses** section.</span></span>

7. <span data-ttu-id="1c383-150">После проверки журнала корректировок вернитесь к проекту или проектам, которые вы обновили, чтобы просмотреть изменения.</span><span class="sxs-lookup"><span data-stu-id="1c383-150">After you confirm the correction journal, navigate back to the project or projects that you updated, to view your changes.</span></span>  

8. <span data-ttu-id="1c383-151">На странице проекта на вкладке **Фактические значения** просмотрите **Представление связанных фактических данных**.</span><span class="sxs-lookup"><span data-stu-id="1c383-151">In the project page, on the **Actuals** tab, review the **Actual Associated View**.</span></span> <span data-ttu-id="1c383-152">Исходные записи и исправленные записи перечислены.</span><span class="sxs-lookup"><span data-stu-id="1c383-152">The original entries and the corrected entries are listed.</span></span> <span data-ttu-id="1c383-153">На следующем рисунке показаны исходные суммы записей расходов и соответствующие исправленные суммы записей расходов.</span><span class="sxs-lookup"><span data-stu-id="1c383-153">The following graphic shows original expense entry amounts and the corresponding corrected expense entry amounts.</span></span> 

![Фактические данные расходов](https://user-images.githubusercontent.com/60806505/77122219-4cd52900-69fa-11ea-8349-ccd2ffebf640.png)
