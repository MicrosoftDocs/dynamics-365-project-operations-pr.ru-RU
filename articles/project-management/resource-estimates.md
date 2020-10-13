---
title: Оценка ресурсов
description: Эта тема предоставляет информацию о том, как рассчитываются оценки ресурсов в Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2ebde2b3c5bcfb5faa02ee476065ac34b1953432
ms.sourcegitcommit: f255b2cbf290973ce62fe2c1c121bd1df15a7392
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/01/2020
ms.locfileid: "3928600"
---
# <a name="resource-estimates"></a><span data-ttu-id="acc87-103">Оценка ресурсов</span><span class="sxs-lookup"><span data-stu-id="acc87-103">Resource estimates</span></span>

<span data-ttu-id="acc87-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="acc87-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="acc87-105">Оценки ресурсов основаны на поэтапных усилиях, определенных в структурной декомпозиции работ вместе с применимыми ценовыми измерениями.</span><span class="sxs-lookup"><span data-stu-id="acc87-105">Resource estimates come from time-phased effort that is defined in the work breakdown structure along with applicable pricing dimensions.</span></span> <span data-ttu-id="acc87-106">Обычно расчет выполняется по формуле **ставка/час для каждой роли x часы.**</span><span class="sxs-lookup"><span data-stu-id="acc87-106">Typically, the calculation is **rate/hr for each role x hours.**</span></span> <span data-ttu-id="acc87-107">Повременные усилия для каждого ресурса хранятся в записи о назначении ресурсов.</span><span class="sxs-lookup"><span data-stu-id="acc87-107">The time-phased effort for each resource is stored in the resource assignment record.</span></span> <span data-ttu-id="acc87-108">Цены хранятся в заранее определенном прайс-листе.</span><span class="sxs-lookup"><span data-stu-id="acc87-108">The pricing is stored in a pre-defined price list.</span></span> <span data-ttu-id="acc87-109">Преобразование единиц осуществляется на основании действующего прайс-листа.</span><span class="sxs-lookup"><span data-stu-id="acc87-109">Unit conversion is applied based on the applicable price list.</span></span>

![Оценки ресурсов](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a><span data-ttu-id="acc87-111">Себестоимость и валюта себестоимости по умолчанию</span><span class="sxs-lookup"><span data-stu-id="acc87-111">Default cost price and cost currency</span></span>

<span data-ttu-id="acc87-112">Значения себестоимости по умолчанию берутся из подразделения.</span><span class="sxs-lookup"><span data-stu-id="acc87-112">Cost prices are defaulted from the Organizational Unit.</span></span>

## <a name="default-bill-rate-and-sales-currency"></a><span data-ttu-id="acc87-113">Ставка и валюта продаж по умолчанию</span><span class="sxs-lookup"><span data-stu-id="acc87-113">Default bill rate and sales currency</span></span>

<span data-ttu-id="acc87-114">Цены продажи применяется один раз за сделку.</span><span class="sxs-lookup"><span data-stu-id="acc87-114">Sales prices are applied once per deal.</span></span> <span data-ttu-id="acc87-115">Иерархия цен продажи по умолчанию следующая:</span><span class="sxs-lookup"><span data-stu-id="acc87-115">The hierarchy for sale price list defaulting is as follows:</span></span>

1. <span data-ttu-id="acc87-116">Предприятие</span><span class="sxs-lookup"><span data-stu-id="acc87-116">Organization</span></span>
2. <span data-ttu-id="acc87-117">Клиент</span><span class="sxs-lookup"><span data-stu-id="acc87-117">Customer</span></span>
3. <span data-ttu-id="acc87-118">Предложение с расценками/контракт</span><span class="sxs-lookup"><span data-stu-id="acc87-118">Quote/contract</span></span>
