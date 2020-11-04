---
title: Отзыв утвержденных записей времени или расходов
description: В этом разделе представлена информация о том, как отозвать ранее утвержденную транзакцию времени или расходов.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: ''
ms.author: rumant
ms.date: 03/08/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 7bacd70881a6c463cc449a365173da5338a3d3fc
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083235"
---
# <a name="recall-approved-time-or-expense-entries"></a><span data-ttu-id="d347d-103">Отзыв утвержденных записей времени или расходов</span><span class="sxs-lookup"><span data-stu-id="d347d-103">Recall approved time or expense entries</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="d347d-104">Участник рабочей группы проекта или другое лицо, представляющее запись времени или расходов, могут отозвать эту запись времени или расходов после ее утверждения.</span><span class="sxs-lookup"><span data-stu-id="d347d-104">A project team member or an other person who submits a time or expense entry can recall that time or expense entry after it has been approved.</span></span> <span data-ttu-id="d347d-105">Процесс отзыва утвержденной записи времени или расходов состоит из двух шагов:</span><span class="sxs-lookup"><span data-stu-id="d347d-105">The process for recalling an approved time or expense entry has two steps:</span></span>

1. <span data-ttu-id="d347d-106">Отправитель запрашивает отзыв.</span><span class="sxs-lookup"><span data-stu-id="d347d-106">A submitter requests a recall.</span></span>
2. <span data-ttu-id="d347d-107">Утверждающий утверждает отзыв.</span><span class="sxs-lookup"><span data-stu-id="d347d-107">An approver approves the recall.</span></span>

## <a name="request-a-recall"></a><span data-ttu-id="d347d-108">Запрос на отзыв</span><span class="sxs-lookup"><span data-stu-id="d347d-108">Request a recall</span></span>

<span data-ttu-id="d347d-109">Выполните следующие шаги для запроса отзыва утвержденной записи времени или расходов.</span><span class="sxs-lookup"><span data-stu-id="d347d-109">Follow these steps to request a recall of an approved time or expense entry.</span></span>

1. <span data-ttu-id="d347d-110">Для записей времени откройте **Проекты** \> **Моя работа** \> **Запись времени**.</span><span class="sxs-lookup"><span data-stu-id="d347d-110">For time entries, go to **Projects** \> **My Work** \> **Time Entry**.</span></span>

    <span data-ttu-id="d347d-111">–или–</span><span class="sxs-lookup"><span data-stu-id="d347d-111">–or–</span></span>

    <span data-ttu-id="d347d-112">Для записей расходов откройте **Проекты** \> **Моя работа** \> **Расходы**.</span><span class="sxs-lookup"><span data-stu-id="d347d-112">For expense entries, go to **Projects** \> **My Work** \> **Expenses**.</span></span>

2. <span data-ttu-id="d347d-113">Для записей времени выберите все записи времени для определенного сочетания проекта и задачи.</span><span class="sxs-lookup"><span data-stu-id="d347d-113">For time entries, select all the time entries for a specific combination of a project and a task.</span></span> <span data-ttu-id="d347d-114">Альтернативно, в сетке выберите отдельные ячейки для времени в конкретный день для определенного проекта.</span><span class="sxs-lookup"><span data-stu-id="d347d-114">Alternatively, in the grid, select the individual cells for time on a specific date for a specific project.</span></span>

    <span data-ttu-id="d347d-115">–или–</span><span class="sxs-lookup"><span data-stu-id="d347d-115">–or–</span></span>

    <span data-ttu-id="d347d-116">Для записей расходов выберите строку для записи расходов, которую требуется отозвать.</span><span class="sxs-lookup"><span data-stu-id="d347d-116">For expense entries, select the row for the expense entry to recall.</span></span>

3. <span data-ttu-id="d347d-117">Выберите **Отозвать**.</span><span class="sxs-lookup"><span data-stu-id="d347d-117">Select **Recall**.</span></span> <span data-ttu-id="d347d-118">Открывается диалоговое окно запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="d347d-118">A confirmation dialog box appears.</span></span> <span data-ttu-id="d347d-119">Если выбранные записи времени и расходов были уже утверждены, будет предложено ввести причину отзыва.</span><span class="sxs-lookup"><span data-stu-id="d347d-119">If the selected time and expense entries were already approved, you're prompted to enter a reason for the recall.</span></span>
4. <span data-ttu-id="d347d-120">Введите причину отзыва, затем выберите **ОК** , чтобы подтвердить операцию.</span><span class="sxs-lookup"><span data-stu-id="d347d-120">Enter a reason for the recall, and then select **OK** to confirm the operation.</span></span> <span data-ttu-id="d347d-121">Система отправляет лицу, которое утвердило записи, запрос на утверждения отзыва.</span><span class="sxs-lookup"><span data-stu-id="d347d-121">The system sends the person who approved the entries a request to approve the recall.</span></span>

> [!NOTE]
> <span data-ttu-id="d347d-122">Хотя утвержденные записи времени и расходов можно отозвать, если за утвержденное время или расход уже выставлен счет клиенту, создать запрос на отзыв невозможно.</span><span class="sxs-lookup"><span data-stu-id="d347d-122">Although approved time and expense entries can be recalled, if an approved time or expense has already been invoiced to the customer, a recall request can't be created.</span></span> <span data-ttu-id="d347d-123">Пользователь при попытке создать запрос на отзыв получит сообщение о том, что время или расход невозможно отозвать, поскольку за них уже был выставлен счет.</span><span class="sxs-lookup"><span data-stu-id="d347d-123">A user who tries to create a recall request will receive a message that states that the time or expense can't be recalled because it was already invoiced.</span></span>

## <a name="approve-or-reject-a-recall-request"></a><span data-ttu-id="d347d-124">Утверждение или отклонение запроса на отзыв</span><span class="sxs-lookup"><span data-stu-id="d347d-124">Approve or reject a recall request</span></span>

<span data-ttu-id="d347d-125">Выполните следующие шаги, чтобы утвердить или отклонить запрос на отзыв.</span><span class="sxs-lookup"><span data-stu-id="d347d-125">Follow these steps to approve or reject a recall request.</span></span>

1. <span data-ttu-id="d347d-126">Перейдите в раздел **Проекты** \> **Моя работа** \> **Утверждения**.</span><span class="sxs-lookup"><span data-stu-id="d347d-126">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="d347d-127">На странице списка **Утверждения** измените представление на **Запросы на отзыв для утверждения**.</span><span class="sxs-lookup"><span data-stu-id="d347d-127">On the **Approvals** list page, change the view to **Recall requests for approval**.</span></span> <span data-ttu-id="d347d-128">Отображается список отправленных запросов на отзыв.</span><span class="sxs-lookup"><span data-stu-id="d347d-128">A list of submitted recall requests is shown.</span></span>
3. <span data-ttu-id="d347d-129">Выберите одну или несколько записей, затем выберите **Утвердить** или **Отклонить**.</span><span class="sxs-lookup"><span data-stu-id="d347d-129">Select one or more entries, and then select either **Approve** or **Reject**.</span></span>
4. <span data-ttu-id="d347d-130">Если выбрано значение **Утвердить** , вы получите предупреждение, поясняющее последствия утверждения.</span><span class="sxs-lookup"><span data-stu-id="d347d-130">If you selected **Approve** , you receive a warning message that explains the impact of the approval.</span></span> <span data-ttu-id="d347d-131">Чтобы подтвердить операцию, выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d347d-131">Select **OK** to confirm the operation.</span></span> <span data-ttu-id="d347d-132">Запрос на отзыв утвержден.</span><span class="sxs-lookup"><span data-stu-id="d347d-132">The recall request is approved.</span></span>

    <span data-ttu-id="d347d-133">–или–</span><span class="sxs-lookup"><span data-stu-id="d347d-133">–or–</span></span>

    <span data-ttu-id="d347d-134">Если выбрано **Отклонить** , запрос на отзыв отклоняется.</span><span class="sxs-lookup"><span data-stu-id="d347d-134">If you selected **Reject** , the recall request is rejected.</span></span>

> [!NOTE]
> <span data-ttu-id="d347d-135">Как и при запросе отзыва, при утверждении отзыва система проверяет наличие каких-либо действий по выставлению счетов по записям времени или расхода.</span><span class="sxs-lookup"><span data-stu-id="d347d-135">As when a recall is requested, when a recall is approved, the system checks for any invoicing activity on the time or expense entries.</span></span> <span data-ttu-id="d347d-136">Если для записи уже выставлен счет или она включена в черновик счете, утверждающий получит сообщение об ошибке с сообщением о том, что время и расход нельзя утвердить для отзыва, поскольку за них уже был выставлен счет.</span><span class="sxs-lookup"><span data-stu-id="d347d-136">If an entry was already invoiced, or if it's on a draft invoice, the approver will receive an error message that states that the time or expense can't be approved for recall, because it was already invoiced.</span></span>

## <a name="impact-of-a-recall-request"></a><span data-ttu-id="d347d-137">Влияние запроса на отзыв</span><span class="sxs-lookup"><span data-stu-id="d347d-137">Impact of a recall request</span></span>

<span data-ttu-id="d347d-138">Когда утверждение отозвано, имеются операционные и финансовые последствия.</span><span class="sxs-lookup"><span data-stu-id="d347d-138">When an approval is recalled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="d347d-139">Операционные последствия</span><span class="sxs-lookup"><span data-stu-id="d347d-139">Operational impact</span></span>

<span data-ttu-id="d347d-140">Если запрос на отзыв одобрен, запись утверждения отмечается как **Отклонено**.</span><span class="sxs-lookup"><span data-stu-id="d347d-140">If a recall request is approved, the approval record is marked as **Rejected**.</span></span> <span data-ttu-id="d347d-141">Состояние записи изменяется на **Возвращено** или **Отклонено** , в зависимости от того, какая это запись: запись времени или запись расхода.</span><span class="sxs-lookup"><span data-stu-id="d347d-141">The status of the entry is changed to either **Returned** or **Rejected** , depending on whether it's a time entry or an expense entry.</span></span>

<span data-ttu-id="d347d-142">Участник рабочей группы по проекту может просмотреть записи, изменить и снова отправить их либо полностью удалить записи.</span><span class="sxs-lookup"><span data-stu-id="d347d-142">The project team member can view entries, edit and then resubmit entries, or delete entries entirely.</span></span>

<span data-ttu-id="d347d-143">Если запрос на отзыв отклонен, состояние записи остается **Утверждено** , и запись не может быть изменена участником проектной группы или утверждающим для проекта.</span><span class="sxs-lookup"><span data-stu-id="d347d-143">If a recall request is rejected, the status of the entry remains **Approved** , and the entry can't be edited by the project team member or the approver for the project.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="d347d-144">Финансовые последствия</span><span class="sxs-lookup"><span data-stu-id="d347d-144">Financial impact</span></span>

<span data-ttu-id="d347d-145">Если запрос на отзыв утвержден, соответствующие фактические данные для стоимости и продаж обновляются следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d347d-145">If a recall request is approved, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="d347d-146">Поле **Состояние корректировки** обновляется до **Скорректировано**.</span><span class="sxs-lookup"><span data-stu-id="d347d-146">The **Adjustment Status** field is updated to **Adjusted**.</span></span>
- <span data-ttu-id="d347d-147">Поле **Состояние выставления счета** обновляется до **Отменено**.</span><span class="sxs-lookup"><span data-stu-id="d347d-147">The **Billing Status** field is updated to **Canceled**.</span></span>

<span data-ttu-id="d347d-148">Затем создаются записи реверсирования в таблице фактических данных.</span><span class="sxs-lookup"><span data-stu-id="d347d-148">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="d347d-149">Для создания записей реверсирования система копирует значения полей из первоначальных фактических данных.</span><span class="sxs-lookup"><span data-stu-id="d347d-149">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="d347d-150">Единственные значения, которые не будут скопированы, — это значения количества.</span><span class="sxs-lookup"><span data-stu-id="d347d-150">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="d347d-151">Вместо этого эти значения обращаются.</span><span class="sxs-lookup"><span data-stu-id="d347d-151">These values are reversed instead.</span></span> <span data-ttu-id="d347d-152">Обращенные фактические значения создаются для фактических значений **Стоимость** и **Продажи без выставления счета**.</span><span class="sxs-lookup"><span data-stu-id="d347d-152">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="d347d-153">В поле **Состояние корректировки** для реверсированных фактических данных задается значение **Не регулируется** , а в поле **Состояние выставления счета** устанавливается значение **Отменено**.</span><span class="sxs-lookup"><span data-stu-id="d347d-153">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable** , and the **Billing status** field is set to **Canceled**.</span></span> <span data-ttu-id="d347d-154">Из-за этих изменений записанная невыполненная работа по расходам и доходам по проекту перестанет учитывать суммы, которые представляют эти фактические данные.</span><span class="sxs-lookup"><span data-stu-id="d347d-154">Because of these changes, the recorded spending and the revenue backlog on the project will no longer account for the amounts that these actuals represent.</span></span>

<span data-ttu-id="d347d-155">Если запрос на отзыв отклонен, это не имеет финансовых последствий для проекта.</span><span class="sxs-lookup"><span data-stu-id="d347d-155">If a recall request is rejected, there is no financial impact on the project.</span></span>

## <a name="changes-to-time-entry-records"></a><span data-ttu-id="d347d-156">Изменения записей ввода времени</span><span class="sxs-lookup"><span data-stu-id="d347d-156">Changes to time entry records</span></span>

<span data-ttu-id="d347d-157">На следующей иллюстрации показаны изменения, которые происходят для утвержденных записей времени в случае их отзыва.</span><span class="sxs-lookup"><span data-stu-id="d347d-157">The following illustration shows the changes that occur for approved time entries when they are recalled.</span></span>

![Переходы статуса записи времени](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-entry-records"></a><span data-ttu-id="d347d-159">Изменения записей ввода расходов</span><span class="sxs-lookup"><span data-stu-id="d347d-159">Changes to expense entry records</span></span>

<span data-ttu-id="d347d-160">На следующей иллюстрации показаны изменения, которые происходят для утвержденных записей расходов в случае их отзыва.</span><span class="sxs-lookup"><span data-stu-id="d347d-160">The following illustration shows the changes that occur for approved expense entries when they are recalled.</span></span>

![Переходы статуса записи расходов](media/ExpenseEntryStateTransitions.png)
