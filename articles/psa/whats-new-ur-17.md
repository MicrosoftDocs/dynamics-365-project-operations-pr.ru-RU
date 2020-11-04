---
title: Что нового или измененного в выпуске-обновлении 17 для Project Service Automation версии 3
description: В этом разделе перечислены функции и исправления, доступные в выпуске-обновлении 17 для Project Service Automation версии 3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: 7ba685568692dafe117de42a71bb14d391cd7cc4
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083144"
---
# <a name="project-service-automation-update-release-17-v3"></a>Выпуск-обновление 17 Project Service Automation, версия 3

Мы рады объявить о последнем обновлении приложения Project Service Automation для Dynamics 365. Этот выпуск содержит некоторые важные усовершенствования, направленные на качество, производительность и удобство использования.  Этот выпуск совместим с Dynamics 365 9.x. Чтобы обновить приложение до этого выпуска, посетите Центр администрирования Dynamics 365 Online, страницу решений, чтобы установить обновление. Дополнительные сведения см. в разделе [Установка, обновление или удаление предпочтительного решения](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

В этом разделе перечислены функции и исправления, появившиеся или изменившиеся в выпуске-обновлении 17 для PSA версии 3. Эта версия имеет номер сборки V3.10.6.34 и становится доступна широкому кругу клиентов посредством самостоятельного обновления в марте 2020 г.


## <a name="update-release-17"></a>Выпуск-обновление 17

### <a name="bug-fixes"></a>Исправления ошибок

**Общие сведения**

- Исправлено: обновление приложения Project Service Automation для обеспечения соблюдения лицензий Team Member (Центр ресурсов проект будет включать метаданные плана обслуживания Team Member 3.x)
 
**Время и расходы**

- Исправлено: невозможно изменить оценку расходов с ненулевой цены на ноль (0). Изменение игнорируется.

**Управление проектами**

- Исправлено: проверка на значения NULL была добавлена для названия должности участника рабочей группы.
- Исправлено: поле **msdyn_userresourceid** в сущности **msdyn_resourceassignment** устарело.
- Исправлено: обновление с 2.x до 3.x теперь обрабатывает пустые контуры усилий в назначениях заданий.

**Sales**

- Исправлено: **Invoice.PreValidateInvoiceUpdate** теперь корректно обрабатывает сценарий переназначения владельцев записей.
- Исправлено: когда класс проводки **Время** , **UnitGroup** недоступна для редактирования для всех сущностей, включая **QuoteLineDetails** , **JournalLine** , **InvoiceLineDetail** и **ContractLineDetails**. Однако поле **Единица измерения** недоступно для редактирования только для **JournalLine** и **InvoiceLineDetails**.


