---
title: Анализ предложений с расценками по проекту
description: В этом разделе представлена информация об анализе предложений с расценками по проекту.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 6ed900620f92e76d293f6b533b101be94b25cff3
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127039"
---
# <a name="analysis-of-project-quotes"></a><span data-ttu-id="15f8c-103">Анализ предложений с расценками по проекту</span><span class="sxs-lookup"><span data-stu-id="15f8c-103">Analysis of project quotes</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="15f8c-104">Dynamics 365 Project Service Automation анализирует предложения с расценками по проекту для оценки прибыльности.</span><span class="sxs-lookup"><span data-stu-id="15f8c-104">Dynamics 365 Project Service Automation analyzes project quotes to estimate profitability.</span></span> <span data-ttu-id="15f8c-105">Он также анализирует, насколько хорошо предложение с расценками соответствует ожиданиям клиента с точки зрения даты доставки или даты завершения, а также в отношении бюджета.</span><span class="sxs-lookup"><span data-stu-id="15f8c-105">It also analyzes how well the quote is aligned with customer expectations about the delivery date or completion date, and about the budget.tions.</span></span>

## <a name="profitability-analysis"></a><span data-ttu-id="15f8c-106">Анализ прибыльности</span><span class="sxs-lookup"><span data-stu-id="15f8c-106">Profitability analysis</span></span>

<span data-ttu-id="15f8c-107">Project Service Automation анализирует доходность, используя валовую прибыль и скорректированную валовую прибыль.</span><span class="sxs-lookup"><span data-stu-id="15f8c-107">Project Service Automation analyzes profitability by using the gross margin and the adjusted gross margin.</span></span>

- <span data-ttu-id="15f8c-108">Значения валовой прибыли вычисляются с помощью следующей формулы:</span><span class="sxs-lookup"><span data-stu-id="15f8c-108">Gross margins are calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- <span data-ttu-id="15f8c-109">Скорректированная валовая прибыль вычисляется с помощью следующей формулы:</span><span class="sxs-lookup"><span data-stu-id="15f8c-109">The adjusted gross margin is calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

<span data-ttu-id="15f8c-110">Если значения валовой прибыли и скорректированной валовой прибыли значительно отличаются, большая часть работы в предложении с расценками классифицируется как неоплачиваемая.</span><span class="sxs-lookup"><span data-stu-id="15f8c-110">If the values for gross margin and adjusted gross margin differ by a wide margin, much of the work in the quote is classified as non-chargeable.</span></span>

## <a name="analysis-of-customer-expectations"></a><span data-ttu-id="15f8c-111">Анализ ожиданий клиента</span><span class="sxs-lookup"><span data-stu-id="15f8c-111">Analysis of customer expectations</span></span>

<span data-ttu-id="15f8c-112">Можно анализировать предложения с расценками и создать диаграммы для ожиданий клиентов по расписанию и бюджету, если ввести значения в следующие поля:</span><span class="sxs-lookup"><span data-stu-id="15f8c-112">You can analyze quotes and generate charts for customer expectations about the schedule and budget if you enter values for the following fields:</span></span>

- <span data-ttu-id="15f8c-113">Поле **Требуемая дата поставки** в заголовке предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="15f8c-113">The **Requested delivery date** field on the quote header.</span></span>
- <span data-ttu-id="15f8c-114">Поле **Бюджет клиента** для каждой строки предложения с расценками (для строк на основе проекта и строк на основе продукта).</span><span class="sxs-lookup"><span data-stu-id="15f8c-114">The **Customer budget** field for each quote line (for project-based lines and product-based lines).</span></span>

<span data-ttu-id="15f8c-115">Анализ ожиданий клиентов относительно расписания выполняется путем сравнения последней даты окончания сведений строки предложения с расценками с требуемой датой поставки по всем строкам предложения с расценками в предложении.</span><span class="sxs-lookup"><span data-stu-id="15f8c-115">Analysis of customer expectations about the schedule is done by comparing the latest end date of the quote line detail with the requested delivery date across all quote lines in the quote.</span></span>

<span data-ttu-id="15f8c-116">Анализ ожиданий клиента о бюджете выполняется путем сравнения суммы общего бюджета клиента с суммой из предложения с расценками по всем строкам этого предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="15f8c-116">Analysis of customer expectations about the budget is done by comparing the sum of the total customer budget with the quoted amount across all quote lines.</span></span>
