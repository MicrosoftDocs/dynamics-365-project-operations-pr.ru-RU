---
title: Изменение сущностей, элементов управления и интерфейса пользователя (Project Service Automation 3.x)
description: В этом разделе описаны изменения решения для Microsoft Dynamics Project Service Automation 3.x.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/15/2019
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
ms.openlocfilehash: 2d93e5eaae7cff302be1cb2e96e3f45c24739b0c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083383"
---
# <a name="entity-control-and-user-interface-changes-project-service-automation-3x"></a>Изменение сущностей, элементов управления и интерфейса пользователя (Project Service Automation 3.x)
В выпуске Microsoft Dynamics Project Service Automation (PSA) 3.x сделано много изменений сущностей, элементов управления, представлений и интерфейса пользователя. В этом разделе содержатся сведения об этих важных изменениях.

## <a name="parent-child-relationships-for-sales-document-sales-document-line-sales-document-line-detail-entities"></a>Отношения "родительское-дочернее" для сущностей документа продаж, строки документа продаж и сведений строки документа продаж
В версиях Dynamics 365 Project Service Automation (PSA), выпущенных до версии 3.0, некоторые отношений между сущностями документов продажи, строк документов продаж и сведений строк документов продаж были реализованы через строковые поля, которые должны были содержать строковое представление GUID связанной сущности. Это было связано с ограничениями платформы, которая требовала значительного объема настраиваемого кода на сторонах сервера и клиента в решении, чтобы эти отношения работали аналогично типичным отношениям сущностей Dynamics CRM и чтобы строковые поля вели себя как поля подстановки.

PSA 3.0 был обновлен, чтобы использовать новые отношения сущностей между сущностями документа продаж и строк документа продаж.

Так как поля подстановки можно теперь использовать для указания ссылок на сущности, поля, которые содержали строковое значение GUID связанной сущности в предыдущих версиях более не требуются и поэтому были объявлены устаревшими. Настраиваемый код на стороне клиента и сервера, который обрабатывает отношения, определенные старыми строковыми полями, также устарели.

### <a name="entity-schema-changes"></a>Изменения схемы сущностей
Следующая таблица содержит список взаимно-однозначного соответствия устаревших строковых полей и новых полей подстановки для сущностей. 

 Сущность |   Устаревшее поле (строка) | Новое поле (подстановка)
--- | --- | ---
invoicedetail (Строка счета) |  msdyn_contractline |    msdyn_contractlineid
msdyn_actual (Фактические) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_contractlineinvoiceschedule (Расписание счета строки контракта по проекту) |    msdyn_contractline |    msdyn_contractlineid
msdyn_contractlinescheduleofvalue (Веха строки контракта по проекту) |   msdyn_contractline |    msdyn_contractlineid
msdyn_fact (Факт) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_invoicelinetransaction (Сведения строки счета) | msdyn_invoiceline <br> msdyn_salescontractline | msdyn_invoicelineid <br> msdyn_salescontractlineid
msdyn_journalline (Строка журнала) |  msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlineresourcecategory (Категория ресурса строки контракта проекта) | msdyn_salescontractline |   msdyn_contractlineid
msdyn_orderlinetransaction (Сведения строки контракта проекта) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlinetransactioncategory (Категория проводки строки контракта проекта) |   msdyn_contractline |    msdyn_contractlineid
msdyn_orderlinetransactionclassification (Классификация проводки строки контракта проекта) |   msdyn_contractline |    msdyn_contractlineid
msdyn_quotelineinvoiceschedule (Расписание счета строки предложения с расценками) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelineresourcecategory (Категория ресурса строки предложения с расценками) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinescheduleofvalue (Веха строки предложения с расценками) | msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransaction (Сведения строки предложения с расценками) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactioncategory (Категория проводки строки предложения с расценками) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactionclassification (Классификация проводки строки предложения с расценками) |  msdyn_quoteline |   msdyn_quotelineid
SalesOrderDetail (Строка заказа) | msdyn_quotelineid | msdyn_quoteline 

### <a name="deprecated-custom-views-and-controls"></a>Устаревшие настраиваемые представления и элементы управления
Следующие настраиваемые представления и элементы управления, а также связанные с ними артефакты, устарели.

- Представление возможности оплаты.
- Настраиваемые элементы управления сетки для отображения сведений строки предложения с расценками на странице **Сведения о проекте** для строки предложения с расценками.
- Настраиваемые элементы управления сетки для отображения сведений строки контракта по проекту на странице **Сведения о проекте** для строки заказа на продажу.

> [!NOTE]
> Полный список устаревших ресурсов см. в разделе [Устаревшие веб-ресурсы в Project Service Automation v3.x](../developer-guides/web-resources-deprecated-v3.x.md)

## <a name="unified-client-interface-app-module"></a>Модуль приложения единого интерфейса клиента
С введением моделей приложения единого интерфейса клиента (UCI) записи карты сайта PSA были удалены из системы.  
Функция, связанная с переключением форм для возможной сделки, предложения с расценками, заказа и счета, стала устаревшей, так как она больше не требуется, потому что модуль приложения UCI содержит только версии форм для PSA.  

Следующие веб-ресурсы устарели:

- msdyn_\SalesDocument\SalesDocumentFormLoader.js
- msdyn_\SalesDocument\PSSalesDocumentCustomFormIds.js

> [!NOTE]
> Полный список устаревших ресурсов см. в разделе [Устаревшие веб-ресурсы в Project Service Automation v3.x](../developer-guides/web-resources-deprecated-v3.x.md).


