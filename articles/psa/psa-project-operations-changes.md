---
title: Изменения функций при обновлении с Project Service Automation до Project Operations
description: В этой теме приведен обзор изменений в функциональности при переходе с Project Service Automation на Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/03/2022
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 7e41b381d6da267f58174305f33fc229c66cd7b7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595422"
---
# <a name="feature-changes-from-project-service-automation-to-project-operations"></a>Изменения функций при обновлении с Project Service Automation до Project Operations

Обновление с Dynamics 365 Project Service Automation до Dynamics 365 Project Operations Lite будет осуществляться в три фазы. Этот тема содержит информацию об основных изменениях, которые вы можете ожидать после завершения обновления.

| Доставка обновлений | Фаза 1 <br>(январь 2022 г.) | Фаза 2 <br>(апрельская волна 2022 г.) | Фаза 3  |
|------------------|------------------------|---------------------------|---------------------------|
| Отсутствие зависимости от структурной декомпозиции работ (WBS) для проектов. | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS включается в поддерживаемые в настоящее время лимиты Project Operations. | &nbsp; | :heavy_check_mark: | :heavy_check_mark: |
| WBS за пределами поддерживаемых в настоящее время лимитов Project Operations, включая поддержку Project Desktop Client/ | &nbsp; | &nbsp; | :heavy_check_mark: |

## <a name="project-management"></a>Управление проектами

Наиболее существенные изменения в пользовательском интерфейсе коснутся области планирования проекта. В Project Operations применяется новый современный подход к управлению структурной декомпозицией работ (WBS) путем использования возможностей планирования, предоставляемых решением [Project for the Web](https://support.microsoft.com/en-us/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5).

## <a name="differences-in-the-scheduling-experience"></a>Различия в интерфейсе планирования

В следующей таблице приведены различия в планировании между Project Service Automation и Project Operations.

|  Составление расписания     |   Project Operations   |   PSA   |
|-----------------|------------------------|---------|
| Шаблоны проектов — возможность определять и применять шаблоны проектов при создании проекта  |  &nbsp;    | :heavy_check_mark: |
| Интеграция структурной декомпозиции работ (WBS) проекта с настольным клиентом   |    &nbsp;  | :heavy_check_mark: |
| Ограничения — начать не раньше, закончить не позже  | :heavy_check_mark: |   &nbsp;  |
| Вехи — задачи с нулевой продолжительностью   | :heavy_check_mark:  |  &nbsp;  |
| Задачи на базе ресурсов будут учитывать доступность назначенных ресурсов   | :heavy_check_mark: |  &nbsp;    |
| Поэтапное редактирование — редактирование планов и работа день за днем   |   &nbsp;  | :heavy_check_mark: |
| Автоматическое/ручное планирование — использование механизма планирования Project для автоматического или ручного планирования задач |  &nbsp; | :heavy_check_mark:  |
| Редактирование больших проекты прямо в пользовательском интерфейсе: ограничений на размер редактируемых планов нет  | Лимит 500 задач  | :heavy_check_mark:       |
| Процент выполнения — возможность отмечать ход выполнения задачи   | :heavy_check_mark:  |  &nbsp;  |
| [Режимы планирования проекта](../project-management/scheduling-modes.md) — возможность определения проекта как проекта с фиксированными единицами, фиксированными трудозатратами или фиксированной длительностью | :heavy_check_mark: | &nbsp; |
| Временная шкала — создание и настройка представления временной шкалы для визуализирования деталей графика и обмена информацией с заинтересованными сторонами | :heavy_check_mark:  | &nbsp; |
| Задачи на основе трудозатрат — поддержка механизма планирования для планирования задач, основанных на трудозатратах  | :heavy_check_mark:  | &nbsp; |
| Диалоговое окно **Информация о задаче** — сохранение сведений о задаче с помощью диалогового окна | :heavy_check_mark:  |  &nbsp;  |
| Перетаскивание — множественный выбор задач и изменение их положения в WBS | :heavy_check_mark: | &nbsp;  |
| Гибкие сохраняемые представления — определение более детальных представлений атрибутов задач   | :heavy_check_mark:  | &nbsp; |
| Сортировка и фильтрация WBS  | :heavy_check_mark:  | &nbsp; |
| Представление досок для реализации проектов по моделям, отличным от модели "водопад"  | :heavy_check_mark:   | &nbsp; |
| Представление временной шкалы — интерактивная диаграмма Ганта, используемая для визуализации и редактирования WBS   | :heavy_check_mark:  | &nbsp; |
| Сочетания клавиш — использование сочетания клавиш для часто выполняемых операций, таких как отступ или вставка  | :heavy_check_mark:  |  &nbsp; |
| Многоуровневая отмена — выполнение анализа "что, если" для понимания последствий изменений путем отмены и повторного применения всего набора операций | :heavy_check_mark: | &nbsp; |
| Вырезание/копирование/вставка — совместная работа над созданием расписания путем копирования и вставки сведений о расписании из одного приложения в другое  | :heavy_check_mark: | &nbsp; |
| Контрольные списки задач — добвление в задачу до 20 пунктов контрольного списка   | :heavy_check_mark: | &nbsp; |

## <a name="project-planning"></a>Планирование проектов

Страница **Проект** в Project Operations имеет значительное количество отличий от страницы **Проект** в Project Service Automation.

Следующие действия были удалены со страницы **Проекты** в рамках фазы 1 обновления:

  - **Открыть в MS Project**
  - **Создать шаблон**
  - **Отменить связь из MS Project**

Страница **Проект** в Project Operations содержит следующие новые вкладки.

- **Оценки материалов**
- **Настройка выставления счетов по задачам**

Вкладка **Состояние** удалена, и поле **Состояние** теперь находится на вкладке **Сводка** вместе с режимом планирования проекта.

   ![Обновления на странице "Проект".](media/projectform.png)

Вкладка **Расписание** теперь называется **Задача** и предоставляет доступ к новому интерфейсу планирования проекта с помощью Project for the Web.

   ![Новая вкладка "Задачи проекта".](media/tasktab.png)

## <a name="scheduling-modes"></a>Режимы планирования

В Project Operations появилась новая функция: [режимы планирования](../project-management/scheduling-modes.md). Все существующие проекты Project Service Automation по умолчанию будут иметь режим **Фиксированная длительность** в Project Operations. Однако режим, устанавливаемый по умолчанию для новых проектов, можно задать, выбрав **Параметры** > **Параметры** > **Параметр** > **Режим планирования**.

   ![Настройки параметров проекта для режима планирования.](media/projectparameter.png)

## <a name="project-planning-limits"></a>Лимиты для планирования проектов

Project Operations использует Project for the Web для всех операций планирования проектов. Project for the Web управляет структурной декомпозицией работ с соблюдением лимитов, указанных в следующей таблице.

| **Поле**                                          | **Лимит**             |
|----------------------------------------------------|-----------------------|
| Максимальное общее количество задач для проекта                  | 500                   |
| Максимальная общая длительность для проекта               | 3650 дней (10 лет)  |
| Максимальное общее количество ресурсов для проекта              | 300                   |
| Максимальное общее количество ссылок (только преемник) для проекта | 600                   |
| Максимальное общее количество пользовательских полей для проекта          | 10                    |
| Максимальное количество уровней иерархии                            | 10 уровней             |
| Максимальное количество ссылок (преемник + предшественник)            | 20                    |
| Максимальная длительность листовой задачи                      | 1250 дней             |
| Максимальная длительность сводной задачи                 | 3650 дней (10 лет)  |
| Максимальное количество ресурсов, назначенных задаче               | 20 ресурсов          |
| Поддерживаемый диапазон дат для задачи                    | 01.01.2000 – 31.12.2149 |
| Пункты контрольного списка                                    | 20                    |

## <a name="project-planning-extensibility-and-development"></a>Расширяемость и разработка механизмов планирования проектов

После обновления до Project Operations вы должны использовать API-интерфейсы Project Scheduling для выполнения операций создания, обновления и удаления для следующих сущностей:

|   имя сущности,           |   Логическое имя сущности       |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Задача проекта            | msdyn_projecttask           |
| Зависимость задач проекта | msdyn_projecttaskdependency |
| Назначение ресурса     | msdyn_resourceassignment    |
| Группа проекта          | msdyn_projectbucket         |
| Участник проектной группы     | msdyn_projectteam           |

Если в настоящее время у вас есть настройки, в которых используются эти сущности, прочитайте рекомендации по внедрению здесь: [Использование API-интерфейсов планирования проектов с сущностями планирования](../project-management/schedule-api-preview.md).

## <a name="data-model-changes"></a>Изменения в модели данных

В рамках фазы 1 обновления в модель данных вносятся изменения. Эти изменения в первую очередь являются представляют собой изменение полей в существующих сущностях. На фазе 1 сущности **msydn_project** и **msdyn_projectteam** представляют собой рефакторинг настроек. 

> [!IMPORTANT]
> На дальнейших фазах обновления в этот раздел будут добавляться дополнительные сущности.

Следующие поля были заменены новыми полями.

|   Объект          |   Старое логическое имя   |   Новое логическое имя    |
|-------------------|----------------------|-----------------------|
| msdyn_project     | msdyn_actualhours    | msdyn_effortcompleted |
| msdyn_project     | msdyn_plannedhours   | msdyn_effort          |
| msdyn_project     | msdyn_remaininghours | msdyn_effortremaining |
| msdyn_project     | msdyn_scheduledend   | msdyn_finish          |
| msdyn_project     | msdyn_wbsduration    | msdyn_duration        |
| msdyn_projectteam | msdyn_assignedhours  | msdyn_effort          |
| msdyn_projectteam | msdyn_from           | msdyn_start           |
| msdyn_projectteam | msdyn_to             | msdyn_finish          |

Добавлены следующие поля.

|   Объект          |   Логическое имя                               |   Description |
|-------------------|----------------------------------------------|---------------|
| msdyn_project     | msdyn_actualfeesales                         | Показывает совокупные фактические сборы от продаж по проекту. Только для использования в Project Service Automation. |
| msdyn_project     | msdyn_actualmaterialcost                     | Показывает совокупную фактическую стоимость материалов по проекту. Только для использования в Project Service Automation. |
| msdyn_project     | msdyn_actualmaterialsales                    | Показывает совокупные фактические продажи материалов по проекту. Только для использования в Project Service Automation. |
| msdyn_project     | msdyn_businesscase                           |                |
| msdyn_project     | msdyn_contractlineproject                    | Строка контракта, связанная с этим проектом. |
| msdyn_project     | msdyn_copyprojectcorrelationid               | Это внутреннее системное поле, исползуемое для функции **Копировать проект**, связанное с идентификатором корреляции. Только для использования в Project Service Automation. |
| msdyn_project     | msdyn_copyprojectsessionid                   | Это внутреннее системное поле, исползуемое для функции **Копировать проект**, связанное с идентификатором сеанса. Только для использования в Project Service Automation. |
| msdyn_project     | msdyn_globalrevisiontoken                    | Глобальный токен версии xRM последней синхронизации из Project Scheduling Service. |
| msdyn_project     | msdyn_msprojectdocument                      | Документ Microsoft Project, принадлежащий к проекту. |
| msdyn_project     | msdyn_plannedmaterialcost                    | Совокупная планируемая стоимость материалов по проекту. Только для использования в Project Service Automation. |
| msdyn_project     | msdyn_plannedmaterialsales                   | Совокупные планируемые продажи материалов по проекту. Только для использования в Project Service Automation. |
| msdyn_project     | msdyn_program                                | Программа, к которой относится этот проект. |
| msdyn_project     | msdyn_quotelineproject                       | Строка предложения с расценками, связанная с этим проектом. |
| msdyn_project     | msdyn_replaylogheader                        | Заголовок для журналов воспроизведения. |
| msdyn_project     | msdyn_schedulemode                           | Режим планирования по умолчанию, используемый для всех задач проекта.  |
| msdyn_project     | msdyn_taskearlieststart                      | Самая ранняя дата начала любой задачи в проекте.  |
| msdyn_project     | msdyn_valuestatement                         |                |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Участник проектной группы, из которого скопирован этот участник проектной группы. |
| msdyn_projectteam | msdyn_creategenericteammemberwithrequirement | Указывает, следует ли создавать требование ресурса для вновь созданного универсального участника рабочей группы.  |
| msdyn_projectteam | msdyn_deletestatus                           | Состояние удаления участника группы для отслеживания того, был ли отправлен запрос на удаление в Project Scheduling Service и отправила ли эта служба ответ успешно и в ожидаемый временной диапазон. |
| msdyn_projectteam | msdyn_effortcompleted                        | Позволяет отслеживать трудозатраты, затраченные участником рабочей группы на назначеные ему задачи. |
| msdyn_projectteam | msdyn_effortremaining                        | Позволяет отслеживать трудозатраты, которые участнику рабочей группы еще предстоит затратить на назначеные ему задачи. |
| msdyn_projectteam | msdyn_markedfordeletiontimer                 | Период ожидания с момента, когда участник рабочей группы отправляет запрос на удаление в Project Scheduling Service до фактического удаления этого участник рабочей группы в Microsoft Dataverse.|
| msdyn_projectteam | msdyn_markedfordeletiontimestamp             | Метка времени для записи времени отправки запрос на удаление участника группы в Project Scheduling Service. |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Показывает участника проектной группы, из которого скопирован этот участник проектной группы.  |

## <a name="project-templates"></a>Шаблоны проектов

Project Operations не поддерживает шаблоны проектов. Однако вы можете воспроизвести большую часть основных функций с помощью [API копирования проекта](../project-management/dev-copy-project.md).

## <a name="desktop-add-in-support"></a>Поддержка классической надстройки

Поддержка классической надстройки Microsoft Project будет недоступна в течение первых двух фаз обновления. На фазе 3 клиенты, размеры проектов которых превышают поддерживаемые в настоящее время лимиты Project for the Web, смогут использовать классическую надстройку.

## <a name="editing-resource-assignment-contours"></a>Редактирование контуров назначения ресурсов

Возможность редактирования контуров назначения ресурсов будет доступна, когда будет доступна фаза 2 обновления.

## <a name="billing-and-pricing"></a>Выставление счетов и ценообразование

Следующие новые функции были добавлены в Project Operations. Эти функции являются аддитивными по своей природе и не влияют на модель данных Project Service Automation.

- [Запись использования материалов по проектам и задачам проекта](../material/material-usage-log.md)
- [Управление субподрядом](../pro/subcontracting/managing-subcontracts-overview.md)
- [Авансы и контракты с предоплатой](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Состояние и проверка соблюдения лимитов контракта](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- [Выставление счетов по задачам](../pro/sales/mapping-projects-tasks-quote-line-sales.md)

## <a name="deprecated-components"></a>Устаревшие компоненты

В следующих таблицах задокументированы все устаревшие поля, перемещаемые в решение для устаревших компонентов после обновления. Дополнительные сведения и ссылку на это решение см. в разделе [Устаревшие компоненты при переходе с Dynamics 365 Project Service Automation 3x на Project Operations 4x](https://github.com/microsoft/Dynamics365-Project-Operations-PowerApps/tree/main/3x-4x-deprecated-solution).

### <a name="invoicedetail"></a>invoicedetail

| Поля                                                    |
|-----------------------------------------------------------------------------------------------|
|invoicedetail.msdyn_contractline    |

### <a name="msdyn_actual"></a>msdyn_actual

| Поля                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_actual.msdyn_salescontractline                                                          |

### <a name="msdyn_characteristicreqforteammember"></a>msdyn_characteristicreqforteammember

| Поля                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_characteristicreqforteammember.msdyn_characteristic                                     |
| msdyn_characteristicreqforteammember.msdyn_characteristicreqforteammemberid                   |
| msdyn_characteristicreqforteammember.msdyn_characteristictype                                 |
| msdyn_characteristicreqforteammember.msdyn_name                                               |
| msdyn_characteristicreqforteammember.msdyn_ratingvalue                                        |
| msdyn_characteristicreqforteammember.msdyn_resourcerequirementid                              |

### <a name="msdyn_contractlineinvoiceschedule"></a>msdyn_contractlineinvoiceschedule

| Поля                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_contractlineinvoiceschedule.msdyn_contractline                                          |
| msdyn_contractlinescheduleofvalue.msdyn_contractline                                          |
 
### <a name="msdyn_dataexport"></a>msdyn_dataexport

| Поля                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_dataexport.msdyn_dataexportid                                                           |
| msdyn_dataexport.msdyn_datatoken                                                              |
| msdyn_dataexport.msdyn_entityname                                                             |
| msdyn_dataexport.msdyn_exportedrecordcount                                                    |
| msdyn_dataexport.msdyn_exportstatus                                                           |
| msdyn_dataexport.msdyn_linkedentitydata                                                       |
| msdyn_dataexport.msdyn_name                                                                   |
| msdyn_dataexport.msdyn_pagingdata                                                             |

### <a name="msdyn_fact"></a>msdyn_fact

| Поля                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_fact.msdyn_salescontractline                                                            |

### <a name="msdyn_findworkevent"></a>msdyn_findworkevent

| Поля                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_findworkevent.msdyn_bookableresource                                                    |
| msdyn_findworkevent.msdyn_findworkeventid                                                     |
| msdyn_findworkevent.msdyn_name                                                                |
| msdyn_findworkevent.msdyn_timestamp                                                           |
| msdyn_findworkevent.msdyn_type                                                                |
| msdyn_findworkevent.msdyn_value                                                               |
| msdyn_findworkevent.msdyn_work                                                                |

### <a name="msdyn_invoicelinetransaction"></a>msdyn_invoicelinetransaction

| Поля                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_invoicelinetransaction.msdyn_invoiceline                                                |
| msdyn_invoicelinetransaction.msdyn_salescontractline                                          |

### <a name="msdyn_journalline"></a>msdyn_journalline

| Поля                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_journalline.msdyn_salescontractline                                                     |

### <a name="msdyn_opportunitylineresourcecategory"></a>msdyn_opportunitylineresourcecategory

| Поля                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylineresourcecategory.msdyn_billingtype                                       |
| msdyn_opportunitylineresourcecategory.msdyn_description                                       |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylineresourcecategoryid                 |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylinetransactionclassification          |
| msdyn_opportunitylineresourcecategory.msdyn_resourcecategory                                  |

### <a name="msdyn_opportunitylinetransaction"></a>msdyn_opportunitylinetransaction

| Поля                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransaction.msdyn_accountcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_accountingdate                                         |
| msdyn_opportunitylinetransaction.msdyn_accountvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_amount                                                 |
| msdyn_opportunitylinetransaction.msdyn_amount_base                                            |
| msdyn_opportunitylinetransaction.msdyn_amountmethod                                           |
| msdyn_opportunitylinetransaction.msdyn_basisamount                                            |
| msdyn_opportunitylinetransaction.msdyn_basisamount_base                                       |
| msdyn_opportunitylinetransaction.msdyn_basisprice                                             |
| msdyn_opportunitylinetransaction.msdyn_basisprice_base                                        |
| msdyn_opportunitylinetransaction.msdyn_basisquantity                                          |
| msdyn_opportunitylinetransaction.msdyn_billingtype                                            |
| msdyn_opportunitylinetransaction.msdyn_bookableresource                                       |
| msdyn_opportunitylinetransaction.msdyn_contactcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_contactvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_customertype                                           |
| msdyn_opportunitylinetransaction.msdyn_description                                            |
| msdyn_opportunitylinetransaction.msdyn_documentdate                                           |
| msdyn_opportunitylinetransaction.msdyn_enddatetime                                            |
| msdyn_opportunitylinetransaction.msdyn_exchangeratedate                                       |
| msdyn_opportunitylinetransaction.msdyn_opportunityline                                        |
| msdyn_opportunitylinetransaction.msdyn_opportunitylinetransactionid                           |
| msdyn_opportunitylinetransaction.msdyn_percent                                                |
| msdyn_opportunitylinetransaction.msdyn_price                                                  |
| msdyn_opportunitylinetransaction.msdyn_price_base                                             |
| msdyn_opportunitylinetransaction.msdyn_pricelist                                              |
| msdyn_opportunitylinetransaction.msdyn_product                                                |
| msdyn_opportunitylinetransaction.msdyn_project                                                |
| msdyn_opportunitylinetransaction.msdyn_quantity                                               |
| msdyn_opportunitylinetransaction.msdyn_resourcecategory                                       |
| msdyn_opportunitylinetransaction.msdyn_resourceorganizationalunitid                           |
| msdyn_opportunitylinetransaction.msdyn_startdatetime                                          |
| msdyn_opportunitylinetransaction.msdyn_task                                                   |
| msdyn_opportunitylinetransaction.msdyn_transactioncategory                                    |
| msdyn_opportunitylinetransaction.msdyn_transactionclassification                              |
| msdyn_opportunitylinetransaction.msdyn_transactiontypecode                                    |
| msdyn_opportunitylinetransaction.msdyn_unit                                                   |
| msdyn_opportunitylinetransaction.msdyn_unitschedule                                           |
| msdyn_opportunitylinetransaction.msdyn_vendortype                                             |

### <a name="msdyn_opportunitylinetransactioncategory"></a>msdyn_opportunitylinetransactioncategory

| Поля                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactioncategory.msdyn_billingtype                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_description                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactioncategoryid           |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactionclassification       |
| msdyn_opportunitylinetransactioncategory.msdyn_transactioncategory                            |

### <a name="msdyn_opportunitylinetransactionclassificatio"></a>msdyn_opportunitylinetransactionclassificatio

| Поля                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactionclassificatio.msdyn_billingtype                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_description                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_include                                   |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunityline                           |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunitylinetransactionclassificatioid |
| msdyn_opportunitylinetransactionclassificatio.msdyn_transactionclassification                 |

### <a name="msdyn_orderlineresourcecategory"></a>msdyn_orderlineresourcecategory

| Поля                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlineresourcecategory.msdyn_contractline                                            |

### <a name="msdyn_orderlinetransaction"></a>msdyn_orderlinetransaction

| Поля                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransaction.msdyn_salescontractline                                            |
| msdyn_orderlinetransactioncategory.msdyn_contractline                                         |

### <a name="msdyn_orderlinetransactionclassification"></a>msdyn_orderlinetransactionclassification

| Поля                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransactionclassification.msdyn_contractline                                   |

### <a name="msdyn_project"></a>msdyn_project

| Поля                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_project.msdyn_actualdurationminutes                                                     |
| msdyn_project.msdyn_actualhours                                                               |
| msdyn_project.msdyn_istemplate                                                                |
| msdyn_project.msdyn_plannedhours                                                              |
| msdyn_project.msdyn_projecttemplate                                                           |
| msdyn_project.msdyn_remaininghours                                                            |
| msdyn_project.msdyn_scheduleddurationminutes                                                  |
| msdyn_project.msdyn_scheduledend                                                              |
| msdyn_project.msdyn_stagename                                                                 |
| msdyn_project.msdyn_wbsduration                                                               |


### <a name="msdyn_projecttask"></a>msdyn_projecttask

| Поля                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttask.msdyn_actualdurationminutes                                                 |
| msdyn_projecttask.msdyn_actualeffort                                                          |
| msdyn_projecttask.msdyn_aggregationdirection                                                  |
| msdyn_projecttask.msdyn_assignedresources                                                     |
| msdyn_projecttask.msdyn_assignedteammembers                                                   |
| msdyn_projecttask.msdyn_autoscheduling                                                        |
| msdyn_projecttask.msdyn_costestimatecontour                                                   |
| msdyn_projecttask.msdyn_effortcontour                                                         |
| msdyn_projecttask.msdyn_islinetask                                                            |
| msdyn_projecttask.msdyn_numberofresources                                                     |
| msdyn_projecttask.msdyn_remaininghours                                                        |
| msdyn_projecttask.msdyn_resourceutilization                                                   |
| msdyn_projecttask.msdyn_salesestimatecontour                                                  |
| msdyn_projecttask.msdyn_scheduledhours                                                        |
| msdyn_projecttask.msdyn_wbsid                                                                 |

### <a name="msdyn_projecttaskstatususer"></a>msdyn_projecttaskstatususer

| Поля                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttaskstatususer.msdyn_bookableresource                                            |
| msdyn_projecttaskstatususer.msdyn_description                                                 |
| msdyn_projecttaskstatususer.msdyn_expectedcompletiondate                                      |
| msdyn_projecttaskstatususer.msdyn_expectedhourstocomplete                                     |
| msdyn_projecttaskstatususer.msdyn_iscompleted                                                 |
| msdyn_projecttaskstatususer.msdyn_name                                                        |
| msdyn_projecttaskstatususer.msdyn_percentcomplete                                             |
| msdyn_projecttaskstatususer.msdyn_projecttaskid                                               |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatusindicator                                  |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatususerid                                     |

### <a name="msdyn_projectteam"></a>msdyn_projectteam

| Поля                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteam.msdyn_applicantcount                                                        |
| msdyn_projectteam.msdyn_applicantsavailable                                                   |
| msdyn_projectteam.msdyn_assignedhours                                                         |
| msdyn_projectteam.msdyn_description                                                           |
| msdyn_projectteam.msdyn_from                                                                  |
| msdyn_projectteam.msdyn_hoursrequested                                                        |
| msdyn_projectteam.msdyn_membershipstatus                                                      |
| msdyn_projectteam.msdyn_number                                                                |
| msdyn_projectteam.msdyn_to                                                                    |

### <a name="msdyn_projectteammembersignup"></a>msdyn_projectteammembersignup

| Поля                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteammembersignup.msdyn_bookableresource                                          |
| msdyn_projectteammembersignup.msdyn_membershipstatus                                          |
| msdyn_projectteammembersignup.msdyn_name                                                      |
| msdyn_projectteammembersignup.msdyn_projectteammembersignupid                                 |
| msdyn_projectteammembersignup.msdyn_teammembership                                            |

### <a name="msdyn_projecttransactioncategory"></a>msdyn_projecttransactioncategory

| Поля                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttransactioncategory.msdyn_billingtype                                            |
| msdyn_projecttransactioncategory.msdyn_name                                                   |
| msdyn_projecttransactioncategory.msdyn_project                                                |
| msdyn_projecttransactioncategory.msdyn_projecttransactioncategoryid                           |
| msdyn_projecttransactioncategory.msdyn_transactioncategory                                    |

### <a name="msdyn_quotelineinvoiceschedule"></a>msdyn_quotelineinvoiceschedule

| Поля                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_quotelineinvoiceschedule.msdyn_quoteline                                                |
| msdyn_quotelineresourcecategory.msdyn_quoteline                                               |
| msdyn_quotelinescheduleofvalue.msdyn_quoteline                                                |
| msdyn_quotelinetransaction.msdyn_quoteline                                                    |
| msdyn_quotelinetransactioncategory.msdyn_quoteline                                            |
| msdyn_quotelinetransactionclassification.msdyn_quoteline                                      |

### <a name="msdyn_resourceassignment"></a>msdyn_resourceassignment

| Поля                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_resourceassignment.msdyn_hours                                                          |
| msdyn_resourceassignment.msdyn_fromdate                                                       |
| msdyn_resourceassignment.msdyn_msprojectclientid                                              |
| msdyn_resourceassignment.msdyn_todate                                                         |
| msdyn_resourceassignmentdetail.msdyn_duration                                                 |
| msdyn_resourceassignmentdetail.msdyn_from                                                     |
| msdyn_resourceassignmentdetail.msdyn_name                                                     |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentdetailid                               |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentid                                     |

### <a name="salesorderdetail"></a>salesorderdetail

| Поля                                                    |
|-----------------------------------------------------------------------------------------------|
| salesorderdetail.msdyn_quoteline                                                              |

