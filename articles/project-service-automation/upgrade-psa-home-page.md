---
title: Обновить домашнюю страницу
description: В этом разделе показан размещение важные сведения о новых возможностях и измененных в Dynamics 365 Project Service Automation, и о процессе обновления до новейшей версии.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 05/30/2019
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 for Project Service 3.x
author: rumant
ms.assetid: c92d0849-e40c-4a56-9719-34030fbf5991
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 55f544636f39fc4faae06fdd512f859800bb7b44
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754991"
---
# <a name="upgrade-home-page"></a><span data-ttu-id="bb2a9-103">Обновить домашнюю страницу</span><span class="sxs-lookup"><span data-stu-id="bb2a9-103">Upgrade home page</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a><span data-ttu-id="bb2a9-104">Обновление с версии PSA 2.x или 1.x до версии 3.x</span><span class="sxs-lookup"><span data-stu-id="bb2a9-104">Upgrade from PSA version 2.x or 1.x to version 3.x</span></span>

### <a name="new-instances"></a><span data-ttu-id="bb2a9-105">Новые экземпляры</span><span class="sxs-lookup"><span data-stu-id="bb2a9-105">New instances</span></span>

<span data-ttu-id="bb2a9-106">По состоянию на 17 мая 2019 года, когда Project Service Automation выбран во время подготовки нового экземпляра, по умолчанию устанавливается версия 3.x.</span><span class="sxs-lookup"><span data-stu-id="bb2a9-106">As of May 17, 2019, when Project Service Automation is selected during the provisioning of a new instance, version 3.x is installed by default.</span></span>

### <a name="existing-instances"></a><span data-ttu-id="bb2a9-107">Существующие экземпляры</span><span class="sxs-lookup"><span data-stu-id="bb2a9-107">Existing instances</span></span>

<span data-ttu-id="bb2a9-108">Ранее клиенты, имеющие экземпляр PSA версии 2.x и нуждающиеся в обновлении до версии 3.x, которая является версией PSA на основе единого интерфейса клиента (UCI), должны были обращаться в службу поддержки Microsoft и предоставлять подробную информацию о своем экземпляре, чтобы служба поддержки могла включить экземпляр для обновления до версии 3.x.</span><span class="sxs-lookup"><span data-stu-id="bb2a9-108">Previously, customers who have an instance of PSA version 2.x and needed to upgrade to version 3.x, which is the Unified client interface-based (UCI) version of PSA , had to contact Microsoft Support and provide the details of thier instance so that support could enable the instance for upgrade to version 3.x.</span></span> <span data-ttu-id="bb2a9-109">С 1 марта 2020 года клиенты, имеющие экземпляр PSA версии 2.x и нуждающиеся в обновлении до версии 3.x, смогут обновлять свои экземпляры непосредственно с портала администрирования, не обращаясь в службу поддержки Microsoft.</span><span class="sxs-lookup"><span data-stu-id="bb2a9-109">As of March 1st, 2020, customers who have an instance of PSA version 2.x and need to upgrade to version 3.x, will able to upgrade their instances directly from the Admin portal without having to contact Microsoft Support.</span></span>  

> [!NOTE]
> <span data-ttu-id="bb2a9-110">PSA версии 3.x включает в себя значительные изменения.</span><span class="sxs-lookup"><span data-stu-id="bb2a9-110">PSA version 3.x includes significant changes.</span></span> <span data-ttu-id="bb2a9-111">Она была построена в рамках единого интерфейса для обеспечения улучшенный интерфейс пользователя.</span><span class="sxs-lookup"><span data-stu-id="bb2a9-111">It has been built on the Unified Interface framework to help provide an improved user experience.</span></span> <span data-ttu-id="bb2a9-112">Модернизированное приложение обеспечивает согласованный единый пользовательский интерфейс, отвечающий принципам гибкого дизайна для оптимального просмотра на любом экране или устройстве.</span><span class="sxs-lookup"><span data-stu-id="bb2a9-112">The redesigned app delivers a consistent, uniform user interface (UI), and it follows responsive design principles for optimal viewing on any screen size or device.</span></span> <span data-ttu-id="bb2a9-113">В приложении произошли другие изменения.</span><span class="sxs-lookup"><span data-stu-id="bb2a9-113">There have been other changes throughout the application.</span></span> <span data-ttu-id="bb2a9-114">Некоторые из этих областей, которые были изменены, содержат цены, резервирование и назначение ресурсов, время, расходы и утверждения.</span><span class="sxs-lookup"><span data-stu-id="bb2a9-114">Some of the areas that have been changed include pricing, booking and assigning resources, time, expenses, and approvals.</span></span>

<span data-ttu-id="bb2a9-115">Перед началом процесса обновления рекомендуется выполнить следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="bb2a9-115">Before you begin the upgrade process, we recommend that you complete the following tasks:</span></span>

- <span data-ttu-id="bb2a9-116">Убедитесь, что на указанном экземпляре установлены как Dynamics 365 Field Service, так и Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="bb2a9-116">Verify whether both Dynamics 365 Field Service and Project Service Automation are installed on the identified instance.</span></span> <span data-ttu-id="bb2a9-117">Если оба решения установятся, необходимо запланировать обновление обоих, прежде чем возобновить регулярное использование экземпляра.</span><span class="sxs-lookup"><span data-stu-id="bb2a9-117">If both solutions are installed, you should plan to upgrade both before you resume regular use of the instance.</span></span>
- <span data-ttu-id="bb2a9-118">Внимательно просмотрите следующие разделы.</span><span class="sxs-lookup"><span data-stu-id="bb2a9-118">Carefully review the following topics.</span></span> <span data-ttu-id="bb2a9-119">Информированность и понимание изменений между версиями помогут вам в процессе обновления.</span><span class="sxs-lookup"><span data-stu-id="bb2a9-119">Awareness and understanding of the changes between versions will help you with the upgrade process.</span></span> <span data-ttu-id="bb2a9-120">Эти разделы содержат нужные сведения об основных изменениях в PSA, а также замечания и рекомендации по планированию обновления до версии 3.x.</span><span class="sxs-lookup"><span data-stu-id="bb2a9-120">These topics provide information about the major changes in PSA, together with considerations and recommendations for planning your upgrade to version 3.x.</span></span>

    - [<span data-ttu-id="bb2a9-121">Что нового или измененного в Project Service Automation версии 3</span><span class="sxs-lookup"><span data-stu-id="bb2a9-121">What's new or changed in Project Service Automation version 3</span></span>](whats-new-changed-v3.md)
    - [<span data-ttu-id="bb2a9-122">Моменты, которые следует учитывать при обновлении Project Service Automation версии 2.x или 1.x до версии 3</span><span class="sxs-lookup"><span data-stu-id="bb2a9-122">Upgrade considerations - Project Service Automation version 2.x or 1.x to version 3</span></span>](upgrade-v3.md)

- <span data-ttu-id="bb2a9-123">Обновите свой экземпляр в песочнице, чтобы оценить изменения в вашей реализации перед обновлением производственного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="bb2a9-123">Upgrade your sandbox instance to evaluate the changes in your implementation before you upgrade your production instance.</span></span>

<span data-ttu-id="bb2a9-124">После того, как вы ознакомились с разделами, которые были упомянуты ранее, и готовы обновиться до PSA версии 3.x или версии на основе UCI, отправьте запрос в службу поддержки Майкрософт, чтобы сделать обновление доступным в Центре администрирования.</span><span class="sxs-lookup"><span data-stu-id="bb2a9-124">After you've reviewed the topics that were mentioned earlier and are ready to upgrade to PSA version 3.x or the UCI-based version, submit a request to Microsoft support to make the upgrade available from Admin center.</span></span> <span data-ttu-id="bb2a9-125">В вашем запросе укажите детали вашего экземпляра.</span><span class="sxs-lookup"><span data-stu-id="bb2a9-125">In your request, provide the details of your instance.</span></span>

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a><span data-ttu-id="bb2a9-126">Более старых версии (PSA версии 2.x) во вновь созданном экземпляре</span><span class="sxs-lookup"><span data-stu-id="bb2a9-126">Older versions of PSA (PSA version 2.x) in a newly created instance</span></span>

<span data-ttu-id="bb2a9-127">По состоянию на 17-е мая 2019 года все новые экземпляры будут иметь UCI в качестве клиента по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bb2a9-127">As of May 17, 2019, all new instances will have UCI as the default client.</span></span> <span data-ttu-id="bb2a9-128">Для согласования с этим изменением, PSA версии 3.x и Field Service версии 8.x будут предоставлены по умолчанию, поскольку эти версии предназначены для работы с клиентом UCI.</span><span class="sxs-lookup"><span data-stu-id="bb2a9-128">For alignment with this change, PSA version 3.x and Field Service version 8.x will be provisioned by default, because these versions are designed to work with the UCI client.</span></span>

<span data-ttu-id="bb2a9-129">Начиная с 1 марта 2020 года клиенты Dynamics PSA больше не смогут создавать новые среды с более старыми версиями PSA, например PSA версии 2.x или ниже.</span><span class="sxs-lookup"><span data-stu-id="bb2a9-129">Starting March 1st 2020, customers of Dynamics PSA will no longer be able to create a new environments with older versions of PSA, for example PSA version 2.x or lower.</span></span> <span data-ttu-id="bb2a9-130">Любая новая среда будет иметь только версию 3.x PSA.</span><span class="sxs-lookup"><span data-stu-id="bb2a9-130">Any new environment will be to get only version 3.x of PSA.</span></span>

> [!NOTE]
> <span data-ttu-id="bb2a9-131">Для получения наилучших результатов при использовании более старых версий приложений Field Service и PSA перейдите на страницу **Параметры системы** и для поля **Использовать только единый интерфейс (рекомендуется)**, выберите **Нет** поскольку эти версии не предназначены для правильной загрузки в UCI.</span><span class="sxs-lookup"><span data-stu-id="bb2a9-131">For the best experience when you use older versions of the Field Service and PSA applications, go to the **System settings** page and for the field, **Use the new Unified Interface only (recommended)** field, select **No** as these versions aren't designed to be correctly loaded in UCI.</span></span> <span data-ttu-id="bb2a9-132">После отключения UCI можно открыть и запустить эти версии Field Service и PSA, используя старый веб-клиент.</span><span class="sxs-lookup"><span data-stu-id="bb2a9-132">After you have turned off UCI, you can open and run these versions of Field Service and PSA by using the old web client.</span></span> <span data-ttu-id="bb2a9-133">Для получения инструкций о том, как отключить клиента UCI, см. раздел [Включить только единый интерфейс](../admin/enable-unified-interface-only.md).</span><span class="sxs-lookup"><span data-stu-id="bb2a9-133">For instructions about how to turn off the UCI client, see [Enable unified interface only](../admin/enable-unified-interface-only.md).</span></span>