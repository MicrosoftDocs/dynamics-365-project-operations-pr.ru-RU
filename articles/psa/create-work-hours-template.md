---
title: Создание шаблона рабочих часов
description: Как создать шаблон рабочих часов в Project Service
author: ruhercul
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
ms.openlocfilehash: a0fce327587940e557e0214c8c0897116ac91901
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4133069"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="a6a82-103">Создание шаблона рабочих часов (Project Service)</span><span class="sxs-lookup"><span data-stu-id="a6a82-103">Create a work hours template (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="a6a82-104">Прежде чем можно создавать расписания проекта, необходимо настроить календарь проекта, который задает число рабочих часов для размещения в день в расписании, а также для всех прочих нерабочих дней.</span><span class="sxs-lookup"><span data-stu-id="a6a82-104">Before you can create project schedules, you need to set up a project calendar that defines the number of working hours to accommodate per day in the schedule and any business closures.</span></span> <span data-ttu-id="a6a82-105">Это делается с шаблоном рабочих часов, содержащим сведения о рабочих часах в день, выходных и любых других нерабочих дней.</span><span class="sxs-lookup"><span data-stu-id="a6a82-105">You do this with a work hours template, which contains details about work hours per day, days off, and any other business closures.</span></span>  
  
 <span data-ttu-id="a6a82-106">При создании проекта можно связывать шаблон работ с календарем проекта для применения расписания для проекта.</span><span class="sxs-lookup"><span data-stu-id="a6a82-106">When you’re creating a project, you associate a work template to the project calendar to apply the schedule for the project.</span></span>  
  
 <span data-ttu-id="a6a82-107">Существует два способа создания шаблона рабочих часов:</span><span class="sxs-lookup"><span data-stu-id="a6a82-107">There are two ways you can create a work hours template:</span></span>  
  
-   <span data-ttu-id="a6a82-108">Создайте шаблон рабочих часов на основе календаря ресурса.</span><span class="sxs-lookup"><span data-stu-id="a6a82-108">Create a work hours template based on a resource’s calendar.</span></span>  
  
-   <span data-ttu-id="a6a82-109">Создайте шаблон рабочих часов.</span><span class="sxs-lookup"><span data-stu-id="a6a82-109">Create a new work hours template.</span></span>  
  
#### <a name="to-create-a-work-hours-template-based-on-a-resources-calendar"></a><span data-ttu-id="a6a82-110">Чтобы создать шаблон рабочих часов на основе календаря ресурса</span><span class="sxs-lookup"><span data-stu-id="a6a82-110">To create a work hours template based on a resource’s calendar</span></span>  
  
1.  <span data-ttu-id="a6a82-111">Перейдите к разделу **Project Service > Ресурсы**.</span><span class="sxs-lookup"><span data-stu-id="a6a82-111">Go to **Project Service > Resources**.</span></span>  
  
2.  <span data-ttu-id="a6a82-112">Выберите ресурс, на основе которого требуется создать рабочие часы.</span><span class="sxs-lookup"><span data-stu-id="a6a82-112">Select the resource you want to base your work hours on.</span></span>  
  
3.  <span data-ttu-id="a6a82-113">Щелкните **Сохранить календарь как**, введите имя шаблона рабочих часов, а затем щелкните **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="a6a82-113">Click **Save Calendar As**, enter a name for the work hours template, and then click **Save**.</span></span>  
  
4.  <span data-ttu-id="a6a82-114">Закончив изменять параметры, щелкните **Сохранить и закрыть**.</span><span class="sxs-lookup"><span data-stu-id="a6a82-114">When you’re done changing options, click **Save and Close**.</span></span>  
  
5.  <span data-ttu-id="a6a82-115">Нажмите кнопку **Сохранить** в правом нижнем углу экрана.</span><span class="sxs-lookup"><span data-stu-id="a6a82-115">Click the **Save** button at the bottom right corner of the screen.</span></span>  
  
#### <a name="to-create-a-new-work-hours-template"></a><span data-ttu-id="a6a82-116">Чтобы создать шаблон рабочих часов</span><span class="sxs-lookup"><span data-stu-id="a6a82-116">To create a new work hours template</span></span>  
  
1.  <span data-ttu-id="a6a82-117">Перейдите к разделу **Project Service > Шаблоны рабочих часов**.</span><span class="sxs-lookup"><span data-stu-id="a6a82-117">Go to **Project Service > Work Hours Templates**.</span></span>  
  
2.  <span data-ttu-id="a6a82-118">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="a6a82-118">Click **New**.</span></span>  
  
3.  <span data-ttu-id="a6a82-119">Введите имя шаблона рабочих часов.</span><span class="sxs-lookup"><span data-stu-id="a6a82-119">Enter a name for the work hours template.</span></span>  
  
4.  <span data-ttu-id="a6a82-120">Выберите ресурс, на котором должны быть основаны рабочие часы, а затем щелкните **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="a6a82-120">Select a resource to base the work hours on, and then click **Save**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="a6a82-121">См. также</span><span class="sxs-lookup"><span data-stu-id="a6a82-121">See Also</span></span>  
 [<span data-ttu-id="a6a82-122">Настройка ресурсов</span><span class="sxs-lookup"><span data-stu-id="a6a82-122">Set up resources</span></span>](../psa/set-up-resources.md)
