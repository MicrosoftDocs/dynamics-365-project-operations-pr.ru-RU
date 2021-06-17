---
title: Что нового и что изменилось в выпуске-обновлении 21 Project Service Automation версии 3
description: В этом разделе перечислены функции и исправления, доступные в выпуске-обновлении 21 Project Service Automation версии 3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: dd894f27baac70238d0bd9e9b1a21a9a499e1ea7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002343"
---
# <a name="project-service-automation-update-release-21-v3"></a><span data-ttu-id="52b32-103">Выпуск-обновление 21 Project Service Automation, версия 3</span><span class="sxs-lookup"><span data-stu-id="52b32-103">Project Service Automation Update Release 21, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="52b32-104">Мы рады объявить о последнем обновлении приложения Project Service Automation для Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="52b32-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="52b32-105">Этот выпуск содержит некоторые важные усовершенствования, направленные на качество, производительность и удобство использования.</span><span class="sxs-lookup"><span data-stu-id="52b32-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="52b32-106">Этот выпуск совместим с Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="52b32-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="52b32-107">Чтобы обновить приложение до этого выпуска, посетите страницу решений Центра администрирования Dynamics 365 Online и установите обновление.</span><span class="sxs-lookup"><span data-stu-id="52b32-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="52b32-108">Дополнительные сведения см. в разделе [Установка, обновление или удаление предпочтительного решения](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="52b32-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="52b32-109">В этом разделе перечислены функции и исправления, появившиеся или изменившиеся в выпуске-обновлении 21 Project Service Automation версии 3.</span><span class="sxs-lookup"><span data-stu-id="52b32-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 21.</span></span> <span data-ttu-id="52b32-110">Эта версия имеет номер сборки V3.10.32.50 и стала доступна для широкой публики после автоматического обновления в июне 2020 г.</span><span class="sxs-lookup"><span data-stu-id="52b32-110">This version has a build number of V 3.10.32.50 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-21"></a><span data-ttu-id="52b32-111">Выпуск-обновление 21</span><span class="sxs-lookup"><span data-stu-id="52b32-111">Update Release 21</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="52b32-112">Исправленные ошибки</span><span class="sxs-lookup"><span data-stu-id="52b32-112">Bug fixes</span></span>

<span data-ttu-id="52b32-113">**Время и расходы**</span><span class="sxs-lookup"><span data-stu-id="52b32-113">**Time and Expense**</span></span>

<span data-ttu-id="52b32-114">Следующие проблемы были исправлены:</span><span class="sxs-lookup"><span data-stu-id="52b32-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="52b32-115">При размещении **Элемент управления сеткой записи времени** на панелях мониторинга сетка не использует всю ширину контейнера сетки панели мониторинга.</span><span class="sxs-lookup"><span data-stu-id="52b32-115">When hosting the **Time Entry Grid Control** in Dashboards, the grid does not utilize the full width of the dashboard grid container.</span></span>
- <span data-ttu-id="52b32-116">Для определенных часовых поясов элемент управления сетки **Запись времени** не отображает записи.</span><span class="sxs-lookup"><span data-stu-id="52b32-116">For specific time zones, the **Time Entry** grid control does not display records.</span></span>
- <span data-ttu-id="52b32-117">Записи времени после 21:00 отображаются не в тот день.</span><span class="sxs-lookup"><span data-stu-id="52b32-117">Time entries that are after 9:00 PM appear on the wrong day.</span></span>
- <span data-ttu-id="52b32-118">Пользователи не могут отправить расходы, если категория расходов **Требуется квитанция расхода** не имеет значения.</span><span class="sxs-lookup"><span data-stu-id="52b32-118">Users are unable to submit expenses if the expense category, **Expense receipt required** has no value.</span></span>

<span data-ttu-id="52b32-119">**Управление ресурсами**</span><span class="sxs-lookup"><span data-stu-id="52b32-119">**Resource Management**</span></span>

<span data-ttu-id="52b32-120">Следующие проблемы были исправлены:</span><span class="sxs-lookup"><span data-stu-id="52b32-120">The following issues have been fixed:</span></span>

- <span data-ttu-id="52b32-121">Неактивные резервирования отображаются в представлении **Выверка**.</span><span class="sxs-lookup"><span data-stu-id="52b32-121">Inactive bookings are displayed in the **Reconciliation** view.</span></span>
- <span data-ttu-id="52b32-122">Отсутствовала проверка обеспечения универсального ресурса для гарантии того, что существует действительный статус резервирования.</span><span class="sxs-lookup"><span data-stu-id="52b32-122">Generic resource fulfillment was missing validation to ensure that a valid booking status exists.</span></span>

<span data-ttu-id="52b32-123">**Управление проектами**</span><span class="sxs-lookup"><span data-stu-id="52b32-123">**Project Management**</span></span>

<span data-ttu-id="52b32-124">Следующие проблемы были исправлены:</span><span class="sxs-lookup"><span data-stu-id="52b32-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="52b32-125">Сетки формы **Проект** (**Назначение ресурсов**, **Задача**, представление **Выверка**, **Оценки расходов**) остаются доступными для редактирования, даже если проект неактивен.</span><span class="sxs-lookup"><span data-stu-id="52b32-125">The **Project** form grids (**Resource Assignment**, **Task**, **Reconciliation** view, **Expense Estimates**) remain editable even when a project is not active.</span></span>
- <span data-ttu-id="52b32-126">Повторяющихся клиентов невозможно объединить с клиентами, которые связаны с подтвержденными контрактами по проекту.</span><span class="sxs-lookup"><span data-stu-id="52b32-126">Duplicate customers can't be merged with customers that are linked to confirmed project contracts.</span></span>
- <span data-ttu-id="52b32-127">Если в ресурс не добавлен действительный календарь, система не возвращает понятное сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="52b32-127">When a resource who does not have a valid calendar is added, the system does not return a user friendly-error message.</span></span>
- <span data-ttu-id="52b32-128">Кнопка **Добавить задачу** в сетке задач активна, когда проект связан с **Надстройка Microsoft Project**.</span><span class="sxs-lookup"><span data-stu-id="52b32-128">The **Add Task** button on the task grid is enabled when the project is linked to **Microsoft Project add-in**.</span></span>
- <span data-ttu-id="52b32-129">Усилия бесконтрольно растут, когда задача с категорией назначена ресурсу с ролью, для которой определена себестоимость.</span><span class="sxs-lookup"><span data-stu-id="52b32-129">Effort grows uncontrollably when a task with a category is assigned to a resource with a role for which there is a cost price defined.</span></span>

<span data-ttu-id="52b32-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="52b32-130">**Sales**</span></span>

<span data-ttu-id="52b32-131">Внесены следующие усовершенствования:</span><span class="sxs-lookup"><span data-stu-id="52b32-131">The following enhancements have been made:</span></span>

- <span data-ttu-id="52b32-132">**Периодичность выставления счетов** и **Дата начала выставления счетов** перемещены на вкладку **Расписание счета**.</span><span class="sxs-lookup"><span data-stu-id="52b32-132">**Invoice Frequency** and **Billing Start** have been moved to the **Invoice Schedule** tab.</span></span>

<span data-ttu-id="52b32-133">Следующие проблемы были исправлены:</span><span class="sxs-lookup"><span data-stu-id="52b32-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="52b32-134">**Общая цена продажи** равна нулю (0) для параметра **Категория**, даже когда **Роль** имеет общую цену продажи, отличную от нуля.</span><span class="sxs-lookup"><span data-stu-id="52b32-134">**Total Sales Price** is zero (0) for **Category** even though **Role** has a total sales price that is not zero.</span></span>
- <span data-ttu-id="52b32-135">Клиенты не могут изменить значение поля **Статус счета** поле на **Готово для выставления счетов**, если другой настроенный процесс обновляет дополнительное поле.</span><span class="sxs-lookup"><span data-stu-id="52b32-135">Customers can't change the value of the **Invoice Status** field to **Ready for invoicing** when another customized process is updating an additional field.</span></span>
- <span data-ttu-id="52b32-136">Кнопка **Обновить строки счета** может создать несколько дублированных строк, если ее нажимать повторно.</span><span class="sxs-lookup"><span data-stu-id="52b32-136">The **Refresh Invoice Lines** button can create multiple duplicated lines if it is repeatedly selected.</span></span>
- <span data-ttu-id="52b32-137">Кнопка **Обновить цены** не работает во вложенной сетке **Цены ролей** в форме **Быстрый просмотр**.</span><span class="sxs-lookup"><span data-stu-id="52b32-137">The **Update Prices** button doesn't work on the **Role Prices** subgrid in the **Quick View** form.</span></span>
- <span data-ttu-id="52b32-138">Логика **Разрешение прайс-листа продаж** неправильно обрабатывает часовые пояса, что приводит к неправильному выбору прайс-листов.</span><span class="sxs-lookup"><span data-stu-id="52b32-138">The **Sales Price List Resolution** logic improperly handles time zones, resulting in the incorrect selection of price lists.</span></span>
- <span data-ttu-id="52b32-139">**Общая фактическая стоимость** проекта может отличаться на незначительную сумму после утверждения однократной записи.</span><span class="sxs-lookup"><span data-stu-id="52b32-139">A project’s **Total Actual Cost** can be off by a fractional amount after a single time entry is approved.</span></span>
- <span data-ttu-id="52b32-140">Логика **Разрешение цены** не предоставляет понятное сообщение об ошибке, если **Полученная цена роли** не имеет значения в полях **Базовая единица** и **Цена в базовой единице**.</span><span class="sxs-lookup"><span data-stu-id="52b32-140">The **Price Resolution** logic does not provide a user-friendly error message if **Retrieved RolePrice** doesn't have values in **'Primary Unit'** and **'Price In Primary Unit'** fields.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]