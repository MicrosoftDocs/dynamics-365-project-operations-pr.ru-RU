---
title: Что нового или измененного в выпуске-обновлении 31 для Project Service Automation версии 3
description: В этом разделе перечислены функции и исправления, доступные в выпуске-обновлении 31 для Project Service Automation версии 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: a595c0a129ac35d3416984e57908e73e1eaef2fd
ms.sourcegitcommit: 6e1498502461e86cff722ccaf8795ff11c7c47ad
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/27/2021
ms.locfileid: "5945551"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a><span data-ttu-id="bac5d-103">Что нового или измененного в выпуске-обновлении 31 для Project Service Automation версии 3</span><span class="sxs-lookup"><span data-stu-id="bac5d-103">What's new or changed in Project Service Automation Update Release 31, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="bac5d-104">Мы рады объявить о последнем обновлении приложения Project Service Automation для Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="bac5d-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="bac5d-105">Этот выпуск содержит некоторые важные усовершенствования, направленные на качество, производительность и удобство использования.</span><span class="sxs-lookup"><span data-stu-id="bac5d-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="bac5d-106">Этот выпуск совместим с Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="bac5d-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="bac5d-107">Чтобы обновить приложение до этого выпуска, посетите страницу решений Центра администрирования Dynamics 365 Online и установите обновление.</span><span class="sxs-lookup"><span data-stu-id="bac5d-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="bac5d-108">Дополнительные сведения см. в разделе [Установка, обновление или удаление предпочтительного решения](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="bac5d-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="bac5d-109">В этом разделе перечислены функции и исправления, появившиеся или изменившиеся в выпуске-обновлении 31 для Project Service Automation версии 3.</span><span class="sxs-lookup"><span data-stu-id="bac5d-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 31.</span></span> <span data-ttu-id="bac5d-110">Эта версия имеет номер сборки V3.10.52.77 и доступна для широкой публики после автоматического обновления в мае 2021 г.</span><span class="sxs-lookup"><span data-stu-id="bac5d-110">This version has a build number of V3.10.52.77 and is generally available through a self-update in May 2021.</span></span>

## <a name="update-release-31"></a><span data-ttu-id="bac5d-111">Выпуск-обновление 31</span><span class="sxs-lookup"><span data-stu-id="bac5d-111">Update Release 31</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="bac5d-112">Исправленные ошибки</span><span class="sxs-lookup"><span data-stu-id="bac5d-112">Bug fixes</span></span>

<span data-ttu-id="bac5d-113">**Время и расходы**</span><span class="sxs-lookup"><span data-stu-id="bac5d-113">**Time and Expense**</span></span>

<span data-ttu-id="bac5d-114">Следующие проблемы были исправлены:</span><span class="sxs-lookup"><span data-stu-id="bac5d-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="bac5d-115">Командные кнопки в элементе управления записи времени на странице **Резервируемый ресурс** были запутанными.</span><span class="sxs-lookup"><span data-stu-id="bac5d-115">Time entry control command buttons on the **Bookable Resource** page were confusing.</span></span>
- <span data-ttu-id="bac5d-116">Исключение нулевой ссылки было создано в **Project.SetTrackingFields** при утверждении записи времени.</span><span class="sxs-lookup"><span data-stu-id="bac5d-116">A null reference exception was generated in **Project.SetTrackingFields** when approving a time entry.</span></span>

<span data-ttu-id="bac5d-117">**Управление ресурсами**</span><span class="sxs-lookup"><span data-stu-id="bac5d-117">**Resource Management**</span></span>

<span data-ttu-id="bac5d-118">Следующие проблемы были исправлены:</span><span class="sxs-lookup"><span data-stu-id="bac5d-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="bac5d-119">**Создать участника рабочей группы** неправильно отображает параметр метаданных настройки резервирования для **Состояние исполненного резервирования по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="bac5d-119">**Create Team Member** doesn't correctly display the booking setup metadata setting for **Default Booking Committed Status**.</span></span>
- <span data-ttu-id="bac5d-120">При обновлении с PSA 1.X до 3.X процесс обновления завершается ошибкой в **UpgradeResourceRequirements**.</span><span class="sxs-lookup"><span data-stu-id="bac5d-120">When upgrading from PSA 1.X to 3.X, the upgrade process fails at **UpgradeResourceRequirements**.</span></span>


<span data-ttu-id="bac5d-121">**Продажи**</span><span class="sxs-lookup"><span data-stu-id="bac5d-121">**Sales**</span></span>

<span data-ttu-id="bac5d-122">Следующие проблемы были исправлены:</span><span class="sxs-lookup"><span data-stu-id="bac5d-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="bac5d-123">Фактический доход конвертирует суммы в валюту проекта в сетке отслеживания.</span><span class="sxs-lookup"><span data-stu-id="bac5d-123">Actual revenue converts the amounts to the project currency in the tracking grid.</span></span>
- <span data-ttu-id="bac5d-124">Валюта по умолчанию неясна при создании строк журнала, строк котировок и строк контрактов в сценариях, где базовая валюта организации отличается от валюты проекта.</span><span class="sxs-lookup"><span data-stu-id="bac5d-124">The currency default is unclear when creating journal lines, quote lines, and contract lines in scenarios where an organization's base currency differs from the project currency.</span></span>
- <span data-ttu-id="bac5d-125">Запрос **Ожидает проверки журнала корректировок** не фильтруется по проекту.</span><span class="sxs-lookup"><span data-stu-id="bac5d-125">**Pending correction journal validation** query doesn't filter by project.</span></span>
- <span data-ttu-id="bac5d-126">Оставшиеся продажи по проекту неправильно рассчитаны.</span><span class="sxs-lookup"><span data-stu-id="bac5d-126">Remaining sales are calculated incorrectly on a project.</span></span>
- <span data-ttu-id="bac5d-127">Предложения с расценками, основанные на контакте, не работают, если они созданы без прайс-листа.</span><span class="sxs-lookup"><span data-stu-id="bac5d-127">Quotes based on a contact fail when they are created without a price list.</span></span>
- <span data-ttu-id="bac5d-128">Когда вы выбираете **Подтвердить счет**, счетчик обработки не отображается.</span><span class="sxs-lookup"><span data-stu-id="bac5d-128">No processing spinner is shown when you select **Confirm Invoice**.</span></span>
- <span data-ttu-id="bac5d-129">Когда вы выбираете **Создать счет**, счетчик обработки не отображается.</span><span class="sxs-lookup"><span data-stu-id="bac5d-129">No processing spinner is shown when you select **Create Invoice**.</span></span>
- <span data-ttu-id="bac5d-130">Закрытие предложения с расценками как утерянного не отменяет резервирования.</span><span class="sxs-lookup"><span data-stu-id="bac5d-130">Closing a quote as lost doesn't cancel the bookings.</span></span>







