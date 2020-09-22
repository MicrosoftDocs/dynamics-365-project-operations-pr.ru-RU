---
title: Настройка Project Service Automation
description: Шаги по настройке Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 56ba0b8d-808c-48d6-965f-abd74b49c2b4
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 52be4705e6ef983dcf421df5d1bfb5c6de8e9a30
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754939"
---
# <a name="configure-project-service"></a><span data-ttu-id="f12f8-103">Настройка Project Service</span><span class="sxs-lookup"><span data-stu-id="f12f8-103">Configure Project Service</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="f12f8-104">Прежде чем вы сможете использовать возможности автоматизации [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] в [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] для управления своими учетными записями организаций, проектами и ресурсами, вам необходимо выполнить ряд настроек, чтобы обеспечить соответствие решения [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] потребностям вашей организации.</span><span class="sxs-lookup"><span data-stu-id="f12f8-104">Before you can use the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automation capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to manage your accounts, projects, and resources, you need to complete a few configuration steps to ensure the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] solution matches your organization’s needs.</span></span> <span data-ttu-id="f12f8-105">Эти настройки включают:</span><span class="sxs-lookup"><span data-stu-id="f12f8-105">These steps include:</span></span>  
  
-   <span data-ttu-id="f12f8-106">[Настройка единиц времени](../project-service/set-up-time-units.md).</span><span class="sxs-lookup"><span data-stu-id="f12f8-106">[Set up time units](../project-service/set-up-time-units.md).</span></span> <span data-ttu-id="f12f8-107">Настройка единиц времени в каталоге продукции, которые будут использоваться в качестве базиса для планирования и выставления счетов по вашим проектам.</span><span class="sxs-lookup"><span data-stu-id="f12f8-107">Configure the time units in the product catalog that you’ll use as a base for scheduling and billing your projects.</span></span>  
  
-   <span data-ttu-id="f12f8-108">[Настройка валют и курса обмена](../project-service/set-up-currencies-exchange-rates.md).</span><span class="sxs-lookup"><span data-stu-id="f12f8-108">[Set up currencies and exchange rates](../project-service/set-up-currencies-exchange-rates.md).</span></span> <span data-ttu-id="f12f8-109">Настройка валют для проектов.</span><span class="sxs-lookup"><span data-stu-id="f12f8-109">Set up the currencies to use for your projects.</span></span>  
  
-   <span data-ttu-id="f12f8-110">[Создание организационных единиц](../project-service/create-organizational-units.md).</span><span class="sxs-lookup"><span data-stu-id="f12f8-110">[Create organizational units](../project-service/create-organizational-units.md).</span></span> <span data-ttu-id="f12f8-111">Настройка групп, которые ваша компания использует для деления своего бизнеса, например по регионам, бизнес-функциям или другим признакам.</span><span class="sxs-lookup"><span data-stu-id="f12f8-111">Set up the groups that your company uses to divide its business, whether by geography, business function, or other logical division.</span></span>  
  
-   <span data-ttu-id="f12f8-112">[Настройка периодичности выставления счетов](../project-service/set-up-invoice-frequencies.md).</span><span class="sxs-lookup"><span data-stu-id="f12f8-112">[Set up invoice frequencies](../project-service/set-up-invoice-frequencies.md).</span></span> <span data-ttu-id="f12f8-113">Настройка периодов времени, которые будут использоваться для выставления счетов клиентам.</span><span class="sxs-lookup"><span data-stu-id="f12f8-113">Set up time periods that you want to use for billing your clients.</span></span>  
  
-   <span data-ttu-id="f12f8-114">[Настройка категорий проводок](../project-service/configure-transaction-categories.md).</span><span class="sxs-lookup"><span data-stu-id="f12f8-114">[Configure transaction categories](../project-service/configure-transaction-categories.md).</span></span> <span data-ttu-id="f12f8-115">Настройка категорий проводок, по которым ваши консультанты смогут получать компенсацию за свои оплачиваемые и неоплачиваемое расходы.</span><span class="sxs-lookup"><span data-stu-id="f12f8-115">Set up transaction categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="f12f8-116">[Настройка категорий расходов](../project-service/configure-expense-categories.md).</span><span class="sxs-lookup"><span data-stu-id="f12f8-116">[Configure expense categories](../project-service/configure-expense-categories.md).</span></span> <span data-ttu-id="f12f8-117">Настройка категорий, по которым ваши консультанты смогут получать компенсацию за свои оплачиваемые и неоплачиваемое расходы.</span><span class="sxs-lookup"><span data-stu-id="f12f8-117">Set up the categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="f12f8-118">[Создание позиций каталога продукции](../project-service/create-product-catalog-items.md).</span><span class="sxs-lookup"><span data-stu-id="f12f8-118">[Create product catalog items](../project-service/create-product-catalog-items.md).</span></span> <span data-ttu-id="f12f8-119">Добавление продаваемых продуктов, например лицензий на программное обеспечение, в каталог продукции.</span><span class="sxs-lookup"><span data-stu-id="f12f8-119">Add the products you sell, such as software licenses, to the product catalog.</span></span>  
  
-   <span data-ttu-id="f12f8-120">[Создание прайс-листа](../project-service/create-price-list.md).</span><span class="sxs-lookup"><span data-stu-id="f12f8-120">[Create a price list](../project-service/create-price-list.md).</span></span> <span data-ttu-id="f12f8-121">Настройка различных прайс-листов в зависимости от того, какие суммы вы желаете выставлять своим клиентам за каждую роль, которая требуется для их проекта.</span><span class="sxs-lookup"><span data-stu-id="f12f8-121">Configure different price lists, depending on how much you want to charge your clients for each role their project requires.</span></span>  
  
-   <span data-ttu-id="f12f8-122">[Настройка ресурсов](../project-service/set-up-resources.md).</span><span class="sxs-lookup"><span data-stu-id="f12f8-122">[Set up resources](../project-service/set-up-resources.md).</span></span> <span data-ttu-id="f12f8-123">Добавление навыков, квалификаций, ролей ресурсов и других сведений о ресурсах, которые потребуются для ваших проектов.</span><span class="sxs-lookup"><span data-stu-id="f12f8-123">Add the skills, proficiencies, resource roles, and other resource information that you’ll need for your projects.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="f12f8-124">См. также</span><span class="sxs-lookup"><span data-stu-id="f12f8-124">See Also</span></span>  
 <span data-ttu-id="f12f8-125">[Обзор Project Service Automation](../project-service/overview.md) </span><span class="sxs-lookup"><span data-stu-id="f12f8-125">[Overview of Project Service Automation](../project-service/overview.md) </span></span>  
 <span data-ttu-id="f12f8-126">[Настройка Project Service Automation](../project-service/configure.md) </span><span class="sxs-lookup"><span data-stu-id="f12f8-126">[Configure Project Service Automation](../project-service/configure.md) </span></span>  
 <span data-ttu-id="f12f8-127">[Руководство для менеджера по работе с клиентами](../project-service/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="f12f8-127">[Account Manager Guide](../project-service/account-manager-guide.md) </span></span>  
 <span data-ttu-id="f12f8-128">[Руководство менеджера по проектам](../project-service/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="f12f8-128">[Project Manager Guide](../project-service/project-manager-guide.md) </span></span>  
 <span data-ttu-id="f12f8-129">[Руководство менеджера по ресурсам](../project-service/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="f12f8-129">[Resource Manager Guide](../project-service/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="f12f8-130">Руководство по совместной работе и вводу данных о времени и расходах</span><span class="sxs-lookup"><span data-stu-id="f12f8-130">Time, Expense, and Collaboration Guid</span></span>](../project-service/time-expense-collaboration-guide.md)
