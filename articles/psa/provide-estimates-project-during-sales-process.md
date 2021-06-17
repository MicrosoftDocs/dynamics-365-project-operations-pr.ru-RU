---
title: Обеспечение оценки работы для проекта в процессе продаж
description: Как обеспечить оценки работы для проекта в процессе продаж в Project Service
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: d1daff101f9f0342bb691253fee1290d2335318c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998247"
---
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a><span data-ttu-id="e7ec7-103">Обеспечение оценки работы для проекта в процессе продаж (Project Service)</span><span class="sxs-lookup"><span data-stu-id="e7ec7-103">Provide work estimates for a project during the sales process (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="e7ec7-104">Во время процесса продаж можно разработать оценки продаж с нуля со строками предложения.</span><span class="sxs-lookup"><span data-stu-id="e7ec7-104">During the sales process, you can work out sales estimates from the ground up with quote lines.</span></span> <span data-ttu-id="e7ec7-105">Возможности [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] в [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] обеспечивают более научный и определенный способ работы с оценками продаж за счет разбивки рабочих элементов и связанных атрибутов, которые улучшают оценки для проекта в структурной декомпозиции работ.</span><span class="sxs-lookup"><span data-stu-id="e7ec7-105">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] provide a more scientific and deterministic way of coming up with sales estimates by breaking down work items and associating relevant attributes that contribute toward the estimates for the project in the work breakdown structure.</span></span>  
  
 <span data-ttu-id="e7ec7-106">После выигрыша продажи можно использовать связанную структурную декомпозицию работ в своем плане проекта, настраивая ее при необходимости для успешного завершения своего проекта.</span><span class="sxs-lookup"><span data-stu-id="e7ec7-106">Once you win the sale, you can use the associated work breakdown structure in your project plan, refining it as necessary for successful completion of your project.</span></span>  
  
## <a name="link-a-project-to-a-quote-line"></a><span data-ttu-id="e7ec7-107">Связь проекта со строкой предложения с расценками</span><span class="sxs-lookup"><span data-stu-id="e7ec7-107">Link a project to a quote line</span></span>  
 <span data-ttu-id="e7ec7-108">При создании строки предложения с расценками на основе проекта можно создать новый проект из строки предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="e7ec7-108">When creating a project-based quote line, you can create a new project from the quote line.</span></span> <span data-ttu-id="e7ec7-109">Затем можно использовать шаблоны проектов, которые являются либо предварительно настроенными стандартные планами проекта или финансовыми оценками, общими для организации, или скопировать план проекта и оценки из прошлого проекта.</span><span class="sxs-lookup"><span data-stu-id="e7ec7-109">You can then use project templates, which are either pre-configured standard project plans and financial estimates common to your organization, or a copy of a project plan and estimates from a past project.</span></span> <span data-ttu-id="e7ec7-110">При создании проекта выбор шаблона проекта обеспечивает основу для настройки плана проекта, оценок и требований роли.</span><span class="sxs-lookup"><span data-stu-id="e7ec7-110">When you create a project, choosing a project template provides a basis to refine the project plan, estimates, and role requirements.</span></span> <span data-ttu-id="e7ec7-111">После создания своего проекта из предложения с расценками проект автоматически связывается со строкой предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="e7ec7-111">By creating your project from the quote, the project is automatically associated with the quote line.</span></span>  
  
## <a name="project-estimate-components"></a><span data-ttu-id="e7ec7-112">Компоненты оценки проекта</span><span class="sxs-lookup"><span data-stu-id="e7ec7-112">Project estimate components</span></span>  
 <span data-ttu-id="e7ec7-113">Структурная декомпозиция работ в проекте обеспечивает способ разбивки рабочих элементов на задачи, ведение иерархии задач и назначение оценки необходимых усилий для завершения каждой задачи.</span><span class="sxs-lookup"><span data-stu-id="e7ec7-113">The work breakdown structure in a project provides a way to break down work into tasks, maintain a hierarchy of tasks, and assign an estimate of effort required to complete each task.</span></span> <span data-ttu-id="e7ec7-114">Также можно связать роли с задачей, чтобы указать оценку типа ресурса, который требуются для завершения задачи и расписание.</span><span class="sxs-lookup"><span data-stu-id="e7ec7-114">You can also associate roles to a task to indicate an estimate of the type of resource required to complete a task and a schedule.</span></span>  
  
 <span data-ttu-id="e7ec7-115">Структурная декомпозиция работ позволяет определить оценки по усилиям и расписанию.</span><span class="sxs-lookup"><span data-stu-id="e7ec7-115">The work breakdown structure helps you determine work effort and schedule estimates.</span></span> <span data-ttu-id="e7ec7-116">По умолчанию в проекте используются прайс-листы по умолчанию, определенные ранее.</span><span class="sxs-lookup"><span data-stu-id="e7ec7-116">By default, the project uses default price lists that you defined earlier.</span></span> <span data-ttu-id="e7ec7-117">Стоимость и цены продажи, определенные в прайс-листах, помогают определить финансовые оценки по разбивке работ по проекту.</span><span class="sxs-lookup"><span data-stu-id="e7ec7-117">The cost and sales prices defined in the price lists help determine financial estimates for the project’s work breakdown.</span></span>  
  
 <span data-ttu-id="e7ec7-118">Если проект связан с предложением с расценками и в предложении с расценками есть другой прайс-лист, отличный от прайс-листа по умолчанию, прайс-лист предложения с расценками используется для финансовых оценок.</span><span class="sxs-lookup"><span data-stu-id="e7ec7-118">If your project is associated with a quote, and the quote has a different price list from the default, the quote’s price list is used for financial estimates.</span></span>  
  
## <a name="import-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="e7ec7-119">Импорт оценок проекта в предложение с расценками</span><span class="sxs-lookup"><span data-stu-id="e7ec7-119">Import estimates from a project into a quote</span></span>  
 <span data-ttu-id="e7ec7-120">После внесения оценок проекта в проект можно импортировать эти оценки в строку предложения с расценками:</span><span class="sxs-lookup"><span data-stu-id="e7ec7-120">Once you have project estimates in the project, you can import these estimates into the quote line:</span></span>  
  
-   <span data-ttu-id="e7ec7-121">В **Сведения строки предложения с расценками** щелкните **Импортировать из оценок**.</span><span class="sxs-lookup"><span data-stu-id="e7ec7-121">In **Quote Line Details**, click **Import from estimates**.</span></span> 

-   <span data-ttu-id="e7ec7-122">Выберите, следует ли импортировать оценки проекта по типу транзакции, роли или уровню узла структурной декомпозиции работ.</span><span class="sxs-lookup"><span data-stu-id="e7ec7-122">Select whether to import project estimates summarized by transaction type, role, or work breakdown structure node level.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="e7ec7-123">См. также</span><span class="sxs-lookup"><span data-stu-id="e7ec7-123">See Also</span></span>  
 [<span data-ttu-id="e7ec7-124">Руководство менеджера по проектам</span><span class="sxs-lookup"><span data-stu-id="e7ec7-124">Project Manager Guide</span></span>](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]