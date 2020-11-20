---
title: Обновление проекта
description: В этой теме предоставлена информация об обновлении проектов в Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8bcbc6c5a62d252398d541649647fbad49006a0c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131449"
---
# <a name="update-a-project"></a><span data-ttu-id="08343-103">Обновление проекта</span><span class="sxs-lookup"><span data-stu-id="08343-103">Update a project</span></span>

<span data-ttu-id="08343-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="08343-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="08343-105">Ниже приводится сводка полей, которые могут быть обновлены в проекте после его создания, а также любые применимые последствия обновлений.</span><span class="sxs-lookup"><span data-stu-id="08343-105">Below is a summary of the fields that can be updated on a project after it has been created and any applicable implications of the updates.</span></span>

## <a name="project-detail-fields"></a><span data-ttu-id="08343-106">Поля сведений о проекте</span><span class="sxs-lookup"><span data-stu-id="08343-106">Project detail fields</span></span>

- <span data-ttu-id="08343-107">**Имя**: заголовок проекта.</span><span class="sxs-lookup"><span data-stu-id="08343-107">**Name**: The title of the project.</span></span>
- <span data-ttu-id="08343-108">**Описание**: обзор проекта.</span><span class="sxs-lookup"><span data-stu-id="08343-108">**Description**: An overview of the project.</span></span>
- <span data-ttu-id="08343-109">**Клиент**: компания, которой будет сдан проект.</span><span class="sxs-lookup"><span data-stu-id="08343-109">**Customer**: The company the project will be delivered to.</span></span>
- <span data-ttu-id="08343-110">**Шаблон календаря**: рабочие часы проекта.</span><span class="sxs-lookup"><span data-stu-id="08343-110">**Calendar template**: The working hours of the project.</span></span> <span data-ttu-id="08343-111">При изменении поля пересчитывается все расписание.</span><span class="sxs-lookup"><span data-stu-id="08343-111">When the field is changed, the entire schedule is recalculated.</span></span>
- <span data-ttu-id="08343-112">**Валюта**: валюта для проекта.</span><span class="sxs-lookup"><span data-stu-id="08343-112">**Currency**: The currency for the project.</span></span> <span data-ttu-id="08343-113">Значение по умолчанию в этом поле зависит от валюты, определенной в контрактной единице.</span><span class="sxs-lookup"><span data-stu-id="08343-113">This field defaults based on the currency defined in the contracting unit.</span></span> <span data-ttu-id="08343-114">При обновлении контрактной единицы также обновляется и это поле.</span><span class="sxs-lookup"><span data-stu-id="08343-114">When the contracting unit is updated, the field is also updated.</span></span>
- <span data-ttu-id="08343-115">**Единица по контракту**: подразделение, представляющее группу или подразделение компании, которое в первую очередь отвечает за обеспечение продажи и управление доставкой работы и услуг клиенту.</span><span class="sxs-lookup"><span data-stu-id="08343-115">**Contracting Unit**: The organizational unit that represents the company group or division that is primarily responsible for winning the sale and managing the delivery of work and services to the customer.</span></span> 
- <span data-ttu-id="08343-116">**Менеджер проекта**: участник рабочей группы проекта, имеющий право проверять и утверждать записи времени и расходы.</span><span class="sxs-lookup"><span data-stu-id="08343-116">**Project Manager**: The project team member who has the authority to review and approve time entries and expenses.</span></span>

## <a name="estimate-fields"></a><span data-ttu-id="08343-117">Поля оценки</span><span class="sxs-lookup"><span data-stu-id="08343-117">Estimate fields</span></span>

- <span data-ttu-id="08343-118">**Ожидаемая дата начала**: дата начала проекта.</span><span class="sxs-lookup"><span data-stu-id="08343-118">**Estimated Start Date**: The date that the project will begin.</span></span> <span data-ttu-id="08343-119">Когда это поле обновляется, любые задачи в проекте будут перемещаться пропорционально новой дате начала.</span><span class="sxs-lookup"><span data-stu-id="08343-119">When this field is updated, any tasks on the project will move proportionately with the start new start date.</span></span>
- <span data-ttu-id="08343-120">**Дата окончания**: дата, на которую планируется завершить проект.</span><span class="sxs-lookup"><span data-stu-id="08343-120">**Finish Date**: The date that the project is scheduled to end.</span></span>
- <span data-ttu-id="08343-121">**Трудозатраты**: предполагаемые трудозатраты по проекту.</span><span class="sxs-lookup"><span data-stu-id="08343-121">**Effort**: The estimated effort of the project.</span></span> <span data-ttu-id="08343-122">Когда задачи добавляются в проект, это поле становится недоступным для редактирования.</span><span class="sxs-lookup"><span data-stu-id="08343-122">When tasks are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="08343-123">**Оценка стоимости труда**: ориентировочная стоимость труда по проекту.</span><span class="sxs-lookup"><span data-stu-id="08343-123">**Estimated Labor Cost**: The estimated labor cost of the project.</span></span> <span data-ttu-id="08343-124">Когда стоимость труда добавляется в проект, это поле становится недоступным для редактирования.</span><span class="sxs-lookup"><span data-stu-id="08343-124">When labor costs are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="08343-125">**Ожидаемые расходы**: ориентировочные расходы по проекту.</span><span class="sxs-lookup"><span data-stu-id="08343-125">**Estimated Expenses**: The estimated expenses of the project.</span></span> <span data-ttu-id="08343-126">Когда расходы добавляются в проект, это поле становится недоступным для редактирования.</span><span class="sxs-lookup"><span data-stu-id="08343-126">When expenses are added to the project, this field is no longer editable.</span></span>

## <a name="project-actual-fields"></a><span data-ttu-id="08343-127">Поля фактических данных по проекту</span><span class="sxs-lookup"><span data-stu-id="08343-127">Project actual fields</span></span>
- <span data-ttu-id="08343-128">**Фактическое начало**: дата начала проекта.</span><span class="sxs-lookup"><span data-stu-id="08343-128">**Actual Start**: The date that the project started.</span></span>
- <span data-ttu-id="08343-129">**Фактическое окончание**: будет обновлено, когда проект будет завершен.</span><span class="sxs-lookup"><span data-stu-id="08343-129">**Actual Finish**: To be updated when a project has been completed.</span></span>

## <a name="project-status-fields"></a><span data-ttu-id="08343-130">Поля состояния проекта</span><span class="sxs-lookup"><span data-stu-id="08343-130">Project status fields</span></span>

- <span data-ttu-id="08343-131">**Общее состояние проекта**: общее состояние проекта, предоставленное менеджером проекта.</span><span class="sxs-lookup"><span data-stu-id="08343-131">**Overall Project Status**: The overall project health provided by the Project manager.</span></span>
- <span data-ttu-id="08343-132">**Комментарии**: описание текущего состояния проекта, предоставленное менеджером проекта.</span><span class="sxs-lookup"><span data-stu-id="08343-132">**Comments**: A narrative regarding the current health of the project provided by the Project manager.</span></span>

