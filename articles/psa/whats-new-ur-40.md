---
title: Что нового и что изменилось в выпуске-обновлении 40 для Project Service Automation версии 3
description: В этой статье перечислены функции и исправления, доступные в выпуске-обновлении 40 для Microsoft Dynamics 365 Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/31/2022
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
ms.openlocfilehash: dca7f340b8d544b183aa0390ac3c11a38f536ed0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912808"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-40-v3"></a>Что нового и что изменилось в выпуске-обновлении 40 для Project Service Automation версии 3

[!include [banner](../includes/psa-now-project-operations.md)]

Мы рады объявить о последнем обновлении для приложения Microsoft Dynamics 365 Project Service Automation. Этот выпуск содержит некоторые важные усовершенствования, направленные на качество, производительность и удобство использования. Он совместим с Dynamics 365 9.x. Чтобы выполнить обновление до этого выпуска, посетите страницу центра администрирования для онлайн-решений Dynamics 365 и установите обновление. Дополнительные сведения см. в разделе [Установка, обновление или удаление предпочтительного решения](/power-platform/admin/install-remove-preferred-solution).

В этой статье перечислены функции и исправления, которые добавлены или изменены в выпуске-обновлении 40 для Project Service Automation, V3. Эта версия имеет номер сборки V3.10.61.61 и будет доступна широкой публике через самостоятельное обновление в феврале 2022 года.

## <a name="update-release-40"></a>Выпуск-обновление 40

### <a name="features"></a>Функции
Фаза 1 перехода с Project Service Automation на Project Operations — облегченное развертывание будет выпущена для всех клиентов в феврале 2022 года. Чтобы узнать, можете ли вы ее использовать, см. раздел [Обновление с Project Service Automation до Project Operations](upgrade-project-operations-non-stocked.md). Если приложение не отображается в вашем экземпляре в Центре администрирования Power Platform, обратитесь в службу поддержки и попросите предоставить тестовый доступ для ваших сред. Ваш запрос должен включать список идентификаторов сред, для которых необходимо включить тестовый доступ.

### <a name="bug-fixes"></a>Исправленные ошибки

Следующие проблемы были исправлены.

**Время и расходы**
- Запись примечания отсутствует при отклонении или отмене записи времени. 

**Продажи**

- При обновлении оценок затрат или продаж с использованием готовых подключаемых модулей, вам ошибочно разрешается отправлять полезные данные JSON, которые недействительны за пределами пользовательского интерфейса.
- При обновлении строк предложений с расценками с помощью быстрого просмотра вам разрешается активировать предолжения с расценками.
