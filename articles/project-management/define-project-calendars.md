---
title: Определение календарей проекта
description: В этом разделе представлена информация о том, как применить шаблон календаря к проекту для отслеживания расписания проекта.
author: ruhercul
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 0d1a2c4bd2d4022bbf79afcef79170eb482e6418
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999012"
---
# <a name="define-project-calendars"></a><span data-ttu-id="8b275-103">Определение календарей проекта</span><span class="sxs-lookup"><span data-stu-id="8b275-103">Define project calendars</span></span>

<span data-ttu-id="8b275-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="8b275-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8b275-105">Чтобы создать проект и управлять им, вы должны применить к проекту шаблон календаря.</span><span class="sxs-lookup"><span data-stu-id="8b275-105">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="8b275-106">Шаблон календаря определяет следующие атрибуты проекта:</span><span class="sxs-lookup"><span data-stu-id="8b275-106">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="8b275-107">Часы работы, включая время начала и окончания</span><span class="sxs-lookup"><span data-stu-id="8b275-107">Working hours, including start and end time</span></span>
- <span data-ttu-id="8b275-108">Рабочие дни</span><span class="sxs-lookup"><span data-stu-id="8b275-108">Working days</span></span>
- <span data-ttu-id="8b275-109">Исключения календаря, такие как нерабочие дни.</span><span class="sxs-lookup"><span data-stu-id="8b275-109">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="8b275-110">Шаблон календаря, применяемый к проекту, является копией шаблона календаря, определенного в настройках вашей организации.</span><span class="sxs-lookup"><span data-stu-id="8b275-110">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="8b275-111">Если вы измените шаблон календаря, эти изменения не распространятся на рабочие часы проекта.</span><span class="sxs-lookup"><span data-stu-id="8b275-111">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="8b275-112">Чтобы изменить рабочие часы проекта, необходимо применить новый шаблон.</span><span class="sxs-lookup"><span data-stu-id="8b275-112">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="8b275-113">Чтобы создать шаблон календаря для вашей организации, есть два ключевых требования:</span><span class="sxs-lookup"><span data-stu-id="8b275-113">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="8b275-114">Определите желаемые рабочие часы шаблона, используя новый или существующий резервируемый ресурс.</span><span class="sxs-lookup"><span data-stu-id="8b275-114">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="8b275-115">Создайте новый шаблон календаря и свяжите его с резервируемым ресурсом.</span><span class="sxs-lookup"><span data-stu-id="8b275-115">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="8b275-116">**Определите рабочие часы шаблона**</span><span class="sxs-lookup"><span data-stu-id="8b275-116">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="8b275-117">Выберите **Ресурсы** \> **Ресурсы**.</span><span class="sxs-lookup"><span data-stu-id="8b275-117">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="8b275-118">Создайте новый ресурс для ссылки в шаблоне календаря или выберите существующий ресурс.</span><span class="sxs-lookup"><span data-stu-id="8b275-118">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="8b275-119">Выберите вкладку **Часы работы** ресурса и следуйте инструкциям в [Задание рабочих часов для ресурса](/dynamics365/field-service/set-work-hours-resource.md) для настройки правил календаря.</span><span class="sxs-lookup"><span data-stu-id="8b275-119">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](/dynamics365/field-service/set-work-hours-resource.md) to configure the calendar rules.</span></span>

<span data-ttu-id="8b275-120">**Создание нового шаблона календаря**</span><span class="sxs-lookup"><span data-stu-id="8b275-120">**Create a new calendar template**</span></span>

1. <span data-ttu-id="8b275-121">Перейдите к **Параметры** \> **Шаблон календаря**.</span><span class="sxs-lookup"><span data-stu-id="8b275-121">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="8b275-122">Выберите **Создать** и введите имя, описание и шаблон ресурса.</span><span class="sxs-lookup"><span data-stu-id="8b275-122">Select **New**, and enter a name, description, and template resource.</span></span>

> [!NOTE]
> <span data-ttu-id="8b275-123">Когда ресурс упоминается в шаблоне календаря, копия календаря ресурса связывается с шаблоном календаря.</span><span class="sxs-lookup"><span data-stu-id="8b275-123">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="8b275-124">Если рабочие часы скопированного шаблона изменятся, эти изменения не распространятся на шаблон календаря.</span><span class="sxs-lookup"><span data-stu-id="8b275-124">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>

<span data-ttu-id="8b275-125">Теперь можно связать рабочий шаблон с шаблоном календаря проекта.</span><span class="sxs-lookup"><span data-stu-id="8b275-125">You can now associate the work template with a project calendar template.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]

