---
title: Журнал интеграции в Project Operations
description: Эта тема предоставляет информацию о работе с журналом интеграции в Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0021147530d1aa9f82cc54ca8c92b9977c1eea2c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287254"
---
# <a name="integration-journal-in-project-operations"></a><span data-ttu-id="c6d20-103">Журнал интеграции в Project Operations</span><span class="sxs-lookup"><span data-stu-id="c6d20-103">Integration journal in Project Operations</span></span>

<span data-ttu-id="c6d20-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/без запасов_</span><span class="sxs-lookup"><span data-stu-id="c6d20-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="c6d20-105">Записи о времени и расходах создают транзакции **Фактически**, которые представляют собой операционное представление работы, выполненной по проекту.</span><span class="sxs-lookup"><span data-stu-id="c6d20-105">Time and expense entries create **Actual** transactions which represent the operational view of work completed against a project.</span></span> <span data-ttu-id="c6d20-106">Dynamics 365 Project Operations предоставляет бухгалтерам инструмент для проверки транзакций и корректировки атрибутов учета по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="c6d20-106">Dynamics 365 Project Operations provides accountants with a tool to review transactions and adjust the accounting attributes as needed.</span></span> <span data-ttu-id="c6d20-107">После завершения проверки и корректировок проводки разносятся во вспомогательную книгу проекта и главную книгу.</span><span class="sxs-lookup"><span data-stu-id="c6d20-107">After the review and adjustments are complete, the transactions are posted to the Project subledger and General ledger.</span></span> <span data-ttu-id="c6d20-108">Бухгалтер может выполнять эти действия, используя журнал **Интеграция Project Operations** (**Dynamics 365 Finance** > **Управление и учет по проектам** > **Журналы** > журнал **Интеграция Project Operations**).</span><span class="sxs-lookup"><span data-stu-id="c6d20-108">An accountant can perform these activities using the **Project Operations Integration** journal(**Dynamics 365 Finance** > **Project management and accounting** > **Journals** > **Project Operations Integration** journal.</span></span>

![Поток журнала интеграции](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a><span data-ttu-id="c6d20-110">Создание записей в журнале интеграции Project Operations</span><span class="sxs-lookup"><span data-stu-id="c6d20-110">Create records in the Project Operations Integration journal</span></span>

<span data-ttu-id="c6d20-111">Записи в журнале интеграции Project Operations создаются с использованием периодического процесса **Импорт из промежуточной таблицы**.</span><span class="sxs-lookup"><span data-stu-id="c6d20-111">Records in the Project Operations Integration journal are created using periodic process, **Import from staging table**.</span></span> <span data-ttu-id="c6d20-112">Вы можете запустить этот процесс, перейдя в раздел **Dynamics 365 Finance** > **Управление и учет по проектам** > **Периодические операции** > **Интеграция Project Operations** > **Импорт из промежуточной таблицы**.</span><span class="sxs-lookup"><span data-stu-id="c6d20-112">You can run this process by going to **Dynamics 365 Finance** > **Project management and accounting** > **Periodic** > **Project Operations Integration** > **Import from staging table**.</span></span> <span data-ttu-id="c6d20-113">Вы можете запустить процесс в интерактивном режиме или настроить его для работы в фоновом режиме, как требуется.</span><span class="sxs-lookup"><span data-stu-id="c6d20-113">You can run the process interactively or configure the process to run in the background as needed.</span></span>

<span data-ttu-id="c6d20-114">При запуске периодического процесса обнаруживаются все фактические данные, которые еще не добавлены в журнал интеграции Project Operations.</span><span class="sxs-lookup"><span data-stu-id="c6d20-114">When the periodic process runs, any actuals that aren't yet added to the Project Operations Integration journal are found.</span></span> <span data-ttu-id="c6d20-115">Создается строка журнала для каждой фактической транзакции.</span><span class="sxs-lookup"><span data-stu-id="c6d20-115">A journal line for each actual transaction is created.</span></span>
<span data-ttu-id="c6d20-116">Система группирует строки журнала в отдельные журналы на основе значения, выбранного в поле **Единица измерения периода в журнале интеграции Project Operations** (вкладка **Finance** > **Управление и учет по проектам** > **Настройка** > **Параметры управления и учета по проектам**, **Project Operations в Dynamics 365 Customer Engagement**).</span><span class="sxs-lookup"><span data-stu-id="c6d20-116">The system groups journal lines into separate journals based on the value selected in the **Period unit on Project Operations Integration journal** field (**Finance** > **Project management and accounting** > **Setup** > **Project management and accounting parameters**, **Project Operations on Dynamics 365 Customer Engagement**\* tab).</span></span> <span data-ttu-id="c6d20-117">Возможные значения для этого поля:</span><span class="sxs-lookup"><span data-stu-id="c6d20-117">Possible values for this field include:</span></span>

  - <span data-ttu-id="c6d20-118">**Дни**: фактические данные сгруппированы по дате транзакции.</span><span class="sxs-lookup"><span data-stu-id="c6d20-118">**Days**: Actuals are grouped by transaction date.</span></span> <span data-ttu-id="c6d20-119">На каждый день создается отдельный журнал.</span><span class="sxs-lookup"><span data-stu-id="c6d20-119">A separate journal is created for each day.</span></span>
  - <span data-ttu-id="c6d20-120">**Месяцы**: фактические данные сгруппированы по календарным месяцам.</span><span class="sxs-lookup"><span data-stu-id="c6d20-120">**Months**: Actuals are grouped by calendar month.</span></span> <span data-ttu-id="c6d20-121">На каждый месяц создается отдельный журнал.</span><span class="sxs-lookup"><span data-stu-id="c6d20-121">A separate journal is created for each month.</span></span>
  - <span data-ttu-id="c6d20-122">**Годы**: фактические данные сгруппированы по календарным годам.</span><span class="sxs-lookup"><span data-stu-id="c6d20-122">**Years**: Actuals are grouped by calendar year.</span></span> <span data-ttu-id="c6d20-123">На каждый год создается отдельный журнал.</span><span class="sxs-lookup"><span data-stu-id="c6d20-123">A separate journal is created for each year.</span></span>
  - <span data-ttu-id="c6d20-124">**Все**: все фактические транзакции включаются в один журнал интеграции.</span><span class="sxs-lookup"><span data-stu-id="c6d20-124">**All**: All actual transactions are included in the same integration journal.</span></span> <span data-ttu-id="c6d20-125">Если журнал недоступен во время выполнения периодического процесса, например, если журнал находится в процессе разноски транзакций, создается новый журнал.</span><span class="sxs-lookup"><span data-stu-id="c6d20-125">If the journal isn't available when the periodic process runs, for example if the journal is in the process of posting transactions, a new journal is created.</span></span>

<span data-ttu-id="c6d20-126">Строки журнала создаются на основе фактических данных по проекту.</span><span class="sxs-lookup"><span data-stu-id="c6d20-126">Journal lines are created based on project actuals.</span></span> <span data-ttu-id="c6d20-127">Следующий список включает некоторые из наиболее примечательных правил по умолчанию и правил преобразования:</span><span class="sxs-lookup"><span data-stu-id="c6d20-127">The following list includes some of the more notable default and transformation rules:</span></span>

  - <span data-ttu-id="c6d20-128">Каждая фактическая транзакция проекта имеет строку в журнале интеграции Project Operations.</span><span class="sxs-lookup"><span data-stu-id="c6d20-128">Each project actual transaction has a line in the Project Operations Integration journal.</span></span> <span data-ttu-id="c6d20-129">Себестоимость и операции продажи, за которые не выставлены счета, для типа выставления счетов по времени и материалам показаны в отдельных строках.</span><span class="sxs-lookup"><span data-stu-id="c6d20-129">Cost and unbilled sales transactions for time and material billing type are shown on separate lines.</span></span>
  - <span data-ttu-id="c6d20-130">Поле **Дата** представляет дату транзакции.</span><span class="sxs-lookup"><span data-stu-id="c6d20-130">The **Date** field represents the date of the transaction.</span></span> <span data-ttu-id="c6d20-131">Поле **Дата отчетности** представляет дату, когда транзакция записана в книгу учета.</span><span class="sxs-lookup"><span data-stu-id="c6d20-131">The **Accounting date** field represents the date that the transaction is recorded to the ledger.</span></span> <span data-ttu-id="c6d20-132">Если дата отчетности приходится на [закрытый финансовый период](https://docs.microsoft.com/dynamics365/finance/general-ledger/close-general-ledger-at-period-end), а параметр **Автоматически устанавливать дату учета равной периоду открытия ГК** установлен на вкладке **Финансы** страницы **Параметры управления и учета по проектам**, система скорректирует дату учета транзакции на первую дату в следующем открытом периоде книги учета.</span><span class="sxs-lookup"><span data-stu-id="c6d20-132">If the accounting date is in a [closed financial period](https://docs.microsoft.com/dynamics365/finance/general-ledger/close-general-ledger-at-period-end), and the parameter **Automatically set accounting date to open ledger period** is set on the **Financial** tab of the **Project management and accounting parameters** page, the system will adjust the accounting date of the transaction to the first date in next open ledger period.</span></span>
  - <span data-ttu-id="c6d20-133">В поле **Ваучер** отображается номер ваучера для каждой фактической транзакции.</span><span class="sxs-lookup"><span data-stu-id="c6d20-133">The **Voucher** field shows the voucher number for every actual transaction.</span></span> <span data-ttu-id="c6d20-134">Последовательность номеров ваучеров определяется на вкладке **Номерные последовательности** на странице **Параметры управления и учета по проектам**.</span><span class="sxs-lookup"><span data-stu-id="c6d20-134">The voucher number sequence is defined on the **Number sequences** tab, on the **Project management and accounting parameters** page.</span></span> <span data-ttu-id="c6d20-135">Каждой строке присваивается новый номер.</span><span class="sxs-lookup"><span data-stu-id="c6d20-135">Each line is assigned a new number.</span></span> <span data-ttu-id="c6d20-136">После разноски ваучера вы можете просмотреть, как связаны затраты и транзакции продажи, по которым не выставлены счета, выбрав **Связанные ваучеры** на странице **Проводка ваучера**.</span><span class="sxs-lookup"><span data-stu-id="c6d20-136">After the voucher is posted, you can view how cost and unbilled sales transaction are related by selecting **Related vouchers** on the **Voucher transaction** page.</span></span>
  - <span data-ttu-id="c6d20-137">Поле **Категория** представляет транзакцию проекта и значения по умолчанию, основанные на категории транзакции для связанных фактических данных проекта.</span><span class="sxs-lookup"><span data-stu-id="c6d20-137">The **Category** field represents a project transaction and defaults based on the transaction category for the related project actual.</span></span>
    - <span data-ttu-id="c6d20-138">Если **Категория транзакции** устанавливается в фактических данных проекта и связанная **Категория проекта** существует в данном юридическом лице, категория по умолчанию соответствует этой категории проекта.</span><span class="sxs-lookup"><span data-stu-id="c6d20-138">If **Transaction category** is set in the Project actual and a related **Project category** exists in a given legal entity, the category defaults to this project category.</span></span>
    - <span data-ttu-id="c6d20-139">Если **Категория транзакции** не задана в фактических данных проекта, система использует значение в поле **Значения по умолчанию для категории проекта** на вкладке **Project Operations в Dynamics 365 Customer Engagement** на странице **Параметры управления и учета по проектам**.</span><span class="sxs-lookup"><span data-stu-id="c6d20-139">If **Transaction category** isn't set in the Project actual, the system uses the value in the **Project category defaults** field on the **Project Operations on Dynamics 365 Customer Engagement** tab on the **Project management and accounting parameters** page.</span></span>
  - <span data-ttu-id="c6d20-140">Поле **Ресурс** представляет ресурс проекта, связанный с этой транзакцией.</span><span class="sxs-lookup"><span data-stu-id="c6d20-140">The **Resource** field represents the project resource related to this transaction.</span></span> <span data-ttu-id="c6d20-141">Ресурс используется в качестве ссылки в предложениях по счетам проекта для клиентов.</span><span class="sxs-lookup"><span data-stu-id="c6d20-141">The resource is used as a reference in Project invoice proposals to customers.</span></span>
  - <span data-ttu-id="c6d20-142">Поле **Обменный курс** по умолчанию устанавливается из значения **Курс валюты** в Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="c6d20-142">The **Exchange rate** field defaults from **Currency exchange rate** set in Dynamics 365 Finance.</span></span> <span data-ttu-id="c6d20-143">Если настройка обменного курса отсутствует, периодический процесс **Импорт из промежуточной таблицы** не будет добавлять запись в журнал, а в журнал выполнения задания будет добавлено сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="c6d20-143">If the exchange rate setup is missing, the **Import from staging** periodic process won't add the record to a journal and an error message will be added to the job execution log.</span></span>
  - <span data-ttu-id="c6d20-144">Поле **Свойство строки** представляет тип выставления счетов в фактических данных по проекту.</span><span class="sxs-lookup"><span data-stu-id="c6d20-144">The **Line property** field represents the billing type in Project actuals.</span></span> <span data-ttu-id="c6d20-145">Сопоставление свойств строки и типа выставления счетов определяется на вкладке **Project Operations в Dynamics 365 Customer Engagement** на странице **Параметры управления и учета по проектам**.</span><span class="sxs-lookup"><span data-stu-id="c6d20-145">Line property and billing type mapping are defined on the **Project Operations on Dynamics 365 Customer Engagement** tab on the **Project management and accounting parameters** page.</span></span>

<span data-ttu-id="c6d20-146">В строках журнала интеграции Project Operations можно обновить только следующие атрибуты учета:</span><span class="sxs-lookup"><span data-stu-id="c6d20-146">Only the following accounting attributes can be updated in the Project Operations integration journal lines:</span></span>

- <span data-ttu-id="c6d20-147">**Налоговая группа выставления счетов** и **Налоговая группа номенклатур выставления счетов**</span><span class="sxs-lookup"><span data-stu-id="c6d20-147">**Billing sales tax group** and **Billing item sales tax group**</span></span>
- <span data-ttu-id="c6d20-148">**Финансовые аналитики** (с использованием действия **Распределить суммы**)</span><span class="sxs-lookup"><span data-stu-id="c6d20-148">**Financial dimensions** (using the **Distribute amounts** action)</span></span>

<span data-ttu-id="c6d20-149">Строки журнала интеграции можно удалить, однако любые неопубликованные строки будут снова вставлены в журнал после повторного запуска периодического процесса **Импорт из промежуточной таблицы**.</span><span class="sxs-lookup"><span data-stu-id="c6d20-149">Integration journal lines can be deleted, however any unposted lines will be inserted into the journal again after you rerun the **Import from staging** periodic process.</span></span>

<span data-ttu-id="c6d20-150">При разноске журнала интеграции создаются проводки вспомогательной книги проекта и главной книги.</span><span class="sxs-lookup"><span data-stu-id="c6d20-150">When you post the Integration journal, a project subledger and general ledger transactions are created.</span></span> <span data-ttu-id="c6d20-151">Они используются для последующего выставления счетов клиентам, признания выручки и финансовой отчетности.</span><span class="sxs-lookup"><span data-stu-id="c6d20-151">These are used in downstream customer invoicing, revenue recognition, and financial reporting.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]