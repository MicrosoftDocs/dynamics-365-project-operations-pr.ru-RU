---
title: Заметки разработчика для утверждений
description: Эта тема предоставляет дополнительную информацию для разработчика о работе с утверждениями.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: a89ea669a262c145b9f391fddc19e79a425fabb5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996807"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="2a8fd-103">Заметки разработчика для утверждений</span><span class="sxs-lookup"><span data-stu-id="2a8fd-103">Developer notes for Approvals</span></span>

<span data-ttu-id="2a8fd-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="2a8fd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2a8fd-105">Dynamics 365 Project Operations включает логику проверки, которая обеспечивает правильный переход записи через этапы утверждения.</span><span class="sxs-lookup"><span data-stu-id="2a8fd-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="2a8fd-106">Правильные переходы записей обеспечивают:</span><span class="sxs-lookup"><span data-stu-id="2a8fd-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="2a8fd-107">Все вспомогательные строки создаются в связанных таблицах, таких как журналы и фактические данные.</span><span class="sxs-lookup"><span data-stu-id="2a8fd-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="2a8fd-108">Утверждающий отмечен как **Утверждающий по проекту** в проекте, прежде чем продолжить.</span><span class="sxs-lookup"><span data-stu-id="2a8fd-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]