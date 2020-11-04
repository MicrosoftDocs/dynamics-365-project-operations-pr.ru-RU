---
title: Настройка категорий расходов
description: Эта тема предоставляет информацию о том, как настроить категории расходов и общие категории для отчетов о расходах.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: f051d70f3dfe3b241dc0a206c0cdfda000f87c76
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083078"
---
# <a name="set-up-expense-categories"></a><span data-ttu-id="6db66-103">Настройка категорий расходов</span><span class="sxs-lookup"><span data-stu-id="6db66-103">Set up expense categories</span></span>

<span data-ttu-id="6db66-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/без запасов_</span><span class="sxs-lookup"><span data-stu-id="6db66-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="6db66-105">Когда сотрудники создают отчеты о расходах, все регистрируемые ими расходы должны быть связаны с категорией расходов.</span><span class="sxs-lookup"><span data-stu-id="6db66-105">When employees create expense reports, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="6db66-106">Категории расходов являются производными от общих категорий, которые могут совместно использоваться юридическими лицами в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="6db66-106">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="6db66-107">В зависимости от того, как определена ваша организация, эти категории расходов также могут совместно использоваться в других областях.</span><span class="sxs-lookup"><span data-stu-id="6db66-107">Depending on how your organization is defined, these expense categories can also be shared in other areas.</span></span> <span data-ttu-id="6db66-108">Основываясь на определении вашей организации и руководящих указаниях от группы внедрения, вы должны определить, будут ли категории, используемые в управлении расходами, использоваться только в управлении расходами или должны совместно использоваться в других областях.</span><span class="sxs-lookup"><span data-stu-id="6db66-108">Based on the definition of your organization and guidance from the implementation team, you must determine whether the categories that are used in Expense management will be used only in Expense management or should be shared in other areas.</span></span>

> [!NOTE]
> <span data-ttu-id="6db66-109">Эти категории могут использоваться совместно в модуле управления проектами и учетом и модуле управления расходами или в модуле управлением проектами и учетом и модуле производства.</span><span class="sxs-lookup"><span data-stu-id="6db66-109">These categories can be shared between Project management and accounting and Expense management, or between Project management and accounting and Production.</span></span> <span data-ttu-id="6db66-110">Однако их нельзя совместно использовать в модуле управления расходами и модуле производства.</span><span class="sxs-lookup"><span data-stu-id="6db66-110">However, they can't be shared between Expense management and Production.</span></span>

<span data-ttu-id="6db66-111">Прежде чем вы сможете начать процесс настройки, необходимо принять следующие решения для каждой категории расходов:</span><span class="sxs-lookup"><span data-stu-id="6db66-111">Before you can begin the setup process, the following decisions must be made for each expense category:</span></span>

- <span data-ttu-id="6db66-112">Что такое категория расходов?</span><span class="sxs-lookup"><span data-stu-id="6db66-112">What is the expense category?</span></span> <span data-ttu-id="6db66-113">Примеры включают категории для билетов на самолет, проживания в гостиницах или пробега.</span><span class="sxs-lookup"><span data-stu-id="6db66-113">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="6db66-114">Можно ли использовать категорию расходов в управлении проектами и бухгалтерском учете?</span><span class="sxs-lookup"><span data-stu-id="6db66-114">Can the expense category also be used in Project management and accounting?</span></span> <span data-ttu-id="6db66-115">Если можно, необходимо также принять следующие решения:</span><span class="sxs-lookup"><span data-stu-id="6db66-115">If it can, you must also make the following decisions:</span></span>

    - <span data-ttu-id="6db66-116">Какие счета затрат будут использоваться для следующих расходов?</span><span class="sxs-lookup"><span data-stu-id="6db66-116">Which cost accounts will be used for the following expenses?</span></span>

        - <span data-ttu-id="6db66-117">Себестоимость</span><span class="sxs-lookup"><span data-stu-id="6db66-117">Cost</span></span>
        - <span data-ttu-id="6db66-118">Распределение заработной платы</span><span class="sxs-lookup"><span data-stu-id="6db66-118">Payroll allocation</span></span>
        - <span data-ttu-id="6db66-119">НЗП - Себестоимость</span><span class="sxs-lookup"><span data-stu-id="6db66-119">WIP-cost value</span></span>
        - <span data-ttu-id="6db66-120">Себестоимость - Номенклатура</span><span class="sxs-lookup"><span data-stu-id="6db66-120">Cost-item</span></span>
        - <span data-ttu-id="6db66-121">НЗП - Себестоимость - Номенклатура</span><span class="sxs-lookup"><span data-stu-id="6db66-121">WIP-cost value-item</span></span>
        - <span data-ttu-id="6db66-122">Начисленный убыток</span><span class="sxs-lookup"><span data-stu-id="6db66-122">Accrued loss</span></span>
        - <span data-ttu-id="6db66-123">НЗП - Начисленный убыток</span><span class="sxs-lookup"><span data-stu-id="6db66-123">WIP-accrued loss</span></span>

    - <span data-ttu-id="6db66-124">Какие счета доходов будут использоваться для следующих источников выручки?</span><span class="sxs-lookup"><span data-stu-id="6db66-124">Which revenue accounts will be used for the following sources of revenue?</span></span>

        - <span data-ttu-id="6db66-125">Выручка по выставленным накладным</span><span class="sxs-lookup"><span data-stu-id="6db66-125">Invoiced revenue</span></span>
        - <span data-ttu-id="6db66-126">Начисленная выручка - Сумма реализации</span><span class="sxs-lookup"><span data-stu-id="6db66-126">Accrued revenue-sales value</span></span>
        - <span data-ttu-id="6db66-127">НЗП - сумма реализации</span><span class="sxs-lookup"><span data-stu-id="6db66-127">WIP-sales value</span></span>
        - <span data-ttu-id="6db66-128">Начисленная выручка - производство</span><span class="sxs-lookup"><span data-stu-id="6db66-128">Accrued revenue-production</span></span>
        - <span data-ttu-id="6db66-129">НЗП - производство</span><span class="sxs-lookup"><span data-stu-id="6db66-129">WIP-production</span></span>
        - <span data-ttu-id="6db66-130">Начисленная выручка - прибыль</span><span class="sxs-lookup"><span data-stu-id="6db66-130">Accrued revenue-profit</span></span>
        - <span data-ttu-id="6db66-131">НЗП- прибыль</span><span class="sxs-lookup"><span data-stu-id="6db66-131">WIP-profit</span></span>
        - <span data-ttu-id="6db66-132">Начисленная выручка - подписка</span><span class="sxs-lookup"><span data-stu-id="6db66-132">Accrued revenue-subscription</span></span>
        - <span data-ttu-id="6db66-133">НЗП - подписка</span><span class="sxs-lookup"><span data-stu-id="6db66-133">WIP-subscription</span></span>

- <span data-ttu-id="6db66-134">Что такое тип расходов?</span><span class="sxs-lookup"><span data-stu-id="6db66-134">What is the expense type?</span></span>
- <span data-ttu-id="6db66-135">Какой метод оплаты используется по умолчанию для категории расходов?</span><span class="sxs-lookup"><span data-stu-id="6db66-135">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="6db66-136">Нужна ли детализация расходов в категории расходов?</span><span class="sxs-lookup"><span data-stu-id="6db66-136">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="6db66-137">Какой основной счет используется по умолчанию для категории расходов?</span><span class="sxs-lookup"><span data-stu-id="6db66-137">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="6db66-138">Какая группа налога с продаж товаров используется по умолчанию для категории расходов?</span><span class="sxs-lookup"><span data-stu-id="6db66-138">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="6db66-139">Допускаются ли дополнительные способы оплаты для категории расходов?</span><span class="sxs-lookup"><span data-stu-id="6db66-139">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="6db66-140">Если да, то какие?</span><span class="sxs-lookup"><span data-stu-id="6db66-140">If so, what are they?</span></span>
- <span data-ttu-id="6db66-141">Есть ли в этой категории расходов подкатегории?</span><span class="sxs-lookup"><span data-stu-id="6db66-141">Are there subcategories in this expense category?</span></span> <span data-ttu-id="6db66-142">Если есть подкатегории, необходимо также принять следующие решения:</span><span class="sxs-lookup"><span data-stu-id="6db66-142">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="6db66-143">Исключаются ли какие-либо подкатегории из налогового возмещения?</span><span class="sxs-lookup"><span data-stu-id="6db66-143">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="6db66-144">Какова налоговая группа номенклатур в подкатегориях?</span><span class="sxs-lookup"><span data-stu-id="6db66-144">What is the item sales tax group of the subcategories?</span></span>
