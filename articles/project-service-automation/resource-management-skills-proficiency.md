---
title: Навыки и модели квалификации
description: В этом разделе представлена информация о том, как использовать навыки и модели квалификации.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: d55a6d72-905f-4b82-a9fe-0b6b082473a6
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: fe4c9a62cd2ec1365daa09714fa6fa19210a7770
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755032"
---
# <a name="skills-and-proficiency-models"></a><span data-ttu-id="eb9cd-103">Навыки и модели квалификации</span><span class="sxs-lookup"><span data-stu-id="eb9cd-103">Skills and proficiency models</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="eb9cd-104">Навыки — это характеристики ресурса, которые являются общими между Dynamics 365 Project Service Automation и, при наличии, Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="eb9cd-104">Skills are resource characteristics that are shared between Dynamics 365 Project Service Automation and if present, Dynamics 365 Field Service.</span></span> 

<span data-ttu-id="eb9cd-105">Для обслуживания репозитория навыков в Project Service Automation перейдите в раздел **Ресурсы** \> **Навыки ресурса**.</span><span class="sxs-lookup"><span data-stu-id="eb9cd-105">To maintain the repository of skills in Project Service Automation, go to **Resources** \> **Resource Skills**.</span></span> 

> ![Навыки ресурса](media/Resource-Management-image84.png)

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="eb9cd-107">Использование моделей квалификации для оценки ресурсов</span><span class="sxs-lookup"><span data-stu-id="eb9cd-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="eb9cd-108">Навыки для ресурсов оцениваются моделями квалификации.</span><span class="sxs-lookup"><span data-stu-id="eb9cd-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="eb9cd-109">Отдельные оценки находятся в модели квалификации.</span><span class="sxs-lookup"><span data-stu-id="eb9cd-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="eb9cd-110">Чтобы создать модель квалификации, выберите **Ресурсы** \> **Модели квалификации**, затем выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="eb9cd-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="eb9cd-111">В новой модели оценки укажите минимальное значение оценки, максимальное значение оценки и сущность, которая оценивается.</span><span class="sxs-lookup"><span data-stu-id="eb9cd-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="eb9cd-112">Во вложенной сетке **Значения оценок** можно определить различные значения оценки, от минимальной до максимальной.</span><span class="sxs-lookup"><span data-stu-id="eb9cd-112">In the **Rating Values** sub-grid, you can define the different rating values, from the minimum to the maximum.</span></span>

> ![Определенные минимальные и максимальные оценки](media/Resource-Management-image85.png)

<span data-ttu-id="eb9cd-114">Эти значения оценок отображаются в фильтрах **Требования ресурсов**, **Таблица расписаний** и **Помощник по расписанию**.</span><span class="sxs-lookup"><span data-stu-id="eb9cd-114">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>