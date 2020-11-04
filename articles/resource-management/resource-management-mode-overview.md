---
title: Обзор режимов управления ресурсами
description: В этой теме предоставлена информация о функциях управления ресурсами в Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4a8e605109e48b50da68abeee989f8ac8d3d659c
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083076"
---
# <a name="resource-management-modes-overview"></a><span data-ttu-id="93112-103">Обзор режимов управления ресурсами</span><span class="sxs-lookup"><span data-stu-id="93112-103">Resource management modes overview</span></span>

<span data-ttu-id="93112-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="93112-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="93112-105">Dynamics 365 Project Operations поддерживает два режима для выполнения всего потока резервирования.</span><span class="sxs-lookup"><span data-stu-id="93112-105">Dynamics 365 Project Operations supports two modes in order for you to execute the overall booking flow.</span></span> <span data-ttu-id="93112-106">Режим управления определяется как параметр проекта и может быть изменен, если требуется изменение вашего бизнеса.</span><span class="sxs-lookup"><span data-stu-id="93112-106">The mode of management is defined as a project parameter and can be modified if your business needs change.</span></span>    

## <a name="central-mode"></a><span data-ttu-id="93112-107">Центральный режим</span><span class="sxs-lookup"><span data-stu-id="93112-107">Central mode</span></span>
<span data-ttu-id="93112-108">Для организаций, которые централизуют распределение ресурсов по проектам, центральный режим предоставляет способ гарантировать, что менеджеры проектов могут определять требования ресурсов на уровне проекта.</span><span class="sxs-lookup"><span data-stu-id="93112-108">For organizations who centralize the allocation for resources to projects, the Central mode provides a way to ensure Project managers can define resource requirements at the project level.</span></span> <span data-ttu-id="93112-109">Выполнение требований ресурсов делегируется менеджеру ресурсов.</span><span class="sxs-lookup"><span data-stu-id="93112-109">Fulfillment of the resource requirements is delegated to a Resource manager.</span></span> <span data-ttu-id="93112-110">Менеджеры проектов могут принять или отклонить ресурсы, предложенные менеджером ресурсов.</span><span class="sxs-lookup"><span data-stu-id="93112-110">Project managers can accept or reject resources that are proposed by the Resource manager.</span></span>

![Центральный режим](./media/resource-management-central.png)

<span data-ttu-id="93112-112">Чтобы управлять ресурсами в центральном режиме, см.:</span><span class="sxs-lookup"><span data-stu-id="93112-112">To manage resources with the Central mode, see:</span></span>

- [<span data-ttu-id="93112-113">Назначение универсальных резервируемых ресурсов задаче и создание требований ресурсов</span><span class="sxs-lookup"><span data-stu-id="93112-113">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="93112-114">Резервирование именованных ресурсов из требований ресурсов</span><span class="sxs-lookup"><span data-stu-id="93112-114">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [<span data-ttu-id="93112-115">Отправка запроса ресурса</span><span class="sxs-lookup"><span data-stu-id="93112-115">Submit a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [<span data-ttu-id="93112-116">Выполнение запросов ресурсов</span><span class="sxs-lookup"><span data-stu-id="93112-116">Fulfill a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [<span data-ttu-id="93112-117">Подтверждение или отклонение предложенного ресурса проекта из запроса ресурса</span><span class="sxs-lookup"><span data-stu-id="93112-117">Accept or reject a proposed project resource from a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a><span data-ttu-id="93112-118">Гибридный режим</span><span class="sxs-lookup"><span data-stu-id="93112-118">Hybrid mode</span></span>
<span data-ttu-id="93112-119">Для организаций, которым требуется гибкость в распределении ресурсов, гибридный режим позволяет менеджерам проектов и менеджерам ресурсов возможность резервировать ресурсы.</span><span class="sxs-lookup"><span data-stu-id="93112-119">For organizations who require flexibility in the allocation of resources, the hybrid mode enables both Project managers and Resource managers the ability to book resources.</span></span>

![Гибридный режим](./media/resource-management-hybrid.png)

<span data-ttu-id="93112-121">В дополнение к поддерживаемому процессу централизованного режима см. следующие темы, чтобы управлять всеми другими поддерживаемыми потоками резервирования в гибридном режиме:</span><span class="sxs-lookup"><span data-stu-id="93112-121">In addition to the supported Central mode process, see the following topics to manage all other supported booking flows in the Hybrid mode:</span></span>

<span data-ttu-id="93112-122">Резервирование ресурса напрямую для проекта:</span><span class="sxs-lookup"><span data-stu-id="93112-122">Book a resource directly to a project:</span></span>
- [<span data-ttu-id="93112-123">Резервирование резервируемых ресурсов для проектной группы и назначение задач</span><span class="sxs-lookup"><span data-stu-id="93112-123">Book named bookable resources to a project team and assign tasks</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

<span data-ttu-id="93112-124">Резервирование ресурса из требования ресурсов:</span><span class="sxs-lookup"><span data-stu-id="93112-124">Book a resource from a resource requirement:</span></span>
- [<span data-ttu-id="93112-125">Назначение универсальных резервируемых ресурсов задаче и создание требований ресурсов</span><span class="sxs-lookup"><span data-stu-id="93112-125">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="93112-126">Резервирование именованных ресурсов из требований ресурсов</span><span class="sxs-lookup"><span data-stu-id="93112-126">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
