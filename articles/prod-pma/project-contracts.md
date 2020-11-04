---
title: Контракты по проектам
description: Эта тема содержит примеры контрактов по проектам, которые вы можете создать для различных типов проектов и источников финансирования, а также способы управления контрактами и выставлением счетов клиентам проекта.
author: Yowelle
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b7d15523f1b22bb8813a47f9f822f12bc4162104
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083319"
---
# <a name="project-contracts"></a><span data-ttu-id="05cc0-103">Контракты по проектам</span><span class="sxs-lookup"><span data-stu-id="05cc0-103">Project contracts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="05cc0-104">Эта статья содержит примеры контрактов по проектам, которые вы можете создать для различных типов проектов и источников финансирования, а также способы управления контрактами и выставлением счетов клиентам проекта.</span><span class="sxs-lookup"><span data-stu-id="05cc0-104">This article provides examples of the project contracts that you can create for various types of projects and funding sources, and how you can manage contracts and invoice project customers.</span></span>

<span data-ttu-id="05cc0-105">Тип проекта, который вы создаете для контракта по проекту, определяет метод, который используется для выставления счетов клиентам проекта.</span><span class="sxs-lookup"><span data-stu-id="05cc0-105">The type of project that you create for a project contract determines the method that is used to invoice project customers.</span></span> <span data-ttu-id="05cc0-106">Вы можете изменить контракт проекта и связанный проект, но не можете изменить тип проекта.</span><span class="sxs-lookup"><span data-stu-id="05cc0-106">You can change a project contract and the related project, but you can't change the project type.</span></span> 

<span data-ttu-id="05cc0-107">Используя контракт по проекту, вы можете выставлять счета одновременно для одного или нескольких проектов.</span><span class="sxs-lookup"><span data-stu-id="05cc0-107">By using a project contract, you can invoice one or more projects at the same time.</span></span> <span data-ttu-id="05cc0-108">Контракт по проекту также помогает гарантировать единообразную процедуру выставления счетов для каждого вложенного проекта в структуре проекта.</span><span class="sxs-lookup"><span data-stu-id="05cc0-108">The project contract also helps guarantee a consistent invoicing procedure for every subproject in a project structure.</span></span> 

<span data-ttu-id="05cc0-109">Каждый проект, по которому будет выставлен счет, должен быть связан с контрактом по проекту.</span><span class="sxs-lookup"><span data-stu-id="05cc0-109">Every project that will be invoiced must be associated with a project contract.</span></span> <span data-ttu-id="05cc0-110">Параметры контракта по проекту применяются ко всем проектам и вложенным проектам, связанным с этим контрактом по проекту.</span><span class="sxs-lookup"><span data-stu-id="05cc0-110">The settings for a project contract apply to all projects and subprojects that are associated with that project contract.</span></span> 

<span data-ttu-id="05cc0-111">В контракте по проекту можно указать один или несколько источников финансирования.</span><span class="sxs-lookup"><span data-stu-id="05cc0-111">A project contract can specify one or more sources of funding.</span></span> <span data-ttu-id="05cc0-112">Таким образом, вы можете разделить выставление счетов между несколькими спонсорами, установить лимиты финансирования, чтобы источники финансирования не выставляли счета на сумму, превышающую указанную, и настроить правила финансирования для начисления расходов.</span><span class="sxs-lookup"><span data-stu-id="05cc0-112">Therefore, you can split the billing among multiple funders, set up funding limits so that funding sources are not billed more than a specified amount, and configure funding rules for charging expenditures.</span></span>

## <a name="funding-for-project-contracts"></a><span data-ttu-id="05cc0-113">Финансирование контрактов по проекту</span><span class="sxs-lookup"><span data-stu-id="05cc0-113">Funding for project contracts</span></span>
<span data-ttu-id="05cc0-114">В некоторых контрактах по проекту указано, что несколько сторон несут ответственность за финансирование проектных затрат.</span><span class="sxs-lookup"><span data-stu-id="05cc0-114">Some project contracts specify that multiple parties share the responsibility for funding the project costs.</span></span> <span data-ttu-id="05cc0-115">Ниже приведено несколько примеров:</span><span class="sxs-lookup"><span data-stu-id="05cc0-115">Here are some examples:</span></span>

-   <span data-ttu-id="05cc0-116">Крупный заказчик, у которого есть несколько подразделений, просит разделить финансирование проекта по подразделениям.</span><span class="sxs-lookup"><span data-stu-id="05cc0-116">A large customer that has multiple divisions requests that funding of a project be split by division.</span></span>
-   <span data-ttu-id="05cc0-117">Ваша компания разделяет расходы на крупный проект с внешней организацией.</span><span class="sxs-lookup"><span data-stu-id="05cc0-117">Your company shares the costs of a large project with an external organization.</span></span>
-   <span data-ttu-id="05cc0-118">Дорожный проект совместно финансируется двумя муниципалитетами.</span><span class="sxs-lookup"><span data-stu-id="05cc0-118">A  road project is co-funded by two municipalities.</span></span>
-   <span data-ttu-id="05cc0-119">Проект моста финансируется за счет государственного гранта и частной корпорации.</span><span class="sxs-lookup"><span data-stu-id="05cc0-119">A bridge project is funded by a government grant and a private corporation.</span></span>

<span data-ttu-id="05cc0-120">В Dynamics 365 Finance вы можете разделить счет за одну транзакцию или весь проект между несколькими клиентами, грантами или организациями.</span><span class="sxs-lookup"><span data-stu-id="05cc0-120">In Dynamics 365 Finance, you can split the billing for a single transaction or an entire project among multiple customers, grants, or organizations.</span></span> 

<span data-ttu-id="05cc0-121">В проектах, у которых есть несколько спонсоров, все стороны, которые вносят вклад в финансирование проекта расширенного финансирования, называются источниками финансирования.</span><span class="sxs-lookup"><span data-stu-id="05cc0-121">In projects that have multiple funders, all parties that contribute to the funding of an advanced funding project are called funding sources.</span></span> <span data-ttu-id="05cc0-122">После того как заказчик, организация или грант определены как источник финансирования, они могут быть назначены одному или нескольким правилам финансирования.</span><span class="sxs-lookup"><span data-stu-id="05cc0-122">After a customer, organization, or grant is defined as a funding source, it can be assigned to one or more funding rules.</span></span> <span data-ttu-id="05cc0-123">Правила финансирования содержат критерии, определяющие, как расходы распределяются между различными источниками финансирования проекта.</span><span class="sxs-lookup"><span data-stu-id="05cc0-123">Funding rules contain the criteria that determines how charges are allocated to the various funding sources for a project.</span></span> 

<span data-ttu-id="05cc0-124">Поскольку номенклатуры в запасах, такие как те, которые указаны в заявках на покупку и заказах на покупку, нельзя разделить, сумма затрат не может быть разделена между несколькими источниками финансирования во время распределения.</span><span class="sxs-lookup"><span data-stu-id="05cc0-124">Because stocked items, such as those that appear on purchase requisitions and purchase orders, can't be split, the cost amount can't be split among multiple funding sources at the time of distribution.</span></span> <span data-ttu-id="05cc0-125">Следовательно, значение источника финансирования остается 0 (нулем) до разноски отпуска запасов.</span><span class="sxs-lookup"><span data-stu-id="05cc0-125">Therefore, the funding source value remains 0 (zero) until the inventory issue is posted.</span></span> <span data-ttu-id="05cc0-126">При разноске расхода запасов сумма затрат распределяется в соответствии с правилами распределения счетов для проекта.</span><span class="sxs-lookup"><span data-stu-id="05cc0-126">When the inventory issue is posted, the cost amount is distributed according to the account distribution rules for the project.</span></span>

<span data-ttu-id="05cc0-127">Вот несколько шагов, которые можно предпринять, чтобы упростить разделение счетов между несколькими источниками финансирования:</span><span class="sxs-lookup"><span data-stu-id="05cc0-127">Here are some steps that you can take to make it easier to split the billing among multiple funding sources:</span></span>

-   <span data-ttu-id="05cc0-128">Укажите, что все проводки, вводимые для проекта, используют ту же валюту продаж, что и контракт по проекту.</span><span class="sxs-lookup"><span data-stu-id="05cc0-128">Specify that all transactions that are entered for a project use the same sales currency as the project contract.</span></span>
-   <span data-ttu-id="05cc0-129">Установите лимиты финансирования, чтобы источник финансирования не выставлял счет для проекта больше указанной суммы.</span><span class="sxs-lookup"><span data-stu-id="05cc0-129">Set up funding limits, so that a funding source isn't invoiced more than a specified amount toward a project.</span></span>
-   <span data-ttu-id="05cc0-130">Настройте правила финансирования и лимиты финансирования для каждого работника, элемента, категории, группы категорий и типа транзакции (или для всех типов транзакций).</span><span class="sxs-lookup"><span data-stu-id="05cc0-130">Configure funding rules and funding limits for each worker, item, category, category group, and transaction type (or for all transaction types).</span></span>
-   <span data-ttu-id="05cc0-131">Выберите необязательные даты начала и окончания, чтобы определить период действия каждого правила финансирования.</span><span class="sxs-lookup"><span data-stu-id="05cc0-131">Select optional start and end dates to define the period when each funding rule is valid.</span></span>
-   <span data-ttu-id="05cc0-132">Укажите процент, за который отвечает каждый источник финансирования.</span><span class="sxs-lookup"><span data-stu-id="05cc0-132">Specify the percentage that each funding source is responsible for.</span></span>
-   <span data-ttu-id="05cc0-133">Укажите, какой источник финансирования отвечает за разницу в округлении, вызванную расчетами распределения финансирования.</span><span class="sxs-lookup"><span data-stu-id="05cc0-133">Specify which funding source is responsible for rounding differences that are caused by funding allocation calculations.</span></span>
-   <span data-ttu-id="05cc0-134">Установите правила, которые определяют, как затраты по проекту выставляются внешним клиентам и взимаются с внутренних организаций.</span><span class="sxs-lookup"><span data-stu-id="05cc0-134">Set up rules that determine how project costs are invoiced to external customers and charged to internal organizations.</span></span>
-   <span data-ttu-id="05cc0-135">Записывайте транзакции на счете отложенного финансирования до тех пор, пока не будет получено дополнительное финансирование или пока вы не решите нести расходы внутри компании.</span><span class="sxs-lookup"><span data-stu-id="05cc0-135">Record transactions in an on-hold funding account until additional funding can be obtained, or until you decide to bear the costs internally.</span></span>

<span data-ttu-id="05cc0-136">Чтобы определить, какую налоговую группу нужно связать с транзакцией, в проекте выполняется поиск присвоения налоговой группы.</span><span class="sxs-lookup"><span data-stu-id="05cc0-136">To determine which tax group to associate with a transaction, the project is searched for a tax group assignment.</span></span> <span data-ttu-id="05cc0-137">Если присвоение налоговой группы не было выполнено на уровне проекта, выполняется поиск контракта по проекту.</span><span class="sxs-lookup"><span data-stu-id="05cc0-137">If no tax group assignment has been made at the project level, the project contract is searched.</span></span>

### <a name="example-multiple-funding-sources-simple"></a><span data-ttu-id="05cc0-138">Пример: несколько источников финансирования (простой)</span><span class="sxs-lookup"><span data-stu-id="05cc0-138">Example: Multiple funding sources (simple)</span></span>

<span data-ttu-id="05cc0-139">В следующей таблице представлены сценарии управления распределением финансирования между несколькими источниками финансирования.</span><span class="sxs-lookup"><span data-stu-id="05cc0-139">The following table provides scenarios for managing funding allocation among multiple funding sources.</span></span> <span data-ttu-id="05cc0-140">Эти сценарии основаны на следующих предположениях:</span><span class="sxs-lookup"><span data-stu-id="05cc0-140">These scenarios are based on the following assumptions:</span></span>

-   <span data-ttu-id="05cc0-141">Настройки приоритета учитываются при распределении средств до применения других критериев правила финансирования.</span><span class="sxs-lookup"><span data-stu-id="05cc0-141">Priority settings are factored into the allocation of funds before other funding rule criteria are applied.</span></span>
-   <span data-ttu-id="05cc0-142">Не указан диапазон дат для определения периода d, когда действует правило финансирования.</span><span class="sxs-lookup"><span data-stu-id="05cc0-142">No date range has been specified to define the period d when the funding rule is valid.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="05cc0-143"><strong>Сценарий</strong></span><span class="sxs-lookup"><span data-stu-id="05cc0-143"><strong>Scenario</strong></span></span></td>
<td><span data-ttu-id="05cc0-144"><strong>Источник финансирования</strong></span><span class="sxs-lookup"><span data-stu-id="05cc0-144"><strong>Funding source</strong></span></span></td>
<td><span data-ttu-id="05cc0-145"><strong>Процент распределения</strong></span><span class="sxs-lookup"><span data-stu-id="05cc0-145"><strong>Allocation percentage</strong></span></span></td>
<td><span data-ttu-id="05cc0-146"><strong>Приоритет распределения</strong></span><span class="sxs-lookup"><span data-stu-id="05cc0-146"><strong>Allocation priority</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="05cc0-147">Вы хотите распределить затраты на один источник финансирования до тех пор, пока его средства не будут исчерпаны, распределить затраты на второй источник финансирования до тех пор, пока его средства не будут исчерпаны, и, наконец, распределить оставшиеся затраты на третий источник финансирования.</span><span class="sxs-lookup"><span data-stu-id="05cc0-147">You want to allocate costs to one funding source until its funds are exhausted, allocate costs to a second funding source until its funds are exhausted, and finally allocate the remaining costs to a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="05cc0-148">Источник　финансирования　1</span><span class="sxs-lookup"><span data-stu-id="05cc0-148">Funding　source　1</span></span></li>
<li><span data-ttu-id="05cc0-149">Источник　финансирования　2</span><span class="sxs-lookup"><span data-stu-id="05cc0-149">Funding　source　2</span></span></li>
<li><span data-ttu-id="05cc0-150">Источник　финансирования　3</span><span class="sxs-lookup"><span data-stu-id="05cc0-150">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="05cc0-151">100%</span><span class="sxs-lookup"><span data-stu-id="05cc0-151">100%</span></span></li>
<li><span data-ttu-id="05cc0-152">100%</span><span class="sxs-lookup"><span data-stu-id="05cc0-152">100%</span></span></li>
<li><span data-ttu-id="05cc0-153">100%</span><span class="sxs-lookup"><span data-stu-id="05cc0-153">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="05cc0-154">1</span><span class="sxs-lookup"><span data-stu-id="05cc0-154">1</span></span></li>
<li><span data-ttu-id="05cc0-155">2</span><span class="sxs-lookup"><span data-stu-id="05cc0-155">2</span></span></li>
<li><span data-ttu-id="05cc0-156">3</span><span class="sxs-lookup"><span data-stu-id="05cc0-156">3</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="05cc0-157">Вы хотите распределить 75 процентов затрат на один источник финансирования и 25 процентов на второй источник финансирования.</span><span class="sxs-lookup"><span data-stu-id="05cc0-157">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="05cc0-158">Когда один из этих источников финансирования исчерпан, вы хотите оплатить оставшиеся затраты из третьего источника финансирования.</span><span class="sxs-lookup"><span data-stu-id="05cc0-158">When either of those funding sources is exhausted, you want to pay the remaining costs from a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="05cc0-159">Источник　финансирования　1</span><span class="sxs-lookup"><span data-stu-id="05cc0-159">Funding　source　1</span></span></li>
<li><span data-ttu-id="05cc0-160">Источник　финансирования　2</span><span class="sxs-lookup"><span data-stu-id="05cc0-160">Funding　source　2</span></span></li>
<li><span data-ttu-id="05cc0-161">Источник　финансирования　3</span><span class="sxs-lookup"><span data-stu-id="05cc0-161">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="05cc0-162">75%</span><span class="sxs-lookup"><span data-stu-id="05cc0-162">75%</span></span></li>
<li><span data-ttu-id="05cc0-163">25%</span><span class="sxs-lookup"><span data-stu-id="05cc0-163">25%</span></span></li>
<li><span data-ttu-id="05cc0-164">100%</span><span class="sxs-lookup"><span data-stu-id="05cc0-164">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="05cc0-165">1</span><span class="sxs-lookup"><span data-stu-id="05cc0-165">1</span></span></li>
<li><span data-ttu-id="05cc0-166">1</span><span class="sxs-lookup"><span data-stu-id="05cc0-166">1</span></span></li>
<li><span data-ttu-id="05cc0-167">2</span><span class="sxs-lookup"><span data-stu-id="05cc0-167">2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="05cc0-168">Вы хотите распределить 75 процентов затрат на один источник финансирования и 25 процентов на второй источник финансирования.</span><span class="sxs-lookup"><span data-stu-id="05cc0-168">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="05cc0-169">Когда один из этих источников финансирования исчерпан, вы хотите разделить оставшиеся затраты между третьим и четвертым источником финансирования.</span><span class="sxs-lookup"><span data-stu-id="05cc0-169">When either of those funding sources is exhausted, you want to split the remaining costs between a third funding source and a fourth funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="05cc0-170">Источник　финансирования　1</span><span class="sxs-lookup"><span data-stu-id="05cc0-170">Funding　source　1</span></span></li>
<li><span data-ttu-id="05cc0-171">Источник　финансирования　2</span><span class="sxs-lookup"><span data-stu-id="05cc0-171">Funding　source　2</span></span></li>
<li><span data-ttu-id="05cc0-172">Источник　финансирования　3</span><span class="sxs-lookup"><span data-stu-id="05cc0-172">Funding　source　3</span></span></li>
<li><span data-ttu-id="05cc0-173">Источник　финансирования　4</span><span class="sxs-lookup"><span data-stu-id="05cc0-173">Funding　source　4</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="05cc0-174">75%</span><span class="sxs-lookup"><span data-stu-id="05cc0-174">75%</span></span></li>
<li><span data-ttu-id="05cc0-175">25%</span><span class="sxs-lookup"><span data-stu-id="05cc0-175">25%</span></span></li>
<li><span data-ttu-id="05cc0-176">50%</span><span class="sxs-lookup"><span data-stu-id="05cc0-176">50%</span></span></li>
<li><span data-ttu-id="05cc0-177">50%</span><span class="sxs-lookup"><span data-stu-id="05cc0-177">50%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="05cc0-178">1</span><span class="sxs-lookup"><span data-stu-id="05cc0-178">1</span></span></li>
<li><span data-ttu-id="05cc0-179">1</span><span class="sxs-lookup"><span data-stu-id="05cc0-179">1</span></span></li>
<li><span data-ttu-id="05cc0-180">2</span><span class="sxs-lookup"><span data-stu-id="05cc0-180">2</span></span></li>
<li><span data-ttu-id="05cc0-181">2</span><span class="sxs-lookup"><span data-stu-id="05cc0-181">2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="05cc0-182">Вы хотите распределить первые 25 процентов затрат на один источник финансирования и остальные на второй источник финансирования.</span><span class="sxs-lookup"><span data-stu-id="05cc0-182">You want to allocate the first 25 percent of costs to one funding source and the rest to a second funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="05cc0-183">Источник　финансирования　1</span><span class="sxs-lookup"><span data-stu-id="05cc0-183">Funding　source　1</span></span></li>
<li><span data-ttu-id="05cc0-184">Источник　финансирования　2</span><span class="sxs-lookup"><span data-stu-id="05cc0-184">Funding　source　2</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="05cc0-185">25%</span><span class="sxs-lookup"><span data-stu-id="05cc0-185">25%</span></span></li>
<li><span data-ttu-id="05cc0-186">100%</span><span class="sxs-lookup"><span data-stu-id="05cc0-186">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="05cc0-187">1</span><span class="sxs-lookup"><span data-stu-id="05cc0-187">1</span></span></li>
<li><span data-ttu-id="05cc0-188">2</span><span class="sxs-lookup"><span data-stu-id="05cc0-188">2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a><span data-ttu-id="05cc0-189">Пример: несколько источников финансирования (сложный)</span><span class="sxs-lookup"><span data-stu-id="05cc0-189">Example: Multiple funding sources (complex)</span></span>

<span data-ttu-id="05cc0-190">У вас есть три источника финансирования, которые вы хотите использовать в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="05cc0-190">You have three funding sources that you want to use in the following order:</span></span>

1.  <span data-ttu-id="05cc0-191">Используйте источник финансирования 2 и источник финансирования 3 одинаково, пока источник финансирования 2 не будет исчерпан.</span><span class="sxs-lookup"><span data-stu-id="05cc0-191">Use funding source 2 and funding source 3 equally until funding source 2 is exhausted.</span></span>
2.  <span data-ttu-id="05cc0-192">Продолжайте использовать источник финансирования 3, пока он не будет исчерпан.</span><span class="sxs-lookup"><span data-stu-id="05cc0-192">Continue to use funding source 3 until it is exhausted.</span></span>
3.  <span data-ttu-id="05cc0-193">Используйте источник финансирования 1 после того, как источник финансирования 3 будет исчерпан.</span><span class="sxs-lookup"><span data-stu-id="05cc0-193">Use funding source 1 after funding source 3 is exhausted.</span></span>

<span data-ttu-id="05cc0-194">Для достижения этой цели следует сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="05cc0-194">To accomplish this goal, you must do the following:</span></span>

-   <span data-ttu-id="05cc0-195">Установите лимиты финансирования для источника финансирования 2 и источника финансирования 3 для соответствующих сумм.</span><span class="sxs-lookup"><span data-stu-id="05cc0-195">Set up funding limits for funding source 2 and funding source 3, for their respective amounts.</span></span>
-   <span data-ttu-id="05cc0-196">Создайте следующие правила финансирования:</span><span class="sxs-lookup"><span data-stu-id="05cc0-196">Create the following funding rules:</span></span>
    -   <span data-ttu-id="05cc0-197">Правило 1 (Приоритет 1): распределяйте 50 процентов транзакций на источник финансирования 2 и 50 процентов на источник финансирования 3.</span><span class="sxs-lookup"><span data-stu-id="05cc0-197">Rule 1 (Priority 1): Allocate 50 percent of transactions to funding source 2 and 50 percent to funding source 3.</span></span>
    -   <span data-ttu-id="05cc0-198">Правило 2 (Приоритет 2): распределяйте 100 процентов транзакций на источник финансирования 3.</span><span class="sxs-lookup"><span data-stu-id="05cc0-198">Rule 2 (Priority 2): Allocate 100 percent of transactions to funding source 3.</span></span>
    -   <span data-ttu-id="05cc0-199">Правило 3 (Приоритет 3): распределяйте 100 процентов транзакций на источник финансирования 1.</span><span class="sxs-lookup"><span data-stu-id="05cc0-199">Rule 3 (Priority 3): Allocate 100 percent of transactions to funding source 1.</span></span>

<span data-ttu-id="05cc0-200">Эта настройка работает, потому что транзакции проверяются на соответствие правилам и ограничениям, чтобы определить, применимы ли какие-либо из них к транзакции.</span><span class="sxs-lookup"><span data-stu-id="05cc0-200">This setup works because transactions are checked against rules and limits to determine whether any of them apply to the transaction.</span></span> <span data-ttu-id="05cc0-201">Если к транзакции не применяются какие-либо особые правила или ограничения, применяется правило «Все транзакции».</span><span class="sxs-lookup"><span data-stu-id="05cc0-201">If no specific rules or limits apply to the transaction, the All transactions rule applies.</span></span> <span data-ttu-id="05cc0-202">Правило "Все транзакции" соответствует всем транзакциям.</span><span class="sxs-lookup"><span data-stu-id="05cc0-202">The All transactions rule matches all transactions.</span></span> 

<span data-ttu-id="05cc0-203">Если найдено правило, соответствующее транзакции, сначала применяется процент, выделенный в этом правиле, но только после того, как совпадения будут проверены на соответствие установленным ограничениям.</span><span class="sxs-lookup"><span data-stu-id="05cc0-203">If a rule is found that matches a transaction, the percentage that has been allocated in that rule is applied first, but only after the matches are checked against any limits that have been set up.</span></span> <span data-ttu-id="05cc0-204">Если лимит был достигнут и средства источника финансирования исчерпаны, правило финансирования, связанное с лимитом финансирования, игнорируется, и программа проверяет следующее применимое правило.</span><span class="sxs-lookup"><span data-stu-id="05cc0-204">If a limit has been met, and a funding source’s funds are exhausted, the funding rule that is associated with the funding limit is disregarded, and the program checks for the next rule that applies.</span></span> 

<span data-ttu-id="05cc0-205">В некоторых случаях правилом может быть выделена только часть транзакции.</span><span class="sxs-lookup"><span data-stu-id="05cc0-205">In some cases, only part of a transaction can be allocated under a rule.</span></span> <span data-ttu-id="05cc0-206">Это может произойти из-за того, что при распределении транзакции достигнут предел.</span><span class="sxs-lookup"><span data-stu-id="05cc0-206">This might happen because a limit is reached when the transaction is allocated.</span></span> <span data-ttu-id="05cc0-207">В этом случае в соответствии с этим правилом выделяется только определенная сумма, например, 50 процентов на каждый источник финансирования.</span><span class="sxs-lookup"><span data-stu-id="05cc0-207">In this case, only a certain amount is allocated according to that rule, such as 50 percent to each funding source.</span></span> <span data-ttu-id="05cc0-208">Так обстоит дело в правиле 1, которое описано ранее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="05cc0-208">This is the case in rule 1, which is described earlier in this section.</span></span> <span data-ttu-id="05cc0-209">Остаток распределяется согласно следующему правилу в последовательности.</span><span class="sxs-lookup"><span data-stu-id="05cc0-209">The remainder is allocated according to the next rule in the sequence.</span></span> 

<span data-ttu-id="05cc0-210">В следующей таблице этот сценарий рассматривается более подробно.</span><span class="sxs-lookup"><span data-stu-id="05cc0-210">The following table examines this scenario in more detail.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="05cc0-211"><strong>Фокус</strong></span><span class="sxs-lookup"><span data-stu-id="05cc0-211"><strong>Focus</strong></span></span></td>
<td><span data-ttu-id="05cc0-212"><strong>Сведения</strong></span><span class="sxs-lookup"><span data-stu-id="05cc0-212"><strong>Details</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="05cc0-213">Правила финансирования</span><span class="sxs-lookup"><span data-stu-id="05cc0-213">Funding rules</span></span></td>
<td><ul>
<li><span data-ttu-id="05cc0-214">Правило 1 (приоритет 1): все транзакции.</span><span class="sxs-lookup"><span data-stu-id="05cc0-214">Rule 1 (Priority 1): All transactions.</span></span> <span data-ttu-id="05cc0-215">Выделите источник финансирования 2 на уровне 50% и источник финансирования 3 на уровне 50%.</span><span class="sxs-lookup"><span data-stu-id="05cc0-215">Allocate funding source 2 at 50% and funding source 3 at 50%.</span></span></li>
<li><span data-ttu-id="05cc0-216">Правило 2 (приоритет 2): все транзакции.</span><span class="sxs-lookup"><span data-stu-id="05cc0-216">Rule 2 (Priority 2): All transactions.</span></span> <span data-ttu-id="05cc0-217">Установите источник финансирования 3 на уровне 100%.</span><span class="sxs-lookup"><span data-stu-id="05cc0-217">Allocate funding source 3 at 100%.</span></span></li>
<li><span data-ttu-id="05cc0-218">Правило 3 (приоритет 2): все транзакции.</span><span class="sxs-lookup"><span data-stu-id="05cc0-218">Rule 3 (Priority 2): All transactions.</span></span> <span data-ttu-id="05cc0-219">Установите источник финансирования 1 на уровне 100%.</span><span class="sxs-lookup"><span data-stu-id="05cc0-219">Allocate funding source 1 at 100%.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="05cc0-220">Лимиты финансирования</span><span class="sxs-lookup"><span data-stu-id="05cc0-220">Funding limits</span></span></td>
<td><ul>
<li><span data-ttu-id="05cc0-221">Лимит источника финансирования 1 = 10 000,00</span><span class="sxs-lookup"><span data-stu-id="05cc0-221">Funding source 1 limit = 10,000.00</span></span></li>
<li><span data-ttu-id="05cc0-222">Лимит источника финансирования 2 = 500,00</span><span class="sxs-lookup"><span data-stu-id="05cc0-222">Funding source 2 limit = 500.00</span></span></li>
<li><span data-ttu-id="05cc0-223">Лимит источника финансирования 3 = 750,00</span><span class="sxs-lookup"><span data-stu-id="05cc0-223">Funding source 3 limit = 750.00</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="05cc0-224">Проводка 1</span><span class="sxs-lookup"><span data-stu-id="05cc0-224">Transaction 1</span></span></td>
<td><span data-ttu-id="05cc0-225"><strong>Сумма транзакции:</strong> 100,00<strong>Финансирование:</strong> Транзакция оплачивается только в соответствии с правилом 1, потому что транзакция полностью оплачивается после применения правила 1.</span><span class="sxs-lookup"><span data-stu-id="05cc0-225"><strong>Transaction amount:</strong> 100.00<strong>Funding:</strong> The transaction is paid according to rule 1 only, because the transaction is fully paid after rule 1 is applied.</span></span> <span data-ttu-id="05cc0-226">Сделка финансируется поровну между источником финансирования 2 и источником финансирования 3.</span><span class="sxs-lookup"><span data-stu-id="05cc0-226">The transaction is funded equally between funding source 2 and funding source 3.</span></span>
<ul>
<li><span data-ttu-id="05cc0-227">Источник финансирования 2: 50,00</span><span class="sxs-lookup"><span data-stu-id="05cc0-227">Funding source 2: 50.00</span></span></li>
<li><span data-ttu-id="05cc0-228">Источник финансирования 3: 50,00</span><span class="sxs-lookup"><span data-stu-id="05cc0-228">Funding source 3: 50.00</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="05cc0-229">Проводка 2</span><span class="sxs-lookup"><span data-stu-id="05cc0-229">Transaction 2</span></span></td>
<td><span data-ttu-id="05cc0-230"><strong>Сумма транзакции:</strong> 5 000,00<strong>Финансирование:</strong> Транзакция оплачивается по всем трем правилам.</span><span class="sxs-lookup"><span data-stu-id="05cc0-230"><strong>Transaction amount:</strong> 5,000.00<strong>Funding:</strong> The transaction is paid according to all three rules.</span></span> <span data-ttu-id="05cc0-231"><strong>Правило 1</strong>
</span><span class="sxs-lookup"><span data-stu-id="05cc0-231"><strong>Rule 1</strong>
</span></span><ul>
<li><span data-ttu-id="05cc0-232">Источник финансирования 2: 450,00</span><span class="sxs-lookup"><span data-stu-id="05cc0-232">Funding source 2: 450.00</span></span></li>
<li><span data-ttu-id="05cc0-233">Источник финансирования 3: 450,00</span><span class="sxs-lookup"><span data-stu-id="05cc0-233">Funding source 3: 450.00</span></span></li>
</ul><span data-ttu-id="05cc0-234">
<strong>Правило 2</strong>
</span><span class="sxs-lookup"><span data-stu-id="05cc0-234">
<strong>Rule 2</strong>
</span></span><ul>
<li><span data-ttu-id="05cc0-235">Источник финансирования 3: 250,00 (= 750,00 – 50,00 – 450,00)</span><span class="sxs-lookup"><span data-stu-id="05cc0-235">Funding source 3: 250.00 (= 750.00 – 50.00 – 450.00)</span></span></li>
</ul><span data-ttu-id="05cc0-236">
<strong>Правило 3</strong>
</span><span class="sxs-lookup"><span data-stu-id="05cc0-236">
<strong>Rule 3</strong>
</span></span><ul>
<li><span data-ttu-id="05cc0-237">Источник финансирования 1: 3850,00 (= 5000,00 – 450,00 – 450,00 – 250,00)</span><span class="sxs-lookup"><span data-stu-id="05cc0-237">Funding source 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="05cc0-238">Общая сумма средств, распределенных по каждому источнику финансирования</span><span class="sxs-lookup"><span data-stu-id="05cc0-238">Total funds that are distributed for each funding source</span></span></td>
<td><ul>
<li><span data-ttu-id="05cc0-239">Источник финансирования 1: 3850,00</span><span class="sxs-lookup"><span data-stu-id="05cc0-239">Funding source 1: 3,850.00</span></span></li>
<li><span data-ttu-id="05cc0-240">Источник финансирования 2: 500,00</span><span class="sxs-lookup"><span data-stu-id="05cc0-240">Funding source 2: 500.00</span></span></li>
<li><span data-ttu-id="05cc0-241">Источник финансирования 3: 750,00</span><span class="sxs-lookup"><span data-stu-id="05cc0-241">Funding source 3: 750.00</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a><span data-ttu-id="05cc0-242">Правила выставления счетов</span><span class="sxs-lookup"><span data-stu-id="05cc0-242">Billing rules</span></span>
<span data-ttu-id="05cc0-243">Когда вы ведете переговоры по контракту по проекту с заказчиком, вы определяете, как и когда вы можете выставить заказчику счет за работу над проектом.</span><span class="sxs-lookup"><span data-stu-id="05cc0-243">When you negotiate a project contract with a customer, you define how and when you can invoice the customer for work on a project.</span></span> <span data-ttu-id="05cc0-244">После настройки контракта по проекту и проекта вы можете настроить правила выставления счетов для проекта.</span><span class="sxs-lookup"><span data-stu-id="05cc0-244">After you set up the project contract and the project, you can set up billing rules for the project.</span></span> <span data-ttu-id="05cc0-245">Правила выставления счетов основываются на условиях проекта, указанных в контракте по проекту.</span><span class="sxs-lookup"><span data-stu-id="05cc0-245">Billing rules are based on the project terms that are specified in the project contract.</span></span> <span data-ttu-id="05cc0-246">Правила выставления счетов, которые вы можете создать, зависят от условий контракта по проекту и типа проекта, такого как "Время и материалы" или "Фиксированная цена", которые вы связываете с правилом выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="05cc0-246">The billing rules that you can create depend on the terms of the project contract and the project type, such as Time and material or Fixed-price, that you associate with the billing rule.</span></span> <span data-ttu-id="05cc0-247">Для контракта по проекту можно создать более одного правила выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="05cc0-247">You can create more than one billing rule for a project contract.</span></span> <span data-ttu-id="05cc0-248">Вы также можете назначить правило выставления счетов нескольким проектам, которые связаны с одним и тем же контрактом по проекту и с одинаковыми условиями выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="05cc0-248">You can also assign a billing rule to multiple projects that are associated with the same project contract and have similar billing terms.</span></span> 

<span data-ttu-id="05cc0-249">Вы можете настроить следующие типы правил выставления счетов:</span><span class="sxs-lookup"><span data-stu-id="05cc0-249">You can set up the following types of billing rules:</span></span>

-   <span data-ttu-id="05cc0-250">**Единица доставки** — выставляйте счет-фактуру клиенту, когда вы комплектуете единицу поставки.</span><span class="sxs-lookup"><span data-stu-id="05cc0-250">**Unit of delivery** – Invoice a customer when you complete a unit of delivery.</span></span> <span data-ttu-id="05cc0-251">Вы определяете единицы поставки в контракте.</span><span class="sxs-lookup"><span data-stu-id="05cc0-251">You define the units of delivery in the contract.</span></span>
-   <span data-ttu-id="05cc0-252">**Ход выполнения** — выставляйте счет заказчику, когда вы выполняете определенный процент проекта.</span><span class="sxs-lookup"><span data-stu-id="05cc0-252">**Progress** – Invoice a customer when you complete a specified percentage of the project.</span></span> <span data-ttu-id="05cc0-253">Вы можете настроить правило выставления счетов для автоматического расчета процента выполненных работ или вручную рассчитать процент выполненных работ и сумму для выставления счета клиенту.</span><span class="sxs-lookup"><span data-stu-id="05cc0-253">You can set up a billing rule to automatically calculate the percentage of work completed, or you can manually calculate the percentage of work completed and the amount to invoice the customer.</span></span>
-   <span data-ttu-id="05cc0-254">**Веха** — выставляйте счета заказчику на полную сумму вехи проекта, когда она будет достигнута.</span><span class="sxs-lookup"><span data-stu-id="05cc0-254">**Milestone** – Invoice a customer for the full amount of a project milestone when the milestone is reached.</span></span>
-   <span data-ttu-id="05cc0-255">**Вознаграждение** — выставляйте клиенту счет за свои услуги плюс вознаграждение за управление, которое обычно составляет процент от стоимости услуг.</span><span class="sxs-lookup"><span data-stu-id="05cc0-255">**Fee** – Invoice a customer for your services plus a management fee, which is typically a percentage of the cost of services.</span></span>
-   <span data-ttu-id="05cc0-256">**Время и материал** — выставляйте заказчику счет на стоимость времени и материалов, которые используются в проекте.</span><span class="sxs-lookup"><span data-stu-id="05cc0-256">**Time and material** – Invoice a customer for the value of time and materials that are used on a project.</span></span>

<span data-ttu-id="05cc0-257">Для всех типов правил выставления счетов вы можете указать процент удержания, который вычитается из счетов клиентов до тех пор, пока проект не достигнет согласованной стадии.</span><span class="sxs-lookup"><span data-stu-id="05cc0-257">For all types of billing rules, you can specify a retention percentage that is deducted from customer invoices until a project reaches an agreed-upon stage.</span></span> <span data-ttu-id="05cc0-258">Процент удержания платежей указан в контракте по проекту.</span><span class="sxs-lookup"><span data-stu-id="05cc0-258">The payment retention percentage is specified in the project contract.</span></span> <span data-ttu-id="05cc0-259">Сумма рассчитывается на основе общей стоимости строк в счете клиента и вычитается из нее.</span><span class="sxs-lookup"><span data-stu-id="05cc0-259">The amount is calculated based on, and subtracted from, the total value of the lines in a customer invoice.</span></span> 

<span data-ttu-id="05cc0-260">Для правил выставления счетов **Время и материал** и **Ход выполнения** , вы можете назначать оплачиваемые категории.</span><span class="sxs-lookup"><span data-stu-id="05cc0-260">For **Time and material** and **Progress** billing rules, you can assign chargeable categories.</span></span> <span data-ttu-id="05cc0-261">Оплачиваемые категории указывают транзакции, которые должны быть включены в счета-фактуры клиентов.</span><span class="sxs-lookup"><span data-stu-id="05cc0-261">Chargeable categories indicate the transactions that should be included in customer invoices.</span></span> 

<span data-ttu-id="05cc0-262">Когда вы готовы выставить счет клиенту, сумма счета для проекта рассчитывается на основе правил выставления счетов, и создается предложение счета по проекту.</span><span class="sxs-lookup"><span data-stu-id="05cc0-262">When you are ready to invoice the customer, the amount to invoice for the project is calculated based on the billing rules, and a project invoice proposal is generated.</span></span> 

<span data-ttu-id="05cc0-263">В следующих разделах представлены примеры, показывающие, как настроить правила выставления счетов для проекта и управлять ими.</span><span class="sxs-lookup"><span data-stu-id="05cc0-263">The following sections provide examples that show how to set up and manage billing rules for a project.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a><span data-ttu-id="05cc0-264">Пример: создание правила выставления счетов на основе количества доставленных единиц</span><span class="sxs-lookup"><span data-stu-id="05cc0-264">Example: Create a billing rule that is based on the number of units delivered</span></span>

<span data-ttu-id="05cc0-265">Ваша организация заключает соглашение о проведении пяти учебных занятий для сотрудников заказчика по цене 10 000 за одно занятие.</span><span class="sxs-lookup"><span data-stu-id="05cc0-265">Your organization enters into an agreement to provide a total of five training sessions to a customer’s employees at a cost of 10,000 per training session.</span></span> <span data-ttu-id="05cc0-266">Вы выставляете счет клиенту после каждого занятия.</span><span class="sxs-lookup"><span data-stu-id="05cc0-266">You invoice the customer after each training session.</span></span> 

<span data-ttu-id="05cc0-267">При настройке правил выставления счетов для контракта вы используете следующие значения:</span><span class="sxs-lookup"><span data-stu-id="05cc0-267">When you set up the billing rules for the contract, you use the following values:</span></span>

-   <span data-ttu-id="05cc0-268">Единица доставки — одно обучающее занятие.</span><span class="sxs-lookup"><span data-stu-id="05cc0-268">The unit of delivery is one training session.</span></span>
-   <span data-ttu-id="05cc0-269">Цена за единицу — 10 000 за занятие.</span><span class="sxs-lookup"><span data-stu-id="05cc0-269">The unit price is 10,000 per training session.</span></span>
-   <span data-ttu-id="05cc0-270">Общее количество единиц — пять учебных занятий.</span><span class="sxs-lookup"><span data-stu-id="05cc0-270">The total number of units is five training sessions.</span></span>

<span data-ttu-id="05cc0-271">По завершении одного занятия вы можете создать счет на 10 000 за первую поставленную единицу продукции и отправить счет клиенту.</span><span class="sxs-lookup"><span data-stu-id="05cc0-271">When you have completed one training session, you can create an invoice for 10,000, for the first unit that was delivered, and send the invoice to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a><span data-ttu-id="05cc0-272">Пример: создание правила выставления счетов, основанного на указанном проценте завершения проекта (расчет вручную)</span><span class="sxs-lookup"><span data-stu-id="05cc0-272">Example: Create a billing rule that is based on a specified percentage of project completion (manual calculation)</span></span>

<span data-ttu-id="05cc0-273">Ваша организация, консалтинговая фирма по программному обеспечению, заключает с заказчиком соглашение о разработке части продукта, который разрабатывает заказчик.</span><span class="sxs-lookup"><span data-stu-id="05cc0-273">Your organization, a software consulting firm, enters into an agreement with a customer to develop part of a product that the customer is developing.</span></span> <span data-ttu-id="05cc0-274">Ваша организация соглашается предоставить программный код в течение шести месяцев.</span><span class="sxs-lookup"><span data-stu-id="05cc0-274">Your organization agrees to deliver the software code over a period of six months.</span></span> <span data-ttu-id="05cc0-275">Заказчик соглашается заплатить вашей организации в общей сложности 100 000 за работу.</span><span class="sxs-lookup"><span data-stu-id="05cc0-275">The customer agrees to pay your organization a total of 100,000 for the work.</span></span> <span data-ttu-id="05cc0-276">Вы создаете правило выставления счетов для выставления счета клиенту на основе процента выполненных работ по проекту, как указано в контракте.</span><span class="sxs-lookup"><span data-stu-id="05cc0-276">You create a billing rule to invoice the customer based on the percentage of work that is completed on the project, as specified in the contract.</span></span>

-   <span data-ttu-id="05cc0-277">В конце первого месяца вы встречаетесь с заказчиком, чтобы определить процент выполненных работ.</span><span class="sxs-lookup"><span data-stu-id="05cc0-277">At the end of the first month, you meet with the customer to determine the percentage of work completed.</span></span> <span data-ttu-id="05cc0-278">После того, как вы и заказчик рассмотрите проект, вы решите, что проект выполнен на 15 процентов.</span><span class="sxs-lookup"><span data-stu-id="05cc0-278">After you and the customer review the project, you decide that the project is 15 percent completed.</span></span>
-   <span data-ttu-id="05cc0-279">Вы создаете счет-фактуру для 15 000 (15 процентов от 100 000) и отправляете его клиенту.</span><span class="sxs-lookup"><span data-stu-id="05cc0-279">You create an invoice for 15,000 (15 percent of 100,000) and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a><span data-ttu-id="05cc0-280">Пример: создание правила выставления счетов, основанного на указанном проценте завершения проекта (автоматический расчет)</span><span class="sxs-lookup"><span data-stu-id="05cc0-280">Example: Create a billing rule that is based on a specified percentage of project completion (automatic calculation)</span></span>

<span data-ttu-id="05cc0-281">Ваша организация, занимающаяся разработкой программного обеспечения, соглашается разработать пакет учета заработной платы для клиента на 30 000 человек.</span><span class="sxs-lookup"><span data-stu-id="05cc0-281">Your organization, a software development firm, agrees to develop a payroll accounting package for a customer for 30,000.</span></span> <span data-ttu-id="05cc0-282">Заказчик соглашается заплатить вашей организации на основе процента выполненной работы.</span><span class="sxs-lookup"><span data-stu-id="05cc0-282">The customer agrees to pay your organization based on the percentage of work completed.</span></span> <span data-ttu-id="05cc0-283">По вашим оценкам, стоимость проекта составляет 20 000.</span><span class="sxs-lookup"><span data-stu-id="05cc0-283">You estimate that the project costs are 20,000.</span></span> <span data-ttu-id="05cc0-284">В контракте по проекту указываются категории работ, которые вы используете в процессе выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="05cc0-284">The project contract specifies the categories of work that you use in the billing process.</span></span> <span data-ttu-id="05cc0-285">Вы устанавливаете правила выставления счетов, которые автоматически рассчитывают суммы накладных для процента работы, выполненной для каждой категории.</span><span class="sxs-lookup"><span data-stu-id="05cc0-285">You set up billing rules that automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="05cc0-286">Вы устанавливаете бюджет для каждой категории:</span><span class="sxs-lookup"><span data-stu-id="05cc0-286">You set up a budget for each category:</span></span>

-   <span data-ttu-id="05cc0-287">**Разработка** — стоимость 15 000, выручка 20 000</span><span class="sxs-lookup"><span data-stu-id="05cc0-287">**Development** – Cost of 15,000 and revenue of 20,000</span></span>
-   <span data-ttu-id="05cc0-288">**Установка** — стоимость 5000, выручка 10 000</span><span class="sxs-lookup"><span data-stu-id="05cc0-288">**Installation** – Cost of 5,000 and revenue of 10,000</span></span>

<span data-ttu-id="05cc0-289">Когда вы создаете счет клиента в первый раз, сумма счета автоматически рассчитывается на основе следующей информации:</span><span class="sxs-lookup"><span data-stu-id="05cc0-289">When you create a customer invoice for the first time, the invoice amount is automatically calculated based on the following information:</span></span>

-   <span data-ttu-id="05cc0-290">Через месяц работник проекта отправляет расписание для проекта.</span><span class="sxs-lookup"><span data-stu-id="05cc0-290">After a month, the worker on the project submits a timesheet for the project.</span></span> <span data-ttu-id="05cc0-291">Стоимость рабочего времени 5000 часов на разработку и 1000 часов на установку.</span><span class="sxs-lookup"><span data-stu-id="05cc0-291">The cost of the worker’s hours is 5,000 for development and 1,000 for installation.</span></span> <span data-ttu-id="05cc0-292">Работы по разработке завершены на 33 процента (фактическая стоимость 5000/бюджетная стоимость 15 000), а работы по установке выполнены на 20 процентов (фактическая стоимость 1000/бюджетная стоимость 5000).</span><span class="sxs-lookup"><span data-stu-id="05cc0-292">The development work is 33 percent completed (5,000 actual cost/15,000 budget cost), and the installation work is 20 percent completed (1,000 actual cost/5,000 budget cost).</span></span>
-   <span data-ttu-id="05cc0-293">Сумма счета-фактуры 8667 вычисляется автоматически (33 процента от 20 000 + 20 процентов от 10 000).</span><span class="sxs-lookup"><span data-stu-id="05cc0-293">The invoice amount of 8,667 is automatically calculated (33 percent of 20,000 + 20 percent of 10,000).</span></span>
-   <span data-ttu-id="05cc0-294">Вы создаете счет-фактуру для 8667 и отправляете его клиенту.</span><span class="sxs-lookup"><span data-stu-id="05cc0-294">You create an invoice for 8,667 and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a><span data-ttu-id="05cc0-295">Пример: создание правила выставления счетов на основе согласованных вех</span><span class="sxs-lookup"><span data-stu-id="05cc0-295">Example: Create a billing rule that is based on agreed-upon milestones</span></span>

<span data-ttu-id="05cc0-296">Ваша организация, консалтинговая компания по вопросам управления, соглашается провести исследование рынка потребительского продукта, который заказчик планирует продать.</span><span class="sxs-lookup"><span data-stu-id="05cc0-296">Your organization, a management consulting firm, agrees to conduct market research for a consumer product that the customer plans to sell.</span></span> <span data-ttu-id="05cc0-297">Клиент соглашается использовать ваши услуги в течение трех месяцев начиная с марта и соглашается заплатить вашей организации 50 000.</span><span class="sxs-lookup"><span data-stu-id="05cc0-297">The customer agrees to use your services for a period of three months, starting in March, and agrees to pay your organization 50,000.</span></span> <span data-ttu-id="05cc0-298">У проекта есть три вехи:</span><span class="sxs-lookup"><span data-stu-id="05cc0-298">The project has three milestones:</span></span>

-   <span data-ttu-id="05cc0-299">Веха 1. Сбор данных о потребителях — 31 марта</span><span class="sxs-lookup"><span data-stu-id="05cc0-299">Milestone 1: Collect consumer data – March 31</span></span>
-   <span data-ttu-id="05cc0-300">Веха 2. Анализ данных о потребителях — 30 апреля</span><span class="sxs-lookup"><span data-stu-id="05cc0-300">Milestone 2: Analyze consumer data – April 30</span></span>
-   <span data-ttu-id="05cc0-301">Веха 3. Представление предложения о жизнеспособности продукта — 31 мая</span><span class="sxs-lookup"><span data-stu-id="05cc0-301">Milestone 3: Present a product viability proposal – May 31</span></span>

<span data-ttu-id="05cc0-302">Заказчик соглашается заплатить вашей организации 10 000 за первый этап, 20 000 за второй этап и 20 000 за третий этап.</span><span class="sxs-lookup"><span data-stu-id="05cc0-302">The customer agrees to pay your organization 10,000 for the first milestone, 20,000 for the second milestone, and 20,000 for the third milestone.</span></span> 

<span data-ttu-id="05cc0-303">Создавая контракт по проекту, вы соглашаетесь выставить счет заказчику на основе выполненной вехи.</span><span class="sxs-lookup"><span data-stu-id="05cc0-303">When you set up the project contract, you agree to bill the customer based on the milestone that has been completed.</span></span> <span data-ttu-id="05cc0-304">Настройка правила выставления счетов включает следующие шаги:</span><span class="sxs-lookup"><span data-stu-id="05cc0-304">The billing rule setup includes the following steps:</span></span>

-   <span data-ttu-id="05cc0-305">Определите вехи проекта.</span><span class="sxs-lookup"><span data-stu-id="05cc0-305">Define the project milestones.</span></span>
-   <span data-ttu-id="05cc0-306">Определите сумму, на которую будет выставлен счет клиенту по завершении каждой вехи.</span><span class="sxs-lookup"><span data-stu-id="05cc0-306">Define the amount to invoice the customer when each milestone is completed.</span></span>

<span data-ttu-id="05cc0-307">Когда 31 марта завершается первая веха, вы отмечаете ее как завершенную, а затем создаете счет на 10 000 и отправляете его клиенту.</span><span class="sxs-lookup"><span data-stu-id="05cc0-307">When the first milestone is completed on March 31, you mark the milestone as completed, and then create an invoice for 10,000 and send it to the customer.</span></span> <span data-ttu-id="05cc0-308">Вы не можете создать счет для вехи, пока не отметите веху как завершенную.</span><span class="sxs-lookup"><span data-stu-id="05cc0-308">You can’t create an invoice for a milestone until you have marked the milestone as completed.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a><span data-ttu-id="05cc0-309">Пример: создание правила выставления счетов, основанного на услугах плюс вознаграждение за управление</span><span class="sxs-lookup"><span data-stu-id="05cc0-309">Example: Create a billing rule that is based on services plus a management fee</span></span>

<span data-ttu-id="05cc0-310">Ваша организация, консалтинговая компания по вопросам управления, соглашается провести исследование рынка для оценки жизнеспособности продукта, разрабатываемого клиентом, розничной компанией.</span><span class="sxs-lookup"><span data-stu-id="05cc0-310">Your organization, a management consulting firm, agrees to conduct market research to evaluate the viability of a product that the customer, a retail company, is developing.</span></span> <span data-ttu-id="05cc0-311">В условиях соглашения указано, что вы будете предоставлять услуги трех своих лучших консультантов по вопросам управления, которые будут проводить исследования в соответствии с условиями и временем.</span><span class="sxs-lookup"><span data-stu-id="05cc0-311">The terms of the agreement specify that you will provide the services of your top three management consultants, who will conduct the research on a time-and-materials basis.</span></span> <span data-ttu-id="05cc0-312">Заказчик соглашается платить 100 в час, плюс 10 процентов вознаграждения за консультационные часы, отнесенные к проекту.</span><span class="sxs-lookup"><span data-stu-id="05cc0-312">The customer agrees to pay 100 per hour, plus a 10 percent management fee for the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="05cc0-313">При настройке контракта по проекту создайте правило выставления счетов, чтобы добавить 10-процентное вознаграждение за управление к часам консультаций, взимаемым с проекта.</span><span class="sxs-lookup"><span data-stu-id="05cc0-313">When you set up the project contract, create a billing rule to add a 10 percent management fee to the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="05cc0-314">Когда вы создаете счет для клиента, ему выставляется счет за управление в размере 10 процентов вознаграждения плюс стоимость часов консультации.</span><span class="sxs-lookup"><span data-stu-id="05cc0-314">When you create an invoice for the customer, the customer is billed a 10 percent management fee plus the cost of the consulting hours.</span></span> <span data-ttu-id="05cc0-315">Например, если три консультанта проработали в общей сложности 200 часов над проектом, счет на 22 000 создается на основе следующего расчета:</span><span class="sxs-lookup"><span data-stu-id="05cc0-315">For example, if the three consultants worked a total of 200 hours on the project, an invoice for 22,000 is created based on the following calculation:</span></span>

-   <span data-ttu-id="05cc0-316">200 часов по 100 часов в час = 20 000</span><span class="sxs-lookup"><span data-stu-id="05cc0-316">200 hours at 100 per hour = 20,000</span></span>
-   <span data-ttu-id="05cc0-317">Вознаграждение за управление 10 процентов = 2000</span><span class="sxs-lookup"><span data-stu-id="05cc0-317">10 percent management fee = 2,000</span></span>
-   <span data-ttu-id="05cc0-318">Общая сумма счета = 22 000</span><span class="sxs-lookup"><span data-stu-id="05cc0-318">Total invoice amount = 22,000</span></span>

<span data-ttu-id="05cc0-319">Если сборы облагаются налогом для клиента и вы выбираете налоговую группу в контракте по проекту, налоговая группа автоматически вводится в правило выставления счетов для сборов.</span><span class="sxs-lookup"><span data-stu-id="05cc0-319">If fees are taxable to a customer, and you select a sales tax group in the project contract, the sales tax group is automatically entered in a billing rule for fees.</span></span>

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a><span data-ttu-id="05cc0-320">Пример: создание правила выставления счетов для времени и материалов</span><span class="sxs-lookup"><span data-stu-id="05cc0-320">Example: Create a billing rule for the value of time and materials</span></span>

<span data-ttu-id="05cc0-321">Ваша организация, консалтинговая компания по программному обеспечению, соглашается предоставить пять технических консультантов для работы над проектом разработки программного обеспечения для клиента в течение следующих шести месяцев.</span><span class="sxs-lookup"><span data-stu-id="05cc0-321">Your organization, a software consulting firm, agrees to provide five technical consultants to work on a software development project for a customer for the next six months.</span></span> <span data-ttu-id="05cc0-322">Заказчик соглашается платить 150 за каждый час консультации, плюс стоимость канцелярских принадлежностей.</span><span class="sxs-lookup"><span data-stu-id="05cc0-322">The customer agrees to pay 150 for each consulting hour, plus the cost of office supplies.</span></span> <span data-ttu-id="05cc0-323">Ваша организация отправляет клиенту счет в конце каждого месяца.</span><span class="sxs-lookup"><span data-stu-id="05cc0-323">Your organization sends an invoice to the customer at the end of each month.</span></span> 

<span data-ttu-id="05cc0-324">При оформлении контракта по проекту вы соглашаетесь ежемесячно выставлять заказчику счет за время и материалы по проекту.</span><span class="sxs-lookup"><span data-stu-id="05cc0-324">When you set up the project contract, you agree to bill the customer each month for time and materials on the project.</span></span> <span data-ttu-id="05cc0-325">Вы создаете правило выставления счетов, которое включает следующую информацию:</span><span class="sxs-lookup"><span data-stu-id="05cc0-325">You create a billing rule that includes the following information:</span></span>

-   <span data-ttu-id="05cc0-326">Срок контракта — шесть месяцев.</span><span class="sxs-lookup"><span data-stu-id="05cc0-326">The contract period is six months.</span></span>
-   <span data-ttu-id="05cc0-327">Время консультации рассчитывается как 150 в час.</span><span class="sxs-lookup"><span data-stu-id="05cc0-327">Consulting time is calculated at a rate of 150 per hour.</span></span>
-   <span data-ttu-id="05cc0-328">Счета на канцелярские товары выставляются по себестоимости, и общая стоимость проекта не должна превышать 10 000.</span><span class="sxs-lookup"><span data-stu-id="05cc0-328">Office supplies are invoiced at cost, and the total cost for the project must not exceed 10,000.</span></span>
-   <span data-ttu-id="05cc0-329">Вы создаете счет-фактуру клиента в конце каждого календарного месяца в течение проекта.</span><span class="sxs-lookup"><span data-stu-id="05cc0-329">You create a customer invoice at the end of each calendar month during the project.</span></span>

<span data-ttu-id="05cc0-330">В течение первого месяца консультанты по проекту регистрируют в общей сложности 800 часов.</span><span class="sxs-lookup"><span data-stu-id="05cc0-330">During the first month, a total of 800 hours are recorded by the consultants on the project.</span></span> <span data-ttu-id="05cc0-331">Стоимость канцелярских принадлежностей, внесенных в счет проекта, составляет 2000.</span><span class="sxs-lookup"><span data-stu-id="05cc0-331">The cost of office supplies that are charged to the project is 2,000.</span></span> <span data-ttu-id="05cc0-332">Таким образом, в конце месяца вы создаете счет-фактуру на 122 000, что рассчитывается как 800 часов из расчета 150 часов в час плюс 2000 для канцелярских принадлежностей.</span><span class="sxs-lookup"><span data-stu-id="05cc0-332">Therefore, at the end of the month, you create an invoice for 122,000, which is calculated as 800 hours at 150 per hour, plus 2,000 for office supplies.</span></span>



