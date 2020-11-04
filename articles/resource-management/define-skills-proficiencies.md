---
title: Определение навыков и квалификаций
description: В этом разделе представлена информация о том, как настроить модели квалификации для оценки ресурсов.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 24538ed1d610a0cae4c2badc0fd33c2f738a8338
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083132"
---
# <a name="define-skills-and-proficiencies"></a>Определение навыков и квалификаций

_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_

Навыки — это характеристики ресурса, которые являются общими между Dynamics 365 Project Operations и, при наличии, Dynamics 365 Field Service. 

- Для обслуживания репозитория навыков в Project Operations перейдите в раздел **Ресурсы** \> **Навыки ресурса**. 

## <a name="use-proficiency-models-to-rate-resources"></a>Использование моделей квалификации для оценки ресурсов

Навыки для ресурсов оцениваются моделями квалификации. Отдельные оценки находятся в модели квалификации. 

1. Чтобы создать модель квалификации, выберите **Ресурсы** \> **Модели квалификации** , затем выберите **Создать**.
2. В новой модели оценки укажите минимальное значение оценки, максимальное значение оценки и сущность, которая оценивается.
3. Во вложенной сетке **Значения оценок** можно определить различные значения оценки, от минимальной до максимальной.


Эти значения оценок отображаются в фильтрах **Требования ресурсов** , **Таблица расписаний** и **Помощник по расписанию**.
