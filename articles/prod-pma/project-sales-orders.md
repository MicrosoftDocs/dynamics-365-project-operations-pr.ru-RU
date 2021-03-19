---
title: Заказы на продажу для временных и материальных проектов
description: В этой теме объясняется, как создавать заказы на продажу на основе проектов для временных и материальных проектов.
author: Yowelle
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 74a90ea0bdb8f760273c0f6b1c61bffcb70b6c8d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289070"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a><span data-ttu-id="01b9f-103">Заказы на продажу для временных и материальных проектов</span><span class="sxs-lookup"><span data-stu-id="01b9f-103">Project sales orders for time and material projects</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="01b9f-104">В этой теме описывается, как создать заказ на продажу для проекта.</span><span class="sxs-lookup"><span data-stu-id="01b9f-104">This topic describes how to create a sales order for a project.</span></span> <span data-ttu-id="01b9f-105">Заказы на продажу могут быть созданы только для проектов типа **время и материалы**.</span><span class="sxs-lookup"><span data-stu-id="01b9f-105">Sales orders can only be created for projects of type **time and material**.</span></span>

<span data-ttu-id="01b9f-106">Если у проекта "время и материалы" несколько источников финансирования в контракте по проекту, вы должны включить параметр **Разрешить заказы на продажу для проектов с несколькими источниками финансирования** на странице **Параметры управления проектом и учета**.</span><span class="sxs-lookup"><span data-stu-id="01b9f-106">If a time and material project has multiple funding sources on the project contract, you must enable the **Allow sales orders for projects with multiple funding sources** parameter on the **Project management and accounting parameters** page.</span></span> 

> [!NOTE]
> - <span data-ttu-id="01b9f-107">Поддержка заказов на продажу для проектов с несколькими источниками финансирования доступна с версии приложения 10.0.2 и выше.</span><span class="sxs-lookup"><span data-stu-id="01b9f-107">Support for project sales orders with multiple funding sources is available starting with application release 10.0.2 and higher.</span></span>
> - <span data-ttu-id="01b9f-108">Параметр, позволяющий включить поддержку заказов на продажу проектов с несколькими источниками финансирования, будет удален в волне выпуска в апреле 2020 года, после чего эта функция будет всегда включена.</span><span class="sxs-lookup"><span data-stu-id="01b9f-108">The parameter to enable the support for project sales orders with multiple funding sources will be removed in the April 2020 release wave, after which the functionality will always be enabled.</span></span>

<span data-ttu-id="01b9f-109">Вы можете создавать заказы на продажу на основе проекта двумя способами:</span><span class="sxs-lookup"><span data-stu-id="01b9f-109">You can create project-based sales orders in two ways:</span></span>

- <span data-ttu-id="01b9f-110">Перейдите в сам проект.</span><span class="sxs-lookup"><span data-stu-id="01b9f-110">Go to the project itself.</span></span> <span data-ttu-id="01b9f-111">На панели действий выберите **Управление > Задачи по номенклатуре > Заказ на продажу**.</span><span class="sxs-lookup"><span data-stu-id="01b9f-111">On the Action Pane, select **Manage > Item tasks > Sales order**.</span></span> <span data-ttu-id="01b9f-112">Информация о проекте по умолчанию будет соответствовать заказу на продажу из проекта.</span><span class="sxs-lookup"><span data-stu-id="01b9f-112">The project information will default to the sales order from the project.</span></span> <span data-ttu-id="01b9f-113">Если у контракта по проекту более одного источника финансирования, вам нужно будет выбрать источник финансирования, чтобы указать клиента для заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="01b9f-113">If the project contract has more than one funding source, you will need to select the funding source to set the customer for the sales order.</span></span> <span data-ttu-id="01b9f-114">Если для проекта есть только один источник финансирования, заказчик будет установлен автоматически.</span><span class="sxs-lookup"><span data-stu-id="01b9f-114">If there is only one funding source for the project, the customer will be automatically set.</span></span>
- <span data-ttu-id="01b9f-115">Перейдите на страницу списка **Все заказы на продажу** и создайте новый заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="01b9f-115">Go to the **All sales order** list page and create a new sales order.</span></span> <span data-ttu-id="01b9f-116">Вам нужно будет выбрать проект для заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="01b9f-116">You will need to select the project for the sales order.</span></span> <span data-ttu-id="01b9f-117">После выбора проекта заказчик будет выбран из источника финансирования, или вам нужно будет выбрать источник финансирования, если у контракта по проекту несколько источников финансирования.</span><span class="sxs-lookup"><span data-stu-id="01b9f-117">After the project is selected, the customer will be set from the funding source or you will need to select the funding source if the project contract has multiple funding sources.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]