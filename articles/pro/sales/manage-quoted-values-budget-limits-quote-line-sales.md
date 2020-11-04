---
title: Строки предложения с расценками на основе проектов (Pro)
description: Эта тема предоставляет информацию об использовании строк предложения с расценками на основе проекта для работы по проекту. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a409d1e378afe97de7fb6c77cf3ad6703661bdff
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083118"
---
# <a name="project-based-quote-lines-pro"></a><span data-ttu-id="ccef3-104">Строки предложения с расценками на основе проектов (Pro)</span><span class="sxs-lookup"><span data-stu-id="ccef3-104">Project-based quote lines (Pro)</span></span>

<span data-ttu-id="ccef3-105">_**Относится к:** развертывание Lite — от сделки до счетов-проформ_</span><span class="sxs-lookup"><span data-stu-id="ccef3-105">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ccef3-106">Строки предложений с расценками на основе проекта предназначены для помощи в оценке проектной работы по заданию.</span><span class="sxs-lookup"><span data-stu-id="ccef3-106">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="ccef3-107">Структура строки предложения с расценками по проекту расширена для оценок проекта за счет следующих понятий:</span><span class="sxs-lookup"><span data-stu-id="ccef3-107">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="ccef3-108">Метод выставления счета</span><span class="sxs-lookup"><span data-stu-id="ccef3-108">Billing Method</span></span>
- <span data-ttu-id="ccef3-109">Сопоставление проектов и задач</span><span class="sxs-lookup"><span data-stu-id="ccef3-109">Project and Task Mapping</span></span>
- <span data-ttu-id="ccef3-110">Включенные классы транзакций</span><span class="sxs-lookup"><span data-stu-id="ccef3-110">Included Transaction classes</span></span>
- <span data-ttu-id="ccef3-111">Максимальный лимит</span><span class="sxs-lookup"><span data-stu-id="ccef3-111">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="ccef3-112">Настройка возможности оплаты</span><span class="sxs-lookup"><span data-stu-id="ccef3-112">Chargeability setup</span></span>
- <span data-ttu-id="ccef3-113">Оценка с использованием сведений строки предложения с расценками</span><span class="sxs-lookup"><span data-stu-id="ccef3-113">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="ccef3-114">Клиенты строки предложения с расценками</span><span class="sxs-lookup"><span data-stu-id="ccef3-114">Quote line Customers</span></span>

<span data-ttu-id="ccef3-115">В следующей таблице представлена информация о полях на вкладке **Общее** строки предложения с расценками по проекту.</span><span class="sxs-lookup"><span data-stu-id="ccef3-115">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="ccef3-116">Эти поля помогают настроить основу для подробной, основательной оценки проектной работы.</span><span class="sxs-lookup"><span data-stu-id="ccef3-116">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="ccef3-117">**Поле**</span><span class="sxs-lookup"><span data-stu-id="ccef3-117">**Field**</span></span> | <span data-ttu-id="ccef3-118">**Релевантность, цель и руководство**</span><span class="sxs-lookup"><span data-stu-id="ccef3-118">**Relevance, purpose, and guidance**</span></span> | <span data-ttu-id="ccef3-119">**Воздействие на последующие элементы**</span><span class="sxs-lookup"><span data-stu-id="ccef3-119">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="ccef3-120">Название</span><span class="sxs-lookup"><span data-stu-id="ccef3-120">Name</span></span> | <span data-ttu-id="ccef3-121">Название строки предложения с расценками, которое должна помочь вам идентифицировать дискретный компонент оцениваемого предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="ccef3-121">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="ccef3-122">Копируется в строку контракта по проекту, которая создается из этой строки предложения с расценками, когда предложение с расценками выиграно.</span><span class="sxs-lookup"><span data-stu-id="ccef3-122">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="ccef3-123">Метод выставления счета</span><span class="sxs-lookup"><span data-stu-id="ccef3-123">Billing Method</span></span> | <span data-ttu-id="ccef3-124">В предложении с расценками, созданном на основе возможной сделки, это значение копируется из соответствующего поля в строке возможной сделки.</span><span class="sxs-lookup"><span data-stu-id="ccef3-124">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="ccef3-125">Это поле включает две основные модели контрактов, поддерживаемые Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="ccef3-125">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="ccef3-126">- Фиксированная цена</span><span class="sxs-lookup"><span data-stu-id="ccef3-126">- Fixed price</span></span></br><span data-ttu-id="ccef3-127">- Время и материал.</span><span class="sxs-lookup"><span data-stu-id="ccef3-127">- Time and material.</span></span>| <span data-ttu-id="ccef3-128">Значение этого поля копируется в строку контракта по проекту, которая создается из этой строки предложения с расценками, когда предложение с расценками выиграно.</span><span class="sxs-lookup"><span data-stu-id="ccef3-128">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="ccef3-129">Project</span><span class="sxs-lookup"><span data-stu-id="ccef3-129">Project</span></span> | <span data-ttu-id="ccef3-130">Используйте это необязательное поле, чтобы определить проект, который будет использоваться для выполнения работы по данному заданию.</span><span class="sxs-lookup"><span data-stu-id="ccef3-130">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="ccef3-131">Когда проект сопоставляется со строкой предложения с расценками, это помогает с настройкой оплачиваемых задач, а также с внесением оценки на основе проекта в строку предложения с расценками в качестве сведений строки предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="ccef3-131">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="ccef3-132">Если проект не сопоставлен со строкой предложения с расценками по проекту, оценку следует создать вручную, создав сведения каждой строки предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="ccef3-132">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="ccef3-133">Значение этого поля копируется в строку контракта по проекту, которая создается из этой строки предложения с расценками, когда предложение с расценками выиграно.</span><span class="sxs-lookup"><span data-stu-id="ccef3-133">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="ccef3-134">Включенные задачи</span><span class="sxs-lookup"><span data-stu-id="ccef3-134">Included Tasks</span></span> | <span data-ttu-id="ccef3-135">Указывает, используется ли эта строка предложения с расценками для всех или некоторых задач проекта для выбранного проекта.</span><span class="sxs-lookup"><span data-stu-id="ccef3-135">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="ccef3-136">Это поле имеет следующие возможные значения:</span><span class="sxs-lookup"><span data-stu-id="ccef3-136">This field has the following possible values:</span></span></br><span data-ttu-id="ccef3-137">- Все задачи проекта</span><span class="sxs-lookup"><span data-stu-id="ccef3-137">- All project tasks</span></span></br><span data-ttu-id="ccef3-138">- Только выбранные задачи проекта</span><span class="sxs-lookup"><span data-stu-id="ccef3-138">- Selected project tasks only</span></span></br><span data-ttu-id="ccef3-139">Пустое значение в этом поле эквивалентно варианту **Все задачи проекта**.</span><span class="sxs-lookup"><span data-stu-id="ccef3-139">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="ccef3-140">Когда выбран вариант **Только выбранные задачи проекта** , то на странице проекта на вкладке **Настройка выставления счетов по задачам** можно выбрать определенные задачи, чтобы связать их с этой строкой предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="ccef3-140">When **Selected project tasks only** is selected then on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="ccef3-141">Значение этого поля копируется в строку контракта по проекту, которая создается из этой строки предложения с расценками, когда предложение с расценками выиграно.</span><span class="sxs-lookup"><span data-stu-id="ccef3-141">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="ccef3-142">Включить время</span><span class="sxs-lookup"><span data-stu-id="ccef3-142">Include Time</span></span> | <span data-ttu-id="ccef3-143">Флаг **Да**/**Нет** указывает, будут ли включены транзакции времени или трудозатраты по выбранному проекту в оценку в этой строке предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="ccef3-143">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="ccef3-144">Значение **Нет** указывает, что транзакции времени или трудозатраты не будут включены в оценку в этой строке предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="ccef3-144">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="ccef3-145">Значение **Да** указывает, что транзакции времени или трудозатраты будут включены в оценку в этой строке предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="ccef3-145">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="ccef3-146">Значение этого поля копируется в строку контракта по проекту, которая создается из этой строки предложения с расценками, когда предложение с расценками выиграно.</span><span class="sxs-lookup"><span data-stu-id="ccef3-146">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="ccef3-147">Включить расход</span><span class="sxs-lookup"><span data-stu-id="ccef3-147">Include Expense</span></span> | <span data-ttu-id="ccef3-148">Флаг **Да**/**Нет** указывает, будут ли включены расходы по выбранному проекту в оценку в этой строке предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="ccef3-148">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="ccef3-149">Значение **Нет** указывает, что затраты не будут включены в оценку в этой строке предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="ccef3-149">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="ccef3-150">Значение **Да** указывает, что затраты будут включены в оценку в этой строке предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="ccef3-150">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="ccef3-151">Значение этого поля копируется далее в строку контракта по проекту, которая создается из этой строки предложения с расценками, когда предложение с расценками выиграно.</span><span class="sxs-lookup"><span data-stu-id="ccef3-151">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="ccef3-152">Включить сбор</span><span class="sxs-lookup"><span data-stu-id="ccef3-152">Include Fee</span></span> | <span data-ttu-id="ccef3-153">Флаг **Да**/**Нет** указывает, будут ли включены сборы по выбранному проекту в оценку в этой строке предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="ccef3-153">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="ccef3-154">Значение **Нет** указывает, что сборы не будут включены в оценку в этой строке предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="ccef3-154">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="ccef3-155">Значение **Да** указывает, что сборы будут включены в оценку в этой строке предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="ccef3-155">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="ccef3-156">Значение этого поля копируется в строку контракта по проекту, которая создается из этой строки предложения с расценками, когда предложение с расценками выиграно.</span><span class="sxs-lookup"><span data-stu-id="ccef3-156">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="ccef3-157">Сумма по предложению</span><span class="sxs-lookup"><span data-stu-id="ccef3-157">Quoted Amount</span></span> | <span data-ttu-id="ccef3-158">Это сумма, которая будет указана заказчику за все работы, прогнозируемые в этой строке предложения с расценками на основе проекта.</span><span class="sxs-lookup"><span data-stu-id="ccef3-158">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="ccef3-159">В предложении с расценками, созданном на основе возможной сделки, это значение копируется из поля **Бюджет клиента** в строке возможной сделки.</span><span class="sxs-lookup"><span data-stu-id="ccef3-159">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="ccef3-160">Если в строке предложения с расценками по проекту есть сведения о строке, это поле заблокировано для редактирования и суммируется из суммы в сведениях строки предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="ccef3-160">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="ccef3-161">Значение этого поля копируется в строку контракта по проекту, которая создается из этой строки предложения с расценками, когда предложение с расценками выиграно.</span><span class="sxs-lookup"><span data-stu-id="ccef3-161">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="ccef3-162">Ожидаемый налог</span><span class="sxs-lookup"><span data-stu-id="ccef3-162">Estimated Tax</span></span> | <span data-ttu-id="ccef3-163">Это редактируемое поле, в котором пользователь может добавить расчетную сумму налога в строку предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="ccef3-163">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="ccef3-164">Если в строке предложения с расценками по проекту есть сведения о строке, это поле заблокировано для редактирования и суммируется из суммы налога в сведениях строки предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="ccef3-164">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="ccef3-165">Значение этого поля копируется в строку контракта по проекту, которая создается из этой строки предложения с расценками, когда предложение с расценками выиграно.</span><span class="sxs-lookup"><span data-stu-id="ccef3-165">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="ccef3-166">Сумма по предложению с расценками после налогообложения</span><span class="sxs-lookup"><span data-stu-id="ccef3-166">Quoted Amount after Tax</span></span> | <span data-ttu-id="ccef3-167">Это поле является суммой строки предложения с расценками после уплаты налогов и предназначено только для чтения.</span><span class="sxs-lookup"><span data-stu-id="ccef3-167">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="ccef3-168">Сумма в этом поле рассчитывается как *Сумма по предложению с расценками + Налог*.</span><span class="sxs-lookup"><span data-stu-id="ccef3-168">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="ccef3-169">Значение этого поля копируется в строку контракта по проекту, которая создается из этой строки предложения с расценками, когда предложение с расценками выиграно.</span><span class="sxs-lookup"><span data-stu-id="ccef3-169">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="ccef3-170">Максимальный лимит</span><span class="sxs-lookup"><span data-stu-id="ccef3-170">Not-to-exceed Limit</span></span> | <span data-ttu-id="ccef3-171">Это поле доступно для редактирования и доступно только в строках предложения с расценками на основе проекта, в которых есть способ выставления счетов **Время и материал**.</span><span class="sxs-lookup"><span data-stu-id="ccef3-171">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="ccef3-172">Значение этого поля копируется в строку контракта по проекту, которая создается из этой строки предложения с расценками, когда предложение с расценками выиграно.</span><span class="sxs-lookup"><span data-stu-id="ccef3-172">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="ccef3-173">Бюджет клиента</span><span class="sxs-lookup"><span data-stu-id="ccef3-173">Customer Budget</span></span> | <span data-ttu-id="ccef3-174">Это поле доступно для редактирования и копируется из соответствующего поля в строке возможной сделки, если предложение с расценками было создано из возможной сделки.</span><span class="sxs-lookup"><span data-stu-id="ccef3-174">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="ccef3-175">Значение этого поля копируется в строку контракта по проекту, которая создается из этой строки предложения с расценками, когда предложение с расценками выиграно.</span><span class="sxs-lookup"><span data-stu-id="ccef3-175">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="ccef3-176">Правила проверки для полей на вкладке "Общие" строк предложения с расценками на основе проекта</span><span class="sxs-lookup"><span data-stu-id="ccef3-176">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="ccef3-177">**Правило 1** : если поле **Включенные задачи** пустое, или если для него установлено **Все задачи проекта** , проект включается в строку предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="ccef3-177">**Rule 1** : If the **Included Tasks** field is blank, or if it is set to **All project tasks** , a project is included in the quote line.</span></span>

<span data-ttu-id="ccef3-178">**Правило 2** : если поле **Включенные задачи** пустое или если для него установлено значение **Все задачи проекта** , проект и определенный класс транзакций могут быть включены только в одну строку предложения с расценками на основе проекта.</span><span class="sxs-lookup"><span data-stu-id="ccef3-178">**Rule 2** : If the **Included Tasks** field is blank, or if it is set to **All project tasks** , a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="ccef3-179">**Правило 3** : если поле **Включенные задачи** пустое или если для него установлено значение **Только выбранные задачи проекта** , проект и определенный класс транзакций могут быть включены в несколько строк предложения с расценками на основе проекта.</span><span class="sxs-lookup"><span data-stu-id="ccef3-179">**Rule 3** : If the **Included Tasks** field is set to **Selected project tasks only** , a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="ccef3-180">**Правило 4** : если у возможной сделки есть несколько предложений с расценками, могут быть строки предложения с расценками из разных предложений с расценками, которые все ссылаются на один и тот же проект и включают один и тот же класс транзакций.</span><span class="sxs-lookup"><span data-stu-id="ccef3-180">**Rule 4** : If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="ccef3-181">**Правило 5** : если предложения с расценками не относятся к одной и той же возможной сделке, они не могут включать один и тот же проект и класс транзакций.</span><span class="sxs-lookup"><span data-stu-id="ccef3-181">**Rule 5** : If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="ccef3-182">
                    <strong>Возможная сделка</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccef3-182">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="ccef3-183">
                    <strong>Предложение с расценками</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccef3-183">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="ccef3-184">
                    <strong>Строка предложения с расценками</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccef3-184">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="ccef3-185">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccef3-185">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="90" valign="top">
                <p><span data-ttu-id="ccef3-186">
                    <strong>Включенные задачи</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccef3-186">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="ccef3-187">
                    <strong>Включить время</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccef3-187">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="ccef3-188">
                    <strong>Включить расход</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccef3-188">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="ccef3-189">
                    <strong>Включить</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccef3-189">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="ccef3-190">
                    <strong>Сбор</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccef3-190">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="ccef3-191">
                    <strong>Действителен/Недействителен</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccef3-191">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="ccef3-192">
                    <strong>Причина</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ccef3-192">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="ccef3-193">O1</span><span class="sxs-lookup"><span data-stu-id="ccef3-193">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="ccef3-194">К1</span><span class="sxs-lookup"><span data-stu-id="ccef3-194">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ccef3-195">QL1</span><span class="sxs-lookup"><span data-stu-id="ccef3-195">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ccef3-196">П1</span><span class="sxs-lookup"><span data-stu-id="ccef3-196">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="ccef3-197">ПУСТО</span><span class="sxs-lookup"><span data-stu-id="ccef3-197">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ccef3-198">Да</span><span class="sxs-lookup"><span data-stu-id="ccef3-198">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ccef3-199">Да</span><span class="sxs-lookup"><span data-stu-id="ccef3-199">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ccef3-200">Да</span><span class="sxs-lookup"><span data-stu-id="ccef3-200">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ccef3-201">Недействительный</span><span class="sxs-lookup"><span data-stu-id="ccef3-201">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ccef3-202">Нарушение правила №2.</span><span class="sxs-lookup"><span data-stu-id="ccef3-202">Violation of Rule #2.</span></span> <span data-ttu-id="ccef3-203">Время, расходы и сборы по проекту P1 включены в строки предложения с расценками, QL1 и QL2.</span><span class="sxs-lookup"><span data-stu-id="ccef3-203">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="ccef3-204">O1</span><span class="sxs-lookup"><span data-stu-id="ccef3-204">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="ccef3-205">К1</span><span class="sxs-lookup"><span data-stu-id="ccef3-205">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ccef3-206">QL2</span><span class="sxs-lookup"><span data-stu-id="ccef3-206">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ccef3-207">П1</span><span class="sxs-lookup"><span data-stu-id="ccef3-207">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="ccef3-208">ПУСТО</span><span class="sxs-lookup"><span data-stu-id="ccef3-208">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ccef3-209">Да</span><span class="sxs-lookup"><span data-stu-id="ccef3-209">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ccef3-210">Да</span><span class="sxs-lookup"><span data-stu-id="ccef3-210">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ccef3-211">Да</span><span class="sxs-lookup"><span data-stu-id="ccef3-211">Yes</span></span> </p>
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
<span data-ttu-id="ccef3-212">O1</span><span class="sxs-lookup"><span data-stu-id="ccef3-212">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="ccef3-213">К1</span><span class="sxs-lookup"><span data-stu-id="ccef3-213">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ccef3-214">QL1</span><span class="sxs-lookup"><span data-stu-id="ccef3-214">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ccef3-215">П1</span><span class="sxs-lookup"><span data-stu-id="ccef3-215">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="ccef3-216">ПУСТО</span><span class="sxs-lookup"><span data-stu-id="ccef3-216">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ccef3-217">Да</span><span class="sxs-lookup"><span data-stu-id="ccef3-217">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ccef3-218">No</span><span class="sxs-lookup"><span data-stu-id="ccef3-218">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ccef3-219">Да</span><span class="sxs-lookup"><span data-stu-id="ccef3-219">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ccef3-220">Недействительный</span><span class="sxs-lookup"><span data-stu-id="ccef3-220">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ccef3-221">Нарушение правила №2.</span><span class="sxs-lookup"><span data-stu-id="ccef3-221">Violation of Rule #2.</span></span> <span data-ttu-id="ccef3-222">Время и сборы по проекту P1 включены в строки предложения с расценками QL1 и QL2.</span><span class="sxs-lookup"><span data-stu-id="ccef3-222">Time and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="ccef3-223">O1</span><span class="sxs-lookup"><span data-stu-id="ccef3-223">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="ccef3-224">К1</span><span class="sxs-lookup"><span data-stu-id="ccef3-224">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ccef3-225">QL2</span><span class="sxs-lookup"><span data-stu-id="ccef3-225">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ccef3-226">П1</span><span class="sxs-lookup"><span data-stu-id="ccef3-226">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="ccef3-227">ПУСТО</span><span class="sxs-lookup"><span data-stu-id="ccef3-227">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ccef3-228">Да</span><span class="sxs-lookup"><span data-stu-id="ccef3-228">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ccef3-229">Да</span><span class="sxs-lookup"><span data-stu-id="ccef3-229">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ccef3-230">Да</span><span class="sxs-lookup"><span data-stu-id="ccef3-230">Yes</span></span> </p>
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
<span data-ttu-id="ccef3-231">O1</span><span class="sxs-lookup"><span data-stu-id="ccef3-231">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="ccef3-232">К1</span><span class="sxs-lookup"><span data-stu-id="ccef3-232">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ccef3-233">QL1</span><span class="sxs-lookup"><span data-stu-id="ccef3-233">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ccef3-234">П1</span><span class="sxs-lookup"><span data-stu-id="ccef3-234">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="ccef3-235">ПУСТО</span><span class="sxs-lookup"><span data-stu-id="ccef3-235">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ccef3-236">Да</span><span class="sxs-lookup"><span data-stu-id="ccef3-236">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ccef3-237">No</span><span class="sxs-lookup"><span data-stu-id="ccef3-237">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ccef3-238">Да</span><span class="sxs-lookup"><span data-stu-id="ccef3-238">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ccef3-239">Действителен</span><span class="sxs-lookup"><span data-stu-id="ccef3-239">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
<span data-ttu-id="ccef3-240">Время и сборы по проекту P1 включены в QL1.</span><span class="sxs-lookup"><span data-stu-id="ccef3-240">Time and Fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="ccef3-241">Расходы по проекту P1 включены в QL2.</span><span class="sxs-lookup"><span data-stu-id="ccef3-241">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="ccef3-242">То, что включается в каждую строку предложения с расценками, не перекрывается и допустимо.</span><span class="sxs-lookup"><span data-stu-id="ccef3-242">There is no overlap in what is being included on each quote line and is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="ccef3-243">O1</span><span class="sxs-lookup"><span data-stu-id="ccef3-243">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="ccef3-244">К1</span><span class="sxs-lookup"><span data-stu-id="ccef3-244">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ccef3-245">QL2</span><span class="sxs-lookup"><span data-stu-id="ccef3-245">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ccef3-246">П1</span><span class="sxs-lookup"><span data-stu-id="ccef3-246">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="ccef3-247">ПУСТО</span><span class="sxs-lookup"><span data-stu-id="ccef3-247">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ccef3-248">No</span><span class="sxs-lookup"><span data-stu-id="ccef3-248">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ccef3-249">Да</span><span class="sxs-lookup"><span data-stu-id="ccef3-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ccef3-250">No</span><span class="sxs-lookup"><span data-stu-id="ccef3-250">No</span></span> </p>
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
<span data-ttu-id="ccef3-251">O1</span><span class="sxs-lookup"><span data-stu-id="ccef3-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="ccef3-252">К1</span><span class="sxs-lookup"><span data-stu-id="ccef3-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ccef3-253">QL1</span><span class="sxs-lookup"><span data-stu-id="ccef3-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ccef3-254">П1</span><span class="sxs-lookup"><span data-stu-id="ccef3-254">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="ccef3-255">Только выбранные задачи</span><span class="sxs-lookup"><span data-stu-id="ccef3-255">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ccef3-256">Да</span><span class="sxs-lookup"><span data-stu-id="ccef3-256">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ccef3-257">Да</span><span class="sxs-lookup"><span data-stu-id="ccef3-257">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ccef3-258">Да</span><span class="sxs-lookup"><span data-stu-id="ccef3-258">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ccef3-259">Недействительный</span><span class="sxs-lookup"><span data-stu-id="ccef3-259">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ccef3-260">Нарушение правила №2 выше</span><span class="sxs-lookup"><span data-stu-id="ccef3-260">Violation of Rule #2 above</span></span> </p>
                <p>
<span data-ttu-id="ccef3-261">Q1 включает время, расходы и сборы на подмножество задач по проекту P1.</span><span class="sxs-lookup"><span data-stu-id="ccef3-261">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="ccef3-262">QL2 включает время, расходы и сборы для всего проекта P1 и частично перекрывается с тем, что включено в Q1.</span><span class="sxs-lookup"><span data-stu-id="ccef3-262">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="ccef3-263">O1</span><span class="sxs-lookup"><span data-stu-id="ccef3-263">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="ccef3-264">К1</span><span class="sxs-lookup"><span data-stu-id="ccef3-264">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ccef3-265">QL2</span><span class="sxs-lookup"><span data-stu-id="ccef3-265">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ccef3-266">П1</span><span class="sxs-lookup"><span data-stu-id="ccef3-266">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="ccef3-267">ПУСТО</span><span class="sxs-lookup"><span data-stu-id="ccef3-267">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ccef3-268">Да</span><span class="sxs-lookup"><span data-stu-id="ccef3-268">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ccef3-269">Да</span><span class="sxs-lookup"><span data-stu-id="ccef3-269">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ccef3-270">Да</span><span class="sxs-lookup"><span data-stu-id="ccef3-270">Yes</span></span> </p>
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
<span data-ttu-id="ccef3-271">O1</span><span class="sxs-lookup"><span data-stu-id="ccef3-271">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="ccef3-272">К1</span><span class="sxs-lookup"><span data-stu-id="ccef3-272">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ccef3-273">QL1</span><span class="sxs-lookup"><span data-stu-id="ccef3-273">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ccef3-274">П1</span><span class="sxs-lookup"><span data-stu-id="ccef3-274">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="ccef3-275">Только выбранные задачи</span><span class="sxs-lookup"><span data-stu-id="ccef3-275">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ccef3-276">Да</span><span class="sxs-lookup"><span data-stu-id="ccef3-276">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ccef3-277">Да</span><span class="sxs-lookup"><span data-stu-id="ccef3-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ccef3-278">Да</span><span class="sxs-lookup"><span data-stu-id="ccef3-278">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ccef3-279">Действителен</span><span class="sxs-lookup"><span data-stu-id="ccef3-279">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ccef3-280">Согласно правилу № 3 выше,</span><span class="sxs-lookup"><span data-stu-id="ccef3-280">Per Rule #3 above,</span></span> </p>
                <p>
<span data-ttu-id="ccef3-281">Q1 включает время, расходы и сборы на подмножество задач по проекту P1.</span><span class="sxs-lookup"><span data-stu-id="ccef3-281">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="ccef3-282">QL2 включает время, расходы и сборы для подмножества задач по проекту P1.</span><span class="sxs-lookup"><span data-stu-id="ccef3-282">QL2 includes Time, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="ccef3-283">Единственная дополнительная проверка касается подмножества задач в QL1, которые отличаются от подмножества задач в QL2.</span><span class="sxs-lookup"><span data-stu-id="ccef3-283">The only additional validation is around the subset of tasks on QL1 which are different from the subset of tasks on QL2.</span></span> <span data-ttu-id="ccef3-284">Это гарантирует отсутствие перекрытий.</span><span class="sxs-lookup"><span data-stu-id="ccef3-284">This ensures that there are no overlaps.</span></span> <span data-ttu-id="ccef3-285">Это выполняется системой, когда задачи связаны.</span><span class="sxs-lookup"><span data-stu-id="ccef3-285">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="ccef3-286">O1</span><span class="sxs-lookup"><span data-stu-id="ccef3-286">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="ccef3-287">К1</span><span class="sxs-lookup"><span data-stu-id="ccef3-287">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ccef3-288">QL2</span><span class="sxs-lookup"><span data-stu-id="ccef3-288">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ccef3-289">П1</span><span class="sxs-lookup"><span data-stu-id="ccef3-289">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="ccef3-290">Только выбранные задачи</span><span class="sxs-lookup"><span data-stu-id="ccef3-290">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ccef3-291">Да</span><span class="sxs-lookup"><span data-stu-id="ccef3-291">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ccef3-292">Да</span><span class="sxs-lookup"><span data-stu-id="ccef3-292">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ccef3-293">Да</span><span class="sxs-lookup"><span data-stu-id="ccef3-293">Yes</span></span> </p>
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
<span data-ttu-id="ccef3-294">O1</span><span class="sxs-lookup"><span data-stu-id="ccef3-294">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="ccef3-295">К1</span><span class="sxs-lookup"><span data-stu-id="ccef3-295">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ccef3-296">QL1</span><span class="sxs-lookup"><span data-stu-id="ccef3-296">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ccef3-297">П1</span><span class="sxs-lookup"><span data-stu-id="ccef3-297">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="ccef3-298">Все задачи проекта или пусто</span><span class="sxs-lookup"><span data-stu-id="ccef3-298">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ccef3-299">Да</span><span class="sxs-lookup"><span data-stu-id="ccef3-299">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ccef3-300">Да</span><span class="sxs-lookup"><span data-stu-id="ccef3-300">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ccef3-301">Да</span><span class="sxs-lookup"><span data-stu-id="ccef3-301">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="ccef3-302">Действителен</span><span class="sxs-lookup"><span data-stu-id="ccef3-302">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ccef3-303">В соответствии с правилом № 5, Q1 и Q2 — это два предложения с расценками по одной и той же возможной сделке, поэтому они оба могут оценивать одни и те же компоненты проекта.</span><span class="sxs-lookup"><span data-stu-id="ccef3-303">Based on Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="ccef3-304">O1</span><span class="sxs-lookup"><span data-stu-id="ccef3-304">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="ccef3-305">К2</span><span class="sxs-lookup"><span data-stu-id="ccef3-305">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ccef3-306">QL1</span><span class="sxs-lookup"><span data-stu-id="ccef3-306">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ccef3-307">П1</span><span class="sxs-lookup"><span data-stu-id="ccef3-307">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="ccef3-308">Все задачи проекта или пусто</span><span class="sxs-lookup"><span data-stu-id="ccef3-308">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ccef3-309">Да</span><span class="sxs-lookup"><span data-stu-id="ccef3-309">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ccef3-310">Да</span><span class="sxs-lookup"><span data-stu-id="ccef3-310">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ccef3-311">Да</span><span class="sxs-lookup"><span data-stu-id="ccef3-311">Yes</span></span> </p>
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
<span data-ttu-id="ccef3-312">O1</span><span class="sxs-lookup"><span data-stu-id="ccef3-312">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="ccef3-313">К1</span><span class="sxs-lookup"><span data-stu-id="ccef3-313">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ccef3-314">QL1</span><span class="sxs-lookup"><span data-stu-id="ccef3-314">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ccef3-315">П1</span><span class="sxs-lookup"><span data-stu-id="ccef3-315">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="ccef3-316">Все задачи проекта или пусто</span><span class="sxs-lookup"><span data-stu-id="ccef3-316">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ccef3-317">Да</span><span class="sxs-lookup"><span data-stu-id="ccef3-317">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ccef3-318">Да</span><span class="sxs-lookup"><span data-stu-id="ccef3-318">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ccef3-319">Да</span><span class="sxs-lookup"><span data-stu-id="ccef3-319">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="ccef3-320">Действителен</span><span class="sxs-lookup"><span data-stu-id="ccef3-320">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ccef3-321">В соответствии с правилом № 4, Q1 и Q2 — это два предложения с расценками для разных возможных сделок, поэтому они не могут оценивать одни и те же компоненты одного проекта.</span><span class="sxs-lookup"><span data-stu-id="ccef3-321">Based on Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="ccef3-322">O2</span><span class="sxs-lookup"><span data-stu-id="ccef3-322">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="ccef3-323">К1</span><span class="sxs-lookup"><span data-stu-id="ccef3-323">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ccef3-324">QL1</span><span class="sxs-lookup"><span data-stu-id="ccef3-324">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ccef3-325">П1</span><span class="sxs-lookup"><span data-stu-id="ccef3-325">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="ccef3-326">Все задачи проекта или пусто</span><span class="sxs-lookup"><span data-stu-id="ccef3-326">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ccef3-327">Да</span><span class="sxs-lookup"><span data-stu-id="ccef3-327">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ccef3-328">Да</span><span class="sxs-lookup"><span data-stu-id="ccef3-328">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ccef3-329">Да</span><span class="sxs-lookup"><span data-stu-id="ccef3-329">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="ccef3-330">Недействительный</span><span class="sxs-lookup"><span data-stu-id="ccef3-330">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

