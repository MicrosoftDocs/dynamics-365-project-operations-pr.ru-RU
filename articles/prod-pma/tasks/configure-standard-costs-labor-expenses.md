---
title: Настройка стандартных затрат на труд и расходов
description: В этой теме объясняется, как установить стандартные затраты на рабочую силу и расходы для проекта.
author: Yowelle
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b16ed50584b2b4535d1c61fe7069708182a4820e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288350"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="dd439-103">Настройка стандартных затрат на труд и расходов</span><span class="sxs-lookup"><span data-stu-id="dd439-103">Configure standard costs for labor and expenses</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dd439-104">В этой теме объясняется, как установить стандартные затраты на рабочую силу и расходы для проекта.</span><span class="sxs-lookup"><span data-stu-id="dd439-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="dd439-105">В этой задаче используется набор данных USSI.</span><span class="sxs-lookup"><span data-stu-id="dd439-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="dd439-106">На панели навигации перейдите **Модули > Управление проектами и учет > Настройка > Цены > Себестоимость (час)**.</span><span class="sxs-lookup"><span data-stu-id="dd439-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="dd439-107">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="dd439-107">Select **New**.</span></span>
3. <span data-ttu-id="dd439-108">В поле **Дата вступления в силу** введите дату.</span><span class="sxs-lookup"><span data-stu-id="dd439-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="dd439-109">В поле **Себестоимость** введите число.</span><span class="sxs-lookup"><span data-stu-id="dd439-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="dd439-110">Вы можете установить стандартную себестоимость для категории проекта или установить себестоимость по номеру работника, номеру проекта, категории, дате или любой их комбинации.</span><span class="sxs-lookup"><span data-stu-id="dd439-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="dd439-111">Применяемая себестоимость является себестоимостью с максимальным уровнем детализации.</span><span class="sxs-lookup"><span data-stu-id="dd439-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="dd439-112">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="dd439-112">Select **Save**.</span></span>
6. <span data-ttu-id="dd439-113">На панели навигации перейдите **Модули > Управление проектами и учет > Настройка > Цены > Цена продажи (час)**.</span><span class="sxs-lookup"><span data-stu-id="dd439-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="dd439-114">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="dd439-114">Select **New**.</span></span>
8. <span data-ttu-id="dd439-115">В поле **Дата вступления в силу** введите дату.</span><span class="sxs-lookup"><span data-stu-id="dd439-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="dd439-116">В поле **Действительно до** параметр выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="dd439-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="dd439-117">В поле **Цены** введите число.</span><span class="sxs-lookup"><span data-stu-id="dd439-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="dd439-118">Вы можете установить стандартную цену продажи для почасовых проводок или для категории проекта.</span><span class="sxs-lookup"><span data-stu-id="dd439-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="dd439-119">Вы также можете установить цены продажи по номеру работника, номеру проекта, категории, дате транзакции или любой их комбинации.</span><span class="sxs-lookup"><span data-stu-id="dd439-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="dd439-120">Фактическая цена продажи, которая применяется, когда работник вводит проводку в журнал часов, является ценой продажи с наивысшим уровнем детализации.</span><span class="sxs-lookup"><span data-stu-id="dd439-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="dd439-121">Например, если установлены и общая цена продажи, и цена продажи для конкретного работника, используется цена продажи для конкретного работника.</span><span class="sxs-lookup"><span data-stu-id="dd439-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="dd439-122">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="dd439-122">Select **Save**.</span></span>
12. <span data-ttu-id="dd439-123">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="dd439-123">Close the page.</span></span>
13. <span data-ttu-id="dd439-124">На панели навигации перейдите **Модули > Управление проектами и учет > Настройка > Цены > Себестоимость (расход)**.</span><span class="sxs-lookup"><span data-stu-id="dd439-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="dd439-125">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="dd439-125">Select **New**.</span></span>
15. <span data-ttu-id="dd439-126">В поле **Дата вступления в силу** введите дату.</span><span class="sxs-lookup"><span data-stu-id="dd439-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="dd439-127">В поле **Себестоимость** введите число.</span><span class="sxs-lookup"><span data-stu-id="dd439-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="dd439-128">Можно заполнить несколько полей, но это минимум, необходимый для сохранения записи.</span><span class="sxs-lookup"><span data-stu-id="dd439-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="dd439-129">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="dd439-129">Select **Save**.</span></span>
18. <span data-ttu-id="dd439-130">На панели навигации перейдите **Модули > Управление проектами и учет > Настройка > Цены > Цена продажи (расход)**.</span><span class="sxs-lookup"><span data-stu-id="dd439-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="dd439-131">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="dd439-131">Select **New**.</span></span>
20. <span data-ttu-id="dd439-132">В поле **Дата вступления в силу** введите дату.</span><span class="sxs-lookup"><span data-stu-id="dd439-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="dd439-133">В поле **Действительно до** параметр выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="dd439-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="dd439-134">В поле **Цены** введите число.</span><span class="sxs-lookup"><span data-stu-id="dd439-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="dd439-135">Фактическая цена продажи, которая применяется, когда работник вводит проводки в журнал расходов, является ценой продажи с наивысшим уровнем детализации.</span><span class="sxs-lookup"><span data-stu-id="dd439-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="dd439-136">Например, если установлены и общая цена продажи, и цена продажи для конкретного работника, используется цена продажи для конкретного работника.</span><span class="sxs-lookup"><span data-stu-id="dd439-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="dd439-137">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="dd439-137">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]