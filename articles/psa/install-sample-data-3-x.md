---
title: Установка демонстрационных данных
description: Эта тема предоставляет информацию об установке демонстрационных данных в Project Service Automation.
ms.custom: dyn365-projectservice
ms.date: 11/08/2018
ms.service: project-operations
ms.reviewer: kfend
ms.suite: ''
applies_to: Dynamics 365 Project Service Automation
author: ruhercul
ms.author: ruhercul
search.audienceType: IT Pro, Developer
search.app: ''
ms.openlocfilehash: c521fb4000b4856fc5c2fbf3275bf3b3e0dfa458
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950595"
---
# <a name="sample-data-installation-for-the-project-service-application"></a><span data-ttu-id="73e61-103">Установка демонстрационных данных для приложения Project Service</span><span class="sxs-lookup"><span data-stu-id="73e61-103">Sample data installation for the Project Service application</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="73e61-104">Чтобы помочь вам развить собственные демонстрационные среды, корпорация Microsoft предоставляет загружаемые пакеты демонстрационных данных, которые демонстрируют возможности ваших приложений.</span><span class="sxs-lookup"><span data-stu-id="73e61-104">To help you build your own demo environments, Microsoft provides downloadable sample data packages that showcase the capabilities of your apps.</span></span> <span data-ttu-id="73e61-105">Существует два типа пакетов демонстрационных данных:</span><span class="sxs-lookup"><span data-stu-id="73e61-105">There are two types of sample data packages:</span></span>
- <span data-ttu-id="73e61-106">справочные данные/данные настройки</span><span class="sxs-lookup"><span data-stu-id="73e61-106">reference/setup data</span></span>
- <span data-ttu-id="73e61-107">демонстрационные данные (справочные данные/данные настройки и данные о транзакциях, такие как заказы на работу и проекты)</span><span class="sxs-lookup"><span data-stu-id="73e61-107">demo data (reference/setup and transactional data such as work orders and projects)</span></span>

<span data-ttu-id="73e61-108">Пакеты демонстрационных **справочных** данных доступны для загрузки в трех различных пакетах, поэтому вы можете установить данные только для Project Service или только для Field Service, а также установить демонстрационные данные для обоих приложений одновременно.</span><span class="sxs-lookup"><span data-stu-id="73e61-108">The sample **reference** data packages are downloadable in three different packages, so you can install data only for Project Service, or only for Field Service, or you can install sample data for both applications at once.</span></span>

<span data-ttu-id="73e61-109">К пакетам демонстрационных справочных данных/данных настройки относится:</span><span class="sxs-lookup"><span data-stu-id="73e61-109">The sample setup/reference data packages are:</span></span>

- [<span data-ttu-id="73e61-110">**V902PSMasterData** — только Project Service версии 3.x</span><span class="sxs-lookup"><span data-stu-id="73e61-110">**V902PSMasterData** - Project Service version 3.x only</span></span>](https://go.microsoft.com/fwlink/?linkid=2026540&clcid=0x409)

- [<span data-ttu-id="73e61-111">**V902FSMasterData** — только Field Service версии 8.x</span><span class="sxs-lookup"><span data-stu-id="73e61-111">**V902FSMasterData** - Field Service version 8.x only</span></span>](https://go.microsoft.com/fwlink/?linkid=2026536&clcid=0x409)

- [<span data-ttu-id="73e61-112">**V902FPSMasterData** — Field Service 8.x и Project Service 3.x</span><span class="sxs-lookup"><span data-stu-id="73e61-112">**V902FPSMasterData** - Field Service 8.x and Project Service 3.x</span></span>](https://go.microsoft.com/fwlink/?linkid=2026041&clcid=0x409)

<span data-ttu-id="73e61-113">Последний пакет **демонстрационных** данных:</span><span class="sxs-lookup"><span data-stu-id="73e61-113">The latest **demo** data package is:</span></span>

 - [<span data-ttu-id="73e61-114">**FPSDemoData** — Field Service 8.x и Project Service 3.x</span><span class="sxs-lookup"><span data-stu-id="73e61-114">**FPSDemoData** - Field Service 8.x and Project Service 3.x</span></span>](https://aka.ms/fpsdemodatapackage)

   <span data-ttu-id="73e61-115">Инструкции по установке немного отличаются в разделе создания и настройки, но в остальном аналогичны инструкциям в предыдущей [**записи блога**](https://aka.ms/fpsdemodatablog).</span><span class="sxs-lookup"><span data-stu-id="73e61-115">Installation instructions differ slightly in the users to create and configure section but the rest is the same as in the previous [**blog post**](https://aka.ms/fpsdemodatablog).</span></span> <span data-ttu-id="73e61-116">Этот пакет включает уменьшенный набор демонстрационных данных, и его установка занимает приблизительно 3 часа.</span><span class="sxs-lookup"><span data-stu-id="73e61-116">This package features a reduced demo data set and takes approximately 3 hours to install.</span></span>

<span data-ttu-id="73e61-117">Эти пакеты демонстрационных данных доступны только на английском языке.</span><span class="sxs-lookup"><span data-stu-id="73e61-117">These sample data packages are available in English only.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="73e61-118">**Демонстрационные данные удалить невозможно.**</span><span class="sxs-lookup"><span data-stu-id="73e61-118">**There is no way to uninstall the sample data.**</span></span> <span data-ttu-id="73e61-119">Вы должны устанавливать эти пакеты только в демонстрационных, оценочных, обучающих или тестовых системах.</span><span class="sxs-lookup"><span data-stu-id="73e61-119">You should only install these packages on demonstration, evaluation, training, or test systems.</span></span> <span data-ttu-id="73e61-120">Также обратите внимание, что установка одного отдельного пакета с последующей установкой другого отдельного пакета не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="73e61-120">Also note that installing an individual package, and then installing the other individual package, is not supported.</span></span> <span data-ttu-id="73e61-121">(Иначе говоря, нельзя установить **FSMasterData**, а затем **PSMasterData** или наоборот.) Если вы обнаружите, что требуются демонстрационные данные для обоих приложений в какой-либо момент в будущем, необходимо установить пакет **v902FPSMasterData**.</span><span class="sxs-lookup"><span data-stu-id="73e61-121">(In other words, you can't install **FSMasterData** followed by **PSMasterData**, or vice versa.) If you see yourself needing sample data for both applications at any point in the future, you should install the **v902FPSMasterData** package.</span></span>

<span data-ttu-id="73e61-122">При установке любых пакетов демонстрационных данных, процесс установки выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="73e61-122">When you install any of the sample data packages, the installation process performs the following actions:</span></span>

- <span data-ttu-id="73e61-123">Создание или задание параметров по умолчанию для использования Project Service, Field Service или обоих приложений (если применимо).</span><span class="sxs-lookup"><span data-stu-id="73e61-123">Creates or sets default parameters for using Project Service, Field Service, or both applications (if applicable).</span></span>

- <span data-ttu-id="73e61-124">Импорт демонстрационных данных для приложений, таких как резервируемые ресурсы, специальные роли для приложения, списки цен продажи и себестоимости, подразделения, записи процесса продаж и другие объекты для демонстрации основных возможностей.</span><span class="sxs-lookup"><span data-stu-id="73e61-124">Imports sample data for the applications, such as bookable resources, application-specific roles, sales and cost price lists, organizational units, sales process records, and other entities to demonstrate key capabilities.</span></span>  

<span data-ttu-id="73e61-125">Пакет **демонстрационных данных** включает вышеуказанные и дополнительные данных о транзакциях, такие как заказы на работу и проекты.</span><span class="sxs-lookup"><span data-stu-id="73e61-125">With the **demo data** package, you get the above and additional transactional data such as work orders and projects.</span></span>

<span data-ttu-id="73e61-126">Интересуетесь, какие возможности можно демонстрировать с демонстрационными данными?</span><span class="sxs-lookup"><span data-stu-id="73e61-126">Wondering what capabilities you can demo with the sample data?</span></span> <span data-ttu-id="73e61-127">См. вымышленный сценарий Fabrikam Robotics в разделе [Технические примечания](#technical-notes).</span><span class="sxs-lookup"><span data-stu-id="73e61-127">See the Fabrikam Robotics fictitious scenario in [Technical notes](#technical-notes).</span></span>

<span data-ttu-id="73e61-128">При возникновении вопросов по установке этих пакетов демонстрационных данных [отправьте нами сообщение по электронной почте по адресу fpsdemodata@microsoft.com](mailto:fpsdemodata@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="73e61-128">If you have questions about installing these sample data packages, [send us an email at fpsdemodata@microsoft.com](mailto:fpsdemodata@microsoft.com).</span></span>

## <a name="requirements"></a><span data-ttu-id="73e61-129">Требования</span><span class="sxs-lookup"><span data-stu-id="73e61-129">Requirements</span></span>

<span data-ttu-id="73e61-130">Протокол установки предполагает следующее о данном целевом экземпляре (организации):</span><span class="sxs-lookup"><span data-stu-id="73e61-130">The installation protocol assumes the following about your target instance (org):</span></span>

- <span data-ttu-id="73e61-131">Базовый язык — английский, базовая валюта — доллар США (USD, $).</span><span class="sxs-lookup"><span data-stu-id="73e61-131">Base language is English and base currency is US dollar (USD,$).</span></span>

- <span data-ttu-id="73e61-132">У организации нет данных Project Service или Field Service либо есть только базовые данные по умолчанию, которые идут с любой новой организацией.</span><span class="sxs-lookup"><span data-stu-id="73e61-132">The org has no Project Service or Field Service data already, or only has barebones default data that comes with any new org.</span></span>

- <span data-ttu-id="73e61-133">Правильная версия бизнес-приложения уже установлена:</span><span class="sxs-lookup"><span data-stu-id="73e61-133">The correct version of the business application is already installed:</span></span>
       
    - <span data-ttu-id="73e61-134">**Для FPSDemoData или v902FPSMasterData:** в организации установлены приложения Field Service версии 8.x и Project Service версии 3.x.</span><span class="sxs-lookup"><span data-stu-id="73e61-134">**For FPSDemoData or v902FPSMasterData:** The org has Field Service version 8.x and Project Service version 3.x installed.</span></span>

    - <span data-ttu-id="73e61-135">**Для v902PSMasterData:** в организации установлено приложение Project Service версии 3.x.</span><span class="sxs-lookup"><span data-stu-id="73e61-135">**For v902PSMasterData:** The org has Project Service version 3.x installed.</span></span>

    - <span data-ttu-id="73e61-136">**Для v902FSMasterData:** в организации установлено приложение Field Service версии 8.x.</span><span class="sxs-lookup"><span data-stu-id="73e61-136">**For v902FSMasterData:** The org has Field Service version 8.x installed.</span></span>

> [!NOTE]
> <span data-ttu-id="73e61-137">Если необходимо установить демонстрационные данные поверх существующей пробной или демонстрационной среды Project Service и Field Service, уже содержащие данные (не рекомендуется), потребуется приостановить предварительные проверки безопасности, выполняемые установщиком.</span><span class="sxs-lookup"><span data-stu-id="73e61-137">If you need to install the sample data on top of an existing Project Service and Field Service trial or demo environment that already has data (not recommended), you'll need to suspend the safety prechecks performed by the installer.</span></span> <span data-ttu-id="73e61-138">Дополнительные сведения см. в технических замечаниях ниже.</span><span class="sxs-lookup"><span data-stu-id="73e61-138">For more information, see the technical notes below.</span></span>

## <a name="prepare-for-installation"></a><span data-ttu-id="73e61-139">Подготовка к установке</span><span class="sxs-lookup"><span data-stu-id="73e61-139">Prepare for installation</span></span>

<span data-ttu-id="73e61-140">Требуется запустить программу установки на компьютере с последней версией Windows (предпочтительно Windows 10).</span><span class="sxs-lookup"><span data-stu-id="73e61-140">You need to run the installer on a computer with a recent version of Windows (Windows 10 preferred).</span></span>

<span data-ttu-id="73e61-141">Необходимо запланировать для компьютера оставаться на связи с сетью и для установки **справочных данных/данных настройки** установить время выполнения **1 час**.</span><span class="sxs-lookup"><span data-stu-id="73e61-141">You should plan for the computer to remain connected to a network, and for the installation to run for up to **1 hour** for **setup/reference data**.</span></span> <span data-ttu-id="73e61-142">(Обычно установка занимает около 30 минут для пакета **FPSMasterData**, содержащего демонстрационные данные для обоих приложений.) Установка **FPSDemoData** займет приблизительно **3 часа**.</span><span class="sxs-lookup"><span data-stu-id="73e61-142">(Normally the installation takes around 30 minutes for **FPSMasterData**, which includes sample data for both applications.) For the **FPSDemoData**, the installation will take around **3 hours**.</span></span>

<span data-ttu-id="73e61-143">На компьютере должна быть отключена функция заставки экрана.</span><span class="sxs-lookup"><span data-stu-id="73e61-143">The computer should have the screen saver function turned off.</span></span> <span data-ttu-id="73e61-144">В противном случае учетные данные сеанса для установки могут быть потеряны при включении заставки (если не будет сохраняться сеанс активным).</span><span class="sxs-lookup"><span data-stu-id="73e61-144">Otherwise, session credentials for the installation may be lost when the screen saver engages (unless you keep your session active throughout).</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="73e61-145">![Снимок экрана настроек заставки экрана, когда заставка отключена](media/sample-data-1.png)</span><span class="sxs-lookup"><span data-stu-id="73e61-145">![Screenshot of screen saver settings, with screen saver turned off](media/sample-data-1.png)</span></span>

## <a name="download-and-unpack"></a><span data-ttu-id="73e61-146">Загрузка и распаковка</span><span class="sxs-lookup"><span data-stu-id="73e61-146">Download and unpack</span></span>

<span data-ttu-id="73e61-147">Установщик демонстрационных данных Project Service и Field Service распространяется как самораспаковывающийся исполнимый файл.</span><span class="sxs-lookup"><span data-stu-id="73e61-147">The Project Service and Field Service sample data installer is distributed as a self-extracting executable.</span></span> <span data-ttu-id="73e61-148">Имена файлов могут отличаться в зависимости от пакета демонстрационных данных, но в остальном шаги совпадают независимо от устанавливаемого пакета.</span><span class="sxs-lookup"><span data-stu-id="73e61-148">The file names may vary depending on the sample data package, but otherwise the steps are the same no matter which package you install.</span></span>

<span data-ttu-id="73e61-149">После загрузки пакета запустите EXE-файл, затем примите условия для распаковки сжатого ZIP-файла.</span><span class="sxs-lookup"><span data-stu-id="73e61-149">After downloading a package, run the .exe file, and then accept terms and conditions to unpack the compressed zip file.</span></span> <span data-ttu-id="73e61-150">Затем требуется извлечь содержимое файла в папку на компьютере.</span><span class="sxs-lookup"><span data-stu-id="73e61-150">You then need to extract contents of that file to a folder on the computer.</span></span>

<span data-ttu-id="73e61-151">В зависимости от используемой операционной системы и параметров безопасности, можно выполнить следующие действия после распаковки ZIP-файла:</span><span class="sxs-lookup"><span data-stu-id="73e61-151">Depending on the operating system and security settings, you may need to perform the following steps after unpacking the zip file:</span></span>

1. <span data-ttu-id="73e61-152">Найдите и щелкните правой кнопкой мыши файл **FPSDemoData.dll** в папке **v902FPSMasterData** / **PackageDeployer_FPSDemoData**.</span><span class="sxs-lookup"><span data-stu-id="73e61-152">Find and right-click the **FPSDemoData.dll** file in the **v902FPSMasterData** / **PackageDeployer_FPSDemoData** folder.</span></span>

2. <span data-ttu-id="73e61-153">Выберите **Разблокировать**.</span><span class="sxs-lookup"><span data-stu-id="73e61-153">Choose **Unblock**.</span></span>

3. <span data-ttu-id="73e61-154">Выберите **Применить**.</span><span class="sxs-lookup"><span data-stu-id="73e61-154">Select **Apply**.</span></span>

4. <span data-ttu-id="73e61-155">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="73e61-155">Select **OK**.</span></span>


## <a name="create-or-configure-users"></a><span data-ttu-id="73e61-156">Создание и настройка пользователей</span><span class="sxs-lookup"><span data-stu-id="73e61-156">Create or configure users</span></span>

<span data-ttu-id="73e61-157">Пакету **FPSDemoData** требуется шесть пользователей, а пакету **FPSMasterData** — один.</span><span class="sxs-lookup"><span data-stu-id="73e61-157">The **FPSDemoData** package requires six users while **FPSMasterData** packages require one user.</span></span> <span data-ttu-id="73e61-158">См. правильный пакет демонстрационных данных.</span><span class="sxs-lookup"><span data-stu-id="73e61-158">Refer to the correct one for your sample data package.</span></span>

## <a name="create-or-configure-users---setupreference-data-packages"></a><span data-ttu-id="73e61-159">Создание и настройка пользователей — пакеты справочных данных/данных настройки</span><span class="sxs-lookup"><span data-stu-id="73e61-159">Create or configure users - setup/reference data packages</span></span>

<span data-ttu-id="73e61-160">Пакет **FPSMasterData** предназначен для установки с одним пользователем с именем Spencer Low с описанными здесь настройками.</span><span class="sxs-lookup"><span data-stu-id="73e61-160">The **FPSMasterData** package is designed to install with one user named Spencer Low with the settings described here.</span></span> <span data-ttu-id="73e61-161">Для правильной установки пакета необходимо создать (либо временно переименовать) пользователей в среде в соответствии с конфигурацией входящих демонстрационных данных.</span><span class="sxs-lookup"><span data-stu-id="73e61-161">To install the package correctly, you need to create (or temporarily rename) users in your environment to match the incoming sample data configuration.</span></span>

<span data-ttu-id="73e61-162">Чтобы создать или настроить пользователей, перейдите в раздел **Параметры** > **Безопасность** > **Пользователи**, и выполните следующее:</span><span class="sxs-lookup"><span data-stu-id="73e61-162">To create or configure users, go to **Settings** > **Security** > **Users**, and do the following:</span></span>

1. <span data-ttu-id="73e61-163">Задайте UserFullname="Spencer Low" с именем пользователя "spencerl" (**в нижнем регистре**) для ролей руководителя проекта и руководителя по методикам.</span><span class="sxs-lookup"><span data-stu-id="73e61-163">Set UserFullname="Spencer Low" with username "spencerl" (**lowercase**) to the Project Manager and Practice Manager roles.</span></span>

2. <span data-ttu-id="73e61-164">Выберите пользователя **Spencer Low** и щелкните **Управление ролями**.</span><span class="sxs-lookup"><span data-stu-id="73e61-164">Select the **Spencer Low** user, and then select **Manage Roles**.</span></span> <span data-ttu-id="73e61-165">Найдите и выберите роль **Системный администратор**, а затем выберите **ОК** для предоставления полных прав администратора пользователю Spencer Low.</span><span class="sxs-lookup"><span data-stu-id="73e61-165">Find and select the **System Administrator** role, and then select **OK** to grant full admin rights to Spencer Low.</span></span> <span data-ttu-id="73e61-166">Этот шаг необходим для обеспечения того, что демонстрационные записи создаются с правильным типом собственности пользователя и, поэтому, заполняют представления правильно.</span><span class="sxs-lookup"><span data-stu-id="73e61-166">This step is necessary to ensure that sample records are created with the correct user ownership and therefore populate views correctly.</span></span>

3. <span data-ttu-id="73e61-167">Из загруженного пакета необходимо обновить файл сопоставления данных с адресами электронной почты контекста пользователя по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="73e61-167">From the downloaded package, you need to update a data mapping file with email addresses of the default user context.</span></span> <span data-ttu-id="73e61-168">Для этого откройте папку **PkgFolder**, затем найдите и откройте файл **ImportUserMapFile.xml** в Блокноте (или в Visual Studio или другом редакторе XML).</span><span class="sxs-lookup"><span data-stu-id="73e61-168">To do this, open **PkgFolder**, and then find and open the **ImportUserMapFile.xml** file in Notepad (or Visual Studio or another XML editor).</span></span> <span data-ttu-id="73e61-169">Задайте в поле **DefaultUserToMapTo=** адрес электронной почты пользователя Spencer Low.</span><span class="sxs-lookup"><span data-stu-id="73e61-169">Set the **DefaultUserToMapTo=** field to the email address of the Spencer Low user.</span></span>

4. <span data-ttu-id="73e61-170">Если вы не используете пользователя Spencer Low с именем пользователя **spencerl**, необходимо обновить дополнительный файл.</span><span class="sxs-lookup"><span data-stu-id="73e61-170">If you aren't using Spencer Low with username **spencerl**, you need to update an additional file.</span></span> <span data-ttu-id="73e61-171">Откройте файл **DemoDataPreImportConfig.xml**, затем найдите тег **userstocreateandconfigure**.</span><span class="sxs-lookup"><span data-stu-id="73e61-171">Open the **DemoDataPreImportConfig.xml** file, and then find the **userstocreateandconfigure** tag.</span></span> <span data-ttu-id="73e61-172">Обновите тег **\<login\>** с использованием имени пользователя вашего пользователя Spencer Low.</span><span class="sxs-lookup"><span data-stu-id="73e61-172">Update the **\<login\>** tag with the username of your Spencer Low user.</span></span> <span data-ttu-id="73e61-173">Дополнительные сведения см. в разделе [Технические примечания](#technical-notes).</span><span class="sxs-lookup"><span data-stu-id="73e61-173">For additional details, see [Technical notes](#technical-notes).</span></span>

## <a name="create-or-configure-users---demo-data-package"></a><span data-ttu-id="73e61-174">Создание и настройка пользователей — пакет демонстрационных данных</span><span class="sxs-lookup"><span data-stu-id="73e61-174">Create or configure users - demo data package</span></span>

<span data-ttu-id="73e61-175">Пакету демонстрационных данных требуется шесть пользователей.</span><span class="sxs-lookup"><span data-stu-id="73e61-175">The demo data package requires six users.</span></span> <span data-ttu-id="73e61-176">Для правильной установки пакета выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="73e61-176">For the package to install correctly, do the following:</span></span>

 1. <span data-ttu-id="73e61-177">Создайте или временно переименуйте существующих пользователей для соответствия конфигурации входящих демонстрационных данных, перейдя в раздел **Параметры** > **Безопасность** > **Пользователи**.</span><span class="sxs-lookup"><span data-stu-id="73e61-177">Create or temporarily rename existing users to match incoming sample data configuration by going to **Settings** > **Security** > **Users**.</span></span>
 
    <span data-ttu-id="73e61-178">Эти роли необходимые только для демонстраций, основанных на личностях.</span><span class="sxs-lookup"><span data-stu-id="73e61-178">These roles are only needed for persona-based demos.</span></span>  
    - <span data-ttu-id="73e61-179">User Fullname="David So" — техник Field Service</span><span class="sxs-lookup"><span data-stu-id="73e61-179">User Fullname="David So" as Field Service Technician</span></span>   
    - <span data-ttu-id="73e61-180">User Fullname="Jamie Reding" — диспетчер Customer Service и Field Service</span><span class="sxs-lookup"><span data-stu-id="73e61-180">User Fullname="Jamie Reding" as Customer Service & Field Service Dispatcher</span></span>   
    - <span data-ttu-id="73e61-181">User Fullname="Molly Clark" — менеджер по работе с клиентами</span><span class="sxs-lookup"><span data-stu-id="73e61-181">User Fullname="Molly Clark" as Account Manager</span></span>   
    - <span data-ttu-id="73e61-182">User Fullname="Spencer Low" — руководитель по методикам и руководитель проекта</span><span class="sxs-lookup"><span data-stu-id="73e61-182">User Fullname="Spencer Low" as Practice and Project Manager</span></span>  
    - <span data-ttu-id="73e61-183">User Fullname="Veronica Quek" — участник рабочей группы</span><span class="sxs-lookup"><span data-stu-id="73e61-183">User Fullname="Veronica Quek" as Team Member</span></span>   
    - <span data-ttu-id="73e61-184">User Fullname="William Contoso"</span><span class="sxs-lookup"><span data-stu-id="73e61-184">User Fullname="William Contoso"</span></span>
  
2. <span data-ttu-id="73e61-185">Для импорта демонстрационных данных назначьте шести пользователям выше роль "Администратор" для правильного импорта примеров записей.</span><span class="sxs-lookup"><span data-stu-id="73e61-185">For the purposes of demo data import, assign the six users above the Administrator role so sample records import correctly.</span></span> 

3. <span data-ttu-id="73e61-186">Откройте **PkgFolder**, затем найдите и откройте **ImportUserMapFile.xml**.</span><span class="sxs-lookup"><span data-stu-id="73e61-186">Open **PkgFolder** and then find and open **ImportUserMapFile.xml**.</span></span> <span data-ttu-id="73e61-187">Обновите поля **Создать=** для добавления адресов электронной почты соответствующих пользователей в системе.</span><span class="sxs-lookup"><span data-stu-id="73e61-187">Update the **New=** fields to the email addresses of corresponding Users in your system.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="73e61-188">![Снимок экрана UserMapFile](media/sample-data-7.png)</span><span class="sxs-lookup"><span data-stu-id="73e61-188">![Screen shot of UserMapFile](media/sample-data-7.png)</span></span>

4. <span data-ttu-id="73e61-189">Если полное имя пользователя "Spencer Low" имеет идентификатор пользователя, отличный от **spencerl**, необходимо обновить дополнительный файл.</span><span class="sxs-lookup"><span data-stu-id="73e61-189">If your "Spencer Low" full name user has a different user ID than **"spencerl"**, then you need to update an additional file.</span></span> <span data-ttu-id="73e61-190">Откройте **DemoDataPreImportConfig.xml** и найдите тег **userstocreateandconfigure**.</span><span class="sxs-lookup"><span data-stu-id="73e61-190">Open **DemoDataPreImportConfig.xml** and find the **userstocreateandconfigure** tag.</span></span> <span data-ttu-id="73e61-191">Обновите тег **\<login\>** для отображения loginId (с учетом регистра).</span><span class="sxs-lookup"><span data-stu-id="73e61-191">Update the **\<login\>** tag with the loginId (case-sensitive).</span></span> 

5. <span data-ttu-id="73e61-192">Календарь первого пользователя (в теге **userstocreateandconfigure** tag) используется для автоматического заполнения рабочих часов для всех резервируемых ресурсов при импорте демонстрационных данных.</span><span class="sxs-lookup"><span data-stu-id="73e61-192">The first user's calendar (in the **userstocreateandconfigure** tag) is used to populate the work hours for all bookable resources on import of demo data.</span></span> <span data-ttu-id="73e61-193">Перейдите в раздел **Параметры** > **Безопасность** > **Пользователи**, найдите пользователя "Spencer Low" и откройте параметр "Рабочие часы".</span><span class="sxs-lookup"><span data-stu-id="73e61-193">Navigate to **Settings** > **Security** > **Users**, find your "Spencer Low" user, and open the "Work Hours" option.</span></span> <span data-ttu-id="73e61-194">Измените существующие рабочие часы, выбрав параметр **Весь недельный цикл с начала до конца**.</span><span class="sxs-lookup"><span data-stu-id="73e61-194">Edit the existing work hours, selecting the **Entire recurring weekly schedule from start to end** option.</span></span> <span data-ttu-id="73e61-195">Убедитесь, что **для рабочих часов задан период с 8:00 до 17:00 (9 часов), с понедельника по пятницу, и что задан часовой пояс "Тихоокеанское время (США и Канада)"**.</span><span class="sxs-lookup"><span data-stu-id="73e61-195">Ensure the **Work hours are set to 8 AM - 5 PM (9 Hours), Monday to Friday and with the Timezone set to Pacific Time (US & Canada)**.</span></span> <span data-ttu-id="73e61-196">Это необходимо для обеспечения правильного отображения таблицы расписаний и проекта.</span><span class="sxs-lookup"><span data-stu-id="73e61-196">This is needed to ensure that the Project and Schedule board show as expected.</span></span>

<span data-ttu-id="73e61-197">**Рекомендация.** Рекомендуется создать резервную копию вашей организации теперь, в случае если будет необходимо вернуться к отправной точке, если что-либо пойдет не так во время установки демонстрационных данных.</span><span class="sxs-lookup"><span data-stu-id="73e61-197">**Recommendation:** Consider creating a backup of your org now, in case you need to revert to your starting point if something goes wrong during the sample data installation.</span></span> <span data-ttu-id="73e61-198">Дополнительные сведения см. в разделе [Резервное копирование и восстановление экземпляров](/dynamics365/customer-engagement/admin/backup-restore-instances).</span><span class="sxs-lookup"><span data-stu-id="73e61-198">For more information, see [Backup and restore instances](/dynamics365/customer-engagement/admin/backup-restore-instances).</span></span>

## <a name="run-the-package-deployer"></a><span data-ttu-id="73e61-199">Запустите Package Deployer</span><span class="sxs-lookup"><span data-stu-id="73e61-199">Run the Package Deployer</span></span>

1. <span data-ttu-id="73e61-200">Найдите и запустите файл **PackageDeployer.exe** в папке **v902FPSMasterData** ИЛИ **PackageDeployer_FPSDemoData**.</span><span class="sxs-lookup"><span data-stu-id="73e61-200">Find and run **PackageDeployer.exe** in the **v902FPSMasterData** OR **PackageDeployer_FPSDemoData** folder.</span></span>

2. <span data-ttu-id="73e61-201">Примите условия соглашения.</span><span class="sxs-lookup"><span data-stu-id="73e61-201">Accept the terms and conditions.</span></span>

3. <span data-ttu-id="73e61-202">В следующем окне:</span><span class="sxs-lookup"><span data-stu-id="73e61-202">On the next window:</span></span>

   <span data-ttu-id="73e61-203">a.</span><span class="sxs-lookup"><span data-stu-id="73e61-203">a.</span></span> <span data-ttu-id="73e61-204">Выберите тип развертывания **Office 365**.</span><span class="sxs-lookup"><span data-stu-id="73e61-204">Select deployment type **Office 365**.</span></span>

   <span data-ttu-id="73e61-205">b.</span><span class="sxs-lookup"><span data-stu-id="73e61-205">b.</span></span> <span data-ttu-id="73e61-206">Используйте имя пользователя и пароль пользователя системного администратора, настроенный в разделе "Создание или настройка пользователей" ("Spencer Low" с именем пользователя "spencerl").</span><span class="sxs-lookup"><span data-stu-id="73e61-206">Use the user and password of the system administrator user configured in "Create or configure users" ("Spencer Low" with "spencerl" username).</span></span>

   <span data-ttu-id="73e61-207">c.</span><span class="sxs-lookup"><span data-stu-id="73e61-207">c.</span></span> <span data-ttu-id="73e61-208">Убедитесь, что установлен флажок **Отображать список доступных организаций**.</span><span class="sxs-lookup"><span data-stu-id="73e61-208">Make sure **Display list of available organizations** is selected.</span></span>

      > [!div class="mx-imgBorder"]
      > <span data-ttu-id="73e61-209">![Снимок экрана окна Package Deployer с установленным флажком "Отображать список доступных организаций"](media/sample-data-2.png)</span><span class="sxs-lookup"><span data-stu-id="73e61-209">![Screenshot of Package Deployer window with "Display list of available organizations" selected](media/sample-data-2.png)</span></span>

4. <span data-ttu-id="73e61-210">Выберите организацию, в которую требуется установить демонстрационные данные.</span><span class="sxs-lookup"><span data-stu-id="73e61-210">Select the organization where you want to install the sample data.</span></span>

5. <span data-ttu-id="73e61-211">Выберите **Далее**, пока не увидите диалог **Настройка демонстрационных данных**.</span><span class="sxs-lookup"><span data-stu-id="73e61-211">Select **Next** until you see the **Demo Data Setup** dialog.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="73e61-212">![Снимок экрана окна состояния установщика демонстрационных данных](media/sample-data-3.png)</span><span class="sxs-lookup"><span data-stu-id="73e61-212">![Screenshot of the demo data installer status window](media/sample-data-3.png)</span></span>

6. <span data-ttu-id="73e61-213">Перед тем как продолжить, обратите внимание, что установка демонстрационных данных может занять до одного часа (обычно ~10 минут).</span><span class="sxs-lookup"><span data-stu-id="73e61-213">Before proceeding, note that installing sample data could take up to one hour (normally ~10 minutes).</span></span> <span data-ttu-id="73e61-214">Необходимо убедиться, что компьютер остается соединенным с сетью в течение процесса установки, и что сеанс остается активным.</span><span class="sxs-lookup"><span data-stu-id="73e61-214">You'll need to make sure the computer remains on and connected to a network throughout the installation process, and that your session remains active.</span></span>   

7. <span data-ttu-id="73e61-215">Когда будете готовы, нажмите кнопку **Далее**, чтобы начать процесс установки демонстрационных данных.</span><span class="sxs-lookup"><span data-stu-id="73e61-215">When you're ready, click **Next** to start the sample data installation process.</span></span> <span data-ttu-id="73e61-216">После загрузки демонстрационных данных щелкните **Готово**.</span><span class="sxs-lookup"><span data-stu-id="73e61-216">After the sample data is loaded, click **Finish**.</span></span>

## <a name="verify-the-sample-data-installation"></a><span data-ttu-id="73e61-217">Проверка установки демонстрационных данных</span><span class="sxs-lookup"><span data-stu-id="73e61-217">Verify the sample data installation</span></span>

<span data-ttu-id="73e61-218">Для проверки работоспособности убедитесь, что количество записей и типов объектов, перечисленных в вымышленном сценарии Fabrikam Robotics отображаются правильным образом.</span><span class="sxs-lookup"><span data-stu-id="73e61-218">For a sanity check, verify that the number of records and types of entities listed in Fabrikam Robotics fictitious scenario appear as expected.</span></span>

<span data-ttu-id="73e61-219">После полной загрузки демонстрационных данных войдите в систему как пользователь Spencer Low и убедитесь в следующем:</span><span class="sxs-lookup"><span data-stu-id="73e61-219">After the sample data completely loads, sign in as the Spencer Low user and confirm the following:</span></span>

- <span data-ttu-id="73e61-220">Если приложение Project Service установлено, перейдите в раздел **Project Service** > **Параметры** > **Прайс-листы**.</span><span class="sxs-lookup"><span data-stu-id="73e61-220">If the Project Service application is installed, go to **Project Service** > **Settings** > **Price Lists**.</span></span> <span data-ttu-id="73e61-221">Убедитесь, что ставки по счету и ставки стоимости существуют с соответствующей валютой для каждой страны/региона в наборе данных.</span><span class="sxs-lookup"><span data-stu-id="73e61-221">Confirm that bill rates and costs rates exist with the appropriate currency for each country/region in the data set.</span></span>

- <span data-ttu-id="73e61-222">Если приложение Project Service установлено, перейдите в раздел **Universal Resource Scheduling** > **Параметры** > **Подразделения**.</span><span class="sxs-lookup"><span data-stu-id="73e61-222">If the Project Service application is installed, go to **Universal Resource Scheduling** > **Settings** > **Organizational Units**.</span></span> <span data-ttu-id="73e61-223">Убедитесь, что список себестоимости с соответствующей валютой был связан с каждой организационно единицей (исключая записи городов).</span><span class="sxs-lookup"><span data-stu-id="73e61-223">Confirm that a cost price list with the appropriate currency has been associated with each org unit (excluding city entries).</span></span> <span data-ttu-id="73e61-224">Если какие-либо отсутствуют, найдите и свяжите правильный список себестоимости.</span><span class="sxs-lookup"><span data-stu-id="73e61-224">If any are missing, find and associate the correct cost price list.</span></span>

- <span data-ttu-id="73e61-225">Если приложение Field Service установлено, перейдите в раздел **Project Service** > **Параметры** > **Прайс-листы**.</span><span class="sxs-lookup"><span data-stu-id="73e61-225">If the Field Service application is installed, go to **Project Service** > **Settings** > **Price Lists**.</span></span> <span data-ttu-id="73e61-226">Убедитесь, что ставки по счету и ставки стоимости существуют.</span><span class="sxs-lookup"><span data-stu-id="73e61-226">Confirm that bill rates and costs rates exist.</span></span> <span data-ttu-id="73e61-227">Перейдите в раздел **Field Service** > **Параметры** > **Прайс-листы** и проверьте, что ставки по счету и ставки стоимости существуют, с соответствующей валютой, для каждой требуемой страны/региона в наборе данных.</span><span class="sxs-lookup"><span data-stu-id="73e61-227">Go to **Field Service** > **Settings** > **Price Lists** and check that bill rates and costs rates exist, with the appropriate currency, for each country/region in the data set.</span></span>

  > [!div class="mx-imgBorder"]
  > <span data-ttu-id="73e61-228">![Снимок экрана активных прайс-листов](media/sample-data-4.png)</span><span class="sxs-lookup"><span data-stu-id="73e61-228">![Screenshot of active price lists](media/sample-data-4.png)</span></span>

  > [!div class="mx-imgBorder"]
  > <span data-ttu-id="73e61-229">![Снимок экрана активных подразделений](media/sample-data-5.png)</span><span class="sxs-lookup"><span data-stu-id="73e61-229">![Screenshot of active organizational units](media/sample-data-5.png)</span></span>

## <a name="technical-notes"></a><span data-ttu-id="73e61-230">Технические примечания</span><span class="sxs-lookup"><span data-stu-id="73e61-230">Technical notes</span></span>

<span data-ttu-id="73e61-231">См. ниже дополнительные технические сведения по установке этих данных.</span><span class="sxs-lookup"><span data-stu-id="73e61-231">See below for more technical details on the installation of this data.</span></span>

### <a name="installing-sample-data-on-top-of-existing-data-not-recommended"></a><span data-ttu-id="73e61-232">Установка демонстрационных данных поверх существующих данных (не рекомендуется)</span><span class="sxs-lookup"><span data-stu-id="73e61-232">Installing sample data on top of existing data (not recommended)</span></span>

<span data-ttu-id="73e61-233">Если необходимо установить демонстрационные данные поверх существующей пробной или демонстрационной среды Field Service или Project Service, уже содержащие данные, потребуется приостановить предварительные проверки безопасности, выполняемые установщиком.</span><span class="sxs-lookup"><span data-stu-id="73e61-233">If you need to install sample data on top of an existing Field Service or Project Service trial or demo environment that already has data, you'll need to suspend the safety prechecks performed by the installer.</span></span>

<span data-ttu-id="73e61-234">Для этого откройте папку **PkgFolder**, чтобы найти и открыть файл **DemoDataPreImportConfig.xml** в Блокноте (или в другом редакторе XML).</span><span class="sxs-lookup"><span data-stu-id="73e61-234">To do this, go to the **PkgFolder** folder to find and open the **DemoDataPreImportConfig.xml** file with Notepad (or another XML editor).</span></span>

<span data-ttu-id="73e61-235">Найдите следующее значение, а затем измените параметр с True на False:</span><span class="sxs-lookup"><span data-stu-id="73e61-235">Find the following value, and then change the setting from true to false:</span></span>

```alias
<TerminateOnPreCheckFailure>true</TerminateOnPreCheckFailure>
```

<span data-ttu-id="73e61-236">Это изменение заставляет установщик обходить некоторые важные проверки безопасности, в том числе:</span><span class="sxs-lookup"><span data-stu-id="73e61-236">This change causes the installer to bypass some important safety checks, including:</span></span>

- <span data-ttu-id="73e61-237">Проверка, что имеется не более одной активной записи **Подразделение**, а затем переименование ее в **Fabrikam US**.</span><span class="sxs-lookup"><span data-stu-id="73e61-237">Confirming that there is no more than one active **Organizational Unit** record, and then renaming it to **Fabrikam US**.</span></span>

- <span data-ttu-id="73e61-238">Проверка, что имеется не более одной активной записи **Рабочий шаблон**.</span><span class="sxs-lookup"><span data-stu-id="73e61-238">Confirming that there is no more than one active **Work Template** record.</span></span>

- <span data-ttu-id="73e61-239">Проверка, что имеется не более одной активной записи **Параметр проекта**, а затем переименование ее в **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="73e61-239">Confirming that there is no more than one active **Project Parameter** record, and then renaming that entry to **Parameters**.</span></span>

### <a name="configuration-components"></a><span data-ttu-id="73e61-240">Компоненты конфигурации</span><span class="sxs-lookup"><span data-stu-id="73e61-240">Configuration components</span></span>

<span data-ttu-id="73e61-241">Имеется несколько других компонентов конфигурации в этом файле конфигурации перед импортом.</span><span class="sxs-lookup"><span data-stu-id="73e61-241">There are a number of other configuration components in this pre-import configuration file.</span></span> <span data-ttu-id="73e61-242">Для технических пользователей некоторые из них включают:</span><span class="sxs-lookup"><span data-stu-id="73e61-242">For technical users, some of these include:</span></span>

- <span data-ttu-id="73e61-243">**\<RequiredSolutions\>** указывает обязательные предварительные установки решений и номера их версий.</span><span class="sxs-lookup"><span data-stu-id="73e61-243">**\<RequiredSolutions\>** specifies prerequisite solution installations and their version numbers.</span></span>

- <span data-ttu-id="73e61-244">**\<InstallSampleData\>** управляет тем, установлены ли готовые демонстрационные данные для приложений.</span><span class="sxs-lookup"><span data-stu-id="73e61-244">**\<InstallSampleData\>** controls whether out-of-the-box sample data for the apps is installed.</span></span>

    - <span data-ttu-id="73e61-245">false — установка этих встроенных данных пропускается (что может быть удалено).</span><span class="sxs-lookup"><span data-stu-id="73e61-245">false - skips installation of this built-in data (which is removable)</span></span>

    - <span data-ttu-id="73e61-246">true — установка встроенных данных одновременно с установкой демонстрационных данных FS и PSA</span><span class="sxs-lookup"><span data-stu-id="73e61-246">true - installs the built-in data concurrent with installation of the FS and PSA sample data</span></span>

- <span data-ttu-id="73e61-247">**\<PreImportDataCollection\>** указывает плоский файл сопоставления данных и связанные записи, которые следует импортировать перед установкой основных демонстрационных данных.</span><span class="sxs-lookup"><span data-stu-id="73e61-247">**\<PreImportDataCollection\>** specifies flat-file Data Maps and associated Records to be imported ahead of the main sample data installation.</span></span>

- <span data-ttu-id="73e61-248">**\<EntitiesToEnableScheduling\>** указывает, какие объекты необходимо включить для резервирования в Microsoft Dynamics Scheduling (также называется Universal Resource Scheduling).</span><span class="sxs-lookup"><span data-stu-id="73e61-248">**\<EntitiesToEnableScheduling\>** specifies which entities should be enabled for Booking in Microsoft Dynamics Scheduling (aka Universal Resource Scheduling).</span></span>

- <span data-ttu-id="73e61-249">**\<UsersToCreateAndConfigure\>** указывает резервируемые ресурсы, которые будут созданы (если они еще не существуют) перед выполнением импорта демонстрационных данных.</span><span class="sxs-lookup"><span data-stu-id="73e61-249">**\<UsersToCreateAndConfigure\>** specifies Bookable Resources that will be created (if they don't exist already) before the sample data import executes.</span></span> <span data-ttu-id="73e61-250">Обратите внимание, что резервируемые ресурсы демонстрационных данных исходной системы соответствуют записям резервируемого ресурса целевой системы по FullName и данным для входа каждого из ресурсов.</span><span class="sxs-lookup"><span data-stu-id="73e61-250">Note that the source system sample data Bookable Resource match with the target system Bookable Resource records on the FullName and login of each resource.</span></span> <span data-ttu-id="73e61-251">Поэтому НЕВОЗМОЖНО изменить имена в этом файле предварительной конфигурации, если только не импортировать сначала демонстрационные данные в целевую систему с использованием этих имен, а затем переименовать резервируемые ресурсы на предпочитаемый вами набор имен вместе с записями разрешенных пользователей, а затем экспортировать данные снова для импорта в вашу окончательную целевую систему (с обновлением старых и новых записей **ImportUserMapFile.xml** соответственно).</span><span class="sxs-lookup"><span data-stu-id="73e61-251">Therefore, it is NOT possible to change the names in this preconfiguration file unless you first import sample data into a target system using these names, then rename the Bookable Resources to your desired name set along with the Enabled User records, and then export the data again for import into your final destination system (updating the **ImportUserMapFile.xml** Old and New entries accordingly).</span></span>

- <span data-ttu-id="73e61-252">**\<PluginsToDisable\>** указывает очень специальные подключаемые модули товаров строки, которых следует отключить при импорте демонстрационных данных, а затем снова включить.</span><span class="sxs-lookup"><span data-stu-id="73e61-252">**\<PluginsToDisable\>** specifies very discrete line-item plug-ins that must be disabled during the sample data import and then reenabled afterwards.</span></span>

### <a name="fabrikam-robotics-fictitious-scenario"></a><span data-ttu-id="73e61-253">Вымышленный сценарий Fabrikam Robotics</span><span class="sxs-lookup"><span data-stu-id="73e61-253">Fabrikam Robotics fictitious scenario</span></span>

<span data-ttu-id="73e61-254">Пакеты демонстрационных справочных данных Field Service и Project Service устанавливают **Решение Fabrikam Manufacturing Master Data (v3.0.0.0)** вместе с приблизительно 4000 записей и приблизительно 40 различными объектами.</span><span class="sxs-lookup"><span data-stu-id="73e61-254">The Field Service and Project Service sample reference data packages install the **Fabrikam Manufacturing Master Data (v3.0.0.0) solution**, along with approximately 4,000 records and approximately 40 different entities.</span></span> <span data-ttu-id="73e61-255">Отдельные пакеты демонстрационных данных для Field Service или Project Service содержат подмножество демонстрационных данных **v902FPSMasterData** для данного приложения.</span><span class="sxs-lookup"><span data-stu-id="73e61-255">The separate sample data packages for Field Service or Project Service contain a subset of the **v902FPSMasterData** sample data for that application.</span></span> <span data-ttu-id="73e61-256">Пакет **Демонстрационные данные** устанавливает **Решение Fabrikam Manufacturing Demo Data (v3.0.0.7)** вместе с приблизительно 22 000 записей в 148 объектах.</span><span class="sxs-lookup"><span data-stu-id="73e61-256">The **Demo Data** package installs the **Fabrikam Manufacturing Demo Data (v3.0.0.7) solution** with approximately 22,000 records across 148 entities.</span></span>

<span data-ttu-id="73e61-257">Выдуманная компания Fabrikam Robotics является производителем роботов сборочного конвейера электронных устройств и известна качеством своей продукции, инновациями и хорошим обслуживанием клиентов, включая планирование монтажа, внедрение и услуги по текущему обслуживанию.</span><span class="sxs-lookup"><span data-stu-id="73e61-257">The fictional company, Fabrikam Robotics, is a manufacturer of electronic device assembly line robots and is known for their product quality, innovation, and solid customer service, including installation planning, implementation, and ongoing maintenance services.</span></span> <span data-ttu-id="73e61-258">Штаб-квартира Fabrikam размещена в США (Fabrikam US), и имеются основанное на проектах сервисное обслуживание во Франции, Индии, Великобритании и Швейцарии.</span><span class="sxs-lookup"><span data-stu-id="73e61-258">Fabrikam is headquartered in the United States (Fabrikam US), and has project-based service operations in France, India, the United Kingdom, and Switzerland.</span></span>

<span data-ttu-id="73e61-259">Операции выездного обслуживания сосредоточены в США, в основном в области большого Сиетла.</span><span class="sxs-lookup"><span data-stu-id="73e61-259">Field service operations are centered in the United States, mostly in the greater Seattle area.</span></span> <span data-ttu-id="73e61-260">Компания сфокусирована на использовании подключений интернета вещей (IoT) для контроля работы активов клиентов и предоставления все более упреждающих услуг на месте.</span><span class="sxs-lookup"><span data-stu-id="73e61-260">The company is focused on leveraging Internet of Things (IoT) connectivity to monitor customer asset performance and deliver increasingly proactive onsite services.</span></span>

<span data-ttu-id="73e61-261">Общий обзор высокого уровня демонстрационных данных выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="73e61-261">A high-level overview of the sample data is as follows:</span></span>

- <span data-ttu-id="73e61-262">Общие элементы демонстрационных данных (включены для обоих приложений)</span><span class="sxs-lookup"><span data-stu-id="73e61-262">Common sample data elements (included for both applications)</span></span>

    - <span data-ttu-id="73e61-263">1 пользователь</span><span class="sxs-lookup"><span data-stu-id="73e61-263">1 user</span></span>

    - <span data-ttu-id="73e61-264">71 учетная запись</span><span class="sxs-lookup"><span data-stu-id="73e61-264">71 accounts</span></span>

    - <span data-ttu-id="73e61-265">137 контактов</span><span class="sxs-lookup"><span data-stu-id="73e61-265">137 contacts</span></span>

    - <span data-ttu-id="73e61-266">Разные типы транзакций и категорий</span><span class="sxs-lookup"><span data-stu-id="73e61-266">Various transaction types and categories</span></span>

    - <span data-ttu-id="73e61-267">50 продуктов с 1-м прайс-листом продуктов</span><span class="sxs-lookup"><span data-stu-id="73e61-267">50 products with 1 product price list</span></span>

    - <span data-ttu-id="73e61-268">14 прайс-листов/списков стоимости</span><span class="sxs-lookup"><span data-stu-id="73e61-268">14 price/cost lists</span></span>

    - <span data-ttu-id="73e61-269">31 характеристика (навыки ресурса) в 2 моделях оценки с 3 уровнями (значениями оценки)</span><span class="sxs-lookup"><span data-stu-id="73e61-269">31 characteristics (resource skills) in 2 rating models with 3 levels (rating values)</span></span>

- <span data-ttu-id="73e61-270">Project Service</span><span class="sxs-lookup"><span data-stu-id="73e61-270">Project Service</span></span>

    - <span data-ttu-id="73e61-271">8 подразделений</span><span class="sxs-lookup"><span data-stu-id="73e61-271">8 organizational units</span></span>

    - <span data-ttu-id="73e61-272">6 уровней загруженности, специфичных для ролей</span><span class="sxs-lookup"><span data-stu-id="73e61-272">6 role-specific utilization levels</span></span>

    - <span data-ttu-id="73e61-273">Более 2,8 тыс. спецификаций цены роли</span><span class="sxs-lookup"><span data-stu-id="73e61-273">2.8k+ role-price specifications</span></span>

- <span data-ttu-id="73e61-274">Field Service</span><span class="sxs-lookup"><span data-stu-id="73e61-274">Field Service</span></span>

    - <span data-ttu-id="73e61-275">4 территории</span><span class="sxs-lookup"><span data-stu-id="73e61-275">4 territories</span></span>

    - <span data-ttu-id="73e61-276">5 типов заказов на работу</span><span class="sxs-lookup"><span data-stu-id="73e61-276">5 work order types</span></span>

    - <span data-ttu-id="73e61-277">22 актива клиентов</span><span class="sxs-lookup"><span data-stu-id="73e61-277">22 customer assets</span></span>

    - <span data-ttu-id="73e61-278">9 типов инцидентов с диапазоном связанных характеристик ресурсов (9), сервисов (13) и задач сервиса (13)</span><span class="sxs-lookup"><span data-stu-id="73e61-278">9 incident types with a range of associated resource characteristics (9), services (13) and service tasks (13)</span></span>
   
<span data-ttu-id="73e61-279">Пакет **Демонстрационные данные** устанавливает приблизительно 179 заказов на работу, 12 проектов и связанные данные о транзакциях.</span><span class="sxs-lookup"><span data-stu-id="73e61-279">The **Demo Data** package installs approximately 179 work orders, 12 projects, and associated transactional data.</span></span> 

### <a name="change-the-work-hours-for-sample-resources"></a><span data-ttu-id="73e61-280">Изменение рабочих часов для демонстрационных ресурсов</span><span class="sxs-lookup"><span data-stu-id="73e61-280">Change the work hours for sample resources</span></span>

<span data-ttu-id="73e61-281">По умолчанию все резервируемые ресурсы имеют календарь с 24 рабочими часами.</span><span class="sxs-lookup"><span data-stu-id="73e61-281">By default, all bookable resources have a 24 work hours calendar.</span></span>

<span data-ttu-id="73e61-282">Если требуется изменить рабочие часы для демонстрационных резервируемых ресурсов, перейдите в раздел **Universal Resource Scheduling** > **Планирование** > **Ресурсы**.</span><span class="sxs-lookup"><span data-stu-id="73e61-282">If you need to change the work hours for sample bookable resources, go to **Universal Resource Scheduling** > **Scheduling** > **Resources**.</span></span>

<span data-ttu-id="73e61-283">Выберите пользователя (например, Spencer Low) и измените рабочие часы пользователя Spencer на часы, которые требуется применить к нескольким пользователям.</span><span class="sxs-lookup"><span data-stu-id="73e61-283">Select a user (for example, Spencer Low) and change Spencer's work hours to the hours you want to apply to multiple users.</span></span> <span data-ttu-id="73e61-284">Перейдите к пункту **Universal Resource Scheduling** > **Настройки** > **Шаблоны рабочих часов** и измените запись **Рабочий шаблон по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="73e61-284">Go to **Universal Resource Scheduling** > **Settings** > **Work Hour Templates** and edit the **Default Work Template** record.</span></span> <span data-ttu-id="73e61-285">В поле **Ресурс шаблона** выберите пользователя с расписанием работы, которое требуется применить к другим ресурсам.</span><span class="sxs-lookup"><span data-stu-id="73e61-285">In the **Template Resource** field, select a user with work hours that you want to apply to other resources.</span></span> <span data-ttu-id="73e61-286">Выберите **Universal Resource Scheduling** > **Планирование** > **Ресурсы** > **Активные резервируемые ресурсы**.</span><span class="sxs-lookup"><span data-stu-id="73e61-286">Go to **Universal Resource Scheduling** > **Scheduling** > **Resources** > **Active Bookable Resources**.</span></span> <span data-ttu-id="73e61-287">Выберите ресурсы, которые требуется изменить, затем выберите **Задать календарь**.</span><span class="sxs-lookup"><span data-stu-id="73e61-287">Select the resources you want to change, and then select **Set Calendar**.</span></span> <span data-ttu-id="73e61-288">В раскрывающемся списке **Рабочий шаблон**, выберите шаблон **Рабочие часы по умолчанию** или другой шаблон с ресурсом с правильным шаблоном.</span><span class="sxs-lookup"><span data-stu-id="73e61-288">On the **Work Template** drop-down list, select the **Default Work Hour** template or another template with the correct templating resource.</span></span> <span data-ttu-id="73e61-289">При переходе к доске расписаний вы должны видеть, что у ресурсов обновились рабочие часы.</span><span class="sxs-lookup"><span data-stu-id="73e61-289">When you go to the schedule board, you should see that the resources now have updated work hours.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="73e61-290">![Снимок экрана активных резервируемых ресурсов](media/sample-data-6.png)</span><span class="sxs-lookup"><span data-stu-id="73e61-290">![Screenshot of active bookable resources](media/sample-data-6.png)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]