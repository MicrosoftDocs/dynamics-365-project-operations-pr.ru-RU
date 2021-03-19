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
ms.openlocfilehash: e3122c5d9495b3ff9a683f477e719ce0c228a84d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286084"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="c8050-103">Почему не удается удалить записи из сущности "Фактические значения"?</span><span class="sxs-lookup"><span data-stu-id="c8050-103">Why can’t I delete records from the Actuals entity?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="c8050-104">Project Service Automation (PSA) не позволяет удалять фактические значения, поскольку они служат как источник истины для транзакций, которые имеют финансовое влияние на последующие системы, такие как главная книга.</span><span class="sxs-lookup"><span data-stu-id="c8050-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="c8050-105">Если фактические значения можно было бы удалить, целостность транзакций финансовой отчетности оказалась бы под вопросом.</span><span class="sxs-lookup"><span data-stu-id="c8050-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="c8050-106">Чтобы поддерживать журнал аудита, клиенты должны использовать журналы для создания компенсирующих транзакций.</span><span class="sxs-lookup"><span data-stu-id="c8050-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]