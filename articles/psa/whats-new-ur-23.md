---
title: Что нового или измененного в выпуске-обновлении 23 для Project Service Automation версии 3
description: В этом разделе перечислены функции и исправления, доступные в выпуске-обновлении 23 для Project Service Automation версии 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: 379379ff643baa10417333b4be5e56d56eb5bc26
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280549"
---
# <a name="project-service-automation-update-release-23-v3"></a><span data-ttu-id="7db36-103">Выпуск-обновление 23 Project Service Automation, версия 3</span><span class="sxs-lookup"><span data-stu-id="7db36-103">Project Service Automation Update Release 23, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="7db36-104">Мы рады объявить о последнем обновлении приложения Project Service Automation для Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="7db36-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="7db36-105">Этот выпуск содержит некоторые важные усовершенствования, направленные на качество, производительность и удобство использования.</span><span class="sxs-lookup"><span data-stu-id="7db36-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="7db36-106">Этот выпуск совместим с Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="7db36-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="7db36-107">Чтобы обновить приложение до этого выпуска, посетите страницу решений Центра администрирования Dynamics 365 Online и установите обновление.</span><span class="sxs-lookup"><span data-stu-id="7db36-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="7db36-108">Дополнительные сведения см. в разделе [Установка, обновление или удаление предпочтительного решения](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="7db36-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="7db36-109">В этом разделе перечислены функции и исправления, появившиеся или изменившиеся в выпуске-обновлении 23 для Project Service Automation версии 3.</span><span class="sxs-lookup"><span data-stu-id="7db36-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 23.</span></span> <span data-ttu-id="7db36-110">У этой версии номер сборки V 3.10.34.30, она становится доступна широкому кругу клиентов посредством самостоятельного обновления в августе 2020 г.</span><span class="sxs-lookup"><span data-stu-id="7db36-110">This version has a build number of V 3.10.34.30 and is generally available through a self-update in August 2020.</span></span>

## <a name="update-release-23"></a><span data-ttu-id="7db36-111">Выпуск-обновление 23</span><span class="sxs-lookup"><span data-stu-id="7db36-111">Update Release 23</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="7db36-112">Исправленные ошибки</span><span class="sxs-lookup"><span data-stu-id="7db36-112">Bug fixes</span></span>

<span data-ttu-id="7db36-113">**Время и расходы**</span><span class="sxs-lookup"><span data-stu-id="7db36-113">**Time and Expense**</span></span>

<span data-ttu-id="7db36-114">Следующие проблемы были исправлены:</span><span class="sxs-lookup"><span data-stu-id="7db36-114">The following issues have been fixed:</span></span>
- <span data-ttu-id="7db36-115">Обработка граничного случая в команде **Удалить участника рабочей группы проекта**, чтобы предоставить значимое исключение.</span><span class="sxs-lookup"><span data-stu-id="7db36-115">Handle edge case in **Project Team Member Delete** to provide a meaningful exception.</span></span>
- <span data-ttu-id="7db36-116">При импорте назначения появляется пустой экран удаления.</span><span class="sxs-lookup"><span data-stu-id="7db36-116">Assignment import results in a blank remove screen.</span></span>

<span data-ttu-id="7db36-117">**Управление ресурсами**</span><span class="sxs-lookup"><span data-stu-id="7db36-117">**Resource Management**</span></span>

<span data-ttu-id="7db36-118">Следующие проблемы были исправлены:</span><span class="sxs-lookup"><span data-stu-id="7db36-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="7db36-119">**Карточка ресурсов сетки использования ресурсов** показывает неверные данные, когда шкала времени больше пяти дней.</span><span class="sxs-lookup"><span data-stu-id="7db36-119">The **Resource utilization grid resource card** shows incorrect data when the time scale is more than five days.</span></span>
- <span data-ttu-id="7db36-120">Когда клиенты создают резервируемый ресурс, подключаемый модуль периодически не может автоматически добавить ресурс в группу Microsoft Office 365.</span><span class="sxs-lookup"><span data-stu-id="7db36-120">When customers create a bookable resource, the plug-in intermittently fails to automatically add the resource to a Microsoft Office 365 group.</span></span>
- <span data-ttu-id="7db36-121">Представление **Выверка** неправильно отображает ручные контуры в представлении **Неделя** или **Месяц**.</span><span class="sxs-lookup"><span data-stu-id="7db36-121">**Reconciliation** view displays manual contours incorrectly in the **Week** or **Month** view.</span></span>

<span data-ttu-id="7db36-122">**Управление проектами**</span><span class="sxs-lookup"><span data-stu-id="7db36-122">**Project Management**</span></span>

<span data-ttu-id="7db36-123">Следующие проблемы были исправлены:</span><span class="sxs-lookup"><span data-stu-id="7db36-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="7db36-124">Чрезмерное количество сущностей **RetrieveMultiple для пользовательских настроек** приводит к снижению производительности для утверждения проектов и других операций.</span><span class="sxs-lookup"><span data-stu-id="7db36-124">An excessive number of **RetrieveMultiple for usersettings** entities are causing degraded performance for project approvals and other operations.</span></span>
- <span data-ttu-id="7db36-125">Подстановка ресурсов сетки **Планирование задач** ограничена отображением не более пяти участников рабочей группы проекта.</span><span class="sxs-lookup"><span data-stu-id="7db36-125">The **Task Planning** grid resource lookup is limited to only show up to five team members from the project team.</span></span> 
- <span data-ttu-id="7db36-126">Подстановка ресурсов сетки **Планирование задач** не фильтрует неактивные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="7db36-126">The **Task Planning** grid resource lookup does not filter inactive resources.</span></span>
- <span data-ttu-id="7db36-127">Ручной режим не работает должным образом в структурной декомпозиции работ в планировании проекта.</span><span class="sxs-lookup"><span data-stu-id="7db36-127">Manual mode is not working as expected in the project planning work breakdown structure.</span></span>
- <span data-ttu-id="7db36-128">В сетке **Планирование задач** отображаются **Категории неактивных транзакций**.</span><span class="sxs-lookup"><span data-stu-id="7db36-128">The **Task Planning** grid shows **Inactive Transaction Categories**.</span></span>
- <span data-ttu-id="7db36-129">В сетке **Назначение ресурсов** округление выполняется неправильно, если задача имеет несколько назначений.</span><span class="sxs-lookup"><span data-stu-id="7db36-129">The **Resource Assignment** grid rounds incorrectly when a task has multiple assignments.</span></span>
- <span data-ttu-id="7db36-130">Значения округления для плановых и фактических затрат для одной задачи различаются.</span><span class="sxs-lookup"><span data-stu-id="7db36-130">Rounding values are different between planned cost and actual cost for a single task.</span></span>

<span data-ttu-id="7db36-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="7db36-131">**Sales**</span></span>

<span data-ttu-id="7db36-132">Следующие проблемы были исправлены:</span><span class="sxs-lookup"><span data-stu-id="7db36-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="7db36-133">При двойном щелчке на пункте **Получить все категории транзакций** создаются несколько строк.</span><span class="sxs-lookup"><span data-stu-id="7db36-133">**Fetch All Transaction Categories** double-click creates multiple lines.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]