---
title: Обзор режимов управления ресурсами
description: В этой теме предоставлена информация о функциях управления ресурсами в Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4a8e605109e48b50da68abeee989f8ac8d3d659c
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083076"
---
# <a name="resource-management-modes-overview"></a>Обзор режимов управления ресурсами

_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_


Dynamics 365 Project Operations поддерживает два режима для выполнения всего потока резервирования. Режим управления определяется как параметр проекта и может быть изменен, если требуется изменение вашего бизнеса.    

## <a name="central-mode"></a>Центральный режим
Для организаций, которые централизуют распределение ресурсов по проектам, центральный режим предоставляет способ гарантировать, что менеджеры проектов могут определять требования ресурсов на уровне проекта. Выполнение требований ресурсов делегируется менеджеру ресурсов. Менеджеры проектов могут принять или отклонить ресурсы, предложенные менеджером ресурсов.

![Центральный режим](./media/resource-management-central.png)

Чтобы управлять ресурсами в центральном режиме, см.:

- [Назначение универсальных резервируемых ресурсов задаче и создание требований ресурсов](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [Резервирование именованных ресурсов из требований ресурсов](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [Отправка запроса ресурса](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [Выполнение запросов ресурсов](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [Подтверждение или отклонение предложенного ресурса проекта из запроса ресурса](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>Гибридный режим
Для организаций, которым требуется гибкость в распределении ресурсов, гибридный режим позволяет менеджерам проектов и менеджерам ресурсов возможность резервировать ресурсы.

![Гибридный режим](./media/resource-management-hybrid.png)

В дополнение к поддерживаемому процессу централизованного режима см. следующие темы, чтобы управлять всеми другими поддерживаемыми потоками резервирования в гибридном режиме:

Резервирование ресурса напрямую для проекта:
- [Резервирование резервируемых ресурсов для проектной группы и назначение задач](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

Резервирование ресурса из требования ресурсов:
- [Назначение универсальных резервируемых ресурсов задаче и создание требований ресурсов](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [Резервирование именованных ресурсов из требований ресурсов](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
