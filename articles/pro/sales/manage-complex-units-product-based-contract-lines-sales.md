---
title: Управление сложными единицами измерения для строк контракта на основе продуктов — облегченное развертывание
description: Эта тема предоставляет информацию о поддержке продажи продуктов на основе подписки.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a58a13c8186f36e6031fe3c6f3c3a57ea920ac9e
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177392"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a><span data-ttu-id="75d1a-103">Управление сложными единицами измерения для строк контракта на основе продуктов — облегченное развертывание</span><span class="sxs-lookup"><span data-stu-id="75d1a-103">Manage complex units for product-based contract lines - lite</span></span>

<span data-ttu-id="75d1a-104">_**Относится к:** развертывание Lite — от сделки до счетов-проформ_</span><span class="sxs-lookup"><span data-stu-id="75d1a-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="75d1a-105">Dynamics 365 Project Operations использует факторы количества для поддержки продажи продуктов на основе подписки.</span><span class="sxs-lookup"><span data-stu-id="75d1a-105">Dynamics 365 Project Operations uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="75d1a-106">Для продуктов на основе подписки количество в контракте или строке контракта по проекту выражается как число пользователе-месяцев.</span><span class="sxs-lookup"><span data-stu-id="75d1a-106">For subscription-based products, the quantity on the contract or project contract line is expressed as the number of user-months.</span></span>

<span data-ttu-id="75d1a-107">Цена программного обеспечения по подписке хранится в каталоге как цена за пользователя в месяц.</span><span class="sxs-lookup"><span data-stu-id="75d1a-107">The price of subscription software is stored in the catalog as the price per-user, per-month.</span></span> <span data-ttu-id="75d1a-108">Во время процесса продажи цена в строке контракта обычно является ценой за пользователя в месяц, которая была согласована и уценена агентом по продажам.</span><span class="sxs-lookup"><span data-stu-id="75d1a-108">During the sales process, the price on the contract line is usually the per-user, per-month price that was negotiated and discounted by the sales agent.</span></span> <span data-ttu-id="75d1a-109">Каждая сделка имеет разное число пользователей и разное количество месяцев подписки.</span><span class="sxs-lookup"><span data-stu-id="75d1a-109">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="75d1a-110">Количество, используемое, чтобы вычислить сумму строки контракта — это произведение количества пользователей на количество месяцев подписки.</span><span class="sxs-lookup"><span data-stu-id="75d1a-110">The quantity used to calculate the amount of the contract line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="75d1a-111">Чтобы поддержать этот тип продажи, в Project Operations поддерживается концепция *коэффициентов количества*.</span><span class="sxs-lookup"><span data-stu-id="75d1a-111">To support this type of sale, Project Operations supports the concept of *quantity factors*.</span></span> <span data-ttu-id="75d1a-112">Факторы количества основаны на атрибутах продукта.</span><span class="sxs-lookup"><span data-stu-id="75d1a-112">Quantity factors rely on product attributes.</span></span> <span data-ttu-id="75d1a-113">При настройке определенных свойств для продукта можно отметить подмножество этих свойств или все свойства как факторы количества.</span><span class="sxs-lookup"><span data-stu-id="75d1a-113">When you configure specific properties for a product, you can flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="75d1a-114">Project Operations проверяет, что только численные свойства или свойства продукта с типом числовых данных отмечены как факторы количества.</span><span class="sxs-lookup"><span data-stu-id="75d1a-114">Project Operations validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="75d1a-115">Когда продукт с настроенными количественными коэффициентами добавляется в строку контракта, поле **Количество** становится доступным только для чтения.</span><span class="sxs-lookup"><span data-stu-id="75d1a-115">When a product with configured quantity factors is added to a contract line, the **Quantity** field  becomes read-only.</span></span> <span data-ttu-id="75d1a-116">После ввода значений для свойств продукта, которые являются факторами количества, Project Operations вычисляет количество по строке контракта.</span><span class="sxs-lookup"><span data-stu-id="75d1a-116">After you enter values for product properties that are quantity factors, Project Operations calculates the quantity of the contract line.</span></span>

<span data-ttu-id="75d1a-117">Например, Dynamics 365 Sales может иметь следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="75d1a-117">For example, Dynamics 365 Sales might have the following properties:</span></span>

- <span data-ttu-id="75d1a-118">**Кол-во пользователей**: количество пользователей.</span><span class="sxs-lookup"><span data-stu-id="75d1a-118">**No of users**: The number of users.</span></span>
- <span data-ttu-id="75d1a-119">**Кол-во месяцев**: количество месяцев подписки.</span><span class="sxs-lookup"><span data-stu-id="75d1a-119">**No of Months**: The number of subscription months.</span></span>
- <span data-ttu-id="75d1a-120">**SKU продукта**: единица складского учета (SKU) для продукта.</span><span class="sxs-lookup"><span data-stu-id="75d1a-120">**Product SKU**: The stock keeping unit (SKU) for the product.</span></span>

<span data-ttu-id="75d1a-121">Свойства **Кол-во пользователей** и **Кол-во месяцев** могут быть отмечены как факторы количества путем редактирования этих свойств в строке продукта.</span><span class="sxs-lookup"><span data-stu-id="75d1a-121">The **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span>

<span data-ttu-id="75d1a-122">Чтобы создать количественные коэффициенты из свойств продукта, выполните следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="75d1a-122">To create quantity factors from product properties, complete the following steps.</span></span>

1. <span data-ttu-id="75d1a-123">В **Project Operations** выберите **Продажи-Продукты**.</span><span class="sxs-lookup"><span data-stu-id="75d1a-123">On the **Project Operations**, select **Sales-Products**.</span></span>
2. <span data-ttu-id="75d1a-124">Откройте продукт, для которого нужно настроить количественные коэффициенты.</span><span class="sxs-lookup"><span data-stu-id="75d1a-124">Open the product for which you need to set up quantity factors.</span></span> <span data-ttu-id="75d1a-125">Убедитесь, что для продукта уже настроены свойства.</span><span class="sxs-lookup"><span data-stu-id="75d1a-125">Make sure that the product has properties already set up.</span></span>
3. <span data-ttu-id="75d1a-126">На странице **Сведения о проекте** выберите вкладку **Коэффициенты количества**.</span><span class="sxs-lookup"><span data-stu-id="75d1a-126">On the **Project Information** page, select the **Quantity Factors** tab.</span></span>
4. <span data-ttu-id="75d1a-127">На вложенной сетке выберите **+ Новый расчет поля**.</span><span class="sxs-lookup"><span data-stu-id="75d1a-127">In the subgrid, select **+ New field computation**.</span></span>
5. <span data-ttu-id="75d1a-128">Введите имя **Коэффициента количества** и выберите значение свойства, которое соответствует вычислению поля.</span><span class="sxs-lookup"><span data-stu-id="75d1a-128">Enter the name of the **Quantity Factor** and select the property value that maps to the field computation.</span></span>
6. <span data-ttu-id="75d1a-129">Сохраните и закройте форму.</span><span class="sxs-lookup"><span data-stu-id="75d1a-129">Save and close the form.</span></span>
7. <span data-ttu-id="75d1a-130">Повторите шаги 2–6 для всех свойств, которые вместе составляют количество для строки контракта на основе продукта.</span><span class="sxs-lookup"><span data-stu-id="75d1a-130">Repeat steps 2-6 for all the properties that together will make up the quantity for the product-based contract line.</span></span>

<span data-ttu-id="75d1a-131">Если настроены количественные коэффициенты, когда пользователь создает строку контракта для этого продукта, количество в строке контракта блокируется.</span><span class="sxs-lookup"><span data-stu-id="75d1a-131">With quantity factors set up, when the user creates a contract line for this product, the quantity of the contract line is locked.</span></span> <span data-ttu-id="75d1a-132">Затем количество рассчитывается как произведение значений свойств для этой строки контракта.</span><span class="sxs-lookup"><span data-stu-id="75d1a-132">The quantity is then calculated as a product of the property values for that contract line.</span></span>
