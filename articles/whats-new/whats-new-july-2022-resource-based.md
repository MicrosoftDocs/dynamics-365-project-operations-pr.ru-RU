---
title: Новые возможности в июле 2022 года — Project Operations для сценариев на основе ресурсов/без запасов
description: В этой статье содержится информация об исправлениях, доступных в выпуске Microsoft Dynamics 365 Project Operations для сценариев на основе ресурсов/без запасов за июль 2022 года.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: e63b29741dbaa400a2176ff8b4c35c6d64dfeab4
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403968"
---
# <a name="whats-new-july-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Новые возможности в июле 2022 года — Project Operations для сценариев на основе ресурсов/без запасов

_**Относится к:** Project Operations для сценариев на основе ресурсов/без запасов_

Эта статья применяется к следующим компонентам и версиям Microsoft Dynamics 365 Project Operations:

- Project Operations в среде Dataverse версии 4.44.0.22
- Управление и учет по проектам в среде Dynamics 365 Finance версии 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Обновления сопоставления с двойной записью Project Operations

В этом выпуске нет обновлений для карт Project Operations с двойной записью. Для получения информации о текущем списке и версиях карт с двойной записью Project Operations см. [Версии карты с двойной записью Project Operations](../environment/resource-dual-write-maps.md).

Всегда запускайте последнюю версию сопоставления в своей среде и включайте все связанные карты таблиц при обновлении решения Project Operations Dataverse и версии решения Finance. Некоторые функции и возможности могут работать некорректно, если не активирована последняя версия сопоставления. Вы можете увидеть активную версию сопоставления в столбце **Версия** на странице **Двойная запись**. Чтобы активировать новую версию сопоставления, выберите **Версии сопоставления таблиц**, выберите последнюю версию, а затем сохраните выбранную версию. Если вы настроили стандартное сопоставление таблиц, примените изменения повторно. Дополнительные сведения см. в [Управление жизненным циклом приложений](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Если вы столкнулись с проблемой при запуске сопоставления, следуйте инструкциям в разделе [В картах отсутствуют столбцы таблицы](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) в руководстве по устранению неполадок с двойной записью.

## <a name="quality-updates"></a>Обновления качества

### <a name="project-operations-on-dataverse"></a>Project Operations на Dataverse

| Область функций | Номер ссылки | Обновление качества |
| --- | --- | --- |
| Развертывание и конфигурация | 2761472 | Исправлена ошибка установки Project Operations. |
| Выставление счетов и цены | 2746940 | Длина имени строки субподряда не должна превышать 100 символов. |
| Выставление счетов и цены | 2739162 | Клиенты должны иметь возможность видеть кнопки ленты в представлении сетки фактических данных. |
| Планирование и отслеживание проектов | 2730318 | Обновлена проверка неподдерживаемых символов в теме проекта. |
| Выставление счетов и цены | 2705361 | Фактические данные о продажах с выставленными счетами для вехи, должны быть включены в поля отслеживания проекта. |
| Выставление счетов и цены | 2675880 | Не допускайте привязки проекта к строке контракта, не связанной с работой. |
| Выставление счетов и цены | 2664396 | Если прайс-лист предложения сохраняется без предложения с расценками, должна появиться ошибка, указывающая, что предложение с расценками не может быть пустым. |
| Выставление счетов и цены | 2184019 | Вкладка **Выставление счетов по задачам** не должна отображаться для проектов, у которых нет соответствующего контракта или предложения с расценками. |
| Время и расходы | 2754459 | Когда повторяющийся облачный поток планирования неактивен, показывать баннер и обходить асинхронную обработку. |
| Выставление счетов и цены | 2724391 | При отсутствии значения клиента в правиле выставления счетов с разбиением по контрактам по проектам возникает неправильное исключение. |
| Выставление счетов и цены | 2708638 | При поиске с использованием поиска в сетке в использованиях материала и утверждениях использования материала не удавалось найти запись.|
| Выставление счетов и цены | 2686977 | Запрет проверки строки счета во время создания счета. |
| Выставление счетов и цены | 2683032 | Копирование оплачиваемых ролей и категорий не масштабировалось свыше 5000 записей.|
| Выставление счетов и цены | 2673363 | При наличии для проекта сметных и фактических значений трудозатрат и расходов значение "Использование стоимости, %" в проекте оказывалось поврежденным. |

### <a name="project-management-and-accounting-in-finance"></a>Управление и учет для проектов в Finance

Для получения сведений об исправлениях ошибок, включенных в это обновление, войдите в Microsoft Dynamics Lifecycle Services (LCS) и просмотрите [статью базы знаний](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Функции, включенные по умолчанию в предстоящем выпуске

В этой таблице перечислены функции, включенные по умолчанию в версии 10.0.29. Большинство функций, включенных автоматически, могут быть отключены в [управлении функциями](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). В будущем некоторые функции, которые были включены автоматически, могут быть удалены из раздела управления функциями и могут стать обязательными. Это изменение гарантирует, что клиенты используют актуальные функции, чтобы добавляемые улучшения были основаны на актуальных функциях. Функции никогда не будут автоматически включены раньше, чем через год, если только они не будут признаны ключевыми.

| Имя функции | Дата включения | Функция добавлена | Состояние функции | Модуль |
| --- | --- | --- |--- |--- |
| Включить корректировку почасовой транзакции на основе изменения распределения правил финансирования | 16 сентября 2022 г. | 7 октября 2020 года | Включено по умолчанию | Управление и учет по проектам |
| Функция отмены счета на предоплату для заказа на покупку по проекту | 16 сентября 2022 г. | 6 октября 2021 года | Включено по умолчанию | Управление и учет по проектам |
| Удалять строки предложения по счету при использовании Project Operations для сценариев, основанных на ресурсах или не учитываемых в запасах | 16 сентября 2022 г. | 6 октября 2021 года | Включено по умолчанию | Управление и учет по проектам |
| Настройка учета для разнесенной проводки по проекту | 16 сентября 2022 г. | 10 мая 2020 г. | Включено по умолчанию | Управление и учет по проектам |
| Включить настройку учета по умолчанию для проекта | 16 сентября 2022 г. | 19 февраля 2020 г. | Включено по умолчанию | Управление и учет по проектам |
| Включение нескольких строк контракта для проекта | 16 сентября 2022 г. | 29 июня 2020 г. | Включено по умолчанию | Управление и учет по проектам |
| Сделайте журналы учета часов по проекту доступными только для чтения, если текущий статус утверждения не поддерживает внесение изменений | 16 сентября 2022 г. | 6 октября 2021 года | Включено по умолчанию | Управление и учет по проектам |
| Включить синхронизацию строк продаж со строками покупки, когда строки покупки обновляются и параметр управления изменениями заказа на покупку включен | 16 сентября 2022 г. | 7 октября 2020 года | Включено по умолчанию | Управление и учет по проектам |
| Включение Project Operations в Dynamics 365 Customer Engagement | 16 сентября 2022 г. | 29 июня 2020 г. | Включено по умолчанию | Управление и учет по проектам |
| Функция коррекции сторнирования проводок по проекту | 16 сентября 2022 г. | 13 июля 2020 г. | Включено по умолчанию | Управление и учет по проектам |

## <a name="features-that-become-mandatory-in-the-upcoming-release"></a>Функции, которые станут обязательными в следующем выпуске

В этой таблице перечислены функции, которые станут обязательными, начиная с версии 10.0.29.

| Имя функции | Дата включения | Функция добавлена | Состояние функции | Модуль |
| --- | --- | --- | --- | --- |
| Рассчитать выделенную сумму источника финансирования без округления обменного курса | 16 сентября 2022 г. | 14 июня 2020 г. | Обязательно | Управление и учет по проектам |
| Включить разноску корректировки по проекту с тем же счетом ГК, который использовался для исходной проводки | 16 сентября 2022 г. | 14 июня 2020 г. | Обязательно | Управление и учет по проектам |
| Подробная информация о выделенной сумме контракта по проекту | 16 сентября 2022 г. | 31 августа, 2019 г. | Обязательно | Управление и учет по проектам |
| Включить сортировку по ресурсу во время создания предложения по счету для проекта | 16 сентября 2022 г. | 31 августа, 2019 г. | Обязательно | Управление и учет по проектам |