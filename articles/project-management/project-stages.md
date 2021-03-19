---
title: Стадии проекта
description: Эта тема предоставляет информацию об этапах проекта, которые доступны в Microsoft Dynamics Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: a5c695e0cd39f8a222e719cc6c9ffe984fe80b07
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286804"
---
# <a name="project-stages"></a><span data-ttu-id="a24f6-103">Стадии проекта</span><span class="sxs-lookup"><span data-stu-id="a24f6-103">Project stages</span></span>

<span data-ttu-id="a24f6-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="a24f6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a24f6-105">Стадии проекта создаются с целью отражения статуса проекта в ходе его выполнения.</span><span class="sxs-lookup"><span data-stu-id="a24f6-105">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="a24f6-106">Настройки могут использоваться для автоматического обновления стадий для включения сведений о потоках бизнес-процесса, Power Automate или расширений подключаемых модулей.</span><span class="sxs-lookup"><span data-stu-id="a24f6-106">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="a24f6-107">Следующие этапы определены в потоке бизнес-процесса по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="a24f6-107">The following stages are defined in the default business process flow:</span></span>

- <span data-ttu-id="a24f6-108">Новая</span><span class="sxs-lookup"><span data-stu-id="a24f6-108">New</span></span>
- <span data-ttu-id="a24f6-109">Предложение с расценками</span><span class="sxs-lookup"><span data-stu-id="a24f6-109">Quote</span></span>
- <span data-ttu-id="a24f6-110">План</span><span class="sxs-lookup"><span data-stu-id="a24f6-110">Plan</span></span>
- <span data-ttu-id="a24f6-111">Доставка</span><span class="sxs-lookup"><span data-stu-id="a24f6-111">Deliver</span></span>
- <span data-ttu-id="a24f6-112">Завершить</span><span class="sxs-lookup"><span data-stu-id="a24f6-112">Complete</span></span>
- <span data-ttu-id="a24f6-113">Закрыть</span><span class="sxs-lookup"><span data-stu-id="a24f6-113">Close</span></span> 

## <a name="new"></a><span data-ttu-id="a24f6-114">Новая</span><span class="sxs-lookup"><span data-stu-id="a24f6-114">New</span></span>

<span data-ttu-id="a24f6-115">При создании проекта стадия проекта задается как **Создать**.</span><span class="sxs-lookup"><span data-stu-id="a24f6-115">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="a24f6-116">Если проект был создан из шаблона, он может иметь расписание, оценку и данные рабочей группы.</span><span class="sxs-lookup"><span data-stu-id="a24f6-116">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="a24f6-117">В противном случае это схема проекта, остальные компоненты необходимо ввести.</span><span class="sxs-lookup"><span data-stu-id="a24f6-117">Otherwise, it's an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="a24f6-118">Предложение с расценками</span><span class="sxs-lookup"><span data-stu-id="a24f6-118">Quote</span></span>

<span data-ttu-id="a24f6-119">При связывании проекта с предложением с расценками или при создании проекта из предложения с расценками стадия проекта задана как **Предложение с расценками**, и также обновляются расчетные даты начала и окончания.</span><span class="sxs-lookup"><span data-stu-id="a24f6-119">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="a24f6-120">Пока проект находится на стадии **Предложение с расценками**, сведения по предложению с расценками отображаются на вкладке **Продажи** на странице **Сущность проекта**.</span><span class="sxs-lookup"><span data-stu-id="a24f6-120">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="a24f6-121">Планирование</span><span class="sxs-lookup"><span data-stu-id="a24f6-121">Plan</span></span>

<span data-ttu-id="a24f6-122">При выигрыше предложения с расценками, связанного с проектом, проект переходит на этап **Контракт**, стадия проекта обновляется на **План**.</span><span class="sxs-lookup"><span data-stu-id="a24f6-122">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="a24f6-123">Пока проект находится на стадии **План**, на странице **Сущность проекта** отображаются сведения о контракте.</span><span class="sxs-lookup"><span data-stu-id="a24f6-123">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="a24f6-124">Доставка</span><span class="sxs-lookup"><span data-stu-id="a24f6-124">Deliver</span></span>

<span data-ttu-id="a24f6-125">Когда планирование проекта завершено, и все готово для запуска проекта, руководитель проекта должен обновить стадию проекта на **Доставка** для отображения того, что проект начался.</span><span class="sxs-lookup"><span data-stu-id="a24f6-125">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="a24f6-126">Завершено</span><span class="sxs-lookup"><span data-stu-id="a24f6-126">Complete</span></span> 

<span data-ttu-id="a24f6-127">Когда работа по проекту выполнена, руководитель проекта может обновить стадию на **Завершено**.</span><span class="sxs-lookup"><span data-stu-id="a24f6-127">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="a24f6-128">Путем обновления стадии проекта на **Завершено** руководитель проекта указывает, что работа на 100 процентов завершена, но проект остается открытым, чтобы можно было зарегистрировать все ожидающие записи времени или расходов.</span><span class="sxs-lookup"><span data-stu-id="a24f6-128">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="a24f6-129">Закрытие</span><span class="sxs-lookup"><span data-stu-id="a24f6-129">Close</span></span>

<span data-ttu-id="a24f6-130">Когда все транзакции зафиксированы для проекта, руководитель проекта может обновить стадию на **Закрыт**.</span><span class="sxs-lookup"><span data-stu-id="a24f6-130">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="a24f6-131">В этот момент никакие транзакции невозможно зафиксировать, и проект становится доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="a24f6-131">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]