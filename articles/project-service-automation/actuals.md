---
title: Фактические
description: В этом разделе представлена информация о фактических значениях проекта.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 44c6e85f-5b21-4e24-999c-15a2f065d977
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8291e0eb8531e8e9690368675f333c44b6e92e48
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755018"
---
# <a name="actuals"></a><span data-ttu-id="42412-103">Фактические</span><span class="sxs-lookup"><span data-stu-id="42412-103">Actuals</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="42412-104">Фактические значения — это сумма работы, которая была выполнена по проекту.</span><span class="sxs-lookup"><span data-stu-id="42412-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="42412-105">Фактические данные проекта можно отслеживать обратно к их исходным документам.</span><span class="sxs-lookup"><span data-stu-id="42412-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="42412-106">Эти исходные документы включают времени, расходы и записи журнала, а также счета.</span><span class="sxs-lookup"><span data-stu-id="42412-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Как фактические показатели проекта отслеживаются к исходным документам](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="42412-108">Отправка записи времени</span><span class="sxs-lookup"><span data-stu-id="42412-108">Submitting a time entry</span></span>

<span data-ttu-id="42412-109">В PSA когда запись время отправлена для проекта, который сопоставляется со строкой контракта по времени и материалам, создаются две строки журнала.</span><span class="sxs-lookup"><span data-stu-id="42412-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="42412-110">Одна строка для стоимости и другая строка для продаж, за которые не выставлены счета.</span><span class="sxs-lookup"><span data-stu-id="42412-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="42412-111">Когда запись время отправлена для проекта, который сопоставляется со строкой контракта с фиксированной ценой, строка журнала создается только для стоимости.</span><span class="sxs-lookup"><span data-stu-id="42412-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="42412-112">Логика для ввода цен по умолчанию находится в строке журнала.</span><span class="sxs-lookup"><span data-stu-id="42412-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="42412-113">Все значения полей из записи времени копируются в строку журнала.</span><span class="sxs-lookup"><span data-stu-id="42412-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="42412-114">Эти поля включают дату транзакции, строку контракта, с которой сопоставлен проект, и результат валюты в соответствующем прайс-листе.</span><span class="sxs-lookup"><span data-stu-id="42412-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="42412-115">Поля, которые влияют на цены по умолчанию, например **Роль** и **Подразделение**, вызывают ввод соответствующей цены по умолчанию в строке журнала.</span><span class="sxs-lookup"><span data-stu-id="42412-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="42412-116">Если вы добавили настраиваемое поле в запись времени и хотите, чтобы значение поля распространялось на фактические данные, создайте это поле в сущности фактических данных и используйте сопоставления полей для копирования поля из записи времени в фактические данные.</span><span class="sxs-lookup"><span data-stu-id="42412-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="42412-117">Отправка записи о расходах</span><span class="sxs-lookup"><span data-stu-id="42412-117">Submitting an expense entry</span></span>

<span data-ttu-id="42412-118">В PSA когда запись расходов отправлена для проекта, который сопоставляется со строкой контракта по времени и материалам, создаются две строки журнала.</span><span class="sxs-lookup"><span data-stu-id="42412-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="42412-119">Одна строка для стоимости и другая строка для продаж, за которые не выставлены счета.</span><span class="sxs-lookup"><span data-stu-id="42412-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="42412-120">Когда запись расхода отправлена для проекта, который сопоставляется со строкой контракта с фиксированной ценой, строка журнала создается только для стоимости.</span><span class="sxs-lookup"><span data-stu-id="42412-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="42412-121">Логика для ввода цен по умолчанию для расходов основана на категории расходов, которая выбрана на странице **Запись расхода**.</span><span class="sxs-lookup"><span data-stu-id="42412-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="42412-122">Дата транзакции, строка контракта, с которой сопоставлен проект, и валюта все используются для определения соответствующего прайс-листа.</span><span class="sxs-lookup"><span data-stu-id="42412-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="42412-123">Однако для самой цены сумма, которую ввел пользователь, задается непосредственно в связанных строках журнала расходов для стоимости и продаж по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="42412-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="42412-124">В текущей версии PSA основанная на категории запись цен по умолчанию за единицу в записях расходов недоступна.</span><span class="sxs-lookup"><span data-stu-id="42412-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-journals-to-record-costs"></a><span data-ttu-id="42412-125">Использование журналов для записи стоимости</span><span class="sxs-lookup"><span data-stu-id="42412-125">Using journals to record costs</span></span>

<span data-ttu-id="42412-126">Журналы в PSA позволяют записывать стоимость или доход в классах проводок по материалам, сборам, времени, расходам и налогам.</span><span class="sxs-lookup"><span data-stu-id="42412-126">In PSA, journals let you record cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="42412-127">Журнал имеется заголовок, строки и действие **Подтвердить**.</span><span class="sxs-lookup"><span data-stu-id="42412-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="42412-128">Ниже приведены некоторые сценарии, в которых можно использовать журнал:</span><span class="sxs-lookup"><span data-stu-id="42412-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="42412-129">Необходимо записывать фактические затраты на материалы и продажи в проекте.</span><span class="sxs-lookup"><span data-stu-id="42412-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="42412-130">Необходимо переместить фактические данные транзакций из другой системы в PSA.</span><span class="sxs-lookup"><span data-stu-id="42412-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="42412-131">Необходимо записывать затраты, возникшие в другой системе, такие как стоимость закупок или стоимость субподряда.</span><span class="sxs-lookup"><span data-stu-id="42412-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="42412-132">Запись фактических данных по событиям проекта</span><span class="sxs-lookup"><span data-stu-id="42412-132">Recording actuals based on project events</span></span>

<span data-ttu-id="42412-133">PSA записывает финансовые транзакции, которые происходят в ходе проекта.</span><span class="sxs-lookup"><span data-stu-id="42412-133">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="42412-134">Эти транзакции записываются как **фактические значения**.</span><span class="sxs-lookup"><span data-stu-id="42412-134">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="42412-135">В следующих таблицах отображаются различные типы созданных фактических данных, в зависимости от того, является ли проект проектом "время и материалы" или проектом с фиксированной ценой.</span><span class="sxs-lookup"><span data-stu-id="42412-135">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="42412-136">**Ресурс принадлежит к тому же подразделению, что и контрактная единица по проекту**</span><span class="sxs-lookup"><span data-stu-id="42412-136">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="42412-137">Событие</span><span class="sxs-lookup"><span data-stu-id="42412-137">Event</span></span></th>
<th colspan="4"><span data-ttu-id="42412-138">Оплачиваемый или проданный проект</span><span class="sxs-lookup"><span data-stu-id="42412-138">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="42412-139">Проект на стадии предварительных продаж</span><span class="sxs-lookup"><span data-stu-id="42412-139">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="42412-140">Внутренний проект</span><span class="sxs-lookup"><span data-stu-id="42412-140">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="42412-141">Время и материалы</span><span class="sxs-lookup"><span data-stu-id="42412-141">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="42412-142">Фиксированная цена</span><span class="sxs-lookup"><span data-stu-id="42412-142">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="42412-143">Фактические</span><span class="sxs-lookup"><span data-stu-id="42412-143">Actuals</span></span></th>
<th><span data-ttu-id="42412-144">Валюта транзакции</span><span class="sxs-lookup"><span data-stu-id="42412-144">Transaction currency</span></span></th>
<th><span data-ttu-id="42412-145">Фиксированная цена</span><span class="sxs-lookup"><span data-stu-id="42412-145">Fixed price</span></span></th>
<th><span data-ttu-id="42412-146">Валюта транзакции</span><span class="sxs-lookup"><span data-stu-id="42412-146">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="42412-147">Создана запись времени.</span><span class="sxs-lookup"><span data-stu-id="42412-147">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="42412-148">Нет действий в сущности фактических данных</span><span class="sxs-lookup"><span data-stu-id="42412-148">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42412-149">Запись времени отправлена.</span><span class="sxs-lookup"><span data-stu-id="42412-149">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="42412-150">Нет действий в сущности фактических данных</span><span class="sxs-lookup"><span data-stu-id="42412-150">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="42412-151">Время одобрено, и нет изменений или увеличения оплачиваемых часов в процессе утверждения.</span><span class="sxs-lookup"><span data-stu-id="42412-151">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="42412-152">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="42412-152">Cost actual</span></span></td>
<td><span data-ttu-id="42412-153">Валюта единицы по контракту</span><span class="sxs-lookup"><span data-stu-id="42412-153">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="42412-154">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="42412-154">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="42412-155">Валюта единицы по контракту</span><span class="sxs-lookup"><span data-stu-id="42412-155">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="42412-156">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="42412-156">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="42412-157">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="42412-157">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42412-158">Фактическая сумма продаж с невыставленными счетами — оплачиваемые</span><span class="sxs-lookup"><span data-stu-id="42412-158">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="42412-159">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="42412-159">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="42412-160">Время одобрено, и имеется уменьшение оплачиваемых часов в процессе утверждения.</span><span class="sxs-lookup"><span data-stu-id="42412-160">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="42412-161">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="42412-161">Cost actual</span></span></td>
<td><span data-ttu-id="42412-162">Валюта единицы по контракту</span><span class="sxs-lookup"><span data-stu-id="42412-162">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="42412-163">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="42412-163">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="42412-164">Валюта единицы по контракту</span><span class="sxs-lookup"><span data-stu-id="42412-164">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="42412-165">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="42412-165">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="42412-166">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="42412-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42412-167">Фактическое количество продаж без выставления счета — оплачивается для нового количества</span><span class="sxs-lookup"><span data-stu-id="42412-167">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="42412-168">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="42412-168">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42412-169">Фактическое количество продаж без выставления счета — не оплачивается для разницы</span><span class="sxs-lookup"><span data-stu-id="42412-169">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="42412-170">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="42412-170">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="42412-171">Счет одобрен, и нет изменения или происходит увеличение оплачиваемых часов в процессе утверждения.</span><span class="sxs-lookup"><span data-stu-id="42412-171">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="42412-172">Обращение продаж без выставления счета</span><span class="sxs-lookup"><span data-stu-id="42412-172">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="42412-173">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="42412-173">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="42412-174">Продажи с выставленными счетами для вехи</span><span class="sxs-lookup"><span data-stu-id="42412-174">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="42412-175">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="42412-175">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="42412-176">Нет данных</span><span class="sxs-lookup"><span data-stu-id="42412-176">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="42412-177">Нет данных</span><span class="sxs-lookup"><span data-stu-id="42412-177">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42412-178">Продажи с выставлением счета</span><span class="sxs-lookup"><span data-stu-id="42412-178">Billed sales</span></span></td>
<td><span data-ttu-id="42412-179">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="42412-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="42412-180">Счет одобрен, и имеется уменьшение оплачиваемых часов в процессе утверждения.</span><span class="sxs-lookup"><span data-stu-id="42412-180">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="42412-181">Обращение продаж без выставления счета</span><span class="sxs-lookup"><span data-stu-id="42412-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="42412-182">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="42412-182">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="42412-183">Нет данных</span><span class="sxs-lookup"><span data-stu-id="42412-183">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="42412-184">Нет данных</span><span class="sxs-lookup"><span data-stu-id="42412-184">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="42412-185">Нет данных</span><span class="sxs-lookup"><span data-stu-id="42412-185">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="42412-186">Нет данных</span><span class="sxs-lookup"><span data-stu-id="42412-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42412-187">Продажи с выставленными счетами — оплачивается для нового количества</span><span class="sxs-lookup"><span data-stu-id="42412-187">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="42412-188">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="42412-188">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42412-189">Продажи с выставленным счетом — не оплачивается для разницы</span><span class="sxs-lookup"><span data-stu-id="42412-189">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="42412-190">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="42412-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="42412-191">Счет исправлен для увеличения оплачиваемого количества.</span><span class="sxs-lookup"><span data-stu-id="42412-191">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="42412-192">Продаж с выставленным счетом — обращение</span><span class="sxs-lookup"><span data-stu-id="42412-192">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="42412-193">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="42412-193">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="42412-194">Обращение продаж с выставленными счетами для вехи</span><span class="sxs-lookup"><span data-stu-id="42412-194">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="42412-195">Изменение в состоянии вехи с <strong>Выставлен счет</strong> на <strong>Готов к выставлению счета</strong></span><span class="sxs-lookup"><span data-stu-id="42412-195">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="42412-196">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="42412-196">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="42412-197">Нет данных</span><span class="sxs-lookup"><span data-stu-id="42412-197">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="42412-198">Нет данных</span><span class="sxs-lookup"><span data-stu-id="42412-198">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42412-199">Продажи с выставлением счета</span><span class="sxs-lookup"><span data-stu-id="42412-199">Billed sales</span></span></td>
<td><span data-ttu-id="42412-200">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="42412-200">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="42412-201">Счет исправлен для уменьшения оплачиваемого количества.</span><span class="sxs-lookup"><span data-stu-id="42412-201">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="42412-202">Продаж с выставленным счетом — обращение</span><span class="sxs-lookup"><span data-stu-id="42412-202">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="42412-203">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="42412-203">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42412-204">Продажи с выставленными счетами для нового количества</span><span class="sxs-lookup"><span data-stu-id="42412-204">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="42412-205">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="42412-205">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42412-206">Продажи без выставленного счета — оплачивается для разницы</span><span class="sxs-lookup"><span data-stu-id="42412-206">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="42412-207">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="42412-207">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="42412-208">**Ресурс принадлежит к подразделению, который отличается от контрактной единицы по проекту**</span><span class="sxs-lookup"><span data-stu-id="42412-208">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="42412-209">Событие</span><span class="sxs-lookup"><span data-stu-id="42412-209">Event</span></span></th>
<th colspan="4"><span data-ttu-id="42412-210">Оплачиваемый или проданный проект</span><span class="sxs-lookup"><span data-stu-id="42412-210">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="42412-211">Проект на стадии предварительных продаж</span><span class="sxs-lookup"><span data-stu-id="42412-211">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="42412-212">Внутренний проект</span><span class="sxs-lookup"><span data-stu-id="42412-212">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="42412-213">Время и материалы</span><span class="sxs-lookup"><span data-stu-id="42412-213">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="42412-214">Фиксированная цена</span><span class="sxs-lookup"><span data-stu-id="42412-214">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="42412-215">Фактические</span><span class="sxs-lookup"><span data-stu-id="42412-215">Actuals</span></span></th>
<th><span data-ttu-id="42412-216">Валюта транзакции</span><span class="sxs-lookup"><span data-stu-id="42412-216">Transaction currency</span></span></th>
<th><span data-ttu-id="42412-217">Фиксированная цена</span><span class="sxs-lookup"><span data-stu-id="42412-217">Fixed price</span></span></th>
<th><span data-ttu-id="42412-218">Валюта транзакции</span><span class="sxs-lookup"><span data-stu-id="42412-218">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="42412-219">Создана запись времени.</span><span class="sxs-lookup"><span data-stu-id="42412-219">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="42412-220">Нет действий в сущности фактических данных</span><span class="sxs-lookup"><span data-stu-id="42412-220">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42412-221">Запись времени отправлена.</span><span class="sxs-lookup"><span data-stu-id="42412-221">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="42412-222">Нет действий в сущности фактических данных</span><span class="sxs-lookup"><span data-stu-id="42412-222">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="42412-223">Время одобрено, и нет изменений или увеличения оплачиваемых часов в процессе утверждения.</span><span class="sxs-lookup"><span data-stu-id="42412-223">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="42412-224">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="42412-224">Cost actual</span></span></td>
<td><span data-ttu-id="42412-225">Валюта единицы по контракту</span><span class="sxs-lookup"><span data-stu-id="42412-225">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="42412-226">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="42412-226">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="42412-227">Валюта единицы по контракту</span><span class="sxs-lookup"><span data-stu-id="42412-227">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="42412-228">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="42412-228">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="42412-229">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="42412-229">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42412-230">Фактическая сумма продаж с невыставленными счетами — оплачиваемые</span><span class="sxs-lookup"><span data-stu-id="42412-230">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="42412-231">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="42412-231">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42412-232">Стоимость единицы распределения ресурсов</span><span class="sxs-lookup"><span data-stu-id="42412-232">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="42412-233">Валюта единицы распределения ресурсов</span><span class="sxs-lookup"><span data-stu-id="42412-233">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42412-234">Внутрихолдинговые продажи</span><span class="sxs-lookup"><span data-stu-id="42412-234">Interorganizational sales</span></span></td>
<td><span data-ttu-id="42412-235">Валюта единицы по контракту</span><span class="sxs-lookup"><span data-stu-id="42412-235">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="42412-236">Время одобрено, и имеется уменьшение оплачиваемых часов в процессе утверждения.</span><span class="sxs-lookup"><span data-stu-id="42412-236">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="42412-237">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="42412-237">Cost actual</span></span></td>
<td><span data-ttu-id="42412-238">Валюта единицы по контракту</span><span class="sxs-lookup"><span data-stu-id="42412-238">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="42412-239">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="42412-239">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="42412-240">Валюта единицы по контракту</span><span class="sxs-lookup"><span data-stu-id="42412-240">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="42412-241">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="42412-241">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="42412-242">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="42412-242">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42412-243">Стоимость единицы распределения ресурсов</span><span class="sxs-lookup"><span data-stu-id="42412-243">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="42412-244">Валюта единицы распределения ресурсов</span><span class="sxs-lookup"><span data-stu-id="42412-244">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42412-245">Внутрихолдинговые продажи</span><span class="sxs-lookup"><span data-stu-id="42412-245">Interorganizational sales</span></span></td>
<td><span data-ttu-id="42412-246">Валюта единицы по контракту</span><span class="sxs-lookup"><span data-stu-id="42412-246">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42412-247">Фактическое количество продаж без выставления счета — оплачивается для нового количества</span><span class="sxs-lookup"><span data-stu-id="42412-247">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="42412-248">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="42412-248">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42412-249">Фактическое количество продаж без выставления счета — не оплачивается для разницы</span><span class="sxs-lookup"><span data-stu-id="42412-249">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="42412-250">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="42412-250">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="42412-251">Счет одобрен, и нет изменения или происходит увеличение оплачиваемых часов в процессе утверждения.</span><span class="sxs-lookup"><span data-stu-id="42412-251">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="42412-252">Обращение продаж без выставления счета</span><span class="sxs-lookup"><span data-stu-id="42412-252">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="42412-253">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="42412-253">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="42412-254">Продажи с выставленными счетами для вехи</span><span class="sxs-lookup"><span data-stu-id="42412-254">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="42412-255">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="42412-255">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="42412-256">Нет данных</span><span class="sxs-lookup"><span data-stu-id="42412-256">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="42412-257">Нет данных</span><span class="sxs-lookup"><span data-stu-id="42412-257">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42412-258">Продажи с выставлением счета</span><span class="sxs-lookup"><span data-stu-id="42412-258">Billed sales</span></span></td>
<td><span data-ttu-id="42412-259">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="42412-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="42412-260">Счет одобрен, и имеется уменьшение оплачиваемых часов в процессе утверждения.</span><span class="sxs-lookup"><span data-stu-id="42412-260">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="42412-261">Обращение продаж без выставления счета</span><span class="sxs-lookup"><span data-stu-id="42412-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="42412-262">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="42412-262">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="42412-263">Нет данных</span><span class="sxs-lookup"><span data-stu-id="42412-263">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="42412-264">Нет данных</span><span class="sxs-lookup"><span data-stu-id="42412-264">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="42412-265">Нет данных</span><span class="sxs-lookup"><span data-stu-id="42412-265">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="42412-266">Нет данных</span><span class="sxs-lookup"><span data-stu-id="42412-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42412-267">Продажи с выставленными счетами — оплачивается для нового количества</span><span class="sxs-lookup"><span data-stu-id="42412-267">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="42412-268">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="42412-268">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42412-269">Продажи с выставленным счетом — не оплачивается для разницы</span><span class="sxs-lookup"><span data-stu-id="42412-269">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="42412-270">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="42412-270">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="42412-271">Счет исправлен для увеличения оплачиваемого количества.</span><span class="sxs-lookup"><span data-stu-id="42412-271">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="42412-272">Продаж с выставленным счетом — обращение</span><span class="sxs-lookup"><span data-stu-id="42412-272">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="42412-273">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="42412-273">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="42412-274">Обращение продаж с выставленными счетами для вехи</span><span class="sxs-lookup"><span data-stu-id="42412-274">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="42412-275">Изменение в состоянии вехи с <strong>Выставлен счет</strong> на <strong>Готов к выставлению счета</strong></span><span class="sxs-lookup"><span data-stu-id="42412-275">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="42412-276">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="42412-276">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="42412-277">Нет данных</span><span class="sxs-lookup"><span data-stu-id="42412-277">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="42412-278">Нет данных</span><span class="sxs-lookup"><span data-stu-id="42412-278">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42412-279">Продажи с выставлением счета</span><span class="sxs-lookup"><span data-stu-id="42412-279">Billed sales</span></span></td>
<td><span data-ttu-id="42412-280">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="42412-280">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="42412-281">Счет исправлен для уменьшения оплачиваемого количества.</span><span class="sxs-lookup"><span data-stu-id="42412-281">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="42412-282">Продаж с выставленным счетом — обращение</span><span class="sxs-lookup"><span data-stu-id="42412-282">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="42412-283">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="42412-283">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42412-284">Продажи с выставленными счетами для нового количества</span><span class="sxs-lookup"><span data-stu-id="42412-284">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="42412-285">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="42412-285">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42412-286">Продажи без выставленного счета — оплачивается для разницы</span><span class="sxs-lookup"><span data-stu-id="42412-286">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="42412-287">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="42412-287">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
