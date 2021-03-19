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
ms.openlocfilehash: 5e77a0442f634a50f8099fadec42ff400fee0e81
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278884"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="08054-103">Обзор признания дохода</span><span class="sxs-lookup"><span data-stu-id="08054-103">Revenue recognition overview</span></span>

<span data-ttu-id="08054-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/без запасов_</span><span class="sxs-lookup"><span data-stu-id="08054-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="08054-105">В Dynamics 365 Project Operations принципы признание дохода различаются в зависимости от выбранного метода выставления счетов для проекта или части проекта.</span><span class="sxs-lookup"><span data-stu-id="08054-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="08054-106">В этом разделе представлена информация о признание дохода в Project Operations.</span><span class="sxs-lookup"><span data-stu-id="08054-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="08054-107">Транзакции учитываются с использованием метода выставления счетов по времени и материалам</span><span class="sxs-lookup"><span data-stu-id="08054-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="08054-108">Признание затрат и доходов взаимосвязаны.</span><span class="sxs-lookup"><span data-stu-id="08054-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="08054-109">Стоимость транзакции и продажи без выставления счетов разносятся с использованием [Журнала интеграции Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="08054-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="08054-110">Профиль затрат и доходов по проекту определяет, будут ли транзакции продаж без выставления счета разноситься в главную книгу.</span><span class="sxs-lookup"><span data-stu-id="08054-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="08054-111">Если выбрано **Начислить доход**, система использует учетные записи **Объем продаж НЗП** и **Значение начисленного дохода от продаж** во время разноски.</span><span class="sxs-lookup"><span data-stu-id="08054-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="08054-112">Ниже показан пример этого метода.</span><span class="sxs-lookup"><span data-stu-id="08054-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="08054-113">Тип проводки</span><span class="sxs-lookup"><span data-stu-id="08054-113">Transaction type</span></span> | <span data-ttu-id="08054-114">Дебет/Кредит</span><span class="sxs-lookup"><span data-stu-id="08054-114">Debit/Credit</span></span> | <span data-ttu-id="08054-115">Сумма</span><span class="sxs-lookup"><span data-stu-id="08054-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="08054-116">Объем продаж НЗП</span><span class="sxs-lookup"><span data-stu-id="08054-116">WIP Sales value</span></span> | <span data-ttu-id="08054-117">Дебет</span><span class="sxs-lookup"><span data-stu-id="08054-117">Debit</span></span> | <span data-ttu-id="08054-118">100</span><span class="sxs-lookup"><span data-stu-id="08054-118">100</span></span> |
  | <span data-ttu-id="08054-119">Значение начисленного дохода от продаж</span><span class="sxs-lookup"><span data-stu-id="08054-119">Accrued revenue sales value</span></span> | <span data-ttu-id="08054-120">Кредит</span><span class="sxs-lookup"><span data-stu-id="08054-120">Credit</span></span> | <span data-ttu-id="08054-121">100</span><span class="sxs-lookup"><span data-stu-id="08054-121">100</span></span> |

- <span data-ttu-id="08054-122">Доход признан во время выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="08054-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="08054-123">Система использует учетную запись **Доход, по которому выставлен счет** во время разноски.</span><span class="sxs-lookup"><span data-stu-id="08054-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="08054-124">Ниже показан пример этого метода.</span><span class="sxs-lookup"><span data-stu-id="08054-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="08054-125">Тип проводки</span><span class="sxs-lookup"><span data-stu-id="08054-125">Transaction type</span></span> | <span data-ttu-id="08054-126">Дебет/Кредит</span><span class="sxs-lookup"><span data-stu-id="08054-126">Debit/Credit</span></span> | <span data-ttu-id="08054-127">Сумма</span><span class="sxs-lookup"><span data-stu-id="08054-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="08054-128">Остаток на счете клиента</span><span class="sxs-lookup"><span data-stu-id="08054-128">Customer balance</span></span> | <span data-ttu-id="08054-129">Дебет</span><span class="sxs-lookup"><span data-stu-id="08054-129">Debit</span></span> | <span data-ttu-id="08054-130">120</span><span class="sxs-lookup"><span data-stu-id="08054-130">120</span></span> |
  | <span data-ttu-id="08054-131">Налог с продаж к оплате</span><span class="sxs-lookup"><span data-stu-id="08054-131">Sales tax payable</span></span> | <span data-ttu-id="08054-132">Кредит</span><span class="sxs-lookup"><span data-stu-id="08054-132">Credit</span></span> | <span data-ttu-id="08054-133">20</span><span class="sxs-lookup"><span data-stu-id="08054-133">20</span></span> |
  | <span data-ttu-id="08054-134">Доход, по которому выставлен счет</span><span class="sxs-lookup"><span data-stu-id="08054-134">Invoiced Revenue</span></span> | <span data-ttu-id="08054-135">Кредит</span><span class="sxs-lookup"><span data-stu-id="08054-135">Credit</span></span> | <span data-ttu-id="08054-136">100</span><span class="sxs-lookup"><span data-stu-id="08054-136">100</span></span> |

- <span data-ttu-id="08054-137">Если доход был начислен при разноске продаж без выставления счета, система сторнирует начисленный доход при выставлении счета.</span><span class="sxs-lookup"><span data-stu-id="08054-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="08054-138">Тип проводки</span><span class="sxs-lookup"><span data-stu-id="08054-138">Transaction type</span></span> | <span data-ttu-id="08054-139">Дебет/Кредит</span><span class="sxs-lookup"><span data-stu-id="08054-139">Debit/Credit</span></span> | <span data-ttu-id="08054-140">Сумма</span><span class="sxs-lookup"><span data-stu-id="08054-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="08054-141">Объем продаж НЗП</span><span class="sxs-lookup"><span data-stu-id="08054-141">WIP Sales value</span></span> | <span data-ttu-id="08054-142">Кредит</span><span class="sxs-lookup"><span data-stu-id="08054-142">Credit</span></span> | <span data-ttu-id="08054-143">100</span><span class="sxs-lookup"><span data-stu-id="08054-143">100</span></span> |
  | <span data-ttu-id="08054-144">Значение начисленного дохода от продаж</span><span class="sxs-lookup"><span data-stu-id="08054-144">Accrued revenue sales value</span></span> | <span data-ttu-id="08054-145">Дебет</span><span class="sxs-lookup"><span data-stu-id="08054-145">Debit</span></span> | <span data-ttu-id="08054-146">100</span><span class="sxs-lookup"><span data-stu-id="08054-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="08054-147">Транзакции учитываются с использованием метода выставления счетов с фиксированной ценой</span><span class="sxs-lookup"><span data-stu-id="08054-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="08054-148">Признание затрат и доходов раздельные.</span><span class="sxs-lookup"><span data-stu-id="08054-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="08054-149">Стоимость транзакции разносится с использованием [Журнала интеграции Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="08054-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="08054-150">Транзакции продаж без выставления счета не создаются.</span><span class="sxs-lookup"><span data-stu-id="08054-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="08054-151">Доход может быть признан во время выставления счета, если в профиле затрат и доходов проекта **Принцип, используемый для расчетов завершения проекта** установлен на **Нет НЗП**.</span><span class="sxs-lookup"><span data-stu-id="08054-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="08054-152">Используйте этот метод только для краткосрочных простых проектов.</span><span class="sxs-lookup"><span data-stu-id="08054-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="08054-153">Доход может быть признан с использованием оценок дохода с фиксированной ценой, с помощью метода **Завершенный контракт** или **Признание дохода от завершения проекта**.</span><span class="sxs-lookup"><span data-stu-id="08054-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="08054-154">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="08054-154">Additional resources</span></span>
[<span data-ttu-id="08054-155">Статья Настройка учета для тарифицируемых проектов</span><span class="sxs-lookup"><span data-stu-id="08054-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="08054-156">Проекты оценки выручки с фиксированной ценой</span><span class="sxs-lookup"><span data-stu-id="08054-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="08054-157">Управление оценками выручки</span><span class="sxs-lookup"><span data-stu-id="08054-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="08054-158">Методы вычисления стоимости для завершения</span><span class="sxs-lookup"><span data-stu-id="08054-158">Cost to complete methods</span></span>](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]