---
title: Синхронизируйте задачи проекта напрямую из Project Service Automation с Finance and Operations
description: В этой теме описаны шаблон и базовая задачи, которые используются для синхронизации задач проекта непосредственно из Microsoft Dynamics 365 Project Service Automation с Dynamics 365 Finance.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 7cc9ee9de576549c132e14c333a1000c22a55236
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288935"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="0940e-103">Синхронизируйте задачи проекта напрямую из Project Service Automation с Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="0940e-103">Synchronize project tasks directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="0940e-104">В этой теме описаны шаблон и базовая задачи, которые используются для синхронизации задач проекта непосредственно из Dynamics 365 Project Service Automation с Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="0940e-104">This topic describes the template and underlying task that are used to synchronize project tasks directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="0940e-105">Интеграция задач проекта, категории транзакций расходов, оценки часов, оценки расходов и блокировка функций доступны в версии 8.0.</span><span class="sxs-lookup"><span data-stu-id="0940e-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="0940e-106">Если вы используете версию Enterprise Edition 7.3.0 после установки KB 4132657 и KB 4132660, вы сможете использовать шаблоны для интеграции задач проекта, категорий транзакций расходов, часовых оценок, оценок расходов и фактических данных, а также для настройки блокировки функций.</span><span class="sxs-lookup"><span data-stu-id="0940e-106">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="0940e-107">Если вам необходимо сбросить распределения по счетам, мы рекомендуем также установить KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="0940e-107">If you must reset the accounting distributions, we recommended that you also install KB 4131710.</span></span>
> - <span data-ttu-id="0940e-108">Интеграция фактических данных по проекту доступна в версии 8.0.1 и последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="0940e-108">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="0940e-109">Поток данных для Project Service Automation в Finance</span><span class="sxs-lookup"><span data-stu-id="0940e-109">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="0940e-110">Решение для интеграции Project Service Automation в Finance использует функцию интеграции данных для синхронизации данных между экземплярами Project Service Automation и Finance.</span><span class="sxs-lookup"><span data-stu-id="0940e-110">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="0940e-111">Шаблон интеграции, доступный с функцией интеграции данных, позволяет передавать данные о задачах проекта из Project Service Automation в Finance.</span><span class="sxs-lookup"><span data-stu-id="0940e-111">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance.</span></span>

<span data-ttu-id="0940e-112">На следующем рисунке показано, как данные синхронизируются между Project Service Automation и Finance.</span><span class="sxs-lookup"><span data-stu-id="0940e-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="0940e-113">[![Поток данных для интеграции Project Service Automation с Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="0940e-113">[![Data flow for Project Service Automation integration with Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="0940e-114">Шаблон и задача</span><span class="sxs-lookup"><span data-stu-id="0940e-114">Template and task</span></span>

<span data-ttu-id="0940e-115">Чтобы получить доступ к шаблону, в центре администрирования Microsoft Power Apps выберите **Проекты**, а затем в правом верхнем углу выберите **Создать проект** для выбора общедоступных шаблонов.</span><span class="sxs-lookup"><span data-stu-id="0940e-115">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="0940e-116">Следующий шаблон и базовая задача используются для синхронизации задач проекта из Project Service Automation в Finance:</span><span class="sxs-lookup"><span data-stu-id="0940e-116">The following template and underlying task are used to synchronize project tasks from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="0940e-117">**Название шаблона в интеграции данных:** задачи проекта (из PSA в Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="0940e-117">**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="0940e-118">**Название задачи в проекте:** задачи проекта</span><span class="sxs-lookup"><span data-stu-id="0940e-118">**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="0940e-119">Перед синхронизацией задач проекта вы должны синхронизировать контракты и проекты.</span><span class="sxs-lookup"><span data-stu-id="0940e-119">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="0940e-120">Набор сущностей</span><span class="sxs-lookup"><span data-stu-id="0940e-120">Entity set</span></span>

| <span data-ttu-id="0940e-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="0940e-121">Project Service Automation</span></span> | <span data-ttu-id="0940e-122">Финансы</span><span class="sxs-lookup"><span data-stu-id="0940e-122">Finance</span></span>                             |
|----------------------------|-------------------------------------|
| <span data-ttu-id="0940e-123">Задачи проекта</span><span class="sxs-lookup"><span data-stu-id="0940e-123">Project Tasks</span></span>              | <span data-ttu-id="0940e-124">Сущность интеграции для задачи проекта</span><span class="sxs-lookup"><span data-stu-id="0940e-124">Integration entity for project task</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="0940e-125">Поток сущностей</span><span class="sxs-lookup"><span data-stu-id="0940e-125">Entity flow</span></span>

<span data-ttu-id="0940e-126">Задачи проекта управляются в Project Service Automation и синхронизируются с Finance как действия проекта.</span><span class="sxs-lookup"><span data-stu-id="0940e-126">Project tasks are managed in Project Service Automation, and they are synchronized to Finance as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="0940e-127">Предварительные условия и настройка сопоставления</span><span class="sxs-lookup"><span data-stu-id="0940e-127">Prerequisites and mapping setup</span></span>

<span data-ttu-id="0940e-128">Перед синхронизацией задач проекта вы должны синхронизировать контракты и проекты.</span><span class="sxs-lookup"><span data-stu-id="0940e-128">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="0940e-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="0940e-129">Power Query</span></span>

<span data-ttu-id="0940e-130">Вы должны использовать Microsoft Power Query для Excel для фильтрации данных, если выполняется следующее условие:</span><span class="sxs-lookup"><span data-stu-id="0940e-130">You must use Microsoft Power Query for Excel to filter data if this condition is met:</span></span>

- <span data-ttu-id="0940e-131">У вас есть записи о конкретных ресурсах в задаче проекта.</span><span class="sxs-lookup"><span data-stu-id="0940e-131">You have resource-specific records in a project task.</span></span>

<span data-ttu-id="0940e-132">Если вам необходимо использовать Power Query, следуйте этим рекомендациям:</span><span class="sxs-lookup"><span data-stu-id="0940e-132">If you must use Power Query, follow this guideline:</span></span>

- <span data-ttu-id="0940e-133">В шаблоне задач проекта (из PSA в Fin and Ops) есть фильтр по умолчанию, который исключает связанные с ресурсами записи из задачи проекта, устанавливая фильтр для **IsLineTask** как **False**.</span><span class="sxs-lookup"><span data-stu-id="0940e-133">The Project tasks (PSA to Fin and Ops) template has a default filter that excludes resource-specific records from a project task by setting the filter on **IsLineTask** to **False**.</span></span> <span data-ttu-id="0940e-134">Если вы создаете свой собственный шаблон, вы должны добавить этот фильтр.</span><span class="sxs-lookup"><span data-stu-id="0940e-134">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="0940e-135">Сопоставление шаблонов в интеграции данных</span><span class="sxs-lookup"><span data-stu-id="0940e-135">Template mapping in Data integration</span></span>

<span data-ttu-id="0940e-136">На следующих рисунках показан пример сопоставления задач шаблона в интеграции данных.</span><span class="sxs-lookup"><span data-stu-id="0940e-136">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="0940e-137">В сопоставлении отображается информация о полях, которые будут синхронизированы из Project Service Automation в Finance.</span><span class="sxs-lookup"><span data-stu-id="0940e-137">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="0940e-138">[![Сопоставление шаблонов](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="0940e-138">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]