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
# <a name="deploy-project-operations-lite-deployment--deal-to-proforma-invoicing"></a>Развертывание Project Operations Lite — от сделки до счетов-проформ

_**Относится к:** развертывание Lite — от сделки до счетов-проформ_

Project Operations поддерживает несколько моделей развертывания. Чтобы определить лучшую модель развертывания, см. раздел [Типы развертывания](determine-deployment-type.md).


> [!IMPORTANT]
> Это развертывание, упрощенное развертывание — от сделки до счетов-проформ, приводит к **развертыванию Project Operations только в Common Data Service**.

- [Установка Project Operations в новой среде CDS](#new)
- [Установка в существующую среду CDS](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a>Установка Project Operations в новой среде CDS

1. Как [глобальный администратор или администратор Power Platform](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) с лицензией Project Operations, создайте новую среду CDS в [центре администрирования PowerPlatform](https://admin.powerplatform.com). Убедись в том, что **База данных CDS** и **Приложения Dynamics 365** включены. Дополнительную информацию см. в разделе [Создание и управление средами в центре администрирования Power Platform](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
2. Выберите **Microsoft Dynamics 365 Project Operations** из списка развертывания приложений Dynamics 365.


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a>Установка Project Operations в существующей среде CDS

1. Как [глобальный администратор или администратор Power Platform](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) с лицензией Project Operations, найдите среду в [центре администрирования PowerPlatform](https://admin.powerplatform.com), в которой вы хотите установить Project Operations.
2. Установите **Microsoft Dynamics 365 Project Operations** из списка развертывания приложений Dynamics 365. Дополнительные сведения см. в статье [Управление приложениями Dynamics 365](https://docs.microsoft.com/power-platform/admin/manage-apps).


