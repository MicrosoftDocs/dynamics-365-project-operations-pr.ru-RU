---
title: Что нового и что изменилось в выпуске-обновлении 13 для Project Service Automation версии 3
description: В этом разделе приведены сведения о новых возможностях в выпуске-обновлении 13 для Project Service Automation версии 3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: c6f6a5b6-b5bb-467c-b7c7-7fb962504c6d
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5f1b6b3879c94a77ab62082aad1e470a3ba66552
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754955"
---
# <a name="project-service-automation-v3-update-release-13"></a><span data-ttu-id="3b39b-103">Project Service Automation версии 3, выпуск-обновление 13</span><span class="sxs-lookup"><span data-stu-id="3b39b-103">Project Service Automation V3, Update Release 13</span></span>
<span data-ttu-id="3b39b-104">С удовольствием объявляем о выходе последнего обновления для приложения Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="3b39b-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="3b39b-105">Этот выпуск содержит некоторые важные усовершенствования, направленные на качество, производительность и удобство использования.</span><span class="sxs-lookup"><span data-stu-id="3b39b-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="3b39b-106">Этот выпуск совместим с Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="3b39b-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="3b39b-107">Чтобы обновить приложение до этого выпуска, посетите Центр администрирования Dynamics 365 Online и перейдите на страницу решений, чтобы установить обновление.</span><span class="sxs-lookup"><span data-stu-id="3b39b-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="3b39b-108">Дополнительные сведения см. в разделе [Установка, обновление или удаление предпочтительного решения](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="3b39b-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="3b39b-109">В этом разделе перечислены функции и исправления, появившиеся или изменившиеся в выпуске-обновлении 13 для Project Service Automation версии 3.</span><span class="sxs-lookup"><span data-stu-id="3b39b-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 13.</span></span> <span data-ttu-id="3b39b-110">Эта версия имеет номер сборки V3.10.3.18 и становится доступна по следующему графику:</span><span class="sxs-lookup"><span data-stu-id="3b39b-110">This version has a build number of V3.10.3.18 and is available on the following schedule:</span></span>

- <span data-ttu-id="3b39b-111">**Общая доступность (самостоятельное обновление):** ноябрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="3b39b-111">**General availability (self-update):** November 2019</span></span>
- <span data-ttu-id="3b39b-112">**Автообновление:** декабрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="3b39b-112">**Auto-update:** December 2019</span></span>


## <a name="update-release-13"></a><span data-ttu-id="3b39b-113">Выпуск-обновление 13</span><span class="sxs-lookup"><span data-stu-id="3b39b-113">Update Release 13</span></span> 

### <a name="bug-fixes"></a><span data-ttu-id="3b39b-114">Исправления ошибок</span><span class="sxs-lookup"><span data-stu-id="3b39b-114">Bug fixes</span></span>

- <span data-ttu-id="3b39b-115">Время и расходы</span><span class="sxs-lookup"><span data-stu-id="3b39b-115">Time and Expense</span></span>

     - <span data-ttu-id="3b39b-116">Исправлено: функция поиска на странице **Утверждение расходов** не работает при поиске по цели расхода.</span><span class="sxs-lookup"><span data-stu-id="3b39b-116">Fixed: Search functionality on the **Expense approval** page does not work when searching by expense purpose.</span></span>

- <span data-ttu-id="3b39b-117">Управление ресурсами</span><span class="sxs-lookup"><span data-stu-id="3b39b-117">Resource Management</span></span>

     - <span data-ttu-id="3b39b-118">Исправлено: числа в сверке теперь выравниваются по правому краю.</span><span class="sxs-lookup"><span data-stu-id="3b39b-118">Fixed: Numbers in the reconciliation have been updated to be right justified.</span></span>
     - <span data-ttu-id="3b39b-119">Исправлено: именованные ресурсы нельзя назначать задачам через вкладку **Расписание**.</span><span class="sxs-lookup"><span data-stu-id="3b39b-119">Fixed: Named Resources can't be assigned to tasks through the **Schedule** tab.</span></span>

- <span data-ttu-id="3b39b-120">Управление проектами</span><span class="sxs-lookup"><span data-stu-id="3b39b-120">Project Management</span></span>

     - <span data-ttu-id="3b39b-121">Исправлено: исключение "пустая ссылка" при назначении участника рабочей группы, когда **TransactionType** не содержит информации о настройке для **Unit** и **DefaultGroup**.</span><span class="sxs-lookup"><span data-stu-id="3b39b-121">Fixed: Null reference exception when assigning team member when the **TransactionType** is missing setup information for **Unit** and **DefaultGroup**.</span></span>

- <span data-ttu-id="3b39b-122">Sales</span><span class="sxs-lookup"><span data-stu-id="3b39b-122">Sales</span></span>

     - <span data-ttu-id="3b39b-123">Исправлено: дублирующиеся записи типа проводки возвращают ошибку при создании записей цен для ролей.</span><span class="sxs-lookup"><span data-stu-id="3b39b-123">Fixed: Duplicate transaction type records return an error when role price records are created.</span></span>
     - <span data-ttu-id="3b39b-124">Исправлено: дополнительные кнопки для пунктов **Новая возможная сделка**, **Предложение с расценками**, **Строка заказа** и **Добавить продукт** отображаются в командах для возможных сделок, предложений с расценками, продуктов для заказа, а также во вложенной сетке "Строки" для проекта.</span><span class="sxs-lookup"><span data-stu-id="3b39b-124">Fixed: Extra buttons for **New Opportunity**, **Quote**, **Order Line**, and **Add Product** are visible in commands for Opportunities, Quotes, Order Products, and the project-based Lines sub-grid.</span></span>


