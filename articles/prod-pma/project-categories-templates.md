---
title: Синхронизация категорий расходов проекта между приложениями для управления финансами и операциями и Project Service Automation
description: В этой статье рассматриваются шаблоны и базовые задачи, которые используются для синхронизации категорий расходов проекта между Microsoft Dynamics 365 Finance и Dynamics 365 Project Service Automation.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 8eba7defb93bd880db4b0e8fe425d07312cf5cb9
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028948"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>Синхронизация категорий расходов проекта между приложениями для управления финансами и операциями и Project Service Automation

[!include[banner](../includes/banner.md)]

В этой статье рассматриваются шаблоны и базовые задачи, которые используются для синхронизации категорий расходов проекта между Dynamics 365 Finance и Dynamics 365 Project Service Automation.

> [!NOTE]
> - Интеграция задач проекта, категории транзакций расходов, оценки часов, оценки расходов и блокировка функций доступны в версии 8.0.
> - Интеграция фактических данных по проекту доступна в версии 8.0.1 и последующих версиях.
> - Если вы используете версию Enterprise Edition 7.3.0 после установки KB 4132657 и KB 4132660, вы сможете использовать шаблоны для интеграции задач проекта, категорий транзакций расходов, часовых оценок, оценок расходов и фактических данных, а также для настройки блокировки функций. Если вам необходимо сбросить распределения по счетам, мы рекомендуем также установить KB 4131710.

## <a name="data-flow-for-project-service-automation-and-finance"></a>Поток данных для Project Service Automation и Finance

Решение для интеграции Project Service Automation и Finance использует функцию интеграции данных для синхронизации данных между экземплярами Project Service Automation и Finance. Шаблоны интеграции, доступные с функцией интеграции данных, позволяют передавать данные о категориях транзакций по расходам проекта между Finance и Project Service Automation.

Если категории расходов по проекту заданы в Finance, сначала выполняется интеграция из Finance в Project Service Automation. Затем идентификаторы интеграции категорий расходов проекта обновляются посредством синхронизации из Project Service Automation в Finance.

Если категории расходов по проекту заданы в Project Service Automation, сначала выполняется интеграция из Project Service Automation в Finance. Категории проектов должны быть уже настроены в Finance перед синхронизацией из Project Service Automation. Затем выполните синхронизацию из Finance обратно в Project Service Automation, а затем из Project Service Automation снова в Finance. Таким образом, вы гарантируете, что категории связаны и что дубликаты не будут созданы.

> [!NOTE]
> Обычно категории расходов по проекту управляются в Finance. Однако, если это не так или если категории расходов уже были созданы в Project Service Automation, необходимо сначала выполнить синхронизацию с помощью шаблона категорий транзакций расходов проекта (из PSA в Fin and Ops). Затем выполните синхронизацию с помощью шаблона категорий расходов по проекту (из Fin and Ops в PSA). Затем вам следует запустить синхронизацию из Project Service Automation в Finance еще раз.
>
> Если вы сначала выполняете синхронизацию из Project Service Automation, перед запуском синхронизации в Finance должны быть выполнены следующие требования:
>
> - Общая категория, соответствующая категории проекта, настроенной в Project Service Automation, должна существовать, и она должна быть включена для обоих **Проект** и **Расходы**.
> - Для каждого юридического лица Finance, с которым необходимо выполнить интеграцию, должны существовать следующие категории проектов:
>
>     - **Категория проекта** существует. 
>     - **Использование в расходах** включено.
>     - **Активно в журнале** включено.
>     - **Тип операции** задано как **Расходы**.

На следующем рисунке показано, как данные синхронизируются между Project Service Automation и Finance.

[![Поток данных для интеграции Project Service Automation с Finance.](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a>Синхронизация категорий расходов по проекту между из Finance в Project Service Automation

### <a name="template-and-task"></a>Шаблон и задача

Чтобы получить доступ к шаблону, в центре администрирования Microsoft Power Apps выберите **Проекты**, а затем в правом верхнем углу выберите **Создать проект** для выбора общедоступных шаблонов.

Следующий шаблон и базовая задача используются для синхронизации категорий расходов по проекту из Finance в Project Service Automation:

- **Название шаблона в интеграции данных:** Категории транзакций расходов по проекту (из Fin and Ops в PSA)
- **Название задачи в проекте:** синхронизировать категории с PSA

### <a name="entity-set"></a>Набор сущностей

| Финансы                           | Project Service Automation |
|-----------------------------------|----------------------------|
| Сущность интеграции для категорий | Категории транзакций     |

### <a name="entity-flow"></a>Поток сущностей

Категории расходов по проекту управляются в Finance и синхронизируются с Project Service Automation как категории транзакций.

### <a name="power-query"></a>Power Query

При синхронизации в Project Service Automation необходимо использовать Microsoft Power Query для Excel, чтобы настроить тип выставления счетов для категории проводки. В шаблоне категорий транзакций расходов по проекту (из Fin and Ops в PSA) есть столбец и сопоставление по умолчанию. При создании собственного шаблона необходимо добавить в Power Query условный столбец. Выполните следующие действия.

1. Щелкните стрелку, чтобы открыть сопоставление задачи категорий расходов проекта в шаблоне категорий транзакций расходов проекта (из Fin and Ops в PSA).
2. Щелкните ссылку **Расширенный запрос и фильтрация**, чтобы открыть Power Query.
2. Выберите **Добавить условный столбец**.
3. Введите имя для нового столбца, например **BillingType**.
4. Введите следующее условие: **если CATEGORYID не равно нулю, то 19235001, в противном случае null**.
5. Нажмите **ОК** в столбце.
6. Обязательно сопоставьте этот новый столбец на странице сопоставления.

На следующих рисунках показан пример сопоставления задач шаблона в интеграции данных. В сопоставлении отображается информация о полях, которые будут синхронизированы из Finance в Project Service Automation.

[![Сопоставление категорий расходов по проекту с шаблоном Project Service Automation.](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a>Синхронизация категорий расходов по проекту между из Project Service Automation в Finance

### <a name="template-and-task"></a>Шаблон и задача

Следующий шаблон и базовая задача используются для синхронизации категорий расходов по проекту из Project Service Automation в Finance:

- **Название шаблона в интеграции данных:** Категории транзакций расходов по проекту (из PSA в Fin and Ops)
- **Название задачи в проекте:** синхронизировать категории с Fin Ops

### <a name="entity-set"></a>Набор сущностей

| Project Service Automation | Финансы                           |
|----------------------------|-----------------------------------|
| Категории транзакций     | Сущность интеграции для категорий |

### <a name="entity-flow"></a>Поток сущностей

Категории расходов по проекту управляются в Finance и синхронизируются с Project Service Automation как категории транзакций. При синхронизации обратно с Finance обновляется категория проекта в Finance с кодом интеграции из Project Service Automation.

### <a name="template-mapping-in-data-integration"></a>Сопоставление шаблонов в интеграции данных

На следующих рисунках показан пример сопоставления задач шаблона в интеграции данных.

> [!NOTE]
> В сопоставлении отображается информация о полях, которые будут синхронизированы из Project Service Automation в Finance.

[![Сопоставление Project Service Automation с шаблоном Finance.](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]