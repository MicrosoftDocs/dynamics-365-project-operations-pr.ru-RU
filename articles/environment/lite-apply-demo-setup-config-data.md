---
title: Применение демонстрационных данных настройки и конфигурации — облегченное развертывание
description: Эта тема предоставляет информацию о том, как применить демонстрационные данные настройки и конфигурации для Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5cfc270c07a568d692f6cd180b9c367ae185044c
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401279"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a><span data-ttu-id="ab0e9-103">Применение демонстрационных данных настройки и конфигурации для Project Operations — облегченное развертывание</span><span class="sxs-lookup"><span data-stu-id="ab0e9-103">Apply demo setup and configuration data for Project Operations - lite</span></span> 

<span data-ttu-id="ab0e9-104">_\*\*Облегченное развертывание — от сделки до счетов-проформ_</span><span class="sxs-lookup"><span data-stu-id="ab0e9-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ab0e9-105">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="ab0e9-105">Prerequisites</span></span>

<span data-ttu-id="ab0e9-106">Перед тем как начать настройку, вы должны иметь подготовленную среду Common Data Service (CDS) для Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="ab0e9-106">Before you begin the configuration, you must have a Common Data Service (CDS) environment provisioned for Dynamics 365 Project Operations.</span></span>


## <a name="instructions"></a><span data-ttu-id="ab0e9-107">Инструкции</span><span class="sxs-lookup"><span data-stu-id="ab0e9-107">Instructions</span></span>

1. <span data-ttu-id="ab0e9-108">Загрузите [пакет основных данных](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="ab0e9-108">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="ab0e9-109">Перейдите в папку *ProjOpsDemoDataSetupAndMaster — интегрированный CMT* и запустите исполняемый файл, *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="ab0e9-109">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="ab0e9-110">На странице 1 мастера настройки Common Data Service (CMT) выберите **Импортировать данные**, затем выберите **Продолжить**.</span><span class="sxs-lookup"><span data-stu-id="ab0e9-110">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Миграция конфигурации](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="ab0e9-112">На странице 2 мастера CMT выберите **Microsoft 365** как **Тип развертывания**.</span><span class="sxs-lookup"><span data-stu-id="ab0e9-112">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="ab0e9-113">Установите флажки **Показать список доступных организаций** и **Показать расширенный**.</span><span class="sxs-lookup"><span data-stu-id="ab0e9-113">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="ab0e9-114">Выберите регион своего клиента, введите свои учетные данные, затем выберите **Войти**.</span><span class="sxs-lookup"><span data-stu-id="ab0e9-114">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![Вход в конфигурацию](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="ab0e9-116">На странице 3 из списка организаций в клиенте выберите организацию, в которую вы хотите импортировать демонстрационные данные, затем выберите **Войти**.</span><span class="sxs-lookup"><span data-stu-id="ab0e9-116">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="ab0e9-117">На странице 4 выберите ZIP-файл *MasterAndSetupData* из распакованной папки, *ProjOpsDemoDataSetupAndMaster — интегрированный CMT*.</span><span class="sxs-lookup"><span data-stu-id="ab0e9-117">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![ZIP-файл](./media/3ZipFile.png)

![Выберите файл](./media/4SelectAFile.png)

9. <span data-ttu-id="ab0e9-120">После выбора ZIP-файла выберите **Импортировать данные**.</span><span class="sxs-lookup"><span data-stu-id="ab0e9-120">After the zip file is selected, select **Import Data**.</span></span>

![Импортировать данные](./media/5ImportData.png)

10. <span data-ttu-id="ab0e9-122">Импорт будет выполняться примерно от двух до десяти минут в зависимости от скорости вашей сети.</span><span class="sxs-lookup"><span data-stu-id="ab0e9-122">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="ab0e9-123">После его завершения выйдите из мастера CMT.</span><span class="sxs-lookup"><span data-stu-id="ab0e9-123">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="ab0e9-124">Проверьте свою организацию на наличие данных по следующим 20 сущностям:</span><span class="sxs-lookup"><span data-stu-id="ab0e9-124">Check your organization for data in the following 20 entities:</span></span>

-   <span data-ttu-id="ab0e9-125">Валюта</span><span class="sxs-lookup"><span data-stu-id="ab0e9-125">Currency</span></span>
-   <span data-ttu-id="ab0e9-126">Уч. запись</span><span class="sxs-lookup"><span data-stu-id="ab0e9-126">Account</span></span>
-   <span data-ttu-id="ab0e9-127">Подразделение</span><span class="sxs-lookup"><span data-stu-id="ab0e9-127">Organizational Unit</span></span>
-   <span data-ttu-id="ab0e9-128">Контактные сведения</span><span class="sxs-lookup"><span data-stu-id="ab0e9-128">Contact</span></span>
-   <span data-ttu-id="ab0e9-129">Налоговая группа</span><span class="sxs-lookup"><span data-stu-id="ab0e9-129">Tax Group</span></span>
-   <span data-ttu-id="ab0e9-130">Группа клиентов</span><span class="sxs-lookup"><span data-stu-id="ab0e9-130">Customer Group</span></span>
-   <span data-ttu-id="ab0e9-131">Единица</span><span class="sxs-lookup"><span data-stu-id="ab0e9-131">Unit</span></span>
-   <span data-ttu-id="ab0e9-132">Группа единиц измерения</span><span class="sxs-lookup"><span data-stu-id="ab0e9-132">Unit Group</span></span>
-   <span data-ttu-id="ab0e9-133">Прайс-лист</span><span class="sxs-lookup"><span data-stu-id="ab0e9-133">Price List</span></span>
-   <span data-ttu-id="ab0e9-134">Прайс-лист параметров проекта</span><span class="sxs-lookup"><span data-stu-id="ab0e9-134">Project Parameter Price List</span></span> 
-   <span data-ttu-id="ab0e9-135">Периодичность выставления счетов</span><span class="sxs-lookup"><span data-stu-id="ab0e9-135">Invoice Frequency</span></span>
-   <span data-ttu-id="ab0e9-136">Категория резервируемого ресурса</span><span class="sxs-lookup"><span data-stu-id="ab0e9-136">Bookable Resource Category</span></span>
-   <span data-ttu-id="ab0e9-137">Категория проводки</span><span class="sxs-lookup"><span data-stu-id="ab0e9-137">Transaction Category</span></span>
-   <span data-ttu-id="ab0e9-138">Категория расходов</span><span class="sxs-lookup"><span data-stu-id="ab0e9-138">Expense Category</span></span>
-   <span data-ttu-id="ab0e9-139">Цена роли</span><span class="sxs-lookup"><span data-stu-id="ab0e9-139">Role Price</span></span>
-   <span data-ttu-id="ab0e9-140">Цена категории проводки</span><span class="sxs-lookup"><span data-stu-id="ab0e9-140">Transaction Category Price</span></span>
-   <span data-ttu-id="ab0e9-141">Характеристика</span><span class="sxs-lookup"><span data-stu-id="ab0e9-141">Characteristic</span></span>
-   <span data-ttu-id="ab0e9-142">Резервируемый ресурс</span><span class="sxs-lookup"><span data-stu-id="ab0e9-142">Bookable Resource</span></span>
-   <span data-ttu-id="ab0e9-143">Назначение категории резервируемого ресурса</span><span class="sxs-lookup"><span data-stu-id="ab0e9-143">Bookable resource category Assn</span></span>
-   <span data-ttu-id="ab0e9-144">Характеристика резервируемого ресурса</span><span class="sxs-lookup"><span data-stu-id="ab0e9-144">Bookable Resource Characteristic</span></span>

![Завершите импорт](./media/6CompleteImport.png)
