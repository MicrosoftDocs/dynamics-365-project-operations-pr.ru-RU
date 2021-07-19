---
title: Домашняя страница измерений ценообразования и стоимости
description: В этом разделе содержатся обзор измерений ценообразования.
author: rumant
ms.custom:
- dyn365-projectservice
- intro-internal
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 5c8c28839f5e7b3259afbea4ab400d0c4fca95fd
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368897"
---
# <a name="pricing-and-costing-dimensions-home-page"></a><span data-ttu-id="83312-103">Домашняя страница измерений ценообразования и стоимости</span><span class="sxs-lookup"><span data-stu-id="83312-103">Pricing and costing dimensions home page</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="83312-104">На измерения, используемые для установки ценообразования и себестоимости трудозатрат в организациях на основе проекта влияют следующие атрибуты:</span><span class="sxs-lookup"><span data-stu-id="83312-104">The dimensions used to set labor pricing and costing in project-based organizations are influenced by the following attributes:</span></span>

- <span data-ttu-id="83312-105">Люди, выполняющие работу, аналогичны по их опыту, роли или географическому положению</span><span class="sxs-lookup"><span data-stu-id="83312-105">People doing work similar to their experience, role, or geography</span></span>
- <span data-ttu-id="83312-106">Работа, которую предстоит выполнять, аналогична по своей сложности или времени суток</span><span class="sxs-lookup"><span data-stu-id="83312-106">Work to be performed similar to its complexity or time of day</span></span>

<span data-ttu-id="83312-107">Учитывая типичный характер этих атрибутов работы и людей, необходимых для выполнения работы, в Project Service Automation доступны два типа значений измерений ценообразования:</span><span class="sxs-lookup"><span data-stu-id="83312-107">Given the typical nature of these attrubutes of the work and the people required to perform the work, there are two types of pricing dimension values available in Project Service Automation:</span></span> 

- <span data-ttu-id="83312-108">**Наборы параметров** — атрибуты, являющиеся фиксированными перечислениями для набора значений.</span><span class="sxs-lookup"><span data-stu-id="83312-108">**Option sets** - Attributes that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="83312-109">**Значения на основе сущностей** — атрибуты, которые могут иметь разнообразный набор значений, которые конечны, но могут изменяться со временем.</span><span class="sxs-lookup"><span data-stu-id="83312-109">**Entity-based values** - Attributes that can have a varied set of values that are finite but can change over time.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="83312-110">Измерения цен</span><span class="sxs-lookup"><span data-stu-id="83312-110">Pricing dimensions</span></span>

<span data-ttu-id="83312-111">PSA поставляется с набором по умолчанию измерений ценообразования.</span><span class="sxs-lookup"><span data-stu-id="83312-111">PSA ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="83312-112">Их можно просматривать, выбрав **Project Service** > **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="83312-112">You can view these by going to **Project Service** > **Parameters**.</span></span> <span data-ttu-id="83312-113">В записи параметров на вкладке **Сумма на основе измерения цен** убедитесь, что роль **msdyn_resourcecategory** и подразделение распределения ресурсов **msdyn_organizationalunit** содержат поля **Применимо к продажам** и **Применимо к стоимости**, в которых задано значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="83312-113">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="83312-114">Это позволит настроить цену и стоимость для каждого сочетания роли и подразделения.</span><span class="sxs-lookup"><span data-stu-id="83312-114">This will allow you to set up the price and cost for each role and organizational unit combination.</span></span>

![Снимок экрана параметров Project Service с выделенным полем "Применимо к продажам"](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> <span data-ttu-id="83312-116">При вы использовали готовые поля роли и подразделение в качестве измерения ценообразования до версии 3 PSA, не будет никаких заметных изменений.</span><span class="sxs-lookup"><span data-stu-id="83312-116">If you have been the using out-of-the box fields of role and organizational unit as pricing dimensions prior to version 3 of PSA, there will not be any observable change.</span></span> <span data-ttu-id="83312-117">Вы можете продолжить использовать Project Service, как обычно.</span><span class="sxs-lookup"><span data-stu-id="83312-117">You can continue to use Project Service as usual.</span></span> 

<span data-ttu-id="83312-118">Если необходима задавать цену или стоимость ваших ресурсов с помощью дополнительных атрибутов, можно создать настраиваемые поля, сущности и измерения.</span><span class="sxs-lookup"><span data-stu-id="83312-118">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="83312-119">Чтобы получить дополнительные сведения, см. следующие разделы, однако обратите внимание, что необходимо выполнять процедуры в указанном ниже порядке:</span><span class="sxs-lookup"><span data-stu-id="83312-119">For more information, see the following topics, however note that you must complete the procedures in the order listed below:</span></span>

- [<span data-ttu-id="83312-120">Создание настраиваемых полей и сущностей</span><span class="sxs-lookup"><span data-stu-id="83312-120">Create custom fields and entities</span></span>](create-custom-fields-entities.md)
- [<span data-ttu-id="83312-121">Добавление настраиваемых полей к настройке цены и транзакционным сущностям</span><span class="sxs-lookup"><span data-stu-id="83312-121">Add custom fields to price setup and transactional entities</span></span>](field-references.md)
- [<span data-ttu-id="83312-122">Создание настраиваемых полей в качестве измерений цен</span><span class="sxs-lookup"><span data-stu-id="83312-122">Set up custom fields as pricing dimensions</span></span>](set-up-pricing-dimensions.md)
- [<span data-ttu-id="83312-123">Обновление атрибутов подключаемых модулей для включения новых измерений ценообразования</span><span class="sxs-lookup"><span data-stu-id="83312-123">Update plug-in attributes to include new pricing dimensions</span></span>](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a><span data-ttu-id="83312-124">Задание цены времени сотрудников</span><span class="sxs-lookup"><span data-stu-id="83312-124">Pricing human resource time</span></span>
<span data-ttu-id="83312-125">Порядок задания цены времени сотрудников в организация часто является стратегически важным фактором, который напрямую влияет на доходность организации.</span><span class="sxs-lookup"><span data-stu-id="83312-125">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="83312-126">Работайте с финансовыми рабочими группами и практическими руководителями, когда ваша организация готова определить, как требуется настроить тарифы выставления счетов и нормы затрат для времени человеческих ресурсов.</span><span class="sxs-lookup"><span data-stu-id="83312-126">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="83312-127">Другие соображения для ценообразования включают, требуется ли повторно использовать поля или сущности, которые в настоящее время не являются измерениями ценообразования, но применяются как измерения ценообразования в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="83312-127">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="83312-128">Такие поля, как **Категория проводки** (**msdyn_transactioncategory**) и **Резервируемый ресурс** (**bookableresource**) являются примерами кандидатов в измерения.</span><span class="sxs-lookup"><span data-stu-id="83312-128">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="83312-129">Следует учесть, должно ли ваше измерение ценообразования быть таблицей или набором параметров.</span><span class="sxs-lookup"><span data-stu-id="83312-129">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="83312-130">Если вы ожидаете изменения в значениях измерения, которые превысят 10 или 12, и нужны дополнительные атрибуты для этих значений, создайте сущность, а не набор параметров.</span><span class="sxs-lookup"><span data-stu-id="83312-130">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, create an entity rather than an option set.</span></span> <span data-ttu-id="83312-131">Поддержание набора параметров, такое как добавление или удаление значений, требует работы администратора или разработчика, в то время как добавить новые строки в таблицу может большинство бизнес-пользователей.</span><span class="sxs-lookup"><span data-stu-id="83312-131">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most business users.</span></span>

<span data-ttu-id="83312-132">Следующий пример показывает ставки выставления счетов, которые настроены на основе роли и подразделения выделения ресурсов, которому ресурс принадлежит.</span><span class="sxs-lookup"><span data-stu-id="83312-132">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="83312-133">Нормы затрат обычно основаны на диапазоне зарплаты сотрудника и подразделении, к которому он относится.</span><span class="sxs-lookup"><span data-stu-id="83312-133">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="83312-134">В этом примере таблицы тарифов для счетов и норм расходов выглядят следующим образом.</span><span class="sxs-lookup"><span data-stu-id="83312-134">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="83312-135">**Пример тарифов для счетов**</span><span class="sxs-lookup"><span data-stu-id="83312-135">**Sample bill rates**</span></span>

| <span data-ttu-id="83312-136">Роль</span><span class="sxs-lookup"><span data-stu-id="83312-136">Role</span></span>        | <span data-ttu-id="83312-137">Подразделение</span><span class="sxs-lookup"><span data-stu-id="83312-137">Org Unit</span></span>    |<span data-ttu-id="83312-138">Единица</span><span class="sxs-lookup"><span data-stu-id="83312-138">Unit</span></span>      |<span data-ttu-id="83312-139">Цена</span><span class="sxs-lookup"><span data-stu-id="83312-139">Price</span></span>      |<span data-ttu-id="83312-140">Валюта</span><span class="sxs-lookup"><span data-stu-id="83312-140">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="83312-141">Разработка</span><span class="sxs-lookup"><span data-stu-id="83312-141">Developer</span></span>   | <span data-ttu-id="83312-142">Contoso US</span><span class="sxs-lookup"><span data-stu-id="83312-142">Contoso US</span></span>  |<span data-ttu-id="83312-143">Час</span><span class="sxs-lookup"><span data-stu-id="83312-143">Hour</span></span> | <span data-ttu-id="83312-144">200</span><span class="sxs-lookup"><span data-stu-id="83312-144">200</span></span>|<span data-ttu-id="83312-145">Доллар США</span><span class="sxs-lookup"><span data-stu-id="83312-145">USD</span></span>     |
| <span data-ttu-id="83312-146">Разработка</span><span class="sxs-lookup"><span data-stu-id="83312-146">Developer</span></span>   | <span data-ttu-id="83312-147">Contoso India</span><span class="sxs-lookup"><span data-stu-id="83312-147">Contoso India</span></span> |<span data-ttu-id="83312-148">Час</span><span class="sxs-lookup"><span data-stu-id="83312-148">Hour</span></span>|   <span data-ttu-id="83312-149">112</span><span class="sxs-lookup"><span data-stu-id="83312-149">112</span></span>|<span data-ttu-id="83312-150">Доллар США</span><span class="sxs-lookup"><span data-stu-id="83312-150">USD</span></span>     |


<span data-ttu-id="83312-151">**Пример норм затрат**</span><span class="sxs-lookup"><span data-stu-id="83312-151">**Sample cost rates**</span></span>

| <span data-ttu-id="83312-152">Диапазон зарплаты</span><span class="sxs-lookup"><span data-stu-id="83312-152">Salary Band</span></span>     | <span data-ttu-id="83312-153">Подразделение</span><span class="sxs-lookup"><span data-stu-id="83312-153">Org Unit</span></span>    |<span data-ttu-id="83312-154">Единица</span><span class="sxs-lookup"><span data-stu-id="83312-154">Unit</span></span>      |<span data-ttu-id="83312-155">Цена</span><span class="sxs-lookup"><span data-stu-id="83312-155">Price</span></span>      |<span data-ttu-id="83312-156">Валюта</span><span class="sxs-lookup"><span data-stu-id="83312-156">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="83312-157">Моя компания_Диапазон1</span><span class="sxs-lookup"><span data-stu-id="83312-157">My company_Band1</span></span> | <span data-ttu-id="83312-158">Contoso US</span><span class="sxs-lookup"><span data-stu-id="83312-158">Contoso US</span></span>  |<span data-ttu-id="83312-159">Час</span><span class="sxs-lookup"><span data-stu-id="83312-159">Hour</span></span> | <span data-ttu-id="83312-160">145</span><span class="sxs-lookup"><span data-stu-id="83312-160">145</span></span>|<span data-ttu-id="83312-161">Доллар США</span><span class="sxs-lookup"><span data-stu-id="83312-161">USD</span></span>     |
| <span data-ttu-id="83312-162">Моя компания_Диапазон2</span><span class="sxs-lookup"><span data-stu-id="83312-162">My company_Band2</span></span> | <span data-ttu-id="83312-163">Contoso India</span><span class="sxs-lookup"><span data-stu-id="83312-163">Contoso India</span></span> |<span data-ttu-id="83312-164">Час</span><span class="sxs-lookup"><span data-stu-id="83312-164">Hour</span></span>|   <span data-ttu-id="83312-165">67</span><span class="sxs-lookup"><span data-stu-id="83312-165">67</span></span>|<span data-ttu-id="83312-166">Доллар США</span><span class="sxs-lookup"><span data-stu-id="83312-166">USD</span></span>     |


[!INCLUDE[footer-include](../includes/footer-banner.md)]