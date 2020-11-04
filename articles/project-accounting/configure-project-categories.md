---
title: Настройка категорий проектов
description: В этом разделе представлена информация о настройке категорий проектов.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 84033182ce047d230724409eef9bc6afcaefd2b4
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083084"
---
# <a name="configure-project-categories"></a><span data-ttu-id="d413a-103">Настройка категорий проектов</span><span class="sxs-lookup"><span data-stu-id="d413a-103">Configure project categories</span></span>

<span data-ttu-id="d413a-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/без запасов_</span><span class="sxs-lookup"><span data-stu-id="d413a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="d413a-105">Project Operations предлагает надежные возможности для категоризации доходов и расходов по проектам.</span><span class="sxs-lookup"><span data-stu-id="d413a-105">Project Operations offers robust capabilities for categorizing revenue and expenses on projects.</span></span> <span data-ttu-id="d413a-106">Категории предоставляют возможность составлять отчеты и анализировать транзакции по проекту, а также определять разноску в главную книгу.</span><span class="sxs-lookup"><span data-stu-id="d413a-106">Categories provide the ability to report on and analyze project transactions, and drive posting to the general ledger.</span></span>

<span data-ttu-id="d413a-107">На следующей диаграмме показана корреляция между категориями транзакций, общими категориями и категориями проектов.</span><span class="sxs-lookup"><span data-stu-id="d413a-107">The following diagram illustrates the correlation between transaction categories, shared categories, and project categories.</span></span> 

<span data-ttu-id="d413a-108">Категории транзакций — это основная группа для транзакций проекта.</span><span class="sxs-lookup"><span data-stu-id="d413a-108">Transaction categories are the basic grouping for project transactions.</span></span> <span data-ttu-id="d413a-109">Внутри этой группы есть набор общих категорий, которые могут совместно использоваться приложениями и модулями.</span><span class="sxs-lookup"><span data-stu-id="d413a-109">Within that grouping, there is a set of shared categories that can be shared across applications and modules.</span></span> <span data-ttu-id="d413a-110">Если углубиться в специфику, категории проектов являются наиболее детализированным уровнем категорий.</span><span class="sxs-lookup"><span data-stu-id="d413a-110">Getting even further into specifics, project categories are the most granular level of categories.</span></span> <span data-ttu-id="d413a-111">Категории проектов зависят от юридического лица, модуля и приложения.</span><span class="sxs-lookup"><span data-stu-id="d413a-111">Project categories are specific to legal entity, module, and application.</span></span>

![Корреляция между категориями транзакций, общими категориями и категориями проектов](media/project-categories.png)

## <a name="transaction-categories"></a><span data-ttu-id="d413a-113">Категории транзакций</span><span class="sxs-lookup"><span data-stu-id="d413a-113">Transaction categories</span></span>

<span data-ttu-id="d413a-114">Категории транзакций представляют собой базовую группу для транзакций проекта и не зависят от компании или типа транзакции.</span><span class="sxs-lookup"><span data-stu-id="d413a-114">Transaction categories represent the basic grouping for project transactions and are not company or transaction type-specific.</span></span> <span data-ttu-id="d413a-115">Например, Contoso Robotics использует категории "Проект", "Поездки", "Установка" и "Транзакция службы" для группировки транзакций проекта.</span><span class="sxs-lookup"><span data-stu-id="d413a-115">For example, Contoso Robotics uses Design, Travel, Installation, and Service Transaction categories to group Project transactions.</span></span>

<span data-ttu-id="d413a-116">Категории транзакций определены в модуле Project Operations.</span><span class="sxs-lookup"><span data-stu-id="d413a-116">Transaction categories are defined in the Project Operations module.</span></span> 
1. <span data-ttu-id="d413a-117">Чтобы открыть форму, перейдите в раздел **Параметры** \> **Категории транзакций**.</span><span class="sxs-lookup"><span data-stu-id="d413a-117">Go to **Settings** \> **Transaction Categories** to open the form.</span></span> 
2. <span data-ttu-id="d413a-118">Создайте новую категорию транзакции, выбрав **Создать** или выбрав **Импорт из Excel**.</span><span class="sxs-lookup"><span data-stu-id="d413a-118">Create a new transaction category either by selecting **New** or by selecting **Import from Excel**.</span></span>

## <a name="shared-categories"></a><span data-ttu-id="d413a-119">Общие категории</span><span class="sxs-lookup"><span data-stu-id="d413a-119">Shared categories</span></span>

<span data-ttu-id="d413a-120">Dynamics 365 использует концепцию общих категорий для категоризации расходов в различных приложениях, таких как Dynamics 365 Finance, Dynamics 365 Supply Chain и Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="d413a-120">Dynamics 365 uses the Shared categories concept to categorize expenses in different applications, such as Dynamics 365 Finance, Dynamics 365 Supply Chain, and Dynamics 365 Project Operations.</span></span> <span data-ttu-id="d413a-121">Для каждой созданной категории транзакций Project Operations автоматически создает четыре связанные общие категории: часы, расходы, сборы и номенклатура.</span><span class="sxs-lookup"><span data-stu-id="d413a-121">For each Transaction category created, Project Operations automatically creates four related Shared categories: Hours, Expense, Fees, and Item.</span></span> <span data-ttu-id="d413a-122">Вы можете просмотреть и настроить общие категории, перейдя в раздел **Управление проектами и учет** \> **Настройка** \> **Категории** \> **Общие категории**.</span><span class="sxs-lookup"><span data-stu-id="d413a-122">You can review and adjust the shared categories by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Shared Categories**.</span></span>

## <a name="project-categories"></a><span data-ttu-id="d413a-123">Категории проектов</span><span class="sxs-lookup"><span data-stu-id="d413a-123">Project categories</span></span>

<span data-ttu-id="d413a-124">Категории проектов представляют собой наиболее детализированный уровень конфигурации категорий и должны настраиваться отдельно и для каждой компании бухгалтером проекта.</span><span class="sxs-lookup"><span data-stu-id="d413a-124">Project categories represent most granular level of category configuration and must be configured separately, and for each company, by a Project accountant.</span></span>

1. <span data-ttu-id="d413a-125">Перейдите в раздел **Управление проектами и учет** \> **Настройка** \> **Категории** \> **Категории проектов**.</span><span class="sxs-lookup"><span data-stu-id="d413a-125">Go to **Project Management and Accounting** \> **Setup** \> **Categories** \> **Project categories**.</span></span>
2. <span data-ttu-id="d413a-126">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="d413a-126">Select **New**.</span></span>
3. <span data-ttu-id="d413a-127">Выберите **Код категории** для общей категории, которую вы создали в предыдущем разделе.</span><span class="sxs-lookup"><span data-stu-id="d413a-127">Select the **Category ID** of the Shared category you created in the previous section.</span></span> <span data-ttu-id="d413a-128">Project Operations позволяет использовать только те общие категории, которые связаны с категориями транзакций.</span><span class="sxs-lookup"><span data-stu-id="d413a-128">Project Operations allows using only those shared categories that are associated with transaction categories.</span></span>
4. <span data-ttu-id="d413a-129">Выберите группу категорий.</span><span class="sxs-lookup"><span data-stu-id="d413a-129">Select a category group.</span></span>

## <a name="category-groups"></a><span data-ttu-id="d413a-130">Группы категорий</span><span class="sxs-lookup"><span data-stu-id="d413a-130">Category groups</span></span>

<span data-ttu-id="d413a-131">Группы категорий используются для совместного использования свойств, в первую очередь профилей разности, между связанными категориями проектов.</span><span class="sxs-lookup"><span data-stu-id="d413a-131">Category groups are used to share properties, primarily posting profiles, between related Project categories.</span></span> <span data-ttu-id="d413a-132">Для каждого типа транзакции должна быть как минимум одна группа категорий, и каждой категории проекта назначается группа.</span><span class="sxs-lookup"><span data-stu-id="d413a-132">There must be at least one category group for each transaction type and each project category is assigned a group.</span></span>

<span data-ttu-id="d413a-133">Спецификации разноски в Project Operations определяются правилами профилей затрат и доходов проекта, категориями проектов и группами категорий.</span><span class="sxs-lookup"><span data-stu-id="d413a-133">The posting specifications in Project Operations are defined by the project cost and revenue profile rules, project categories, and category groups.</span></span> <span data-ttu-id="d413a-134">Вы можете настроить группы категорий, перейдя в раздел **Управление проектами и учетом** \> **Настройка** \> **Категории** \> **Группы категорий**.</span><span class="sxs-lookup"><span data-stu-id="d413a-134">You can set up category groups by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Category groups**.</span></span>
