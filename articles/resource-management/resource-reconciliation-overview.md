---
title: Обзор выверки ресурсов
description: В этом разделе приводятся сведения об обеспечении согласования резервирования ресурсов и назначения проектам.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1b60ed9d15f51ff01f27bcc231f5db27513a838f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897467"
---
# <a name="resource-reconciliation-overview"></a>Обзор выверки ресурсов

_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_

Для участников рабочей группы резервирования и назначения свободно связаны между собой. Другими словами, ресурсы могут иметь назначения без резервирований, или могут иметь резервирования без назначений. В идеальном случае, назначения и резервирования должны соответствовать друг другу, чтобы ресурсы имели выделенные мощности для выполнения назначенных задач. Тем не менее резервирования могут быть основаны на доступности, а значения времени выполнения задач могут измениться по мере развития проекта. Следовательно, мягкие связи резервирований и назначений предоставляют гибкость.

Вкладка **Сверка** в форме **Проект** позволяет руководителям проекта сверить резервирования участников рабочей группы и их назначения для проектных групп.

Вкладка **Сверка** также отображает резервирования и назначения вплоть до уровня индивидуального назначения задачи для каждого участника рабочей группы. Часы отображаются в ячейках, отражающих периоды времени от месяцев и вниз до дней.

Вкладка также отображает общий нетто итог для проекта, вместе со столбцом **Итого**.

Для каждого из ресурсов вкладка вычислит различие между резервированиями участника рабочей группы и сверткой назначений задач участников рабочей группы. В идеальном случае это различие должно быть равно 0 (нулю). Другими словами, не должно быть разницы между резервированиями и назначениями. Различия окрашены и затенены, чтобы нарисовать два условия:

- **Недорезервирование** — недостаток резервирования возникает, когда ресурс имеет больше назначений, чем резервирований. Поскольку вся его производительность не была зарезервирована, руководитель проекта может захотеть исправить это состояние, расширив резервирования, чтобы дефицит охватывать.
- **Перерезервирование** — избыточные резервирования происходящих, когда ресурс зарезервирован на проект, но ему не назначены задачи. Это условие может быть допустимо в случаях, когда ресурс был зарезервирован для проекта до того, как было выполнено назначение задачи. Тем не менее, в других случаях ресурс не запланирован для назначения задачам. В таких случаях руководитель проекта должен рассмотреть отмену резервирования ресурса, чтобы его производительность могла быть использована для другого проекта.

В некоторых случаях, когда вы просматриваете время на более высоком уровне, чем уровень дня (например, уровень месяца), вы можете видеть нулевое чистое различие для ресурса (иначе говоря, резервирования = назначения). Однако при просмотре времени на уровне недели вы можете увидеть ноль часов назначения и 40 часов резервирования для первой недели, но 40 часов назначений и ноль часов резервирования для второй недели. В целом резервирования и назначения выверены, однако они отличаются от одной недели до следующей.

При просмотре времени на высоких уровнях ячейки на вкладке **Сверка** имеют индикатор, чтобы информировать о различиях на более низких уровнях. Дважды щелкнув в ячейке, можно увеличить ее для просмотра различия. Можно затем щелкнуть правой кнопкой мыши, чтобы уменьшить ее. Выбрав ресурс, затем используя элемент управления **Следующая разница** на панели инструментов сетки, можно перейти к следующему различию между резервированиями и назначениями для данного ресурса. Затем можно использовать элемент управления **Предыдущая разница** для перехода назад. Можно также отключить индикатор различия и поведение перехода в разделе **Параметры**.


Если имеются назначения для ресурса, но нет резервирований, на странице **Проекты** на вкладке **Сверка** выберите недостаток резервирований, затем выберите **Продлить резервирование**. Открывается диалоговое окно **Продлить резервирование**, в котором отображается резервирование, необходимое для исправления недостатка ресурсов. Оно также показывает существующие резервирования ресурса по всем проекты или другим планируемым объектам. Если вы выбираете **ОК** для создания резервирования для этого ресурса, независимо от доступности ресурса, это может привести к избыточному резервированию.

Руководитель проекта и руководитель по ресурсам затем могут использовать доску расписания для управления всеми ситуациями, где ресурс излишне зарезервирован с превышением его производительности.
