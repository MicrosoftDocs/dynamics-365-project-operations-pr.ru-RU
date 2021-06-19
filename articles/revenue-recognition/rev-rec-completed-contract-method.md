---
title: Управление оценками дохода
description: В этом разделе представлена информация о том, как работать с оценками дохода для проектов.
author: sigitac
ms.date: 11/04/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e3cbaff18d8bd4d6f6a7577bba25b3e843b1757e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013863"
---
# <a name="manage-revenue-estimates"></a><span data-ttu-id="5919f-103">Управление оценками дохода</span><span class="sxs-lookup"><span data-stu-id="5919f-103">Manage revenue estimates</span></span>

<span data-ttu-id="5919f-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/без запасов_</span><span class="sxs-lookup"><span data-stu-id="5919f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="5919f-105">Вы можете создавать, рассчитывать, разносить, отменять или исключать оценки доходов.</span><span class="sxs-lookup"><span data-stu-id="5919f-105">You can create, calculate, post, reverse, or eliminate revenue estimates.</span></span> <span data-ttu-id="5919f-106">Вы можете сделать это вручную или с помощью периодического процесса.</span><span class="sxs-lookup"><span data-stu-id="5919f-106">You can do this either manually or by using a periodic process.</span></span> <span data-ttu-id="5919f-107">В этом разделе представлена информация о том, как работать с оценками дохода для проектов.</span><span class="sxs-lookup"><span data-stu-id="5919f-107">This topic provides information about how to work with revenue estimates for projects.</span></span>

### <a name="manage-revenue-estimates-manually"></a><span data-ttu-id="5919f-108">Управление оценками дохода вручную</span><span class="sxs-lookup"><span data-stu-id="5919f-108">Manage revenue estimates manually</span></span>

<span data-ttu-id="5919f-109">В проекте оценки дохода с фиксированной ценой или на странице **Запрос на оценку** (**Управление и учет по проектам** > **Отчеты и запросы** > **Запросы на оценку и отчеты**), выберите **Оценки**.</span><span class="sxs-lookup"><span data-stu-id="5919f-109">On the fixed price revenue estimate project or the **Estimate inquiry** page (**Project management and accounting** > **Reports and inquiries** > **Estimates inquiries and reports**), select **Estimates**.</span></span>

### <a name="manage-revenue-estimates-using-a-periodic-process"></a><span data-ttu-id="5919f-110">Управляйте оценками дохода, используя периодический процесс</span><span class="sxs-lookup"><span data-stu-id="5919f-110">Manage revenue estimates using a periodic process</span></span>

<span data-ttu-id="5919f-111">Перейдите к **Управление и учет по проектам** > **Периодический** > **Оценки** и выберите соответствующий процесс.</span><span class="sxs-lookup"><span data-stu-id="5919f-111">Go to **Project management and accounting** > **Periodic** > **Estimates** and select the corresponding process.</span></span>

## <a name="create-a-revenue-estimate"></a><span data-ttu-id="5919f-112">Создайте оценку дохода</span><span class="sxs-lookup"><span data-stu-id="5919f-112">Create a revenue estimate</span></span>

<span data-ttu-id="5919f-113">Для создания оценки дохода выполните следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="5919f-113">Complete the following steps to create a revenue estimate.</span></span> 

1. <span data-ttu-id="5919f-114">Перейти к **Управление и учет по проектам** > **Периодический** > **Оценки**.</span><span class="sxs-lookup"><span data-stu-id="5919f-114">Go to **Project management and accounting** > **Periodic** > **Estimates**.</span></span>
2. <span data-ttu-id="5919f-115">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="5919f-115">Select **New**.</span></span> <span data-ttu-id="5919f-116">На странице **Создание оценки** выберите следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="5919f-116">On the **Estimate creation** page, select the following parameters:</span></span>

   - <span data-ttu-id="5919f-117">**Код периода**: этот код определяет, как часто разносятся оценки.</span><span class="sxs-lookup"><span data-stu-id="5919f-117">**Period code**: This code determines how frequently estimates are posted.</span></span>
   - <span data-ttu-id="5919f-118">**Дата оценки**: дата обработки оценки.</span><span class="sxs-lookup"><span data-stu-id="5919f-118">**Estimate date**: The date the estimate is processed.</span></span>
   - <span data-ttu-id="5919f-119">**Непрерывный**: установите этот флажок, чтобы создавать оценки, только если оценки были разнесены в предыдущий период или если оценка является первой созданной оценкой.</span><span class="sxs-lookup"><span data-stu-id="5919f-119">**Continuous**: Select this check box to create estimates only if estimates were posted in the previous period, or if the estimate is the first estimate that has been created.</span></span> <span data-ttu-id="5919f-120">Если этот параметр не выбран, оценки создаются, даже если оценки не разносились в предыдущем периоде.</span><span class="sxs-lookup"><span data-stu-id="5919f-120">If this is not selected, estimates are created even if estimates were not posted in the previous period.</span></span>
   - <span data-ttu-id="5919f-121">**Метод вычисления стоимости для завершения**: определите, как оценить оставшуюся работу по проекту.</span><span class="sxs-lookup"><span data-stu-id="5919f-121">**Cost to complete method**: Define how to estimate the remaining project work.</span></span> <span data-ttu-id="5919f-122">Дополнительные сведения см. в [Методы вычисления стоимости для завершения](cost-complete-methods.md).</span><span class="sxs-lookup"><span data-stu-id="5919f-122">For more information, see [Cost to complete methods](cost-complete-methods.md).</span></span>
   - <span data-ttu-id="5919f-123">**Метод завершения** : Выберите метод завершения из следующих вариантов:</span><span class="sxs-lookup"><span data-stu-id="5919f-123">**Completion method**: Select a completion method from the following options:</span></span>
     - <span data-ttu-id="5919f-124">**Автоматический**: процент завершения рассчитывается автоматически и на основе строк затрат, включенных в расчет.</span><span class="sxs-lookup"><span data-stu-id="5919f-124">**Automatic**: The completion percentage is calculated automatically and based on the cost lines included in the calculation.</span></span> <span data-ttu-id="5919f-125">Шаблон затрат определяет включаемые строки затрат.</span><span class="sxs-lookup"><span data-stu-id="5919f-125">The cost template defines the cost lines that are included.</span></span>
     - <span data-ttu-id="5919f-126">**Вручную**: процент завершения равен проценту завершения последней оценки.</span><span class="sxs-lookup"><span data-stu-id="5919f-126">**Manual**: The completion percentage equals the completion percentage of the last estimate.</span></span> <span data-ttu-id="5919f-127">После создания сметы вы можете изменить **Расчет вручную** на странице **Оценки**.</span><span class="sxs-lookup"><span data-stu-id="5919f-127">After the estimate is created, you can change the **Manual calculation** on the **Estimates** page.</span></span>
     - <span data-ttu-id="5919f-128">**Из шаблона стоимости**: сочетание автоматического и ручного методов.</span><span class="sxs-lookup"><span data-stu-id="5919f-128">**From cost template**: A combination of the automatic and manual methods.</span></span> <span data-ttu-id="5919f-129">Этот параметр устанавливается автоматически или вручную в зависимости от значения по умолчанию в шаблоне стоимости.</span><span class="sxs-lookup"><span data-stu-id="5919f-129">This option is set automatically or manually, depending on the default value in the cost template.</span></span>
   - <span data-ttu-id="5919f-130">**Модель прогноза**: выберите модель прогноза для оценки.</span><span class="sxs-lookup"><span data-stu-id="5919f-130">**Forecast model**: Select a forecast model for the estimate.</span></span>
   - <span data-ttu-id="5919f-131">**Распечатать список оценок**: создать и показать список оценок.</span><span class="sxs-lookup"><span data-stu-id="5919f-131">**Print estimate list**: Create and show an estimate list.</span></span> <span data-ttu-id="5919f-132">Список содержит статус текущей функции.</span><span class="sxs-lookup"><span data-stu-id="5919f-132">The list contains the status of the current function.</span></span> <span data-ttu-id="5919f-133">Вы можете распечатать любые предупреждения об оценке в отчете.</span><span class="sxs-lookup"><span data-stu-id="5919f-133">You can print any warnings about the estimate on the report.</span></span> <span data-ttu-id="5919f-134">Следующие условия вызывают появление предупреждений в списке оценок:</span><span class="sxs-lookup"><span data-stu-id="5919f-134">The following conditions cause warnings to appear in the estimate list:</span></span>
     - <span data-ttu-id="5919f-135">Процент выполнения более 100 процентов.</span><span class="sxs-lookup"><span data-stu-id="5919f-135">A completion percentage of more than 100 percent.</span></span>
     - <span data-ttu-id="5919f-136">Процент выполнения менее ноля процентов.</span><span class="sxs-lookup"><span data-stu-id="5919f-136">A completion percentage less than zero percent.</span></span>
     - <span data-ttu-id="5919f-137">Отрицательная сумма в столбец **Для выполнения**.</span><span class="sxs-lookup"><span data-stu-id="5919f-137">A negative amount in the **To complete** column.</span></span>
     - <span data-ttu-id="5919f-138">Оценка без соответствующей суммы контракта.</span><span class="sxs-lookup"><span data-stu-id="5919f-138">An estimate with no corresponding contract amount.</span></span>
     - <span data-ttu-id="5919f-139">Оценка без прилагаемой оценки стоимости.</span><span class="sxs-lookup"><span data-stu-id="5919f-139">An estimate with no attached cost estimate.</span></span>
   - <span data-ttu-id="5919f-140">**Показать Infolog**: выберите этот параметр, чтобы получать сообщение, содержащее информацию о проектах оценки, которые были обработаны при выполнении задания.</span><span class="sxs-lookup"><span data-stu-id="5919f-140">**Show Infolog**: Select this option to receive a message that contains information about the estimate projects that were processed when the job was run.</span></span>


## <a name="post-wip-or-accruals"></a><span data-ttu-id="5919f-141">Разнести НЗП или начисления</span><span class="sxs-lookup"><span data-stu-id="5919f-141">Post WIP or accruals</span></span>

<span data-ttu-id="5919f-142">После оценки оценок они сохраняются, понижаются или повышаются.</span><span class="sxs-lookup"><span data-stu-id="5919f-142">After the estimates are evaluated, they are maintained, decreased, or increased.</span></span> <span data-ttu-id="5919f-143">Затем вы можете разнести НЗП, когда будете работать с принцип оценки **Завершенный контракт**, или разнести начисления, когда вы работаете с принцип оценки **Завершенный процент**.</span><span class="sxs-lookup"><span data-stu-id="5919f-143">You can then post the WIP when you work with the **Completed contract** assessment principle, or post the accruals when you work with the **Completed percentage** assessment principle.</span></span>
  
<span data-ttu-id="5919f-144">Статус периода оценки изменится с **Создано** на **Разнесено**.</span><span class="sxs-lookup"><span data-stu-id="5919f-144">The estimate period status changes from **Created** to **Posted**.</span></span>

## <a name="reverse-wip-or-accruals"></a><span data-ttu-id="5919f-145">Обратное НЗП или начисления</span><span class="sxs-lookup"><span data-stu-id="5919f-145">Reverse WIP or accruals</span></span>

<span data-ttu-id="5919f-146">Используйте вариант сторнирования для кредитования уже разнесенных НЗП или начислений, а затем создайте оценки за период.</span><span class="sxs-lookup"><span data-stu-id="5919f-146">Use the reverse option to credit already posted WIP or accruals, and then create estimates for the period.</span></span>

> [!NOTE]
> <span data-ttu-id="5919f-147">Чтобы сторнировать период, который находится между другими периодами, сторнируйте необходимые периоды оценки и затем вновь разнесите их.</span><span class="sxs-lookup"><span data-stu-id="5919f-147">To reverse a period that is in between other periods, reverse the necessary estimate periods and then repost them.</span></span> <span data-ttu-id="5919f-148">Поскольку все последующие периоды зависят от оценок за предыдущий период, не пропускайте никакие периоды.</span><span class="sxs-lookup"><span data-stu-id="5919f-148">Because all subsequent periods depend on the estimates from the previous period, don't skip any periods.</span></span>

## <a name="eliminate-the-estimate-project-and-finish-the-project"></a><span data-ttu-id="5919f-149">Исключить проект оценки и завершить проект</span><span class="sxs-lookup"><span data-stu-id="5919f-149">Eliminate the estimate project and finish the project</span></span>

<span data-ttu-id="5919f-150">Заключительный шаг в процессе оценки — исключить проект оценки и завершить проект с фиксированной ценой, когда процент выполнения достигнет 100 процентов.</span><span class="sxs-lookup"><span data-stu-id="5919f-150">The final step in the estimate process is to eliminate the estimate project and end the fixed price project when the percentage of completion reaches 100 percent.</span></span>

<span data-ttu-id="5919f-151">При выполнении исключения происходит следующее:</span><span class="sxs-lookup"><span data-stu-id="5919f-151">The following occurs when you run the elimination:</span></span>

- <span data-ttu-id="5919f-152">Для проекта с фиксированной ценой и завершенным контрактом значения НЗП снимаются с балансовых счетов и разносятся по счетам прибылей и убытков.</span><span class="sxs-lookup"><span data-stu-id="5919f-152">For a fixed price project with a completed contract, the WIP values clear from the balance accounts and post to the profit and loss accounts.</span></span>
- <span data-ttu-id="5919f-153">Для проекта с фиксированной ценой и выполненным процентом начисления удаляются из счетов прибылей и убытков.</span><span class="sxs-lookup"><span data-stu-id="5919f-153">For a fixed-price project with a completed percentage, the accruals are removed from the profit and loss accounts.</span></span>

<span data-ttu-id="5919f-154">Оценка меняет статус на **Исключено**.</span><span class="sxs-lookup"><span data-stu-id="5919f-154">The estimate changes the status to **Eliminated**.</span></span>

> [!NOTE]
> <span data-ttu-id="5919f-155">В особых случаях процентное соотношение может превышать 100 процентов.</span><span class="sxs-lookup"><span data-stu-id="5919f-155">In special cases, the percentage can extend beyond 100 percent.</span></span> <span data-ttu-id="5919f-156">В этом случае уменьшите процент выполнения, используя **Задать метод нулевой стоимости для завершения**, чтобы достичь 100 процентов.</span><span class="sxs-lookup"><span data-stu-id="5919f-156">When this happens, reduce the percentage of completion by using the **Set cost to complete to zero method** to reach 100 percent.</span></span>

## <a name="reverse-elimination"></a><span data-ttu-id="5919f-157">Отменить исключение</span><span class="sxs-lookup"><span data-stu-id="5919f-157">Reverse elimination</span></span>

1. <span data-ttu-id="5919f-158">Перейти к **Управление и учет по проектам** > **Периодические** > **Оценки** > **Отменить исключение**.</span><span class="sxs-lookup"><span data-stu-id="5919f-158">Go to **Project management and accounting** > **Periodic** > **Estimates** > **Reverse elimination**.</span></span> 
2. <span data-ttu-id="5919f-159">На панели действий на вкладка **Процесс** в группе **Ведение** выберите **Оценка**.</span><span class="sxs-lookup"><span data-stu-id="5919f-159">On the Action Pane, on the **Process** tab, in the **Maintain** group, select **Estimate**.</span></span> 
3. <span data-ttu-id="5919f-160">Выберите **Отменить исключение**.</span><span class="sxs-lookup"><span data-stu-id="5919f-160">Select **Reverse elimination**.</span></span>

<span data-ttu-id="5919f-161">Используйте эту страницу, чтобы отменить все исключения с указанной датой оценки и статусом оценки **Исключено**.</span><span class="sxs-lookup"><span data-stu-id="5919f-161">Use this page to reverse all eliminations with a specified estimate date and with an estimate status of **Eliminated**.</span></span> <span data-ttu-id="5919f-162">Статус транзакции изменится после того, как вы выберете соответствующие поля.</span><span class="sxs-lookup"><span data-stu-id="5919f-162">The transaction status changes after you select the appropriate fields.</span></span>

<span data-ttu-id="5919f-163">Это также автоматически изменяет статус проекта на **В процессе**, если стадия проекта завершена.</span><span class="sxs-lookup"><span data-stu-id="5919f-163">This also automatically changes the project status to **In process** if the project stage is set to finished.</span></span> <span data-ttu-id="5919f-164">Статус оценки периода проекта снова изменится на **Разнесено**.</span><span class="sxs-lookup"><span data-stu-id="5919f-164">The estimate status of the project period changes back to **Posted**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]