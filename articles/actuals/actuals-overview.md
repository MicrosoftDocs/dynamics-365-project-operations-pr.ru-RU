---
title: Домашняя страница "Фактические значения"
description: В этой теме предоставлена информация о порядке работы с фактическими данными в Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 75ad336a995aba3505325466433a5c5e2bb3e776
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/01/2020
ms.locfileid: "3907334"
---
# <a name="actuals"></a><span data-ttu-id="301b8-103">Фактические значения</span><span class="sxs-lookup"><span data-stu-id="301b8-103">Actuals</span></span>

<span data-ttu-id="301b8-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/без запасов_</span><span class="sxs-lookup"><span data-stu-id="301b8-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="301b8-105">Фактические значения — это сумма работы, которая была выполнена по проекту.</span><span class="sxs-lookup"><span data-stu-id="301b8-105">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="301b8-106">Они создаются на основе записей о времени и расходах, а также журнальных записей и счетов-фактур.</span><span class="sxs-lookup"><span data-stu-id="301b8-106">They are created as a result of time and expense entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="301b8-107">Отправка строк журналов и времени</span><span class="sxs-lookup"><span data-stu-id="301b8-107">Journal lines and time submission</span></span>

<span data-ttu-id="301b8-108">Для получения дополнительной информации о записи времени см. тему [Обзор записи времени](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="301b8-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="301b8-109">Время и материалы</span><span class="sxs-lookup"><span data-stu-id="301b8-109">Time and materials</span></span>

<span data-ttu-id="301b8-110">Когда отправляемая запись времени связана с проектом, который сопоставлен со строкой контракта на время и материалы, система создает две строки журнала: одну для затрат и одну для продаж, за которые не выставлен счет.</span><span class="sxs-lookup"><span data-stu-id="301b8-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="301b8-111">Фиксированная цена</span><span class="sxs-lookup"><span data-stu-id="301b8-111">Fixed price</span></span>

<span data-ttu-id="301b8-112">Когда отправляемая запись времени связана с проектом, который сопоставляется со строкой контракта с фиксированной ценой, система создает одну строку журнала для стоимости.</span><span class="sxs-lookup"><span data-stu-id="301b8-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="301b8-113">Цены по умолчанию</span><span class="sxs-lookup"><span data-stu-id="301b8-113">Default pricing</span></span>

<span data-ttu-id="301b8-114">Логика создания цен по умолчанию находится в строке журнала.</span><span class="sxs-lookup"><span data-stu-id="301b8-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="301b8-115">Значения полей из записи времени копируются в строку журнала.</span><span class="sxs-lookup"><span data-stu-id="301b8-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="301b8-116">Эти значения включают дату транзакции, строку контракта, с которой сопоставлен проект, и результат валюты в соответствующем прайс-листе.</span><span class="sxs-lookup"><span data-stu-id="301b8-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="301b8-117">Поля, которые влияют на цены по умолчанию, например **Роль** и **Подразделение**, используются для определения соответствующей цены в строке журнала.</span><span class="sxs-lookup"><span data-stu-id="301b8-117">The fields that affect default pricing, such as **Role** and **Org Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="301b8-118">Вы можете добавить настраиваемое поле к записи времени.</span><span class="sxs-lookup"><span data-stu-id="301b8-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="301b8-119">Если вы хотите, чтобы значение поля распространялось на фактические данные, создайте это поле в сущности фактических данных и используйте сопоставления полей для копирования поля из записи времени в фактические данные.</span><span class="sxs-lookup"><span data-stu-id="301b8-119">If you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="301b8-120">Строки журнала и базовая отправка расходов</span><span class="sxs-lookup"><span data-stu-id="301b8-120">Journal lines and basic expense submission</span></span>

<span data-ttu-id="301b8-121">Дополнительные сведения о записи расходов см. в теме [Обзор расходов](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="301b8-121">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="301b8-122">Время и материалы</span><span class="sxs-lookup"><span data-stu-id="301b8-122">Time and materials</span></span>

<span data-ttu-id="301b8-123">Когда отправляемая базовая запись затрат связана с проектом, который сопоставлен со строкой контракта на время и материалы, система создает две строки журнала: одну для затрат и одну для продаж, за которые не выставлен счет.</span><span class="sxs-lookup"><span data-stu-id="301b8-123">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="301b8-124">Фиксированная цена</span><span class="sxs-lookup"><span data-stu-id="301b8-124">Fixed price</span></span>

<span data-ttu-id="301b8-125">Когда отправляемая базовая запись расходов связана с проектом, который сопоставляется со строкой контракта с фиксированной ценой, система создает одну строку журнала для стоимости.</span><span class="sxs-lookup"><span data-stu-id="301b8-125">When a basic expense entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="301b8-126">Цены по умолчанию</span><span class="sxs-lookup"><span data-stu-id="301b8-126">Default pricing</span></span>

<span data-ttu-id="301b8-127">Логика ввода цен по умолчанию для расходов основана на категории расходов.</span><span class="sxs-lookup"><span data-stu-id="301b8-127">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="301b8-128">Дата транзакции, строка контракта, с которой сопоставлен проект, и валюта все используются для определения соответствующего прайс-листа.</span><span class="sxs-lookup"><span data-stu-id="301b8-128">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="301b8-129">Однако по умолчанию сумма, которая введена для самой цены, задается непосредственно в связанных строках журнала расходов для стоимости и продаж.</span><span class="sxs-lookup"><span data-stu-id="301b8-129">However, by default, the amount that is entered for the price itself is set directly on the related expense journal lines for cost and sales.</span></span>

<span data-ttu-id="301b8-130">Основанная на категории запись цен по умолчанию за единицу в записях расходов недоступна.</span><span class="sxs-lookup"><span data-stu-id="301b8-130">Category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="301b8-131">Использование журналов записей для записи стоимости</span><span class="sxs-lookup"><span data-stu-id="301b8-131">Use entry journals to record costs</span></span>

<span data-ttu-id="301b8-132">Журналы можно использовать для записи стоимости или дохода в классах проводок по материалам, сборам, времени, расходам и налогам.</span><span class="sxs-lookup"><span data-stu-id="301b8-132">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="301b8-133">Журналы могут использоваться для следующих целей:</span><span class="sxs-lookup"><span data-stu-id="301b8-133">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="301b8-134">Запись фактических затрат на материалы и продажи в проекте.</span><span class="sxs-lookup"><span data-stu-id="301b8-134">Record the actual cost of materials and sales on a project.</span></span>
- <span data-ttu-id="301b8-135">Перемещение фактических данных из другой системы в Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="301b8-135">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="301b8-136">Запись затрат, которые произошли в другой системе.</span><span class="sxs-lookup"><span data-stu-id="301b8-136">Record costs that occurred in another system.</span></span> <span data-ttu-id="301b8-137">Эти затраты могут включать затраты на закупку или субподряд.</span><span class="sxs-lookup"><span data-stu-id="301b8-137">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="301b8-138">Приложение не проверяет тип строки журнала или соответствующие цены, введенные в строке журнала.</span><span class="sxs-lookup"><span data-stu-id="301b8-138">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="301b8-139">Следовательно, только пользователь, который полностью осознает влияние на учет от фактических данных по проекту должен использовать журналы записей для создания фактических данных.</span><span class="sxs-lookup"><span data-stu-id="301b8-139">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="301b8-140">Из-за влияния этого типа журнала вам следует тщательно выбирать, у кого есть доступ для создания журналов входа.</span><span class="sxs-lookup"><span data-stu-id="301b8-140">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>
## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="301b8-141">Запись фактических данных по событиям проекта</span><span class="sxs-lookup"><span data-stu-id="301b8-141">Record actuals based on project events</span></span>

<span data-ttu-id="301b8-142">Project Operations записывает финансовые транзакции, которые происходят в ходе проекта.</span><span class="sxs-lookup"><span data-stu-id="301b8-142">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="301b8-143">Эти транзакции записываются как фактические значения.</span><span class="sxs-lookup"><span data-stu-id="301b8-143">These transactions are recorded as actuals.</span></span> <span data-ttu-id="301b8-144">В следующих таблицах отображаются различные типы созданных фактических данных, в зависимости от того, является ли проект проектом "время и материалы" или проектом с фиксированной ценой.</span><span class="sxs-lookup"><span data-stu-id="301b8-144">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="301b8-145">Ресурс принадлежит к тому же подразделению, что и контрактная единица по проекту</span><span class="sxs-lookup"><span data-stu-id="301b8-145">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="301b8-146">Событие</span><span class="sxs-lookup"><span data-stu-id="301b8-146">Event</span></span></th>
<th colspan="4"><span data-ttu-id="301b8-147">Оплачиваемый или проданный проект</span><span class="sxs-lookup"><span data-stu-id="301b8-147">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="301b8-148">Проект на стадии предварительных продаж</span><span class="sxs-lookup"><span data-stu-id="301b8-148">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="301b8-149">Внутренний проект</span><span class="sxs-lookup"><span data-stu-id="301b8-149">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="301b8-150">Время и материалы</span><span class="sxs-lookup"><span data-stu-id="301b8-150">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="301b8-151">Фиксированная цена</span><span class="sxs-lookup"><span data-stu-id="301b8-151">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="301b8-152">Фактические</span><span class="sxs-lookup"><span data-stu-id="301b8-152">Actuals</span></span></th>
<th><span data-ttu-id="301b8-153">Валюта транзакции</span><span class="sxs-lookup"><span data-stu-id="301b8-153">Transaction currency</span></span></th>
<th><span data-ttu-id="301b8-154">Фиксированная цена</span><span class="sxs-lookup"><span data-stu-id="301b8-154">Fixed price</span></span></th>
<th><span data-ttu-id="301b8-155">Валюта транзакции</span><span class="sxs-lookup"><span data-stu-id="301b8-155">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="301b8-156">Создана запись времени.</span><span class="sxs-lookup"><span data-stu-id="301b8-156">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="301b8-157">Нет действий в сущности фактических данных</span><span class="sxs-lookup"><span data-stu-id="301b8-157">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="301b8-158">Запись времени отправлена.</span><span class="sxs-lookup"><span data-stu-id="301b8-158">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="301b8-159">Нет действий в сущности фактических данных</span><span class="sxs-lookup"><span data-stu-id="301b8-159">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="301b8-160">Время одобрено, и нет изменений или увеличения оплачиваемых часов в процессе утверждения.</span><span class="sxs-lookup"><span data-stu-id="301b8-160">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="301b8-161">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="301b8-161">Cost actual</span></span></td>
<td><span data-ttu-id="301b8-162">Валюта единицы по контракту</span><span class="sxs-lookup"><span data-stu-id="301b8-162">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="301b8-163">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="301b8-163">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="301b8-164">Валюта единицы по контракту</span><span class="sxs-lookup"><span data-stu-id="301b8-164">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="301b8-165">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="301b8-165">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="301b8-166">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="301b8-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="301b8-167">Фактическая сумма продаж с невыставленными счетами — оплачиваемые</span><span class="sxs-lookup"><span data-stu-id="301b8-167">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="301b8-168">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="301b8-168">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="301b8-169">Время одобрено, и имеется уменьшение оплачиваемых часов в процессе утверждения.</span><span class="sxs-lookup"><span data-stu-id="301b8-169">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="301b8-170">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="301b8-170">Cost actual</span></span></td>
<td><span data-ttu-id="301b8-171">Валюта единицы по контракту</span><span class="sxs-lookup"><span data-stu-id="301b8-171">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="301b8-172">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="301b8-172">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="301b8-173">Валюта единицы по контракту</span><span class="sxs-lookup"><span data-stu-id="301b8-173">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="301b8-174">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="301b8-174">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="301b8-175">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="301b8-175">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="301b8-176">Фактическое количество продаж без выставления счета — оплачивается для нового количества</span><span class="sxs-lookup"><span data-stu-id="301b8-176">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="301b8-177">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="301b8-177">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="301b8-178">Фактическое количество продаж без выставления счета — не оплачивается для разницы</span><span class="sxs-lookup"><span data-stu-id="301b8-178">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="301b8-179">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="301b8-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="301b8-180">Счет одобрен, и нет изменения или происходит увеличение оплачиваемых часов в процессе утверждения.</span><span class="sxs-lookup"><span data-stu-id="301b8-180">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="301b8-181">Обращение продаж без выставления счета</span><span class="sxs-lookup"><span data-stu-id="301b8-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="301b8-182">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="301b8-182">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="301b8-183">Продажи с выставленными счетами для вехи</span><span class="sxs-lookup"><span data-stu-id="301b8-183">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="301b8-184">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="301b8-184">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="301b8-185">Нет данных</span><span class="sxs-lookup"><span data-stu-id="301b8-185">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="301b8-186">Нет данных</span><span class="sxs-lookup"><span data-stu-id="301b8-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="301b8-187">Продажи с выставлением счета</span><span class="sxs-lookup"><span data-stu-id="301b8-187">Billed sales</span></span></td>
<td><span data-ttu-id="301b8-188">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="301b8-188">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="301b8-189">Счет одобрен, и имеется уменьшение оплачиваемых часов в процессе утверждения.</span><span class="sxs-lookup"><span data-stu-id="301b8-189">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="301b8-190">Обращение продаж без выставления счета</span><span class="sxs-lookup"><span data-stu-id="301b8-190">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="301b8-191">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="301b8-191">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="301b8-192">Нет данных</span><span class="sxs-lookup"><span data-stu-id="301b8-192">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="301b8-193">Нет данных</span><span class="sxs-lookup"><span data-stu-id="301b8-193">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="301b8-194">Нет данных</span><span class="sxs-lookup"><span data-stu-id="301b8-194">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="301b8-195">Нет данных</span><span class="sxs-lookup"><span data-stu-id="301b8-195">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="301b8-196">Продажи с выставленными счетами — оплачивается для нового количества</span><span class="sxs-lookup"><span data-stu-id="301b8-196">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="301b8-197">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="301b8-197">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="301b8-198">Продажи с выставленным счетом — не оплачивается для разницы</span><span class="sxs-lookup"><span data-stu-id="301b8-198">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="301b8-199">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="301b8-199">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="301b8-200">Счет исправлен для увеличения оплачиваемого количества.</span><span class="sxs-lookup"><span data-stu-id="301b8-200">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="301b8-201">Продаж с выставленным счетом — обращение</span><span class="sxs-lookup"><span data-stu-id="301b8-201">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="301b8-202">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="301b8-202">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="301b8-203">Обращение продаж с выставленными счетами для вехи</span><span class="sxs-lookup"><span data-stu-id="301b8-203">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="301b8-204">Изменение в состоянии вехи с <strong>Выставлен счет</strong> на <strong>Готов к выставлению счета</strong></span><span class="sxs-lookup"><span data-stu-id="301b8-204">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="301b8-205">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="301b8-205">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="301b8-206">Нет данных</span><span class="sxs-lookup"><span data-stu-id="301b8-206">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="301b8-207">Нет данных</span><span class="sxs-lookup"><span data-stu-id="301b8-207">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="301b8-208">Продажи с выставлением счета</span><span class="sxs-lookup"><span data-stu-id="301b8-208">Billed sales</span></span></td>
<td><span data-ttu-id="301b8-209">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="301b8-209">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="301b8-210">Счет исправлен для уменьшения оплачиваемого количества.</span><span class="sxs-lookup"><span data-stu-id="301b8-210">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="301b8-211">Продаж с выставленным счетом — обращение</span><span class="sxs-lookup"><span data-stu-id="301b8-211">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="301b8-212">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="301b8-212">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="301b8-213">Продажи с выставленными счетами для нового количества</span><span class="sxs-lookup"><span data-stu-id="301b8-213">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="301b8-214">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="301b8-214">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="301b8-215">Продажи без выставленного счета — оплачивается для разницы</span><span class="sxs-lookup"><span data-stu-id="301b8-215">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="301b8-216">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="301b8-216">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="301b8-217">Ресурс принадлежит к подразделению, который отличается от контрактной единицы по проекту</span><span class="sxs-lookup"><span data-stu-id="301b8-217">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="301b8-218">Событие</span><span class="sxs-lookup"><span data-stu-id="301b8-218">Event</span></span></th>
<th colspan="4"><span data-ttu-id="301b8-219">Оплачиваемый или проданный проект</span><span class="sxs-lookup"><span data-stu-id="301b8-219">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="301b8-220">Проект на стадии предварительных продаж</span><span class="sxs-lookup"><span data-stu-id="301b8-220">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="301b8-221">Внутренний проект</span><span class="sxs-lookup"><span data-stu-id="301b8-221">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="301b8-222">Время и материалы</span><span class="sxs-lookup"><span data-stu-id="301b8-222">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="301b8-223">Фиксированная цена</span><span class="sxs-lookup"><span data-stu-id="301b8-223">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="301b8-224">Фактические</span><span class="sxs-lookup"><span data-stu-id="301b8-224">Actuals</span></span></th>
<th><span data-ttu-id="301b8-225">Валюта транзакции</span><span class="sxs-lookup"><span data-stu-id="301b8-225">Transaction currency</span></span></th>
<th><span data-ttu-id="301b8-226">Фиксированная цена</span><span class="sxs-lookup"><span data-stu-id="301b8-226">Fixed price</span></span></th>
<th><span data-ttu-id="301b8-227">Валюта транзакции</span><span class="sxs-lookup"><span data-stu-id="301b8-227">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="301b8-228">Создана запись времени.</span><span class="sxs-lookup"><span data-stu-id="301b8-228">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="301b8-229">Нет действий в сущности фактических данных</span><span class="sxs-lookup"><span data-stu-id="301b8-229">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="301b8-230">Запись времени отправлена.</span><span class="sxs-lookup"><span data-stu-id="301b8-230">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="301b8-231">Нет действий в сущности фактических данных</span><span class="sxs-lookup"><span data-stu-id="301b8-231">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="301b8-232">Время одобрено, и нет изменений или увеличения оплачиваемых часов в процессе утверждения.</span><span class="sxs-lookup"><span data-stu-id="301b8-232">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="301b8-233">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="301b8-233">Cost actual</span></span></td>
<td><span data-ttu-id="301b8-234">Валюта единицы по контракту</span><span class="sxs-lookup"><span data-stu-id="301b8-234">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="301b8-235">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="301b8-235">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="301b8-236">Валюта единицы по контракту</span><span class="sxs-lookup"><span data-stu-id="301b8-236">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="301b8-237">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="301b8-237">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="301b8-238">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="301b8-238">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="301b8-239">Фактическая сумма продаж с невыставленными счетами — оплачиваемые</span><span class="sxs-lookup"><span data-stu-id="301b8-239">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="301b8-240">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="301b8-240">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="301b8-241">Стоимость единицы распределения ресурсов</span><span class="sxs-lookup"><span data-stu-id="301b8-241">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="301b8-242">Валюта единицы распределения ресурсов</span><span class="sxs-lookup"><span data-stu-id="301b8-242">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="301b8-243">Внутрихолдинговые продажи</span><span class="sxs-lookup"><span data-stu-id="301b8-243">Interorganizational sales</span></span></td>
<td><span data-ttu-id="301b8-244">Валюта единицы по контракту</span><span class="sxs-lookup"><span data-stu-id="301b8-244">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="301b8-245">Время одобрено, и имеется уменьшение оплачиваемых часов в процессе утверждения.</span><span class="sxs-lookup"><span data-stu-id="301b8-245">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="301b8-246">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="301b8-246">Cost actual</span></span></td>
<td><span data-ttu-id="301b8-247">Валюта единицы по контракту</span><span class="sxs-lookup"><span data-stu-id="301b8-247">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="301b8-248">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="301b8-248">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="301b8-249">Валюта единицы по контракту</span><span class="sxs-lookup"><span data-stu-id="301b8-249">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="301b8-250">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="301b8-250">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="301b8-251">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="301b8-251">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="301b8-252">Стоимость единицы распределения ресурсов</span><span class="sxs-lookup"><span data-stu-id="301b8-252">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="301b8-253">Валюта единицы распределения ресурсов</span><span class="sxs-lookup"><span data-stu-id="301b8-253">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="301b8-254">Внутрихолдинговые продажи</span><span class="sxs-lookup"><span data-stu-id="301b8-254">Interorganizational sales</span></span></td>
<td><span data-ttu-id="301b8-255">Валюта единицы по контракту</span><span class="sxs-lookup"><span data-stu-id="301b8-255">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="301b8-256">Фактическое количество продаж без выставления счета — оплачивается для нового количества</span><span class="sxs-lookup"><span data-stu-id="301b8-256">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="301b8-257">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="301b8-257">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="301b8-258">Фактическое количество продаж без выставления счета — не оплачивается для разницы</span><span class="sxs-lookup"><span data-stu-id="301b8-258">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="301b8-259">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="301b8-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="301b8-260">Счет одобрен, и нет изменения или происходит увеличение оплачиваемых часов в процессе утверждения.</span><span class="sxs-lookup"><span data-stu-id="301b8-260">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="301b8-261">Обращение продаж без выставления счета</span><span class="sxs-lookup"><span data-stu-id="301b8-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="301b8-262">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="301b8-262">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="301b8-263">Продажи с выставленными счетами для вехи</span><span class="sxs-lookup"><span data-stu-id="301b8-263">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="301b8-264">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="301b8-264">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="301b8-265">Нет данных</span><span class="sxs-lookup"><span data-stu-id="301b8-265">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="301b8-266">Нет данных</span><span class="sxs-lookup"><span data-stu-id="301b8-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="301b8-267">Продажи с выставлением счета</span><span class="sxs-lookup"><span data-stu-id="301b8-267">Billed sales</span></span></td>
<td><span data-ttu-id="301b8-268">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="301b8-268">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="301b8-269">Счет одобрен, и имеется уменьшение оплачиваемых часов в процессе утверждения.</span><span class="sxs-lookup"><span data-stu-id="301b8-269">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="301b8-270">Обращение продаж без выставления счета</span><span class="sxs-lookup"><span data-stu-id="301b8-270">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="301b8-271">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="301b8-271">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="301b8-272">Нет данных</span><span class="sxs-lookup"><span data-stu-id="301b8-272">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="301b8-273">Нет данных</span><span class="sxs-lookup"><span data-stu-id="301b8-273">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="301b8-274">Нет данных</span><span class="sxs-lookup"><span data-stu-id="301b8-274">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="301b8-275">Нет данных</span><span class="sxs-lookup"><span data-stu-id="301b8-275">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="301b8-276">Продажи с выставленными счетами — оплачивается для нового количества</span><span class="sxs-lookup"><span data-stu-id="301b8-276">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="301b8-277">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="301b8-277">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="301b8-278">Продажи с выставленным счетом — не оплачивается для разницы</span><span class="sxs-lookup"><span data-stu-id="301b8-278">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="301b8-279">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="301b8-279">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="301b8-280">Счет исправлен для увеличения оплачиваемого количества.</span><span class="sxs-lookup"><span data-stu-id="301b8-280">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="301b8-281">Продаж с выставленным счетом — обращение</span><span class="sxs-lookup"><span data-stu-id="301b8-281">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="301b8-282">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="301b8-282">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="301b8-283">Обращение продаж с выставленными счетами для вехи</span><span class="sxs-lookup"><span data-stu-id="301b8-283">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="301b8-284">Изменение в состоянии вехи с <strong>Выставлен счет</strong> на <strong>Готов к выставлению счета</strong></span><span class="sxs-lookup"><span data-stu-id="301b8-284">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="301b8-285">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="301b8-285">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="301b8-286">Нет данных</span><span class="sxs-lookup"><span data-stu-id="301b8-286">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="301b8-287">Нет данных</span><span class="sxs-lookup"><span data-stu-id="301b8-287">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="301b8-288">Продажи с выставлением счета</span><span class="sxs-lookup"><span data-stu-id="301b8-288">Billed sales</span></span></td>
<td><span data-ttu-id="301b8-289">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="301b8-289">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="301b8-290">Счет исправлен для уменьшения оплачиваемого количества.</span><span class="sxs-lookup"><span data-stu-id="301b8-290">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="301b8-291">Продаж с выставленным счетом — обращение</span><span class="sxs-lookup"><span data-stu-id="301b8-291">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="301b8-292">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="301b8-292">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="301b8-293">Продажи с выставленными счетами для нового количества</span><span class="sxs-lookup"><span data-stu-id="301b8-293">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="301b8-294">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="301b8-294">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="301b8-295">Продажи без выставленного счета — оплачивается для разницы</span><span class="sxs-lookup"><span data-stu-id="301b8-295">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="301b8-296">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="301b8-296">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
