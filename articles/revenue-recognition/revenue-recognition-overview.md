---
title: Обзор признания дохода
description: В этом разделе представлена информация о признание дохода в Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6844f4c5d4cda8a6a901b0302448f70f4c597f5d
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531530"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="fbe2f-103">Обзор признания дохода</span><span class="sxs-lookup"><span data-stu-id="fbe2f-103">Revenue recognition overview</span></span>

<span data-ttu-id="fbe2f-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/без запасов_</span><span class="sxs-lookup"><span data-stu-id="fbe2f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="fbe2f-105">В Dynamics 365 Project Operations принципы признание дохода различаются в зависимости от выбранного метода выставления счетов для проекта или части проекта.</span><span class="sxs-lookup"><span data-stu-id="fbe2f-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="fbe2f-106">В этом разделе представлена информация о признание дохода в Project Operations.</span><span class="sxs-lookup"><span data-stu-id="fbe2f-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="fbe2f-107">Транзакции учитываются с использованием метода выставления счетов по времени и материалам</span><span class="sxs-lookup"><span data-stu-id="fbe2f-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="fbe2f-108">Признание затрат и доходов взаимосвязаны.</span><span class="sxs-lookup"><span data-stu-id="fbe2f-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="fbe2f-109">Стоимость транзакции и продажи без выставления счетов разносятся с использованием [Журнала интеграции Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="fbe2f-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="fbe2f-110">Профиль затрат и доходов по проекту определяет, будут ли транзакции продаж без выставления счета разноситься в главную книгу.</span><span class="sxs-lookup"><span data-stu-id="fbe2f-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="fbe2f-111">Если выбрано **Начислить доход**, система использует учетные записи **Объем продаж НЗП** и **Значение начисленного дохода от продаж** во время разноски.</span><span class="sxs-lookup"><span data-stu-id="fbe2f-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="fbe2f-112">Ниже показан пример этого метода.</span><span class="sxs-lookup"><span data-stu-id="fbe2f-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="fbe2f-113">Тип проводки</span><span class="sxs-lookup"><span data-stu-id="fbe2f-113">Transaction type</span></span> | <span data-ttu-id="fbe2f-114">Дебет/Кредит</span><span class="sxs-lookup"><span data-stu-id="fbe2f-114">Debit/Credit</span></span> | <span data-ttu-id="fbe2f-115">Сумма</span><span class="sxs-lookup"><span data-stu-id="fbe2f-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="fbe2f-116">Объем продаж НЗП</span><span class="sxs-lookup"><span data-stu-id="fbe2f-116">WIP Sales value</span></span> | <span data-ttu-id="fbe2f-117">Дебет</span><span class="sxs-lookup"><span data-stu-id="fbe2f-117">Debit</span></span> | <span data-ttu-id="fbe2f-118">100</span><span class="sxs-lookup"><span data-stu-id="fbe2f-118">100</span></span> |
  | <span data-ttu-id="fbe2f-119">Значение начисленного дохода от продаж</span><span class="sxs-lookup"><span data-stu-id="fbe2f-119">Accrued revenue sales value</span></span> | <span data-ttu-id="fbe2f-120">Кредит</span><span class="sxs-lookup"><span data-stu-id="fbe2f-120">Credit</span></span> | <span data-ttu-id="fbe2f-121">100</span><span class="sxs-lookup"><span data-stu-id="fbe2f-121">100</span></span> |

- <span data-ttu-id="fbe2f-122">Доход признан во время выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="fbe2f-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="fbe2f-123">Система использует учетную запись **Доход, по которому выставлен счет** во время разноски.</span><span class="sxs-lookup"><span data-stu-id="fbe2f-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="fbe2f-124">Ниже показан пример этого метода.</span><span class="sxs-lookup"><span data-stu-id="fbe2f-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="fbe2f-125">Тип проводки</span><span class="sxs-lookup"><span data-stu-id="fbe2f-125">Transaction type</span></span> | <span data-ttu-id="fbe2f-126">Дебет/Кредит</span><span class="sxs-lookup"><span data-stu-id="fbe2f-126">Debit/Credit</span></span> | <span data-ttu-id="fbe2f-127">Сумма</span><span class="sxs-lookup"><span data-stu-id="fbe2f-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="fbe2f-128">Остаток на счете клиента</span><span class="sxs-lookup"><span data-stu-id="fbe2f-128">Customer balance</span></span> | <span data-ttu-id="fbe2f-129">Дебет</span><span class="sxs-lookup"><span data-stu-id="fbe2f-129">Debit</span></span> | <span data-ttu-id="fbe2f-130">120</span><span class="sxs-lookup"><span data-stu-id="fbe2f-130">120</span></span> |
  | <span data-ttu-id="fbe2f-131">Налог с продаж к оплате</span><span class="sxs-lookup"><span data-stu-id="fbe2f-131">Sales tax payable</span></span> | <span data-ttu-id="fbe2f-132">Кредит</span><span class="sxs-lookup"><span data-stu-id="fbe2f-132">Credit</span></span> | <span data-ttu-id="fbe2f-133">20</span><span class="sxs-lookup"><span data-stu-id="fbe2f-133">20</span></span> |
  | <span data-ttu-id="fbe2f-134">Доход, по которому выставлен счет</span><span class="sxs-lookup"><span data-stu-id="fbe2f-134">Invoiced Revenue</span></span> | <span data-ttu-id="fbe2f-135">Кредит</span><span class="sxs-lookup"><span data-stu-id="fbe2f-135">Credit</span></span> | <span data-ttu-id="fbe2f-136">100</span><span class="sxs-lookup"><span data-stu-id="fbe2f-136">100</span></span> |

- <span data-ttu-id="fbe2f-137">Если доход был начислен при разноске продаж без выставления счета, система сторнирует начисленный доход при выставлении счета.</span><span class="sxs-lookup"><span data-stu-id="fbe2f-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="fbe2f-138">Тип проводки</span><span class="sxs-lookup"><span data-stu-id="fbe2f-138">Transaction type</span></span> | <span data-ttu-id="fbe2f-139">Дебет/Кредит</span><span class="sxs-lookup"><span data-stu-id="fbe2f-139">Debit/Credit</span></span> | <span data-ttu-id="fbe2f-140">Сумма</span><span class="sxs-lookup"><span data-stu-id="fbe2f-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="fbe2f-141">Объем продаж НЗП</span><span class="sxs-lookup"><span data-stu-id="fbe2f-141">WIP Sales value</span></span> | <span data-ttu-id="fbe2f-142">Кредит</span><span class="sxs-lookup"><span data-stu-id="fbe2f-142">Credit</span></span> | <span data-ttu-id="fbe2f-143">100</span><span class="sxs-lookup"><span data-stu-id="fbe2f-143">100</span></span> |
  | <span data-ttu-id="fbe2f-144">Значение начисленного дохода от продаж</span><span class="sxs-lookup"><span data-stu-id="fbe2f-144">Accrued revenue sales value</span></span> | <span data-ttu-id="fbe2f-145">Дебет</span><span class="sxs-lookup"><span data-stu-id="fbe2f-145">Debit</span></span> | <span data-ttu-id="fbe2f-146">100</span><span class="sxs-lookup"><span data-stu-id="fbe2f-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="fbe2f-147">Транзакции учитываются с использованием метода выставления счетов с фиксированной ценой</span><span class="sxs-lookup"><span data-stu-id="fbe2f-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="fbe2f-148">Признание затрат и доходов раздельные.</span><span class="sxs-lookup"><span data-stu-id="fbe2f-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="fbe2f-149">Стоимость транзакции разносится с использованием [Журнала интеграции Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="fbe2f-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="fbe2f-150">Транзакции продаж без выставления счета не создаются.</span><span class="sxs-lookup"><span data-stu-id="fbe2f-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="fbe2f-151">Доход может быть признан во время выставления счета, если в профиле затрат и доходов проекта **Принцип, используемый для расчетов завершения проекта** установлен на **Нет НЗП**.</span><span class="sxs-lookup"><span data-stu-id="fbe2f-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="fbe2f-152">Используйте этот метод только для краткосрочных простых проектов.</span><span class="sxs-lookup"><span data-stu-id="fbe2f-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="fbe2f-153">Доход может быть признан с использованием оценок дохода с фиксированной ценой, с помощью метода **Завершенный контракт** или **Признание дохода от завершения проекта**.</span><span class="sxs-lookup"><span data-stu-id="fbe2f-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fbe2f-154">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="fbe2f-154">Additional resources</span></span>
[<span data-ttu-id="fbe2f-155">Статья Настройка учета для тарифицируемых проектов</span><span class="sxs-lookup"><span data-stu-id="fbe2f-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="fbe2f-156">Проекты оценки выручки с фиксированной ценой</span><span class="sxs-lookup"><span data-stu-id="fbe2f-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="fbe2f-157">Управление оценками выручки</span><span class="sxs-lookup"><span data-stu-id="fbe2f-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="fbe2f-158">Методы вычисления стоимости для завершения</span><span class="sxs-lookup"><span data-stu-id="fbe2f-158">Cost to complete methods</span></span>](cost-complete-methods.md)
