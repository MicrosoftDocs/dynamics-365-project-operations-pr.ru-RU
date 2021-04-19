---
title: Подразделения
description: В этом разделе представлена информация о подразделениях в Dynamics 365 Project Service Automation.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/04/2019
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
ms.openlocfilehash: 89ff652e186601ccdf75d99dc08a4f082e576cb0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291680"
---
# <a name="organizational-units"></a><span data-ttu-id="75d4f-103">Подразделения</span><span class="sxs-lookup"><span data-stu-id="75d4f-103">Organizational units</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="75d4f-104">В Dynamics 365 Project Service Automation подразделение является отдельной группой или подразделением в компании профессиональных услуг, которая использует оплачиваемые ресурсы с нормами затрат.</span><span class="sxs-lookup"><span data-stu-id="75d4f-104">Dynamics 365 Project Service Automation, an organizational unit is a distinct group or division in a professional services company that employs billable resources that have cost rates.</span></span>

<span data-ttu-id="75d4f-105">Для компаний профессиональных услуг, использующих технические ресурсы в различных областях применения или линиях бизнеса, стоимость заполнения роли в одной области деятельности или линии бизнеса может отличаться от стоимости заполнения роли в другой области деятельности или линии бизнеса.</span><span class="sxs-lookup"><span data-stu-id="75d4f-105">For professional services companies that employ technical resources in various practice areas or business lines, the cost to fill a role in one practice area or business line might differ from the cost to fill a role in another practice area or business line.</span></span> <span data-ttu-id="75d4f-106">Концепция подразделения помогает в этом сценарии, создавая способ группировать оплачиваемые роли в отделении компании, которое имеет отдельную структуру издержек для этих ролей.</span><span class="sxs-lookup"><span data-stu-id="75d4f-106">The concept  organizational units helps in this scenario by providing a way to group a set of billable roles in a division of a company that has a distinct cost structure for these roles.</span></span>

## <a name="key-attributes-and-associations-of-organizational-units"></a><span data-ttu-id="75d4f-107">Ключевые атрибуты и связи подразделений</span><span class="sxs-lookup"><span data-stu-id="75d4f-107">Key attributes and associations of organizational units</span></span>

<span data-ttu-id="75d4f-108">В PSA подразделение в PSA имеет конкретную валюту и определенные списки себестоимости.</span><span class="sxs-lookup"><span data-stu-id="75d4f-108">In PSA, an organizational unit in PSA has a specific currency and specific cost price lists.</span></span>

<span data-ttu-id="75d4f-109">Валюта подразделения — это основная валюта, используемая в отслеживании затрат.</span><span class="sxs-lookup"><span data-stu-id="75d4f-109">The currency of an organizational unit is the primary currency that is used to track costs.</span></span>

<span data-ttu-id="75d4f-110">Один или несколько списков себестоимости можно добавлять в каждое подразделение.</span><span class="sxs-lookup"><span data-stu-id="75d4f-110">One or more cost price lists can be attached to each organizational unit.</span></span> <span data-ttu-id="75d4f-111">PSA накладывает следующие ограничения в прайс-листы, которые можно присоединять к подразделению:</span><span class="sxs-lookup"><span data-stu-id="75d4f-111">PSA puts the following limitations on the price lists that can be attached to an organizational unit:</span></span>

- <span data-ttu-id="75d4f-112">Прайс-листы должны быть в валюте подразделения</span><span class="sxs-lookup"><span data-stu-id="75d4f-112">Price lists must be in the currency of the organizational unit</span></span>
- <span data-ttu-id="75d4f-113">Прайс-листы должны быть списками себестоимости</span><span class="sxs-lookup"><span data-stu-id="75d4f-113">Price lists must be of cost price lists</span></span>

<span data-ttu-id="75d4f-114">Кроме того, имеется атрибут для подразделения в сущности ресурса.</span><span class="sxs-lookup"><span data-stu-id="75d4f-114">In addition, there is an attribute for the organizational unit on the Resource entity.</span></span> <span data-ttu-id="75d4f-115">Каждый ресурс может быть назначен только одному подразделению.</span><span class="sxs-lookup"><span data-stu-id="75d4f-115">Each resource can be assigned to one organizational unit.</span></span>

## <a name="roles-of-organizational-units"></a><span data-ttu-id="75d4f-116">Роли подразделений</span><span class="sxs-lookup"><span data-stu-id="75d4f-116">Roles of organizational units</span></span>

<span data-ttu-id="75d4f-117">Подразделение выполняет две роли в PSA:</span><span class="sxs-lookup"><span data-stu-id="75d4f-117">The organizational unit plays two roles in PSA:</span></span>

- <span data-ttu-id="75d4f-118">**Единица по контракту** — подразделение, представляющее группу или подразделение компании, которое в первую очередь отвечает за обеспечение продажи и управление доставкой работы и услуг клиенту.</span><span class="sxs-lookup"><span data-stu-id="75d4f-118">**Contracting unit** – The organizational unit that represents the company group or division that is primarily responsible for winning the sale and managing the delivery of work and services to the customer.</span></span> <span data-ttu-id="75d4f-119">Контрактная единица идентифицируется полем **Единица по контракту** в разделе заголовка страниц **Возможная сделка**, **Предложение с расценками**, **Контракт по проекту** и **Проект**.</span><span class="sxs-lookup"><span data-stu-id="75d4f-119">The contracting unit is identified by the **Contracting Unit** field in the header section of the **Opportunity**, **Quote**, **Project Contract**, and **Project** pages.</span></span>
- <span data-ttu-id="75d4f-120">**Единица распределения ресурсов** — подразделение, которому принадлежит или назначен ресурс.</span><span class="sxs-lookup"><span data-stu-id="75d4f-120">**Resourcing unit** – The organizational unit that a resource belongs to or is assigned to.</span></span> <span data-ttu-id="75d4f-121">Это подразделение может предоставить свои ресурсы для некоторых ролей по техническим заданиям (ТЗ) и проектам, за которые отвечает контрактная единица.</span><span class="sxs-lookup"><span data-stu-id="75d4f-121">This organizational unit can provide its resources for some roles on statements of work (SOWs) and projects that are owned by the contracting unit.</span></span>

> ![Единицы по контракту и единицы распределения ресурсов](media/advanced-1.png)

## <a name="organizational-unit-faqs"></a><span data-ttu-id="75d4f-123">Вопросы и ответы по подразделениям</span><span class="sxs-lookup"><span data-stu-id="75d4f-123">Organizational unit FAQs</span></span>

<span data-ttu-id="75d4f-124">Ниже приведены некоторые наиболее часто задаваемые вопросы о подразделениях:</span><span class="sxs-lookup"><span data-stu-id="75d4f-124">Here are some of the most frequently asked questions about organizational units.</span></span>

### <a name="how-is-the-organizational-unit-entity-in-psa-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a><span data-ttu-id="75d4f-125">Как сущность подразделения в PSA связана с сущностью организации, которая уже существует в Dynamics 365?</span><span class="sxs-lookup"><span data-stu-id="75d4f-125">How is the Organizational Unit entity in PSA related to the Organization entity that already exists in Dynamics 365?</span></span>

<span data-ttu-id="75d4f-126">Сущность организации в Microsoft Dynamics 365 представляет имя глобального экземпляра Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="75d4f-126">The Organization entity in Microsoft Dynamics 365 represents the name of a global Dynamics 365 instance.</span></span> <span data-ttu-id="75d4f-127">Обычно это имя является именем глобального предприятия.</span><span class="sxs-lookup"><span data-stu-id="75d4f-127">This name is usually the name of the global enterprise.</span></span>

<span data-ttu-id="75d4f-128">Сущность подразделения представляет собой группу или подразделение в глобальном предприятии.</span><span class="sxs-lookup"><span data-stu-id="75d4f-128">The Organizational Unit entity represents a group or division in the global enterprise.</span></span> <span data-ttu-id="75d4f-129">Эти группа или подразделения имеют набор ролей и список себестоимости для этих ролей, и эти роли и прайс-лист отличаются от ролей и прайс-листа других групп или отделений на предприятии.</span><span class="sxs-lookup"><span data-stu-id="75d4f-129">This group or division has a set of roles and a cost price list for those roles, and those roles and price list differ from the roles and price list of other groups or divisions in the enterprise.</span></span>

<span data-ttu-id="75d4f-130">При установке PSA создается подразделение по умолчанию на основе организации.</span><span class="sxs-lookup"><span data-stu-id="75d4f-130">When PSA is installed, a default organizational unit is created based on the organization.</span></span> <span data-ttu-id="75d4f-131">Все существующие ресурсы назначены подразделению по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="75d4f-131">All existing resources are assigned to the default organizational unit.</span></span> <span data-ttu-id="75d4f-132">Если какие-либо новые пользователи или ресурсы Active Directory импортированы в Dynamics 365, процесс импорта пользователей назначает их подразделению по умолчанию в PSA.</span><span class="sxs-lookup"><span data-stu-id="75d4f-132">If any new Active Directory users or resources are imported into Dynamics 365, the user import process assigns them to the default organizational unit in PSA.</span></span>
 
### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a><span data-ttu-id="75d4f-133">Чем сущность организационного подразделения отличается от сущности бизнес-подразделения?</span><span class="sxs-lookup"><span data-stu-id="75d4f-133">How does the organizational unit entity differ from the business unit entity?</span></span>

<span data-ttu-id="75d4f-134">В Dynamics 365 сущность бизнес-подразделения является объектом безопасности.</span><span class="sxs-lookup"><span data-stu-id="75d4f-134">In Dynamics 365, the Business Unit entity is a security construct.</span></span> <span data-ttu-id="75d4f-135">Связь пользователя с бизнес-подразделением определяет сущности и записи сущности, к которым пользователь имеет доступ.</span><span class="sxs-lookup"><span data-stu-id="75d4f-135">The association of a user with a business unit determines the entities and entity records that the user has access to.</span></span> <span data-ttu-id="75d4f-136">Она также определяет разрешения (создание, чтение, запись, удаление, добавление, дополнение, назначение или общий доступ), которые пользователь имеет для этих записей сущности.</span><span class="sxs-lookup"><span data-stu-id="75d4f-136">It also determines the permissions (Create, Read, Write, Delete, Append, Append To, Assign, or Share) that the user has for those entity records.</span></span>

<span data-ttu-id="75d4f-137">Сущность подразделения представляет группу или отделение компании, имеющие отдельные нормы затрат для сотрудников, которые назначены им.</span><span class="sxs-lookup"><span data-stu-id="75d4f-137">The Organizational Unit entity represents a company group or division that has distinct cost rates for employees that are assigned to it.</span></span> <span data-ttu-id="75d4f-138">Связь ресурса с подразделением определяет стоимость ресурса во взаимодействии проекта.</span><span class="sxs-lookup"><span data-stu-id="75d4f-138">The association of a resource with an organizational unit determines the resource's cost to a project engagement.</span></span>

<span data-ttu-id="75d4f-139">При внедрении Dynamics 365 оптимизируйте авторизацию безопасности для иерархии бизнес-подразделений и назначение пользователей для бизнес-подразделений.</span><span class="sxs-lookup"><span data-stu-id="75d4f-139">When you implement Dynamics 365, optimize security authorization for the hierarchy of business units and the assignment of users to business units.</span></span> <span data-ttu-id="75d4f-140">Назначьте всех пользователей, которые должны обычно получать доступ к тому же набору записей, в одно бизнес-подразделение.</span><span class="sxs-lookup"><span data-stu-id="75d4f-140">Assign all users who must typically access the same set of records to the same business unit.</span></span> <span data-ttu-id="75d4f-141">Подразделение не влияет на авторизацию безопасности или доступ.</span><span class="sxs-lookup"><span data-stu-id="75d4f-141">The organizational unit has no effect on security authorization or access.</span></span>

#### <a name="example-of-organizational-units-and-business-units"></a><span data-ttu-id="75d4f-142">Пример организационных подразделений и бизнес-подразделений</span><span class="sxs-lookup"><span data-stu-id="75d4f-142">Example of organizational units and business units</span></span>

<span data-ttu-id="75d4f-143">Contoso, Ltd. успешно использует технологию Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="75d4f-143">Contoso, Ltd. has a thriving Microsoft technology practice.</span></span> <span data-ttu-id="75d4f-144">Дементий и Елизавета оба являются разработчиками на C\#, но Елизавета находится в США, тогда как Дементий — в Индии.</span><span class="sxs-lookup"><span data-stu-id="75d4f-144">Prakash and Tricia are both C\# developers, but Tricia is in the United States, whereas Prakash is in India.</span></span> <span data-ttu-id="75d4f-145">Для большинства взаимодействий проекта требуются ресурсы из Contoso India и Contoso US, и для Дементия, и для Елизаветы требуется одинаковый уровень доступа безопасности к проектам в этой области деятельности.</span><span class="sxs-lookup"><span data-stu-id="75d4f-145">Most of the project engagements require resources from Contoso India and Contoso US, and Prakash and Tricia require the same level of security access to projects in this practice area.</span></span> <span data-ttu-id="75d4f-146">Однако стоимость разработчиков из Contoso India существенно отличается от стоимости разработчиков из Contoso US.</span><span class="sxs-lookup"><span data-stu-id="75d4f-146">However, the cost of developers from Contoso India differs significantly from the cost of developers from Contoso US.</span></span>

<span data-ttu-id="75d4f-147">Ниже приведен оптимальный способ дизайна для данного сценария с помощью Dynamics 365 и PSA.</span><span class="sxs-lookup"><span data-stu-id="75d4f-147">Here is an optimal way to design for this scenario by using Dynamics 365 and PSA.</span></span>

1. <span data-ttu-id="75d4f-148">Создайте использование технологии Майкрософт в виде бизнес-подразделения и свяжите с ним Дементия и Елизавету.</span><span class="sxs-lookup"><span data-stu-id="75d4f-148">Create the Microsoft technology practice as a business unit, and associate Prakash and Tricia with it.</span></span> <span data-ttu-id="75d4f-149">Таким образом, можно гарантировать, что оба сотрудника имеют одинаковый уровень доступа безопасности к любым проектам в этой области деятельности.</span><span class="sxs-lookup"><span data-stu-id="75d4f-149">In this way, you help guarantee that both employees have the same level of security access to any projects in that practice area.</span></span> <span data-ttu-id="75d4f-150">Они смогут проверять ход выполнения и сообщать о времени, затратах и обновлениях задач.</span><span class="sxs-lookup"><span data-stu-id="75d4f-150">They both will be able to check progress and report time, expenses, and task updates.</span></span> 
2. <span data-ttu-id="75d4f-151">Создайте два организационных подразделения, чтобы правильно отражать затраты на проект.</span><span class="sxs-lookup"><span data-stu-id="75d4f-151">Create two organizational units to hel guarantee that the cost to the project is correctly reflected.</span></span> 
3. <span data-ttu-id="75d4f-152">Свяжите Елизавету с Contoso US и свяжите Дементия с Contoso India.</span><span class="sxs-lookup"><span data-stu-id="75d4f-152">Associate Tricia wtih Contoso US and associate Prakash with Contoso India.</span></span>
4. <span data-ttu-id="75d4f-153">Назначьте соответствующие списки себестоимости обоим организационным подразделениям.</span><span class="sxs-lookup"><span data-stu-id="75d4f-153">Assign appropriate cost price lists to both organizational units.</span></span> <span data-ttu-id="75d4f-154">Таким образом можно гарантировать, что затраты, которые записываются по проекту для Дементия и Елизаветы, точно отражаются различие в стоимости между Contoso US и Contoso India.</span><span class="sxs-lookup"><span data-stu-id="75d4f-154">TIn this way, you help guarantee that the costs that are recorded on the project for Prakash and Tricia accurately reflect the difference in costs between Contoso US and Contoso India.</span></span>

### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a><span data-ttu-id="75d4f-155">Связаны ли подразделения с территориями сбыта в Dynamics 365?</span><span class="sxs-lookup"><span data-stu-id="75d4f-155">Are organizational units related to sales territories in Dynamics 365?</span></span>

<span data-ttu-id="75d4f-156">Нет никакой связи или отношений между территориями сбыта и подразделениями.</span><span class="sxs-lookup"><span data-stu-id="75d4f-156">There is no association or relationship between sales territories and organizational units.</span></span> <span data-ttu-id="75d4f-157">Территория сбыта — это обычно географический регион, в котором происходят продажи.</span><span class="sxs-lookup"><span data-stu-id="75d4f-157">A sales territory is typically a geographical area where sales occur.</span></span> <span data-ttu-id="75d4f-158">Прайс-лист продаж можно связать с каждой территорией сбыта.</span><span class="sxs-lookup"><span data-stu-id="75d4f-158">A sales price list can be associated with each sales territory.</span></span>

<span data-ttu-id="75d4f-159">Организационное подразделение является внутренней группой или отделением в компании, которое отслеживает затраты для набора ролей, которые они продают другим отделениям или внешним клиентам.</span><span class="sxs-lookup"><span data-stu-id="75d4f-159">An organizational unit is an internal group or division in the company that tracks costs for a set of roles that it sells to other divisions or to external customers.</span></span>

#### <a name="example-of-organizational-units-and-sales-territories"></a><span data-ttu-id="75d4f-160">Пример организационных подразделений и территорий сбыта</span><span class="sxs-lookup"><span data-stu-id="75d4f-160">Example of organizational units and sales territories</span></span>

<span data-ttu-id="75d4f-161">У компании Contoso, Ltd. есть два центра разработки: Contoso US и Contoso India.</span><span class="sxs-lookup"><span data-stu-id="75d4f-161">Contoso, Ltd. has two development centers: Contoso US and Contoso India.</span></span> <span data-ttu-id="75d4f-162">Стоимость ресурсов существенно отличается между этими двумя центрами разработки.</span><span class="sxs-lookup"><span data-stu-id="75d4f-162">Costs of resources differ greatly between these two development centers.</span></span>

<span data-ttu-id="75d4f-163">Contoso продает свои ИТ-услуги на многих международных рынках, такие как Латинская Америка, Северная Америка, Азиатско-Тихоокеанский регион, Западная Европа и Ближний Восток.</span><span class="sxs-lookup"><span data-stu-id="75d4f-163">Contoso sells its IT services in many international markets, such as Latin America, North America, Asia-Pacific, Western Europe, and the Middle East.</span></span> <span data-ttu-id="75d4f-164">Ставки по счетам для одних и тех же ролей проекта могут широко варьироваться на этих рынках.</span><span class="sxs-lookup"><span data-stu-id="75d4f-164">Bill rates for the same project roles can vary widely across these markets.</span></span>

<span data-ttu-id="75d4f-165">Contoso US и Contoso India должны быть настроены как организационные единицы, и каждая организационная единица должна иметь собственный список себестоимости.</span><span class="sxs-lookup"><span data-stu-id="75d4f-165">Contoso US and Contoso India should be set up as organizational units, and each organizational unit should have its own cost price list.</span></span> <span data-ttu-id="75d4f-166">Азиатско-Тихоокеанский регион, Латинская Америка, Северная Америка, Западная Европа и Ближний Восток должны быть настроены как территории сбыта, и каждая территория сбыта должна иметь собственный прайс-лист продаж.</span><span class="sxs-lookup"><span data-stu-id="75d4f-166">Asia-Pacific, Latin America, North America, Western Europe, and the Middle East should be set up as sales territories, and each sales territory should have its own sales price list.</span></span>

### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a><span data-ttu-id="75d4f-167">Почему имеется ограничение на связь прайс-листов с подразделениями?</span><span class="sxs-lookup"><span data-stu-id="75d4f-167">Why is there a restriction on the association of price lists with organizational units?</span></span> 

<span data-ttu-id="75d4f-168">Цена продажи обычно уникальная для географических регионов или рынков, на которых продаются услуги.</span><span class="sxs-lookup"><span data-stu-id="75d4f-168">Sales pricing is usually unique to the geographical areas or markets where services are sold.</span></span> <span data-ttu-id="75d4f-169">Внутренние отделы компании обычно не имеют собственных продажных цен для идентичного типа услуг.</span><span class="sxs-lookup"><span data-stu-id="75d4f-169">Internal divisions of a company don't usually have their own sales pricing for the same type of services.</span></span> <span data-ttu-id="75d4f-170">Однако внутренние отделения имеют различную себестоимость проданных товаров (COGS), в зависимости от навыков сотрудников и состояния рынка труда региона, где они работают.</span><span class="sxs-lookup"><span data-stu-id="75d4f-170">However, internal divisions have a different cost of goods sold (COGS), depending on the skills of the people that they employ and the labor conditions of the region where they operate.</span></span> <span data-ttu-id="75d4f-171">Поскольку организационные подразделения моделируют внутренние отделы компании, их могут иметь только списки себестоимости.</span><span class="sxs-lookup"><span data-stu-id="75d4f-171">Because organizational units are modeled as internal divisions of a company, they can have only cost price lists.</span></span>

### <a name="why-cant-we-associate-sales-price-lists-to-organizational-units"></a><span data-ttu-id="75d4f-172">Почему мы не можем связать прайс-листы продаж с подразделениями?</span><span class="sxs-lookup"><span data-stu-id="75d4f-172">Why can’t we associate sales price lists to organizational units?</span></span>

<span data-ttu-id="75d4f-173">В PSA прайс-листы продаж можно связать с клиентами и территориями сбыта.</span><span class="sxs-lookup"><span data-stu-id="75d4f-173">In PSA, sales price lists can be associated with customers and sales territories.</span></span> <span data-ttu-id="75d4f-174">Транзакционные сущности, такие как возможная сделка, предложение, контракт по проекту и проект, используют прайс-листы продажи, которые присоединены к учетной записи клиента или территории сбыта для определения ставок по счету и потенциального дохода по взаимодействию проекта.</span><span class="sxs-lookup"><span data-stu-id="75d4f-174">Transactional entities like Opportunity, Quote, Project Contract, and Project use sales price lists that are attached to the customer account or the sales territory to determine bill rates and potential revenue on the project engagement.</span></span>

<span data-ttu-id="75d4f-175">Списки себестоимости связаны с подразделениями.</span><span class="sxs-lookup"><span data-stu-id="75d4f-175">Cost price lists are associated with organizational units.</span></span> <span data-ttu-id="75d4f-176">Транзакционные сущности, такие как возможная сделка, предложение, контракт по проекту и проект, используют списки себестоимости, прикрепленные к единице по контракту, для определения затрат на взаимодействие по проекту.</span><span class="sxs-lookup"><span data-stu-id="75d4f-176">Transactional entities like Opportunity, Quote, Project Contract, and Project use cost price lists that are attached to the contracting unit to determine costs to a project engagement.</span></span>

### <a name="are-organizational-units-hierarchical-in-psa"></a><span data-ttu-id="75d4f-177">Являются ли подразделения иерархическими в PSA?</span><span class="sxs-lookup"><span data-stu-id="75d4f-177">Are organizational units hierarchical in PSA?</span></span>

<span data-ttu-id="75d4f-178">Нет.</span><span class="sxs-lookup"><span data-stu-id="75d4f-178">No.</span></span> <span data-ttu-id="75d4f-179">В текущем выпуске PSA подразделения не являются иерархическими.</span><span class="sxs-lookup"><span data-stu-id="75d4f-179">In the current release of PSA, organizational units are not hierarchical.</span></span> <span data-ttu-id="75d4f-180">Поэтому нельзя:</span><span class="sxs-lookup"><span data-stu-id="75d4f-180">This means that you can’t:</span></span>

- <span data-ttu-id="75d4f-181">Настроить схему для себестоимости по умолчанию, которая распространяется вверх по иерархии.</span><span class="sxs-lookup"><span data-stu-id="75d4f-181">Configure a pattern for defaulting cost prices that traverses up a hierarchy.</span></span> 
- <span data-ttu-id="75d4f-182">Сообщать о доходах или затратах, свернутых по разным уровням иерархии подразделений.</span><span class="sxs-lookup"><span data-stu-id="75d4f-182">Report revenue or cost rolled up at different levels of the organizational unit hierarchy.</span></span>

### <a name="were-a-big-multinational-firm-with-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-make-the-best-use-of-the-organizational-unit-concept-in-this-version-of-the-project-service-app"></a><span data-ttu-id="75d4f-183">Мы большая многонациональная фирма со сложной многоуровневой иерархией центров затрат, отделений и офисов выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="75d4f-183">We're a big multinational firm with a complex, multilevel hierarchy of cost centers, divisions, and billing offices.</span></span> <span data-ttu-id="75d4f-184">Как мы можем оптимально использовать понятие подразделения в этой версии приложения Project Service?</span><span class="sxs-lookup"><span data-stu-id="75d4f-184">How can we make the best use of the organizational unit concept in this version of the Project Service app?</span></span>

<span data-ttu-id="75d4f-185">При наличии сложной иерархии центров затрат, отделений, офисов выставления счетов и т. д. настройте листовые узлы этой иерархии как отдельные подразделения.</span><span class="sxs-lookup"><span data-stu-id="75d4f-185">When you have a complex hierarchy of cost centers, divisions, billing offices, etc., set up the leaf nodes of that hierarchy as distinct organizational units.</span></span>
<span data-ttu-id="75d4f-186">Следующий пример показывает типичную иерархию:</span><span class="sxs-lookup"><span data-stu-id="75d4f-186">The following example shows a typical hierarchy:</span></span>

<span data-ttu-id="75d4f-187">**Contoso India**</span><span class="sxs-lookup"><span data-stu-id="75d4f-187">**Contoso India**</span></span>

  - <span data-ttu-id="75d4f-188">Работа с SAP</span><span class="sxs-lookup"><span data-stu-id="75d4f-188">SAP Practice</span></span> 

    - <span data-ttu-id="75d4f-189">Технические консультанты</span><span class="sxs-lookup"><span data-stu-id="75d4f-189">Technical Consultants</span></span> 
    - <span data-ttu-id="75d4f-190">Функциональные консультанты</span><span class="sxs-lookup"><span data-stu-id="75d4f-190">Functional Consultants</span></span> 
    
  - <span data-ttu-id="75d4f-191">Работа с технологиями Microsoft</span><span class="sxs-lookup"><span data-stu-id="75d4f-191">Microsoft Technology Practice</span></span> 

    - <span data-ttu-id="75d4f-192">Технические консультанты</span><span class="sxs-lookup"><span data-stu-id="75d4f-192">Technical Consultants</span></span>
    - <span data-ttu-id="75d4f-193">Функциональные консультанты</span><span class="sxs-lookup"><span data-stu-id="75d4f-193">Functional Consultants</span></span> 
    
<span data-ttu-id="75d4f-194">**Contoso US**</span><span class="sxs-lookup"><span data-stu-id="75d4f-194">**Contoso US**</span></span>

 - <span data-ttu-id="75d4f-195">Работа с SAP</span><span class="sxs-lookup"><span data-stu-id="75d4f-195">SAP Practice</span></span> 

    - <span data-ttu-id="75d4f-196">Технические консультанты</span><span class="sxs-lookup"><span data-stu-id="75d4f-196">Technical Consultants</span></span> 
    - <span data-ttu-id="75d4f-197">Функциональные консультанты</span><span class="sxs-lookup"><span data-stu-id="75d4f-197">Functional Consultants</span></span> 
    
 - <span data-ttu-id="75d4f-198">Работа с технологиями Microsoft</span><span class="sxs-lookup"><span data-stu-id="75d4f-198">Microsoft Technology Practice</span></span> 

    - <span data-ttu-id="75d4f-199">Технические консультанты</span><span class="sxs-lookup"><span data-stu-id="75d4f-199">Technical Consultants</span></span> 
    - <span data-ttu-id="75d4f-200">Функциональные консультанты</span><span class="sxs-lookup"><span data-stu-id="75d4f-200">Functional Consultants</span></span> 
 
<span data-ttu-id="75d4f-201">Если ваша иерархия аналогично, ее необходимо определить как плоский список, как показано здесь:</span><span class="sxs-lookup"><span data-stu-id="75d4f-201">If your hierarchy is similar, you must set it up as a flat list, as shown here:</span></span>
- <span data-ttu-id="75d4f-202">Contoso India - Работа с SAP - Технические консультанты</span><span class="sxs-lookup"><span data-stu-id="75d4f-202">Contoso India - SAP Practice - Technical Consultants</span></span> 
- <span data-ttu-id="75d4f-203">Contoso India - Работа с SAP - Функциональные консультанты</span><span class="sxs-lookup"><span data-stu-id="75d4f-203">Contoso India - SAP Practice - Functional Consultants</span></span>       
- <span data-ttu-id="75d4f-204">Contoso India - Работа с технологиями Microsoft - Функциональные консультанты</span><span class="sxs-lookup"><span data-stu-id="75d4f-204">Contoso India - Microsoft Technology Practice Functional Consultants</span></span> 
- <span data-ttu-id="75d4f-205">Contoso India - Работа с технологиями Microsoft - Функциональные консультанты</span><span class="sxs-lookup"><span data-stu-id="75d4f-205">Contoso India - Microsoft Technology Practice Functional Consultants</span></span> 
- <span data-ttu-id="75d4f-206">Contoso US - Работа с SAP - Технические консультанты</span><span class="sxs-lookup"><span data-stu-id="75d4f-206">Contoso US - SAP Practice - Technical Consultants</span></span>  
- <span data-ttu-id="75d4f-207">Contoso US - Работа с SAP - Функциональные консультанты</span><span class="sxs-lookup"><span data-stu-id="75d4f-207">Contoso US - SAP Practice - Functional Consultants</span></span>  
- <span data-ttu-id="75d4f-208">Contoso US - Работа с технологиями Microsoft - Технические консультанты</span><span class="sxs-lookup"><span data-stu-id="75d4f-208">Contoso US - Microsoft Technology Practice - Technical Consultants</span></span> 
- <span data-ttu-id="75d4f-209">Contoso US - Работа с технологиями Microsoft - Функциональные консультанты</span><span class="sxs-lookup"><span data-stu-id="75d4f-209">Contoso US - Microsoft Technology Practice - Functional Consultants</span></span>

### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-organizational-unit-concept-in-the-current-version-of-psa"></a><span data-ttu-id="75d4f-210">Мы небольшая компания профессиональных услуг, которая работает как только одно подразделение.</span><span class="sxs-lookup"><span data-stu-id="75d4f-210">We're a small professional services company that operates as only one division.</span></span> <span data-ttu-id="75d4f-211">Как мы можем оптимально использовать концепцию подразделений в текущей версии PSA?</span><span class="sxs-lookup"><span data-stu-id="75d4f-211">How can we best use the organizational unit concept in the current version of PSA?</span></span>

<span data-ttu-id="75d4f-212">Если ваша компания работает как одна единица, которая имеет один список себестоимости, необязательно настраивать какие-либо подразделения.</span><span class="sxs-lookup"><span data-stu-id="75d4f-212">If your company operates as one unit that has one cost price list, you don't have to set up any organizational units.</span></span> <span data-ttu-id="75d4f-213">Во время установки PSA Dynamics 365 создает одно подразделение по умолчанию, имеющее то же имя, что и организация.</span><span class="sxs-lookup"><span data-stu-id="75d4f-213">During PSA installation, Dynamics 365 creates one default organizational unit that has the same name as the organization.</span></span> <span data-ttu-id="75d4f-214">По умолчанию все пользователи назначаются этому подразделению.</span><span class="sxs-lookup"><span data-stu-id="75d4f-214">By default, all users are assigned to this organizational unit.</span></span> <span data-ttu-id="75d4f-215">Когда система требуется, чтобы было выбрано подразделение, это подразделение выбирается по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="75d4f-215">Whenever the system requires that an organizational unit be selected, this organizational unit is selected by default.</span></span>

### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract-what-is-the-default-contracting-unit"></a><span data-ttu-id="75d4f-216">Когда проект создается из строки предложения с расценками проекта или строки контракта по проекту, контрактная единица по умолчанию берется из предложения с расценками или контракта по проекту.</span><span class="sxs-lookup"><span data-stu-id="75d4f-216">When a project is created from a quote or project contract line, the default contracting unit comes from the quote or project contract.</span></span> <span data-ttu-id="75d4f-217">При проект создается до сущностей продаж, таких как предложение с расценками или контракт по проекту, что будет контрактной единицей по умолчанию?</span><span class="sxs-lookup"><span data-stu-id="75d4f-217">If a project is created before sales entities such as quote or project contract, what is the default contracting unit?</span></span>

<span data-ttu-id="75d4f-218">Когда проект создается самостоятельно, контрактная единица проекта по умолчанию основана на создавшем его пользователе.</span><span class="sxs-lookup"><span data-stu-id="75d4f-218">When a project is created on its own, the default contracting unit of the project is based on the user who creates it.</span></span> <span data-ttu-id="75d4f-219">Этот пользователь также будет руководителем проекта по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="75d4f-219">That user is also the default project manager.</span></span> <span data-ttu-id="75d4f-220">Если проект сопоставлен сущности продаж, такой как предложение с расценками или контракт по проекту, то контрактная единица по проекту основана на этой сущности продаж.</span><span class="sxs-lookup"><span data-stu-id="75d4f-220">If the project is mapped to a sales entity such as a quote or project contract, the contracting unit on the project is based on the sales entity instead.</span></span> <span data-ttu-id="75d4f-221">В этом случае оценки проекта могут быть пересчитаны, поскольку список себестоимости используется для вычисления изменений оценки стоимости, если контрактная единица изменена.</span><span class="sxs-lookup"><span data-stu-id="75d4f-221">In this case, project estimates might be recalculated, because the cost price list is used to calculate the cost estimate changes if the contracting unit is changed.</span></span> <span data-ttu-id="75d4f-222">Прайс-лист по продажам используется для вычисления оценок продаж, которые будут изменены, чтобы они были синхронизированы с прайс-листом проекта в предложении с расценками.</span><span class="sxs-lookup"><span data-stu-id="75d4f-222">The sales price list is used to calculate the sales estimates that will be changed so that they are in sync with the project price list on the quote.</span></span>

<span data-ttu-id="75d4f-223">Поля **Единица по контракту** и **Валюта** в проекта заблокированы для редактирования, поскольку они должны быть синхронизированы со значениями в сущности продаж (предложение с расценками или контракт по проекту), с которыми сопоставлен проект.</span><span class="sxs-lookup"><span data-stu-id="75d4f-223">The **Contracting Unit** and **Currency** fields on the project are locked for editing, because they must be in sync with the values on the sales entity (quote or project contract) that the project is mapped to.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]