---
title: Оценки расходов
description: Эта тема предоставляет информацию об определении или оценке расходов на основе проекта.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2afe4ff2f84fc5426c409e6314da73b11a4de281
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083110"
---
# <a name="expense-estimates"></a><span data-ttu-id="adfec-103">Оценки расходов</span><span class="sxs-lookup"><span data-stu-id="adfec-103">Expense estimates</span></span>
<span data-ttu-id="adfec-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="adfec-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="adfec-105">Помимо определения оценок на основе ресурсов, Dynamics 365 Project Operations позволяет руководителям проектов определять расходы на основе проектов для каждого проекта.</span><span class="sxs-lookup"><span data-stu-id="adfec-105">Along with defining resource-based estimates, Dynamics 365 Project Operations allows Project managers to define project-based expenses for each project.</span></span> <span data-ttu-id="adfec-106">Каждая статья расходов может быть связана с определенной задачей проекта или категорией расходов.</span><span class="sxs-lookup"><span data-stu-id="adfec-106">Each expense item can be associated with a specific project task or expense category.</span></span> <span data-ttu-id="adfec-107">Категории расходов обычно определяются на организационном уровне.</span><span class="sxs-lookup"><span data-stu-id="adfec-107">Expense categories are typically defined at the organizational level.</span></span> <span data-ttu-id="adfec-108">Цена для каждой категории расходов обычно определяется в следующей иерархии:</span><span class="sxs-lookup"><span data-stu-id="adfec-108">Pricing for each expense category is typically defined in the following hierarchy:</span></span>

- <span data-ttu-id="adfec-109">Предприятие</span><span class="sxs-lookup"><span data-stu-id="adfec-109">Organization</span></span>
- <span data-ttu-id="adfec-110">Клиент</span><span class="sxs-lookup"><span data-stu-id="adfec-110">Customer</span></span>
- <span data-ttu-id="adfec-111">Предложение с расценками/контракт</span><span class="sxs-lookup"><span data-stu-id="adfec-111">Quote/contract</span></span>

<span data-ttu-id="adfec-112">Выполните следующие шаги, чтобы просмотреть, добавить или удалить расходы по проекту.</span><span class="sxs-lookup"><span data-stu-id="adfec-112">Complete the following steps to view, add, or delete a project expense.</span></span>

1. <span data-ttu-id="adfec-113">Перейдите к пункту **Проекты** и выберите проект, над которым хотите работать.</span><span class="sxs-lookup"><span data-stu-id="adfec-113">Go to **Projects** , and select the project you want to work on.</span></span>
2. <span data-ttu-id="adfec-114">Выберите вкладку **Оценка проекта** и просмотрите список расходов по проекту.</span><span class="sxs-lookup"><span data-stu-id="adfec-114">Select the **Project Estimates** tab and view the list of project expenses.</span></span>
3. <span data-ttu-id="adfec-115">Выберите **Создать расход** , чтобы добавить расход.</span><span class="sxs-lookup"><span data-stu-id="adfec-115">Select **New Expense** to add an expense.</span></span> <span data-ttu-id="adfec-116">Или выберите расход, который нужно удалить, затем выберите **Удалить расход**.</span><span class="sxs-lookup"><span data-stu-id="adfec-116">Or, select an expense to delete, and then select **Delete Expense**.</span></span>

<span data-ttu-id="adfec-117">Для каждой статьи строки расходов определены следующие атрибуты:</span><span class="sxs-lookup"><span data-stu-id="adfec-117">The following attributes are defined for each expense line item:</span></span>

- <span data-ttu-id="adfec-118">**Категория** : общие группы, используемые для описания всех расходов, понесенных по проекту.</span><span class="sxs-lookup"><span data-stu-id="adfec-118">**Category** : The common groupings used to describe all expenses incurred on a project.</span></span>
- <span data-ttu-id="adfec-119">**Дата начала** : дата, когда предполагается понести расходы.</span><span class="sxs-lookup"><span data-stu-id="adfec-119">**Start Date** : The date when the expense is forecasted to be incurred.</span></span>
- <span data-ttu-id="adfec-120">**Количество** : примерное количество статей расходов для определенной категории.</span><span class="sxs-lookup"><span data-stu-id="adfec-120">**Quantity** : The estimated number of expense items for a specific category.</span></span>
- <span data-ttu-id="adfec-121">**Себестоимость единицы** : цена за единицу, используемая для расчета стоимости расхода.</span><span class="sxs-lookup"><span data-stu-id="adfec-121">**Unit Cost Price** : The unit price used to calculate to cost of the expense.</span></span>
- <span data-ttu-id="adfec-122">**Цена продажи ед. изм.** : цена за единицу, используемая для расчета цены продажи.</span><span class="sxs-lookup"><span data-stu-id="adfec-122">**Unit Sales Price** : The unit price used to calculate the sale prices of the expense.</span></span>

