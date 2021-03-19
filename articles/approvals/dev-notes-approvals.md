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
# <a name="developer-notes-for-approvals"></a>Заметки разработчика для утверждений

_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_

Dynamics 365 Project Operations включает логику проверки, которая обеспечивает правильный переход записи через этапы утверждения. Правильные переходы записей обеспечивают: 

  - Все вспомогательные строки создаются в связанных таблицах, таких как журналы и фактические данные.
  - Утверждающий отмечен как **Утверждающий по проекту** в проекте, прежде чем продолжить.


[!INCLUDE[footer-include](../includes/footer-banner.md)]