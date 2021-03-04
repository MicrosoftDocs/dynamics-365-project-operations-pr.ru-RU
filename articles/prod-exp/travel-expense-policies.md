---
title: Настройка политик расходов
description: Вы можете настроить политики расходов, которым ваши сотрудники должны следовать при вводе и отправке отчетов о расходах и заявок на командировки в Microsoft Dynamics 365 Finance.
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ab99c0ec769eb2e0914fc7d993f83d20e2c327f6
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960713"
---
# <a name="set-up-expense-policies"></a><span data-ttu-id="fa7eb-103">Настройка политик расходов</span><span class="sxs-lookup"><span data-stu-id="fa7eb-103">Set up expense policies</span></span>

<span data-ttu-id="fa7eb-104">Вы можете определить политики, которым ваши сотрудники должны следовать при вводе и отправке отчетов о расходах и заявок на командировки.</span><span class="sxs-lookup"><span data-stu-id="fa7eb-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="fa7eb-105">Внедрение политик расходов может помочь вам эффективно управлять расходами.</span><span class="sxs-lookup"><span data-stu-id="fa7eb-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="fa7eb-106">Например, вы можете установить политику расходов на гостиницу в Нью-Йорке, которая гласит, что суточные расходы не могут превышать 250 долларов США.</span><span class="sxs-lookup"><span data-stu-id="fa7eb-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="fa7eb-107">Если работник отправляет отчет о расходах или заявку на командировку, в котором стоимость номера превышает эту сумму, система уведомит</span><span class="sxs-lookup"><span data-stu-id="fa7eb-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="fa7eb-108">сотрудника, что сумма политики для расходов была превышена.</span><span class="sxs-lookup"><span data-stu-id="fa7eb-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="fa7eb-109">Вы можете настроить сообщение, которое работник будет получать, когда вы</span><span class="sxs-lookup"><span data-stu-id="fa7eb-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="fa7eb-110">определили политику.</span><span class="sxs-lookup"><span data-stu-id="fa7eb-110">define the policy.</span></span>      
        
<span data-ttu-id="fa7eb-111">Можно определить три типа политик:</span><span class="sxs-lookup"><span data-stu-id="fa7eb-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="fa7eb-112">Предупреждение — позволяет работнику подавать отчет о расходах или заявку на командировку, но расходы будут отмечены для всех утверждающих и</span><span class="sxs-lookup"><span data-stu-id="fa7eb-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="fa7eb-113">для последующего отчета.</span><span class="sxs-lookup"><span data-stu-id="fa7eb-113">for later reporting.</span></span>        

- <span data-ttu-id="fa7eb-114">Ошибка — требует, чтобы работник пересмотрел расходы в соответствии с политикой перед отправкой отчета о расходах или заявки на командировку.</span><span class="sxs-lookup"><span data-stu-id="fa7eb-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
 - <span data-ttu-id="fa7eb-115">Обоснование — требует от работника или менеджера ввести обоснование превышения суммы по политике перед подачей отчета о расходах или заявки на командировку.</span><span class="sxs-lookup"><span data-stu-id="fa7eb-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="fa7eb-116">Советы по политикам</span><span class="sxs-lookup"><span data-stu-id="fa7eb-116">Policy tips</span></span>
<span data-ttu-id="fa7eb-117">Вот несколько советов, которые могут помочь вам при создании новых политик для управления расходами.</span><span class="sxs-lookup"><span data-stu-id="fa7eb-117">Here are a few suggestions that can assist you when creating new policies for expense management.</span></span> 
* <span data-ttu-id="fa7eb-118">Политики действуют по датам и не вступают в силу, если политика создана с датой, более поздней, чем дата, когда произошли расходы.</span><span class="sxs-lookup"><span data-stu-id="fa7eb-118">Policies are date effective and won't take effect if the policy is created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="fa7eb-119">Например, если вы создаете новую политику сегодня, чтобы обеспечить максимальный расход на еду в размере 50 долларов США, то любые существующие расходы, введенные до вчерашнего дня, не будут проверяться на соответствие этой политике.</span><span class="sxs-lookup"><span data-stu-id="fa7eb-119">For example, if you are creating a new policy today to enforce a maximum meal expense of $50, then any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
* <span data-ttu-id="fa7eb-120">При создании политики для категории расходов, которая может быть детализирована, рассмотрите возможность добавления условия для типа строки расходов.</span><span class="sxs-lookup"><span data-stu-id="fa7eb-120">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="fa7eb-121">Некоторые политики, такие как требование квитанции, могут не иметь смысла для строк с детализацией и должны применяться только к строке заголовка или строке без детализации.</span><span class="sxs-lookup"><span data-stu-id="fa7eb-121">Some policies such as requiring a receipt may not make sense for itemized lines and should only be applied to the header line or a non-itemized line.</span></span> 
* <span data-ttu-id="fa7eb-122">По умолчанию политики управления расходами сравниваются с исходной сущностью.</span><span class="sxs-lookup"><span data-stu-id="fa7eb-122">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="fa7eb-123">Для внутрихолдинговых сценариев вы можете вместо этого настроить политику, которая будет оцениваться по целевой сущности (заемной сущности).</span><span class="sxs-lookup"><span data-stu-id="fa7eb-123">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="fa7eb-124">Чтобы применить политики к целевой сущности, включите функцию "Оценивать политику расходов по сравнению с юридическим лицом-заемщиком" в рабочей области **Управление функциями**.</span><span class="sxs-lookup"><span data-stu-id="fa7eb-124">To run the policies against the destination entity, turn on the "Evaluate Expense policy against borrowing legal entity" feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="fa7eb-125">Когда оценивать политики</span><span class="sxs-lookup"><span data-stu-id="fa7eb-125">When to evaluate policies</span></span>

<span data-ttu-id="fa7eb-126">В параметрах управления расходами имеется вариант выбрать оценку политик управления расходами при сохранении строки или при отправке отчета о расходах.</span><span class="sxs-lookup"><span data-stu-id="fa7eb-126">In expense management parameters, there is an option to either evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="fa7eb-127">Если вы выберете оценку при сохранении строки, это гарантирует, что пользователи получат более раннее представление о том, что им нужно сделать, чтобы сразу заполнить отчет о расходах.</span><span class="sxs-lookup"><span data-stu-id="fa7eb-127">If you choose to evaluate when a line is saved this ensures that users have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="fa7eb-128">В противном случае вы можете отложить оценку политики и сэкономить время, если проверка выполняется в конце, во время отправки в рабочий процесс.</span><span class="sxs-lookup"><span data-stu-id="fa7eb-128">Otherwise, you can delay policy evaluation and save time if you have validation occur at the end, during submission to workflow.</span></span>
