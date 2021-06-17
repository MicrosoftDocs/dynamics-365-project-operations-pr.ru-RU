---
title: Единицы измерения и группы единиц измерения
description: В этом разделе представлена информация о том, как создавать единицы и группы единиц в Dynamics 365 Project Operations.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 646e20189efb4aab56972f01a52b1bff19f2e79f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996087"
---
# <a name="units-and-unit-groups"></a><span data-ttu-id="f93c4-103">Единицы измерения и группы единиц измерения</span><span class="sxs-lookup"><span data-stu-id="f93c4-103">Units and unit groups</span></span>

<span data-ttu-id="f93c4-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="f93c4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f93c4-105">Единицы измерения являются количествами или измерениями продаваемых продуктов или услуг.</span><span class="sxs-lookup"><span data-stu-id="f93c4-105">Units are the quantities or measurements that you sell your products or services in.</span></span> <span data-ttu-id="f93c4-106">Например, если продаются товары для сада, единицей измерения семян могут быть пакеты, ящики и паллеты.</span><span class="sxs-lookup"><span data-stu-id="f93c4-106">For example, if you sell gardening supplies, you might sell seeds in units of packets, boxes, and pallets.</span></span> <span data-ttu-id="f93c4-107">Группа единиц измерения — это набор упомянутых единиц.</span><span class="sxs-lookup"><span data-stu-id="f93c4-107">A unit group is a collection of these different units.</span></span>

<span data-ttu-id="f93c4-108">Чтобы выполнить шаги, описанные в этой теме, убедитесь, что вам назначена роль системного администратора или менеджера Sales Professional или у вас есть эквивалентные разрешения.</span><span class="sxs-lookup"><span data-stu-id="f93c4-108">To complete the steps in this topic, make sure that you have been assigned to the System Administrator or Sales Professional Manager role or have equivalent permissions.</span></span>

## <a name="create-a-unit-group"></a><span data-ttu-id="f93c4-109">Создание группы единиц измерения</span><span class="sxs-lookup"><span data-stu-id="f93c4-109">Create a unit group</span></span>

1. <span data-ttu-id="f93c4-110">На карте сайта выберите **Единицы измерения**.</span><span class="sxs-lookup"><span data-stu-id="f93c4-110">In the site map, select **Units**.</span></span>
2. <span data-ttu-id="f93c4-111">Выберите **Создать** и в диалоговом окне **Создать группу единиц измерения** введите имя единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="f93c4-111">Select **New**, and in the **Create Unit Group** dialog box, enter the unit name.</span></span>
3. <span data-ttu-id="f93c4-112">В поле **Основная единица измерения** введите наименьшую общую единицу измерения, по которой будет продаваться продукт.</span><span class="sxs-lookup"><span data-stu-id="f93c4-112">In the **Primary unit** field, enter the lowest common unit of measure that the product will be sold in.</span></span> <span data-ttu-id="f93c4-113">Например, вы можете ввести "штука" или "унция".</span><span class="sxs-lookup"><span data-stu-id="f93c4-113">For example, you might enter "piece" or "ounce".</span></span>
4. <span data-ttu-id="f93c4-114">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f93c4-114">Select **OK**.</span></span>

## <a name="add-units-to-a-unit-group"></a><span data-ttu-id="f93c4-115">Добавление единиц измерения в группу единиц измерения</span><span class="sxs-lookup"><span data-stu-id="f93c4-115">Add units to a unit group</span></span>

1. <span data-ttu-id="f93c4-116">Откройте группу единиц измерения и на вкладке **Связанные** выберите **Единицы измерения**.</span><span class="sxs-lookup"><span data-stu-id="f93c4-116">Open a unit group, and on the **Related** tab, select **Units**.</span></span> <span data-ttu-id="f93c4-117">Вы увидите, что основная единица измерения уже добавлена.</span><span class="sxs-lookup"><span data-stu-id="f93c4-117">You will see that the primary unit is already added.</span></span>
2. <span data-ttu-id="f93c4-118">Выберите **Добавить новую единицу измерения** и на странице **Быстрое создание: единица измерения** в поле **Имя** введите название единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="f93c4-118">Select **Add New Unit**, and on the **Quick Create: Unit** page, in the **Name** field, enter the nanem of the unit.</span></span>
3. <span data-ttu-id="f93c4-119">В поле **Количество** введите количество, которое будет содержать единица измерения.</span><span class="sxs-lookup"><span data-stu-id="f93c4-119">In the **QUantity** field, enter the quantity that the unit will contain.</span></span> <span data-ttu-id="f93c4-120">Например, если в коробке находится две штуки, введите "2".</span><span class="sxs-lookup"><span data-stu-id="f93c4-120">For example, if a box contains two pieces, enter "2".</span></span> 
4. <span data-ttu-id="f93c4-121">В поле **Базовая единица измерения** выберите базовую единицу измерения, чтобы установить наименьшую единицу измерения для данной единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="f93c4-121">In the **Base unit** field, select a base unit to establish the lowest unit of measurement for the unit.</span></span> <span data-ttu-id="f93c4-122">Например, вы можете выбрать "Штука".</span><span class="sxs-lookup"><span data-stu-id="f93c4-122">For example, you might select "Piece".</span></span>
5. <span data-ttu-id="f93c4-123">Выберите **Сохранить**:</span><span class="sxs-lookup"><span data-stu-id="f93c4-123">Select **Save**:</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]