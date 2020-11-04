---
title: Что нового или измененного в выпуске-обновлении 17.5, исправление, Project Service Automation, версия 3
description: В этом разделе перечислены функции и исправления, доступные в выпуске-обновлении 17.5 для Project Service Automation версии 3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 03/13/2020
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
ms.openlocfilehash: 359eb8f8ca41d69d4f30dd44497a4deb6a6c4f8d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083143"
---
# <a name="project-service-automation-update-release-175-v3"></a><span data-ttu-id="db628-103">Выпуск-обновление 17.5 Project Service Automation, версия 3</span><span class="sxs-lookup"><span data-stu-id="db628-103">Project Service Automation Update Release 17.5, V3</span></span>

<span data-ttu-id="db628-104">Мы рады объявить о последнем обновлении приложения Project Service Automation для Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="db628-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="db628-105">Этот выпуск содержит некоторые важные усовершенствования, направленные на качество, производительность и удобство использования.</span><span class="sxs-lookup"><span data-stu-id="db628-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="db628-106">Этот выпуск совместим с Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="db628-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="db628-107">Чтобы обновить приложение до этого выпуска, посетите Центр администрирования Dynamics 365 Online, страницу решений, чтобы установить обновление.</span><span class="sxs-lookup"><span data-stu-id="db628-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="db628-108">Дополнительные сведения см. в разделе [Установка, обновление или удаление предпочтительного решения](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="db628-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="db628-109">В этом разделе перечислены функции и исправления, появившиеся или изменившиеся в выпуске-обновлении 17.5 для версии 3.</span><span class="sxs-lookup"><span data-stu-id="db628-109">This topic lists the features and fixes that are new or changed for V3, Update Release 17.5.</span></span> <span data-ttu-id="db628-110">Эта версия имеет номер сборки V3.10.7.32 и становится доступна широкому кругу клиентов посредством самостоятельного обновления в марте 2020 г.</span><span class="sxs-lookup"><span data-stu-id="db628-110">This version has a build number of V3.10.7.32 and is generally available through a self-update in March 2020.</span></span>


## <a name="update-release-175"></a><span data-ttu-id="db628-111">Выпуск-обновление 17.5</span><span class="sxs-lookup"><span data-stu-id="db628-111">Update Release 17.5</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="db628-112">Исправления ошибок</span><span class="sxs-lookup"><span data-stu-id="db628-112">Bug fixes</span></span>


<span data-ttu-id="db628-113">**Управление проектами**</span><span class="sxs-lookup"><span data-stu-id="db628-113">**Project Management**</span></span>

- <span data-ttu-id="db628-114">Исправлено: устранены проблемы синхронизации на стороне сервера, возникающие при выполнении длительных задач.</span><span class="sxs-lookup"><span data-stu-id="db628-114">Fixed: Addressed server-side synchronization issues that occur with long duration tasks.</span></span>
- <span data-ttu-id="db628-115">Исправлено: устранена ошибка, из-за которой шаблоны 24-часового рабочего времени неправильно добавляли дополнительный день к задачам.</span><span class="sxs-lookup"><span data-stu-id="db628-115">Fixed: Addressed 24-hour work hour templates inaccurately adding an additional day to tasks.</span></span>
- <span data-ttu-id="db628-116">Исправлено: устранена ошибка, из-за которой шаблоны рабочего времени в часовом поясе +13 часов по Гринвичу некорректно переносили задачи на один день вперед.</span><span class="sxs-lookup"><span data-stu-id="db628-116">Fixed: Addressed +13 GMT work hour templates inaccurately shifting tasks one day ahead.</span></span>

