---
title: Новые возможности в сентябре 2022 г. — Project Operations для сценариев на основе ресурсов/без запасов
description: В этой статье содержится информация об исправлениях, доступных в выпуске Microsoft Dynamics 365 Project Operations для сценариев на основе ресурсов/без запасов за сентябрь 2022 года.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 04b5f2f8223cdc80028860dd880dde314be244eb
ms.sourcegitcommit: b3a70bc4f2850cff5c2b7114cff7bd61ec298143
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/06/2022
ms.locfileid: "9634822"
---
# <a name="whats-new-september-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Новые возможности в сентябре 2022 г. — Project Operations для сценариев на основе ресурсов/без запасов

_**Относится к:** Project Operations для сценариев на основе ресурсов/без запасов_

Эта статья применяется к следующим компонентам и версиям Microsoft Dynamics 365 Project Operations:

- Project Operations в среде Dataverse версии 4.46.0.60
- Управление и учет по проектам в среде Dynamics 365 Finance версии 10.0.29

## <a name="features-included-in-this-release"></a>Функции, входящие в данный выпуск

| Область функций | Имя функции | Дополнительная информация |
| --- | --- | --- |
| Управление возможными сделками | **Пересмотр и активация предложений с расценками**<br>Project Operations обеспечивает полную поддержку процесса продаж. Предложения по проекту можно активировать для представления состояния, в котором предложение доступно только для чтения и находится на рассмотрении. Активированные предложения с расценками можно изменить, чтобы создать новые предложения с увеличенным номером редакции. Активированные предложения с расценками по проекту или пересмотренные предложения могут быть закрыты как выигранные или потерянные. | [Активация и пересмотр предложения с расценками по проекту](/dynamics365/project-operations/sales/activation-and-revision) |
| Выставление счетов и цены | **Цена по умолчанию не зависит от часового пояса**<br>В Project Operations представлена концепция даты, не зависящей от часового пояса, для всех фактических данных проекта. Новое поле, **Дата транзакции**, теперь доступно в строках журнала и фактических данных и будет использоваться для хранения даты, когда произошла транзакция, но без преобразования этой даты в универсальное скоординированное время. Эта дата будет использоваться для последующих процессов, таких как установление цены по умолчанию и создание счета-фактуры. | <p>[Определение ставок затрат для сметных и фактических значений на основе проекта](/dynamics365/project-operations/pricing-costing/cost-price-resolution)</p><p>[Определение значений цены продажи для оценок и фактических значений на основе проекта](/dynamics365/project-operations/pricing-costing/sales-price-resolution)</p> |
| Выставление счетов и цены | **Переопределение цен с датой вступления в силу в Project Operations**<br>Переопределение цены со сроком действия предоставляет способ переопределить или изменить определенные цены в прайс-листе. | [Переопределения цены со сроком действия](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Субподряд | **Субподряд и сверка счетов-фактур поставщиков**<br>Эта функция позволяет клиентам создавать субконтракты для приобретения времени ресурсов, категорий расходов и материалов, которые используются для работы над проектом. Это также позволяет клиентам записывать в приложениях для управления финансами и операциями, счета-фактуры поставщиков, которые будут доступны менеджерам проектов в Dataverse для подтверждения. | <p>[Управление субподрядом](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview)</p><p>[Создание накладных поставщиков](/dynamics365/project-operations/procurement/vendor-invoicing-concept-and-creation)</p> |
| Время и расходы | **Глобальный утверждающий**<br>Эта функция обеспечивает утверждение независимого поставщика программного обеспечения (ISV) и централизованное утверждение, независимо от статуса проекта или участника рабочей группы в проекте. | [Безопасность и утверждения](/dynamics365/project-operations/approvals/approvals-security) |
| Управление расходами | **Возможность проводки обязательств по расходам в валюте поставщика**<br>Эта функция позволяет проводить отчеты о расходах в валюте поставщика для метода оплаты наличными. | [Возможность проводки обязательств по расходам в валюте поставщика](/dynamics365/project-operations/expense/posting-expense-reports#enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature) |
| Закупки по проекту | **Платежи поставщикам с оплатой после получения оплаты от клиентов**<br>Эта функция позволяет использовать функцию «Оплата при оплате» (PWP) со средами Project Operations без склада. Это позволяет блокировать/удерживать платежи поставщика на основе условий удержания до тех пор, пока платеж не будет получен от клиента. | [Платежи поставщикам с оплатой после получения оплаты от клиентов](/dynamics365/project-operations/procurement/pay-when-paid) |
| Закупки по проекту | **Заявки на покупку по проекту**<br>Эта функция позволяет пользователям создавать связанные с проектом заказы на покупку в юридических лицах, для которых включена интеграция Project Operations в Dynamics 365 Customer Engagement. Заказы на закупку по проекту можно использовать для записи закупок нескладируемых материалов по проекту сотрудником отдела закупок. Заказы на покупку по проекту не будут синхронизированы с Dataverse. Однако вы можете использовать виртуальную сущность для отображения строк заказа на покупку по проекту в Dataverse для информации менеджера проекта. Связанная с проектом стоимость счета-фактуры поставщика интегрирована с сущностью «Фактические данные проекта» в Dataverse. Затраты по проекту регистрируются в субкниге проекта с помощью журнала интеграции Project Operations. | |
|Планирование и отслеживание проектов|**Использование API расписания проекта для выполнения операций с сущностями планирования** </br> </br>API редактирования контура назначения ресурсов позволяет разработчикам программным образом указывать трудозатраты исполнителя задачи в любом поддерживаемом диапазоне дат с целью более детального поэтапного планирования трудозатрат.|[Использование API расписания проекта для выполнения операций с сущностями планирования](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="project-operations-dual-write-maps-updates"></a>Обновления сопоставления с двойной записью Project Operations

В следующей таблице приведены сопоставления двойной записи, измененные или добавленные в выпуске Project Operations за сентябрь 2022 года.

| Сопоставление сущностей | Обновленная версия | Комментарии |
| -------------- | ------------------- | ------------|
| Фактические данные интеграции Project Operations (msdyn_actuals) | 1.0.0.15 | Эта карта поддерживает обработку фактических значений субконтракта с помощью Project Operations для сценариев на основе ресурсов. |
| Сущность экспорта накладной поставщика проекта интеграции Project Operations (msdyn_projectvendorinvoices) | 1.0.0.2 | Эта карта поддерживает обработку фактических значений субконтракта с помощью Project Operations для сценариев на основе ресурсов. |
| Сущность экспорта строки накладной поставщика проекта интеграции Project Operations (msdyn_projectvendorinvoicelines) | 1.0.0.5 | Эта карта поддерживает обработку фактических значений субконтракта с помощью Project Operations для сценариев на основе ресурсов. |

Всегда запускайте последнюю версию сопоставления в своей среде и включайте все связанные карты таблиц при обновлении решения Project Operations Dataverse и версии решения Finance. Некоторые функции и возможности могут работать некорректно, если не активирована последняя версия сопоставления. Вы можете увидеть активную версию сопоставления в столбце **Версия** на странице **Двойная запись**. Чтобы активировать новую версию сопоставления, выберите **Версии сопоставления таблиц**, выберите последнюю версию, а затем сохраните выбранную версию. Если вы настроили стандартное сопоставление таблиц, примените изменения повторно. Дополнительные сведения см. в [Управление жизненным циклом приложений](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Если вы столкнулись с проблемой при запуске сопоставления, следуйте инструкциям в разделе [В картах отсутствуют столбцы таблицы](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) в руководстве по устранению неполадок с двойной записью.

## <a name="quality-updates"></a>Обновления качества

### <a name="project-operations-on-dataverse"></a>Project Operations на Dataverse

| Область функций | Номер ссылки | Обновление качества |
| --- | --- | --- |
| Выставление счетов и цены | 2754422 | Оценки материалов и расходов не передаются в Finance при копировании проектов в Dataverse. |
| Время и расходы | 2787409 | Недействительный утверждающий может утвердить ввод времени, не связанного с проектом. |
| Управление возможными сделками | 2788907 | Обновлено сообщение об ошибке при проверке уникальности для строк заказа, содержащих флаги. |
| Время и расходы | 2842253 | Обработка исключений Null для утверждения времени. |
| Выставление счетов и цены | 2844181 | Неспособность получить идентификатор корреляции блокирует создание счета. |
| Выставление счетов и цены | 2876628 | QLD, CLD — при расчете разрешения прайс-листа следует использовать устаревшие поля диапазона дат прайс-листа. |
| Субподряд | 2893222 | Если для строки субподряда роль не указана, должна быть возможность выбрать эту строку для участника рабочей группы для любой роли. |

### <a name="project-management-and-accounting-in-finance"></a>Управление и учет для проектов в Finance

Для получения сведений об исправлениях ошибок, включенных в это обновление, войдите в Microsoft Dynamics Lifecycle Services и просмотрите [статью базы знаний](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Функции, включенные по умолчанию в предстоящем выпуске

В этой таблице перечислены функции, включенные по умолчанию в версии 10.0.30. Большинство функций, включенных автоматически, могут быть отключены в [управлении функциями](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). В будущем некоторые функции, которые были включены автоматически, могут быть удалены из раздела управления функциями и могут стать обязательными. Это изменение гарантирует, что клиенты используют актуальные функции, чтобы добавляемые улучшения были основаны на актуальных функциях. Функции никогда не будут автоматически включены раньше, чем через год, если только они не будут признаны ключевыми.

| Имя функции | Дата включения | Функция добавлена | Состояние функции | Модуль |
| --- | --- | --- |--- |--- |
| Включение асинхронной операции, когда пользователю нужно переключаться между синхронными и асинхронными операциями | 21 октября 2022 года | 9 апреля 2021 г. | Включено по умолчанию | Управление расходами |
| Требуется оценка политики расходов для квитанций | 21 октября 2022 года | 20 декабря 2021 г. | Включено по умолчанию | Управление расходами |
| Представление списка отчетов о расходах, созданных делегированными работниками | 21 октября 2022 года | 19 февраля 2020 г. | Включено по умолчанию | Управление расходами |
| Расчет общего пробега за финансовый год | 21 октября 2022 года | 10 мая 2022 г. | Включено по умолчанию | Управление расходами |