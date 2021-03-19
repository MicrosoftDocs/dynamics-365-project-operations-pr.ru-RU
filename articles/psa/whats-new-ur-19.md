---
title: Что нового и что изменилось в выпуске-обновлении 19 для Project Service Automation версии 3
description: В этом разделе перечислены функции и исправления, доступные в выпуске-обновлении 19 для Project Service Automation версии 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: b9baeca9e79e233c25a6310e426d755b9162bbad
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280729"
---
# <a name="project-service-automation-update-release-19-v3"></a><span data-ttu-id="c29ac-103">Выпуск-обновление 19 Project Service Automation, версия 3</span><span class="sxs-lookup"><span data-stu-id="c29ac-103">Project Service Automation Update Release 19, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="c29ac-104">Мы рады объявить о последнем обновлении приложения Project Service Automation для Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="c29ac-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="c29ac-105">Этот выпуск содержит некоторые важные усовершенствования, направленные на качество, производительность и удобство использования.</span><span class="sxs-lookup"><span data-stu-id="c29ac-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="c29ac-106">Этот выпуск совместим с Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="c29ac-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="c29ac-107">Чтобы обновить приложение до этого выпуска, посетите страницу решений Центра администрирования Dynamics 365 Online и установите обновление.</span><span class="sxs-lookup"><span data-stu-id="c29ac-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="c29ac-108">Дополнительные сведения см. в разделе [Установка, обновление или удаление предпочтительного решения](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="c29ac-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="c29ac-109">В этом разделе перечислены функции и исправления, появившиеся или изменившиеся в выпуске-обновлении 19 для PSA версии 3.</span><span class="sxs-lookup"><span data-stu-id="c29ac-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 19.</span></span> <span data-ttu-id="c29ac-110">Эта версия имеет номер сборки V3.10.30.41 и доступна для широкой публики после автоматического обновления в мае 2020 г.</span><span class="sxs-lookup"><span data-stu-id="c29ac-110">This version has a build number of V3.10.30.41 and is generally available through a self-update in May 2020.</span></span>

## <a name="update-release-19"></a><span data-ttu-id="c29ac-111">Выпуск-обновление 19</span><span class="sxs-lookup"><span data-stu-id="c29ac-111">Update Release 19</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="c29ac-112">Исправленные ошибки</span><span class="sxs-lookup"><span data-stu-id="c29ac-112">Bug fixes</span></span>

<span data-ttu-id="c29ac-113">**Время и расходы**</span><span class="sxs-lookup"><span data-stu-id="c29ac-113">**Time and Expense**</span></span>

<span data-ttu-id="c29ac-114">Следующие проблемы были исправлены:</span><span class="sxs-lookup"><span data-stu-id="c29ac-114">The following issues have been fixed:</span></span> 

- <span data-ttu-id="c29ac-115">Ошибки при импорте записей времени отображаются неправильно.</span><span class="sxs-lookup"><span data-stu-id="c29ac-115">Errors derived from time entry imports are not surfaced correctly.</span></span>
- <span data-ttu-id="c29ac-116">Сетка записи времени не поддерживает работу поля **Только дата**.</span><span class="sxs-lookup"><span data-stu-id="c29ac-116">Time Entry Grid does not support **Date Only** field behavior.</span></span>
- <span data-ttu-id="c29ac-117">Ресурсы проекта не могут создавать расходы, связанные с проектом.</span><span class="sxs-lookup"><span data-stu-id="c29ac-117">Project Resources are unable to create an expense with a project.</span></span>

<span data-ttu-id="c29ac-118">**Управление проектами**</span><span class="sxs-lookup"><span data-stu-id="c29ac-118">**Project Management**</span></span>

<span data-ttu-id="c29ac-119">Следующие проблемы были исправлены:</span><span class="sxs-lookup"><span data-stu-id="c29ac-119">The following issues have been fixed:</span></span> 

-  <span data-ttu-id="c29ac-120">Дочерняя задача второго уровня приводит к неправильной оценке трудозатрат во время расчета ПОПЗ.</span><span class="sxs-lookup"><span data-stu-id="c29ac-120">Grandchild task causes an incorrect effort estimate during the Completion (EAC) Calculation.</span></span>

<span data-ttu-id="c29ac-121">**Sales**</span><span class="sxs-lookup"><span data-stu-id="c29ac-121">**Sales**</span></span>

<span data-ttu-id="c29ac-122">Следующие проблемы были исправлены:</span><span class="sxs-lookup"><span data-stu-id="c29ac-122">The following issues have been fixed:</span></span> 

- <span data-ttu-id="c29ac-123">Действие **Пересчитать** не работает со сведениями строки контракта расходов или строки предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="c29ac-123">The **Recalculate** action does not work with expense contract line details or quote line details.</span></span>
- <span data-ttu-id="c29ac-124">**Обновить цены** отсутствует для оценки расходов.</span><span class="sxs-lookup"><span data-stu-id="c29ac-124">**Update Prices** is missing for expense estimates.</span></span>
-  <span data-ttu-id="c29ac-125">Клиенты не могут выбрать пользовательские причины состояния контракта на странице **Контракт по проекту**.</span><span class="sxs-lookup"><span data-stu-id="c29ac-125">Customers are unable to select custom contract status reasons from the **Project Contract** page.</span></span>
- <span data-ttu-id="c29ac-126">Клиенты замечают снижение производительности при создании собственного прайс-листа из предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="c29ac-126">Customers experience degraded performance when creating a custom price list from a quote.</span></span>
- <span data-ttu-id="c29ac-127">Клиенты замечают несоответствие **единиц измерения** по умолчанию на страницах **Сведения строки предложения с расценками** и **Сведения строки контракта**.</span><span class="sxs-lookup"><span data-stu-id="c29ac-127">Customers experience inconsistency with **unit** defaults on **Quote Line Details** and **Contract Line Details** pages.</span></span>
- <span data-ttu-id="c29ac-128">Добавление невключаемых в накладную категорий проводок во включаемую в накладную строку контракта не учитывает тип **Не оплачивается** для категории проводки.</span><span class="sxs-lookup"><span data-stu-id="c29ac-128">Adding non-chargeable transaction category items to a chargeable contract line will not respect the **Non-chargeable** billing type of the transaction category.</span></span>
- <span data-ttu-id="c29ac-129">Клиенты не могут использовать недавно добавленные роли и категории в ранее созданных контрактах.</span><span class="sxs-lookup"><span data-stu-id="c29ac-129">Customers can't use the newly added roles and category on previously created contracts.</span></span>
- <span data-ttu-id="c29ac-130">Клиенты замечают снижение производительности из-за избыточного извлечения в PreValidateProjectTeamMemberUpdate.cs</span><span class="sxs-lookup"><span data-stu-id="c29ac-130">Customers experience degraded performance Unnecessary retrieve in PreValidateProjectTeamMemberUpdate.cs</span></span>
- <span data-ttu-id="c29ac-131">Роли, установленные в качестве неоплачиваемых в списке **Категории ресурсов**, должны быть добавлены на вкладку **Оплачиваемые роли** как **Неоплачиваемые** в строке контракта по проекту.</span><span class="sxs-lookup"><span data-stu-id="c29ac-131">Roles set up as non-chargeable in the **Resource Categories** list should be added to the **Chargeable Roles** tab as **Non0chargeable** on the contract line for a project.</span></span>
- <span data-ttu-id="c29ac-132">Клиенты могут замечать снижение производительности при создании проекта, потому что **GetBookableResourceIdFromUser** извлекает все столбцы резервируемых ресурсов вместо только основного идентификатора.</span><span class="sxs-lookup"><span data-stu-id="c29ac-132">Customers may experience degraded performance when creating a project because **GetBookableResourceIdFromUser** retrieves all columns of bookable resources instead of just the primary ID.</span></span>
- <span data-ttu-id="c29ac-133">В сущности **TransactionType** отсутствует подключаемый модуль обновления предварительной проверки для предотвращения ввода пользователями недопустимых значений **Units** и **UnitGroups** для типов транзакций.</span><span class="sxs-lookup"><span data-stu-id="c29ac-133">**TransactionType** entity missing the pre-validation update plug-in to prevent users from entering **Units** and **UnitGroups** that are not valid for transaction types.</span></span>
- <span data-ttu-id="c29ac-134">Шаг **Удалить** не работает для импорта записи времени.</span><span class="sxs-lookup"><span data-stu-id="c29ac-134">The **Remove** step does not work for time entry import.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]