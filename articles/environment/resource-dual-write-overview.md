---
title: Интеграция с двойной записью Project Operations
description: В этом разделе представлен обзор интеграции с двойной записью Project Operations.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: b65c40e8aaa9524c1c634738dadd23f21e86e2ec095c47bc849467c8806addbc
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007927"
---
# <a name="project-operations-dual-write-integration-overview"></a>Обзор интеграции с двойной записью Project Operations

_**Относится к:** Project Operations для сценариев на основе ресурсов/без запасов_

Project Operations использует [возможности двойной записи](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page), чтобы синхронизировать данные между Microsoft Dataverse и Dynamics 365 Finance.

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
