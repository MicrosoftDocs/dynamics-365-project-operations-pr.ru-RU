---
title: Настройка подлежащих оплате компонентов строки контракта на основе проекта
description: Эта тема предоставляет информацию о том, как добавить платные компоненты в строки контракта в Project Operations.
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ddada2cb412ba7370fb0a750325a84772937d8d0
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858489"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a><span data-ttu-id="650f8-103">Настройка подлежащих оплате компонентов строки контракта на основе проекта</span><span class="sxs-lookup"><span data-stu-id="650f8-103">Configure chargeable components of a project-based contract line</span></span>

<span data-ttu-id="650f8-104">_**Относится к:** Облегченное развертывание — от сделки до счетов-проформ, Project Operations для сценариев на основе ресурсов/нескладируемых запасов_</span><span class="sxs-lookup"><span data-stu-id="650f8-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="650f8-105">Строка контракта на основе проекта имеет *включенные* компоненты и *оплачиваемые* компоненты.</span><span class="sxs-lookup"><span data-stu-id="650f8-105">A project-based contract line has *included* components and *chargeable* components.</span></span>

<span data-ttu-id="650f8-106">Включенные компоненты — это компоненты, на которые распространяется:</span><span class="sxs-lookup"><span data-stu-id="650f8-106">Included components are components that are subject to:</span></span>

  - <span data-ttu-id="650f8-107">Метод выставления счетов и разделение клиентов</span><span class="sxs-lookup"><span data-stu-id="650f8-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="650f8-108">Максимальные лимиты</span><span class="sxs-lookup"><span data-stu-id="650f8-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="650f8-109">Настройки периодичности выставления счетов, определенные в строке контракта на основе проекта</span><span class="sxs-lookup"><span data-stu-id="650f8-109">Invoice frequency settings defined on the project-based contract line</span></span>

<span data-ttu-id="650f8-110">Подмножество включенных компонентов можно пометить как оплачиваемые с помощью поля **Тип выставления счетов**.</span><span class="sxs-lookup"><span data-stu-id="650f8-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="650f8-111">Поле **Тип выставления счетов** — это набор параметров, который позволяет использовать следующие значения в контексте строки контракта:</span><span class="sxs-lookup"><span data-stu-id="650f8-111">The **Billing Type** field is an option-set that allows the following values in the context of a contract line:</span></span>

  - <span data-ttu-id="650f8-112">Оплачивается</span><span class="sxs-lookup"><span data-stu-id="650f8-112">Chargeable</span></span>
  - <span data-ttu-id="650f8-113">Не оплачивается</span><span class="sxs-lookup"><span data-stu-id="650f8-113">Non-chargeable</span></span>

<span data-ttu-id="650f8-114">Оплачиваемые компоненты можно определить по задачам, ролям и категориям транзакций.</span><span class="sxs-lookup"><span data-stu-id="650f8-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="650f8-115">Возможность выставления счетов определяется для задач по строке контракта по проекту и применяется ко всем классам транзакций, включенным в строку.</span><span class="sxs-lookup"><span data-stu-id="650f8-115">Chargeability is defined on tasks for a project contract line and applies to all transaction classes included on the line.</span></span> <span data-ttu-id="650f8-116">Если поле **Включить задачи** в строке контракта пустое или имеет значение **Весь проект**, то вкладка **Оплачиваемые задачи** будет недоступна.</span><span class="sxs-lookup"><span data-stu-id="650f8-116">If the **Include Tasks** field on a contract line is blank or set to **Entire project**, the **Chargeable tasks** tab will not be available.</span></span>

<span data-ttu-id="650f8-117">Возможность выставления счетов, определенная для ролей в строке контракта по проекту, применяется только к классу транзакций **Время**.</span><span class="sxs-lookup"><span data-stu-id="650f8-117">Chargeability defined on roles for a project contract line only applies to the **Time** transaction class.</span></span> <span data-ttu-id="650f8-118">Если поле **Включить время** в строке контракта пустое или имеет значение **Нет**, то вкладка **Оплачиваемые роли** будет недоступна.</span><span class="sxs-lookup"><span data-stu-id="650f8-118">If the **Include Time** field on a contract line is set to **No**, the **Chargeable roles** tab will not be available.</span></span>

<span data-ttu-id="650f8-119">Возможность выставления счетов, определенная для категорий транзакций в строке контракта по проекту, применяется только к классу транзакций **Расходы**.</span><span class="sxs-lookup"><span data-stu-id="650f8-119">Chargeability defined on transaction categories for a project contract line only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="650f8-120">Если поле **Включить расходы** в строке контракта пустое или имеет значение **Нет**, то вкладка **Оплачиваемые категории** будет недоступна.</span><span class="sxs-lookup"><span data-stu-id="650f8-120">If the **Include Expenses** field is set to **No**, the **Chargeable Categories** tab will not be available.</span></span>

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a><span data-ttu-id="650f8-121">Обновление задачи проекта как оплачиваемой или не оплачиваемой</span><span class="sxs-lookup"><span data-stu-id="650f8-121">Update a project task as chargeable or non-chargeable</span></span>

<span data-ttu-id="650f8-122">Задача проекта может быть оплачиваемой или не оплачиваемой по конкретной строке контракта, что делает возможной следующую настройку:</span><span class="sxs-lookup"><span data-stu-id="650f8-122">A project task can be chargeable or non-chargeable on a specific contract line, which makes the following setup possible:</span></span>

<span data-ttu-id="650f8-123">Если строка контракта на основе проекта включает **Время** и определенная задача **T1** связана с ней как оплачиваемая.</span><span class="sxs-lookup"><span data-stu-id="650f8-123">If a project-based contract line includes **Time** and a certain task, **T1** is associated to it as chargeable.</span></span> <span data-ttu-id="650f8-124">Если есть вторая строка контракта, которая включает **Расходы**, вы можете связать задачу T1 в строке контракта как не оплачиваемую.</span><span class="sxs-lookup"><span data-stu-id="650f8-124">If there is a second contract line that includes **Expense**, you can associate the T1 task on the contract line as non-chargeable.</span></span> <span data-ttu-id="650f8-125">В результате все время, записанное на задачу, оплачивается, а все расходы — не оплачиваются.</span><span class="sxs-lookup"><span data-stu-id="650f8-125">The result is that all of the time recorded on the task is chargeable and all expenses are non-chargeable.</span></span>

<span data-ttu-id="650f8-126">Тип выставления счетов для задачи можно настроить на вкладке **Оплачиваемые задачи** строки контракта, обновив поле **Тип выставления счетов** во вложенной сетке задач строки контракта.</span><span class="sxs-lookup"><span data-stu-id="650f8-126">A task's billing type can be configured on the **Chargeable Tasks** tab of the contract line by updating the **Billing Type** field on the contract line tasks subgrid.</span></span> <span data-ttu-id="650f8-127">Кроме того, вы можете обновить поле **Тип выставления счетов** во вложенной сетке в настройке выставления счетов по задаче проекта, в которой отображаются строки контракта, связанные с задачей.</span><span class="sxs-lookup"><span data-stu-id="650f8-127">Alternatively, you can update the **Billing Type** field on the subgrid of the task Billing setup of a project that shows the contract lines associated to a task.</span></span>

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a><span data-ttu-id="650f8-128">Обновление роли как оплачиваемой или не оплачиваемой</span><span class="sxs-lookup"><span data-stu-id="650f8-128">Update a role as chargeable or non-chargeable</span></span>

<span data-ttu-id="650f8-129">Роль может быть оплачиваемой или неоплачиваемой по определенной строке контракта.</span><span class="sxs-lookup"><span data-stu-id="650f8-129">A role can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="650f8-130">Тип выставления счетов для роли можно настроить на вкладке **Оплачиваемые роли** строки контракта.</span><span class="sxs-lookup"><span data-stu-id="650f8-130">A role's billing type can be configured on the **Chargeable Roles** tab of a contract line.</span></span> <span data-ttu-id="650f8-131">Для этого обновите поле **Тип выставления счетов** во вложенной сетке **Оплачиваемые роли**.</span><span class="sxs-lookup"><span data-stu-id="650f8-131">To do this, update the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a><span data-ttu-id="650f8-132">Обновление категории транзакций как оплачиваемой или неоплачиваемой</span><span class="sxs-lookup"><span data-stu-id="650f8-132">Update a transaction category as chargeable or non-chargeable</span></span>

<span data-ttu-id="650f8-133">Категория транзакций может быть оплачиваемой или неоплачиваемой по определенной строке контракта.</span><span class="sxs-lookup"><span data-stu-id="650f8-133">A transaction category can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="650f8-134">Тип выставления счетов для транзакции можно настроить на вкладке **Оплачиваемые транзакции** строки контракта на основе проекта.</span><span class="sxs-lookup"><span data-stu-id="650f8-134">A transaction's billing type can be configured on the **Chargeable Categories** tab of a project-based contract line.</span></span> <span data-ttu-id="650f8-135">Для этого обновите поле **Тип выставления счетов** во вложенной сетке **Оплачиваемые категории**.</span><span class="sxs-lookup"><span data-stu-id="650f8-135">To do this, update the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="650f8-136">Разрешение возможности выставления счетов</span><span class="sxs-lookup"><span data-stu-id="650f8-136">Resolve chargeability</span></span>

<span data-ttu-id="650f8-137">Оценка или фактическое значение, созданное для времени, считается подлежащим оплате в том случае, если:</span><span class="sxs-lookup"><span data-stu-id="650f8-137">An estimate or actual created for time is only considered chargeable if:</span></span>

   - <span data-ttu-id="650f8-138">**Время** включено в строку контракта.</span><span class="sxs-lookup"><span data-stu-id="650f8-138">**Time** is included on the contract line.</span></span>
   - <span data-ttu-id="650f8-139">**Роль** настроена как подлежащая оплате в строке контракта.</span><span class="sxs-lookup"><span data-stu-id="650f8-139">**Role** is configured as chargeable on the contract line.</span></span>
   - <span data-ttu-id="650f8-140">**Включенные задачи** заданы как **Выбранные задачи** в строке контракта.</span><span class="sxs-lookup"><span data-stu-id="650f8-140">**Included Tasks** is set to **Selected tasks** on the contract line.</span></span>
 
 <span data-ttu-id="650f8-141">Если эти три условия верны, задача конфигурируется как подлежащая оплате.</span><span class="sxs-lookup"><span data-stu-id="650f8-141">If these three things are true, the task is configured as chargeable.</span></span> 

<span data-ttu-id="650f8-142">Оценка или фактическое значение, созданное для расходов, считается подлежащим оплате в том случае, если:</span><span class="sxs-lookup"><span data-stu-id="650f8-142">An estimate or actual created for expense is only considered chargeable if:</span></span>

   - <span data-ttu-id="650f8-143">**Расходы** включены в строку контракта</span><span class="sxs-lookup"><span data-stu-id="650f8-143">**Expense** is included on the contract line</span></span>
   - <span data-ttu-id="650f8-144">**Категория проводки** настроена как подлежащая оплате в строке контракта</span><span class="sxs-lookup"><span data-stu-id="650f8-144">**Transaction category** is configured as chargeable on the contract line</span></span>
   - <span data-ttu-id="650f8-145">**Включенные задачи** заданы как **Выбранная задача** в строке контракта</span><span class="sxs-lookup"><span data-stu-id="650f8-145">**Included Tasks** is set to **Selected task** on the contract line</span></span>
  
 <span data-ttu-id="650f8-146">Если эти три условия верны, **Задача** конфигурируется как подлежащая оплате.</span><span class="sxs-lookup"><span data-stu-id="650f8-146">If these three things are true, the **Task** is configured as chargeable.</span></span> 

<span data-ttu-id="650f8-147">Оценка или фактическое значение, созданное для материала, считается подлежащим оплате в том случае, если:</span><span class="sxs-lookup"><span data-stu-id="650f8-147">An estimate or actual created for material is only considered chargeable if:</span></span>

   - <span data-ttu-id="650f8-148">**Материалы** включены в строку контракта</span><span class="sxs-lookup"><span data-stu-id="650f8-148">**Materials** is included on the contract line</span></span>
   - <span data-ttu-id="650f8-149">**Включенные задачи** заданы как **Выбранные задачи** в строке контракта</span><span class="sxs-lookup"><span data-stu-id="650f8-149">**Included Tasks** is set to **Selected tasks** on the contract line</span></span>

<span data-ttu-id="650f8-150">Если эти два условия верны, **Задача** конфигурируется как подлежащая оплате.</span><span class="sxs-lookup"><span data-stu-id="650f8-150">If these two things are true, the **Task** is configured as chargeable.</span></span> 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="650f8-151">
                    <strong>Включает время</strong>
                </span><span class="sxs-lookup"><span data-stu-id="650f8-151">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="650f8-152">
                    <strong>Включает расходы</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="650f8-152">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="650f8-153">
                    <strong>Включить материалы</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="650f8-153">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="650f8-154">
                    <strong>Включенные задачи</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="650f8-154">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="650f8-155">
                    <strong>Роль</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="650f8-155">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="650f8-156">
                    <strong>Категория</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="650f8-156">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="650f8-157">
                    <strong>Задача</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="650f8-157">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="650f8-158">
                    <strong>Влияние возможности оплаты</strong>
                </span><span class="sxs-lookup"><span data-stu-id="650f8-158">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="650f8-159">Да</span><span class="sxs-lookup"><span data-stu-id="650f8-159">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="650f8-160">Да</span><span class="sxs-lookup"><span data-stu-id="650f8-160">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="650f8-161">Да</span><span class="sxs-lookup"><span data-stu-id="650f8-161">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="650f8-162">Весь проект</span><span class="sxs-lookup"><span data-stu-id="650f8-162">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="650f8-163">Оплачивается</span><span class="sxs-lookup"><span data-stu-id="650f8-163">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="650f8-164">Оплачивается</span><span class="sxs-lookup"><span data-stu-id="650f8-164">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="650f8-165">Не может быть установлено</span><span class="sxs-lookup"><span data-stu-id="650f8-165">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="650f8-166">Выставление счетов за фактическое время: <strong>Оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="650f8-166">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="650f8-167">Тип выставления счетов за фактические расходы: <strong>Оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="650f8-167">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="650f8-168">Тип выставления счетов за фактические материалы: <strong>Оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="650f8-168">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="650f8-169">Да</span><span class="sxs-lookup"><span data-stu-id="650f8-169">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="650f8-170">Да</span><span class="sxs-lookup"><span data-stu-id="650f8-170">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="650f8-171">Да</span><span class="sxs-lookup"><span data-stu-id="650f8-171">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="650f8-172">Только выбранные задачи</span><span class="sxs-lookup"><span data-stu-id="650f8-172">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="650f8-173">Оплачивается</span><span class="sxs-lookup"><span data-stu-id="650f8-173">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="650f8-174">Оплачивается</span><span class="sxs-lookup"><span data-stu-id="650f8-174">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="650f8-175">Оплачивается</span><span class="sxs-lookup"><span data-stu-id="650f8-175">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="650f8-176">Выставление счетов за фактическое время: <strong>Оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="650f8-176">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="650f8-177">Тип выставления счетов за фактические расходы: <strong>Оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="650f8-177">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="650f8-178">Тип выставления счетов за фактические материалы: <strong>Оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="650f8-178">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="650f8-179">Да</span><span class="sxs-lookup"><span data-stu-id="650f8-179">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="650f8-180">Да</span><span class="sxs-lookup"><span data-stu-id="650f8-180">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="650f8-181">Да</span><span class="sxs-lookup"><span data-stu-id="650f8-181">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="650f8-182">Только выбранные задачи</span><span class="sxs-lookup"><span data-stu-id="650f8-182">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="650f8-183">
                    <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="650f8-183">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="650f8-184">Оплачивается</span><span class="sxs-lookup"><span data-stu-id="650f8-184">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="650f8-185">Оплачивается</span><span class="sxs-lookup"><span data-stu-id="650f8-185">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="650f8-186">Выставления счетов за фактическое время: <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="650f8-186">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="650f8-187">Тип выставления счетов за фактические расходы: Оплачивается</span><span class="sxs-lookup"><span data-stu-id="650f8-187">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="650f8-188">Тип выставления счетов за фактические материалы: Оплачивается</span><span class="sxs-lookup"><span data-stu-id="650f8-188">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="650f8-189">Да</span><span class="sxs-lookup"><span data-stu-id="650f8-189">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="650f8-190">Да</span><span class="sxs-lookup"><span data-stu-id="650f8-190">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="650f8-191">Да</span><span class="sxs-lookup"><span data-stu-id="650f8-191">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="650f8-192">Только выбранные задачи</span><span class="sxs-lookup"><span data-stu-id="650f8-192">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="650f8-193">Оплачивается</span><span class="sxs-lookup"><span data-stu-id="650f8-193">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="650f8-194">Оплачивается</span><span class="sxs-lookup"><span data-stu-id="650f8-194">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="650f8-195">
                    <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="650f8-195">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="650f8-196">Выставления счетов за фактическое время: <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="650f8-196">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="650f8-197">Тип выставления счетов за фактические расходы: <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="650f8-197">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="650f8-198">Тип выставления счетов за фактические материалы: <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="650f8-198">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="650f8-199">Да</span><span class="sxs-lookup"><span data-stu-id="650f8-199">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="650f8-200">Да</span><span class="sxs-lookup"><span data-stu-id="650f8-200">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="650f8-201">Да</span><span class="sxs-lookup"><span data-stu-id="650f8-201">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="650f8-202">Только выбранные задачи</span><span class="sxs-lookup"><span data-stu-id="650f8-202">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="650f8-203">
                    <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="650f8-203">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="650f8-204">Оплачивается</span><span class="sxs-lookup"><span data-stu-id="650f8-204">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="650f8-205">
                    <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="650f8-205">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="650f8-206">Выставления счетов за фактическое время: <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="650f8-206">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="650f8-207">Тип выставления счетов за фактические расходы: <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="650f8-207">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="650f8-208">Тип выставления счетов за фактические материалы: <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="650f8-208">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="650f8-209">Да</span><span class="sxs-lookup"><span data-stu-id="650f8-209">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="650f8-210">Да</span><span class="sxs-lookup"><span data-stu-id="650f8-210">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="650f8-211">Да</span><span class="sxs-lookup"><span data-stu-id="650f8-211">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="650f8-212">Только выбранные задачи</span><span class="sxs-lookup"><span data-stu-id="650f8-212">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="650f8-213">
                    <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="650f8-213">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="650f8-214">
                    <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="650f8-214">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="650f8-215">Оплачивается</span><span class="sxs-lookup"><span data-stu-id="650f8-215">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="650f8-216">Выставления счетов за фактическое время: <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="650f8-216">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="650f8-217">Тип выставления счетов за фактические расходы: <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="650f8-217">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="650f8-218">Тип выставления счетов за фактические материалы: Оплачивается</span><span class="sxs-lookup"><span data-stu-id="650f8-218">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="650f8-219">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="650f8-219">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="650f8-220">Да</span><span class="sxs-lookup"><span data-stu-id="650f8-220">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="650f8-221">Да</span><span class="sxs-lookup"><span data-stu-id="650f8-221">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="650f8-222">Весь проект</span><span class="sxs-lookup"><span data-stu-id="650f8-222">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="650f8-223">Не может быть установлено</span><span class="sxs-lookup"><span data-stu-id="650f8-223">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="650f8-224">
                    <strong>Оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="650f8-224">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="650f8-225">Не может быть установлено</span><span class="sxs-lookup"><span data-stu-id="650f8-225">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="650f8-226">Выставления счетов за фактическое время: <strong>Недоступно</strong>
                </span><span class="sxs-lookup"><span data-stu-id="650f8-226">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="650f8-227">Тип выставления счетов за фактические расходы: Оплачивается</span><span class="sxs-lookup"><span data-stu-id="650f8-227">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="650f8-228">Тип выставления счетов за фактические материалы: Оплачивается</span><span class="sxs-lookup"><span data-stu-id="650f8-228">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="650f8-229">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="650f8-229">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="650f8-230">Да</span><span class="sxs-lookup"><span data-stu-id="650f8-230">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="650f8-231">Да</span><span class="sxs-lookup"><span data-stu-id="650f8-231">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="650f8-232">Весь проект</span><span class="sxs-lookup"><span data-stu-id="650f8-232">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="650f8-233">Не может быть установлено</span><span class="sxs-lookup"><span data-stu-id="650f8-233">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="650f8-234">
                    <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="650f8-234">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="650f8-235">Не может быть установлено</span><span class="sxs-lookup"><span data-stu-id="650f8-235">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="650f8-236">Выставления счетов за фактическое время: <strong>Недоступно</strong>
                </span><span class="sxs-lookup"><span data-stu-id="650f8-236">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="650f8-237">Тип выставления счетов за фактические расходы: <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="650f8-237">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="650f8-238">Тип выставления счетов за фактические материалы: Оплачивается</span><span class="sxs-lookup"><span data-stu-id="650f8-238">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="650f8-239">Да</span><span class="sxs-lookup"><span data-stu-id="650f8-239">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="650f8-240">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="650f8-240">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="650f8-241">Да</span><span class="sxs-lookup"><span data-stu-id="650f8-241">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="650f8-242">Весь проект</span><span class="sxs-lookup"><span data-stu-id="650f8-242">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="650f8-243">Оплачивается</span><span class="sxs-lookup"><span data-stu-id="650f8-243">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="650f8-244">Не может быть установлено</span><span class="sxs-lookup"><span data-stu-id="650f8-244">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="650f8-245">Не может быть установлено</span><span class="sxs-lookup"><span data-stu-id="650f8-245">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="650f8-246">Выставления счетов за фактическое время: Оплачивается</span><span class="sxs-lookup"><span data-stu-id="650f8-246">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="650f8-247">Тип выставления счетов за фактические расходы: <strong>Недоступно</strong>
                </span><span class="sxs-lookup"><span data-stu-id="650f8-247">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="650f8-248">Тип выставления счетов за фактические материалы: Оплачивается</span><span class="sxs-lookup"><span data-stu-id="650f8-248">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="650f8-249">Да</span><span class="sxs-lookup"><span data-stu-id="650f8-249">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="650f8-250">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="650f8-250">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="650f8-251">Да</span><span class="sxs-lookup"><span data-stu-id="650f8-251">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="650f8-252">Весь проект</span><span class="sxs-lookup"><span data-stu-id="650f8-252">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="650f8-253">
                    <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="650f8-253">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="650f8-254">Не может быть установлено</span><span class="sxs-lookup"><span data-stu-id="650f8-254">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="650f8-255">Не может быть установлено</span><span class="sxs-lookup"><span data-stu-id="650f8-255">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="650f8-256">Выставления счетов за фактическое время: <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="650f8-256">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="650f8-257">Тип выставления счетов за фактические расходы: <strong>Недоступно</strong>
                </span><span class="sxs-lookup"><span data-stu-id="650f8-257">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="650f8-258">Тип выставления счетов за фактические материалы: Оплачивается</span><span class="sxs-lookup"><span data-stu-id="650f8-258">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="650f8-259">Да</span><span class="sxs-lookup"><span data-stu-id="650f8-259">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="650f8-260">Да</span><span class="sxs-lookup"><span data-stu-id="650f8-260">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="650f8-261">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="650f8-261">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="650f8-262">Весь проект</span><span class="sxs-lookup"><span data-stu-id="650f8-262">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="650f8-263">Оплачивается</span><span class="sxs-lookup"><span data-stu-id="650f8-263">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="650f8-264">Оплачивается</span><span class="sxs-lookup"><span data-stu-id="650f8-264">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="650f8-265">Не может быть установлено</span><span class="sxs-lookup"><span data-stu-id="650f8-265">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="650f8-266">Выставления счетов за фактическое время: Оплачивается</span><span class="sxs-lookup"><span data-stu-id="650f8-266">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="650f8-267">Тип выставления счетов за фактические расходы: Оплачивается</span><span class="sxs-lookup"><span data-stu-id="650f8-267">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="650f8-268">Тип выставления счетов за фактические материалы: <strong>Недоступно</strong>
                </span><span class="sxs-lookup"><span data-stu-id="650f8-268">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="650f8-269">Да</span><span class="sxs-lookup"><span data-stu-id="650f8-269">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="650f8-270">Да</span><span class="sxs-lookup"><span data-stu-id="650f8-270">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="650f8-271">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="650f8-271">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="650f8-272">Весь проект</span><span class="sxs-lookup"><span data-stu-id="650f8-272">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="650f8-273">
                    <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="650f8-273">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="650f8-274">
                    <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="650f8-274">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="650f8-275">Не может быть установлено</span><span class="sxs-lookup"><span data-stu-id="650f8-275">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="650f8-276">Выставления счетов за фактическое время: <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="650f8-276">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="650f8-277">Тип выставления счетов за фактические расходы: <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="650f8-277">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="650f8-278">Тип выставления счетов за фактические материалы: <strong>Недоступно</strong>
                </span><span class="sxs-lookup"><span data-stu-id="650f8-278">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
