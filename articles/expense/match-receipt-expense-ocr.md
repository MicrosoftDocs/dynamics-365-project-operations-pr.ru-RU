---
title: Распознавание текста для сопоставления чеков с расходами
description: Эта тема предоставляет информацию об оптическом распознавании символов (OCR) для квитанций.
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
ms.openlocfilehash: 62d6316c9602089518a94267d8ef2b7fb8d59cd0
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083153"
---
# <a name="match-a-receipt-to-an-expense-using-ocr"></a><span data-ttu-id="db33b-103">Распознавание текста для сопоставления чеков с расходами</span><span class="sxs-lookup"><span data-stu-id="db33b-103">Match a receipt to an expense using OCR</span></span>

<span data-ttu-id="db33b-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="db33b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="db33b-105">Ввод расходов был улучшен за счет внедрения обработки оптического распознавания символов (OCR) для квитанций.</span><span class="sxs-lookup"><span data-stu-id="db33b-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="db33b-106">Эта функция предназначена для улучшения работы пользователей при создании отчетов о расходах.</span><span class="sxs-lookup"><span data-stu-id="db33b-106">This functionality is designed to improve the user experience when creating expense reports.</span></span>

## <a name="key-features"></a><span data-ttu-id="db33b-107">Ключевые функции</span><span class="sxs-lookup"><span data-stu-id="db33b-107">Key features</span></span>

- <span data-ttu-id="db33b-108">Система извлекает имя продавца, дату и общую сумму из квитанций.</span><span class="sxs-lookup"><span data-stu-id="db33b-108">The system extracts the merchant name, date, and total amount from receipts.</span></span>
- <span data-ttu-id="db33b-109">Система попытается сопоставить непривязанные квитанции с непривязанными проводками расходов.</span><span class="sxs-lookup"><span data-stu-id="db33b-109">The system will try to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="db33b-110">Из квитанций можно создавать вводимые вручную проводки расходов.</span><span class="sxs-lookup"><span data-stu-id="db33b-110">You can create manually entered expense transactions from receipts.</span></span>

## <a name="attach-receipts-to-an-expense-report"></a><span data-ttu-id="db33b-111">Прикрепление квитанций к отчету о расходах</span><span class="sxs-lookup"><span data-stu-id="db33b-111">Attach receipts to an expense report</span></span>

<span data-ttu-id="db33b-112">Чтобы автоматически прикреплять квитанции, содержащие транзакции по кредитной карте, при создании отчета о расходах, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="db33b-112">To automatically attach receipts that include credit card transactions when an expense report is created, complete the following steps.</span></span>

  1. <span data-ttu-id="db33b-113">Открой рабочую область **Управление расходами**.</span><span class="sxs-lookup"><span data-stu-id="db33b-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="db33b-114">На вкладке **Квитанции** убедитесь, что существуют непривязанные квитанции.</span><span class="sxs-lookup"><span data-stu-id="db33b-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="db33b-115">Вы также можете отправлять квитанции на вкладке **Квитанции**.</span><span class="sxs-lookup"><span data-stu-id="db33b-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="db33b-116">На вкладке **Расходы** убедитесь, что существуют непривязанные расходы.</span><span class="sxs-lookup"><span data-stu-id="db33b-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="db33b-117">Как правило, администратор расходов импортирует эти расходы от поставщика кредитной карты.</span><span class="sxs-lookup"><span data-stu-id="db33b-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="db33b-118">Выберите **Создать отчет о расходах**.</span><span class="sxs-lookup"><span data-stu-id="db33b-118">Select **New expense report**.</span></span> <span data-ttu-id="db33b-119">Обратите внимание, что вы можете включать теперь также расходы и квитанции при создании отчета о расходах.</span><span class="sxs-lookup"><span data-stu-id="db33b-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="db33b-120">Если вы добавляете и расходы, и квитанции, запускается автоматическое сопоставление квитанций с расходами.</span><span class="sxs-lookup"><span data-stu-id="db33b-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

## <a name="create-or-match-receipts-to-an-expense-report"></a><span data-ttu-id="db33b-121">Создание или сопоставление квитанций для отчета о расходах</span><span class="sxs-lookup"><span data-stu-id="db33b-121">Create or match receipts to an expense report</span></span>
<span data-ttu-id="db33b-122">Чтобы создать расход или сопоставить расход с квитанцией, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="db33b-122">To create an expense, or match an expense from a receipt, complete the following steps.</span></span>

  1. <span data-ttu-id="db33b-123">В отчете о расходах на вкладке **Квитанции** прикрепите квитанцию, выбрав **Добавить чеки**.</span><span class="sxs-lookup"><span data-stu-id="db33b-123">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="db33b-124">Под загруженным изображением квитанции обратите внимание на параметры **Создайте** и **Сопоставить**.</span><span class="sxs-lookup"><span data-stu-id="db33b-124">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="db33b-125">Выберите **Создать** для создания вводимой вручную расходной проводки и заполнения значений, извлеченных из квитанции.</span><span class="sxs-lookup"><span data-stu-id="db33b-125">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="db33b-126">Если вы выберете **Сопоставить** , система пытается сопоставить существующий расход с квитанцией.</span><span class="sxs-lookup"><span data-stu-id="db33b-126">If you select **Match** , the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="db33b-127">Установка</span><span class="sxs-lookup"><span data-stu-id="db33b-127">Installation</span></span>

<span data-ttu-id="db33b-128">Чтобы использовать эти расширенные возможности по расходам, установите надстройку службы управления расходами для Microsoft Dynamics 365 Finance и включите функции в своем экземпляре.</span><span class="sxs-lookup"><span data-stu-id="db33b-128">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="db33b-129">Вы можете получить доступ к надстройке из своего проекта в Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="db33b-129">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="db33b-130">Войдите в LCS и откройте желаемую среду.</span><span class="sxs-lookup"><span data-stu-id="db33b-130">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="db33b-131">Перейти к пункту **Полная информация**.</span><span class="sxs-lookup"><span data-stu-id="db33b-131">Go to **Full details**.</span></span>
3. <span data-ttu-id="db33b-132">Выберите **Ведение** или прокрутите вниз до экспресс-вкладки **Надстройки среды**.</span><span class="sxs-lookup"><span data-stu-id="db33b-132">Select **Maintain** , or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="db33b-133">Выберите **Установить новую надстройку**.</span><span class="sxs-lookup"><span data-stu-id="db33b-133">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="db33b-134">Выберите **Служба управления расходами**.</span><span class="sxs-lookup"><span data-stu-id="db33b-134">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="db33b-135">Следуйте инструкциям по установке и согласитесь с условиями.</span><span class="sxs-lookup"><span data-stu-id="db33b-135">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="db33b-136">Выберите **Установить**.</span><span class="sxs-lookup"><span data-stu-id="db33b-136">Select **Install**.</span></span>

<span data-ttu-id="db33b-137">В рабочей области **Управление функциями** включите следующие функции:</span><span class="sxs-lookup"><span data-stu-id="db33b-137">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="db33b-138">Новый взгляд на отчеты о расходах</span><span class="sxs-lookup"><span data-stu-id="db33b-138">Expense reports re-imagined</span></span>
- <span data-ttu-id="db33b-139">Автоматическое сопоставление и создание расходов из чека</span><span class="sxs-lookup"><span data-stu-id="db33b-139">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="db33b-140">Когда вы включаете эти функции, происходят следующие действия:</span><span class="sxs-lookup"><span data-stu-id="db33b-140">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="db33b-141">Существующая рабочая область **Управление расходами** заменяется новой рабочей областью.</span><span class="sxs-lookup"><span data-stu-id="db33b-141">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="db33b-142">Добавляется новый пункт меню для видимости поля расходов.</span><span class="sxs-lookup"><span data-stu-id="db33b-142">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="db33b-143">Вы все еще можете открыть старую страницу **Отчеты о расходах** , перейдя по пути **Управление расходами > Мои расходы > Отчеты о расходах**.</span><span class="sxs-lookup"><span data-stu-id="db33b-143">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="db33b-144">Рабочие процессы и любые утверждения по-прежнему переносят вас на существующую страницу отчетов о расходах.</span><span class="sxs-lookup"><span data-stu-id="db33b-144">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="db33b-145">Квитанции будут обработаны через службы Microsoft Azure Cognitive Services, и метаданные будут извлечены и добавлены.</span><span class="sxs-lookup"><span data-stu-id="db33b-145">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="db33b-146">Добавлена опция, позволяющая создавать отчет о расходах, включающий сопоставленные непривязанные квитанции.</span><span class="sxs-lookup"><span data-stu-id="db33b-146">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="db33b-147">Опция, которая добавляется к отчетам о расходах, позволяет создать строку расходов из квитанции или пытается сопоставить существующую квитанцию с существующей строкой расходов.</span><span class="sxs-lookup"><span data-stu-id="db33b-147">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="db33b-148">Вопросы и ответы</span><span class="sxs-lookup"><span data-stu-id="db33b-148">Frequently asked questions</span></span>

<span data-ttu-id="db33b-149">**Использует ли Microsoft мои данные для своих моделей?**</span><span class="sxs-lookup"><span data-stu-id="db33b-149">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="db33b-150">Нет, Microsoft построила общую модель машинного обучения для своей службы обработки квитанций.</span><span class="sxs-lookup"><span data-stu-id="db33b-150">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="db33b-151">Эта модель не основана на загружаемых вами квитанциях.</span><span class="sxs-lookup"><span data-stu-id="db33b-151">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="db33b-152">**Где эта функция доступна и обрабатывается?**</span><span class="sxs-lookup"><span data-stu-id="db33b-152">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="db33b-153">В настоящее время поддерживается в США.</span><span class="sxs-lookup"><span data-stu-id="db33b-153">Currently, the United States is supported.</span></span>

<span data-ttu-id="db33b-154">**Куда уходят мои чеки?**</span><span class="sxs-lookup"><span data-stu-id="db33b-154">**Where do my receipts go?**</span></span>

<span data-ttu-id="db33b-155">Приложение Finance обращается в Cognitive Services для извлечения данных из полей.</span><span class="sxs-lookup"><span data-stu-id="db33b-155">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="db33b-156">Службы Cognitive Services хранят копию вашей квитанции до 24 часов, пока происходит обработка.</span><span class="sxs-lookup"><span data-stu-id="db33b-156">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="db33b-157">После завершения обработки службы Cognitive Services удалят квитанцию.</span><span class="sxs-lookup"><span data-stu-id="db33b-157">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="db33b-158">Квитанции по-прежнему хранятся в Finance.</span><span class="sxs-lookup"><span data-stu-id="db33b-158">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="db33b-159">Дополнительные сведения см. в разделе [Включение распознавания чеков с помощью новой возможности распознавателя документов](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="db33b-159">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>
