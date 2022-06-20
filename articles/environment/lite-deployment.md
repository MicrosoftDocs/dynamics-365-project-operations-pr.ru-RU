---
title: Развертывание Project Operations — облегченное
description: В этой статье содержится информация о том, как установить облегченное развертывание Project Operations — от сделки до счетов-проформ.
author: stsporen
ms.date: 02/28/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 86293b725e86db3d4b8bdaf5810b16b7c670e8a3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930334"
---
# <a name="deploy-project-operations---lite"></a>Развертывание Project Operations — облегченное

_**Относится к:** развертывание Lite — от сделки до счетов-проформ_



Project Operations поддерживает несколько моделей развертывания. Чтобы определить лучшую модель развертывания, см. раздел [Типы развертывания](determine-deployment-type.md).


> [!IMPORTANT]
> Это развертывание, упрощенное развертывание — от сделки до счетов-проформ, приводит к **развертыванию Project Operations только в Dataverse**.

- [Установка Project Operations в новую среду Dataverse](#new)
- [Установка в существующую среду Dataverse](#existing)



## <a name="install-project-operations-to-a-new-dataverse-environment"></a><a name="new"></a>Установка Project Operations в новую среду Dataverse

1. В качестве [глобального администратора или администратора Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) с лицензией Project Operations создайте новую среду Dataverse в [центре администрирования PowerPlatform](https://admin.powerplatform.com). Убедитесь, что параметры **Создать базу данных для этой среды** и **Приложения Dynamics 365** включены. Дополнительную информацию см. в разделе [Создание и управление средами в центре администрирования Power Platform](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
2. Выбрать **Microsoft Dynamics 365 Project Operations** из списка развертывания приложений Dynamics 365.


## <a name="install-project-operations-to-an-existing-dataverse-environment"></a><a name="existing"></a>Установка Project Operations в существующую среду Dataverse
1. Убедитесь, что в среде не настроена [двойная запись](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview), поскольку в таком случае при установке будут установлены возможности [Project Operations для сценариев на основе ресурсов/без запасов](project-operations-integrated-deployment-overview.md).
2. Как [глобальный администратор или администратор Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) с лицензией Project Operations, найдите среду в [центре администрирования PowerPlatform](https://admin.powerplatform.com), в которой вы хотите установить Project Operations.
3. Установите **Microsoft Dynamics 365 Project Operations** из списка развертывания приложений Dynamics 365. Дополнительные сведения см. в статье [Управление приложениями Dynamics 365](/power-platform/admin/manage-apps).




[!INCLUDE[footer-include](../includes/footer-banner.md)]
