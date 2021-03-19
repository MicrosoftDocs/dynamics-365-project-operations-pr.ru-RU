---
title: Заметки разработчика для утверждений
description: Эта тема предоставляет дополнительную информацию для разработчика о работе с утверждениями.
author: stsporen
manager: Annbe
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d58c776b0341c08b0292e1b459a7d7ebac550bcc
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290285"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="52ab5-103">Заметки разработчика для утверждений</span><span class="sxs-lookup"><span data-stu-id="52ab5-103">Developer notes for Approvals</span></span>

<span data-ttu-id="52ab5-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="52ab5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="52ab5-105">Dynamics 365 Project Operations включает логику проверки, которая обеспечивает правильный переход записи через этапы утверждения.</span><span class="sxs-lookup"><span data-stu-id="52ab5-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="52ab5-106">Правильные переходы записей обеспечивают:</span><span class="sxs-lookup"><span data-stu-id="52ab5-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="52ab5-107">Все вспомогательные строки создаются в связанных таблицах, таких как журналы и фактические данные.</span><span class="sxs-lookup"><span data-stu-id="52ab5-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="52ab5-108">Утверждающий отмечен как **Утверждающий по проекту** в проекте, прежде чем продолжить.</span><span class="sxs-lookup"><span data-stu-id="52ab5-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]