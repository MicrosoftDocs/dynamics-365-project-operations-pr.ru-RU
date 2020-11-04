---
title: Строки возможной сделки на основе продуктов
description: Эта тема предоставляет информацию о позициях строк возможной сделки на основе продукта в Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 17ffcf8dc94d42102115281d281d6b553cf1fa17
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083114"
---
# <a name="product-based-opportunity-lines"></a><span data-ttu-id="9fa06-103">Строки возможной сделки на основе продуктов</span><span class="sxs-lookup"><span data-stu-id="9fa06-103">Product-based opportunity lines</span></span>

<span data-ttu-id="9fa06-104">_**Относится к:** развертывание Lite — от сделки до счетов-проформ_</span><span class="sxs-lookup"><span data-stu-id="9fa06-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9fa06-105">Строки возможной сделки на основе продукта — это позиции строки в возможной сделке.</span><span class="sxs-lookup"><span data-stu-id="9fa06-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="9fa06-106">Эти строки доставляются клиенту как отдельные позиции строки в конечном счете без каких-либо других дополнительных услуг.</span><span class="sxs-lookup"><span data-stu-id="9fa06-106">These lines are delivered to the customer as distinct line items on the eventual invoice without any other value-added services.</span></span> <span data-ttu-id="9fa06-107">Связанные расходы и потребление не отслеживаются для задач любых связанных проектов.</span><span class="sxs-lookup"><span data-stu-id="9fa06-107">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="9fa06-108">Строки на основе продуктов могут быть номенклатурами каталога или вписываемыми продуктами.</span><span class="sxs-lookup"><span data-stu-id="9fa06-108">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="9fa06-109">Большая часть функциональных возможностей строк возможной сделки на основе продуктов соответствует функциональности, предоставляемой приложением Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="9fa06-109">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="9fa06-110">Для получения дополнительной информации о строках возможных сделок на основе продуктов см. раздел [Добавление продуктов в возможную сделку](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span><span class="sxs-lookup"><span data-stu-id="9fa06-110">For more information about product-based opportunity lines, see [Add products to an opportunity](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="9fa06-111">Одна из концепций о строках возможных сделок на основе продуктов, которая характерна для возможных сделок, основанных на проектах, это **Бюджет клиента**.</span><span class="sxs-lookup"><span data-stu-id="9fa06-111">One concept about product-based opportunity lines that is specific to project-based opportunities is **Customer Budget**.</span></span> <span data-ttu-id="9fa06-112">Используйте это поле для отслеживания суммы, которую клиент готов заплатить за позицию строки.</span><span class="sxs-lookup"><span data-stu-id="9fa06-112">Use this field to track the amount the customer is willing to pay for the line item.</span></span>

<span data-ttu-id="9fa06-113">Если для метода дохода в сводке возможной сделки установлено значение **Рассчитывается системой** , значения бюджета клиента по строкам на основе продуктов и проектов суммируются для расчета предполагаемой выручки.</span><span class="sxs-lookup"><span data-stu-id="9fa06-113">If the revenue method of the Opportunity summary is set to **System Calculated** , the customer budget values across product- and project-based lines are summarized to calculate the estimated revenue.</span></span>
