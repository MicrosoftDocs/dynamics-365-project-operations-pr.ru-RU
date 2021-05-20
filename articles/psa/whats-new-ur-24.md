---
title: Что нового или измененного в выпуске-обновлении 24 для Project Service Automation версии 3
description: В этом разделе перечислены функции и исправления, доступные в выпуске-обновлении 24 для Project Service Automation версии 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 956dcd2a06fad1eec488ad81bec2de4bd0550e82
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948931"
---
# <a name="project-service-automation-update-release-24-v3"></a><span data-ttu-id="bedc8-103">Выпуск-обновление 24 Project Service Automation, версия 3</span><span class="sxs-lookup"><span data-stu-id="bedc8-103">Project Service Automation Update Release 24, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="bedc8-104">Мы рады объявить о последнем обновлении приложения Project Service Automation для Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="bedc8-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="bedc8-105">Этот выпуск содержит некоторые важные усовершенствования, направленные на качество, производительность и удобство использования.</span><span class="sxs-lookup"><span data-stu-id="bedc8-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="bedc8-106">Этот выпуск совместим с Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="bedc8-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="bedc8-107">Чтобы обновить приложение до этого выпуска, посетите страницу решений Центра администрирования Dynamics 365 Online и установите обновление.</span><span class="sxs-lookup"><span data-stu-id="bedc8-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="bedc8-108">Дополнительные сведения см. в разделе [Установка, обновление или удаление предпочтительного решения](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="bedc8-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="bedc8-109">В этом разделе перечислены функции и исправления, появившиеся или изменившиеся в выпуске-обновлении 24 для Project Service Automation версии 3.</span><span class="sxs-lookup"><span data-stu-id="bedc8-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 24.</span></span> <span data-ttu-id="bedc8-110">У этой версии номер сборки V 3.10.42.43, она становится доступна широкому кругу клиентов посредством самостоятельного обновления в октябре 2020 г.</span><span class="sxs-lookup"><span data-stu-id="bedc8-110">This version has a build number of V 3.10.42.43 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-24"></a><span data-ttu-id="bedc8-111">Выпуск-обновление 24</span><span class="sxs-lookup"><span data-stu-id="bedc8-111">Update Release 24</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="bedc8-112">Исправленные ошибки</span><span class="sxs-lookup"><span data-stu-id="bedc8-112">Bug fixes</span></span>

<span data-ttu-id="bedc8-113">**Sales**</span><span class="sxs-lookup"><span data-stu-id="bedc8-113">**Sales**</span></span>

<span data-ttu-id="bedc8-114">Следующие проблемы были исправлены:</span><span class="sxs-lookup"><span data-stu-id="bedc8-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="bedc8-115">Проблема при установке прайс-листа по умолчанию для продуктов.</span><span class="sxs-lookup"><span data-stu-id="bedc8-115">Problem while setting default price list of products.</span></span>
- <span data-ttu-id="bedc8-116">Производительность реализации предложения с расценками низкая из-за встроенного прайс-листа и копии записей расценок для ролей.</span><span class="sxs-lookup"><span data-stu-id="bedc8-116">Performance of Quote win is slow due to the embedded price list and role price records copy.</span></span>
- <span data-ttu-id="bedc8-117">**Контракт по проекту/Центр продаж** > **Позиция строки продукта/количество в строке заказа** автоматически округляется до ближайшего целого числа.</span><span class="sxs-lookup"><span data-stu-id="bedc8-117">**Project Contract/Sales Hub** > **Product Line Item/Order Line Quantity** is automatically rounded to the nearest integer.</span></span>
- <span data-ttu-id="bedc8-118">Получите системные привилегии при чтении прайс-листов.</span><span class="sxs-lookup"><span data-stu-id="bedc8-118">Elevate to system privileges when reading price lists.</span></span>
- <span data-ttu-id="bedc8-119">Скопируйте поля адреса клиента **address1_freighttermscode** и **address1_shippingmethodcode** в предложение с расценками/заказ.</span><span class="sxs-lookup"><span data-stu-id="bedc8-119">Copy customer address fields **address1_freighttermscode** and **address1_shippingmethodcode** to Quote/Order.</span></span> 


<span data-ttu-id="bedc8-120">**Время и расходы**</span><span class="sxs-lookup"><span data-stu-id="bedc8-120">**Time and Expense**</span></span>

<span data-ttu-id="bedc8-121">Следующие проблемы были исправлены:</span><span class="sxs-lookup"><span data-stu-id="bedc8-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="bedc8-122">**Сетка записи времени** не поддерживает временное поведение **Только дата**.</span><span class="sxs-lookup"><span data-stu-id="bedc8-122">The **Time Entry Grid** doesn't support **Date Only** time behavior.</span></span>
- <span data-ttu-id="bedc8-123">**Запись времени** не обновляется автоматически.</span><span class="sxs-lookup"><span data-stu-id="bedc8-123">**Time Entry** is not refreshing automatically.</span></span> <span data-ttu-id="bedc8-124">Требуется ручное обновление.</span><span class="sxs-lookup"><span data-stu-id="bedc8-124">A manual refresh is required.</span></span>
- <span data-ttu-id="bedc8-125">Невозможно импортировать записи времени из назначения, когда есть перерыв (0 часов) в назначениях ресурса.</span><span class="sxs-lookup"><span data-stu-id="bedc8-125">Unable to import the time entries from an assignment when there is a break (0 hours) in a resource's assignments.</span></span>
- <span data-ttu-id="bedc8-126">При создании записи времени установите начало так же, как **msdyn_date**.</span><span class="sxs-lookup"><span data-stu-id="bedc8-126">When creating a time entry, set the start to the same as **msdyn_date**.</span></span>
- <span data-ttu-id="bedc8-127">Повторно включите массовое редактирование для записи времени.</span><span class="sxs-lookup"><span data-stu-id="bedc8-127">Re-enable bulk edit for time entry.</span></span>

<span data-ttu-id="bedc8-128">**Управление ресурсами**</span><span class="sxs-lookup"><span data-stu-id="bedc8-128">**Resource Management**</span></span>

<span data-ttu-id="bedc8-129">Следующие проблемы были исправлены:</span><span class="sxs-lookup"><span data-stu-id="bedc8-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="bedc8-130">Попытка обновить статус резервирования, охватывающего несколько дней, без требования вызовет исключение ссылки NULL.</span><span class="sxs-lookup"><span data-stu-id="bedc8-130">Trying to update the status of an inter-day booking without a requirement will throw a null-ref exception.</span></span>
- <span data-ttu-id="bedc8-131">Ошибка при загрузке **Представления выверки**.</span><span class="sxs-lookup"><span data-stu-id="bedc8-131">Error loading the **Reconciliation View**.</span></span>


<span data-ttu-id="bedc8-132">**Управление проектами**</span><span class="sxs-lookup"><span data-stu-id="bedc8-132">**Project Management**</span></span>

<span data-ttu-id="bedc8-133">Следующие проблемы были исправлены:</span><span class="sxs-lookup"><span data-stu-id="bedc8-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="bedc8-134">В **Расписании проекта** при изменении с **Вручную** на **Авто** автосохранение не завершается.</span><span class="sxs-lookup"><span data-stu-id="bedc8-134">In the **Project Schedule**, when changing from **Manual** to **Auto**, auto save is not completing.</span></span>
- <span data-ttu-id="bedc8-135">Значения себестоимости расходов не должны рассчитываться в сторону дисперсии на **Сетке отслеживания проектов**.</span><span class="sxs-lookup"><span data-stu-id="bedc8-135">Expense costs should not calculate toward variance on the **Project Tracking Grid**.</span></span>
- <span data-ttu-id="bedc8-136">Непоследовательное поведение для столбцов **Тег оценок** во время загрузки по сравнению с изменением типа **Повременное**.</span><span class="sxs-lookup"><span data-stu-id="bedc8-136">Inconsistent behavior for **Estimates tag** columns during load versus changing the **Time-Phase** type.</span></span>
- <span data-ttu-id="bedc8-137">Фактическая себестоимость в проекте может не отражать итоговые суммы от раздела **Фактические значения**.</span><span class="sxs-lookup"><span data-stu-id="bedc8-137">The actual cost on a project may not reflect the totals from **Actuals**.</span></span>
- <span data-ttu-id="bedc8-138">**Предполагаемая дата окончания** на вкладке **Сводка** не соответствует значению **Расписание WBS**.</span><span class="sxs-lookup"><span data-stu-id="bedc8-138">**Estimated Finish Date** on the **Summary** tab does not match the **WBS Schedule**.</span></span>
- <span data-ttu-id="bedc8-139">**Обновить фактические часы** на повышении уровня работает некорректно.</span><span class="sxs-lookup"><span data-stu-id="bedc8-139">**Update Actual Hours** on outdent does not work correctly.</span></span>
- <span data-ttu-id="bedc8-140">Менеджер проекта вне корневого **подразделения** не может создать проект.</span><span class="sxs-lookup"><span data-stu-id="bedc8-140">A Project manager outside of root **BU** can't create a project.</span></span>
- <span data-ttu-id="bedc8-141">Изменения в задаче или категории в разделе **Оценки расходов** не сохраняются.</span><span class="sxs-lookup"><span data-stu-id="bedc8-141">Changes to task or category on **Expense Estimates** are not persisted.</span></span>
- <span data-ttu-id="bedc8-142">**Копировать контракт** копирует графики счетов и статус выполнения.</span><span class="sxs-lookup"><span data-stu-id="bedc8-142">**Copy of contract** copies the invoice schedules and the run status.</span></span>
- <span data-ttu-id="bedc8-143">Кнопка **Обновить фактические данные** неправильно рассчитывает суммарные задачи.</span><span class="sxs-lookup"><span data-stu-id="bedc8-143">**Refresh Actuals** button incorrectly calculates summary tasks.</span></span>
- <span data-ttu-id="bedc8-144">Надстройка Microsoft Project: исправьте ошибку ссылки NULL, если какой-либо участник рабочей группы имеет пустую единицу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bedc8-144">Microsoft Project Add-in: Fix null reference error if any team member has an empty resourcing unit.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]