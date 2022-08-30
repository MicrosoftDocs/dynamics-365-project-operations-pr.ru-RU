---
title: Новые возможности в августе 2022 года — Project Operations для сценариев на основе ресурсов/без запасов
description: В этой статье содержится информация об исправлениях, доступных в выпуске Microsoft Dynamics 365 Project Operations для сценариев на основе ресурсов/без запасов за август 2022 года.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 112dbb98de09ef342c03d122a29cb8025058e47f
ms.sourcegitcommit: 6b6c2bfd04e3e613ed1f38355c7cd47c3a56748d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/24/2022
ms.locfileid: "9348027"
---
# <a name="whats-new-august-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Новые возможности в августе 2022 года — Project Operations для сценариев на основе ресурсов/без запасов

_**Относится к:** Project Operations для сценариев на основе ресурсов/без запасов_

Эта статья применяется к следующим компонентам и версиям Microsoft Dynamics 365 Project Operations:

- Project Operations в среде Dataverse версии 4.45.0.53
- Управление и учет по проектам в среде Dynamics 365 Finance версии 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Обновления сопоставления с двойной записью Project Operations

В этом выпуске нет обновлений для карт Project Operations с двойной записью. Для получения информации о текущем списке и версиях карт с двойной записью Project Operations см. [Версии карты с двойной записью Project Operations](../environment/resource-dual-write-maps.md).

Всегда запускайте последнюю версию сопоставления в своей среде и включайте все связанные карты таблиц при обновлении решения Project Operations Dataverse и версии решения Finance. Некоторые функции и возможности могут работать некорректно, если не активирована последняя версия сопоставления. Вы можете увидеть активную версию сопоставления в столбце **Версия** на странице **Двойная запись**. Чтобы активировать новую версию сопоставления, выберите **Версии сопоставления таблиц**, выберите последнюю версию, а затем сохраните выбранную версию. Если вы настроили стандартное сопоставление таблиц, примените изменения повторно. Дополнительные сведения см. в [Управление жизненным циклом приложений](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Если вы столкнулись с проблемой при запуске сопоставления, следуйте инструкциям в разделе [В картах отсутствуют столбцы таблицы](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) в руководстве по устранению неполадок с двойной записью.

## <a name="quality-updates"></a>Обновления качества

### <a name="project-operations-on-dataverse"></a>Project Operations на Dataverse

| Область функций | Номер ссылки | Обновление качества |
| --- | --- | --- |
|   Управление возможными сделками | 2762089 | Обработка ошибок при закрытии договора как упущенного, если автоматическое сохранение в организации отключено.|

### <a name="project-management-and-accounting-in-finance"></a>Управление и учет для проектов в Finance

Для получения сведений об исправлениях ошибок, включенных в это обновление, войдите в Microsoft Dynamics Lifecycle Services (LCS) и просмотрите [статью базы знаний](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).
