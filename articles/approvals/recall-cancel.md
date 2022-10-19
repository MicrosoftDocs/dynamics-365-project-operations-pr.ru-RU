---
title: Отзыв ранее утвержденных записей
description: В этой статье поясняется, как участник проектной группы может запросить отзыв ранее отправленных и утвержденных записей о времени, расходах и использовании материалов, а также как руководитель проекта может утвердить или отклонить запросы на отзыв.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 54fc7ac2301a4423ebf70b0b67ad489580c347b5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930380"
---
# <a name="recall-previously-approved-entries"></a>Отзыв ранее утвержденных записей

_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_

Участник рабочей группы проекта, отправивший в систему запись времени, расходов или использования материалов, может отозвать эту запись послее ее утверждения. Процесс отзыва состоит из двух основных шагов:

1. Отправитель запрашивает отзыв.
2. Утверждающий утверждает запрос на отзыв.

## <a name="request-a-recall"></a>Запрос на отзыв

Чтобы запросить отзыв утвержденных записей времени, расходов или использования материалов, выполните следующие действия.

1. В зависимости от типа записи, которую требуется отозвать, выполните одно из следующих действий:

    - Для записей времени выберите **Проекты** \> **Моя работа** \> **Запись времени** и выберите все записи времени для определенного сочетания проекта и задачи. Альтернативно, в сетке выберите отдельные ячейки для времени в конкретный день для определенного проекта.
    - Для записей расходов выберите **Проекты** \> **Моя работа** \> **Расходы**, и выберите строку для записи расходов, которую требуется отозвать.
    - Для записей использования материалов выберите **Проекты** \> **Моя работа** \> **Журнал использования материалов**, и выберите строку для записи использования материалов, которую требуется отозвать.

2. Выберите **Отозвать**. Открывается диалоговое окно запроса подтверждения. Если выбранные записи времени, расходов или использования материалов уже утверждены, будет предложено ввести причину отзыва.
3. Введите причину отзыва, затем выберите **ОК**, чтобы подтвердить операцию. Система отправляет лицу, которое утвердило записи, запрос на утверждения отзыва.

> [!IMPORTANT]
> Невозможно создать запрос на отзыв утвержденной записи времени, расходов или использования материалов, по которой уже выставлен счет клиенту. При попытке это сделать вы получите сообщение о том, что запись времени, расходов или использования материалов невозможно отозвать, поскольку за них уже был выставлен счет. В этом случае вы можете запросить отзыв записи только в том случае, если был выставлен корректирующий счет для полного списания начислений или возврата средств, уплаченных клиентом по исходному счету.

## <a name="approve-or-reject-a-recall-request"></a>Утверждение или отклонение запроса на отзыв

Выполните следующие шаги, чтобы утвердить или отклонить запрос на отзыв.

1. Перейдите в раздел **Проекты** \> **Моя работа** \> **Утверждения**.
2. На странице списка **Утверждения** измените представление на **Запросы на отзыв для утверждения**. Отображается список отправленных запросов на отзыв.
3. Выберите одну или несколько записей, затем выберите **Утвердить** или **Отклонить**.
4. Если выбрано значение **Утвердить**, вы получите предупреждение, поясняющее последствия утверждения. Чтобы подтвердить операцию, выберите **ОК**. Запрос на отзыв утвержден.

    –или–

    Если выбрано **Отклонить**, запрос на отзыв отклоняется.

> [!IMPORTANT]
> При утверждении отзыва, как и при его запросе, система проверяет наличие каких-либо действий по выставлению счетов по записям времени, расходов или использования материалов. Если для записи уже выставлен счет или она включена в черновик счете, утверждающий получает сообщение об ошибке с сообщением о том, что время и расход нельзя утвердить для отзыва, поскольку за них уже был выставлен счет. В этом случае утверждающий может утвердить отзыв только в том случае, если был выставлен корректирующий счет для полного списания начислений или возврата средств, уплаченных клиентом по исходному счету.

## <a name="impact-of-a-recall-request"></a>Влияние запроса на отзыв

Когда утверждение отозвано, имеются операционные и финансовые последствия.

### <a name="operational-impact"></a>Операционные последствия

Если запрос на отзыв одобрен, запись утверждения отмечается как **Отклонено**. Состояние записи изменяется на **Возвращено** или **Отклонено**, в зависимости от того, какая это запись: запись времени, запись расходов или запись использования материалов.

Участник рабочей группы по проекту может просмотреть записи, изменить и снова отправить их либо полностью удалить записи.

Если запрос на отзыв отклонен, состояние записи остается **Утверждено**, и запись не может быть изменена участником проектной группы или утверждающим для проекта.

### <a name="financial-impact"></a>Финансовые последствия

Если запрос на отзыв утвержден, соответствующие фактические данные для стоимости и продаж обновляются следующим образом:

- Поле **Состояние корректировки** обновляется до **Скорректировано**.
- Поле **Состояние выставления счета** обновляется до **Отменено**.

Затем создаются записи реверсирования в таблице фактических данных. Для создания записей реверсирования система копирует значения полей из первоначальных фактических данных. Единственные значения, которые не будут скопированы, — это значения количества. Вместо этого эти значения обращаются. Обращенные фактические значения создаются для фактических значений **Стоимость** и **Продажи без выставления счета**. В поле **Состояние корректировки** для реверсированных фактических данных задается значение **Не регулируется**, а в поле **Состояние выставления счета** устанавливается значение **Отменено**. Из-за этих изменений записанная невыполненная работа по расходам и доходам по проекту перестанет учитывать суммы, которые представляют эти фактические данные.

Если запрос на отзыв отклонен, это не имеет финансовых последствий для проекта.

## <a name="changes-to-time-entry-records"></a>Изменения записей ввода времени

На следующей иллюстрации показаны изменения, которые происходят для утвержденных записей времени и соответствующих записей утверждения в случае их отзыва.

![Переходы статуса записи времени.](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-and-material-usage-entry-records"></a>Изменения в записях о расходах и использовании материалов

На следующей иллюстрации показаны изменения, которые происходят для утвержденных записей расходов и использования материалов и соответствующих записей утверждения в случае их отзыва.

![Переходы статуса записи расходов.](media/ExpenseEntryStateTransitions.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]