---
title: Рекомендации по обновлению структурной декомпозиции работ
description: В этом разделе приведены сведения об обновлении структурной декомпозиции работ из Project Service Automation версий с 2.x по 3.x.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
author: ruhercul
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
ms.openlocfilehash: cea8ce7f61fbc0f0c8c8deb522bc332be102238d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149559"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a>Рекомендации по обновлению структурной декомпозиции работ

[!include [banner](../includes/psa-now-project-operations.md)]

В этом разделе приведены сведения об обновлении структурной декомпозиции работ из Project Service Automation версий с 2.x по 3.x. В этом разделе определяется рабочее состояние проекта в Project Service Automation (PSA), которое требуется для успешного обновления. Также имеется информация об общих условиях блокировки, которые приведут к сбою обновления. Дополнительные сведения об определении задач проекта и их функций в расписании проекта см. [Расписания проекта](project-creating.md).

## <a name="key-entities"></a>Основные сущности
Для точной структурной декомпозиции работ, которая уже загружена ресурсами, требуются следующие сущности:

- [Проект](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [Проектная группа](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [Задача проекта](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [Назначения ресурсов](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [Зависимость задач проекта](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [Резервируемые ресурсы](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

Чтобы определить загруженную ресурсом структурную декомпозицию работ, необходимо выполнить следующие шаги:

1. Создание нового проекта. Дополнительные сведения о том, как создать новый проект, см. в статье [msdyn_project](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).
2. Создайте одну или несколько задач. Дополнительные сведения о том, как создать задачу, см. в статье [msdyn_projecttask](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).
3. Определите зависимости задачи. Дополнительные сведения см. в разделе [Зависимость задач проекта](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency),
4. Назначьте участников проектной рабочей группы проекту. Дополнительные сведения см. в статье [msdyn_projectteam](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).
5. Назначьте участников проектной рабочей группы задаче. Дополнительные сведения см. в статье [msdyn_resourceassignment](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).

## <a name="project-team-relationships"></a>Отношения проектной рабочей группы

Чтобы обеспечить успешное обновление, необходимо правильно поддерживать следующие отношения:
- Всех участники проектной рабочей группы должны быть связаны с резервируемым ресурсом.
- Всех участники проектной рабочей группы должны быть связаны с тем же проектом. 

## <a name="project-task-relationships"></a>Отношения задачи проекта
Чтобы обеспечить успешное обновление, необходимо правильно поддерживать следующие отношения:

- Все связанные задачи должно быть связано с тем же проектом.
- Каждая задача строки должна иметь родительскую задачу.
- Каждая задача должна иметь родительский проект.

### <a name="valid-conditions"></a>Допустимые условия

- Все длительности задачи должны быть больше или равны (>=) одному часу и менее 1800000 минут (1250 дней).*
- Все задачи должны иметь дату начала не ранее 01/01/2000.*
- Все задачи должны иметь дату начала не позднее 17 лет с сегодняшнего дня.*
- Все задачи должны иметь дату начала ранее или равную их дате окончания.
- Все типы проводок по классификациям (расходы, материалы, налоги и время) должны иметь значения для **Единица измерения по умолчанию** и **Группа единиц измерения**.
- Форматы даты с буквами следует избегать.

### <a name="potential-mitigation-steps"></a>Шаги по устранению потенциальных проблем
- С помощью расширенного поиска выявите задачи проекта, которые не содержат идентификатора проекта.
- С помощью расширенного поиска выявите задачи проекта, у которых запланированная длительность превышает 1 800 000.
- Прежде чем вносить какие-либо изменения в данные, вы должны изучить все настройки, связанные с сущностью, которые могли бы привести к неправильному состоянию данных. Решить проблему с этими настройками необходимо до того, как переходить к каким-либо связанным с данными обновлениям.
- Что касается найденных "потерянных" задач, рассмотрите возможность удаления этих задач, если они не нужны или если они должны быть связаны с соответствующим родительским проектом.
- Что касается задач, длительность которых превышает 1250 дней, рассмотрите возможность добавления нескольких задач, чтобы разделить эту длительность на меньшие периоды, если это допустимо.

> [!NOTE]
> Элементы, отмеченные звездочкой (\*), имеют ограничения, связанные с тем, что система управления отношениями с клиентами (CRM) поддерживает только 7320 расширений повторения. Необходимо оставаться ниже этого предела.

## <a name="resource-assignment-relationships"></a>Отношения назначений ресурсов
Чтобы обеспечить успешное обновление, необходимо правильно поддерживать следующие отношения:

- Все назначения ресурсов в структурной декомпозиции работ должны быть связаны с тем же проектом.
- Все назначения ресурсов в структурной декомпозиции работ должны быть связаны с участниками проектной рабочей группы в том же проекте.

### <a name="potential-mitigation-steps"></a>Шаги по устранению потенциальных проблем
- Выявите все задачи, не соответствующие приведенным выше условиям.  
- Все назначения ресурсов, которые больше не действительны, необходимо удалить.

## <a name="project-task-dependency-relationships"></a>Отношения зависимости задачи проекта
Чтобы обеспечить успешное обновление, необходимо правильно поддерживать следующие отношения:

- Все зависимости задач проекта должны быть связаны с одним и тем же проектом.
- Задача не может иметь одну и ту же зависимость, на которую ссылаются более одного раза.


[!INCLUDE[footer-include](../includes/footer-banner.md)]