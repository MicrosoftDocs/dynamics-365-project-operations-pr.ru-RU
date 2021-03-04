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
ms.openlocfilehash: 9e4e910d0ff0a5f2603148fcc5daa0d423a4d174
ms.sourcegitcommit: a9dbcd3aff4c6ae495412e4980e105ae160fd1ec
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "4483964"
---
# <a name="developer-notes-for-approvals"></a>Заметки разработчика для утверждений

_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_

Dynamics 365 Project Operations включает логику проверки, которая обеспечивает правильный переход записи через этапы утверждения. Правильные переходы записей обеспечивают: 

  - Все вспомогательные строки создаются в связанных таблицах, таких как журналы и фактические данные.
  - Утверждающий отмечен как **Утверждающий по проекту** в проекте, прежде чем продолжить.


[!INCLUDE[footer-include](../includes/footer-banner.md)]