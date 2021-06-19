---
title: Оцените продажи и затраты по проекту, если резервируемый ресурс выполняет несколько ролей для проекта.
description: В этом разделе представлена информация о том, как использовать измерения цен для поддержки ценообразования и стоимости ресурса, который выполняет несколько ролей в проекте.
author: rumant
ms.custom:
- dyn365-projectservice
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
ms.openlocfilehash: 5b2b57f5268a92168952b6da5123886df70cd4e2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013277"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-for-a-project"></a><span data-ttu-id="fd42c-103">Оцените продажи и затраты по проекту, если резервируемый ресурс выполняет несколько ролей для проекта.</span><span class="sxs-lookup"><span data-stu-id="fd42c-103">Estimate project sales and costs when a bookable resource fills multiple roles for a project</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="fd42c-104">Компаниям, работающим на основе проектов, часто требуется один ресурс для выполнения нескольких ролей в проекте.</span><span class="sxs-lookup"><span data-stu-id="fd42c-104">Project-based companies often have the need for one resource to perform multiple roles on a project.</span></span> <span data-ttu-id="fd42c-105">Каждая из этих ролей может оцениваться и оплачиваться по-разному, что означает, что время, затрачиваемое одним и тем же ресурсом на проект, может получить различную финансовую оценку в зависимости от счета и ставок затрат для каждой из ролей.</span><span class="sxs-lookup"><span data-stu-id="fd42c-105">Each of these roles could be priced and costed differently, which means the same resource's time on the project could get a different financial estimate depending on the bill and cost rates for each of the roles.</span></span> <span data-ttu-id="fd42c-106">Project Service Automation позволяет настраивать значения в записи члена группы для именованного ресурса и допускает различные переопределения для каждой задачи, которой назначен член группы.</span><span class="sxs-lookup"><span data-stu-id="fd42c-106">Project Service Automation allows the setup of the values on the team member record for the named resource and allows for different overrides on each of the tasks that the team member is assigned to.</span></span>

<span data-ttu-id="fd42c-107">В следующем примере объясняется, как простое переопределение этого значения позволяет ресурсу иметь несколько ролей в проекте с разными затратами и ставками счетов.</span><span class="sxs-lookup"><span data-stu-id="fd42c-107">The following example  explains how the simple override of this value allows a resource to have multiple roles on a project with different cost and bill rates.</span></span>

## <a name="create-tasks"></a><span data-ttu-id="fd42c-108">Создание задач</span><span class="sxs-lookup"><span data-stu-id="fd42c-108">Create tasks</span></span>
<span data-ttu-id="fd42c-109">Создайте две задачи проекта на 40 часов каждая, задача A и задача B. Выберите задачу A в качестве предшественницы задачи B.</span><span class="sxs-lookup"><span data-stu-id="fd42c-109">Create two project tasks for 40 hours each, Task A and Task B. Select Task A as a predecessor to Task B.</span></span>

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a><span data-ttu-id="fd42c-110">Настройка роли и подразделения для типового члена рабочей группы проекта</span><span class="sxs-lookup"><span data-stu-id="fd42c-110">Set up Role and Organization Unit for a generic project team member</span></span>

1. <span data-ttu-id="fd42c-111">На странице **Расписание** выберите строку **Задача** для задачи A.</span><span class="sxs-lookup"><span data-stu-id="fd42c-111">On the **Schedule** page, select the **Task** row for Task A.</span></span> 
2. <span data-ttu-id="fd42c-112">В поле **Ресурсы** выберите **Создать** в раскрывающемся списке.</span><span class="sxs-lookup"><span data-stu-id="fd42c-112">In the **Resources** field, select **Create** in the drop-down list.</span></span>
3. <span data-ttu-id="fd42c-113">На странице **Быстрое создание члена команды** укажите атрибуты типового члена рабочей группы, который может выполнить эту задачу.</span><span class="sxs-lookup"><span data-stu-id="fd42c-113">On the **Team Member Quick Create** page, specify the attributes of the generic team member who can perform this task.</span></span>
4. <span data-ttu-id="fd42c-114">Выберите соответствующую роль и организационное подразделение, а затем выберите **Сохранить и закрыть**.</span><span class="sxs-lookup"><span data-stu-id="fd42c-114">Select the appropriate role and organizational unit, and then select **Save and Close**.</span></span> <span data-ttu-id="fd42c-115">Создается типовой член рабочей группы, которому назначается эта задача.</span><span class="sxs-lookup"><span data-stu-id="fd42c-115">A generic team member is created and assigned to this task.</span></span> 

<span data-ttu-id="fd42c-116">Повторите эти шаги для задачи B и убедитесь, что роль и подразделение типового члена рабочей группы, созданного для задачи B, отличается от задачи A.</span><span class="sxs-lookup"><span data-stu-id="fd42c-116">Repeat these steps for Task B and make sure that the role and organizational unit on the generic team member created for Task B is different than Task A.</span></span> 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a><span data-ttu-id="fd42c-117">Настройка роли и подразделения для задачи проекта</span><span class="sxs-lookup"><span data-stu-id="fd42c-117">Set up role and organization unit for a project task</span></span>

1. <span data-ttu-id="fd42c-118">После создания задачи A выберите эту задачу, затем выберите **Изменить задачу**.</span><span class="sxs-lookup"><span data-stu-id="fd42c-118">After you create Task A, select the task, and then select **Edit task**.</span></span>
2. <span data-ttu-id="fd42c-119">На странице **Сведения о задаче** найдите поля **Роль** и **Подразделение**, добавьте значения, необходимые для ресурса, который будет выполнять эту задачу.</span><span class="sxs-lookup"><span data-stu-id="fd42c-119">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="fd42c-120">Если вы выполняете эти сценарии с использованием демонстрационных данных Project Service Automation, выберите **Ведущий консультант** для роли и **Fabrikam US** в качестве подразделения.</span><span class="sxs-lookup"><span data-stu-id="fd42c-120">If you are completing this scenarios using Project Service Automation demo data, select **Consulting Lead** for the role, and **Fabrikam US** as the organizational unit.</span></span>

3. <span data-ttu-id="fd42c-121">Выберите задачу B, затем выберите **Изменить задачу**.</span><span class="sxs-lookup"><span data-stu-id="fd42c-121">Select Task B and then select **Edit task**.</span></span>
4. <span data-ttu-id="fd42c-122">На странице **Сведения о задаче** найдите поля **Роль** и **Подразделение**, добавьте значения, необходимые для ресурса, который будет выполнять эту задачу.</span><span class="sxs-lookup"><span data-stu-id="fd42c-122">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> <span data-ttu-id="fd42c-123">Убедитесь, что значения в полях **Роль** и **Подразделение** для задачи B отличаются от значений для задачи A.</span><span class="sxs-lookup"><span data-stu-id="fd42c-123">Make sure that the values in the **Role** and **Organizational Unit** fields are different for Task B from the values for Task A.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="fd42c-124">Если вы выполняете эти сценарии с использованием демонстрационных данных Project Service Automation, выберите **Специалист по сетям** для роли и **Fabrikam US** в качестве подразделения.</span><span class="sxs-lookup"><span data-stu-id="fd42c-124">If you are completing this scenarios using Project Service Automation demo data, select **Network Technician** for the role, and **Fabrikam US** as the organizational unit.</span></span>

5. <span data-ttu-id="fd42c-125">Сохраните и закройте страницу **Сведения о задаче**.</span><span class="sxs-lookup"><span data-stu-id="fd42c-125">Save and close the **Task Details** page.</span></span> 

## <a name="team-member-and-estimates-behavior"></a><span data-ttu-id="fd42c-126">Участник рабочей группы и поведение оценок</span><span class="sxs-lookup"><span data-stu-id="fd42c-126">Team member and estimates behavior</span></span> 

1. <span data-ttu-id="fd42c-127">На странице **Сведения о задаче** в разделе **Участник рабочей группы** выберите двух типовых участников рабочей группы, затем выберите **Создать требования**.</span><span class="sxs-lookup"><span data-stu-id="fd42c-127">On the **Task Details** page, on the **Team Member**, select the two generic team Members and then select **Generate Requirements**.</span></span> 
2. <span data-ttu-id="fd42c-128">Выберите строку участника рабочей группы для роли **Ведущий консультант**, затем выберите **Зарезервировать**.</span><span class="sxs-lookup"><span data-stu-id="fd42c-128">Select the team member row for **Consulting Lead** and then select **Book**.</span></span> <span data-ttu-id="fd42c-129">Доска расписания откроется и зарезервирует ресурс для этого требования.</span><span class="sxs-lookup"><span data-stu-id="fd42c-129">The schedule board opens and books a resource to that requirement.</span></span>
3. <span data-ttu-id="fd42c-130">Выберите строку участника рабочей группы для роли **Специалист по сетям** и выберите **Зарезервировать**.</span><span class="sxs-lookup"><span data-stu-id="fd42c-130">Select the team member row for **Network Technician** and the select **Book**.</span></span> <span data-ttu-id="fd42c-131">Доска расписания откроется и зарезервирует этот же ресурс для этого требования.</span><span class="sxs-lookup"><span data-stu-id="fd42c-131">The schedule board opens and books the same resource on that requirement.</span></span>

### <a name="team-member-grid"></a><span data-ttu-id="fd42c-132">Сетка участников рабочей группы</span><span class="sxs-lookup"><span data-stu-id="fd42c-132">Team Member grid</span></span> 
<span data-ttu-id="fd42c-133">В сетке **Участник рабочей группы** обратите внимание, что две записи типовых участников рабочей группы удалены и заменены одним ресурсом.</span><span class="sxs-lookup"><span data-stu-id="fd42c-133">On the **Team Member** grid, notice that the two generic team member records are deleted and have been replaced one resource.</span></span> <span data-ttu-id="fd42c-134">Для этого ресурса существует один набор значений, который показывает набор значений по умолчанию для параметров **Роль** и **Подразделение**.</span><span class="sxs-lookup"><span data-stu-id="fd42c-134">There is one set of values for that resource that shows a default set of values for **Role** and **Organizational Unit**.</span></span>
<span data-ttu-id="fd42c-135">Когда вы разворачиваете строку этой записи участника рабочей группы, вы можете увидеть отдельные назначения в записи участника рабочей группы для обеих этих задач.</span><span class="sxs-lookup"><span data-stu-id="fd42c-135">When you expand the row of that Team Member record, you can see distinct assignments on the team member record for both of those tasks.</span></span> <span data-ttu-id="fd42c-136">В каждой строке назначения указаны значения для конкретных задач для параметров **Роль** и **Подразделение**.</span><span class="sxs-lookup"><span data-stu-id="fd42c-136">Each assignment row has task-specific values for **Role** and **Organizational Unit**.</span></span> 

### <a name="estimates-grid"></a><span data-ttu-id="fd42c-137">Сетка оценок</span><span class="sxs-lookup"><span data-stu-id="fd42c-137">Estimates grid</span></span> 
<span data-ttu-id="fd42c-138">Когда вы перейдете к сетке **Оценки**, вы заметите, что оба назначения для одного и того же ресурса расцениваются по-разному.</span><span class="sxs-lookup"><span data-stu-id="fd42c-138">When you navigate to the **Estimates** grid, you will notice that both assignments for the same resource are priced differently.</span></span>
<span data-ttu-id="fd42c-139">Назначение ресурса для задачи A расценивается с использованием атрибута **Роль** со значением **Ведущий консультант**.</span><span class="sxs-lookup"><span data-stu-id="fd42c-139">The assignment for the resource on Task A is priced using the **Role** attribute value of **Consulting Lead**.</span></span> <span data-ttu-id="fd42c-140">Назначение этого же ресурса для задачи B расценивается с использованием атрибута **Роль** со значением **Специалист по сетям**.</span><span class="sxs-lookup"><span data-stu-id="fd42c-140">The assignment for the same resource on Task B is priced using the **Role** attribute value of **Network Technician**.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]