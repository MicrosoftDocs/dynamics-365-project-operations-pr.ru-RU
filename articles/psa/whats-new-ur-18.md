---
title: Что нового и что изменилось в выпуске-обновлении 18 для Project Service Automation версии 3
description: В этом разделе перечислены функции и исправления, доступные в выпуске-обновлении 18 для Project Service Automation версии 3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: f7def50e77a83fd790b81b1b4fd36008ce293b0c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006662"
---
# <a name="project-service-automation-update-release-18-v3"></a><span data-ttu-id="f9b08-103">Выпуск-обновление 18 Project Service Automation, версия 3</span><span class="sxs-lookup"><span data-stu-id="f9b08-103">Project Service Automation Update Release 18, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="f9b08-104">Мы рады объявить о последнем обновлении приложения Project Service Automation для Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="f9b08-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="f9b08-105">Этот выпуск содержит некоторые важные усовершенствования, направленные на качество, производительность и удобство использования.</span><span class="sxs-lookup"><span data-stu-id="f9b08-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="f9b08-106">Этот выпуск совместим с Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="f9b08-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="f9b08-107">Чтобы обновить приложение до этого выпуска, посетите Центр администрирования Dynamics 365 Online, страницу решений, чтобы установить обновление.</span><span class="sxs-lookup"><span data-stu-id="f9b08-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="f9b08-108">Дополнительные сведения см. в разделе [Установка, обновление или удаление предпочтительного решения](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="f9b08-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="f9b08-109">В этом разделе перечислены функции и исправления, появившиеся или изменившиеся в выпуске-обновлении 18 для Project Service Automation версии 3.</span><span class="sxs-lookup"><span data-stu-id="f9b08-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 18.</span></span> <span data-ttu-id="f9b08-110">Эта версия имеет номер сборки V3.10.8.12 и доступна для широкой публики после автоматического обновления в апреле 2020 г.</span><span class="sxs-lookup"><span data-stu-id="f9b08-110">This version has a build number of V3.10.8.12 and is generally available through a self-update in April 2020.</span></span>

## <a name="update-release-18"></a><span data-ttu-id="f9b08-111">Выпуск-обновление 18</span><span class="sxs-lookup"><span data-stu-id="f9b08-111">Update Release 18</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="f9b08-112">Исправленные ошибки</span><span class="sxs-lookup"><span data-stu-id="f9b08-112">Bug fixes</span></span>

<span data-ttu-id="f9b08-113">**Время и расходы**</span><span class="sxs-lookup"><span data-stu-id="f9b08-113">**Time and Expense**</span></span>

- <span data-ttu-id="f9b08-114">Исправлено: потоки **Отозвать**, **Запросить** и **Отменить утверждение** создают исключения с непонятными сообщениями об ошибках.</span><span class="sxs-lookup"><span data-stu-id="f9b08-114">Fixed: **Recall**, **Request**, and **Cancel Approval** flows throw exceptions with unclear error messages.</span></span>
- <span data-ttu-id="f9b08-115">Исправлено: в случае сбоя **Отменить утверждение** для расхода соответствующая ошибка с исключением не создается.</span><span class="sxs-lookup"><span data-stu-id="f9b08-115">Fixed: When **Cancel Approval** fails for an expense, a relevant exception error is not thrown.</span></span>
- <span data-ttu-id="f9b08-116">Исправлено: сетка "Запись времени" неправильно обрабатывает нерабочие дни в Австралии после перехода на летнее время в октябре.</span><span class="sxs-lookup"><span data-stu-id="f9b08-116">Fixed: The Time Entry grid incorrectly handles non-working days in Australia after the daylight savings time (DST) switch in October.</span></span>
- <span data-ttu-id="f9b08-117">Исправлено: неверная логика по умолчанию препятствует отправке расходов.</span><span class="sxs-lookup"><span data-stu-id="f9b08-117">Fixed: Incorrect defaulting logic prevents submission of expenses.</span></span>
- <span data-ttu-id="f9b08-118">Исправлено: в случае сбоя утверждения записи времени утверждение остается в состоянии **Ожидание**.</span><span class="sxs-lookup"><span data-stu-id="f9b08-118">Fixed: When time entry approval fails, the approval remains in a state of **Pending**.</span></span>
- <span data-ttu-id="f9b08-119">Исправлено: ошибки SQL при массовых утверждениях (взаимоблокировка/тайм-аут).</span><span class="sxs-lookup"><span data-stu-id="f9b08-119">Fixed: SQL Errors on bulk approvals (deadlock/timeout).</span></span>
- <span data-ttu-id="f9b08-120">Исправлено: значительные проблемы с производительностью в пользовательском интерфейсе, вызванные обновлением участников рабочей группы при утверждении записей времени.</span><span class="sxs-lookup"><span data-stu-id="f9b08-120">Fixed: Significant performance issues in the user experience caused by updating team members while approving time entries.</span></span>

<span data-ttu-id="f9b08-121">**Управление проектами**</span><span class="sxs-lookup"><span data-stu-id="f9b08-121">**Project Management**</span></span>

- <span data-ttu-id="f9b08-122">Исправлено: уведомление о часовом поясе перемещено из представления **Выверка** в основную форму **Проект**.</span><span class="sxs-lookup"><span data-stu-id="f9b08-122">Fixed: Time zone notification moved from the **Reconciliation** view to the **Project** main form.</span></span>
- <span data-ttu-id="f9b08-123">Исправлено: шаблон календаря неправильно сбрасывается до значений по умолчанию при открытии новой формы проекта.</span><span class="sxs-lookup"><span data-stu-id="f9b08-123">Fixed: Calendar template is not correctly defaulting when a new project form opens.</span></span>
- <span data-ttu-id="f9b08-124">Исправлено: в браузерах на основе Chromium пользователи не могут легко выбирать предшествующие задачи для удаления.</span><span class="sxs-lookup"><span data-stu-id="f9b08-124">Fixed: For chromium-based browsers, users are unable to easily select predecessor tasks to delete.</span></span>
- <span data-ttu-id="f9b08-125">Исправлено: при создании или копировании **Проект из пустого шаблона** извлекаются несвязанные назначения.</span><span class="sxs-lookup"><span data-stu-id="f9b08-125">Fixed: Creating or copying **Project from Empty template** fetches unrelated assignments.</span></span>
- <span data-ttu-id="f9b08-126">Исправлено: в определенных пограничных случаях создание нового назначения из сетки задач приводит к созданию дублирующихся записей.</span><span class="sxs-lookup"><span data-stu-id="f9b08-126">Fixed: In specific edge cases, creating a new assignment from the task grid results in duplicate records being created.</span></span>
- <span data-ttu-id="f9b08-127">Исправлено: в ручном режиме пользователи не могут обновлять даты начала задачи так, чтобы они были позже текущей сохраненной даты.</span><span class="sxs-lookup"><span data-stu-id="f9b08-127">Fixed: In manual mode, users are unable to update task start dates to be later than the current date saved.</span></span>

<span data-ttu-id="f9b08-128">**Управление ресурсами**</span><span class="sxs-lookup"><span data-stu-id="f9b08-128">**Resource Management**</span></span>

- <span data-ttu-id="f9b08-129">Исправлено: в строке промежуточных итогов представления **Выверка** неверно рассчитывается отклонение резервирования после расширения резервирований.</span><span class="sxs-lookup"><span data-stu-id="f9b08-129">Fixed: **Reconciliation** view subtotal row incorrectly calculates bookings variance after extending bookings.</span></span>
- <span data-ttu-id="f9b08-130">Исправлено: в представлении **Выверка** неправильно отображаются назначения ресурсов, когда у резервируемое ресурса есть календарь, несоответствующий календарю проекта.</span><span class="sxs-lookup"><span data-stu-id="f9b08-130">Fixed: **Reconciliation** view incorrectly displays resource assignments when the bookable resource has a calendar that does not match the project calendar.</span></span>

<span data-ttu-id="f9b08-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="f9b08-131">**Sales**</span></span>

- <span data-ttu-id="f9b08-132">Исправлено: при повторном утверждении записей времени (**Утвердить > Отмена >** Утвердить снова) создается дублирующее не подлежащее оплате фактическое значение.</span><span class="sxs-lookup"><span data-stu-id="f9b08-132">Fixed: When time entries are re-approved (**Approve > Cancel >** approve again), a duplicate non-chargeable actual is created.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]