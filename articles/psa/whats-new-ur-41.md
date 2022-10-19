---
title: Что нового и что изменилось в выпуске-обновлении 41 для Project Service Automation версии 3
description: В этой статье перечислены функции и исправления, доступные в выпуске-обновлении 41 для Microsoft Dynamics 365 Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 03/07/2022
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
ms.openlocfilehash: 8625ae16e45da30614b3a3eec44193bee0c0b36f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930564"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-41-v3"></a>Что нового и что изменилось в выпуске-обновлении 41 для Project Service Automation версии 3

[!include [banner](../includes/psa-now-project-operations.md)]

Мы рады объявить о последнем обновлении для приложения Microsoft Dynamics 365 Project Service Automation. Этот выпуск содержит некоторые важные усовершенствования, направленные на качество, производительность и удобство использования. Он совместим с Dynamics 365 9.x. Чтобы выполнить обновление до этого выпуска, посетите страницу центра администрирования для онлайн-решений Dynamics 365 и установите обновление. Дополнительные сведения см. в разделе [Установка, обновление или удаление предпочтительного решения](/power-platform/admin/install-remove-preferred-solution).

В этой статье перечислены функции и исправления, которые добавлены или изменены в выпуске-обновлении 41 для Project Service Automation, V3. Эта версия имеет номер сборки V3.10.62.162 и становится доступна широкому кругу клиентов посредством самостоятельного обновления в марте 2022 г.

## <a name="update-release-41"></a>Выпуск-обновление 41

### <a name="bug-fixes"></a>Исправленные ошибки

Следующие проблемы были исправлены.

**Управление проектами**
- При попытке создать проект из шаблона, основанного на проекте, созданном с помощью классической надстройки, появляется следующая ошибка: "Проверка поля "Запланированная работа" назначения ресурса: дата окончания каждого временного среза назначения ресурса не должна быть раньше его даты начала".

**Время и расходы**
- При попытке удалить запись времени отображается следующее сообщение об ошибке: "Непредвиденная ошибка, вызванная кодом независимого поставщика программных продуктов".

**Продажи**
- Когда вы создаете счет для вехи с фиксированной ценой, поля **Описание** и **Внешнее описание** не заполняются. 