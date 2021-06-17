---
title: Почему цена по умолчанию принимает нулевое значение в фактических данных стоимости расходов?
description: Устранение неполадки, когда цена по умолчанию принимает нулевое значение в фактических данных стоимости расходов.
author: rumant
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
ms.openlocfilehash: 03c958635dec66b0f243872dfb929eba6a20119b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/10/2021
ms.locfileid: "5992802"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a>Почему цена по умолчанию принимает нулевое значение в фактических данных стоимости расходов?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Эти вопросы и ответы относятся к фактическим данным расходов с классом транзакции "Расход" и типом транзакции "Стоимость".

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a>Устранение неполадок норм затрат в фактических данных стоимости расходов

Перейдите к связанной записи расходов и убедитесь, что имеется сумма в поле записи расходов. Если в исходной записи расходов поле суммы не заполнено, причина проблемы обнаружена.
 
Чтобы устранить эту проблему, заново создайте запись расхода с действительной суммой и утвердите ее.


[!INCLUDE[footer-include](../includes/footer-banner.md)]