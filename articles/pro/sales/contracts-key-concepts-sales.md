---
title: Основные понятия контрактов по проектам
description: В этом разделе представлена информация об основных понятиях контрактов по проекту.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 66d6b72b19a90ecc9161cd16ce9d4dd22798803b
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083094"
---
# <a name="key-concepts-of-project-contracts"></a>Основные понятия контрактов по проектам

_**Относится к:** развертывание Lite — от сделки до счетов-проформ_

В этой теме рассматриваются основные понятия, которые необходимо знать, прежде чем использовать контракты по проектам в Dynamics 365 Project Operations:

## <a name="contracting-unit"></a>Единица по контракту

Подрядная единица представляет собой подразделение или практику, которой принадлежит реализация проекта. Вы можете настроить затраты на ресурсы для каждой контрактной единицы. Когда вы указываете стоимость ресурса для ресурса, вы также можете установить разные ставки стоимости для ресурсов. Подрядная единица заимствует эти ресурсы у других подразделений или практик внутри предприятия. Ставки себестоимости ресурсов называются трансфертными ценами, заимствованием ресурсов или ценами обмена. Когда вы настраиваете ставки себестоимости для заимствования ресурсов из других подразделений, используйте валюту подразделения, из которого заимствуются ресурсы.

## <a name="cost-currency"></a>Валюта затрат

Валюта затрат в Project Operations — это валюта, в которой указываются затраты на экране. Эта валюта выводится из валюты, прикрепленной к полю **Единица по контракту** для контракта и проекта. Затраты могут регистрироваться в любой валюте по проекту. Однако существует конвертация валюты из валюты, в которой были учтены затраты, в валюту затрат по проекту при отображении на экране.

Поскольку обменные курсы на платформе Common Data Service (CDS) не могут быть актуальными по дате, итоговые суммы затрат на экране могут со временем измениться, если вы обновите курсы обмена валют. Однако затраты, записанные в базе данных, остаются неизменными, поскольку суммы хранятся в той валюте, в которой они были понесены.

## <a name="sales-currency"></a>Валюта продаж

Валюта продаж в Project Operations — это валюта, в которой записываются и отображаются оценочные и фактические суммы продаж. Валюта продаж — это также валюта, в которой клиенту выставляется счет за сделку. В контракте по проекту валюта продаж по умолчанию берется из записи клиента или учетной записи и может быть изменена при создании контракта. Когда контракт создается путем закрытия предложения с расценками как выигранного, валюта контракта устанавливается по умолчанию из валюты предложения с расценками.

Когда вы создаете контракт по проекту с нуля, поле **Валюта продаж** нельзя редактировать. Прайс-листы на продукты и проекты по умолчанию основаны на этой валюте в контракте.

В отличие от затрат, продажная стоимость может быть записана только в валюте продаж.

## <a name="billing-method"></a>Метод выставления счета

Для проектов обычно имеются два типа моделей контрактов, с фиксированной ценой и на основе потребления. Эти модели представлены в Project Operations как методы выставления счетов с двумя возможными значениями:

- Время и материал: модель контракта, основанная на потреблении, где все понесенные затраты подкрепляются соответствующей выручкой. По мере того, как вы оцениваете или несете дополнительные расходы, соответствующие оценочные и фактические продажи также увеличиваются. Укажите максимально допустимые ограничения для строк контракта, в которых используется этот метод выставления счетов, ограничивающие фактический доход. На расчетный доход не влияют ограничения, наложенные максимальными лимитами.
- Фиксированная цена: модель контракта с фиксированным вознаграждением, которая указывает, что стоимость продаж не будет зависеть от понесенных затрат. Стоимость продажи является фиксированной и не изменяется по мере того, как вы оцениваете или несете дополнительные расходы.

## <a name="project-price-lists"></a>Прайс-листы проектов

Прайс-листы проекта используются для цен по умолчанию, а не для ставок затрат, для времени, расходов и других компонентов, связанных с проектом. Прайс-листов может быть несколько. Каждый прайс-лист имеет свою дату вступления в силу для каждого контракта по проекту. Перекрывающиеся даты вступления в силу прайс-листов проекта не поддерживаются в Project Operations.

Когда контракт по проекту создается путем реализации предложения с расценками по проекту, прайс-листы проекта копируются с указанием названия и даты контракта. Копирование этой информации представляет собой индивидуальную цену для компонентов проекта в этом контракте по проекту.

## <a name="product-price-lists"></a>Прайс-листы продуктов

Прайс-листы продуктов используются для цен по умолчанию, а не для ставок затрат, для строк на основе продуктов в контракте. Для каждого контракта существует только один прайс-лист на продукты.

## <a name="transaction-classes"></a>Классы проводок

Project Operations поддерживает четыре типа классов транзакций:

- Время
- Расходы
- Материал
- Сбор

Себестоимость и продажная стоимость могут быть оценены и понесены по классам транзакций "Время", "Расходы" и "Материалы". Сбор — это класс транзакций, предназначенный только для получения дохода.

## <a name="work-entities-and-billing-entities"></a>Сущности работы и сущности выставления счетов

Сущности, которые представляют работу, — это проекты и задачи. Сущности, которые представляют выставление счетов, — это строки контракта. Вы можете связать различные сущности работы с вариантами выставления счетов, связав их со строками контракта.

## <a name="multi-customer-deals"></a>Сделки с несколькими клиентами

Сделки с несколькими клиентами содержат несколько клиентов , которым выставляются счета по сделке. Распространенные примеры:

- OEM-предприятия и их партнеры: партнеры и торговые посредники продают продукт с некоторыми дополнительными услугами, как правило, в рамках конкретной сделки с клиентом. OEM-предприятие предлагает профинансировать часть проекта. 

- Проекты государственного сектора: несколько департаментов местного правительства соглашаются финансировать проект, и им выставляются счета в соответствии с заранее согласованным разделением. Например, школьный округ и местное управление соглашаются финансировать строительство плавательного бассейна.

## <a name="invoice-schedules"></a>Расписания счетов

Графики выставления счетов специфичны для каждой строки контракта и необходимы для работы автоматического выставления счетов. Графики выставления счетов создаются на основе определенных дат начала и окончания, а также частоты выставления счетов. Эти графики используются на стадии контракта, когда настроен процесс автоматического создания счетов. Когда контракт по проекту создается из предложения с расценками, расписание выставления счетов копируется в контракт по проекту из предложения с расценками.

## <a name="changes-from-the-dynamics-365-sales-contract"></a>Изменения оп сравнению с контрактом Dynamics 365 Sales

Контракты Project Operations построены на основе контрактов Dynamics 365 Sales. Однако есть некоторые важные отклонения и различия в функциональности, о которых вам следует знать:

- Контракты Project Operations имеют два разных типа строк: одон для проектов, а другой для продуктов.
- Контракты Project Operations имеют свою собственную форму и элементы пользовательского интерфейса, бизнес-правила, бизнес-логику в надстройках и клиентские скрипты, которые делают их уникальными по сравнению с контрактами в Sales.

По этим причинам вы не должны использовать контракт Sales и контракт Project как взаимозаменяемые.