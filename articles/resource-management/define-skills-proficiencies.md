---
title: Определение навыков и квалификаций
description: В этом разделе представлена информация о том, как настроить модели квалификации для оценки ресурсов.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 9376e0b268a3ab682716da604ceecfa1e878da68
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897647"
---
# <a name="define-skills-and-proficiencies"></a>Определение навыков и квалификаций

_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_

Навыки — это характеристики ресурса, которые являются общими между Dynamics 365 Project Operations и, при наличии, Dynamics 365 Field Service. 

- Для обслуживания репозитория навыков в Project Operations перейдите в раздел **Ресурсы** \> **Навыки ресурса**. 

## <a name="use-proficiency-models-to-rate-resources"></a>Использование моделей квалификации для оценки ресурсов

Навыки для ресурсов оцениваются моделями квалификации. Отдельные оценки находятся в модели квалификации. 

1. Чтобы создать модель квалификации, выберите **Ресурсы** \> **Модели квалификации**, затем выберите **Создать**.
2. В новой модели оценки укажите минимальное значение оценки, максимальное значение оценки и сущность, которая оценивается.
3. Во вложенной сетке **Значения оценок** можно определить различные значения оценки, от минимальной до максимальной.


Эти значения оценок отображаются в фильтрах **Требования ресурсов**, **Таблица расписаний** и **Помощник по расписанию**.
