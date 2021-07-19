---
title: Фактические значения
description: Этот раздел содержит информацию о том, как работать с фактическими значениями в Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 9e046602a3005930c41ab8c50472d5b1a72303c6
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368627"
---
# <a name="actuals"></a><span data-ttu-id="2086c-103">Фактические значения</span><span class="sxs-lookup"><span data-stu-id="2086c-103">Actuals</span></span> 

<span data-ttu-id="2086c-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="2086c-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2086c-105">Фактические данные представляют собой проанализированный и утвержденный финансовый и календарный прогресс по проекту.</span><span class="sxs-lookup"><span data-stu-id="2086c-105">Actuals represent the reviewed and approved financial and schedule progress on a project.</span></span> <span data-ttu-id="2086c-106">Они создаются в результате утверждения записей о времени, расходах, использовании материалов, а также записей журналов и счетов.</span><span class="sxs-lookup"><span data-stu-id="2086c-106">They are created as a result of approval of time, expense, material usage entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="2086c-107">Отправка строк журналов и времени</span><span class="sxs-lookup"><span data-stu-id="2086c-107">Journal lines and time submission</span></span>

<span data-ttu-id="2086c-108">Для получения дополнительной информации о записи времени см. тему [Обзор записи времени](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="2086c-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="2086c-109">Время и материалы</span><span class="sxs-lookup"><span data-stu-id="2086c-109">Time and materials</span></span>

<span data-ttu-id="2086c-110">Когда отправляемая запись времени связана с проектом, который сопоставлен со строкой контракта на время и материалы, система создает две строки журнала: одну для затрат и одну для продаж, за которые не выставлен счет.</span><span class="sxs-lookup"><span data-stu-id="2086c-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="2086c-111">Фиксированная цена</span><span class="sxs-lookup"><span data-stu-id="2086c-111">Fixed price</span></span>

<span data-ttu-id="2086c-112">Когда отправляемая запись времени связана с проектом, который сопоставляется со строкой контракта с фиксированной ценой, система создает одну строку журнала для стоимости.</span><span class="sxs-lookup"><span data-stu-id="2086c-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="2086c-113">Цены по умолчанию</span><span class="sxs-lookup"><span data-stu-id="2086c-113">Default pricing</span></span>

<span data-ttu-id="2086c-114">Логика создания цен по умолчанию находится в строке журнала.</span><span class="sxs-lookup"><span data-stu-id="2086c-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="2086c-115">Значения полей из записи времени копируются в строку журнала.</span><span class="sxs-lookup"><span data-stu-id="2086c-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="2086c-116">Эти значения включают дату транзакции, строку контракта, с которой сопоставлен проект, и результат валюты в соответствующем прайс-листе.</span><span class="sxs-lookup"><span data-stu-id="2086c-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="2086c-117">Поля, которые влияют на цены по умолчанию, например **Роль** и **Единица распределения ресурсов** используются для определения соответствующей цены в строке журнала.</span><span class="sxs-lookup"><span data-stu-id="2086c-117">The fields that affect default pricing, such as **Role** and **Resourcing Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="2086c-118">Вы можете добавить настраиваемое поле к записи времени.</span><span class="sxs-lookup"><span data-stu-id="2086c-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="2086c-119">Если вы хотите, чтобы значение поля распространялось на фактические значения, создайте поле в таблицах **Фактические значения** и **Строка журнала**.</span><span class="sxs-lookup"><span data-stu-id="2086c-119">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="2086c-120">Используйте настраиваемый код для распространения значения выбранного поля из "Запись времени" в "Фактические значения" по строке журнала с помощью источников транзакции.</span><span class="sxs-lookup"><span data-stu-id="2086c-120">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="2086c-121">Для получения дополнительной информации об источниках транзакций и подключениях см. [Связь фактических данных с исходными записями](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="2086c-121">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="2086c-122">Строки журнала и базовая отправка расходов</span><span class="sxs-lookup"><span data-stu-id="2086c-122">Journal lines and basic expense submission</span></span>

<span data-ttu-id="2086c-123">Дополнительные сведения о записи расходов см. в теме [Обзор расходов](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="2086c-123">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="2086c-124">Время и материалы</span><span class="sxs-lookup"><span data-stu-id="2086c-124">Time and materials</span></span>

<span data-ttu-id="2086c-125">Когда отправляемая базовая запись затрат связана с проектом, который сопоставлен со строкой контракта на время и материалы, система создает две строки журнала: одну для затрат и одну для продаж, за которые не выставлен счет.</span><span class="sxs-lookup"><span data-stu-id="2086c-125">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="2086c-126">Фиксированная цена</span><span class="sxs-lookup"><span data-stu-id="2086c-126">Fixed price</span></span>

<span data-ttu-id="2086c-127">Когда отправленная базовая запись расхода связана с проектом, который сопоставляется со строкой контракта с фиксированной ценой, система создает одну строку журнала для стоимости.</span><span class="sxs-lookup"><span data-stu-id="2086c-127">When a submitted basic expense entry is linked to a project that's mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="2086c-128">Цены по умолчанию</span><span class="sxs-lookup"><span data-stu-id="2086c-128">Default pricing</span></span>

<span data-ttu-id="2086c-129">Логика ввода цен по умолчанию для расходов основана на категории расходов.</span><span class="sxs-lookup"><span data-stu-id="2086c-129">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="2086c-130">Дата транзакции, строка контракта, с которой сопоставлен проект, и валюта все используются для определения соответствующего прайс-листа.</span><span class="sxs-lookup"><span data-stu-id="2086c-130">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="2086c-131">Поля, которые влияют на цены по умолчанию, например **Категория проводки** и **Единица распределения ресурсов** используются для определения соответствующей цены в строке журнала.</span><span class="sxs-lookup"><span data-stu-id="2086c-131">The fields that affect default pricing, such as **Transaction Category** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="2086c-132">Однако это работает только в том случае, если в прайс-листе указан метод ценообразования **Цена за единицу**.</span><span class="sxs-lookup"><span data-stu-id="2086c-132">However, this only works when the pricing method in the price list is **Price per unit**.</span></span> <span data-ttu-id="2086c-133">Если метод ценообразования — **По себестоимости** или **Наценка по стоимости**, цена, введенная при создании записи расхода, используется для стоимости, а цена в строке журнала продаж рассчитывается на основе метода ценообразования.</span><span class="sxs-lookup"><span data-stu-id="2086c-133">If pricing method is **At cost** or **Markup over cost**, the price entered when the expense entry is created is used for cost and the price on the sales journal line is calculated based on the pricing method.</span></span> 

<span data-ttu-id="2086c-134">Вы можете добавить настраиваемое поле в запись расхода.</span><span class="sxs-lookup"><span data-stu-id="2086c-134">You can add a custom field on the expense entry.</span></span> <span data-ttu-id="2086c-135">Если вы хотите, чтобы значение поля распространялось на фактические значения, создайте поле в таблицах **Фактические значения** и **Строка журнала**.</span><span class="sxs-lookup"><span data-stu-id="2086c-135">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="2086c-136">Используйте настраиваемый код для распространения значения выбранного поля из "Запись времени" в "Фактические значения" по строке журнала с помощью источников транзакции.</span><span class="sxs-lookup"><span data-stu-id="2086c-136">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="2086c-137">Для получения дополнительной информации об источниках транзакций и подключениях см. [Связь фактических данных с исходными записями](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="2086c-137">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-material-usage-log-submission"></a><span data-ttu-id="2086c-138">Отправка строк журнала и журнала использования материалов</span><span class="sxs-lookup"><span data-stu-id="2086c-138">Journal lines and material usage log submission</span></span>

<span data-ttu-id="2086c-139">Для получения дополнительной информации о записи расходов см. [Журнал использования материалов](../material/material-usage-log.md).</span><span class="sxs-lookup"><span data-stu-id="2086c-139">For more information about expense entry, see [Material Usage Log](../material/material-usage-log.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="2086c-140">Время и материалы</span><span class="sxs-lookup"><span data-stu-id="2086c-140">Time and materials</span></span>

<span data-ttu-id="2086c-141">Когда отправленная запись журнала использования материалов связана с проектом, который сопоставлен со строкой контракта на время и материалы, система создает две строки журнала: одну для стоимости и одну для продаж без выставления счета.</span><span class="sxs-lookup"><span data-stu-id="2086c-141">When a submitted material usage log entry is linked to a project that is mapped to a time and materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="2086c-142">Фиксированная цена</span><span class="sxs-lookup"><span data-stu-id="2086c-142">Fixed price</span></span>

<span data-ttu-id="2086c-143">Когда отправленная запись журнала использования материала связана с проектом, который сопоставляется со строкой контракта с фиксированной ценой, система создает одну строку журнала для стоимости.</span><span class="sxs-lookup"><span data-stu-id="2086c-143">When a submitted material usage log entry is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="2086c-144">Цены по умолчанию</span><span class="sxs-lookup"><span data-stu-id="2086c-144">Default pricing</span></span>

<span data-ttu-id="2086c-145">Логика ввода цен по умолчанию для материала основана на комбинации продукта и единицы.</span><span class="sxs-lookup"><span data-stu-id="2086c-145">The logic for entering default prices for material is based on the product and unit combination.</span></span> <span data-ttu-id="2086c-146">Дата транзакции, строка контракта, с которой сопоставлен проект, и валюта все используются для определения соответствующего прайс-листа.</span><span class="sxs-lookup"><span data-stu-id="2086c-146">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="2086c-147">Поля, которые влияют на цены по умолчанию, например **Артикул** и **Единица** используются для определения соответствующей цены в строке журнала.</span><span class="sxs-lookup"><span data-stu-id="2086c-147">The fields that affect default pricing, such as **Product ID** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="2086c-148">Однако это работает только для продуктов из каталога.</span><span class="sxs-lookup"><span data-stu-id="2086c-148">However, this only works for catalog products.</span></span> <span data-ttu-id="2086c-149">Для вписанных продуктов цена, введенная при создании записи в журнале использования материала, используется для стоимости и цены продажи в строках журнала.</span><span class="sxs-lookup"><span data-stu-id="2086c-149">For write-in products, the price entered when the material usage log entry is created is used for cost and sales price on the journal lines.</span></span> 

<span data-ttu-id="2086c-150">Вы можете добавить настраиваемое поле в запись **Журнал использования материалов**.</span><span class="sxs-lookup"><span data-stu-id="2086c-150">You can add a custom field on the **Material Usage Log** entry.</span></span> <span data-ttu-id="2086c-151">Если вы хотите, чтобы значение поля распространялось на фактические значения, создайте поле в таблицах **Фактические значения** и **Строка журнала**.</span><span class="sxs-lookup"><span data-stu-id="2086c-151">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="2086c-152">Используйте настраиваемый код для распространения значения выбранного поля из "Запись времени" в "Фактические значения" по строке журнала с помощью источников транзакции.</span><span class="sxs-lookup"><span data-stu-id="2086c-152">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="2086c-153">Для получения дополнительной информации об источниках транзакций и подключениях см. [Связь фактических данных с исходными записями](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="2086c-153">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="2086c-154">Использование журналов записей для записи стоимости</span><span class="sxs-lookup"><span data-stu-id="2086c-154">Use entry journals to record costs</span></span>

<span data-ttu-id="2086c-155">Журналы можно использовать для записи стоимости или дохода в классах проводок по материалам, сборам, времени, расходам и налогам.</span><span class="sxs-lookup"><span data-stu-id="2086c-155">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="2086c-156">Журналы могут использоваться для следующих целей:</span><span class="sxs-lookup"><span data-stu-id="2086c-156">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="2086c-157">Перемещение фактических данных транзакций из другой системы в Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="2086c-157">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="2086c-158">Запись затрат, которые произошли в другой системе.</span><span class="sxs-lookup"><span data-stu-id="2086c-158">Record costs that occurred in another system.</span></span> <span data-ttu-id="2086c-159">Эти затраты могут включать затраты на закупку или субподряд.</span><span class="sxs-lookup"><span data-stu-id="2086c-159">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2086c-160">Приложение не проверяет тип строки журнала или соответствующие цены, введенные в строке журнала.</span><span class="sxs-lookup"><span data-stu-id="2086c-160">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="2086c-161">Следовательно, только пользователь, который полностью осознает влияние на учет от фактических данных по проекту должен использовать журналы записей для создания фактических данных.</span><span class="sxs-lookup"><span data-stu-id="2086c-161">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="2086c-162">Из-за влияния этого типа журнала вам следует тщательно выбирать, у кого есть доступ для создания журналов входа.</span><span class="sxs-lookup"><span data-stu-id="2086c-162">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>

## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="2086c-163">Запись фактических данных по событиям проекта</span><span class="sxs-lookup"><span data-stu-id="2086c-163">Record actuals based on project events</span></span>

<span data-ttu-id="2086c-164">Project Operations записывает финансовые транзакции, которые происходят в ходе проекта.</span><span class="sxs-lookup"><span data-stu-id="2086c-164">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="2086c-165">Эти транзакции записываются как фактические значения.</span><span class="sxs-lookup"><span data-stu-id="2086c-165">These transactions are recorded as actuals.</span></span> <span data-ttu-id="2086c-166">В следующих таблицах отображаются различные типы созданных фактических данных, в зависимости от того, является ли проект проектом "время и материалы" или проектом с фиксированной ценой.</span><span class="sxs-lookup"><span data-stu-id="2086c-166">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="2086c-167">Ресурс принадлежит к тому же подразделению, что и контрактная единица по проекту</span><span class="sxs-lookup"><span data-stu-id="2086c-167">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="2086c-168">Событие</span><span class="sxs-lookup"><span data-stu-id="2086c-168">Event</span></span></th>
<th colspan="4"><span data-ttu-id="2086c-169">Оплачиваемый или проданный проект</span><span class="sxs-lookup"><span data-stu-id="2086c-169">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="2086c-170">Проект на стадии предварительных продаж</span><span class="sxs-lookup"><span data-stu-id="2086c-170">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="2086c-171">Внутренний проект</span><span class="sxs-lookup"><span data-stu-id="2086c-171">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="2086c-172">Время и материалы</span><span class="sxs-lookup"><span data-stu-id="2086c-172">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="2086c-173">Фиксированная цена</span><span class="sxs-lookup"><span data-stu-id="2086c-173">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="2086c-174">Фактические</span><span class="sxs-lookup"><span data-stu-id="2086c-174">Actuals</span></span></th>
<th><span data-ttu-id="2086c-175">Валюта транзакции</span><span class="sxs-lookup"><span data-stu-id="2086c-175">Transaction currency</span></span></th>
<th><span data-ttu-id="2086c-176">Фиксированная цена</span><span class="sxs-lookup"><span data-stu-id="2086c-176">Fixed price</span></span></th>
<th><span data-ttu-id="2086c-177">Валюта транзакции</span><span class="sxs-lookup"><span data-stu-id="2086c-177">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2086c-178">Создана запись времени.</span><span class="sxs-lookup"><span data-stu-id="2086c-178">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="2086c-179">Нет действий в сущности фактических данных</span><span class="sxs-lookup"><span data-stu-id="2086c-179">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2086c-180">Запись времени отправлена.</span><span class="sxs-lookup"><span data-stu-id="2086c-180">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="2086c-181">Нет действий в сущности фактических данных</span><span class="sxs-lookup"><span data-stu-id="2086c-181">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="2086c-182">Время одобрено, и нет изменений или увеличения оплачиваемых часов в процессе утверждения.</span><span class="sxs-lookup"><span data-stu-id="2086c-182">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="2086c-183">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="2086c-183">Cost actual</span></span></td>
<td><span data-ttu-id="2086c-184">Валюта единицы по контракту</span><span class="sxs-lookup"><span data-stu-id="2086c-184">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="2086c-185">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="2086c-185">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="2086c-186">Валюта единицы по контракту</span><span class="sxs-lookup"><span data-stu-id="2086c-186">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="2086c-187">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="2086c-187">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="2086c-188">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="2086c-188">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2086c-189">Фактическая сумма продаж с невыставленными счетами — оплачиваемые</span><span class="sxs-lookup"><span data-stu-id="2086c-189">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="2086c-190">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="2086c-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="2086c-191">Время одобрено, и имеется уменьшение оплачиваемых часов в процессе утверждения.</span><span class="sxs-lookup"><span data-stu-id="2086c-191">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="2086c-192">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="2086c-192">Cost actual</span></span></td>
<td><span data-ttu-id="2086c-193">Валюта единицы по контракту</span><span class="sxs-lookup"><span data-stu-id="2086c-193">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="2086c-194">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="2086c-194">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="2086c-195">Валюта единицы по контракту</span><span class="sxs-lookup"><span data-stu-id="2086c-195">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="2086c-196">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="2086c-196">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="2086c-197">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="2086c-197">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2086c-198">Фактическое количество продаж без выставления счета — оплачивается для нового количества</span><span class="sxs-lookup"><span data-stu-id="2086c-198">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="2086c-199">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="2086c-199">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2086c-200">Фактическое количество продаж без выставления счета — не оплачивается для разницы</span><span class="sxs-lookup"><span data-stu-id="2086c-200">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="2086c-201">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="2086c-201">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="2086c-202">Счет одобрен, и нет изменения или происходит увеличение оплачиваемых часов в процессе утверждения.</span><span class="sxs-lookup"><span data-stu-id="2086c-202">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="2086c-203">Обращение продаж без выставления счета</span><span class="sxs-lookup"><span data-stu-id="2086c-203">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="2086c-204">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="2086c-204">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="2086c-205">Продажи с выставленными счетами для вехи</span><span class="sxs-lookup"><span data-stu-id="2086c-205">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="2086c-206">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="2086c-206">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="2086c-207">Нет данных</span><span class="sxs-lookup"><span data-stu-id="2086c-207">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="2086c-208">Нет данных</span><span class="sxs-lookup"><span data-stu-id="2086c-208">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2086c-209">Продажи с выставлением счета</span><span class="sxs-lookup"><span data-stu-id="2086c-209">Billed sales</span></span></td>
<td><span data-ttu-id="2086c-210">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="2086c-210">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="2086c-211">Счет одобрен, и имеется уменьшение оплачиваемых часов в процессе утверждения.</span><span class="sxs-lookup"><span data-stu-id="2086c-211">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="2086c-212">Обращение продаж без выставления счета</span><span class="sxs-lookup"><span data-stu-id="2086c-212">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="2086c-213">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="2086c-213">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="2086c-214">Нет данных</span><span class="sxs-lookup"><span data-stu-id="2086c-214">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="2086c-215">Нет данных</span><span class="sxs-lookup"><span data-stu-id="2086c-215">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="2086c-216">Нет данных</span><span class="sxs-lookup"><span data-stu-id="2086c-216">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="2086c-217">Нет данных</span><span class="sxs-lookup"><span data-stu-id="2086c-217">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2086c-218">Продажи с выставленными счетами — оплачивается для нового количества</span><span class="sxs-lookup"><span data-stu-id="2086c-218">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="2086c-219">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="2086c-219">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2086c-220">Продажи с выставленным счетом — не оплачивается для разницы</span><span class="sxs-lookup"><span data-stu-id="2086c-220">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="2086c-221">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="2086c-221">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="2086c-222">Счет исправлен для увеличения оплачиваемого количества.</span><span class="sxs-lookup"><span data-stu-id="2086c-222">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="2086c-223">Продаж с выставленным счетом — обращение</span><span class="sxs-lookup"><span data-stu-id="2086c-223">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="2086c-224">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="2086c-224">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="2086c-225">Обращение продаж с выставленными счетами для вехи</span><span class="sxs-lookup"><span data-stu-id="2086c-225">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="2086c-226">Изменение в состоянии вехи с <strong>Выставлен счет</strong> на <strong>Готов к выставлению счета</strong></span><span class="sxs-lookup"><span data-stu-id="2086c-226">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="2086c-227">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="2086c-227">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="2086c-228">Нет данных</span><span class="sxs-lookup"><span data-stu-id="2086c-228">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="2086c-229">Нет данных</span><span class="sxs-lookup"><span data-stu-id="2086c-229">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2086c-230">Продажи с выставлением счета</span><span class="sxs-lookup"><span data-stu-id="2086c-230">Billed sales</span></span></td>
<td><span data-ttu-id="2086c-231">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="2086c-231">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="2086c-232">Счет исправлен для уменьшения оплачиваемого количества.</span><span class="sxs-lookup"><span data-stu-id="2086c-232">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="2086c-233">Продаж с выставленным счетом — обращение</span><span class="sxs-lookup"><span data-stu-id="2086c-233">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="2086c-234">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="2086c-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2086c-235">Продажи с выставленными счетами для нового количества</span><span class="sxs-lookup"><span data-stu-id="2086c-235">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="2086c-236">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="2086c-236">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2086c-237">Продажи без выставленного счета — оплачивается для разницы</span><span class="sxs-lookup"><span data-stu-id="2086c-237">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="2086c-238">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="2086c-238">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="2086c-239">Ресурс принадлежит к подразделению, который отличается от контрактной единицы по проекту</span><span class="sxs-lookup"><span data-stu-id="2086c-239">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="2086c-240">Событие</span><span class="sxs-lookup"><span data-stu-id="2086c-240">Event</span></span></th>
<th colspan="4"><span data-ttu-id="2086c-241">Оплачиваемый или проданный проект</span><span class="sxs-lookup"><span data-stu-id="2086c-241">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="2086c-242">Проект на стадии предварительных продаж</span><span class="sxs-lookup"><span data-stu-id="2086c-242">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="2086c-243">Внутренний проект</span><span class="sxs-lookup"><span data-stu-id="2086c-243">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="2086c-244">Время и материалы</span><span class="sxs-lookup"><span data-stu-id="2086c-244">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="2086c-245">Фиксированная цена</span><span class="sxs-lookup"><span data-stu-id="2086c-245">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="2086c-246">Фактические</span><span class="sxs-lookup"><span data-stu-id="2086c-246">Actuals</span></span></th>
<th><span data-ttu-id="2086c-247">Валюта транзакции</span><span class="sxs-lookup"><span data-stu-id="2086c-247">Transaction currency</span></span></th>
<th><span data-ttu-id="2086c-248">Фиксированная цена</span><span class="sxs-lookup"><span data-stu-id="2086c-248">Fixed price</span></span></th>
<th><span data-ttu-id="2086c-249">Валюта транзакции</span><span class="sxs-lookup"><span data-stu-id="2086c-249">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2086c-250">Создана запись времени.</span><span class="sxs-lookup"><span data-stu-id="2086c-250">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="2086c-251">Нет действий в сущности фактических данных</span><span class="sxs-lookup"><span data-stu-id="2086c-251">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2086c-252">Запись времени отправлена.</span><span class="sxs-lookup"><span data-stu-id="2086c-252">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="2086c-253">Нет действий в сущности фактических данных</span><span class="sxs-lookup"><span data-stu-id="2086c-253">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="2086c-254">Время одобрено, и нет изменений или увеличения оплачиваемых часов в процессе утверждения.</span><span class="sxs-lookup"><span data-stu-id="2086c-254">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="2086c-255">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="2086c-255">Cost actual</span></span></td>
<td><span data-ttu-id="2086c-256">Валюта единицы по контракту</span><span class="sxs-lookup"><span data-stu-id="2086c-256">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="2086c-257">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="2086c-257">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="2086c-258">Валюта единицы по контракту</span><span class="sxs-lookup"><span data-stu-id="2086c-258">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="2086c-259">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="2086c-259">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="2086c-260">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="2086c-260">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2086c-261">Фактическая сумма продаж с невыставленными счетами — оплачиваемые</span><span class="sxs-lookup"><span data-stu-id="2086c-261">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="2086c-262">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="2086c-262">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2086c-263">Стоимость единицы распределения ресурсов</span><span class="sxs-lookup"><span data-stu-id="2086c-263">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="2086c-264">Валюта единицы распределения ресурсов</span><span class="sxs-lookup"><span data-stu-id="2086c-264">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2086c-265">Внутрихолдинговые продажи</span><span class="sxs-lookup"><span data-stu-id="2086c-265">Interorganizational sales</span></span></td>
<td><span data-ttu-id="2086c-266">Валюта единицы по контракту</span><span class="sxs-lookup"><span data-stu-id="2086c-266">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="2086c-267">Время одобрено, и имеется уменьшение оплачиваемых часов в процессе утверждения.</span><span class="sxs-lookup"><span data-stu-id="2086c-267">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="2086c-268">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="2086c-268">Cost actual</span></span></td>
<td><span data-ttu-id="2086c-269">Валюта единицы по контракту</span><span class="sxs-lookup"><span data-stu-id="2086c-269">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="2086c-270">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="2086c-270">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="2086c-271">Валюта единицы по контракту</span><span class="sxs-lookup"><span data-stu-id="2086c-271">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="2086c-272">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="2086c-272">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="2086c-273">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="2086c-273">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2086c-274">Стоимость единицы распределения ресурсов</span><span class="sxs-lookup"><span data-stu-id="2086c-274">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="2086c-275">Валюта единицы распределения ресурсов</span><span class="sxs-lookup"><span data-stu-id="2086c-275">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2086c-276">Внутрихолдинговые продажи</span><span class="sxs-lookup"><span data-stu-id="2086c-276">Interorganizational sales</span></span></td>
<td><span data-ttu-id="2086c-277">Валюта единицы по контракту</span><span class="sxs-lookup"><span data-stu-id="2086c-277">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2086c-278">Фактическое количество продаж без выставления счета — оплачивается для нового количества</span><span class="sxs-lookup"><span data-stu-id="2086c-278">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="2086c-279">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="2086c-279">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2086c-280">Фактическое количество продаж без выставления счета — не оплачивается для разницы</span><span class="sxs-lookup"><span data-stu-id="2086c-280">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="2086c-281">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="2086c-281">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="2086c-282">Счет одобрен, и нет изменения или происходит увеличение оплачиваемых часов в процессе утверждения.</span><span class="sxs-lookup"><span data-stu-id="2086c-282">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="2086c-283">Обращение продаж без выставления счета</span><span class="sxs-lookup"><span data-stu-id="2086c-283">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="2086c-284">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="2086c-284">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="2086c-285">Продажи с выставленными счетами для вехи</span><span class="sxs-lookup"><span data-stu-id="2086c-285">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="2086c-286">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="2086c-286">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="2086c-287">Нет данных</span><span class="sxs-lookup"><span data-stu-id="2086c-287">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="2086c-288">Нет данных</span><span class="sxs-lookup"><span data-stu-id="2086c-288">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2086c-289">Продажи с выставлением счета</span><span class="sxs-lookup"><span data-stu-id="2086c-289">Billed sales</span></span></td>
<td><span data-ttu-id="2086c-290">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="2086c-290">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="2086c-291">Счет одобрен, и имеется уменьшение оплачиваемых часов в процессе утверждения.</span><span class="sxs-lookup"><span data-stu-id="2086c-291">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="2086c-292">Обращение продаж без выставления счета</span><span class="sxs-lookup"><span data-stu-id="2086c-292">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="2086c-293">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="2086c-293">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="2086c-294">Нет данных</span><span class="sxs-lookup"><span data-stu-id="2086c-294">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="2086c-295">Нет данных</span><span class="sxs-lookup"><span data-stu-id="2086c-295">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="2086c-296">Нет данных</span><span class="sxs-lookup"><span data-stu-id="2086c-296">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="2086c-297">Нет данных</span><span class="sxs-lookup"><span data-stu-id="2086c-297">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2086c-298">Продажи с выставленными счетами — оплачивается для нового количества</span><span class="sxs-lookup"><span data-stu-id="2086c-298">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="2086c-299">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="2086c-299">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2086c-300">Продажи с выставленным счетом — не оплачивается для разницы</span><span class="sxs-lookup"><span data-stu-id="2086c-300">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="2086c-301">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="2086c-301">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="2086c-302">Счет исправлен для увеличения оплачиваемого количества.</span><span class="sxs-lookup"><span data-stu-id="2086c-302">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="2086c-303">Продаж с выставленным счетом — обращение</span><span class="sxs-lookup"><span data-stu-id="2086c-303">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="2086c-304">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="2086c-304">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="2086c-305">Обращение продаж с выставленными счетами для вехи</span><span class="sxs-lookup"><span data-stu-id="2086c-305">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="2086c-306">Изменение в состоянии вехи с <strong>Выставлен счет</strong> на <strong>Готов к выставлению счета</strong></span><span class="sxs-lookup"><span data-stu-id="2086c-306">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="2086c-307">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="2086c-307">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="2086c-308">Нет данных</span><span class="sxs-lookup"><span data-stu-id="2086c-308">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="2086c-309">Нет данных</span><span class="sxs-lookup"><span data-stu-id="2086c-309">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2086c-310">Продажи с выставлением счета</span><span class="sxs-lookup"><span data-stu-id="2086c-310">Billed sales</span></span></td>
<td><span data-ttu-id="2086c-311">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="2086c-311">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="2086c-312">Счет исправлен для уменьшения оплачиваемого количества.</span><span class="sxs-lookup"><span data-stu-id="2086c-312">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="2086c-313">Продаж с выставленным счетом — обращение</span><span class="sxs-lookup"><span data-stu-id="2086c-313">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="2086c-314">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="2086c-314">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2086c-315">Продажи с выставленными счетами для нового количества</span><span class="sxs-lookup"><span data-stu-id="2086c-315">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="2086c-316">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="2086c-316">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2086c-317">Продажи без выставленного счета — оплачивается для разницы</span><span class="sxs-lookup"><span data-stu-id="2086c-317">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="2086c-318">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="2086c-318">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
