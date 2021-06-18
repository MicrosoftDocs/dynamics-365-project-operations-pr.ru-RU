---
title: Производительность планирования ресурсов проекта
description: Эта тема предоставляет информацию о том, как повысить производительность планирования ресурсов для большого количества проектов.
author: Yowelle
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 113023909f88cb4dd498190ef21b6955482b25dd
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010037"
---
# <a name="project-resource-scheduling-performance"></a><span data-ttu-id="a4cee-103">Производительность планирования ресурсов проекта</span><span class="sxs-lookup"><span data-stu-id="a4cee-103">Project resource scheduling performance</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


<span data-ttu-id="a4cee-104">Проблемы с производительностью, связанные с планированием ресурсов, могут возникнуть, когда количество проектов достигает тысяч.</span><span class="sxs-lookup"><span data-stu-id="a4cee-104">Performance issues related to resource scheduling can occur when the number of projects reaches into the thousands.</span></span> <span data-ttu-id="a4cee-105">Для повышения производительности планирования ресурсов доступна функция, позволяющая пользователям сократить время, необходимое для запуска формы доступности ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a4cee-105">To improve resource scheduling performance, a feature is available that allows users to reduce the time that it takes to launch the resource availability form.</span></span> <span data-ttu-id="a4cee-106">В частности, это удаляет процесс синхронизации свертки емкости ресурсов и использует таблицу **ResProjectResource** для ускорения поиска ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a4cee-106">Specifically, this removes the resource capacity roll-up synchronization process and uses the **ResProjectResource** table to speed up the resource lookup.</span></span> <span data-ttu-id="a4cee-107">Обратите внимание, что таблица **ResRollup** больше не будет использоваться.</span><span class="sxs-lookup"><span data-stu-id="a4cee-107">Note that the **ResRollup** table will no longer be used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a4cee-108">Если есть зависимость от процесса синхронизации свертки емкости ресурсов или от таблицы **ResProjectResource**, не используйте эту функцию.</span><span class="sxs-lookup"><span data-stu-id="a4cee-108">If there is a dependency on either the resource capacity roll-up synchronization process or the **ResProjectResource** table, do not use this feature.</span></span>

## <a name="enable-resource-scheduling-performance-enhancement"></a><span data-ttu-id="a4cee-109">Включение повышения производительности планирования ресурсов</span><span class="sxs-lookup"><span data-stu-id="a4cee-109">Enable resource scheduling performance enhancement</span></span>
<span data-ttu-id="a4cee-110">Чтобы включить повышение производительности планирования ресурсов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a4cee-110">To enable resource scheduling performance enhancement, complete the following steps.</span></span>

1. <span data-ttu-id="a4cee-111">Перейдите в раздел **Управление функциями** > **Все** и в списке функций найдите **Включить функцию повышения производительности планирования ресурсов проектов**.</span><span class="sxs-lookup"><span data-stu-id="a4cee-111">Go to **Feature management** > **All**, and in the feature list, locate **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="a4cee-112">Выберите **Включить сейчас**.</span><span class="sxs-lookup"><span data-stu-id="a4cee-112">Select **Enable now**.</span></span>

> [!NOTE]
> <span data-ttu-id="a4cee-113">Если вы не можете найти функцию в списке, выберите **Проверить наличие обновлений**, чтобы обновить список.</span><span class="sxs-lookup"><span data-stu-id="a4cee-113">If you can't find the feature in the list, select **Check for updates** to refresh the list.</span></span>

3. <span data-ttu-id="a4cee-114">Обновите браузер, затем перейдите в раздел **Управление и учет по проектам** > **Периодические задачи** > **Ресурсы проектов** > **Синхронизация емкости календарей ресурсов во всех компаниях**.</span><span class="sxs-lookup"><span data-stu-id="a4cee-114">Refresh your browser, and then go to **Project management and accounting** > **Periodic** > **Project resources** > **Synchronize resource calendars capacity across all companies**.</span></span>
4. <span data-ttu-id="a4cee-115">Установите для параметра **Удалить существующие записи о емкости** значение **Да**, чтобы удалить предыдущие данные.</span><span class="sxs-lookup"><span data-stu-id="a4cee-115">Set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="a4cee-116">Если вы хотите генерировать инкрементные данные, установите для него значение **Нет**.</span><span class="sxs-lookup"><span data-stu-id="a4cee-116">If you want generate incremental data, set it to **No**.</span></span>
5. <span data-ttu-id="a4cee-117">В поле **Код периода** выберите период, за который должны быть созданы данные.</span><span class="sxs-lookup"><span data-stu-id="a4cee-117">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="a4cee-118">Если вы выбираете код периода, дату начала и окончания определять не нужно.</span><span class="sxs-lookup"><span data-stu-id="a4cee-118">If you select a period code, a start and end date do not need to be defined.</span></span>
6. <span data-ttu-id="a4cee-119">Если вы оставите поле **Код периода** пустым, выберите конкретные даты начала и окончания для генерации данных.</span><span class="sxs-lookup"><span data-stu-id="a4cee-119">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
7. <span data-ttu-id="a4cee-120">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="a4cee-120">Select **OK**.</span></span>

 > [!NOTE]
 > <span data-ttu-id="a4cee-121">Это распределит общие данные в таблицу **ResCalendarCapacity** для всех компаний в вашей среде, поэтому пакетное задание нужно запускать только в одном юридическом лице.</span><span class="sxs-lookup"><span data-stu-id="a4cee-121">This will distribute general data to the **ResCalendarCapacity** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="a4cee-122">Данные в этом пакетном задании необходимы для расчета емкости ресурсов с помощью связанного календаря.</span><span class="sxs-lookup"><span data-stu-id="a4cee-122">The data in this batch job is needed to calculate resource capacity through the associated calendar.</span></span>

8. <span data-ttu-id="a4cee-123">Перейдите в раздел **Управление и учет по проектам** > **Периодические задачи** > **Ресурсы проектов** > **Заполнить ресурсы проектов во всех компаниях**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="a4cee-123">Go to **Project management and accounting** > **Periodic** > **Project resources** > **Populate project resources across all companies** and then select **OK**.</span></span> <span data-ttu-id="a4cee-124">Это сценарий обновления данных для общих данных в таблицах **ResProjectResource**, **ResCalendarDateTimeRange** и **ResEffectiveDateTimeRange**.</span><span class="sxs-lookup"><span data-stu-id="a4cee-124">This is the data upgrade script for general data in the **ResProjectResource**, **ResCalendarDateTimeRange**, and **ResEffectiveDateTimeRange** tables.</span></span> <span data-ttu-id="a4cee-125">Значения для полей **PSAPRojSchedRole.RootActivity** также обновляются.</span><span class="sxs-lookup"><span data-stu-id="a4cee-125">Values for the **PSAPRojSchedRole.RootActivity** field are also updated.</span></span> <span data-ttu-id="a4cee-126">Если это не будет выполнено, вы получите предупреждение при попытке выполнить операции планирования ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a4cee-126">If this is not run, you will receive a warning when you try to execute resource scheduling operations.</span></span>
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a><span data-ttu-id="a4cee-127">Выключение повышения производительности планирования ресурсов</span><span class="sxs-lookup"><span data-stu-id="a4cee-127">Turn off resource scheduling performance enhancement</span></span>

1. <span data-ttu-id="a4cee-128">Перейдите в раздел **Управление функциями** > **Все** и найдите **Включить функцию повышения производительности планирования ресурсов проектов**.</span><span class="sxs-lookup"><span data-stu-id="a4cee-128">Go to **Feature management** > **All**  and search for **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="a4cee-129">Выберите функцию, затем выберите кнопку **Отключить**.</span><span class="sxs-lookup"><span data-stu-id="a4cee-129">Select the feature, and then select the **Disable** button.</span></span>
3. <span data-ttu-id="a4cee-130">Обновите свой браузер.</span><span class="sxs-lookup"><span data-stu-id="a4cee-130">Refresh your browser.</span></span>
4. <span data-ttu-id="a4cee-131">Перейдите в раздел **Управление и учет по проектам** > **Периодические задачи** > **Синхронизация загрузки** > **Синхронизация операций сведения загрузки ресурсов**.</span><span class="sxs-lookup"><span data-stu-id="a4cee-131">Go to **Project management and accounting** > **Periodic** > **Capacity synchronization** > **Synchronize resource capacity roll-ups**.</span></span>
5. <span data-ttu-id="a4cee-132">На странице **Синхронизация сведения мощности** задайте для параметра **Удалить существующие записи мощности** значение **Да**, чтобы удалить предыдущие данные.</span><span class="sxs-lookup"><span data-stu-id="a4cee-132">On the **Capacity roll-up synchronization** page, set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="a4cee-133">Если вы хотите генерировать инкрементные данные, установите для него значение **Нет**.</span><span class="sxs-lookup"><span data-stu-id="a4cee-133">If you want to generate incremental data, set it to **No**.</span></span>
6. <span data-ttu-id="a4cee-134">В поле **Код периода** выберите период, за который должны быть созданы данные.</span><span class="sxs-lookup"><span data-stu-id="a4cee-134">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="a4cee-135">Если вы выбираете код периода, дату начала и окончания определять не нужно.</span><span class="sxs-lookup"><span data-stu-id="a4cee-135">If you select a period code, a start and end date do not need to be defined.</span></span>
7. <span data-ttu-id="a4cee-136">Если вы оставите поле **Код периода** пустым, выберите конкретные даты начала и окончания для генерации данных.</span><span class="sxs-lookup"><span data-stu-id="a4cee-136">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
8. <span data-ttu-id="a4cee-137">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="a4cee-137">Select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="a4cee-138">Это распределит общие данные в таблицу **ResRollup** для всех компаний в вашей среде, поэтому пакетное задание нужно запускать только в одном юридическом лице.</span><span class="sxs-lookup"><span data-stu-id="a4cee-138">This will distribute general data to the **ResRollup** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="a4cee-139">Это пакетное задание необходимо для всех представлений **Доступность ресурсов**.</span><span class="sxs-lookup"><span data-stu-id="a4cee-139">This batch job is needed for all **Resource Availability** views.</span></span> <span data-ttu-id="a4cee-140">Если это пакетное задание не запущено, данные **ResRollup** будут генерироваться "на лету", что может занять время.</span><span class="sxs-lookup"><span data-stu-id="a4cee-140">If this batch job is not run, the **ResRollup** data will be generated on the fly, which can take time.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]