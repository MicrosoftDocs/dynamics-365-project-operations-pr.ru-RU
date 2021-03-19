---
title: Просмотр невыполненной работы по выставлению счетов для проектов и контрактов по проекту
description: В этом разделе представлена информация о том, как проверить невыполненные работы по времени, расходам и продуктам, а также как отметить их как готовые к выставлению счетов.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom: ''
ms.author: rumant
ms.date: 03/11/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: bdeeb100614cda78d0ba536310bb6b411c863b71
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282799"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a><span data-ttu-id="ac3d9-103">Просмотр невыполненной работы по выставлению счетов для проектов и контрактов по проекту</span><span class="sxs-lookup"><span data-stu-id="ac3d9-103">Review the invoicing backlog on projects and project contracts</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="ac3d9-104">Когда транзакция готова к созданию и обработке счета, транзакция должна быть отмечена как **Готово к выставлению счета**.</span><span class="sxs-lookup"><span data-stu-id="ac3d9-104">When a transaction is ready to have an invoice created and processed, the transaction should be marked **Ready to invoice**.</span></span> <span data-ttu-id="ac3d9-105">В этом разделе описываются виды транзакций, которые можно создавать.</span><span class="sxs-lookup"><span data-stu-id="ac3d9-105">This topic describes the types of transactions that can be created.</span></span>

## <a name="review-the-time-and-material-billing-backlog"></a><span data-ttu-id="ac3d9-106">Просмотр невыполненной работы по выставлению счетов по времени и материалам</span><span class="sxs-lookup"><span data-stu-id="ac3d9-106">Review the time and material billing backlog</span></span>

<span data-ttu-id="ac3d9-107">Когда запись времени или расхода отправляется и утверждается для проекта, приложение PSA, создает фактические данные проекта.</span><span class="sxs-lookup"><span data-stu-id="ac3d9-107">When a time or expense entry is submitted and approved for a project, PSA creates a project actual.</span></span> <span data-ttu-id="ac3d9-108">Если сочетание проекта и класса транзакции сопоставляется строке контракта для проекта на основе времени и материалов, два фактических значения создается при утверждении записи:</span><span class="sxs-lookup"><span data-stu-id="ac3d9-108">If the combination of the project and the transaction class are mapped to a contract line for a time-and-materials project, two actuals are created when the entry is approved:</span></span>

- <span data-ttu-id="ac3d9-109">Фактические данные стоимости</span><span class="sxs-lookup"><span data-stu-id="ac3d9-109">Cost actual</span></span> 
- <span data-ttu-id="ac3d9-110">Фактические данные продажи без выставления счета</span><span class="sxs-lookup"><span data-stu-id="ac3d9-110">Unbilled sales actual</span></span>

<span data-ttu-id="ac3d9-111">Фактические данные продаж без выставленного счета представляют невыполненную работу по выставлению счетов, и их состояние выставления счетов должно быть установлено в значение **Готово к выставлению счета**.</span><span class="sxs-lookup"><span data-stu-id="ac3d9-111">Unbilled sales actuals represent the billing backlog, and their billing status must be set to **Ready to Invoice**.</span></span> <span data-ttu-id="ac3d9-112">Когда создается счет по проекту, фактические данные продаж без выставленного счета, отмеченные как **Готово к выставлению счета**, копируются как сведения строки счета.</span><span class="sxs-lookup"><span data-stu-id="ac3d9-112">When a project invoice is created, unbilled sales actuals that are marked **Ready to Invoice** are copied over as invoice line details.</span></span>

<span data-ttu-id="ac3d9-113">Для проверки невыполненной работы по выставлению счетов для времени и материалов откройте **Продажи** \> **Выставление счетов** \> **Задолженность по выставлению счетов по времени и материалам**.</span><span class="sxs-lookup"><span data-stu-id="ac3d9-113">To review the billing backlog for time and materials, go to **Sales** \> **Billing** \> **Time and Material Billing Backlog**.</span></span> <span data-ttu-id="ac3d9-114">Выберите все фактические данные продаж без выставленного счета, которые готовы к выставлению счетов, затем выберите **Готово к выставлению счета**.</span><span class="sxs-lookup"><span data-stu-id="ac3d9-114">Select all the unbilled sales actuals that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="ac3d9-115">Состояние выставления счета этих фактических данных изменяется на **Готово к выставлению счета**.</span><span class="sxs-lookup"><span data-stu-id="ac3d9-115">The billing status of these actuals is changed to **Ready to Invoice**.</span></span>

![Задолженность по выставлению счетов по времени и материалам](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a><span data-ttu-id="ac3d9-117">Просмотр невыполненной работы по выставлению счетов по продуктам</span><span class="sxs-lookup"><span data-stu-id="ac3d9-117">Review the product billing backlog</span></span>

<span data-ttu-id="ac3d9-118">В PSA когда контракт по проекту имеет строки на основании продуктов, эти строки рассматриваются для выставления счетов каждый раз, когда создается счет для контракта по проекту.</span><span class="sxs-lookup"><span data-stu-id="ac3d9-118">In PSA, when a project contract has product-based contract lines, those lines are considered for invoicing whenever an invoice is created for the project contract.</span></span> <span data-ttu-id="ac3d9-119">Любой продукт, который имеет строки контракта, отмеченные как **Готово к выставлению счета**, будет скопирован в счет по проекту в виде строк счета по проекту.</span><span class="sxs-lookup"><span data-stu-id="ac3d9-119">Any product that has contract lines that are marked **Ready to Invoice** is copied over to the project invoice as project invoice lines.</span></span>

<span data-ttu-id="ac3d9-120">Для просмотра невыполненных работ по выставлению счетов для продуктов откройте **Продажи** \> **Выставление счетов** \> **Задолженность по выставлению счетов по продуктам**.</span><span class="sxs-lookup"><span data-stu-id="ac3d9-120">To review the billing backlog for products, go to **Sales** \> **Billing** \> **Product Billing Backlog**.</span></span> <span data-ttu-id="ac3d9-121">Выберите все строки контракта на основе продуктов, которые готовы к выставлению счетов, затем выберите **Готово к выставлению счета**.</span><span class="sxs-lookup"><span data-stu-id="ac3d9-121">Select all the product-based contract lines that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="ac3d9-122">Состояние выставления счета этих строк изменяется на **Готово к выставлению счета**.</span><span class="sxs-lookup"><span data-stu-id="ac3d9-122">The billing status of these lines is changed to **Ready to Invoice**.</span></span>

![Задолженность по выставлению счетов по продуктам](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a><span data-ttu-id="ac3d9-124">Просмотр вех выставления счетов в контрактах с фиксированной ценой</span><span class="sxs-lookup"><span data-stu-id="ac3d9-124">Review billing milestones on fixed-price contracts</span></span>

<span data-ttu-id="ac3d9-125">Каждая строка контракта по проекту с методом выставления счетов с фиксированной ценой должны определять вехи контракта.</span><span class="sxs-lookup"><span data-stu-id="ac3d9-125">Each project contract line that has a fixed-price billing method must define contract milestones.</span></span> <span data-ttu-id="ac3d9-126">Счета за эти вехи контракта можно выставлять только в том случае, если они отмечены как **Готово к выставлению счета**.</span><span class="sxs-lookup"><span data-stu-id="ac3d9-126">These contract milestones can be invoiced only if they are marked **Ready to Invoice**.</span></span> 

<span data-ttu-id="ac3d9-127">Для просмотра вех выставления счетов откройте **Продажи** \> **Выставление счетов** \> **Вехи фиксированных цен**.</span><span class="sxs-lookup"><span data-stu-id="ac3d9-127">To review billing milestones, go to **Sales** \> **Billing** \> **Fixed Price Milestones**.</span></span> <span data-ttu-id="ac3d9-128">Выберите вехи, которые готовы к выставлению счетов, затем выберите **Готово к выставлению счета**.</span><span class="sxs-lookup"><span data-stu-id="ac3d9-128">Select the milestones that are ready to be invoiced, and then select **Ready to invoice**.</span></span> <span data-ttu-id="ac3d9-129">Состояние выставления счета этих вех изменяется на **Готово к выставлению счета**.</span><span class="sxs-lookup"><span data-stu-id="ac3d9-129">The billing status of these milestones is changed to **Ready to Invoice**.</span></span>

![Вехи фиксированных цен](media/FPBacklog.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]