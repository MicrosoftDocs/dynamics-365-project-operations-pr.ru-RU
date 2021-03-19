---
title: Синхронизация категорий расходов по проекту между Finance and Operations и Project Service Automation
description: В этой теме описаны шаблоны и базовые задачи, которые используются для синхронизации категорий расходов по проекту между Microsoft Dynamics 365 Finance и Dynamics 365 Project Service Automation.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 4abb7fe6554825b97df4cc04ee1b02d731cb4af9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289655"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="b60d8-103">Синхронизация категорий расходов по проекту между Finance and Operations и Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="b60d8-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b60d8-104">В этой теме описаны шаблоны и базовые задачи, которые используются для синхронизации категорий расходов по проекту между Dynamics 365 Finance и Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="b60d8-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Dynamics 365 Finance and Dynamics 365 Project Service Automation.</span></span>

> [!NOTE]
> - <span data-ttu-id="b60d8-105">Интеграция задач проекта, категории транзакций расходов, оценки часов, оценки расходов и блокировка функций доступны в версии 8.0.</span><span class="sxs-lookup"><span data-stu-id="b60d8-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="b60d8-106">Интеграция фактических данных по проекту доступна в версии 8.0.1 и последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="b60d8-106">Actuals integration is available in version 8.0.1 or later.</span></span>
> - <span data-ttu-id="b60d8-107">Если вы используете версию Enterprise Edition 7.3.0 после установки KB 4132657 и KB 4132660, вы сможете использовать шаблоны для интеграции задач проекта, категорий транзакций расходов, часовых оценок, оценок расходов и фактических данных, а также для настройки блокировки функций.</span><span class="sxs-lookup"><span data-stu-id="b60d8-107">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="b60d8-108">Если вам необходимо сбросить распределения по счетам, мы рекомендуем также установить KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="b60d8-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance"></a><span data-ttu-id="b60d8-109">Поток данных для Project Service Automation и Finance</span><span class="sxs-lookup"><span data-stu-id="b60d8-109">Data flow for Project Service Automation and Finance</span></span>

<span data-ttu-id="b60d8-110">Решение для интеграции Project Service Automation и Finance использует функцию интеграции данных для синхронизации данных между экземплярами Project Service Automation и Finance.</span><span class="sxs-lookup"><span data-stu-id="b60d8-110">The Project Service Automation and Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="b60d8-111">Шаблоны интеграции, доступные с функцией интеграции данных, позволяют передавать данные о категориях транзакций по расходам проекта между Finance и Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="b60d8-111">The integration templates that are available with the Data integration feature enable the flow of data about project expense transaction categories between Finance and Project Service Automation.</span></span>

<span data-ttu-id="b60d8-112">Если категории расходов по проекту заданы в Finance, сначала выполняется интеграция из Finance в Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="b60d8-112">If the project expense categories are mastered in Finance, the integration flow is first from Finance to Project Service Automation.</span></span> <span data-ttu-id="b60d8-113">Затем идентификаторы интеграции категорий расходов проекта обновляются посредством синхронизации из Project Service Automation в Finance.</span><span class="sxs-lookup"><span data-stu-id="b60d8-113">The integration IDs of the project expense categories are then updated through synchronization from Project Service Automation to Finance.</span></span>

<span data-ttu-id="b60d8-114">Если категории расходов по проекту заданы в Project Service Automation, сначала выполняется интеграция из Project Service Automation в Finance.</span><span class="sxs-lookup"><span data-stu-id="b60d8-114">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance.</span></span> <span data-ttu-id="b60d8-115">Категории проектов должны быть уже настроены в Finance перед синхронизацией из Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="b60d8-115">The project categories must already be configured in Finance before the synchronization from Project Service Automation.</span></span> <span data-ttu-id="b60d8-116">Затем выполните синхронизацию из Finance обратно в Project Service Automation, а затем из Project Service Automation снова в Finance.</span><span class="sxs-lookup"><span data-stu-id="b60d8-116">Then synchronize from Finance back to Project Service Automation, and then from Project Service Automation to Finance again.</span></span> <span data-ttu-id="b60d8-117">Таким образом, вы гарантируете, что категории связаны и что дубликаты не будут созданы.</span><span class="sxs-lookup"><span data-stu-id="b60d8-117">In this way, you help guarantee that the categories are linked, and that no duplicates are created.</span></span>

> [!NOTE]
> <span data-ttu-id="b60d8-118">Обычно категории расходов по проекту управляются в Finance.</span><span class="sxs-lookup"><span data-stu-id="b60d8-118">Typically, the project expense categories are mastered in Finance.</span></span> <span data-ttu-id="b60d8-119">Однако, если это не так или если категории расходов уже были созданы в Project Service Automation, необходимо сначала выполнить синхронизацию с помощью шаблона категорий транзакций расходов проекта (из PSA в Fin and Ops).</span><span class="sxs-lookup"><span data-stu-id="b60d8-119">However, if they aren't, or if expense categories have already been created in Project Service Automation, you must first synchronize by using the Project expense transaction categories (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="b60d8-120">Затем выполните синхронизацию с помощью шаблона категорий расходов по проекту (из Fin and Ops в PSA).</span><span class="sxs-lookup"><span data-stu-id="b60d8-120">Then synchronize by using the Project expense transaction categories (Fin and Ops to PSA) template.</span></span> <span data-ttu-id="b60d8-121">Затем вам следует запустить синхронизацию из Project Service Automation в Finance еще раз.</span><span class="sxs-lookup"><span data-stu-id="b60d8-121">You should then run the synchronization from Project Service Automation to Finance one more time.</span></span>
>
> <span data-ttu-id="b60d8-122">Если вы сначала выполняете синхронизацию из Project Service Automation, перед запуском синхронизации в Finance должны быть выполнены следующие требования:</span><span class="sxs-lookup"><span data-stu-id="b60d8-122">If you synchronize first from Project Service Automation, the following requirements must be met in Finance before the synchronization is run:</span></span>
>
> - <span data-ttu-id="b60d8-123">Общая категория, соответствующая категории проекта, настроенной в Project Service Automation, должна существовать, и она должна быть включена для обоих **Проект** и **Расходы**.</span><span class="sxs-lookup"><span data-stu-id="b60d8-123">The shared category that matches the project category that is set up in Project Service Automation must exist, and it must be enabled for both **Project** and **Expense**.</span></span>
> - <span data-ttu-id="b60d8-124">Для каждого юридического лица Finance, с которым необходимо выполнить интеграцию, должны существовать следующие категории проектов:</span><span class="sxs-lookup"><span data-stu-id="b60d8-124">For each Finance legal entity that must be integrated with, the following project categories must exist:</span></span>
>
>     - <span data-ttu-id="b60d8-125">**Категория проекта** существует.</span><span class="sxs-lookup"><span data-stu-id="b60d8-125">**Project category** exists.</span></span> 
>     - <span data-ttu-id="b60d8-126">**Использование в расходах** включено.</span><span class="sxs-lookup"><span data-stu-id="b60d8-126">**Use in Expense** is enabled.</span></span>
>     - <span data-ttu-id="b60d8-127">**Активно в журнале** включено.</span><span class="sxs-lookup"><span data-stu-id="b60d8-127">**Active in journal** is enabled.</span></span>
>     - <span data-ttu-id="b60d8-128">**Тип операции** задано как **Расходы**.</span><span class="sxs-lookup"><span data-stu-id="b60d8-128">**Transaction type** is set to **Expense**.</span></span>

<span data-ttu-id="b60d8-129">На следующем рисунке показано, как данные синхронизируются между Project Service Automation и Finance.</span><span class="sxs-lookup"><span data-stu-id="b60d8-129">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="b60d8-130">[![Поток данных для интеграции Project Service Automation с Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="b60d8-130">[![Data flow for Project Service Automation integration with Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a><span data-ttu-id="b60d8-131">Синхронизация категорий расходов по проекту между из Finance в Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="b60d8-131">Project expense category synchronization from Finance to Project Service Automation</span></span>

### <a name="template-and-task"></a><span data-ttu-id="b60d8-132">Шаблон и задача</span><span class="sxs-lookup"><span data-stu-id="b60d8-132">Template and task</span></span>

<span data-ttu-id="b60d8-133">Чтобы получить доступ к шаблону, в центре администрирования Microsoft Power Apps выберите **Проекты**, а затем в правом верхнем углу выберите **Создать проект** для выбора общедоступных шаблонов.</span><span class="sxs-lookup"><span data-stu-id="b60d8-133">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="b60d8-134">Следующий шаблон и базовая задача используются для синхронизации категорий расходов по проекту из Finance в Project Service Automation:</span><span class="sxs-lookup"><span data-stu-id="b60d8-134">The following template and underlying task are used to synchronize project expense categories from Finance to Project Service Automation:</span></span>

- <span data-ttu-id="b60d8-135">**Название шаблона в интеграции данных:** Категории транзакций расходов по проекту (из Fin and Ops в PSA)</span><span class="sxs-lookup"><span data-stu-id="b60d8-135">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
- <span data-ttu-id="b60d8-136">**Название задачи в проекте:** синхронизировать категории с PSA</span><span class="sxs-lookup"><span data-stu-id="b60d8-136">**Name of the task in the project:** Sync categories to PSA</span></span>

### <a name="entity-set"></a><span data-ttu-id="b60d8-137">Набор сущностей</span><span class="sxs-lookup"><span data-stu-id="b60d8-137">Entity set</span></span>

| <span data-ttu-id="b60d8-138">Финансы</span><span class="sxs-lookup"><span data-stu-id="b60d8-138">Finance</span></span>                           | <span data-ttu-id="b60d8-139">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="b60d8-139">Project Service Automation</span></span> |
|-----------------------------------|----------------------------|
| <span data-ttu-id="b60d8-140">Сущность интеграции для категорий</span><span class="sxs-lookup"><span data-stu-id="b60d8-140">Integration entity for categories</span></span> | <span data-ttu-id="b60d8-141">Категории транзакций</span><span class="sxs-lookup"><span data-stu-id="b60d8-141">Transaction categories</span></span>     |

### <a name="entity-flow"></a><span data-ttu-id="b60d8-142">Поток сущностей</span><span class="sxs-lookup"><span data-stu-id="b60d8-142">Entity flow</span></span>

<span data-ttu-id="b60d8-143">Категории расходов по проекту управляются в Finance и синхронизируются с Project Service Automation как категории транзакций.</span><span class="sxs-lookup"><span data-stu-id="b60d8-143">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="b60d8-144">Power Query</span><span class="sxs-lookup"><span data-stu-id="b60d8-144">Power Query</span></span>

<span data-ttu-id="b60d8-145">При синхронизации с Project Service Automation необходимо использовать Microsoft Power Query для Excel, чтобы задать тип выставления счетов для категории транзакции.</span><span class="sxs-lookup"><span data-stu-id="b60d8-145">When you're synchronizing to Project Service Automation, you must use Microsoft Power Query for Excel to set the billing type on the transaction category.</span></span> <span data-ttu-id="b60d8-146">В шаблоне категорий транзакций расходов по проекту (из Fin and Ops в PSA) есть столбец и сопоставление по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b60d8-146">The Project expense transaction categories (Fin and Ops to PSA) template provides a default column and mapping.</span></span> <span data-ttu-id="b60d8-147">Если вы создаете свой собственный шаблон, вы должны добавить условный столбец в Power Query.</span><span class="sxs-lookup"><span data-stu-id="b60d8-147">If you create your own template, you must add a conditional column in Power Query.</span></span> <span data-ttu-id="b60d8-148">Выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="b60d8-148">Follow these steps.</span></span>

1. <span data-ttu-id="b60d8-149">Щелкните стрелку, чтобы открыть сопоставление задачи категорий расходов проекта в шаблоне категорий транзакций расходов проекта (из Fin and Ops в PSA).</span><span class="sxs-lookup"><span data-stu-id="b60d8-149">Click the arrow to open the mapping of the project expense categories task in the Project expense transaction categories (Fin and Ops to PSA) template.</span></span>
2. <span data-ttu-id="b60d8-150">Щелкните ссылку **Расширенный запрос и фильтрация** для открытия Power Query.</span><span class="sxs-lookup"><span data-stu-id="b60d8-150">Click the **Advance Query and Filtering** link to open Power Query.</span></span>
2. <span data-ttu-id="b60d8-151">Выберите **Добавить условный столбец**.</span><span class="sxs-lookup"><span data-stu-id="b60d8-151">Select **Add Conditional Column**.</span></span>
3. <span data-ttu-id="b60d8-152">Введите имя для нового столбца, например **BillingType**.</span><span class="sxs-lookup"><span data-stu-id="b60d8-152">Enter a name for the new column, such as **BillingType**.</span></span>
4. <span data-ttu-id="b60d8-153">Введите следующее условие: **если CATEGORYID не равно нулю, то 19235001, в противном случае null**.</span><span class="sxs-lookup"><span data-stu-id="b60d8-153">Enter the following condition: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
5. <span data-ttu-id="b60d8-154">Нажмите **ОК** в столбце.</span><span class="sxs-lookup"><span data-stu-id="b60d8-154">Click **OK** on the column.</span></span>
6. <span data-ttu-id="b60d8-155">Обязательно сопоставьте этот новый столбец на странице сопоставления.</span><span class="sxs-lookup"><span data-stu-id="b60d8-155">Be sure to map this new column on the mapping page.</span></span>

<span data-ttu-id="b60d8-156">На следующих рисунках показан пример сопоставления задач шаблона в интеграции данных.</span><span class="sxs-lookup"><span data-stu-id="b60d8-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="b60d8-157">В сопоставлении отображается информация о полях, которые будут синхронизированы из Finance в Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="b60d8-157">The mapping shows the field information that will be synchronized from Finance to Project Service Automation.</span></span>

<span data-ttu-id="b60d8-158">[![Сопоставление категорий расходов по проекту с шаблоном Project Service Automation](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="b60d8-158">[![Project expense category to Project Service Automation template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a><span data-ttu-id="b60d8-159">Синхронизация категорий расходов по проекту между из Project Service Automation в Finance</span><span class="sxs-lookup"><span data-stu-id="b60d8-159">Project expense category synchronization from Project Service Automation to Finance</span></span>

### <a name="template-and-task"></a><span data-ttu-id="b60d8-160">Шаблон и задача</span><span class="sxs-lookup"><span data-stu-id="b60d8-160">Template and task</span></span>

<span data-ttu-id="b60d8-161">Следующий шаблон и базовая задача используются для синхронизации категорий расходов по проекту из Project Service Automation в Finance:</span><span class="sxs-lookup"><span data-stu-id="b60d8-161">The following template and underlying task are used to synchronize project expense categories from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="b60d8-162">**Название шаблона в интеграции данных:** Категории транзакций расходов по проекту (из PSA в Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="b60d8-162">**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="b60d8-163">**Название задачи в проекте:** синхронизировать категории с Fin Ops</span><span class="sxs-lookup"><span data-stu-id="b60d8-163">**Name of the task in the project:** Sync categories to Fin Ops</span></span>

### <a name="entity-set"></a><span data-ttu-id="b60d8-164">Набор сущностей</span><span class="sxs-lookup"><span data-stu-id="b60d8-164">Entity set</span></span>

| <span data-ttu-id="b60d8-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="b60d8-165">Project Service Automation</span></span> | <span data-ttu-id="b60d8-166">Финансы</span><span class="sxs-lookup"><span data-stu-id="b60d8-166">Finance</span></span>                           |
|----------------------------|-----------------------------------|
| <span data-ttu-id="b60d8-167">Категории транзакций</span><span class="sxs-lookup"><span data-stu-id="b60d8-167">Transaction categories</span></span>     | <span data-ttu-id="b60d8-168">Сущность интеграции для категорий</span><span class="sxs-lookup"><span data-stu-id="b60d8-168">Integration entity for categories</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="b60d8-169">Поток сущностей</span><span class="sxs-lookup"><span data-stu-id="b60d8-169">Entity flow</span></span>

<span data-ttu-id="b60d8-170">Категории расходов по проекту управляются в Finance и синхронизируются с Project Service Automation как категории транзакций.</span><span class="sxs-lookup"><span data-stu-id="b60d8-170">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="b60d8-171">При синхронизации обратно с Finance обновляется категория проекта в Finance с кодом интеграции из Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="b60d8-171">The synchronization back to Finance updates the project category in Finance with the integration ID from Project Service Automation.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="b60d8-172">Сопоставление шаблонов в интеграции данных</span><span class="sxs-lookup"><span data-stu-id="b60d8-172">Template mapping in Data integration</span></span>

<span data-ttu-id="b60d8-173">На следующих рисунках показан пример сопоставления задач шаблона в интеграции данных.</span><span class="sxs-lookup"><span data-stu-id="b60d8-173">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="b60d8-174">В сопоставлении отображается информация о полях, которые будут синхронизированы из Project Service Automation в Finance.</span><span class="sxs-lookup"><span data-stu-id="b60d8-174">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="b60d8-175">[![Сопоставление Project Service Automation с шаблоном Finance](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="b60d8-175">[![Project Service Automation to Finance template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]