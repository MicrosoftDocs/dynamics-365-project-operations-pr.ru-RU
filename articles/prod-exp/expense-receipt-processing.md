---
title: Обработка чеков по расходам
description: Эта тема предоставляет информацию об оптическом распознавании символов (OCR) для квитанций. Эта функция предназначена для улучшения работы пользователей при создании отчетов о расходах в Microsoft Dynamics 365 Finance.
author: stsporen
manager: AnnBe
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 31c08ea264e6caec3217f4b424275495f39123e3
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083346"
---
# <a name="expense-receipt-processing"></a><span data-ttu-id="dde83-104">Обработка чеков по расходам</span><span class="sxs-lookup"><span data-stu-id="dde83-104">Expense receipt processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dde83-105">Ввод расходов был улучшен за счет внедрения обработки оптического распознавания символов (OCR) для квитанций.</span><span class="sxs-lookup"><span data-stu-id="dde83-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="dde83-106">Эта функция предназначена для улучшения работы пользователей при создании отчетов о расходах.</span><span class="sxs-lookup"><span data-stu-id="dde83-106">This feature is designed to improve the user experience when expense reports are created.</span></span>

## <a name="key-features"></a><span data-ttu-id="dde83-107">Ключевые функции</span><span class="sxs-lookup"><span data-stu-id="dde83-107">Key features</span></span>

- <span data-ttu-id="dde83-108">Имя продавца, дата и общая сумма извлекаются из квитанций.</span><span class="sxs-lookup"><span data-stu-id="dde83-108">The merchant name, date, and total amount are extracted from receipts.</span></span>
- <span data-ttu-id="dde83-109">Функция попытается сопоставить непривязанные квитанции с непривязанными проводками расходов.</span><span class="sxs-lookup"><span data-stu-id="dde83-109">The feature tries to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="dde83-110">Из квитанций пользователи могут создавать вводимые вручную проводки расходов.</span><span class="sxs-lookup"><span data-stu-id="dde83-110">Users can create manually entered expense transactions from receipts.</span></span>

## <a name="usage-examples"></a><span data-ttu-id="dde83-111">Примеры использования</span><span class="sxs-lookup"><span data-stu-id="dde83-111">Usage examples</span></span>

<span data-ttu-id="dde83-112">Чтобы автоматически прикреплять квитанции, содержащие транзакции по кредитной карте, при создании отчета о расходах, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="dde83-112">To automatically attach receipts that include credit card transactions when an expense report is created, do the following:</span></span>

  1. <span data-ttu-id="dde83-113">Открой рабочую область **Управление расходами**.</span><span class="sxs-lookup"><span data-stu-id="dde83-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="dde83-114">На вкладке **Квитанции** убедитесь, что существуют непривязанные квитанции.</span><span class="sxs-lookup"><span data-stu-id="dde83-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="dde83-115">Вы также можете отправлять квитанции на вкладке **Квитанции**.</span><span class="sxs-lookup"><span data-stu-id="dde83-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="dde83-116">На вкладке **Расходы** убедитесь, что существуют непривязанные расходы.</span><span class="sxs-lookup"><span data-stu-id="dde83-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="dde83-117">Как правило, администратор расходов импортирует эти расходы от поставщика кредитной карты.</span><span class="sxs-lookup"><span data-stu-id="dde83-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="dde83-118">Выберите **Создать отчет о расходах**.</span><span class="sxs-lookup"><span data-stu-id="dde83-118">Select **New expense report**.</span></span> <span data-ttu-id="dde83-119">Обратите внимание, что вы можете включать теперь также расходы и квитанции при создании отчета о расходах.</span><span class="sxs-lookup"><span data-stu-id="dde83-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="dde83-120">Если вы добавляете и расходы, и квитанции, запускается автоматическое сопоставление квитанций с расходами.</span><span class="sxs-lookup"><span data-stu-id="dde83-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

<span data-ttu-id="dde83-121">Чтобы создать расход или сопоставить расход с квитанцией, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="dde83-121">To create an expense, or match an expense from a receipt, do the following:</span></span>

  1. <span data-ttu-id="dde83-122">В отчете о расходах на вкладке **Квитанции** прикрепите квитанцию, выбрав **Добавить чеки**.</span><span class="sxs-lookup"><span data-stu-id="dde83-122">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="dde83-123">Под загруженным изображением квитанции обратите внимание на параметры **Создайте** и **Сопоставить**.</span><span class="sxs-lookup"><span data-stu-id="dde83-123">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="dde83-124">Выберите **Создать** для создания вводимой вручную расходной проводки и заполнения значений, извлеченных из квитанции.</span><span class="sxs-lookup"><span data-stu-id="dde83-124">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="dde83-125">Если вы выберете **Сопоставить** , система пытается сопоставить существующий расход с квитанцией.</span><span class="sxs-lookup"><span data-stu-id="dde83-125">If you select **Match** , the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="dde83-126">Установка</span><span class="sxs-lookup"><span data-stu-id="dde83-126">Installation</span></span>

<span data-ttu-id="dde83-127">Эта функция работает в сочетании с функцией **Переработанные отчеты о расходах** , чтобы помочь упростить работу с расходами.</span><span class="sxs-lookup"><span data-stu-id="dde83-127">This feature works in combination with the **Expense reports re-imagined** feature to help simplify the expense experience.</span></span> <span data-ttu-id="dde83-128">Эта функция доступна только для сред уровня 2+, то есть для среды песочницы и рабочей среды.</span><span class="sxs-lookup"><span data-stu-id="dde83-128">This feature is only available for Tier 2+ environments, which are Sandbox and Production.</span></span>

<span data-ttu-id="dde83-129">Чтобы использовать эти расширенные возможности по расходам, установите надстройку службы управления расходами для Microsoft Dynamics 365 Finance и включите функции в своем экземпляре.</span><span class="sxs-lookup"><span data-stu-id="dde83-129">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="dde83-130">Вы можете получить доступ к надстройке из своего проекта в Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="dde83-130">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="dde83-131">Войдите в LCS и откройте желаемую среду.</span><span class="sxs-lookup"><span data-stu-id="dde83-131">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="dde83-132">Перейти к пункту **Полная информация**.</span><span class="sxs-lookup"><span data-stu-id="dde83-132">Go to **Full details**.</span></span>
3. <span data-ttu-id="dde83-133">Выберите **Ведение** или прокрутите вниз до экспресс-вкладки **Надстройки среды**.</span><span class="sxs-lookup"><span data-stu-id="dde83-133">Select **Maintain** , or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="dde83-134">Выберите **Установить новую надстройку**.</span><span class="sxs-lookup"><span data-stu-id="dde83-134">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="dde83-135">Выберите **Служба управления расходами**.</span><span class="sxs-lookup"><span data-stu-id="dde83-135">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="dde83-136">Следуйте инструкциям по установке и согласитесь с условиями.</span><span class="sxs-lookup"><span data-stu-id="dde83-136">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="dde83-137">Выберите **Установить**.</span><span class="sxs-lookup"><span data-stu-id="dde83-137">Select **Install**.</span></span>

<span data-ttu-id="dde83-138">В рабочей области **Управление функциями** включите следующие функции:</span><span class="sxs-lookup"><span data-stu-id="dde83-138">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="dde83-139">Новый взгляд на отчеты о расходах</span><span class="sxs-lookup"><span data-stu-id="dde83-139">Expense reports re-imagined</span></span>
- <span data-ttu-id="dde83-140">Автоматическое сопоставление и создание расходов из чека</span><span class="sxs-lookup"><span data-stu-id="dde83-140">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="dde83-141">Когда вы включаете эти функции, происходят следующие действия:</span><span class="sxs-lookup"><span data-stu-id="dde83-141">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="dde83-142">Существующая рабочая область **Управление расходами** заменяется новой рабочей областью.</span><span class="sxs-lookup"><span data-stu-id="dde83-142">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="dde83-143">Добавляется новый пункт меню для видимости поля расходов.</span><span class="sxs-lookup"><span data-stu-id="dde83-143">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="dde83-144">Вы все еще можете открыть старую страницу **Отчеты о расходах** , перейдя по пути **Управление расходами > Мои расходы > Отчеты о расходах**.</span><span class="sxs-lookup"><span data-stu-id="dde83-144">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="dde83-145">Рабочие процессы и любые утверждения по-прежнему переносят вас на существующую страницу отчетов о расходах.</span><span class="sxs-lookup"><span data-stu-id="dde83-145">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="dde83-146">Квитанции будут обработаны через службы Microsoft Azure Cognitive Services, и метаданные будут извлечены и добавлены.</span><span class="sxs-lookup"><span data-stu-id="dde83-146">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="dde83-147">Добавлена опция, позволяющая создавать отчет о расходах, включающий сопоставленные непривязанные квитанции.</span><span class="sxs-lookup"><span data-stu-id="dde83-147">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="dde83-148">Опция, которая добавляется к отчетам о расходах, позволяет создать строку расходов из квитанции или пытается сопоставить существующую квитанцию с существующей строкой расходов.</span><span class="sxs-lookup"><span data-stu-id="dde83-148">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

<span data-ttu-id="dde83-149">Для получения дополнительной информации о функции переработанных отчетов о расходах см. раздел [Переработанные отчеты о расходах](ExpenseWorkspaceNew.md).</span><span class="sxs-lookup"><span data-stu-id="dde83-149">For more information about the Expense reports re-imagined feature, see [Expense reports reimagined](ExpenseWorkspaceNew.md).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="dde83-150">Вопросы и ответы</span><span class="sxs-lookup"><span data-stu-id="dde83-150">Frequently asked questions</span></span>

<span data-ttu-id="dde83-151">**Использует ли Microsoft мои данные для своих моделей?**</span><span class="sxs-lookup"><span data-stu-id="dde83-151">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="dde83-152">Нет, Microsoft построила общую модель машинного обучения для своей службы обработки квитанций.</span><span class="sxs-lookup"><span data-stu-id="dde83-152">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="dde83-153">Эта модель не основана на загружаемых вами квитанциях.</span><span class="sxs-lookup"><span data-stu-id="dde83-153">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="dde83-154">**Где эта функция доступна и обрабатывается?**</span><span class="sxs-lookup"><span data-stu-id="dde83-154">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="dde83-155">В настоящее время поддерживается в США.</span><span class="sxs-lookup"><span data-stu-id="dde83-155">Currently, the United States is supported.</span></span>

<span data-ttu-id="dde83-156">**Куда уходят мои чеки?**</span><span class="sxs-lookup"><span data-stu-id="dde83-156">**Where do my receipts go?**</span></span>

<span data-ttu-id="dde83-157">Приложение Finance обращается в Cognitive Services для извлечения данных из полей.</span><span class="sxs-lookup"><span data-stu-id="dde83-157">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="dde83-158">Службы Cognitive Services хранят копию вашей квитанции до 24 часов, пока происходит обработка.</span><span class="sxs-lookup"><span data-stu-id="dde83-158">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="dde83-159">После завершения обработки службы Cognitive Services удалят квитанцию.</span><span class="sxs-lookup"><span data-stu-id="dde83-159">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="dde83-160">Квитанции по-прежнему хранятся в Finance.</span><span class="sxs-lookup"><span data-stu-id="dde83-160">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="dde83-161">Дополнительные сведения см. в разделе [Включение распознавания чеков с помощью новой возможности распознавателя документов](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="dde83-161">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>
