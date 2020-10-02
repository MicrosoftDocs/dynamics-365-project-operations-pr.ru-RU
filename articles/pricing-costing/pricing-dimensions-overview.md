---
title: Обзор измерений цен
description: В этой теме предоставлена информация об измерениях ценообразования в Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: fe2ab3a1b12c00e346e27709d66b5a0cb81a3b56
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898232"
---
# <a name="pricing-dimensions-overview"></a><span data-ttu-id="c7575-103">Обзор измерений цен</span><span class="sxs-lookup"><span data-stu-id="c7575-103">Pricing dimensions overview</span></span>

<span data-ttu-id="c7575-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="c7575-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c7575-105">Измерения, используемые в трудовых ресурсах для настройки ценообразования и стоимости, подразделяются на две категории:</span><span class="sxs-lookup"><span data-stu-id="c7575-105">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="c7575-106">Люди</span><span class="sxs-lookup"><span data-stu-id="c7575-106">People</span></span>
- <span data-ttu-id="c7575-107">Запланированная работа</span><span class="sxs-lookup"><span data-stu-id="c7575-107">Planned work</span></span>

<span data-ttu-id="c7575-108">По этой причине, имеются два типа доступных значений измерений ценообразования:</span><span class="sxs-lookup"><span data-stu-id="c7575-108">Because of this, there are two types of pricing dimension values available:</span></span>

- <span data-ttu-id="c7575-109">**Наборы параметров**: измерения, являющиеся фиксированными перечислениями для набора значений.</span><span class="sxs-lookup"><span data-stu-id="c7575-109">**Option sets**: Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="c7575-110">**Значения на основе сущности**: измерения, которые могут быть переменным набором значений.</span><span class="sxs-lookup"><span data-stu-id="c7575-110">**Entity-based values**: Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="c7575-111">Измерения цен</span><span class="sxs-lookup"><span data-stu-id="c7575-111">Pricing dimensions</span></span>

<span data-ttu-id="c7575-112">Dynamics 365 Project Operations поставляется с набором измерений ценообразования по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c7575-112">Dynamics 365 Project Operations ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="c7575-113">Эти измерения ценообразования можно просматривать, выбрав **Project Operations** > **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="c7575-113">You can view these pricing dimensions by going to **Project Operations** > **Parameters**.</span></span> <span data-ttu-id="c7575-114">В записи параметров на вкладке **Сумма на основе измерения цен** убедитесь, что роль **msdyn_resourcecategory** и подразделение распределения ресурсов **msdyn_organizationalunit** содержат поля **Применимо к продажам** и **Применимо к стоимости**, в которых задано значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="c7575-114">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="c7575-115">Когда эти поля включены, можно настроить цену и стоимость для каждого сочетания роли и подразделения.</span><span class="sxs-lookup"><span data-stu-id="c7575-115">With these fields enabled, you can set up the price and cost for each role and organizational unit combination.</span></span>

<span data-ttu-id="c7575-116">Если необходима задавать цену или стоимость ваших ресурсов с помощью дополнительных атрибутов, можно создать настраиваемые поля, сущности и измерения.</span><span class="sxs-lookup"><span data-stu-id="c7575-116">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span>

## <a name="pricing-human-resource-time"></a><span data-ttu-id="c7575-117">Задание цены времени сотрудников</span><span class="sxs-lookup"><span data-stu-id="c7575-117">Pricing human resource time</span></span>
<span data-ttu-id="c7575-118">Порядок задания цены времени сотрудников в организация часто является стратегически важным фактором, который напрямую влияет на доходность организации.</span><span class="sxs-lookup"><span data-stu-id="c7575-118">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="c7575-119">Работайте с финансовыми рабочими группами и практическими руководителями, когда ваша организация готова определить, как требуется настроить тарифы выставления счетов и нормы затрат для времени человеческих ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c7575-119">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="c7575-120">Другие соображения для ценообразования включают, требуется ли повторно использовать поля или сущности, которые в настоящее время не являются измерениями ценообразования, но применяются как измерения ценообразования в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="c7575-120">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="c7575-121">Такие поля, как **Категория проводки** (**msdyn_transactioncategory**) и **Резервируемый ресурс** (**bookableresource**) являются примерами кандидатов в измерения.</span><span class="sxs-lookup"><span data-stu-id="c7575-121">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="c7575-122">Следует учесть, должно ли ваше измерение ценообразования быть таблицей или набором параметров.</span><span class="sxs-lookup"><span data-stu-id="c7575-122">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="c7575-123">Если вы ожидаете изменения в значениях измерения, которые превысят 10 или 12, и нужны дополнительные атрибуты для этих значений, можно создать сущность, а не набор параметров.</span><span class="sxs-lookup"><span data-stu-id="c7575-123">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="c7575-124">Поддержание набора параметров, такое как добавление или удаление значений, требует работы администратора или разработчика, в то время как добавить новые строки в таблицу может большинство пользователей.</span><span class="sxs-lookup"><span data-stu-id="c7575-124">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="c7575-125">Следующий пример показывает ставки выставления счетов, которые настроены на основе роли и подразделения выделения ресурсов, которому ресурс принадлежит.</span><span class="sxs-lookup"><span data-stu-id="c7575-125">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="c7575-126">Нормы затрат обычно основаны на диапазоне зарплаты сотрудника и подразделении, к которому он относится.</span><span class="sxs-lookup"><span data-stu-id="c7575-126">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="c7575-127">В этом примере таблицы тарифов для счетов и норм расходов выглядят следующим образом.</span><span class="sxs-lookup"><span data-stu-id="c7575-127">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="c7575-128">**Пример тарифов для счетов**</span><span class="sxs-lookup"><span data-stu-id="c7575-128">**Sample bill rates**</span></span>

| <span data-ttu-id="c7575-129">Роль</span><span class="sxs-lookup"><span data-stu-id="c7575-129">Role</span></span>        | <span data-ttu-id="c7575-130">Подразделение</span><span class="sxs-lookup"><span data-stu-id="c7575-130">Org Unit</span></span>    |<span data-ttu-id="c7575-131">Единица измерения</span><span class="sxs-lookup"><span data-stu-id="c7575-131">Unit</span></span>      |<span data-ttu-id="c7575-132">Цена</span><span class="sxs-lookup"><span data-stu-id="c7575-132">Price</span></span>      |<span data-ttu-id="c7575-133">Валюта</span><span class="sxs-lookup"><span data-stu-id="c7575-133">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="c7575-134">Разработчик</span><span class="sxs-lookup"><span data-stu-id="c7575-134">Developer</span></span>   | <span data-ttu-id="c7575-135">Contoso US</span><span class="sxs-lookup"><span data-stu-id="c7575-135">Contoso US</span></span>  |<span data-ttu-id="c7575-136">Hour</span><span class="sxs-lookup"><span data-stu-id="c7575-136">Hour</span></span> | <span data-ttu-id="c7575-137">200</span><span class="sxs-lookup"><span data-stu-id="c7575-137">200</span></span>|<span data-ttu-id="c7575-138">Доллар США</span><span class="sxs-lookup"><span data-stu-id="c7575-138">USD</span></span>     |
| <span data-ttu-id="c7575-139">Разработчик</span><span class="sxs-lookup"><span data-stu-id="c7575-139">Developer</span></span>   | <span data-ttu-id="c7575-140">Contoso India</span><span class="sxs-lookup"><span data-stu-id="c7575-140">Contoso India</span></span> |<span data-ttu-id="c7575-141">Hour</span><span class="sxs-lookup"><span data-stu-id="c7575-141">Hour</span></span>|   <span data-ttu-id="c7575-142">112</span><span class="sxs-lookup"><span data-stu-id="c7575-142">112</span></span>|<span data-ttu-id="c7575-143">Доллар США</span><span class="sxs-lookup"><span data-stu-id="c7575-143">USD</span></span>     |


<span data-ttu-id="c7575-144">**Пример норм затрат**</span><span class="sxs-lookup"><span data-stu-id="c7575-144">**Sample cost rates**</span></span>

| <span data-ttu-id="c7575-145">Диапазон зарплаты</span><span class="sxs-lookup"><span data-stu-id="c7575-145">Salary Band</span></span>     | <span data-ttu-id="c7575-146">Подразделение</span><span class="sxs-lookup"><span data-stu-id="c7575-146">Org Unit</span></span>    |<span data-ttu-id="c7575-147">Единица измерения</span><span class="sxs-lookup"><span data-stu-id="c7575-147">Unit</span></span>      |<span data-ttu-id="c7575-148">Цена</span><span class="sxs-lookup"><span data-stu-id="c7575-148">Price</span></span>      |<span data-ttu-id="c7575-149">Валюта</span><span class="sxs-lookup"><span data-stu-id="c7575-149">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="c7575-150">Моя компания_Диапазон1</span><span class="sxs-lookup"><span data-stu-id="c7575-150">My company_Band1</span></span> | <span data-ttu-id="c7575-151">Contoso US</span><span class="sxs-lookup"><span data-stu-id="c7575-151">Contoso US</span></span>  |<span data-ttu-id="c7575-152">Hour</span><span class="sxs-lookup"><span data-stu-id="c7575-152">Hour</span></span> | <span data-ttu-id="c7575-153">145</span><span class="sxs-lookup"><span data-stu-id="c7575-153">145</span></span>|<span data-ttu-id="c7575-154">Доллар США</span><span class="sxs-lookup"><span data-stu-id="c7575-154">USD</span></span>     |
| <span data-ttu-id="c7575-155">Моя компания_Диапазон2</span><span class="sxs-lookup"><span data-stu-id="c7575-155">My company_Band2</span></span> | <span data-ttu-id="c7575-156">Contoso India</span><span class="sxs-lookup"><span data-stu-id="c7575-156">Contoso India</span></span> |<span data-ttu-id="c7575-157">Hour</span><span class="sxs-lookup"><span data-stu-id="c7575-157">Hour</span></span>|   <span data-ttu-id="c7575-158">67</span><span class="sxs-lookup"><span data-stu-id="c7575-158">67</span></span>|<span data-ttu-id="c7575-159">Доллар США</span><span class="sxs-lookup"><span data-stu-id="c7575-159">USD</span></span>     |
