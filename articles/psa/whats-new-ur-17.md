---
title: Что нового или измененного в выпуске-обновлении 17 для Project Service Automation версии 3
description: В этом разделе перечислены функции и исправления, доступные в выпуске-обновлении 17 для Project Service Automation версии 3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: 364a64e0ea501ac5b7faaf254c7af3648cfe1f9b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006707"
---
# <a name="project-service-automation-update-release-17-v3"></a><span data-ttu-id="991d1-103">Выпуск-обновление 17 Project Service Automation, версия 3</span><span class="sxs-lookup"><span data-stu-id="991d1-103">Project Service Automation Update Release 17, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="991d1-104">Мы рады объявить о последнем обновлении приложения Project Service Automation для Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="991d1-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="991d1-105">Этот выпуск содержит некоторые важные усовершенствования, направленные на качество, производительность и удобство использования.</span><span class="sxs-lookup"><span data-stu-id="991d1-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="991d1-106">Этот выпуск совместим с Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="991d1-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="991d1-107">Чтобы обновить приложение до этого выпуска, посетите Центр администрирования Dynamics 365 Online, страницу решений, чтобы установить обновление.</span><span class="sxs-lookup"><span data-stu-id="991d1-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="991d1-108">Дополнительные сведения см. в разделе [Установка, обновление или удаление предпочтительного решения](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="991d1-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="991d1-109">В этом разделе перечислены функции и исправления, появившиеся или изменившиеся в выпуске-обновлении 17 для PSA версии 3.</span><span class="sxs-lookup"><span data-stu-id="991d1-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 17.</span></span> <span data-ttu-id="991d1-110">Эта версия имеет номер сборки V3.10.6.34 и становится доступна широкому кругу клиентов посредством самостоятельного обновления в марте 2020 г.</span><span class="sxs-lookup"><span data-stu-id="991d1-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in March 2020.</span></span>


## <a name="update-release-17"></a><span data-ttu-id="991d1-111">Выпуск-обновление 17</span><span class="sxs-lookup"><span data-stu-id="991d1-111">Update Release 17</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="991d1-112">Исправления ошибок</span><span class="sxs-lookup"><span data-stu-id="991d1-112">Bug fixes</span></span>

<span data-ttu-id="991d1-113">**Общие сведения**</span><span class="sxs-lookup"><span data-stu-id="991d1-113">**General**</span></span>

- <span data-ttu-id="991d1-114">Исправлено: обновление приложения Project Service Automation для обеспечения соблюдения лицензий Team Member (Центр ресурсов проект будет включать метаданные плана обслуживания Team Member 3.x)</span><span class="sxs-lookup"><span data-stu-id="991d1-114">Fixed: Update Project Service Automation to enforce Team Member licenses (Project Resource Hub will include Team Member Service plan metadata 3.x)</span></span>
 
<span data-ttu-id="991d1-115">**Время и расходы**</span><span class="sxs-lookup"><span data-stu-id="991d1-115">**Time and Expense**</span></span>

- <span data-ttu-id="991d1-116">Исправлено: невозможно изменить оценку расходов с ненулевой цены на ноль (0).</span><span class="sxs-lookup"><span data-stu-id="991d1-116">Fixed: It is not possible to change an expense estimate from a non-zero price to zero (0).</span></span> <span data-ttu-id="991d1-117">Изменение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="991d1-117">The change is ignored.</span></span>

<span data-ttu-id="991d1-118">**Управление проектами**</span><span class="sxs-lookup"><span data-stu-id="991d1-118">**Project Management**</span></span>

- <span data-ttu-id="991d1-119">Исправлено: проверка на значения NULL была добавлена для названия должности участника рабочей группы.</span><span class="sxs-lookup"><span data-stu-id="991d1-119">Fixed: A check for null values has been added on a team member's position name.</span></span>
- <span data-ttu-id="991d1-120">Исправлено: поле **msdyn_userresourceid** в сущности **msdyn_resourceassignment** устарело.</span><span class="sxs-lookup"><span data-stu-id="991d1-120">Fixed: **msdyn_userresourceid** field on the **msdyn_resourceassignment** entity has been deprecated.</span></span>
- <span data-ttu-id="991d1-121">Исправлено: обновление с 2.x до 3.x теперь обрабатывает пустые контуры усилий в назначениях заданий.</span><span class="sxs-lookup"><span data-stu-id="991d1-121">Fixed: Upgrade from 2.x to 3.x now handles empty effort contours on task assignments.</span></span>

<span data-ttu-id="991d1-122">**Sales**</span><span class="sxs-lookup"><span data-stu-id="991d1-122">**Sales**</span></span>

- <span data-ttu-id="991d1-123">Исправлено: **Invoice.PreValidateInvoiceUpdate** теперь корректно обрабатывает сценарий переназначения владельцев записей.</span><span class="sxs-lookup"><span data-stu-id="991d1-123">Fixed: **Invoice.PreValidateInvoiceUpdate** now handles the scenario of reassigning record owners properly.</span></span>
- <span data-ttu-id="991d1-124">Исправлено: когда класс проводки **Время**, **UnitGroup** недоступна для редактирования для всех сущностей, включая **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail** и **ContractLineDetails**.</span><span class="sxs-lookup"><span data-stu-id="991d1-124">Fixed: When the transaction class is **Time**, **UnitGroup** is non-editable for all entities including, **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail**, and **ContractLineDetails**.</span></span> <span data-ttu-id="991d1-125">Однако поле **Единица измерения** недоступно для редактирования только для **JournalLine** и **InvoiceLineDetails**.</span><span class="sxs-lookup"><span data-stu-id="991d1-125">However, **Unit** is non-editable only for **JournalLine** and **InvoiceLineDetails**.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]