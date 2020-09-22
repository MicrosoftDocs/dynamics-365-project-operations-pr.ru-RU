---
title: Синхронизируйте оценки проекта напрямую из Project Service Automation с Finance and Operations
description: В этой теме описаны шаблоны и базовые задачи, которые используются для синхронизации оценок часов проекта и оценки расходов по проекту непосредственно из Microsoft Dynamics 365 Project Service Automation с Dynamics 365 Finance.
author: KimANelson
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
ms.assetid: d688ce9a-41e3-4ebe-952e-700f8351fbe9
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: a24a967d82c2e005e61234d34da8a583b61ff7b1
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754944"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="c3537-103">Синхронизируйте оценки проекта напрямую из Project Service Automation с Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c3537-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c3537-104">В этой теме описаны шаблоны и базовые задачи, которые используются для синхронизации оценок часов проекта и оценки расходов по проекту непосредственно из Dynamics 365 Project Service Automation с Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="c3537-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="c3537-105">Интеграция задач проекта, категории транзакций расходов, оценки часов, оценки расходов и блокировка функций доступны в версии 8.0.</span><span class="sxs-lookup"><span data-stu-id="c3537-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in version 8.0.</span></span>
> - <span data-ttu-id="c3537-106">Интеграция фактических данных по проекту доступна в версии 8.0.1 и последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="c3537-106">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="c3537-107">Поток данных для Project Service Automation в Finance</span><span class="sxs-lookup"><span data-stu-id="c3537-107">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="c3537-108">Решение для интеграции Project Service Automation в Finance использует функцию интеграции данных для синхронизации данных между экземплярами Project Service Automation и Finance.</span><span class="sxs-lookup"><span data-stu-id="c3537-108">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="c3537-109">Шаблоны интеграции, доступные с функцией интеграции данных, позволяют передавать данные об оценках часов проекта и оценках расходов по проекту из Project Service Automation в Finance.</span><span class="sxs-lookup"><span data-stu-id="c3537-109">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance.</span></span>

<span data-ttu-id="c3537-110">На следующем рисунке показано, как данные синхронизируются между Project Service Automation и Finance.</span><span class="sxs-lookup"><span data-stu-id="c3537-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="c3537-111">[![Поток данных для интеграции Project Service Automation с Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="c3537-111">[![Data flow for Project Service Automation integration with Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="c3537-112">Оценки часов проекта</span><span class="sxs-lookup"><span data-stu-id="c3537-112">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="c3537-113">Шаблон и задачи</span><span class="sxs-lookup"><span data-stu-id="c3537-113">Template and tasks</span></span>

<span data-ttu-id="c3537-114">Чтобы получить доступ к доступным шаблонам, в центре администрирования Microsoft Power Apps выберите **Проекты**, а затем в правом верхнем углу выберите **Создать проект** для выбора общедоступных шаблонов.</span><span class="sxs-lookup"><span data-stu-id="c3537-114">To access the available templates, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="c3537-115">Следующий шаблон и базовые задачи используются для синхронизации оценок часов проекта из Project Service Automation в Finance:</span><span class="sxs-lookup"><span data-stu-id="c3537-115">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="c3537-116">**Название шаблона в интеграции данных:** оценки часов проекта (из PSA в Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="c3537-116">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="c3537-117">**Название задач в проекте:**</span><span class="sxs-lookup"><span data-stu-id="c3537-117">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="c3537-118">Отношения транзакций</span><span class="sxs-lookup"><span data-stu-id="c3537-118">Transaction relationships</span></span>
    - <span data-ttu-id="c3537-119">Оценки расходов</span><span class="sxs-lookup"><span data-stu-id="c3537-119">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="c3537-120">Набор сущностей</span><span class="sxs-lookup"><span data-stu-id="c3537-120">Entity set</span></span>

| <span data-ttu-id="c3537-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="c3537-121">Project Service Automation</span></span> | <span data-ttu-id="c3537-122">Финансы</span><span class="sxs-lookup"><span data-stu-id="c3537-122">Finance</span></span>                                       |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="c3537-123">Задачи проекта</span><span class="sxs-lookup"><span data-stu-id="c3537-123">Project tasks</span></span>              | <span data-ttu-id="c3537-124">Сущность интеграции для оценок часов проекта</span><span class="sxs-lookup"><span data-stu-id="c3537-124">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="c3537-125">Поток сущностей</span><span class="sxs-lookup"><span data-stu-id="c3537-125">Entity flow</span></span>

<span data-ttu-id="c3537-126">Оценки часов проекта управляются в Project Service Automation и синхронизируются с Finance как прогнозы часов проекта.</span><span class="sxs-lookup"><span data-stu-id="c3537-126">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="c3537-127">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="c3537-127">Prerequisites</span></span>

<span data-ttu-id="c3537-128">Перед синхронизацией оценок часов проекта необходимо синхронизировать проекты, задачи проекта и категории транзакций расходов по проекту.</span><span class="sxs-lookup"><span data-stu-id="c3537-128">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="c3537-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="c3537-129">Power Query</span></span>

<span data-ttu-id="c3537-130">В шаблоне оценок часов проекта необходимо использовать Microsoft Power Query для Excel для выполнения следующих задач:</span><span class="sxs-lookup"><span data-stu-id="c3537-130">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="c3537-131">Установите идентификатор модели прогноза по умолчанию, который будет использоваться, когда интеграция создает новые часовые прогнозы.</span><span class="sxs-lookup"><span data-stu-id="c3537-131">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="c3537-132">Отфильтруйте любые записи о ресурсах в задаче, которые не смогут интегрироваться в прогнозы часов.</span><span class="sxs-lookup"><span data-stu-id="c3537-132">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="c3537-133">Отфильтруйте все пустые строки категорий транзакций.</span><span class="sxs-lookup"><span data-stu-id="c3537-133">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="c3537-134">Невыполнение этой задачи может привести к неверным прогнозам часов.</span><span class="sxs-lookup"><span data-stu-id="c3537-134">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="c3537-135">Задайте идентификатор модели прогноза по умолчанию</span><span class="sxs-lookup"><span data-stu-id="c3537-135">Set the default forecast model ID</span></span>

<span data-ttu-id="c3537-136">Чтобы обновить идентификатор модели прогноза по умолчанию в шаблоне, щелкните стрелку **Сопоставить**, чтобы открыть сопоставление.</span><span class="sxs-lookup"><span data-stu-id="c3537-136">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="c3537-137">Затем выберите ссылку **Расширенный запрос и фильтрация**.</span><span class="sxs-lookup"><span data-stu-id="c3537-137">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="c3537-138">Если вы используете шаблон оценок часов проекта по умолчанию (PSA в Fin and Ops), выберите последнее **Вставленное условие** в списке **Примененные шаги**.</span><span class="sxs-lookup"><span data-stu-id="c3537-138">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="c3537-139">В записи **Функция** замените **O\_forecast** на название идентификатора модели прогноза, который следует использовать при интеграции.</span><span class="sxs-lookup"><span data-stu-id="c3537-139">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="c3537-140">В шаблоне по умолчанию есть идентификатор модели прогноза из демонстрационных данных.</span><span class="sxs-lookup"><span data-stu-id="c3537-140">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="c3537-141">Если вы создаете новый шаблон, вы должны добавить этот столбец.</span><span class="sxs-lookup"><span data-stu-id="c3537-141">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="c3537-142">В Power Query выберите **Добавить условный столбец** и введите имя нового столбца, например **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="c3537-142">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="c3537-143">Введите условие для столбца, где, если задача проекта не равна null, то \<введите идентификатор модели прогноза\>; иначе null.</span><span class="sxs-lookup"><span data-stu-id="c3537-143">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="c3537-144">Отфильтровать записи по конкретным ресурсам</span><span class="sxs-lookup"><span data-stu-id="c3537-144">Filter out resource-specific records</span></span>

<span data-ttu-id="c3537-145">В шаблоне оценок часов проекта (из PSA в Fin and Ops) есть фильтр по умолчанию, который удаляет все записи, относящиеся к конкретным ресурсам.</span><span class="sxs-lookup"><span data-stu-id="c3537-145">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="c3537-146">Если вы создаете свой собственный шаблон, вы должны добавить этот фильтр.</span><span class="sxs-lookup"><span data-stu-id="c3537-146">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="c3537-147">Выберите ссылку **Расширенный запрос и фильтрация** для фильтрации в столбце **msdyn\_islinetask**, чтобы были включены только записи **false**.</span><span class="sxs-lookup"><span data-stu-id="c3537-147">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="c3537-148">Отфильтруйте пустые строки категорий транзакций</span><span class="sxs-lookup"><span data-stu-id="c3537-148">Filter out empty transaction category rows</span></span>

<span data-ttu-id="c3537-149">Вы должны добавить фильтр, чтобы удалить все строки с пустыми категориями транзакций.</span><span class="sxs-lookup"><span data-stu-id="c3537-149">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="c3537-150">Эта задача требуется независимо от того, используете ли вы шаблон по умолчанию или создаете собственный шаблон.</span><span class="sxs-lookup"><span data-stu-id="c3537-150">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="c3537-151">Этот фильтр удаляет все итоговые строки из Project Service Automation, которые могут привести к тому, что прогнозы часов в Finance будут неверными.</span><span class="sxs-lookup"><span data-stu-id="c3537-151">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance to be incorrect.</span></span> <span data-ttu-id="c3537-152">Выберите ссылку **Расширенный запрос и фильтрация** для фильтрации пустых записей (null) в столбце **msdyn\_transactioncategory\_value**.</span><span class="sxs-lookup"><span data-stu-id="c3537-152">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="c3537-153">Сопоставление шаблонов в интеграции данных</span><span class="sxs-lookup"><span data-stu-id="c3537-153">Template mapping in Data integration</span></span>

<span data-ttu-id="c3537-154">На следующих рисунках показан пример сопоставления задач шаблона в интеграции данных.</span><span class="sxs-lookup"><span data-stu-id="c3537-154">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="c3537-155">В сопоставлении отображается информация о полях, которые будут синхронизированы из Project Service Automation в Finance.</span><span class="sxs-lookup"><span data-stu-id="c3537-155">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="c3537-156">[![Сопоставление шаблонов](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="c3537-156">[![Template mapping](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="c3537-157">Оценки расходов по проекту</span><span class="sxs-lookup"><span data-stu-id="c3537-157">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="c3537-158">Шаблон и задачи</span><span class="sxs-lookup"><span data-stu-id="c3537-158">Template and tasks</span></span>

<span data-ttu-id="c3537-159">Следующий шаблон и базовые задачи используются для синхронизации оценок расходов по проекту из Project Service Automation в Finance:</span><span class="sxs-lookup"><span data-stu-id="c3537-159">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="c3537-160">**Название шаблона в интеграции данных:** оценки расходов по проекту (из PSA в Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="c3537-160">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="c3537-161">**Название задач в проекте:**</span><span class="sxs-lookup"><span data-stu-id="c3537-161">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="c3537-162">Отношения транзакций</span><span class="sxs-lookup"><span data-stu-id="c3537-162">Transaction relationships</span></span> 
    - <span data-ttu-id="c3537-163">Оценки расходов</span><span class="sxs-lookup"><span data-stu-id="c3537-163">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="c3537-164">Набор сущностей</span><span class="sxs-lookup"><span data-stu-id="c3537-164">Entity set</span></span>

| <span data-ttu-id="c3537-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="c3537-165">Project Service Automation</span></span> | <span data-ttu-id="c3537-166">Финансы</span><span class="sxs-lookup"><span data-stu-id="c3537-166">Finance</span></span>                                                  |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="c3537-167">Подключения проводки</span><span class="sxs-lookup"><span data-stu-id="c3537-167">Transaction Connections</span></span>    | <span data-ttu-id="c3537-168">Сущность интеграции для отношений транзакций проекта</span><span class="sxs-lookup"><span data-stu-id="c3537-168">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="c3537-169">Строки оценки</span><span class="sxs-lookup"><span data-stu-id="c3537-169">Estimate Lines</span></span>             | <span data-ttu-id="c3537-170">Сущность интеграции для оценок расходов по проекту</span><span class="sxs-lookup"><span data-stu-id="c3537-170">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="c3537-171">Поток сущностей</span><span class="sxs-lookup"><span data-stu-id="c3537-171">Entity flow</span></span>

<span data-ttu-id="c3537-172">Оценки расходов по проекту управляются в Project Service Automation и синхронизируются с Finance как прогнозы расходов по проекту.</span><span class="sxs-lookup"><span data-stu-id="c3537-172">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="c3537-173">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="c3537-173">Prerequisites</span></span>

<span data-ttu-id="c3537-174">Перед синхронизацией оценок расходов по проекту необходимо синхронизировать проекты, задачи проекта и категории транзакций расходов по проекту.</span><span class="sxs-lookup"><span data-stu-id="c3537-174">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="c3537-175">Power Query</span><span class="sxs-lookup"><span data-stu-id="c3537-175">Power Query</span></span>

<span data-ttu-id="c3537-176">В шаблоне оценок расходов по проекту необходимо использовать Power Query для выполнения следующих задач:</span><span class="sxs-lookup"><span data-stu-id="c3537-176">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="c3537-177">Фильтр для включения только записей строк оценки расходов.</span><span class="sxs-lookup"><span data-stu-id="c3537-177">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="c3537-178">Установите идентификатор модели прогноза по умолчанию, который будет использоваться, когда интеграция создает новые часовые прогнозы.</span><span class="sxs-lookup"><span data-stu-id="c3537-178">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="c3537-179">Преобразуйте типы выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="c3537-179">Transform the billing types.</span></span>
- <span data-ttu-id="c3537-180">Преобразуйте типы транзакций.</span><span class="sxs-lookup"><span data-stu-id="c3537-180">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="c3537-181">Фильтр для включения только строк оценки расходов</span><span class="sxs-lookup"><span data-stu-id="c3537-181">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="c3537-182">В шаблоне оценок расходов по проекту (из PSA в Fin and Ops) есть фильтр по умолчанию, который включает в интеграцию только строки расходов.</span><span class="sxs-lookup"><span data-stu-id="c3537-182">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="c3537-183">Если вы создаете свой собственный шаблон, вы должны добавить этот фильтр.</span><span class="sxs-lookup"><span data-stu-id="c3537-183">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="c3537-184">Выберите задачу **Отношений транзакций**, а затем щелкните стрелку **Сопоставление**, чтобы открыть сопоставление.</span><span class="sxs-lookup"><span data-stu-id="c3537-184">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="c3537-185">Выберите ссылку **Расширенный запрос и фильтрация**.</span><span class="sxs-lookup"><span data-stu-id="c3537-185">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="c3537-186">Отфильтруйте столбец **msdyn\_transactiontype1**, чтобы он включал только **msdyn\_estimateline**.</span><span class="sxs-lookup"><span data-stu-id="c3537-186">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="c3537-187">Задайте идентификатор модели прогноза по умолчанию</span><span class="sxs-lookup"><span data-stu-id="c3537-187">Set the default forecast model ID</span></span>

<span data-ttu-id="c3537-188">Чтобы обновить идентификатор модели прогноза по умолчанию в шаблоне, выберите задачу **Оценки расходов** и нажмите стрелку **Сопоставить**, чтобы открыть сопоставление.</span><span class="sxs-lookup"><span data-stu-id="c3537-188">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="c3537-189">Выберите ссылку **Расширенный запрос и фильтрация**.</span><span class="sxs-lookup"><span data-stu-id="c3537-189">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="c3537-190">Если вы используете шаблон оценок расходов по проекту по умолчанию (PSA в Fin and Ops), в Power Query сначала выберите последнее **Вставленное условие** в разделе **Примененные шаги**.</span><span class="sxs-lookup"><span data-stu-id="c3537-190">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="c3537-191">В записи **Функция** замените **O\_forecast** на название идентификатора модели прогноза, который следует использовать при интеграции.</span><span class="sxs-lookup"><span data-stu-id="c3537-191">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="c3537-192">В шаблоне по умолчанию есть идентификатор модели прогноза из демонстрационных данных.</span><span class="sxs-lookup"><span data-stu-id="c3537-192">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="c3537-193">Если вы создаете новый шаблон, вы должны добавить этот столбец.</span><span class="sxs-lookup"><span data-stu-id="c3537-193">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="c3537-194">В Power Query выберите **Добавить условный столбец** и введите имя нового столбца, например **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="c3537-194">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="c3537-195">Введите условие для столбца, где, если идентификатор строки расходов не равен null, то \<введите идентификатор модели прогноза\>; иначе null.</span><span class="sxs-lookup"><span data-stu-id="c3537-195">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="c3537-196">Преобразуйте типы выставления счетов</span><span class="sxs-lookup"><span data-stu-id="c3537-196">Transform the billing types</span></span>

<span data-ttu-id="c3537-197">Шаблон оценки расходов по проекту (из PSA в Fin and Ops) включает условный столбец, который используется для преобразования типов выставления счетов, получаемых от Project Service Automation во время интеграции.</span><span class="sxs-lookup"><span data-stu-id="c3537-197">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="c3537-198">Если вы создаете свой собственный шаблон, вы должны добавить этот условный столбец.</span><span class="sxs-lookup"><span data-stu-id="c3537-198">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="c3537-199">Выберите ссылку **Расширенный запрос и фильтрация**, а затем выберите **Добавить условный столбец**.</span><span class="sxs-lookup"><span data-stu-id="c3537-199">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="c3537-200">Введите имя для нового столбца, например **BillingType**.</span><span class="sxs-lookup"><span data-stu-id="c3537-200">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="c3537-201">Затем введите следующее условие:</span><span class="sxs-lookup"><span data-stu-id="c3537-201">Then enter the following condition:</span></span>

<span data-ttu-id="c3537-202">Если **msdyn\_billingtype** = 192350000, тогда **NonChargeable**</span><span class="sxs-lookup"><span data-stu-id="c3537-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="c3537-203">иначе **msdyn\_billingtype** = 192350001, тогда **Chargeable**</span><span class="sxs-lookup"><span data-stu-id="c3537-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="c3537-204">иначе **msdyn\_billingtype** = 192350002, тогда **Complimentary**</span><span class="sxs-lookup"><span data-stu-id="c3537-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="c3537-205">иначе **NotAvailable**</span><span class="sxs-lookup"><span data-stu-id="c3537-205">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="c3537-206">Преобразуйте типы транзакций</span><span class="sxs-lookup"><span data-stu-id="c3537-206">Transform the transaction types</span></span>

<span data-ttu-id="c3537-207">Шаблон оценки расходов по проекту (из PSA в Fin and Ops) включает условный столбец, который используется для преобразования типов транзакций, получаемых от Project Service Automation во время интеграции.</span><span class="sxs-lookup"><span data-stu-id="c3537-207">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="c3537-208">Если вы создаете свой собственный шаблон, вы должны добавить этот условный столбец.</span><span class="sxs-lookup"><span data-stu-id="c3537-208">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="c3537-209">Выберите ссылку **Расширенный запрос и фильтрация**, а затем выберите **Добавить условный столбец**.</span><span class="sxs-lookup"><span data-stu-id="c3537-209">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="c3537-210">Введите имя для нового столбца, например **TransactionType**.</span><span class="sxs-lookup"><span data-stu-id="c3537-210">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="c3537-211">Затем введите следующее условие:</span><span class="sxs-lookup"><span data-stu-id="c3537-211">Then enter the following condition:</span></span>

<span data-ttu-id="c3537-212">Если **msdyn\_transactiontypecode** = 192350000, тогда **Cost**</span><span class="sxs-lookup"><span data-stu-id="c3537-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="c3537-213">иначе, если **msdyn\_transactiontypecode** = 192350005, тогда **Sales**</span><span class="sxs-lookup"><span data-stu-id="c3537-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="c3537-214">иначе **null**</span><span class="sxs-lookup"><span data-stu-id="c3537-214">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="c3537-215">Сопоставление шаблонов в интеграции данных</span><span class="sxs-lookup"><span data-stu-id="c3537-215">Template mapping in Data integration</span></span>

<span data-ttu-id="c3537-216">На следующих рисунках показаны примеры сопоставлений задач шаблона в интеграции данных.</span><span class="sxs-lookup"><span data-stu-id="c3537-216">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="c3537-217">В сопоставлении отображается информация о полях, которые будут синхронизированы из Project Service Automation в Finance.</span><span class="sxs-lookup"><span data-stu-id="c3537-217">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="c3537-218">[![Сопоставление шаблонов](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="c3537-218">[![Template mapping](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="c3537-219">[![Сопоставление шаблонов](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="c3537-219">[![Template mapping](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>
