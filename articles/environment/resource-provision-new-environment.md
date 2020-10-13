---
title: Подготовка новой среды
description: Эта тема предоставляет информацию о подготовке новой среды Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 45700371c50e3b5a840df45fc24fa8a5b4584b61
ms.sourcegitcommit: 87b7a8d793c19c50f3765b8d788cde24a6a0ca24
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949378"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="27418-103">Подготовка новой среды</span><span class="sxs-lookup"><span data-stu-id="27418-103">Provision a new environment</span></span>

<span data-ttu-id="27418-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/без запасов_</span><span class="sxs-lookup"><span data-stu-id="27418-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="27418-105">Эта тема предоставляет информацию о том, как подготовить новую среду Dynamics 365 Project Operations для сценариев на основе ресурсов/отсутствия запасов.</span><span class="sxs-lookup"><span data-stu-id="27418-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="27418-106">Включение автоматической подготовки Project Operations в проекте LCS</span><span class="sxs-lookup"><span data-stu-id="27418-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="27418-107">Используйте следующие шаги, чтобы включить поток автоматической подготовки Project Operations для вашего проекта LCS.</span><span class="sxs-lookup"><span data-stu-id="27418-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="27418-108">Перейдите к [LCS](https://lcs.dynamics.com/v2) и выберите плитку **Управление предварительными версиями функций**.</span><span class="sxs-lookup"><span data-stu-id="27418-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="27418-109">В списке **Предварительная версия функции** выберите **Project Operations** и выберите **Функция предварительного просмотра включена**, чтобы включить Project Operations.</span><span class="sxs-lookup"><span data-stu-id="27418-109">In the **Preview feature** list, select **Project Operations** and the select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="27418-110">Этот шаг выполняется только один раз для каждого проекта LCS.</span><span class="sxs-lookup"><span data-stu-id="27418-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="27418-111">Подготовка среды Project Operations</span><span class="sxs-lookup"><span data-stu-id="27418-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="27418-112">Откройте новую [демонстрационную среду](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) Dynamics 365 Finance или развертывание [песочницы/производственной среды](https://docs.microsoft.com/edynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure).</span><span class="sxs-lookup"><span data-stu-id="27418-112">Open a new Dynamics 365 Finance [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](https://docs.microsoft.com/edynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="27418-113">Перейдите к мастеру **Подготовка среды**.</span><span class="sxs-lookup"><span data-stu-id="27418-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="27418-114">Убедитесь, что выбрана версия приложения 10.0.13 или выше.</span><span class="sxs-lookup"><span data-stu-id="27418-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="27418-115">Для подготовки Project Operations в разделе **Дополнительные параметры** выберите **Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="27418-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="27418-116">Включите параметр **Настройка Common Data Service**, выбрав **Да**, затем введите информацию в обязательные поля:</span><span class="sxs-lookup"><span data-stu-id="27418-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="27418-117">Название</span><span class="sxs-lookup"><span data-stu-id="27418-117">Name</span></span>
  - <span data-ttu-id="27418-118">Область</span><span class="sxs-lookup"><span data-stu-id="27418-118">Region</span></span>
  - <span data-ttu-id="27418-119">Язык</span><span class="sxs-lookup"><span data-stu-id="27418-119">Language</span></span>
  - <span data-ttu-id="27418-120">Валюта</span><span class="sxs-lookup"><span data-stu-id="27418-120">Currency</span></span>
 
5. <span data-ttu-id="27418-121">В поле **Шаблон Common Data Service** выберите **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="27418-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="27418-122">Выберите тип среды для вашего развертывания.</span><span class="sxs-lookup"><span data-stu-id="27418-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="27418-123">Пробная версия на основе подписки позволит вам развернуть среду CDS на 30 дней.</span><span class="sxs-lookup"><span data-stu-id="27418-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Параметры развертывания](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="27418-125">Выберите **Принимаю**, чтобы подтвердить условия использования, затем выберите **Готово**, чтобы вернуться к настройкам развертывания.</span><span class="sxs-lookup"><span data-stu-id="27418-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Согласие на развертывание](./media/2DeploymentConsent.png)

7. <span data-ttu-id="27418-127">Заполните оставшиеся обязательные поля в мастере и подтвердите развертывание.</span><span class="sxs-lookup"><span data-stu-id="27418-127">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="27418-128">Время подготовки среды зависит от типа среды.</span><span class="sxs-lookup"><span data-stu-id="27418-128">Environment provisioning time varies based on the environment type.</span></span> <span data-ttu-id="27418-129">Подготовка может занять до шести часов.</span><span class="sxs-lookup"><span data-stu-id="27418-129">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="27418-130">После успешного завершения развертывания среда будет отображаться как **Развернуто**.</span><span class="sxs-lookup"><span data-stu-id="27418-130">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

8. <span data-ttu-id="27418-131">Чтобы убедиться, что среда успешно развернута, выберите **Войти** и войдите в среду для подтверждения.</span><span class="sxs-lookup"><span data-stu-id="27418-131">To confirm the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![Сведения о среде ](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a><span data-ttu-id="27418-133">Применение демонстрационных данных Project Operations Finance (необязательный шаг)</span><span class="sxs-lookup"><span data-stu-id="27418-133">Apply Project Operations Finance demo data (optional step)</span></span>

<span data-ttu-id="27418-134">Примените демонстрационные данные Project Operations Finance к размещенной в облаке среде выпуска службы 10.0.13, как описано в [этой статье](resource-apply-finance-demo-data.md).</span><span class="sxs-lookup"><span data-stu-id="27418-134">Apply Project Operations Finance demo data to 10.0.13 service release Cloud Hosted Environment as described in [this article](resource-apply-finance-demo-data.md).</span></span>

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="27418-135">Применение обновлений к среде Finance</span><span class="sxs-lookup"><span data-stu-id="27418-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="27418-136">Для Project Operations требуется среда Finance с версией приложения **10.0.13 (10.0.569.20009)** или выше.</span><span class="sxs-lookup"><span data-stu-id="27418-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="27418-137">Для получения этой версии вам может потребоваться применить качественные обновления к вашей среде Finance.</span><span class="sxs-lookup"><span data-stu-id="27418-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="27418-138">В LCS на странице **Сведения о среде** в разделе **Доступные обновления** выберите **Посмотреть обновление**.</span><span class="sxs-lookup"><span data-stu-id="27418-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Просмотр обновлений](./media/5ViewUpdates.png)

2. <span data-ttu-id="27418-140">На странице **Двоичные обновления** выберите **Сохранить пакет.**</span><span class="sxs-lookup"><span data-stu-id="27418-140">On the **Binary updates** page, select **Save package.**</span></span>

![Сохранить пакет](./media/6SavePackage.png)

3. <span data-ttu-id="27418-142">Выберите **Сохранить все** и затем выберите **Сохранить пакет**.</span><span class="sxs-lookup"><span data-stu-id="27418-142">Click **Select all** and then select **Save package**.</span></span>

![Просмотр и сохранение обновлений](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="27418-144">Введите имя и описание пакета, затем выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="27418-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="27418-145">В зависимости от подключения к Интернету этот процесс может занять некоторое время.</span><span class="sxs-lookup"><span data-stu-id="27418-145">Depending on the internet connection, this process might take some time.</span></span>

![Отправка пакета в библиотеку ресурсов](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="27418-147">После сохранения пакета выберите **Готово** и сохраните этот пакет в библиотеке ресурсов вашего проекта LCS.</span><span class="sxs-lookup"><span data-stu-id="27418-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="27418-148">Сохранение и проверка пакета может занять около 15 минут.</span><span class="sxs-lookup"><span data-stu-id="27418-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="27418-149">Чтобы применить обновление, перейдите на страницу **Сведения о среде** в LCS и выберите **Ведение** > **Применить обновления**.</span><span class="sxs-lookup"><span data-stu-id="27418-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Ведение сред](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="27418-151">В списке обновлений выберите созданный вами пакет и выберите **Применять**.</span><span class="sxs-lookup"><span data-stu-id="27418-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Применить обновления](./media/10ApplyUpdates.png)

<span data-ttu-id="27418-153">Обслуживание среды займет некоторое время.</span><span class="sxs-lookup"><span data-stu-id="27418-153">Environment servicing will take some time.</span></span> <span data-ttu-id="27418-154">После его завершения среда вернется в развернутое состояние.</span><span class="sxs-lookup"><span data-stu-id="27418-154">After it is complete, the environment will return to a deployed state.</span></span>

![Среда развернута](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="27418-156">Установка соединения с двойной записью</span><span class="sxs-lookup"><span data-stu-id="27418-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="27418-157">В своем проекте LCS перейдите на страницу **Сведения о среде**.</span><span class="sxs-lookup"><span data-stu-id="27418-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="27418-158">В разделе **Сведения о среде Common Data Service** выберите **Ссылка на CDS для приложений**.</span><span class="sxs-lookup"><span data-stu-id="27418-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="27418-159">После создания ссылки снова выберите **Ссылка на CDS для приложений**.</span><span class="sxs-lookup"><span data-stu-id="27418-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="27418-160">Вы будете перенаправлены на страницу двойной записи в Finance.</span><span class="sxs-lookup"><span data-stu-id="27418-160">You will be redirected to Dual Write in Finance.</span></span>

![Связь с CDS](./media/12LinktoCDS.png)

4. <span data-ttu-id="27418-162">Выберите **Применить решение** для доступа к сущностям, которые будут сопоставлены при интеграции.</span><span class="sxs-lookup"><span data-stu-id="27418-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Применение решений](./media/13ApplySolutions.png)

5. <span data-ttu-id="27418-164">Выберите оба решения, **Сопоставление сущностей двойной записи Dynamics 365 Finance and Operations** и **Сопоставления сущностей двойной записи Dynamics 365 Project Operations**, затем выберите **Применить**.</span><span class="sxs-lookup"><span data-stu-id="27418-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![Подтверждение решений](./media/14ConfirmSolutions.png)

<span data-ttu-id="27418-166">После применения решений к среде применяются сущности двойной записи.</span><span class="sxs-lookup"><span data-stu-id="27418-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Применение решений](./media/15ApplyingSolutions.png)

<span data-ttu-id="27418-168">После применения сущностей все доступные сопоставления перечислены в среде.</span><span class="sxs-lookup"><span data-stu-id="27418-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Сопоставления двойной записи](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="27418-170">Обновление сущностей данных после обновления</span><span class="sxs-lookup"><span data-stu-id="27418-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="27418-171">В Finance перейдите в рабочую область **Управление данными**.</span><span class="sxs-lookup"><span data-stu-id="27418-171">In Finance, go to the **Data management** workspace.</span></span>

![Рабочая область управления данными](./media/16DataManagement.png)

2. <span data-ttu-id="27418-173">Выберите плитку **Параметры структуры**.</span><span class="sxs-lookup"><span data-stu-id="27418-173">Select the **Framework parameters** tile.</span></span>

![Параметры структуры](./media/17FrameworkParameters.png)

3. <span data-ttu-id="27418-175">На странице **Параметры сущности** выберите **Обновить список сущностей**.</span><span class="sxs-lookup"><span data-stu-id="27418-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Обновление списка сущностей](./media/18RefreshEntityList.png)

<span data-ttu-id="27418-177">Обновление займет около 20 минут.</span><span class="sxs-lookup"><span data-stu-id="27418-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="27418-178">Вы получите уведомление, когда оно будет завершено.</span><span class="sxs-lookup"><span data-stu-id="27418-178">You will receive an alert when it is complete.</span></span>

![Подтверждение обновления](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="27418-180">Запуск сопоставлений двойной записи Project Operations</span><span class="sxs-lookup"><span data-stu-id="27418-180">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="27418-181">В своем проекте LCS перейдите на страницу **Сведения о среде**.</span><span class="sxs-lookup"><span data-stu-id="27418-181">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="27418-182">В разделе **Сведения о среде Common Data Service** выберите **Ссылка на CDS для приложений.**</span><span class="sxs-lookup"><span data-stu-id="27418-182">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="27418-183">После выбора ссылки вы будете перенаправлены к списку сущностей в сопоставлениях.</span><span class="sxs-lookup"><span data-stu-id="27418-183">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="27418-184">Запустите сопоставления, как описано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="27418-184">Start the maps as described in the following table.</span></span> <span data-ttu-id="27418-185">Убедитесь, что вы соблюдаете указанную последовательность.</span><span class="sxs-lookup"><span data-stu-id="27418-185">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="27418-186">**Сопоставление сущностей**</span><span class="sxs-lookup"><span data-stu-id="27418-186">**Entity Map**</span></span> | <span data-ttu-id="27418-187">**Обновление сущности**</span><span class="sxs-lookup"><span data-stu-id="27418-187">**Refresh entity**</span></span> | <span data-ttu-id="27418-188">**Начальная синхронизация**</span><span class="sxs-lookup"><span data-stu-id="27418-188">**Initial sync**</span></span> | <span data-ttu-id="27418-189">**Главный объект для начальной синхронизации**</span><span class="sxs-lookup"><span data-stu-id="27418-189">**Master for initial sync**</span></span> | <span data-ttu-id="27418-190">**Выполнение необходимых условий**</span><span class="sxs-lookup"><span data-stu-id="27418-190">**Run prerequisites**</span></span> | <span data-ttu-id="27418-191">**Начальная синхронизация необходимых условий**</span><span class="sxs-lookup"><span data-stu-id="27418-191">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="27418-192">**Роли ресурсов проекта для всех компаний (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="27418-192">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="27418-193">No</span><span class="sxs-lookup"><span data-stu-id="27418-193">No</span></span> | <span data-ttu-id="27418-194">Да</span><span class="sxs-lookup"><span data-stu-id="27418-194">Yes</span></span> | <span data-ttu-id="27418-195">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="27418-195">Common Data Service</span></span> | <span data-ttu-id="27418-196">No</span><span class="sxs-lookup"><span data-stu-id="27418-196">No</span></span> | <span data-ttu-id="27418-197">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="27418-197">N\A</span></span> |
| <span data-ttu-id="27418-198">**Юридические лица (cdm\_companies)**</span><span class="sxs-lookup"><span data-stu-id="27418-198">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="27418-199">No</span><span class="sxs-lookup"><span data-stu-id="27418-199">No</span></span> | <span data-ttu-id="27418-200">Да</span><span class="sxs-lookup"><span data-stu-id="27418-200">Yes</span></span> | <span data-ttu-id="27418-201">Приложения Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="27418-201">Finance and Operations apps</span></span> | <span data-ttu-id="27418-202">No</span><span class="sxs-lookup"><span data-stu-id="27418-202">No</span></span> | <span data-ttu-id="27418-203">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="27418-203">N\A</span></span> |
| <span data-ttu-id="27418-204">**Фактические данные интеграции Project Operations (msdyn\_actuals)**</span><span class="sxs-lookup"><span data-stu-id="27418-204">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="27418-205">No</span><span class="sxs-lookup"><span data-stu-id="27418-205">No</span></span> | <span data-ttu-id="27418-206">No</span><span class="sxs-lookup"><span data-stu-id="27418-206">No</span></span> | <span data-ttu-id="27418-207">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="27418-207">N\A</span></span> | <span data-ttu-id="27418-208">Да</span><span class="sxs-lookup"><span data-stu-id="27418-208">Yes</span></span> | <span data-ttu-id="27418-209">No</span><span class="sxs-lookup"><span data-stu-id="27418-209">No</span></span> |
| <span data-ttu-id="27418-210">**Строки контракта по проекту (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="27418-210">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="27418-211">No</span><span class="sxs-lookup"><span data-stu-id="27418-211">No</span></span> | <span data-ttu-id="27418-212">No</span><span class="sxs-lookup"><span data-stu-id="27418-212">No</span></span> | <span data-ttu-id="27418-213">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="27418-213">N\A</span></span> | <span data-ttu-id="27418-214">No</span><span class="sxs-lookup"><span data-stu-id="27418-214">No</span></span> | <span data-ttu-id="27418-215">No</span><span class="sxs-lookup"><span data-stu-id="27418-215">No</span></span> |
| <span data-ttu-id="27418-216">**Сущность интеграции для отношений транзакций проекта (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="27418-216">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="27418-217">No</span><span class="sxs-lookup"><span data-stu-id="27418-217">No</span></span> | <span data-ttu-id="27418-218">No</span><span class="sxs-lookup"><span data-stu-id="27418-218">No</span></span> | <span data-ttu-id="27418-219">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="27418-219">N\A</span></span> | <span data-ttu-id="27418-220">No</span><span class="sxs-lookup"><span data-stu-id="27418-220">No</span></span> | <span data-ttu-id="27418-221">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="27418-221">N\A</span></span> |
| <span data-ttu-id="27418-222">**Основные этапы строки контракта интеграции Project Operations (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="27418-222">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="27418-223">No</span><span class="sxs-lookup"><span data-stu-id="27418-223">No</span></span> | <span data-ttu-id="27418-224">No</span><span class="sxs-lookup"><span data-stu-id="27418-224">No</span></span> | <span data-ttu-id="27418-225">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="27418-225">N\A</span></span> | <span data-ttu-id="27418-226">No</span><span class="sxs-lookup"><span data-stu-id="27418-226">No</span></span> | <span data-ttu-id="27418-227">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="27418-227">N\A</span></span> |
| <span data-ttu-id="27418-228">**Сущность интеграции Project Operations для оценки расходов (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="27418-228">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="27418-229">No</span><span class="sxs-lookup"><span data-stu-id="27418-229">No</span></span> | <span data-ttu-id="27418-230">No</span><span class="sxs-lookup"><span data-stu-id="27418-230">No</span></span> | <span data-ttu-id="27418-231">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="27418-231">N\A</span></span> | <span data-ttu-id="27418-232">No</span><span class="sxs-lookup"><span data-stu-id="27418-232">No</span></span> | <span data-ttu-id="27418-233">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="27418-233">N\A</span></span> |
| <span data-ttu-id="27418-234">**Сущность интеграции Project Operations для оценки часов (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="27418-234">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="27418-235">No</span><span class="sxs-lookup"><span data-stu-id="27418-235">No</span></span> | <span data-ttu-id="27418-236">No</span><span class="sxs-lookup"><span data-stu-id="27418-236">No</span></span> | <span data-ttu-id="27418-237">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="27418-237">N\A</span></span> | <span data-ttu-id="27418-238">No</span><span class="sxs-lookup"><span data-stu-id="27418-238">No</span></span> | <span data-ttu-id="27418-239">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="27418-239">N\A</span></span> |
| <span data-ttu-id="27418-240">**Сущность экспорта расходов проекта интеграции Project Operations (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="27418-240">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="27418-241">Да</span><span class="sxs-lookup"><span data-stu-id="27418-241">Yes</span></span> | <span data-ttu-id="27418-242">No</span><span class="sxs-lookup"><span data-stu-id="27418-242">No</span></span> | <span data-ttu-id="27418-243">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="27418-243">N\A</span></span> | <span data-ttu-id="27418-244">No</span><span class="sxs-lookup"><span data-stu-id="27418-244">No</span></span> | <span data-ttu-id="27418-245">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="27418-245">N\A</span></span> |
| <span data-ttu-id="27418-246">**Сущность интеграции Project Operations для оценки часов (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="27418-246">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="27418-247">Да</span><span class="sxs-lookup"><span data-stu-id="27418-247">Yes</span></span> | <span data-ttu-id="27418-248">No</span><span class="sxs-lookup"><span data-stu-id="27418-248">No</span></span> | <span data-ttu-id="27418-249">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="27418-249">N\A</span></span> | <span data-ttu-id="27418-250">No</span><span class="sxs-lookup"><span data-stu-id="27418-250">No</span></span> | <span data-ttu-id="27418-251">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="27418-251">N\A</span></span> |

4. <span data-ttu-id="27418-252">Чтобы обновить сущность, выберите имя сопоставления, затем выберите **Обновить сущности**.</span><span class="sxs-lookup"><span data-stu-id="27418-252">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 
5. <span data-ttu-id="27418-253">После завершения обновления продолжите запуск сопоставления.</span><span class="sxs-lookup"><span data-stu-id="27418-253">Proceed with running the map after the refresh is complete.</span></span>

![Обновление сопоставления](./media/20RefreshMapping.png)

<span data-ttu-id="27418-255">Прежде чем включить следующее сопоставление, убедитесь, что сопоставление в таблице находится в состоянии **Запущено**.</span><span class="sxs-lookup"><span data-stu-id="27418-255">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="27418-256">Запуск сопоставлений с большим количеством предварительных условий может занять некоторое время.</span><span class="sxs-lookup"><span data-stu-id="27418-256">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="27418-257">Чтобы запустить сопоставление с предварительными условиями, включите переключатель **Показать связанные сопоставления сущностей**.</span><span class="sxs-lookup"><span data-stu-id="27418-257">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="27418-258">Если в таблице указано, что **Начальная синхронизация необходимых условий** имеет значение **Нет**, убедитесь, что флаг **Начальная синхронизация** имеет значение **Откл.** на всех сопоставления необходимых условий перед их запуском.</span><span class="sxs-lookup"><span data-stu-id="27418-258">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Запуск сопоставления](./media/21RunMap.png)

6. <span data-ttu-id="27418-260">Убедитесь, что все связанные с проектом сопоставления находятся в рабочем состоянии.</span><span class="sxs-lookup"><span data-stu-id="27418-260">Validate all project related maps are in the running state.</span></span>

![Все сопоставления работают](./media/22AllMapsRunning.png)

<span data-ttu-id="27418-262">Теперь ваша среда Project Operations подготовлена и настроена.</span><span class="sxs-lookup"><span data-stu-id="27418-262">Your Project Operations environment is now provisioned and configured.</span></span>
