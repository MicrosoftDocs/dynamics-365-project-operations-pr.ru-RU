---
title: Оценка ресурсов
description: Эта тема предоставляет информацию о том, как рассчитываются оценки ресурсов в Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 454b8931db53739a7bc19364911109802a1ed087
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127392"
---
# <a name="resource-estimates"></a><span data-ttu-id="9e628-103">Оценка ресурсов</span><span class="sxs-lookup"><span data-stu-id="9e628-103">Resource estimates</span></span>

<span data-ttu-id="9e628-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="9e628-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9e628-105">Оценки ресурсов основаны на поэтапных усилиях, определенных в структурной декомпозиции работ вместе с применимыми ценовыми измерениями.</span><span class="sxs-lookup"><span data-stu-id="9e628-105">Resource estimates come from time-phased effort that is defined in the work breakdown structure along with applicable pricing dimensions.</span></span> <span data-ttu-id="9e628-106">Обычно расчет выполняется по формуле **ставка/час для каждой роли x часы.**</span><span class="sxs-lookup"><span data-stu-id="9e628-106">Typically, the calculation is **rate/hr for each role x hours.**</span></span> <span data-ttu-id="9e628-107">Повременные усилия для каждого ресурса хранятся в записи о назначении ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9e628-107">The time-phased effort for each resource is stored in the resource assignment record.</span></span> <span data-ttu-id="9e628-108">Цены хранятся в заранее определенном прайс-листе.</span><span class="sxs-lookup"><span data-stu-id="9e628-108">The pricing is stored in a pre-defined price list.</span></span> <span data-ttu-id="9e628-109">Преобразование единиц осуществляется на основании действующего прайс-листа.</span><span class="sxs-lookup"><span data-stu-id="9e628-109">Unit conversion is applied based on the applicable price list.</span></span>

![Оценки ресурсов](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a><span data-ttu-id="9e628-111">Себестоимость и валюта себестоимости по умолчанию</span><span class="sxs-lookup"><span data-stu-id="9e628-111">Default cost price and cost currency</span></span>

<span data-ttu-id="9e628-112">Значения себестоимости по умолчанию берутся из подразделения.</span><span class="sxs-lookup"><span data-stu-id="9e628-112">Cost prices are defaulted from the Organizational Unit.</span></span>

## <a name="default-bill-rate-and-sales-currency"></a><span data-ttu-id="9e628-113">Ставка и валюта продаж по умолчанию</span><span class="sxs-lookup"><span data-stu-id="9e628-113">Default bill rate and sales currency</span></span>

<span data-ttu-id="9e628-114">Цены продажи применяется один раз за сделку.</span><span class="sxs-lookup"><span data-stu-id="9e628-114">Sales prices are applied once per deal.</span></span> <span data-ttu-id="9e628-115">Иерархия цен продажи по умолчанию следующая:</span><span class="sxs-lookup"><span data-stu-id="9e628-115">The hierarchy for sale price list defaulting is as follows:</span></span>

1. <span data-ttu-id="9e628-116">Предприятие</span><span class="sxs-lookup"><span data-stu-id="9e628-116">Organization</span></span>
2. <span data-ttu-id="9e628-117">Клиент</span><span class="sxs-lookup"><span data-stu-id="9e628-117">Customer</span></span>
3. <span data-ttu-id="9e628-118">Предложение с расценками/контракт</span><span class="sxs-lookup"><span data-stu-id="9e628-118">Quote/contract</span></span>
