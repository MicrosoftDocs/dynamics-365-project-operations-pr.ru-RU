---
title: Использование доски расписания для резервирования ресурсов для проекта
description: В этом разделе представлена информация о том, как резервировать ресурсы.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 169f7b98-119b-4aa2-b121-c73c0396fcde
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: b377e0c80b2c4eb5028f131620213ea534a1a4dc
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755009"
---
# <a name="use-the-schedule-board-to-book-project-resources"></a><span data-ttu-id="9f301-103">Использование доски расписания для резервирования ресурсов для проекта</span><span class="sxs-lookup"><span data-stu-id="9f301-103">Use the Schedule Board to book project resources</span></span>

<span data-ttu-id="9f301-104">В дополнение к резервированию ресурсов для проекта из самого проекта, можно окончательно или предварительно резервировать ресурсы с доски расписания.</span><span class="sxs-lookup"><span data-stu-id="9f301-104">In addition to booking resources on a project from within a project, you can hard-book or soft-book resources from the Schedule Board.</span></span>

<span data-ttu-id="9f301-105">Прежде чем можно будет резервировать с доски расписания, нужно создать или сформировать требования ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9f301-105">Before you can book from the Schedule Board, you must create or generate resource requirements.</span></span> <span data-ttu-id="9f301-106">Выполните эти действия, чтобы создать требования ресурсов из доски расписания.</span><span class="sxs-lookup"><span data-stu-id="9f301-106">Follow these steps to create resource requirements from the Schedule Board.</span></span>

1. <span data-ttu-id="9f301-107">Если область **Требования к резервированию** внизу страницы свернута, выберите элемент управление развертыванием, чтобы развернуть ее.</span><span class="sxs-lookup"><span data-stu-id="9f301-107">If the **Booking Requirements** pane at the bottom of the page is collapsed, select the expander control to expand it.</span></span>
2. <span data-ttu-id="9f301-108">В области **Требования к резервированию** на вкладке **Проект** выберите требование для резервирования.</span><span class="sxs-lookup"><span data-stu-id="9f301-108">In the **Booking Requirements** pane, on the **Project** tab, select the requirement to book.</span></span>

    ![Требование, выбранное на вкладке "Проект"](media/Resource-Management-image73.png)

3. <span data-ttu-id="9f301-110">Выберите фильтр **Найти доступность** для фильтрации резервируемых ресурсов и просмотра доступных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9f301-110">Select **Find Availability** to filter the bookable resources and view the available resources.</span></span> 
4. <span data-ttu-id="9f301-111">Выберите один или несколько ресурсов на доске расписания.</span><span class="sxs-lookup"><span data-stu-id="9f301-111">Select one or more resources from the Schedule Board.</span></span> 
5. <span data-ttu-id="9f301-112">В области **Создать резервирование ресурса** с правой стороны страницы введите данные резервирования, затем выберите **Зарезервировать и выйти**.</span><span class="sxs-lookup"><span data-stu-id="9f301-112">In the **Create Resource Booking** pane on the right side of the page, enter the booking information, and then select **Book and exit**.</span></span>

    ![Область создания резервирования ресурса для выбранного резервируемого ресурса](media/Resource-Management-image74.png)

6. <span data-ttu-id="9f301-114">Пока требование выбрано в области **Создать резервирование ресурса**, выберите одну или несколько ячеек ресурса для создания резервирования.</span><span class="sxs-lookup"><span data-stu-id="9f301-114">While the requirement is selected in the **Create Resource Booking** pane, select one or more cells of a resource to create the booking.</span></span>

    ![Несколько ячеек, выбранные для ресурса](media/Resource-Management-image75.png)

7. <span data-ttu-id="9f301-116">Выберите **Резервировать**.</span><span class="sxs-lookup"><span data-stu-id="9f301-116">Select **Book**.</span></span>

<span data-ttu-id="9f301-117">Требования выполняется с помощью выбранного ресурса.</span><span class="sxs-lookup"><span data-stu-id="9f301-117">The requirement is fulfilled by using the selected resource.</span></span> <span data-ttu-id="9f301-118">В области **Требования к резервированию** обратите внимание, что требование обновлено, и ресурс отображается как зарезервированный по проекту.</span><span class="sxs-lookup"><span data-stu-id="9f301-118">In the **Booking Requirements** pane, notice that the requirement has been updated, and the resource is shown as booked on the project.</span></span>

![Ресурс, зарезервированный по проекту](media/Resource-Management-image76.png)
