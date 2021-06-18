---
title: Выполнение универсального требования к ресурсам
description: В этом разделе представлена информация о том, как резервировать именованные ресурсы для требования универсального ресурса.
author: ruhercul
ms.date: 09/23/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e36875a0d5dcb24d9669e2ea989c6fc7db7bcd7c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005852"
---
# <a name="generic-resource-requirement-fulfillment"></a><span data-ttu-id="47bdc-103">Выполнение универсального требования к ресурсам</span><span class="sxs-lookup"><span data-stu-id="47bdc-103">Generic resource requirement fulfillment</span></span>

<span data-ttu-id="47bdc-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="47bdc-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="47bdc-105">Вы можете зарезервировать именованный ресурс для замены универсального ресурса, имеющего требование ресурса.</span><span class="sxs-lookup"><span data-stu-id="47bdc-105">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="47bdc-106">На странице **Проекты** выберите вкладку **Рабочая группа**.</span><span class="sxs-lookup"><span data-stu-id="47bdc-106">On the **Projects** page, select the **Team** tab.</span></span>
2. <span data-ttu-id="47bdc-107">Выберите универсальный ресурс, имеющий требование ресурса, в списке, затем выберите **Резервировать**.</span><span class="sxs-lookup"><span data-stu-id="47bdc-107">Select the generic resource that has a resource requirement from the list, and then select **Book**.</span></span> <span data-ttu-id="47bdc-108">Или откройте требование ресурса, затем выберите **Резервировать**.</span><span class="sxs-lookup"><span data-stu-id="47bdc-108">Or, open the resource requirement and then select **Book**.</span></span>
3. <span data-ttu-id="47bdc-109">На странице **Помощник по расписанию** выберите именованный ресурс для резервирования в проектную группу, затем выберите **Резервировать**.</span><span class="sxs-lookup"><span data-stu-id="47bdc-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then select **Book**.</span></span>

<span data-ttu-id="47bdc-110">Когда резервирование завершено и заполнено именованным ресурсом, универсальный ресурс заменяется именованным ресурсом.</span><span class="sxs-lookup"><span data-stu-id="47bdc-110">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

<span data-ttu-id="47bdc-111">Назначения в расписании также обновляются с именованным ресурсом.</span><span class="sxs-lookup"><span data-stu-id="47bdc-111">The assignments on the schedule are updated with the named resource as well.</span></span>

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="47bdc-112">Заполнение универсального ресурса несколькими именованными ресурсами</span><span class="sxs-lookup"><span data-stu-id="47bdc-112">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="47bdc-113">Выполнение требования для универсального ресурса с несколькими именованными ресурсами аналогично назначению одного именованного ресурса.</span><span class="sxs-lookup"><span data-stu-id="47bdc-113">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="47bdc-114">Например, имеется задача с длительностью 5 дней и 120 часами необходимых усилий.</span><span class="sxs-lookup"><span data-stu-id="47bdc-114">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="47bdc-115">Эта задача не может быть выполнена одним ресурсом, который работает типичный восьмичасовой рабочий день в пятидневную рабочую неделю.</span><span class="sxs-lookup"><span data-stu-id="47bdc-115">This task can't be completed by one resource that works a typical eight-hour day over a five-day week.</span></span> 

<span data-ttu-id="47bdc-116">Требование содержит 120 часов инженерных работ по робототехнике, что дает 24 часа в день.</span><span class="sxs-lookup"><span data-stu-id="47bdc-116">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

<span data-ttu-id="47bdc-117">В этом примере требуется несколько именованных ресурсов для выполнения требования универсального ресурса.</span><span class="sxs-lookup"><span data-stu-id="47bdc-117">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="47bdc-118">Необходимо зарезервировать несколько ресурсов для выполнения требования.</span><span class="sxs-lookup"><span data-stu-id="47bdc-118">You will need to book multiple resources to fulfill the requirement.</span></span>

<span data-ttu-id="47bdc-119">Основное отличие в этом сценарии заключается в том, что универсальный ресурс остается в рабочей группе назначенным задаче, а зарезервированные участники рабочей группы, являющиеся именованными ресурсами, не назначаются как часть позиции.</span><span class="sxs-lookup"><span data-stu-id="47bdc-119">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="47bdc-120">Руководитель проекта может назначить работу именованным ресурсам по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="47bdc-120">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="47bdc-121">Представление **Выверка** помогает руководителю проекта в разбиении резервирований нескольких ресурсов на назначения задач.</span><span class="sxs-lookup"><span data-stu-id="47bdc-121">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="47bdc-122">Это не делается автоматически, поскольку в любом сценарии, более сложным чем приведенный выше простой пример, например, где имеется набор задач, составляющих требование или намерение, как руководитель проекта хочет выполнить назначение, должно быть предположено системой.</span><span class="sxs-lookup"><span data-stu-id="47bdc-122">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement or the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="47bdc-123">Поскольку система не может понять намерения, вероятно, что предположения будут отличаться от запланированных и произойдет неправильный или непредсказуемый результат.</span><span class="sxs-lookup"><span data-stu-id="47bdc-123">Because the system can't understand intent, it's likely that the assumptions will be different than intended and an incorrect or unpredictable result will occur.</span></span> <span data-ttu-id="47bdc-124">Прогнозируемый результат заключается в том, что универсальный ресурс остается назначенным, пока руководитель не создаст намеренно назначения с помощью представления **Выверка**.</span><span class="sxs-lookup"><span data-stu-id="47bdc-124">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]