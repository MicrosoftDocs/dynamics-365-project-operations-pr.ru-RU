---
title: Новые возможности в ноябре 2021 г. — Project Operations для сценариев на основе ресурсов/без запасов
description: В этой статье содержится информация об обновлениях качества, доступных в выпуске Project Operations за ноябрь 2021 года для сценариев на основе ресурсов/без запасов.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d5b58965f728321cc30d4e476b0dacf621fdec71
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932910"
---
# <a name="whats-new-november-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Новые возможности в ноябре 2021 г. — Project Operations для сценариев на основе ресурсов/без запасов

*Относится к: Project Operations для сценариев на основе ресурсов/без запасов*

Эта статья применяется к следующим компонентам и версиям Microsoft Dynamics 365 Project Operations:

- Project Operations в среде Dataverse версии 4.26.0.145, 4.26.0.148, 4.26.0.150, 4.26.0.155
- Управление и учет по проектам в среде Dynamics 365 Finance версии 10.0.22

## <a name="features-included-in-this-release"></a>Функции, входящие в данный выпуск

В состав этого выпуска входят следующие функции:

- Программные интерфейсы (API) планирования проектов теперь поддерживают возможность создания и удаления сегментов проекта.

## <a name="project-operations-dual-write-maps-updates"></a>Обновления сопоставления с двойной записью Project Operations

В этом выпуске нет обновлений для карт Project Operations с двойной записью. Для получения информации о текущем списке и версиях карт с двойной записью Project Operations см. [Версии карты с двойной записью Project Operations](/dynamics365/project-operations/environment/resource-dual-write-maps).

Всегда запускайте последнюю версию сопоставления в своей среде и включайте все связанные карты таблиц при обновлении решения Project Operations Dataverse и версии решения Finance. Некоторые функции и возможности могут работать некорректно, если не активирована последняя версия сопоставления. Вы можете увидеть активную версию сопоставления в столбце **Версия** на странице **Двойная запись**. Чтобы активировать новую версию сопоставления, выберите **Версии сопоставления таблиц**, выберите последнюю версию, а затем сохраните выбранную версию. Если вы настроили стандартное сопоставление таблиц, примените изменения повторно. Дополнительные сведения см. в [Управление жизненным циклом приложений](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Если вы столкнулись с проблемой при запуске сопоставления, следуйте инструкциям в разделе [В картах отсутствуют столбцы таблицы](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) в руководстве по устранению неполадок с двойной записью.

## <a name="quality-updates"></a>Обновления качества

### <a name="project-operations-in-dataverse"></a>Project Operations в Dataverse

| Область функций | Номер ссылки | Обновление качества |
| --- | --- | --- |
| Выставление счетов и цены | 2240080 | Поле **Условия оплаты** не должно дублироваться в предварительной накладной. |
| Выставление счетов и цены | 2358236 | Коррекция накладной должна допускать исправления со строками нулевой цены. |
| Управление ресурсами | 2410072 | Разрешить настройку ресурса, который назначен задаче в качестве менеджера проекта. |
| Выставление счетов и цены | 2430234 | Устранить проблему с расчетом эффективности затрат. |
| Время и расходы | 2436978 | Разрешить вводить время в формате чч:мм. |
| Выставление счетов и цены | 2448623 | Разрешить обновление прайс-листов после того, как они будут связаны с организационным подразделением. |
| Время и расходы | 2460396 | Разрешить удаление записи времени путем очистки ячейки. |
| Выставление счетов и цены | 2467386 | Разрешить удаление проекта, в котором есть задача, даже если задача связана с выигранным предложением. |
| Время и расходы | 2461744 | Представление **Мои неудачные утверждения** содержит только утверждения проектов на этапе **Отправлено**. |
| Время и расходы | 2464082 | Удалить ссылку из утверждений проекта на набор утверждений при совпадении целевого статуса. |
| Время и расходы | 2468108 | Задание расписания не должно устанавливать статус **Обработка** для набора утверждения. |
| Время и расходы | 2471503 | Удалить наборы утверждений, которым уже семь дней. |
| Выставление счетов и цены | 2480687 | Ссылку на строку предложения не должна удаляться при создании вехи строки предложения. |

### <a name="project-management-and-accounting-in-finance"></a>Управление и учет для проектов в Finance

| Область функций | Номер ссылки | Обновление качества |
| --- | --- | --- |
| Управление и учет по проектам | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Удерживаемые суммы поставщика в проводках расходов по проекту не отображаются в списке проводок. |
| Управление и учет по проектам | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Счет-фактура внутрихолдингового поставщика не работает, если включена интеграция накладных поставщика. |
| Управление и учет по проектам | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Условия оплаты по счетам-фактурам проекта не работают должным образом. |
| Управление и учет по проектам | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Когда удержание поставщика разблокировано, в разноске ваучера есть дополнительные строки, которые неверны. |
| Управление и учет по проектам | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Когда журнал интеграции Project Operations разносится, он дает сбой из-за отсутствия измерений для учетной записи, в которую не выполняется разноска. |
| Управление и учет по проектам | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | Вкладка **Проект** недоступна для редактирования в незавершенном счете-фактуре поставщика, когда номенклатуре присвоена категория закупки. |
| Управление и учет по проектам | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Панель навигации отсутствует, если вы не вошли в Project Operations Dataverse. |
| Управление и учет по проектам | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Когда вы проводите выручку по счету-фактуре по проекту в случае примененного фиксированного платежа, возникает проблема, потому что транзакции по ваучеру не балансируются. |
| Управление и учет по проектам | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Создание оценки после разноски предложения по накладной блокирует импорт строк коррекции. |
| Управление и учет по проектам | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Изменение записи вехи с полностью выставленными счетами не должно быть возможным. |
| Проезд и расходы | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Все отчеты о расходах видны при поиске категории в мобильном приложении "Расходы". |
| Проезд и расходы | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Неправильные суммы по проводкам по поставщику и налогу с продаж разносятся из расхода, созданного из проводки по кредитной карте. |
| Проезд и расходы | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Когда вы обновляете страницу **Отчет о затратах**, отображается ненужное предупреждение. |
| Проезд и расходы | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Неправильный промежуточный утверждающий используется, когда вы удаляете промежуточного утверждающего, а затем повторно отправляете отчет о расходах через рабочий процесс. |
| Проезд и расходы | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Возникает ошибка разноски, связанная с настройкой вехи. |