---
title: Стадии проекта
description: В этом разделе представлена информация о стадиях проекта.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 983c25a0-ed21-4151-a109-b385a88285fa
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 70aa057e127df7ba925e84f5d056a06a4cc8833e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754930"
---
# <a name="project-stages"></a><span data-ttu-id="8d6bd-103">Стадии проекта</span><span class="sxs-lookup"><span data-stu-id="8d6bd-103">Project stages</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="8d6bd-104">Стадии проекта обновляются с целью отражения статуса проекта в ходе его выполнения.</span><span class="sxs-lookup"><span data-stu-id="8d6bd-104">Project stages are updated to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="8d6bd-105">Последовательность операций бизнес-процесса по умолчанию автоматически обновляет некоторые стадии проекта, в то время как остальные вручную обновляются руководителем проекта.</span><span class="sxs-lookup"><span data-stu-id="8d6bd-105">The default business process flow automatically updates some stages of the project while others are manually updated by the project manager.</span></span> 

<span data-ttu-id="8d6bd-106">Следующие этапы определены в последовательности операций бизнес-процесса по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="8d6bd-106">The following stages are defined in the default BPF:</span></span>

- <span data-ttu-id="8d6bd-107">Создано</span><span class="sxs-lookup"><span data-stu-id="8d6bd-107">New</span></span>
- <span data-ttu-id="8d6bd-108">Предложение с расценками</span><span class="sxs-lookup"><span data-stu-id="8d6bd-108">Quote</span></span>
- <span data-ttu-id="8d6bd-109">Планирование</span><span class="sxs-lookup"><span data-stu-id="8d6bd-109">Plan</span></span>
- <span data-ttu-id="8d6bd-110">Доставка</span><span class="sxs-lookup"><span data-stu-id="8d6bd-110">Deliver</span></span>
- <span data-ttu-id="8d6bd-111">Завершено</span><span class="sxs-lookup"><span data-stu-id="8d6bd-111">Complete</span></span>
- <span data-ttu-id="8d6bd-112">Закрытие</span><span class="sxs-lookup"><span data-stu-id="8d6bd-112">Close</span></span> 

## <a name="new"></a><span data-ttu-id="8d6bd-113">Создано</span><span class="sxs-lookup"><span data-stu-id="8d6bd-113">New</span></span>

<span data-ttu-id="8d6bd-114">При создании проекта стадия проекта задается как **Создать**.</span><span class="sxs-lookup"><span data-stu-id="8d6bd-114">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="8d6bd-115">Если проект был создан из шаблона, он может иметь расписание, оценку и данные рабочей группы.</span><span class="sxs-lookup"><span data-stu-id="8d6bd-115">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="8d6bd-116">В противном случае это просто схема проекта, остальные компоненты необходимо ввести.</span><span class="sxs-lookup"><span data-stu-id="8d6bd-116">Otherwise, it's just an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="8d6bd-117">Предложение с расценками</span><span class="sxs-lookup"><span data-stu-id="8d6bd-117">Quote</span></span>

<span data-ttu-id="8d6bd-118">При связывании проекта с предложением с расценками или при создании проекта из предложения с расценками стадия проекта задана как **Предложение с расценками**, и также обновляются расчетные даты начала и окончания.</span><span class="sxs-lookup"><span data-stu-id="8d6bd-118">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="8d6bd-119">Пока проект находится на стадии **Предложение с расценками**, сведения по предложению с расценками отображаются на вкладке **Продажи** на странице **Сущность проекта**.</span><span class="sxs-lookup"><span data-stu-id="8d6bd-119">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="8d6bd-120">Планирование</span><span class="sxs-lookup"><span data-stu-id="8d6bd-120">Plan</span></span>

<span data-ttu-id="8d6bd-121">При выигрыше предложения с расценками, связанного с проектом, проект переходит на этап **Контракт**, стадия проекта обновляется на **План**.</span><span class="sxs-lookup"><span data-stu-id="8d6bd-121">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="8d6bd-122">Пока проект находится на стадии **План**, на странице **Сущность проекта** отображаются сведения о контракте.</span><span class="sxs-lookup"><span data-stu-id="8d6bd-122">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="8d6bd-123">Доставка</span><span class="sxs-lookup"><span data-stu-id="8d6bd-123">Deliver</span></span>

<span data-ttu-id="8d6bd-124">Когда планирование проекта завершено, и все готово для запуска проекта, руководитель проекта должен обновить стадию проекта на **Доставка** для отображения того, что проект начался.</span><span class="sxs-lookup"><span data-stu-id="8d6bd-124">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="8d6bd-125">Завершено</span><span class="sxs-lookup"><span data-stu-id="8d6bd-125">Complete</span></span> 

<span data-ttu-id="8d6bd-126">Когда работа по проекту выполнена, руководитель проекта может обновить стадию на **Завершено**.</span><span class="sxs-lookup"><span data-stu-id="8d6bd-126">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="8d6bd-127">Путем обновления стадии проекта на **Завершено** руководитель проекта указывает, что работа на 100 процентов завершена, но проект остается открытым, чтобы можно было зарегистрировать все ожидающие записи времени или расходов.</span><span class="sxs-lookup"><span data-stu-id="8d6bd-127">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="8d6bd-128">Закрытие</span><span class="sxs-lookup"><span data-stu-id="8d6bd-128">Close</span></span>

<span data-ttu-id="8d6bd-129">Когда все транзакции зафиксированы для проекта, руководитель проекта может обновить стадию на **Закрыт**.</span><span class="sxs-lookup"><span data-stu-id="8d6bd-129">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="8d6bd-130">В этот момент никакие транзакции невозможно зафиксировать, и проект становится доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="8d6bd-130">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>
