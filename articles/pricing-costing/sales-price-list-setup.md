---
title: Настройка прайс-листа продаж
description: В этой теме предоставлена информация о прайс-листах продаж для ценообразования проекта.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 712dedb6766ff36181e261a66f3af99469449574
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004907"
---
# <a name="set-up-a-sales-price-list"></a><span data-ttu-id="1deb1-103">Настройка прайс-листа продаж</span><span class="sxs-lookup"><span data-stu-id="1deb1-103">Set up a sales price list</span></span>

<span data-ttu-id="1deb1-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="1deb1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1deb1-105">Для предложений с расценками и контрактов по проекту прайс-лист проекта имеет другую схему переопределения цен, чем прайс-лист продуктов.</span><span class="sxs-lookup"><span data-stu-id="1deb1-105">For project quotes and contracts, a project price list has a different price override pattern than a product price list.</span></span> <span data-ttu-id="1deb1-106">В строке предложения с ценами на основе каталога продуктов можно переопределить цену для ролей и категорий непосредственно в строке предложения, поскольку каждая строка предложения указывает ровно на один элемент каталога.</span><span class="sxs-lookup"><span data-stu-id="1deb1-106">On a product catalog–based quote line, you can override the price to roles and categories directly on the quote line, because each quote line points to exactly one catalog item.</span></span> <span data-ttu-id="1deb1-107">Однако в строке предложения на основе проекта невозможно переопределить цену для ролей и категорий непосредственно в строке предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="1deb1-107">However, on a project-based quote line, you can't override the price to roles and categories directly on the quote line.</span></span> <span data-ttu-id="1deb1-108">Вы можете используйте прайс-лист проекта для работы с двумя различными шаблонами переопределения.</span><span class="sxs-lookup"><span data-stu-id="1deb1-108">You can use the project price list to work with the two distinct override patterns.</span></span>

> [!NOTE]
> <span data-ttu-id="1deb1-109">Рекомендуется иметь различные прайс-листы для ваших ресурсов проекта и номенклатур каталога из-за их разного поведения при переопределении цены.</span><span class="sxs-lookup"><span data-stu-id="1deb1-109">We recommend that you have a separate price list for your project resources and your catalog items, because of the behavior differences between the two when you override pricing.</span></span>

<span data-ttu-id="1deb1-110">Каждая из следующих сущностей может иметь один или несколько связанных прайс-листов продажи для ценообразования проекта:</span><span class="sxs-lookup"><span data-stu-id="1deb1-110">Each of the following entities can have one or more associated sales price lists for project pricing:</span></span>

- <span data-ttu-id="1deb1-111">Клиент (организация)</span><span class="sxs-lookup"><span data-stu-id="1deb1-111">Customer (account)</span></span> 
- <span data-ttu-id="1deb1-112">Возможная сделка</span><span class="sxs-lookup"><span data-stu-id="1deb1-112">Opportunity</span></span> 
- <span data-ttu-id="1deb1-113">Предложение с расценками</span><span class="sxs-lookup"><span data-stu-id="1deb1-113">Quote</span></span> 
- <span data-ttu-id="1deb1-114">Контракт проекта</span><span class="sxs-lookup"><span data-stu-id="1deb1-114">Project Contract</span></span>

<span data-ttu-id="1deb1-115">Связи этих сущностей с прайс-листом указывается прайс-листами проекта.</span><span class="sxs-lookup"><span data-stu-id="1deb1-115">The association of these entities with a price list is indicated by the project price lists.</span></span> <span data-ttu-id="1deb1-116">Можно связать один или несколько прайс-листов с сущностями продаж "Клиент", "Возможная сделка", "Предложение" и "Контракт по проекту".</span><span class="sxs-lookup"><span data-stu-id="1deb1-116">You can associate one or more price lists with the Customer, Opportunity, Quote, and Project Contract sales entities.</span></span>

<span data-ttu-id="1deb1-117">Прайс-лист по умолчанию не вводится автоматически в запись клиента.</span><span class="sxs-lookup"><span data-stu-id="1deb1-117">A default project price list isn't automatically entered on a customer record.</span></span> <span data-ttu-id="1deb1-118">Однако можно вручную добавить прайс-лист проекта в запись клиента.</span><span class="sxs-lookup"><span data-stu-id="1deb1-118">However, you can manually attach a project price list to the customer record.</span></span> <span data-ttu-id="1deb1-119">Тем не менее, добавлять прайс-лист проекта вручную следует только при наличии настраиваемого соглашения по ценам с клиентом.</span><span class="sxs-lookup"><span data-stu-id="1deb1-119">Nevertheless, you should manually attach a project price list only when you have a custom pricing agreement with the customer.</span></span> 

<span data-ttu-id="1deb1-120">Если прайс-лист по проекту присоединен к сущности продаж, проверяются следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="1deb1-120">When a project price list is attached to a sales entity, the following information is validated:</span></span>

- <span data-ttu-id="1deb1-121">Прайс-лист имеет контекст **Продажи**.</span><span class="sxs-lookup"><span data-stu-id="1deb1-121">The price list has a context of **Sales**.</span></span> 
- <span data-ttu-id="1deb1-122">Валюта прайс-листа соответствует валюте клиента.</span><span class="sxs-lookup"><span data-stu-id="1deb1-122">The price list currency matches the customer currency.</span></span> 

<span data-ttu-id="1deb1-123">В контракте проекта используется следующий порядок старшинства для автоматического задания связанных прайс-листов проекта:</span><span class="sxs-lookup"><span data-stu-id="1deb1-123">On a project contract, the following order of precedence is used to automatically set related project price lists:</span></span>

1. <span data-ttu-id="1deb1-124">Предложение с расценками</span><span class="sxs-lookup"><span data-stu-id="1deb1-124">Quote</span></span>
2. <span data-ttu-id="1deb1-125">Возможная сделка</span><span class="sxs-lookup"><span data-stu-id="1deb1-125">Opportunity</span></span>
3. <span data-ttu-id="1deb1-126">Клиент</span><span class="sxs-lookup"><span data-stu-id="1deb1-126">Customer</span></span> 
4. <span data-ttu-id="1deb1-127">Глобальные параметры</span><span class="sxs-lookup"><span data-stu-id="1deb1-127">Global settings</span></span> 

<span data-ttu-id="1deb1-128">Если прайс-лист по проекту введен по умолчанию, система проверяет, что валюта совпадает с валютой клиента, а также, что введенные прайс-листы по умолчанию имеют контекст **Продажи**.</span><span class="sxs-lookup"><span data-stu-id="1deb1-128">When a project price list is entered by default, the system validates that the currency matches the customer’s currency, and that the default price lists that have been entered have a context of **Sales**.</span></span>

<span data-ttu-id="1deb1-129">Можно связать несколько прайс-листов с сущностями "Клиент", "Возможная сделка", "Предложение" и "Контракт по проекту".</span><span class="sxs-lookup"><span data-stu-id="1deb1-129">You can associate multiple project price lists with the Customer, Opportunity, Quote, and Project Contract entities.</span></span> <span data-ttu-id="1deb1-130">Эта возможность поддерживает цены по умолчанию на конкретные даты для длительного контракта по проекту, где может потребоваться несколько прайс-листов для учета обновления цен из-за инфляции.</span><span class="sxs-lookup"><span data-stu-id="1deb1-130">This capability supports date-specific default prices for a long-running project contract, where you might require more than one price list to account for price updates that occur because of inflation.</span></span> <span data-ttu-id="1deb1-131">Однако если прайс-листы, связанные с сущностью клиента, возможной сделки, предложения или контракта по проекту, имеют перекрывающиеся даты действия, то цены по умолчанию могут быть неверными.</span><span class="sxs-lookup"><span data-stu-id="1deb1-131">However, if the price lists that you associate with the Customer, Opportunity, Quote, or Project Contract entity have overlapping date effectivity, the default prices might be incorrect.</span></span> <span data-ttu-id="1deb1-132">Поэтому необходимо убедиться в том, что прайс-листы проекта, имеющие перекрывающие даты действия, не связанные с этими сущностями.</span><span class="sxs-lookup"><span data-stu-id="1deb1-132">Therefore, you should make sure that project price lists that have overlapping date effectivity aren't associated with those entities.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]