---
title: Производительность планирования ресурсов проекта
description: Эта тема предоставляет информацию о том, как повысить производительность планирования ресурсов для большого количества проектов.
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: c3f219ce0635545976a6a4639233f166e18468af
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083171"
---
# <a name="project-resource-scheduling-performance"></a>Производительность планирования ресурсов проекта

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


Проблемы с производительностью, связанные с планированием ресурсов, могут возникнуть, когда количество проектов достигает тысяч. Для повышения производительности планирования ресурсов доступна функция, позволяющая пользователям сократить время, необходимое для запуска формы доступности ресурсов. В частности, это удаляет процесс синхронизации свертки емкости ресурсов и использует таблицу **ResProjectResource** для ускорения поиска ресурсов. Обратите внимание, что таблица **ResRollup** больше не будет использоваться.

> [!IMPORTANT]
> Если есть зависимость от процесса синхронизации свертки емкости ресурсов или от таблицы **ResProjectResource** , не используйте эту функцию.

## <a name="enable-resource-scheduling-performance-enhancement"></a>Включение повышения производительности планирования ресурсов
Чтобы включить повышение производительности планирования ресурсов, выполните следующие действия.

1. Перейдите в раздел **Управление функциями** > **Все** и в списке функций найдите **Включить функцию повышения производительности планирования ресурсов проектов**.
2. Выберите **Включить сейчас**.

> [!NOTE]
> Если вы не можете найти функцию в списке, выберите **Проверить наличие обновлений** , чтобы обновить список.

3. Обновите браузер, затем перейдите в раздел **Управление и учет по проектам** > **Периодические задачи** > **Ресурсы проектов** > **Синхронизация емкости календарей ресурсов во всех компаниях**.
4. Установите для параметра **Удалить существующие записи о емкости** значение **Да** , чтобы удалить предыдущие данные. Если вы хотите генерировать инкрементные данные, установите для него значение **Нет**.
5. В поле **Код периода** выберите период, за который должны быть созданы данные. Если вы выбираете код периода, дату начала и окончания определять не нужно.
6. Если вы оставите поле **Код периода** пустым, выберите конкретные даты начала и окончания для генерации данных.
7. Нажмите **ОК**.

 > [!NOTE]
 > Это распределит общие данные в таблицу **ResCalendarCapacity** для всех компаний в вашей среде, поэтому пакетное задание нужно запускать только в одном юридическом лице. Данные в этом пакетном задании необходимы для расчета емкости ресурсов с помощью связанного календаря.

8. Перейдите в раздел **Управление и учет по проектам** > **Периодические задачи** > **Ресурсы проектов** > **Заполнить ресурсы проектов во всех компаниях** , затем выберите **ОК**. Это сценарий обновления данных для общих данных в таблицах **ResProjectResource** , **ResCalendarDateTimeRange** и **ResEffectiveDateTimeRange**. Значения для полей **PSAPRojSchedRole.RootActivity** также обновляются. Если это не будет выполнено, вы получите предупреждение при попытке выполнить операции планирования ресурсов.
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a>Выключение повышения производительности планирования ресурсов

1. Перейдите в раздел **Управление функциями** > **Все** и найдите **Включить функцию повышения производительности планирования ресурсов проектов**.
2. Выберите функцию, затем выберите кнопку **Отключить**.
3. Обновите свой браузер.
4. Перейдите в раздел **Управление и учет по проектам** > **Периодические задачи** > **Синхронизация загрузки** > **Синхронизация операций сведения загрузки ресурсов**.
5. На странице **Синхронизация сведения мощности** задайте для параметра **Удалить существующие записи мощности** значение **Да** , чтобы удалить предыдущие данные. Если вы хотите генерировать инкрементные данные, установите для него значение **Нет**.
6. В поле **Код периода** выберите период, за который должны быть созданы данные. Если вы выбираете код периода, дату начала и окончания определять не нужно.
7. Если вы оставите поле **Код периода** пустым, выберите конкретные даты начала и окончания для генерации данных.
8. Нажмите **ОК**.

> [!NOTE]
> Это распределит общие данные в таблицу **ResRollup** для всех компаний в вашей среде, поэтому пакетное задание нужно запускать только в одном юридическом лице. Это пакетное задание необходимо для всех представлений **Доступность ресурсов**. Если это пакетное задание не запущено, данные **ResRollup** будут генерироваться "на лету", что может занять время.