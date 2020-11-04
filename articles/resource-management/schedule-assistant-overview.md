---
title: Обзор помощника по расписанию
description: Эта тема предоставляет информацию о работе с помощником по расписанию для резервирования ресурсов.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: da551e805f395e466952df1dbb7d193bdddba358
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083044"
---
# <a name="schedule-assistant-overview"></a><span data-ttu-id="7570f-103">Обзор помощника по расписанию</span><span class="sxs-lookup"><span data-stu-id="7570f-103">Schedule assistant overview</span></span>

<span data-ttu-id="7570f-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="7570f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="7570f-105">Помощник по расписанию используется для резервирования ресурсов на основе требований, определенных менеджером проекта.</span><span class="sxs-lookup"><span data-stu-id="7570f-105">The Schedule assistant is used to book resources based on requirements defined by the Project manager.</span></span> <span data-ttu-id="7570f-106">Помощник по расписанию использует параметры, указанные в требовании к ресурсу, чтобы найти ресурс.</span><span class="sxs-lookup"><span data-stu-id="7570f-106">The schedule assistant relies on the parameters provided in the resource requirement to find the resource.</span></span> <span data-ttu-id="7570f-107">Помощник по расписанию рекомендует ресурсы, соответствующие соответствующим требованиям, например временным окнам или необходимым навыкам.</span><span class="sxs-lookup"><span data-stu-id="7570f-107">The Schedule assistant recommends resources that match relevant requirements, like time windows or skills needed.</span></span>

<span data-ttu-id="7570f-108">После того, как подходящие ресурсы определены, менеджер ресурсов или проекта может зарезервировать ресурс для работы.</span><span class="sxs-lookup"><span data-stu-id="7570f-108">After suitable resources are identified, the Resource or Project manager can book the resource to the work.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="7570f-109">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="7570f-109">Prerequisites</span></span>

<span data-ttu-id="7570f-110">Помощник по расписанию является частью решения Universal Resource Scheduling.</span><span class="sxs-lookup"><span data-stu-id="7570f-110">The Schedule assistant is a part of the Universal Resource Scheduling solution.</span></span> <span data-ttu-id="7570f-111">Это решение поставляется и устанавливается вместе с Dynamics 365 Project Operations, Dynamics 365 Field Service и Dynamics 365 Customer Service.</span><span class="sxs-lookup"><span data-stu-id="7570f-111">This solution is included and installed with Dynamics 365 Project Operations, Dynamics 365 Field Service, and Dynamics 365 Customer Service.</span></span>

## <a name="matching-requirements-and-resources"></a><span data-ttu-id="7570f-112">Сопоставление требований и ресурсов</span><span class="sxs-lookup"><span data-stu-id="7570f-112">Matching requirements and resources</span></span>

<span data-ttu-id="7570f-113">Сгенерированная потребность в ресурсах основана на таких деталях, как:</span><span class="sxs-lookup"><span data-stu-id="7570f-113">A generated resource requirement is based on details such as:</span></span>

-   <span data-ttu-id="7570f-114">Характеристики</span><span class="sxs-lookup"><span data-stu-id="7570f-114">Characteristics</span></span>
-   <span data-ttu-id="7570f-115">Роли</span><span class="sxs-lookup"><span data-stu-id="7570f-115">Roles</span></span>
-   <span data-ttu-id="7570f-116">Бизнес-единицы</span><span class="sxs-lookup"><span data-stu-id="7570f-116">Business units</span></span>
-   <span data-ttu-id="7570f-117">Предпочтения ресурсов</span><span class="sxs-lookup"><span data-stu-id="7570f-117">Resource preferences</span></span>
-   <span data-ttu-id="7570f-118">Контуры усилий</span><span class="sxs-lookup"><span data-stu-id="7570f-118">Effort contours</span></span>
-   <span data-ttu-id="7570f-119">Часовой пояс</span><span class="sxs-lookup"><span data-stu-id="7570f-119">Time zone</span></span>

<span data-ttu-id="7570f-120">Помощник по расписанию использует эти данные для фильтрации ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7570f-120">The Schedule assistant uses these details to filter resources.</span></span>

## <a name="launch-the-schedule-assistant"></a><span data-ttu-id="7570f-121">Запуск помощника по расписанию</span><span class="sxs-lookup"><span data-stu-id="7570f-121">Launch the Schedule assistant</span></span>

<span data-ttu-id="7570f-122">Помощник по расписанию можно запустить двумя способами.</span><span class="sxs-lookup"><span data-stu-id="7570f-122">There are two ways in which the schedule assistant is launched.</span></span> <span data-ttu-id="7570f-123">Если вы используете гибридный режим, в сетке участников рабочей группы вы можете выбрать любого участника рабочей группы с невыполненными требованиями к ресурсам, затем выбрать **Зарезервировать**.</span><span class="sxs-lookup"><span data-stu-id="7570f-123">If you're using the hybrid mode, in the team member grid you can select any team member with an unfulfilled resource requirement, and then select **Book**.</span></span> <span data-ttu-id="7570f-124">Если вы используете центральный режим, диспетчер ресурсов находит и выбирает ресурс.</span><span class="sxs-lookup"><span data-stu-id="7570f-124">If you're using the central mode, the Resource manager finds and selects the resource.</span></span>

## <a name="schedule-assistant-filters"></a><span data-ttu-id="7570f-125">Фильтры помощника по расписанию</span><span class="sxs-lookup"><span data-stu-id="7570f-125">Schedule assistant filters</span></span>

<span data-ttu-id="7570f-126">После выполнения помощника по расписанию сведения о требованиях к ресурсам отображаются в виде отфильтрованных значений на левой панели.</span><span class="sxs-lookup"><span data-stu-id="7570f-126">After the Schedule assistant runs, the details from the resource requirement are displayed as filtered values in the left pane.</span></span> <span data-ttu-id="7570f-127">Менеджер ресурсов или менеджер проекта может точно настроить результаты, настроив фильтры в соответствии с потребностями планирования.</span><span class="sxs-lookup"><span data-stu-id="7570f-127">The Resource manager or the Project manager can fine-tune results by adjusting filters to meet the scheduling needs.</span></span>

<span data-ttu-id="7570f-128">На панели фильтров отображаются параметры, связанные с работой, в том числе:</span><span class="sxs-lookup"><span data-stu-id="7570f-128">The filter pane shows work-related options, including:</span></span>

-   <span data-ttu-id="7570f-129">Начало и окончание работы</span><span class="sxs-lookup"><span data-stu-id="7570f-129">Work start and end</span></span>
-   <span data-ttu-id="7570f-130">Характеристики</span><span class="sxs-lookup"><span data-stu-id="7570f-130">Characteristics</span></span>
-   <span data-ttu-id="7570f-131">Роли</span><span class="sxs-lookup"><span data-stu-id="7570f-131">Roles</span></span>
-   <span data-ttu-id="7570f-132">Подразделения</span><span class="sxs-lookup"><span data-stu-id="7570f-132">Organizational units</span></span>
-   <span data-ttu-id="7570f-133">Компания распределения ресурсов</span><span class="sxs-lookup"><span data-stu-id="7570f-133">Resourcing company</span></span>
-   <span data-ttu-id="7570f-134">Типы ресурсов</span><span class="sxs-lookup"><span data-stu-id="7570f-134">Resource types</span></span>
-   <span data-ttu-id="7570f-135">Предпочитаемые ресурсы</span><span class="sxs-lookup"><span data-stu-id="7570f-135">Preferred resources</span></span>
