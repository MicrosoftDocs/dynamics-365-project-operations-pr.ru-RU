---
title: Заявки на командировку
description: В этом разделе представлена информация о заявках на командировку.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 0261405abb9305d7f6abcde9cb90d9b184868580
ms.sourcegitcommit: a0f80d024a5d3112a39781815bd31d0c05ddaf6f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/30/2020
ms.locfileid: "3906304"
---
# <a name="travel-requisitions"></a><span data-ttu-id="b0b17-103">Заявки на командировку</span><span class="sxs-lookup"><span data-stu-id="b0b17-103">Travel requisitions</span></span>

<span data-ttu-id="b0b17-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/без запасов_</span><span class="sxs-lookup"><span data-stu-id="b0b17-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="b0b17-105">В заявке на командировку перечислены расходы, которые будут понесены с целью поездки.</span><span class="sxs-lookup"><span data-stu-id="b0b17-105">A travel requisition lists the expenses that will be incurred for the purpose of travel.</span></span> <span data-ttu-id="b0b17-106">Заявка на командировку отправляется на рассмотрение и может использоваться для утверждения расходов.</span><span class="sxs-lookup"><span data-stu-id="b0b17-106">A travel requisition is submitted for review and can be used to authorize expenses.</span></span>

<span data-ttu-id="b0b17-107">Вам может потребоваться подать заявку на командировку до того, как вы понесете какие-либо расходы, которые несет организация.</span><span class="sxs-lookup"><span data-stu-id="b0b17-107">You may be required to submit a travel requisition before you incur any expense that is charged to the organization.</span></span> <span data-ttu-id="b0b17-108">Это требование применяется независимо от того, списываете ли вы расходы с корпоративной кредитной карты, тратите ли вы наличные, полученные в качестве аванса наличными, или расходуете личные средства, которые будут возмещены организацией.</span><span class="sxs-lookup"><span data-stu-id="b0b17-108">This requirement applies, regardless of whether you charge expenses to a corporate credit card, spend cash that you received from a cash advance, or incur out-of-pocket expenses that will be reimbursed by the organization.</span></span>

<span data-ttu-id="b0b17-109">Заявки на командировки и политики могут использоваться для управления расходами организации.</span><span class="sxs-lookup"><span data-stu-id="b0b17-109">Travel requisitions and policies can be used to help manage organization expenditures.</span></span> <span data-ttu-id="b0b17-110">Например, если ваша организация работает над проектом с фиксированной ценой, для которого требуются командировки, командировочные расходы участников рабочей группы проекта должны укладываться в бюджет проекта.</span><span class="sxs-lookup"><span data-stu-id="b0b17-110">For example, if your organization is working on a fixed-price project that requires travel, the travel expenses of the project's team members must fit within the project budget.</span></span> <span data-ttu-id="b0b17-111">Требуя утверждения командировочных расходов до их затрат, организация может помочь убедиться, что проект остается в рамках бюджета.</span><span class="sxs-lookup"><span data-stu-id="b0b17-111">By requiring that travel expenses be approved before they are incurred, the organization can help make sure that the project remains within budget.</span></span>

## <a name="configuration"></a><span data-ttu-id="b0b17-112">Настройка</span><span class="sxs-lookup"><span data-stu-id="b0b17-112">Configuration</span></span> 

<span data-ttu-id="b0b17-113">Заявки на командировку можно настроить как "обязательные", включив параметр "Предварительная авторизация командировки обязательна" в параметрах управления расходами.</span><span class="sxs-lookup"><span data-stu-id="b0b17-113">Travel Requisitions can be configured as "mandatory" by enabling the "Pre-authorization of travel is mandatory" parameter in Expense Management Parameters.</span></span> 

## <a name="create-and-submit-a-travel-requisition"></a><span data-ttu-id="b0b17-114">Создание и отправка заявки на командировку</span><span class="sxs-lookup"><span data-stu-id="b0b17-114">Create and submit a travel requisition</span></span>

1. <span data-ttu-id="b0b17-115">Перейдите в раздел **Мои расходы: заявка на командировку** и выберите **Создать заявку на командировку**.</span><span class="sxs-lookup"><span data-stu-id="b0b17-115">Go to **My expenses: Travel Requisition**, and select **New travel Requisition**.</span></span>
2. <span data-ttu-id="b0b17-116">Введите цель и место назначения для заявки.</span><span class="sxs-lookup"><span data-stu-id="b0b17-116">Enter a purpose and destination for the requisition.</span></span>
3. <span data-ttu-id="b0b17-117">В поле **Описание командировки** введите любую дополнительную информацию.</span><span class="sxs-lookup"><span data-stu-id="b0b17-117">In the  **Travel description** field, enter any additional information.</span></span> 
4. <span data-ttu-id="b0b17-118">Для каждого из ожидаемых расходов, таких как билеты на самолет, питание или аренда автомобиля, создайте статью расходов.</span><span class="sxs-lookup"><span data-stu-id="b0b17-118">For each of the expected expenses, such as Flight, meals, or car rental, create an expense line item.</span></span> <span data-ttu-id="b0b17-119">Включите предполагаемую дату, предполагаемую сумму и валюту для каждого расхода.</span><span class="sxs-lookup"><span data-stu-id="b0b17-119">Include the estimated date, estimated amount, and the currency for each expense.</span></span> 
5. <span data-ttu-id="b0b17-120">Когда вы закончите добавлять ожидаемые расходы, выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="b0b17-120">When you have finished adding the expected expenses, select **Save**.</span></span>
6. <span data-ttu-id="b0b17-121">Когда вы будете готовы отправить заявку на командировку, выберите **Рабочий процесс** > **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="b0b17-121">When you are ready to submit the travel requisition, select **Workflow** > **Submit**.</span></span>

<span data-ttu-id="b0b17-122">Вы можете просмотреть утвержденные заявки на командировку в разделе **Мои расходы: заявка на командировку**.</span><span class="sxs-lookup"><span data-stu-id="b0b17-122">You can view your approved travel requisitions under **My Expenses: Travel Requisition**.</span></span> 

## <a name="view-available-travel-requisitions"></a><span data-ttu-id="b0b17-123">Просмотр доступных заявок на командировку</span><span class="sxs-lookup"><span data-stu-id="b0b17-123">View available travel requisitions</span></span>

<span data-ttu-id="b0b17-124">Вы можете просмотреть все свои заявки на командировку в разделе **Мои расходы: заявки на командировку**.</span><span class="sxs-lookup"><span data-stu-id="b0b17-124">You can view all of your travel requisitions under **My Expenses: Travel Requisitions**.</span></span>

## <a name="approve-travel-requisitions"></a><span data-ttu-id="b0b17-125">Утверждение заявки на командировку</span><span class="sxs-lookup"><span data-stu-id="b0b17-125">Approve travel requisitions</span></span>

<span data-ttu-id="b0b17-126">Выберите заявку на командировку, которую вы хотите утвердить, затем выберите **Рабочий процесс** > **Утвердить**.</span><span class="sxs-lookup"><span data-stu-id="b0b17-126">Select the travel requisition that you want to approve, and then select **Workflow** > **Approve**.</span></span>  

## <a name="submit-an-expense-report-using-your-approved-travel-requisition"></a><span data-ttu-id="b0b17-127">Отправка отчета о расходах с использованием утвержденной заявки на командировку</span><span class="sxs-lookup"><span data-stu-id="b0b17-127">Submit an expense report using your approved travel requisition</span></span>

1. <span data-ttu-id="b0b17-128">Создайте новый отчет о расходах и в заголовке отчета о расходах и из списка утвержденных заявок на командировки выберите **Сопоставить с заявкой на командировку**.</span><span class="sxs-lookup"><span data-stu-id="b0b17-128">Create a new expense report and in the expense report header, and from the list of approved travel requisitions, select **Map to Travel requisition**.</span></span>
2. <span data-ttu-id="b0b17-129">Поле **Сумма заявки на командировку** автоматически обновляется в заголовке отчета о расходах.</span><span class="sxs-lookup"><span data-stu-id="b0b17-129">The **Travel requisition amount** field is automatically updated in the expense report header.</span></span>
3. <span data-ttu-id="b0b17-130">Добавьте все расходы на командировку.</span><span class="sxs-lookup"><span data-stu-id="b0b17-130">Add each expense incurred for the trip.</span></span> <span data-ttu-id="b0b17-131">Если поле **Предварительно авторизовано** включено, сверенная сумма и разрешенная сумма для конкретной категории расходов будут обновлены.</span><span class="sxs-lookup"><span data-stu-id="b0b17-131">If the **Pre-authorized** field is enabled, the reconciled amount and authorized amount for the specific expense category will be updated.</span></span>

> [!NOTE]
> <span data-ttu-id="b0b17-132">Когда вы сопоставляете отчет о расходах с утвержденной заявкой на командировку, сумма транзакции не может превышать разрешенную сумму.</span><span class="sxs-lookup"><span data-stu-id="b0b17-132">When you map an expense report to an approved travel requisition, the transaction amount can't be greater than the authorized amount.</span></span> 
