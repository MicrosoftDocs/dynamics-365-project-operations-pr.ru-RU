---
title: Подтверждение счета-проформы
description: Этой теме предоставляется информация о подтверждении счета-проформы.
author: rumant
manager: AnnBe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fa1e6c17fbda76a283c2ec68760a00e846decf83
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128119"
---
# <a name="confirm-a-proforma-invoice"></a><span data-ttu-id="2d648-103">Подтверждение счета-проформы</span><span class="sxs-lookup"><span data-stu-id="2d648-103">Confirm a proforma invoice</span></span>

<span data-ttu-id="2d648-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/без запасов_</span><span class="sxs-lookup"><span data-stu-id="2d648-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="2d648-105">После подтверждения счета-проформы статус счета по проекту изменяется на **Подтверждено**.</span><span class="sxs-lookup"><span data-stu-id="2d648-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="2d648-106">Когда счет подтвержден, он становится доступным только для чтения.</span><span class="sxs-lookup"><span data-stu-id="2d648-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="2d648-107">В дальнейшем счет можно будет исправить только в том случае, если есть какие-либо исправления или кредиты, инициированные клиентом, или если он отмечен как оплаченный.</span><span class="sxs-lookup"><span data-stu-id="2d648-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, or when it's marked as paid.</span></span>

<span data-ttu-id="2d648-108">В следующей таблице перечислены фактические данные, созданные системой.</span><span class="sxs-lookup"><span data-stu-id="2d648-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="2d648-109">Эти фактические данные создаются при выполнении определенных операций с черновиком счета по проекту до его подтверждения.</span><span class="sxs-lookup"><span data-stu-id="2d648-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="416" valign="top">
                <p><span data-ttu-id="2d648-110">
                    <strong>Сценарий</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2d648-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="608" valign="top">
                <p><span data-ttu-id="2d648-111">
                    <strong>Фактические данные, созданные при подтверждении</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2d648-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2d648-112">Выставление счета по транзакции за время без каких-либо изменений в черновике счета.</span><span class="sxs-lookup"><span data-stu-id="2d648-112">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d648-113">Сторнирование продаж с невыставленным счетом по часам и сумме в исходном утвержденном времени.</span><span class="sxs-lookup"><span data-stu-id="2d648-113">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d648-114">Фактические данные продаж с выставленным счетом по часам и сумме в исходном утвержденном времени.</span><span class="sxs-lookup"><span data-stu-id="2d648-114">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="2d648-115">Выставление счета по транзакции по времени, которая была отредактирована для уменьшения количества.</span><span class="sxs-lookup"><span data-stu-id="2d648-115">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d648-116">Сторнирование продаж с невыставленным счетом по часам и сумме в исходном утвержденном времени.</span><span class="sxs-lookup"><span data-stu-id="2d648-116">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d648-117">Новая фактическая сумма продаж, по которой не выставлен счет, которая оплачивается по часам и сумме в отредактированных сведениях строки счета, сторнирование фактических данных продаж, по которым не выставлены счета, и эквивалентная фактическая сумма продаж, по которым выставлен счет.</span><span class="sxs-lookup"><span data-stu-id="2d648-117">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d648-118">Новая фактическая сумма продаж, по которой не выставлен счет, которая не оплачивается по оставшимся часам и сумме после вычитания исправленных цифр в отредактированных сведениях строки счета, сторнирование фактических данных продаж, по которым не выставлены счета, и эквивалентная фактическая сумма продаж, по которым выставлен счет.</span><span class="sxs-lookup"><span data-stu-id="2d648-118">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2d648-119">Выставление счета по транзакции по времени, которая была отредактирована для увеличения количества.</span><span class="sxs-lookup"><span data-stu-id="2d648-119">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d648-120">Сторнирование продаж с невыставленным счетом по часам и сумме в исходном утвержденном времени.</span><span class="sxs-lookup"><span data-stu-id="2d648-120">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d648-121">Новая фактическая сумма продаж, по которой не выставлен счет, которая оплачивается по часам и сумме в отредактированных сведениях строки счета, сторнирование фактических данных продаж, по которым не выставлены счета, и эквивалентная фактическая сумма продаж, по которым выставлен счет.</span><span class="sxs-lookup"><span data-stu-id="2d648-121">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2d648-122">Выставление счета по транзакции за расходы без каких-либо изменений в черновике счета.</span><span class="sxs-lookup"><span data-stu-id="2d648-122">Invoicing an expense transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d648-123">Сторнирование продаж с невыставленным счетом по количеству и сумме в исходных утвержденных расходах.</span><span class="sxs-lookup"><span data-stu-id="2d648-123">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d648-124">Фактические данные продаж с выставленным счетом по количеству и сумме в исходных утвержденных расходах.</span><span class="sxs-lookup"><span data-stu-id="2d648-124">A billed sales actual for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="2d648-125">Выставление счета по транзакции по расходам, которая была отредактирована для уменьшения количества.</span><span class="sxs-lookup"><span data-stu-id="2d648-125">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d648-126">Сторнирование продаж с невыставленным счетом по количеству и сумме в исходных утвержденных расходах.</span><span class="sxs-lookup"><span data-stu-id="2d648-126">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d648-127">Новая фактическая сумма продаж, по которой не выставлен счет, которая оплачивается по количеству и сумме в отредактированных сведениях строки счета, сторнирование фактических данных продаж, по которым не выставлены счета, и эквивалентная фактическая сумма продаж, по которым выставлен счет.</span><span class="sxs-lookup"><span data-stu-id="2d648-127">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d648-128">Новая фактическая сумма продаж, по которой не выставлен счет, которая не оплачивается по оставшемуся количеству и сумме после вычитания исправленных цифр в отредактированных сведениях строки счета, сторнирование фактических данных продаж, по которым не выставлены счета, и эквивалент фактической суммы продаж, по которым выставлен счет.</span><span class="sxs-lookup"><span data-stu-id="2d648-128">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent of the billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2d648-129">Выставление счета по транзакции по расходам, которая была отредактирована для увеличения количества.</span><span class="sxs-lookup"><span data-stu-id="2d648-129">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d648-130">Сторнирование продаж с невыставленным счетом по количеству и сумме в исходных утвержденных расходах.</span><span class="sxs-lookup"><span data-stu-id="2d648-130">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d648-131">Новая фактическая сумма продаж, по которой не выставлен счет, которая оплачивается по количеству и сумме в отредактированных сведениях строки счета, сторнирование фактических данных продаж, по которым не выставлены счета, и эквивалентная фактическая сумма продаж, по которым выставлен счет.</span><span class="sxs-lookup"><span data-stu-id="2d648-131">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the untilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2d648-132">Выставление вознаграждения.</span><span class="sxs-lookup"><span data-stu-id="2d648-132">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d648-133">Сторнирование продаж с невыставленным счетом по сумме вознаграждения в исходной строке журнала.</span><span class="sxs-lookup"><span data-stu-id="2d648-133">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d648-134">Фактические данные продаж с выставленным счетом по количеству и сумме в исходной строке журнала вознаграждения.</span><span class="sxs-lookup"><span data-stu-id="2d648-134">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="2d648-135">Выставление счета за веху.</span><span class="sxs-lookup"><span data-stu-id="2d648-135">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d648-136">Фактические данные продаж с выставленным счетом по сумме вехи в исходной вехе в строке контракта по проекту.</span><span class="sxs-lookup"><span data-stu-id="2d648-136">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>
