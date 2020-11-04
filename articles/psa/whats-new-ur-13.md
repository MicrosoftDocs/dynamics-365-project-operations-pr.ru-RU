---
title: Что нового или измененного в выпуске-обновлении 13 для Project Service Automation версии 3
description: В этом разделе приведены сведения о новых возможностях в выпуске-обновлении 13 для Project Service Automation версии 3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: 435b70255dd0053a496362c9ced9e742cfcca843
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083148"
---
# <a name="project-service-automation-update-release-13-v3"></a><span data-ttu-id="d4e68-103">Выпуск-обновление 13 Project Service Automation, версия 3</span><span class="sxs-lookup"><span data-stu-id="d4e68-103">Project Service Automation Update Release 13, V3</span></span>
<span data-ttu-id="d4e68-104">С удовольствием объявляем о выходе последнего обновления для приложения Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="d4e68-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="d4e68-105">Этот выпуск содержит некоторые важные усовершенствования, направленные на качество, производительность и удобство использования.</span><span class="sxs-lookup"><span data-stu-id="d4e68-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="d4e68-106">Этот выпуск совместим с Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="d4e68-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="d4e68-107">Чтобы обновить приложение до этого выпуска, посетите Центр администрирования Dynamics 365 Online и перейдите на страницу решений, чтобы установить обновление.</span><span class="sxs-lookup"><span data-stu-id="d4e68-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="d4e68-108">Дополнительные сведения см. в разделе [Установка, обновление или удаление предпочтительного решения](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="d4e68-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="d4e68-109">В этом разделе перечислены функции и исправления, появившиеся или изменившиеся в выпуске-обновлении 13 для Project Service Automation версии 3.</span><span class="sxs-lookup"><span data-stu-id="d4e68-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 13.</span></span> <span data-ttu-id="d4e68-110">Эта версия имеет номер сборки V3.10.3.18 и становится доступна по следующему графику:</span><span class="sxs-lookup"><span data-stu-id="d4e68-110">This version has a build number of V3.10.3.18 and is available on the following schedule:</span></span>

- <span data-ttu-id="d4e68-111">**Общая доступность (самостоятельное обновление):** ноябрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="d4e68-111">**General availability (self-update):** November 2019</span></span>
- <span data-ttu-id="d4e68-112">**Автообновление:** декабрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="d4e68-112">**Auto-update:** December 2019</span></span>


## <a name="update-release-13"></a><span data-ttu-id="d4e68-113">Выпуск-обновление 13</span><span class="sxs-lookup"><span data-stu-id="d4e68-113">Update Release 13</span></span> 

### <a name="bug-fixes"></a><span data-ttu-id="d4e68-114">Исправления ошибок</span><span class="sxs-lookup"><span data-stu-id="d4e68-114">Bug fixes</span></span>

- <span data-ttu-id="d4e68-115">Время и расходы</span><span class="sxs-lookup"><span data-stu-id="d4e68-115">Time and Expense</span></span>

     - <span data-ttu-id="d4e68-116">Исправлено: функция поиска на странице **Утверждение расходов** не работает при поиске по цели расхода.</span><span class="sxs-lookup"><span data-stu-id="d4e68-116">Fixed: Search functionality on the **Expense approval** page does not work when searching by expense purpose.</span></span>

- <span data-ttu-id="d4e68-117">Управление ресурсами</span><span class="sxs-lookup"><span data-stu-id="d4e68-117">Resource Management</span></span>

     - <span data-ttu-id="d4e68-118">Исправлено: числа в сверке теперь выравниваются по правому краю.</span><span class="sxs-lookup"><span data-stu-id="d4e68-118">Fixed: Numbers in the reconciliation have been updated to be right justified.</span></span>
     - <span data-ttu-id="d4e68-119">Исправлено: именованные ресурсы нельзя назначать задачам через вкладку **Расписание**.</span><span class="sxs-lookup"><span data-stu-id="d4e68-119">Fixed: Named Resources can't be assigned to tasks through the **Schedule** tab.</span></span>

- <span data-ttu-id="d4e68-120">Управление проектами</span><span class="sxs-lookup"><span data-stu-id="d4e68-120">Project Management</span></span>

     - <span data-ttu-id="d4e68-121">Исправлено: исключение "пустая ссылка" при назначении участника рабочей группы, когда **TransactionType** не содержит информации о настройке для **Unit** и **DefaultGroup**.</span><span class="sxs-lookup"><span data-stu-id="d4e68-121">Fixed: Null reference exception when assigning team member when the **TransactionType** is missing setup information for **Unit** and **DefaultGroup**.</span></span>

- <span data-ttu-id="d4e68-122">Sales</span><span class="sxs-lookup"><span data-stu-id="d4e68-122">Sales</span></span>

     - <span data-ttu-id="d4e68-123">Исправлено: дублирующиеся записи типа проводки возвращают ошибку при создании записей цен для ролей.</span><span class="sxs-lookup"><span data-stu-id="d4e68-123">Fixed: Duplicate transaction type records return an error when role price records are created.</span></span>
     - <span data-ttu-id="d4e68-124">Исправлено: дополнительные кнопки для пунктов **Новая возможная сделка** , **Предложение с расценками** , **Строка заказа** и **Добавить продукт** отображаются в командах для возможных сделок, предложений с расценками, продуктов для заказа, а также во вложенной сетке "Строки" для проекта.</span><span class="sxs-lookup"><span data-stu-id="d4e68-124">Fixed: Extra buttons for **New Opportunity** , **Quote** , **Order Line** , and **Add Product** are visible in commands for Opportunities, Quotes, Order Products, and the project-based Lines sub-grid.</span></span>


