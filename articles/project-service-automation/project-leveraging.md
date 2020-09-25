---
title: Оценки продаж и проекты
description: В этом разделе представлена информация о том, как использовать расписания и оценки в процессе продаж.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: eb5ab6a1-fdff-490e-9c2a-19aef493de11
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 4431c1c894a01bfecc132575d8981ebc9fe50b51
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754934"
---
# <a name="sales-estimates-and-projects"></a><span data-ttu-id="b8660-103">Оценки продаж и проекты</span><span class="sxs-lookup"><span data-stu-id="b8660-103">Sales estimates and projects</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="b8660-104">Во время процесса продаж можно создать оценки продаж, связав проект с предложением с расценками по продажам.</span><span class="sxs-lookup"><span data-stu-id="b8660-104">During the sales process, you can create sales estimates by linking a project to a sales quote.</span></span> <span data-ttu-id="b8660-105">Таким образом, детерминистская оценка может возникнуть в ходе процесса продаж, чтобы воспользоваться возможностями планирования и оценки проекта.</span><span class="sxs-lookup"><span data-stu-id="b8660-105">In this way, deterministic estimation can occur during the sales process, to take advantage of project scheduling and estimation capabilities.</span></span> <span data-ttu-id="b8660-106">Если продажа проходит, расписание, которое использовалось для целей оценки продаж, можно использовать в качестве основы для дальнейшего уточнения плана проекта.</span><span class="sxs-lookup"><span data-stu-id="b8660-106">If the sale goes through, the schedule that was used for sales estimation purposes can be used as the basis for further refinement of the project plan.</span></span>

## <a name="linking-a-project-to-a-quote-line"></a><span data-ttu-id="b8660-107">Связывание проекта со строкой предложения с расценками</span><span class="sxs-lookup"><span data-stu-id="b8660-107">Linking a project to a quote line</span></span>

<span data-ttu-id="b8660-108">При создании строки предложения с расценками на основе проекта можно создать новый проект или связать существующий проект на странице **Строка предложения с расценками**.</span><span class="sxs-lookup"><span data-stu-id="b8660-108">When you create a project-based quote line, you can create a new project or associate an existing project pn the **Quote Line** page.</span></span> 

> ![Форма строки предложения с расценками](media/project-8.png)
 
<span data-ttu-id="b8660-110">При создании нового проекта из сведений строки предложения с расценками можно воспользоваться шаблонами проекта.</span><span class="sxs-lookup"><span data-stu-id="b8660-110">When you create a new project from the quote line details, you can take advantage of project templates.</span></span> <span data-ttu-id="b8660-111">Шаблоны проектов — это модельные проекты, которые представляют собой стандартные планы и финансовые оценки проекта, которые типичны в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="b8660-111">Project templates are model projects that represent standard project plans and financial estimates that are typical in an organization.</span></span> <span data-ttu-id="b8660-112">Они также могут представлять копии планов и оценок проектов из последних проектов.</span><span class="sxs-lookup"><span data-stu-id="b8660-112">They can also represent copies of project plans and estimates from past projects.</span></span>

> ![Сведения строки предложения с расценками](media/project-9.png)
  
<span data-ttu-id="b8660-114">При создании проекта из предложения с расценками проект автоматически связывается со строкой предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="b8660-114">When you create the project from the quote, the project is automatically associated with the quote line.</span></span>

## <a name="components-of-estimates-in-a-project"></a><span data-ttu-id="b8660-115">Компоненты оценок в проекте</span><span class="sxs-lookup"><span data-stu-id="b8660-115">Components of estimates in a project</span></span>

<span data-ttu-id="b8660-116">Расписание позволяет разделить работу на задачи, поддерживать иерархию задач, определить, какие ресурсы требуются для выполнения задачи, и назначить оценку усилий, необходимых для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="b8660-116">A schedule lets you divide work into tasks, maintain a hierarchy of tasks, determine what resources are required to complete a task, and assign an estimate of the effort that is required to complete a task.</span></span>

<span data-ttu-id="b8660-117">Можно определить рабочие усилия и оценки расписания с помощью полей на вкладке **Расписание** страницы **Проект**.</span><span class="sxs-lookup"><span data-stu-id="b8660-117">You can define the work effort and schedule estimates by using the fields on the **Schedule** tab of the **Project** page.</span></span> <span data-ttu-id="b8660-118">Поскольку прайс-лист связан с проектом, финансовые оценки вычисляются с помощью стоимости и цен продаж, которые определены в прайс-листе.</span><span class="sxs-lookup"><span data-stu-id="b8660-118">Because a price list is associated with the project, financial estimates are calculated by using cost and sales prices that are defined in the price list.</span></span>

## <a name="importing-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="b8660-119">Импорт оценок из проекта в предложение с расценками</span><span class="sxs-lookup"><span data-stu-id="b8660-119">Importing estimates from a project into a quote</span></span>

<span data-ttu-id="b8660-120">После определения оценок проекта, можно импортировать их в строку предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="b8660-120">After you define project estimates, you can import them into the quote line.</span></span> <span data-ttu-id="b8660-121">На странице **Сведения строки предложения с расценками**, выберите **Импортировать из оценок** на ленте, чтобы получить сводку оценок проекта по типу транзакции, роли или уровню задачи.</span><span class="sxs-lookup"><span data-stu-id="b8660-121">On the **Quote Line Details** page, select **Import from estimates** on the ribbon to summarize project estimates by transaction type, role, or task level.</span></span>