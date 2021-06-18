---
title: Обновите Project Operations в вашей среде Finance
description: В этой теме содержится информация о том, как обновить Project Operations в вашей среде Dynamics 365 Finance.
author: ruhercul
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d85a180aa094a048b4422605b25151d10785f67d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011072"
---
# <a name="update-project-operations-in-your-finance-environment"></a><span data-ttu-id="29b2e-103">Обновите Project Operations в вашей среде Finance</span><span class="sxs-lookup"><span data-stu-id="29b2e-103">Update Project Operations in your Finance environment</span></span>

<span data-ttu-id="29b2e-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/без запасов_</span><span class="sxs-lookup"><span data-stu-id="29b2e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="29b2e-105">В этой теме содержится информация о том, как обновить Dynamics 365 Project Operations в вашей среде Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="29b2e-105">This topic provides information about how to update Dynamics 365 Project Operations in your Dynamics 365 Finance environment.</span></span> <span data-ttu-id="29b2e-106">Для обновления Project Operations до Обновление 5 (UR5) требуются три процедуры:</span><span class="sxs-lookup"><span data-stu-id="29b2e-106">There are three procedures that are required to update Project Operations to Update 5 (UR5):</span></span>

- [<span data-ttu-id="29b2e-107">Импортируйте пакет в предварительный проект</span><span class="sxs-lookup"><span data-stu-id="29b2e-107">Import the package into your preview project</span></span>](#import)
- [<span data-ttu-id="29b2e-108">Примените обновление</span><span class="sxs-lookup"><span data-stu-id="29b2e-108">Apply the update</span></span>](#apply)
- [<span data-ttu-id="29b2e-109">Обновите вашу среду Dataverse</span><span class="sxs-lookup"><span data-stu-id="29b2e-109">Update your Dataverse environment</span></span>](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a><span data-ttu-id="29b2e-110">Импортируйте пакет в ваш проект LCS</span><span class="sxs-lookup"><span data-stu-id="29b2e-110">Import the package into your LCS project</span></span>

1. <span data-ttu-id="29b2e-111">Войдите в [Lifecycle Services (LCS)](https://lcs.dynamics.com/) как владелец проекта или менеджер среды.</span><span class="sxs-lookup"><span data-stu-id="29b2e-111">Sign in to [Lifecycle Services (LCS)](https://lcs.dynamics.com/) as a Project Owner or Environment manager.</span></span>
2. <span data-ttu-id="29b2e-112">Из списка проектов выберите ваш проект LCS.</span><span class="sxs-lookup"><span data-stu-id="29b2e-112">From the list of projects, select your LCS project.</span></span>
3. <span data-ttu-id="29b2e-113">На странице **Проект** в группе **Среды** откройте среду, которую вы хотите обновить.</span><span class="sxs-lookup"><span data-stu-id="29b2e-113">On the **Project** page, in the **Environments** group, open the environment that you want to update.</span></span>
4. <span data-ttu-id="29b2e-114">Убедитесь, что среда работает.</span><span class="sxs-lookup"><span data-stu-id="29b2e-114">Verify that the environment is running.</span></span> <span data-ttu-id="29b2e-115">Если она не запущена, запустите среду.</span><span class="sxs-lookup"><span data-stu-id="29b2e-115">If it isn't started, start the environment.</span></span>
5. <span data-ttu-id="29b2e-116">В разделе **Новый выпуск** под **Доступные обновления**, выберите **Просмотр сведений об обновлении** для 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="29b2e-116">In the **New release** section under **Available updates**, select **View update** for 10.0.15.</span></span>

![Кнопка "Просмотр сведений об обновлении"](media/view-update.png)

6. <span data-ttu-id="29b2e-118">На странице **Двоичные обновления** выберите **Сохранить пакет**.</span><span class="sxs-lookup"><span data-stu-id="29b2e-118">On the **Binary updates** page, select **Save package**.</span></span>
7. <span data-ttu-id="29b2e-119">На странице **Просмотреть и сохранить обновления** выберите **Сохранить пакет**.</span><span class="sxs-lookup"><span data-stu-id="29b2e-119">On the **Review and save updates** page, select **Save package**.</span></span>
8. <span data-ttu-id="29b2e-120">В открывшейся области **Сохранить пакет в библиотеке активов** введите имя пакета и затем выберите **Сохранить пакет**.</span><span class="sxs-lookup"><span data-stu-id="29b2e-120">On the **Save package to asset library** pane that opens, enter the package name and then select **Save package**.</span></span>
9. <span data-ttu-id="29b2e-121">Когда LCS закончит сохранение пакета, кнопка **Готово** будет включена.</span><span class="sxs-lookup"><span data-stu-id="29b2e-121">When LCS has finished saving the package, the **Done** button is enabled.</span></span> <span data-ttu-id="29b2e-122">Нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="29b2e-122">Select **Done**.</span></span> <span data-ttu-id="29b2e-123">LCS проверит пакет.</span><span class="sxs-lookup"><span data-stu-id="29b2e-123">LCS will verify the package.</span></span> <span data-ttu-id="29b2e-124">Проверка может занять от нескольких минут до одного часа.</span><span class="sxs-lookup"><span data-stu-id="29b2e-124">Verification can take a few minutes or up to one hour.</span></span>


## <a name="apply-the-package-update"></a><a name="apply"></a><span data-ttu-id="29b2e-125">Примените обновление пакета</span><span class="sxs-lookup"><span data-stu-id="29b2e-125">Apply the package update</span></span>

1. <span data-ttu-id="29b2e-126">В LCS на страница **Сведения о среде**, выберите **Обслуживание** > **Применить обновления**.</span><span class="sxs-lookup"><span data-stu-id="29b2e-126">In LCS, on the **Environment details** page, select **Maintain** > **Apply Updates**.</span></span>
2. <span data-ttu-id="29b2e-127">В списке выберите пакет, который вы сохранили ранее, а затем выберите **Применить**.</span><span class="sxs-lookup"><span data-stu-id="29b2e-127">From the list, select the package that you saved earlier, and then select **Apply**.</span></span>
3. <span data-ttu-id="29b2e-128">Выбрать **Да**, чтобы подтвердить, что вы хотите развернуть пакет.</span><span class="sxs-lookup"><span data-stu-id="29b2e-128">Select **Yes** to confirm that you want to deploy the package.</span></span>

![Диалоговое окно подтверждения развертывания пакета](media/confirm-package-deployment.png)

4. <span data-ttu-id="29b2e-130">Выбрать **Да**, чтобы подтвердить, что вы хотите обновить приложение.</span><span class="sxs-lookup"><span data-stu-id="29b2e-130">Select **Yes** to confirm that you want to update the application.</span></span>

![Диалоговое окно подтверждения обновления приложения](media/confirm-application-update.png)

<span data-ttu-id="29b2e-132">Начнется развертывание и обновление приложения.</span><span class="sxs-lookup"><span data-stu-id="29b2e-132">The deployment and application update will start.</span></span> 

<span data-ttu-id="29b2e-133">На странице **Сведения о среде**, в правом верхнем углу, статус среды обновится до **Обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="29b2e-133">On the **Environment details** page, in the top-right corner, the environment status will update to **Servicing**.</span></span> <span data-ttu-id="29b2e-134">Примерно через два часа обновление будет завершено.</span><span class="sxs-lookup"><span data-stu-id="29b2e-134">In approximately two hours, the update will be complete.</span></span> <span data-ttu-id="29b2e-135">Информация о выпуске приложения обновится до **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** и статус среды обновится до **Развернута**.</span><span class="sxs-lookup"><span data-stu-id="29b2e-135">The application release information will update to **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** and the environment status will update to **Deployed**.</span></span>


## <a name="update-your-dataverse-environment"></a><a name="update"></a><span data-ttu-id="29b2e-136">Обновите вашу среду Dataverse</span><span class="sxs-lookup"><span data-stu-id="29b2e-136">Update your Dataverse environment</span></span>

1. <span data-ttu-id="29b2e-137">Войдите в в [центр администрирования Power Platform](https://admin.powerplatform.com/).</span><span class="sxs-lookup"><span data-stu-id="29b2e-137">Sign in to the [Power Platform admin center](https://admin.powerplatform.com/).</span></span>
2. <span data-ttu-id="29b2e-138">В списке найдите и откройте среду, которую вы использовали для установки Project Operations.</span><span class="sxs-lookup"><span data-stu-id="29b2e-138">In the list, find and open the environment that you used to install Project Operations.</span></span>
3. <span data-ttu-id="29b2e-139">На страница **Среды**, выберите **Ресурс** > **Приложения Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="29b2e-139">On the **Environments** page, select **Resource** > **Dynamics 365 apps**.</span></span>
4. <span data-ttu-id="29b2e-140">В списке найдите **Microsoft Dynamics 365 Project Operations**, а в столбец **Состояние** выберите **Доступно обновление**.</span><span class="sxs-lookup"><span data-stu-id="29b2e-140">In the list, locate **Microsoft Dynamics 365 Project Operations**, and in the **Status** column, select **Update Available**.</span></span>
5. <span data-ttu-id="29b2e-141">Выберите флажок **Я согласен с условиями обслуживания**, а затем выберите **Обновить**.</span><span class="sxs-lookup"><span data-stu-id="29b2e-141">Select the **I agree to the terms of service** check box, and then select **Update**.</span></span> <span data-ttu-id="29b2e-142">Будет установлена последняя версия решения.</span><span class="sxs-lookup"><span data-stu-id="29b2e-142">The latest version of the solution will be installed.</span></span>

<span data-ttu-id="29b2e-143">После завершения установки у вас будет установлена версия 4.5.0.134.</span><span class="sxs-lookup"><span data-stu-id="29b2e-143">After the installation is complete, you'll have version 4.5.0.134 installed.</span></span>

## <a name="configure-new-features"></a><span data-ttu-id="29b2e-144">Настройка новых функций</span><span class="sxs-lookup"><span data-stu-id="29b2e-144">Configure new features</span></span>

### <a name="enable-dual-write-mapping"></a><span data-ttu-id="29b2e-145">Включить сопоставление с двойной записью</span><span class="sxs-lookup"><span data-stu-id="29b2e-145">Enable dual-write mapping</span></span>

<span data-ttu-id="29b2e-146">После завершения обновления сред Finance и Dataverse, вы можете включить необходимые сопоставления с двойной записью.</span><span class="sxs-lookup"><span data-stu-id="29b2e-146">After you complete the update on the Finance and Dataverse environments, you can enable the required dual-write mappings.</span></span> <span data-ttu-id="29b2e-147">Выполните следующие процедуры, чтобы включить сопоставления с двойной записью.</span><span class="sxs-lookup"><span data-stu-id="29b2e-147">Complete the following procedures to enable dual-write mappings.</span></span>

- [<span data-ttu-id="29b2e-148">Обновление настроек безопасности в среде Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="29b2e-148">Update security settings on Customer Engagement environment</span></span>](#security)
- [<span data-ttu-id="29b2e-149">Обновить информационные объекты</span><span class="sxs-lookup"><span data-stu-id="29b2e-149">Refresh data entities</span></span>](#refresh)
- [<span data-ttu-id="29b2e-150">Обновите и запустите сопоставления с двойной записью</span><span class="sxs-lookup"><span data-stu-id="29b2e-150">Update and run the dual-write mappings</span></span>](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a><span data-ttu-id="29b2e-151">Обновление настроек безопасности в среде Dataverse</span><span class="sxs-lookup"><span data-stu-id="29b2e-151">Update security settings on the Dataverse environment</span></span>

<span data-ttu-id="29b2e-152">Следующие обновления привилегий безопасности для объектов требуются как часть обновления UR5.</span><span class="sxs-lookup"><span data-stu-id="29b2e-152">The following updates to the security privileges for entities are required as part of the update to UR5.</span></span>

1. <span data-ttu-id="29b2e-153">В вашей среде Dataverse перейдите в **Параметры**, а в группа **Система** выберите **Безопасность** .</span><span class="sxs-lookup"><span data-stu-id="29b2e-153">In your Dataverse environment, go to **Settings**, and in the **System** group, select **Security**.</span></span>

![Параметры среды Dataverse](media/Picture21.png)

2. <span data-ttu-id="29b2e-155">Выбор **ролей безопасности**.</span><span class="sxs-lookup"><span data-stu-id="29b2e-155">Select **Security Roles**.</span></span>
3. <span data-ttu-id="29b2e-156">В списке ролей выберите **пользователь приложения с двойной записью** и выберите вкладку **Настраиваемые объекты**.</span><span class="sxs-lookup"><span data-stu-id="29b2e-156">From the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span> 
4. <span data-ttu-id="29b2e-157">Убедитесь, что роль установлена на **Чтение** и разрешения **Добавить к** для:</span><span class="sxs-lookup"><span data-stu-id="29b2e-157">Verify that the role has **Read** and **Append To** permissions for:</span></span>

      - <span data-ttu-id="29b2e-158">**Тип обменного курса валют**</span><span class="sxs-lookup"><span data-stu-id="29b2e-158">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="29b2e-159">**План счетов**</span><span class="sxs-lookup"><span data-stu-id="29b2e-159">**Chart Of Accounts**</span></span> 
      - <span data-ttu-id="29b2e-160">**Финансовый календарь**</span><span class="sxs-lookup"><span data-stu-id="29b2e-160">**Fiscal Calendar**</span></span> 
      - <span data-ttu-id="29b2e-161">**Реестр**</span><span class="sxs-lookup"><span data-stu-id="29b2e-161">**Ledger**</span></span>

5. <span data-ttu-id="29b2e-162">После обновления роли безопасности перейдите к **Параметры** > **Безопасность** > **Рабочие группы**.</span><span class="sxs-lookup"><span data-stu-id="29b2e-162">After the security role is updated, go to **Settings** > **Security** > **Teams**.</span></span> <span data-ttu-id="29b2e-163">Убедитесь, что роль **пользователь приложения с двойной записью** была применена к рабочей группе.</span><span class="sxs-lookup"><span data-stu-id="29b2e-163">Verify that the **dual-write app user** role has been applied to the team.</span></span> 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a><span data-ttu-id="29b2e-164">Обновить информационные объекты из обновления</span><span class="sxs-lookup"><span data-stu-id="29b2e-164">Refresh data entities from the update</span></span>

1. <span data-ttu-id="29b2e-165">В вашей среде Finance откройте рабочая область **Управление данными**, а затем откройте страница **Параметры структуры**.</span><span class="sxs-lookup"><span data-stu-id="29b2e-165">In your Finance environment, open the **Data management** workspace, and then open the **Framework parameters** page.</span></span>
2. <span data-ttu-id="29b2e-166">На вкладка **Параметры объекта** выберите **Обновить список сущностей**.</span><span class="sxs-lookup"><span data-stu-id="29b2e-166">On the **Entity settings** tab, select **Refresh entity list**.</span></span>
3. <span data-ttu-id="29b2e-167">Выбрать **Закрыть**, чтобы подтвердить обновление объекта.</span><span class="sxs-lookup"><span data-stu-id="29b2e-167">Select **Close** to confirm the entity refresh.</span></span>

 > [!NOTE]
 > <span data-ttu-id="29b2e-168">Эта процедура займет от приблизительно 20 минут.</span><span class="sxs-lookup"><span data-stu-id="29b2e-168">This process will take approximately 20 minutes to complete.</span></span> <span data-ttu-id="29b2e-169">Вы получите уведомление, когда обновление будет завершено.</span><span class="sxs-lookup"><span data-stu-id="29b2e-169">You will be notified when the refresh is complete.</span></span>

### <a name="update-dual-write-mappings"></a><a name="run"></a><span data-ttu-id="29b2e-170">Обновить сопоставления с двойной записью</span><span class="sxs-lookup"><span data-stu-id="29b2e-170">Update dual-write mappings</span></span>

1. <span data-ttu-id="29b2e-171">В рабочая область **Управление данными** выберите **Двойная запись**.</span><span class="sxs-lookup"><span data-stu-id="29b2e-171">In the **Data management** workspace, select **Dual-write**.</span></span>
2. <span data-ttu-id="29b2e-172">Выбрать **Применить решения**, выберите оба решения в списке, а затем выберите **Применить**.</span><span class="sxs-lookup"><span data-stu-id="29b2e-172">Select **Apply solutions**, select both solutions in the list, and then select **Apply**.</span></span>
3. <span data-ttu-id="29b2e-173">На странице **Двойная запись** выберите следующие сопоставления таблиц, а затем выберите **Остановить**.</span><span class="sxs-lookup"><span data-stu-id="29b2e-173">On the **Dual-write** page, select the following table maps, and then select **Stop**.</span></span>

    - <span data-ttu-id="29b2e-174">**Фактические данные интеграции Project Operations (msdyn_actuals)**</span><span class="sxs-lookup"><span data-stu-id="29b2e-174">**Project Operations integration actuals (msdyn_actuals)**</span></span>
    - <span data-ttu-id="29b2e-175">**Категории расходов проекта интеграции Project Operations (msdyn_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="29b2e-175">**Project Operations integration project expense categories (msdyn_expensecategories)**</span></span>
    - <span data-ttu-id="29b2e-176">**Фактические данные интеграции Project Operations сущность экспорта расходов по проекту (msdyn_expenses)**</span><span class="sxs-lookup"><span data-stu-id="29b2e-176">**Project Operations integration actuals project expenses export entity (msdyn_expenses)**</span></span>

4. <span data-ttu-id="29b2e-177">На странице **Версия сопоставления таблиц** примените новую версию сопоставления к каждому из трех объектов.</span><span class="sxs-lookup"><span data-stu-id="29b2e-177">On the **Table map version** page, apply a new version of the map to each of the three entities.</span></span>
5. <span data-ttu-id="29b2e-178">На странице **Двойная запись** выберите выполнение, чтобы перезапустить сопоставления.</span><span class="sxs-lookup"><span data-stu-id="29b2e-178">On the **Dual-write** page, select run to restart the maps.</span></span>
6. <span data-ttu-id="29b2e-179">Из списка сопоставлений выберите сопоставление **Реестр (msdyn_ledgers)** со всеми обязательными компонентами и выберите флажок **Начальная синхронизация**.</span><span class="sxs-lookup"><span data-stu-id="29b2e-179">From the list of maps, select the **Ledger (msdyn_ledgers)** map with all prerequisites and select the **Initial sync** check box.</span></span> 
7. <span data-ttu-id="29b2e-180">В поле **Главная запись для начальной синхронизации** выберите **Приложения Finance and Operations**, а затем выберите **Выполнить**.</span><span class="sxs-lookup"><span data-stu-id="29b2e-180">In the **Master for initial sync** field, select **Finance and Operations apps** and then select **Run**.</span></span>
 
 ![Синхронизация сопоставления реестра](media/DW6.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]