---
title: Вопросы и ответы по управлению ресурсами
description: Этот раздел содержит ответы на часто задаваемые вопросы об управлении ресурсами.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: fdf7f1e2-e4a2-4c68-aa03-4a41c7b10531
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 87da759b3b30ed6d38866c045194cde79837c209
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755007"
---
# <a name="resource-management-faq"></a><span data-ttu-id="37e9f-103">Вопросы и ответы по управлению ресурсами</span><span class="sxs-lookup"><span data-stu-id="37e9f-103">Resource management FAQ</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a><span data-ttu-id="37e9f-104">В чем разница между участником рабочей группы и требованием ресурса?</span><span class="sxs-lookup"><span data-stu-id="37e9f-104">What is the difference between a team member and a resource requirement?</span></span>

<span data-ttu-id="37e9f-105">Участника проектной группы можно назначить задачам, зарезервировать или избыточно зарезервировать, а также задать как утверждающего.</span><span class="sxs-lookup"><span data-stu-id="37e9f-105">A project team member can be assigned to tasks, booked or overbooked, and set as an approver.</span></span> <span data-ttu-id="37e9f-106">Требование ресурса может существовать без участника проектной группы, как черновое примечание требования.</span><span class="sxs-lookup"><span data-stu-id="37e9f-106">A resource requirement can exist without a project team member, as a draft note of demand.</span></span> 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a><span data-ttu-id="37e9f-107">В чем разница между предложенными и предварительно зарезервированными часами?</span><span class="sxs-lookup"><span data-stu-id="37e9f-107">What is the difference between proposed and soft-booked hours?</span></span>

<span data-ttu-id="37e9f-108">Предлагаемые часы и предварительно зарезервированные часы различаются по видимости.</span><span class="sxs-lookup"><span data-stu-id="37e9f-108">Proposed hours and soft-booked hours differ in visibility.</span></span> <span data-ttu-id="37e9f-109">Предлагаемые часы отображаются только менеджерам по ресурсам и руководителю проекта, который инициировал требование с помощью запроса ресурса.</span><span class="sxs-lookup"><span data-stu-id="37e9f-109">Proposed hours are visible only to resource managers and the project manager who initiated the demand by using a resource request.</span></span> <span data-ttu-id="37e9f-110">Предварительно зарезервированные часы видны всем, кто имеет доступ к доске расписания.</span><span class="sxs-lookup"><span data-stu-id="37e9f-110">Soft-booked hours are visible to anyone who has access to the Schedule Board.</span></span>

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a><span data-ttu-id="37e9f-111">Как посмотреть предварительно зарезервированные часы для ресурсов в рабочей группе?</span><span class="sxs-lookup"><span data-stu-id="37e9f-111">How can I see the soft-booked hours for resources on a team?</span></span>

<span data-ttu-id="37e9f-112">Предварительные резервирования можно создавать при резервировании требования ресурса.</span><span class="sxs-lookup"><span data-stu-id="37e9f-112">Soft bookings can made when you book a resource requirement.</span></span> <span data-ttu-id="37e9f-113">Ресурсы, которые предварительно зарезервированы для рабочей группы проекта, отображаются как участники рабочей группы, имеющие предварительно зарезервированные часы.</span><span class="sxs-lookup"><span data-stu-id="37e9f-113">Resources that are soft-booked on a project team appear as team members who have soft-booked hours.</span></span> <span data-ttu-id="37e9f-114">Также они отображаются на доске расписания.</span><span class="sxs-lookup"><span data-stu-id="37e9f-114">They also appear on the Schedule Board.</span></span>

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a><span data-ttu-id="37e9f-115">Как изменить необходимые часы, а также даты начала и окончания, для ресурса (универсального или именованного), который я зарезервировал?</span><span class="sxs-lookup"><span data-stu-id="37e9f-115">How do I change the required hours, and the start and end dates, for a resource (generic or named) that I booked?</span></span>

<span data-ttu-id="37e9f-116">После того как ресурс зарезервирован, выберите **Ведение резервирований** для внесения изменений, когда это необходимо.</span><span class="sxs-lookup"><span data-stu-id="37e9f-116">After resources are booked, select **Maintain Bookings** to make any changes that are required.</span></span>

## <a name="what-resources-types-does-project-service-automation-support"></a><span data-ttu-id="37e9f-117">Какие типы ресурсов поддерживает Project Service Automation?</span><span class="sxs-lookup"><span data-stu-id="37e9f-117">What resources types does Project Service Automation support?</span></span>

<span data-ttu-id="37e9f-118">**Пользователь** и **Контакт** — это единственные типы ресурсов, которые поддерживаются в Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="37e9f-118">**User** and **Contact** are the only resource types that are supported in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="37e9f-119">Хотя можно создать другие типы ресурсов (например, **Оборудование** и **Группа**), для них не поддерживается сквозное использование.</span><span class="sxs-lookup"><span data-stu-id="37e9f-119">Although you can create other types of resources (for example, **Equipment** and **Group**), no end-to-end use case is supported for them.</span></span>

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a><span data-ttu-id="37e9f-120">В чем разница между назначением и резервированием?</span><span class="sxs-lookup"><span data-stu-id="37e9f-120">What is the difference between an assignment and a booking?</span></span>

<span data-ttu-id="37e9f-121">Назначения — это назначение ресурсов задачам проекта в расписании проекта.</span><span class="sxs-lookup"><span data-stu-id="37e9f-121">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="37e9f-122">Ресурсы могут быть реальными или универсальными ресурсами.</span><span class="sxs-lookup"><span data-stu-id="37e9f-122">The resources can be either real or generic resources.</span></span> <span data-ttu-id="37e9f-123">Резервирования — это окончательное или предварительное назначение ресурсов проекту.</span><span class="sxs-lookup"><span data-stu-id="37e9f-123">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="37e9f-124">Окончательные резервирования потребляет производительность ресурса.</span><span class="sxs-lookup"><span data-stu-id="37e9f-124">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="37e9f-125">В идеальном случае для реальных ресурсов резервирования и назначения должны быть согласованы, поскольку они не отличаются.</span><span class="sxs-lookup"><span data-stu-id="37e9f-125">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="37e9f-126">Однако PSA не задает такое согласование принудительно.</span><span class="sxs-lookup"><span data-stu-id="37e9f-126">However, PSA doesn't enforce this agreement.</span></span> <span data-ttu-id="37e9f-127">Представление "Выверка" показывает руководителю проекта места, в которых резервирования и назначения ресурсов не согласованы.</span><span class="sxs-lookup"><span data-stu-id="37e9f-127">The Reconciliation view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>