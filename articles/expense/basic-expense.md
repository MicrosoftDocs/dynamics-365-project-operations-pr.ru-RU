---
title: Запись расходов (Lite)
description: Этот тема предоставляет информацию о том, как работать с записью расходов в развертывании Lite.
author: stsporen
manager: AnnBe
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d87094882751f0751a8d9d539fa4cdcfc6b7b0d7
ms.sourcegitcommit: 16c442258ba24c79076cf5877a0f3c1f51a85f61
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2020
ms.locfileid: "4590962"
---
# <a name="expense-entry-lite"></a><span data-ttu-id="fd2c9-103">Запись расходов (Lite)</span><span class="sxs-lookup"><span data-stu-id="fd2c9-103">Expense entry (lite)</span></span>

<span data-ttu-id="fd2c9-104">_**Относится к:** развертывание Lite — от сделки до счетов-проформ_</span><span class="sxs-lookup"><span data-stu-id="fd2c9-104">_**Applies to:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="fd2c9-105">Базовое (или Lite) управление расходами — это возможность фиксировать простые расходы.</span><span class="sxs-lookup"><span data-stu-id="fd2c9-105">Basic, or lite, expense management is the capability to record simple expenses.</span></span> <span data-ttu-id="fd2c9-106">Вы можете записать расходы по проекту, а затем утверждающий проекта проверит и утвердит их.</span><span class="sxs-lookup"><span data-stu-id="fd2c9-106">You can record expenses against a project, and then the project approver will review and approve them.</span></span>

<span data-ttu-id="fd2c9-107">Для получения дополнительной информации о возможностях расходов в Dynamics 365 Project Operations см. [Обзор расходов](expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="fd2c9-107">For more information about expense capabilities in Dynamics 365 Project Operations, see [Expense overview](expense-overview.md).</span></span>

## <a name="capture-a-basic-expense"></a><span data-ttu-id="fd2c9-108">Учет базовых расходов</span><span class="sxs-lookup"><span data-stu-id="fd2c9-108">Capture a basic expense</span></span>

<span data-ttu-id="fd2c9-109">Вы можете зафиксировать свои расходы, чтобы отправить их утверждающему.</span><span class="sxs-lookup"><span data-stu-id="fd2c9-109">You can capture your expenses so that you can submit them to the approver.</span></span>

1. <span data-ttu-id="fd2c9-110">Выберите **Расходы** и выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="fd2c9-110">Go to **Expenses**, and select **New**.</span></span>
2. <span data-ttu-id="fd2c9-111">На странице **Создать расход** введите необходимую информацию о расходах, затем выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="fd2c9-111">On the **New Expense** page, enter the required expense information, and then select **Save**.</span></span>

## <a name="submit-a-basic-expense"></a><span data-ttu-id="fd2c9-112">Отправка базового расхода</span><span class="sxs-lookup"><span data-stu-id="fd2c9-112">Submit a basic expense</span></span>

<span data-ttu-id="fd2c9-113">После того, как вы закончите регистрировать все свои расходы и будете готовы к их утверждению, вы должны их отправить.</span><span class="sxs-lookup"><span data-stu-id="fd2c9-113">After you've finished capturing all your expenses, and you're ready to have them approved, you must submit them.</span></span>

1. <span data-ttu-id="fd2c9-114">Выберите **Расходы** и выберите расход.</span><span class="sxs-lookup"><span data-stu-id="fd2c9-114">Go to **Expenses**, and select an expense.</span></span> <span data-ttu-id="fd2c9-115">Или выберите все расходы, установив флажок в заголовке.</span><span class="sxs-lookup"><span data-stu-id="fd2c9-115">Or, select all the expenses by using the check box on the header.</span></span>
2. <span data-ttu-id="fd2c9-116">Выберите **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="fd2c9-116">Select **Submit**.</span></span> <span data-ttu-id="fd2c9-117">Система обрабатывает выбранные записи, затем создает запросы на утверждение расходов.</span><span class="sxs-lookup"><span data-stu-id="fd2c9-117">The system processes the selected entries and then creates expense approval requests.</span></span>

## <a name="add-an-attachment"></a><span data-ttu-id="fd2c9-118">Добавить вложение</span><span class="sxs-lookup"><span data-stu-id="fd2c9-118">Add an attachment</span></span>

<span data-ttu-id="fd2c9-119">Возможно, вам придется предоставить утверждающему дополнительную документацию о ваших расходах.</span><span class="sxs-lookup"><span data-stu-id="fd2c9-119">You may have to provide the approver with additional documentation about your expense.</span></span> <span data-ttu-id="fd2c9-120">Вы можете прикрепить квитанцию к временной шкале записи расхода.</span><span class="sxs-lookup"><span data-stu-id="fd2c9-120">You can attach a receipt in the timeline of the expense entry.</span></span> <span data-ttu-id="fd2c9-121">Выбрать **Изменить** и в разделе **временная шкала**, а затем выберите значок скрепки, чтобы прикрепить квитанцию.</span><span class="sxs-lookup"><span data-stu-id="fd2c9-121">Select **Edit** and in the **Timeline** section, and then select the paperclip icon to attach your receipt.</span></span>

## <a name="recall-a-basic-expense"></a><span data-ttu-id="fd2c9-122">Отзыв базового расхода</span><span class="sxs-lookup"><span data-stu-id="fd2c9-122">Recall a basic expense</span></span>

<span data-ttu-id="fd2c9-123">Если вы отправили расход по ошибке, вы можете его отозвать.</span><span class="sxs-lookup"><span data-stu-id="fd2c9-123">When you submit an expense by mistake, you can recall it.</span></span> <span data-ttu-id="fd2c9-124">Время, необходимое для отзыва записи о расходах, зависит от стадии ее утверждения.</span><span class="sxs-lookup"><span data-stu-id="fd2c9-124">The time that is required to recall an expense entry depends on its approval stage.</span></span>  <span data-ttu-id="fd2c9-125">Если утверждающий еще не утвердил запись, отзыв может произойти немедленно.</span><span class="sxs-lookup"><span data-stu-id="fd2c9-125">If the approver hasn't yet approved the entry, the recall can occur immediately.</span></span> <span data-ttu-id="fd2c9-126">Однако если запись уже была утверждена, утверждающему предлагается утвердить отзыв и отменить транзакции.</span><span class="sxs-lookup"><span data-stu-id="fd2c9-126">However, if the entry has already been approved, the approver is asked to approve the recall and reverse the transactions.</span></span>

1. <span data-ttu-id="fd2c9-127">Выберите **Расходы**, затем в списке расходов выберите расход, который нужно отозвать.</span><span class="sxs-lookup"><span data-stu-id="fd2c9-127">Go to **Expenses**, and then, in the list of expenses, select the expense to recall.</span></span>
2. <span data-ttu-id="fd2c9-128">Выберите **Отозвать**.</span><span class="sxs-lookup"><span data-stu-id="fd2c9-128">Select **Recall**.</span></span> <span data-ttu-id="fd2c9-129">Если запись о расходе еще не утверждена, система немедленно отзывает ее.</span><span class="sxs-lookup"><span data-stu-id="fd2c9-129">If the expense entry hasn't yet been approved, the system immediately recalls it.</span></span> <span data-ttu-id="fd2c9-130">Если запись о расходе уже была утверждена, создается запрос отзыва, чтобы уведомить утверждающего, что вы хотите отменить расход.</span><span class="sxs-lookup"><span data-stu-id="fd2c9-130">If the expense entry has already been approved, a recall request is created to notify the approver that you want to reverse the expense.</span></span> <span data-ttu-id="fd2c9-131">После этого утверждающий подтвердит, что сторнирование может быть выполнено, и запись будет возвращена.</span><span class="sxs-lookup"><span data-stu-id="fd2c9-131">The approver will then confirm that the reversal can be done, and the entry will be returned.</span></span>

## <a name="delete-a-basic-expense"></a><span data-ttu-id="fd2c9-132">Удаление базового расхода</span><span class="sxs-lookup"><span data-stu-id="fd2c9-132">Delete a basic expense</span></span>

<span data-ttu-id="fd2c9-133">Расходы, которые еще не были отправлены, можно удалить.</span><span class="sxs-lookup"><span data-stu-id="fd2c9-133">Expenses that haven't yet been submitted can be deleted.</span></span> <span data-ttu-id="fd2c9-134">Чтобы удалить уже отправленный расход, вы должны сначала отозвать его.</span><span class="sxs-lookup"><span data-stu-id="fd2c9-134">To delete an expense that has already been submitted, you must first recall it.</span></span>

## <a name="see-also"></a><span data-ttu-id="fd2c9-135">См. также</span><span class="sxs-lookup"><span data-stu-id="fd2c9-135">See also</span></span>

- [<span data-ttu-id="fd2c9-136">Обзор утверждений</span><span class="sxs-lookup"><span data-stu-id="fd2c9-136">Approvals overview</span></span>](../approvals/approvals-overview.md)
