---
title: Расчет себестоимости строк контракта на основе продуктов — облегченное развертывание
description: В этом разделе представлена информация о создании
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9458a57863244a68359f57185325c03a46bd6569
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003557"
---
# <a name="cost-product-based-contract-lines---lite"></a><span data-ttu-id="9628d-103">Расчет себестоимости строк контракта на основе продуктов — облегченное развертывание</span><span class="sxs-lookup"><span data-stu-id="9628d-103">Cost product-based contract lines - lite</span></span>

<span data-ttu-id="9628d-104">_**Относится к:** развертывание Lite — от сделки до счетов-проформ_</span><span class="sxs-lookup"><span data-stu-id="9628d-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="9628d-105">Строки контракта на основе продуктов в Dynamics 365 Project Operations включить поле **Себестоимость**, в котором хранится себестоимость продукта для последующих расчетов прибыльности.</span><span class="sxs-lookup"><span data-stu-id="9628d-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="9628d-106">Когда для продукта из каталога создается строка контракта на основе продукта, стоимость строки по умолчанию берется из поле **Нормативная стоимость** в каталоге товаров.</span><span class="sxs-lookup"><span data-stu-id="9628d-106">When a product-based contract line is created for a catalog product, the cost of the line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="9628d-107">Поле **Стандартные затраты** в каталоге продуктов настроено в базовой валюте организации.</span><span class="sxs-lookup"><span data-stu-id="9628d-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="9628d-108">Когда стоимость единицы в строке контракта устанавливается по умолчанию, она конвертируется в валюту продаж по контракту.</span><span class="sxs-lookup"><span data-stu-id="9628d-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="9628d-109">Стоимость единицы измерения в строке контракта на основе продуктов</span><span class="sxs-lookup"><span data-stu-id="9628d-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="9628d-110">Назначение стоимости единицы измерения в строке контракта на основе продукта позволяет учесть разные затраты на продукт для каждой продажи единицы.</span><span class="sxs-lookup"><span data-stu-id="9628d-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="9628d-111">Хотя это не всегда необходимо, существуют определенные сценарии, в которых стоимость продукта может быть снижена поставщиком для клиента.</span><span class="sxs-lookup"><span data-stu-id="9628d-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="9628d-112">Рассмотрим следующий сценарий:</span><span class="sxs-lookup"><span data-stu-id="9628d-112">Consider the following scenario:</span></span>

<span data-ttu-id="9628d-113">Fabrikam Robotics устанавливает роботизированные манипуляторы на сборочных линиях корпорации Adatum Corporation.</span><span class="sxs-lookup"><span data-stu-id="9628d-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="9628d-114">Fabrikam предоставляет услуги по установке, но роботизированные манипуляторы поставляются компанией Trey Research.</span><span class="sxs-lookup"><span data-stu-id="9628d-114">Fabrikam provides installation services but the robotic arms are from Trey Research.</span></span> <span data-ttu-id="9628d-115">Если установка роботизированных манипуляторов в корпорации Adatum Corporation откроет новую вертикаль отрасли производства для роботизированных манипуляторов компании Trey Research, эта компания может предложить Fabrikam особую скидку на эту сделку.</span><span class="sxs-lookup"><span data-stu-id="9628d-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="9628d-116">В этом случае Fabrikam создает строки контракта на основе продуктов для Robotic Arms.</span><span class="sxs-lookup"><span data-stu-id="9628d-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms.</span></span> <span data-ttu-id="9628d-117">Для этого контракта вводится стоимость за единицу.</span><span class="sxs-lookup"><span data-stu-id="9628d-117">A per unit cost is entered for this contract.</span></span> <span data-ttu-id="9628d-118">Стоимость отличается от стоимости роботизированных манипуляторов от Trey Research.</span><span class="sxs-lookup"><span data-stu-id="9628d-118">The cost is different from the cost of robotic arms from Trey Research.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]