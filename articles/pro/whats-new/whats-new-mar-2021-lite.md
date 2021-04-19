---
title: Что нового в марте 2021 г. — облегченное развертывание Project Operations
description: Эта тема предоставляет информацию об обновлениях качества, доступных в облегченном развертывании Project Operations выпуска за март 2021 г.
author: sigitac
manager: tfehr
ms.date: 03/03/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: bd1518ef8f5645bace63a222b92cfd16d9c19a21
ms.sourcegitcommit: f78087174a8512199a1bcbd7e8610bbc80e64801
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500034"
---
# <a name="whats-new-march-2021---project-operations-lite-deployment"></a><span data-ttu-id="cfba0-103">Что нового в марте 2021 г. — облегченное развертывание Project Operations</span><span class="sxs-lookup"><span data-stu-id="cfba0-103">What's new March 2021 - Project Operations lite deployment</span></span>

<span data-ttu-id="cfba0-104">_Относится к: облегченное развертывание — от сделки до счетов-проформ_</span><span class="sxs-lookup"><span data-stu-id="cfba0-104">_Applies To: Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="cfba0-105">Эта тема применяется к следующим компонентам и версиям Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="cfba0-105">This topic applies to the following Dynamics 365 Project Operations components and versions:</span></span>

- <span data-ttu-id="cfba0-106">Project Operations в среде Dataverse версии 4.8.0.91</span><span class="sxs-lookup"><span data-stu-id="cfba0-106">Project Operations on Dataverse environment version 4.8.0.91</span></span> 

## <a name="quality-updates"></a><span data-ttu-id="cfba0-107">Обновления качества</span><span class="sxs-lookup"><span data-stu-id="cfba0-107">Quality updates</span></span>

| <span data-ttu-id="cfba0-108">**Область функций**</span><span class="sxs-lookup"><span data-stu-id="cfba0-108">**Feature area**</span></span> | <span data-ttu-id="cfba0-109">**Номер ссылки**</span><span class="sxs-lookup"><span data-stu-id="cfba0-109">**Reference number**</span></span> | <span data-ttu-id="cfba0-110">**Обновление качества**</span><span class="sxs-lookup"><span data-stu-id="cfba0-110">**Quality update**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="cfba0-111">Выставление счетов и ценообразование</span><span class="sxs-lookup"><span data-stu-id="cfba0-111">Billing and pricing</span></span> | <span data-ttu-id="cfba0-112">2133873</span><span class="sxs-lookup"><span data-stu-id="cfba0-112">2133873</span></span> | <span data-ttu-id="cfba0-113">Исправлено отображение обозначения денежной единицы **Цена продажи единицы** в таблице **Оценка расходов**.</span><span class="sxs-lookup"><span data-stu-id="cfba0-113">Fixed the display of **Unit Sales Price** currency symbol in the **Expense Estimates** grid.</span></span> |
| <span data-ttu-id="cfba0-114">Выставление счетов и ценообразование</span><span class="sxs-lookup"><span data-stu-id="cfba0-114">Billing and pricing</span></span> | <span data-ttu-id="cfba0-115">2174616</span><span class="sxs-lookup"><span data-stu-id="cfba0-115">2174616</span></span> | <span data-ttu-id="cfba0-116">Когда предложение выиграно, пользовательский прайс-лист указывается в деталях строки контракта, которые копируются из предложения.</span><span class="sxs-lookup"><span data-stu-id="cfba0-116">When a quote is won, the contract custom pricelist is referenced on contract line details that are copied from the quote.</span></span> |
| <span data-ttu-id="cfba0-117">Управление возможными сделками</span><span class="sxs-lookup"><span data-stu-id="cfba0-117">Opportunity Management</span></span> | <span data-ttu-id="cfba0-118">2167475</span><span class="sxs-lookup"><span data-stu-id="cfba0-118">2167475</span></span> | <span data-ttu-id="cfba0-119">Фиксированная сумма налога в корректирующем счете-фактуре, которая является фактической записью, по которой не выставлен счет.</span><span class="sxs-lookup"><span data-stu-id="cfba0-119">Fixed tax amount in the correction invoice that originated an unbilled actual entry.</span></span> |
| <span data-ttu-id="cfba0-120">Управление возможными сделками</span><span class="sxs-lookup"><span data-stu-id="cfba0-120">Opportunity Management</span></span> | <span data-ttu-id="cfba0-121">2176285</span><span class="sxs-lookup"><span data-stu-id="cfba0-121">2176285</span></span> | <span data-ttu-id="cfba0-122">Сумма налога не должна копироваться из деталей строки контракта/предложения с расценками продаж в детали строки контракта/предложения с расценками затрат.</span><span class="sxs-lookup"><span data-stu-id="cfba0-122">Tax amount must not be copied from sales contract/quote line details to cost contract/quote line details.</span></span> |
| <span data-ttu-id="cfba0-123">Управление возможными сделками</span><span class="sxs-lookup"><span data-stu-id="cfba0-123">Opportunity Management</span></span> | <span data-ttu-id="cfba0-124">2188079</span><span class="sxs-lookup"><span data-stu-id="cfba0-124">2188079</span></span> | <span data-ttu-id="cfba0-125">Правило раздельного выставления счетов не должно создаваться для контрактов, не основанных на работе.</span><span class="sxs-lookup"><span data-stu-id="cfba0-125">Split billing rule must not be created for contracts that are not work-based.</span></span> |
| <span data-ttu-id="cfba0-126">Планирование и отслеживание</span><span class="sxs-lookup"><span data-stu-id="cfba0-126">Planning and Tracking</span></span> | <span data-ttu-id="cfba0-127">2138853</span><span class="sxs-lookup"><span data-stu-id="cfba0-127">2138853</span></span> | <span data-ttu-id="cfba0-128">Функция копирования проекта обновлена, чтобы строки оценки расходов, содержащие задачи, копировались в целевой проект.</span><span class="sxs-lookup"><span data-stu-id="cfba0-128">Project copy function updated to ensure expense estimate lines that reference tasks are copied to the destination project.</span></span> |
| <span data-ttu-id="cfba0-129">Планирование и отслеживание</span><span class="sxs-lookup"><span data-stu-id="cfba0-129">Planning and Tracking</span></span> | <span data-ttu-id="cfba0-130">2173259</span><span class="sxs-lookup"><span data-stu-id="cfba0-130">2173259</span></span> | <span data-ttu-id="cfba0-131">Функция копирования проекта обновлена, чтобы не показывалось сообщение об ошибке **Копирование WBS** в определенных сценариях.</span><span class="sxs-lookup"><span data-stu-id="cfba0-131">Project copy function updated to ensure it doesn't display the **Copying WBS** error message in certain scenarios.</span></span> |
| <span data-ttu-id="cfba0-132">Время и расходы</span><span class="sxs-lookup"><span data-stu-id="cfba0-132">Time and Expense</span></span> | <span data-ttu-id="cfba0-133">2148910</span><span class="sxs-lookup"><span data-stu-id="cfba0-133">2148910</span></span> | <span data-ttu-id="cfba0-134">Исправлена проблема отображения страницы **Изменить запись** в таблице **Ввод времени**.</span><span class="sxs-lookup"><span data-stu-id="cfba0-134">Fixed display issue with the **Edit Entry** page in the **Time Entry** grid.</span></span> |
| <span data-ttu-id="cfba0-135">Время и расходы</span><span class="sxs-lookup"><span data-stu-id="cfba0-135">Time and Expense</span></span> | <span data-ttu-id="cfba0-136">2159798</span><span class="sxs-lookup"><span data-stu-id="cfba0-136">2159798</span></span> | <span data-ttu-id="cfba0-137">Усиленный контроль, гарантирующий, что утвержденные записи о расходах нельзя редактировать.</span><span class="sxs-lookup"><span data-stu-id="cfba0-137">Tightened controls to ensure approved expense entries can't be edited.</span></span> |

