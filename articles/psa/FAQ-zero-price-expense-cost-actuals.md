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
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a>Почему цена по умолчанию принимает нулевое значение в фактических данных стоимости расходов?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Эти вопросы и ответы относятся к фактическим данным расходов с классом транзакции "Расход" и типом транзакции "Стоимость".

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a>Устранение неполадок норм затрат в фактических данных стоимости расходов

Перейдите к связанной записи расходов и убедитесь, что имеется сумма в поле записи расходов. Если в исходной записи расходов поле суммы не заполнено, причина проблемы обнаружена.
 
Чтобы устранить эту проблему, заново создайте запись расхода с действительной суммой и утвердите ее.
