---
title: Строки возможной сделки на основе продуктов — облегченное развертывание
description: Эта тема предоставляет информацию о позициях строк возможной сделки на основе продукта в Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7865da682ae607f017bf59ce1ae1addc9fefa60b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994512"
---
# <a name="product-based-opportunity-lines---lite"></a><span data-ttu-id="6ae75-103">Строки возможной сделки на основе продуктов — облегченное развертывание</span><span class="sxs-lookup"><span data-stu-id="6ae75-103">Product-based opportunity lines - lite</span></span>

<span data-ttu-id="6ae75-104">_**Относится к:** развертывание Lite — от сделки до счетов-проформ_</span><span class="sxs-lookup"><span data-stu-id="6ae75-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6ae75-105">Строки возможной сделки на основе продукта — это позиции строки в возможной сделке.</span><span class="sxs-lookup"><span data-stu-id="6ae75-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="6ae75-106">Эти отдельные элементы строки включаются в окончательный счет, который предоставляется клиенту.</span><span class="sxs-lookup"><span data-stu-id="6ae75-106">These distinct line items are on the eventual invoice that is provided to the customer.</span></span> <span data-ttu-id="6ae75-107">В счете не указаны другие дополнительные услуги.</span><span class="sxs-lookup"><span data-stu-id="6ae75-107">The invoice doesn't include any other additional services.</span></span> <span data-ttu-id="6ae75-108">Связанные расходы и потребление не отслеживаются для задач любых связанных проектов.</span><span class="sxs-lookup"><span data-stu-id="6ae75-108">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="6ae75-109">Строки на основе продуктов могут быть номенклатурами каталога или вписываемыми продуктами.</span><span class="sxs-lookup"><span data-stu-id="6ae75-109">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="6ae75-110">Большая часть функциональных возможностей строк возможной сделки на основе продуктов соответствует функциональности, предоставляемой приложением Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="6ae75-110">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="6ae75-111">Для получения дополнительной информации о строках возможных сделок на основе продуктов см. раздел [Добавление продуктов в возможную сделку](/dynamics365/sales-enterprise/add-products-opportunity).</span><span class="sxs-lookup"><span data-stu-id="6ae75-111">For more information about product-based opportunity lines, see [Add products to an opportunity](/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="6ae75-112">**Бюджет клиента** — это концепция, характерная для строк возможных сделок на основе проектов.</span><span class="sxs-lookup"><span data-stu-id="6ae75-112">**Customer budget** is a concept that is specific to project-based opportunity lines.</span></span> <span data-ttu-id="6ae75-113">Поле **Бюджет клиента** отслеживает сумму, которую клиент готов заплатить за товар.</span><span class="sxs-lookup"><span data-stu-id="6ae75-113">The **Customer budget** field tracks the amount the customer is willing to pay for the item.</span></span>

<span data-ttu-id="6ae75-114">Когда в сводке по возможным сделкам используется метод выручки **Рассчитывается системой**, значения бюджета клиента по строкам возможной сделки суммируются для расчета предполагаемой выручки.</span><span class="sxs-lookup"><span data-stu-id="6ae75-114">When the revenue method of the Opportunity summary is **System Calculated**, the customer budget values across the opportunity lines are summarized to calculate the estimated revenue.</span></span> 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]