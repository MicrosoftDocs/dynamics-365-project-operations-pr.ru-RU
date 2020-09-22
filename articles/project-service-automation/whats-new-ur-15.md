---
title: Что нового и что изменилось в выпуске-обновлении 15 для Project Service Automation версии 3
description: В этом разделе приведены сведения о новых возможностях в выпуске-обновлении 15 для Project Service Automation версии 3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: 75117934-8042-448b-91dc-b43f1f677e4f
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 68e0faa4c1afdb0d1520388253671330f9b7d334
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754953"
---
# <a name="project-service-automation-v3-update-release-15"></a><span data-ttu-id="d8f99-103">Project Service Automation версии 3, выпуск-обновление 15</span><span class="sxs-lookup"><span data-stu-id="d8f99-103">Project Service Automation V3, Update Release 15</span></span>

<span data-ttu-id="d8f99-104">С удовольствием объявляем о выходе последнего обновления для приложения Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="d8f99-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="d8f99-105">Этот выпуск содержит некоторые важные усовершенствования, направленные на качество, производительность и удобство использования.</span><span class="sxs-lookup"><span data-stu-id="d8f99-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="d8f99-106">Этот выпуск совместим с Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="d8f99-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="d8f99-107">Чтобы обновить приложение до этого выпуска, посетите Центр администрирования Dynamics 365 Online и перейдите на страницу решений, чтобы установить обновление.</span><span class="sxs-lookup"><span data-stu-id="d8f99-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="d8f99-108">Дополнительные сведения см. в разделе [Установка, обновление или удаление предпочтительного решения](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="d8f99-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="d8f99-109">В этом разделе перечислены функции и исправления, появившиеся или изменившиеся в выпуске-обновлении 15 для PSA версии 3.</span><span class="sxs-lookup"><span data-stu-id="d8f99-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 15.</span></span> <span data-ttu-id="d8f99-110">Эта версия имеет номер сборки V3.10.5.28 и становится доступна широкому кругу клиентов посредством самостоятельного обновления в январе 2020 г.</span><span class="sxs-lookup"><span data-stu-id="d8f99-110">This version has a build number of V3.10.5.28 and is generally available through a self-update in January 2020.</span></span>

## <a name="update-release-15"></a><span data-ttu-id="d8f99-111">Выпуск-обновление 15</span><span class="sxs-lookup"><span data-stu-id="d8f99-111">Update Release 15</span></span> 

### <a name="enhancements"></a><span data-ttu-id="d8f99-112">Усовершенствования</span><span class="sxs-lookup"><span data-stu-id="d8f99-112">Enhancements</span></span>

- <span data-ttu-id="d8f99-113">Управление проектами</span><span class="sxs-lookup"><span data-stu-id="d8f99-113">Project Management</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="d8f99-114">Исправления ошибок</span><span class="sxs-lookup"><span data-stu-id="d8f99-114">Bug fixes</span></span>

- <span data-ttu-id="d8f99-115">Время и расходы</span><span class="sxs-lookup"><span data-stu-id="d8f99-115">Time and Expense</span></span>

  - <span data-ttu-id="d8f99-116">Исправлено: добавлена обработка ошибок при загрузке в представлении сверки.</span><span class="sxs-lookup"><span data-stu-id="d8f99-116">Fixed: Add on-load error handling in the reconciliation view.</span></span>
  - <span data-ttu-id="d8f99-117">Исправлено: в центре ресурсов проекта переименовано поле **Сумма** во избежание двусмысленности.</span><span class="sxs-lookup"><span data-stu-id="d8f99-117">Fixed: Project Resource Hub: Rename **Amount** to reduce ambiguity.</span></span>
  - <span data-ttu-id="d8f99-118">Исправлено: корректировка представления **Копировать столбцы записи времени** так, чтобы оно включало тип.</span><span class="sxs-lookup"><span data-stu-id="d8f99-118">Fixed: Adjust the view **Copy Time Entry Columns** to include the type.</span></span>
  - <span data-ttu-id="d8f99-119">Исправлено: редактирование длительности записи времени в представлении сетки с использованием десятичных чисел приводит к неизвестной ошибке для некоторых чисел.</span><span class="sxs-lookup"><span data-stu-id="d8f99-119">Fixed: Editing time entry duration in the grid view using decimal numbers results in unknown error for some numbers.</span></span>

- <span data-ttu-id="d8f99-120">Управление проектами</span><span class="sxs-lookup"><span data-stu-id="d8f99-120">Project Management</span></span>

  - <span data-ttu-id="d8f99-121">Исправлено: раскрывающееся меню **Использовать в режиме отслеживания** теперь расширяется в соответствии с шириной пунктов в нем.</span><span class="sxs-lookup"><span data-stu-id="d8f99-121">Fixed: The drop-down menu for **Use in Tracking View** now expands based on the width of the options.</span></span>
  - <span data-ttu-id="d8f99-122">Исправлено: при управлении проектами в часовом поясе +13 в расчетах задач могут отображаться неточные результаты.</span><span class="sxs-lookup"><span data-stu-id="d8f99-122">Fixed: When managing projects in the +13 time zone, tasks calculations can display inaccurate results.</span></span>
  - <span data-ttu-id="d8f99-123">Исправлено: **Время окончания участника рабочей группы** при использовании 24-часового календаря исправлено.</span><span class="sxs-lookup"><span data-stu-id="d8f99-123">Fixed: **Team Member End Time** has been corrected when using a 24-hour calendar.</span></span>
  - <span data-ttu-id="d8f99-124">Исправлено: снова активирован параметр **BPF** в главной форме **msdyn_project**.</span><span class="sxs-lookup"><span data-stu-id="d8f99-124">Fixed: Re-activated the **BPF** in **msdyn_project** main form.</span></span>
  - <span data-ttu-id="d8f99-125">Исправлено: расчет заданий больше не игнорирует один день.</span><span class="sxs-lookup"><span data-stu-id="d8f99-125">Fixed: Assignments calculation no longer ignores one day.</span></span>
  - <span data-ttu-id="d8f99-126">Исправлено: в форму проекта добавлен новый баннер для уведомления о том, что у пользователя и проекта разные часовые пояса.</span><span class="sxs-lookup"><span data-stu-id="d8f99-126">Fixed: A new notification banner has been added to the project form when the time zone differs between user and project.</span></span>

- <span data-ttu-id="d8f99-127">Sales</span><span class="sxs-lookup"><span data-stu-id="d8f99-127">Sales</span></span>

  - <span data-ttu-id="d8f99-128">Исправлено: подстановку категории оценки расходов можно использовать для фильтрации дубликатов.</span><span class="sxs-lookup"><span data-stu-id="d8f99-128">Fixed: Expense estimate category lookup can be used to filter duplicates.</span></span>
  - <span data-ttu-id="d8f99-129">Исправлено: код в **PluginDomain.ExecuteInTryCatchBlock(..)** больше не скрывает происхождение исключения.</span><span class="sxs-lookup"><span data-stu-id="d8f99-129">Fixed: Code in **PluginDomain.ExecuteInTryCatchBlock(..)** no longer hides the origin of the exception.</span></span>
  - <span data-ttu-id="d8f99-130">Исправлено: в поле **Подстановка проекта** в форме **Строка предложения с расценками** больше не появляется сообщение об ошибке, когда проектов больше 1000.</span><span class="sxs-lookup"><span data-stu-id="d8f99-130">Fixed: No longer get an error message in **Project lookup** in the **Quote Line** form when there are more than 1000 projects.</span></span>
  - <span data-ttu-id="d8f99-131">Исправлено: сетка **Оценки** для оценок труда и оценок расходов теперь отображается правильный символ валюты.</span><span class="sxs-lookup"><span data-stu-id="d8f99-131">Fixed: **Estimates** grid for labor estimates and expense estimates now displays the correct currency symbol.</span></span>
  - <span data-ttu-id="d8f99-132">Исправлено: после того как организация обновит PSA с выпуска-обновления 14 до выпуска-обновления 15, вкладка **Расписание** в форме **Проект** больше не является пустой.</span><span class="sxs-lookup"><span data-stu-id="d8f99-132">Fixed: After an organization updates PSA from Update Release 14 to Update Release 15, the **Schedule** tab no longer appears as blank on the **Project** form.</span></span>
