---
title: Резервирования и назначения
description: Этот тема предоставляет информацию о различиях между резервированием ресурсов и назначением ресурсов.
author: ruhercul
manager: Annbe
ms.date: 01/08/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3aaf8dcbae0a5762879c2b1223eba3bdc33af1a7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279919"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="1ee51-103">Резервирования и назначения</span><span class="sxs-lookup"><span data-stu-id="1ee51-103">Bookings vs assignments</span></span>

<span data-ttu-id="1ee51-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="1ee51-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1ee51-105">Резервирования — это окончательное или предварительное назначение ресурсов проекту.</span><span class="sxs-lookup"><span data-stu-id="1ee51-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="1ee51-106">Окончательные резервирования потребляет производительность ресурса.</span><span class="sxs-lookup"><span data-stu-id="1ee51-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="1ee51-107">Резервирования представляют собой организационные концепции для рабочих групп, чтобы они могли понять, как ресурсы будут задействованы в различных проектах.</span><span class="sxs-lookup"><span data-stu-id="1ee51-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="1ee51-108">Dynamics 365 Project Operations рассматривает резервирования как концепцию уровня проекта.</span><span class="sxs-lookup"><span data-stu-id="1ee51-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="1ee51-109">В отличие от резервирований, назначения — это назначение ресурсов задачам проекта в расписании проекта.</span><span class="sxs-lookup"><span data-stu-id="1ee51-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="1ee51-110">Ресурсы могут быть именованными или универсальными.</span><span class="sxs-lookup"><span data-stu-id="1ee51-110">The resources can be named or generic.</span></span>  <span data-ttu-id="1ee51-111">Когда потребность в ресурсах наследуется из назначений задач проекта, Project Operations использует профили трудозатрат по назначению ресурсов для построения профилей сведений требования ресурса.</span><span class="sxs-lookup"><span data-stu-id="1ee51-111">When a resource requirement is derived from the project task assignments, Project Operations uses the effort contours of the resources assignment to build the contours of the resource requirement details.</span></span> <span data-ttu-id="1ee51-112">Однако ссылка на назначения ресурсов не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1ee51-112">However, a refence to the resource assignments isn't maintained.</span></span> <span data-ttu-id="1ee51-113">Обновления для резервирований, наследуемых из требований к ресурсам, не обновляют назначения ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1ee51-113">Updates to the bookings derived from the resource requirement don't update any resource assignments.</span></span>

<span data-ttu-id="1ee51-114">Обычно сумма резервирований для ресурса равна сумме назначений ресурса по одной или нескольким задачам.</span><span class="sxs-lookup"><span data-stu-id="1ee51-114">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="1ee51-115">Однако Project Operations не задает такое согласование принудительно.</span><span class="sxs-lookup"><span data-stu-id="1ee51-115">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="1ee51-116">Представление **Выверка** показывает руководителю проекта места, в которых резервирования и назначения ресурсов не согласованы.</span><span class="sxs-lookup"><span data-stu-id="1ee51-116">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]