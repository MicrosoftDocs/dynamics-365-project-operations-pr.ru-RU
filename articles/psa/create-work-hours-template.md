---
title: Создание шаблона рабочих часов
description: В этом разделе описывается, как создать шаблон рабочих часов в Project Service.
author: ruhercul
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
ms.openlocfilehash: 105e3cb2ef7b904e96dc21013906e0b7444e3b88
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997212"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="513d3-103">Создание шаблона рабочих часов (Project Service)</span><span class="sxs-lookup"><span data-stu-id="513d3-103">Create a work hours template (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="513d3-104">Чтобы создать проект и управлять им, вы должны применить к проекту шаблон календаря.</span><span class="sxs-lookup"><span data-stu-id="513d3-104">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="513d3-105">Шаблон календаря определяет следующие атрибуты проекта:</span><span class="sxs-lookup"><span data-stu-id="513d3-105">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="513d3-106">Часы работы, включая время начала и окончания</span><span class="sxs-lookup"><span data-stu-id="513d3-106">Working hours, including start and end time</span></span>
- <span data-ttu-id="513d3-107">Рабочие дни</span><span class="sxs-lookup"><span data-stu-id="513d3-107">Working days</span></span>
- <span data-ttu-id="513d3-108">Исключения календаря, такие как нерабочие дни.</span><span class="sxs-lookup"><span data-stu-id="513d3-108">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="513d3-109">Шаблон календаря, применяемый к проекту, является копией шаблона календаря, определенного в настройках вашей организации.</span><span class="sxs-lookup"><span data-stu-id="513d3-109">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="513d3-110">Если вы измените шаблон календаря, эти изменения не распространятся на рабочие часы проекта.</span><span class="sxs-lookup"><span data-stu-id="513d3-110">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="513d3-111">Чтобы изменить рабочие часы проекта, необходимо применить новый шаблон.</span><span class="sxs-lookup"><span data-stu-id="513d3-111">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="513d3-112">Чтобы создать шаблон календаря для вашей организации, есть два ключевых требования:</span><span class="sxs-lookup"><span data-stu-id="513d3-112">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="513d3-113">Определите желаемые рабочие часы шаблона, используя новый или существующий резервируемый ресурс.</span><span class="sxs-lookup"><span data-stu-id="513d3-113">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="513d3-114">Создайте новый шаблон календаря и свяжите его с резервируемым ресурсом.</span><span class="sxs-lookup"><span data-stu-id="513d3-114">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="513d3-115">**Определите рабочие часы шаблона**</span><span class="sxs-lookup"><span data-stu-id="513d3-115">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="513d3-116">Выберите **Ресурсы** \> **Ресурсы**.</span><span class="sxs-lookup"><span data-stu-id="513d3-116">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="513d3-117">Создайте новый ресурс для ссылки в шаблоне календаря или выберите существующий ресурс.</span><span class="sxs-lookup"><span data-stu-id="513d3-117">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="513d3-118">Выберите вкладку **Часы работы** ресурса и следуйте инструкциям в [Задание рабочих часов для ресурса](/dynamics365/field-service/set-work-hours-resource.md) для настройки правил календаря.</span><span class="sxs-lookup"><span data-stu-id="513d3-118">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](/dynamics365/field-service/set-work-hours-resource.md) to configure the calendar rules.</span></span>

<span data-ttu-id="513d3-119">**Создание нового шаблона календаря**</span><span class="sxs-lookup"><span data-stu-id="513d3-119">**Create a new calendar template**</span></span>

1. <span data-ttu-id="513d3-120">Перейдите к **Параметры** \> **Шаблон календаря**.</span><span class="sxs-lookup"><span data-stu-id="513d3-120">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="513d3-121">Выберите **Создать** и введите имя, описание и шаблон ресурса.</span><span class="sxs-lookup"><span data-stu-id="513d3-121">Select **New**, and enter a name, description, and template resource.</span></span>


> [!NOTE]
> <span data-ttu-id="513d3-122">Когда ресурс упоминается в шаблоне календаря, копия календаря ресурса связывается с шаблоном календаря.</span><span class="sxs-lookup"><span data-stu-id="513d3-122">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="513d3-123">Если рабочие часы скопированного шаблона изменятся, эти изменения не распространятся на шаблон календаря.</span><span class="sxs-lookup"><span data-stu-id="513d3-123">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>


### <a name="see-also"></a><span data-ttu-id="513d3-124">См. также</span><span class="sxs-lookup"><span data-stu-id="513d3-124">See Also</span></span>  
 [<span data-ttu-id="513d3-125">Настройка ресурсов</span><span class="sxs-lookup"><span data-stu-id="513d3-125">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
