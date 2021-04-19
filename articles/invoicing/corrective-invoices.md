---
title: Создание корректирующих счетов на основе проектов
description: В этой теме содержится информация о корректирующих счетах в Project Operations.
author: rumant
manager: Annbe
ms.date: 03/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 32772d64b3fc77f0af9618edff40e3b295593454
ms.sourcegitcommit: 504c09365bf404c1f1aa9b5034c1e1e5bc9d0d54
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788890"
---
# <a name="create-corrective-project-based-invoices"></a><span data-ttu-id="098cd-103">Создание корректирующих счетов на основе проектов</span><span class="sxs-lookup"><span data-stu-id="098cd-103">Create corrective project-based invoices</span></span> 

<span data-ttu-id="098cd-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/без запасов_</span><span class="sxs-lookup"><span data-stu-id="098cd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="098cd-105">Подтвержденный счет по проекту может быть скорректирован для обработки изменений или кредитов по согласованию с заказчиком и менеджером проекта.</span><span class="sxs-lookup"><span data-stu-id="098cd-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="098cd-106">Чтобы внести изменения в подтвержденный счет, откройте подтвержденный счет и выберите **Исправить этот счет**.</span><span class="sxs-lookup"><span data-stu-id="098cd-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="098cd-107">Этот выбор недоступен, если счет по проекту не подтвержден.</span><span class="sxs-lookup"><span data-stu-id="098cd-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="098cd-108">Новый черновик счета создается из подтвержденного счета.</span><span class="sxs-lookup"><span data-stu-id="098cd-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="098cd-109">Все детали строк счета из ранее подтвержденного счета копируются в новый черновик.</span><span class="sxs-lookup"><span data-stu-id="098cd-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="098cd-110">Ниже приведены некоторые ключевые моменты, которые помогут вам лучше понять сведения строки в новом исправленном счете:</span><span class="sxs-lookup"><span data-stu-id="098cd-110">The following are some key points to help you understand more about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="098cd-111">Все количества обновляются до нуля.</span><span class="sxs-lookup"><span data-stu-id="098cd-111">All quantities are updated to zero.</span></span> <span data-ttu-id="098cd-112">Предполагается, что все номенклатуры с выставленными счетами, полностью кредитуются.</span><span class="sxs-lookup"><span data-stu-id="098cd-112">This assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="098cd-113">При необходимости вы можете вручную обновить эти количества, чтобы отразить количество, по которому выставляется счет, а не количество, которое кредитуется.</span><span class="sxs-lookup"><span data-stu-id="098cd-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="098cd-114">На основе введенного количества приложение рассчитывает кредитуемое количество.</span><span class="sxs-lookup"><span data-stu-id="098cd-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="098cd-115">Эта сумма отражается в фактических данных, которые создаются при подтверждении исправленного счета.</span><span class="sxs-lookup"><span data-stu-id="098cd-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="098cd-116">Если вы вносите изменения в сумму налога, вы должны ввести правильную сумму налога, а не сумму налога, которая кредитуется.</span><span class="sxs-lookup"><span data-stu-id="098cd-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="098cd-117">Исправления вех всегда обрабатываются как полные кредиты.</span><span class="sxs-lookup"><span data-stu-id="098cd-117">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="098cd-118">Суммы предоплаты или авансы могут быть исправлены, если клиенту выставлен счет на неправильную сумму.</span><span class="sxs-lookup"><span data-stu-id="098cd-118">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="098cd-119">Выверки предоплаты и авансов можно исправить, если неверная сумма была использована для сверки с расходами в ранее подтвержденном счете.</span><span class="sxs-lookup"><span data-stu-id="098cd-119">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="098cd-120">У сведений строки счета, которые являются исправлением других платежей с уже выставленными счетами, поле **Исправление** задано как **Да**.</span><span class="sxs-lookup"><span data-stu-id="098cd-120">Invoice line details that are corrections to other already invoiced charges have the **Correction** field set to **Yes**.</span></span> <span data-ttu-id="098cd-121">В счетах, в которых есть исправленные данные строк счетов, есть поле с именем **Есть исправления**, в котором также установлено значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="098cd-121">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a><span data-ttu-id="098cd-122">Фактические данные, созданные при подтверждении корректирующего счета</span><span class="sxs-lookup"><span data-stu-id="098cd-122">Actuals created on confirmation of a corrective invoice</span></span>

<span data-ttu-id="098cd-123">В следующей таблице перечислены фактические данные, которые создаются при подтверждении корректирующего счета.</span><span class="sxs-lookup"><span data-stu-id="098cd-123">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="098cd-124">
                    <strong>Сценарий</strong>
                </span><span class="sxs-lookup"><span data-stu-id="098cd-124">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="098cd-125">
                    <strong>Фактические данные, созданные при подтверждении</strong>
                </span><span class="sxs-lookup"><span data-stu-id="098cd-125">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="098cd-126">Подтвердите исправление выставленной предоплаты или аванса.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="098cd-126">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="098cd-127">Сторнирование продажи с невыставленным счетом для предоплаты или аванса, созданного для выверки.</span><span class="sxs-lookup"><span data-stu-id="098cd-127">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="098cd-128">Эта сумма является положительной, потому что она предназначена для компенсации отрицательного результата, который был создан при выставлении предоплаты или аванса.</span><span class="sxs-lookup"><span data-stu-id="098cd-128">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="098cd-129">Фактические данные сторнирования продаж с выставленными счетам создаются для суммы предоплаты или аванса, чтобы сторнировать исходные продажи с выставленными счетами.</span><span class="sxs-lookup"><span data-stu-id="098cd-129">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="098cd-130">Новые фактические данные продаж с выставленными счетами создаются для исправленной суммы в строке исправленного счета на основе предоплаты или аванса.</span><span class="sxs-lookup"><span data-stu-id="098cd-130">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="098cd-131">Фактическая сумма продаж с невыставленными счетами с отрицательной суммой строки счета на основе предоплаты или аванса, которая будет использоваться для сверки.</span><span class="sxs-lookup"><span data-stu-id="098cd-131">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="098cd-132">Подтверждение исправления ранее выверенной предоплаты или аванса.</span><span class="sxs-lookup"><span data-stu-id="098cd-132">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="098cd-133">Сторнирование продажи с невыставленным счетом для предоплаты или аванса, созданного для выверки.</span><span class="sxs-lookup"><span data-stu-id="098cd-133">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="098cd-134">Эта сумма является положительной и предназначена для компенсации отрицательного результата, который был создан при выполнении предыдущей выверки.</span><span class="sxs-lookup"><span data-stu-id="098cd-134">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="098cd-135">Фактические данные сторнирования продажи с выставленными счетами на сумму в предыдущем счете.</span><span class="sxs-lookup"><span data-stu-id="098cd-135">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="098cd-136">Новые фактические данные продаж с выставленными счетами для исправленной суммы предоплаты, которая применена в исправленном счете.</span><span class="sxs-lookup"><span data-stu-id="098cd-136">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="098cd-137">Фактическая сумма продаж с невыставленными счетами с отрицательной суммой из исправленного остатка предоплаты или аванса, которая будет использоваться для сверки последующих счетов.</span><span class="sxs-lookup"><span data-stu-id="098cd-137">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="098cd-138">Выставление счета на полную сумму транзакции по ранее выставленному счету за время.</span><span class="sxs-lookup"><span data-stu-id="098cd-138">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="098cd-139">Сторнирование продаж с выставленным счетом по часам и сумме в сведениях исходной строки счета за время.</span><span class="sxs-lookup"><span data-stu-id="098cd-139">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="098cd-140">Новая фактическая сумма продаж с невыставленным счетом за часы и сумму в сведениях исходной строки счета за время.</span><span class="sxs-lookup"><span data-stu-id="098cd-140">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="098cd-141">Выставление счета на частичный кредит по транзакции за время.</span><span class="sxs-lookup"><span data-stu-id="098cd-141">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="098cd-142">Сторнирование продаж с выставленным счетом по часам и сумме, выставленным в сведениях исходной строки счета за время.</span><span class="sxs-lookup"><span data-stu-id="098cd-142">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="098cd-143">Новая фактическая сумма продаж, по которой не выставлен счет, которая оплачивается по часам и сумме в отредактированных сведениях строки счета, сторнирование этого и эквивалентная фактическая сумма продаж, по которым выставлен счет.</span><span class="sxs-lookup"><span data-stu-id="098cd-143">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="098cd-144">Новый фактический объем продаж, по которому не выставлены счета, который подлежит оплате за оставшиеся часы и сумму после вычета исправленных цифр в сведениях строки счета.</span><span class="sxs-lookup"><span data-stu-id="098cd-144">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="098cd-145">Выставление счета на полную сумму транзакции по ранее выставленному счету за расходы.</span><span class="sxs-lookup"><span data-stu-id="098cd-145">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="098cd-146">Сторнирование продаж с выставленным счетом по количеству и сумме в сведениях исходной строки счета за расходы.</span><span class="sxs-lookup"><span data-stu-id="098cd-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="098cd-147">Новая фактическая сумма продаж, за которые не выставлены счета, по количеству и сумме в сведениях исходной строки счета за расходы.</span><span class="sxs-lookup"><span data-stu-id="098cd-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="098cd-148">Выставление счета на частичную сумму транзакции по ранее выставленному счету за расходы.</span><span class="sxs-lookup"><span data-stu-id="098cd-148">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="098cd-149">Сторнирование продаж с выставленным счетом по выставленным количеству и сумме в сведениях исходной строки счета за расходы.</span><span class="sxs-lookup"><span data-stu-id="098cd-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="098cd-150">Новая фактическая сумма продаж, по которой не выставлен счет, которая оплачивается по количестве и сумме в скорректированных сведениях строки счета, сторнирование этого и эквивалентная фактическая сумма продаж, по которым выставлен счет.</span><span class="sxs-lookup"><span data-stu-id="098cd-150">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="098cd-151">Новый фактический объем продаж, по которому не выставлены счета, который подлежит оплате за оставшееся количество и сумму после вычета исправленных цифр в сведениях строки счета.</span><span class="sxs-lookup"><span data-stu-id="098cd-151">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="098cd-152">Выставление счета на полную сумму транзакции по ранее выставленному счету за вознаграждение.</span><span class="sxs-lookup"><span data-stu-id="098cd-152">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="098cd-153">Сторнирование продаж с выставленным счетом по количеству и сумме в сведениях исходной строки счета за вознаграждение.</span><span class="sxs-lookup"><span data-stu-id="098cd-153">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="098cd-154">Новая фактическая сумма продаж, за которые не выставлены счета, по количеству и сумме в сведениях исходной строки счета за вознаграждение.</span><span class="sxs-lookup"><span data-stu-id="098cd-154">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="098cd-155">Выставление счета на частичную сумму транзакции по ранее выставленному счету за вознаграждение.</span><span class="sxs-lookup"><span data-stu-id="098cd-155">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="098cd-156">Сторнирование продаж с выставленным счетом по количеству и выставленной сумме в сведениях исходной строки счета за вознаграждение.</span><span class="sxs-lookup"><span data-stu-id="098cd-156">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="098cd-157">Новая фактическая сумма продаж, по которой не выставлен счет, которая оплачивается по количестве и сумме в отредактированных корректирующих сведениях строки счета, сторнирование этого и эквивалентная фактическая сумма продаж, по которым выставлен счет.</span><span class="sxs-lookup"><span data-stu-id="098cd-157">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="098cd-158">Выставление счета на полную сумму транзакции по ранее выставленному счету за веху.</span><span class="sxs-lookup"><span data-stu-id="098cd-158">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="098cd-159">Сторнирование продаж с выставленным счетом по сумме в сведениях исходной строки счета за веху.</span><span class="sxs-lookup"><span data-stu-id="098cd-159">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="098cd-160">Статус счета вехи обновляется с <b>Счет клиента разнесен</b> на <b>Готово к выставлению счета</b>.</span><span class="sxs-lookup"><span data-stu-id="098cd-160">The invoice status on the milestone is updated from <b>Customer invoice posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="098cd-161">Выставление счета на частичную сумму транзакции по ранее выставленному счету за веху.</span><span class="sxs-lookup"><span data-stu-id="098cd-161">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="098cd-162">не поддерживается</span><span class="sxs-lookup"><span data-stu-id="098cd-162">Unsupported</span></span> </p>
            </td>
        </tr>        
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
