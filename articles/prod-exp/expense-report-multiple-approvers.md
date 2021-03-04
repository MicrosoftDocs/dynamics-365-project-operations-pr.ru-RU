---
title: Несколько утверждающих для отчета о расходах
description: Эта тема предоставляет информацию об отчетах о расходах, которые требуют утверждения несколькими людьми.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b6d07f00fd6c1ba2d860787665d95f95f7b1a89
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960623"
---
# <a name="multiple-approvers-on-an-expense-report"></a><span data-ttu-id="4b2a9-103">Несколько утверждающих для отчета о расходах</span><span class="sxs-lookup"><span data-stu-id="4b2a9-103">Multiple approvers on an expense report</span></span>

<span data-ttu-id="4b2a9-104">В зависимости от политик утверждения расходов в вашей организации может потребоваться, чтобы несколько человек утверждали отчет о расходах, отправленный сотрудником.</span><span class="sxs-lookup"><span data-stu-id="4b2a9-104">Depending on your organization's expense approval policies, more than one person might have to approve an expense report that is submitted by an employee.</span></span> <span data-ttu-id="4b2a9-105">Когда вы настраиваете рабочий процесс для утверждения отчета о расходах, вы можете добавить элементы рабочего процесса, которые включают задачи или шаги для одного или нескольких утверждающих отчетов о расходах.</span><span class="sxs-lookup"><span data-stu-id="4b2a9-105">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="4b2a9-106">Например, вы можете потребовать, чтобы все отчеты о расходах утверждались сначала руководителем сотрудника, который представил отчет, и затем координатором по расчетам с поставщиками.</span><span class="sxs-lookup"><span data-stu-id="4b2a9-106">For example, you might require that all expense reports be approved first by the manager of the employee who submitted the report and then by the Accounts payable coordinator.</span></span>

<span data-ttu-id="4b2a9-107">Если вы решите потребовать нескольких утверждающих отчетов о расходах, вы можете добавить элементы рабочего процесса любым из следующих способов:</span><span class="sxs-lookup"><span data-stu-id="4b2a9-107">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="4b2a9-108">Добавьте один элемент утверждения с одним шагом.</span><span class="sxs-lookup"><span data-stu-id="4b2a9-108">Add one approval element that has one step.</span></span> <span data-ttu-id="4b2a9-109">Например, для этого шага может потребоваться, чтобы отчет о расходах был назначен группе пользователей и чтобы он был утвержден 50 процентами членов группы пользователей.</span><span class="sxs-lookup"><span data-stu-id="4b2a9-109">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="4b2a9-110">Добавьте один элемент утверждения с несколькими шагами.</span><span class="sxs-lookup"><span data-stu-id="4b2a9-110">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="4b2a9-111">Например, элемент утверждения может включать следующие шаги:</span><span class="sxs-lookup"><span data-stu-id="4b2a9-111">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="4b2a9-112">Руководитель сотрудника, представившего отчет о расходах, утверждает его.</span><span class="sxs-lookup"><span data-stu-id="4b2a9-112">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="4b2a9-113">Клерк по расчетам с поставщиками проверяет чеки и статьи отчета о расходах.</span><span class="sxs-lookup"><span data-stu-id="4b2a9-113">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="4b2a9-114">Отчет о расходах утверждается владельцем бюджета.</span><span class="sxs-lookup"><span data-stu-id="4b2a9-114">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="4b2a9-115">Добавьте несколько элементов утверждения, каждый из которых имеет один шаг.</span><span class="sxs-lookup"><span data-stu-id="4b2a9-115">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="4b2a9-116">Например, вы можете добавить отдельный элемент утверждения для каждого из следующих шагов:</span><span class="sxs-lookup"><span data-stu-id="4b2a9-116">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="4b2a9-117">Отчет о расходах утверждается руководителем сотрудника.</span><span class="sxs-lookup"><span data-stu-id="4b2a9-117">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="4b2a9-118">Отчет о расходах утверждается владельцем бюджета.</span><span class="sxs-lookup"><span data-stu-id="4b2a9-118">The budget owner approves the expense report.</span></span>
