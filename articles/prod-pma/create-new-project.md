---
title: Создание проекта
description: В этом разделе представлена информация о том, как создать новый проект.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b29340dc88aea888ea2f5ea975eaea59d014279
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270739"
---
# <a name="create-a-new-project"></a><span data-ttu-id="4a462-103">Создание проекта</span><span class="sxs-lookup"><span data-stu-id="4a462-103">Create a new project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4a462-104">Чтобы создать новый проект, выполните указанные ниже шаги.</span><span class="sxs-lookup"><span data-stu-id="4a462-104">Complete the following steps to create a new project.</span></span>

1. <span data-ttu-id="4a462-105">На странице **Управление проектом** выберите **Создать проект** и введите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="4a462-105">On the **Project management** page, select **New project**, and enter the following values:</span></span>

    - <span data-ttu-id="4a462-106">**Тип проекта:** Время и материал</span><span class="sxs-lookup"><span data-stu-id="4a462-106">**Project type:** Time and material</span></span>
    - <span data-ttu-id="4a462-107">**Название проекта:** XYZ обновление фаза 2</span><span class="sxs-lookup"><span data-stu-id="4a462-107">**Project name:** XYZ Upgrade Phase 2</span></span>
    - <span data-ttu-id="4a462-108">**Группа проекта:** TM\_WIP</span><span class="sxs-lookup"><span data-stu-id="4a462-108">**Project group:** TM\_WIP</span></span>
    - <span data-ttu-id="4a462-109">**Идентификатор контракта по проекту:** 00000002</span><span class="sxs-lookup"><span data-stu-id="4a462-109">**Project contract ID:** 00000002</span></span>

2. <span data-ttu-id="4a462-110">Выберите **Создать проект**.</span><span class="sxs-lookup"><span data-stu-id="4a462-110">Select **Create project**.</span></span>

## <a name="assign-a-resource-to-a-project"></a><span data-ttu-id="4a462-111">Назначение ресурса проекту</span><span class="sxs-lookup"><span data-stu-id="4a462-111">Assign a resource to a project</span></span>

1. <span data-ttu-id="4a462-112">На странице **Работники** в списке **Работники** выберите запись для работника, для которого настроены компетенции, и откройте запись работника.</span><span class="sxs-lookup"><span data-stu-id="4a462-112">On the **Workers** page, in the **Workers** list, select the record for the worker that you previously set up competencies for, and open the worker record.</span></span>
2. <span data-ttu-id="4a462-113">На панели действий на вкладке **Проект** в группе **Настройка** выберите **Назначить проекты**.</span><span class="sxs-lookup"><span data-stu-id="4a462-113">On the Action Pane, on the **Project** tab, in the **Setup** group, select **Assign projects**.</span></span>
3. <span data-ttu-id="4a462-114">На странице **Назначения проекта проверки ресурсов** на вкладке **Проекты** в поле **Добавить проект в выбранные проекты** отфильтруйте по проекту **XYZ обновление фаза 2**.</span><span class="sxs-lookup"><span data-stu-id="4a462-114">On the **Resource validation project assignments** page, on the **Projects** tab, in the **Add the project to selected projects** field, filter on the **XYZ Upgrade Phase 2** project.</span></span>
4. <span data-ttu-id="4a462-115">В области **Остальные проекты** выберите проект, а затем нажмите кнопку со стрелкой, чтобы добавить его в область **Выбранные проекты**.</span><span class="sxs-lookup"><span data-stu-id="4a462-115">In the **Remaining projects** pane, select a project, and then select the arrow button to add it to the **Selected projects** pane.</span></span>

<span data-ttu-id="4a462-116">Вы также можете назначать категории для ресурса по своему усмотрению.</span><span class="sxs-lookup"><span data-stu-id="4a462-116">You can also assign categories for a resource as you require.</span></span> <span data-ttu-id="4a462-117">Тип категории: **Расход** или **Доход**.</span><span class="sxs-lookup"><span data-stu-id="4a462-117">The category type is either **Cost** or **Revenue**.</span></span> <span data-ttu-id="4a462-118">Тип категории определяется вашей организацией.</span><span class="sxs-lookup"><span data-stu-id="4a462-118">The category type is determined by your organization.</span></span> <span data-ttu-id="4a462-119">Если для ресурса не назначены категории, Finance ищет категорию по умолчанию для почасовых цен для затрат и доходов.</span><span class="sxs-lookup"><span data-stu-id="4a462-119">If no categories are assigned for a resource, Finance looks up the default category on hour prices for cost and revenue.</span></span>

## <a name="set-up-project-resource-and-role-characteristics"></a><span data-ttu-id="4a462-120">Настройка характеристик ресурсов и ролей проекта</span><span class="sxs-lookup"><span data-stu-id="4a462-120">Set up project resource and role characteristics</span></span>

<span data-ttu-id="4a462-121">Менеджер проекта может использовать функцию выделения ресурсов проекту для создания ролей, необходимых для проекта.</span><span class="sxs-lookup"><span data-stu-id="4a462-121">A project manager can use the project resourcing functionality to create the roles that are required for the project.</span></span> <span data-ttu-id="4a462-122">Роли могут использоваться, если подтвержденные ресурсы все еще неизвестны, когда ресурсы резервируются.</span><span class="sxs-lookup"><span data-stu-id="4a462-122">Roles can be used if confirmed resources are still unknown when resources are being reserved.</span></span> <span data-ttu-id="4a462-123">Роли можно временно зарезервировать как запланированные ресурсы, чтобы вы могли продолжить этапы планирования проекта.</span><span class="sxs-lookup"><span data-stu-id="4a462-123">Roles can be temporarily reserved as planned resources, so that you can continue the project planning stages.</span></span>

<span data-ttu-id="4a462-124">[![Пример роли](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span><span class="sxs-lookup"><span data-stu-id="4a462-124">[![Example of a role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span></span> 

<span data-ttu-id="4a462-125">**Сценарий:** компания Contoso была нанята для завершения проекта «Время и материалы с утвержденным уставом проекта.</span><span class="sxs-lookup"><span data-stu-id="4a462-125">**Scenario:** Contoso was hired to complete a Time and material project that has an approved project charter.</span></span> <span data-ttu-id="4a462-126">Младший менеджер проекта все еще завершает объем проекта.</span><span class="sxs-lookup"><span data-stu-id="4a462-126">The junior project manager is still completing the scope of the project.</span></span> <span data-ttu-id="4a462-127">Менеджер ресурсов в настоящее время определяет конкретные ресурсы, которые будут зарезервированы для работы над новым проектом.</span><span class="sxs-lookup"><span data-stu-id="4a462-127">The resource manager is currently identifying specific resources that will be reserved to work on the new project.</span></span> <span data-ttu-id="4a462-128">Из-за критического характера проекта спонсор проекта попросил "старшего менеджера проекта" в качестве одной из ролей.</span><span class="sxs-lookup"><span data-stu-id="4a462-128">Because of the critical nature of the project, the project sponsor requested Senior project manager as one of the roles.</span></span> <span data-ttu-id="4a462-129">Менеджер ресурсов должен получить новый ресурс и определить роль в системе на случай, если младшему менеджеру проекта потребуется информация о ресурсах во время планирования проекта.</span><span class="sxs-lookup"><span data-stu-id="4a462-129">The resource manager must acquire the new resource and define the role in the system in case the junior project manager requires the resource information during project planning.</span></span>

<span data-ttu-id="4a462-130">Следующие шаги показывают, как менеджер ресурсов может настроить роль старшего менеджера проекта и связать с ней характеристики ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4a462-130">The following steps show how the resource manager can set up the Senior project manager role and associate resource characteristics with it.</span></span> <span data-ttu-id="4a462-131">Позже эту роль можно использовать для поиска доступных ресурсов, соответствующих требуемой компетенции ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4a462-131">Later, the role can be used to search for available resources that match the required resource competencies.</span></span>

1. <span data-ttu-id="4a462-132">На странице **Настройка ролей** выберите **Создать** и введите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="4a462-132">On the **Setup roles** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="4a462-133">**Код роли:** старший менеджер проекта</span><span class="sxs-lookup"><span data-stu-id="4a462-133">**Role ID:** Senior Project Manager</span></span>
    - <span data-ttu-id="4a462-134">**Описание:** старший менеджер проекта</span><span class="sxs-lookup"><span data-stu-id="4a462-134">**Description:** Senior Project Manager</span></span>

2. <span data-ttu-id="4a462-135">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="4a462-135">Select **Create**.</span></span>
3. <span data-ttu-id="4a462-136">Выберите роль **Старший менеджер проекта**, а затем выберите **Настроить характеристики**.</span><span class="sxs-lookup"><span data-stu-id="4a462-136">Select the **Senior Project Manager** role, and then select **Configure characteristics**.</span></span>
4. <span data-ttu-id="4a462-137">В поле **Тип характеристик** выберите **Навык**.</span><span class="sxs-lookup"><span data-stu-id="4a462-137">In the **Characteristics type** field, select **Skill**.</span></span>
5. <span data-ttu-id="4a462-138">В поле **Доступные характеристики** введите навык для поиска.</span><span class="sxs-lookup"><span data-stu-id="4a462-138">In the **Available characteristics** field, enter the skill to search for.</span></span>
6. <span data-ttu-id="4a462-139">В поле **Тип характеристик** выберите **Сертификат**.</span><span class="sxs-lookup"><span data-stu-id="4a462-139">In the **Characteristic type** field, select **Certificate**.</span></span>
7. <span data-ttu-id="4a462-140">В поле **Доступные характеристики** введите тип сертификата для поиска.</span><span class="sxs-lookup"><span data-stu-id="4a462-140">In the **Available characteristics** field, enter the certificate type to search for.</span></span>

## <a name="assign-a-project-resource-to-a-project"></a><span data-ttu-id="4a462-141">Назначение ресурса проекта для проекта</span><span class="sxs-lookup"><span data-stu-id="4a462-141">Assign a project resource to a project</span></span>

1. <span data-ttu-id="4a462-142">На странице **Все проекты** выберите проект **XYZ обновление фаза 2**.</span><span class="sxs-lookup"><span data-stu-id="4a462-142">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="4a462-143">На вкладке **Проектная группа и планирование** выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="4a462-143">On the **Project team and scheduling** tab, select **Add**.</span></span>
3. <span data-ttu-id="4a462-144">В поле **Роль** выберите **Участник рабочей группы**.</span><span class="sxs-lookup"><span data-stu-id="4a462-144">In the **Role** field, select **Team member**.</span></span>
4. <span data-ttu-id="4a462-145">Выберите **Резервировать из календаря**.</span><span class="sxs-lookup"><span data-stu-id="4a462-145">Select **Book from calendar**.</span></span>
5. <span data-ttu-id="4a462-146">На странице **Доступность ресурсов** выберите **Просмотр настроек**.</span><span class="sxs-lookup"><span data-stu-id="4a462-146">On the **Resource availability** page, select **View settings**.</span></span>
6. <span data-ttu-id="4a462-147">На странице **Настройка параметров просмотра** введите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="4a462-147">On the **Adjust view settings** page, enter the following values:</span></span>

    - <span data-ttu-id="4a462-148">**Формат представления диапазона дат:** день</span><span class="sxs-lookup"><span data-stu-id="4a462-148">**Format for date range view:** Day</span></span>
    - <span data-ttu-id="4a462-149">**Показать описания доступности:** да</span><span class="sxs-lookup"><span data-stu-id="4a462-149">**Display availability descriptions:** Yes</span></span>
    - <span data-ttu-id="4a462-150">**Отображение оставшихся ресурсов:** да</span><span class="sxs-lookup"><span data-stu-id="4a462-150">**Display remaining capacity:** Yes</span></span>

7. <span data-ttu-id="4a462-151">Выберите ресурс из списка ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4a462-151">In the list of resources, select a resource.</span></span>
8. <span data-ttu-id="4a462-152">Выберите **Окончательное резервирование** и **Полная загрузка**.</span><span class="sxs-lookup"><span data-stu-id="4a462-152">Select **Hard book** and **Full capacity**.</span></span>

## <a name="assign-a-resource-to-a-default-role"></a><span data-ttu-id="4a462-153">Назначение ресурса роли по умолчанию</span><span class="sxs-lookup"><span data-stu-id="4a462-153">Assign a resource to a default role</span></span>

<span data-ttu-id="4a462-154">Чтобы помочь менеджерам проектов или ресурсов детализировать могут ресурсы, которые можно зарезервировать для проекта.</span><span class="sxs-lookup"><span data-stu-id="4a462-154">To help project or resource managers can drill down further on the resources that can be reserved for a project.</span></span> <span data-ttu-id="4a462-155">Вы можете связать роль по умолчанию с существующим ресурсом или только что приобретенным ресурсом.</span><span class="sxs-lookup"><span data-stu-id="4a462-155">You can associate a default role with an existing resource or a newly acquired resource.</span></span> <span data-ttu-id="4a462-156">Например, когда Даниэл был принят на работу, у него был опыт и навыки, необходимые для выполнения роли бизнес-аналитика.</span><span class="sxs-lookup"><span data-stu-id="4a462-156">For example, when Daniel was hired, he had the experience and skills to fill the Business analyst role.</span></span> <span data-ttu-id="4a462-157">Менеджер ресурсов назначил эту роль роли Дэниела по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4a462-157">The resource manager assigned this role as Daniel's default role.</span></span> <span data-ttu-id="4a462-158">Поэтому менеджер ресурсов добавил Даниэля в группу бизнес-аналитиков, готовых работать над проектами.</span><span class="sxs-lookup"><span data-stu-id="4a462-158">Therefore, the resource manager added Daniel to a pool of business analysts who are available to work on projects.</span></span>

<span data-ttu-id="4a462-159">Во время резервирования ресурсов менеджеры проектов могут фильтровать ресурсы ролей, доступные для работы над проектами.</span><span class="sxs-lookup"><span data-stu-id="4a462-159">During resource reservation, project managers can filter the role resources that are available to work on projects.</span></span> <span data-ttu-id="4a462-160">Они могут использовать эту информацию в качестве одного критерия при выполнении многокритериального анализа решений во время выполнения ресурса.</span><span class="sxs-lookup"><span data-stu-id="4a462-160">They can use this information as one criterion when they perform multi-criteria decision analysis during resource fulfillment.</span></span> <span data-ttu-id="4a462-161">Они также могут добавлять в фильтр другие характеристики ресурсов для поиска ресурсов, обладающих определенными навыками, образованием и опытом для данного проекта.</span><span class="sxs-lookup"><span data-stu-id="4a462-161">They can also add other resource characteristics to the filter to search for resources that have specific skills, education, and experience for a given project.</span></span>

<span data-ttu-id="4a462-162">**Сценарий:** утвержденный проект начат, и роль старшего менеджера проекта была зарезервирована в качестве запланированного ресурса на этапе планирования проекта.</span><span class="sxs-lookup"><span data-stu-id="4a462-162">**Scenario:** An approved project has started, and the Senior project manager role was reserved as a planned resource during the project planning stage.</span></span> <span data-ttu-id="4a462-163">Менеджер ресурсов теперь получил ресурс для выполнения роли старшего менеджера проекта.</span><span class="sxs-lookup"><span data-stu-id="4a462-163">The resource manager has now acquired a resource to fulfill the Senior project manager role.</span></span>

1. <span data-ttu-id="4a462-164">На странице **Список ресурсов** выберите **Даниэль Гольдшмидт**.</span><span class="sxs-lookup"><span data-stu-id="4a462-164">On the **Resources list** page, select **Daniel Goldschmidt**.</span></span>
2. <span data-ttu-id="4a462-165">На странице **Роль ресурса** выберите **Создать** и введите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="4a462-165">On the **Resource role** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="4a462-166">**Действует:** введите текущую дату.</span><span class="sxs-lookup"><span data-stu-id="4a462-166">**Effective:** Enter the current date.</span></span>
    - <span data-ttu-id="4a462-167">**Истекает:** Введите **Никогда**.</span><span class="sxs-lookup"><span data-stu-id="4a462-167">**Expiration:** Enter **Never**.</span></span>
    - <span data-ttu-id="4a462-168">**Роль:** введите **старший менеджер проекта**.</span><span class="sxs-lookup"><span data-stu-id="4a462-168">**Role:** Enter **Senior Project Manager**.</span></span>

3. <span data-ttu-id="4a462-169">Выберите **Сохранить** и закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="4a462-169">Select **Save**, and then close the page.</span></span>
4. <span data-ttu-id="4a462-170">На вкладке **Компетенции** добавьте навык **ProjectMgmt** и сертификат **PMP**.</span><span class="sxs-lookup"><span data-stu-id="4a462-170">On the **Competencies** tab, add the **ProjectMgmt** skill and the **PMP** certificate.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]