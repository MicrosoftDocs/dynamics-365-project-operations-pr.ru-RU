---
title: Настройка ставок себестоимости и продаж для продуктов из каталога
description: Эта тема предоставляет информацию о том, как настроить ставки себестоимости и продаж для позиций в каталоге продуктов.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5178a9143536bf4b2573403125325017861cdd5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083255"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products"></a><span data-ttu-id="03f9e-103">Настройка ставок себестоимости и продаж для продуктов из каталога</span><span class="sxs-lookup"><span data-stu-id="03f9e-103">Set up cost and sales rates for catalog products</span></span>

<span data-ttu-id="03f9e-104">_**Относится к:** развертывание Lite — от сделки до счетов-проформ_</span><span class="sxs-lookup"><span data-stu-id="03f9e-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="03f9e-105">Настройка цен для позиций каталога продуктов в Dynamics 365 Project Operations такая же, как и в Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="03f9e-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="03f9e-106">Поскольку продукты не могут быть оценены или использованы в проектах в Project Operations, нет необходимости устанавливать цены каталога продуктов в прайс-листах проектов для предложений с расценками и контрактов.</span><span class="sxs-lookup"><span data-stu-id="03f9e-106">Because products can't be estimated or used on projects in Project Operations, there is no need to set product catalog prices on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="03f9e-107">Цены по каталогу продуктов должны быть установлены в поле **Цена продукта** предложения с расценками, контракта или организации.</span><span class="sxs-lookup"><span data-stu-id="03f9e-107">Product catalog prices should be set up in the **Product Price** field of a quote, contract, or account.</span></span> <span data-ttu-id="03f9e-108">Не устанавливайте цены по каталогу продуктов в прайс-листах проекта для этих сущностей.</span><span class="sxs-lookup"><span data-stu-id="03f9e-108">Don't set up product catalog prices in the project price lists for these entities.</span></span> <span data-ttu-id="03f9e-109">Прайс-листы проектов являются эксклюзивными для Project Operations.</span><span class="sxs-lookup"><span data-stu-id="03f9e-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="03f9e-110">Существует бизнес-логика для конкретного приложения, которая копирует прайс-листы из предложения с расценками в контракт.</span><span class="sxs-lookup"><span data-stu-id="03f9e-110">There is application-specific business logic that copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="03f9e-111">В результате создается прайс-лист по проекту специально для контракта.</span><span class="sxs-lookup"><span data-stu-id="03f9e-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="03f9e-112">Операция копирования может задержать процесс выигрыша предложения с расценками, если прайс-лист проекта в предложении с расценками становится слишком большим.</span><span class="sxs-lookup"><span data-stu-id="03f9e-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="03f9e-113">Прайс-листы продуктов не копируются для создания настраиваемых прайс-листов по контрактам.</span><span class="sxs-lookup"><span data-stu-id="03f9e-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="03f9e-114">Это означает, что прайс-листы продуктов не влияют на производительность процесса реализации предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="03f9e-114">This means that product price lists don't impact the performance of the quote win process.</span></span>
