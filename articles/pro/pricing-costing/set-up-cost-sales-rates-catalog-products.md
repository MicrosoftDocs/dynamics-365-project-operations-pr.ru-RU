---
title: Настройка ставок себестоимости и продаж для продуктов из каталога — облегченное развертывание
description: Эта тема предоставляет информацию о том, как настроить ставки себестоимости и продаж для позиций в каталоге продуктов.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 135b182af73bdab7a3520589431332ad059ec497
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176717"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="3d4b8-103">Настройка ставок себестоимости и продаж для продуктов из каталога — облегченное развертывание</span><span class="sxs-lookup"><span data-stu-id="3d4b8-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="3d4b8-104">_**Относится к:** развертывание Lite — от сделки до счетов-проформ_</span><span class="sxs-lookup"><span data-stu-id="3d4b8-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="3d4b8-105">Настройка цен для позиций каталога продуктов в Dynamics 365 Project Operations такая же, как и в Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="3d4b8-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="3d4b8-106">Поскольку продукты не могут быть оценены или использованы в проектах в Project Operations, нет необходимости устанавливать цены каталога продуктов в прайс-листах проектов для предложений с расценками и контрактов.</span><span class="sxs-lookup"><span data-stu-id="3d4b8-106">Because products can't be estimated or used on projects in Project Operations, there is no need to set product catalog prices on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="3d4b8-107">Цены по каталогу продуктов должны быть установлены в поле **Цена продукта** предложения с расценками, контракта или организации.</span><span class="sxs-lookup"><span data-stu-id="3d4b8-107">Product catalog prices should be set up in the **Product Price** field of a quote, contract, or account.</span></span> <span data-ttu-id="3d4b8-108">Не устанавливайте цены по каталогу продуктов в прайс-листах проекта для этих сущностей.</span><span class="sxs-lookup"><span data-stu-id="3d4b8-108">Don't set up product catalog prices in the project price lists for these entities.</span></span> <span data-ttu-id="3d4b8-109">Прайс-листы проектов являются эксклюзивными для Project Operations.</span><span class="sxs-lookup"><span data-stu-id="3d4b8-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="3d4b8-110">Существует бизнес-логика для конкретного приложения, которая копирует прайс-листы из предложения с расценками в контракт.</span><span class="sxs-lookup"><span data-stu-id="3d4b8-110">There is application-specific business logic that copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="3d4b8-111">В результате создается прайс-лист по проекту специально для контракта.</span><span class="sxs-lookup"><span data-stu-id="3d4b8-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="3d4b8-112">Операция копирования может задержать процесс выигрыша предложения с расценками, если прайс-лист проекта в предложении с расценками становится слишком большим.</span><span class="sxs-lookup"><span data-stu-id="3d4b8-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="3d4b8-113">Прайс-листы продуктов не копируются для создания настраиваемых прайс-листов по контрактам.</span><span class="sxs-lookup"><span data-stu-id="3d4b8-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="3d4b8-114">Это означает, что прайс-листы продуктов не влияют на производительность процесса реализации предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="3d4b8-114">This means that product price lists don't impact the performance of the quote win process.</span></span>
