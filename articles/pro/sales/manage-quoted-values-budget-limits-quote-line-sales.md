---
title: Обзор строк предложения с расценками на основе проекта — облегченное развертывание
description: Эта тема предоставляет информацию об использовании строк предложения с расценками на основе проекта для работы по проекту. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: be1663c0d226fa19fe4b9df566e16d215f1fc08e
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181108"
---
# <a name="project-based-quote-lines-overview---lite"></a><span data-ttu-id="bbae9-104">Обзор строк предложения с расценками на основе проекта — облегченное развертывание</span><span class="sxs-lookup"><span data-stu-id="bbae9-104">Project-based quote lines overview - lite</span></span>

<span data-ttu-id="bbae9-105">_**Относится к:** развертывание Lite — от сделки до счетов-проформ_</span><span class="sxs-lookup"><span data-stu-id="bbae9-105">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="bbae9-106">Строки предложений с расценками на основе проекта предназначены для помощи в оценке проектной работы по заданию.</span><span class="sxs-lookup"><span data-stu-id="bbae9-106">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="bbae9-107">Структура строки предложения с расценками по проекту расширена для оценок проекта за счет следующих понятий:</span><span class="sxs-lookup"><span data-stu-id="bbae9-107">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="bbae9-108">Метод выставления счета</span><span class="sxs-lookup"><span data-stu-id="bbae9-108">Billing Method</span></span>
- <span data-ttu-id="bbae9-109">Сопоставление проектов и задач</span><span class="sxs-lookup"><span data-stu-id="bbae9-109">Project and Task Mapping</span></span>
- <span data-ttu-id="bbae9-110">Включенные классы транзакций</span><span class="sxs-lookup"><span data-stu-id="bbae9-110">Included Transaction classes</span></span>
- <span data-ttu-id="bbae9-111">Максимальный лимит</span><span class="sxs-lookup"><span data-stu-id="bbae9-111">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="bbae9-112">Настройка возможности оплаты</span><span class="sxs-lookup"><span data-stu-id="bbae9-112">Chargeability setup</span></span>
- <span data-ttu-id="bbae9-113">Оценка с использованием сведений строки предложения с расценками</span><span class="sxs-lookup"><span data-stu-id="bbae9-113">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="bbae9-114">Клиенты строки предложения с расценками</span><span class="sxs-lookup"><span data-stu-id="bbae9-114">Quote line Customers</span></span>

<span data-ttu-id="bbae9-115">В следующей таблице представлена информация о полях на вкладке **Общее** строки предложения с расценками по проекту.</span><span class="sxs-lookup"><span data-stu-id="bbae9-115">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="bbae9-116">Эти поля помогают настроить основу для подробной, основательной оценки проектной работы.</span><span class="sxs-lookup"><span data-stu-id="bbae9-116">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="bbae9-117">**Поле**</span><span class="sxs-lookup"><span data-stu-id="bbae9-117">**Field**</span></span> | <span data-ttu-id="bbae9-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="bbae9-118">**Description**</span></span> | <span data-ttu-id="bbae9-119">**Воздействие на последующие элементы**</span><span class="sxs-lookup"><span data-stu-id="bbae9-119">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="bbae9-120">Название</span><span class="sxs-lookup"><span data-stu-id="bbae9-120">Name</span></span> | <span data-ttu-id="bbae9-121">Название строки предложения с расценками, которое должна помочь вам идентифицировать дискретный компонент оцениваемого предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="bbae9-121">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="bbae9-122">Копируется в строку контракта по проекту, которая создается из этой строки предложения с расценками, когда предложение с расценками выиграно.</span><span class="sxs-lookup"><span data-stu-id="bbae9-122">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="bbae9-123">Метод выставления счета</span><span class="sxs-lookup"><span data-stu-id="bbae9-123">Billing Method</span></span> | <span data-ttu-id="bbae9-124">В предложении с расценками, созданном на основе возможной сделки, это значение копируется из соответствующего поля в строке возможной сделки.</span><span class="sxs-lookup"><span data-stu-id="bbae9-124">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="bbae9-125">Это поле включает две основные модели контрактов, поддерживаемые Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="bbae9-125">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="bbae9-126">- Фиксированная цена</span><span class="sxs-lookup"><span data-stu-id="bbae9-126">- Fixed price</span></span></br><span data-ttu-id="bbae9-127">- Время и материал.</span><span class="sxs-lookup"><span data-stu-id="bbae9-127">- Time and material.</span></span>| <span data-ttu-id="bbae9-128">Значение этого поля копируется в строку контракта по проекту, которая создается из этой строки предложения с расценками, когда предложение с расценками выиграно.</span><span class="sxs-lookup"><span data-stu-id="bbae9-128">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="bbae9-129">Project</span><span class="sxs-lookup"><span data-stu-id="bbae9-129">Project</span></span> | <span data-ttu-id="bbae9-130">Используйте это необязательное поле, чтобы определить проект, который будет использоваться для выполнения работы по данному заданию.</span><span class="sxs-lookup"><span data-stu-id="bbae9-130">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="bbae9-131">Когда проект сопоставляется со строкой предложения с расценками, это помогает с настройкой оплачиваемых задач, а также с внесением оценки на основе проекта в строку предложения с расценками в качестве сведений строки предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="bbae9-131">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="bbae9-132">Если проект не сопоставлен со строкой предложения с расценками по проекту, оценку следует создать вручную, создав сведения каждой строки предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="bbae9-132">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="bbae9-133">Значение этого поля копируется в строку контракта по проекту, которая создается из этой строки предложения с расценками, когда предложение с расценками выиграно.</span><span class="sxs-lookup"><span data-stu-id="bbae9-133">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="bbae9-134">Включенные задачи</span><span class="sxs-lookup"><span data-stu-id="bbae9-134">Included Tasks</span></span> | <span data-ttu-id="bbae9-135">Указывает, используется ли эта строка предложения с расценками для всех или некоторых задач проекта для выбранного проекта.</span><span class="sxs-lookup"><span data-stu-id="bbae9-135">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="bbae9-136">Это поле имеет следующие возможные значения:</span><span class="sxs-lookup"><span data-stu-id="bbae9-136">This field has the following possible values:</span></span></br><span data-ttu-id="bbae9-137">- Все задачи проекта</span><span class="sxs-lookup"><span data-stu-id="bbae9-137">- All project tasks</span></span></br><span data-ttu-id="bbae9-138">- Только выбранные задачи проекта</span><span class="sxs-lookup"><span data-stu-id="bbae9-138">- Selected project tasks only</span></span></br><span data-ttu-id="bbae9-139">Пустое значение в этом поле эквивалентно варианту **Все задачи проекта**.</span><span class="sxs-lookup"><span data-stu-id="bbae9-139">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="bbae9-140">Когда выбран вариант **Только выбранные задачи проекта**, то на странице проекта на вкладке **Настройка выставления счетов по задачам** можно выбрать определенные задачи, чтобы связать их с этой строкой предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="bbae9-140">When **Selected project tasks only** is selected then on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="bbae9-141">Значение этого поля копируется в строку контракта по проекту, которая создается из этой строки предложения с расценками, когда предложение с расценками выиграно.</span><span class="sxs-lookup"><span data-stu-id="bbae9-141">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="bbae9-142">Включить время</span><span class="sxs-lookup"><span data-stu-id="bbae9-142">Include Time</span></span> | <span data-ttu-id="bbae9-143">Флаг **Да**/**Нет** указывает, будут ли включены транзакции времени или трудозатраты по выбранному проекту в оценку в этой строке предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="bbae9-143">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="bbae9-144">Значение **Нет** указывает, что транзакции времени или трудозатраты не будут включены в оценку в этой строке предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="bbae9-144">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="bbae9-145">Значение **Да** указывает, что транзакции времени или трудозатраты будут включены в оценку в этой строке предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="bbae9-145">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="bbae9-146">Значение этого поля копируется в строку контракта по проекту, которая создается из этой строки предложения с расценками, когда предложение с расценками выиграно.</span><span class="sxs-lookup"><span data-stu-id="bbae9-146">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="bbae9-147">Включить расход</span><span class="sxs-lookup"><span data-stu-id="bbae9-147">Include Expense</span></span> | <span data-ttu-id="bbae9-148">Флаг **Да**/**Нет** указывает, будут ли включены расходы по выбранному проекту в оценку в этой строке предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="bbae9-148">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="bbae9-149">Значение **Нет** указывает, что затраты не будут включены в оценку в этой строке предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="bbae9-149">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="bbae9-150">Значение **Да** указывает, что затраты будут включены в оценку в этой строке предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="bbae9-150">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="bbae9-151">Значение этого поля копируется далее в строку контракта по проекту, которая создается из этой строки предложения с расценками, когда предложение с расценками выиграно.</span><span class="sxs-lookup"><span data-stu-id="bbae9-151">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="bbae9-152">Включить сбор</span><span class="sxs-lookup"><span data-stu-id="bbae9-152">Include Fee</span></span> | <span data-ttu-id="bbae9-153">Флаг **Да**/**Нет** указывает, будут ли включены сборы по выбранному проекту в оценку в этой строке предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="bbae9-153">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="bbae9-154">Значение **Нет** указывает, что сборы не будут включены в оценку в этой строке предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="bbae9-154">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="bbae9-155">Значение **Да** указывает, что сборы будут включены в оценку в этой строке предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="bbae9-155">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="bbae9-156">Значение этого поля копируется в строку контракта по проекту, которая создается из этой строки предложения с расценками, когда предложение с расценками выиграно.</span><span class="sxs-lookup"><span data-stu-id="bbae9-156">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="bbae9-157">Сумма по предложению</span><span class="sxs-lookup"><span data-stu-id="bbae9-157">Quoted Amount</span></span> | <span data-ttu-id="bbae9-158">Это сумма, которая будет указана заказчику за все работы, прогнозируемые в этой строке предложения с расценками на основе проекта.</span><span class="sxs-lookup"><span data-stu-id="bbae9-158">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="bbae9-159">В предложении с расценками, созданном на основе возможной сделки, это значение копируется из поля **Бюджет клиента** в строке возможной сделки.</span><span class="sxs-lookup"><span data-stu-id="bbae9-159">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="bbae9-160">Если в строке предложения с расценками по проекту есть сведения о строке, это поле заблокировано для редактирования и суммируется из суммы в сведениях строки предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="bbae9-160">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="bbae9-161">Значение этого поля копируется в строку контракта по проекту, которая создается из этой строки предложения с расценками, когда предложение с расценками выиграно.</span><span class="sxs-lookup"><span data-stu-id="bbae9-161">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="bbae9-162">Ожидаемый налог</span><span class="sxs-lookup"><span data-stu-id="bbae9-162">Estimated Tax</span></span> | <span data-ttu-id="bbae9-163">Это редактируемое поле, в котором пользователь может добавить расчетную сумму налога в строку предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="bbae9-163">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="bbae9-164">Если в строке предложения с расценками по проекту есть сведения о строке, это поле заблокировано для редактирования и суммируется из суммы налога в сведениях строки предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="bbae9-164">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="bbae9-165">Значение этого поля копируется в строку контракта по проекту, которая создается из этой строки предложения с расценками, когда предложение с расценками выиграно.</span><span class="sxs-lookup"><span data-stu-id="bbae9-165">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="bbae9-166">Сумма по предложению с расценками после налогообложения</span><span class="sxs-lookup"><span data-stu-id="bbae9-166">Quoted Amount after Tax</span></span> | <span data-ttu-id="bbae9-167">Это поле является суммой строки предложения с расценками после уплаты налогов и предназначено только для чтения.</span><span class="sxs-lookup"><span data-stu-id="bbae9-167">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="bbae9-168">Сумма в этом поле рассчитывается как *Сумма по предложению с расценками + Налог*.</span><span class="sxs-lookup"><span data-stu-id="bbae9-168">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="bbae9-169">Значение этого поля копируется в строку контракта по проекту, которая создается из этой строки предложения с расценками, когда предложение с расценками выиграно.</span><span class="sxs-lookup"><span data-stu-id="bbae9-169">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="bbae9-170">Максимальный лимит</span><span class="sxs-lookup"><span data-stu-id="bbae9-170">Not-to-exceed Limit</span></span> | <span data-ttu-id="bbae9-171">Это поле доступно для редактирования и доступно только в строках предложения с расценками на основе проекта, в которых есть способ выставления счетов **Время и материал**.</span><span class="sxs-lookup"><span data-stu-id="bbae9-171">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="bbae9-172">Значение этого поля копируется в строку контракта по проекту, которая создается из этой строки предложения с расценками, когда предложение с расценками выиграно.</span><span class="sxs-lookup"><span data-stu-id="bbae9-172">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="bbae9-173">Бюджет клиента</span><span class="sxs-lookup"><span data-stu-id="bbae9-173">Customer Budget</span></span> | <span data-ttu-id="bbae9-174">Это поле доступно для редактирования и копируется из соответствующего поля в строке возможной сделки, если предложение с расценками было создано из возможной сделки.</span><span class="sxs-lookup"><span data-stu-id="bbae9-174">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="bbae9-175">Значение этого поля копируется в строку контракта по проекту, которая создается из этой строки предложения с расценками, когда предложение с расценками выиграно.</span><span class="sxs-lookup"><span data-stu-id="bbae9-175">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="bbae9-176">Правила проверки для полей на вкладке "Общие" строк предложения с расценками на основе проекта</span><span class="sxs-lookup"><span data-stu-id="bbae9-176">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="bbae9-177">**Правило 1**: если поле **Включенные задачи** пустое, или если для него установлено **Все задачи проекта**, проект включается в строку предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="bbae9-177">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="bbae9-178">**Правило 2**: если поле **Включенные задачи** пустое или если для него установлено значение **Все задачи проекта**, проект и определенный класс транзакций могут быть включены только в одну строку предложения с расценками на основе проекта.</span><span class="sxs-lookup"><span data-stu-id="bbae9-178">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="bbae9-179">**Правило 3**: если поле **Включенные задачи** пустое или если для него установлено значение **Только выбранные задачи проекта**, проект и определенный класс транзакций могут быть включены в несколько строк предложения с расценками на основе проекта.</span><span class="sxs-lookup"><span data-stu-id="bbae9-179">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="bbae9-180">**Правило 4**: если у возможной сделки есть несколько предложений с расценками, могут быть строки предложения с расценками из разных предложений с расценками, которые все ссылаются на один и тот же проект и включают один и тот же класс транзакций.</span><span class="sxs-lookup"><span data-stu-id="bbae9-180">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="bbae9-181">**Правило 5**: если предложения с расценками не относятся к одной и той же возможной сделке, они не могут включать один и тот же проект и класс транзакций.</span><span class="sxs-lookup"><span data-stu-id="bbae9-181">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="bbae9-182">
                    <strong>Возможная сделка</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bbae9-182">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="bbae9-183">
                    <strong>Предложение с расценками</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bbae9-183">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="bbae9-184">
                    <strong>Строка предложения с расценками</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bbae9-184">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="bbae9-185">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bbae9-185">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="90" valign="top">
                <p><span data-ttu-id="bbae9-186">
                    <strong>Включенные задачи</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bbae9-186">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="bbae9-187">
                    <strong>Включить время</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bbae9-187">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="bbae9-188">
                    <strong>Включить расход</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bbae9-188">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="bbae9-189">
                    <strong>Включить</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bbae9-189">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="bbae9-190">
                    <strong>Сбор</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bbae9-190">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="bbae9-191">
                    <strong>Действителен/Недействителен</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bbae9-191">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="bbae9-192">
                    <strong>Причина</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bbae9-192">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="bbae9-193">O1</span><span class="sxs-lookup"><span data-stu-id="bbae9-193">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="bbae9-194">К1</span><span class="sxs-lookup"><span data-stu-id="bbae9-194">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bbae9-195">QL1</span><span class="sxs-lookup"><span data-stu-id="bbae9-195">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bbae9-196">П1</span><span class="sxs-lookup"><span data-stu-id="bbae9-196">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="bbae9-197">ПУСТО</span><span class="sxs-lookup"><span data-stu-id="bbae9-197">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="bbae9-198">Да</span><span class="sxs-lookup"><span data-stu-id="bbae9-198">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="bbae9-199">Да</span><span class="sxs-lookup"><span data-stu-id="bbae9-199">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bbae9-200">Да</span><span class="sxs-lookup"><span data-stu-id="bbae9-200">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="bbae9-201">Недействительный</span><span class="sxs-lookup"><span data-stu-id="bbae9-201">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="bbae9-202">Нарушение правила №2.</span><span class="sxs-lookup"><span data-stu-id="bbae9-202">Violation of Rule #2.</span></span> <span data-ttu-id="bbae9-203">Время, расходы и сборы по проекту P1 включены в строки предложения с расценками, QL1 и QL2.</span><span class="sxs-lookup"><span data-stu-id="bbae9-203">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="bbae9-204">O1</span><span class="sxs-lookup"><span data-stu-id="bbae9-204">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="bbae9-205">К1</span><span class="sxs-lookup"><span data-stu-id="bbae9-205">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bbae9-206">QL2</span><span class="sxs-lookup"><span data-stu-id="bbae9-206">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bbae9-207">П1</span><span class="sxs-lookup"><span data-stu-id="bbae9-207">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="bbae9-208">ПУСТО</span><span class="sxs-lookup"><span data-stu-id="bbae9-208">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="bbae9-209">Да</span><span class="sxs-lookup"><span data-stu-id="bbae9-209">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="bbae9-210">Да</span><span class="sxs-lookup"><span data-stu-id="bbae9-210">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bbae9-211">Да</span><span class="sxs-lookup"><span data-stu-id="bbae9-211">Yes</span></span> </p>
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
            <td width="90" valign="top">
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
<span data-ttu-id="bbae9-212">O1</span><span class="sxs-lookup"><span data-stu-id="bbae9-212">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="bbae9-213">К1</span><span class="sxs-lookup"><span data-stu-id="bbae9-213">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bbae9-214">QL1</span><span class="sxs-lookup"><span data-stu-id="bbae9-214">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bbae9-215">П1</span><span class="sxs-lookup"><span data-stu-id="bbae9-215">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="bbae9-216">ПУСТО</span><span class="sxs-lookup"><span data-stu-id="bbae9-216">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="bbae9-217">Да</span><span class="sxs-lookup"><span data-stu-id="bbae9-217">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="bbae9-218">No</span><span class="sxs-lookup"><span data-stu-id="bbae9-218">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bbae9-219">Да</span><span class="sxs-lookup"><span data-stu-id="bbae9-219">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="bbae9-220">Недействительный</span><span class="sxs-lookup"><span data-stu-id="bbae9-220">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="bbae9-221">Нарушение правила №2.</span><span class="sxs-lookup"><span data-stu-id="bbae9-221">Violation of Rule #2.</span></span> <span data-ttu-id="bbae9-222">Время и сборы по проекту P1 включены в строки предложения с расценками QL1 и QL2.</span><span class="sxs-lookup"><span data-stu-id="bbae9-222">Time and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="bbae9-223">O1</span><span class="sxs-lookup"><span data-stu-id="bbae9-223">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="bbae9-224">К1</span><span class="sxs-lookup"><span data-stu-id="bbae9-224">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bbae9-225">QL2</span><span class="sxs-lookup"><span data-stu-id="bbae9-225">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bbae9-226">П1</span><span class="sxs-lookup"><span data-stu-id="bbae9-226">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="bbae9-227">ПУСТО</span><span class="sxs-lookup"><span data-stu-id="bbae9-227">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="bbae9-228">Да</span><span class="sxs-lookup"><span data-stu-id="bbae9-228">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="bbae9-229">Да</span><span class="sxs-lookup"><span data-stu-id="bbae9-229">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bbae9-230">Да</span><span class="sxs-lookup"><span data-stu-id="bbae9-230">Yes</span></span> </p>
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
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="bbae9-231">O1</span><span class="sxs-lookup"><span data-stu-id="bbae9-231">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="bbae9-232">К1</span><span class="sxs-lookup"><span data-stu-id="bbae9-232">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bbae9-233">QL1</span><span class="sxs-lookup"><span data-stu-id="bbae9-233">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bbae9-234">П1</span><span class="sxs-lookup"><span data-stu-id="bbae9-234">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="bbae9-235">ПУСТО</span><span class="sxs-lookup"><span data-stu-id="bbae9-235">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="bbae9-236">Да</span><span class="sxs-lookup"><span data-stu-id="bbae9-236">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="bbae9-237">No</span><span class="sxs-lookup"><span data-stu-id="bbae9-237">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bbae9-238">Да</span><span class="sxs-lookup"><span data-stu-id="bbae9-238">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="bbae9-239">Действителен</span><span class="sxs-lookup"><span data-stu-id="bbae9-239">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
<span data-ttu-id="bbae9-240">Время и сборы по проекту P1 включены в QL1.</span><span class="sxs-lookup"><span data-stu-id="bbae9-240">Time and Fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="bbae9-241">Расходы по проекту P1 включены в QL2.</span><span class="sxs-lookup"><span data-stu-id="bbae9-241">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="bbae9-242">То, что включается в каждую строку предложения с расценками, не перекрывается и допустимо.</span><span class="sxs-lookup"><span data-stu-id="bbae9-242">There is no overlap in what is being included on each quote line and is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="bbae9-243">O1</span><span class="sxs-lookup"><span data-stu-id="bbae9-243">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="bbae9-244">К1</span><span class="sxs-lookup"><span data-stu-id="bbae9-244">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bbae9-245">QL2</span><span class="sxs-lookup"><span data-stu-id="bbae9-245">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bbae9-246">П1</span><span class="sxs-lookup"><span data-stu-id="bbae9-246">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="bbae9-247">ПУСТО</span><span class="sxs-lookup"><span data-stu-id="bbae9-247">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="bbae9-248">No</span><span class="sxs-lookup"><span data-stu-id="bbae9-248">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="bbae9-249">Да</span><span class="sxs-lookup"><span data-stu-id="bbae9-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bbae9-250">No</span><span class="sxs-lookup"><span data-stu-id="bbae9-250">No</span></span> </p>
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
            <td width="90" valign="top">
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
<span data-ttu-id="bbae9-251">O1</span><span class="sxs-lookup"><span data-stu-id="bbae9-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="bbae9-252">К1</span><span class="sxs-lookup"><span data-stu-id="bbae9-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bbae9-253">QL1</span><span class="sxs-lookup"><span data-stu-id="bbae9-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bbae9-254">П1</span><span class="sxs-lookup"><span data-stu-id="bbae9-254">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="bbae9-255">Только выбранные задачи</span><span class="sxs-lookup"><span data-stu-id="bbae9-255">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="bbae9-256">Да</span><span class="sxs-lookup"><span data-stu-id="bbae9-256">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="bbae9-257">Да</span><span class="sxs-lookup"><span data-stu-id="bbae9-257">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bbae9-258">Да</span><span class="sxs-lookup"><span data-stu-id="bbae9-258">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="bbae9-259">Недействительный</span><span class="sxs-lookup"><span data-stu-id="bbae9-259">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="bbae9-260">Нарушение правила №2 выше</span><span class="sxs-lookup"><span data-stu-id="bbae9-260">Violation of Rule #2 above</span></span> </p>
                <p>
<span data-ttu-id="bbae9-261">Q1 включает время, расходы и сборы на подмножество задач по проекту P1.</span><span class="sxs-lookup"><span data-stu-id="bbae9-261">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="bbae9-262">QL2 включает время, расходы и сборы для всего проекта P1 и частично перекрывается с тем, что включено в Q1.</span><span class="sxs-lookup"><span data-stu-id="bbae9-262">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="bbae9-263">O1</span><span class="sxs-lookup"><span data-stu-id="bbae9-263">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="bbae9-264">К1</span><span class="sxs-lookup"><span data-stu-id="bbae9-264">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bbae9-265">QL2</span><span class="sxs-lookup"><span data-stu-id="bbae9-265">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bbae9-266">П1</span><span class="sxs-lookup"><span data-stu-id="bbae9-266">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="bbae9-267">ПУСТО</span><span class="sxs-lookup"><span data-stu-id="bbae9-267">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="bbae9-268">Да</span><span class="sxs-lookup"><span data-stu-id="bbae9-268">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="bbae9-269">Да</span><span class="sxs-lookup"><span data-stu-id="bbae9-269">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bbae9-270">Да</span><span class="sxs-lookup"><span data-stu-id="bbae9-270">Yes</span></span> </p>
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
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="bbae9-271">O1</span><span class="sxs-lookup"><span data-stu-id="bbae9-271">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="bbae9-272">К1</span><span class="sxs-lookup"><span data-stu-id="bbae9-272">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bbae9-273">QL1</span><span class="sxs-lookup"><span data-stu-id="bbae9-273">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bbae9-274">П1</span><span class="sxs-lookup"><span data-stu-id="bbae9-274">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="bbae9-275">Только выбранные задачи</span><span class="sxs-lookup"><span data-stu-id="bbae9-275">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="bbae9-276">Да</span><span class="sxs-lookup"><span data-stu-id="bbae9-276">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="bbae9-277">Да</span><span class="sxs-lookup"><span data-stu-id="bbae9-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bbae9-278">Да</span><span class="sxs-lookup"><span data-stu-id="bbae9-278">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="bbae9-279">Действителен</span><span class="sxs-lookup"><span data-stu-id="bbae9-279">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="bbae9-280">Согласно правилу № 3 выше,</span><span class="sxs-lookup"><span data-stu-id="bbae9-280">Per Rule #3 above,</span></span> </p>
                <p>
<span data-ttu-id="bbae9-281">Q1 включает время, расходы и сборы на подмножество задач по проекту P1.</span><span class="sxs-lookup"><span data-stu-id="bbae9-281">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="bbae9-282">QL2 включает время, расходы и сборы для подмножества задач по проекту P1.</span><span class="sxs-lookup"><span data-stu-id="bbae9-282">QL2 includes Time, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="bbae9-283">Единственная дополнительная проверка касается подмножества задач в QL1, которые отличаются от подмножества задач в QL2.</span><span class="sxs-lookup"><span data-stu-id="bbae9-283">The only additional validation is around the subset of tasks on QL1 which are different from the subset of tasks on QL2.</span></span> <span data-ttu-id="bbae9-284">Это гарантирует отсутствие перекрытий.</span><span class="sxs-lookup"><span data-stu-id="bbae9-284">This ensures that there are no overlaps.</span></span> <span data-ttu-id="bbae9-285">Это выполняется системой, когда задачи связаны.</span><span class="sxs-lookup"><span data-stu-id="bbae9-285">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="bbae9-286">O1</span><span class="sxs-lookup"><span data-stu-id="bbae9-286">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="bbae9-287">К1</span><span class="sxs-lookup"><span data-stu-id="bbae9-287">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bbae9-288">QL2</span><span class="sxs-lookup"><span data-stu-id="bbae9-288">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bbae9-289">П1</span><span class="sxs-lookup"><span data-stu-id="bbae9-289">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="bbae9-290">Только выбранные задачи</span><span class="sxs-lookup"><span data-stu-id="bbae9-290">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="bbae9-291">Да</span><span class="sxs-lookup"><span data-stu-id="bbae9-291">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="bbae9-292">Да</span><span class="sxs-lookup"><span data-stu-id="bbae9-292">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bbae9-293">Да</span><span class="sxs-lookup"><span data-stu-id="bbae9-293">Yes</span></span> </p>
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
            <td width="90" valign="top">
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
<span data-ttu-id="bbae9-294">O1</span><span class="sxs-lookup"><span data-stu-id="bbae9-294">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="bbae9-295">К1</span><span class="sxs-lookup"><span data-stu-id="bbae9-295">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bbae9-296">QL1</span><span class="sxs-lookup"><span data-stu-id="bbae9-296">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bbae9-297">П1</span><span class="sxs-lookup"><span data-stu-id="bbae9-297">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="bbae9-298">Все задачи проекта или пусто</span><span class="sxs-lookup"><span data-stu-id="bbae9-298">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="bbae9-299">Да</span><span class="sxs-lookup"><span data-stu-id="bbae9-299">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="bbae9-300">Да</span><span class="sxs-lookup"><span data-stu-id="bbae9-300">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bbae9-301">Да</span><span class="sxs-lookup"><span data-stu-id="bbae9-301">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="bbae9-302">Действителен</span><span class="sxs-lookup"><span data-stu-id="bbae9-302">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="bbae9-303">В соответствии с правилом № 5, Q1 и Q2 — это два предложения с расценками по одной и той же возможной сделке, поэтому они оба могут оценивать одни и те же компоненты проекта.</span><span class="sxs-lookup"><span data-stu-id="bbae9-303">Based on Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="bbae9-304">O1</span><span class="sxs-lookup"><span data-stu-id="bbae9-304">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="bbae9-305">К2</span><span class="sxs-lookup"><span data-stu-id="bbae9-305">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bbae9-306">QL1</span><span class="sxs-lookup"><span data-stu-id="bbae9-306">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bbae9-307">П1</span><span class="sxs-lookup"><span data-stu-id="bbae9-307">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="bbae9-308">Все задачи проекта или пусто</span><span class="sxs-lookup"><span data-stu-id="bbae9-308">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="bbae9-309">Да</span><span class="sxs-lookup"><span data-stu-id="bbae9-309">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="bbae9-310">Да</span><span class="sxs-lookup"><span data-stu-id="bbae9-310">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bbae9-311">Да</span><span class="sxs-lookup"><span data-stu-id="bbae9-311">Yes</span></span> </p>
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
            <td width="90" valign="top">
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
<span data-ttu-id="bbae9-312">O1</span><span class="sxs-lookup"><span data-stu-id="bbae9-312">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="bbae9-313">К1</span><span class="sxs-lookup"><span data-stu-id="bbae9-313">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bbae9-314">QL1</span><span class="sxs-lookup"><span data-stu-id="bbae9-314">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bbae9-315">П1</span><span class="sxs-lookup"><span data-stu-id="bbae9-315">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="bbae9-316">Все задачи проекта или пусто</span><span class="sxs-lookup"><span data-stu-id="bbae9-316">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="bbae9-317">Да</span><span class="sxs-lookup"><span data-stu-id="bbae9-317">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="bbae9-318">Да</span><span class="sxs-lookup"><span data-stu-id="bbae9-318">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bbae9-319">Да</span><span class="sxs-lookup"><span data-stu-id="bbae9-319">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="bbae9-320">Действителен</span><span class="sxs-lookup"><span data-stu-id="bbae9-320">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="bbae9-321">В соответствии с правилом № 4, Q1 и Q2 — это два предложения с расценками для разных возможных сделок, поэтому они не могут оценивать одни и те же компоненты одного проекта.</span><span class="sxs-lookup"><span data-stu-id="bbae9-321">Based on Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="bbae9-322">O2</span><span class="sxs-lookup"><span data-stu-id="bbae9-322">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="bbae9-323">К1</span><span class="sxs-lookup"><span data-stu-id="bbae9-323">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bbae9-324">QL1</span><span class="sxs-lookup"><span data-stu-id="bbae9-324">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bbae9-325">П1</span><span class="sxs-lookup"><span data-stu-id="bbae9-325">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="bbae9-326">Все задачи проекта или пусто</span><span class="sxs-lookup"><span data-stu-id="bbae9-326">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="bbae9-327">Да</span><span class="sxs-lookup"><span data-stu-id="bbae9-327">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="bbae9-328">Да</span><span class="sxs-lookup"><span data-stu-id="bbae9-328">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="bbae9-329">Да</span><span class="sxs-lookup"><span data-stu-id="bbae9-329">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="bbae9-330">Недействительный</span><span class="sxs-lookup"><span data-stu-id="bbae9-330">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

