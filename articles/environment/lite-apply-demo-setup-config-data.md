---
title: Применение демонстрационных данных настройки и конфигурации — облегченное развертывание
description: Эта тема предоставляет информацию о том, как применить демонстрационные данные настройки и конфигурации для Project Operations.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7729b4a9ef5f498b78af298f7233d7dd45434bb3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997167"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a><span data-ttu-id="a0a53-103">Применение демонстрационных данных настройки и конфигурации для Project Operations — облегченное развертывание</span><span class="sxs-lookup"><span data-stu-id="a0a53-103">Apply demo setup and configuration data for Project Operations - lite</span></span> 

<span data-ttu-id="a0a53-104">_\*\*Облегченное развертывание — от сделки до счетов-проформ_</span><span class="sxs-lookup"><span data-stu-id="a0a53-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="a0a53-105">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="a0a53-105">Prerequisites</span></span>

<span data-ttu-id="a0a53-106">Перед тем как начать настройку, вы должны иметь подготовленную среду Common Data Service (CDS) для Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="a0a53-106">Before you begin the configuration, you must have a Common Data Service (CDS) environment provisioned for Dynamics 365 Project Operations.</span></span>


## <a name="instructions"></a><span data-ttu-id="a0a53-107">Инструкции</span><span class="sxs-lookup"><span data-stu-id="a0a53-107">Instructions</span></span>

1. <span data-ttu-id="a0a53-108">Загрузите [пакет основных данных](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip).</span><span class="sxs-lookup"><span data-stu-id="a0a53-108">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip).</span></span> 
2. <span data-ttu-id="a0a53-109">Перейдите в папку *ProjOpsSampleSetupData - CE only CMT* и запустите исполняемый файл, *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="a0a53-109">Navigate to the folder *ProjOpsSampleSetupData - CE only CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="a0a53-110">На странице 1 мастера настройки Common Data Service (CMT) выберите **Импортировать данные**, затем выберите **Продолжить**.</span><span class="sxs-lookup"><span data-stu-id="a0a53-110">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

    ![Миграция конфигурации](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="a0a53-112">На странице 2 мастера CMT выберите **Microsoft 365** как **Тип развертывания**.</span><span class="sxs-lookup"><span data-stu-id="a0a53-112">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="a0a53-113">Установите флажки **Показать список доступных организаций** и **Показать расширенный**.</span><span class="sxs-lookup"><span data-stu-id="a0a53-113">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="a0a53-114">Выберите регион своего клиента, введите свои учетные данные, затем выберите **Войти**.</span><span class="sxs-lookup"><span data-stu-id="a0a53-114">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

   ![Вход в конфигурацию](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="a0a53-116">На странице 3 из списка организаций в клиенте выберите организацию, в которую вы хотите импортировать демонстрационные данные, затем выберите **Войти**.</span><span class="sxs-lookup"><span data-stu-id="a0a53-116">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="a0a53-117">На странице 4 выберите ZIP-файл, *SampleSetupAndConfigData* из распакованной папки, *ProjOpsSampleSetupData - CE only CMT*.</span><span class="sxs-lookup"><span data-stu-id="a0a53-117">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder, *ProjOpsSampleSetupData - CE only CMT*.</span></span>

   ![ZIP-файл](./media/3ZipFile.png)

   ![Выберите файл](./media/4SelectAFile.png)

9. <span data-ttu-id="a0a53-120">После выбора ZIP-файла выберите **Импортировать данные**.</span><span class="sxs-lookup"><span data-stu-id="a0a53-120">After the zip file is selected, select **Import Data**.</span></span>

   ![Импортировать данные](./media/5ImportData.png)

10. <span data-ttu-id="a0a53-122">Импорт будет выполняться примерно от двух до десяти минут в зависимости от скорости вашей сети.</span><span class="sxs-lookup"><span data-stu-id="a0a53-122">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="a0a53-123">После его завершения выйдите из мастера CMT.</span><span class="sxs-lookup"><span data-stu-id="a0a53-123">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="a0a53-124">Проверьте свою организацию на наличие данных по следующим 18 сущностям:</span><span class="sxs-lookup"><span data-stu-id="a0a53-124">Check your organization for data in the following 18 entities:</span></span>

    -   <span data-ttu-id="a0a53-125">Валюта</span><span class="sxs-lookup"><span data-stu-id="a0a53-125">Currency</span></span>
    -   <span data-ttu-id="a0a53-126">Учетная запись</span><span class="sxs-lookup"><span data-stu-id="a0a53-126">Account</span></span>
    -   <span data-ttu-id="a0a53-127">Подразделение</span><span class="sxs-lookup"><span data-stu-id="a0a53-127">Organizational Unit</span></span>
    -   <span data-ttu-id="a0a53-128">Контакт</span><span class="sxs-lookup"><span data-stu-id="a0a53-128">Contact</span></span>
    -   <span data-ttu-id="a0a53-129">Единица</span><span class="sxs-lookup"><span data-stu-id="a0a53-129">Unit</span></span>
    -   <span data-ttu-id="a0a53-130">Группа единиц измерения</span><span class="sxs-lookup"><span data-stu-id="a0a53-130">Unit Group</span></span>
    -   <span data-ttu-id="a0a53-131">Прайс-лист</span><span class="sxs-lookup"><span data-stu-id="a0a53-131">Price List</span></span>
    -   <span data-ttu-id="a0a53-132">Прайс-лист параметров проекта</span><span class="sxs-lookup"><span data-stu-id="a0a53-132">Project Parameter Price List</span></span> 
    -   <span data-ttu-id="a0a53-133">Периодичность выставления счетов</span><span class="sxs-lookup"><span data-stu-id="a0a53-133">Invoice Frequency</span></span>
    -   <span data-ttu-id="a0a53-134">Категория резервируемого ресурса</span><span class="sxs-lookup"><span data-stu-id="a0a53-134">Bookable Resource Category</span></span>
    -   <span data-ttu-id="a0a53-135">Категория проводки</span><span class="sxs-lookup"><span data-stu-id="a0a53-135">Transaction Category</span></span>
    -   <span data-ttu-id="a0a53-136">Категория расходов</span><span class="sxs-lookup"><span data-stu-id="a0a53-136">Expense Category</span></span>
    -   <span data-ttu-id="a0a53-137">Цена роли</span><span class="sxs-lookup"><span data-stu-id="a0a53-137">Role Price</span></span>
    -   <span data-ttu-id="a0a53-138">Цена категории проводки</span><span class="sxs-lookup"><span data-stu-id="a0a53-138">Transaction Category Price</span></span>
    -   <span data-ttu-id="a0a53-139">Характеристика</span><span class="sxs-lookup"><span data-stu-id="a0a53-139">Characteristic</span></span>
    -   <span data-ttu-id="a0a53-140">Резервируемый ресурс</span><span class="sxs-lookup"><span data-stu-id="a0a53-140">Bookable Resource</span></span>
    -   <span data-ttu-id="a0a53-141">Назначение категории резервируемого ресурса</span><span class="sxs-lookup"><span data-stu-id="a0a53-141">Bookable resource category Assn</span></span>
    -   <span data-ttu-id="a0a53-142">Характеристика резервируемого ресурса</span><span class="sxs-lookup"><span data-stu-id="a0a53-142">Bookable Resource Characteristic</span></span>

    ![Завершите импорт](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
