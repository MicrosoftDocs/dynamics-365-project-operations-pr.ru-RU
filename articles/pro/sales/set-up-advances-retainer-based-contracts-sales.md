---
title: Авансы и контракты с предоплатой
description: Эта тема предоставляет информацию о моделях контрактов на основе предоплаты и авансах в Project Operations.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5ccf8ff4fa52fa6ff9fe534dfbe6736afc24ffba
ms.sourcegitcommit: f8edff6422b82fdf2cea897faa6abb51e2c0c3c8
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/21/2020
ms.locfileid: "4088069"
---
# <a name="advances-and-retainer-based-contracts"></a>Авансы и контракты с предоплатой 


_**Относится к:** развертывание Lite — от сделки до счетов-проформ_

Dynamics 365 Project Operations поддерживает контракты на основе предоплаты. Контракт на основе предоплаты — это согласованный набор равномерно распределенных платежей, по которым заказчику будут выставляться счета на протяжении всего срока проекта. Этот тип контракта обычно используется для моделей выставления счетов на основе времени и материалов или потребления, когда необходимо предоставить клиенту предсказуемый график счетов и платежей. Фактическая выручка, начисленная за каждый период, сверяется с платежом, полученным от клиента в начале периода. В соответствии с концепцией модели выставления счетов за время и материалы, значения выручки, начисленные за каждый период, могут варьироваться в зависимости от понесенных затрат. Если накопленный доход превышает сумму, полученную в начале периода, компания, выполняющая проект, может:

- Выставить заказчику счет только за превышение 
- Отложить сверку выручки на следующий период выставления счетов и выставить один окончательный счет в конце проекта за оставшийся невыверенный доход

Основное различие между моделью контрактов на основе предоплаты и моделью контракта с фиксированной ценой в Project Operations заключается в том, что в модели контракта с фиксированной ценой сумма счета не связана и не привязана к понесенным затратам. Для выставления счетов используется подход, основанный на этапах, которые соответствует затратам, понесенным за этот период. В контракте на основе предоплаты выручка, по которой может быть выставлен счет, записывается на основе метода выставления счетов в строке контракта. Когда методом выставления счетов является время и материалы, выручка, на которую можно выставить счета, привязана к затратам, понесенным в любой данный период, и может варьироваться от периода к периоду. Однако клиенту выставляется счет только на сумму периодической предоплаты. Система использует другой счет в конце периода для сверки выручки, подлежащей оплате, зарегистрированной в течение периода, с суммой, на которую клиенту был выставлен счет в начале периода.

Преимущество этого метода заключается в том, что затраты клиента становятся предсказуемыми в графике предоплаты, в отличие от типичной модели времени и материалов. У организации, реализующей проект, также есть некоторое пространство для покрытия риска возмещения затрат, понесенных из-за любого увеличения объема, чего не позволила бы им модель с фиксированной ценой.

В дополнение к периодическому расписанию, основанному на предоплате, Project Operations может записывать единовременный аванс от клиента и согласовывать его с различными компонентами стоимости проекта.

Предоплата в Project Operations не доступна для использования, пока клиенту не выставлен на нее счет. На это указывают следующие поля во вложенной сетке авансов и предоплаты.

| Поле | Релевантность, цель и руководство | Воздействие на последующие элементы |
| --- | --- | --- |
| Доступная сумма | Сумма, которая может быть использована по записи предоплаты или аванса. | Пока на аванс или предоплату не выставлен на счет, ее нельзя использовать, что означает, что доступная сумма будет равна нулю. |
| Использованная сумма | Сумма, которая уже использована из предоплаты или аванса. | Аванс или предоплата могут быть частично выверены в счете с фактическими затратами, при этом некоторая часть будет помечена как уже использованная или израсходованная. Оставшаяся сумма аванса или предоплаты доступна для сверки в будущем счете с фактическими затратами. |