---
title: Что нового и что изменилось в выпуске-обновлении 16 для Project Service Automation версии 3
description: В этом разделе перечислены функции и исправления, доступные в выпуске-обновлении 16 для Project Service Automation версии 3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: b890a7b6-1664-4812-8732-fed77653cc05
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 0f4c206fd5b7a36d940e966b28c2437525812a98
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754952"
---
# <a name="project-service-automation-v3-update-release-16"></a><span data-ttu-id="614a5-103">Project Service Automation версии 3, выпуск-обновление 16</span><span class="sxs-lookup"><span data-stu-id="614a5-103">Project Service Automation V3, Update Release 16</span></span>
<span data-ttu-id="614a5-104">Мы рады объявить о последнем обновлении приложения Project Service Automation для Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="614a5-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="614a5-105">Этот выпуск содержит некоторые важные усовершенствования, направленные на качество, производительность и удобство использования.</span><span class="sxs-lookup"><span data-stu-id="614a5-105">This release includes some important improvements to quality, performance, and usability.</span></span>

<span data-ttu-id="614a5-106">Этот выпуск совместим с Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="614a5-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="614a5-107">Чтобы обновить приложение до этого выпуска, посетите Центр администрирования Dynamics 365 Online, страницу решений, чтобы установить обновление.</span><span class="sxs-lookup"><span data-stu-id="614a5-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="614a5-108">Дополнительные сведения см. в разделе [Установка, обновление предпочтительного решения](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page).</span><span class="sxs-lookup"><span data-stu-id="614a5-108">For more information, see [Install, Update a Preferred Solution](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page).</span></span> <span data-ttu-id="614a5-109">В этом разделе перечислены функции и исправления, появившиеся или изменившиеся в выпуске-обновлении 16 для PSA версии 3.</span><span class="sxs-lookup"><span data-stu-id="614a5-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 16.</span></span> <span data-ttu-id="614a5-110">У этой версии номер сборки V3.10.6.34, она становится доступна широкому кругу клиентов посредством самостоятельного обновления в январе 2020 г.</span><span class="sxs-lookup"><span data-stu-id="614a5-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in January 2020</span></span>

## <a name="update-release-16"></a><span data-ttu-id="614a5-111">Выпуск-обновление 16</span><span class="sxs-lookup"><span data-stu-id="614a5-111">Update Release 16</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="614a5-112">Исправленные ошибки</span><span class="sxs-lookup"><span data-stu-id="614a5-112">Bug fixes</span></span>

-   <span data-ttu-id="614a5-113">Время и расходы</span><span class="sxs-lookup"><span data-stu-id="614a5-113">Time and Expense</span></span>

    -   <span data-ttu-id="614a5-114">Исправлено: пользователи, пытающиеся отправить удаленные записи о времени и расходах для одобрений, теперь будут получать соответствующие сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="614a5-114">Fixed: Users attempting to submit deleted time and expense entries for approvals will now receive relevant error messages.</span></span>

-   <span data-ttu-id="614a5-115">Управление проектами</span><span class="sxs-lookup"><span data-stu-id="614a5-115">Project Management</span></span>

    -   <span data-ttu-id="614a5-116">Исправлено: ресурсные единицы, определенные для участников рабочей группы в шаблонах, учитываются при применении этих шаблонов к новому проекту.</span><span class="sxs-lookup"><span data-stu-id="614a5-116">Fixed: The resourcing units defined for team members in templates are respected with the templates are applied to a new project.</span></span>

    -   <span data-ttu-id="614a5-117">Исправлено: улучшена обработка переназначения владельца записи.</span><span class="sxs-lookup"><span data-stu-id="614a5-117">Fixed: Improved handling of the re-assignment of record ownership.</span></span>

    -   <span data-ttu-id="614a5-118">Исправлено: проекты, которые находятся в процессе копирования, не будут допущены к копированию, пока все операции копирования не будут завершены.</span><span class="sxs-lookup"><span data-stu-id="614a5-118">Fixed: Projects that are in the process of being copied will not be permitted to copied until all copy operations are complete.</span></span>

-   <span data-ttu-id="614a5-119">Управление ресурсами</span><span class="sxs-lookup"><span data-stu-id="614a5-119">Resource Management</span></span>

    -   <span data-ttu-id="614a5-120">Исправлено: расширение резервирований теперь правильно обрабатывает короткие периоды и больше не создает ноль часов для расширенных резервирований.</span><span class="sxs-lookup"><span data-stu-id="614a5-120">Fixed: Extend bookings now handles short durations correctly and no longer creates zero hours for extended bookings.</span></span>

    -   <span data-ttu-id="614a5-121">Исправлено: представление выверки теперь отображается, когда часовой пояс проекта составляет +5:30 по Гринвичу, а часовой пояс пользователя отличается.</span><span class="sxs-lookup"><span data-stu-id="614a5-121">Fixed: The reconciliation view now renders when the project time zone is +5:30 GMT and the user’s time aone is different.</span></span>

-   <span data-ttu-id="614a5-122">Sales</span><span class="sxs-lookup"><span data-stu-id="614a5-122">Sales</span></span>

    -   <span data-ttu-id="614a5-123">Исправлено: при удалении проекта, сопоставленного со строкой контракта, и при сопоставлении нового проекта записи фактических данных нового проекта не переоценивались на основе правил выставления счетов и ценообразования, определенных в строке контракта.</span><span class="sxs-lookup"><span data-stu-id="614a5-123">Fixed: When a project mapped to a contract line is removed and a new project is mapped, the actual records on the new project were not getting re-evaluated based on the billing and pricing rules defined on the contract line.</span></span> <span data-ttu-id="614a5-124">Это было исправлено в этом выпуске.</span><span class="sxs-lookup"><span data-stu-id="614a5-124">This has been fixed in this release.</span></span> <span data-ttu-id="614a5-125">Ценообразование и фактические записи в новом сопоставленном проекте будут сторнированы и правильно заново созданы в соответствии с правилами ценообразования и выставления счетов в строке контракта.</span><span class="sxs-lookup"><span data-stu-id="614a5-125">Pricing and actual records on the newly mapped project will get reversed and re-created correctly based on the pricing and billing rules of the contract line.</span></span> <span data-ttu-id="614a5-126">Фактические записи проекта, для которого отменено сопоставление, также будут пересмотрены и, как следствие, заново созданы.</span><span class="sxs-lookup"><span data-stu-id="614a5-126">The actual records of the un-mapped project will also get re-evaluated and re-created as a consequence.</span></span>

    -   <span data-ttu-id="614a5-127">Исправлено: дополнительная проверка была добавлена в поле **Сумма** строки оценки, чтобы гарантировать, что нулевые значения не сохраняются.</span><span class="sxs-lookup"><span data-stu-id="614a5-127">Fixed: Additional validation has been added to an estimate line’s **Amount** field to ensure that null values are not persisted.</span></span>

    -   <span data-ttu-id="614a5-128">Исправлено: когда в проекте были обновлены фактические данные, в основную форму проекта была добавлена кнопка обновления, чтобы пользователи могли повторно синхронизировать фактические данные.</span><span class="sxs-lookup"><span data-stu-id="614a5-128">Fixed: When actuals have been updated on a project, a refresh button has been added to the project main form to allow users to re-sync the actuals.</span></span>

    -   <span data-ttu-id="614a5-129">Исправлено: когда пользователи обновляются с 2.X до 3.X, проекты со значением NULL для имени проекта будут разрешены.</span><span class="sxs-lookup"><span data-stu-id="614a5-129">Fixed: When users upgrade from 2.X to 3.X, projects with a NULL value for project name will be permitted.</span></span>
