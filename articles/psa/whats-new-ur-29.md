---
title: Что нового или измененного в выпуске-обновлении 29 для Project Service Automation версии V3
description: В этом разделе перечислены функции и исправления, доступные в выпуске-обновлении 29 для Project Service Automation версии V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 320f4f74cb5997e42e2dc9e1d8c8a5ab95ae6647
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010487"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a><span data-ttu-id="8dabc-103">Что нового или измененного в выпуске-обновлении 29 для Project Service Automation версии V3</span><span class="sxs-lookup"><span data-stu-id="8dabc-103">What's new or changed in Project Service Automation Update Release 29, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="8dabc-104">Мы рады объявить о последнем обновлении приложения Project Service Automation для Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="8dabc-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="8dabc-105">Этот выпуск содержит некоторые важные усовершенствования, направленные на качество, производительность и удобство использования.</span><span class="sxs-lookup"><span data-stu-id="8dabc-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="8dabc-106">Этот выпуск совместим с Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="8dabc-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="8dabc-107">Чтобы обновить приложение до этого выпуска, посетите страницу решений Центра администрирования Dynamics 365 Online и установите обновление.</span><span class="sxs-lookup"><span data-stu-id="8dabc-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="8dabc-108">Дополнительные сведения см. в разделе [Установка, обновление или удаление предпочтительного решения](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="8dabc-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="8dabc-109">В этом разделе перечислены функции и исправления, появившиеся или изменившиеся в выпуске-обновлении 29 для Project Service Automation V3.</span><span class="sxs-lookup"><span data-stu-id="8dabc-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 29.</span></span> <span data-ttu-id="8dabc-110">Эта версия имеет номер сборки V3.10.47.7 и обычно доступна через самостоятельное обновление в феврале 2021 года.</span><span class="sxs-lookup"><span data-stu-id="8dabc-110">This version has a build number of V3.10.47.7 and is generally available through a self-update in February 2021.</span></span>

## <a name="update-release-29"></a><span data-ttu-id="8dabc-111">Выпуск-обновление 29</span><span class="sxs-lookup"><span data-stu-id="8dabc-111">Update Release 29</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="8dabc-112">Исправленные ошибки</span><span class="sxs-lookup"><span data-stu-id="8dabc-112">Bug fixes</span></span>

<span data-ttu-id="8dabc-113">**Время и расходы**</span><span class="sxs-lookup"><span data-stu-id="8dabc-113">**Time and Expense**</span></span>

<span data-ttu-id="8dabc-114">Следующие проблемы были исправлены:</span><span class="sxs-lookup"><span data-stu-id="8dabc-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="8dabc-115">Пользователи не могут видеть рабочее время, зарегистрированное в нерабочие дни, в сетке ввода времени.</span><span class="sxs-lookup"><span data-stu-id="8dabc-115">Users can't see working hours logged on non-working days in the time entry grid.</span></span>
- <span data-ttu-id="8dabc-116">Утвержденные записи расходов можно редактировать в сетке.</span><span class="sxs-lookup"><span data-stu-id="8dabc-116">Approved expense entries can be edited on the grid.</span></span>

<span data-ttu-id="8dabc-117">**Управление проектами**</span><span class="sxs-lookup"><span data-stu-id="8dabc-117">**Project Management**</span></span>

<span data-ttu-id="8dabc-118">Следующие проблемы были исправлены:</span><span class="sxs-lookup"><span data-stu-id="8dabc-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="8dabc-119">Отсутствует логика проверки, гарантирующая, что часы работы по назначению ресурсов не могут быть отрицательными.</span><span class="sxs-lookup"><span data-stu-id="8dabc-119">Missing validation logic to ensure resource assignment effort hours can't be negative.</span></span>
- <span data-ttu-id="8dabc-120">Пользовательское действие **AssignResourcesForTask** обновляет все поля, а не только измененные поля.</span><span class="sxs-lookup"><span data-stu-id="8dabc-120">The custom action, **AssignResourcesForTask** updates all fields instead of only changed fields.</span></span>
- <span data-ttu-id="8dabc-121">При копировании проекта в среде с надстройками или рабочими процессами, зарегистрированными в событии **CreateProject** атрибут **msdyn_bulkgenerationstatus** не обновляется, если **CopyWBSToProject** вызывает сбой.</span><span class="sxs-lookup"><span data-stu-id="8dabc-121">When copying a project in an environment with plug-ins or workflows that are registered on the **CreateProject** event, the **msdyn_bulkgenerationstatus** attribute isn't updated if the **CopyWBSToProject** fails.</span></span>
- <span data-ttu-id="8dabc-122">Когда вы разворачиваете календарь проекта, рабочие дни не сортируются в по возрастанию, что приводит к сбою обновления некоторых задач проекта.</span><span class="sxs-lookup"><span data-stu-id="8dabc-122">When you expand the project calendar, the working days aren't sorted in ascending order causing some project task updates to fail.</span></span>
- <span data-ttu-id="8dabc-123">Смена менеджера проекта в существующем проекте запускает логику установки подразделения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8dabc-123">Changing the Project Manager on an existing project triggers the organizational unit defaulting logic.</span></span>

<span data-ttu-id="8dabc-124">**Продажи**</span><span class="sxs-lookup"><span data-stu-id="8dabc-124">**Sales**</span></span>

<span data-ttu-id="8dabc-125">Следующие проблемы были исправлены:</span><span class="sxs-lookup"><span data-stu-id="8dabc-125">The following issues have been fixed:</span></span>

- <span data-ttu-id="8dabc-126">Вкладка **Производительность по контракту** на странице **Контракт** автоматически завершается с ошибкой во время инициализации, если отсутствуют строки контракта.</span><span class="sxs-lookup"><span data-stu-id="8dabc-126">The **Contract Performance** tab on the **Contract** page fails silently during initialization when no contract lines are present.</span></span>