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
# <a name="deploy-project-operations---lite"></a>Развертывание Project Operations — облегченное

_**Относится к:** развертывание Lite — от сделки до счетов-проформ_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Project Operations поддерживает несколько моделей развертывания. Чтобы определить лучшую модель развертывания, см. раздел [Типы развертывания](determine-deployment-type.md).


> [!IMPORTANT]
> Это развертывание, упрощенное развертывание — от сделки до счетов-проформ, приводит к **развертыванию Project Operations только в Common Data Service**.

- [Установка Project Operations в новой среде CDS](#new)
- [Установка в существующую среду CDS](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a>Установка Project Operations в новой среде CDS

1. Как [глобальный администратор или администратор Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) с лицензией Project Operations, создайте новую среду CDS в [центре администрирования PowerPlatform](https://admin.powerplatform.com). Убедись в том, что **База данных CDS** и **Приложения Dynamics 365** включены. Дополнительную информацию см. в разделе [Создание и управление средами в центре администрирования Power Platform](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
2. Выбрать **Microsoft Dynamics 365 Project Operations** из списка развертывания приложений Dynamics 365.


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a>Установка Project Operations в существующей среде CDS

1. Как [глобальный администратор или администратор Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) с лицензией Project Operations, найдите среду в [центре администрирования PowerPlatform](https://admin.powerplatform.com), в которой вы хотите установить Project Operations.
2. Установите **Microsoft Dynamics 365 Project Operations** из списка развертывания приложений Dynamics 365. Дополнительные сведения см. в статье [Управление приложениями Dynamics 365](/power-platform/admin/manage-apps).




[!INCLUDE[footer-include](../includes/footer-banner.md)]