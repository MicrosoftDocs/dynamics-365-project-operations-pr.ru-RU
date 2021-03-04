---
title: Что нового или измененного в выпуске обновления 26 для Project Service Automation версии V3
description: В этом разделе перечислены функции и исправления, доступные в выпуске-обновлении 26 для Project Service Automation версии версии 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: 14fcccf5804e5da0926dbc69bdfa040229a7f068
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143574"
---
# <a name="project-service-automation-update-release-26-v3"></a><span data-ttu-id="bae25-103">Выпуск обновления 26 для Project Service Automation, версия V3</span><span class="sxs-lookup"><span data-stu-id="bae25-103">Project Service Automation Update Release 26, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="bae25-104">Мы рады объявить о последнем обновлении приложения Project Service Automation для Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="bae25-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="bae25-105">Этот выпуск содержит некоторые важные усовершенствования, направленные на качество, производительность и удобство использования.</span><span class="sxs-lookup"><span data-stu-id="bae25-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="bae25-106">Этот выпуск совместим с Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="bae25-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="bae25-107">Чтобы обновить приложение до этого выпуска, посетите страницу решений Центра администрирования Dynamics 365 Online и установите обновление.</span><span class="sxs-lookup"><span data-stu-id="bae25-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="bae25-108">Дополнительные сведения см. в разделе [Установка, обновление или удаление предпочтительного решения](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="bae25-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="bae25-109">В этом разделе перечислены функции и исправления, появившиеся или изменившиеся в выпуске обновления 26 для Project Service Automation версии V3.</span><span class="sxs-lookup"><span data-stu-id="bae25-109">This topic lists the features and fixes that are new or changed for Project Service Automation Update Release 26, V3.</span></span> <span data-ttu-id="bae25-110">Эта версия имеет номер сборки V3.10.44.59 и обычно доступна через самостоятельное обновление в декабре 2020 года.</span><span class="sxs-lookup"><span data-stu-id="bae25-110">This version has a build number of V3.10.44.59 and is generally available through a self-update in December 2020.</span></span>

## <a name="update-release-26"></a><span data-ttu-id="bae25-111">Выпуск-обновление 26</span><span class="sxs-lookup"><span data-stu-id="bae25-111">Update Release 26</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="bae25-112">Исправленные ошибки</span><span class="sxs-lookup"><span data-stu-id="bae25-112">Bug fixes</span></span>

<span data-ttu-id="bae25-113">**Время и расходы**</span><span class="sxs-lookup"><span data-stu-id="bae25-113">**Time and Expense**</span></span>

<span data-ttu-id="bae25-114">Следующие проблемы были исправлены:</span><span class="sxs-lookup"><span data-stu-id="bae25-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="bae25-115">Пользователи могут изменить задачу на запись времени, которая была утверждена/отправлена.</span><span class="sxs-lookup"><span data-stu-id="bae25-115">Users are able to change the task on a time entry that has been approved/submitted.</span></span>
- <span data-ttu-id="bae25-116">Ошибка «Ссылка на объект не указана» при сохранении записи времени.</span><span class="sxs-lookup"><span data-stu-id="bae25-116">"Object Reference Not Set" error when saving time entry.</span></span>
- <span data-ttu-id="bae25-117">Импорт записи времени из назначений ресурсов создает записи времени с неправильными значениями DateTime.</span><span class="sxs-lookup"><span data-stu-id="bae25-117">Time entry import from resource assignments creates time entries with the incorrect DateTime values.</span></span>
- <span data-ttu-id="bae25-118">Когда установлены приложения Project Service Automation и Field Service, кнопка **Создать** дважды отображается на панели команд для записей времени в приложении Field Service.</span><span class="sxs-lookup"><span data-stu-id="bae25-118">When Project Service Automation and the Field Service app are both installed, the **New** button is displaying twice on the command bar for time entries in the Field Service app.</span></span>
- <span data-ttu-id="bae25-119">Обновления ячеек **Разрешить единицу измерения** и **Группа единиц измерения** в сетке **Оценки расходов**.</span><span class="sxs-lookup"><span data-stu-id="bae25-119">**Allow Unit** and **Unit group** cells updates now work on the **Expense Estimates** grid.</span></span>
- <span data-ttu-id="bae25-120">Форма **Обновить изменение записи времени** включает **временная шкала**.</span><span class="sxs-lookup"><span data-stu-id="bae25-120">**Update Time Entry Edit** form includes **Timeline**.</span></span>
- <span data-ttu-id="bae25-121">Утверждение времени для несвязанных с проектом записей времени блокирует систему при поиске роли утверждающего проект.</span><span class="sxs-lookup"><span data-stu-id="bae25-121">Time approval for non-project time entries blocks the system when searching for a project approver role.</span></span>

<span data-ttu-id="bae25-122">**Управление ресурсами**</span><span class="sxs-lookup"><span data-stu-id="bae25-122">**Resource Management**</span></span>

<span data-ttu-id="bae25-123">Следующие проблемы были исправлены:</span><span class="sxs-lookup"><span data-stu-id="bae25-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="bae25-124">Добавлена проверка в подключаемый модуль **PostProjectCreate**, чтобы проверить наличие основного требования перед его созданием.</span><span class="sxs-lookup"><span data-stu-id="bae25-124">Added validation in the **PostProjectCreate** plug-in to check for a primary requirement before creating one.</span></span>
- <span data-ttu-id="bae25-125">Форма быстрого создания **Участник рабочей группы проекта** выдает исключение пустой ссылки, если поля удаляются из формы.</span><span class="sxs-lookup"><span data-stu-id="bae25-125">**Project Team Member** quick create form throws a null reference exception if fields are removed from the form.</span></span>
- <span data-ttu-id="bae25-126">Создать требования на 12 часов за 1 год не удастся.</span><span class="sxs-lookup"><span data-stu-id="bae25-126">Generate requirements for 12 hours over 1 year will fail.</span></span>
- <span data-ttu-id="bae25-127">Улучшено сообщение об ошибке исключение нулевой ссылки во время создания требования ресурса.</span><span class="sxs-lookup"><span data-stu-id="bae25-127">Improved error message null reference exception during resource requirement creation.</span></span>

<span data-ttu-id="bae25-128">**Управление проектами**</span><span class="sxs-lookup"><span data-stu-id="bae25-128">**Project Management**</span></span>

<span data-ttu-id="bae25-129">Следующие проблемы были исправлены:</span><span class="sxs-lookup"><span data-stu-id="bae25-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="bae25-130">Улучшенная проверка для устранения исключения нулевой ссылки, созданного в подключаемый модуль **PreProjectUpdate**.</span><span class="sxs-lookup"><span data-stu-id="bae25-130">Improved validation to address null reference exception generated in the **PreProjectUpdate** plug-in.</span></span>
- <span data-ttu-id="bae25-131">Проекты, опубликованные надстройкой рабочего стола Microsoft Project, удаляют неназначенные назначения.</span><span class="sxs-lookup"><span data-stu-id="bae25-131">Projects published by the Microsoft Project desktop add-in delete unassigned assignments.</span></span>
- <span data-ttu-id="bae25-132">Добавлена новая проверка, когда ссылка на проект задачи недействительна из-за исключения нулевой ссылки в подключаемый модуль **PreValidateProjectTaskUpdate**.</span><span class="sxs-lookup"><span data-stu-id="bae25-132">Added new validation when a task’s project reference is invalid due to null reference exception in **PreValidateProjectTaskUpdate** plug-in.</span></span>
- <span data-ttu-id="bae25-133">Сетка участников рабочей группы не показывает отдельных назначений в записи участника рабочей группы.</span><span class="sxs-lookup"><span data-stu-id="bae25-133">Team Member grid does not show distinct assignments on the team member record.</span></span>
- <span data-ttu-id="bae25-134">Добавлены новые сообщения о проверке и ошибках из-за исключения нулевой ссылки в подключаемый модуль **PreProjectTaskDelete**.</span><span class="sxs-lookup"><span data-stu-id="bae25-134">Added new validation and error messages due to null reference exception in **PreProjectTaskDelete** plug-in.</span></span>

<span data-ttu-id="bae25-135">**Sales**</span><span class="sxs-lookup"><span data-stu-id="bae25-135">**Sales**</span></span>

<span data-ttu-id="bae25-136">Следующие проблемы были исправлены:</span><span class="sxs-lookup"><span data-stu-id="bae25-136">The following issues have been fixed:</span></span>

- <span data-ttu-id="bae25-137">При выборе строки на основании проекта в предложении с расценками или контракте кнопка **Предложение** должна быть видна только при выборе линейки продуктов, связанных с существующим продуктом.</span><span class="sxs-lookup"><span data-stu-id="bae25-137">When selecting a project-based line in quote or contract, the **Suggestion** button should only be visible when selecting a product-based line associated with an existing product.</span></span>
- <span data-ttu-id="bae25-138">Разделить привилегию **Create_Product** с привилегией **Create_ProjectContract**.</span><span class="sxs-lookup"><span data-stu-id="bae25-138">Split **Create_Product** privilege from **Create_ProjectContract** privilege.</span></span>
- <span data-ttu-id="bae25-139">Удаление строки счета вызывает ошибку нулевой ссылки на **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span><span class="sxs-lookup"><span data-stu-id="bae25-139">Deleting an invoice line causes null reference failure on **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span></span>
