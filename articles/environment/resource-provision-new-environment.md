---
title: Подготовка новой среды
description: Эта тема предоставляет информацию о подготовке новой среды Project Operations.
author: sigitac
manager: Annbe
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9ee9e4c31d1972e3a75ad214071b31527f0ca826
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950550"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="29d0f-103">Подготовка новой среды</span><span class="sxs-lookup"><span data-stu-id="29d0f-103">Provision a new environment</span></span>

<span data-ttu-id="29d0f-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/без запасов_</span><span class="sxs-lookup"><span data-stu-id="29d0f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="29d0f-105">В этом разделе представлена информация о том, как подготовить новую среду Dynamics 365 Project Operations для сценариев на основе ресурсов/без запасов.</span><span class="sxs-lookup"><span data-stu-id="29d0f-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="29d0f-106">Включение автоматической подготовки Project Operations в проекте LCS</span><span class="sxs-lookup"><span data-stu-id="29d0f-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="29d0f-107">Используйте следующие шаги, чтобы включить поток автоматической подготовки Project Operations для вашего проекта LCS.</span><span class="sxs-lookup"><span data-stu-id="29d0f-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="29d0f-108">Перейдите к [LCS](https://lcs.dynamics.com/v2) и выберите плитку **Управление предварительными версиями функций**.</span><span class="sxs-lookup"><span data-stu-id="29d0f-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="29d0f-109">В списке **Предварительная версия функции** выберите **Функция Project Operations** и выберите **Предварительная версия функции включена**, чтобы включить Project Operations.</span><span class="sxs-lookup"><span data-stu-id="29d0f-109">In the **Preview feature** list, select **Project Operations Feature**, and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="29d0f-110">Этот шаг выполняется только один раз для каждого проекта LCS.</span><span class="sxs-lookup"><span data-stu-id="29d0f-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="29d0f-111">Подготовка среды Project Operations</span><span class="sxs-lookup"><span data-stu-id="29d0f-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="29d0f-112">Откройте новую [демонстрационную среду](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) Dynamics 365 Finance или развертывание [песочницы/производственной среды](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure).</span><span class="sxs-lookup"><span data-stu-id="29d0f-112">Open a new Dynamics 365 Finance [demo environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="29d0f-113">Перейдите к мастеру **Подготовка среды**.</span><span class="sxs-lookup"><span data-stu-id="29d0f-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="29d0f-114">Убедитесь, что выбрана версия приложения 10.0.13 или выше.</span><span class="sxs-lookup"><span data-stu-id="29d0f-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="29d0f-115">Для подготовки Project Operations в разделе **Дополнительные параметры** выберите **Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="29d0f-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="29d0f-116">Включите параметр **Настройка Common Data Service**, выбрав **Да**, затем введите информацию в обязательные поля:</span><span class="sxs-lookup"><span data-stu-id="29d0f-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="29d0f-117">Название</span><span class="sxs-lookup"><span data-stu-id="29d0f-117">Name</span></span>
  - <span data-ttu-id="29d0f-118">Область</span><span class="sxs-lookup"><span data-stu-id="29d0f-118">Region</span></span>
  - <span data-ttu-id="29d0f-119">Язык</span><span class="sxs-lookup"><span data-stu-id="29d0f-119">Language</span></span>
  - <span data-ttu-id="29d0f-120">Валюта</span><span class="sxs-lookup"><span data-stu-id="29d0f-120">Currency</span></span>
 
5. <span data-ttu-id="29d0f-121">В поле **Шаблон Common Data Service** выберите **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="29d0f-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="29d0f-122">Выберите тип среды для вашего развертывания.</span><span class="sxs-lookup"><span data-stu-id="29d0f-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="29d0f-123">Пробная версия на основе подписки позволит вам развернуть среду CDS на 30 дней.</span><span class="sxs-lookup"><span data-stu-id="29d0f-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Параметры развертывания](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="29d0f-125">Выберите **Принимаю**, чтобы подтвердить условия использования, затем выберите **Готово**, чтобы вернуться к настройкам развертывания.</span><span class="sxs-lookup"><span data-stu-id="29d0f-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Согласие на развертывание](./media/2DeploymentConsent.png)

7. <span data-ttu-id="29d0f-127">Необязательно — примените демонстрационные данные к среде.</span><span class="sxs-lookup"><span data-stu-id="29d0f-127">Optional - Apply demo data to the environment.</span></span> <span data-ttu-id="29d0f-128">Перейдите к **Дополнительные параметры**, выберите **Настроить конфигурацию базы данных SQL**, и установите **Укажите набор данных для базы данных приложения** на **Демонстрация**.</span><span class="sxs-lookup"><span data-stu-id="29d0f-128">Go to **Advanced settings**, select **Customize SQL Database Configuration**, and set **Specify a dataset for Application database** to **Demo**.</span></span>

8. <span data-ttu-id="29d0f-129">Заполните оставшиеся обязательные поля в мастере и подтвердите развертывание.</span><span class="sxs-lookup"><span data-stu-id="29d0f-129">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="29d0f-130">Время подготовки среды зависит от типа среды.</span><span class="sxs-lookup"><span data-stu-id="29d0f-130">The time to provision the environment varies based on the environment type.</span></span> <span data-ttu-id="29d0f-131">Подготовка может занять до шести часов.</span><span class="sxs-lookup"><span data-stu-id="29d0f-131">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="29d0f-132">После успешного завершения развертывания среда будет отображаться как **Развернуто**.</span><span class="sxs-lookup"><span data-stu-id="29d0f-132">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

9. <span data-ttu-id="29d0f-133">Чтобы убедиться, что среда успешно развернута, выберите **Вход** и войдите в среду для подтверждения.</span><span class="sxs-lookup"><span data-stu-id="29d0f-133">To confirm that the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![Сведения о среде ](./media/3EnvironmentDetails.png)

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="29d0f-135">Применение обновлений к среде Finance</span><span class="sxs-lookup"><span data-stu-id="29d0f-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="29d0f-136">Для Project Operations требуется среда Finance с версией приложения **10.0.13 (10.0.569.20009)** или выше.</span><span class="sxs-lookup"><span data-stu-id="29d0f-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="29d0f-137">Для получения этой версии вам может потребоваться применить качественные обновления к вашей среде Finance.</span><span class="sxs-lookup"><span data-stu-id="29d0f-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="29d0f-138">В LCS на странице **Сведения о среде** в разделе **Доступные обновления** выберите **Посмотреть обновление**.</span><span class="sxs-lookup"><span data-stu-id="29d0f-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Просмотр обновлений](./media/5ViewUpdates.png)

2. <span data-ttu-id="29d0f-140">На странице **Двоичные обновления** выберите **Сохранить пакет.**</span><span class="sxs-lookup"><span data-stu-id="29d0f-140">On the **Binary updates** page, select **Save package.**</span></span>

![Сохранить пакет](./media/6SavePackage.png)

3. <span data-ttu-id="29d0f-142">Выберите **Сохранить все** и затем выберите **Сохранить пакет**.</span><span class="sxs-lookup"><span data-stu-id="29d0f-142">Click **Select all** and then select **Save package**.</span></span>

![Просмотр и сохранение обновлений](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="29d0f-144">Введите имя и описание пакета, затем выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="29d0f-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="29d0f-145">В зависимости от подключения к Интернету этот процесс может занять некоторое время.</span><span class="sxs-lookup"><span data-stu-id="29d0f-145">Depending on the internet connection, this process might take some time.</span></span>

![Отправка пакета в библиотеку ресурсов](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="29d0f-147">После сохранения пакета выберите **Готово** и сохраните этот пакет в библиотеке ресурсов вашего проекта LCS.</span><span class="sxs-lookup"><span data-stu-id="29d0f-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="29d0f-148">Сохранение и проверка пакета может занять около 15 минут.</span><span class="sxs-lookup"><span data-stu-id="29d0f-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="29d0f-149">Чтобы применить обновление, перейдите на страницу **Сведения о среде** в LCS и выберите **Ведение** > **Применить обновления**.</span><span class="sxs-lookup"><span data-stu-id="29d0f-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Ведение сред](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="29d0f-151">В списке обновлений выберите созданный вами пакет и выберите **Применять**.</span><span class="sxs-lookup"><span data-stu-id="29d0f-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Применить обновления](./media/10ApplyUpdates.png)

<span data-ttu-id="29d0f-153">Обслуживание среды займет некоторое время.</span><span class="sxs-lookup"><span data-stu-id="29d0f-153">Environment servicing will take some time.</span></span> <span data-ttu-id="29d0f-154">После его завершения среда вернется в развернутое состояние.</span><span class="sxs-lookup"><span data-stu-id="29d0f-154">After it is complete, the environment will return to a deployed state.</span></span>

![Среда развернута](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="29d0f-156">Установка соединения с двойной записью</span><span class="sxs-lookup"><span data-stu-id="29d0f-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="29d0f-157">В своем проекте LCS перейдите на страницу **Сведения о среде**.</span><span class="sxs-lookup"><span data-stu-id="29d0f-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="29d0f-158">В разделе **Сведения о среде Common Data Service** выберите **Ссылка на CDS для приложений**.</span><span class="sxs-lookup"><span data-stu-id="29d0f-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="29d0f-159">После создания ссылки снова выберите **Ссылка на CDS для приложений**.</span><span class="sxs-lookup"><span data-stu-id="29d0f-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="29d0f-160">Вы будете перенаправлены на страницу двойной записи в Finance.</span><span class="sxs-lookup"><span data-stu-id="29d0f-160">You will be redirected to Dual Write in Finance.</span></span>

![Связь с CDS](./media/12LinktoCDS.png)

4. <span data-ttu-id="29d0f-162">Выберите **Применить решение** для доступа к сущностям, которые будут сопоставлены при интеграции.</span><span class="sxs-lookup"><span data-stu-id="29d0f-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Применение решений](./media/13ApplySolutions.png)

5. <span data-ttu-id="29d0f-164">Выберите оба решения, **Сопоставление сущностей с двойной записью Dynamics 365 Finance and Operations**, а также **Сопоставления сущностей с двойной записью Dynamics 365 Project Operations**, а затем выберите **Применить**.</span><span class="sxs-lookup"><span data-stu-id="29d0f-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![Подтверждение решений](./media/14ConfirmSolutions.png)

<span data-ttu-id="29d0f-166">После применения решений к среде применяются сущности двойной записи.</span><span class="sxs-lookup"><span data-stu-id="29d0f-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Применение решений](./media/15ApplyingSolutions.png)

<span data-ttu-id="29d0f-168">После применения сущностей все доступные сопоставления перечислены в среде.</span><span class="sxs-lookup"><span data-stu-id="29d0f-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Сопоставления двойной записи](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="29d0f-170">Обновление сущностей данных после обновления</span><span class="sxs-lookup"><span data-stu-id="29d0f-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="29d0f-171">В Finance перейдите в рабочую область **Управление данными**.</span><span class="sxs-lookup"><span data-stu-id="29d0f-171">In Finance, go to the **Data management** workspace.</span></span>

![Рабочая область управления данными](./media/16DataManagement.png)

2. <span data-ttu-id="29d0f-173">Выберите плитку **Параметры структуры**.</span><span class="sxs-lookup"><span data-stu-id="29d0f-173">Select the **Framework parameters** tile.</span></span>

![Параметры структуры](./media/17FrameworkParameters.png)

3. <span data-ttu-id="29d0f-175">На странице **Параметры сущности** выберите **Обновить список сущностей**.</span><span class="sxs-lookup"><span data-stu-id="29d0f-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Обновление списка сущностей](./media/18RefreshEntityList.png)

<span data-ttu-id="29d0f-177">Обновление займет около 20 минут.</span><span class="sxs-lookup"><span data-stu-id="29d0f-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="29d0f-178">Вы получите уведомление, когда оно будет завершено.</span><span class="sxs-lookup"><span data-stu-id="29d0f-178">You will receive an alert when it is complete.</span></span>

![Подтверждение обновления](./media/19RefreshConfirmation.png)

## <a name="update-security-settings-on-project-operations-on-dataverse"></a><span data-ttu-id="29d0f-180">Обновите настройки безопасности в Project Operations на Dataverse</span><span class="sxs-lookup"><span data-stu-id="29d0f-180">Update security settings on Project Operations on Dataverse</span></span>

1. <span data-ttu-id="29d0f-181">Перейдите к Project Operations в вашей среде Dataverse.</span><span class="sxs-lookup"><span data-stu-id="29d0f-181">Go to Project Operations on your Dataverse environment.</span></span> 
2. <span data-ttu-id="29d0f-182">Перейдите к **Параметры** > **Безопасность** > **Роли безопасности**.</span><span class="sxs-lookup"><span data-stu-id="29d0f-182">Go to **Settings** > **Security** > **Security roles**.</span></span> 
3. <span data-ttu-id="29d0f-183">На странице **Роли безопасности** в списке ролей выберите **пользователь приложения с двойной записью** и выберите вкладку **Настраиваемые сущности**.</span><span class="sxs-lookup"><span data-stu-id="29d0f-183">On the **Security roles** page, in the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span>  
4. <span data-ttu-id="29d0f-184">Убедитесь, что роль установлена на **Чтение** и разрешения **Добавить к** для:</span><span class="sxs-lookup"><span data-stu-id="29d0f-184">Verify that the role has **Read** and **Append To** permissions for the:</span></span>
      
      - <span data-ttu-id="29d0f-185">**Тип обменного курса валют**</span><span class="sxs-lookup"><span data-stu-id="29d0f-185">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="29d0f-186">**План счетов**</span><span class="sxs-lookup"><span data-stu-id="29d0f-186">**Chart Of Accounts**</span></span>
      - <span data-ttu-id="29d0f-187">**Финансовый календарь**</span><span class="sxs-lookup"><span data-stu-id="29d0f-187">**Fiscal Calendar**</span></span>
      - <span data-ttu-id="29d0f-188">**Реестр**</span><span class="sxs-lookup"><span data-stu-id="29d0f-188">**Ledger**</span></span>

5. <span data-ttu-id="29d0f-189">После обновления роль безопасности перейдите к **Параметры** > **Безопасность** > **Рабочие группы**, и выберите рабочую группу по умолчанию в представлении **Рабочие группы ответственного локального подразделения**.</span><span class="sxs-lookup"><span data-stu-id="29d0f-189">After the security role is updated, go to **Settings** > **Security** > **Teams**, and select the default team in the **Local Business Owner** team view.</span></span>
6. <span data-ttu-id="29d0f-190">Выберите **Управление ролями** и убедитесь, что привилегии безопасности **пользователь приложения с двойной записью** применяются к этой рабочей группе.</span><span class="sxs-lookup"><span data-stu-id="29d0f-190">Select **Manage Roles** and verify that the **dual-write app user** security privilege is applied to this team.</span></span>

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="29d0f-191">Запуск сопоставлений двойной записи Project Operations</span><span class="sxs-lookup"><span data-stu-id="29d0f-191">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="29d0f-192">В своем проекте LCS перейдите на страницу **Сведения о среде**.</span><span class="sxs-lookup"><span data-stu-id="29d0f-192">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="29d0f-193">В разделе **Сведения о среде Common Data Service** выберите **Ссылка на CDS для приложений.**</span><span class="sxs-lookup"><span data-stu-id="29d0f-193">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="29d0f-194">После выбора ссылки вы будете перенаправлены к списку сущностей в сопоставлениях.</span><span class="sxs-lookup"><span data-stu-id="29d0f-194">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="29d0f-195">Запустите сопоставления, как описано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="29d0f-195">Start the maps as described in the following table.</span></span> <span data-ttu-id="29d0f-196">Убедитесь, что вы соблюдаете указанную последовательность.</span><span class="sxs-lookup"><span data-stu-id="29d0f-196">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="29d0f-197">**Сопоставление сущностей**</span><span class="sxs-lookup"><span data-stu-id="29d0f-197">**Entity Map**</span></span> | <span data-ttu-id="29d0f-198">**Обновление сущности**</span><span class="sxs-lookup"><span data-stu-id="29d0f-198">**Refresh entity**</span></span> | <span data-ttu-id="29d0f-199">**Начальная синхронизация**</span><span class="sxs-lookup"><span data-stu-id="29d0f-199">**Initial sync**</span></span> | <span data-ttu-id="29d0f-200">**Главный объект для начальной синхронизации**</span><span class="sxs-lookup"><span data-stu-id="29d0f-200">**Master for initial sync**</span></span> | <span data-ttu-id="29d0f-201">**Выполнение необходимых условий**</span><span class="sxs-lookup"><span data-stu-id="29d0f-201">**Run prerequisites**</span></span> | <span data-ttu-id="29d0f-202">**Начальная синхронизация необходимых условий**</span><span class="sxs-lookup"><span data-stu-id="29d0f-202">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="29d0f-203">**Роли ресурсов проекта для всех компаний (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="29d0f-203">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="29d0f-204">No</span><span class="sxs-lookup"><span data-stu-id="29d0f-204">No</span></span> | <span data-ttu-id="29d0f-205">Да</span><span class="sxs-lookup"><span data-stu-id="29d0f-205">Yes</span></span> | <span data-ttu-id="29d0f-206">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="29d0f-206">Common Data Service</span></span> | <span data-ttu-id="29d0f-207">No</span><span class="sxs-lookup"><span data-stu-id="29d0f-207">No</span></span> | <span data-ttu-id="29d0f-208">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="29d0f-208">N\A</span></span> |
| <span data-ttu-id="29d0f-209">**Юридические лица (cdm\_companies)**</span><span class="sxs-lookup"><span data-stu-id="29d0f-209">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="29d0f-210">No</span><span class="sxs-lookup"><span data-stu-id="29d0f-210">No</span></span> | <span data-ttu-id="29d0f-211">Да</span><span class="sxs-lookup"><span data-stu-id="29d0f-211">Yes</span></span> | <span data-ttu-id="29d0f-212">Приложения Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="29d0f-212">Finance and Operations apps</span></span> | <span data-ttu-id="29d0f-213">No</span><span class="sxs-lookup"><span data-stu-id="29d0f-213">No</span></span> | <span data-ttu-id="29d0f-214">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="29d0f-214">N\A</span></span> |
| <span data-ttu-id="29d0f-215">**Книга учета (msdyn_ledgers)**</span><span class="sxs-lookup"><span data-stu-id="29d0f-215">**Ledger (msdyn_ledgers)**</span></span> | <span data-ttu-id="29d0f-216">No</span><span class="sxs-lookup"><span data-stu-id="29d0f-216">No</span></span> | <span data-ttu-id="29d0f-217">Да</span><span class="sxs-lookup"><span data-stu-id="29d0f-217">Yes</span></span> | <span data-ttu-id="29d0f-218">Приложения Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="29d0f-218">Finance and Operations apps</span></span> | <span data-ttu-id="29d0f-219">Да</span><span class="sxs-lookup"><span data-stu-id="29d0f-219">Yes</span></span> | <span data-ttu-id="29d0f-220">Да, приложения Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="29d0f-220">Yes, Finance and Operations apps</span></span> |
| <span data-ttu-id="29d0f-221">**Фактические данные интеграции Project Operations (msdyn\_actuals)**</span><span class="sxs-lookup"><span data-stu-id="29d0f-221">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="29d0f-222">No</span><span class="sxs-lookup"><span data-stu-id="29d0f-222">No</span></span> | <span data-ttu-id="29d0f-223">No</span><span class="sxs-lookup"><span data-stu-id="29d0f-223">No</span></span> | <span data-ttu-id="29d0f-224">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="29d0f-224">N\A</span></span> | <span data-ttu-id="29d0f-225">Да</span><span class="sxs-lookup"><span data-stu-id="29d0f-225">Yes</span></span> | <span data-ttu-id="29d0f-226">No</span><span class="sxs-lookup"><span data-stu-id="29d0f-226">No</span></span> |
| <span data-ttu-id="29d0f-227">**Строки контракта по проекту (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="29d0f-227">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="29d0f-228">No</span><span class="sxs-lookup"><span data-stu-id="29d0f-228">No</span></span> | <span data-ttu-id="29d0f-229">No</span><span class="sxs-lookup"><span data-stu-id="29d0f-229">No</span></span> | <span data-ttu-id="29d0f-230">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="29d0f-230">N\A</span></span> | <span data-ttu-id="29d0f-231">No</span><span class="sxs-lookup"><span data-stu-id="29d0f-231">No</span></span> | <span data-ttu-id="29d0f-232">No</span><span class="sxs-lookup"><span data-stu-id="29d0f-232">No</span></span> |
| <span data-ttu-id="29d0f-233">**Сущность интеграции для отношений транзакций проекта (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="29d0f-233">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="29d0f-234">No</span><span class="sxs-lookup"><span data-stu-id="29d0f-234">No</span></span> | <span data-ttu-id="29d0f-235">No</span><span class="sxs-lookup"><span data-stu-id="29d0f-235">No</span></span> | <span data-ttu-id="29d0f-236">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="29d0f-236">N\A</span></span> | <span data-ttu-id="29d0f-237">No</span><span class="sxs-lookup"><span data-stu-id="29d0f-237">No</span></span> | <span data-ttu-id="29d0f-238">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="29d0f-238">N\A</span></span> |
| <span data-ttu-id="29d0f-239">**Основные этапы строки контракта интеграции Project Operations (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="29d0f-239">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="29d0f-240">No</span><span class="sxs-lookup"><span data-stu-id="29d0f-240">No</span></span> | <span data-ttu-id="29d0f-241">No</span><span class="sxs-lookup"><span data-stu-id="29d0f-241">No</span></span> | <span data-ttu-id="29d0f-242">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="29d0f-242">N\A</span></span> | <span data-ttu-id="29d0f-243">No</span><span class="sxs-lookup"><span data-stu-id="29d0f-243">No</span></span> | <span data-ttu-id="29d0f-244">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="29d0f-244">N\A</span></span> |
| <span data-ttu-id="29d0f-245">**Сущность интеграции Project Operations для оценки расходов (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="29d0f-245">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="29d0f-246">No</span><span class="sxs-lookup"><span data-stu-id="29d0f-246">No</span></span> | <span data-ttu-id="29d0f-247">No</span><span class="sxs-lookup"><span data-stu-id="29d0f-247">No</span></span> | <span data-ttu-id="29d0f-248">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="29d0f-248">N\A</span></span> | <span data-ttu-id="29d0f-249">No</span><span class="sxs-lookup"><span data-stu-id="29d0f-249">No</span></span> | <span data-ttu-id="29d0f-250">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="29d0f-250">N\A</span></span> |
| <span data-ttu-id="29d0f-251">**Сущность экспорта категорий расходов проекта интеграции Project Operations (msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="29d0f-251">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="29d0f-252">No</span><span class="sxs-lookup"><span data-stu-id="29d0f-252">No</span></span> | <span data-ttu-id="29d0f-253">No</span><span class="sxs-lookup"><span data-stu-id="29d0f-253">No</span></span> | <span data-ttu-id="29d0f-254">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="29d0f-254">N\A</span></span> | <span data-ttu-id="29d0f-255">No</span><span class="sxs-lookup"><span data-stu-id="29d0f-255">No</span></span> | <span data-ttu-id="29d0f-256">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="29d0f-256">N\A</span></span> |
| <span data-ttu-id="29d0f-257">**Сущность экспорта расходов проекта интеграции Project Operations (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="29d0f-257">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="29d0f-258">Да</span><span class="sxs-lookup"><span data-stu-id="29d0f-258">Yes</span></span> | <span data-ttu-id="29d0f-259">No</span><span class="sxs-lookup"><span data-stu-id="29d0f-259">No</span></span> | <span data-ttu-id="29d0f-260">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="29d0f-260">N\A</span></span> | <span data-ttu-id="29d0f-261">No</span><span class="sxs-lookup"><span data-stu-id="29d0f-261">No</span></span> | <span data-ttu-id="29d0f-262">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="29d0f-262">N\A</span></span> |
| <span data-ttu-id="29d0f-263">**Сущность интеграции Project Operations для оценки часов (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="29d0f-263">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="29d0f-264">Да</span><span class="sxs-lookup"><span data-stu-id="29d0f-264">Yes</span></span> | <span data-ttu-id="29d0f-265">No</span><span class="sxs-lookup"><span data-stu-id="29d0f-265">No</span></span> | <span data-ttu-id="29d0f-266">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="29d0f-266">N\A</span></span> | <span data-ttu-id="29d0f-267">No</span><span class="sxs-lookup"><span data-stu-id="29d0f-267">No</span></span> | <span data-ttu-id="29d0f-268">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="29d0f-268">N\A</span></span> |


4. <span data-ttu-id="29d0f-269">Чтобы обновить сущность, выберите имя сопоставления, затем выберите **Обновить сущности**.</span><span class="sxs-lookup"><span data-stu-id="29d0f-269">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![Обновление сопоставления](./media/20RefreshMapping.png)

5. <span data-ttu-id="29d0f-271">После завершения обновления запустите сопоставление.</span><span class="sxs-lookup"><span data-stu-id="29d0f-271">After the refresh is complete, run the map.</span></span> <span data-ttu-id="29d0f-272">Прежде чем включить следующее сопоставление, убедитесь, что сопоставление в таблице находится в состоянии **Запущено**.</span><span class="sxs-lookup"><span data-stu-id="29d0f-272">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="29d0f-273">Запуск сопоставлений с большим количеством предварительных условий может занять некоторое время.</span><span class="sxs-lookup"><span data-stu-id="29d0f-273">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="29d0f-274">Чтобы запустить сопоставление с предварительными условиями, включите переключатель **Показать связанные сопоставления сущностей**.</span><span class="sxs-lookup"><span data-stu-id="29d0f-274">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="29d0f-275">Если в таблице указано, что **Начальная синхронизация необходимых условий** имеет значение **Нет**, убедитесь, что флаг **Начальная синхронизация** имеет значение **Откл.** на всех сопоставления необходимых условий перед их запуском.</span><span class="sxs-lookup"><span data-stu-id="29d0f-275">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Запуск сопоставления](./media/21RunMap.png)

6. <span data-ttu-id="29d0f-277">Убедитесь, что все связанные с проектом сопоставления находятся в рабочем состоянии.</span><span class="sxs-lookup"><span data-stu-id="29d0f-277">Validate all project related maps are in the running state.</span></span>

![Все сопоставления работают](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a><span data-ttu-id="29d0f-279">Применение данных конфигурации в CDS для Project Operations (необязательно)</span><span class="sxs-lookup"><span data-stu-id="29d0f-279">Apply configuration data in CDS for Project Operations (optional)</span></span>

<span data-ttu-id="29d0f-280">Если вы применили демонстрационные данные к среде Finance, см. раздела [Настройка и применение данных конфигурации в Common Data Service для Project Operations](resource-apply-pro-setup-config-data.md), чтобы применить демонстрационные данные к среде CDS.</span><span class="sxs-lookup"><span data-stu-id="29d0f-280">If you have applied demo data to the Finance environment, see [Set up and apply configuration data in the Common Data Service for Project Operations](resource-apply-pro-setup-config-data.md) to apply demo data to CDS environment.</span></span>


<span data-ttu-id="29d0f-281">Теперь ваша среда Project Operations подготовлена и настроена.</span><span class="sxs-lookup"><span data-stu-id="29d0f-281">Your Project Operations environment is now provisioned and configured.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]