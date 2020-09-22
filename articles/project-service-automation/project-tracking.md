---
title: Ход выполнение проекта и освоения затрат
description: В этом разделе представлена информация о том, как отслеживать ход выполнения проекта и потребление затрат.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 0d742164-5469-421d-8917-63160a81f651
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8aa5814938129f30885d8161a7c86197ab013364
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755014"
---
# <a name="project-progress-and-cost-consumption"></a><span data-ttu-id="69f64-103">Ход выполнение проекта и освоения затрат</span><span class="sxs-lookup"><span data-stu-id="69f64-103">Project progress and cost consumption</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="69f64-104">Необходимость отслеживать ход выполнения относительно расписания меняется по отраслям.</span><span class="sxs-lookup"><span data-stu-id="69f64-104">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="69f64-105">В некоторых отраслях отслеживание требуется на детальном уровне, а в других отраслях отслеживание выполняется на высоком уровне.</span><span class="sxs-lookup"><span data-stu-id="69f64-105">Some industries track at a granular level, whereas other industries track at a higher level.</span></span> <span data-ttu-id="69f64-106">В этом разделе показано, как планировать, чтобы удовлетворить требованиям организации.</span><span class="sxs-lookup"><span data-stu-id="69f64-106">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="69f64-107">Представление отслеживания усилий</span><span class="sxs-lookup"><span data-stu-id="69f64-107">Effort tracking view</span></span>

<span data-ttu-id="69f64-108">Представление **Отслеживание усилий** отслеживает ход выполнения задач в расписании.</span><span class="sxs-lookup"><span data-stu-id="69f64-108">The **Effort tracking** view tracks the progress of tasks in the schedule.</span></span> <span data-ttu-id="69f64-109">Оно сравнивает фактические затраты времени, которое было потрачено на задачу, с запланированными затратами времени на эту задачу.</span><span class="sxs-lookup"><span data-stu-id="69f64-109">It compares the actual effort hours that have been spent on a task to the planned effort hours for that task.</span></span> <span data-ttu-id="69f64-110">PSA использует следующие формулы для вычисления показателей отслеживания:</span><span class="sxs-lookup"><span data-stu-id="69f64-110">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="69f64-111">Процент хода выполнения = Фактические усилия, затраченные по настоящее время ÷ Запланированные усилия для задачи</span><span class="sxs-lookup"><span data-stu-id="69f64-111">Progress percentage = Actual effort spent to date ÷ Planned effort for the task</span></span> 
- <span data-ttu-id="69f64-112">Оценка до завершения (ETC) = Запланированные усилия — Фактические усилия, затраченные по настоящее время</span><span class="sxs-lookup"><span data-stu-id="69f64-112">Estimate to complete (ETC) = Planned effort – Actual effort spent to date</span></span> 
- <span data-ttu-id="69f64-113">Оценка при завершении (EAC) = Оставшиеся усилия + Фактические усилия, затраченные по настоящее время</span><span class="sxs-lookup"><span data-stu-id="69f64-113">Estimate at complete (EAC) = Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="69f64-114">Отклонение от ожидаемых усилий = Запланированные усилия — EAC</span><span class="sxs-lookup"><span data-stu-id="69f64-114">Projected effort variance = Planned effort – EAC</span></span>

<span data-ttu-id="69f64-115">PSA отображает ожидаемое отклонения усилий для задачи.</span><span class="sxs-lookup"><span data-stu-id="69f64-115">PSA shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="69f64-116">Если EAC превышает запланированные усилия, прогнозируется, что на выполнение задачи потребуется больше времени, чем запланировано первоначально.</span><span class="sxs-lookup"><span data-stu-id="69f64-116">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned.</span></span> <span data-ttu-id="69f64-117">Следовательно, она отстает от графика.</span><span class="sxs-lookup"><span data-stu-id="69f64-117">Therefore, it's behind schedule.</span></span> <span data-ttu-id="69f64-118">Если EAC меньше запланированных усилий, прогнозируется, что на выполнение задачи потребуется меньше времени, чем запланировано первоначально.</span><span class="sxs-lookup"><span data-stu-id="69f64-118">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned.</span></span> <span data-ttu-id="69f64-119">Следовательно, она опережает график.</span><span class="sxs-lookup"><span data-stu-id="69f64-119">Therefore, it's ahead of schedule.</span></span>

## <a name="re-projecting-effort"></a><span data-ttu-id="69f64-120">Повторное прогнозирование усилий</span><span class="sxs-lookup"><span data-stu-id="69f64-120">Re-projecting effort</span></span>

<span data-ttu-id="69f64-121">Руководители проекта часто пересматривают первоначальные оценки для задачи.</span><span class="sxs-lookup"><span data-stu-id="69f64-121">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="69f64-122">Повторное прогнозирование проекта является восприятием оценок руководителем проекта в соответствии с текущим состоянием проекта.</span><span class="sxs-lookup"><span data-stu-id="69f64-122">Project re-projections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="69f64-123">Однако не рекомендуется, чтобы руководители проектов изменяли значения в базовом плане проекта, поскольку базовый план проекта представляет определенный источник истинных значений для оценки графика выполнения и затрат проекта, согласованный со всеми заинтересованными лицами проекта.</span><span class="sxs-lookup"><span data-stu-id="69f64-123">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="69f64-124">Существует два способа, которыми руководитель проекта может изменить прогноз усилий по задачам:</span><span class="sxs-lookup"><span data-stu-id="69f64-124">There are two ways that a project manager can re-project effort on tasks:</span></span>

- <span data-ttu-id="69f64-125">Переопределить ETC по умолчанию с новой оценкой фактических оставшихся усилий для задачи.</span><span class="sxs-lookup"><span data-stu-id="69f64-125">Override the default ETC with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="69f64-126">Переопределить процент хода выполнения по умолчанию с новой оценкой истинного хода выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="69f64-126">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="69f64-127">Каждый из этих способов приводит к повторному вычислению ETC, ПОПЗ и процента выполнения задачи, а также прогнозируемого отклонения усилий для задачи.</span><span class="sxs-lookup"><span data-stu-id="69f64-127">Each of these approaches cause a recalculation of the task's ETC, EAC, and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="69f64-128">ПОПЗ, ETC и процент выполнения сводных задач также пересчитывается, и дает новый прогноз отклонения усилий.</span><span class="sxs-lookup"><span data-stu-id="69f64-128">The EAC, ETC, and progress percentage on the summary tasks are also recalculated, and produce a new projection of effort variance.</span></span>

## <a name="re-projection-of-effort-on-summary-tasks"></a><span data-ttu-id="69f64-129">Повторное прогнозирование усилий для сводных задач</span><span class="sxs-lookup"><span data-stu-id="69f64-129">Re-projection of effort on summary tasks</span></span>

<span data-ttu-id="69f64-130">Усилия по сводным задачам или задачам-контейнерам можно снова спрогнозировать.</span><span class="sxs-lookup"><span data-stu-id="69f64-130">Effort on summary tasks or container tasks can be re-projected.</span></span> <span data-ttu-id="69f64-131">Независимо от того, выполняет ли пользователь повторное прогнозирование с использованием оставшихся усилий или процента выполнения сводных задачах, начинается следующий набор расчетов:</span><span class="sxs-lookup"><span data-stu-id="69f64-131">Regardless of whether the user re-projects by using the remaining effort or the progress percentage on the summary tasks, the following set of calculations begins:</span></span>

- <span data-ttu-id="69f64-132">Рассчитываются ПОПЗ, ETC и процент выполнения для задачи.</span><span class="sxs-lookup"><span data-stu-id="69f64-132">The EAC, ETC, and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="69f64-133">Новое значение ПОПЗ распространяется вниз в дочерние задачи в той же пропорции, что и первоначальное значение ПОПЗ для задачи.</span><span class="sxs-lookup"><span data-stu-id="69f64-133">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="69f64-134">Рассчитывается новое значение ПОПЗ по каждой отдельной задаче вплоть доя задач листового узла.</span><span class="sxs-lookup"><span data-stu-id="69f64-134">The new EAC on each of the individualt tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="69f64-135">Для затронутых дочерних задач вниз до листовых узлов пересчитываются значения ETC и процент выполнения на основе значения ПОПЗ.</span><span class="sxs-lookup"><span data-stu-id="69f64-135">The affected child tasks down to the leaf nodes have their ETC and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="69f64-136">Это приводит к новому прогнозу для отклонения усилий задачи.</span><span class="sxs-lookup"><span data-stu-id="69f64-136">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="69f64-137">Значения ПОПЗ сводных задач пересчитываются вплоть до корневого узла.</span><span class="sxs-lookup"><span data-stu-id="69f64-137">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>

### <a name="cost-tracking-view"></a><span data-ttu-id="69f64-138">Представление отслеживания стоимости</span><span class="sxs-lookup"><span data-stu-id="69f64-138">Cost tracking view</span></span> 

<span data-ttu-id="69f64-139">Представление **Отслеживание стоимости** сравнивает фактическую стоимость, которая была потрачена по задаче, с запланированной стоимостью для задачи.</span><span class="sxs-lookup"><span data-stu-id="69f64-139">The **Cost tracking** view compares the actual cost that was spent on a task to the planned cost on a task.</span></span> 

> [!NOTE]
> <span data-ttu-id="69f64-140">В этом представлении отображаются только затраты на работу, не включая затраты из оценок расходов.</span><span class="sxs-lookup"><span data-stu-id="69f64-140">This view shows only labor costs and doesn’t include costs from the expense estimates.</span></span> 

<span data-ttu-id="69f64-141">PSA использует следующие формулы для вычисления показателей отслеживания:</span><span class="sxs-lookup"><span data-stu-id="69f64-141">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="69f64-142">Потребленный процент стоимости = Фактическая стоимости, затраченная на сегодняшний день ÷ Запланированная стоимость для задачи</span><span class="sxs-lookup"><span data-stu-id="69f64-142">Percentage of cost consumed = Actual cost spent to date ÷ Planned cost for the task</span></span>
- <span data-ttu-id="69f64-143">Стоимость до завершения (CTC) = Запланированная стоимость — Фактическая стоимость, затраченная по настоящее время</span><span class="sxs-lookup"><span data-stu-id="69f64-143">Cost to complete (CTC) = Planned cost – Actual cost spent to date</span></span>
- <span data-ttu-id="69f64-144">ПОПЗ = CTC + Фактическая стоимость, потраченная по настоящее время</span><span class="sxs-lookup"><span data-stu-id="69f64-144">EAC = CTC + Actual cost spent to date</span></span>
- <span data-ttu-id="69f64-145">Ожидаемое отклонение стоимости = Запланированная стоимость — ПОПЗ</span><span class="sxs-lookup"><span data-stu-id="69f64-145">Projected cost variance = Planned cost – EAC</span></span>

<span data-ttu-id="69f64-146">Прогноз отклонения стоимости отображается для задачи.</span><span class="sxs-lookup"><span data-stu-id="69f64-146">A projection of the cost variance is shown on the task.</span></span> <span data-ttu-id="69f64-147">Если EAC превышает запланированную стоимость, прогнозируется, что на задачу потребуется большая стоимость, чем запланировано первоначально.</span><span class="sxs-lookup"><span data-stu-id="69f64-147">If the EAC is more than the planned cost, the task is projected to cost more than was originally planned.</span></span> <span data-ttu-id="69f64-148">Следовательно, имеется тенденция превышения бюджета.</span><span class="sxs-lookup"><span data-stu-id="69f64-148">Therefore, it's trending over budget.</span></span> <span data-ttu-id="69f64-149">Если EAC меньше запланированной стоимости, прогнозируется, что на задачу потребуется меньшая стоимость, чем запланировано первоначально.</span><span class="sxs-lookup"><span data-stu-id="69f64-149">If the EAC is less than the planned cost, the task is projected to cost less than was originally planned.</span></span> <span data-ttu-id="69f64-150">Следовательно, имеется тенденция расходов ниже бюджета.</span><span class="sxs-lookup"><span data-stu-id="69f64-150">Therefore, it's trending under budget.</span></span>

## <a name="project-managers-re-projection-of-cost"></a><span data-ttu-id="69f64-151">Изменение прогноза стоимости руководителем проекта</span><span class="sxs-lookup"><span data-stu-id="69f64-151">Project manager’s re-projection of cost</span></span>

<span data-ttu-id="69f64-152">При изменении прогноза усилий CTC, ПОПЗ, процент потребленной стоимости и отклонение прогнозируемой стоимости все пересчитываются в представлении **Отслеживание стоимости**.</span><span class="sxs-lookup"><span data-stu-id="69f64-152">When effort is re-projected, the CTC, EAC, percentage of cost consumed, and projected cost variance are all recalculated in the **Cost tracking** view.</span></span>

## <a name="project-status-summary"></a><span data-ttu-id="69f64-153">Общие сведения о состоянии проекта</span><span class="sxs-lookup"><span data-stu-id="69f64-153">Project status summary</span></span>

<span data-ttu-id="69f64-154">Отслеживание данных в представлениях **Отслеживание усилий** и **Отслеживание стоимости** показывает ход выполнения и потребление стоимости на уровнях корневого узла проекта, сводных задач и задач листовых узлов.</span><span class="sxs-lookup"><span data-stu-id="69f64-154">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="69f64-155">Раздел **Состояние** на странице **Сущность** проекта отображается сводка состояния на уровне проекта.</span><span class="sxs-lookup"><span data-stu-id="69f64-155">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="69f64-156">Поля сводки состояния</span><span class="sxs-lookup"><span data-stu-id="69f64-156">Status summary fields</span></span>

<span data-ttu-id="69f64-157">Поле **Общее состояние проекта** — это изменяемое поле, которое показывает общее состояние проекта.</span><span class="sxs-lookup"><span data-stu-id="69f64-157">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="69f64-158">В нем используется кодирование цветами, такими как зеленый, желтый и красный, для обозначения возрастания риска.</span><span class="sxs-lookup"><span data-stu-id="69f64-158">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="69f64-159">Поле **Комментарии** позволяет руководителю проекта ввести конкретные комментарии о состоянии.</span><span class="sxs-lookup"><span data-stu-id="69f64-159">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="69f64-160">Поле **Время обновления состояния** не допускает редактирования и содержит значение отметки времени, которая указывает, когда состояние было обновлено в последний раз.</span><span class="sxs-lookup"><span data-stu-id="69f64-160">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="69f64-161">Поля **Отклонение от календарного плана** и **Отклонение стоимости** задаются из даты отслеживания.</span><span class="sxs-lookup"><span data-stu-id="69f64-161">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="69f64-162">Если расписание и отклонение стоимости для корневого узла в представлении **Отслеживание усилий** положительно, для этих полей можно задать значение **С опережением**.</span><span class="sxs-lookup"><span data-stu-id="69f64-162">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="69f64-163">Если расписание и отклонение стоимости для корневого узла отрицательные, можно задать для них значение **С опозданием**.</span><span class="sxs-lookup"><span data-stu-id="69f64-163">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>
