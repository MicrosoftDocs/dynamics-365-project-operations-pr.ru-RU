---
title: Регистрация на подписку на предварительную версию — облегченное развертывание
description: Эта тема предоставляет информацию о том, как подписаться на развертывание и развернуть развертывание Project Operations Lite — от сделки до счетов-проформ.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2b5a65f5e29915c349d40400ebbf3e4923b36a67
ms.sourcegitcommit: 52b26950bb3b1596ad81aa4ff91745ee9615d1b0
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334798"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a><span data-ttu-id="275ed-103">Регистрация на подписку на предварительную версию — облегченное развертывание</span><span class="sxs-lookup"><span data-stu-id="275ed-103">Sign up for a preview subscription - lite</span></span> 

<span data-ttu-id="275ed-104">В этой теме описано, как подписаться на пробное предложение и как развернуть сделку Dynamics 365 Project Operations (облегченное развертывание) по выставлению счетов-проформ.</span><span class="sxs-lookup"><span data-stu-id="275ed-104">This topic explains how to subscribe to the trial offer and deploy Dynamics 365 Project Operations lite deployment - deal to proforma invoicing.</span></span>

> [!NOTE]
> <span data-ttu-id="275ed-105">Этот процесс изменится в следующих выпусках Project Operations.</span><span class="sxs-lookup"><span data-stu-id="275ed-105">This process will change in upcoming releases of Project Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="275ed-106">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="275ed-106">Prerequisites</span></span>
- <span data-ttu-id="275ed-107">Пользователь, развертывающий предварительную версию, должен иметь права глобального администратора клиента Azure.</span><span class="sxs-lookup"><span data-stu-id="275ed-107">The user who deploys the preview must have Azure tenant global administrator rights.</span></span> <span data-ttu-id="275ed-108">Вы можете создать клиента во время первой активации предложения.</span><span class="sxs-lookup"><span data-stu-id="275ed-108">You can create a tenant during the first offer redemption.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="275ed-109">Только один человек, администратор клиента, в организации должен выполнять эту задачу.</span><span class="sxs-lookup"><span data-stu-id="275ed-109">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="275ed-110">Если вы не являетесь подписчиком этого выпуска, подождите, пока ваша организация не будет зарегистрирована и вы не получите свои учетные данные.</span><span class="sxs-lookup"><span data-stu-id="275ed-110">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>
> 
> <span data-ttu-id="275ed-111">Пробным предложением клиент может воспользоваться только один раз.</span><span class="sxs-lookup"><span data-stu-id="275ed-111">Trials are single use in the tenant.</span></span> <span data-ttu-id="275ed-112">Вы можете запустить пробную версию только один раз.</span><span class="sxs-lookup"><span data-stu-id="275ed-112">You can only run a trial one time.</span></span> <span data-ttu-id="275ed-113">Мы рекомендуем вам создать нового клиента для целей предоставления пробного версии.</span><span class="sxs-lookup"><span data-stu-id="275ed-113">We recommend that you create a new tenant for the purpose of the trial.</span></span>

### <a name="dynamics-365-project-operations-trial"></a><span data-ttu-id="275ed-114">Пробная версия Dynamics 365 Project Operations</span><span class="sxs-lookup"><span data-stu-id="275ed-114">Dynamics 365 Project Operations trial</span></span> 

<span data-ttu-id="275ed-115">Прежде чем начать, убедитесь, что вы вошли в браузер с рабочей учетной записью пользователя в клиенте, где вы хотите получить предварительную версию Project Operations.</span><span class="sxs-lookup"><span data-stu-id="275ed-115">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="275ed-116">Перейдите в раздел [Пробная версия Project Operations](https://aka.ms/try-po), чтобы активировать код первого предложения, **Dynamics 365 Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="275ed-116">Go to [Project Operations Trial](https://aka.ms/try-po) to redeem the first offer code, **Dynamics 365 Project Operations**.</span></span>
2. <span data-ttu-id="275ed-117">Подтвердите ваш заказ.</span><span class="sxs-lookup"><span data-stu-id="275ed-117">Confirm your order.</span></span>

  <span data-ttu-id="275ed-118">Вы увидите, что предложение успешно принято.</span><span class="sxs-lookup"><span data-stu-id="275ed-118">You'll see the confirmation offer was successfully redeemed.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="275ed-119">Назначение лицензий</span><span class="sxs-lookup"><span data-stu-id="275ed-119">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="275ed-120">Вам понадобится административный доступ к порталу Microsoft 365 вашей организации, чтобы выполнить следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="275ed-120">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>


1. <span data-ttu-id="275ed-121">Перейдите в [Центр администрирования Microsoft 365](https://portal.office.com/), чтобы назначить лицензии вашим пользователям.</span><span class="sxs-lookup"><span data-stu-id="275ed-121">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>
2. <span data-ttu-id="275ed-122">На странице **Активные пользователи** выберите пользователей, которым вы хотите назначить лицензию.</span><span class="sxs-lookup"><span data-stu-id="275ed-122">On the **Active users** page, select the users that you want to assign a license to.</span></span>
3. <span data-ttu-id="275ed-123">Убедитесь, что выбрана лицензия **Dynamics 365 Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="275ed-123">Verify that the **Dynamics 365 Project Operations** license is selected.</span></span> 
4. <span data-ttu-id="275ed-124">Выберите **Сохранить изменения**.</span><span class="sxs-lookup"><span data-stu-id="275ed-124">Select **Save changes**.</span></span>

## <a name="create-a-new-dataverse-environment"></a><span data-ttu-id="275ed-125">Создание новой среды Dataverse</span><span class="sxs-lookup"><span data-stu-id="275ed-125">Create a new Dataverse environment</span></span>

1. <span data-ttu-id="275ed-126">Подготовьте новую среду развертывания Project Operations Dataverse, следуя инструкциям в теме [модель развертывания Dataverse](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="275ed-126">Provision a new Project Operations Dataverse deployment environment by following instructions in the topic, [Dataverse deployment model](lite-deployment.md).</span></span> <span data-ttu-id="275ed-127">При выборе типа среды обязательно используйте вариант **Пробная версия (по подписке)**.</span><span class="sxs-lookup"><span data-stu-id="275ed-127">When you select the environment type, make sure to use **Trial (Subscription based)**.</span></span>

  ![Создать среду](./media/19CreateEnvironment.png)

2. <span data-ttu-id="275ed-129">Выберите параметр **Включение приложений Dynamics 365** и оставьте поле **Автоматически развернуть эти приложения** пустым.</span><span class="sxs-lookup"><span data-stu-id="275ed-129">Select the **Enable Dynamics 365 apps** setting, and leave **Automatically deploy these apps** blank.</span></span>  
3. <span data-ttu-id="275ed-130">Выберите **Сохранить**, чтобы создать среду.</span><span class="sxs-lookup"><span data-stu-id="275ed-130">Select **Save** to create the environment.</span></span>

  ![Добавить базу данных](./media/20CreateEnvironment1.png)

4. <span data-ttu-id="275ed-132">После создания среды установите решение **Microsoft Dynamics 365 Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="275ed-132">After the environment is created, install **Microsoft Dynamics 365 Project Operations** solution.</span></span> 

![Установка решения](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a><span data-ttu-id="275ed-134">Установка демонстрационных данных конфигурации и настройки CDS</span><span class="sxs-lookup"><span data-stu-id="275ed-134">Install a CDS configuration and setup demo data</span></span>

<span data-ttu-id="275ed-135">Установите демонстрационные данные конфигурации и настройки CDS, следуя инструкциям в теме [Применение демонстрационных данных настройки и конфигурации](lite-apply-demo-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="275ed-135">Install the CDS configuration and set up demo data by following instructions in the topic, [Apply demo setup and configuration data](lite-apply-demo-setup-config-data.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
