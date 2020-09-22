---
title: Планирование ресурсов для проекта
description: Порядок планирования ресурсов для проекта в Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 4935567d-9318-4f7c-9c02-c584a78b7841
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: d9767e324b3caec4b5f9723347537dbe97ea34fb
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755029"
---
# <a name="schedule-resources-for-a-project-project-service"></a><span data-ttu-id="b4c4c-103">Планирование ресурсов для проекта (Project Service)</span><span class="sxs-lookup"><span data-stu-id="b4c4c-103">Schedule resources for a project (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="b4c4c-104">Можно проверить доступность ресурсов, чтобы получить полное представление о том, в какой степени зарезервированы ваши ресурсы, или можно фильтровать представление по навыкам, рабочей группе, расположению и другим параметрам.</span><span class="sxs-lookup"><span data-stu-id="b4c4c-104">You can check resource availability to get an overall view of how booked your resources are, or you can filter the view by skills, team, location, and other options.</span></span>  
  
<span data-ttu-id="b4c4c-105">В таблице расписаний представлен список ресурсов и их доступность.</span><span class="sxs-lookup"><span data-stu-id="b4c4c-105">The schedule board shows list of resources and their availability.</span></span> <span data-ttu-id="b4c4c-106">Выберите режим просмотра для отображения доступности по **часам**, **дню**, **неделе** или **месяцу**.</span><span class="sxs-lookup"><span data-stu-id="b4c4c-106">Select a view mode to show availability by **Hours**, **Day**, **Week**, or **Month**.</span></span>  
  
<span data-ttu-id="b4c4c-107">Прежде чем использовать таблицу расписаний, важно ее настроить.</span><span class="sxs-lookup"><span data-stu-id="b4c4c-107">Before you use the schedule board, it’s important to set it up.</span></span> <span data-ttu-id="b4c4c-108">Дополнительные сведения см. в разделе [Настройка таблицы расписаний (Field Service или Project Service Automation)](../field-service/configure-schedule-board.md).</span><span class="sxs-lookup"><span data-stu-id="b4c4c-108">For more information, see [Configure the schedule board (Field Service or Project Service Automation)](../field-service/configure-schedule-board.md).</span></span>
  
<span data-ttu-id="b4c4c-109">Если вы используете более старую версию, сведения о доступности ресурсов см. в разделе [Просмотр доступности ресурсов](../project-service/view-resource-availability.md).</span><span class="sxs-lookup"><span data-stu-id="b4c4c-109">If you are using an older version, for resource availability, see [View resource availability](../project-service/view-resource-availability.md).</span></span>  

> [!IMPORTANT]
>  <span data-ttu-id="b4c4c-110">Для использования функциональности резервирования таблицы расписаний, геокодирование и службы расположений включите карты.</span><span class="sxs-lookup"><span data-stu-id="b4c4c-110">To use the schedule board booking functionality, geocoding, and location services, you need to turn on maps.</span></span>  
> 
> 1. <span data-ttu-id="b4c4c-111">В главном меню щелкните **Планирование ресурсов** > **Администрирование**.</span><span class="sxs-lookup"><span data-stu-id="b4c4c-111">On the main menu, select **Resource Scheduling** > **Administration**.</span></span>  
> 2. <span data-ttu-id="b4c4c-112">Щелкните **Параметры планирования**.</span><span class="sxs-lookup"><span data-stu-id="b4c4c-112">Click **Scheduling parameters**.</span></span>  
> 3. <span data-ttu-id="b4c4c-113">Откройте запись и прокрутите ее вниз до раздела **Resource Scheduling Optimization**.</span><span class="sxs-lookup"><span data-stu-id="b4c4c-113">Open record and scroll down to the **Resource Scheduling Optimization** section.</span></span>  
> 4. <span data-ttu-id="b4c4c-114">В поле **Подключиться к картам** выберите **Да**.</span><span class="sxs-lookup"><span data-stu-id="b4c4c-114">On the **Connect to Maps** field, choose **Yes**.</span></span>  
> 5. <span data-ttu-id="b4c4c-115">Примите условия и сохраните запись.</span><span class="sxs-lookup"><span data-stu-id="b4c4c-115">Accept terms and save the record.</span></span>  
> 6. <span data-ttu-id="b4c4c-116">В главном меню выберите **Project Service** > **Таблица расписаний**.</span><span class="sxs-lookup"><span data-stu-id="b4c4c-116">On the main menu, select **Project Service** > **Schedule board**.</span></span> <span data-ttu-id="b4c4c-117">Здесь существует несколько способов запланировать требование резервирования вручную.</span><span class="sxs-lookup"><span data-stu-id="b4c4c-117">From here, there are several ways to manually schedule a booking requirement.</span></span> <span data-ttu-id="b4c4c-118">Выберите метод, подходящий для вас.</span><span class="sxs-lookup"><span data-stu-id="b4c4c-118">Choose the method that works for you.</span></span>
  
## <a name="find-available-resources"></a><span data-ttu-id="b4c4c-119">Поиск доступных ресурсов</span><span class="sxs-lookup"><span data-stu-id="b4c4c-119">Find available resources</span></span>

1.  <span data-ttu-id="b4c4c-120">В списке **Требование резервирования** щелкните правой кнопкой мыши незапланированное резервирование и выберите одно из следующего:</span><span class="sxs-lookup"><span data-stu-id="b4c4c-120">From the **Booking Requirement** list, right-click an unscheduled booking and choose one of the following:</span></span>  
  
- <span data-ttu-id="b4c4c-121">Выберите **Поиск доступности — текущие ресурсы**, чтобы найти доступный ресурс в списке в таблице расписаний.</span><span class="sxs-lookup"><span data-stu-id="b4c4c-121">Choose **Find availability - Current Resources** to find an available resource from the list on the schedule board.</span></span>  
- <span data-ttu-id="b4c4c-122">Выберите **Поиск доступности — все ресурсы**, чтобы найти доступный ресурс из ресурсов в системе.</span><span class="sxs-lookup"><span data-stu-id="b4c4c-122">Choose **Find availability - All Resources**, to find an available resource from resources in the system</span></span>  
   > [!NOTE]
   >  <span data-ttu-id="b4c4c-123">При этом фильтры покажут параметры для выбранного требования резервирования.</span><span class="sxs-lookup"><span data-stu-id="b4c4c-123">When you do this, the filters will show options for the selected booking requirement.</span></span>  
  
2. <span data-ttu-id="b4c4c-124">Когда вы увидите доступный период времени, щелкните его правой кнопкой мыши в таблице расписаний и выберите **Резервировать здесь**.</span><span class="sxs-lookup"><span data-stu-id="b4c4c-124">When you see an available slot, right-click the time slot on the schedule board and choose **Book Here**.</span></span> <span data-ttu-id="b4c4c-125">Либо перетащите требование резервирования в доступный период времени.</span><span class="sxs-lookup"><span data-stu-id="b4c4c-125">Or, drag and drop the booking requirement to the available time slot.</span></span>  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a><span data-ttu-id="b4c4c-126">Резервирование ресурса с помощью ежедневного представления и поиск не полностью зарезервированных ресурсов</span><span class="sxs-lookup"><span data-stu-id="b4c4c-126">Book a resource using the daily view and find who’s under-booked</span></span>
  
1.  <span data-ttu-id="b4c4c-127">В таблице расписаний выберите **Режим просмотра** и выберите **Дни**.</span><span class="sxs-lookup"><span data-stu-id="b4c4c-127">On the schedule board, select **View Mode** and select **Days**.</span></span>  
  
    <span data-ttu-id="b4c4c-128">Отобразится представление решетки с количеством часов, в течение которых ресурс зарезервирован в день, и указанием дней, когда он свободен.</span><span class="sxs-lookup"><span data-stu-id="b4c4c-128">This shows a grid view of how many hours a resource is booked per day and which days they are free.</span></span>  
  
2.  <span data-ttu-id="b4c4c-129">Щелкните имя ресурса, которые требуется зарезервировать, и выберите **Зарезервировать**.</span><span class="sxs-lookup"><span data-stu-id="b4c4c-129">Click the name of the resource you want to book, and then select **Book**.</span></span>  
  
3.  <span data-ttu-id="b4c4c-130">В диалоговом окне **Резервирование ресурса (создать)** выберите проект, для которого требуется зарезервировать ресурс, а также метод резервирования и время начала и окончания.</span><span class="sxs-lookup"><span data-stu-id="b4c4c-130">On the **Resource booking (create)** dialog box, choose the project that you want to book the resource for along with booking method and start and end times.</span></span>  
  
4.  <span data-ttu-id="b4c4c-131">По завершении выберите **Зарезервировать**.</span><span class="sxs-lookup"><span data-stu-id="b4c4c-131">When you’re done, select **Book**.</span></span>  
  
## <a name="view-to-the-schedule-board"></a><span data-ttu-id="b4c4c-132">Просмотр таблицы расписаний</span><span class="sxs-lookup"><span data-stu-id="b4c4c-132">View to the schedule board</span></span>
  
1.  <span data-ttu-id="b4c4c-133">Выберите незапланированное требование резервирования из списка внизу.</span><span class="sxs-lookup"><span data-stu-id="b4c4c-133">Select an unscheduled booking requirement from the list at the bottom.</span></span>  
  
2.  <span data-ttu-id="b4c4c-134">Перетащите требование резервирования на доступный ресурс/период времени в таблице расписаний.</span><span class="sxs-lookup"><span data-stu-id="b4c4c-134">Drag the booking requirement to an available resource/time slot on the schedule board.</span></span>  
  
3.  <span data-ttu-id="b4c4c-135">По завершении выберите **Зарезервировать**.</span><span class="sxs-lookup"><span data-stu-id="b4c4c-135">When you're done, select **Book**.</span></span>  
  
### <a name="additional-resources"></a><span data-ttu-id="b4c4c-136">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b4c4c-136">Additional resources</span></span>  
 [<span data-ttu-id="b4c4c-137">Руководство по диспетчеру ресурсов</span><span class="sxs-lookup"><span data-stu-id="b4c4c-137">Resource manager guide</span></span>](../project-service/resource-manager-guide.md)
