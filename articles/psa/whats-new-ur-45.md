---
title: Что нового или измененного в выпуске-обновлении 45 для Project Service Automation версии 3
description: В этой статье перечислены функции и исправления, доступные в выпуске-обновлении 45 для Microsoft Dynamics 365 Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 07/14/2022
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
ms.openlocfilehash: 98f7c973917d7d6334e6e0aeb15214c538b33143
ms.sourcegitcommit: 36fda4f45ddeb0f81d30bd1e22852727df644754
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/16/2022
ms.locfileid: "9169165"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-45-v3"></a>Что нового или измененного в выпуске-обновлении 45 для Project Service Automation версии 3

[!include [banner](../includes/psa-now-project-operations.md)]

Мы рады объявить о последнем обновлении для приложения Microsoft Dynamics 365 Project Service Automation. Этот выпуск содержит некоторые важные усовершенствования, направленные на качество, производительность и удобство использования. Он совместим с Dynamics 365 9.x. Чтобы выполнить обновление до этого выпуска, посетите страницу центра администрирования для онлайн-решений Dynamics 365 и установите обновление. Дополнительные сведения см. в разделе [Установка, обновление или удаление предпочтительного решения](/power-platform/admin/install-remove-preferred-solution).

В этой статье перечислены функции и исправления, которые добавлены или изменены в выпуске-обновлении 45 для Project Service Automation, V3. Эта версия имеет номер сборки V3.10.76.168 и доступна через самообновление в июле 2022 года.

## <a name="update-release-45"></a>Выпуск-обновление 45

### <a name="bug-fixes"></a>Исправленные ошибки

Следующие проблемы были исправлены.

**Продажи**

- Пользователи не могут успешно создавать счета после того, как пытаются создать счет на продажу без выставления счета, если они также просматривают тот же экземпляр страницы и не обновляют ее.

**Время и расходы**

- Когда включены современные утверждения и утвержден отзыв проекта, статус этапа записи неправильно меняется на **Запрос на отзыв утвержден**.
- Когда включены современные утверждения, а Облачные потоки неактивны, процесс утверждения завершается неудачно, а отправляющие и утверждающие пользователи не получают уведомления.
