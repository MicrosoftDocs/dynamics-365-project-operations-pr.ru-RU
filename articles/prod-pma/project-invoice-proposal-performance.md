---
title: Выполнение предложения по счетам по проекту
description: Этот тема содержит информацию об улучшении производительности предложений по счетам по проекту.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 5a14acf51d277b16896d64c4b12ee00bfb326910
ms.sourcegitcommit: 3a4b181be08ef0428104d72b54a3e61ac2782f14
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/17/2021
ms.locfileid: "6269806"
---
# <a name="project-invoice-proposal-performance"></a><span data-ttu-id="7ce2e-103">Выполнение предложения по счетам по проекту</span><span class="sxs-lookup"><span data-stu-id="7ce2e-103">Project invoice proposal performance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7ce2e-104">При создании нового предложения по счетам по проекту вы можете столкнуться с проблемами производительности по мере увеличения количества проектов и вложенных проектов.</span><span class="sxs-lookup"><span data-stu-id="7ce2e-104">When you create a new invoice proposal you might encounter performance issues as the number of projects and subprojects increase.</span></span> <span data-ttu-id="7ce2e-105">Для повышения производительности доступна функция, которая сокращает время, необходимое для создания нового предложения по счетам по проекту для разнесенных транзакций по проекту.</span><span class="sxs-lookup"><span data-stu-id="7ce2e-105">To improve performance, a feature is available that reduces the time needed to create a new invoice proposal for posted project transactions.</span></span>

## <a name="enable-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="7ce2e-106">Включение повышения производительности предложений по счетам по проекту</span><span class="sxs-lookup"><span data-stu-id="7ce2e-106">Enable project invoice proposal performance enhancement</span></span>
<span data-ttu-id="7ce2e-107">Чтобы включить функцию повышения производительности предложений по счетам по проекту, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="7ce2e-107">To enable the project invoice proposal performance enhancement feature, complete the following steps.</span></span>

1.  <span data-ttu-id="7ce2e-108">Перейдите **Управление функциями** > **Все**.</span><span class="sxs-lookup"><span data-stu-id="7ce2e-108">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="7ce2e-109">В списке функций найдите **Повышение эффективности предложений по счетам по проекту**.</span><span class="sxs-lookup"><span data-stu-id="7ce2e-109">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="7ce2e-110">Выберите **Включить сейчас**.</span><span class="sxs-lookup"><span data-stu-id="7ce2e-110">Select **Enable now**.</span></span>
3.  <span data-ttu-id="7ce2e-111">Обновите страницу в браузере, а затем создайте новое предложение по счетам.</span><span class="sxs-lookup"><span data-stu-id="7ce2e-111">Refresh your browser, and then create a new invoice proposal.</span></span>

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="7ce2e-112">Выключение повышения производительности предложений по счетам по проекту</span><span class="sxs-lookup"><span data-stu-id="7ce2e-112">Turn off project invoice proposal performance enhancement</span></span>
<span data-ttu-id="7ce2e-113">Чтобы выключить функцию повышения производительности предложений по счетам по проекту, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="7ce2e-113">Complete the following steps to turn off the project invoice proposal performance enhancement.</span></span>

1.  <span data-ttu-id="7ce2e-114">Перейдите **Управление функциями** > **Все**.</span><span class="sxs-lookup"><span data-stu-id="7ce2e-114">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="7ce2e-115">В списке функций найдите **Повышение эффективности предложений по счетам по проекту**.</span><span class="sxs-lookup"><span data-stu-id="7ce2e-115">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="7ce2e-116">Выберите **Отключить**.</span><span class="sxs-lookup"><span data-stu-id="7ce2e-116">Select **Disable**.</span></span>
3.  <span data-ttu-id="7ce2e-117">Обновите свой браузер.</span><span class="sxs-lookup"><span data-stu-id="7ce2e-117">Refresh your browser.</span></span>

> [!NOTE]
> <span data-ttu-id="7ce2e-118">Параметр эффективности предлагаемого счета не может быть применен, если включены правила выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="7ce2e-118">Invoice proposal performance can't be applied when billing rules are enabled.</span></span>
> 
> <span data-ttu-id="7ce2e-119">Во время пакетного процесса создания предложений по счетам количество подзадач разделит задачи на максимально возможное количество в зависимости от количества контрактов с транзакциями, которые учитываются в счетах, независимо от того, какую информацию вы указали.</span><span class="sxs-lookup"><span data-stu-id="7ce2e-119">During the batch process to create invoice proposals, the number of subtasks will split the tasks to a maximum number based on the number of contracts with invoiceable transactions, regardless of what you have entered.</span></span> <span data-ttu-id="7ce2e-120">Например, если вы введете **3** в поле количества подзадач для создания предложения по счету в пакете, а есть только два контракта с транзакциями, учитываемыми в счете, то будут созданы только две подзадачи.</span><span class="sxs-lookup"><span data-stu-id="7ce2e-120">For example, if you enter **3** for the number of subtasks for invoice proposal creation in batch, and there are only two contracts with invoiceable transactions, only two subtasks are created.</span></span>
