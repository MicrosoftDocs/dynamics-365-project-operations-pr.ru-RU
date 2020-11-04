---
title: Резервирования и назначения
description: Этот тема предоставляет информацию о различиях между резервированием ресурсов и назначением ресурсов.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fa99783e52dbcdeaf80bbfd03df0f458f86b5e99
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083037"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="750f0-103">Резервирования и назначения</span><span class="sxs-lookup"><span data-stu-id="750f0-103">Bookings vs assignments</span></span>

<span data-ttu-id="750f0-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="750f0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="750f0-105">Резервирования — это окончательное или предварительное назначение ресурсов проекту.</span><span class="sxs-lookup"><span data-stu-id="750f0-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="750f0-106">Окончательные резервирования потребляет производительность ресурса.</span><span class="sxs-lookup"><span data-stu-id="750f0-106">Hard bookings consume a resource's capacity.</span></span> 

<span data-ttu-id="750f0-107">Назначения — это назначение ресурсов задачам проекта в расписании проекта.</span><span class="sxs-lookup"><span data-stu-id="750f0-107">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="750f0-108">Ресурсы могут быть реальными или универсальными.</span><span class="sxs-lookup"><span data-stu-id="750f0-108">The resources can be real or generic.</span></span> 

<span data-ttu-id="750f0-109">В идеальном случае для реальных ресурсов резервирования и назначения должны быть согласованы, поскольку они не отличаются.</span><span class="sxs-lookup"><span data-stu-id="750f0-109">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="750f0-110">Однако Microsoft Dynamics Project Operations не задает такое согласование принудительно.</span><span class="sxs-lookup"><span data-stu-id="750f0-110">However, Microsoft Dynamics Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="750f0-111">Представление **Выверка** показывает руководителю проекта места, в которых резервирования и назначения ресурсов не согласованы.</span><span class="sxs-lookup"><span data-stu-id="750f0-111">The **Reconciliation** view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>
