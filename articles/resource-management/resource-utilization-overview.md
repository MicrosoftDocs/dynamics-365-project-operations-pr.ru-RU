---
title: Обзор загруженности ресурсов
description: В этой теме представлена информация о загруженности ресурсов в Project Operations.
author: ruhercul
ms.date: 11/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: a683931bcd6a357c5feec9198b190b948ad17a40
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000812"
---
# <a name="resource-utilization-overview"></a><span data-ttu-id="61fa5-103">Обзор загруженности ресурсов</span><span class="sxs-lookup"><span data-stu-id="61fa5-103">Resource utilization overview</span></span>

<span data-ttu-id="61fa5-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="61fa5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="61fa5-105">Ресурсы могут иметь целевую оплачиваемую загруженность.</span><span class="sxs-lookup"><span data-stu-id="61fa5-105">Resources can have a target billable utilization.</span></span> <span data-ttu-id="61fa5-106">Эта целевая загруженность определяется как атрибут роли ресурса по умолчанию или задается в записи отдельного резервируемого ресурса.</span><span class="sxs-lookup"><span data-stu-id="61fa5-106">This target utilization is defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="61fa5-107">Расчеты загруженности основаны на фактических часах, о которых сообщают ресурсы с помощью утвержденных записей времени.</span><span class="sxs-lookup"><span data-stu-id="61fa5-107">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="61fa5-108">Формулы следующие используются для расчета загруженности:</span><span class="sxs-lookup"><span data-stu-id="61fa5-108">The following formulas are used to calculate utilization:</span></span>

  - <span data-ttu-id="61fa5-109">Оплачиваемая загруженность = Оплачиваемые фактические часов ÷ Производительность ресурса</span><span class="sxs-lookup"><span data-stu-id="61fa5-109">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
  - <span data-ttu-id="61fa5-110">Неоплачиваемая загруженность = Фактическое время с ИД типа выставления счетов = Не подлежит оплате, Бесплатно или Недоступно ÷ Производительность ресурса</span><span class="sxs-lookup"><span data-stu-id="61fa5-110">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
  - <span data-ttu-id="61fa5-111">Внутреннее = Фактическое время без контракта на продажу ÷ Производительность ресурса</span><span class="sxs-lookup"><span data-stu-id="61fa5-111">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
  - <span data-ttu-id="61fa5-112">Производительность ресурса = Рабочие часы ресурса – Не на работе – Нерабочие дни</span><span class="sxs-lookup"><span data-stu-id="61fa5-112">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="61fa5-113">Представление **Загруженность ресурсов** можно найти на панели **Ресурсы**.</span><span class="sxs-lookup"><span data-stu-id="61fa5-113">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

<span data-ttu-id="61fa5-114">Каждая ячейка в сетке представляет процент оплачиваемой загруженности ресурса в период, такой как день, неделя или месяц.</span><span class="sxs-lookup"><span data-stu-id="61fa5-114">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="61fa5-115">Следующие формулы используются для задания цветов ячеек:</span><span class="sxs-lookup"><span data-stu-id="61fa5-115">The following formulas are used to color the cells:</span></span>

  - <span data-ttu-id="61fa5-116">**Зеленый**: Оплачиваемая загруженность >= Целевая загруженность ресурса</span><span class="sxs-lookup"><span data-stu-id="61fa5-116">**Green**: Billable utilization >= Resource target utilization</span></span>
  - <span data-ttu-id="61fa5-117">**Желтый**: Целевая загруженность – 20 <= Оплачиваемая загруженность < Целевая загруженность</span><span class="sxs-lookup"><span data-stu-id="61fa5-117">**Yellow**: Target utilization – 20 <= Billable utilization < Target utilization</span></span>
  - <span data-ttu-id="61fa5-118">**Красный**: Оплачиваемая загруженность < Целевая загруженность – 20</span><span class="sxs-lookup"><span data-stu-id="61fa5-118">**Red**: Billable utilization < Target utilization – 20</span></span>

<span data-ttu-id="61fa5-119">Поскольку представление **Загруженность ресурсов** основано на доске расписания, можно использовать возможности фильтрации доски расписания для фильтрации результатов.</span><span class="sxs-lookup"><span data-stu-id="61fa5-119">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="61fa5-120">Сетка требует, чтобы вы задали целевую загруженность для роли или отдельного ресурса.</span><span class="sxs-lookup"><span data-stu-id="61fa5-120">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="61fa5-121">Чтобы выполнить эту настройку, выберите **Ресурсы** > **Роли ресурса**.</span><span class="sxs-lookup"><span data-stu-id="61fa5-121">To do this setup, go to **Resources** > **Resource roles**.</span></span>

<span data-ttu-id="61fa5-122">Кроме того, необходимо назначить роль по умолчанию всем резервируемым ресурсам.</span><span class="sxs-lookup"><span data-stu-id="61fa5-122">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="61fa5-123">Выберите **Ресурсы** > **Ресурсы**.</span><span class="sxs-lookup"><span data-stu-id="61fa5-123">Go to **Resources** > **Resources**.</span></span> <span data-ttu-id="61fa5-124">На вкладке **Project Service** убедитесь, что определена роль ресурса, и что в поле **По умолчанию** установлено значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="61fa5-124">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field is set to **Yes**.</span></span> <span data-ttu-id="61fa5-125">Можно добавить дополнительные роли, в которых **По умолчанию** = **Нет**.</span><span class="sxs-lookup"><span data-stu-id="61fa5-125">You can add additional roles where **Is Default** = **No**.</span></span> <span data-ttu-id="61fa5-126">Роль, в которой **По умолчанию** = **Да**, используется для оценки загруженности ресурса относительно цели для этой роли.</span><span class="sxs-lookup"><span data-stu-id="61fa5-126">The role where the **Is Default** = **Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

<span data-ttu-id="61fa5-127">На вкладке **Project Service** можно также задать индивидуальную целевую загруженность для ресурса.</span><span class="sxs-lookup"><span data-stu-id="61fa5-127">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="61fa5-128">Расчет загруженности затем использует целевую загруженность, чтобы оценить цель ресурса вместо цели роли ресурса по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="61fa5-128">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="61fa5-129">Загруженность отображается для ресурса только в том случае, если этот ресурс имеет утвержденное оплачиваемое время в течение периода, который отображается в сетке.</span><span class="sxs-lookup"><span data-stu-id="61fa5-129">Utilization is only shown for a resource if that resource has approved, chargeable time during the period shown in the grid.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]