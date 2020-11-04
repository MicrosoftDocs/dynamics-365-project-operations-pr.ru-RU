---
title: Создание расширенных контрактов для выставления счетов на основе хода выполнения
description: В этой теме объясняется, как создавать контракты по проекту, чтобы вы могли создавать счета для клиентов на основе процента выполненных работ.
author: RadhikaRS
manager: AnnBe
ms.date: 03/26/2020
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
ms.openlocfilehash: 1a83785a9db4dffc4585acf11ef971c08594f312
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083317"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a><span data-ttu-id="49d19-103">Создание расширенных контрактов для выставления счетов на основе хода выполнения</span><span class="sxs-lookup"><span data-stu-id="49d19-103">Create advanced contracts for billing based on progress</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="49d19-104">В этой теме объясняется, как создавать контракты по проекту, чтобы вы могли создавать счета для клиентов на основе процента выполненных работ.</span><span class="sxs-lookup"><span data-stu-id="49d19-104">This topic explains how to create project contracts so that you can create invoices for customers, based on a percentage of completed work.</span></span> <span data-ttu-id="49d19-105">Суммы счетов автоматически рассчитываются для бюджетных категорий работ, которые вы настроили для проекта.</span><span class="sxs-lookup"><span data-stu-id="49d19-105">Invoice amounts are automatically calculated for the budget categories of work that you set up for a project.</span></span> <span data-ttu-id="49d19-106">Сроки выставления счета устанавливаются при согласовании контракта по проекту с клиентом.</span><span class="sxs-lookup"><span data-stu-id="49d19-106">The invoice timing is set when you negotiate the project contract with the customer.</span></span>

<span data-ttu-id="49d19-107">Используйте процедуры, описанные в этой теме, чтобы настроить контракт, связанный проект и правила выставления счетов, которые вычисляют суммы счетов для бюджетных категорий работ, которые вы настроили для проекта.</span><span class="sxs-lookup"><span data-stu-id="49d19-107">Use the procedures in this topic to set up a contract, an associated project, and the billing rules that calculate invoice amounts for the budget categories of work that you set up for the project.</span></span>

<span data-ttu-id="49d19-108">После того как вы создали контракт и проект, вы можете настроить детали проекта.</span><span class="sxs-lookup"><span data-stu-id="49d19-108">After you've created the contract and the project, you can set up the details of the project.</span></span> <span data-ttu-id="49d19-109">Например, вы можете определить действия и назначить работников для проекта.</span><span class="sxs-lookup"><span data-stu-id="49d19-109">For example, you can define activities and assign workers to the project.</span></span>

## <a name="example"></a><span data-ttu-id="49d19-110">Пример</span><span class="sxs-lookup"><span data-stu-id="49d19-110">Example</span></span>

<span data-ttu-id="49d19-111">Ваша организация занимается разработкой программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="49d19-111">Your organization is a software development firm.</span></span> <span data-ttu-id="49d19-112">Вы соглашаетесь разработать пакет расчета заработной платы для клиента за общую плату в 20 000 долларов США (USD).</span><span class="sxs-lookup"><span data-stu-id="49d19-112">You agree to develop a payroll accounting package for a customer for a total fee of 20,000 US dollars (USD).</span></span> <span data-ttu-id="49d19-113">Ваша организация соглашается выставлять заказчику счета по мере выполнения вами определенных процентов проекта.</span><span class="sxs-lookup"><span data-stu-id="49d19-113">Your organization agrees to invoice the customer as you complete specific percentages of the project.</span></span> <span data-ttu-id="49d19-114">Вы настраиваете следующие категории проекта для работы, чтобы использовать их в процессе выставления счетов:</span><span class="sxs-lookup"><span data-stu-id="49d19-114">You set up the following project categories for the work, so that you can use them in the billing process:</span></span>

- <span data-ttu-id="49d19-115">Консалтинг</span><span class="sxs-lookup"><span data-stu-id="49d19-115">Consulting</span></span>
- <span data-ttu-id="49d19-116">Проектирование</span><span class="sxs-lookup"><span data-stu-id="49d19-116">Design</span></span>
- <span data-ttu-id="49d19-117">Установка</span><span class="sxs-lookup"><span data-stu-id="49d19-117">Installation</span></span>

<span data-ttu-id="49d19-118">Вы также устанавливаете правила выставления счетов, которые автоматически рассчитывают суммы счетов для процента работы по проекту, выполненной в каждой категории.</span><span class="sxs-lookup"><span data-stu-id="49d19-118">You also set up billing rules that automatically calculate the invoice amounts for the percentage of project work that is completed in each category.</span></span>

<span data-ttu-id="49d19-119">Менеджер бюджета создает бюджет для категорий проекта.</span><span class="sxs-lookup"><span data-stu-id="49d19-119">The budget manager creates a budget for the project categories.</span></span> <span data-ttu-id="49d19-120">Объем выполненных работ автоматически рассчитывается как процент от фактических работ по сравнению с заложенными в бюджет суммами.</span><span class="sxs-lookup"><span data-stu-id="49d19-120">The amount of completed work is automatically calculated as a percentage of actual work in comparison to the budgeted amounts.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="49d19-121">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="49d19-121">Prerequisites</span></span>

<span data-ttu-id="49d19-122">Перед созданием проекта, в котором используются правила выставления счетов, необходимо настроить номерные серии для правил выставления счетов и журнал сборов, который используется для разноски счетов, выставляемых на основе хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="49d19-122">Before you create a project that uses billing rules, you must set up the number sequences for billing rules and a fee journal that is used to post progress billings.</span></span>

1. <span data-ttu-id="49d19-123">Перейдите в раздел **Управление и учет по проектам** \> **Настройка** \> **Параметры модуля "Управление и учет по проектам"**.</span><span class="sxs-lookup"><span data-stu-id="49d19-123">Go to **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>
2. <span data-ttu-id="49d19-124">На странице **Параметры модуля "Управление и учет по проектам"** на вкладке **Номерные серии** настройте номерную серию, которую вы хотите использовать при создании правил выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="49d19-124">On the **Project management and accounting parameters** page, on the **Number sequences** tab, set up the number sequence that you want to use when billing rules are created.</span></span>
3. <span data-ttu-id="49d19-125">Перейдите в раздел **Управление и учет по проектам** \> **Журналы** \> **Сбор**.</span><span class="sxs-lookup"><span data-stu-id="49d19-125">Go to **Project management and accounting** \> **Journals** \> **Fee**.</span></span>
4. <span data-ttu-id="49d19-126">На странице **Журнал сборов** выберите **Создать** и введите название журнала.</span><span class="sxs-lookup"><span data-stu-id="49d19-126">On the **Fee journal** page, select **New** , and enter the journal name.</span></span>

## <a name="create-a-contract-for-progress-billings"></a><span data-ttu-id="49d19-127">Создание контракта для выставления счетов на основе хода выполнения</span><span class="sxs-lookup"><span data-stu-id="49d19-127">Create a contract for progress billings</span></span>

<span data-ttu-id="49d19-128">Используйте эту процедуру, чтобы создать контракт по проекту для проекта с фиксированной ценой.</span><span class="sxs-lookup"><span data-stu-id="49d19-128">Use this procedure to create a project contract for a fixed-price project.</span></span> <span data-ttu-id="49d19-129">Вы создаете счет по проекту, когда работа, выполненная по проекту, достигает указанного процента.</span><span class="sxs-lookup"><span data-stu-id="49d19-129">You create a project invoice when the work that is completed on the project reaches a specified percentage.</span></span>

1. <span data-ttu-id="49d19-130">Перейдите в раздел **Управление и учет по проектам** \> **Проекты** \> **Контракты по проектам**.</span><span class="sxs-lookup"><span data-stu-id="49d19-130">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="49d19-131">На странице **Контракты по проектам** выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="49d19-131">On the **Project contracts** page, select **New**.</span></span>
3. <span data-ttu-id="49d19-132">В диалоговом окне **Создать контракт по проекту** задайте следующие поля:</span><span class="sxs-lookup"><span data-stu-id="49d19-132">In the **New project contract** dialog box, set the following fields:</span></span>

    - <span data-ttu-id="49d19-133">**Название**</span><span class="sxs-lookup"><span data-stu-id="49d19-133">**Name**</span></span>
    - <span data-ttu-id="49d19-134">**Тип финансирования**</span><span class="sxs-lookup"><span data-stu-id="49d19-134">**Funding type**</span></span>
    - <span data-ttu-id="49d19-135">**Источник финансирования**</span><span class="sxs-lookup"><span data-stu-id="49d19-135">**Funding source**</span></span>
    - <span data-ttu-id="49d19-136">**Валюта продаж** — по умолчанию эта валюта используется для счетов клиентам, связанных с контрактом по проекту.</span><span class="sxs-lookup"><span data-stu-id="49d19-136">**Sales currency** – By default, this currency is used for customer invoices that are associated with the project contract.</span></span> <span data-ttu-id="49d19-137">Однако вы можете изменить валюту продаж в конкретном счете клиенту.</span><span class="sxs-lookup"><span data-stu-id="49d19-137">However, you can change the sales currency on a specific customer invoice.</span></span>

4. <span data-ttu-id="49d19-138">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="49d19-138">Select **OK**.</span></span> <span data-ttu-id="49d19-139">Информация копируется в заголовок страницы **Контракты по проектам**.</span><span class="sxs-lookup"><span data-stu-id="49d19-139">The information is copied to the header of the **Project contracts** page.</span></span>
5. <span data-ttu-id="49d19-140">На странице **Контракты по проектам** заполните остальную необходимую информацию для проекта.</span><span class="sxs-lookup"><span data-stu-id="49d19-140">On the **Project contracts** page, fill in the rest of the required information for the project.</span></span>

## <a name="create-a-project-for-progress-billings"></a><span data-ttu-id="49d19-141">Создание проекта для выставления счетов на основе хода выполнения</span><span class="sxs-lookup"><span data-stu-id="49d19-141">Create a project for progress billings</span></span>

<span data-ttu-id="49d19-142">Выполните следующие действия, чтобы создать проект и все вложенные проекты, связанные с контрактом по проекту.</span><span class="sxs-lookup"><span data-stu-id="49d19-142">Follow these steps to create a project and any subprojects that are associated with a project contract.</span></span>

1. <span data-ttu-id="49d19-143">Перейдите в раздел **Управление проектами и учет** \> **Проекты** \> **Все проекты**.</span><span class="sxs-lookup"><span data-stu-id="49d19-143">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="49d19-144">На странице **Все проекты** выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="49d19-144">On the **All projects** page, select **New**.</span></span>
3. <span data-ttu-id="49d19-145">В диалоговом окне **Создать проект** в поле **Тип проекта** выберите **Время и расходы**.</span><span class="sxs-lookup"><span data-stu-id="49d19-145">In the **New project** dialog box, in the **Project type** field, select **Time and material**.</span></span>
4. <span data-ttu-id="49d19-146">Выберите группу проектов.</span><span class="sxs-lookup"><span data-stu-id="49d19-146">Select a project group.</span></span> <span data-ttu-id="49d19-147">Группа проектов определяет информацию разноски для проектов, которые назначены группе.</span><span class="sxs-lookup"><span data-stu-id="49d19-147">A project group defines the posting information for the projects that are assigned to the group.</span></span>
5. <span data-ttu-id="49d19-148">Выберите **Создать проект**.</span><span class="sxs-lookup"><span data-stu-id="49d19-148">Select **Create project**.</span></span>
6. <span data-ttu-id="49d19-149">После создания проекта установите стадию проекта **В работе**.</span><span class="sxs-lookup"><span data-stu-id="49d19-149">After the project is created, set the project stage to **In process**.</span></span>

## <a name="create-a-budget-for-a-project"></a><span data-ttu-id="49d19-150">Создание бюджета для проекта</span><span class="sxs-lookup"><span data-stu-id="49d19-150">Create a budget for a project</span></span>

<span data-ttu-id="49d19-151">Категории бюджета используются для автоматического расчета сумм счетов для процента работы, выполненной для каждой категории.</span><span class="sxs-lookup"><span data-stu-id="49d19-151">Budget categories are used to automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="49d19-152">Выполните следующие шаги, чтобы создать категории бюджета для предполагаемых затрат.</span><span class="sxs-lookup"><span data-stu-id="49d19-152">Follow these steps to create budget categories for the estimated costs.</span></span>

1. <span data-ttu-id="49d19-153">Перейдите в раздел **Управление проектами и учет** \> **Проекты** \> **Все проекты**.</span><span class="sxs-lookup"><span data-stu-id="49d19-153">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="49d19-154">На странице **Все проекты** выберите и откройте нужный проект.</span><span class="sxs-lookup"><span data-stu-id="49d19-154">On the **All projects** page, select and open the project that you want.</span></span>
3. <span data-ttu-id="49d19-155">На странице **Проекты** на панели действий на вкладке **План** в группе **Бюджет** выберите **Бюджет проекта**.</span><span class="sxs-lookup"><span data-stu-id="49d19-155">On the **Projects** page, on the Action Pane, on the **Plan** tab, in the **Budget** group, select **Project budget**.</span></span>
4. <span data-ttu-id="49d19-156">На странице **Бюджет проекта** введите ориентировочную стоимость для каждой категории в проекте.</span><span class="sxs-lookup"><span data-stu-id="49d19-156">On the **Project budget** page, enter an estimated cost for each category in the project.</span></span>

## <a name="create-billing-rules-for-progress-billings"></a><span data-ttu-id="49d19-157">Создание правил выставления счетов для выставления счетов на основе хода выполнения</span><span class="sxs-lookup"><span data-stu-id="49d19-157">Create billing rules for progress billings</span></span>

1. <span data-ttu-id="49d19-158">Перейдите в раздел **Управление и учет по проектам** \> **Проекты** \> **Контракты по проектам**.</span><span class="sxs-lookup"><span data-stu-id="49d19-158">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="49d19-159">На странице **Контракты по проекту** выберите и откройте контракт по проекту.</span><span class="sxs-lookup"><span data-stu-id="49d19-159">On the **Project contracts** page, select and open a project contract.</span></span>
3. <span data-ttu-id="49d19-160">На странице контракта по проекту на экспресс-вкладке **Правила выставления счетов** выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="49d19-160">On the project contract page, on the **Billing rules** FastTab, select **Add**.</span></span>
4. <span data-ttu-id="49d19-161">На странице **Правило выставления счетов** в поле **Тип строки** выберите **Обработать**.</span><span class="sxs-lookup"><span data-stu-id="49d19-161">On the **Billing rule** page, in the **Line type** field, select **Progress**.</span></span>
5. <span data-ttu-id="49d19-162">На экспресс-вкладке **Сведения строки правила выставления счетов** в поле **Сумма контракта** введите общую сумму контракта.</span><span class="sxs-lookup"><span data-stu-id="49d19-162">On the **Billing rule line details** FastTab, in the **Contract value** field, enter the total value of the contract.</span></span>
6. <span data-ttu-id="49d19-163">В поле **Категория** выберите категорию, в которую будет проводиться транзакция оплаты.</span><span class="sxs-lookup"><span data-stu-id="49d19-163">In the **Category** field, select the category to post the fee transaction to.</span></span>
7. <span data-ttu-id="49d19-164">В поле **Проект** выберите проект, в котором используется это правило выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="49d19-164">In the **Project** field, select the project that uses this billing rule.</span></span>
8. <span data-ttu-id="49d19-165">Необязательно: назначьте правило выставления счетов дополнительным проектам.</span><span class="sxs-lookup"><span data-stu-id="49d19-165">Optional: Assign the billing rule to additional projects.</span></span> <span data-ttu-id="49d19-166">На экспресс-вкладке **Проект** в разделе **Доступные проекты** выберите проект, затем выберите кнопку со стрелкой вправо, чтобы добавить проект в раздел **Выбранные проекты**.</span><span class="sxs-lookup"><span data-stu-id="49d19-166">On the **Project** FastTab, in the **Available projects** section, select a project, and then select the right arrow button to add the project to the **Selected projects** section.</span></span>
9. <span data-ttu-id="49d19-167">Необязательно: рассчитайте процентную сумму, которую клиент удерживает из платежей по счету.</span><span class="sxs-lookup"><span data-stu-id="49d19-167">Optional: Calculate the percentage amount that the customer withholds from payments on an invoice.</span></span> <span data-ttu-id="49d19-168">На экспресс-вкладке **Условия удержания платежей** выберите источник финансирования, затем в поле **Процент удержания** введите процент удержания.</span><span class="sxs-lookup"><span data-stu-id="49d19-168">On the **Payment retention terms** FastTab, select the funding source, and then, in the **Retention percentage** field, enter the retention percentage.</span></span>
10. <span data-ttu-id="49d19-169">Повторите эти шаги, чтобы создать дополнительные правила выставления счетов для контракта по проекту.</span><span class="sxs-lookup"><span data-stu-id="49d19-169">Repeat these steps to create additional billing rules for the project contract.</span></span>
