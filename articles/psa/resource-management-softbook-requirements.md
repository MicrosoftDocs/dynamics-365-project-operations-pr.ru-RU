---
title: Предварительное резервирование требований
description: В этом разделе представлена информация о том, как предварительно резервировать требования.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: bc58c805bfe1a3087600b8d4a6be2d1bcdd18188
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997932"
---
# <a name="soft-book-requirements"></a><span data-ttu-id="0f713-103">Предварительное резервирование требований</span><span class="sxs-lookup"><span data-stu-id="0f713-103">Soft-book requirements</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="0f713-104">Требование ресурса можно окончательно зарезервировать.</span><span class="sxs-lookup"><span data-stu-id="0f713-104">A resource requirement can be hard-booked.</span></span> <span data-ttu-id="0f713-105">Окончательное резервирование создает предложение, которое потребляет производительность ресурса.</span><span class="sxs-lookup"><span data-stu-id="0f713-105">A hard booking creates a proposal that consumes a resource's capacity.</span></span> <span data-ttu-id="0f713-106">Предложение затем отправляется обратно запрашивающей стороне на утверждение.</span><span class="sxs-lookup"><span data-stu-id="0f713-106">The proposal is then sent back to the requester for approval.</span></span> <span data-ttu-id="0f713-107">Предварительное резервирование предварительно добавляет ресурс в рабочую группу проекта и имеет другое состояние на доске расписания, но оно не потребляет производительность ресурса.</span><span class="sxs-lookup"><span data-stu-id="0f713-107">A soft booking tentatively adds a resource to a project team and has a different status on the Schedule Board, but it doesn't consume the resource's capacity.</span></span> <span data-ttu-id="0f713-108">Ресурс можно предварительно зарезервировать из доски расписания, задав в поле **Состояние резервирования** значение **Предварительно**.</span><span class="sxs-lookup"><span data-stu-id="0f713-108">To soft-book a resource from the Schedule Board, set the **Booking Status** field to **Soft**.</span></span>

![Задано состояние резервирования "Предварительно"](media/Resource-Management-image77.png)

<span data-ttu-id="0f713-110">Когда вкладка **Рабочая группа** находится в представлении **Именованные участники рабочей группы**, ресурс отображается там.</span><span class="sxs-lookup"><span data-stu-id="0f713-110">When the **Team** tab is in the **Named Team Members** view, the resource appears there.</span></span> <span data-ttu-id="0f713-111">Предварительно зарезервированные часы отображаются в столбце **Предварительно зарезервированные часы**.</span><span class="sxs-lookup"><span data-stu-id="0f713-111">The soft-booked hours are reported in the **Soft Booked Hours** column.</span></span>

![Предварительно зарезервированные часы в представлении именованных участников рабочей группы](media/Resource-Management-image78.png)

<span data-ttu-id="0f713-113">Предварительно зарезервированных участников рабочей группы можно назначить задачам.</span><span class="sxs-lookup"><span data-stu-id="0f713-113">Soft-booked team members can be assigned to tasks.</span></span>

![Предварительно зарезервированный участник рабочей группы, назначенный задаче](media/Resource-Management-image79.png)

<span data-ttu-id="0f713-115">На вкладке **Выверка** никакие резервирования для предварительно зарезервированного ресурса не отображаются, поскольку на вкладке **Выверка** учитываются только окончательные резервирования.</span><span class="sxs-lookup"><span data-stu-id="0f713-115">On the **Reconciliation** tab, no bookings are shown for a soft-book resource, because the **Reconciliation** tab considers only hard-bookings.</span></span>

![Предварительно зарезервированный ресурс без резервирований на вкладке "Выверка"](media/Resource-Management-image80.png)

> [!NOTE]
> <span data-ttu-id="0f713-117">Нельзя предварительно зарезервировать ресурс из требования, которое было создано из универсального участника рабочей группы.</span><span class="sxs-lookup"><span data-stu-id="0f713-117">You can't soft-book a resource from a requirement that was generated from a generic team member.</span></span>

<span data-ttu-id="0f713-118">На доске расписания различная расцветка используется для предварительных резервирований ресурса.</span><span class="sxs-lookup"><span data-stu-id="0f713-118">On the Schedule Board, a different coloring is used for soft bookings for a resource.</span></span>

![Предварительные резервирования на доске расписания](media/Resource-Management-image81.png)

<span data-ttu-id="0f713-120">Чтобы преобразовать предварительное резервирование в окончательное резервирование, на доске расписания щелкните правой кнопкой мыши на предварительном резервировании, затем выберите **Изменить состояние** \> **Окончательное резервирование** \> **Окончательно**.</span><span class="sxs-lookup"><span data-stu-id="0f713-120">To convert a soft booking to a hard booking, on the Schedule Board, right-click the soft booking, and then select **Change Status** \> **Hard Book** \> **Hard**.</span></span>

![Изменение состояние резервирования на окончательное](media/Resource-Management-image82.png)

<span data-ttu-id="0f713-122">Резервирование изменено, и его состояние меняется на доске расписания.</span><span class="sxs-lookup"><span data-stu-id="0f713-122">The booking is changed, and the status is changed on the Schedule Board.</span></span> <span data-ttu-id="0f713-123">Поскольку состояние резервирования теперь **Окончательно**, ресурс отображается как зарезервированный, и его производительность и доступность корректируются.</span><span class="sxs-lookup"><span data-stu-id="0f713-123">Because the booking status is now **Hard**, the resource is shown as booked, and its capacity and availability are adjusted.</span></span>

<span data-ttu-id="0f713-124">Можно использовать этот же метод для отмены окончательного резервирования или предварительного резервирования с доски расписания.</span><span class="sxs-lookup"><span data-stu-id="0f713-124">You can use the same method to cancel a hard booking or a soft booking from the Schedule Board.</span></span>

<span data-ttu-id="0f713-125">Чтобы преобразовать ресурс из предварительно зарезервированного в окончательно зарезервированный на вкладке **Рабочая группа** проекта, выберите ресурс, затем выберите **Подтвердить**.</span><span class="sxs-lookup"><span data-stu-id="0f713-125">To convert a resource that is soft-booked to hard-booked on the project's **Team** tab, select the resource, and then select **Confirm**.</span></span>

![Команда подтверждения](media/Resource-Management-image83.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]