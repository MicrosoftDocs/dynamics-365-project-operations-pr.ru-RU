---
title: Запрос графика расходов федеральных наград
description: Эта тема предоставляет информацию о запросе графика расходов федеральных наград.
author: velofog
manager: Ann Beebe
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 70dff12c106723dda801668412cfd084c462db4b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288980"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="5f96f-103">Запрос графика расходов федеральных наград</span><span class="sxs-lookup"><span data-stu-id="5f96f-103">Schedule of Expenditures of Federal Awards inquiry</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5f96f-104">Согласно циркуляру A-133 Управления по управлению и бюджету, агентства, получающие федеральные средства, подчиняются требованиям аудита, которые также известны как единый аудит.</span><span class="sxs-lookup"><span data-stu-id="5f96f-104">According to Office of Management and Budget Circular A-133, agencies that receive federal funds are subject to audit requirements, which are also known as single audits.</span></span> <span data-ttu-id="5f96f-105">Процесс аудита используется для составления отчетов о доходах и расходах по федеральным грантам на регулярной основе.</span><span class="sxs-lookup"><span data-stu-id="5f96f-105">The audit process is used to report on the revenues and expenditures of federal grants on a recurring basis.</span></span> <span data-ttu-id="5f96f-106">Часть единого аудиторского отчета включает график расходов по федеральным грантам (SEFA).</span><span class="sxs-lookup"><span data-stu-id="5f96f-106">Part of the single audit report includes the Schedule of Expenditures of Federal Awards (SEFA).</span></span>

<span data-ttu-id="5f96f-107">Запрос графика расходов по федеральным заказам включает название и номер Каталога федеральной внутренней помощи (CFDA), номер гранта, год предоставления гранта, название федерального агентства, которое предоставляет средства, и название сквозной сущности.</span><span class="sxs-lookup"><span data-stu-id="5f96f-107">The Schedule of Expenditures of Federal Awards inquiry includes the Catalog of Federal Domestic Assistance (CFDA) title and number, the grant number, the year of the grant, the name of the federal agency that provides the funds, and the name of the pass-through entity.</span></span> <span data-ttu-id="5f96f-108">Запрос рассчитан на определенный период.</span><span class="sxs-lookup"><span data-stu-id="5f96f-108">The inquiry is for a specific period.</span></span> <span data-ttu-id="5f96f-109">Как правило, этот период совпадает с периодом финансового отчета, то есть финансовый год.</span><span class="sxs-lookup"><span data-stu-id="5f96f-109">Typically, that period is the same as the financial statement period, which is a fiscal year.</span></span>

<span data-ttu-id="5f96f-110">Запрос включает гранты, прогнозные даты которых находятся в выбранном диапазоне дат.</span><span class="sxs-lookup"><span data-stu-id="5f96f-110">The inquiry includes grants that have projection dates in the selected date range.</span></span> <span data-ttu-id="5f96f-111">В столбце **Агентство грантодателя** запроса указан заказчик гранта или, в случае сквозного гранта, агентство, предоставляющее грант.</span><span class="sxs-lookup"><span data-stu-id="5f96f-111">The **Grantor agency** column of the inquiry shows the grant customer or, for a pass-through grant, the grantor agency.</span></span> <span data-ttu-id="5f96f-112">Для сквозного гранта в столбце **Сквозное агентство** показывается заказчик гранта.</span><span class="sxs-lookup"><span data-stu-id="5f96f-112">For a pass-through grant, the **Pass-through agency** column shows the grant customer.</span></span> <span data-ttu-id="5f96f-113">Если гран не является сквозным грантом, столбец **Сквозное агентство** является пустым.</span><span class="sxs-lookup"><span data-stu-id="5f96f-113">If the grant isn't a pass-through grant, the **Pass-through agency** column is blank.</span></span>

## <a name="set-up-the-cfda-clusters"></a><span data-ttu-id="5f96f-114">Настройка кластеров CFDA</span><span class="sxs-lookup"><span data-stu-id="5f96f-114">Set up the CFDA clusters</span></span>

<span data-ttu-id="5f96f-115">Вы должны настроить кластеры CFDA, которые могут быть связаны с номерами CFDA в запросе "График расходов по федеральным грантам".</span><span class="sxs-lookup"><span data-stu-id="5f96f-115">You must set up the CFDA clusters that can be associated with CFDA numbers in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="5f96f-116">Перейдите в раздел **Управление и учет по проектам \> Настройка \> Гранты \> Каталог кластеров федеральной внутренней помощи**.</span><span class="sxs-lookup"><span data-stu-id="5f96f-116">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance clusters**.</span></span>
2. <span data-ttu-id="5f96f-117">Выберите **Создать**, чтобы создать кластер CFDA.</span><span class="sxs-lookup"><span data-stu-id="5f96f-117">Select **New** to create a CFDA cluster.</span></span>
3. <span data-ttu-id="5f96f-118">Введите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="5f96f-118">Enter the cluster name.</span></span>
4. <span data-ttu-id="5f96f-119">Выберите **Сохранить**, чтобы сохранить изменения.</span><span class="sxs-lookup"><span data-stu-id="5f96f-119">Select **Save** to save your changes.</span></span>

## <a name="set-up-cfda-numbers"></a><span data-ttu-id="5f96f-120">Настройка номеров CFDA</span><span class="sxs-lookup"><span data-stu-id="5f96f-120">Set up CFDA numbers</span></span>

<span data-ttu-id="5f96f-121">Вы должны настроить номера CFDA, которые могут быть добавлены в гранты и включены в запрос "График расходов по федеральным грантам".</span><span class="sxs-lookup"><span data-stu-id="5f96f-121">You must set up CFDA numbers that can be added to grants and included in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="5f96f-122">Перейдите в раздел **Управление и учет по проектам \> Настройка \> Гранты \> Номера каталога кластеров федеральной внутренней помощи**.</span><span class="sxs-lookup"><span data-stu-id="5f96f-122">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance numbers**.</span></span>
2. <span data-ttu-id="5f96f-123">Выберите **Создать**, чтобы создать номер CFDA.</span><span class="sxs-lookup"><span data-stu-id="5f96f-123">Select **New** to create a CFDA number.</span></span>
3. <span data-ttu-id="5f96f-124">В столбце **Число** введите номер CFDA.</span><span class="sxs-lookup"><span data-stu-id="5f96f-124">In the **Number** column, enter the CFDA number.</span></span>
4. <span data-ttu-id="5f96f-125">Нажмите клавишу **Tab**.</span><span class="sxs-lookup"><span data-stu-id="5f96f-125">Press the **Tab** key.</span></span>
5. <span data-ttu-id="5f96f-126">В столбце **Описание** введите заголовок CFDA.</span><span class="sxs-lookup"><span data-stu-id="5f96f-126">In the **Description** column, enter the CFDA title.</span></span>
6. <span data-ttu-id="5f96f-127">Нажмите клавишу **Tab**.</span><span class="sxs-lookup"><span data-stu-id="5f96f-127">Press the **Tab** key.</span></span>
7. <span data-ttu-id="5f96f-128">Необязательно: в поле **Кластер программы** добавьте соответствующий кластер CFDA.</span><span class="sxs-lookup"><span data-stu-id="5f96f-128">Optional: In the **Program cluster** field, add the appropriate CFDA cluster.</span></span>
8. <span data-ttu-id="5f96f-129">Выберите **Сохранить**, чтобы сохранить изменения.</span><span class="sxs-lookup"><span data-stu-id="5f96f-129">Select **Save** to save your changes.</span></span>

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="5f96f-130">Настройка грантов для отчета по запросу о графике расходов федеральных наград</span><span class="sxs-lookup"><span data-stu-id="5f96f-130">Set up grants to report for the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="5f96f-131">Перейдите в раздел **Управление и учет по проектам \> Гранты \> Гранты** и выберите существующий грант.</span><span class="sxs-lookup"><span data-stu-id="5f96f-131">Go to **Project management and accounting \> Grants \> Grants**, and select an existing grant.</span></span>
2. <span data-ttu-id="5f96f-132">На экспресс-вкладке **Настройка** в поле **Каталог федеральной внутренней помощи** присвойте номер CFDA.</span><span class="sxs-lookup"><span data-stu-id="5f96f-132">On the **Setup** FastTab, in the **Catalog of Federal Domestic Assistance** field, assign the CFDA number.</span></span> <span data-ttu-id="5f96f-133">Номер CFDA на гранте определяет кластер CFDA для отчетности.</span><span class="sxs-lookup"><span data-stu-id="5f96f-133">The CFDA number on the grant determines the CFDA cluster for reporting.</span></span>
3. <span data-ttu-id="5f96f-134">На экспресс-вкладке **Контактные данные** введите информацию о грантодателе, выполнив следующие действия:</span><span class="sxs-lookup"><span data-stu-id="5f96f-134">On **Contact information** FastTab, enter the grantor information by following these steps:</span></span>

    1. <span data-ttu-id="5f96f-135">В поле **Клиент гранта** введите клиента, ответственного за грант.</span><span class="sxs-lookup"><span data-stu-id="5f96f-135">In the **Grant customer** field, enter the customer who is responsible for the grant.</span></span> <span data-ttu-id="5f96f-136">Для существующего гранта эта информация может быть уже введена.</span><span class="sxs-lookup"><span data-stu-id="5f96f-136">For an existing grant, this information might already be entered.</span></span>
    2. <span data-ttu-id="5f96f-137">Укажите, является ли клиент гранта спонсором.</span><span class="sxs-lookup"><span data-stu-id="5f96f-137">Indicate whether the grant customer is the funder.</span></span> <span data-ttu-id="5f96f-138">Если клиент гранта является спонсором, оставьте флажок **Сквозной режим** снятым.</span><span class="sxs-lookup"><span data-stu-id="5f96f-138">If the grant customer is the funder, leave the **Pass-through** check box cleared.</span></span> <span data-ttu-id="5f96f-139">Если другой клиент является спонсором, а клиент гранта несет ответственность за расходование и отслеживание денежных средство, установите флажок **Сквозной режим**.</span><span class="sxs-lookup"><span data-stu-id="5f96f-139">If another customer is the funder, and the grant customer is responsible for spending and tracking the money, select the **Pass-through** check box.</span></span>

4. <span data-ttu-id="5f96f-140">Если вы установили флажок **Сквозной режим** на предыдущем шаге, в поле **Агентство грантодателя** введите клиента, предоставившего грант.</span><span class="sxs-lookup"><span data-stu-id="5f96f-140">If you selected the **Pass-through** check box in the previous step, in the **Grantor agency** field, enter the customer who provided the grant.</span></span> <span data-ttu-id="5f96f-141">Агентство, предоставляющее грант, и клиент гранта не могут быть одним и тем же клиентом.</span><span class="sxs-lookup"><span data-stu-id="5f96f-141">The grantor agency and the grant customer can't be the same customer.</span></span>

<span data-ttu-id="5f96f-142">Вот пример сквозного гранта:</span><span class="sxs-lookup"><span data-stu-id="5f96f-142">Here is an example of a pass-through grant:</span></span>

<span data-ttu-id="5f96f-143">Федеральное правительство профинансировало инфраструктурный проект штата.</span><span class="sxs-lookup"><span data-stu-id="5f96f-143">The federal government funded an infrastructure project for a state.</span></span> <span data-ttu-id="5f96f-144">Федеральное правительство предоставило штату денежные средства на расходы.</span><span class="sxs-lookup"><span data-stu-id="5f96f-144">The federal government gave the money to the state to spend.</span></span> <span data-ttu-id="5f96f-145">В этом случае федеральное правительство является органом, предоставляющим грант, а штат — клиентом гранта.</span><span class="sxs-lookup"><span data-stu-id="5f96f-145">In this case, the federal government is the grantor agency, and the state is the grant customer.</span></span>

> [!NOTE] 
> <span data-ttu-id="5f96f-146">Когда вы впервые включаете эту функцию, начальные номера CFDA будут вводиться с использованием существующих номеров грантов.</span><span class="sxs-lookup"><span data-stu-id="5f96f-146">When you first turn on the feature, initial CFDA numbers will be entered by using the existing numbers on grants.</span></span>

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a><span data-ttu-id="5f96f-147">Исключение грантов из отчетности SEFA в зависимости от типа гранта</span><span class="sxs-lookup"><span data-stu-id="5f96f-147">Exclude grants from SEFA reporting based on the grant type</span></span>

1. <span data-ttu-id="5f96f-148">Перейдите в раздел **Управление и учет по проектам \> Настройка \> Гранты \> Типы грантов**.</span><span class="sxs-lookup"><span data-stu-id="5f96f-148">Go to **Project management and accounting \> Setup \> Grants \> Grant types**.</span></span>
2. <span data-ttu-id="5f96f-149">На экспресс-вкладке **Информация по умолчанию** выберите флажок **Исключить из графика расходов федеральных премий**.</span><span class="sxs-lookup"><span data-stu-id="5f96f-149">On the **Default information** FastTab, select the **Exclude from Schedule of Expenditures of Federal Awards** check box.</span></span>
3. <span data-ttu-id="5f96f-150">Выберите **Сохранить**, чтобы сохранить изменения.</span><span class="sxs-lookup"><span data-stu-id="5f96f-150">Select **Save** to save your changes.</span></span>

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="5f96f-151">Запуск запроса графика расходов федеральных наград</span><span class="sxs-lookup"><span data-stu-id="5f96f-151">Run the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="5f96f-152">Перейдите в раздел **Управление и учет по проектам \> Запросы и отчеты \> Запрос гранта \> График расходов федеральных наград**.</span><span class="sxs-lookup"><span data-stu-id="5f96f-152">Go to **Project management and accounting \> Inquiries and reports \> Grant inquiry \> Schedule of Expenditures of Federal Awards**.</span></span>
2. <span data-ttu-id="5f96f-153">В разделе **Параметры** выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="5f96f-153">In the **Parameters** section, follow these steps:</span></span>

    1. <span data-ttu-id="5f96f-154">В поле **Интервал дат** выберите код для интервала дат.</span><span class="sxs-lookup"><span data-stu-id="5f96f-154">In the **Date interval** field, select the code for the date interval.</span></span> <span data-ttu-id="5f96f-155">В качестве альтернативы в полях **Дата начала** и **Дата окончания** определите интервал дат.</span><span class="sxs-lookup"><span data-stu-id="5f96f-155">Alternatively, in the **From date** and **To date** fields, define the date interval.</span></span>
    2. <span data-ttu-id="5f96f-156">Необязательно: чтобы включить в запрос только транзакции с выставленными счетами, установите для параметра **Включать только доходы с выставленными счетами** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="5f96f-156">Optional: To include only billed transactions as revenue in the inquiry, set the **Include only billed revenues** option to **Yes**.</span></span>

## <a name="columns"></a><span data-ttu-id="5f96f-157">Число столбцов</span><span class="sxs-lookup"><span data-stu-id="5f96f-157">Columns</span></span>

<span data-ttu-id="5f96f-158">Запрос графика расходов федеральных наград включает следующие столбцы:</span><span class="sxs-lookup"><span data-stu-id="5f96f-158">The Schedule of Expenditures of Federal Awards inquiry includes the following columns:</span></span>

- <span data-ttu-id="5f96f-159">Наименование кластера каталога федеральной внутренней помощи</span><span class="sxs-lookup"><span data-stu-id="5f96f-159">Catalog of Federal Domestic Assistance cluster name</span></span>
- <span data-ttu-id="5f96f-160">Агентство грантодателя</span><span class="sxs-lookup"><span data-stu-id="5f96f-160">Grantor agency</span></span>
- <span data-ttu-id="5f96f-161">Сквозное агентство</span><span class="sxs-lookup"><span data-stu-id="5f96f-161">Pass-through agency</span></span>
- <span data-ttu-id="5f96f-162">Имя гранта</span><span class="sxs-lookup"><span data-stu-id="5f96f-162">Grant name</span></span>
- <span data-ttu-id="5f96f-163">Код гранта</span><span class="sxs-lookup"><span data-stu-id="5f96f-163">Grant ID</span></span>
- <span data-ttu-id="5f96f-164">Код приложения гранта</span><span class="sxs-lookup"><span data-stu-id="5f96f-164">Grant application ID</span></span>
- <span data-ttu-id="5f96f-165">Каталог федеральной внутренней помощи</span><span class="sxs-lookup"><span data-stu-id="5f96f-165">Catalog of Federal Domestic Assistance</span></span>
- <span data-ttu-id="5f96f-166">Получения</span><span class="sxs-lookup"><span data-stu-id="5f96f-166">Receipts</span></span>
- <span data-ttu-id="5f96f-167">Расходы</span><span class="sxs-lookup"><span data-stu-id="5f96f-167">Expenditures</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]