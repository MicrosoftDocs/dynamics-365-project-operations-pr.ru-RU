---
title: Что нового или измененного в выпуске-обновлении 28 для Project Service Automation версии версии 3
description: В этом разделе перечислены функции и исправления, доступные в выпуске-обновлении 28 для Project Service Automation версии версии 3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.openlocfilehash: b06a5ee6d0e2da76801a36701f38f1885d6c7562
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010532"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a>Что нового или измененного в выпуске-обновлении 28 для Project Service Automation версии версии 3

[!include [banner](../includes/psa-now-project-operations.md)]

Мы рады объявить о последнем обновлении приложения Project Service Automation для Dynamics 365. Этот выпуск содержит некоторые важные усовершенствования, направленные на качество, производительность и удобство использования. Этот выпуск совместим с Dynamics 365 9.x. Чтобы обновить приложение до этого выпуска, посетите страницу решений Центра администрирования Dynamics 365 Online и установите обновление. Дополнительные сведения см. в разделе [Установка, обновление или удаление предпочтительного решения](/power-platform/admin/install-remove-preferred-solution).

В этой теме перечислены новые или измененные функции и исправления для Project Service Automation версии 3, выпуск-обновление 28. Эта версия имеет номер сборки версии 3.10.46.32 и она общедоступна через самообновление в январе 2021 года.

## <a name="update-release-28"></a>Выпуск-обновление 28

### <a name="bug-fixes"></a>Исправленные ошибки

**Время и расходы**

Следующие проблемы были исправлены:

- Пользователи могут использовать **Групповое редактирование** для обновления записей времени, которые были утверждены и отправлены.

**Управление проектами**

Следующие проблемы были исправлены:

- В случаях, когда GUID задачи интерпретируется как число, задачи нельзя открыть для редактирования с помощью **Изменить задачу** в ленте на страница **Структурная декомпозиция работ**.

**Sales**

Следующие проблемы были исправлены:

- Исключение нулевой ссылки создается, когда вызывается подключаемый модуль **GetEstimatesForProject**.
- **Пометить как готовое к выставлению счета** в сетке вехи только частично обновляет атрибуты, за исключением атрибута **InvoiceStatus**, который обновляется.



[!INCLUDE[footer-include](../includes/footer-banner.md)]