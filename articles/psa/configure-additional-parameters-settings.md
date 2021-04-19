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
ms.openlocfilehash: bac484e29f1a0578042f350b1657a42e80b48cb4
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290780"
---
# <a name="configure-additional-parameter-settings-project-service"></a><span data-ttu-id="807bd-103">Настройка дополнительных параметров (Project Service)</span><span class="sxs-lookup"><span data-stu-id="807bd-103">Configure additional parameter settings (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="807bd-104">После настройки элементов в предыдущих шагах нужно настроить дополнительные параметры проекта для проектов.</span><span class="sxs-lookup"><span data-stu-id="807bd-104">Once you’ve configured the items in previous topics, you need to set additional project parameters to use for your projects.</span></span> <span data-ttu-id="807bd-105">При первой установке [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] были созданы параметры для первого создания всех записей, необходимых для работы [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="807bd-105">When you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you created a parameters setting to first create all the records required for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to work.</span></span> <span data-ttu-id="807bd-106">Теперь пришло время, чтобы вернуться назад и настроить дополнительные поля для этих параметров.</span><span class="sxs-lookup"><span data-stu-id="807bd-106">Now it’s time to go back and configure additional fields for these settings.</span></span>  
  
 <span data-ttu-id="807bd-107">Необходимо настроить следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="807bd-107">You’ll need to have configured the following settings:</span></span>  
  
-   <span data-ttu-id="807bd-108">Подразделение</span><span class="sxs-lookup"><span data-stu-id="807bd-108">Organizational unit</span></span>  
  
-   <span data-ttu-id="807bd-109">Периодичность выставления счета</span><span class="sxs-lookup"><span data-stu-id="807bd-109">Invoice frequency</span></span>  
  
-   <span data-ttu-id="807bd-110">Шаблоны рабочих часов</span><span class="sxs-lookup"><span data-stu-id="807bd-110">Work hours template</span></span>  
  
-   <span data-ttu-id="807bd-111">Прайс-лист</span><span class="sxs-lookup"><span data-stu-id="807bd-111">Price list</span></span>  
 
<span data-ttu-id="807bd-112">На этом этапе также указывается, какой тип распределения ресурсов необходим:</span><span class="sxs-lookup"><span data-stu-id="807bd-112">In this step, you’ll also indicate what type of resource allocation you want:</span></span>  
  
- <span data-ttu-id="807bd-113">**Центральный**.</span><span class="sxs-lookup"><span data-stu-id="807bd-113">**Central**.</span></span> <span data-ttu-id="807bd-114">Только руководитель по ресурсам может распределять ресурсы для проектов.</span><span class="sxs-lookup"><span data-stu-id="807bd-114">Only resource managers can allocate resources to projects.</span></span>  
  
- <span data-ttu-id="807bd-115">**Гибридный**.</span><span class="sxs-lookup"><span data-stu-id="807bd-115">**Hybrid**.</span></span> <span data-ttu-id="807bd-116">Руководители по ресурсам, руководители проекта и менеджеры по работе с клиентами могут распределять ресурсы по проектам.</span><span class="sxs-lookup"><span data-stu-id="807bd-116">Resource managers, project managers, and account managers can allocate resources to projects.</span></span>  
  
 
<span data-ttu-id="807bd-117">Настройка параметров проекта:</span><span class="sxs-lookup"><span data-stu-id="807bd-117">To set project parameters:</span></span>  
  
1. <span data-ttu-id="807bd-118">Перейдите к разделу **Project Service > Параметры**.</span><span class="sxs-lookup"><span data-stu-id="807bd-118">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="807bd-119">Щелкните параметр, который требуется настроить (созданный при первой установке [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]) или щелкните **Создать** для создания нового.</span><span class="sxs-lookup"><span data-stu-id="807bd-119">Click the parameters setting you want to configure (the one you created when you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), or click **New** to create a new one.</span></span>  
  
3. <span data-ttu-id="807bd-120">В области **Общие сведения** настройте все параметры для параметров проекта.</span><span class="sxs-lookup"><span data-stu-id="807bd-120">In the **General** area, set all the options for your project parameters.</span></span>  
  
4. <span data-ttu-id="807bd-121">В области **Прайс-лист** щелкните **+** для добавления прайс-листа, выберите прайс-лист в раскрывающемся списке **Прайс-лист параметров проекта**, а затем щелкните **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="807bd-121">In the **Price List** area, click **+** to add a price list, select a price list in the **Project Parameter Price List** drop-down list, and then click **Save**.</span></span>  
  
5. <span data-ttu-id="807bd-122">Нажмите кнопку **Сохранить** в правом нижнем углу экрана.</span><span class="sxs-lookup"><span data-stu-id="807bd-122">Click the **Save** button in the bottom right corner of the screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="807bd-123">Для правильной работы Project Service необходимо вести запись параметров проекта.</span><span class="sxs-lookup"><span data-stu-id="807bd-123">The project parameter record must be maintained for Project Service to function correcly.</span></span> <span data-ttu-id="807bd-124">Удалять эту запись не следует.</span><span class="sxs-lookup"><span data-stu-id="807bd-124">This record should not be deleted.</span></span>

### <a name="see-also"></a><span data-ttu-id="807bd-125">См. также</span><span class="sxs-lookup"><span data-stu-id="807bd-125">See Also</span></span>  
 [<span data-ttu-id="807bd-126">Настройка ресурсов</span><span class="sxs-lookup"><span data-stu-id="807bd-126">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]