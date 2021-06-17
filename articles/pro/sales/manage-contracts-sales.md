---
title: Управление контрактами по проекту
description: Эта тема предоставляет информацию о просмотре контрактов на основе проектов.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5e2f182f66bd1f4fe57d19e4bf82525ac8b84c29
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003107"
---
# <a name="manage-project-contracts"></a><span data-ttu-id="7c5e6-103">Управление контрактами по проекту</span><span class="sxs-lookup"><span data-stu-id="7c5e6-103">Manage project contracts</span></span>

<span data-ttu-id="7c5e6-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="7c5e6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="7c5e6-105">Контракты по проекту в Dynamics 365 Project Operations фиксируют договорные обязательства и детали выставления счетов по проекту и управляют ими.</span><span class="sxs-lookup"><span data-stu-id="7c5e6-105">Project contracts in Dynamics 365 Project Operations capture and manage the contractually agreed on commitments and billing details of a project.</span></span> <span data-ttu-id="7c5e6-106">Структура контракта по проекту в Project Operations настроена для работы на основе проекта со следующими компонентами:</span><span class="sxs-lookup"><span data-stu-id="7c5e6-106">The structure of a project contract in Project Operations is tailored to project-based work with the following components:</span></span>

- <span data-ttu-id="7c5e6-107">Строки контракта, которые определяют дискретные компоненты работы, которые будут представлены как компоненты высокого уровня в счете по проекту.</span><span class="sxs-lookup"><span data-stu-id="7c5e6-107">Contract lines that identify the discrete components of work that will be presented as high-level components on a project invoice.</span></span>
- <span data-ttu-id="7c5e6-108">Детали строки контракта, которые идентифицируют и оценивают работу для каждого компонента высокого уровня или строки контракта.</span><span class="sxs-lookup"><span data-stu-id="7c5e6-108">Contract line details that identify and estimate the work for each high-level component or contract line.</span></span> <span data-ttu-id="7c5e6-109">Оценка включает график и финансовые аспекты для работы, привязанной к этой строке контракта.</span><span class="sxs-lookup"><span data-stu-id="7c5e6-109">The estimate includes the schedule and the financial aspects for the work tied to the contract line.</span></span>
- <span data-ttu-id="7c5e6-110">Модели контрактов и оплачиваемые компоненты настраиваются для каждой строки контракта, в которой содержится порядок выставления счетов для каждой строки контракта и всего контракта.</span><span class="sxs-lookup"><span data-stu-id="7c5e6-110">Contracting models and chargeable components are set up for each contract line that holds the billing arrangement for each contract line and the overall contract.</span></span>

## <a name="view-all-project-based-contracts"></a><span data-ttu-id="7c5e6-111">Просмотр всех контрактов на основе проектов</span><span class="sxs-lookup"><span data-stu-id="7c5e6-111">View all project-based contracts</span></span>

<span data-ttu-id="7c5e6-112">Список всех контрактов по проектам можно увидеть на странице списка **Контракты**.</span><span class="sxs-lookup"><span data-stu-id="7c5e6-112">A list of all project contracts can be seen on the **Contracts** list page.</span></span> 

1. <span data-ttu-id="7c5e6-113">Перейдите в раздел **Продажи** > **Контракты**.</span><span class="sxs-lookup"><span data-stu-id="7c5e6-113">Go to **Sales** > **Contracts**.</span></span> <span data-ttu-id="7c5e6-114">Отображается список всех контрактов в системе.</span><span class="sxs-lookup"><span data-stu-id="7c5e6-114">A list of all your project Contracts in the system are shown.</span></span> 
2. <span data-ttu-id="7c5e6-115">Выберите **Переключатель представлений** (стрелка раскрывающегося списка рядом с именем представления) для выбора других фильтрованных представлений.</span><span class="sxs-lookup"><span data-stu-id="7c5e6-115">Select the **View switcher** (the drop-down arrow next to the name of the view) to select other filtered views.</span></span> <span data-ttu-id="7c5e6-116">Можно создавать собственные представления с настраиваемыми критериями фильтрации.</span><span class="sxs-lookup"><span data-stu-id="7c5e6-116">You can create your own views with custom filter criteria.</span></span>

<span data-ttu-id="7c5e6-117">Контракты могут быть созданы или удалены с этой страницы списка или страниц со сведениями.</span><span class="sxs-lookup"><span data-stu-id="7c5e6-117">Contracts can be created or deleted from this list page or detail pages.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]