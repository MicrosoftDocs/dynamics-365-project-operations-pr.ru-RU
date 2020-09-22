---
title: Почему цена по умолчанию принимает нулевое значение в фактических данных стоимости расходов?
description: Устранение неполадки, когда цена по умолчанию принимает нулевое значение в фактических данных стоимости расходов.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 8/22/2018
ms.topic: article
ms.prod: Project Service
ms.technology: ''
ms.assetid: bc1ebc58-c733-4310-8435-572ed9a9fef9
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 3fb678822877a61d141de75aea29b7d5cdf292c4
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754948"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a>Почему цена по умолчанию принимает нулевое значение в фактических данных стоимости расходов?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Эти вопросы и ответы относятся к фактическим данным расходов с классом транзакции "Расход" и типом транзакции "Стоимость".

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a>Устранение неполадок норм затрат в фактических данных стоимости расходов

Перейдите к связанной записи расходов и убедитесь, что имеется сумма в поле записи расходов. Если в исходной записи расходов поле суммы не заполнено, причина проблемы обнаружена.
 
Чтобы устранить эту проблему, заново создайте запись расхода с действительной суммой и утвердите ее.
