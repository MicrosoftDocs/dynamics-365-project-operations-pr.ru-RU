---
title: Что нового и что изменилось в выпуске-обновлении 42 для Project Service Automation версии 3
description: В этой статье перечислены функции и исправления, доступные в выпуске-обновлении 42 для Microsoft Dynamics 365 Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/05/2022
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: e9911531e4acbd78db416f554c8d85c4f1fee1cf
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912731"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-42-v3"></a>Что нового и что изменилось в выпуске-обновлении 42 для Project Service Automation версии 3

[!include [banner](../includes/psa-now-project-operations.md)]

Мы рады объявить о последнем обновлении для приложения Microsoft Dynamics 365 Project Service Automation. Этот выпуск содержит некоторые важные усовершенствования, направленные на качество, производительность и удобство использования. Он совместим с Dynamics 365 9.x. Чтобы выполнить обновление до этого выпуска, посетите страницу центра администрирования для онлайн-решений Dynamics 365 и установите обновление. Дополнительные сведения см. в разделе [Установка, обновление или удаление предпочтительного решения](/power-platform/admin/install-remove-preferred-solution).

В этой статье перечислены функции и исправления, которые добавлены или изменены в выпуске-обновлении 42 для Project Service Automation, V3. Эта версия имеет номер сборки V3.10.73.61 и доступна для широкой публики после автоматического обновления в апреле 2022 г.

## <a name="update-release-42"></a>Выпуск-обновление 42

### <a name="bug-fixes"></a>Исправленные ошибки

Следующие проблемы были исправлены.

**Время и расходы**

- При отклонении табеля учета времени пользователь, который его отклонил, ошибочно идентифицируется как **Система**.
- При импорте записей времени отсутствует значение поля **Категория ресурса**.
- Утверждающие проектов могут утверждать отправленные проекты, когда у них нет явно заданного разрешения **Может утверждать**.

**Продажи**

- Когда фактические значения регистрируются для задач не корневого уровня, фактические затраты агрегируются неправильно.
