---
title: Добавление подписки Azure в проект LCS
description: Эта тема предоставляет информацию о том, как подключить подписку Azure к проекту LCS.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e741f35f9b229d2897cec06054d91ae620397228
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175817"
---
# <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="36d2c-103">Добавление подписки Azure в проект LCS</span><span class="sxs-lookup"><span data-stu-id="36d2c-103">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="36d2c-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/без запасов_</span><span class="sxs-lookup"><span data-stu-id="36d2c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="36d2c-105">Среды, размещенные в облаке, должны быть развернуты с использованием существующей подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="36d2c-105">Cloud-hosted environments must be deployed using an existing Azure subscription.</span></span> <span data-ttu-id="36d2c-106">Эта тема объясняет, как подключить существующую подписку Azure к проекту LCS.</span><span class="sxs-lookup"><span data-stu-id="36d2c-106">This topic explains how to connect your existing Azure subscription to an LCS project.</span></span> 

## <a name="grant-admin-consent"></a><span data-ttu-id="36d2c-107">Предоставление согласия администратора</span><span class="sxs-lookup"><span data-stu-id="36d2c-107">Grant admin consent</span></span>

1. <span data-ttu-id="36d2c-108">В вашем проекте LCS в разделе **Среды** выберите **Настройки Microsoft Azure**.</span><span class="sxs-lookup"><span data-stu-id="36d2c-108">In your LCS project, in the **Environments** section, select **Microsoft Azure settings**.</span></span>

![Параметры приложения Microsoft Azure](./media/1MicrosoftAzureSettings.png)

2. <span data-ttu-id="36d2c-110">На странице **Параметры проекта** на вкладке **Соединители Azure** выберите **Авторизовать**.</span><span class="sxs-lookup"><span data-stu-id="36d2c-110">On the **Project settings** page, on the **Azure connectors** tab, select **Authorize**.</span></span> <span data-ttu-id="36d2c-111">Это позволяет развертывать среды в этом проекте.</span><span class="sxs-lookup"><span data-stu-id="36d2c-111">This allows environments to be deployed to this project.</span></span>

![Соединители Azure](./media/2AzureConnectors.png)

3. <span data-ttu-id="36d2c-113">Выбрать **Авторизовать** еще раз, чтобы предоставить согласие администратора.</span><span class="sxs-lookup"><span data-stu-id="36d2c-113">Select **Authorize** again to provide admin consent.</span></span>

![Предоставление согласия администратора](./media/3GrantAdminConsent.png)

4. <span data-ttu-id="36d2c-115">Примите запрос на разрешения.</span><span class="sxs-lookup"><span data-stu-id="36d2c-115">Accept the permissions request.</span></span>

![Примите запрос на разрешения](./media/4AcceptPermissionRequest.png)

<span data-ttu-id="36d2c-117">Авторизация завершена.</span><span class="sxs-lookup"><span data-stu-id="36d2c-117">The authorization is now complete.</span></span> 

![Авторизация прошла успешно](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a><span data-ttu-id="36d2c-119">Предоставление службам развертывания Dynamics доступа к вашей подписке Azure</span><span class="sxs-lookup"><span data-stu-id="36d2c-119">Provide Dynamics Deployment Services access to your Azure subscription</span></span>

1. <span data-ttu-id="36d2c-120">Перейдите в раздел [Выставление счетов Microsoft Azure](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) и выберите свою подписку.</span><span class="sxs-lookup"><span data-stu-id="36d2c-120">Go to [Microsoft Azure billing](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) and select your subscription.</span></span> <span data-ttu-id="36d2c-121">Службам развертывания Dynamics необходим доступ к этой подписке, чтобы иметь возможность развертывать среды.</span><span class="sxs-lookup"><span data-stu-id="36d2c-121">Dynamics Deployment Services needs to access this subscription to be able to deploy environments.</span></span>

![Сведения о подписке Azure](./media/6AzureSubscription.png)

2. <span data-ttu-id="36d2c-123">Выберите **Контроль доступа (IAM)** в области навигации, затем выберите **Добавить назначение роли**.</span><span class="sxs-lookup"><span data-stu-id="36d2c-123">Select **Access control (IAM)** in the navigation pane, and then select **Add role assignment**.</span></span>
3. <span data-ttu-id="36d2c-124">В ползунке справа выберите **Участник роли** и в представленном списке найдите и выберите **Службы развертывания Dynamics**.</span><span class="sxs-lookup"><span data-stu-id="36d2c-124">In the slider on the right side, select **Contributor role**, and in the list provided, find and select **Dynamics Deployment Services**.</span></span> 
4. <span data-ttu-id="36d2c-125">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="36d2c-125">Select **Save**.</span></span>

![Доступ к подписке](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a><span data-ttu-id="36d2c-127">Добавление соединителя подписки в проект LCS</span><span class="sxs-lookup"><span data-stu-id="36d2c-127">Add a subscription connector to an LCS project</span></span>

1. <span data-ttu-id="36d2c-128">В вашем проекте LCS на странице **Параметры Microsoft Azure** выберите **Добавить**, чтобы добавить новый соединитель.</span><span class="sxs-lookup"><span data-stu-id="36d2c-128">In your LCS project, on the **Microsoft Azure settings** page, select **Add** to add a new connector.</span></span>
2. <span data-ttu-id="36d2c-129">Введите идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="36d2c-129">Enter your Azure subscription ID.</span></span> <span data-ttu-id="36d2c-130">Вы можете найти свой идентификатор подписки Azure в [портале Azure](https://ms.portal.azure.com/) в разделе **Параметры** в нижнем левом углу экрана.</span><span class="sxs-lookup"><span data-stu-id="36d2c-130">You can find your Azure subscription ID in the [Azure portal](https://ms.portal.azure.com/), under  **Settings**  in the lower left of the screen.</span></span>
3. <span data-ttu-id="36d2c-131">В поле **Настроить для использования Azure Resource Manager** выберите **Да**.</span><span class="sxs-lookup"><span data-stu-id="36d2c-131">In the **Configure to use Azure Resource Manager** field, select **Yes**.</span></span>
4. <span data-ttu-id="36d2c-132">Убедитесь, что домен клиента AAD для подписки Azure соответствует используемой подписке Azure, являющейся владельцем домена, и выберите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="36d2c-132">Make sure Azure's Subscription AAD Tenant Domain matches the domain-owning Azure subscription that you are using, and select **Next**.</span></span>
5. <span data-ttu-id="36d2c-133">На экране **Настройка Microsoft Azure** выберите **Далее**, чтобы подтвердить.</span><span class="sxs-lookup"><span data-stu-id="36d2c-133">On the **Microsoft Azure Setup** screen, select **Next** to confirm.</span></span> <span data-ttu-id="36d2c-134">Если вы получили сообщение об ошибке на этом экране, вернитесь в раздел [Предоставление доступа службам развертывания Dynamics к подписке Azure](#provide) в этой теме и убедитесь, что вы выполнили все шаги.</span><span class="sxs-lookup"><span data-stu-id="36d2c-134">If you receive an error on this screen, return to the section [Provide Dynamics Deployment Services access to Azure subscription](#provide) in this topic and make sure you have completed all of the steps.</span></span>
6. <span data-ttu-id="36d2c-135">Загрузите сертификат управления Azure в локальную папку на своем компьютере, затем отправьте его на портал управления Azure, перейдя в пункт **Параметры** > **Сертификаты управления**.</span><span class="sxs-lookup"><span data-stu-id="36d2c-135">Download the Azure Management Certificate to a local folder on your computer, and then upload it to Azure Management Portal by going to **Settings** > **Management Certificates**.</span></span> <span data-ttu-id="36d2c-136">Этот сертификат позволит LCS взаимодействовать с Azure от вашего имени.</span><span class="sxs-lookup"><span data-stu-id="36d2c-136">This certificate will enable LCS to communicate with Azure on your behalf.</span></span> <span data-ttu-id="36d2c-137">Вы можете пропустить этот шаг, если у вашего пользователя есть доступ к подписке.</span><span class="sxs-lookup"><span data-stu-id="36d2c-137">You can skip this step if your user has access to the subscription.</span></span>
7. <span data-ttu-id="36d2c-138">Выберите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="36d2c-138">Select  **Next**.</span></span>
8. <span data-ttu-id="36d2c-139">Выберите регион Azure для развертывания и выберите центр обработки данных, расположенный рядом с местом, где вы планируете использовать эту систему.</span><span class="sxs-lookup"><span data-stu-id="36d2c-139">Select the Azure region to deploy in and select a data center that is close to where you plan to use this system.</span></span>
9.  <span data-ttu-id="36d2c-140">Выберите **Подключиться**.</span><span class="sxs-lookup"><span data-stu-id="36d2c-140">Select  **Connect**.</span></span>

<span data-ttu-id="36d2c-141">Вы успешно подключили свою подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="36d2c-141">You have successfully connected your Azure subscription.</span></span> <span data-ttu-id="36d2c-142">Теперь вы можете развернуть развернутые в облаке среды Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="36d2c-142">You can now deploy Dynamics 365 Finance cloud-hosted environments.</span></span>


