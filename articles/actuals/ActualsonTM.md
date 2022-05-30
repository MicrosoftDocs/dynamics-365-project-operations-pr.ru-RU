---
title: Роль фактических значений во взаимодействии типа "время и материалы"
description: В этом теме приведена информация о влиянии таблицы "Фактические значения" на различные события в течение жизненного цикла взаимодействия типа "время и материалы" в Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 02/22/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: a4ea3f9cf74d8a67447571001b75065b8cde5c00
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580840"
---
# <a name="actuals-impact-in-a-time-and-materials-engagement"></a>Роль фактических значений во взаимодействии типа "время и материалы"

_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_

В следующей таблице перечислены фактические значения для различных типов транзакций, которые создаются при различных событиях в рамках взаимодействия типа "время и материалы".

| Мероприятие | Фактические данные стоимости | Фактические данные продажи без выставления счета | Фактическое значение продаж с выставленным счетом | Пример |
|---|---|---|---|---|
| Создается время. | Неприменимо | Неприменимо | Неприменимо | <p>Сергей Климов из подразделения Fabrikam в США, стоимостная ставка которого составляет 100 долларов США в час, работает над проектом под названием "Установка манипулятора в Adatum". Для этого проекта его контрактная ставка, по которой выставляются счета, составляет 200 долларов США в час. Вот пример записи времени от Сергея Климова:</p><p>Сергей Климов, 8 часов</p> |
| Время отправляется в систему. | Неприменимо | Неприменимо | Неприменимо | Для записи времени создается строка журнала стоимости и журналы "Продажи без выставления счета". В запись в журнале вводится цена и стоимостная ставка, предусмотренные по умолчанию. |
| Запись времени отзывается до ее утверждения. | Неприменимо | Неприменимо | Неприменимо | |
| Время утверждается: количество отправленных в систему часов равно количеству оплачиваемых часов. | Создается фактическое значение стоимости. | Создается фактическое значение продаж без выставленного счета. | Неприменимо | <p>Новые созданные фактические значения:</p><ul><li>**Фактическая стоимость:** Сергей Климов, 8 часов, 800 долларов США</li><li>**Фактическое значение продаж без выставленного счета:** Сергей Климов, 8 часов, 1600 долларов США</li></ul> |
| Время утверждается: количество оплачиваемых часов уменьшается и становится меньше количества отправленных в систему часов. | Создается фактическое значение стоимости. | <p>Создается два фактических значения продаж без выставленного счета:</p><ul><li>Подлежащее оплате фактическое значение продаж без выставленного счета для количества оплачиваемых часов</li><li>Не подлежащее оплате фактическое значение продаж без выставленного счета для оставшегося количества</li></ul> | Неприменимо | <p>Новые созданные фактические значения:</p><ul><li>**Фактическая стоимость:** Сергей Климов, 8 часов, 800 долларов США</li><li>**Фактическое значение продаж без выставленного счета:** Сергей Климов, 6 часов, 1200 долларов США, *Оплачивается*</li><li>**Фактическое значение продаж без выставленного счета:** Сергей Климов, 2 часов, 400 долларов США, *Не оплачивается*</li></ul> |
| Время утверждается: количество оплачиваемых часов увеличивается и становится больше количества отправленных в систему часов. | Создается фактическое значение стоимости. | Создается фактическое значение продаж без выставленного счета. | Неприменимо | <p>Новые созданные фактические значения:</p><ul><li>**Фактическая стоимость:** Сергей Климов, 8 часов, 800 долларов США</li><li>**Фактическое значение продаж без выставленного счета:** Сергей Климов, 10 часов, 2000 долларов США</li></ul> |
| Утверждение времени отменяется. | <p>Состояние корректировки исходного фактического значения стоимости меняется на **Скорректировано**.</p><p>Создается сторнирующее фактическое значение стоимости, в качестве состояния корректировки для которого устанавливается **Не регулируется**.</p> | <p>Состояние корректировки исходного фактического значения продаж без выставленного счета меняется на **Скорректировано**.</p><p>Создается сторнирующее фактическое значение продаж без выставленного счета, в качестве состояния корректировки для которого устанавливается **Не регулируется**.</p> | Неприменимо | <p>Обновленные существующие фактические значения:</p><ul><li>**Фактическая стоимость:** Сергей Климов, 8 часов, 800 долларов США, *Скорректировано*</li><li>**Фактическое значение продаж без выставленного счета:** Сергей Климов, 8 часов, 1600 долларов США, *Скорректировано*</li></ul><p>Новые фактические значения, созданные для сторнирования ранее отраженного финансового результата:</p><ul><li>**Фактическая стоимость:** Сергей Климов, 8 часов, 800 долларов США, *Не регулируется*</li><li>**Фактическое значение продаж без выставленного счета:** Сергей Климов, 8 часов, 1600 долларов США, *Не регулируется*</li></ul> |
| Запись времени отзывается после ее утверждения. | <p>Состояние корректировки исходного фактического значения стоимости меняется на **Скорректировано**.</p><p>Создается сторнирующее фактическое значение стоимости, в качестве состояния корректировки для которого устанавливается **Не регулируется**.</p> | <p>Состояние корректировки исходного фактического значения продаж без выставленного счета меняется на **Скорректировано**.</p><p>Создается сторнирующее фактическое значение продаж без выставленного счета, в качестве состояния корректировки для которого устанавливается **Не регулируется**.</p> | Неприменимо | <p>Обновленные существующие фактические значения:</p><ul><li>**Фактическая стоимость:** Сергей Климов, 8 часов, 800 долларов США, *Скорректировано*</li><li>**Фактическое значение продаж без выставленного счета:** Сергей Климов, 8 часов, 1600 долларов США, *Скорректировано*</li></ul><p>Новые фактические значения, созданные для сторнирования ранее отраженного финансового результата:</p><ul><li>**Фактическая стоимость:** Сергей Климов, 8 часов, 800 долларов США, *Не регулируется*</li><li>**Фактическое значение продаж без выставленного счета:** Сергей Климов, 8 часов, 1600 долларов США, *Не регулируется*</li></ul> |
| Контракт подтверждается. | <p>Состояние корректировки старых фактических значений затрат меняется на **Скорректировано**.</p><p>Создаются сторнирующие фактические значения затрат, в качестве состояния корректировки для которых устанавливается **Не регулируется**.</p><p>После переоценки контрактных правил создаются новые фактические значения затрат.</p> | <p>Состояние корректировки старых фактических значений продаж без выставленного счета меняется на **Скорректировано**.</p><p>Создаются сторнирующте фактические значения продаж без выставленного счета, в качестве состояния корректировки для которых устанавливается **Не регулируется**.</p><p>После переоценки контрактных правил создаются новые фактические значения продаж без выставленного счета.</p> | Неприменимо | <p>Обновленные существующие фактические значения:</p><ul><li>**Фактическая стоимость:** Сергей Климов, 8 часов, 800 долларов США, *Скорректировано*</li><li>**Фактическое значение продаж без выставленного счета:** Сергей Климов, 8 часов, 1600 долларов США, *Скорректировано*</li></ul><p>Новые фактические значения, созданные для сторнирования ранее отраженного финансового результата:</p><ul><li>**Фактическая стоимость:** Сергей Климов, 8 часов, 800 долларов США, *Не регулируется*</li><li>**Фактическое значение продаж без выставленного счета:** Сергей Климов, 8 часов, 1600 долларов США, *Не регулируется*</li></ul><p>Новые фактические значения, созданные для переоцененного финансового результата:</p><ul><li>**Фактическая стоимость:** Сергей Климов, 8 часов, 800 долларов США</li><li>**Фактическое значение продаж без выставленного счета:** Сергей Климов, 8 часов, 1600 долларов США</li></ul> |
| Создается счет. | Неприменимо | Неприменимо | Неприменимо | |
| Счет подтверждается. Количество в сведениях строки счета не изменятся относительно фактического значения продаж без выставленного счета. | Неприменимо | <p>Состояние выставления счета для старых фактических значений продаж без выставленного счета обновляется.</p><p>Создаются сторнирующте фактические значения продаж без выставленного счета, в качестве состояния корректировки для которых устанавливается **Не регулируется**. | Создается фактическое значение продаж с выставленным счетом. | <p>Существующее фактическое значение, которое остается неизменным:</p><ul><li>**Фактическая стоимость:** Сергей Климов, 8 часов, 800 долларов США</li></ul><p>Обновленное существующее фактическое значение:</p><ul><li>**Фактическое значение продаж без выставленного счета:** Сергей Климов, 8 часов, 1600 долларов США, *Счет клиента разнесен*</li></ul>Новое фактическое значение, созданное для сторнирования финансовой незавершенной работы:</p><ul><li>**Фактическое значение продаж без выставленного счета:** Сергей Климов, 8 часов, 1600 долларов США</li></ul><p>Новое фактическое значение, созданное для учета значений продаж с выставленным счетом:</p><ul><li>**Фактическое значение продаж с выставленным счетом:** Сергей Климов, 8 часов, 1600 долларов США</li></ul> |
| Счет подтверждается после того, как количество в сведениях строки счета уменьшается относительно количества в фактическом значении продаж без выставленного счета. | Неприменимо | <p>Состояние корректировки исходных фактических значений продаж без выставленного счета меняется на **Скорректировано**.</p><p>Для исходных фактических значений продаж без выставленного счета создаются сторнирующие фактические значения продаж без выставленного счета. Для них устаналивается состояние корректировки **Не регулируется**.</p><p>Создается два новых фактических значения продаж без выставленного счета:</p><ul><li>Подлежащее оплате фактическое значение продаж без выставленного счета для количества оплачиваемых часов</li><li>Не подлежащее оплате фактическое значение продаж без выставленного счета для оставшегося количества</li></ul><p>Для двух новых фактических значений продаж без выставленного счета создаются сторнирующие фактические значения продаж без выставленного счета.</p> | <p>Создается два фактических значения продаж с выставленным счетом:</p><ul><li>Подлежащее оплате фактическое значение продаж с выставленным счетом для количества оплачиваемых часов</li><li>Не подлежащее оплате фактическое значение продаж с выставленным счетом для оставшегося количества</li></ul> | <p>Существующее фактическое значение, которое остается неизменным:</p><ul><li>**Фактическая стоимость:** Сергей Климов, 8 часов, 800 долларов США</li></ul><p>Обновленное существующее фактическое значение:</p><ul><li>**Фактическое значение продаж без выставленного счета:** Сергей Климов, 8 часов, 1600 долларов США, *Скорректировано*</li></ul><p>Новое фактическое значение, созданное для сторнирования ранее отраженной финансовой незавершенной работы:</p><ul><li>**Фактическое значение продаж без выставленного счета:** Сергей Климов, 8 часов, 1600 долларов США, *Не регулируется*</li></ul><p>Новые фактические значения, созданные для учета обновленной незавершенной работы продаж:</p><ul><li>**Фактическое значение продаж без выставленного счета:** Сергей Климов, 6 часов, 1200 долларов США, *Оплачивается*</li><li>**Фактическое значение продаж без выставленного счета:** Сергей Климов, 2 часов, 400 долларов США, *Не оплачивается*</li></ul><p>Новые фактические значения, созданные для реверсирования обновленной незавершенной работы продаж:</p><ul><li>**Фактическое значение продаж без выставленного счета:** Сергей Климов, 6 часов, 1200 долларов США, *Оплачивается*</li><li>**Фактическое значение продаж без выставленного счета:** Сергей Климов, 2 часов, 400 долларов США, *Не оплачивается*</li></ul><p>Новые фактические значения, созданные для учета значений продаж с выставленным счетом:</p><ul><li>**Фактическое значение продаж с выставленным счетом:** Сергей Климов, 6 часов, 1200 долларов США, *Оплачивается*</li><li>**Фактическое значение продаж с выставленным счетом:** Сергей Климов, 2 часов, 400 долларов США, *Не оплачивается*</li></ul> |
| Счет подтверждается после того, как количество в сведениях строки счета увеличивается относительно количества в фактическом значении продаж без выставленного счета. | Неприменимо | <p>Состояние корректировки исходных фактических значений продаж без выставленного счета меняется на **Скорректировано**.</p><p>Для исходных фактических значений продаж без выставленного счета создаются сторнирующие фактические значения продаж без выставленного счета. Для них устаналивается состояние корректировки **Не регулируется**.</p><p>Создаются новые фактические значения продаж без выставленного счета для нового количества.</p><p>Для новых фактических значений продаж без выставленного счета создаются сторнирующие фактические значения продаж без выставленного счета.</p> | Создаются фактические значения продаж с выставленным счетом для нового количества. | <p>Существующее фактическое значение, которое остается неизменным:</p><ul><li>**Фактическая стоимость:** Сергей Климов, 8 часов, 800 долларов США</li></ul><p>Обновленное существующее фактическое значение:</p><ul><li>**Фактическое значение продаж без выставленного счета:** Сергей Климов, 8 часов, 1600 долларов США, *Скорректировано*</li></ul><p>Новое фактическое значение, созданное для сторнирования ранее отраженной финансовой незавершенной работы:</p><ul><li>**Фактическое значение продаж без выставленного счета:** Сергей Климов, 8 часов, 1600 долларов США, *Не регулируется*</li></ul><p>Новое фактическое значение, созданное для учета обновленной незавершенной работы продаж:</p><ul><li>**Фактическое значение продаж без выставленного счета:** Сергей Климов, 10 часов, 2000 долларов США, *Оплачивается*</li></ul><p>Новое фактическое значение, созданное для сторнирования обновленной незавершенной работы продаж:</p><ul><li>**Фактическое значение продаж без выставленного счета:** Сергей Климов, 10 часов, 2000 долларов США, *Не оплачивается*, *Не регулируется*</li></ul><p>Новое фактическое значение, созданное для учета значений продаж с выставленным счетом:</p><ul><li>**Фактическое значение продаж с выставленным счетом:** Сергей Климов, 10 часов, 2000 долларов США, *Оплачивается*</li></ul> |
| В счет вносится исправление для уменьшения подлежащего оплате количества или цены. | Неприменимо | <p>Создается два фактических значения продаж без выставленного счета:</p><ul><li>Подлежащее оплате фактическое значение продаж без выставленного счета для количества в корректирующем счете</li><li>Подлежащее оплате фактическое значение продаж без выставленного счета для оставшегося количества</li></ul><p>Для двух новых фактических значений продаж без выставленного счета создаются сторнирующие фактические значения продаж без выставленного счета.</p> | <p>Создаются сторнирующие фактических значения продаж с выставленным счетом.</p><p>Создаются новые фактические значения продаж с выставленным счетом для нового количества. | <p>Существующие фактические значения, которые остаются неизменными:</p><ul><li>**Фактическая стоимость:** Сергей Климов, 8 часов, 800 долларов США</li><li>**Фактическое значение продаж без выставленного счета:** Сергей Климов, 8 часов, 1600 долларов США, *Счет клиента разнесен*</li><li>**Фактическое значение продаж без выставленного счета:** Сергей Климов, 8 часов, 1600 долларов США</li></ul><p>Обновленное существующее фактическое значение:</p><ul><li>**Фактическое значение продаж с выставленным счетом:** Сергей Климов, 8 часов, 1600 долларов США, *Скорректировано*</li></ul><p>Новое фактическое значение, созданное для сторнирования ранее отраженных значений продаж с выставленным счетом:</p><ul><li>**Фактическое значение продаж с выставленным счетом:** Сергей Климов, 8 часов, 1600 долларов США, *Не регулируется*</li></ul><p>Новые фактические значения, созданные для учета исправленной незавершенной работы продаж:</p><ul><li>**Фактическое значение продаж без выставленного счета:** Сергей Климов, 6 часов, 1200 долларов США, *Оплачивается*, *Счет клиента разнесен*</li><li>**Фактическое значение продаж без выставленного счета:** Сергей Климов, 2 часов, 400 долларов США, *Оплачивается*</li></ul><p>Новое фактическое значение, созданное для сторнирования исправленной незавершенной работы продаж:</p><ul><li>**Фактическое значение продаж без выставленного счета:** Сергей Климов, 6 часов, 1200 долларов США, *Не оплачивается*, *Не регулируется*</li></ul><p>Новое фактическое значение, созданное для учета исправленных значений продаж с выставленным счетом:</p><ul><li>**Фактическое значение продаж с выставленным счетом:** Сергей Климов, 6 часов, 1200 долларов США, *Оплачивается*</li></ul> |
| В счет вносится исправление для увеличения подлежащего оплате количества или цены. | Неприменимо | <p>Создаются новые фактические значения продаж без выставленного счета для нового количества.</p> <p>Для новых фактических значений продаж без выставленного счета создаются сторнирующие фактические значения продаж без выставленного счета.</p> | <p>Создаются сторнирующие фактических значения продаж с выставленным счетом.</p>Создаются новые фактические значения продаж с выставленным счетом для нового количества.</p> | <p>Существующие фактические значения, которые остаются неизменными:</p><ul><li>**Фактическая стоимость:** Сергей Климов, 8 часов, 800 долларов США</li><li>**Фактическое значение продаж без выставленного счета:** Сергей Климов, 8 часов, 1600 долларов США, *Счет клиента разнесен*</li><li>**Фактическое значение продаж без выставленного счета:** Сергей Климов, 8 часов, 1600 долларов США</li></ul><p>Обновленное существующее фактическое значение:</p><ul><li>**Фактическое значение продаж с выставленным счетом:** Сергей Климов, 8 часов, 1600 долларов США, *Скорректировано*</li></ul><p>Новое фактическое значение, созданное для сторнирования ранее отраженных значений продаж с выставленным счетом:</p><ul><li>**Фактическое значение продаж с выставленным счетом:** Сергей Климов, 8 часов, 1600 долларов США, *Не регулируется*</li></ul><p>Новое фактическое значение, созданное для учета исправленной незавершенной работы продаж:</p><ul><li>**Фактическое значение продаж без выставленного счета:** Сергей Климов, 10 часов, 2000 долларов США, *Оплачивается*, *Счет клиента разнесен*</li></ul><p>Новое фактическое значение, созданное для сторнирования исправленной незавершенной работы продаж:</p><ul><li>**Фактическое значение продаж без выставленного счета:** Сергей Климов, 10 часов, 2000 долларов США, *Оплачивается*</li></ul><p>Новое фактическое значение, созданное для учета исправленных значений продаж с выставленным счетом:</p><ul><li>**Фактическое значение продаж с выставленным счетом:** Сергей Климов, 10 часов, 2000 долларов США, *Оплачивается*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]