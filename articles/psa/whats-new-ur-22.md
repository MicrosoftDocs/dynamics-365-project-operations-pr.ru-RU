---
title: Что нового и что изменилось в выпуске-обновлении 22 Project Service Automation версии 3
description: В этом разделе перечислены функции и исправления, доступные в выпуске-обновлении 22 Project Service Automation версии 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.openlocfilehash: db4cbb9f9daadcb1911325f8bee987d5e480e1cf
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150999"
---
# <a name="project-service-automation-update-release-22-v3"></a><span data-ttu-id="f57e9-103">Выпуск-обновление 22 Project Service Automation, версия 3</span><span class="sxs-lookup"><span data-stu-id="f57e9-103">Project Service Automation Update Release 22, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="f57e9-104">Мы рады объявить о последнем обновлении приложения Project Service Automation для Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="f57e9-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="f57e9-105">Этот выпуск содержит некоторые важные усовершенствования, направленные на качество, производительность и удобство использования.</span><span class="sxs-lookup"><span data-stu-id="f57e9-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="f57e9-106">Этот выпуск совместим с Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="f57e9-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="f57e9-107">Чтобы обновить приложение до этого выпуска, посетите страницу решений Центра администрирования Dynamics 365 Online и установите обновление.</span><span class="sxs-lookup"><span data-stu-id="f57e9-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="f57e9-108">Дополнительные сведения см. в разделе [Установка, обновление или удаление предпочтительного решения](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="f57e9-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="f57e9-109">В этом разделе перечислены функции и исправления, появившиеся или изменившиеся в выпуске-обновлении 22 Project Service Automation версии 3.</span><span class="sxs-lookup"><span data-stu-id="f57e9-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 22.</span></span> <span data-ttu-id="f57e9-110">Эта версия имеет номер сборки V3.10.33.48 и стала доступна для широкой публики после автоматического обновления в июне 2020 г.</span><span class="sxs-lookup"><span data-stu-id="f57e9-110">This version has a build number of V 3.10.33.48 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-22"></a><span data-ttu-id="f57e9-111">Выпуск-обновление 22</span><span class="sxs-lookup"><span data-stu-id="f57e9-111">Update Release 22</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="f57e9-112">Исправленные ошибки</span><span class="sxs-lookup"><span data-stu-id="f57e9-112">Bug fixes</span></span>



<span data-ttu-id="f57e9-113">**Время и расходы**</span><span class="sxs-lookup"><span data-stu-id="f57e9-113">**Time and Expense**</span></span>

<span data-ttu-id="f57e9-114">Следующие проблемы были исправлены:</span><span class="sxs-lookup"><span data-stu-id="f57e9-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="f57e9-115">**Записи времени** не добавляются автоматически в расписание записей времени после импорта.</span><span class="sxs-lookup"><span data-stu-id="f57e9-115">**Time entries** are not automatically added in the Time entries schedule after import.</span></span>
- <span data-ttu-id="f57e9-116">Средство выбора даты сетки **Запись времени** не распознает региональные параметры пользователя.</span><span class="sxs-lookup"><span data-stu-id="f57e9-116">The **Time Entry** grid date picker does not recognize a user's regional settings.</span></span>

<span data-ttu-id="f57e9-117">**Управление ресурсами**</span><span class="sxs-lookup"><span data-stu-id="f57e9-117">**Resource Management**</span></span>

<span data-ttu-id="f57e9-118">Следующие проблемы были исправлены:</span><span class="sxs-lookup"><span data-stu-id="f57e9-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="f57e9-119">В ручном режиме меняется на **Назначение ресурсов**, профили не распознаются при создании **Требования ресурсов**.</span><span class="sxs-lookup"><span data-stu-id="f57e9-119">In manual mode, changes to **Resource Assignment** contours are not recognized when generating **Resource Requirements**.</span></span>
- <span data-ttu-id="f57e9-120">**Запросы ресурсов** не поддерживают настраиваемые статусы запросов.</span><span class="sxs-lookup"><span data-stu-id="f57e9-120">**Resource Requests** do not support custom request statuses.</span></span>

<span data-ttu-id="f57e9-121">**Управление проектами**</span><span class="sxs-lookup"><span data-stu-id="f57e9-121">**Project Management**</span></span>

<span data-ttu-id="f57e9-122">Следующие проблемы были исправлены:</span><span class="sxs-lookup"><span data-stu-id="f57e9-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="f57e9-123">При двойном щелчке EstimateGridControl не будут правильно проанализированы числа в нидерландском формате.</span><span class="sxs-lookup"><span data-stu-id="f57e9-123">Using double-click on EstimateGridControl will not correctly parse Dutch format numbers.</span></span>
- <span data-ttu-id="f57e9-124">Назначенные часы обновляются неправильно при изменении назначений с помощью надстройки клиента для настольного компьютера Microsoft Project.</span><span class="sxs-lookup"><span data-stu-id="f57e9-124">Assigned hours do not update correctly when assignments are changed using the Microsoft Project desktop client add-in.</span></span>
- <span data-ttu-id="f57e9-125">В сетках "Отслеживание проекта" и "Оценки" отображается неправильный код валюты продажи, если валюта контракта отличается от валюты клиента и организация настроена на отображение кодов валюты вместо символов валюты.</span><span class="sxs-lookup"><span data-stu-id="f57e9-125">Project Tracking and Estimates grids display incorrect sales currency code when contract currency is different than customer currency and organization is configured to display currency codes instead of currency symbols.</span></span>
- <span data-ttu-id="f57e9-126">К дате окончания участника рабочей группы добавляется один день, если расписание рабочих часов составляет 24 часа в сутки.</span><span class="sxs-lookup"><span data-stu-id="f57e9-126">A Team member's finish date will add one day if the work hour schedule is 24-hours per day.</span></span>
- <span data-ttu-id="f57e9-127">В расписании проекта добавление категории транзакции к задаче не запускает автосохранение.</span><span class="sxs-lookup"><span data-stu-id="f57e9-127">On the Project Schedule, adding a Transaction Category to a task does not trigger auto save.</span></span>
- <span data-ttu-id="f57e9-128">При добавлении участника рабочей группы в шаблон проекта отображается следующая ошибка: "Невозможно связать требования ресурсов с шаблонами проекта".</span><span class="sxs-lookup"><span data-stu-id="f57e9-128">The following error is displayed when adding a team member to the Project Template: "Resource requirements cannot be associated with project templates".</span></span> 
- <span data-ttu-id="f57e9-129">Сценарий правила ленты msdyn.Approval.CanApproveOrReject отображает ошибку тайм-аута.</span><span class="sxs-lookup"><span data-stu-id="f57e9-129">Ribbon rule script "msdyn.Approval.CanApproveOrReject" displays a timeout error.</span></span>

<span data-ttu-id="f57e9-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="f57e9-130">**Sales**</span></span>

<span data-ttu-id="f57e9-131">Следующие проблемы были исправлены:</span><span class="sxs-lookup"><span data-stu-id="f57e9-131">The following issues have been fixed:</span></span>

- <span data-ttu-id="f57e9-132">Сообщение об ошибке проверки не отображается при выборе прайс-листа стоимости при поиске прайс-листа в форме/объекте "Новый прайс-лист проекта предложения с расценками".</span><span class="sxs-lookup"><span data-stu-id="f57e9-132">Validation error message not displayed when a Cost Price List is selected in Price List lookup on 'New Quote Project Price List' form/entity.</span></span>
- <span data-ttu-id="f57e9-133">Закрытие предложения с расценками как реализованного не приводит к переходу к созданному контракту, если последовательность операций бизнес-процесса, прикрепленная к предложению с расценками, находится на конечной стадии.</span><span class="sxs-lookup"><span data-stu-id="f57e9-133">Closing the quote as won does not navigate to the created contract if a BPF attached to the quote is in the final stage.</span></span>
- <span data-ttu-id="f57e9-134">Реверсирование **Продажи без выставления счетов** связано с исходной стоимостью при вызове записи времени.</span><span class="sxs-lookup"><span data-stu-id="f57e9-134">Reversing **Unbilled Sales** is linked to original cost when a time entry is recalled.</span></span>
- <span data-ttu-id="f57e9-135">После нажатия кнопки **Подтвердить** статус счета не меняется на **Подтверждено**, пока не будет обновлен счет.</span><span class="sxs-lookup"><span data-stu-id="f57e9-135">After selecting the **Confirm** button, the invoice status doesn't change to **Confirmed** unless the invoice is refreshed.</span></span>
