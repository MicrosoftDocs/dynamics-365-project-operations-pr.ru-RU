---
title: Создание рабочей группы проекта
description: В этом разделе представлена информация о том, как создавать рабочие группы по проекте и управлять ими.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kdwns
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 121a007d91c2da4f3b9951901781757b8bcca8fe
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270874"
---
# <a name="create-a-project-team"></a><span data-ttu-id="dcd54-103">Создание проектной группы</span><span class="sxs-lookup"><span data-stu-id="dcd54-103">Create a project team</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dcd54-104">Чтобы использовать роли, которые были ранее настроены в проекте, менеджер проекта должен связать роли с проектом.</span><span class="sxs-lookup"><span data-stu-id="dcd54-104">To use the roles that were previously set up in a project, a project manager must associate the roles with the project.</span></span> <span data-ttu-id="dcd54-105">Для проекта можно назначить несколько ролей.</span><span class="sxs-lookup"><span data-stu-id="dcd54-105">Multiple roles can be assigned for a project.</span></span> <span data-ttu-id="dcd54-106">Во избежание путаницы эти роли автоматически маркируются во время резервирования.</span><span class="sxs-lookup"><span data-stu-id="dcd54-106">To prevent confusion, these roles are automatically labeled during reservation.</span></span> <span data-ttu-id="dcd54-107">Например, если менеджеру проекта требуются три инженера-программиста, три роли инженера-программиста с **программист 1**, **программист 2** и **программист 3** в качестве меток генерируются автоматически.</span><span class="sxs-lookup"><span data-stu-id="dcd54-107">For example, if the project manager requires three software engineers, three Software engineer roles that have **software engineer 1**, **software engineer 2**, and **software engineer 3** as their labels are automatically generated.</span></span> <span data-ttu-id="dcd54-108">Если характеристики роли были ранее заданы для роли, они применяются как фильтр во время поиска ресурса.</span><span class="sxs-lookup"><span data-stu-id="dcd54-108">If role characteristics were previously set for the role, they are applied as a filter during searches for a resource.</span></span> <span data-ttu-id="dcd54-109">Дополнительные характеристики могут быть добавлены по мере необходимости для дальнейшего уточнения поиска.</span><span class="sxs-lookup"><span data-stu-id="dcd54-109">Additional characteristics can be added as required to further refine the search.</span></span>

<span data-ttu-id="dcd54-110">Параметры просмотра также можно настроить, чтобы лучше видеть доступность ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dcd54-110">View settings can also be customized to give a better view of resource availability.</span></span> <span data-ttu-id="dcd54-111">Есть варианты отображения почасовой, ежедневной, еженедельной, ежемесячной, ежеквартальной и годовой доступности.</span><span class="sxs-lookup"><span data-stu-id="dcd54-111">There are options to show hourly, daily, weekly, monthly, quarterly, and annual availability.</span></span> <span data-ttu-id="dcd54-112">Также есть возможность показать доступную и оставшуюся емкость ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dcd54-112">There is also an option to show available and remaining capacity on resources.</span></span> <span data-ttu-id="dcd54-113">Эта опция полезна для управления временем, когда вы оцениваете доступное время для действий или доступность ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dcd54-113">This option is useful for time management, when you're estimating available time for activities or resource availability.</span></span>

<span data-ttu-id="dcd54-114">Менеджер проекта может выбрать роль на странице, а затем, если есть доступный ресурс, который соответствует требованиям, выбрать резервирование ресурса для заполнения роли.</span><span class="sxs-lookup"><span data-stu-id="dcd54-114">The project manager can select a role on the page and then, if there is an available resource that fits the requirement, select to reserve a resource to fill the role.</span></span> <span data-ttu-id="dcd54-115">Обратите внимание, что на данном этапе планирования ресурсы резервировать не нужно.</span><span class="sxs-lookup"><span data-stu-id="dcd54-115">Note that the resources don't have to be reserved at this point in the planning stage.</span></span> <span data-ttu-id="dcd54-116">При создании WBS вы можете заменить роли укомплектованными ресурсами для проекта.</span><span class="sxs-lookup"><span data-stu-id="dcd54-116">When you create a WBS, you can replace roles with staffed resources for the project.</span></span> <span data-ttu-id="dcd54-117">Если роли заменяются укомплектованными ресурсами в WBS, настройка ресурсов автоматически обновляет список и расписание проектной группы.</span><span class="sxs-lookup"><span data-stu-id="dcd54-117">If roles are replaced with staffed resources in the WBS, the resource setup automatically updates the project team listing and scheduling.</span></span>

<span data-ttu-id="dcd54-118">[![Список проектной команды, включающий как роли, так и фактические ресурсы](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span><span class="sxs-lookup"><span data-stu-id="dcd54-118">[![Project team listing that includes both roles and actual resources](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span></span> 

<span data-ttu-id="dcd54-119">У менеджера проекта есть различные варианты резервирования ресурса для проекта, например **Оставшаяся загрузка**, **Полная загрузка**, **Процент загрузки** и **Указать часы**.</span><span class="sxs-lookup"><span data-stu-id="dcd54-119">The project manager has various options for booking a resource for a project, such as **Remaining capacity**, **Full capacity**, **Capacity percentage**, and **Specify hours**.</span></span> <span data-ttu-id="dcd54-120">Эти параметры резервирования можно отменить в любой момент, если назначение ресурсов изменится.</span><span class="sxs-lookup"><span data-stu-id="dcd54-120">These booking options can be canceled at any time if resource assignments change.</span></span> <span data-ttu-id="dcd54-121">Поддерживаются два типа резервирования:</span><span class="sxs-lookup"><span data-stu-id="dcd54-121">Two types of booking are supported:</span></span>

- <span data-ttu-id="dcd54-122">**Окончательное резервирование** — резервирование ресурсов было одобрено и подтверждено для работы над заданием в течение указанного срока.</span><span class="sxs-lookup"><span data-stu-id="dcd54-122">**Hard Book** – The resource reservation was approved and confirmed to work on the engagement for the specified duration.</span></span>
- <span data-ttu-id="dcd54-123">**Предварительное резервирование** — резервирование ресурсов было предварительно подтверждено для работы над заданием в течение указанного срока.</span><span class="sxs-lookup"><span data-stu-id="dcd54-123">**Soft book** – The resource reservations was tentatively set to work on the engagement for the specified duration.</span></span>

<span data-ttu-id="dcd54-124">В следующей процедуре поясняется создание проектной группы.</span><span class="sxs-lookup"><span data-stu-id="dcd54-124">The following procedure explains how to create a project team.</span></span>

## <a name="create-a-project-team"></a><span data-ttu-id="dcd54-125">Создание проектной группы</span><span class="sxs-lookup"><span data-stu-id="dcd54-125">Create a project team</span></span>

1. <span data-ttu-id="dcd54-126">На странице списка **Все проекты** выберите проект, а затем выберите **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="dcd54-126">On the **All projects** list page, select a project, and then select **Edit**.</span></span>
2. <span data-ttu-id="dcd54-127">На вкладке **Проектная группа и планирование** в поле **Дата окончания расписания** введите дату начала расписания плюс один месяц.</span><span class="sxs-lookup"><span data-stu-id="dcd54-127">On the **Project team and scheduling** tab, in the **Schedule end date** field, enter the schedule start date plus one month.</span></span> <span data-ttu-id="dcd54-128">Например, если дата начала расписания — 24 июня 2017 г. (24.06.2017), введите **24.07.2017**.</span><span class="sxs-lookup"><span data-stu-id="dcd54-128">For example, if the schedule start date is June 24, 2017 (24/06/2017), enter **24/07/2017**.</span></span>
3. <span data-ttu-id="dcd54-129">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="dcd54-129">Select **Add**.</span></span>
4. <span data-ttu-id="dcd54-130">В области **Добавить роли в проект** в поле **Роль** выберите **Старший менеджер проекта**.</span><span class="sxs-lookup"><span data-stu-id="dcd54-130">In the **Add roles to the project** pane, in the **Role** field, select **Senior Project Manager**.</span></span>
5. <span data-ttu-id="dcd54-131">Выберите **Необходимые компетенции**.</span><span class="sxs-lookup"><span data-stu-id="dcd54-131">Select **Required competencies**.</span></span>
6. <span data-ttu-id="dcd54-132">На странице **Выберите характеристики** выберете характеристики, которые вы ранее задали для роли старшего менеджера проекта по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="dcd54-132">On the **Choose characteristics** page, the characteristics that you previously set for the Senior project manager role are selected by default.</span></span> <span data-ttu-id="dcd54-133">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="dcd54-133">Select **OK**.</span></span>
7. <span data-ttu-id="dcd54-134">На странице **Добавить роли в проект** в поле **Количество ресурсов** введите **1**.</span><span class="sxs-lookup"><span data-stu-id="dcd54-134">On the **Add roles to project** page, in the **Number of resources** field, enter **1**.</span></span>
8. <span data-ttu-id="dcd54-135">В поле **Ресурс** поиск показывает все ресурсы, обладающие необходимыми компетенциями.</span><span class="sxs-lookup"><span data-stu-id="dcd54-135">In the **Resource** field, the lookup shows all resources that have the required competencies.</span></span> <span data-ttu-id="dcd54-136">Выберите **Даниэл Гольдшмидт**, а затем выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="dcd54-136">Select **Daniel Goldschmidt**, and then select **Create**.</span></span>
9. <span data-ttu-id="dcd54-137">Откройте страницу **Проект** и выберите **Add**.</span><span class="sxs-lookup"><span data-stu-id="dcd54-137">On the **Project** page, select **Add**.</span></span>
10. <span data-ttu-id="dcd54-138">В области **Добавить роли в проект** в поле **Роль** выберите **Участник рабочей группы**.</span><span class="sxs-lookup"><span data-stu-id="dcd54-138">In the **Add roles to the project** pane, in the **Role** field, select **Team member**.</span></span> <span data-ttu-id="dcd54-139">В поле **Количество ресурсов** введите **5**.</span><span class="sxs-lookup"><span data-stu-id="dcd54-139">In the **Number of resources** field, enter **5**.</span></span>
11. <span data-ttu-id="dcd54-140">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="dcd54-140">Select **Create**.</span></span>
12. <span data-ttu-id="dcd54-141">На странице **Проекты** выберите **Выполнить ресурс**.</span><span class="sxs-lookup"><span data-stu-id="dcd54-141">On the **Projects** page, select **Fulfill resource**.</span></span>

## <a name="monitor-project-teams"></a><span data-ttu-id="dcd54-142">Мониторинг проектных групп</span><span class="sxs-lookup"><span data-stu-id="dcd54-142">Monitor project teams</span></span>
1. <span data-ttu-id="dcd54-143">На странице **Все проекты** выберите ссылку **Идентификатор проекта** для проекта **XYZ обновление фаза 2**.</span><span class="sxs-lookup"><span data-stu-id="dcd54-143">On the **All projects** page, select the **Project ID** link for the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="dcd54-144">На экспресс-вкладке **Работая группа и планирование** проверьте правильность перечисленных ресурсов проекта.</span><span class="sxs-lookup"><span data-stu-id="dcd54-144">On the **Project team and scheduling** FastTab, verify that the project resources that are listed are correct.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]