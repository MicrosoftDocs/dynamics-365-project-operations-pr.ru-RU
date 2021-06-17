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
# <a name="developer-notes-for-approvals"></a>Заметки разработчика для утверждений

_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_

Dynamics 365 Project Operations включает логику проверки, которая обеспечивает правильный переход записи через этапы утверждения. Правильные переходы записей обеспечивают: 

  - Все вспомогательные строки создаются в связанных таблицах, таких как журналы и фактические данные.
  - Утверждающий отмечен как **Утверждающий по проекту** в проекте, прежде чем продолжить.


[!INCLUDE[footer-include](../includes/footer-banner.md)]