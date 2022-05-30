---
title: Включение функций мобильного приложения Project Finder Mobile
description: Как включить функций мобильного приложения Project Finder Mobile для Project Service
author: JohnPBurrows
ms.prod: ''
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 3f8f23c1f32d94a514de9ae40bd07b3d8063824c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593701"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a>Включение функций мобильного приложения Project Finder Mobile (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Ваши ресурсы могут использовать мобильное приложение Project Finder Mobile на телефоне с [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], чтобы находить новые проекты для работы и обновлять свои наборы навыков.  
  
 Приложение доступно для [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], телефонов [!INCLUDE[tn_android](../includes/tn-android.md)] и [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].  
    
 Чтобы пользователи могли просматривать требования к ресурсам проекта и обновлять свои навыки, необходимо выбрать параметры в настройках параметров для вашего подразделения.
  
> [!NOTE]
>  Приложение Project Finder Mobile работает только с [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], но не с локальными установками.  
  
1. Перейдите к разделу **Project Service > Параметры**.  
  
2. Щелкните настройку параметров, которую нужно использовать для включения функций приложения Project Finder Mobile.  
  
3. В разделе **Общие** для параметра **Требования к ресурсам видны для ресурсов** нажмите **Да**.  
  
4. Задайте для параметра **Разрешить ресурсу изменять навык** значение **Да**.  
  
   ![ProjectService_ProjectFinderEnable.](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")  
  
   Это глобальный параметр. Руководители проекта могут указывать, будет ли тот или иной проект видим, на странице проекта **Рабочая группа проекта**.  
  
   ![ProjectService_ProjectTeamVisible.](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")  
  
## <a name="email-notifications"></a>Уведомления по электронной почте  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] отправляет электронные сообщения о запросах ресурсов следующим получателям в следующих ситуациях.  
  
|Получатель|Мероприятие|  
|---------------|-----------|  
|Руководитель проекта|- Когда ресурс регистрируется на проект с помощью приложения Project Finder Mobile.|  
|Ресурс|- Работа над проектом, на который зарегистрировался ресурс, уже выполнена другим ресурсом.<br />- Запрос на утверждение навыков обработан (положительно или отрицательно).<br />- Запрос на регистрацию в проекте обработан (положительно или отрицательно).|  
  
## <a name="privacy-notice"></a>Уведомление о конфиденциальности  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a>См. также  
 [Настройка ресурсов](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
