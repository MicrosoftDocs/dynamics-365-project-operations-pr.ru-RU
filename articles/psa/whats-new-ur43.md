---
title: Что нового и что изменилось в выпуске-обновлении 43 для Project Service Automation версии 3
description: В этой статье перечислены функции и исправления, доступные в выпуске-обновлении 43 для Microsoft Dynamics 365 Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 05/04/2022
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
ms.openlocfilehash: b12cfda08f1ea1fc441782003130be445a437f7c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915338"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-43-v3"></a>Что нового и что изменилось в выпуске-обновлении 43 для Project Service Automation версии 3

[!include [banner](../includes/psa-now-project-operations.md)]

Мы рады объявить о последнем обновлении для приложения Microsoft Dynamics 365 Project Service Automation. Этот выпуск содержит некоторые важные усовершенствования, направленные на качество, производительность и удобство использования. Он совместим с Dynamics 365 9.x. Чтобы выполнить обновление до этого выпуска, посетите страницу центра администрирования для онлайн-решений Dynamics 365 и установите обновление. Дополнительные сведения см. в разделе [Установка, обновление или удаление предпочтительного решения](/power-platform/admin/install-remove-preferred-solution).

В этой статье перечислены функции и исправления, которые добавлены или изменены в выпуске-обновлении 43 для Project Service Automation, V3. Эта версия имеет номер сборки V3.10.74.200 и доступна для широкой публики после автоматического обновления в мае 2022 г.

## <a name="update-release-43"></a>Выпуск-обновление 43

### <a name="bug-fixes"></a>Исправленные ошибки

Следующие проблемы были исправлены.


**Время и расходы**

- При импорте записей времени из резервирований или назначений ресурсов ссылка на связанный резервируемый ресурс не сохраняется.
- Когда сетка ввода времени развернута на весь экран, навигация по сетке с помощью клавиши табуляции не работает.
- При отправке записи времени, созданной другим пользователем, в поле **Кем отправлено** неправильно указывается пользователь, который создал табель учета рабочего времени.
