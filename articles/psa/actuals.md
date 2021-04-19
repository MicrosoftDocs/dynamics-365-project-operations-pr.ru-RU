---
title: Обзор фактических значений
description: В этом разделе представлена информация о фактических значениях проекта.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: c4a3424bed704243dfb5524fa541c3fcc0899e57
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285634"
---
# <a name="actuals-overview"></a><span data-ttu-id="49918-103">Обзор фактических значений</span><span class="sxs-lookup"><span data-stu-id="49918-103">Actuals overview</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="49918-104">Фактические значения — это сумма работы, которая была выполнена по проекту.</span><span class="sxs-lookup"><span data-stu-id="49918-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="49918-105">Фактические данные проекта можно отслеживать обратно к их исходным документам.</span><span class="sxs-lookup"><span data-stu-id="49918-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="49918-106">Эти исходные документы включают времени, расходы и записи журнала, а также счета.</span><span class="sxs-lookup"><span data-stu-id="49918-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Как фактические показатели проекта отслеживаются к исходным документам](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="49918-108">Отправка записи времени</span><span class="sxs-lookup"><span data-stu-id="49918-108">Submitting a time entry</span></span>

<span data-ttu-id="49918-109">В PSA когда запись время отправлена для проекта, который сопоставляется со строкой контракта по времени и материалам, создаются две строки журнала.</span><span class="sxs-lookup"><span data-stu-id="49918-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="49918-110">Одна строка для стоимости и другая строка для продаж, за которые не выставлены счета.</span><span class="sxs-lookup"><span data-stu-id="49918-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="49918-111">Когда запись время отправлена для проекта, который сопоставляется со строкой контракта с фиксированной ценой, строка журнала создается только для стоимости.</span><span class="sxs-lookup"><span data-stu-id="49918-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="49918-112">Логика для ввода цен по умолчанию находится в строке журнала.</span><span class="sxs-lookup"><span data-stu-id="49918-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="49918-113">Все значения полей из записи времени копируются в строку журнала.</span><span class="sxs-lookup"><span data-stu-id="49918-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="49918-114">Эти поля включают дату транзакции, строку контракта, с которой сопоставлен проект, и результат валюты в соответствующем прайс-листе.</span><span class="sxs-lookup"><span data-stu-id="49918-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="49918-115">Поля, которые влияют на цены по умолчанию, например **Роль** и **Подразделение**, вызывают ввод соответствующей цены по умолчанию в строке журнала.</span><span class="sxs-lookup"><span data-stu-id="49918-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="49918-116">Если вы добавили настраиваемое поле в запись времени и хотите, чтобы значение поля распространялось на фактические данные, создайте это поле в сущности фактических данных и используйте сопоставления полей для копирования поля из записи времени в фактические данные.</span><span class="sxs-lookup"><span data-stu-id="49918-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="49918-117">Отправка записи о расходах</span><span class="sxs-lookup"><span data-stu-id="49918-117">Submitting an expense entry</span></span>

<span data-ttu-id="49918-118">В PSA когда запись расходов отправлена для проекта, который сопоставляется со строкой контракта по времени и материалам, создаются две строки журнала.</span><span class="sxs-lookup"><span data-stu-id="49918-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="49918-119">Одна строка для стоимости и другая строка для продаж, за которые не выставлены счета.</span><span class="sxs-lookup"><span data-stu-id="49918-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="49918-120">Когда запись расхода отправлена для проекта, который сопоставляется со строкой контракта с фиксированной ценой, строка журнала создается только для стоимости.</span><span class="sxs-lookup"><span data-stu-id="49918-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="49918-121">Логика для ввода цен по умолчанию для расходов основана на категории расходов, которая выбрана на странице **Запись расхода**.</span><span class="sxs-lookup"><span data-stu-id="49918-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="49918-122">Дата транзакции, строка контракта, с которой сопоставлен проект, и валюта все используются для определения соответствующего прайс-листа.</span><span class="sxs-lookup"><span data-stu-id="49918-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="49918-123">Однако для самой цены сумма, которую ввел пользователь, задается непосредственно в связанных строках журнала расходов для стоимости и продаж по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="49918-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="49918-124">В текущей версии PSA основанная на категории запись цен по умолчанию за единицу в записях расходов недоступна.</span><span class="sxs-lookup"><span data-stu-id="49918-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="49918-125">Использование журналов записей для записи стоимости</span><span class="sxs-lookup"><span data-stu-id="49918-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="49918-126">Журналы записей в ПСА позволяют записывать стоимость или доход в классах проводок по материалам, сборам, времени, расходам и налогам.</span><span class="sxs-lookup"><span data-stu-id="49918-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="49918-127">Журнал имеется заголовок, строки и действие **Подтвердить**.</span><span class="sxs-lookup"><span data-stu-id="49918-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="49918-128">Ниже приведены некоторые сценарии, в которых можно использовать журнал:</span><span class="sxs-lookup"><span data-stu-id="49918-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="49918-129">Необходимо записывать фактические затраты на материалы и продажи в проекте.</span><span class="sxs-lookup"><span data-stu-id="49918-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="49918-130">Необходимо переместить фактические данные транзакций из другой системы в PSA.</span><span class="sxs-lookup"><span data-stu-id="49918-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="49918-131">Необходимо записывать затраты, возникшие в другой системе, такие как стоимость закупок или стоимость субподряда.</span><span class="sxs-lookup"><span data-stu-id="49918-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="49918-132">Использовать журналы записей для создания фактических значений должны только пользователи, которые полностью понимают влияние учета фактических значений на проект.</span><span class="sxs-lookup"><span data-stu-id="49918-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="49918-133">Это связано с тем, что приложение не проверяет тип строки журнала или связанные цены, вводимые в строку журнала.</span><span class="sxs-lookup"><span data-stu-id="49918-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="49918-134">Из-за влияния, которое может оказать этот тип журнала, будьте осторожны при предоставлении доступа для создания журналов записей.</span><span class="sxs-lookup"><span data-stu-id="49918-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="49918-135">Запись фактических данных по событиям проекта</span><span class="sxs-lookup"><span data-stu-id="49918-135">Recording actuals based on project events</span></span>

<span data-ttu-id="49918-136">PSA записывает финансовые транзакции, которые происходят в ходе проекта.</span><span class="sxs-lookup"><span data-stu-id="49918-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="49918-137">Эти транзакции записываются как **фактические значения**.</span><span class="sxs-lookup"><span data-stu-id="49918-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="49918-138">В следующих таблицах отображаются различные типы созданных фактических данных, в зависимости от того, является ли проект проектом "время и материалы" или проектом с фиксированной ценой.</span><span class="sxs-lookup"><span data-stu-id="49918-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="49918-139">**Ресурс принадлежит к тому же подразделению, что и контрактная единица по проекту**</span><span class="sxs-lookup"><span data-stu-id="49918-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="49918-140">Событие</span><span class="sxs-lookup"><span data-stu-id="49918-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="49918-141">Оплачиваемый или проданный проект</span><span class="sxs-lookup"><span data-stu-id="49918-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="49918-142">Проект на стадии предварительных продаж</span><span class="sxs-lookup"><span data-stu-id="49918-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="49918-143">Внутренний проект</span><span class="sxs-lookup"><span data-stu-id="49918-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="49918-144">Время и материалы</span><span class="sxs-lookup"><span data-stu-id="49918-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="49918-145">Фиксированная цена</span><span class="sxs-lookup"><span data-stu-id="49918-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="49918-146">Фактические</span><span class="sxs-lookup"><span data-stu-id="49918-146">Actuals</span></span></th>
<th><span data-ttu-id="49918-147">Валюта транзакции</span><span class="sxs-lookup"><span data-stu-id="49918-147">Transaction currency</span></span></th>
<th><span data-ttu-id="49918-148">Фиксированная цена</span><span class="sxs-lookup"><span data-stu-id="49918-148">Fixed price</span></span></th>
<th><span data-ttu-id="49918-149">Валюта транзакции</span><span class="sxs-lookup"><span data-stu-id="49918-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="49918-150">Создана запись времени.</span><span class="sxs-lookup"><span data-stu-id="49918-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="49918-151">Нет действий в сущности фактических данных</span><span class="sxs-lookup"><span data-stu-id="49918-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49918-152">Запись времени отправлена.</span><span class="sxs-lookup"><span data-stu-id="49918-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="49918-153">Нет действий в сущности фактических данных</span><span class="sxs-lookup"><span data-stu-id="49918-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="49918-154">Время одобрено, и нет изменений или увеличения оплачиваемых часов в процессе утверждения.</span><span class="sxs-lookup"><span data-stu-id="49918-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="49918-155">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="49918-155">Cost actual</span></span></td>
<td><span data-ttu-id="49918-156">Валюта единицы по контракту</span><span class="sxs-lookup"><span data-stu-id="49918-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="49918-157">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="49918-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="49918-158">Валюта единицы по контракту</span><span class="sxs-lookup"><span data-stu-id="49918-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="49918-159">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="49918-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="49918-160">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="49918-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49918-161">Фактическая сумма продаж с невыставленными счетами — оплачиваемые</span><span class="sxs-lookup"><span data-stu-id="49918-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="49918-162">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="49918-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="49918-163">Время одобрено, и имеется уменьшение оплачиваемых часов в процессе утверждения.</span><span class="sxs-lookup"><span data-stu-id="49918-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="49918-164">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="49918-164">Cost actual</span></span></td>
<td><span data-ttu-id="49918-165">Валюта единицы по контракту</span><span class="sxs-lookup"><span data-stu-id="49918-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="49918-166">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="49918-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="49918-167">Валюта единицы по контракту</span><span class="sxs-lookup"><span data-stu-id="49918-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="49918-168">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="49918-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="49918-169">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="49918-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49918-170">Фактическое количество продаж без выставления счета — оплачивается для нового количества</span><span class="sxs-lookup"><span data-stu-id="49918-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="49918-171">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="49918-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49918-172">Фактическое количество продаж без выставления счета — не оплачивается для разницы</span><span class="sxs-lookup"><span data-stu-id="49918-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="49918-173">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="49918-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="49918-174">Счет одобрен, и нет изменения или происходит увеличение оплачиваемых часов в процессе утверждения.</span><span class="sxs-lookup"><span data-stu-id="49918-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="49918-175">Обращение продаж без выставления счета</span><span class="sxs-lookup"><span data-stu-id="49918-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="49918-176">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="49918-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="49918-177">Продажи с выставленными счетами для вехи</span><span class="sxs-lookup"><span data-stu-id="49918-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="49918-178">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="49918-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="49918-179">Нет данных</span><span class="sxs-lookup"><span data-stu-id="49918-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="49918-180">Нет данных</span><span class="sxs-lookup"><span data-stu-id="49918-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49918-181">Продажи с выставлением счета</span><span class="sxs-lookup"><span data-stu-id="49918-181">Billed sales</span></span></td>
<td><span data-ttu-id="49918-182">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="49918-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="49918-183">Счет одобрен, и имеется уменьшение оплачиваемых часов в процессе утверждения.</span><span class="sxs-lookup"><span data-stu-id="49918-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="49918-184">Обращение продаж без выставления счета</span><span class="sxs-lookup"><span data-stu-id="49918-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="49918-185">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="49918-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="49918-186">Нет данных</span><span class="sxs-lookup"><span data-stu-id="49918-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="49918-187">Нет данных</span><span class="sxs-lookup"><span data-stu-id="49918-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="49918-188">Нет данных</span><span class="sxs-lookup"><span data-stu-id="49918-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="49918-189">Нет данных</span><span class="sxs-lookup"><span data-stu-id="49918-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49918-190">Продажи с выставленными счетами — оплачивается для нового количества</span><span class="sxs-lookup"><span data-stu-id="49918-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="49918-191">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="49918-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49918-192">Продажи с выставленным счетом — не оплачивается для разницы</span><span class="sxs-lookup"><span data-stu-id="49918-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="49918-193">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="49918-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="49918-194">Счет исправлен для увеличения оплачиваемого количества.</span><span class="sxs-lookup"><span data-stu-id="49918-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="49918-195">Продаж с выставленным счетом — обращение</span><span class="sxs-lookup"><span data-stu-id="49918-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="49918-196">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="49918-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="49918-197">Обращение продаж с выставленными счетами для вехи</span><span class="sxs-lookup"><span data-stu-id="49918-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="49918-198">Изменение в состоянии вехи с <strong>Выставлен счет</strong> на <strong>Готов к выставлению счета</strong></span><span class="sxs-lookup"><span data-stu-id="49918-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="49918-199">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="49918-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="49918-200">Нет данных</span><span class="sxs-lookup"><span data-stu-id="49918-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="49918-201">Нет данных</span><span class="sxs-lookup"><span data-stu-id="49918-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49918-202">Продажи с выставлением счета</span><span class="sxs-lookup"><span data-stu-id="49918-202">Billed sales</span></span></td>
<td><span data-ttu-id="49918-203">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="49918-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="49918-204">Счет исправлен для уменьшения оплачиваемого количества.</span><span class="sxs-lookup"><span data-stu-id="49918-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="49918-205">Продаж с выставленным счетом — обращение</span><span class="sxs-lookup"><span data-stu-id="49918-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="49918-206">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="49918-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49918-207">Продажи с выставленными счетами для нового количества</span><span class="sxs-lookup"><span data-stu-id="49918-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="49918-208">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="49918-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49918-209">Продажи без выставленного счета — оплачивается для разницы</span><span class="sxs-lookup"><span data-stu-id="49918-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="49918-210">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="49918-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="49918-211">**Ресурс принадлежит к подразделению, который отличается от контрактной единицы по проекту**</span><span class="sxs-lookup"><span data-stu-id="49918-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="49918-212">Событие</span><span class="sxs-lookup"><span data-stu-id="49918-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="49918-213">Оплачиваемый или проданный проект</span><span class="sxs-lookup"><span data-stu-id="49918-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="49918-214">Проект на стадии предварительных продаж</span><span class="sxs-lookup"><span data-stu-id="49918-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="49918-215">Внутренний проект</span><span class="sxs-lookup"><span data-stu-id="49918-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="49918-216">Время и материалы</span><span class="sxs-lookup"><span data-stu-id="49918-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="49918-217">Фиксированная цена</span><span class="sxs-lookup"><span data-stu-id="49918-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="49918-218">Фактические</span><span class="sxs-lookup"><span data-stu-id="49918-218">Actuals</span></span></th>
<th><span data-ttu-id="49918-219">Валюта транзакции</span><span class="sxs-lookup"><span data-stu-id="49918-219">Transaction currency</span></span></th>
<th><span data-ttu-id="49918-220">Фиксированная цена</span><span class="sxs-lookup"><span data-stu-id="49918-220">Fixed price</span></span></th>
<th><span data-ttu-id="49918-221">Валюта транзакции</span><span class="sxs-lookup"><span data-stu-id="49918-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="49918-222">Создана запись времени.</span><span class="sxs-lookup"><span data-stu-id="49918-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="49918-223">Нет действий в сущности фактических данных</span><span class="sxs-lookup"><span data-stu-id="49918-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49918-224">Запись времени отправлена.</span><span class="sxs-lookup"><span data-stu-id="49918-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="49918-225">Нет действий в сущности фактических данных</span><span class="sxs-lookup"><span data-stu-id="49918-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="49918-226">Время одобрено, и нет изменений или увеличения оплачиваемых часов в процессе утверждения.</span><span class="sxs-lookup"><span data-stu-id="49918-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="49918-227">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="49918-227">Cost actual</span></span></td>
<td><span data-ttu-id="49918-228">Валюта единицы по контракту</span><span class="sxs-lookup"><span data-stu-id="49918-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="49918-229">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="49918-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="49918-230">Валюта единицы по контракту</span><span class="sxs-lookup"><span data-stu-id="49918-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="49918-231">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="49918-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="49918-232">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="49918-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49918-233">Фактическая сумма продаж с невыставленными счетами — оплачиваемые</span><span class="sxs-lookup"><span data-stu-id="49918-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="49918-234">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="49918-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49918-235">Стоимость единицы распределения ресурсов</span><span class="sxs-lookup"><span data-stu-id="49918-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="49918-236">Валюта единицы распределения ресурсов</span><span class="sxs-lookup"><span data-stu-id="49918-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49918-237">Внутрихолдинговые продажи</span><span class="sxs-lookup"><span data-stu-id="49918-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="49918-238">Валюта единицы по контракту</span><span class="sxs-lookup"><span data-stu-id="49918-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="49918-239">Время одобрено, и имеется уменьшение оплачиваемых часов в процессе утверждения.</span><span class="sxs-lookup"><span data-stu-id="49918-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="49918-240">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="49918-240">Cost actual</span></span></td>
<td><span data-ttu-id="49918-241">Валюта единицы по контракту</span><span class="sxs-lookup"><span data-stu-id="49918-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="49918-242">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="49918-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="49918-243">Валюта единицы по контракту</span><span class="sxs-lookup"><span data-stu-id="49918-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="49918-244">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="49918-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="49918-245">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="49918-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49918-246">Стоимость единицы распределения ресурсов</span><span class="sxs-lookup"><span data-stu-id="49918-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="49918-247">Валюта единицы распределения ресурсов</span><span class="sxs-lookup"><span data-stu-id="49918-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49918-248">Внутрихолдинговые продажи</span><span class="sxs-lookup"><span data-stu-id="49918-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="49918-249">Валюта единицы по контракту</span><span class="sxs-lookup"><span data-stu-id="49918-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49918-250">Фактическое количество продаж без выставления счета — оплачивается для нового количества</span><span class="sxs-lookup"><span data-stu-id="49918-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="49918-251">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="49918-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49918-252">Фактическое количество продаж без выставления счета — не оплачивается для разницы</span><span class="sxs-lookup"><span data-stu-id="49918-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="49918-253">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="49918-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="49918-254">Счет одобрен, и нет изменения или происходит увеличение оплачиваемых часов в процессе утверждения.</span><span class="sxs-lookup"><span data-stu-id="49918-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="49918-255">Обращение продаж без выставления счета</span><span class="sxs-lookup"><span data-stu-id="49918-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="49918-256">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="49918-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="49918-257">Продажи с выставленными счетами для вехи</span><span class="sxs-lookup"><span data-stu-id="49918-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="49918-258">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="49918-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="49918-259">Нет данных</span><span class="sxs-lookup"><span data-stu-id="49918-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="49918-260">Нет данных</span><span class="sxs-lookup"><span data-stu-id="49918-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49918-261">Продажи с выставлением счета</span><span class="sxs-lookup"><span data-stu-id="49918-261">Billed sales</span></span></td>
<td><span data-ttu-id="49918-262">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="49918-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="49918-263">Счет одобрен, и имеется уменьшение оплачиваемых часов в процессе утверждения.</span><span class="sxs-lookup"><span data-stu-id="49918-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="49918-264">Обращение продаж без выставления счета</span><span class="sxs-lookup"><span data-stu-id="49918-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="49918-265">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="49918-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="49918-266">Нет данных</span><span class="sxs-lookup"><span data-stu-id="49918-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="49918-267">Нет данных</span><span class="sxs-lookup"><span data-stu-id="49918-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="49918-268">Нет данных</span><span class="sxs-lookup"><span data-stu-id="49918-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="49918-269">Нет данных</span><span class="sxs-lookup"><span data-stu-id="49918-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49918-270">Продажи с выставленными счетами — оплачивается для нового количества</span><span class="sxs-lookup"><span data-stu-id="49918-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="49918-271">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="49918-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49918-272">Продажи с выставленным счетом — не оплачивается для разницы</span><span class="sxs-lookup"><span data-stu-id="49918-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="49918-273">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="49918-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="49918-274">Счет исправлен для увеличения оплачиваемого количества.</span><span class="sxs-lookup"><span data-stu-id="49918-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="49918-275">Продаж с выставленным счетом — обращение</span><span class="sxs-lookup"><span data-stu-id="49918-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="49918-276">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="49918-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="49918-277">Обращение продаж с выставленными счетами для вехи</span><span class="sxs-lookup"><span data-stu-id="49918-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="49918-278">Изменение в состоянии вехи с <strong>Выставлен счет</strong> на <strong>Готов к выставлению счета</strong></span><span class="sxs-lookup"><span data-stu-id="49918-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="49918-279">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="49918-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="49918-280">Нет данных</span><span class="sxs-lookup"><span data-stu-id="49918-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="49918-281">Нет данных</span><span class="sxs-lookup"><span data-stu-id="49918-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49918-282">Продажи с выставлением счета</span><span class="sxs-lookup"><span data-stu-id="49918-282">Billed sales</span></span></td>
<td><span data-ttu-id="49918-283">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="49918-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="49918-284">Счет исправлен для уменьшения оплачиваемого количества.</span><span class="sxs-lookup"><span data-stu-id="49918-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="49918-285">Продаж с выставленным счетом — обращение</span><span class="sxs-lookup"><span data-stu-id="49918-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="49918-286">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="49918-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49918-287">Продажи с выставленными счетами для нового количества</span><span class="sxs-lookup"><span data-stu-id="49918-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="49918-288">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="49918-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49918-289">Продажи без выставленного счета — оплачивается для разницы</span><span class="sxs-lookup"><span data-stu-id="49918-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="49918-290">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="49918-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]