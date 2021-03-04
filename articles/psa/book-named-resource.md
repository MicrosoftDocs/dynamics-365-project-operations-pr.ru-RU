---
title: Резервирование именованных ресурсов из требований ресурсов
description: В этом разделе представлена информация о резервировании именованных ресурсов для требования универсального ресурса.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: c7a6370bde434b74d05e342240abd9bba84d34d8
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145121"
---
# <a name="book-named-resources-from-resource-requirements"></a><span data-ttu-id="1ed40-103">Резервирование именованных ресурсов из требований ресурсов</span><span class="sxs-lookup"><span data-stu-id="1ed40-103">Book named resources from resource requirements</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="1ed40-104">Вы можете зарезервировать именованный ресурс для замены универсального ресурса, имеющего требование ресурса.</span><span class="sxs-lookup"><span data-stu-id="1ed40-104">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="1ed40-105">В Project Service Automation (PSA) на странице **Проекты** щелкните вкладку **Рабочая группа**.</span><span class="sxs-lookup"><span data-stu-id="1ed40-105">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab.</span></span>
2. <span data-ttu-id="1ed40-106">Выберите универсальный ресурс, имеющий требование ресурса, в списке, затем щелкните **Резервировать**.</span><span class="sxs-lookup"><span data-stu-id="1ed40-106">Select the generic resource that has a resource requirement from the list and then click **Book**.</span></span> <span data-ttu-id="1ed40-107">Или откройте требование ресурса, затем щелкните **Резервировать**.</span><span class="sxs-lookup"><span data-stu-id="1ed40-107">Or, open the resource requirement and then click **Book**.</span></span>


![Резервирование универсального участника рабочей группы](media/RM-how-to-14.png)


3. <span data-ttu-id="1ed40-109">На странице **Помощник по расписанию** выберите именованный ресурс для резервирования в проектную группу, затем щелкните **Резервировать**.</span><span class="sxs-lookup"><span data-stu-id="1ed40-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then click **Book**.</span></span>

![Резервирование универсального участника рабочей группы с помощью помощника по расписанию](media/RM-how-to-15.png)

<span data-ttu-id="1ed40-111">Когда резервирование завершено и заполнено именованным ресурсом, универсальный ресурс заменяется именованным ресурсом.</span><span class="sxs-lookup"><span data-stu-id="1ed40-111">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

![Именованный участник рабочей группы заменяет универсального участника рабочей группы](media/RM-how-to-16.png)

<span data-ttu-id="1ed40-113">Назначения в расписании также обновляются с именованным ресурсом.</span><span class="sxs-lookup"><span data-stu-id="1ed40-113">The assignments on the schedule are updated with the named resource as well.</span></span>

![Именованный участник рабочей группы, назначенный задачам проекта](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="1ed40-115">Заполнение универсального ресурса несколькими именованными ресурсами</span><span class="sxs-lookup"><span data-stu-id="1ed40-115">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="1ed40-116">Выполнение требования для универсального ресурса с несколькими именованными ресурсами аналогично назначению одного именованного ресурса.</span><span class="sxs-lookup"><span data-stu-id="1ed40-116">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="1ed40-117">Например, имеется задача с длительностью 5 дней и 120 часами необходимых усилий.</span><span class="sxs-lookup"><span data-stu-id="1ed40-117">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="1ed40-118">Эта задача не может быть выполнена одним ресурсом, который работает типичный восьмичасовой рабочий день в пятидневную рабочую неделю.</span><span class="sxs-lookup"><span data-stu-id="1ed40-118">This task can't be completed by one resource that works a typical eight-hour day over a five day week.</span></span> 

![Задача, для которой необходимо 120 часов усилий в течение пяти дней](media/RM-how-to-21.png)

<span data-ttu-id="1ed40-120">Требование содержит 120 часов инженерных работ по робототехнике, что дает 24 часа в день.</span><span class="sxs-lookup"><span data-stu-id="1ed40-120">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

![Требование в день](media/RM-how-to-22.png)

<span data-ttu-id="1ed40-122">В этом примере требуется несколько именованных ресурсов для выполнения требования универсального ресурса.</span><span class="sxs-lookup"><span data-stu-id="1ed40-122">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="1ed40-123">Необходимо зарезервировать несколько ресурсов для выполнения требования.</span><span class="sxs-lookup"><span data-stu-id="1ed40-123">You will need to book multiple resources to fulfill the requirement.</span></span>

![Резервирование нескольких ресурсов для выполнения требования](media/RM-how-to-23.png)

<span data-ttu-id="1ed40-125">Основное отличие в этом сценарии заключается в том, что универсальный ресурс остается в рабочей группе назначенным задаче, а зарезервированные участники рабочей группы, являющиеся именованными ресурсами, не назначаются как часть позиции.</span><span class="sxs-lookup"><span data-stu-id="1ed40-125">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="1ed40-126">Руководитель проекта может назначить работу именованным ресурсам по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="1ed40-126">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="1ed40-127">Представление **Выверка** помогает руководителю проекта в разбиении резервирований нескольких ресурсов на назначения задач.</span><span class="sxs-lookup"><span data-stu-id="1ed40-127">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="1ed40-128">Это не делается автоматически, поскольку в любом сценарии, более сложным чем приведенный выше простой пример, например, где имеется набор задач, составляющих требование, намерение, как руководитель проекта хочет выполнить назначение, должно быть предположено системой.</span><span class="sxs-lookup"><span data-stu-id="1ed40-128">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement, the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="1ed40-129">Поскольку система не может понять намерение, есть вероятность, что предположения будут отличаться от намерений, и неправильный или непредсказуемый результат может получиться.</span><span class="sxs-lookup"><span data-stu-id="1ed40-129">Because the system can't understand intent, chances are that the assumptions will be different than intended and an incorrect or unpredictable result will happen.</span></span> <span data-ttu-id="1ed40-130">Прогнозируемый результат заключается в том, что универсальный ресурс остается назначенным, пока руководитель не создаст намеренно назначения с помощью представления **Выверка**.</span><span class="sxs-lookup"><span data-stu-id="1ed40-130">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>


