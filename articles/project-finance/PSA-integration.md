---
title: Обзор Project Service Automation
description: В этой теме представлена информация о интеграционном решении Dynamics 365 Project Service Automation в Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: 897e1a1c-d31c-42b8-bb59-6b67202d8d61
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 080a545d8713e52d9778367aec1969b815d683e5
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754978"
---
# <a name="project-service-automation-overview"></a><span data-ttu-id="3e7a8-103">Обзор Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="3e7a8-103">Project Service Automation overview</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="3e7a8-104">Решение для интеграции Project Service Automation в Finance использует функцию интеграции данных для синхронизации данных между экземплярами Dynamics 365 Finance и Dynamics 365 Project Service Automation через Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="3e7a8-104">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Dynamics 365 Finance and Dynamics 365 Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="3e7a8-105">Шаблоны интеграции, доступные с функцией интеграции данных, обеспечивают потоки проектов, контракты по проектам, строки контрактов по проектам, вехи строк контрактов проекта, задачи проекта категории транзакций расходов, оценки часов и оценки расходов из Project Service Automation в Finance.</span><span class="sxs-lookup"><span data-stu-id="3e7a8-105">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="3e7a8-106">Если вы используете выпуск версию 7.3.0, вам необходимо установить KB 4074835.</span><span class="sxs-lookup"><span data-stu-id="3e7a8-106">If you're using version 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="3e7a8-107">После этого вы сможете интегрировать проекты с фиксированной ценой.</span><span class="sxs-lookup"><span data-stu-id="3e7a8-107">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="3e7a8-108">Если вы используете версию 7.3.0 и переносите транзакции сборов из Project Service Automation, вы должны установить KB 4345320, чтобы включить эти сборы в счет проекта.</span><span class="sxs-lookup"><span data-stu-id="3e7a8-108">If you're using version 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="3e7a8-109">Если вы используете версию 8.0, вы сможете использовать интеграцию задач проекта, категории транзакций расходов, оценки часов, оценки расходов и блокировку функций.</span><span class="sxs-lookup"><span data-stu-id="3e7a8-109">If you're using version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="3e7a8-110">Если вы используете версию 8.0.1 или новее, вы сможете синхронизировать фактические данные.</span><span class="sxs-lookup"><span data-stu-id="3e7a8-110">If you're using version 8.0.1 or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="3e7a8-111">Прежде чем вы сможете интегрировать Project Service Automation и Finance, вы должны настроить параметры интеграции Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="3e7a8-111">Before you can integrate Project Service Automation Finance, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="3e7a8-112">Для получения дополнительной информации см. [Параметры интеграции Project Service Automation](PSA-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="3e7a8-112">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="3e7a8-113">Это интеграционное решение обеспечивает прямую синхронизацию в следующих сценариях:</span><span class="sxs-lookup"><span data-stu-id="3e7a8-113">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="3e7a8-114">Поддерживайте контракты по проекту в Project Service Automation и синхронизируйте их напрямую из Project Service Automation в Finance.</span><span class="sxs-lookup"><span data-stu-id="3e7a8-114">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="3e7a8-115">Создавайте проекты в Project Service Automation и синхронизируйте их напрямую из Project Service Automation в Finance.</span><span class="sxs-lookup"><span data-stu-id="3e7a8-115">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="3e7a8-116">Поддерживайте строки контрактов по проекту в Project Service Automation и синхронизируйте их напрямую из Project Service Automation в Finance.</span><span class="sxs-lookup"><span data-stu-id="3e7a8-116">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="3e7a8-117">Поддерживайте вехи строк контрактов по проекту в Project Service Automation и синхронизируйте их напрямую из Project Service Automation в Finance.</span><span class="sxs-lookup"><span data-stu-id="3e7a8-117">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="3e7a8-118">Поддерживайте задачи по проекту в Project Service Automation и синхронизируйте их напрямую из Project Service Automation в Finance.</span><span class="sxs-lookup"><span data-stu-id="3e7a8-118">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="3e7a8-119">Поддерживайте категории транзакций расходов в Finance и синхронизируйте их напрямую из Finance в Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="3e7a8-119">Maintain expense transaction categories in Finance, and synchronize them directly from Finance to Project Service Automation.</span></span>
- <span data-ttu-id="3e7a8-120">Создавайте оценки часов проекта в Project Service Automation и синхронизируйте их напрямую из Project Service Automation в Finance.</span><span class="sxs-lookup"><span data-stu-id="3e7a8-120">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="3e7a8-121">Создавайте оценки расходов проекта в Project Service Automation и синхронизируйте их напрямую из Project Service Automation в Finance.</span><span class="sxs-lookup"><span data-stu-id="3e7a8-121">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="3e7a8-122">Создавайте фактические данные о времени, расходах и вознаграждении по проекту в Project Service Automation, а также создавайте транзакции по проекту в журнале интеграции Project Service Automation, чтобы их можно было разнести в Finance.</span><span class="sxs-lookup"><span data-stu-id="3e7a8-122">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="3e7a8-123">Синхронизация данных</span><span class="sxs-lookup"><span data-stu-id="3e7a8-123">Data synchronization</span></span>

<span data-ttu-id="3e7a8-124">На следующем рисунке показано, как данные синхронизируются в рамках интеграции между Project Service Automation и Finance.</span><span class="sxs-lookup"><span data-stu-id="3e7a8-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance.</span></span>

> [!NOTE]
> <span data-ttu-id="3e7a8-125">В настоящее время доступны не все шаблоны.</span><span class="sxs-lookup"><span data-stu-id="3e7a8-125">Not all templates are currently available.</span></span> <span data-ttu-id="3e7a8-126">Шаблоны будут выпускаться по мере их завершения.</span><span class="sxs-lookup"><span data-stu-id="3e7a8-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="3e7a8-127">[![Интеграция Project Service Automation с Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="3e7a8-127">[![Project Service Automation integration with Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance"></a><span data-ttu-id="3e7a8-128">Системные требования для Finance</span><span class="sxs-lookup"><span data-stu-id="3e7a8-128">System requirements for Finance</span></span>

<span data-ttu-id="3e7a8-129">Чтобы использовать решение интеграции Project Service Automation с Finance, необходимо установить выпуск Enterprise Edition 7.3 с обновлением платформы 12 или новее.</span><span class="sxs-lookup"><span data-stu-id="3e7a8-129">To use the Project Service Automation to Finance integration solution, you must install Enterprise edition 7.3 with Platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="3e7a8-130">Системные требования для Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="3e7a8-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="3e7a8-131">Чтобы использовать решение интеграции Project Service Automation с Finance, необходимо установить следующие компоненты:</span><span class="sxs-lookup"><span data-stu-id="3e7a8-131">To use the Project Service Automation to Finance integration solution, you must install the following components:</span></span>

- <span data-ttu-id="3e7a8-132">Dynamics 365 Project Service Automation версии 9.0.0.0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="3e7a8-132">Dynamics 365 Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="3e7a8-133">Решение Prospect to Cash для Dynamics 365 Sales, версия 1.14.0.0 (v14) или более поздняя</span><span class="sxs-lookup"><span data-stu-id="3e7a8-133">Prospect to cash solution for Dynamics 365 Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="3e7a8-134">Решение Project Service Automation и Finance для Dynamics 365 Project Service Automation версии 1.0.0.0 или более поздняя</span><span class="sxs-lookup"><span data-stu-id="3e7a8-134">Project Service Automation to Finance solution for Dynamics 365 Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="3e7a8-135">Установите решение интеграции Project Service Automation с Finance в свой экземпляр Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="3e7a8-135">Install the Project Service Automation to Finance integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="3e7a8-136">Загрузите решение для интеграции Project Service Automation с Finance из [Центра загрузки Microsoft](https://www.microsoft.com/download/details.aspx?id=57016) и следуйте инструкциям, прилагаемым к решению.</span><span class="sxs-lookup"><span data-stu-id="3e7a8-136">Download the Project Service Automation to Finance integration solution from [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>