---
title: Почему не удается удалить записи из сущности фактических значений?
description: В этом разделе представлена информация о том, почему нельзя удалить записи из сущности фактических данных.
author: JPBurrows
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 11/6/2018
ms.topic: article
ms.prod: Project Service
ms.technology: Applies to all versions of Project Service
ms.assetid: ff504c34-7337-474f-89e8-d8afdd1e0a98
ms.author: Jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5817940933c161dccac0fe549fabacbe57e7077a
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754909"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a>Почему не удается удалить записи из сущности "Фактические значения"?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Project Service Automation (PSA) не позволяет удалять фактические значения, поскольку они служат как источник истины для транзакций, которые имеют финансовое влияние на последующие системы, такие как главная книга. Если фактические значения можно было бы удалить, целостность транзакций финансовой отчетности оказалась бы под вопросом. Чтобы поддерживать журнал аудита, клиенты должны использовать журналы для создания компенсирующих транзакций.

