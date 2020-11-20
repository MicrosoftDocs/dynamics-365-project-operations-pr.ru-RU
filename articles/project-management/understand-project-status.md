---
title: Состояние проекта
description: В этой теме предоставлена информация о состоянии, назначенном проектам в Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: bc5bc174518e46b32cf88ea7231bb2df10fde292
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127309"
---
# <a name="understand-project-status"></a><span data-ttu-id="e1d20-103">Состояние проекта</span><span class="sxs-lookup"><span data-stu-id="e1d20-103">Understand project status</span></span>

<span data-ttu-id="e1d20-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="e1d20-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="e1d20-105">В разделе **Статус** на странице **Сущность проекта** представлена сводная информация о состоянии проекта с учетом затрат и усилий.</span><span class="sxs-lookup"><span data-stu-id="e1d20-105">The **Status** section on the **Project Entity** page provides a summary of a project's health based upon cost and effort.</span></span>


## <a name="status-summary-fields"></a><span data-ttu-id="e1d20-106">Поля сводки состояния</span><span class="sxs-lookup"><span data-stu-id="e1d20-106">Status summary fields</span></span>

- <span data-ttu-id="e1d20-107">Поле **Общее состояние проекта** — это изменяемое поле, которое показывает общее состояние проекта.</span><span class="sxs-lookup"><span data-stu-id="e1d20-107">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="e1d20-108">В этом поле используется кодирование цветами, такими как зеленый, желтый и красный, для обозначения возрастания риска.</span><span class="sxs-lookup"><span data-stu-id="e1d20-108">This field uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> 
- <span data-ttu-id="e1d20-109">Поле **Комментарии** позволяет руководителю проекта ввести конкретные комментарии о состоянии.</span><span class="sxs-lookup"><span data-stu-id="e1d20-109">The **Comments** field lets the project manager enter specific comments about the status.</span></span> 
- <span data-ttu-id="e1d20-110">Поле **Время обновления состояния** не редактируется.</span><span class="sxs-lookup"><span data-stu-id="e1d20-110">The **Status updated on** field isn't editable.</span></span> <span data-ttu-id="e1d20-111">Значение в этом поле представляет собой метку времени, которая указывает, когда статус был обновлен в последний раз.</span><span class="sxs-lookup"><span data-stu-id="e1d20-111">The value in this field is a timestamp that indicates when the status was last updated.</span></span>
- <span data-ttu-id="e1d20-112">Поля **Отклонение от календарного плана** и **Отклонение стоимости** задаются из сетки отслеживания.</span><span class="sxs-lookup"><span data-stu-id="e1d20-112">The **Schedule performance** and **Cost performance** fields are set from the tracking grid.</span></span> <span data-ttu-id="e1d20-113">Если расписание и отклонение стоимости для корневого узла в представлении **Отслеживание усилий** положительно, эти поля обновляются на значение **С опережением**.</span><span class="sxs-lookup"><span data-stu-id="e1d20-113">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, these fields are updated to **Ahead**.</span></span> <span data-ttu-id="e1d20-114">Если расписание и отклонение стоимости для корневого узла отрицательные, для этих полей задается значение **С опозданием**.</span><span class="sxs-lookup"><span data-stu-id="e1d20-114">When the schedule and cost variance for the root node are negative, these fields are set to **Behind**.</span></span>
