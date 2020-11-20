---
title: Обзор утверждений
description: В этой теме предоставлена информация о работе с утверждениями в Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 14c6914cf9b5fb52e7554e51604e79f0920064df
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123844"
---
# <a name="approvals-overview"></a><span data-ttu-id="9c25c-103">Обзор утверждений</span><span class="sxs-lookup"><span data-stu-id="9c25c-103">Approvals overview</span></span>

<span data-ttu-id="9c25c-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="9c25c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9c25c-105">Отправки времени и расходов проходят через рабочий процесс утверждения.</span><span class="sxs-lookup"><span data-stu-id="9c25c-105">Time and Expense submissions move through an approval workflow.</span></span> <span data-ttu-id="9c25c-106">После утверждения записей транзакции записываются в фактических данных или время регистрируется в расписании.</span><span class="sxs-lookup"><span data-stu-id="9c25c-106">After the entries are approved, transactions are recorded in actuals or time is booked in the schedule.</span></span>

## <a name="approvals-workflow"></a><span data-ttu-id="9c25c-107">Рабочий процесс утверждений</span><span class="sxs-lookup"><span data-stu-id="9c25c-107">Approvals workflow</span></span>
<span data-ttu-id="9c25c-108">Когда вы создаете и отправляете запись о времени или расходах, создается запись утверждения.</span><span class="sxs-lookup"><span data-stu-id="9c25c-108">When you create and submit a time or expense entry, an approval entry is created.</span></span> <span data-ttu-id="9c25c-109">Утверждающий проекта или ваш руководитель просматривает и утверждает вашу запись.</span><span class="sxs-lookup"><span data-stu-id="9c25c-109">The Project approver or your manager reviews and approves your entry.</span></span> <span data-ttu-id="9c25c-110">Если запись связана с проектом, после утверждения будут созданы фактические данные.</span><span class="sxs-lookup"><span data-stu-id="9c25c-110">If the entry is related to a project, when it's approved, the actuals will be created.</span></span> <span data-ttu-id="9c25c-111">Это позволяет отслеживать стоимость и выставление счетов.</span><span class="sxs-lookup"><span data-stu-id="9c25c-111">This allows the cost and billing to be tracked.</span></span> 

## <a name="approve-an-entry"></a><span data-ttu-id="9c25c-112">Утверждение записи</span><span class="sxs-lookup"><span data-stu-id="9c25c-112">Approve an entry</span></span>
<span data-ttu-id="9c25c-113">Форма **Утверждения** позволяет переключаться между различными представлениями, чтобы вы могли просматривать различные типы утверждений.</span><span class="sxs-lookup"><span data-stu-id="9c25c-113">The **Approvals** form allows you to switch between different views so that you can view the different types of approvals.</span></span>
  
1. <span data-ttu-id="9c25c-114">Перейдите на форму **Утверждения** и выберите **Затраты**, **Время** или **Отзывы**.</span><span class="sxs-lookup"><span data-stu-id="9c25c-114">Go to the **Approvals** form and select **Expenses**, **Time**, or **Recalls**.</span></span>
2. <span data-ttu-id="9c25c-115">Просмотрите каждое утверждение и выберите те, которые хотите утвердить.</span><span class="sxs-lookup"><span data-stu-id="9c25c-115">Review each approval, and select the ones you want to approve.</span></span>
3. <span data-ttu-id="9c25c-116">Выберите **Утвердить** для утверждения выбранных записей.</span><span class="sxs-lookup"><span data-stu-id="9c25c-116">Select **Approve** to approve the selected entries.</span></span>
<span data-ttu-id="9c25c-117">Система обработает эти записи и создаст фактические данные или резервирование.</span><span class="sxs-lookup"><span data-stu-id="9c25c-117">The system will process these entries and create actuals or a booking.</span></span>

## <a name="reject-an-entry"></a><span data-ttu-id="9c25c-118">Отклонение записи</span><span class="sxs-lookup"><span data-stu-id="9c25c-118">Reject an entry</span></span>
<span data-ttu-id="9c25c-119">В качестве лица, утверждающего проект, вам, возможно, придется отправить запись обратно пользователю для исправления.</span><span class="sxs-lookup"><span data-stu-id="9c25c-119">As the Project approver, you may have to send an entry back to a user for correction.</span></span>
  
1. <span data-ttu-id="9c25c-120">Перейдите к форме **Утверждения** и выберите запись, которую нужно отклонить.</span><span class="sxs-lookup"><span data-stu-id="9c25c-120">Go to the **Approvals** form and select the entry to reject.</span></span> 
2. <span data-ttu-id="9c25c-121">Выберите **Отклонить**.</span><span class="sxs-lookup"><span data-stu-id="9c25c-121">Select **Reject**.</span></span>
3. <span data-ttu-id="9c25c-122">Необязательно — добавьте комментарий в диалог **Комментарии отклонения**, чтобы проинформировать пользователя, почему запись отклоняется.</span><span class="sxs-lookup"><span data-stu-id="9c25c-122">Optional - Add a comment in the **Rejection Comments** dialog to inform the user why the entry is being rejected.</span></span>
4. <span data-ttu-id="9c25c-123">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="9c25c-123">Select **OK**.</span></span> <span data-ttu-id="9c25c-124">Запись будет возвращена пользователю.</span><span class="sxs-lookup"><span data-stu-id="9c25c-124">The entry will be returned to the user.</span></span>
  
## <a name="recall-entries"></a><span data-ttu-id="9c25c-125">Отзыв записей</span><span class="sxs-lookup"><span data-stu-id="9c25c-125">Recall entries</span></span>
<span data-ttu-id="9c25c-126">В какой-то момент вам может потребоваться отозвать отправленную запись.</span><span class="sxs-lookup"><span data-stu-id="9c25c-126">At some point, you might need to recall a submitted entry.</span></span> <span data-ttu-id="9c25c-127">Если запись не была одобрена, она будет немедленно возвращена.</span><span class="sxs-lookup"><span data-stu-id="9c25c-127">If the entry has not been approved, it will be returned immediately.</span></span> <span data-ttu-id="9c25c-128">Однако одобренная запись может иметь существенное влияние.</span><span class="sxs-lookup"><span data-stu-id="9c25c-128">An approved entry however, may have a material impact.</span></span> <span data-ttu-id="9c25c-129">Утверждающий проекта должен утвердить отзыв, чтобы отменить транзакцию в фактических данных.</span><span class="sxs-lookup"><span data-stu-id="9c25c-129">The Project approver is required to approve the recall in order to reverse the transaction in Actuals.</span></span>

## <a name="specify-project-approvers"></a><span data-ttu-id="9c25c-130">Указание утверждающих проекта</span><span class="sxs-lookup"><span data-stu-id="9c25c-130">Specify Project approvers</span></span>
<span data-ttu-id="9c25c-131">В каждом проекте есть несколько участников рабочей группы проекта.</span><span class="sxs-lookup"><span data-stu-id="9c25c-131">Each project has a number of project team members.</span></span> <span data-ttu-id="9c25c-132">Вы можете указать, какие участники рабочей группы также являются утверждающими.</span><span class="sxs-lookup"><span data-stu-id="9c25c-132">You can specify which team members are also Project approvers.</span></span>

1. <span data-ttu-id="9c25c-133">Перейдите в форму **Проекты** и откройте проект из списка.</span><span class="sxs-lookup"><span data-stu-id="9c25c-133">Go to the **Projects** form and open the project from the list.</span></span>
2. <span data-ttu-id="9c25c-134">На вкладке **Рабочая группа** выберите участника рабочей группы, который будет утверждающим для проекта, затем выберите **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="9c25c-134">On the **Team** tab, select the team member who will be a Project approver and then select **Edit**.</span></span>
3. <span data-ttu-id="9c25c-135">Задайте в поле **Утверждающий проекта** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="9c25c-135">Set the **Project Approver** field to **Yes**.</span></span>
4. <span data-ttu-id="9c25c-136">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="9c25c-136">Select **Save**.</span></span>
5. <span data-ttu-id="9c25c-137">Чтобы добавить еще утверждающих для проекта, повторите шаги со 2 по 4.</span><span class="sxs-lookup"><span data-stu-id="9c25c-137">Repeat steps 2-4 to add additional Project approvers.</span></span>

## <a name="configure-the-users-manager"></a><span data-ttu-id="9c25c-138">Настройка руководителя пользователя</span><span class="sxs-lookup"><span data-stu-id="9c25c-138">Configure the user's manager</span></span>

1. <span data-ttu-id="9c25c-139">Выберите **Параметры** > **Безопасность** > **Пользователи**.</span><span class="sxs-lookup"><span data-stu-id="9c25c-139">Go to **Settings** > **Security** > **Users**.</span></span>
2. <span data-ttu-id="9c25c-140">Выберите пользователя, которому вы назначаете менеджера, и в области **Информация об организации** выберите менеджера из списка.</span><span class="sxs-lookup"><span data-stu-id="9c25c-140">Select the user to whom you are assigning a manager and in the **Organization Information** area, select the manager from the list.</span></span> 
3. <span data-ttu-id="9c25c-141">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="9c25c-141">Select **Save**.</span></span>


