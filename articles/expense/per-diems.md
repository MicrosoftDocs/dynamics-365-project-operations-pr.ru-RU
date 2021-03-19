---
title: Суточные
description: Эта тема предоставляет информацию о правилах выплаты суточных, которые используются в управлении расходами.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 70e26a5e0f9a06730a2166318006429195335d4d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276319"
---
# <a name="per-diems"></a><span data-ttu-id="d5330-103">Суточные</span><span class="sxs-lookup"><span data-stu-id="d5330-103">Per diems</span></span>

<span data-ttu-id="d5330-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/без запасов_</span><span class="sxs-lookup"><span data-stu-id="d5330-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="d5330-105">Суточные — это пособие, которое выплачивается работнику, который путешествует по работе.</span><span class="sxs-lookup"><span data-stu-id="d5330-105">A per diem is an allowance that is paid to a worker who is traveling for work.</span></span> <span data-ttu-id="d5330-106">В управлении расходами вы можете создавать правила выплаты суточных для различных командировочных ситуаций.</span><span class="sxs-lookup"><span data-stu-id="d5330-106">In Expense management, you can create per diem rules for  various travel situations.</span></span> <span data-ttu-id="d5330-107">Ставки суточных могут зависеть от времени года, места поездки или и того, и другого.</span><span class="sxs-lookup"><span data-stu-id="d5330-107">Per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="d5330-108">При создании правила суточных вы можете указать, что процент суточных будет удерживаться, если работник получает бесплатное питание или услуги.</span><span class="sxs-lookup"><span data-stu-id="d5330-108">When you create a per diem  rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="d5330-109">Вы также можете установить минимальное и максимальное количество часов, за которые суточные могут применяться к командировкам работника.</span><span class="sxs-lookup"><span data-stu-id="d5330-109">You can also set a minimum and maximum number of hours that the per diem rate can apply to a worker's travel.</span></span>

## <a name="configuration"></a><span data-ttu-id="d5330-110">Настройка</span><span class="sxs-lookup"><span data-stu-id="d5330-110">Configuration</span></span> 

1. <span data-ttu-id="d5330-111">Чтобы добавить местоположения суточных, выберите **Настройка** > **Расчеты и коды** > **Расположение суточных**.</span><span class="sxs-lookup"><span data-stu-id="d5330-111">To add per diem locations, go to **Set up** > **Calculations and codes** > **Per diem locations**.</span></span>
2. <span data-ttu-id="d5330-112">Для каждого из добавленных выше расположений выберите ставку суточных и валюту, которые действительны между определенной датой начала и окончания для гостиницы, питания и других расходов.</span><span class="sxs-lookup"><span data-stu-id="d5330-112">For each of the locations added above, select a per diem rate and currency that is valid between a specific start and end date for hotel, meals, and other expenses.</span></span> <span data-ttu-id="d5330-113">Ставки суточных и валюта настраиваются в разделе **Настройка** > **Расчеты и коды** > **Суточные**.</span><span class="sxs-lookup"><span data-stu-id="d5330-113">Per diem rates and currencies are configured under **Set up** > **Calculations and codes** > **Per diems**.</span></span>
3. <span data-ttu-id="d5330-114">На странице **Расположение суточных** настройте уровни ставок суточных.</span><span class="sxs-lookup"><span data-stu-id="d5330-114">On the **Per diem locations** page, configure per diem rate tiers.</span></span> <span data-ttu-id="d5330-115">Уровни ставок суточных позволяют определить процентное соотношение суточных расходов на проживание, питание и другие расходы.</span><span class="sxs-lookup"><span data-stu-id="d5330-115">Per diem rate tiers allow you to define the percentage split of a daily allowance for hotel, meal, and other expenses.</span></span> 
4. <span data-ttu-id="d5330-116">Чтобы указать процентное сокращение расходов на питание за завтрак, обед или ужин, обновите поля на странице **Параметры управления расходами** на вкладке **Суточные**.</span><span class="sxs-lookup"><span data-stu-id="d5330-116">To specify the meal percentage reduction for breakfast, lunch, or dinner, update the fields on the **Expense management parameters** page on the **Per diem** tab.</span></span> 
    
## <a name="submit-expenses-using-per-diem"></a><span data-ttu-id="d5330-117">Отправка расходов с использованием суточных</span><span class="sxs-lookup"><span data-stu-id="d5330-117">Submit expenses using per diem</span></span>
<span data-ttu-id="d5330-118">Для отправки расходов с использованием суточных используйте категорию расходов **Суточные** при создании отчета о расходах.</span><span class="sxs-lookup"><span data-stu-id="d5330-118">To submit expenses utilizing per diems, use the **Per diem** expense category when you create an expense report.</span></span> <span data-ttu-id="d5330-119">Введите **Ежедневно с сегодняшнего дня**, **Ежедневно до настоящего времени** и **Расположение суточных**.</span><span class="sxs-lookup"><span data-stu-id="d5330-119">Enter the **Per diem from date**, **Per diem to date**,  and the **Per diem location**.</span></span> <span data-ttu-id="d5330-120">Сумма будет рассчитана на основе ставок суточных для выбранного места, а уменьшение стоимости питания будет рассчитано на основе уровней ставок суточных.</span><span class="sxs-lookup"><span data-stu-id="d5330-120">The amount will be calculated based on the per diem rates for the selected location and meal reduction will be calculated based on the per diem rate tiers.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]