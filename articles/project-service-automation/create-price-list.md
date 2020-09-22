---
title: Создание прайс-листа
description: Как создать прайс-лист в Project Service
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: bdd05aea-27a3-431d-9a80-2e220fb25e53
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 756af2fe3bc73d478b0355493aae6f0e49ac5835
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755045"
---
# <a name="create-a-price-list-project-service"></a><span data-ttu-id="c9810-103">Создание прайс-листа (Project Service)</span><span class="sxs-lookup"><span data-stu-id="c9810-103">Create a price list (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="c9810-104">Прайс-листы предоставляют шаблон, который ваши менеджеры по работе с клиентами могут использовать для создания ценовых предложений и проектов и для определения расходов по проекту.</span><span class="sxs-lookup"><span data-stu-id="c9810-104">Price lists provide a template your account managers can use for creating quotes and projects, and for establishing the costs of a project.</span></span> <span data-ttu-id="c9810-105">Они предоставляют постатейный список ролей и расходов с указанием цены по каждой из них, которую вы будете взимать.</span><span class="sxs-lookup"><span data-stu-id="c9810-105">They provide a line item list of roles and expenses, and the price you will charge for each.</span></span> <span data-ttu-id="c9810-106">Можно создать несколько прайс-листов, чтобы поддерживать отдельные структуры цен для разных регионов или каналов продаж.</span><span class="sxs-lookup"><span data-stu-id="c9810-106">You can create multiple price lists so that you can maintain separate price structures for different regions you sell your products in or for different sales channels.</span></span> <span data-ttu-id="c9810-107">Рекомендуется создать хотя бы один прайс-лист для каждой валюты, в которой планируется выставлять счета клиентам.</span><span class="sxs-lookup"><span data-stu-id="c9810-107">It’s a good idea to create at least one price list for every currency you plan to bill your customers in.</span></span>  
  
<span data-ttu-id="c9810-108">Чтобы можно было подготовить финансовую оценку работы, которую предстоит выполнить, проследите, чтобы каждый проект имел соответствующий список себестоимостей и цен продажи.</span><span class="sxs-lookup"><span data-stu-id="c9810-108">To create financial estimates for the work to be delivered, make sure every project has a backing cost and sales price list.</span></span> <span data-ttu-id="c9810-109">Настройте список себестоимостей и цен продажи, который по умолчанию будет применяться ко всем проектам, создаваемым в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="c9810-109">Set up a default cost and sales pricelist that applies to all projects created in your organization.</span></span>  
  
<span data-ttu-id="c9810-110">Прайс-листы опираются на категории ролей и расходов, поэтому перед созданием прайс-листа удостоверьтесь, что вы уже настроили категории ролей и расходов, которые вы предполагаете использовать при создании прайс-листа.</span><span class="sxs-lookup"><span data-stu-id="c9810-110">Price lists rely on roles and expense categories, so before you create a price list, make sure you’ve already configured the roles and expense categories you want to use while creating the price list.</span></span>  
  
1.  <span data-ttu-id="c9810-111">Перейдите к разделу **Project Service > Прайс-листы**.</span><span class="sxs-lookup"><span data-stu-id="c9810-111">Go to **Project Service > Price Lists**.</span></span>  
  
2.  <span data-ttu-id="c9810-112">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="c9810-112">Click **New**.</span></span>  
  
3.  <span data-ttu-id="c9810-113">В параметре **Контекст** выберите назначение создаваемого прайс-листа: **Стоимость**, **Покупка** или **Продажи**.</span><span class="sxs-lookup"><span data-stu-id="c9810-113">In **Context**, select whether this price list is for **Cost**, **Purchase**, or **Sales**.</span></span>  
  
4.  <span data-ttu-id="c9810-114">В параметре **Имя** введите имя для прайс-листа.</span><span class="sxs-lookup"><span data-stu-id="c9810-114">In **Name**, enter a name for the price list.</span></span>  
  
5.  <span data-ttu-id="c9810-115">В параметре **Валюта** выберите валюту, в которой вы планируете выставлять счета или калькулировать стоимость.</span><span class="sxs-lookup"><span data-stu-id="c9810-115">In **Currency**, select the currency you’re going to use for billing or costing.</span></span>  
  
6.  <span data-ttu-id="c9810-116">В параметре **Единица времени** укажите период времени, для которого указывается цена, например день или час.</span><span class="sxs-lookup"><span data-stu-id="c9810-116">In **Time Unit**, specify the period of time the price applies to, such as day or hour.</span></span>  
  
7.  <span data-ttu-id="c9810-117">Если требуется, заполните параметры **Дата начала**, **Дата окончания** и **Описание**.</span><span class="sxs-lookup"><span data-stu-id="c9810-117">Fill in the **Start Date**, **End Date**, and **Description** as needed.</span></span>  
  
8.  <span data-ttu-id="c9810-118">Щелкните **Сохранить**, чтобы создать запись и продолжить ее редактирование.</span><span class="sxs-lookup"><span data-stu-id="c9810-118">Click **Save** to create the record so you can continue editing it.</span></span>  
  
9. <span data-ttu-id="c9810-119">Чтобы добавить в прайс-лист цену роли, щелкните **+** в **Цены роли**.</span><span class="sxs-lookup"><span data-stu-id="c9810-119">To add a role price to the price list, click **+** under **Role prices**.</span></span>  
  
10. <span data-ttu-id="c9810-120">В области **Цена роли** введите детали, а затем щелкните **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="c9810-120">In the **Role Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="c9810-121">Если требуется, добавьте другие цены ролей.</span><span class="sxs-lookup"><span data-stu-id="c9810-121">Continue adding role prices as necessary.</span></span> <span data-ttu-id="c9810-122">По завершении щелкните **Сохранить** в правом нижнем углу экрана.</span><span class="sxs-lookup"><span data-stu-id="c9810-122">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
11. <span data-ttu-id="c9810-123">Чтобы добавить в прайс-лист цену категории расхода, щелкните **+** в **Цены категории**.</span><span class="sxs-lookup"><span data-stu-id="c9810-123">To add an expense category price to the price list, click **+** under **Category prices**.</span></span>  
  
12. <span data-ttu-id="c9810-124">В области **Цена категории проводки** введите детали, а затем щелкните **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="c9810-124">In the **Transaction Category Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="c9810-125">Если требуется, добавьте другие цены категорий.</span><span class="sxs-lookup"><span data-stu-id="c9810-125">Continue adding category prices as necessary.</span></span> <span data-ttu-id="c9810-126">По завершении щелкните **Сохранить** в правом нижнем углу экрана.</span><span class="sxs-lookup"><span data-stu-id="c9810-126">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
13. <span data-ttu-id="c9810-127">Чтобы добавить в прайс-лист дополнительные позиции, щелкните **+** в **Позиции прайс-листа**.</span><span class="sxs-lookup"><span data-stu-id="c9810-127">To add price list items to the price list, click **+** under **Price List Items**.</span></span>  
  
14. <span data-ttu-id="c9810-128">В области **Позиция прайс-листа** введите детали, а затем щелкните **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="c9810-128">In the **Price List Item** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="c9810-129">Если требуется, добавьте в прайс-лист другие позиции.</span><span class="sxs-lookup"><span data-stu-id="c9810-129">Continue adding price list items as necessary.</span></span> <span data-ttu-id="c9810-130">По завершении щелкните **Сохранить** в правом нижнем углу экрана.</span><span class="sxs-lookup"><span data-stu-id="c9810-130">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
15. <span data-ttu-id="c9810-131">Чтобы добавить в прайс-лист отношения территории, щелкните **+** в **Отношения территории**.</span><span class="sxs-lookup"><span data-stu-id="c9810-131">To add territory relationships to the price list, click **+** under **Territory Relationships**.</span></span>  
  
16. <span data-ttu-id="c9810-132">В окне **Новое соединение** введите детали, а затем щелкните **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="c9810-132">In the **New Connection** window, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="c9810-133">Если требуется, добавьте другие отношения территории.</span><span class="sxs-lookup"><span data-stu-id="c9810-133">Continue adding territory relationships as necessary.</span></span> <span data-ttu-id="c9810-134">По завершении щелкните **Сохранить** в правом нижнем углу экрана.</span><span class="sxs-lookup"><span data-stu-id="c9810-134">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="c9810-135">См. также</span><span class="sxs-lookup"><span data-stu-id="c9810-135">See Also</span></span>  
 [<span data-ttu-id="c9810-136">Настройка Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="c9810-136">Configure Project Service Automation</span></span>](../project-service/configure.md)
