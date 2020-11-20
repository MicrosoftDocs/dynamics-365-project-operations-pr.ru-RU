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
ms.openlocfilehash: 10872366453985561bda0c07e50cff7f5f6d333e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131719"
---
# <a name="expense-estimates"></a><span data-ttu-id="dfdb1-103">Оценки расходов</span><span class="sxs-lookup"><span data-stu-id="dfdb1-103">Expense estimates</span></span>
<span data-ttu-id="dfdb1-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="dfdb1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="dfdb1-105">Помимо определения оценок на основе ресурсов, Dynamics 365 Project Operations позволяет руководителям проектов определять расходы на основе проектов для каждого проекта.</span><span class="sxs-lookup"><span data-stu-id="dfdb1-105">Along with defining resource-based estimates, Dynamics 365 Project Operations allows Project managers to define project-based expenses for each project.</span></span> <span data-ttu-id="dfdb1-106">Каждая статья расходов может быть связана с определенной задачей проекта или категорией расходов.</span><span class="sxs-lookup"><span data-stu-id="dfdb1-106">Each expense item can be associated with a specific project task or expense category.</span></span> <span data-ttu-id="dfdb1-107">Категории расходов обычно определяются на организационном уровне.</span><span class="sxs-lookup"><span data-stu-id="dfdb1-107">Expense categories are typically defined at the organizational level.</span></span> <span data-ttu-id="dfdb1-108">Цена для каждой категории расходов обычно определяется в следующей иерархии:</span><span class="sxs-lookup"><span data-stu-id="dfdb1-108">Pricing for each expense category is typically defined in the following hierarchy:</span></span>

- <span data-ttu-id="dfdb1-109">Предприятие</span><span class="sxs-lookup"><span data-stu-id="dfdb1-109">Organization</span></span>
- <span data-ttu-id="dfdb1-110">Клиент</span><span class="sxs-lookup"><span data-stu-id="dfdb1-110">Customer</span></span>
- <span data-ttu-id="dfdb1-111">Предложение с расценками/контракт</span><span class="sxs-lookup"><span data-stu-id="dfdb1-111">Quote/contract</span></span>

<span data-ttu-id="dfdb1-112">Выполните следующие шаги, чтобы просмотреть, добавить или удалить расходы по проекту.</span><span class="sxs-lookup"><span data-stu-id="dfdb1-112">Complete the following steps to view, add, or delete a project expense.</span></span>

1. <span data-ttu-id="dfdb1-113">Перейдите к пункту **Проекты** и выберите проект, над которым хотите работать.</span><span class="sxs-lookup"><span data-stu-id="dfdb1-113">Go to **Projects**, and select the project you want to work on.</span></span>
2. <span data-ttu-id="dfdb1-114">Выберите вкладку **Оценка проекта** и просмотрите список расходов по проекту.</span><span class="sxs-lookup"><span data-stu-id="dfdb1-114">Select the **Project Estimates** tab and view the list of project expenses.</span></span>
3. <span data-ttu-id="dfdb1-115">Выберите **Создать расход**, чтобы добавить расход.</span><span class="sxs-lookup"><span data-stu-id="dfdb1-115">Select **New Expense** to add an expense.</span></span> <span data-ttu-id="dfdb1-116">Или выберите расход, который нужно удалить, затем выберите **Удалить расход**.</span><span class="sxs-lookup"><span data-stu-id="dfdb1-116">Or, select an expense to delete, and then select **Delete Expense**.</span></span>

<span data-ttu-id="dfdb1-117">Для каждой статьи строки расходов определены следующие атрибуты:</span><span class="sxs-lookup"><span data-stu-id="dfdb1-117">The following attributes are defined for each expense line item:</span></span>

- <span data-ttu-id="dfdb1-118">**Категория**: общие группы, используемые для описания всех расходов, понесенных по проекту.</span><span class="sxs-lookup"><span data-stu-id="dfdb1-118">**Category**: The common groupings used to describe all expenses incurred on a project.</span></span>
- <span data-ttu-id="dfdb1-119">**Дата начала**: дата, когда предполагается понести расходы.</span><span class="sxs-lookup"><span data-stu-id="dfdb1-119">**Start Date**: The date when the expense is forecasted to be incurred.</span></span>
- <span data-ttu-id="dfdb1-120">**Количество**: примерное количество статей расходов для определенной категории.</span><span class="sxs-lookup"><span data-stu-id="dfdb1-120">**Quantity**: The estimated number of expense items for a specific category.</span></span>
- <span data-ttu-id="dfdb1-121">**Себестоимость единицы**: цена за единицу, используемая для расчета стоимости расхода.</span><span class="sxs-lookup"><span data-stu-id="dfdb1-121">**Unit Cost Price**: The unit price used to calculate to cost of the expense.</span></span>
- <span data-ttu-id="dfdb1-122">**Цена продажи ед. изм.**: цена за единицу, используемая для расчета цены продажи.</span><span class="sxs-lookup"><span data-stu-id="dfdb1-122">**Unit Sales Price**: The unit price used to calculate the sale prices of the expense.</span></span>

