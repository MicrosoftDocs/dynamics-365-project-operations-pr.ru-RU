---
title: Почему цена по умолчанию принимает нулевое значение в фактических данных расходов продаж?
description: Следующие три проверки помогут вам диагностировать, почему цена по умолчанию принимает нулевое значение в фактических данных расходов продаж.
author: rumant
manager: kfend
ms.prod: ''
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: bd474d7c0cd64262fdb21d6269efa781b6dc31f2
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285903"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-sales-actuals"></a><span data-ttu-id="9cccf-103">Почему цена по умолчанию принимает нулевое значение в фактических данных расходов продаж?</span><span class="sxs-lookup"><span data-stu-id="9cccf-103">Why is the price defaulting to zero on expense sales actuals?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="9cccf-104">Эти вопросы и ответы относятся к фактическим данным расходов с классом транзакции "Расход" и типом транзакции "Продажи без выставления счета".</span><span class="sxs-lookup"><span data-stu-id="9cccf-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Unbilled Sales.</span></span> <span data-ttu-id="9cccf-105">Следующие три проверки помогут вам диагностировать, почему цена (ставка по счету) по умолчанию принимает нулевое значение в фактических данных расходов продаж.</span><span class="sxs-lookup"><span data-stu-id="9cccf-105">The following three checks will help you troubleshoot why price (bill rate) is defaulting to 0 on expense sales actuals.</span></span>

## <a name="check-1-identify-the-sales-price-list-for-project"></a><span data-ttu-id="9cccf-106">Проверка 1. Укажите прайс-лист продаж для проекта</span><span class="sxs-lookup"><span data-stu-id="9cccf-106">Check 1: Identify the sales price list for project</span></span>

<span data-ttu-id="9cccf-107">Найдите проект из проектного поля фактических данных и перейдите на страницу проекта.</span><span class="sxs-lookup"><span data-stu-id="9cccf-107">Find the project from the project field of the actual and go to the project page.</span></span> <span data-ttu-id="9cccf-108">Затем перейдите на вкладку "Продажи". В сетке строк контракта по проекту щелкните ссылку в поле "Контракт по проекту".</span><span class="sxs-lookup"><span data-stu-id="9cccf-108">Then go to the Sales tab. On the Project Contract lines grid, click on the link in the Project Contract field.</span></span> <span data-ttu-id="9cccf-109">Открывается страница "Контракт по проекту".</span><span class="sxs-lookup"><span data-stu-id="9cccf-109">The Project Contract page will open.</span></span> <span data-ttu-id="9cccf-110">На странице контракта по проекту перейдите на вкладку прайс-листов проекта. Убедитесь, что хотя бы один прайс-лист добавлен здесь.</span><span class="sxs-lookup"><span data-stu-id="9cccf-110">On the Project Contract page, go to the Project Price Lists tab. Check if there is at least one price list attached here.</span></span>

<span data-ttu-id="9cccf-111">Если нет прайс-листов, добавленных в сетке прайс-листов проекта контракта по проекту:</span><span class="sxs-lookup"><span data-stu-id="9cccf-111">If there is no price list attached in the Project Price Lists grid of the Project Contract:</span></span>

- <span data-ttu-id="9cccf-112">Добавьте прайс-лист в сетку прайс-листов проекта.</span><span class="sxs-lookup"><span data-stu-id="9cccf-112">Attach a price list to the Project Price lists grid.</span></span> <span data-ttu-id="9cccf-113">Прайс-листы, которые можно прикреплять здесь, должны иметь поле контекста с заданным значением "Продажи" и поле валюты в прайс-листе должно соответствовать полю валюты в контракте по проекту.</span><span class="sxs-lookup"><span data-stu-id="9cccf-113">The price lists allowed to be attached here should have the context field set to Sales and the currency field on the price list should match the currency field on the Project Contract.</span></span> <span data-ttu-id="9cccf-114">После внесения необходимых исправлений заново создайте запись расходов, утвердите ее и убедитесь, что в фактических данных продаж без выставления счета отображается действительная цена.</span><span class="sxs-lookup"><span data-stu-id="9cccf-114">Once you’ve made the required fixes, recreate an expense entry, approve it, and verify that the unbilled sales actual shows a valid price.</span></span>
- <span data-ttu-id="9cccf-115">Если один или несколько прайс-листов присоединены в сетке прайс-листов проекта для контракта по проекту, переходите к проверке 2.</span><span class="sxs-lookup"><span data-stu-id="9cccf-115">If you have one or more price lists attached in the Project Price Lists grid of the Project Contract, go to Check 2.</span></span>

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-expense-actual"></a><span data-ttu-id="9cccf-116">Проверка 2. Действительны ли все прайс-листы, определенные выше, для конкретной даты фактических данных о расходах?</span><span class="sxs-lookup"><span data-stu-id="9cccf-116">Check 2: Are any of the price lists identified above valid for the specific date of the expense actual?</span></span>

<span data-ttu-id="9cccf-117">Чтобы приложение Project Service учитывало прайс-лист для выбора цены по умолчанию, этот прайс-лист должен быть применим на дату фактических данных расходов продаж.</span><span class="sxs-lookup"><span data-stu-id="9cccf-117">For Project Service to consider a price list for defaulting price, that price list should be applicable for the date on the expense sales actual.</span></span> <span data-ttu-id="9cccf-118">Проверьте следующее, чтобы проверьте, применимы ли прайс-листы, указанные выше.</span><span class="sxs-lookup"><span data-stu-id="9cccf-118">Check the following to see if the price list(s) identified above are applicable:</span></span>

- <span data-ttu-id="9cccf-119">Сначала проверьте, не пусты ли даты начала и окончания на вкладке общих сведений для прикрепленных прайс-листов.</span><span class="sxs-lookup"><span data-stu-id="9cccf-119">Start by checking if start and end dates on the general tab for the price lists attached aren’t empty.</span></span> <span data-ttu-id="9cccf-120">Если даты начала и окончания в прайс-листах, указанных выше, пусты, проблема обнаружена.</span><span class="sxs-lookup"><span data-stu-id="9cccf-120">If the start and end dates on the price lists identified above are empty, you have isolated the problem.</span></span> 
- <span data-ttu-id="9cccf-121">Запишите значение поля даты начала в фактических данных расходов продаж и проверьте, применимы ли определенные выше прайс-листы на эту дату.</span><span class="sxs-lookup"><span data-stu-id="9cccf-121">Make a note of the start date field on your expense sales actual and check if any of the price lists identified is applicable for that date.</span></span> <span data-ttu-id="9cccf-122">Например, дата фактических данных о расходах должна лежать между датами начала и окончания для прайс-листа.</span><span class="sxs-lookup"><span data-stu-id="9cccf-122">For example, the date of the expense actual should fall within the start date and end date on the price list.</span></span> 
    - <span data-ttu-id="9cccf-123">Если нет прайс-листа, который охватывает эту дату в фактических данных расходов продаж, проблема обнаружена.</span><span class="sxs-lookup"><span data-stu-id="9cccf-123">If there is no price list that covers that date on the expense sales actual, you have isolated the problem.</span></span> <span data-ttu-id="9cccf-124">Измените даты начала и окончания действия прайс-листа, чтобы этот прайс-лист охватывал дату фактических данных расходов.</span><span class="sxs-lookup"><span data-stu-id="9cccf-124">Modify the start and end dates of the price list to ensure that the price list covers the date of the expense actual.</span></span> 
    - <span data-ttu-id="9cccf-125">Если несколько прайс-листов охватывают дату в фактических данных расходов продаж, проблема обнаружена.</span><span class="sxs-lookup"><span data-stu-id="9cccf-125">If there is more than one price list that covers the date on the expense sales actual, you have isolated the problem.</span></span> <span data-ttu-id="9cccf-126">Измените даты начала и окончания прайс-листов, чтобы только один прайс-лист охватывал дату фактических данных расходов.</span><span class="sxs-lookup"><span data-stu-id="9cccf-126">Edit the start and end dates of the price list(s) so that there is only one price list that covers the date of the expense actual.</span></span> 
    - <span data-ttu-id="9cccf-127">Если есть только один прайс-лист, который охватывает эту дату фактических данных расходов, переходите к проверке 3.</span><span class="sxs-lookup"><span data-stu-id="9cccf-127">If there is only one price list that covers that date of the expense actual, move to Check 3.</span></span>
<span data-ttu-id="9cccf-128">После внесения необходимых исправлений заново создайте запись расходов, утвердите ее и убедитесь, что в фактических данных продаж без выставления счета отображается действительная цена.</span><span class="sxs-lookup"><span data-stu-id="9cccf-128">Once you’ve done made the required fixes, recreate an expense entry, approve it, and verify that the unbilled sales actual shows a valid price.</span></span>

## <a name="check-3-is-there-a-valid-price-for-the-expense-category-in-the-applicable-project-price-list"></a><span data-ttu-id="9cccf-129">Проверка 3. Имеется ли действительная цена по категории расходов в применимом прайс-листе проекта?</span><span class="sxs-lookup"><span data-stu-id="9cccf-129">Check 3: Is there a valid price for the expense category in the applicable project price list?</span></span> 

<span data-ttu-id="9cccf-130">Если вы успешно выполнили проверки 1 и 2, теперь должен остаться только один прайс-лист проекта, который применим для даты фактических данных расходов продаж.</span><span class="sxs-lookup"><span data-stu-id="9cccf-130">If you have successfully completed Check 1 and Check 2, you should now have only one project price list that is applicable for the date of the expense sales actual.</span></span> <span data-ttu-id="9cccf-131">Откройте этот прайс-лист проекта и перейдите на вкладку цен категории. Убедитесь в наличии строки в сетке для определенной категории расходов в фактических данных расходов.</span><span class="sxs-lookup"><span data-stu-id="9cccf-131">Open this Project Price List and go to the Category Prices tab. Make sure that there is a row in the grid for the specific expense category on the Expense actual.</span></span>
 
- <span data-ttu-id="9cccf-132">Если такой строки нет, причина проблемы обнаружена.</span><span class="sxs-lookup"><span data-stu-id="9cccf-132">If there is no row, then you have isolated the problem.</span></span> <span data-ttu-id="9cccf-133">Создайте строку в сетке цен категорий для категории в ваших фактических данных расходов.</span><span class="sxs-lookup"><span data-stu-id="9cccf-133">Create a row in the Category price grid for the category on your expense actual.</span></span> <span data-ttu-id="9cccf-134">Затем, заново создайте запись расходов, утвердите ее и убедитесь, что в фактических данных продаж без выставления счета отображается действительная цена.</span><span class="sxs-lookup"><span data-stu-id="9cccf-134">Then, recreate an expense entry, approve it, and verify that the unbilled sales actual shows a valid price.</span></span> 
- <span data-ttu-id="9cccf-135">Если имеется строка для категории расходов в сетке цен категорий, проверьте, имеется ли в ней действительная цена.</span><span class="sxs-lookup"><span data-stu-id="9cccf-135">If there is a row for the expense category in the category prices grid, check if it has a valid price.</span></span>

<span data-ttu-id="9cccf-136">Чтобы понять, что такое действительная цена, используйте следующие методы:</span><span class="sxs-lookup"><span data-stu-id="9cccf-136">To understand what a valid price is, use these methods:</span></span>

- <span data-ttu-id="9cccf-137">Если для поля метода ценообразования в строке цены категории задано значение "По себестоимости", тогда цена за единицу в фактических данных расходов продаж будет по умолчанию принимать значение в записи расходов.</span><span class="sxs-lookup"><span data-stu-id="9cccf-137">If the Pricing Method field on the Category price line is set to At Cost, then the unit rate on your Expense sales actual will be defaulted to the value in the Expense entry.</span></span>
- <span data-ttu-id="9cccf-138">Если для поля метода ценообразования в строке цены категории задано значение "Процент наценки", убедитесь, что в поле процентов задано допустимое значение.</span><span class="sxs-lookup"><span data-stu-id="9cccf-138">If the Pricing Method field on the Category price line is set to Markup Percentage, then check if the Percent field is set to a valid value.</span></span> <span data-ttu-id="9cccf-139">Цена за единицу в фактических данных расходов продаж по умолчанию определяется путем применения процента наценки к цене в записи расходов.</span><span class="sxs-lookup"><span data-stu-id="9cccf-139">The unit rate on your Expense sales actual is defaulted by applying this markup percent to the price in the Expense entry.</span></span>
- <span data-ttu-id="9cccf-140">Если для поля метода ценообразования в строке цены категории задано значение "Цена за единицу", убедитесь, что в поле цены задано допустимое значение.</span><span class="sxs-lookup"><span data-stu-id="9cccf-140">If the Pricing Method field on the Category price line is set to Price per Unit, then check if the Price field is set to a valid value.</span></span> <span data-ttu-id="9cccf-141">Цена за единицу в фактических данных расходов продаж будет по умолчанию равна сумме, указанной в поле цены.</span><span class="sxs-lookup"><span data-stu-id="9cccf-141">The unit rate on your Expense sales actual will be defaulted to the currency amount specified in the Price field.</span></span>

<span data-ttu-id="9cccf-142">Если настроенная цена по категории расходов недействительна, причина проблемы обнаружена.</span><span class="sxs-lookup"><span data-stu-id="9cccf-142">If the price setup for the expense category isn't valid, then you have isolated the problem.</span></span> <span data-ttu-id="9cccf-143">Решение заключается в изменении строки цены категории на действительную ценой для категории расхода в соответствии с приведенными выше правилами.</span><span class="sxs-lookup"><span data-stu-id="9cccf-143">The solution is to edit the category price line with a valid price for the expense category in accordance with the rules above.</span></span> <span data-ttu-id="9cccf-144">После выполнения этого заново создайте запись расходов, утвердите ее и убедитесь, что в фактических данных продаж без выставления счета получается действительная цена.</span><span class="sxs-lookup"><span data-stu-id="9cccf-144">Once you’ve done that, recreate an expense entry, approve it, and then check that the unbilled sales actual gets a valid price.</span></span>

<span data-ttu-id="9cccf-145">Если вы все еще не видите действительную цену в ваших фактических данных расходов продаж после выполнения трех приведенных выше проверок, зарегистрируйте обращение в службу поддержки.</span><span class="sxs-lookup"><span data-stu-id="9cccf-145">If you still don't see a valid price on your expense sales actual after doing the three checks above, log a support ticket.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]