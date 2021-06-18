---
title: Что нового или измененного в выпуске-обновлении 30 для Project Service Automation версии 3
description: В этом разделе перечислены функции и исправления, доступные в выпуске-обновлении 30 для Project Service Automation версии 3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: 3b6b7dba9c2a22587d27006b9972c950fbb454f2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010442"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a><span data-ttu-id="164bc-103">Что нового или измененного в выпуске-обновлении 30 для Project Service Automation версии 3</span><span class="sxs-lookup"><span data-stu-id="164bc-103">What's new or changed in Project Service Automation Update Release 30, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="164bc-104">Мы рады объявить о последнем обновлении приложения Project Service Automation для Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="164bc-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="164bc-105">Этот выпуск содержит некоторые важные усовершенствования, направленные на качество, производительность и удобство использования.</span><span class="sxs-lookup"><span data-stu-id="164bc-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="164bc-106">Этот выпуск совместим с Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="164bc-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="164bc-107">Чтобы обновить приложение до этого выпуска, посетите страницу решений Центра администрирования Dynamics 365 Online и установите обновление.</span><span class="sxs-lookup"><span data-stu-id="164bc-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="164bc-108">Дополнительные сведения см. в разделе [Установка, обновление или удаление предпочтительного решения](/power-platform/admin/install-remove-preferred-solution.md).</span><span class="sxs-lookup"><span data-stu-id="164bc-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution.md).</span></span>

<span data-ttu-id="164bc-109">В этом разделе перечислены функции и исправления, появившиеся или изменившиеся в выпуске-обновлении 30 для Project Service Automation версии 3.</span><span class="sxs-lookup"><span data-stu-id="164bc-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 30.</span></span> <span data-ttu-id="164bc-110">Эта версия имеет номер сборки V3.10.51.61 и доступна для широкой публики после автоматического обновления в апреле 2021 г.</span><span class="sxs-lookup"><span data-stu-id="164bc-110">This version has a build number of V3.10.51.61 and is generally available through a self-update in April 2021.</span></span>

## <a name="update-release-30"></a><span data-ttu-id="164bc-111">Выпуск-обновление 30</span><span class="sxs-lookup"><span data-stu-id="164bc-111">Update Release 30</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="164bc-112">Исправленные ошибки</span><span class="sxs-lookup"><span data-stu-id="164bc-112">Bug fixes</span></span>

<span data-ttu-id="164bc-113">**Время и расходы**</span><span class="sxs-lookup"><span data-stu-id="164bc-113">**Time and Expense**</span></span>

<span data-ttu-id="164bc-114">Следующие проблемы были исправлены:</span><span class="sxs-lookup"><span data-stu-id="164bc-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="164bc-115">Ошибка возникает, когда вы создаете и сохраняете запись времени на странице **Быстрое создание**, если поле **Роль** удалено.</span><span class="sxs-lookup"><span data-stu-id="164bc-115">An error occurs when you create and save a time entry on the **Quick Create** page if the **Role** field is removed.</span></span>
- <span data-ttu-id="164bc-116">Фильтр "Запись времени" применяет неправильный оператор фильтра.</span><span class="sxs-lookup"><span data-stu-id="164bc-116">The Time Entry filter applies the wrong filter operator.</span></span>
- <span data-ttu-id="164bc-117">Скопированные табели учета рабочего времени не отображаются автоматически, когда вы выбираете **Копировать неделю** в элементе управления записи времени.</span><span class="sxs-lookup"><span data-stu-id="164bc-117">Copied timesheets aren't automatically displayed when you select **Copy Week** on the time entry control.</span></span>

<span data-ttu-id="164bc-118">**Управление ресурсами**</span><span class="sxs-lookup"><span data-stu-id="164bc-118">**Resource Management**</span></span>

<span data-ttu-id="164bc-119">Следующие проблемы были исправлены:</span><span class="sxs-lookup"><span data-stu-id="164bc-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="164bc-120">При продлении резервирования статус резервирования, присвоенный окончательному резервированию, неверен.</span><span class="sxs-lookup"><span data-stu-id="164bc-120">When you extend a booking, the booking status assigned to the hard booking is incorrect.</span></span> <span data-ttu-id="164bc-121">При продлении резервирования учитывается статус резервирования, определенный как **Выделено** в метаданных настройки резервирования.</span><span class="sxs-lookup"><span data-stu-id="164bc-121">Extending a booking respects the booking status defined as **Committed** in the booking setup metadata.</span></span>
- <span data-ttu-id="164bc-122">Если допустимый статус резервирования не указан, сообщение об ошибке локализовано неправильно.</span><span class="sxs-lookup"><span data-stu-id="164bc-122">When a valid booking status isn't specified, the error message is not correctly localized.</span></span>

<span data-ttu-id="164bc-123">**Управление проектами**</span><span class="sxs-lookup"><span data-stu-id="164bc-123">**Project Management**</span></span>

<span data-ttu-id="164bc-124">Следующие проблемы были исправлены:</span><span class="sxs-lookup"><span data-stu-id="164bc-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="164bc-125">Проекты нельзя создавать в одной валюте и включать связанные задачи в другой валюте.</span><span class="sxs-lookup"><span data-stu-id="164bc-125">Projects can't be created in one currency and include related tasks in another currency.</span></span>

<span data-ttu-id="164bc-126">**Продажи**</span><span class="sxs-lookup"><span data-stu-id="164bc-126">**Sales**</span></span>

<span data-ttu-id="164bc-127">Следующие проблемы были исправлены:</span><span class="sxs-lookup"><span data-stu-id="164bc-127">The following issues have been fixed:</span></span>

- <span data-ttu-id="164bc-128">При копировании прайс-листа цены не обновляются.</span><span class="sxs-lookup"><span data-stu-id="164bc-128">When a price list is copied, prices aren't updated.</span></span>
- <span data-ttu-id="164bc-129">Закрытие предложения с расценками как выигранного не удается, если у сведений о стоимости есть значение для происхождения.</span><span class="sxs-lookup"><span data-stu-id="164bc-129">Closing a quote as won fails when the cost detail has a value for origin.</span></span>
- <span data-ttu-id="164bc-130">В сущности **Задача проекта** **Предполагаемая стоимость** переименовано в **Запланированная стоимость (базовая)**.</span><span class="sxs-lookup"><span data-stu-id="164bc-130">On the **Project Task** entity, **Estimated Cost** has been renamed to **Planned Cost (Base)**.</span></span>
- <span data-ttu-id="164bc-131">Исключение нулевой ссылки выдается при создании или удалении счетов.</span><span class="sxs-lookup"><span data-stu-id="164bc-131">A null reference exception is generated when invoices are created or deleted.</span></span>
