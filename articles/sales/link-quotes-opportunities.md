---
title: Создание предложений с расценками по проектам на основе возможных сделок
description: В этом разделе представлена информация о создании предложения с расценками по проекту из возможной сделки.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 606098473db479d0015e3a7a3c01a3d3b6de9db1
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898548"
---
# <a name="create-project-quotes-from-opportunities"></a><span data-ttu-id="bb9d5-103">Создание предложений с расценками по проектам на основе возможных сделок</span><span class="sxs-lookup"><span data-stu-id="bb9d5-103">Create project quotes from opportunities</span></span>

<span data-ttu-id="bb9d5-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="bb9d5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="bb9d5-105">Предложения с расценками могут быть созданы на основе возможных сделок проекта следующими способами:</span><span class="sxs-lookup"><span data-stu-id="bb9d5-105">Quotes can be created from project opportunities in the following ways:</span></span>

- <span data-ttu-id="bb9d5-106">С вкладки **Предложения с расценками** на странице **Возможная сделка проекта**</span><span class="sxs-lookup"><span data-stu-id="bb9d5-106">From the **Quotes** tab on the **Project Opportunity** page</span></span>
- <span data-ttu-id="bb9d5-107">Из потока процесса продаж возможных сделок</span><span class="sxs-lookup"><span data-stu-id="bb9d5-107">From the Opportunity sales process flow</span></span>
- <span data-ttu-id="bb9d5-108">Обновив ссылку на возможную сделку в существующем предложении с расценками</span><span class="sxs-lookup"><span data-stu-id="bb9d5-108">By updating the opportunity reference on an existing quote</span></span>

## <a name="from-the-quotes-tab-of-the-project-opportunity-page"></a><span data-ttu-id="bb9d5-109">С вкладки "Предложения с расценками" на странице "Возможная сделка проекта"</span><span class="sxs-lookup"><span data-stu-id="bb9d5-109">From the Quotes tab of the Project Opportunity page</span></span>

<span data-ttu-id="bb9d5-110">Чтобы создать предложение с расценками по проекту на основе возможной сделки, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-110">To create a project quote from an opportunity, complete the following steps.</span></span>

1. <span data-ttu-id="bb9d5-111">Откройте страницу **Возможная сделка проекта** и выберите вкладку **Предложения с расценками**.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-111">Open the **Project Opportunity** page and select the **Quotes** tab.</span></span> 
2. <span data-ttu-id="bb9d5-112">На вложенной сетке **Предложения с расценками** выберите **+** для создания нового предложения с расценками по проекту на основе возможной сделки.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-112">On the **Quotes** sub-grid, select the **+** to create a new project quote based on the opportunity.</span></span> <span data-ttu-id="bb9d5-113">Все строки возможной сделки и связанные прайс-листы проекта копируются в новое предложение с расценками из возможной сделки.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-113">All of the opportunity lines and related Project price lists are copied to the new quote from the opportunity.</span></span>

## <a name="from-the-opportunity-sales-process-flow"></a><span data-ttu-id="bb9d5-114">Из потока процесса продаж возможных сделок</span><span class="sxs-lookup"><span data-stu-id="bb9d5-114">From the Opportunity sales process flow</span></span>

<span data-ttu-id="bb9d5-115">Чтобы создать предложение с расценками из потока процесса продаж возможной сделки, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-115">To create a quote from the Opportunity sales process flow, complete the following steps.</span></span>

1. <span data-ttu-id="bb9d5-116">В потоке процесса продаж возможной сделки откройте возможную сделку.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-116">From the Opportunity sales process flow, open the Opportunity.</span></span>
2. <span data-ttu-id="bb9d5-117">Выберите стадию **Квалифицировать**.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-117">Select the **Qualify** stage.</span></span> 
3. <span data-ttu-id="bb9d5-118">Выберите **Далее**, затем выберите **+ Создать**, чтобы создать новое предложение с расценками.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-118">Select **Next** and then select **+ Create** to create a new quote.</span></span> <span data-ttu-id="bb9d5-119">Большая часть информации на вкладке **Сводка** для этого нового предложения с расценками будет по умолчанию взята из возможной сделки.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-119">Most of the information on the **Summary** tab for this new quote will have defaulted from the opportunity.</span></span> 
4. <span data-ttu-id="bb9d5-120">Введите любую необходимую информацию, которая отсутствует, или при необходимости обновите значения по умолчанию на вкладке **Сводка**.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-120">Enter in any required information that is missing, or update defaulted values as necessary on the **Summary** tab,</span></span>
5. <span data-ttu-id="bb9d5-121">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-121">Select **Save**.</span></span> <span data-ttu-id="bb9d5-122">Новое предложение с расценками создается и связывается с возможной сделкой.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-122">The new quote is created and associated to the opportunity.</span></span> <span data-ttu-id="bb9d5-123">Теперь вы можете просмотреть информацию о предложении с расценками на вкладке **Предложения с расценками** страницы **Возможная сделка**.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-123">You can now view the quote information on the **Quotes** tab of the **Opportunity** page.</span></span> 

   <span data-ttu-id="bb9d5-124">Процесс продаж возможной сделки переходит на следующий этап, **Предложить**.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-124">The Opportunity sales process moves to the next stage, **Propose**.</span></span>


## <a name="by-updating-the-opportunity-reference-on-an-existing-quote"></a><span data-ttu-id="bb9d5-125">Обновив ссылку на возможную сделку в существующем предложении с расценками</span><span class="sxs-lookup"><span data-stu-id="bb9d5-125">By updating the opportunity reference on an existing quote</span></span>

<span data-ttu-id="bb9d5-126">Существующее предложение с расценками может быть связано с возможной сделкой.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-126">An existing quote can be linked to an Opportunity.</span></span> <span data-ttu-id="bb9d5-127">Выполните следующие шаги, чтобы обновить информацию о возможной сделке в существующем предложении с расценками.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-127">Complete the following steps to update the Opportunity information on an existing quote.</span></span>

1. <span data-ttu-id="bb9d5-128">Откройте страницу **Предложение с расценками** и выберите вкладку **Сводка**.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-128">Open the **Quote** page and select the **Summary** tab.</span></span>
2. <span data-ttu-id="bb9d5-129">В поле **Возможная сделка** выберите возможную сделку, которую вы хотите связать с предложением с расценками.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-129">In the **Opportunity** field, select the opportunity that you want to link to the quote.</span></span> <span data-ttu-id="bb9d5-130">Вы можете увидеть предложение с расценками в сетке **Предложения с расценками** возможной сделки.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-130">You can see the quote in the **Quotes** grid of the Opportunity.</span></span> 
3. <span data-ttu-id="bb9d5-131">Используя процесс продаж возможных сделок, возможная сделка может быть перемещена на следующий этап, **Предложить**.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-131">Using the Opportunity sales process, the opportunity can be moved to the next stage, **Propose**.</span></span> 

   <span data-ttu-id="bb9d5-132">Когда вы перемещаете возможную сделку на этот этап, вы можете выбрать это предложение с расценками из списка предложений с расценками, связанных с этой возможной сделкой.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-132">When you move an opportunity to this stage, you can select this quote from a list of quotes associated with this opportunity.</span></span> <span data-ttu-id="bb9d5-133">Выбор этого предложения с расценками означает, что вы продолжаете работать с ним.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-133">Selecting this quote indicates that you're moving forward with it.</span></span>

   <span data-ttu-id="bb9d5-134">Все остальные предложения с расценками, связанные с возможной сделкой, будут по-прежнему доступны и активны, пока одно из них не будет реализовано.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-134">All the other quotes associated with the Opportunity will still be available and active until one of them is won.</span></span> <span data-ttu-id="bb9d5-135">Вы можете вернуть процесс продаж обратно на предыдущий этап **Квалифицировать** и выбрать другое предложение с расценками, чтобы двигаться дальше с ним.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-135">You can move the sales process back to the previous stage **Qualify**, and pick another quote to move forward with.</span></span>
