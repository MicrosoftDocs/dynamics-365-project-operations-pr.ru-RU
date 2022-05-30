---
title: Применение значений финансовых аналитик по умолчанию для записей времени проекта
description: В этой теме приведена информация о том, как финансовые аналитики по умолчанию применяются к записям времени.
author: stsporen
ms.date: 01/24/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: cc51fcdcbbfec23591471c0f7522d571be813a84
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597952"
---
# <a name="defaulting-financial-dimensions-for-project-time-entries"></a>Применение значений финансовых аналитик по умолчанию для записей времени проекта

[!include [banner](../includes/banner.md)]

При использовании финансовых аналитик для записей времени по проекту значение аналитики по умолчанию оценивается в следующем порядке:

1. Ресурс
2. Project
3. Источник финансирования

Например, если аналитика по умолчанию указана для ресурса, значение по умолчанию имеет приоритет над значением по умолчанию, указанным в проекте. Аналогично, если аналитика по умолчанию указана дляпроекта, значение по умолчанию имеет приоритет над значением по умолчанию, указаным для источника финансирования.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
