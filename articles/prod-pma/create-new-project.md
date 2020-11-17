---
title: Создание проекта
description: В этом разделе представлена информация о том, как создать новый проект.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 727d287c571b2a64bf10b2393a87567093a420d2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083323"
---
# <a name="create-a-new-project"></a>Создание проекта

[!include [banner](../includes/banner.md)]

Чтобы создать новый проект, выполните указанные ниже шаги.

1. На странице **Управление проектом** выберите **Создать проект** и введите следующие значения:

    - **Тип проекта:** Время и материал
    - **Название проекта:** XYZ обновление фаза 2
    - **Группа проекта:** TM\_WIP
    - **Идентификатор контракта по проекту:** 00000002

2. Выберите **Создать проект**.

## <a name="assign-a-resource-to-a-project"></a>Назначение ресурса проекту

1. На странице **Работники** в списке **Работники** выберите запись для работника, для которого настроены компетенции, и откройте запись работника.
2. На панели действий на вкладке **Проект** в группе **Настройка** выберите **Назначить проекты**.
3. На странице **Назначения проекта проверки ресурсов** на вкладке **Проекты** в поле **Добавить проект в выбранные проекты** отфильтруйте по проекту **XYZ обновление фаза 2**.
4. В области **Остальные проекты** выберите проект, а затем нажмите кнопку со стрелкой, чтобы добавить его в область **Выбранные проекты**.

Вы также можете назначать категории для ресурса по своему усмотрению. Тип категории: **Расход** или **Доход**. Тип категории определяется вашей организацией. Если для ресурса не назначены категории, Finance ищет категорию по умолчанию для почасовых цен для затрат и доходов.

## <a name="set-up-project-resource-and-role-characteristics"></a>Настройка характеристик ресурсов и ролей проекта

Менеджер проекта может использовать функцию выделения ресурсов проекту для создания ролей, необходимых для проекта. Роли могут использоваться, если подтвержденные ресурсы все еще неизвестны, когда ресурсы резервируются. Роли можно временно зарезервировать как запланированные ресурсы, чтобы вы могли продолжить этапы планирования проекта.

[![Пример роли](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Сценарий:** компания Contoso была нанята для завершения проекта «Время и материалы с утвержденным уставом проекта. Младший менеджер проекта все еще завершает объем проекта. Менеджер ресурсов в настоящее время определяет конкретные ресурсы, которые будут зарезервированы для работы над новым проектом. Из-за критического характера проекта спонсор проекта попросил "старшего менеджера проекта" в качестве одной из ролей. Менеджер ресурсов должен получить новый ресурс и определить роль в системе на случай, если младшему менеджеру проекта потребуется информация о ресурсах во время планирования проекта.

Следующие шаги показывают, как менеджер ресурсов может настроить роль старшего менеджера проекта и связать с ней характеристики ресурсов. Позже эту роль можно использовать для поиска доступных ресурсов, соответствующих требуемой компетенции ресурсов.

1. На странице **Настройка ролей** выберите **Создать** и введите следующие значения:

    - **Код роли:** старший менеджер проекта
    - **Описание:** старший менеджер проекта

2. Выберите **Создать**.
3. Выберите роль **Старший менеджер проекта** , а затем выберите **Настроить характеристики**.
4. В поле **Тип характеристик** выберите **Навык**.
5. В поле **Доступные характеристики** введите навык для поиска.
6. В поле **Тип характеристик** выберите **Сертификат**.
7. В поле **Доступные характеристики** введите тип сертификата для поиска.

## <a name="assign-a-project-resource-to-a-project"></a>Назначение ресурса проекта для проекта

1. На странице **Все проекты** выберите проект **XYZ обновление фаза 2**.
2. На вкладке **Проектная группа и планирование** выберите **Добавить**.
3. В поле **Роль** выберите **Участник рабочей группы**.
4. Выберите **Резервировать из календаря**.
5. На странице **Доступность ресурсов** выберите **Просмотр настроек**.
6. На странице **Настройка параметров просмотра** введите следующие значения:

    - **Формат представления диапазона дат:** день
    - **Показать описания доступности:** да
    - **Отображение оставшихся ресурсов:** да

7. Выберите ресурс из списка ресурсов.
8. Выберите **Окончательное резервирование** и **Полная загрузка**.

## <a name="assign-a-resource-to-a-default-role"></a>Назначение ресурса роли по умолчанию

Чтобы помочь менеджерам проектов или ресурсов детализировать могут ресурсы, которые можно зарезервировать для проекта. Вы можете связать роль по умолчанию с существующим ресурсом или только что приобретенным ресурсом. Например, когда Даниэл был принят на работу, у него был опыт и навыки, необходимые для выполнения роли бизнес-аналитика. Менеджер ресурсов назначил эту роль роли Дэниела по умолчанию. Поэтому менеджер ресурсов добавил Даниэля в группу бизнес-аналитиков, готовых работать над проектами.

Во время резервирования ресурсов менеджеры проектов могут фильтровать ресурсы ролей, доступные для работы над проектами. Они могут использовать эту информацию в качестве одного критерия при выполнении многокритериального анализа решений во время выполнения ресурса. Они также могут добавлять в фильтр другие характеристики ресурсов для поиска ресурсов, обладающих определенными навыками, образованием и опытом для данного проекта.

**Сценарий:** утвержденный проект начат, и роль старшего менеджера проекта была зарезервирована в качестве запланированного ресурса на этапе планирования проекта. Менеджер ресурсов теперь получил ресурс для выполнения роли старшего менеджера проекта.

1. На странице **Список ресурсов** выберите **Даниэль Гольдшмидт**.
2. На странице **Роль ресурса** выберите **Создать** и введите следующие значения:

    - **Действует:** введите текущую дату.
    - **Истекает:** Введите **Никогда**.
    - **Роль:** введите **старший менеджер проекта**.

3. Выберите **Сохранить** и закройте страницу.
4. На вкладке **Компетенции** добавьте навык **ProjectMgmt** и сертификат **PMP**.