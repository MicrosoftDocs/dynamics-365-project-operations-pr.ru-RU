---
title: Строки возможной сделки на основе продуктов — облегченное развертывание
description: Эта тема предоставляет информацию о позициях строк возможной сделки на основе продукта в Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b826bf3a1320eee2758af7a094e9f1c2eac6a119
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764970"
---
# <a name="product-based-opportunity-lines---lite"></a><span data-ttu-id="175f2-103">Строки возможной сделки на основе продуктов — облегченное развертывание</span><span class="sxs-lookup"><span data-stu-id="175f2-103">Product-based opportunity lines - lite</span></span>

<span data-ttu-id="175f2-104">_**Относится к:** развертывание Lite — от сделки до счетов-проформ_</span><span class="sxs-lookup"><span data-stu-id="175f2-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="175f2-105">Строки возможной сделки на основе продукта — это позиции строки в возможной сделке.</span><span class="sxs-lookup"><span data-stu-id="175f2-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="175f2-106">Эти отдельные элементы строки включаются в окончательный счет, который предоставляется клиенту.</span><span class="sxs-lookup"><span data-stu-id="175f2-106">These distinct line items are on the eventual invoice that is provided to the customer.</span></span> <span data-ttu-id="175f2-107">В счете не указаны другие дополнительные услуги.</span><span class="sxs-lookup"><span data-stu-id="175f2-107">The invoice doesn't include any other additional services.</span></span> <span data-ttu-id="175f2-108">Связанные расходы и потребление не отслеживаются для задач любых связанных проектов.</span><span class="sxs-lookup"><span data-stu-id="175f2-108">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="175f2-109">Строки на основе продуктов могут быть номенклатурами каталога или вписываемыми продуктами.</span><span class="sxs-lookup"><span data-stu-id="175f2-109">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="175f2-110">Большая часть функциональных возможностей строк возможной сделки на основе продуктов соответствует функциональности, предоставляемой приложением Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="175f2-110">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="175f2-111">Для получения дополнительной информации о строках возможных сделок на основе продуктов см. раздел [Добавление продуктов в возможную сделку](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span><span class="sxs-lookup"><span data-stu-id="175f2-111">For more information about product-based opportunity lines, see [Add products to an opportunity](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="175f2-112">**Бюджет клиента** — это концепция, характерная для строк возможных сделок на основе проектов.</span><span class="sxs-lookup"><span data-stu-id="175f2-112">**Customer budget** is a concept that is specific to project-based opportunity lines.</span></span> <span data-ttu-id="175f2-113">Поле **Бюджет клиента** отслеживает сумму, которую клиент готов заплатить за товар.</span><span class="sxs-lookup"><span data-stu-id="175f2-113">The **Customer budget** field tracks the amount the customer is willing to pay for the item.</span></span>

<span data-ttu-id="175f2-114">Когда в сводке по возможным сделкам используется метод выручки **Рассчитывается системой**, значения бюджета клиента по строкам возможной сделки суммируются для расчета предполагаемой выручки.</span><span class="sxs-lookup"><span data-stu-id="175f2-114">When the revenue method of the Opportunity summary is **System Calculated**, the customer budget values across the opportunity lines are summarized to calculate the estimated revenue.</span></span> 

