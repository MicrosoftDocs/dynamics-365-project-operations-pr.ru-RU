---
title: Использование надстройки Project Service для планирования работы в Microsoft Project | MicrosoftDocs
description: В этом разделе представлена информация о том, как добавить, настроить и использовать надстройку Microsoft Project для Microsoft Project Service.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 04/06/2019
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
ms.openlocfilehash: 6bc74442866caccc02e53afc913a55aab81f9629
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129694"
---
# <a name="use-the-project-service-automation-add-in-to-plan-your-work-in-microsoft-project"></a>Использование надстройки Project Service Automation для планирования работы в Microsoft Project

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] упрощает планирование проектов, включая оценки. Вы можете определить работу, чтобы затраты, усилие и значение продаж были четкими при отправке окончательного предложения.  

 Теперь вы можете установить [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] и выполнять планирование работы в знакомой среде [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]. Используйте надежные возможности планирования и управления [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], а затем обновите план проекта в Project Service Automation.  

> [!IMPORTANT]
> - Чтобы вы могли использовать функцию управления документами SharePoint для хранения файлов [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] для проектов [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], администратор [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] должен включить управление документами. 
> - Приложение [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] совместимо только с [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.  

## <a name="download-and-install-the-add-in"></a>Загрузка и установка надстройки  
 Подготовьте сведения о входе в [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Они вам потребуются для подключения из [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] к [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

1.  В центре загрузки загрузите надстройку для поддерживаемой версии Project Service, [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) или [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).  

2.  Щелкните ссылку загрузки.  

3.  При завершении загрузки нажмите кнопку **Да** для установки надстройки.  

## <a name="configure-the-add-in"></a>Настройка надстройки  

1. Откройте [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] и перейдите на вкладку **Project Service**.  

2. Щелкните **Подключить**.  

3. Введите сведения для входа и щелкните **Войти**.  

   Теперь вы можете начать использовать надстройку.  

## <a name="read-from-a-template"></a>Чтение из шаблона  
 Выполните чтение из шаблона, который вы создали в [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] и скопировали в [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], чтобы начать планирование проекта. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Создание шаблона проекта (Project Service Automation)](../psa/create-project-template.md)  

1.  На вкладке **Project Service** щелкните **Чтение** > **Шаблон проекта Project Service Automation**.  

2.  Выберите шаблон проекта в списке и нажмите кнопку **Открыть**.  

    > [!NOTE]
    >  По умолчанию задачи, которые копируются из шаблона в Project, задаются для планирования вручную.  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a>Назначение ролей [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ресурсам проекта  

1.  Откройте проект и щелкните ленту **Задача**.  

2.  Щелкните меню **Диаграмма Ганта** и выберите **Ведомость ресурсов**.  

3.  В ведомости ресурсов щелкните раскрывающееся меню **Роль ресурса Project Service** и выберите роль Project Service Automation.  

## <a name="staff-your-project-with-resources"></a>Комплектация проекта ресурсами  

1.  На вкладке Project Service выберите строку и щелкните **Найти ресурсы**.  

2.  На экране **Зарезервировать ресурс** выберите ресурс, который вы хотите использовать для проекта.  

3.  Щелкните **Зарезервировать**, затем нажмите кнопку **OK**.  

## <a name="publish-your-project"></a>Публикация проекта  
По завершении планирования проекта следующим шагом будет импорт и публикация проекта в [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

Проект импортируется в [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Будут применены цены и процесс создания рабочих групп. Откройте проект в [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], чтобы просмотреть рабочую группу, оценки проекта и структурную декомпозицию работ. В следующей таблице показано, где можно найти результаты:


|                                                                                          |                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Диаграмма Ганта**   | Импорт на экран [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Структурная декомпозиция работ**. |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Лист ресурсов** |   Импорт на экран [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Участники рабочей группы проекта**.   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Использование использования**    |    Импорт на экран [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Оценки проекта**.     |

**Импорт и публикация проекта**  
1. На вкладке **Project Service** щелкните **Опубликовать** > **Новый проект Project Service Automation**.  

2. В диалоговом окне **Опубликовать в новом проекте Project Service** введите **Имя проекта** и выберите **Клиент**.  

3. Дополнительно установите флажок **Связать план проекта с Project Service Automation**, чтобы связать файл Project плана с Project Service Automation.  

4. Нажмите кнопку **Опубликовать**.  

   В результате связи файла Project с [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] файл Project становится шаблоном и задает структурную декомпозицию работ в [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] как доступную только для чтения.  Чтобы внести изменения в план проекта, вам нужно внести их в [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] и опубликовать как обновления в [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

## <a name="edit-a-project-thats-been-imported"></a>Изменение импортированного проекта  
 Для внесения изменений в план проекта, который был импортирован в [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], доступно два варианта:  

- Откройте файл шаблона и отредактируйте его в [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

- Отмените связь файла и отредактируйте его прямо в Project Service. По умолчанию проект, который был отправлен из [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], блокируется, и его можно отредактировать только в Project. Чтобы отредактировать файл в [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], необходимо удалить связь файла.  

### <a name="edit-in-pn_microsoft_project"></a>Изменение в [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]  

1. В основном меню щелкните **Project Service** > **Проекты**.  

2. В списке проектов откройте проект, созданный в [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Щелкните **Открыть в MS Project** в ленте. В результате откроется связанный файл шаблона в [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a>Отмена связи файла и его редактирование в [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service  

1. В основном меню щелкните **Project Service** > **Проекты**.  

2. В списке проектов откройте проект, созданный в [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Щелкните **Отменить связь из MS Project** в ленте.  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a>Отправка файла Project в SharePoint или группы Office  
 Вы можете отправить файл Project в SharePoint и найти его в разделе "Связанные документы" для проекта [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  Ваш администратор должен настроить управление документами SharePoint и включить его для сущности Project. 

 Вы также можете отправить файл Project в [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)], если у вас настроены группы Office Groups.

### <a name="upload-a-file-for-sharepoint"></a>Отправка файла в SharePoint  

1. В основном меню щелкните **Project Service** > **Отправить**.  

2. Выберите **В документы проекта Project Service Automation**.  

3. В диалоговом окне **Включить открытие в [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** выберите **Да** или **Нет**.  

   - Если щелкнуть **Да**, вы сможете нажать кнопку **Открыть в [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** в Project Service Automation, запустить [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] и отправить файл Project из библиотеки документов SharePoint.  

   - Если щелкнуть **Нет**, ссылка для кнопки **Открыть в [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** не будет работать.  

4. Файл [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] находится в [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] в разделе **Документы** для определенного проекта [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

### <a name="upload-a-file-for-office-groups"></a>Отправка файла для групп Office  

1. В основном меню щелкните **Project Service** > **Отправить**.  

2. Выберите **В документы проекта Project Service Automation**.  

3. В диалоговом окне **Включить открытие в [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** выберите **Да** или **Нет**.  

   - Если щелкнуть **Да**, вы сможете нажать кнопку **Открыть в [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** в Project Service Automation, запустить [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] и отправить файл Project из библиотеки документов SharePoint.  

   - Если щелкнуть **Нет**, ссылка для кнопки **Открыть в [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** не будет работать.  

4. Файл [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] находится в [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] в разделе **Документы** для определенного проекта [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

## <a name="publish--your-project-as-a-template"></a>Публикация проекта как шаблона  
 Вы можете сохранить проект и повторно использовать его, сохранив проект как шаблон проекта в [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  Шаблоны проекта — это многоразовые планы проектов в [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Создание шаблона проекта (Project Service Automation)](../psa/create-project-template.md)  

1. На вкладке **Project Service** щелкните **Опубликовать** > **Новый шаблон проекта Project Service Automation**.  

2. В диалоговом окне **Опубликовать в новом проекте в шаблоне Project Service** введите **Имя шаблона проекта**.  

3. При желании установите флажок **Связать план проекта с Project Service Automation**, чтобы связать файл Project с [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

4. Нажмите кнопку **Опубликовать**.  

В результате связи файла Project с [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] файл Project становится шаблоном и задает структурную декомпозицию работ в шаблоне [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] как доступную только для чтения.  Чтобы внести изменения в план проекта, вам нужно внести их в [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] и опубликовать как обновления в [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].

### <a name="see-also"></a>См. также  
 [Руководство менеджера по проектам](../psa/project-manager-guide.md)
