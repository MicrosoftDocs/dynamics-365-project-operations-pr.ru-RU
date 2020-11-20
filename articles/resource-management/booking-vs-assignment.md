---
title: Резервирования и назначения
description: Этот тема предоставляет информацию о различиях между резервированием ресурсов и назначением ресурсов.
author: ruhercul
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8fe6937dfdfe137f28917c16da1d7dc6155284ae
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130234"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="4c3c5-103">Резервирования и назначения</span><span class="sxs-lookup"><span data-stu-id="4c3c5-103">Bookings vs assignments</span></span>

<span data-ttu-id="4c3c5-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="4c3c5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4c3c5-105">Резервирования — это окончательное или предварительное назначение ресурсов проекту.</span><span class="sxs-lookup"><span data-stu-id="4c3c5-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="4c3c5-106">Окончательные резервирования потребляет производительность ресурса.</span><span class="sxs-lookup"><span data-stu-id="4c3c5-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="4c3c5-107">Резервирования представляют собой организационные концепции для рабочих групп, чтобы они могли понять, как ресурсы будут задействованы в различных проектах.</span><span class="sxs-lookup"><span data-stu-id="4c3c5-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="4c3c5-108">Dynamics 365 Project Operations рассматривает резервирования как концепцию уровня проекта.</span><span class="sxs-lookup"><span data-stu-id="4c3c5-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="4c3c5-109">В отличие от резервирований, назначения — это назначение ресурсов задачам проекта в расписании проекта.</span><span class="sxs-lookup"><span data-stu-id="4c3c5-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="4c3c5-110">Ресурсы могут быть именованными или универсальными.</span><span class="sxs-lookup"><span data-stu-id="4c3c5-110">The resources can be named or generic.</span></span> 

<span data-ttu-id="4c3c5-111">Обычно сумма резервирований для ресурса равна сумме назначений ресурса по одной или нескольким задачам.</span><span class="sxs-lookup"><span data-stu-id="4c3c5-111">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="4c3c5-112">Однако Project Operations не задает такое согласование принудительно.</span><span class="sxs-lookup"><span data-stu-id="4c3c5-112">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="4c3c5-113">Представление **Выверка** показывает руководителю проекта места, в которых резервирования и назначения ресурсов не согласованы.</span><span class="sxs-lookup"><span data-stu-id="4c3c5-113">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>
