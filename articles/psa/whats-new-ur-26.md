---
title: Что нового или измененного в выпуске обновления 26 для Project Service Automation версии V3
ms.openlocfilehash: 849e7288ee91d3e9360c0b03f6b8b37ff29338e7
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643279"
---
<a name="project-service-automation-update-release-26-v3"></a><span data-ttu-id="f2b86-102">Выпуск обновления 26 для Project Service Automation, версия V3</span><span class="sxs-lookup"><span data-stu-id="f2b86-102">Project Service Automation Update Release 26, V3</span></span>
================================================

<span data-ttu-id="f2b86-103">Мы рады объявить о последнем обновлении приложения Project Service Automation для Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="f2b86-103">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="f2b86-104">Этот выпуск содержит некоторые важные усовершенствования, направленные на качество, производительность и удобство использования.</span><span class="sxs-lookup"><span data-stu-id="f2b86-104">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="f2b86-105">Этот выпуск совместим с Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="f2b86-105">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="f2b86-106">Чтобы обновить приложение до этого выпуска, посетите страницу решений Центра администрирования Dynamics 365 Online и установите обновление.</span><span class="sxs-lookup"><span data-stu-id="f2b86-106">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="f2b86-107">Дополнительные сведения см. в разделе [Установка, обновление или удаление предпочтительного решения](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="f2b86-107">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="f2b86-108">В этом разделе перечислены функции и исправления, появившиеся или изменившиеся в выпуске обновления 26 для Project Service Automation версии V3.</span><span class="sxs-lookup"><span data-stu-id="f2b86-108">This topic lists the features and fixes that are new or changed for Project Service Automation Update Release 26, V3.</span></span> <span data-ttu-id="f2b86-109">Эта версия имеет номер сборки V3.10.44.59 и обычно доступна через самостоятельное обновление в декабре 2020 года.</span><span class="sxs-lookup"><span data-stu-id="f2b86-109">This version has a build number of V3.10.44.59 and is generally available through a self-update in December 2020.</span></span>

<a name="update-release-26"></a><span data-ttu-id="f2b86-110">Выпуск-обновление 26</span><span class="sxs-lookup"><span data-stu-id="f2b86-110">Update Release 26</span></span>
-----------------

### <a name="bug-fixes"></a><span data-ttu-id="f2b86-111">Исправленные ошибки</span><span class="sxs-lookup"><span data-stu-id="f2b86-111">Bug fixes</span></span>

<span data-ttu-id="f2b86-112">**Время и расходы**</span><span class="sxs-lookup"><span data-stu-id="f2b86-112">**Time and Expense**</span></span>

<span data-ttu-id="f2b86-113">Следующие проблемы были исправлены:</span><span class="sxs-lookup"><span data-stu-id="f2b86-113">The following issues have been fixed:</span></span>

-   <span data-ttu-id="f2b86-114">Пользователи могут изменить задачу на запись времени, которая была утверждена/отправлена.</span><span class="sxs-lookup"><span data-stu-id="f2b86-114">Users are able to change the task on a time entry that has been approved/submitted.</span></span>

-   <span data-ttu-id="f2b86-115">Ошибка «Ссылка на объект не указана» при сохранении записи времени.</span><span class="sxs-lookup"><span data-stu-id="f2b86-115">"Object Reference Not Set" error when saving time entry.</span></span>

-   <span data-ttu-id="f2b86-116">Импорт записи времени из назначений ресурсов создает записи времени с неправильными значениями DateTime.</span><span class="sxs-lookup"><span data-stu-id="f2b86-116">Time entry import from resource assignments creates time entries with the incorrect DateTime values.</span></span>

-   <span data-ttu-id="f2b86-117">Когда установлены приложения Project Service Automation и Field Service, кнопка **Создать** дважды отображается на панели команд для записей времени в приложении Field Service.</span><span class="sxs-lookup"><span data-stu-id="f2b86-117">When Project Service Automation and the Field Service app are both installed, the **New** button is displaying twice on the command bar for time entries in the Field Service app.</span></span>

-   <span data-ttu-id="f2b86-118">Обновления ячеек **Разрешить единицу измерения** и **Группа единиц измерения** в сетке **Оценки расходов**.</span><span class="sxs-lookup"><span data-stu-id="f2b86-118">**Allow Unit** and **Unit group** cells updates now work on the **Expense Estimates** grid.</span></span>

-   <span data-ttu-id="f2b86-119">Форма **Обновить изменение записи времени** включает **временная шкала**.</span><span class="sxs-lookup"><span data-stu-id="f2b86-119">**Update Time Entry Edit** form includes **Timeline**.</span></span>

-   <span data-ttu-id="f2b86-120">Утверждение времени для несвязанных с проектом записей времени блокирует систему при поиске роли утверждающего проект.</span><span class="sxs-lookup"><span data-stu-id="f2b86-120">Time approval for non-project time entries blocks the system when searching for a project approver role.</span></span>

<span data-ttu-id="f2b86-121">**Управление ресурсами**</span><span class="sxs-lookup"><span data-stu-id="f2b86-121">**Resource Management**</span></span>

<span data-ttu-id="f2b86-122">Следующие проблемы были исправлены:</span><span class="sxs-lookup"><span data-stu-id="f2b86-122">The following issues have been fixed:</span></span>

-   <span data-ttu-id="f2b86-123">Добавлена проверка в подключаемый модуль **PostProjectCreate**, чтобы проверить наличие основного требования перед его созданием.</span><span class="sxs-lookup"><span data-stu-id="f2b86-123">Added validation in the **PostProjectCreate** plug-in to check for a primary requirement before creating one.</span></span>

-   <span data-ttu-id="f2b86-124">Форма быстрого создания **Участник рабочей группы проекта** выдает исключение пустой ссылки, если поля удаляются из формы.</span><span class="sxs-lookup"><span data-stu-id="f2b86-124">**Project Team Member** quick create form throws a null reference exception if fields are removed from the form.</span></span>

-   <span data-ttu-id="f2b86-125">Создать требования на 12 часов за 1 год не удастся.</span><span class="sxs-lookup"><span data-stu-id="f2b86-125">Generate requirements for 12 hours over 1 year will fail.</span></span>

-   <span data-ttu-id="f2b86-126">Улучшено сообщение об ошибке исключение нулевой ссылки во время создания требования ресурса.</span><span class="sxs-lookup"><span data-stu-id="f2b86-126">Improved error message null reference exception during resource requirement creation.</span></span>

<span data-ttu-id="f2b86-127">**Управление проектами**</span><span class="sxs-lookup"><span data-stu-id="f2b86-127">**Project Management**</span></span>

<span data-ttu-id="f2b86-128">Следующие проблемы были исправлены:</span><span class="sxs-lookup"><span data-stu-id="f2b86-128">The following issues have been fixed:</span></span>

-   <span data-ttu-id="f2b86-129">Улучшенная проверка для устранения исключения нулевой ссылки, созданного в подключаемый модуль **PreProjectUpdate**.</span><span class="sxs-lookup"><span data-stu-id="f2b86-129">Improved validation to address null reference exception generated in the **PreProjectUpdate** plug-in.</span></span>

-   <span data-ttu-id="f2b86-130">Проекты, опубликованные надстройкой рабочего стола Microsoft Project, удаляют неназначенные назначения.</span><span class="sxs-lookup"><span data-stu-id="f2b86-130">Projects published by the Microsoft Project desktop add-in delete unassigned assignments.</span></span>

-   <span data-ttu-id="f2b86-131">Добавлена новая проверка, когда ссылка на проект задачи недействительна из-за исключения нулевой ссылки в подключаемый модуль **PreValidateProjectTaskUpdate**.</span><span class="sxs-lookup"><span data-stu-id="f2b86-131">Added new validation when a task’s project reference is invalid due to null reference exception in **PreValidateProjectTaskUpdate** plug-in.</span></span>

-   <span data-ttu-id="f2b86-132">Сетка участников рабочей группы не показывает отдельных назначений в записи участника рабочей группы.</span><span class="sxs-lookup"><span data-stu-id="f2b86-132">Team Member grid does not show distinct assignments on the team member record.</span></span>

-   <span data-ttu-id="f2b86-133">Добавлены новые сообщения о проверке и ошибках из-за исключения нулевой ссылки в подключаемый модуль **PreProjectTaskDelete**.</span><span class="sxs-lookup"><span data-stu-id="f2b86-133">Added new validation and error messages due to null reference exception in **PreProjectTaskDelete** plug-in.</span></span>

<span data-ttu-id="f2b86-134">**Sales**</span><span class="sxs-lookup"><span data-stu-id="f2b86-134">**Sales**</span></span>

<span data-ttu-id="f2b86-135">Следующие проблемы были исправлены:</span><span class="sxs-lookup"><span data-stu-id="f2b86-135">The following issues have been fixed:</span></span>

-   <span data-ttu-id="f2b86-136">При выборе строки на основании проекта в предложении с расценками или контракте кнопка **Предложение** должна быть видна только при выборе линейки продуктов, связанных с существующим продуктом.</span><span class="sxs-lookup"><span data-stu-id="f2b86-136">When selecting a project-based line in quote or contract, the **Suggestion** button should only be visible when selecting a product-based line associated with an existing product.</span></span>

-   <span data-ttu-id="f2b86-137">Разделить привилегию **Create_Product** с привилегией **Create_ProjectContract**.</span><span class="sxs-lookup"><span data-stu-id="f2b86-137">Split **Create_Product** privilege from **Create_ProjectContract** privilege.</span></span>

-   <span data-ttu-id="f2b86-138">Удаление строки счета вызывает ошибку нулевой ссылки на **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span><span class="sxs-lookup"><span data-stu-id="f2b86-138">Deleting an invoice line causes null reference failure on **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span></span>
