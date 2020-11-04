---
title: Запись расходов (Lite)
description: Этот тема предоставляет информацию о том, как работать с записью расходов в развертывании Lite.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 746d5d9ff56222e7d6b9b6e264db75d5814365c7
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083072"
---
# <a name="expense-entry-lite"></a><span data-ttu-id="7573c-103">Запись расходов (Lite)</span><span class="sxs-lookup"><span data-stu-id="7573c-103">Expense entry (lite)</span></span>

<span data-ttu-id="7573c-104">_**Относится к:** развертывание Lite — от сделки до счетов-проформ_</span><span class="sxs-lookup"><span data-stu-id="7573c-104">_**Applies to:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="7573c-105">Базовое (или Lite) управление расходами — это возможность фиксировать простые расходы.</span><span class="sxs-lookup"><span data-stu-id="7573c-105">Basic, or lite, expense management is the capability to record simple expenses.</span></span> <span data-ttu-id="7573c-106">Вы можете записать расходы по проекту, а затем утверждающий проекта проверит и утвердит их.</span><span class="sxs-lookup"><span data-stu-id="7573c-106">You can record expenses against a project, and then the project approver will review and approve them.</span></span>

<span data-ttu-id="7573c-107">Дополнительные сведения о возможностях расходов в Dynamics 365 Project Operations см. в теме [Обзор расходов](expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7573c-107">For more information about expense capabilities in Dynamics 365 Project Operations, see [Expense overview](expense-overview.md).</span></span>

## <a name="capture-a-basic-expense"></a><span data-ttu-id="7573c-108">Учет базовых расходов</span><span class="sxs-lookup"><span data-stu-id="7573c-108">Capture a basic expense</span></span>

<span data-ttu-id="7573c-109">Вы можете зафиксировать свои расходы, чтобы отправить их утверждающему.</span><span class="sxs-lookup"><span data-stu-id="7573c-109">You can capture your expenses so that you can submit them to the approver.</span></span>

1. <span data-ttu-id="7573c-110">Выберите **Расходы** и выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="7573c-110">Go to **Expenses** , and select **New**.</span></span>
2. <span data-ttu-id="7573c-111">На странице **Создать расход** введите необходимую информацию о расходах, затем выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="7573c-111">On the **New Expense** page, enter the required expense information, and then select **Save**.</span></span>

## <a name="submit-a-basic-expense"></a><span data-ttu-id="7573c-112">Отправка базового расхода</span><span class="sxs-lookup"><span data-stu-id="7573c-112">Submit a basic expense</span></span>

<span data-ttu-id="7573c-113">После того, как вы закончите регистрировать все свои расходы и будете готовы к их утверждению, вы должны их отправить.</span><span class="sxs-lookup"><span data-stu-id="7573c-113">After you've finished capturing all your expenses, and you're ready to have them approved, you must submit them.</span></span>

1. <span data-ttu-id="7573c-114">Выберите **Расходы** и выберите расход.</span><span class="sxs-lookup"><span data-stu-id="7573c-114">Go to **Expenses** , and select an expense.</span></span> <span data-ttu-id="7573c-115">Или выберите все расходы, установив флажок в заголовке.</span><span class="sxs-lookup"><span data-stu-id="7573c-115">Or, select all the expenses by using the check box on the header.</span></span>
2. <span data-ttu-id="7573c-116">Выберите **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="7573c-116">Select **Submit**.</span></span> <span data-ttu-id="7573c-117">Система обрабатывает выбранные записи, затем создает запросы на утверждение расходов.</span><span class="sxs-lookup"><span data-stu-id="7573c-117">The system processes the selected entries and then creates expense approval requests.</span></span>

## <a name="recall-a-basic-expense"></a><span data-ttu-id="7573c-118">Отзыв базового расхода</span><span class="sxs-lookup"><span data-stu-id="7573c-118">Recall a basic expense</span></span>

<span data-ttu-id="7573c-119">Если вы отправили расход по ошибке, вы можете его отозвать.</span><span class="sxs-lookup"><span data-stu-id="7573c-119">When you submit an expense by mistake, you can recall it.</span></span> <span data-ttu-id="7573c-120">Время, необходимое для отзыва записи о расходах, зависит от стадии ее утверждения.</span><span class="sxs-lookup"><span data-stu-id="7573c-120">The time that is required to recall an expense entry depends on its approval stage.</span></span>  <span data-ttu-id="7573c-121">Если утверждающий еще не утвердил запись, отзыв может произойти немедленно.</span><span class="sxs-lookup"><span data-stu-id="7573c-121">If the approver hasn't yet approved the entry, the recall can occur immediately.</span></span> <span data-ttu-id="7573c-122">Однако если запись уже была утверждена, утверждающему предлагается утвердить отзыв и отменить транзакции.</span><span class="sxs-lookup"><span data-stu-id="7573c-122">However, if the entry has already been approved, the approver is asked to approve the recall and reverse the transactions.</span></span>

1. <span data-ttu-id="7573c-123">Выберите **Расходы** , затем в списке расходов выберите расход, который нужно отозвать.</span><span class="sxs-lookup"><span data-stu-id="7573c-123">Go to **Expenses** , and then, in the list of expenses, select the expense to recall.</span></span>
2. <span data-ttu-id="7573c-124">Выберите **Отозвать**.</span><span class="sxs-lookup"><span data-stu-id="7573c-124">Select **Recall**.</span></span> <span data-ttu-id="7573c-125">Если запись о расходе еще не утверждена, система немедленно отзывает ее.</span><span class="sxs-lookup"><span data-stu-id="7573c-125">If the expense entry hasn't yet been approved, the system immediately recalls it.</span></span> <span data-ttu-id="7573c-126">Если запись о расходе уже была утверждена, создается запрос отзыва, чтобы уведомить утверждающего, что вы хотите отменить расход.</span><span class="sxs-lookup"><span data-stu-id="7573c-126">If the expense entry has already been approved, a recall request is created to notify the approver that you want to reverse the expense.</span></span> <span data-ttu-id="7573c-127">После этого утверждающий подтвердит, что сторнирование может быть выполнено, и запись будет возвращена.</span><span class="sxs-lookup"><span data-stu-id="7573c-127">The approver will then confirm that the reversal can be done, and the entry will be returned.</span></span>

## <a name="delete-a-basic-expense"></a><span data-ttu-id="7573c-128">Удаление базового расхода</span><span class="sxs-lookup"><span data-stu-id="7573c-128">Delete a basic expense</span></span>

<span data-ttu-id="7573c-129">Расходы, которые еще не были отправлены, можно удалить.</span><span class="sxs-lookup"><span data-stu-id="7573c-129">Expenses that haven't yet been submitted can be deleted.</span></span> <span data-ttu-id="7573c-130">Чтобы удалить уже отправленный расход, вы должны сначала отозвать его.</span><span class="sxs-lookup"><span data-stu-id="7573c-130">To delete an expense that has already been submitted, you must first recall it.</span></span>

## <a name="see-also"></a><span data-ttu-id="7573c-131">См. также</span><span class="sxs-lookup"><span data-stu-id="7573c-131">See also</span></span>

- [<span data-ttu-id="7573c-132">Обзор утверждений</span><span class="sxs-lookup"><span data-stu-id="7573c-132">Approvals overview</span></span>](../approvals/approvals-overview.md)
