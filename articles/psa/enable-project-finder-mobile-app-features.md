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
# <a name="enable-project-finder-mobile-app-features-project-service"></a>Включение функций мобильного приложения Project Finder Mobile (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Ваши ресурсы могут использовать мобильное приложение Project Finder Mobile на телефоне с [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], чтобы находить новые проекты для работы и обновлять свои наборы навыков.  
  
 Приложение доступно для [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], телефонов [!INCLUDE[tn_android](../includes/tn-android.md)] и [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].  
  
 Необходимо задать пару параметров в разделе настроек для вашего организационного подразделения, чтобы разрешить пользователям просматривать требования к ресурсам проекта и обновлять свои навыки.  
  
> [!NOTE]
>  Приложение Project Finder Mobile работает только с [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], но не с локальными установками.  
  
1. Перейдите к разделу **Project Service > Параметры**.  
  
2. Щелкните настройку параметров, которую нужно использовать для включения функций приложения Project Finder Mobile.  
  
3. В разделе **Общие** для параметра **Требования к ресурсам видны для ресурсов** нажмите **Да**.  
  
4. Задайте для параметра **Разрешить ресурсу изменять навык** значение **Да**.  
  
   ![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")  
  
   Это глобальный параметр. Руководители проекта могут указывать, будет ли тот или иной проект видим, на странице проекта **Рабочая группа проекта**.  
  
   ![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")  
  
## <a name="email-notifications"></a>Уведомления по электронной почте  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] отправляет электронные сообщения о запросах ресурсов следующим получателям в следующих ситуациях.  
  
|Получатель|Мероприятие|  
|---------------|-----------|  
|Руководитель проекта|- Когда ресурс регистрируется на проект с помощью приложения Project Finder Mobile.|  
|Ресурс|- Когда работа над проектом, на который зарегистрировался ресурс, уже выполнена другим ресурсом.<br />- Когда запрос на утверждение навыков обработан (положительно или отрицательно).<br />- Когда запрос на регистрацию в проекте обработан (положительно или отрицательно).|  
  
## <a name="privacy-notice"></a>Уведомление о конфиденциальности  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a>См. также  
 [Настройка ресурсов](../psa/set-up-resources.md)
