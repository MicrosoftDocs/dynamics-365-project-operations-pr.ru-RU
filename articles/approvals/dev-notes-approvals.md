---
title: Заметки разработчика для утверждений
description: В этой статье содержится дополнительная информация от разработчиков о работе с утверждениями.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: df3e27f95bffb9c169644fa3e42ff1e9b2b6ff54
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924768"
---
# <a name="developer-notes-for-approvals"></a>Заметки разработчика для утверждений

_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_

Dynamics 365 Project Operations включает логику проверки, которая обеспечивает правильный переход записи через этапы утверждения. Правильные переходы записей обеспечивают: 

  - Все вспомогательные строки создаются в связанных таблицах, таких как журналы и фактические данные.
  - Утверждающий отмечен как **Утверждающий по проекту** в проекте, прежде чем продолжить.


[!INCLUDE[footer-include](../includes/footer-banner.md)]