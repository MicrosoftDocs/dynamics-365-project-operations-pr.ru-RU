---
title: Разработка шаблонов проектов с помощью копирования проектов
description: Эта тема предоставляет информацию о том, как создавать шаблоны проектов с помощью настраиваемого действия копирования проекта.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cb49109e8c199bc4569702ae844a19985534294d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083128"
---
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="cb122-103">Разработка шаблонов проектов с помощью копирования проектов</span><span class="sxs-lookup"><span data-stu-id="cb122-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="cb122-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="cb122-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="cb122-105">Dynamics 365 Project Operations поддерживает возможность копирования проекта и возврата любых назначений обратно к универсальным ресурсам, представляющим роль.</span><span class="sxs-lookup"><span data-stu-id="cb122-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="cb122-106">Клиенты могут использовать эту функцию для создания базовых шаблонов проектов.</span><span class="sxs-lookup"><span data-stu-id="cb122-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="cb122-107">Когда вы выбираете действие **Копировать проект** , статус целевого проекта обновляется.</span><span class="sxs-lookup"><span data-stu-id="cb122-107">When you select **Copy Project** , the status of the target project is updated.</span></span> <span data-ttu-id="cb122-108">Используйте поле **Причина состояния** , чтобы определить, когда действие копирования завершено.</span><span class="sxs-lookup"><span data-stu-id="cb122-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="cb122-109">Выбор действия **Копировать проект** также обновляет дату начала проекта до текущей даты начала, если в целевой сущности проекта не обнаружена целевая дата.</span><span class="sxs-lookup"><span data-stu-id="cb122-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="cb122-110">Настраиваемое действие копирования проекта</span><span class="sxs-lookup"><span data-stu-id="cb122-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="cb122-111">Название</span><span class="sxs-lookup"><span data-stu-id="cb122-111">Name</span></span> 

<span data-ttu-id="cb122-112">**msdyn_CopyProjectV2**</span><span class="sxs-lookup"><span data-stu-id="cb122-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="cb122-113">Входные параметры</span><span class="sxs-lookup"><span data-stu-id="cb122-113">Input parameters</span></span>
<span data-ttu-id="cb122-114">Имеются три входных параметра:</span><span class="sxs-lookup"><span data-stu-id="cb122-114">There are three input parameters:</span></span>

| <span data-ttu-id="cb122-115">Параметр</span><span class="sxs-lookup"><span data-stu-id="cb122-115">Parameter</span></span>          | <span data-ttu-id="cb122-116">Тип</span><span class="sxs-lookup"><span data-stu-id="cb122-116">Type</span></span>   | <span data-ttu-id="cb122-117">Значения</span><span class="sxs-lookup"><span data-stu-id="cb122-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="cb122-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="cb122-118">ProjectCopyOption</span></span>  | <span data-ttu-id="cb122-119">String</span><span class="sxs-lookup"><span data-stu-id="cb122-119">String</span></span> | <span data-ttu-id="cb122-120">**{"removeNamedResources":true}** или **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="cb122-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="cb122-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="cb122-121">SourceProject</span></span>      | <span data-ttu-id="cb122-122">Ссылка на сущность</span><span class="sxs-lookup"><span data-stu-id="cb122-122">Entity Reference</span></span> | <span data-ttu-id="cb122-123">Исходный проект</span><span class="sxs-lookup"><span data-stu-id="cb122-123">Source Project</span></span> |
| <span data-ttu-id="cb122-124">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="cb122-124">Target</span></span>             | <span data-ttu-id="cb122-125">Ссылка на сущность</span><span class="sxs-lookup"><span data-stu-id="cb122-125">Entity Reference</span></span> | <span data-ttu-id="cb122-126">Целевой проект</span><span class="sxs-lookup"><span data-stu-id="cb122-126">Target Project</span></span> |


- <span data-ttu-id="cb122-127">**{"clearTeamsAndAssignments":true}** : поведение по умолчанию для Project для Интернета, и удаляет все назначения и участников рабочей группы.</span><span class="sxs-lookup"><span data-stu-id="cb122-127">**{"clearTeamsAndAssignments":true}** : Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="cb122-128">**{"removeNamedResources":true}** поведение по умолчанию для Project Operations, и возвратит назначения на универсальные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="cb122-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="cb122-129">Дополнительные сведения о значениях по умолчанию для действий см. в разделе [Использование действий веб-API](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span><span class="sxs-lookup"><span data-stu-id="cb122-129">For more defaults on actions, see [Use Web API actions](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="cb122-130">Указание полей для копирования</span><span class="sxs-lookup"><span data-stu-id="cb122-130">Specify fields to copy</span></span> 
<span data-ttu-id="cb122-131">Когда действие **Копировать проект** вызывается, оно смотрит на представление проекта **Копировать столбцы проекта** , чтобы определить, какие поля копировать при копировании проекта.</span><span class="sxs-lookup"><span data-stu-id="cb122-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>
