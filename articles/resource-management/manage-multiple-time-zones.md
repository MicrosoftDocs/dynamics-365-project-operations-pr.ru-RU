---
title: Управление часовыми поясами
description: Когда проект создается, его часовой пояс основан на часовом поясе, определенном в применяемом шаблоне рабочего времени.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 27f58f0dacc3404119a719547ad374629c740740
ms.sourcegitcommit: 396e0fea2f1598a5313cb0128eca4fe0bb5aade9
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961934"
---
# <a name="manage-time-zones"></a><span data-ttu-id="1672c-103">Управление часовыми поясами</span><span class="sxs-lookup"><span data-stu-id="1672c-103">Manage time zones</span></span>

<span data-ttu-id="1672c-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="1672c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


## <a name="projects"></a><span data-ttu-id="1672c-105">Проекты</span><span class="sxs-lookup"><span data-stu-id="1672c-105">Projects</span></span>

<span data-ttu-id="1672c-106">Когда проект создается, часовой пояс основан на часовом поясе, определенном в примененном шаблоне рабочего времени.</span><span class="sxs-lookup"><span data-stu-id="1672c-106">When a project is created, the time zone is based on the time zone defined in the applied work hour template.</span></span> <span data-ttu-id="1672c-107">В форме **Проект** даты всегда относятся к часовому поясу пользователя, который вошел в систему на каждой вкладке, за исключением вкладки **Задача**. Когда вы просматриваете структурную декомпозицию работ, даты всегда будут отображаться в часовом поясе проекта.</span><span class="sxs-lookup"><span data-stu-id="1672c-107">On the **Project** for, the dates are always relative to the time zone of the user that is logged in on each tab, except the **Task** tab. When you view the work breakdown structure, the dates will always be displayed in the project’s time zone.</span></span>

## <a name="tasks"></a><span data-ttu-id="1672c-108">Задачи</span><span class="sxs-lookup"><span data-stu-id="1672c-108">Tasks</span></span>

<span data-ttu-id="1672c-109">Когда задача создана, время начала, время окончания и часы/день контролируются рабочими часами проекта.</span><span class="sxs-lookup"><span data-stu-id="1672c-109">When a task is created, the start time, end time, and hours/day is controlled by the working hours of the project.</span></span> <span data-ttu-id="1672c-110">Например, если задача создается с проектом, часовой пояс которого -8 PST, и имеет следующие рабочие часы: с 9:00 до 17:00 с понедельника по пятницу, любая задача, созданная без назначения, будет учитывать время начала и время окончания календаря проекта.</span><span class="sxs-lookup"><span data-stu-id="1672c-110">For example, if a task is created with a project whose time zone is -8 PST and has the following working hours: 9:00 AM to 5:00 PM Monday to Friday, any task created without an assignment will respect the start time and end time of the project calendar.</span></span>

## <a name="manage-resources-with-time-zones"></a><span data-ttu-id="1672c-111">Управление ресурсами с помощью часовых поясов</span><span class="sxs-lookup"><span data-stu-id="1672c-111">Manage resources with time zones</span></span>

<span data-ttu-id="1672c-112">Для точных и предсказуемых результатов при использовании функции **Продлить резервирование**, необходимо выполнить два основных условия:</span><span class="sxs-lookup"><span data-stu-id="1672c-112">For accurate and predictable results when using **Extend Booking**, there are two key prerequisites that must be met:</span></span>  

- <span data-ttu-id="1672c-113">Пользователь должен настроить часовой пояс своего устройства в соответствии с часовым поясом, определенным в разделе **Параметры персонализации** системы.</span><span class="sxs-lookup"><span data-stu-id="1672c-113">The user must configure their device's time zone to match the time zone defined in the system's **Personalization Settings**.</span></span>
 
  ![Настройки часового пояса в Windows 10](media/reconcile-assignments-03.png)

  ![Настройки часового пояса в параметрах персонализации](media/reconcile-assignments-04.png)
 
- <span data-ttu-id="1672c-116">Резервируемый ресурс должен иметь как минимум одну минуту рабочего времени, которая перекрывается с контурами, используемыми для определения запрошенного продления.</span><span class="sxs-lookup"><span data-stu-id="1672c-116">The bookable resource must have at least one minute of working time that overlaps with the contours that are used to define the requested extension.</span></span> <span data-ttu-id="1672c-117">Например, следующие ресурсы с рабочим временем, приходящимся на промежуток с 9:00 до 19:00.</span><span class="sxs-lookup"><span data-stu-id="1672c-117">For example, the following resources with working hours that fall between 9:00 AM and 7:00 PM.</span></span> 

  ![Сравнение контуров ресурсов](media/reconcile-assignments-05.png)

<span data-ttu-id="1672c-119">В следующей таблице показаны:</span><span class="sxs-lookup"><span data-stu-id="1672c-119">The following table shows:</span></span>

- <span data-ttu-id="1672c-120">Шаблон календаря проекта</span><span class="sxs-lookup"><span data-stu-id="1672c-120">A project calendar template</span></span>
- <span data-ttu-id="1672c-121">Ресурс A: этот ресурс использует тот же календарь и находится в том же часовом поясе, что и проект.</span><span class="sxs-lookup"><span data-stu-id="1672c-121">Resource A: This resource has the same calendar and is in the same time zone as the project.</span></span> <span data-ttu-id="1672c-122">Временем начала резервирований будет 9:00.</span><span class="sxs-lookup"><span data-stu-id="1672c-122">The start time of the bookings will be 9:00 AM.</span></span>
- <span data-ttu-id="1672c-123">Ресурс B: этот ресурс расположен в другом часовом поясе, чем проект, и начинает работать в 07:00 в своем часовом поясе.</span><span class="sxs-lookup"><span data-stu-id="1672c-123">Resource B: This resource is located in a different time zone than the project and starts at 7:00 AM in their time zone.</span></span> <span data-ttu-id="1672c-124">Однако резервирования будут начинаться в 9:00, так как это самое раннее время начала в контуре назначения.</span><span class="sxs-lookup"><span data-stu-id="1672c-124">However, the bookings will begin at 9:00 AM as that is the earliest start time of the assignment contour.</span></span>
- <span data-ttu-id="1672c-125">Ресурсы C и D: ресурсы расположены в разных часовых поясах, которые отличаются друг от друга и от проекта, и их резервирования начинаются не раньше, чем их соответствующее доступное время начала.</span><span class="sxs-lookup"><span data-stu-id="1672c-125">Resources C and D: The resources are located in different time zones, both different from each other and the project, and their bookings start no earlier than their respective available start times.</span></span>

|<span data-ttu-id="1672c-126">Сущность</span><span class="sxs-lookup"><span data-stu-id="1672c-126">Entity</span></span>  |<span data-ttu-id="1672c-127">Календарь</span><span class="sxs-lookup"><span data-stu-id="1672c-127">Calendar</span></span>  |
|-|-|
|<span data-ttu-id="1672c-128">Шаблон календаря проекта</span><span class="sxs-lookup"><span data-stu-id="1672c-128">Project calendar template</span></span>   | ![календарь проекта](media/reconcile-assignments-06.png) |
|<span data-ttu-id="1672c-130">Ресурс A</span><span class="sxs-lookup"><span data-stu-id="1672c-130">Resource A</span></span>  | ![Календарь ресурса A](media/reconcile-assignments-06.png) |
|<span data-ttu-id="1672c-132">Ресурс B</span><span class="sxs-lookup"><span data-stu-id="1672c-132">Resource B</span></span>  |  ![Календарь ресурса B](media/reconcile-assignments-07.png) |
|<span data-ttu-id="1672c-134">Ресурс C</span><span class="sxs-lookup"><span data-stu-id="1672c-134">Resource C</span></span>  |  ![Календарь ресурса C](media/reconcile-assignments-08.png) |
|<span data-ttu-id="1672c-136">Ресурс D</span><span class="sxs-lookup"><span data-stu-id="1672c-136">Resource D</span></span>  | ![Календарь ресурса D](media/reconcile-assignments-09.png)  |
 
<span data-ttu-id="1672c-138">Когда вы перейдете в представление **Выверка**, отображаются назначения ресурсов и связанные с ними нехватки резервирования.</span><span class="sxs-lookup"><span data-stu-id="1672c-138">When you navigate to the **Reconciliation** view, the resource assignments and the associated booking shortages are displayed.</span></span>

![Представление выверки перед продлением](media/reconcile-assignments-10.png)

<span data-ttu-id="1672c-140">После использования функции расширенного резервирования для каждого ресурса резервирования успешно продлеваются для каждого ресурса, поскольку рабочие часы каждого ресурса совпадают с контурами нехватки.</span><span class="sxs-lookup"><span data-stu-id="1672c-140">After the extend booking functionality has been used for each resource, bookings are successfully extended for each resource because each resource’s working hours overlapped with the contours of the shortage.</span></span>

![Представление выверки после продления резервирования](media/reconcile-assignments-11.png) 

<span data-ttu-id="1672c-142">Обратите внимание, что при более внимательном рассмотрении деталей резервирования можно увидеть разницу во времени начала резервирования.</span><span class="sxs-lookup"><span data-stu-id="1672c-142">Notice that a closer look at the details of the bookings shows differences in the start time of the bookings.</span></span> <span data-ttu-id="1672c-143">Резервирования начинаются не ранее времени начала контура назначения и не ранее доступного времени начала работы ресурса.</span><span class="sxs-lookup"><span data-stu-id="1672c-143">The bookings start no earlier than the start time of the assignment contour and no earlier than the available start time of the resource.</span></span>

![Новые резервирования ресурсов на таблице расписаний](media/reconcile-assignments-12.png)
