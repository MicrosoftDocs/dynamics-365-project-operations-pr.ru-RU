---
title: Настройка и применение демонстрационных данных в Common Data Service
description: Эта тема предоставляет информацию о настройке и применении данных конфигурации в Project Operations.
author: sigitac
ms.date: 05/10/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2ea00df6112fb69b61f1889463424fdfee79aec9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001307"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a><span data-ttu-id="7b94d-103">Настройка и применение демонстрационных данных в Common Data Service</span><span class="sxs-lookup"><span data-stu-id="7b94d-103">Set up and apply configuration data in the Common Data Service</span></span> 

<span data-ttu-id="7b94d-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/без запасов_</span><span class="sxs-lookup"><span data-stu-id="7b94d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="7b94d-105">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="7b94d-105">Prerequisites</span></span>

<span data-ttu-id="7b94d-106">Прежде чем вы начнете настраивать данные в Common Data Service (CDS), должны быть выполнены следующие предварительные условия:</span><span class="sxs-lookup"><span data-stu-id="7b94d-106">Before you begin to configure data in the Common Data Service (CDS), the following prerequisites must be met:</span></span>

1.  <span data-ttu-id="7b94d-107">Подготовьте среду CDS и среду Dynamics 365 Finance для Project Operations.</span><span class="sxs-lookup"><span data-stu-id="7b94d-107">Provision a CDS environment and a Dynamics 365 Finance environment for Project Operations.</span></span>
2.  <span data-ttu-id="7b94d-108">Информация о юридических лицах от Dynamics 365 Finance является общей в среде CDS.</span><span class="sxs-lookup"><span data-stu-id="7b94d-108">Legal entity information from Dynamics 365 Finance is shared to the CDS environment.</span></span> <span data-ttu-id="7b94d-109">Это означает, что сущность **Компания** в CDS имеет следующие записи компаний:</span><span class="sxs-lookup"><span data-stu-id="7b94d-109">This means that the **Company** entity in CDS has the following company records:</span></span>
  - <span data-ttu-id="7b94d-110">THPM</span><span class="sxs-lookup"><span data-stu-id="7b94d-110">THPM</span></span>
  - <span data-ttu-id="7b94d-111">USPM</span><span class="sxs-lookup"><span data-stu-id="7b94d-111">USPM</span></span>
  - <span data-ttu-id="7b94d-112">GBPM</span><span class="sxs-lookup"><span data-stu-id="7b94d-112">GBPM</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="7b94d-113">Установка данных настройки и конфигурации</span><span class="sxs-lookup"><span data-stu-id="7b94d-113">Install setup and configuration data</span></span>

1. <span data-ttu-id="7b94d-114">Загрузите, разблокируйте и разархивируйте [Пакет данных настройки и конфигурации](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip).</span><span class="sxs-lookup"><span data-stu-id="7b94d-114">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip).</span></span>
2. <span data-ttu-id="7b94d-115">Перейдите в распакованную папку и запустите исполняемый файл, *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="7b94d-115">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="7b94d-116">На странице 1 мастера настройки Common Data Service (CMT) выберите **Импортировать данные**, затем выберите **Продолжить**.</span><span class="sxs-lookup"><span data-stu-id="7b94d-116">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Миграция конфигурации](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="7b94d-118">На странице 2 мастера CMT выберите **Microsoft 365** как **Тип развертывания**.</span><span class="sxs-lookup"><span data-stu-id="7b94d-118">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="7b94d-119">Установите флажки **Показать список доступных организаций** и **Показать расширенный**.</span><span class="sxs-lookup"><span data-stu-id="7b94d-119">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="7b94d-120">Выберите регион своего клиента, введите свои учетные данные и выберите **Войти**.</span><span class="sxs-lookup"><span data-stu-id="7b94d-120">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Вход в конфигурацию](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="7b94d-122">На странице 3 из списка организаций в клиенте выберите организацию, в которую вы хотите импортировать демонстрационные данные, и выберите **Войти**.</span><span class="sxs-lookup"><span data-stu-id="7b94d-122">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="7b94d-123">На странице 4 выберите ZIP-файл *SampleSetupAndConfigData* из распакованной папки.</span><span class="sxs-lookup"><span data-stu-id="7b94d-123">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Выбор ZIP-файла](./media/3ZipFile.png)

![Выберите файл](./media/4SelectAFile.png)

9. <span data-ttu-id="7b94d-126">После выбора ZIP-файла выберите **Импортировать данные**.</span><span class="sxs-lookup"><span data-stu-id="7b94d-126">After the zip file is selected, select **Import Data**.</span></span>

![Импортировать данные](./media/5ImportData.png)

10. <span data-ttu-id="7b94d-128">Импорт будет выполняться примерно от двух до десяти минут в зависимости от скорости вашей сети.</span><span class="sxs-lookup"><span data-stu-id="7b94d-128">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="7b94d-129">После завершения импорта выйдите из мастера CMT.</span><span class="sxs-lookup"><span data-stu-id="7b94d-129">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="7b94d-130">Проверьте свою организацию на наличие данных по следующим 26 сущностям:</span><span class="sxs-lookup"><span data-stu-id="7b94d-130">Check your organization for data in the following 26 entities:</span></span>

  - <span data-ttu-id="7b94d-131">Валюта</span><span class="sxs-lookup"><span data-stu-id="7b94d-131">Currency</span></span>
  - <span data-ttu-id="7b94d-132">План счетов</span><span class="sxs-lookup"><span data-stu-id="7b94d-132">Chart of Accounts</span></span>
  - <span data-ttu-id="7b94d-133">Финансовый календарь</span><span class="sxs-lookup"><span data-stu-id="7b94d-133">Fiscal Calendar</span></span>
  - <span data-ttu-id="7b94d-134">Типы валютных курсов</span><span class="sxs-lookup"><span data-stu-id="7b94d-134">Currency Exchange Rate Types</span></span>
  - <span data-ttu-id="7b94d-135">День оплаты</span><span class="sxs-lookup"><span data-stu-id="7b94d-135">Payment Day</span></span>
  - <span data-ttu-id="7b94d-136">Расписание оплаты</span><span class="sxs-lookup"><span data-stu-id="7b94d-136">Payment Schedule</span></span>
  - <span data-ttu-id="7b94d-137">Условия оплаты</span><span class="sxs-lookup"><span data-stu-id="7b94d-137">Payment Term</span></span>
  - <span data-ttu-id="7b94d-138">Подразделение</span><span class="sxs-lookup"><span data-stu-id="7b94d-138">Organizational Unit</span></span>
  - <span data-ttu-id="7b94d-139">Контакт</span><span class="sxs-lookup"><span data-stu-id="7b94d-139">Contact</span></span>
  - <span data-ttu-id="7b94d-140">Налоговая группа</span><span class="sxs-lookup"><span data-stu-id="7b94d-140">Tax Group</span></span>
  - <span data-ttu-id="7b94d-141">Группа клиентов</span><span class="sxs-lookup"><span data-stu-id="7b94d-141">Customer Group</span></span>
  - <span data-ttu-id="7b94d-142">Группа поставщиков</span><span class="sxs-lookup"><span data-stu-id="7b94d-142">Vendor Group</span></span>
  - <span data-ttu-id="7b94d-143">Единица</span><span class="sxs-lookup"><span data-stu-id="7b94d-143">Unit</span></span>
  - <span data-ttu-id="7b94d-144">Группа единиц измерения</span><span class="sxs-lookup"><span data-stu-id="7b94d-144">Unit Group</span></span>
  - <span data-ttu-id="7b94d-145">Прайс-лист</span><span class="sxs-lookup"><span data-stu-id="7b94d-145">Price List</span></span>
  - <span data-ttu-id="7b94d-146">Прайс-лист параметров проекта</span><span class="sxs-lookup"><span data-stu-id="7b94d-146">Project Parameter Price List</span></span>
  - <span data-ttu-id="7b94d-147">Периодичность выставления счетов</span><span class="sxs-lookup"><span data-stu-id="7b94d-147">Invoice Frequency</span></span>
  - <span data-ttu-id="7b94d-148">Категория резервируемого ресурса</span><span class="sxs-lookup"><span data-stu-id="7b94d-148">Bookable Resource Category</span></span>
  - <span data-ttu-id="7b94d-149">Категория проводки</span><span class="sxs-lookup"><span data-stu-id="7b94d-149">Transaction Category</span></span>
  - <span data-ttu-id="7b94d-150">Категория расходов</span><span class="sxs-lookup"><span data-stu-id="7b94d-150">Expense Category</span></span>
  - <span data-ttu-id="7b94d-151">Цена роли</span><span class="sxs-lookup"><span data-stu-id="7b94d-151">Role Price</span></span>
  - <span data-ttu-id="7b94d-152">Цена категории проводки</span><span class="sxs-lookup"><span data-stu-id="7b94d-152">Transaction Category Price</span></span>
  - <span data-ttu-id="7b94d-153">Характеристика</span><span class="sxs-lookup"><span data-stu-id="7b94d-153">Characteristic</span></span>
  - <span data-ttu-id="7b94d-154">Резервируемый ресурс</span><span class="sxs-lookup"><span data-stu-id="7b94d-154">Bookable Resource</span></span>
  - <span data-ttu-id="7b94d-155">Назначение категории резервируемого ресурса</span><span class="sxs-lookup"><span data-stu-id="7b94d-155">Bookable resource category Assn</span></span>
  - <span data-ttu-id="7b94d-156">Характеристика резервируемого ресурса</span><span class="sxs-lookup"><span data-stu-id="7b94d-156">Bookable Resource Characteristic</span></span>

![Завершите импорт](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="7b94d-158">Обновление конфигураций Project Operations</span><span class="sxs-lookup"><span data-stu-id="7b94d-158">Update Project Operations configurations</span></span>

1. <span data-ttu-id="7b94d-159">Перейдите в среду CE.</span><span class="sxs-lookup"><span data-stu-id="7b94d-159">Navigate to the CE environment.</span></span> <span data-ttu-id="7b94d-160">Вы можете найти ее, открыв [Центр администрирования Power Platform](https://admin.powerplatform.microsoft.com/environments), выбрав среду, затем выбрав **Открыть среду**.</span><span class="sxs-lookup"><span data-stu-id="7b94d-160">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Открыть среду](./media/7OpenEnvironment.png)

2. <span data-ttu-id="7b94d-162">Выберите **Проекты** > **Ресурсы**, затем выберите **Создать**, чтобы создать доступный для резервирования ресурс для вашего пользователя.</span><span class="sxs-lookup"><span data-stu-id="7b94d-162">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Резервируемые ресурсы](./media/8BookableResources.png)

3. <span data-ttu-id="7b94d-164">На вкладке **Общие** выберите своего администратора.</span><span class="sxs-lookup"><span data-stu-id="7b94d-164">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="7b94d-165">Убедитесь, что часовой пояс соответствует тому, в котором вы находитесь.</span><span class="sxs-lookup"><span data-stu-id="7b94d-165">Verify that the time zone matches the one you are in.</span></span> 

![Создание резервируемого ресурса](./media/9NewBookableResource.png)

4. <span data-ttu-id="7b94d-167">На вкладке **Планирование** в поле **Компания** выберите компанию **USPM**, затем выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="7b94d-167">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Вкладка планирования](./media/10SchedulingTab.png)

5. <span data-ttu-id="7b94d-169">Перейдите на вкладку **Рабочие часы**.</span><span class="sxs-lookup"><span data-stu-id="7b94d-169">Select the **Work hours** tab.</span></span>  

![Рабочие часы](./media/11WorkHours.png)

6. <span data-ttu-id="7b94d-171">Дважды щелкните любое значение в календаре и выберите **Изменить** > **Все события этой серии**.</span><span class="sxs-lookup"><span data-stu-id="7b94d-171">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Рабочий календарь](./media/12WorkCalendar.png)

7. <span data-ttu-id="7b94d-173">Измените рабочие часы на восьмичасовой (8) рабочий день, отметьте выходные как нерабочие дни и убедитесь, что часовой пояс соответствует вашему.</span><span class="sxs-lookup"><span data-stu-id="7b94d-173">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="7b94d-174">Выберите **Сохранить и закрыть**.</span><span class="sxs-lookup"><span data-stu-id="7b94d-174">Select **Save and close**.</span></span>

![Обновление календаря](./media/13UpdateCalendar.png)

9. <span data-ttu-id="7b94d-176">Перейдите в раздел **Параметры** > **Шаблоны календаря** и выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="7b94d-176">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Шаблоны календарей](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="7b94d-178">Введите имя, выберите созданный вами шаблон ресурса, затем выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="7b94d-178">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Сохранение шаблона календаря](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="7b94d-180">Выберите **Параметры** и дважды щелкните запись.</span><span class="sxs-lookup"><span data-stu-id="7b94d-180">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Параметры проекта](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="7b94d-182">Обновите следующие поля:</span><span class="sxs-lookup"><span data-stu-id="7b94d-182">Update the following fields:</span></span>

 - <span data-ttu-id="7b94d-183">**Компания по умолчанию**: USPM</span><span class="sxs-lookup"><span data-stu-id="7b94d-183">**Default company**: USPM</span></span>
 - <span data-ttu-id="7b94d-184">**Подразделение по умолчанию**: Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="7b94d-184">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="7b94d-185">**Частота выставления счетов**: седьмой и последний день</span><span class="sxs-lookup"><span data-stu-id="7b94d-185">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="7b94d-186">**Шаблон рабочего времени**: измените на созданный вами шаблон.</span><span class="sxs-lookup"><span data-stu-id="7b94d-186">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="7b94d-187">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="7b94d-187">Select **Save**.</span></span> 

![Обновление параметров проекта](./media/17UpdatedProjectParameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
