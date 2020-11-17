---
title: Типы стадий проекта
description: В этом разделе представлена информация о стадиях проекта.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 06/19/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 521bf4b3090473a603626a99fded53906b644a7a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083239"
---
# <a name="project-stage-types"></a>Типы стадий проекта 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Стадии проекта создаются с целью отражения статуса проекта в ходе его выполнения. Настройки могут использоваться для автоматического обновления стадий для включения сведений о потоках бизнес-процесса, Power Automate или расширений подключаемых модулей.

Следующие этапы определены в последовательности операций бизнес-процесса по умолчанию:

- Новое
- Предложение с расценками
- Планирование
- Доставка
- Завершено
- Закрытие 

## <a name="new"></a>Создано

При создании проекта стадия проекта задается как **Создать**. Если проект был создан из шаблона, он может иметь расписание, оценку и данные рабочей группы. В противном случае это просто схема проекта, остальные компоненты необходимо ввести.

## <a name="quote"></a>Предложение с расценками

При связывании проекта с предложением с расценками или при создании проекта из предложения с расценками стадия проекта задана как **Предложение с расценками** , и также обновляются расчетные даты начала и окончания. Пока проект находится на стадии **Предложение с расценками** , сведения по предложению с расценками отображаются на вкладке **Продажи** на странице **Сущность проекта**.

## <a name="plan"></a>Планирование

При выигрыше предложения с расценками, связанного с проектом, проект переходит на этап **Контракт** , стадия проекта обновляется на **План**. Пока проект находится на стадии **План** , на странице **Сущность проекта** отображаются сведения о контракте.

## <a name="deliver"></a>Доставка

Когда планирование проекта завершено, и все готово для запуска проекта, руководитель проекта должен обновить стадию проекта на **Доставка** для отображения того, что проект начался.

## <a name="complete"></a>Завершено 

Когда работа по проекту выполнена, руководитель проекта может обновить стадию на **Завершено**. Путем обновления стадии проекта на **Завершено** руководитель проекта указывает, что работа на 100 процентов завершена, но проект остается открытым, чтобы можно было зарегистрировать все ожидающие записи времени или расходов.

## <a name="close"></a>Закрытие

Когда все транзакции зафиксированы для проекта, руководитель проекта может обновить стадию на **Закрыт**. В этот момент никакие транзакции невозможно зафиксировать, и проект становится доступен только для чтения.