---
title: Журнал интеграции в Project Operations
description: Эта тема предоставляет информацию о работе с журналом интеграции в Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ffe3373184c8cd776bf3705fd674bedf221d9b77
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4133426"
---
# <a name="integration-journal-in-project-operations"></a>Журнал интеграции в Project Operations

_**Относится к:** Project Operations для сценариев на основе ресурсов/без запасов_

Записи о времени и расходах создают транзакции **Фактически**, которые представляют собой операционное представление работы, выполненной по проекту. Dynamics 365 Project Operations предоставляет бухгалтерам инструмент для проверки транзакций и корректировки атрибутов учета по мере необходимости. После завершения проверки и корректировок проводки разносятся во вспомогательную книгу проекта и главную книгу. Бухгалтер может выполнять эти действия, используя журнал **Интеграция Project Operations** (**Dynamics 365 Finance** > **Управление и учет по проектам** > **Журналы** > журнал **Интеграция Project Operations**).

![Поток журнала интеграции](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Создание записей в журнале интеграции Project Operations

Записи в журнале интеграции Project Operations создаются с использованием периодического процесса **Импорт из промежуточной таблицы**. Вы можете запустить этот процесс, перейдя в раздел **Dynamics 365 Finance** > **Управление и учет по проектам** > **Периодические операции** > **Интеграция Project Operations** > **Импорт из промежуточной таблицы**. Вы можете запустить процесс в интерактивном режиме или настроить его для работы в фоновом режиме, как требуется.

При запуске периодического процесса обнаруживаются все фактические данные, которые еще не добавлены в журнал интеграции Project Operations. Создается строка журнала для каждой фактической транзакции.
Система группирует строки журнала в отдельные журналы на основе значения, выбранного в поле **Единица измерения периода в журнале интеграции Project Operations** (вкладка **Finance** > **Управление и учет по проектам** > **Настройка** > **Параметры управления и учета по проектам**, **Project Operations в Dynamics 365 Customer Engagement**). Возможные значения для этого поля:

  - _*Дни**: фактические данные сгруппированы по дате транзакции. На каждый день создается отдельный журнал.
  - **Месяцы**: фактические данные сгруппированы по календарным месяцам. На каждый месяц создается отдельный журнал.
  - **Годы**: фактические данные сгруппированы по календарным годам. На каждый год создается отдельный журнал.
  - **Все**: все фактические транзакции включаются в один журнал интеграции. Если журнал недоступен во время выполнения периодического процесса, например, если журнал находится в процессе разноски транзакций, создается новый журнал.

Строки журнала создаются на основе фактических данных по проекту. Следующий список включает некоторые из наиболее примечательных правил по умолчанию и правил преобразования:

  - Каждая фактическая транзакция проекта имеет строку в журнале интеграции Project Operations. Себестоимость и операции продажи, за которые не выставлены счета, для типа выставления счетов по времени и материалам показаны в отдельных строках.
  - Поле **Дата** представляет дату транзакции. Поле **Дата отчетности** представляет дату, когда транзакция записана в книгу учета. Если дата отчетности приходится на [закрытый финансовый период](https://docs.microsoft.com/dynamics365/finance/general-ledger/close-general-ledger-at-period-end), а параметр **Автоматически устанавливать дату учета равной периоду открытия ГК** установлен на вкладке **Финансы** страницы **Параметры управления и учета по проектам**, система скорректирует дату учета транзакции на первую дату в следующем открытом периоде книги учета.
  - В поле **Ваучер** отображается номер ваучера для каждой фактической транзакции. Последовательность номеров ваучеров определяется на вкладке **Номерные последовательности** на странице **Параметры управления и учета по проектам**. Каждой строке присваивается новый номер. После разноски ваучера вы можете просмотреть, как связаны затраты и транзакции продажи, по которым не выставлены счета, выбрав **Связанные ваучеры** на странице **Проводка ваучера**.
  - Поле **Категория** представляет транзакцию проекта и значения по умолчанию, основанные на категории транзакции для связанных фактических данных проекта.
    - Если **Категория транзакции** устанавливается в фактических данных проекта и связанная **Категория проекта** существует в данном юридическом лице, категория по умолчанию соответствует этой категории проекта.
    - Если **Категория транзакции** не задана в фактических данных проекта, система использует значение в поле **Значения по умолчанию для категории проекта** на вкладке **Project Operations в Dynamics 365 Customer Engagement** на странице **Параметры управления и учета по проектам**.
  - Поле **Ресурс** представляет ресурс проекта, связанный с этой транзакцией. Ресурс используется в качестве ссылки в предложениях по счетам проекта для клиентов.
  - Поле **Обменный курс** по умолчанию устанавливается из значения **Курс валюты** в Dynamics 365 Finance. Если настройка обменного курса отсутствует, периодический процесс **Импорт из промежуточной таблицы** не будет добавлять запись в журнал, а в журнал выполнения задания будет добавлено сообщение об ошибке.
  - Поле **Свойство строки** представляет тип выставления счетов в фактических данных по проекту. Сопоставление свойств строки и типа выставления счетов определяется на вкладке **Project Operations в Dynamics 365 Customer Engagement** на странице **Параметры управления и учета по проектам**.

В строках журнала интеграции Project Operations можно обновить только следующие атрибуты учета:

- **Налоговая группа выставления счетов** и **Налоговая группа номенклатур выставления счетов**
- **Финансовые аналитики** (с использованием действия **Распределить суммы**)

Строки журнала интеграции можно удалить, однако любые неопубликованные строки будут снова вставлены в журнал после повторного запуска периодического процесса **Импорт из промежуточной таблицы**.

При разноске журнала интеграции создаются проводки вспомогательной книги проекта и главной книги. Они используются для последующего выставления счетов клиентам, признания выручки и финансовой отчетности.