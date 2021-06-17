---
title: Заказы на покупку для проекта
description: В этой статье описаны различные методы, которые можно использовать для создания заказов на покупку для проекта. Используемый метод зависит от цели заказа на покупку и когда купленные номенклатуры потреблены назначены к оплате по проекту.
author: Yowelle
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3c3ce2d0c0fb3cecf22157db5cb37eb744027d0f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999372"
---
# <a name="purchase-orders-for-a-project"></a><span data-ttu-id="2548f-104">Заказы на покупку для проекта</span><span class="sxs-lookup"><span data-stu-id="2548f-104">Purchase orders for a project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2548f-105">В этой статье описаны различные методы, которые можно использовать для создания заказов на покупку для проекта.</span><span class="sxs-lookup"><span data-stu-id="2548f-105">This article describes the various methods that you can use to create purchase orders for a project.</span></span> <span data-ttu-id="2548f-106">Используемый метод зависит от цели заказа на покупку и когда купленные номенклатуры потреблены назначены к оплате по проекту.</span><span class="sxs-lookup"><span data-stu-id="2548f-106">The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.</span></span>

### <a name="methods-for-creating-a-purchase-order"></a><span data-ttu-id="2548f-107">Способы создания заказа на покупку</span><span class="sxs-lookup"><span data-stu-id="2548f-107">Methods for creating a purchase order</span></span>

<span data-ttu-id="2548f-108">Вы можете использовать один из следующих методов для создания заказа на покупку в управлении проектами и учете.</span><span class="sxs-lookup"><span data-stu-id="2548f-108">You can use one of the following methods to create a purchase order in Project management and accounting.</span></span> <span data-ttu-id="2548f-109">Цель заказа на покупку определяет, когда заказ на покупку потреблен и, следовательно, когда номенклатуры оплачиваются по проекту.</span><span class="sxs-lookup"><span data-stu-id="2548f-109">The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2548f-110">Способ</span><span class="sxs-lookup"><span data-stu-id="2548f-110">Method</span></span></th>
<th><span data-ttu-id="2548f-111">Назначение</span><span class="sxs-lookup"><span data-stu-id="2548f-111">Purpose</span></span></th>
<th><span data-ttu-id="2548f-112">Потребление номенклатур</span><span class="sxs-lookup"><span data-stu-id="2548f-112">Consumption of items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2548f-113">Создайте заказ на покупку прямо из проекта.</span><span class="sxs-lookup"><span data-stu-id="2548f-113">Create a purchase order directly from a project.</span></span></td>
<td><span data-ttu-id="2548f-114">Используйте этот метод для покупки номенклатур у внешнего поставщика для использования в проекте.</span><span class="sxs-lookup"><span data-stu-id="2548f-114">Use this method to purchase items from an external vendor for consumption on a project.</span></span> <span data-ttu-id="2548f-115">Вы можете создать заказ на покупку двумя способами:</span><span class="sxs-lookup"><span data-stu-id="2548f-115">You can create the purchase order in two ways:</span></span>
<ul>
<li><span data-ttu-id="2548f-116">Непосредственно из проекта.</span><span class="sxs-lookup"><span data-stu-id="2548f-116">From the project itself.</span></span> <span data-ttu-id="2548f-117">В этом случае проект уже определен для заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="2548f-117">In this case, the project is already defined for the purchase order.</span></span></li>
<li><span data-ttu-id="2548f-118">Перейдя к заказу на покупку проекта.</span><span class="sxs-lookup"><span data-stu-id="2548f-118">By navigating to the project purchase order.</span></span> <span data-ttu-id="2548f-119">Вы должны выбрать и поставщика, и проект, для которого будет создан заказ на покупку.</span><span class="sxs-lookup"><span data-stu-id="2548f-119">You must select both the vendor and the project to create the purchase order for.</span></span></li>
</ul></td>
<td><span data-ttu-id="2548f-120">Номенклатуры потребляются при обновлении счета поставщика.</span><span class="sxs-lookup"><span data-stu-id="2548f-120">Items are consumed when the vendor invoice is updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2548f-121">Создайте заказ на покупку из заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="2548f-121">Create a purchase order from a sales order.</span></span></td>
<td><span data-ttu-id="2548f-122">Используйте этот метод для покупки номенклатур при создании заказа на продажу из проекта.</span><span class="sxs-lookup"><span data-stu-id="2548f-122">Use this method to purchase items when you create a sales order from a project.</span></span></td>
<td><span data-ttu-id="2548f-123">Номенклатуры потребляются, когда клиенту выставлен счет по заказу на продажу.</span><span class="sxs-lookup"><span data-stu-id="2548f-123">Items are consumed when the sales order is invoiced to the customer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2548f-124">Создайте заказ на покупку из потребности в номенклатуре.</span><span class="sxs-lookup"><span data-stu-id="2548f-124">Create a purchase order from an item requirement.</span></span></td>
<td><span data-ttu-id="2548f-125">Используйте этот метод для покупки номенклатур при создании требования к номенклатуре из проекта.</span><span class="sxs-lookup"><span data-stu-id="2548f-125">Use this method to purchase items when you create an item requirement from a project.</span></span></td>
<td><span data-ttu-id="2548f-126">Номенклатуры потребляются при обновлении отборочной накладной требования к номенклатуре.</span><span class="sxs-lookup"><span data-stu-id="2548f-126">Items are consumed when the item requirement packing slip is updated.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE] 
> <span data-ttu-id="2548f-127">При обновлении счета поставщика или отборочной накладной вам будет предложено обновить отборочную накладную по требованию к номенклатуре.</span><span class="sxs-lookup"><span data-stu-id="2548f-127">When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.</span></span>

<span data-ttu-id="2548f-128">Для получения дополнительной информации см. [Получение номенклатур по заказу на покупку из требования номенклатуры](tasks/receive-items-purchase-order-item-requirement.md).</span><span class="sxs-lookup"><span data-stu-id="2548f-128">For more information, see [Receive items on purchase order from item requirement](tasks/receive-items-purchase-order-item-requirement.md).</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]