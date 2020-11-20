---
title: Почему не удается удалить записи из сущности фактических значений?
description: В этом разделе представлена информация о том, почему нельзя удалить записи из сущности фактических данных.
author: JPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/6/2018
ms.topic: article
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
ms.openlocfilehash: b9b45e3ae0cd9273af4d2a5cd9cce30502c0aa78
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127174"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="425f6-103">Почему не удается удалить записи из сущности "Фактические значения"?</span><span class="sxs-lookup"><span data-stu-id="425f6-103">Why can’t I delete records from the Actuals entity?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="425f6-104">Project Service Automation (PSA) не позволяет удалять фактические значения, поскольку они служат как источник истины для транзакций, которые имеют финансовое влияние на последующие системы, такие как главная книга.</span><span class="sxs-lookup"><span data-stu-id="425f6-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="425f6-105">Если фактические значения можно было бы удалить, целостность транзакций финансовой отчетности оказалась бы под вопросом.</span><span class="sxs-lookup"><span data-stu-id="425f6-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="425f6-106">Чтобы поддерживать журнал аудита, клиенты должны использовать журналы для создания компенсирующих транзакций.</span><span class="sxs-lookup"><span data-stu-id="425f6-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>

