---
title: Обзор строк предложения с расценками на основе проекта
description: Эта тема предоставляет информацию об использовании строк предложения с расценками на основе проекта для работы по проекту.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 32337b05f09ef7c5b84fdff9870744d6367e2693
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994872"
---
# <a name="project-based-quote-lines-overview"></a><span data-ttu-id="96d1b-103">Обзор строк предложения с расценками на основе проекта</span><span class="sxs-lookup"><span data-stu-id="96d1b-103">Project-based quote lines overview</span></span> 

<span data-ttu-id="96d1b-104">_**Относится к:** Облегченное развертывание — от сделки до счетов-проформ, Project Operations для сценариев на основе ресурсов/нескладируемых запасов_</span><span class="sxs-lookup"><span data-stu-id="96d1b-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="96d1b-105">Строки предложений с расценками на основе проекта предназначены для помощи в оценке проектной работы по заданию.</span><span class="sxs-lookup"><span data-stu-id="96d1b-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="96d1b-106">Структура строки предложения с расценками по проекту расширена для оценок проекта за счет следующих понятий:</span><span class="sxs-lookup"><span data-stu-id="96d1b-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="96d1b-107">Метод выставления счета</span><span class="sxs-lookup"><span data-stu-id="96d1b-107">Billing Method</span></span>
- <span data-ttu-id="96d1b-108">Сопоставление проектов и задач</span><span class="sxs-lookup"><span data-stu-id="96d1b-108">Project and Task Mapping</span></span>
- <span data-ttu-id="96d1b-109">Включенные классы транзакций</span><span class="sxs-lookup"><span data-stu-id="96d1b-109">Included Transaction classes</span></span>
- <span data-ttu-id="96d1b-110">Максимальный лимит</span><span class="sxs-lookup"><span data-stu-id="96d1b-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="96d1b-111">Настройка возможности оплаты</span><span class="sxs-lookup"><span data-stu-id="96d1b-111">Chargeability setup</span></span>
- <span data-ttu-id="96d1b-112">Оценка с использованием сведений строки предложения с расценками</span><span class="sxs-lookup"><span data-stu-id="96d1b-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="96d1b-113">Клиенты строки предложения с расценками</span><span class="sxs-lookup"><span data-stu-id="96d1b-113">Quote line Customers</span></span>

<span data-ttu-id="96d1b-114">В следующей таблице представлена информация о полях на вкладке **Общее** строки предложения с расценками по проекту.</span><span class="sxs-lookup"><span data-stu-id="96d1b-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="96d1b-115">Эти поля помогают настроить основу для подробной, основательной оценки проектной работы.</span><span class="sxs-lookup"><span data-stu-id="96d1b-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="96d1b-116">**Поле**</span><span class="sxs-lookup"><span data-stu-id="96d1b-116">**Field**</span></span> | <span data-ttu-id="96d1b-117">**Описание**</span><span class="sxs-lookup"><span data-stu-id="96d1b-117">**Description**</span></span> | <span data-ttu-id="96d1b-118">**Воздействие на последующие элементы**</span><span class="sxs-lookup"><span data-stu-id="96d1b-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="96d1b-119">имени</span><span class="sxs-lookup"><span data-stu-id="96d1b-119">Name</span></span> | <span data-ttu-id="96d1b-120">Название строки предложения с расценками, которая помогает вам идентифицировать дискретный компонент оцениваемого предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="96d1b-120">The name of quote line that helps you to identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="96d1b-121">Копируется в строку контракта по проекту, которая создается из этой строки предложения с расценками, когда предложение с расценками выиграно.</span><span class="sxs-lookup"><span data-stu-id="96d1b-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="96d1b-122">Метод выставления счета</span><span class="sxs-lookup"><span data-stu-id="96d1b-122">Billing Method</span></span> | <span data-ttu-id="96d1b-123">В предложении с расценками, созданном на основе возможной сделки, это значение копируется из соответствующего поля в строке возможной сделки.</span><span class="sxs-lookup"><span data-stu-id="96d1b-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="96d1b-124">Это поле включает две основные модели заключения контрактов, поддерживаемые Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="96d1b-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="96d1b-125">- Фиксированная цена</span><span class="sxs-lookup"><span data-stu-id="96d1b-125">- Fixed price</span></span></br><span data-ttu-id="96d1b-126">- Время и материал.</span><span class="sxs-lookup"><span data-stu-id="96d1b-126">- Time and material.</span></span>| <span data-ttu-id="96d1b-127">Это значение копируется в строку контракта по проекту, которая создается из этой строки предложения с расценками, когда предложение с расценками реализовано.</span><span class="sxs-lookup"><span data-stu-id="96d1b-127">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="96d1b-128">Project</span><span class="sxs-lookup"><span data-stu-id="96d1b-128">Project</span></span> | <span data-ttu-id="96d1b-129">Используйте это необязательное поле, чтобы определить проект, который будет использоваться для выполнения работы по данному заданию.</span><span class="sxs-lookup"><span data-stu-id="96d1b-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="96d1b-130">Когда проект сопоставляется со строкой предложения с расценками, это помогает с настройкой оплачиваемых задач, а также с внесением оценки на основе проекта в строку предложения с расценками в качестве сведений строки предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="96d1b-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="96d1b-131">Если проект не сопоставлен со строкой предложения с расценками по проекту, оценку следует создать вручную, создав сведения каждой строки предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="96d1b-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="96d1b-132">Это значение копируется в строку контракта по проекту, которая создается из этой строки предложения с расценками, когда предложение с расценками реализовано.</span><span class="sxs-lookup"><span data-stu-id="96d1b-132">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="96d1b-133">Включенные задачи</span><span class="sxs-lookup"><span data-stu-id="96d1b-133">Included Tasks</span></span> | <span data-ttu-id="96d1b-134">Указывает, используется ли эта строка предложения с расценками для всех или некоторых задач проекта для выбранного проекта.</span><span class="sxs-lookup"><span data-stu-id="96d1b-134">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="96d1b-135">Это поле имеет следующие возможные значения:</span><span class="sxs-lookup"><span data-stu-id="96d1b-135">This field has the following possible values:</span></span></br><span data-ttu-id="96d1b-136">- Все задачи проекта</span><span class="sxs-lookup"><span data-stu-id="96d1b-136">- All project tasks</span></span></br><span data-ttu-id="96d1b-137">- Только выбранные задачи проекта</span><span class="sxs-lookup"><span data-stu-id="96d1b-137">- Selected project tasks only</span></span></br><span data-ttu-id="96d1b-138">Пустое значение в этом поле эквивалентно варианту **Все задачи проекта**.</span><span class="sxs-lookup"><span data-stu-id="96d1b-138">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="96d1b-139">Когда **Только выбранные задачи проекта** выбрано на странице проекта, на вкладке **Настройка выставления счетов по задачам** можно выбрать определенные задачи, чтобы связать их с этой строкой предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="96d1b-139">When **Selected project tasks only** is selected on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="96d1b-140">Это значение копируется в строку контракта по проекту, которая создается из этой строки предложения с расценками, когда предложение с расценками реализовано.</span><span class="sxs-lookup"><span data-stu-id="96d1b-140">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="96d1b-141">Включить время</span><span class="sxs-lookup"><span data-stu-id="96d1b-141">Include Time</span></span> | <span data-ttu-id="96d1b-142">Значение **Да**/**Нет** указывает, будут ли включены в оценку для этой строки предложения с расценками транзакции времени или затраты на оплату труда по выбранному проекту.</span><span class="sxs-lookup"><span data-stu-id="96d1b-142">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="96d1b-143">Значение **Нет** указывает, что транзакции времени или трудозатраты не будут включены в оценку в этой строке предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="96d1b-143">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="96d1b-144">Значение **Да** указывает, что транзакции времени или трудозатраты будут включены в оценку в этой строке предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="96d1b-144">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="96d1b-145">Это значение копируется в строку контракта по проекту, которая создается из этой строки предложения с расценками, когда предложение с расценками реализовано.</span><span class="sxs-lookup"><span data-stu-id="96d1b-145">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="96d1b-146">Включить расход</span><span class="sxs-lookup"><span data-stu-id="96d1b-146">Include Expense</span></span> | <span data-ttu-id="96d1b-147">Значение **Да**/**Нет** указывает, будет ли включены в оценку для этой строки предложения с расценками стоимость расходов по выбранному проекту.</span><span class="sxs-lookup"><span data-stu-id="96d1b-147">A **Yes**/**No** value indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="96d1b-148">Значение **Нет** указывает, что затраты не будут включены в оценку в этой строке предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="96d1b-148">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="96d1b-149">Значение **Да** указывает, что затраты будут включены в оценку в этой строке предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="96d1b-149">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="96d1b-150">Это значение копируется в строку контракта по проекту, которая создается из этой строки предложения с расценками, когда предложение с расценками реализовано.</span><span class="sxs-lookup"><span data-stu-id="96d1b-150">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="96d1b-151">Включить материал</span><span class="sxs-lookup"><span data-stu-id="96d1b-151">Include Material</span></span> | <span data-ttu-id="96d1b-152">Значение **Да**/**Нет** указывает, будет ли включены в оценку для этой строки предложения с расценками стоимость материалов по выбранному проекту.</span><span class="sxs-lookup"><span data-stu-id="96d1b-152">A **Yes**/**No** value indicates if material costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="96d1b-153">Значение **Нет** указывает, что в оценку этой строки предложения с расценками стоимость материалов по выбранному проекту не будет включена.</span><span class="sxs-lookup"><span data-stu-id="96d1b-153">A **No** value indicates that the material costs will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="96d1b-154">Значение **Да** указывает, что в оценку этой строки предложения с расценками стоимость материалов по выбранному проекту будет включена.</span><span class="sxs-lookup"><span data-stu-id="96d1b-154">A **Yes** value indicates that the material costs will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="96d1b-155">Это значение копируется в строку контракта по проекту, которая создается из этой строки предложения с расценками, когда предложение с расценками реализовано.</span><span class="sxs-lookup"><span data-stu-id="96d1b-155">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="96d1b-156">Включить сбор</span><span class="sxs-lookup"><span data-stu-id="96d1b-156">Include Fee</span></span> | <span data-ttu-id="96d1b-157">Значение **Да**/**Нет** указывает, будут ли включены в оценку для этой строки предложения с расценками сборы по выбранному проекту.</span><span class="sxs-lookup"><span data-stu-id="96d1b-157">A **Yes**/**No** value indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="96d1b-158">Значение **Нет** указывает, что сборы не будут включены в оценку в этой строке предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="96d1b-158">A **No** value indicates that the fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="96d1b-159">Значение **Да** указывает, что сборы будут включены в оценку в этой строке предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="96d1b-159">A **Yes** value indicates that the fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="96d1b-160">Это значение копируется в строку контракта по проекту, которая создается из этой строки предложения с расценками, когда предложение с расценками реализовано.</span><span class="sxs-lookup"><span data-stu-id="96d1b-160">This value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="96d1b-161">Сумма по предложению</span><span class="sxs-lookup"><span data-stu-id="96d1b-161">Quoted Amount</span></span> | <span data-ttu-id="96d1b-162">Это сумма, которая будет указана в предложении с расценками для заказчика за все работы, прогнозируемые в данной строке предложения с расценками на основе проекта.</span><span class="sxs-lookup"><span data-stu-id="96d1b-162">This is the amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="96d1b-163">В предложении с расценками, созданном на основе возможной сделки, это значение копируется из поля **Бюджет клиента** в строке возможной сделки.</span><span class="sxs-lookup"><span data-stu-id="96d1b-163">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="96d1b-164">Если в строке предложения с расценками по проекту есть сведения о строке, это поле заблокировано для редактирования и суммируется из суммы в сведениях строки предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="96d1b-164">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="96d1b-165">Это значение копируется в строку контракта по проекту, которая создается из этой строки предложения с расценками, когда предложение с расценками реализовано.</span><span class="sxs-lookup"><span data-stu-id="96d1b-165">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="96d1b-166">Ожидаемый налог</span><span class="sxs-lookup"><span data-stu-id="96d1b-166">Estimated Tax</span></span> | <span data-ttu-id="96d1b-167">Это редактируемое поле, в котором пользователь может добавить расчетную сумму налога в строку предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="96d1b-167">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="96d1b-168">Если в строке предложения с расценками по проекту есть сведения о строке, это поле заблокировано для редактирования и суммируется из суммы налога в сведениях строки предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="96d1b-168">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="96d1b-169">Это значение копируется в строку контракта по проекту, которая создается из этой строки предложения с расценками, когда предложение с расценками реализовано.</span><span class="sxs-lookup"><span data-stu-id="96d1b-169">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="96d1b-170">Сумма по предложению с расценками после налогообложения</span><span class="sxs-lookup"><span data-stu-id="96d1b-170">Quoted Amount after Tax</span></span> | <span data-ttu-id="96d1b-171">Это поле является суммой строки предложения с расценками после уплаты налогов и предназначено только для чтения.</span><span class="sxs-lookup"><span data-stu-id="96d1b-171">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="96d1b-172">Сумма в этом поле рассчитывается как *Сумма по предложению с расценками + Налог*.</span><span class="sxs-lookup"><span data-stu-id="96d1b-172">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="96d1b-173">Это значение копируется в строку контракта по проекту, которая создается из этой строки предложения с расценками, когда предложение с расценками реализовано.</span><span class="sxs-lookup"><span data-stu-id="96d1b-173">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="96d1b-174">Максимальный лимит</span><span class="sxs-lookup"><span data-stu-id="96d1b-174">Not-to-exceed Limit</span></span> | <span data-ttu-id="96d1b-175">Это поле доступно для редактирования и доступно только в строках предложения с расценками на основе проекта, в которых есть способ выставления счетов **Время и материал**.</span><span class="sxs-lookup"><span data-stu-id="96d1b-175">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="96d1b-176">Это значение копируется в строку контракта по проекту, которая создается из этой строки предложения с расценками, когда предложение с расценками реализовано.</span><span class="sxs-lookup"><span data-stu-id="96d1b-176">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="96d1b-177">Бюджет клиента</span><span class="sxs-lookup"><span data-stu-id="96d1b-177">Customer Budget</span></span> | <span data-ttu-id="96d1b-178">Это поле доступно для редактирования и копируется из соответствующего поля в строке возможной сделки, если предложение с расценками было создано из возможной сделки.</span><span class="sxs-lookup"><span data-stu-id="96d1b-178">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="96d1b-179">Это значение копируется в строку контракта по проекту, которая создается из этой строки предложения с расценками, когда предложение с расценками реализовано.</span><span class="sxs-lookup"><span data-stu-id="96d1b-179">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="96d1b-180">Правила проверки для полей на вкладке "Общие" строк предложения с расценками на основе проекта</span><span class="sxs-lookup"><span data-stu-id="96d1b-180">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="96d1b-181">**Правило 1**: если поле **Включенные задачи** пустое, или если для него установлено **Все задачи проекта**, проект включается в строку предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="96d1b-181">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="96d1b-182">**Правило 2**: если поле **Включенные задачи** пустое или если для него установлено значение **Все задачи проекта**, проект и определенный класс транзакций могут быть включены только в одну строку предложения с расценками на основе проекта.</span><span class="sxs-lookup"><span data-stu-id="96d1b-182">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="96d1b-183">**Правило 3**: если поле **Включенные задачи** пустое или если для него установлено значение **Только выбранные задачи проекта**, проект и определенный класс транзакций могут быть включены в несколько строк предложения с расценками на основе проекта.</span><span class="sxs-lookup"><span data-stu-id="96d1b-183">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="96d1b-184">**Правило 4**: если у возможной сделки есть несколько предложений с расценками, могут быть строки предложения с расценками из разных предложений с расценками, которые все ссылаются на один и тот же проект и включают один и тот же класс транзакций.</span><span class="sxs-lookup"><span data-stu-id="96d1b-184">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="96d1b-185">**Правило 5**: если предложения с расценками не относятся к одной и той же возможной сделке, они не могут включать один и тот же проект и класс транзакций.</span><span class="sxs-lookup"><span data-stu-id="96d1b-185">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p><span data-ttu-id="96d1b-186">
                    <strong>Возможная сделка</strong>
                </span><span class="sxs-lookup"><span data-stu-id="96d1b-186">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="39" valign="top">
                <p><span data-ttu-id="96d1b-187">
                    <strong>Предложение с расценками</strong>
                </span><span class="sxs-lookup"><span data-stu-id="96d1b-187">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="40" valign="top">
                <p><span data-ttu-id="96d1b-188">
                    <strong>Строка предложения с расценками</strong>
                </span><span class="sxs-lookup"><span data-stu-id="96d1b-188">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="96d1b-189">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="96d1b-189">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="77" valign="top">
                <p><span data-ttu-id="96d1b-190">
                    <strong>Включенные задачи</strong>
                </span><span class="sxs-lookup"><span data-stu-id="96d1b-190">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="45" valign="top">
                <p><span data-ttu-id="96d1b-191">
                    <strong>Включить время</strong>
                </span><span class="sxs-lookup"><span data-stu-id="96d1b-191">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="46" valign="top">
                <p><span data-ttu-id="96d1b-192">
                    <strong>Включить расход</strong>
                </span><span class="sxs-lookup"><span data-stu-id="96d1b-192">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="43" valign="top">
                <p><span data-ttu-id="96d1b-193">
                    <strong>Включить материал</strong>
                </span><span class="sxs-lookup"><span data-stu-id="96d1b-193">
                    <strong>Include Material</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="96d1b-194">
                    <strong>Включить</strong>
                </span><span class="sxs-lookup"><span data-stu-id="96d1b-194">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="96d1b-195">
                    <strong>Сбор</strong>
                </span><span class="sxs-lookup"><span data-stu-id="96d1b-195">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="49" valign="top">
                <p><span data-ttu-id="96d1b-196">
                    <strong>Действителен/Недействителен</strong>
                </span><span class="sxs-lookup"><span data-stu-id="96d1b-196">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="200" valign="top">
                <p><span data-ttu-id="96d1b-197">
                    <strong>Причина</strong>
                </span><span class="sxs-lookup"><span data-stu-id="96d1b-197">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="96d1b-198">O1</span><span class="sxs-lookup"><span data-stu-id="96d1b-198">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="96d1b-199">К1</span><span class="sxs-lookup"><span data-stu-id="96d1b-199">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="96d1b-200">QL1</span><span class="sxs-lookup"><span data-stu-id="96d1b-200">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96d1b-201">П1</span><span class="sxs-lookup"><span data-stu-id="96d1b-201">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="96d1b-202">Пусто</span><span class="sxs-lookup"><span data-stu-id="96d1b-202">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="96d1b-203">Да</span><span class="sxs-lookup"><span data-stu-id="96d1b-203">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="96d1b-204">Да</span><span class="sxs-lookup"><span data-stu-id="96d1b-204">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="96d1b-205">Да</span><span class="sxs-lookup"><span data-stu-id="96d1b-205">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96d1b-206">Да</span><span class="sxs-lookup"><span data-stu-id="96d1b-206">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="96d1b-207">Недействительный</span><span class="sxs-lookup"><span data-stu-id="96d1b-207">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="96d1b-208">Нарушение правила №2.</span><span class="sxs-lookup"><span data-stu-id="96d1b-208">Violation of Rule #2.</span></span> <span data-ttu-id="96d1b-209">Время, расходы и сборы по проекту P1 включены в строки предложения с расценками, QL1 и QL2</span><span class="sxs-lookup"><span data-stu-id="96d1b-209">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="96d1b-210">O1</span><span class="sxs-lookup"><span data-stu-id="96d1b-210">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="96d1b-211">К1</span><span class="sxs-lookup"><span data-stu-id="96d1b-211">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="96d1b-212">QL2</span><span class="sxs-lookup"><span data-stu-id="96d1b-212">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96d1b-213">П1</span><span class="sxs-lookup"><span data-stu-id="96d1b-213">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="96d1b-214">Пусто</span><span class="sxs-lookup"><span data-stu-id="96d1b-214">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="96d1b-215">Да</span><span class="sxs-lookup"><span data-stu-id="96d1b-215">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="96d1b-216">Да</span><span class="sxs-lookup"><span data-stu-id="96d1b-216">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="96d1b-217">Да</span><span class="sxs-lookup"><span data-stu-id="96d1b-217">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96d1b-218">Да</span><span class="sxs-lookup"><span data-stu-id="96d1b-218">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="96d1b-219">O1</span><span class="sxs-lookup"><span data-stu-id="96d1b-219">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="96d1b-220">К1</span><span class="sxs-lookup"><span data-stu-id="96d1b-220">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="96d1b-221">QL1</span><span class="sxs-lookup"><span data-stu-id="96d1b-221">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96d1b-222">П1</span><span class="sxs-lookup"><span data-stu-id="96d1b-222">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="96d1b-223">Пусто</span><span class="sxs-lookup"><span data-stu-id="96d1b-223">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="96d1b-224">Да</span><span class="sxs-lookup"><span data-stu-id="96d1b-224">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="96d1b-225">No</span><span class="sxs-lookup"><span data-stu-id="96d1b-225">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="96d1b-226">Да</span><span class="sxs-lookup"><span data-stu-id="96d1b-226">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96d1b-227">Да</span><span class="sxs-lookup"><span data-stu-id="96d1b-227">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="96d1b-228">Недействительный</span><span class="sxs-lookup"><span data-stu-id="96d1b-228">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="96d1b-229">Нарушение правила №2.</span><span class="sxs-lookup"><span data-stu-id="96d1b-229">Violation of Rule #2.</span></span> <span data-ttu-id="96d1b-230">Время, материалы и сборы по проекту P1 включены в строки предложения с расценками, QL1 и QL2</span><span class="sxs-lookup"><span data-stu-id="96d1b-230">Time, Material, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="96d1b-231">O1</span><span class="sxs-lookup"><span data-stu-id="96d1b-231">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="96d1b-232">К1</span><span class="sxs-lookup"><span data-stu-id="96d1b-232">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="96d1b-233">QL2</span><span class="sxs-lookup"><span data-stu-id="96d1b-233">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96d1b-234">П1</span><span class="sxs-lookup"><span data-stu-id="96d1b-234">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="96d1b-235">Пусто</span><span class="sxs-lookup"><span data-stu-id="96d1b-235">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="96d1b-236">Да</span><span class="sxs-lookup"><span data-stu-id="96d1b-236">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="96d1b-237">Да</span><span class="sxs-lookup"><span data-stu-id="96d1b-237">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="96d1b-238">Да</span><span class="sxs-lookup"><span data-stu-id="96d1b-238">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96d1b-239">Да</span><span class="sxs-lookup"><span data-stu-id="96d1b-239">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="96d1b-240">O1</span><span class="sxs-lookup"><span data-stu-id="96d1b-240">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="96d1b-241">К1</span><span class="sxs-lookup"><span data-stu-id="96d1b-241">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="96d1b-242">QL1</span><span class="sxs-lookup"><span data-stu-id="96d1b-242">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96d1b-243">П1</span><span class="sxs-lookup"><span data-stu-id="96d1b-243">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="96d1b-244">Пусто</span><span class="sxs-lookup"><span data-stu-id="96d1b-244">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="96d1b-245">Да</span><span class="sxs-lookup"><span data-stu-id="96d1b-245">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="96d1b-246">No</span><span class="sxs-lookup"><span data-stu-id="96d1b-246">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="96d1b-247">Да</span><span class="sxs-lookup"><span data-stu-id="96d1b-247">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96d1b-248">Да</span><span class="sxs-lookup"><span data-stu-id="96d1b-248">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="96d1b-249">Действителен</span><span class="sxs-lookup"><span data-stu-id="96d1b-249">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="96d1b-250">Время, материал и сборы по проекту P1 включены в QL1</span><span class="sxs-lookup"><span data-stu-id="96d1b-250">Time, Material, and Fees on P1 project are included on QL1</span></span> <br>
<span data-ttu-id="96d1b-251">Расходы по проекту P1 включены в QL2</span><span class="sxs-lookup"><span data-stu-id="96d1b-251">Expense on P1 project is included on QL2</span></span> <br>
<span data-ttu-id="96d1b-252">Нет перекрытия того, что включено в каждую строку предложения с расценками и, следовательно, все правильно.</span><span class="sxs-lookup"><span data-stu-id="96d1b-252">No overlap in what is being included on each quote line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="96d1b-253">O1</span><span class="sxs-lookup"><span data-stu-id="96d1b-253">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="96d1b-254">К1</span><span class="sxs-lookup"><span data-stu-id="96d1b-254">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="96d1b-255">QL2</span><span class="sxs-lookup"><span data-stu-id="96d1b-255">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96d1b-256">П1</span><span class="sxs-lookup"><span data-stu-id="96d1b-256">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="96d1b-257">Пусто</span><span class="sxs-lookup"><span data-stu-id="96d1b-257">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="96d1b-258">No</span><span class="sxs-lookup"><span data-stu-id="96d1b-258">No</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="96d1b-259">Да</span><span class="sxs-lookup"><span data-stu-id="96d1b-259">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="96d1b-260">No</span><span class="sxs-lookup"><span data-stu-id="96d1b-260">No</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96d1b-261">No</span><span class="sxs-lookup"><span data-stu-id="96d1b-261">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="96d1b-262">O1</span><span class="sxs-lookup"><span data-stu-id="96d1b-262">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="96d1b-263">К1</span><span class="sxs-lookup"><span data-stu-id="96d1b-263">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="96d1b-264">QL1</span><span class="sxs-lookup"><span data-stu-id="96d1b-264">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96d1b-265">П1</span><span class="sxs-lookup"><span data-stu-id="96d1b-265">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="96d1b-266">Только выбранные задачи</span><span class="sxs-lookup"><span data-stu-id="96d1b-266">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="96d1b-267">Да</span><span class="sxs-lookup"><span data-stu-id="96d1b-267">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="96d1b-268">Да</span><span class="sxs-lookup"><span data-stu-id="96d1b-268">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="96d1b-269">Да</span><span class="sxs-lookup"><span data-stu-id="96d1b-269">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96d1b-270">Да</span><span class="sxs-lookup"><span data-stu-id="96d1b-270">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="96d1b-271">Недействительный</span><span class="sxs-lookup"><span data-stu-id="96d1b-271">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="96d1b-272">Нарушение правила № 2</span><span class="sxs-lookup"><span data-stu-id="96d1b-272">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="96d1b-273">Q1 включает время, материал, расходы и сборы по подмножеству задач по проекту P1</span><span class="sxs-lookup"><span data-stu-id="96d1b-273">Q1 includes Time, Material, Expenses and Fees on a subset of tasks on project P1</span></span> </p>
                <p>
<span data-ttu-id="96d1b-274">QL2 включает время, расходы и сборы для всего проекта P1 и поэтому частично совпадает с тем, что включено в Q1.</span><span class="sxs-lookup"><span data-stu-id="96d1b-274">QL2 includes Time, Expenses, and Fees for the whole project P1 and therefore overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="96d1b-275">O1</span><span class="sxs-lookup"><span data-stu-id="96d1b-275">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="96d1b-276">К1</span><span class="sxs-lookup"><span data-stu-id="96d1b-276">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="96d1b-277">QL2</span><span class="sxs-lookup"><span data-stu-id="96d1b-277">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96d1b-278">П1</span><span class="sxs-lookup"><span data-stu-id="96d1b-278">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="96d1b-279">Пусто</span><span class="sxs-lookup"><span data-stu-id="96d1b-279">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="96d1b-280">Да</span><span class="sxs-lookup"><span data-stu-id="96d1b-280">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="96d1b-281">Да</span><span class="sxs-lookup"><span data-stu-id="96d1b-281">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="96d1b-282">Да</span><span class="sxs-lookup"><span data-stu-id="96d1b-282">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96d1b-283">Да</span><span class="sxs-lookup"><span data-stu-id="96d1b-283">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="96d1b-284">O1</span><span class="sxs-lookup"><span data-stu-id="96d1b-284">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="96d1b-285">К1</span><span class="sxs-lookup"><span data-stu-id="96d1b-285">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="96d1b-286">QL1</span><span class="sxs-lookup"><span data-stu-id="96d1b-286">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96d1b-287">П1</span><span class="sxs-lookup"><span data-stu-id="96d1b-287">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="96d1b-288">Только выбранные задачи</span><span class="sxs-lookup"><span data-stu-id="96d1b-288">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="96d1b-289">Да</span><span class="sxs-lookup"><span data-stu-id="96d1b-289">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="96d1b-290">Да</span><span class="sxs-lookup"><span data-stu-id="96d1b-290">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="96d1b-291">Да</span><span class="sxs-lookup"><span data-stu-id="96d1b-291">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96d1b-292">Да</span><span class="sxs-lookup"><span data-stu-id="96d1b-292">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="96d1b-293">Действителен</span><span class="sxs-lookup"><span data-stu-id="96d1b-293">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="96d1b-294">Согласно правилу № 3</span><span class="sxs-lookup"><span data-stu-id="96d1b-294">Per Rule #3,</span></span> </p>
                <p>
<span data-ttu-id="96d1b-295">Q1 включает время, материал, расходы и сборы по подмножеству задач по проекту P1.</span><span class="sxs-lookup"><span data-stu-id="96d1b-295">Q1 includes Time, Material, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="96d1b-296">QL2 включает время, материал, расходы и сборы для подмножества задач по проекту P1.</span><span class="sxs-lookup"><span data-stu-id="96d1b-296">QL2 includes Time, Material, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="96d1b-297">Единственная дополнительная проверка связана с тем, что подмножество задач в QL1 отличается от подмножества задач в QL2, чтобы гарантировать, что там нет перекрытий.</span><span class="sxs-lookup"><span data-stu-id="96d1b-297">The only additional validation is around the subset of tasks on QL1 which is different from the subset of tasks on QL2 to ensure that there is no overlap.</span></span> <span data-ttu-id="96d1b-298">Это выполняется системой, когда задачи связаны.</span><span class="sxs-lookup"><span data-stu-id="96d1b-298">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="96d1b-299">O1</span><span class="sxs-lookup"><span data-stu-id="96d1b-299">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="96d1b-300">К1</span><span class="sxs-lookup"><span data-stu-id="96d1b-300">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="96d1b-301">QL2</span><span class="sxs-lookup"><span data-stu-id="96d1b-301">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96d1b-302">П1</span><span class="sxs-lookup"><span data-stu-id="96d1b-302">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="96d1b-303">Только выбранные задачи</span><span class="sxs-lookup"><span data-stu-id="96d1b-303">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="96d1b-304">Да</span><span class="sxs-lookup"><span data-stu-id="96d1b-304">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="96d1b-305">Да</span><span class="sxs-lookup"><span data-stu-id="96d1b-305">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="96d1b-306">Да</span><span class="sxs-lookup"><span data-stu-id="96d1b-306">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96d1b-307">Да</span><span class="sxs-lookup"><span data-stu-id="96d1b-307">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="96d1b-308">O1</span><span class="sxs-lookup"><span data-stu-id="96d1b-308">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="96d1b-309">К1</span><span class="sxs-lookup"><span data-stu-id="96d1b-309">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="96d1b-310">QL1</span><span class="sxs-lookup"><span data-stu-id="96d1b-310">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96d1b-311">П1</span><span class="sxs-lookup"><span data-stu-id="96d1b-311">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="96d1b-312">Все задачи проекта или пусто</span><span class="sxs-lookup"><span data-stu-id="96d1b-312">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="96d1b-313">Да</span><span class="sxs-lookup"><span data-stu-id="96d1b-313">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="96d1b-314">Да</span><span class="sxs-lookup"><span data-stu-id="96d1b-314">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="96d1b-315">Да</span><span class="sxs-lookup"><span data-stu-id="96d1b-315">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96d1b-316">Да</span><span class="sxs-lookup"><span data-stu-id="96d1b-316">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="96d1b-317">Действителен</span><span class="sxs-lookup"><span data-stu-id="96d1b-317">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="96d1b-318">Согласно правилу № 5, Q1 и Q2 — это два предложения с расценками по одной и той же возможной сделке, поэтому они оба могут оценивать одни и те же компоненты проекта.</span><span class="sxs-lookup"><span data-stu-id="96d1b-318">Per Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="96d1b-319">O1</span><span class="sxs-lookup"><span data-stu-id="96d1b-319">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="96d1b-320">К2</span><span class="sxs-lookup"><span data-stu-id="96d1b-320">Q2</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="96d1b-321">QL1</span><span class="sxs-lookup"><span data-stu-id="96d1b-321">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96d1b-322">П1</span><span class="sxs-lookup"><span data-stu-id="96d1b-322">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="96d1b-323">Все задачи проекта или пусто</span><span class="sxs-lookup"><span data-stu-id="96d1b-323">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="96d1b-324">Да</span><span class="sxs-lookup"><span data-stu-id="96d1b-324">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="96d1b-325">Да</span><span class="sxs-lookup"><span data-stu-id="96d1b-325">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="96d1b-326">Да</span><span class="sxs-lookup"><span data-stu-id="96d1b-326">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96d1b-327">Да</span><span class="sxs-lookup"><span data-stu-id="96d1b-327">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="96d1b-328">O1</span><span class="sxs-lookup"><span data-stu-id="96d1b-328">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="96d1b-329">К1</span><span class="sxs-lookup"><span data-stu-id="96d1b-329">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="96d1b-330">QL1</span><span class="sxs-lookup"><span data-stu-id="96d1b-330">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96d1b-331">П1</span><span class="sxs-lookup"><span data-stu-id="96d1b-331">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="96d1b-332">Все задачи проекта или пусто</span><span class="sxs-lookup"><span data-stu-id="96d1b-332">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="96d1b-333">Да</span><span class="sxs-lookup"><span data-stu-id="96d1b-333">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="96d1b-334">Да</span><span class="sxs-lookup"><span data-stu-id="96d1b-334">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="96d1b-335">Да</span><span class="sxs-lookup"><span data-stu-id="96d1b-335">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96d1b-336">Да</span><span class="sxs-lookup"><span data-stu-id="96d1b-336">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="96d1b-337">Недействительный</span><span class="sxs-lookup"><span data-stu-id="96d1b-337">Not Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="96d1b-338">Согласно правилу № 4, Q1 и Q2 — это два предложения с расценками по разным возможным сделкам, поэтому они оба не могут оценивать одни и те же компоненты одного проекта.</span><span class="sxs-lookup"><span data-stu-id="96d1b-338">Per Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="96d1b-339">O2</span><span class="sxs-lookup"><span data-stu-id="96d1b-339">O2</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="96d1b-340">К1</span><span class="sxs-lookup"><span data-stu-id="96d1b-340">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="96d1b-341">QL1</span><span class="sxs-lookup"><span data-stu-id="96d1b-341">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96d1b-342">П1</span><span class="sxs-lookup"><span data-stu-id="96d1b-342">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="96d1b-343">Все задачи проекта или пусто</span><span class="sxs-lookup"><span data-stu-id="96d1b-343">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="96d1b-344">Да</span><span class="sxs-lookup"><span data-stu-id="96d1b-344">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="96d1b-345">Да</span><span class="sxs-lookup"><span data-stu-id="96d1b-345">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="96d1b-346">Да</span><span class="sxs-lookup"><span data-stu-id="96d1b-346">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96d1b-347">Да</span><span class="sxs-lookup"><span data-stu-id="96d1b-347">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
