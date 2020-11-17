---
title: Как назначить резервируемый ресурс задаче в веб-приложении
description: Обзор способов назначения резервируемых ресурсов.
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 7b95eff52351904f97c62b3806f17b02db47860b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083376"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a>Как назначить резервируемый ресурс задаче в веб-приложении (приложение Project Service v2.x)?

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Существует два способа назначить ресурс задаче в Project Service. Можно зарезервировать ресурс как участника рабочей группы, а затем назначить его задаче. Кроме того, можно создать универсального участника рабочей группы через назначение роли для задач, создать рабочую группу, а затем выполнять требования по комплектованию с именованным ресурсом.

Обратите внимание, что если нужно назначить резервируемый ресурс задаче, участник группы резервируемого ресурса должен иметь достаточно доступных резервирований. Состояние резервирования должно быть типом исполнения "Окончательное резервирование" и состоянием "Исполнено". Если нет достаточных резервирований для этого ресурса, Project Service удаляет назначение и выводит следующее сообщение об ошибке:

*Не удалось назначить ресурс задаче — У следующих ресурсов нет достаточного количества часов, зарезервированных для проекта*

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>Резервирование ресурса как участника рабочей группы, затем назначение ресурса задаче

При использовании этого метода вы добавляете ресурс в рабочую группу проекта, затем назначаете задачи ресурсу в расписании проекта. Вот как это делается:
1.  В сетке участников рабочих групп добавьте нового участника рабочей группы, выбрав **Создать**.
2.  На экране быстрого создания участника рабочей группы выберите имя резервируемого ресурса и задайте роль.
3.  Выберите даты **От** и **До**.

    > [!div class="mx-imgBorder"] 
    > ![Снимок экрана с добавлением участника рабочей группы](media/FAQ-Resources-to-Tasks2-1.png "Снимок экрана с добавлением участника рабочей группы")
 
4.  Выберите один из следующих методов распределения для резервирования ресурса:
    - **Полная загрузка** резервирует полную загрузку ресурса для указанных дат от и до.
    - **Процент загрузки** резервирует ресурс для процент производительности ресурса для указанных дат от и до.
    - **По часам — распределить равномерно** резервирует ресурс для указанного количества часов, распределяя их равномерно по дням за указанные даты от и до.
    - **По часам — передняя погрузка** резервирует ресурс для указанного количества часов с передней погрузкой часов по дням за указанные даты от и до.

    Не следует выбирать вариант **Нет** , поскольку он добавляет ресурсы в рабочую группу, но не создает никаких резервирований, которые загружают ресурс.
5.  Нажмите кнопку **Сохранить**.

    Обратите внимание, что часов резервирования должно быть достаточно, чтобы охватывать диапазоны часов и дат задач, на которые назначен этот ресурс. Если они не находятся в соответствии, нельзя назначить ресурс задаче.

6.  На структурной декомпозиции работ (WBS) для задачи щелкните раскрывающееся меню ячейки ресурса. Затем: 

    1. Выберите **Добавить**.
    2. Выберите раскрывающийся список по заголовком **Ресурсы** и выберите участника рабочей группы, который был добавлен выше.
    3. Нажмите **ОК**. Участник команды теперь назначен задаче.

    > [!div class="mx-imgBorder"] 
    > ![Снимок экрана с добавлением ресурсов с помощью WBS](media/FAQ-Resources-to-Tasks2-2.png "Снимок экрана с добавлением ресурсов с помощью WBS")
 
В сетке участников рабочих групп вы увидите сводку назначенных часов ресурса в поле "Назначенные часы". Значение будет меньше или равно зарезервированным часам для ресурса. 

> [!div class="mx-imgBorder"] 
> ![Снимок экрана с назначенными часами для ресурса](media/FAQ-Resources-to-Tasks2-3.png "Снимок экрана с назначенными часами для ресурса")
 
Если задача, которую вы пытаетесь назначить ресурсу, начинается после конечной даты резервирований ресурса, ресурс не будет появляться в раскрывающемся списке".

Обратите внимание, что можно назначить ресурсу больше часов, чем его зарезервированные часы, если ресурс имеет некоторую оставшуюся нераспределенную производительность. В этом случае ресурс будет только частично назначен вплоть до его резервирований. Можно просмотреть эти оставшиеся неназначенные часы задач, добавив столбец "Необеспеченные персоналом часы" в структурную декомпозицию работ.

Если ресурсам назначены все их зарезервированные часы (их зарезервированные часы равны их назначенным часам), вы увидите следующее сообщение об ошибке при попытке назначить им дополнительные задачи:

*Не удалось назначить ресурс задаче — У следующих ресурсов нет достаточного количества часов, зарезервированных для проекта.*

Кроме того, участник рабочей группы руководителя проекта по умолчанию, который добавляется к группе при создании проекта, добавляется без каких-либо резервирований и ему не может быть назначена никакая задача. Они не отображаются в раскрывающемся списке ресурсов для задач.

Если требуется назначить этот ресурс, необходимо удалить его из группы, а затем повторно добавить его, используя метод распределения, отличный от "Нет". Причина их добавления в рабочую группу при создании проекта заключается в том, что проект должен иметь по крайней мере одного утверждающего по умолчанию.

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a>Создание универсального участника рабочей группы через назначение роли для задач

Этот способ обеспечивает, что ресурсы имеют достаточно резервирований для задач. Во-первых, следует создать местозаполнитель или универсальный ресурс, описывающий характеристики именованного ресурса, который должен обязательно работать на задачах, путем создания рабочей группы после назначения ролей задачам. Вот как это делается:

1. В структурной декомпозиции работ выберите задачу.
2. Выберите значок раскрывающегося списка **Назначенная роль** в ячейке ресурса.
3. Выберите раскрывающийся список **Роль** и выберите роль для универсального ресурса.
4. Нажмите **ОК**.

    > [!div class="mx-imgBorder"] 
    > ![Снимок экрана с использованием WBS для добавления ресурсов](media/FAQ-Resources-to-Tasks2-4.png "Снимок экрана с использованием WBS для добавления ресурсов")
 
После завершения назначение ролей задачам в WBS выберите **Создать рабочую группу проекта**. Project Service создает минимальное количество универсальных участников рабочей группы на основе ролей, подразделений для выделения ресурсов и календаря проекта путем суммирования назначений задач.

> [!div class="mx-imgBorder"] 
> ![Снимок экрана с созданием рабочей группы проекта](media/FAQ-Resources-to-Tasks2-5.png "Снимок экрана с созданием рабочей группы проекта")
 
В сетке участников рабочей группы можно видеть ресурсы типа "Универсальный ресурс" с именем ролей и должностей. Если два ресурса нужны для того, чтобы роль выполнила работу, функция "Создать рабочую группу" создает двух участников рабочей группы и использует имя должности для их разделения.

> [!div class="mx-imgBorder"] 
> ![Снимок экрана с добавлением двух универсальных ресурсов](media/FAQ-Resources-to-Tasks2-6.png "Снимок экрана с добавлением двух универсальных ресурсов")
 
Можно открыть потребность в комплектации ресурсов для универсального участника рабочей группы, выбрав ссылку под пунктом "Требование ресурса".

> [!div class="mx-imgBorder"] 
> ![Снимок экрана с открытием потребности в комплектации ресурса](media/FAQ-Resources-to-Tasks2-7.png "Снимок экрана с открытием потребности в комплектации ресурса")

Выберите **Резервировать** для универсального ресурса, после чего можно будет использовать доску расписания для поиска и резервирования реального ресурса. Можно также отправить требование для заполнения менеджером по ресурсам, выбрав **Отправить запрос**.

Когда универсальный ресурс заполняется именованным ресурсом, универсальный ресурс удаляется из участников группы, и назначения задач для универсального ресурса назначаются именованному ресурсу, который заполнив требования ресурса для универсального ресурса.
 
