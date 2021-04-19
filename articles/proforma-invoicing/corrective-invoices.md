---
title: Корректирующие счетов на основе проектов
description: В этой теме содержится информация о создании и подтверждении корректирующих счетов на основе проектов в Project Operations.
author: rumant
manager: Annbe
ms.date: 03/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fc96bb40f5207efc381986d46a3e37dfc1dc111c
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867057"
---
# <a name="corrective-project-based-invoices"></a><span data-ttu-id="d2456-103">Корректирующие счетов на основе проектов</span><span class="sxs-lookup"><span data-stu-id="d2456-103">Corrective project-based invoices</span></span>

<span data-ttu-id="d2456-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/без запасов_</span><span class="sxs-lookup"><span data-stu-id="d2456-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="d2456-105">Подтвержденный счет по проекту может быть скорректирован для обработки изменений или кредитов по согласованию с заказчиком и менеджером проекта.</span><span class="sxs-lookup"><span data-stu-id="d2456-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="d2456-106">Чтобы внести изменения в подтвержденный счет, откройте подтвержденный счет и выберите **Исправить этот счет**.</span><span class="sxs-lookup"><span data-stu-id="d2456-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="d2456-107">Этот выбор недоступен, пока счет проекта не подтвержден или в счете на основе проектов есть авансы или гонорары, или выверка авансов или гонораров.</span><span class="sxs-lookup"><span data-stu-id="d2456-107">This selection isn't available unless a project invoice is confirmed or the project-based invoice has advances or retainers or reconciliations of advances or retainers.</span></span>

<span data-ttu-id="d2456-108">Новый черновик счета создается из подтвержденного счета.</span><span class="sxs-lookup"><span data-stu-id="d2456-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="d2456-109">Все детали строк счета из ранее подтвержденного счета копируются в новый черновик.</span><span class="sxs-lookup"><span data-stu-id="d2456-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="d2456-110">Ниже приведены некоторые из ключевых моментов, которые нужно знать о деталях строк в новом исправленном счете:</span><span class="sxs-lookup"><span data-stu-id="d2456-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="d2456-111">Все количества обновляются до нуля.</span><span class="sxs-lookup"><span data-stu-id="d2456-111">All quantities are updated to zero.</span></span> <span data-ttu-id="d2456-112">Dynamics 365 Project Operations предполагает, что все номенклатуры с выставленными счетами, полностью кредитуются.</span><span class="sxs-lookup"><span data-stu-id="d2456-112">Dynamics 365 Project Operations assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="d2456-113">При необходимости вы можете вручную обновить эти количества, чтобы отразить количество, по которому выставляется счет, а не количество, которое кредитуется.</span><span class="sxs-lookup"><span data-stu-id="d2456-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="d2456-114">На основе введенного количества приложение рассчитывает кредитуемое количество.</span><span class="sxs-lookup"><span data-stu-id="d2456-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="d2456-115">Эта сумма отражается в фактических данных, которые создаются при подтверждении исправленного счета.</span><span class="sxs-lookup"><span data-stu-id="d2456-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="d2456-116">Если вы вносите изменения в сумму налога, вы должны ввести правильную сумму налога, а не сумму налога, которая кредитуется.</span><span class="sxs-lookup"><span data-stu-id="d2456-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="d2456-117">Исправления вех всегда обрабатываются как полные кредиты.</span><span class="sxs-lookup"><span data-stu-id="d2456-117">Milestone corrections are always processed as full credits.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="d2456-118">Для сведений строки счета, которые являются исправлением других платежей с уже выставленными счетами, поле **Исправление** задано как **Да**.</span><span class="sxs-lookup"><span data-stu-id="d2456-118">For invoice line details that are corrections to other already invoiced charges, the **Correction** field is set to **Yes**.</span></span> <span data-ttu-id="d2456-119">Для счетов, у которых есть исправленные сведения строки счета поле **Содержит корректировки** задано как **Да**.</span><span class="sxs-lookup"><span data-stu-id="d2456-119">For invoices that have corrected invoice line details, the **Has corrections** field is set to **Yes**.</span></span>

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a><span data-ttu-id="d2456-120">Фактические данные, созданные при подтверждении корректирующего счета</span><span class="sxs-lookup"><span data-stu-id="d2456-120">Actuals created when a corrective invoice is confirmed</span></span>

<span data-ttu-id="d2456-121">В следующей таблице перечислены фактические данные, которые создаются при подтверждении корректирующего счета.</span><span class="sxs-lookup"><span data-stu-id="d2456-121">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="d2456-122">
                    <strong>Сценарий</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d2456-122">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="d2456-123">
                    <strong>Фактические данные, созданные при подтверждении</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d2456-123">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d2456-124">Выставление счета на полную сумму транзакции по ранее выставленному счету за время.</span><span class="sxs-lookup"><span data-stu-id="d2456-124">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2456-125">Сторнирование продаж с выставленным счетом по часам и сумме в сведениях исходной строки счета за время.</span><span class="sxs-lookup"><span data-stu-id="d2456-125">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2456-126">Новая фактическая сумма продаж с невыставленным счетом за часы и сумму в сведениях исходной строки счета за время.</span><span class="sxs-lookup"><span data-stu-id="d2456-126">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="d2456-127">Выставление счета на частичный кредит по транзакции за время.</span><span class="sxs-lookup"><span data-stu-id="d2456-127">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2456-128">Сторнирование продаж с выставленным счетом по часам и сумме, выставленным в сведениях исходной строки счета за время.</span><span class="sxs-lookup"><span data-stu-id="d2456-128">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2456-129">Новая фактическая сумма продаж, по которой не выставлен счет, которая оплачивается по часам и сумме в отредактированных сведениях строки счета, сторнирование этого и эквивалентная фактическая сумма продаж, по которым выставлен счет.</span><span class="sxs-lookup"><span data-stu-id="d2456-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2456-130">Новый фактический объем продаж, по которому не выставлены счета, который подлежит оплате за оставшиеся часы и сумму после вычета исправленных цифр в сведениях строки счета.</span><span class="sxs-lookup"><span data-stu-id="d2456-130">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d2456-131">Выставление счета на полную сумму транзакции по ранее выставленному счету за расходы.</span><span class="sxs-lookup"><span data-stu-id="d2456-131">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2456-132">Сторнирование продаж с выставленным счетом по количеству и сумме в сведениях исходной строки счета за расходы.</span><span class="sxs-lookup"><span data-stu-id="d2456-132">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2456-133">Новая фактическая сумма продаж, за которые не выставлены счета, по количеству и сумме в сведениях исходной строки счета за расходы.</span><span class="sxs-lookup"><span data-stu-id="d2456-133">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="d2456-134">Выставление счета на частичную сумму транзакции по ранее выставленному счету за расходы.</span><span class="sxs-lookup"><span data-stu-id="d2456-134">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2456-135">Сторнирование продаж с выставленным счетом по выставленным количеству и сумме в сведениях исходной строки счета за расходы.</span><span class="sxs-lookup"><span data-stu-id="d2456-135">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2456-136">Новая фактическая сумма продаж, по которой не выставлен счет, которая оплачивается по количестве и сумме в скорректированных сведениях строки счета, сторнирование этого и эквивалентная фактическая сумма продаж, по которым выставлен счет.</span><span class="sxs-lookup"><span data-stu-id="d2456-136">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2456-137">Новый фактический объем продаж, по которому не выставлены счета, который подлежит оплате за оставшееся количество и сумму после вычета исправленных цифр в сведениях строки счета.</span><span class="sxs-lookup"><span data-stu-id="d2456-137">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
                <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d2456-138">Выставление счета на полный кредит проводки материала с ранее выставленным счетом.</span><span class="sxs-lookup"><span data-stu-id="d2456-138">Invoicing the full credit of a previously invoiced material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2456-139">Сторнирование продаж с выставленными счетами для количества и суммы в исходных сведениях строки счета для материала.</span><span class="sxs-lookup"><span data-stu-id="d2456-139">A billed sales reversal for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2456-140">Фактические новые продажи без выставленных счетов для количества и суммы в исходных сведениях строки счета для материала.</span><span class="sxs-lookup"><span data-stu-id="d2456-140">A new unbilled sales actual for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="d2456-141">Выставление счета на частичный кредит в проводке материала.</span><span class="sxs-lookup"><span data-stu-id="d2456-141">Invoicing the partial credit on a material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2456-142">Сторнирование продаж с выставленными счетами для количества и суммы с выставленным счетом в исходных сведениях строки счета для материала.</span><span class="sxs-lookup"><span data-stu-id="d2456-142">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2456-143">Новые фактические продажи без выставленных счетов, которые подлежат оплате за количество и сумму в отредактированных сведениях строки счета, сторнирование этого и эквивалент фактических продаж, по которым выставлен счет.</span><span class="sxs-lookup"><span data-stu-id="d2456-143">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2456-144">Новый фактический объем продаж, по которому не выставлены счета, который подлежит оплате за оставшееся количество и сумму после вычета исправленных цифр в сведениях строки счета.</span><span class="sxs-lookup"><span data-stu-id="d2456-144">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d2456-145">Выставление счета на полную сумму транзакции по ранее выставленному счету за вознаграждение.</span><span class="sxs-lookup"><span data-stu-id="d2456-145">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2456-146">Сторнирование продаж с выставленным счетом по количеству и сумме в сведениях исходной строки счета за вознаграждение.</span><span class="sxs-lookup"><span data-stu-id="d2456-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2456-147">Новая фактическая сумма продаж, за которые не выставлены счета, по количеству и сумме в сведениях исходной строки счета за вознаграждение.</span><span class="sxs-lookup"><span data-stu-id="d2456-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d2456-148">Выставление счета на частичную сумму транзакции по ранее выставленному счету за вознаграждение.</span><span class="sxs-lookup"><span data-stu-id="d2456-148">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2456-149">Сторнирование продаж с выставленным счетом по количеству и выставленной сумме в сведениях исходной строки счета за вознаграждение.</span><span class="sxs-lookup"><span data-stu-id="d2456-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2456-150">Новая фактическая сумма продаж, по которой не выставлен счет, которая оплачивается по количестве и сумме в отредактированных корректирующих сведениях строки счета, сторнирование этого и эквивалентная фактическая сумма продаж, по которым выставлен счет.</span><span class="sxs-lookup"><span data-stu-id="d2456-150">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="d2456-151">Выставление счета на полную сумму транзакции по ранее выставленному счету за веху.</span><span class="sxs-lookup"><span data-stu-id="d2456-151">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2456-152">Сторнирование продаж с выставленным счетом по сумме в сведениях исходной строки счета за веху.</span><span class="sxs-lookup"><span data-stu-id="d2456-152">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="d2456-153">Статус счета вехи обновляется с <b>Счет клиента разнесен</b> на <b>Готово к выставлению счета</b>.</span><span class="sxs-lookup"><span data-stu-id="d2456-153">The invoice status of the milestone is updated from <b>Customer Invoice Posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="d2456-154">Выставление счета на частичную сумму транзакции по ранее выставленному счету за веху.</span><span class="sxs-lookup"><span data-stu-id="d2456-154">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d2456-155">Этот сценарий не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d2456-155">This scenario isn't supported.</span></span>
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
