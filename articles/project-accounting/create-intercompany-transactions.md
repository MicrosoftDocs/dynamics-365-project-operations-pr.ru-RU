---
title: Создавать внутрихолдинговые транзакции
description: В этом разделе представлена информация о том, как создавать внутрихолдинговые транзакции.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6d23e45d99be61e93d98a8377ff5fa05b3febb6b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287434"
---
# <a name="create-intercompany-transactions"></a><span data-ttu-id="cd20c-103">Создавать внутрихолдинговые транзакции</span><span class="sxs-lookup"><span data-stu-id="cd20c-103">Create intercompany transactions</span></span>

<span data-ttu-id="cd20c-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/без запасов_</span><span class="sxs-lookup"><span data-stu-id="cd20c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="cd20c-105">Внутрихолдинговые транзакции — это транзакции времени и расходов из контракта по проекту, которые принадлежат одной компании или подразделению, тогда как ресурсы в контракте по проекту являются частью другой компании или подразделения.</span><span class="sxs-lookup"><span data-stu-id="cd20c-105">Intercompany transactions are time and expense transactions from a project contract that belong to one company or organizational unit, while the resources on the project contract are part of a different company or organizational unit.</span></span>

<span data-ttu-id="cd20c-106">Когда внутрихолдинговая транзакция утверждается, создаются следующие фактические транзакции</span><span class="sxs-lookup"><span data-stu-id="cd20c-106">When an intercompany transaction is approved, the following actual transactions are created</span></span>

| <span data-ttu-id="cd20c-107">**Тип проводки**</span><span class="sxs-lookup"><span data-stu-id="cd20c-107">**Transaction type**</span></span> | <span data-ttu-id="cd20c-108">**Примененный прайс-лист**</span><span class="sxs-lookup"><span data-stu-id="cd20c-108">**Price list applied**</span></span> | <span data-ttu-id="cd20c-109">**Валюта транзакции**</span><span class="sxs-lookup"><span data-stu-id="cd20c-109">**Transaction currency**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="cd20c-110">Себестоимость</span><span class="sxs-lookup"><span data-stu-id="cd20c-110">Cost</span></span> | <span data-ttu-id="cd20c-111">Прайс-лист стоимости единицы по контракту</span><span class="sxs-lookup"><span data-stu-id="cd20c-111">Contracting unit cost price list</span></span> | <span data-ttu-id="cd20c-112">Валюта в строке цены</span><span class="sxs-lookup"><span data-stu-id="cd20c-112">Currency on the price line</span></span> |
| <span data-ttu-id="cd20c-113">Продажи без выставления счета.</span><span class="sxs-lookup"><span data-stu-id="cd20c-113">Unbilled sales.</span></span> <span data-ttu-id="cd20c-114">Они создаются только для фактических данных, связанных со строкой контракта с типом выставления счетов, временем и материалом.</span><span class="sxs-lookup"><span data-stu-id="cd20c-114">These are created only for actuals that are associated with a contract line with the billing type, time, and material.</span></span> | <span data-ttu-id="cd20c-115">Прайс-лист продаж по проекту контракта</span><span class="sxs-lookup"><span data-stu-id="cd20c-115">Contract project sales price list</span></span> | <span data-ttu-id="cd20c-116">Валюта по контракту</span><span class="sxs-lookup"><span data-stu-id="cd20c-116">Contract currency</span></span> |
| <span data-ttu-id="cd20c-117">Стоимость единицы распределения ресурсов</span><span class="sxs-lookup"><span data-stu-id="cd20c-117">Resourcing unit cost</span></span> | <span data-ttu-id="cd20c-118">Прайс-лист стоимости единицы распределения ресурсов</span><span class="sxs-lookup"><span data-stu-id="cd20c-118">Resourcing unit cost price list</span></span> | <span data-ttu-id="cd20c-119">Валюта в строке цены</span><span class="sxs-lookup"><span data-stu-id="cd20c-119">Currency on the price line</span></span> |
| <span data-ttu-id="cd20c-120">Внутрихолдинговые продажи подразделений</span><span class="sxs-lookup"><span data-stu-id="cd20c-120">Inter-organizational unit sales</span></span> | <span data-ttu-id="cd20c-121">Прайс-лист стоимости единицы по контракту</span><span class="sxs-lookup"><span data-stu-id="cd20c-121">Contracting unit cost price list</span></span> | <span data-ttu-id="cd20c-122">Валюта в строке цены</span><span class="sxs-lookup"><span data-stu-id="cd20c-122">Currency on the price line</span></span> |

<span data-ttu-id="cd20c-123">Стоимость, стоимость единицы распределения ресурсов, а также цены и валюта транзакций внутрихолдинговых продаж подразделений зависят от **подразделения**.</span><span class="sxs-lookup"><span data-stu-id="cd20c-123">Cost, resourcing unit cost, and inter-organizational unit sales transaction pricing and currency is driven by **organizational unit**.</span></span> <span data-ttu-id="cd20c-124">Это важно помнить при принятии решения о том, как структурировать компании и подразделения в вашей реализации.</span><span class="sxs-lookup"><span data-stu-id="cd20c-124">This is important to remember when deciding how to structure companies and organizational units in your implementation.</span></span>

<span data-ttu-id="cd20c-125">Когда вы создаете возможную сделку, предложение с расценками, контракт по проекту и записи по проекту, система проверяет, совпадает ли валюта подразделения по контракту с валютой учета компании по контракту.</span><span class="sxs-lookup"><span data-stu-id="cd20c-125">When you create opportunity, quote, project contract, and project records, the system verifies that the contracting unit's currency matches the contracting company's accounting currency.</span></span> <span data-ttu-id="cd20c-126">Если они не совпадают, эти записи не могут быть созданы.</span><span class="sxs-lookup"><span data-stu-id="cd20c-126">When they aren't the same, these records can't be created.</span></span> <span data-ttu-id="cd20c-127">Валюта подразделения определяется в Dynamics 365 Project Operations переходом к **Dataverse** > **Параметры** > **Подразделения**.</span><span class="sxs-lookup"><span data-stu-id="cd20c-127">The organizational unit currency is defined in Dynamics 365 Project Operations by going to **Dataverse** > **Settings** > **Organizational units**.</span></span> <span data-ttu-id="cd20c-128">Валюта учета компании определяется в Dynamics 365 Finance переходом к **Главная книга** > **Настройка главной книги** > **Книга учета**.</span><span class="sxs-lookup"><span data-stu-id="cd20c-128">A company's accounting currency is defined in Dynamics 365 Finance by going to **General ledger** > **Ledger setup** > **Ledger**.</span></span> <span data-ttu-id="cd20c-129">Валюта синхронизируется с вашей средой Dataverse с использованием сопоставления с двойной записью книги учета.</span><span class="sxs-lookup"><span data-stu-id="cd20c-129">The currency is synchronized to your Dataverse environment using Ledgers Dual Write map.</span></span>

<span data-ttu-id="cd20c-130">Система создает стоимость единицы распределения ресурсов и фактические данные продаж подразделения в следующих ситуациях:</span><span class="sxs-lookup"><span data-stu-id="cd20c-130">The system creates resourcing unit cost and inter-organizational unit sales actuals  in the following situations:</span></span>

  - <span data-ttu-id="cd20c-131">Когда единицу распределения ресурсов отличается от единицы по контракту</span><span class="sxs-lookup"><span data-stu-id="cd20c-131">When the resourcing unit differs from the contracting unit</span></span>
  - <span data-ttu-id="cd20c-132">Когда компания распределения ресурсов отличается от компании по контракту</span><span class="sxs-lookup"><span data-stu-id="cd20c-132">When the resourcing company differs from contracting company</span></span>

<span data-ttu-id="cd20c-133">Тем не менее, только транзакции, в которых есть компания распределения ресурсов, отличная от компании по контракту, будут переданы в среда Dynamics 365 Finance для дополнительного учета.</span><span class="sxs-lookup"><span data-stu-id="cd20c-133">However, only transactions that have a different resourcing company from the contracting company will be transferred to the Dynamics 365 Finance environment for additional accounting.</span></span>

<span data-ttu-id="cd20c-134">Учет фактических данных о проекте регистрируется в журнале интеграции Project Operations в Finance.</span><span class="sxs-lookup"><span data-stu-id="cd20c-134">Accounting for project actuals is recorded in the Project Operations integration journal in Finance.</span></span> <span data-ttu-id="cd20c-135">Система создает следующие строки журнала.</span><span class="sxs-lookup"><span data-stu-id="cd20c-135">The system creates the following journal lines.</span></span>

| <span data-ttu-id="cd20c-136">**Тип проводки**</span><span class="sxs-lookup"><span data-stu-id="cd20c-136">**Transaction type**</span></span> | <span data-ttu-id="cd20c-137">**Юридическое лицо**</span><span class="sxs-lookup"><span data-stu-id="cd20c-137">**Legal entity**</span></span> | <span data-ttu-id="cd20c-138">**Создает транзакцию по проекту при разноске**</span><span class="sxs-lookup"><span data-stu-id="cd20c-138">**Creates project transaction on posting**</span></span> | <span data-ttu-id="cd20c-139">**Финансовые аналитики по умолчанию из**</span><span class="sxs-lookup"><span data-stu-id="cd20c-139">**Financial dimensions default from**</span></span> | <span data-ttu-id="cd20c-140">**Налоговая группа выставления счетов и налоговая группа номенклатур выставления счетов**</span><span class="sxs-lookup"><span data-stu-id="cd20c-140">**Default billing sales tax group and billing item sales tax group**</span></span> |
| --- | --- | --- | --- | --- |
| <span data-ttu-id="cd20c-141">Себестоимость</span><span class="sxs-lookup"><span data-stu-id="cd20c-141">Cost</span></span> | <span data-ttu-id="cd20c-142">Не добавляется в журнал интеграции</span><span class="sxs-lookup"><span data-stu-id="cd20c-142">Doesn't get added to the integration journal</span></span> | <span data-ttu-id="cd20c-143">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="cd20c-143">N\A</span></span> | <span data-ttu-id="cd20c-144">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="cd20c-144">N\A</span></span> | <span data-ttu-id="cd20c-145">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="cd20c-145">N\A</span></span> |
| <span data-ttu-id="cd20c-146">Продажи без выставления счета</span><span class="sxs-lookup"><span data-stu-id="cd20c-146">Unbilled sales</span></span> | <span data-ttu-id="cd20c-147">Журнал интеграции юридических лиц-заемщиков</span><span class="sxs-lookup"><span data-stu-id="cd20c-147">The borrowing legal entity integration journal</span></span> | <span data-ttu-id="cd20c-148">Да</span><span class="sxs-lookup"><span data-stu-id="cd20c-148">Yes</span></span> | <span data-ttu-id="cd20c-149">Project</span><span class="sxs-lookup"><span data-stu-id="cd20c-149">Project</span></span> | <span data-ttu-id="cd20c-150">**Налоговая группа выставления счетов**: на основе **клиент по контракту**</span><span class="sxs-lookup"><span data-stu-id="cd20c-150">**Billing sales tax group**: Based on the **contract customer**</span></span> <br/> <span data-ttu-id="cd20c-151">**Налоговая группа номенклатур выставления счетов**: из текущей категории проекта юридического лица в строке журнала</span><span class="sxs-lookup"><span data-stu-id="cd20c-151">**Billing item sales tax group**: From the current legal entity project category on the journal line</span></span> |
| <span data-ttu-id="cd20c-152">Стоимость единицы распределения ресурсов</span><span class="sxs-lookup"><span data-stu-id="cd20c-152">Resourcing unit cost</span></span> | <span data-ttu-id="cd20c-153">Журнал интеграции юридических лиц-кредиторов</span><span class="sxs-lookup"><span data-stu-id="cd20c-153">Lending legal entity integration journal</span></span> | <span data-ttu-id="cd20c-154">No</span><span class="sxs-lookup"><span data-stu-id="cd20c-154">No</span></span> | <span data-ttu-id="cd20c-155">Внутрихолдинговый клиент</span><span class="sxs-lookup"><span data-stu-id="cd20c-155">Intercompany customer</span></span> | <span data-ttu-id="cd20c-156">**Налоговая группа выставления счетов**: на основе **внутрихолдинговый клиент**</span><span class="sxs-lookup"><span data-stu-id="cd20c-156">**Billing sales tax group**: Based on the **intercompany customer**</span></span> <br/> <span data-ttu-id="cd20c-157">**Налоговая группа номенклатур выставления счетов**: из текущей категории проекта юридического лица в строке журнала</span><span class="sxs-lookup"><span data-stu-id="cd20c-157">**Billing item sales tax group**: From the current legal entity project category on the journal line</span></span> |
| <span data-ttu-id="cd20c-158">Внутрихолдинговые продажи</span><span class="sxs-lookup"><span data-stu-id="cd20c-158">Inter-organizational sales</span></span> | <span data-ttu-id="cd20c-159">Журнал интеграции юридических лиц-кредиторов</span><span class="sxs-lookup"><span data-stu-id="cd20c-159">Lending legal entity integration journal</span></span> | <span data-ttu-id="cd20c-160">No</span><span class="sxs-lookup"><span data-stu-id="cd20c-160">No</span></span> | <span data-ttu-id="cd20c-161">Внутрихолдинговый клиент</span><span class="sxs-lookup"><span data-stu-id="cd20c-161">Intercompany customer</span></span> | <span data-ttu-id="cd20c-162">**Налоговая группа выставления счетов**: на основе **внутрихолдинговый клиент**</span><span class="sxs-lookup"><span data-stu-id="cd20c-162">**Billing sales tax group**: Based on the **intercompany customer**</span></span> <br/> <span data-ttu-id="cd20c-163">**Налоговая группа номенклатур выставления счетов**: из текущей категории проекта юридического лица в строке журнала</span><span class="sxs-lookup"><span data-stu-id="cd20c-163">**Billing item sales tax group**: From the current legal entity project category on the journal line</span></span> |

### <a name="example-intercompany-transactions"></a><span data-ttu-id="cd20c-164">Пример: внутрихолдинговые транзакции</span><span class="sxs-lookup"><span data-stu-id="cd20c-164">Example: Intercompany transactions</span></span>

<span data-ttu-id="cd20c-165">Евгения Абрамова, разработчик, работающий в GBPM, записывает 10 часов работы в рамках проекта USPM Adventure Works, который утверждается руководителем проекта.</span><span class="sxs-lookup"><span data-stu-id="cd20c-165">Molly Clark, developer employed in GBPM records 10 hours of work against a USPM Adventure Works project, which is approved by the project manager.</span></span> <span data-ttu-id="cd20c-166">Стоимость разработчика в GBPM составляет 88 британских фунтов стерлингов в час.</span><span class="sxs-lookup"><span data-stu-id="cd20c-166">Developer cost in GBPM is 88 GBP per hour.</span></span> <span data-ttu-id="cd20c-167">GBPM выставит счет USPM на 120 долларов США (USD) за каждый час разработки.</span><span class="sxs-lookup"><span data-stu-id="cd20c-167">GBPM will bill USPM 120 USD per developer hour.</span></span> <span data-ttu-id="cd20c-168">USPM выставит счет заказчику Adventure Works, 200 долларов США (USD) за работу, выполненную ресурсом GBPM.</span><span class="sxs-lookup"><span data-stu-id="cd20c-168">USPM will bill the customer Adventure Works, 200 USD for work done by the GBPM resource.</span></span> <span data-ttu-id="cd20c-169">Дополнительные сведения см. в разделе [Настройка внутрихолдингового выставления счетов](configure-intercompany-invoicing.md).</span><span class="sxs-lookup"><span data-stu-id="cd20c-169">For more information, see [Configure intercompany invoicing](configure-intercompany-invoicing.md).</span></span>

1. <span data-ttu-id="cd20c-170">В Project Operations перейдите к **Ресурсы** и выберите **Евгения Абрамова** из списка.</span><span class="sxs-lookup"><span data-stu-id="cd20c-170">In Project Operations, go to **Resources**, and select **Molly Clark** from the list.</span></span> <span data-ttu-id="cd20c-171">На вкладке **Планирование** в поле **Компания** выберите **GBPM**.</span><span class="sxs-lookup"><span data-stu-id="cd20c-171">On the **Scheduling** tab, in the **Company** field, select **GBPM**.</span></span>
2. <span data-ttu-id="cd20c-172">Перейдите к **Продажи** > **Клиенты** и выберите **Создать**, чтобы создать новую запись клиента для Adventure Works.</span><span class="sxs-lookup"><span data-stu-id="cd20c-172">Go to **Sales** > **Customers**, and select **New** to create a new customer record for Adventure Works.</span></span>
    1. <span data-ttu-id="cd20c-173">Настройте компанию на **USPM**.</span><span class="sxs-lookup"><span data-stu-id="cd20c-173">Set the company to **USPM**.</span></span>
    2. <span data-ttu-id="cd20c-174">Задавать **Тип отношений** на **Клиент**.</span><span class="sxs-lookup"><span data-stu-id="cd20c-174">Set **Relationship type** to **Customer**.</span></span>
    3. <span data-ttu-id="cd20c-175">Выбрать **Группа клиентов 10 — внутренние**.</span><span class="sxs-lookup"><span data-stu-id="cd20c-175">Select **Customer group 10 – Domestic**.</span></span>
    4. <span data-ttu-id="cd20c-176">Задайте валюту на **доллар США (USD)**.</span><span class="sxs-lookup"><span data-stu-id="cd20c-176">Set currency to **USD**.</span></span>
    5. <span data-ttu-id="cd20c-177">Сохранить запись.</span><span class="sxs-lookup"><span data-stu-id="cd20c-177">Save the record.</span></span>
3. <span data-ttu-id="cd20c-178">Перейти к **Продажи** > **Контракты по проектам** и создайте новый контракт по проекту для Adventure Works.</span><span class="sxs-lookup"><span data-stu-id="cd20c-178">Go to **Sales** > **Project Contracts** and create a new project contract for Adventure Works.</span></span>
    1. <span data-ttu-id="cd20c-179">Установите для ответственной компании **USPM** и подразделение на **Contoso Robotics US**.</span><span class="sxs-lookup"><span data-stu-id="cd20c-179">Set the owning company to **USPM** and the contracting unit to **Contoso Robotics US**.</span></span>
    2. <span data-ttu-id="cd20c-180">Выберите в качестве клиента Adventure Works.</span><span class="sxs-lookup"><span data-stu-id="cd20c-180">Select Adventure Works as the customer.</span></span>
    3. <span data-ttu-id="cd20c-181">Выберите прайс-лист продукта и сохраните запись.</span><span class="sxs-lookup"><span data-stu-id="cd20c-181">Select a product price list and save the record.</span></span>
    4. <span data-ttu-id="cd20c-182">На вкладке **Строки контракта** создайте новую строку контракта.</span><span class="sxs-lookup"><span data-stu-id="cd20c-182">On the **Contract Lines** tab, create a new contract line.</span></span> <span data-ttu-id="cd20c-183">Задайте любое имя и выберите **Время и материалы** как способ выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="cd20c-183">Set any name, and select **Time and Materials** as the billing method.</span></span>
    5. <span data-ttu-id="cd20c-184">Создайте новый проект и свяжите его с этой строкой контракта.</span><span class="sxs-lookup"><span data-stu-id="cd20c-184">Create a new project and associate it with this contract line.</span></span>
4. <span data-ttu-id="cd20c-185">Войдите в систему как ресурс, **Евгения Абрамова**.</span><span class="sxs-lookup"><span data-stu-id="cd20c-185">Sign in as the resource, **Molly Clark**.</span></span> <span data-ttu-id="cd20c-186">Перейти к **Проекты** > **Записи времени** и создайте запись времени для проекта Adventure Works.</span><span class="sxs-lookup"><span data-stu-id="cd20c-186">Go to **Projects** > **Time entries**, and create a time entry for the Adventure Works project.</span></span>
5. <span data-ttu-id="cd20c-187">Войдите в систему как Руководитель проекта.</span><span class="sxs-lookup"><span data-stu-id="cd20c-187">Sign in as the Project manager.</span></span> <span data-ttu-id="cd20c-188">Перейти к **Проекты** > **Утверждения** и утвердите транзакцию записи времени, зарегистрированную Евгенией Абрамовой.</span><span class="sxs-lookup"><span data-stu-id="cd20c-188">Go to **Projects** > **Approvals**, and approve the time entry transaction logged by Molly Clark.</span></span>
6. <span data-ttu-id="cd20c-189">Перейдите к проекту Adventure Works и выберите **Связанные** > **Фактические данные**.</span><span class="sxs-lookup"><span data-stu-id="cd20c-189">Navigate to the Adventure Works project and select **Related** > **Actuals**.</span></span> <span data-ttu-id="cd20c-190">Создаются следующие транзакции по фактическим данным.</span><span class="sxs-lookup"><span data-stu-id="cd20c-190">The following actuals transactions are created.</span></span>

| <span data-ttu-id="cd20c-191">**Тип проводки**</span><span class="sxs-lookup"><span data-stu-id="cd20c-191">**Transaction type**</span></span> | <span data-ttu-id="cd20c-192">**Цена**</span><span class="sxs-lookup"><span data-stu-id="cd20c-192">**Price**</span></span> | <span data-ttu-id="cd20c-193">**Валюта транзакции**</span><span class="sxs-lookup"><span data-stu-id="cd20c-193">**Transaction currency**</span></span> | <span data-ttu-id="cd20c-194">**Сумма**</span><span class="sxs-lookup"><span data-stu-id="cd20c-194">**Amount**</span></span> |
| --- | --- | --- | --- |
| <span data-ttu-id="cd20c-195">Себестоимость</span><span class="sxs-lookup"><span data-stu-id="cd20c-195">Cost</span></span> | <span data-ttu-id="cd20c-196">120</span><span class="sxs-lookup"><span data-stu-id="cd20c-196">120</span></span> | <span data-ttu-id="cd20c-197">USD</span><span class="sxs-lookup"><span data-stu-id="cd20c-197">USD</span></span> | <span data-ttu-id="cd20c-198">1200</span><span class="sxs-lookup"><span data-stu-id="cd20c-198">1200</span></span> |
| <span data-ttu-id="cd20c-199">Продажи без выставления счета</span><span class="sxs-lookup"><span data-stu-id="cd20c-199">Unbilled sales</span></span> | <span data-ttu-id="cd20c-200">200</span><span class="sxs-lookup"><span data-stu-id="cd20c-200">200</span></span> | <span data-ttu-id="cd20c-201">USD</span><span class="sxs-lookup"><span data-stu-id="cd20c-201">USD</span></span> | <span data-ttu-id="cd20c-202">2000</span><span class="sxs-lookup"><span data-stu-id="cd20c-202">2000</span></span> |
| <span data-ttu-id="cd20c-203">Стоимость единицы распределения ресурсов</span><span class="sxs-lookup"><span data-stu-id="cd20c-203">Resourcing unit cost</span></span> | <span data-ttu-id="cd20c-204">88</span><span class="sxs-lookup"><span data-stu-id="cd20c-204">88</span></span> | <span data-ttu-id="cd20c-205">GBP</span><span class="sxs-lookup"><span data-stu-id="cd20c-205">GBP</span></span> | <span data-ttu-id="cd20c-206">880</span><span class="sxs-lookup"><span data-stu-id="cd20c-206">880</span></span> |
| <span data-ttu-id="cd20c-207">Внутрихолдинговые продажи подразделений</span><span class="sxs-lookup"><span data-stu-id="cd20c-207">Inter-org unit sales</span></span> | <span data-ttu-id="cd20c-208">120</span><span class="sxs-lookup"><span data-stu-id="cd20c-208">120</span></span> | <span data-ttu-id="cd20c-209">USD</span><span class="sxs-lookup"><span data-stu-id="cd20c-209">USD</span></span> | <span data-ttu-id="cd20c-210">1200</span><span class="sxs-lookup"><span data-stu-id="cd20c-210">1200</span></span> |

7. <span data-ttu-id="cd20c-211">Войдите в систему как бухгалтер USPM.</span><span class="sxs-lookup"><span data-stu-id="cd20c-211">Sign in as a USPM accountant.</span></span> <span data-ttu-id="cd20c-212">Откройте экземпляр "Финансы" Project Operations и выберите компанию **USPM**.</span><span class="sxs-lookup"><span data-stu-id="cd20c-212">Open the Finance instance of Project Operations, and select the company **USPM**.</span></span> 
8. <span data-ttu-id="cd20c-213">Перейти к **Управление и учет по проектам** > **Периодический** > **Project Operations on Customer Engagement** > **Импорт из промежуточной таблицы** и выберите выполнение периодического процесса.</span><span class="sxs-lookup"><span data-stu-id="cd20c-213">Go to **Project management and accounting** > **Periodic** > **Project Operations on Customer Engagement** > **Import from staging** and select to run the periodic process.</span></span> <span data-ttu-id="cd20c-214">Этот периодический процесс будет заполнять журнал интеграции Project Operations.</span><span class="sxs-lookup"><span data-stu-id="cd20c-214">This periodic process will fill in Project Operations Integration journal.</span></span>
9. <span data-ttu-id="cd20c-215">Перейти к **Управление и учет по проектам** > **Журналы** > **Журнал интеграции Project Operations** и просмотрите строки журнала.</span><span class="sxs-lookup"><span data-stu-id="cd20c-215">Go to **Project management and accounting** > **Journals** > **Project Operations integration journal** and review the journal lines.</span></span> <span data-ttu-id="cd20c-216">Система создает следующую строку.</span><span class="sxs-lookup"><span data-stu-id="cd20c-216">The system creates the following line.</span></span>

    | <span data-ttu-id="cd20c-217">**Тип проводки**</span><span class="sxs-lookup"><span data-stu-id="cd20c-217">**Transaction type**</span></span> | <span data-ttu-id="cd20c-218">**Цена**</span><span class="sxs-lookup"><span data-stu-id="cd20c-218">**Price**</span></span> | <span data-ttu-id="cd20c-219">**Валюта транзакции**</span><span class="sxs-lookup"><span data-stu-id="cd20c-219">**Transaction currency**</span></span> | <span data-ttu-id="cd20c-220">**Сумма**</span><span class="sxs-lookup"><span data-stu-id="cd20c-220">**Amount**</span></span> |
    | --- | --- | --- | --- |
    | <span data-ttu-id="cd20c-221">Продажи без выставления счета</span><span class="sxs-lookup"><span data-stu-id="cd20c-221">Unbilled sales</span></span> | <span data-ttu-id="cd20c-222">200</span><span class="sxs-lookup"><span data-stu-id="cd20c-222">200</span></span> | <span data-ttu-id="cd20c-223">USD</span><span class="sxs-lookup"><span data-stu-id="cd20c-223">USD</span></span> | <span data-ttu-id="cd20c-224">2000</span><span class="sxs-lookup"><span data-stu-id="cd20c-224">2000</span></span> |

    <span data-ttu-id="cd20c-225">Если система настроена для начисления выручки по этому проекту, разносится следующее:</span><span class="sxs-lookup"><span data-stu-id="cd20c-225">If the system is set up to accrue revenue for this project, the following is posted:</span></span>

    - <span data-ttu-id="cd20c-226">Дебет: Проект — Объем продаж НЗП 200 долларов США (USD)</span><span class="sxs-lookup"><span data-stu-id="cd20c-226">Debit: Project – WIP sales value 200 USD</span></span>
    - <span data-ttu-id="cd20c-227">Кредит: Проект — Начисленная выручка 200 долларов США (USD)</span><span class="sxs-lookup"><span data-stu-id="cd20c-227">Credit: Project – Accrued Revenue 200 USD</span></span>

    <span data-ttu-id="cd20c-228">Эта продажа без выставления счета теперь готова к выставлению счета.</span><span class="sxs-lookup"><span data-stu-id="cd20c-228">This unbilled sale is now ready for invoicing.</span></span> <span data-ttu-id="cd20c-229">При необходимости счет для клиента Adventure Works может быть разнесен.</span><span class="sxs-lookup"><span data-stu-id="cd20c-229">The invoice for the customer Adventure Works can be financially posted when needed.</span></span>

10. <span data-ttu-id="cd20c-230">Войдите в систему как бухгалтер **GBPM**.</span><span class="sxs-lookup"><span data-stu-id="cd20c-230">Sign in as the **GBPM** accountant.</span></span> <span data-ttu-id="cd20c-231">Откройте экземпляр "Финансы" Project Operations и откройте компанию **GBPM**.</span><span class="sxs-lookup"><span data-stu-id="cd20c-231">Open the Finance instance of Project Operations, and open the company, **GBPM**.</span></span> 
11. <span data-ttu-id="cd20c-232">Перейти к **Управление и учет по проектам** > **Периодический** > **Project Operations on Customer Engagement** > **Импорт из промежуточной таблицы** и выполните периодический процесс для заполнения журнала интеграции Project Operations.</span><span class="sxs-lookup"><span data-stu-id="cd20c-232">Go to **Project management and accounting** > **Periodic** > **Project Operations on Customer Engagement** > **Import from staging** and run the periodic process to  fill in Project Operations Integration journal.</span></span>
12. <span data-ttu-id="cd20c-233">Перейти к **Управление и учет по проектам** > **Журналы** > **Журнал интеграции Project Operations** и просмотрите строки.</span><span class="sxs-lookup"><span data-stu-id="cd20c-233">Go to **Project management and accounting** > **Journals** > **Project Operations integration journal** and review the lines.</span></span> <span data-ttu-id="cd20c-234">Система создает следующие строки.</span><span class="sxs-lookup"><span data-stu-id="cd20c-234">The system creates the following lines.</span></span>

    | <span data-ttu-id="cd20c-235">**Тип проводки**</span><span class="sxs-lookup"><span data-stu-id="cd20c-235">**Transaction type**</span></span> | <span data-ttu-id="cd20c-236">**Цена**</span><span class="sxs-lookup"><span data-stu-id="cd20c-236">**Price**</span></span> | <span data-ttu-id="cd20c-237">**Валюта транзакции**</span><span class="sxs-lookup"><span data-stu-id="cd20c-237">**Transaction currency**</span></span> | <span data-ttu-id="cd20c-238">**Сумма**</span><span class="sxs-lookup"><span data-stu-id="cd20c-238">**Amount**</span></span> |
    | --- | --- | --- | --- |
    | <span data-ttu-id="cd20c-239">Стоимость единицы распределения ресурсов</span><span class="sxs-lookup"><span data-stu-id="cd20c-239">Resourcing unit cost</span></span> | <span data-ttu-id="cd20c-240">88</span><span class="sxs-lookup"><span data-stu-id="cd20c-240">88</span></span> | <span data-ttu-id="cd20c-241">GBP</span><span class="sxs-lookup"><span data-stu-id="cd20c-241">GBP</span></span> | <span data-ttu-id="cd20c-242">880</span><span class="sxs-lookup"><span data-stu-id="cd20c-242">880</span></span> |
    | <span data-ttu-id="cd20c-243">Внутрихолдинговые продажи подразделений</span><span class="sxs-lookup"><span data-stu-id="cd20c-243">Inter-org unit sales</span></span> | <span data-ttu-id="cd20c-244">120</span><span class="sxs-lookup"><span data-stu-id="cd20c-244">120</span></span> | <span data-ttu-id="cd20c-245">USD</span><span class="sxs-lookup"><span data-stu-id="cd20c-245">USD</span></span> | <span data-ttu-id="cd20c-246">1200</span><span class="sxs-lookup"><span data-stu-id="cd20c-246">1200</span></span> |

    <span data-ttu-id="cd20c-247">Публикация этих записей приводит к следующим транзакциям по ваучерам:</span><span class="sxs-lookup"><span data-stu-id="cd20c-247">Posting these records result in the following voucher transactions:</span></span>

    - <span data-ttu-id="cd20c-248">Дебет: Стоимость проекта 88 британских фунтов стерлингов</span><span class="sxs-lookup"><span data-stu-id="cd20c-248">Debit: Project cost 88 GBP</span></span>
    - <span data-ttu-id="cd20c-249">Кредит: — Распределение заработной платы 88 британских фунтов стерлингов</span><span class="sxs-lookup"><span data-stu-id="cd20c-249">Credit: Payroll allocation 88 GBP</span></span>

    <span data-ttu-id="cd20c-250">Если система настроена для начисления внутрихолдинговой выручки, разносится следующее:</span><span class="sxs-lookup"><span data-stu-id="cd20c-250">If system is set up to accrue intercompany revenue, the following is posted:</span></span>

    - <span data-ttu-id="cd20c-251">Дебет: Проект — Объем продаж НЗП 120 долларов США (USD)</span><span class="sxs-lookup"><span data-stu-id="cd20c-251">Debit: Project – WIP sales value 120 USD</span></span>
    - <span data-ttu-id="cd20c-252">Кредит: Проект — Начисленная выручка 120 долларов США (USD)</span><span class="sxs-lookup"><span data-stu-id="cd20c-252">Credit: Project – Accrued Revenue 120 USD</span></span>

    <span data-ttu-id="cd20c-253">Теперь система готова к созданию счета внутрихолдингового клиента.</span><span class="sxs-lookup"><span data-stu-id="cd20c-253">The system is now ready to create an intercompany customer invoice.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]