---
title: Создание и подтверждение журналов корректировок
description: В этом разделе представлена информация о том, как создать и подтвердить журнал корректировок.
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
ms.openlocfilehash: 274f99527804b0db81b26201a22eb5a8cbe86c9a
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896972"
---
# <a name="create-and-confirm-correction-journals"></a><span data-ttu-id="e5f0f-103">Создание и подтверждение журналов корректировок</span><span class="sxs-lookup"><span data-stu-id="e5f0f-103">Create and confirm Correction journals</span></span>

<span data-ttu-id="e5f0f-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="e5f0f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e5f0f-105">Иногда запись времени или расходов может быть введена неправильно.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-105">Occasionally a time or expense entry may be entered incorrectly.</span></span> <span data-ttu-id="e5f0f-106">Например, консультант мог выбрать неправильную дату при создании записи времени или мог ошибочно поменять местами числа при вводе расходов.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-106">For example, a consultant might select the wrong date when creating a time entry or they might transpose the numbers when entering an expense.</span></span> <span data-ttu-id="e5f0f-107">Если консультант не может сделать обновления отправленных записей, администратор может напрямую исправить запись для проекта.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-107">If a consultant can’t make the updates to the submitted entries, an administrator can directly correct the entry for a project.</span></span>

<span data-ttu-id="e5f0f-108">Для выполнения процедур, описанных в этой теме, вам понадобятся разрешения администратора.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-108">To complete the procedures in this topic, you will need Administrator permissions.</span></span>

## <a name="correct-approved-time-entries"></a><span data-ttu-id="e5f0f-109">Исправление утвержденных записей времени</span><span class="sxs-lookup"><span data-stu-id="e5f0f-109">Correct approved time entries</span></span>     

<span data-ttu-id="e5f0f-110">Выполните следующие шаги, чтобы исправить одну или несколько записей времени для проекта.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-110">Complete the following steps to correct single or multiple time entries for a project.</span></span>

1. <span data-ttu-id="e5f0f-111">В области **Продажи** выберите **Проводки**, затем выберите **Утвержденное время**.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-111">In the **Sales** area, select **Transactions**, and then select **Approved Time**.</span></span> 

2. <span data-ttu-id="e5f0f-112">В списке **Утвержденное время** найдите и выберите одну или несколько утвержденных записей времени для исправления.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-112">In the **Approved Time** list, locate and select one or more approved time entries to correct.</span></span> <span data-ttu-id="e5f0f-113">Вы можете использовать фильтр для поиска связанных записей.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-113">You can use the filter to locate related entries.</span></span> <span data-ttu-id="e5f0f-114">Например, вы можете отфильтровать по идентификатору проекта и выбрать все утвержденные записи времени с этим идентификатором проекта.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-114">For example, you might filter on a Project ID, and select all approved time entries with that Project ID.</span></span>

3. <span data-ttu-id="e5f0f-115">Выберите **Исправить записи**.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-115">Select **Correct entries**.</span></span> <span data-ttu-id="e5f0f-116">Новый журнал исправлений создается автоматически с назначенным типом **Корректировка времени**.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-116">A new correction journal is automatically created, with the assigned type **Time correction**.</span></span> <span data-ttu-id="e5f0f-117">Выбранные вами записи будут добавлены в журнал.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-117">The entries you selected are added to the journal.</span></span> 

4. <span data-ttu-id="e5f0f-118">На странице **Создать журнал** введите **Описание** для журнала корректировок, затем выберите вкладку **Корректировки записей времени**.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-118">On the **New Journal** page, enter a **Description** for your correction journal, and then select the **Time Entry Corrections** tab.</span></span>  

5. <span data-ttu-id="e5f0f-119">В разделе **Новые значения для записей времени** обновите поля, введя требуемую правильную информацию.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-119">In the **New Values for Time Entries** section, update the fields with the correct information as necessary.</span></span> <span data-ttu-id="e5f0f-120">Например, вы можете изменить назначенный проект или резервируемый ресурс.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-120">For example, you can change the assigned project or the bookable resource.</span></span>

6. <span data-ttu-id="e5f0f-121">Выберите **Предварительный просмотр**.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-121">Select **Preview**.</span></span> <span data-ttu-id="e5f0f-122">В диалоговом окне выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-122">In the dialog box, select **OK**.</span></span> <span data-ttu-id="e5f0f-123">На вкладке **Строки журнала** можно просмотреть список исходных фактических данных, связанных с выбранными записями времени, которые были сторнированы, и соответствующие исправленные строки, которые были созданы.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-123">On the **Journal lines** tab, you can view a list of the original actuals that are related to the selected time entries that have been reversed and the corrected corresponding lines that have been created.</span></span> <span data-ttu-id="e5f0f-124">Если необходимо внести дополнительные исправления, повторите шаги 5 и 6.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-124">If additional corrections need to be made, repeat steps 5 and 6.</span></span> 

> [!NOTE]
> <span data-ttu-id="e5f0f-125">Все исправленные фактические значения будут иметь те значения, которые вы выбрали в разделе **Новые значения для записей времени**.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-125">All the corrected actuals will have the same values that you selected in the **New values for Time Entries** section.</span></span>

7. <span data-ttu-id="e5f0f-126">Если исправления отображаются так, как ожидается, выберите **Подтвердить**.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-126">If the corrections appear as expected, select **Confirm**.</span></span> <span data-ttu-id="e5f0f-127">В диалоговом окне выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-127">In the dialog box, select **OK**.</span></span>

8. <span data-ttu-id="e5f0f-128">Вернитесь в область **Продажи**, выберите **Проекты**, затем откройте проект, для которого вы только что обновили записи времени.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-128">Return to the **Sales** area, select **Projects**, and then open the project for which you just updated the time entries.</span></span> 

9. <span data-ttu-id="e5f0f-129">На странице **Проекта**, на вкладке **Фактические данные** просмотрите внесенные изменения.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-129">On the **Projects** page, on the **Actuals** tab, view the changes that you made.</span></span> 

> [!NOTE]
> <span data-ttu-id="e5f0f-130">Если вкладка **Фактические данные** не видна, выберите **Связанные** > **Фактические данные**.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-130">If the **Actuals** tab is not visible, select **Related** > **Actuals**.</span></span>  

10. <span data-ttu-id="e5f0f-131">В списке **Представление связанных фактических данных** можно увидеть, что исходные записи времени, которые были сторнированы, все еще указаны в списке, как и соответствующие исправленные записи времени.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-131">In the **Actual Associated View** list, you can see that the original time entries that have been reversed are still listed, as are the corresponding corrected time entries.</span></span> 

<span data-ttu-id="e5f0f-132">Например, на следующем рисунке есть две номенклатуры строки с количеством 8,00, дебет которых перечислен в столбце "Сумма".</span><span class="sxs-lookup"><span data-stu-id="e5f0f-132">For example, in the following graphic, there are two line items with a quantity of 8.00 that have debits listed in the Amount column.</span></span> <span data-ttu-id="e5f0f-133">Кроме того, есть две номенклатуры строки с количеством –8,00, которые отображают суммы кредита в столбце "Сумма".</span><span class="sxs-lookup"><span data-stu-id="e5f0f-133">Additionally, there are two line items with a quantity of -8.00 that show credited amounts in the Amount column.</span></span> <span data-ttu-id="e5f0f-134">Эти коррекции сводят количество к нулю.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-134">These corrections bring the quantity to zero.</span></span>

 
## <a name="correct-approved-expense-entries"></a><span data-ttu-id="e5f0f-135">Исправление утвержденных записей расходов</span><span class="sxs-lookup"><span data-stu-id="e5f0f-135">Correct approved expense entries</span></span>

<span data-ttu-id="e5f0f-136">Выполните следующие шаги, чтобы исправить одну или несколько записей расходов.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-136">Complete the following steps to correct one or more expense entries.</span></span> 

1. <span data-ttu-id="e5f0f-137">В области **Продажи** в левой панели навигации в пункте **Проводки** выберите **Утвержденные расходы**.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-137">In the **Sales** area, in the left navigation pane, under **Transactions**, select **Approved Expenses**.</span></span>

2. <span data-ttu-id="e5f0f-138">В списке **Утвержденные расходы** выберите проект, который вы хотите исправить, затем выберите **Исправить записи**.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-138">In the **Approved Expenses** list, select the project that you want to correct, and then select **Correct entries**.</span></span> <span data-ttu-id="e5f0f-139">Новый журнал исправлений будет создан автоматически с назначенным типом **Корректировка расходов**.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-139">A new correction journal will be created automatically with the assigned type of **Expense correction**.</span></span> 

3. <span data-ttu-id="e5f0f-140">На странице **Создать журнал** введите **Описание** для исправления, и на вкладке **Корректировка расходов** в разделе **Новые значения для расходов** выберите поля данных, которые вы хотите исправить для выбранных строк расходов.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-140">On the **New Journal** page, enter a **Description** for the correction, and on the **Expense Correction** tab, in the **New Values for Expenses** section, select the data fields that you want to correct for the selected expense lines.</span></span> <span data-ttu-id="e5f0f-141">Например, вы можете назначить расходы другому **Проекту** или исправить поля **Категория расходов**, **Дата расхода** или **Резервируемый ресурс**.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-141">For example, you can assign the expense to another **Project**, or correct the **Expense Category**, **Expense Date**, or **Bookable Resource**.</span></span>

4. <span data-ttu-id="e5f0f-142">Выберите **Предварительный просмотр**.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-142">Select **Preview**.</span></span> <span data-ttu-id="e5f0f-143">В диалоговом окне выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-143">In the dialog box, select **OK**.</span></span> 

5. <span data-ttu-id="e5f0f-144">Проверьте корректировки на вкладке **Строки журнала**. Можно просмотреть список исходных фактических данных, связанных с выбранными записями расходов, которые были сторнированы, и соответствующие исправленные строки, которые были созданы.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-144">Verify the corrections on the **Journal lines** tab. You can view a list of the original actuals that are related to the selected expense entries that have been reversed and the corrected corresponding lines that have been created.</span></span>

6. <span data-ttu-id="e5f0f-145">Если исправленные значения отображаются так, как ожидается, выберите **Подтвердить**.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-145">If the corrected values are as expected, select **Confirm**.</span></span> <span data-ttu-id="e5f0f-146">В диалоговом окне выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-146">In the dialog box, select **OK.**</span></span> <span data-ttu-id="e5f0f-147">Если значения не отображаются должным образом, выберите **Отмена**, чтобы вернуться к списку **Утвержденные расходы**.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-147">If the values are not showing as expected, select **Cancel** to return to the **Approved Expenses** list.</span></span> <span data-ttu-id="e5f0f-148">Повторите шаги со 2 по 5.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-148">Repeat steps 2 through 5.</span></span> 

> [!NOTE]
> <span data-ttu-id="e5f0f-149">Исправленные фактические значения будут иметь те значения, которые вы выбрали в разделе **Новые значения для расходов**.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-149">The corrected actuals will have the same values that you selected in the **New values for Expenses** section.</span></span>

7. <span data-ttu-id="e5f0f-150">После проверки журнала корректировок вернитесь к проекту или проектам, которые вы обновили, чтобы просмотреть изменения.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-150">After you confirm the correction journal, navigate back to the project or projects that you updated, to view your changes.</span></span>  

8. <span data-ttu-id="e5f0f-151">На странице проекта на вкладке **Фактические значения** просмотрите **Представление связанных фактических данных**.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-151">In the project page, on the **Actuals** tab, review the **Actual Associated View**.</span></span> <span data-ttu-id="e5f0f-152">Исходные записи и исправленные записи перечислены.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-152">The original entries and the corrected entries are listed.</span></span> <span data-ttu-id="e5f0f-153">На следующем рисунке показаны исходные суммы записей расходов и соответствующие исправленные суммы записей расходов.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-153">The following graphic shows original expense entry amounts and the corresponding corrected expense entry amounts.</span></span> 


