---
title: Настройка дополнительных параметров
description: Как настроить дополнительные параметры в Project Service
author: JohnPBurrows
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 5ce7ffd635b10689c8295d9349966450f11282d1
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129379"
---
# <a name="configure-additional-parameter-settings-project-service"></a><span data-ttu-id="83b0e-103">Настройка дополнительных параметров (Project Service)</span><span class="sxs-lookup"><span data-stu-id="83b0e-103">Configure additional parameter settings (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="83b0e-104">После настройки элементов в предыдущих шагах нужно настроить дополнительные параметры проекта для проектов.</span><span class="sxs-lookup"><span data-stu-id="83b0e-104">Once you’ve configured the items in previous topics, you need to set additional project parameters to use for your projects.</span></span> <span data-ttu-id="83b0e-105">При первой установке [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] были созданы параметры для первого создания всех записей, необходимых для работы [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="83b0e-105">When you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you created a parameters setting to first create all the records required for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to work.</span></span> <span data-ttu-id="83b0e-106">Теперь пришло время, чтобы вернуться назад и настроить дополнительные поля для этих параметров.</span><span class="sxs-lookup"><span data-stu-id="83b0e-106">Now it’s time to go back and configure additional fields for these settings.</span></span>  
  
 <span data-ttu-id="83b0e-107">Необходимо настроить следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="83b0e-107">You’ll need to have configured the following settings:</span></span>  
  
-   <span data-ttu-id="83b0e-108">Подразделение</span><span class="sxs-lookup"><span data-stu-id="83b0e-108">Organizational unit</span></span>  
  
-   <span data-ttu-id="83b0e-109">Периодичность выставления счета</span><span class="sxs-lookup"><span data-stu-id="83b0e-109">Invoice frequency</span></span>  
  
-   <span data-ttu-id="83b0e-110">Шаблоны рабочих часов</span><span class="sxs-lookup"><span data-stu-id="83b0e-110">Work hours template</span></span>  
  
-   <span data-ttu-id="83b0e-111">Прайс-лист</span><span class="sxs-lookup"><span data-stu-id="83b0e-111">Price list</span></span>  
 
<span data-ttu-id="83b0e-112">На этом этапе также указывается, какой тип распределения ресурсов необходим:</span><span class="sxs-lookup"><span data-stu-id="83b0e-112">In this step, you’ll also indicate what type of resource allocation you want:</span></span>  
  
- <span data-ttu-id="83b0e-113">**Центральный**.</span><span class="sxs-lookup"><span data-stu-id="83b0e-113">**Central**.</span></span> <span data-ttu-id="83b0e-114">Только руководитель по ресурсам может распределять ресурсы для проектов.</span><span class="sxs-lookup"><span data-stu-id="83b0e-114">Only resource managers can allocate resources to projects.</span></span>  
  
- <span data-ttu-id="83b0e-115">**Гибридный**.</span><span class="sxs-lookup"><span data-stu-id="83b0e-115">**Hybrid**.</span></span> <span data-ttu-id="83b0e-116">Руководители по ресурсам, руководители проекта и менеджеры по работе с клиентами могут распределять ресурсы по проектам.</span><span class="sxs-lookup"><span data-stu-id="83b0e-116">Resource managers, project managers, and account managers can allocate resources to projects.</span></span>  
  
 
<span data-ttu-id="83b0e-117">Настройка параметров проекта:</span><span class="sxs-lookup"><span data-stu-id="83b0e-117">To set project parameters:</span></span>  
  
1. <span data-ttu-id="83b0e-118">Перейдите к разделу **Project Service > Параметры**.</span><span class="sxs-lookup"><span data-stu-id="83b0e-118">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="83b0e-119">Щелкните параметр, который требуется настроить (созданный при первой установке [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]) или щелкните **Создать** для создания нового.</span><span class="sxs-lookup"><span data-stu-id="83b0e-119">Click the parameters setting you want to configure (the one you created when you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), or click **New** to create a new one.</span></span>  
  
3. <span data-ttu-id="83b0e-120">В области **Общие сведения** настройте все параметры для параметров проекта.</span><span class="sxs-lookup"><span data-stu-id="83b0e-120">In the **General** area, set all the options for your project parameters.</span></span>  
  
4. <span data-ttu-id="83b0e-121">В области **Прайс-лист** щелкните **+** для добавления прайс-листа, выберите прайс-лист в раскрывающемся списке **Прайс-лист параметров проекта**, а затем щелкните **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="83b0e-121">In the **Price List** area, click **+** to add a price list, select a price list in the **Project Parameter Price List** drop-down list, and then click **Save**.</span></span>  
  
5. <span data-ttu-id="83b0e-122">Нажмите кнопку **Сохранить** в правом нижнем углу экрана.</span><span class="sxs-lookup"><span data-stu-id="83b0e-122">Click the **Save** button in the bottom right corner of the screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="83b0e-123">Для правильной работы Project Service необходимо вести запись параметров проекта.</span><span class="sxs-lookup"><span data-stu-id="83b0e-123">The project parameter record must be maintained for Project Service to function correcly.</span></span> <span data-ttu-id="83b0e-124">Удалять эту запись не следует.</span><span class="sxs-lookup"><span data-stu-id="83b0e-124">This record should not be deleted.</span></span>

### <a name="see-also"></a><span data-ttu-id="83b0e-125">См. также</span><span class="sxs-lookup"><span data-stu-id="83b0e-125">See Also</span></span>  
 [<span data-ttu-id="83b0e-126">Настройка ресурсов</span><span class="sxs-lookup"><span data-stu-id="83b0e-126">Set up resources</span></span>](../psa/set-up-resources.md)
