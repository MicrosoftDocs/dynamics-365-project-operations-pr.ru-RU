---
title: Обзор помощника по расписанию
description: Эта тема предоставляет информацию о работе с помощником по расписанию для резервирования ресурсов.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 92b12bd9272805a736286bf7e0ff926cb6361c05
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125644"
---
# <a name="schedule-assistant-overview"></a><span data-ttu-id="ea590-103">Обзор помощника по расписанию</span><span class="sxs-lookup"><span data-stu-id="ea590-103">Schedule assistant overview</span></span>

<span data-ttu-id="ea590-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="ea590-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ea590-105">Помощник по расписанию используется для резервирования ресурсов на основе требований, определенных менеджером проекта.</span><span class="sxs-lookup"><span data-stu-id="ea590-105">The Schedule assistant is used to book resources based on requirements defined by the Project manager.</span></span> <span data-ttu-id="ea590-106">Помощник по расписанию использует параметры, указанные в требовании к ресурсу, чтобы найти ресурс.</span><span class="sxs-lookup"><span data-stu-id="ea590-106">The schedule assistant relies on the parameters provided in the resource requirement to find the resource.</span></span> <span data-ttu-id="ea590-107">Помощник по расписанию рекомендует ресурсы, соответствующие соответствующим требованиям, например временным окнам или необходимым навыкам.</span><span class="sxs-lookup"><span data-stu-id="ea590-107">The Schedule assistant recommends resources that match relevant requirements, like time windows or skills needed.</span></span>

<span data-ttu-id="ea590-108">После того, как подходящие ресурсы определены, менеджер ресурсов или проекта может зарезервировать ресурс для работы.</span><span class="sxs-lookup"><span data-stu-id="ea590-108">After suitable resources are identified, the Resource or Project manager can book the resource to the work.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ea590-109">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="ea590-109">Prerequisites</span></span>

<span data-ttu-id="ea590-110">Помощник по расписанию является частью решения Universal Resource Scheduling.</span><span class="sxs-lookup"><span data-stu-id="ea590-110">The Schedule assistant is a part of the Universal Resource Scheduling solution.</span></span> <span data-ttu-id="ea590-111">Это решение поставляется и устанавливается вместе с Dynamics 365 Project Operations, Dynamics 365 Field Service и Dynamics 365 Customer Service.</span><span class="sxs-lookup"><span data-stu-id="ea590-111">This solution is included and installed with Dynamics 365 Project Operations, Dynamics 365 Field Service, and Dynamics 365 Customer Service.</span></span>

## <a name="matching-requirements-and-resources"></a><span data-ttu-id="ea590-112">Сопоставление требований и ресурсов</span><span class="sxs-lookup"><span data-stu-id="ea590-112">Matching requirements and resources</span></span>

<span data-ttu-id="ea590-113">Сгенерированная потребность в ресурсах основана на таких деталях, как:</span><span class="sxs-lookup"><span data-stu-id="ea590-113">A generated resource requirement is based on details such as:</span></span>

-   <span data-ttu-id="ea590-114">Характеристики</span><span class="sxs-lookup"><span data-stu-id="ea590-114">Characteristics</span></span>
-   <span data-ttu-id="ea590-115">Роли</span><span class="sxs-lookup"><span data-stu-id="ea590-115">Roles</span></span>
-   <span data-ttu-id="ea590-116">Бизнес-единицы</span><span class="sxs-lookup"><span data-stu-id="ea590-116">Business units</span></span>
-   <span data-ttu-id="ea590-117">Предпочтения ресурсов</span><span class="sxs-lookup"><span data-stu-id="ea590-117">Resource preferences</span></span>
-   <span data-ttu-id="ea590-118">Контуры усилий</span><span class="sxs-lookup"><span data-stu-id="ea590-118">Effort contours</span></span>
-   <span data-ttu-id="ea590-119">Часовой пояс</span><span class="sxs-lookup"><span data-stu-id="ea590-119">Time zone</span></span>

<span data-ttu-id="ea590-120">Помощник по расписанию использует эти данные для фильтрации ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ea590-120">The Schedule assistant uses these details to filter resources.</span></span>

## <a name="launch-the-schedule-assistant"></a><span data-ttu-id="ea590-121">Запуск помощника по расписанию</span><span class="sxs-lookup"><span data-stu-id="ea590-121">Launch the Schedule assistant</span></span>

<span data-ttu-id="ea590-122">Помощник по расписанию можно запустить двумя способами.</span><span class="sxs-lookup"><span data-stu-id="ea590-122">There are two ways in which the schedule assistant is launched.</span></span> <span data-ttu-id="ea590-123">Если вы используете гибридный режим, в сетке участников рабочей группы вы можете выбрать любого участника рабочей группы с невыполненными требованиями к ресурсам, затем выбрать **Зарезервировать**.</span><span class="sxs-lookup"><span data-stu-id="ea590-123">If you're using the hybrid mode, in the team member grid you can select any team member with an unfulfilled resource requirement, and then select **Book**.</span></span> <span data-ttu-id="ea590-124">Если вы используете центральный режим, диспетчер ресурсов находит и выбирает ресурс.</span><span class="sxs-lookup"><span data-stu-id="ea590-124">If you're using the central mode, the Resource manager finds and selects the resource.</span></span>

## <a name="schedule-assistant-filters"></a><span data-ttu-id="ea590-125">Фильтры помощника по расписанию</span><span class="sxs-lookup"><span data-stu-id="ea590-125">Schedule assistant filters</span></span>

<span data-ttu-id="ea590-126">После выполнения помощника по расписанию сведения о требованиях к ресурсам отображаются в виде отфильтрованных значений на левой панели.</span><span class="sxs-lookup"><span data-stu-id="ea590-126">After the Schedule assistant runs, the details from the resource requirement are displayed as filtered values in the left pane.</span></span> <span data-ttu-id="ea590-127">Менеджер ресурсов или менеджер проекта может точно настроить результаты, настроив фильтры в соответствии с потребностями планирования.</span><span class="sxs-lookup"><span data-stu-id="ea590-127">The Resource manager or the Project manager can fine-tune results by adjusting filters to meet the scheduling needs.</span></span>

<span data-ttu-id="ea590-128">На панели фильтров отображаются параметры, связанные с работой, в том числе:</span><span class="sxs-lookup"><span data-stu-id="ea590-128">The filter pane shows work-related options, including:</span></span>

-   <span data-ttu-id="ea590-129">Начало и окончание работы</span><span class="sxs-lookup"><span data-stu-id="ea590-129">Work start and end</span></span>
-   <span data-ttu-id="ea590-130">Характеристики</span><span class="sxs-lookup"><span data-stu-id="ea590-130">Characteristics</span></span>
-   <span data-ttu-id="ea590-131">Роли</span><span class="sxs-lookup"><span data-stu-id="ea590-131">Roles</span></span>
-   <span data-ttu-id="ea590-132">Подразделения</span><span class="sxs-lookup"><span data-stu-id="ea590-132">Organizational units</span></span>
-   <span data-ttu-id="ea590-133">Компания распределения ресурсов</span><span class="sxs-lookup"><span data-stu-id="ea590-133">Resourcing company</span></span>
-   <span data-ttu-id="ea590-134">Типы ресурсов</span><span class="sxs-lookup"><span data-stu-id="ea590-134">Resource types</span></span>
-   <span data-ttu-id="ea590-135">Предпочитаемые ресурсы</span><span class="sxs-lookup"><span data-stu-id="ea590-135">Preferred resources</span></span>
