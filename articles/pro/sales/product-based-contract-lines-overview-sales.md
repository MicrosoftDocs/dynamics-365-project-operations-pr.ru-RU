---
title: Обзор строк контракта на основе продуктов — облегченное развертывание
description: В этом разделе представлена информация о строках контракта на основе продуктов.
author: rumant
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 8464eefbce9ba266360e10039e2a0be78982d8fa
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369752"
---
# <a name="product-based-contract-lines-overview---lite"></a><span data-ttu-id="0febd-103">Обзор строк контракта на основе продуктов — облегченное развертывание</span><span class="sxs-lookup"><span data-stu-id="0febd-103">Product-based contract lines overview - lite</span></span>

<span data-ttu-id="0febd-104">_**Относится к:** развертывание Lite — от сделки до счетов-проформ_</span><span class="sxs-lookup"><span data-stu-id="0febd-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0febd-105">Можно создать строки контракта на основе продукта в Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="0febd-105">You can create product-based contract lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="0febd-106">Строки контракта на основе продукта могут быть вручную созданными строками или они могут быть номенклатурами из каталога продуктов.</span><span class="sxs-lookup"><span data-stu-id="0febd-106">Product-based contract lines can be manually created lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="0febd-107">Каталог продукции</span><span class="sxs-lookup"><span data-stu-id="0febd-107">Product catalog</span></span>

<span data-ttu-id="0febd-108">Продукты в каталоге продуктов имеют единицу измерения и группу единиц измерения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0febd-108">The products in the product catalog have a default unit and unit group.</span></span> <span data-ttu-id="0febd-109">Если несколько продуктов имеют один и тот же набор атрибутов, можно создать семейство продуктов, которое также имеет эти атрибуты.</span><span class="sxs-lookup"><span data-stu-id="0febd-109">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="0febd-110">Все продукты виз одного семейства продуктов наследуют одинаковый набор атрибутов.</span><span class="sxs-lookup"><span data-stu-id="0febd-110">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="0febd-111">Например, компания продает лицензии на подписку на программное обеспечение разных видов.</span><span class="sxs-lookup"><span data-stu-id="0febd-111">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="0febd-112">Все программное обеспечение по подписке имеет два следующих атрибута:</span><span class="sxs-lookup"><span data-stu-id="0febd-112">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="0febd-113">Количество пользователей</span><span class="sxs-lookup"><span data-stu-id="0febd-113">Number of users</span></span>
- <span data-ttu-id="0febd-114">Длительность подписки (в месяцах)</span><span class="sxs-lookup"><span data-stu-id="0febd-114">Subscription duration (in months)</span></span>

<span data-ttu-id="0febd-115">Чтобы поддерживать этот тип каталога, создайте семейство продуктов с именем **Программное обеспечение по подписке**.</span><span class="sxs-lookup"><span data-stu-id="0febd-115">To maintain this type of catalog, create a product family that is named **Subscription Software**.</span></span> <span data-ttu-id="0febd-116">Добавьте атрибуты **Количество пользователей** и **Срок подписки** к семейству продуктов.</span><span class="sxs-lookup"><span data-stu-id="0febd-116">Add the attributes, **Number of users** and **Subscription duration** to the product family.</span></span> <span data-ttu-id="0febd-117">Затем добавьте отдельные продукты в семейство продуктов **Программное обеспечение по подписке**.</span><span class="sxs-lookup"><span data-stu-id="0febd-117">Then, add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-contract"></a><span data-ttu-id="0febd-118">Добавление номенклатур каталога продуктов в контракт по проекту</span><span class="sxs-lookup"><span data-stu-id="0febd-118">Add product catalog items to a project Contract</span></span>

<span data-ttu-id="0febd-119">Контракты по проекту содержат разделы для двух типов строк: строки на основе проекта и строки на основе продукта.</span><span class="sxs-lookup"><span data-stu-id="0febd-119">Project contracts have sections for two types of lines, project-based and product-based.</span></span> <span data-ttu-id="0febd-120">Строки на основе продукта включают все продукты и единицы, указанные в прайс-листе продуктов по контракту.</span><span class="sxs-lookup"><span data-stu-id="0febd-120">Product-based lines include all of the products and units in the product price list on the contract.</span></span> <span data-ttu-id="0febd-121">Продукты, которые не входят в прайс-лист продуктов по контракту, могут быть добавлены.</span><span class="sxs-lookup"><span data-stu-id="0febd-121">Products that aren't part of contract's product price list can be added.</span></span>

<span data-ttu-id="0febd-122">Вы можете выбрать товары из других прайс-листов или прямо из каталога товаров.</span><span class="sxs-lookup"><span data-stu-id="0febd-122">You can select products from other price lists, or directly from the product catalog.</span></span> <span data-ttu-id="0febd-123">При выборе продуктов непосредственно из каталога продуктов прайс-лист по умолчанию для этого продукта используется для продажной цены продукта.</span><span class="sxs-lookup"><span data-stu-id="0febd-123">When you select products directly from a product catalog, the default price list of that product is used for the product's sales price.</span></span> <span data-ttu-id="0febd-124">Если прайс-лист по умолчанию не установлен, то устанавливается цена 0 (нуль).</span><span class="sxs-lookup"><span data-stu-id="0febd-124">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="0febd-125">Если строка контракта основана на каталоге продуктов, можно переопределить продажную цену непосредственно в строке.</span><span class="sxs-lookup"><span data-stu-id="0febd-125">If a contract line is based on a product catalog, you can override the sales price directly on the line.</span></span> <span data-ttu-id="0febd-126">В строке контракта есть поле **Цены** с двумя значениями:</span><span class="sxs-lookup"><span data-stu-id="0febd-126">A contract line has the **Pricing** field with the two values:</span></span>

- <span data-ttu-id="0febd-127">**Переопределить ценообразование**</span><span class="sxs-lookup"><span data-stu-id="0febd-127">**Override pricing**</span></span>
- <span data-ttu-id="0febd-128">**Использовать значение по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="0febd-128">**Use default**</span></span>

<span data-ttu-id="0febd-129">Если установить в поле **Цены** значение **Переопределить цены**, цена по умолчанию не задается.</span><span class="sxs-lookup"><span data-stu-id="0febd-129">If you set the **Pricing** field to **Override pricing**, the default price isn't set.</span></span> <span data-ttu-id="0febd-130">Введите цену для продукта в строке контракта.</span><span class="sxs-lookup"><span data-stu-id="0febd-130">Enter a price for the product on the contract line.</span></span> <span data-ttu-id="0febd-131">Если вы установите в поле значение **Использовать по умолчанию**, используется цена продажи по умолчанию, и поле нельзя редактировать.</span><span class="sxs-lookup"><span data-stu-id="0febd-131">If you set the field to **Use default**, the default sales price is used and the field can't be edited.</span></span>

<span data-ttu-id="0febd-132">После установки Project Operations продажные цены по умолчанию вводятся в строки на основе продукта в контракте.</span><span class="sxs-lookup"><span data-stu-id="0febd-132">After you install Project Operations, default sales prices are entered on the product-based lines on a contract.</span></span> <span data-ttu-id="0febd-133">В поле **Цены** устанавливается значение **Переопределить цены**, чтобы можно было изменять цены по умолчанию в строках контракта.</span><span class="sxs-lookup"><span data-stu-id="0febd-133">The **Pricing** field is set to **Override pricing** so that you can edit the default price on the contract lines.</span></span> <span data-ttu-id="0febd-134">Это специфичное для Project Operations переопределение поведения строк на основе продуктов в Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="0febd-134">This is a Project Operations-specific override to product-based lines behavior in Dynamics 365 Sales.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]