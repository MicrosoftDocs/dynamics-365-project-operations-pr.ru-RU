---
title: Определение календарей проекта
description: Эта тема предоставляет информацию об использовании календаря проекта для отслеживания графика проекта.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 774399f2c02d8434c9c042c3a9f995792893bfce
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083362"
---
# <a name="define-project-calendars"></a><span data-ttu-id="17ec0-103">Определение календарей проекта</span><span class="sxs-lookup"><span data-stu-id="17ec0-103">Define project calendars</span></span>

<span data-ttu-id="17ec0-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="17ec0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="17ec0-105">Чтобы создать календарь проекта, вы создаете шаблон календаря проекта, который определяет количество рабочих часов в день и любые нерабочие дни.</span><span class="sxs-lookup"><span data-stu-id="17ec0-105">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="17ec0-106">Для создания шаблона календаря проекта вы связываете шаблон работы с полем **Шаблон календаря** для проекта.</span><span class="sxs-lookup"><span data-stu-id="17ec0-106">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="17ec0-107">Выполните следующие действия, чтобы создать шаблон работы.</span><span class="sxs-lookup"><span data-stu-id="17ec0-107">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="17ec0-108">В левой области переходов выберите **Ресурсы**.</span><span class="sxs-lookup"><span data-stu-id="17ec0-108">In the left navigation pane, select **Resources**.</span></span> 
2. <span data-ttu-id="17ec0-109">На странице списка **Ресурсы** откройте запись пользователя, затем выберите **Показать рабочие часы**.</span><span class="sxs-lookup"><span data-stu-id="17ec0-109">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="17ec0-110">Убедитесь, что на странице браузера разрешены всплывающие окна.</span><span class="sxs-lookup"><span data-stu-id="17ec0-110">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="17ec0-111">Это позволяет видеть рабочие часы, заданные для ресурса.</span><span class="sxs-lookup"><span data-stu-id="17ec0-111">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="17ec0-112">На вкладке **Месячное представление** выберите **Установить**.</span><span class="sxs-lookup"><span data-stu-id="17ec0-112">On the **Monthly View** tab, select **Set Up**.</span></span> <span data-ttu-id="17ec0-113">Появится список с тремя параметрами:</span><span class="sxs-lookup"><span data-stu-id="17ec0-113">A list of three options appears:</span></span> 

  - <span data-ttu-id="17ec0-114">Новое недельное расписание</span><span class="sxs-lookup"><span data-stu-id="17ec0-114">New Weekly Schedule</span></span>
  - <span data-ttu-id="17ec0-115">Расписание работы на один день</span><span class="sxs-lookup"><span data-stu-id="17ec0-115">Work Schedule for One Day</span></span>
  - <span data-ttu-id="17ec0-116">Выходные</span><span class="sxs-lookup"><span data-stu-id="17ec0-116">Time Off</span></span>

4. <span data-ttu-id="17ec0-117">Выберите **Новое недельное расписание** , затем задайте параметры для этого расписания ресурсов.</span><span class="sxs-lookup"><span data-stu-id="17ec0-117">Select **New Weekly Schedule** , and then set the options for this resource schedule.</span></span> <span data-ttu-id="17ec0-118">Можно задать периодическое недельное расписание, ежедневные параметры часов, нерабочие дни и т. д.</span><span class="sxs-lookup"><span data-stu-id="17ec0-118">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="17ec0-119">Укажите диапазон дат, выберите **Сохранить** , затем выберите **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="17ec0-119">Set the date range, select **Save** , and then select **Close**.</span></span> 
6. <span data-ttu-id="17ec0-120">Вернитесь на страницу списка **Ресурсы** и выберите ресурс, для которого вы задаете рабочие часы.</span><span class="sxs-lookup"><span data-stu-id="17ec0-120">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="17ec0-121">Выберите **Задать календарь как** , чтобы задать шаблон работы.</span><span class="sxs-lookup"><span data-stu-id="17ec0-121">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="17ec0-122">В диалоговом окне **Рабочий шаблон** введите имя рабочего шаблона, затем выберите **Применить**.</span><span class="sxs-lookup"><span data-stu-id="17ec0-122">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="17ec0-123">Теперь можно связать рабочий шаблон с шаблоном календаря проекта.</span><span class="sxs-lookup"><span data-stu-id="17ec0-123">You can now associate the work template with a project calendar template.</span></span>
