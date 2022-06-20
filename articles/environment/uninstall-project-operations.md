---
title: Удаление Dynamics 365 Project Operations
description: В этой статье представлена информация о том, как удалить Dynamics 365 Project Operations.
author: stsporen
ms.date: 11/09/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 33a505594d6db47b4f8a0c8a630a0836f424e7d5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911980"
---
# <a name="uninstall-dynamics-365-project-operations"></a>Удаление Dynamics 365 Project Operations 

_**Относится к:** Project Operations для сценариев на основе ресурсов/без запасов_

Чтобы удалить Dynamics 365 Project Operations, вам должна быть назначена роль администратора.

1. Перейдите в раздел **Параметры** > **Решения**.

    ![Страница параметров.](./media/uninstall-proj-ops-solutions.png)
  
2. Удалите решения в том порядке, в котором они перечислены в следующей таблице. 

    | Этап | Имя решения                                    | Заметка                                                                                         |
    |------|----------------------------------------------------|----------------------------------------------------------------------------------------------|
    | 1 | msdyn_ProjectServiceUpgrade_managed.cab            | Если не найдено, пропустите это решение.                                                            |
    | 2 | ProjectOperations_Anchor                           | Если не найдено, пропустите это решение.                                                            |
    | 3 | Dynamics365ProjectOperationsDualWriteEntityMaps    | Если не найдено, пропустите это решение.                                                            |
    | 4 | Dynamics365ProjectOperationsDualWrite              | Если не найдено, пропустите это решение.                                                            |
    | 5 | ProjectService                                     | Нет дополнительных примечаний.                                                                         |
    | 6 | ProjectServiceCore_Patch                           | Нет дополнительных примечаний.                                                                         |
    | 7 | ProjectServiceCore                                 | Нет дополнительных примечаний.                                                                         |
    | 8 | ProjectServiceDeprecatedComponents                 | Если не найдено, пропустите это решение.                                                            |
    | 9 | FieldServiceCommon                                 | Требуется для двойной записи с Dynamics 365 Finance или Dynamics 365 Supply Chain Management.   |
    | 10 | msdyn_AssetCommon                                  | Требуется для двойной записи с Dynamics 365 Finance или Dynamics 365 Supply Chain Management.   |
    | 11 | msdyn_TESA_Anchor                                  | Требуется для Dynamics 365 Field Service.                                                     |
    | 12 | msdyn_TESA_Patch                                   | Требуется для Dynamics 365 Field Service.                                                     |
    | 13 | msdyn_TESA                                         | Требуется для Dynamics 365 Field Service.                                                     |
    | 14 | ResourceSchedulingControls                         | Требуется для Dynamics 365 Field Service.                                                     |
    | 15 | MicrosoftDynamicsScheduling3_CumulativePatch       | Требуется для Dynamics 365 Field Service.                                                     |
    | 16 | MicrosoftDynamicsScheduling_Patch_xx               | Требуется для Dynamics 365 Field Service.                                                     |
    | 17 | MicrosoftDynamicsScheduling                        | Требуется для Dynamics 365 Field Service.                                                     |
    | 18 | Dynamics365FinanceAndOperationsAnchor              | Если не найдено, пропустите это решение.                                                            |
    | 19 | Dynamics365Notes                                   | Если не найдено, пропустите это решение.                                                            |
    | 20 | Dynamics365FinanceAndOperationsDualWriteEntityMaps | Если не найдено, пропустите это решение.                                                            |
    | 21 | DualWriteCore                                      | Если не найдено, пропустите это решение.                                                            |
    | 22 | Dynamics365AssetManagementApp                      | Если не найдено, пропустите это решение.                                                            |
    | 23 | Dynamics365AssetManagement                         | Если не найдено, пропустите это решение.                                                            |
    | 24 | Dynamics365SupplyChainExtended                     | Если не найдено, пропустите это решение.                                                            |
    | 25 | Dynamics365FinanceExtended                         | Если не найдено, пропустите это решение.                                                            |
    | 26 | HCMCommon                                          | Если не найдено, пропустите это решение.                                                            |
    | 27 | Dynamics365FinanceAndOperationsCommon              | Если не найдено, пропустите это решение.                                                            |
    | 28 | Сторона                                              | Если не найдено, пропустите это решение.                                                            |
    | 29 | Dynamics365Company                                 | Если не найдено, пропустите это решение.                                                            |
    | 30 | CurrencyExchangeRates                              | Если не найдено, пропустите это решение.                                                            |
    | 31 | AssetCommon                                        | Если не найдено, пропустите это решение.                                                            |
