---
title: Настройка ставок себестоимости и продаж для продуктов из каталога — облегченное развертывание
description: Эта тема предоставляет информацию о том, как настроить ставки себестоимости и продаж для позиций в каталоге продуктов.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5e851193df8151821e112e01a9f33df5afee7df7
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764575"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="fc4df-103">Настройка ставок себестоимости и продаж для продуктов из каталога — облегченное развертывание</span><span class="sxs-lookup"><span data-stu-id="fc4df-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="fc4df-104">_**Относится к:** развертывание Lite — от сделки до счетов-проформ_</span><span class="sxs-lookup"><span data-stu-id="fc4df-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="fc4df-105">Настройка цен на позиции каталога продукции в Dynamics 365 Project Operations так же, как и в Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="fc4df-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="fc4df-106">В Project Operations продукты не могут быть оценены или использованы в проектах, поэтому цены из каталога продуктов не нужно указывать в прайс-листах проектов для предложений с расценками и контрактов.</span><span class="sxs-lookup"><span data-stu-id="fc4df-106">In Project Operations, products can't be estimated or used on projects, so product catalog prices don't need to be set on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="fc4df-107">Использовать поле **Цена продукта** предложения с расценкам, контракта или учетной записи для настройки цен из каталога продуктов.</span><span class="sxs-lookup"><span data-stu-id="fc4df-107">Use the **Product Price** field of a quote, contract, or account to set up product catalog prices.</span></span> <span data-ttu-id="fc4df-108">Не указывайте цены из каталога продуктов в прайс-листах проекта.</span><span class="sxs-lookup"><span data-stu-id="fc4df-108">Don't set up product catalog prices in the project price lists.</span></span> <span data-ttu-id="fc4df-109">Прайс-листы проектов являются эксклюзивными для Project Operations.</span><span class="sxs-lookup"><span data-stu-id="fc4df-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="fc4df-110">Бизнес-логика для конкретного приложения копирует прайс-листы из предложения с расценками в контракт.</span><span class="sxs-lookup"><span data-stu-id="fc4df-110">Application-specific business logic copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="fc4df-111">В результате создается прайс-лист по проекту специально для контракта.</span><span class="sxs-lookup"><span data-stu-id="fc4df-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="fc4df-112">Операция копирования может задержать процесс выигрыша предложения с расценками, если прайс-лист проекта в предложении с расценками становится слишком большим.</span><span class="sxs-lookup"><span data-stu-id="fc4df-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="fc4df-113">Прайс-листы продуктов не копируются для создания настраиваемых прайс-листов по контрактам.</span><span class="sxs-lookup"><span data-stu-id="fc4df-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="fc4df-114">Поскольку здесь не используется копирование, это не влияет на производительность обработки предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="fc4df-114">Because there's no copying involved, the performance of the quote process isn't affected.</span></span>
