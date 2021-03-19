---
title: Отключайте измерение цен
description: В этом разделе показана настройка измерения цены в решении Project Service.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 6e4b80b9c4b1b0f57d04079c9d2f84051b451d29
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281854"
---
# <a name="turn-off-a-pricing-dimension"></a><span data-ttu-id="b7040-103">Отключайте измерение цен</span><span class="sxs-lookup"><span data-stu-id="b7040-103">Turn off a pricing dimension</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="b7040-104">Возможно, вам придется пересматривать и обновлять свою стратегию ценообразования каждые несколько лет.</span><span class="sxs-lookup"><span data-stu-id="b7040-104">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="b7040-105">Для любых обновлений, которые вы делаете, может потребоваться отключить существующее измерение цен и создать новое.</span><span class="sxs-lookup"><span data-stu-id="b7040-105">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="b7040-106">Например, ранее можно было оценить по **Роли**, но сейчас вы решили оценивать по **Опыт работы**.</span><span class="sxs-lookup"><span data-stu-id="b7040-106">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="b7040-107">Для этого может потребоваться отключить **Роль** в качестве измерения цены и создать **Опыт работы** в качестве нового измерения цены.</span><span class="sxs-lookup"><span data-stu-id="b7040-107">This may require you to turn off **Role** as a pricing dimension and create **Work Expereince** as a new pricing dimension.</span></span> 

<span data-ttu-id="b7040-108">Отключить измерение цены, независимо от того, является ли оно готовым или нестандартным, можно сделать, установив для полей **Применимо к стоимости** и **Применимо к продажам** Измерения цен на **Нет**.</span><span class="sxs-lookup"><span data-stu-id="b7040-108">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="b7040-109">Однако, когда вы сделаете это, вы можете получить следующее сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="b7040-109">However, when you do this, you might receive the following error message.</span></span>

![Ошибка бизнес-процесса при отключении измерения цены](media/Business-Process-Error.png)


<span data-ttu-id="b7040-111">Это сообщение об ошибке указывает на то, что существуют записи цен, которые ранее были настроены для отключаемого измерения.</span><span class="sxs-lookup"><span data-stu-id="b7040-111">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="b7040-112">Все записи **Цена роли** и **Наценка цены роли**, относящиеся к измерению, должны быть удалены, прежде чем применимость измерения можно будет установить на **Нет**.</span><span class="sxs-lookup"><span data-stu-id="b7040-112">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="b7040-113">Это правило применяется как к готовым измерениям цен, так и к любым настраиваемым измерениям, которые вы могли создать.</span><span class="sxs-lookup"><span data-stu-id="b7040-113">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="b7040-114">Причина такой проверки заключается в том, что Project Service имеет ограничение, заключающееся в том, что каждая запись **Цена роли** должна иметь уникальную комбинацию измерений.</span><span class="sxs-lookup"><span data-stu-id="b7040-114">The reason for this validation is because Project Service has a constraint that each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="b7040-115">Например, в прайс-листе под названием **Нормы затрат США 2018 год** будет следующие строки **Цена роли**.</span><span class="sxs-lookup"><span data-stu-id="b7040-115">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="b7040-116">Стандартный заголовок</span><span class="sxs-lookup"><span data-stu-id="b7040-116">Standard Title</span></span>         | <span data-ttu-id="b7040-117">Подразделение</span><span class="sxs-lookup"><span data-stu-id="b7040-117">Org Unit</span></span>    |<span data-ttu-id="b7040-118">Единица измерения</span><span class="sxs-lookup"><span data-stu-id="b7040-118">Unit</span></span>   |<span data-ttu-id="b7040-119">Цена</span><span class="sxs-lookup"><span data-stu-id="b7040-119">Price</span></span>  |<span data-ttu-id="b7040-120">Валюта</span><span class="sxs-lookup"><span data-stu-id="b7040-120">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="b7040-121">Системный инженер</span><span class="sxs-lookup"><span data-stu-id="b7040-121">Systems Engineer</span></span>|<span data-ttu-id="b7040-122">Contoso US</span><span class="sxs-lookup"><span data-stu-id="b7040-122">Contoso US</span></span>|<span data-ttu-id="b7040-123">Hour</span><span class="sxs-lookup"><span data-stu-id="b7040-123">Hour</span></span>| <span data-ttu-id="b7040-124">100</span><span class="sxs-lookup"><span data-stu-id="b7040-124">100</span></span>|<span data-ttu-id="b7040-125">Доллар США</span><span class="sxs-lookup"><span data-stu-id="b7040-125">USD</span></span>|
| <span data-ttu-id="b7040-126">Старший системный инженер</span><span class="sxs-lookup"><span data-stu-id="b7040-126">Senior Systems Engineer</span></span>|<span data-ttu-id="b7040-127">Contoso US</span><span class="sxs-lookup"><span data-stu-id="b7040-127">Contoso US</span></span>|<span data-ttu-id="b7040-128">Hour</span><span class="sxs-lookup"><span data-stu-id="b7040-128">Hour</span></span>| <span data-ttu-id="b7040-129">150</span><span class="sxs-lookup"><span data-stu-id="b7040-129">150</span></span>| <span data-ttu-id="b7040-130">Доллар США</span><span class="sxs-lookup"><span data-stu-id="b7040-130">USD</span></span>|


<span data-ttu-id="b7040-131">Когда вы отключите **Стандартный заголовок** в качестве измерения цены, и механизм ценообразования Project Service выполнит поиск цены, он будет использовать только значение **Подразделение** из контекста ввода.</span><span class="sxs-lookup"><span data-stu-id="b7040-131">When you turn off **Standard Title** as the pricing dimension, and the Project Service pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="b7040-132">Если **Подразделением** контекста ввода является "Contoso US", результат будет недетерминированным, потому что обе строки будут совпадать.</span><span class="sxs-lookup"><span data-stu-id="b7040-132">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="b7040-133">Во избежание этого сценария, при создании записи **Цена роли**, Project Service утверждает что комбинация измерений является уникальной.</span><span class="sxs-lookup"><span data-stu-id="b7040-133">To avoid this scenario, when you create **Role Price** records, Project Service validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="b7040-134">Если измерение отключено после создания записей **Цена роли**, это ограничение может быть нарушено.</span><span class="sxs-lookup"><span data-stu-id="b7040-134">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="b7040-135">Следовательно, перед тем, как отключить измерение, необходимо удалить все строки **Цена роли** и **Наценка цены роли**,в которых заполнено это значение измерения.</span><span class="sxs-lookup"><span data-stu-id="b7040-135">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]