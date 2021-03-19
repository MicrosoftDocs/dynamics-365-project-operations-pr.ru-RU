---
title: Отправка запроса ресурса
description: Можно отправить созданное требование ресурса в виде запроса ресурса. Запрос затем отправляется руководителю по ресурсам для выполнения.
author: ruhercul
manager: Annbe
ms.date: 10/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: bc97af1ec90e60417c502eb329a85004e769e05b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279154"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="eb414-104">Отправка запроса ресурса</span><span class="sxs-lookup"><span data-stu-id="eb414-104">Submit a resource request</span></span>

<span data-ttu-id="eb414-105">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="eb414-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="eb414-106">Можно отправить созданное требование ресурса в виде запроса ресурса.</span><span class="sxs-lookup"><span data-stu-id="eb414-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="eb414-107">Запрос затем отправляется руководителю по ресурсам для выполнения.</span><span class="sxs-lookup"><span data-stu-id="eb414-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="eb414-108">В Dynamics 365 Project Operations на странице **Проекты**, щелкните выберите **Рабочая группа** для просмотра списка резервируемых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="eb414-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="eb414-109">Выберите универсальный ресурс, имеющий требование ресурса, в списке, затем щелкните **Отправить запрос**.</span><span class="sxs-lookup"><span data-stu-id="eb414-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="eb414-110">Состояние запроса универсального участника рабочей группы изменяется на **Отправлен**.</span><span class="sxs-lookup"><span data-stu-id="eb414-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="eb414-111">После выполнения запроса универсальный ресурс заменяется именованным ресурсом, если руководитель по ресурсам выполняет запрос путем резервирования именованного ресурса.</span><span class="sxs-lookup"><span data-stu-id="eb414-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="eb414-112">В противном случае, если менеджер по ресурсам предлагает именованный ресурс, универсальный ресурс останется в рабочей группе, и его состояние изменится на **Требует проверки**.</span><span class="sxs-lookup"><span data-stu-id="eb414-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]