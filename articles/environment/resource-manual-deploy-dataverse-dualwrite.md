---
title: Ручное развертывание приложения Project Operations Dataverse с поддержкой двойной записи
description: В этом разделе объясняется, как вручную развернуть приложение Project Operations Dataverse, чтобы обеспечить поддержку двойной записи.
author: stsporen
ms.date: 06/18/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 2ad147da542fc9e7a2705da7a834d1a6512907e5
ms.sourcegitcommit: 205a94ab4168de25b102f31d00a691c8205ba63e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/18/2021
ms.locfileid: "6274024"
---
# <a name="manually-deploy-the-project-operations-dataverse-app-with-dual-write-support"></a><span data-ttu-id="fca9a-103">Ручное развертывание приложения Project Operations Dataverse с поддержкой двойной записи</span><span class="sxs-lookup"><span data-stu-id="fca9a-103">Manually deploy the Project Operations Dataverse app with dual-write support</span></span>

<span data-ttu-id="fca9a-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/без запасов_</span><span class="sxs-lookup"><span data-stu-id="fca9a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="fca9a-105">В этом разделе объясняется, как вручную развернуть Microsoft Dynamics 365 Project Operations в Microsoft Dataverse, чтобы обеспечить поддержку двойной записи.</span><span class="sxs-lookup"><span data-stu-id="fca9a-105">This topic explains how to manually deploy Microsoft Dynamics 365 Project Operations in Microsoft Dataverse so that it supports dual-write.</span></span> <span data-ttu-id="fca9a-106">Project Operations определяет конфигурацию среды и добавляет дополнительную поддержку для двойной записи, если выполняются предварительные условия.</span><span class="sxs-lookup"><span data-stu-id="fca9a-106">Project Operations detects the environment's configuration and adds additional support for dual-write if the prerequisites are met.</span></span>

<span data-ttu-id="fca9a-107">Если во время развертывания через Microsoft Dynamics Lifecycle Services (LCS) вы следовали инструкциям из этого раздела, вы можете пропустить развертывание для интеграции Microsoft Power Platform (ранее известной как среда Common Data Service).</span><span class="sxs-lookup"><span data-stu-id="fca9a-107">During deployment through Microsoft Dynamics Lifecycle Services (LCS), if you've followed the instructions in this topic, you can skip the deployment of the Microsoft Power Platform integration (previously known as the Common Data Service environment).</span></span>

<span data-ttu-id="fca9a-108">Процесс развертывания Project Operations в Dataverse с поддержкой двойной записи включает четыре основных шага:</span><span class="sxs-lookup"><span data-stu-id="fca9a-108">The process of deploying Project Operations in Dataverse so that it supports dual-write has four main steps:</span></span>

1. <span data-ttu-id="fca9a-109">[Создайте новую среду в Dataverse, которая поддерживает двойную запись](#create).</span><span class="sxs-lookup"><span data-stu-id="fca9a-109">[Create a new environment in Dataverse that supports dual-write](#create).</span></span>
2. <span data-ttu-id="fca9a-110">[Добавьте в среду необходимые условия для двойной записи](#prerequisites).</span><span class="sxs-lookup"><span data-stu-id="fca9a-110">[Add dual-write prerequisites to the environment](#prerequisites).</span></span>
3. <span data-ttu-id="fca9a-111">[Добавьте приложение Project Operations Dataverse](#dataverse).</span><span class="sxs-lookup"><span data-stu-id="fca9a-111">[Add the Project Operations Dataverse app](#dataverse).</span></span>
4. <span data-ttu-id="fca9a-112">[Свяжите свои среды](#link).</span><span class="sxs-lookup"><span data-stu-id="fca9a-112">[Link your environments](#link).</span></span>

## <a name="create-a-new-environment-in-dataverse-that-supports-dual-write"></a><a name="create"></a><span data-ttu-id="fca9a-113">Создайте новую среду в Dataverse, которая поддерживает двойную запись</span><span class="sxs-lookup"><span data-stu-id="fca9a-113">Create a new environment in Dataverse that supports dual-write</span></span>

<span data-ttu-id="fca9a-114">Для выполнения этой процедуры вы должны войти в систему как администратор.</span><span class="sxs-lookup"><span data-stu-id="fca9a-114">To complete this procedure, you must sign in as an administrator.</span></span>

1. <span data-ttu-id="fca9a-115">Откройте [центр администрирования Power Platform](https://admin.powerplatform.com) и войдите как администратор.</span><span class="sxs-lookup"><span data-stu-id="fca9a-115">Open the [Power Platform admin center](https://admin.powerplatform.com), and sign in as an administrator.</span></span>
2. <span data-ttu-id="fca9a-116">Создайте новую среду и укажите ее имя.</span><span class="sxs-lookup"><span data-stu-id="fca9a-116">Create a new environment, and name it.</span></span>
3. <span data-ttu-id="fca9a-117">Выберите тип среды.</span><span class="sxs-lookup"><span data-stu-id="fca9a-117">Select the environment type.</span></span> <span data-ttu-id="fca9a-118">Если вы подписались на пробное предложение, выберите **Пробная версия (по подписке)**.</span><span class="sxs-lookup"><span data-stu-id="fca9a-118">If you signed up for the trial offer, select **Trial (subscription-based)**.</span></span>
4. <span data-ttu-id="fca9a-119">Подтвердите регион развертывания.</span><span class="sxs-lookup"><span data-stu-id="fca9a-119">Confirm the deployment region.</span></span>
5. <span data-ttu-id="fca9a-120">Включите параметр **Создать базу данных для этой среды**.</span><span class="sxs-lookup"><span data-stu-id="fca9a-120">Enable the **Create a database for this environment** option.</span></span> 
6. <span data-ttu-id="fca9a-121">Подтвердите язык, а затем убедитесь, что валюта соответствует валюте ваших приложений для Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="fca9a-121">Confirm the language, and then confirm that the currency matches the currency for your Finance and Operations apps.</span></span>
7. <span data-ttu-id="fca9a-122">Включите параметр **Приложения Dynamics 365** и убедитесь, что для поля **Автоматически разворачивать эти приложения** установлено значение **Нет**.</span><span class="sxs-lookup"><span data-stu-id="fca9a-122">Enable the **Dynamics 365 apps** option, and confirm that the **Automatically deploy these apps** field is set to **None**.</span></span>
8. <span data-ttu-id="fca9a-123">Добавьте группу безопасности, если она требуется.</span><span class="sxs-lookup"><span data-stu-id="fca9a-123">Add a security group, if a security group is required.</span></span>
9. <span data-ttu-id="fca9a-124">Выберите **Сохранить**, чтобы создать среду.</span><span class="sxs-lookup"><span data-stu-id="fca9a-124">Select **Save** to create the environment.</span></span>
10. <span data-ttu-id="fca9a-125">Подождите, пока развертывание не будет завершено и среда не достигнет состояния **Готово**.</span><span class="sxs-lookup"><span data-stu-id="fca9a-125">Wait until the deployment is completed and the environment reaches the **Ready** state.</span></span>

## <a name="add-dual-write-prerequisites-to-the-environment"></a><a name="prerequisites"></a><span data-ttu-id="fca9a-126">Добавить в среду необходимые условия для двойной записи</span><span class="sxs-lookup"><span data-stu-id="fca9a-126">Add dual-write prerequisites to the environment</span></span>

<span data-ttu-id="fca9a-127">Поддержка двойной записи включает дополнительные поля, которые добавляются к ключевым сущностям, таким как **Компания**.</span><span class="sxs-lookup"><span data-stu-id="fca9a-127">Dual-write support includes additional fields that are added to key entities, such as the **Company** entity.</span></span> <span data-ttu-id="fca9a-128">Если вы добавляете поддержку двойной записи в существующую среду, вам может потребоваться обновить данные, чтобы включить поддержку.</span><span class="sxs-lookup"><span data-stu-id="fca9a-128">If you're adding dual-write support to an existing environment, you might have to update the data to enable the support.</span></span> <span data-ttu-id="fca9a-129">Для получения информации о том, как загрузить данные, см. [Загрузка данных компании](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data).</span><span class="sxs-lookup"><span data-stu-id="fca9a-129">For information about how to bootstrap the data, see [Bootstrap company data](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data).</span></span> <span data-ttu-id="fca9a-130">Для получения дополнительной информации о двойной записи см. [Системные требования для двойной записи](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).</span><span class="sxs-lookup"><span data-stu-id="fca9a-130">For more information about dual-write, see [Dual-write system requirements](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).</span></span>

<span data-ttu-id="fca9a-131">Выполните эту процедуру, чтобы добавить в среду необходимые условия для двойной записи.</span><span class="sxs-lookup"><span data-stu-id="fca9a-131">Complete this procedure to add the dual-write prerequisites to your environment.</span></span>

1. <span data-ttu-id="fca9a-132">Откройте только что созданную среду и перейдите в раздел **Ресурс** \> **Приложения Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="fca9a-132">Open the environment that you just created, and then go to **Resource** \> **Dynamics 365 apps**.</span></span>
2. <span data-ttu-id="fca9a-133">Выберите **Ядро с двойной записью** в списке приложений и установите его.</span><span class="sxs-lookup"><span data-stu-id="fca9a-133">Select **Dual-write core solution** in the app list, and install it.</span></span>
3. <span data-ttu-id="fca9a-134">Дождитесь завершения установки.</span><span class="sxs-lookup"><span data-stu-id="fca9a-134">Wait until the installation is completed.</span></span> <span data-ttu-id="fca9a-135">Затем выберите **Оркестрация приложения для двойной записи** в списке приложений и установите его.</span><span class="sxs-lookup"><span data-stu-id="fca9a-135">Then select **Dual-write application orchestration solution** in the app list, and install it.</span></span>

## <a name="add-the-project-operations-dataverse-app"></a><a name="dataverse"></a><span data-ttu-id="fca9a-136">Добавить приложение Project Operations Dataverse</span><span class="sxs-lookup"><span data-stu-id="fca9a-136">Add the Project Operations Dataverse app</span></span>

<span data-ttu-id="fca9a-137">Вы можете выполнить эту процедуру, только если вы выполнили предыдущие процедуры перед установкой Project Operations.</span><span class="sxs-lookup"><span data-stu-id="fca9a-137">You can complete this procedure only if you completed the previous procedures before you installed Project Operations.</span></span> <span data-ttu-id="fca9a-138">Во время установки система анализирует конфигурацию среды и при необходимости добавляет поддержку двойной записи.</span><span class="sxs-lookup"><span data-stu-id="fca9a-138">During installation, the system analyzes the environment configuration and adds support for dual-write if it's required.</span></span>

1. <span data-ttu-id="fca9a-139">Откройте ранее созданную среду и перейдите в раздел **Ресурс** \> **Приложения Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="fca9a-139">Open the environment that you created earlier, and then go to **Resource** \> **Dynamics 365 apps**.</span></span>
2. <span data-ttu-id="fca9a-140">Выберите **Microsoft Dynamics 365 Project Operations** в списке приложений и установите его.</span><span class="sxs-lookup"><span data-stu-id="fca9a-140">Select **Microsoft Dynamics 365 Project Operations** in the app list, and install it.</span></span>

## <a name="link-your-environments"></a><a name="link"></a><span data-ttu-id="fca9a-141">Свяжите свои среды</span><span class="sxs-lookup"><span data-stu-id="fca9a-141">Link your environments</span></span>

<span data-ttu-id="fca9a-142">После того как среда Dataverse будет развернута, вы можете настроить ссылку в своих приложениях для Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="fca9a-142">After the Dataverse environment is deployed, you can set up the link in your Finance and Operations apps.</span></span> <span data-ttu-id="fca9a-143">Следуйте инструкциям по ссылке [Использование мастера двойной записи для связывания сред](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).</span><span class="sxs-lookup"><span data-stu-id="fca9a-143">Follow the steps in [Use the dual-write wizard to link your environments](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).</span></span>
