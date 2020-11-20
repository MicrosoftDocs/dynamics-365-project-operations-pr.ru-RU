---
title: Почему цена по умолчанию принимает нулевое значение в фактических данных стоимости времени?
description: Устранение неполадки, когда цена по умолчанию принимает нулевое значение в фактических данных стоимости времени.
author: rumant
manager: kfend
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
ms.openlocfilehash: 124719410f89dea506d43a1b64cb91c85d4f3968
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131395"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a><span data-ttu-id="d41d4-103">Почему цена по умолчанию принимает нулевое значение в фактических данных стоимости времени?</span><span class="sxs-lookup"><span data-stu-id="d41d4-103">Why is the price defaulting to zero on time cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="d41d4-104">Эти вопросы и ответы относятся к фактическим данным с классом транзакции "Время" и типом транзакции "Стоимость".</span><span class="sxs-lookup"><span data-stu-id="d41d4-104">This FAQ applies to actuals where the transaction class is set to Time and transaction type is Cost.</span></span> <span data-ttu-id="d41d4-105">Следующие три проверки помогут вам диагностировать, почему цена по умолчанию принимает нулевое значение в фактических данных стоимости времени.</span><span class="sxs-lookup"><span data-stu-id="d41d4-105">The following three checks will help you troubleshoot why the price is defaulting to 0 on time cost actuals.</span></span>
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a><span data-ttu-id="d41d4-106">Проверка 1. Определите прайс-лист стоимости для проекта</span><span class="sxs-lookup"><span data-stu-id="d41d4-106">Check 1: Identify the cost price list for the project</span></span>

<span data-ttu-id="d41d4-107">Найдите проект из проектного поля фактических данных, затем перейдите на страницу проекта.</span><span class="sxs-lookup"><span data-stu-id="d41d4-107">Find the project from the project field of the actual and then go to the project page.</span></span> <span data-ttu-id="d41d4-108">Щелкните ссылку единицы по контракту в этом поле.</span><span class="sxs-lookup"><span data-stu-id="d41d4-108">Click on the contracting unit link in the field.</span></span> <span data-ttu-id="d41d4-109">На странице единицы по контракту проверьте, имеет ли единица по контракту прайс-лист в сетке "Прайс-листы стоимости".</span><span class="sxs-lookup"><span data-stu-id="d41d4-109">On the Contracting Unit page, check if the contracting unit has a price list in the Cost Price Lists grid.</span></span>

<span data-ttu-id="d41d4-110">При наличии нескольких прайс-листов причина проблемы обнаружена.</span><span class="sxs-lookup"><span data-stu-id="d41d4-110">If there is more than one price list, you have isolated the problem.</span></span> <span data-ttu-id="d41d4-111">Project Service поддерживает только один прайс-лист на подразделение.</span><span class="sxs-lookup"><span data-stu-id="d41d4-111">Project Service only supports one price list per organizational unit.</span></span> <span data-ttu-id="d41d4-112">Удалите все прайс-листы из этой сущности, чтобы остался только один прайс-лист, присоединенный к сетке "Прайс-листы стоимости" подразделения.</span><span class="sxs-lookup"><span data-stu-id="d41d4-112">Remove all prices lists from this entity until there is only one price list attached in the Cost Price Lists grid of the Organizational Unit.</span></span>

<span data-ttu-id="d41d4-113">Если к подразделению не присоединены никакие прайс-листы, запишите валюту подразделения.</span><span class="sxs-lookup"><span data-stu-id="d41d4-113">If there are no price lists attached to the Organizational Unit, make a note of the currency of the Organizational unit.</span></span> <span data-ttu-id="d41d4-114">Перейдите в Project Service, затем откройте "Параметры" и выберите вкладку "Прайс-листы". Проверьте, имеются ли какие-либо прайс-листы с контекстом "Стоимость" и валютой, которая соответствует валюте подразделения.</span><span class="sxs-lookup"><span data-stu-id="d41d4-114">Go to the Project Service and then Parameters and open the Price Lists tab. Check if there are any price lists with context set to Cost and currency that matches the currency of the Organizational Unit.</span></span>
 
<span data-ttu-id="d41d4-115">Если нет прайс-листов, соответствующих этим критериям, то вы изолировали проблему.</span><span class="sxs-lookup"><span data-stu-id="d41d4-115">If there are no price lists that match that criteria, you have isolated the problem.</span></span> <span data-ttu-id="d41d4-116">Обеспечьте наличие хотя бы одного прайс-листа с контекстом "Стоимость" и валютой, совпадающей с валютой подразделения.</span><span class="sxs-lookup"><span data-stu-id="d41d4-116">Make sure to have at least one price list whose context is set to Cost and whose currency matches the currency of the Organizational Unit.</span></span>

<span data-ttu-id="d41d4-117">Если существует несколько прайс-листов, которые соответствуют критериям, продолжайте читать этот документ для выполнения дополнительных проверок.</span><span class="sxs-lookup"><span data-stu-id="d41d4-117">If there is more than one price list that match that criteria, continue reading this document to make more checks.</span></span>

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a><span data-ttu-id="d41d4-118">Проверка 2. Действительны ли все прайс-листы, определенные выше, для конкретной даты фактических данных о стоимости времени?</span><span class="sxs-lookup"><span data-stu-id="d41d4-118">Check 2: Are any of the price lists identified above valid for the specific date of the time cost actual?</span></span>

<span data-ttu-id="d41d4-119">Чтобы приложение Project Service учитывало прайс-лист для выбора цены по умолчанию, этот прайс-лист должен быть применим на дату фактических данных стоимости времени.</span><span class="sxs-lookup"><span data-stu-id="d41d4-119">For Project Service to consider a price list for defaulting price, that price list should be applicable for the date on the time cost actual.</span></span> <span data-ttu-id="d41d4-120">Проверьте следующее, чтобы проверьте, применимы ли прайс-листы, указанные выше.</span><span class="sxs-lookup"><span data-stu-id="d41d4-120">Check the following to see if the price list(s) identified above are applicable:</span></span>

- <span data-ttu-id="d41d4-121">Проверьте, не пусты ли даты начала и окончания на вкладке общих сведений для прикрепленных прайс-листов.</span><span class="sxs-lookup"><span data-stu-id="d41d4-121">Check if the start and end dates on the general tab for the price lists attached aren’t empty.</span></span> <span data-ttu-id="d41d4-122">Если даты начала и окончания в прайс-листах, указанных выше, пусты, причина проблемы обнаружена.</span><span class="sxs-lookup"><span data-stu-id="d41d4-122">If the start and end dates on price lists identified above are empty, you have isolated the problem.</span></span> 
- <span data-ttu-id="d41d4-123">Запишите значение поля даты начала в фактических данных стоимости времени и проверьте, применимы ли определенные выше прайс-листы на эту дату.</span><span class="sxs-lookup"><span data-stu-id="d41d4-123">Make a note of the start date field on your time cost actual and check if any of the price lists identified is applicable for that date.</span></span> <span data-ttu-id="d41d4-124">Например, дата фактических данных о стоимости времени должна лежать между датами начала и окончания для прайс-листа.</span><span class="sxs-lookup"><span data-stu-id="d41d4-124">For example, the date of the time cost actual should fall within the start date and end date on the price list.</span></span> 
    - <span data-ttu-id="d41d4-125">Если нет прайс-листа, который охватывает эту дату в фактических данных стоимости времени, причина проблемы обнаружена.</span><span class="sxs-lookup"><span data-stu-id="d41d4-125">If there is no price list that covers that date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="d41d4-126">Измените даты начала и окончания действия прайс-листа, чтобы этот прайс-лист охватывал дату фактических данных стоимости времени.</span><span class="sxs-lookup"><span data-stu-id="d41d4-126">Modify the start and end dates of the price list to ensure that the price list covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="d41d4-127">Если несколько прайс-листов охватывают дату в фактических данных стоимости времени, причина проблемы обнаружена.</span><span class="sxs-lookup"><span data-stu-id="d41d4-127">If there is more than one price list that covers the date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="d41d4-128">Это можно исправить, изменив даты начала и окончания прайс-листов, чтобы только один прайс-лист охватывал дату фактических данных стоимости времени.</span><span class="sxs-lookup"><span data-stu-id="d41d4-128">You can fix this by editing the start and end dates of the price list(s) so that there is only one price list that covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="d41d4-129">Если имеется только один прайс-лист, который охватывает эту дату фактических данных стоимости времени, перейти к следующей проверке в документе.</span><span class="sxs-lookup"><span data-stu-id="d41d4-129">If there is only one price list that covers that date of the time cost actual, move to the next check in the document.</span></span>
<span data-ttu-id="d41d4-130">После внесения необходимых исправлений заново создайте запись времени, утвердите ее и убедитесь, что в фактических данных стоимости времени отображается действительная цена.</span><span class="sxs-lookup"><span data-stu-id="d41d4-130">Once you’ve done made the required fixes, recreate a time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a><span data-ttu-id="d41d4-131">Проверка 3. Имеется ли цена в прайс-листе для измерений ценообразования в фактических данных стоимости времени?</span><span class="sxs-lookup"><span data-stu-id="d41d4-131">Check 3: Is there a price in the price list for the pricing dimensions on the time cost actual?</span></span>

<span data-ttu-id="d41d4-132">Если вы успешно выполнили проверки 1 и 2, теперь должен остаться только один прайс-лист, который применим для даты фактических данных стоимости времени.</span><span class="sxs-lookup"><span data-stu-id="d41d4-132">If you have successfully completed Check 1 and Check 2, you should now have only one price list that is applicable for the date of the time cost actual.</span></span> <span data-ttu-id="d41d4-133">Откройте этот прайс-лист и перейдите на вкладку цены ролей. Убедитесь в наличии строки в сетке для измерений ценообразования в фактических данных стоимости времени.</span><span class="sxs-lookup"><span data-stu-id="d41d4-133">Open this Price List and go to the Role Prices tab. Make sure that there is a row in the grid for the pricing dimensions on the time cost actual.</span></span>

<span data-ttu-id="d41d4-134">Если нет стоки в сетке цены роли для типа ценообразования в фактических данных стоимости времени, причина проблемы обнаружена.</span><span class="sxs-lookup"><span data-stu-id="d41d4-134">If there is no row in the role price grid for the pricing dimensions on the time cost actual, then you have isolated the problem.</span></span> <span data-ttu-id="d41d4-135">Создайте строку в сетке цен ролей для измерений ценообразования ваших фактических данных стоимости времени.</span><span class="sxs-lookup"><span data-stu-id="d41d4-135">Create a row in the Role prices grid for the pricing dimensions on your time cost actual.</span></span> <span data-ttu-id="d41d4-136">После этого заново создайте запись времени, утвердите ее и убедитесь, что в фактических данных стоимости времени отображается действительная цена.</span><span class="sxs-lookup"><span data-stu-id="d41d4-136">Once this is done, recreate time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>
 
<span data-ttu-id="d41d4-137">Если вы все еще не видите действительную цену в ваших фактических данных стоимости времени после выполнения трех приведенных выше проверок, зарегистрируйте обращение в службу поддержки.</span><span class="sxs-lookup"><span data-stu-id="d41d4-137">If you still don't see a valid price on your time cost actual after you’ve done the three checks above, please log a support ticket.</span></span>



