---
title: Что нового или измененного в выпуске-обновлении 28 для Project Service Automation версии версии 3
description: В этом разделе перечислены функции и исправления, доступные в выпуске-обновлении 28 для Project Service Automation версии версии 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.openlocfilehash: 079679302b2d8dac3074732b2392a7b811ac9711
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280234"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a><span data-ttu-id="8f84f-103">Что нового или измененного в выпуске-обновлении 28 для Project Service Automation версии версии 3</span><span class="sxs-lookup"><span data-stu-id="8f84f-103">What's new or changed in Project Service Automation Update Release 28, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="8f84f-104">Мы рады объявить о последнем обновлении приложения Project Service Automation для Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="8f84f-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="8f84f-105">Этот выпуск содержит некоторые важные усовершенствования, направленные на качество, производительность и удобство использования.</span><span class="sxs-lookup"><span data-stu-id="8f84f-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="8f84f-106">Этот выпуск совместим с Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="8f84f-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="8f84f-107">Чтобы обновить приложение до этого выпуска, посетите страницу решений Центра администрирования Dynamics 365 Online и установите обновление.</span><span class="sxs-lookup"><span data-stu-id="8f84f-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="8f84f-108">Дополнительные сведения см. в разделе [Установка, обновление или удаление предпочтительного решения](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="8f84f-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="8f84f-109">В этой теме перечислены новые или измененные функции и исправления для Project Service Automation версии 3, выпуск-обновление 28. Эта версия имеет номер сборки версии 3.10.46.32 и она общедоступна через самообновление в январе 2021 года.</span><span class="sxs-lookup"><span data-stu-id="8f84f-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 28 This version has a build number of V3.10.46.32 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-28"></a><span data-ttu-id="8f84f-110">Выпуск-обновление 28</span><span class="sxs-lookup"><span data-stu-id="8f84f-110">Update Release 28</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="8f84f-111">Исправленные ошибки</span><span class="sxs-lookup"><span data-stu-id="8f84f-111">Bug fixes</span></span>

<span data-ttu-id="8f84f-112">**Время и расходы**</span><span class="sxs-lookup"><span data-stu-id="8f84f-112">**Time and Expense**</span></span>

<span data-ttu-id="8f84f-113">Следующие проблемы были исправлены:</span><span class="sxs-lookup"><span data-stu-id="8f84f-113">The following issues have been fixed:</span></span>

- <span data-ttu-id="8f84f-114">Пользователи могут использовать **Групповое редактирование** для обновления записей времени, которые были утверждены и отправлены.</span><span class="sxs-lookup"><span data-stu-id="8f84f-114">Users can use **Bulk Edit** to update time entries that have been approved and submitted.</span></span>

<span data-ttu-id="8f84f-115">**Управление проектами**</span><span class="sxs-lookup"><span data-stu-id="8f84f-115">**Project Management**</span></span>

<span data-ttu-id="8f84f-116">Следующие проблемы были исправлены:</span><span class="sxs-lookup"><span data-stu-id="8f84f-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="8f84f-117">В случаях, когда GUID задачи интерпретируется как число, задачи нельзя открыть для редактирования с помощью **Изменить задачу** в ленте на страница **Структурная декомпозиция работ**.</span><span class="sxs-lookup"><span data-stu-id="8f84f-117">In cases where the task GUID is interpreted as a number, tasks can't be opened for edit using **Edit Task** in the ribbon on the **Work Breakdown Structure** page.</span></span>

<span data-ttu-id="8f84f-118">**Sales**</span><span class="sxs-lookup"><span data-stu-id="8f84f-118">**Sales**</span></span>

<span data-ttu-id="8f84f-119">Следующие проблемы были исправлены:</span><span class="sxs-lookup"><span data-stu-id="8f84f-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="8f84f-120">Исключение нулевой ссылки создается, когда вызывается подключаемый модуль **GetEstimatesForProject**.</span><span class="sxs-lookup"><span data-stu-id="8f84f-120">A null reference exception is generated when the **GetEstimatesForProject** plug-in is invoked.</span></span>
- <span data-ttu-id="8f84f-121">**Пометить как готовое к выставлению счета** в сетке вехи только частично обновляет атрибуты, за исключением атрибута **InvoiceStatus**, который обновляется.</span><span class="sxs-lookup"><span data-stu-id="8f84f-121">**Mark ready to invoice** on the milestone grid only partially updates attributes, except for the **InvoiceStatus** attribute, which is updated.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]