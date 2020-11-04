---
title: Подтверждение счета-проформы
description: В этой теме предоставлена информация о подтверждении счетов-проформ в Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4b67ee6848efdcb85cf732c1eaa3e40cdc51a2e2
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083096"
---
# <a name="confirming-a-proforma-invoice"></a><span data-ttu-id="9b8c2-103">Подтверждение счета-проформы</span><span class="sxs-lookup"><span data-stu-id="9b8c2-103">Confirming a proforma invoice</span></span>

<span data-ttu-id="9b8c2-104">_**Относится к:** развертывание Lite — от сделки до счетов-проформ_</span><span class="sxs-lookup"><span data-stu-id="9b8c2-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="9b8c2-105">После подтверждения счета-проформы статус счета по проекту изменяется на **Подтверждено**.</span><span class="sxs-lookup"><span data-stu-id="9b8c2-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="9b8c2-106">Когда счет подтвержден, он становится доступным только для чтения.</span><span class="sxs-lookup"><span data-stu-id="9b8c2-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="9b8c2-107">В дальнейшем счет можно будет исправить только в том случае, если есть какие-либо исправления или кредиты, инициированные клиентом, или если счет отмечен как оплаченный.</span><span class="sxs-lookup"><span data-stu-id="9b8c2-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, of if the invoice is marked as paid.</span></span>

<span data-ttu-id="9b8c2-108">В следующей таблице перечислены фактические данные, созданные системой.</span><span class="sxs-lookup"><span data-stu-id="9b8c2-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="9b8c2-109">Эти фактические данные создаются при выполнении определенных операций с черновиком счета по проекту до его подтверждения.</span><span class="sxs-lookup"><span data-stu-id="9b8c2-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="9b8c2-110">
                    <strong>Сценарий</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9b8c2-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="9b8c2-111">
                    <strong>Фактические данные, созданные при подтверждении</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9b8c2-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9b8c2-112">Выставление счета на аванс или предоплату</span><span class="sxs-lookup"><span data-stu-id="9b8c2-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9b8c2-113">Фактические продажи типа <strong>Предоплата</strong>, за которые не выставлен счет, создаются на сумму аванса или предоплаты.</span><span class="sxs-lookup"><span data-stu-id="9b8c2-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9b8c2-114">Фактическая сумма продаж с невыставленными счетами с отрицательной суммой предоплаты или аванса для использования для сверки.</span><span class="sxs-lookup"><span data-stu-id="9b8c2-114">An unbilled sales actual of a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9b8c2-115">После полной выверки предоплаты или аванса по счету.</span><span class="sxs-lookup"><span data-stu-id="9b8c2-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9b8c2-116">Сторнирование продажи с невыставленным счетом для предоплаты или аванса, созданного для выверки.</span><span class="sxs-lookup"><span data-stu-id="9b8c2-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="9b8c2-117">Эта сумма является положительной, так как она предназначена для компенсации отрицательного результата, который был создан при выставлении предоплаты или аванса.</span><span class="sxs-lookup"><span data-stu-id="9b8c2-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9b8c2-118">Фактические данные продажи с выставленными счетами на сумму в этом счете.</span><span class="sxs-lookup"><span data-stu-id="9b8c2-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="9b8c2-119">После частичной выверки предоплаты или аванса по счету.</span><span class="sxs-lookup"><span data-stu-id="9b8c2-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9b8c2-120">Сторнирование продажи с невыставленным счетом для предоплаты или аванса, созданного для выверки.</span><span class="sxs-lookup"><span data-stu-id="9b8c2-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="9b8c2-121">Эта сумма является положительной, так как она предназначена для компенсации отрицательного результата, который был создан при выставлении предоплаты или аванса.</span><span class="sxs-lookup"><span data-stu-id="9b8c2-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9b8c2-122">Фактические данные продажи с выставленными счетами на сумму в этом счете.</span><span class="sxs-lookup"><span data-stu-id="9b8c2-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9b8c2-123">Отрицательная фактическая сумма продаж с невыставленными счетами, равная оставшейся сумме предоплаты или аванса для использования для выверки в будущих счетах.</span><span class="sxs-lookup"><span data-stu-id="9b8c2-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9b8c2-124">Выставление счета по транзакции за время без каких-либо изменений в черновике счета.</span><span class="sxs-lookup"><span data-stu-id="9b8c2-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9b8c2-125">Сторнирование продаж с невыставленным счетом по часам и сумме в исходном утвержденном времени.</span><span class="sxs-lookup"><span data-stu-id="9b8c2-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9b8c2-126">Фактические данные продаж с выставленным счетом по часам и сумме в исходном утвержденном времени.</span><span class="sxs-lookup"><span data-stu-id="9b8c2-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="9b8c2-127">Выставление счета по транзакции по времени, которая была отредактирована для уменьшения количества.</span><span class="sxs-lookup"><span data-stu-id="9b8c2-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9b8c2-128">Сторнирование продаж с невыставленным счетом по часам и сумме в исходном утвержденном времени.</span><span class="sxs-lookup"><span data-stu-id="9b8c2-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9b8c2-129">Новая фактическая сумма продаж, по которой не выставлен счет, которая оплачивается по часам и сумме в отредактированных сведениях строки счета, сторнирование фактических данных продаж и эквивалентная фактическая сумма продаж, по которым выставлен счет.</span><span class="sxs-lookup"><span data-stu-id="9b8c2-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9b8c2-130">Новая фактическая сумма продаж, по которой не выставлен счет, которая не оплачивается по оставшимся часам и сумме после вычитания исправленных цифр в отредактированных сведениях строки счета, сторнирование фактических данных продаж и эквивалентная фактическая сумма продаж, по которым выставлен счет.</span><span class="sxs-lookup"><span data-stu-id="9b8c2-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9b8c2-131">Выставление счета по транзакции по времени, которая была отредактирована для увеличения количества.</span><span class="sxs-lookup"><span data-stu-id="9b8c2-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9b8c2-132">Сторнирование продаж с невыставленным счетом по часам и сумме в исходном утвержденном времени.</span><span class="sxs-lookup"><span data-stu-id="9b8c2-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9b8c2-133">Новая фактическая сумма продаж, по которой не выставлен счет, которая оплачивается по часам и сумме в отредактированных сведениях строки счета, сторнирование фактических данных продаж, по которым не выставлены счета, и эквивалентная фактическая сумма продаж, по которым выставлен счет.</span><span class="sxs-lookup"><span data-stu-id="9b8c2-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9b8c2-134">Выставление счета по транзакции за расходы без каких-либо изменений в черновике счета.</span><span class="sxs-lookup"><span data-stu-id="9b8c2-134">Invoicing an expense transaction without any edits on draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9b8c2-135">Сторнирование продаж с невыставленным счетом по количеству и сумме в исходных утвержденных расходах.</span><span class="sxs-lookup"><span data-stu-id="9b8c2-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9b8c2-136">Фактические данные продаж с выставленным счетом по количеству и сумме в исходных утвержденных расходах</span><span class="sxs-lookup"><span data-stu-id="9b8c2-136">A billed sales actual for the quantity and amount on the original expense approval</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="9b8c2-137">Выставление счета по транзакции по расходам, которая была отредактирована для уменьшения количества.</span><span class="sxs-lookup"><span data-stu-id="9b8c2-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9b8c2-138">Сторнирование продаж с невыставленным счетом по количеству и сумме в исходных утвержденных расходах.</span><span class="sxs-lookup"><span data-stu-id="9b8c2-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9b8c2-139">Новая фактическая сумма продаж, по которой не выставлен счет, которая оплачивается по количеству и сумме в отредактированных сведениях строки счета, сторнирование фактических данных продаж, по которым не выставлены счета, и эквивалентная фактическая сумма продаж, по которым выставлен счет.</span><span class="sxs-lookup"><span data-stu-id="9b8c2-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9b8c2-140">Новая фактическая сумма продаж, по которой не выставлен счет, которая не оплачивается по оставшемуся количеству и сумме после вычитания исправленных цифр в отредактированных сведениях строки счета, сторнирование фактических данных продаж, по которым не выставлены счета, и эквивалент фактической суммы продаж, по которым выставлен счет.</span><span class="sxs-lookup"><span data-stu-id="9b8c2-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9b8c2-141">Выставление счета по транзакции по расходам, которая была отредактирована для увеличения количества.</span><span class="sxs-lookup"><span data-stu-id="9b8c2-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9b8c2-142">Сторнирование продаж с невыставленным счетом по количеству и сумме в исходных утвержденных расходах.</span><span class="sxs-lookup"><span data-stu-id="9b8c2-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9b8c2-143">Новая фактическая сумма продаж, по которой не выставлен счет, которая оплачивается по количеству и сумме в отредактированных сведениях строки счета, сторнирование фактических данных продаж, по которым не выставлены счета, и эквивалентная фактическая сумма продаж, по которым выставлен счет.</span><span class="sxs-lookup"><span data-stu-id="9b8c2-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9b8c2-144">Выставление вознаграждения.</span><span class="sxs-lookup"><span data-stu-id="9b8c2-144">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9b8c2-145">Сторнирование продаж с невыставленным счетом по сумме вознаграждения в исходной строке журнала.</span><span class="sxs-lookup"><span data-stu-id="9b8c2-145">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9b8c2-146">Фактические данные продаж с выставленным счетом по количеству и сумме в исходной строке журнала вознаграждения.</span><span class="sxs-lookup"><span data-stu-id="9b8c2-146">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="9b8c2-147">Выставление счета за веху.</span><span class="sxs-lookup"><span data-stu-id="9b8c2-147">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9b8c2-148">Фактические данные продаж с выставленным счетом по сумме вехи в исходной вехе в строке контракта по проекту.</span><span class="sxs-lookup"><span data-stu-id="9b8c2-148">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="9b8c2-149">Выставление счета по строке контракта на основе продуктов.</span><span class="sxs-lookup"><span data-stu-id="9b8c2-149">Invoicing a product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9b8c2-150">Фактические данные продаж с выставленным счетом для строки продуктов с количеством и суммой, полученными из строки контракта на основе продукта.</span><span class="sxs-lookup"><span data-stu-id="9b8c2-150">A billed sales actual for the product line with the quantity and amount coming from the product-based contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>
