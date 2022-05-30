---
title: Изменения управления ресурсами (Project Service Automation 3.x)
description: В этом разделе представлена информация об изменениях в области управления ресурсами.
author: makk
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: d19b8b453c544bb4c6fd11a8b9f750cb08e0c168
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595514"
---
# <a name="resource-management-changes-project-service-automation-3x"></a>Изменения управления ресурсами (Project Service Automation 3.x)

[!include [banner](../../includes/psa-now-project-operations.md)]

Разделы этой темы содержат сведения об изменениях, которые были сделаны в области управления ресурсами Dynamics 365 Project Service Automation версии 3.x.

## <a name="project-estimates"></a>Оценки проекта

Вместо сущности **msdyn\_projecttask** (**Задача проекта**), оценки проекта основаны на сущности **msdyn\_resourceassignment** (**Назначение ресурса**). Назначения ресурсов стали "источником истины" для планирования и цен задач.

## <a name="line-tasks"></a>Задачи строки

В PSA 3.x задачи строки устарели (нерекомендуемый). Назначения теперь указывают на всю задачу, а не на задачи строки.

Следующий пример показывает, как задача с названием "Тестовая задача" назначается участникам рабочей группы A и B в предыдущих версиях PSA и в PSA 3.x.

- **До PSA 3.x:**

    - Тестовая задача

        - Тестовая задача — задача строки 1

            - Назначение A

        - Тестовая задача — задача строки 2

            - Назначение B

- **PSA 3.x:**

    - Тестовая задача

        - Назначение A
        - Назначение B

## <a name="unassigned-assignment"></a>Неназначенное назначение

В PSA 3.x неназначенное назначение — это назначение, которое назначено участнику рабочей группы **NULL** и ресурсу **NULL**. Неназначенные назначения могут возникать в паре случаев:

- Если задача была создано, но пока еще не была назначена какому-либо участнику рабочей группы, неназначенное назначение всегда создается. 
- Если все назначенные для задачи будут удалены, то неназначенное назначение снова создается для этой задачи.

## <a name="scheduling-fields-on-the-project-task-entity"></a>Поля планирования в сущности задачи проекта

Поля в сущности **msdyn\_projecttask** стали нерекомендуемыми или были перемещены в сущность **msdyn\_resourceassignment**, или на них теперь имеются ссылки из сущности **msdyn\_projectteam** (**Участник проектной группы**).

| Нерекомендуемое поле в msdyn\_projecttask (Задача проекта) | Новое поле в msdyn\_resourceassignment (Назначение ресурса) | Комментарии |
|---|---|---|
| msdyn\_assignedresources | Нет | |
| msdyn\_assignedteammembers | Нет | |
| msdyn\_numberofresources | Нет | |
| msdyn\_scheduledhours | Нет | |
| msdyn\_effortcontour | msdyn\_plannedwork | Был изменен формат структуры данных нотации объектов JavaScript (JSON), которая хранится в поле. |

## <a name="schedule-contour"></a>Контур расписания

Контур расписания хранится в поле **Запланированная работа** (**msdyn\_plannedwork**) каждой сущности **Resource Assignment** (**msdyn\_resourceassignment**).

### <a name="structure"></a>Структура

Новая структура контура расписания состоит из гибких слоев времени, которые определяются для каждого дня расписания. Каждый слой времени имеет следующие свойства:

- **Начало** — время начала рабочих часов на определенный день по календарю проекта.
- **Конец** — время окончания рабочих часов на определенный день по календарю проекта.
- **Часы** — число часов, которые назначены на день.

**Пример**

В этом примере используется календарь проекта, где рабочий день занимает время с 9 утра до 5 вечера в часовом поясе UTC-8.

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a>Автоматическое и ручное планирование

Если задача автоматически запланирована, часы загружаются сначала, а длительность задачи может быть уменьшена.

**Пример**

Следующая задача автоматической запланирована на 18 часов за 3 дня (с 3-го декабря 2018 по 5-е декабря 2018).

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

Если задача запланирована вручную, часы распределяются равномерно по всем датам.

**Пример**

Следующая задача вручную запланирована на 18 часов за 3 дня (с 3-го декабря 2018 по 5-е декабря 2018).

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a>Единица назначение

Единица назначения устарела в PSA 3.x. Часы усилий по задаче теперь поровну делятся на дни среди всех назначенных ресурсов.

**Пример**

В этом примере задача назначена двум ресурсам и автоматически запланирована на 36 часов за 3 дня (с 3-го декабря 2018 по 5-е декабря 2018).

- Назначение 1:

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- Назначение 2:

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a>Измерения цен

В PSA 3.x специфичные для ресурсов поля измерения цен (такие как **Роль** и **Подразделение**) были удалены из сущности **msdyn\_projecttask**. Эти поля теперь можно извлечь из соответствующего участника рабочей группы проекта (**msdyn\_projectteam**) назначения ресурса (**msdyn\_resourceassignment**) при создании оценок проекта. Новое поле **msdyn\_organizationalunit** было добавлено в сущность **msdyn\_projectteam**.

| Нерекомендуемое поле в msdyn\_projecttask (Задача проекта) | Поле из msdyn\_projectteam (Участник проектной группы), которое используется взамен |
|---|---|
| msdyn\_resourcecategory | msdyn\_resourcecategory |
| msdyn\_organizationalunit | msdyn\_organizationalunit |

## <a name="contours"></a>Контуры

Поле цен и контуров оценки устарели в сущности **msdyn\_projecttask**. Они удалены из сущности **msdyn\_resourceassignment**.

| Нерекомендуемое поле в msdyn\_projecttask (Задача проекта) | Новое поле в msdyn\_resourceassignment (Назначение ресурса) |
|---|---|
| msdyn\_costestimatecontour | msdyn\_plannedcostcontour |
| msdyn\_salesestimatecontour | msdyn\_plannedsalescontour |

Следующие поля добавлены в сущность **msdyn\_resourceassignment**:

* msdyn\_plannedcost
* msdyn\_plannedsales

Следующие поля для плановой, фактической и оставшейся стоимости и продажам не изменились в сущности **msdyn\_projecttask**:

* msdyn\_plannedcost
* msdyn\_plannedsales
* msdyn\_actualcost
* msdyn\_actualsales
* msdyn\_remainingcost
* msdyn\_remainingsales


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
