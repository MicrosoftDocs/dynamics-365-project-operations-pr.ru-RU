---
title: Настройка ставок себестоимости трудозатрат
description: В этой теме представлена информация о том, как установить ставки стоимости трудозатрат в Project Operations
author: rumant
manager: Annbe
ms.date: 10/12/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 605bf2a578528117a6ef70614a8e5ff5a3fc300c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274789"
---
# <a name="set-up-labor-cost-rates"></a><span data-ttu-id="f9bf1-103">Настройка ставок себестоимости трудозатрат</span><span class="sxs-lookup"><span data-stu-id="f9bf1-103">Set up labor cost rates</span></span>

<span data-ttu-id="f9bf1-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/без запасов_</span><span class="sxs-lookup"><span data-stu-id="f9bf1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="f9bf1-105">В каждом прайс-листе есть набор ставок оплаты труда (цены ролей), которые соответствуют содержанию и сроку действия прайс-листа.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-105">Each price list has a set of labor rates (role prices) that align with the content and date effectivity of the price list.</span></span>

1. <span data-ttu-id="f9bf1-106">Создайте прайс-лист и на вкладке **Цена роли** во вложенной сетке выберите **Создать роль**.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-106">Create a price list and on the **Role Price** tab, in the subgrid, select **New Role**.</span></span>
2. <span data-ttu-id="f9bf1-107">На странице **Быстрое создание** выберите роль и организационное подразделение.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-107">On the **Quick Create** page, select the role and organization unit.</span></span>
3. <span data-ttu-id="f9bf1-108">Введите всю остальную необходимую информацию в поля.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-108">Enter any other required field information.</span></span>

<span data-ttu-id="f9bf1-109">Следующая таблица включает некоторые поля, которые важны при создании ставок оплаты труда в списке себестоимости.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-109">The following table includes some of the fields that are important when creating labor rates on a cost price list.</span></span>

| <span data-ttu-id="f9bf1-110">Поле</span><span class="sxs-lookup"><span data-stu-id="f9bf1-110">Field</span></span> | <span data-ttu-id="f9bf1-111">Размещение</span><span class="sxs-lookup"><span data-stu-id="f9bf1-111">Location</span></span> | <span data-ttu-id="f9bf1-112">Описание:</span><span class="sxs-lookup"><span data-stu-id="f9bf1-112">Description</span></span> | <span data-ttu-id="f9bf1-113">Воздействие на последующие элементы</span><span class="sxs-lookup"><span data-stu-id="f9bf1-113">Downstream impact</span></span> |
| --- | --- | --- | --- |
| <span data-ttu-id="f9bf1-114">Роль</span><span class="sxs-lookup"><span data-stu-id="f9bf1-114">Role</span></span> | <span data-ttu-id="f9bf1-115">Вкладка **Общие** и страницы **Быстрое создание**</span><span class="sxs-lookup"><span data-stu-id="f9bf1-115">**General** tab and **Quick Create** pages</span></span> | <span data-ttu-id="f9bf1-116">Выберите роль, к которой применяется ставка стоимости.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-116">Select the role that the cost rate applies to.</span></span> | <span data-ttu-id="f9bf1-117">Роль во входящей оценке или фактической стоимости будет сопоставлена с этой строкой, чтобы установить стоимость роли по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-117">The role on the incoming estimate or actual will be matched against this line to default the cost of the role.</span></span> |
| <span data-ttu-id="f9bf1-118">Компания распределения ресурсов</span><span class="sxs-lookup"><span data-stu-id="f9bf1-118">Resourcing Company</span></span> | <span data-ttu-id="f9bf1-119">Вкладка **Общие** и страницы **Быстрое создание**</span><span class="sxs-lookup"><span data-stu-id="f9bf1-119">**General** tab and **Quick Create** pages</span></span> | <span data-ttu-id="f9bf1-120">Выберите юридическое лицо, которому назначена роль.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-120">Select the legal entity that the role is assigned to.</span></span> <span data-ttu-id="f9bf1-121">Например, разработчик из Fabrikam India или разработчик из Fabrikam USA.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-121">For example, a developer from Fabrikam India or a developer from Fabrikam USA.</span></span> | <span data-ttu-id="f9bf1-122">Компания распределения ресурсов во входящей оценке или фактическая стоимость будет сопоставлена с этой строкой, чтобы установить ставку стоимости роли по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-122">The resourcing company on the incoming estimate or actual will be matched against this line to default the cost rate of the role.</span></span> |
| <span data-ttu-id="f9bf1-123">Единица распределения ресурсов</span><span class="sxs-lookup"><span data-stu-id="f9bf1-123">Resourcing Unit</span></span> | <span data-ttu-id="f9bf1-124">Вкладка **Общие** и страницы **Быстрое создание**</span><span class="sxs-lookup"><span data-stu-id="f9bf1-124">**General** tab and **Quick Create** pages</span></span> | <span data-ttu-id="f9bf1-125">Выберите организационное подразделение или подразделение компании, из которой будет использоваться эта роль.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-125">Select the organizational unit or division of the company from where this role will be used.</span></span> <span data-ttu-id="f9bf1-126">Например, разработчик из подразделения робототехники компании Fabrikam India или разработчик из подразделения программного обеспечения компании Fabrikam USA.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-126">For example, a developer from the Robotics division of Fabrikam India or a developer from the Software division of Fabrikam USA.</span></span> | <span data-ttu-id="f9bf1-127">Подразделение распределения ресурсов во входящей оценке или фактическая стоимость будет сопоставлена с этой строкой, чтобы установить стоимость роли по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-127">The resourcing unit on the incoming estimate or actual will be matched against this line to default the cost of the role.</span></span> |
| <span data-ttu-id="f9bf1-128">Цена</span><span class="sxs-lookup"><span data-stu-id="f9bf1-128">Price</span></span> | <span data-ttu-id="f9bf1-129">Вкладка **Общие** и страницы **Быстрое создание**</span><span class="sxs-lookup"><span data-stu-id="f9bf1-129">**General** tab and **Quick Create** pages</span></span> | <span data-ttu-id="f9bf1-130">Установите ставку стоимости для комбинации роли, компании распределения ресурсов и подразделения распределения ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-130">Set up the cost rate for the role, resourcing company, and resourcing unit combination.</span></span> <span data-ttu-id="f9bf1-131">Например, разработчик из Fabrikam India стоит 1000 индийских рупий или разработчик из Fabrikam USA стоит 150 долларов США.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-131">For example, a developer from Fabrikam India costs 1000 INR or a developer from Fabrikam USA costs 150 USD.</span></span> | <span data-ttu-id="f9bf1-132">Цена — это ставка затрат, которая по умолчанию основана на стоимости единицы строки входящей оценки или фактических данных для класса транзакций **Время**.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-132">The price is the cost rate that defaults on the per unit cost of the incoming estimate or actual line for the **Time** transaction class.</span></span> |
| <span data-ttu-id="f9bf1-133">Валюта</span><span class="sxs-lookup"><span data-stu-id="f9bf1-133">Currency</span></span> | <span data-ttu-id="f9bf1-134">Вкладка **Общие** и страницы **Быстрое создание**</span><span class="sxs-lookup"><span data-stu-id="f9bf1-134">**General** tab and **Quick Create** pages</span></span> | <span data-ttu-id="f9bf1-135">По умолчанию значение валюты берется из валюты, указанной в заголовке списка себестоимости, но может быть переопределено.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-135">By default, the currency value comes from the currency on the header of the cost price list but can be overridden.</span></span> <span data-ttu-id="f9bf1-136">Например, разработчик из Fabrikam India стоит 1000 индийских рупий.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-136">For example, a developer from Fabrikam India costs 1000 INR.</span></span> <span data-ttu-id="f9bf1-137">Разработчик из Fabrikam USA стоит 150 долларов США.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-137">A developer from Fabrikam USA costs 150 USD.</span></span> | <span data-ttu-id="f9bf1-138">Эта валюта по умолчанию основана на стоимости единицы строки входящей фактической стоимости для класса транзакций **Время**.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-138">This currency defaults on the per unit cost of the incoming actual cost line for the **Time** transaction class.</span></span> <span data-ttu-id="f9bf1-139">В смете проекта стоимость в валюте конвертируется в валюту проекта и отображается в поэтапном представлении сметы по времени.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-139">On a project estimate, the currency value is converted to the project currency and shown on the Time-phased view of the estimate.</span></span> |
| <span data-ttu-id="f9bf1-140">Группа единиц измерения</span><span class="sxs-lookup"><span data-stu-id="f9bf1-140">Unit Schedule</span></span> | <span data-ttu-id="f9bf1-141">Вкладка **Общие** и страницы **Быстрое создание**</span><span class="sxs-lookup"><span data-stu-id="f9bf1-141">**General** tab and **Quick Create** pages</span></span> | <span data-ttu-id="f9bf1-142">По умолчанию для расписания единиц выбрано время, и его нельзя изменить в сущности цены роли, потому что в ней используются экспресс-ставки по единицам времени.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-142">The unit schedule defaults to Time and can't be changed on the Role price entity because it is used express rates by units of time.</span></span> | <span data-ttu-id="f9bf1-143">Это не влияет на последующие элементы.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-143">There is no downstream impact.</span></span> |
| <span data-ttu-id="f9bf1-144">Единица</span><span class="sxs-lookup"><span data-stu-id="f9bf1-144">Unit</span></span> | <span data-ttu-id="f9bf1-145">Вкладка **Общие** и страницы **Быстрое создание**</span><span class="sxs-lookup"><span data-stu-id="f9bf1-145">**General** tab and **Quick Create** pages</span></span> | <span data-ttu-id="f9bf1-146">По умолчанию значение берется из поля **Единицы времени** в заголовке списка себестоимости.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-146">By default, the value comes from the **Time Unit** field on the header of the cost price list.</span></span> <span data-ttu-id="f9bf1-147">Значение можно переопределить.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-147">The value can be overridden.</span></span> <span data-ttu-id="f9bf1-148">Например, разработчик из Fabrikam India стоит 1000 индийских рупий за **Индийский день**.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-148">For example, a developer from Fabrikam India costs 1000 INR per **India Day**.</span></span> <span data-ttu-id="f9bf1-149">Стоимость разработчика из Fabrikam USA составляет 150 долларов США за **День США**.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-149">A developer from Fabrikam USA costs 150 USD per **US Day**.</span></span> | <span data-ttu-id="f9bf1-150">Система использует систему единиц и преобразование в базовые единицы для вычисления затрат на единицу для вычисления цены по умолчанию за единицу во входящей оценке или фактической строке.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-150">The system uses the system of units and conversion in base units to compute a per unit cost to calculate the default price per unit on an incoming estimate or actual line.</span></span> <span data-ttu-id="f9bf1-151">Например, оценка указана за 10 **Индийских дней** работы разработчика из Индии, и единица **Индийский день** определяется как 10 часов.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-151">For example, an estimate is for 10 **India Days** worth of work for a developer from India, and the unit, **India Day** is defined as 10 hours.</span></span> <span data-ttu-id="f9bf1-152">При калькуляции этой строки сметы приложение рассчитывает удельную стоимость в смете как: 1000 индийских рупий/10 часов = 100 индийских рупий за час, которые конвертируются в доллары США и отображаются как удельная стоимость на странице **Оценки проекта**.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-152">When costing that estimate line, the application calculates the unit cost on the estimate as: 1000 INR/ 10 hours = 100 INR per hour which is converted into USD and shown as the unit cost on the **Project Estimates** page.</span></span> |

## <a name="transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity"></a><span data-ttu-id="f9bf1-153">Трансфертное ценообразование и затраты на ресурсы за пределами вашего подразделения или юридического лица</span><span class="sxs-lookup"><span data-stu-id="f9bf1-153">Transfer pricing and costs for resources outside of your division or legal entity</span></span>

<span data-ttu-id="f9bf1-154">В компаниях на основе проектов принято привлекать к проектам сотрудников из разных юридических лиц или подразделений.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-154">In project-based companies, it's common to use employees from different legal entities or divisions on projects.</span></span> <span data-ttu-id="f9bf1-155">Проект может выполняться одним юридическим лицом, но сотрудники или консультанты, которые работают над проектом, могут быть из того же юридического лица или из другого, или может быть сочетание того и другого.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-155">A project can be executed by one legal entity, but the employees or consultants that work on the project could come from the same legal entity or from a different one, or there may be a combination of both.</span></span> <span data-ttu-id="f9bf1-156">В Dynamics 365 Project Operations юридическое лицо, которое отвечает за выполнение проекта, является **Ответственной компанией**, а подразделение, которое отвечает за выполнение, является **Единицей по контракту**.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-156">In Dynamics 365 Project Operations, the legal entity that owns the delivery of the project is the **Owning Company** and the division that owns the delivery is the **Contracting Unit**.</span></span> <span data-ttu-id="f9bf1-157">Другие юридические лица, предоставляющие ресурсы, называются **Компания распределения ресурсов**, и подразделения, которые предоставляют ресурсы, называется **Единица распределения ресурсов**.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-157">Other legal entities that provide resources are the **Resourcing companies** and divisions that provide resources are the **Resourcing Units**.</span></span> <span data-ttu-id="f9bf1-158">В большинстве стран от компаний требуется обеспечить, чтобы юридическое лицо или подразделение, предоставляющее ресурсы, взимало плату с компании-владельца и подрядчика за использование ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-158">In most countries, companies are required to ensure that the resourcing legal entity or division, charge the owning company and the contracting unit for the use of resources.</span></span>

<span data-ttu-id="f9bf1-159">Например, корпорация Fabrikam должна убедиться, что подразделение Fabrikam India-Robotics согласовало тарифную карту с Fabrikam US-Robotics или Fabrikam UK-Robotics.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-159">For example, the Fabrikam corporation must ensure that Fabrikam India-Robotics has a negotiated a cost rate card with Fabrikam US-Robotics or Fabrikam UK-Robotics.</span></span>

<span data-ttu-id="f9bf1-160">Разработчик из подразделения Fabrikam India-Robotic взимает плату 100 долларов США при предоставлении в аренду в Fabrikam US-Robotics и 150 долларов США при предоставлении в аренду Fabrikam UK-Robotics.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-160">A developer from Fabrikam India-Robotic charges $100 when lent to Fabrikam US-Robotics and $150 when lent to Fabrikam U-Robotics.</span></span>

### <a name="set-up-costs-for-outside-resources"></a><span data-ttu-id="f9bf1-161">Настройка значений стоимости для внешних ресурсов</span><span class="sxs-lookup"><span data-stu-id="f9bf1-161">Set up costs for outside resources</span></span>

1. <span data-ttu-id="f9bf1-162">Создайте прайс-лист под названием *Расценки Fabrikam US-Robotics* и установите диапазон дат действия.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-162">Create a cost price list called, *Fabrikam US-Robotics cost rates* and set a date effective range.</span></span>
2. <span data-ttu-id="f9bf1-163">В прайс-листе себестоимости установите ставки, используя информацию из следующей таблицы.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-163">In the cost price list, set up rates using information from the following table.</span></span> 

| <span data-ttu-id="f9bf1-164">Роль</span><span class="sxs-lookup"><span data-stu-id="f9bf1-164">Role</span></span> | <span data-ttu-id="f9bf1-165">Компания распределения ресурсов</span><span class="sxs-lookup"><span data-stu-id="f9bf1-165">Resourcing Company</span></span> | <span data-ttu-id="f9bf1-166">Единица распределения ресурсов</span><span class="sxs-lookup"><span data-stu-id="f9bf1-166">Resourcing Unit</span></span> | <span data-ttu-id="f9bf1-167">Ставка по стоимости</span><span class="sxs-lookup"><span data-stu-id="f9bf1-167">Cost rate</span></span> |
| --- | --- | --- | --- |
| <span data-ttu-id="f9bf1-168">Developer</span><span class="sxs-lookup"><span data-stu-id="f9bf1-168">Developer</span></span> | <span data-ttu-id="f9bf1-169">Fabrikam India</span><span class="sxs-lookup"><span data-stu-id="f9bf1-169">Fabrikam India</span></span> | <span data-ttu-id="f9bf1-170">Fabrikam India-Robotics</span><span class="sxs-lookup"><span data-stu-id="f9bf1-170">Fabrikam India-Robotics</span></span> | <span data-ttu-id="f9bf1-171">100 долларов</span><span class="sxs-lookup"><span data-stu-id="f9bf1-171">$100</span></span> |
| <span data-ttu-id="f9bf1-172">Developer</span><span class="sxs-lookup"><span data-stu-id="f9bf1-172">Developer</span></span> | <span data-ttu-id="f9bf1-173">Fabrikam Philippines</span><span class="sxs-lookup"><span data-stu-id="f9bf1-173">Fabrikam Philippines</span></span> | <span data-ttu-id="f9bf1-174">Fabrikam Philippines-Robotics</span><span class="sxs-lookup"><span data-stu-id="f9bf1-174">Fabrikam Philippines-Robotics</span></span> | <span data-ttu-id="f9bf1-175">90 долларов США</span><span class="sxs-lookup"><span data-stu-id="f9bf1-175">$90</span></span> |
| <span data-ttu-id="f9bf1-176">Developer</span><span class="sxs-lookup"><span data-stu-id="f9bf1-176">Developer</span></span> | <span data-ttu-id="f9bf1-177">Fabrikam US</span><span class="sxs-lookup"><span data-stu-id="f9bf1-177">Fabrikam US</span></span> | <span data-ttu-id="f9bf1-178">Fabrikam US-Robotics</span><span class="sxs-lookup"><span data-stu-id="f9bf1-178">Fabrikam US-Robotics</span></span> | <span data-ttu-id="f9bf1-179">150 долларов США</span><span class="sxs-lookup"><span data-stu-id="f9bf1-179">$150</span></span> |

3. <span data-ttu-id="f9bf1-180">Приложите этот прайс-лист себестоимости к подразделению Fabrikam US-Robotics.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-180">Attach this cost price list to the Fabrikam US-Robotics organization unit.</span></span>

### <a name="set-up-transfer-pricing-for-a-resource-in-the-appropriate-currency"></a><span data-ttu-id="f9bf1-181">Настройка трансфертных цен для ресурса в соответствующей валюте</span><span class="sxs-lookup"><span data-stu-id="f9bf1-181">Set up transfer pricing for a resource in the appropriate currency</span></span> 

<span data-ttu-id="f9bf1-182">В Project Operations цены на ресурсы могут быть установлены в любой валюте.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-182">In Project Operations, resource pricing can be set up in any currency.</span></span> <span data-ttu-id="f9bf1-183">По умолчанию используется валюта, указанная в заголовке прайс-листа, но ее можно изменить.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-183">The currency defaults to what is on the price list header, but can be changed.</span></span>

<span data-ttu-id="f9bf1-184">Используя пример настройки трансфертной цены, информацию можно изменить на:</span><span class="sxs-lookup"><span data-stu-id="f9bf1-184">Using the example for transfer price set up, the information could be changed to:</span></span>

<span data-ttu-id="f9bf1-185">Корпорация Fabrikam должна убедиться, что подразделение Fabrikam India-Robotics согласовало тарифы с Fabrikam US-Robotics или Fabrikam UK-Robotics.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-185">Fabrikam corporation must ensure that Fabrikam India-Robotics has a negotiated a cost rate with Fabrikam US-Robotics or Fabrikam UK-Robotics.</span></span>

<span data-ttu-id="f9bf1-186">Разработчик из подразделения Fabrikam India-Robotic стоит 5000 индийских рупий при предоставлении в аренду в Fabrikam US-Robotics и 5500 индийских рупий при предоставлении в аренду Fabrikam UK-Robotics.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-186">A developer from Fabrikam India-Robotics costs 5000 INR when lent to Fabrikam US-Robotics and 5500 INR when lent to Fabrikam UK-Robotics.</span></span>

<span data-ttu-id="f9bf1-187">В прайс-листе себестоимости для Fabrikam US-Robotics ставки затрат могут быть выражены как:</span><span class="sxs-lookup"><span data-stu-id="f9bf1-187">In the cost price list for Fabrikam US-Robotics, cost rates can be expressed as:</span></span>

| <span data-ttu-id="f9bf1-188">Роль</span><span class="sxs-lookup"><span data-stu-id="f9bf1-188">Role</span></span> | <span data-ttu-id="f9bf1-189">Компания распределения ресурсов</span><span class="sxs-lookup"><span data-stu-id="f9bf1-189">Resourcing Company</span></span> | <span data-ttu-id="f9bf1-190">Себестоимость</span><span class="sxs-lookup"><span data-stu-id="f9bf1-190">Cost</span></span> |
| --- | --- | --- |
| <span data-ttu-id="f9bf1-191">Developer</span><span class="sxs-lookup"><span data-stu-id="f9bf1-191">Developer</span></span> | <span data-ttu-id="f9bf1-192">Fabrikam India</span><span class="sxs-lookup"><span data-stu-id="f9bf1-192">Fabrikam India</span></span> | <span data-ttu-id="f9bf1-193">5000 индийских рупий</span><span class="sxs-lookup"><span data-stu-id="f9bf1-193">5000 INR</span></span> |
| <span data-ttu-id="f9bf1-194">Developer</span><span class="sxs-lookup"><span data-stu-id="f9bf1-194">Developer</span></span> | <span data-ttu-id="f9bf1-195">Fabrikam US</span><span class="sxs-lookup"><span data-stu-id="f9bf1-195">Fabrikam US</span></span> | <span data-ttu-id="f9bf1-196">115 USD</span><span class="sxs-lookup"><span data-stu-id="f9bf1-196">115 USD</span></span> |

<span data-ttu-id="f9bf1-197">В прайс-листе себестоимости для Fabrikam UK-Robotics ставки затрат могут быть выражены как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="f9bf1-197">In the cost price list for Fabrikam UK-Robotics, cost rates can be expressed below:</span></span>

| <span data-ttu-id="f9bf1-198">Роль</span><span class="sxs-lookup"><span data-stu-id="f9bf1-198">Role</span></span> | <span data-ttu-id="f9bf1-199">Компания распределения ресурсов</span><span class="sxs-lookup"><span data-stu-id="f9bf1-199">Resourcing company</span></span> | <span data-ttu-id="f9bf1-200">Себестоимость</span><span class="sxs-lookup"><span data-stu-id="f9bf1-200">Cost</span></span> |
| --- | --- | --- |
| <span data-ttu-id="f9bf1-201">Developer</span><span class="sxs-lookup"><span data-stu-id="f9bf1-201">Developer</span></span> | <span data-ttu-id="f9bf1-202">Fabrikam India</span><span class="sxs-lookup"><span data-stu-id="f9bf1-202">Fabrikam India</span></span> | <span data-ttu-id="f9bf1-203">5500 индийских рупий</span><span class="sxs-lookup"><span data-stu-id="f9bf1-203">5500 INR</span></span> |
| <span data-ttu-id="f9bf1-204">Developer</span><span class="sxs-lookup"><span data-stu-id="f9bf1-204">Developer</span></span> | <span data-ttu-id="f9bf1-205">Fabrikam UK</span><span class="sxs-lookup"><span data-stu-id="f9bf1-205">Fabrikam UK</span></span> | <span data-ttu-id="f9bf1-206">115 GBP</span><span class="sxs-lookup"><span data-stu-id="f9bf1-206">115 GBP</span></span> |

<span data-ttu-id="f9bf1-207">В прайс-листе себестоимости может быть указана ставка оплаты труда в нескольких валютах.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-207">The cost price list can provide labor rates in multiple currencies.</span></span> <span data-ttu-id="f9bf1-208">При создании сметы затрат по проекту Project Operations преобразует эти ставки затрат в валюту проекта и отобразит их пользователю.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-208">When generating a cost estimate on the project, Project Operations will convert these cost rates into the project currency and display it to the user.</span></span> <span data-ttu-id="f9bf1-209">Когда запись времени утверждается и создается фактическая стоимость, фактическая стоимость оценивается в валюте соответствующей строки цены роли в прайс-листе себестоимости.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-209">When a time entry is approved and a cost actual is created, the cost actual is priced in the currency of that matching role price line on the cost price list.</span></span> <span data-ttu-id="f9bf1-210">Фактические затраты на время по одному проекту могут регистрироваться в нескольких валютах.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-210">Cost actuals for time on a single project can be recorded in multiple currencies.</span></span> <span data-ttu-id="f9bf1-211">Однако при сворачивании или суммировании фактических затрат на рабочую силу на уровне проекта Project Operations преобразует все суммы затрат на рабочую силу в валюту проекта, которую пользователь может просмотреть.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-211">However, when rolling up or summarizing the actual labor costs at the project level, Project Operations will convert all labor cost amounts into the project currency, which the user can view.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]