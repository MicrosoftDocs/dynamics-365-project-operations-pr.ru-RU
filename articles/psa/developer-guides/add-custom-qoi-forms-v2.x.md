---
title: Добавление новых форм настраиваемых сущностей (Project Service Automation 2.x)
description: В этом разделе представлена информация о том, как добавлять формы пользовательской сущности для возможных сделок, предложений с расценками, заказов или счетов в Dynamics 365 Project Service Automation 2.x.
author: makk
ms.custom:
- dyn365-projectservice
ms.date: 3/14/2019
ms.topic: article
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: ffc702bbe9cedb2a0cc8da8d8f58e48005950127
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584336"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a>Добавление новых форм настраиваемых сущностей (Project Service Automation 2.x)

[!include [banner](../../includes/psa-now-project-operations.md)]

## <a name="type-field"></a>Поле типа 

Dynamics 365 Project Service Automation использует поле **Тип** (**msdyn\_ordertype**) сущностей возможной сделки, предложения с расценками, заказа и счета, чтобы отличать версии **на основе работы** этих сущностей от версий **на основе сущности** и **на основе услуги**. Версии на основе работы этих сущностей обрабатываются PSA. Множество бизнес-логики на стороне клиента и стороне сервера этого решения зависит от поля **Тип**. Следовательно, важно, чтобы поле было инициализировано с правильным значением при создании сущностей. Неправильное значение может привести к неверным поведениям, и некоторая бизнес-логика может работать неправильно.

## <a name="automatic-form-switching"></a>Автоматическое переключение форм

Во избежание потенциального повреждения данных и необычного поведения, которые вызваны неправильной инициализацией и редактированием записей сущности продаж, PSA теперь содержит логику для автоматического переключения форм в готовых формах. Эта логика переводит пользователя на правильную форму для работы с версией на основе работы или какого-либо другого типа сущности возможной сделки, предложения с расценками, заказа или счета. Если пользователь открывает версию на основе работы сущности возможной сделки, предложения с расценками, заказа или счета, форма переключается на форму **Сведения о проекте**.

Логика автоматического переключения форм основывается на сопоставлении между значением **formId** и полем **msdyn\_ordertype**. Все готовые формы были добавлены к данному сопоставлению. Однако настраиваемые формы необходимо вручную добавить, чтобы указать, для работы с какой версией сущности они предназначены. Это основано на поле **msdyn\_ordertype**. Если переключение форм отсутствует в сопоставлении, логика переключается на готовую форму на основе значения, сохраненного в поле **msdyn\_ordertype** сущности.

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a>Добавление настраиваемых форм и включение логики переключения форм

Следующий пример показывает, как добавить настраиваемую форму **Мои сведения о проекте**, чтобы она работала с возможными сделками на основе работ. Этот же процесс используется для добавления настраиваемых форм, чтобы они работали с предложениями с расценками, заказами и счетами.

Выполните следующие шаги для создания настраиваемой версии формы **Сведения о проекте**.

1. В сущности возможной сделки, откройте форму **Сведения о проекте** и сохраните копию под названием **Мои сведения о проекте**.
2. Откройте новую форму, затем в свойствах убедитесь, что имеются скрипты инициализации формы из формы **Сведения о проекте**. 

    > [!IMPORTANT]
    > Не следует удалять эти скрипты. В противном случае некоторые данные могут быть инициализированы неправильно.

3. Убедитесь, что в форме имеется поле **Тип** (**msdyn\_ordertype**). 

    > [!IMPORTANT]
    > Не удаляйте данное поле. В противном случае скрипты инициализации не будут выполняться.

4. Найдите значение **formId** новой формы. Этот шаг можно выполнить двумя способами:

    - Экспортируйте форму **Мои сведения о проекте** в составе неуправляемого решения, затем найдите значение **formId** в файле customization.xml экспортированного решения.
    - Откройте форму **Мои сведения о проекте** в редакторе форм, затем найдите глобальный уникальный идентификатор (GUID) рядом с параметром **fromId** в URL-адресе, как показано на следующем рисунке.

    ![Значение formId новой формы в URL-адресе.](media/how-to-add-custom-forms-in-v2.0.png)

5. Создайте сопоставление **msdyn\_ordertype** для значения **formId**, изменив веб-ресурс msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js. Удалите код из ресурса и замените его следующим кодом.

    ```javascript
    define(["require", "exports"], function (require, exports) {
        "use strict";
        var SalesDocumentCustomFormIds = (function () {
            function SalesDocumentCustomFormIds() {
            }
            SalesDocumentCustomFormIds.overwriteFormIds = function (mappedFormIds) {
                /*
                ---- Notes ----
                mappedFormIds[SalesEntity][OrderType] => The array of forms IDs that support particular entity and order type
                Add or overwrite customized formId for the particular entity and order type by calling:
                    mappedFormIds[<EntityType>][<msdyn_ordertype>].push("<formId>");
                Allowed msdyn_ordertype values for reference:
                    ServiceBased: 690970002 (Field Service version of the entity)
                    WorkBased: 192350001 (PSA version of the entity)
                    ItemBased: 192350000 (Regular out of the box entity)
                Uncomment and update one of the following lines to register custom PSA form for required entity:
                */      
                //mappedFormIds[1][192350001].push("<formId>"); //Quote
                //mappedFormIds[5][192350001].push("<formId>"); //Quote Line
                //mappedFormIds[2][192350001].push("<formId>"); //Sales Order
                //mappedFormIds[6][192350001].push("<formId>"); //Sales Order Line
                // In this example we have added new form for Opportunity
                mappedFormIds[0][192350001].push("192EE537-DCC4-45D3-B7AF-EA694B9113D2"); //Opportunity
                //mappedFormIds[4][192350001].push("<formId>"); //Opportunity Line
            };
            return SalesDocumentCustomFormIds;
        }());
        exports.default = SalesDocumentCustomFormIds;
    });
    ```

6. Сохраните и затем опубликуйте настройки.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
