---
title: Расчет себестоимости строк контракта на основе продуктов — облегченное развертывание
description: В этом разделе представлена информация о создании
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0e961bcf32a5dd662b7cd27a23eb5f664c45c292
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177257"
---
# <a name="cost-product-based-contract-lines---lite"></a><span data-ttu-id="e49e3-103">Расчет себестоимости строк контракта на основе продуктов — облегченное развертывание</span><span class="sxs-lookup"><span data-stu-id="e49e3-103">Cost product-based contract lines - lite</span></span>

<span data-ttu-id="e49e3-104">_**Относится к:** развертывание Lite — от сделки до счетов-проформ_</span><span class="sxs-lookup"><span data-stu-id="e49e3-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="e49e3-105">Строки контрактов на основе продуктов в Dynamics 365 Project Operations включают поле **Себестоимость**, в котором хранится себестоимость продукта для последующих расчетов рентабельности.</span><span class="sxs-lookup"><span data-stu-id="e49e3-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="e49e3-106">Когда для продукта из каталога создается строка контракта на основе продукта, стоимость строки контракта на основе продукта устанавливается по умолчанию из поля **Стандартные затраты** в каталоге товаров.</span><span class="sxs-lookup"><span data-stu-id="e49e3-106">When a product-based contract line is created for a catalog product, the cost of the product-based contract line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="e49e3-107">Поле **Стандартные затраты** в каталоге продуктов настроено в базовой валюте организации.</span><span class="sxs-lookup"><span data-stu-id="e49e3-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="e49e3-108">Когда стоимость единицы в строке контракта устанавливается по умолчанию, она конвертируется в валюту продаж по контракту.</span><span class="sxs-lookup"><span data-stu-id="e49e3-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="e49e3-109">Стоимость единицы измерения в строке контракта на основе продуктов</span><span class="sxs-lookup"><span data-stu-id="e49e3-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="e49e3-110">Назначение стоимости единицы измерения в строке контракта на основе продукта позволяет учесть разные затраты на продукт для каждой продажи единицы.</span><span class="sxs-lookup"><span data-stu-id="e49e3-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="e49e3-111">Хотя это не всегда необходимо, существуют определенные сценарии, в которых стоимость продукта может быть снижена поставщиком для клиента.</span><span class="sxs-lookup"><span data-stu-id="e49e3-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="e49e3-112">Рассмотрим следующий сценарий:</span><span class="sxs-lookup"><span data-stu-id="e49e3-112">Consider the following scenario:</span></span>

<span data-ttu-id="e49e3-113">Fabrikam Robotics устанавливает роботизированные манипуляторы на сборочных линиях корпорации Adatum Corporation.</span><span class="sxs-lookup"><span data-stu-id="e49e3-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="e49e3-114">Fabrikam предоставляет услуги по установке, но роботизированные манипуляторы закупаются у компании Trey Research.</span><span class="sxs-lookup"><span data-stu-id="e49e3-114">Fabrikam provides installation services but the robotic arms are procured from Trey Research.</span></span> <span data-ttu-id="e49e3-115">Если установка роботизированных манипуляторов в корпорации Adatum Corporation откроет новую вертикаль отрасли производства для роботизированных манипуляторов компании Trey Research, эта компания может предложить Fabrikam особую скидку на эту сделку.</span><span class="sxs-lookup"><span data-stu-id="e49e3-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="e49e3-116">В этом случае Fabrikam создает строку контракта на основе продукта для Robotic Arms и вводит стоимость за единицу для этого контракта, которая отличается от стандартной стоимости роботизированного манипулятора Trey Research.</span><span class="sxs-lookup"><span data-stu-id="e49e3-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms and inputs a per unit cost for this contract that is different from the standard cost of robotic arms from Trey Research.</span></span>
