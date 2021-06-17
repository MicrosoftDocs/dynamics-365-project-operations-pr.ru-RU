---
title: Что нового или измененного в выпуске-обновлении 13 для Project Service Automation версии 3
description: В этом разделе приведены сведения о новых возможностях в выпуске-обновлении 13 для Project Service Automation версии 3.
author: ruhercul
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
ms.openlocfilehash: c328821064065e19938406856d327f690f577e7a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000317"
---
# <a name="project-service-automation-update-release-13-v3"></a><span data-ttu-id="6602b-103">Выпуск-обновление 13 Project Service Automation, версия 3</span><span class="sxs-lookup"><span data-stu-id="6602b-103">Project Service Automation Update Release 13, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="6602b-104">С удовольствием объявляем о выходе последнего обновления для приложения Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="6602b-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="6602b-105">Этот выпуск содержит некоторые важные усовершенствования, направленные на качество, производительность и удобство использования.</span><span class="sxs-lookup"><span data-stu-id="6602b-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="6602b-106">Этот выпуск совместим с Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="6602b-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="6602b-107">Чтобы обновить приложение до этого выпуска, посетите Центр администрирования Dynamics 365 Online и перейдите на страницу решений, чтобы установить обновление.</span><span class="sxs-lookup"><span data-stu-id="6602b-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="6602b-108">Дополнительные сведения см. в разделе [Установка, обновление или удаление предпочтительного решения](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="6602b-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="6602b-109">В этом разделе перечислены функции и исправления, появившиеся или изменившиеся в выпуске-обновлении 13 для Project Service Automation версии 3.</span><span class="sxs-lookup"><span data-stu-id="6602b-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 13.</span></span> <span data-ttu-id="6602b-110">Эта версия имеет номер сборки V3.10.3.18 и становится доступна по следующему графику:</span><span class="sxs-lookup"><span data-stu-id="6602b-110">This version has a build number of V3.10.3.18 and is available on the following schedule:</span></span>

- <span data-ttu-id="6602b-111">**Общая доступность (самостоятельное обновление):** ноябрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="6602b-111">**General availability (self-update):** November 2019</span></span>
- <span data-ttu-id="6602b-112">**Автообновление:** декабрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="6602b-112">**Auto-update:** December 2019</span></span>


## <a name="update-release-13"></a><span data-ttu-id="6602b-113">Выпуск-обновление 13</span><span class="sxs-lookup"><span data-stu-id="6602b-113">Update Release 13</span></span> 

### <a name="bug-fixes"></a><span data-ttu-id="6602b-114">Исправления ошибок</span><span class="sxs-lookup"><span data-stu-id="6602b-114">Bug fixes</span></span>

- <span data-ttu-id="6602b-115">Время и расходы</span><span class="sxs-lookup"><span data-stu-id="6602b-115">Time and Expense</span></span>

     - <span data-ttu-id="6602b-116">Исправлено: функция поиска на странице **Утверждение расходов** не работает при поиске по цели расхода.</span><span class="sxs-lookup"><span data-stu-id="6602b-116">Fixed: Search functionality on the **Expense approval** page does not work when searching by expense purpose.</span></span>

- <span data-ttu-id="6602b-117">Управление ресурсами</span><span class="sxs-lookup"><span data-stu-id="6602b-117">Resource Management</span></span>

     - <span data-ttu-id="6602b-118">Исправлено: числа в сверке теперь выравниваются по правому краю.</span><span class="sxs-lookup"><span data-stu-id="6602b-118">Fixed: Numbers in the reconciliation have been updated to be right justified.</span></span>
     - <span data-ttu-id="6602b-119">Исправлено: именованные ресурсы нельзя назначать задачам через вкладку **Расписание**.</span><span class="sxs-lookup"><span data-stu-id="6602b-119">Fixed: Named Resources can't be assigned to tasks through the **Schedule** tab.</span></span>

- <span data-ttu-id="6602b-120">Управление проектами</span><span class="sxs-lookup"><span data-stu-id="6602b-120">Project Management</span></span>

     - <span data-ttu-id="6602b-121">Исправлено: исключение "пустая ссылка" при назначении участника рабочей группы, когда **TransactionType** не содержит информации о настройке для **Unit** и **DefaultGroup**.</span><span class="sxs-lookup"><span data-stu-id="6602b-121">Fixed: Null reference exception when assigning team member when the **TransactionType** is missing setup information for **Unit** and **DefaultGroup**.</span></span>

- <span data-ttu-id="6602b-122">Sales</span><span class="sxs-lookup"><span data-stu-id="6602b-122">Sales</span></span>

     - <span data-ttu-id="6602b-123">Исправлено: дублирующиеся записи типа проводки возвращают ошибку при создании записей цен для ролей.</span><span class="sxs-lookup"><span data-stu-id="6602b-123">Fixed: Duplicate transaction type records return an error when role price records are created.</span></span>
     - <span data-ttu-id="6602b-124">Исправлено: дополнительные кнопки для **Создать возможную сделку**, **Предложение с расценками**, **Строка заказа** и **Добавить продукт** отображаются в командах для возможных сделок, предложений с расценками, продуктов по заказу и вложенной сетки строк на основе проекта.</span><span class="sxs-lookup"><span data-stu-id="6602b-124">Fixed: Extra buttons for **New Opportunity**, **Quote**, **Order Line**, and **Add Product** are visible in commands for Opportunities, Quotes, Order Products, and the project-based Lines subgrid.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]