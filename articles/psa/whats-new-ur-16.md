---
title: Что нового или измененного в выпуске-обновлении 16 для Project Service Automation версии 3
description: В этом разделе перечислены функции и исправления, доступные в выпуске-обновлении 16 для Project Service Automation версии 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
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
ms.openlocfilehash: 2c93d34b61001b7755d426539ac384641a7bc9da
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121594"
---
# <a name="project-service-automation-update-release-16-v3"></a><span data-ttu-id="101d3-103">Выпуск-обновление 16 Project Service Automation, версия 3</span><span class="sxs-lookup"><span data-stu-id="101d3-103">Project Service Automation Update Release 16, V3</span></span>

<span data-ttu-id="101d3-104">Мы рады объявить о последнем обновлении приложения Project Service Automation для Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="101d3-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="101d3-105">Этот выпуск содержит некоторые важные усовершенствования, направленные на качество, производительность и удобство использования.</span><span class="sxs-lookup"><span data-stu-id="101d3-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="101d3-106">Этот выпуск совместим с Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="101d3-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="101d3-107">Чтобы обновить приложение до этого выпуска, посетите Центр администрирования Dynamics 365 Online, страницу решений, чтобы установить обновление.</span><span class="sxs-lookup"><span data-stu-id="101d3-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="101d3-108">Дополнительные сведения см. в разделе [Установка, обновление предпочтительного решения](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page).</span><span class="sxs-lookup"><span data-stu-id="101d3-108">For more information, see [Install, Update a Preferred Solution](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page).</span></span>
<span data-ttu-id="101d3-109">В этом разделе перечислены функции и исправления, появившиеся или изменившиеся в выпуске-обновлении 16 для PSA версии 3.</span><span class="sxs-lookup"><span data-stu-id="101d3-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 16.</span></span> <span data-ttu-id="101d3-110">Эта версия имеет номер сборки V3.10.6.34 и становится доступна широкому кругу клиентов посредством самостоятельного обновления в январе 2020 г.</span><span class="sxs-lookup"><span data-stu-id="101d3-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in January 2020.</span></span>


## <a name="update-release-16"></a><span data-ttu-id="101d3-111">Выпуск-обновление 16</span><span class="sxs-lookup"><span data-stu-id="101d3-111">Update Release 16</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="101d3-112">Исправления ошибок</span><span class="sxs-lookup"><span data-stu-id="101d3-112">Bug fixes</span></span>

-   <span data-ttu-id="101d3-113">Время и расходы</span><span class="sxs-lookup"><span data-stu-id="101d3-113">Time and Expense</span></span>

    -   <span data-ttu-id="101d3-114">Исправлено: пользователи, пытающиеся отправить удаленные записи о времени и расходах для одобрений, теперь будут получать соответствующие сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="101d3-114">Fixed: Users attempting to submit deleted time and expense entries for approvals will now receive relevant error messages.</span></span>

-   <span data-ttu-id="101d3-115">Управление проектами</span><span class="sxs-lookup"><span data-stu-id="101d3-115">Project Management</span></span>

    -   <span data-ttu-id="101d3-116">Исправлено: ресурсные единицы, определенные для участников рабочей группы в шаблонах, учитываются при применении этих шаблонов к новому проекту.</span><span class="sxs-lookup"><span data-stu-id="101d3-116">Fixed: The resourcing units defined for team members in templates are respected with the templates are applied to a new project.</span></span>

    -   <span data-ttu-id="101d3-117">Исправлено: улучшена обработка переназначения владельца записи.</span><span class="sxs-lookup"><span data-stu-id="101d3-117">Fixed: Improved handling of the re-assignment of record ownership.</span></span>

    -   <span data-ttu-id="101d3-118">Исправлено: проекты, которые находятся в процессе копирования, не будут допущены к копированию, пока все операции копирования не будут завершены.</span><span class="sxs-lookup"><span data-stu-id="101d3-118">Fixed: Projects that are in the process of being copied will not be permitted to copied until all copy operations are complete.</span></span>

-   <span data-ttu-id="101d3-119">Управление ресурсами</span><span class="sxs-lookup"><span data-stu-id="101d3-119">Resource Management</span></span>

    -   <span data-ttu-id="101d3-120">Исправлено: расширение резервирований теперь правильно обрабатывает короткие периоды и больше не создает ноль часов для расширенных резервирований.</span><span class="sxs-lookup"><span data-stu-id="101d3-120">Fixed: Extend bookings now handles short durations correctly and no longer creates zero hours for extended bookings.</span></span>

    -   <span data-ttu-id="101d3-121">Исправлено: представление выверки теперь отображается, когда часовой пояс проекта составляет +5:30 по Гринвичу, а часовой пояс пользователя отличается.</span><span class="sxs-lookup"><span data-stu-id="101d3-121">Fixed: The reconciliation view now renders when the project time zone is +5:30 GMT and the user’s time aone is different.</span></span>

-   <span data-ttu-id="101d3-122">Sales</span><span class="sxs-lookup"><span data-stu-id="101d3-122">Sales</span></span>

    -   <span data-ttu-id="101d3-123">Исправлено: при удалении проекта, сопоставленного со строкой контракта, и при сопоставлении нового проекта записи фактических данных нового проекта не переоценивались на основе правил выставления счетов и ценообразования, определенных в строке контракта.</span><span class="sxs-lookup"><span data-stu-id="101d3-123">Fixed: When a project mapped to a contract line is removed and a new project is mapped, the actual records on the new project were not getting re-evaluated based on the billing and pricing rules defined on the contract line.</span></span> <span data-ttu-id="101d3-124">Это было исправлено в этом выпуске.</span><span class="sxs-lookup"><span data-stu-id="101d3-124">This has been fixed in this release.</span></span> <span data-ttu-id="101d3-125">Ценообразование и фактические записи в новом сопоставленном проекте будут сторнированы и правильно заново созданы в соответствии с правилами ценообразования и выставления счетов в строке контракта.</span><span class="sxs-lookup"><span data-stu-id="101d3-125">Pricing and actual records on the newly mapped project will get reversed and re-created correctly based on the pricing and billing rules of the contract line.</span></span> <span data-ttu-id="101d3-126">Фактические записи проекта, для которого отменено сопоставление, также будут пересмотрены и, как следствие, заново созданы.</span><span class="sxs-lookup"><span data-stu-id="101d3-126">The actual records of the un-mapped project will also get re-evaluated and re-created as a consequence.</span></span>

    -   <span data-ttu-id="101d3-127">Исправлено: дополнительная проверка была добавлена в поле **Сумма** строки оценки, чтобы гарантировать, что нулевые значения не сохраняются.</span><span class="sxs-lookup"><span data-stu-id="101d3-127">Fixed: Additional validation has been added to an estimate line’s **Amount** field to ensure that null values are not persisted.</span></span>

    -   <span data-ttu-id="101d3-128">Исправлено: когда в проекте были обновлены фактические данные, в основную форму проекта была добавлена кнопка обновления, чтобы пользователи могли повторно синхронизировать фактические данные.</span><span class="sxs-lookup"><span data-stu-id="101d3-128">Fixed: When actuals have been updated on a project, a refresh button has been added to the project main form to allow users to re-sync the actuals.</span></span>

    -   <span data-ttu-id="101d3-129">Исправлено: когда пользователи обновляются с 2.X до 3.X, проекты со значением NULL для имени проекта будут разрешены.</span><span class="sxs-lookup"><span data-stu-id="101d3-129">Fixed: When users upgrade from 2.X to 3.X, projects with a NULL value for project name will be permitted.</span></span>

