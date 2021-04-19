---
title: Прайс-листы продуктов
description: Эта тема предоставляет информацию о прайс-листах в ценах каталога, используемых для предложений с расценками и контрактов по проектам.
author: rumant
manager: AnnBe
ms.date: 04/05/2021
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
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e37f0bf9eef946ab4ebd658cef4e1269cbaf686d
ms.sourcegitcommit: ac90be6106592f883a0de39a75836fb40255d65a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2021
ms.locfileid: "5877506"
---
# <a name="product-price-lists"></a><span data-ttu-id="7c56d-103">Прайс-листы продуктов</span><span class="sxs-lookup"><span data-stu-id="7c56d-103">Product price lists</span></span>

<span data-ttu-id="7c56d-104">_**Относится к:** развертывание Lite — от сделки до счетов-проформ_</span><span class="sxs-lookup"><span data-stu-id="7c56d-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

 <span data-ttu-id="7c56d-105">В Project Operations **Прайс-листы продуктов** и связанные сущности позиций прайс-листа поддерживают функциональность для ценообразования продуктов на основе строк предложений с расценками и строк контракта.</span><span class="sxs-lookup"><span data-stu-id="7c56d-105">In Project Operations, **Product price lists** and related price list item entities support functionality for pricing products on product-based quote and contract lines.</span></span> <span data-ttu-id="7c56d-106">Для продуктов, используемых в проектах, используются записи позиций прайс-листа для прайс-листов проекта.</span><span class="sxs-lookup"><span data-stu-id="7c56d-106">For products used on projects, the price list item records for project price lists are used.</span></span> 

<span data-ttu-id="7c56d-107">Продукты должны быть настроены таким образом, чтобы они имели стоимость и прайс-листы по умолчанию в каталоге продуктов.</span><span class="sxs-lookup"><span data-stu-id="7c56d-107">Products should be set up so that they have default cost and price lists in the product catalog.</span></span> <span data-ttu-id="7c56d-108">Используйте прайс-лист, стандартную себестоимость и текущую стоимость, чтобы настроить стоимость и прайс-листы по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7c56d-108">Use the list price, standard cost, and current cost to configure default cost and list prices.</span></span> <span data-ttu-id="7c56d-109">Цены прайс-листов по умолчанию используются в строке предложения с расценками или строке контракта по проекту только тогда, когда система не может найти строку прайс-листа для этого продукта в прайс-листе продукт для предложения с расценками и контракта по проекту.</span><span class="sxs-lookup"><span data-stu-id="7c56d-109">The default list prices are used on a quote line or a project contract line only when the system can't find a price list line for that product in the product price list for the quote or project contract.</span></span>

<span data-ttu-id="7c56d-110">Себестоимость строк каталога продукции может быть изменена между предложениями с расценками.</span><span class="sxs-lookup"><span data-stu-id="7c56d-110">The cost price of product catalog lines can be changed between quotes.</span></span> <span data-ttu-id="7c56d-111">Эта возможность важна, поскольку если пользователь не будет точно отслеживать затраты, то будет невозможно определить операционную прибыль по взаимодействиям проекта.</span><span class="sxs-lookup"><span data-stu-id="7c56d-111">This capability is important, because if you don't accurately track costs, you can't determine operational profits on project engagements.</span></span> <span data-ttu-id="7c56d-112">По умолчанию стандартная себестоимость продукта используется как себестоимость.</span><span class="sxs-lookup"><span data-stu-id="7c56d-112">By default, the standard cost of the product is used as the cost price.</span></span> <span data-ttu-id="7c56d-113">Однако себестоимость по умолчанию можно обновить в строке предложения с расценками, если себестоимость для этого предложения с расценками отличается.</span><span class="sxs-lookup"><span data-stu-id="7c56d-113">However, the default cost price can be updated on the quote line if there's a different cost price for that quote.</span></span>

## <a name="price-list-items"></a><span data-ttu-id="7c56d-114">Элементы прайс-листа</span><span class="sxs-lookup"><span data-stu-id="7c56d-114">Price list items</span></span>

<span data-ttu-id="7c56d-115">Продукты можно добавлять из каталога продукции в различные прайс-листы.</span><span class="sxs-lookup"><span data-stu-id="7c56d-115">You can add products from a product catalog to different price lists.</span></span> <span data-ttu-id="7c56d-116">Строки прайс-листа для продуктов всегда ссылают на конкретную единицу измерения.</span><span class="sxs-lookup"><span data-stu-id="7c56d-116">Price list lines for products always reference a specific unit.</span></span> <span data-ttu-id="7c56d-117">Цены для продукта в позициях прайс-листа можно задать как сумму в валюте.</span><span class="sxs-lookup"><span data-stu-id="7c56d-117">Pricing for a product on price list items can be configured as a currency amount.</span></span> <span data-ttu-id="7c56d-118">В качестве альтернативы их можно настроить как функции прейскурантной цены, текущей стоимости или стандартной стоимости.</span><span class="sxs-lookup"><span data-stu-id="7c56d-118">Alternatively, it can be configured as a function of the list price, current cost, or standard cost.</span></span>

<span data-ttu-id="7c56d-119">Функции цен поддерживает различные параметры округления при настройке цены продуктов в качестве функции прейскурантной цены, стандартной стоимости или текущей стоимости.</span><span class="sxs-lookup"><span data-stu-id="7c56d-119">Pricing functionality supports various rounding options when product prices are configured as a function of the list price, standard cost, or current cost.</span></span> <span data-ttu-id="7c56d-120">Помимо использования нескольких способов ценообразования и параметров округления, можно связать списки скидок с позициями прайс-листа.</span><span class="sxs-lookup"><span data-stu-id="7c56d-120">In addition to taking advantage of multiple pricing methods and rounding options, you can associate discount lists with price list items.</span></span> 

 
## <a name="default-product-price-list"></a><span data-ttu-id="7c56d-121">Прайс-лист продукта по умолчанию</span><span class="sxs-lookup"><span data-stu-id="7c56d-121">Default product price list</span></span>
<span data-ttu-id="7c56d-122">Каждая запись клиента имеет поле **Прайс-лист по умолчанию**, где можно задать прайс-лист, соответствующий валюте клиента.</span><span class="sxs-lookup"><span data-stu-id="7c56d-122">Each customer record has a **Default Price List** field, where you can specify a price list that matches the currency of the customer.</span></span> <span data-ttu-id="7c56d-123">Значение по умолчанию не вводится автоматически в это поле.</span><span class="sxs-lookup"><span data-stu-id="7c56d-123">A default value isn't automatically entered in this field.</span></span> <span data-ttu-id="7c56d-124">Если имеется настраиваемое соглашение о ценах с конкретным клиентом, можно использовать это поле, чтобы связать прайс-лист с этим клиентом.</span><span class="sxs-lookup"><span data-stu-id="7c56d-124">When a custom pricing agreement with a specific customer exists, you can use this field to associate a price list with that customer.</span></span>

<span data-ttu-id="7c56d-125">Сущности возможной сделки, предложения с расценками и контракта по проекту используют следующий порядок для ввода прайс-листов продукта по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7c56d-125">The Opportunity, Quote, and Project Contract entities use the following order to enter default product price lists.</span></span> <span data-ttu-id="7c56d-126">Этот же порядок используется для прайс-листов проекта.</span><span class="sxs-lookup"><span data-stu-id="7c56d-126">The same order is used for project price lists.</span></span>

1.  <span data-ttu-id="7c56d-127">Предложение с расценками</span><span class="sxs-lookup"><span data-stu-id="7c56d-127">Quote</span></span>
2.  <span data-ttu-id="7c56d-128">Возможная сделка</span><span class="sxs-lookup"><span data-stu-id="7c56d-128">Opportunity</span></span>
3.  <span data-ttu-id="7c56d-129">Клиент</span><span class="sxs-lookup"><span data-stu-id="7c56d-129">Customer</span></span>
4.  <span data-ttu-id="7c56d-130">Глобальные параметры</span><span class="sxs-lookup"><span data-stu-id="7c56d-130">Global settings</span></span> 

<span data-ttu-id="7c56d-131">По умолчанию в поле **Продукт** в строке предложения с расценками перечислены все активные продукты в прайс-лист продуктов в предложении с расценками.</span><span class="sxs-lookup"><span data-stu-id="7c56d-131">By default, the **Product** field on the quote line lists all the active products in the product price list of the quote.</span></span> <span data-ttu-id="7c56d-132">Если продукт был деактивирован или это черновик продукта, он не указывается, даже если он есть в прайс-листе.</span><span class="sxs-lookup"><span data-stu-id="7c56d-132">If a product has been inactivated, or if it's a draft product, it isn't listed, even if it's in the price list.</span></span> 

<span data-ttu-id="7c56d-133">Строки каталога продуктов добавляются как строки счета в первом счете, создаваемым для контракта по проекту.</span><span class="sxs-lookup"><span data-stu-id="7c56d-133">Product catalog lines are added as invoice lines on the first invoice that is created for a project contract.</span></span> <span data-ttu-id="7c56d-134">В черновике счета эта строки счета можно удалить.</span><span class="sxs-lookup"><span data-stu-id="7c56d-134">On a draft invoice, those invoice lines can be deleted.</span></span> <span data-ttu-id="7c56d-135">В этом случае строки будут отображаться в последующем счете, пока по ним не будет выставлен счет или пока счет не будет отправлен клиенту.</span><span class="sxs-lookup"><span data-stu-id="7c56d-135">In that case, the lines will appear on a subsequent invoice until they are invoiced, or until the invoice is sent to the customer.</span></span> <span data-ttu-id="7c56d-136">Невозможно выставить частичное количество по строке счета за продукт.</span><span class="sxs-lookup"><span data-stu-id="7c56d-136">You can't invoice a partial quantity of a product invoice line.</span></span> <span data-ttu-id="7c56d-137">При выставлении счета за строки продуктов из контракта по проекту создаются фактические показатели.</span><span class="sxs-lookup"><span data-stu-id="7c56d-137">When the product lines from the project contract are invoiced, actuals are created.</span></span> <span data-ttu-id="7c56d-138">Однако эти фактические данные не связаны со связанной сущностью проекта.</span><span class="sxs-lookup"><span data-stu-id="7c56d-138">However, those actuals aren't linked to the related project entity.</span></span> <span data-ttu-id="7c56d-139">Другими словами, строки контракта по проекту на основе продукта не зависят от любого использования на основе проекта.</span><span class="sxs-lookup"><span data-stu-id="7c56d-139">In other words, product-based project contract lines are independent of any project-based use.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
