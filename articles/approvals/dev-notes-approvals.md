---
title: Заметки разработчика для утверждений
description: Эта тема предоставляет дополнительную информацию для разработчика о работе с утверждениями.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cfa4928eda286bee298a2c33f4e9c25b576f495795fc2deda33b393e372465b1
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991682"
---
# <a name="developer-notes-for-approvals"></a>Заметки разработчика для утверждений

_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_

Dynamics 365 Project Operations включает логику проверки, которая обеспечивает правильный переход записи через этапы утверждения. Правильные переходы записей обеспечивают: 

  - Все вспомогательные строки создаются в связанных таблицах, таких как журналы и фактические данные.
  - Утверждающий отмечен как **Утверждающий по проекту** в проекте, прежде чем продолжить.


[!INCLUDE[footer-include](../includes/footer-banner.md)]