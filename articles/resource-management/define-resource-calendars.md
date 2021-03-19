---
title: Определение календарей ресурсов
description: Эта тема предоставляет информацию о том, как определить календари рабочего времени для ресурсов в Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: a7b7c45ad2116519b0369bfd3d7cf6743704f4e1
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279829"
---
# <a name="define-resource-calendars"></a><span data-ttu-id="99da2-103">Определение календарей ресурсов</span><span class="sxs-lookup"><span data-stu-id="99da2-103">Define resource calendars</span></span>

<span data-ttu-id="99da2-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="99da2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="99da2-105">Каждый доступный для резервирования ресурс, работающий над проектом, должен иметь календарь рабочих часов, чтобы определить их доступность.</span><span class="sxs-lookup"><span data-stu-id="99da2-105">Each bookable resource working on a project must have a calendar of working hours to define their availability.</span></span> <span data-ttu-id="99da2-106">Рабочие часы для ресурса можно определить двумя способами:</span><span class="sxs-lookup"><span data-stu-id="99da2-106">Workings hours for a resource can be defined in two ways:</span></span> 

   - <span data-ttu-id="99da2-107">Определите индивидуальные календарные правила для ресурса</span><span class="sxs-lookup"><span data-stu-id="99da2-107">Define individual calendar rules for a resource</span></span>
   - <span data-ttu-id="99da2-108">Примените существующий шаблон календаря для ресурса</span><span class="sxs-lookup"><span data-stu-id="99da2-108">Apply an existing calendar template for the resource</span></span>

## <a name="define-a-resources-working-hours"></a><span data-ttu-id="99da2-109">Определение рабочих часов ресурса</span><span class="sxs-lookup"><span data-stu-id="99da2-109">Define a resource's working hours</span></span>

1. <span data-ttu-id="99da2-110">В меню **Ресурсы** выберите **Ресурсы**.</span><span class="sxs-lookup"><span data-stu-id="99da2-110">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="99da2-111">В представлении сетки выберите подходящий **Резервируемый ресурс**.</span><span class="sxs-lookup"><span data-stu-id="99da2-111">From the grid view, select the applicable **Bookable Resource**.</span></span>
3. <span data-ttu-id="99da2-112">На странице **Сведения о ресурсах** выберите вкладку **Рабочие часы**. По умолчанию для календаря резервируемых ресурсов используются рабочие часы из шаблона рабочего времени по умолчанию, определенного для организации.</span><span class="sxs-lookup"><span data-stu-id="99da2-112">On the **Resource Details** page, select the **Working Hours** tab. By default, the bookable resources calendar defaults to the working hours of the default work hour template that is defined for the organization.</span></span>
4. <span data-ttu-id="99da2-113">Чтобы обновить рабочие часы, щелкните правой кнопкой мыши дату начала предлагаемого календарного правила, которое необходимо определить.</span><span class="sxs-lookup"><span data-stu-id="99da2-113">To update the working hours, right-click on the start date of the proposed calendar rule to be defined.</span></span> <span data-ttu-id="99da2-114">Используйте меню правила календаря, чтобы определить правило календаря для определенного дня, остатка ряда или всего календаря.</span><span class="sxs-lookup"><span data-stu-id="99da2-114">Use the calendar rule menu to define a calendar rule for a specific day, the remainder of the series, or the entire calendar.</span></span>
5. <span data-ttu-id="99da2-115">После выбора опции вы можете определить:</span><span class="sxs-lookup"><span data-stu-id="99da2-115">After the option is selected, you can then define:</span></span>

    - <span data-ttu-id="99da2-116">День недели, в который будет применяться рабочее время.</span><span class="sxs-lookup"><span data-stu-id="99da2-116">The day of the week where the working hours will apply.</span></span>
    - <span data-ttu-id="99da2-117">Промежутки рабочего времени в течение каждого дня.</span><span class="sxs-lookup"><span data-stu-id="99da2-117">The working times within each day.</span></span>
    - <span data-ttu-id="99da2-118">Часовой пояс для правила календаря.</span><span class="sxs-lookup"><span data-stu-id="99da2-118">The time zone for the calendar rule.</span></span>
    - <span data-ttu-id="99da2-119">Если применимо, для правила также можно указать нерабочее время.</span><span class="sxs-lookup"><span data-stu-id="99da2-119">If applicable, non-working time can also be specified for the rule.</span></span>

## <a name="applying-a-calendar-template-to-a-resource"></a><span data-ttu-id="99da2-120">Применение шаблона календаря к ресурсу</span><span class="sxs-lookup"><span data-stu-id="99da2-120">Applying a calendar template to a resource</span></span>

1. <span data-ttu-id="99da2-121">В меню **Ресурсы** выберите **Ресурсы**.</span><span class="sxs-lookup"><span data-stu-id="99da2-121">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="99da2-122">В виде сетки выберите до 25 **Резервируемых ресурсов** для обновления.</span><span class="sxs-lookup"><span data-stu-id="99da2-122">From the grid view, select up to 25 **Bookable Resources** to update.</span></span>
3. <span data-ttu-id="99da2-123">Выберите **Задать календарь**, и диалоговое окно предложит вам список доступных шаблонов рабочего времени.</span><span class="sxs-lookup"><span data-stu-id="99da2-123">Select **Set Calendar** and a dialog will prompt you with a list of available work hour templates.</span></span>
4. <span data-ttu-id="99da2-124">Выберите шаблон, который хотите использовать, затем выберите **Применить**.</span><span class="sxs-lookup"><span data-stu-id="99da2-124">Select the template you want to use, and then select **Apply**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]