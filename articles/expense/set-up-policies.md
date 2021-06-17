---
title: Определение политик расходов
description: Вы можете определить политики расходов, которым ваши сотрудники должны следовать при вводе и отправке отчетов о расходах и заявок на командировки.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fa108db9aa0d2a22c35d2d046917ddae1f3842c1
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001892"
---
# <a name="define-expense-policies"></a><span data-ttu-id="4821e-103">Определение политик расходов</span><span class="sxs-lookup"><span data-stu-id="4821e-103">Define expense policies</span></span>

<span data-ttu-id="4821e-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="4821e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4821e-105">Вы можете определить политики, которым ваши сотрудники должны следовать при вводе и отправке отчетов о расходах и заявок на командировки.</span><span class="sxs-lookup"><span data-stu-id="4821e-105">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="4821e-106">Внедрение политик расходов может помочь вам эффективно управлять расходами.</span><span class="sxs-lookup"><span data-stu-id="4821e-106">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="4821e-107">Например, вы можете установить политику расходов на гостиницу в Нью-Йорке, которая гласит, что суточные расходы не могут превышать 250 долларов США.</span><span class="sxs-lookup"><span data-stu-id="4821e-107">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="4821e-108">Если работник отправляет отчет о расходах или заявку на командировку, где стоимость номера превышает эту сумму, система уведомит</span><span class="sxs-lookup"><span data-stu-id="4821e-108">If a worker submits an expense report or travel requisition where the room rate exceeds this amount, the system will notify the</span></span>         
<span data-ttu-id="4821e-109">сотрудника, что сумма политики для расходов была превышена.</span><span class="sxs-lookup"><span data-stu-id="4821e-109">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="4821e-110">Вы можете настроить сообщение, которое работник будет получать, когда вы</span><span class="sxs-lookup"><span data-stu-id="4821e-110">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="4821e-111">определили политику.</span><span class="sxs-lookup"><span data-stu-id="4821e-111">define the policy.</span></span>      
        
<span data-ttu-id="4821e-112">Можно определить три типа политик:</span><span class="sxs-lookup"><span data-stu-id="4821e-112">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="4821e-113">**Предупреждение**: позволяет работнику подавать отчет о расходах или заявку на командировку, но расходы будут отмечены для всех утверждающих и</span><span class="sxs-lookup"><span data-stu-id="4821e-113">**Warning**: Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>         
  <span data-ttu-id="4821e-114">для последующего отчета.</span><span class="sxs-lookup"><span data-stu-id="4821e-114">for later reporting.</span></span>        

- <span data-ttu-id="4821e-115">**Ошибка**: требует, чтобы работник пересмотрел расходы в соответствии с политикой перед отправкой отчета о расходах или заявки на командировку.</span><span class="sxs-lookup"><span data-stu-id="4821e-115">**Error**: Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>        
 
 - <span data-ttu-id="4821e-116">**Обоснование**: требует от работника или менеджера ввести обоснование превышения суммы по политике перед подачей отчета о расходах или заявки на командировку.</span><span class="sxs-lookup"><span data-stu-id="4821e-116">**Justification**: Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="4821e-117">Советы по политикам</span><span class="sxs-lookup"><span data-stu-id="4821e-117">Policy tips</span></span>
<span data-ttu-id="4821e-118">Вот несколько советов, которые могут помочь вам при создании новых политик для управления расходами:</span><span class="sxs-lookup"><span data-stu-id="4821e-118">Here are a few suggestions that can assist you when creating new policies for expense management:</span></span> 

- <span data-ttu-id="4821e-119">Политики действуют по датам, что означает, что политика не вступит в силу, если она создана с датой, более поздней, чем дата, когда произошли расходы.</span><span class="sxs-lookup"><span data-stu-id="4821e-119">Policies are date effective which means a policy won't take effect if it's created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="4821e-120">Например, вы сегодня создаете новую политику, чтобы обеспечить максимальные расходы на питание в размере 50 долларов США.</span><span class="sxs-lookup"><span data-stu-id="4821e-120">For example, you create a new policy today to enforce a maximum meal expense of $50.</span></span> <span data-ttu-id="4821e-121">Любые существующие расходы, введенные на вчерашний день, не будут проверяться на соответствие этой политике.</span><span class="sxs-lookup"><span data-stu-id="4821e-121">Any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
- <span data-ttu-id="4821e-122">При создании политики для категории расходов, которая может быть детализирована, рассмотрите возможность добавления условия для типа строки расходов.</span><span class="sxs-lookup"><span data-stu-id="4821e-122">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="4821e-123">Некоторые политики, например требование получения квитанции, могут не иметь смысла для детализированных строк.</span><span class="sxs-lookup"><span data-stu-id="4821e-123">Some policies, such as requiring a receipt, may not make sense for itemized lines.</span></span> <span data-ttu-id="4821e-124">В этом случае политика применяется только к строке заголовка или строке без детализации.</span><span class="sxs-lookup"><span data-stu-id="4821e-124">In this situation, the policy only is applied to the header line or a non-itemized line.</span></span> 
- <span data-ttu-id="4821e-125">По умолчанию политики управления расходами сравниваются с исходной сущностью.</span><span class="sxs-lookup"><span data-stu-id="4821e-125">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="4821e-126">Для внутрихолдинговых сценариев вы можете вместо этого настроить политику, которая будет оцениваться по целевой сущности (заемной сущности).</span><span class="sxs-lookup"><span data-stu-id="4821e-126">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="4821e-127">Чтобы применить политики к целевой сущности, включите функцию **Оценивать политику расходов по сравнению с юридическим лицом-заемщиком** в рабочей области **Управление функциями**.</span><span class="sxs-lookup"><span data-stu-id="4821e-127">To run the policies against the destination entity, turn on the **Evaluate Expense policy against borrowing legal entity** feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="4821e-128">Когда оценивать политики</span><span class="sxs-lookup"><span data-stu-id="4821e-128">When to evaluate policies</span></span>

<span data-ttu-id="4821e-129">В параметрах управления расходами вы можете выбрать оценку политик управления расходами при сохранении строки или при отправке отчета о расходах.</span><span class="sxs-lookup"><span data-stu-id="4821e-129">In expense management parameters, you can select to evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="4821e-130">Если вы выберете оценку при сохранении строки, пользователи получат более раннее представление о том, что им нужно сделать, чтобы сразу заполнить отчет о расходах.</span><span class="sxs-lookup"><span data-stu-id="4821e-130">If you choose to evaluate when a line is saved, users will have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="4821e-131">В противном случае вы можете отложить оценку политики и сэкономить время, выполнив проверку в конце, во время отправки в рабочий процесс.</span><span class="sxs-lookup"><span data-stu-id="4821e-131">Otherwise, you can delay policy evaluation and save time by validating at the end, during the submission to workflow.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]