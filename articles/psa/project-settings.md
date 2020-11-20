---
title: Параметры проекта
description: В этом разделе представлена информация о параметрах управления проектом.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: b2cda6bfd7f152ee948cf49fab91aed475968a09
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123124"
---
# <a name="project-settings"></a><span data-ttu-id="45cf1-103">Параметры проекта</span><span class="sxs-lookup"><span data-stu-id="45cf1-103">Project settings</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="45cf1-104">Используйте следующие параметры для получения доступа к функциям планирования проекта.</span><span class="sxs-lookup"><span data-stu-id="45cf1-104">Use the following settings to access the project planning features.</span></span>

## <a name="work-template"></a><span data-ttu-id="45cf1-105">Рабочий шаблон</span><span class="sxs-lookup"><span data-stu-id="45cf1-105">Work template</span></span>

<span data-ttu-id="45cf1-106">Чтобы создать календарь проекта, вы создаете шаблон календаря проекта, который определяет количество рабочих часов в день и любые нерабочие дни.</span><span class="sxs-lookup"><span data-stu-id="45cf1-106">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="45cf1-107">Для создания шаблона календаря проекта вы связываете шаблон работы с полем **Шаблон календаря** для проекта.</span><span class="sxs-lookup"><span data-stu-id="45cf1-107">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="45cf1-108">Выполните следующие действия, чтобы создать шаблон работы.</span><span class="sxs-lookup"><span data-stu-id="45cf1-108">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="45cf1-109">В PSA в левой панели навигации щелкните **Ресурсы**.</span><span class="sxs-lookup"><span data-stu-id="45cf1-109">In PSA, in the left navigation pane, click **Resources**.</span></span> 
2. <span data-ttu-id="45cf1-110">На странице списка **Ресурсы** откройте запись пользователя, затем выберите **Показать рабочие часы**.</span><span class="sxs-lookup"><span data-stu-id="45cf1-110">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="45cf1-111">Убедитесь, что на странице браузера разрешены всплывающие окна.</span><span class="sxs-lookup"><span data-stu-id="45cf1-111">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="45cf1-112">Это позволяет видеть рабочие часы, заданные для ресурса.</span><span class="sxs-lookup"><span data-stu-id="45cf1-112">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="45cf1-113">На вкладке **Месячное представление** щелкните **Установить**.</span><span class="sxs-lookup"><span data-stu-id="45cf1-113">On the **Monthly View** tab, click **Set Up**.</span></span> <span data-ttu-id="45cf1-114">Появится список с тремя параметрами:</span><span class="sxs-lookup"><span data-stu-id="45cf1-114">A list of three options appears:</span></span> 

  - <span data-ttu-id="45cf1-115">Новое недельное расписание</span><span class="sxs-lookup"><span data-stu-id="45cf1-115">New Weekly Schedule</span></span>
  - <span data-ttu-id="45cf1-116">Расписание работы на один день</span><span class="sxs-lookup"><span data-stu-id="45cf1-116">Work Schedule for One Day</span></span>
  - <span data-ttu-id="45cf1-117">Нерабочие часы</span><span class="sxs-lookup"><span data-stu-id="45cf1-117">Time Off</span></span>

> ![Настройка параметров](media/project-13.png)

4. <span data-ttu-id="45cf1-119">Выберите **Новое недельное расписание**, затем задайте параметры для этого расписания ресурсов.</span><span class="sxs-lookup"><span data-stu-id="45cf1-119">Select **New Weekly Schedule**, and then set the options for this resource schedule.</span></span> <span data-ttu-id="45cf1-120">Можно задать периодическое недельное расписание, ежедневные параметры часов, нерабочие дни и т. д.</span><span class="sxs-lookup"><span data-stu-id="45cf1-120">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="45cf1-121">Укажите диапазон дат, выберите **Сохранить**, затем щелкните **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="45cf1-121">Set the date range, select **Save**, and then click **Close**.</span></span> 
6. <span data-ttu-id="45cf1-122">Вернитесь на страницу списка **Ресурсы** и выберите ресурс, для которого вы задаете рабочие часы.</span><span class="sxs-lookup"><span data-stu-id="45cf1-122">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="45cf1-123">Выберите **Задать календарь как**, чтобы задать шаблон работы.</span><span class="sxs-lookup"><span data-stu-id="45cf1-123">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="45cf1-124">В диалоговом окне **Рабочий шаблон** введите имя рабочего шаблона, затем выберите **Применить**.</span><span class="sxs-lookup"><span data-stu-id="45cf1-124">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="45cf1-125">Теперь можно связать рабочий шаблон с шаблоном календаря проекта.</span><span class="sxs-lookup"><span data-stu-id="45cf1-125">You can now associate the work template with a project calendar template.</span></span>

## <a name="resource-roles"></a><span data-ttu-id="45cf1-126">Роли ресурсов</span><span class="sxs-lookup"><span data-stu-id="45cf1-126">Resource roles</span></span>

<span data-ttu-id="45cf1-127">Термин *роль ресурса* обозначает набор навыков, компетенций и сертификаций, которыми должен обладать пользователь, чтобы выполнять определенный набор задач по проекту.</span><span class="sxs-lookup"><span data-stu-id="45cf1-127">The term *resource role* refers to the set of skills, competencies, and certifications that a person must have to perform a specific set of tasks on a project.</span></span> <span data-ttu-id="45cf1-128">PSA позволяет задавать стоимость и выставлять счета за время ресурса на основе роли, с которой этот ресурс связан.</span><span class="sxs-lookup"><span data-stu-id="45cf1-128">PSA lets you cost and bill a resource's time based on the role that the resource is associated with.</span></span> <span data-ttu-id="45cf1-129">В каждой организации необходимо настроить эти роли с помощью левой области переходов в меню **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="45cf1-129">Every organization must set up these roles by using the left navigation on the **Project Service** menu.</span></span>

<span data-ttu-id="45cf1-130">В каждой организации необходимо настроить эти роли на странице **Активные категории ресурсов**.</span><span class="sxs-lookup"><span data-stu-id="45cf1-130">Every organization must set up these roles on the **Active Resource Categories** page.</span></span> <span data-ttu-id="45cf1-131">Чтобы открыть эту страницу, в левой области навигации выберите **Роли ресурса**.</span><span class="sxs-lookup"><span data-stu-id="45cf1-131">To open this page, in the left navigation pane, select **Resource Roles**.</span></span>

## <a name="price-lists"></a><span data-ttu-id="45cf1-132">Прайс-листы</span><span class="sxs-lookup"><span data-stu-id="45cf1-132">Price lists</span></span>

<span data-ttu-id="45cf1-133">Прайс-листы позволяют задавать себестоимость и цены продажи для ролей ресурсов, категории расходов, продукты и другие элементы в организации.</span><span class="sxs-lookup"><span data-stu-id="45cf1-133">Price lists let you set cost and sales prices for resource roles, expense categories, products, and other elements in an organization.</span></span> <span data-ttu-id="45cf1-134">Прежде чем задать финансовые оценки для работы, которую необходимо выполнить по проекту, следует создать базовый прайс-лист себестоимости и продаж.</span><span class="sxs-lookup"><span data-stu-id="45cf1-134">Before you set financial estimates for the work that must be delivered for a project, you should create a backing cost and sales price list.</span></span> <span data-ttu-id="45cf1-135">В разделе параметров необходимо также настроить прайс-лист стоимости и продаж по умолчанию, который применяется ко всем проектам, созданным в организации.</span><span class="sxs-lookup"><span data-stu-id="45cf1-135">In the parameters section, you should also set up a default cost and sales price list that applies to all projects that are created in the organization.</span></span> <span data-ttu-id="45cf1-136">На странице **Активные параметры проекта** убедитесь, что настроен прайс-лист стоимости и продаж по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="45cf1-136">On the **Active Project Parameters** page, make sure that you set up a default cost and sales price list.</span></span>
