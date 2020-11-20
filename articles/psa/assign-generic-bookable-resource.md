---
title: Назначение универсальных резервируемых ресурсов задаче и проектной группе
description: В этом разделе приводятся сведения о резервировании универсальных ресурсов для задач и проектных групп.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 19761b3e570ad664522e832069a8ac50fffead64
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127084"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a><span data-ttu-id="2d7bc-103">Назначение универсальных резервируемые ресурсов задаче и требованиям универсальных ресурсов</span><span class="sxs-lookup"><span data-stu-id="2d7bc-103">Assign generic bookable resources to a task and generate resource requirements</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="2d7bc-104">Помимо резервирования и назначения именованных или реальных ресурсов вашему проекту, можно назначать универсальные ресурсы задачам проекта.</span><span class="sxs-lookup"><span data-stu-id="2d7bc-104">In addition to booking and assigning named or real resources to your project, you can assign generic resources to project tasks.</span></span> <span data-ttu-id="2d7bc-105">Эти ресурсы могут служить в качестве местозаполнителей для именованных ресурсов, пока вы не будете готовы набрать персонал в проект с именованными ресурсами.</span><span class="sxs-lookup"><span data-stu-id="2d7bc-105">These resources can serve as placeholders for named resources until you are ready to staff your project with named resources.</span></span> 

1. <span data-ttu-id="2d7bc-106">В Project Service Automation (PSA) откройте страницу **Проект** и на вкладке **Расписание** введите название должности универсального ресурса в ячейке **Ресурс** в расписании.</span><span class="sxs-lookup"><span data-stu-id="2d7bc-106">In Project Service Automation (PSA), open the **Project** page and on the **Schedule** tab, enter the position name of the generic resource in the **Resource** cell of the schedule.</span></span> <span data-ttu-id="2d7bc-107">Или щелкните значок **Ресурс** в ячейке для открытия средства выбора ресурса, затем введите имя универсального ресурса, который нужно создать.</span><span class="sxs-lookup"><span data-stu-id="2d7bc-107">Or, click the **Resource** icon in the cell to open the resource picker and then enter the name of the generic resource that you want to create.</span></span>

![Создание и назначение универсального участника рабочей группы](media/RM-how-to-9.png)

<span data-ttu-id="2d7bc-109">При этом откроется панель **Быстрое создание: Участник проектной группы**.</span><span class="sxs-lookup"><span data-stu-id="2d7bc-109">This will open the **Quick Create: Project Team Member** panel.</span></span> 

2. <span data-ttu-id="2d7bc-110">Введите роль и подразделение универсального ресурса участника рабочей группы, затем щелкните **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="2d7bc-110">Enter the role and organization unit of the generic resource team member and then click **Save**.</span></span>

![Быстрое создание универсального участника рабочей группы](media/RM-how-to-10.png)

3. <span data-ttu-id="2d7bc-112">После создания нового универсального ресурса участника рабочей группы он назначается задаче.</span><span class="sxs-lookup"><span data-stu-id="2d7bc-112">After you have created the new generic resource team member, it is assigned to the task.</span></span> <span data-ttu-id="2d7bc-113">Вы можете продолжить назначить этот универсальный ресурс другим задачам в расписании задач.</span><span class="sxs-lookup"><span data-stu-id="2d7bc-113">You can continue to assign that generic resource to other tasks in the task schedule.</span></span>

![Назначение существующего универсального участника рабочей группы задачам](media/RM-how-to-11.png)

4. <span data-ttu-id="2d7bc-115">После назначения универсального ресурса можно создать требование ресурса и заполнить его, напрямую зарезервировав или отправив запрос ресурса руководителю по ресурсам.</span><span class="sxs-lookup"><span data-stu-id="2d7bc-115">After you have assigned the generic resource, you can generate a resource requirement and fulfill it by directly booking or submitting a resource request to a resource manager.</span></span>

![Создание требования для универсального участника рабочей группы](media/RM-how-to-12.png)

<span data-ttu-id="2d7bc-117">В сетке участников рабочей группы, помимо использования упомянутого выше средства выбора ресурсов, можно добавлять универсальные ресурсы напрямую.</span><span class="sxs-lookup"><span data-stu-id="2d7bc-117">On the team member grid, in addition to being able to use the resource picker as mentioned above, you can add generic resources directly.</span></span> <span data-ttu-id="2d7bc-118">Ресурсы добавляются с требованием ресурса, которое основано на датах начала и окончания и методе распределение, указанным на панели **Быстрое создание: участник проектной группы**.</span><span class="sxs-lookup"><span data-stu-id="2d7bc-118">The resources are added with a resource requirement that is based on the start/end dates and allocation method specified in the **Quick Create: Project Team Member** panel.</span></span>

<span data-ttu-id="2d7bc-119">Вы можете видеть различие, если добавляете универсального участника рабочей группы напрямую, затем назначаете дополнительные задачи в универсальный ресурс, когда у них есть необходимые часы для покрытия.</span><span class="sxs-lookup"><span data-stu-id="2d7bc-119">You can see a difference if you add the generic team member directly and then assign more tasks to the generic resource than they have required hours to cover.</span></span> <span data-ttu-id="2d7bc-120">Щелкните **Создать требование**, чтобы заново создать требование и сбалансировать необходимые часы и назначения.</span><span class="sxs-lookup"><span data-stu-id="2d7bc-120">Click **Generate Requirement** to regenerate the requirement to balance the required hours against assignments.</span></span>

<span data-ttu-id="2d7bc-121">Можно также нажать ссылку **Требование ресурса** в сетке рабочей группы для открытия требования и добавления и добавления квалификации, предпочитаемых ресурсов и т. д.</span><span class="sxs-lookup"><span data-stu-id="2d7bc-121">You can also click the **Resource requirement** link in the team grid to open the requirement and add skills, preferred resources, etc.</span></span>

![Требование ресурса](media/RM-how-to-13.png)

