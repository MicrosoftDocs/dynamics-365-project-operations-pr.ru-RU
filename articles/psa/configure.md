---
title: Настройка Project Service Automation
description: Шаги по настройке Project Service
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: ef1724bb92e62ae21472e133fff0978c4faeeffa
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002863"
---
# <a name="configure-project-service"></a><span data-ttu-id="cd844-103">Настройка Project Service</span><span class="sxs-lookup"><span data-stu-id="cd844-103">Configure Project Service</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="cd844-104">Прежде чем вы сможете использовать возможности автоматизации [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] в [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] для управления своими учетными записями организаций, проектами и ресурсами, вам необходимо выполнить ряд настроек, чтобы обеспечить соответствие решения [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] потребностям вашей организации.</span><span class="sxs-lookup"><span data-stu-id="cd844-104">Before you can use the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automation capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to manage your accounts, projects, and resources, you need to complete a few configuration steps to ensure the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] solution matches your organization’s needs.</span></span> <span data-ttu-id="cd844-105">Эти настройки включают:</span><span class="sxs-lookup"><span data-stu-id="cd844-105">These steps include:</span></span>  
  
-   <span data-ttu-id="cd844-106">[Настройка единиц времени](../psa/set-up-time-units.md).</span><span class="sxs-lookup"><span data-stu-id="cd844-106">[Set up time units](../psa/set-up-time-units.md).</span></span> <span data-ttu-id="cd844-107">Настройка единиц времени в каталоге продукции, которые будут использоваться в качестве базиса для планирования и выставления счетов по вашим проектам.</span><span class="sxs-lookup"><span data-stu-id="cd844-107">Configure the time units in the product catalog that you’ll use as a base for scheduling and billing your projects.</span></span>  
  
-   <span data-ttu-id="cd844-108">[Настройка валют и курса обмена](../psa/set-up-currencies-exchange-rates.md).</span><span class="sxs-lookup"><span data-stu-id="cd844-108">[Set up currencies and exchange rates](../psa/set-up-currencies-exchange-rates.md).</span></span> <span data-ttu-id="cd844-109">Настройка валют для проектов.</span><span class="sxs-lookup"><span data-stu-id="cd844-109">Set up the currencies to use for your projects.</span></span>  
  
-   <span data-ttu-id="cd844-110">[Создание организационных единиц](../psa/create-organizational-units.md).</span><span class="sxs-lookup"><span data-stu-id="cd844-110">[Create organizational units](../psa/create-organizational-units.md).</span></span> <span data-ttu-id="cd844-111">Настройка групп, которые ваша компания использует для деления своего бизнеса, например по регионам, бизнес-функциям или другим признакам.</span><span class="sxs-lookup"><span data-stu-id="cd844-111">Set up the groups that your company uses to divide its business, whether by geography, business function, or other logical division.</span></span>  
  
-   <span data-ttu-id="cd844-112">[Настройка периодичности выставления счетов](../psa/set-up-invoice-frequencies.md).</span><span class="sxs-lookup"><span data-stu-id="cd844-112">[Set up invoice frequencies](../psa/set-up-invoice-frequencies.md).</span></span> <span data-ttu-id="cd844-113">Настройка периодов времени, которые будут использоваться для выставления счетов клиентам.</span><span class="sxs-lookup"><span data-stu-id="cd844-113">Set up time periods that you want to use for billing your clients.</span></span>  
  
-   <span data-ttu-id="cd844-114">[Настройка категорий проводок](../psa/configure-transaction-categories.md).</span><span class="sxs-lookup"><span data-stu-id="cd844-114">[Configure transaction categories](../psa/configure-transaction-categories.md).</span></span> <span data-ttu-id="cd844-115">Настройка категорий проводок, по которым ваши консультанты смогут получать компенсацию за свои оплачиваемые и неоплачиваемое расходы.</span><span class="sxs-lookup"><span data-stu-id="cd844-115">Set up transaction categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="cd844-116">[Настройка категорий расходов](../psa/configure-expense-categories.md).</span><span class="sxs-lookup"><span data-stu-id="cd844-116">[Configure expense categories](../psa/configure-expense-categories.md).</span></span> <span data-ttu-id="cd844-117">Настройка категорий, по которым ваши консультанты смогут получать компенсацию за свои оплачиваемые и неоплачиваемое расходы.</span><span class="sxs-lookup"><span data-stu-id="cd844-117">Set up the categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="cd844-118">[Создание позиций каталога продукции](../psa/create-product-catalog-items.md).</span><span class="sxs-lookup"><span data-stu-id="cd844-118">[Create product catalog items](../psa/create-product-catalog-items.md).</span></span> <span data-ttu-id="cd844-119">Добавление продаваемых продуктов, например лицензий на программное обеспечение, в каталог продукции.</span><span class="sxs-lookup"><span data-stu-id="cd844-119">Add the products you sell, such as software licenses, to the product catalog.</span></span>  
  
-   <span data-ttu-id="cd844-120">[Создание прайс-листа](../psa/create-price-list.md).</span><span class="sxs-lookup"><span data-stu-id="cd844-120">[Create a price list](../psa/create-price-list.md).</span></span> <span data-ttu-id="cd844-121">Настройка различных прайс-листов в зависимости от того, какие суммы вы желаете выставлять своим клиентам за каждую роль, которая требуется для их проекта.</span><span class="sxs-lookup"><span data-stu-id="cd844-121">Configure different price lists, depending on how much you want to charge your clients for each role their project requires.</span></span>  
  
-   <span data-ttu-id="cd844-122">[Настройка ресурсов](../psa/set-up-resources.md).</span><span class="sxs-lookup"><span data-stu-id="cd844-122">[Set up resources](../psa/set-up-resources.md).</span></span> <span data-ttu-id="cd844-123">Добавление навыков, квалификаций, ролей ресурсов и других сведений о ресурсах, которые потребуются для ваших проектов.</span><span class="sxs-lookup"><span data-stu-id="cd844-123">Add the skills, proficiencies, resource roles, and other resource information that you’ll need for your projects.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="cd844-124">См. также</span><span class="sxs-lookup"><span data-stu-id="cd844-124">See Also</span></span>  
 <span data-ttu-id="cd844-125">[Обзор Project Service Automation](../psa/overview.md) </span><span class="sxs-lookup"><span data-stu-id="cd844-125">[Overview of Project Service Automation](../psa/overview.md) </span></span>  
 <span data-ttu-id="cd844-126">[Настройка Project Service Automation](../psa/configure.md) </span><span class="sxs-lookup"><span data-stu-id="cd844-126">[Configure Project Service Automation](../psa/configure.md) </span></span>  
 <span data-ttu-id="cd844-127">[Руководство для менеджера по работе с клиентами](../psa/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="cd844-127">[Account Manager Guide](../psa/account-manager-guide.md) </span></span>  
 <span data-ttu-id="cd844-128">[Руководство менеджера по проектам](../psa/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="cd844-128">[Project Manager Guide](../psa/project-manager-guide.md) </span></span>  
 <span data-ttu-id="cd844-129">[Руководство менеджера по ресурсам](../psa/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="cd844-129">[Resource Manager Guide](../psa/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="cd844-130">Руководство по совместной работе и вводу данных о времени и расходах</span><span class="sxs-lookup"><span data-stu-id="cd844-130">Time, Expense, and Collaboration Guid</span></span>](../psa/time-expense-collaboration-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]