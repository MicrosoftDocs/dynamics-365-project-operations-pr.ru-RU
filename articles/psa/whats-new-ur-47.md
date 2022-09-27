---
title: Что нового или измененного в выпуске-обновлении 47 для Project Service Automation версии 3
description: В этой статье перечислены функции и исправления, доступные в выпуске-обновлении 47 для Microsoft Dynamics 365 Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 09/14/2022
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
ms.openlocfilehash: 08e8fa9c41bdd77d93e4d5207266115022fba1b2
ms.sourcegitcommit: 498a5d5a33c47cab788fac4215fc47662042155a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/14/2022
ms.locfileid: "9477242"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-47-v3"></a>Что нового или измененного в выпуске-обновлении 47 для Project Service Automation версии 3

[!include [banner](../includes/psa-now-project-operations.md)]

Мы рады объявить о последнем обновлении для приложения Microsoft Dynamics 365 Project Service Automation. Этот выпуск содержит некоторые важные усовершенствования, направленные на качество, производительность и удобство использования. Он совместим с Dynamics 365 9.x. Чтобы выполнить обновление до этого выпуска, посетите страницу центра администрирования для онлайн-решений Dynamics 365 и установите обновление. Дополнительные сведения см. в разделе [Установка, обновление или удаление предпочтительного решения](/power-platform/admin/install-remove-preferred-solution).

В этой статье перечислены функции и исправления, которые добавлены или изменены в выпуске-обновлении 45 для Project Service Automation, V3. Эта версия имеет номер сборки V3.10.78.8 и доступна через самообновление в июле 2022 года.

## <a name="update-release-47"></a>Выпуск-обновление 47

### <a name="bug-fixes"></a>Исправленные ошибки

Следующие проблемы были исправлены.

**Управление ресурсами**
- Проверка была обновлена, чтобы гарантировать, что пользователи не могут инициировать исключение ссылки NULL при попытке создать участника проектной группы без **Резервируемый ресурс**.
