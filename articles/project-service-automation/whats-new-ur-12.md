---
title: Что нового и что изменилось в выпуске-обновлении 12 для Project Service Automation версии 3
description: В этом разделе приведены сведения о новых возможностях в выпуске-обновлении 12 для Project Service Automation версии 3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: af8dbfe3-7ce9-4374-9c03-17b2e1d6ac32
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 758717562c12a72848f1a874fa8b1171139ebb0c
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754956"
---
# <a name="project-service-automation-v3-update-release-12"></a><span data-ttu-id="ef7c4-103">Project Service Automation версии 3, выпуск-обновление 12</span><span class="sxs-lookup"><span data-stu-id="ef7c4-103">Project Service Automation V3, Update Release 12</span></span>
<span data-ttu-id="ef7c4-104">С удовольствием объявляем о выходе последнего обновления для приложения Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="ef7c4-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="ef7c4-105">Этот выпуск содержит некоторые важные усовершенствования, направленные на качество, производительность и удобство использования.</span><span class="sxs-lookup"><span data-stu-id="ef7c4-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="ef7c4-106">Этот выпуск совместим с Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="ef7c4-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="ef7c4-107">Чтобы обновить приложение до этого выпуска, посетите Центр администрирования Dynamics 365 Online и перейдите на страницу решений, чтобы установить обновление.</span><span class="sxs-lookup"><span data-stu-id="ef7c4-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="ef7c4-108">Дополнительные сведения см. в разделе [Установка, обновление или удаление предпочтительного решения](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="ef7c4-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="ef7c4-109">В этом разделе перечислены функции и исправления, появившиеся или изменившиеся в выпуске-обновлении 12 для Project Service Automation версии 3.</span><span class="sxs-lookup"><span data-stu-id="ef7c4-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 12.</span></span> <span data-ttu-id="ef7c4-110">Эта версия имеет номер сборки V3.10.2.34 и становится доступна широкому кругу клиентов посредством самостоятельного обновления в октябре 2019 года.</span><span class="sxs-lookup"><span data-stu-id="ef7c4-110">This version has a build number of V3.10.2.34 and is generally available through a self-update in October 2019.</span></span>

## <a name="update-release-12"></a><span data-ttu-id="ef7c4-111">Выпуск-обновление 12</span><span class="sxs-lookup"><span data-stu-id="ef7c4-111">Update Release 12</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="ef7c4-112">Исправления ошибок</span><span class="sxs-lookup"><span data-stu-id="ef7c4-112">Bug fixes</span></span>

- <span data-ttu-id="ef7c4-113">Время и расходы</span><span class="sxs-lookup"><span data-stu-id="ef7c4-113">Time and Expense</span></span>

    - <span data-ttu-id="ef7c4-114">Исправлено: сообщения об ошибках при записи времени обновлены и теперь содержат больше контекста.</span><span class="sxs-lookup"><span data-stu-id="ef7c4-114">Fixed: Time entry error messaging has been updated with more relevant context.</span></span>
    - <span data-ttu-id="ef7c4-115">Исправлено: в сетке записи времени и расписании правильно отображается вертикальная полоса прокрутки, когда она необходима.</span><span class="sxs-lookup"><span data-stu-id="ef7c4-115">Fixed: Time entry grid and schedule correctly displays the vertical scrollbar when required.</span></span>
    - <span data-ttu-id="ef7c4-116">Исправлено: отправленные записи расходов и времени можно утверждать.</span><span class="sxs-lookup"><span data-stu-id="ef7c4-116">Fixed: Submitted expense and time entries can be approved.</span></span>
    - <span data-ttu-id="ef7c4-117">Исправлено: сообщение в диалоговом окне подтверждения "Отменить утверждение" теперь отражает изменение статуса утверждения с **Утверждено** на **Отправлено**.</span><span class="sxs-lookup"><span data-stu-id="ef7c4-117">Fixed: Cancel approval confirmation dialog message has been corrected to reflect the status of the approval when changed from **Approved** to **Submitted**.</span></span>
    - <span data-ttu-id="ef7c4-118">Исправлено: поля **Цена**, **Единица измерения** и **Количество** в записи расходов блокируются после утверждения записи.</span><span class="sxs-lookup"><span data-stu-id="ef7c4-118">Fixed: **Price**, **Unit**, and **Quantity** fields are now locked on the Expense record after it is has been approved.</span></span>

- <span data-ttu-id="ef7c4-119">Управление проектами</span><span class="sxs-lookup"><span data-stu-id="ef7c4-119">Project Management</span></span>

    - <span data-ttu-id="ef7c4-120">Исправлено: действие **Создать** в главной форме **Участник рабочей группы** удалено.</span><span class="sxs-lookup"><span data-stu-id="ef7c4-120">Fixed: **New** action on **Team member** main form has been removed.</span></span>
    - <span data-ttu-id="ef7c4-121">Исправлено: в назначениях ресурсов теперь учитываются ошибки неточного округления, из-за которых сдвигается дата окончания задачи.</span><span class="sxs-lookup"><span data-stu-id="ef7c4-121">Fixed: Resource assignments have been updated to account for inaccurate rounding errors, which lead to a shift in a task’s end date.</span></span>
    - <span data-ttu-id="ef7c4-122">Исправлено: в таблице задач ошибки на стороне сервера теперь отображаются для пользователя, если это релевантно.</span><span class="sxs-lookup"><span data-stu-id="ef7c4-122">Fixed: In the task grid, relevant server-side errors will be surfaced to the user.</span></span>
    - <span data-ttu-id="ef7c4-123">Исправлено: в средстве выбора людей для задачи теперь отрисовываются имена участников рабочей группы, а не их должности.</span><span class="sxs-lookup"><span data-stu-id="ef7c4-123">Fixed: The team member’s name now renders in the task people picker instead of the position name.</span></span>

- <span data-ttu-id="ef7c4-124">Управление ресурсами</span><span class="sxs-lookup"><span data-stu-id="ef7c4-124">Resource Management</span></span>

    - <span data-ttu-id="ef7c4-125">Исправлено: в сведениях требования ресурса для проектов, создаваемых по шаблону, теперь используется календарь проекта.</span><span class="sxs-lookup"><span data-stu-id="ef7c4-125">Fixed: Resource requirement details for projects created from a template now use the project calendar.</span></span>
    - <span data-ttu-id="ef7c4-126">Исправлено: в создаваемое для роли требование ресурса теперь по умолчанию подставляются навыки и компетенции из основных данных этой роли.</span><span class="sxs-lookup"><span data-stu-id="ef7c4-126">Fixed: Skills and competencies now default from role master data to the resource requirement created for that role.</span></span>

- <span data-ttu-id="ef7c4-127">Sales</span><span class="sxs-lookup"><span data-stu-id="ef7c4-127">Sales</span></span>

    - <span data-ttu-id="ef7c4-128">Исправлено: дублирующиеся идентификаторы объектов в главной форме **Контракт**.</span><span class="sxs-lookup"><span data-stu-id="ef7c4-128">Fixed: Duplicate object IDs found on the **Contract main** form.</span></span>
    - <span data-ttu-id="ef7c4-129">Исправлено: логика обновлена так, чтобы вкладка **Анализ предложения с расценками** отображалась и на ней была видна настройка метаданных вкладки.</span><span class="sxs-lookup"><span data-stu-id="ef7c4-129">Fixed: Logic has been updated to make the **Quote Analysis** tab visible so that it displays the metadata setup of the tab.</span></span>
    - <span data-ttu-id="ef7c4-130">Исправлено: дата учета в записи фактических данных теперь определяется датой записи времени/расхода, а не датой утверждения.</span><span class="sxs-lookup"><span data-stu-id="ef7c4-130">Fixed: Accounting date on the actual record now comes from the date of the time/expense entry date and not the date of the approval.</span></span>
