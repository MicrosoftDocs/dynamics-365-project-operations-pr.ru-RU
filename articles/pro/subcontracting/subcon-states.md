---
title: Переходы между состояниями по субподряду
description: Эта тема объясняет переходы между состояниями по субподряду в Microsoft Dynamics 365 Project Operations по мере создания, исполнения и закрытия субподряда.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: d67f4a3cd834c25462304c2d75c824427fcbd034
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903519"
---
# <a name="state-transitions-on-a-subcontract"></a>Переходы между состояниями по субподряду 

[!include [banner](../../includes/dataverse-preview.md)]

_**Относится к:** развертывание Lite — от сделки до счетов-проформ_

Эта тема объясняет переходы между состояниями по субподряду в Microsoft Dynamics 365 Project Operations. Каждое состояние представлено как черновик, подтверждено, закрыто или отменено. На следующем изображении представлены переходы между состояниями.

![Модель состояний субподряда](../media/SubconStates.png)  

В следующей таблице представлено описание того, что представляет собой каждое состояние в жизненном цикле субподряда в Project Operations.

| State | Description | Разрешенные переходы |
| --- | --- | --- |
| Черновик | Это представляет собой начальное состояние субподряда. Ведутся переговоры с поставщиком. Строки и цены могут быть изменены. Субподряд в этом состоянии можно использовать для оценки и укомплектования персоналом проектных требований к ресурсам и материалам. На него также можно ссылаться по времени, расходам и использованию материалов по проекту. Субподряд в этом состоянии можно редактировать и удалять. | Подтверждена |
| Подтверждена | Это представляет собой этап субподряда после завершения переговоров с поставщиком о ценах и закупаемых позициях. Однако фактическая доставка материалов и/или работы субподрядными ресурсами все еще продолжается. Субподряд в этом состоянии можно использовать для оценки и укомплектования персоналом проектных требований к ресурсам и материалам. На него также можно ссылаться по времени, расходам и использованию материалов по проекту. Субподряд в этом состоянии нельзя изменить или удалить. Кнопка **Отмена** позволяет отменить подтвержденный субподряд. Кнопка **Повторно открыть** позволяет повторно открыть субподряд, чтобы вернуть его в состояние **Черновик**. Используйте кнопку **Закрыть**, чтобы закрыть подтвержденный субподряд. | Закрытые <br> Отмененные <br> Черновик |
| Закрытые | Это представляет собой этап субподряда, когда фактическая поставка материалов и/или работы субподрядными ресурсами завершена. Субподряд в этом состоянии больше нельзя использовать для оценки и укомплектования персоналом проектных требований к ресурсам и материалам. Кроме того, на него больше нельзя ссылаться по времени, расходам и использованию материалов по проекту. Субподряд в этом состоянии нельзя изменить или удалить. | None |
| Отмененные | Это представляет собой этап субподряда, когда фактическая поставка материалов и/или работы субподрядными ресурсами больше не требуется. Субконтракт в этом состоянии не может использоваться для оценки потребностей проекта в ресурсах и материалах и комплектации его персоналом, а также нельзя ссылаться на него по времени, расходам и использованию материалов по проекту. Субподряд в этом состоянии нельзя изменить или удалить. | None |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]