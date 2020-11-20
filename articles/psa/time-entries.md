---
title: Создание записей времени
description: В этом разделе представлена информация о том, как создать записи времени.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: d8c87f0fd2cc021bb9088d0fac73ccd52980a905
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131304"
---
# <a name="create-time-entries"></a><span data-ttu-id="6fd94-103">Создание записей времени</span><span class="sxs-lookup"><span data-stu-id="6fd94-103">Create time entries</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="6fd94-104">В предыдущих версиях Dynamics 365 Project Service Automation, записи времени вводились еженедельно.</span><span class="sxs-lookup"><span data-stu-id="6fd94-104">In previous versions of Dynamics 365 Project Service Automation, time entries were entered on a weekly basis.</span></span> <span data-ttu-id="6fd94-105">В версии 3 Project Service Automation записи времени вводятся ежедневно.</span><span class="sxs-lookup"><span data-stu-id="6fd94-105">In version 3 of Project Service Automation, time entries are entered on a daily basis.</span></span> <span data-ttu-id="6fd94-106">Однако после создания нескольких записей времени их можно массово создавать или копировать.</span><span class="sxs-lookup"><span data-stu-id="6fd94-106">However, after a few time entries have been created, you can bulk create or copy them.</span></span>

## <a name="create-a-time-entry"></a><span data-ttu-id="6fd94-107">Создание записи времени</span><span class="sxs-lookup"><span data-stu-id="6fd94-107">Create a time entry</span></span>

<span data-ttu-id="6fd94-108">Выполните следующие действия, чтобы создать запись времени.</span><span class="sxs-lookup"><span data-stu-id="6fd94-108">Follow these steps to create a time entry.</span></span>

1. <span data-ttu-id="6fd94-109">На странице **Записи времени** выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="6fd94-109">On the **Time Entries** page, select **New**.</span></span>
2. <span data-ttu-id="6fd94-110">В диалоговом окне **Быстрое создание: Запись времени** введите длительность записи времени в минутах, часах или днях.</span><span class="sxs-lookup"><span data-stu-id="6fd94-110">In the **Quick Create: Time Entry** dialog box, enter the duration of the time entry in minutes, hours, or days.</span></span> <span data-ttu-id="6fd94-111">Длительность следует вводить в следующем формате: *x* мин, *x* ч или *x* дней.</span><span class="sxs-lookup"><span data-stu-id="6fd94-111">The duration must be entered in the following format: *x* minutes, *x* hours, or *x* days.</span></span> <span data-ttu-id="6fd94-112">Часы и дни также можно вводить как десятичные числа, например *x,x* ч или *x,x* дней.</span><span class="sxs-lookup"><span data-stu-id="6fd94-112">Hours and days can also be entered as decimal values, such as *x.x* hours or *x.x* days.</span></span>
3. <span data-ttu-id="6fd94-113">Выберите тип записи времени и проект, для которого вы входите запись времени.</span><span class="sxs-lookup"><span data-stu-id="6fd94-113">Select the type of time entry and the project that you're entering the time entry for.</span></span>
4. <span data-ttu-id="6fd94-114">В поле **Задача проекта** найдите задачу для этой записи времени.</span><span class="sxs-lookup"><span data-stu-id="6fd94-114">In the **Project Task** field, find the task for this time entry.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6fd94-115">Если вы создаете запись времени для задачи, которая не назначена пользователю, в поле **Задача проекта** выберите кнопку **Поиск**, выберите **Изменить представление**, затем выберите **Все активные задачи проекта** для отображения списка всех задач.</span><span class="sxs-lookup"><span data-stu-id="6fd94-115">If you're creating a time entry for a task that isn't assigned to a user, in the **Project Task** field, select the **Search** button, select **Change View**, and then select **All Active Project Tasks** to list all tasks.</span></span>

5. <span data-ttu-id="6fd94-116">Введите описание, если описание является обязательным, затем выберите **Сохранить и закрыть**.</span><span class="sxs-lookup"><span data-stu-id="6fd94-116">Enter a description, if a description is required, and then select **Save and Close**.</span></span>

<span data-ttu-id="6fd94-117">После создания и сохранения записи времени можно изменить ее в сетке записей времени.</span><span class="sxs-lookup"><span data-stu-id="6fd94-117">After the time entry is created and saved, you can edit it in the time entry grid.</span></span> <span data-ttu-id="6fd94-118">Сетка записи времени поддерживает два формата:</span><span class="sxs-lookup"><span data-stu-id="6fd94-118">The time entry grid supports two formats:</span></span>

- <span data-ttu-id="6fd94-119">Можно ввести записи времени в формате **чч:мм**.</span><span class="sxs-lookup"><span data-stu-id="6fd94-119">You can enter time entries in **hh:mm** format.</span></span> <span data-ttu-id="6fd94-120">Этот формат затем преобразуется в часы и доли часов.</span><span class="sxs-lookup"><span data-stu-id="6fd94-120">This format is then converted to hours and fractions.</span></span>
- <span data-ttu-id="6fd94-121">Можно вводить часы и доли часов напрямую.</span><span class="sxs-lookup"><span data-stu-id="6fd94-121">You can enter hours and fractions directly.</span></span>

<span data-ttu-id="6fd94-122">Обратите внимание, что дробные доли часа — это не минуты.</span><span class="sxs-lookup"><span data-stu-id="6fd94-122">Note that the fractions of an hour aren't minutes.</span></span> <span data-ttu-id="6fd94-123">Следовательно, 1,5 часа представляют 1 час и 30 минут.</span><span class="sxs-lookup"><span data-stu-id="6fd94-123">Therefore, 1.5 hours represents 1 hour and 30 minutes.</span></span> <span data-ttu-id="6fd94-124">Это же правило применяется с дробным частям дня.</span><span class="sxs-lookup"><span data-stu-id="6fd94-124">The same rule applies to fractions of a day.</span></span> <span data-ttu-id="6fd94-125">Один день состоит из 24 часов, и 0,5 дня представляют 12 часов.</span><span class="sxs-lookup"><span data-stu-id="6fd94-125">One day is 24 hours, and 0.5 days represents 12 hours.</span></span>

## <a name="bulk-create-time-entries"></a><span data-ttu-id="6fd94-126">Массовое создание записей времени</span><span class="sxs-lookup"><span data-stu-id="6fd94-126">Bulk create time entries</span></span>

<span data-ttu-id="6fd94-127">После создания нескольких записей времени можно скопировать их для массового создания дополнительных записей времени.</span><span class="sxs-lookup"><span data-stu-id="6fd94-127">After a few time entries have been created, you can copy them to create additional time entries in bulk.</span></span>

1. <span data-ttu-id="6fd94-128">На странице **Записи времени** выберите **Копировать неделю**.</span><span class="sxs-lookup"><span data-stu-id="6fd94-128">On the **Time Entries** page, select **Copy Week**.</span></span>
2. <span data-ttu-id="6fd94-129">В группе полей **Из периода** в полях **Дата начала** и **Дата окончания** определите диапазон дат, из которого требуется скопировать записи времени.</span><span class="sxs-lookup"><span data-stu-id="6fd94-129">In the **From Period** field group, in the **Start Date** and **End Date** fields, define the date range to copy time entries from.</span></span>
3. <span data-ttu-id="6fd94-130">В группе полей **В период** в поле **Дата начала** укажите дату, для которой требуется создать записи времени.</span><span class="sxs-lookup"><span data-stu-id="6fd94-130">In the **To Period** field group, in the **Start Date** field, specify the date to create time entries for.</span></span>
4. <span data-ttu-id="6fd94-131">Выберите **Копировать**, чтобы создать копии записей времени, соответствующих дню недели, указанному в группе полей **В период**.</span><span class="sxs-lookup"><span data-stu-id="6fd94-131">Select **Copy** to create a copy of the time entries that correspond to the day of the week that is specified in the **To Period** field group.</span></span> <span data-ttu-id="6fd94-132">Например, запись времени для понедельника на прошлой неделе копируется в понедельник недели, которая указана в группе полей **В период**.</span><span class="sxs-lookup"><span data-stu-id="6fd94-132">For example, the time entry for Monday of last week is copied to Monday of the week that is specified in the **To Period** field group.</span></span>

## <a name="import-data-for-time-entries"></a><span data-ttu-id="6fd94-133">Импорт данных для записей времени</span><span class="sxs-lookup"><span data-stu-id="6fd94-133">Import data for time entries</span></span>

<span data-ttu-id="6fd94-134">Можно импортировать данные из резервирований и назначений проекта.</span><span class="sxs-lookup"><span data-stu-id="6fd94-134">You can import data from project bookings and assignments.</span></span> <span data-ttu-id="6fd94-135">При импорте данных можно указать диапазон дат резервирований для импорта, затем явно выбрать резервирования, которые должны быть созданы как записи времени **Черновик**.</span><span class="sxs-lookup"><span data-stu-id="6fd94-135">When you import data, you can specify the date range of the bookings to import and then explicitly select the bookings that should be created as **Draft** time entries.</span></span>

## <a name="group-by-sort-search-and-filter-capabilities"></a><span data-ttu-id="6fd94-136">Возможности группировки, сортировки, поиска и фильтрации</span><span class="sxs-lookup"><span data-stu-id="6fd94-136">Group by, sort, search, and filter capabilities</span></span>

<span data-ttu-id="6fd94-137">Можно группировать и фильтровать записи времени по измерениям, которые определены в столбцах.</span><span class="sxs-lookup"><span data-stu-id="6fd94-137">You can group and filter time entries by the dimensions that are specified in the columns.</span></span> <span data-ttu-id="6fd94-138">В поле **Группировать по** выберите измерение, которое следует использовать для фильтрации записей времени.</span><span class="sxs-lookup"><span data-stu-id="6fd94-138">In the **Group by** field, select the dimension to use to filter time entries.</span></span> <span data-ttu-id="6fd94-139">Также можно сортировать записи ввода времени в восходящем или нисходящем порядке с помощью стрелок сортировки в заголовках столбцов.</span><span class="sxs-lookup"><span data-stu-id="6fd94-139">You can also sort the time entry records in ascending or descending order by using the sort arrow on the column headings.</span></span> <span data-ttu-id="6fd94-140">Кроме этого, можно отображать или скрывать записи, выбирая кнопку **Фильтр** в заголовках столбцов, затем, в поле **Поиск** вводя текст, который должен использоваться для поиска записей времени по имени проекта, задаче проекта, записи времени или ресурсу.</span><span class="sxs-lookup"><span data-stu-id="6fd94-140">Additionally, you can show or hide entries by selecting the **Filter** button on the column headings, and then, in the **Search** box, entering the text that should be used to search for time entries by project name, project task, time entry, or resource.</span></span>
