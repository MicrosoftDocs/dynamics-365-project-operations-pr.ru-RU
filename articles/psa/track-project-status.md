---
title: Отслеживание состояния проекта
description: Порядок отслеживания состояния проекта в Project Service
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
ms.openlocfilehash: 2385f7e52f3b5051b76daa9169f98bd73487e22d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014402"
---
# <a name="track-a-projects-status-project-service"></a><span data-ttu-id="f3e9c-103">Отслеживание состояния проекта (Project Service)</span><span class="sxs-lookup"><span data-stu-id="f3e9c-103">Track a project’s status (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="f3e9c-104">Используйте [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] для отслеживания хода выполнения проекта клиента.</span><span class="sxs-lookup"><span data-stu-id="f3e9c-104">Use the [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] to track the progress of a client’s project.</span></span>  

<span data-ttu-id="f3e9c-105">По мере выполнения проекта его стадии обновляются для отражения стадии реализации:</span><span class="sxs-lookup"><span data-stu-id="f3e9c-105">As the engagement progresses, the project stages update to reflect the stage of the engagement:</span></span>  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   <span data-ttu-id="f3e9c-106">**Создать**</span><span class="sxs-lookup"><span data-stu-id="f3e9c-106">**New**</span></span>    | <span data-ttu-id="f3e9c-107">При создании проекта стадия задается как **Создать**.</span><span class="sxs-lookup"><span data-stu-id="f3e9c-107">When you create a project, the stage is set to **New**.</span></span> <span data-ttu-id="f3e9c-108">Если проект создан из шаблона, то на этой стадии проект может иметь расписание, оценки и данные групп.</span><span class="sxs-lookup"><span data-stu-id="f3e9c-108">If you created the project from a template, at this stage the project may have a schedule, estimates, and team data.</span></span> <span data-ttu-id="f3e9c-109">В противном случае это будет макетом проекта и необходимо вручную ввести оставшиеся компоненты проекта.</span><span class="sxs-lookup"><span data-stu-id="f3e9c-109">Otherwise, it will be the outline of the project and you need to manually enter the rest of the project components.</span></span> |
|  <span data-ttu-id="f3e9c-110">**Предложение с расценками**</span><span class="sxs-lookup"><span data-stu-id="f3e9c-110">**Quote**</span></span>   |      <span data-ttu-id="f3e9c-111">При связывании проекта с предложением с расценками или его создании из предложения стадия проекта задана как **Предложение с расценками**, и также обновляются расчетные даты начала и окончания.</span><span class="sxs-lookup"><span data-stu-id="f3e9c-111">When you associate a project to a quote or create it from a quote, the project stage is set to **Quote**, and the estimated start and end datesare updated as well.</span></span> <span data-ttu-id="f3e9c-112">Когда проект находится на стадии предложения с расценками, сведения по предложению отображаются на вкладке **Продажи** на странице **Проект**.</span><span class="sxs-lookup"><span data-stu-id="f3e9c-112">When the project is in the quote stage, details on the quote display on the **Sales** tab on the **Project** page.</span></span>      |
|   <span data-ttu-id="f3e9c-113">**План**</span><span class="sxs-lookup"><span data-stu-id="f3e9c-113">**Plan**</span></span>   |                                     <span data-ttu-id="f3e9c-114">При выигрыше предложения с расценками, связанного с проектом, а также когда работы переходят на стадию контракта, стадия проект обновляется на **План**.</span><span class="sxs-lookup"><span data-stu-id="f3e9c-114">When you win a quote associated with a project, and when the engagement progresses to the contract stage, the project stage updates to **Plan**.</span></span> <span data-ttu-id="f3e9c-115">Сведения о контракте отображаются на вкладке **Продажи** на странице **Проект**.</span><span class="sxs-lookup"><span data-stu-id="f3e9c-115">Contract details display on the **Sales** tab on the **Project** page.</span></span>                                      |
| <span data-ttu-id="f3e9c-116">**Завершен**</span><span class="sxs-lookup"><span data-stu-id="f3e9c-116">**Complete**</span></span> |                    <span data-ttu-id="f3e9c-117">Когда работа над проектом завершена, можно переместить стадию на **Завершено**.</span><span class="sxs-lookup"><span data-stu-id="f3e9c-117">When the project work is complete, you can flip the stage to **Complete**.</span></span> <span data-ttu-id="f3e9c-118">Когда стадия проекта указана как "завершено", считается, что работа выполнена на 100%, но проект оставлен открытым для времени ожидания или внесения записей о расходах.</span><span class="sxs-lookup"><span data-stu-id="f3e9c-118">When the project stage is set to complete, it’s understood that the work is 100% complete but the project is kept open for any pending time or expense entries to be recorded.</span></span>                     |
|  <span data-ttu-id="f3e9c-119">**Закрыть**</span><span class="sxs-lookup"><span data-stu-id="f3e9c-119">**Close**</span></span>   |           <span data-ttu-id="f3e9c-120">Когда все транзакции записанных по проекту и регистрация данных не планируется, можно вручную задать стадию как **Закрыто**.</span><span class="sxs-lookup"><span data-stu-id="f3e9c-120">When all transactions have been recorded on the project and you don't expect any more to be logged, you can manually set the stage to **Close**.</span></span> <span data-ttu-id="f3e9c-121">Исполнения проект задан как **Закрыто**, регистрация транзакций по проекту невозможна и проекта доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="f3e9c-121">When the project is set to **Close**, you can’t log any more transactions on the project and the project will be read only.</span></span>           |

## <a name="to-track-a-projects-status"></a><span data-ttu-id="f3e9c-122">Отслеживание состояния проекта</span><span class="sxs-lookup"><span data-stu-id="f3e9c-122">To track a project’s status</span></span>  

1.  <span data-ttu-id="f3e9c-123">Перейдите к разделу **Project Service > Проекты**.</span><span class="sxs-lookup"><span data-stu-id="f3e9c-123">Go to **Project Service > Projects**.</span></span>  

2.  <span data-ttu-id="f3e9c-124">Щелкните проект, над которым вы хотите работать.</span><span class="sxs-lookup"><span data-stu-id="f3e9c-124">Click the project you want to work on.</span></span>  

3.  <span data-ttu-id="f3e9c-125">В строке в верхней части экрана щелкните стрелку вниз рядом с именем проекта и щелкните **Отслеживание проекта**.</span><span class="sxs-lookup"><span data-stu-id="f3e9c-125">In the bar across the top of the screen, select the down arrow next to the project name, and then click **Project Tracking**.</span></span>  

4.  <span data-ttu-id="f3e9c-126">Выберите **Отслеживание усилий** или **Отслеживание стоимости** в раскрывающемся списке над списком задач.</span><span class="sxs-lookup"><span data-stu-id="f3e9c-126">Select **Effort Tracking** or **Cost Tracking** in the drop-down list above the task list.</span></span>  

5.  <span data-ttu-id="f3e9c-127">Дважды щелкните любую задачу, чтобы изменить ее.</span><span class="sxs-lookup"><span data-stu-id="f3e9c-127">Double-click any task to edit it.</span></span> <span data-ttu-id="f3e9c-128">Также можно переместить или изменить размер областей в диаграмме Ганта для изменения времени и хода выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="f3e9c-128">You can also move or resize the bars in the Gantt chart to change the time and progress for a task.</span></span>  

### <a name="see-also"></a><span data-ttu-id="f3e9c-129">См. также</span><span class="sxs-lookup"><span data-stu-id="f3e9c-129">See Also</span></span>  
 [<span data-ttu-id="f3e9c-130">Руководство менеджера по проектам</span><span class="sxs-lookup"><span data-stu-id="f3e9c-130">Project Manager Guide</span></span>](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]