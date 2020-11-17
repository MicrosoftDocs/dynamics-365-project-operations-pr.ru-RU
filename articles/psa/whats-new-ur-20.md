---
title: Что нового и что изменилось в выпуске-обновлении 20 для Project Service Automation версии 3
description: В этом разделе перечислены функции и исправления, доступные в выпуске-обновлении 20 для Project Service Automation версии 3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: 12edae76dbc6de63d3e2d36058c4092f80ede77d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083137"
---
# <a name="project-service-automation-update-release-20-v3"></a>Выпуск-обновление 20 Project Service Automation, версия 3

Мы рады объявить о последнем обновлении приложения Project Service Automation для Dynamics 365. Этот выпуск содержит некоторые важные усовершенствования, направленные на качество, производительность и удобство использования. Этот выпуск совместим с Dynamics 365 9.x. Чтобы обновить приложение до этого выпуска, посетите страницу решений Центра администрирования Dynamics 365 Online и установите обновление. Дополнительные сведения см. в разделе [Установка, обновление или удаление предпочтительного решения](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

В этом разделе перечислены функции и исправления, появившиеся или изменившиеся в выпуске-обновлении 20 для Project Service Automation версии 3. Эта версия имеет номер сборки V3.10.31.37 и стала доступна для широкой публики после автоматического обновления в июне 2020 г.

## <a name="update-release-20"></a>Выпуск-обновление 20

### <a name="bug-fixes"></a>Исправленные ошибки

**Управление проектами**

Следующие проблемы были исправлены:

- Импорт членов команды проекта с методом распределения, который требует часов, вызывает непонятное сообщение об ошибке, когда указанные часы равны нулю.
- Пользователи получают неверную ошибку, когда в поле **Описание** для задачи проекта введено максимальное количество символов.
- Страница **Загрузка надстройки Microsoft Dynamics 365 Project Service Automation** перенаправляет на страницу загрузки на английском языке, когда языковые настройки пользователя установлены на японский.
- При возникновении ошибки сервера метка синхронизации на вкладке **Расписание** формы **Проекты** иногда остается.
- Избыточные обновления задач отправляются на сервер при изменении задачи.

**Sales**

Следующие проблемы были исправлены:

- В форме **Контракт** двойной щелчок **Создать накладные** создает две накладные для одной фактической записи.
- В Internet Explorer 11 пользователи не могут создавать записи расходов.
- Отмена затрат и отмена фактических продаж без счета не связаны.
- Кнопка **Обновить фактические показатели** в форме **Проект** не обновляет **Фактические часы по задаче**.
- Подключаемый модуль **PreValidateProjectTeamMemberCreate** может создавать дубликаты общих резервируемых ресурсов, когда атрибут **msdyn_isgenericresourceprojectscoped** имеет значение **False**.
- **Пересчитать** очищает подлежащие оплате затраты в сведениях строки предложения с расценками на основе продуктов и в сведениях по строке контракта.
- В некоторых сценариях подключаемый модуль **PostEstimateLineUpdate** отображает ошибку пустой ссылки.
- Продолжительность фазы времени на диаграмме **Анализ рентабельности** не соответствует длительности затрат в строке предложения с фиксированной ценой.
- Значения единиц и групп единиц измерения по умолчанию неверны для категорий расходов в формах **Сведения строки контракта** и **Сведения строки предложения с расценками**.
- Списки **Себестоимость подразделения** допускают частичное совпадение даты вступления в силу.
- Пользователям не разрешено изменять **Подразделение** , если тип заказа не основан на работе, так как это приведет к ошибке пустой ссылки.
- При попытке перейти из формы **Сведения строки предложения с расценками** на вкладку **Предложение с расценками** форма обновляется и открывается вкладка **Сводка**.