---
title: Почему цена по умолчанию принимает нулевое значение в фактических данных стоимости расходов?
description: Устранение неполадки, когда цена по умолчанию принимает нулевое значение в фактических данных стоимости расходов.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/22/2018
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
ms.openlocfilehash: 9f4ff8a96250d675faeda3246c2d0a6c5bd83286
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083209"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="84d17-103">Почему цена по умолчанию принимает нулевое значение в фактических данных стоимости расходов?</span><span class="sxs-lookup"><span data-stu-id="84d17-103">Why is the price defaulting to zero on expense cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="84d17-104">Эти вопросы и ответы относятся к фактическим данным расходов с классом транзакции "Расход" и типом транзакции "Стоимость".</span><span class="sxs-lookup"><span data-stu-id="84d17-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="84d17-105">Устранение неполадок норм затрат в фактических данных стоимости расходов</span><span class="sxs-lookup"><span data-stu-id="84d17-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="84d17-106">Перейдите к связанной записи расходов и убедитесь, что имеется сумма в поле записи расходов.</span><span class="sxs-lookup"><span data-stu-id="84d17-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="84d17-107">Если в исходной записи расходов поле суммы не заполнено, причина проблемы обнаружена.</span><span class="sxs-lookup"><span data-stu-id="84d17-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="84d17-108">Чтобы устранить эту проблему, заново создайте запись расхода с действительной суммой и утвердите ее.</span><span class="sxs-lookup"><span data-stu-id="84d17-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>
