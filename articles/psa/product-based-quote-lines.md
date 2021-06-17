---
title: Строки предложения с расценками на основе продуктов
description: В этом разделе представлена информация о строках предложения с расценками на основе продуктов.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 1bd789f4ee4d5b4603093be24aa25addafa9e8e8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998517"
---
# <a name="product-based-quote-lines"></a><span data-ttu-id="0f280-103">Строки предложения с расценками на основе продуктов</span><span class="sxs-lookup"><span data-stu-id="0f280-103">Product-based quote lines</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


<span data-ttu-id="0f280-104">Можно создать строки предложения с расценками на основе продукта в Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="0f280-104">You can create product-based quote lines in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="0f280-105">Строки предложения с расценками на основе продукта могут быть "вписанными" строками или они могут быть номенклатурами из каталога продуктов.</span><span class="sxs-lookup"><span data-stu-id="0f280-105">Product-based quote lines can be "write-in" lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="0f280-106">Каталог продукции</span><span class="sxs-lookup"><span data-stu-id="0f280-106">Product catalog</span></span>

<span data-ttu-id="0f280-107">Продуктов в каталоге продукции Dynamics 365 имеют единицу измерения и группу единиц измерения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0f280-107">The products in a Dynamics 365 product catalog have a default unit and unit group.</span></span> <span data-ttu-id="0f280-108">Если несколько продуктов имеют один и тот же набор атрибутов, можно создать семейство продуктов, которое также имеет эти атрибуты.</span><span class="sxs-lookup"><span data-stu-id="0f280-108">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="0f280-109">Все продукты виз одного семейства продуктов наследуют одинаковый набор атрибутов.</span><span class="sxs-lookup"><span data-stu-id="0f280-109">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="0f280-110">Например, компания продает лицензии на подписку на различное программное обеспечение.</span><span class="sxs-lookup"><span data-stu-id="0f280-110">For example, a company sells subscription licenses for a variety of software.</span></span> <span data-ttu-id="0f280-111">Все программное обеспечение по подписке имеет два следующих атрибута:</span><span class="sxs-lookup"><span data-stu-id="0f280-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="0f280-112">Число пользователей</span><span class="sxs-lookup"><span data-stu-id="0f280-112">Number of users</span></span> 
- <span data-ttu-id="0f280-113">Длительность подписки (в месяцах)</span><span class="sxs-lookup"><span data-stu-id="0f280-113">Subscription duration (in months)</span></span>

<span data-ttu-id="0f280-114">Удобный способ ведения каталога такого типа — создать семейство продуктов с названием **Программное обеспечение по подписке**, которое имеет атрибуты **Число пользователей** и **Длительности подписки**.</span><span class="sxs-lookup"><span data-stu-id="0f280-114">A good way to maintain this type of catalog is to create a product family that is named **Subscription Software**, and that has **Number of users** and **Subscription duration** as attributes.</span></span> <span data-ttu-id="0f280-115">Затем можно добавить отдельные продукты, такие как **Dynamics 365 Sales** или **Dynamics 365 Field Service** в семейство продуктов **Программное обеспечение по подписке**.</span><span class="sxs-lookup"><span data-stu-id="0f280-115">You can then add individual products, such as **Dynamics 365 Sales** or **Dynamics 365 Field Service** to the **Subscription Software** product family.</span></span>

## <a name="adding-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="0f280-116">Добавление номенклатур каталога продуктов в предложение с расценками по проекту</span><span class="sxs-lookup"><span data-stu-id="0f280-116">Adding product catalog items to a project quote</span></span>

<span data-ttu-id="0f280-117">На страницах предложения с расценками по проекту и контракта по проекту содержатся разделы для двух типов строк: строки на основе проекта и строки на основе продукта.</span><span class="sxs-lookup"><span data-stu-id="0f280-117">Project quote and project contract pages have sections for two types of lines: project-based lines and product-based lines.</span></span> <span data-ttu-id="0f280-118">Для строк на основе продукта Dynamics 365 используется для добавления номенклатур из каталога продуктов в предложение с расценками.</span><span class="sxs-lookup"><span data-stu-id="0f280-118">For product-based lines, Dynamics 365 is used to add items from a product catalog to a quote.</span></span> <span data-ttu-id="0f280-119">Раскрывающийся список в строке предложения с расценками или строке контракта по проекту включает все продукты и единицы измерения в прайс-листе продуктов, который вложен в предложение с расценками или контракт по проекту.</span><span class="sxs-lookup"><span data-stu-id="0f280-119">The drop-down list on the quote line or project contract line includes all the products and units in the product price list that is attached to the quote or project contract.</span></span> <span data-ttu-id="0f280-120">Можно также добавлять продукты, которые не входят в прайс-лист продуктов предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="0f280-120">You can also add products that aren't part of quote's product price list.</span></span>

<span data-ttu-id="0f280-121">Кроме того, можно выбрать продукты из других прайс-листов, либо вы можете выбрать продукты непосредственно из каталога продуктов.</span><span class="sxs-lookup"><span data-stu-id="0f280-121">Additionally, you can select products from other price lists, or you can select products directly from the product catalog.</span></span> <span data-ttu-id="0f280-122">При выборе продуктов непосредственно из каталога продуктов прайс-лист по умолчанию для этого продукта используется для получения продажной цены продукта.</span><span class="sxs-lookup"><span data-stu-id="0f280-122">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="0f280-123">Если прайс-лист по умолчанию не установлен, то устанавливается цена 0 (нуль).</span><span class="sxs-lookup"><span data-stu-id="0f280-123">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="0f280-124">Если строка предложения с расценками основана на каталоге продуктов, можно переопределить продажную цену непосредственно в строке предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="0f280-124">If a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="0f280-125">Обратите внимание, кто строка предложения с расценками в Dynamics 365 имеет поле **Ценообразование**.</span><span class="sxs-lookup"><span data-stu-id="0f280-125">Note that a quote line in Dynamics 365 has a **Pricing** field.</span></span> <span data-ttu-id="0f280-126">Доступны два значения:</span><span class="sxs-lookup"><span data-stu-id="0f280-126">Two values are available:</span></span>

- <span data-ttu-id="0f280-127">Переопределить ценообразование</span><span class="sxs-lookup"><span data-stu-id="0f280-127">Override pricing</span></span>  
- <span data-ttu-id="0f280-128">Использовать значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="0f280-128">Use default</span></span>

<span data-ttu-id="0f280-129">Если установить в этом поле значение **Переопределить ценообразование**, Dynamics 365 не задает цену по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0f280-129">If you set this field to **Override pricing**, Dynamics 365 doesn't set a default price.</span></span> <span data-ttu-id="0f280-130">Необходимо ввести цену продукта в строке предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="0f280-130">You must enter a price for the product on the quote line.</span></span> <span data-ttu-id="0f280-131">Если в этом поле задано значение **Использовать значение по умолчанию**, Dynamics 365 использует продажную цену по умолчанию и блокирует поле для исключения его изменения.</span><span class="sxs-lookup"><span data-stu-id="0f280-131">If you set this field to **Use default**, Dynamics 365 uses the default sales price and locks the field to prevent editing.</span></span>

<span data-ttu-id="0f280-132">После установки PSA продажные цены по умолчанию вводятся в строки на основе продукта в предложении с расценками.</span><span class="sxs-lookup"><span data-stu-id="0f280-132">After you install PSA, default sales prices are entered on the product-based lines on a quote.</span></span> <span data-ttu-id="0f280-133">Затем в поле **Ценообразование** устанавливается значение **Переопределить ценообразование**, чтобы можно было изменять цены по умолчанию в строках предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="0f280-133">The **Pricing** field is then set to **Override pricing** so that you can edit the default price on the quote lines.</span></span>

> ![Задание переопределения ценообразования](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a><span data-ttu-id="0f280-135">Факторы количества для продуктов</span><span class="sxs-lookup"><span data-stu-id="0f280-135">Quantity factors for products</span></span>

<span data-ttu-id="0f280-136">PSA использует факторы количества для поддержки продажи продуктов на основе подписки.</span><span class="sxs-lookup"><span data-stu-id="0f280-136">PSA uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="0f280-137">Для продуктов на основе подписки количество в строке предложения с расценками или строке контракта по проекту выражается как число месяцев пользователя.</span><span class="sxs-lookup"><span data-stu-id="0f280-137">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user months.</span></span>

<span data-ttu-id="0f280-138">Обычно цена программного обеспечения по подписке хранится в каталоге как цены за пользователя в месяц.</span><span class="sxs-lookup"><span data-stu-id="0f280-138">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="0f280-139">Однако вместо этого можно использовать другие описания времени.</span><span class="sxs-lookup"><span data-stu-id="0f280-139">However, you can use other time descriptions instead.</span></span> <span data-ttu-id="0f280-140">Во время процесса продажи цена в строке предложения с расценками обычно является ценой за пользователя в месяц, которая была согласована и уценена ИТ-агентом по продажам.</span><span class="sxs-lookup"><span data-stu-id="0f280-140">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="0f280-141">Каждая сделка имеет разное число пользователей и разное количество месяцев подписки.</span><span class="sxs-lookup"><span data-stu-id="0f280-141">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="0f280-142">Количество, используемое, чтобы вычислить сумму строки предложения с расценками — это произведение количества пользователей на количество месяцев подписки.</span><span class="sxs-lookup"><span data-stu-id="0f280-142">The quantity that is used to compute the amount of the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="0f280-143">Чтобы поддержать этот тип продажи, в PSA введена концепция коэффициентов количества.</span><span class="sxs-lookup"><span data-stu-id="0f280-143">To support this type of sale, PSA introduced the concept of quantity factors.</span></span> <span data-ttu-id="0f280-144">Факторы количества основаны на атрибутах продукта в Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="0f280-144">Quantity factors rely on the product attributes in Dynamics 365.</span></span> <span data-ttu-id="0f280-145">При настройке определенных свойств для продукта PSA позволяет отметить подмножество этих свойств или все свойства как факторы количества.</span><span class="sxs-lookup"><span data-stu-id="0f280-145">When you configure specific properties for a product, PSA lets you flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="0f280-146">PSA проверяет, что только численные свойства или свойства продукта с типом числовых данных отмечены как факторы количества.</span><span class="sxs-lookup"><span data-stu-id="0f280-146">PSA validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="0f280-147">Если продукт, для которого настроены факторы количества, добавляется в строку предложения с расценками, поле **Количество** в строке предложения с расценками становится доступным только для чтения.</span><span class="sxs-lookup"><span data-stu-id="0f280-147">When a product that quantity factors are configured for is added to a quote line, the **Quantity** field on the quote line becomes a read-only field.</span></span> <span data-ttu-id="0f280-148">После ввода значений для свойств продукта, которые являются факторами количества, PSA вычисляет количество по строке предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="0f280-148">After you enter values for product properties that are quantity factors, PSA computes the quantity of the quote line.</span></span>

<span data-ttu-id="0f280-149">Например, Dynamics 365 может иметь следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="0f280-149">For example, Dynamics 365 might have the following properties:</span></span> 

- <span data-ttu-id="0f280-150">**Кол-во пользователей** — количество пользователей</span><span class="sxs-lookup"><span data-stu-id="0f280-150">**No of users** - The number of users</span></span> 
- <span data-ttu-id="0f280-151">**Кол-во месяцев** — количество месяцев подписки</span><span class="sxs-lookup"><span data-stu-id="0f280-151">**No of Months** - The number of subscription months</span></span>
- <span data-ttu-id="0f280-152">**SKU продукта**</span><span class="sxs-lookup"><span data-stu-id="0f280-152">**Product SKU**</span></span> 

<span data-ttu-id="0f280-153">Свойства **Кол-во пользователей** и **Кол-во месяцев** могут быть отмечены как факторы количества путем редактирования этих свойств в строке продукта.</span><span class="sxs-lookup"><span data-stu-id="0f280-153">Tne **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span> 

> ![Отметка свойств "Кол-во пользователей" и "Кол-во месяцев" как факторов качества](media/basic-guide-11.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]