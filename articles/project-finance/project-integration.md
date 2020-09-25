---
title: Интеграция Microsoft Project Client
description: Планирование и ведение графика проекта может быть сложной задачей, поэтому руководителям проектов необходимо использовать инструменты, которые помогают им справляться с этой задачей. Интеграция с Microsoft Project Client обеспечивает поддержку для открытия и управления структурной декомпозицией работ.
author: KimANelson
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: c6478e05-50ee-4993-87f4-6ce9cb78f076
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: e35e1e54bad659d1329c333479830b680a17cbb0
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755016"
---
# <a name="microsoft-project-client-integration"></a><span data-ttu-id="8e8ca-104">Интеграция Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="8e8ca-104">Microsoft Project client integration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8e8ca-105">Планирование и ведение графика проекта может быть сложной задачей, поэтому руководителям проектов необходимо использовать инструменты, которые помогают им справляться с этой задачей.</span><span class="sxs-lookup"><span data-stu-id="8e8ca-105">Planning and maintaining a project schedule can be complex, so project managers need to use tools that help them manage this task.</span></span> <span data-ttu-id="8e8ca-106">Интеграция с Microsoft Project Client обеспечивает поддержку для открытия и управления структурной декомпозицией работ.</span><span class="sxs-lookup"><span data-stu-id="8e8ca-106">Integration with Microsoft Project Client provides support to open and manage a project work breakdown structure.</span></span> <span data-ttu-id="8e8ca-107">Менеджер проекта может публиковать любые изменения обратно в структурную декомпозицию работ проекта Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="8e8ca-107">The project manager can publish any changes back to the Dynamics 365 Finance project work breakdown structure.</span></span>

> [!NOTE]
> <span data-ttu-id="8e8ca-108">Если вы используете июльское обновление (версия 10.0.4), вы должны установить KB 4054797 и 4055884.</span><span class="sxs-lookup"><span data-stu-id="8e8ca-108">If you are using the July update (version 10.0.4), you must install KB 4054797 and 4055884.</span></span>

## <a name="configure-the-microsoft-project-client-add-in"></a><span data-ttu-id="8e8ca-109">Конфигурация надстройки Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="8e8ca-109">Configure the Microsoft Project Client add-in</span></span>
<span data-ttu-id="8e8ca-110">Чтобы включить интеграцию с Microsoft Project Client, следует установить надстройку Microsoft Dynamics 365 в клиентском приложении Microsoft Project пользователя.</span><span class="sxs-lookup"><span data-stu-id="8e8ca-110">To enable the integration with Microsoft Project Client, a Microsoft Dynamics 365 add-in is required to be installed in the user’s client Microsoft Project application.</span></span> <span data-ttu-id="8e8ca-111">Это делается путем открытия **Рабочее пространство управления проектами**.</span><span class="sxs-lookup"><span data-stu-id="8e8ca-111">This is done by opening the **Project management workspace**.</span></span>

<span data-ttu-id="8e8ca-112">•   Щелкните **Настроить надстройку клиента проекта** в разделе **Ссылки** > **Настройка** рабочего пространства.</span><span class="sxs-lookup"><span data-stu-id="8e8ca-112">•   Click **Configure project client add-in** from the **Links** > **Setup** section of the workspace.</span></span>

<span data-ttu-id="8e8ca-113">•   Щелкните **Открыть**, затем щелкните **Выполнить** при появлении запроса.</span><span class="sxs-lookup"><span data-stu-id="8e8ca-113">•   Click **Open**, then click **Run** when prompted.</span></span>

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a><span data-ttu-id="8e8ca-114">Открытие и редактирование существующей черновой структурной декомпозиции работ в Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="8e8ca-114">Open and edit an existing draft work breakdown structure in Microsoft Project Client</span></span>
<span data-ttu-id="8e8ca-115">Если для проекта в Dynamics 365 Finance структурная декомпозиция работ уже создана, структурную декомпозицию работ можно открыть в приложении Microsoft Project Client, если структурная декомпозиция работ находится в состоянии черновика.</span><span class="sxs-lookup"><span data-stu-id="8e8ca-115">If a project in Dynamics 365 Finance already has a work breakdown structure created, the work breakdown structure can be opened in the Microsoft Project Client application if the work breakdown structure is in a draft status.</span></span> <span data-ttu-id="8e8ca-116">Чтобы открыть на странице **Проект**, щелкните ссылку **Открыть в Microsoft Project** на вкладке **План**. Эту страницу также можно открыть из приложения Microsoft Project Client, нажав **Открыть** на вкладке **Microsoft Dynamics 365**. Выберите **Юридическое лицо** и **Проект** из списка.</span><span class="sxs-lookup"><span data-stu-id="8e8ca-116">To open from the **Project** page, click **Open in Microsoft Project** link from the **Plan** tab. This page can also be opened from within the Microsoft Project Client application by clicking **Open** in the **Microsoft Dynamics 365** tab. Select the **Legal entity** and **Project** from the list.</span></span>

> [!NOTE]
> <span data-ttu-id="8e8ca-117">Если вы используете Internet Explorer в качестве браузера, вам нужно будет нажать **Сохранить** для открытия вручную из того места, куда загружен файл.</span><span class="sxs-lookup"><span data-stu-id="8e8ca-117">If you're using Internet Explorer as your browser, you will need to click **Save** to manually open from the location that the file is downloaded to.</span></span> <span data-ttu-id="8e8ca-118">Или щелкните **Сохранить и открыть**, чтобы открыть файл в Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="8e8ca-118">Or, click **Save and open** to open the file in Microsoft Project Client.</span></span> <span data-ttu-id="8e8ca-119">Не переименовывайте имя файла при сохранении.</span><span class="sxs-lookup"><span data-stu-id="8e8ca-119">Do not rename the file name when saving.</span></span>

<span data-ttu-id="8e8ca-120">Прежде чем вносить какие-либо изменения в файл с помощью Microsoft Project Client, вам необходимо проверить его. Нажмите **Проверить** на вкладке **Microsoft Dynamics 365**. Это предотвратит одновременное редактирование иерархической структуры работ из Finance другими пользователями.</span><span class="sxs-lookup"><span data-stu-id="8e8ca-120">Before making any edits to the file using Microsoft Project Client, you need to check it out. Click **Check out** in the **Microsoft Dynamics 365** tab. This will prevent other users from editing the work breakdown structure from within Finance at the same time.</span></span> <span data-ttu-id="8e8ca-121">Чтобы опубликовать структурную декомпозицию работ после внесения любых изменений, щелкните **Вернуть** на вкладке **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="8e8ca-121">To publish the work breakdown structure after completing any edits, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

<span data-ttu-id="8e8ca-122">Если группа проекта уже добавлена к проекту в Finance, список ресурсов будет заполнен участниками группы.</span><span class="sxs-lookup"><span data-stu-id="8e8ca-122">If a project team has already been added to the project in Finance, the resource list will be populated with the team members.</span></span> <span data-ttu-id="8e8ca-123">Если рабочая группа проекта еще не добавлена в проект, вы можете выбрать ресурсы и создать рабочую группу в Microsoft Project Client, нажав кнопку **Ресурсы** на вкладке **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="8e8ca-123">If a project team has not yet been added to the project, you can select resources and build the team within Microsoft Project Client by clicking the **Resources** button on the **Microsoft Dynamics 365** tab.</span></span> 

<span data-ttu-id="8e8ca-124">Следующие данные будут синхронизированы с Finance как часть процесса возврата:</span><span class="sxs-lookup"><span data-stu-id="8e8ca-124">The following data will be synced back to Finance as part of the check-in process:</span></span>

<span data-ttu-id="8e8ca-125">•   Имя задачи</span><span class="sxs-lookup"><span data-stu-id="8e8ca-125">•   Task name</span></span>

<span data-ttu-id="8e8ca-126">•   Дата начала</span><span class="sxs-lookup"><span data-stu-id="8e8ca-126">•   Start date</span></span>

<span data-ttu-id="8e8ca-127">•   Дата окончания</span><span class="sxs-lookup"><span data-stu-id="8e8ca-127">•   Finish date</span></span>

<span data-ttu-id="8e8ca-128">•   Предшественники</span><span class="sxs-lookup"><span data-stu-id="8e8ca-128">•   Predecessors</span></span>

<span data-ttu-id="8e8ca-129">•   Имена ресурсов</span><span class="sxs-lookup"><span data-stu-id="8e8ca-129">•   Resource names</span></span>

<span data-ttu-id="8e8ca-130">•   Категория</span><span class="sxs-lookup"><span data-stu-id="8e8ca-130">•   Category</span></span>

<span data-ttu-id="8e8ca-131">•   Категория ресурса</span><span class="sxs-lookup"><span data-stu-id="8e8ca-131">•   Resource category</span></span>

<span data-ttu-id="8e8ca-132">•   Рабочие часы</span><span class="sxs-lookup"><span data-stu-id="8e8ca-132">•   Work hours</span></span>

<span data-ttu-id="8e8ca-133">•   Примечания</span><span class="sxs-lookup"><span data-stu-id="8e8ca-133">•   Notes</span></span>

<span data-ttu-id="8e8ca-134">•   Приоритет</span><span class="sxs-lookup"><span data-stu-id="8e8ca-134">•   Priority</span></span>

> [!NOTE]
> <span data-ttu-id="8e8ca-135">Если вы добавите какие-либо другие столбцы в файл клиента Microsoft Project,Microsoft Project Client, они не будут сохранены в файле и не будут отображаться при повторном открытии файла.</span><span class="sxs-lookup"><span data-stu-id="8e8ca-135">If you add any other columns to your Microsoft Project Client file, they will not be saved to the file and will not be displayed when the file is opened again.</span></span>

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="8e8ca-136">Создайте структурную декомпозицию работ для существующего проекта с помощью Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="8e8ca-136">Create the work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="8e8ca-137">Чтобы создать структурную декомпозицию работ с помощью Microsoft Project Client выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="8e8ca-137">To create a new work breakdown structure using Microsoft Project Client, follow these steps:</span></span>


1.  <span data-ttu-id="8e8ca-138">Откройте Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="8e8ca-138">Open Microsoft Project Client.</span></span>

2.  <span data-ttu-id="8e8ca-139">На вкладке **Microsoft Dynamics 365** щелкните **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="8e8ca-139">On the **Microsoft Dynamics 365** tab, click **Open**.</span></span>

3.  <span data-ttu-id="8e8ca-140">Выберите **Юридическое лицо** для проекта.</span><span class="sxs-lookup"><span data-stu-id="8e8ca-140">Select the **Legal entity** for the project.</span></span>

4.  <span data-ttu-id="8e8ca-141">Выберите **Проект**.</span><span class="sxs-lookup"><span data-stu-id="8e8ca-141">Select the **Project**.</span></span>

5.  <span data-ttu-id="8e8ca-142">Нажмите **Проверить** на вкладке **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="8e8ca-142">Click **Check out** on the **Microsoft Dynamics 365** tab.</span></span>

6.  <span data-ttu-id="8e8ca-143">Когда будете готовы опубликовать в Finance, щелкните **Вернуть** на вкладке **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="8e8ca-143">When ready to publish to Finance, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="8e8ca-144">Замените существующую структурную декомпозицию работ для существующего проекта с помощью Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="8e8ca-144">Replace the existing work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="8e8ca-145">Чтобы создать новую структурную декомпозицию работ с помощью Microsoft Project Client и заменить существующую структурную декомпозицию работ для существующего проекта, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="8e8ca-145">To create a new work breakdown structure using Microsoft Project Client and replace an existing work breakdown structure for an existing project, follow these steps:</span></span>

1.  <span data-ttu-id="8e8ca-146">Откройте Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="8e8ca-146">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="8e8ca-147">Создайте расписание Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="8e8ca-147">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="8e8ca-148">На вкладке **Microsoft Dynamics 365** щелкните **Сохранить изменения** > **Заменить существующий проект**.</span><span class="sxs-lookup"><span data-stu-id="8e8ca-148">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Replace existing project**.</span></span>

4.  <span data-ttu-id="8e8ca-149">Выберите **Юридическое лицо** для проекта.</span><span class="sxs-lookup"><span data-stu-id="8e8ca-149">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="8e8ca-150">Выберите **Проект**.</span><span class="sxs-lookup"><span data-stu-id="8e8ca-150">Select the **Project**.</span></span>

6.  <span data-ttu-id="8e8ca-151">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="8e8ca-151">Click **OK**.</span></span>

## <a name="create-a-new-project-from-within-microsoft-project-client"></a><span data-ttu-id="8e8ca-152">Создайте новый проект в Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="8e8ca-152">Create a new project from within Microsoft Project Client</span></span>


1.  <span data-ttu-id="8e8ca-153">Откройте Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="8e8ca-153">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="8e8ca-154">Создайте расписание Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="8e8ca-154">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="8e8ca-155">На вкладке **Microsoft Dynamics 365** щелкните **Сохранить изменения** > **Сохранить в новый проект**.</span><span class="sxs-lookup"><span data-stu-id="8e8ca-155">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Save to new Project**.</span></span>

4.  <span data-ttu-id="8e8ca-156">Выберите **Юридическое лицо** для проекта.</span><span class="sxs-lookup"><span data-stu-id="8e8ca-156">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="8e8ca-157">Введите **Идентификатор проекта**, если необходимо.</span><span class="sxs-lookup"><span data-stu-id="8e8ca-157">Enter the **Project ID**, if necessary.</span></span>

6.  <span data-ttu-id="8e8ca-158">Введите **Имя проекта**.</span><span class="sxs-lookup"><span data-stu-id="8e8ca-158">Enter the **Project name**.</span></span>

7.  <span data-ttu-id="8e8ca-159">Выберите **Тип проекта**, **Группа проектов** и **Код контракта по проекту**.</span><span class="sxs-lookup"><span data-stu-id="8e8ca-159">Select the **Project type**, **Project group** and the **Project contract ID**.</span></span> <span data-ttu-id="8e8ca-160">Кроме того, вы можете создать новый контракт по проекту, нажав **Создать**.</span><span class="sxs-lookup"><span data-stu-id="8e8ca-160">Alternatively, you can create a new project contract by clicking **New**.</span></span>

8.  <span data-ttu-id="8e8ca-161">Выберите **Календарь** для использования в качестве ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8e8ca-161">Select the **Calendar** to be used for resourcing.</span></span>

11. <span data-ttu-id="8e8ca-162">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="8e8ca-162">Click **OK**.</span></span>