---
title: Режимы планирования
description: В этом разделе представлена информация о режимах планирования.
author: ruhercul
manager: AnnBe
ms.date: 05/04/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fe54944999617b248ff925148a78601dd4be7aca
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981451"
---
# <a name="scheduling-modes"></a><span data-ttu-id="80518-103">Режимы планирования</span><span class="sxs-lookup"><span data-stu-id="80518-103">Scheduling modes</span></span>

<span data-ttu-id="80518-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="80518-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="80518-105">Dynamics 365 Project Operations предоставляет организациям возможность определять, как они управляют изменениями ключевых переменных в задачах в структурная декомпозиция работ.</span><span class="sxs-lookup"><span data-stu-id="80518-105">Dynamics 365 Project Operations provides the ability for organizations to define how they manage changes to key variables in tasks within the work breakdown structure.</span></span> <span data-ttu-id="80518-106">В зависимости от конкретных потребностей организации руководители проектов могут вносить изменения в режим планирования при создании проекта.</span><span class="sxs-lookup"><span data-stu-id="80518-106">Based on the specific needs of the organization, Project Managers can make changes to the scheduling mode when a project is created.</span></span>

<span data-ttu-id="80518-107">В Project Operations доступно три режима планирования:</span><span class="sxs-lookup"><span data-stu-id="80518-107">There are three scheduling modes available in Project Operations:</span></span>

  - <span data-ttu-id="80518-108">Фиксированная длительность (это режим по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="80518-108">Fixed duration (this is the default mode)</span></span>
  - <span data-ttu-id="80518-109">Фиксированная работа</span><span class="sxs-lookup"><span data-stu-id="80518-109">Fixed work</span></span>
  - <span data-ttu-id="80518-110">Фиксированные единицы</span><span class="sxs-lookup"><span data-stu-id="80518-110">Fixed units</span></span>

<span data-ttu-id="80518-111">Значения, на которые влияет определение конкретного режима планирования, определяются по следующей формуле:</span><span class="sxs-lookup"><span data-stu-id="80518-111">The values impacted by the definition of a specific scheduling mode are determined by the following formula:</span></span>

  <span data-ttu-id="80518-112">Трудозатраты (*Работа*) = Длительность x Единицы</span><span class="sxs-lookup"><span data-stu-id="80518-112">Effort (*Work*) = Duration x Units</span></span>

<span data-ttu-id="80518-113">Когда вы определяете режим планирования проекта, вы устанавливаете одно из этих значений, которое затем нельзя изменить.</span><span class="sxs-lookup"><span data-stu-id="80518-113">When you define a project’s scheduling mode, you are setting one of these values, which then can't be changed.</span></span> <span data-ttu-id="80518-114">Сохранение этого значения как константы дает этому значению приоритет, который уведомляет систему о том, чтобы не изменять его при изменении двух других значений.</span><span class="sxs-lookup"><span data-stu-id="80518-114">Holding this value as a constant places a priority on that value, which notifies the system not to change it when the other two values change.</span></span> <span data-ttu-id="80518-115">В следующей таблице представлена информация о влиянии выбора определенного режима.</span><span class="sxs-lookup"><span data-stu-id="80518-115">The following table provides information about the impacts of selecting a specific mode.</span></span>

| <span data-ttu-id="80518-116">**Закрепить задачу**</span><span class="sxs-lookup"><span data-stu-id="80518-116">**In this task**</span></span>             | <span data-ttu-id="80518-117">**Если вы пересматриваете единицы**</span><span class="sxs-lookup"><span data-stu-id="80518-117">**If you revise units**</span></span>   | <span data-ttu-id="80518-118">**Если вы пересматриваете длительность**</span><span class="sxs-lookup"><span data-stu-id="80518-118">**If you revise duration**</span></span> | <span data-ttu-id="80518-119">**Если вы пересматриваете трудозатраты**</span><span class="sxs-lookup"><span data-stu-id="80518-119">**If you revise effort**</span></span>  |
|----------------------|---------------------------|----------------------------|---------------------------|
| <span data-ttu-id="80518-120">Задачи фиксированных единиц</span><span class="sxs-lookup"><span data-stu-id="80518-120">Fixed units task</span></span>     | <span data-ttu-id="80518-121">Длительность пересчитывается.</span><span class="sxs-lookup"><span data-stu-id="80518-121">Duration is recalculated.</span></span> | <span data-ttu-id="80518-122">Перерасчет трудозатрат.</span><span class="sxs-lookup"><span data-stu-id="80518-122">Effort is recalculated.</span></span>    | <span data-ttu-id="80518-123">Длительность пересчитывается.</span><span class="sxs-lookup"><span data-stu-id="80518-123">Duration is recalculated.</span></span> |
| <span data-ttu-id="80518-124">Задача постоянных трудозатрат</span><span class="sxs-lookup"><span data-stu-id="80518-124">Fixed effort task</span></span>    | <span data-ttu-id="80518-125">Длительность пересчитывается.</span><span class="sxs-lookup"><span data-stu-id="80518-125">Duration is recalculated.</span></span> | <span data-ttu-id="80518-126">Единицы пересчитываются.</span><span class="sxs-lookup"><span data-stu-id="80518-126">Units are recalculated.</span></span>    | <span data-ttu-id="80518-127">Длительность пересчитывается.</span><span class="sxs-lookup"><span data-stu-id="80518-127">Duration is recalculated.</span></span> |
| <span data-ttu-id="80518-128">Задача фиксированной длительности</span><span class="sxs-lookup"><span data-stu-id="80518-128">Fixed duration task</span></span>  | <span data-ttu-id="80518-129">Перерасчет трудозатрат.</span><span class="sxs-lookup"><span data-stu-id="80518-129">Effort is recalculated.</span></span>   | <span data-ttu-id="80518-130">Перерасчет трудозатрат.</span><span class="sxs-lookup"><span data-stu-id="80518-130">Effort is recalculated.</span></span>    | <span data-ttu-id="80518-131">Единицы пересчитываются.</span><span class="sxs-lookup"><span data-stu-id="80518-131">Units are recalculated.</span></span>   |

<span data-ttu-id="80518-132">Дополнительные сведения о последствиях данного режима см. [Измените тип задачи для более точного планирования](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span><span class="sxs-lookup"><span data-stu-id="80518-132">For more information about the implications of a given mode, see [Change the task type for more accurate scheduling](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span></span> <span data-ttu-id="80518-133">В данной теме термин **Работа** используется вместо **Трудозатраты**.</span><span class="sxs-lookup"><span data-stu-id="80518-133">In the topic, the term **Work** is used instead of **Effort**.</span></span>

## <a name="change-the-organizations-scheduling-mode"></a><span data-ttu-id="80518-134">Изменить режим планирования организации</span><span class="sxs-lookup"><span data-stu-id="80518-134">Change the organization’s scheduling mode</span></span>

<span data-ttu-id="80518-135">Выполните следующие шаги, чтобы определить режим планирования организации.</span><span class="sxs-lookup"><span data-stu-id="80518-135">Complete the following steps to define the scheduling mode of an organization.</span></span>

1. <span data-ttu-id="80518-136">Перейти к **Настройки** \> **Общие** \> **Параметры**, а затем выберите параметр проекта.</span><span class="sxs-lookup"><span data-stu-id="80518-136">Go to **Settings** \> **General** \> **Parameters**, and then select the project parameter.</span></span> 
2. <span data-ttu-id="80518-137">На странице **Параметры проекта** выберите режим планирования по умолчанию для организации, а затем определите возможность для руководителя проекта переопределить настройку при создании нового проекта.</span><span class="sxs-lookup"><span data-stu-id="80518-137">On the **Project Parameters** page, select the default scheduling mode for the organization, and then define ability for the Project manager to override the setting when creating a new project.</span></span>

## <a name="change-the-scheduling-mode-setting-on-a-project"></a><span data-ttu-id="80518-138">Изменить настройку режима планирования для проекта</span><span class="sxs-lookup"><span data-stu-id="80518-138">Change the scheduling mode setting on a project</span></span>

<span data-ttu-id="80518-139">Если организация позволяет руководителю проекта переопределить режим планирования по умолчанию, руководитель проекта может внести это изменение при создании нового проекта.</span><span class="sxs-lookup"><span data-stu-id="80518-139">If an organization allows the Project manager to override the default scheduling mode, the Project manager can make that change when they create a new project.</span></span> <span data-ttu-id="80518-140">Однако после сохранения проекта режим планирования изменить нельзя.</span><span class="sxs-lookup"><span data-stu-id="80518-140">However, after the project has been saved, the scheduling mode can't be changed.</span></span>

## <a name="copied-projects"></a><span data-ttu-id="80518-141">Скопированные проекты</span><span class="sxs-lookup"><span data-stu-id="80518-141">Copied projects</span></span>

<span data-ttu-id="80518-142">Поскольку проект создается при выполнении действия копирования проекта, руководитель проекта не может установить режим планирования.</span><span class="sxs-lookup"><span data-stu-id="80518-142">Because a project is created when the copy project action is taken, the Project manager can't set the scheduling mode.</span></span> <span data-ttu-id="80518-143">Целевой проект всегда будет по умолчанию настроен на режим, определенный на уровне организации.</span><span class="sxs-lookup"><span data-stu-id="80518-143">The destination project will always default to the mode defined at the organizational level.</span></span>

## <a name="copied-tasks"></a><span data-ttu-id="80518-144">Скопированные задачи</span><span class="sxs-lookup"><span data-stu-id="80518-144">Copied tasks</span></span>

<span data-ttu-id="80518-145">Когда задача копируется из одного проекта в другой, задача наследует режим планирования целевого проекта.</span><span class="sxs-lookup"><span data-stu-id="80518-145">When a task is copied from one project to another, the task inherits the scheduling mode of the destination project.</span></span>
