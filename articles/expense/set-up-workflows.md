---
title: Настройка рабочих процессов для управления расходами
description: Вы можете настроить рабочий процесс, который будет использоваться для проверки и утверждения командировочных и расходных документов.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: af6463b07e282ae1ff6aa7dc1a540ff7c8cc318a
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127714"
---
# <a name="set-up-workflows-for-expense-management"></a><span data-ttu-id="f7bc8-103">Настройка рабочих процессов для управления расходами</span><span class="sxs-lookup"><span data-stu-id="f7bc8-103">Set up workflows for Expense management</span></span>

<span data-ttu-id="f7bc8-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="f7bc8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f7bc8-105">Вы можете настроить рабочий процесс для проверки и утверждения командировочных и расходных документов.</span><span class="sxs-lookup"><span data-stu-id="f7bc8-105">You can set up a workflow process to review and approve travel and expense documents.</span></span> <span data-ttu-id="f7bc8-106">Вы можете определить рабочие процессы для отчетов о расходах, запросов командировочных и запросов денежных авансов.</span><span class="sxs-lookup"><span data-stu-id="f7bc8-106">You can define workflows for expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="f7bc8-107">Рабочий процесс представляет собой бизнес-процесс и определяет, как документ проходит через систему.</span><span class="sxs-lookup"><span data-stu-id="f7bc8-107">A workflow represents a business process and defines how a document flows through the system.</span></span> <span data-ttu-id="f7bc8-108">Рабочий процесс также указывает, кто должен выполнить задачу или утвердить документ.</span><span class="sxs-lookup"><span data-stu-id="f7bc8-108">The workflow also indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="f7bc8-109">Использование системы рабочих процессов в вашей организации дает несколько преимуществ:</span><span class="sxs-lookup"><span data-stu-id="f7bc8-109">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="f7bc8-110">**Последовательные процессы**: вы можете определить процесс утверждения для определенных документов, таких как заявки на покупку и отчеты о расходах.</span><span class="sxs-lookup"><span data-stu-id="f7bc8-110">**Consistent processes**: You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="f7bc8-111">Использование системы рабочих процессов помогает обеспечить последовательную и эффективную обработку и утверждение документов.</span><span class="sxs-lookup"><span data-stu-id="f7bc8-111">Using the workflow system helps ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="f7bc8-112">**Видимость процесса**: вы можете отслеживать статус, историю и показатели производительности конкретного экземпляра рабочего процесса.</span><span class="sxs-lookup"><span data-stu-id="f7bc8-112">**Process visibility**: You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="f7bc8-113">Это поможет вам определить, следует ли вносить изменения в рабочий процесс для повышения эффективности.</span><span class="sxs-lookup"><span data-stu-id="f7bc8-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="f7bc8-114">**Централизованный список работ**: пользователи могут просматривать централизованный список работ для просмотра назначенных им задач рабочего процесса и утверждений.</span><span class="sxs-lookup"><span data-stu-id="f7bc8-114">**Centralized work list**: Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

## <a name="workflow-types"></a><span data-ttu-id="f7bc8-115">Типы рабочих процессов</span><span class="sxs-lookup"><span data-stu-id="f7bc8-115">Workflow types</span></span>

<span data-ttu-id="f7bc8-116">В следующей таблице показаны типы рабочих процессов, которые можно создавать в рабочей области **Управление расходами**.</span><span class="sxs-lookup"><span data-stu-id="f7bc8-116">The following table lists the types of workflows that you can create in **Expense Management**.</span></span>


|              <span data-ttu-id="f7bc8-117"><strong>Тип</strong></span><span class="sxs-lookup"><span data-stu-id="f7bc8-117"><strong>Type</strong></span></span>              |                   <span data-ttu-id="f7bc8-118"><strong>Используйте этот тип для</strong></span><span class="sxs-lookup"><span data-stu-id="f7bc8-118"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <span data-ttu-id="f7bc8-119"><strong>Автоматическое утверждение отчетов о расходах</strong></span><span class="sxs-lookup"><span data-stu-id="f7bc8-119"><strong>Expense report auto approval</strong></span></span> |            <span data-ttu-id="f7bc8-120">Создание рабочих процессов утверждения для отчетов о расходах.</span><span class="sxs-lookup"><span data-stu-id="f7bc8-120">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="f7bc8-121"><strong>Автоматическая разноска отчетов о расходах</strong></span><span class="sxs-lookup"><span data-stu-id="f7bc8-121"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="f7bc8-122">Создание рабочих процессов автоматической разноски для отчетов о расходах.</span><span class="sxs-lookup"><span data-stu-id="f7bc8-122">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="f7bc8-123"><strong>Элемент строки расходов</strong></span><span class="sxs-lookup"><span data-stu-id="f7bc8-123"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="f7bc8-124">Создание рабочих процессов утверждения для элементов строки в отчетах о расходах.</span><span class="sxs-lookup"><span data-stu-id="f7bc8-124">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="f7bc8-125"><strong>Автоматическая разноска элементов строки расходов</strong></span><span class="sxs-lookup"><span data-stu-id="f7bc8-125"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="f7bc8-126">Создание рабочих процессов автоматической разноски для элементов строки в отчетах о расходах.</span><span class="sxs-lookup"><span data-stu-id="f7bc8-126">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="f7bc8-127"><strong>Заявка на командировку</strong></span><span class="sxs-lookup"><span data-stu-id="f7bc8-127"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="f7bc8-128">Создание рабочих процессов утверждения для заявок на командировку.</span><span class="sxs-lookup"><span data-stu-id="f7bc8-128">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="f7bc8-129"><strong>Запрос денежного аванса</strong></span><span class="sxs-lookup"><span data-stu-id="f7bc8-129"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="f7bc8-130">Создание рабочих процессов утверждения для запросов на получение аванса.</span><span class="sxs-lookup"><span data-stu-id="f7bc8-130">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="f7bc8-131"><strong>Возврат НДС</strong></span><span class="sxs-lookup"><span data-stu-id="f7bc8-131"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="f7bc8-132">Создание рабочих процессов утверждения для возмещения налога на добавленную стоимость (НДС).</span><span class="sxs-lookup"><span data-stu-id="f7bc8-132">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |
