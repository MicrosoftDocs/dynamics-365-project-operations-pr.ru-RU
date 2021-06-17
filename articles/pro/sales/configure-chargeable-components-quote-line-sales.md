---
title: Настройка подлежащих оплате компонентов строки предложения с расценками
description: Эта тема предоставляет информацию о настройке оплачиваемых и неоплачиваемых компонентов в строке предложения с расценками на основе проекта.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c933a3800aae72624dbcbe3f06df20e5981d74d4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003782"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a><span data-ttu-id="4d74d-103">Настройка подлежащих оплате компонентов строки предложения с расценками</span><span class="sxs-lookup"><span data-stu-id="4d74d-103">Configure the chargeable components of a quote line</span></span> 

<span data-ttu-id="4d74d-104">_**Относится к:** Облегченное развертывание — от сделки до счетов-проформ, Project Operations для сценариев на основе ресурсов/нескладируемых запасов_</span><span class="sxs-lookup"><span data-stu-id="4d74d-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="4d74d-105">Строка предложения с расценками на основе проекта имеет концепцию *включенных* компонентов и *оплачиваемых* компонентов.</span><span class="sxs-lookup"><span data-stu-id="4d74d-105">A project-based quote line has the concept of *included* components and *chargeable* components.</span></span>

<span data-ttu-id="4d74d-106">Для включенных компонентов используются:</span><span class="sxs-lookup"><span data-stu-id="4d74d-106">Included components are subject to:</span></span>

  - <span data-ttu-id="4d74d-107">Метод выставления счетов и разделение клиентов</span><span class="sxs-lookup"><span data-stu-id="4d74d-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="4d74d-108">Максимальные лимиты</span><span class="sxs-lookup"><span data-stu-id="4d74d-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="4d74d-109">Настройки периодичности выставления счетов, определенные в строке предложения с расценками на основе проекта</span><span class="sxs-lookup"><span data-stu-id="4d74d-109">Invoice frequency settings defined on the project-based quote line</span></span>

<span data-ttu-id="4d74d-110">Подмножество включенных компонентов можно пометить как оплачиваемые с помощью поля **Тип выставления счетов**.</span><span class="sxs-lookup"><span data-stu-id="4d74d-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="4d74d-111">Поле **Тип выставления счетов** — это набор параметров, который позволяет использовать следующие значения в контексте строки предложения с расценками:</span><span class="sxs-lookup"><span data-stu-id="4d74d-111">The **Billing Type** field is an option-set that allows the following values in the context of a quote line:</span></span>

  - <span data-ttu-id="4d74d-112">Оплачивается</span><span class="sxs-lookup"><span data-stu-id="4d74d-112">Chargeable</span></span>
  - <span data-ttu-id="4d74d-113">Не оплачивается</span><span class="sxs-lookup"><span data-stu-id="4d74d-113">Non-chargeable</span></span>

<span data-ttu-id="4d74d-114">Оплачиваемые компоненты можно определить по задачам, ролям и категориям транзакций.</span><span class="sxs-lookup"><span data-stu-id="4d74d-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="4d74d-115">Возможность выставления счетов определяется для задач по строке предложения с расценками и применяется ко всем классам транзакций, включенным в эту строку.</span><span class="sxs-lookup"><span data-stu-id="4d74d-115">Chargeability is defined on the tasks for a quote line and applies to all transaction classes included on that line.</span></span> <span data-ttu-id="4d74d-116">Если поле **Включить задачи** имеет значение **Весь проект** или оставлено пустым, то вкладка **Оплачиваемые задачи** недоступна.</span><span class="sxs-lookup"><span data-stu-id="4d74d-116">If the **Include Tasks** field is set to **Entire project** or left blank, the **Chargeable Tasks** tab isn't available.</span></span>

<span data-ttu-id="4d74d-117">Возможность выставления счетов определяется для строки предложения с расценками и применяется только к классу транзакций **Время**.</span><span class="sxs-lookup"><span data-stu-id="4d74d-117">Chargeability is defined on roles for a quote line and only applies to the **Time** transaction class.</span></span> <span data-ttu-id="4d74d-118">Если поле **Включить время** имеет значение **Нет** в строке предложения с расценками по проекту, то вкладка **Оплачиваемые роли** недоступна.</span><span class="sxs-lookup"><span data-stu-id="4d74d-118">If the field, **Include Time** is set to **No** on a project quote line, the **Chargeable Roles** tab isn't available.</span></span>

<span data-ttu-id="4d74d-119">Возможность выставления счетов определяется для категорий транзакций в строке предложения с расценками и применяется только к классу транзакций **Расходы**.</span><span class="sxs-lookup"><span data-stu-id="4d74d-119">Chargeability is defined on transaction categories for a  quote line and only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="4d74d-120">Если поле **Включить расходы** имеет значение **Нет** в строке предложения с расценками по проекту, то вкладка **Оплачиваемые категории** недоступна.</span><span class="sxs-lookup"><span data-stu-id="4d74d-120">If the field, **Include Expenses** is set to **No** on a project quote line, the **Chargeable Categories** tab isn't available.</span></span>

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="4d74d-121">Обновление задачи проекта как оплачиваемой или неоплачиваемой</span><span class="sxs-lookup"><span data-stu-id="4d74d-121">Update a project task to be chargeable or non-chargeable</span></span>

<span data-ttu-id="4d74d-122">Задача проекта может быть оплачиваемой или неоплачиваемой в контексте конкретной строки предложения с расценками на основе проекта, что делает возможной следующую настройку.</span><span class="sxs-lookup"><span data-stu-id="4d74d-122">A project task can be chargeable or non-chargeable in the context of a specific project-based quote line, which makes the following setup possible.</span></span>

<span data-ttu-id="4d74d-123">Если строка предложения с расценками по проекту включает **Время** и задача **T1**, то задача связана со строкой предложения с расценками как оплачиваемая.</span><span class="sxs-lookup"><span data-stu-id="4d74d-123">If a project-based quote line includes **Time** and the task **T1**, the task is associated to the quote line as chargeable.</span></span> <span data-ttu-id="4d74d-124">Если есть вторая строка предложения с расценками, которая включает **Расходы**, вы можете связать задачу **T1** в строке предложения с расценками как неоплачиваемую.</span><span class="sxs-lookup"><span data-stu-id="4d74d-124">If there is a second quote line that includes **Expenses**, you can associate the **T1** task on the quote line as non-chargeable.</span></span> <span data-ttu-id="4d74d-125">В результате все время, записанное на задачу, оплачивается, а все расходы, записанные для задачи, — не оплачиваются.</span><span class="sxs-lookup"><span data-stu-id="4d74d-125">The result is that all time recorded on the task is chargeable and all expenses recorded on the task are non-chargeable.</span></span>

<span data-ttu-id="4d74d-126">Тип выставления счетов для задачи можно настроить на вкладке **Оплачиваемые задачи** строки предложения с расценками по проекту, обновив поле **Тип выставления счетов** во вложенной сетке **Задачи строки предложения с расценками**.</span><span class="sxs-lookup"><span data-stu-id="4d74d-126">A task's billing type can be configured on the **Chargeable Tasks** tab of a project-based quote line by updating the **Billing Type** field on the **Quote Line Tasks** subgrid.</span></span> <span data-ttu-id="4d74d-127">Кроме того, вы можете обновить тип выставления счетов для задачи проекта в поле **Тип выставления счетов** во вложенной сетке в настройке выставления счетов по задаче проекта, в которой отображаются строки предложения с расценками, связанные с задачей.</span><span class="sxs-lookup"><span data-stu-id="4d74d-127">Alternatively, you can update the billing type for a project task in the **Billing Type** field on the subgrid on the task billing setup of a project that shows the quote lines associated to a task.</span></span>

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="4d74d-128">Обновление роли как оплачиваемой или неоплачиваемой</span><span class="sxs-lookup"><span data-stu-id="4d74d-128">Update a role to be chargeable or non-chargeable</span></span>

<span data-ttu-id="4d74d-129">Роль может быть оплачиваемой или неоплачиваемой в контексте конкретной строки предложения с расценками по проекту.</span><span class="sxs-lookup"><span data-stu-id="4d74d-129">A role can be chargeable or non-chargeable in the context of a specific project-based quote line.</span></span>

<span data-ttu-id="4d74d-130">Тип выставления счетов для роли можно настроить на вкладке **Оплачиваемые роли** строки предложения с расценками, обновив поле **Тип выставления счетов** во вложенной сетке **Оплачиваемые роли**.</span><span class="sxs-lookup"><span data-stu-id="4d74d-130">A role's billing type can be configured on the **Chargeable Roles** tab of a quote line by updating the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="4d74d-131">Обновление категории транзакций как оплачиваемой или неоплачиваемой</span><span class="sxs-lookup"><span data-stu-id="4d74d-131">Update a transaction category to be chargeable or non-chargeable</span></span>

<span data-ttu-id="4d74d-132">Категория транзакций может быть оплачиваемой или неоплачиваемой по определенной строке предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="4d74d-132">A transaction category can be chargeable or non-chargeable on a specific quote line.</span></span>

<span data-ttu-id="4d74d-133">Тип выставления счетов для транзакции можно настроить на вкладке **Оплачиваемые категории** строки предложения с расценками, обновив поле **Тип выставления счетов** во вложенной сетке **Оплачиваемые категории**.</span><span class="sxs-lookup"><span data-stu-id="4d74d-133">A transaction's billing type can be configured on the **Chargeable Categories** tab of a quote line by updating the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="4d74d-134">Разрешение возможности выставления счетов</span><span class="sxs-lookup"><span data-stu-id="4d74d-134">Resolve chargeability</span></span>
<span data-ttu-id="4d74d-135">Оценка или фактическое значение, созданное для времени, будет считаться подлежащим оплате в том случае, если:</span><span class="sxs-lookup"><span data-stu-id="4d74d-135">An estimate or actual created for time will only be considered chargeable if:</span></span>

   - <span data-ttu-id="4d74d-136">**Время** включено в строку предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="4d74d-136">**Time** is included on the quote line.</span></span>
   - <span data-ttu-id="4d74d-137">**Роль** настроена как подлежащая оплате в строке предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="4d74d-137">**Role** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="4d74d-138">**Включенные задачи** заданы как **Выбранные задачи** в строке предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="4d74d-138">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span> 

<span data-ttu-id="4d74d-139">Если эти три условия верны, **Задача** также конфигурируется как подлежащая оплате.</span><span class="sxs-lookup"><span data-stu-id="4d74d-139">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="4d74d-140">Оценка или фактическое значение, созданное для расходов, считается подлежащим оплате в том случае, если:</span><span class="sxs-lookup"><span data-stu-id="4d74d-140">An estimate or actual created for expense is only considered chargeable if:</span></span> 

   - <span data-ttu-id="4d74d-141">**Расходы** включены в строку предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="4d74d-141">**Expense** is included on the quote line.</span></span>
   - <span data-ttu-id="4d74d-142">**Категория проводки** настроена как подлежащая оплате в строке предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="4d74d-142">**Transaction category** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="4d74d-143">**Включенные задачи** заданы как **Выбранные задачи** в строке предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="4d74d-143">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="4d74d-144">Если эти три условия верны, **Задача** также конфигурируется как подлежащая оплате.</span><span class="sxs-lookup"><span data-stu-id="4d74d-144">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="4d74d-145">Оценка или фактическое значение, созданное для материала, будет считаться подлежащим оплате в том случае, если:</span><span class="sxs-lookup"><span data-stu-id="4d74d-145">An estimate or actual created for material will only be considered chargeable if:</span></span>

   - <span data-ttu-id="4d74d-146">**Материалы** включены в строку предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="4d74d-146">**Materials** is included on the quote line.</span></span>
   - <span data-ttu-id="4d74d-147">**Включенные задачи** заданы как **Выбранные задачи** в строке предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="4d74d-147">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="4d74d-148">Если эти два условия верны, **Задача** также должна быть настроена как подлежащая оплате.</span><span class="sxs-lookup"><span data-stu-id="4d74d-148">If these two things are true, the **Task** should also be configured as chargeable.</span></span> 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="4d74d-149">
                    <strong>Включает время</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4d74d-149">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="4d74d-150">
                    <strong>Включает расходы</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="4d74d-150">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="4d74d-151">
                    <strong>Включить материалы</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="4d74d-151">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="4d74d-152">
                    <strong>Включенные задачи</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="4d74d-152">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="4d74d-153">
                    <strong>Роль</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="4d74d-153">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="4d74d-154">
                    <strong>Категория</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="4d74d-154">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="4d74d-155">
                    <strong>Задача</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="4d74d-155">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="4d74d-156">
                    <strong>Влияние возможности оплаты</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4d74d-156">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="4d74d-157">Да</span><span class="sxs-lookup"><span data-stu-id="4d74d-157">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="4d74d-158">Да</span><span class="sxs-lookup"><span data-stu-id="4d74d-158">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="4d74d-159">Да</span><span class="sxs-lookup"><span data-stu-id="4d74d-159">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="4d74d-160">Весь проект</span><span class="sxs-lookup"><span data-stu-id="4d74d-160">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4d74d-161">Оплачивается</span><span class="sxs-lookup"><span data-stu-id="4d74d-161">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="4d74d-162">Оплачивается</span><span class="sxs-lookup"><span data-stu-id="4d74d-162">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4d74d-163">Не может быть задано</span><span class="sxs-lookup"><span data-stu-id="4d74d-163">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="4d74d-164">Выставления счетов за фактическое время: Оплачивается</span><span class="sxs-lookup"><span data-stu-id="4d74d-164">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="4d74d-165">Тип выставления счетов за фактические расходы: Оплачивается</span><span class="sxs-lookup"><span data-stu-id="4d74d-165">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="4d74d-166">Тип выставления счетов за фактические материалы: Оплачивается</span><span class="sxs-lookup"><span data-stu-id="4d74d-166">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="4d74d-167">Да</span><span class="sxs-lookup"><span data-stu-id="4d74d-167">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="4d74d-168">Да</span><span class="sxs-lookup"><span data-stu-id="4d74d-168">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="4d74d-169">Да</span><span class="sxs-lookup"><span data-stu-id="4d74d-169">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="4d74d-170">Только выбранные задачи</span><span class="sxs-lookup"><span data-stu-id="4d74d-170">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4d74d-171">Оплачивается</span><span class="sxs-lookup"><span data-stu-id="4d74d-171">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="4d74d-172">Оплачивается</span><span class="sxs-lookup"><span data-stu-id="4d74d-172">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4d74d-173">Оплачивается</span><span class="sxs-lookup"><span data-stu-id="4d74d-173">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="4d74d-174">Выставления счетов за фактическое время: Оплачивается</span><span class="sxs-lookup"><span data-stu-id="4d74d-174">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="4d74d-175">Тип выставления счетов за фактические расходы: Оплачивается</span><span class="sxs-lookup"><span data-stu-id="4d74d-175">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="4d74d-176">Тип выставления счетов за фактические материалы: Оплачивается</span><span class="sxs-lookup"><span data-stu-id="4d74d-176">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="4d74d-177">Да</span><span class="sxs-lookup"><span data-stu-id="4d74d-177">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="4d74d-178">Да</span><span class="sxs-lookup"><span data-stu-id="4d74d-178">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="4d74d-179">Да</span><span class="sxs-lookup"><span data-stu-id="4d74d-179">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="4d74d-180">Только выбранные задачи</span><span class="sxs-lookup"><span data-stu-id="4d74d-180">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="4d74d-181">
                    <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4d74d-181">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="4d74d-182">Оплачивается</span><span class="sxs-lookup"><span data-stu-id="4d74d-182">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4d74d-183">Оплачивается</span><span class="sxs-lookup"><span data-stu-id="4d74d-183">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="4d74d-184">Выставления счетов за фактическое время: <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4d74d-184">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="4d74d-185">Тип выставления счетов за фактические расходы: Оплачивается</span><span class="sxs-lookup"><span data-stu-id="4d74d-185">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="4d74d-186">Тип выставления счетов за фактические материалы: Оплачивается</span><span class="sxs-lookup"><span data-stu-id="4d74d-186">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="4d74d-187">Да</span><span class="sxs-lookup"><span data-stu-id="4d74d-187">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="4d74d-188">Да</span><span class="sxs-lookup"><span data-stu-id="4d74d-188">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="4d74d-189">Да</span><span class="sxs-lookup"><span data-stu-id="4d74d-189">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="4d74d-190">Только выбранные задачи</span><span class="sxs-lookup"><span data-stu-id="4d74d-190">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4d74d-191">Оплачивается</span><span class="sxs-lookup"><span data-stu-id="4d74d-191">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="4d74d-192">Оплачивается</span><span class="sxs-lookup"><span data-stu-id="4d74d-192">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="4d74d-193">
                    <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4d74d-193">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="4d74d-194">Выставления счетов за фактическое время: <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4d74d-194">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="4d74d-195">Тип выставления счетов за фактические расходы: <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4d74d-195">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="4d74d-196">Тип выставления счетов за фактические материалы: <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4d74d-196">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="4d74d-197">Да</span><span class="sxs-lookup"><span data-stu-id="4d74d-197">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="4d74d-198">Да</span><span class="sxs-lookup"><span data-stu-id="4d74d-198">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="4d74d-199">Да</span><span class="sxs-lookup"><span data-stu-id="4d74d-199">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="4d74d-200">Только выбранные задачи</span><span class="sxs-lookup"><span data-stu-id="4d74d-200">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="4d74d-201">
                    <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4d74d-201">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="4d74d-202">Оплачивается</span><span class="sxs-lookup"><span data-stu-id="4d74d-202">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="4d74d-203">
                    <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4d74d-203">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="4d74d-204">Выставления счетов за фактическое время: <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4d74d-204">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="4d74d-205">Тип выставления счетов за фактические расходы: <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4d74d-205">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="4d74d-206">Тип выставления счетов за фактические материалы: <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4d74d-206">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="4d74d-207">Да</span><span class="sxs-lookup"><span data-stu-id="4d74d-207">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="4d74d-208">Да</span><span class="sxs-lookup"><span data-stu-id="4d74d-208">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="4d74d-209">Да</span><span class="sxs-lookup"><span data-stu-id="4d74d-209">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="4d74d-210">Только выбранные задачи</span><span class="sxs-lookup"><span data-stu-id="4d74d-210">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="4d74d-211">
                    <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4d74d-211">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="4d74d-212">
                    <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4d74d-212">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4d74d-213">Оплачивается</span><span class="sxs-lookup"><span data-stu-id="4d74d-213">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="4d74d-214">Выставления счетов за фактическое время: <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4d74d-214">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="4d74d-215">Тип выставления счетов за фактические расходы: <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4d74d-215">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="4d74d-216">Тип выставления счетов за фактические материалы: Оплачивается</span><span class="sxs-lookup"><span data-stu-id="4d74d-216">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="4d74d-217">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4d74d-217">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="4d74d-218">Да</span><span class="sxs-lookup"><span data-stu-id="4d74d-218">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="4d74d-219">Да</span><span class="sxs-lookup"><span data-stu-id="4d74d-219">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="4d74d-220">Весь проект</span><span class="sxs-lookup"><span data-stu-id="4d74d-220">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4d74d-221">Не может быть задано</span><span class="sxs-lookup"><span data-stu-id="4d74d-221">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="4d74d-222">
                    <strong>Оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4d74d-222">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4d74d-223">Не может быть задано</span><span class="sxs-lookup"><span data-stu-id="4d74d-223">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="4d74d-224">Выставления счетов за фактическое время: <strong>Недоступно</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4d74d-224">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="4d74d-225">Тип выставления счетов за фактические расходы: Оплачивается</span><span class="sxs-lookup"><span data-stu-id="4d74d-225">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="4d74d-226">Тип выставления счетов за фактические материалы: Оплачивается</span><span class="sxs-lookup"><span data-stu-id="4d74d-226">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="4d74d-227">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4d74d-227">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="4d74d-228">Да</span><span class="sxs-lookup"><span data-stu-id="4d74d-228">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="4d74d-229">Да</span><span class="sxs-lookup"><span data-stu-id="4d74d-229">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="4d74d-230">Весь проект</span><span class="sxs-lookup"><span data-stu-id="4d74d-230">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4d74d-231">Не может быть задано</span><span class="sxs-lookup"><span data-stu-id="4d74d-231">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="4d74d-232">
                    <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4d74d-232">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4d74d-233">Не может быть задано</span><span class="sxs-lookup"><span data-stu-id="4d74d-233">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="4d74d-234">Выставления счетов за фактическое время: <strong>Недоступно</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4d74d-234">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="4d74d-235">Тип выставления счетов за фактические расходы: <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4d74d-235">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="4d74d-236">Тип выставления счетов за фактические материалы: Оплачивается</span><span class="sxs-lookup"><span data-stu-id="4d74d-236">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="4d74d-237">Да</span><span class="sxs-lookup"><span data-stu-id="4d74d-237">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="4d74d-238">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4d74d-238">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="4d74d-239">Да</span><span class="sxs-lookup"><span data-stu-id="4d74d-239">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="4d74d-240">Весь проект</span><span class="sxs-lookup"><span data-stu-id="4d74d-240">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4d74d-241">Оплачивается</span><span class="sxs-lookup"><span data-stu-id="4d74d-241">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="4d74d-242">Не может быть задано</span><span class="sxs-lookup"><span data-stu-id="4d74d-242">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4d74d-243">Не может быть задано</span><span class="sxs-lookup"><span data-stu-id="4d74d-243">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="4d74d-244">Выставления счетов за фактическое время: Оплачивается</span><span class="sxs-lookup"><span data-stu-id="4d74d-244">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="4d74d-245">Тип выставления счетов за фактические расходы: <strong>Недоступно</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4d74d-245">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="4d74d-246">Тип выставления счетов за фактические материалы: Оплачивается</span><span class="sxs-lookup"><span data-stu-id="4d74d-246">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="4d74d-247">Да</span><span class="sxs-lookup"><span data-stu-id="4d74d-247">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="4d74d-248">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4d74d-248">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="4d74d-249">Да</span><span class="sxs-lookup"><span data-stu-id="4d74d-249">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="4d74d-250">Весь проект</span><span class="sxs-lookup"><span data-stu-id="4d74d-250">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="4d74d-251">
                    <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4d74d-251">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="4d74d-252">Не может быть задано</span><span class="sxs-lookup"><span data-stu-id="4d74d-252">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4d74d-253">Не может быть задано</span><span class="sxs-lookup"><span data-stu-id="4d74d-253">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="4d74d-254">Выставления счетов за фактическое время: <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4d74d-254">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="4d74d-255">Тип выставления счетов за фактические расходы: <strong>Недоступно</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4d74d-255">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="4d74d-256">Тип выставления счетов за фактические материалы: Оплачивается</span><span class="sxs-lookup"><span data-stu-id="4d74d-256">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="4d74d-257">Да</span><span class="sxs-lookup"><span data-stu-id="4d74d-257">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="4d74d-258">Да</span><span class="sxs-lookup"><span data-stu-id="4d74d-258">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="4d74d-259">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4d74d-259">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="4d74d-260">Весь проект</span><span class="sxs-lookup"><span data-stu-id="4d74d-260">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4d74d-261">Оплачивается</span><span class="sxs-lookup"><span data-stu-id="4d74d-261">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="4d74d-262">Оплачивается</span><span class="sxs-lookup"><span data-stu-id="4d74d-262">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4d74d-263">Не может быть задано</span><span class="sxs-lookup"><span data-stu-id="4d74d-263">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="4d74d-264">Выставления счетов за фактическое время: Оплачивается</span><span class="sxs-lookup"><span data-stu-id="4d74d-264">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="4d74d-265">Тип выставления счетов за фактические расходы: Оплачивается</span><span class="sxs-lookup"><span data-stu-id="4d74d-265">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="4d74d-266">Тип выставления счетов за фактические материалы: <strong>Недоступно</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4d74d-266">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="4d74d-267">Да</span><span class="sxs-lookup"><span data-stu-id="4d74d-267">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="4d74d-268">Да</span><span class="sxs-lookup"><span data-stu-id="4d74d-268">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="4d74d-269">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4d74d-269">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="4d74d-270">Весь проект</span><span class="sxs-lookup"><span data-stu-id="4d74d-270">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="4d74d-271">
                    <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4d74d-271">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="4d74d-272">
                    <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4d74d-272">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="4d74d-273">Не может быть задано</span><span class="sxs-lookup"><span data-stu-id="4d74d-273">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="4d74d-274">Выставления счетов за фактическое время: <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4d74d-274">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="4d74d-275">Тип выставления счетов за фактические расходы: <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4d74d-275">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="4d74d-276">Тип выставления счетов за фактические материалы: <strong>Недоступно</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4d74d-276">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
