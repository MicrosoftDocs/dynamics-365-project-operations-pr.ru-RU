---
title: Управление проектами и резервированиями в календаре Office 365
description: Как управлять проектами и резервированиями в календаре Office 365
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
- D365PS
- ProjectOperations
ms.openlocfilehash: b38affbfc8d339ac1a2093391286ea4c095207be8de2e8eeca558e6fcc5bcc07
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/06/2021
ms.locfileid: "6985450"
---
# <a name="manage-projects-and-bookings-in-your-calendar-project-service"></a>Управление проектами и резервированиями в календаре (Project Service)

> [!Note]
> УСТАРЕЛО: эта функция устарела и больше недоступна.

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 

Просматривайте личные встречи, резервирования работы над проектом и назначения заказов на работу выездного обслуживания с помощью календаря [!INCLUDE[pn_office_365](../includes/pn-office-365.md)].  
  
 Имя все в одном месте, управлять днем легко. Все ваши собрания, встречи, резервирования и задачи доступны в календаре [!INCLUDE[pn_office_365](../includes/pn-office-365.md)].  
  
 Если вы используете [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], вы также можете ввести личные встречи в представление записи времени Project Service. Это позволяет менеджерам по проектам и ресурсам знать вашу доступность для выполнения проектов. Это также экономит ваше время, поскольку вам не требуется вводить информацию о личных встречах дважды. Вы можете просто импортировать личные встречи из календаря в представление записи времени Project Service.  
  
 Календарь синхронизирует резервирования проектов и заказов на работу, начиная с текущей даты, на предстоящие четыре недели. Этот параметр невозможно изменить.  
  
 Поддерживается только односторонняя синхронизация из PSA в календарь [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]. Вы можете синхронизировать данные в обратном порядке. 
  
 Дополнительные сведения об использовании календаря [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] см. в разделе [Календарь в Outlook в Интернете для бизнеса](https://support.office.com/article/Calendar-in-Outlook-on-the-web-for-business-5219c457-d1fe-4c2f-9032-1a816b88e936).  
  
## <a name="setup"></a>Установка  
 Прежде чем вы сможете просматривать резервирования и управлять ими в календаре [!INCLUDE[pn_office_365](../includes/pn-office-365.md)], вам нужно настроить несколько элементов.  
  
- Вам понадобятся учетные данные глобального администратора или системного администратора [!INCLUDE[pn_office_365](../includes/pn-office-365.md)].  
  
- Администратор должен будет настроить профиль почтового сервера, и каждый пользователь должен будет настроить свой почтовый ящик. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Настройка обработки электронной почты через синхронизацию на стороне сервера](/dynamics365/customerengagement/on-premises/admin/set-up-server-side-synchronization-of-email-appointments-contacts-and-tasks)  
  
## <a name="turn-on-synchronization-for-your-organization-admin-task"></a>Включение синхронизации для организации (задача администратора)  
  
1.  В основном меню щелкните **Параметры** > **Администрирование**.  
  
2.  Нажмите **Системные параметры**.  
  
3.  Выберите вкладку **Синхронизация**.  
  
4.  В разделе **Выберите, нужно ли включать синхронизацию резервирований ресурсов с** установите флажок **Синхронизировать резервирования ресурсов с Outlook**.  
  
## <a name="turn-on-synchronization-for-your-user-profile-user-task"></a>Включение синхронизации для профиля пользователя (задача пользователя)  
  
1.  Нажмите кнопку **Параметры** в правом верхнем углу экрана.  
  
2.  Щелкните **Параметры**.  
  
3.  Выберите вкладку **Синхронизация**.  
  
4.  В разделе **Синхронизировать резервирования ресурсов с Outlook** установите флажок **Синхронизировать резервирования ресурсов с Outlook**.  
  
## <a name="import-your-personal-appointments-user-task"></a>Импорт личных встреч (задача пользователя)  
 Вы можете импортировать личные встречи из календаря в представление записи времени Project Service Automation.  
  
1. Откройте календарь [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] и щелкните **Импорт данных**.  
  
2. На экране фильтров выберите **Встречи из Exchange** и нажмите кнопку **Применить**.  
  
3. Система отобразит встречи в представлении записи времени как предложенные записи из текущей недели. Для добавления записей за другую неделю щелкните **Назад** или **Далее**.  
  
4. Выберите встречу, которую вы хотите добавить в представление записи времени Project Service Automation.  
  
5. Во всплывающем окне **Запись времени** выберите соответствующие параметры для преобразования встречи в представления записи времени Project Service Automation.  
  
6. Щелкните **Сохранить**.  
  
### <a name="see-also"></a>См. также  
 [Руководство по совместной работе и вводу данных о времени и расходах](../psa/time-expense-collaboration-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]