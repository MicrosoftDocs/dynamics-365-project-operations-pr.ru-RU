---
title: Бизнес-проводки в Project Operations
description: В этой теме приведен обзор концепции бизнес-проводок в Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 01/31/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2022-01-31
ms.openlocfilehash: 0c6fe583af0dcaa62204b35c1093746b13b6e00e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582220"
---
# <a name="business-transactions-in-project-operations"></a>Бизнес-проводки в Project Operations

_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_

В Microsoft Dynamics 365 Project Operations *бизнес-проводка* — это абстрактная концепция, которая не представлена никакой сущностью. Однако некоторые общие поля и процессы в сущностях предназначены для использования концепции бизнес-транзакций. Следующие сущности используют эту абстракции:

- Сведения строки предложения с расценками
- Сведения строки контракта
- Строки оценки
- Сроки журнала
- Фактические

Из этих сущностей "Сведения строки предложения с расценками", "Сведения строки контракта" и "Строки оценки" сопоставляются с *этапом оценки* в жизненном цикле проекта. Сущности "Строки журнала" и "Фактические значения" сопоставляются с *этапом выполнения* в жизненном цикле проекта.

Project Operations рассматривает записи во всех пяти этих сущностях как бизнес-проводки. Единственное отличие заключается в том, что записи в сущностях, которые сопоставляются с этапом оценки ("Сведения строки предложения с расценками", "Сведения строки контракта" и "Строки оценки"), считаются *финансовыми прогнозами*, а записи в сущностях, которые сопоставляются с этапом выполнения ("Строки журнала" и "Фактические значения"), считаются *финансовыми фактами*, которые уже имели место.

Чтобы получить дополнительные сведения, см. разделы [Оценки](../project-management/estimating-projects-overview.md) и [Фактические данные](actuals-overview.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Основные понятия, уникальные для деловых операций

Следующие основные понятия уникальны для концепции деловых операций:

- Тип проводки
- Класс проводки
- Происхождение проводки
- Подключение проводки

### <a name="transaction-type"></a>Тип проводки

Тип транзакции представляет время и контекст финансового влияния на проект. Он определяется набором параметров, который имеет следующие поддерживаемые значения в Project Operations:

- Себестоимость
- Контракт проекта
- Продажи без выставления счета
- Продажи с выставлением счета
- Внутрихолдинговые продажи
- Стоимость единицы распределения ресурсов

### <a name="transaction-class"></a>Класс проводки

Класс транзакции представляет различные типы затрат, понесенных по проектам. Он определяется набором параметров, который имеет следующие поддерживаемые значения в Project Operations:

- Время
- Расходы
- Материал
- Сбор
- Веха
- Налог

> [!NOTE]
> Значение **Веха** обычно используется бизнес-логикой для выставления счетов с фиксированной ценой в Project Operations.

### <a name="transaction-origin"></a>Происхождение проводки

Происхождение проводки — это сущность, в которой хранится источник каждой бизнес-проводки для целей отчетности и прослеживаемости. Когда начинается выполнение проекта, каждая бизнес-проводка создает другую бизнес-проводку, которая, в свою очередь, создает еще одну бизнес-проводку и так далее.

### <a name="transaction-connection"></a>Подключение проводки

Подключение проводок — это сущность, в которой хранится отношение между двумя похожими бизнес-проводками, такими как фактическое значение стоимости и связанное фактическое значение продаж или сторнирования проводок, запускаемые действиями по выставлению счетов, такими как подтверждение счета или внесение исправлений в счет.

Вместе сущности "Происхождение проводки" и "Подключение проводки" помогают отслеживать отношения между бизнес-проводками и действиями, которые вызвали создание определенной бизнес-проводки.

[!INCLUDE[footer-include](../includes/footer-banner.md)]