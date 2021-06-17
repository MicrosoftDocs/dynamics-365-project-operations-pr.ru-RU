---
title: Реализация настраиваемых полей для мобильного приложения Microsoft Dynamics 365 Project Timesheet iOS и Android
description: В этой теме представлены общие шаблоны использования расширений для реализации настраиваемых полей.
author: Yowelle
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 23b002559dcbb9118ccb2b36d70707ccb37b19ad
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003061"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a>Реализация настраиваемых полей для мобильного приложения Microsoft Dynamics 365 Project Timesheet iOS и Android

[!include [banner](../includes/banner.md)]

В этой теме представлены общие шаблоны использования расширений для реализации настраиваемых полей. Рассмотрены следующие вопросы:

- Различные типы данных, поддерживаемые платформой настраиваемых полей
- Как отображать поля, доступные только для чтения или редактируемые в записях расписания, и сохранять введенные пользователем значения обратно в базу данных
- Как показать поля только для чтения в заголовке расписания
- Как интегрировать другую настраиваемую бизнес-логику для ввода значений по умолчанию в поля и выполнения дополнительной проверки

## <a name="audience"></a>Аудитория

Этот тема предназначен для разработчиков, которые интегрируют свои настраиваемые поля в мобильное приложение Microsoft Dynamics 365 Project Timesheet для Apple iOS и Google Android. Предполагается, что читатели знакомы с разработкой X++ и функциями расписания проекта.

## <a name="data-contract--tstimesheetcustomfield-x-class"></a>Контракт данных — класс TSTimesheetCustomField X++

Класс **TSTimesheetCustomField** — это класс контракта данных X++, который представляет информацию о настраиваемом поле для функций расписания. Списки объектов настраиваемых полей передаются как в контракте данных TSTimesheetDetails, так и в контракте данных TSTimesheetEntry для отображения настраиваемых полей в мобильном приложении.

- **TSTimesheetDetails** — контракт заголовка расписания.
- **TSTimesheetEntry** — контракт транзакции расписания. Группы этих объектов с одинаковой информацией о проекте и значение **TimesheetLineRecId** составляют строку.

### <a name="fieldbasetype-types"></a>fieldBaseType (Types)

В свойстве **FieldBaseType** объекта **TsTimesheetCustom** определяется тип поля, отображаемого в приложении. Последующие значения **Types** поддерживаются.

| Значение Types | Тип              | Заметки |
|-------------|-------------------|-------|
| 0           | Строка (и Enum) | Поле отображается как текстовое поле. |
| 1           | Integer           | Значение отображается в виде числа без десятичных знаков. |
| 2           | Вещественное число              | Значение отображается в виде числа с десятичными знаками.<p>Чтобы отобразить в приложении реальную стоимость в валюте, используйте свойство **fieldExtenededType**. Вы можете использовать свойство **numberOfDecimals** для задания количества отображаемых десятичных знаков.</p> |
| 3           | Дата              | Форматы даты определяются заданным пользователем параметром **Дата, время и числовой формат**, указанным в **Предпочтительный язык и страна/регион** в **Параметры пользователя**. |
| 4           | Boolean           | |
| 15          | GUID              | |
| 16          | Int64             | |

- Если свойство **stringOptions** не указано в объекте **TSTimesheetCustomField**, пользователю предоставляется поле с произвольным текстом.

    Свойство **stringLength** можно использовать для установки максимальной длины строки, которую могут вводить пользователи.

- Если свойство **stringOptions** указано в **TSTimesheetCustomField**, эти элементы списка — единственные значения, которые пользователи могут выбирать с помощью переключателей (кнопок).

    В этом случае строковое поле может действовать как значение перечисления для ввода пользователя. Чтобы сохранить значение в базе данных в виде перечисления, вручную сопоставьте строковое значение обратно со значением перечисления перед сохранением в базе данных с помощью цепочки команд (см. раздел "Использование цепочки команд в классе TSTimesheetEntryService для сохранения записи расписания из приложение обратно в базу данных" ниже в этой теме для примера).

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a>fieldExtendedType (TSCustomFieldExtendedType)

Это свойство можно использовать для форматирования реальных значений в виде валюты. Этот подход применим только тогда, когда значение **fieldBaseType** — **Вещественное число**.

- **TSCustomFieldExtendedType:None** — форматирование не применяется.
- **TSCustomFieldExtendedType::Currency** — отформатируйте значение как валюту.

    Когда форматирование валюты активно, поле **stringValue** можно использовать для передачи кода валюты, который должен отображаться в приложении. Это значение доступно только для чтения.

    В поле **realValue** содержится сумма денег, которую необходимо сохранить в базе данных.

### <a name="fieldsection-tscustomfieldsection"></a>fieldSection (TSCustomFieldSection)

Вы можете использовать это свойство, чтобы указать, где в приложении должно отображаться настраиваемое поле.

- **TSCustomFieldSection::Header** — поле появится в разделе **Подробные сведения** в приложении. Они всегда доступны только для чтения.
- **TSCustomFieldSection::Line** — поле появится после всех стандартных полей строк в записях расписания. Эти поля могут быть доступны для редактирования или только для чтения.

### <a name="fieldname-fieldnameshort"></a>fieldName (FieldNameShort)

Это свойство определяет поле, когда значения, предоставляемые приложением, сохраняются обратно в базу данных.

### <a name="tablename-tablenameshort"></a>tableName (TableNameShort)

Это свойство определяет поле, когда значения, предоставляемые приложением, сохраняются обратно в базу данных.

### <a name="iseditable-noyes"></a>isEditable (NoYes)

Установите для этого свойства значение **Да**, чтобы указать, что поле в разделе записи расписания должно быть доступно для редактирования пользователями. Установите для свойства значение **Нет**, чтобы сделать поле доступным только для чтения.

### <a name="ismandatory-noyes"></a>isMandatory (NoYes)

Установите для этого свойства значение **Да**, чтобы указать, что поле в разделе записи расписания должно быть обязательным.

### <a name="label-str"></a>label (str)

Это свойство определяет метку, которая отображается рядом с полем в приложении.

### <a name="stringoptions-list-of-strings"></a>stringOptions (список строк)

Это свойство применимо только, когда для **fieldBaseType** задано значение **Строка**. Если задано **stringOptions**, строковые значения, доступные для выбора с помощью переключателей, задаются строками в списке. Если строки не указаны, допускается ввод произвольного текста в поле строки (см. пример в разделе "Использование цепочки команд в классе TSTimesheetEntryService для сохранения записи расписания из приложения обратно в базу данных" далее в этой теме).

### <a name="stringlength-int"></a>stringLength (int)

Это свойство определяет максимальную длину строкового поля. Это применимо только, когда для **fieldBaseType** задано значение **Строка**.

### <a name="numberofdecimals-int"></a>numberOfDecimals (int)

Это свойство определяет количество десятичных знаков, отображаемых для вещественного поля. Это применимо только, когда для **fieldBaseType** задано значение **Вещественное число**.

### <a name="ordersequence-int"></a>orderSequence (int)

Это свойство управляет порядком, в котором настраиваемые поля отображаются в приложении, если указано более одного настраиваемого поля. Поля с меньшими номерами отображаются первыми.

### <a name="booleanvalue-boolean"></a>booleanValue (логическое)

Для полей с типом **Логическое**, это свойство передает логическое значение поля между сервером и приложением.

### <a name="guidvalue-guid"></a>guidValue (guid)

Для полей с типом **GUID**, это свойство передает глобальный уникальный идентификатор (GUID) поля между сервером и приложением.

### <a name="int64value-int64"></a>int64Value (int64)

Для полей с типом **Int64**, это свойство передает значение int64 поля между сервером и приложением.

### <a name="intvalue-int"></a>intValue (int)

Для полей с типом **Int**, это свойство передает значение int поля между сервером и приложением.

### <a name="realvalue-real"></a>realValue (real)

Для полей с типом **Вещественное**, это свойство передает значение "real" поля между сервером и приложением.

### <a name="stringvalue-str"></a>stringValue (str)

Для полей с типом **Строка**, это свойство передает значение "строка" поля между сервером и приложением. Он также используется для полей с типом **Вещественный**, отформатированных как валюта. Для этих полей свойство используется для передачи кода валюты в приложение.

### <a name="datevalue-date"></a>dateValue (дата)

Для полей с типом **Дата**, это свойство передает значение "дата" поля между сервером и приложением.

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a>Показать и сохранить настраиваемое поле в разделе записи расписания

Ниже приведен снимок экрана мобильного приложения для создания записи расписания. Он показывает стандартные поля и настраиваемое поле в разделе "Запись времени" под названием "Тестовая строка" с уже установленным значением перечисления "Второй параметр".

![Настраиваемое поле тестовой строки в приложении](media/timesheet-entry.jpg)



Ниже приведен снимок экрана мобильного приложения, на котором пользователь выбирает один из вариантов перечисления, доступных для настраиваемого поля «Тестовая строка».  Два варианта — «Первый вариант» и «Второй вариант» показаны как переключатели. В настоящее время выбран второй вариант.

![Кнопки выбора (переключатели) для настраиваемого поля тестовой строки](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a>Расширьте таблицу TSTimesheetLine, чтобы в ней было настраиваемое поле

В типичных сценариях вполне вероятно, что данные для настраиваемого поля в разделе записи расписания будут сохранены в таблице TSTimesheetLine. Однако можно использовать другие таблицы, если данные можно получить на основе предоставленной записи TSTimesheetTrans или если у нее нет определенного контекста записи (например, если поле установлено как доступное только для чтения в параметрах проекта).

Обратите внимание, что настраиваемые поля не обязательно должны иметь какие-либо резервные записи базы данных. Их можно динамически генерировать на основе логики X++. Этот подход может быть полезен в сценариях только для чтения (см. Раздел «Использование цепочки команд в классе TSTimesheetDetails, метод buildCustomFieldListForHeader для заполнения сведений расписания» для примера динамически генерируемых значений настраиваемых полей).

Ниже скриншот из Visual Studio дерева объектов приложения. Он показывает расширение таблицы TSTimesheetLine с полем TestLineString, добавленным в качестве настраиваемого поля.

![Строка](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a>Используйте цепочку команд в методе buildCustomFieldList класса TSTimesheetSettings, чтобы отобразить поле в разделе записи расписания.

Этот код управляет настройками отображения поля в приложении. Например, он контролирует тип поля, метку, является ли поле обязательным и в каком разделе отображается поле.

В следующем примере показано строковое поле для записей времени. В этом поле есть два варианта: **Первый вариант** и **Второй вариант**, которые доступны с помощью переключателей. Поле в приложении связано с полем **TestLineString**, которое добавляется в таблицу TSTimesheetLine.

Обратите внимание на использование метода **TSTimesheetCustomField::newFromMetatdata()** для упрощения инициализации свойств настраиваемого поля: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength** и **numberOfDecimals**. Вы также можете установить эти параметры вручную по своему усмотрению.

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a>Используйте цепочку команд в методе buildCustomFieldListForEntry класса TSTimesheetEntry, чтобы ввести значения в запись расписания

Метод **buildCustomFieldListForEntry** используется для ввода значений в сохраненные строки расписания в мобильном приложении. В качестве параметра требуется запись TSTimesheetTrans. Поля из этой записи можно использовать для заполнения значения настраиваемого поля в приложении.

```xpp
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a>Используйте цепочку команд в классе TSTimesheetEntryService, чтобы сохранить запись расписания из приложения обратно в базу данных.

Чтобы сохранить настраиваемое поле обратно в базу данных при типичном использовании, необходимо расширить несколько методов:

- Метод **расписаниеLineNeedsUpdating** используется для определения того, была ли запись строки изменена пользователем в приложении и должна ли быть сохранена в базе данных. Если производительность не вызывает беспокойства, этот метод можно упростить, чтобы он всегда возвращал **true**.
- Методы **populateTimesheetLineFromEntryDuringCreate** и **populateTimesheetLineFromEntryDuringUpdate** можно расширить, чтобы они вводили значения в запись базы данных TSTimesheetLine из предоставленной записи контракта данных TSTimesheetEntry. Обратите внимание, что в следующем примере сопоставление поля базы данных и поля ввода выполняется вручную с помощью кода X++.
- Метод **populateTimesheetWeekFromEntry** также может быть расширен, если настраиваемое поле, сопоставленное с объектом **TSTimesheetEntry**, должно записать обратно в таблицу базы данных TSTimesheetLineweek.

> [!NOTE]
> В следующем примере сохраняется значение **firstOption** или **secondOption**, которое пользователь выбирает для базы данных как необработанное строковое значение. Если поле базы данных является полем типа **Enum**, эти значения могут быть вручную сопоставлены со значением перечисления, а затем сохранены в поле перечисления в таблице базы данных.

```xpp
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a>Показать настраиваемое поле в разделе заголовка

Ниже приведен снимок экрана мобильного приложения пользователя, просматривающего расписание. Кнопка «Дополнительная информация» была выбрана в правом верхнем углу, чтобы отобразить параметр «Подробнее».  

![Команда "Подробнее"](media/show-more.png)

Ниже приведен снимок экрана мобильного приложения, на котором показан раздел "Дополнительно" расписания. В раздел заголовка расписания добавлено настраиваемое поле «Коэффициент использования этого расписания (вычисляемое настраиваемое поле)». В настраиваемом поле установлено значение «0,667» только для чтения.

![Раздел "Подробнее"](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a>Расширьте таблицу TSTimesheetTable, чтобы в ней было настраиваемое поле

В типичных сценариях вполне вероятно, что данные для настраиваемого поля в разделе заголовка будут сохранены извлечены из таблицы TSTimesheetHeader. Однако можно использовать другие таблицы, если данные можно получить на основе предоставленной записи TSTimesheetTable или если у нее нет определенного контекста записи (например, если поле установлено как доступное только для чтения в параметрах проекта).

Обратите внимание, что настраиваемые поля не обязательно должны иметь какие-либо резервные записи базы данных. Их можно динамически генерировать на основе логики X++. Следующий пример демонстрирует этот подход.

Поля в разделе заголовка в приложении всегда доступны только для чтения.

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a>Используйте цепочку команд в методе buildCustomFieldList класса TSTimesheetSettings, чтобы отобразить поле в разделе заголовка.

Этот код управляет настройками отображения поля в приложении. Например, он контролирует тип поля, метку, является ли поле обязательным и в каком разделе отображается поле.

В следующем примере показано вычисленное значение в разделе заголовка в приложении.

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a>Используйте цепочку команд в методе buildCustomFieldListForHeader класса TSTimesheetDetails, чтобы заполнить сведения расписания

Метод **buildCustomFieldListForHeader** используется для заполнения сведений заголовка расписания в мобильном приложении. В качестве параметра требуется запись TSTimesheetTable. Поля из этой записи можно использовать для заполнения значения настраиваемого поля в приложении. В следующем примере не считываются значения из базы данных. Вместо этого используется логика X++ для генерации вычисленного значения, которое затем отображается в приложении.


```xpp
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a>Другие возможности настройки/расширения

### <a name="adding-additional-validation-for-the-app"></a>Добавление дополнительной проверки для приложения

Существующая логика для функциональности расписания на уровне базы данных по-прежнему будет работать должным образом. Чтобы прервать завершение операций сохранения или отправки и показать конкретное сообщение об ошибке, вы можете добавить **показать ошибку ("сообщение пользователю")** в код через цепочку расширения команд. Вот три примера полезных расширяемых методов:

- Если **validateWrite** в таблице TSTimesheetLine возвращает **false** во время операции сохранения строки расписания в мобильном приложении, отображается сообщение об ошибке.
- Если **validateSubmit** в таблице TSTimesheetTable возвращает **false** во время передачи расписания в приложении, пользователю отображается сообщение об ошибке.
- Логика, заполняющая поля (например, **Свойство строки**) во время метода **insert** в таблице TSTimesheetLine, по-прежнему будет работать.

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a>Скрытие и отметка стандартных полей как доступных только для чтения через конфигурацию

Из параметров проекта вы можете сделать стандартные поля доступными только для чтения или скрытыми в мобильном приложении. Задайте параметры в разделе **Мобильные расписания** на вкладке **Расписание** на странице **Параметры управления проектами и учета**.

![Параметры проекта](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a>Изменение действий, доступных для выбора через расширения

Действия, которые доступны для выбора для проекта, заполняются через методы **getActivitiesForProject()** и **getActivityQuery()** в классе **TsTimesheetProjectService**. Вы можете использовать цепочку команд, чтобы изменить это поведение в соответствии с вашим бизнес-сценарием для действий, доступных для выбора для конкретного проекта.

### <a name="entering-a-default-project-category-on-timesheet-entries"></a>Ввод категории проекта по умолчанию в записях расписания

Ввод категории проекта по умолчанию в записи расписания происходит на трех уровнях. Вы можете использовать цепочку команд, чтобы расширить поведение на любом или всех этих уровнях для достижения желаемого поведения. Используется следующая иерархия:

1. Приложение пытается поместить категорию по умолчанию из ресурса проекта. Эта категория по умолчанию установлена в методах **getCurrentUserResource** и **getDelegatedResourcesForCurrentUser** в классе **TSTimesheetSettingsService**.
2. Если категория по умолчанию не указана на уровне ресурсов проекта, приложение пытается извлечь ее из операции проекта. Эта категория по умолчанию установлена в методе **getActivitiesForProject** в классе **TSTimesheetProjectService**.
3. Если категория по умолчанию не указана на уровне действий проекта, категория по умолчанию берется из параметров проекта. Эта категория по умолчанию установлена в методе **getProjectDetailsbyRule** в классе **TSTimesheetProjectService**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]