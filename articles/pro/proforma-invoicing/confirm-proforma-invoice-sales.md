---
title: Подтверждение счета-проформы — облегченное развертывание
description: В этой теме предоставлена информация о подтверждении счетов-проформ в Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 02b671e4ad327b2448529d7119211613f3a9cb27
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176537"
---
# <a name="confirm-a-proforma-invoice---lite"></a><span data-ttu-id="0a982-103">Подтверждение счета-проформы — облегченное развертывание</span><span class="sxs-lookup"><span data-stu-id="0a982-103">Confirm a proforma invoice - lite</span></span>

<span data-ttu-id="0a982-104">_**Относится к:** развертывание Lite — от сделки до счетов-проформ_</span><span class="sxs-lookup"><span data-stu-id="0a982-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="0a982-105">После подтверждения счета-проформы статус счета по проекту изменяется на **Подтверждено**.</span><span class="sxs-lookup"><span data-stu-id="0a982-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="0a982-106">Когда счет подтвержден, он становится доступным только для чтения.</span><span class="sxs-lookup"><span data-stu-id="0a982-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="0a982-107">В дальнейшем счет можно будет исправить только в том случае, если есть какие-либо исправления или кредиты, инициированные клиентом, или если счет отмечен как оплаченный.</span><span class="sxs-lookup"><span data-stu-id="0a982-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, of if the invoice is marked as paid.</span></span>

<span data-ttu-id="0a982-108">В следующей таблице перечислены фактические данные, созданные системой.</span><span class="sxs-lookup"><span data-stu-id="0a982-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="0a982-109">Эти фактические данные создаются при выполнении определенных операций с черновиком счета по проекту до его подтверждения.</span><span class="sxs-lookup"><span data-stu-id="0a982-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="0a982-110">
                    <strong>Сценарий</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0a982-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="0a982-111">
                    <strong>Фактические данные, созданные при подтверждении</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0a982-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0a982-112">Выставление счета на аванс или предоплату</span><span class="sxs-lookup"><span data-stu-id="0a982-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0a982-113">Фактические продажи типа <strong>Предоплата</strong>, за которые не выставлен счет, создаются на сумму аванса или предоплаты.</span><span class="sxs-lookup"><span data-stu-id="0a982-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0a982-114">Фактическая сумма продаж с невыставленными счетами с отрицательной суммой предоплаты или аванса для использования для сверки.</span><span class="sxs-lookup"><span data-stu-id="0a982-114">An unbilled sales actual of a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0a982-115">После полной выверки предоплаты или аванса по счету.</span><span class="sxs-lookup"><span data-stu-id="0a982-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0a982-116">Сторнирование продажи с невыставленным счетом для предоплаты или аванса, созданного для выверки.</span><span class="sxs-lookup"><span data-stu-id="0a982-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="0a982-117">Эта сумма является положительной, так как она предназначена для компенсации отрицательного результата, который был создан при выставлении предоплаты или аванса.</span><span class="sxs-lookup"><span data-stu-id="0a982-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0a982-118">Фактические данные продажи с выставленными счетами на сумму в этом счете.</span><span class="sxs-lookup"><span data-stu-id="0a982-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="0a982-119">После частичной выверки предоплаты или аванса по счету.</span><span class="sxs-lookup"><span data-stu-id="0a982-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0a982-120">Сторнирование продажи с невыставленным счетом для предоплаты или аванса, созданного для выверки.</span><span class="sxs-lookup"><span data-stu-id="0a982-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="0a982-121">Эта сумма является положительной, так как она предназначена для компенсации отрицательного результата, который был создан при выставлении предоплаты или аванса.</span><span class="sxs-lookup"><span data-stu-id="0a982-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0a982-122">Фактические данные продажи с выставленными счетами на сумму в этом счете.</span><span class="sxs-lookup"><span data-stu-id="0a982-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0a982-123">Отрицательная фактическая сумма продаж с невыставленными счетами, равная оставшейся сумме предоплаты или аванса для использования для выверки в будущих счетах.</span><span class="sxs-lookup"><span data-stu-id="0a982-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0a982-124">Выставление счета по транзакции за время без каких-либо изменений в черновике счета.</span><span class="sxs-lookup"><span data-stu-id="0a982-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0a982-125">Сторнирование продаж с невыставленным счетом по часам и сумме в исходном утвержденном времени.</span><span class="sxs-lookup"><span data-stu-id="0a982-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0a982-126">Фактические данные продаж с выставленным счетом по часам и сумме в исходном утвержденном времени.</span><span class="sxs-lookup"><span data-stu-id="0a982-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="0a982-127">Выставление счета по транзакции по времени, которая была отредактирована для уменьшения количества.</span><span class="sxs-lookup"><span data-stu-id="0a982-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0a982-128">Сторнирование продаж с невыставленным счетом по часам и сумме в исходном утвержденном времени.</span><span class="sxs-lookup"><span data-stu-id="0a982-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0a982-129">Новая фактическая сумма продаж, по которой не выставлен счет, которая оплачивается по часам и сумме в отредактированных сведениях строки счета, сторнирование фактических данных продаж и эквивалентная фактическая сумма продаж, по которым выставлен счет.</span><span class="sxs-lookup"><span data-stu-id="0a982-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0a982-130">Новая фактическая сумма продаж, по которой не выставлен счет, которая не оплачивается по оставшимся часам и сумме после вычитания исправленных цифр в отредактированных сведениях строки счета, сторнирование фактических данных продаж и эквивалентная фактическая сумма продаж, по которым выставлен счет.</span><span class="sxs-lookup"><span data-stu-id="0a982-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0a982-131">Выставление счета по транзакции по времени, которая была отредактирована для увеличения количества.</span><span class="sxs-lookup"><span data-stu-id="0a982-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0a982-132">Сторнирование продаж с невыставленным счетом по часам и сумме в исходном утвержденном времени.</span><span class="sxs-lookup"><span data-stu-id="0a982-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0a982-133">Новая фактическая сумма продаж, по которой не выставлен счет, которая оплачивается по часам и сумме в отредактированных сведениях строки счета, сторнирование фактических данных продаж, по которым не выставлены счета, и эквивалентная фактическая сумма продаж, по которым выставлен счет.</span><span class="sxs-lookup"><span data-stu-id="0a982-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0a982-134">Выставление счета по транзакции за расходы без каких-либо изменений в черновике счета.</span><span class="sxs-lookup"><span data-stu-id="0a982-134">Invoicing an expense transaction without any edits on draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0a982-135">Сторнирование продаж с невыставленным счетом по количеству и сумме в исходных утвержденных расходах.</span><span class="sxs-lookup"><span data-stu-id="0a982-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0a982-136">Фактические данные продаж с выставленным счетом по количеству и сумме в исходных утвержденных расходах</span><span class="sxs-lookup"><span data-stu-id="0a982-136">A billed sales actual for the quantity and amount on the original expense approval</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="0a982-137">Выставление счета по транзакции по расходам, которая была отредактирована для уменьшения количества.</span><span class="sxs-lookup"><span data-stu-id="0a982-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0a982-138">Сторнирование продаж с невыставленным счетом по количеству и сумме в исходных утвержденных расходах.</span><span class="sxs-lookup"><span data-stu-id="0a982-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0a982-139">Новая фактическая сумма продаж, по которой не выставлен счет, которая оплачивается по количеству и сумме в отредактированных сведениях строки счета, сторнирование фактических данных продаж, по которым не выставлены счета, и эквивалентная фактическая сумма продаж, по которым выставлен счет.</span><span class="sxs-lookup"><span data-stu-id="0a982-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0a982-140">Новая фактическая сумма продаж, по которой не выставлен счет, которая не оплачивается по оставшемуся количеству и сумме после вычитания исправленных цифр в отредактированных сведениях строки счета, сторнирование фактических данных продаж, по которым не выставлены счета, и эквивалент фактической суммы продаж, по которым выставлен счет.</span><span class="sxs-lookup"><span data-stu-id="0a982-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0a982-141">Выставление счета по транзакции по расходам, которая была отредактирована для увеличения количества.</span><span class="sxs-lookup"><span data-stu-id="0a982-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0a982-142">Сторнирование продаж с невыставленным счетом по количеству и сумме в исходных утвержденных расходах.</span><span class="sxs-lookup"><span data-stu-id="0a982-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0a982-143">Новая фактическая сумма продаж, по которой не выставлен счет, которая оплачивается по количеству и сумме в отредактированных сведениях строки счета, сторнирование фактических данных продаж, по которым не выставлены счета, и эквивалентная фактическая сумма продаж, по которым выставлен счет.</span><span class="sxs-lookup"><span data-stu-id="0a982-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0a982-144">Выставление вознаграждения.</span><span class="sxs-lookup"><span data-stu-id="0a982-144">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0a982-145">Сторнирование продаж с невыставленным счетом по сумме вознаграждения в исходной строке журнала.</span><span class="sxs-lookup"><span data-stu-id="0a982-145">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0a982-146">Фактические данные продаж с выставленным счетом по количеству и сумме в исходной строке журнала вознаграждения.</span><span class="sxs-lookup"><span data-stu-id="0a982-146">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="0a982-147">Выставление счета за веху.</span><span class="sxs-lookup"><span data-stu-id="0a982-147">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0a982-148">Фактические данные продаж с выставленным счетом по сумме вехи в исходной вехе в строке контракта по проекту.</span><span class="sxs-lookup"><span data-stu-id="0a982-148">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="0a982-149">Выставление счета по строке контракта на основе продуктов.</span><span class="sxs-lookup"><span data-stu-id="0a982-149">Invoicing a product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0a982-150">Фактические данные продаж с выставленным счетом для строки продуктов с количеством и суммой, полученными из строки контракта на основе продукта.</span><span class="sxs-lookup"><span data-stu-id="0a982-150">A billed sales actual for the product line with the quantity and amount coming from the product-based contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>
