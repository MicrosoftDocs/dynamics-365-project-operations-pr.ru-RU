---
title: Переходы между состояниями для счета поставщика
description: В этой теме рассматриваются переходы между состояниями счета поставщика в Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7efb52621ee325d5025dfad0b45218d1fe20a063
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584704"
---
# <a name="state-transitions-on-a-vendor-invoice"></a>Переходы между состояниями для счета поставщика

[!include [banner](../../includes/dataverse-preview.md)]

_**Относится к:** развертывание Lite — от сделки до счетов-проформ_

В этой теме рассматриваются переходы между состояниями счета поставщика в Microsoft Dynamics 365 Project Operations. Используются следующие состояния: **Черновик**, **На проверке**, **Подтверждено**, **На удержании** и **Отменено**.

На следующей иллюстрации показаны переходы состояний.

![Модель переходов состояний субподряда.](../media/VI_State_Model.jpg)

В следующей таблице поясняется, что представляет собой каждое состояние в жизненном цикле счета поставщика в Project Operations.

| State | Description | Разрешенные переходы |
| --- | --- | --- |
| Черновик | Это состояние является начальным состоянием счета поставщика. Строки и цены могут быть изменены. Счет поставщика в этом состоянии можно редактировать и удалять. | В процессе |
| На проверке | Это состояние означает, что счет поставщика обрабатывается. По крайней мере одна строка счета поставщика имеет состояние проверки **В процессе**. | Подтверждено, На удержании |
| Подтверждена | Это состояние представляет стадию счета поставщика, на которой приложение создало фактические значения затрат для каждой строки счета поставщика. Любые связанные фактические значения затрат, сопоставленные со строками счета поставщика, были сторнированы и заменены фактическими значениями затрат из этих строк счета поставщика. Счет поставщика в этом состоянии нельзя изменить или удалить. Вы можете использовать кнопку **Отмена** кнопку для отмены подтвержденного счета поставщика. Действие "Отмена" отменяет влияние действия "Подтвердить". | Отмененные |
| На удержании | <p>Это состояние представляет стадию счета поставщика, на которой счет поставщика не может двигаться дальше из-за проблемы со счетом или статусом поставщика. Счет поставщика в этом состоянии нельзя подтвердить, отменить, изменить или удалить.</p><p>Вы можете использовать действие "Открыть повторно", чтобы перевести счет поставщика в состояние **Черновик** или **На проверку**. Если хотя бы одна строка в счете поставщика имеет состояние проверки **В процессе** или **Завершено**, счет поставщика будет повторно открыт в состоянии **На проверке**. Если все строки в счете поставщика имеют состояние проверки **Не начато**, счет поставщика будет повторно открыт в состоянии **Черновик**.</p> | Черновик, На проверке |
| Отмененные | Это состояние представляет собой этап субподряда, когда фактическая поставка материалов и/или работы субподрядными ресурсами больше не требуется. Субподряд в этом состоянии не может использоваться для оценки потребностей проекта в ресурсах и материалах и комплектации его персоналом, а также нельзя ссылаться на него во времени, расходах и использовании материалов по проекту. Субподряд в этом состоянии нельзя изменить или удалить. | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]