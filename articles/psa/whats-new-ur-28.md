---
title: Что нового или измененного в выпуске-обновлении 28 для Project Service Automation версии версии 3
description: В этой статье перечислены функции и исправления, доступные в выпуске-обновлении 28 для Project Service Automation, V3.
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 56a87bce55c560e541e20709b10d38b9512ffcee
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930610"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a>Что нового или измененного в выпуске-обновлении 28 для Project Service Automation версии версии 3

[!include [banner](../includes/psa-now-project-operations.md)]

Мы рады объявить о последнем обновлении приложения Project Service Automation для Dynamics 365. Этот выпуск содержит некоторые важные усовершенствования, направленные на качество, производительность и удобство использования. Этот выпуск совместим с Dynamics 365 9.x. Чтобы обновить приложение до этого выпуска, посетите страницу решений Центра администрирования Dynamics 365 Online и установите обновление. Дополнительные сведения см. в разделе [Установка, обновление или удаление предпочтительного решения](/power-platform/admin/install-remove-preferred-solution).

В этой статье перечислены новые и измененные функции и исправления для Project Service Automation версии 3, выпуск-обновление 28. Эта версия имеет номер сборки V3.10.46.32 и становится доступна широкому кругу клиентов посредством самостоятельного обновления в январе 2021 г.

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
