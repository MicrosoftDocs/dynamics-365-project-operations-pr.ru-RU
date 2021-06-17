---
title: Развертывание Project Operations — облегченное
description: Эта тема предоставляет информацию о том, как установить развертывание Project Operations Lite — от сделки до счетов-проформ.
author: stsporen
ms.date: 10/02/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cb1f1ad86e19d84d68a40b32b2fdb08dc4777a78
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995547"
---
# <a name="deploy-project-operations---lite"></a><span data-ttu-id="3e541-103">Развертывание Project Operations — облегченное</span><span class="sxs-lookup"><span data-stu-id="3e541-103">Deploy Project Operations - lite</span></span>

<span data-ttu-id="3e541-104">_**Относится к:** развертывание Lite — от сделки до счетов-проформ_</span><span class="sxs-lookup"><span data-stu-id="3e541-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="3e541-105">Project Operations поддерживает несколько моделей развертывания.</span><span class="sxs-lookup"><span data-stu-id="3e541-105">Project Operations supports multiple deployment models.</span></span> <span data-ttu-id="3e541-106">Чтобы определить лучшую модель развертывания, см. раздел [Типы развертывания](determine-deployment-type.md).</span><span class="sxs-lookup"><span data-stu-id="3e541-106">To determine the best deployment model, see [Deployment types](determine-deployment-type.md).</span></span>


> [!IMPORTANT]
> <span data-ttu-id="3e541-107">Это развертывание, упрощенное развертывание — от сделки до счетов-проформ, приводит к **развертыванию Project Operations только в Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="3e541-107">This deployment, Lite deployment – deal to proforma invoicing, results in a **Common Data Service-only deployment of Project Operations**.</span></span>

- [<span data-ttu-id="3e541-108">Установка Project Operations в новой среде CDS</span><span class="sxs-lookup"><span data-stu-id="3e541-108">Install Project Operations into a new CDS environment</span></span>](#new)
- [<span data-ttu-id="3e541-109">Установка в существующую среду CDS</span><span class="sxs-lookup"><span data-stu-id="3e541-109">Install into an existing CDS environment</span></span>](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a><span data-ttu-id="3e541-110">Установка Project Operations в новой среде CDS</span><span class="sxs-lookup"><span data-stu-id="3e541-110">Install Project Operations to a new CDS environment</span></span>

1. <span data-ttu-id="3e541-111">Как [глобальный администратор или администратор Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) с лицензией Project Operations, создайте новую среду CDS в [центре администрирования PowerPlatform](https://admin.powerplatform.com).</span><span class="sxs-lookup"><span data-stu-id="3e541-111">As the [Global or Power Platform Administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, create a new CDS environment in the [PowerPlatform admin center](https://admin.powerplatform.com).</span></span> <span data-ttu-id="3e541-112">Убедись в том, что **База данных CDS** и **Приложения Dynamics 365** включены.</span><span class="sxs-lookup"><span data-stu-id="3e541-112">Make sure that **CDS database** and **Dynamics 365 Apps** are enabled.</span></span> <span data-ttu-id="3e541-113">Дополнительную информацию см. в разделе [Создание и управление средами в центре администрирования Power Platform](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span><span class="sxs-lookup"><span data-stu-id="3e541-113">For more information, see [Create and manage environments in the Power Platform admin center](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span></span>
2. <span data-ttu-id="3e541-114">Выбрать **Microsoft Dynamics 365 Project Operations** из списка развертывания приложений Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="3e541-114">Select **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span>


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a><span data-ttu-id="3e541-115">Установка Project Operations в существующей среде CDS</span><span class="sxs-lookup"><span data-stu-id="3e541-115">Install Project Operations to an existing CDS environment</span></span>

1. <span data-ttu-id="3e541-116">Как [глобальный администратор или администратор Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) с лицензией Project Operations, найдите среду в [центре администрирования PowerPlatform](https://admin.powerplatform.com), в которой вы хотите установить Project Operations.</span><span class="sxs-lookup"><span data-stu-id="3e541-116">As the [Global or Power Platform Administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, locate the environment in the [PowerPlatform admin center](https://admin.powerplatform.com) where you want to install Project Operations.</span></span>
2. <span data-ttu-id="3e541-117">Установите **Microsoft Dynamics 365 Project Operations** из списка развертывания приложений Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="3e541-117">Install **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span> <span data-ttu-id="3e541-118">Дополнительные сведения см. в статье [Управление приложениями Dynamics 365](/power-platform/admin/manage-apps).</span><span class="sxs-lookup"><span data-stu-id="3e541-118">For more information, see [Manage Dynamics 365 apps](/power-platform/admin/manage-apps).</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]