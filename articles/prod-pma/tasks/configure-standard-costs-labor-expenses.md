---
title: Настройка стандартных затрат на труд и расходов
description: В этой теме объясняется, как установить стандартные затраты на рабочую силу и расходы для проекта.
author: Yowelle
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b3eb6b1d4d75b095383689dd53a59a15fe9e884a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083245"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a>Настройка стандартных затрат на труд и расходов

[!include [banner](../../includes/banner.md)]

В этой теме объясняется, как установить стандартные затраты на рабочую силу и расходы для проекта. В этой задаче используется набор данных USSI.

1. На панели навигации перейдите **Модули > Управление проектами и учет > Настройка > Цены > Себестоимость (час)**.
2. Выберите **Создать**.
3. В поле **Дата вступления в силу** введите дату.
4. В поле **Себестоимость** введите число. Вы можете установить стандартную себестоимость для категории проекта или установить себестоимость по номеру работника, номеру проекта, категории, дате или любой их комбинации. Применяемая себестоимость является себестоимостью с максимальным уровнем детализации.  
5. Нажмите кнопку **Сохранить**.
6. На панели навигации перейдите **Модули > Управление проектами и учет > Настройка > Цены > Цена продажи (час)**.
7. Выберите **Создать**.
8. В поле **Дата вступления в силу** введите дату.
9. В поле **Действительно до** параметр выберите вариант.
10. В поле **Цены** введите число. Вы можете установить стандартную цену продажи для почасовых проводок или для категории проекта. Вы также можете установить цены продажи по номеру работника, номеру проекта, категории, дате транзакции или любой их комбинации. Фактическая цена продажи, которая применяется, когда работник вводит проводку в журнал часов, является ценой продажи с наивысшим уровнем детализации. Например, если установлены и общая цена продажи, и цена продажи для конкретного работника, используется цена продажи для конкретного работника.  
11. Нажмите кнопку **Сохранить**.
12. Закройте страницу.
13. На панели навигации перейдите **Модули > Управление проектами и учет > Настройка > Цены > Себестоимость (расход)**.
14. Выберите **Создать**.
15. В поле **Дата вступления в силу** введите дату.
16. В поле **Себестоимость** введите число. Можно заполнить несколько полей, но это минимум, необходимый для сохранения записи.  
17. Нажмите кнопку **Сохранить**.
18. На панели навигации перейдите **Модули > Управление проектами и учет > Настройка > Цены > Цена продажи (расход)**.
19. Выберите **Создать**.
20. В поле **Дата вступления в силу** введите дату.
21. В поле **Действительно до** параметр выберите вариант.
22. В поле **Цены** введите число. Фактическая цена продажи, которая применяется, когда работник вводит проводки в журнал расходов, является ценой продажи с наивысшим уровнем детализации. Например, если установлены и общая цена продажи, и цена продажи для конкретного работника, используется цена продажи для конкретного работника.  
23. Нажмите кнопку **Сохранить**.
