---
title: Отправка запроса ресурса
description: В этом разделе представлена информация об отправке запрос ресурса проекта.
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
author: JohnPBurrows
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
ms.openlocfilehash: da3e2798079816409ffbcfed911c05f3d51307fef22c48d112802927828faeb2
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/06/2021
ms.locfileid: "6985022"
---
# <a name="submitting-a-resource-request"></a>Отправка запроса ресурса

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Можно отправить созданное требование ресурса в виде запроса ресурса. Запрос затем отправляется руководителю по ресурсам для выполнения.

1. В Project Service Automation (PSA) на странице **Проекты**, щелкните вкладку **Рабочая группа** для просмотра списка резервируемых ресурсов. 
2. Выберите универсальный ресурс, имеющий требование ресурса, в списке, затем щелкните **Отправить запрос**.

![Отправка запроса ресурса.](media/RM-how-to-18.png)

Состояние запроса универсального участника рабочей группы изменяется на **Отправлен**.

После выполнения запроса менеджером по ресурсам универсальный ресурс будет заменен именованным ресурсом, если руководитель по ресурсам выполняет запрос с резервированием именованного ресурса. В противном случае универсальный ресурс останется в рабочей группе, и его состояние изменится на **Требует проверки**, если руководитель по ресурсам предложил именованный ресурс.


[!INCLUDE[footer-include](../includes/footer-banner.md)]