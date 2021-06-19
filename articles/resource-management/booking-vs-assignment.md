---
title: Резервирования и назначения
description: Этот тема предоставляет информацию о различиях между резервированием ресурсов и назначением ресурсов.
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3c1a1003af0b23c4be44fefac0b3c4ea725f96b2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012782"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="2082d-103">Резервирования и назначения</span><span class="sxs-lookup"><span data-stu-id="2082d-103">Bookings vs assignments</span></span>

<span data-ttu-id="2082d-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="2082d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2082d-105">Резервирования — это окончательное или предварительное назначение ресурсов проекту.</span><span class="sxs-lookup"><span data-stu-id="2082d-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="2082d-106">Окончательные резервирования потребляет производительность ресурса.</span><span class="sxs-lookup"><span data-stu-id="2082d-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="2082d-107">Резервирования представляют собой организационные концепции для рабочих групп, чтобы они могли понять, как ресурсы будут задействованы в различных проектах.</span><span class="sxs-lookup"><span data-stu-id="2082d-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="2082d-108">Dynamics 365 Project Operations рассматривает резервирования как концепцию уровня проекта.</span><span class="sxs-lookup"><span data-stu-id="2082d-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="2082d-109">В отличие от резервирований, назначения — это назначение ресурсов задачам проекта в расписании проекта.</span><span class="sxs-lookup"><span data-stu-id="2082d-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="2082d-110">Ресурсы могут быть именованными или универсальными.</span><span class="sxs-lookup"><span data-stu-id="2082d-110">The resources can be named or generic.</span></span>  <span data-ttu-id="2082d-111">Когда потребность в ресурсах наследуется из назначений задач проекта, Project Operations использует профили трудозатрат по назначению ресурсов для построения профилей сведений требования ресурса.</span><span class="sxs-lookup"><span data-stu-id="2082d-111">When a resource requirement is derived from the project task assignments, Project Operations uses the effort contours of the resources assignment to build the contours of the resource requirement details.</span></span> <span data-ttu-id="2082d-112">Однако ссылка на назначения ресурсов не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="2082d-112">However, a refence to the resource assignments isn't maintained.</span></span> <span data-ttu-id="2082d-113">Обновления для резервирований, наследуемых из требований к ресурсам, не обновляют назначения ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2082d-113">Updates to the bookings derived from the resource requirement don't update any resource assignments.</span></span>

<span data-ttu-id="2082d-114">Обычно сумма резервирований для ресурса равна сумме назначений ресурса по одной или нескольким задачам.</span><span class="sxs-lookup"><span data-stu-id="2082d-114">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="2082d-115">Однако Project Operations не задает такое согласование принудительно.</span><span class="sxs-lookup"><span data-stu-id="2082d-115">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="2082d-116">Представление **Выверка** показывает руководителю проекта места, в которых резервирования и назначения ресурсов не согласованы.</span><span class="sxs-lookup"><span data-stu-id="2082d-116">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]