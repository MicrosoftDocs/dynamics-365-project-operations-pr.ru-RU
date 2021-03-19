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
ms.openlocfilehash: f0941c549cc38f0938a5819e8cb6ca9912f14790
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274474"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="50ac2-103">Настройка ставок себестоимости и продаж для продуктов из каталога — облегченное развертывание</span><span class="sxs-lookup"><span data-stu-id="50ac2-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="50ac2-104">_**Относится к:** развертывание Lite — от сделки до счетов-проформ_</span><span class="sxs-lookup"><span data-stu-id="50ac2-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="50ac2-105">Настройка цен на позиции каталога продукции в Dynamics 365 Project Operations так же, как и в Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="50ac2-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="50ac2-106">В Project Operations продукты не могут быть оценены или использованы в проектах, поэтому цены из каталога продуктов не нужно указывать в прайс-листах проектов для предложений с расценками и контрактов.</span><span class="sxs-lookup"><span data-stu-id="50ac2-106">In Project Operations, products can't be estimated or used on projects, so product catalog prices don't need to be set on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="50ac2-107">Использовать поле **Цена продукта** предложения с расценкам, контракта или учетной записи для настройки цен из каталога продуктов.</span><span class="sxs-lookup"><span data-stu-id="50ac2-107">Use the **Product Price** field of a quote, contract, or account to set up product catalog prices.</span></span> <span data-ttu-id="50ac2-108">Не указывайте цены из каталога продуктов в прайс-листах проекта.</span><span class="sxs-lookup"><span data-stu-id="50ac2-108">Don't set up product catalog prices in the project price lists.</span></span> <span data-ttu-id="50ac2-109">Прайс-листы проектов являются эксклюзивными для Project Operations.</span><span class="sxs-lookup"><span data-stu-id="50ac2-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="50ac2-110">Бизнес-логика для конкретного приложения копирует прайс-листы из предложения с расценками в контракт.</span><span class="sxs-lookup"><span data-stu-id="50ac2-110">Application-specific business logic copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="50ac2-111">В результате создается прайс-лист по проекту специально для контракта.</span><span class="sxs-lookup"><span data-stu-id="50ac2-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="50ac2-112">Операция копирования может задержать процесс выигрыша предложения с расценками, если прайс-лист проекта в предложении с расценками становится слишком большим.</span><span class="sxs-lookup"><span data-stu-id="50ac2-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="50ac2-113">Прайс-листы продуктов не копируются для создания настраиваемых прайс-листов по контрактам.</span><span class="sxs-lookup"><span data-stu-id="50ac2-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="50ac2-114">Поскольку здесь не используется копирование, это не влияет на производительность обработки предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="50ac2-114">Because there's no copying involved, the performance of the quote process isn't affected.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]