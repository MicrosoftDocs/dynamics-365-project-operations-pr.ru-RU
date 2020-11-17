---
title: Почему цена по умолчанию принимает нулевое значение в фактических данных продаж времени?
description: Устранение неполадки, когда цена по умолчанию принимает нулевое значение в фактических данных продаж времени.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: c886c4a53b4ba47e381b891fe22a565ad8fd1ac6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083312"
---
# <a name="why-is-price-defaulting-to-zero-on-time-sales-actuals"></a>Почему цена по умолчанию принимает нулевое значение в фактических данных продаж времени?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Эти вопросы и ответы относятся к фактическим данным с классом транзакции "Время" и типом транзакции "Продажи без выставления счета". Следующие три проверки помогут вам диагностировать, почему цена (ставка по счету) по умолчанию принимает нулевое значение в фактических данных продаж времени.

## <a name="check-1-identify-the-sales-price-list-for-the-project"></a>Проверка 1. Определите прайс-лист продаж для проекта

Найдите проект из проектного поля фактических данных и перейдите на страницу проекта. Затем перейдите на вкладку "Продажи" и в сетке строк контракта по проекту щелкните ссылку в поле "Контракт по проекту". Открывается страница контракта по проекту. На странице контракта по проекту перейдите на вкладку прайс-листов проекта. Убедитесь, что хотя бы один прайс-лист добавлен здесь. Если нет прайс-листов, добавленных в сетке прайс-листов проекта контракта по проекту, причина проблемы выявлена. Добавьте прайс-лист в сетку прайс-листов проекта. Прайс-листы, которые можно прикреплять здесь, должны иметь поле контекста с заданным значением "Продажи" и поле валюты в прайс-листе должно соответствовать полю валюты в контракте по проекту. После внесения необходимых исправлений заново создайте запись времени, утвердите ее и убедитесь, что в фактических данных продаж без выставления счета отображается действительная цена. 

Если один или несколько прайс-листов присоединены в сетке прайс-листов проекта для контракта по проекту, переходите к следующей проверке в этом документе.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-sales-actual"></a>Проверка 2. Действительны ли все прайс-листы, определенные выше, для конкретной даты фактических данных о продажах времени?

Чтобы приложение Project Service учитывало прайс-лист для выбора цены по умолчанию, этот прайс-лист должен быть применим на дату фактических данных продажи времени. Проверьте следующее, чтобы проверьте, применимы ли прайс-листы, указанные выше.
- Проверьте, не пусты ли даты начала и окончания на вкладке общих сведений для прикрепленных прайс-листов. Если даты начала и окончания в прайс-листах, указанных выше, пусты, причина проблемы обнаружена. 
- Запишите значение поля даты начала в фактических данных продажи времени и проверьте, применимы ли определенные выше прайс-листы на эту дату. Например, дата фактических данных о продаже времени должна лежать между датами начала и окончания для прайс-листа. 
    - Если нет прайс-листа, который охватывает эту дату в фактических данных продажи времени, причина проблемы обнаружена. Измените даты начала и окончания действия прайс-листа, чтобы этот прайс-лист охватывал дату фактических данных продажи времени. 
    - Если несколько прайс-листов охватывают дату в фактических данных продажи времени, причина проблемы обнаружена. Это можно исправить, изменив даты начала и окончания прайс-листов, чтобы только один прайс-лист охватывал дату фактических данных продажи времени. 
    - Если есть только один прайс-лист, который охватывает эту дату фактических данных продажи времени, переходите к проверке 3.
После внесения необходимых исправлений заново создайте запись времени, утвердите ее и убедитесь, что в фактических данных продажи времени отображается действительная цена.

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-sales-actual"></a>Проверка 3. Имеется ли цена в прайс-листе для измерений ценообразования в фактических данных продажи времени?

Если вы успешно выполнили проверки 1 и 2, теперь должен остаться только один прайс-лист, который применим для даты фактических данных продажи времени. Откройте этот прайс-лист и перейдите на вкладку цены ролей. Убедитесь в наличии строки в сетке для измерений ценообразования в фактических данных продажи времени.

Если нет стоки в сетке цены роли для типа ценообразования в фактических данных продажи времени, причина проблемы обнаружена. Создайте строку в сетке цен ролей для измерений ценообразования ваших фактических данных продажи времени. После этого заново создайте запись времени, утвердите ее и убедитесь, что в фактических данных продажи времени отображается действительная цена.

Если вы все еще не видите действительную цену в ваших фактических данных продаж времени после выполнения трех приведенных выше проверок, зарегистрируйте обращение в службу поддержки. 
