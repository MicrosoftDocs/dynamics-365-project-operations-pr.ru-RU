---
title: Настройка и применение демонстрационных данных в Common Data Service
description: Эта тема предоставляет информацию о настройке и применении данных конфигурации в Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 1651d3b3b85d3dc581bf61976fada249bafd6b7b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289835"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a><span data-ttu-id="1c75e-103">Настройка и применение демонстрационных данных в Common Data Service</span><span class="sxs-lookup"><span data-stu-id="1c75e-103">Set up and apply configuration data in the Common Data Service</span></span> 

<span data-ttu-id="1c75e-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/без запасов_</span><span class="sxs-lookup"><span data-stu-id="1c75e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="1c75e-105">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="1c75e-105">Prerequisites</span></span>

<span data-ttu-id="1c75e-106">Прежде чем приступить к настройке данных в Common Data Service (CDS), должны быть выполнены следующие предварительные условия:</span><span class="sxs-lookup"><span data-stu-id="1c75e-106">Before you beging to configure data in the Common Data Service (CDS), the following prerequisites must be met:</span></span>

1.  <span data-ttu-id="1c75e-107">Подготовьте среду CDS и среду Dynamics 365 Finance для Project Operations.</span><span class="sxs-lookup"><span data-stu-id="1c75e-107">Provision a CDS environment and a Dynamics 365 Finance environment for Project Operations.</span></span>
2.  <span data-ttu-id="1c75e-108">Информация о юридических лицах от Dynamics 365 Finance является общей в среде CDS.</span><span class="sxs-lookup"><span data-stu-id="1c75e-108">Legal entity information from Dynamics 365 Finance is shared to the CDS environment.</span></span> <span data-ttu-id="1c75e-109">Это означает, что сущность **Компания** в CDS имеет следующие записи компаний:</span><span class="sxs-lookup"><span data-stu-id="1c75e-109">This means that the **Company** entity in CDS has the following company records:</span></span>
  - <span data-ttu-id="1c75e-110">THPM</span><span class="sxs-lookup"><span data-stu-id="1c75e-110">THPM</span></span>
  - <span data-ttu-id="1c75e-111">USPM</span><span class="sxs-lookup"><span data-stu-id="1c75e-111">USPM</span></span>
  - <span data-ttu-id="1c75e-112">GBPM</span><span class="sxs-lookup"><span data-stu-id="1c75e-112">GBPM</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="1c75e-113">Установка данных настройки и конфигурации</span><span class="sxs-lookup"><span data-stu-id="1c75e-113">Install setup and configuration data</span></span>

1. <span data-ttu-id="1c75e-114">Загрузите, разблокируйте и разархивируйте [Пакет данных настройки и конфигурации](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span><span class="sxs-lookup"><span data-stu-id="1c75e-114">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="1c75e-115">Перейдите в распакованную папку и запустите исполняемый файл, *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="1c75e-115">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="1c75e-116">На странице 1 мастера настройки Common Data Service (CMT) выберите **Импортировать данные**, затем выберите **Продолжить**.</span><span class="sxs-lookup"><span data-stu-id="1c75e-116">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Миграция конфигурации](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="1c75e-118">На странице 2 мастера CMT выберите **Microsoft 365** как **Тип развертывания**.</span><span class="sxs-lookup"><span data-stu-id="1c75e-118">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="1c75e-119">Установите флажки **Показать список доступных организаций** и **Показать расширенный**.</span><span class="sxs-lookup"><span data-stu-id="1c75e-119">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="1c75e-120">Выберите регион своего клиента, введите свои учетные данные и выберите **Войти**.</span><span class="sxs-lookup"><span data-stu-id="1c75e-120">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Вход в конфигурацию](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="1c75e-122">На странице 3 из списка организаций в клиенте выберите организацию, в которую вы хотите импортировать демонстрационные данные, и выберите **Войти**.</span><span class="sxs-lookup"><span data-stu-id="1c75e-122">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="1c75e-123">На странице 4 выберите ZIP-файл *SampleSetupAndConfigData* из распакованной папки.</span><span class="sxs-lookup"><span data-stu-id="1c75e-123">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Выбор ZIP-файла](./media/3ZipFile.png)

![Выберите файл](./media/4SelectAFile.png)

9. <span data-ttu-id="1c75e-126">После выбора ZIP-файла выберите **Импортировать данные**.</span><span class="sxs-lookup"><span data-stu-id="1c75e-126">After the zip file is selected, select **Import Data**.</span></span>

![Импортировать данные](./media/5ImportData.png)

10. <span data-ttu-id="1c75e-128">Импорт будет выполняться примерно от двух до десяти минут в зависимости от скорости вашей сети.</span><span class="sxs-lookup"><span data-stu-id="1c75e-128">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="1c75e-129">После завершения импорта выйдите из мастера CMT.</span><span class="sxs-lookup"><span data-stu-id="1c75e-129">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="1c75e-130">Проверьте свою организацию на наличие данных по следующим 19 сущностям:</span><span class="sxs-lookup"><span data-stu-id="1c75e-130">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="1c75e-131">Валюта</span><span class="sxs-lookup"><span data-stu-id="1c75e-131">Currency</span></span>
  - <span data-ttu-id="1c75e-132">Подразделение</span><span class="sxs-lookup"><span data-stu-id="1c75e-132">Organizational Unit</span></span>
  - <span data-ttu-id="1c75e-133">Контактные сведения</span><span class="sxs-lookup"><span data-stu-id="1c75e-133">Contact</span></span>
  - <span data-ttu-id="1c75e-134">Налоговая группа</span><span class="sxs-lookup"><span data-stu-id="1c75e-134">Tax Group</span></span>
  - <span data-ttu-id="1c75e-135">Группа клиентов</span><span class="sxs-lookup"><span data-stu-id="1c75e-135">Customer Group</span></span>
  - <span data-ttu-id="1c75e-136">Единица</span><span class="sxs-lookup"><span data-stu-id="1c75e-136">Unit</span></span>
  - <span data-ttu-id="1c75e-137">Группа единиц измерения</span><span class="sxs-lookup"><span data-stu-id="1c75e-137">Unit Group</span></span>
  - <span data-ttu-id="1c75e-138">Прайс-лист</span><span class="sxs-lookup"><span data-stu-id="1c75e-138">Price List</span></span>
  - <span data-ttu-id="1c75e-139">Прайс-лист параметров проекта</span><span class="sxs-lookup"><span data-stu-id="1c75e-139">Project Parameter Price List</span></span>
  - <span data-ttu-id="1c75e-140">Периодичность выставления счетов</span><span class="sxs-lookup"><span data-stu-id="1c75e-140">Invoice Frequency</span></span>
  - <span data-ttu-id="1c75e-141">Категория резервируемого ресурса</span><span class="sxs-lookup"><span data-stu-id="1c75e-141">Bookable Resource Category</span></span>
  - <span data-ttu-id="1c75e-142">Категория проводки</span><span class="sxs-lookup"><span data-stu-id="1c75e-142">Transaction Category</span></span>
  - <span data-ttu-id="1c75e-143">Категория расходов</span><span class="sxs-lookup"><span data-stu-id="1c75e-143">Expense Category</span></span>
  - <span data-ttu-id="1c75e-144">Цена роли</span><span class="sxs-lookup"><span data-stu-id="1c75e-144">Role Price</span></span>
  - <span data-ttu-id="1c75e-145">Цена категории проводки</span><span class="sxs-lookup"><span data-stu-id="1c75e-145">Transaction Category Price</span></span>
  - <span data-ttu-id="1c75e-146">Характеристика</span><span class="sxs-lookup"><span data-stu-id="1c75e-146">Characteristic</span></span>
  - <span data-ttu-id="1c75e-147">Резервируемый ресурс</span><span class="sxs-lookup"><span data-stu-id="1c75e-147">Bookable Resource</span></span>
  - <span data-ttu-id="1c75e-148">Назначение категории резервируемого ресурса</span><span class="sxs-lookup"><span data-stu-id="1c75e-148">Bookable resource category Assn</span></span>
  - <span data-ttu-id="1c75e-149">Характеристика резервируемого ресурса</span><span class="sxs-lookup"><span data-stu-id="1c75e-149">Bookable Resource Characteristic</span></span>

![Завершите импорт](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="1c75e-151">Обновление конфигураций Project Operations</span><span class="sxs-lookup"><span data-stu-id="1c75e-151">Update Project Operations configurations</span></span>

1. <span data-ttu-id="1c75e-152">Перейдите в среду CE.</span><span class="sxs-lookup"><span data-stu-id="1c75e-152">Navigate to the CE environment.</span></span> <span data-ttu-id="1c75e-153">Вы можете найти ее, открыв [Центр администрирования Power Platform](https://admin.powerplatform.microsoft.com/environments), выбрав среду, затем выбрав **Открыть среду**.</span><span class="sxs-lookup"><span data-stu-id="1c75e-153">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Открыть среду](./media/7OpenEnvironment.png)

2. <span data-ttu-id="1c75e-155">Выберите **Проекты** > **Ресурсы**, затем выберите **Создать**, чтобы создать доступный для резервирования ресурс для вашего пользователя.</span><span class="sxs-lookup"><span data-stu-id="1c75e-155">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Резервируемые ресурсы](./media/8BookableResources.png)

3. <span data-ttu-id="1c75e-157">На вкладке **Общие** выберите своего администратора.</span><span class="sxs-lookup"><span data-stu-id="1c75e-157">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="1c75e-158">Убедитесь, что часовой пояс соответствует тому, в котором вы находитесь.</span><span class="sxs-lookup"><span data-stu-id="1c75e-158">Verify that the time zone matches the one you are in.</span></span> 

![Создание резервируемого ресурса](./media/9NewBookableResource.png)

4. <span data-ttu-id="1c75e-160">На вкладке **Планирование** в поле **Компания** выберите компанию **USPM**, затем выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="1c75e-160">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Вкладка планирования](./media/10SchedulingTab.png)

5. <span data-ttu-id="1c75e-162">Перейдите на вкладку **Рабочие часы**.</span><span class="sxs-lookup"><span data-stu-id="1c75e-162">Select the **Work hours** tab.</span></span>  

![Рабочие часы](./media/11WorkHours.png)

6. <span data-ttu-id="1c75e-164">Дважды щелкните любое значение в календаре и выберите **Изменить** > **Все события этой серии**.</span><span class="sxs-lookup"><span data-stu-id="1c75e-164">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Рабочий календарь](./media/12WorkCalendar.png)

7. <span data-ttu-id="1c75e-166">Измените рабочие часы на восьмичасовой (8) рабочий день, отметьте выходные как нерабочие дни и убедитесь, что часовой пояс соответствует вашему.</span><span class="sxs-lookup"><span data-stu-id="1c75e-166">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="1c75e-167">Выберите **Сохранить и закрыть**.</span><span class="sxs-lookup"><span data-stu-id="1c75e-167">Select **Save and close**.</span></span>

![Обновление календаря](./media/13UpdateCalendar.png)

9. <span data-ttu-id="1c75e-169">Перейдите в раздел **Параметры** > **Шаблоны календаря** и выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="1c75e-169">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Шаблоны календарей](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="1c75e-171">Введите имя, выберите созданный вами шаблон ресурса, затем выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="1c75e-171">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Сохранение шаблона календаря](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="1c75e-173">Выберите **Параметры** и дважды щелкните запись.</span><span class="sxs-lookup"><span data-stu-id="1c75e-173">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Параметры проекта](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="1c75e-175">Обновите следующие поля:</span><span class="sxs-lookup"><span data-stu-id="1c75e-175">Update the following fields:</span></span>

 - <span data-ttu-id="1c75e-176">**Компания по умолчанию**: USPM</span><span class="sxs-lookup"><span data-stu-id="1c75e-176">**Default company**: USPM</span></span>
 - <span data-ttu-id="1c75e-177">**Подразделение по умолчанию**: Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="1c75e-177">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="1c75e-178">**Частота выставления счетов**: седьмой и последний день</span><span class="sxs-lookup"><span data-stu-id="1c75e-178">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="1c75e-179">**Шаблон рабочего времени**: измените на созданный вами шаблон.</span><span class="sxs-lookup"><span data-stu-id="1c75e-179">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="1c75e-180">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="1c75e-180">Select **Save**.</span></span> 

![Обновление параметров проекта](./media/17UpdatedProjectParameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]