---
title: Импорт оценки в строку контракта на основе проекта — облегченное развертывание
description: Эта тема предоставляет информацию об импорте финансовых оценок из проекта в строку контракта.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b6b017177e718110969363844d5db4c393949d28
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273484"
---
# <a name="import-an-estimate-to-a-project-based-contract-line---lite"></a><span data-ttu-id="2b629-103">Импорт оценки в строку контракта на основе проекта — облегченное развертывание</span><span class="sxs-lookup"><span data-stu-id="2b629-103">Import an estimate to a project-based contract line - lite</span></span>

<span data-ttu-id="2b629-104">_**Относится к:** развертывание Lite — от сделки до счетов-проформ_</span><span class="sxs-lookup"><span data-stu-id="2b629-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2b629-105">В Dynamics 365 Project Operations вы можете импортировать оценки из проекта в строку контракта на основе проекта.</span><span class="sxs-lookup"><span data-stu-id="2b629-105">In Dynamics 365 Project Operations, you can import estimates from a project to a project-based contract line.</span></span>

1. <span data-ttu-id="2b629-106">Убедитесь, что поле **Проект** в строке контракта на основе проекта заполнено.</span><span class="sxs-lookup"><span data-stu-id="2b629-106">Verify that the **Project** field on the project-based contract line has been filled in.</span></span>
2. <span data-ttu-id="2b629-107">На вкладке **Сведения строки контракта** во вложенной сетке выберите **Импортировать из оценки проекта**.</span><span class="sxs-lookup"><span data-stu-id="2b629-107">On the **Contract Line Details** tab, on the subgrid, select **Import from Project Estimation**.</span></span> <span data-ttu-id="2b629-108">Откроется диалоговая страница с параметрами суммирования.</span><span class="sxs-lookup"><span data-stu-id="2b629-108">A dialog page with summarization options opens.</span></span> <span data-ttu-id="2b629-109">Доступны следующие параметры суммирования: **Класс транзакций**, **Категория**, **Роль** и **Задача проекта**.</span><span class="sxs-lookup"><span data-stu-id="2b629-109">Summarization options available are **Transaction Class**, **Category**, **Role**, and **Project Task**.</span></span>
3. <span data-ttu-id="2b629-110">На основании выбора сводки оценка из проекта для всех классов транзакций и задач, включенных в эту строку контракта, копируется.</span><span class="sxs-lookup"><span data-stu-id="2b629-110">Based on the summary selection, the estimate from the project for all the transaction classes and tasks included on this contract line are copied.</span></span> <span data-ttu-id="2b629-111">Чтобы проверить, какие классы транзакций включены, на вкладке **Общие** в строке контракта по проекту проверьте значения в полях **Включить время**, **Включить расходы** и **Включить сборы**.</span><span class="sxs-lookup"><span data-stu-id="2b629-111">To check what transaction classes are included, on the **General** tab on the project-based contract line, check the values in the **Include Time**, **Include Expenses**, and **Include Fees** fields.</span></span> 
4. <span data-ttu-id="2b629-112">Чтобы увидеть, какие задачи включены, выберите вкладку **Оплачиваемые задачи** в строке контракта.</span><span class="sxs-lookup"><span data-stu-id="2b629-112">To see what tasks are included, select the **Chargeable Tasks** tab on the contract line.</span></span> <span data-ttu-id="2b629-113">На основе связанных задач, у которых в поле **Включенные классы транзакций** установлено значение **Да**, все оценки для этих комбинаций задач и классов транзакций импортируются в строку контракта.</span><span class="sxs-lookup"><span data-stu-id="2b629-113">Based on the associated tasks that have the field **Included Transaction Classes** set to **Yes**, all estimates for those task and transaction class combinations are imported to the contract line.</span></span>

<span data-ttu-id="2b629-114">Когда вы импортируете оценки, система по умолчанию устанавливает цены на основе прайс-листов проекта, прикрепленных к контракту, и типа выставления счетов, настроенного в строке контракта.</span><span class="sxs-lookup"><span data-stu-id="2b629-114">When you import estimates, the system defaults pricing based on the project price lists attached to the contract and billing type setup on the contract line.</span></span> <span data-ttu-id="2b629-115">Если задача, роль или категория настроены в строке контракта как нетарифицируемая, импортированная строка оценки будет установлена как нетарифицируемая и не будет добавляться к контрактному значению строки контракта.</span><span class="sxs-lookup"><span data-stu-id="2b629-115">If a task, role, or category is set up on the contract line as non-chargeable, the imported estimate line will be non-chargeable and will not add up to the contracted value of the contract line.</span></span>

<span data-ttu-id="2b629-116">Если в строке контракта есть сведения о строке, поля **Сумма контракта** и **Оценка налога** в строке контракта суммируются и не могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="2b629-116">When a contract line has line details, the **Contract Value** and **Estimated Tax** fields on the contract line are summarized and can't be edited.</span></span>

<span data-ttu-id="2b629-117">Когда выбрано несколько параметров суммирования, система пытается выполнить суммирование по всем из выбранных параметров.</span><span class="sxs-lookup"><span data-stu-id="2b629-117">When multiple summarization options are selected, the system attempts to summarize by all of the selected options.</span></span> <span data-ttu-id="2b629-118">Выходные данные суммирования приводят к большему количеству импортированных строк контракта, чем если бы вы выбрали только один параметр суммирования.</span><span class="sxs-lookup"><span data-stu-id="2b629-118">The summarization output results in more imported contract lines than if you select only one summarization option.</span></span>

<span data-ttu-id="2b629-119">Например, если в проекте есть следующие строки оценки для расходов:</span><span class="sxs-lookup"><span data-stu-id="2b629-119">For example, if the project has the following estimate lines for expenses:</span></span>

| <span data-ttu-id="2b629-120">Задача</span><span class="sxs-lookup"><span data-stu-id="2b629-120">Task</span></span> | <span data-ttu-id="2b629-121">Категории</span><span class="sxs-lookup"><span data-stu-id="2b629-121">Category</span></span> | <span data-ttu-id="2b629-122">Дата</span><span class="sxs-lookup"><span data-stu-id="2b629-122">Date</span></span> | <span data-ttu-id="2b629-123">Количество</span><span class="sxs-lookup"><span data-stu-id="2b629-123">Quantity</span></span> | <span data-ttu-id="2b629-124">Цена за единицу</span><span class="sxs-lookup"><span data-stu-id="2b629-124">Unit price</span></span> | <span data-ttu-id="2b629-125">Сумма</span><span class="sxs-lookup"><span data-stu-id="2b629-125">Amount</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="2b629-126">Задача A</span><span class="sxs-lookup"><span data-stu-id="2b629-126">Task A</span></span> | <span data-ttu-id="2b629-127">Стоимость авиабилета</span><span class="sxs-lookup"><span data-stu-id="2b629-127">Airfare</span></span> | <span data-ttu-id="2b629-128">01.10.2020</span><span class="sxs-lookup"><span data-stu-id="2b629-128">10/1/2020</span></span> | <span data-ttu-id="2b629-129">4</span><span class="sxs-lookup"><span data-stu-id="2b629-129">4</span></span> | <span data-ttu-id="2b629-130">400</span><span class="sxs-lookup"><span data-stu-id="2b629-130">400</span></span> | <span data-ttu-id="2b629-131">1600</span><span class="sxs-lookup"><span data-stu-id="2b629-131">1600</span></span> |
| <span data-ttu-id="2b629-132">Задача B</span><span class="sxs-lookup"><span data-stu-id="2b629-132">Task B</span></span> | <span data-ttu-id="2b629-133">Отель</span><span class="sxs-lookup"><span data-stu-id="2b629-133">Hotel</span></span> | <span data-ttu-id="2b629-134">01.10.2020</span><span class="sxs-lookup"><span data-stu-id="2b629-134">10/1/2020</span></span> | <span data-ttu-id="2b629-135">4</span><span class="sxs-lookup"><span data-stu-id="2b629-135">4</span></span> | <span data-ttu-id="2b629-136">200</span><span class="sxs-lookup"><span data-stu-id="2b629-136">200</span></span> | <span data-ttu-id="2b629-137">800</span><span class="sxs-lookup"><span data-stu-id="2b629-137">800</span></span> |
| <span data-ttu-id="2b629-138">Задача C</span><span class="sxs-lookup"><span data-stu-id="2b629-138">Task C</span></span> | <span data-ttu-id="2b629-139">Отель</span><span class="sxs-lookup"><span data-stu-id="2b629-139">Hotel</span></span> | <span data-ttu-id="2b629-140">01.11.2020</span><span class="sxs-lookup"><span data-stu-id="2b629-140">11/1/2020</span></span> | <span data-ttu-id="2b629-141">2</span><span class="sxs-lookup"><span data-stu-id="2b629-141">2</span></span> | <span data-ttu-id="2b629-142">200</span><span class="sxs-lookup"><span data-stu-id="2b629-142">200</span></span> | <span data-ttu-id="2b629-143">400</span><span class="sxs-lookup"><span data-stu-id="2b629-143">400</span></span> |

<span data-ttu-id="2b629-144">Когда пользователь выбирает суммирование по параметру **Класс транзакции**, будет импортирована следующая информация:</span><span class="sxs-lookup"><span data-stu-id="2b629-144">When the user selects to summarize by **Transaction Class**, the following information will be imported:</span></span>

| <span data-ttu-id="2b629-145">Задача</span><span class="sxs-lookup"><span data-stu-id="2b629-145">Task</span></span> | <span data-ttu-id="2b629-146">Категории</span><span class="sxs-lookup"><span data-stu-id="2b629-146">Category</span></span> | <span data-ttu-id="2b629-147">Дата</span><span class="sxs-lookup"><span data-stu-id="2b629-147">Date</span></span> | <span data-ttu-id="2b629-148">Количество</span><span class="sxs-lookup"><span data-stu-id="2b629-148">Quantity</span></span> | <span data-ttu-id="2b629-149">Цена за единицу</span><span class="sxs-lookup"><span data-stu-id="2b629-149">Unit price</span></span> | <span data-ttu-id="2b629-150">Сумма</span><span class="sxs-lookup"><span data-stu-id="2b629-150">Amount</span></span> |
| --- | --- | --- | --- | --- | --- |
| &nbsp; | &nbsp; | <span data-ttu-id="2b629-151">01.10.2020</span><span class="sxs-lookup"><span data-stu-id="2b629-151">10/1/2020</span></span> | <span data-ttu-id="2b629-152">3.34</span><span class="sxs-lookup"><span data-stu-id="2b629-152">3.34</span></span> | <span data-ttu-id="2b629-153">840</span><span class="sxs-lookup"><span data-stu-id="2b629-153">840</span></span> | <span data-ttu-id="2b629-154">2800</span><span class="sxs-lookup"><span data-stu-id="2b629-154">2800</span></span> |

<span data-ttu-id="2b629-155">Когда пользователь выбирает суммирование по параметрам **Класс транзакции** и **Категория**, будет импортирована следующая информация:</span><span class="sxs-lookup"><span data-stu-id="2b629-155">When the user selects to summarize by **Transaction Class** and **Category**, the following information will be imported:</span></span>

| <span data-ttu-id="2b629-156">Задача</span><span class="sxs-lookup"><span data-stu-id="2b629-156">Task</span></span> | <span data-ttu-id="2b629-157">Категории</span><span class="sxs-lookup"><span data-stu-id="2b629-157">Category</span></span> | <span data-ttu-id="2b629-158">Дата</span><span class="sxs-lookup"><span data-stu-id="2b629-158">Date</span></span> | <span data-ttu-id="2b629-159">Количество</span><span class="sxs-lookup"><span data-stu-id="2b629-159">Quantity</span></span> | <span data-ttu-id="2b629-160">Цена за единицу</span><span class="sxs-lookup"><span data-stu-id="2b629-160">Unit price</span></span> | <span data-ttu-id="2b629-161">Сумма</span><span class="sxs-lookup"><span data-stu-id="2b629-161">Amount</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="2b629-162">Задача A</span><span class="sxs-lookup"><span data-stu-id="2b629-162">Task A</span></span> | <span data-ttu-id="2b629-163">Стоимость авиабилета</span><span class="sxs-lookup"><span data-stu-id="2b629-163">Airfare</span></span> | <span data-ttu-id="2b629-164">01.10.2020</span><span class="sxs-lookup"><span data-stu-id="2b629-164">10/1/2020</span></span> | <span data-ttu-id="2b629-165">4</span><span class="sxs-lookup"><span data-stu-id="2b629-165">4</span></span> | <span data-ttu-id="2b629-166">400</span><span class="sxs-lookup"><span data-stu-id="2b629-166">400</span></span> | <span data-ttu-id="2b629-167">1600</span><span class="sxs-lookup"><span data-stu-id="2b629-167">1600</span></span> |
| &nbsp;| <span data-ttu-id="2b629-168">Отель</span><span class="sxs-lookup"><span data-stu-id="2b629-168">Hotel</span></span> | <span data-ttu-id="2b629-169">01.10.2020</span><span class="sxs-lookup"><span data-stu-id="2b629-169">10/1/2020</span></span> | <span data-ttu-id="2b629-170">6</span><span class="sxs-lookup"><span data-stu-id="2b629-170">6</span></span> | <span data-ttu-id="2b629-171">200</span><span class="sxs-lookup"><span data-stu-id="2b629-171">200</span></span> | <span data-ttu-id="2b629-172">1200</span><span class="sxs-lookup"><span data-stu-id="2b629-172">1200</span></span> |

<span data-ttu-id="2b629-173">Когда пользователь выбирает суммирование по параметрам **Класс транзакции**, **Категория** и **Задача листового узла**, будет импортирована следующая информация.</span><span class="sxs-lookup"><span data-stu-id="2b629-173">When the user selects to summarize by **Transaction Class**, **Category**, and **Leaf Node Task**, the following will be imported.</span></span> <span data-ttu-id="2b629-174">Обратите внимание, что этот результат такой же, как и в проекте:</span><span class="sxs-lookup"><span data-stu-id="2b629-174">Notice that this result is the same as what is on the project:</span></span>

| <span data-ttu-id="2b629-175">Задача</span><span class="sxs-lookup"><span data-stu-id="2b629-175">Task</span></span> | <span data-ttu-id="2b629-176">Категории</span><span class="sxs-lookup"><span data-stu-id="2b629-176">Category</span></span> | <span data-ttu-id="2b629-177">Дата</span><span class="sxs-lookup"><span data-stu-id="2b629-177">Date</span></span> | <span data-ttu-id="2b629-178">Количество</span><span class="sxs-lookup"><span data-stu-id="2b629-178">Quantity</span></span> | <span data-ttu-id="2b629-179">Цена за единицу</span><span class="sxs-lookup"><span data-stu-id="2b629-179">Unit price</span></span> | <span data-ttu-id="2b629-180">Сумма</span><span class="sxs-lookup"><span data-stu-id="2b629-180">Amount</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="2b629-181">Задача A</span><span class="sxs-lookup"><span data-stu-id="2b629-181">Task A</span></span> | <span data-ttu-id="2b629-182">Стоимость авиабилета</span><span class="sxs-lookup"><span data-stu-id="2b629-182">Airfare</span></span> | <span data-ttu-id="2b629-183">01.10.2020</span><span class="sxs-lookup"><span data-stu-id="2b629-183">10/1/2020</span></span> | <span data-ttu-id="2b629-184">4</span><span class="sxs-lookup"><span data-stu-id="2b629-184">4</span></span> | <span data-ttu-id="2b629-185">400</span><span class="sxs-lookup"><span data-stu-id="2b629-185">400</span></span> | <span data-ttu-id="2b629-186">1600</span><span class="sxs-lookup"><span data-stu-id="2b629-186">1600</span></span> |
| <span data-ttu-id="2b629-187">Задача B</span><span class="sxs-lookup"><span data-stu-id="2b629-187">Task B</span></span> | <span data-ttu-id="2b629-188">Отель</span><span class="sxs-lookup"><span data-stu-id="2b629-188">Hotel</span></span> | <span data-ttu-id="2b629-189">01.10.2020</span><span class="sxs-lookup"><span data-stu-id="2b629-189">10/1/2020</span></span> | <span data-ttu-id="2b629-190">4</span><span class="sxs-lookup"><span data-stu-id="2b629-190">4</span></span> | <span data-ttu-id="2b629-191">200</span><span class="sxs-lookup"><span data-stu-id="2b629-191">200</span></span> | <span data-ttu-id="2b629-192">800</span><span class="sxs-lookup"><span data-stu-id="2b629-192">800</span></span> |
| <span data-ttu-id="2b629-193">Задача C</span><span class="sxs-lookup"><span data-stu-id="2b629-193">Task C</span></span> | <span data-ttu-id="2b629-194">Отель</span><span class="sxs-lookup"><span data-stu-id="2b629-194">Hotel</span></span> | <span data-ttu-id="2b629-195">01.11.2020</span><span class="sxs-lookup"><span data-stu-id="2b629-195">11/1/2020</span></span> | <span data-ttu-id="2b629-196">2</span><span class="sxs-lookup"><span data-stu-id="2b629-196">2</span></span> | <span data-ttu-id="2b629-197">200</span><span class="sxs-lookup"><span data-stu-id="2b629-197">200</span></span> | <span data-ttu-id="2b629-198">400</span><span class="sxs-lookup"><span data-stu-id="2b629-198">400</span></span> |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]