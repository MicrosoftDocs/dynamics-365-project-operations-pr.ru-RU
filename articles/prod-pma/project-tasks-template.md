---
title: Синхронизация задач по проекту напрямую из Project Service Automation в приложения для управления финансами и операциями
description: В этой статье рассматривается шаблон и базовая задача, которая используется для синхронизации задач по проекту непосредственно из Microsoft Dynamics 365 Project Service Automation в Dynamics 365 Finance.
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
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: ed559fcd9e0e666f68e7d9f4f1fca91417fe4970
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028377"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a>Синхронизация задач по проекту напрямую из Project Service Automation в приложения для управления финансами и операциями

[!include[banner](../includes/banner.md)]

В этой статье рассматривается шаблон и базовая задача, которая используется для синхронизации задач по проекту непосредственно из Dynamics 365 Project Service Automation в Dynamics 365 Finance.

> [!NOTE]
> - Интеграция задач проекта, категории транзакций расходов, оценки часов, оценки расходов и блокировка функций доступны в версии 8.0.
> - Если вы используете версию Enterprise Edition 7.3.0 после установки KB 4132657 и KB 4132660, вы сможете использовать шаблоны для интеграции задач проекта, категорий транзакций расходов, часовых оценок, оценок расходов и фактических данных, а также для настройки блокировки функций. Если вам необходимо сбросить распределения по счетам, мы рекомендуем также установить KB 4131710.
> - Интеграция фактических данных по проекту доступна в версии 8.0.1 и последующих версиях.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Поток данных для Project Service Automation в Finance

Решение для интеграции Project Service Automation в Finance использует функцию интеграции данных для синхронизации данных между экземплярами Project Service Automation и Finance. Шаблон интеграции, доступный с функцией интеграции данных, позволяет передавать данные о задачах проекта из Project Service Automation в Finance.

На следующем рисунке показано, как данные синхронизируются между Project Service Automation и Finance.

[![Поток данных для интеграции Project Service Automation с Finance.](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>Шаблон и задача

Чтобы получить доступ к шаблону, в центре администрирования Microsoft Power Apps выберите **Проекты**, а затем в правом верхнем углу выберите **Создать проект** для выбора общедоступных шаблонов.

Следующий шаблон и базовая задача используются для синхронизации задач проекта из Project Service Automation в Finance:

- **Название шаблона в интеграции данных:** задачи проекта (из PSA в Fin and Ops)
- **Название задачи в проекте:** задачи проекта

Перед синхронизацией задач проекта вы должны синхронизировать контракты и проекты.

## <a name="entity-set"></a>Набор сущностей

| Project Service Automation | Финансы                             |
|----------------------------|-------------------------------------|
| Задачи проекта              | Сущность интеграции для задачи проекта |

## <a name="entity-flow"></a>Поток сущностей

Задачи проекта управляются в Project Service Automation и синхронизируются с Finance как действия проекта.

## <a name="prerequisites-and-mapping-setup"></a>Предварительные условия и настройка сопоставления

Перед синхронизацией задач проекта вы должны синхронизировать контракты и проекты.

## <a name="power-query"></a>Power Query

Необходимо использовать Microsoft Power Query для Excel для фильтрации данных, если выполняется следующее условие:

- У вас есть записи о конкретных ресурсах в задаче проекта.

При использовании Power Query необходимо придерживаться следующего правила:

- В шаблоне задач проекта (из PSA в Fin and Ops) есть фильтр по умолчанию, который исключает связанные с ресурсами записи из задачи проекта, устанавливая фильтр для **IsLineTask** как **False**. Если вы создаете свой собственный шаблон, вы должны добавить этот фильтр.

## <a name="template-mapping-in-data-integration"></a>Сопоставление шаблонов в интеграции данных

На следующих рисунках показан пример сопоставления задач шаблона в интеграции данных. В сопоставлении отображается информация о полях, которые будут синхронизированы из Project Service Automation в Finance.

[![Сопоставление шаблонов.](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]