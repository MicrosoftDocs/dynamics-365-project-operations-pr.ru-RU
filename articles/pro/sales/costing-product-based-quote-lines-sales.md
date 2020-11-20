---
title: Определение строк предложения с расценками на основе продуктов
description: В этом разделе представлена информация о применении себестоимости к строке предложения с расценками на основе продуктов.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d21ab159294cac66ffeb8abcf0943b4babd7b360
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4118940"
---
# <a name="costing-product-based-quote-lines"></a><span data-ttu-id="fed85-103">Определение строк предложения с расценками на основе продуктов</span><span class="sxs-lookup"><span data-stu-id="fed85-103">Costing product-based quote lines</span></span>

<span data-ttu-id="fed85-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="fed85-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="fed85-105">Строки предложений на основе продуктов в Dynamics 365 Project Operations также имеют поле **Себестоимость**.</span><span class="sxs-lookup"><span data-stu-id="fed85-105">Product-based quote lines in Dynamics 365 Project Operations also have a **Cost Price** field.</span></span> <span data-ttu-id="fed85-106">Это поле используется для отслеживания себестоимости продукта в строке предложения с расценками и для последующих расчетов рентабельности.</span><span class="sxs-lookup"><span data-stu-id="fed85-106">This field is used to track the cost price for the product on the quote line and for downstream profitability calculations.</span></span>

<span data-ttu-id="fed85-107">Когда для продукта из каталога создается строка предложения с расценками на основе продукта, стоимость строки предложения с расценками на основе продукта устанавливается по умолчанию из поля **Нормативная стоимость** в каталоге товаров.</span><span class="sxs-lookup"><span data-stu-id="fed85-107">When a product-based quote line is created for a catalog product, the cost of the product-based quote line is defaulted from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="fed85-108">Поле стандартной стоимости в каталоге продуктов настроено в базовой валюте организации.</span><span class="sxs-lookup"><span data-stu-id="fed85-108">The standard cost field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="fed85-109">Стоимость единицы измерения по умолчанию в строке предложения с расценками на основе продукта конвертируется в валюту продаж в предложении с расценками.</span><span class="sxs-lookup"><span data-stu-id="fed85-109">The default unit cost on the product-based quote line is converted to the sales currency on the quote.</span></span>

## <a name="unit-cost-on-a-product-based-quote-line"></a><span data-ttu-id="fed85-110">Стоимость единицы измерения в строке предложения с расценками на основе продуктов</span><span class="sxs-lookup"><span data-stu-id="fed85-110">Unit cost on a product-based quote line</span></span>

<span data-ttu-id="fed85-111">Назначение стоимости единицы измерения в строке предложения с расценками на основе продукта состоит в том, чтобы учесть разные затраты на продукт для каждой продажи.</span><span class="sxs-lookup"><span data-stu-id="fed85-111">The purpose of having a unit cost on a product-based quote line is to allow for different costs for a product for each sale.</span></span> <span data-ttu-id="fed85-112">Это нетипичный сценарий, но иногда стоимость продукта может быть снижена поставщиком в зависимости от покупателя конечной продажи.</span><span class="sxs-lookup"><span data-stu-id="fed85-112">This is not a typical scenario, but sometimes the cost of the product may be discounted by the supplier depending on the customer of the final sale.</span></span>

<span data-ttu-id="fed85-113">Например:</span><span class="sxs-lookup"><span data-stu-id="fed85-113">For example:</span></span>

<span data-ttu-id="fed85-114">Fabrikam Robotics устанавливает роботизированные манипуляторы на сборочных линиях корпорации A Datum Corporation.</span><span class="sxs-lookup"><span data-stu-id="fed85-114">Fabrikam Robotics is installing robotic arms at A Datum Corporation's assembly lines.</span></span> <span data-ttu-id="fed85-115">Fabrikam предоставляет услуги по установке, но роботизированные манипуляторы закупаются у компании Trey Robotics.</span><span class="sxs-lookup"><span data-stu-id="fed85-115">Fabrikam provides installation services but the robotic arms are procured from Trey robotics.</span></span> <span data-ttu-id="fed85-116">Если установка роботизированных манипуляторов в корпорации A Datum Corporation откроет новую вертикаль отрасли производства для роботизированных манипуляторов компании Trey, компания Trey может предоставить Fabrikam особую скидку на эту сделку.</span><span class="sxs-lookup"><span data-stu-id="fed85-116">If the installation of robotic arms at A Datum Corporation opens a new industry vertical for Trey's robotic arms, Trey could give a special discount for this deal to Fabrikam.</span></span>

<span data-ttu-id="fed85-117">В этом случае Fabrikam создаст строку предложения с расценками на основе продукта для роботизированных манипуляторов и введет специальную стоимость за единицу измерения для этого предложения.</span><span class="sxs-lookup"><span data-stu-id="fed85-117">In this case, Fabrikam will create product-based quote line for Robotic Arms and input a special per unit cost for this quote.</span></span> <span data-ttu-id="fed85-118">Эта стоимость отличается от стандартной стоимости манипуляторов Trey Robotic.</span><span class="sxs-lookup"><span data-stu-id="fed85-118">This cost is different from the standard cost of Trey Robotic Arms.</span></span>
