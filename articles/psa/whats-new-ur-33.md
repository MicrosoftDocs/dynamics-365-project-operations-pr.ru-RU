---
title: Новые возможности и изменения в Project Service Automation (обновление 33, версия 3)
description: В этом разделе перечислены функции и исправления, доступные в Project Service Automation (обновление 33, версия 3).
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.openlocfilehash: 2c96e4abd484bb66285421baaad82ead9589bbe9
ms.sourcegitcommit: be5beba71ee9770c0083b4fe5cc89e7ec6b741b8
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334590"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a><span data-ttu-id="d417c-103">Новые возможности и изменения в Project Service Automation (обновление 33, версия 3)</span><span class="sxs-lookup"><span data-stu-id="d417c-103">What's new or changed in Project Service Automation Update Release 33, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="d417c-104">Мы рады объявить о последнем обновлении для приложения Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="d417c-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="d417c-105">Этот выпуск содержит некоторые важные усовершенствования, направленные на качество, производительность и удобство использования.</span><span class="sxs-lookup"><span data-stu-id="d417c-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="d417c-106">Он совместим с Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="d417c-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="d417c-107">Чтобы выполнить обновление до этого выпуска, посетите страницу центра администрирования для онлайн-решений Dynamics 365 и установите обновление.</span><span class="sxs-lookup"><span data-stu-id="d417c-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="d417c-108">Дополнительные сведения см. в разделе [Установка, обновление или удаление предпочтительного решения](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="d417c-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="d417c-109">В этом разделе перечислены функции и исправления, появившиеся или изменившиеся в Project Service Automation версии 3 (обновление 33).</span><span class="sxs-lookup"><span data-stu-id="d417c-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 33.</span></span> <span data-ttu-id="d417c-110">Эта версия имеет номер сборки V3.10.54.98 и доступна через самообновление в июле 2021 года.</span><span class="sxs-lookup"><span data-stu-id="d417c-110">This version has a build number of V3.10.54.98 and is generally available through a self-update in July 2021.</span></span>

## <a name="update-release-33"></a><span data-ttu-id="d417c-111">Выпуск-обновление 33</span><span class="sxs-lookup"><span data-stu-id="d417c-111">Update Release 33</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="d417c-112">Исправленные ошибки</span><span class="sxs-lookup"><span data-stu-id="d417c-112">Bug fixes</span></span>

<span data-ttu-id="d417c-113">**Время и расходы**</span><span class="sxs-lookup"><span data-stu-id="d417c-113">**Time and Expense**</span></span>

<span data-ttu-id="d417c-114">Следующие проблемы были исправлены:</span><span class="sxs-lookup"><span data-stu-id="d417c-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="d417c-115">Два заблокированных поля, **msdyn_description**, а также **msdyn_externaldescription** доступны для редактирования после отправки.</span><span class="sxs-lookup"><span data-stu-id="d417c-115">Two locked fields, **msdyn_description** and **msdyn_externaldescription** are editable after submission.</span></span>
- <span data-ttu-id="d417c-116">Сообщение об ошибке возникает, если создается расход, не связанный с проектом.</span><span class="sxs-lookup"><span data-stu-id="d417c-116">An error message occurs if an expense is created that isn't related to a project.</span></span>
- <span data-ttu-id="d417c-117">Когда создается запись времени, роль ресурса по умолчанию становится неактивной.</span><span class="sxs-lookup"><span data-stu-id="d417c-117">When a time entry is created, the resource role defaults to an inactive role.</span></span>
- <span data-ttu-id="d417c-118">Строки журнала, связанные с отозванными и удаленными расходами, не удаляются.</span><span class="sxs-lookup"><span data-stu-id="d417c-118">Journal lines associated with a recalled and deleted expense aren't deleted.</span></span>
- <span data-ttu-id="d417c-119">В **Форме для быстрого создания записи времени** обновите представление **Список задач по проекту**, чтобы изменить дату, отображаемую по умолчанию, на дату начала задачи.</span><span class="sxs-lookup"><span data-stu-id="d417c-119">On the **Time entry Quick Create Form**, update the **Project Task List** view to change the date displayed by default to the start date of the task.</span></span>
- <span data-ttu-id="d417c-120">Когда вы создаете запись времени на вкладке **Связанные** ресурса, доступного для бронирования, запись времени создается неверно для авторизованного пользователя вместо родительского ресурса, доступного для бронирования.</span><span class="sxs-lookup"><span data-stu-id="d417c-120">When you create a time entry from the **Related** tab of the bookable resource, the time entry is incorrectly created for the signed-in user instead of the parent bookable resource.</span></span>
- <span data-ttu-id="d417c-121">Новые поля добавляются в диалоговое окно **Массовое утверждение MDD**.</span><span class="sxs-lookup"><span data-stu-id="d417c-121">New fields are added to the **Bulk approval MDD** dialog box.</span></span>

<span data-ttu-id="d417c-122">**Планирование проектов**</span><span class="sxs-lookup"><span data-stu-id="d417c-122">**Project planning**</span></span>

<span data-ttu-id="d417c-123">Следующие проблемы были исправлены:</span><span class="sxs-lookup"><span data-stu-id="d417c-123">The following issues have been fixed:</span></span>
- <span data-ttu-id="d417c-124">Низкая производительность при создании проекта, когда шаблоны рабочего времени проекта применяются со сложными календарями.</span><span class="sxs-lookup"><span data-stu-id="d417c-124">Slow project creation performance when project work hour templates are applied with complex calendars.</span></span>
- <span data-ttu-id="d417c-125">Когда дата начала позднее даты окончания, в шаблоне проекта копирования отображается ошибка из-за различий во временном компоненте каждого поля.</span><span class="sxs-lookup"><span data-stu-id="d417c-125">When the start date is greater than the end date, an error displays on the copy project template because of differences in the time component of each field.</span></span>

<span data-ttu-id="d417c-126">**Управление ресурсами**</span><span class="sxs-lookup"><span data-stu-id="d417c-126">**Resource management**</span></span>

<span data-ttu-id="d417c-127">Следующие проблемы были исправлены:</span><span class="sxs-lookup"><span data-stu-id="d417c-127">The following issues have been fixed:</span></span>
- <span data-ttu-id="d417c-128">В запросе использования ресурсов используется неверный параметр, и XML приводит к неверным результатам фильтрации в сетке **Загруженность ресурсов**.</span><span class="sxs-lookup"><span data-stu-id="d417c-128">An incorrect parameter is used in the resource utilization query and the XML leads to incorrect filter results on the **Resource Utilization** grid.</span></span>
- <span data-ttu-id="d417c-129">В окне подтверждения **Продлить бронирование** отображается неправильная дата окончания для бронирований.</span><span class="sxs-lookup"><span data-stu-id="d417c-129">The **Extend Bookings** confirmation displays incorrect end date for bookings.</span></span>

<span data-ttu-id="d417c-130">**Продажи**</span><span class="sxs-lookup"><span data-stu-id="d417c-130">**Sales**</span></span>

<span data-ttu-id="d417c-131">Следующие проблемы были исправлены:</span><span class="sxs-lookup"><span data-stu-id="d417c-131">The following issues have been fixed:</span></span>
- <span data-ttu-id="d417c-132">Сообщение об ошибке появляется, если цена категории создается с пропущенными значениями.</span><span class="sxs-lookup"><span data-stu-id="d417c-132">An error message occurs if a category price is created with missing values.</span></span>
- <span data-ttu-id="d417c-133">Сообщение об ошибке появляется, если срок этапа в строке контракта создается без строки заказа.</span><span class="sxs-lookup"><span data-stu-id="d417c-133">An error message occurs if a contract line milestone is created without an order line.</span></span>
