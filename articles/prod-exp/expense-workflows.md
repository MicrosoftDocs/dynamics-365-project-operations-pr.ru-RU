---
title: Настройка рабочих процессов управления расходами
description: Вы можете настроить рабочий процесс для проверки и утверждения командировочных и расходных документов.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8f3235d12499c68a52f9d1c7e118e7bc91dc3a0a
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960533"
---
# <a name="set-up-expense-management-workflows"></a><span data-ttu-id="36c54-103">Настройка рабочих процессов управления расходами</span><span class="sxs-lookup"><span data-stu-id="36c54-103">Set up Expense management workflows</span></span>

<span data-ttu-id="36c54-104">Вы можете настроить рабочий процесс, который будет использоваться для проверки и утверждения командировочных и расходных документов.</span><span class="sxs-lookup"><span data-stu-id="36c54-104">You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="36c54-105">Документы, для которых можно определить рабочие процессы, включают отчеты о расходах, заявки на командировки и запросы денежных авансов.</span><span class="sxs-lookup"><span data-stu-id="36c54-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="36c54-106">Рабочий процесс представляет собой бизнес-процесс.</span><span class="sxs-lookup"><span data-stu-id="36c54-106">A workflow represents a business process.</span></span> <span data-ttu-id="36c54-107">Он определяет, как документ проходит через систему, и указывает, кто должен выполнить задачу или утвердить документ.</span><span class="sxs-lookup"><span data-stu-id="36c54-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="36c54-108">Использование системы рабочих процессов в вашей организации дает несколько преимуществ:</span><span class="sxs-lookup"><span data-stu-id="36c54-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="36c54-109">**Последовательные процессы** — вы можете определить процесс утверждения для определенных документов, таких как заявки на покупку и отчеты о расходах.</span><span class="sxs-lookup"><span data-stu-id="36c54-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="36c54-110">Использование системы рабочих процессов помогает обеспечить последовательную и эффективную обработку и утверждение документов.</span><span class="sxs-lookup"><span data-stu-id="36c54-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="36c54-111">Видимость процесса — вы можете отслеживать статус, историю и показатели производительности конкретного экземпляра рабочего процесса.</span><span class="sxs-lookup"><span data-stu-id="36c54-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="36c54-112">Это поможет вам определить, следует ли вносить изменения в рабочий процесс для повышения эффективности.</span><span class="sxs-lookup"><span data-stu-id="36c54-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="36c54-113">Централизованный список работ — пользователи могут просматривать централизованный список работ для просмотра назначенных им задач рабочего процесса и утверждений.</span><span class="sxs-lookup"><span data-stu-id="36c54-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="36c54-114">**Типы рабочих процессов, которые можно создавать**</span><span class="sxs-lookup"><span data-stu-id="36c54-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="36c54-115">В следующей таблице показаны типы рабочих процессов, которые можно создавать в рабочей области **Расходы**.</span><span class="sxs-lookup"><span data-stu-id="36c54-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>


|              <span data-ttu-id="36c54-116"><strong>Тип</strong></span><span class="sxs-lookup"><span data-stu-id="36c54-116"><strong>Type</strong></span></span>              |                   <span data-ttu-id="36c54-117"><strong>Используйте этот тип для</strong></span><span class="sxs-lookup"><span data-stu-id="36c54-117"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <span data-ttu-id="36c54-118"><strong>Авансовый отчет</strong></span><span class="sxs-lookup"><span data-stu-id="36c54-118"><strong>Expense report</strong></span></span>         |            <span data-ttu-id="36c54-119">Создание рабочих процессов утверждения для отчетов о расходах.</span><span class="sxs-lookup"><span data-stu-id="36c54-119">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="36c54-120"><strong>Автоматическая разноска отчетов о расходах</strong></span><span class="sxs-lookup"><span data-stu-id="36c54-120"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="36c54-121">Создание рабочих процессов автоматической разноски для отчетов о расходах.</span><span class="sxs-lookup"><span data-stu-id="36c54-121">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="36c54-122"><strong>Элемент строки расходов</strong></span><span class="sxs-lookup"><span data-stu-id="36c54-122"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="36c54-123">Создание рабочих процессов утверждения для элементов строки в отчетах о расходах.</span><span class="sxs-lookup"><span data-stu-id="36c54-123">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="36c54-124"><strong>Автоматическая разноска элементов строки расходов</strong></span><span class="sxs-lookup"><span data-stu-id="36c54-124"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="36c54-125">Создание рабочих процессов автоматической разноски для элементов строки в отчетах о расходах.</span><span class="sxs-lookup"><span data-stu-id="36c54-125">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="36c54-126"><strong>Заявка на командировку</strong></span><span class="sxs-lookup"><span data-stu-id="36c54-126"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="36c54-127">Создание рабочих процессов утверждения для заявок на командировку.</span><span class="sxs-lookup"><span data-stu-id="36c54-127">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="36c54-128"><strong>Запрос денежного аванса</strong></span><span class="sxs-lookup"><span data-stu-id="36c54-128"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="36c54-129">Создание рабочих процессов утверждения для запросов на получение аванса.</span><span class="sxs-lookup"><span data-stu-id="36c54-129">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="36c54-130"><strong>Возврат НДС</strong></span><span class="sxs-lookup"><span data-stu-id="36c54-130"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="36c54-131">Создание рабочих процессов утверждения для возмещения налога на добавленную стоимость (НДС).</span><span class="sxs-lookup"><span data-stu-id="36c54-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |

