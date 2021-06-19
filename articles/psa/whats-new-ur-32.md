---
title: Что нового или измененного в выпуске-обновлении 32 для Project Service Automation версии 3
description: В этом разделе перечислены функции и исправления, доступные в выпуске-обновлении 32 для Project Service Automation версии 3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
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
ms.openlocfilehash: 11bf451ef4f24e2301ffde4f86a556a8a4fe30b0
ms.sourcegitcommit: 886102894244887d72e5a6213071e8d8a52c9d48
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129682"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a><span data-ttu-id="54eb5-103">Что нового или измененного в выпуске-обновлении 32 для Project Service Automation версии 3</span><span class="sxs-lookup"><span data-stu-id="54eb5-103">What's new or changed in Project Service Automation Update Release 32, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="54eb5-104">Мы рады объявить о последнем обновлении для приложения Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="54eb5-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="54eb5-105">Этот выпуск содержит некоторые важные усовершенствования, направленные на качество, производительность и удобство использования.</span><span class="sxs-lookup"><span data-stu-id="54eb5-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="54eb5-106">Он совместим с Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="54eb5-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="54eb5-107">Чтобы выполнить обновление до этого выпуска, посетите страницу центра администрирования для онлайн-решений Dynamics 365 и установите обновление.</span><span class="sxs-lookup"><span data-stu-id="54eb5-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="54eb5-108">Дополнительные сведения см. в разделе [Установка, обновление или удаление предпочтительного решения](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="54eb5-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="54eb5-109">В этом разделе перечислены функции и исправления, появившиеся или изменившиеся в выпуске-обновлении 32 для Project Service Automation версии 3.</span><span class="sxs-lookup"><span data-stu-id="54eb5-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 32.</span></span> <span data-ttu-id="54eb5-110">Эта версия имеет номер сборки V3.10.53.108 и обычно доступна через самостоятельное обновление в июне 2021 года.</span><span class="sxs-lookup"><span data-stu-id="54eb5-110">This version has a build number of V3.10.53.108 and is generally available through a self-update in June 2021.</span></span>

## <a name="update-release-32"></a><span data-ttu-id="54eb5-111">Выпуск-обновление 32</span><span class="sxs-lookup"><span data-stu-id="54eb5-111">Update Release 32</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="54eb5-112">Исправленные ошибки</span><span class="sxs-lookup"><span data-stu-id="54eb5-112">Bug fixes</span></span>

#### <a name="general"></a><span data-ttu-id="54eb5-113">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="54eb5-113">General</span></span>

- <span data-ttu-id="54eb5-114">В случае сбоя крупного обновления следует заблокировать только основные точки входа приложения, чтобы обеспечить доступность общих объектов.</span><span class="sxs-lookup"><span data-stu-id="54eb5-114">When a major upgrade fails, only the main application entry points should be blocked, to ensure that shared entities are still accessible.</span></span>

#### <a name="time-and-expense"></a><span data-ttu-id="54eb5-115">Время и расходы</span><span class="sxs-lookup"><span data-stu-id="54eb5-115">Time and Expense</span></span>

<span data-ttu-id="54eb5-116">Следующие проблемы были исправлены:</span><span class="sxs-lookup"><span data-stu-id="54eb5-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="54eb5-117">**TimeEntriesImportFromResourceAssignment** не поддерживает время начала и окончания сегмента контура назначения ресурсов.</span><span class="sxs-lookup"><span data-stu-id="54eb5-117">**TimeEntriesImportFromResourceAssignment** doesn't maintain the start and end times of the resource assignment contour slice.</span></span>
- <span data-ttu-id="54eb5-118">Когда вы выбираете **Открыть запись** в сетке **Запись времени**, вам может быть запрещено выбирать другие формы.</span><span class="sxs-lookup"><span data-stu-id="54eb5-118">When you select **Open Entry** on the **Time Entry** grid, you might be prevented from selecting other forms.</span></span>
- <span data-ttu-id="54eb5-119">Пока вы импортируете назначения для записей времени, запрос клиентского кода может генерировать длинный URL-адрес, который вызывает сбой запроса.</span><span class="sxs-lookup"><span data-stu-id="54eb5-119">While you import assignments to time entries, the client code query could generate a long URL that fails the query.</span></span>
- <span data-ttu-id="54eb5-120">В сетке **Запись времени** после удаления значения из ячейки фокус не остается в сетке.</span><span class="sxs-lookup"><span data-stu-id="54eb5-120">In the **Time Entry** grid, after a value is deleted from a cell, the focus doesn't remain in the grid.</span></span>
- <span data-ttu-id="54eb5-121">Кнопка **Отклонить** была удалена из представления **Утверждения в обработке** для современных разрешений.</span><span class="sxs-lookup"><span data-stu-id="54eb5-121">The **Reject** button has been removed from the **Processing approvals** view for modern approvals.</span></span>
- <span data-ttu-id="54eb5-122">На стабильность и производительность массового утверждения записей времени влияют тупиковые ситуации и неспособность надлежащим образом обрабатывать настройки, связанные с сущностью **Запись времени**.</span><span class="sxs-lookup"><span data-stu-id="54eb5-122">The stability and performance of time entry bulk approval are affected by deadlocks and a failure to appropriately handle customizations that are related to the **Time Entry** entity.</span></span>

#### <a name="project-planning"></a><span data-ttu-id="54eb5-123">Планирование проектов</span><span class="sxs-lookup"><span data-stu-id="54eb5-123">Project Planning</span></span>

- <span data-ttu-id="54eb5-124">Исключение нулевой ссылки создается при обновлении проекта, имеющего нулевое значение в поле **Единица по контракту**.</span><span class="sxs-lookup"><span data-stu-id="54eb5-124">A null reference exception is generated when you update a project that has a null value in the **Contracting Unit** field.</span></span>
- <span data-ttu-id="54eb5-125">**Обновить итоги проекта** неправильно рассчитывает оставшуюся стоимость и оставшиеся продажи по проекту.</span><span class="sxs-lookup"><span data-stu-id="54eb5-125">**Refresh Project Totals** incorrectly calculates the remaining cost and remaining sales on a project.</span></span>
- <span data-ttu-id="54eb5-126">Избыточные расчеты цен влияют на производительность, связанную с обновлениями контуров назначения ресурсов.</span><span class="sxs-lookup"><span data-stu-id="54eb5-126">Redundant pricing calculations affect performance that is related to updates on resource assignment contours.</span></span>

#### <a name="resource-management"></a><span data-ttu-id="54eb5-127">Управление ресурсами</span><span class="sxs-lookup"><span data-stu-id="54eb5-127">Resource Management</span></span>

<span data-ttu-id="54eb5-128">Следующая ошибка была исправлена:</span><span class="sxs-lookup"><span data-stu-id="54eb5-128">The following issue has been fixed:</span></span>

- <span data-ttu-id="54eb5-129">Когда календарная емкость ресурса, доступного для бронирования, превышает 1, Project Service Automation неправильно распознает емкость как 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="54eb5-129">When a bookable resource's calendar capacity is more than 1, Project Service Automation incorrectly recognizes the capacity as 0 (zero).</span></span> <span data-ttu-id="54eb5-130">Следовательно, в представлении расписания возникает бесконечный цикл.</span><span class="sxs-lookup"><span data-stu-id="54eb5-130">Therefore, an infinite loop occurs in the schedule view.</span></span>

#### <a name="sales"></a><span data-ttu-id="54eb5-131">Продажи</span><span class="sxs-lookup"><span data-stu-id="54eb5-131">Sales</span></span>

<span data-ttu-id="54eb5-132">Следующие проблемы были исправлены:</span><span class="sxs-lookup"><span data-stu-id="54eb5-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="54eb5-133">Когда создается строка журнала с настраиваемым типом транзакции, возникает следующее исключение нулевой ссылки: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType (TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span><span class="sxs-lookup"><span data-stu-id="54eb5-133">When a journal line is created that has a custom transaction type, the following null reference exception occurs: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span></span>
- <span data-ttu-id="54eb5-134">Не добавляйте деактивированные роли и категории перед копированием предложения с расценками в оплачиваемые роли и категории вновь скопированного предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="54eb5-134">Roles and categories that are inactivated before a quotation is copied should not be added to chargeable roles and categories of the newly copied quotation.</span></span>
- <span data-ttu-id="54eb5-135">Дата документа и дата учета не согласованы с датой начала, которая указана в сведениях строки счета-фактуры, которая создается непосредственно в черновике счета-фактуры.</span><span class="sxs-lookup"><span data-stu-id="54eb5-135">The document date and accounting date aren't aligned with the start date that is provided on an invoice line detail that is created directly on a draft invoice.</span></span>
- <span data-ttu-id="54eb5-136">Исключения нулевых ссылок создаются в сценариях, связанных с деактивацией ролей и категорий перед копированием предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="54eb5-136">Null reference exceptions are generated in scenarios that are related to inactivation of roles and categories before a quotation is copied.</span></span>
- <span data-ttu-id="54eb5-137">Действие **Обновить цены** на странице **Проекты** не обновляет оценки расходов и оценки материалов.</span><span class="sxs-lookup"><span data-stu-id="54eb5-137">The **Update Prices** action on the **Projects** page doesn't update expense estimates and material estimates.</span></span>
