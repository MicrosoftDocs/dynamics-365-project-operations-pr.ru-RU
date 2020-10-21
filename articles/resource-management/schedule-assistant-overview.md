---
title: Обзор помощника по расписанию
description: Эта тема предоставляет информацию о работе с помощником по расписанию для резервирования ресурсов.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: da551e805f395e466952df1dbb7d193bdddba358
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908508"
---
# <a name="schedule-assistant-overview"></a>Обзор помощника по расписанию

_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_

Помощник по расписанию используется для резервирования ресурсов на основе требований, определенных менеджером проекта. Помощник по расписанию использует параметры, указанные в требовании к ресурсу, чтобы найти ресурс. Помощник по расписанию рекомендует ресурсы, соответствующие соответствующим требованиям, например временным окнам или необходимым навыкам.

После того, как подходящие ресурсы определены, менеджер ресурсов или проекта может зарезервировать ресурс для работы.

## <a name="prerequisites"></a>Предварительные условия

Помощник по расписанию является частью решения Universal Resource Scheduling. Это решение поставляется и устанавливается вместе с Dynamics 365 Project Operations, Dynamics 365 Field Service и Dynamics 365 Customer Service.

## <a name="matching-requirements-and-resources"></a>Сопоставление требований и ресурсов

Сгенерированная потребность в ресурсах основана на таких деталях, как:

-   Характеристики
-   Роли
-   Бизнес-единицы
-   Предпочтения ресурсов
-   Контуры усилий
-   Часовой пояс

Помощник по расписанию использует эти данные для фильтрации ресурсов.

## <a name="launch-the-schedule-assistant"></a>Запуск помощника по расписанию

Помощник по расписанию можно запустить двумя способами. Если вы используете гибридный режим, в сетке участников рабочей группы вы можете выбрать любого участника рабочей группы с невыполненными требованиями к ресурсам, затем выбрать **Зарезервировать**. Если вы используете центральный режим, диспетчер ресурсов находит и выбирает ресурс.

## <a name="schedule-assistant-filters"></a>Фильтры помощника по расписанию

После выполнения помощника по расписанию сведения о требованиях к ресурсам отображаются в виде отфильтрованных значений на левой панели. Менеджер ресурсов или менеджер проекта может точно настроить результаты, настроив фильтры в соответствии с потребностями планирования.

На панели фильтров отображаются параметры, связанные с работой, в том числе:

-   Начало и окончание работы
-   Характеристики
-   Роли
-   Подразделения
-   Компания распределения ресурсов
-   Типы ресурсов
-   Предпочитаемые ресурсы