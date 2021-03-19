---
title: Настройка управления расходами
description: В этой статье описываются соображения и решения, которые необходимо принять в процессе планирования перед настройкой управления расходами в Microsoft Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 74a8435464c8573ca831b7886f00c2695fd29827
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271369"
---
# <a name="configure-expense-management"></a><span data-ttu-id="05bd7-103">Настройка управления расходами</span><span class="sxs-lookup"><span data-stu-id="05bd7-103">Configure expense management</span></span>

<span data-ttu-id="05bd7-104">В этой теме описываются соображения и решения, которые необходимо принять в процессе планирования перед настройкой управления расходами.</span><span class="sxs-lookup"><span data-stu-id="05bd7-104">This topic describes the considerations and the decisions that you must make during the planning process before you configure Expense management.</span></span> <span data-ttu-id="05bd7-105">В управлении расходами вы можете хранить информацию о способах оплаты, заявках на командировки, отчетах о расходах, политиках и т. д.</span><span class="sxs-lookup"><span data-stu-id="05bd7-105">In Expense management, you can store information about payment methods, travel requisitions, expense reports, policies, and so on.</span></span>

<span data-ttu-id="05bd7-106">Поскольку многие решения, которые вы принимаете при планировании конфигурации для управления расходами, основаны на иерархии и финансовой структуре вашей организации, вы должны ссылаться на документы планирования для этих областей.</span><span class="sxs-lookup"><span data-stu-id="05bd7-106">Because many of the decisions that you make when you plan your configuration for Expense management are based on your organization’s hierarchy and financial structure, you must refer to the planning documents for those areas.</span></span>

## <a name="intercompany-expenses"></a><span data-ttu-id="05bd7-107">Внутрихолдинговые расходы</span><span class="sxs-lookup"><span data-stu-id="05bd7-107">Intercompany expenses</span></span>

<span data-ttu-id="05bd7-108">Когда вы включаете внутрихолдинговые расходы, вы разрешаете юридическим лицам и сотрудникам нести расходы от имени другого юридического лица и получать оплату от юридического лица-нанимателя в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="05bd7-108">When you enable intercompany expenses, you allow legal entities and employees to incur expenses on behalf of another legal entity, and collect payment from the legal entity of employment within your organization.</span></span> <span data-ttu-id="05bd7-109">Например, сотрудник юридического лица A завершает проект для юридического лица B, и проект несет командировочные расходы.</span><span class="sxs-lookup"><span data-stu-id="05bd7-109">For example, an employee in legal entity A completes a project for legal entity B, and the project incurs travel related expenses.</span></span> <span data-ttu-id="05bd7-110">Если внутрихолдинговые расходы включены, сотрудник может затем подать отчет о расходах, в котором расходы будут разнесены на юридическое лицо B, и затем расходы должны быть оплачены юридическим лицом A. Если в вашей организации нет нескольких юридических лиц, вам не требуется включать внутрихолдинговые расходы.</span><span class="sxs-lookup"><span data-stu-id="05bd7-110">If intercompany expenses are enabled, the employee can then file an expense report that will post the expense to legal entity B, and the expense must then be paid by legal entity A. If your organization doesn’t have multiple legal entities, you don’t have to enable intercompany expenses.</span></span>

<span data-ttu-id="05bd7-111">**Решение:** вы хотите включить внутрихолдинговые расходы?</span><span class="sxs-lookup"><span data-stu-id="05bd7-111">**Decision:** Do you want to enable intercompany expenses?</span></span>

## <a name="financial-management"></a><span data-ttu-id="05bd7-112">Финансовый менеджмент</span><span class="sxs-lookup"><span data-stu-id="05bd7-112">Financial management</span></span>

<span data-ttu-id="05bd7-113">Управление расходами тесно интегрировано с финансовым управлением вашей организации.</span><span class="sxs-lookup"><span data-stu-id="05bd7-113">Expense management is tightly integrated with the financial management of your organization.</span></span> <span data-ttu-id="05bd7-114">Большая часть вашей конфигурации для управления расходами будет основана на решениях, которые вы приняли в отношении финансов вашей организации.</span><span class="sxs-lookup"><span data-stu-id="05bd7-114">Lots of your configuration for Expense management will be based on the decisions that you’ve made about your organization’s finances.</span></span> <span data-ttu-id="05bd7-115">В следующих разделах описываются различные области, требующие планирования и принятия решений, основанные на финансовых решениях вашей организации и рекомендациях вашей рабочей группы руководства.</span><span class="sxs-lookup"><span data-stu-id="05bd7-115">The following sections describe the various areas that require planning and decisions, based on your organization’s financial decisions and guidance from your leadership team.</span></span>

### <a name="per-diems"></a><span data-ttu-id="05bd7-116">Суточные</span><span class="sxs-lookup"><span data-stu-id="05bd7-116">Per diems</span></span>

<span data-ttu-id="05bd7-117">Вы должны определить суточные, которые предоставляет ваша организация сотрудникам.</span><span class="sxs-lookup"><span data-stu-id="05bd7-117">You must define the employee per diems that your organization provides.</span></span> <span data-ttu-id="05bd7-118">Поскольку суточные обычно используются для покрытия таких расходов, как питание, проживание и другие непредвиденные расходы, вы можете создать правила для суточных, которые предлагает ваша организация.</span><span class="sxs-lookup"><span data-stu-id="05bd7-118">Because per diems are typically used to cover expenses such as meals, lodging, and other incidental expenses, you can create rules for the per diem allowances that your organization offers.</span></span> <span data-ttu-id="05bd7-119">Ставки суточных могут зависеть от времени года, места поездки или и того, и другого.</span><span class="sxs-lookup"><span data-stu-id="05bd7-119">per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="05bd7-120">При определении правила суточных вы можете указать, что процент суточных будет удерживаться, если работник получает бесплатное питание или услуги.</span><span class="sxs-lookup"><span data-stu-id="05bd7-120">When you define a per diem rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="05bd7-121">Вы также можете определить уровни ставок суточных, чтобы задать минимальное и максимальное количество часов, за которые суточные могут применяться к командировкам работника.</span><span class="sxs-lookup"><span data-stu-id="05bd7-121">You can also define per diem rate tiers to set the minimum and maximum number of hours that the per diem rate can be applied to a worker’s travel.</span></span>

<span data-ttu-id="05bd7-122">**Решения:**</span><span class="sxs-lookup"><span data-stu-id="05bd7-122">**Decisions:**</span></span>

- <span data-ttu-id="05bd7-123">Правила выплаты суточных по умолчанию для первого и последнего дня:</span><span class="sxs-lookup"><span data-stu-id="05bd7-123">Default per diem rules for the first and last days:</span></span>

    - <span data-ttu-id="05bd7-124">Какое минимальное количество часов сотрудник может заявить за день и при этом получать суточные?</span><span class="sxs-lookup"><span data-stu-id="05bd7-124">What is the minimum number of hours that an employee can claim for a day and still receive a per diem?</span></span>
    - <span data-ttu-id="05bd7-125">Есть ли уменьшение суммы на питание в первый и последний день?</span><span class="sxs-lookup"><span data-stu-id="05bd7-125">Is there a reduction in the amount that is offered for meals for the first day and last day?</span></span> <span data-ttu-id="05bd7-126">Если есть уменьшение, каков процент уменьшения?</span><span class="sxs-lookup"><span data-stu-id="05bd7-126">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="05bd7-127">Есть ли уменьшение суммы на проживание в первый и последний день?</span><span class="sxs-lookup"><span data-stu-id="05bd7-127">Is there a reduction in the amount that is offered for a hotel for the first day and last day?</span></span> <span data-ttu-id="05bd7-128">Если есть уменьшение, каков процент уменьшения?</span><span class="sxs-lookup"><span data-stu-id="05bd7-128">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="05bd7-129">Есть ли уменьшение суммы на прочие расходы, понесенные в первый и последний день?</span><span class="sxs-lookup"><span data-stu-id="05bd7-129">Is there a reduction in the amount that is offered for other expenses that are incurred on the first day and last day?</span></span> <span data-ttu-id="05bd7-130">Если есть уменьшение, каков процент уменьшения?</span><span class="sxs-lookup"><span data-stu-id="05bd7-130">If there is a reduction, what is the percentage of the reduction?</span></span>

- <span data-ttu-id="05bd7-131">Правила выплаты суточных по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="05bd7-131">Default per diem rules:</span></span>

    - <span data-ttu-id="05bd7-132">Есть ли процентное снижение суточных для каждого приема пищи, если, например, питание является бесплатным?</span><span class="sxs-lookup"><span data-stu-id="05bd7-132">Is there a percentage reduction in the per diem allowance for each meal if, for example, the meal is complimentary?</span></span> <span data-ttu-id="05bd7-133">Если есть уменьшение, каков процент уменьшения для каждого приема пищи?</span><span class="sxs-lookup"><span data-stu-id="05bd7-133">If there is a reduction, what is the reduction percentage for each meal?</span></span>
    - <span data-ttu-id="05bd7-134">Рассчитывается ли уменьшение суммы на питание за день, за поездку или на количество приемов пищи в день?</span><span class="sxs-lookup"><span data-stu-id="05bd7-134">Is the meal reduction calculated per day, per trip, or by the number of meals per day?</span></span>
    - <span data-ttu-id="05bd7-135">Следует ли округлять суточные в обычном порядке или в большую сторону?</span><span class="sxs-lookup"><span data-stu-id="05bd7-135">Should per diem amounts be rounded in the regular manner or rounded up?</span></span>
    - <span data-ttu-id="05bd7-136">Суточные рассчитываются на 24-часовой период или на календарный день?</span><span class="sxs-lookup"><span data-stu-id="05bd7-136">Are per diems calculated on a 24-hour period or on a calendar day?</span></span>

- <span data-ttu-id="05bd7-137">Правила выплаты суточных в зависимости от местоположения:</span><span class="sxs-lookup"><span data-stu-id="05bd7-137">Per diem rules that are based on location:</span></span>

    - <span data-ttu-id="05bd7-138">Различаются ли ставки суточных в зависимости от местоположения?</span><span class="sxs-lookup"><span data-stu-id="05bd7-138">Do per diem rates vary according to location?</span></span> <span data-ttu-id="05bd7-139">Какие местоположения включены?</span><span class="sxs-lookup"><span data-stu-id="05bd7-139">What locations are included?</span></span>
    - <span data-ttu-id="05bd7-140">Если ставки суточных меняются в зависимости от местоположения, то для каждого местоположения какая процентная сумма предусмотрена для следующих видов расходов:</span><span class="sxs-lookup"><span data-stu-id="05bd7-140">If per diem rates vary according to location, for each location, what percentage amount is provided for the following types of expenses:</span></span>

        - <span data-ttu-id="05bd7-141">Питание</span><span class="sxs-lookup"><span data-stu-id="05bd7-141">Meals</span></span>
        - <span data-ttu-id="05bd7-142">Отель</span><span class="sxs-lookup"><span data-stu-id="05bd7-142">Hotel</span></span>
        - <span data-ttu-id="05bd7-143">Другие расходы</span><span class="sxs-lookup"><span data-stu-id="05bd7-143">Other expenses</span></span>

### <a name="expense-management-journals-and-accounts"></a><span data-ttu-id="05bd7-144">Журналы и счета управления расходами</span><span class="sxs-lookup"><span data-stu-id="05bd7-144">Expense management journals and accounts</span></span>

<span data-ttu-id="05bd7-145">Управление расходами требует использования нескольких журналов и счетов.</span><span class="sxs-lookup"><span data-stu-id="05bd7-145">Expense management requires that you use multiple journals and accounts.</span></span> <span data-ttu-id="05bd7-146">Вы должны решить, например, будет ли использоваться один и тот же счет для денежных авансов и споров по кредитным картам.</span><span class="sxs-lookup"><span data-stu-id="05bd7-146">You must decide, for example, whether the same account is used for cash advances and credit card disputes.</span></span>

<span data-ttu-id="05bd7-147">**Решения:**</span><span class="sxs-lookup"><span data-stu-id="05bd7-147">**Decisions:**</span></span>

- <span data-ttu-id="05bd7-148">В какой журнал книги учета разносятся утвержденные отчеты о расходах?</span><span class="sxs-lookup"><span data-stu-id="05bd7-148">Which ledger journal are approved expense reports posted to?</span></span>
- <span data-ttu-id="05bd7-149">Какой счет используется для денежных авансов?</span><span class="sxs-lookup"><span data-stu-id="05bd7-149">Which account is used for cash advances?</span></span>
- <span data-ttu-id="05bd7-150">Следует ли немедленно разносить денежные авансы?</span><span class="sxs-lookup"><span data-stu-id="05bd7-150">Should cash advances be posted immediately?</span></span>

### <a name="payment-methods"></a><span data-ttu-id="05bd7-151">Способы оплаты</span><span class="sxs-lookup"><span data-stu-id="05bd7-151">Payment methods</span></span>

<span data-ttu-id="05bd7-152">Когда вы разрешаете сотрудникам нести расходы от имени вашего бизнеса, вы должны определить способы оплаты, которые сотрудники могут использовать.</span><span class="sxs-lookup"><span data-stu-id="05bd7-152">When you allow employees to incur expenses on behalf of your business, you must define the payment methods that employees are allowed to use.</span></span> <span data-ttu-id="05bd7-153">Например, вы можете разрешить сотрудникам использовать наличные деньги или корпоративную кредитную карту.</span><span class="sxs-lookup"><span data-stu-id="05bd7-153">For example, you might allow employees to use cash or a corporate credit card.</span></span> <span data-ttu-id="05bd7-154">Вы также можете разрешить сотрудникам использовать личные кредитные карты, а затем возмещать расходы сотрудникам.</span><span class="sxs-lookup"><span data-stu-id="05bd7-154">You might also allow employees to use personal credit cards, and then reimburse the employees.</span></span> <span data-ttu-id="05bd7-155">Вы должны принять следующие решения для каждого разрешенного вами способа оплаты.</span><span class="sxs-lookup"><span data-stu-id="05bd7-155">You must make the following decisions for each payment method that you allow.</span></span>

<span data-ttu-id="05bd7-156">**Решения:**</span><span class="sxs-lookup"><span data-stu-id="05bd7-156">**Decisions:**</span></span>

- <span data-ttu-id="05bd7-157">Какие способы оплаты разрешены?</span><span class="sxs-lookup"><span data-stu-id="05bd7-157">What payment methods are allowed?</span></span>
- <span data-ttu-id="05bd7-158">Кому принадлежат расходы по способу оплаты?</span><span class="sxs-lookup"><span data-stu-id="05bd7-158">Who owns the payment method expenses?</span></span>
- <span data-ttu-id="05bd7-159">Есть ли тип корреспондирующего счета?</span><span class="sxs-lookup"><span data-stu-id="05bd7-159">Is there an offset account type?</span></span> <span data-ttu-id="05bd7-160">Если есть тип корреспондирующего счета, то какой это тип?</span><span class="sxs-lookup"><span data-stu-id="05bd7-160">If there is an offset account type, what is it?</span></span>
- <span data-ttu-id="05bd7-161">Если есть корреспондирующий счет, то какой это счет?</span><span class="sxs-lookup"><span data-stu-id="05bd7-161">If there is an offset account, what is the account?</span></span>
- <span data-ttu-id="05bd7-162">Если способ оплаты — это кредитная карта, следует ли использовать этот метод оплаты только для импортированных транзакций?</span><span class="sxs-lookup"><span data-stu-id="05bd7-162">If the payment method is a credit card, should the payment method be used only with imported transactions?</span></span>

### <a name="expense-categories-and-shared-categories"></a><span data-ttu-id="05bd7-163">Категории расходов и общие категории</span><span class="sxs-lookup"><span data-stu-id="05bd7-163">Expense categories and shared categories</span></span>

<span data-ttu-id="05bd7-164">Когда сотрудники создают отчет о расходах, все регистрируемые ими расходы должны быть связаны с категорией расходов.</span><span class="sxs-lookup"><span data-stu-id="05bd7-164">When employees create an expense report, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="05bd7-165">Категории расходов являются производными от общих категорий, которые могут совместно использоваться юридическими лицами в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="05bd7-165">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="05bd7-166">Эти категории также могут быть общими для управления проектами и учета, в зависимости от того, как определена ваша организация.</span><span class="sxs-lookup"><span data-stu-id="05bd7-166">These categories can also be shared in Project management and accounting, depending on the way that your organization is defined.</span></span> <span data-ttu-id="05bd7-167">Основываясь на определении вашей организации и руководящих указаниях от группы внедрения, определите, будут ли категории, используемые в управлении расходами, использоваться только в управлении расходами или они должны быть общими для управления и учета по проекту и управления расходами.</span><span class="sxs-lookup"><span data-stu-id="05bd7-167">Based on the definition of your organization and guidance from the implementation team, determine whether the categories that are used in Expense management will be used only in Expense management, or whether they should be shared between Project management and accounting and Expense management.</span></span> <span data-ttu-id="05bd7-168">Обратите внимание, что эти категории могут использоваться совместно в модулях управления проектами и расходами или в модулях управлением проектами и производством, но не в модулях управления расходами и производством.</span><span class="sxs-lookup"><span data-stu-id="05bd7-168">Note that these categories can be shared between Project and Expense or Project and Production, but not between Expense and Production.</span></span> <span data-ttu-id="05bd7-169">Вы должны принять следующие решения для каждой категории расходов.</span><span class="sxs-lookup"><span data-stu-id="05bd7-169">You must make the following decisions for each expense category.</span></span>

<span data-ttu-id="05bd7-170">**Решения:**</span><span class="sxs-lookup"><span data-stu-id="05bd7-170">**Decisions:**</span></span>

- <span data-ttu-id="05bd7-171">Что такое категория расходов?</span><span class="sxs-lookup"><span data-stu-id="05bd7-171">What is the expense category?</span></span> <span data-ttu-id="05bd7-172">Примеры включают категории для билетов на самолет, проживания в гостиницах или пробега.</span><span class="sxs-lookup"><span data-stu-id="05bd7-172">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="05bd7-173">Можно ли использовать категорию расходов в управлении проектами и бухгалтерском учете?</span><span class="sxs-lookup"><span data-stu-id="05bd7-173">Can the expense category also be used in Project management and accounting?</span></span>
- <span data-ttu-id="05bd7-174">Что такое тип расходов?</span><span class="sxs-lookup"><span data-stu-id="05bd7-174">What is the expense type?</span></span>
- <span data-ttu-id="05bd7-175">Какой метод оплаты используется по умолчанию для категории расходов?</span><span class="sxs-lookup"><span data-stu-id="05bd7-175">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="05bd7-176">Нужна ли детализация расходов в категории расходов?</span><span class="sxs-lookup"><span data-stu-id="05bd7-176">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="05bd7-177">Какой основной счет используется по умолчанию для категории расходов?</span><span class="sxs-lookup"><span data-stu-id="05bd7-177">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="05bd7-178">Какая группа налога с продаж товаров используется по умолчанию для категории расходов?</span><span class="sxs-lookup"><span data-stu-id="05bd7-178">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="05bd7-179">Допускаются ли дополнительные способы оплаты для категории расходов?</span><span class="sxs-lookup"><span data-stu-id="05bd7-179">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="05bd7-180">Если разрешены дополнительные способы оплаты, какие они?</span><span class="sxs-lookup"><span data-stu-id="05bd7-180">If additional payment methods are allowed, what are they?</span></span>
- <span data-ttu-id="05bd7-181">Есть ли в этой категории расходов подкатегории?</span><span class="sxs-lookup"><span data-stu-id="05bd7-181">Are there subcategories in this expense category?</span></span> <span data-ttu-id="05bd7-182">Если есть подкатегории, необходимо также принять следующие решения:</span><span class="sxs-lookup"><span data-stu-id="05bd7-182">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="05bd7-183">Исключаются ли какие-либо подкатегории из налогового возмещения?</span><span class="sxs-lookup"><span data-stu-id="05bd7-183">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="05bd7-184">Какова налоговая группа номенклатур в подкатегориях?</span><span class="sxs-lookup"><span data-stu-id="05bd7-184">What is the item sales tax group of the subcategories?</span></span>

<span data-ttu-id="05bd7-185">Если категория расходов также используется в управлении и бухгалтерском учете проектов, ответьте на оставшиеся вопросы.</span><span class="sxs-lookup"><span data-stu-id="05bd7-185">If the expense category is also used in Project management and accounting, answer the remaining questions.</span></span> <span data-ttu-id="05bd7-186">В противном случае переходите к следующему разделу.</span><span class="sxs-lookup"><span data-stu-id="05bd7-186">Otherwise, move on to the next section.</span></span>

- <span data-ttu-id="05bd7-187">Какие счета затрат будут использоваться для следующих расходов?</span><span class="sxs-lookup"><span data-stu-id="05bd7-187">Which cost accounts will be used for the following expenses?</span></span>

    - <span data-ttu-id="05bd7-188">Себестоимость</span><span class="sxs-lookup"><span data-stu-id="05bd7-188">Cost</span></span>
    - <span data-ttu-id="05bd7-189">Распределение заработной платы</span><span class="sxs-lookup"><span data-stu-id="05bd7-189">Payroll allocation</span></span>
    - <span data-ttu-id="05bd7-190">НЗП - Себестоимость</span><span class="sxs-lookup"><span data-stu-id="05bd7-190">WIP-cost value</span></span>
    - <span data-ttu-id="05bd7-191">Себестоимость - Номенклатура</span><span class="sxs-lookup"><span data-stu-id="05bd7-191">Cost-item</span></span>
    - <span data-ttu-id="05bd7-192">НЗП - Себестоимость - Номенклатура</span><span class="sxs-lookup"><span data-stu-id="05bd7-192">WIP-cost value-item</span></span>
    - <span data-ttu-id="05bd7-193">Начисленный убыток</span><span class="sxs-lookup"><span data-stu-id="05bd7-193">Accrued loss</span></span>
    - <span data-ttu-id="05bd7-194">НЗП - Начисленный убыток</span><span class="sxs-lookup"><span data-stu-id="05bd7-194">WIP-accrued loss</span></span>

- <span data-ttu-id="05bd7-195">Какие счета доходов будут использоваться для следующего?</span><span class="sxs-lookup"><span data-stu-id="05bd7-195">Which revenue accounts will be used for the following?</span></span>

    - <span data-ttu-id="05bd7-196">Выручка по выставленным накладным</span><span class="sxs-lookup"><span data-stu-id="05bd7-196">Invoiced revenue</span></span>
    - <span data-ttu-id="05bd7-197">Начисленная выручка - Сумма реализации</span><span class="sxs-lookup"><span data-stu-id="05bd7-197">Accrued revenue-sales value</span></span>
    - <span data-ttu-id="05bd7-198">НЗП - сумма реализации</span><span class="sxs-lookup"><span data-stu-id="05bd7-198">WIP-sales value</span></span>
    - <span data-ttu-id="05bd7-199">Начисленная выручка - производство</span><span class="sxs-lookup"><span data-stu-id="05bd7-199">Accrued revenue-production</span></span>
    - <span data-ttu-id="05bd7-200">НЗП - производство</span><span class="sxs-lookup"><span data-stu-id="05bd7-200">WIP-production</span></span>
    - <span data-ttu-id="05bd7-201">Начисленная выручка - прибыль</span><span class="sxs-lookup"><span data-stu-id="05bd7-201">Accrued revenue-profit</span></span>
    - <span data-ttu-id="05bd7-202">НЗП- прибыль</span><span class="sxs-lookup"><span data-stu-id="05bd7-202">WIP-profit</span></span>
    - <span data-ttu-id="05bd7-203">Начисленная выручка - подписка</span><span class="sxs-lookup"><span data-stu-id="05bd7-203">Accrued revenue-subscription</span></span>
    - <span data-ttu-id="05bd7-204">НЗП - подписка</span><span class="sxs-lookup"><span data-stu-id="05bd7-204">WIP-subscription</span></span>

### <a name="taxes"></a><span data-ttu-id="05bd7-205">Налоги</span><span class="sxs-lookup"><span data-stu-id="05bd7-205">Taxes</span></span>

<span data-ttu-id="05bd7-206">Для налогов, связанных с расходами, вы должны определить, что должно входить в отчеты о расходах или быть включено в них.</span><span class="sxs-lookup"><span data-stu-id="05bd7-206">For expense-related taxes, you must determine what is included or enabled on expense reports.</span></span>

<span data-ttu-id="05bd7-207">**Решения:**</span><span class="sxs-lookup"><span data-stu-id="05bd7-207">**Decisions:**</span></span>

- <span data-ttu-id="05bd7-208">Включен ли налог с продаж в сумму расходов?</span><span class="sxs-lookup"><span data-stu-id="05bd7-208">Is sales tax included in the expense amounts?</span></span>
- <span data-ttu-id="05bd7-209">Следует ли разрешить возврат налогов на расходы?</span><span class="sxs-lookup"><span data-stu-id="05bd7-209">Should tax recovery be enabled on expenses?</span></span>

    > [!NOTE]
    > <span data-ttu-id="05bd7-210">Если при планировании главной книги вы решили применить налог с продаж в США и использовать налоговые правила, вы не сможете включить возврат налога на расходы.</span><span class="sxs-lookup"><span data-stu-id="05bd7-210">When you were planning the general ledger, if you decided to apply U.S. sales tax and use tax rules, you can’t enable tax recovery on expenses.</span></span> <span data-ttu-id="05bd7-211">(Чтобы применить налог с продаж в США и использовать налоговые правила, установите для параметра **Применить правила налогообложения для налога с продаж** значение **Да**.)</span><span class="sxs-lookup"><span data-stu-id="05bd7-211">(To apply U.S. sales tax and use tax rules, set the **Apply sales tax taxations rules** option to **Yes**.)</span></span>

## <a name="policies"></a><span data-ttu-id="05bd7-212">Политики</span><span class="sxs-lookup"><span data-stu-id="05bd7-212">Policies</span></span>

<span data-ttu-id="05bd7-213">Создавая политики отчетов о расходах, вы можете помочь своей организации сэкономить время и деньги, когда сотрудники несут расходы от ее имени.</span><span class="sxs-lookup"><span data-stu-id="05bd7-213">By creating expense report policies, you can help your organization save time and money when employees incur expenses on its behalf.</span></span> <span data-ttu-id="05bd7-214">Политики помогают гарантировать, что сотрудники остаются в рамках бюджета, предоставляют всю необходимую информацию и тратят деньги только по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="05bd7-214">Policies help guarantee that employees stay in budget, provide all required information, and spend money only as they require it.</span></span> <span data-ttu-id="05bd7-215">Вы должны принять следующие решения для каждой политики отчета о расходах и каждой политики утверждения отчета о расходах, которую вы создаете.</span><span class="sxs-lookup"><span data-stu-id="05bd7-215">You must make the following decisions for each expense report policy and each expense report approval policy that you create.</span></span>

<span data-ttu-id="05bd7-216">**Решения:**</span><span class="sxs-lookup"><span data-stu-id="05bd7-216">**Decisions:**</span></span>

- <span data-ttu-id="05bd7-217">Какое имя у политики?</span><span class="sxs-lookup"><span data-stu-id="05bd7-217">What is the name of the policy?</span></span>
- <span data-ttu-id="05bd7-218">Для чего предназначена политика расходов?</span><span class="sxs-lookup"><span data-stu-id="05bd7-218">What is the expense policy for?</span></span>
- <span data-ttu-id="05bd7-219">Если вы ранее решили включить внутрихолдинговые расходы, к каким компаниям в вашей организации будет применяться эта политика?</span><span class="sxs-lookup"><span data-stu-id="05bd7-219">If you previously decided to enable intercompany expenses, which companies in your organization will this policy apply to?</span></span>
- <span data-ttu-id="05bd7-220">Когда политика вступает в силу?</span><span class="sxs-lookup"><span data-stu-id="05bd7-220">When does the policy become effective?</span></span>
- <span data-ttu-id="05bd7-221">Когда истекает срок действия политики?</span><span class="sxs-lookup"><span data-stu-id="05bd7-221">When does the policy expire?</span></span>
- <span data-ttu-id="05bd7-222">Какое правило политики?</span><span class="sxs-lookup"><span data-stu-id="05bd7-222">What is the policy rule?</span></span>
- <span data-ttu-id="05bd7-223">Каков результат действия правила политики?</span><span class="sxs-lookup"><span data-stu-id="05bd7-223">What is the outcome of the policy rule?</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]