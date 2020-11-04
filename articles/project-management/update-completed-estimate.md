---
title: Обновление предварительной оценки по завершении
description: Эта тема предоставляет информацию об обновлении прогнозов усилий по проекту.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
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
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 16393133a5de17308caceb069d7bca670caa04c8
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083371"
---
# <a name="update-estimate-at-completion"></a><span data-ttu-id="f7697-103">Обновление предварительной оценки по завершении</span><span class="sxs-lookup"><span data-stu-id="f7697-103">Update estimate at completion</span></span>

<span data-ttu-id="f7697-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="f7697-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f7697-105">Руководители проекта часто пересматривают первоначальные оценки для задачи.</span><span class="sxs-lookup"><span data-stu-id="f7697-105">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="f7697-106">Повторное прогнозирование проекта является восприятием оценок руководителем проекта в соответствии с текущим состоянием проекта.</span><span class="sxs-lookup"><span data-stu-id="f7697-106">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="f7697-107">Однако не рекомендуется, чтобы руководители проектов изменяли значения в базовом плане проекта, поскольку базовый план проекта представляет определенный источник истинных значений для оценки графика выполнения и затрат проекта, согласованный со всеми заинтересованными лицами проекта.</span><span class="sxs-lookup"><span data-stu-id="f7697-107">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="f7697-108">Существует два способа, которыми руководитель проекта может изменить прогноз усилий по задачам:</span><span class="sxs-lookup"><span data-stu-id="f7697-108">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="f7697-109">Переопределить оценку для завершения (ETC) по умолчанию с новой оценкой фактических оставшихся усилий для задачи.</span><span class="sxs-lookup"><span data-stu-id="f7697-109">Override the default estimate to complete (ETC) with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="f7697-110">Переопределить процент хода выполнения по умолчанию с новой оценкой истинного хода выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="f7697-110">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="f7697-111">Каждый из этих способов приводит к повторному вычислению ETC, предварительной оценки по завершению (ПОПЗ) и процента выполнения задачи, а также прогнозируемого отклонения усилий для задачи.</span><span class="sxs-lookup"><span data-stu-id="f7697-111">Each of these approaches cause a recalculation of the task's ETC, estimate at complete (EAC), and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="f7697-112">ПОПЗ, ETC и процент выполнения сводных задач пересчитываются, и выдается новый прогноз отклонения усилий.</span><span class="sxs-lookup"><span data-stu-id="f7697-112">The EAC, ETC, and progress percentage on the summary tasks are recalculated, and produce a new projection of effort variance.</span></span>
