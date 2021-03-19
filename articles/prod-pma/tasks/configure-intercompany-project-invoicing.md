---
title: Настройка выставления счетов внутрихолдингового проекта
description: В этой теме показано, как настроить выставление счетов по проекту между двумя компаниями в вашей организации.
author: Yowelle
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9df15cb3712356a164de3507f5dbc17a9ff9a652
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288395"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="0b2c3-103">Настройка выставления счетов внутрихолдингового проекта</span><span class="sxs-lookup"><span data-stu-id="0b2c3-103">Configure intercompany project invoicing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0b2c3-104">В этой теме показано, как настроить выставление счетов по проекту между двумя компаниями в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="0b2c3-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="0b2c3-105">В этой задаче используется набор данных USSI.</span><span class="sxs-lookup"><span data-stu-id="0b2c3-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="0b2c3-106">На панели навигации перейдите **Модули > Расчеты с поставщиками > Продавцы > Все поставщики**.</span><span class="sxs-lookup"><span data-stu-id="0b2c3-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="0b2c3-107">В списке **Все поставщики** найдите и выберите нужную запись.</span><span class="sxs-lookup"><span data-stu-id="0b2c3-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="0b2c3-108">На панели действий выберите **Общее**.</span><span class="sxs-lookup"><span data-stu-id="0b2c3-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="0b2c3-109">Выберите **Внутрихолдинговый**.</span><span class="sxs-lookup"><span data-stu-id="0b2c3-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="0b2c3-110">Задайте **Активный** как **Да** для включения внутрихолдинговой торговли.</span><span class="sxs-lookup"><span data-stu-id="0b2c3-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="0b2c3-111">В поле **Компания клиента** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="0b2c3-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="0b2c3-112">В поле **Моя организация** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="0b2c3-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="0b2c3-113">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="0b2c3-113">Select **Save**.</span></span>
9. <span data-ttu-id="0b2c3-114">Закройте страницы, чтобы вернуться на домашнюю страницу.</span><span class="sxs-lookup"><span data-stu-id="0b2c3-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="0b2c3-115">На панели навигации перейдите **Модули > Управление проектами и учет > Настройка > Параметры управления проектами и учета**.</span><span class="sxs-lookup"><span data-stu-id="0b2c3-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="0b2c3-116">Перейдите на вкладку **Внутрихолдинговый**.</span><span class="sxs-lookup"><span data-stu-id="0b2c3-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="0b2c3-117">Переместите ползунок на **Да** для включения внутрихолдингового планирования ресурсов и расписаний.</span><span class="sxs-lookup"><span data-stu-id="0b2c3-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="0b2c3-118">В списке отметьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="0b2c3-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="0b2c3-119">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="0b2c3-119">Select **New**.</span></span>
15. <span data-ttu-id="0b2c3-120">В поле **Получающая информация о компании** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="0b2c3-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="0b2c3-121">Выберите флажок **Начислить доход**.</span><span class="sxs-lookup"><span data-stu-id="0b2c3-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="0b2c3-122">В поле **Категория расписания по умолчанию** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="0b2c3-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="0b2c3-123">В поле **Категория расходов по умолчанию** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="0b2c3-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="0b2c3-124">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="0b2c3-124">Select **Save**.</span></span>
20. <span data-ttu-id="0b2c3-125">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="0b2c3-125">Close the page.</span></span>
21. <span data-ttu-id="0b2c3-126">На панели навигации перейдите **Модули > Управление проектами и учет > Настройка > Разноска > Настройка разноски ГК**.</span><span class="sxs-lookup"><span data-stu-id="0b2c3-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="0b2c3-127">В поле **Типы счетов ГК** выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="0b2c3-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="0b2c3-128">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="0b2c3-128">Select **New**.</span></span>
24. <span data-ttu-id="0b2c3-129">В поле **Счет ГК** новой строки укажите желаемые значения.</span><span class="sxs-lookup"><span data-stu-id="0b2c3-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="0b2c3-130">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="0b2c3-130">Select **Save**.</span></span>
26. <span data-ttu-id="0b2c3-131">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="0b2c3-131">Close the page.</span></span>
27. <span data-ttu-id="0b2c3-132">На панели навигации перейдите **Модули > Управление проектами и учет > Настройка > Цены > Трансферная цена**.</span><span class="sxs-lookup"><span data-stu-id="0b2c3-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="0b2c3-133">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="0b2c3-133">Select **New**.</span></span>
29. <span data-ttu-id="0b2c3-134">В поле **Дата вступления в силу** введите дату.</span><span class="sxs-lookup"><span data-stu-id="0b2c3-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="0b2c3-135">В поле **Получающая информация о компании** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="0b2c3-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="0b2c3-136">В поле **Модель трансферных цен** выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="0b2c3-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="0b2c3-137">В поле **Цены** введите число.</span><span class="sxs-lookup"><span data-stu-id="0b2c3-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="0b2c3-138">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="0b2c3-138">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]