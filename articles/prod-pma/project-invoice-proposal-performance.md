---
title: Выполнение предложения по счетам по проекту
description: Этот тема содержит информацию об улучшении производительности предложений по счетам по проекту.
author: Yowelle
manager: AnnBe
ms.date: 03/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 78c924cba8107471a5f8e6d6a38265890d32d72b
ms.sourcegitcommit: 2350c6f3728067a8298adde640e6fdd5984eb077
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/10/2021
ms.locfileid: "5573575"
---
# <a name="project-invoice-proposal-performance"></a><span data-ttu-id="c7a20-103">Выполнение предложения по счетам по проекту</span><span class="sxs-lookup"><span data-stu-id="c7a20-103">Project invoice proposal performance</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="c7a20-104">При создании нового предложения по счетам по проекту вы можете столкнуться с проблемами производительности по мере увеличения количества проектов и вложенных проектов.</span><span class="sxs-lookup"><span data-stu-id="c7a20-104">When you create a new invoice proposal you might encounter performance issues as the number of projects and subprojects increase.</span></span> <span data-ttu-id="c7a20-105">Для повышения производительности доступна функция, которая сокращает время, необходимое для создания нового предложения по счетам по проекту для разнесенных транзакций по проекту.</span><span class="sxs-lookup"><span data-stu-id="c7a20-105">To improve performance, a feature is available that reduces the time needed to create a new invoice proposal for posted project transactions.</span></span>

## <a name="enable-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="c7a20-106">Включение повышения производительности предложений по счетам по проекту</span><span class="sxs-lookup"><span data-stu-id="c7a20-106">Enable project invoice proposal performance enhancement</span></span>
<span data-ttu-id="c7a20-107">Чтобы включить функцию повышения производительности предложений по счетам по проекту, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="c7a20-107">To enable the project invoice proposal performance enhancement feature, complete the following steps.</span></span>

1.  <span data-ttu-id="c7a20-108">Перейдите **Управление функциями** > **Все**.</span><span class="sxs-lookup"><span data-stu-id="c7a20-108">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="c7a20-109">В списке функций найдите **Повышение эффективности предложений по счетам по проекту**.</span><span class="sxs-lookup"><span data-stu-id="c7a20-109">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="c7a20-110">Выберите **Включить сейчас**.</span><span class="sxs-lookup"><span data-stu-id="c7a20-110">Select **Enable now**.</span></span>
3.  <span data-ttu-id="c7a20-111">Обновите страницу в браузере, а затем создайте новое предложение по счетам.</span><span class="sxs-lookup"><span data-stu-id="c7a20-111">Refresh your browser, and then create a new invoice proposal.</span></span>

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="c7a20-112">Выключение повышения производительности предложений по счетам по проекту</span><span class="sxs-lookup"><span data-stu-id="c7a20-112">Turn off project invoice proposal performance enhancement</span></span>
<span data-ttu-id="c7a20-113">Чтобы выключить функцию повышения производительности предложений по счетам по проекту, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="c7a20-113">Complete the following steps to turn off the project invoice proposal performance enhancement.</span></span>

1.  <span data-ttu-id="c7a20-114">Перейдите **Управление функциями** > **Все**.</span><span class="sxs-lookup"><span data-stu-id="c7a20-114">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="c7a20-115">В списке функций найдите **Повышение эффективности предложений по счетам по проекту**.</span><span class="sxs-lookup"><span data-stu-id="c7a20-115">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="c7a20-116">Выберите **Отключить**.</span><span class="sxs-lookup"><span data-stu-id="c7a20-116">Select **Disable**.</span></span>
3.  <span data-ttu-id="c7a20-117">Обновите свой браузер.</span><span class="sxs-lookup"><span data-stu-id="c7a20-117">Refresh your browser.</span></span>

> [!NOTE]
> <span data-ttu-id="c7a20-118">Производительность предложениями по счетам по проекту не может быть повышена, если применяются правила выставления счетов или запущены пакетные процессы.</span><span class="sxs-lookup"><span data-stu-id="c7a20-118">Invoice proposal performance can't be applied when billing rules are enabled or batch processes are running.</span></span>
