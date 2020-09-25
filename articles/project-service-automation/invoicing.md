---
title: Выставление счетов в Project Service Automation
description: В этом разделе представлена информация о выставлении счетов.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 03/11/2019
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365  Project Service Automation 2.x and 3.x
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 8d95f17aba0a4cab65a6f020aade5e19568de3be
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754880"
---
# <a name="invoicing-in-project-service-automation"></a><span data-ttu-id="7b45c-103">Выставление счетов в Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="7b45c-103">Invoicing in Project Service Automation</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="7b45c-104">Выставление счетов в Dynamics 365 Project Service Automation полезно, поскольку дает руководителям проекта второй уровень утверждения перед созданием счетов для клиентов.</span><span class="sxs-lookup"><span data-stu-id="7b45c-104">Invoicing in Dynamics 365 Project Service Automation is useful because it gives project managers a second level of approval before they create invoices for customers.</span></span> <span data-ttu-id="7b45c-105">Первый уровень утверждения завершается, когда утверждаются записи времени и расходов, представленные участниками проектной группы.</span><span class="sxs-lookup"><span data-stu-id="7b45c-105">The first level of approval is completed when the time and expense entries that project team members submit are approved.</span></span>

<span data-ttu-id="7b45c-106">PSA не предназначен для создания счетов для клиентов по следующим причинам:</span><span class="sxs-lookup"><span data-stu-id="7b45c-106">PSA isn't designed to generate customer-facing invoices, for the following reasons:</span></span>

- <span data-ttu-id="7b45c-107">Он не содержит данных о налогах.</span><span class="sxs-lookup"><span data-stu-id="7b45c-107">It doesn't contain tax information.</span></span>
- <span data-ttu-id="7b45c-108">Он не может преобразовывать другие валюты в валюты выставления счетов с помощью правильно настроенных курсов обмена.</span><span class="sxs-lookup"><span data-stu-id="7b45c-108">It can't convert other currencies to the invoicing currency by using correctly configured exchange rates.</span></span>
- <span data-ttu-id="7b45c-109">Он не может правильно форматировать счета, чтобы их можно было напечатать.</span><span class="sxs-lookup"><span data-stu-id="7b45c-109">It can't correctly format invoices so that they can be printed.</span></span>

<span data-ttu-id="7b45c-110">Вместо этого можно использовать финансовую или бухгалтерскую систему для создания счетов для клиентов, которые используют данные из предложений счета, созданных в PSA.</span><span class="sxs-lookup"><span data-stu-id="7b45c-110">Instead, you can use a financial or accounting system to create customer-facing invoices that use the information from invoice proposals that are generated in PSA.</span></span>

## <a name="creating-project-invoices-in-psa"></a><span data-ttu-id="7b45c-111">Создание счетов по проекту в PSA</span><span class="sxs-lookup"><span data-stu-id="7b45c-111">Creating project invoices in PSA</span></span>

<span data-ttu-id="7b45c-112">Счета проекта можно создавать по отдельности или массово.</span><span class="sxs-lookup"><span data-stu-id="7b45c-112">Project invoices can be created one at a time or in bulk.</span></span> <span data-ttu-id="7b45c-113">Можно создавать их вручную или можно настроить таким образом, чтобы они создавались в автоматизированных прогонах.</span><span class="sxs-lookup"><span data-stu-id="7b45c-113">You can create them manually, or they can be configured so that they are generated in automated runs.</span></span>

### <a name="manually-create-project-invoices-in-psa"></a><span data-ttu-id="7b45c-114">Создание счетов проекта вручную в PSA</span><span class="sxs-lookup"><span data-stu-id="7b45c-114">Manually create project invoices in PSA</span></span>

<span data-ttu-id="7b45c-115">Со страницы списка **Контракты по проекту** можно создать счета по проекту отдельно для каждого контракта по проекту или можно создать счета пакетом для нескольких контрактов по проекту.</span><span class="sxs-lookup"><span data-stu-id="7b45c-115">From the **Project Contracts** list page, you can create project invoices separately for each project contract, or you can create invoices in bulk for multiple project contracts.</span></span>

<span data-ttu-id="7b45c-116">Выполните эти шаги для создания счета для конкретного контракта по проекту.</span><span class="sxs-lookup"><span data-stu-id="7b45c-116">Follow this step to create an invoice for a specific project contract.</span></span>

- <span data-ttu-id="7b45c-117">На странице списка **Контракты по проекту** откройте контракт по проекту, затем выберите **Создать счет**.</span><span class="sxs-lookup"><span data-stu-id="7b45c-117">On the **Project Contracts** list page, open a project contract, and then select **Create Invoice**.</span></span>

    ![Создание счетов по проекту для конкретного контракта по проекту](media/CreateProjectInvoicesOneByOne.png)

    <span data-ttu-id="7b45c-119">Счет создается для всех транзакций для выбранного контракта по проекту с состоянием **Готово к выставлению счета**.</span><span class="sxs-lookup"><span data-stu-id="7b45c-119">An invoice is generated for all transactions for the selected project contract that have a status of **Ready to Invoice**.</span></span> <span data-ttu-id="7b45c-120">Эти транзакции включают время, расходы, вехи и строки контракта на основании продукта.</span><span class="sxs-lookup"><span data-stu-id="7b45c-120">These transactions include time, expenses, milestones, and product-based contract lines.</span></span>

<span data-ttu-id="7b45c-121">Выполните следующие шаги для массового создания счетов.</span><span class="sxs-lookup"><span data-stu-id="7b45c-121">Follow these steps to create invoices in bulk.</span></span>

1. <span data-ttu-id="7b45c-122">На странице списка **Контракты по проекту** выберите один или несколько контрактов по проекту, для которых необходимо создать счет, затем выберите **Создать счета проекта**.</span><span class="sxs-lookup"><span data-stu-id="7b45c-122">On the **Project Contracts** list page, select one or more project contracts that you must create an invoice for, and then select **Create Project Invoices**.</span></span>

    ![Массовое создание счетов по проекту](media/CreateProjectInvoicesBulk.png)

    <span data-ttu-id="7b45c-124">Предупреждение информирует, что может быть задержка до того, как счета будут созданы.</span><span class="sxs-lookup"><span data-stu-id="7b45c-124">A warning message informs you that there might be a delay before invoices are created.</span></span> <span data-ttu-id="7b45c-125">Ход выполнения также отображается.</span><span class="sxs-lookup"><span data-stu-id="7b45c-125">The process is also shown.</span></span>

2. <span data-ttu-id="7b45c-126">Выберите **ОК**, чтобы закрыть окно сообщения.</span><span class="sxs-lookup"><span data-stu-id="7b45c-126">Select **OK** to close the message box.</span></span>

    <span data-ttu-id="7b45c-127">Счет создается для всех транзакций по строке контракта с состоянием **Готово к выставлению счета**.</span><span class="sxs-lookup"><span data-stu-id="7b45c-127">An invoice is generated for all transactions on a contract line that have a status of **Ready to Invoice**.</span></span> <span data-ttu-id="7b45c-128">Эти транзакции включают время, расходы, вехи и строки контракта на основании продукта.</span><span class="sxs-lookup"><span data-stu-id="7b45c-128">These transactions include time, expenses, milestones, and product-based contract lines.</span></span>

3. <span data-ttu-id="7b45c-129">Для просмотра созданных счетов выберите **Продажи** \> **Выставление счетов** \> **Счета**.</span><span class="sxs-lookup"><span data-stu-id="7b45c-129">To view the invoices that are generated, go to **Sales** \> **Billing** \> **Invoices**.</span></span> <span data-ttu-id="7b45c-130">Вы увидите по одному счету для каждого контракта по проекту.</span><span class="sxs-lookup"><span data-stu-id="7b45c-130">You will see one invoice for each project contract.</span></span>

### <a name="set-up-automated-creation-of-project-invoices-in-psa"></a><span data-ttu-id="7b45c-131">Настройка автоматизированного создания счетов по проекту в PSA</span><span class="sxs-lookup"><span data-stu-id="7b45c-131">Set up automated creation of project invoices in PSA</span></span>

<span data-ttu-id="7b45c-132">Выполните следующие шаги для настройки автоматического запуска выставления счетов в PSA.</span><span class="sxs-lookup"><span data-stu-id="7b45c-132">Follow these steps to configure an automated invoice run in PSA.</span></span>

1. <span data-ttu-id="7b45c-133">Перейдите в раздел **Project Service** \> **Параметры** \> **Пакетные задания**.</span><span class="sxs-lookup"><span data-stu-id="7b45c-133">Go to **Project Service** \> **Settings** \> **Batch jobs**.</span></span>
2. <span data-ttu-id="7b45c-134">Создайте пакетное задание и назовите его **Создание счетов PSA**.</span><span class="sxs-lookup"><span data-stu-id="7b45c-134">Create a batch job, and name it **PSA Create Invoices**.</span></span> <span data-ttu-id="7b45c-135">Имя пакетного задания должно включать термин "Создание счетов".</span><span class="sxs-lookup"><span data-stu-id="7b45c-135">The name of the batch job must include the term "Create Invoices."</span></span>
3. <span data-ttu-id="7b45c-136">В поле **Тип задания** выберите **Нет**.</span><span class="sxs-lookup"><span data-stu-id="7b45c-136">In the **Job type** field, select **None**.</span></span> <span data-ttu-id="7b45c-137">По умолчанию для параметров **Частота ежедневно** и **Активно** задано значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="7b45c-137">By default, the **Frequency Daily** and **Is Active** options are set to **Yes**.</span></span>
4. <span data-ttu-id="7b45c-138">Выберите **Запустить рабочий процесс**.</span><span class="sxs-lookup"><span data-stu-id="7b45c-138">Select **Run Workflow**.</span></span> <span data-ttu-id="7b45c-139">В диалоговом окне **Поиск в записях** отображаются три рабочих процесса:</span><span class="sxs-lookup"><span data-stu-id="7b45c-139">In the **Look Up Record** dialog box, you will see three workflows:</span></span>

    - <span data-ttu-id="7b45c-140">ProcessRunCaller</span><span class="sxs-lookup"><span data-stu-id="7b45c-140">ProcessRunCaller</span></span>
    - <span data-ttu-id="7b45c-141">ProcessRunner</span><span class="sxs-lookup"><span data-stu-id="7b45c-141">ProcessRunner</span></span>
    - <span data-ttu-id="7b45c-142">UpdateRoleUtilization</span><span class="sxs-lookup"><span data-stu-id="7b45c-142">UpdateRoleUtilization</span></span>

5. <span data-ttu-id="7b45c-143">Выберите **ProcessRunCaller**, затем выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="7b45c-143">Select **ProcessRunCaller**, and then select **Add**.</span></span>
6. <span data-ttu-id="7b45c-144">В следующем диалоговом окне выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="7b45c-144">In the next dialog box, select **OK**.</span></span> <span data-ttu-id="7b45c-145">За рабочим процессом **Сон** следует рабочий процесс **Обработка**.</span><span class="sxs-lookup"><span data-stu-id="7b45c-145">A **Sleep** workflow is followed by a **Process** workflow.</span></span>

    <span data-ttu-id="7b45c-146">Можно также выбрать **ProcessRunner** на шаге 5.</span><span class="sxs-lookup"><span data-stu-id="7b45c-146">You can also select **ProcessRunner** in step 5.</span></span> <span data-ttu-id="7b45c-147">Затем при выборе **OK** за рабочим процессом **Обработка** следует рабочий процесс **Сон**.</span><span class="sxs-lookup"><span data-stu-id="7b45c-147">Then, when you select **OK**, a **Process** workflow is followed by a **Sleep** workflow.</span></span>

<span data-ttu-id="7b45c-148">Рабочие процессы **ProcessRunCaller** и **ProcessRunner** создают счета.</span><span class="sxs-lookup"><span data-stu-id="7b45c-148">The **ProcessRunCaller** and **ProcessRunner** workflows create invoices.</span></span> <span data-ttu-id="7b45c-149">**ProcessRunCaller** вызывает **ProcessRunner**.</span><span class="sxs-lookup"><span data-stu-id="7b45c-149">**ProcessRunCaller** calls **ProcessRunner**.</span></span> <span data-ttu-id="7b45c-150">Счета фактически создаются рабочим процессом **ProcessRunner**.</span><span class="sxs-lookup"><span data-stu-id="7b45c-150">**ProcessRunner** is the workflow that actually creates the invoices.</span></span> <span data-ttu-id="7b45c-151">Он перебирает все строки контракта, для которых должны быть созданы счета, и создает счета для этих строк.</span><span class="sxs-lookup"><span data-stu-id="7b45c-151">It goes through all the contract lines that invoices must be created for, and it creates invoices for those lines.</span></span> <span data-ttu-id="7b45c-152">Чтобы определить строки контракта, для которых должны быть созданы счета, задание проверяет даты запуска счетов для строк контракта.</span><span class="sxs-lookup"><span data-stu-id="7b45c-152">To determine the contract lines that invoices must be created for, the job looks at invoice run dates for the contract lines.</span></span> <span data-ttu-id="7b45c-153">Если строки контракта, принадлежащие к одному контракту, имеют одинаковую дату запуска счета, транзакции объединяются в один счет с двумя строками счета.</span><span class="sxs-lookup"><span data-stu-id="7b45c-153">If contract lines that belong to one contract have the same invoice run date, the transactions are combined into one invoice that has two invoice lines.</span></span> <span data-ttu-id="7b45c-154">Если транзакции, для которых требуется создать счета, отсутствуют, задание пропускает создание счета.</span><span class="sxs-lookup"><span data-stu-id="7b45c-154">If there are no transactions to create invoices for, the job skips invoice creation.</span></span>

<span data-ttu-id="7b45c-155">После завершения работы **ProcessRunner** он вызывает **ProcessRunCaller**, предоставляет время завершения и закрывается.</span><span class="sxs-lookup"><span data-stu-id="7b45c-155">After **ProcessRunner** has finished running, it calls **ProcessRunCaller**, provides the end time, and is closed.</span></span> <span data-ttu-id="7b45c-156">**ProcessRunCaller** затем запускает таймер, который работает 24 часа с указанного времени завершения.</span><span class="sxs-lookup"><span data-stu-id="7b45c-156">**ProcessRunCaller** then starts a timer that runs for 24 hours from the specified end time.</span></span> <span data-ttu-id="7b45c-157">По завершении работы таймера процесс **ProcessRunCaller** закрывается.</span><span class="sxs-lookup"><span data-stu-id="7b45c-157">At the end of the timer, **ProcessRunCaller** is closed.</span></span>

<span data-ttu-id="7b45c-158">Задание пакетной обработки для создания счетов — это повторяющееся задание.</span><span class="sxs-lookup"><span data-stu-id="7b45c-158">The batch process job for creating invoices is a recurrent job.</span></span> <span data-ttu-id="7b45c-159">Если это процесс пакетной обработки запускается много раз, создается несколько экземпляров задания, что вызывает ошибки.</span><span class="sxs-lookup"><span data-stu-id="7b45c-159">If this batch process is run many times, multiple instances of the job are created and cause errors.</span></span> <span data-ttu-id="7b45c-160">Следовательно, необходимо запустить пакетный процесс только один раз, и заново запускать его следует только в том случае, если он перестал работать.</span><span class="sxs-lookup"><span data-stu-id="7b45c-160">Therefore, you should start the batch process only one time, and you should restart it only if it stops running.</span></span>
 
### <a name="edit-a-draft-psa-invoice"></a><span data-ttu-id="7b45c-161">Изменение черновика счета PSA</span><span class="sxs-lookup"><span data-stu-id="7b45c-161">Edit a draft PSA invoice</span></span>

<span data-ttu-id="7b45c-162">При создании черновика счета по проекту все транзакции продаж, за которые не выставлены счета, созданные, когда записи времени и расходов были утверждены, выбираются в счет.</span><span class="sxs-lookup"><span data-stu-id="7b45c-162">When you create a draft project invoice, all unbilled sales transactions that were created when the time and expense entries were approved are pulled onto the invoice.</span></span> <span data-ttu-id="7b45c-163">Можно внести следующие корректировки, пока счет по-прежнему на этапе черновика:</span><span class="sxs-lookup"><span data-stu-id="7b45c-163">You can make the following adjustments while the invoice is still in a draft stage:</span></span>

- <span data-ttu-id="7b45c-164">Удаление или изменение сведений строки счета.</span><span class="sxs-lookup"><span data-stu-id="7b45c-164">Delete or edit invoice line details.</span></span>
- <span data-ttu-id="7b45c-165">Изменение и корректировка количества и типа выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="7b45c-165">Edit and adjust the quantity and billing type.</span></span>
- <span data-ttu-id="7b45c-166">Прямое добавление времени, расходов и сборов в качестве транзакций по счету.</span><span class="sxs-lookup"><span data-stu-id="7b45c-166">Directly add time, expense, and fees as transactions on the invoice.</span></span> <span data-ttu-id="7b45c-167">Можно использовать эту функцию, если строка счета сопоставлена строке контракта, которая допускает эти классы транзакций.</span><span class="sxs-lookup"><span data-stu-id="7b45c-167">You can use this feature if the invoice line is mapped to a contract line that allows for these transaction classes.</span></span>

<span data-ttu-id="7b45c-168">Выберите **Подтвердить**, чтобы подтвердить счет.</span><span class="sxs-lookup"><span data-stu-id="7b45c-168">Select **Confirm** to confirm an invoice.</span></span> <span data-ttu-id="7b45c-169">Действие подтверждения является односторонним.</span><span class="sxs-lookup"><span data-stu-id="7b45c-169">The Confirm action is a one-way action.</span></span> <span data-ttu-id="7b45c-170">Если вы выбираете **Подтвердить**, система делает счет доступным только для чтения и создает фактические данные продаж с выставленными счетами из каждых сведений строки счета для каждой строки счета.</span><span class="sxs-lookup"><span data-stu-id="7b45c-170">When you select **Confirm**, the system makes the invoice read-only and creates billed sales actuals from each invoice line detail for each invoice line.</span></span> <span data-ttu-id="7b45c-171">Если сведения строки счета ссылаются на фактические данные продаж, за которые не выставлены счета, система также реверсирует фактические данные продаж, за которые не выставлены счета.</span><span class="sxs-lookup"><span data-stu-id="7b45c-171">If the invoice line detail references an unbilled sales actual, the system also reverses the unbilled sales actual.</span></span> <span data-ttu-id="7b45c-172">(Любые сведения строки счета, которые были созданы из записи времени и расходов, будут ссылаться на фактические данные продаж с невыставленными счетами.) Системы интеграции главной книги могут использовать это обращение для обращения незавершенной работы (НЗП) для целей бухгалтерского учета.</span><span class="sxs-lookup"><span data-stu-id="7b45c-172">(Any invoice line detail that was created from a time or expense entry will reference an unbilled sales actual.) General ledger integration systems can use this reversal to reverse project work in progress (WIP) for accounting purposes.</span></span>

### <a name="correct-a-confirmed-psa-invoice"></a><span data-ttu-id="7b45c-173">Исправление утвержденного счета PSA</span><span class="sxs-lookup"><span data-stu-id="7b45c-173">Correct a confirmed PSA invoice</span></span>

<span data-ttu-id="7b45c-174">Утвержденные счета PSA можно редактировать (корректировать).</span><span class="sxs-lookup"><span data-stu-id="7b45c-174">Confirmed PSA invoices can be edited (corrected).</span></span> <span data-ttu-id="7b45c-175">При исправлении утвержденного счета создается черновик нового корректирующего счета.</span><span class="sxs-lookup"><span data-stu-id="7b45c-175">When you correct a confirmed invoice, a new draft corrective invoice is created.</span></span> <span data-ttu-id="7b45c-176">Поскольку предполагается, что требуется реверсировать все транзакции и количества из первоначального счетов, этот корректирующий счет включает все транзакции из первоначального счета, и все количества в нем равны 0 (нулю).</span><span class="sxs-lookup"><span data-stu-id="7b45c-176">Because the assumption is that you want to reverse all the transactions and quantities from the original invoice, this corrective invoice includes all the transactions from the original invoice, and all the quantities on it are 0 (zero).</span></span>

<span data-ttu-id="7b45c-177">Если какие-либо транзакции не требуют исправления, можно удалить их из черновика корректирующего счета.</span><span class="sxs-lookup"><span data-stu-id="7b45c-177">If any transactions don't require correction, you can remove them from the draft corrective invoice.</span></span> <span data-ttu-id="7b45c-178">Если требуется реверсировать или вернуть только часть количества, можно изменить поле **Количество** в сведениях строки.</span><span class="sxs-lookup"><span data-stu-id="7b45c-178">If you want to reverse or return only a partial quantity, you can edit the **Quantity** field on the line detail.</span></span> <span data-ttu-id="7b45c-179">Если открыть сведения строки счета, можно просмотреть первоначальное количество по счету.</span><span class="sxs-lookup"><span data-stu-id="7b45c-179">If you open the invoice line detail, you can see the original invoice quantity.</span></span> <span data-ttu-id="7b45c-180">Затем можно изменить текущее количество по счету, чтобы оно было меньше или больше количества по первоначальному счету.</span><span class="sxs-lookup"><span data-stu-id="7b45c-180">You can then edit the current invoice quantity so that it's less than or more than the original invoice quantity.</span></span>

<span data-ttu-id="7b45c-181">При утверждении корректирующего счета фактические значения исходных выставленных продаж реверсируется, и создаются новые фактические данные продаж, за которые выставлен счет.</span><span class="sxs-lookup"><span data-stu-id="7b45c-181">When you confirm a corrective invoice, the original billed sales actual is reversed, and a new billed sales actual is created.</span></span> <span data-ttu-id="7b45c-182">Если количество было уменьшено, разница вызовет также создание новых фактических данных продаж, за которые не выставлен счет.</span><span class="sxs-lookup"><span data-stu-id="7b45c-182">If the quantity was reduced, the difference will cause a new unbilled sales actual to be created too.</span></span> <span data-ttu-id="7b45c-183">Например, если исходный выставленный счет продаж был за восемь часов, а в сведениях по строке корректирующего счета количество уменьшено до 6 часов, PSA обращает исходную строку счета продаж и создает два новых фактических значения:</span><span class="sxs-lookup"><span data-stu-id="7b45c-183">For example, if the original billed sales was for eight hours, and the corrective invoice line detail has a reduced quantity of six hours, PSA reverses the original billed sales line and creates two new actuals:</span></span>

- <span data-ttu-id="7b45c-184">Фактические данные выставленного счета продаж на 6 часов.</span><span class="sxs-lookup"><span data-stu-id="7b45c-184">A billed sales actual for six hours.</span></span>
- <span data-ttu-id="7b45c-185">Фактические данные продаж на остальные 2 часа, за которые счет не выставлен.</span><span class="sxs-lookup"><span data-stu-id="7b45c-185">An unbilled sales actual for the remaining two hours.</span></span> <span data-ttu-id="7b45c-186">За эту транзакцию можно выставить счет позднее или ее можно пометить как не подлежащую оплате, в зависимости от переговоров с клиентом.</span><span class="sxs-lookup"><span data-stu-id="7b45c-186">This transaction can either be billed later or marked as non-chargeable, depending on the negotiations with the customer.</span></span>