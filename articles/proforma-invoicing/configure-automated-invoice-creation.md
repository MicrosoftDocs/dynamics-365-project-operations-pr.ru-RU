---
title: Настройка автоматического создания счетов
description: Эта тема предоставляет информацию о том, как настроить систему для автоматического создания счетов.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 764fd4568619e4f5676ee3cbf7fce14ffb069548
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898142"
---
# <a name="configure-automated-invoice-creation"></a><span data-ttu-id="d719a-103">Настройка автоматического создания счетов</span><span class="sxs-lookup"><span data-stu-id="d719a-103">Configure automated invoice creation</span></span>

<span data-ttu-id="d719a-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="d719a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d719a-105">Выполните следующие шаги, чтобы настроить автоматический запуск счетов в Project Operations.</span><span class="sxs-lookup"><span data-stu-id="d719a-105">Complete the following steps to configure an automated invoice run in Project operations.</span></span>

1. <span data-ttu-id="d719a-106">Перейдите в раздел **Параметры** \> **Пакетные задания**.</span><span class="sxs-lookup"><span data-stu-id="d719a-106">Go to **Settings** \> **Batch jobs**.</span></span>
2. <span data-ttu-id="d719a-107">Создайте пакетное задание и назовите его **Создание счетов в Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="d719a-107">Create a batch job, and name it **Project operations create invoices**.</span></span> <span data-ttu-id="d719a-108">Имя пакетного задания должно включать термин "создание счетов".</span><span class="sxs-lookup"><span data-stu-id="d719a-108">The name of the batch job must include the term "create invoices."</span></span>
3. <span data-ttu-id="d719a-109">В поле **Тип задания** выберите **Нет**.</span><span class="sxs-lookup"><span data-stu-id="d719a-109">In the **Job type** field, select **None**.</span></span> <span data-ttu-id="d719a-110">По умолчанию для параметров **Частота ежедневно** и **Активно** задано значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="d719a-110">By default, the **Frequency Daily** and **Is Active** options are set to **Yes**.</span></span>
4. <span data-ttu-id="d719a-111">Выберите **Запустить рабочий процесс**.</span><span class="sxs-lookup"><span data-stu-id="d719a-111">Select **Run Workflow**.</span></span> <span data-ttu-id="d719a-112">В диалоговом окне **Поиск в записях** отображаются три рабочих процесса:</span><span class="sxs-lookup"><span data-stu-id="d719a-112">In the **Look Up Record** dialog box, you will see three workflows:</span></span>

    - <span data-ttu-id="d719a-113">ProcessRunCaller</span><span class="sxs-lookup"><span data-stu-id="d719a-113">ProcessRunCaller</span></span>
    - <span data-ttu-id="d719a-114">ProcessRunner</span><span class="sxs-lookup"><span data-stu-id="d719a-114">ProcessRunner</span></span>
    - <span data-ttu-id="d719a-115">UpdateRoleUtilization</span><span class="sxs-lookup"><span data-stu-id="d719a-115">UpdateRoleUtilization</span></span>

5. <span data-ttu-id="d719a-116">Выберите **ProcessRunCaller**, затем выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="d719a-116">Select **ProcessRunCaller**, and then select **Add**.</span></span>
6. <span data-ttu-id="d719a-117">В следующем диалоговом окне выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d719a-117">In the next dialog box, select **OK**.</span></span> <span data-ttu-id="d719a-118">За рабочим процессом **Сон** следует рабочий процесс **Обработка**.</span><span class="sxs-lookup"><span data-stu-id="d719a-118">A **Sleep** workflow is followed by a **Process** workflow.</span></span>

    <span data-ttu-id="d719a-119">Можно также выбрать **ProcessRunner** на шаге 5.</span><span class="sxs-lookup"><span data-stu-id="d719a-119">You can also select **ProcessRunner** in step 5.</span></span> <span data-ttu-id="d719a-120">Затем при выборе **OK** за рабочим процессом **Обработка** следует рабочий процесс **Сон**.</span><span class="sxs-lookup"><span data-stu-id="d719a-120">Then, when you select **OK**, a **Process** workflow is followed by a **Sleep** workflow.</span></span>

<span data-ttu-id="d719a-121">Рабочие процессы **ProcessRunCaller** и **ProcessRunner** создают счета.</span><span class="sxs-lookup"><span data-stu-id="d719a-121">The **ProcessRunCaller** and **ProcessRunner** workflows create invoices.</span></span> <span data-ttu-id="d719a-122">**ProcessRunCaller** вызывает **ProcessRunner**.</span><span class="sxs-lookup"><span data-stu-id="d719a-122">**ProcessRunCaller** calls **ProcessRunner**.</span></span> <span data-ttu-id="d719a-123">Счета фактически создаются рабочим процессом **ProcessRunner**.</span><span class="sxs-lookup"><span data-stu-id="d719a-123">**ProcessRunner** is the workflow that actually creates the invoices.</span></span> <span data-ttu-id="d719a-124">Он перебирает все строки контракта, для которых должны быть созданы счета, и создает счета для этих строк.</span><span class="sxs-lookup"><span data-stu-id="d719a-124">It goes through all the contract lines that invoices must be created for, and it creates invoices for those lines.</span></span> <span data-ttu-id="d719a-125">Чтобы определить строки контракта, для которых должны быть созданы счета, задание проверяет даты запуска счетов для строк контракта.</span><span class="sxs-lookup"><span data-stu-id="d719a-125">To determine the contract lines that invoices must be created for, the job looks at invoice run dates for the contract lines.</span></span> <span data-ttu-id="d719a-126">Если строки контракта, принадлежащие к одному контракту, имеют одинаковую дату запуска счета, транзакции объединяются в один счет с двумя строками счета.</span><span class="sxs-lookup"><span data-stu-id="d719a-126">If contract lines that belong to one contract have the same invoice run date, the transactions are combined into one invoice that has two invoice lines.</span></span> <span data-ttu-id="d719a-127">Если транзакции, для которых требуется создать счета, отсутствуют, задание пропускает создание счета.</span><span class="sxs-lookup"><span data-stu-id="d719a-127">If there are no transactions to create invoices for, the job skips invoice creation.</span></span>

<span data-ttu-id="d719a-128">После завершения работы **ProcessRunner** он вызывает **ProcessRunCaller**, предоставляет время завершения и закрывается.</span><span class="sxs-lookup"><span data-stu-id="d719a-128">After **ProcessRunner** has finished running, it calls **ProcessRunCaller**, provides the end time, and is closed.</span></span> <span data-ttu-id="d719a-129">**ProcessRunCaller** затем запускает таймер, который работает 24 часа с указанного времени завершения.</span><span class="sxs-lookup"><span data-stu-id="d719a-129">**ProcessRunCaller** then starts a timer that runs for 24 hours from the specified end time.</span></span> <span data-ttu-id="d719a-130">По завершении работы таймера процесс **ProcessRunCaller** закрывается.</span><span class="sxs-lookup"><span data-stu-id="d719a-130">At the end of the timer, **ProcessRunCaller** is closed.</span></span>

<span data-ttu-id="d719a-131">Задание пакетной обработки для создания счетов — это повторяющееся задание.</span><span class="sxs-lookup"><span data-stu-id="d719a-131">The batch process job for creating invoices is a recurrent job.</span></span> <span data-ttu-id="d719a-132">Если это процесс пакетной обработки запускается много раз, создается несколько экземпляров задания, что вызывает ошибки.</span><span class="sxs-lookup"><span data-stu-id="d719a-132">If this batch process is run many times, multiple instances of the job are created and cause errors.</span></span> <span data-ttu-id="d719a-133">Следовательно, необходимо запустить пакетный процесс только один раз, и заново запускать его следует только в том случае, если он перестал работать.</span><span class="sxs-lookup"><span data-stu-id="d719a-133">Therefore, you should start the batch process only one time, and you should restart it only if it stops running.</span></span>

> [!NOTE]
> <span data-ttu-id="d719a-134">Пакетное выставление счетов запускается только для строк контракта по проекту, которые настроены с помощью графиков счетов.</span><span class="sxs-lookup"><span data-stu-id="d719a-134">Batch invoicing only runs for project contract lines that are configured by invoice schedules.</span></span> <span data-ttu-id="d719a-135">В строке контракта с методом выставления счетов с фиксированной ценой должны быть настроены вехи.</span><span class="sxs-lookup"><span data-stu-id="d719a-135">A contract line with a fixed price billing method must have milestones configured.</span></span> <span data-ttu-id="d719a-136">Для строки контракта по проекту с методом выставления счетов с учетом времени и материала потребуется настроить расписание счетов на основе даты.</span><span class="sxs-lookup"><span data-stu-id="d719a-136">A project contract line with a time and material billing method will need a date-based invoice schedule set up.</span></span> <span data-ttu-id="d719a-137">То же самое справедливо для строки контракта на основе проекта.</span><span class="sxs-lookup"><span data-stu-id="d719a-137">The same applies to a project-based contract line.</span></span>     
