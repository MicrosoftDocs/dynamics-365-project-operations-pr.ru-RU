---
title: Обзор строк контракта на основе проекта
description: Эта тема предоставляет информацию о работе со строками контракта на основе проекта.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 824fdd54d7b513b49afd1a6d76d3387df81418e2
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858174"
---
# <a name="project-based-contract-lines-overview"></a><span data-ttu-id="a24b8-103">Обзор строк контракта на основе проекта</span><span class="sxs-lookup"><span data-stu-id="a24b8-103">Project-based contract lines overview</span></span>

<span data-ttu-id="a24b8-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="a24b8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a24b8-105">Строки контрактов на основе проектов в Dynamics 365 Project Operations предназначены для хранения соглашений об оценке и выставления счетов для определенных компонентов проектной работы по соглашению.</span><span class="sxs-lookup"><span data-stu-id="a24b8-105">Project-based contract lines in Dynamics 365 Project Operations are designed to hold the estimate and billing agreements for specific components of project work on an engagement.</span></span> <span data-ttu-id="a24b8-106">Структура строки контракта на основе проекта расширена для оценок проекта и сценариев выставления счетов за счет следующих концепций:</span><span class="sxs-lookup"><span data-stu-id="a24b8-106">The structure of a project–based contract line is extended for project estimates and billing scenarios with the following concepts:</span></span>

- <span data-ttu-id="a24b8-107">Метод выставления счета</span><span class="sxs-lookup"><span data-stu-id="a24b8-107">Billing method</span></span>
- <span data-ttu-id="a24b8-108">Сопоставление проектов и задач</span><span class="sxs-lookup"><span data-stu-id="a24b8-108">Project and task mapping</span></span>
- <span data-ttu-id="a24b8-109">Включенные классы транзакций</span><span class="sxs-lookup"><span data-stu-id="a24b8-109">Included transaction classes</span></span>
- <span data-ttu-id="a24b8-110">Максимальный лимит</span><span class="sxs-lookup"><span data-stu-id="a24b8-110">Not-to-exceed limit</span></span>
- <span data-ttu-id="a24b8-111">Настройка возможности оплаты</span><span class="sxs-lookup"><span data-stu-id="a24b8-111">Chargeability setup</span></span>
- <span data-ttu-id="a24b8-112">Оценки с использованием сведений о строке контракта</span><span class="sxs-lookup"><span data-stu-id="a24b8-112">Estimates using contract line details</span></span>
- <span data-ttu-id="a24b8-113">Клиенты строки контракта</span><span class="sxs-lookup"><span data-stu-id="a24b8-113">Contract line customers</span></span>

<span data-ttu-id="a24b8-114">Следующая таблица включает поля на вкладке **Общие** строк контрактов на основе проекта, которая помогает создать основу для подробной оценки снизу вверх и выставления счетов за работу на основе проекта.</span><span class="sxs-lookup"><span data-stu-id="a24b8-114">The following table includes the fields on the **General** tab of project–based contract lines that help set up the basis for a detailed, ground–up estimate and billing arrangements for project–based work.</span></span>

| <span data-ttu-id="a24b8-115">Поле</span><span class="sxs-lookup"><span data-stu-id="a24b8-115">Field</span></span> | <span data-ttu-id="a24b8-116">Описание:</span><span class="sxs-lookup"><span data-stu-id="a24b8-116">Description</span></span> | <span data-ttu-id="a24b8-117">Воздействие на последующие элементы</span><span class="sxs-lookup"><span data-stu-id="a24b8-117">Downstream impact</span></span> |
| --- | --- | --- |
| <span data-ttu-id="a24b8-118">**Название**</span><span class="sxs-lookup"><span data-stu-id="a24b8-118">**Name**</span></span> | <span data-ttu-id="a24b8-119">Имя строки контракта.</span><span class="sxs-lookup"><span data-stu-id="a24b8-119">Name of the contract line.</span></span> <span data-ttu-id="a24b8-120">Это идентифицирует дискретный компонент контракта, который оценивается.</span><span class="sxs-lookup"><span data-stu-id="a24b8-120">This identifies the discrete component of the contract that is being estimated.</span></span> <span data-ttu-id="a24b8-121">Для контракта по проекту, созданного на основе предложения с расценками, это значение копируется из соответствующего значения строки предложения с расценками по проекту.</span><span class="sxs-lookup"><span data-stu-id="a24b8-121">For a project contract created from a quote, this value is copied from a corresponding value of the project-based quote line.</span></span> | <span data-ttu-id="a24b8-122">Имя копируется в строку счета по проекту, которая создается из этой строки контракта при создании счета.</span><span class="sxs-lookup"><span data-stu-id="a24b8-122">The name copied over to the project invoice line that is created from this contract line when the invoice is created.</span></span> |
| <span data-ttu-id="a24b8-123">**Метод выставления счета**</span><span class="sxs-lookup"><span data-stu-id="a24b8-123">**Billing Method**</span></span> | <span data-ttu-id="a24b8-124">В контракте по проекту, созданному на основе предложения с расценками, это значение копируется из соответствующего поля строки предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="a24b8-124">On a project contract created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="a24b8-125">Это набор параметров, который представляет две основные модели заключения контрактов, поддерживаемые Project Operations:</span><span class="sxs-lookup"><span data-stu-id="a24b8-125">This is an option set that represents the two main contracting models supported by Project Operations:</span></span></br><span data-ttu-id="a24b8-126">- **Фиксированная цена**</span><span class="sxs-lookup"><span data-stu-id="a24b8-126">- **Fixed Price**</span></span></br><span data-ttu-id="a24b8-127">- **Время и материал**</span><span class="sxs-lookup"><span data-stu-id="a24b8-127">- **Time and Material**</span></span> | <span data-ttu-id="a24b8-128">Фактическая транзакция будет обработана в зависимости от метода выставления счетов в указанной строке контракта.</span><span class="sxs-lookup"><span data-stu-id="a24b8-128">Based on the billing method of the referenced contract line, the actual transaction will be processed.</span></span> <span data-ttu-id="a24b8-129">Если в строке контракта, на которую ссылается фактическое значение, указан метод выставления счетов по времени и материалам, создаются записи о затратах и фактических продажах без выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="a24b8-129">If the contract line referenced by the actual has a time and material billing method, cost and unbilled sales actual records are created.</span></span> <span data-ttu-id="a24b8-130">Если в строке контракта, на которую ссылается фактическое значение, используется метод расчета с фиксированной ценой, создается только фактическая стоимость.</span><span class="sxs-lookup"><span data-stu-id="a24b8-130">If the contract line referenced by the actual has a fixed price billing method, only a cost actual is created.</span></span> |
| <span data-ttu-id="a24b8-131">**Project**</span><span class="sxs-lookup"><span data-stu-id="a24b8-131">**Project**</span></span> | <span data-ttu-id="a24b8-132">Используйте это поле, чтобы определить проект, который будет использоваться для выполнения работы по данному заданию.</span><span class="sxs-lookup"><span data-stu-id="a24b8-132">Use this field to identify the project that will be used to deliver the work on this engagement.</span></span> | <span data-ttu-id="a24b8-133">Это значение будет использоваться вместе с **Включенные задачи** и **Включенные классы транзакций** для разрешения ссылки на строку контракта в записи строки фактических данных или оценки.</span><span class="sxs-lookup"><span data-stu-id="a24b8-133">This value will be used in conjunction with **Included Tasks** and **Included Transaction Classes** to resolve the contract line reference on an actual or estimate line record.</span></span> |
| <span data-ttu-id="a24b8-134">**Включенные задачи**</span><span class="sxs-lookup"><span data-stu-id="a24b8-134">**Included Tasks**</span></span> | <span data-ttu-id="a24b8-135">Указывает, включает ли эта строка контракта все задачи проекта для выбранного проекта или только подмножество задач.</span><span class="sxs-lookup"><span data-stu-id="a24b8-135">Indicates if this contract line includes all project tasks for the selected project or only a subset of the tasks.</span></span> <span data-ttu-id="a24b8-136">Это набор параметров, который имеет следующие возможные значения:</span><span class="sxs-lookup"><span data-stu-id="a24b8-136">This is an option set that has the following possible values:</span></span></br><span data-ttu-id="a24b8-137">- **Все задачи проекта**</span><span class="sxs-lookup"><span data-stu-id="a24b8-137">- **All Project Tasks**</span></span></br><span data-ttu-id="a24b8-138">- **Только выбранные задачи проекта**.</span><span class="sxs-lookup"><span data-stu-id="a24b8-138">- **Selected Project Tasks Only**.</span></span> <span data-ttu-id="a24b8-139">Пустое значение в этом поле равно выбору **Все задачи проекта**.</span><span class="sxs-lookup"><span data-stu-id="a24b8-139">A blank value in this field is equal to selecting **All Project Tasks**.</span></span> | <span data-ttu-id="a24b8-140">Если выбран вариант **Только выбранные задачи**, вы можете выбрать определенные задачи и связать их с этой строкой контракта на вкладке **Настройка выставления счетов по задачам** на странице **Проект**.</span><span class="sxs-lookup"><span data-stu-id="a24b8-140">If **Selected Tasks Only** is selected, you can select specific tasks and associate them to this contract line on the **Task Billing Setup** tab on the **Project** page.</span></span> <span data-ttu-id="a24b8-141">Значение будет использоваться вместе с классами **Проект** и **Включенные транзакции** для разрешения ссылки на строку контракта в записи строки фактических данных или оценки.</span><span class="sxs-lookup"><span data-stu-id="a24b8-141">The value will be used in conjunction with **Project** and **Included Transaction** classes to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="a24b8-142">**Включить время**</span><span class="sxs-lookup"><span data-stu-id="a24b8-142">**Include Time**</span></span> | <span data-ttu-id="a24b8-143">Значение **Да**/**Нет** указывает, будут ли включены в эту строку контракта транзакции времени или затраты на оплату труда по выбранному проекту.</span><span class="sxs-lookup"><span data-stu-id="a24b8-143">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="a24b8-144">Значение **Нет** указывает, что операции по времени или затраты на рабочую силу не будут включены в эту строку контракта.</span><span class="sxs-lookup"><span data-stu-id="a24b8-144">A **No** value indicates that the time transactions or labor cost will not be included on this contract line.</span></span> <span data-ttu-id="a24b8-145">Значение **Да** указывает, что они будут.</span><span class="sxs-lookup"><span data-stu-id="a24b8-145">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="a24b8-146">Это значение используется вместе с проектом для разрешения ссылки на строку контракта в записи строки фактических данных или оценки.</span><span class="sxs-lookup"><span data-stu-id="a24b8-146">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="a24b8-147">**Включить расход**</span><span class="sxs-lookup"><span data-stu-id="a24b8-147">**Include Expense**</span></span> | <span data-ttu-id="a24b8-148">Значение **Да**/**Нет** указывает, будет ли включена в эту строку контракта стоимость расходов по выбранному проекту.</span><span class="sxs-lookup"><span data-stu-id="a24b8-148">A **Yes**/**No** value indicates if expense costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="a24b8-149">Значение **Нет** указывает, что стоимость расходов не будут включена в эту строку контракта.</span><span class="sxs-lookup"><span data-stu-id="a24b8-149">A **No** value indicates that the expense cost will not be included on this contract line.</span></span> <span data-ttu-id="a24b8-150">Значение **Да** указывает, что будет.</span><span class="sxs-lookup"><span data-stu-id="a24b8-150">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="a24b8-151">Это значение используется вместе с проектом для разрешения ссылки на строку контракта в записи строки фактических данных или оценки.</span><span class="sxs-lookup"><span data-stu-id="a24b8-151">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="a24b8-152">**Включить материалы**</span><span class="sxs-lookup"><span data-stu-id="a24b8-152">**Include Materials**</span></span> | <span data-ttu-id="a24b8-153">Значение **Да**/**Нет** указывает, будет ли включена в эту строку контракта стоимость материалов по выбранному проекту.</span><span class="sxs-lookup"><span data-stu-id="a24b8-153">A **Yes**/**No** value indicates if material costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="a24b8-154">Значение **Нет** указывает, что в эту строку контракта стоимость материалов по выбранному проекту не будет включена.</span><span class="sxs-lookup"><span data-stu-id="a24b8-154">A **No** value indicates that the material costs will not be included on this contract line.</span></span> <span data-ttu-id="a24b8-155">Значение **Да** указывает, что будет.</span><span class="sxs-lookup"><span data-stu-id="a24b8-155">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="a24b8-156">Это значение используется вместе с проектом для разрешения ссылки на строку контракта в записи строки фактических данных или оценки.</span><span class="sxs-lookup"><span data-stu-id="a24b8-156">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="a24b8-157">**Включить сбор**</span><span class="sxs-lookup"><span data-stu-id="a24b8-157">**Include Fee**</span></span> | <span data-ttu-id="a24b8-158">Значение **Да**/**Нет** указывает, будут ли включены в эту строку контракта сборы по выбранному проекту.</span><span class="sxs-lookup"><span data-stu-id="a24b8-158">A **Yes**/**No** value indicates if fees on the selected project will be included on this contract line.</span></span> <span data-ttu-id="a24b8-159">Значение **Нет** указывает, что сборы не будут включены в эту строку контракта.</span><span class="sxs-lookup"><span data-stu-id="a24b8-159">A **No** value indicates that the fees will not be included on this contract line.</span></span> <span data-ttu-id="a24b8-160">Значение **Да** указывает, что они будут.</span><span class="sxs-lookup"><span data-stu-id="a24b8-160">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="a24b8-161">Это значение используется вместе с проектом для разрешения ссылки на строку контракта в записи строки фактических данных или оценки.</span><span class="sxs-lookup"><span data-stu-id="a24b8-161">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="a24b8-162">**Сумма по контракту**</span><span class="sxs-lookup"><span data-stu-id="a24b8-162">**Contracted Amount**</span></span> | <span data-ttu-id="a24b8-163">В строке контракта с фиксированной ценой это согласованная сумма, по которой заказчику будет выставлен счет за все компоненты работы, связанные с этой строкой контракта.</span><span class="sxs-lookup"><span data-stu-id="a24b8-163">On a fixed price contract line, this amount is the agreed-on value that will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="a24b8-164">В строке контракта по времени и материалам эта сумма является оценочным значением, по которому будет выставлен счет клиенту за все компоненты работы, связанные с этой строкой контракта.</span><span class="sxs-lookup"><span data-stu-id="a24b8-164">On a time and material contract line, this amount is an estimated value of what will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="a24b8-165">В контракте по проекту, созданному на основе предложения с расценками, это значение копируется из соответствующего поля строки предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="a24b8-165">On a project contract that is created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="a24b8-166">Если в строке контракта на основе проекта есть детали строки, это поле заблокировано для редактирования и суммируется из суммы в деталях строки контракта.</span><span class="sxs-lookup"><span data-stu-id="a24b8-166">When a project–based contract line has line details, this field is locked for editing and is summarized from the amount on the contract line details.</span></span> | <span data-ttu-id="a24b8-167">Если в строке контракта есть сведения о строке, это значение можно изменить, изменив суммы в деталях строки.</span><span class="sxs-lookup"><span data-stu-id="a24b8-167">When the contract line has line details, this value can be modified by changing the amounts on the line details.</span></span> <span data-ttu-id="a24b8-168">В строке контракта с фиксированной ценой это значение используется для создания суммы до налогообложения для периодических этапов выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="a24b8-168">On a fixed price contract line, this value is used to generate the amount before tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="a24b8-169">**Ожидаемый налог**</span><span class="sxs-lookup"><span data-stu-id="a24b8-169">**Estimated Tax**</span></span> | <span data-ttu-id="a24b8-170">Пользователь может редактировать это поле, чтобы ввести расчетную сумму налога в строку контракта.</span><span class="sxs-lookup"><span data-stu-id="a24b8-170">The user can edit this field to input the estimated tax amount on the contract line.</span></span> <span data-ttu-id="a24b8-171">Если в строке контракта на основе проекта есть детали строки, это поле заблокировано для редактирования и суммируется из суммы налога в деталях строки контракта.</span><span class="sxs-lookup"><span data-stu-id="a24b8-171">When a project–based contract line has line details, this field is locked for editing and is summarized from the tax amount on the contract line details.</span></span> | <span data-ttu-id="a24b8-172">Если в строке контракта есть сведения о строке, это значение можно изменить, изменив суммы налога в деталях строки.</span><span class="sxs-lookup"><span data-stu-id="a24b8-172">When the contract line has line details, this value can be modified by changing the tax amounts on the line details.</span></span> <span data-ttu-id="a24b8-173">В строке контракта с фиксированной ценой это значение используется для создания налога для периодических этапов выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="a24b8-173">On a fixed price contract line, this value is used to generate the tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="a24b8-174">**Сумма по контракту после налогообложения**</span><span class="sxs-lookup"><span data-stu-id="a24b8-174">**Contracted Amount after Tax**</span></span> | <span data-ttu-id="a24b8-175">Сумма по строке контракта после налогообложения.</span><span class="sxs-lookup"><span data-stu-id="a24b8-175">The contract line amount after tax.</span></span> <span data-ttu-id="a24b8-176">Это поле доступно только для чтения и рассчитывается как **Сумма контракта + Налог**.</span><span class="sxs-lookup"><span data-stu-id="a24b8-176">This field is read only and is calculated as **Contracted Amount + Tax**.</span></span> | <span data-ttu-id="a24b8-177">В строке контракта с фиксированной ценой это значение используется для создания периодических этапов выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="a24b8-177">On a fixed price contract line, this value is used to generate periodic billing milestones.</span></span> |
| <span data-ttu-id="a24b8-178">**Максимальный лимит**</span><span class="sxs-lookup"><span data-stu-id="a24b8-178">**Not-to-Exceed Limit**</span></span> | <span data-ttu-id="a24b8-179">Пользователь может редактировать это поле, и оно доступно только для строк контракта на основе проекта, в которых указан метод выставления счетов, заданный как время и материалы.</span><span class="sxs-lookup"><span data-stu-id="a24b8-179">The user can edit this field and it is only available on project-based contract lines that have the billing method set as time and material.</span></span> | <span data-ttu-id="a24b8-180">Пользователь может редактировать это поле.</span><span class="sxs-lookup"><span data-stu-id="a24b8-180">The user can edit this field.</span></span> <span data-ttu-id="a24b8-181">Когда фактические данные для времени и материалов ссылаются на эту строку контракта в отношении времени и материалов, сумма фактических расходов оценивается по отношению к максимальному лимиту в этой строке контракта.</span><span class="sxs-lookup"><span data-stu-id="a24b8-181">When an actual for time and material references this contract line for time and material, the amount on the actual is evaluated against the not-to-exceed limit on the contract line.</span></span> <span data-ttu-id="a24b8-182">Эта оценка завершается после учета уже потраченных и подтвержденных сумм.</span><span class="sxs-lookup"><span data-stu-id="a24b8-182">This evaluation is completed after  the already spent and committed amounts are accounted for.</span></span> |
| <span data-ttu-id="a24b8-183">**Бюджет клиента**</span><span class="sxs-lookup"><span data-stu-id="a24b8-183">**Customer Budget**</span></span> | <span data-ttu-id="a24b8-184">Это поле доступно для редактирования и копируется из соответствующего поля строки предложения с расценками, если контракт создан из предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="a24b8-184">This field is editable and is copied from the corresponding field on the quote line if the contract was created from a quote.</span></span> | <span data-ttu-id="a24b8-185">Это поле используется только для информации и не имеет никакого значения для последующей обработки.</span><span class="sxs-lookup"><span data-stu-id="a24b8-185">This field is only used for information and does not have any downstream significance.</span></span> |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a><span data-ttu-id="a24b8-186">Правила проверки для параметров на вкладке "Общие" строк контракта на основе проекта</span><span class="sxs-lookup"><span data-stu-id="a24b8-186">Validation rules for the options on the General tab of project-based contract lines</span></span>

<span data-ttu-id="a24b8-187">Правило 1. Если поле **Включенные задачи** пустое или установлено на **Все задачи проекта**, все задачи проекта включены в строку договора.</span><span class="sxs-lookup"><span data-stu-id="a24b8-187">Rule 1: If the **Included Tasks** field is blank or set to **All Project Tasks**, all tasks of the project are included on the contract line.</span></span>

<span data-ttu-id="a24b8-188">Правило 2. Когда поле **Включенные задачи** пустое или явно установлено на **Все задачи проекта**, проект и определенный класс транзакций могут быть включены только в одну строку контракта на основе проекта для контракта.</span><span class="sxs-lookup"><span data-stu-id="a24b8-188">Rule 2: When the **Included Tasks** field is blank or explicitly set to **All Project Tasks**, a project and a certain transaction class can only be included on one project-based contract line of a contract.</span></span>

<span data-ttu-id="a24b8-189">Правило 3. Когда поле **Включенные задачи** пустое или явно установлено на **Только выбранные задачи проекта**, проект и определенный класс транзакций могут быть включены в несколько строк контракта на основе проекта для контракта.</span><span class="sxs-lookup"><span data-stu-id="a24b8-189">Rule 3: When the **Included Tasks** field is set to **Selected Project Tasks Only**, a project and a certain transaction class can be included on multiple project-based contract lines of a contract.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p><span data-ttu-id="a24b8-190">
                    <strong>Контракт</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a24b8-190">
                    <strong>Contract</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="a24b8-191">
                    <strong>Строка контракта</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a24b8-191">
                    <strong>Contract line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="a24b8-192">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a24b8-192">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="67" valign="top">
                <p><span data-ttu-id="a24b8-193">
                    <strong>Включенные задачи</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a24b8-193">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="a24b8-194">
                    <strong>Включить время</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a24b8-194">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="a24b8-195">
                    <strong>Включить расход</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a24b8-195">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="a24b8-196">
                    <strong>Включить материалы</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a24b8-196">
                    <strong>Include Materials</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="a24b8-197">
                    <strong>Включить</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a24b8-197">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="a24b8-198">
                    <strong>Сбор</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a24b8-198">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="53" valign="top">
                <p><span data-ttu-id="a24b8-199">
                    <strong>Действителен/Недействителен</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a24b8-199">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="250" valign="top">
                <p><span data-ttu-id="a24b8-200">
                    <strong>Причина</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a24b8-200">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="a24b8-201">C1</span><span class="sxs-lookup"><span data-stu-id="a24b8-201">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a24b8-202">CL1</span><span class="sxs-lookup"><span data-stu-id="a24b8-202">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a24b8-203">П1</span><span class="sxs-lookup"><span data-stu-id="a24b8-203">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="a24b8-204">Пусто</span><span class="sxs-lookup"><span data-stu-id="a24b8-204">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a24b8-205">Да</span><span class="sxs-lookup"><span data-stu-id="a24b8-205">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a24b8-206">Да</span><span class="sxs-lookup"><span data-stu-id="a24b8-206">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a24b8-207">Да</span><span class="sxs-lookup"><span data-stu-id="a24b8-207">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a24b8-208">Да</span><span class="sxs-lookup"><span data-stu-id="a24b8-208">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a24b8-209">Недействительный</span><span class="sxs-lookup"><span data-stu-id="a24b8-209">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a24b8-210">Нарушение правила №2.</span><span class="sxs-lookup"><span data-stu-id="a24b8-210">Violation of Rule #2.</span></span> <span data-ttu-id="a24b8-211">Время, расходы, материалы и сборы по проекту P1 включены в строки контракта CL1 и CL2.</span><span class="sxs-lookup"><span data-stu-id="a24b8-211">Time, Expense, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="a24b8-212">C1</span><span class="sxs-lookup"><span data-stu-id="a24b8-212">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a24b8-213">CL2</span><span class="sxs-lookup"><span data-stu-id="a24b8-213">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a24b8-214">П1</span><span class="sxs-lookup"><span data-stu-id="a24b8-214">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="a24b8-215">Пусто</span><span class="sxs-lookup"><span data-stu-id="a24b8-215">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a24b8-216">Да</span><span class="sxs-lookup"><span data-stu-id="a24b8-216">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a24b8-217">Да</span><span class="sxs-lookup"><span data-stu-id="a24b8-217">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a24b8-218">Да</span><span class="sxs-lookup"><span data-stu-id="a24b8-218">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a24b8-219">Да</span><span class="sxs-lookup"><span data-stu-id="a24b8-219">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="a24b8-220">C1</span><span class="sxs-lookup"><span data-stu-id="a24b8-220">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a24b8-221">CL1</span><span class="sxs-lookup"><span data-stu-id="a24b8-221">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a24b8-222">П1</span><span class="sxs-lookup"><span data-stu-id="a24b8-222">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="a24b8-223">Пусто</span><span class="sxs-lookup"><span data-stu-id="a24b8-223">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a24b8-224">Да</span><span class="sxs-lookup"><span data-stu-id="a24b8-224">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a24b8-225">No</span><span class="sxs-lookup"><span data-stu-id="a24b8-225">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a24b8-226">Да</span><span class="sxs-lookup"><span data-stu-id="a24b8-226">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a24b8-227">Да</span><span class="sxs-lookup"><span data-stu-id="a24b8-227">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a24b8-228">Недействительный</span><span class="sxs-lookup"><span data-stu-id="a24b8-228">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a24b8-229">Нарушение правила №2.</span><span class="sxs-lookup"><span data-stu-id="a24b8-229">Violation of Rule #2.</span></span> <span data-ttu-id="a24b8-230">Время, материалы и сборы по проекту P1 включены в строки контракта CL1 и CL2.</span><span class="sxs-lookup"><span data-stu-id="a24b8-230">Time, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="a24b8-231">C1</span><span class="sxs-lookup"><span data-stu-id="a24b8-231">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a24b8-232">CL2</span><span class="sxs-lookup"><span data-stu-id="a24b8-232">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a24b8-233">П1</span><span class="sxs-lookup"><span data-stu-id="a24b8-233">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="a24b8-234">Пусто</span><span class="sxs-lookup"><span data-stu-id="a24b8-234">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a24b8-235">Да</span><span class="sxs-lookup"><span data-stu-id="a24b8-235">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a24b8-236">Да</span><span class="sxs-lookup"><span data-stu-id="a24b8-236">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a24b8-237">Да</span><span class="sxs-lookup"><span data-stu-id="a24b8-237">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a24b8-238">Да</span><span class="sxs-lookup"><span data-stu-id="a24b8-238">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="a24b8-239">C1</span><span class="sxs-lookup"><span data-stu-id="a24b8-239">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a24b8-240">CL1</span><span class="sxs-lookup"><span data-stu-id="a24b8-240">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a24b8-241">П1</span><span class="sxs-lookup"><span data-stu-id="a24b8-241">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="a24b8-242">Пусто</span><span class="sxs-lookup"><span data-stu-id="a24b8-242">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a24b8-243">Да</span><span class="sxs-lookup"><span data-stu-id="a24b8-243">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a24b8-244">No</span><span class="sxs-lookup"><span data-stu-id="a24b8-244">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a24b8-245">Да</span><span class="sxs-lookup"><span data-stu-id="a24b8-245">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a24b8-246">Да</span><span class="sxs-lookup"><span data-stu-id="a24b8-246">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a24b8-247">Действителен</span><span class="sxs-lookup"><span data-stu-id="a24b8-247">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a24b8-248">Время, материалы и сборы по проекту P1 включены в CL1.</span><span class="sxs-lookup"><span data-stu-id="a24b8-248">Time, Materials, and Fees on P1 project are included on CL1.</span></span>
                </p>
                <ul>
                    <li>
<span data-ttu-id="a24b8-249">Расходы по проекту P1 включены в CL2.</span><span class="sxs-lookup"><span data-stu-id="a24b8-249">Expense on P1 project is included on CL2.</span></span>
                    </li>
                </ul>
                <p>
<span data-ttu-id="a24b8-250">Нет перекрытия того, что включено в каждую строку контракта и, следовательно, все правильно.</span><span class="sxs-lookup"><span data-stu-id="a24b8-250">No overlap in what is being included on each Contract line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="a24b8-251">C1</span><span class="sxs-lookup"><span data-stu-id="a24b8-251">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a24b8-252">CL2</span><span class="sxs-lookup"><span data-stu-id="a24b8-252">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a24b8-253">П1</span><span class="sxs-lookup"><span data-stu-id="a24b8-253">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="a24b8-254">Пусто</span><span class="sxs-lookup"><span data-stu-id="a24b8-254">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a24b8-255">No</span><span class="sxs-lookup"><span data-stu-id="a24b8-255">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a24b8-256">Да</span><span class="sxs-lookup"><span data-stu-id="a24b8-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a24b8-257">No</span><span class="sxs-lookup"><span data-stu-id="a24b8-257">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a24b8-258">No</span><span class="sxs-lookup"><span data-stu-id="a24b8-258">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="a24b8-259">C1</span><span class="sxs-lookup"><span data-stu-id="a24b8-259">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a24b8-260">CL1</span><span class="sxs-lookup"><span data-stu-id="a24b8-260">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a24b8-261">П1</span><span class="sxs-lookup"><span data-stu-id="a24b8-261">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="a24b8-262">Только выбранные задачи</span><span class="sxs-lookup"><span data-stu-id="a24b8-262">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a24b8-263">Да</span><span class="sxs-lookup"><span data-stu-id="a24b8-263">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a24b8-264">Да</span><span class="sxs-lookup"><span data-stu-id="a24b8-264">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a24b8-265">Да</span><span class="sxs-lookup"><span data-stu-id="a24b8-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a24b8-266">Да</span><span class="sxs-lookup"><span data-stu-id="a24b8-266">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a24b8-267">Недействительный</span><span class="sxs-lookup"><span data-stu-id="a24b8-267">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a24b8-268">Нарушение правила № 2</span><span class="sxs-lookup"><span data-stu-id="a24b8-268">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="a24b8-269">C1 включает время, материалы, расходы и сборы по подмножеству задач по проекту P1.</span><span class="sxs-lookup"><span data-stu-id="a24b8-269">C1 includes Time, Materials, Expenses and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="a24b8-270">CL2 включает время, материалы, расходы и сборы для всего проекта P1 и, следовательно, частично совпадает с тем, что включено в C1.</span><span class="sxs-lookup"><span data-stu-id="a24b8-270">CL2 includes Time, Materials, Expenses and Fees for the whole project P1 and therefore overlaps with what is included on C1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="a24b8-271">C1</span><span class="sxs-lookup"><span data-stu-id="a24b8-271">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a24b8-272">CL2</span><span class="sxs-lookup"><span data-stu-id="a24b8-272">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a24b8-273">П1</span><span class="sxs-lookup"><span data-stu-id="a24b8-273">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="a24b8-274">Пусто</span><span class="sxs-lookup"><span data-stu-id="a24b8-274">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a24b8-275">Да</span><span class="sxs-lookup"><span data-stu-id="a24b8-275">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a24b8-276">Да</span><span class="sxs-lookup"><span data-stu-id="a24b8-276">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a24b8-277">Да</span><span class="sxs-lookup"><span data-stu-id="a24b8-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a24b8-278">Да</span><span class="sxs-lookup"><span data-stu-id="a24b8-278">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="a24b8-279">C1</span><span class="sxs-lookup"><span data-stu-id="a24b8-279">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a24b8-280">CL1</span><span class="sxs-lookup"><span data-stu-id="a24b8-280">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a24b8-281">П1</span><span class="sxs-lookup"><span data-stu-id="a24b8-281">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="a24b8-282">Только выбранные задачи</span><span class="sxs-lookup"><span data-stu-id="a24b8-282">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a24b8-283">Да</span><span class="sxs-lookup"><span data-stu-id="a24b8-283">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a24b8-284">Да</span><span class="sxs-lookup"><span data-stu-id="a24b8-284">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a24b8-285">Да</span><span class="sxs-lookup"><span data-stu-id="a24b8-285">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a24b8-286">Да</span><span class="sxs-lookup"><span data-stu-id="a24b8-286">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a24b8-287">Действителен</span><span class="sxs-lookup"><span data-stu-id="a24b8-287">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a24b8-288">Согласно правилу № 3</span><span class="sxs-lookup"><span data-stu-id="a24b8-288">Per Rule #3</span></span> </p>
                <p>
<span data-ttu-id="a24b8-289">C1 включает время, расходы, материалы и сборы по подмножеству задач по проекту P1.</span><span class="sxs-lookup"><span data-stu-id="a24b8-289">C1 includes Time, Expenses, Materials, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="a24b8-290">CL2 включает время, расходы, материалы и сборы для подмножества задач по проекту P1.</span><span class="sxs-lookup"><span data-stu-id="a24b8-290">CL2 includes Time, Expenses, Materials, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="a24b8-291">Единственная дополнительная проверка связана с тем, что подмножество задач в CL1 отличается от подмножества задач в CL2, чтобы гарантировать, что там нет перекрытий.</span><span class="sxs-lookup"><span data-stu-id="a24b8-291">The only additional validation is around the subset of tasks on CL1 is different from the subset of tasks on CL2 to ensure that there are no overlaps there.</span></span> <span data-ttu-id="a24b8-292">Это выполняется системой, когда задачи связаны.</span><span class="sxs-lookup"><span data-stu-id="a24b8-292">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="a24b8-293">C1</span><span class="sxs-lookup"><span data-stu-id="a24b8-293">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a24b8-294">CL2</span><span class="sxs-lookup"><span data-stu-id="a24b8-294">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a24b8-295">П1</span><span class="sxs-lookup"><span data-stu-id="a24b8-295">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="a24b8-296">Только выбранные задачи</span><span class="sxs-lookup"><span data-stu-id="a24b8-296">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a24b8-297">Да</span><span class="sxs-lookup"><span data-stu-id="a24b8-297">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a24b8-298">Да</span><span class="sxs-lookup"><span data-stu-id="a24b8-298">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a24b8-299">Да</span><span class="sxs-lookup"><span data-stu-id="a24b8-299">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a24b8-300">Да</span><span class="sxs-lookup"><span data-stu-id="a24b8-300">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]