---
title: Обзор строк предложения с расценками по проекту
description: В этой теме дана информация об использовании строк предложения с расценками для проектной работы.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fa48a90c275eae1b0c0dbce685ae718dd9674c88
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858048"
---
# <a name="project-quote-lines-overview"></a><span data-ttu-id="69350-103">Обзор строк предложения с расценками по проекту</span><span class="sxs-lookup"><span data-stu-id="69350-103">Project quote lines overview</span></span>

<span data-ttu-id="69350-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/без запасов_</span><span class="sxs-lookup"><span data-stu-id="69350-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="69350-105">Строки предложений с расценками на основе проекта предназначены для помощи в оценке проектной работы по заданию.</span><span class="sxs-lookup"><span data-stu-id="69350-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="69350-106">Структура строки предложения с расценками по проекту расширена для оценок проекта за счет следующих понятий:</span><span class="sxs-lookup"><span data-stu-id="69350-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="69350-107">Метод выставления счета</span><span class="sxs-lookup"><span data-stu-id="69350-107">Billing Method</span></span>
- <span data-ttu-id="69350-108">Сопоставление проекта</span><span class="sxs-lookup"><span data-stu-id="69350-108">Project Mapping</span></span>
- <span data-ttu-id="69350-109">Включенные классы транзакций</span><span class="sxs-lookup"><span data-stu-id="69350-109">Included Transaction classes</span></span>
- <span data-ttu-id="69350-110">Максимальный лимит</span><span class="sxs-lookup"><span data-stu-id="69350-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="69350-111">Настройка возможности оплаты</span><span class="sxs-lookup"><span data-stu-id="69350-111">Chargeability setup</span></span>
- <span data-ttu-id="69350-112">Оценка с использованием сведений строки предложения с расценками</span><span class="sxs-lookup"><span data-stu-id="69350-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="69350-113">Клиенты строки предложения с расценками</span><span class="sxs-lookup"><span data-stu-id="69350-113">Quote line Customers</span></span>

<span data-ttu-id="69350-114">В следующей таблице представлена информация о полях на вкладке **Общее** строки предложения с расценками по проекту.</span><span class="sxs-lookup"><span data-stu-id="69350-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="69350-115">Эти поля помогают настроить основу для подробной, основательной оценки проектной работы.</span><span class="sxs-lookup"><span data-stu-id="69350-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="69350-116">**Поле**</span><span class="sxs-lookup"><span data-stu-id="69350-116">**Field**</span></span> | <span data-ttu-id="69350-117">**Описание**</span><span class="sxs-lookup"><span data-stu-id="69350-117">**Description**</span></span> | <span data-ttu-id="69350-118">**Воздействие на последующие элементы**</span><span class="sxs-lookup"><span data-stu-id="69350-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="69350-119">Название</span><span class="sxs-lookup"><span data-stu-id="69350-119">Name</span></span> | <span data-ttu-id="69350-120">Название строки предложения с расценками, которое должна помочь вам идентифицировать дискретный компонент оцениваемого предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="69350-120">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="69350-121">Копируется в строку контракта по проекту, которая создается из этой строки предложения с расценками, когда предложение с расценками выиграно.</span><span class="sxs-lookup"><span data-stu-id="69350-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="69350-122">Метод выставления счета</span><span class="sxs-lookup"><span data-stu-id="69350-122">Billing Method</span></span> | <span data-ttu-id="69350-123">В предложении с расценками, созданном на основе возможной сделки, это значение копируется из соответствующего поля в строке возможной сделки.</span><span class="sxs-lookup"><span data-stu-id="69350-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="69350-124">Это поле включает две основные модели заключения контрактов, поддерживаемые Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="69350-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="69350-125">- Фиксированная цена</span><span class="sxs-lookup"><span data-stu-id="69350-125">- Fixed price</span></span></br><span data-ttu-id="69350-126">- Время и материал.</span><span class="sxs-lookup"><span data-stu-id="69350-126">- Time and material.</span></span>| <span data-ttu-id="69350-127">Значение этого поля копируется в строку контракта по проекту, которая создается из этой строки предложения с расценками, когда предложение с расценками выиграно.</span><span class="sxs-lookup"><span data-stu-id="69350-127">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="69350-128">Project</span><span class="sxs-lookup"><span data-stu-id="69350-128">Project</span></span> | <span data-ttu-id="69350-129">Используйте это необязательное поле, чтобы определить проект, который будет использоваться для выполнения работы по данному заданию.</span><span class="sxs-lookup"><span data-stu-id="69350-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="69350-130">Когда проект сопоставляется со строкой предложения с расценками, это помогает с настройкой оплачиваемых задач, а также с внесением оценки на основе проекта в строку предложения с расценками в качестве сведений строки предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="69350-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="69350-131">Если проект не сопоставлен со строкой предложения с расценками по проекту, оценку следует создать вручную, создав сведения каждой строки предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="69350-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="69350-132">Значение этого поля копируется в строку контракта по проекту, которая создается из этой строки предложения с расценками, когда предложение с расценками выиграно.</span><span class="sxs-lookup"><span data-stu-id="69350-132">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="69350-133">Включить время</span><span class="sxs-lookup"><span data-stu-id="69350-133">Include Time</span></span> | <span data-ttu-id="69350-134">Флаг **Да**/**Нет** указывает, будут ли включены транзакции времени или трудозатраты по выбранному проекту в оценку в этой строке предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="69350-134">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="69350-135">Значение **Нет** указывает, что транзакции времени или трудозатраты не будут включены в оценку в этой строке предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="69350-135">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="69350-136">Значение **Да** указывает, что транзакции времени или трудозатраты будут включены в оценку в этой строке предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="69350-136">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="69350-137">Значение этого поля копируется в строку контракта по проекту, которая создается из этой строки предложения с расценками, когда предложение с расценками выиграно.</span><span class="sxs-lookup"><span data-stu-id="69350-137">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="69350-138">Включить расход</span><span class="sxs-lookup"><span data-stu-id="69350-138">Include Expense</span></span> | <span data-ttu-id="69350-139">Флаг **Да**/**Нет** указывает, будут ли включены расходы по выбранному проекту в оценку в этой строке предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="69350-139">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="69350-140">Значение **Нет** указывает, что затраты не будут включены в оценку в этой строке предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="69350-140">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="69350-141">Значение **Да** указывает, что затраты будут включены в оценку в этой строке предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="69350-141">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="69350-142">Значение этого поля копируется далее в строку контракта по проекту, которая создается из этой строки предложения с расценками, когда предложение с расценками выиграно.</span><span class="sxs-lookup"><span data-stu-id="69350-142">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="69350-143">Включить сбор</span><span class="sxs-lookup"><span data-stu-id="69350-143">Include Fee</span></span> | <span data-ttu-id="69350-144">Флаг **Да**/**Нет** указывает, будут ли включены сборы по выбранному проекту в оценку в этой строке предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="69350-144">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="69350-145">Значение **Нет** указывает, что сборы не будут включены в оценку в этой строке предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="69350-145">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="69350-146">Значение **Да** указывает, что сборы будут включены в оценку в этой строке предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="69350-146">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="69350-147">Значение этого поля копируется в строку контракта по проекту, которая создается из этой строки предложения с расценками, когда предложение с расценками выиграно.</span><span class="sxs-lookup"><span data-stu-id="69350-147">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="69350-148">Сумма по предложению</span><span class="sxs-lookup"><span data-stu-id="69350-148">Quoted Amount</span></span> | <span data-ttu-id="69350-149">Это сумма, которая будет указана заказчику за все работы, прогнозируемые в этой строке предложения с расценками на основе проекта.</span><span class="sxs-lookup"><span data-stu-id="69350-149">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="69350-150">В предложении с расценками, созданном на основе возможной сделки, это значение копируется из поля **Бюджет клиента** в строке возможной сделки.</span><span class="sxs-lookup"><span data-stu-id="69350-150">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="69350-151">Если в строке предложения с расценками по проекту есть сведения о строке, это поле заблокировано для редактирования и суммируется из суммы в сведениях строки предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="69350-151">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="69350-152">Значение этого поля копируется в строку контракта по проекту, которая создается из этой строки предложения с расценками, когда предложение с расценками выиграно.</span><span class="sxs-lookup"><span data-stu-id="69350-152">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="69350-153">Ожидаемый налог</span><span class="sxs-lookup"><span data-stu-id="69350-153">Estimated Tax</span></span> | <span data-ttu-id="69350-154">Это редактируемое поле, в котором пользователь может добавить расчетную сумму налога в строку предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="69350-154">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="69350-155">Если в строке предложения с расценками по проекту есть сведения о строке, это поле заблокировано для редактирования и суммируется из суммы налога в сведениях строки предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="69350-155">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="69350-156">Значение этого поля копируется в строку контракта по проекту, которая создается из этой строки предложения с расценками, когда предложение с расценками выиграно.</span><span class="sxs-lookup"><span data-stu-id="69350-156">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="69350-157">Сумма по предложению с расценками после налогообложения</span><span class="sxs-lookup"><span data-stu-id="69350-157">Quoted Amount after Tax</span></span> | <span data-ttu-id="69350-158">Это поле является суммой строки предложения с расценками после уплаты налогов и предназначено только для чтения.</span><span class="sxs-lookup"><span data-stu-id="69350-158">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="69350-159">Сумма в этом поле рассчитывается как *Сумма по предложению с расценками + Налог*.</span><span class="sxs-lookup"><span data-stu-id="69350-159">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="69350-160">Значение этого поля копируется в строку контракта по проекту, которая создается из этой строки предложения с расценками, когда предложение с расценками выиграно.</span><span class="sxs-lookup"><span data-stu-id="69350-160">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="69350-161">Максимальный лимит</span><span class="sxs-lookup"><span data-stu-id="69350-161">Not-to-exceed Limit</span></span> | <span data-ttu-id="69350-162">Это поле доступно для редактирования и доступно только в строках предложения с расценками на основе проекта, в которых есть способ выставления счетов **Время и материал**.</span><span class="sxs-lookup"><span data-stu-id="69350-162">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="69350-163">Значение этого поля копируется в строку контракта по проекту, которая создается из этой строки предложения с расценками, когда предложение с расценками выиграно.</span><span class="sxs-lookup"><span data-stu-id="69350-163">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="69350-164">Бюджет клиента</span><span class="sxs-lookup"><span data-stu-id="69350-164">Customer Budget</span></span> | <span data-ttu-id="69350-165">Это поле доступно для редактирования и копируется из соответствующего поля в строке возможной сделки, если предложение с расценками было создано из возможной сделки.</span><span class="sxs-lookup"><span data-stu-id="69350-165">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="69350-166">Значение этого поля копируется в строку контракта по проекту, которая создается из этой строки предложения с расценками, когда предложение с расценками выиграно.</span><span class="sxs-lookup"><span data-stu-id="69350-166">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="69350-167">Правила проверки для полей на вкладке "Общие" строк предложения с расценками на основе проекта</span><span class="sxs-lookup"><span data-stu-id="69350-167">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="69350-168">**Правило 1**: определенный класс транзакций в выбранном проекте может быть включен только в одну строку предложения с расценками на основе проекта.</span><span class="sxs-lookup"><span data-stu-id="69350-168">**Rule 1**: A certain transaction class on the selected project can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="69350-169">**Правило 2**: если у возможной сделки есть несколько предложений с расценками, могут быть строки предложения с расценками из разных предложений с расценками, которые все ссылаются на один и тот же проект и включают один и тот же класс транзакций.</span><span class="sxs-lookup"><span data-stu-id="69350-169">**Rule 2**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="69350-170">**Правило 3**: если предложения с расценками не относятся к одной и той же возможной сделке, они не могут включать один и тот же проект и класс транзакций.</span><span class="sxs-lookup"><span data-stu-id="69350-170">**Rule 3**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="69350-171">
                    <strong>Возможная сделка</strong>
                </span><span class="sxs-lookup"><span data-stu-id="69350-171">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="69350-172">
                    <strong>Предложение с расценками</strong>
                </span><span class="sxs-lookup"><span data-stu-id="69350-172">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="69350-173">
                    <strong>Строка предложения с расценками</strong>
                </span><span class="sxs-lookup"><span data-stu-id="69350-173">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="69350-174">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="69350-174">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="69350-175">
                    <strong>Включить время</strong>
                </span><span class="sxs-lookup"><span data-stu-id="69350-175">
                    <strong>Include time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="69350-176">
                    <strong>Включить расход</strong>
                </span><span class="sxs-lookup"><span data-stu-id="69350-176">
                    <strong>Include expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="69350-177">
                    <strong>Включить</strong>
                </span><span class="sxs-lookup"><span data-stu-id="69350-177">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="69350-178">
                    <strong>сбор</strong>
                </span><span class="sxs-lookup"><span data-stu-id="69350-178">
                    <strong>fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="69350-179">
                    <strong>Действителен/Недействителен</strong>
                </span><span class="sxs-lookup"><span data-stu-id="69350-179">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="69350-180">
                    <strong>Причина</strong>
                </span><span class="sxs-lookup"><span data-stu-id="69350-180">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="69350-181">O1</span><span class="sxs-lookup"><span data-stu-id="69350-181">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="69350-182">К1</span><span class="sxs-lookup"><span data-stu-id="69350-182">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="69350-183">QL1</span><span class="sxs-lookup"><span data-stu-id="69350-183">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="69350-184">П1</span><span class="sxs-lookup"><span data-stu-id="69350-184">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="69350-185">Да</span><span class="sxs-lookup"><span data-stu-id="69350-185">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="69350-186">Да</span><span class="sxs-lookup"><span data-stu-id="69350-186">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="69350-187">Да</span><span class="sxs-lookup"><span data-stu-id="69350-187">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="69350-188">Недействительный</span><span class="sxs-lookup"><span data-stu-id="69350-188">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="69350-189">Нарушение правила №1.</span><span class="sxs-lookup"><span data-stu-id="69350-189">Violation of Rule #1.</span></span> <span data-ttu-id="69350-190">Время, расходы и сборы по проекту P1 включены в обе строки предложения с расценками, QL1 и QL2.</span><span class="sxs-lookup"><span data-stu-id="69350-190">Time, Expense, and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="69350-191">O1</span><span class="sxs-lookup"><span data-stu-id="69350-191">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="69350-192">К1</span><span class="sxs-lookup"><span data-stu-id="69350-192">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="69350-193">QL2</span><span class="sxs-lookup"><span data-stu-id="69350-193">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="69350-194">П1</span><span class="sxs-lookup"><span data-stu-id="69350-194">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="69350-195">Да</span><span class="sxs-lookup"><span data-stu-id="69350-195">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="69350-196">Да</span><span class="sxs-lookup"><span data-stu-id="69350-196">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="69350-197">Да</span><span class="sxs-lookup"><span data-stu-id="69350-197">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="69350-198">O1</span><span class="sxs-lookup"><span data-stu-id="69350-198">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="69350-199">К1</span><span class="sxs-lookup"><span data-stu-id="69350-199">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="69350-200">QL1</span><span class="sxs-lookup"><span data-stu-id="69350-200">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="69350-201">П1</span><span class="sxs-lookup"><span data-stu-id="69350-201">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="69350-202">Да</span><span class="sxs-lookup"><span data-stu-id="69350-202">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="69350-203">No</span><span class="sxs-lookup"><span data-stu-id="69350-203">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="69350-204">Да</span><span class="sxs-lookup"><span data-stu-id="69350-204">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="69350-205">Недействительный</span><span class="sxs-lookup"><span data-stu-id="69350-205">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="69350-206">Нарушение правила №1.</span><span class="sxs-lookup"><span data-stu-id="69350-206">Violation of Rule #1.</span></span> <span data-ttu-id="69350-207">Время и сборы по проекту P1 включены в обе строки предложения с расценками, QL1 и QL2.</span><span class="sxs-lookup"><span data-stu-id="69350-207">Time and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="69350-208">O1</span><span class="sxs-lookup"><span data-stu-id="69350-208">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="69350-209">К1</span><span class="sxs-lookup"><span data-stu-id="69350-209">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="69350-210">QL2</span><span class="sxs-lookup"><span data-stu-id="69350-210">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="69350-211">П1</span><span class="sxs-lookup"><span data-stu-id="69350-211">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="69350-212">Да</span><span class="sxs-lookup"><span data-stu-id="69350-212">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="69350-213">Да</span><span class="sxs-lookup"><span data-stu-id="69350-213">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="69350-214">Да</span><span class="sxs-lookup"><span data-stu-id="69350-214">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="69350-215">O1</span><span class="sxs-lookup"><span data-stu-id="69350-215">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="69350-216">К1</span><span class="sxs-lookup"><span data-stu-id="69350-216">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="69350-217">QL1</span><span class="sxs-lookup"><span data-stu-id="69350-217">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="69350-218">П1</span><span class="sxs-lookup"><span data-stu-id="69350-218">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="69350-219">Да</span><span class="sxs-lookup"><span data-stu-id="69350-219">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="69350-220">No</span><span class="sxs-lookup"><span data-stu-id="69350-220">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="69350-221">Да</span><span class="sxs-lookup"><span data-stu-id="69350-221">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="69350-222">Действителен</span><span class="sxs-lookup"><span data-stu-id="69350-222">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
<span data-ttu-id="69350-223">Время и сборы по проекту P1 включены в QL1.</span><span class="sxs-lookup"><span data-stu-id="69350-223">Time and fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="69350-224">Расходы по проекту P1 включены в QL2.</span><span class="sxs-lookup"><span data-stu-id="69350-224">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="69350-225">То, что включается в каждую строку предложения с расценками, не перекрывается, поэтому это допустимо.</span><span class="sxs-lookup"><span data-stu-id="69350-225">There is no overlap in what is being included on each quote line so it is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="69350-226">O1</span><span class="sxs-lookup"><span data-stu-id="69350-226">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="69350-227">К1</span><span class="sxs-lookup"><span data-stu-id="69350-227">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="69350-228">QL2</span><span class="sxs-lookup"><span data-stu-id="69350-228">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="69350-229">П1</span><span class="sxs-lookup"><span data-stu-id="69350-229">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="69350-230">No</span><span class="sxs-lookup"><span data-stu-id="69350-230">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="69350-231">Да</span><span class="sxs-lookup"><span data-stu-id="69350-231">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="69350-232">No</span><span class="sxs-lookup"><span data-stu-id="69350-232">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="69350-233">O1</span><span class="sxs-lookup"><span data-stu-id="69350-233">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="69350-234">К1</span><span class="sxs-lookup"><span data-stu-id="69350-234">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="69350-235">QL1</span><span class="sxs-lookup"><span data-stu-id="69350-235">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="69350-236">П1</span><span class="sxs-lookup"><span data-stu-id="69350-236">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="69350-237">Да</span><span class="sxs-lookup"><span data-stu-id="69350-237">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="69350-238">Да</span><span class="sxs-lookup"><span data-stu-id="69350-238">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="69350-239">Да</span><span class="sxs-lookup"><span data-stu-id="69350-239">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="69350-240">Недействительный</span><span class="sxs-lookup"><span data-stu-id="69350-240">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="69350-241">Нарушение правила №1 выше</span><span class="sxs-lookup"><span data-stu-id="69350-241">Violation of Rule #1 above</span></span> </p>
                <p>
<span data-ttu-id="69350-242">Q1 включает время, расходы и сборы для всего проекта P1.</span><span class="sxs-lookup"><span data-stu-id="69350-242">Q1 includes Time, Expenses, and Fees for the whole project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="69350-243">QL2 включает время, расходы и сборы для всего проекта P1 и частично перекрывается с тем, что включено в Q1.</span><span class="sxs-lookup"><span data-stu-id="69350-243">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="69350-244">O1</span><span class="sxs-lookup"><span data-stu-id="69350-244">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="69350-245">К1</span><span class="sxs-lookup"><span data-stu-id="69350-245">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="69350-246">QL2</span><span class="sxs-lookup"><span data-stu-id="69350-246">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="69350-247">П1</span><span class="sxs-lookup"><span data-stu-id="69350-247">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="69350-248">Да</span><span class="sxs-lookup"><span data-stu-id="69350-248">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="69350-249">Да</span><span class="sxs-lookup"><span data-stu-id="69350-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="69350-250">Да</span><span class="sxs-lookup"><span data-stu-id="69350-250">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="69350-251">O1</span><span class="sxs-lookup"><span data-stu-id="69350-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="69350-252">К1</span><span class="sxs-lookup"><span data-stu-id="69350-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="69350-253">QL1</span><span class="sxs-lookup"><span data-stu-id="69350-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="69350-254">П1</span><span class="sxs-lookup"><span data-stu-id="69350-254">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="69350-255">Да</span><span class="sxs-lookup"><span data-stu-id="69350-255">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="69350-256">Да</span><span class="sxs-lookup"><span data-stu-id="69350-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="69350-257">Да</span><span class="sxs-lookup"><span data-stu-id="69350-257">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="69350-258">Действителен</span><span class="sxs-lookup"><span data-stu-id="69350-258">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="69350-259">В соответствии с правилом № 2, Q1 и Q2 — это два предложения с расценками по одной и той же возможной сделке, поэтому они оба могут оценивать одни и те же компоненты проекта.</span><span class="sxs-lookup"><span data-stu-id="69350-259">Based on Rule #2, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="69350-260">O1</span><span class="sxs-lookup"><span data-stu-id="69350-260">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="69350-261">К2</span><span class="sxs-lookup"><span data-stu-id="69350-261">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="69350-262">QL1 в Q2</span><span class="sxs-lookup"><span data-stu-id="69350-262">QL1 on Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="69350-263">П1</span><span class="sxs-lookup"><span data-stu-id="69350-263">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="69350-264">Да</span><span class="sxs-lookup"><span data-stu-id="69350-264">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="69350-265">Да</span><span class="sxs-lookup"><span data-stu-id="69350-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="69350-266">Да</span><span class="sxs-lookup"><span data-stu-id="69350-266">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="69350-267">O1</span><span class="sxs-lookup"><span data-stu-id="69350-267">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="69350-268">К1</span><span class="sxs-lookup"><span data-stu-id="69350-268">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="69350-269">QL1</span><span class="sxs-lookup"><span data-stu-id="69350-269">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="69350-270">П1</span><span class="sxs-lookup"><span data-stu-id="69350-270">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="69350-271">Да</span><span class="sxs-lookup"><span data-stu-id="69350-271">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="69350-272">Да</span><span class="sxs-lookup"><span data-stu-id="69350-272">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="69350-273">Да</span><span class="sxs-lookup"><span data-stu-id="69350-273">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="69350-274">Действителен</span><span class="sxs-lookup"><span data-stu-id="69350-274">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="69350-275">В соответствии с правилом № 3, Q1 и Q2 — это два предложения с расценками для разных возможных сделок, поэтому они не могут оценивать одни и те же компоненты одного проекта.</span><span class="sxs-lookup"><span data-stu-id="69350-275">Based on Rule #3, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="69350-276">O2</span><span class="sxs-lookup"><span data-stu-id="69350-276">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="69350-277">К1</span><span class="sxs-lookup"><span data-stu-id="69350-277">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="69350-278">QL1</span><span class="sxs-lookup"><span data-stu-id="69350-278">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="69350-279">П1</span><span class="sxs-lookup"><span data-stu-id="69350-279">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="69350-280">Да</span><span class="sxs-lookup"><span data-stu-id="69350-280">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="69350-281">Да</span><span class="sxs-lookup"><span data-stu-id="69350-281">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="69350-282">Да</span><span class="sxs-lookup"><span data-stu-id="69350-282">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="69350-283">Недействительный</span><span class="sxs-lookup"><span data-stu-id="69350-283">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../includes/footer-banner.md)]
