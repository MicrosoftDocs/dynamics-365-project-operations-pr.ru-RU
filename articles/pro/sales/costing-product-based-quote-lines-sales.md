---
title: Определение строк предложения с расценками на основе продуктов
description: В этом разделе представлена информация о применении себестоимости к строке предложения с расценками на основе продуктов.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 1fa7896e249abfefd3e93cba4bad789e67e14f31
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003467"
---
# <a name="costing-product-based-quote-lines"></a><span data-ttu-id="b2da8-103">Определение строк предложения с расценками на основе продуктов</span><span class="sxs-lookup"><span data-stu-id="b2da8-103">Costing product-based quote lines</span></span>

<span data-ttu-id="b2da8-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="b2da8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="b2da8-105">Строки предложений на основе продуктов в Dynamics 365 Project Operations также имеют поле **Себестоимость**.</span><span class="sxs-lookup"><span data-stu-id="b2da8-105">Product-based quote lines in Dynamics 365 Project Operations also have a **Cost Price** field.</span></span> <span data-ttu-id="b2da8-106">Это поле используется для отслеживания себестоимости продукта в строке предложения с расценками и для последующих расчетов рентабельности.</span><span class="sxs-lookup"><span data-stu-id="b2da8-106">This field is used to track the cost price for the product on the quote line and for downstream profitability calculations.</span></span>

<span data-ttu-id="b2da8-107">Когда для продукта из каталога создается строка предложения с расценками на основе продукта, стоимость строки предложения с расценками на основе продукта устанавливается по умолчанию из поля **Нормативная стоимость** в каталоге товаров.</span><span class="sxs-lookup"><span data-stu-id="b2da8-107">When a product-based quote line is created for a catalog product, the cost of the product-based quote line is defaulted from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="b2da8-108">Поле стандартной стоимости в каталоге продуктов настроено в базовой валюте организации.</span><span class="sxs-lookup"><span data-stu-id="b2da8-108">The standard cost field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="b2da8-109">Стоимость единицы измерения по умолчанию в строке предложения с расценками на основе продукта конвертируется в валюту продаж в предложении с расценками.</span><span class="sxs-lookup"><span data-stu-id="b2da8-109">The default unit cost on the product-based quote line is converted to the sales currency on the quote.</span></span>

## <a name="unit-cost-on-a-product-based-quote-line"></a><span data-ttu-id="b2da8-110">Стоимость единицы измерения в строке предложения с расценками на основе продуктов</span><span class="sxs-lookup"><span data-stu-id="b2da8-110">Unit cost on a product-based quote line</span></span>

<span data-ttu-id="b2da8-111">Назначение стоимости единицы измерения в строке предложения с расценками на основе продукта состоит в том, чтобы учесть разные затраты на продукт для каждой продажи.</span><span class="sxs-lookup"><span data-stu-id="b2da8-111">The purpose of having a unit cost on a product-based quote line is to allow for different costs for a product for each sale.</span></span> <span data-ttu-id="b2da8-112">Это нетипичный сценарий, но иногда стоимость продукта может быть снижена поставщиком в зависимости от покупателя конечной продажи.</span><span class="sxs-lookup"><span data-stu-id="b2da8-112">This is not a typical scenario, but sometimes the cost of the product may be discounted by the supplier depending on the customer of the final sale.</span></span>

<span data-ttu-id="b2da8-113">Например:</span><span class="sxs-lookup"><span data-stu-id="b2da8-113">For example:</span></span>

<span data-ttu-id="b2da8-114">Fabrikam Robotics устанавливает роботизированные манипуляторы на сборочных линиях корпорации A Datum Corporation.</span><span class="sxs-lookup"><span data-stu-id="b2da8-114">Fabrikam Robotics is installing robotic arms at A Datum Corporation's assembly lines.</span></span> <span data-ttu-id="b2da8-115">Fabrikam предоставляет услуги по установке, но роботизированные манипуляторы закупаются у компании Trey Robotics.</span><span class="sxs-lookup"><span data-stu-id="b2da8-115">Fabrikam provides installation services but the robotic arms are procured from Trey robotics.</span></span> <span data-ttu-id="b2da8-116">Если установка роботизированных манипуляторов в корпорации A Datum Corporation откроет новую вертикаль отрасли производства для роботизированных манипуляторов компании Trey, компания Trey может предоставить Fabrikam особую скидку на эту сделку.</span><span class="sxs-lookup"><span data-stu-id="b2da8-116">If the installation of robotic arms at A Datum Corporation opens a new industry vertical for Trey's robotic arms, Trey could give a special discount for this deal to Fabrikam.</span></span>

<span data-ttu-id="b2da8-117">В этом случае Fabrikam создаст строку предложения с расценками на основе продукта для роботизированных манипуляторов и введет специальную стоимость за единицу измерения для этого предложения.</span><span class="sxs-lookup"><span data-stu-id="b2da8-117">In this case, Fabrikam will create product-based quote line for Robotic Arms and input a special per unit cost for this quote.</span></span> <span data-ttu-id="b2da8-118">Эта стоимость отличается от стандартной стоимости манипуляторов Trey Robotic.</span><span class="sxs-lookup"><span data-stu-id="b2da8-118">This cost is different from the standard cost of Trey Robotic Arms.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]