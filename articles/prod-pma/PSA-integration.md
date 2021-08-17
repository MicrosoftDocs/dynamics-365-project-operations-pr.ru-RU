---
title: Обзор Project Service Automation
description: В этой теме представлена информация о интеграционном решении Dynamics 365 Project Service Automation в Dynamics 365 Finance.
author: ruhercul
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: ruhercul
ms.search.scope: Core, Operations
ms.custom: intro-internal
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 551d511fda83857459a0488cfb48a9c7829171d2e4bd526ab27b4ee74b21910d
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/06/2021
ms.locfileid: "7005902"
---
# <a name="project-service-automation-overview"></a>Обзор Project Service Automation

[!include[banner](../includes/banner.md)]
[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Решение для интеграции Project Service Automation в Finance использует функцию интеграции данных для синхронизации данных между экземплярами Dynamics 365 Finance и Dynamics 365 Project Service Automation через Common Data Service. Шаблоны интеграции, доступные с функцией интеграции данных, обеспечивают потоки проектов, контракты по проектам, строки контрактов по проектам, вехи строк контрактов проекта, задачи проекта категории транзакций расходов, оценки часов и оценки расходов из Project Service Automation в Finance.

> [!NOTE]
> - Если вы используете выпуск версию 7.3.0, вам необходимо установить KB 4074835. После этого вы сможете интегрировать проекты с фиксированной ценой.
> - Если вы используете версию 7.3.0 и переносите транзакции сборов из Project Service Automation, вы должны установить KB 4345320, чтобы включить эти сборы в счет проекта.
> - Если вы используете версию 8.0, вы сможете использовать интеграцию задач проекта, категории транзакций расходов, оценки часов, оценки расходов и блокировку функций.
> - Если вы используете версию 8.0.1 или новее, вы сможете синхронизировать фактические данные.

Прежде чем вы сможете интегрировать Project Service Automation и Finance, вы должны настроить параметры интеграции Project Service Automation. Для получения дополнительной информации см. [Параметры интеграции Project Service Automation](PSA-parameters.md).

Это интеграционное решение обеспечивает прямую синхронизацию в следующих сценариях:

- Поддерживайте контракты по проекту в Project Service Automation и синхронизируйте их напрямую из Project Service Automation в Finance.
- Создавайте проекты в Project Service Automation и синхронизируйте их напрямую из Project Service Automation в Finance.
- Поддерживайте строки контрактов по проекту в Project Service Automation и синхронизируйте их напрямую из Project Service Automation в Finance.
- Поддерживайте вехи строк контрактов по проекту в Project Service Automation и синхронизируйте их напрямую из Project Service Automation в Finance.
- Поддерживайте задачи по проекту в Project Service Automation и синхронизируйте их напрямую из Project Service Automation в Finance.
- Поддерживайте категории транзакций расходов в Finance и синхронизируйте их напрямую из Finance в Project Service Automation.
- Создавайте оценки часов проекта в Project Service Automation и синхронизируйте их напрямую из Project Service Automation в Finance.
- Создавайте оценки расходов проекта в Project Service Automation и синхронизируйте их напрямую из Project Service Automation в Finance.
- Создавайте фактические данные о времени, расходах и вознаграждении по проекту в Project Service Automation, а также создавайте транзакции по проекту в журнале интеграции Project Service Automation, чтобы их можно было разнести в Finance.

## <a name="data-synchronization"></a>Синхронизация данных

На следующем рисунке показано, как данные синхронизируются в рамках интеграции между Project Service Automation и Finance.

> [!NOTE]
> В настоящее время доступны не все шаблоны. Шаблоны будут выпускаться по мере их завершения.

[![Интеграция Project Service Automation с Finance.](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance"></a>Системные требования для Finance

Чтобы использовать решение интеграции Project Service Automation с Finance, необходимо установить выпуск Enterprise Edition 7.3 с обновлением платформы 12 или новее.

## <a name="system-requirements-for-project-service-automation"></a>Системные требования для Project Service Automation

Чтобы использовать решение интеграции Project Service Automation с Finance, необходимо установить следующие компоненты:

- Dynamics 365 Project Service Automation версии 9.0.0.0 или более поздней
- Решение Prospect to Cash для Dynamics 365 Sales, версия 1.14.0.0 (v14) или более поздняя
- Решение Project Service Automation и Finance для Dynamics 365 Project Service Automation версии 1.0.0.0 или более поздняя

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a>Установите решение интеграции Project Service Automation с Finance в свой экземпляр Project Service Automation

Загрузите решение для интеграции Project Service Automation с Finance из [Центра загрузки Microsoft](https://www.microsoft.com/download/details.aspx?id=57016) и следуйте инструкциям, прилагаемым к решению.


[!INCLUDE[footer-include](../includes/footer-banner.md)]