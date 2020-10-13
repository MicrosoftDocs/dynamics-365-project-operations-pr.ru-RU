---
title: Ключевые концепции управления ресурсами
description: В этой теме предоставлена информация о возможностях управления ресурсами в Microsoft Dynamics Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 124d9bad5cc0c16955417a8213db047a2d8bae1d
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897557"
---
# <a name="resource-management-key-concepts"></a><span data-ttu-id="90af8-103">Ключевые концепции управления ресурсами</span><span class="sxs-lookup"><span data-stu-id="90af8-103">Resource management key concepts</span></span>

<span data-ttu-id="90af8-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="90af8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="90af8-105">Ресурсы — самый важный актив организаций, основанных на сервисе.</span><span class="sxs-lookup"><span data-stu-id="90af8-105">Resources are the most important asset of a service-based organization.</span></span> <span data-ttu-id="90af8-106">Возможность находить правильные ресурсы в правильное время, резервировать эти ресурсы для проектов и поддерживать их загрузку помогает организации достигать целевого дохода и целей по удовлетворенности клиентов.</span><span class="sxs-lookup"><span data-stu-id="90af8-106">The ability to find the right resources at the right time, book those resources on projects and keep them utilized, helps the organization meet revenue targets and customer satisfaction goals.</span></span> <span data-ttu-id="90af8-107">Функции выделения ресурсов проекта в Dynamics 365 Project Operations можно использовать, чтобы выполнить следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="90af8-107">You can use the project resourcing functionality in Dynamics 365 Project Operations to do the following tasks:</span></span>

- <span data-ttu-id="90af8-108">Формирование рабочих групп проекта путем резервирования доступных квалифицированных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="90af8-108">Form project teams by booking available and qualified resources.</span></span>
- <span data-ttu-id="90af8-109">Создание записей универсальных участников рабочей группы, определение их ролей и подразделения ресурса.</span><span class="sxs-lookup"><span data-stu-id="90af8-109">Create generic team member records and define their roles and resource organization unit.</span></span>
- <span data-ttu-id="90af8-110">Формирование требований ресурса для универсальных участников рабочей группы из их назначений задач.</span><span class="sxs-lookup"><span data-stu-id="90af8-110">Generate resource requirements for generic team members from their task assignments.</span></span>
- <span data-ttu-id="90af8-111">Подбор навыков путем идентификации навыков, определенных в требовании, и навыков доступных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="90af8-111">Match skills by identifying the skills defined on the resource demand against available resource skills.</span></span>
- <span data-ttu-id="90af8-112">Замена ресурсов.</span><span class="sxs-lookup"><span data-stu-id="90af8-112">Substitute resources.</span></span>
- <span data-ttu-id="90af8-113">Согласование назначений расписания проектов и резервирований ресурсов.</span><span class="sxs-lookup"><span data-stu-id="90af8-113">Align project schedule assignments and resource bookings.</span></span>
- <span data-ttu-id="90af8-114">Выверка различий в резервированиях и назначениях.</span><span class="sxs-lookup"><span data-stu-id="90af8-114">Reconcile differences in bookings and assignments.</span></span>
- <span data-ttu-id="90af8-115">Изменение резервирований ресурсов в случае отсутствия на работе.</span><span class="sxs-lookup"><span data-stu-id="90af8-115">Change resource bookings in response to out-of-office status.</span></span>
- <span data-ttu-id="90af8-116">Сотрудничество между руководителями проектов и менеджерами по ресурсам.</span><span class="sxs-lookup"><span data-stu-id="90af8-116">Collaborate between project managers and resource managers.</span></span>
- <span data-ttu-id="90af8-117">Просмотр истории загруженности ресурсов относительно целевого значения, включая разбивку того, как использовалось время ресурсов.</span><span class="sxs-lookup"><span data-stu-id="90af8-117">View the history of resource utilization against a target, including a breakdown of how the resources' time was utilized.</span></span>
- <span data-ttu-id="90af8-118">Ведение репозитория навыков и квалификации.</span><span class="sxs-lookup"><span data-stu-id="90af8-118">Maintain a skills and proficiency repository.</span></span>


<span data-ttu-id="90af8-119">Можно подбирать сотрудников для проекта с рабочей группой универсальных или именованных ресурсов в Project Operations.</span><span class="sxs-lookup"><span data-stu-id="90af8-119">You can staff your project with a team of generic or named resources in Project Operations.</span></span> <span data-ttu-id="90af8-120">Можно использовать разные методы добавления и назначения участников рабочей группы и управления их резервированиями и назначениями.</span><span class="sxs-lookup"><span data-stu-id="90af8-120">You can use various methods to add and assign team members and to manage their bookings and assignments.</span></span> 
