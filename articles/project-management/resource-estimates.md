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
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083108"
---
# <a name="resource-estimates"></a><span data-ttu-id="afddd-103">Оценка ресурсов</span><span class="sxs-lookup"><span data-stu-id="afddd-103">Resource estimates</span></span>

<span data-ttu-id="afddd-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="afddd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="afddd-105">Оценки ресурсов основаны на поэтапных усилиях, определенных в структурной декомпозиции работ вместе с применимыми ценовыми измерениями.</span><span class="sxs-lookup"><span data-stu-id="afddd-105">Resource estimates come from time-phased effort that is defined in the work breakdown structure along with applicable pricing dimensions.</span></span> <span data-ttu-id="afddd-106">Обычно расчет выполняется по формуле **ставка/час для каждой роли x часы.**</span><span class="sxs-lookup"><span data-stu-id="afddd-106">Typically, the calculation is **rate/hr for each role x hours.**</span></span> <span data-ttu-id="afddd-107">Повременные усилия для каждого ресурса хранятся в записи о назначении ресурсов.</span><span class="sxs-lookup"><span data-stu-id="afddd-107">The time-phased effort for each resource is stored in the resource assignment record.</span></span> <span data-ttu-id="afddd-108">Цены хранятся в заранее определенном прайс-листе.</span><span class="sxs-lookup"><span data-stu-id="afddd-108">The pricing is stored in a pre-defined price list.</span></span> <span data-ttu-id="afddd-109">Преобразование единиц осуществляется на основании действующего прайс-листа.</span><span class="sxs-lookup"><span data-stu-id="afddd-109">Unit conversion is applied based on the applicable price list.</span></span>

![Оценки ресурсов](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a><span data-ttu-id="afddd-111">Себестоимость и валюта себестоимости по умолчанию</span><span class="sxs-lookup"><span data-stu-id="afddd-111">Default cost price and cost currency</span></span>

<span data-ttu-id="afddd-112">Значения себестоимости по умолчанию берутся из подразделения.</span><span class="sxs-lookup"><span data-stu-id="afddd-112">Cost prices are defaulted from the Organizational Unit.</span></span>

## <a name="default-bill-rate-and-sales-currency"></a><span data-ttu-id="afddd-113">Ставка и валюта продаж по умолчанию</span><span class="sxs-lookup"><span data-stu-id="afddd-113">Default bill rate and sales currency</span></span>

<span data-ttu-id="afddd-114">Цены продажи применяется один раз за сделку.</span><span class="sxs-lookup"><span data-stu-id="afddd-114">Sales prices are applied once per deal.</span></span> <span data-ttu-id="afddd-115">Иерархия цен продажи по умолчанию следующая:</span><span class="sxs-lookup"><span data-stu-id="afddd-115">The hierarchy for sale price list defaulting is as follows:</span></span>

1. <span data-ttu-id="afddd-116">Предприятие</span><span class="sxs-lookup"><span data-stu-id="afddd-116">Organization</span></span>
2. <span data-ttu-id="afddd-117">Клиент</span><span class="sxs-lookup"><span data-stu-id="afddd-117">Customer</span></span>
3. <span data-ttu-id="afddd-118">Предложение с расценками/контракт</span><span class="sxs-lookup"><span data-stu-id="afddd-118">Quote/contract</span></span>
