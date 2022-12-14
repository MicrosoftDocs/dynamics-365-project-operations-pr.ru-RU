---
title: Развертывание Project Operations Lite
description: В этой статье содержится информация о том, как установить облегченное развертывание Project Operations — от сделки до счетов-проформ.
author: stsporen
ms.date: 11/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 2c508f56b3018b6a86fea78bcf9ee4136e90f385
ms.sourcegitcommit: 38cb012502cbd640abbc21a0912b195112b27ccb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/30/2022
ms.locfileid: "9810995"
---
# <a name="deploy-project-operations-lite"></a>Развертывание Project Operations Lite

_**Относится к:** развертывание Lite — от сделки до счетов-проформ_



Project Operations поддерживает несколько моделей развертывания. Чтобы определить лучшую модель развертывания, см. раздел [Типы развертывания](determine-deployment-type.md).


> [!IMPORTANT]
> Это развертывание, упрощенное развертывание — от сделки до счетов-проформ, приводит к **развертыванию Project Operations только в Dataverse**.

- [Установка Project Operations в новую среду Dataverse](#new)
- [Установка в существующую среду Dataverse](#existing)
- [Установка в существующую среду Dataverse с компонентами двойной записи](#existingdw)



## <a name="install-project-operations-lite-to-a-new-dataverse-environment"></a><a name="new"></a>Установка Project Operations Lite в новую среду Dataverse

1. В качестве [глобального администратора или администратора Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) с лицензией Project Operations создайте новую среду Dataverse в [центре администрирования PowerPlatform](https://admin.powerplatform.com). Убедитесь, что параметры **Создать базу данных для этой среды** и **Приложения Dynamics 365** включены. Дополнительную информацию см. в разделе [Создание и управление средами в центре администрирования Power Platform](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
1. Выбрать **Microsoft Dynamics 365 Project Operations** из списка развертывания приложений Dynamics 365.


## <a name="install-project-operations-lite-to-an-existing-dataverse-environment"></a><a name="existing"></a>Установка Project Operations Lite в существующую среду Dataverse 
1. Как [глобальный администратор или администратор Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) с лицензией Project Operations, найдите среду в [центре администрирования PowerPlatform](https://admin.powerplatform.com), в которой вы хотите установить Project Operations.
1. Установите **Microsoft Dynamics 365 Project Operations** из списка развертывания приложений Dynamics 365. Дополнительные сведения см. в статье [Управление приложениями Dynamics 365](/power-platform/admin/manage-apps).

## <a name="install-project-operations-lite-to-an-existing-dataverse-environment-where-dual-write-solutions-are-already-present"></a><a name="existingdw"></a>Установка Project Operations Lite в существующую среду Dataverse, в которой уже присутствуют решения для двойной записи

Если вы хотите продолжить работу с Project Operations в режиме упрощенного развертывания, выполните следующие действия:

1. Как [глобальный администратор или администратор Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) с лицензией Project Operations, найдите среду в [центре администрирования PowerPlatform](https://admin.powerplatform.com), в которой вы хотите установить Project Operations.
1. Установите **Microsoft Dynamics 365 Project Operations** из списка развертывания приложений Dynamics 365. Дополнительные сведения см. в статье [Управление приложениями Dynamics 365](/power-platform/admin/manage-apps).
1. Поскольку в вашей среде установлены компоненты для двойной записи, необходимые для интеграции с установленными приложениями для управления финансами и операциями, при установке Project Operations также будут установлены возможности и расширения, необходимые для интеграции связанных с проектами данных с приложениями для управления финансами и операциями Поскольку вы хотите использовать Project Operations в виде облегченного развертывания, эти компоненты интеграции следует удалить, так как они будут создавать ограничения и накладные расходы для облегченных сценариев развертывания. Вручную удалите решения **Двойная запись Dynamics 365 Project Operations** и **Сопоставления сущностей двойной записи Dynamics 365 Project Operations** , чтобы удалить эти компоненты.
1. Выберите **Project Operations -> Параметры -> Параметры**. Откройте страницу подробностей  **Параметры проекта** и установите в поле **Режим обновления решения** значение **Только Lite**. Это гарантирует, что при последующих обновлениях Project Operations компоненты интеграции не будут снова установлены в Project Operations.  

[!INCLUDE[footer-include](../includes/footer-banner.md)]
