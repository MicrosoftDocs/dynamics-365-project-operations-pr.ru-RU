---
title: Заголовок возможной сделки
description: Эта тема предоставляет сведения об общей информации о сделках на основе проектов и строках возможных сделок на основе проектов.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2f08de54767f49c308d0ccc7f2e1c6ef880b7f99
ms.sourcegitcommit: a0f80d024a5d3112a39781815bd31d0c05ddaf6f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/30/2020
ms.locfileid: "3906303"
---
# <a name="opportunity-header"></a>Заголовок возможной сделки

_**Относится к:** развертывание Lite — от сделки до счетов-проформ_

Заголовок возможной сделки содержит общую информацию о сделке на основе проекта, которая применяется ко всем строкам возможной сделки на основе проекта.

Возможные сделки на основе проектов в Dynamics 365 Project Operations — это расширения возможных сделок в Dynamics 365 Sales. Эти расширения предоставляют дополнительные функции, специфичные и необходимые для возможных сделок на основе проекта. Эти расширения могут включать новые поля и действия ленты, доступные в возможных сделках на основе проекта. Вы можете обнаружить, что некоторые поля, функции и логика задания значений по умолчанию, доступные в Sales, недоступны в Project Operations.

В следующей таблице представлены поля в возможной сделке на основе проекта, которые либо уникальны для Project Operations, либо имеют некоторые важные изменения в поведении по сравнению с возможными сделками в Sales.

| **Поле** | **Расположение** | **Релевантность, цель и руководство** | **Воздействие на последующие элементы** |
| --- | --- | --- | --- |
| Тип | Вкладке "Общие" (скрытая) | Это поле набора параметров имеет следующие параметры:</br>- На основе работы (доступно только с Project Operations)</br>- На основе номенклатуры (доступно только при установленных Project Operations и Sales)</br>- На основе сервисного обслуживания (доступно, если установлен Field Service) | Когда вы используете Project Operations, для этого поля автоматически устанавливается значение **На основе работ**, что классифицирует возможную сделку как основанную на проекте. Возможная сделка должна быть на основе проекта для включения всех специфичных для проекта расширений и функций в процессе последующих продаж для этой сделки. |
| Контактные сведения | Вкладка "Общие сведения" | Ссылка на основное контактное лицо клиента по данной сделке. | |
| Уч. запись | Вкладка "Общие сведения" | Ссылка на запись компании или учетную запись клиента. | |
| Менеджер по работе с клиентами | Вкладка "Общие сведения" | Имя менеджера по работе с клиентами для этой возможной сделки на основе проекта. | Менеджер по работе с клиентами отвечает за управление отношениями с клиентом до завершения этого проекта. На основе записи резервируемого ресурса, связанного с менеджером по работе с клиентами, контрактная единица задается по умолчанию. |
| Единица по контракту | Вкладка "Общие сведения" | Подразделение, отвечающее за реализацию проекта или проектов, связанных с этой сделкой. | Подрядное подразделение — это подразделение компании, которое будет завершать проекты после закрытия сделки. У каждой контрактной единицы есть валюта, и эта валюта используется для отчета о предполагаемых и фактических затратах, понесенных в ходе проекта. |

Для всех остальных полей и разделов на вкладке **Сводка** возможной сделки см. раздел [Создание или изменение возможных сделок (Sales и Центр продаж)](https://docs.microsoft.com/dynamics365/sales-enterprise/create-edit-opportunity-sales)
