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
ms.openlocfilehash: d99ab4c7b2ebf6ba56b86a3e0151036c6247e484
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949040"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service-for-project-operations"></a><span data-ttu-id="b4aa1-103">Настройка и применение данных конфигурации в Common Data Service для Project Operations</span><span class="sxs-lookup"><span data-stu-id="b4aa1-103">Set up and apply configuration data in the Common Data Service for Project Operations</span></span>

<span data-ttu-id="b4aa1-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/без запасов_</span><span class="sxs-lookup"><span data-stu-id="b4aa1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="b4aa1-105">Установка данных настройки и конфигурации</span><span class="sxs-lookup"><span data-stu-id="b4aa1-105">Install setup and configuration data</span></span>

1. <span data-ttu-id="b4aa1-106">Загрузите, разблокируйте и разархивируйте [Пакет данных настройки и конфигурации](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span><span class="sxs-lookup"><span data-stu-id="b4aa1-106">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="b4aa1-107">Перейдите в распакованную папку и запустите исполняемый файл, *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="b4aa1-107">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="b4aa1-108">На странице 1 мастера настройки Common Data Service (CMT) выберите **Импортировать данные**, затем выберите **Продолжить**.</span><span class="sxs-lookup"><span data-stu-id="b4aa1-108">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Миграция конфигурации](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="b4aa1-110">На странице 2 мастера CMT выберите **Office 365** как **Тип развертывания**.</span><span class="sxs-lookup"><span data-stu-id="b4aa1-110">On Page 2 of the CMT Wizard, select **Office 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="b4aa1-111">Установите флажки **Показать список доступных организаций** и **Показать расширенный**.</span><span class="sxs-lookup"><span data-stu-id="b4aa1-111">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="b4aa1-112">Выберите регион своего клиента, введите свои учетные данные и выберите **Войти**.</span><span class="sxs-lookup"><span data-stu-id="b4aa1-112">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Вход в конфигурацию](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="b4aa1-114">На странице 3 из списка организаций в клиенте выберите организацию, в которую вы хотите импортировать демонстрационные данные, и выберите **Войти**.</span><span class="sxs-lookup"><span data-stu-id="b4aa1-114">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="b4aa1-115">На странице 4 выберите ZIP-файл *SampleSetupAndConfigData* из распакованной папки.</span><span class="sxs-lookup"><span data-stu-id="b4aa1-115">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Выбор ZIP-файла](./media/3ZipFile.png)

![Выберите файл](./media/4SelectAFile.png)

9. <span data-ttu-id="b4aa1-118">После выбора ZIP-файла выберите **Импортировать данные**.</span><span class="sxs-lookup"><span data-stu-id="b4aa1-118">After the zip file is selected, select **Import Data**.</span></span>

![Импортировать данные](./media/5ImportData.png)

10. <span data-ttu-id="b4aa1-120">Импорт будет выполняться примерно от двух до десяти минут в зависимости от скорости вашей сети.</span><span class="sxs-lookup"><span data-stu-id="b4aa1-120">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="b4aa1-121">После завершения импорта выйдите из мастера CMT.</span><span class="sxs-lookup"><span data-stu-id="b4aa1-121">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="b4aa1-122">Проверьте свою организацию на наличие данных по следующим 19 сущностям:</span><span class="sxs-lookup"><span data-stu-id="b4aa1-122">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="b4aa1-123">Валюта</span><span class="sxs-lookup"><span data-stu-id="b4aa1-123">Currency</span></span>
  - <span data-ttu-id="b4aa1-124">Подразделение</span><span class="sxs-lookup"><span data-stu-id="b4aa1-124">Organizational Unit</span></span>
  - <span data-ttu-id="b4aa1-125">Контактные сведения</span><span class="sxs-lookup"><span data-stu-id="b4aa1-125">Contact</span></span>
  - <span data-ttu-id="b4aa1-126">Налоговая группа</span><span class="sxs-lookup"><span data-stu-id="b4aa1-126">Tax Group</span></span>
  - <span data-ttu-id="b4aa1-127">Группа клиентов</span><span class="sxs-lookup"><span data-stu-id="b4aa1-127">Customer Group</span></span>
  - <span data-ttu-id="b4aa1-128">Единица</span><span class="sxs-lookup"><span data-stu-id="b4aa1-128">Unit</span></span>
  - <span data-ttu-id="b4aa1-129">Группа единиц измерения</span><span class="sxs-lookup"><span data-stu-id="b4aa1-129">Unit Group</span></span>
  - <span data-ttu-id="b4aa1-130">Прайс-лист</span><span class="sxs-lookup"><span data-stu-id="b4aa1-130">Price List</span></span>
  - <span data-ttu-id="b4aa1-131">Прайс-лист параметров проекта</span><span class="sxs-lookup"><span data-stu-id="b4aa1-131">Project Parameter Price List</span></span>
  - <span data-ttu-id="b4aa1-132">Периодичность выставления счетов</span><span class="sxs-lookup"><span data-stu-id="b4aa1-132">Invoice Frequency</span></span>
  - <span data-ttu-id="b4aa1-133">Категория резервируемого ресурса</span><span class="sxs-lookup"><span data-stu-id="b4aa1-133">Bookable Resource Category</span></span>
  - <span data-ttu-id="b4aa1-134">Категория проводки</span><span class="sxs-lookup"><span data-stu-id="b4aa1-134">Transaction Category</span></span>
  - <span data-ttu-id="b4aa1-135">Категория расходов</span><span class="sxs-lookup"><span data-stu-id="b4aa1-135">Expense Category</span></span>
  - <span data-ttu-id="b4aa1-136">Цена роли</span><span class="sxs-lookup"><span data-stu-id="b4aa1-136">Role Price</span></span>
  - <span data-ttu-id="b4aa1-137">Цена категории проводки</span><span class="sxs-lookup"><span data-stu-id="b4aa1-137">Transaction Category Price</span></span>
  - <span data-ttu-id="b4aa1-138">Характеристика</span><span class="sxs-lookup"><span data-stu-id="b4aa1-138">Characteristic</span></span>
  - <span data-ttu-id="b4aa1-139">Резервируемый ресурс</span><span class="sxs-lookup"><span data-stu-id="b4aa1-139">Bookable Resource</span></span>
  - <span data-ttu-id="b4aa1-140">Назначение категории резервируемого ресурса</span><span class="sxs-lookup"><span data-stu-id="b4aa1-140">Bookable resource category Assn</span></span>
  - <span data-ttu-id="b4aa1-141">Характеристика резервируемого ресурса</span><span class="sxs-lookup"><span data-stu-id="b4aa1-141">Bookable Resource Characteristic</span></span>

![Завершите импорт](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="b4aa1-143">Обновление конфигураций Project Operations</span><span class="sxs-lookup"><span data-stu-id="b4aa1-143">Update Project Operations configurations</span></span>

1. <span data-ttu-id="b4aa1-144">Перейдите в среду CE.</span><span class="sxs-lookup"><span data-stu-id="b4aa1-144">Navigate to the CE environment.</span></span> <span data-ttu-id="b4aa1-145">Вы можете найти ее, открыв [Центр администрирования Power Platform](https://admin.powerplatform.microsoft.com/environments), выбрав среду, затем выбрав **Открыть среду**.</span><span class="sxs-lookup"><span data-stu-id="b4aa1-145">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Открыть среду](./media/7OpenEnvironment.png)

2. <span data-ttu-id="b4aa1-147">Выберите **Проекты** > **Ресурсы**, затем выберите **Создать**, чтобы создать доступный для резервирования ресурс для вашего пользователя.</span><span class="sxs-lookup"><span data-stu-id="b4aa1-147">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Резервируемые ресурсы](./media/8BookableResources.png)

3. <span data-ttu-id="b4aa1-149">На вкладке **Общие** выберите своего администратора.</span><span class="sxs-lookup"><span data-stu-id="b4aa1-149">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="b4aa1-150">Убедитесь, что часовой пояс соответствует тому, в котором вы находитесь.</span><span class="sxs-lookup"><span data-stu-id="b4aa1-150">Verify that the time zone matches the one you are in.</span></span> 

![Создание резервируемого ресурса](./media/9NewBookableResource.png)

4. <span data-ttu-id="b4aa1-152">На вкладке **Планирование** в поле **Компания** выберите компанию **USPM**, затем выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="b4aa1-152">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Вкладка планирования](./media/10SchedulingTab.png)

5. <span data-ttu-id="b4aa1-154">Перейдите на вкладку **Рабочие часы**.</span><span class="sxs-lookup"><span data-stu-id="b4aa1-154">Select the **Work hours** tab.</span></span>  

![Рабочие часы](./media/11WorkHours.png)

6. <span data-ttu-id="b4aa1-156">Дважды щелкните любое значение в календаре и выберите **Изменить** > **Все события этой серии**.</span><span class="sxs-lookup"><span data-stu-id="b4aa1-156">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Рабочий календарь](./media/12WorkCalendar.png)

7. <span data-ttu-id="b4aa1-158">Измените рабочие часы на восьмичасовой (8) рабочий день, отметьте выходные как нерабочие дни и убедитесь, что часовой пояс соответствует вашему.</span><span class="sxs-lookup"><span data-stu-id="b4aa1-158">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="b4aa1-159">Выберите **Сохранить и закрыть**.</span><span class="sxs-lookup"><span data-stu-id="b4aa1-159">Select **Save and close**.</span></span>

![Обновление календаря](./media/13UpdateCalendar.png)

9. <span data-ttu-id="b4aa1-161">Перейдите в раздел **Параметры** > **Шаблоны календаря** и выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="b4aa1-161">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Шаблоны календарей](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="b4aa1-163">Введите имя, выберите созданный вами шаблон ресурса, затем выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="b4aa1-163">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Сохранение шаблона календаря](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="b4aa1-165">Выберите **Параметры** и дважды щелкните запись.</span><span class="sxs-lookup"><span data-stu-id="b4aa1-165">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Параметры проекта](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="b4aa1-167">Обновите следующие поля:</span><span class="sxs-lookup"><span data-stu-id="b4aa1-167">Update the following fields:</span></span>

 - <span data-ttu-id="b4aa1-168">**Компания по умолчанию**: USPM</span><span class="sxs-lookup"><span data-stu-id="b4aa1-168">**Default company**: USPM</span></span>
 - <span data-ttu-id="b4aa1-169">**Подразделение по умолчанию**: Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="b4aa1-169">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="b4aa1-170">**Частота выставления счетов**: седьмой и последний день</span><span class="sxs-lookup"><span data-stu-id="b4aa1-170">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="b4aa1-171">**Шаблон рабочего времени**: измените на созданный вами шаблон.</span><span class="sxs-lookup"><span data-stu-id="b4aa1-171">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="b4aa1-172">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="b4aa1-172">Select **Save**.</span></span> 

![Обновление параметров проекта](./media/17UpdatedProjectParameters.png)
