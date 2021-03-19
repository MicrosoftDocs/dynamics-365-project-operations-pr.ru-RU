---
title: Проекты оценки дохода с фиксированной ценой
description: В этом разделе представлена информация о доходе с фиксированной ценой в проектах.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7cf4d7853f7fedaeeeba99bc589f39989b924423
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278929"
---
# <a name="fixed-price-revenue-estimate-projects"></a><span data-ttu-id="3a888-103">Проекты оценки дохода с фиксированной ценой</span><span class="sxs-lookup"><span data-stu-id="3a888-103">Fixed price revenue estimate projects</span></span> 

<span data-ttu-id="3a888-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/без запасов_</span><span class="sxs-lookup"><span data-stu-id="3a888-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="3a888-105">Когда вы создаете строку контракта по проекту со следующими атрибутами в Dynamics 365 Project Operations на Microsoft Dataverse, система автоматически создает проект оценки дохода с фиксированной ценой.</span><span class="sxs-lookup"><span data-stu-id="3a888-105">When you create a project contract line with the following attributes in Dynamics 365 Project Operations on Microsoft Dataverse, the system automatically creates a fixed price revenue estimate project.</span></span> <span data-ttu-id="3a888-106">Информация в этом проекте основана на следующем:</span><span class="sxs-lookup"><span data-stu-id="3a888-106">The information in this project is based on the following:</span></span>

  - <span data-ttu-id="3a888-107">Метод выставления счетов с фиксированной ценой.</span><span class="sxs-lookup"><span data-stu-id="3a888-107">A fixed price billing method.</span></span>
  - <span data-ttu-id="3a888-108">Связанный проект.</span><span class="sxs-lookup"><span data-stu-id="3a888-108">An associated project.</span></span>
  - <span data-ttu-id="3a888-109">По крайней мере одна веха, определенная на вкладке **Расписание выставления счетов** на странице **Строка контракта по проекту**.</span><span class="sxs-lookup"><span data-stu-id="3a888-109">At least one milestone defined on the **Invoice schedule** tab on the **Project contract line** page.</span></span>

## <a name="review-fixed-price-revenue-estimates-projects"></a><span data-ttu-id="3a888-110">Просмотр проектов оценки дохода с фиксированной ценой</span><span class="sxs-lookup"><span data-stu-id="3a888-110">Review fixed price revenue estimates projects</span></span>
<span data-ttu-id="3a888-111">Чтобы просмотреть проекты оценки доходов с фиксированной ценой, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="3a888-111">To review fixed price revenue estimates projects, complete the following steps:</span></span>

1. <span data-ttu-id="3a888-112">В среде Dynamics 365 Finance перейдите в **Управление и учет по проектам** > **Проекты** > **Проекты оценки дохода с фиксированной ценой**.</span><span class="sxs-lookup"><span data-stu-id="3a888-112">In the Dynamics 365 Finance environment, go to **Projects management and accounting** > **Projects** > **Fixed price revenue estimate projects**.</span></span>
2. <span data-ttu-id="3a888-113">Выберите проект, который хотите просмотреть, и дважды щелкните значок **Идентификатор проекта оценки**, чтобы открыть запись и просмотреть информацию о проекте.</span><span class="sxs-lookup"><span data-stu-id="3a888-113">Select the project that you want to view and double-click the **Estimate project ID** to open the record and review the details of the project.</span></span>
3. <span data-ttu-id="3a888-114">Разверните вкладку **Проект**. Вы увидите один проект в сетке **Избранные проекты**.</span><span class="sxs-lookup"><span data-stu-id="3a888-114">Expand the **Project** tab. You will see one project in the **Selected projects** grid.</span></span> <span data-ttu-id="3a888-115">Система использует это как проект по умолчанию, потому что это проект, связанный со строкой контракта по проекту.</span><span class="sxs-lookup"><span data-stu-id="3a888-115">The system uses this as default project because it is the project associated to the project contract line.</span></span> 
4. <span data-ttu-id="3a888-116">Чтобы изменить связь, выберите дополнительные проекты и добавьте их в сетка **Избранные проекты**.</span><span class="sxs-lookup"><span data-stu-id="3a888-116">To change the association, select additional projects and add them to the **Selected projects** grid.</span></span> <span data-ttu-id="3a888-117">Если в этой сетке выбрано несколько проектов, процент завершения проекта и оценки дохода рассчитываются вместе для всех выбранных проектов.</span><span class="sxs-lookup"><span data-stu-id="3a888-117">If multiple projects are selected in this grid, the project percentage completion and revenue estimates are calculated together for of the all selected projects.</span></span>

  <span data-ttu-id="3a888-118">Стоимость проекта, профиль дохода, шаблон стоимости и код периода можно установить вручную.</span><span class="sxs-lookup"><span data-stu-id="3a888-118">Project cost, revenue profile, cost template, and the period code can be set manually.</span></span> <span data-ttu-id="3a888-119">Если они не установлены вручную, значения по умолчанию используются во время первого расчета оценки для проекта с использованием правил, настроенных для профилей затрат и доходов по проекту.</span><span class="sxs-lookup"><span data-stu-id="3a888-119">If they aren't set manually, the values default during the first estimate calculation for the project using the rules configured for project cost and revenue profiles.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]