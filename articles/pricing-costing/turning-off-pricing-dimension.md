---
title: Отключение измерения цен
description: В этом разделе представлена информация о том, как отключить измерения цен.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 986fae72c6b44b3f76281aefb81ffdaa96f71ae7
ms.sourcegitcommit: 13a4e58eddbb0f81aca07c1ff452c420dbd8a68f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/30/2020
ms.locfileid: "4650065"
---
# <a name="turning-off-a-pricing-dimension"></a><span data-ttu-id="683a0-103">Отключение измерения цен</span><span class="sxs-lookup"><span data-stu-id="683a0-103">Turning off a pricing dimension</span></span>

<span data-ttu-id="683a0-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="683a0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="683a0-105">Возможно, вам придется пересматривать и обновлять свою стратегию ценообразования каждые несколько лет.</span><span class="sxs-lookup"><span data-stu-id="683a0-105">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="683a0-106">Для любых обновлений, которые вы делаете, может потребоваться отключить существующее измерение цен и создать новое.</span><span class="sxs-lookup"><span data-stu-id="683a0-106">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="683a0-107">Например, ранее можно было оценить по **Роли**, но сейчас вы решили оценивать по **Опыт работы**.</span><span class="sxs-lookup"><span data-stu-id="683a0-107">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="683a0-108">Для этого может потребоваться отключить **Роль** в качестве измерения цены и создать **Опыт работы** в качестве нового измерения цены.</span><span class="sxs-lookup"><span data-stu-id="683a0-108">This may require you to turn off **Role** as a pricing dimension and create **Work Experience** as a new pricing dimension.</span></span> 

<span data-ttu-id="683a0-109">Отключить измерение цены, независимо от того, является ли оно готовым или нестандартным, можно сделать, установив для полей **Применимо к стоимости** и **Применимо к продажам** Измерения цен на **Нет**.</span><span class="sxs-lookup"><span data-stu-id="683a0-109">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="683a0-110">Однако, когда вы это сделаете, вы можете получить сообщение об ошибке **Измерение ценообразования нельзя обновить или удалить, если есть связанные записи о ценах**.</span><span class="sxs-lookup"><span data-stu-id="683a0-110">However, when you do this, you might receive the error message, **Pricing dimension cannot be updated or deleted if there are associated price records.**</span></span>

![Ошибка бизнес-процесса при отключении измерения цены](media/Business-Process-Error.png)

<span data-ttu-id="683a0-112">Это сообщение об ошибке указывает на то, что существуют записи цен, которые ранее были настроены для отключаемого измерения.</span><span class="sxs-lookup"><span data-stu-id="683a0-112">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="683a0-113">Все записи **Цена роли** и **Наценка цены роли**, относящиеся к измерению, должны быть удалены, прежде чем применимость измерения можно будет установить на **Нет**.</span><span class="sxs-lookup"><span data-stu-id="683a0-113">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="683a0-114">Это правило применяется как к готовым измерениям цен, так и к любым настраиваемым измерениям, которые вы могли создать.</span><span class="sxs-lookup"><span data-stu-id="683a0-114">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="683a0-115">Причина такой проверки заключается в том, что каждая запись **Цена роли** должна иметь уникальную комбинацию измерений.</span><span class="sxs-lookup"><span data-stu-id="683a0-115">The reason for this validation is because each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="683a0-116">Например, в прайс-листе под названием **Нормы затрат США 2018 год** будет следующие строки **Цена роли**.</span><span class="sxs-lookup"><span data-stu-id="683a0-116">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="683a0-117">Стандартный заголовок</span><span class="sxs-lookup"><span data-stu-id="683a0-117">Standard Title</span></span>         | <span data-ttu-id="683a0-118">Подразделение</span><span class="sxs-lookup"><span data-stu-id="683a0-118">Org Unit</span></span>    |<span data-ttu-id="683a0-119">Единица измерения</span><span class="sxs-lookup"><span data-stu-id="683a0-119">Unit</span></span>   |<span data-ttu-id="683a0-120">Цена</span><span class="sxs-lookup"><span data-stu-id="683a0-120">Price</span></span>  |<span data-ttu-id="683a0-121">Валюта</span><span class="sxs-lookup"><span data-stu-id="683a0-121">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="683a0-122">Системный инженер</span><span class="sxs-lookup"><span data-stu-id="683a0-122">Systems Engineer</span></span>|<span data-ttu-id="683a0-123">Contoso US</span><span class="sxs-lookup"><span data-stu-id="683a0-123">Contoso US</span></span>|<span data-ttu-id="683a0-124">Hour</span><span class="sxs-lookup"><span data-stu-id="683a0-124">Hour</span></span>| <span data-ttu-id="683a0-125">100</span><span class="sxs-lookup"><span data-stu-id="683a0-125">100</span></span>|<span data-ttu-id="683a0-126">Доллар США</span><span class="sxs-lookup"><span data-stu-id="683a0-126">USD</span></span>|
| <span data-ttu-id="683a0-127">Старший системный инженер</span><span class="sxs-lookup"><span data-stu-id="683a0-127">Senior Systems Engineer</span></span>|<span data-ttu-id="683a0-128">Contoso US</span><span class="sxs-lookup"><span data-stu-id="683a0-128">Contoso US</span></span>|<span data-ttu-id="683a0-129">Hour</span><span class="sxs-lookup"><span data-stu-id="683a0-129">Hour</span></span>| <span data-ttu-id="683a0-130">150</span><span class="sxs-lookup"><span data-stu-id="683a0-130">150</span></span>| <span data-ttu-id="683a0-131">Доллар США</span><span class="sxs-lookup"><span data-stu-id="683a0-131">USD</span></span>|


<span data-ttu-id="683a0-132">Когда вы отключите **Стандартный заголовок** в качестве измерения цены, и механизм ценообразования выполнит поиск цены, он будет использовать только значение **Подразделение** из контекста ввода.</span><span class="sxs-lookup"><span data-stu-id="683a0-132">When you turn off **Standard Title** as the pricing dimension, and the pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="683a0-133">Если **Подразделением** контекста ввода является "Contoso US", результат будет недетерминированным, потому что обе строки будут совпадать.</span><span class="sxs-lookup"><span data-stu-id="683a0-133">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="683a0-134">Во избежание этого сценария, при создании записи **Цена роли**, система проверяет, что комбинация измерений является уникальной.</span><span class="sxs-lookup"><span data-stu-id="683a0-134">To avoid this scenario, when you create **Role Price** records, the system validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="683a0-135">Если измерение отключено после создания записей **Цена роли**, это ограничение может быть нарушено.</span><span class="sxs-lookup"><span data-stu-id="683a0-135">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="683a0-136">Следовательно, перед тем, как отключить измерение, необходимо удалить все строки **Цена роли** и **Наценка цены роли**,в которых заполнено это значение измерения.</span><span class="sxs-lookup"><span data-stu-id="683a0-136">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>
