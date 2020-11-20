---
title: Обновление предварительной оценки по завершении
description: Эта тема предоставляет информацию об обновлении прогнозов усилий по проекту.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 59d04869839cebd6e197f94f2ada8ab12c495c3b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127219"
---
# <a name="update-estimate-at-completion"></a><span data-ttu-id="72923-103">Обновление предварительной оценки по завершении</span><span class="sxs-lookup"><span data-stu-id="72923-103">Update estimate at completion</span></span>

<span data-ttu-id="72923-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="72923-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="72923-105">Руководители проекта часто пересматривают первоначальные оценки для задачи.</span><span class="sxs-lookup"><span data-stu-id="72923-105">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="72923-106">Повторное прогнозирование проекта является восприятием оценок руководителем проекта в соответствии с текущим состоянием проекта.</span><span class="sxs-lookup"><span data-stu-id="72923-106">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="72923-107">Однако не рекомендуется, чтобы руководители проектов изменяли значения в базовом плане проекта, поскольку базовый план проекта представляет определенный источник истинных значений для оценки графика выполнения и затрат проекта, согласованный со всеми заинтересованными лицами проекта.</span><span class="sxs-lookup"><span data-stu-id="72923-107">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="72923-108">Существует два способа, которыми руководитель проекта может изменить прогноз усилий по задачам:</span><span class="sxs-lookup"><span data-stu-id="72923-108">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="72923-109">Переопределить оценку для завершения (ETC) по умолчанию с новой оценкой фактических оставшихся усилий для задачи.</span><span class="sxs-lookup"><span data-stu-id="72923-109">Override the default estimate to complete (ETC) with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="72923-110">Переопределить процент хода выполнения по умолчанию с новой оценкой истинного хода выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="72923-110">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="72923-111">Каждый из этих способов приводит к повторному вычислению ETC, предварительной оценки по завершению (ПОПЗ) и процента выполнения задачи, а также прогнозируемого отклонения усилий для задачи.</span><span class="sxs-lookup"><span data-stu-id="72923-111">Each of these approaches cause a recalculation of the task's ETC, estimate at complete (EAC), and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="72923-112">ПОПЗ, ETC и процент выполнения сводных задач пересчитываются, и выдается новый прогноз отклонения усилий.</span><span class="sxs-lookup"><span data-stu-id="72923-112">The EAC, ETC, and progress percentage on the summary tasks are recalculated, and produce a new projection of effort variance.</span></span>
