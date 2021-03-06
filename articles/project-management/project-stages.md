---
title: Стадии проекта
description: Эта тема предоставляет информацию об этапах проекта, которые доступны в Microsoft Dynamics Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: b11c67ebd21fdf423eeae2db8154f26787c2e64f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897962"
---
# <a name="project-stages"></a>Стадии проекта

_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_

Стадии проекта создаются с целью отражения статуса проекта в ходе его выполнения. Настройки могут использоваться для автоматического обновления стадий для включения сведений о потоках бизнес-процесса, Power Automate или расширений подключаемых модулей.

Следующие этапы определены в потоке бизнес-процесса по умолчанию:

- Новая
- Предложение с расценками
- План
- Доставка
- Завершить
- Закрыть 

## <a name="new"></a>Новая

При создании проекта стадия проекта задается как **Создать**. Если проект был создан из шаблона, он может иметь расписание, оценку и данные рабочей группы. В противном случае это схема проекта, остальные компоненты необходимо ввести.

## <a name="quote"></a>Предложение с расценками

При связывании проекта с предложением с расценками или при создании проекта из предложения с расценками стадия проекта задана как **Предложение с расценками**, и также обновляются расчетные даты начала и окончания. Пока проект находится на стадии **Предложение с расценками**, сведения по предложению с расценками отображаются на вкладке **Продажи** на странице **Сущность проекта**.

## <a name="plan"></a>Планирование

При выигрыше предложения с расценками, связанного с проектом, проект переходит на этап **Контракт**, стадия проекта обновляется на **План**. Пока проект находится на стадии **План**, на странице **Сущность проекта** отображаются сведения о контракте.

## <a name="deliver"></a>Доставка

Когда планирование проекта завершено, и все готово для запуска проекта, руководитель проекта должен обновить стадию проекта на **Доставка** для отображения того, что проект начался.

## <a name="complete"></a>Завершено 

Когда работа по проекту выполнена, руководитель проекта может обновить стадию на **Завершено**. Путем обновления стадии проекта на **Завершено** руководитель проекта указывает, что работа на 100 процентов завершена, но проект остается открытым, чтобы можно было зарегистрировать все ожидающие записи времени или расходов.

## <a name="close"></a>Закрытие

Когда все транзакции зафиксированы для проекта, руководитель проекта может обновить стадию на **Закрыт**. В этот момент никакие транзакции невозможно зафиксировать, и проект становится доступен только для чтения.

