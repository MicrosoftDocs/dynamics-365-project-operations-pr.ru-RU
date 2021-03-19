---
title: Что нового или измененного в выпуске-обновлении 25 для Project Service Automation версии V3
description: В этом разделе перечислены функции и исправления, доступные в выпуске-обновлении 25 для Project Service Automation версии V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: 30822ec64b31e110202a587dd941bdff60116712
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280459"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a><span data-ttu-id="77f69-103">Что нового или измененного в выпуске-обновлении 25 для Project Service Automation версии V3</span><span class="sxs-lookup"><span data-stu-id="77f69-103">What's new or changed in Project Service Automation Update Release 25, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="77f69-104">Мы рады объявить о последнем обновлении приложения Project Service Automation для Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="77f69-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="77f69-105">Этот выпуск содержит некоторые важные усовершенствования, направленные на качество, производительность и удобство использования.</span><span class="sxs-lookup"><span data-stu-id="77f69-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="77f69-106">Этот выпуск совместим с Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="77f69-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="77f69-107">Чтобы обновить приложение до этого выпуска, посетите страницу решений Центра администрирования Dynamics 365 Online и установите обновление.</span><span class="sxs-lookup"><span data-stu-id="77f69-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="77f69-108">Дополнительные сведения см. в разделе [Установка, обновление или удаление предпочтительного решения](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="77f69-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="77f69-109">В этой теме перечислены новые или измененные функции и исправления для Project Service Automation V3, выпуск-обновление 25. Эта версия имеет номер сборки V 3.10.43.76 и она общедоступна через самообновление в октябре 2020 года.</span><span class="sxs-lookup"><span data-stu-id="77f69-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 25 This version has a build number of V 3.10.43.76 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-25"></a><span data-ttu-id="77f69-110">Выпуск-обновление 25</span><span class="sxs-lookup"><span data-stu-id="77f69-110">Update Release 25</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="77f69-111">Исправленные ошибки</span><span class="sxs-lookup"><span data-stu-id="77f69-111">Bug fixes</span></span>

<span data-ttu-id="77f69-112">**Время и расходы**</span><span class="sxs-lookup"><span data-stu-id="77f69-112">**Time and Expense**</span></span>

<span data-ttu-id="77f69-113">Следующая ошибка была исправлена:</span><span class="sxs-lookup"><span data-stu-id="77f69-113">The following issue has been fixed:</span></span>

- <span data-ttu-id="77f69-114">Диаграмма ввода времени, показывающая дополнительные данные, основанные на извлечении слишком большого интервала.</span><span class="sxs-lookup"><span data-stu-id="77f69-114">Time entry chart showing additional data based on too large of an interval being retrieved.</span></span>

<span data-ttu-id="77f69-115">**Управление ресурсами**</span><span class="sxs-lookup"><span data-stu-id="77f69-115">**Resource Management**</span></span>

<span data-ttu-id="77f69-116">Следующая ошибка была исправлена:</span><span class="sxs-lookup"><span data-stu-id="77f69-116">The following issue has been fixed:</span></span>

- <span data-ttu-id="77f69-117">Добавлен код Package Deployer, чтобы пропустить импорт исправления Universal Resource Scheduling, если уже существует исправление более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="77f69-117">Added package deployer code to skip the Universal Resource Scheduling patch import if a higher version patch already exists.</span></span>

<span data-ttu-id="77f69-118">**Управление проектами**</span><span class="sxs-lookup"><span data-stu-id="77f69-118">**Project Management**</span></span>

<span data-ttu-id="77f69-119">Следующие проблемы были исправлены:</span><span class="sxs-lookup"><span data-stu-id="77f69-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="77f69-120">Исправлены расхождения в округлении и обменном курсе, приводящие к неправильной плановой себестоимости в сетке отслеживания проекта.</span><span class="sxs-lookup"><span data-stu-id="77f69-120">Corrected rounding and exchange rate discrepancies resulting in incorrect planned cost in the project tracking grid.</span></span>
- <span data-ttu-id="77f69-121">Поддержка возможности отображения двух или более сеток реагирования в форме **Проект**.</span><span class="sxs-lookup"><span data-stu-id="77f69-121">Support the ability to display two or more react grids on the **Project** form.</span></span>
- <span data-ttu-id="77f69-122">Предоставляется проверка для исправления возможности назначать задачу после даты окончания календаря, что приводит к сбою назначения ресурсов.</span><span class="sxs-lookup"><span data-stu-id="77f69-122">Provided validation to address the ability to assign a task past the calendar end date, which results in a failed resource assignment.</span></span>
- <span data-ttu-id="77f69-123">Улучшена обработка ошибок для устранения исключения ссылки NULL, созданного из следующих мест:</span><span class="sxs-lookup"><span data-stu-id="77f69-123">Improved error handling to address Null Reference Exception generated from the following:</span></span>

    - <span data-ttu-id="77f69-124">Подключаемый модуль **PreValidateProjectTeamMemberCreate**</span><span class="sxs-lookup"><span data-stu-id="77f69-124">**PreValidateProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="77f69-125">**PreValidateProjectTaskCreate**, когда задача проекта создается без связанного проекта</span><span class="sxs-lookup"><span data-stu-id="77f69-125">**PreValidateProjectTaskCreate** when a project task is created without an associated project</span></span>
    - <span data-ttu-id="77f69-126">Подключаемый модуль **PreProjectTeamMemberCreate**</span><span class="sxs-lookup"><span data-stu-id="77f69-126">**PreProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="77f69-127">Подключаемый модуль **PostProjectTeamMemberDelete**</span><span class="sxs-lookup"><span data-stu-id="77f69-127">**PostProjectTeamMemberDelete** plug-in</span></span>
    - <span data-ttu-id="77f69-128">Подключаемый модуль **PreValidateProjectTaskDelete**</span><span class="sxs-lookup"><span data-stu-id="77f69-128">**PreValidateProjectTaskDelete** plug-in</span></span>

<span data-ttu-id="77f69-129">**Sales**</span><span class="sxs-lookup"><span data-stu-id="77f69-129">**Sales**</span></span>

<span data-ttu-id="77f69-130">Следующие проблемы были исправлены:</span><span class="sxs-lookup"><span data-stu-id="77f69-130">The following issues have been fixed:</span></span>

- <span data-ttu-id="77f69-131">Улучшена обработка ошибок для устранений исключений ссылки NULL, сгенерированных из **Копирование проекта: оценки управления HelperResource**.</span><span class="sxs-lookup"><span data-stu-id="77f69-131">Improved error handling to address Null Reference Exceptions generated from **Copy Project: Estimates HelperResource Management**.</span></span>
- <span data-ttu-id="77f69-132">**Не готово к выставлению счета** в пункте **Задолженность по выставлению счетов по времени и материалам** не очищает статус выставления счета.</span><span class="sxs-lookup"><span data-stu-id="77f69-132">**Not ready to Invoice** on a **Time and Material Billing Backlog** doesn't clear the billing status.</span></span>
- <span data-ttu-id="77f69-133">Исправлена неправильная подпись кнопок **Цены** на вкладках **Цена роли** и **Каталог номенклатур**.</span><span class="sxs-lookup"><span data-stu-id="77f69-133">Corrected mislabeled **Prices** buttons on the **Role Price** and **Catalog Items** tab.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]