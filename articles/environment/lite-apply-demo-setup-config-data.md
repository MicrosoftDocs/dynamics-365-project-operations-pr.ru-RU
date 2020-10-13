---
title: Применение демонстрационных данных настройки и конфигурации
description: Эта тема предоставляет информацию о том, как применить демонстрационные данные настройки и конфигурации для Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 42e02f393e89d20b2a462645f519a3792bee8f2f
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949037"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="9ae00-103">Применение демонстрационных данных настройки и конфигурации для развертывания Project Operations Lite — от сделки до счетов-проформ</span><span class="sxs-lookup"><span data-stu-id="9ae00-103">Apply demo setup and configuration data for Project Operations lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="9ae00-104">_\*\*Облегченное развертывание — от сделки до счетов-проформ_</span><span class="sxs-lookup"><span data-stu-id="9ae00-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

1. <span data-ttu-id="9ae00-105">Загрузите [пакет основных данных](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="9ae00-105">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="9ae00-106">Перейдите в папку *ProjOpsDemoDataSetupAndMaster — интегрированный CMT* и запустите исполняемый файл, *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="9ae00-106">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="9ae00-107">На странице 1 мастера настройки Common Data Service (CMT) выберите **Импортировать данные**, затем выберите **Продолжить**.</span><span class="sxs-lookup"><span data-stu-id="9ae00-107">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Миграция конфигурации](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="9ae00-109">На странице 2 мастера CMT выберите **Office 365** как **Тип развертывания**.</span><span class="sxs-lookup"><span data-stu-id="9ae00-109">On Page 2 of the CMT Wizard, select **Office 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="9ae00-110">Установите флажки **Показать список доступных организаций** и **Показать расширенный**.</span><span class="sxs-lookup"><span data-stu-id="9ae00-110">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="9ae00-111">Выберите регион своего клиента, введите свои учетные данные, затем выберите **Войти**.</span><span class="sxs-lookup"><span data-stu-id="9ae00-111">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![Вход в конфигурацию](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="9ae00-113">На странице 3 из списка организаций в клиенте выберите организацию, в которую вы хотите импортировать демонстрационные данные, затем выберите **Войти**.</span><span class="sxs-lookup"><span data-stu-id="9ae00-113">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="9ae00-114">На странице 4 выберите ZIP-файл *MasterAndSetupData* из распакованной папки, *ProjOpsDemoDataSetupAndMaster — интегрированный CMT*.</span><span class="sxs-lookup"><span data-stu-id="9ae00-114">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![ZIP-файл](./media/3ZipFile.png)

![Выберите файл](./media/4SelectAFile.png)

9. <span data-ttu-id="9ae00-117">После выбора ZIP-файла выберите **Импортировать данные**.</span><span class="sxs-lookup"><span data-stu-id="9ae00-117">After the zip file is selected, select **Import Data**.</span></span>

![Импортировать данные](./media/5ImportData.png)

10. <span data-ttu-id="9ae00-119">Импорт будет выполняться примерно от двух до десяти минут в зависимости от скорости вашей сети.</span><span class="sxs-lookup"><span data-stu-id="9ae00-119">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="9ae00-120">После его завершения выйдите из мастера CMT.</span><span class="sxs-lookup"><span data-stu-id="9ae00-120">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="9ae00-121">Проверьте свою организацию на наличие данных по следующим 20 сущностям:</span><span class="sxs-lookup"><span data-stu-id="9ae00-121">Check your organization for data in the following 20 entities:</span></span>

- <span data-ttu-id="9ae00-122">Валюта</span><span class="sxs-lookup"><span data-stu-id="9ae00-122">Currency</span></span>
- <span data-ttu-id="9ae00-123">Подразделение</span><span class="sxs-lookup"><span data-stu-id="9ae00-123">Organizational Unit</span></span>
- <span data-ttu-id="9ae00-124">Контактные сведения</span><span class="sxs-lookup"><span data-stu-id="9ae00-124">Contact</span></span>
- <span data-ttu-id="9ae00-125">Налоговая группа</span><span class="sxs-lookup"><span data-stu-id="9ae00-125">Tax Group</span></span>
- <span data-ttu-id="9ae00-126">Группа клиентов</span><span class="sxs-lookup"><span data-stu-id="9ae00-126">Customer Group</span></span>
- <span data-ttu-id="9ae00-127">Единица</span><span class="sxs-lookup"><span data-stu-id="9ae00-127">Unit</span></span>
- <span data-ttu-id="9ae00-128">Группа единиц измерения</span><span class="sxs-lookup"><span data-stu-id="9ae00-128">Unit Group</span></span>
- <span data-ttu-id="9ae00-129">Прайс-лист</span><span class="sxs-lookup"><span data-stu-id="9ae00-129">Price List</span></span>
- <span data-ttu-id="9ae00-130">Прайс-лист параметров проекта</span><span class="sxs-lookup"><span data-stu-id="9ae00-130">Project Parameter Price List</span></span>
- <span data-ttu-id="9ae00-131">Периодичность выставления счетов</span><span class="sxs-lookup"><span data-stu-id="9ae00-131">Invoice Frequency</span></span>
- <span data-ttu-id="9ae00-132">Сведения периодичности выставления счета</span><span class="sxs-lookup"><span data-stu-id="9ae00-132">Invoice Frequency Detail</span></span>
- <span data-ttu-id="9ae00-133">Категория резервируемого ресурса</span><span class="sxs-lookup"><span data-stu-id="9ae00-133">Bookable Resource Category</span></span>
- <span data-ttu-id="9ae00-134">Категория проводки</span><span class="sxs-lookup"><span data-stu-id="9ae00-134">Transaction Category</span></span>
- <span data-ttu-id="9ae00-135">Категория расходов</span><span class="sxs-lookup"><span data-stu-id="9ae00-135">Expense Category</span></span>
- <span data-ttu-id="9ae00-136">Цена роли</span><span class="sxs-lookup"><span data-stu-id="9ae00-136">Role Price</span></span>
- <span data-ttu-id="9ae00-137">Цена категории проводки</span><span class="sxs-lookup"><span data-stu-id="9ae00-137">Transaction Category Price</span></span>
- <span data-ttu-id="9ae00-138">Характеристика</span><span class="sxs-lookup"><span data-stu-id="9ae00-138">Characteristic</span></span>
- <span data-ttu-id="9ae00-139">Резервируемый ресурс</span><span class="sxs-lookup"><span data-stu-id="9ae00-139">Bookable Resource</span></span>
- <span data-ttu-id="9ae00-140">Назначение категории резервируемого ресурса</span><span class="sxs-lookup"><span data-stu-id="9ae00-140">Bookable resource category Assn</span></span>
- <span data-ttu-id="9ae00-141">Характеристика резервируемого ресурса</span><span class="sxs-lookup"><span data-stu-id="9ae00-141">Bookable Resource Characteristic</span></span>

![Завершите импорт](./media/6CompleteImport.png)
