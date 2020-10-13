---
title: Применение демонстрационных данных Project Operations к размещенной в облаке среде Finance
description: В этой теме объясняется, как применить демонстрационные данные из Project Operations к размещенной в облаке среде Dynamics 365 Finance.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 1a94862d5a024eb1630f33c0c96699e8b4b49bf2
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949045"
---
# <a name="apply-project-operations-demo-data-to-a-finance-cloud-hosted-environment"></a><span data-ttu-id="03e3e-103">Применение демонстрационных данных Project Operations к размещенной в облаке среде Finance</span><span class="sxs-lookup"><span data-stu-id="03e3e-103">Apply Project Operations demo data to a Finance Cloud-hosted environment</span></span>

<span data-ttu-id="03e3e-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/без запасов_</span><span class="sxs-lookup"><span data-stu-id="03e3e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

><span data-ttu-id="03e3e-105">[Важно] Эта тема применима только к Microsoft Dynamics 365 Finance версии 10.0.13 и может выполняться только в облачной среде.</span><span class="sxs-lookup"><span data-stu-id="03e3e-105">[Important] This topic is only applicable only Microsoft Dynamics 365 Finance version 10.0.13 and can be performed only on a Cloud-hosted environment.</span></span> <span data-ttu-id="03e3e-106">Выполните действия, описанные в этой теме, **ПЕРЕД** применением обновлений качества к среде.</span><span class="sxs-lookup"><span data-stu-id="03e3e-106">Complete the steps in this topic **BEFORE** you apply quality updates to the environment.</span></span>

1. <span data-ttu-id="03e3e-107">В своем проекте LCS откройте страницу **Сведения о среде**.</span><span class="sxs-lookup"><span data-stu-id="03e3e-107">In your LCS project, open the **Environment details** page.</span></span> <span data-ttu-id="03e3e-108">Обратите внимание, что она включает сведения, необходимые для подключения к среде с помощью протокола удаленного рабочего стола (RDP).</span><span class="sxs-lookup"><span data-stu-id="03e3e-108">Notice that it includes the details needed to connect to the environment by using Remote Desktop Protocol (RDP).</span></span>

![Сведения о среде ](./media/1EnvironmentDetails.png)

<span data-ttu-id="03e3e-110">Первый набор выделенных учетных данных — это учетные данные локальной учетной записи, которые содержат гиперссылку на подключение к удаленному рабочему столу.</span><span class="sxs-lookup"><span data-stu-id="03e3e-110">The first set of highlighted credentials are the local account credentials and contain a hyperlink to the remote desktop connection.</span></span> <span data-ttu-id="03e3e-111">Учетные данные включают имя пользователя и пароль администратора среды.</span><span class="sxs-lookup"><span data-stu-id="03e3e-111">The credentials include the environment admin username and password.</span></span> <span data-ttu-id="03e3e-112">Второй набор учетных данных используется для входа в сервер SQL Server в этой среде.</span><span class="sxs-lookup"><span data-stu-id="03e3e-112">The second set of credentials are used to log in to SQL Server in this environment.</span></span>

2. <span data-ttu-id="03e3e-113">Удаленно подключитесь к среде по гиперссылке в пункте **Локальные учетные записи** и используйте **Учетные данные локальной учетной записи** для аутентификации.</span><span class="sxs-lookup"><span data-stu-id="03e3e-113">Remote to the environment by the hyperlink in **Local Accounts**, and use the **Local Account credentials** to authenticate.</span></span>
3. <span data-ttu-id="03e3e-114">Выберите **Службы IIS** > **Пулы приложений** > **AOSService** и остановите эту службу.</span><span class="sxs-lookup"><span data-stu-id="03e3e-114">Go to **Internet Information Services** > **Application Pools** > **AOSService** and stop the service.</span></span> <span data-ttu-id="03e3e-115">На этом этапе вы останавливаете службу, чтобы продолжить замену базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="03e3e-115">You are stopping the service at this point so that you can continue to replace the SQL database.</span></span>

![Остановка AOS](./media/2StopAOS.png)

4. <span data-ttu-id="03e3e-117">Выберите **Службы** и остановите следующие два пункта:</span><span class="sxs-lookup"><span data-stu-id="03e3e-117">Go to **Services** and stop the following two items:</span></span>

- <span data-ttu-id="03e3e-118">Microsoft Dynamics 365 Unified Operations: служба управления пакетными заданиями</span><span class="sxs-lookup"><span data-stu-id="03e3e-118">Microsoft Dynamics 365 Unified Operations: Batch Management Service</span></span>
- <span data-ttu-id="03e3e-119">Microsoft Dynamics 365 Unified Operations: структура импорта и экспорта данных</span><span class="sxs-lookup"><span data-stu-id="03e3e-119">Microsoft Dynamics 365 Unified Operations: Data Import Export Framework</span></span>

![Остановка служб](./media/3StopServices.png)

5. <span data-ttu-id="03e3e-121">Откройте Microsoft SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="03e3e-121">Open Microsoft SQL Server Management Studio.</span></span> <span data-ttu-id="03e3e-122">Войдите с учетными данными SQL-сервера и используйте пользователя и пароль axdbadmin со страницы LCS **Сведения о средах**.</span><span class="sxs-lookup"><span data-stu-id="03e3e-122">Log in with SQL server credentials and use the axdbadmin user and password from the LCS **Environments details** page.</span></span>

![SQL Server Management Studio](./media/4SSMS.png)

6. <span data-ttu-id="03e3e-124">В обозревателе объектов **Базы данных** и найдите **AXDB**.</span><span class="sxs-lookup"><span data-stu-id="03e3e-124">In Object Explorer, **Databases** and locate **AXDB**.</span></span> <span data-ttu-id="03e3e-125">Вы замените базу данных новой базой данных, которая находится в [Центре загрузок](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span><span class="sxs-lookup"><span data-stu-id="03e3e-125">You will replace database with a new database that is located in the [Download Center](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span></span> 
7. <span data-ttu-id="03e3e-126">Скопируйте ZIP-файл на виртуальную машину, к которой вы удаленно подключены, и извлеките ZIP-файл.</span><span class="sxs-lookup"><span data-stu-id="03e3e-126">Copy the zip file to the VM you are remoted into and extract zip contents.</span></span>
8. <span data-ttu-id="03e3e-127">В SQL Server Management Studio щелкните правой кнопкой мыши **AxDB**, затем выберите **Задачи** > **Восстановить** > **База данных**.</span><span class="sxs-lookup"><span data-stu-id="03e3e-127">In SQL Server Management Studio, right-click **AxDB**, and then select **Tasks** > **Restore** > **Database**.</span></span>

![Восстановление базы данных](./media/5RestoreDatabase.png)

9. <span data-ttu-id="03e3e-129">Выберите **Исходное устройство** и перейдите к файлу, извлеченному из скопированного вами ZIP-архива.</span><span class="sxs-lookup"><span data-stu-id="03e3e-129">Select **Source Device** and navigate to the file extracted from zip you copied.</span></span>

![Исходные устройства](./media/6SourceDevice.png)

10. <span data-ttu-id="03e3e-131">Выберите **Параметры**, затем выберите **Перезаписать существующую базу данных** и **Закрыть существующие подключения к целевой базе данных**.</span><span class="sxs-lookup"><span data-stu-id="03e3e-131">Select **Options**, and then select **Overwrite the existing database** and **Close existing connections to destination database**.</span></span> 
11. <span data-ttu-id="03e3e-132">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="03e3e-132">Select **OK**.</span></span>

![Восстановление параметров](./media/7RestoreSetting.png)

<span data-ttu-id="03e3e-134">Вы получите подтверждение, что восстановление AXDB прошло успешно.</span><span class="sxs-lookup"><span data-stu-id="03e3e-134">You will receive confirmation that the AXDB restore was successful.</span></span> <span data-ttu-id="03e3e-135">Получив это подтверждение, вы можете закрыть SQL Services Management Studio.</span><span class="sxs-lookup"><span data-stu-id="03e3e-135">After you receive this confirmation, you can close SQL Services Management Studio.</span></span>

12. <span data-ttu-id="03e3e-136">Вернитесь в раздел **Службы IIS** > **Пулы приложений** > **AOSService** и запустите службу AOSService.</span><span class="sxs-lookup"><span data-stu-id="03e3e-136">Go back to **Internet Information Services** > **Application Pools** > **AOSService** and start the AOSService.</span></span>
13. <span data-ttu-id="03e3e-137">Перейдите в раздел **Службы** и запустите две службы, которые вы остановили ранее.</span><span class="sxs-lookup"><span data-stu-id="03e3e-137">Go to **Services** and start the two services you stopped earlier.</span></span>

14. <span data-ttu-id="03e3e-138">Найдите на этой виртуальной машине инструмент AdminUserProvisioning.</span><span class="sxs-lookup"><span data-stu-id="03e3e-138">Locate the AdminUserProvisioning tool on this VM.</span></span> <span data-ttu-id="03e3e-139">Ищите K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span><span class="sxs-lookup"><span data-stu-id="03e3e-139">Look under, K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span></span>
15. <span data-ttu-id="03e3e-140">Запустите файл .ext, используя свой адрес пользователя в поле **Адрес электронной почты**.</span><span class="sxs-lookup"><span data-stu-id="03e3e-140">Run the .ext file using your user address in the **Email Address** field.</span></span> 
16. <span data-ttu-id="03e3e-141">Выберите **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="03e3e-141">Select **Submit**.</span></span>

![Подготовка пользователя-администратора](./media/8AdminUserProvisioning.png)

<span data-ttu-id="03e3e-143">Это займет пару минут.</span><span class="sxs-lookup"><span data-stu-id="03e3e-143">This takes a couple of minutes to complete.</span></span> <span data-ttu-id="03e3e-144">Вы должны получить подтверждающее сообщение об успешном обновлении пользователя-администратора.</span><span class="sxs-lookup"><span data-stu-id="03e3e-144">You should receive a confirmation message that the Admin user was successfully updated.</span></span>

17. <span data-ttu-id="03e3e-145">Наконец, запустите командную строку от имени администратора и выполните команду iisreset</span><span class="sxs-lookup"><span data-stu-id="03e3e-145">Lastly, run Command Prompt as Administrator and perform iisreset</span></span>

![Сброс IIS](./media/9IISReset.png)

18. <span data-ttu-id="03e3e-147">Закройте сеанс удаленного рабочего стола и используйте страницу LCS **Сведения о среде**, чтобы войти в среду и убедиться, что она работает должным образом.</span><span class="sxs-lookup"><span data-stu-id="03e3e-147">Close the remote desktop session and use the LCS **Environment details** page to log in to the environment to confirm it is working as expected.</span></span>

![Finance and Operations](./media/10FinanceAndOperations.png)
