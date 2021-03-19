---
title: Руководство по диспетчеру ресурсов
description: Руководство по управлению ресурсами в Project Service
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 4b9df18e7240450f01271b73eb6ea7e215be38c5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282844"
---
# <a name="resource-manager-guide-project-service"></a><span data-ttu-id="48b91-103">Руководство для менеджера по управлению ресурсами (Project Service)</span><span class="sxs-lookup"><span data-stu-id="48b91-103">Resource manager guide (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="48b91-104">Возможности [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] в [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] помогают находить подходящие ресурсы в подходящее время для подходящего проекта и позволяют обеспечить, что все ресурсы используются эффективно.</span><span class="sxs-lookup"><span data-stu-id="48b91-104">The [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] help you find the right resources at the right time for the right project and make sure all resources are utilized efficiently.</span></span>  
  
 <span data-ttu-id="48b91-105">Эффективно размещайте консультантов своей организации с помощью [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="48b91-105">Deploy your company’s consultants efficiently and effectively with the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> <span data-ttu-id="48b91-106">Вам предоставляются средства, необходимые для планирования ресурсов на основе требований и расписаний консультационных проектов и с учетом профессиональных знаний и доступности ваших консультантов.</span><span class="sxs-lookup"><span data-stu-id="48b91-106">These provide you with the tools you need to schedule resources based on the requirements and schedules of consulting projects and on the skills and availability of your consultants.</span></span> <span data-ttu-id="48b91-107">Вы сможете быстро находить наиболее квалифицированных консультантов, доступных для участия в работе над проектами, и сможете легко составлять более оптимальные графики их работы в ходе исполнения каждого проекта.</span><span class="sxs-lookup"><span data-stu-id="48b91-107">You can quickly find the most qualified consultants who are available to work on projects, and you can easily see how to better schedule them during the course of each project.</span></span>  
  
 <span data-ttu-id="48b91-108">Планирование ресурсов поможет вам выполнять следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="48b91-108">Resource scheduling helps you do the following:</span></span>  
  
- <span data-ttu-id="48b91-109">Выбор подходящих ресурсов для проектов на основании того, в какой степени уровни их профессиональных навыков и знаний соответствуют требованиям к ресурсам проекта.</span><span class="sxs-lookup"><span data-stu-id="48b91-109">Match resources to projects, based on how well their skills and proficiency levels match the project resource requirements.</span></span>  
  
- <span data-ttu-id="48b91-110">Согласование расписания ресурса с календарем проекта на основе доступности и запланированной недоступности каждого ресурса.</span><span class="sxs-lookup"><span data-stu-id="48b91-110">Match a resource’s schedule to a project calendar, based on their availability and scheduled time off.</span></span> <span data-ttu-id="48b91-111">Календарь со цветовой кодировкой позволяет визуально оценивать доступность ресурса.</span><span class="sxs-lookup"><span data-stu-id="48b91-111">The color-coded calendar gives you visual cues about resource availability.</span></span>  
  
- <span data-ttu-id="48b91-112">Отображение производительности каждого консультанта и определение степени использования этой производительности в данный момент.</span><span class="sxs-lookup"><span data-stu-id="48b91-112">Review the capacity of each consultant and determine how that capacity is currently used.</span></span> <span data-ttu-id="48b91-113">Это помогает определять случаи, когда консультант недо- или перегружен, и определять, работает ли консультант с установленной производительностью.</span><span class="sxs-lookup"><span data-stu-id="48b91-113">This can help you find where a consultant might be under- or over-utilized, or if they’re working at capacity.</span></span>  
  
- <span data-ttu-id="48b91-114">Назначение части рабочего времени сотрудника (в процентах или в виде конкретного количества часов)определенному проекту.</span><span class="sxs-lookup"><span data-stu-id="48b91-114">Assign a percentage or a specific number of hours for a worker’s capacity to a project.</span></span>  
  
- <span data-ttu-id="48b91-115">Групповое резервирование ресурсов.</span><span class="sxs-lookup"><span data-stu-id="48b91-115">Make group resource bookings.</span></span>  
  
- <span data-ttu-id="48b91-116">Предварительное или окончательное резервирование ресурсов, преобразование предварительно зарезервированных часов в окончательно зарезервированные часы в одно действие.</span><span class="sxs-lookup"><span data-stu-id="48b91-116">Soft book or hard book resources, and convert soft-booked hours into hard-booked hours in one step.</span></span>  
  
- <span data-ttu-id="48b91-117">Автоматическое формирование рабочей группы проекта на основе ресурсов, указанных в структурной декомпозиции работ для проекта.</span><span class="sxs-lookup"><span data-stu-id="48b91-117">Automatically form a project team based on resources defined in a work breakdown structure for a project.</span></span>  
  
- <span data-ttu-id="48b91-118">Выполнение запросов на ресурсы (резервирование, предложение, поиск ресурсов на замену).</span><span class="sxs-lookup"><span data-stu-id="48b91-118">Fulfill resource requests (book, propose, find substitute resources).</span></span>  
  
- <span data-ttu-id="48b91-119">Назначение ресурсов в соответствии с централизованной (назначает руководитель по ресурсам) или гибридной (может назначать не только руководитель по ресурсам, но и другие руководители) моделью.</span><span class="sxs-lookup"><span data-stu-id="48b91-119">Assign resources according to a central (resource manager assigns) or hybrid model (resource manager and other managers can assign).</span></span> <span data-ttu-id="48b91-120">Дополнительные сведения об отличиях в настройке централизованной и гибридной моделей управления ресурсами см. в разделе [Задание настроек дополнительных параметров (Project Service)](../psa/configure-additional-parameters-settings.md).</span><span class="sxs-lookup"><span data-stu-id="48b91-120">For more information about setting a central versus hybrid resource management model, see [Configure additional parameters settings (Project Service)](../psa/configure-additional-parameters-settings.md).</span></span>  
  
  <span data-ttu-id="48b91-121">Вы можете эффективно управлять ресурсами в разных проектах и обеспечивать надлежащую укомплектованность штата проектов.</span><span class="sxs-lookup"><span data-stu-id="48b91-121">You can manage resources efficiently across projects and ensure that projects are staffed appropriately.</span></span> <span data-ttu-id="48b91-122">Вам понадобится выполнять следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="48b91-122">You’ll need to perform the following tasks:</span></span>  
  
- <span data-ttu-id="48b91-123">[Управление запросами на ресурсы](../psa/manage-resource-requests.md).</span><span class="sxs-lookup"><span data-stu-id="48b91-123">[Manage resource requests](../psa/manage-resource-requests.md).</span></span> <span data-ttu-id="48b91-124">Выбирайте консультантов с подходящими навыками и квалификацией для соответствующих проектов.</span><span class="sxs-lookup"><span data-stu-id="48b91-124">Match the skills and proficiencies of your consultants to the right projects.</span></span>  
  
- <span data-ttu-id="48b91-125">[Просмотр доступности ресурсов](../psa/view-resource-availability.md).</span><span class="sxs-lookup"><span data-stu-id="48b91-125">[View resource availability](../psa/view-resource-availability.md).</span></span> <span data-ttu-id="48b91-126">Проверяйте доступность консультантов на представлении календаря.</span><span class="sxs-lookup"><span data-stu-id="48b91-126">Check consultants’ availability in a calendar view.</span></span>  
  
- <span data-ttu-id="48b91-127">[Просмотр использования ресурсов](../psa/view-resource-utilization.md).</span><span class="sxs-lookup"><span data-stu-id="48b91-127">[View resource utilization](../psa/view-resource-utilization.md).</span></span> <span data-ttu-id="48b91-128">Смотрите, на сколько процентов зарезервировано время ваших консультантов в данный момент.</span><span class="sxs-lookup"><span data-stu-id="48b91-128">See the percentage of time that your consultants are currently booked.</span></span>  
  
- <span data-ttu-id="48b91-129">[Планирование ресурсов для проекта](../psa/schedule-resources-project.md).</span><span class="sxs-lookup"><span data-stu-id="48b91-129">[Schedule resources for a project](../psa/schedule-resources-project.md).</span></span> <span data-ttu-id="48b91-130">Запланируйте консультантов для проекта.</span><span class="sxs-lookup"><span data-stu-id="48b91-130">Schedule consultants for a project.</span></span>  
  
  <span data-ttu-id="48b91-131">Дополнительные сведения об отправке запросов на ресурсы для отдельных проектов см. в разделе [Отправка запросов ресурса](../psa/submit-resource-requests.md).</span><span class="sxs-lookup"><span data-stu-id="48b91-131">For more information about submitting resource requests for individual projects, see [Submit resource requests](../psa/submit-resource-requests.md).</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="48b91-132">См. также</span><span class="sxs-lookup"><span data-stu-id="48b91-132">See Also</span></span>  
 <span data-ttu-id="48b91-133">[Обзор Project Service](../psa/overview.md) </span><span class="sxs-lookup"><span data-stu-id="48b91-133">[Overview of Project Service](../psa/overview.md) </span></span>  
 <span data-ttu-id="48b91-134">[Руководство администратора](../psa/admin-guide.md) </span><span class="sxs-lookup"><span data-stu-id="48b91-134">[Administrator Guide](../psa/admin-guide.md) </span></span>  
 <span data-ttu-id="48b91-135">[Руководство для менеджера по работе с клиентами](../psa/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="48b91-135">[Account Manager Guiden](../psa/account-manager-guide.md) </span></span>  
 <span data-ttu-id="48b91-136">[Руководство менеджера по проектам](../psa/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="48b91-136">[Project Manager Guide](../psa/project-manager-guide.md) </span></span>  
 [<span data-ttu-id="48b91-137">Руководство по совместной работе и вводу данных о времени и расходах</span><span class="sxs-lookup"><span data-stu-id="48b91-137">Time, Expense, and Collaboration Guide</span></span>](../psa/time-expense-collaboration-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]