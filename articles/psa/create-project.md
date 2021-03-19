---
title: Создание проекта
description: Как создать проект в Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/13/2020
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
ms.openlocfilehash: 164dff56bb61f6d9bc4cf0b0678a25e0169a31ee
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285094"
---
# <a name="create-a-project-project-service"></a><span data-ttu-id="e2c5a-103">Создание проекта (Project Service)</span><span class="sxs-lookup"><span data-stu-id="e2c5a-103">Create a project (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="e2c5a-104">Создайте проект с помощью возможностей [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] в [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)], когда вам требуется создать возможную сделку, ценовое предложение или контракт для услуг на основе проекта.</span><span class="sxs-lookup"><span data-stu-id="e2c5a-104">Create a project using the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] when you want to create an opportunity, quote, or contract for project-based services.</span></span> <span data-ttu-id="e2c5a-105">Возможности [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] помогают осуществлять управление проектом, от стадии возможной сделки до полного завершения проекта.</span><span class="sxs-lookup"><span data-stu-id="e2c5a-105">The [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities help you manage your project from opportunity through completion.</span></span> <span data-ttu-id="e2c5a-106">Когда вы создаете проект, вы также создаете структурную декомпозицию работ, которая влияет на ваши расценки, сметную стоимость и управление ресурсами.</span><span class="sxs-lookup"><span data-stu-id="e2c5a-106">When you create a project, you’ll also create a work breakdown structure, which affects your quotes, cost estimates, and resource management.</span></span>  
  
1.  <span data-ttu-id="e2c5a-107">Перейдите к разделу **Project Service > Проекты**.</span><span class="sxs-lookup"><span data-stu-id="e2c5a-107">Go to **Project Service > Projects**.</span></span>  
  
2.  <span data-ttu-id="e2c5a-108">Щелкните **Создать проект**.</span><span class="sxs-lookup"><span data-stu-id="e2c5a-108">Click **New Project**.</span></span>  
  
3.  <span data-ttu-id="e2c5a-109">В области **Сводка** введите имя проекта, а затем введите как можно больше других сведений.</span><span class="sxs-lookup"><span data-stu-id="e2c5a-109">In the **Summary** area, enter a name for your project, and then fill in as many of the details as you can.</span></span> <span data-ttu-id="e2c5a-110">Элементы, отмеченные красной звездочкой (\*), обязательны.</span><span class="sxs-lookup"><span data-stu-id="e2c5a-110">Items marked with a red asterisk (\*) are required.</span></span>  
  
4.  <span data-ttu-id="e2c5a-111">Щелкните **Сохранить**, чтобы создать проект и продолжить его редактирование.</span><span class="sxs-lookup"><span data-stu-id="e2c5a-111">Click **Save** to create your project so you can continue editing it.</span></span>  
  
<span data-ttu-id="e2c5a-112">Затем создается структурная декомпозиция работ для проекта, позволяющая определить задачи, сроки и роли ресурсов, необходимые для проекта.</span><span class="sxs-lookup"><span data-stu-id="e2c5a-112">Next, you’ll create a work breakdown structure for your project to define the tasks, timing, and resource roles needed for the project.</span></span>  

> [!NOTE]
> <span data-ttu-id="e2c5a-113">При планировании Project Service Automation учитывает часовой пояс применяемого шаблона **Рабочие часы**.</span><span class="sxs-lookup"><span data-stu-id="e2c5a-113">When scheduling, Project Service Automation respects the time zone of the applied **Work Hour** template.</span></span> <span data-ttu-id="e2c5a-114">Однако при просмотре запланированных задач даты начала и окончания задачи будут отображаться в часовом поясе пользователя.</span><span class="sxs-lookup"><span data-stu-id="e2c5a-114">However, when viewing the schedule tasks, the start and end dates of a task will be displayed in the user's time zone.</span></span> <span data-ttu-id="e2c5a-115">Это относится к другим повременным представлениям в форме **Проект**.</span><span class="sxs-lookup"><span data-stu-id="e2c5a-115">This applies to other time-phased views in the **Project** form.</span></span> <span data-ttu-id="e2c5a-116">Если часовой пояс пользователя не совпадает с часовым поясом шаблона рабочего времени, примененного к проекту, появится предупреждение, объясняющее разницу.</span><span class="sxs-lookup"><span data-stu-id="e2c5a-116">If the user's time zone does not match the time zone of the work hour template applied to the project, a warning which explains the difference will occur.</span></span> 
  
### <a name="see-also"></a><span data-ttu-id="e2c5a-117">См. также</span><span class="sxs-lookup"><span data-stu-id="e2c5a-117">See Also</span></span>  
 [<span data-ttu-id="e2c5a-118">Руководство менеджера по проектам</span><span class="sxs-lookup"><span data-stu-id="e2c5a-118">Project Manager Guide</span></span>](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]