---
title: Получение номенклатур по заказу на покупку из требования номенклатуры
description: В этой теме объясняется, как получить номенклатуру заказа на покупку из требования номенклатуры.
author: KimANelson
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.assetid: c61e3a5e-da3d-4f4c-87fa-03dea19f6936
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c5ed287aa24aff647ef1dc625f9e9f5f086ee662
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754891"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="b2ba1-103">Получение номенклатур по заказу на покупку из требования номенклатуры</span><span class="sxs-lookup"><span data-stu-id="b2ba1-103">Receive items on purchase order from item requirement</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b2ba1-104">В этой теме объясняется, как получить номенклатуру заказа на покупку из требования номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="b2ba1-104">This topic explains how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="b2ba1-105">Используя требование номенклатуры вместо транзакции номенклатуры, вы можете спланировать доставку непосредственно перед тем, как номенклатура будет фактически использована, создать заказ на покупку, включить номенклатуру в структуру торгового соглашения и включить требование номенклатуры в производственное планирование.</span><span class="sxs-lookup"><span data-stu-id="b2ba1-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="b2ba1-106">В этой задаче используется набор данных USSI.</span><span class="sxs-lookup"><span data-stu-id="b2ba1-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="b2ba1-107">На панели навигации перейдите **Модули > Управление проектами и учет > Проекты > Все проекты**.</span><span class="sxs-lookup"><span data-stu-id="b2ba1-107">In the navigation pane, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="b2ba1-108">В списке щелкните ссылку в нужной строке.</span><span class="sxs-lookup"><span data-stu-id="b2ba1-108">In the list, select the link in the desired row.</span></span>
3. <span data-ttu-id="b2ba1-109">На панели действий выберите **План**.</span><span class="sxs-lookup"><span data-stu-id="b2ba1-109">On the Action Pane, select **Plan**.</span></span>
4. <span data-ttu-id="b2ba1-110">Выберите **Требования номенклатур**.</span><span class="sxs-lookup"><span data-stu-id="b2ba1-110">Select **Item requirements**.</span></span>
5. <span data-ttu-id="b2ba1-111">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="b2ba1-111">Select **New**.</span></span>
6. <span data-ttu-id="b2ba1-112">В новой строке введите или выберите значение в поле **Номер номенклатуры**.</span><span class="sxs-lookup"><span data-stu-id="b2ba1-112">In the new row, enter or select a value in the **Item number** field.</span></span>
7. <span data-ttu-id="b2ba1-113">В поле **Количество** введите число.</span><span class="sxs-lookup"><span data-stu-id="b2ba1-113">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="b2ba1-114">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="b2ba1-114">Select **Save**.</span></span>
9. <span data-ttu-id="b2ba1-115">На панели действий выберите **Управление**.</span><span class="sxs-lookup"><span data-stu-id="b2ba1-115">On the Action Pane, select **Manage**.</span></span>
10. <span data-ttu-id="b2ba1-116">Выберите **Функции**.</span><span class="sxs-lookup"><span data-stu-id="b2ba1-116">Select **Functions**.</span></span>
11. <span data-ttu-id="b2ba1-117">Выберите **Создание заказа на покупку**.</span><span class="sxs-lookup"><span data-stu-id="b2ba1-117">Select **Create purchase order**.</span></span>
12. <span data-ttu-id="b2ba1-118">Выберите флажок **Включить все**.</span><span class="sxs-lookup"><span data-stu-id="b2ba1-118">Select the **Include all** check box.</span></span>
13. <span data-ttu-id="b2ba1-119">В поле **Организация поставщика** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="b2ba1-119">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="b2ba1-120">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b2ba1-120">Select **OK**.</span></span>
15. <span data-ttu-id="b2ba1-121">На панели навигации перейдите **Модули > Расчеты с поставщиками > Заказы на покупку > Все заказы на покупку**.</span><span class="sxs-lookup"><span data-stu-id="b2ba1-121">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
16. <span data-ttu-id="b2ba1-122">В списке щелкните ссылку в нужной строке.</span><span class="sxs-lookup"><span data-stu-id="b2ba1-122">In the list, select the link in the desired row.</span></span>
17. <span data-ttu-id="b2ba1-123">На панели действий выберите **Покупка**.</span><span class="sxs-lookup"><span data-stu-id="b2ba1-123">On the Action Pane, select **Purchase**.</span></span>
18. <span data-ttu-id="b2ba1-124">Выберите **Подтвердить**.</span><span class="sxs-lookup"><span data-stu-id="b2ba1-124">Select **Confirm**.</span></span>
19. <span data-ttu-id="b2ba1-125">На панели действий выберите **Получение**.</span><span class="sxs-lookup"><span data-stu-id="b2ba1-125">On the Action Pane, select **Receive**.</span></span>
20. <span data-ttu-id="b2ba1-126">Выберите **Получение продукта**.</span><span class="sxs-lookup"><span data-stu-id="b2ba1-126">Select **Product receipt**.</span></span>
21. <span data-ttu-id="b2ba1-127">В поле **Получение продукта** введите значение.</span><span class="sxs-lookup"><span data-stu-id="b2ba1-127">In the **Product receipt** field, type a value.</span></span>
22. <span data-ttu-id="b2ba1-128">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b2ba1-128">Select **OK**.</span></span>

