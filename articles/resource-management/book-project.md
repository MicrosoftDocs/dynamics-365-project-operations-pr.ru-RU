---
title: Резервирование для проекта
description: В этом разделе представлена информация о резервировании ресурса для проекта.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 19128264ed3db7efeeba948155f0ddbdc806c2a0
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908525"
---
# <a name="book-to-a-project"></a>Резервирование для проекта

_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_

Бывают случаи, когда менеджеру проекта или менеджеру ресурсов нужно будет выделить ресурс для проекта без определенных требований, определяемых универсальным участником рабочей группы. Это можно достигнуть одним из трех способов.

- Резервирование из сетки участников рабочих групп
- Резервирование с доски расписания
- Резервирование из формы **Проект**

## <a name="book-from-the-team-member-grid"></a>Резервирование из сетки участников рабочих групп

Если ваша организация работает в гибридном режиме распределения ресурсов, менеджер проекта может зарезервировать ресурс непосредственно для проекта, выполнив следующие шаги.

1. В проекте перейдите к сетке участников рабочей группы и выберите **Создать**.
2. Определите название должности и роль ресурса.
3. Выберите доступный для резервирования ресурс из доступной подстановки.
4. После выбора ресурса определите следующую информацию в полях для резервирования ресурса:

    - Дата начала
    - Дата окончания
    - Метод выделения
    - Часы, если применимо
    - Утверждающий проекта

6. Выберите **Сохранить и закрыть**

## <a name="book-from-the-schedule-board"></a>Резервирование с доски расписания

Когда менеджеру ресурсов необходимо зарезервировать ресурс непосредственно для проекта, он может использовать доску расписания и требования проекта. Требование проекта — это требование ресурса, которое всегда доступно для резервирования по нему. Чтобы зарезервировать напрямую для проекта из доски расписания, выполните следующие шаги.

1. Перейдите к доске расписания и на левой странице отфильтруйте ресурсы, которые вы рассматриваете для требования.
2. На нижней панели выберите вкладку **Проект**, чтобы просмотреть список требований проекта.
3. Перетащите требование на ресурс и укажите следующую информацию:

    - Дата начала
    - Дата окончания
    - Состояние резервирования
    - Метод резервирования
    - Продолжительность

## <a name="book-from-the-project-form"></a>Резервирование из формы "Проект"

Как менеджеру проекта, вам может потребоваться зарезервировать ресурс для проекта, но вы знаете только критерии, а не название ресурса. Выполните следующие шаги, чтобы использовать помощник по расписанию для поиска ресурса на основе любых доступных атрибутов ресурса. 

1. Перейдите к проекту и выберите **Резервировать**, чтобы открыть помощник по расписанию.
2. Используя фильтры в левой части помощника по расписанию, уточните критерии и выберите **Поиск**.
3. На основе ресурсов, возвращенных в результатах, вы можете зарезервировать ресурс.

> [!NOTE]
> Этот метод не создает никаких резервирований для ресурса. Вместо этого он добавляет ресурс в рабочую группу. После того как участник рабочей группы был добавлен в проект, менеджер проекта может использовать ведение резервирований или продление резервирований, чтобы добавить необходимые резервирования к ресурсу.