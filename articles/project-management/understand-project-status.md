---
title: Состояние проекта
description: В этом разделе представлена информация о статусе, назначенном проектам в Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fc9b107507008fd2381d3669552d754d2c867a7f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286489"
---
# <a name="understand-project-status"></a><span data-ttu-id="e3e54-103">Состояние проекта</span><span class="sxs-lookup"><span data-stu-id="e3e54-103">Understand project status</span></span>

<span data-ttu-id="e3e54-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="e3e54-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="e3e54-105">В разделе **Статус** на странице **Сущность проекта** представлена сводная информация о состоянии проекта с учетом затрат и усилий.</span><span class="sxs-lookup"><span data-stu-id="e3e54-105">The **Status** section on the **Project Entity** page provides a summary of a project's health based upon cost and effort.</span></span>


## <a name="status-summary-fields"></a><span data-ttu-id="e3e54-106">Поля сводки состояния</span><span class="sxs-lookup"><span data-stu-id="e3e54-106">Status summary fields</span></span>

- <span data-ttu-id="e3e54-107">Поле **Общее состояние проекта** — это изменяемое поле, которое показывает общее состояние проекта.</span><span class="sxs-lookup"><span data-stu-id="e3e54-107">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="e3e54-108">В этом поле используется кодирование цветами, такими как зеленый, желтый и красный, для обозначения возрастания риска.</span><span class="sxs-lookup"><span data-stu-id="e3e54-108">This field uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> 
- <span data-ttu-id="e3e54-109">Поле **Комментарии** позволяет руководителю проекта ввести конкретные комментарии о состоянии.</span><span class="sxs-lookup"><span data-stu-id="e3e54-109">The **Comments** field lets the project manager enter specific comments about the status.</span></span> 
- <span data-ttu-id="e3e54-110">Поле **Время обновления состояния** не редактируется.</span><span class="sxs-lookup"><span data-stu-id="e3e54-110">The **Status updated on** field isn't editable.</span></span> <span data-ttu-id="e3e54-111">Значение в этом поле представляет собой метку времени, которая указывает, когда статус был обновлен в последний раз.</span><span class="sxs-lookup"><span data-stu-id="e3e54-111">The value in this field is a timestamp that indicates when the status was last updated.</span></span>
- <span data-ttu-id="e3e54-112">Поля **Отклонение от календарного плана** и **Отклонение стоимости** задаются из сетки отслеживания.</span><span class="sxs-lookup"><span data-stu-id="e3e54-112">The **Schedule performance** and **Cost performance** fields are set from the tracking grid.</span></span> <span data-ttu-id="e3e54-113">Если расписание и отклонение стоимости для корневого узла в представлении **Отслеживание усилий** положительно, эти поля обновляются на значение **С опережением**.</span><span class="sxs-lookup"><span data-stu-id="e3e54-113">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, these fields are updated to **Ahead**.</span></span> <span data-ttu-id="e3e54-114">Если расписание и отклонение стоимости для корневого узла отрицательные, для этих полей задается значение **С опозданием**.</span><span class="sxs-lookup"><span data-stu-id="e3e54-114">When the schedule and cost variance for the root node are negative, these fields are set to **Behind**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]