---
title: Настройка ролей ресурсов
description: Порядок настройки ролей ресурсов в Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 5f899d17980df16602c964bab4bbab1e976b3ebf
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083186"
---
# <a name="configure-resource-roles-project-service"></a><span data-ttu-id="db3b4-103">Настройка ролей ресурсов (Project Service)</span><span class="sxs-lookup"><span data-stu-id="db3b4-103">Configure resource roles (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="db3b4-104">Роли имеют важное значение для планирования проекта при определении потребностей в ресурсах и расходов по проекту.</span><span class="sxs-lookup"><span data-stu-id="db3b4-104">Roles play an important part in project planning, when determining resource requirements or costs of a project.</span></span> <span data-ttu-id="db3b4-105">Для каждой роли, которая нужна для проекта, необходимо создать роль ресурса и связать с этой ролью навыки и квалификацию.</span><span class="sxs-lookup"><span data-stu-id="db3b4-105">For each role your projects require, you need to create a resource role and associate skills and proficiencies to that role.</span></span> <span data-ttu-id="db3b4-106">Например, может потребоваться создать роли для разработчика, руководителя проекта или тестировщика игры.</span><span class="sxs-lookup"><span data-stu-id="db3b4-106">For example, you might want to create roles for developer, project manager, or game tester.</span></span> <span data-ttu-id="db3b4-107">Также потребуется настроить уровни навыков и квалификации, требуемые для каждой роли.</span><span class="sxs-lookup"><span data-stu-id="db3b4-107">You’ll also set the skills and proficiency levels required for the role.</span></span>  
  
 <span data-ttu-id="db3b4-108">Назначьте роли ресурса, чтобы обеспечить эффективную оценку реализуемости проекта для своей организации.</span><span class="sxs-lookup"><span data-stu-id="db3b4-108">Configure resource roles to ensure effective project estimation for your organization.</span></span>  <span data-ttu-id="db3b4-109">Также проследите, чтобы был точно указан тип выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="db3b4-109">Also make sure you accurately set the billing type.</span></span> <span data-ttu-id="db3b4-110">Позиция, настроенная как "не подлежащая оплате", не отображается в контракте или ценовом предложении.</span><span class="sxs-lookup"><span data-stu-id="db3b4-110">An item set with a non-chargeable billing type doesn’t show up on contract or quote lines.</span></span>  
  
 <span data-ttu-id="db3b4-111">После того как роли ресурсов настроены, можно приступить к настройке себестоимостей и цен продажи с использованием прайс-листа.</span><span class="sxs-lookup"><span data-stu-id="db3b4-111">Once you’ve set up resource roles, you can set up cost and sales prices with a price list.</span></span>  
  
 <span data-ttu-id="db3b4-112">Для каждой роли, которую требуется добавить, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="db3b4-112">For each role you want to add, do the following:</span></span>  
  
1.  <span data-ttu-id="db3b4-113">Перейдите к разделу **Project Service > Роли ресурса**.</span><span class="sxs-lookup"><span data-stu-id="db3b4-113">Go to **Project Service > Resource Roles**.</span></span>  
  
2.  <span data-ttu-id="db3b4-114">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="db3b4-114">Click **New**.</span></span>  
  
3.  <span data-ttu-id="db3b4-115">В области **Общие сведения** введите имя роли в поле **Имя** , при необходимости заполните другие поля.</span><span class="sxs-lookup"><span data-stu-id="db3b4-115">In the **General** area, enter a name for the role in **Name** , and then fill in the other fields as necessary.</span></span>  
  
4.  <span data-ttu-id="db3b4-116">Щелкните **Сохранить** , чтобы создать запись и продолжить ее редактирование.</span><span class="sxs-lookup"><span data-stu-id="db3b4-116">Click **Save** to create the record so you can continue editing it.</span></span>  
  
5.  <span data-ttu-id="db3b4-117">В области **Навыки** щелкните **+** , чтобы добавить навык.</span><span class="sxs-lookup"><span data-stu-id="db3b4-117">In the **Skills** area, click **+** to add a skill.</span></span>  
  
6.  <span data-ttu-id="db3b4-118">В области **Требование компетентности роли** щелкните в поле **Навык** , щелкните кнопку **Поиск** , а затем выберите навык.</span><span class="sxs-lookup"><span data-stu-id="db3b4-118">In the **Role competency requirement** pane, click in the **Skill** field, click the **Search** button, and then select a skill.</span></span>  
  
7.  <span data-ttu-id="db3b4-119">Выберите квалификацию для этого навыка, а затем щелкните **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="db3b4-119">Select a proficiency for that skill, and then click **Save**.</span></span>  
  
8.  <span data-ttu-id="db3b4-120">Если требуется, добавьте другие навыки.</span><span class="sxs-lookup"><span data-stu-id="db3b4-120">Continue adding skills as necessary.</span></span> <span data-ttu-id="db3b4-121">По завершении щелкните **Сохранить** в правом нижнем углу экрана.</span><span class="sxs-lookup"><span data-stu-id="db3b4-121">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
9. <span data-ttu-id="db3b4-122">Чтобы сделать эту роль ресурса доступной для использования в проектах, щелкните **Активировать**.</span><span class="sxs-lookup"><span data-stu-id="db3b4-122">To make this resource role available for projects to use, click **Activate**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="db3b4-123">См. также</span><span class="sxs-lookup"><span data-stu-id="db3b4-123">See Also</span></span>  
 [<span data-ttu-id="db3b4-124">Настройка ресурсов</span><span class="sxs-lookup"><span data-stu-id="db3b4-124">Set up resources</span></span>](../psa/set-up-resources.md)
