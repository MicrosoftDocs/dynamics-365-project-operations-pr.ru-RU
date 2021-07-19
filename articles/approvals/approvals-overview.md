---
title: Обзор утверждений
description: В этой теме предоставлена информация о работе с утверждениями в Project Operations.
author: stsporen
ms.date: 03/31/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.custom: intro-internal
ms.openlocfilehash: 9148c9f55e8664850c38aebbc9c4bbaa243475ad
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368672"
---
# <a name="approvals-overview"></a><span data-ttu-id="aac4b-103">Обзор утверждений</span><span class="sxs-lookup"><span data-stu-id="aac4b-103">Approvals overview</span></span>

<span data-ttu-id="aac4b-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="aac4b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="aac4b-105">Отправка сведений о времени, расходам и использовании материалов проходит через бизнес-процесс утверждения.</span><span class="sxs-lookup"><span data-stu-id="aac4b-105">Time, expense, and material usage submissions move through an approval workflow.</span></span> <span data-ttu-id="aac4b-106">После утверждения записей транзакции записываются в фактических данных или время регистрируется в расписании.</span><span class="sxs-lookup"><span data-stu-id="aac4b-106">After the entries are approved, transactions are recorded in actuals or time is booked in the schedule.</span></span>

## <a name="approvals-workflow"></a><span data-ttu-id="aac4b-107">Рабочий процесс утверждений</span><span class="sxs-lookup"><span data-stu-id="aac4b-107">Approvals workflow</span></span>
<span data-ttu-id="aac4b-108">Когда вы создаете и отправляете запись времени, расходов или использования материалов, создается запись утверждения.</span><span class="sxs-lookup"><span data-stu-id="aac4b-108">When you create and submit a time, expense, or material usage entry, an approval record is created.</span></span> <span data-ttu-id="aac4b-109">Утверждающий по проекту или руководитель просматривает и одобряет запись.</span><span class="sxs-lookup"><span data-stu-id="aac4b-109">The project approver or manager reviews and approves the entry.</span></span> <span data-ttu-id="aac4b-110">Если запись связана с проектом, фактические значения будут созданы после его утверждения.</span><span class="sxs-lookup"><span data-stu-id="aac4b-110">If the entry is related to a project, the actuals will be created when it's approved.</span></span> <span data-ttu-id="aac4b-111">Это позволяет отслеживать стоимость и выставление счетов.</span><span class="sxs-lookup"><span data-stu-id="aac4b-111">This allows the cost and billing to be tracked.</span></span>

## <a name="approve-an-entry"></a><span data-ttu-id="aac4b-112">Утверждение записи</span><span class="sxs-lookup"><span data-stu-id="aac4b-112">Approve an entry</span></span>
<span data-ttu-id="aac4b-113">На странице **Утверждения** можно переключаться между различными представлениями, чтобы вы могли просматривать различные типы утверждений.</span><span class="sxs-lookup"><span data-stu-id="aac4b-113">The **Approvals** page allows you to switch between different views so that you can view the different types of approvals.</span></span>
  
1. <span data-ttu-id="aac4b-114">Перейдите на страницу **Утверждения** и выберите **Расходы**, **Время**, **Использование материалов** или **Отзыв**.</span><span class="sxs-lookup"><span data-stu-id="aac4b-114">Go to the **Approvals** page and select **Expenses**, **Time**, **Material Usage**, or **Recalls**.</span></span>
2. <span data-ttu-id="aac4b-115">Просмотрите каждое утверждение и выберите те, которые хотите утвердить.</span><span class="sxs-lookup"><span data-stu-id="aac4b-115">Review each approval, and select the ones you want to approve.</span></span>
3. <span data-ttu-id="aac4b-116">Выберите **Утвердить** для утверждения выбранных записей.</span><span class="sxs-lookup"><span data-stu-id="aac4b-116">Select **Approve** to approve the selected entries.</span></span>
<span data-ttu-id="aac4b-117">Система обрабатывает эти записи и создает фактические значения.</span><span class="sxs-lookup"><span data-stu-id="aac4b-117">The system processes these entries and create actuals.</span></span>

## <a name="reject-an-entry"></a><span data-ttu-id="aac4b-118">Отклонение записи</span><span class="sxs-lookup"><span data-stu-id="aac4b-118">Reject an entry</span></span>
<span data-ttu-id="aac4b-119">В качестве лица, утверждающего проект, вам, возможно, придется отправить запись обратно пользователю для исправления.</span><span class="sxs-lookup"><span data-stu-id="aac4b-119">As the Project approver, you may have to send an entry back to a user for correction.</span></span>
  
1. <span data-ttu-id="aac4b-120">Перейдите на страницу **Утверждения** и выберите запись, которую нужно отклонить.</span><span class="sxs-lookup"><span data-stu-id="aac4b-120">Go to the **Approvals** page and select the entry to reject.</span></span> 
2. <span data-ttu-id="aac4b-121">Выберите **Отклонить**.</span><span class="sxs-lookup"><span data-stu-id="aac4b-121">Select **Reject**.</span></span>
3. <span data-ttu-id="aac4b-122">Необязательно: добавьте комментарий в диалоговом окне **Комментарии к отклонению**, чтобы проинформировать пользователя, почему запись отклоняется.</span><span class="sxs-lookup"><span data-stu-id="aac4b-122">Optional, add a comment in the **Rejection Comments** dialog box to inform the user why the entry is being rejected.</span></span>
4. <span data-ttu-id="aac4b-123">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="aac4b-123">Select **OK**.</span></span> <span data-ttu-id="aac4b-124">Запись будет возвращена пользователю.</span><span class="sxs-lookup"><span data-stu-id="aac4b-124">The entry will be returned to the user.</span></span>
  
## <a name="cancel-approval"></a><span data-ttu-id="aac4b-125">Отменить утверждение</span><span class="sxs-lookup"><span data-stu-id="aac4b-125">Cancel approval</span></span>
<span data-ttu-id="aac4b-126">В некоторых случаях вам может потребоваться отменить ранее утвержденную запись.</span><span class="sxs-lookup"><span data-stu-id="aac4b-126">In some cases, you might need to cancel a previously approved entry.</span></span> <span data-ttu-id="aac4b-127">Отмена ранее утвержденной записи повлечет финансовые последствия.</span><span class="sxs-lookup"><span data-stu-id="aac4b-127">Canceling a previously approved entry will have a financial impact.</span></span> 

## <a name="approving-recall-requests"></a><span data-ttu-id="aac4b-128">Утверждение запросов на отклонение</span><span class="sxs-lookup"><span data-stu-id="aac4b-128">Approving recall requests</span></span>
<span data-ttu-id="aac4b-129">В некоторых случаях консультанту может потребоваться отозвать ранее утвержденную запись.</span><span class="sxs-lookup"><span data-stu-id="aac4b-129">In some cases, a consultant may need to recall a previously approved entry.</span></span> <span data-ttu-id="aac4b-130">Отмена ранее утвержденной записи повлечет финансовые последствия.</span><span class="sxs-lookup"><span data-stu-id="aac4b-130">Canceling a previously approved entry will have a financial impact.</span></span> <span data-ttu-id="aac4b-131">Утверждающий по проекту должен утвердить отзыв, чтобы отменить транзакцию в фактических данных.</span><span class="sxs-lookup"><span data-stu-id="aac4b-131">The project approver is required to approve the recall to reverse the transaction in Actuals.</span></span>

## <a name="specify-project-approvers"></a><span data-ttu-id="aac4b-132">Указание утверждающих проекта</span><span class="sxs-lookup"><span data-stu-id="aac4b-132">Specify Project approvers</span></span>
<span data-ttu-id="aac4b-133">В каждом проекте есть несколько участников рабочей группы проекта.</span><span class="sxs-lookup"><span data-stu-id="aac4b-133">Each project has a number of project team members.</span></span> <span data-ttu-id="aac4b-134">Вы можете указать, какие участники рабочей группы также являются утверждающими.</span><span class="sxs-lookup"><span data-stu-id="aac4b-134">You can specify which team members are also Project approvers.</span></span>

1. <span data-ttu-id="aac4b-135">Перейдите на страницу **Проекты** и откройте проект из списка.</span><span class="sxs-lookup"><span data-stu-id="aac4b-135">Go to the **Projects** page and open the project from the list.</span></span>
2. <span data-ttu-id="aac4b-136">На вкладке **Рабочая группа** выберите участника рабочей группы, который будет утверждающим для проекта, затем выберите **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="aac4b-136">On the **Team** tab, select the team member who will be a Project approver and then select **Edit**.</span></span>
3. <span data-ttu-id="aac4b-137">Задайте в поле **Утверждающий проекта** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="aac4b-137">Set the **Project Approver** field to **Yes**.</span></span>
4. <span data-ttu-id="aac4b-138">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="aac4b-138">Select **Save**.</span></span>
5. <span data-ttu-id="aac4b-139">Чтобы добавить еще утверждающих для проекта, повторите шаги со 2 по 4.</span><span class="sxs-lookup"><span data-stu-id="aac4b-139">Repeat steps 2-4 to add additional Project approvers.</span></span>

## <a name="configure-the-users-manager"></a><span data-ttu-id="aac4b-140">Настройка руководителя пользователя</span><span class="sxs-lookup"><span data-stu-id="aac4b-140">Configure the user's manager</span></span>

1. <span data-ttu-id="aac4b-141">Выберите **Параметры** > **Безопасность** > **Пользователи**.</span><span class="sxs-lookup"><span data-stu-id="aac4b-141">Go to **Settings** > **Security** > **Users**.</span></span>
2. <span data-ttu-id="aac4b-142">Выберите пользователя, которому вы назначаете менеджера, и в области **Информация об организации** выберите менеджера из списка.</span><span class="sxs-lookup"><span data-stu-id="aac4b-142">Select the user to whom you are assigning a manager and in the **Organization Information** area, select the manager from the list.</span></span> 
3. <span data-ttu-id="aac4b-143">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="aac4b-143">Select **Save**.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
