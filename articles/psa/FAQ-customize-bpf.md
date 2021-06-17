---
title: Как настроить последовательность операций бизнес-процесса стадий проекта?
description: Обзор порядка настройки последовательности операций бизнес-процесса стадий проекта.
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 2e6c60fe67aea908013077bde40c2faeabc2f39e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993162"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a><span data-ttu-id="3bfab-103">Как настроить последовательность операций бизнес-процесса стадий проекта?</span><span class="sxs-lookup"><span data-stu-id="3bfab-103">How do I customize the Project Stages business process flow?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

<span data-ttu-id="3bfab-104">Известное ограничение в предыдущих версиях приложения Project Service требует, чтобы названия стадий в последовательности операций бизнес-процесса полностью совпадали с ожидаемыми английскими именам (**Quote**, **Plan**, **Close**).</span><span class="sxs-lookup"><span data-stu-id="3bfab-104">There's a known limitation in earlier versions of the Project Service application that the names of the stages in the Project Stages business process flow must exactly match the expected English names (**Quote**, **Plan**, **Close**).</span></span> <span data-ttu-id="3bfab-105">В противном случае бизнес-логика, которая полагается на английские имена, не будет работать надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="3bfab-105">Otherwise, the business logic, which relies on the English stage names, doesn't work as expected.</span></span> <span data-ttu-id="3bfab-106">Поэтому вы не видите знакомые действия, такие как **Переключить процесс** или **Изменить процесс**, в форме проекта, и настройка последовательности операций бизнес-процесса не поощряется.</span><span class="sxs-lookup"><span data-stu-id="3bfab-106">That's why you don't see familiar actions such as **Switch Process** or **Edit Process** available on the project form, and customizing the business process flow isn't encouraged.</span></span> 

<span data-ttu-id="3bfab-107">Это ограничение было устранено в версии 2.4.5.48 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="3bfab-107">This limitation has been addressed in version 2.4.5.48 and later.</span></span> <span data-ttu-id="3bfab-108">В данной статье приведены предлагаемые временные решения, если необходимо настроить последовательность операций бизнес-процесса по умолчанию для более ранних версий.</span><span class="sxs-lookup"><span data-stu-id="3bfab-108">This article provides suggested workarounds if you need to customize the default business process flow for earlier versions.</span></span>  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a><span data-ttu-id="3bfab-109">Бизнес-логика требует полного совпадения с именами стадий на английском языке</span><span class="sxs-lookup"><span data-stu-id="3bfab-109">Business logic requires an exact match with English stage names</span></span>

<span data-ttu-id="3bfab-110">Последовательность операций бизнес-процесса стадий проекта включает бизнес-логику, которая управляет следующим поведением в приложении:</span><span class="sxs-lookup"><span data-stu-id="3bfab-110">The Project Stages business process flow includes business logic that drives the following behaviors in the app:</span></span>
- <span data-ttu-id="3bfab-111">Когда проект связан с предложением с расценками, код задает последовательность операций бизнес-процесса для стадии **Quote**.</span><span class="sxs-lookup"><span data-stu-id="3bfab-111">When the project is associated with a quote, the code sets the business process flow to the **Quote** stage.</span></span>
- <span data-ttu-id="3bfab-112">Когда проект связан с контрактом, код задает последовательность операций бизнес-процесса для стадии **Plan**.</span><span class="sxs-lookup"><span data-stu-id="3bfab-112">When the project is associated with a contract, the code sets the business process flow to the **Plan** stage.</span></span>
- <span data-ttu-id="3bfab-113">Когда последовательность операций бизнес-процесса переходит на стадию **Close**, запись проекта деактивируется.</span><span class="sxs-lookup"><span data-stu-id="3bfab-113">When the business process flow is advanced to the **Close** stage, the project record is deactivated.</span></span> <span data-ttu-id="3bfab-114">Когда проект деактивирован, форма проекта и структурная декомпозиция работ (WBS) становятся доступны только для чтения, резервирования именованных ресурсов освобождаются, и все связанные прайс-листы деактивируются.</span><span class="sxs-lookup"><span data-stu-id="3bfab-114">When the project is deactivated, the project form and work breakdown structure (WBS) are set to read-only, the named resource bookings are released, and any associated price lists are deactivated.</span></span>

<span data-ttu-id="3bfab-115">Эта бизнес-логика полагается на английские имена стадий проекта.</span><span class="sxs-lookup"><span data-stu-id="3bfab-115">This business logic relies on the English names for the project stages.</span></span> <span data-ttu-id="3bfab-116">Эта зависимость от английских имен стадий является главной причиной, по которой настройка последовательности операций бизнес-процесса стадий проекта не поощряется, а также по этой причине вы не видите часто используемые действия последовательности операций бизнес-процесса, такие как **Переключить процесс** или **Изменить процесс** в сущности проекта.</span><span class="sxs-lookup"><span data-stu-id="3bfab-116">This dependency on the English stage names is the main reason why customization of the Project Stages business process flow isn't encouraged, as well as why you don’t see the common business process flow actions like **Switch Process** or **Edit Process** on the project entity.</span></span>

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a><span data-ttu-id="3bfab-117">Что происходит, если имена стадий не совпадают с английскими именами?</span><span class="sxs-lookup"><span data-stu-id="3bfab-117">What happens if the stage names don't match the English names?</span></span>

<span data-ttu-id="3bfab-118">В версии 1.x приложения Project Service на платформе 8.2 когда имена стадий в последовательности операций бизнес-процесса не соответствуют в точности английским именам стадий, бизнес-логика, которая определяет правильные стадии для предложений с расценками или контрактов или закрывает проект, пропускается.</span><span class="sxs-lookup"><span data-stu-id="3bfab-118">In the Project Service app version 1.x on the 8.2 platform, when the stage names in the business process flow don’t match the English stage names exactly, the business logic that sets the right stage for quotes or contracts, or that closes the project, is skipped.</span></span> <span data-ttu-id="3bfab-119">Сообщения об ошибках не отображаются.</span><span class="sxs-lookup"><span data-stu-id="3bfab-119">No error messages are displayed.</span></span> <span data-ttu-id="3bfab-120">Поэтому возникает впечатление, что можно настраивать последовательность операций бизнес-процесса стадий проекта.</span><span class="sxs-lookup"><span data-stu-id="3bfab-120">Therefore it appears that you are able to customize the Project Stages business process flow.</span></span> <span data-ttu-id="3bfab-121">Однако вы не увидите такие автоматические процессы, работающие для предложений с расценками, контрактов и закрытия проекта.</span><span class="sxs-lookup"><span data-stu-id="3bfab-121">However, you won’t see any of the automatic processes working for quotes, contracts, and project close.</span></span>

<span data-ttu-id="3bfab-122">В версии 2.4.4.30 приложения Project Service или раннее на платформе 9.0 было сделано значительное архитектурное изменение в последовательностях операций бизнес-процессов, которое требуют переработки бизнес-логики последовательности операций бизнес-процесса.</span><span class="sxs-lookup"><span data-stu-id="3bfab-122">In the Project Service app version 2.4.4.30 or earlier on the 9.0 platform, there was a significant architectural change to business process flows, which required a re-write of the business process flow business logic.</span></span> <span data-ttu-id="3bfab-123">В результате если имена стадий процесса не совпадают с ожидаемыми английскими именами, вы получите сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="3bfab-123">As a result, if the process stage names don’t match the expected English names, you do receive an error message.</span></span> 

<span data-ttu-id="3bfab-124">Поэтому, если требуется настроить последовательность операций бизнес-процесса стадий проекта для сущности проекта, можно добавить лишь совершенно новые стадии в последовательность операций бизнес-процесса по умолчанию, сохранив стадии **Quote**, **Plan** и **Close** без изменений.</span><span class="sxs-lookup"><span data-stu-id="3bfab-124">Therefore, if you want to customize the Project Stages business process flow for the project entity, you can only add brand new stages to the default business process flow for the project entity, while keeping the **Quote**, **Plan**, and **Close** stages as-is.</span></span> <span data-ttu-id="3bfab-125">Это ограничение обеспечивает, чтобы не возникали ошибки из бизнес-логики, которая ожидает имена стадий на английском языке в последовательности операций бизнес-процесса.</span><span class="sxs-lookup"><span data-stu-id="3bfab-125">This restriction ensures that you don’t get errors from the business logic that expects the English stage names in the business process flow.</span></span>

<span data-ttu-id="3bfab-126">В версии 2.4.5.48 или выше бизнес-логика, описанная в этой статье, была удалена из последовательности операций бизнес-процесса по умолчанию для сущности проекта.</span><span class="sxs-lookup"><span data-stu-id="3bfab-126">In version 2.4.5.48 or later, the business logic described in this article has been removed from the default business process flow for the project entity.</span></span> <span data-ttu-id="3bfab-127">Обновление до этой или более поздней версии позволит настраивать или заменять последовательность операций бизнес-процесса по умолчанию своей собственной.</span><span class="sxs-lookup"><span data-stu-id="3bfab-127">Upgrading to that version or later will let you customize or replace the default business process flow with one of your own.</span></span> 

## <a name="workarounds-for-earlier-versions"></a><span data-ttu-id="3bfab-128">Обходные решения для более ранних версий</span><span class="sxs-lookup"><span data-stu-id="3bfab-128">Workarounds for earlier versions</span></span>

<span data-ttu-id="3bfab-129">Если обновление невозможно, можно настроить последовательность операций бизнес-процесса стадий проекта для сущности проекта одним из следующих двух способов:</span><span class="sxs-lookup"><span data-stu-id="3bfab-129">If upgrading isn't an option, you can customize the Project Stages business process flow for the project entity in one of these two ways:</span></span>

1. <span data-ttu-id="3bfab-130">Добавить дополнительные стадии в конфигурацию по умолчанию, сохранив английские имена стадий **Quote**, **Plan** и **Close**.</span><span class="sxs-lookup"><span data-stu-id="3bfab-130">Add additional stages to the default configuration, while retaining the English stage names for **Quote**, **Plan**, and **Close**.</span></span>


![Снимок экрана добавления стадий в конфигурацию по умолчанию](media/FAQ-Customize-BPF-1.png)
 
2. <span data-ttu-id="3bfab-132">Создать собственную последовательность операций бизнес-процесса и сделать ее основной последовательностью операций бизнес-процесса для сущности проекта, что позволит задать любые требуемые имена стадий.</span><span class="sxs-lookup"><span data-stu-id="3bfab-132">Create your own business process flow and make it the primary business process flow for the project entity, which lets you have any stage names you want.</span></span> <span data-ttu-id="3bfab-133">Однако если необходимо использовать стандартные стадии проекта **Quote**, **Plan** и **Close**, необходимо выполнить некоторые настройки, которые управляются вашими настраиваемыми именами стадий.</span><span class="sxs-lookup"><span data-stu-id="3bfab-133">However, if you want to use the same standard project stages **Quote**, **Plan**, and **Close**, you need to do some customizations that are driven off your custom stage names.</span></span> <span data-ttu-id="3bfab-134">Более сложная логика находится в закрытии проекта, которую по-прежнему можно запустить, просто деактивировав запись проекта.</span><span class="sxs-lookup"><span data-stu-id="3bfab-134">The more complex logic is in the closing of the project, which you can still trigger by just deactivating the project record.</span></span>

![Настройка BPF](media/FAQ-Customize-BPF-2.png)

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a><span data-ttu-id="3bfab-136">Дополнительные замечания для приложения Project Service версии 2.4.4.30 или ранее на платформе 9.0</span><span class="sxs-lookup"><span data-stu-id="3bfab-136">Additional considerations for Project Service app version 2.4.4.30 or earlier on platform 9.0</span></span>

<span data-ttu-id="3bfab-137">В приложении Project Service версии 2.4.4.30 или более ранней на платформе 9.0 с настраиваемой последовательностью операций бизнес-процесса поле **Имя стадии** в сущности проекта, используемое в представлениях диаграммы **Проект по стадии** и списка проектов, не будет обновляться, поскольку оно связано с последовательностью операций бизнес-процесса стадий проекта по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3bfab-137">In Project Service 2.4.4.30 or earlier on platform 9.0, with a custom business process flow the **Stage Name** field on the project entity used in the **Project By Stage** chart and project list views won’t update, because it’s coupled to the default Project Stages business process flow.</span></span> <span data-ttu-id="3bfab-138">Эту проблему можно решить, выполнив следующие действия.</span><span class="sxs-lookup"><span data-stu-id="3bfab-138">You can address this issue with the following steps:</span></span>

- <span data-ttu-id="3bfab-139">Добавьте настраиваемое поле для захвата текущей стадии последовательности операций бизнес-процесса, которое обновляется, когда пользователь проходит по пользовательской последовательности операций бизнес-процесса.</span><span class="sxs-lookup"><span data-stu-id="3bfab-139">Add a custom field to capture the current business process flow stage that is updated as the user advances through the custom business process flow.</span></span>

- <span data-ttu-id="3bfab-140">Измените диаграмму **Проект по стадии** для работы с настраиваемым полем вместо конфигурации по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3bfab-140">Modify the **Project By Stage** chart to work with your custom field instead of the default configuration.</span></span>

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a><span data-ttu-id="3bfab-141">Шаги для создания вашей собственной последовательности операций бизнес-процесса для сущности проекта</span><span class="sxs-lookup"><span data-stu-id="3bfab-141">Steps to create your own business process flow for the project entity</span></span>

<span data-ttu-id="3bfab-142">Чтобы создать собственную последовательность операций бизнес-процесса для сущности проекта, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="3bfab-142">To create your own business process flow for the project entity do the following:</span></span>

1. <span data-ttu-id="3bfab-143">Перейдите в раздел **Параметры** > **Центр обработки**.</span><span class="sxs-lookup"><span data-stu-id="3bfab-143">Go to **Settings** > **Process Center**.</span></span> <span data-ttu-id="3bfab-144">Не копируйте последовательность операций бизнес-процесса стадий проекта, поскольку при этом выполняется копирование также бизнес-логики Project Service.</span><span class="sxs-lookup"><span data-stu-id="3bfab-144">Don’t copy the Project Stages business process flow because that also copies the Project Service business logic.</span></span>

  ![Создание процесса](media/FAQ-Customize-BPF-3.png)

2. <span data-ttu-id="3bfab-146">Используйте конструктор процессов для создания требуемых имен стадий.</span><span class="sxs-lookup"><span data-stu-id="3bfab-146">Use the Process Designer to create the stage names you want.</span></span> <span data-ttu-id="3bfab-147">Если требуются те же функциональные возможности, что и стадии по умолчанию для **Quote**, **Plan** и **Close**, необходимо создать их на основе имен стадий вашей настраиваемой последовательности операций бизнес-процесса.</span><span class="sxs-lookup"><span data-stu-id="3bfab-147">If you want the same functionality as the default stages for **Quote**, **Plan**, and **Close**, you’ll have to create that based on your custom business process flow’s stage names.</span></span>

   ![Снимок экрана конструктора процессов, используемого для настройки BPF](media/FAQ-Customize-BPF-4.png) 

3. <span data-ttu-id="3bfab-149">В конструкторе процессов нажмите **Последовательность операций процесса заказа**, чтобы сделать настраиваемую последовательность операций бизнес-процесса основной последовательностью операций бизнес-процесса для сущности проекта, переместив ее над последовательностью операций бизнес-процесса стадий проекта на верх списка.</span><span class="sxs-lookup"><span data-stu-id="3bfab-149">In the Process Designer, click **Order Process Flow** to make the custom business process flow the primary business process flow for the project entity by moving it above the Project Stages business process flow to the top of the list.</span></span>


   [<span data-ttu-id="3bfab-150">Снимок экрана использования последовательности операций заказа</span><span class="sxs-lookup"><span data-stu-id="3bfab-150">Screenshot of using Order Process Flow</span></span>](media/FAQ-Customize-BPF-5-720.png)

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a><span data-ttu-id="3bfab-151">Следующие действия применимы к приложению Project Service 2.4.4.30 или ранее на платформе 9.0</span><span class="sxs-lookup"><span data-stu-id="3bfab-151">The following steps apply to Project Service app 2.4.4.30 or earlier on the 9.0 platform</span></span>

4. <span data-ttu-id="3bfab-152">Добавьте новое настраиваемое поле в сущность проекта для захвата настраиваемых стадий в вашей настраиваемой последовательности операций бизнес-процесса.</span><span class="sxs-lookup"><span data-stu-id="3bfab-152">Add a new custom field to the project entity to capture the custom stages in your custom business process flow.</span></span> <span data-ttu-id="3bfab-153">Потребуется добавить бизнес-логику (подключаемый модуль или бизнес-процесс) для обновления этого поля, когда стадия в настраиваемой последовательности операций бизнес-процесса обновляется.</span><span class="sxs-lookup"><span data-stu-id="3bfab-153">You’ll need to add business logic (plugin/workflow) to update this field when the stage on the custom business process flow is updated.</span></span>

   ![Снимок экрана настраиваемой сущности проекта](media/FAQ-Customize-BPF-6-720.png)

5. <span data-ttu-id="3bfab-155">Измените диаграмму **Проект по стадии** для использования вашего нового настраиваемого поля для стадий.</span><span class="sxs-lookup"><span data-stu-id="3bfab-155">Modify the **Project By Stage** chart to use your new custom field for stages.</span></span>

   ![Снимок экрана использования диаграммы "Проект по стадии"](media/FAQ-Customize-BPF-7-720.png)

6. <span data-ttu-id="3bfab-157">Измените все представления для сущности проекта для включения вашего нового настраиваемого поля для стадий.</span><span class="sxs-lookup"><span data-stu-id="3bfab-157">Modify any views for the project entity to include your new custom field for stages.</span></span>

   ![Снимок экрана изменения представлений сущности проекта](media/FAQ-Customize-BPF-8-720.png)



[!INCLUDE[footer-include](../includes/footer-banner.md)]