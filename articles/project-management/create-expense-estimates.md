---
title: Оценки расходов
description: Эта тема предоставляет информацию об определении или оценке расходов на основе проекта.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3f0429366c69346113003355679c055cd2c74ca3
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287074"
---
# <a name="expense-estimates"></a><span data-ttu-id="9c07f-103">Оценки расходов</span><span class="sxs-lookup"><span data-stu-id="9c07f-103">Expense estimates</span></span>
<span data-ttu-id="9c07f-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="9c07f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9c07f-105">Наряду с определением оценок на основе ресурсов Dynamics 365 Project Operations позволяет менеджерам проектов определять расходы по каждому проекту.</span><span class="sxs-lookup"><span data-stu-id="9c07f-105">Along with defining resource-based estimates, Dynamics 365 Project Operations allows Project managers to define project-based expenses for each project.</span></span> <span data-ttu-id="9c07f-106">Каждая статья расходов может быть связана с определенной задачей проекта или категорией расходов.</span><span class="sxs-lookup"><span data-stu-id="9c07f-106">Each expense item can be associated with a specific project task or expense category.</span></span> <span data-ttu-id="9c07f-107">Категории расходов обычно определяются на организационном уровне.</span><span class="sxs-lookup"><span data-stu-id="9c07f-107">Expense categories are typically defined at the organizational level.</span></span> <span data-ttu-id="9c07f-108">Цена для каждой категории расходов обычно определяется в следующей иерархии:</span><span class="sxs-lookup"><span data-stu-id="9c07f-108">Pricing for each expense category is typically defined in the following hierarchy:</span></span>

- <span data-ttu-id="9c07f-109">Предприятие</span><span class="sxs-lookup"><span data-stu-id="9c07f-109">Organization</span></span>
- <span data-ttu-id="9c07f-110">Клиент</span><span class="sxs-lookup"><span data-stu-id="9c07f-110">Customer</span></span>
- <span data-ttu-id="9c07f-111">Предложение с расценками/контракт</span><span class="sxs-lookup"><span data-stu-id="9c07f-111">Quote/contract</span></span>

<span data-ttu-id="9c07f-112">Выполните следующие шаги, чтобы просмотреть, добавить или удалить расходы по проекту.</span><span class="sxs-lookup"><span data-stu-id="9c07f-112">Complete the following steps to view, add, or delete a project expense.</span></span>

1. <span data-ttu-id="9c07f-113">Перейдите к пункту **Проекты** и выберите проект, над которым хотите работать.</span><span class="sxs-lookup"><span data-stu-id="9c07f-113">Go to **Projects**, and select the project you want to work on.</span></span>
2. <span data-ttu-id="9c07f-114">Выберите вкладку **Оценка проекта** и просмотрите список расходов по проекту.</span><span class="sxs-lookup"><span data-stu-id="9c07f-114">Select the **Project Estimates** tab and view the list of project expenses.</span></span>
3. <span data-ttu-id="9c07f-115">Выберите **Создать расход**, чтобы добавить расход.</span><span class="sxs-lookup"><span data-stu-id="9c07f-115">Select **New Expense** to add an expense.</span></span> <span data-ttu-id="9c07f-116">Или выберите расход, который нужно удалить, затем выберите **Удалить расход**.</span><span class="sxs-lookup"><span data-stu-id="9c07f-116">Or, select an expense to delete, and then select **Delete Expense**.</span></span>

<span data-ttu-id="9c07f-117">Для каждой статьи строки расходов определены следующие атрибуты:</span><span class="sxs-lookup"><span data-stu-id="9c07f-117">The following attributes are defined for each expense line item:</span></span>

- <span data-ttu-id="9c07f-118">**Категория**: общие группы, используемые для описания всех расходов, понесенных по проекту.</span><span class="sxs-lookup"><span data-stu-id="9c07f-118">**Category**: The common groupings used to describe all expenses incurred on a project.</span></span>
- <span data-ttu-id="9c07f-119">**Дата начала**: дата, когда предполагается понести расходы.</span><span class="sxs-lookup"><span data-stu-id="9c07f-119">**Start Date**: The date when the expense is forecasted to be incurred.</span></span>
- <span data-ttu-id="9c07f-120">**Количество**: примерное количество статей расходов для определенной категории.</span><span class="sxs-lookup"><span data-stu-id="9c07f-120">**Quantity**: The estimated number of expense items for a specific category.</span></span>
- <span data-ttu-id="9c07f-121">**Себестоимость единицы**: цена за единицу, используемая для расчета стоимости расхода.</span><span class="sxs-lookup"><span data-stu-id="9c07f-121">**Unit Cost Price**: The unit price used to calculate to cost of the expense.</span></span>
- <span data-ttu-id="9c07f-122">**Цена продажи ед. изм.**: цена за единицу, используемая для расчета цены продажи.</span><span class="sxs-lookup"><span data-stu-id="9c07f-122">**Unit Sales Price**: The unit price used to calculate the sale prices of the expense.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]