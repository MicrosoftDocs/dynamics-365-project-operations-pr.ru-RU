---
title: Шаблоны проектов
description: В этом разделе представлена информация о том, как использовать шаблоны проектов для быстрой настройки проекта.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: f0161bf9-af4c-4a21-b767-ac20a8e30688
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5a3112c2eef9525946314bdb587c44904557fa52
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754929"
---
# <a name="project-templates"></a><span data-ttu-id="c1a26-103">Шаблоны проектов</span><span class="sxs-lookup"><span data-stu-id="c1a26-103">Project templates</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="c1a26-104">Шаблон проекта — это предварительно определенная структура, которая помогает быстро и легко начать проект.</span><span class="sxs-lookup"><span data-stu-id="c1a26-104">A project template is a predefined framework that helps you quickly and easily start a project.</span></span> <span data-ttu-id="c1a26-105">Можно использовать предварительно заданный шаблон для создания нового проекта одним щелчком.</span><span class="sxs-lookup"><span data-stu-id="c1a26-105">You can use a predefined template to create a new project with a single click.</span></span> <span data-ttu-id="c1a26-106">В отношении проектов необходимо определить обязательные условия для шаблонов проекта.</span><span class="sxs-lookup"><span data-stu-id="c1a26-106">As for projects, you must define the prerequisites for project templates.</span></span> <span data-ttu-id="c1a26-107">Следует задать календарь по проекту для каждого шаблона проекта, и роли и прайс-листы необходимо предопределить в организации, чтобы эти компоненты шаблона содержали полезные данные.</span><span class="sxs-lookup"><span data-stu-id="c1a26-107">You must define a project calendar for each project template, and roles and price lists must be predefined in the organization, so that the components of the template have useful data.</span></span>

<span data-ttu-id="c1a26-108">Шаблон проекта состоит из трех компонентов: расписание, оценки проекта и участники проектной группы.</span><span class="sxs-lookup"><span data-stu-id="c1a26-108">A project template consists of three components: a schedule, project estimates, and project team members.</span></span>

## <a name="schedule"></a><span data-ttu-id="c1a26-109">Расписание</span><span class="sxs-lookup"><span data-stu-id="c1a26-109">Schedule</span></span>

<span data-ttu-id="c1a26-110">Расписание в шаблоне проекта имеет тот же набор элементов, что и расписание в проекте.</span><span class="sxs-lookup"><span data-stu-id="c1a26-110">A schedule in a project template has the same set of elements as a schedule in a project.</span></span> <span data-ttu-id="c1a26-111">Можно создать иерархию задач, связать роли с задачами, определить атрибуты расписания и задать зависимости.</span><span class="sxs-lookup"><span data-stu-id="c1a26-111">You can create a task hierarchy, associate roles with tasks, define schedule attributes, and set dependencies.</span></span> <span data-ttu-id="c1a26-112">Расписание в шаблоне проекта также поддерживает режимы задачи для каждой задачи.</span><span class="sxs-lookup"><span data-stu-id="c1a26-112">A schedule in a project template also supports task modes for each task.</span></span> <span data-ttu-id="c1a26-113">Следовательно, оно поддерживает подсистему планирования.</span><span class="sxs-lookup"><span data-stu-id="c1a26-113">Therefore, it supports the scheduling engine.</span></span> <span data-ttu-id="c1a26-114">Необходимо связать календарь проекта с проектом.</span><span class="sxs-lookup"><span data-stu-id="c1a26-114">You must associate a project calendar with the project.</span></span> <span data-ttu-id="c1a26-115">При составлении рабочего расписания нет разницы между шаблоном проекта и проектом.</span><span class="sxs-lookup"><span data-stu-id="c1a26-115">When you create a work schedule, there is no difference between a project template and a project.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="c1a26-116">Оценки проекта</span><span class="sxs-lookup"><span data-stu-id="c1a26-116">Project estimates</span></span>

<span data-ttu-id="c1a26-117">Оценки проекта в шаблоне проекта работают таким же образом, как и оценки проекта в проекте.</span><span class="sxs-lookup"><span data-stu-id="c1a26-117">Project estimates in a project template work the same way as project estimates in a project.</span></span> <span data-ttu-id="c1a26-118">Однако затраты и продажные цены извлекаются из прайс-листов стоимости и продаж по умолчанию, которые определены в параметрах.</span><span class="sxs-lookup"><span data-stu-id="c1a26-118">However, the cost and sales prices are pulled from the default cost and sales price lists that are defined in the parameters.</span></span>

## <a name="creating-a-project-from-a-template"></a><span data-ttu-id="c1a26-119">Создание проекта из шаблона</span><span class="sxs-lookup"><span data-stu-id="c1a26-119">Creating a project from a template</span></span>
 
<span data-ttu-id="c1a26-120">Существует несколько способов создания проекта из шаблона проекта:</span><span class="sxs-lookup"><span data-stu-id="c1a26-120">There are several ways to create a project from a project template:</span></span>

- <span data-ttu-id="c1a26-121">При создании проекта из предложения с расценками можно выбрать шаблон проекта в диалоговом окне **Быстрое создание: Проект**.</span><span class="sxs-lookup"><span data-stu-id="c1a26-121">When you create a project from a quote, you can select a project template in the **Quick Create: Project** dialog box.</span></span>

> ![Диалоговое окно "Быстрое создание: проект"](media/project-11.png)

- <span data-ttu-id="c1a26-123">При создании нового проекта путем выбора пункта **Создать проект**, страница **Проект** отображается перед сохранением записи.</span><span class="sxs-lookup"><span data-stu-id="c1a26-123">When you create a project by selecting **New Project**, the **Project** page appears before the record is saved.</span></span> <span data-ttu-id="c1a26-124">В поле **Выберите шаблон** выберите один из предопределенных шаблонов проекта в организации.</span><span class="sxs-lookup"><span data-stu-id="c1a26-124">In the **Pick a Template** field, select one of the predefined project templates in the organization.</span></span>
- <span data-ttu-id="c1a26-125">Используйте **Создание проекта из шаблона** на странице **Сущность шаблона**.</span><span class="sxs-lookup"><span data-stu-id="c1a26-125">Use **Create Project from a Template** on the **Template Entity** page.</span></span>

## <a name="copying-components-of-template-to-project"></a><span data-ttu-id="c1a26-126">Копирование компонентов шаблона в проект</span><span class="sxs-lookup"><span data-stu-id="c1a26-126">Copying components of template to project</span></span>

<span data-ttu-id="c1a26-127">При копировании компонентов шаблона проекта в проект несколько переопределений выполняется, в зависимости от настроек в проекте.</span><span class="sxs-lookup"><span data-stu-id="c1a26-127">When you copy the components of a project template to a project, a few overrides can occur, depending on the settings in the project.</span></span>

### <a name="copying-the-schedule"></a><span data-ttu-id="c1a26-128">Копирование расписания</span><span class="sxs-lookup"><span data-stu-id="c1a26-128">Copying the schedule</span></span>

<span data-ttu-id="c1a26-129">При копировании расписания из шаблона проекта рабочие часы из календаря проекта применяются к расписанию задач, если календарь проекта отличается от календаря шаблона.</span><span class="sxs-lookup"><span data-stu-id="c1a26-129">When you copy the schedule from a project template, if the project has a different project calendar than the template, work hours from the project's calendar are applied to the task schedule.</span></span> <span data-ttu-id="c1a26-130">Таким образом расписание корректируется в соответствии со связанным календарем проекта.</span><span class="sxs-lookup"><span data-stu-id="c1a26-130">In this way, the schedule is adjusted to match the backing project calendar.</span></span> <span data-ttu-id="c1a26-131">Аналогично первая задача в расписании принимает дату начала проекта, и расписание остальной иерархии обновляется с учетом продолжительности и зависимостей, определенных в шаблоне.</span><span class="sxs-lookup"><span data-stu-id="c1a26-131">Similarly, the first task on the schedule takes the project's start date, and the schedule of the rest of the hierarchy is updated based on the duration and dependencies that are specified in the template.</span></span> 

### <a name="copying-project-estimates"></a><span data-ttu-id="c1a26-132">Копирование оценок проекта</span><span class="sxs-lookup"><span data-stu-id="c1a26-132">Copying project estimates</span></span> 

<span data-ttu-id="c1a26-133">При копировании между строками оценки проекта прайс-листы обновляются.</span><span class="sxs-lookup"><span data-stu-id="c1a26-133">When you copy across project estimate lines, the price lists are updated.</span></span> <span data-ttu-id="c1a26-134">Для списка себестоимости эти обновления основаны на подразделении, отвечающем за проект.</span><span class="sxs-lookup"><span data-stu-id="c1a26-134">For the cost price list, these updates are based on the owning unit of the project.</span></span> <span data-ttu-id="c1a26-135">Для прайс-листа продаж они основаны на клиенте.</span><span class="sxs-lookup"><span data-stu-id="c1a26-135">For the sales price list, they are based on the customer.</span></span> <span data-ttu-id="c1a26-136">Для проектов, которые связаны с сущностью продаж, стоимость единицы и цены продажи определяются на основе этих прейскурантов.</span><span class="sxs-lookup"><span data-stu-id="c1a26-136">For projects that are associated with a sales entity, the unit cost and sales prices are determined based on these price lists.</span></span>

### <a name="copying-a-project-team"></a><span data-ttu-id="c1a26-137">Копирование проектной группы</span><span class="sxs-lookup"><span data-stu-id="c1a26-137">Copying a project team</span></span>

<span data-ttu-id="c1a26-138">При копировании рабочей группы проекта из шаблона проекта в проект, универсальные ресурсы копируются вместе с навыками и компетенциями, определенными в шаблоне.</span><span class="sxs-lookup"><span data-stu-id="c1a26-138">When a project team is copied from a project template to a project, the generic resources are copied, together with the skills and proficiencies that are defined in the template.</span></span> <span data-ttu-id="c1a26-139">Назначения универсальных ресурсов также обслуживаются как в шаблоне проекта.</span><span class="sxs-lookup"><span data-stu-id="c1a26-139">Generic resource assignments are also maintained as they were in the project template.</span></span> <span data-ttu-id="c1a26-140">Именованные ресурсы не поддерживаются в шаблонах проектов.</span><span class="sxs-lookup"><span data-stu-id="c1a26-140">Named resources aren't supported in project templates.</span></span>
