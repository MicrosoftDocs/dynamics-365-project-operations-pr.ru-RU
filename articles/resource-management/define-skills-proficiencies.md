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
# <a name="define-skills-and-proficiencies"></a><span data-ttu-id="c14b2-103">Определение навыков и квалификаций</span><span class="sxs-lookup"><span data-stu-id="c14b2-103">Define skills and proficiencies</span></span>

<span data-ttu-id="c14b2-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="c14b2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c14b2-105">Навыки — это характеристики ресурса, которые являются общими между Dynamics 365 Project Operations и, при наличии, Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="c14b2-105">Skills are resource characteristics that are shared between Dynamics 365 Project Operations and if present, Dynamics 365 Field Service.</span></span> 

- <span data-ttu-id="c14b2-106">Для обслуживания репозитория навыков в Project Operations перейдите в раздел **Ресурсы** \> **Навыки ресурса**.</span><span class="sxs-lookup"><span data-stu-id="c14b2-106">To maintain the repository of skills in Project Operations, go to **Resources** \> **Resource Skills**.</span></span> 

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="c14b2-107">Использование моделей квалификации для оценки ресурсов</span><span class="sxs-lookup"><span data-stu-id="c14b2-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="c14b2-108">Навыки для ресурсов оцениваются моделями квалификации.</span><span class="sxs-lookup"><span data-stu-id="c14b2-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="c14b2-109">Отдельные оценки находятся в модели квалификации.</span><span class="sxs-lookup"><span data-stu-id="c14b2-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="c14b2-110">Чтобы создать модель квалификации, выберите **Ресурсы** \> **Модели квалификации** , затем выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="c14b2-110">To create a proficiency model, go to **Resources** \> **Proficiency Models** , and then select **New**.</span></span>
2. <span data-ttu-id="c14b2-111">В новой модели оценки укажите минимальное значение оценки, максимальное значение оценки и сущность, которая оценивается.</span><span class="sxs-lookup"><span data-stu-id="c14b2-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="c14b2-112">Во вложенной сетке **Значения оценок** можно определить различные значения оценки, от минимальной до максимальной.</span><span class="sxs-lookup"><span data-stu-id="c14b2-112">In the **Rating Values** sub-grid, you can define the different rating values, from the minimum to the maximum.</span></span>


<span data-ttu-id="c14b2-113">Эти значения оценок отображаются в фильтрах **Требования ресурсов** , **Таблица расписаний** и **Помощник по расписанию**.</span><span class="sxs-lookup"><span data-stu-id="c14b2-113">These rating values are shown on the **Resource Requirements** , **Schedule Board** , and **Schedule Assistant** filters.</span></span>
