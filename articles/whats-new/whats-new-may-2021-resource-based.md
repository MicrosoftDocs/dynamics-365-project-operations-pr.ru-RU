---
title: Новые возможности, май 2021 — Project Operations для сценариев на основе ресурсов/без запасов
description: В этой теме содержится информация об обновлениях качества, доступных в выпуске Project Operations за май 2021 года, для сценариев на основе ресурсов/без запасов.
author: sigitac
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 07ae18faef6acb9d64b889bbfdba89de0c96a453
ms.sourcegitcommit: d48dce64f6c5b16db3250096715c9d9f92a81971
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/20/2021
ms.locfileid: "6083942"
---
# <a name="whats-new-may-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Новые возможности, май 2021 — Project Operations для сценариев на основе ресурсов/без запасов

_**Относится к:** Project Operations для сценариев на основе ресурсов/без запасов_

Эта тема применяется к следующим компонентам и версиям Dynamics 365 Project Operations:

- Project Operations в среде Dynamics 365 Dataverse версии 4.10.0.186
- Управление проектами и учет в приложениях среды Finance and Operations версии 10.0.18

## <a name="features-included-in-this-release"></a>Функции, входящие в данный выпуск

В состав этого выпуска входят следующие функции:

- [Режимы планирования](../project-management/scheduling-modes.md): менеджеры проектов могут определять, следует ли управлять проектом, используя режим планирования с фиксированной продолжительностью, фиксированными трудозатратами или фиксированными единицами.
- [Настройка расстояния с использованием ставки за проделанное расстояние](../expense/set-up-mileage.md): обновлять уровни нормы пробега для отчетов о расходах сотрудников.

## <a name="project-operations-dual-write-maps-updates"></a>Обновления сопоставления с двойной записью Project Operations

В следующем списке показаны сопоставления с двойной записью, которые были изменены или добавлены в выпуск Project Operations от мая 2021 года.

| Сопоставление сущностей | Обновленная версия | Комментарии |
| --- | --- | --- |
| Источник финансирования проекта (msdyn\_projectcontractsplitbillingrules) | 1.0.0.2 | Синхронизация условий оплаты клиента контракта по проекту. |
| Предложение по счетам по проекту V2 (счета) | 1.0.0.3 | Синхронизация условий оплаты счёта-проформы. |
| Сущность экспорта строки накладной поставщика проекта интеграции Project Operations (msdyn\_projectvendorinvoicelines) | 1.0.0.1 | Обновления качества |
| Проекты V2 (msdyn\_projects) | 1.0.0.2 | Обновления качества |

Всегда следует запускать последнюю версию сопоставления в своей среде и включать все связанные сопоставления таблиц при обновлении решения Project Operations Dataverse и версии решения приложений Finance and Operations. Некоторые функции и возможности могут работать некорректно, если не активирована последняя версия сопоставления. Вы можете увидеть активную версию сопоставления в столбце **Версия** на странице **Двойная запись**. Чтобы активировать новую версию сопоставления, выберите **Версии сопоставления таблиц**, выберите последнюю версию, а затем сохраните выбранную версию. Если вы настроили готовое сопоставление таблицы, повторно примените изменения. Дополнительные сведения см. в [Управление жизненным циклом приложений](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management.md).

Если вы столкнулись с проблемой при запуске сопоставления, следуйте инструкциям в разделе [Проблема с отсутствующими столбцами таблицы на сопоставлениях](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades.md#missing-table-columns-issue-on-maps) в руководстве по устранению неполадок с двойной записью.

## <a name="quality-updates"></a>Обновления качества

### <a name="project-operations-on-dataverse"></a>Project Operations на Dataverse

| **Область функций** | **Номер ссылки** | **Обновление качества** |
| --- | --- | --- |
| Выставление счетов и цены | 2227635 | Значения в полях **Группа единиц измерения** и **Единица измерения** берутся по умолчанию из продукта в сетке **Оценки материалов**. |
| Выставление счетов и цены | 2234127 | Поле **ИД задачи** теперь правильно интегрируется с фактические данными по проекту Dataverse при разноске накладной поставщика. |
| Выставление счетов и цены | 2235564 | Сохранение строки журнала гарантирует, что валюта, отображаемая в записи строки журнала, соответствует валюте строки по умолчанию после сохранения. |
| Выставление счетов и цены | 2246671 | Если сделать транзакцию неоплачиваемой во время выставления счета-фактуры, исходная запись о продажах без выставления счетов будет сторнирована и будет создана новая запись о продажах, по которой не выставлен счет. |
| Выставление счетов и цены | 2264042 | Правильное исправление счета-фактуры не должно блокироваться, если есть сведения исправления счета-фактуры, недопустимые в среде. |
| Выставление счетов и цены | 2146367 | Сопоставление двойной записи заголовка счета-фактуры проекта расширено и теперь включает условия оплаты. |
|   Управление возможными сделками | 2086888 | Не добавляйте деактивированные роли и категории перед копированием предложения с расценками в оплачиваемые роли и категории вновь скопированного предложения с расценками. |
|   Управление возможными сделками | 2234376 | Поля только для чтения затенены в сетке **Оценки материалов**. |
|   Управление возможными сделками | 2238337 | Предложение с расценками на основе контакта можно сохранить, даже если оно не связана с прайс-листом проекта. |
|   Управление возможными сделками | 2239810 | Закрытие предложения с расценками как потерянного также закрывает связанный проект и отменяет все бронирования. |
| Планирование и отслеживание проектов | 2099559 | Добавлены дополнительные проверки работоспособности системы перед открытием сетки **Задачи проекта**. |
| Планирование и отслеживание проектов | 2178987 | Исправлена временная ошибка, возникающая при выборе **Следующий этап** на странице **Проект**. |
| Управление ресурсами | 2224817 | Функциональность для расширения резервирования по умолчанию имеет правильный статус бронирования. |
| Запись времени | 2202476 | На странице **Запись времени** теперь используется элемент управления сеткой реагирования и исправлены такие проблемы, как несовпадение сетки. |
| Запись времени | 2223377 | Запись времени скрыта из раздела **Связанный** на странице **Резервируемый ресурс**, чтобы избежать путаницы с удобством использования. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Управление и учет по проектам в Dynamics 365 Finance

| Область функций | Номер ссылки | Обновление качества |
| --- | --- | --- |
| Управление и учет по проектам | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | В Project Operations для сценариев на основе ресурсов: из-за ошибки интеграции невозможно преобразовать предложение с расценками в выигранное предложение. |
| Управление и учет по проектам | [546604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546604) | В Project Operations: ошибка возникает при попытке связать строку контракта с идентификатором проекта из-за проверки перекрытия строк контракта и типов транзакций. |
| Управление и учет по проектам | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** задает адрес счета источника финансирования от другого клиента. |
| Проезд и расходы | [480451](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480451) | Может произойти ошибка разноски, связанная с настройкой пробега. |
| Проезд и расходы | [522084](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522084) | Функция **Разделить на личные** для транзакций расходов в иностранной валюте не работает. |
| Проезд и расходы | [523938](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523938) | В раскрывающемся меню категории расходов отображаются неправильные категории независимо от того, настроены ли представители как ресурс. |
| Проезд и расходы | [539266](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539266) | Вы не можете сохранить отчет о расходах внутри компании из-за ошибки **Проверка ресурса/категории**. |
| Проезд и расходы | [532610](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532610) | Неправильный расчет нормы пробега в разноске отчета о расходах имеет разделенные строки. |
| Проезд и расходы | [537404](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537404) | Вы не можете разнести отчет о расходах внутри компании, если налог включен, а тип счета смещения в методе оплаты — **Рабочая роль** . |
| Проезд и расходы | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | Откат сущности данных **TrvRequisitionLine** и связанного уникального индекса. |
| Проезд и расходы | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | Отчет о расходах поддерживает создание и обновление строки исходного документа. |
| Проезд и расходы | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | Показан неправильный журнал субкниги во внутрихолдинговом сценарии, если налог с продаж разносится на целевое юридическое лицо. |
| Проезд и расходы | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | В Project Operations: оценка расходов не удаляется из Finance, когда она удаляется из Dataverse. |
| Проезд и расходы | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | Если категория расходов не относится к категории проектов, финансовые аналитики, выбранные на странице **Расходы** не копируется в отчет о расходах. |