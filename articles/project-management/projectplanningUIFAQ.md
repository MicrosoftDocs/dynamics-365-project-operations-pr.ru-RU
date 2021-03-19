---
title: Устранение неполадок при работе в сетке задач
description: Этот тема предоставляет информацию об устранении неполадок, необходимую при работе в сетке задач.
author: ruhercul
manager: tfehr
ms.date: 01/19/2021
ms.topic: article
ms.product: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: dedd989cc7c959d9ea97a0abfb13f8f1b2150a56
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286579"
---
# <a name="troubleshoot-working-in-the-task-grid"></a><span data-ttu-id="86db0-103">Устранение неполадок при работе в сетке задач</span><span class="sxs-lookup"><span data-stu-id="86db0-103">Troubleshoot working in the Task grid</span></span> 

<span data-ttu-id="86db0-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="86db0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="86db0-105">В этой теме описывается, как исправить проблемы, с которыми вы можете столкнуться при работе с управлением затратами.</span><span class="sxs-lookup"><span data-stu-id="86db0-105">This topic describes how to fix issues that you might encounter while working with cost management.</span></span>

## <a name="enable-cookies"></a><span data-ttu-id="86db0-106">Включите файлы "cookie"</span><span class="sxs-lookup"><span data-stu-id="86db0-106">Enable cookies</span></span>

<span data-ttu-id="86db0-107">Project Operations требует, чтобы сторонние файлы cookie были включены для визуализации структурной декомпозиции работ.</span><span class="sxs-lookup"><span data-stu-id="86db0-107">Project Operations requires that third-party cookies be enabled in order to render the work breakdown structure.</span></span> <span data-ttu-id="86db0-108">Если сторонние файлы cookie не включены, вместо просмотра задач вы увидите пустую страницу при выборе вкладка **Задачи** на страница **Проект**.</span><span class="sxs-lookup"><span data-stu-id="86db0-108">When third-party cookies aren't enabled, instead of seeing tasks, you will see a blank page when you select the **Tasks** tab on the **Project** page.</span></span>

![Пустая вкладка, если сторонние файлы cookie не включены](media/blankschedule.png)


### <a name="workaround"></a><span data-ttu-id="86db0-110">Решение</span><span class="sxs-lookup"><span data-stu-id="86db0-110">Workaround</span></span>
<span data-ttu-id="86db0-111">Для браузеров Microsoft Edge или Google Chrome, следующие процедуры описывают, как обновить настройки вашего браузера, чтобы включить сторонние файлы cookie.</span><span class="sxs-lookup"><span data-stu-id="86db0-111">For Microsoft Edge or Google Chrome browsers, the following procedures outline how to update your browser setting to enable third-party cookies.</span></span>

#### <a name="microsoft-edge"></a><span data-ttu-id="86db0-112">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="86db0-112">Microsoft Edge</span></span>

1. <span data-ttu-id="86db0-113">Откройте браузер Edge.</span><span class="sxs-lookup"><span data-stu-id="86db0-113">Open your Edge browser.</span></span>
2. <span data-ttu-id="86db0-114">В правом верхнем углу нажмите **Многоточие** (...) и выберите **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="86db0-114">In the upper-right corner, select the **ellipsis** (...), and then select **Settings**.</span></span>
3. <span data-ttu-id="86db0-115">Под **Файлы cookie и разрешения для сайтов**, выбрать **Файлы cookie и данные сайтов**.</span><span class="sxs-lookup"><span data-stu-id="86db0-115">Under **Cookies and site permissions**, select **Cookies and site data**.</span></span>
4. <span data-ttu-id="86db0-116">Выключить **Блокировать сторонние файлы cookie**.</span><span class="sxs-lookup"><span data-stu-id="86db0-116">Turn off **Block third-party cookies**.</span></span>

#### <a name="google-chrome"></a><span data-ttu-id="86db0-117">Google Chrome</span><span class="sxs-lookup"><span data-stu-id="86db0-117">Google Chrome</span></span>

1. <span data-ttu-id="86db0-118">Откройте браузер Chrome.</span><span class="sxs-lookup"><span data-stu-id="86db0-118">Open your Chrome browser.</span></span>
2. <span data-ttu-id="86db0-119">В правом верхнем углу выберите три вертикальные точки, затем выберите **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="86db0-119">In the upper-right corner, select the three vertical dots, and then select **Settings**.</span></span>
3. <span data-ttu-id="86db0-120">Под **Конфиденциальность и безопасность**, выбрать **Файлы cookie и другие данные сайтов**.</span><span class="sxs-lookup"><span data-stu-id="86db0-120">Under **Privacy and security**, select **Cookies and other site data**.</span></span>
4. <span data-ttu-id="86db0-121">Выберите **Разрешить все файлы cookie**.</span><span class="sxs-lookup"><span data-stu-id="86db0-121">Select **Allow all cookies**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="86db0-122">Если вы заблокируете сторонние файлы cookie, все файлы cookie и данные сайтов с других сайтов будут заблокированы, даже если сайт разрешен в вашем списке исключений.</span><span class="sxs-lookup"><span data-stu-id="86db0-122">If you block third-party cookies, all cookies and site data from other sites will be blocked, even if the site is allowed on your exceptions list.</span></span>

## <a name="pex-endpoint"></a><span data-ttu-id="86db0-123">Конечная точка PEX</span><span class="sxs-lookup"><span data-stu-id="86db0-123">PEX Endpoint</span></span>

<span data-ttu-id="86db0-124">Project Operations требует, чтобы параметр проекта ссылался на конечную точку PEX.</span><span class="sxs-lookup"><span data-stu-id="86db0-124">Project Operations requires that a project parameter reference the PEX Endpoint.</span></span> <span data-ttu-id="86db0-125">Этот конечная точка требуется для связи со службой, используемой для визуализации структурной декомпозиции работ.</span><span class="sxs-lookup"><span data-stu-id="86db0-125">This endpoint is required to communicate with the service used to render the work breakdown structure.</span></span> <span data-ttu-id="86db0-126">Если параметр не включен, вы получите сообщение об ошибке "Параметр проекта недействителен".</span><span class="sxs-lookup"><span data-stu-id="86db0-126">If the parameter isn't enabled, you will receive the error, "The project parameter is not valid".</span></span> 

### <a name="workaround"></a><span data-ttu-id="86db0-127">Решение</span><span class="sxs-lookup"><span data-stu-id="86db0-127">Workaround</span></span>
 ![Поле конечная точка PEX в параметре проекта](media/projectparameter.png)

1. <span data-ttu-id="86db0-129">Добавить поле **Конечная точка PEX** на страницу **Параметры проекта**.</span><span class="sxs-lookup"><span data-stu-id="86db0-129">Add the **PEX Endpoint** field to the **Project Parameters** page.</span></span>
2. <span data-ttu-id="86db0-130">Обновите поле следующим значением: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`</span><span class="sxs-lookup"><span data-stu-id="86db0-130">Update the field with the following value: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`</span></span>
3. <span data-ttu-id="86db0-131">Удалите поле со страницы **Параметры проекта**.</span><span class="sxs-lookup"><span data-stu-id="86db0-131">Remove the field from the **Project Parameters** page.</span></span>

## <a name="privileges-for-project-for-the-web"></a><span data-ttu-id="86db0-132">Привилегии для Project для Интернета</span><span class="sxs-lookup"><span data-stu-id="86db0-132">Privileges for Project for the Web</span></span>

<span data-ttu-id="86db0-133">Project Operations полагается на внешнюю службу планирования.</span><span class="sxs-lookup"><span data-stu-id="86db0-133">Project Operations relies on an external scheduling service.</span></span> <span data-ttu-id="86db0-134">Служба требует, чтобы у пользователя было несколько ролей, назначенных для чтения и записи сущностей, связанных со структурной декомпозицией работ.</span><span class="sxs-lookup"><span data-stu-id="86db0-134">The service requires that a user have several roles assigned to read and write to entities related to the work breakdown structure.</span></span> <span data-ttu-id="86db0-135">Эти сущности включают задачи проекта, назначения ресурсов и зависимости задач.</span><span class="sxs-lookup"><span data-stu-id="86db0-135">These entities include project tasks, resource assignments, and task dependencies.</span></span> <span data-ttu-id="86db0-136">Если пользователь не может отобразить структуру декомпозиции работ при переходе к вкладке **Задачи**, вероятно, потому, что Project for Project Operations не был включен.</span><span class="sxs-lookup"><span data-stu-id="86db0-136">If a user can't render the work breakdown structure when they go to the **Tasks** tab, it's probably because Project for Project Operations hasn't been enabled.</span></span> <span data-ttu-id="86db0-137">Пользователь может получить либо ошибку роли безопасности, либо ошибку, связанную с отказом в доступе.</span><span class="sxs-lookup"><span data-stu-id="86db0-137">A user might receive either a security role error, or an error related to a denial of access.</span></span>


## <a name="workaround"></a><span data-ttu-id="86db0-138">Решение</span><span class="sxs-lookup"><span data-stu-id="86db0-138">Workaround</span></span>

1. <span data-ttu-id="86db0-139">Перейти к представлению **Параметр > Безопасность > Пользователи > Пользователи приложения**.</span><span class="sxs-lookup"><span data-stu-id="86db0-139">Go to **Setting > Security > Users > Application Users**.</span></span>  

   ![Читатель приложения](media/applicationuser.jpg)
   
2. <span data-ttu-id="86db0-141">Дважды щелкните запись пользователя приложения, чтобы проверить следующее:</span><span class="sxs-lookup"><span data-stu-id="86db0-141">Double-click the application user record to verify the following:</span></span>

 - <span data-ttu-id="86db0-142">Пользователь имеет доступ к проекту.</span><span class="sxs-lookup"><span data-stu-id="86db0-142">The user has access to the project.</span></span> <span data-ttu-id="86db0-143">Эта проверка обычно выполняется путем проверки того, что пользователь имеет роль безопасности **Руководитель проекта**.</span><span class="sxs-lookup"><span data-stu-id="86db0-143">This verification is typically done by ensuring that the user has **Project Manager** security role.</span></span>
 - <span data-ttu-id="86db0-144">Пользователь приложения Microsoft Project существует и настроен правильно.</span><span class="sxs-lookup"><span data-stu-id="86db0-144">The Microsoft Project application user exists and is configured correctly.</span></span>
 
3. <span data-ttu-id="86db0-145">Если этот пользователь не существует, можно создать новую запись пользователя.</span><span class="sxs-lookup"><span data-stu-id="86db0-145">If this user doesn't exist, you can create a new user record.</span></span> <span data-ttu-id="86db0-146">Выбрать **Новые пользователи**.</span><span class="sxs-lookup"><span data-stu-id="86db0-146">Select **New Users**.</span></span> <span data-ttu-id="86db0-147">Измените форму записи на **Пользователь приложения**, а затем добавьте **ИД приложения** .</span><span class="sxs-lookup"><span data-stu-id="86db0-147">Change the entry form to **Application User**, and then add the **Application ID**.</span></span>

   ![Сведения о пользователе приложения](media/applicationuserdetails.jpg)

4. <span data-ttu-id="86db0-149">Убедитесь, что пользователю назначена правильная лицензия и что служба включена в сведениях о тарифных планах лицензии.</span><span class="sxs-lookup"><span data-stu-id="86db0-149">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
5. <span data-ttu-id="86db0-150">Убедитесь, что пользователь может открыть project.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="86db0-150">Verify that the user can open project.microsoft.com.</span></span>
6. <span data-ttu-id="86db0-151">С помощью параметров проекта убедитесь, что система указывает на правильный конечную точку проекта.</span><span class="sxs-lookup"><span data-stu-id="86db0-151">Verify through the project parameters that the system is pointing to the correct project endpoint.</span></span>
7. <span data-ttu-id="86db0-152">Убедитесь, что пользователь приложения проекта создан.</span><span class="sxs-lookup"><span data-stu-id="86db0-152">Verify that the project application user is created.</span></span>
8. <span data-ttu-id="86db0-153">Примените к пользователю следующие роли безопасности:</span><span class="sxs-lookup"><span data-stu-id="86db0-153">Apply the following security roles to the user:</span></span>

  - <span data-ttu-id="86db0-154">Пользователь Dataverse</span><span class="sxs-lookup"><span data-stu-id="86db0-154">Dataverse User</span></span>
  - <span data-ttu-id="86db0-155">Система Project Operations</span><span class="sxs-lookup"><span data-stu-id="86db0-155">Project Operations System</span></span>
  - <span data-ttu-id="86db0-156">Система проектов</span><span class="sxs-lookup"><span data-stu-id="86db0-156">Project System</span></span>

## <a name="error-when-updating-the-work-breakdown-structure"></a><span data-ttu-id="86db0-157">Ошибка при обновлении структурной декомпозиции работ</span><span class="sxs-lookup"><span data-stu-id="86db0-157">Error when updating the work breakdown structure</span></span>

<span data-ttu-id="86db0-158">Когда одно или несколько обновлений вносятся в структурная декомпозиция работ, изменения в конечном итоге не срабатывают и не сохраняются.</span><span class="sxs-lookup"><span data-stu-id="86db0-158">When one or more updates are made to the work breakdown structure, the changes eventually fail and aren't saved.</span></span> <span data-ttu-id="86db0-159">В сетке расписания возникает ошибка, в которой указано, что "Недавнее внесенное вами изменение не может быть сохранено".</span><span class="sxs-lookup"><span data-stu-id="86db0-159">An error occurs in the schedule grid noting that “Recent change you’ve made couldn’t be saved.”</span></span>

### <a name="workaround"></a><span data-ttu-id="86db0-160">Решение</span><span class="sxs-lookup"><span data-stu-id="86db0-160">Workaround</span></span>

1. <span data-ttu-id="86db0-161">Убедитесь, что пользователю назначена правильная лицензия и что служба включена в сведениях о тарифных планах лицензии.</span><span class="sxs-lookup"><span data-stu-id="86db0-161">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
2. <span data-ttu-id="86db0-162">Убедитесь, что пользователь может открыть project.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="86db0-162">Verify that the user can open project.microsoft.com.</span></span>
3. <span data-ttu-id="86db0-163">Убедитесь, что система указывает на правильный конечную точку проекта.</span><span class="sxs-lookup"><span data-stu-id="86db0-163">Verify that the system is pointing to the correct project endpoint,.</span></span>
4. <span data-ttu-id="86db0-164">Убедитесь, что пользователь приложения проекта создан.</span><span class="sxs-lookup"><span data-stu-id="86db0-164">Verify that the Project Application user has been created.</span></span>
5. <span data-ttu-id="86db0-165">Примените к пользователю следующие роли безопасности:</span><span class="sxs-lookup"><span data-stu-id="86db0-165">Apply the following security roles to the user:</span></span>
  
  - <span data-ttu-id="86db0-166">Пользователь Dataverse или базовый пользователь</span><span class="sxs-lookup"><span data-stu-id="86db0-166">Dataverse user or Base user</span></span>
  - <span data-ttu-id="86db0-167">Система Project Operations</span><span class="sxs-lookup"><span data-stu-id="86db0-167">Project Operations System</span></span>
  - <span data-ttu-id="86db0-168">Система проектов</span><span class="sxs-lookup"><span data-stu-id="86db0-168">Project System</span></span>
  - <span data-ttu-id="86db0-169">Система двойной записи Project Operations (эта роль требуется, если вы развертываете сценарий Project Operations на основе ресурсов/отсутствия запасов).</span><span class="sxs-lookup"><span data-stu-id="86db0-169">Project Operations Dual Write System (This role is required if you are deploying the resource/non-stocked based scenario of Project Operations.)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]