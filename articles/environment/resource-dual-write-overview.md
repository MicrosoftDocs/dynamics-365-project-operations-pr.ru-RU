---
title: Интеграция с двойной записью Project Operations
description: В этом разделе представлен обзор интеграции с двойной записью Project Operations.
author: sigitac
ms.date: 04/28/2021
ms.topic: overview
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 9b57b8bab9a6821e71a16b191804af21ae5d0b5a
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582772"
---
# <a name="project-operations-dual-write-integration-overview"></a>Обзор интеграции с двойной записью Project Operations

_**Относится к:** Project Operations для сценариев на основе ресурсов/без запасов_

Project Operations использует [возможности двойной записи](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) для синхронизации данных в Microsoft Dataverse и Dynamics 365 Finance.

На следующем рисунке показано, как данные синхронизируются в рамках этой интеграции между Dataverse и Финансы.

![Обзор потоков данных Project Operations.](./media/ProjectOperationsFlows.jpg)

Project Operations на Dataverse предоставляет современный пользовательский интерфейс и простую расширяемость без кода/с минимумом кода, используя возможности Power Platform. Руководители проектов, менеджеры ресурсов, участники проектных групп и другие сотрудники, непосредственно взаимодействующие с клиентами, выполняют свои действия в Project Operations на Dataverse.

Project Operations в Финансы обеспечивает учет проектов и поддержку признания выручки. Project Operations подключается к финансовой платформе в Финансы для расчета налога, курсов обмена валют, отчетности по финансовым аналитикам и многого другого. Опыт бухгалтеров по проектам в основном основан на Финансах.

Интеграция Project Operations состоит из следующих компонентов:


- [Настройка Project Operations и интеграция данных конфигурации](resource-dual-write-setup-integration.md) 
- [Оценки проекта и фактические данные](resource-dual-write-estimates-actuals.md)
- [Счета проекта](resource-dual-write-project-invoice.md)
- [Управление расходами](resource-dual-write-expense.md)
- [Накладная поставщика](resource-dual-write-vendor-invoice.md)
