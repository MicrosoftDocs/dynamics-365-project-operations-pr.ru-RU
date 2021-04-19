---
title: Настройка подлежащих оплате компонентов строки предложения с расценками
description: Эта тема предоставляет информацию о настройке оплачиваемых и неоплачиваемых компонентов в строке предложения с расценками на основе проекта.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1a9e1851bd8c5a4070df2774c945d1f3eabaaa8a
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858309"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a><span data-ttu-id="50d48-103">Настройка подлежащих оплате компонентов строки предложения с расценками</span><span class="sxs-lookup"><span data-stu-id="50d48-103">Configure the chargeable components of a quote line</span></span> 

<span data-ttu-id="50d48-104">_**Относится к:** Облегченное развертывание — от сделки до счетов-проформ, Project Operations для сценариев на основе ресурсов/нескладируемых запасов_</span><span class="sxs-lookup"><span data-stu-id="50d48-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="50d48-105">Строка предложения с расценками на основе проекта имеет концепцию *включенных* компонентов и *оплачиваемых* компонентов.</span><span class="sxs-lookup"><span data-stu-id="50d48-105">A project-based quote line has the concept of *included* components and *chargeable* components.</span></span>

<span data-ttu-id="50d48-106">Для включенных компонентов используются:</span><span class="sxs-lookup"><span data-stu-id="50d48-106">Included components are subject to:</span></span>

  - <span data-ttu-id="50d48-107">Метод выставления счетов и разделение клиентов</span><span class="sxs-lookup"><span data-stu-id="50d48-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="50d48-108">Максимальные лимиты</span><span class="sxs-lookup"><span data-stu-id="50d48-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="50d48-109">Настройки периодичности выставления счетов, определенные в строке предложения с расценками на основе проекта</span><span class="sxs-lookup"><span data-stu-id="50d48-109">Invoice frequency settings defined on the project-based quote line</span></span>

<span data-ttu-id="50d48-110">Подмножество включенных компонентов можно пометить как оплачиваемые с помощью поля **Тип выставления счетов**.</span><span class="sxs-lookup"><span data-stu-id="50d48-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="50d48-111">Поле **Тип выставления счетов** — это набор параметров, который позволяет использовать следующие значения в контексте строки предложения с расценками:</span><span class="sxs-lookup"><span data-stu-id="50d48-111">The **Billing Type** field is an option-set that allows the following values in the context of a quote line:</span></span>

  - <span data-ttu-id="50d48-112">Оплачивается</span><span class="sxs-lookup"><span data-stu-id="50d48-112">Chargeable</span></span>
  - <span data-ttu-id="50d48-113">Не оплачивается</span><span class="sxs-lookup"><span data-stu-id="50d48-113">Non-chargeable</span></span>

<span data-ttu-id="50d48-114">Оплачиваемые компоненты можно определить по задачам, ролям и категориям транзакций.</span><span class="sxs-lookup"><span data-stu-id="50d48-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="50d48-115">Возможность выставления счетов определяется для задач по строке предложения с расценками и применяется ко всем классам транзакций, включенным в эту строку.</span><span class="sxs-lookup"><span data-stu-id="50d48-115">Chargeability is defined on the tasks for a quote line and applies to all transaction classes included on that line.</span></span> <span data-ttu-id="50d48-116">Если поле **Включить задачи** имеет значение **Весь проект** или оставлено пустым, то вкладка **Оплачиваемые задачи** недоступна.</span><span class="sxs-lookup"><span data-stu-id="50d48-116">If the **Include Tasks** field is set to **Entire project** or left blank, the **Chargeable Tasks** tab isn't available.</span></span>

<span data-ttu-id="50d48-117">Возможность выставления счетов определяется для строки предложения с расценками и применяется только к классу транзакций **Время**.</span><span class="sxs-lookup"><span data-stu-id="50d48-117">Chargeability is defined on roles for a quote line and only applies to the **Time** transaction class.</span></span> <span data-ttu-id="50d48-118">Если поле **Включить время** имеет значение **Нет** в строке предложения с расценками по проекту, то вкладка **Оплачиваемые роли** недоступна.</span><span class="sxs-lookup"><span data-stu-id="50d48-118">If the field, **Include Time** is set to **No** on a project quote line, the **Chargeable Roles** tab isn't available.</span></span>

<span data-ttu-id="50d48-119">Возможность выставления счетов определяется для категорий транзакций в строке предложения с расценками и применяется только к классу транзакций **Расходы**.</span><span class="sxs-lookup"><span data-stu-id="50d48-119">Chargeability is defined on transaction categories for a  quote line and only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="50d48-120">Если поле **Включить расходы** имеет значение **Нет** в строке предложения с расценками по проекту, то вкладка **Оплачиваемые категории** недоступна.</span><span class="sxs-lookup"><span data-stu-id="50d48-120">If the field, **Include Expenses** is set to **No** on a project quote line, the **Chargeable Categories** tab isn't available.</span></span>

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="50d48-121">Обновление задачи проекта как оплачиваемой или неоплачиваемой</span><span class="sxs-lookup"><span data-stu-id="50d48-121">Update a project task to be chargeable or non-chargeable</span></span>

<span data-ttu-id="50d48-122">Задача проекта может быть оплачиваемой или неоплачиваемой в контексте конкретной строки предложения с расценками на основе проекта, что делает возможной следующую настройку.</span><span class="sxs-lookup"><span data-stu-id="50d48-122">A project task can be chargeable or non-chargeable in the context of a specific project-based quote line, which makes the following setup possible.</span></span>

<span data-ttu-id="50d48-123">Если строка предложения с расценками по проекту включает **Время** и задача **T1**, то задача связана со строкой предложения с расценками как оплачиваемая.</span><span class="sxs-lookup"><span data-stu-id="50d48-123">If a project-based quote line includes **Time** and the task **T1**, the task is associated to the quote line as chargeable.</span></span> <span data-ttu-id="50d48-124">Если есть вторая строка предложения с расценками, которая включает **Расходы**, вы можете связать задачу **T1** в строке предложения с расценками как неоплачиваемую.</span><span class="sxs-lookup"><span data-stu-id="50d48-124">If there is a second quote line that includes **Expenses**, you can associate the **T1** task on the quote line as non-chargeable.</span></span> <span data-ttu-id="50d48-125">В результате все время, записанное на задачу, оплачивается, а все расходы, записанные для задачи, — не оплачиваются.</span><span class="sxs-lookup"><span data-stu-id="50d48-125">The result is that all time recorded on the task is chargeable and all expenses recorded on the task are non-chargeable.</span></span>

<span data-ttu-id="50d48-126">Тип выставления счетов для задачи можно настроить на вкладке **Оплачиваемые задачи** строки предложения с расценками по проекту, обновив поле **Тип выставления счетов** во вложенной сетке **Задачи строки предложения с расценками**.</span><span class="sxs-lookup"><span data-stu-id="50d48-126">A task's billing type can be configured on the **Chargeable Tasks** tab of a project-based quote line by updating the **Billing Type** field on the **Quote Line Tasks** subgrid.</span></span> <span data-ttu-id="50d48-127">Кроме того, вы можете обновить тип выставления счетов для задачи проекта в поле **Тип выставления счетов** во вложенной сетке в настройке выставления счетов по задаче проекта, в которой отображаются строки предложения с расценками, связанные с задачей.</span><span class="sxs-lookup"><span data-stu-id="50d48-127">Alternatively, you can update the billing type for a project task in the **Billing Type** field on the subgrid on the task billing setup of a project that shows the quote lines associated to a task.</span></span>

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="50d48-128">Обновление роли как оплачиваемой или неоплачиваемой</span><span class="sxs-lookup"><span data-stu-id="50d48-128">Update a role to be chargeable or non-chargeable</span></span>

<span data-ttu-id="50d48-129">Роль может быть оплачиваемой или неоплачиваемой в контексте конкретной строки предложения с расценками по проекту.</span><span class="sxs-lookup"><span data-stu-id="50d48-129">A role can be chargeable or non-chargeable in the context of a specific project-based quote line.</span></span>

<span data-ttu-id="50d48-130">Тип выставления счетов для роли можно настроить на вкладке **Оплачиваемые роли** строки предложения с расценками, обновив поле **Тип выставления счетов** во вложенной сетке **Оплачиваемые роли**.</span><span class="sxs-lookup"><span data-stu-id="50d48-130">A role's billing type can be configured on the **Chargeable Roles** tab of a quote line by updating the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="50d48-131">Обновление категории транзакций как оплачиваемой или неоплачиваемой</span><span class="sxs-lookup"><span data-stu-id="50d48-131">Update a transaction category to be chargeable or non-chargeable</span></span>

<span data-ttu-id="50d48-132">Категория транзакций может быть оплачиваемой или неоплачиваемой по определенной строке предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="50d48-132">A transaction category can be chargeable or non-chargeable on a specific quote line.</span></span>

<span data-ttu-id="50d48-133">Тип выставления счетов для транзакции можно настроить на вкладке **Оплачиваемые категории** строки предложения с расценками, обновив поле **Тип выставления счетов** во вложенной сетке **Оплачиваемые категории**.</span><span class="sxs-lookup"><span data-stu-id="50d48-133">A transaction's billing type can be configured on the **Chargeable Categories** tab of a quote line by updating the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="50d48-134">Разрешение возможности выставления счетов</span><span class="sxs-lookup"><span data-stu-id="50d48-134">Resolve chargeability</span></span>
<span data-ttu-id="50d48-135">Оценка или фактическое значение, созданное для времени, будет считаться подлежащим оплате в том случае, если:</span><span class="sxs-lookup"><span data-stu-id="50d48-135">An estimate or actual created for time will only be considered chargeable if:</span></span>

   - <span data-ttu-id="50d48-136">**Время** включено в строку предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="50d48-136">**Time** is included on the quote line.</span></span>
   - <span data-ttu-id="50d48-137">**Роль** настроена как подлежащая оплате в строке предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="50d48-137">**Role** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="50d48-138">**Включенные задачи** заданы как **Выбранные задачи** в строке предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="50d48-138">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span> 

<span data-ttu-id="50d48-139">Если эти три условия верны, **Задача** также конфигурируется как подлежащая оплате.</span><span class="sxs-lookup"><span data-stu-id="50d48-139">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="50d48-140">Оценка или фактическое значение, созданное для расходов, считается подлежащим оплате в том случае, если:</span><span class="sxs-lookup"><span data-stu-id="50d48-140">An estimate or actual created for expense is only considered chargeable if:</span></span> 

   - <span data-ttu-id="50d48-141">**Расходы** включены в строку предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="50d48-141">**Expense** is included on the quote line.</span></span>
   - <span data-ttu-id="50d48-142">**Категория проводки** настроена как подлежащая оплате в строке предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="50d48-142">**Transaction category** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="50d48-143">**Включенные задачи** заданы как **Выбранные задачи** в строке предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="50d48-143">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="50d48-144">Если эти три условия верны, **Задача** также конфигурируется как подлежащая оплате.</span><span class="sxs-lookup"><span data-stu-id="50d48-144">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="50d48-145">Оценка или фактическое значение, созданное для материала, будет считаться подлежащим оплате в том случае, если:</span><span class="sxs-lookup"><span data-stu-id="50d48-145">An estimate or actual created for material will only be considered chargeable if:</span></span>

   - <span data-ttu-id="50d48-146">**Материалы** включены в строку предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="50d48-146">**Materials** is included on the quote line.</span></span>
   - <span data-ttu-id="50d48-147">**Включенные задачи** заданы как **Выбранные задачи** в строке предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="50d48-147">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="50d48-148">Если эти два условия верны, **Задача** также должна быть настроена как подлежащая оплате.</span><span class="sxs-lookup"><span data-stu-id="50d48-148">If these two things are true, the **Task** should also be configured as chargeable.</span></span> 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="50d48-149">
                    <strong>Включает время</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50d48-149">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="50d48-150">
                    <strong>Включает расходы</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="50d48-150">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="50d48-151">
                    <strong>Включить материалы</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="50d48-151">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="50d48-152">
                    <strong>Включенные задачи</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="50d48-152">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="50d48-153">
                    <strong>Роль</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="50d48-153">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="50d48-154">
                    <strong>Категория</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="50d48-154">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="50d48-155">
                    <strong>Задача</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="50d48-155">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="50d48-156">
                    <strong>Влияние возможности оплаты</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50d48-156">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="50d48-157">Да</span><span class="sxs-lookup"><span data-stu-id="50d48-157">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="50d48-158">Да</span><span class="sxs-lookup"><span data-stu-id="50d48-158">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="50d48-159">Да</span><span class="sxs-lookup"><span data-stu-id="50d48-159">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="50d48-160">Весь проект</span><span class="sxs-lookup"><span data-stu-id="50d48-160">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="50d48-161">Оплачивается</span><span class="sxs-lookup"><span data-stu-id="50d48-161">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="50d48-162">Оплачивается</span><span class="sxs-lookup"><span data-stu-id="50d48-162">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="50d48-163">Не может быть задано</span><span class="sxs-lookup"><span data-stu-id="50d48-163">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="50d48-164">Выставления счетов за фактическое время: Оплачивается</span><span class="sxs-lookup"><span data-stu-id="50d48-164">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="50d48-165">Тип выставления счетов за фактические расходы: Оплачивается</span><span class="sxs-lookup"><span data-stu-id="50d48-165">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="50d48-166">Тип выставления счетов за фактические материалы: Оплачивается</span><span class="sxs-lookup"><span data-stu-id="50d48-166">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="50d48-167">Да</span><span class="sxs-lookup"><span data-stu-id="50d48-167">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="50d48-168">Да</span><span class="sxs-lookup"><span data-stu-id="50d48-168">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="50d48-169">Да</span><span class="sxs-lookup"><span data-stu-id="50d48-169">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="50d48-170">Только выбранные задачи</span><span class="sxs-lookup"><span data-stu-id="50d48-170">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="50d48-171">Оплачивается</span><span class="sxs-lookup"><span data-stu-id="50d48-171">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="50d48-172">Оплачивается</span><span class="sxs-lookup"><span data-stu-id="50d48-172">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="50d48-173">Оплачивается</span><span class="sxs-lookup"><span data-stu-id="50d48-173">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="50d48-174">Выставления счетов за фактическое время: Оплачивается</span><span class="sxs-lookup"><span data-stu-id="50d48-174">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="50d48-175">Тип выставления счетов за фактические расходы: Оплачивается</span><span class="sxs-lookup"><span data-stu-id="50d48-175">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="50d48-176">Тип выставления счетов за фактические материалы: Оплачивается</span><span class="sxs-lookup"><span data-stu-id="50d48-176">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="50d48-177">Да</span><span class="sxs-lookup"><span data-stu-id="50d48-177">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="50d48-178">Да</span><span class="sxs-lookup"><span data-stu-id="50d48-178">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="50d48-179">Да</span><span class="sxs-lookup"><span data-stu-id="50d48-179">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="50d48-180">Только выбранные задачи</span><span class="sxs-lookup"><span data-stu-id="50d48-180">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="50d48-181">
                    <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50d48-181">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="50d48-182">Оплачивается</span><span class="sxs-lookup"><span data-stu-id="50d48-182">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="50d48-183">Оплачивается</span><span class="sxs-lookup"><span data-stu-id="50d48-183">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="50d48-184">Выставления счетов за фактическое время: <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50d48-184">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="50d48-185">Тип выставления счетов за фактические расходы: Оплачивается</span><span class="sxs-lookup"><span data-stu-id="50d48-185">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="50d48-186">Тип выставления счетов за фактические материалы: Оплачивается</span><span class="sxs-lookup"><span data-stu-id="50d48-186">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="50d48-187">Да</span><span class="sxs-lookup"><span data-stu-id="50d48-187">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="50d48-188">Да</span><span class="sxs-lookup"><span data-stu-id="50d48-188">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="50d48-189">Да</span><span class="sxs-lookup"><span data-stu-id="50d48-189">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="50d48-190">Только выбранные задачи</span><span class="sxs-lookup"><span data-stu-id="50d48-190">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="50d48-191">Оплачивается</span><span class="sxs-lookup"><span data-stu-id="50d48-191">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="50d48-192">Оплачивается</span><span class="sxs-lookup"><span data-stu-id="50d48-192">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="50d48-193">
                    <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50d48-193">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="50d48-194">Выставления счетов за фактическое время: <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50d48-194">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="50d48-195">Тип выставления счетов за фактические расходы: <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50d48-195">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="50d48-196">Тип выставления счетов за фактические материалы: <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50d48-196">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="50d48-197">Да</span><span class="sxs-lookup"><span data-stu-id="50d48-197">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="50d48-198">Да</span><span class="sxs-lookup"><span data-stu-id="50d48-198">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="50d48-199">Да</span><span class="sxs-lookup"><span data-stu-id="50d48-199">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="50d48-200">Только выбранные задачи</span><span class="sxs-lookup"><span data-stu-id="50d48-200">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="50d48-201">
                    <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50d48-201">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="50d48-202">Оплачивается</span><span class="sxs-lookup"><span data-stu-id="50d48-202">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="50d48-203">
                    <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50d48-203">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="50d48-204">Выставления счетов за фактическое время: <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50d48-204">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="50d48-205">Тип выставления счетов за фактические расходы: <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50d48-205">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="50d48-206">Тип выставления счетов за фактические материалы: <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50d48-206">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="50d48-207">Да</span><span class="sxs-lookup"><span data-stu-id="50d48-207">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="50d48-208">Да</span><span class="sxs-lookup"><span data-stu-id="50d48-208">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="50d48-209">Да</span><span class="sxs-lookup"><span data-stu-id="50d48-209">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="50d48-210">Только выбранные задачи</span><span class="sxs-lookup"><span data-stu-id="50d48-210">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="50d48-211">
                    <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50d48-211">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="50d48-212">
                    <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50d48-212">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="50d48-213">Оплачивается</span><span class="sxs-lookup"><span data-stu-id="50d48-213">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="50d48-214">Выставления счетов за фактическое время: <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50d48-214">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="50d48-215">Тип выставления счетов за фактические расходы: <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50d48-215">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="50d48-216">Тип выставления счетов за фактические материалы: Оплачивается</span><span class="sxs-lookup"><span data-stu-id="50d48-216">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="50d48-217">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50d48-217">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="50d48-218">Да</span><span class="sxs-lookup"><span data-stu-id="50d48-218">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="50d48-219">Да</span><span class="sxs-lookup"><span data-stu-id="50d48-219">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="50d48-220">Весь проект</span><span class="sxs-lookup"><span data-stu-id="50d48-220">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="50d48-221">Не может быть задано</span><span class="sxs-lookup"><span data-stu-id="50d48-221">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="50d48-222">
                    <strong>Оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50d48-222">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="50d48-223">Не может быть задано</span><span class="sxs-lookup"><span data-stu-id="50d48-223">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="50d48-224">Выставления счетов за фактическое время: <strong>Недоступно</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50d48-224">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="50d48-225">Тип выставления счетов за фактические расходы: Оплачивается</span><span class="sxs-lookup"><span data-stu-id="50d48-225">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="50d48-226">Тип выставления счетов за фактические материалы: Оплачивается</span><span class="sxs-lookup"><span data-stu-id="50d48-226">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="50d48-227">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50d48-227">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="50d48-228">Да</span><span class="sxs-lookup"><span data-stu-id="50d48-228">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="50d48-229">Да</span><span class="sxs-lookup"><span data-stu-id="50d48-229">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="50d48-230">Весь проект</span><span class="sxs-lookup"><span data-stu-id="50d48-230">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="50d48-231">Не может быть задано</span><span class="sxs-lookup"><span data-stu-id="50d48-231">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="50d48-232">
                    <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50d48-232">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="50d48-233">Не может быть задано</span><span class="sxs-lookup"><span data-stu-id="50d48-233">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="50d48-234">Выставления счетов за фактическое время: <strong>Недоступно</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50d48-234">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="50d48-235">Тип выставления счетов за фактические расходы: <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50d48-235">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="50d48-236">Тип выставления счетов за фактические материалы: Оплачивается</span><span class="sxs-lookup"><span data-stu-id="50d48-236">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="50d48-237">Да</span><span class="sxs-lookup"><span data-stu-id="50d48-237">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="50d48-238">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50d48-238">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="50d48-239">Да</span><span class="sxs-lookup"><span data-stu-id="50d48-239">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="50d48-240">Весь проект</span><span class="sxs-lookup"><span data-stu-id="50d48-240">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="50d48-241">Оплачивается</span><span class="sxs-lookup"><span data-stu-id="50d48-241">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="50d48-242">Не может быть задано</span><span class="sxs-lookup"><span data-stu-id="50d48-242">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="50d48-243">Не может быть задано</span><span class="sxs-lookup"><span data-stu-id="50d48-243">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="50d48-244">Выставления счетов за фактическое время: Оплачивается</span><span class="sxs-lookup"><span data-stu-id="50d48-244">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="50d48-245">Тип выставления счетов за фактические расходы: <strong>Недоступно</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50d48-245">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="50d48-246">Тип выставления счетов за фактические материалы: Оплачивается</span><span class="sxs-lookup"><span data-stu-id="50d48-246">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="50d48-247">Да</span><span class="sxs-lookup"><span data-stu-id="50d48-247">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="50d48-248">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50d48-248">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="50d48-249">Да</span><span class="sxs-lookup"><span data-stu-id="50d48-249">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="50d48-250">Весь проект</span><span class="sxs-lookup"><span data-stu-id="50d48-250">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="50d48-251">
                    <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50d48-251">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="50d48-252">Не может быть задано</span><span class="sxs-lookup"><span data-stu-id="50d48-252">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="50d48-253">Не может быть задано</span><span class="sxs-lookup"><span data-stu-id="50d48-253">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="50d48-254">Выставления счетов за фактическое время: <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50d48-254">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="50d48-255">Тип выставления счетов за фактические расходы: <strong>Недоступно</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50d48-255">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="50d48-256">Тип выставления счетов за фактические материалы: Оплачивается</span><span class="sxs-lookup"><span data-stu-id="50d48-256">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="50d48-257">Да</span><span class="sxs-lookup"><span data-stu-id="50d48-257">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="50d48-258">Да</span><span class="sxs-lookup"><span data-stu-id="50d48-258">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="50d48-259">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50d48-259">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="50d48-260">Весь проект</span><span class="sxs-lookup"><span data-stu-id="50d48-260">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="50d48-261">Оплачивается</span><span class="sxs-lookup"><span data-stu-id="50d48-261">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="50d48-262">Оплачивается</span><span class="sxs-lookup"><span data-stu-id="50d48-262">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="50d48-263">Не может быть задано</span><span class="sxs-lookup"><span data-stu-id="50d48-263">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="50d48-264">Выставления счетов за фактическое время: Оплачивается</span><span class="sxs-lookup"><span data-stu-id="50d48-264">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="50d48-265">Тип выставления счетов за фактические расходы: Оплачивается</span><span class="sxs-lookup"><span data-stu-id="50d48-265">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="50d48-266">Тип выставления счетов за фактические материалы: <strong>Недоступно</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50d48-266">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="50d48-267">Да</span><span class="sxs-lookup"><span data-stu-id="50d48-267">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="50d48-268">Да</span><span class="sxs-lookup"><span data-stu-id="50d48-268">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="50d48-269">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50d48-269">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="50d48-270">Весь проект</span><span class="sxs-lookup"><span data-stu-id="50d48-270">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="50d48-271">
                    <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50d48-271">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="50d48-272">
                    <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50d48-272">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="50d48-273">Не может быть задано</span><span class="sxs-lookup"><span data-stu-id="50d48-273">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="50d48-274">Выставления счетов за фактическое время: <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50d48-274">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="50d48-275">Тип выставления счетов за фактические расходы: <strong>Не оплачивается</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50d48-275">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="50d48-276">Тип выставления счетов за фактические материалы: <strong>Недоступно</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50d48-276">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
