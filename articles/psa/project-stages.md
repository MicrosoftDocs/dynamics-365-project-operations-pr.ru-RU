---
title: Типы стадий проекта
description: В этом разделе представлена информация о стадиях проекта.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: 3503b17e54fc0b321582c30ce534e4cb3f497a5f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283699"
---
# <a name="project-stage-types"></a><span data-ttu-id="adaf3-103">Типы стадий проекта</span><span class="sxs-lookup"><span data-stu-id="adaf3-103">Project stage types</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="adaf3-104">Стадии проекта создаются с целью отражения статуса проекта в ходе его выполнения.</span><span class="sxs-lookup"><span data-stu-id="adaf3-104">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="adaf3-105">Настройки могут использоваться для автоматического обновления стадий для включения сведений о потоках бизнес-процесса, Power Automate или расширений подключаемых модулей.</span><span class="sxs-lookup"><span data-stu-id="adaf3-105">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="adaf3-106">Следующие этапы определены в последовательности операций бизнес-процесса по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="adaf3-106">The following stages are defined in the default BPF:</span></span>

- <span data-ttu-id="adaf3-107">Новое</span><span class="sxs-lookup"><span data-stu-id="adaf3-107">New</span></span>
- <span data-ttu-id="adaf3-108">Предложение с расценками</span><span class="sxs-lookup"><span data-stu-id="adaf3-108">Quote</span></span>
- <span data-ttu-id="adaf3-109">Планирование</span><span class="sxs-lookup"><span data-stu-id="adaf3-109">Plan</span></span>
- <span data-ttu-id="adaf3-110">Доставка</span><span class="sxs-lookup"><span data-stu-id="adaf3-110">Deliver</span></span>
- <span data-ttu-id="adaf3-111">Завершено</span><span class="sxs-lookup"><span data-stu-id="adaf3-111">Complete</span></span>
- <span data-ttu-id="adaf3-112">Закрытие</span><span class="sxs-lookup"><span data-stu-id="adaf3-112">Close</span></span> 

## <a name="new"></a><span data-ttu-id="adaf3-113">Создано</span><span class="sxs-lookup"><span data-stu-id="adaf3-113">New</span></span>

<span data-ttu-id="adaf3-114">При создании проекта стадия проекта задается как **Создать**.</span><span class="sxs-lookup"><span data-stu-id="adaf3-114">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="adaf3-115">Если проект был создан из шаблона, он может иметь расписание, оценку и данные рабочей группы.</span><span class="sxs-lookup"><span data-stu-id="adaf3-115">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="adaf3-116">В противном случае это просто схема проекта, остальные компоненты необходимо ввести.</span><span class="sxs-lookup"><span data-stu-id="adaf3-116">Otherwise, it's just an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="adaf3-117">Предложение с расценками</span><span class="sxs-lookup"><span data-stu-id="adaf3-117">Quote</span></span>

<span data-ttu-id="adaf3-118">При связывании проекта с предложением с расценками или при создании проекта из предложения с расценками стадия проекта задана как **Предложение с расценками**, и также обновляются расчетные даты начала и окончания.</span><span class="sxs-lookup"><span data-stu-id="adaf3-118">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="adaf3-119">Пока проект находится на стадии **Предложение с расценками**, сведения по предложению с расценками отображаются на вкладке **Продажи** на странице **Сущность проекта**.</span><span class="sxs-lookup"><span data-stu-id="adaf3-119">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="adaf3-120">Планирование</span><span class="sxs-lookup"><span data-stu-id="adaf3-120">Plan</span></span>

<span data-ttu-id="adaf3-121">При выигрыше предложения с расценками, связанного с проектом, проект переходит на этап **Контракт**, стадия проекта обновляется на **План**.</span><span class="sxs-lookup"><span data-stu-id="adaf3-121">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="adaf3-122">Пока проект находится на стадии **План**, на странице **Сущность проекта** отображаются сведения о контракте.</span><span class="sxs-lookup"><span data-stu-id="adaf3-122">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="adaf3-123">Доставка</span><span class="sxs-lookup"><span data-stu-id="adaf3-123">Deliver</span></span>

<span data-ttu-id="adaf3-124">Когда планирование проекта завершено, и все готово для запуска проекта, руководитель проекта должен обновить стадию проекта на **Доставка** для отображения того, что проект начался.</span><span class="sxs-lookup"><span data-stu-id="adaf3-124">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="adaf3-125">Завершено</span><span class="sxs-lookup"><span data-stu-id="adaf3-125">Complete</span></span> 

<span data-ttu-id="adaf3-126">Когда работа по проекту выполнена, руководитель проекта может обновить стадию на **Завершено**.</span><span class="sxs-lookup"><span data-stu-id="adaf3-126">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="adaf3-127">Путем обновления стадии проекта на **Завершено** руководитель проекта указывает, что работа на 100 процентов завершена, но проект остается открытым, чтобы можно было зарегистрировать все ожидающие записи времени или расходов.</span><span class="sxs-lookup"><span data-stu-id="adaf3-127">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="adaf3-128">Закрытие</span><span class="sxs-lookup"><span data-stu-id="adaf3-128">Close</span></span>

<span data-ttu-id="adaf3-129">Когда все транзакции зафиксированы для проекта, руководитель проекта может обновить стадию на **Закрыт**.</span><span class="sxs-lookup"><span data-stu-id="adaf3-129">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="adaf3-130">В этот момент никакие транзакции невозможно зафиксировать, и проект становится доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="adaf3-130">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]