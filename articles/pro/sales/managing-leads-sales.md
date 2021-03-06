---
title: Управление интересами (Pro)
description: В этом разделе представлена информация об управлении интересами на основе проекта (pro).
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 005e36811643b0b1e98a686792cf39125ae97949
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896342"
---
# <a name="manage-leads-pro"></a>Управление интересами (Pro)

_**Относится к:** развертывание Lite — от сделки до счетов-проформ_

Интересами на основе проекта можно управлять и квалифицировать их в Project Operations. Процесс управления интересами включает в себя создание интересов на основе работы и их квалификацию. 

## <a name="list-of-project-sales-leads"></a>Список потенциальных клиентов по проекту

В разделе **Продажи** в левой навигационной панели откройте страницу списка **Интересы**, чтобы просмотреть список всех записей интересов в системе. Показанный список интересов основан на работе и других типах интересов, которые можно создать, если у вас также есть приложения Dynamics 365 Sales или Dynamics 365 Field Service.

Вы можете создать отфильтрованное представление, чтобы видеть только интересы на основе проекта, создав фильтр по значению **Тип**. Например, вы можете выбрать отображение только интересов по работе.

## <a name="creating-a-new-lead-for-a-project-based-deal"></a>Создание нового интереса для сделки на основе проекта

Когда интерес на основе проекта квалифицирован, создаются возможная сделка и учетная запись. Возможная сделка на основе проекта является отправной точкой для деятельности по достижению продаж на этапе возможной сделки. Возможные сделки, основанные на проектах, обладают уникальными возможностями, которые необходимы для работ по проекту продаж. Эти возможности включают:

- Методы выставления счетов за время и материалы и по фиксированной цене
- Несколько действующих на дату прайс-листов для человеческих ресурсов, расходов и материалов, потраченных по проектам.

Чтобы квалифицированный интерес автоматически создавал возможную сделку, установите атрибут **Тип** на **На основе работы**, когда вы создаете интерес. Если вы выберете другой тип, интерес не будет создавать возможную сделку на основе проекта, когда он будет квалифицирован. Если возможная сделка на основе проекта не создана, возможности конкретного проекта не будут доступны в последующих процессах продаж.

В следующей таблице содержится важная информация о полях для интереса и последующие последствия этих полей.

| **Поле** | **Расположение** | **Релевантность, цель и руководство** | **Воздействие на последующие элементы** |
| --- | --- | --- | --- |
| Описание | Вкладка "Общие сведения" | Это текстовое поле, и оно должно содержать краткое описание сделки. | Тема интереса по умолчанию будет иметь значение темы возможной сделки и название предложения с расценками и контракт по проекту. |
| Тип | Вкладка "Общие сведения" | Это поле набора параметров имеет следующие параметры:</br>- На основе работы (доступно только при установленном Project Operations)</br>- На основе номенклатуры (доступно только при установленных Project Operations и Sales)</br>- На основе сервисного обслуживания (доступно, если установлен Field Service) | Когда значение этого поля установлено на **На основе работы** в интересе, интерес квалифицируется для создания возможной сделки на основе проекта. Возможная сделка на основе проекта требуется для включения всех специфичных для проекта расширений и функций в процессе последующих продаж для этой сделки. |
| Имя | Вкладка "Общие сведения" | Имя контакта перспективного клиента | Когда интерес квалифицирован, создаются учетная запись, контакт и возможная сделка. Имя контакта — это значение, установленное здесь. |
| Фамилия | Вкладка "Общие сведения" | Фамилия контакта перспективного клиента | Когда интерес квалифицирован, создаются учетная запись, контакт и возможная сделка. Фамилия контакта — это значение, установленное здесь. |
| Компания | Вкладка "Общие сведения" | Название компании потенциального клиента | Когда интерес квалифицирован, создаются учетная запись, контакт и возможная сделка. Имя созданной учетной записи — это значение, установленное здесь. |
| Валюта | Вкладка сведений | Валюта перспективного клиента | Когда интерес квалифицирован, создаются учетная запись, контакт и возможная сделка. Валюта созданной учетной записи — это значение, установленное здесь. |

## <a name="qualify-a-new-project-based-lead"></a>Квалифицировать новый интерес на основе проекта

Интересы, для которых для параметра **Тип** задано значение **На основе работы**, называются интересами на основе проекта. После квалификации интереса на основе проекта создается следующее:

- Учетная запись, использующая поле **Компания** из интереса.
- Запись контакта, связанная с учетной записью на основе значений в полях **Имя** и **Фамилия** в интересе.
- Возможная сделка на основе проекта, у которой в поле **Тип** установлено значение &quot;**На основе работы**.

Для получения более подробной информации о квалификации интересов см. в разделе [Квалификация или конвертирование интересов](https://docs.microsoft.com/dynamics365/sales-enterprise/qualify-lead-convert-opportunity-sales).

## <a name="business-process-flow-for-project-based-deals"></a>Поток бизнес-процесса для сделок на основе проектов

Следующие потоки бизнес-процессов поддерживаются для сделок на основе проектов в Project Operations:

- Бизнес-процесс преобразования интереса в возможную сделку
- Преобразование возможной сделки в продажу

Бизнес-процесс преобразования интереса в возможную сделку поддерживает следующие этапы:

| Имя стадии | Сопоставленная сущность | Функциональность |
| --- | --- | --- |
| Квалифицировать | Интерес | Квалификация интереса для создания учетной записи, контакта и возможной сделки. |
| Подготовить | Возможная сделка | Разработайте возможную сделку для добавления дополнительной информации о проделанной работе, основных заинтересованных сторонах и конкуренции. |
| Предложить | Возможная сделка | Разработайте предложение и получите одобрение от группы внутренней проверки. |
| Закрыть | Возможная сделка | Реализуйте возможную сделку для закрытия сделки. |
