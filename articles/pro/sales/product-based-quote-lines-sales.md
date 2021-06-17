---
title: Обзор строк предложения с расценками на основе продуктов — облегченное развертывание
description: Эта тема предоставляет информацию о работе со строками предложений с расценками на основе продукта.
author: rumant
ms.date: 10/30/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5cc3a97194e01b14de054a93a6268c1f0c24bc25
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994467"
---
# <a name="product-based-quote-lines-overview---lite"></a><span data-ttu-id="0c38a-103">Обзор строк предложения с расценками на основе продуктов — облегченное развертывание</span><span class="sxs-lookup"><span data-stu-id="0c38a-103">Product-based quote lines overview - lite</span></span>

<span data-ttu-id="0c38a-104">_**Относится к:** развертывание Lite — от сделки до счетов-проформ_</span><span class="sxs-lookup"><span data-stu-id="0c38a-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0c38a-105">Можно создать строки предложения с расценками на основе продукта в Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="0c38a-105">You can create product-based quote lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="0c38a-106">Строки предложения с расценками на основе продукта могут быть добавлены вручную или они могут быть номенклатурами из каталога продуктов.</span><span class="sxs-lookup"><span data-stu-id="0c38a-106">Product-based quote lines can be manually added, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="0c38a-107">Каталог продукции</span><span class="sxs-lookup"><span data-stu-id="0c38a-107">Product catalog</span></span>

<span data-ttu-id="0c38a-108">Каждый продукт в каталоге продукции имеют единицу измерения и группу единиц измерения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0c38a-108">Each product in the product catalog has a default unit and unit group.</span></span> <span data-ttu-id="0c38a-109">Если несколько продуктов имеют один и тот же набор атрибутов, можно создать семейство продуктов, для которого эти атрибуты общие.</span><span class="sxs-lookup"><span data-stu-id="0c38a-109">If multiple products share the same set of attributes, you can create a product family that share those attributes.</span></span> 

<span data-ttu-id="0c38a-110">Например, компания продает лицензии на подписку на программное обеспечение разных видов.</span><span class="sxs-lookup"><span data-stu-id="0c38a-110">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="0c38a-111">Все программное обеспечение по подписке имеет два следующих атрибута:</span><span class="sxs-lookup"><span data-stu-id="0c38a-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="0c38a-112">Количество пользователей</span><span class="sxs-lookup"><span data-stu-id="0c38a-112">Number of users</span></span>
- <span data-ttu-id="0c38a-113">Длительность подписки, измеренная в месяцах</span><span class="sxs-lookup"><span data-stu-id="0c38a-113">A subscription duration measured in months</span></span>

<span data-ttu-id="0c38a-114">Для ведения каталога такого типа создайте семейство продуктов с названием **Программное обеспечение по подписке** и добавьте количество пользователей и длительности подписки в качестве атрибутов.</span><span class="sxs-lookup"><span data-stu-id="0c38a-114">To maintain this type of catalog, create a product family named **Subscription Software** and add the number of users and the subscription duration as attributes.</span></span> <span data-ttu-id="0c38a-115">Затем вы можете добавить отдельные продукты в семейство продуктов **Программное обеспечение по подписке**.</span><span class="sxs-lookup"><span data-stu-id="0c38a-115">Next, you can add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="0c38a-116">Добавление номенклатур каталога продуктов в предложение с расценками по проекту</span><span class="sxs-lookup"><span data-stu-id="0c38a-116">Add product catalog items to a project quote</span></span>

<span data-ttu-id="0c38a-117">На страницах **Предложение с расценками по проекту** и **Контракт по проекту** содержатся разделы для строк на основе проекта и строк на основе продукта.</span><span class="sxs-lookup"><span data-stu-id="0c38a-117">The **Project Quote** and **Project Contract** pages have sections for project-based lines and product-based lines.</span></span> <span data-ttu-id="0c38a-118">Для строк на основе продуктов раскрывающийся список в строке предложения с расценками или строке контракта по проекту включает все продукты и единицы измерения в прайс-листе продуктов.</span><span class="sxs-lookup"><span data-stu-id="0c38a-118">For product-based lines, the drop-down list on the quote line or project contract line includes all the products and units in the product price list.</span></span> <span data-ttu-id="0c38a-119">Можно также добавлять продукты, которые не входят в прайс-лист продуктов.</span><span class="sxs-lookup"><span data-stu-id="0c38a-119">You can also add products that aren't part of the product price list.</span></span>

<span data-ttu-id="0c38a-120">Кроме того, можно выбрать продукты из других прайс-листов или непосредственно из каталога продуктов.</span><span class="sxs-lookup"><span data-stu-id="0c38a-120">Additionally, you can select products from other price lists or directly from the product catalog.</span></span> <span data-ttu-id="0c38a-121">При выборе продуктов непосредственно из каталога продуктов прайс-лист по умолчанию для этого продукта используется для получения продажной цены продукта.</span><span class="sxs-lookup"><span data-stu-id="0c38a-121">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="0c38a-122">Если прайс-лист по умолчанию не установлен, то устанавливается нулевая (0) цена.</span><span class="sxs-lookup"><span data-stu-id="0c38a-122">If a default price list isn't set, the price is set to zero (0).</span></span>

<span data-ttu-id="0c38a-123">Когда строка предложения с расценками основана на каталоге продуктов, можно переопределить продажную цену непосредственно в строке предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="0c38a-123">When a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="0c38a-124">Строка предложения с расценками в поле **Цены** с двумя доступными значениями:</span><span class="sxs-lookup"><span data-stu-id="0c38a-124">A quote line in **Pricing** field with two available values:</span></span>

- <span data-ttu-id="0c38a-125">**Переопределить цены**</span><span class="sxs-lookup"><span data-stu-id="0c38a-125">**Override Pricing**</span></span>
- <span data-ttu-id="0c38a-126">**Использовать режим по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="0c38a-126">**Use Default**</span></span>

<span data-ttu-id="0c38a-127">Если вы выберете **Переопределить цены**, цена по умолчанию не устанавливается.</span><span class="sxs-lookup"><span data-stu-id="0c38a-127">If you select **Override Pricing**, the default price isn't set.</span></span> <span data-ttu-id="0c38a-128">Вместо этого необходимо ввести цену продукта в строке предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="0c38a-128">Instead, you must enter a price for the product on the quote line.</span></span> <span data-ttu-id="0c38a-129">Если вы выберете **Использовать по умолчанию**, используется цена продажи по умолчанию, и поле заблокировано для редактирования.</span><span class="sxs-lookup"><span data-stu-id="0c38a-129">If you select **Use Default**, the default sales price is used and the field is locked for editing.</span></span>

<span data-ttu-id="0c38a-130">Продажные цены по умолчанию вводятся в строки на основе продукта в предложении с расценками.</span><span class="sxs-lookup"><span data-stu-id="0c38a-130">Default sales prices are entered on the product-based lines of a quote.</span></span> <span data-ttu-id="0c38a-131">Затем в поле **Цены** устанавливается значение **Переопределить цены**, чтобы можно было изменять цены по умолчанию в строках предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="0c38a-131">The **Pricing** field is then set to **Override Pricing** so that you can edit the default price on the quote lines.</span></span> <span data-ttu-id="0c38a-132">Это специфичное для Project Operations переопределение поведения строк на основе продуктов в Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="0c38a-132">This is a Project Operations-specific override to the product-based lines behavior in Dynamics 365 Sales.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]