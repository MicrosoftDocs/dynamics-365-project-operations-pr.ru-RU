---
title: Что нового или измененного в выпуске-обновлении 14 для Project Service Automation версии 3
description: В этом разделе приведены сведения о новых возможностях в выпуске-обновлении 14 для Project Service Automation версии 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
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
ms.openlocfilehash: e19c8ffe7d92ab7ec9eb46aff8f944c62b0bb4bc
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280999"
---
# <a name="project-service-automation-update-release-14-v3"></a><span data-ttu-id="4b574-103">Выпуск-обновление 14 Project Service Automation, версия 3</span><span class="sxs-lookup"><span data-stu-id="4b574-103">Project Service Automation Update Release 14, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="4b574-104">С удовольствием объявляем о выходе последнего обновления для приложения Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="4b574-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="4b574-105">Этот выпуск содержит некоторые важные усовершенствования, направленные на качество, производительность и удобство использования.</span><span class="sxs-lookup"><span data-stu-id="4b574-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="4b574-106">Этот выпуск совместим с Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="4b574-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="4b574-107">Чтобы обновить приложение до этого выпуска, посетите Центр администрирования Dynamics 365 Online и перейдите на страницу решений, чтобы установить обновление.</span><span class="sxs-lookup"><span data-stu-id="4b574-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="4b574-108">Дополнительные сведения см. в разделе [Установка, обновление или удаление предпочтительного решения](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="4b574-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="4b574-109">В этом разделе перечислены функции и исправления, появившиеся или изменившиеся в выпуске-обновлении 14 для PSA версии 3.</span><span class="sxs-lookup"><span data-stu-id="4b574-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 14.</span></span> <span data-ttu-id="4b574-110">Эта версия имеет номер сборки V3.10.4.21 и становится доступна по следующему графику:</span><span class="sxs-lookup"><span data-stu-id="4b574-110">This version has a build number of V3.10.4.21 and is available on the following schedule:</span></span>

- <span data-ttu-id="4b574-111">**Общая доступность (самостоятельное обновление):** январь 2020 г.</span><span class="sxs-lookup"><span data-stu-id="4b574-111">**General availability (self-update):** January 2020</span></span>
- <span data-ttu-id="4b574-112">**Автообновление:** февраль 2020 г.</span><span class="sxs-lookup"><span data-stu-id="4b574-112">**Auto-update:** February 2020</span></span>

## <a name="update-release-14"></a><span data-ttu-id="4b574-113">Выпуск-обновление 14</span><span class="sxs-lookup"><span data-stu-id="4b574-113">Update Release 14</span></span>

### <a name="enhancements"></a><span data-ttu-id="4b574-114">Усовершенствования</span><span class="sxs-lookup"><span data-stu-id="4b574-114">Enhancements</span></span>

- <span data-ttu-id="4b574-115">Sales</span><span class="sxs-lookup"><span data-stu-id="4b574-115">Sales</span></span>

     - <span data-ttu-id="4b574-116">Пользовательские значения полей из формы **Сведения строки предложения с расценками** копируются в форму **Сведения строки контракта проекта**, когда предложение с расценками переходит в состояние **Закрыто и реализовано**.</span><span class="sxs-lookup"><span data-stu-id="4b574-116">Custom field values from **Quote Line Details** are copied to **Project Contract Line Details** when a quote is updated to **Closed as won**.</span></span>
     - <span data-ttu-id="4b574-117">Подтвержденные проекты можно переводить в состояние **Закрыто и нереализовано**.</span><span class="sxs-lookup"><span data-stu-id="4b574-117">Confirmed projects can be **Closed as lost**.</span></span>

- <span data-ttu-id="4b574-118">Управление ресурсами</span><span class="sxs-lookup"><span data-stu-id="4b574-118">Resource Management</span></span>

     - <span data-ttu-id="4b574-119">При продлении резервирований пользователи видят диалоговое окно подтверждения для подведения итогов резервирования и предоставления ссылки на страницу "Ведение резервирований".</span><span class="sxs-lookup"><span data-stu-id="4b574-119">When extending bookings, users will be prompted with a confirmation dialog box to summarize booking results and provide a link to Maintain Bookings.</span></span>


### <a name="bug-fixes"></a><span data-ttu-id="4b574-120">Исправления ошибок</span><span class="sxs-lookup"><span data-stu-id="4b574-120">Bug fixes</span></span>

- <span data-ttu-id="4b574-121">Время и расходы</span><span class="sxs-lookup"><span data-stu-id="4b574-121">Time and Expense</span></span>

     - <span data-ttu-id="4b574-122">Исправлено: улучшено взаимодействие с пользователем, когда пользователь не выбрал ни одной записи для исправления.</span><span class="sxs-lookup"><span data-stu-id="4b574-122">Fixed: Improved the user experience when the user has not selected any entries to be corrected.</span></span>

- <span data-ttu-id="4b574-123">Управление ресурсами</span><span class="sxs-lookup"><span data-stu-id="4b574-123">Resource Management</span></span>

     - <span data-ttu-id="4b574-124">Исправлено: при многократном резервировании ресурса происходит переполнение имени резервируемого ресурса.</span><span class="sxs-lookup"><span data-stu-id="4b574-124">Fixed: Booking a resource multiple times overflows the name of the bookable resource.</span></span>

- <span data-ttu-id="4b574-125">Sales</span><span class="sxs-lookup"><span data-stu-id="4b574-125">Sales</span></span>

     - <span data-ttu-id="4b574-126">Исправлено: общая цена продажи не рассчитывается до тех пор, пока пользователь не введет себестоимость для оценки расходов по проекту.</span><span class="sxs-lookup"><span data-stu-id="4b574-126">Fixed: The total sales price is not calculated until the user also inputs a cost price for expense estimates on a project.</span></span>
     - <span data-ttu-id="4b574-127">Исправлено: закрыть предложение с расценками как **Реализованное**, нельзя, если контракт по проекту не находится в состоянии **Черновик**.</span><span class="sxs-lookup"><span data-stu-id="4b574-127">Fixed: Closing a quote as **Won** fails if the associated project contract is not in a **Draft** state.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]