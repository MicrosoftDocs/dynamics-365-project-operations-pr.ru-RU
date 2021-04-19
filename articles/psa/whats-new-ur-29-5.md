---
title: Что нового или измененного в выпуске-обновлении 29.5, исправление, Project Service Automation, исправление версии 3
description: В этом разделе перечислены функции и исправления, доступные в выпуске-обновлении 29.5 для Project Service Automation исправление версии 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 03/26/2021
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
ms.openlocfilehash: 99ba353236ad88b8bdff2c1b25e1247fa4bf3455
ms.sourcegitcommit: 9ebf7dd501898053bfa824f732adabf3f273613b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/26/2021
ms.locfileid: "5715701"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-295-v3"></a><span data-ttu-id="93e7e-103">Что нового или измененного в выпуске-обновлении 29.5 для Project Service Automation версии 3</span><span class="sxs-lookup"><span data-stu-id="93e7e-103">What's new or changed in Project Service Automation Update Release 29.5, V3</span></span>

<span data-ttu-id="93e7e-104">Мы рады объявить о последнем обновлении приложения Project Service Automation для Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="93e7e-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="93e7e-105">Этот выпуск содержит некоторые важные усовершенствования, направленные на качество, производительность и удобство использования.</span><span class="sxs-lookup"><span data-stu-id="93e7e-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="93e7e-106">Этот выпуск совместим с Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="93e7e-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="93e7e-107">Чтобы обновить приложение до этого выпуска, посетите страницу решений Центра администрирования Dynamics 365 Online и установите обновление.</span><span class="sxs-lookup"><span data-stu-id="93e7e-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="93e7e-108">Дополнительные сведения см. в разделе [Установка, обновление или удаление предпочтительного решения](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="93e7e-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="93e7e-109">В этом разделе перечислены функции и исправления, появившиеся или изменившиеся в выпуске-обновлении 29.5 для Project Service Automation версии 3.</span><span class="sxs-lookup"><span data-stu-id="93e7e-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 29.5.</span></span> <span data-ttu-id="93e7e-110">Эта версия имеет номер сборки V3.10.47.150 и становится доступна широкому кругу клиентов посредством самостоятельного обновления в январе 2021 г.</span><span class="sxs-lookup"><span data-stu-id="93e7e-110">This version has a build number of V3.10.47.150 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-295"></a><span data-ttu-id="93e7e-111">Выпуск-обновление 29.5</span><span class="sxs-lookup"><span data-stu-id="93e7e-111">Update Release 29.5</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="93e7e-112">Исправленные ошибки</span><span class="sxs-lookup"><span data-stu-id="93e7e-112">Bug fixes</span></span>


<span data-ttu-id="93e7e-113">**Продажи**</span><span class="sxs-lookup"><span data-stu-id="93e7e-113">**Sales**</span></span>

<span data-ttu-id="93e7e-114">Следующие проблемы были исправлены:</span><span class="sxs-lookup"><span data-stu-id="93e7e-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="93e7e-115">Возможное исключение с нулевой ссылкой происходит в **ContractLineMapHelper.UpdateContractLineDetailPriceListReference**, когда вы закрываете предложение с расценками как выигранное и у предложения с расценками нет прайс-листа.</span><span class="sxs-lookup"><span data-stu-id="93e7e-115">A possible null reference exception occurs in **ContractLineMapHelper.UpdateContractLineDetailPriceListReference** when you close a quote as won and the quote has no price list.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
