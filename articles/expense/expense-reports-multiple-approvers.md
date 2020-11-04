---
title: Отчеты о расходах и несколько утверждающих
description: Эта тема предоставляет информацию об отчетах о расходах, которые требуют утверждения несколькими людьми.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 548673541cee5ce598721f94415c0444995c8325
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083191"
---
# <a name="expense-reports-and-multiple-approvers"></a><span data-ttu-id="0de31-103">Отчеты о расходах и несколько утверждающих</span><span class="sxs-lookup"><span data-stu-id="0de31-103">Expense reports and multiple approvers</span></span>

<span data-ttu-id="0de31-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="0de31-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0de31-105">В зависимости от политик утверждения расходов в вашей организации может потребоваться утвердить представленный отчет о расходах более чем одному человеку.</span><span class="sxs-lookup"><span data-stu-id="0de31-105">Depending on your organization's expense approval policies, more than one person might have to approve a submitted expense report.</span></span> <span data-ttu-id="0de31-106">Когда вы настраиваете рабочий процесс для утверждения отчета о расходах, вы можете добавить элементы рабочего процесса, которые включают задачи или шаги для одного или нескольких утверждающих отчетов о расходах.</span><span class="sxs-lookup"><span data-stu-id="0de31-106">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="0de31-107">Например, вы можете потребовать, чтобы все отчеты о расходах утверждались двумя отдельными людьми: руководителем сотрудника, который представил отчет, и координатором по расчетам с поставщиками.</span><span class="sxs-lookup"><span data-stu-id="0de31-107">For example, you might require that all expense reports be approved by two separate people, the manager of the employee who submitted the report and the Accounts payable coordinator.</span></span>

<span data-ttu-id="0de31-108">Если вы решите потребовать нескольких утверждающих отчетов о расходах, вы можете добавить элементы рабочего процесса любым из следующих способов:</span><span class="sxs-lookup"><span data-stu-id="0de31-108">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="0de31-109">Добавьте один элемент утверждения с одним шагом.</span><span class="sxs-lookup"><span data-stu-id="0de31-109">Add one approval element that has one step.</span></span> <span data-ttu-id="0de31-110">Например, для этого шага может потребоваться, чтобы отчет о расходах был назначен группе пользователей и чтобы он был утвержден 50 процентами членов группы пользователей.</span><span class="sxs-lookup"><span data-stu-id="0de31-110">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="0de31-111">Добавьте один элемент утверждения с несколькими шагами.</span><span class="sxs-lookup"><span data-stu-id="0de31-111">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="0de31-112">Например, элемент утверждения может включать следующие шаги:</span><span class="sxs-lookup"><span data-stu-id="0de31-112">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="0de31-113">Руководитель сотрудника, представившего отчет о расходах, утверждает его.</span><span class="sxs-lookup"><span data-stu-id="0de31-113">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="0de31-114">Клерк по расчетам с поставщиками проверяет чеки и статьи отчета о расходах.</span><span class="sxs-lookup"><span data-stu-id="0de31-114">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="0de31-115">Отчет о расходах утверждается владельцем бюджета.</span><span class="sxs-lookup"><span data-stu-id="0de31-115">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="0de31-116">Добавьте несколько элементов утверждения, каждый из которых имеет один шаг.</span><span class="sxs-lookup"><span data-stu-id="0de31-116">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="0de31-117">Например, вы можете добавить отдельный элемент утверждения для каждого из следующих шагов:</span><span class="sxs-lookup"><span data-stu-id="0de31-117">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="0de31-118">Отчет о расходах утверждается руководителем сотрудника.</span><span class="sxs-lookup"><span data-stu-id="0de31-118">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="0de31-119">Отчет о расходах утверждается владельцем бюджета.</span><span class="sxs-lookup"><span data-stu-id="0de31-119">The budget owner approves the expense report.</span></span>
