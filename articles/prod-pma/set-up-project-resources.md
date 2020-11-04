---
title: Настройка ресурсов проекта
description: В этом разделе представлена информация о настройке или запросе ресурсов проекта.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7eec8ad5d78019219b2e04ca75eeaa5a3c8a748f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083360"
---
# <a name="set-up-project-resources"></a><span data-ttu-id="82f03-103">Настройка ресурсов проекта</span><span class="sxs-lookup"><span data-stu-id="82f03-103">Set up project resources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="82f03-104">Вы должны настроить календарь и связать его с сотрудником или работником.</span><span class="sxs-lookup"><span data-stu-id="82f03-104">You must set up a calendar and associate it with an employee or a worker.</span></span> <span data-ttu-id="82f03-105">Календарь используется для планирования проекта и рабочего времени ресурсов, зарезервированных для проекта.</span><span class="sxs-lookup"><span data-stu-id="82f03-105">The calendar is used to schedule the project and the working time of the resources that are reserved for the project.</span></span> <span data-ttu-id="82f03-106">Во время настройки календаря менеджеры проектов могут выполнять выравнивание ресурсов в рамках оптимизации ресурсов.</span><span class="sxs-lookup"><span data-stu-id="82f03-106">During calendar setup, project managers can do resource leveling as part of resource optimization.</span></span> <span data-ttu-id="82f03-107">Исходя из календарного расписания, на ресурсы могут быть наложены ограничения.</span><span class="sxs-lookup"><span data-stu-id="82f03-107">Based on the calendar schedule, restrictions can be put on resources.</span></span> <span data-ttu-id="82f03-108">Вы можете настроить календарь на странице **Календари**.</span><span class="sxs-lookup"><span data-stu-id="82f03-108">You can set up a calendar on the **Calendars** page.</span></span>

<span data-ttu-id="82f03-109">Когда вы настраиваете сотрудника в качестве ресурса проекта, вы можете выбирать из сотрудников, которые работают в компании, для которой вы настраиваете ресурсы.</span><span class="sxs-lookup"><span data-stu-id="82f03-109">When you set up a worker as a project resource, you can select from workers who work in the company that you're setting up resources for.</span></span> <span data-ttu-id="82f03-110">Кроме того, вы можете выбрать сотрудников из других компаний в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="82f03-110">Alternatively, you can select workers from other companies in your organization.</span></span> <span data-ttu-id="82f03-111">Эти работники называются ресурсами внутри компании.</span><span class="sxs-lookup"><span data-stu-id="82f03-111">These workers are known as intercompany resources.</span></span>

<span data-ttu-id="82f03-112">Следующие процедуры объясняют, как настроить сотрудника в качестве ресурса проекта в вашей компании и как настроить ресурс внутрихолдингового проекта.</span><span class="sxs-lookup"><span data-stu-id="82f03-112">The following procedures explain how to set up a worker as a project resource in your company and how to set up an intercompany project resource.</span></span>

## <a name="set-up-a-worker-as-a-project-resource"></a><span data-ttu-id="82f03-113">Настройка работника в качестве ресурса проекта</span><span class="sxs-lookup"><span data-stu-id="82f03-113">Set up a worker as a project resource</span></span>

1. <span data-ttu-id="82f03-114">На странице **Работники** в списке **Работники** выберите работника, которого вы добавляете в качестве ресурса проекта, и откройте запись работника.</span><span class="sxs-lookup"><span data-stu-id="82f03-114">On the **Workers** page, in the **Workers** list, select the worker that you're adding as a project resource, and open the worker record.</span></span>
2. <span data-ttu-id="82f03-115">На панели действий выберите **Проект** &gt; **Настройка** &gt; **Настройка проекта**.</span><span class="sxs-lookup"><span data-stu-id="82f03-115">On the Action Pane, select **Project** &gt; **Setup** &gt; **Project setup**.</span></span>
3. <span data-ttu-id="82f03-116">Выберите календарь и закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="82f03-116">Select a calendar, and then close the page.</span></span>

<span data-ttu-id="82f03-117">Вы также можете указать проекты по умолчанию для ресурса как тип предварительного назначения.</span><span class="sxs-lookup"><span data-stu-id="82f03-117">You can also specify default projects for a resource as a type of pre-assignment.</span></span> <span data-ttu-id="82f03-118">Предварительные назначения могут использоваться, когда менеджер ресурсов или менеджер проекта заранее знает, над какими проектами будет работать ресурс.</span><span class="sxs-lookup"><span data-stu-id="82f03-118">Pre-assignments can be used when the resource manager or project manager knows which projects the resource will be working on in advance.</span></span> <span data-ttu-id="82f03-119">Предварительные задания также могут быть основаны на запросе спонсора проекта или заказчика.</span><span class="sxs-lookup"><span data-stu-id="82f03-119">Pre-assignments can also be based on the request of a project sponsor or customer.</span></span> <span data-ttu-id="82f03-120">Чтобы предварительно назначить проект, на странице **Назначение проектов** , на вкладке **Проекты** в списке **Остальные проекты** выберите соответствующий проект.</span><span class="sxs-lookup"><span data-stu-id="82f03-120">To pre-assign a project, on the **Assign projects** page, on the **Projects** tab, in the **Remaining projects** list, select the appropriate project.</span></span>

## <a name="set-up-an-intercompany-resource"></a><span data-ttu-id="82f03-121">Настройка внутрихолдингового ресурса</span><span class="sxs-lookup"><span data-stu-id="82f03-121">Set up an intercompany resource</span></span>

<span data-ttu-id="82f03-122">Когда вы настраиваете работника в качестве внутрихолдингового ресурса, вы должны выполнить настройку как в компании-кредиторе, так и в компании-заемщике.</span><span class="sxs-lookup"><span data-stu-id="82f03-122">When you set up a worker as an intercompany resource, you must complete the setup in both the lending company and the borrowing company.</span></span>

### <a name="in-the-lending-company"></a><span data-ttu-id="82f03-123">В компании-кредиторе</span><span class="sxs-lookup"><span data-stu-id="82f03-123">In the lending company</span></span>

1. <span data-ttu-id="82f03-124">В Finance убедитесь, что выбрана компания-кредитор, а затем выполните процедуру, описанную в предыдущем разделе "Настройка работника в качестве ресурса проекта".</span><span class="sxs-lookup"><span data-stu-id="82f03-124">In Finance, verify that the lending company is selected, and then complete the procedure in the previous section, "Set up a worker as a project resource."</span></span>
2. <span data-ttu-id="82f03-125">На странице **Внутрихолдинговый учет** выберите **ССоздат**.</span><span class="sxs-lookup"><span data-stu-id="82f03-125">On the **Intercompany accounting** page, select **New**.</span></span>
3. <span data-ttu-id="82f03-126">В поле **Идентификатор юридического лица** выберите компанию-кредитора.</span><span class="sxs-lookup"><span data-stu-id="82f03-126">In the **Legal entity ID** field, select the lending company.</span></span> <span data-ttu-id="82f03-127">Заполните оставшиеся поля нужным образом и выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="82f03-127">Fill in the remaining fields as appropriate, and then select **Save**.</span></span>
4. <span data-ttu-id="82f03-128">На странице **Трансфертная цена** выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="82f03-128">On the **Transfer price** page, select **New**.</span></span>
5. <span data-ttu-id="82f03-129">В поле **Юридическое лицо-заемщик** выберите соответствующую компанию.</span><span class="sxs-lookup"><span data-stu-id="82f03-129">In the **Borrowing legal entity** field, select the appropriate company.</span></span>
6. <span data-ttu-id="82f03-130">Чтобы одолжить компании-заемщику только тот ресурс, который вы создали в начале этого раздела, в поле **Ресурс** выберите имя созданного вами ресурса.</span><span class="sxs-lookup"><span data-stu-id="82f03-130">To lend the borrowing company only the resource that you created at the beginning of this section, in the **Resource** field, select the name of the resource that you created.</span></span> <span data-ttu-id="82f03-131">Чтобы сделать все ресурсы кредитной компании доступными для компании-заемщика, оставьте поле **Ресурс** пустым.</span><span class="sxs-lookup"><span data-stu-id="82f03-131">To make all resources in the lending company available to the borrowing company, leave the **Resource** field blank.</span></span>
7. <span data-ttu-id="82f03-132">На странице **Параметры управления проектом и учета** на вкладке **Внутрихолдинговый** установите параметр **Включить внутрихолдинговое планирование ресурсов и расписаний** как **Да**.</span><span class="sxs-lookup"><span data-stu-id="82f03-132">On the **Project management and accounting parameters** page, on the **Intercompany** tab, set the **Enable intercompany resource scheduling and timesheets** option to **Yes**.</span></span>

### <a name="in-the-borrowing-company"></a><span data-ttu-id="82f03-133">В компании-заемщике</span><span class="sxs-lookup"><span data-stu-id="82f03-133">In the borrowing company</span></span>

- <span data-ttu-id="82f03-134">На странице **Список ресурсов** в фильтре поиска введите имя ресурса, который вы создали для компании-кредитора, чтобы убедиться, что это имя включено в список ресурсов для компании-заемщика.</span><span class="sxs-lookup"><span data-stu-id="82f03-134">On the **Resources list** page, in the search filter, enter the name of the resource that you created for the lending company, to verify that the name is included in the resource list for the borrowing company.</span></span>

## <a name="request-project-resources"></a><span data-ttu-id="82f03-135">Запрос ресурсов проекта</span><span class="sxs-lookup"><span data-stu-id="82f03-135">Request project resources</span></span>
<span data-ttu-id="82f03-136">Функциональность только для планирования ресурсов проекта позволяет менеджерам ресурсов распределять укомплектованные ресурсы по заданиям или проектам.</span><span class="sxs-lookup"><span data-stu-id="82f03-136">The functionality for project resource scheduling only lets resource managers distribute staffed resources on engagements or projects.</span></span> <span data-ttu-id="82f03-137">Чтобы включить эту функцию, выполните следующие задачи или убедитесь, что они выполнены:</span><span class="sxs-lookup"><span data-stu-id="82f03-137">To enable this functionality, complete the following tasks, or verify that they have been completed:</span></span>

- <span data-ttu-id="82f03-138">Настройте номерные серии.</span><span class="sxs-lookup"><span data-stu-id="82f03-138">Set up number sequences.</span></span>
- <span data-ttu-id="82f03-139">Настройте процессы управления проектами и учета.</span><span class="sxs-lookup"><span data-stu-id="82f03-139">Set up project management and accounting workflows.</span></span>
- <span data-ttu-id="82f03-140">Включите рабочие процессы запроса ресурсов.</span><span class="sxs-lookup"><span data-stu-id="82f03-140">Enable resource request workflows.</span></span>

<span data-ttu-id="82f03-141">После того, как предыдущие задачи будут выполнены, вы можете выполнить следующие задачи по мере необходимости:</span><span class="sxs-lookup"><span data-stu-id="82f03-141">After the preceding tasks have been completed, you can complete the following tasks as you require:</span></span>

- <span data-ttu-id="82f03-142">Создайте запрос ресурса из укомплектованного ресурса с предварительным резервированием.</span><span class="sxs-lookup"><span data-stu-id="82f03-142">Create a resource request from a soft-booked staffed resource.</span></span>
- <span data-ttu-id="82f03-143">Контролируйте запросы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="82f03-143">Monitor resource requests.</span></span>
- <span data-ttu-id="82f03-144">Выполните запросы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="82f03-144">Fulfill resource requests.</span></span>
- <span data-ttu-id="82f03-145">Запросите у WBS кадровый ресурс.</span><span class="sxs-lookup"><span data-stu-id="82f03-145">Request a staffed resource from a WBS.</span></span>
- <span data-ttu-id="82f03-146">Зарезервируйте ресурсы для проекта без запроса укомплектованного ресурса.</span><span class="sxs-lookup"><span data-stu-id="82f03-146">Book resources to a project without having a request for a staffed resource.</span></span>
