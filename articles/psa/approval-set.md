---
title: Наборы утверждения
description: Этот тема предоставляет информацию о наборе утверждений, запросах и подмножествах этих операций.
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ac73313420029ece740d0bdb9c21c7abaa9defc6
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116887"
---
# <a name="approval-sets"></a><span data-ttu-id="87c8c-103">Наборы утверждения</span><span class="sxs-lookup"><span data-stu-id="87c8c-103">Approval sets</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="87c8c-104">Наборы утверждений объединяют запросы на утверждение в более мелкие подмножества операций.</span><span class="sxs-lookup"><span data-stu-id="87c8c-104">Approval sets group approval requests together into smaller subsets of operations.</span></span> <span data-ttu-id="87c8c-105">Такая группировка позволяет обрабатывать утверждения в порядке по проектам и позволяет повторять попытки и упорядочивать.</span><span class="sxs-lookup"><span data-stu-id="87c8c-105">This grouping allows approvals to be processed in order by Project and allows for retrying and sequencing.</span></span> <span data-ttu-id="87c8c-106">Группирование повышает надежность и отслеживаемость обработки утверждений для больших объемов утверждений.</span><span class="sxs-lookup"><span data-stu-id="87c8c-106">Grouping improves the reliability and traceability of approval processing for large volumes of approvals.</span></span>

<span data-ttu-id="87c8c-107">Наборы утверждений указывают на общее состояние обработки связанных записей.</span><span class="sxs-lookup"><span data-stu-id="87c8c-107">Approval sets indicate the overall processing state of their related records.</span></span> <span data-ttu-id="87c8c-108">Когда запись утверждения обрабатывается с использованием набора утверждений, запись перемещается из **Отправлено** в **Утверждено**, и отвязывается от набора утверждения.</span><span class="sxs-lookup"><span data-stu-id="87c8c-108">When an approval record is processed using an approval set, the record moves from **Submitted** to **Approved**, and is unlinked from the approval set.</span></span> <span data-ttu-id="87c8c-109">Если запись не выполняется при ее отправке на утверждение, она остается в состоянии **Отправлено** и набор утверждений помечается как неудавшийся.</span><span class="sxs-lookup"><span data-stu-id="87c8c-109">If a record fails when it is submitted for approval, the record remains in a status of **Submitted** and the approval set is marked as failed.</span></span> <span data-ttu-id="87c8c-110">Набор утверждений регистрирует сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="87c8c-110">The approval set logs the error message of the failure.</span></span>

## <a name="processing-approvals-and-approval-sets"></a><span data-ttu-id="87c8c-111">Обработка утверждений и наборов утверждений</span><span class="sxs-lookup"><span data-stu-id="87c8c-111">Processing approvals and approval sets</span></span>
<span data-ttu-id="87c8c-112">Утверждения, поставленные в очередь на обработку, отображаются в предоставлении **Утверждения в обработке**.</span><span class="sxs-lookup"><span data-stu-id="87c8c-112">Approvals that are queued for processing are visible in the **Processing Approvals** view.</span></span> <span data-ttu-id="87c8c-113">Система пытается обработать все записи несколько раз в асинхронном режиме, включая повторную попытку утверждения, если предыдущие попытки оказались неудачными.</span><span class="sxs-lookup"><span data-stu-id="87c8c-113">The system tries to process all the entries multiple times asynchronously, including retrying an approval if previous attempts failed.</span></span>

<span data-ttu-id="87c8c-114">Поле **Срок действия набора утверждений** записывает количество оставшихся попыток обработки набора, прежде чем он будет помечен как неудачный.</span><span class="sxs-lookup"><span data-stu-id="87c8c-114">The **Approval Set Lifetime** field records the number of attempts left to process the set before it's marked as failed.</span></span>

## <a name="failed-approvals-and-approval-sets"></a><span data-ttu-id="87c8c-115">Сбой утверждений и наборов утверждений</span><span class="sxs-lookup"><span data-stu-id="87c8c-115">Failed approvals and approval sets</span></span>
<span data-ttu-id="87c8c-116">В представлении **Неудачные утверждения** перечислены все утверждения, требующие вмешательства пользователя.</span><span class="sxs-lookup"><span data-stu-id="87c8c-116">The **Failed Approvals** view lists all approvals that require user intervention.</span></span> <span data-ttu-id="87c8c-117">Откройте связанные журналы наборов утверждений, чтобы определить причину сбоя.</span><span class="sxs-lookup"><span data-stu-id="87c8c-117">Open the associated approval set logs to identify the cause of the failure.</span></span>
<span data-ttu-id="87c8c-118">Если выбрать **Повторить**, будет добавлено значение к счетчику сроку действия набора утверждений, набор утверждений будет возвращен в состояние **Обработка**, и система попытается обработать оставшиеся записи.</span><span class="sxs-lookup"><span data-stu-id="87c8c-118">Selecting **Retry** adds to the approval set lifetime count, moves the approval set back to a status of **Processing**, and attempts to process the remaining records.</span></span>

## <a name="configure-approval-sets"></a><span data-ttu-id="87c8c-119">Настройка наборов утверждений</span><span class="sxs-lookup"><span data-stu-id="87c8c-119">Configure approval sets</span></span>

###  <a name="enable-the-approval-sets-feature"></a><span data-ttu-id="87c8c-120">Включите функцию наборов утверждений</span><span class="sxs-lookup"><span data-stu-id="87c8c-120">Enable the Approval sets feature</span></span>
<span data-ttu-id="87c8c-121">Прежде чем включить функцию наборов утверждений, убедитесь, что в настоящее время нет обрабатываемых утверждений.</span><span class="sxs-lookup"><span data-stu-id="87c8c-121">Before you enable the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="87c8c-122">Перейдите на страницу **Параметры проекта** и выберите **Управление функциями** > **Включить современные утверждения**.</span><span class="sxs-lookup"><span data-stu-id="87c8c-122">Go to the **Project parameters** page and select **Feature Control** > **Enable Modern Approvals**.</span></span>

### <a name="turn-off-the-approval-sets-feature"></a><span data-ttu-id="87c8c-123">Выключите функцию наборов утверждений</span><span class="sxs-lookup"><span data-stu-id="87c8c-123">Turn off the Approval sets feature</span></span>
<span data-ttu-id="87c8c-124">Прежде чем выключить функцию наборов утверждений, убедитесь, что в настоящее время нет обрабатываемых утверждений.</span><span class="sxs-lookup"><span data-stu-id="87c8c-124">Before you turn off the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="87c8c-125">Перейдите на страницу **Параметры проекта** и выберите **Управление функциями** > **Отключить современные утверждения**.</span><span class="sxs-lookup"><span data-stu-id="87c8c-125">Go to the **Project Parameters** page and select **Feature Control** > **Disable Modern Approvals**.</span></span>

### <a name="configuring-the-asynchronous-threshold"></a><span data-ttu-id="87c8c-126">Настройка асинхронного порога</span><span class="sxs-lookup"><span data-stu-id="87c8c-126">Configuring the asynchronous threshold</span></span> 
<span data-ttu-id="87c8c-127">При создании наборов утверждения обработка переходит в фоновый режим, когда выбранное количество записей для утверждения превышает указанный порог.</span><span class="sxs-lookup"><span data-stu-id="87c8c-127">When approval sets are created, processing moves to the background when the selected number of records for approval exceeds the indicated threshold.</span></span> <span data-ttu-id="87c8c-128">Используйте поле **Асинхронный порог** для настройки, когда обработка утверждений должна выполняться синхронно или асинхронно.</span><span class="sxs-lookup"><span data-stu-id="87c8c-128">Use the **Asynchronous Threshold** field to configure when approval processing should be run synchronously or asynchronously.</span></span>
<span data-ttu-id="87c8c-129">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="87c8c-129">Valid values are:</span></span>

  - <span data-ttu-id="87c8c-130">Ноль: все запросы должны обрабатываться асинхронно.</span><span class="sxs-lookup"><span data-stu-id="87c8c-130">Zero: All requests should be processed asynchronously.</span></span> 
  - <span data-ttu-id="87c8c-131">Числа больше нуля: утверждения обрабатываются асинхронно только тогда, когда количество отправленных утверждений превышает это значение.</span><span class="sxs-lookup"><span data-stu-id="87c8c-131">Numbers greater than zero: Approvals are processed asynchronously only when the submitted number of approvals exceeds this value.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
