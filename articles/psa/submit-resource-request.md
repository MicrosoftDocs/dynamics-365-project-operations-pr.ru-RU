---
title: Отправка запроса ресурса
description: В этом разделе представлена информация об отправке запрос ресурса проекта.
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: bcea3d640d7e9ee2b071c55bff9ade3268edb319
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083281"
---
# <a name="submitting-a-resource-request"></a>Отправка запроса ресурса

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Можно отправить созданное требование ресурса в виде запроса ресурса. Запрос затем отправляется руководителю по ресурсам для выполнения.

1. В Project Service Automation (PSA) на странице **Проекты** , щелкните вкладку **Рабочая группа** для просмотра списка резервируемых ресурсов. 
2. Выберите универсальный ресурс, имеющий требование ресурса, в списке, затем щелкните **Отправить запрос**.

![Отправка запроса ресурса](media/RM-how-to-18.png)

Состояние запроса универсального участника рабочей группы изменяется на **Отправлен**.

После выполнения запроса менеджером по ресурсам универсальный ресурс будет заменен именованным ресурсом, если руководитель по ресурсам выполняет запрос с резервированием именованного ресурса. В противном случае универсальный ресурс останется в рабочей группе, и его состояние изменится на **Требует проверки** , если руководитель по ресурсам предложил именованный ресурс.
