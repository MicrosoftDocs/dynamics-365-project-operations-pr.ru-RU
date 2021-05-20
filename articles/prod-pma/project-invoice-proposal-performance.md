---
title: Выполнение предложения по счетам по проекту
description: Этот тема содержит информацию об улучшении производительности предложений по счетам по проекту.
author: Yowelle
manager: AnnBe
ms.date: 04/20/2021
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
ms.openlocfilehash: 1641d5f731029fdbdc16c4b652cc752a583058c6
ms.sourcegitcommit: 68d52fc983861114e654ffc8d2472b4db9b48981
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920318"
---
# <a name="project-invoice-proposal-performance"></a><span data-ttu-id="870ca-103">Выполнение предложения по счетам по проекту</span><span class="sxs-lookup"><span data-stu-id="870ca-103">Project invoice proposal performance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="870ca-104">При создании нового предложения по счетам по проекту вы можете столкнуться с проблемами производительности по мере увеличения количества проектов и вложенных проектов.</span><span class="sxs-lookup"><span data-stu-id="870ca-104">When you create a new invoice proposal you might encounter performance issues as the number of projects and subprojects increase.</span></span> <span data-ttu-id="870ca-105">Для повышения производительности доступна функция, которая сокращает время, необходимое для создания нового предложения по счетам по проекту для разнесенных транзакций по проекту.</span><span class="sxs-lookup"><span data-stu-id="870ca-105">To improve performance, a feature is available that reduces the time needed to create a new invoice proposal for posted project transactions.</span></span>

## <a name="enable-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="870ca-106">Включение повышения производительности предложений по счетам по проекту</span><span class="sxs-lookup"><span data-stu-id="870ca-106">Enable project invoice proposal performance enhancement</span></span>
<span data-ttu-id="870ca-107">Чтобы включить функцию повышения производительности предложений по счетам по проекту, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="870ca-107">To enable the project invoice proposal performance enhancement feature, complete the following steps.</span></span>

1.  <span data-ttu-id="870ca-108">Перейдите **Управление функциями** > **Все**.</span><span class="sxs-lookup"><span data-stu-id="870ca-108">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="870ca-109">В списке функций найдите **Повышение эффективности предложений по счетам по проекту**.</span><span class="sxs-lookup"><span data-stu-id="870ca-109">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="870ca-110">Выберите **Включить сейчас**.</span><span class="sxs-lookup"><span data-stu-id="870ca-110">Select **Enable now**.</span></span>
3.  <span data-ttu-id="870ca-111">Обновите страницу в браузере, а затем создайте новое предложение по счетам.</span><span class="sxs-lookup"><span data-stu-id="870ca-111">Refresh your browser, and then create a new invoice proposal.</span></span>

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="870ca-112">Выключение повышения производительности предложений по счетам по проекту</span><span class="sxs-lookup"><span data-stu-id="870ca-112">Turn off project invoice proposal performance enhancement</span></span>
<span data-ttu-id="870ca-113">Чтобы выключить функцию повышения производительности предложений по счетам по проекту, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="870ca-113">Complete the following steps to turn off the project invoice proposal performance enhancement.</span></span>

1.  <span data-ttu-id="870ca-114">Перейдите **Управление функциями** > **Все**.</span><span class="sxs-lookup"><span data-stu-id="870ca-114">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="870ca-115">В списке функций найдите **Повышение эффективности предложений по счетам по проекту**.</span><span class="sxs-lookup"><span data-stu-id="870ca-115">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="870ca-116">Выберите **Отключить**.</span><span class="sxs-lookup"><span data-stu-id="870ca-116">Select **Disable**.</span></span>
3.  <span data-ttu-id="870ca-117">Обновите свой браузер.</span><span class="sxs-lookup"><span data-stu-id="870ca-117">Refresh your browser.</span></span>

> [!NOTE]
> <span data-ttu-id="870ca-118">Производительность предложениями по счетам по проекту не может быть повышена, если применяются правила выставления счетов или запущены пакетные процессы.</span><span class="sxs-lookup"><span data-stu-id="870ca-118">Invoice proposal performance can't be applied when billing rules are enabled or batch processes are running.</span></span>
