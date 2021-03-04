---
title: Планирование проекта со структурной декомпозицией работ
description: Порядок планирования проекта со структурной декомпозицией работ в Project Service
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
ms.openlocfilehash: cf12cc3bcf061e1daffafb248cfd76809c6444ec
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149829"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a><span data-ttu-id="4cd4a-103">Планирование проекта со структурной декомпозицией работ (Project Service)</span><span class="sxs-lookup"><span data-stu-id="4cd4a-103">Schedule a project with a work breakdown structure (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="4cd4a-104">Расписание проекта определяет, какую работу необходимо выполнить, какие ресурсы будут выполнять работу и период времени, за который необходимо выполнить работу.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-104">A project schedule communicates what work needs to be performed, which resources will perform the work, and the timeframe in which that work needs to be completed.</span></span> <span data-ttu-id="4cd4a-105">Расписание проекта отражает все работы, связанные с выполнением проекта в срок.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-105">The project schedule reflects all the work associated with delivering the project on time.</span></span> <span data-ttu-id="4cd4a-106">Одним из первых шагов в стадии начала проекта — составление расписания проекта.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-106">One of the first steps in the initiation phase of the project is to come up with a project schedule.</span></span> <span data-ttu-id="4cd4a-107">Чтобы составить расписание проекта необходимо создать структурную декомпозицию работ.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-107">To establish a project schedule, you need to create a work breakdown structure.</span></span>  
  
 <span data-ttu-id="4cd4a-108">Создание структуры проекта со структурной декомпозицией работ, которая поможет сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="4cd4a-108">Create a project structure with a work breakdown structure, which helps you:</span></span>  
  
- <span data-ttu-id="4cd4a-109">Разбить работу на управляемые задачи</span><span class="sxs-lookup"><span data-stu-id="4cd4a-109">Break down work into manageable tasks</span></span>  
  
- <span data-ttu-id="4cd4a-110">Оценить время, требуемое для выполнения задачи</span><span class="sxs-lookup"><span data-stu-id="4cd4a-110">Estimate the time required to complete a task</span></span>  
  
- <span data-ttu-id="4cd4a-111">Задавать зависимости задач и длительность задач</span><span class="sxs-lookup"><span data-stu-id="4cd4a-111">Set task dependencies and task duration</span></span>  
  
- <span data-ttu-id="4cd4a-112">Определять роли, необходимые для выполнения каждой задачи</span><span class="sxs-lookup"><span data-stu-id="4cd4a-112">Determine the roles required to complete each task</span></span>  
  
  <span data-ttu-id="4cd4a-113">Расписание проекта в структурной декомпозиции работ похож на интерактивную диаграмму Ганта.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-113">The project schedule in the work breakdown structure has a familiar look and feel, complete with an interactive Gantt chart.</span></span>  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a><span data-ttu-id="4cd4a-114">Создание структурной декомпозиции работ для проекта</span><span class="sxs-lookup"><span data-stu-id="4cd4a-114">Create a work breakdown structure for a project</span></span>  
 <span data-ttu-id="4cd4a-115">Создание структурной декомпозиции работ для представления последовательности задач в проекте.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-115">Create a work breakdown structure to represent the sequence of tasks in a project.</span></span> <span data-ttu-id="4cd4a-116">Структурная декомпозиция работ включает задачи, требования для каждой задачи и сведения о выручке и расходах.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-116">The work breakdown structure includes tasks, requirements for each task, and revenue and cost information.</span></span> <span data-ttu-id="4cd4a-117">В структурной декомпозиции работ можно добавить:</span><span class="sxs-lookup"><span data-stu-id="4cd4a-117">In your work breakdown structure, you can add:</span></span>  
  
-   <span data-ttu-id="4cd4a-118">Последовательность задач в иерархии</span><span class="sxs-lookup"><span data-stu-id="4cd4a-118">The sequence of tasks in a hierarchy</span></span>  
  
-   <span data-ttu-id="4cd4a-119">Другие задачи (если есть), которые необходимо выполнить перед началом задачи</span><span class="sxs-lookup"><span data-stu-id="4cd4a-119">Other tasks, if any, that must be completed before a task can be started</span></span>  
  
-   <span data-ttu-id="4cd4a-120">Дата начала, дате окончания и длительности задачи</span><span class="sxs-lookup"><span data-stu-id="4cd4a-120">The starting date, ending date, and duration of a task</span></span>  
  
-   <span data-ttu-id="4cd4a-121">Количество часов, требуемых для задачи</span><span class="sxs-lookup"><span data-stu-id="4cd4a-121">The number of hours required for a task</span></span>  
  
-   <span data-ttu-id="4cd4a-122">Требуемые навыки работников и образование</span><span class="sxs-lookup"><span data-stu-id="4cd4a-122">Any required worker skills and education</span></span>  
  
-   <span data-ttu-id="4cd4a-123">Рабочие, назначенные для задачи</span><span class="sxs-lookup"><span data-stu-id="4cd4a-123">The workers who are assigned to a task</span></span>  
  
-   <span data-ttu-id="4cd4a-124">Предполагаемые выручка и расходы</span><span class="sxs-lookup"><span data-stu-id="4cd4a-124">Estimated revenue and costs</span></span>  
  
## <a name="task-types"></a><span data-ttu-id="4cd4a-125">Типы задач</span><span class="sxs-lookup"><span data-stu-id="4cd4a-125">Task types</span></span>  
<span data-ttu-id="4cd4a-126">Будут использоваться следующие типы задач при создании своей структурной декомпозиции работ:</span><span class="sxs-lookup"><span data-stu-id="4cd4a-126">You’ll use the following types of tasks when creating your work breakdown structure:</span></span>  

| | | 
|---------------------------------------|-----------------------------------------------------------------| 
| <span data-ttu-id="4cd4a-127">**Корневой узел проекта**</span><span class="sxs-lookup"><span data-stu-id="4cd4a-127">**Project root node**</span></span> | <span data-ttu-id="4cd4a-128">Сводная задача верхнего уровня для проекта.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-128">The top-level summary task for the project.</span></span> <span data-ttu-id="4cd4a-129">Все другие задачи проекта создаются под ней.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-129">All other project tasks are created under it.</span></span> <span data-ttu-id="4cd4a-130">Название корневой задачи — имя проекта.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-130">The name of the root task is the project name.</span></span> <span data-ttu-id="4cd4a-131">Усилия, даты и длительность корневого узла основаны на значениях в иерархии под ним.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-131">The effort, dates, and duration of the root node are based on the values on the hierarchy below it.</span></span> <span data-ttu-id="4cd4a-132">Нельзя изменять свойства корневого узла или удалять корневой узел.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-132">You can’t edit root node properties or delete the root node.</span></span> | 
| <span data-ttu-id="4cd4a-133">**Сводные задачи или задачи контейнера**</span><span class="sxs-lookup"><span data-stu-id="4cd4a-133">**Summary or container tasks**</span></span> | <span data-ttu-id="4cd4a-134">Сводная задача — это задача, в которой есть подзадачи.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-134">A summary task is a task that has sub-tasks under it.</span></span> <span data-ttu-id="4cd4a-135">В сводной задачи нет своих усилий работы или стоимости.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-135">A summary task doesn’t have any work effort or cost of its own.</span></span> <span data-ttu-id="4cd4a-136">Ее усилия по работе и стоимость являются сверткой подзадач.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-136">Its work effort and cost are a rollup of its sub-tasks.</span></span> <span data-ttu-id="4cd4a-137">Можно изменить имя сводной задачи, но нельзя изменить усилия, даты и длительность, поскольку они автоматически рассчитываются.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-137">You can change the name of a summary task, but you can’t change the effort, dates, or duration, because those are automatically calculated.</span></span> <span data-ttu-id="4cd4a-138">При удалении сводной задачи удаляется задача и все ее подзадачи.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-138">Deleting a summary task deletes the task and all of its sub-tasks.</span></span>|  
| <span data-ttu-id="4cd4a-139">**Задачи листового узла**</span><span class="sxs-lookup"><span data-stu-id="4cd4a-139">**Leaf node tasks**</span></span> | <span data-ttu-id="4cd4a-140">Задача листового узла представляет наиболее подробную работу над проектом.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-140">A leaf node task represents the most detailed work on the project.</span></span> <span data-ttu-id="4cd4a-141">В ней содержится расчетное усилие, плановое количество ресурсов, запланированные даты начала и окончания и продолжительность.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-141">It has an estimated effort, a planned number of resources, planned start and end dates, and a duration.</span></span>|

  
## <a name="task-hierarchy"></a><span data-ttu-id="4cd4a-142">Иерархия задач</span><span class="sxs-lookup"><span data-stu-id="4cd4a-142">Task hierarchy</span></span>  
 <span data-ttu-id="4cd4a-143">Имеются следующие параметры при создании иерархии задач:</span><span class="sxs-lookup"><span data-stu-id="4cd4a-143">You have the following options when creating a task hierarchy:</span></span>  
  
- <span data-ttu-id="4cd4a-144">**Добавить задачу**.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-144">**Add task**.</span></span>   <span data-ttu-id="4cd4a-145">Можно добавить задачу в расположении, выбранном в иерархии задач.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-145">You can add a task at a position you choose in the task hierarchy.</span></span> <span data-ttu-id="4cd4a-146">Если не выбрать расположение, новая задача появляется в конце.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-146">If you don’t select a position, your new task appears at the end.</span></span>  
  
- <span data-ttu-id="4cd4a-147">**Понизить уровень задачи**.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-147">**Indent task**.</span></span>   <span data-ttu-id="4cd4a-148">Понизьте уровень задачи, чтобы сделать ее дочерней относительно задачи непосредственно над ней.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-148">Indent a task to make it a child of the task directly above it.</span></span>  
  
- <span data-ttu-id="4cd4a-149">**Повысить уровень задачи**</span><span class="sxs-lookup"><span data-stu-id="4cd4a-149">**Outdent task**.</span></span>   <span data-ttu-id="4cd4a-150">Повысьте уровень задачи, чтобы она больше не была дочерней относительно исходной родительской задачи.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-150">Outdent a task to make it so it’s no longer a sub-task of its original parent task.</span></span>  
  
- <span data-ttu-id="4cd4a-151">**Переместить вверх и вниз**.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-151">**Move up and Move down**.</span></span>   <span data-ttu-id="4cd4a-152">Перемещайте задачи вверх и вниз по иерархии родительской задачи.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-152">Move tasks up and down in the hierarchy of its parent task.</span></span> <span data-ttu-id="4cd4a-153">Перемещение задачи вверх или вниз не влияет на ее усилие, стоимость, даты и длительность.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-153">Moving a task up or down has no effect on its effort, cost, dates, or duration.</span></span>  
  
## <a name="task-attributes"></a><span data-ttu-id="4cd4a-154">Атрибуты задачи</span><span class="sxs-lookup"><span data-stu-id="4cd4a-154">Task attributes</span></span>  
 <span data-ttu-id="4cd4a-155">Название задачи описывает работу, которая должны быть выполнена.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-155">A task’s name describes the work that needs to be completed.</span></span> <span data-ttu-id="4cd4a-156">Следует использовать разные атрибуты задач для описания расписания и требований к персоналу для задачи.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-156">You use various task attributes to describe the schedule and staffing requirements for the task.</span></span>  
  
### <a name="schedule-attributes"></a><span data-ttu-id="4cd4a-157">Атрибуты расписания</span><span class="sxs-lookup"><span data-stu-id="4cd4a-157">Schedule attributes</span></span>

 - <span data-ttu-id="4cd4a-158">Назначение значений **Рабочие часы**, **Количество ресурсов**, **Дата начала**, **Дата окончания** и **Длительность** для определения расписания для задачи.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-158">Assign values to **Effort hours**, **Number of resources**, **Start date**, **End date**, and **Duration** to determine the schedule for the task.</span></span> 
 - <span data-ttu-id="4cd4a-159">**Усилия** — это оценка часов, которые потребуются для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-159">**Effort** is an estimate of the hours it takes to complete the task.</span></span>
 - <span data-ttu-id="4cd4a-160">**Количество ресурсов** — оценка, которую менеджер проекта помещает в задачу для составления наилучшего расписания.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-160">**Number of resources** is an estimate that the project manager puts in the task to help come up with the best possible schedule.</span></span> 
 - <span data-ttu-id="4cd4a-161">**Длительность** (в днях) указывает число рабочих дней, которые потребуются для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-161">**Duration** (in days) indicates the number of work days it will take to complete the task.</span></span>  
  
### <a name="staffing-attributes"></a><span data-ttu-id="4cd4a-162">Атрибуты персонала</span><span class="sxs-lookup"><span data-stu-id="4cd4a-162">Staffing attributes</span></span>

 - <span data-ttu-id="4cd4a-163">**Роль**, **Подразделение ресурса**, **Количество ресурсов** и **Ресурсы** описывают требования к персоналу для задачи.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-163">**Role**, **Resource organizational unit**, **Number of resources**, and **Resources** describe the staffing requirements for the task.</span></span> 
 - <span data-ttu-id="4cd4a-164">**Роль** описывает тип ресурса, необходимого для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-164">**Role** describes the type of resource needed to perform the task.</span></span> 
 - <span data-ttu-id="4cd4a-165">**Подразделение ресурса** указывает подразделение, из которого ресурсы должны быть укомплектованы персоналом для этой задачи; это также влияет на оценку стоимости и продаж по задаче, так как это учитывается при определении цены продажи единицы для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-165">**Resource organizational unit** indicates the organizational unit from which resources should be staffed for that task; this also impacts the cost and sales estimate of the task, since this is accounted for when determining the unit sales price for the resource.</span></span> 
 - <span data-ttu-id="4cd4a-166">**Ресурсы** содержит общий ресурс или именованный ресурс при нахождении ресурса.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-166">**Resources** holds a generic resource or a named resource when one is found.</span></span>  
  
## <a name="task-dependencies"></a><span data-ttu-id="4cd4a-167">Зависимости задач</span><span class="sxs-lookup"><span data-stu-id="4cd4a-167">Task dependencies</span></span>  
 <span data-ttu-id="4cd4a-168">Можно создавать отношения предшественников между одной или несколькими задачами в структурной декомпозиции работ.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-168">You can create predecessor relationships between one or more tasks in the work breakdown structure.</span></span> <span data-ttu-id="4cd4a-169">Может потребоваться задать одно или несколько значений для поля предшественника по задаче, чтобы указать задачи, от которых он будет зависеть.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-169">You can set one or more values for the predecessor field on tasks to indicate the tasks that it will be dependent on.</span></span> <span data-ttu-id="4cd4a-170">При назначении значения предшественника для задачи задача может начаться, только когда все задачи предшественника будут завершены.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-170">When you assign a predecessor value to a task, the task can only start when all the predecessor tasks have completed.</span></span> <span data-ttu-id="4cd4a-171">Установка этой зависимости по задаче приведет к пересчету запланированной даты начала задачи как последнего окончания всех предшественников.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-171">Setting this dependency on a task will result in the recalculation of the planned start date of the task as the latest end of all of its predecessors.</span></span> <span data-ttu-id="4cd4a-172">Влияния на расписание, связанные с предшественниками, не ограничиваются режимом задачи, указанным для задачи.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-172">Predecessor-related impacts on a schedule are not limited by the task mode defined on the task.</span></span>  
  
## <a name="task-mode"></a><span data-ttu-id="4cd4a-173">Режим задачи</span><span class="sxs-lookup"><span data-stu-id="4cd4a-173">Task mode</span></span>  
 <span data-ttu-id="4cd4a-174">Режим задачи — один из важных факторов, определяющие планирование задач листового узла.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-174">Task mode is one of the important factors that determine scheduling leaf node tasks.</span></span> <span data-ttu-id="4cd4a-175">Есть два режима задач по каждой задачи: режим автоматического планирования и режим ручного планирования.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-175">There are two task modes for every task: auto scheduling mode and manual scheduling mode.</span></span>  
  
-   <span data-ttu-id="4cd4a-176">**Автоматические создание расписания**.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-176">**Auto scheduling**.</span></span>   <span data-ttu-id="4cd4a-177">Когда вы задаете режим задачи "автоматическое планирование", модуль планирования задачи использует правила планирования для следующих атрибутов задачи для определения расписания для задачи:</span><span class="sxs-lookup"><span data-stu-id="4cd4a-177">When you set the task mode to Automatically Scheduled, the task scheduling engine uses the scheduling rules on the following task attributes to determine the schedule for the task:</span></span>  
  
    -   <span data-ttu-id="4cd4a-178">Предшественники</span><span class="sxs-lookup"><span data-stu-id="4cd4a-178">Predecessors</span></span>  
  
    -   <span data-ttu-id="4cd4a-179">Усилия</span><span class="sxs-lookup"><span data-stu-id="4cd4a-179">Effort</span></span>  
  
    -   <span data-ttu-id="4cd4a-180">Количество ресурсов</span><span class="sxs-lookup"><span data-stu-id="4cd4a-180">Number of resources</span></span>  
  
    -   <span data-ttu-id="4cd4a-181">даты начала и окончания;</span><span class="sxs-lookup"><span data-stu-id="4cd4a-181">Start and end dates</span></span>  
  
-   <span data-ttu-id="4cd4a-182">**Правила планирования**.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-182">**Scheduling rules**.</span></span>   <span data-ttu-id="4cd4a-183">Дата начала задачи листового узла не имеет предшественников по умолчанию относительно даты начала планирования проекта.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-183">The start date of a leaf node task that does not have predecessors defaults to the project’s scheduling start date.</span></span> <span data-ttu-id="4cd4a-184">Длительность задачи листового узла всегда рассчитывается как число рабочих дней между датами начала и окончания.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-184">The duration of a leaf node task is always calculated as the number of working days between its start and end dates.</span></span> <span data-ttu-id="4cd4a-185">Если задача планируется автоматически, модуль планирования соответствует правилам ниже:</span><span class="sxs-lookup"><span data-stu-id="4cd4a-185">When a task is automatically scheduled, the scheduling engine follows the rules below:</span></span>  
  
    -   <span data-ttu-id="4cd4a-186">Даты начала и окончания задачи всегда должны быть рабочими днями относительно календаря планирования проекта</span><span class="sxs-lookup"><span data-stu-id="4cd4a-186">Start and end dates of a task must always be working days according to the project’s scheduling calendar</span></span>  
  
    -   <span data-ttu-id="4cd4a-187">Дата начала задачи, у которой есть предшественник, по умолчанию является последней датой окончания ее предшественников</span><span class="sxs-lookup"><span data-stu-id="4cd4a-187">The start date of a task that has predecessors defaults to the latest end date of its predecessors</span></span>  
  
    -   <span data-ttu-id="4cd4a-188">Усилия = число людей \* длительность \* часы в стандартном рабочем дне календаря проекта</span><span class="sxs-lookup"><span data-stu-id="4cd4a-188">Effort = Number of people \* Duration \* hours in a standard work day of the project calendar</span></span>  
  
-   <span data-ttu-id="4cd4a-189">**Ручное планирование**.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-189">**Manual scheduling**.</span></span>   <span data-ttu-id="4cd4a-190">В некоторых случаях может потребоваться отклониться от этих правил.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-190">In some cases, you might want to deviate from these rules.</span></span> <span data-ttu-id="4cd4a-191">В этих случаях можно задать режим ручного планирования задачи.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-191">In these cases, you can set the task mode for the task to be manually scheduled.</span></span> <span data-ttu-id="4cd4a-192">При этом модуль планирования не рассчитывает значения для других атрибутов планирования.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-192">This stops the scheduling engine from calculating the values for other scheduling attributes.</span></span> <span data-ttu-id="4cd4a-193">Установка предшественников по задачам всегда влияет на дату начала зависимой задачи.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-193">Setting predecessors on tasks always impacts the dependent task’s start date.</span></span>  
  
## <a name="create-a-work-breakdown-structure"></a><span data-ttu-id="4cd4a-194">Создание структурной декомпозиции работ</span><span class="sxs-lookup"><span data-stu-id="4cd4a-194">Create a work breakdown structure</span></span>  
  
1.  <span data-ttu-id="4cd4a-195">Перейдите к разделу **Project Service > Проекты**.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-195">Go to **Project Service > Projects**.</span></span>  
  
2.  <span data-ttu-id="4cd4a-196">Щелкните проект, над которым вы хотите работать.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-196">Click the project you want to work on.</span></span>  
  
3.  <span data-ttu-id="4cd4a-197">В строке в верхней части экрана щелкните стрелку вниз рядом с именем проекта и щелкните "Структурная декомпозиция работ".</span><span class="sxs-lookup"><span data-stu-id="4cd4a-197">In the bar across the top of the screen, select the down arrow next to the project name, and then click Work breakdown structure.</span></span>  
  
4.  <span data-ttu-id="4cd4a-198">Для добавления задачи щелкните **Добавить задачу**.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-198">To add a task, click **Add Task**.</span></span> <span data-ttu-id="4cd4a-199">Заполните поля для задачи, затем щелкните **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-199">Fill in the fields for the task, and then click **Save**.</span></span>  
  
5.  <span data-ttu-id="4cd4a-200">Продолжите добавлять задачи до завершения структурной декомпозиции работ.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-200">Continue adding tasks until your work breakdown structure is complete.</span></span> <span data-ttu-id="4cd4a-201">При создании своей структурной декомпозиции работ можно выполнить следующие действия для упорядочивания своих задач:</span><span class="sxs-lookup"><span data-stu-id="4cd4a-201">While creating your work breakdown structure, you can do the following to organize your tasks:</span></span>  
  
    -   <span data-ttu-id="4cd4a-202">Выберите задачу и щелкните **Понизить уровень**, чтобы переместить ее под другую задачу или щелкните "Повысить уровень" для повышения.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-202">Select a task and click **Indent** to move it under another task or click Outdent to move it out a level.</span></span>  
  
    -   <span data-ttu-id="4cd4a-203">Выберите задачу и щелкните **Вверх** или **Вниз**, чтобы переместить ее вверх или вниз в списке.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-203">Select a task and click **Move Up** or **Move Down** to move it up or down in the list.</span></span>  
  
    -   <span data-ttu-id="4cd4a-204">Щелкните **Скрыть Ганта**, чтобы скрыть диаграмму Ганта, и щелкните **Показать Ганта**, чтобы показать ее.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-204">Click **Hide Gantt** to hide the Gantt chart, and click **Show Gantt** to display it again.</span></span>  
  
    -   <span data-ttu-id="4cd4a-205">Выберите другой период времени диаграммы Ганта в области **Шкала времени**.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-205">Select a different period of time for the Gantt chart in **Time Scale**.</span></span>  
  
6.  <span data-ttu-id="4cd4a-206">Для добавления ролей, указанных в структурной декомпозиции работ, для участников рабочей группы своего проекта щелкните **Создать рабочую группу проекта**.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-206">To add the roles you specified in your work breakdown structure to your project’s team members, click **Generate Project Team**.</span></span>  
  
7.  <span data-ttu-id="4cd4a-207">По окончании внесения изменений щелкните **Сохранить** в правом нижнем углу экрана.</span><span class="sxs-lookup"><span data-stu-id="4cd4a-207">Click **Save** at the bottom right corner of the screen when you’re done making changes.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="4cd4a-208">См. также</span><span class="sxs-lookup"><span data-stu-id="4cd4a-208">See Also</span></span>  
 [<span data-ttu-id="4cd4a-209">Руководство менеджера по проектам</span><span class="sxs-lookup"><span data-stu-id="4cd4a-209">Project manager guide</span></span>](../psa/project-manager-guide.md)
