---
title: Регистрация на подписки на предварительную версию Project Operations для сценариев ресурсов/отсутствия запасов
description: Эта тема предоставляет информацию о том, как подписаться и развернуть roject Operations для сценариев на основе ресурсов/отсутствия запасов.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4d35a8bf9e8a841b45808b26ae2587c5b7d99d72
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949042"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a><span data-ttu-id="1d332-103">Регистрация на подписки на предварительную версию Project Operations для сценариев ресурсов/отсутствия запасов</span><span class="sxs-lookup"><span data-stu-id="1d332-103">Sign up for Project Operations preview subscriptions for resource/ non-stocked scenarios</span></span>

<span data-ttu-id="1d332-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/без запасов_</span><span class="sxs-lookup"><span data-stu-id="1d332-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="1d332-105">В этой теме объясняется, как подписаться на предварительную версию/предложение партнера и развернуть среду Project Operations для сценариев на основе ресурсов/отсутствия запасов.</span><span class="sxs-lookup"><span data-stu-id="1d332-105">This topic explains how to subscribe to the preview/partner offer and deploy Project Operations environment for resource/ non-stocked based scenarios.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="1d332-106">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="1d332-106">Prerequisites</span></span>

- <span data-ttu-id="1d332-107">Вы получите электронное письмо с приглашением принять участие в предварительной версии.</span><span class="sxs-lookup"><span data-stu-id="1d332-107">You will receive an email inviting you to participate in the preview.</span></span> <span data-ttu-id="1d332-108">Вы можете запросить предварительную версию на [веб-сайте Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span><span class="sxs-lookup"><span data-stu-id="1d332-108">You can request a preview on the [Project Operations website](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span></span>
- <span data-ttu-id="1d332-109">Пользователь, развертывающий предварительную версию, должен иметь права глобального администратора клиента Azure.</span><span class="sxs-lookup"><span data-stu-id="1d332-109">The user who deploys the preview must have Azure tenant global administrator rights.</span></span>
- <span data-ttu-id="1d332-110">Для развертывания среды Finance требуется действующая подписка Azure, за которую будет взиматься плата за среду.</span><span class="sxs-lookup"><span data-stu-id="1d332-110">Deploying a Finance environment requires a valid Azure subscription that will be billed per environment.</span></span> <span data-ttu-id="1d332-111">Вы можете использовать существующую подписку вашей организации или использовать [пробную версию Azure](https://azure.microsoft.com/en-us/free/) для начала.</span><span class="sxs-lookup"><span data-stu-id="1d332-111">You can use your organizations existing subscription or use an [Azure trial](https://azure.microsoft.com/en-us/free/) to get started.</span></span> <span data-ttu-id="1d332-112">Среда CDS будет предоставляться бесплатно в течение ограниченного 30-дневного периода.</span><span class="sxs-lookup"><span data-stu-id="1d332-112">The CDS environment will be provided free for a limited 30 day period.</span></span>

## <a name="subscribe"></a><span data-ttu-id="1d332-113">Подписаться</span><span class="sxs-lookup"><span data-stu-id="1d332-113">Subscribe</span></span>

<span data-ttu-id="1d332-114">Когда ваш [запрос на предварительную версию](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) будет утвержден, вы получите два предложения от Microsoft по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="1d332-114">When your [preview request](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) is approved, you will receive two offers from Microsoft by email.</span></span> <span data-ttu-id="1d332-115">Эти предложения позволяют развернуть предварительную версию Project Operations:</span><span class="sxs-lookup"><span data-stu-id="1d332-115">These offers allow you to deploy the Project Operations Preview:</span></span>

- <span data-ttu-id="1d332-116">Dynamics 365 Project Operations — пробная предварительная версия</span><span class="sxs-lookup"><span data-stu-id="1d332-116">Dynamics 365 Project Operations – Preview Trial</span></span>
- <span data-ttu-id="1d332-117">Пробная предварительная версия Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1d332-117">Dynamics 365 for Finance and Operations Preview Trial.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1d332-118">Только один человек, администратор клиента, в организации должен выполнять эту задачу.</span><span class="sxs-lookup"><span data-stu-id="1d332-118">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="1d332-119">Если вы не являетесь подписчиком этого выпуска, подождите, пока ваша организация не будет зарегистрирована и вы не получите свои учетные данные.</span><span class="sxs-lookup"><span data-stu-id="1d332-119">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>

### <a name="dynamics-365-project-operations--preview-trial"></a><span data-ttu-id="1d332-120">Dynamics 365 Project Operations — пробная предварительная версия</span><span class="sxs-lookup"><span data-stu-id="1d332-120">Dynamics 365 Project Operations – Preview trial</span></span>

1. <span data-ttu-id="1d332-121">Активируйте первое предложение, **Пробная версия Dynamics 365 Project Operations**, используя URL-адрес, указанный в приветственном письме.</span><span class="sxs-lookup"><span data-stu-id="1d332-121">Redeem the first offer, **Dynamics 365 Project Operations Trial**, with the URL provided in your welcome email.</span></span>

![Первое предложение](./media/1FirstOffer.png)

2. <span data-ttu-id="1d332-123">Убедитесь, что вы вошли в систему как пользователь, принадлежащий к организации, которая будет подписываться на службу.</span><span class="sxs-lookup"><span data-stu-id="1d332-123">Verify that you are logged in as the user who belongs to the organization who will be subscribing to the service.</span></span>
3. <span data-ttu-id="1d332-124">Продолжайте активировать предложение.</span><span class="sxs-lookup"><span data-stu-id="1d332-124">Proceed with redeeming the offer.</span></span> 
4. <span data-ttu-id="1d332-125">Выберите **Да, добавить в мою учетную запись**.</span><span class="sxs-lookup"><span data-stu-id="1d332-125">Select **Yes, add it to my account**.</span></span>

![Активировать предложение](./media/2RedeemFirstOffer.png)

![Подтвердить предложение](./media/3ConfirmFirstOffer.png)

![Предложение активировано](./media/4OfferSuccessfulyRedeemed.png)

### <a name="dynamics-365-finance-preview-trial"></a><span data-ttu-id="1d332-129">Пробная предварительная версия Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="1d332-129">Dynamics 365 Finance preview trial</span></span>

<span data-ttu-id="1d332-130">Повторите те же шаги со вторым предложением из приветственного письма.</span><span class="sxs-lookup"><span data-stu-id="1d332-130">Repeat the same steps with the second offer from the Welcome email.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="1d332-131">Назначение лицензий</span><span class="sxs-lookup"><span data-stu-id="1d332-131">Assign Licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1d332-132">Вам понадобится административный доступ к порталу Office 365 вашей организации, чтобы выполнить следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="1d332-132">You will need administrative access to your organization's Office 365 Portal to complete the following steps.</span></span>

1. <span data-ttu-id="1d332-133">Перейдите в [Центр администрирования Microsoft 365](https://portal.office.com/), чтобы назначить лицензии вашим пользователям.</span><span class="sxs-lookup"><span data-stu-id="1d332-133">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign licenses to your users.</span></span>

![Портал администрирования Office](./media/5OfficeAdminPortal.png)

2. <span data-ttu-id="1d332-135">На странице **Активные пользователи** выберите пользователей, которым вы хотите назначить лицензию.</span><span class="sxs-lookup"><span data-stu-id="1d332-135">On the **Active users** page, select the users that you want to assign a license to.</span></span>

![Назначение лицензий](./media/6AssignLicenses.png)

3. <span data-ttu-id="1d332-137">Убедитесь, что выбрана лицензия Project Operations, и выберите **Сохранить изменения**.</span><span class="sxs-lookup"><span data-stu-id="1d332-137">Verify that the Project Operations license has been selected and select **Save changes**.</span></span> 

> [!NOTE]
> <span data-ttu-id="1d332-138">Пробное предложение Finance не нужно назначать пользователю.</span><span class="sxs-lookup"><span data-stu-id="1d332-138">The Finance trial offer does not need to be assigned to a user.</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="1d332-139">Запуск нового проекта в LCS</span><span class="sxs-lookup"><span data-stu-id="1d332-139">Start a new project in LCS</span></span>

<span data-ttu-id="1d332-140">Создайте новый проект LCS, как описано в теме [Запуск нового проекта в LCS](create-lcs-project.md)</span><span class="sxs-lookup"><span data-stu-id="1d332-140">Create a new LCS project as described in the topic, [Start a new project in LCS](create-lcs-project.md)</span></span>

## <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="1d332-141">Добавление подписки Azure в проект LCS</span><span class="sxs-lookup"><span data-stu-id="1d332-141">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="1d332-142">Чтобы выполнить эту задачу, выполните действия, описанные в теме [Добавление подписки Azure в проект LCS](resource-add-azure-subscription-lcs-project.md).</span><span class="sxs-lookup"><span data-stu-id="1d332-142">To complete this task, follow the steps in the topic, [Add an Azure subscription to LCS project](resource-add-azure-subscription-lcs-project.md).</span></span>

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="1d332-143">Развертывание демонстрационной среды Finance с помощью Project Operations для сценариев, связанных с ресурсами/отсутствием запасов</span><span class="sxs-lookup"><span data-stu-id="1d332-143">Deploy Finance demo environment with Project Operations for resource/non-stocked scenarios</span></span>

<span data-ttu-id="1d332-144">Следуйте инструкциям в теме [Подготовка новой среды](resource-provision-new-environment.md) для завершения развертывания.</span><span class="sxs-lookup"><span data-stu-id="1d332-144">Follow the guidance in the topic, [Provision a new environment](resource-provision-new-environment.md) to complete the deployment.</span></span> <span data-ttu-id="1d332-145">Используйте тип развертывания [демонстрационной среды](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) для предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="1d332-145">Use the [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) deployment type for preview.</span></span>

## <a name="install-cds-setup-and-configuration-data"></a><span data-ttu-id="1d332-146">Установка данных настройки и конфигурации CDS</span><span class="sxs-lookup"><span data-stu-id="1d332-146">Install CDS setup and configuration data</span></span>

<span data-ttu-id="1d332-147">Установите данные настройки и конфигурации CDS, как описано в теме [Настройка и применение данных конфигурации в Common Data Service](resource-apply-pro-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="1d332-147">Install CDS setup and configuration data as described in the topic, [Set up and apply configuration data in the Common Data Service](resource-apply-pro-setup-config-data.md).</span></span>

