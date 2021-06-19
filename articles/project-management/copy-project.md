---
title: Копирование проекта
description: В этом разделе представлена информация о копировании проектов в Dynamics 365 Project Operations.
author: ruhercul
ms.date: 05/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c3055ab5b8c07faa2bc9167956d283e2a66029dd
ms.sourcegitcommit: 173f2b1f4e063c440a5f78d76d456c62aadbd89e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/24/2021
ms.locfileid: "6091270"
---
# <a name="copy-a-project"></a><span data-ttu-id="fd4ce-103">Копирование проекта</span><span class="sxs-lookup"><span data-stu-id="fd4ce-103">Copy a project</span></span>

<span data-ttu-id="fd4ce-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="fd4ce-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="fd4ce-105">С Dynamics 365 Project Operations вы можете быстро создавать новые проекты, выбирая **Копировать проект** в форме **Проекты**.</span><span class="sxs-lookup"><span data-stu-id="fd4ce-105">With Dynamics 365 Project Operations, you can quickly build new projects by selecting **Copy Project** on the **Projects** form.</span></span> <span data-ttu-id="fd4ce-106">Чтобы скопировать проект, откройте проект, который вы хотите скопировать, затем выберите **Копировать проект**.</span><span class="sxs-lookup"><span data-stu-id="fd4ce-106">To copy a project, open the project you want to copy, and then select **Copy project**.</span></span> <span data-ttu-id="fd4ce-107">Действие скопирует следующее:</span><span class="sxs-lookup"><span data-stu-id="fd4ce-107">The action will copy the following:</span></span>

- <span data-ttu-id="fd4ce-108">Свойства проекта</span><span class="sxs-lookup"><span data-stu-id="fd4ce-108">Project properties</span></span> 
- <span data-ttu-id="fd4ce-109">Структурная декомпозиция работ</span><span class="sxs-lookup"><span data-stu-id="fd4ce-109">Work breakdown structure</span></span>
- <span data-ttu-id="fd4ce-110">Участники проектной группы</span><span class="sxs-lookup"><span data-stu-id="fd4ce-110">Project team members</span></span>
- <span data-ttu-id="fd4ce-111">Оценки проекта</span><span class="sxs-lookup"><span data-stu-id="fd4ce-111">Project estimates</span></span>
- <span data-ttu-id="fd4ce-112">Оценки расходов по проекту</span><span class="sxs-lookup"><span data-stu-id="fd4ce-112">Project expense estimates</span></span>
- <span data-ttu-id="fd4ce-113">Оценки материалов проекта</span><span class="sxs-lookup"><span data-stu-id="fd4ce-113">Project material estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="fd4ce-114">Свойства проекта</span><span class="sxs-lookup"><span data-stu-id="fd4ce-114">Project properties</span></span>

<span data-ttu-id="fd4ce-115">При копировании проекта копируются значения в следующих полях:</span><span class="sxs-lookup"><span data-stu-id="fd4ce-115">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="fd4ce-116">Название</span><span class="sxs-lookup"><span data-stu-id="fd4ce-116">Name</span></span>
- <span data-ttu-id="fd4ce-117">Описание:</span><span class="sxs-lookup"><span data-stu-id="fd4ce-117">Description</span></span>
- <span data-ttu-id="fd4ce-118">Клиент</span><span class="sxs-lookup"><span data-stu-id="fd4ce-118">Customer</span></span>
- <span data-ttu-id="fd4ce-119">Шаблон календаря</span><span class="sxs-lookup"><span data-stu-id="fd4ce-119">Calendar Template</span></span>
- <span data-ttu-id="fd4ce-120">Валюта</span><span class="sxs-lookup"><span data-stu-id="fd4ce-120">Currency</span></span>
- <span data-ttu-id="fd4ce-121">Единица по контракту</span><span class="sxs-lookup"><span data-stu-id="fd4ce-121">Contracting Unit</span></span>
- <span data-ttu-id="fd4ce-122">Руководитель проекта</span><span class="sxs-lookup"><span data-stu-id="fd4ce-122">Project Manager</span></span>
- <span data-ttu-id="fd4ce-123">Состояние</span><span class="sxs-lookup"><span data-stu-id="fd4ce-123">Status</span></span>
- <span data-ttu-id="fd4ce-124">Общее состояние проекта</span><span class="sxs-lookup"><span data-stu-id="fd4ce-124">Overall Project Status</span></span>
- <span data-ttu-id="fd4ce-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fd4ce-125">Comments</span></span>
- <span data-ttu-id="fd4ce-126">Оценки</span><span class="sxs-lookup"><span data-stu-id="fd4ce-126">Estimates</span></span>
- <span data-ttu-id="fd4ce-127">Предполагаемая дата начала: это дата создания проекта из копии.</span><span class="sxs-lookup"><span data-stu-id="fd4ce-127">Estimated Start Date: This is the date that the project is created from the copy.</span></span>
- <span data-ttu-id="fd4ce-128">Предполагаемая дата окончания: эта дата корректируется в зависимости от даты начала нового проекта, созданного из копии.</span><span class="sxs-lookup"><span data-stu-id="fd4ce-128">Estimated Finish Date: This date is adjusted based on the start date of the new project that was made from the copy.</span></span>
- <span data-ttu-id="fd4ce-129">Усилия (часы)</span><span class="sxs-lookup"><span data-stu-id="fd4ce-129">Effort (Hours)</span></span>
- <span data-ttu-id="fd4ce-130">Расчетная стоимость трудозатрат</span><span class="sxs-lookup"><span data-stu-id="fd4ce-130">Estimated Labor Cost</span></span>
- <span data-ttu-id="fd4ce-131">Расчетная стоимость расходов</span><span class="sxs-lookup"><span data-stu-id="fd4ce-131">Estimated Expense Cost</span></span>
- <span data-ttu-id="fd4ce-132">Расчетная стоимость материалов</span><span class="sxs-lookup"><span data-stu-id="fd4ce-132">Estimated Material Cost</span></span>

> [!NOTE]
> <span data-ttu-id="fd4ce-133">Копирование проекта — это длительная операция.</span><span class="sxs-lookup"><span data-stu-id="fd4ce-133">Copy project is a long running operation.</span></span> <span data-ttu-id="fd4ce-134">Записи проекта, их соответствующие атрибуты и многие связанные сущности также копируются.</span><span class="sxs-lookup"><span data-stu-id="fd4ce-134">Project records, their relevant attributes, and many related entities are also copied.</span></span> <span data-ttu-id="fd4ce-135">Из-за длительного характера операции после начала копирования страница целевого проекта блокируется для редактирования до завершения операции копирования.</span><span class="sxs-lookup"><span data-stu-id="fd4ce-135">Because of the long running nature of the operation, after the copy starts, the target project page is locked for editing until the copy operation is complete.</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="fd4ce-136">Структурная декомпозиция работ</span><span class="sxs-lookup"><span data-stu-id="fd4ce-136">Work breakdown structure</span></span>

<span data-ttu-id="fd4ce-137">При копировании проекта копируется вся иерархическая структурная декомпозиция работ с загруженными ресурсами.</span><span class="sxs-lookup"><span data-stu-id="fd4ce-137">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="fd4ce-138">Именованные ресурсы заменяются универсальными ресурсами.</span><span class="sxs-lookup"><span data-stu-id="fd4ce-138">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="fd4ce-139">Если у именованных ресурсов нет того же рабочего времени, что и у универсального ресурса, расписание будет пересчитано, и продолжительность задач может измениться.</span><span class="sxs-lookup"><span data-stu-id="fd4ce-139">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="fd4ce-140">Участники проектной группы</span><span class="sxs-lookup"><span data-stu-id="fd4ce-140">Project team members</span></span>

<span data-ttu-id="fd4ce-141">Когда проектная группа копируется из исходного проекта, копируются универсальные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="fd4ce-141">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="fd4ce-142">Назначения универсальных ресурсов также обслуживаются как в исходном проекте.</span><span class="sxs-lookup"><span data-stu-id="fd4ce-142">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="fd4ce-143">Именованные ресурсы будут преобразованы в универсальных участников рабочей группы.</span><span class="sxs-lookup"><span data-stu-id="fd4ce-143">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="fd4ce-144">Оценки</span><span class="sxs-lookup"><span data-stu-id="fd4ce-144">Estimates</span></span>

<span data-ttu-id="fd4ce-145">При копировании проекта строки оценок ресурсов, расходов и материалов копируются из исходного проекта.</span><span class="sxs-lookup"><span data-stu-id="fd4ce-145">When the project is copied, resource, expense and material estimate lines are copied from the source project.</span></span> 

<span data-ttu-id="fd4ce-146">Для получения информации о том, как программными средствами получить доступ к копированию проекта, см. раздел [Разработка шаблонов проектов с помощью копирования проекта](dev-copy-project.md).</span><span class="sxs-lookup"><span data-stu-id="fd4ce-146">For information on how to programmatically access Copy Project, see [Develop project templates with Copy Project](dev-copy-project.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
