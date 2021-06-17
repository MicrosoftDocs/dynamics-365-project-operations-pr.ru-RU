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
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 78c7a9486d0338adfd7770447f21d17509e654f7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996627"
---
# <a name="actuals"></a><span data-ttu-id="1d1e3-103">Фактические значения</span><span class="sxs-lookup"><span data-stu-id="1d1e3-103">Actuals</span></span> 

<span data-ttu-id="1d1e3-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="1d1e3-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1d1e3-105">Фактические данные представляют собой проанализированный и утвержденный финансовый и календарный прогресс по проекту.</span><span class="sxs-lookup"><span data-stu-id="1d1e3-105">Actuals represent the reviewed and approved financial and schedule progress on a project.</span></span> <span data-ttu-id="1d1e3-106">Они создаются в результате утверждения записей о времени, расходах, использовании материалов, а также записей журналов и счетов.</span><span class="sxs-lookup"><span data-stu-id="1d1e3-106">They are created as a result of approval of time, expense, material usage entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="1d1e3-107">Отправка строк журналов и времени</span><span class="sxs-lookup"><span data-stu-id="1d1e3-107">Journal lines and time submission</span></span>

<span data-ttu-id="1d1e3-108">Для получения дополнительной информации о записи времени см. тему [Обзор записи времени](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1d1e3-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="1d1e3-109">Время и материалы</span><span class="sxs-lookup"><span data-stu-id="1d1e3-109">Time and materials</span></span>

<span data-ttu-id="1d1e3-110">Когда отправляемая запись времени связана с проектом, который сопоставлен со строкой контракта на время и материалы, система создает две строки журнала: одну для затрат и одну для продаж, за которые не выставлен счет.</span><span class="sxs-lookup"><span data-stu-id="1d1e3-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="1d1e3-111">Фиксированная цена</span><span class="sxs-lookup"><span data-stu-id="1d1e3-111">Fixed price</span></span>

<span data-ttu-id="1d1e3-112">Когда отправляемая запись времени связана с проектом, который сопоставляется со строкой контракта с фиксированной ценой, система создает одну строку журнала для стоимости.</span><span class="sxs-lookup"><span data-stu-id="1d1e3-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="1d1e3-113">Цены по умолчанию</span><span class="sxs-lookup"><span data-stu-id="1d1e3-113">Default pricing</span></span>

<span data-ttu-id="1d1e3-114">Логика создания цен по умолчанию находится в строке журнала.</span><span class="sxs-lookup"><span data-stu-id="1d1e3-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="1d1e3-115">Значения полей из записи времени копируются в строку журнала.</span><span class="sxs-lookup"><span data-stu-id="1d1e3-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="1d1e3-116">Эти значения включают дату транзакции, строку контракта, с которой сопоставлен проект, и результат валюты в соответствующем прайс-листе.</span><span class="sxs-lookup"><span data-stu-id="1d1e3-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="1d1e3-117">Поля, которые влияют на цены по умолчанию, например **Роль** и **Единица распределения ресурсов** используются для определения соответствующей цены в строке журнала.</span><span class="sxs-lookup"><span data-stu-id="1d1e3-117">The fields that affect default pricing, such as **Role** and **Resourcing Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="1d1e3-118">Вы можете добавить настраиваемое поле к записи времени.</span><span class="sxs-lookup"><span data-stu-id="1d1e3-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="1d1e3-119">Если вы хотите, чтобы значение поля распространялось на фактические значения, создайте поле в таблицах **Фактические значения** и **Строка журнала**.</span><span class="sxs-lookup"><span data-stu-id="1d1e3-119">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="1d1e3-120">Используйте настраиваемый код для распространения значения выбранного поля из "Запись времени" в "Фактические значения" по строке журнала с помощью источников транзакции.</span><span class="sxs-lookup"><span data-stu-id="1d1e3-120">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="1d1e3-121">Для получения дополнительной информации об источниках транзакций и подключениях см. [Связь фактических данных с исходными записями](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="1d1e3-121">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="1d1e3-122">Строки журнала и базовая отправка расходов</span><span class="sxs-lookup"><span data-stu-id="1d1e3-122">Journal lines and basic expense submission</span></span>

<span data-ttu-id="1d1e3-123">Дополнительные сведения о записи расходов см. в теме [Обзор расходов](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1d1e3-123">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="1d1e3-124">Время и материалы</span><span class="sxs-lookup"><span data-stu-id="1d1e3-124">Time and materials</span></span>

<span data-ttu-id="1d1e3-125">Когда отправляемая базовая запись затрат связана с проектом, который сопоставлен со строкой контракта на время и материалы, система создает две строки журнала: одну для затрат и одну для продаж, за которые не выставлен счет.</span><span class="sxs-lookup"><span data-stu-id="1d1e3-125">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="1d1e3-126">Фиксированная цена</span><span class="sxs-lookup"><span data-stu-id="1d1e3-126">Fixed price</span></span>

<span data-ttu-id="1d1e3-127">Когда отправленная базовая запись расхода связана с проектом, который сопоставляется со строкой контракта с фиксированной ценой, система создает одну строку журнала для стоимости.</span><span class="sxs-lookup"><span data-stu-id="1d1e3-127">When a submitted basic expense entry is linked to a project that's mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="1d1e3-128">Цены по умолчанию</span><span class="sxs-lookup"><span data-stu-id="1d1e3-128">Default pricing</span></span>

<span data-ttu-id="1d1e3-129">Логика ввода цен по умолчанию для расходов основана на категории расходов.</span><span class="sxs-lookup"><span data-stu-id="1d1e3-129">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="1d1e3-130">Дата транзакции, строка контракта, с которой сопоставлен проект, и валюта все используются для определения соответствующего прайс-листа.</span><span class="sxs-lookup"><span data-stu-id="1d1e3-130">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="1d1e3-131">Поля, которые влияют на цены по умолчанию, например **Категория проводки** и **Единица распределения ресурсов** используются для определения соответствующей цены в строке журнала.</span><span class="sxs-lookup"><span data-stu-id="1d1e3-131">The fields that affect default pricing, such as **Transaction Category** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="1d1e3-132">Однако это работает только в том случае, если в прайс-листе указан метод ценообразования **Цена за единицу**.</span><span class="sxs-lookup"><span data-stu-id="1d1e3-132">However, this only works when the pricing method in the price list is **Price per unit**.</span></span> <span data-ttu-id="1d1e3-133">Если метод ценообразования — **По себестоимости** или **Наценка по стоимости**, цена, введенная при создании записи расхода, используется для стоимости, а цена в строке журнала продаж рассчитывается на основе метода ценообразования.</span><span class="sxs-lookup"><span data-stu-id="1d1e3-133">If pricing method is **At cost** or **Markup over cost**, the price entered when the expense entry is created is used for cost and the price on the sales journal line is calculated based on the pricing method.</span></span> 

<span data-ttu-id="1d1e3-134">Вы можете добавить настраиваемое поле в запись расхода.</span><span class="sxs-lookup"><span data-stu-id="1d1e3-134">You can add a custom field on the expense entry.</span></span> <span data-ttu-id="1d1e3-135">Если вы хотите, чтобы значение поля распространялось на фактические значения, создайте поле в таблицах **Фактические значения** и **Строка журнала**.</span><span class="sxs-lookup"><span data-stu-id="1d1e3-135">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="1d1e3-136">Используйте настраиваемый код для распространения значения выбранного поля из "Запись времени" в "Фактические значения" по строке журнала с помощью источников транзакции.</span><span class="sxs-lookup"><span data-stu-id="1d1e3-136">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="1d1e3-137">Для получения дополнительной информации об источниках транзакций и подключениях см. [Связь фактических данных с исходными записями](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="1d1e3-137">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-material-usage-log-submission"></a><span data-ttu-id="1d1e3-138">Отправка строк журнала и журнала использования материалов</span><span class="sxs-lookup"><span data-stu-id="1d1e3-138">Journal lines and material usage log submission</span></span>

<span data-ttu-id="1d1e3-139">Для получения дополнительной информации о записи расходов см. [Журнал использования материалов](../material/material-usage-log.md).</span><span class="sxs-lookup"><span data-stu-id="1d1e3-139">For more information about expense entry, see [Material Usage Log](../material/material-usage-log.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="1d1e3-140">Время и материалы</span><span class="sxs-lookup"><span data-stu-id="1d1e3-140">Time and materials</span></span>

<span data-ttu-id="1d1e3-141">Когда отправленная запись журнала использования материалов связана с проектом, который сопоставлен со строкой контракта на время и материалы, система создает две строки журнала: одну для стоимости и одну для продаж без выставления счета.</span><span class="sxs-lookup"><span data-stu-id="1d1e3-141">When a submitted material usage log entry is linked to a project that is mapped to a time and materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="1d1e3-142">Фиксированная цена</span><span class="sxs-lookup"><span data-stu-id="1d1e3-142">Fixed price</span></span>

<span data-ttu-id="1d1e3-143">Когда отправленная запись журнала использования материала связана с проектом, который сопоставляется со строкой контракта с фиксированной ценой, система создает одну строку журнала для стоимости.</span><span class="sxs-lookup"><span data-stu-id="1d1e3-143">When a submitted material usage log entry is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="1d1e3-144">Цены по умолчанию</span><span class="sxs-lookup"><span data-stu-id="1d1e3-144">Default pricing</span></span>

<span data-ttu-id="1d1e3-145">Логика ввода цен по умолчанию для материала основана на комбинации продукта и единицы.</span><span class="sxs-lookup"><span data-stu-id="1d1e3-145">The logic for entering default prices for material is based on the product and unit combination.</span></span> <span data-ttu-id="1d1e3-146">Дата транзакции, строка контракта, с которой сопоставлен проект, и валюта все используются для определения соответствующего прайс-листа.</span><span class="sxs-lookup"><span data-stu-id="1d1e3-146">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="1d1e3-147">Поля, которые влияют на цены по умолчанию, например **Артикул** и **Единица** используются для определения соответствующей цены в строке журнала.</span><span class="sxs-lookup"><span data-stu-id="1d1e3-147">The fields that affect default pricing, such as **Product ID** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="1d1e3-148">Однако это работает только для продуктов из каталога.</span><span class="sxs-lookup"><span data-stu-id="1d1e3-148">However, this only works for catalog products.</span></span> <span data-ttu-id="1d1e3-149">Для вписанных продуктов цена, введенная при создании записи в журнале использования материала, используется для стоимости и цены продажи в строках журнала.</span><span class="sxs-lookup"><span data-stu-id="1d1e3-149">For write-in products, the price entered when the material usage log entry is created is used for cost and sales price on the journal lines.</span></span> 

<span data-ttu-id="1d1e3-150">Вы можете добавить настраиваемое поле в запись **Журнал использования материалов**.</span><span class="sxs-lookup"><span data-stu-id="1d1e3-150">You can add a custom field on the **Material Usage Log** entry.</span></span> <span data-ttu-id="1d1e3-151">Если вы хотите, чтобы значение поля распространялось на фактические значения, создайте поле в таблицах **Фактические значения** и **Строка журнала**.</span><span class="sxs-lookup"><span data-stu-id="1d1e3-151">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="1d1e3-152">Используйте настраиваемый код для распространения значения выбранного поля из "Запись времени" в "Фактические значения" по строке журнала с помощью источников транзакции.</span><span class="sxs-lookup"><span data-stu-id="1d1e3-152">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="1d1e3-153">Для получения дополнительной информации об источниках транзакций и подключениях см. [Связь фактических данных с исходными записями](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="1d1e3-153">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="1d1e3-154">Использование журналов записей для записи стоимости</span><span class="sxs-lookup"><span data-stu-id="1d1e3-154">Use entry journals to record costs</span></span>

<span data-ttu-id="1d1e3-155">Журналы можно использовать для записи стоимости или дохода в классах проводок по материалам, сборам, времени, расходам и налогам.</span><span class="sxs-lookup"><span data-stu-id="1d1e3-155">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="1d1e3-156">Журналы могут использоваться для следующих целей:</span><span class="sxs-lookup"><span data-stu-id="1d1e3-156">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="1d1e3-157">Перемещение фактических данных транзакций из другой системы в Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="1d1e3-157">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="1d1e3-158">Запись затрат, которые произошли в другой системе.</span><span class="sxs-lookup"><span data-stu-id="1d1e3-158">Record costs that occurred in another system.</span></span> <span data-ttu-id="1d1e3-159">Эти затраты могут включать затраты на закупку или субподряд.</span><span class="sxs-lookup"><span data-stu-id="1d1e3-159">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1d1e3-160">Приложение не проверяет тип строки журнала или соответствующие цены, введенные в строке журнала.</span><span class="sxs-lookup"><span data-stu-id="1d1e3-160">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="1d1e3-161">Следовательно, только пользователь, который полностью осознает влияние на учет от фактических данных по проекту должен использовать журналы записей для создания фактических данных.</span><span class="sxs-lookup"><span data-stu-id="1d1e3-161">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="1d1e3-162">Из-за влияния этого типа журнала вам следует тщательно выбирать, у кого есть доступ для создания журналов входа.</span><span class="sxs-lookup"><span data-stu-id="1d1e3-162">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>

## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="1d1e3-163">Запись фактических данных по событиям проекта</span><span class="sxs-lookup"><span data-stu-id="1d1e3-163">Record actuals based on project events</span></span>

<span data-ttu-id="1d1e3-164">Project Operations записывает финансовые транзакции, которые происходят в ходе проекта.</span><span class="sxs-lookup"><span data-stu-id="1d1e3-164">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="1d1e3-165">Эти транзакции записываются как фактические значения.</span><span class="sxs-lookup"><span data-stu-id="1d1e3-165">These transactions are recorded as actuals.</span></span> <span data-ttu-id="1d1e3-166">В следующих таблицах отображаются различные типы созданных фактических данных, в зависимости от того, является ли проект проектом "время и материалы" или проектом с фиксированной ценой.</span><span class="sxs-lookup"><span data-stu-id="1d1e3-166">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="1d1e3-167">Ресурс принадлежит к тому же подразделению, что и контрактная единица по проекту</span><span class="sxs-lookup"><span data-stu-id="1d1e3-167">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="1d1e3-168">Событие</span><span class="sxs-lookup"><span data-stu-id="1d1e3-168">Event</span></span></th>
<th colspan="4"><span data-ttu-id="1d1e3-169">Оплачиваемый или проданный проект</span><span class="sxs-lookup"><span data-stu-id="1d1e3-169">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="1d1e3-170">Проект на стадии предварительных продаж</span><span class="sxs-lookup"><span data-stu-id="1d1e3-170">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="1d1e3-171">Внутренний проект</span><span class="sxs-lookup"><span data-stu-id="1d1e3-171">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="1d1e3-172">Время и материалы</span><span class="sxs-lookup"><span data-stu-id="1d1e3-172">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="1d1e3-173">Фиксированная цена</span><span class="sxs-lookup"><span data-stu-id="1d1e3-173">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="1d1e3-174">Фактические</span><span class="sxs-lookup"><span data-stu-id="1d1e3-174">Actuals</span></span></th>
<th><span data-ttu-id="1d1e3-175">Валюта транзакции</span><span class="sxs-lookup"><span data-stu-id="1d1e3-175">Transaction currency</span></span></th>
<th><span data-ttu-id="1d1e3-176">Фиксированная цена</span><span class="sxs-lookup"><span data-stu-id="1d1e3-176">Fixed price</span></span></th>
<th><span data-ttu-id="1d1e3-177">Валюта транзакции</span><span class="sxs-lookup"><span data-stu-id="1d1e3-177">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1d1e3-178">Создана запись времени.</span><span class="sxs-lookup"><span data-stu-id="1d1e3-178">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="1d1e3-179">Нет действий в сущности фактических данных</span><span class="sxs-lookup"><span data-stu-id="1d1e3-179">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d1e3-180">Запись времени отправлена.</span><span class="sxs-lookup"><span data-stu-id="1d1e3-180">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="1d1e3-181">Нет действий в сущности фактических данных</span><span class="sxs-lookup"><span data-stu-id="1d1e3-181">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="1d1e3-182">Время одобрено, и нет изменений или увеличения оплачиваемых часов в процессе утверждения.</span><span class="sxs-lookup"><span data-stu-id="1d1e3-182">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="1d1e3-183">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="1d1e3-183">Cost actual</span></span></td>
<td><span data-ttu-id="1d1e3-184">Валюта единицы по контракту</span><span class="sxs-lookup"><span data-stu-id="1d1e3-184">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="1d1e3-185">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="1d1e3-185">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="1d1e3-186">Валюта единицы по контракту</span><span class="sxs-lookup"><span data-stu-id="1d1e3-186">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="1d1e3-187">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="1d1e3-187">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="1d1e3-188">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="1d1e3-188">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d1e3-189">Фактическая сумма продаж с невыставленными счетами — оплачиваемые</span><span class="sxs-lookup"><span data-stu-id="1d1e3-189">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="1d1e3-190">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="1d1e3-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="1d1e3-191">Время одобрено, и имеется уменьшение оплачиваемых часов в процессе утверждения.</span><span class="sxs-lookup"><span data-stu-id="1d1e3-191">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="1d1e3-192">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="1d1e3-192">Cost actual</span></span></td>
<td><span data-ttu-id="1d1e3-193">Валюта единицы по контракту</span><span class="sxs-lookup"><span data-stu-id="1d1e3-193">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="1d1e3-194">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="1d1e3-194">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="1d1e3-195">Валюта единицы по контракту</span><span class="sxs-lookup"><span data-stu-id="1d1e3-195">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="1d1e3-196">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="1d1e3-196">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="1d1e3-197">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="1d1e3-197">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d1e3-198">Фактическое количество продаж без выставления счета — оплачивается для нового количества</span><span class="sxs-lookup"><span data-stu-id="1d1e3-198">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="1d1e3-199">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="1d1e3-199">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d1e3-200">Фактическое количество продаж без выставления счета — не оплачивается для разницы</span><span class="sxs-lookup"><span data-stu-id="1d1e3-200">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="1d1e3-201">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="1d1e3-201">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="1d1e3-202">Счет одобрен, и нет изменения или происходит увеличение оплачиваемых часов в процессе утверждения.</span><span class="sxs-lookup"><span data-stu-id="1d1e3-202">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="1d1e3-203">Обращение продаж без выставления счета</span><span class="sxs-lookup"><span data-stu-id="1d1e3-203">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="1d1e3-204">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="1d1e3-204">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="1d1e3-205">Продажи с выставленными счетами для вехи</span><span class="sxs-lookup"><span data-stu-id="1d1e3-205">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="1d1e3-206">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="1d1e3-206">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="1d1e3-207">Нет данных</span><span class="sxs-lookup"><span data-stu-id="1d1e3-207">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="1d1e3-208">Нет данных</span><span class="sxs-lookup"><span data-stu-id="1d1e3-208">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d1e3-209">Продажи с выставлением счета</span><span class="sxs-lookup"><span data-stu-id="1d1e3-209">Billed sales</span></span></td>
<td><span data-ttu-id="1d1e3-210">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="1d1e3-210">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="1d1e3-211">Счет одобрен, и имеется уменьшение оплачиваемых часов в процессе утверждения.</span><span class="sxs-lookup"><span data-stu-id="1d1e3-211">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="1d1e3-212">Обращение продаж без выставления счета</span><span class="sxs-lookup"><span data-stu-id="1d1e3-212">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="1d1e3-213">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="1d1e3-213">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="1d1e3-214">Нет данных</span><span class="sxs-lookup"><span data-stu-id="1d1e3-214">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="1d1e3-215">Нет данных</span><span class="sxs-lookup"><span data-stu-id="1d1e3-215">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="1d1e3-216">Нет данных</span><span class="sxs-lookup"><span data-stu-id="1d1e3-216">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="1d1e3-217">Нет данных</span><span class="sxs-lookup"><span data-stu-id="1d1e3-217">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d1e3-218">Продажи с выставленными счетами — оплачивается для нового количества</span><span class="sxs-lookup"><span data-stu-id="1d1e3-218">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="1d1e3-219">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="1d1e3-219">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d1e3-220">Продажи с выставленным счетом — не оплачивается для разницы</span><span class="sxs-lookup"><span data-stu-id="1d1e3-220">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="1d1e3-221">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="1d1e3-221">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="1d1e3-222">Счет исправлен для увеличения оплачиваемого количества.</span><span class="sxs-lookup"><span data-stu-id="1d1e3-222">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="1d1e3-223">Продаж с выставленным счетом — обращение</span><span class="sxs-lookup"><span data-stu-id="1d1e3-223">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="1d1e3-224">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="1d1e3-224">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="1d1e3-225">Обращение продаж с выставленными счетами для вехи</span><span class="sxs-lookup"><span data-stu-id="1d1e3-225">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="1d1e3-226">Изменение в состоянии вехи с <strong>Выставлен счет</strong> на <strong>Готов к выставлению счета</strong></span><span class="sxs-lookup"><span data-stu-id="1d1e3-226">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="1d1e3-227">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="1d1e3-227">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="1d1e3-228">Нет данных</span><span class="sxs-lookup"><span data-stu-id="1d1e3-228">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="1d1e3-229">Нет данных</span><span class="sxs-lookup"><span data-stu-id="1d1e3-229">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d1e3-230">Продажи с выставлением счета</span><span class="sxs-lookup"><span data-stu-id="1d1e3-230">Billed sales</span></span></td>
<td><span data-ttu-id="1d1e3-231">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="1d1e3-231">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="1d1e3-232">Счет исправлен для уменьшения оплачиваемого количества.</span><span class="sxs-lookup"><span data-stu-id="1d1e3-232">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="1d1e3-233">Продаж с выставленным счетом — обращение</span><span class="sxs-lookup"><span data-stu-id="1d1e3-233">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="1d1e3-234">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="1d1e3-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d1e3-235">Продажи с выставленными счетами для нового количества</span><span class="sxs-lookup"><span data-stu-id="1d1e3-235">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="1d1e3-236">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="1d1e3-236">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d1e3-237">Продажи без выставленного счета — оплачивается для разницы</span><span class="sxs-lookup"><span data-stu-id="1d1e3-237">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="1d1e3-238">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="1d1e3-238">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="1d1e3-239">Ресурс принадлежит к подразделению, который отличается от контрактной единицы по проекту</span><span class="sxs-lookup"><span data-stu-id="1d1e3-239">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="1d1e3-240">Событие</span><span class="sxs-lookup"><span data-stu-id="1d1e3-240">Event</span></span></th>
<th colspan="4"><span data-ttu-id="1d1e3-241">Оплачиваемый или проданный проект</span><span class="sxs-lookup"><span data-stu-id="1d1e3-241">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="1d1e3-242">Проект на стадии предварительных продаж</span><span class="sxs-lookup"><span data-stu-id="1d1e3-242">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="1d1e3-243">Внутренний проект</span><span class="sxs-lookup"><span data-stu-id="1d1e3-243">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="1d1e3-244">Время и материалы</span><span class="sxs-lookup"><span data-stu-id="1d1e3-244">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="1d1e3-245">Фиксированная цена</span><span class="sxs-lookup"><span data-stu-id="1d1e3-245">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="1d1e3-246">Фактические</span><span class="sxs-lookup"><span data-stu-id="1d1e3-246">Actuals</span></span></th>
<th><span data-ttu-id="1d1e3-247">Валюта транзакции</span><span class="sxs-lookup"><span data-stu-id="1d1e3-247">Transaction currency</span></span></th>
<th><span data-ttu-id="1d1e3-248">Фиксированная цена</span><span class="sxs-lookup"><span data-stu-id="1d1e3-248">Fixed price</span></span></th>
<th><span data-ttu-id="1d1e3-249">Валюта транзакции</span><span class="sxs-lookup"><span data-stu-id="1d1e3-249">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1d1e3-250">Создана запись времени.</span><span class="sxs-lookup"><span data-stu-id="1d1e3-250">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="1d1e3-251">Нет действий в сущности фактических данных</span><span class="sxs-lookup"><span data-stu-id="1d1e3-251">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d1e3-252">Запись времени отправлена.</span><span class="sxs-lookup"><span data-stu-id="1d1e3-252">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="1d1e3-253">Нет действий в сущности фактических данных</span><span class="sxs-lookup"><span data-stu-id="1d1e3-253">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="1d1e3-254">Время одобрено, и нет изменений или увеличения оплачиваемых часов в процессе утверждения.</span><span class="sxs-lookup"><span data-stu-id="1d1e3-254">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="1d1e3-255">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="1d1e3-255">Cost actual</span></span></td>
<td><span data-ttu-id="1d1e3-256">Валюта единицы по контракту</span><span class="sxs-lookup"><span data-stu-id="1d1e3-256">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="1d1e3-257">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="1d1e3-257">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="1d1e3-258">Валюта единицы по контракту</span><span class="sxs-lookup"><span data-stu-id="1d1e3-258">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="1d1e3-259">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="1d1e3-259">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="1d1e3-260">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="1d1e3-260">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d1e3-261">Фактическая сумма продаж с невыставленными счетами — оплачиваемые</span><span class="sxs-lookup"><span data-stu-id="1d1e3-261">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="1d1e3-262">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="1d1e3-262">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d1e3-263">Стоимость единицы распределения ресурсов</span><span class="sxs-lookup"><span data-stu-id="1d1e3-263">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="1d1e3-264">Валюта единицы распределения ресурсов</span><span class="sxs-lookup"><span data-stu-id="1d1e3-264">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d1e3-265">Внутрихолдинговые продажи</span><span class="sxs-lookup"><span data-stu-id="1d1e3-265">Interorganizational sales</span></span></td>
<td><span data-ttu-id="1d1e3-266">Валюта единицы по контракту</span><span class="sxs-lookup"><span data-stu-id="1d1e3-266">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="1d1e3-267">Время одобрено, и имеется уменьшение оплачиваемых часов в процессе утверждения.</span><span class="sxs-lookup"><span data-stu-id="1d1e3-267">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="1d1e3-268">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="1d1e3-268">Cost actual</span></span></td>
<td><span data-ttu-id="1d1e3-269">Валюта единицы по контракту</span><span class="sxs-lookup"><span data-stu-id="1d1e3-269">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="1d1e3-270">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="1d1e3-270">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="1d1e3-271">Валюта единицы по контракту</span><span class="sxs-lookup"><span data-stu-id="1d1e3-271">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="1d1e3-272">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="1d1e3-272">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="1d1e3-273">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="1d1e3-273">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d1e3-274">Стоимость единицы распределения ресурсов</span><span class="sxs-lookup"><span data-stu-id="1d1e3-274">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="1d1e3-275">Валюта единицы распределения ресурсов</span><span class="sxs-lookup"><span data-stu-id="1d1e3-275">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d1e3-276">Внутрихолдинговые продажи</span><span class="sxs-lookup"><span data-stu-id="1d1e3-276">Interorganizational sales</span></span></td>
<td><span data-ttu-id="1d1e3-277">Валюта единицы по контракту</span><span class="sxs-lookup"><span data-stu-id="1d1e3-277">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d1e3-278">Фактическое количество продаж без выставления счета — оплачивается для нового количества</span><span class="sxs-lookup"><span data-stu-id="1d1e3-278">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="1d1e3-279">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="1d1e3-279">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d1e3-280">Фактическое количество продаж без выставления счета — не оплачивается для разницы</span><span class="sxs-lookup"><span data-stu-id="1d1e3-280">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="1d1e3-281">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="1d1e3-281">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="1d1e3-282">Счет одобрен, и нет изменения или происходит увеличение оплачиваемых часов в процессе утверждения.</span><span class="sxs-lookup"><span data-stu-id="1d1e3-282">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="1d1e3-283">Обращение продаж без выставления счета</span><span class="sxs-lookup"><span data-stu-id="1d1e3-283">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="1d1e3-284">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="1d1e3-284">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="1d1e3-285">Продажи с выставленными счетами для вехи</span><span class="sxs-lookup"><span data-stu-id="1d1e3-285">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="1d1e3-286">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="1d1e3-286">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="1d1e3-287">Нет данных</span><span class="sxs-lookup"><span data-stu-id="1d1e3-287">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="1d1e3-288">Нет данных</span><span class="sxs-lookup"><span data-stu-id="1d1e3-288">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d1e3-289">Продажи с выставлением счета</span><span class="sxs-lookup"><span data-stu-id="1d1e3-289">Billed sales</span></span></td>
<td><span data-ttu-id="1d1e3-290">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="1d1e3-290">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="1d1e3-291">Счет одобрен, и имеется уменьшение оплачиваемых часов в процессе утверждения.</span><span class="sxs-lookup"><span data-stu-id="1d1e3-291">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="1d1e3-292">Обращение продаж без выставления счета</span><span class="sxs-lookup"><span data-stu-id="1d1e3-292">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="1d1e3-293">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="1d1e3-293">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="1d1e3-294">Нет данных</span><span class="sxs-lookup"><span data-stu-id="1d1e3-294">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="1d1e3-295">Нет данных</span><span class="sxs-lookup"><span data-stu-id="1d1e3-295">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="1d1e3-296">Нет данных</span><span class="sxs-lookup"><span data-stu-id="1d1e3-296">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="1d1e3-297">Нет данных</span><span class="sxs-lookup"><span data-stu-id="1d1e3-297">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d1e3-298">Продажи с выставленными счетами — оплачивается для нового количества</span><span class="sxs-lookup"><span data-stu-id="1d1e3-298">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="1d1e3-299">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="1d1e3-299">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d1e3-300">Продажи с выставленным счетом — не оплачивается для разницы</span><span class="sxs-lookup"><span data-stu-id="1d1e3-300">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="1d1e3-301">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="1d1e3-301">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="1d1e3-302">Счет исправлен для увеличения оплачиваемого количества.</span><span class="sxs-lookup"><span data-stu-id="1d1e3-302">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="1d1e3-303">Продаж с выставленным счетом — обращение</span><span class="sxs-lookup"><span data-stu-id="1d1e3-303">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="1d1e3-304">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="1d1e3-304">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="1d1e3-305">Обращение продаж с выставленными счетами для вехи</span><span class="sxs-lookup"><span data-stu-id="1d1e3-305">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="1d1e3-306">Изменение в состоянии вехи с <strong>Выставлен счет</strong> на <strong>Готов к выставлению счета</strong></span><span class="sxs-lookup"><span data-stu-id="1d1e3-306">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="1d1e3-307">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="1d1e3-307">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="1d1e3-308">Нет данных</span><span class="sxs-lookup"><span data-stu-id="1d1e3-308">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="1d1e3-309">Нет данных</span><span class="sxs-lookup"><span data-stu-id="1d1e3-309">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d1e3-310">Продажи с выставлением счета</span><span class="sxs-lookup"><span data-stu-id="1d1e3-310">Billed sales</span></span></td>
<td><span data-ttu-id="1d1e3-311">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="1d1e3-311">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="1d1e3-312">Счет исправлен для уменьшения оплачиваемого количества.</span><span class="sxs-lookup"><span data-stu-id="1d1e3-312">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="1d1e3-313">Продаж с выставленным счетом — обращение</span><span class="sxs-lookup"><span data-stu-id="1d1e3-313">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="1d1e3-314">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="1d1e3-314">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d1e3-315">Продажи с выставленными счетами для нового количества</span><span class="sxs-lookup"><span data-stu-id="1d1e3-315">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="1d1e3-316">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="1d1e3-316">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d1e3-317">Продажи без выставленного счета — оплачивается для разницы</span><span class="sxs-lookup"><span data-stu-id="1d1e3-317">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="1d1e3-318">Валюта контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="1d1e3-318">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
