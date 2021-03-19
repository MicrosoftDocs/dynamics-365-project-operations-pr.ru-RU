---
title: Скорректированные счета — облегченное развертывание
description: В этой теме предоставлена информация о скорректированных счетах в Project Operations
author: rumant
manager: Annbe
ms.date: 10/15/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: eb949ff3a53bcba19d44e1c3d6fe08a6b368108d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274249"
---
# <a name="corrected-invoices---lite"></a><span data-ttu-id="23a5c-103">Скорректированные счета — облегченное развертывание</span><span class="sxs-lookup"><span data-stu-id="23a5c-103">Corrected invoices - lite</span></span>

<span data-ttu-id="23a5c-104">_**Относится к:** развертывание Lite — от сделки до счетов-проформ_</span><span class="sxs-lookup"><span data-stu-id="23a5c-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="23a5c-105">Подтвержденный счет по проекту может быть скорректирован для обработки изменений или кредитов по согласованию с заказчиком и менеджером проекта.</span><span class="sxs-lookup"><span data-stu-id="23a5c-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="23a5c-106">Чтобы внести изменения в подтвержденный счет, откройте подтвержденный счет и выберите **Исправить этот счет**.</span><span class="sxs-lookup"><span data-stu-id="23a5c-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="23a5c-107">Этот выбор недоступен, если счет по проекту не подтвержден.</span><span class="sxs-lookup"><span data-stu-id="23a5c-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="23a5c-108">Новый черновик счета создается из подтвержденного счета.</span><span class="sxs-lookup"><span data-stu-id="23a5c-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="23a5c-109">Все детали строк счета из ранее подтвержденного счета копируются в новый черновик.</span><span class="sxs-lookup"><span data-stu-id="23a5c-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="23a5c-110">Ниже приведены некоторые из ключевых моментов, которые нужно знать о деталях строк в новом исправленном счете:</span><span class="sxs-lookup"><span data-stu-id="23a5c-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="23a5c-111">Все количества обновляются до нуля.</span><span class="sxs-lookup"><span data-stu-id="23a5c-111">All quantities are updated to zero.</span></span> <span data-ttu-id="23a5c-112">Приложение предполагает, что все позиции, по которым выставлен счет, полностью кредитуются.</span><span class="sxs-lookup"><span data-stu-id="23a5c-112">The application assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="23a5c-113">При необходимости вы можете вручную обновить эти количества, чтобы отразить количество, по которому выставляется счет, а не количество, которое кредитуется.</span><span class="sxs-lookup"><span data-stu-id="23a5c-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="23a5c-114">На основе введенного количества приложение рассчитывает кредитуемое количество.</span><span class="sxs-lookup"><span data-stu-id="23a5c-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="23a5c-115">Эта сумма отражается в фактических данных, которые создаются при подтверждении исправленного счета.</span><span class="sxs-lookup"><span data-stu-id="23a5c-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="23a5c-116">Если вы вносите изменения в сумму налога, вы должны ввести правильную сумму налога, а не сумму налога, которая кредитуется.</span><span class="sxs-lookup"><span data-stu-id="23a5c-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="23a5c-117">Ранее подтвержденные строки контракта на основе продуктов не копируются.</span><span class="sxs-lookup"><span data-stu-id="23a5c-117">Previously confirmed product-based contract lines are not copied over.</span></span> <span data-ttu-id="23a5c-118">Обработка исправлений в счете по проекту на основе продуктов не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="23a5c-118">Processing corrections on a product-based project invoice is not supported.</span></span>
- <span data-ttu-id="23a5c-119">Исправления вех всегда обрабатываются как полные кредиты.</span><span class="sxs-lookup"><span data-stu-id="23a5c-119">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="23a5c-120">Суммы предоплаты или авансы могут быть исправлены, если клиенту выставлен счет на неправильную сумму.</span><span class="sxs-lookup"><span data-stu-id="23a5c-120">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="23a5c-121">Выверки предоплаты и авансов можно исправить, если неверная сумма была использована для сверки с расходами в ранее подтвержденном счете.</span><span class="sxs-lookup"><span data-stu-id="23a5c-121">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="23a5c-122">Детали строк счетов, которые являются исправлениями других уже выставленных счетов, имеют в поле **Исправление** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="23a5c-122">Invoice line details that are corrections to other already invoiced charges have the field **Correction** set to **Yes**.</span></span> <span data-ttu-id="23a5c-123">В счетах, в которых есть исправленные данные строк счетов, есть поле с именем **Есть исправления**, в котором также установлено значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="23a5c-123">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a><span data-ttu-id="23a5c-124">Фактические данные, созданные при подтверждении корректирующего счета:</span><span class="sxs-lookup"><span data-stu-id="23a5c-124">Actuals created on Confirmation of a corrective invoice:</span></span>

<span data-ttu-id="23a5c-125">Ниже представлены фактические данные, созданные приложением при подтверждении корректировки на основе операций, выполненных над черновиком корректировочного счета до подтверждения.</span><span class="sxs-lookup"><span data-stu-id="23a5c-125">Below are the actuals created by the application on confirmation of a corrective based on the operations performed on the draft corrective invoice before confirmation.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="23a5c-126">
                    <strong>Сценарий</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23a5c-126">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="23a5c-127">
                    <strong>Фактические данные, созданные при подтверждении</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23a5c-127">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="23a5c-128">Подтвердите исправление выставленной предоплаты или аванса.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="23a5c-128">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="23a5c-129">Сторнирование продажи с невыставленным счетом для предоплаты или аванса, созданного для выверки.</span><span class="sxs-lookup"><span data-stu-id="23a5c-129">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="23a5c-130">Эта сумма является положительной, потому что она предназначена для компенсации отрицательного результата, который был создан при выставлении предоплаты или аванса.</span><span class="sxs-lookup"><span data-stu-id="23a5c-130">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="23a5c-131">Фактические данные сторнирования продаж с выставленными счетам создаются для суммы предоплаты или аванса, чтобы сторнировать исходные продажи с выставленными счетами.</span><span class="sxs-lookup"><span data-stu-id="23a5c-131">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="23a5c-132">Новые фактические данные продаж с выставленными счетами создаются для исправленной суммы в строке исправленного счета на основе предоплаты или аванса.</span><span class="sxs-lookup"><span data-stu-id="23a5c-132">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="23a5c-133">Фактическая сумма продаж с невыставленными счетами с отрицательной суммой строки счета на основе предоплаты или аванса, которая будет использоваться для сверки.</span><span class="sxs-lookup"><span data-stu-id="23a5c-133">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="23a5c-134">Подтверждение исправления ранее выверенной предоплаты или аванса.</span><span class="sxs-lookup"><span data-stu-id="23a5c-134">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="23a5c-135">Сторнирование продажи с невыставленным счетом для предоплаты или аванса, созданного для выверки.</span><span class="sxs-lookup"><span data-stu-id="23a5c-135">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="23a5c-136">Эта сумма является положительной и предназначена для компенсации отрицательного результата, который был создан при выполнении предыдущей выверки.</span><span class="sxs-lookup"><span data-stu-id="23a5c-136">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="23a5c-137">Фактические данные сторнирования продажи с выставленными счетами на сумму в предыдущем счете.</span><span class="sxs-lookup"><span data-stu-id="23a5c-137">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="23a5c-138">Новые фактические данные продаж с выставленными счетами для исправленной суммы предоплаты, которая применена в исправленном счете.</span><span class="sxs-lookup"><span data-stu-id="23a5c-138">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="23a5c-139">Фактическая сумма продаж с невыставленными счетами с отрицательной суммой из исправленного остатка предоплаты или аванса, которая будет использоваться для сверки последующих счетов.</span><span class="sxs-lookup"><span data-stu-id="23a5c-139">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="23a5c-140">Выставление счета на полную сумму транзакции по ранее выставленному счету за время.</span><span class="sxs-lookup"><span data-stu-id="23a5c-140">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="23a5c-141">Сторнирование продаж с выставленным счетом по часам и сумме в сведениях исходной строки счета за время.</span><span class="sxs-lookup"><span data-stu-id="23a5c-141">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="23a5c-142">Новая фактическая сумма продаж с невыставленным счетом за часы и сумму в сведениях исходной строки счета за время.</span><span class="sxs-lookup"><span data-stu-id="23a5c-142">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="23a5c-143">Выставление счета на частичный кредит по транзакции за время.</span><span class="sxs-lookup"><span data-stu-id="23a5c-143">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="23a5c-144">Сторнирование продаж с выставленным счетом по часам и сумме, выставленным в сведениях исходной строки счета за время.</span><span class="sxs-lookup"><span data-stu-id="23a5c-144">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="23a5c-145">Новая фактическая сумма продаж, по которой не выставлен счет, которая оплачивается по часам и сумме в отредактированных сведениях строки счета, сторнирование этого и эквивалентная фактическая сумма продаж, по которым выставлен счет.</span><span class="sxs-lookup"><span data-stu-id="23a5c-145">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="23a5c-146">Новый фактический объем продаж, по которому не выставлены счета, который подлежит оплате за оставшиеся часы и сумму после вычета исправленных цифр в сведениях строки счета.</span><span class="sxs-lookup"><span data-stu-id="23a5c-146">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="23a5c-147">Выставление счета на полную сумму транзакции по ранее выставленному счету за расходы.</span><span class="sxs-lookup"><span data-stu-id="23a5c-147">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="23a5c-148">Сторнирование продаж с выставленным счетом по количеству и сумме в сведениях исходной строки счета за расходы.</span><span class="sxs-lookup"><span data-stu-id="23a5c-148">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="23a5c-149">Новая фактическая сумма продаж, за которые не выставлены счета, по количеству и сумме в сведениях исходной строки счета за расходы.</span><span class="sxs-lookup"><span data-stu-id="23a5c-149">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="23a5c-150">Выставление счета на частичную сумму транзакции по ранее выставленному счету за расходы.</span><span class="sxs-lookup"><span data-stu-id="23a5c-150">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="23a5c-151">Сторнирование продаж с выставленным счетом по выставленным количеству и сумме в сведениях исходной строки счета за расходы.</span><span class="sxs-lookup"><span data-stu-id="23a5c-151">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="23a5c-152">Новая фактическая сумма продаж, по которой не выставлен счет, которая оплачивается по количестве и сумме в скорректированных сведениях строки счета, сторнирование этого и эквивалентная фактическая сумма продаж, по которым выставлен счет.</span><span class="sxs-lookup"><span data-stu-id="23a5c-152">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="23a5c-153">Новый фактический объем продаж, по которому не выставлены счета, который подлежит оплате за оставшееся количество и сумму после вычета исправленных цифр в сведениях строки счета.</span><span class="sxs-lookup"><span data-stu-id="23a5c-153">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="23a5c-154">Выставление счета на полную сумму транзакции по ранее выставленному счету за вознаграждение.</span><span class="sxs-lookup"><span data-stu-id="23a5c-154">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="23a5c-155">Сторнирование продаж с выставленным счетом по количеству и сумме в сведениях исходной строки счета за вознаграждение.</span><span class="sxs-lookup"><span data-stu-id="23a5c-155">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="23a5c-156">Новая фактическая сумма продаж, за которые не выставлены счета, по количеству и сумме в сведениях исходной строки счета за вознаграждение.</span><span class="sxs-lookup"><span data-stu-id="23a5c-156">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="23a5c-157">Выставление счета на частичную сумму транзакции по ранее выставленному счету за вознаграждение.</span><span class="sxs-lookup"><span data-stu-id="23a5c-157">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="23a5c-158">Сторнирование продаж с выставленным счетом по количеству и выставленной сумме в сведениях исходной строки счета за вознаграждение.</span><span class="sxs-lookup"><span data-stu-id="23a5c-158">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="23a5c-159">Новая фактическая сумма продаж, по которой не выставлен счет, которая оплачивается по количестве и сумме в отредактированных корректирующих сведениях строки счета, сторнирование этого и эквивалентная фактическая сумма продаж, по которым выставлен счет.</span><span class="sxs-lookup"><span data-stu-id="23a5c-159">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="23a5c-160">Выставление счета на полную сумму транзакции по ранее выставленному счету за веху.</span><span class="sxs-lookup"><span data-stu-id="23a5c-160">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="23a5c-161">Сторнирование продаж с выставленным счетом по сумме в сведениях исходной строки счета за веху.</span><span class="sxs-lookup"><span data-stu-id="23a5c-161">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="23a5c-162">Статус промежуточного счета или выставления счетов в строке контракта по проекту обновляется до **Готово к выставлению счета**.</span><span class="sxs-lookup"><span data-stu-id="23a5c-162">The milestone invoice or billing status on the project contract line is updated to **Ready to Invoice**.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="23a5c-163">Выставление счета на частичную сумму транзакции по ранее выставленному счету за веху.</span><span class="sxs-lookup"><span data-stu-id="23a5c-163">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="23a5c-164">не поддерживается</span><span class="sxs-lookup"><span data-stu-id="23a5c-164">Unsupported</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="23a5c-165">Кредиты и исправления строки контракта на основе продукта, по которой ранее были выставлены счета.</span><span class="sxs-lookup"><span data-stu-id="23a5c-165">Credits and corrections of a previously invoiced product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="23a5c-166">не поддерживается</span><span class="sxs-lookup"><span data-stu-id="23a5c-166">Unsupported</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]