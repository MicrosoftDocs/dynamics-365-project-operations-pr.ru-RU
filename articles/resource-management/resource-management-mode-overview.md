---
title: Обзор режимов управления ресурсами
description: В этом разделе представлена информация о функции управления ресурсами в Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 872f4f2878f474e16674932f23fe192c6a8de6eb
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279469"
---
# <a name="resource-management-modes-overview"></a><span data-ttu-id="7c807-103">Обзор режимов управления ресурсами</span><span class="sxs-lookup"><span data-stu-id="7c807-103">Resource management modes overview</span></span>

<span data-ttu-id="7c807-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="7c807-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="7c807-105">Dynamics 365 Project Operations поддерживает два режима для выполнения всего процесса бронирования.</span><span class="sxs-lookup"><span data-stu-id="7c807-105">Dynamics 365 Project Operations supports two modes in order for you to execute the overall booking flow.</span></span> <span data-ttu-id="7c807-106">Режим управления определяется как параметр проекта и может быть изменен, если требуется изменение вашего бизнеса.</span><span class="sxs-lookup"><span data-stu-id="7c807-106">The mode of management is defined as a project parameter and can be modified if your business needs change.</span></span>    

## <a name="central-mode"></a><span data-ttu-id="7c807-107">Центральный режим</span><span class="sxs-lookup"><span data-stu-id="7c807-107">Central mode</span></span>
<span data-ttu-id="7c807-108">Для организаций, которые централизуют распределение ресурсов по проектам, центральный режим предоставляет способ гарантировать, что менеджеры проектов могут определять требования ресурсов на уровне проекта.</span><span class="sxs-lookup"><span data-stu-id="7c807-108">For organizations who centralize the allocation for resources to projects, the Central mode provides a way to ensure Project managers can define resource requirements at the project level.</span></span> <span data-ttu-id="7c807-109">Выполнение требований ресурсов делегируется менеджеру ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7c807-109">Fulfillment of the resource requirements is delegated to a Resource manager.</span></span> <span data-ttu-id="7c807-110">Менеджеры проектов могут принять или отклонить ресурсы, предложенные менеджером ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7c807-110">Project managers can accept or reject resources that are proposed by the Resource manager.</span></span>

![Центральный режим](./media/resource-management-central.png)

<span data-ttu-id="7c807-112">Чтобы управлять ресурсами в центральном режиме, см.:</span><span class="sxs-lookup"><span data-stu-id="7c807-112">To manage resources with the Central mode, see:</span></span>

- [<span data-ttu-id="7c807-113">Назначение универсальных резервируемых ресурсов задаче и создание требований ресурсов</span><span class="sxs-lookup"><span data-stu-id="7c807-113">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="7c807-114">Резервирование именованных ресурсов из требований ресурсов</span><span class="sxs-lookup"><span data-stu-id="7c807-114">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [<span data-ttu-id="7c807-115">Отправка запроса ресурса</span><span class="sxs-lookup"><span data-stu-id="7c807-115">Submit a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [<span data-ttu-id="7c807-116">Выполнение запросов ресурсов</span><span class="sxs-lookup"><span data-stu-id="7c807-116">Fulfill a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [<span data-ttu-id="7c807-117">Подтверждение или отклонение предложенного ресурса проекта из запроса ресурса</span><span class="sxs-lookup"><span data-stu-id="7c807-117">Accept or reject a proposed project resource from a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a><span data-ttu-id="7c807-118">Гибридный режим</span><span class="sxs-lookup"><span data-stu-id="7c807-118">Hybrid mode</span></span>
<span data-ttu-id="7c807-119">Для организаций, которым требуется гибкость в распределении ресурсов, гибридный режим позволяет менеджерам проектов и менеджерам ресурсов возможность резервировать ресурсы.</span><span class="sxs-lookup"><span data-stu-id="7c807-119">For organizations who require flexibility in the allocation of resources, the hybrid mode enables both Project managers and Resource managers the ability to book resources.</span></span>

![Гибридный режим](./media/resource-management-hybrid.png)

<span data-ttu-id="7c807-121">В дополнение к поддерживаемому процессу централизованного режима см. следующие темы, чтобы управлять всеми другими поддерживаемыми потоками резервирования в гибридном режиме:</span><span class="sxs-lookup"><span data-stu-id="7c807-121">In addition to the supported Central mode process, see the following topics to manage all other supported booking flows in the Hybrid mode:</span></span>

<span data-ttu-id="7c807-122">Резервирование ресурса напрямую для проекта:</span><span class="sxs-lookup"><span data-stu-id="7c807-122">Book a resource directly to a project:</span></span>
- [<span data-ttu-id="7c807-123">Резервирование резервируемых ресурсов для проектной группы и назначение задач</span><span class="sxs-lookup"><span data-stu-id="7c807-123">Book named bookable resources to a project team and assign tasks</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

<span data-ttu-id="7c807-124">Резервирование ресурса из требования ресурсов:</span><span class="sxs-lookup"><span data-stu-id="7c807-124">Book a resource from a resource requirement:</span></span>
- [<span data-ttu-id="7c807-125">Назначение универсальных резервируемых ресурсов задаче и создание требований ресурсов</span><span class="sxs-lookup"><span data-stu-id="7c807-125">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="7c807-126">Резервирование именованных ресурсов из требований ресурсов</span><span class="sxs-lookup"><span data-stu-id="7c807-126">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]