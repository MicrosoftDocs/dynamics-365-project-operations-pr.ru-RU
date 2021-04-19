---
title: Прогнозы и бюджеты проектов
description: Microsoft Dynamics 365 Finance предоставляет прогнозы проектов и бюджеты проектов для управления и контроля ваших проектов.
author: Yowelle
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ForecastModel, ProjYearEndProcess
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23501
ms.assetid: 4e6d1384-19a2-4232-b3f3-d2590c218bd7
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2685e99800ef6fd0b613377271259da0da805aad
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289430"
---
# <a name="project-forecasts-and-budgets"></a><span data-ttu-id="73be7-103">Прогнозы и бюджеты проектов</span><span class="sxs-lookup"><span data-stu-id="73be7-103">Project forecasts and budgets</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="73be7-104">Есть два способа управления и контроля проектов: прогнозы проектов и бюджеты проектов.</span><span class="sxs-lookup"><span data-stu-id="73be7-104">There are two ways to manage and control your projects: project forecasts and project budgets.</span></span> 

<span data-ttu-id="73be7-105">Используйте прогнозирование, если у вашей организации есть операционная перспектива и она нацелена на доходы и расходы, полученные от конкретных транзакций.</span><span class="sxs-lookup"><span data-stu-id="73be7-105">Use project forecasting if your organization has an operational perspective, and if it focuses on revenues and costs that are derived from specific transactions.</span></span> <span data-ttu-id="73be7-106">Если ваша организация больше фокусируется на финансовых суммах, вы можете использовать бюджетирование.</span><span class="sxs-lookup"><span data-stu-id="73be7-106">Use project budgeting if your organization focuses more on the financial amounts.</span></span> 

<span data-ttu-id="73be7-107">И прогнозы проектов, и бюджеты проектов используют модели прогнозов для хранения предполагаемых сумм транзакций.</span><span class="sxs-lookup"><span data-stu-id="73be7-107">Both project forecasts and project budgets use forecast models to hold the projected transaction amounts.</span></span> 

<span data-ttu-id="73be7-108">У каждого метода свои преимущества.</span><span class="sxs-lookup"><span data-stu-id="73be7-108">Each method has its advantages.</span></span> <span data-ttu-id="73be7-109">Прежде чем выбрать метод для своей организации, вам следует учесть следующие моменты.</span><span class="sxs-lookup"><span data-stu-id="73be7-109">You should consider the following points before you select a method for your organization.</span></span>

|   <span data-ttu-id="73be7-110">Метод выделения</span><span class="sxs-lookup"><span data-stu-id="73be7-110">Allocation method</span></span>       |           <span data-ttu-id="73be7-111">Прогнозирование проекта</span><span class="sxs-lookup"><span data-stu-id="73be7-111">Project forecasting</span></span>            |        <span data-ttu-id="73be7-112">Бюджетирование проекта</span><span class="sxs-lookup"><span data-stu-id="73be7-112">Project budgeting</span></span>                           |
|---------------------------|------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="73be7-113">**Распределение периода**</span><span class="sxs-lookup"><span data-stu-id="73be7-113">**Period allocation**</span></span>     | <span data-ttu-id="73be7-114">Вы не можете явно распределить транзакции по финансовым периодам.</span><span class="sxs-lookup"><span data-stu-id="73be7-114">You can't explicitly allocate transactions over a fiscal period.</span></span> <span data-ttu-id="73be7-115">Вместо этого прогноз и управление прогнозом основаны на сроке службы проекта.</span><span class="sxs-lookup"><span data-stu-id="73be7-115">Instead, the forecast, and the control of the forecast, are based on the life of the project.</span></span> <span data-ttu-id="73be7-116">Поскольку прогнозы основаны на определенной дате, вы должны определить период, исходя из этой даты.</span><span class="sxs-lookup"><span data-stu-id="73be7-116">Because forecasts are based on a specific date, you must infer the period from the date.</span></span> | <span data-ttu-id="73be7-117">Вы не можете явно распределить транзакции по всему проекту или финансовому периоду.</span><span class="sxs-lookup"><span data-stu-id="73be7-117">You can allocate transactions over the whole project or a fiscal period.</span></span> <span data-ttu-id="73be7-118">Если вы распределяете в течение определенного периода, вы можете перенести неиспользованные суммы на следующий финансовый период.</span><span class="sxs-lookup"><span data-stu-id="73be7-118">If you allocate over a period, you can carry unused amounts forward to the next fiscal period.</span></span> |
| <span data-ttu-id="73be7-119">**Просмотр транзакций**</span><span class="sxs-lookup"><span data-stu-id="73be7-119">**Viewing transactions**</span></span>  | <span data-ttu-id="73be7-120">Вы можете просматривать транзакции в формах прогнозов, где вы видите прогнозы для всей компании и для всех проектов, независимо от иерархии.</span><span class="sxs-lookup"><span data-stu-id="73be7-120">You can view transactions in the forecast forms, where you see the forecasts for the whole company and for all projects, regardless of the hierarchy.</span></span> <span data-ttu-id="73be7-121">Чтобы сосредоточиться на конкретном проекте, вы должны отфильтровать данные.</span><span class="sxs-lookup"><span data-stu-id="73be7-121">To focus on a particular project, you must filter the data.</span></span>                                       | <span data-ttu-id="73be7-122">Вы можете просмотреть бюджетные транзакции для отдельной иерархии проекта.</span><span class="sxs-lookup"><span data-stu-id="73be7-122">You can view budgeted transactions for a single project hierarchy.</span></span> <span data-ttu-id="73be7-123">Таким образом, вы можете просматривать детали транзакции для родительского проекта или его вложенных проектов.</span><span class="sxs-lookup"><span data-stu-id="73be7-123">Therefore, you can view transaction details for a parent project or its subprojects.</span></span>                 |
| <span data-ttu-id="73be7-124">**Переменные транзакции**</span><span class="sxs-lookup"><span data-stu-id="73be7-124">**Transaction variables**</span></span> | <span data-ttu-id="73be7-125">При вводе транзакций прогноза можно использовать все атрибуты, существующие для фактической транзакции.</span><span class="sxs-lookup"><span data-stu-id="73be7-125">When you enter forecast transactions, you can use every attribute that exists for an actual transaction.</span></span> <span data-ttu-id="73be7-126">Это позволяет сделать прогноз более подробным.</span><span class="sxs-lookup"><span data-stu-id="73be7-126">This allows for greater detail in the forecast.</span></span> <span data-ttu-id="73be7-127">Например, вы можете ввести подробные сведения о количествах, работниках, номенклатурах или свойствах строк.</span><span class="sxs-lookup"><span data-stu-id="73be7-127">For example, you can enter details for quantities, workers, items, or line properties.</span></span>         | <span data-ttu-id="73be7-128">Когда вы вводите детали бюджета, вы можете использовать только суммы, категории и действия.</span><span class="sxs-lookup"><span data-stu-id="73be7-128">When you enter budget details, you can use only amounts, categories, and activities.</span></span>                    |
| <span data-ttu-id="73be7-129">**Безопасность**</span><span class="sxs-lookup"><span data-stu-id="73be7-129">**Security**</span></span>              | <span data-ttu-id="73be7-130">Прогнозирование основано на транзакциях, которые вы вводите в формы прогноза, и не включает механизм управления процессом.</span><span class="sxs-lookup"><span data-stu-id="73be7-130">Forecasting is based on transactions that you enter in the forecast forms and involves no process control mechanism.</span></span> <span data-ttu-id="73be7-131">Любой работник, у которого есть разрешения для формы прогноза, может изменять информацию без одобрения.</span><span class="sxs-lookup"><span data-stu-id="73be7-131">Any worker who has permissions for a forecast form can revise information without approval.</span></span>                                        | <span data-ttu-id="73be7-132">Бюджетирование использует систему рабочего процесса, которая позволяет управлять изменениями и позволяет вам вести историю изменений.</span><span class="sxs-lookup"><span data-stu-id="73be7-132">Budgeting uses the workflow system, which enables change management and lets you keep a history of the revisions.</span></span>         |
| <span data-ttu-id="73be7-133">**Типы записей**</span><span class="sxs-lookup"><span data-stu-id="73be7-133">**Entry types**</span></span>           | <span data-ttu-id="73be7-134">Записи транзакций прогноза основаны на количестве единиц, а также на стоимости и цене продажи единицы.</span><span class="sxs-lookup"><span data-stu-id="73be7-134">Forecast transaction entries are based on the number of units, and on cost and sales unit prices.</span></span>  | <span data-ttu-id="73be7-135">Детали бюджета основаны на суммах, которые разделены между расходами и доходами.</span><span class="sxs-lookup"><span data-stu-id="73be7-135">Budget details are based on amounts, which are split between costs and revenues.</span></span>                                          |
| <span data-ttu-id="73be7-136">**Модели прогнозов**</span><span class="sxs-lookup"><span data-stu-id="73be7-136">**Forecast models**</span></span>       | <span data-ttu-id="73be7-137">Поскольку каждый прогноз должен быть связан с моделью, вы можете создать несколько моделей прогнозов, а также настроить вложенные модели.</span><span class="sxs-lookup"><span data-stu-id="73be7-137">Because each forecast must be associated with a model, you can create multiple forecast models and also set up submodels.</span></span>           | <span data-ttu-id="73be7-138">Составление бюджета проекта ограничивает модели прогноза, которые используются для составления бюджета.</span><span class="sxs-lookup"><span data-stu-id="73be7-138">Project budgeting limits the forecast models that are used for budgeting.</span></span> <span data-ttu-id="73be7-139">Меньшее количество моделей прогнозов может помочь повысить согласованность прогнозов.</span><span class="sxs-lookup"><span data-stu-id="73be7-139">Fewer forecast models can help increase consistency in projections.</span></span>                           |
| <span data-ttu-id="73be7-140">**Перерасход средств**</span><span class="sxs-lookup"><span data-stu-id="73be7-140">**Cost overruns**</span></span>         | <span data-ttu-id="73be7-141">Вы можете разрешить или запретить ввод только тех транзакций, которые вызовут перерасход средств.</span><span class="sxs-lookup"><span data-stu-id="73be7-141">You can only allow or disallow the entry of transactions that will cause a cost overrun.</span></span>   | <span data-ttu-id="73be7-142">Составление бюджета проекта предоставляет пользователям дополнительные возможности управления.</span><span class="sxs-lookup"><span data-stu-id="73be7-142">Project budgeting provides additional control options for users.</span></span> <span data-ttu-id="73be7-143">Вы можете разрешить предупреждения и перерасход.</span><span class="sxs-lookup"><span data-stu-id="73be7-143">You can allow warnings and overruns.</span></span>                    |
| <span data-ttu-id="73be7-144">**Элемент управления**</span><span class="sxs-lookup"><span data-stu-id="73be7-144">**Control**</span></span>               | <span data-ttu-id="73be7-145">Управление прогнозом осуществляется с помощью уменьшения прогноза.</span><span class="sxs-lookup"><span data-stu-id="73be7-145">Forecast control is performed by using forecast reduction.</span></span> <span data-ttu-id="73be7-146">Фактические суммы вычитаются из прогнозируемых балансов транзакций без какого-либо журнала аудита.</span><span class="sxs-lookup"><span data-stu-id="73be7-146">Actual amounts are subtracted from forecast transaction balances without any audit trail.</span></span> <span data-ttu-id="73be7-147">Это может затруднить отслеживание фактических транзакций.</span><span class="sxs-lookup"><span data-stu-id="73be7-147">This can make it more difficult to trace where the actual transactions occurred.</span></span>                   | <span data-ttu-id="73be7-148">При контроле бюджета проекта фактические суммы вычитаются из сумм в оставшемся бюджете.</span><span class="sxs-lookup"><span data-stu-id="73be7-148">In project budget control, actual amounts are subtracted from amounts in the remaining budget.</span></span> <span data-ttu-id="73be7-149">Это позволяет вести более точный журнал аудита.</span><span class="sxs-lookup"><span data-stu-id="73be7-149">This allows for a clearer audit trail.</span></span>                                   |

## <a name="project-forecasts"></a><span data-ttu-id="73be7-150">Прогнозы проекта</span><span class="sxs-lookup"><span data-stu-id="73be7-150">Project forecasts</span></span>
<span data-ttu-id="73be7-151">При использовании прогнозирования проекта можно вводить транзакции прогноза в формы прогноза для каждого типа транзакции.</span><span class="sxs-lookup"><span data-stu-id="73be7-151">When you use project forecasting, you can enter forecast transactions in forecast forms for each transaction type.</span></span> <span data-ttu-id="73be7-152">Каждый атрибут, доступный для фактической транзакции, может использоваться для прогнозируемой транзакции, например, прибыльность строки, атрибуты строки, работники или описания.</span><span class="sxs-lookup"><span data-stu-id="73be7-152">Every attribute that is available for an actual transaction can be used for a forecast transaction—for example, line profitability, line attributes, workers, or descriptions.</span></span> <span data-ttu-id="73be7-153">Вы также можете спрогнозировать, через какое время после несения затрат вы будете выставлять счет клиенту.</span><span class="sxs-lookup"><span data-stu-id="73be7-153">You can also project how long after you incur a cost you will invoice a customer.</span></span> 

<span data-ttu-id="73be7-154">Операции прогнозирования проекта основаны на единицах и суммах.</span><span class="sxs-lookup"><span data-stu-id="73be7-154">Project forecasting transactions are based on units and amounts.</span></span> 

<span data-ttu-id="73be7-155">Вы должны связать каждый прогноз проекта с моделью прогноза.</span><span class="sxs-lookup"><span data-stu-id="73be7-155">You must associate each project forecast with a forecast model.</span></span> <span data-ttu-id="73be7-156">При вводе транзакции прогноза автоматически предлагается модель прогноза.</span><span class="sxs-lookup"><span data-stu-id="73be7-156">When you enter a forecast transaction, a forecast model is automatically suggested.</span></span> <span data-ttu-id="73be7-157">Модель прогноза действует как контейнер для транзакций прогноза.</span><span class="sxs-lookup"><span data-stu-id="73be7-157">The forecast model acts as a container for the forecast transactions.</span></span> 

<span data-ttu-id="73be7-158">Вы можете обозначить модели прогноза как вложенные модели для модели.</span><span class="sxs-lookup"><span data-stu-id="73be7-158">You can designate forecast models as submodels for a model.</span></span> <span data-ttu-id="73be7-159">Это позволяет делать прогнозы по региону, периоду времени или отделу.</span><span class="sxs-lookup"><span data-stu-id="73be7-159">This lets you forecast by region, time period, or department.</span></span> <span data-ttu-id="73be7-160">Вы можете скопировать транзакции прогноза в модель, чтобы создать новую модель, а также можете перенести транзакции в главную книгу.</span><span class="sxs-lookup"><span data-stu-id="73be7-160">You can copy the forecast transactions in a model to create a new model, and you can also transfer the transactions to the general ledger.</span></span> <span data-ttu-id="73be7-161">Поскольку между прогнозом и моделью существует взаимно однозначная связь, каждая модель прогноза составляет отдельный бюджет для проекта.</span><span class="sxs-lookup"><span data-stu-id="73be7-161">Because there is a one-to-one relationship between a forecast and a model, each forecast model makes up a separate budget for a project.</span></span> 

<span data-ttu-id="73be7-162">Модели прогнозов могут использовать сокращение прогнозов в качестве механизма управления проектами.</span><span class="sxs-lookup"><span data-stu-id="73be7-162">Forecast models can use forecast reduction as the control mechanism for projects.</span></span> <span data-ttu-id="73be7-163">При сокращении прогноза фактические транзакции уменьшают прогнозируемые балансы транзакций.</span><span class="sxs-lookup"><span data-stu-id="73be7-163">In forecast reduction, actual transactions reduce forecast transaction balances.</span></span> <span data-ttu-id="73be7-164">Однако, поскольку сокращение прогноза применяется к самому высокому проекту в иерархии, оно обеспечивает ограниченное представление изменений в прогнозе.</span><span class="sxs-lookup"><span data-stu-id="73be7-164">However, because forecast reduction is applied to the highest project in the hierarchy, it provides a limited view of changes in the forecast.</span></span> <span data-ttu-id="73be7-165">Например, если работник связан с вложенным проектом, фактические транзакции для работника отправляются в родительский проект.</span><span class="sxs-lookup"><span data-stu-id="73be7-165">For example, if a worker is associated with a subproject, the actual transactions for the worker are posted to the parent project.</span></span> <span data-ttu-id="73be7-166">Это может затруднить отслеживание изменений, потому что вы не можете легко определить, какая транзакция в каком вложенном проекте вызвала уменьшение прогнозируемой суммы.</span><span class="sxs-lookup"><span data-stu-id="73be7-166">This can make it difficult to track changes, because you can't easily determine which transaction in which subproject caused a reduction to the forecast amount.</span></span> <span data-ttu-id="73be7-167">Поэтому рекомендуется создать копию модели прогноза для использования при сокращении прогноза.</span><span class="sxs-lookup"><span data-stu-id="73be7-167">Therefore, it's a good idea to create a copy of a forecast model for forecast reduction to use.</span></span> <span data-ttu-id="73be7-168">Затем вы можете использовать отчеты для просмотра того, что изначально прогнозировалось.</span><span class="sxs-lookup"><span data-stu-id="73be7-168">You can then use reports to view what was originally forecasted.</span></span> 

<span data-ttu-id="73be7-169">Вы можете пересматривать, копировать, удалять или переносить прогнозы проекта в бюджет главной книги.</span><span class="sxs-lookup"><span data-stu-id="73be7-169">You can revise, copy, delete, or transfer project forecasts to a general ledger budget.</span></span> <span data-ttu-id="73be7-170">Однако нет никакого технологического контроля.</span><span class="sxs-lookup"><span data-stu-id="73be7-170">However, there is no process control.</span></span> <span data-ttu-id="73be7-171">Любой работник, у которого есть разрешение для формы прогноза, может вносить изменения без рассмотрения.</span><span class="sxs-lookup"><span data-stu-id="73be7-171">Any worker who has permission for a forecast form can make revisions without review.</span></span>

-   <span data-ttu-id="73be7-172">**Пересмотреть** — вы можете пересмотреть транзакцию прогноза в тех же формах, где были сделаны исходные записи.</span><span class="sxs-lookup"><span data-stu-id="73be7-172">**Revise**– You can revise a forecast transaction in the same forms where the original entries were made.</span></span>
-   <span data-ttu-id="73be7-173">**Копировать или удалить** — при копировании транзакций прогноза вы копируете строки транзакции одной модели прогноза в другую модель прогноза.</span><span class="sxs-lookup"><span data-stu-id="73be7-173">**Copy or delete** – When you copy forecast transactions, you copy the transaction lines of one forecast model to another forecast model.</span></span> <span data-ttu-id="73be7-174">При удалении прогноза вы удаляете транзакции прогноза из модели прогноза.</span><span class="sxs-lookup"><span data-stu-id="73be7-174">When you delete a forecast, you delete the forecast transactions from a forecast model.</span></span> <span data-ttu-id="73be7-175">Чтобы ограничить количество операций прогноза, которые копируются или удаляются, выберите определенные типы операций и даты.</span><span class="sxs-lookup"><span data-stu-id="73be7-175">To limit the forecast transactions that are copied or deleted, select specific transaction types and dates.</span></span> <span data-ttu-id="73be7-176">Это позволяет копировать или удалять только определенные части прогноза.</span><span class="sxs-lookup"><span data-stu-id="73be7-176">This lets you copy or delete only specific parts of a forecast.</span></span>
-   <span data-ttu-id="73be7-177">**Перенести** — когда вы переносите прогноз проекта в бюджет главной книги, вы переносите операции прогноза модели прогноза в бюджет главной книги.</span><span class="sxs-lookup"><span data-stu-id="73be7-177">**Transfer** – When you transfer a project forecast to a general ledger budget, you transfer the forecast transactions of a forecast model to a general ledger budget.</span></span> <span data-ttu-id="73be7-178">Вы можете перезаписать любые ранее перенесенные транзакции в бюджете главной книги, в которую вы переносите прогноз проекта.</span><span class="sxs-lookup"><span data-stu-id="73be7-178">You can overwrite any previously transferred transactions in the general ledger budget that you transfer your project forecast to.</span></span>

## <a name="project-budgets"></a><span data-ttu-id="73be7-179">Бюджеты проекта</span><span class="sxs-lookup"><span data-stu-id="73be7-179">Project budgets</span></span>
<span data-ttu-id="73be7-180">Составление бюджета по проекту — более простой метод, чем прогнозирование, хотя он интегрируется с моделями прогноза.</span><span class="sxs-lookup"><span data-stu-id="73be7-180">Project budgeting is a simpler method than forecasting, although it does integrate with forecast models.</span></span> <span data-ttu-id="73be7-181">Оно использует единую форму ввода для исходных сведений и изменений бюджета и позволяет делать прогнозы, основанные только на сумме, категории или деятельности.</span><span class="sxs-lookup"><span data-stu-id="73be7-181">It uses a single entry form for original budget details and revisions, and allows for projections that are based only on amount, category, or activity.</span></span> 

<span data-ttu-id="73be7-182">При составлении бюджета проекта все исходные бюджеты и изменения должны отправляться в рабочий процесс проекта для утверждения.</span><span class="sxs-lookup"><span data-stu-id="73be7-182">In project budgeting, all original budgets and revisions must be sent to a project workflow for approval.</span></span> <span data-ttu-id="73be7-183">Рабочие процессы дают вам больший контроль над процессом и создают запись истории изменений.</span><span class="sxs-lookup"><span data-stu-id="73be7-183">Workflows give you increased control over the process and create a change history record.</span></span> 

<span data-ttu-id="73be7-184">Составление бюджета проекта похоже на составление бюджета главной книги, но его проще и быстрее настроить.</span><span class="sxs-lookup"><span data-stu-id="73be7-184">Project budgeting resembles general ledger budgeting, but is faster and easier to set up.</span></span> <span data-ttu-id="73be7-185">Многие параметры бюджетирования в главной книге, такие как номерные серии или валюта, не нужно настраивать отдельно для проектов.</span><span class="sxs-lookup"><span data-stu-id="73be7-185">Many of the options in general ledger budgeting, such as number sequences or currency, do not have to be set up separately for projects.</span></span>

<span data-ttu-id="73be7-186">Бюджеты проекта автоматически связываются с двумя моделями прогноза: одной для исходного бюджета и одной для оставшегося бюджета.</span><span class="sxs-lookup"><span data-stu-id="73be7-186">Project budgets are automatically associated with two forecast models, one for original budget and one for remaining budget.</span></span> <span data-ttu-id="73be7-187">Следовательно, отчеты, основанные на моделях прогноза, могут использовать данные бюджета.</span><span class="sxs-lookup"><span data-stu-id="73be7-187">Therefore, reports that are based on forecast models can use budget data.</span></span> <span data-ttu-id="73be7-188">Когда бюджет проекта подтвержден, система создает транзакции прогноза на основе связанных моделей, которые используются для отчетности и контроля.</span><span class="sxs-lookup"><span data-stu-id="73be7-188">When a project budget is committed, the system creates forecast transactions based on the associated models, which are used for reporting and control purposes.</span></span>

## <a name="forecast-models"></a><span data-ttu-id="73be7-189">Модели прогнозов</span><span class="sxs-lookup"><span data-stu-id="73be7-189">Forecast models</span></span>
<span data-ttu-id="73be7-190">У модели прогнозов одноуровневая иерархия.</span><span class="sxs-lookup"><span data-stu-id="73be7-190">Forecast models have a single-layer hierarchy.</span></span> <span data-ttu-id="73be7-191">Это означает, что один прогноз проекта должен быть связан с одной моделью прогноза.</span><span class="sxs-lookup"><span data-stu-id="73be7-191">This means that one project forecast must be associated with one forecast model.</span></span>

<span data-ttu-id="73be7-192">Если вы используете прогнозирование проекта, вы можете идентифицировать модели как вложенные модели.</span><span class="sxs-lookup"><span data-stu-id="73be7-192">If you use project forecasting, you can identify models as submodels.</span></span> <span data-ttu-id="73be7-193">Затем можно делать прогнозы по подразделению, периоду времени или региону.</span><span class="sxs-lookup"><span data-stu-id="73be7-193">You can then create forecasts by department, time period, or region.</span></span> <span data-ttu-id="73be7-194">Например, вы можете создать модель прогноза на год, а затем создать вложенные модели для региональных прогнозов северо-востока, юго-востока, северо-запада и юго-запада, которые будут представлены региональными руководителями.</span><span class="sxs-lookup"><span data-stu-id="73be7-194">For example, you can create a forecast model for a year, and then create submodels for the Northeast, Southeast, Northwest, and Southwest regional forecasts that regional heads submit.</span></span> <span data-ttu-id="73be7-195">Выбирая различные параметры в доступных отчетах, вы можете просматривать информацию по общему прогнозу или по вложенной модели.</span><span class="sxs-lookup"><span data-stu-id="73be7-195">By selecting different options in the available reports, you can view information by total forecast or by submodel.</span></span>





[!INCLUDE[footer-include](../includes/footer-banner.md)]