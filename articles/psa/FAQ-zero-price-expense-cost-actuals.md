---
title: Почему цена по умолчанию принимает нулевое значение в фактических данных стоимости расходов?
description: Устранение неполадки, когда цена по умолчанию принимает нулевое значение в фактических данных стоимости расходов.
author: rumant
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 742b0b9c495b4b3ecb4705be3ece5656f0322ca9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285868"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="c5dcb-103">Почему цена по умолчанию принимает нулевое значение в фактических данных стоимости расходов?</span><span class="sxs-lookup"><span data-stu-id="c5dcb-103">Why is the price defaulting to zero on expense cost actuals</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="c5dcb-104">Эти вопросы и ответы относятся к фактическим данным расходов с классом транзакции "Расход" и типом транзакции "Стоимость".</span><span class="sxs-lookup"><span data-stu-id="c5dcb-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="c5dcb-105">Устранение неполадок норм затрат в фактических данных стоимости расходов</span><span class="sxs-lookup"><span data-stu-id="c5dcb-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="c5dcb-106">Перейдите к связанной записи расходов и убедитесь, что имеется сумма в поле записи расходов.</span><span class="sxs-lookup"><span data-stu-id="c5dcb-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="c5dcb-107">Если в исходной записи расходов поле суммы не заполнено, причина проблемы обнаружена.</span><span class="sxs-lookup"><span data-stu-id="c5dcb-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="c5dcb-108">Чтобы устранить эту проблему, заново создайте запись расхода с действительной суммой и утвердите ее.</span><span class="sxs-lookup"><span data-stu-id="c5dcb-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]