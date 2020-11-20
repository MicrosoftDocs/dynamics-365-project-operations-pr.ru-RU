---
title: Отмена ранее одобренных записей времени и расходов
description: В этом разделе представлена информация о том, как отменить утвержденную транзакцию времени или расходов проекта.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 84fc057599dd98162320d6104ed4a7612e894ecb
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123349"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a><span data-ttu-id="bface-103">Отмена ранее одобренных записей времени или расходов</span><span class="sxs-lookup"><span data-stu-id="bface-103">Cancel previously approved time or expense entries</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="bface-104">В последней версии Dynamics 365 Project Service Automation утверждающие могут отменить записи времени или расходов, которые они одобрили ранее.</span><span class="sxs-lookup"><span data-stu-id="bface-104">In the latest version of Dynamics 365 Project Service Automation, approvers can cancel time or expense entries that they previously approved.</span></span>

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a><span data-ttu-id="bface-105">Отмена ранее одобренной записи времени или расходов</span><span class="sxs-lookup"><span data-stu-id="bface-105">Cancel a previously approved time or expense entry</span></span>

<span data-ttu-id="bface-106">Выполните следующие шаги для отмены записи времени или расходов, которую вы ранее утвердили.</span><span class="sxs-lookup"><span data-stu-id="bface-106">Follow these steps to cancel a time or expense entry that you previously approved.</span></span>

1. <span data-ttu-id="bface-107">Перейдите в раздел **Проекты** \> **Моя работа** \> **Утверждения**.</span><span class="sxs-lookup"><span data-stu-id="bface-107">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="bface-108">На странице списка **Утверждения** измените представление на **Мои прошлые утверждения**.</span><span class="sxs-lookup"><span data-stu-id="bface-108">On the **Approvals** list page, change the view to **My past approvals**.</span></span> <span data-ttu-id="bface-109">Будет показан список записей времени и расходов, которые вы ранее одобрили.</span><span class="sxs-lookup"><span data-stu-id="bface-109">A list of the time and expense entries that you previously approved is shown.</span></span>
3. <span data-ttu-id="bface-110">Выберите одну или несколько записей, затем выберите **Отменить утверждение**.</span><span class="sxs-lookup"><span data-stu-id="bface-110">Select one or more entries, and then select **Cancel approval**.</span></span> <span data-ttu-id="bface-111">Вы получите предупреждение.</span><span class="sxs-lookup"><span data-stu-id="bface-111">You receive a warning message.</span></span>
4. <span data-ttu-id="bface-112">Выберите **OK**, чтобы отменить утверждение.</span><span class="sxs-lookup"><span data-stu-id="bface-112">Select **OK** to cancel the approval.</span></span>

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a><span data-ttu-id="bface-113">Сведения о влиянии отмены утверждения записи времени или расходов</span><span class="sxs-lookup"><span data-stu-id="bface-113">Understand the impact of canceling a time or expense entry approval</span></span>

<span data-ttu-id="bface-114">Когда утверждение отменено, имеются операционные и финансовые последствия.</span><span class="sxs-lookup"><span data-stu-id="bface-114">When an approval is canceled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="bface-115">Операционные последствия</span><span class="sxs-lookup"><span data-stu-id="bface-115">Operational impact</span></span>

<span data-ttu-id="bface-116">На стороне операций при отмене утверждения состояние записи сбрасывается на **Черновик**, и утверждение больше не отображается в представлении **Мои прошлые утверждения**.</span><span class="sxs-lookup"><span data-stu-id="bface-116">On the operations side, when an approval is canceled, the status of the record is reset to **Draft**, and the approval no longer appears in the **My past approvals** view.</span></span> <span data-ttu-id="bface-117">Вместо этого отмененное утверждение появляется в представлении **Записи времени для утверждения** или представлении **Записи расхода на утверждение**, в зависимости от того, была ли это запись времени или запись расходов.</span><span class="sxs-lookup"><span data-stu-id="bface-117">Instead, the canceled approval appears in either the **Time entries for approval** view or the **Expense entries for approval** view, depending on whether it was a time entry or an expense entry.</span></span> <span data-ttu-id="bface-118">Кроме того, состояние соответствующей записи времени или расхода изменяется на **Отправлено**, чтобы соответствующая запись соответствовала утверждения с состоянием **Черновик**.</span><span class="sxs-lookup"><span data-stu-id="bface-118">Additionally, the status of the related time or expense entry is changed to **Submitted**, so that the related entry is consistent with approvals that have a status of **Draft**.</span></span>

<span data-ttu-id="bface-119">Как утверждающий, вы можете изменять некоторые поля утверждения, которое имеет статус **Черновик**.</span><span class="sxs-lookup"><span data-stu-id="bface-119">As an approver, you can edit some of the fields of an approval that has a status of **Draft**.</span></span> <span data-ttu-id="bface-120">Эти поля включают **Тип выставления счетов** и **Оплачиваемые часы для записей времени**.</span><span class="sxs-lookup"><span data-stu-id="bface-120">These fields include **Billing Type** and **Billable Hours for Time Entries**.</span></span> <span data-ttu-id="bface-121">После внесения изменений можно утвердить запись повторно.</span><span class="sxs-lookup"><span data-stu-id="bface-121">After you make changes, you can approve the record again.</span></span> <span data-ttu-id="bface-122">Можно также отклонить запись.</span><span class="sxs-lookup"><span data-stu-id="bface-122">Alternatively, you can reject the entry.</span></span> <span data-ttu-id="bface-123">Если вы отклонили утверждение записи времени, состояние записи изменяется на **Возвращено**.</span><span class="sxs-lookup"><span data-stu-id="bface-123">If you reject the approval of a time entry, the status of the entry is changed to **Returned**.</span></span> <span data-ttu-id="bface-124">Если вы отклонили утверждение записи расхода, состояние записи изменяется на **Отклонено**.</span><span class="sxs-lookup"><span data-stu-id="bface-124">If you reject the approval of an expense entry, the status is changed to **Rejected**.</span></span> <span data-ttu-id="bface-125">Функционально возвращенные и отклоненные записи ведут себя так же, как записи в состоянии **Черновик**.</span><span class="sxs-lookup"><span data-stu-id="bface-125">Functionally, both returned and rejected entries behave the same as an entry that has a status of **Draft**.</span></span> <span data-ttu-id="bface-126">Участник рабочей группы проекта может внести все требуемые изменения в заново отправить ее на утверждение или полностью удалить запись.</span><span class="sxs-lookup"><span data-stu-id="bface-126">A project team member can either make any required changes to the entry and then resubmit it for approval, or delete the entry entirely.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="bface-127">Финансовые последствия</span><span class="sxs-lookup"><span data-stu-id="bface-127">Financial impact</span></span>

<span data-ttu-id="bface-128">При отмене утверждения для проект также имеются финансовые последствия.</span><span class="sxs-lookup"><span data-stu-id="bface-128">A project is also affected financially when an approval is canceled.</span></span> <span data-ttu-id="bface-129">Сначала соответствующие фактические данные для стоимости и продаж обновляются следующим образом:</span><span class="sxs-lookup"><span data-stu-id="bface-129">First, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="bface-130">Для состояния корректировки задается значение **Скорректировано**.</span><span class="sxs-lookup"><span data-stu-id="bface-130">The adjustment status is set to **Adjusted**.</span></span>
- <span data-ttu-id="bface-131">Для состояния выставления счета задается значение **Отменено**.</span><span class="sxs-lookup"><span data-stu-id="bface-131">The billing status is set to **Canceled**.</span></span>

<span data-ttu-id="bface-132">Затем создаются записи реверсирования в таблице фактических данных.</span><span class="sxs-lookup"><span data-stu-id="bface-132">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="bface-133">Для создания записей реверсирования система копирует значения полей из первоначальных фактических данных.</span><span class="sxs-lookup"><span data-stu-id="bface-133">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="bface-134">Единственные значения, которые не будут скопированы, — это значения количества.</span><span class="sxs-lookup"><span data-stu-id="bface-134">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="bface-135">Вместо этого эти значения обращаются.</span><span class="sxs-lookup"><span data-stu-id="bface-135">These values are reversed instead.</span></span> <span data-ttu-id="bface-136">Обращенные фактические значения создаются для фактических значений **Стоимость** и **Продажи без выставления счета**.</span><span class="sxs-lookup"><span data-stu-id="bface-136">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="bface-137">В поле **Состояние корректировки** для реверсированных фактических данных задается значение **Не регулируется**, а для состояния выставления счета устанавливается значение **Отменено**.</span><span class="sxs-lookup"><span data-stu-id="bface-137">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable**, and the billing status is set to **Canceled**.</span></span>

<span data-ttu-id="bface-138">После выполнения этих изменений сумма записывается как потраченная на проект, и невыполненная работа по доходам по проекту перестанет учитывать суммы, которые представляют эти фактические данные.</span><span class="sxs-lookup"><span data-stu-id="bface-138">After these changes are made, the amount that is recorded as spent on the project and the revenue backlog on the project will longer account for the amounts that these actuals represent.</span></span>
