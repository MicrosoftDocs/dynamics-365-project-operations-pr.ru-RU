---
title: Подтверждение счета-проформы на основе проектов
description: В этой теме содержится информация о подтверждении счета-проформы на основе проектов.
author: rumant
manager: AnnBe
ms.date: 04/05/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 53c647dca506822312053fb5c9b086a2947974c2
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867147"
---
# <a name="confirm-a-proforma-project-based-invoice"></a><span data-ttu-id="83bed-103">Подтверждение счета-проформы на основе проектов</span><span class="sxs-lookup"><span data-stu-id="83bed-103">Confirm a proforma project-based invoice</span></span>

<span data-ttu-id="83bed-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/без запасов_</span><span class="sxs-lookup"><span data-stu-id="83bed-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="83bed-105">После подтверждения счета-проформы статус счета по проекту изменяется на **Подтверждено**.</span><span class="sxs-lookup"><span data-stu-id="83bed-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="83bed-106">Когда счет подтвержден, он становится доступным только для чтения.</span><span class="sxs-lookup"><span data-stu-id="83bed-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="83bed-107">В дальнейшем счет можно будет исправить только в том случае, если есть какие-либо исправления или кредиты со стороны клиента.</span><span class="sxs-lookup"><span data-stu-id="83bed-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits.</span></span>

<span data-ttu-id="83bed-108">В следующей таблице перечислены фактические данные, созданные системой.</span><span class="sxs-lookup"><span data-stu-id="83bed-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="83bed-109">Эти фактические данные создаются при выполнении определенных операций с черновиком счета по проекту до его подтверждения.</span><span class="sxs-lookup"><span data-stu-id="83bed-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="83bed-110">
                    <strong>Сценарий</strong>
                </span><span class="sxs-lookup"><span data-stu-id="83bed-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="83bed-111">
                    <strong>Фактические данные, созданные при подтверждении</strong>
                </span><span class="sxs-lookup"><span data-stu-id="83bed-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="83bed-112">Выставление счета на аванс или предоплату</span><span class="sxs-lookup"><span data-stu-id="83bed-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="83bed-113">Фактические продажи типа <strong>Предоплата</strong>, за которые не выставлен счет, создаются на сумму аванса или предоплаты.</span><span class="sxs-lookup"><span data-stu-id="83bed-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="83bed-114">Фактические продажи, по которым не выставлен счет, с отрицательной суммой гонорара или аванса, которая будет использоваться для выверки.</span><span class="sxs-lookup"><span data-stu-id="83bed-114">An unbilled sales actual with a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="83bed-115">После полной выверки предоплаты или аванса по счету.</span><span class="sxs-lookup"><span data-stu-id="83bed-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="83bed-116">Сторнирование продажи с невыставленным счетом для предоплаты или аванса, созданного для выверки.</span><span class="sxs-lookup"><span data-stu-id="83bed-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="83bed-117">Эта сумма является положительной, так как она предназначена для компенсации отрицательного результата, который был создан при выставлении предоплаты или аванса.</span><span class="sxs-lookup"><span data-stu-id="83bed-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="83bed-118">Фактические данные продажи с выставленными счетами на сумму в этом счете.</span><span class="sxs-lookup"><span data-stu-id="83bed-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="83bed-119">После частичной выверки предоплаты или аванса по счету.</span><span class="sxs-lookup"><span data-stu-id="83bed-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="83bed-120">Сторнирование продажи с невыставленным счетом для предоплаты или аванса, созданного для выверки.</span><span class="sxs-lookup"><span data-stu-id="83bed-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="83bed-121">Эта сумма является положительной, так как она предназначена для компенсации отрицательного результата, который был создан при выставлении предоплаты или аванса.</span><span class="sxs-lookup"><span data-stu-id="83bed-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="83bed-122">Фактические данные продажи с выставленными счетами на сумму в этом счете.</span><span class="sxs-lookup"><span data-stu-id="83bed-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="83bed-123">Отрицательная фактическая сумма продаж с невыставленными счетами, равная оставшейся сумме предоплаты или аванса для использования для выверки в будущих счетах.</span><span class="sxs-lookup"><span data-stu-id="83bed-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="83bed-124">Выставление счета по транзакции за время без каких-либо изменений в черновике счета.</span><span class="sxs-lookup"><span data-stu-id="83bed-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="83bed-125">Сторнирование продаж с невыставленным счетом по часам и сумме в исходном утвержденном времени.</span><span class="sxs-lookup"><span data-stu-id="83bed-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="83bed-126">Фактические данные продаж с выставленным счетом по часам и сумме в исходном утвержденном времени.</span><span class="sxs-lookup"><span data-stu-id="83bed-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="83bed-127">Выставление счета по транзакции по времени, которая была отредактирована для уменьшения количества.</span><span class="sxs-lookup"><span data-stu-id="83bed-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="83bed-128">Сторнирование продаж с невыставленным счетом по часам и сумме в исходном утвержденном времени.</span><span class="sxs-lookup"><span data-stu-id="83bed-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="83bed-129">Новая фактическая сумма продаж, по которой не выставлен счет, которая оплачивается по часам и сумме в отредактированных сведениях строки счета, сторнирование фактических данных продаж и эквивалентная фактическая сумма продаж, по которым выставлен счет.</span><span class="sxs-lookup"><span data-stu-id="83bed-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="83bed-130">Новые фактические продажи с невыставленными счетами, не подлежащие оплате, за оставшиеся часы и сумму после вычета исправленных данных в измененных сведениях строки счета, сторнирование фактических продаж и эквивалентные фактические продажи с выставленными счетами.</span><span class="sxs-lookup"><span data-stu-id="83bed-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="83bed-131">Выставление счета по транзакции по времени, которая была отредактирована для увеличения количества.</span><span class="sxs-lookup"><span data-stu-id="83bed-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="83bed-132">Сторнирование продаж с невыставленным счетом по часам и сумме в исходном утвержденном времени.</span><span class="sxs-lookup"><span data-stu-id="83bed-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="83bed-133">Новая фактическая сумма продаж, по которой не выставлен счет, которая оплачивается по часам и сумме в отредактированных сведениях строки счета, сторнирование фактических данных продаж, по которым не выставлены счета, и эквивалентная фактическая сумма продаж, по которым выставлен счет.</span><span class="sxs-lookup"><span data-stu-id="83bed-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="83bed-134">Выставление счета по транзакции за расходы без каких-либо изменений в черновике счета.</span><span class="sxs-lookup"><span data-stu-id="83bed-134">Invoicing an expense transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="83bed-135">Сторнирование продаж с невыставленным счетом по количеству и сумме в исходных утвержденных расходах.</span><span class="sxs-lookup"><span data-stu-id="83bed-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="83bed-136">Фактические данные продаж с выставленным счетом по количеству и сумме в исходных утвержденных расходах.</span><span class="sxs-lookup"><span data-stu-id="83bed-136">A billed sales actual for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="83bed-137">Выставление счета по транзакции по расходам, которая была отредактирована для уменьшения количества.</span><span class="sxs-lookup"><span data-stu-id="83bed-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="83bed-138">Сторнирование продаж с невыставленным счетом по количеству и сумме в исходных утвержденных расходах.</span><span class="sxs-lookup"><span data-stu-id="83bed-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="83bed-139">Новая фактическая сумма продаж, по которой не выставлен счет, которая оплачивается по количеству и сумме в отредактированных сведениях строки счета, сторнирование фактических данных продаж, по которым не выставлены счета, и эквивалентная фактическая сумма продаж, по которым выставлен счет.</span><span class="sxs-lookup"><span data-stu-id="83bed-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="83bed-140">Новая фактическая сумма продаж, по которой не выставлен счет, которая не оплачивается по оставшемуся количеству и сумме после вычитания исправленных цифр в отредактированных сведениях строки счета, сторнирование фактических данных продаж, по которым не выставлены счета, и эквивалент фактической суммы продаж, по которым выставлен счет.</span><span class="sxs-lookup"><span data-stu-id="83bed-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="83bed-141">Выставление счета по транзакции по расходам, которая была отредактирована для увеличения количества.</span><span class="sxs-lookup"><span data-stu-id="83bed-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="83bed-142">Сторнирование продаж с невыставленным счетом по количеству и сумме в исходных утвержденных расходах.</span><span class="sxs-lookup"><span data-stu-id="83bed-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="83bed-143">Новая фактическая сумма продаж, по которой не выставлен счет, которая оплачивается по количеству и сумме в отредактированных сведениях строки счета, сторнирование фактических данных продаж, по которым не выставлены счета, и эквивалентная фактическая сумма продаж, по которым выставлен счет.</span><span class="sxs-lookup"><span data-stu-id="83bed-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="83bed-144">Выставление счет по проводке материала без каких-либо изменений в черновике счета.</span><span class="sxs-lookup"><span data-stu-id="83bed-144">Invoicing a material transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="83bed-145">Сторнирование продаж без выставленных счетов для количества и суммы в исходном утверждении по использованию материала.</span><span class="sxs-lookup"><span data-stu-id="83bed-145">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="83bed-146">Фактические продажи с выставленными счетами для количества и суммы в исходном утверждении по использованию материала.</span><span class="sxs-lookup"><span data-stu-id="83bed-146">A billed sales actual for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="83bed-147">Фактурирование проводки материала, которая была отредактирована для уменьшения количества.</span><span class="sxs-lookup"><span data-stu-id="83bed-147">Invoicing a material transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="83bed-148">Сторнирование продаж без выставленных счетов для количества и суммы в исходном утверждении по времени.</span><span class="sxs-lookup"><span data-stu-id="83bed-148">An unbilled sales reversal for the quantity and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="83bed-149">Новая фактическая сумма продаж, по которой не выставлен счет, которая оплачивается по количеству и сумме в отредактированных сведениях строки счета, сторнирование фактических данных продаж, по которым не выставлены счета, и эквивалентная фактическая сумма продаж, по которым выставлен счет.</span><span class="sxs-lookup"><span data-stu-id="83bed-149">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="83bed-150">Новая фактическая сумма продаж, по которой не выставлен счет, которая не оплачивается по оставшемуся количеству и сумме после вычитания исправленных цифр в отредактированных сведениях строки счета, сторнирование фактических данных продаж, по которым не выставлены счета, и эквивалент фактической суммы продаж, по которым выставлен счет.</span><span class="sxs-lookup"><span data-stu-id="83bed-150">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="83bed-151">Фактурирование проводки материала, которая была отредактирована для увеличения количества.</span><span class="sxs-lookup"><span data-stu-id="83bed-151">Invoicing a material transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="83bed-152">Сторнирование продаж без выставленных счетов для количества и суммы в исходном утверждении по использованию материала.</span><span class="sxs-lookup"><span data-stu-id="83bed-152">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="83bed-153">Новая фактическая сумма продаж, по которой не выставлен счет, которая оплачивается по количеству и сумме в отредактированных сведениях строки счета, сторнирование фактических данных продаж, по которым не выставлены счета, и эквивалентная фактическая сумма продаж, по которым выставлен счет.</span><span class="sxs-lookup"><span data-stu-id="83bed-153">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="83bed-154">Выставление вознаграждения.</span><span class="sxs-lookup"><span data-stu-id="83bed-154">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="83bed-155">Сторнирование продаж с невыставленным счетом по сумме вознаграждения в исходной строке журнала.</span><span class="sxs-lookup"><span data-stu-id="83bed-155">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="83bed-156">Фактические данные продаж с выставленным счетом по количеству и сумме в исходной строке журнала вознаграждения.</span><span class="sxs-lookup"><span data-stu-id="83bed-156">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="83bed-157">Выставление счета за веху.</span><span class="sxs-lookup"><span data-stu-id="83bed-157">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="83bed-158">Фактические данные продаж с выставленным счетом по сумме вехи в исходной вехе в строке контракта по проекту.</span><span class="sxs-lookup"><span data-stu-id="83bed-158">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
       
    </tbody>
</table>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
