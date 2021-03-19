---
title: Отправка запроса ресурса
description: В этом разделе представлена информация об отправке запрос ресурса проекта.
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 8976ca2360be8676350178059615c59995544a71
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282259"
---
# <a name="submitting-a-resource-request"></a><span data-ttu-id="d7d89-103">Отправка запроса ресурса</span><span class="sxs-lookup"><span data-stu-id="d7d89-103">Submitting a resource request</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="d7d89-104">Можно отправить созданное требование ресурса в виде запроса ресурса.</span><span class="sxs-lookup"><span data-stu-id="d7d89-104">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="d7d89-105">Запрос затем отправляется руководителю по ресурсам для выполнения.</span><span class="sxs-lookup"><span data-stu-id="d7d89-105">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="d7d89-106">В Project Service Automation (PSA) на странице **Проекты**, щелкните вкладку **Рабочая группа** для просмотра списка резервируемых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d7d89-106">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab to view a list bookable resources.</span></span> 
2. <span data-ttu-id="d7d89-107">Выберите универсальный ресурс, имеющий требование ресурса, в списке, затем щелкните **Отправить запрос**.</span><span class="sxs-lookup"><span data-stu-id="d7d89-107">Select the generic resource that has a resource requirement from the list and then click **Submit Request**.</span></span>

![Отправка запроса ресурса](media/RM-how-to-18.png)

<span data-ttu-id="d7d89-109">Состояние запроса универсального участника рабочей группы изменяется на **Отправлен**.</span><span class="sxs-lookup"><span data-stu-id="d7d89-109">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="d7d89-110">После выполнения запроса менеджером по ресурсам универсальный ресурс будет заменен именованным ресурсом, если руководитель по ресурсам выполняет запрос с резервированием именованного ресурса.</span><span class="sxs-lookup"><span data-stu-id="d7d89-110">After the request is fulfilled by the resource manager, the generic resource will be replaced by a named resource if the resource manager fulfills the request with the booking of a named resource.</span></span> <span data-ttu-id="d7d89-111">В противном случае универсальный ресурс останется в рабочей группе, и его состояние изменится на **Требует проверки**, если руководитель по ресурсам предложил именованный ресурс.</span><span class="sxs-lookup"><span data-stu-id="d7d89-111">Otherwise, the generic resource will remain on the team and the request status will change to **Needs Review**, if the resource manager has proposed a named resource.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]