---
title: Создание назначений ресурсов
description: Эта тема предоставляет информацию о создании назначений универсальных и именованных ресурсов.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 20eb3880b17fb1f765ad79bd720520b0c8004c0a
ms.sourcegitcommit: a0f80d024a5d3112a39781815bd31d0c05ddaf6f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/30/2020
ms.locfileid: "3906301"
---
# <a name="create-resource-assignments"></a>Создание назначений ресурсов

_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_


Назначение ресурсов — это прямая связь участника проектной группы с задачей листового узла. В этой теме представлена информация о различных способах назначения ресурсов.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Создание универсального участника рабочей группы через назначение задач


Когда вы создаете универсального участника рабочей группы посредством назначения задачи, вы создаете заполнитель или универсальный ресурс. Этот универсальный ресурс описывает характеристики именованного ресурса, который должен в конечном счете работать на задачах. Затем создается требование или подается запрос с помощью этого требования, который используется для поиска и резервирования именованного ресурса.

1. В таблице расписания для задачи выберите значок ресурса в ячейке **Ресурс**.
2. Введите название, которое будет местозаполнителем для имени ресурса. Например, Руководитель программы.
3. Выберите **Создать** и в поле **Быстрое создание участника рабочей группы проекта** задайте роль для универсального ресурса.
4. Назначьте требуемые задачи этому ресурсу-местозаполнителю путем выбора ресурса в поле **Селектор ресурсов** для задачи. Ресурсы отображаются в разделе **Участники рабочей группы**.
5. Завершив назначение универсального ресурса, выберите этот универсальный ресурс на вкладке **Рабочая группа**, выберите этот универсальный ресурс, затем выберите **Создать требование**, чтобы создать требование ресурса для универсального ресурса.
6. Выберите **Резервировать** для универсального ресурса, после чего используйте доску расписания для поиска и резервирования реального ресурса. Можно также отправить требование для заполнения менеджером по ресурсам.
7. Когда универсальный ресурс полностью выполнен (частичное выполнение требований ресурсов не приведет к назначению ресурса) с именованным ресурсом, универсальный ресурс удаляется из рабочей группы. Назначения задач для универсального ресурса назначаются именованному ресурсу, который выполнил требования к ресурсам универсального ресурса.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Назначение именованного ресурса из списка всех резервируемых ресурсов

Окно поиска в области **Средство выбора ресурсов** можно использовать для поиска всех активных резервируемых ресурсов и назначения их любой задаче листового узла. Ресурсы, назначенные таким образом, добавляются в рабочую группу без всяких резервирований. Это подобно добавлению участников рабочей группы и выбору значения **Нет** в качестве способа распределения. Ресурс отображается на вкладках **Рабочая группа**, **Назначение ресурса** и **Выверка** как ресурсы только с назначениями и дефицитом резервирования. Зарезервируйте их, если требуется использовать их доступность.

1. Из сетки задач, доски или шкалы времени перейдите к ячейке **Кому назначено**.
2. В поле поиска начните вводить имя. Результаты поиска для имени отображаются в области **Селектор ресурсов** в разделе **Другие ресурсы**.
3. Выберите ресурс, который вы хотите назначить задаче, или выберите имя ресурса в разделе **Другие ресурсы рабочей группы**.
