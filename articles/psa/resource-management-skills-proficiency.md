---
title: Навыки и модели квалификации
description: В этом разделе представлена информация о том, как использовать навыки и модели квалификации.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/13/2019
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
ms.openlocfilehash: 82eeab4c9682e5b777da4e66f6c4f3f1afb3c19b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282979"
---
# <a name="skills-and-proficiency-models"></a><span data-ttu-id="d3783-103">Навыки и модели квалификации</span><span class="sxs-lookup"><span data-stu-id="d3783-103">Skills and proficiency models</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="d3783-104">Навыки — это характеристики ресурса, которые являются общими между Dynamics 365 Project Service Automation и, при наличии, Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="d3783-104">Skills are resource characteristics that are shared between Dynamics 365 Project Service Automation and if present, Dynamics 365 Field Service.</span></span> 

<span data-ttu-id="d3783-105">Для обслуживания репозитория навыков в Project Service Automation перейдите в раздел **Ресурсы** \> **Навыки ресурса**.</span><span class="sxs-lookup"><span data-stu-id="d3783-105">To maintain the repository of skills in Project Service Automation, go to **Resources** \> **Resource Skills**.</span></span> 

> ![Навыки ресурса](media/Resource-Management-image84.png)

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="d3783-107">Использование моделей квалификации для оценки ресурсов</span><span class="sxs-lookup"><span data-stu-id="d3783-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="d3783-108">Навыки для ресурсов оцениваются моделями квалификации.</span><span class="sxs-lookup"><span data-stu-id="d3783-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="d3783-109">Отдельные оценки находятся в модели квалификации.</span><span class="sxs-lookup"><span data-stu-id="d3783-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="d3783-110">Чтобы создать модель квалификации, выберите **Ресурсы** \> **Модели квалификации**, затем выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="d3783-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="d3783-111">В новой модели оценки укажите минимальное значение оценки, максимальное значение оценки и сущность, которая оценивается.</span><span class="sxs-lookup"><span data-stu-id="d3783-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="d3783-112">Во вложенной сетке **Значения оценок** можно определить различные значения оценки, от минимальной до максимальной.</span><span class="sxs-lookup"><span data-stu-id="d3783-112">In the **Rating Values** subgrid, you can define the different rating values, from the minimum to the maximum.</span></span>

> ![Определенные минимальные и максимальные оценки](media/Resource-Management-image85.png)

<span data-ttu-id="d3783-114">Эти значения оценок отображаются в фильтрах **Требования ресурсов**, **Таблица расписаний** и **Помощник по расписанию**.</span><span class="sxs-lookup"><span data-stu-id="d3783-114">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]