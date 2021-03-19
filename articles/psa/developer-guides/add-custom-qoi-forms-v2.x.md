---
title: Добавление новых форм настраиваемых сущностей (Project Service Automation 2.x)
description: В этом разделе представлена информация о том, как добавлять формы пользовательской сущности для возможных сделок, предложений с расценками, заказов или счетов в Dynamics 365 Project Service Automation 2.x.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 3/14/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 9c9e31dc6d4d5a8ad5cc568f2d7d673c8703936d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284869"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a><span data-ttu-id="ed8c3-103">Добавление новых форм настраиваемых сущностей (Project Service Automation 2.x)</span><span class="sxs-lookup"><span data-stu-id="ed8c3-103">Add new custom entity forms (Project Service Automation 2.x)</span></span>

[!include [banner](../../includes/psa-now-project-operations.md)]

## <a name="type-field"></a><span data-ttu-id="ed8c3-104">Поле типа</span><span class="sxs-lookup"><span data-stu-id="ed8c3-104">Type field</span></span> 

<span data-ttu-id="ed8c3-105">Dynamics 365 Project Service Automation использует поле **Тип** (**msdyn\_ordertype**) сущностей возможной сделки, предложения с расценками, заказа и счета, чтобы отличать версии **на основе работы** этих сущностей от версий **на основе сущности** и **на основе услуги**.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-105">Dynamics 365 Project Service Automation relies on the **Type** (**msdyn\_ordertype**) field of the Opportunity, Quote, Order, and Invoice entities to distinguish **work-based** versions of these entities from **item-based** and **service-based** versions.</span></span> <span data-ttu-id="ed8c3-106">Версии на основе работы этих сущностей обрабатываются PSA.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-106">Work-based versions of these entities are handled by PSA.</span></span> <span data-ttu-id="ed8c3-107">Множество бизнес-логики на стороне клиента и стороне сервера этого решения зависит от поля **Тип**.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-107">Lots of business logic on the client side and server side of the solution depends on the **Type** field.</span></span> <span data-ttu-id="ed8c3-108">Следовательно, важно, чтобы поле было инициализировано с правильным значением при создании сущностей.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-108">Therefore, it's important that the field be initialized with a correct value when the entities are created.</span></span> <span data-ttu-id="ed8c3-109">Неправильное значение может привести к неверным поведениям, и некоторая бизнес-логика может работать неправильно.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-109">An incorrect value can cause incorrect behaviors, and some business logic might not run correctly.</span></span>

## <a name="automatic-form-switching"></a><span data-ttu-id="ed8c3-110">Автоматическое переключение форм</span><span class="sxs-lookup"><span data-stu-id="ed8c3-110">Automatic form switching</span></span>

<span data-ttu-id="ed8c3-111">Во избежание потенциального повреждения данных и необычного поведения, которые вызваны неправильной инициализацией и редактированием записей сущности продаж, PSA теперь содержит логику для автоматического переключения форм в готовых формах.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-111">To avoid potential data corruption and unexpected behaviors that are caused by incorrect initialization and editing of the sales entity records, PSA now includes logic for automatic form switching in out-of-box forms.</span></span> <span data-ttu-id="ed8c3-112">Эта логика переводит пользователя на правильную форму для работы с версией на основе работы или какого-либо другого типа сущности возможной сделки, предложения с расценками, заказа или счета.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-112">This logic takes users to the correct form for working with the work-based version or any other type of Opportunity, Quote, Order, or Invoice entity.</span></span> <span data-ttu-id="ed8c3-113">Если пользователь открывает версию на основе работы сущности возможной сделки, предложения с расценками, заказа или счета, форма переключается на форму **Сведения о проекте**.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-113">When a user opens the work-based version of an Opportunity, Quote, Order, or Invoice entity, the form is switched to **Project Information**.</span></span>

<span data-ttu-id="ed8c3-114">Логика автоматического переключения форм основывается на сопоставлении между значением **formId** и полем **msdyn\_ordertype**.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-114">The automatic form switching logic relies on the mapping between the **formId** value and the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="ed8c3-115">Все готовые формы были добавлены к данному сопоставлению.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-115">All out-of-box forms have been added to that mapping.</span></span> <span data-ttu-id="ed8c3-116">Однако настраиваемые формы необходимо вручную добавить, чтобы указать, для работы с какой версией сущности они предназначены.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-116">However, custom forms must be manually added to indicate which version of the entity they are intended to handle.</span></span> <span data-ttu-id="ed8c3-117">Это основано на поле **msdyn\_ordertype**.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-117">This is based on the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="ed8c3-118">Если переключение форм отсутствует в сопоставлении, логика переключается на готовую форму на основе значения, сохраненного в поле **msdyn\_ordertype** сущности.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-118">If the form switching is missing from the mapping, logic will switch to the out-of-box form, based on the value that is saved in the **msdyn\_ordertype** field of the entity.</span></span>

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a><span data-ttu-id="ed8c3-119">Добавление настраиваемых форм и включение логики переключения форм</span><span class="sxs-lookup"><span data-stu-id="ed8c3-119">Add custom forms and turn on the form switching logic</span></span>

<span data-ttu-id="ed8c3-120">Следующий пример показывает, как добавить настраиваемую форму **Мои сведения о проекте**, чтобы она работала с возможными сделками на основе работ.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-120">The following example shows how to add a custom form, **My Project Information**, so that it works with work-based opportunities.</span></span> <span data-ttu-id="ed8c3-121">Этот же процесс используется для добавления настраиваемых форм, чтобы они работали с предложениями с расценками, заказами и счетами.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-121">The same process is used to add custom forms so that they work with quotes, orders, and invoices.</span></span>

<span data-ttu-id="ed8c3-122">Выполните следующие шаги для создания настраиваемой версии формы **Сведения о проекте**.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-122">Follow these steps to create a custom version of the **Project Information** form.</span></span>

1. <span data-ttu-id="ed8c3-123">В сущности возможной сделки, откройте форму **Сведения о проекте** и сохраните копию под названием **Мои сведения о проекте**.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-123">In the Opportunity entity, open the **Project Information** form, and save a copy under the name **My Project Information**.</span></span>
2. <span data-ttu-id="ed8c3-124">Откройте новую форму, затем в свойствах убедитесь, что имеются скрипты инициализации формы из формы **Сведения о проекте**.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-124">Open the new form, and then, in the properties, make sure that the form initialization scripts from the **Project Information** form are present.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="ed8c3-125">Не следует удалять эти скрипты.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-125">Don't remove the scripts.</span></span> <span data-ttu-id="ed8c3-126">В противном случае некоторые данные могут быть инициализированы неправильно.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-126">Otherwise, some data might be initialized incorrectly.</span></span>

3. <span data-ttu-id="ed8c3-127">Убедитесь, что в форме имеется поле **Тип** (**msdyn\_ordertype**).</span><span class="sxs-lookup"><span data-stu-id="ed8c3-127">Verify that the **Type** (**msdyn\_ordertype**) field is present in the form.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="ed8c3-128">Не удаляйте данное поле.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-128">Don't remove this field.</span></span> <span data-ttu-id="ed8c3-129">В противном случае скрипты инициализации не будут выполняться.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-129">Otherwise, the initialization scripts will fail.</span></span>

4. <span data-ttu-id="ed8c3-130">Найдите значение **formId** новой формы.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-130">Find the **formId** value of the new form.</span></span> <span data-ttu-id="ed8c3-131">Этот шаг можно выполнить двумя способами:</span><span class="sxs-lookup"><span data-stu-id="ed8c3-131">You can complete this step in two ways:</span></span>

    - <span data-ttu-id="ed8c3-132">Экспортируйте форму **Мои сведения о проекте** в составе неуправляемого решения, затем найдите значение **formId** в файле customization.xml экспортированного решения.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-132">Export the **My Project Information** form as part of an unmanaged solution, and then look up the **formId** value in the customization.xml file of the exported solution.</span></span>
    - <span data-ttu-id="ed8c3-133">Откройте форму **Мои сведения о проекте** в редакторе форм, затем найдите глобальный уникальный идентификатор (GUID) рядом с параметром **fromId** в URL-адресе, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-133">Open the **My Project Information** form in the form editor, and then look for the globally unique identifier (GUID) next to the **fromId** parameter in the URL, as shown in the following illustration.</span></span>

    ![Значение formId новой формы в URL-адресе](media/how-to-add-custom-forms-in-v2.0.png)

5. <span data-ttu-id="ed8c3-135">Создайте сопоставление **msdyn\_ordertype** для значения **formId**, изменив веб-ресурс msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-135">Create an **msdyn\_ordertype** mapping for the **formId** value by editing the msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js web resource.</span></span> <span data-ttu-id="ed8c3-136">Удалите код из ресурса и замените его следующим кодом.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-136">Remove the code from the resource, and replace it with the following code.</span></span>

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

6. <span data-ttu-id="ed8c3-137">Сохраните и затем опубликуйте настройки.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-137">Save and then publish the customizations.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]