---
title: Создание записей времени
description: В этом разделе представлена информация о том, как создать записи времени.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
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
ms.openlocfilehash: 878413a24baa340b745a045a6991a63a00851c8b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083279"
---
# <a name="create-time-entries"></a>Создание записей времени

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

В предыдущих версиях Dynamics 365 Project Service Automation, записи времени вводились еженедельно. В версии 3 Project Service Automation записи времени вводятся ежедневно. Однако после создания нескольких записей времени их можно массово создавать или копировать.

## <a name="create-a-time-entry"></a>Создание записи времени

Выполните следующие действия, чтобы создать запись времени.

1. На странице **Записи времени** выберите **Создать**.
2. В диалоговом окне **Быстрое создание: Запись времени** введите длительность записи времени в минутах, часах или днях. Длительность следует вводить в следующем формате: *x* мин, *x* ч или *x* дней. Часы и дни также можно вводить как десятичные числа, например *x,x* ч или *x,x* дней.
3. Выберите тип записи времени и проект, для которого вы входите запись времени.
4. В поле **Задача проекта** найдите задачу для этой записи времени.

    > [!NOTE]
    > Если вы создаете запись времени для задачи, которая не назначена пользователю, в поле **Задача проекта** выберите кнопку **Поиск** , выберите **Изменить представление** , затем выберите **Все активные задачи проекта** для отображения списка всех задач.

5. Введите описание, если описание является обязательным, затем выберите **Сохранить и закрыть**.

После создания и сохранения записи времени можно изменить ее в сетке записей времени. Сетка записи времени поддерживает два формата:

- Можно ввести записи времени в формате **чч:мм**. Этот формат затем преобразуется в часы и доли часов.
- Можно вводить часы и доли часов напрямую.

Обратите внимание, что дробные доли часа — это не минуты. Следовательно, 1,5 часа представляют 1 час и 30 минут. Это же правило применяется с дробным частям дня. Один день состоит из 24 часов, и 0,5 дня представляют 12 часов.

## <a name="bulk-create-time-entries"></a>Массовое создание записей времени

После создания нескольких записей времени можно скопировать их для массового создания дополнительных записей времени.

1. На странице **Записи времени** выберите **Копировать неделю**.
2. В группе полей **Из периода** в полях **Дата начала** и **Дата окончания** определите диапазон дат, из которого требуется скопировать записи времени.
3. В группе полей **В период** в поле **Дата начала** укажите дату, для которой требуется создать записи времени.
4. Выберите **Копировать** , чтобы создать копии записей времени, соответствующих дню недели, указанному в группе полей **В период**. Например, запись времени для понедельника на прошлой неделе копируется в понедельник недели, которая указана в группе полей **В период**.

## <a name="import-data-for-time-entries"></a>Импорт данных для записей времени

Можно импортировать данные из резервирований и назначений проекта. При импорте данных можно указать диапазон дат резервирований для импорта, затем явно выбрать резервирования, которые должны быть созданы как записи времени **Черновик**.

## <a name="group-by-sort-search-and-filter-capabilities"></a>Возможности группировки, сортировки, поиска и фильтрации

Можно группировать и фильтровать записи времени по измерениям, которые определены в столбцах. В поле **Группировать по** выберите измерение, которое следует использовать для фильтрации записей времени. Также можно сортировать записи ввода времени в восходящем или нисходящем порядке с помощью стрелок сортировки в заголовках столбцов. Кроме этого, можно отображать или скрывать записи, выбирая кнопку **Фильтр** в заголовках столбцов, затем, в поле **Поиск** вводя текст, который должен использоваться для поиска записей времени по имени проекта, задаче проекта, записи времени или ресурсу.