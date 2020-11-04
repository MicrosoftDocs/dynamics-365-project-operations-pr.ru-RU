---
title: Скорректированные счета
description: В этом разделе представлена информация о скорректированных счетах.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: b31e702cc15bbb3937e8c4b305064212f63ce919
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083356"
---
# <a name="corrected-invoices"></a><span data-ttu-id="ef82c-103">Скорректированные счета</span><span class="sxs-lookup"><span data-stu-id="ef82c-103">Corrected invoices</span></span>

<span data-ttu-id="ef82c-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/без запасов_</span><span class="sxs-lookup"><span data-stu-id="ef82c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="ef82c-105">Утвержденные счета можно редактировать.</span><span class="sxs-lookup"><span data-stu-id="ef82c-105">Confirmed invoices can be edited.</span></span> <span data-ttu-id="ef82c-106">При редактировании утвержденного счета создается черновик скорректированного счета.</span><span class="sxs-lookup"><span data-stu-id="ef82c-106">When you edit a confirmed invoice, a draft of the corrected invoice is created.</span></span> <span data-ttu-id="ef82c-107">Поскольку предполагается, что требуется реверсировать все транзакции и количества из первоначального счетов, этот скорректированный счет включает все транзакции из первоначального счета, и все количества в нем равны нулю (0).</span><span class="sxs-lookup"><span data-stu-id="ef82c-107">Because the assumption is that you want to reverse all the transactions and quantities from the original invoice, the corrected invoice includes all the transactions from the original invoice, and all the quantities on it are zero (0).</span></span>

<span data-ttu-id="ef82c-108">Когда какие-либо транзакции не требуют исправления, можно удалить их из черновика корректирующего счета.</span><span class="sxs-lookup"><span data-stu-id="ef82c-108">When transactions don't require correction, you can remove them from the draft corrective invoice.</span></span> <span data-ttu-id="ef82c-109">Чтобы реверсировать или вернуть только часть количества, можно изменить поле "Количество" в сведениях строки.</span><span class="sxs-lookup"><span data-stu-id="ef82c-109">To reverse or return only a partial quantity, you can edit the Quantity field on the line detail.</span></span> <span data-ttu-id="ef82c-110">Если открыть сведения строки счета, можно просмотреть первоначальное количество по счету.</span><span class="sxs-lookup"><span data-stu-id="ef82c-110">If you open the invoice line detail, you can see the original invoice quantity.</span></span> <span data-ttu-id="ef82c-111">Затем можно изменить текущее количество по счету, чтобы оно было меньше или больше количества по первоначальному счету.</span><span class="sxs-lookup"><span data-stu-id="ef82c-111">You can then edit the current invoice quantity so that it's less than or more than the original invoice quantity.</span></span>

<span data-ttu-id="ef82c-112">При утверждении корректирующего счета фактические значения исходных выставленных продаж реверсируется, и создаются новые фактические данные продаж, за которые выставлен счет.</span><span class="sxs-lookup"><span data-stu-id="ef82c-112">When you confirm a corrective invoice, the original billed sales actual is reversed, and a new billed sales actual is created.</span></span> <span data-ttu-id="ef82c-113">Если количество было уменьшено, разница вызовет также создание новых фактических данных продаж, за которые не выставлен счет.</span><span class="sxs-lookup"><span data-stu-id="ef82c-113">If the quantity was reduced, the difference will cause a new unbilled sales actual to be created too.</span></span> <span data-ttu-id="ef82c-114">Например, если исходный выставленный счет продажи был за восемь часов, а в сведениях по строке скорректированного счета количество уменьшено до шести часов, исходная строка счета продаж обращается и создаются два новых фактических значения:</span><span class="sxs-lookup"><span data-stu-id="ef82c-114">For example, if the original billed sale was for eight hours, and the corrected invoice line detail has a reduced quantity of six hours, the original billed sales line is revered and two new actuals are created:</span></span>

- <span data-ttu-id="ef82c-115">Фактические данные выставленного счета продаж на 6 часов.</span><span class="sxs-lookup"><span data-stu-id="ef82c-115">A billed sales actual for six hours.</span></span>
- <span data-ttu-id="ef82c-116">Фактические данные продаж на остальные 2 часа, за которые счет не выставлен.</span><span class="sxs-lookup"><span data-stu-id="ef82c-116">An unbilled sales actual for the remaining two hours.</span></span> <span data-ttu-id="ef82c-117">За эту транзакцию можно выставить счет позднее или ее можно пометить как не подлежащую оплате, в зависимости от переговоров с клиентом.</span><span class="sxs-lookup"><span data-stu-id="ef82c-117">This transaction can either be billed later or marked as non-chargeable, depending on the negotiations with the customer.</span></span>
