---
title: Настройка подлежащих оплате компонентов строки контракта на основе проекта
description: Эта тема предоставляет информацию о том, как добавить платные компоненты в строки контракта в Project Operations.
author: rumant
ms.date: 10/08/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b29c912828aa4af2d2d9cb47869012087cb834b4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003737"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a><span data-ttu-id="ccaec-103">Настройка подлежащих оплате компонентов строки контракта на основе проекта</span><span class="sxs-lookup"><span data-stu-id="ccaec-103">Configure chargeable components of a project-based contract line</span></span>

<span data-ttu-id="ccaec-104">_**Относится к:** Облегченное развертывание — от сделки до счетов-проформ, Project Operations для сценариев на основе ресурсов/нескладируемых запасов_</span><span class="sxs-lookup"><span data-stu-id="ccaec-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="ccaec-105">Строка контракта на основе проекта имеет *включенные* компоненты и *оплачиваемые* компоненты.</span><span class="sxs-lookup"><span data-stu-id="ccaec-105">A project-based contract line has *included* components and *chargeable* components.</span></span>

<span data-ttu-id="ccaec-106">Включенные компоненты — это компоненты, на которые распространяется:</span><span class="sxs-lookup"><span data-stu-id="ccaec-106">Included components are components that are subject to:</span></span>

  - <span data-ttu-id="ccaec-107">Метод выставления счетов и разделение клиентов</span><span class="sxs-lookup"><span data-stu-id="ccaec-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="ccaec-108">Максимальные лимиты</span><span class="sxs-lookup"><span data-stu-id="ccaec-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="ccaec-109">Настройки периодичности выставления счетов, определенные в строке контракта на основе проекта</span><span class="sxs-lookup"><span data-stu-id="ccaec-109">Invoice frequency settings defined on the project-based contract line</span></span>

<span data-ttu-id="ccaec-110">Подмножество включенных компонентов можно пометить как оплачиваемые с помощью поля **Тип выставления счетов**.</span><span class="sxs-lookup"><span data-stu-id="ccaec-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="ccaec-111">Поле **Тип выставления счетов** — это набор параметров, который позволяет использовать следующие значения в контексте строки контракта:</span><span class="sxs-lookup"><span data-stu-id="ccaec-111">The **Billing Type** field is an option-set that allows the following values in the context of a contract line:</span></span>

  - <span data-ttu-id="ccaec-112">Оплачивается</span><span class="sxs-lookup"><span data-stu-id="ccaec-112">Chargeable</span></span>
  - <span data-ttu-id="ccaec-113">Не оплачивается</span><span class="sxs-lookup"><span data-stu-id="ccaec-113">Non-chargeable</span></span>

<span data-ttu-id="ccaec-114">Оплачиваемые компоненты можно определить по задачам, ролям и категориям транзакций.</span><span class="sxs-lookup"><span data-stu-id="ccaec-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="ccaec-115">Возможность выставления счетов определяется для задач по строке контракта по проекту и применяется ко всем классам транзакций, включенным в строку.</span><span class="sxs-lookup"><span data-stu-id="ccaec-115">Chargeability is defined on tasks for a project contract line and applies to all transaction classes included on the line.</span></span> <span data-ttu-id="ccaec-116">Если поле **Включить задачи** в строке контракта пустое или имеет значение **Весь проект**, то вкладка **Оплачиваемые задачи** будет недоступна.</span><span class="sxs-lookup"><span data-stu-id="ccaec-116">If the **Include Tasks** field on a contract line is blank or set to **Entire project**, the **Chargeable tasks** tab will not be available.</span></span>

<span data-ttu-id="ccaec-117">Возможность выставления счетов, определенная для ролей в строке контракта по проекту, применяется только к классу транзакций **Время**.</span><span class="sxs-lookup"><span data-stu-id="ccaec-117">Chargeability defined on roles for a project contract line only applies to the **Time** transaction class.</span></span> <span data-ttu-id="ccaec-118">Если поле **Включить время** в строке контракта пустое или имеет значение **Нет**, то вкладка **Оплачиваемые роли** будет недоступна.</span><span class="sxs-lookup"><span data-stu-id="ccaec-118">If the **Include Time** field on a contract line is set to **No**, the **Chargeable roles** tab will not be available.</span></span>

<span data-ttu-id="ccaec-119">Возможность выставления счетов, определенная для категорий транзакций в строке контракта по проекту, применяется только к классу транзакций **Расходы**.</span><span class="sxs-lookup"><span data-stu-id="ccaec-119">Chargeability defined on transaction categories for a project contract line only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="ccaec-120">Если поле **Включить расходы** в строке контракта пустое или имеет значение **Нет**, то вкладка **Оплачиваемые категории** будет недоступна.</span><span class="sxs-lookup"><span data-stu-id="ccaec-120">If the **Include Expenses** field is set to **No**, the **Chargeable Categories** tab will not be available.</span></span>

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a><span data-ttu-id="ccaec-121">Обновление задачи проекта как оплачиваемой или не оплачиваемой</span><span class="sxs-lookup"><span data-stu-id="ccaec-121">Update a project task as chargeable or non-chargeable</span></span>

<span data-ttu-id="ccaec-122">Задача проекта может быть оплачиваемой или не оплачиваемой по конкретной строке контракта, что делает возможной следующую настройку:</span><span class="sxs-lookup"><span data-stu-id="ccaec-122">A project task can be chargeable or non-chargeable on a specific contract line, which makes the following setup possible:</span></span>

<span data-ttu-id="ccaec-123">Если строка контракта на основе проекта включает **Время** и определенная задача **T1** связана с ней как оплачиваемая.</span><span class="sxs-lookup"><span data-stu-id="ccaec-123">If a project-based contract line includes **Time** and a certain task, **T1** is associated to it as chargeable.</span></span> <span data-ttu-id="ccaec-124">Если есть вторая строка контракта, которая включает **Расходы**, вы можете связать задачу T1 в строке контракта как не оплачиваемую.</span><span class="sxs-lookup"><span data-stu-id="ccaec-124">If there is a second contract line that includes **Expense**, you can associate the T1 task on the contract line as non-chargeable.</span></span> <span data-ttu-id="ccaec-125">В результате все время, записанное на задачу, оплачивается, а все расходы — не оплачиваются.</span><span class="sxs-lookup"><span data-stu-id="ccaec-125">The result is that all of the time recorded on the task is chargeable and all expenses are non-chargeable.</span></span>

<span data-ttu-id="ccaec-126">Тип выставления счетов для задачи можно настроить на вкладке **Оплачиваемые задачи** строки контракта, обновив поле **Тип выставления счетов** во вложенной сетке задач строки контракта.</span><span class="sxs-lookup"><span data-stu-id="ccaec-126">A task's billing type can be configured on the **Chargeable Tasks** tab of the contract line by updating the **Billing Type** field on the contract line tasks subgrid.</span></span> <span data-ttu-id="ccaec-127">Кроме того, вы можете обновить поле **Тип выставления счетов** во вложенной сетке в настройке выставления счетов по задаче проекта, в которой отображаются строки контракта, связанные с задачей.</span><span class="sxs-lookup"><span data-stu-id="ccaec-127">Alternatively, you can update the **Billing Type** field on the subgrid of the task Billing setup of a project that shows the contract lines associated to a task.</span></span>

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a><span data-ttu-id="ccaec-128">Обновление роли как оплачиваемой или не оплачиваемой</span><span class="sxs-lookup"><span data-stu-id="ccaec-128">Update a role as chargeable or non-chargeable</span></span>

<span data-ttu-id="ccaec-129">Роль может быть оплачиваемой или неоплачиваемой по определенной строке контракта.</span><span class="sxs-lookup"><span data-stu-id="ccaec-129">A role can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="ccaec-130">Тип выставления счетов для роли можно настроить на вкладке **Оплачиваемые роли** строки контракта.</span><span class="sxs-lookup"><span data-stu-id="ccaec-130">A role's billing type can be configured on the **Chargeable Roles** tab of a contract line.</span></span> <span data-ttu-id="ccaec-131">Для этого обновите поле **Тип выставления счетов** во вложенной сетке **Оплачиваемые роли**.</span><span class="sxs-lookup"><span data-stu-id="ccaec-131">To do this, update the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a><span data-ttu-id="ccaec-132">Обновление категории транзакций как оплачиваемой или неоплачиваемой</span><span class="sxs-lookup"><span data-stu-id="ccaec-132">Update a transaction category as chargeable or non-chargeable</span></span>

<span data-ttu-id="ccaec-133">Категория транзакций может быть оплачиваемой или неоплачиваемой по определенной строке контракта.</span><span class="sxs-lookup"><span data-stu-id="ccaec-133">A transaction category can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="ccaec-134">Тип выставления счетов для транзакции можно настроить на вкладке **Оплачиваемые транзакции** строки контракта на основе проекта.</span><span class="sxs-lookup"><span data-stu-id="ccaec-134">A transaction's billing type can be configured on the **Chargeable Categories** tab of a project-based contract line.</span></span> <span data-ttu-id="ccaec-135">Для этого обновите поле **Тип выставления счетов** во вложенной сетке **Оплачиваемые категории**.</span><span class="sxs-lookup"><span data-stu-id="ccaec-135">To do this, update the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="ccaec-136">Разрешение возможности выставления счетов</span><span class="sxs-lookup"><span data-stu-id="ccaec-136">Resolve chargeability</span></span>

<span data-ttu-id="ccaec-137">Оценка или фактическое значение, созданное для времени, считается подлежащим оплате в том случае, если:</span><span class="sxs-lookup"><span data-stu-id="ccaec-137">An estimate or actual created for time is only considered chargeable if:</span></span>

   - <span data-ttu-id="ccaec-138">**Время** включено в строку контракта.</span><span class="sxs-lookup"><span data-stu-id="ccaec-138">**Time** is included on the contract line.</span></span>
   - <span data-ttu-id="ccaec-139">**Роль** настроена как подлежащая оплате в строке контракта.</span><span class="sxs-lookup"><span data-stu-id="ccaec-139">**Role** is configured as chargeable on the contract line.</span></span>
   - <span data-ttu-id="ccaec-140">**Включенные задачи** заданы как **Выбранные задачи** в строке контракта.</span><span class="sxs-lookup"><span data-stu-id="ccaec-140">**Included Tasks** is set to **Selected tasks** on the contract line.</span></span>
 
 <span data-ttu-id="ccaec-141">Если эти три условия верны, задача конфигурируется как подлежащая оплате.</span><span class="sxs-lookup"><span data-stu-id="ccaec-141">If these three things are true, the task is configured as chargeable.</span></span> 

<span data-ttu-id="ccaec-142">Оценка или фактическое значение, созданное для расходов, считается подлежащим оплате в том случае, если:</span><span class="sxs-lookup"><span data-stu-id="ccaec-142">An estimate or actual created for expense is only considered chargeable if:</span></span>

   - <span data-ttu-id="ccaec-143">**Расходы** включены в строку контракта</span><span class="sxs-lookup"><span data-stu-id="ccaec-143">**Expense** is included on the contract line</span></span>
   - <span data-ttu-id="ccaec-144">**Категория проводки** настроена как подлежащая оплате в строке контракта</span><span class="sxs-lookup"><span data-stu-id="ccaec-144">**Transaction category** is configured as chargeable on the contract line</span></span>
   - <span data-ttu-id="ccaec-145">**Включенные задачи** заданы как **Выбранная задача** в строке контракта</span><span class="sxs-lookup"><span data-stu-id="ccaec-145">**Included Tasks** is set to **Selected task** on the contract line</span></span>
  
 <span data-ttu-id="ccaec-146">Если эти три условия верны, **Задача** конфигурируется как подлежащая оплате.</span><span class="sxs-lookup"><span data-stu-id="ccaec-146">If these three things are true, the **Task** is configured as chargeable.</span></span> 

<span data-ttu-id="ccaec-147">Оценка или фактическое значение, созданное для материала, считается подлежащим оплате в том случае, если:</span><span class="sxs-lookup"><span data-stu-id="ccaec-147">An estimate or actual created for material is only considered chargeable if:</span></span>

   - <span data-ttu-id="ccaec-148">**Материалы** включены в строку контракта</span><span class="sxs-lookup"><span data-stu-id="ccaec-148">**Materials** is included on the contract line</span></span>
   - <span data-ttu-id="ccaec-149">**Включенные задачи** заданы как **Выбранные задачи** в строке контракта</span><span class="sxs-lookup"><span data-stu-id="ccaec-149">**Included Tasks** is set to **Selected tasks** on the contract line</span></span>

<span data-ttu-id="ccaec-150">Если эти два условия верны, **Задача** конфигурируется как подлежащая оплате.</span><span class="sxs-lookup"><span data-stu-id="ccaec-150">If these two things are true, the **Task** is configured as chargeable.</span></span> 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="ccaec-151">
                    <strong>Включает время</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccaec-151">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="ccaec-152">
                    <strong>Включает расходы</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccaec-152">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="ccaec-153">
                    <strong>Включить материалы</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccaec-153">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="ccaec-154">
                    <strong>Включенные задачи</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccaec-154">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="ccaec-155">
                    <strong>Роль</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccaec-155">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="ccaec-156">
                    <strong>Категория</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccaec-156">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="ccaec-157">
                    <strong>Задача</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccaec-157">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="ccaec-158">
                    <strong>Влияние возможности оплаты</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccaec-158">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ccaec-159">Да</span><span class="sxs-lookup"><span data-stu-id="ccaec-159">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="ccaec-160">Да</span><span class="sxs-lookup"><span data-stu-id="ccaec-160">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="ccaec-161">Да</span><span class="sxs-lookup"><span data-stu-id="ccaec-161">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="ccaec-162">Весь проект</span><span class="sxs-lookup"><span data-stu-id="ccaec-162">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ccaec-163">Оплачивается</span><span class="sxs-lookup"><span data-stu-id="ccaec-163">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ccaec-164">Оплачивается</span><span class="sxs-lookup"><span data-stu-id="ccaec-164">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ccaec-165">Не может быть установлено</span><span class="sxs-lookup"><span data-stu-id="ccaec-165">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="ccaec-166">Выставление счетов за фактическое время: <strong>Оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccaec-166">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ccaec-167">Тип выставления счетов за фактические расходы: <strong>Оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccaec-167">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ccaec-168">Тип выставления счетов за фактические материалы: <strong>Оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccaec-168">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ccaec-169">Да</span><span class="sxs-lookup"><span data-stu-id="ccaec-169">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="ccaec-170">Да</span><span class="sxs-lookup"><span data-stu-id="ccaec-170">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="ccaec-171">Да</span><span class="sxs-lookup"><span data-stu-id="ccaec-171">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="ccaec-172">Только выбранные задачи</span><span class="sxs-lookup"><span data-stu-id="ccaec-172">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ccaec-173">Оплачивается</span><span class="sxs-lookup"><span data-stu-id="ccaec-173">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ccaec-174">Оплачивается</span><span class="sxs-lookup"><span data-stu-id="ccaec-174">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ccaec-175">Оплачивается</span><span class="sxs-lookup"><span data-stu-id="ccaec-175">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="ccaec-176">Выставление счетов за фактическое время: <strong>Оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccaec-176">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ccaec-177">Тип выставления счетов за фактические расходы: <strong>Оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccaec-177">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ccaec-178">Тип выставления счетов за фактические материалы: <strong>Оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccaec-178">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ccaec-179">Да</span><span class="sxs-lookup"><span data-stu-id="ccaec-179">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="ccaec-180">Да</span><span class="sxs-lookup"><span data-stu-id="ccaec-180">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="ccaec-181">Да</span><span class="sxs-lookup"><span data-stu-id="ccaec-181">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="ccaec-182">Только выбранные задачи</span><span class="sxs-lookup"><span data-stu-id="ccaec-182">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="ccaec-183">
                    <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccaec-183">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ccaec-184">Оплачивается</span><span class="sxs-lookup"><span data-stu-id="ccaec-184">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ccaec-185">Оплачивается</span><span class="sxs-lookup"><span data-stu-id="ccaec-185">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="ccaec-186">Выставления счетов за фактическое время: <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccaec-186">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ccaec-187">Тип выставления счетов за фактические расходы: Оплачивается</span><span class="sxs-lookup"><span data-stu-id="ccaec-187">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="ccaec-188">Тип выставления счетов за фактические материалы: Оплачивается</span><span class="sxs-lookup"><span data-stu-id="ccaec-188">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ccaec-189">Да</span><span class="sxs-lookup"><span data-stu-id="ccaec-189">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="ccaec-190">Да</span><span class="sxs-lookup"><span data-stu-id="ccaec-190">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="ccaec-191">Да</span><span class="sxs-lookup"><span data-stu-id="ccaec-191">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="ccaec-192">Только выбранные задачи</span><span class="sxs-lookup"><span data-stu-id="ccaec-192">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ccaec-193">Оплачивается</span><span class="sxs-lookup"><span data-stu-id="ccaec-193">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ccaec-194">Оплачивается</span><span class="sxs-lookup"><span data-stu-id="ccaec-194">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="ccaec-195">
                    <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccaec-195">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="ccaec-196">Выставления счетов за фактическое время: <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccaec-196">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ccaec-197">Тип выставления счетов за фактические расходы: <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccaec-197">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ccaec-198">Тип выставления счетов за фактические материалы: <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccaec-198">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ccaec-199">Да</span><span class="sxs-lookup"><span data-stu-id="ccaec-199">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="ccaec-200">Да</span><span class="sxs-lookup"><span data-stu-id="ccaec-200">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="ccaec-201">Да</span><span class="sxs-lookup"><span data-stu-id="ccaec-201">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="ccaec-202">Только выбранные задачи</span><span class="sxs-lookup"><span data-stu-id="ccaec-202">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="ccaec-203">
                    <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccaec-203">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ccaec-204">Оплачивается</span><span class="sxs-lookup"><span data-stu-id="ccaec-204">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="ccaec-205">
                    <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccaec-205">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="ccaec-206">Выставления счетов за фактическое время: <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccaec-206">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ccaec-207">Тип выставления счетов за фактические расходы: <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccaec-207">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ccaec-208">Тип выставления счетов за фактические материалы: <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccaec-208">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ccaec-209">Да</span><span class="sxs-lookup"><span data-stu-id="ccaec-209">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="ccaec-210">Да</span><span class="sxs-lookup"><span data-stu-id="ccaec-210">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="ccaec-211">Да</span><span class="sxs-lookup"><span data-stu-id="ccaec-211">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="ccaec-212">Только выбранные задачи</span><span class="sxs-lookup"><span data-stu-id="ccaec-212">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="ccaec-213">
                    <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccaec-213">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="ccaec-214">
                    <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccaec-214">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ccaec-215">Оплачивается</span><span class="sxs-lookup"><span data-stu-id="ccaec-215">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="ccaec-216">Выставления счетов за фактическое время: <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccaec-216">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ccaec-217">Тип выставления счетов за фактические расходы: <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccaec-217">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ccaec-218">Тип выставления счетов за фактические материалы: Оплачивается</span><span class="sxs-lookup"><span data-stu-id="ccaec-218">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="ccaec-219">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccaec-219">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="ccaec-220">Да</span><span class="sxs-lookup"><span data-stu-id="ccaec-220">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="ccaec-221">Да</span><span class="sxs-lookup"><span data-stu-id="ccaec-221">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="ccaec-222">Весь проект</span><span class="sxs-lookup"><span data-stu-id="ccaec-222">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ccaec-223">Не может быть установлено</span><span class="sxs-lookup"><span data-stu-id="ccaec-223">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="ccaec-224">
                    <strong>Оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccaec-224">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ccaec-225">Не может быть установлено</span><span class="sxs-lookup"><span data-stu-id="ccaec-225">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="ccaec-226">Выставления счетов за фактическое время: <strong>Недоступно</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccaec-226">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ccaec-227">Тип выставления счетов за фактические расходы: Оплачивается</span><span class="sxs-lookup"><span data-stu-id="ccaec-227">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="ccaec-228">Тип выставления счетов за фактические материалы: Оплачивается</span><span class="sxs-lookup"><span data-stu-id="ccaec-228">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="ccaec-229">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccaec-229">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="ccaec-230">Да</span><span class="sxs-lookup"><span data-stu-id="ccaec-230">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="ccaec-231">Да</span><span class="sxs-lookup"><span data-stu-id="ccaec-231">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="ccaec-232">Весь проект</span><span class="sxs-lookup"><span data-stu-id="ccaec-232">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ccaec-233">Не может быть установлено</span><span class="sxs-lookup"><span data-stu-id="ccaec-233">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="ccaec-234">
                    <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccaec-234">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ccaec-235">Не может быть установлено</span><span class="sxs-lookup"><span data-stu-id="ccaec-235">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="ccaec-236">Выставления счетов за фактическое время: <strong>Недоступно</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccaec-236">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ccaec-237">Тип выставления счетов за фактические расходы: <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccaec-237">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ccaec-238">Тип выставления счетов за фактические материалы: Оплачивается</span><span class="sxs-lookup"><span data-stu-id="ccaec-238">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ccaec-239">Да</span><span class="sxs-lookup"><span data-stu-id="ccaec-239">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="ccaec-240">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccaec-240">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="ccaec-241">Да</span><span class="sxs-lookup"><span data-stu-id="ccaec-241">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="ccaec-242">Весь проект</span><span class="sxs-lookup"><span data-stu-id="ccaec-242">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ccaec-243">Оплачивается</span><span class="sxs-lookup"><span data-stu-id="ccaec-243">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ccaec-244">Не может быть установлено</span><span class="sxs-lookup"><span data-stu-id="ccaec-244">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ccaec-245">Не может быть установлено</span><span class="sxs-lookup"><span data-stu-id="ccaec-245">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="ccaec-246">Выставления счетов за фактическое время: Оплачивается</span><span class="sxs-lookup"><span data-stu-id="ccaec-246">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="ccaec-247">Тип выставления счетов за фактические расходы: <strong>Недоступно</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccaec-247">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ccaec-248">Тип выставления счетов за фактические материалы: Оплачивается</span><span class="sxs-lookup"><span data-stu-id="ccaec-248">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ccaec-249">Да</span><span class="sxs-lookup"><span data-stu-id="ccaec-249">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="ccaec-250">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccaec-250">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="ccaec-251">Да</span><span class="sxs-lookup"><span data-stu-id="ccaec-251">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="ccaec-252">Весь проект</span><span class="sxs-lookup"><span data-stu-id="ccaec-252">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="ccaec-253">
                    <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccaec-253">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ccaec-254">Не может быть установлено</span><span class="sxs-lookup"><span data-stu-id="ccaec-254">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ccaec-255">Не может быть установлено</span><span class="sxs-lookup"><span data-stu-id="ccaec-255">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="ccaec-256">Выставления счетов за фактическое время: <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccaec-256">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="ccaec-257">Тип выставления счетов за фактические расходы: <strong>Недоступно</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccaec-257">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ccaec-258">Тип выставления счетов за фактические материалы: Оплачивается</span><span class="sxs-lookup"><span data-stu-id="ccaec-258">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ccaec-259">Да</span><span class="sxs-lookup"><span data-stu-id="ccaec-259">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="ccaec-260">Да</span><span class="sxs-lookup"><span data-stu-id="ccaec-260">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="ccaec-261">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccaec-261">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="ccaec-262">Весь проект</span><span class="sxs-lookup"><span data-stu-id="ccaec-262">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ccaec-263">Оплачивается</span><span class="sxs-lookup"><span data-stu-id="ccaec-263">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ccaec-264">Оплачивается</span><span class="sxs-lookup"><span data-stu-id="ccaec-264">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ccaec-265">Не может быть установлено</span><span class="sxs-lookup"><span data-stu-id="ccaec-265">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="ccaec-266">Выставления счетов за фактическое время: Оплачивается</span><span class="sxs-lookup"><span data-stu-id="ccaec-266">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="ccaec-267">Тип выставления счетов за фактические расходы: Оплачивается</span><span class="sxs-lookup"><span data-stu-id="ccaec-267">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="ccaec-268">Тип выставления счетов за фактические материалы: <strong>Недоступно</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccaec-268">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ccaec-269">Да</span><span class="sxs-lookup"><span data-stu-id="ccaec-269">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="ccaec-270">Да</span><span class="sxs-lookup"><span data-stu-id="ccaec-270">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="ccaec-271">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccaec-271">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="ccaec-272">Весь проект</span><span class="sxs-lookup"><span data-stu-id="ccaec-272">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="ccaec-273">
                    <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccaec-273">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="ccaec-274">
                    <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccaec-274">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ccaec-275">Не может быть установлено</span><span class="sxs-lookup"><span data-stu-id="ccaec-275">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="ccaec-276">Выставления счетов за фактическое время: <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccaec-276">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="ccaec-277">Тип выставления счетов за фактические расходы: <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccaec-277">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="ccaec-278">Тип выставления счетов за фактические материалы: <strong>Недоступно</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccaec-278">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
