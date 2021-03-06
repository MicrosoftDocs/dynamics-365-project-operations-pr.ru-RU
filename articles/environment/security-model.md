---
title: Модель безопасности
description: В этой теме предоставлена информация о модели безопасности в Dynamics 365 Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ffcfa8a9c8e31c5665acd3c3919fa90d36a3f3ca
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896747"
---
# <a name="security-model"></a>Модель безопасности

_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_

Microsoft Dynamics 365 Project Operations содержит уникальную модель безопасности, которая позволяет использовать ролевую модель безопасности бизнеса, которая взаимодействует с группами Microsoft Office. 


## <a name="security-roles"></a>Роли безопасности
Возможности внешнего интерфейса Project Operations включают следующие роли:

| Роль                          | Описание:                                                                                                                                                                 | Область. |
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|
| Руководитель по методикам              | Поддерживает отчетность по нескольким проектам.                                                                                                            | Бизнес-единица              |
| Утверждающий проекта              | Утверждает время и расходы по проекту.                                                                                                                              | Бизнес-единица |
| Администратор выставления счетов по проекту | Создает предложение по выставлению счетов.                                                                                                                                                 | Бизнес-единица |
| Руководитель проекта               | Создает план проекта и запрашивает ресурсы.                                                                                                                              | Бизнес-единица |
| Ресурс проекта              | Участники рабочих групп, которые могут быть зарезервированы и сообщают время.                                                                                                          | Бизнес-единица|
| Руководитель по ресурсам              | Все функции управления ресурсами, такие как выполнение запросов и резервирование ресурсов, разделены для поддержки гибридной конфигурации "Менеджер проектов + менеджер ресурсов" и единой централизованной роли менеджера ресурсов. | Бизнес-единица |


Microsoft Project для Интернета включает в себя следующие роли:
| Роль                          | Описание:                                                                                                          | Область. |                                                       
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----|
| Пользователь проекта | Коллективный пользователь Project, который может создавать свои собственные проекты и просматривать любые проекты, которыми с ним поделились.| Пользователь|
| Система проектов | Роль, используемая для контекста приложения. Клиенты не должны использовать эту системную роль. | Глобальные|

## <a name="security-enforcement"></a>Обеспечение безопасности
Действия, выполняемые на уровне проекта, выполняются в контексте вошедшего в систему пользователя. Это означает, что для создания, открытия или удаления проекта пользователь должен иметь доступ в CDS. Доступ в CDS может быть предоставлен через любой из возможных механизмов, включенных в платформу. Например, пользователь с большей областью действия может получить доступ к проекту или если было выполнено явное действие предоставления доступа к проекту, которое предоставляет пользователю доступ.

Это важно учитывать при создании проектов в Project Operations.

## <a name="modern-group-collaboration-with-project-operations"></a>Современное групповое сотрудничество с Project Operations
Project для Интернета и Project Operations поддерживают современные группы для совместной работы. Пользователи, добавленные в проект через группу, могут редактировать план проекта.

Project для Интернета автоматически добавляет пользователей в группу после назначения.

Группы позволяют совместно работать над разрешениями проекта и вспомогательными артефактами совместной работы. На следующей диаграмме показаны события и изменения состояния, которые происходят во время процесса назначения группы.

Project Operations не создает группу посредством неявного действия, а только посредством явного действия нажатия групп.

Поиск участников группы в диалоге **Управление группами** ограничен теми, кто настроен как часть группы безопасности среды. Подробнее см. в разделе [Управление доступом пользователей к средам: группы безопасности и лицензии](https://docs.microsoft.com/power-platform/admin/control-user-access).

1. Проект создается и принадлежит создавшему пользователю.
2. Владелец проекта обновлен до рабочей группы.
3. Группа владельцев сопоставлена с указанной или созданной группой Office.
4. Первоначальный владелец проекта добавляется в группу Office.

## <a name="deployment-recommendation"></a>Рекомендация по развертыванию
По мере развития модели совместной работы групп Office будут добавлены функции, обеспечивающие более подробный контроль со временем. Клиентам, развертывающим Project Operations сегодня, рекомендуется сосредоточиться на традиционной модели безопасности Microsoft Dynamics 365.

Дополнительные сведения см. в разделе [Безопасность в Common Data Service](https://docs.microsoft.com/power-platform/admin/wp-security).

## <a name="project-operations-and-microsoft-dynamics-365-finance-security"></a>Безопасность Project Operations и Microsoft Dynamics 365 Finance
Project Operations включает в себя следующие роли:

- Руководитель проекта
- Бухгалтер проекта

Дополнительные сведения о безопасности в Finance см. в разделе [Безопасность на основе ролей](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security).


