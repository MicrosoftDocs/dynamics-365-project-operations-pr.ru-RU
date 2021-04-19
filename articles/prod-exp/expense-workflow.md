---
title: Рабочий процесс управления расходами
description: В этой теме объясняется, как можно использовать систему рабочих процессов в Microsoft Dynamics 365 Finance, чтобы настроить процесс проверки отчетов о расходах в управлении расходами.
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
ms.openlocfilehash: fde336f53d72e9ddf38c5123d9e774a4c3a22a28
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271684"
---
# <a name="expense-management-workflow"></a><span data-ttu-id="7bb91-103">Рабочий процесс управления расходами</span><span class="sxs-lookup"><span data-stu-id="7bb91-103">Expense management workflow</span></span>

<span data-ttu-id="7bb91-104">Вы можете использовать систему рабочих процессов, чтобы настроить процесс проверки отчетов о расходах в управлении расходами.</span><span class="sxs-lookup"><span data-stu-id="7bb91-104">You can use the workflow system to set up a review process for expense reports in Expense management.</span></span> <span data-ttu-id="7bb91-105">Вы можете настроить рабочий процесс, который использует следующие критерии для определения того, кто утверждает отчеты о расходах:</span><span class="sxs-lookup"><span data-stu-id="7bb91-105">You can set up a workflow that uses the following criteria to determine who approves expense reports:</span></span>

- <span data-ttu-id="7bb91-106">Иерархия отчетности сотрудников и предопределенные лимиты утверждения</span><span class="sxs-lookup"><span data-stu-id="7bb91-106">The employee reporting hierarchy and predefined approval limits</span></span>
- <span data-ttu-id="7bb91-107">Многоуровневое утверждение, поддерживающее промежуточных утверждающих и окончательного утверждающего</span><span class="sxs-lookup"><span data-stu-id="7bb91-107">Multi-level approval that supports interim approvers and a final approver</span></span>
- <span data-ttu-id="7bb91-108">Финансовые измерения и ответственность за проект</span><span class="sxs-lookup"><span data-stu-id="7bb91-108">Financial dimensions and project responsibility</span></span>
- <span data-ttu-id="7bb91-109">Присвоение определенным пользователям или группам пользователей</span><span class="sxs-lookup"><span data-stu-id="7bb91-109">Assignment to specific users or user groups</span></span>

<span data-ttu-id="7bb91-110">Утверждения рабочего процесса могут быть созданы для отчетов о расходах, заявок на командировки, денежных авансов и возмещения налога на добавленную стоимость (НДС).</span><span class="sxs-lookup"><span data-stu-id="7bb91-110">Workflow approvals can be created for expense reports, travel requisitions, cash advances, and value-added tax (VAT) recovery.</span></span>

<span data-ttu-id="7bb91-111">**Пример**</span><span class="sxs-lookup"><span data-stu-id="7bb91-111">**Example**</span></span>

<span data-ttu-id="7bb91-112">Следующий процесс является примером рабочего процесса управления расходами для отчета о расходах.</span><span class="sxs-lookup"><span data-stu-id="7bb91-112">The following process is an example of the expense management workflow for an expense report.</span></span>

1. <span data-ttu-id="7bb91-113">Сотрудник создает и сохраняет отчет о расходах.</span><span class="sxs-lookup"><span data-stu-id="7bb91-113">An employee creates and saves an expense report.</span></span>
2. <span data-ttu-id="7bb91-114">Сотрудник отправляет отчет о расходах на утверждение.</span><span class="sxs-lookup"><span data-stu-id="7bb91-114">The employee submits the expense report for approval.</span></span> <span data-ttu-id="7bb91-115">Утверждающий определяется на основе правил, определенных при настройке рабочего процесса.</span><span class="sxs-lookup"><span data-stu-id="7bb91-115">The approver is identified based on the rules that were defined when the workflow was set up.</span></span>
3. <span data-ttu-id="7bb91-116">Утверждающий получает уведомление о том, что отчет о расходах готов к утверждению.</span><span class="sxs-lookup"><span data-stu-id="7bb91-116">The approver receives a notification that an expense report is ready for approval.</span></span> <span data-ttu-id="7bb91-117">Утверждающий проверяет отчет о расходах и проверяет выполнение следующих условий:</span><span class="sxs-lookup"><span data-stu-id="7bb91-117">The approver reviews the expense report and verifies that the following conditions are met:</span></span>

    - <span data-ttu-id="7bb91-118">Расходы не нарушают никакие политики расходов.</span><span class="sxs-lookup"><span data-stu-id="7bb91-118">The expenses don't violate any expense policies.</span></span> <span data-ttu-id="7bb91-119">Если расход нарушает политику, утверждающий проверяет, что отчет о расходах включает действительное бизнес-обоснование.</span><span class="sxs-lookup"><span data-stu-id="7bb91-119">If an expense violates a policy, the approver verifies that the expense report includes a valid business justification.</span></span>
    - <span data-ttu-id="7bb91-120">Электронные квитанции прилагаются к отчету о расходах.</span><span class="sxs-lookup"><span data-stu-id="7bb91-120">Electronic receipts are attached to the expense report.</span></span>

4. <span data-ttu-id="7bb91-121">Утверждающий утверждает отчет о расходах.</span><span class="sxs-lookup"><span data-stu-id="7bb91-121">The approver approves the expense report.</span></span>
5. <span data-ttu-id="7bb91-122">Отчет о расходах назначается координатору расчетов с поставщиками для проводки.</span><span class="sxs-lookup"><span data-stu-id="7bb91-122">The expense report is assigned to the Accounts payable coordinator for posting.</span></span>
6. <span data-ttu-id="7bb91-123">В зависимости от того, настроена ли автоматическая разноска, выполняется один из следующих шагов:</span><span class="sxs-lookup"><span data-stu-id="7bb91-123">One of the following steps occurs, depending on whether automatic posting is configured:</span></span>

    - <span data-ttu-id="7bb91-124">Если настроена автоматическая проводка, отчет о расходах обрабатывается для оплаты, и статус отчета о расходах обновляется.</span><span class="sxs-lookup"><span data-stu-id="7bb91-124">If automatic posting is configured, the expense report is processed for payment, and the status of the expense report is updated.</span></span>
    - <span data-ttu-id="7bb91-125">Если автоматическая разноска не настроена, координатор по расчетам с поставщиками проверяет, были ли отправлены все исходные квитанции и совпадают ли квитанции с расходами в отчете о расходах.</span><span class="sxs-lookup"><span data-stu-id="7bb91-125">If automatic posting isn't configured, the Accounts payable coordinator verifies that all original receipts have been submitted, and that the receipts are aligned with the expenses on the expense report.</span></span> <span data-ttu-id="7bb91-126">Все налоговые коды, введенные в отчет о расходах, также должны быть проверены как правильные.</span><span class="sxs-lookup"><span data-stu-id="7bb91-126">All tax codes that are entered on the expense report must also be verified as correct.</span></span>

<span data-ttu-id="7bb91-127">После проверки этих требований разносится отчет о расходах.</span><span class="sxs-lookup"><span data-stu-id="7bb91-127">After these requirements are verified, the expense report is posted.</span></span>

<span data-ttu-id="7bb91-128">После разноски отчета о расходах платеж разрешается для отчета о расходах, и сотруднику возмещаются расходы.</span><span class="sxs-lookup"><span data-stu-id="7bb91-128">After the expense report is posted, payment is authorized for the expense report, and the employee is reimbursed.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]