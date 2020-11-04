---
title: Включение функций мобильного приложения Project Finder Mobile
description: Как включить функций мобильного приложения Project Finder Mobile для Project Service
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
ms.openlocfilehash: 749c5682dc2e639843a0a8a085fe8af65502d433
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083195"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a><span data-ttu-id="70da2-103">Включение функций мобильного приложения Project Finder Mobile (Project Service)</span><span class="sxs-lookup"><span data-stu-id="70da2-103">Enable Project Finder Mobile app features (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="70da2-104">Ваши ресурсы могут использовать мобильное приложение Project Finder Mobile на телефоне с [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], чтобы находить новые проекты для работы и обновлять свои наборы навыков.</span><span class="sxs-lookup"><span data-stu-id="70da2-104">Your resources can use the Project Finder Mobile app on their phone with [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to find new projects to work on and update their skill sets.</span></span>  
  
 <span data-ttu-id="70da2-105">Приложение доступно для [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], телефонов [!INCLUDE[tn_android](../includes/tn-android.md)] и [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].</span><span class="sxs-lookup"><span data-stu-id="70da2-105">The app is available for [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] phones, and [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].</span></span>  
  
 <span data-ttu-id="70da2-106">Необходимо задать пару параметров в разделе настроек для вашего организационного подразделения, чтобы разрешить пользователям просматривать требования к ресурсам проекта и обновлять свои навыки.</span><span class="sxs-lookup"><span data-stu-id="70da2-106">You need to set a couple of options in the parameters setting for your organizational unit to allow users to view projects' resource requirements and update their skills.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="70da2-107">Приложение Project Finder Mobile работает только с [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], но не с локальными установками.</span><span class="sxs-lookup"><span data-stu-id="70da2-107">The Project Finder Mobile app only works with [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], not with on-premises installations.</span></span>  
  
1. <span data-ttu-id="70da2-108">Перейдите к разделу **Project Service > Параметры**.</span><span class="sxs-lookup"><span data-stu-id="70da2-108">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="70da2-109">Щелкните настройку параметров, которую нужно использовать для включения функций приложения Project Finder Mobile.</span><span class="sxs-lookup"><span data-stu-id="70da2-109">Click the parameters setting you want to use for allowing the Project Finder Mobile app features.</span></span>  
  
3. <span data-ttu-id="70da2-110">В разделе **Общие** для параметра **Требования к ресурсам видны для ресурсов** нажмите **Да**.</span><span class="sxs-lookup"><span data-stu-id="70da2-110">In the **General** area, set **Resource requirements visible to resources** to **Yes**.</span></span>  
  
4. <span data-ttu-id="70da2-111">Задайте для параметра **Разрешить ресурсу изменять навык** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="70da2-111">Set **Allow skill update by resource** to **Yes**.</span></span>  
  
   <span data-ttu-id="70da2-112">![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span><span class="sxs-lookup"><span data-stu-id="70da2-112">![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span></span>  
  
   <span data-ttu-id="70da2-113">Это глобальный параметр.</span><span class="sxs-lookup"><span data-stu-id="70da2-113">This is a global setting.</span></span> <span data-ttu-id="70da2-114">Руководители проекта могут указывать, будет ли тот или иной проект видим, на странице проекта **Рабочая группа проекта**.</span><span class="sxs-lookup"><span data-stu-id="70da2-114">Project managers can set whether an individual project will be visible on that project's **Project Team** page.</span></span>  
  
   <span data-ttu-id="70da2-115">![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span><span class="sxs-lookup"><span data-stu-id="70da2-115">![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span></span>  
  
## <a name="email-notifications"></a><span data-ttu-id="70da2-116">Уведомления по электронной почте</span><span class="sxs-lookup"><span data-stu-id="70da2-116">Email notifications</span></span>  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] <span data-ttu-id="70da2-117">отправляет электронные сообщения о запросах ресурсов следующим получателям в следующих ситуациях.</span><span class="sxs-lookup"><span data-stu-id="70da2-117">sends emails regarding resource requests to the following recipients at the following times:</span></span>  
  
|<span data-ttu-id="70da2-118">Получатель</span><span class="sxs-lookup"><span data-stu-id="70da2-118">Recipient</span></span>|<span data-ttu-id="70da2-119">Мероприятие</span><span class="sxs-lookup"><span data-stu-id="70da2-119">Event</span></span>|  
|---------------|-----------|  
|<span data-ttu-id="70da2-120">Руководитель проекта</span><span class="sxs-lookup"><span data-stu-id="70da2-120">Project manager</span></span>|<span data-ttu-id="70da2-121">- Когда ресурс регистрируется на проект с помощью приложения Project Finder Mobile.</span><span class="sxs-lookup"><span data-stu-id="70da2-121">-   When a resource signs up for a project with the Project Finder Mobile app.</span></span>|  
|<span data-ttu-id="70da2-122">Ресурс</span><span class="sxs-lookup"><span data-stu-id="70da2-122">Resource</span></span>|<span data-ttu-id="70da2-123">- Когда работа над проектом, на который зарегистрировался ресурс, уже выполнена другим ресурсом.</span><span class="sxs-lookup"><span data-stu-id="70da2-123">-   When the project work the resource has signed up for has already been fulfilled by another resource.</span></span><br /><span data-ttu-id="70da2-124">- Когда запрос на утверждение навыков обработан (положительно или отрицательно).</span><span class="sxs-lookup"><span data-stu-id="70da2-124">-   When their skill approval request has been approved or rejected.</span></span><br /><span data-ttu-id="70da2-125">- Когда запрос на регистрацию в проекте обработан (положительно или отрицательно).</span><span class="sxs-lookup"><span data-stu-id="70da2-125">-   When their project sign up request has been approved or rejected.</span></span>|  
  
## <a name="privacy-notice"></a><span data-ttu-id="70da2-126">Уведомление о конфиденциальности</span><span class="sxs-lookup"><span data-stu-id="70da2-126">Privacy notice</span></span>  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a><span data-ttu-id="70da2-127">См. также</span><span class="sxs-lookup"><span data-stu-id="70da2-127">See Also</span></span>  
 [<span data-ttu-id="70da2-128">Настройка ресурсов</span><span class="sxs-lookup"><span data-stu-id="70da2-128">Set up resources</span></span>](../psa/set-up-resources.md)
