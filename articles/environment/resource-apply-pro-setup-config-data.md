---
title: Настройка и применение данных конфигурации в Common Data Service для Project Operations
description: Эта тема предоставляет информацию о настройке и применении данных конфигурации в Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5e72b88a4dae1eb89859fdfd55f6d5e6ee5befcd
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083061"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service-for-project-operations"></a><span data-ttu-id="87ac2-103">Настройка и применение данных конфигурации в Common Data Service для Project Operations</span><span class="sxs-lookup"><span data-stu-id="87ac2-103">Set up and apply configuration data in the Common Data Service for Project Operations</span></span>

<span data-ttu-id="87ac2-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/без запасов_</span><span class="sxs-lookup"><span data-stu-id="87ac2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="87ac2-105">Установка данных настройки и конфигурации</span><span class="sxs-lookup"><span data-stu-id="87ac2-105">Install setup and configuration data</span></span>

1. <span data-ttu-id="87ac2-106">Загрузите, разблокируйте и разархивируйте [Пакет данных настройки и конфигурации](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span><span class="sxs-lookup"><span data-stu-id="87ac2-106">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="87ac2-107">Перейдите в распакованную папку и запустите исполняемый файл, *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="87ac2-107">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="87ac2-108">На странице 1 мастера настройки Common Data Service (CMT) выберите **Импортировать данные** , затем выберите **Продолжить**.</span><span class="sxs-lookup"><span data-stu-id="87ac2-108">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Миграция конфигурации](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="87ac2-110">На странице 2 мастера CMT выберите **Microsoft 365** как **Тип развертывания**.</span><span class="sxs-lookup"><span data-stu-id="87ac2-110">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="87ac2-111">Установите флажки **Показать список доступных организаций** и **Показать расширенный**.</span><span class="sxs-lookup"><span data-stu-id="87ac2-111">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="87ac2-112">Выберите регион своего клиента, введите свои учетные данные и выберите **Войти**.</span><span class="sxs-lookup"><span data-stu-id="87ac2-112">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Вход в конфигурацию](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="87ac2-114">На странице 3 из списка организаций в клиенте выберите организацию, в которую вы хотите импортировать демонстрационные данные, и выберите **Войти**.</span><span class="sxs-lookup"><span data-stu-id="87ac2-114">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="87ac2-115">На странице 4 выберите ZIP-файл *SampleSetupAndConfigData* из распакованной папки.</span><span class="sxs-lookup"><span data-stu-id="87ac2-115">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Выбор ZIP-файла](./media/3ZipFile.png)

![Выберите файл](./media/4SelectAFile.png)

9. <span data-ttu-id="87ac2-118">После выбора ZIP-файла выберите **Импортировать данные**.</span><span class="sxs-lookup"><span data-stu-id="87ac2-118">After the zip file is selected, select **Import Data**.</span></span>

![Импортировать данные](./media/5ImportData.png)

10. <span data-ttu-id="87ac2-120">Импорт будет выполняться примерно от двух до десяти минут в зависимости от скорости вашей сети.</span><span class="sxs-lookup"><span data-stu-id="87ac2-120">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="87ac2-121">После завершения импорта выйдите из мастера CMT.</span><span class="sxs-lookup"><span data-stu-id="87ac2-121">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="87ac2-122">Проверьте свою организацию на наличие данных по следующим 19 сущностям:</span><span class="sxs-lookup"><span data-stu-id="87ac2-122">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="87ac2-123">Валюта</span><span class="sxs-lookup"><span data-stu-id="87ac2-123">Currency</span></span>
  - <span data-ttu-id="87ac2-124">Подразделение</span><span class="sxs-lookup"><span data-stu-id="87ac2-124">Organizational Unit</span></span>
  - <span data-ttu-id="87ac2-125">Контактные сведения</span><span class="sxs-lookup"><span data-stu-id="87ac2-125">Contact</span></span>
  - <span data-ttu-id="87ac2-126">Налоговая группа</span><span class="sxs-lookup"><span data-stu-id="87ac2-126">Tax Group</span></span>
  - <span data-ttu-id="87ac2-127">Группа клиентов</span><span class="sxs-lookup"><span data-stu-id="87ac2-127">Customer Group</span></span>
  - <span data-ttu-id="87ac2-128">Единица</span><span class="sxs-lookup"><span data-stu-id="87ac2-128">Unit</span></span>
  - <span data-ttu-id="87ac2-129">Группа единиц измерения</span><span class="sxs-lookup"><span data-stu-id="87ac2-129">Unit Group</span></span>
  - <span data-ttu-id="87ac2-130">Прайс-лист</span><span class="sxs-lookup"><span data-stu-id="87ac2-130">Price List</span></span>
  - <span data-ttu-id="87ac2-131">Прайс-лист параметров проекта</span><span class="sxs-lookup"><span data-stu-id="87ac2-131">Project Parameter Price List</span></span>
  - <span data-ttu-id="87ac2-132">Периодичность выставления счетов</span><span class="sxs-lookup"><span data-stu-id="87ac2-132">Invoice Frequency</span></span>
  - <span data-ttu-id="87ac2-133">Категория резервируемого ресурса</span><span class="sxs-lookup"><span data-stu-id="87ac2-133">Bookable Resource Category</span></span>
  - <span data-ttu-id="87ac2-134">Категория проводки</span><span class="sxs-lookup"><span data-stu-id="87ac2-134">Transaction Category</span></span>
  - <span data-ttu-id="87ac2-135">Категория расходов</span><span class="sxs-lookup"><span data-stu-id="87ac2-135">Expense Category</span></span>
  - <span data-ttu-id="87ac2-136">Цена роли</span><span class="sxs-lookup"><span data-stu-id="87ac2-136">Role Price</span></span>
  - <span data-ttu-id="87ac2-137">Цена категории проводки</span><span class="sxs-lookup"><span data-stu-id="87ac2-137">Transaction Category Price</span></span>
  - <span data-ttu-id="87ac2-138">Характеристика</span><span class="sxs-lookup"><span data-stu-id="87ac2-138">Characteristic</span></span>
  - <span data-ttu-id="87ac2-139">Резервируемый ресурс</span><span class="sxs-lookup"><span data-stu-id="87ac2-139">Bookable Resource</span></span>
  - <span data-ttu-id="87ac2-140">Назначение категории резервируемого ресурса</span><span class="sxs-lookup"><span data-stu-id="87ac2-140">Bookable resource category Assn</span></span>
  - <span data-ttu-id="87ac2-141">Характеристика резервируемого ресурса</span><span class="sxs-lookup"><span data-stu-id="87ac2-141">Bookable Resource Characteristic</span></span>

![Завершите импорт](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="87ac2-143">Обновление конфигураций Project Operations</span><span class="sxs-lookup"><span data-stu-id="87ac2-143">Update Project Operations configurations</span></span>

1. <span data-ttu-id="87ac2-144">Перейдите в среду CE.</span><span class="sxs-lookup"><span data-stu-id="87ac2-144">Navigate to the CE environment.</span></span> <span data-ttu-id="87ac2-145">Вы можете найти ее, открыв [Центр администрирования Power Platform](https://admin.powerplatform.microsoft.com/environments), выбрав среду, затем выбрав **Открыть среду**.</span><span class="sxs-lookup"><span data-stu-id="87ac2-145">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Открыть среду](./media/7OpenEnvironment.png)

2. <span data-ttu-id="87ac2-147">Выберите **Проекты** > **Ресурсы** , затем выберите **Создать** , чтобы создать доступный для резервирования ресурс для вашего пользователя.</span><span class="sxs-lookup"><span data-stu-id="87ac2-147">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Резервируемые ресурсы](./media/8BookableResources.png)

3. <span data-ttu-id="87ac2-149">На вкладке **Общие** выберите своего администратора.</span><span class="sxs-lookup"><span data-stu-id="87ac2-149">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="87ac2-150">Убедитесь, что часовой пояс соответствует тому, в котором вы находитесь.</span><span class="sxs-lookup"><span data-stu-id="87ac2-150">Verify that the time zone matches the one you are in.</span></span> 

![Создание резервируемого ресурса](./media/9NewBookableResource.png)

4. <span data-ttu-id="87ac2-152">На вкладке **Планирование** в поле **Компания** выберите компанию **USPM** , затем выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="87ac2-152">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Вкладка планирования](./media/10SchedulingTab.png)

5. <span data-ttu-id="87ac2-154">Перейдите на вкладку **Рабочие часы**.</span><span class="sxs-lookup"><span data-stu-id="87ac2-154">Select the **Work hours** tab.</span></span>  

![Рабочие часы](./media/11WorkHours.png)

6. <span data-ttu-id="87ac2-156">Дважды щелкните любое значение в календаре и выберите **Изменить** > **Все события этой серии**.</span><span class="sxs-lookup"><span data-stu-id="87ac2-156">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Рабочий календарь](./media/12WorkCalendar.png)

7. <span data-ttu-id="87ac2-158">Измените рабочие часы на восьмичасовой (8) рабочий день, отметьте выходные как нерабочие дни и убедитесь, что часовой пояс соответствует вашему.</span><span class="sxs-lookup"><span data-stu-id="87ac2-158">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="87ac2-159">Выберите **Сохранить и закрыть**.</span><span class="sxs-lookup"><span data-stu-id="87ac2-159">Select **Save and close**.</span></span>

![Обновление календаря](./media/13UpdateCalendar.png)

9. <span data-ttu-id="87ac2-161">Перейдите в раздел **Параметры** > **Шаблоны календаря** и выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="87ac2-161">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Шаблоны календарей](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="87ac2-163">Введите имя, выберите созданный вами шаблон ресурса, затем выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="87ac2-163">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Сохранение шаблона календаря](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="87ac2-165">Выберите **Параметры** и дважды щелкните запись.</span><span class="sxs-lookup"><span data-stu-id="87ac2-165">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Параметры проекта](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="87ac2-167">Обновите следующие поля:</span><span class="sxs-lookup"><span data-stu-id="87ac2-167">Update the following fields:</span></span>

 - <span data-ttu-id="87ac2-168">**Компания по умолчанию** : USPM</span><span class="sxs-lookup"><span data-stu-id="87ac2-168">**Default company** : USPM</span></span>
 - <span data-ttu-id="87ac2-169">**Подразделение по умолчанию** : Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="87ac2-169">**Default Organizational Unit** : Contoso Robotics Global</span></span>
 - <span data-ttu-id="87ac2-170">**Частота выставления счетов** : седьмой и последний день</span><span class="sxs-lookup"><span data-stu-id="87ac2-170">**Invoice Frequency** : Seventh and Last day</span></span>
 - <span data-ttu-id="87ac2-171">**Шаблон рабочего времени** : измените на созданный вами шаблон.</span><span class="sxs-lookup"><span data-stu-id="87ac2-171">**Work hour template** : Change to the template you created.</span></span>

13. <span data-ttu-id="87ac2-172">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="87ac2-172">Select **Save**.</span></span> 

![Обновление параметров проекта](./media/17UpdatedProjectParameters.png)
