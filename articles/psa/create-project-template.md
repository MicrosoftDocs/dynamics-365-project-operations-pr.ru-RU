---
title: Создание шаблона проекта
description: Как создать шаблон проекта в Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: efc404131208e1c971cb091cf174c1f4707552f0
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149379"
---
# <a name="create-a-project-template-project-service"></a><span data-ttu-id="67e40-103">Создание шаблона проекта (Project Service)</span><span class="sxs-lookup"><span data-stu-id="67e40-103">Create a project template (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="67e40-104">Шаблоны проектов позволяют сэкономить время, если компания регулярно подает заявки на аналогичные проекты.</span><span class="sxs-lookup"><span data-stu-id="67e40-104">Project templates save you time if your company regularly bids on similar types of projects.</span></span> <span data-ttu-id="67e40-105">Они предоставляют стандартный набор ролей и расчетное время (в часах) для конкретного типа проекта.</span><span class="sxs-lookup"><span data-stu-id="67e40-105">They provide a standard set of roles and estimated hours for a type of project.</span></span> <span data-ttu-id="67e40-106">Менеджеры по работе с клиентами и руководители проектов могут создавать проекты, основанные на шаблоне проекта, или копировать шаблон и создать на его основе собственный.</span><span class="sxs-lookup"><span data-stu-id="67e40-106">Account managers and project managers can create projects based on a project template, or they can copy the template and make one of their own.</span></span>  
  
## <a name="components-of-project-template"></a><span data-ttu-id="67e40-107">Компоненты шаблона проекта</span><span class="sxs-lookup"><span data-stu-id="67e40-107">Components of project template</span></span>
 <span data-ttu-id="67e40-108">Шаблон проекта состоит из трех компонентов.</span><span class="sxs-lookup"><span data-stu-id="67e40-108">A project template consists of three components:</span></span>  
  
- <span data-ttu-id="67e40-109">**Структурная декомпозиция работ**: структурная декомпозиция работ в шаблоне проекта имеет тот же набор элементов, что и в проекте.</span><span class="sxs-lookup"><span data-stu-id="67e40-109">**Work breakdown structure**: A work breakdown structure in a project template has the same set of elements as in the project.</span></span> <span data-ttu-id="67e40-110">Можно создать иерархию задач, связать роли с задачей, определить атрибуты расписания, назначить зависимости и просмотреть все данные в диаграмме Ганнта.</span><span class="sxs-lookup"><span data-stu-id="67e40-110">You can create a task hierarchy, associate roles to task, define schedule attributes, set dependencies and view all the data in the Gantt.</span></span> <span data-ttu-id="67e40-111">Структурная декомпозиция работ в шаблонах проекта также поддерживает режимы задач для каждой задачи.</span><span class="sxs-lookup"><span data-stu-id="67e40-111">The work breakdown structure in project templates also support task modes for each task.</span></span> <span data-ttu-id="67e40-112">При составлении рабочего расписания нет разницы между шаблоном проекта и проектом.</span><span class="sxs-lookup"><span data-stu-id="67e40-112">There is no difference between a project template and a project when creating work schedule.</span></span>  
  
- <span data-ttu-id="67e40-113">**Оценки проекта**: оценки проекта в шаблонах функционируют так же, как в проектах, с той разницей, что прейскуранты для определения себестоимости и цены продажи по умолчанию всегда являются прейскурантами себестоимости и цены продажи по умолчанию, определенными в параметрах [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="67e40-113">**Project estimates**: Project estimates in templates work the same way as they do in projects, except the price lists for defaulting the cost and sales prices are always the default cost and sales price lists defined in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] parameters.</span></span> <span data-ttu-id="67e40-114">Остальная функциональность — такая же, как в проекте.</span><span class="sxs-lookup"><span data-stu-id="67e40-114">The rest of the functionality is the same as in a project.</span></span>  
  
- <span data-ttu-id="67e40-115">**Образование проектной группы**: при создании проектной группы для шаблона проекта невозможно зарезервировать в шаблоне именованный ресурс.</span><span class="sxs-lookup"><span data-stu-id="67e40-115">**Project team formation**: When forming a project team for a project template, you can’t book a named resource in a template.</span></span> <span data-ttu-id="67e40-116">Можно использовать команду **Создать рабочую группу проекта** в структурной декомпозиции работ, чтобы создать набор универсальных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="67e40-116">You can use **Generate Project Team** in the work breakdown structure to generate a set of generic resources.</span></span> <span data-ttu-id="67e40-117">Кроме того, можно указать необходимые навыки и компетенции для универсальных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="67e40-117">You can also specify required skills and proficiencies for generic resources.</span></span> <span data-ttu-id="67e40-118">Невозможно заменить универсальный ресурс в шаблонах проекта резервируемым ресурсом.</span><span class="sxs-lookup"><span data-stu-id="67e40-118">You can’t substitute a generic resource with a bookable resource in project templates.</span></span>  
  
## <a name="create-a-project-from-a-template"></a><span data-ttu-id="67e40-119">Создание проекта из шаблона</span><span class="sxs-lookup"><span data-stu-id="67e40-119">Create a project from a template</span></span>  
 <span data-ttu-id="67e40-120">Можно создать проект из шаблона следующими способами.</span><span class="sxs-lookup"><span data-stu-id="67e40-120">You can create a project from a template in these following ways:</span></span>  
  
-   <span data-ttu-id="67e40-121">При создании проекта из предложения с расценками можно выбрать шаблон проекта в форме быстрого создания проекта.</span><span class="sxs-lookup"><span data-stu-id="67e40-121">When creating a project from the quote, you can choose a project template in the project quick create form.</span></span>  
  
-   <span data-ttu-id="67e40-122">При создании проекта с помощью кнопки **Создать проект** перед сохранением записи отображается форма проекта.</span><span class="sxs-lookup"><span data-stu-id="67e40-122">When creating a project by clicking **New Project**, the project form displays before you save the record.</span></span> <span data-ttu-id="67e40-123">Здесь можно щелкнуть поле **Выбрать шаблон**, чтобы выбрать из списка готовых шаблонов проекта в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="67e40-123">From here, you can click **Pick a template** field to choose from the list of pre-defined project templates in your organization.</span></span>  
  
-   <span data-ttu-id="67e40-124">Щелкните **Создать проект из шаблона** на странице **Шаблон проекта**, чтобы создать проект из шаблона.</span><span class="sxs-lookup"><span data-stu-id="67e40-124">Click **Create project from a template** on the **Project Template** page to create a project from the template.</span></span>  
  
## <a name="copying-components-of-a-template-to-a-project"></a><span data-ttu-id="67e40-125">Копирование компонентов шаблона в проект</span><span class="sxs-lookup"><span data-stu-id="67e40-125">Copying components of a template to a project</span></span>  
 <span data-ttu-id="67e40-126">При копировании компонентов шаблона в проект следует помнить некоторые моменты.</span><span class="sxs-lookup"><span data-stu-id="67e40-126">When you copy components of a template into a project, there are a few things you should know about.</span></span>  
  
 <span data-ttu-id="67e40-127">**Копирование структурной декомпозиции работ**: при копировании структурной декомпозиции работ из шаблона проекта рабочие часы из календаря проекта будут применены к расписанию задач, если календарь проекта отличается от календаря шаблона.</span><span class="sxs-lookup"><span data-stu-id="67e40-127">**Copying a work breakdown structure**: When you copy the work breakdown structure from a project template, if the project has a different project calendar than the template, the work hours from the project’s calendar will be applied to the schedule of tasks.</span></span> <span data-ttu-id="67e40-128">Это корректирует расписание в соответствии с резервным календарем проекта.</span><span class="sxs-lookup"><span data-stu-id="67e40-128">This adjusts the schedule to the backing project calendar.</span></span> <span data-ttu-id="67e40-129">Аналогично первая задача в структурной декомпозиции работ принимает дату начала проекта, так что остальное расписание иерархии задач обновляется с учетом продолжительности и зависимостей, определенных в структурной декомпозиции работ шаблона.</span><span class="sxs-lookup"><span data-stu-id="67e40-129">Similarly, the first task on the work breakdown structure takes the project’s start date, so the rest of the task hierarchy schedule is updated based on the duration and dependencies specified in the template’s work breakdown structure.</span></span>  
  
 <span data-ttu-id="67e40-130">**Копирование оценок проекта**: при копировании строк оценки проекта прейскуранты обновляются с учетом ответственного подразделения проекта для прейскуранта затрат и клиента для прейскуранта цен продажи.</span><span class="sxs-lookup"><span data-stu-id="67e40-130">**Copying project estimates**: When you copy across project estimate lines, price lists are updated based on the owning unit of the project for the cost price list and customer for the sales price list.</span></span> <span data-ttu-id="67e40-131">Стоимость единицы и цены продажи определяются на основе этих прейскурантов в проектах, которые связаны с сущностью продаж.</span><span class="sxs-lookup"><span data-stu-id="67e40-131">The unit cost and sales prices are determined from these price lists on projects that are associated to a sales entity.</span></span>  
  
 <span data-ttu-id="67e40-132">**Копирование рабочей группы проекта**: при копировании рабочей группы проекта из шаблона в проект универсальные ресурсы копируются вместе с навыками и компетенциями, определенными в шаблоне.</span><span class="sxs-lookup"><span data-stu-id="67e40-132">**Copying a project team**: When you copy the project team from the template to a project, the generic resources are copied across, along with the skills and proficiencies defined in the template.</span></span> <span data-ttu-id="67e40-133">Универсальные назначения ресурсов также обслуживаются как в шаблоне проекта.</span><span class="sxs-lookup"><span data-stu-id="67e40-133">Generic resource assignments are also maintained as in the project template.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="67e40-134">См. также</span><span class="sxs-lookup"><span data-stu-id="67e40-134">See Also</span></span>  
 [<span data-ttu-id="67e40-135">Руководство менеджера по проектам</span><span class="sxs-lookup"><span data-stu-id="67e40-135">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
