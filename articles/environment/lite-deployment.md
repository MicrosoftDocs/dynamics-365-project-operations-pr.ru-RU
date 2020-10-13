---
title: Развертывание Project Operations Lite — от сделки до счетов-проформ
description: Эта тема предоставляет информацию о том, как установить развертывание Project Operations Lite — от сделки до счетов-проформ.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e938876d459b3f6dfedd90e57e3042cda96bffb7
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949036"
---
# <a name="deploy-project-operations-lite-deployment--deal-to-proforma-invoicing"></a><span data-ttu-id="1d5ec-103">Развертывание Project Operations Lite — от сделки до счетов-проформ</span><span class="sxs-lookup"><span data-stu-id="1d5ec-103">Deploy Project Operations Lite deployment – deal to proforma invoicing</span></span>

<span data-ttu-id="1d5ec-104">_**Относится к:** развертывание Lite — от сделки до счетов-проформ_</span><span class="sxs-lookup"><span data-stu-id="1d5ec-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1d5ec-105">Project Operations поддерживает несколько моделей развертывания.</span><span class="sxs-lookup"><span data-stu-id="1d5ec-105">Project Operations supports multiple deployment models.</span></span> <span data-ttu-id="1d5ec-106">Чтобы определить лучшую модель развертывания, см. раздел [Типы развертывания](determine-deployment-type.md).</span><span class="sxs-lookup"><span data-stu-id="1d5ec-106">To determine the best deployment model, see [Deployment types](determine-deployment-type.md).</span></span>


> [!IMPORTANT]
> <span data-ttu-id="1d5ec-107">Это развертывание, упрощенное развертывание — от сделки до счетов-проформ, приводит к **развертыванию Project Operations только в Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="1d5ec-107">This deployment, Lite deployment – deal to proforma invoicing, results in a **Common Data Service-only deployment of Project Operations**.</span></span>

- [<span data-ttu-id="1d5ec-108">Установка Project Operations в новой среде CDS</span><span class="sxs-lookup"><span data-stu-id="1d5ec-108">Install Project Operations into a new CDS environment</span></span>](#new)
- [<span data-ttu-id="1d5ec-109">Установка в существующую среду CDS</span><span class="sxs-lookup"><span data-stu-id="1d5ec-109">Install into an existing CDS environment</span></span>](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a><span data-ttu-id="1d5ec-110">Установка Project Operations в новой среде CDS</span><span class="sxs-lookup"><span data-stu-id="1d5ec-110">Install Project Operations to a new CDS environment</span></span>

1. <span data-ttu-id="1d5ec-111">Как [глобальный администратор или администратор Power Platform](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) с лицензией Project Operations, создайте новую среду CDS в [центре администрирования PowerPlatform](https://admin.powerplatform.com).</span><span class="sxs-lookup"><span data-stu-id="1d5ec-111">As the [Global or Power Platform Administrator](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, create a new CDS environment in the [PowerPlatform admin center](https://admin.powerplatform.com).</span></span> <span data-ttu-id="1d5ec-112">Убедись в том, что **База данных CDS** и **Приложения Dynamics 365** включены.</span><span class="sxs-lookup"><span data-stu-id="1d5ec-112">Make sure that **CDS database** and **Dynamics 365 Apps** are enabled.</span></span> <span data-ttu-id="1d5ec-113">Дополнительную информацию см. в разделе [Создание и управление средами в центре администрирования Power Platform](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span><span class="sxs-lookup"><span data-stu-id="1d5ec-113">For more information, see [Create and manage environments in the Power Platform admin center](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span></span>
2. <span data-ttu-id="1d5ec-114">Выберите **Microsoft Dynamics 365 Project Operations** из списка развертывания приложений Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="1d5ec-114">Select **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span>


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a><span data-ttu-id="1d5ec-115">Установка Project Operations в существующей среде CDS</span><span class="sxs-lookup"><span data-stu-id="1d5ec-115">Install Project Operations to an existing CDS environment</span></span>

1. <span data-ttu-id="1d5ec-116">Как [глобальный администратор или администратор Power Platform](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) с лицензией Project Operations, найдите среду в [центре администрирования PowerPlatform](https://admin.powerplatform.com), в которой вы хотите установить Project Operations.</span><span class="sxs-lookup"><span data-stu-id="1d5ec-116">As the [Global or Power Platform Administrator](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, locate the environment in the [PowerPlatform admin center](https://admin.powerplatform.com) where you want to install Project Operations.</span></span>
2. <span data-ttu-id="1d5ec-117">Установите **Microsoft Dynamics 365 Project Operations** из списка развертывания приложений Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="1d5ec-117">Install **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span> <span data-ttu-id="1d5ec-118">Дополнительные сведения см. в статье [Управление приложениями Dynamics 365](https://docs.microsoft.com/power-platform/admin/manage-apps).</span><span class="sxs-lookup"><span data-stu-id="1d5ec-118">For more information, see [Manage Dynamics 365 apps](https://docs.microsoft.com/power-platform/admin/manage-apps).</span></span>


