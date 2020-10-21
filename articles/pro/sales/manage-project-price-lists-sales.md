---
title: Управление прайс-листами проекта в предложениях с расценками по проекту
description: В этой теме предоставлена информация о работе с прайс-листами проекта в предложениях с расценками. (Sales)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4013d2e8cc0d2329f824a17484ee6f4a054a390e
ms.sourcegitcommit: f6509f7d50de4d4ebb92c1bf2cfcdf09f17458eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/06/2020
ms.locfileid: "3966848"
---
# <a name="manage-project-price-lists-on-project-quotes-sales"></a>Управление прайс-листами проекта в предложениях с расценками по проекту (Sales)

_**Относится к:** развертывание Lite — от сделки до счетов-проформ_

Предложения с расценками по проектам предназначены для поддержки прайс-листов продажи с несколькими датами действия. В Dynamics 365 Project Operations добавлена новая связанная сущность под названием **Прайс-листы проектов**. Эта сущность имеет отношение "1 ко многим" с предложением с расценками по проекту.

Прайс-листы проектов используются для определения цены времени и транзакций затрат по проекту. Если в предложении с расценками содержится один или несколько прайс-листов проекта, эти прайс-листы используются для определения цены времени, оценок затрат и фактических затрат по проектам, которые связаны с предложением с расценками через строку предложения с расценками.

Если в предложении с расценками по проекту нет прайс-листов проекта, вы получите предупреждающее сообщение. В сообщении говорится, что из-за отсутствия прайс-листов по проекту ваши предполагаемые и фактические работы и расходы по проекту не будут оценены. Вместо этого они будут иметь нулевую (0) цену для продажной стоимости.

## <a name="associate-or-disassociate-a-project-price-list-on-a-project-quote"></a>Связывание или отключение прайс-листа проекта с предложением с расценками по проекту

Чтобы создать или выбрать конкретный прайс-лист для оценки работ и расходов по проекту, выполните следующие действия.

1. В предложении с расценками выберите вкладку **Цена проекта** и во вложенной сетке выберите **+ Добавить новый прайс-лист проекта**.
2. На странице быстрого создания выберите прайс-лист. В раскрывающемся списке отображаются все прайс-листы, для которых задан контекст **Продажи** и валюта совпадает с валютой в предложении с расценками.
4. Введите описание для связи прайс-листа проекта и выберите **Сохранить и закрыть**.

Создается связь прайс-листа проекта.

Вы можете повторить этот процесс, если вам нужно связать более одного прайс-листа проекта с предложением с расценками по проекту. Создавайте несколько прайс-листов проекта, только если у вас разные даты вступления в силу для каждого из связанных прайс-листов проекта.

> [!NOTE]
> Project Operations не поддерживает перекрывающиеся даты вступления в силу прайс-листов проекта. Если существует несколько прайс-листов проекта для транзакции с заданной датой, цена в этой транзакции будет по умолчанию равна нулю (0).
Чтобы удалить связь с прайс-листом проекта, выберите прайс-лист проекта, затем выберите **Удалить прайс-лист проекта предложения с расценками**. Прайс-лист удаляется из прайс-листов проекта предложения с расценками, но сам прайс-лист не удаляется. Удаляется только связь с предложением с расценками.

## <a name="set-up-default-project-price-lists-on-a-quote"></a>Настройка прайс-листов проекта по умолчанию в предложении с расценками

Прайс-листы проектов могут быть настроены по умолчанию для предложения с расценками по проекту. Такая настройка гарантирует, что все предложения с расценками в вашей организации всегда начинаются со стандартного прайс-листа для этого ценового периода.

### <a name="set-up-organizational-default-for-project-price-lists"></a>Настройка организационного значения по умолчанию для прайс-листов проектов

1. Выберите **Параметры** > **Общее** > **Параметры**.
2. На странице списка **Активные параметры** найдите запись и дважды щелкните ее, чтобы открыть. 
3. На странице **Параметры** выберите вкладку **Прайс-лист**. Вы можете увидеть список прайс-листов по умолчанию. Это перечень стандартных затрат и прайс-листы продаж. Наличие связанного прайс-листа продаж здесь для каждой валюты, в которой вы продаете, гарантирует, что этот прайс-лист продаж будет использоваться по умолчанию для любого предложения с расценками, которое вы создаете для клиентов, совершающих сделки в этой валюте.

### <a name="set-up-customer-specific-project-price-lists"></a>Настройка прайс-листы проектов для конкретных клиентов

Прайс-листы проектов для конкретных клиентов также могут быть настроены после того, как вы заключите с клиентами генеральное ценовое соглашение.

Чтобы настроить прайс-лист проекта для конкретного клиента, выполните следующие действия.

1. В области **Продажи** выберите **Клиенты**.
2. В списке ваших активных учетных записей выберите и откройте запись клиента, для которой у вас есть специальный прайс-лист.
3. На вкладке **Прайс-листы проектов** вы можете создать новую связь прайс-листа, чтобы иметь специальный прайс-лист проекта для этого клиента.

## <a name="create-custom-pricing-on-a-project-quote"></a>Создание настраиваемых цен для предложения с расценками по проекту

После того как у вас есть прайс-листы проектов по умолчанию для организации и конкретных клиентов, ваши предложения с расценками по проекту будут автоматически создаваться с этими связанными прайс-листами проектов. Однако в некоторых случаях вам может потребоваться создать индивидуальную цену для конкретного предложения с расценками по проекту. 

1. На странице **Предложение с расценками по проекту** на вкладке **Прайс-лист проекта** убедитесь в том, что во вложенной сетке не выбрана конкретная запись прайс-листа.
2. Выберите **Создать настраиваемые цены**. Это сделает копии всех стандартных прайс-листов, в настоящее время связанных с предложением с расценками, и свяжет эти копии с предложением с расценками. Существующие связи со стандартными прайс-листами будут удалены. Затем продавец может начать редактировать цены в этих копиях. Эти измененные цены будут применяться только к этому предложению с расценками по проекту.